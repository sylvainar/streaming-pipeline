# OBS

Install on linux

```
apt install ffmpeg

add-apt-repository ppa:obsproject/obs-studio
apt-get update
apt-get install obs-studio
```

# RTMP

Acts as an RTMP server, distributing content.
  
<https://hub.docker.com/r/tiangolo/nginx-rtmp>

# HLS

Convert the RTMP feed to HLS to facilitate distribution.

```
ffmpeg -listen 1 -i rtmp://streamsource.com/stream01 \
    -c:v libx264 -crf 21 -preset veryfast \
    -c:a aac -b:a 128k -ac 2 \
    -f hls -hls_time 4 -hls_playlist_type event stream.m3u8
```

Source : <https://www.martin-riedl.de/2018/08/24/using-ffmpeg-as-a-hls-streaming-server-part-1/>

# Display

Gonna try this:

<https://github.com/video-dev/hls.js>
