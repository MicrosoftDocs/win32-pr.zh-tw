---
description: 深入瞭解： JetExternalRestore2 函數
title: JetExternalRestore2 函式
TOCTitle: JetExternalRestore2 Function
ms:assetid: 66331be0-7abc-43a0-8b8b-dbdd227c918e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269272(v=EXCHG.10)
ms:contentKeyID: 32765574
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetExternalRestore2W
- JetExternalRestore2A
- JetExternalRestore2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c96314e401a81271f5a71bc056faa95fc1ae0dbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944693"
---
# <a name="jetexternalrestore2-function"></a><span data-ttu-id="2e779-103">JetExternalRestore2 函式</span><span class="sxs-lookup"><span data-stu-id="2e779-103">JetExternalRestore2 Function</span></span>


<span data-ttu-id="2e779-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2e779-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetexternalrestore2-function"></a><span data-ttu-id="2e779-105">JetExternalRestore2 函式</span><span class="sxs-lookup"><span data-stu-id="2e779-105">JetExternalRestore2 Function</span></span>

<span data-ttu-id="2e779-106">**JetExternalRestore2** 函式會還原使用外部備份 api 所建立的外部備份，並提供用於迴圈記錄作業的檢查點。</span><span class="sxs-lookup"><span data-stu-id="2e779-106">The **JetExternalRestore2** function restores an external backup that was taken with the external backup APIs and provides checkpoints to use for circular logging operations.</span></span> <span data-ttu-id="2e779-107">這稱為「硬復原」，這類似于 [JetInit](./jetinit-function.md) 函式所執行的軟復原。</span><span class="sxs-lookup"><span data-stu-id="2e779-107">This is known as hard recovery, which is similar but different than soft recovery as performed by the [JetInit](./jetinit-function.md) function.</span></span>

