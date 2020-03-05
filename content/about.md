---
title: About
date: 2016-10-21
url: /about.html
# slug: about
---

![gogogo](https://tva1.sinaimg.cn/large/6bdf06f1ly1feixu3c97xj20lo08cdoq.jpg)

#### Hi，这是一个80后奶爸的博客，博客建立在家里DIY的主机上。

博客从 [**2016.10.21**](https://wrdan.com/life/1st.html) 至今已经运行 <span id="htmer_time" style="color: #2d96bd; font-weight: bold;"></span>

> 爱好电影，摄影，懂一点php、js。 总想每天闲下来的时候写些什么，
> 但就是没（tuo）有（yan）时（zheng）间，希望这次能坚持下来。努力，奋斗！*
> 鉴于垃圾、无意义评论太多，特开启评论审核，通过审核才可以发布（审核一般在24小时内）。


### 主机配置：
 - CPU：Intel(R) Celeron(R) CPU J3160 @ 1.60GHz
 - RAM：金士顿（Kingston） 8G DDR3L 1.35V @1600MHz
 - SSD：英特尔（Intel）530 120G 
 - HHD：西数WD 2T企业盘 + 日立HGST 500G
 - 功耗：整机在30W左右

### 主机系统：
 - VMware ESXi 6.5

### 网站环境：
 - CentOS 6.5 + lnmp + typecho

### 联系我
如果有想跟我交流的朋友，欢迎发邮件联系我。😄

📧 [i#wrdan.com](http://mail.qq.com/cgi-bin/qm_share?t=qm_mailme&email=i@wrdan.com)


<script>
function secondToDate(second) {
     if (!second) {
         return 0;
     }
     var time = new Array(0, 0, 0, 0, 0);
     if (second >= 365 * 24 * 3600) {
        time[0] = parseInt(second / (365 * 24 * 3600));
        second %= 365 * 24 * 3600;
    }
    if (second >= 24 * 3600) {
        time[1] = parseInt(second / (24 * 3600));
        second %= 24 * 3600;
    }
    if (second >= 3600) {
        time[2] = parseInt(second / 3600);
        second %= 3600;
    }
    if (second >= 60) {
        time[3] = parseInt(second / 60);
        second %= 60;
    }
    if (second > 0) {
        time[4] = second;
    }
    return time;
};
function setTime() {
         // 博客创建时间秒数，时间格式中，月比较特殊，是从0开始的，所以想要显示5月，得写4才行，如下
         var create_time = Math.round(new Date(Date.UTC(2016, 10, 21, 00, 00, 00)).getTime() / 1000);// 当前时间秒数,增加时区的差异
         var timestamp = Math.round((new Date().getTime() + 8 * 60 * 60 * 1000) / 1000);
         currentTime = secondToDate((timestamp - create_time));
         if (currentTime[0]==0){
             currentTimeHtml = currentTime[1] + '天'+ currentTime[2] + '时' + currentTime[3] + '分' + currentTime[4] + '秒';
         }else{
             currentTimeHtml = currentTime[0] + '年' + currentTime[1] + '天' + currentTime[2] + '时' + currentTime[3] + '分' + currentTime[4] + '秒';
         }
         // 兼容pjax，当htmer_time存在时输出，否则清空计时器
         if (document.getElementById("htmer_time")){
             document.getElementById("htmer_time").innerHTML = currentTimeHtml;
         }else{
              clearInterval(timer);
         }
}
var timer = setInterval(setTime, 1000);
</script>