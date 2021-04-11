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
# <a name="jetreadfile-function"></a><span data-ttu-id="e48bd-103">JetReadFile 函式</span><span class="sxs-lookup"><span data-stu-id="e48bd-103">JetReadFile Function</span></span>


<span data-ttu-id="e48bd-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e48bd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetreadfile-function"></a><span data-ttu-id="e48bd-105">JetReadFile 函式</span><span class="sxs-lookup"><span data-stu-id="e48bd-105">JetReadFile Function</span></span>

<span data-ttu-id="e48bd-106">**JetReadFile** 函式會抓取以 [JetOpenFile](./jetopenfile-function.md)開啟的檔案內容。</span><span class="sxs-lookup"><span data-stu-id="e48bd-106">The **JetReadFile** function retrieves the contents of a file opened with [JetOpenFile](./jetopenfile-function.md).</span></span>

```cpp
    JET_ERR JET_API JetReadFile(
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="e48bd-107">參數</span><span class="sxs-lookup"><span data-stu-id="e48bd-107">Parameters</span></span>

<span data-ttu-id="e48bd-108">*hfFile*</span><span class="sxs-lookup"><span data-stu-id="e48bd-108">*hfFile*</span></span>

<span data-ttu-id="e48bd-109">要讀取之檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e48bd-109">The handle of the file to be read.</span></span>

<span data-ttu-id="e48bd-110">*光伏*</span><span class="sxs-lookup"><span data-stu-id="e48bd-110">*pv*</span></span>

<span data-ttu-id="e48bd-111">將接收檔案資料的輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e48bd-111">Output buffer that will receive the file data.</span></span>

<span data-ttu-id="e48bd-112">*Cb*</span><span class="sxs-lookup"><span data-stu-id="e48bd-112">*cb*</span></span>

<span data-ttu-id="e48bd-113">輸出緩衝區的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e48bd-113">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="e48bd-114">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="e48bd-114">*pcbActual*</span></span>

<span data-ttu-id="e48bd-115">接收實際取出的檔案資料量。</span><span class="sxs-lookup"><span data-stu-id="e48bd-115">Receives the actual amount of file data retrieved.</span></span>

### <a name="return-value"></a><span data-ttu-id="e48bd-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="e48bd-116">Return Value</span></span>

<span data-ttu-id="e48bd-117">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="e48bd-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e48bd-118">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="e48bd-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e48bd-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e48bd-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="e48bd-120">Description</span><span class="sxs-lookup"><span data-stu-id="e48bd-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e48bd-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e48bd-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e48bd-122">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="e48bd-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e48bd-123">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="e48bd-123">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="e48bd-124">作業失敗，因為目前的外部備份已被 <a href="gg269240(v=exchg.10).md">JetStopService</a>的呼叫中止。</span><span class="sxs-lookup"><span data-stu-id="e48bd-124">The operation failed because the current external backup has been aborted by a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span> <span data-ttu-id="e48bd-125">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="e48bd-125">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e48bd-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="e48bd-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="e48bd-127">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="e48bd-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e48bd-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="e48bd-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="e48bd-129">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="e48bd-129">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="e48bd-130">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="e48bd-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e48bd-131">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="e48bd-131">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="e48bd-132">提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="e48bd-132">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="e48bd-133">在下列情況下， <strong>JetReadFile</strong> 可能會發生：</span><span class="sxs-lookup"><span data-stu-id="e48bd-133">This can happen for <strong>JetReadFile</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="e48bd-134">指定的實例控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="e48bd-134">The specified instance handle is invalid.</span></span> <span data-ttu-id="e48bd-135">Windows XP 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="e48bd-135">Windows XP and later releases.</span></span></p></li>
<li><p><span data-ttu-id="e48bd-136">輸出緩衝區大小不是資料庫頁面大小的倍數 (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) 。</span><span class="sxs-lookup"><span data-stu-id="e48bd-136">The output buffer size is not a multiple of the database page size (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>).</span></span> <span data-ttu-id="e48bd-137">Windows XP 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="e48bd-137">Windows XP and later releases.</span></span></p></li>
<li><p><span data-ttu-id="e48bd-138">輸出緩衝區大小小於三個資料庫頁面 (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) ，而這是指定控制碼的第一個 <strong>JetReadFile</strong> 呼叫。</span><span class="sxs-lookup"><span data-stu-id="e48bd-138">The output buffer size is smaller than three database pages (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) and this is the first call to <strong>JetReadFile</strong> for the specified handle.</span></span> <span data-ttu-id="e48bd-139">Windows XP 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="e48bd-139">Windows XP and later releases.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e48bd-140">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="e48bd-140">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="e48bd-141">作業失敗，因為沒有任何外部備份正在進行中。</span><span class="sxs-lookup"><span data-stu-id="e48bd-141">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e48bd-142">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="e48bd-142">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="e48bd-143">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="e48bd-143">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e48bd-144">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="e48bd-144">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="e48bd-145">作業失敗，因為從資料庫檔案或資料庫修補檔案讀取資料庫頁面時，偵測到無法復原的資料損毀。</span><span class="sxs-lookup"><span data-stu-id="e48bd-145">The operation failed because non-recoverable data corruption was detected while reading a database page from a database file or database patch file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e48bd-146">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="e48bd-146">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="e48bd-147">作業失敗，因為讀取交易記錄檔時偵測到無法復原的資料損毀。</span><span class="sxs-lookup"><span data-stu-id="e48bd-147">The operation failed because non-recoverable data corruption was detected while reading a transaction log file.</span></span> <span data-ttu-id="e48bd-148">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="e48bd-148">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e48bd-149">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="e48bd-149">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="e48bd-150">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="e48bd-150">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e48bd-151">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="e48bd-151">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="e48bd-152">作業失敗，因為嘗試使用舊版模式中的引擎 (Windows 2000 相容性模式) 在事實中，如果有多個實例存在，則只支援一個實例。</span><span class="sxs-lookup"><span data-stu-id="e48bd-152">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e48bd-153">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="e48bd-153">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="e48bd-154">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="e48bd-154">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e48bd-155">成功時，會將檔案中的下一個資料區塊讀入輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e48bd-155">On success, the next chunk of data from the file will be read into the output buffer.</span></span> <span data-ttu-id="e48bd-156">也會傳回實際抓取的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="e48bd-156">The actual number of bytes retrieved will also be returned.</span></span> <span data-ttu-id="e48bd-157">進行下一次讀取的檔案位移將會依此數量前進。</span><span class="sxs-lookup"><span data-stu-id="e48bd-157">The file offset at which the next read will occur will be advanced by this amount.</span></span>

<span data-ttu-id="e48bd-158">失敗時，輸出緩衝區的狀態是未定義的。</span><span class="sxs-lookup"><span data-stu-id="e48bd-158">On failure, the state of the output buffer is undefined.</span></span> <span data-ttu-id="e48bd-159">失敗會導致整個實例的整個備份進程取消。</span><span class="sxs-lookup"><span data-stu-id="e48bd-159">The failure will result in the cancellation of the entire backup process for the instance.</span></span> <span data-ttu-id="e48bd-160">在 Windows XP 和更新版本中，如果在讀取資料庫檔案時發生錯誤，將不會取消備份。</span><span class="sxs-lookup"><span data-stu-id="e48bd-160">On Windows XP and later releases, the backup will not be canceled if an error occurred while reading a database file.</span></span> <span data-ttu-id="e48bd-161">不過，仍會取消該資料庫檔案的備份，而且對應的控制碼將會自動關閉。</span><span class="sxs-lookup"><span data-stu-id="e48bd-161">However, the backup of that database file will still be canceled and the corresponding handle will automatically be closed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="e48bd-162">備註</span><span class="sxs-lookup"><span data-stu-id="e48bd-162">Remarks</span></span>

<span data-ttu-id="e48bd-163">使用已在基礎 (檔中傳回所有資料的控制碼進行的任何呼叫 **JetReadFile** ，例如先前的呼叫所傳回的位元組數，會比輸出) 緩衝區的大小還少，但會傳回零位元組的資料。</span><span class="sxs-lookup"><span data-stu-id="e48bd-163">Any call to **JetReadFile** using a handle that has already returned all the data in the underlying file (such as a previous call returned less bytes than the size of the output buffer) will always succeed but return zero bytes of data.</span></span>

<span data-ttu-id="e48bd-164">應該使用大型的輸出緩衝區來將備份效能最大化。</span><span class="sxs-lookup"><span data-stu-id="e48bd-164">A large output buffer should be used to maximize backup performance.</span></span> <span data-ttu-id="e48bd-165">在特定情況下，可能需要進行一些實驗，才能找出資源耗用量與輸送量之間的正確取捨。</span><span class="sxs-lookup"><span data-stu-id="e48bd-165">Some experimentation may be required to find the right tradeoff between resource consumption and throughput for a given situation.</span></span> <span data-ttu-id="e48bd-166">在任何情況下，輸出緩衝區都不應小於64KB。</span><span class="sxs-lookup"><span data-stu-id="e48bd-166">The output buffer should be no smaller than 64KB in any case.</span></span>

<span data-ttu-id="e48bd-167">不支援多個使用相同檔案控制代碼對 **JetReadFile** 的並行呼叫。</span><span class="sxs-lookup"><span data-stu-id="e48bd-167">Multiple concurrent calls to **JetReadFile** using the same file handle are not supported.</span></span> <span data-ttu-id="e48bd-168">這表示，您不可能將數個緩衝區排入佇列，以針對相同的檔案進行並行讀取，以達到高順序的輸送量。</span><span class="sxs-lookup"><span data-stu-id="e48bd-168">This means that it is not possible to queue several buffers for read concurrently against the same file to achieve high sequential throughput.</span></span> <span data-ttu-id="e48bd-169">應該改為使用單一大型緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e48bd-169">A single large buffer should be used instead.</span></span>

<span data-ttu-id="e48bd-170">如果實例已設定為已啟用資料庫頁面清除 (請參閱系統參數中的 JET_paramZeroDatabaseDuringBackup) 然後，會從資料庫中移除已刪除的資料，作為對資料庫檔案進行 **JetReadFile** 呼叫的副作用。</span><span class="sxs-lookup"><span data-stu-id="e48bd-170">If the instance is configured such that database page scrubbing is enabled (see JET_paramZeroDatabaseDuringBackup in System Parameters) then deleted data will be removed from the database as a side effect of a call to **JetReadFile** against the database file.</span></span>

<span data-ttu-id="e48bd-171">瞭解備份和資料損毀的互動方式非常重要。</span><span class="sxs-lookup"><span data-stu-id="e48bd-171">It is very important to understand how backup and data corruption interact.</span></span> <span data-ttu-id="e48bd-172">如果資料庫引擎在備份期間偵測到資料損毀，就會使受影響資料庫或整個實例的備份失敗。</span><span class="sxs-lookup"><span data-stu-id="e48bd-172">If the database engine detects data corruption during a backup then it will either fail the backup of the affected database or of the entire instance.</span></span> <span data-ttu-id="e48bd-173">這是設計的設計決策，旨在防止資料遺失。</span><span class="sxs-lookup"><span data-stu-id="e48bd-173">This is a conscious design decision intended to protect against data loss.</span></span> <span data-ttu-id="e48bd-174">如果資料庫引擎允許備份在出現資料損毀的情況下成功，則可能會捨棄較舊、未損毀的備份。</span><span class="sxs-lookup"><span data-stu-id="e48bd-174">If the database engine allowed a backup to succeed where data corruption was present then it is possible that an older, uncorrupted backup could be discarded as a result.</span></span> <span data-ttu-id="e48bd-175">這會很不幸，因為可以藉由還原該備份並重新執行該資料庫的所有交易記錄檔，來修正即時實例的資料損毀。</span><span class="sxs-lookup"><span data-stu-id="e48bd-175">This would be unfortunate because it would be possible to fix the data corruption on the live instance by restoring that backup and replaying all the transaction log files against that database.</span></span> <span data-ttu-id="e48bd-176">這零的資料遺失案例會假設未啟用迴圈記錄 (請參閱[系統參數](./extensible-storage-engine-system-parameters.md)) 中的[JET_paramCircularLog](./transaction-log-parameters.md) 。</span><span class="sxs-lookup"><span data-stu-id="e48bd-176">This zero data loss scenario presumes that circular logging is not enabled (see [JET_paramCircularLog](./transaction-log-parameters.md) in [System Parameters](./extensible-storage-engine-system-parameters.md)).</span></span>

<span data-ttu-id="e48bd-177">也請務必瞭解，當資料損毀時，資料流程備份將會是最可能最先被偵測到的位置。</span><span class="sxs-lookup"><span data-stu-id="e48bd-177">It is also important to understand that when data corruption is present streaming backup will be the most likely place that it will first be detected.</span></span> <span data-ttu-id="e48bd-178">這是因為串流備份是唯一會定期掃描資料庫檔案的每一頁的進程。</span><span class="sxs-lookup"><span data-stu-id="e48bd-178">This is the case because streaming backup is the only process that routinely scans every single page of the database file.</span></span> <span data-ttu-id="e48bd-179">串流備份也有可能是第一次偵測硬體失敗的早期徵兆，因為間歇的資料損毀錯誤。</span><span class="sxs-lookup"><span data-stu-id="e48bd-179">It is also likely that streaming backup will be the first process to detect the early signs of hardware failure as manifested by intermittent data corruption errors.</span></span> <span data-ttu-id="e48bd-180">這是因為備份所取出的資料量，以及抓取的速度。</span><span class="sxs-lookup"><span data-stu-id="e48bd-180">This is due to the amount of data retrieved by backup as well as the speed at which it is retrieved.</span></span>

<span data-ttu-id="e48bd-181">資料庫引擎會透過使用區塊總和檢查碼，來偵測資料損毀。</span><span class="sxs-lookup"><span data-stu-id="e48bd-181">Data corruption is detected by the database engine through the use of block checksums.</span></span> <span data-ttu-id="e48bd-182">這些總和檢查碼會在資料庫頁面寫入之前設定，並在讀取的資料庫頁面上進行驗證。</span><span class="sxs-lookup"><span data-stu-id="e48bd-182">These checksums are set just prior to a database page write and are verified on a database page read.</span></span> <span data-ttu-id="e48bd-183">此配置可讓資料庫引擎判斷資料已在某個時間點損毀，但無法讓資料庫引擎判斷該損毀的來源。</span><span class="sxs-lookup"><span data-stu-id="e48bd-183">This scheme enables the database engine to determine that data has been corrupted at some point but it does not enable the database engine to determine the source of that corruption.</span></span> <span data-ttu-id="e48bd-184">在過去，發現這類損毀的主要原因是來自資料庫引擎本身以外的來源。</span><span class="sxs-lookup"><span data-stu-id="e48bd-184">Historically, the predominant cause of such corruption has been found to come from sources other than the database engine itself.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e48bd-185">規格需求</span><span class="sxs-lookup"><span data-stu-id="e48bd-185">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e48bd-186"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="e48bd-186"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e48bd-187">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="e48bd-187">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e48bd-188"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="e48bd-188"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e48bd-189">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="e48bd-189">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e48bd-190"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="e48bd-190"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e48bd-191">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="e48bd-191">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e48bd-192"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="e48bd-192"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e48bd-193">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="e48bd-193">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e48bd-194"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e48bd-194"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e48bd-195">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="e48bd-195">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e48bd-196">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e48bd-196">See Also</span></span>

[<span data-ttu-id="e48bd-197">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e48bd-197">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e48bd-198">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="e48bd-198">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="e48bd-199">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="e48bd-199">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="e48bd-200">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="e48bd-200">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="e48bd-201">JetStopService</span><span class="sxs-lookup"><span data-stu-id="e48bd-201">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="e48bd-202">系統參數</span><span class="sxs-lookup"><span data-stu-id="e48bd-202">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
