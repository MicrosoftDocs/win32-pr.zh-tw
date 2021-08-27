---
description: 深入瞭解： JetGetTruncateLogInfoInstance 函數
title: JetGetTruncateLogInfoInstance 函式
TOCTitle: JetGetTruncateLogInfoInstance Function
ms:assetid: 1ecb2f2f-2cad-4c55-9296-5e5893b57695
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269199(v=EXCHG.10)
ms:contentKeyID: 32765502
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTruncateLogInfoInstanceA
- JetGetTruncateLogInfoInstanceW
- JetGetTruncateLogInfoInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 36583267277f7c5254adc85047ce99631f6c03ef
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479074"
---
# <a name="jetgettruncateloginfoinstance-function"></a>JetGetTruncateLogInfoInstance 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetgettruncateloginfoinstance-function"></a>JetGetTruncateLogInfoInstance 函式

**JetGetTruncateLogInfoInstance** 函式會在由 [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)起始的備份期間使用，以查詢實例是否有交易記錄檔的名稱，可在備份順利完成之後安全地刪除。

**Windows xp：****JetGetTruncateLogInfoInstance** 是在 Windows xp 引進。  

```cpp
    JET_ERR JET_API JetGetTruncateLogInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>參數

*實例*

此呼叫所要使用的實例。

*szz*

輸出緩衝區，可接收以 null 終止字串的清單，這些字串描述可在成功完成備份之後安全刪除的交易記錄檔集合。

此緩衝區中傳回的字串清單，與登錄所使用的多字串格式相同。 每個以 null 終止的字串會依序傳回，後面接著最後一個 null 結束字元。

*cbMax*

輸出緩衝區的大小上限（以位元組為單位）。

*pcbActual*

輸出緩衝區的指標，此輸出緩衝區會接收實際的字串資料量。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errInvalidParameter</p> | <p>其中一個提供的參數包含未預期的值，或數個參數值的組合導致非預期的結果。</p><p><strong>Windows XP 和更新版本：</strong> 當指定的實例控制碼無效時， <strong>JetGetTruncateLogInfoInstance</strong>就會發生這種情況。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p><p><strong>Windows XP：</strong> 此傳回值是在 Windows XP 中引進。</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>作業失敗，因為目前的外部備份已被 <a href="gg294067(v=exchg.10).md">JetStopBackup</a>的呼叫中止。</p><p><strong>Windows XP：</strong> 此傳回值是在 Windows XP 中引進。</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>備份作業失敗，因為它的呼叫順序不是。</p> | 
| <p>JET_errNoBackup</p> | <p>作業失敗，因為沒有任何外部備份正在進行中。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>作業無法完成，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉中。</p> | 
| <p><strong>JetGetTruncateLogInfoInstance</strong></p> | <p>有未處理的檔案控制代碼，該控制碼是使用實例的 <a href="gg269249(v=exchg.10).md">JetOpenFile</a> 所建立。</p> | 



如果此函式成功，則在已成功完成備份之後，可以安全地刪除的一組交易記錄檔所要求的相關資訊，將會放在提供這些記錄的輸出緩衝區中。 備份狀態電腦將會是最先進的，因此不再允許資料庫檔案的備份。 您只可以開啟資料庫修補檔和交易記錄檔，以進行備份。

如果此函式失敗，輸出緩衝區的狀態就會是未定義的。 失敗會導致整個實例的整個備份進程取消。

#### <a name="remarks"></a>備註

如果輸出緩衝區太小，無法接受備份檔案集中應包含的完整檔案清單，則此 API 不會傳回錯誤或警告。 應用程式應該一律提供緩衝區來接收此清單的實際大小，並使用該資訊來判斷清單是否已遭截斷。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista 或 Windows XP。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008 或 Windows server 2003。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | | <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetGetTruncateLogInfoInstanceW</strong> (Unicode) 和 <strong>JetGetTruncateLogInfoInstanceA</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetResetSessionCoNtext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
