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
ms.openlocfilehash: 2994b636a7b8483d4b3f219648f137166b75790d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686114"
---
# <a name="ipropertyfiltercollectionremoveitem-property"></a>IPropertyFilterCollection：： RemoveItem 屬性

> [!NOTE]
> Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。 在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。 

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
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP2） \[ 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]<br/>                             |
| 可轉散發套件<br/>          | Windows 桌面搜尋 (WDS) 2.6。5<br/>                                             |
| 標頭<br/>                   | <dl> <dt>WdsSharedIDL。h</dt> </dl> |



 

 





