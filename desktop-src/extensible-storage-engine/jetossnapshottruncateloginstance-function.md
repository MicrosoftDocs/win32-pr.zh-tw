---
description: 深入瞭解： JetOSSnapshotTruncateLogInstance 函數
title: JetOSSnapshotTruncateLogInstance 函式
TOCTitle: JetOSSnapshotTruncateLogInstance Function
ms:assetid: ddc51957-5b89-4abf-9193-c34ef626a63e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294115(v=EXCHG.10)
ms:contentKeyID: 32765729
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLogInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cef30d012c28c809bb35d59a82fd596ba69bd175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689528"
---
# <a name="jetossnapshottruncateloginstance-function"></a>JetOSSnapshotTruncateLogInstance 函式


_**適用于：** Windows |Windows Server_

## <a name="jetossnapshottruncateloginstance-function"></a>JetOSSnapshotTruncateLogInstance 函式

**JetOSSnapshotTruncateLogInstance** 函式會在快照會話期間截斷指定之實例的記錄檔。

**Windows vista：**  **JetOSSnapshotTruncateLogInstance** 是在 windows vista 中引進的。

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLogInstance(
      __in          const JET_OSSNAPID snapId,
      __in          JET_INSTANCE instance,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*snapId*

快照集會話的識別碼。

*實例*

此呼叫將使用的實例。

*grbit*

此呼叫的選項。 這個參數可以有下列值的組合。

*grbit* 可以是下列其中一個值：

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
<td><p>JET_bitAllDatabasesSnapshot</p></td>
<td><p>附加所有資料庫，讓儲存引擎可以計算並進行記錄截斷。</p></td>
</tr>
<tr class="even">
<td><p>0 (零)</p></td>
<td><p>不會發生截斷。</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。

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
<td><p>JET_errInvalidGrbit</p></td>
<td><p><em>Grbit</em>參數無效。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>快照會話不是處於截斷可能發生的狀態。 可能的原因包括：</p>
<ul>
<li><p>呼叫會在快照集會話超時之後完成。</p></li>
<li><p>此會話已指定為複製快照集。</p></li>
</ul></td>
</tr>
</tbody>
</table>


如果此函式成功，則會截斷屬於快照會話一部分的一個或所有實例的記錄檔（如果可能的話）。

#### <a name="remarks"></a>備註

只有在使用 JET_bitContinueAfterThaw 選項建立快照集時，才應該呼叫這個函數。 否則，快照集會話會在呼叫 [JetOSSnapshotThaw](./jetossnapshotthaw-function.md)之後結束。

#### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows Vista。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows Server 2008。</p></td>
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

[錯誤處理參數](./error-handling-parameters.md)  
[可擴充儲存引擎錯誤](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
