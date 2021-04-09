---
title: 'IPropertyFilter IndexColumn 屬性 (WdsSharedIDL .h) '
description: 要篩選之屬性的索引資料行名稱。
ms.assetid: 18ce0c89-bdaa-4f83-bf03-c11b55a842f5
keywords:
- IndexColumn 屬性舊版 Windows 環境功能
- IndexColumn 屬性舊版 Windows 環境功能，IPropertyFilter 介面
- IPropertyFilter 介面舊版 Windows 環境功能，IndexColumn 屬性
topic_type:
- apiref
api_name:
- IPropertyFilter.IndexColumn
- IPropertyFilter.get_IndexColumn
- IPropertyFilter.put_IndexColumn
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1e55a59b4615f4b6c19dcb5f07d16394d2531f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025046"
---
# <a name="ipropertyfilterindexcolumn-property"></a>IPropertyFilter：： IndexColumn 屬性

> [!NOTE]
> Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。 在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。 

要篩選之屬性的索引資料行名稱。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_IndexColumn(
  [in]          BSTR column
);

HRESULT get_IndexColumn(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a>屬性值

設定資料行屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP2） \[ 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]<br/>                             |
| 可轉散發套件<br/>          | Windows 桌面搜尋 (WDS) 2.6。5<br/>                                             |
| 標頭<br/>                   | <dl> <dt>WdsSharedIDL。h</dt> </dl> |



 

 





