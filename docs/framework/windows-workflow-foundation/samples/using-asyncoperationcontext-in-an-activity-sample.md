---
title: 在活动示例中使用 AsyncOperationContext
ms.date: 03/30/2017
ms.assetid: 0888a0bd-d227-4c00-ad6a-b654a01740e8
ms.openlocfilehash: 4358a364a3f7ec69b7c1c548fcf82fe494f37505
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/17/2018
ms.locfileid: "45742883"
---
# <a name="using-asyncoperationcontext-in-an-activity-sample"></a>在活动示例中使用 AsyncOperationContext
此示例演示如何开发一个自定义 <xref:System.Activities.CodeActivity>，该活动使用 <xref:System.Activities.AsyncCodeActivityContext> 在工作流外部异步执行工作。  
  
## <a name="sample-details"></a>示例详细信息  
 该示例活动使用 <xref:System.IO.FileStream.BeginWrite%2A> 类上的 <xref:System.IO.FileStream.EndWrite%2A> 和 <xref:System.IO.FileStream> 方法以异步方式将数据写入文件。 此处介绍的模式适合于与其他异步方法一起使用。 在执行异步操作时，可以执行工作流中的其他活动，但无法持久化工作流。  
  
#### <a name="to-set-up-build-and-run-the-sample"></a>设置、生成和运行示例  
  
1.  在 [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] 中打开 Async.sln 示例解决方案。  
  
2.  生成和运行解决方案。  
  
> [!IMPORTANT]
>  您的计算机上可能已安装这些示例。 在继续操作之前，请先检查以下（默认）目录：  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  如果此目录不存在，请转到[Windows Communication Foundation (WCF) 和.NET Framework 4 的 Windows Workflow Foundation (WF) 示例](https://go.microsoft.com/fwlink/?LinkId=150780)若要下载所有 Windows Communication Foundation (WCF) 和[!INCLUDE[wf1](../../../../includes/wf1-md.md)]示例。 此示例位于以下目录：  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\CustomActivities\Code-Bodied\Async`