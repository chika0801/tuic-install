### 快速安装

#### 服务端

  - 参考 [TUIC 安装指南](https://github.com/chika0801/tuic-install/blob/main/README.md)。

#### Windows 客户端

  - sing-box：参考 [sing-box Windows 客户端使用方法](https://github.com/chika0801/sing-box-examples/blob/main/Tun/README.md)，将 [sing-box Windows 客户端配置](https://github.com/chika0801/sing-box-examples/blob/main/Tun/config_client_windows.json) 进行如下修改。

原内容
```jsonc
        {
            "tag": "proxy",
            // 粘贴你的客户端配置，需要保留 "tag": "proxy",
        },
```

替换为
```jsonc
        {
            "type": "socks",
            "tag": "proxy",
            "server": "127.0.0.1",
            "server_port": 10808
        },
```

  - v2rayN：参考 [v2rayN - V6.X 配置示例](https://github.com/chika0801/tuic-install/blob/main/README.md)，将 [客户端配置](https://raw.githubusercontent.com/chika0801/tuic-install/main/config_client.json) 中的 50001 改为 10808。


