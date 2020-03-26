# 一个下载CNTV（央视网视频）特定节目的python程序

## 背景

之前在b站转载视频的时候发现央视网有很多小时候在电视上看到的节目  于是希望把这些节目转载到b站   之前在b站转载视频的时候发现央视网有很多小时候在电视上看到的节目

于是希望把这些节目转载到b站   但是每个节目都有很多集例如城市之间这个节目集数很多    一个一个下载在太麻烦了    于是我编写了一个程序

利用这个程序下载央视网的一些节目实现批量下载 方便了我转载到b站  但是后来b站不允许此类转载没通过审核  我这个程序后来也就没有再使用

我现在发到这个博客上记录一下

## 准备工作

首先你需要在你自己的电脑上安装Python的环境我这里使用的是python3并且安装第3方库 

BeautifulSoup

requests

youtube-dl

## python程序

```python
#coding=utf-8
import io
import sys
import os
from  bs4 import BeautifulSoup
import requests
#import retry
import time
qian_url = 'http://tv.cntv.cn/videoset/c10556/page/1'
import youtube_dl
sys.stdout = io.TextIOWrapper(sys.stdout.buffer,encoding='utf-8')         #改变标准输出的默认编码

j = 1
while (j < 2 ):
    full_url = qian_url
    j = j+1

    web_data = requests.get(full_url)
    soup = BeautifulSoup(web_data.text,'lxml')
    #print(soup)
    videourl = soup.select('div > ul > li > a ')
    #print(videourl)
    #time.sleep(2)
    fanzhuan=list(reversed(videourl[:12]))#12代表前十二个视频
    #print(fanzhuan)

    for l in videourl[0:12]:
        o = l.get('href')
        #print(o)
        nowurl="http://tv.cntv.cn"+o
        os.system(command='youtube-dl '+nowurl)

```

## 运行

安装好这些第3方库之后你只需要把Python程序中的节目地址换成你需要下载的节目网址即可

然后运行Python程序这样他就会自动把那一个页面的所有节目都下载下来 

## 运行效果

![colab运行CNTV爬虫](https://github.com/tothepythonmoon/2badaoblog/blob/master/blog/No_0013_%E4%B8%80%E4%B8%AA%E4%B8%8B%E8%BD%BDCNTV%EF%BC%88%E5%A4%AE%E8%A7%86%E7%BD%91%E8%A7%86%E9%A2%91%EF%BC%89%E7%89%B9%E5%AE%9A%E8%8A%82%E7%9B%AE%E7%9A%84python%E7%A8%8B%E5%BA%8F/colab%E8%BF%90%E8%A1%8CCNTV%E7%88%AC%E8%99%AB.png?raw=true)

---

---

![CNTV购物街截图](https://github.com/tothepythonmoon/2badaoblog/blob/master/blog/No_0013_%E4%B8%80%E4%B8%AA%E4%B8%8B%E8%BD%BDCNTV%EF%BC%88%E5%A4%AE%E8%A7%86%E7%BD%91%E8%A7%86%E9%A2%91%EF%BC%89%E7%89%B9%E5%AE%9A%E8%8A%82%E7%9B%AE%E7%9A%84python%E7%A8%8B%E5%BA%8F/CNTV%E8%B4%AD%E7%89%A9%E8%A1%97%E6%88%AA%E5%9B%BE.png?raw=true)
