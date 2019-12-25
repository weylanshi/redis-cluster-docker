# 使用docker搭建redis集群

使用docker-compse搭建，可以进每个节点下的dockerfile查看具体配置
集群槽分配使用redis-cli --cluster create xxx
redis-trib.rb 脚本是redis 5.0以前使用的，已废弃使用

此项目仅用于测试redis集群搭建

运行步骤
1. dcoker-compose up  // 运行所有节点 -d 后台运行
2. docker exec -it [容器id] /bin/bash // 进去其中一个容器
3. redis-cli --cluster create 172.16.238.11:6371 172.16.238.12:6372 172.16.238.13:6373 172.16.238.14:6374 172.16.238.15:6375 172.16.238.16:6376 --cluster-replicas 1  // 使用官方工具搭建分配槽  
4. docker-compose down // 关闭集群
