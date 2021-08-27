---
description: 深入瞭解： JetTruncateLog 函數
title: JetTruncateLog 函式
TOCTitle: JetTruncateLog Function
ms:assetid: 60cbf563-4228-452a-9b20-c7b1330c4514
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269263(v=EXCHG.10)
ms:contentKeyID: 32765565
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTruncateLog
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aa924a7061e834d4398ed68adb800912261279f7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474354"
---
# <a name="jettruncatelog-function"></a>JetTruncateLog 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jettruncatelog-function"></a>JetTruncateLog 函式

**JetTruncateLog** 函式會在由 [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)起始的備份期間使用，以刪除目前的備份成功完成後，將不再需要的任何交易記錄檔。

```cpp
    JET_ERR JET_API JetTruncateLog(void);
```

### <a name="parameters"></a>參數

此函式沒有參數。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>作業失敗，因為目前的外部備份已被 <a href="gg294067(v=exchg.10).md">JetStopBackup</a>的呼叫中止。</p><p><strong>Windows Server 2003：</strong> 此傳回值會在 Windows Server 2003 中引進。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p><p><strong>Windows XP：</strong> 此傳回值會在 Windows XP 中引進。</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>備份作業失敗，因為它的呼叫順序不是。 如果有任何未處理的檔案控制代碼是針對實例使用<a href="gg269249(v=exchg.10).md">JetOpenFile</a>所建立， <strong>JetTruncateLog</strong>就會傳回這個錯誤。</p> | 
| <p>JET_errInvalidParameter</p> | <p>提供的其中一個參數包含未預期的值，或數個參數的組合產生了非預期的結果。 當指定的實例控制碼無效時， <strong>JetTruncateLog</strong> 就會發生這種情況。</p><p><strong>Windows XP：</strong> 此傳回值會在 Windows XP 中引進。</p> | 
| <p>JET_errNoBackup</p> | <p>作業失敗，因為沒有任何外部備份正在進行中。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>作業無法完成，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>作業失敗，因為嘗試使用舊版模式中的引擎 (Windows 2000 相容性模式) 只支援一個實例，而事實上有多個實例已經存在。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉中。</p> | 



如果此函式成功，則會刪除目前的備份成功完成後，將不再需要的交易記錄檔集合。 備份狀態電腦將會是最先進的，因此不再允許資料庫檔案的備份。 現在只允許開啟資料庫修補檔和交易記錄檔進行備份。

如果此函式失敗，備份狀態電腦可以是 advanced，使資料庫檔案的備份不再被允許。 可能會刪除一些小於所需數目的交易記錄檔，但一律會從最舊到最年輕刪除。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[可擴充的儲存體引擎檔案](./extensible-storage-engine-files.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)
