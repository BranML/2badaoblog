#  No_0007_git命令学习（一）-clone和push

## 从服务器将项目下载到本地

```
git clone https://github.com/chromium/chromium.git
```

**代码解释**

git 代表git命令 clone 代表克隆 https://github.com/xxxxxxxx/xxxxxxx 代表你所要从服务器端下载到本地的项目地址（项目地址获取方式如下图 以chromium为例）

![](https://raw.githubusercontent.com/tothepythonmoon/2badaoblog/master/blog/No_0007_git%E5%91%BD%E4%BB%A4%E5%AD%A6%E4%B9%A0%EF%BC%88%E4%B8%80%EF%BC%89-clone%E5%92%8Cpush/git_clone%E6%8C%89%E9%92%AE.jpg)

## 将本地项目上传到github

1.进入需要上传的项目目录

2.依次使用如下命令

```
git add .
git commit -m "message"
git push origin master
```

**中途会要求你输入github用户名和密码**

**代码解释**

git add . 上传位置为当前项目文件夹下的根目录

git commit -m "message" 上传内容的描述

git push origin master 利用push功能以master身份上传origin分支