<span data-ttu-id="2e779-108">**Windows xp： JetExternalRestore2** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="2e779-108">**Windows XP:  JetExternalRestore2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetExternalRestore2(
      __in          JET_PSTR szCheckpointFilePath,
      __in          JET_PSTR szLogPath,
      __in_opt      JET_RSTMAP* rgrstmap,
      __in          long crstfilemap,
      __in          JET_PSTR szBackupLogPath,
      __in_out      JET_LOGINFO* pLogInfo,
      __in_opt      JET_PSTR szTargetInstanceName,
      __in_opt      JET_PSTR szTargetInstanceLogPath,
      __in_opt      JET_PSTR szTargetInstanceCheckpointPath,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a><span data-ttu-id="2e779-109">參數</span><span class="sxs-lookup"><span data-stu-id="2e779-109">Parameters</span></span>

<span data-ttu-id="2e779-110">*szCheckpointFilePath*</span><span class="sxs-lookup"><span data-stu-id="2e779-110">*szCheckpointFilePath*</span></span>

<span data-ttu-id="2e779-111">如果未指定 *szTargetInstanceCheckpointPath* 或路徑具有使用中或執行中的實例時，要在復原期間使用的檢查點檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="2e779-111">The path for the checkpoint file to use during recovery if *szTargetInstanceCheckpointPath* is not specified or that path has an active or running instance.</span></span>

<span data-ttu-id="2e779-112">*szLogPath*</span><span class="sxs-lookup"><span data-stu-id="2e779-112">*szLogPath*</span></span>

<span data-ttu-id="2e779-113">最後階段記錄檔的路徑或目錄 (復原) 復原，而且可能會向前復原記錄檔。</span><span class="sxs-lookup"><span data-stu-id="2e779-113">The path or directory for the logs for the final phase (undo) of the recovery and possibly for the roll forward logs.</span></span> <span data-ttu-id="2e779-114">此路徑可能與 *szBackupLogPath* 相同。</span><span class="sxs-lookup"><span data-stu-id="2e779-114">This path may be the same as the *szBackupLogPath*.</span></span>

<span data-ttu-id="2e779-115">*rgrstmap*</span><span class="sxs-lookup"><span data-stu-id="2e779-115">*rgrstmap*</span></span>

<span data-ttu-id="2e779-116">這是 [JET_RSTMAP](./jet-rstmap-structure.md) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="2e779-116">This is an array of [JET_RSTMAP](./jet-rstmap-structure.md) structures.</span></span> <span data-ttu-id="2e779-117">這是舊的和新的資料庫路徑或檔案名的對應。</span><span class="sxs-lookup"><span data-stu-id="2e779-117">This is a map of old and new database paths or filenames.</span></span> <span data-ttu-id="2e779-118">這是使用的原因，是因為資料庫可能需要復原到與其備份來源位置不同的位置。</span><span class="sxs-lookup"><span data-stu-id="2e779-118">This is used because the databases may need to be recovered to a location other than the location they were backed up from.</span></span> <span data-ttu-id="2e779-119">如果將多個資料庫附加至單一記錄集，則還原對應可以指定要還原的資料庫子集。</span><span class="sxs-lookup"><span data-stu-id="2e779-119">In the case where multiple databases are attached to a single logging set, the restore map can specify a subset of the databases to restore.</span></span>

<span data-ttu-id="2e779-120">*crstfilemap*</span><span class="sxs-lookup"><span data-stu-id="2e779-120">*crstfilemap*</span></span>

<span data-ttu-id="2e779-121">*Rgrstmap* 陣列參數中的專案數。</span><span class="sxs-lookup"><span data-stu-id="2e779-121">The number of entries in the *rgrstmap* array parameter.</span></span>

<span data-ttu-id="2e779-122">*szBackupLogPath*</span><span class="sxs-lookup"><span data-stu-id="2e779-122">*szBackupLogPath*</span></span>

<span data-ttu-id="2e779-123">要還原記錄檔之目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="2e779-123">The path to the directory where the log files are restored.</span></span> <span data-ttu-id="2e779-124">這些是在外部備份順序期間讀取的記錄。</span><span class="sxs-lookup"><span data-stu-id="2e779-124">These are the logs that were read off during the external backup sequence.</span></span> <span data-ttu-id="2e779-125">此路徑可能與 *szLogPath* 相同。</span><span class="sxs-lookup"><span data-stu-id="2e779-125">This path may be the same as the *szLogPath*.</span></span>

<span data-ttu-id="2e779-126">*pLogInfo*</span><span class="sxs-lookup"><span data-stu-id="2e779-126">*pLogInfo*</span></span>

<span data-ttu-id="2e779-127">*PLogInfo* 描述要復原之備份記錄的幾個層面，此參數可讓 **JetExternalRestore2** 取得 **JetExternalRestore2** 具有的明確 *genLow* 和 *genHigh* 參數，以及基底記錄檔名稱，而不是 "edb" 的假設記錄基底名稱。</span><span class="sxs-lookup"><span data-stu-id="2e779-127">The *pLogInfo* describes several aspects of the backup logs to recovery, this parameter allows **JetExternalRestore2** to take the explicit *genLow* and *genHigh* parameters that **JetExternalRestore2** has, as well as the base log name, instead of a presumed log base name of "edb".</span></span>

<span data-ttu-id="2e779-128">*szTargetInstanceName*</span><span class="sxs-lookup"><span data-stu-id="2e779-128">*szTargetInstanceName*</span></span>

<span data-ttu-id="2e779-129">此參數已被取代，無法在您的應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="2e779-129">This parameter is deprecated and cannot be used in your application.</span></span>

<span data-ttu-id="2e779-130">*szTargetInstanceLogPath*</span><span class="sxs-lookup"><span data-stu-id="2e779-130">*szTargetInstanceLogPath*</span></span>

<span data-ttu-id="2e779-131">如果您想要向前復原的記錄檔位置是在使用中的記錄集或實例中，則為向前復原記錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="2e779-131">The path for the roll forward logs if the location of the logs you would like to roll forward are in an active logging set or instance.</span></span> <span data-ttu-id="2e779-132">如果目標實例使用迴圈記錄，則不應指定此項。</span><span class="sxs-lookup"><span data-stu-id="2e779-132">This should not be specified if the target instance is using circular logging.</span></span>

<span data-ttu-id="2e779-133">*szTargetInstanceCheckpointPath*</span><span class="sxs-lookup"><span data-stu-id="2e779-133">*szTargetInstanceCheckpointPath*</span></span>

<span data-ttu-id="2e779-134">如果此目標沒有執行中的實例，則為復原期間的檢查點路徑。</span><span class="sxs-lookup"><span data-stu-id="2e779-134">The path for the checkpoint during recovery if there is no active instance running at this target.</span></span> <span data-ttu-id="2e779-135">如果目標實例使用迴圈記錄，則不應指定此項。</span><span class="sxs-lookup"><span data-stu-id="2e779-135">This should not be specified if the target instance is using circular logging.</span></span>

<span data-ttu-id="2e779-136">*pfn*</span><span class="sxs-lookup"><span data-stu-id="2e779-136">*pfn*</span></span>

<span data-ttu-id="2e779-137">狀態回呼，會報告復原的進度。</span><span class="sxs-lookup"><span data-stu-id="2e779-137">The status callback, which reports the progress of the recovery.</span></span>

### <a name="return-value"></a><span data-ttu-id="2e779-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="2e779-138">Return Value</span></span>

<span data-ttu-id="2e779-139">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="2e779-139">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="2e779-140">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="2e779-140">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2e779-141">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2e779-141">Return code</span></span></p></th>
<th><p><span data-ttu-id="2e779-142">Description</span><span class="sxs-lookup"><span data-stu-id="2e779-142">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e779-143">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="2e779-143">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="2e779-144">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="2e779-144">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e779-145">JET_errBadRestoreTargetInstance</span><span class="sxs-lookup"><span data-stu-id="2e779-145">JET_errBadRestoreTargetInstance</span></span></p></td>
<td><p><span data-ttu-id="2e779-146">指定的 <em>szTargetInstanceLogPath</em> 不屬於初始化的實例。</span><span class="sxs-lookup"><span data-stu-id="2e779-146">The <em>szTargetInstanceLogPath</em> specified does not belong to an initialized instance.</span></span> <span data-ttu-id="2e779-147">只有在 Windows XP 和更新版本中才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e779-147">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e779-148">JET_errDatabaseCorrupted</span><span class="sxs-lookup"><span data-stu-id="2e779-148">JET_errDatabaseCorrupted</span></span></p></td>
<td><p><span data-ttu-id="2e779-149">這表示資料庫已損毀或無法辨識的檔案。</span><span class="sxs-lookup"><span data-stu-id="2e779-149">This indicates the database was corrupted, or an unrecognized file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e779-150">JET_errEndingRestoreLogTooLow</span><span class="sxs-lookup"><span data-stu-id="2e779-150">JET_errEndingRestoreLogTooLow</span></span></p></td>
<td><p><span data-ttu-id="2e779-151">如果 <em>szBackupLogPath</em>中的記錄檔有一個以上的記錄檔產生，則會傳回此錯誤，該錯誤會在 <em>GenHigh</em> 或 <em>pLogInfo ulGenHigh</em>中指定。</span><span class="sxs-lookup"><span data-stu-id="2e779-151">This error is returned if one for the log files in the <em>szBackupLogPath</em>, has a log generation above that specified in <em>genHigh</em> or <em>pLogInfo.ulGenHigh</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e779-152">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="2e779-152">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="2e779-153">作業失敗，因為它無法開啟要求的檔案，因為在指定的路徑中找不到該檔案。</span><span class="sxs-lookup"><span data-stu-id="2e779-153">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e779-154">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="2e779-154">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="2e779-155">提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="2e779-155">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="2e779-156"><a href="gg294088(v=exchg.10).md">JetExternalRestore</a>可能會發生這種情況，因此當<em>szTargetCheckpointPath</em>和<em>szTargetInstanceLogPath</em>都未指定，或未指定兩者皆未指定時。</span><span class="sxs-lookup"><span data-stu-id="2e779-156">This can happen for <a href="gg294088(v=exchg.10).md">JetExternalRestore</a>, and so on when the <em>szTargetCheckpointPath</em> and the <em>szTargetInstanceLogPath</em> are either not both specified or not both unspecified.</span></span> <span data-ttu-id="2e779-157">也就是說，它們必須相符，而且兩者都指定或都未指定。</span><span class="sxs-lookup"><span data-stu-id="2e779-157">That is, they must match, and be both specified or both unspecified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e779-158">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="2e779-158">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="2e779-159">因為找不到指定的路徑，所以操作失敗。</span><span class="sxs-lookup"><span data-stu-id="2e779-159">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e779-160">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="2e779-160">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="2e779-161">作業失敗，因為無法配置足夠的記憶體來完成。</span><span class="sxs-lookup"><span data-stu-id="2e779-161">The operation failed because not enough memory could be allocated to complete it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e779-162">JET_errRestoreOfNonBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="2e779-162">JET_errRestoreOfNonBackupDatabase</span></span></p></td>
<td><p><span data-ttu-id="2e779-163">如果還原期間指定的資料庫檔案不是使用外部備份進行備份的資料庫，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e779-163">This error is returned if the database file specified during restore is not a database that was backed up with external backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e779-164">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="2e779-164">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="2e779-165">資料庫引擎無法在單一實例模式中執行外部還原或硬復原。</span><span class="sxs-lookup"><span data-stu-id="2e779-165">The database engine cannot run external restore or hard recovery in single instance mode.</span></span> <span data-ttu-id="2e779-166">只有在 Windows XP 和更新版本中才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e779-166">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e779-167">JET_errStartingRestoreLogTooHigh</span><span class="sxs-lookup"><span data-stu-id="2e779-167">JET_errStartingRestoreLogTooHigh</span></span></p></td>
<td><p><span data-ttu-id="2e779-168">如果 <em>szBackupLogPath</em>中的其中一個記錄檔產生低於 <em>genLow</em> 或 <em>pLogInfo</em>所指定的記錄檔，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e779-168">This error is returned if one of the log files in the <em>szBackupLogPath</em>, has a log generation below that specified by the <em>genLow</em> or <em>pLogInfo.ulGenLow</em>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2e779-169">成功時， *rgrstmap* 中的所有資料庫都會完全復原並處於乾淨或一致狀態。</span><span class="sxs-lookup"><span data-stu-id="2e779-169">On success, all databases from the *rgrstmap* are completely recovered and in a clean or consistent state.</span></span> <span data-ttu-id="2e779-170">此時，可以將資料庫重新掛接至現有的實例。</span><span class="sxs-lookup"><span data-stu-id="2e779-170">At this point the database can be remounted to an existing instance.</span></span>

<span data-ttu-id="2e779-171">失敗時，引擎無法復原資料庫。</span><span class="sxs-lookup"><span data-stu-id="2e779-171">On failure, the engine could not recover the database.</span></span> <span data-ttu-id="2e779-172">資料庫處於無效狀態，若要重試強制進行修復，必須再次還原整個資料庫。</span><span class="sxs-lookup"><span data-stu-id="2e779-172">The database is in an invalid state, and in order to retry hard recovery the entire database must be restored again.</span></span> <span data-ttu-id="2e779-173">一般來說，這種情況的來源是磁片或記錄檔損毀，或是其他形式的記錄 mismanagement 或非連續記錄集。</span><span class="sxs-lookup"><span data-stu-id="2e779-173">Typically, the source of such a situation is disk or log corruption, or some other form of log mismanagement, or a non-continuous log set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="2e779-174">備註</span><span class="sxs-lookup"><span data-stu-id="2e779-174">Remarks</span></span>

<span data-ttu-id="2e779-175">請參閱 [JetExternalRestore](./jetexternalrestore-function.md)。</span><span class="sxs-lookup"><span data-stu-id="2e779-175">See [JetExternalRestore](./jetexternalrestore-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="2e779-176">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e779-176">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e779-177"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="2e779-177"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2e779-178">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="2e779-178">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e779-179"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="2e779-179"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2e779-180">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="2e779-180">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e779-181"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="2e779-181"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2e779-182">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="2e779-182">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e779-183"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="2e779-183"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2e779-184">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="2e779-184">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e779-185"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="2e779-185"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2e779-186">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="2e779-186">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e779-187"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="2e779-187"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="2e779-188">實作為 <strong>JetExternalRestore2W</strong> (Unicode) 和 <strong>JetExternalRestore2A</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="2e779-188">Implemented as <strong>JetExternalRestore2W</strong> (Unicode) and <strong>JetExternalRestore2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="2e779-189">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e779-189">See Also</span></span>

[<span data-ttu-id="2e779-190">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2e779-190">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2e779-191">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="2e779-191">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="2e779-192">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="2e779-192">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="2e779-193">JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="2e779-193">JET_RSTMAP</span></span>](./jet-rstmap-structure.md)  
[<span data-ttu-id="2e779-194">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="2e779-194">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="2e779-195">JetExternalRestore</span><span class="sxs-lookup"><span data-stu-id="2e779-195">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="2e779-196">JetInit</span><span class="sxs-lookup"><span data-stu-id="2e779-196">JetInit</span></span>](./jetinit-function.md)
