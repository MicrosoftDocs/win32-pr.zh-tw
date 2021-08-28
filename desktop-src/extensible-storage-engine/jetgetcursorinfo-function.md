---
description: 深入瞭解： JetGetCursorInfo 函數
title: JetGetCursorInfo 函式
TOCTitle: JetGetCursorInfo Function
ms:assetid: e779fa5d-1d7e-46f1-80c9-f7c819279188
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294126(v=EXCHG.10)
ms:contentKeyID: 32765740
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCursorInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c0b5d3410ddb7f4210317508739b4f7dd00dd592
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470774"
---
# <a name="jetgetcursorinfo-function"></a>JetGetCursorInfo 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetgetcursorinfo-function"></a>JetGetCursorInfo 函式

**JetGetCursorInfo** 函數是用來判斷資料指標的目前記錄更新是否會根據記錄的目前更新狀態而產生寫入衝突。 即使 **JetGetCursorInfo** 傳回 JET_errSuccess，還是可能會傳回寫入衝突，因為另一個會話可能會在目前的會話更新相同記錄之前更新記錄。

```cpp
    JET_ERR JET_API JetGetCursorInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫將使用的會話。

*tableid*

將用於此呼叫的資料指標。

*pvResult*

保留供未來使用。

*cbMax*

必須設定為 0 (零) ，否則未使用。 它存在於未來的功能。

*InfoLevel*

必須設定為 0 (零) ，否則未使用。 它存在於未來的功能。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errInvalidParameter</p> | <p>可能是 <em>cbMax</em> 不是 0 (零) 或 <em>InfoLevel</em> 不是 0 (零) 。</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>資料指標目前不在記錄上，因此無法傳回邏輯記錄的資訊。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>相同的會話無法同時用於一個以上的執行緒。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 
| <p>JET_errWriteConflict</p> | <p>資料指標目前的記錄已由另一個會話更新，且此會話的此記錄更新會導致寫入衝突。</p> | 



成功時，此作業對資料指標的位置沒有任何作用，但只表示沒有任何其他會話目前已更新此記錄。

失敗時，如果傳回負錯誤碼，則資料指標或資料庫不會有任何影響。

#### <a name="remarks"></a>備註

這項作業不會影響資料指標或資料的狀態。 它只會傳回錯誤碼，描述呼叫會話的目前記錄更新是否已知為產生 JET_errWriteConflict，或未知而無法傳回 JET_errWriteConflict。 如果另一個會話已更新此記錄以使用此記錄，將會確定此會話的這項記錄更新會導致寫入衝突。 在此會話認可或回復交易至交易層級 0 (零) 之前，這會是正確的。 但是，如果 **JetGetCursorInfo** 傳回 JET_errSuccess，則在目前的會話之前，另一個會話仍可能更新此記錄，因此在目前的交易中，此會話的目前記錄更新仍可能會導致寫入衝突。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetLock](./jetgetlock-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetUpdate](./jetupdate-function.md)
