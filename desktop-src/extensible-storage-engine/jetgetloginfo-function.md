---
description: 深入瞭解： JetGetLogInfo 函數
title: JetGetLogInfo 函式
TOCTitle: JetGetLogInfo Function
ms:assetid: a9d14830-d731-4d47-bdc2-c0660a08678e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294055(v=EXCHG.10)
ms:contentKeyID: 32765665
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLogInfoA
- JetGetLogInfoW
- JetGetLogInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 889e660254610441e56204c2585049e3c7e5ad38
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465825"
---
# <a name="jetgetloginfo-function"></a>JetGetLogInfo 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetgetloginfo-function"></a>JetGetLogInfo 函式

**JetGetLogInfo** 函式會在 [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)所起始的備份期間使用，以查詢資料庫修補檔的名稱和交易記錄檔的名稱，這些檔案應該會成為備份檔案集的一部分。 之後可能會使用 [JetOpenFile](./jetopenfile-function.md) 來開啟這些檔案，並使用 [JetReadFile](./jetreadfile-function.md)進行讀取。

```cpp
    JET_ERR JET_API JetGetLogInfo(
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>參數

*szz*

輸出緩衝區會接收 null 結束字串的清單，這些字串會描述資料庫修補檔和交易記錄檔的集合，而這些檔案應該是備份檔案集的一部分。

此緩衝區中傳回的字串清單，與登錄所用的多重字串格式相同。 每個以 null 終止的字串會依序傳回，後面接著最後一個 null 結束字元。

*cbMax*

輸出緩衝區的大小上限（以位元組為單位）。

*pcbActual*

接收輸出緩衝區中收到的實際字串資料量。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>作業失敗，因為目前的外部備份已被 <a href="gg294067(v=exchg.10).md">JetStopBackup</a>的呼叫中止。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>備份作業失敗，因為它的呼叫順序不是。 如果有任何未完成的檔案控制代碼使用<a href="gg269249(v=exchg.10).md">JetOpenFile</a>建立實例， <strong>JetGetLogInfo</strong>將會傳回此錯誤。</p> | 
| <p>JET_errInvalidParameter</p> | <p>提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。 當指定的實例控制碼無效 (Windows XP 和更新版本) 時， <strong>JetGetLogInfo</strong>就會發生這種情況。</p> | 
| <p>JET_errNoBackup</p> | <p>作業失敗，因為沒有任何外部備份正在進行中。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>作業失敗，因為嘗試使用舊版模式中的引擎 (Windows 2000 相容性模式) 只有當有多個實例存在時，才支援一個實例。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 



成功時，在提供的輸出緩衝區中，會將資料庫修補檔和交易記錄檔集上所要求的資訊放入備份檔案集的一部分。 備份狀態電腦將會是最先進的，因此不再允許資料庫檔案的備份。 現在只允許開啟資料庫修補檔和交易記錄檔進行備份。

失敗時，輸出緩衝區的狀態是未定義的。 失敗會導致整個實例的整個備份進程取消。

#### <a name="remarks"></a>備註

請務必注意，如果輸出緩衝區太小而無法接受備份檔案集中應包含的完整檔案清單，則此 API 不會傳回錯誤或警告。 應用程式應該一律提供緩衝區來接收此清單的實際大小，並使用該資訊來判斷清單是否已遭截斷。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | | <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetGetLogInfoW</strong> (Unicode) 和 <strong>JetGetLogInfoA</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)
