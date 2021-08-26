---
title: 'IResultType PropertyCount 屬性 (WdsSharedIDL .h) '
description: 這個屬性包含型別所公開的屬性數目。
ms.assetid: 4ca4b18c-d228-4275-b00d-06c6f227e0ae
keywords:
- PropertyCount 屬性舊版 Windows 環境功能
- PropertyCount 屬性舊版 Windows 環境功能，IResultType 介面
- IResultType 介面舊版 Windows 環境功能，PropertyCount 屬性
topic_type:
- apiref
api_name:
- IResultType.PropertyCount
- IResultType.get_PropertyCount
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6952f2efb6e0d14be22daf71e352747915b2ba05bf543d764ee9af5f496715ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014628"
---
# <a name="iresulttypepropertycount-property"></a>IResultType：:P ropertyCount 屬性

> [!NOTE]
> WindowsDesktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集的形式提供。 在更新版本中，請改用[Windows Search API](../search/-search-reference-entry-page.md) 。 

這個屬性包含型別所公開的屬性數目。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_PropertyCount(
  [out, retval] long *count
);
```



## <a name="property-value"></a>屬性值

傳回公開的屬性數目的位址。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows只有 Server 2003 （含 SP1） \[ 桌面應用程式\]<br/>                             |
| 可轉散發套件<br/>          | Windows (WDS 的桌面搜尋) 2.6。5<br/>                                             |
| 標頭<br/>                   | <dl> <dt>WdsSharedIDL。h</dt> </dl> |



 

 





