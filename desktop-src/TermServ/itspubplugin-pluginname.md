---
title: ItsPubPlugin pluginName 屬性
description: 捕獲外掛程式的名稱。
ms.assetid: c1ea46b6-fac6-4140-a278-cb04ee9af739
ms.tgt_platform: multiple
keywords:
- pluginName 屬性遠端桌面服務
- pluginName 屬性遠端桌面服務，ItsPubPlugin 介面
- ItsPubPlugin 介面遠端桌面服務，pluginName 屬性
topic_type:
- apiref
api_name:
- ItsPubPlugin.pluginName
- ItsPubPlugin.get_pluginName
api_location:
- Cpubplugin.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa1cd3103e901255a6226db3e128e81bb17c02e6b586a48ca434ed44932861c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118128637"
---
# <a name="itspubpluginpluginname-property"></a>ItsPubPlugin：:p luginName 屬性

捕獲外掛程式的名稱。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_pluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>屬性值

**BSTR** 變數的指標，用來接收外掛程式的名稱。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                         |
| IDL<br/>                      | <dl> <dt>Cpubplugin .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ItsPubPlugin**](/windows/desktop/api/tspubplugincom/nn-tspubplugincom-itspubplugin)
</dt> </dl>

 

 





