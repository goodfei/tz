# 搭梯子
## vps
https://github.com/mack-a/v2ray-agent
```
wget -P /root -N --no-check-certificate "https://raw.githubusercontent.com/mack-a/v2ray-agent/master/install.sh" && chmod 700 /root/install.sh && /root/install.sh
```
我使用的 VLESS+TCP+TLS_Vision
【vasma】命令打开脚本

## 客户端
- mac
  https://github.com/yanue/V2rayU/releases
- ios
  Shadowrocket
- windows
  https://github.com/2dust/v2rayN/releases
- android
  https://github.com/2dust/v2rayNG/releases

## mac V2rayU flow 不支持 xtls-rprx-vision 解决办法
```
cd ~

# mac Intel
wget https://github.com/XTLS/Xray-core/releases/download/v1.8.0/Xray-macos-64.zip
unzip Xray-macos-64.zip -d ~/Xray

 # mac m1
wget https://github.com/XTLS/Xray-core/releases/download/v1.8.0/Xray-macos-arm64-v8a.zip
unzip Xray-macos-arm64-v8a.zip -d ~/Xray

cp -r ~/.V2rayU/v2ray-core ~/.V2rayU/v2ray-core-bak
mv ~/Xray/* ~/.V2rayU/v2ray-core/
cp ~/.V2rayU/v2ray-core/xray ~/.V2rayU/v2ray-core/v2ray # Don't forget this
sudo chmod 777 ~/.V2rayU/v2ray-core
```

Cloudflare WARP 模式
下载脚本
```
wget git.io/warp.sh
chmod +x warp.sh
```

运行脚本 中文菜单
```./warp.sh menu```

先后执行如下安装：
- 1 - 安装 Cloudflare WARP 官方客户端
- 4 - 安装 WireGuard 相关组件
- 7 - 自动配置 WARP WireGuard 双栈全局网络
使用 ./warp.sh status 来查看服务的状态，如果正常的话，会显示如下的信息。
```
WireGuard	: Running
IPv4 Network	: WARP
IPv6 Network	: WARP
```
使用 curl ipinfo.io 命令来检查你的 IP 地址，如果显示的是 Cloudflare 的 IP 地址，那么恭喜你，你已经成功了。
