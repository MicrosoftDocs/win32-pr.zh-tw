---
description: 深入瞭解： JetRestoreInstance 函數
title: JetRestoreInstance 函式
TOCTitle: JetRestoreInstance Function
ms:assetid: 7ba2b6ee-96f5-44c5-9842-5e58580f60f1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269306(v=EXCHG.10)
ms:contentKeyID: 32765597
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestoreInstanceW
- JetRestoreInstance
- JetRestoreInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bb7af096a63880a88496631999ddbc26a975cac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194874"
---
# <a name="jetrestoreinstance-function"></a><span data-ttu-id="4a1c9-103">JetRestoreInstance 函式</span><span class="sxs-lookup"><span data-stu-id="4a1c9-103">JetRestoreInstance Function</span></span>


<span data-ttu-id="4a1c9-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4a1c9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrestoreinstance-function"></a><span data-ttu-id="4a1c9-105">JetRestoreInstance 函式</span><span class="sxs-lookup"><span data-stu-id="4a1c9-105">JetRestoreInstance Function</span></span>

<span data-ttu-id="4a1c9-106">**JetRestoreInstance** 函式會還原和復原實例的串流備份，包括所有附加的資料庫。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-106">The **JetRestoreInstance** function restores and recovers a streaming backup of an instance including all the attached databases.</span></span> <span data-ttu-id="4a1c9-107">它是設計來搭配使用 [JetBackupInstance](./jetbackupinstance-function.md) 函式所建立的備份。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-107">It is designed to work with a backup created with the [JetBackupInstance](./jetbackupinstance-function.md) function.</span></span> <span data-ttu-id="4a1c9-108">這是最簡單且最封裝的還原功能。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-108">This is the simplest and most encapsulated one restore function.</span></span>

<span data-ttu-id="4a1c9-109">**Windows xp：**  **JetRestoreInstance** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-109">**Windows XP:**  **JetRestoreInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetRestoreInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR sz,
      __in_opt      JET_PCSTR szDest,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a><span data-ttu-id="4a1c9-110">參數</span><span class="sxs-lookup"><span data-stu-id="4a1c9-110">Parameters</span></span>

<span data-ttu-id="4a1c9-111">*實例*</span><span class="sxs-lookup"><span data-stu-id="4a1c9-111">*instance*</span></span>

<span data-ttu-id="4a1c9-112">指定要用於此呼叫的實例。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-112">Specifies the instance to use for this call.</span></span>

<span data-ttu-id="4a1c9-113">若為 Windows XP 和更新版本，則使用這個參數取決於引擎的操作模式。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-113">For Windows XP and later releases, the use of this parameter depends on the operating mode of the engine.</span></span> <span data-ttu-id="4a1c9-114">如果引擎是在舊版模式下運作 (Windows 2000 相容性模式) 只支援一個實例，此參數可以是 Null，也可以設定為包含 Null 或 JET_instanceNil 的有效輸出緩衝區，此緩衝區會傳回做為初始化的副作用所建立的全域實例控制碼。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-114">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported then this parameter may either be NULL or it may be set to a valid output buffer containing NULL or JET_instanceNil that will return the global instance handle created as a side effect of the initialization.</span></span> <span data-ttu-id="4a1c9-115">然後，這個實例控制碼可以傳遞給任何其他接受實例的 API。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-115">This instance handle can then be passed to any other API that takes an instance.</span></span> <span data-ttu-id="4a1c9-116">如果引擎是在多重實例模式中作業，則這個參數必須設定為有效的輸入緩衝區，其中包含正在初始化的 [JetCreateInstance](./jetcreateinstance-function.md) 所傳回的實例控制碼。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-116">If the engine is operating in multi-instance mode then this parameter must be set to a valid input buffer that contains the instance handle returned by [JetCreateInstance](./jetcreateinstance-function.md) that is being initialized.</span></span>

