---
description: 深入瞭解： JetOpenFile 函數
title: JetOpenFile 函式
TOCTitle: JetOpenFile Function
ms:assetid: 52f69050-ca1c-4a6b-a188-22bd7cb96bf5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269249(v=EXCHG.10)
ms:contentKeyID: 32765551
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenFileW
- JetOpenFile
- JetOpenFileA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ffe4527390e21e86ed46820125eb2a422367d8ec
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480374"
---
# <a name="jetopenfile-function"></a>JetOpenFile 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetopenfile-function"></a>JetOpenFile 函式

**JetOpenFile** 函式會開啟連接的資料庫、資料庫修補檔或作用中實例的交易記錄檔，以執行串流模糊備份。 之後可以使用 [JetReadFile](./jetreadfile-function.md)，透過傳回的控制碼讀取這些檔案中的資料。 傳回的控制碼必須使用 [JetCloseFile](./jetclosefile-function.md)來關閉。 實例的外部備份必須先前已使用 [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)起始。

```cpp
    JET_ERR JET_API JetOpenFile(
      __in          const tchar* szFileName,
      __out         JET_HANDLE* phfFile,
      __out         unsigned long* pulFileSizeLow,
      __out         unsigned long* pulFileSizeHigh
    );
```

### <a name="parameters"></a>參數

*szFileName*

附加的資料庫、資料庫修補檔或由將讀取以進行備份之實例管理的交易記錄檔的相對或絕對路徑。

*phfFile*

輸出緩衝區，接收要讀取之檔案的控制碼。

*pulFileSizeLow*

輸出緩衝區，此緩衝區會接收最不重要的檔案大小32位。

*pulFileSizeHigh*

輸出緩衝區，可接收檔案大小最大的32位。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>作業失敗，因為目前的外部備份已被 <a href="gg294067(v=exchg.10).md">JetStopBackup</a>的呼叫中止。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errFileAccessDenied</p> | <p>作業失敗，因為它無法開啟要求的檔案，因為發生共用違規或許可權不足。</p> | 
| <p>JET_errFileNotFound</p> | <p>作業失敗，因為它無法開啟要求的檔案，因為在指定的路徑中找不到該檔案。 只有 Windows 2000 才會傳回此錯誤。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>備份作業失敗，因為它的呼叫順序不是。</p> | 
| <p>JET_errInvalidParameter</p> | <p>提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。 在下列情況下， <strong>JetOpenFile</strong> 可能會發生：</p><ul><li><p>指定的實例控制碼無效 (Windows XP 和更新版本) 。</p></li><li><p>指定的 filename 參數為 Null 或長度為零的字串 (Windows XP 和更新版本) 。</p></li></ul> | 
| <p>JET_errInvalidPath</p> | <p>因為找不到指定的路徑，所以操作失敗。</p> | 
| <p>JET_errMissingFileToBackup</p> | <p>無法開啟要求的檔案進行備份，因為找不到該檔案。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errNoBackup</p> | <p>作業失敗，因為沒有任何外部備份正在進行中。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errOutOfMemory</p> | <p>作業失敗，因為無法配置足夠的記憶體來完成。 如果嘗試在先前使用<strong>JetOpenFile</strong>開啟的檔案已由<a href="gg294127(v=exchg.10).md">JetCloseFile</a>關閉之前開啟另一個檔案， <strong>JetOpenFile</strong>會傳回 JET_errOutOfMemory。 目前只支援一個未處理的檔案控制代碼。</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>作業失敗，因為嘗試使用舊版模式中的引擎 (Windows 2000 相容性模式) 只有當有多個實例存在時，才支援一個實例。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。 JET_errRestoreInProgress 無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 



成功時，將會傳回所要求檔案的控制碼。 如果是資料庫檔案的控制碼，該資料庫檔案將會準備進行串流備份，這可能會導致在與資料庫檔案相同的位置中建立資料庫修補檔案。 資料庫修補檔案的路徑和檔案名與資料庫檔案完全相同，但具有。PAT 擴充功能。 也會傳回檔案的大小。

失敗時，輸出緩衝區的狀態將會是未定義的。 可能會在磁片上暫時建立資料庫修補檔案，而且可能會刪除修補檔案位置上的任何現有檔案。 失敗會導致整個實例的整個備份進程取消。 在 Windows XP 和更新版本中，如果在呼叫時嘗試備份未附加至實例的資料庫，將不會取消備份。

**警告**  基於安全性理由，請務必注意， **JetOpenFile** 不會驗證所要求的檔案路徑是否與應該針對該實例備份的檔案集合相關聯。 如此一來，您就可以使用此函式來存取任何可由目前線程的安全性內容開啟的檔案。 應用程式必須將傳遞給此函式的路徑限制為已知的良好檔案路徑集，否則可能會洩漏資訊攻擊。

#### <a name="remarks"></a>備註

必須要有控制碼和檔案大小輸出緩衝區。 如果不存在，引擎將會損毀，因為輸出緩衝區參數未經過驗證。

目前，每次只能開啟一個檔案進行備份。

**JetOpenFile** 不會在開啟要求的檔案之前判斷提示備份許可權。

此函式所報告之檔案的大小，可能不符合磁片上的檔案大小。 在 Windows XP 和更新版本中，額外的資訊可能會附加到資料庫檔案，在還原作業期間，資料庫引擎會使用此檔案。 因此，應用程式應該只依賴 **JetOpenFile** 傳回的檔案大小，或 [JetReadFile](./jetreadfile-function.md)所傳回之資料的實際位元組數目。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | | <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetOpenFileW</strong> (Unicode) 和 <strong>JetOpenFileA</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)
