![MQTT 5.0 公有云](https://static.emqx.net/images/3a5367d7e54adc84c9e25f670add6437.png)

全球首个 [MQTT 5.0 公有云服务](https://cloud.emqx.cn/) EMQ X Cloud 国内版正式上线，首次注册用户提供 7 天免费试用，目前已经支持华为云、阿里云，其他云服务商将陆续上线。

EMQ X [MQTT 服务器](https://www.emqx.cn/products/broker)在过去的几年中为全球数千家企业用户选用，为客户的物联网应用提供稳定的基础服务。EMQ X Cloud - MQTT 5.0 公有云服务来自于我们服务客户总结的一些最佳实践，致力于提供快速部署、轻松管理、弹性扩展、跨多云部署的物联网 MQTT 5.0 服务。借助云服务商提供的基础计算设施，EMQ X Cloud 面向全球数十个国家与地区提供服务，为 5G 与万物互联应用提供低成本、安全可靠的云服务。

在 EMQ X Cloud 上，用户仅需数分钟即可创建高可用、独享实例的 EMQ X 集群，立即开始原型设计与应用开发而无需关注后续的运维工作。产品上线后，集群可进行不停机扩容以应对业务增长带来的容量扩张，保证可用性的同时最大化节省使用成本。

与其它大部分公有 IoT Hub 云平台不同的是，EMQ X Cloud 提供独有隔离环境的 MQTT 5.0 服务器集群，拥有显著的成本优势及更少的使用限制，在消息量较多的情况下 EMQ X Cloud 仍能保持较低的使用成本。通过对等网络等功能，可以实现对接用户在私有网络中部署的大数据分析、消息存储以及其他业务系统。

EMQ X Cloud 支持现有物联网项目迁移，完全兼容 EMQ X 企业版，支持向 EMQ X 企业版双向迁移，通过少量适配调整可以与公有云平台 IoT Hub 双向迁移。



## 产品特性

[MQTT 云服务](https://cloud.emqx.cn/)为应用程序及设备提供安全可靠的双向通信能力，在支持大规模集群海量设备连接的基础上同时提供了其他增值能力，如设备管理、规则引擎、数据持久化与 Kafka 数据桥接等，覆盖了各类 IoT 应用场景。

EMQ X Cloud 关键特性如下：

**协议完整支持**

MQTT 云服务支持 MQTT v3.1，v3.1.1 与 v5.0 协议版本，是全球首个支持 MQTT 5.0 的公有云服务，支持 MQTT WebSocket 服务，完整支持 QoS0, QoS1 与 QoS2 级别 MQTT 消息。

**易于部署和管理**

只需要简单的操作即可在数分钟内创建完美配置优化、高度可用的多节点 MQTT 5.0 集群，将复杂的运维监控工作完全托管至 EMQ X Cloud 运维团队。

**按实例收费**

按集群实例收费，而非消息条数，不限 API 与规则引擎的使用，成本清晰可控。提供多种规格实例，完全覆盖各个级别应用规模。

**容量预估与伸缩**

通过连接数与消息吞吐量自动预估容量，通过紧密的监控来制定伸缩计划，集群大小可随业务规模平滑调整。

**高可用与私有实例**

每个部署使用独立的 VPS、负载均衡、DNS 等基础资源，保证系统安全与稳定。

**规则引擎与消息实时编解码**

内置规则引擎，可以动态编写 SQL 灵活处理设备消息与事件数据，简化业务开发流程；可以通过规则引擎的处理函数或外部服务实现二进制/特殊格式消息编解码。

**与大数据分析和存储系统的集成**

通过规则引擎与不同的大数据分析系统、存储系统集成，如 Apache Kafka，Apache Pulsar，PostgreSQL，InfluxDB，OpenTSDB 和 Redis 等。



## 使用限制

EMQ X Cloud 上相关的限制取决于购买的连接数与消息向下行 TPS，对应的参数均进行过严密性能测试。

公有云 IoT Hub 基于性能与稳定性考虑，在设备接入、消息收发调用层面做了一定的限制，此处整理现有公有云 IoT Hub 公开的限制信息以供参考。

注意：以下各表中 EMQ X Cloud 的“不限”指不做技术手段限制，相关项的性能取决于硬件限制，在性能消耗接近临界值时会触发限流处理，具体数据以实际使用场景为准。

| 限制描述                  | EMQ X Cloud            | 公有云 IoT Hub                               |
| ------------------------- | ---------------------- | -------------------------------------------- |
| 每秒建立连接次数          | 1000                   | 500~1000                                     |
| 单客户端订阅主题数        | 不限                   | 10~100                                       |
| 单客户端每秒订阅请求      | 不限                   | 10~1W                                        |
| 单客户端上行消息速度      | 不限                   | QoS0：30~50条/秒QoS1：10~20条/秒QoS2：不支持 |
| 单客户端消息下行          | 不限                   | 50~100条/s                                   |
| 单客户端每秒吞吐带宽      | 不限                   | 1024KB                                       |
| 单个消息长度              | 默认 1024KB 可申请调整 | 256KB                                        |
| 离线消息最大存储时长      | 永不过期               | 1周                                          |
| Topic 数量                | 不限                   | 50~100个                                     |
| 权限                      | 自定义                 | 设备只能对自己的Topic进行消息发布订阅        |
| 订阅/取消订阅操作响应时间 | 立即                   | 5~10秒                                       |


## 支持云平台

国内：现已支持华为云上海、广州、北京，阿里云深圳、上海、杭州、北京共七个数据中心。

如需其他地区节点可通过工单申请，申请成功后预计在 1~2 周即可支持。（仅限中国大陆地区节点）。国内多家云服务商已在计划中，后续开放支持。



国际：现已支持 AWS 美国东部（弗吉尼亚北部）、美国西部（俄勒冈州）、欧洲（爱尔兰）三个计算中心。

如需亚洲或其他地区 AWS 节点可通过工单申请，申请成功后预计在 1~2 周即可支持。（中国大陆地区节点不做支持）。Azure 和 Google Cloud Platform 已在计划中，即将支持。



## 界面概览

创建部署实例，选择云平台与区域，根据最大连接数与消息吞吐量预估服务价格：

![MQTT 公有云价格估算](https://static.emqx.net/images/7f3273f6e7a28984094f8ef2bf5ce701.png)           

添加客户端认证与发布订阅 ACL 规则，支持批量导入：

![MQTT 认证鉴权](https://static.emqx.net/images/44027dce75955fb611d2e8f861e9be9a.png)

运行情况与业务指标查看，提供不同维度集群运行统计功能：

![MQTT 服务器指标监控](https://static.emqx.net/images/b846c4c0fc4fe795abe1059c51a67f16.png)           

账单与费用信息，当日、当月以及历史消费数据清晰明了：

![EMQ X Cloud 财务管理](https://static.emqx.net/images/7b9079726c73b8b4fb20f5e2547d1803.png)            



## 关于 EMQ

[EMQ - 杭州映云科技](https://www.emqx.cn/)是全球领先的消息与流处理开源软件企业，聚焦服务于新产业周期的 5G\&IoT、边缘计算(Edge)与云计算(Cloud)市场，面向全球运营。

EMQ 总部位于杭州，在北京、上海、硅谷、法兰克福设有分支机构，核心产品包括面向云和边缘计算的 IoT
消息中间件以及轻量级流式处理中间件，累计已服务全球 6000+ 企业用户，并与 50+ 世界 500 强企业达成战略合作，典型用户包括 HPE、VMware、Verifone、Ericsson、华为、中国电信、中国移动、国家电网、上汽大众等。

2018 年开始，EMQ 与中国电信合作构建全球最大的 **NB-IoT** 接入平台；

同年 EMQ 核心产品 EMQ X 实现千万级并发连接，同步推出了边缘计算消息服务；

2019 年 EMQ 推出多活&跨 IDC 消息平台以及边缘计算流处理软件 Kuiper；

2020 年 EMQ 正式上线全球首个 **MQTT 5.0 公有云服务 EMQ X Cloud**，并在国内与海外同步运营；

2020 年 6 月，EMQ 发布 [Hamler](https://www.hamler-lang.org/) 编程语言，将赋予行业尤其是 5G、IoT、云计算和边缘计算等潜力领域，构建下一代高可靠、可扩展、具备软实时支持应用的能力；

未来，EMQ 将在核心产品 EMQ X 5.0 版本发布 **5G 大基建超大规模多协议超融合接入平台**，与海内外用户携手共进，推动行业与时代发展。