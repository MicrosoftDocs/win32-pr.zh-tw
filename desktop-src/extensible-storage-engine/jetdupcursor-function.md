---
description: 深入瞭解： JetDupCursor 函數
title: JetDupCursor 函式
TOCTitle: JetDupCursor Function
ms:assetid: 154b7d2d-4656-46b3-873c-2e194a9059b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269193(v=EXCHG.10)
ms:contentKeyID: 32765496
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupCursor
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a96f93357bc3df143fa63ed690295e40980cfc94
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472654"
---
# <a name="jetdupcursor-function"></a>JetDupCursor 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetdupcursor-function"></a>JetDupCursor 函式

**JetDupCursor** 函式會重複開啟的資料指標，並將控制碼傳回至重複的資料指標。 如果複製的資料指標是唯讀資料指標，則重復資料指標也是唯讀資料指標。 任何與建立搜尋索引鍵或更新記錄相關的狀態都不會複製到重複的資料指標中。 此外，原始資料指標的位置不會複製到重複的資料指標中。 重複的資料指標一律會在叢集索引上開啟，而且其位置一律會在資料表的第一個資料列上。

```cpp
    JET_ERR JET_API JetDupCursor(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_TABLEID* ptableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*ptableid*

*Tableid* 的指標。

*grbit*

保留供未來使用。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errOutOfCursors</p> | <p>沒有任何可用的資料指標資源存在。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>相同的會話無法同時用於一個以上的執行緒。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 



成功時， *ptableid* 會設定為重複的資料指標。

失敗時，不會進行任何變更。 *Tableid* 的狀態不變。

#### <a name="remarks"></a>備註

重複的資料指標沒有複製整個資料指標狀態。 重復資料指標的位置（包括目前的索引）通常與指定的資料指標不同。 在叢集索引和資料表的第一個資料列上，一律會傳回重複的資料指標。 如果資料表是空的，則重複的資料指標不會在任何資料列上。

使用 **JetDupCursor** 開啟的資料表通常應該以 [JetCloseTable](./jetclosetable-function.md)關閉。 在交易中呼叫 **JetDupCursor** 時，就會發生此規則的例外狀況，且會使用 [JetRollback](./jetrollback-function.md)) 將交易回復 (。 回復交易時，資料指標會自動關閉。 在此情況下，使用 [JetCloseTable](./jetclosetable-function.md)關閉資料表是錯誤的。

可以同時開啟的資料表數目會直接受到 [JET_paramMaxOpenTables](./resource-parameters.md)的影響。 如需詳細資訊，請參閱 [系統參數](./extensible-storage-engine-system-parameters.md) 。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)  
[系統參數](./extensible-storage-engine-system-parameters.md)
