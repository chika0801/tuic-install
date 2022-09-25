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

![1](https://user-images.githubusercontent.com/88967758/192125636-756da577-f9ec-453e-a5ac-812b7da57009.jpg)

![2](https://user-images.githubusercontent.com/88967758/192125637-fec41d38-4867-4218-a128-d5b36daa0d4b.jpg)

![3](https://user-images.githubusercontent.com/88967758/192125638-3d015582-6fdb-48f7-93fa-05626993a7ea.jpg)

</details>

## v2rayN配置指南

<details><summary>点击查看详细步骤</summary> 

![sagernet](https://user-images.githubusercontent.com/88967758/192125877-25eb2878-451e-471a-a530-9b75e27f3b1e.jpg)

</details>
