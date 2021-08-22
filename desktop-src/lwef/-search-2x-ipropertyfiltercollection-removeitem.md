---
title: 'IPropertyFilterCollection RemoveItem 屬性 (WdsSharedIDL .h) '
description: 移除集合中的特定篩選。
ms.assetid: a8b8a1f7-d47a-45dc-81c9-f01ecf6c1560
keywords:
- RemoveItem 屬性舊版 Windows 環境功能
- RemoveItem 屬性舊版 Windows 環境功能，IPropertyFilterCollection 介面
- IPropertyFilterCollection 介面舊版 Windows 環境功能，RemoveItem 屬性
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.RemoveItem
- IPropertyFilterCollection.put_RemoveItem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54822e95e2ea7d6e10fdd5bbf833adb63b51cb01e8d860ce77f550432b41e926
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755417"
---
# <a name="ipropertyfiltercollectionremoveitem-property"></a>IPropertyFilterCollection：： RemoveItem 屬性

> [!NOTE]
> WindowsDesktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集的形式提供。 在更新版本中，請改用[Windows Search API](../search/-search-reference-entry-page.md) 。 

移除集合中的特定篩選。

此屬性是唯寫的。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_RemoveItem(
  [in] long index
);
```



## <a name="property-value"></a>屬性值

接受要移除之篩選的索引指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows只有 Server 2003 （含 SP1） \[ 桌面應用程式\]<br/>                             |
| 可轉散發套件<br/>          | Windows (WDS 的桌面搜尋) 2.6。5<br/>                                             |
| 標頭<br/>                   | <dl> <dt>WdsSharedIDL。h</dt> </dl> |



 

 





