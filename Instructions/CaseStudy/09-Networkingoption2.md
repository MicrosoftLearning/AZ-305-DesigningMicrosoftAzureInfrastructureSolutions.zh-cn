---
casestudy:
  title: 设计网络解决方案 - BI 企业应用程序
  module: Network infrastructure solutions
---
# <a name="design-a-network-infrastructure-solution"></a>设计网络基础结构解决方案  

## <a name="requirements"></a>要求

As the Tailwind Traders Enterprise IT team prepares to define the strategy to migrate some of company’s workloads to Azure, it must identify the required networking components and design a network infrastructure necessary to support them. Considering the global scope of its operations, Tailwind Traders will be using multiple Azure regions to host its applications. Most of these applications have dependencies on infrastructure and data services, which will also reside in Azure. Internal applications migrated to Azure must remain accessible to Tailwind Traders users. Internet-facing applications migrated to Azure must remain accessible to any external customer. 

为了整合初始网络设计，Tailwind Traders Enterprise IT 团队选择了两个关键的应用程序，它们代表了预计将迁移到 Azure 的最常见的工作负载类别。  

## <a name="design---bi-enterprise-application"></a>设计 - BI 企业应用程序 

![BI 企业应用程序体系结构](media/compute.png)

-   基于 Windows 的内部三层商业智能 (BI) 企业应用程序，前端层运行 IIS Web 服务器，中间层托管基于 .NET Framework 的业务逻辑，后端层实现为 SQL Server Always On 可用性组数据库。 

-   此应用程序归类为任务关键型应用程序，需要预配高可用性（99.99% 可用性 SLA）和灾难恢复（10 分钟 RPO 和 2 小时 RTO）。

-   To provide connectivity to internal apps migrated to Azure, Tailwind Traders will need to establish hybrid connectivity from their on-premises datacenters. The Enterprise IT group already established that such connectivity will be implemented by using ExpressRoute circuit from its main Seattle datacenter, however, at this point it is not clear yet what would be failover solution in case that circuit becomes unavailable. The Tailwind Traders CFO wants to avoid paying for another, redundant ExpressRoute circuit. 

- There are additional considerations that apply to on-premises connectivity to internal apps migrated to Azure. Since the Tailwind Traders Azure environment will consist of multiple subscriptions and, effectively, multiple virtual networks, to minimize cost, it is important to minimize the number of Azure resources required to implement core networking capabilities. Such capabilities include hybrid connectivity to on-premises locations as well as traffic filtering. Incidentally, this need to minimize cost aligns with the Information Security and Risk requirements, which state that all traffic between on-premises locations and Azure virtual networks must flow via a single virtual network, which will be hosting components responsible for hybrid connectivity and traffic filtering. 

-   As per requirements defined by the Tailwind Traders Information Security and Risk teams, all communication between Azure VMs in different tiers that are part of the same application must allow only the ports required to run and maintain the application. However, due to IP address space limitations, it might not be possible to allocate dedicated subnets to each tier. Enterprise IT group needs to identify the optimal way to configure source and destination for traffic filtering that would not require directly referencing IP addresses or IP address ranges.


## <a name="tasks---bi-enterprise-application"></a>任务 - BI 企业应用程序 

1. Tailwind Traders Enterprise IT 团队在准备定义将公司的某些工作负荷迁移到 Azure 的策略时，必须确定所需的网络组件并设计支持这些组件所需的网络基础结构。 

2. 考虑到其运营遍及全球，Tailwind Traders 将使用多个 Azure 区域来托管其应用程序。 

3. 根据存储（关系）案例研究，如何更新网络设计，以保护对存储帐户的访问，并确保仅精选用户有权访问存储帐户？

4. 根据 SQL 后端的现代化，计划如何实现对数据库的实际访问，以便前端在其代码库中没有硬编码的机密？

如何整合“体系结构良好的框架”支柱，以生成高质量、稳定且高效的云体系结构？
