# instaloader--批量下载ins照片

## 准备工作

+ 安装python环境
+ 安装pip
+ 网络能够访问Instagram

## 安装instaloader

```bash
pip3 install instaloader
```

## 使用instaloader下载ins上的照片

```bash
instaloader 用户名
```

这样该用户名下的照片和相关信息就会被下载下来了

## 只下载照片

```bash
instaloader --no-metadata-json --no-captions 用户名
```

## 下载指定日期内的照片

```bash
instaloader --post-filter="date_utc >= datetime (2020,6,1)"
```

