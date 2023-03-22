# 搭梯子
## vps
```
wget -P /root -N --no-check-certificate "https://raw.githubusercontent.com/mack-a/v2ray-agent/master/install.sh" && chmod 700 /root/install.sh && /root/install.sh
```
我使用的 VLESS+TCP+TLS_Vision

## 客户端
mac
https://github.com/yanue/V2rayU/releases
ios
Shadowrocket
windows
https://github.com/2dust/v2rayN/releases
android
https://github.com/2dust/v2rayNG/releases

## mac V2rayU flow 不支持 xtls-rprx-vision 解决办法
```
cd ~

# mac Intel
wget https://github.com/XTLS/Xray-core/releases/download/v1.7.5/Xray-macos-64.zip
unzip Xray-macos-64.zip -d ~/Xray

 # mac m1
wget https://github.com/XTLS/Xray-core/releases/download/v1.7.5/Xray-macos-arm64-v8a.zip
unzip Xray-macos-arm64-v8a.zip -d ~/Xray

cp -r ~/.V2rayU/v2ray-core ~/.V2rayU/v2ray-core-bak
// 这里不对，把 ~/Xray 下文件 cp 到 ~/.V2rayU/v2ray-core
mv -r ~/Xray ~/.V2rayU/v2ray-core
cp ~/.V2rayU/v2ray-core/xray ~/.V2rayU/v2ray-core/v2ray # Don't forget this
sudo chmod 777 ~/.V2rayU/v2ray-core
```
