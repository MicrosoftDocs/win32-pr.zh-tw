---
description: 深入瞭解： JetGetAttachInfoInstance 函數
title: JetGetAttachInfoInstance 函式
TOCTitle: JetGetAttachInfoInstance Function
ms:assetid: 978e7817-0720-42fc-a5c1-46e4d44239f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269350(v=EXCHG.10)
ms:contentKeyID: 32765637
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetAttachInfoInstanceW
- JetGetAttachInfoInstanceA
- JetGetAttachInfoInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8bbfac13e1536c0a8261e3c63a4308a84a60cf09
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474094"
---
# <a name="jetgetattachinfoinstance-function"></a>JetGetAttachInfoInstance 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetgetattachinfoinstance-function"></a>JetGetAttachInfoInstance 函式

**JetGetAttachInfoInstance** 函式是在 [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)所起始的備份期間，用來查詢實例，以取得應該成為備份檔案集一部分的資料庫檔案名。 只會考慮目前使用 [JetAttachDatabase](./jetattachdatabase-function.md) 連接到實例的資料庫。 之後可能會使用 [JetOpenFileInstance](./jetopenfileinstance-function.md) 來開啟這些檔案，並使用 [JetReadFileInstance](./jetreadfileinstance-function.md)進行讀取。

**Windows xp： JetGetAttachInfoInstance** 是在 Windows xp 引進。

```cpp
    JET_ERR JET_API JetGetAttachInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>參數

*實例*

此呼叫所要使用的實例。

針對 Windows 2000，無法使用接受此參數的 API 變體，因為只支援一個實例。 在此情況下，這種全域實例的使用是隱含的。

針對 Windows XP 和更新版本，只有在引擎處於舊版模式時，才會呼叫不接受這個參數的 API 變體 (Windows 2000 相容性模式) 只支援一個實例。 否則，作業將會失敗，並 JET_errRunningInMultiInstanceMode。

*szz*

輸出緩衝區，此輸出緩衝區會接收以 null 結束字串的清單，這些字串會描述應該是備份檔案集一部分的資料庫檔案集。 此緩衝區中傳回的字串清單，與登錄所用的多重字串格式相同。 每個以 null 終止的字串會依序傳回，後面接著最後一個 null 結束字元。

*cbMax*

輸出緩衝區的大小上限（以位元組為單位）。

*pcbActual*

輸出緩衝區的指標，此輸出緩衝區會接收實際的字串資料量。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>作業失敗，因為目前的外部備份已被 <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>的呼叫中止。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>的結果。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>備份作業失敗，因為它的呼叫順序不是。 如果目前的備份不是完整備份， <strong>JetGetAttachInfoInstance</strong>會傳回此錯誤。</p> | 
| <p>JET_errInvalidParameter</p> | <p>提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。 當指定的實例控制碼無效 (Windows XP 和更新版本) 時， <strong>JetGetAttachInfoInstance</strong>就會發生這種情況。</p> | 
| <p>JET_errNoBackup</p> | <p>作業失敗，因為沒有任何外部備份正在進行中。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>作業失敗，因為嘗試使用舊版模式中的引擎 (Windows 2000 相容性模式) 只有當有多個實例存在時，才支援一個實例。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 



成功時，在所提供的輸出緩衝區中，會將所要求的資料庫檔案集合的資訊放入備份檔案集的一部分。

失敗時，輸出緩衝區的狀態是未定義的。 失敗會導致整個實例的整個備份進程取消。

#### <a name="remarks"></a>備註

請務必注意，如果輸出緩衝區太小而無法接受備份檔案集中應包含的完整檔案清單，則此 API 不會傳回錯誤或警告。 應用程式應該一律提供緩衝區來接收此清單的實際大小，並使用該資訊來判斷清單是否已遭截斷。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista 或 Windows XP。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008 或 Windows server 2003。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | | <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetGetAttachInfoInstanceW</strong> (Unicode) 和 <strong>JetGetAttachInfoInstanceA</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)  
[JetOpenFileInstance](./jetopenfileinstance-function.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopBackupInstance](./jetstopbackupinstance-function.md)  
[JetStopServiceInstance](./jetstopserviceinstance-function.md)
