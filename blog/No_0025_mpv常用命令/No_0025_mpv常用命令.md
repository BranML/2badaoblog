# No_0025_mpv常用命令

## mpv调用ytdl并传递用户名和密码

**实现的功能：直接用mpv播放网站上的视频，并且是需要登录才能看的视频**

```bash
mpv --ytdl-raw-options=username=your_username,password=your_password download_url
```

