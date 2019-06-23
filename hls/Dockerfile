FROM jrottenberg/ffmpeg
ENTRYPOINT echo
CMD  -listen 1 -i rtmp://rtmp:1935/live/1234 \
    -c:v libx264 -crf 21 -preset veryfast \
    -c:a aac -b:a 128k -ac 2 \
    -f hls -hls_time 4 -hls_playlist_type event stream.m3u8 
