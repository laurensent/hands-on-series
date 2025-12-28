# Hands-on Series TODO

> **Recommended Order**: ThreadPool -> Pool -> Cache -> RateLimiter -> Spring -> RPC -> MQ -> KV
>
> From simple to complex. Later projects can reuse earlier components (e.g., RPC uses thread pool, MQ uses storage design).

---

## Hands-on ThreadPool

### 线程池核心

- [ ] ThreadPoolExecutor - 核心线程池实现

- [ ] 核心线程数 / 最大线程数 / 队列容量

- [ ] 四种拒绝策略（Abort/Discard/CallerRuns/DiscardOldest）

- [ ] 线程工厂（命名、优先级、守护线程）

- [ ] 优雅关闭（shutdown / shutdownNow）

### 任务队列

- [ ] ArrayBlockingQueue - 有界阻塞队列

- [ ] LinkedBlockingQueue - 链式阻塞队列

- [ ] SynchronousQueue - 直接提交

- [ ] PriorityBlockingQueue - 优先级队列

### 扩展功能

- [ ] 动态调整参数

- [ ] 监控指标（活跃线程数、队列大小、完成任务数）

- [ ] 任务超时取消

---

## Hands-on Pool

### 连接池

- [ ] 池化接口设计

- [ ] 连接创建/销毁

- [ ] 空闲连接管理

- [ ] 最大/最小连接数控制

- [ ] 连接有效性检测

- [ ] 等待超时机制

---

## Hands-on Cache

### 本地缓存

- [ ] Cache 接口设计

- [ ] LRU 淘汰策略

- [ ] LFU 淘汰策略

- [ ] 过期时间支持

- [ ] 并发安全

---

## Hands-on RateLimiter

### 限流算法

- [ ] 固定窗口计数器

- [ ] 滑动窗口计数器

- [ ] 漏桶算法（Leaky Bucket）

- [ ] 令牌桶算法（Token Bucket）

### 分布式限流

- [ ] Redis + Lua 实现

- [ ] 集群限流策略

---

## Hands-on Spring

### IoC Container

- [ ] BeanDefinition - Bean 定义信息

- [ ] BeanFactory - 基础容器接口

- [ ] DefaultBeanFactory - 默认实现，支持单例/原型

- [ ] 构造器注入

- [ ] Setter 注入

- [ ] @Autowired 字段注入

- [ ] 循环依赖处理（三级缓存）

- [ ] BeanPostProcessor - Bean 后置处理器

- [ ] ApplicationContext - 高级容器

### AOP

- [ ] JDK 动态代理实现

- [ ] CGLIB 代理实现

- [ ] PointCut - 切点表达式解析

- [ ] Advice - 通知类型（Before/After/Around）

- [ ] Advisor - 切面组装

- [ ] AOP 与 IoC 整合

### MVC

- [ ] DispatcherServlet - 核心分发器

- [ ] HandlerMapping - 请求映射

- [ ] HandlerAdapter - 处理器适配

- [ ] @Controller / @RequestMapping 注解

- [ ] 参数解析器（PathVariable/RequestParam/RequestBody）

- [ ] 返回值处理器（ViewResolver/JSON）

- [ ] 拦截器链

### JDBC/ORM

- [ ] JdbcTemplate 封装

- [ ] RowMapper 结果映射

- [ ] 事务管理器

- [ ] @Transactional 声明式事务

- [ ] 事务传播行为

---

## Hands-on RPC

### 通信层

- [ ] 自定义协议设计（魔数/版本/序列化类型/消息类型/请求ID/数据长度）

- [ ] 编解码器（Encoder/Decoder）

- [ ] Netty Server/Client 实现

- [ ] 序列化（JSON/Hessian/Protobuf）

### 服务调用

- [ ] 服务接口定义

- [ ] @RpcService / @RpcReference 注解

- [ ] 动态代理生成客户端 Stub

- [ ] 请求/响应模型

### 注册发现

- [ ] 注册中心接口抽象

- [ ] Zookeeper / Nacos 实现

- [ ] 服务注册/注销/发现

### 高级特性

- [ ] 负载均衡（Random/RoundRobin/ConsistentHash）

- [ ] 超时重试

- [ ] 心跳检测

---

## Hands-on MQ

### 消息模型

- [ ] Topic - 主题

- [ ] Queue - 消息队列

- [ ] Producer / Consumer - 生产者消费者

- [ ] Message - 消息格式设计

### 存储层

- [ ] CommitLog - 顺序写日志

- [ ] ConsumeQueue - 消费队列索引

- [ ] Index - 消息索引

- [ ] 刷盘策略（同步/异步）

### 消费机制

- [ ] Push / Pull 模式

- [ ] 消费位点管理

- [ ] 消息确认（ACK）

- [ ] 消息重试 / 死信队列

---

## Hands-on KV

### 存储引擎

- [ ] MemTable - 内存表（跳表/红黑树实现）

- [ ] WAL - 预写日志，保证持久性

- [ ] SSTable - 有序字符串表，磁盘存储格式

- [ ] LSM-Tree - 日志结构合并树

- [ ] Compaction - 合并压缩策略（Leveled/Tiered）

### 数据结构

- [ ] SkipList - 跳表实现

- [ ] BloomFilter - 布隆过滤器，快速判断 key 不存在

- [ ] Block - 数据块格式设计

- [ ] Index - 索引结构（稀疏索引/块索引）

### 核心 API

- [ ] Get / Put / Delete - 基础操作

- [ ] Scan / Range Query - 范围查询

- [ ] Batch Write - 批量写入

- [ ] Iterator - 迭代器

### 高级特性

- [ ] Snapshot - 快照读

- [ ] Transaction - 事务支持（MVCC）

- [ ] Compression - 数据压缩（Snappy/LZ4）

- [ ] Cache - 块缓存 / 行缓存
