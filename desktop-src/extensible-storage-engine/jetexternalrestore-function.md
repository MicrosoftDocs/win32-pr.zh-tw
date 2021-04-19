---
description: 深入瞭解： JetExternalRestore 函數
title: JetExternalRestore 函式
TOCTitle: JetExternalRestore Function
ms:assetid: c930689a-3ea6-4c5a-9318-76f519f23343
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294088(v=EXCHG.10)
ms:contentKeyID: 32765703
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetExternalRestoreA
- JetExternalRestore
- JetExternalRestoreW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 087949817ac0bcbe2effe2ff136a6ce80084daa2
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "106981866"
---
# <a name="jetexternalrestore-function"></a><span data-ttu-id="51728-103">JetExternalRestore 函式</span><span class="sxs-lookup"><span data-stu-id="51728-103">JetExternalRestore Function</span></span>


<span data-ttu-id="51728-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="51728-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetexternalrestore-function"></a><span data-ttu-id="51728-105">JetExternalRestore 函式</span><span class="sxs-lookup"><span data-stu-id="51728-105">JetExternalRestore Function</span></span>

<span data-ttu-id="51728-106">**JetExternalRestore** 函式會還原使用外部備份 api 所建立的外部備份，並指定在還原過程中重新執行的記錄檔編號範圍。</span><span class="sxs-lookup"><span data-stu-id="51728-106">The **JetExternalRestore** function restores an external backup that was taken with the external backup APIs and specifies a range of log file numbers to replay during the restore process.</span></span> <span data-ttu-id="51728-107">這稱為「硬復原」，類似于 [JetInit](./jetinit-function.md) 函式所執行的軟復原。</span><span class="sxs-lookup"><span data-stu-id="51728-107">This is known as hard recovery, which is similar to but different than soft recovery as performed by the [JetInit](./jetinit-function.md) function.</span></span>

```cpp
JET_ERR JET_API JetExternalRestore(
  __in          JET_PSTR szCheckpointFilePath,
  __in          JET_PSTR szLogPath,
  __in_opt      JET_RSTMAP* rgrstmap,
  __in          long crstfilemap,
  __in          JET_PSTR szBackupLogPath,
  __in          long genLow,
  __in          long genHigh,
  __in          JET_PFNSTATUS pfn
);
```

### <a name="parameters"></a><span data-ttu-id="51728-108">參數</span><span class="sxs-lookup"><span data-stu-id="51728-108">Parameters</span></span>

<span data-ttu-id="51728-109">*szCheckpointFilePath*</span><span class="sxs-lookup"><span data-stu-id="51728-109">*szCheckpointFilePath*</span></span>

<span data-ttu-id="51728-110">如果未指定 *szTargetInstanceCheckpointPath* ，或已經有使用中或執行中的實例時，要在復原期間使用的檢查點檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="51728-110">The path for the checkpoint file to use during recovery if *szTargetInstanceCheckpointPath* is not specified or already has an active or running instance.</span></span>

<span data-ttu-id="51728-111">*szLogPath*</span><span class="sxs-lookup"><span data-stu-id="51728-111">*szLogPath*</span></span>

<span data-ttu-id="51728-112">最後一個階段記錄檔的路徑或目錄 (復原) 復原，也可能用於向前復原記錄。</span><span class="sxs-lookup"><span data-stu-id="51728-112">The path or directory for the logs for the final phase (undo) of recovery, and possibly for the roll forward logs.</span></span> <span data-ttu-id="51728-113">此路徑可能與 *szBackupLogPath* 相同。</span><span class="sxs-lookup"><span data-stu-id="51728-113">This path may be the same as the *szBackupLogPath*.</span></span>

<span data-ttu-id="51728-114">*rgrstmap*</span><span class="sxs-lookup"><span data-stu-id="51728-114">*rgrstmap*</span></span>

<span data-ttu-id="51728-115">這是 [JET_RSTMAP](./jet-rstmap-structure.md) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="51728-115">This is an array of [JET_RSTMAP](./jet-rstmap-structure.md) structures.</span></span> <span data-ttu-id="51728-116">這是舊的和新的資料庫路徑或檔案名的對應。</span><span class="sxs-lookup"><span data-stu-id="51728-116">This is a map of old and new database paths or filenames.</span></span> <span data-ttu-id="51728-117">這是使用的原因，是因為資料庫可能需要復原到與其備份來源位置不同的位置。</span><span class="sxs-lookup"><span data-stu-id="51728-117">This is used because the databases may need to be recovered to a location other than the location they were backed up from.</span></span> <span data-ttu-id="51728-118">如果將多個資料庫附加至單一記錄集，則還原對應可以指定要還原的資料庫子集。</span><span class="sxs-lookup"><span data-stu-id="51728-118">In the case where multiple databases are attached to a single logging set, the restore map can specify a subset of databases to restore.</span></span>

