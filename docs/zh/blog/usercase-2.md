---
blog: true
title: openGemini：助力华为云工业物联平台实现百万点位接入
pubDate: '2024-09-28'
author: openGemini
abstract: openGemini解决了InfluxDB单机的性能瓶颈，端到端性能提升2-5倍，支持百万级设备接入
cover: /images/cover/usercase.png
recommend: 0
category: 用户案例
tag: 物联网
---

全球工业4.0浪潮席卷而至，长期看，为提高企业的经济效益和竞争实力，降本增效是大势所趋，数字化转型为工业制造提供新机遇。

在数字化转型过程中，数字化技术起到了非常重要的作用，其中数据库、大数据平台和云数据平台等基础软件，构成了企业数字化转型的重要基础设施，即“数据基础设施”。随着各行业的数字化场景的发展，新的业务挑战对“数据基础设施”的技术路线演进产生了极大的推动作用。

## **数字化转型，IT手段治理OT数据更符合新的发展需求**

由于中国的企业数字化发展较晚，海外工业基础软件（如Wonderware实时库、Pi System）具备先发优势，占领了中国工业制造大部分市场，这类软件具有采购成本高、维护成本大、扩展性差，软件闭源、非国产化、服务响应不及时、数据共享能力弱等众多共性问题，严重制约了企业数字化转型进程。

华为云IoT工业物联平台，面向工业企业推出一站式OT数据治理平台，重点解决OT数据的接入，清洗，建模，分析及应用，其中集团-工厂级联架构，助力集团化企业快速实现集团、工厂和车间的协同管理。在“5G+工业互联网”融合发展的当下，华为云IoT工业物联平台在IT治理OT数据方面进一步探索和突破，采用了开源的InfluxDB时序数据库存储和分析工厂各环节设备数据，大幅降低用户成本，已在多个行业实践并取得明显应用效果。

InfluxDB是一款广泛使用的开源时序数据库，DBEngines排名第一，具有很好的读写性能和数据压缩能力。但随着工业物联平台业务的发展，InfluxDB遇到了一些瓶颈：

- 不具备扩展性：社区开源的为单机版，其他开源的Influx-proxy集群方案组件众多，安装部署、后期维护成本高、复杂度大
- 单机版性能存在限制：开源的单机性能和数据采集点有限，无法支持业务规模、数据采集点持续增长的情况
- 非国产化：在复杂的国际形势下，存在一些不确定性

## **轻松满足每秒百万点位数据写入，查询性能大幅提升**

![图片](/images/docs_img/usercase-2-1.png)

对于工业物联平台来说，希望替代后的系统具备功能稳定、高效的数据写入及数据查询（包括最新数据和历史数据）、可云化部署、可边缘部署、支持线性扩展的特性，他们早在6月份就关注到openGemini的开源发布，一直跟openGemini技术团队保持技术交流，借此契机，在内部对比测试InfluxDB后，果断选择了openGemini。

在软件使用上，openGemini兼容InfluxDB，业务对接零修改；

在软件运维层面，openGemini安装包体积小，边缘设备照常安装，支持arm和容器化部，具备完善的可观测性（内置260项观测指标），让系统的运营维护变的轻松简单；

此外，扩展性和性能也是十分看重的，凭借着openGemini分布式集群设计，以及查询引擎和存储引擎方面的大量优化（如数据分区分级、向量化、连接复用、预聚合、降采样等）,实现了良好的集群横向扩展能力，同时具备卓越的性能，轻松支持百万级点位数据并发写入和大量数据并发查询毫秒级响应。

## **结语**

随着外部竞争越发激烈，从近些年密集的政策可以看到，国家在持续、积极的推动企业数字化转型，相信越来越多的企业会加入到数字化转型的进程中，IT治理OT数据、IT与OT融合的局面正在到来，尤其在优秀的开源软件加持下，这将进一步降低企业数字化转型的投入成本，新的“数据基础设施”必然会得到更好的发展。

工业场景下，数据普遍为时序数据库，时序数据库提供了一种开放、高效、低成本的数据处理和分析解决方案。**openGemini社区为业界提供了一款可以解决实际问题的时序数据库，欢迎更多企业与社区携手，发挥好IT与OT融合技术优势，共同推动企业数字化转型。**