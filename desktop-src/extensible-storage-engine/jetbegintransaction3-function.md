---
description: 深入瞭解： JetBeginTransaction3 函數
title: JetBeginTransaction3 函式
TOCTitle: JetBeginTransaction3 Function
ms:assetid: 7f8ed059-0b97-46fa-9925-e46cdcbee6ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835043(v=EXCHG.10)
ms:contentKeyID: 49894665
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetBeginTransaction3
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b263cb18c09df8205a49e1c4a1a683e339803f35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973002"
---
# <a name="jetbegintransaction3-function"></a>JetBeginTransaction3 函式


_**適用于：** Windows |Windows Server_

**JetBeginTransaction3** 函式會讓會話進入交易並建立新的儲存點。 您可以在單一會話中多次呼叫此函數，以建立額外的儲存點。 您可以使用這些儲存點，選擇性地保留或捨棄資料庫的變更。

**JetBeginTransaction3** 函式是在 Windows 8 作業系統中引進的。

``` c++
JET_ERR JET_API JetBeginTransaction3(
  __in          JET_SESID sesid,
  __in          int64 trxid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*trxid*

使用者提供的選擇性識別碼，用來識別交易。

*grbit*

一組位，指定下表所列的零或多個呼叫選項值。

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
<td><p>JET_bitTransactionReadOnly</p></td>
<td><p>交易不會修改資料庫。 如果嘗試更新，這項作業將會失敗，並產生 JET_errTransReadOnly 的回應碼。 除非指定的會話尚未存在於交易中，否則會忽略這個選項。 從 Windows XP 開始的 Windows 作業系統版本中有提供此選項。</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>傳回值

此函數會傳回 [JET_ERR](./jet-err.md) 資料類型，其中包含下表所列的其中一個傳回碼。 如需可能的可延伸儲存引擎 (ESE) 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>傳回碼</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>作業已成功完成。</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因為呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a> 函數。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p>
<p>自 Windows XP 起的 Windows 版本會傳回這個傳回碼。</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>相同的會話無法同時用於一個以上的執行緒。 從 Windows XP 開始的 Windows 版本會傳回這個錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在關閉。</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransTooDeep</p></td>
<td><p>無法啟動新的交易，因為會話已經是 database engine 允許的最大儲存點深度。</p></td>
</tr>
</tbody>
</table>


成功時，所提供的會話將會在交易內。 如果會話先前是在交易內，則會建立新的儲存點。

失敗時，會話的交易式狀態將保持不變。 不會變更資料庫狀態。

#### <a name="remarks"></a>備註

如需交易運作方式的詳細資訊，請參閱 [JetBeginTransaction](./jetbegintransaction-function.md)。

#### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows 8。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows Server 2012。</p></td>
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
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetResetSessionCoNtext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSessionCoNtext](./jetsetsessioncontext-function.md)  
[系統參數](./extensible-storage-engine-system-parameters.md)
