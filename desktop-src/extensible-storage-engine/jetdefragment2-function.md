---
description: 深入瞭解： JetDefragment2 函數
title: JetDefragment2 函式
TOCTitle: JetDefragment2 Function
ms:assetid: cfb190cf-8bd3-4479-a6a1-7c0c9e8c74ca
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294095(v=EXCHG.10)
ms:contentKeyID: 32765710
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDefragment2
- JetDefragment2A
- JetDefragment2W
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7cf6dfa2ca38fb488d2234efa8798f2619bab09a19578c8aec64e47747fdf7ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119728471"
---
# <a name="jetdefragment2-function"></a>JetDefragment2 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetdefragment2-function"></a>JetDefragment2 函式

**JetDefragment2** 函式會啟動並停止資料庫重組工作，這些工作會改善資料庫中的資料組織，並提供回呼參數以報告磁碟重組的進度。 這樣做的目的是要在資料庫內更有效率地使用現有的磁片配置，以限制資料庫成長。 它也可以確保資料更緊密地封裝，藉此減少工作集。 最後，它可以透過更妥善的資料組織來加速一般作業，藉以改善應用程式效能。

**Windows xp：****JetDefragment2** 是在 Windows xp 引進。  

**JetDefragment2** 也包含回呼函式參數，可用來報告磁碟重組程式的進度。

資料庫磁碟重組是一項線上作業，不會中斷一般資料庫活動，例如查詢作業或資料更新。 **JetDefragment2** 也不會建立所有現有資料的複本。 相反地，它會將資料庫重組。 最後， **JetDefragment2** 會復原內部資料庫空間以便重複使用，但不會釋出超過作業系統檔案系統的空間。

產生的資料格式可能更有效率，但通常不是最佳的。 磁碟重組僅限於釋出資料庫頁面以供重複使用，其中包含已經過邏輯刪除的資料。 磁碟重組也可讓資料庫頁面在某些情況下可供重複使用，方法是合併兩個頁面的資料以容納在單一頁面上。

這項作業不同于 [JetCompact](./jetcompact-function.md) ，這會讓唯讀資料庫的複本成為高度最佳的格式。

