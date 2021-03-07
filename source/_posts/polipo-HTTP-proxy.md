---
title: polipo HTTP proxy
date: 2021-03-07 15:09:35
tags:
---
sudo apt-get install polipo
<br>
sudo vim /etc/polipo/config
Add:
socksParentProxy = "127.0.0.1:1080"
socksProxyType = socks5
proxyPort = 8123
<br>
sudo service polipo restart
or sudo systemctl restart polipo
<br>
export http_proxy='' https_proxy=''
export http_proxy='http://127.0.0.1:8123' https_proxy='https://127.0.0.1:8123'
<br>

