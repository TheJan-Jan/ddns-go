## Docker中使用

- 不挂载主机目录, 删除容器同时会删除配置

  ```bash
  # host模式, 同时支持IPv4/IPv6, Liunx系统推荐
  docker run -d --name ddns-go --restart=always --net=host jeessy/ddns-go
  # 桥接模式, 只支持IPv4, Mac/Windows系统推荐
  docker run -d --name ddns-go --restart=always -p 9876:9876 jeessy/ddns-go
  ```
