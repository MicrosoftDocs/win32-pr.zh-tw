---
description: 深入瞭解： JetTruncateLogInstance 函數
title: JetTruncateLogInstance 函式
TOCTitle: JetTruncateLogInstance Function
ms:assetid: 9b6852c6-a991-4d7b-bc54-49092f788751
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269352(v=EXCHG.10)
ms:contentKeyID: 32765639
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTruncateLogInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7286b97b80c323eb6bba7b9d28057bf45eec3920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985613"
---
# <a name="jettruncateloginstance-function"></a>JetTruncateLogInstance 函式


_**適用于：** Windows |Windows Server_

## <a name="jettruncateloginstance-function"></a>JetTruncateLogInstance 函式

**JetTruncateLogInstance** 函式是在由 [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)所起始的備份期間，用來刪除目前的備份成功完成後，將不再需要的任何交易記錄檔。

**Windows xp：**  **JetTruncateLogInstance** 是在 windows xp 中引進的。

```cpp
    JET_ERR JET_API JetTruncateLogInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>參數

*實例*

此呼叫所要使用的實例。

針對 Windows 2000，無法使用接受此參數的 API 變體，因為只支援一個實例。 在此情況下，這種全域實例的使用是隱含的。

若為 Windows XP 和更新版本，則只有在引擎處於舊版模式時，才會呼叫不接受這個參數的 API 變數 (Windows 2000 相容性模式) 只支援一個實例。 否則，作業將會失敗，並 JET_errRunningInMultiInstanceMode。

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
<td><p>JET_errBackupAbortByServer</p></td>
<td><p><strong>Windows Server 2003：</strong>  此傳回值是在 Windows Server 2003 中引進。</p>
<p>作業失敗，因為目前的外部備份已被 <a href="gg294067(v=exchg.10).md">JetStopBackup</a>的呼叫中止。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackupSequence</p></td>
<td><p>備份作業失敗，因為它的呼叫順序不是。 如果有任何未處理的檔案控制代碼是針對實例使用<a href="gg269249(v=exchg.10).md">JetOpenFile</a>所建立， <a href="gg269263(v=exchg.10).md">JetTruncateLog</a>就會傳回這個錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>提供的其中一個參數包含未預期的值，或數個參數的組合產生了非預期的結果。 當指定的實例控制碼無效時， <a href="gg269263(v=exchg.10).md">JetTruncateLog</a> 就會發生這種情況。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoBackup</p></td>
<td><p>作業失敗，因為沒有任何外部備份正在進行中。</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>作業無法完成，因為與會話相關聯的實例正在進行還原作業。</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>作業失敗，因為嘗試使用舊版模式中的引擎 (Windows 2000 相容性模式) 在事實中，如果有多個實例存在，則只支援一個實例。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在關閉中。</p></td>
</tr>
</tbody>
</table>


如果此函式成功，則會刪除目前的備份成功完成後，將不再需要的交易記錄檔集合。 備份狀態電腦將會是最先進的，因此不再允許資料庫檔案的備份。 現在只允許開啟資料庫修補檔和交易記錄檔進行備份。

如果此函式失敗，備份狀態電腦可以是 advanced，使資料庫檔案的備份不再被允許。 可能會刪除一些小於所需數目的交易記錄檔，但一律會從最舊到最年輕刪除。

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

[可擴充儲存引擎檔案](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)
