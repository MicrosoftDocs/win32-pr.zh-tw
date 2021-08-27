---
description: 深入瞭解： JetEscrowUpdate 函數
title: JetEscrowUpdate 函式
TOCTitle: JetEscrowUpdate Function
ms:assetid: e509b6c9-a8ce-4898-a426-485e286869fa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294125(v=EXCHG.10)
ms:contentKeyID: 32765739
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEscrowUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9f037b8c26829d7b1f3a10b05e1d4bd83bd186a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469795"
---
# <a name="jetescrowupdate-function"></a>JetEscrowUpdate 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetescrowupdate-function"></a>JetEscrowUpdate 函式

**JetEscrowUpdate** 函數會在一個資料行上執行不可部分完成的加法運算。 此函數可讓多個會話同時更新相同的記錄，而不會發生衝突。

```cpp
    JET_ERR JET_API JetEscrowUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in          void* pv,
      __in          unsigned long cbMax,
      __out_opt     void* pvOld,
      __in          unsigned long cbOldMax,
      __out_opt     unsigned long* pcbOldActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*columnid*

要更新之資料行的 *columnid* 。

*光伏*

包含資料行之加數的緩衝區指標。

*cbMax*

包含加數的緩衝區大小。

*pvOld*

將會忽略) 中儲存之資料行的目前值的輸出緩衝區， (版本控制。

*cbOldMax*

將接收資料行目前值的輸出緩衝區大小上限。 目前只支援 JET_coltypLong，因此緩衝區的長度必須是4個位元組或0個位元組。 如果 *pvOld* 為 Null，則 *cbOldMax* 應為0。

*pcbOldActual*

接收輸出緩衝區中所接收的實際原始值資料量。

*grbit*

指定零或多個下列選項的位群組。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitEscrowNoRollback</p> | <p>即使執行保管更新的會話具有其交易回復，但這種更新將不會復原。 請注意，因為記錄檔記錄可能不會排清到磁片，所以使用此旗標完成的最新的證書處理更新可能會在發生損毀時遺失。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errAlreadyPrepared</p> | <p>資料指標具有以 <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>準備的更新。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>傳入了不正確緩衝區大小。 目前只支援 JET_coltypLong，因此緩衝區必須是4個位元組。</p> | 
| <p>JET_errInvalidOperation</p> | <p>指定了不正確資料行。 必須使用指定的 JET_bitColumnEscrowUpdate 來建立資料行。 只有 JET_coltypLong 的固定資料行可以指定為可更新的可更新資料行。</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>資料指標必須在記錄上，才能更新資料行。</p> | 
| <p>JET_errNotInTransaction</p> | <p>交易更新只能由交易中的會話執行。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errPermissionDenied</p> | <p>資料指標不能是唯讀的，而是更新記錄。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>相同的會話無法同時從一個以上的執行緒使用。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 
| <p>JET_errTransReadOnly</p> | <p>會話必須有寫入權限，才能更新記錄。</p> | 
| <p>JET_errWriteConflict</p> | <p>要求衝突更新時傳回的錯誤。</p> | 



#### <a name="remarks"></a>備註

一般來說，如果兩個會話嘗試同時更新記錄，除非會話已完全序列化，否則第二個會話會收到 JET_errWriteConflict 錯誤。 若要將兩個更新相同記錄的會話序列化，第二個會話必須在第一次交易認可交易之後啟動其交易。 如需詳細資訊，請參閱 [JetBeginTransaction](./jetbegintransaction-function.md) 。

相同記錄中的多個資料行可以進行證書更新。 這些更新不會影響彼此。

只有 **JetEscrowUpdate** 作業會彼此相容。 如果有兩個不同的會話嘗試準備更新或刪除相同的記錄，則會產生寫入衝突。


| <p></p> | <p></p> | <p>會話 B<br /><strong>JetEscrowUpdate</strong></p> | <p><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a></p> | <p><a href="gg269315(v=exchg.10).md">JetDelete</a></p> | 
|---------|---------|--------------------------------------------------------|---------------------------------------------------------------|--------------------------------------------------------|
| <p></p> | <p><strong>JetEscrowUpdate</strong></p> | <p>JET_errSuccess</p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | 
| <p></p> | <p><a href="gg269288(v=exchg.10).md">JetUpdate</a></p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | 
| <p>會話 A</p> | <p><a href="gg269315(v=exchg.10).md">JetDelete</a></p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | 



除非 JET_bitEscrowNoRollback 是) 指定的，否則會使用 [JetRollback](./jetrollback-function.md) (來建立版本的託管作業。 **JetEscrowUpdate** 會傳回儲存在資料庫中之資料行的原始值，因為應用程式可能會想要在叫用 sentinel 值時執行特殊動作。 [JetRetrieveColumn](./jetretrievecolumn-function.md) 會傳回正確設定資料行版本的視圖，並忽略並行會話所做的更新。

假設有兩個會話在相同記錄的相同資料行上運作，我們可以查看其運作方式。 假設資料行的開頭值為0。


| <p>工作階段</p> | <p>作業</p> | <p>儲存的值</p> | <p>傳回值</p> | 
|----------------|------------------|---------------------|-----------------------|
| <p>A</p> | <p><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></p> | <p></p> | <p></p> | 
| <p>A</p> | <p><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></p> | <p></p> | <p>0</p> | 
| <p>A</p> | <p><strong>JetEscrowUpdate</strong> (4) </p> | <p>4</p> | <p>0</p> | 
| <p>A</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>4</p> | 
| <p>B</p> | <p><a href="gg294083(v=exchg.10).md">JetBeginTransaction</a></p> | <p></p> | <p></p> | 
| <p>B</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>0</p> | 
| <p>B</p> | <p><strong>JetEscrowUpdate</strong> (3) </p> | <p>7</p> | <p>4</p> | 
| <p>B</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>3</p> | 
| <p>A</p> | <p><strong>JetEscrowUpdate</strong> (2) </p> | <p>9</p> | <p>7</p> | 
| <p>A</p> | <p><strong>JetEscrowUpdate</strong> (-7) </p> | <p>2</p> | <p>9</p> | 
| <p>B</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>3</p> | 
| <p>A</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>-1</p> | 
| <p>B</p> | <p><a href="gg269273(v=exchg.10).md">JetRollback</a></p> | <p>-1</p> | <p></p> | 
| <p>A</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>-1</p> | 



不建議將執行交易更新的相同交易中的記錄取代為記錄。 尤其是，如果記錄上的更新是以一個 [JET_TABLEID](./jet-tableid.md) 準備，而另一個 [JET_TABLEID](./jet-tableid.md) 用來將更新記錄，則在呼叫 [JetUpdate](./jetupdate-function.md) 時，將會遺失已更新的保管。 即使在更新期間未設定「託管」資料行，也會發生這種情況。

當可更新的可更新資料行值為零時，就可以觸發特殊的行為。 只有當 **JetEscrowUpdate** 作業導致資料行的值為零時，才會發生這種行為。 動作不會立即發生，但會在造成資料行值為零之交易之後的某段時間發生。 資料行的值仍然必須為零 (也就是，如果沒有任何其他會話修改了資料行) 。 如果資料行是使用 JET_bitColumnDeleteOnZero 建立的，將會刪除包含此資料行的記錄。 如果資料行是使用 JET_bitColumnFinalize 所建立，則會發出回呼。 損毀可能會導致這些動作不會發生，但是 (使用 [JetDefragment](./jetdefragment-function.md) 函式的線上維護) 將會正確地重做動作。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetUpdate](./jetupdate-function.md)