<span data-ttu-id="51728-119">*crstfilemap*</span><span class="sxs-lookup"><span data-stu-id="51728-119">*crstfilemap*</span></span>

<span data-ttu-id="51728-120">*Rgrstmap* 陣列參數中的專案數。</span><span class="sxs-lookup"><span data-stu-id="51728-120">The number of entries in the *rgrstmap* array parameter.</span></span>

<span data-ttu-id="51728-121">*szBackupLogPath*</span><span class="sxs-lookup"><span data-stu-id="51728-121">*szBackupLogPath*</span></span>

<span data-ttu-id="51728-122">要還原記錄檔之目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="51728-122">The path to the directory where the log files are restored.</span></span> <span data-ttu-id="51728-123">這些是在外部備份順序期間讀取的記錄。</span><span class="sxs-lookup"><span data-stu-id="51728-123">These are the logs that were read off during the external backup sequence.</span></span> <span data-ttu-id="51728-124">此路徑可能與 szLogPath 相同。</span><span class="sxs-lookup"><span data-stu-id="51728-124">This path may be the same as the szLogPath.</span></span>

<span data-ttu-id="51728-125">*genLow*</span><span class="sxs-lookup"><span data-stu-id="51728-125">*genLow*</span></span>

<span data-ttu-id="51728-126">要從 *szBackupLogPath* 重新執行的最小記錄檔編號。</span><span class="sxs-lookup"><span data-stu-id="51728-126">The lowest log file number that is to be replayed from *szBackupLogPath*.</span></span> <span data-ttu-id="51728-127">不帶正負號長度的完整精確度應該保留下來，但在目前的引擎版本中，這個數位是從0x00000 到0xFFFFF 的範圍內的十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="51728-127">The full fidelity of an unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="51728-128">在未來版本中可能會有所變動。</span><span class="sxs-lookup"><span data-stu-id="51728-128">This may change in future versions.</span></span>

<span data-ttu-id="51728-129">*genHigh*</span><span class="sxs-lookup"><span data-stu-id="51728-129">*genHigh*</span></span>

<span data-ttu-id="51728-130">要從 *szBackupLogPath* 重新執行的最高記錄檔編號。</span><span class="sxs-lookup"><span data-stu-id="51728-130">The highest log file number that is to be replayed from *szBackupLogPath*.</span></span> <span data-ttu-id="51728-131">不帶正負號長度的完整精確度應該保留，但在目前的引擎版本中，這個數位是從0x00000 到0xFFFFF 的十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="51728-131">The full fidelity of a unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="51728-132">在未來版本中可能會有所變動。</span><span class="sxs-lookup"><span data-stu-id="51728-132">This may change in future versions.</span></span>

<span data-ttu-id="51728-133">*pfn*</span><span class="sxs-lookup"><span data-stu-id="51728-133">*pfn*</span></span>

<span data-ttu-id="51728-134">狀態回呼，用來報告復原的進度。</span><span class="sxs-lookup"><span data-stu-id="51728-134">The status callback, to report progress of the recovery.</span></span>

### <a name="return-value"></a><span data-ttu-id="51728-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="51728-135">Return Value</span></span>

