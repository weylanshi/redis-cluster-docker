# 使用docker搭建redis集群

使用docker-compse搭建，可以进每个节点下的dockerfile查看具体配置
集群槽分配使用redis-cli --cluster create xxx
redis-trib.rb 脚本是redis 5.0以前使用的，已废弃使用

运行步骤
1. dcoker-compose up  // 运行所有节点
2. sh start_slave.sh  // 修改脚本中的ip 为本地ip 再运行，等待redis槽分配完毕 