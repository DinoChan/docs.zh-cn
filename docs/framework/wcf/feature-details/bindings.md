---
title: Windows Communication Foundation 绑定
ms.date: 03/30/2017
helpviewer_keywords:
- WCF [WCF], bindings
- Windows Communication Foundation [WCF], bindings
- bindings [WCF]
ms.assetid: 83639133-89f7-43f0-b4ef-8d9e57c08d25
ms.openlocfilehash: 1930826cf51d67ceb789e20920ca42f04d1adc1b
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/26/2018
ms.locfileid: "47199328"
---
# <a name="windows-communication-foundation-bindings"></a>Windows Communication Foundation 绑定
Windows Communication Foundation (WCF) 将如何与其他软件的通信方式编写的应用程序软件。 使用绑定指定客户端与服务彼此通信所需的传输、编码和协议详细信息。 WCF 使用绑定来生成的终结点的基础网络表示，因此必须进行通信双方达成大多数绑定详细信息。 完成此任务的最简单方法是让服务的客户端使用该服务的终结点所使用的相同绑定。 有关如何执行此操作的详细信息，请参阅[配置 Windows Communication Foundation 服务和客户端使用的绑定](https://msdn.microsoft.com/library/bd8b277b-932f-472f-a42a-b02bb5257dfb)。  
  
 绑定由绑定元素的集合组成。 每个元素描述终结点与客户端的通信方式的某一方面。 一个绑定必须至少包括一个传输绑定元素，至少包括一个消息编码绑定元素（默认情况下，传输绑定元素可能提供该元素）以及包括任意数目的其他协议绑定元素。 使用本说明中生成运行时的进程，每个绑定元素均可为该运行时提供代码。  
  
 WCF 提供了包含常见选择的绑定元素的绑定。 这些绑定可以与其默认设置一起使用，您也可以根据用户需求修改这些默认值。 这些系统提供的绑定具有一些属性，可以通过这些属性直接控制绑定元素及其设置。 通过为绑定的每个版本提供其自己的名称，还可以轻松地并行使用该绑定的多个版本。 有关详细信息，请参阅[Configuring System-Provided 绑定](../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)。  
  
 如果需要的绑定元素集合不是由系统提供的这些绑定之一提供，则可以创建由所需绑定元素的集合组成的自定义绑定。 这些自定义绑定易于创建且不需要新类，但是，它们不提供用于控制绑定元素或其设置的属性。 你可以访问这些绑定元素并通过包含它们的集合修改其设置。 有关详细信息，请参阅[自定义绑定](../../../../docs/framework/wcf/extending/custom-bindings.md)。  
  
## <a name="in-this-section"></a>本节内容  
 [配置系统提供的绑定](../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 介绍如何使用和修改 WCF 提供的用于支持常见的方案的绑定。  
  
 [使用绑定来配置 Windows Communication Foundation 服务和客户端](https://msdn.microsoft.com/library/bd8b277b-932f-472f-a42a-b02bb5257dfb)  
 介绍如何在代码和以声明方式使用配置中以强制方式定义服务和客户端的 Windows Communication Foundation (WCF) 绑定。  
  
 [自定义绑定](../../../../docs/framework/wcf/extending/custom-bindings.md)  
 描述什么是 <xref:System.ServiceModel.Channels.CustomBinding> 以及何时使用它。  
  
## <a name="reference"></a>参考  
 <xref:System.ServiceModel.Channels.Binding>  
  
 <xref:System.ServiceModel.Channels.BindingElement>  
  
 <xref:System.ServiceModel.Channels.CustomBinding>  
  
## <a name="related-sections"></a>相关章节  
 [扩展绑定](../../../../docs/framework/wcf/extending/extending-bindings.md)
