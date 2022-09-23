---
casestudy:
  title: 设计关系存储解决方案
  module: Relational storage solutions
---
# <a name="design-relational-storage-case-study"></a>设计关系存储案例研究

## <a name="requirements"></a>要求

Tailwind Traders is looking to move their existing public website database into Azure, as the website front end is being moved there as well.  The website front end will initially only be deployed in 2 regions for redundancy.  However, it is expected that as traffic increases the website will be replicated to other regions around the world. The database, which you are being asked to migrate, holds the product catalog, and all online orders.  Currently the database runs on a single Microsoft SQL Server Always On availability group on premises.

Tailwind Traders 的主要关注点：

-   <bpt id="p1">**</bpt>High availability.<ept id="p1">**</ept>  A primary concern for Tailwind Traders is that this database be highly available as it is critical to their business.  Any outages may result in lost sales or customer confidence.

-   <bpt id="p1">**</bpt>Website performance.<ept id="p1">**</ept>  While the performance of placing orders is normally satisfactory, browsing or searching pages with many items listed is reported as being “sluggish.”

-   <bpt id="p1">**</bpt>Security.<ept id="p1">**</ept>  Tailwind Traders is very concerned about personal or financial information stored in the database being exposed.  In addition to implementing proper security measures, the security team needs to verify that industry standard best practices are implemented, when possible.


## <a name="tasks"></a>任务

1.  Tailwind Traders 希望将其现有的公共网站数据库转移到 Azure 上，因为网站前端也将被转移到 Azure 上。 
2.  用图表说明你的决定并解释你的解决方案。 

如何整合“架构良好的框架”支柱，以生成高质量、稳定且高效的云体系结构？
