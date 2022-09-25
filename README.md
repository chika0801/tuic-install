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
