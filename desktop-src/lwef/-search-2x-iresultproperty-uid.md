---
title: 'IResultProperty UID 屬性 (WdsSharedIDL .h) '
description: 屬性的唯一識別碼。
ms.assetid: b5cee5b3-78b4-4d2a-b442-f6624497ef71
keywords:
- UID 屬性舊版 Windows 環境功能
- UID 屬性舊版 Windows 環境功能，IResultProperty 介面
- IResultProperty 介面舊版 Windows 環境功能，UID 屬性
topic_type:
- apiref
api_name:
- IResultProperty.UID
- IResultProperty.get_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08921e366cca2be40a8a79fe43d7a15cec54f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024951"
---
# <a name="iresultpropertyuid-property"></a>IResultProperty：： UID 屬性

> [!NOTE]
> Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。 在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。 

屬性的唯一識別碼。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a>屬性值

傳回唯一屬性識別碼的指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP2） \[ 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]<br/>                             |
| 可轉散發套件<br/>          | Windows 桌面搜尋 (WDS) 2.6。5<br/>                                             |
| 標頭<br/>                   | <dl> <dt>WdsSharedIDL。h</dt> </dl> |



 

 





