---
casestudy:
  title: 设计应用体系结构解决方案
  module: App architecture solutions
---
# <a name="design-an-app-architecture-solution"></a>设计应用体系结构解决方案

## <a name="requirements"></a>要求

Tailwind Traders is looking to update their website to include customer supplied product images in addition to the already existing photos provided by marketing. They believe that having more photos of products in use will give potential customers a better feel for how past customers loved their products after purchasing them. They do have some requirements as outlined below:

* Uploaded images will need to be scanned before getting posted on the website. Legal and Marketing are both requesting that after initial upload, the images be checked for any issues that reflect poorly upon the company or could cause legal issues. An in-house API has already been developed and deployed that can perform the necessary scanning. 

* Based on existing patterns, Tailwind Traders expects the image uploads to happen very unevenly throughout the day. Certain periods may experience more uploads than the scanning software can handle, while other periods may experience very few or no uploads.

* 系统扫描并批准上传的图像后，Tailwind Traders 希望客户收到一封电子邮件，感谢他们共享其图像。

* Cost and management of the solution is a concern, especially since Tailwind Traders isn’t sure how popular this feature will be initially. Minimize costs and leverage serverless solutions where possible.

 

![应用体系结构](media/Apparchitecture.png)

 

## <a name="task"></a>任务

为要添加到公司网站的客户图像设计体系结构。  

* 图像应存储在何处？

* 如何确保所有的图像都被扫描，即使上传速度超过扫描速度？

* 图像获得批准并更新目录数据库后，将如何通知客户？ 

如何整合“架构良好的框架”支柱，以生成高质量、稳定且高效的云体系结构？

 
