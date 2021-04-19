---
description: 深入瞭解： JetRestore2 函數
title: JetRestore2 函式
TOCTitle: JetRestore2 Function
ms:assetid: 7f7fc2e3-727a-43e4-8497-64ff56d92b9f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269313(v=EXCHG.10)
ms:contentKeyID: 32765603
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestore2
- JetRestore2A
- JetRestore2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bb297aac0bc26e50bba519206eff346abb7943c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991926"
---
# <a name="jetrestore2-function"></a><span data-ttu-id="b3aa4-103">JetRestore2 函式</span><span class="sxs-lookup"><span data-stu-id="b3aa4-103">JetRestore2 Function</span></span>


<span data-ttu-id="b3aa4-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b3aa4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrestore2-function"></a><span data-ttu-id="b3aa4-105">JetRestore2 函式</span><span class="sxs-lookup"><span data-stu-id="b3aa4-105">JetRestore2 Function</span></span>

<span data-ttu-id="b3aa4-106">**JetRestore2** 會還原並復原實例的串流備份，包括所有附加的資料庫。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-106">The **JetRestore2** restores and recovers a streaming backup of an instance, including all the attached databases.</span></span> <span data-ttu-id="b3aa4-107">這項功能主要是為了與 Windows 2000 及舊版的資料庫引擎回溯相容，其中只允許一個資料庫的實例。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-107">This function is primarily for backwards compatibility with Windows 2000 and earlier database engines, where only one instance of a database is allowed.</span></span> <span data-ttu-id="b3aa4-108">在此情況下，使用中的實例是已還原的實例。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-108">In this case, the active instance is the instance that is restored.</span></span>

