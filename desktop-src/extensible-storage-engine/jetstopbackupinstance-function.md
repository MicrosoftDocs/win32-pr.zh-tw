---
description: 深入瞭解： JetStopBackupInstance 函數
title: JetStopBackupInstance 函式
TOCTitle: JetStopBackupInstance Function
ms:assetid: 7d008eac-2a32-402b-91ef-965ed3c3b0de
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269309(v=EXCHG.10)
ms:contentKeyID: 32765599
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c4dae676cfbbb0f2509a7d86fbb6507b8e2110f1
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987241"
---
# <a name="jetstopbackupinstance-function"></a>JetStopBackupInstance 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetstopbackupinstance-function"></a>JetStopBackupInstance 函式

**JetStopBackupInstance** 函式會防止串流備份相關的活動繼續執行特定執行中的實例，進而以可預測的方式結束串流備份。

**Windows xp：****JetStopBackupInstance** 是在 Windows xp 引進。  

```cpp
    JET_ERR JET_API JetStopBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>參數

*實例*

識別要用於 API 呼叫的正在執行的實例。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errInvalidParameter</p> | <p>指定的實例參數有不正確值 (不是目前正在執行) 的實例。</p><p><strong>Windows XP：</strong> 此傳回值會在 Windows XP 中引進。</p> | 



如果此函式成功，則指定的實例將開始失敗任何新的串流備份 Api。

如果此函式失敗，就不會執行在實例上進行備份終止的任何步驟，也不會發生實例狀態的變更。

#### <a name="remarks"></a>備註

備份通常是由進程機制之外的事件所觸發，而使用此 API 時，ESENT 應用程式本身會對串流備份 Api 進行任何進一步的呼叫，以使其失敗。 大部分的串流備份 Api 都會隨著 JET_errBackupAbortByServer 開始失敗。 因此，任何串流備份進度 (例如 [JetReadFileInstance](./jetreadfileinstance-function.md)) 都會傳回錯誤。 備份終止 (的備份作業（例如 [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) ）仍會被允許。

#### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista 或 Windows XP。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008 或 Windows server 2003。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | 
| <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)
