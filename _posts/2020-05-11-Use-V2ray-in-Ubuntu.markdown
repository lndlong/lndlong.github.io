---
layout: post
title:  "Use V2ray in Ubuntu"
date:   2020-05-11 22:43:30 +0800
---

#Download   
Download by: https://github.com/v2ray/v2ray-core/releases   
AND https://install.direct/go.sh copy to [touch go.sh] file
#Install   
then in same folder running this command
:     sudo bash go.sh --local ./v2ray-linux-64*.zip

#Configuration
emacs /etc/v2ray/config.json  to change configuration           //copy windows OS config.json use Xftp send

change local netword manual -> socks host -> 127.0.0.1:10808    //this is used by chromium
like up step, sreach "setting" in firefox find "network setting" and edit socks5 like up step.
#Use v2ray
## 启动            //may be use by master
systemctl start v2ray
## 停止
systemctl stop v2ray
## 重启
systemctl restart v2ray
## 开机自启
systemctl enable v2ray
