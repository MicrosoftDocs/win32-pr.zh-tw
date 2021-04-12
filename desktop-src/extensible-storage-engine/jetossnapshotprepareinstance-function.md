---
description: 深入瞭解： JetOSSnapshotPrepareInstance 函數
title: JetOSSnapshotPrepareInstance 函式
TOCTitle: JetOSSnapshotPrepareInstance Function
ms:assetid: b4f06342-633f-47c6-be32-64ec058920fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294064(v=EXCHG.10)
ms:contentKeyID: 32765679
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepareInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8cc5179a55aabfa3324e3caab7005f4abe437a6d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104386536"
---
# <a name="jetossnapshotprepareinstance-function"></a>JetOSSnapshotPrepareInstance 函式


_**適用于：** Windows |Windows Server_

## <a name="jetossnapshotprepareinstance-function"></a>JetOSSnapshotPrepareInstance 函式

**JetOSSnapshotPrepareInstance** 函式會選取要成為快照會話一部分的特定實例。

**Windows vista：** **JetOSSnapshotPrepareInstance** 是在 windows vista 中引進的。

```cpp
JET_ERR JET_API JetOSSnapshotPrepareInstance(
  __in          JET_OSSNAPID snapId,
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

此呼叫的選項。 這個參數保留給未來使用。 唯一有效的值為 0 (零) 。

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
<td><p>JET_errInvalidParameter</p></td>
<td><p>快照集識別碼指標為 <strong>Null</strong> 或 <em>grbit</em> 參數無效。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>快照會話已在進行中。</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>快照集會話的識別碼無效。</p></td>
</tr>
</tbody>
</table>


如果此函式成功，則指定的實例將會是快照集會話的一部分。

如果此函式失敗，則不會發生引擎狀態的變更。

#### <a name="remarks"></a>備註

一般 API 順序呼叫是： [JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)，並選擇性地接著一或多個 **JetOSSnapshotPrepareInstance** 呼叫，然後再接著 [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)。 當凍結開始之後，就可以使用 [JetOSSnapshotThaw](./jetossnapshotthaw-function.md)來終止。 在準備之後的任何時間，快照集會話都可以使用 [JetOSSnapshotAbort](./jetossnapshotabort-function.md)突然終止。 將會產生快照集不同步驟的事件記錄檔專案。

如果在會話開始 ([JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)) 和凍結時間 ([JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)) 之間沒有呼叫 **JetOSSnapshotPrepareInstance** ，則引擎中所有執行中的實例都會凍結，並且成為快照會話的一部分。 發生這種情況的原因有兩種：

  - 它可為想要所有實例的使用者簡化程式碼。

  - 它允許快照集 Api 的呼叫端回溯相容性。

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
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
