#
IPod Touch
```
ffmpeg -i source.mp4 -vcodec libx264 -profile:v main -level 3.1 -preset medium -crf 23 -x264-params ref=4 -acodec copy -movflags +faststart destination.mp4
```

