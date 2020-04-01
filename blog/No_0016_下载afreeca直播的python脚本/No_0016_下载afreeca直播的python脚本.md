# 下载afreeca直播的python脚本

## 介绍

afreecaTV是韩国的直播平台 它的直播流使用m3u8格式 利用ffmpeg下载直播流发现 里面的直播流xxx.ts文件只有四个是实时更新的

于是利用循环请求xxx.m3u8的方式获取直播流xxx.ts视频文件的地址并利用youtube-dl将其下载 其中用了现学现卖的多线程

## 代码

```python
import requests
from bs4 import BeautifulSoup
import threading
import os

#利用youtube-dl下载
def xiazai(dz):
    os.system(command='youtube-dl ' + dz)
#模拟浏览器头文件
headers = {
    "User-Agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_14_4) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/72.0.3683.103 Safari/537.36"}
#不停访问直播地址，获取m3u8文件并得到ts的地址
def geturl():
    #请求直播地址
    kk=requests.get('http://live-hls-local-cf.afreecatv.com/livestream-west-03/auth_playlist.m3u8?aid=.A32.7bbT56vyHM9fKZk.csJsI1RW2VeHNHmUaPUq_SjZ7KihDQOUHfdz0dNu6muEimIgZ8S1Hs16GZAo_m8eIbBp2NsxPQCbDns-Shp-6BJh0CC1JoP90BjiKUEeaJCekH6InFTu0R150RFiHhyv',headers=headers)
    #print(kk)
    #处理返回的页面代码
    ooo = BeautifulSoup(kk.text, 'lxml')
    #标签内的就是三个ts地址
    p=ooo.select("body > p")[0]
    #print(p)
    #进行地址切片，这里要注意直播流的序号一位数，两位数，三位数，四位数切片都不同，可以学习正则表达式改进
    #四位数切片【260：339】
    f=p.string[260:339]
    #print(f)
    #拼接出真实的ts地址
    down="http://live-hls-local-cf.afreecatv.com/livestream-west-03/"+f
    print(down)
    #返回下载链接
    return down
#存放ts下载链接的
a=[]
#不停地请求直播地址大概50可以请求到5个hls流文件
for j in range(50000):
    #获取直播ts地址
    dizhi=geturl()
    #创建线程
    threads = []
    #如果下载地址没在存放下载的列表里就利用线程调用youtube-dl下载
    if dizhi not in a:
        t = threading.Thread(target=xiazai, args=(dizhi,))
        t.start()
        threads.append(t)
        #把已经调用youtube-dl下载的ts放到a列表里面
        a.append(dizhi)
#释放线程
for t in threads:
    t.join()
#打印a下载列表
print(a)
```

## 使用这个脚本

你需要从网页获取到直播间的m3u8地址  并把它填写到请求直播地址的位置即可

## 总结

下载的都是直播实时画面 每个视频文件5秒左右 需要后期合并成一个文件