<span data-ttu-id="51728-136">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="51728-136">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="51728-137">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="51728-137">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="51728-138">傳回碼</span><span class="sxs-lookup"><span data-stu-id="51728-138">Return code</span></span></p></th>
<th><p><span data-ttu-id="51728-139">Description</span><span class="sxs-lookup"><span data-stu-id="51728-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51728-140">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="51728-140">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="51728-141">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="51728-141">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51728-142">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="51728-142">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="51728-143">作業失敗，因為無法配置足夠的記憶體來完成。</span><span class="sxs-lookup"><span data-stu-id="51728-143">The operation failed because not enough memory could be allocated to complete it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51728-144">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="51728-144">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="51728-145">提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="51728-145">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="51728-146"><strong>JetExternalRestore</strong>可能會發生這種情況，因此當<em>szTargetCheckpointPath</em>和<em>szTargetInstanceLogPath</em>都未指定，或未指定兩者皆未指定時。</span><span class="sxs-lookup"><span data-stu-id="51728-146">This can happen for <strong>JetExternalRestore</strong>, and so on when the <em>szTargetCheckpointPath</em> and the <em>szTargetInstanceLogPath</em> are either not both specified or not both unspecified.</span></span> <span data-ttu-id="51728-147">也就是說，它們必須相符，而且兩者都指定或都未指定。</span><span class="sxs-lookup"><span data-stu-id="51728-147">That is, they must match, and be both specified or both unspecified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51728-148">JET_errDatabaseCorrupted</span><span class="sxs-lookup"><span data-stu-id="51728-148">JET_errDatabaseCorrupted</span></span></p></td>
<td><p><span data-ttu-id="51728-149">這表示資料庫已損毀或無法辨識的檔案。</span><span class="sxs-lookup"><span data-stu-id="51728-149">This indicates the database was corrupted, or an unrecognized file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51728-150">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="51728-150">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="51728-151">作業失敗，因為它無法開啟要求的檔案，因為在指定的路徑中找不到該檔案。</span><span class="sxs-lookup"><span data-stu-id="51728-151">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51728-152">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="51728-152">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="51728-153">因為找不到指定的路徑，所以操作失敗。</span><span class="sxs-lookup"><span data-stu-id="51728-153">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51728-154">JET_errRestoreOfNonBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="51728-154">JET_errRestoreOfNonBackupDatabase</span></span></p></td>
<td><p><span data-ttu-id="51728-155">如果還原期間指定的資料庫檔案不是使用外部備份進行備份的資料庫，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="51728-155">This error is returned if the database file specified during restore is not a database that was backed up with external backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51728-156">JET_errStartingRestoreLogTooHigh</span><span class="sxs-lookup"><span data-stu-id="51728-156">JET_errStartingRestoreLogTooHigh</span></span></p></td>
<td><p><span data-ttu-id="51728-157">如果 <em>szBackupLogPath</em>中的其中一個記錄檔產生低於 <em>genLow</em> 或 <em>pLogInfo</em>所指定的記錄檔，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="51728-157">This error is returned if one of the log files in the <em>szBackupLogPath</em>, has a log generation below that specified by the <em>genLow</em> or <em>pLogInfo.ulGenLow</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51728-158">JET_errEndingRestoreLogTooLow</span><span class="sxs-lookup"><span data-stu-id="51728-158">JET_errEndingRestoreLogTooLow</span></span></p></td>
<td><p><span data-ttu-id="51728-159">如果 <em>szBackupLogPath</em>中記錄檔的記錄檔產生超過 <em>genHigh</em> 或 <em>pLogInfo</em>中指定的記錄檔，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="51728-159">This error is returned if one fo the log files in the <em>szBackupLogPath</em>, has a log generation above that specified in <em>genHigh</em> or <em>pLogInfo.ulGenHigh</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51728-160">JET_errBadRestoreTargetInstance</span><span class="sxs-lookup"><span data-stu-id="51728-160">JET_errBadRestoreTargetInstance</span></span></p></td>
<td><p><span data-ttu-id="51728-161">指定的 <em>szTargetInstanceLogPath</em> 不屬於初始化的實例。</span><span class="sxs-lookup"><span data-stu-id="51728-161">The <em>szTargetInstanceLogPath</em> specified does not belong to an initialized instance.</span></span> <span data-ttu-id="51728-162">只有在 Windows XP 和更新版本中才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="51728-162">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51728-163">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="51728-163">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="51728-164">資料庫引擎無法在單一實例模式中執行外部還原或硬復原。</span><span class="sxs-lookup"><span data-stu-id="51728-164">The database engine cannot run external restore or hard recovery in single instance mode.</span></span> <span data-ttu-id="51728-165">只有在 Windows XP 和更新版本中才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="51728-165">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="51728-166">成功時， *rgrstmap* 中的所有資料庫都會完全復原並處於乾淨或一致狀態。</span><span class="sxs-lookup"><span data-stu-id="51728-166">On success, all databases from the *rgrstmap* are completely recovered and in a clean or consistent state.</span></span> <span data-ttu-id="51728-167">此時，可以將資料庫重新掛接至現有的實例。</span><span class="sxs-lookup"><span data-stu-id="51728-167">At this point the database can be remounted to an existing instance.</span></span>

