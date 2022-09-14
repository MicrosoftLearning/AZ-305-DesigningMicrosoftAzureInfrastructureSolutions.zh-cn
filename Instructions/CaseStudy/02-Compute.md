---
casestudy:
  title: 设计计算解决方案
  module: Compute solutions
---

# <a name="design-a-compute-solution"></a>设计计算解决方案

## <a name="requirements"></a>要求

Tailwind Traders would like to migrate their product catalog application to the cloud. This application has a traditional 3-tier configuration using SQL Server as the data store. The IT team hopes you can help modernize the application. They have provided this diagram and several areas that could be improved. 

![计算体系结构](media/compute.png)

* The frontend application is a .NET core-based web app. During peak periods 1750 customers visit the website each hour. 

* The application runs on IIS web servers in a front-end tier. This tier handles all customer requests for purchasing products. During the latest holiday sale, the front-end servers reached their performance limits and page loads were lengthy. The IT team has considered adding more servers, but during off hours the servers are often idle.

* The middle tier hosts the business logic that processes customer requests. These requests are often for help desk support. Support requests are queued and lately the wait times have been very long. Customers are offered email rather than wait for a representative. But many customers seem frustrated and are disconnecting rather than wait. Customer requests are 75-125 per hour. 

* Tailwind Traders 希望将其产品目录应用程序迁移到云中。

* 虽然高可用性是一个问题，但由于法律要求，公司必须将所有资源保存在一个区域。

## <a name="tasks"></a>任务

* 此应用程序具有传统的 3 层配置，同时使用 SQL Server 作为数据存储。 

* IT 团队希望你能够帮助实现应用程序的现代化。 

如何整合“架构良好的框架”支柱，以生成高质量、稳定且高效的云体系结构？