<span data-ttu-id="4a1c9-117">*深圳*</span><span class="sxs-lookup"><span data-stu-id="4a1c9-117">*sz*</span></span>

<span data-ttu-id="4a1c9-118">備份所在的資料夾。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-118">The folder where the backup is located.</span></span> <span data-ttu-id="4a1c9-119">應使用 [JetBackup](./jetbackup-function.md) api 來產生備份。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-119">The backup should have been generated using the [JetBackup](./jetbackup-function.md) APIs.</span></span>

<span data-ttu-id="4a1c9-120">*szDest*</span><span class="sxs-lookup"><span data-stu-id="4a1c9-120">*szDest*</span></span>

<span data-ttu-id="4a1c9-121">將從備份組複製和復原資料庫檔案的資料夾名稱。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-121">Name of the folder where the database files from the backup set will be copied and recovered.</span></span> <span data-ttu-id="4a1c9-122">如果這是設定為 Null (這是舊版 [JetRestore](./jetrestore-function.md)) 的情況，則會將資料庫檔案複製和復原到其原始位置。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-122">If this is set to NULL (which is the case for the legacy [JetRestore](./jetrestore-function.md)), the database files will be copied and recovered to their original location.</span></span>

<span data-ttu-id="4a1c9-123">*pfn*</span><span class="sxs-lookup"><span data-stu-id="4a1c9-123">*pfn*</span></span>

<span data-ttu-id="4a1c9-124">函式的選擇性指標，將會呼叫該函式做為還原作業進度的通知資訊。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-124">The optional pointer to the function which will be called as notification information about the progress of the restore operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="4a1c9-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="4a1c9-125">Return Value</span></span>

<span data-ttu-id="4a1c9-126">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-126">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="4a1c9-127">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-127">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4a1c9-128">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4a1c9-128">Return code</span></span></p></th>
<th><p><span data-ttu-id="4a1c9-129">Description</span><span class="sxs-lookup"><span data-stu-id="4a1c9-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4a1c9-130">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="4a1c9-130">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="4a1c9-131">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-131">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a1c9-132">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="4a1c9-132">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="4a1c9-133">作業失敗，因為此實例的引擎已初始化。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-133">The operation failed because the engine is already initialized for this instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a1c9-134">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="4a1c9-134">JET_errInvalidLogSequence</span></span></p></td>
<td><p><span data-ttu-id="4a1c9-135">來自備份組和目前記錄檔路徑的記錄檔集合不相符。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-135">The set of log files from the backup set and from the current log path do not match.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a1c9-136">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="4a1c9-136">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="4a1c9-137">提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-137">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="4a1c9-138">當引擎處於多重實例模式時， <strong>JetRestoreInstance</strong> 會傳回這個錯誤，而 pinstance 指的是不正確實例 Windows XP 和更新的版本。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-138">This error will be returned by <strong>JetRestoreInstance</strong> when the engine is in multi-instance mode and pinstance refers to an invalid instance Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a1c9-139">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="4a1c9-139">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="4a1c9-140">作業失敗，因為提供的部分路徑 (備份路徑、目的地路徑、實例的記錄檔或系統路徑) 無效。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-140">The operation failed because some of paths provided are invalid (the backup path, the destination path, the log or system path for the instance).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a1c9-141">JET_errPageSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="4a1c9-141">JET_errPageSizeMismatch</span></span></p></td>
<td><p><span data-ttu-id="4a1c9-142">作業失敗，因為引擎設定 <a href="gg294044(v=exchg.10).md">為使用資料庫</a> 頁面大小 (針對 <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) 不符合用來建立交易記錄檔的資料庫頁面大小，或與交易記錄檔相關聯的資料庫。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-142">The operation failed because the engine is configured to use a database page size (using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) that does not match the database page size used to create the transaction log files or the databases associated with the transaction log files.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a1c9-143">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="4a1c9-143">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="4a1c9-144">作業失敗，因為參數隱含的單一實例模式 (Windows 2000 相容性模式) ，而且引擎已在多重實例模式中。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-144">The operation failed because the parameters implied single instance mode (Windows 2000 compatibility mode) and the engine is already in multi-instance mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4a1c9-145">成功時，會將備份組的資料庫檔案還原至其位置，並執行復原，讓資料庫處於乾淨的交易一致性狀態。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-145">On success, database files from the backup set will be restored over to their location and recovery will be run such that the databases will be in a clean transactional consistency state.</span></span> <span data-ttu-id="4a1c9-146">如果有這類檔案，復原將會從備份組和記錄檔路徑中重新執行記錄檔。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-146">Recovery will replay the log files from the backup set and the log files from the log path if such files do exists.</span></span> <span data-ttu-id="4a1c9-147">這項復原會導致變更檢查點檔案、交易記錄檔，以及這些交易記錄檔所參考的任何資料庫。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-147">This recovery will result in changes to the checkpoint file, the transaction log files, and any databases referenced by those transaction log files.</span></span>

