---
casestudy:
  title: Fabrikam Residences
  module: Logging and monitoring solutions
---
# <a name="case-study-fabrikam-residences"></a>案例研究：Fabrikam Residences

## <a name="requirements"></a>要求

**本案例研究需要你完成以下模块和案例研究：计算、关系数据、非关系数据、身份验证和应用程序体系结构**

You have taken a new position with Fabrikam Residences, which is very successful and is experiencing rapid growth. Fabrikam Residences is a building contractor for new homes and major home renovations and have become successful by providing quality buildings and offering newer integrated home technologies than their competitors.  

Currently these technologies are provided and managed by separate sub-contract companies. The owners of Fabrikam Residences want to begin offering these upgraded technology options in-house to provide better quality, support and data on customer patterns and needs. 
 
Initially, the company wants to offer HVAC (heating and cooling) control and monitoring, security system monitoring and alerts, and home automation. This will require a new website, data storage solution and data ingestion solution.

The company has seen tremendous growth over the past 2 years. The company is estimating it may double in size over the next 12-18 months. With such rapid growth in the regional market, the company has no current plans to expand outside of the regional market.

## <a name="current-situation"></a>当前情况

The Fabrikam Headquarters operates a small datacenter in a single location. The datacenter hosts the company <bpt id="p1">**</bpt>Project Management (PM) software<ept id="p1">**</ept>.

![项目管理软件体系结构](media/fabrikam.png)

- 你在 Fabrikam Residences 担任新职位，该公司非常成功，正经历着快速发展。  

- 图像和文档存储在服务器的映射驱动器上，该驱动器驻留在专用 NAS 设备上。

- 企业用户和办公室工作人员使用 Web 前端输入数据，例如供应交付计划和变更单。

-   Fabrikam Residences 是新房和大型房屋翻新的建筑承包商，通过提供优质建筑和提供比竞争对手更新的集成家居技术而获得成功。

The <bpt id="p1">**</bpt>Home Technology software<ept id="p1">**</ept> is currently provided and hosted by third parties and involves at least three different websites the customer must visit.  It is proposed the software be replaced with an in-house developed and unified solution.

![HVAC、安全性和自动化应用关系图](media/software.png)

## <a name="requirements"></a>要求 

**项目管理软件**

- 将尽可能多的系统迁移到公有云提供商。

- 目前，这些技术由独立的分包公司提供和管理。

- Fabrikam Residences 的所有者希望开始在内部提供这些升级的技术选项，以提供更好的质量、支持和有关客户模式和需求的数据。

**新家庭技术解决方案**

- 添加一个新解决方案，从家庭监视传感器持续收集数据。
  - 为一些传感器读数建立数据库，用于趋势分析和报告。
  - 根据所有者需求提供可配置的实时警报。
  
- 设计一个关系数据库解决方案来保存房主的偏好和设置。
  - 系统必须可缩放。
  - 冗余至关重要。
  
- The new unified website will be developed in house and hosted on Linux.  This website will be used to view monitors and change preferences for items such as temperature or alert thresholds. Loads can vary widely, and the system must be able to scale quickly.

-   为用户提供一种登录系统的方法，而无需创建另一个用户帐户和密码。

- 实施安全控制并每周提供报告，概述公司如何与行业标准最佳做法匹配。

## <a name="tasks"></a>任务 

1. 最初，该公司希望提供 HVAC（采暖和制冷）控制和监视、安全系统监视和警报，以及家庭自动化。

2. 这需要一个新的网站、数据存储解决方案和数据引入解决方案。

如何整合“架构良好的框架”支柱，以生成高质量、稳定且高效的云体系结构？