<span data-ttu-id="51728-168">失敗時，引擎無法復原資料庫。</span><span class="sxs-lookup"><span data-stu-id="51728-168">On failure, the engine could not recover the database.</span></span> <span data-ttu-id="51728-169">資料庫處於無效狀態，若要重試強制進行修復，必須再次還原整個資料庫。</span><span class="sxs-lookup"><span data-stu-id="51728-169">The database is in an invalid state, and in order to retry hard recovery the entire database must be restored again.</span></span> <span data-ttu-id="51728-170">一般來說，這種情況的來源是磁片或記錄檔損毀，或是其他形式的記錄 mismanagement 或非連續記錄集。</span><span class="sxs-lookup"><span data-stu-id="51728-170">Typically, the source of such a situation is disk or log corruption, or some other form of log mismanagement, or a non-continuous log set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="51728-171">備註</span><span class="sxs-lookup"><span data-stu-id="51728-171">Remarks</span></span>

<span data-ttu-id="51728-172">若要瞭解「硬性」復原的運作方式，您必須瞭解有三個階段的復原，而第二個階段可以有兩個部分。</span><span class="sxs-lookup"><span data-stu-id="51728-172">To understand how a "hard" recovery works, you must understand that there are three phases of recovery, and the second phase can have two parts.</span></span> <span data-ttu-id="51728-173">在第一個階段中，必須有記錄才能將備份的資料庫帶入一致性 (或者可以) 使用初始增量記錄集。</span><span class="sxs-lookup"><span data-stu-id="51728-173">In Phase I, logs are required to bring a backed up database to consistency (or an initial set of incremental logs can be used).</span></span> <span data-ttu-id="51728-174">在第二階段中，可以使用任何其他可用的向前復原記錄檔，讓資料庫保持一致。</span><span class="sxs-lookup"><span data-stu-id="51728-174">In Phase II, any additional roll forward logs that are available are consumed to make the database consistent.</span></span> <span data-ttu-id="51728-175">此外，還會重複執行其他向前復原記錄。</span><span class="sxs-lookup"><span data-stu-id="51728-175">There is also a replay of the additional roll forward logs.</span></span> <span data-ttu-id="51728-176">第 III 階段是復原的復原階段。</span><span class="sxs-lookup"><span data-stu-id="51728-176">Phase III is the undo phase of recovery.</span></span>

<span data-ttu-id="51728-177">階段 I：重新執行一組必須還原的記錄檔，以便讓資料庫進入一致的狀態 (或執行一組初始的記錄檔) 。</span><span class="sxs-lookup"><span data-stu-id="51728-177">Phase I: The replay of the set of logs that must be restored for the database to be brought to a consistent state (or an initial set of log files) is performed.</span></span> <span data-ttu-id="51728-178">基本上，這是針對正在還原的資料庫，重新執行不是選擇性的一組記錄檔。</span><span class="sxs-lookup"><span data-stu-id="51728-178">Basically, this is the replay of the set of log files that are not optional for the databases being restored.</span></span> <span data-ttu-id="51728-179">如果記錄檔範圍中有遺失的記錄，則還原將會失敗。</span><span class="sxs-lookup"><span data-stu-id="51728-179">If there are missing logs from this range of logs then the restore will fail.</span></span> <span data-ttu-id="51728-180">這些記錄檔應該放在 *szBackupLogPath* 參數所指定的目錄中。</span><span class="sxs-lookup"><span data-stu-id="51728-180">These logs should be put in the directory specified in the *szBackupLogPath* parameter.</span></span>

