---
description: 深入瞭解： JetEndExternalBackupInstance2 函數
title: JetEndExternalBackupInstance2 函式
TOCTitle: JetEndExternalBackupInstance2 Function
ms:assetid: a30961f7-a1fb-44fe-881a-d46bf8f743b3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294047(v=EXCHG.10)
ms:contentKeyID: 32765646
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackupInstance2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f4235736d9933a510922e5fcc4ffc72c27cd0037
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477614"
---
# <a name="jetendexternalbackupinstance2-function"></a>JetEndExternalBackupInstance2 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetendexternalbackupinstance2-function"></a>JetEndExternalBackupInstance2 函式

**JetEndExternalBackupInstance2** 函數會結束外部備份會話。 此 API 是一系列 Api 中的最後一個 API，必須呼叫這些 api，以執行線上 (非 VSS 型) 備份成功。

**Windows xp： JetEndExternalBackupInstance2** 是在 Windows xp 引進。

```cpp
    JET_ERR JET_API JetEndExternalBackupInstance2(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*實例*

此呼叫所要使用的實例。

**Windows 2000：** 針對 Windows 2000，無法使用接受此參數的 API 變體，因為只支援一個實例。 在此情況下，這種全域實例的使用是隱含的。

**Windows XP：** 針對 Windows XP 和更新版本，只有在引擎處於舊版模式時，才會呼叫不接受這個參數的 API 變體 (Windows 2000 相容性模式) 只支援一個實例。 否則，作業將會失敗，並 JET_errRunningInMultiInstanceMode。

*grbit*

指定零或多個下列選項的位群組。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitBackupEndAbort<br />0x0002</p> | <p>用戶端應用程式正在中止備份。</p> | 
| <p>JET_bitBackupEndNormal<br />0x0001</p> | <p>用戶端應用程式已完全完成備份，且正常結束。</p> | 
| <p>JET_bitBackupTruncateDone<br />0x0100</p> | <p><strong>Windows Vista：</strong>JET_bitBackupTruncateDone 是 Windows Vista 引進。</p><p>引擎可以在適當的情況下標記資料庫標頭 (例如，完整備份已完成) ，即使未完成截斷的呼叫也是一樣。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errBackupAbortByCaller</p> | <p><strong>Windows XP：</strong>此傳回值會在 Windows XP 中引進。</p><p>呼叫端在備份順序中途終止備份，而不會向 <a href="gg294067(v=exchg.10).md">JetStopBackup</a>發出任何信號。 當 Windows Server 2003 和更新版本中的備份用戶端發生錯誤時，就會產生此錯誤。 在 Windows XP 中，系統會針對外部備份順序的蓄意終止傳回此錯誤。</p> | 
| <p>JET_errBackupAbortByServer</p> | <p><strong>Windows Server 2003：</strong>此傳回值會在 Windows Server 2003 中引進。</p><p>作業失敗，因為目前的外部備份已被 <a href="gg294067(v=exchg.10).md">JetStopBackup</a>的呼叫中止。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p><strong>Windows XP：</strong>此傳回值會在 Windows XP 中引進。</p><p>作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p> | 
| <p>JET_errNoBackup</p> | <p>作業失敗，因為沒有任何外部備份正在進行中。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>作業無法完成，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>作業失敗，因為嘗試使用舊版模式中的引擎 (Windows 2000 相容性模式) 只支援一個實例，而事實上有多個實例已經存在。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉中。</p> | 



如果函式成功，則外部備份成功。 [成功] 表示所有檔案 (例如，資料庫和記錄檔) ，適用于 [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) 中指定的 (備份類型，可從備份引擎取出。 備份的檔案可以透過「硬復原」 ([JetExternalRestore](./jetexternalrestore-function.md)) 來復原。

如果此函式失敗，則外部備份通常會結束。 失敗表示因為用戶端或應用程式使用錯誤，所以備份無效。 檢查此 API 的傳回碼以確認備份順序是否成功，是很重要的。

#### <a name="remarks"></a>備註

如果引擎設定為記錄事件，則會記錄事件，以指出外部備份的解決方式。

如果備份順序未依順序完成，而且成功呼叫 [JetEndExternalBackup](./jetendexternalbackup-function.md)，則後續的增量備份可能會包含比預期的應用程式更多的資料。

如需外部備份 API 序列的詳細資訊，請參閱 [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)。

在 Windows Vista 之前，如果未執行記錄截斷，則引擎會將備份視為複本備份。 不過，備份可能是未完成截斷的一般備份 (例如，如果有卸離的資料庫) 。 JET_bitBackupTruncateDone 選項可以用來通知引擎，並允許適當的資料庫標頭修改。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista 或 Windows XP。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008 或 Windows server 2003。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[錯誤處理參數](./error-handling-parameters.md)  
[可擴充的儲存體引擎錯誤](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JetExternalRestore](./jetexternalrestore-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)
