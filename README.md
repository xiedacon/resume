## 谢达 / Xie Da

- 男 / 1995 / 本科 / 华中农业大学

## 个人信息

- 手机：15271883834
- 微信：xiedacon
- Email：xiedacon@qq.com
- GitHub：[https://github.com/xiedacon](https://github.com/xiedacon)
- Blog：[http://www.xiedacon.com](http://www.xiedacon.com)

## 技能清单

- 熟悉 Node.js / TypeScript
- 掌握 Golang / Python / Java
- 熟悉 MySQL/ MongoDB / Redis 相关类库的使用
- 熟悉 Linux / Git / Docker 等必备开发技能
- 熟悉 Thrift / gRPC 协议原理
- 了解 Consul / ZooKeeper / OpenResty

## 工作经历

### 字节跳动 ( Node.js 研发工程师、Golang 研发工程师 ) <span style="float: right;">2020 年 7 月 ~ 今<span>

- 主要工作：负责公司内部 Node.js 基础生态建设
- 其它工作：负责公司内部部署平台、数据库管控平台的开发、设计与维护
- 主要成就
  1. 重写日志基础类库，性能提升 100% ~ 300%，并在绝大多数业务中落地
  2. 重写 RPC 调用相关类库，接入各类内部基础设施，在功能完善度方面仅次于 Golang，自研 Thrift 协议加载解析、序列化与反序列化、代码 / 类型生成等能力，整体性能提升 91% ~ 153%

### 杭州大搜车 ( Node.js 研发工程师 ) <span style="float: right;">2018 年 8 月 ~ 2020 年 6 月<span>

- 主要工作：负责公司内部平台系统的开发、设计与维护
- 其它工作：负责公司 Node.js 开发体系建设，与各种技术攻坚
- 主要成就
  1. 从零搭建物联网平台、微信开发平台等系统
  2. 构建 TypeScript 开发体系，融合公司 Java 基建，使 Node.js 能更好的在公司内部推广并落地

## 项目经历

### [字节跳动] 数据库管控平台 <span style="float: right;">2022 年 11 月 ~ 今<span>

- 项目介绍：公司内部数据库管控平台，负责内部所有数据库实例的管理与运维
- 主要职责：主力开发，负责老平台功能梳理，新平台编程规范制定，Code Review，与 DBA、产品沟通业务需求，以及部分业务功能开发维护工作
- 相关技术：Golang + Python + MySQL + MongoDB + Redis
- 项目结果
  1. 基于内部框架实现与 Golang 自身特性制定新平台编程规范，包括目录结构、接口规范、分层设计与单元测试等方面
  2. 协调组内成员与前端、产品、DBA 的开发、测试与联调工作，使新平台按时完成开发与上线
  3. 完成部分数据库运维工单的开发设计工作，以及内部工单审查系统的接入

### [字节跳动] 部署平台 <span style="float: right;">2022 年 9 月 ~ 2022 年 11 月<span>

- 项目介绍：公司内部 Node.js 服务部署平台，主打 Serverless 快速部署，使用体验对标 Vercel
- 主要职责：主力开发，负责业务功能设计与实现，并协调各方资源，保证业务功能如期交付
- 相关技术：Node.js + TypeScript + MySQL + MongoDB + Redis
- 项目结果
  1. 与内部云开发平台负责人讨论并确定设计与实现方案，对工作量进行拆分，协调各方人力进行开发、测试与联调，最终接入云开发平台，实现本地快速开发与部署上线

### [字节跳动] 内部 Node.js 基础生态建设 <span style="float: right;">2020 年 7 月 ~ 2022 年 9 月<span>

- 项目介绍：支撑公司内部 Node.js 基础生态，与其它语言对齐，包括机器 / 环境信息、服务发现、业务 / 链路日志与打点、HTTP / RPC 调用、MySQL / MongoDB / Redis / MQ 连接、自研框架等功能
- 主要职责：主要负责人，负责 Node.js 基础生态维护与迭代，主要负责机器 / 环境信息、服务发现、业务 / 链路日志与打点、HTTP / RPC 调用、MySQL 等方面
- 相关技术：Node.js + TypeScript + RPC + MySQL
- 项目结果
  1. 重写机器 / 环境信息、服务发现类库，并建立对齐机制，持续与其它语言对齐，避免脱节
  2. 重写日志基础类库，性能提升 100% ~ 300%，并在绝大多数业务中落地
  3. 重写 RPC 调用相关类库，接入各类内部基础设施，并自研 Thrift 协议加载解析、序列化与反序列化、代码 / 类型生成等能力
     1. 一项 RPC 相关的发明专利，专利号 CN202110803025.5
     2. 支持 ACL、CircuitBreaker 等多种服务治理能力
     3. 支持轮询、权重随机、一致性 Hash 等多种负载均衡策略
     4. 支持多种序列化协议与网络协议 ( Thrift / 内部自研二进制协议 + TCP / HTTP )
     5. 支持泛化调用能力，无需 IDL 即可进行 RPC 调用
     6. 支持代码 / 类型生成，将 IDL 编译成可运行代码
     7. 提升 RPC Client 与 RPC Server 整体性能，以下为开启链路日志与打点后的结果
        1. RPC Client QPS 提升 153% ( 4300+ )，响应耗时降低 61% ( 2.2ms )
        2. RPC Server QPS 提升 91% ( 4400+ )，响应耗时降低 48% ( 2.2ms )
     8. 推动业务升级与使用新版本 RPC，截止 2022 年 9 月，在 800+ 业务中落地
  4. 重构 HTTP 调用相关类库，抽离核心逻辑，用以适应公司内的多种应用场景
  5. 重构 MySQL 类库 ( 基于 sequelize / sequelize-typescript )，抽离 MySQL 驱动，解决服务发现下数据库机器动态下线问题
  6. 编写服务发现、日志、链路信息、数据库等方面的指南与科普文档
  7. 推动公司内业务项目 Node.js 版本升级，并收敛 Node.js 基础库与自研框架版本

### [杭州大搜车] 微信开发平台 <span style="float: right;">2020 年 2 月 ~ 2020 年 6 月<span>

- 项目介绍：公司内部微信开发 / 运营辅助平台，包括公众号、小程序等方面，与小程序工程化、微信群控共建公司微信生态
- 主要职责：技术负责人，负责平台服务端、后台前端、小程序 sdk 的设计与实现
- 相关技术：Node.js + Egg.js + TypeScript + MySQL + Redis + RocketMQ + AntDesign
- 项目结果
  1. 一个月时间完成项目主要功能，并基于其开发了一套小程序二维码裂变业务系统
  2. 2 业务系统接入

### [杭州大搜车] 保险业务系统 <span style="float: right;">2019 年 12 月 ~ 2020 年 1 月<span>

- 项目介绍：某保险相关业务系统，使用 Node.js 作为 BFF 层与部分业务服务
- 主要职责：主力开发，负责 BFF 层搭建、后台前端搭建
- 相关技术：Node.js + Egg.js + TypeScript + AntDesign
- 项目结果
  1. 在公司内部落地 BFF 层，与 Java、前端同学配合，以十一人、一个月的时间完成了正常情况下需要 20 ~ 30 人来实现的业务系统，向公司老板们证明 Node.js 的实力
  2. 开发人员比例，前端 : Node.js : Java = 4 : 2 : 5

### [杭州大搜车] 内部 Node.js 开发框架体系建设 <span style="float: right;">2019 年 7 月 ~ 2020 年 6 月<span>

- 项目简介：公司内部 Node.js 开发框架体系，基于 Egg.js，包含 MySQL / Redis / RocketMQ 连接、Dubbo 调用、单点登录、任务调度、全链路、多环境治理等功能
- 主要职责：主要维护人，负责接入各种 Java 基建，提升公司内部 Node.js 的使用体验
- 相关技术：Node.js + Egg.js + TypeScript + MySQL + Redis + RocketMQ
- 项目结果
  1. 完善并落地 TypeScript 开发体系，事业部内新 Node.js 项目均使用该体系开发
  2. 参考 node-zookeeper-client 与 Java Zookeeper 源码，完成纯 TypeScript 的 ZooKeeper SDK，并在内部广泛应用
  3. 打通公司内部全链路、RocketMQ、多环境治理等基建，使 Node.js 能享受到完善的基建支持
  4. 在 20+ 业务中落地

### [杭州大搜车] 物联网平台 <span style="float: right;">2019 年 3 月 ~ 2019 年 8 月<span>

- 项目简介：公司内部物联网设备的管控中心，实现了包括消息通信、设备管理、设备监控、能力抽象、数据采集等功能
- 主要职责：后端负责人，负责平台架构 / 通讯协议设计、服务端 / 后台前端实现
- 相关技术：Node.js + Egg.js + TypeScript + MySQL + Redis + RocketMQ + MQTT + AntDesign
- 项目结果
  1. 一项物联网相关的发明专利，专利号 CN201910807168.6
  2. 50+ 实时在线设备、10+ 业务系统接入

### [杭州大搜车] 钉钉基础服务 <span style="float: right;">2019 年 2 月 ~ 2020 年 6 月<span>

- 项目简介：公司内部钉钉 OA 工具，支撑公司钉钉相关消息推送、审批流程、员工数据等
- 主要职责：主力开发，负责服务接入与功能迭代
- 相关技术：Node.js + Egg.js + MySQL + Redis + RocketMQ
- 项目结果
  1. 日均处理 600+ 钉钉审批
  2. 50+ 业务系统接入、150+ 钉钉审批接入

### [杭州大搜车] 流量网关 <span style="float: right;">2018 年 8 月 ~ 2019 年 2 月<span>

- 项目简介：公司内部 API 网关，承载公司部分流量入口，日均 TPS 200+
- 主要职责：主力开发，负责网关转发层开发，性能优化
- 相关技术：OpenResty + Node.js + MySQL + Redis
- 项目结果
  1. 完成转发规则静态化，使网关 TPS 从 1000+ 提升至 3700+，性能约为原生 nginx 的 45%
  2. 设计并实现插件系统，方便网关业务扩展

## 开源项目

- [zk-client](https://github.com/xiedacon/zk-client)：纯 TypeScript 实现的 ZooKeeper SDK，支持自动重连，支持 ZooKeeper 3.6 的 API，单测覆盖率 77%

## 致谢

感谢您花时间阅读我的简历，期待能有机会和您共事
