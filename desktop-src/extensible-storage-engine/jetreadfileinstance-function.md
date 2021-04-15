---
description: 深入瞭解： JetReadFileInstance 函數
title: JetReadFileInstance 函式
TOCTitle: JetReadFileInstance Function
ms:assetid: b17b4b43-86e5-4507-8a85-bbd5eac0aa3c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294060(v=EXCHG.10)
ms:contentKeyID: 32765675
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetReadFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9aad9828a92d67f2e7411aa534103696d913934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510915"
---
# <a name="jetreadfileinstance-function"></a>JetReadFileInstance 函式


_**適用于：** Windows |Windows Server_

## <a name="jetreadfileinstance-function"></a>JetReadFileInstance 函式

**JetReadFileInstance** 函式會抓取以 [JetOpenFileInstance](./jetopenfileinstance-function.md)函式開啟之檔案的內容。

**Windows** xp：   **JetReadFileInstance** 是在 windows xp 中引進的。

```cpp
    JET_ERR JET_API JetReadFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcb
    );
```

### <a name="parameters"></a>參數

*實例*

要用於特定 API 呼叫的實例。

請注意，對於 Windows 2000，無法使用接受此參數的 API 變體，因為只支援一個實例。 在此情況下，這種全域實例的使用是隱含的。

若為 Windows XP 和更新版本，您可以呼叫 API 變數，此變數不會在引擎處於舊版模式時，才接受此參數 (Windows 2000 相容性模式) 在只支援一個實例的情況下。 否則，作業將會失敗，並傳回 JET_errRunningInMultiInstanceMode 錯誤。

*hfFile*

要讀取之檔案的控制碼。

*光伏*

將接收檔案資料的輸出緩衝區。

*Cb*

輸出緩衝區的大小上限（以位元組為單位）。

*Pcb*

取出的實際檔資料量。

### <a name="return-value"></a>傳回值

