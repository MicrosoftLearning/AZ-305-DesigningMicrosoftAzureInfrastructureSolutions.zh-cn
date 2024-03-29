---
casestudy:
  title: 设计关系存储解决方案
  module: Relational storage solutions
---
# 设计关系存储案例研究

## 要求

Tailwind Traders 希望将其现有的公共网站数据库转移到 Azure 上，因为网站前端也将被转移到 Azure 上。  网站前端最初将仅部署在 2 个区域以实现冗余。  但是，预计随着流量的增加，该网站将复制到世界各地的其他区域。 要求迁移的数据库会保存产品目录和所有在线订单。  目前，数据库在本地的单个 Microsoft SQL Server Always On 可用性组上运行。

![非关系存储体系结构](media/relational%20storage.png)

Tailwind Traders 的主要关注点：

-   高可用性。  Tailwind Traders 主要关注的是此数据库的高可用性，因为它对他们的业务至关重要。  任何中断都可能导致销售或客户失去信心。

-   **网站性能。**  虽然下订单的表现通常令人满意，但浏览或搜索列出许多项的页面被报告为“缓慢”。

-   **安全性**。  Tailwind Traders 非常担心存储在数据库中的个人或财务信息被暴露。  除了实施适当的安全措施外，安全团队还需要尽可能验证是否实施了行业标准最佳做法。


## 任务

1.  设计数据库解决方案。 设计应包括授权、身份验证、定价、性能和高可用性。 
2.  用图表说明你的决定并解释你的解决方案。 

如何整合“体系结构良好的框架”支柱，以生成高质量、稳定且高效的云体系结构？
