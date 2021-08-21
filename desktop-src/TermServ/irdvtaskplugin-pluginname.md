---
title: 'IRDVTaskPlugin PluginName 屬性 (Tspubplugincom .h) '
description: 包含工作代理程式的顯示名稱。
ms.assetid: 6f414270-e90b-4075-80fe-f918acbdd205
ms.tgt_platform: multiple
keywords:
- PluginName 屬性遠端桌面服務
- PluginName 屬性遠端桌面服務，IRDVTaskPlugin 介面
- IRDVTaskPlugin 介面遠端桌面服務，PluginName 屬性
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.PluginName
- IRDVTaskPlugin.get_PluginName
api_location:
- tspubplugincom.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 078934c8f19085bf233df78501798a8416ceadf7ba6a0b663cb14b8a8c46b223
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129329"
---
# <a name="irdvtaskpluginpluginname-property"></a>IRDVTaskPlugin：:P luginName 屬性

包含工作代理程式的顯示名稱。 此名稱僅供記錄之用。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_PluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>屬性值

工作代理程式的顯示名稱。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 Enterprise<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Tspubplugincom。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





