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
ms.openlocfilehash: 1804c0abd249d93470cb2570f5bd58c600e8d3be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508316"
---
# <a name="iresulttypepropertycount-property"></a>IResultType：:P ropertyCount 屬性

> [!NOTE]
> Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。 在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。 

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
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP2） \[ 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]<br/>                             |
| 可轉散發套件<br/>          | Windows 桌面搜尋 (WDS) 2.6。5<br/>                                             |
| 標頭<br/>                   | <dl> <dt>WdsSharedIDL。h</dt> </dl> |



 

 





