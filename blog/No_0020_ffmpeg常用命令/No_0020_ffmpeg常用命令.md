# ffmpeg常用命令

## 放大声音

**放大为当前音量的n倍**

例如放大2倍 如下

```bash
ffmpeg -i input.aac -filter:a "volume=2" output.aac
```

## 音频和视频同时2倍速

``` bash
ffmpeg -i test.mp4 -filter_complex "[0:v]setpts=0.5*PTS[v];[0:a]atempo=2.0[a]" -map "[v]" -map "[a]" test-2.mp4
```