```cpp
JET_ERR JET_API JetDefragment2(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          JET_PCSTR szTableName,
  __out_opt     unsigned long* pcPasses,
  __out_opt     unsigned long* pcSeconds,
  __in          JET_CALLBACK callback,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*dbid*

要重組的資料庫。

*szTableName*

有時 *szTableName* 是必要的，有時會被禁止：

| *grbit* | *szTableName* |
| --- | --- |
| `JET_bitDefragmentBTreeBatch` | 必須是 `NULL`。 |
| `JET_bitDefragmentBTree` | 指定要重組的資料表/BTree 表名稱。 |
| *其他* | 必須是 `NULL`。 |
 
針對指定資料庫識別碼所描述的整個資料庫執行磁碟重組。

*pcPasses*

開始進行線上磁碟重組工作時，此選擇性的輸入參數會設定磁碟重組傳遞的最大數目。 停止線上磁碟重組工作時，此選擇性輸出緩衝區會設定為執行的行程數目。

當此參數設定為 Null 時，線上磁碟重組傳遞的數目是無限制的。

*pcSeconds*

開始進行線上磁碟重組工作時，此選擇性的輸入參數會設定磁碟重組的最長時間。 停止線上磁碟重組工作時，此選擇性輸出緩衝區會設定為用於重組的時間長度。

當此參數設定為 Null 或 *pcSeconds* 指向負值時，重組的最長時間是無限制的。

*回撥*

可定期重組呼叫以報告進度的回呼函數。

| *grbit* | *szTableName* |
| --- | --- |
| `JET_bitDefragmentBTreeBatch` | 必須是 `NULL`。 |
| `JET_bitDefragmentBTree` | 必須是 `NULL`。 |
| *其他* | 選擇性。


*grbit*

指定零或多個下列選項的位群組。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>值</p></th>
<th><p>意義</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitDefragmentAvailSpaceTreesOnly</p></td>
<td><p>此選項可用來重組 ESE 資料庫空間配置的可用空間部分。 資料庫空間分為兩種類型：擁有的空間和可用空間。 擁有的空間會配置給資料表或索引，而可用空間可供在資料表或索引內使用。 可用空間的行為更動態，而且需要進行線上磁碟重組，而非擁有的空間或資料表或索引資料。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDefragmentBatchStart</p></td>
<td><p>此選項可用來啟動新的磁碟重組工作。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDefragmentBatchStop</p></td>
<td><p>此選項可用來停止現有的已啟動磁碟重組工作。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDefragmentBTree</p></td>
<td><p>此選項是用來重組 szTableName 所指定的 B 型樹狀目錄。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDefragmentBTreeBatch</p></td>
<td><p>這個選項是用來呼叫整個資料庫上的 OLD2。</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>傳回碼</p></th>
<th><p>描述</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>作業已成功完成。</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseFileReadOnly</p></td>
<td><p>針對磁碟重組選擇的資料庫是唯讀的，而且無法以任何方式更新，包括磁碟重組。</p></td>
</tr>
<tr class="even">
<td><p>JET_errDistributedTransactionAlreadyPreparedToCommit</p></td>
<td><p>指定的會話處於 [準備認可] 狀態，直到目前的交易認可或回復時，才會開始新的更新。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabaseId</p></td>
<td><p>給定的資料庫識別碼與實例中的已知資料庫不相符。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>相同的會話無法同時用於一個以上的執行緒。 只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在關閉。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTransReadOnly</p></td>
<td><p>指定的會話僅具有唯讀許可權，無法啟動可能執行更新的工作，包括磁碟重組。</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemory</p></td>
<td><p>當版本存放區的設定大小不足以保存所有未處理的更新時，就會發生此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnDefragAlreadyRunning</p></td>
<td><p>已通過 JET_bitDefragmentBatchStart 選項，但是磁碟重組工作已在指定的資料庫上執行磁碟重組。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDefragNotRunning</p></td>
<td><p>已通過 JET_bitDefragmentBatchStop 選項，但目前沒有正在執行的磁碟重組工作。</p></td>
</tr>
</tbody>
</table>


成功時，會執行要求的動作，以指定的選項針對指定的資料啟動磁碟重組工作，或執行停止現有磁碟重組工作的動作。

失敗時，啟動或停止線上磁碟重組作業所要求的動作不會完成。 不會發生其他副作用。

#### <a name="remarks"></a>備註

線上磁碟重組是透過參數設定以及此 API 來控制。 預設系統參數值為 JET_OnlineDefragAll，表示已針對所有支援的資料結構啟用磁碟重組。 不過，您可以使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md)來停用線上磁碟重組，或選擇性地針對資料庫空間樹狀結構（僅限資料庫）、僅限串流檔案或這些選項的任何組合來啟用它。 如果進行線上磁碟重組的系統設定是過時的設定， **JetDefragment2** 就會將設定視為 JET_OnlineDefragAll。

每個資料庫最多隻能執行一項工作。 工作會以執行緒的形式在裝載 ESE 的進程中執行。

用來啟動線上磁碟重組工作的會話，可以在磁碟重組工作繼續時用於資料庫作業，因為磁碟重組工作會配置自己的會話。 指定的會話只會用來檢查與工作啟動會話相關聯的許可權，並不會實際用於進行磁碟重組作業。

#### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows Vista 或 Windows XP。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows server 2008 或 Windows server 2003。</p></td>
</tr>
<tr class="odd">
<td><p><strong>標頭</strong></p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
<tr class="even">
<td><p><strong>程式庫</strong></p></td>
<td><p>使用 ESENT。</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>需要 ESENT.dll。</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>實作為 <strong>JetDefragment2W</strong> (Unicode) 和 <strong>JetDefragment2A</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetCompact](./jetcompact-function.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)
