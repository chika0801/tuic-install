## [TUIC](https://github.com/EAimTY/tuic) 安装指南

1. 下载程序（**linux-amd64**）

```
curl -Lo /root/tuic https://github.com/EAimTY/tuic/releases/download/0.8.4/tuic-server-0.8.4-x86_64-linux-musl && chmod +x /root/tuic
```

2. 下载配置

```
curl -Lo /root/tuic_config.json https://raw.githubusercontent.com/chika0801/tuic-install/main/config_server.json
```

3. 下载systemctl配置

```
curl -Lo /etc/systemd/system/tuic.service https://raw.githubusercontent.com/chika0801/tuic-install/main/tuic.service && systemctl daemon-reload
```

4. 上传证书和私钥

- 将证书文件改名为 **fullchain.cer**，将私钥文件改名为 **private.key**，将它们上传到 **/root** 目录

5. 启动程序

```
 systemctl enable --now tuic && sleep 0.2 && systemctl status tuic
```

| 项目 | |
| :--- | :--- |
| 程序 | **/root/tuic** |
| 配置 | **/root/tuic_config.json** |
| 检查 | `/root/tuic -c tuic_config.json` |
| 查看日志 | `journalctl -u tuic --output cat -e` |
| 实时日志 | `journalctl -u tuic --output cat -f` |

## v2rayN - V6.X 配置示例

<details><summary>点击查看</summary>

1. 下载Windows客户端程序[tuic-client-0.8.4-x86_64-windows-msvc.exe](https://github.com/EAimTY/tuic/releases/download/0.8.4/tuic-client-0.8.4-x86_64-windows-msvc.exe)，重命名为tuic.exe，复制到v2rayN\bin\tuic文件夹。

2. 下载客户端配置[config_client.json](https://raw.githubusercontent.com/chika0801/tuic-install/main/config_client.json)，修改chika.example.com为证书中包含的域名，修改10.0.0.1为VPS的IP。

3. 服务器 ——> 添加自定义配置服务器 ——> 浏览 ——> 选择客户端配置 ——> Core类型 tuic ——> Socks端口 50001

![1](https://user-images.githubusercontent.com/88967758/227561846-0f93ca76-0dce-41d3-9232-bd25a29276cf.png)

小技巧：只要证书在有效期内，证书中包含的域名不用解析到VPS的IP。一份证书，在多个VPS上使用。

</details>

## Shadowrocket 配置示例

<details><summary>点击查看</summary><br>

| 选项 | 值 |
| :--- | :--- |
| 类型 | TUIC |
| 地址 | VPS的IP |
| 端口 | 16386 |
| 密码 | chika |
| 模式 | bbr |
| 允许不安全 | 不选 |
| UDP转发 | 选上 |
| SNI | 证书中包含的域名 |
| ALPN | h3 |

</details>
