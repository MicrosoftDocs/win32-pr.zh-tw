---
title: 'IPropertyFilterCollection AddItem 屬性 (WdsSharedIDL .h) '
description: 將新的篩選準則加入至集合。
ms.assetid: 01078e7a-811a-4dfb-b122-4801f39413d8
keywords:
- AddItem 屬性舊版 Windows 環境功能
- AddItem 屬性舊版 Windows 環境功能，IPropertyFilterCollection 介面
- IPropertyFilterCollection 介面舊版 Windows 環境功能，AddItem 屬性
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.AddItem
- IPropertyFilterCollection.get_AddItem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeafec95549fefa244dff6ff44ad9110150ae1b410e38b423a0a31f09cf54194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755445"
---
# <a name="ipropertyfiltercollectionadditem-property"></a>IPropertyFilterCollection：： AddItem 屬性

> [!NOTE]
> WindowsDesktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集的形式提供。 在更新版本中，請改用[Windows Search API](../search/-search-reference-entry-page.md) 。 

將新的篩選準則加入至集合。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_AddItem(
  [out, retval] IPropertyFilter **filter
);
```



## <a name="property-value"></a>屬性值

傳回新篩選的位址指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows只有 Server 2003 （含 SP1） \[ 桌面應用程式\]<br/>                             |
| 可轉散發套件<br/>          | Windows (WDS 的桌面搜尋) 2.6。5<br/>                                             |
| 標頭<br/>                   | <dl> <dt>WdsSharedIDL。h</dt> </dl> |



 

 





