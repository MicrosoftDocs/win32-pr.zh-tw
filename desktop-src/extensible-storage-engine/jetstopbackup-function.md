---
description: 深入瞭解： JetStopBackup 函數
title: JetStopBackup 函式
TOCTitle: JetStopBackup Function
ms:assetid: b7545284-2fdb-4470-8466-fc2109ad63c5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294067(v=EXCHG.10)
ms:contentKeyID: 32765682
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd11857be7096ce30f2fcf06f8ab4f975185da57
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982361"
---
# <a name="jetstopbackup-function"></a>JetStopBackup 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetstopbackup-function"></a>JetStopBackup 函式

**JetStopBackup** 函式會防止任何串流備份相關的活動繼續執行特定執行中的實例，進而以可預測的方式結束串流備份。

**Windows XP：** 這項功能是在 Windows XP 中引進。

[JetStopService](./jetstopservice-function.md) 是僅允許一個實例時的舊版呼叫。 在此情況下，唯一的作用中實例是準備進行終止的實例。

```cpp
JET_ERR JET_API JetStopBackup(void);
```

### <a name="parameters"></a>參數

此函式沒有參數。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>使用具有多個實例模式的 <a href="gg269240(v=exchg.10).md">JetStopService</a> 時，不會清除要準備終止的實例。</p><p><strong>Windows XP：</strong> 此傳回值會在 Windows XP 中引進。</p> | 



如果此函式成功，實例將開始失敗任何新的串流備份 Api。

如果此函式失敗，就不會執行在實例上進行備份終止的任何步驟，也不會發生實例狀態的變更。

#### <a name="remarks"></a>備註

備份通常是由進程機制之外的事件所觸發，而使用此 API 時，ESENT 應用程式本身會對串流備份 Api 進行任何進一步的呼叫，以使其失敗。 大部分的串流備份 Api 都會隨著 JET_errBackupAbortByServer 開始失敗。 因此，任何串流備份進度 (如 [JetReadFileInstance](./jetreadfileinstance-function.md)) 都會傳回錯誤。 備份終止 (的備份作業（例如 [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) ）仍會被允許。

#### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | 
| <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)
