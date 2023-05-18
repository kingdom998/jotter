# docker 常用命令

* docker容器内访问宿主机host服务, 绑定host后，其他容器就可以直接使用 host.docker.internal 代替 ip 访问所建的容器
```
docker run -d -p 3000:3000 --add-host=host.docker.internal:host-gateway --name gf grafana/grafana                        
```
