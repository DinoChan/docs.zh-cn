---
title: IMetaDataEmit::DefineEvent 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineEvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineEvent
helpviewer_keywords:
- IMetaDataEmit::DefineEvent method [.NET Framework metadata]
- DefineEvent method [.NET Framework metadata]
ms.assetid: cf064bac-9a9f-41c5-9e1d-108ff7af3afe
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ce94765467899ac7c906b0dfcdf0ceb78c659b5f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
ms.locfileid: "33448199"
---
# <a name="imetadataemitdefineevent-method"></a>IMetaDataEmit::DefineEvent 方法
使用指定的元数据签名中，创建事件的定义并获取该事件定义的标记。  
  
## <a name="syntax"></a>语法  
  
```  
HRESULT DefineEvent (   
    [in]  mdTypeDef    td,   
    [in]  LPCWSTR      szEvent,   
    [in]  DWORD        dwEventFlags,   
    [in]  mdToken      tkEventType,   
    [in]  mdMethodDef  mdAddOn,   
    [in]  mdMethodDef  mdRemoveOn,   
    [in]  mdMethodDef  mdFire,   
    [in]  mdMethodDef  rmdOtherMethods[],   
    [out] mdEvent      *pmdEvent   
);  
```  
  
#### <a name="parameters"></a>参数  
 `td`  
 [in]为目标类或接口标记。 这可以是`mdTypeDef`或`mdTypeDefNil`令牌。  
  
 `szEvent`  
 [in]事件的名称。  
  
 `dwEventFlags`  
 [in]事件的标志。  
  
 `tkEventType`  
 [in]Event 类令牌。 这是`mdTypeDef`、 `mdTypeRef`，或`mdTokenNil`令牌。  
  
 `mdAddOn`  
 [in]用于订阅的事件或为 null 的方法。  
  
 `mdRemoveOn`  
 [in]用于取消订阅事件，或者为 null 的方法。  
  
 `mdFire`  
 [in]（由派生类） 中用于引发事件的方法。  
  
 `rmdOtherMethods[]`  
 [in]有关其他方法与事件关联的令牌的数组。 数组终止于`mdMethodDefNil`令牌。  
  
 `pmdEvent`  
 [out]分配给事件元数据标记。  
  
## <a name="requirements"></a>要求  
 **平台：** 请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **标头：** Cor.h  
  
 **库：** 用作 MSCorEE.dll 中的资源  
  
 **.NET framework 版本：** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅  
 [IMetaDataEmit Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [IMetaDataEmit2 Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
