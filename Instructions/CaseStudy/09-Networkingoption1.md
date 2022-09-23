
# <a name="design-a-network-infrastructure-solution"></a>设计网络基础结构解决方案  

## <a name="requirements"></a>要求

As the Tailwind Traders Enterprise IT team prepares to define the strategy to migrate some of company’s workloads to Azure, it must identify the required networking components and design a network infrastructure necessary to support them. Considering the global scope of its operations, Tailwind Traders will be using multiple Azure regions to host its applications. Most of these applications have dependencies on infrastructure and data services, which will also reside in Azure. Internal applications migrated to Azure must remain accessible to Tailwind Traders users. Internet-facing applications migrated to Azure must remain accessible to any external customer. 

为了整合初始网络设计，Tailwind Traders 企业 IT 团队选择了两个关键的应用程序，它们代表了预计将迁移到 Azure 的最常见的工作负载类别。  

### <a name="design---product-catalog-enterprise-application"></a>设计 - 产品目录企业应用程序

![产品目录体系结构](media/catalog.png)

- An internet-facing, Windows-based two-tier .NET Core-based web app providing access to the product catalog, hosted in a SQL Server Always On Availability Group database. This application is categorized as mission-critical, with availability SLA of 99.99%, 10-minute RPO and 2-hour RTO. 

-   Business leads emphasize the importance of the optimal customer experience when accessing internet-facing apps, so it is critical that the time it takes to load web pages and download static content is minimized. Similarly, a failure of individual servers hosting web app components and their dependencies should have negligible impact on the web app availability perceived by customers. While it’s understood that a regional failure might introduce some interruption to existing web sessions, the failover to a disaster recovery site should be automatic.

- 为了利用 Azure PaaS 服务提供的优势，企业 IT 团队决定使用 Azure SQL 数据库来实现产品目录企业应用程序的数据库。 

- Tailwind Traders 信息安全和风险团队要求，属于同一应用程序的 Azure VM 和 PaaS 服务之间的所有通信都必须通过 Azure 主干（而不是 PaaS 服务的公共终结点）传输。 

## <a name="tasks---product-catalog-enterprise-application"></a>任务 - 产品目录企业应用程序

1. Tailwind Traders Enterprise IT 团队在准备定义将公司的某些工作负荷迁移到 Azure 的策略时，必须确定所需的网络组件并设计支持这些组件所需的网络基础结构。 

如何整合“架构良好的框架”支柱，以生成高质量、稳定且高效的云体系结构？

