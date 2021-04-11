---
description: 深入瞭解： JetReadFile 函數
title: JetReadFile 函式
TOCTitle: JetReadFile Function
ms:assetid: 59dc9e04-7e02-4835-9aed-95cfcf74d780
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269257(v=EXCHG.10)
ms:contentKeyID: 32765559
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetReadFile
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 57e11f3b5478f18bc7883974c2f598bf24dcb8fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193795"
---
# <a name="jetreadfile-function"></a>JetReadFile 函式


_**適用于：** Windows |Windows Server_

## <a name="jetreadfile-function"></a>JetReadFile 函式

**JetReadFile** 函式會抓取以 [JetOpenFile](./jetopenfile-function.md)開啟的檔案內容。

```cpp
    JET_ERR JET_API JetReadFile(
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>參數

*hfFile*

要讀取之檔案的控制碼。

*光伏*

將接收檔案資料的輸出緩衝區。

*Cb*

輸出緩衝區的大小上限（以位元組為單位）。

*pcbActual*

接收實際取出的檔案資料量。

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
<td><p>作業失敗，因為目前的外部備份已被 <a href="gg269240(v=exchg.10).md">JetStopService</a>的呼叫中止。 只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。 在下列情況下， <strong>JetReadFile</strong> 可能會發生：</p>
<ul>
<li><p>指定的實例控制碼無效。 Windows XP 和更新版本。</p></li>
<li><p>輸出緩衝區大小不是資料庫頁面大小的倍數 (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) 。 Windows XP 和更新版本。</p></li>
<li><p>輸出緩衝區大小小於三個資料庫頁面 (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) ，而這是指定控制碼的第一個 <strong>JetReadFile</strong> 呼叫。 Windows XP 和更新版本。</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackup</p></td>
<td><p>作業失敗，因為沒有任何外部備份正在進行中。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p></td>
</tr>
<tr class="even">
<td><p>JET_errReadVerifyFailure</p></td>
<td><p>作業失敗，因為從資料庫檔案或資料庫修補檔案讀取資料庫頁面時，偵測到無法復原的資料損毀。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogReadVerifyFailure</p></td>
<td><p>作業失敗，因為讀取交易記錄檔時偵測到無法復原的資料損毀。 只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>作業失敗，因為嘗試使用舊版模式中的引擎 (Windows 2000 相容性模式) 在事實中，如果有多個實例存在，則只支援一個實例。</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在關閉。</p></td>
</tr>
</tbody>
</table>


成功時，會將檔案中的下一個資料區塊讀入輸出緩衝區。 也會傳回實際抓取的位元組數目。 進行下一次讀取的檔案位移將會依此數量前進。

失敗時，輸出緩衝區的狀態是未定義的。 失敗會導致整個實例的整個備份進程取消。 在 Windows XP 和更新版本中，如果在讀取資料庫檔案時發生錯誤，將不會取消備份。 不過，仍會取消該資料庫檔案的備份，而且對應的控制碼將會自動關閉。

#### <a name="remarks"></a>備註

使用已在基礎 (檔中傳回所有資料的控制碼進行的任何呼叫 **JetReadFile** ，例如先前的呼叫所傳回的位元組數，會比輸出) 緩衝區的大小還少，但會傳回零位元組的資料。

應該使用大型的輸出緩衝區來將備份效能最大化。 在特定情況下，可能需要進行一些實驗，才能找出資源耗用量與輸送量之間的正確取捨。 在任何情況下，輸出緩衝區都不應小於64KB。

不支援多個使用相同檔案控制代碼對 **JetReadFile** 的並行呼叫。 這表示，您不可能將數個緩衝區排入佇列，以針對相同的檔案進行並行讀取，以達到高順序的輸送量。 應該改為使用單一大型緩衝區。

如果實例已設定為已啟用資料庫頁面清除 (請參閱系統參數中的 JET_paramZeroDatabaseDuringBackup) 然後，會從資料庫中移除已刪除的資料，作為對資料庫檔案進行 **JetReadFile** 呼叫的副作用。

瞭解備份和資料損毀的互動方式非常重要。 如果資料庫引擎在備份期間偵測到資料損毀，就會使受影響資料庫或整個實例的備份失敗。 這是設計的設計決策，旨在防止資料遺失。 如果資料庫引擎允許備份在出現資料損毀的情況下成功，則可能會捨棄較舊、未損毀的備份。 這會很不幸，因為可以藉由還原該備份並重新執行該資料庫的所有交易記錄檔，來修正即時實例的資料損毀。 這零的資料遺失案例會假設未啟用迴圈記錄 (請參閱[系統參數](./extensible-storage-engine-system-parameters.md)) 中的[JET_paramCircularLog](./transaction-log-parameters.md) 。

也請務必瞭解，當資料損毀時，資料流程備份將會是最可能最先被偵測到的位置。 這是因為串流備份是唯一會定期掃描資料庫檔案的每一頁的進程。 串流備份也有可能是第一次偵測硬體失敗的早期徵兆，因為間歇的資料損毀錯誤。 這是因為備份所取出的資料量，以及抓取的速度。

資料庫引擎會透過使用區塊總和檢查碼，來偵測資料損毀。 這些總和檢查碼會在資料庫頁面寫入之前設定，並在讀取的資料庫頁面上進行驗證。 此配置可讓資料庫引擎判斷資料已在某個時間點損毀，但無法讓資料庫引擎判斷該損毀的來源。 在過去，發現這類損毀的主要原因是來自資料庫引擎本身以外的來源。

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
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetStopService](./jetstopservice-function.md)  
[系統參數](./extensible-storage-engine-system-parameters.md)
