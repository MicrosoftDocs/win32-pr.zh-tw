---
title: 'IResultType PreceivedType 屬性 (WdsSharedIDL .h) '
description: 這個屬性包含用來識別索引中之類型的字串。
ms.assetid: 26d5f14c-162a-4ded-ac72-875561b8c977
keywords:
- PreceivedType 屬性舊版 Windows 環境功能
- PreceivedType 屬性舊版 Windows 環境功能，IResultType 介面
- IResultType 介面舊版 Windows 環境功能，PreceivedType 屬性
topic_type:
- apiref
api_name:
- IResultType.PreceivedType
- IResultType.get_PreceivedType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 765a770dc07f1fc0287e861ca79fc2aa941ea7cc425fff29e5e4c5772410c06e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014612"
---
# <a name="iresulttypepreceivedtype-property"></a>IResultType：:P receivedType 屬性

> [!NOTE]
> WindowsDesktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集的形式提供。 在更新版本中，請改用[Windows Search API](../search/-search-reference-entry-page.md) 。 

這個屬性包含用來識別索引中之類型的字串。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_PreceivedType(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>屬性值

傳回在索引中 identifyint 類型之字串的位址。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows只有 Server 2003 （含 SP1） \[ 桌面應用程式\]<br/>                             |
| 可轉散發套件<br/>          | Windows (WDS 的桌面搜尋) 2.6。5<br/>                                             |
| 標頭<br/>                   | <dl> <dt>WdsSharedIDL。h</dt> </dl> |



 

 