<span data-ttu-id="4a1c9-148">失敗時，實例會保持未初始化的狀態。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-148">On failure, the instance remains in an uninitialized state.</span></span> <span data-ttu-id="4a1c9-149">交易記錄檔的狀態以及這些交易記錄檔所參考的任何資料庫，在嘗試初始化還原和復原資料庫時，可能已經變更。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-149">The state of the transaction log files and any databases referenced by those transaction log files will likely have been changed in the attempt to initialize the restore and recover the databases.</span></span>

#### <a name="remarks"></a><span data-ttu-id="4a1c9-150">備註</span><span class="sxs-lookup"><span data-stu-id="4a1c9-150">Remarks</span></span>

<span data-ttu-id="4a1c9-151">復原進程會在備份期間重建附加至實例的資料庫，並將變更儲存回資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-151">The recovery process will reconstruct the databases attached to the instance during the backup and save the changes back to the database files.</span></span> <span data-ttu-id="4a1c9-152">結果會是交易一致的資料庫。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-152">The result will be databases that are transaction consistent.</span></span> <span data-ttu-id="4a1c9-153">可能的話，它也會儲存到資料庫中，因為備份是在交易記錄中找到最新的變更之後所做的變更。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-153">If possible, it will also save to the database the changes done since the backup was taken until the most recent change found in the transaction logs.</span></span> <span data-ttu-id="4a1c9-154">如果建立備份後產生的交易記錄仍存在於交易記錄檔目錄中，就可能會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-154">This would be possible if the transaction logs generated since the backup was taken are still present in the transaction log directory.</span></span> <span data-ttu-id="4a1c9-155">請注意，如果已啟用實例的迴圈記錄，則會重複使用所產生的交易記錄，讓復原能夠儲存在備份時所發生的變更。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-155">Note that if circular logging was enabled for the instance, the transaction logs generated are reused such that the recovery will be able to save the changes which took place up to the backup moment.</span></span> <span data-ttu-id="4a1c9-156">在任何情況下，如果要對資料庫重新執行的交易記錄檔數目很大，則此程式可能需要相當長的時間。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-156">In any case, it is possible for this process to take quite some time if the number of transaction log files to replay against the databases is large.</span></span>

<span data-ttu-id="4a1c9-157">您必須在已經使用 [JetCreateInstance](./jetcreateinstance-function.md)建立的實例上呼叫 **JetRestoreInstance** 。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-157">**JetRestoreInstance** must be called on an instance which was already created using [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