```cpp
    JET_ERR JET_API JetRestore2(
      __in          JET_PCSTR sz,
      __in_opt      JET_PCSTR szDest,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a><span data-ttu-id="b3aa4-109">參數</span><span class="sxs-lookup"><span data-stu-id="b3aa4-109">Parameters</span></span>

<span data-ttu-id="b3aa4-110">*深圳*</span><span class="sxs-lookup"><span data-stu-id="b3aa4-110">*sz*</span></span>

<span data-ttu-id="b3aa4-111">備份所在的資料夾。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-111">The folder where the backup is located.</span></span> <span data-ttu-id="b3aa4-112">應使用 [JetBackup](./jetbackup-function.md) api 來產生備份。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-112">The backup should have been generated using the [JetBackup](./jetbackup-function.md) APIs.</span></span>

<span data-ttu-id="b3aa4-113">*szDest*</span><span class="sxs-lookup"><span data-stu-id="b3aa4-113">*szDest*</span></span>

<span data-ttu-id="b3aa4-114">將從備份組複製和復原資料庫檔案的資料夾名稱。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-114">Name of the folder where the database files from the backup set will be copied and recovered.</span></span> <span data-ttu-id="b3aa4-115">如果這是設定為 Null (這是舊版 [JetRestore](./jetrestore-function.md)) 的情況，則會將資料庫檔案複製和復原到其原始位置。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-115">If this is set to NULL (which is the case for the legacy [JetRestore](./jetrestore-function.md)), the database files will be copied and recovered to their original location.</span></span>

<span data-ttu-id="b3aa4-116">*pfn*</span><span class="sxs-lookup"><span data-stu-id="b3aa4-116">*pfn*</span></span>

<span data-ttu-id="b3aa4-117">函式的選擇性指標，將會呼叫該函式做為還原作業進度的通知資訊。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-117">The optional pointer to the function which will be called as notification information about the progress of the restore operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="b3aa4-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="b3aa4-118">Return Value</span></span>

<span data-ttu-id="b3aa4-119">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b3aa4-120">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b3aa4-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b3aa4-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="b3aa4-122">Description</span><span class="sxs-lookup"><span data-stu-id="b3aa4-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b3aa4-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b3aa4-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b3aa4-124">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3aa4-125">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="b3aa4-125">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="b3aa4-126">作業失敗，因為此實例的引擎已初始化。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-126">The operation failed because the engine is already initialized for this instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3aa4-127">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="b3aa4-127">JET_errInvalidLogSequence</span></span></p></td>
<td><p><span data-ttu-id="b3aa4-128">來自備份組和目前記錄檔路徑的記錄檔集合不相符。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-128">The set of log files from the backup set and from the current log path do not match.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3aa4-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="b3aa4-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="b3aa4-130">提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-130">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="b3aa4-131">當引擎處於多重實例模式時， <a href="gg269306(v=exchg.10).md">JetRestoreInstance</a> 會傳回這個錯誤，而 pinstance 指的是不正確實例 Windows XP 和更新的版本。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-131">This error will be returned by <a href="gg269306(v=exchg.10).md">JetRestoreInstance</a> when the engine is in multi-instance mode and pinstance refers to an invalid instance Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3aa4-132">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="b3aa4-132">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="b3aa4-133">作業失敗，因為提供的部分路徑 (備份路徑、目的地路徑、實例的記錄檔或系統路徑) 無效。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-133">The operation failed because some of paths provided are invalid (the backup path, the destination path, the log or system path for the instance).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3aa4-134">JET_errPageSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="b3aa4-134">JET_errPageSizeMismatch</span></span></p></td>
<td><p><span data-ttu-id="b3aa4-135">作業失敗，因為引擎設定 <a href="gg294044(v=exchg.10).md">為使用資料庫</a> 頁面大小 (針對 <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) 不符合用來建立交易記錄檔的資料庫頁面大小，或與交易記錄檔相關聯的資料庫。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-135">The operation failed because the engine is configured to use a database page size (using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) that does not match the database page size used to create the transaction log files or the databases associated with the transaction log files.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3aa4-136">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="b3aa4-136">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="b3aa4-137">作業失敗，因為參數隱含的單一實例模式 (Windows 2000 相容性模式) ，而且引擎已在多重實例模式中。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-137">The operation failed because the parameters implied single instance mode (Windows 2000 compatibility mode) and the engine is already in multi-instance mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b3aa4-138">成功時，會將備份組的資料庫檔案還原至其位置，並執行復原，讓資料庫處於乾淨的交易一致性狀態。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-138">On success, database files from the backup set will be restored over to their location and recovery will be run such that the databases will be in a clean transactional consistency state.</span></span> <span data-ttu-id="b3aa4-139">如果有這類檔案，復原將會從備份組和記錄檔路徑中重新執行記錄檔。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-139">Recovery will replay the log files from the backup set and the log files from the log path if such files do exists.</span></span> <span data-ttu-id="b3aa4-140">這項復原會導致變更檢查點檔案、交易記錄檔，以及這些交易記錄檔所參考的任何資料庫。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-140">This recovery will result in changes to the checkpoint file, the transaction log files, and any databases referenced by those transaction log files.</span></span>

<span data-ttu-id="b3aa4-141">失敗時，實例會保持未初始化的狀態。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-141">On failure, the instance remains in an uninitialized state.</span></span> <span data-ttu-id="b3aa4-142">交易記錄檔的狀態以及這些交易記錄檔所參考的任何資料庫，在嘗試初始化還原和復原資料庫時，可能已經變更。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-142">The state of the transaction log files and any databases referenced by those transaction log files will likely have been changed in the attempt to initialize the restore and recover the databases.</span></span>

#### <a name="remarks"></a><span data-ttu-id="b3aa4-143">備註</span><span class="sxs-lookup"><span data-stu-id="b3aa4-143">Remarks</span></span>

<span data-ttu-id="b3aa4-144">復原進程會在備份期間重建附加至實例的資料庫，並將變更儲存回資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-144">The recovery process will reconstruct the databases attached to the instance during the backup and save the changes back to the database files.</span></span> <span data-ttu-id="b3aa4-145">結果會是交易一致的資料庫。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-145">The result will be databases that are transaction consistent.</span></span> <span data-ttu-id="b3aa4-146">可能的話，它也會儲存到資料庫中，因為備份是在交易記錄中找到最新的變更之後所做的變更。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-146">If possible, it will also save to the database the changes done since the backup was taken until the most recent change found in the transaction logs.</span></span> <span data-ttu-id="b3aa4-147">如果建立備份後產生的交易記錄仍存在於交易記錄檔目錄中，就可能會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-147">This would be possible if the transaction logs generated since the backup was taken are still present in the transaction log directory.</span></span> <span data-ttu-id="b3aa4-148">請注意，如果已啟用實例的迴圈記錄，則會重複使用所產生的交易記錄，讓復原能夠儲存在備份時所發生的變更。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-148">Note that if circular logging was enabled for the instance, the transaction logs generated are reused such that the recovery will be able to save the changes which took place up to the backup moment.</span></span> <span data-ttu-id="b3aa4-149">在任何情況下，如果要對資料庫重新執行的交易記錄檔數目很大，則此程式可能需要相當長的時間。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-149">In any case, it is possible for this process to take quite some time if the number of transaction log files to replay against the databases is large.</span></span>

<span data-ttu-id="b3aa4-150">在針對該實例呼叫[JetInit](./jetinit-function.md)之前，必須在實例上呼叫[JetRestore](./jetrestore-function.md)函數。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-150">[JetRestore](./jetrestore-function.md) functions must be called on an instance before [JetInit](./jetinit-function.md) is called for that instance.</span></span>

<span data-ttu-id="b3aa4-151">由於復原期間會使用大量的資料庫頁面和交易記錄，因此有一系列的錯誤可能會由這些函數傳回。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-151">Because during recovery a significant number of database pages and transaction logs will be used, there is an entire series of error which might be returned by these functions.</span></span> <span data-ttu-id="b3aa4-152">這類錯誤可能來自暫時性的資源配置失敗，例如 Jet_errOutOfMemory 為代表實體損毀的錯誤，例如 JET_errReadVerifyFailure、JET_errLogFileCorrupt 或 JET_errBadPageLink。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-152">Such errors can be from temporary resource allocation failures like Jet_errOutOfMemory to errors representing physical corruptions like JET_errReadVerifyFailure, JET_errLogFileCorrupt or JET_errBadPageLink.</span></span> <span data-ttu-id="b3aa4-153">這些錯誤幾乎都是由硬體問題所造成，因此無法避免。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-153">These errors are almost always caused by hardware problems and thus cannot be avoided.</span></span> <span data-ttu-id="b3aa4-154">檔案 mismanagement 本身最常是 JET_errMissingLogFile 或 JET_errAttachedDatabaseMismatch 或 JET_errDatabaseSharingViolation 或 JET_errInvalidLogSequence 的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-154">File mismanagement will manifest itself most often as JET_errMissingLogFile or JET_errAttachedDatabaseMismatch or JET_errDatabaseSharingViolation or JET_errInvalidLogSequence.</span></span> <span data-ttu-id="b3aa4-155">這些錯誤是由應用程式所 preventable。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-155">These errors are preventable by the application.</span></span> <span data-ttu-id="b3aa4-156">應用程式必須小心保護這些檔案的存放庫，使其不受使用者或其他應用程式這類外部強制操作的影響。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-156">The application must be careful to protect the repository of these files from manipulation by outside forces such as the user or other applications.</span></span> <span data-ttu-id="b3aa4-157">如果應用程式想要完全終結實例，則必須刪除與該實例相關聯的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-157">If the application desires to destroy an instance entirely then all the files associated with the instance must be deleted.</span></span> <span data-ttu-id="b3aa4-158">這些包括檢查點檔案、交易記錄檔，以及附加至實例的任何資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-158">These include the checkpoint file, the transaction log files, and any database files attached to the instance.</span></span>

<span data-ttu-id="b3aa4-159">復原的不同步驟將會產生事件記錄檔專案，包括交易記錄檔的重新執行進度和最後的還原結果。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-159">The different steps of the recovery will have Event Log entries generated including the transaction log replay progress and the final result of the restore.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b3aa4-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3aa4-160">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b3aa4-161"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="b3aa4-161"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b3aa4-162">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-162">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3aa4-163"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="b3aa4-163"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b3aa4-164">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-164">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3aa4-165"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="b3aa4-165"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b3aa4-166">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-166">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3aa4-167"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="b3aa4-167"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b3aa4-168">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-168">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3aa4-169"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b3aa4-169"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b3aa4-170">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-170">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3aa4-171"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="b3aa4-171"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="b3aa4-172">實作為 <strong>JetRestore2W</strong> (Unicode) 和 <strong>JetRestore2A</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="b3aa4-172">Implemented as <strong>JetRestore2W</strong> (Unicode) and <strong>JetRestore2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b3aa4-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3aa4-173">See Also</span></span>

[<span data-ttu-id="b3aa4-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b3aa4-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b3aa4-175">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="b3aa4-175">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="b3aa4-176">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="b3aa4-176">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="b3aa4-177">JetBackup</span><span class="sxs-lookup"><span data-stu-id="b3aa4-177">JetBackup</span></span>](./jetbackup-function.md)  
[<span data-ttu-id="b3aa4-178">JetBackupInstance</span><span class="sxs-lookup"><span data-stu-id="b3aa4-178">JetBackupInstance</span></span>](./jetbackupinstance-function.md)  
[<span data-ttu-id="b3aa4-179">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="b3aa4-179">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="b3aa4-180">JetInit</span><span class="sxs-lookup"><span data-stu-id="b3aa4-180">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="b3aa4-181">JetRestore</span><span class="sxs-lookup"><span data-stu-id="b3aa4-181">JetRestore</span></span>](./jetrestore-function.md)  
[<span data-ttu-id="b3aa4-182">JetRestoreInstance</span><span class="sxs-lookup"><span data-stu-id="b3aa4-182">JetRestoreInstance</span></span>](./jetrestoreinstance-function.md)  
[<span data-ttu-id="b3aa4-183">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="b3aa4-183">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
