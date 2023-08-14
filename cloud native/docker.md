* mac 启动 docker (因为 docker-desktop 有版权问题，现使用 [colima](https://github.com/abiosoft/colima) 开源工具)
```
brew install colima # 安装 colima
colima start --network-address # 启动（network-address 参数实现了端口的绑定，没有此参数 docker -p 端口绑定无效绑定）
```