---
description: 深入瞭解： JetDeleteTable 函數
title: JetDeleteTable 函式
TOCTitle: JetDeleteTable Function
ms:assetid: e8a4131f-a69b-41f3-94c6-a1607fc23c1f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294128(v=EXCHG.10)
ms:contentKeyID: 32765742
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteTable
- JetDeleteTableA
- JetDeleteTableW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2cdac49d766835a0d26a3b9d474b8759a552ed1d
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984901"
---
# <a name="jetdeletetable-function"></a>JetDeleteTable 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetdeletetable-function"></a>JetDeleteTable 函式

**JetDeleteTable** 函數會刪除 ESE 資料庫中的資料表。

```cpp
    JET_ERR JET_API JetDeleteTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName
    );
```

### <a name="parameters"></a>參數

*sesid*

要用於 API 呼叫的資料庫會話內容。

*dbid*

用於 API 呼叫的資料庫識別碼。

*szTableName*

要刪除的資料表名稱。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errTableInUse</p> | <p>嘗試刪除資料表，而另一個會話具有開啟的資料表識別碼 (<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>) 具有 <a href="gg294118(v=exchg.10).md">JetOpenTable</a> 或 <a href="gg269193(v=exchg.10).md">JetDupCursor</a>。</p> | 
| <p>JET_errCannotDeletetemporary 資料表</p> | <p>嘗試刪除臨時表。 當臨時表以 <a href="gg294087(v=exchg.10).md">JetCloseTable</a>關閉時，就會自動刪除。</p> | 
| <p>JET_errCannotDeleteTemplateTable</p> | <p>嘗試刪除範本資料表，也就是可以繼承 DDL 的資料表。</p> | 



#### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | 
| <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 
| <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetDeleteTableW</strong> (Unicode) 和 <strong>JetDeleteTableA</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_DBID](./jet-dbid.md)  
[JET_SESID](./jet-sesid.md)  
[JetCloseTable](./jetclosetable-function.md)
