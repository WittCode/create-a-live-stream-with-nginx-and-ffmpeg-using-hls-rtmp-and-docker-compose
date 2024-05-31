FROM ubuntu:24.04

RUN apt update
RUN apt install -y ffmpeg

WORKDIR /media
COPY YOUR_VIDEO_FILE .

ENTRYPOINT ffmpeg -re -i YOUR_VIDEO_FILE -c:v libx264 -c:a aac -f flv rtmp://nginx-c/hls/my-video