<span data-ttu-id="4a1c9-158">由於復原期間會使用大量的資料庫頁面和交易記錄，因此有一系列的錯誤可能會由這些函數傳回。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-158">Because during recovery a significant number of database pages and transaction logs will be used, there is an entire series of error which might be returned by these functions.</span></span> <span data-ttu-id="4a1c9-159">這類錯誤可能來自暫時性的資源配置失敗，例如 Jet_errOutOfMemory 為代表實體損毀的錯誤，例如 JET_errReadVerifyFailure、JET_errLogFileCorrupt 或 JET_errBadPageLink。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-159">Such errors can be from temporary resource allocation failures like Jet_errOutOfMemory to errors representing physical corruptions like JET_errReadVerifyFailure, JET_errLogFileCorrupt or JET_errBadPageLink.</span></span> <span data-ttu-id="4a1c9-160">這些錯誤幾乎都是由硬體問題所造成，因此無法避免。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-160">These errors are almost always caused by hardware problems and thus cannot be avoided.</span></span> <span data-ttu-id="4a1c9-161">檔案 mismanagement 本身最常是 JET_errMissingLogFile 或 JET_errAttachedDatabaseMismatch 或 JET_errDatabaseSharingViolation 或 JET_errInvalidLogSequence 的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-161">File mismanagement will manifest itself most often as JET_errMissingLogFile or JET_errAttachedDatabaseMismatch or JET_errDatabaseSharingViolation or JET_errInvalidLogSequence.</span></span> <span data-ttu-id="4a1c9-162">這些錯誤是由應用程式所 preventable。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-162">These errors are preventable by the application.</span></span> <span data-ttu-id="4a1c9-163">應用程式必須小心保護這些檔案的存放庫，使其不受使用者或其他應用程式這類外部強制操作的影響。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-163">The application must be careful to protect the repository of these files from manipulation by outside forces such as the user or other applications.</span></span> <span data-ttu-id="4a1c9-164">如果應用程式想要完全終結實例，則必須刪除與該實例相關聯的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-164">If the application desires to destroy an instance entirely then all the files associated with the instance must be deleted.</span></span> <span data-ttu-id="4a1c9-165">這些包括檢查點檔案、交易記錄檔，以及附加至實例的任何資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-165">These include the checkpoint file, the transaction log files, and any database files attached to the instance.</span></span>

<span data-ttu-id="4a1c9-166">復原的不同步驟將會產生事件記錄檔專案，包括交易記錄檔的重新執行進度和最後的還原結果。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-166">The different steps of the recovery will have Event Log entries generated including the transaction log replay progress and the final result of the restore.</span></span>

#### <a name="requirements"></a><span data-ttu-id="4a1c9-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a1c9-167">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4a1c9-168"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="4a1c9-168"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4a1c9-169">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-169">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a1c9-170"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="4a1c9-170"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4a1c9-171">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-171">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a1c9-172"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="4a1c9-172"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4a1c9-173">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-173">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a1c9-174"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="4a1c9-174"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="4a1c9-175">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-175">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a1c9-176"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="4a1c9-176"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="4a1c9-177">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-177">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a1c9-178"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="4a1c9-178"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="4a1c9-179">實作為 <strong>JetRestoreInstanceW</strong> (Unicode) 和 <strong>JetRestoreInstanceA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="4a1c9-179">Implemented as <strong>JetRestoreInstanceW</strong> (Unicode) and <strong>JetRestoreInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4a1c9-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a1c9-180">See Also</span></span>

[<span data-ttu-id="4a1c9-181">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4a1c9-181">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4a1c9-182">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="4a1c9-182">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="4a1c9-183">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="4a1c9-183">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="4a1c9-184">JetBackup</span><span class="sxs-lookup"><span data-stu-id="4a1c9-184">JetBackup</span></span>](./jetbackup-function.md)  
[<span data-ttu-id="4a1c9-185">JetBackupInstance</span><span class="sxs-lookup"><span data-stu-id="4a1c9-185">JetBackupInstance</span></span>](./jetbackupinstance-function.md)  
[<span data-ttu-id="4a1c9-186">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="4a1c9-186">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="4a1c9-187">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="4a1c9-187">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
