---
title: 'IResultVerb Name 屬性 (WdsSharedIDL .h) '
description: 這個屬性會傳回動詞的 cononical 名稱指標，例如 print、open 等等。
ms.assetid: e911ef1c-0ac9-4b70-a3af-c05e42bd1f0f
keywords:
- 名稱屬性舊版 Windows 環境功能
- Name 屬性舊版 Windows 環境功能，IResultVerb 介面
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
ms.openlocfilehash: c2c831ea0dad36f733995062d8a76fc27d4cc837
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933971"
---
# <a name="iresultverbname-property"></a>IResultVerb：： Name 屬性

> [!NOTE]
> Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。 在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。 

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
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP2） \[ 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]<br/>                             |
| 可轉散發套件<br/>          | Windows 桌面搜尋 (WDS) 2.6。5<br/>                                             |
| 標頭<br/>                   | <dl> <dt>WdsSharedIDL。h</dt> </dl> |



 

 





