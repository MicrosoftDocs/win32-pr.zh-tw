---
description: 深入瞭解： JetEndExternalBackupInstance 函數
title: JetEndExternalBackupInstance 函式
TOCTitle: JetEndExternalBackupInstance Function
ms:assetid: 2256f63e-91f5-44ad-b67e-506dd71ffa94
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269204(v=EXCHG.10)
ms:contentKeyID: 32765507
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackupInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a017a0dbb4fa2f92c3e43a9dd2ff5649b65ee375
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027142"
---
# <a name="jetendexternalbackupinstance-function"></a>JetEndExternalBackupInstance 函式


_**適用于：** Windows |Windows Server_

## <a name="jetendexternalbackupinstance-function"></a>JetEndExternalBackupInstance 函式

**JetEndExternalBackupInstance** 函數會結束外部備份會話。 此 API 是一系列 Api 中的最後一個 API，必須呼叫這些 api，以執行線上 (非 VSS 型) 備份成功。

**Windows xp： JetEndExternalBackupInstance** 是在 windows xp 中引進的。

```cpp
    JET_ERR JET_API JetEndExternalBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>參數

*實例*

此呼叫所要使用的實例。

**Windows 2000：** 針對 Windows 2000，無法使用接受此參數的 API 變體，因為只支援一個實例。 在此情況下，這種全域實例的使用是隱含的。

**WINDOWS XP：** 若為 Windows XP 和更新版本，則只有在引擎處於舊版模式時，才會呼叫不接受這個參數的 API 變數 (Windows 2000 相容性模式) 只支援一個實例。 否則，作業將會失敗，並 JET_errRunningInMultiInstanceMode。

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
<td><p>JET_errBackupAbortByCaller</p></td>
<td><p><strong>WINDOWS XP：  </strong>這個傳回值是在 Windows XP 中引進的。</p>
<p>呼叫端在備份順序中途終止備份，而不會向 <a href="gg294067(v=exchg.10).md">JetStopBackup</a>發出任何信號。 此錯誤是 Windows Server 2003 和更新版本中的備份用戶端發生錯誤的結果。 在 Windows XP 上，會針對外部備份順序的刻意終止傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBackupAbortByServer</p></td>
<td><p><strong>Windows Server 2003：  </strong>此傳回值是在 Windows Server 2003 中引進。</p>
<p>作業失敗，因為目前的外部備份已被 <a href="gg294067(v=exchg.10).md">JetStopBackup</a>的呼叫中止。</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p><strong>WINDOWS XP：  </strong>這個傳回值是在 Windows XP 中引進的。</p>
<p>作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackup</p></td>
<td><p>作業失敗，因為沒有任何外部備份正在進行中。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>作業無法完成，因為與會話相關聯的實例正在進行還原作業。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>作業失敗，因為嘗試使用舊版模式中的引擎 (Windows 2000 相容性模式) 只支援一個實例，而事實上有多個實例已經存在。</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在關閉中。</p></td>
</tr>
</tbody>
</table>


如果函式成功，則外部備份成功。 [成功] 表示所有檔案 (例如，資料庫和記錄檔) ，適用于 [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) 中指定的 (備份類型，可從備份引擎取出。 備份的檔案可以透過「硬復原」 ([JetExternalRestore](./jetexternalrestore-function.md)) 來復原。

如果此函式失敗，則外部備份通常會結束。 失敗表示因為用戶端或應用程式使用錯誤，所以備份無效。 檢查此 API 的傳回碼以確認備份順序是否成功，是很重要的。

#### <a name="remarks"></a>備註

如果引擎設定為記錄事件，則會記錄事件，以指出外部備份的解決方式。

如果備份順序未依順序完成，而且成功呼叫 [JetEndExternalBackup](./jetendexternalbackup-function.md)，則後續的增量備份可能會包含比預期的應用程式更多的資料。

如需外部備份 API 序列的詳細資訊，請參閱 [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)。

在 Windows Vista 之前，如果未執行記錄截斷，引擎會將備份視為複本備份。 不過，備份可能是未完成截斷的一般備份 (例如，如果有卸離的資料庫) 。 JET_bitBackupTruncateDone 選項可以用來通知引擎這項資訊，並允許適當的資料庫標頭修改。

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
<td><p>需要 Windows Server 2008 或 Windows Server 2003。</p></td>
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
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JET_ERR](./jet-err.md)  
[JetExternalRestore](./jetexternalrestore-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)
