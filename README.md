# RTSP to WebRTC

## Embed your Cameras RTSP Stream via WebRTC

> This is a clone of the [RTSPtoWebRTC Project deepch](https://github.com/deepch/RTSPtoWebRTC)!


Steps to run this project:

1. Install [Go for LINUX, Windows or macOS](https://golang.org/doc/install?download)

2. Download /Clone this Repository [RTSPtoWebRTC](https://github.com/mpolinowski/RTSPtoWebRTC)

3. Enter the folder you downloaded the code into and edit the file `./config.json` to add your personal IP camera URLs, e.g.:


```json
}
   "INSTAR_8015_FHD": {
      "on_demand": true,
      "url": "rtsp://admin:instar@192.168.2.77/11"
   },
    "INSTAR_9020_FHD": {
      "on_demand": true,
      "url": "rtsp://admin:instar@192.168.2.117/12"
   },
    "INSTAR_IN-7011_HD": {
      "on_demand": true,
      "url": "rtsp://admin:instar@192.168.2.63/11"
   }
}
```


4. Now run the following command to run the application in development mode:

```bash
$ go run .
```

or build and run your application:

```bash
$ go build .
$ ./RTSPtoWebRTC
```

> The build command will build the binary release version of your Go application. This file will be called `RTSPtoWebRTC` - without an extension - on LINUX and can be executed from your command line or through a script (make sure that the file is made executable before running). If you run the command on Windows, you end up with an `RTSPtoWebRTC.exe` file that you can execute by double-clicking.


4. Open your Web browser and visit the following URL:


```bash
http://127.0.0.1:8888
```


---

![RTSPtoWebRTC](./webrtc_02.gif)

---


################ ORIGINAL README #####################

---

# RTSPtoWebRTC

RTSP Stream to WebBrowser over WebRTC based on Pion

full native! not use ffmpeg or gstreamer

if you need RTSPtoWSMP4f use https://github.com/deepch/RTSPtoWSMP4f

## Team

Deepch - https://github.com/deepch streaming developer

Dmitry - https://github.com/vdalex25 web developer

Now test work on (chrome, safari, firefox) no MAC OS

![RTSPtoWebRTC image](doc/demo4.png)

## Installation
1.
```bash
$ export GO111MODULE=on
$ go get github.com/deepch/RTSPtoWebRTC
```
2.
```bash
$ cd ~/go/src/github.com/deepch/RTSPtoWebRTC
```
3.
```bash
$ go run .
```
or
```bash
$ go build .
$ ./RTSPtoWebRTC
```
4.
```bash
open web browser http://127.0.0.1:8083 work chrome, safari, firefox
```

## Configuration

### Edit file config.json

format:

```bash
{
  "server": {
    "http_port": ":8083"
  },
  "streams": {
    "demo1": {
      "url": "rtsp://170.93.143.139/rtplive/470011e600ef003a004ee33696235daa"
    },
    "demo2": {
      "url": "rtsp://170.93.143.139/rtplive/470011e600ef003a004ee33696235daa"
    },
    "demo3": {
      "url": "rtsp://170.93.143.139/rtplive/470011e600ef003a004ee33696235daa"
    }
  }
}
```

## Limitations

Video Codecs Supported: H264

Audio Codecs Supported: pcm alaw and pcm mulaw 

[![paypal.me/AndreySemochkin](https://ionicabizau.github.io/badges/paypal.svg)](https://www.paypal.me/AndreySemochkin) - You can make one-time donations via PayPal. I'll probably buy a ~~coffee~~ tea. :tea:
