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
ms.openlocfilehash: 97f5aa6ff6659047e9be48fd7b7a41f652c5cfd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968773"
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
| Idl<br/>                      | <dl> <dt>Cpubplugin .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ItsPubPlugin**](/windows/desktop/api/tspubplugincom/nn-tspubplugincom-itspubplugin)
</dt> </dl>

 

 





