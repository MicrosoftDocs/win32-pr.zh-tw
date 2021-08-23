---
title: 'IResultProperty IndexColumn 屬性 (WdsSharedIDL .h) '
description: 索引中的屬性資料行名稱。
ms.assetid: a043be43-49ef-46e0-bfb6-01104288e9ef
keywords:
- IndexColumn 屬性舊版 Windows 環境功能
- IndexColumn 屬性舊版 Windows 環境功能，IResultProperty 介面
- IResultProperty 介面舊版 Windows 環境功能，IndexColumn 屬性
topic_type:
- apiref
api_name:
- IResultProperty.IndexColumn
- IResultProperty.get_IndexColumn
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a78d91b9e823dbf8d3c7a2273247706f9ae2bb04c6f64d08f5555eb875023c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118754771"
---
# <a name="iresultpropertyindexcolumn-property"></a>IResultProperty：： IndexColumn 屬性

> [!NOTE]
> WindowsDesktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集的形式提供。 在更新版本中，請改用[Windows Search API](../search/-search-reference-entry-page.md) 。 

索引中的屬性資料行名稱。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_IndexColumn(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a>屬性值

傳回索引中資料行名稱的指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows只有 Server 2003 （含 SP1） \[ 桌面應用程式\]<br/>                             |
| 可轉散發套件<br/>          | Windows (WDS 的桌面搜尋) 2.6。5<br/>                                             |
| 標頭<br/>                   | <dl> <dt>WdsSharedIDL。h</dt> </dl> |



 

 





