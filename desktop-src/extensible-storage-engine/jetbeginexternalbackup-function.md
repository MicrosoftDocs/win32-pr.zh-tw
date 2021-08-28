---
description: 深入瞭解： JetBeginExternalBackup 函數
title: JetBeginExternalBackup 函式
TOCTitle: JetBeginExternalBackup Function
ms:assetid: 702e6cbf-4648-40f2-b2eb-6194759d4cde
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269292(v=EXCHG.10)
ms:contentKeyID: 32765584
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8d0e47a117c044899a8b078290be622cfecdae91
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482904"
---
# <a name="jetbeginexternalbackup-function"></a>JetBeginExternalBackup 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetbeginexternalbackup-function"></a>JetBeginExternalBackup 函式

**JetBeginExternalBackup** 函式會在引擎和資料庫在線上且使用中時，起始外部備份。 **JetBeginExternalBackup** 是一系列函式中的第一個函式，必須呼叫這些函式，以執行 (非 VSS 型) 備份成功連線。

外部備份可以用來執行完整、增量或差異備份。

備份將會是模糊的，因為備份會與交易記錄中的單一時間點一致，但無法控制確切的時間點。

```cpp
    JET_ERR JET_API JetBeginExternalBackup(
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*grbit*

指定零或多個下列選項的位群組。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitBackupAtomic</p> | <p>此旗標已被取代。 使用此位會導致傳回 JET_errInvalidgrbit。</p> | 
| <p>JET_bitBackupIncremental</p> | <p>建立增量備份，而不是完整備份。 這表示只會備份自上次完整或增量備份之後的記錄檔。</p> | 
| <p>JET_bitBackupSnapshot</p> | <p>保留供未來使用。 針對 Windows XP 定義。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errBackupInProgress</p> | <p>如果外部備份或快照集備份已在處理中，則會傳回此錯誤，直到 <strong>JetBeginExternalBackup</strong> (或呼叫它的其中一個變數) 為止。 ESE 一次只允許一個線上備份。</p> | 
| <p>JET_errBackupNotAllowedYet</p> | <p>實例或資料庫引擎處於復原或處於關機或終止階段。</p> | 
| <p>JET_errCheckpointCorrupt</p> | <p>在完整備份上，無法讀取檢查點檔案，或無法驗證檔案。</p> | 
| <p>JET_errCheckpointFileNotFound</p> | <p>在完整備份上，找不到檢查點檔案。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p><p><strong>Windows XP：</strong>此傳回值會在 Windows XP 中引進。</p> | 
| <p>JET_errInvalidBackup</p> | <p>啟用迴圈記錄，並 JET_bitBackupIncremental 指定的備份類型。 如需如何控制迴圈或非迴圈記錄的詳細資訊，請參閱<strong>交易記錄錯誤</strong>中的<a href="gg269235(v=exchg.10).md">JET_paramCircularLog</a> 。</p> | 
| <p>JET_errInvalidgrbit</p> | <p>一或多個 <em>grbit</em> 成員無效。</p> | 
| <p>JET_errLoggingDisabled</p> | <p>修復或記錄已停用。 如果已停用記錄功能，您就無法進行線上備份。 如需有關記錄和復原的詳細資訊，請參閱 <a href="gg269235(v=exchg.10).md">JET_paramRecovery</a>。</p> | 
| <p>JET_errLogWriteFail</p> | <p>引擎已停止寫入記錄磁片磁碟機，因為記錄檔已滿或磁片 IO 錯誤。</p> | 
| <p>JET_errMissingFullBackup</p> | <p>增量備份是指定 (與 JET_bitBackupIncremental) ，而不是針對記錄集的其中一個連接資料庫所建立的完整備份。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errOutOfMemory</p> | <p>作業失敗，因為無法配置足夠的記憶體來完成。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>作業無法完成，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>作業失敗，因為嘗試使用舊版模式中的引擎 (Windows 2000 相容性模式) 只有當有多個實例存在時，才支援一個實例。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉中。</p> | 



如果函式成功，則會起始外部備份並初始化備份狀態引擎。 您現在可以呼叫後續的 Api 來完成外部備份順序，以及串流或讀取資料庫檔案、資料庫修補檔 (是否支援) 和記錄檔。 您可以記錄外部備份已開始的事件。

如果函式失敗，將不會起始備份會話。 如果另一個備份會話正在進行中，則不會取消。

#### <a name="remarks"></a>備註

**JetBeginExternalBackup**) 所啟動的外部備份程式 (，其設計目的是要讓整個實例的模糊交易線上備份成為串流的目標裝置。 備份將會包含所有附加至實例的資料庫檔案，其使用 [JetAttachDatabase](./jetattachdatabase-function.md) (進行完整備份) ，後面接著其相關聯的資料庫修補檔案 (如果支援) ，最後是備份程式期間產生的交易記錄檔。 最終結果將會是一組可從資料流程還原的檔案，可能會與現有的資料庫和記錄檔結合，最後會復原到一致的狀態。

完整備份的一般作業順序是由下列呼叫所組成。 首先，呼叫 **JetBeginExternalBackup** 以開始備份程式。 然後，呼叫 [JetGetAttachInfo](./jetgetattachinfo-function.md) 以取得附加至需要備份之實例的資料庫清單。 針對每個資料庫，會呼叫 [JetOpenFile](./jetopenfile-function.md) ，後面接著幾個 [JetReadFile](./jetreadfile-function.md) 呼叫，然後呼叫 [JetCloseFile](./jetclosefile-function.md)。 然後，呼叫 [JetGetLogInfo](./jetgetloginfo-function.md) 以取得要備份之資料庫修補和記錄檔的清單。 針對每個檔案，會進行另一個 [JetOpenFile](./jetopenfile-function.md)、 [JetReadFile](./jetreadfile-function.md)和 [JetCloseFile](./jetclosefile-function.md) 呼叫順序。 然後，會使用 [JetTruncateLog](./jettruncatelog-function.md)刪除任何不想要的交易記錄檔。 最後，會呼叫 [JetEndExternalBackup](./jetendexternalbackup-function.md)來結束備份。

您也可以修改這組步驟，以執行實例的增量備份。 增量備份會列舉和備份記錄檔。 只有在未啟用迴圈記錄的情況下，才可以進行增量備份。

您也可以修改這組步驟，以允許執行實例的後續差異備份。 若要執行差異備份，請勿在先前的完整或增量備份中呼叫 [JetTruncateLog](./jettruncatelog-function.md) 。 藉由不呼叫 [JetTruncateLog](./jettruncatelog-function.md)，您可以讓後續的備份與最後一個完整或增量備份有關。 只有在未啟用迴圈記錄的情況下，才可以進行差異備份。

資料庫修補檔是特殊的輔助檔案，用於在備份期間于特定情況下儲存資料庫頁面映射。 在還原作業期間，此檔案必須存在於與其相關聯資料庫相同的位置。 這個檔案只會用於 Windows 2000。 因此，任何針對 Windows 2000 和其他版本所撰寫的應用程式都必須支援資料庫修補檔案（如果存在的話），但如果不存在，也不能失敗。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JetEndExternalBackup](./jetendexternalbackup-function.md)  
[JetEndExternalBackupInstance2](./jetendexternalbackupinstance2-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)