<span data-ttu-id="51728-181">第二階段：選擇性地，可能會有一些記錄檔，這些記錄檔是從增量或差異備份和使用中實例的記錄檔向前復原記錄檔。</span><span class="sxs-lookup"><span data-stu-id="51728-181">Phase II: Optionally, there may be some sets of log files that are roll forward log files that come from incremental or differential backups and from the log files of an active instance.</span></span> <span data-ttu-id="51728-182">如果是來自增量或差異備份的記錄檔，記錄檔可以放在 *szBackupLogPath* 或 *szTargetInstanceLogPath* 參數所指定的目錄中，而前者是建議的目錄。</span><span class="sxs-lookup"><span data-stu-id="51728-182">In the case of log files from incremental or differential backups, the log files can be placed in the directories specified in either the *szBackupLogPath* or the *szTargetInstanceLogPath* parameters, with the former being the recommended directory.</span></span> <span data-ttu-id="51728-183">用於向前復原階段 (階段 II) 的記錄，應該來自第一系列階段中所播放的相同記錄檔系列，而且應該持續遞增記錄檔編號，而不會有與記錄階段之間的差距。</span><span class="sxs-lookup"><span data-stu-id="51728-183">The logs used for the roll forward phase (phase II) should come from the same series of logs played during Phase I and should have continuously incrementing log numbers with no gaps from the Phase I logs.</span></span> <span data-ttu-id="51728-184">若要使用目前正在使用中實例的記錄檔來完全更新資料庫，必須指定 *szTargetInstanceLogPath* 和 *szTargetInstanceCheckpointPath* 參數。</span><span class="sxs-lookup"><span data-stu-id="51728-184">To play a database to be fully up to date with the log files currently being used by an active instance, the *szTargetInstanceLogPath* and *szTargetInstanceCheckpointPath* parameters must be specified.</span></span> <span data-ttu-id="51728-185">即使其他資料庫附加至該記錄集，也可以這麼做。</span><span class="sxs-lookup"><span data-stu-id="51728-185">This can be done even while other databases are attached to that log set.</span></span>

<span data-ttu-id="51728-186">第 III 階段：在復原的最後一個階段中，會回復任何未認可的交易，而這需要產生新的記錄檔和更新檢查點檔案。</span><span class="sxs-lookup"><span data-stu-id="51728-186">Phase III: In the final phase of recovery, any uncommitted transactions are rolled back, which requires generating new log files and updating the checkpoint file.</span></span> <span data-ttu-id="51728-187">這個階段有時稱為「復原」。</span><span class="sxs-lookup"><span data-stu-id="51728-187">This phase is sometimes referred to as "undo".</span></span> <span data-ttu-id="51728-188">在此階段中使用的檢查點檔案路徑是類似于階段 III 記錄檔位置的路徑，亦即，如果 *szLogPath* 用於階段 iii，則會使用 szCheckpointFilePath，如果 *SzTargetInstanceLogPath* 用於復原 *szTargetInstanceCheckpointPath* 的第三階段，將會使用 。</span><span class="sxs-lookup"><span data-stu-id="51728-188">The checkpoint file path to use during this phase is the path analogous to the phase III log location, that is, if *szLogPath* is used for Phase III, *szCheckpointFilePath* will be used, if *szTargetInstanceLogPath* is used for phase III of recovery *szTargetInstanceCheckpointPath* will be used.</span></span>

<span data-ttu-id="51728-189">若要瞭解路徑的運作方式，請使用此流程圖：</span><span class="sxs-lookup"><span data-stu-id="51728-189">To understand how the paths work, use this flow chart:</span></span>

<span data-ttu-id="51728-190">![ESE_Documentation_ese1](images/Gg294088.ESE_Documentation_ese1(EXCHG.10).gif "ESE_Documentation_ese1")</span><span class="sxs-lookup"><span data-stu-id="51728-190">![ESE_Documentation_ese1](images/Gg294088.ESE_Documentation_ese1(EXCHG.10).gif "ESE_Documentation_ese1")</span></span>

#### <a name="requirements"></a><span data-ttu-id="51728-191">規格需求</span><span class="sxs-lookup"><span data-stu-id="51728-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51728-192"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="51728-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="51728-193">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="51728-193">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51728-194"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="51728-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="51728-195">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="51728-195">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51728-196"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="51728-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="51728-197">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="51728-197">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51728-198"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="51728-198"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="51728-199">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="51728-199">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51728-200"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="51728-200"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="51728-201">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="51728-201">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51728-202"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="51728-202"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="51728-203">實作為 <strong>JetExternalRestoreW</strong> (Unicode) 和 <strong>JetExternalRestoreA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="51728-203">Implemented as <strong>JetExternalRestoreW</strong> (Unicode) and <strong>JetExternalRestoreA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="51728-204">另請參閱</span><span class="sxs-lookup"><span data-stu-id="51728-204">See Also</span></span>

[<span data-ttu-id="51728-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="51728-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="51728-206">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="51728-206">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="51728-207">JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="51728-207">JET_RSTMAP</span></span>](./jet-rstmap-structure.md)  
[<span data-ttu-id="51728-208">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="51728-208">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="51728-209">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="51728-209">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="51728-210">JetInit</span><span class="sxs-lookup"><span data-stu-id="51728-210">JetInit</span></span>](./jetinit-function.md)
