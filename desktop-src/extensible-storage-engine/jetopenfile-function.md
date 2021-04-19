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
ms.openlocfilehash: 2996ffc46e2f6b37cdfec12cd4ee2fc62efa188a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972369"
---
# <a name="jetopenfile-function"></a>JetOpenFile 函式


_**適用于：** Windows |Windows Server_

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
<td><p>作業失敗，因為目前的外部備份已被 <a href="gg294067(v=exchg.10).md">JetStopBackup</a>的呼叫中止。 只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileAccessDenied</p></td>
<td><p>作業失敗，因為它無法開啟要求的檔案，因為發生共用違規或許可權不足。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>作業失敗，因為它無法開啟要求的檔案，因為在指定的路徑中找不到該檔案。 此錯誤只會由 Windows 2000 傳回。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackupSequence</p></td>
<td><p>備份作業失敗，因為它的呼叫順序不是。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。 在下列情況下， <strong>JetOpenFile</strong> 可能會發生：</p>
<ul>
<li><p>指定的實例控制碼 (Windows XP 和更新版本) 無效。</p></li>
<li><p>指定的 filename 參數為 Null 或 (Windows XP 和更新版本) 的長度為零的字串。</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>因為找不到指定的路徑，所以操作失敗。</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingFileToBackup</p></td>
<td><p>無法開啟要求的檔案進行備份，因為找不到該檔案。 只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
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
<td><p>JET_errOutOfMemory</p></td>
<td><p>作業失敗，因為無法配置足夠的記憶體來完成。 如果嘗試在先前使用<strong>JetOpenFile</strong>開啟的檔案已由<a href="gg294127(v=exchg.10).md">JetCloseFile</a>關閉之前開啟另一個檔案， <strong>JetOpenFile</strong>會傳回 JET_errOutOfMemory。 目前只支援一個未處理的檔案控制代碼。</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>作業失敗，因為嘗試使用舊版模式中的引擎 (Windows 2000 相容性模式) 在事實中，如果有多個實例存在，則只支援一個實例。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在關閉。 JET_errRestoreInProgress 無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p></td>
</tr>
</tbody>
</table>


成功時，將會傳回所要求檔案的控制碼。 如果是資料庫檔案的控制碼，該資料庫檔案將會準備進行串流備份，這可能會導致在與資料庫檔案相同的位置中建立資料庫修補檔案。 資料庫修補檔案的路徑和檔案名與資料庫檔案完全相同，但具有。PAT 擴充功能。 也會傳回檔案的大小。

失敗時，輸出緩衝區的狀態將會是未定義的。 可能會在磁片上暫時建立資料庫修補檔案，而且可能會刪除修補檔案位置上的任何現有檔案。 失敗會導致整個實例的整個備份進程取消。 在 Windows XP 和更新版本中，如果在呼叫時嘗試備份未附加至實例的資料庫，將不會取消備份。

**警告**  基於安全性理由，請務必注意， **JetOpenFile** 不會驗證所要求的檔案路徑是否與應該針對該實例備份的檔案集合相關聯。 如此一來，您就可以使用此函式來存取任何可由目前線程的安全性內容開啟的檔案。 應用程式必須將傳遞給此函式的路徑限制為已知的良好檔案路徑集，否則可能會洩漏資訊攻擊。

#### <a name="remarks"></a>備註

必須要有控制碼和檔案大小輸出緩衝區。 如果不存在，引擎將會損毀，因為輸出緩衝區參數未經過驗證。

目前，每次只能開啟一個檔案進行備份。

**JetOpenFile** 不會在開啟要求的檔案之前判斷提示備份許可權。

此函式所報告之檔案的大小，可能不符合磁片上的檔案大小。 在 Windows XP 和更新版本中，額外的資訊可能會附加到資料庫檔案，資料庫引擎會在還原作業期間使用該檔案。 因此，應用程式應該只依賴 **JetOpenFile** 傳回的檔案大小，或 [JetReadFile](./jetreadfile-function.md)所傳回之資料的實際位元組數目。

#### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</p></td>
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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>實作為 <strong>JetOpenFileW</strong> (Unicode) 和 <strong>JetOpenFileA</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


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
