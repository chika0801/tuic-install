## TUIC安装指南

- 下载 [TUIC](https://github.com/EAimTY/tuic/releases)
- 程序 `/root/tuic`
- 配置 `/root/tuic_config.json`
- 证书 `/root/fullchain.cer`
- 私钥 `/root/private.key`
- systemctl文件 `/etc/systemd/system/tuic.service`


```
chmod +x /root/tuic
```

```
systemctl daemon-reload && systemctl enable tuic
```

```
systemctl start tuic
```

```
systemctl status tuic
```

- 查看日志 `journalctl -u tuic --output cat -e`
- 实时日志 `journalctl -u tuic --output cat -f`

官方文档 [Server](https://github.com/EAimTY/tuic/blob/dev/README.md#server) [Client](https://github.com/EAimTY/tuic/blob/dev/README.md#client)

## v2rayN配置指南

<details><summary>点击查看详细步骤</summary> 

![1](https://user-images.githubusercontent.com/88967758/192556695-3b62d99a-8dee-46b8-b39a-0f13888e14fc.jpg)

![2](https://user-images.githubusercontent.com/88967758/192556731-b13c11cd-2bda-4f38-90c5-ecac77c27eb9.jpg)

![3](https://user-images.githubusercontent.com/88967758/192125638-3d015582-6fdb-48f7-93fa-05626993a7ea.jpg)

</details>

## SagerNet配置指南

<details><summary>点击查看详细步骤</summary> 

![sagernet](https://user-images.githubusercontent.com/88967758/192247392-a4e6756c-c829-4ba6-a96f-ca39e9b163f9.jpg)

</details>
