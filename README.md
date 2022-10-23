## Docker中使用

- 不挂载主机目录, 删除容器同时会删除配置

  ```bash
  # host模式(推荐)
  docker run -d --name ddns-go --restart=always --net=host boythejan/ddns-go
  # 桥接模式
  docker run -d --name ddns-go --restart=always -p 9876:9876 boythejan/ddns-go
  ```
