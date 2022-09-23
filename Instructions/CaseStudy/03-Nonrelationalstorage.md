---
casestudy:
  title: 设计非关系存储解决方案
  module: Non-relational storage solutions
---
# <a name="design-non-relational-storage-case-study"></a>设计非关系存储案例研究

## <a name="requirements"></a>要求

Tailwind Traders wants to reduce storage costs by reducing duplicate content and, whenever applicable, migrating it to the cloud. They would like a solution that centralizes maintenance while still providing world-wide access for customers who browse media files and marketing literature. Additionally, they would like to address the storage of company data files. 

![非关系存储体系结构](media/Nonrelational%20storage.png)

 

* <bpt id="p1">**</bpt>Media files<ept id="p1">**</ept>. Media files include product photos and feature videos that are displayed on the company’s public website, which is developed and maintained in house. When a customer browses to an item, the corresponding media files are displayed. The media files are in different formats, but JPEG and MP4 are the most common. 

* <bpt id="p1">**</bpt>Marketing literature<ept id="p1">**</ept>. The marketing literature includes customer stories, sales flyers, sizing charts, and eco-friendly manufacturing information. Internal marketing users access the literature via a mapped drive on their Windows workstations. Customers access the literature directly from the company’s public website.

* <bpt id="p1">**</bpt>Corporate documents<ept id="p1">**</ept>. These are internal documents for departments such as human resources and finance. These documents are accessed and managed via an internally developed web application. Legal requires that various documents be retained for a specific period of time. Occasionally documents will need to be maintained longer when legal or HR issues are being investigated. Most corporate documents older than one year are only kept for compliance reasons and are seldom accessed.

* Tailwind Traders 希望通过减少重复内容并在适用的情况下将其迁移到云来降低存储成本。 

* 他们希望有这样一种解决方案：能够集中维护，同时仍为浏览媒体文件和营销资料的客户提供全球访问权限。 

## <a name="tasks"></a>任务

1. 为 Tailwind Traders 设计存储解决方案。  

      * 代表什么类型的数据？  

      * 在设计中会考虑哪些因素？

      * 你会使用 Blob 访问层吗？

      * 你会使用不可变存储吗？

      * 如何安全访问内容？

2.  此外，他们还希望解决公司数据文件的存储问题。 

如何整合“架构良好的框架”支柱，以生成高质量、稳定且高效的云体系结构？
