---
title: 'IResultVerb Name 屬性 (WdsSharedIDL .h) '
description: 這個屬性會傳回動詞的 cononical 名稱指標，例如 print、open 等等。
ms.assetid: e911ef1c-0ac9-4b70-a3af-c05e42bd1f0f
keywords:
- 名稱屬性舊版 Windows 環境功能
- 名稱屬性舊版 Windows 環境功能，IResultVerb 介面
- IResultVerb 介面舊版 Windows 環境功能，名稱屬性
topic_type:
- apiref
api_name:
- IResultVerb.Name
- IResultVerb.get_Name
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e58377a9286a6e3fe4abb8d0a1d4ebf9e10bd3072295484ca32fb56d465a6f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976968"
---
# <a name="iresultverbname-property"></a>IResultVerb：： Name 屬性

> [!NOTE]
> WindowsDesktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集的形式提供。 在更新版本中，請改用[Windows Search API](../search/-search-reference-entry-page.md) 。 

這個屬性會傳回動詞的 cononical 名稱指標，例如 print、open 等等。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_Name(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>屬性值

名稱是動詞 cononical 名稱的指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows只有 Server 2003 （含 SP1） \[ 桌面應用程式\]<br/>                             |
| 可轉散發套件<br/>          | Windows (WDS 的桌面搜尋) 2.6。5<br/>                                             |
| 標頭<br/>                   | <dl> <dt>WdsSharedIDL。h</dt> </dl> |



 

 





