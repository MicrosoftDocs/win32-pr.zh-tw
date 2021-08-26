---
description: 深入瞭解： JetSetCursorFilter 函數
title: JetSetCursorFilter 函式
TOCTitle: JetSetCursorFilter Function
ms:assetid: 3cea5beb-2cf8-4053-8e7f-7b8645580ef0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835040(v=EXCHG.10)
ms:contentKeyID: 49894662
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetCursorFilter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5958d288e8b101795d1c8e4b4db789ade4b98418
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477514"
---
# <a name="jetsetcursorfilter-function"></a>JetSetCursorFilter 函式


_**適用于：** Windows |Windows伺服器_

**JetSetCursorFilter** 函式會設定 [JetMove](./jetmove-function.md)函數的簡單篩選陣列。

**JetSetCursorFilter** 函式是在 Windows 8 作業系統中引進的。

``` c++
JET_ERR JET_API JetSetCursorFilter(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in_ecount(cFilters)  JET_INDEX_COLUMN* rgFilters,
  __in          DWORD cFilters,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>參數

*sesid*

要用於 API 呼叫的資料庫會話內容。

*tableid*

要放置的游標。

*rgFilters*

簡單的記錄篩選。

*cFilters*

篩選的數目。

*grbit*

一組位，指定下表所列的零或多個移動選項。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>None</p> | <p>預設選項。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回 [JET_ERR](./jet-err.md) 資料類型，其中包含下表所列的其中一個傳回碼。 如需可能的可延伸儲存體引擎 (ESE) 錯誤的詳細資訊，請參閱[可擴展的儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 



#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows 8。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows Server 2012。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JetMove](./jetmove-function.md)  
[JET_ERR](./jet-err.md)
