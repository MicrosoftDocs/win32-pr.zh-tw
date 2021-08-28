---
description: 深入瞭解： JetRenameTable 函數
title: JetRenameTable 函式
TOCTitle: JetRenameTable Function
ms:assetid: face9341-58e3-450b-980d-08eb1dc3e9d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294142(v=EXCHG.10)
ms:contentKeyID: 32765756
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameTableW
- JetRenameTableA
- JetRenameTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0d91f7af4896e5cb3145321de087a2803aaddd09
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985741"
---
# <a name="jetrenametable-function"></a>JetRenameTable 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetrenametable-function"></a>JetRenameTable 函式

**JetRenameTable** 函數可以用來變更現有資料表的名稱。

```cpp
    JET_ERR JET_API JetRenameTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szName,
      __in          const tchar* szNameNew
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*dbid*

此呼叫所要使用的資料庫。

*szName*

即將重新命名之資料表的目前名稱。

*szNameNew*

將重新命名之資料表的新名稱。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errInvalidDatabase</p> | <p>指定的資料庫無效。</p><p>此錯誤只有在暫存資料庫上嘗試資料表重新命名作業時，才會在 Windows 2000 中傳回。 在稍後的版本中，會傳回此案例的 JET_errInvalidDatabaseId。</p> | 
| <p>JET_errInvalidDatabaseId</p> | <p>指定的資料庫識別碼無效。</p> | 
| <p>JET_errInvalidName</p> | <p>其中一個指定的物件名稱無效。 所有物件名稱都必須符合同一組規則。 這些規則如下：</p><ul><li><p>物件名稱必須由 ASCII 字元組成。</p></li><li><p>物件名稱的長度必須至少有一個字元。</p></li><li><p>物件名稱的長度不得超過 JET_cbNameMost (64) 個字元。</p></li><li><p>物件名稱不能以空格開頭。</p></li><li><p>物件名稱不能包含 ASCII 控制字元 (0x00 到 0x1F) 。</p></li><li><p>物件名稱不能包含驚嘆號 (！ ) ，句號 (。 ) ，左括弧 ( [) ，或右括弧 (]，只有在驗證後，才會將字串的部分設為第一個空格 ) 如果有任何 (將用於物件名稱。 這實際上是指物件名稱不能包含空格。</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。 在下列情況下， <strong>JetRenameTable</strong> 可能會發生：</p><ul><li><p><em>>szname</em> 為 Null。</p></li><li><p><em>szNameNew</em> 為 Null。</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errObjectNotFound</p> | <p>此資料庫的指定資料表不存在。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>相同的會話無法同時用於一個以上的執行緒。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 
| <p>JET_errTransReadOnly</p> | <p>無法在唯讀交易範圍內完成更新。 唯讀交易是指使用 JET_bitTransactionReadOnly 呼叫 <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> 來啟動的交易。</p><p>只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 



成功時，指定資料庫中指定之資料表的名稱會永久變更為新的名稱。

失敗時，將不會變更資料庫狀態。

#### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | 
| <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 
| <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetRenameTableW</strong> (Unicode) 和 <strong>JetRenameTableA</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)
