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
# <a name="jetreadfileinstance-function"></a><span data-ttu-id="ea111-103">JetReadFileInstance 函式</span><span class="sxs-lookup"><span data-stu-id="ea111-103">JetReadFileInstance Function</span></span>


<span data-ttu-id="ea111-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ea111-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetreadfileinstance-function"></a><span data-ttu-id="ea111-105">JetReadFileInstance 函式</span><span class="sxs-lookup"><span data-stu-id="ea111-105">JetReadFileInstance Function</span></span>

<span data-ttu-id="ea111-106">**JetReadFileInstance** 函式會抓取以 [JetOpenFileInstance](./jetopenfileinstance-function.md)函式開啟之檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="ea111-106">The **JetReadFileInstance** function retrieves the contents of a file opened with the [JetOpenFileInstance](./jetopenfileinstance-function.md) function.</span></span>

<span data-ttu-id="ea111-107">**Windows** xp：   **JetReadFileInstance** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="ea111-107">**Windows XP**:   **JetReadFileInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetReadFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcb
    );
```

### <a name="parameters"></a><span data-ttu-id="ea111-108">參數</span><span class="sxs-lookup"><span data-stu-id="ea111-108">Parameters</span></span>

<span data-ttu-id="ea111-109">*實例*</span><span class="sxs-lookup"><span data-stu-id="ea111-109">*instance*</span></span>

<span data-ttu-id="ea111-110">要用於特定 API 呼叫的實例。</span><span class="sxs-lookup"><span data-stu-id="ea111-110">The instance to use for a particular API call.</span></span>

<span data-ttu-id="ea111-111">請注意，對於 Windows 2000，無法使用接受此參數的 API 變體，因為只支援一個實例。</span><span class="sxs-lookup"><span data-stu-id="ea111-111">Note that for Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="ea111-112">在此情況下，這種全域實例的使用是隱含的。</span><span class="sxs-lookup"><span data-stu-id="ea111-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="ea111-113">若為 Windows XP 和更新版本，您可以呼叫 API 變數，此變數不會在引擎處於舊版模式時，才接受此參數 (Windows 2000 相容性模式) 在只支援一個實例的情況下。</span><span class="sxs-lookup"><span data-stu-id="ea111-113">For Windows XP and later releases, you can call the API variant that does not accept this parameter only when the engine is in legacy mode (Windows 2000 compatibility mode) in cases where only one instance is supported.</span></span> <span data-ttu-id="ea111-114">否則，作業將會失敗，並傳回 JET_errRunningInMultiInstanceMode 錯誤。</span><span class="sxs-lookup"><span data-stu-id="ea111-114">Otherwise, the operation will fail and return the JET_errRunningInMultiInstanceMode error.</span></span>

<span data-ttu-id="ea111-115">*hfFile*</span><span class="sxs-lookup"><span data-stu-id="ea111-115">*hfFile*</span></span>

<span data-ttu-id="ea111-116">要讀取之檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ea111-116">The handle of the file to be read.</span></span>

<span data-ttu-id="ea111-117">*光伏*</span><span class="sxs-lookup"><span data-stu-id="ea111-117">*pv*</span></span>

<span data-ttu-id="ea111-118">將接收檔案資料的輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ea111-118">The output buffer that will receive the file data.</span></span>

<span data-ttu-id="ea111-119">*Cb*</span><span class="sxs-lookup"><span data-stu-id="ea111-119">*cb*</span></span>

<span data-ttu-id="ea111-120">輸出緩衝區的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ea111-120">The maximum size, in bytes, of the output buffer.</span></span>

<span data-ttu-id="ea111-121">*Pcb*</span><span class="sxs-lookup"><span data-stu-id="ea111-121">*pcb*</span></span>

<span data-ttu-id="ea111-122">取出的實際檔資料量。</span><span class="sxs-lookup"><span data-stu-id="ea111-122">The actual amount of file data retrieved.</span></span>

### <a name="return-value"></a><span data-ttu-id="ea111-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="ea111-123">Return Value</span></span>

<span data-ttu-id="ea111-124">此函式可協助您傳回可延伸儲存引擎中所定義之任何 [JET_ERR](./jet-err.md) 資料類型， (ESE) API。</span><span class="sxs-lookup"><span data-stu-id="ea111-124">This function facilitates the return of any [JET_ERR](./jet-err.md) data types that are defined in the Extensible Storage Engine (ESE) API.</span></span> <span data-ttu-id="ea111-125">如需有關 JET 錯誤的詳細資訊，請參閱 [可擴充儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="ea111-125">For more information about JET errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ea111-126">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ea111-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="ea111-127">意義</span><span class="sxs-lookup"><span data-stu-id="ea111-127">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea111-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ea111-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ea111-129">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="ea111-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea111-130">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="ea111-130">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="ea111-131">作業失敗，因為目前的外部備份已被 <a href="gg269240(v=exchg.10).md">JetStopService</a> 函數的呼叫中止。</span><span class="sxs-lookup"><span data-stu-id="ea111-131">The operation failed because the current external backup has been aborted by a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span> <span data-ttu-id="ea111-132">只有 Windows XP 和更新版本的 Windows 會傳回這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="ea111-132">This error will be returned only by Windows XP and later Windows versions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea111-133">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="ea111-133">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="ea111-134">無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因為呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a> 函數。</span><span class="sxs-lookup"><span data-stu-id="ea111-134">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea111-135">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="ea111-135">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="ea111-136">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，要求撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="ea111-136">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error requiring that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="ea111-137">只有 Windows XP 和更新版本的 Windows 會傳回這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="ea111-137">This error will be returned only by Windows XP and later Windows versions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea111-138">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="ea111-138">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="ea111-139">其中一個指定的參數包含未預期的值，或與另一個參數的值結合時沒有意義的值。</span><span class="sxs-lookup"><span data-stu-id="ea111-139">One of the specified parameters contained either an unexpected value or a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="ea111-140">當發生下列任何情況時， <strong>JetReadFileInstance</strong> 函式可能會發生這種情況：</span><span class="sxs-lookup"><span data-stu-id="ea111-140">This can happen for the <strong>JetReadFileInstance</strong> function when any of the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="ea111-141">指定的實例控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="ea111-141">The specified instance handle is invalid.</span></span> <span data-ttu-id="ea111-142">Windows XP 及更新版本的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="ea111-142">Windows XP and later Windows versions.</span></span></p></li>
<li><p><span data-ttu-id="ea111-143">輸出緩衝區大小不是資料庫頁面大小的倍數 (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) 。</span><span class="sxs-lookup"><span data-stu-id="ea111-143">The output buffer size is not a multiple of the database page size (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>).</span></span> <span data-ttu-id="ea111-144">Windows XP 及更新版本的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="ea111-144">Windows XP and later Windows versions.</span></span></p></li>
<li><p><span data-ttu-id="ea111-145">輸出緩衝區大小小於三個資料庫頁面 (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) ，而這是指定之控制碼的第一次呼叫 <strong>JetReadFileInstance</strong> 函數。</span><span class="sxs-lookup"><span data-stu-id="ea111-145">The output buffer size is smaller than three database pages (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>), and this is the first call to the <strong>JetReadFileInstance</strong> function for the specified handle.</span></span> <span data-ttu-id="ea111-146">Windows XP 及更新版本的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="ea111-146">Windows XP and later Windows versions.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea111-147">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="ea111-147">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="ea111-148">作業失敗，因為讀取交易記錄檔時偵測到無法復原的資料損毀。</span><span class="sxs-lookup"><span data-stu-id="ea111-148">The operation failed because unrecoverable data corruption was detected while reading a transaction log file.</span></span> <span data-ttu-id="ea111-149">只有 Windows XP 和更新版本的 Windows 會傳回這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="ea111-149">This error will be returned only by Windows XP and later Windows versions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea111-150">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="ea111-150">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="ea111-151">作業失敗，因為沒有任何外部備份正在進行中。</span><span class="sxs-lookup"><span data-stu-id="ea111-151">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea111-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="ea111-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="ea111-153">無法完成作業，因為與此會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="ea111-153">It is not possible to complete the operation because the instance associated with this session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea111-154">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="ea111-154">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="ea111-155">作業失敗，因為從資料庫檔案或資料庫修補檔案讀取資料庫頁面時，偵測到無法復原的資料損毀。</span><span class="sxs-lookup"><span data-stu-id="ea111-155">The operation failed because unrecoverable data corruption was detected while reading a database page from a database file or database patch file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea111-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="ea111-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="ea111-157">無法完成作業，因為與此會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="ea111-157">It is not possible to complete the operation because a restore operation is in progress on the instance associated with this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea111-158">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="ea111-158">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="ea111-159">作業失敗，因為嘗試在舊版模式中使用引擎 (Windows 2000 相容性模式) 在只支援一個實例，但已有多個實例存在的情況下。</span><span class="sxs-lookup"><span data-stu-id="ea111-159">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) in a case where only one instance is supported but multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea111-160">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="ea111-160">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="ea111-161">無法完成作業，因為與此會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="ea111-161">It is not possible to complete the operation because the instance associated with this session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ea111-162">成功時，會將檔案中的下一個資料區塊讀入輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ea111-162">On success, the next chunk of data from the file will be read into the output buffer.</span></span> <span data-ttu-id="ea111-163">也會傳回實際抓取的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="ea111-163">The actual number of bytes retrieved will also be returned.</span></span> <span data-ttu-id="ea111-164">進行下一次讀取的檔案位移將會依此數量前進。</span><span class="sxs-lookup"><span data-stu-id="ea111-164">The file offset at which the next read will occur will be advanced by this amount.</span></span>

<span data-ttu-id="ea111-165">失敗時，輸出緩衝區的狀態是未定義的。</span><span class="sxs-lookup"><span data-stu-id="ea111-165">On failure, the state of the output buffer is undefined.</span></span> <span data-ttu-id="ea111-166">失敗會導致取消目前實例的整個備份進程。</span><span class="sxs-lookup"><span data-stu-id="ea111-166">The failure will result in the cancellation of the entire backup process for the current instance.</span></span> <span data-ttu-id="ea111-167">在 Windows XP 和更新版本的 Windows 版本中，如果在讀取資料庫檔案時發生錯誤，則不會取消備份。</span><span class="sxs-lookup"><span data-stu-id="ea111-167">In Windows XP and later Windows versions, the backup will not be canceled if an error occurred while reading a database file.</span></span> <span data-ttu-id="ea111-168">不過，仍會取消該資料庫檔案的備份，而且對應的控制碼將會自動關閉。</span><span class="sxs-lookup"><span data-stu-id="ea111-168">However, the backup of that database file will still be canceled and the corresponding handle will automatically be closed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ea111-169">備註</span><span class="sxs-lookup"><span data-stu-id="ea111-169">Remarks</span></span>

<span data-ttu-id="ea111-170">使用已傳回基礎檔案中所有資料的控制碼來進行 **JetReadFileInstance** 函式的任何呼叫 (例如，如果前一個呼叫傳回的位元組數目比輸出) 緩衝區的大小還少，則會傳回零位元組的資料。</span><span class="sxs-lookup"><span data-stu-id="ea111-170">Any call to the **JetReadFileInstance** function made by using a handle that has already returned all the data in the underlying file (such as if a previous call returned fewer bytes than the size of the output buffer) will always succeed but will return zero bytes of data.</span></span>

<span data-ttu-id="ea111-171">您應該使用大型的輸出緩衝區來最大化備份效能。</span><span class="sxs-lookup"><span data-stu-id="ea111-171">You should use a large output buffer to maximize backup performance.</span></span> <span data-ttu-id="ea111-172">在特定情況下，您可能需要實驗以找出資源耗用量與輸送量之間的最佳取捨。</span><span class="sxs-lookup"><span data-stu-id="ea111-172">You might need to experiment to find the optimal tradeoff between resource consumption and throughput for a particular situation.</span></span> <span data-ttu-id="ea111-173">在任何情況下，輸出緩衝區都不應小於 64 KB。</span><span class="sxs-lookup"><span data-stu-id="ea111-173">In any case, the output buffer should be no smaller than 64 KB.</span></span> <span data-ttu-id="ea111-174">您傳遞給 **JetReadFileInstance** 的指標必須對齊記憶體頁面界限 (4 kb 或 8 kb) 。</span><span class="sxs-lookup"><span data-stu-id="ea111-174">The pointer that you pass to **JetReadFileInstance** must be aligned with a memory page boundary (either 4 KB or 8 KB).</span></span> <span data-ttu-id="ea111-175">您可以藉由呼叫 **VirtualAlloc** 函式來完成這項作業。</span><span class="sxs-lookup"><span data-stu-id="ea111-175">You can do this by calling the **VirtualAlloc** function.</span></span>

<span data-ttu-id="ea111-176">不支援使用相同的檔案控制代碼對 **JetReadFileInstance** 進行多次並行呼叫。</span><span class="sxs-lookup"><span data-stu-id="ea111-176">Multiple concurrent calls to **JetReadFileInstance** made by using the same file handle are not supported.</span></span> <span data-ttu-id="ea111-177">這表示，您無法將數個緩衝區排入佇列，以針對相同檔案進行並行讀取，以達到高順序的輸送量。</span><span class="sxs-lookup"><span data-stu-id="ea111-177">This means that it is not possible to queue several buffers for concurrent reading against the same file to achieve high sequential throughput.</span></span> <span data-ttu-id="ea111-178">您應該改為使用單一大型緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ea111-178">You should use a single large buffer instead.</span></span>

<span data-ttu-id="ea111-179">如果您已設定特定的實例，以便啟用資料庫頁面清除 (請參閱 [系統參數](./extensible-storage-engine-system-parameters.md)) 中的 [JET_paramCircularLog](./transaction-log-parameters.md)參數，將會從資料庫中移除已刪除的資料，做為對資料庫檔案進行 **JetReadFileInstance** 呼叫的副作用。</span><span class="sxs-lookup"><span data-stu-id="ea111-179">If you have configured a particular instance such that database page scrubbing is enabled (see the [JET_paramCircularLog](./transaction-log-parameters.md) parameter in [System Parameters](./extensible-storage-engine-system-parameters.md)), deleted data will be removed from the database as a side-effect of a call to **JetReadFileInstance** against the database file.</span></span>

<span data-ttu-id="ea111-180">瞭解備份和資料損毀的互動方式非常重要。</span><span class="sxs-lookup"><span data-stu-id="ea111-180">It is very important to understand how backup and data corruption interact.</span></span> <span data-ttu-id="ea111-181">如果資料庫引擎在備份期間偵測到資料損毀，就會使受影響資料庫或整個實例的備份失敗。</span><span class="sxs-lookup"><span data-stu-id="ea111-181">If the database engine detects data corruption during a backup, it will fail the backup of either the affected database or the entire instance.</span></span> <span data-ttu-id="ea111-182">這是設計的設計決策，旨在防止資料遺失。</span><span class="sxs-lookup"><span data-stu-id="ea111-182">This is a conscious design decision intended to protect against data loss.</span></span> <span data-ttu-id="ea111-183">如果資料庫引擎允許在資料損毀的情況下成功備份，可能會捨棄較舊、未損毀的備份。</span><span class="sxs-lookup"><span data-stu-id="ea111-183">If the database engine allowed a backup to succeed where data corruption was present, it is possible that an older, uncorrupted backup could be discarded as a result.</span></span> <span data-ttu-id="ea111-184">這會很不幸，因為如此一來，就可以藉由還原該備份並重新執行該資料庫的所有交易記錄檔，來修正即時實例的資料損毀。</span><span class="sxs-lookup"><span data-stu-id="ea111-184">This would be unfortunate because then it would be possible to fix the data corruption on the live instance by restoring that backup and replaying all the transaction log files against that database.</span></span> <span data-ttu-id="ea111-185">這種零資料遺失案例會假設未啟用迴圈記錄 (請參閱[系統參數](./extensible-storage-engine-system-parameters.md)) 中的[JET_paramCircularLog](./transaction-log-parameters.md) 。</span><span class="sxs-lookup"><span data-stu-id="ea111-185">This zero-data-loss scenario presumes that circular logging is not enabled (see [JET_paramCircularLog](./transaction-log-parameters.md) in [System Parameters](./extensible-storage-engine-system-parameters.md)).</span></span>

<span data-ttu-id="ea111-186">也請務必瞭解，在串流備份期間，通常會先偵測到資料損毀的情況。</span><span class="sxs-lookup"><span data-stu-id="ea111-186">It is also important to understand that cases of data corruption are usually first detected during streaming backup.</span></span> <span data-ttu-id="ea111-187">這是因為串流備份是唯一會定期掃描資料庫檔案的每一頁的進程。</span><span class="sxs-lookup"><span data-stu-id="ea111-187">This is because streaming backup is the only process that routinely scans every single page of the database file.</span></span> <span data-ttu-id="ea111-188">串流備份也有可能是第一次偵測硬體失敗的早期徵兆的程式，因為這兩種方式都是由備份所取出的資料量，以及抓取資料的速度。</span><span class="sxs-lookup"><span data-stu-id="ea111-188">It is also likely that streaming backup will be the first process to detect the early signs of hardware failure as manifested by intermittent data corruption errors, because of both the amount of data retrieved by backup and the speed at which that data is retrieved.</span></span>

<span data-ttu-id="ea111-189">資料庫引擎會透過使用區塊總和檢查碼，來偵測資料損毀。</span><span class="sxs-lookup"><span data-stu-id="ea111-189">Data corruption is detected by the database engine through the use of block checksums.</span></span> <span data-ttu-id="ea111-190">這些總和檢查碼會在資料庫頁面寫入之前設定，並在讀取的資料庫頁面上進行驗證。</span><span class="sxs-lookup"><span data-stu-id="ea111-190">These checksums are set just before a database page write and are verified on a database page read.</span></span> <span data-ttu-id="ea111-191">此配置可讓資料庫引擎判斷資料已在某個時間點損毀，但不會讓資料庫引擎判斷該損毀的來源。</span><span class="sxs-lookup"><span data-stu-id="ea111-191">This scheme enables the database engine to determine that data has been corrupted at some point, but it does not enable the database engine to determine the source of that corruption.</span></span> <span data-ttu-id="ea111-192">在過去，這類資料損毀的實例源自資料庫引擎本身以外的來源。</span><span class="sxs-lookup"><span data-stu-id="ea111-192">Historically, instances of such data corruption have originated from sources other than the database engine itself.</span></span>

#### <a name="requirements"></a><span data-ttu-id="ea111-193">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea111-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea111-194">用戶端</span><span class="sxs-lookup"><span data-stu-id="ea111-194">Client</span></span></p></td>
<td><p><span data-ttu-id="ea111-195">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="ea111-195">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea111-196">伺服器</span><span class="sxs-lookup"><span data-stu-id="ea111-196">Server</span></span></p></td>
<td><p><span data-ttu-id="ea111-197">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="ea111-197">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea111-198">標頭</span><span class="sxs-lookup"><span data-stu-id="ea111-198">Header</span></span></p></td>
<td><p><span data-ttu-id="ea111-199">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="ea111-199">Is declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea111-200">程式庫</span><span class="sxs-lookup"><span data-stu-id="ea111-200">Library</span></span></p></td>
<td><p><span data-ttu-id="ea111-201">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="ea111-201">Uses ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea111-202">DLL</span><span class="sxs-lookup"><span data-stu-id="ea111-202">DLL</span></span></p></td>
<td><p><span data-ttu-id="ea111-203">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="ea111-203">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ea111-204">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ea111-204">See Also</span></span>

[<span data-ttu-id="ea111-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ea111-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ea111-206">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="ea111-206">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="ea111-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="ea111-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="ea111-208">JetOpenFileInstance</span><span class="sxs-lookup"><span data-stu-id="ea111-208">JetOpenFileInstance</span></span>](./jetopenfileinstance-function.md)  
[<span data-ttu-id="ea111-209">JetStopService</span><span class="sxs-lookup"><span data-stu-id="ea111-209">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="ea111-210">系統參數</span><span class="sxs-lookup"><span data-stu-id="ea111-210">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
