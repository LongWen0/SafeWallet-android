2022年3月31日版本号v0.24.01

1.增加vpn设置入口，vpn连接状态显示，vpn和tor二选一，或全不选。

2.解决市值排名随机出现未按币种市值排序。

3.增加ETH，BNB币收款交易记录显示，解决所有币的交易记录显示刷新问题.

4.解决恢复钱包时ETH，BNB币没有交易记录问题。

5.增加SAFE同步数据块的处理机制，逻辑如下：  

  （1）创建恢复钱包初始化时通过调用api获取种子ip地址缓存；如果调用api失败就用默认ip；api:https://chain.anwang.org/insight-api-safe/utils/address/seed
  
  （2）每次同步数据（创建钱包，恢复钱包，日常数据同步）从缓存数据库中随机取5个种子节点ip,通过发送消息VersionMessage解析其返回信息获取所有查询种子节点的区块高度。
  
  （3）.比对获得各种子节点的区块高度大小，选择区块高度最大连接成功次数多的种子节点进行连接开始同步数据。  
  
6.增加新建钱包时安全中心下区块链的更新方式选择，包括API和blockchain。  


