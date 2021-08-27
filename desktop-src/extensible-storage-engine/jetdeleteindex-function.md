---
description: 深入瞭解： JetDeleteIndex 函數
title: JetDeleteIndex 函式
TOCTitle: JetDeleteIndex Function
ms:assetid: c540503b-d5a6-47f2-9113-9650891c4b6d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294081(v=EXCHG.10)
ms:contentKeyID: 32765696
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteIndexW
- JetDeleteIndexA
- JetDeleteIndex
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a934581754477f336415926716a9a8c7e6097d81
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985891"
---
# <a name="jetdeleteindex-function"></a>JetDeleteIndex 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetdeleteindex-function"></a>JetDeleteIndex 函式

**JetDeleteIndex** 函數會從資料表中刪除索引。

```cpp
    JET_ERR JET_API JetDeleteIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName
    );
```

### <a name="parameters"></a>參數

*sesid*

要用於 API 呼叫的資料庫會話內容。

*tableid*

包含要刪除之資料行的資料表。

*szIndexName*

要刪除的索引名稱。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errFixedDDL</p> | <p>嘗試刪除固定資料表中的索引 (例如，一個是以 JET_bitTableCreateFixedDDL) 所建立的。</p> | 
| <p>JET_errFixedInheritedDDL</p> | <p>嘗試刪除範本資料表中的索引。 範本資料表具有固定的 DDL。</p> | 
| <p>JET_errIndexNotFound</p> | <p>在 <em>szIndexName</em> 中找不到名為的索引。</p> | 
| <p>JET_errPermissionDenied</p> | <p>因為資料表是以唯讀方式開啟，所以無法更新。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>多個執行緒嘗試使用相同的資料庫會話。</p> | 
| <p>JET_errTransReadOnly</p> | <p>交易已開啟為唯讀交易。</p> | 



#### <a name="remarks"></a>備註

成功時，會刪除索引，因此無法再使用。 使用索引時，不能有任何使用中的交易。

成功時，會在第一筆記錄之前設定貨幣。

#### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | 
| <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 
| <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetDeleteIndexW</strong> (Unicode) 和 <strong>JetDeleteIndexA</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)
