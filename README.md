# x-ui sw
> **Disclaimer: This project is only for personal learning and communication, please do not use it for illegal purposes, please do not use it in a production environment**


**If you think this project is helpful to you, you may wish to give a** :star2: 

# Features

- System Status Monitoring
- Support multi-user multi-protocol, web page visualization operation
- Supported protocols: vmess, vless, trojan, shadowsocks, dokodemo-door, socks, http
- Support for configuring more transport configurations
- Traffic statistics, limit traffic, limit expiration time
- Customizable xray configuration templates
- Support https access panel (self-provided domain name + ssl certificate)
- Support one-click SSL certificate application and automatic renewal
- For more advanced configuration items, please refer to the panel

# Os support
- Ubuntu 22 or higher version
- Centos|almalinux 9 or higher version
- Debian 12 or higher version


# Install & Upgrade

```
bash <(curl -Ls https://raw.githubusercontent.com/imafaz/x-ui/master/install.sh)
```

## Manual install & upgrade

1. First download the latest compressed package from https://github.com/imafaz/x-ui/releases , generally choose Architecture `amd64`
2. Then upload the compressed package to the server's `/root/` directory and `root` rootlog in to the server with user

> If your server cpu architecture is not `amd64` replace another architecture

```
cd /root/
rm x-ui/ /usr/local/x-ui/ /usr/bin/x-ui -rf
tar zxvf x-ui-amd64.tar.gz
chmod +x x-ui/x-ui x-ui/bin/xray-linux-* x-ui/x-ui.sh
cp x-ui/x-ui.sh /usr/bin/x-ui
cp -f x-ui/x-ui.service /etc/systemd/system/
mv x-ui/ /usr/local/
systemctl daemon-reload
systemctl enable x-ui
systemctl restart x-ui
```


## suggestion system

- CentOS 7+
- Ubuntu 16+
- Debian 8+