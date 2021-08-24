---
title: 'IResultType UID 屬性 (WdsSharedIDL .h) '
description: 此屬性包含類型的唯一識別碼。
ms.assetid: 31c2ef7d-f5a7-441e-80ea-fd7e46fded07
keywords:
- UID 屬性舊版 Windows 環境功能
- UID 屬性舊版 Windows 環境功能，IResultType 介面
- IResultType 介面舊版 Windows 環境功能，UID 屬性
topic_type:
- apiref
api_name:
- IResultType.UID
- IResultType.get_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89a67561d10d07a69ed7990f7491f12cb479060829ede212bc565230c2895c93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014568"
---
# <a name="iresulttypeuid-property"></a>IResultType：： UID 屬性

> [!NOTE]
> WindowsDesktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集的形式提供。 在更新版本中，請改用[Windows Search API](../search/-search-reference-entry-page.md) 。 

此屬性包含類型的唯一識別碼。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a>屬性值

包含 uid 的位置位址。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows只有 Server 2003 （含 SP1） \[ 桌面應用程式\]<br/>                             |
| 可轉散發套件<br/>          | Windows (WDS 的桌面搜尋) 2.6。5<br/>                                             |
| 標頭<br/>                   | <dl> <dt>WdsSharedIDL。h</dt> </dl> |



 

 





