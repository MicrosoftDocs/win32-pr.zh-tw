---
title: 'IResultProperty DataType 屬性 (WdsSharedIDL .h) '
description: 屬性資料類型。
ms.assetid: 2bf83256-0d69-48f2-aa7d-d34dcba17050
keywords:
- DataType 屬性舊版 Windows 環境功能
- DataType 屬性舊版 Windows 環境功能，IResultProperty 介面
- IResultProperty 介面舊版 Windows 環境功能，DataType 屬性
topic_type:
- apiref
api_name:
- IResultProperty.DataType
- IResultProperty.get_DataType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f669fdbb01459e99edb0ccc9ba75fed1cbd60ebfe789fdb4393d217239cdc1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755257"
---
# <a name="iresultpropertydatatype-property"></a>IResultProperty：:D ataType 屬性

> [!NOTE]
> WindowsDesktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集的形式提供。 在更新版本中，請改用[Windows Search API](../search/-search-reference-entry-page.md) 。 

屬性資料類型。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_DataType(
  [out, retval] VARTYPE *vt
);
```



## <a name="property-value"></a>屬性值

傳回屬性資料類型的指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows只有 Server 2003 （含 SP1） \[ 桌面應用程式\]<br/>                             |
| 可轉散發套件<br/>          | Windows (WDS 的桌面搜尋) 2.6。5<br/>                                             |
| 標頭<br/>                   | <dl> <dt>WdsSharedIDL。h</dt> </dl> |



 

 





