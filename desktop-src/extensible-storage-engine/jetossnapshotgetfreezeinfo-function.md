---
description: 深入瞭解： JetOSSnapshotGetFreezeInfo 函數
title: JetOSSnapshotGetFreezeInfo 函式
TOCTitle: JetOSSnapshotGetFreezeInfo Function
ms:assetid: b94eaf91-7407-4c62-ab1e-3249ad076c1a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294070(v=EXCHG.10)
ms:contentKeyID: 32765685
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotGetFreezeInfo
- JetOSSnapshotGetFreezeInfoA
- JetOSSnapshotGetFreezeInfoW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2fbfd3fb31567ea73b8266b5aeba506d62be7714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987282"
---
# <a name="jetossnapshotgetfreezeinfo-function"></a>JetOSSnapshotGetFreezeInfo 函式


_**適用于：** Windows |Windows Server_

## <a name="jetossnapshotgetfreezeinfo-function"></a>JetOSSnapshotGetFreezeInfo 函式

**JetOSSnapshotGetFreezeInfo** 函式會在任何指定的時間，取得屬於快照會話一部分的實例和資料庫清單。

**Windows vista：**  **JetOSSnapshotGetFreezeInfo** 是在 windows vista 中引進的。

```cpp
    JET_ERR JET_API JetOSSnapshotGetFreezeInfo(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*snapId*

要啟動之快照集會話的識別碼。

*pcInstanceInfo*

目前正在執行的實例數目，這些實例是快照集會話的一部分。

*paInstanceInfo*

結構的陣列，每個執行中的實例各一個，描述其所屬的實例和資料庫。

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
<td><p>JET_errOutOfMemory</p></td>
<td><p>因為記憶體不足，所以函數失敗。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p><em>pcInstanceInfo</em> 或 <em>paInstanceInfo</em> 為 <strong>Null</strong>。</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>快照集會話的識別碼無效。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>快照集會話不在進行中。</p></td>
</tr>
</tbody>
</table>


如果此函式成功，則會正確填滿實例資訊，而且必須在稍後使用傳回的實例資訊陣列的指標呼叫 [JetFreeBuffer](./jetfreebuffer-function.md) 來釋放。

如果此函式失敗，則不會發生引擎狀態的變更。

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>實作為 <strong>JetOSSnapshotGetFreezeInfoW</strong> (Unicode) 和 <strong>JetOSSnapshotGetFreezeInfoA</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[錯誤處理參數](./error-handling-parameters.md)  
[可擴充儲存引擎錯誤](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetFreeBuffer](./jetfreebuffer-function.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
