---
title: 西瓜视频播放器 一款带解析器、能节省流量的HTML5视频播放器
date: 2019-05-19
categories: ['share']
tags: [西瓜视频播放器,HTML5视频播放器,H5视频播放器]
url: /share/xgplayer.html
slug: xgplayer
---
西瓜播放器是 字节跳动出品的 html5播放器，被应用在了很多场景如：抖音、西瓜视频、火山视频等头条系产品中。


<!--more-->


## 示例：
演示视频如未加载，请重新刷新页面。演示支持0.5到100倍速度播放，微信内联播放，微信内全屏播放，自定义视频加载logo，视频加载页加载特效，自定义视频时间等。

<br>
<div id="mse"></div>
<script src="//cdn.jsdelivr.net/npm/xgplayer@1.1.4/browser/index.js" charset="utf-8"></script>
      <script>
      let player = new Player({
        "id": "mse",
        "url": "https://pro-file.xiaoheiban.cn/201905/1558245667000_87679.mp4",
        "playsinline": true,
        "whitelist": [
                ""
        ],
        "fluid": true,
        poster:"https://pro-file.xiaoheiban.cn/201905/1558246773000_35321.png",
        "playbackRate": [
                0.5,
                1,
                2,
                4,
                8,
                10,
                20,
                50,
                100
        ],
        "enterLogo": {
                "url": "https://wrdan.com/usr/themes/jan/images/logo.png",
                "width": 80,
                "height": 50
        },
        "enterBg": {
                "color": "rgba(0,0,0,0.87)"
        },
        "enterTips": {
                "background": "linear-gradient(to right, rgba(0,0,0,0.87), #2bbc8a, rgb(86, 248, 118), #2bbc8a, rgba(0,0,0,0.87))"
        },
        "x5-video-player-fullscreen": "true",
        "x5-video-player-type": "h5",
        "x5-video-orientation": "landscape",
        "keyShortcut": "on"
      });
</script>

## 官网

[https://h5player.bytedance.com/](https://h5player.bytedance.com)