此函式可協助您傳回可延伸儲存引擎中所定義之任何 [JET_ERR](./jet-err.md) 資料類型， (ESE) API。 如需有關 JET 錯誤的詳細資訊，請參閱 [可擴充儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>傳回碼</p></th>
<th><p>意義</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>作業已成功完成。</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupAbortByServer</p></td>
<td><p>作業失敗，因為目前的外部備份已被 <a href="gg269240(v=exchg.10).md">JetStopService</a> 函數的呼叫中止。 只有 Windows XP 和更新版本的 Windows 會傳回這個錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因為呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a> 函數。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，要求撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本的 Windows 會傳回這個錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>其中一個指定的參數包含未預期的值，或與另一個參數的值結合時沒有意義的值。 當發生下列任何情況時， <strong>JetReadFileInstance</strong> 函式可能會發生這種情況：</p>
<ul>
<li><p>指定的實例控制碼無效。 Windows XP 及更新版本的 Windows 版本。</p></li>
<li><p>輸出緩衝區大小不是資料庫頁面大小的倍數 (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) 。 Windows XP 及更新版本的 Windows 版本。</p></li>
<li><p>輸出緩衝區大小小於三個資料庫頁面 (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) ，而這是指定之控制碼的第一次呼叫 <strong>JetReadFileInstance</strong> 函數。 Windows XP 及更新版本的 Windows 版本。</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errLogReadVerifyFailure</p></td>
<td><p>作業失敗，因為讀取交易記錄檔時偵測到無法復原的資料損毀。 只有 Windows XP 和更新版本的 Windows 會傳回這個錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoBackup</p></td>
<td><p>作業失敗，因為沒有任何外部備份正在進行中。</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>無法完成作業，因為與此會話相關聯的實例尚未初始化。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errReadVerifyFailure</p></td>
<td><p>作業失敗，因為從資料庫檔案或資料庫修補檔案讀取資料庫頁面時，偵測到無法復原的資料損毀。</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>無法完成作業，因為與此會話相關聯的實例正在進行還原作業。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>作業失敗，因為嘗試在舊版模式中使用引擎 (Windows 2000 相容性模式) 在只支援一個實例，但已有多個實例存在的情況下。</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>無法完成作業，因為與此會話相關聯的實例正在關閉。</p></td>
</tr>
</tbody>
</table>


成功時，會將檔案中的下一個資料區塊讀入輸出緩衝區。 也會傳回實際抓取的位元組數目。 進行下一次讀取的檔案位移將會依此數量前進。

失敗時，輸出緩衝區的狀態是未定義的。 失敗會導致取消目前實例的整個備份進程。 在 Windows XP 和更新版本的 Windows 版本中，如果在讀取資料庫檔案時發生錯誤，則不會取消備份。 不過，仍會取消該資料庫檔案的備份，而且對應的控制碼將會自動關閉。

#### <a name="remarks"></a>備註

使用已傳回基礎檔案中所有資料的控制碼來進行 **JetReadFileInstance** 函式的任何呼叫 (例如，如果前一個呼叫傳回的位元組數目比輸出) 緩衝區的大小還少，則會傳回零位元組的資料。

您應該使用大型的輸出緩衝區來最大化備份效能。 在特定情況下，您可能需要實驗以找出資源耗用量與輸送量之間的最佳取捨。 在任何情況下，輸出緩衝區都不應小於 64 KB。 您傳遞給 **JetReadFileInstance** 的指標必須對齊記憶體頁面界限 (4 kb 或 8 kb) 。 您可以藉由呼叫 **VirtualAlloc** 函式來完成這項作業。

不支援使用相同的檔案控制代碼對 **JetReadFileInstance** 進行多次並行呼叫。 這表示，您無法將數個緩衝區排入佇列，以針對相同檔案進行並行讀取，以達到高順序的輸送量。 您應該改為使用單一大型緩衝區。

如果您已設定特定的實例，以便啟用資料庫頁面清除 (請參閱 [系統參數](./extensible-storage-engine-system-parameters.md)) 中的 [JET_paramCircularLog](./transaction-log-parameters.md)參數，將會從資料庫中移除已刪除的資料，做為對資料庫檔案進行 **JetReadFileInstance** 呼叫的副作用。

瞭解備份和資料損毀的互動方式非常重要。 如果資料庫引擎在備份期間偵測到資料損毀，就會使受影響資料庫或整個實例的備份失敗。 這是設計的設計決策，旨在防止資料遺失。 如果資料庫引擎允許在資料損毀的情況下成功備份，可能會捨棄較舊、未損毀的備份。 這會很不幸，因為如此一來，就可以藉由還原該備份並重新執行該資料庫的所有交易記錄檔，來修正即時實例的資料損毀。 這種零資料遺失案例會假設未啟用迴圈記錄 (請參閱[系統參數](./extensible-storage-engine-system-parameters.md)) 中的[JET_paramCircularLog](./transaction-log-parameters.md) 。

也請務必瞭解，在串流備份期間，通常會先偵測到資料損毀的情況。 這是因為串流備份是唯一會定期掃描資料庫檔案的每一頁的進程。 串流備份也有可能是第一次偵測硬體失敗的早期徵兆的程式，因為這兩種方式都是由備份所取出的資料量，以及抓取資料的速度。

資料庫引擎會透過使用區塊總和檢查碼，來偵測資料損毀。 這些總和檢查碼會在資料庫頁面寫入之前設定，並在讀取的資料庫頁面上進行驗證。 此配置可讓資料庫引擎判斷資料已在某個時間點損毀，但不會讓資料庫引擎判斷該損毀的來源。 在過去，這類資料損毀的實例源自資料庫引擎本身以外的來源。

#### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>用戶端</p></td>
<td><p>需要 Windows Vista 或 Windows XP。</p></td>
</tr>
<tr class="even">
<td><p>伺服器</p></td>
<td><p>需要 Windows Server 2008 或 Windows Server 2003。</p></td>
</tr>
<tr class="odd">
<td><p>標頭</p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
<tr class="even">
<td><p>程式庫</p></td>
<td><p>使用 ESENT。</p></td>
</tr>
<tr class="odd">
<td><p>DLL</p></td>
<td><p>需要 ESENT.dll。</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFileInstance](./jetopenfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)  
[系統參數](./extensible-storage-engine-system-parameters.md)
