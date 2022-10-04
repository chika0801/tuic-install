## TUIC安装指南

1.下载程序
```
curl -sLo /root/tuic https://github.com/EAimTY/tuic/releases/download/0.8.4/tuic-server-0.8.4-x86_64-linux-gnu && chmod +x /root/tuic
```

2.下载服务器配置
```
curl -sLo /root/tuic_config.json https://raw.githubusercontent.com/chika0801/tuic-install/main/config_server.json
```

3.下载systemctl配置文件
```
curl -sLo /etc/systemd/system/tuic.service https://raw.githubusercontent.com/chika0801/tuic-install/main/tuic.service
```

4.上传证书和私钥
将证书文件改名为fullchain.cer，将密钥文件改名为private.key，使用WinSCP连接你的VPS，将它们上传到/root/目录。

5.启动程序
```
systemctl daemon-reload && systemctl enable tuic
```

```
systemctl start tuic
```

```
systemctl status tuic
```

- 下载 [TUIC](https://github.com/EAimTY/tuic/releases)
- 程序 `/root/tuic`
- 配置 `/root/tuic_config.json`
- 证书 `/root/fullchain.cer`
- 私钥 `/root/private.key`
- systemctl配置文件 `/etc/systemd/system/tuic.service`
- 查看日志 `journalctl -u tuic --output cat -e`
- 实时日志 `journalctl -u tuic --output cat -f`

官方文档 [Server](https://github.com/EAimTY/tuic/blob/dev/README.md#server) [Client](https://github.com/EAimTY/tuic/blob/dev/README.md#client)

## v2rayN配置指南

<details><summary>点击查看详细步骤</summary> 

![1](https://user-images.githubusercontent.com/88967758/192556695-3b62d99a-8dee-46b8-b39a-0f13888e14fc.jpg)

![2](https://user-images.githubusercontent.com/88967758/192556731-b13c11cd-2bda-4f38-90c5-ecac77c27eb9.jpg)

![3](https://user-images.githubusercontent.com/88967758/192557055-a91fb74f-0050-4a05-831c-ca795886b8c9.jpg)

</details>

## SagerNet配置指南

<details><summary>点击查看详细步骤</summary> 

![sagernet](https://user-images.githubusercontent.com/88967758/192247392-a4e6756c-c829-4ba6-a96f-ca39e9b163f9.jpg)

</details>
