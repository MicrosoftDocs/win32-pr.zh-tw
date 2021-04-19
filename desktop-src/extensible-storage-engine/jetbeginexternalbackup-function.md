---
description: 深入瞭解： JetBeginExternalBackup 函數
title: JetBeginExternalBackup 函式
TOCTitle: JetBeginExternalBackup Function
ms:assetid: 702e6cbf-4648-40f2-b2eb-6194759d4cde
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269292(v=EXCHG.10)
ms:contentKeyID: 32765584
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d410adb592c3d56d2f9880ec809749396318258a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000326"
---
# <a name="jetbeginexternalbackup-function"></a><span data-ttu-id="f4c78-103">JetBeginExternalBackup 函式</span><span class="sxs-lookup"><span data-stu-id="f4c78-103">JetBeginExternalBackup Function</span></span>


<span data-ttu-id="f4c78-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f4c78-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbeginexternalbackup-function"></a><span data-ttu-id="f4c78-105">JetBeginExternalBackup 函式</span><span class="sxs-lookup"><span data-stu-id="f4c78-105">JetBeginExternalBackup Function</span></span>

<span data-ttu-id="f4c78-106">**JetBeginExternalBackup** 函式會在引擎和資料庫在線上且使用中時，起始外部備份。</span><span class="sxs-lookup"><span data-stu-id="f4c78-106">The **JetBeginExternalBackup** function initiates an external backup while the engine and database is online and active.</span></span> <span data-ttu-id="f4c78-107">**JetBeginExternalBackup** 是一系列函式中的第一個函式，必須呼叫這些函式，以執行 (非 VSS 型) 備份成功連線。</span><span class="sxs-lookup"><span data-stu-id="f4c78-107">**JetBeginExternalBackup** is the first in a series of functions that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="f4c78-108">外部備份可以用來執行完整、增量或差異備份。</span><span class="sxs-lookup"><span data-stu-id="f4c78-108">An external backup can be used to implement full, incremental, or differential backups.</span></span>

<span data-ttu-id="f4c78-109">備份將會是模糊的，因為備份會與交易記錄中的單一時間點一致，但無法控制確切的時間點。</span><span class="sxs-lookup"><span data-stu-id="f4c78-109">The backup will be fuzzy, in that the backup will be consistent to a single point in time in the transaction history, but controlling the exact point in time is not possible.</span></span>

```cpp
    JET_ERR JET_API JetBeginExternalBackup(
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="f4c78-110">參數</span><span class="sxs-lookup"><span data-stu-id="f4c78-110">Parameters</span></span>

<span data-ttu-id="f4c78-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="f4c78-111">*grbit*</span></span>

<span data-ttu-id="f4c78-112">指定零或多個下列選項的位群組。</span><span class="sxs-lookup"><span data-stu-id="f4c78-112">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f4c78-113">值</span><span class="sxs-lookup"><span data-stu-id="f4c78-113">Value</span></span></p></th>
<th><p><span data-ttu-id="f4c78-114">意義</span><span class="sxs-lookup"><span data-stu-id="f4c78-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4c78-115">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="f4c78-115">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="f4c78-116">此旗標已被取代。</span><span class="sxs-lookup"><span data-stu-id="f4c78-116">This flag is deprecated.</span></span> <span data-ttu-id="f4c78-117">使用此位會導致傳回 JET_errInvalidgrbit。</span><span class="sxs-lookup"><span data-stu-id="f4c78-117">Usage of this bit will result in JET_errInvalidgrbit being returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4c78-118">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="f4c78-118">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="f4c78-119">建立增量備份，而不是完整備份。</span><span class="sxs-lookup"><span data-stu-id="f4c78-119">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="f4c78-120">這表示只會備份自上次完整或增量備份之後的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="f4c78-120">This means that only the log files since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4c78-121">JET_bitBackupSnapshot</span><span class="sxs-lookup"><span data-stu-id="f4c78-121">JET_bitBackupSnapshot</span></span></p></td>
<td><p><span data-ttu-id="f4c78-122">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="f4c78-122">Reserved for future use.</span></span> <span data-ttu-id="f4c78-123">針對 Windows XP 定義。</span><span class="sxs-lookup"><span data-stu-id="f4c78-123">Defined for Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="f4c78-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="f4c78-124">Return Value</span></span>

<span data-ttu-id="f4c78-125">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="f4c78-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f4c78-126">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="f4c78-126">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f4c78-127">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f4c78-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="f4c78-128">Description</span><span class="sxs-lookup"><span data-stu-id="f4c78-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4c78-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f4c78-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f4c78-130">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="f4c78-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4c78-131">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="f4c78-131">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="f4c78-132">如果外部備份或快照集備份已在處理中，則會傳回此錯誤，直到 <strong>JetBeginExternalBackup</strong> (或呼叫它的其中一個變數) 為止。</span><span class="sxs-lookup"><span data-stu-id="f4c78-132">If an external backup or snapshot backup is already in process, this error will be returned, until <strong>JetBeginExternalBackup</strong> (or one of the variants of it) is called.</span></span> <span data-ttu-id="f4c78-133">ESE 一次只允許一個線上備份。</span><span class="sxs-lookup"><span data-stu-id="f4c78-133">ESE allows only one online backup at a time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4c78-134">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="f4c78-134">JET_errBackupNotAllowedYet</span></span></p></td>
<td><p><span data-ttu-id="f4c78-135">實例或資料庫引擎處於復原或處於關機或終止階段。</span><span class="sxs-lookup"><span data-stu-id="f4c78-135">The instance or database engine is either in recovery or in a shutdown or termination phase.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4c78-136">JET_errCheckpointCorrupt</span><span class="sxs-lookup"><span data-stu-id="f4c78-136">JET_errCheckpointCorrupt</span></span></p></td>
<td><p><span data-ttu-id="f4c78-137">在完整備份上，無法讀取檢查點檔案，或無法驗證檔案。</span><span class="sxs-lookup"><span data-stu-id="f4c78-137">On a full backup, the checkpoint file could not be read, or the file could not be verified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4c78-138">JET_errCheckpointFileNotFound</span><span class="sxs-lookup"><span data-stu-id="f4c78-138">JET_errCheckpointFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="f4c78-139">在完整備份上，找不到檢查點檔案。</span><span class="sxs-lookup"><span data-stu-id="f4c78-139">On a full backup, the checkpoint file could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4c78-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="f4c78-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="f4c78-141">無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</span><span class="sxs-lookup"><span data-stu-id="f4c78-141">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4c78-142">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="f4c78-142">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="f4c78-143">作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="f4c78-143">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="f4c78-144"><strong>WINDOWS XP：  </strong>這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="f4c78-144"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4c78-145">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="f4c78-145">JET_errInvalidBackup</span></span></p></td>
<td><p><span data-ttu-id="f4c78-146">啟用迴圈記錄，並 JET_bitBackupIncremental 指定的備份類型。</span><span class="sxs-lookup"><span data-stu-id="f4c78-146">Circular logging is enabled and the backup type specified is JET_bitBackupIncremental.</span></span> <span data-ttu-id="f4c78-147">如需如何控制迴圈或非迴圈記錄的詳細資訊，請參閱<strong>交易記錄錯誤</strong>中的<a href="gg269235(v=exchg.10).md">JET_paramCircularLog</a> 。</span><span class="sxs-lookup"><span data-stu-id="f4c78-147">See <a href="gg269235(v=exchg.10).md">JET_paramCircularLog</a> in the <strong>Transaction Log Errors</strong> for information about how to control circular or non-circular logging.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4c78-148">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="f4c78-148">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="f4c78-149">一或多個 <em>grbit</em> 成員無效。</span><span class="sxs-lookup"><span data-stu-id="f4c78-149">One or more of the <em>grbit</em> members was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4c78-150">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="f4c78-150">JET_errLoggingDisabled</span></span></p></td>
<td><p><span data-ttu-id="f4c78-151">修復或記錄已停用。</span><span class="sxs-lookup"><span data-stu-id="f4c78-151">Recovery or logging is disabled.</span></span> <span data-ttu-id="f4c78-152">如果已停用記錄功能，您就無法進行線上備份。</span><span class="sxs-lookup"><span data-stu-id="f4c78-152">You cannot do an online backup if logging is disabled.</span></span> <span data-ttu-id="f4c78-153">如需有關記錄和復原的詳細資訊，請參閱 <a href="gg269235(v=exchg.10).md">JET_paramRecovery</a>。</span><span class="sxs-lookup"><span data-stu-id="f4c78-153">For more information about logging and recovery, see <a href="gg269235(v=exchg.10).md">JET_paramRecovery</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4c78-154">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="f4c78-154">JET_errLogWriteFail</span></span></p></td>
<td><p><span data-ttu-id="f4c78-155">引擎已停止寫入記錄磁片磁碟機，因為記錄檔已滿或磁片 IO 錯誤。</span><span class="sxs-lookup"><span data-stu-id="f4c78-155">The engine has stopped writing to the log drive, due to log being full or disk IO errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4c78-156">JET_errMissingFullBackup</span><span class="sxs-lookup"><span data-stu-id="f4c78-156">JET_errMissingFullBackup</span></span></p></td>
<td><p><span data-ttu-id="f4c78-157">增量備份是指定 (與 JET_bitBackupIncremental) ，而不是針對記錄集的其中一個連接資料庫所建立的完整備份。</span><span class="sxs-lookup"><span data-stu-id="f4c78-157">The incremental backup was specified (with JET_bitBackupIncremental), and never was a full backup taken for one of the attached databases for the logging set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4c78-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="f4c78-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="f4c78-159">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="f4c78-159">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4c78-160">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="f4c78-160">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="f4c78-161">作業失敗，因為無法配置足夠的記憶體來完成。</span><span class="sxs-lookup"><span data-stu-id="f4c78-161">The operation failed because not enough memory could be allocated to complete it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4c78-162">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="f4c78-162">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="f4c78-163">作業無法完成，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="f4c78-163">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4c78-164">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="f4c78-164">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="f4c78-165">作業失敗，因為嘗試使用舊版模式中的引擎 (Windows 2000 相容性模式) 在事實中，如果有多個實例存在，則只支援一個實例。</span><span class="sxs-lookup"><span data-stu-id="f4c78-165">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4c78-166">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="f4c78-166">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="f4c78-167">無法完成作業，因為與會話相關聯的實例正在關閉中。</span><span class="sxs-lookup"><span data-stu-id="f4c78-167">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f4c78-168">如果函式成功，則會起始外部備份並初始化備份狀態引擎。</span><span class="sxs-lookup"><span data-stu-id="f4c78-168">If the function succeeds, an external backup is initiated and the backup state engine is initialized.</span></span> <span data-ttu-id="f4c78-169">您現在可以呼叫後續的 Api 來完成外部備份順序，以及串流或讀取資料庫檔案、資料庫修補檔 (是否支援) 和記錄檔。</span><span class="sxs-lookup"><span data-stu-id="f4c78-169">Subsequent APIs can now be called to complete the external backup sequence and stream or read off the database file, the database patch file (if supported), and the log file.</span></span> <span data-ttu-id="f4c78-170">您可以記錄外部備份已開始的事件。</span><span class="sxs-lookup"><span data-stu-id="f4c78-170">An event can be logged that an external backup has begun.</span></span>

<span data-ttu-id="f4c78-171">如果函式失敗，將不會起始備份會話。</span><span class="sxs-lookup"><span data-stu-id="f4c78-171">If the function fails, the backup session will not be initiated.</span></span> <span data-ttu-id="f4c78-172">如果另一個備份會話正在進行中，則不會取消。</span><span class="sxs-lookup"><span data-stu-id="f4c78-172">If another backup session is in progress, it will not be cancelled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f4c78-173">備註</span><span class="sxs-lookup"><span data-stu-id="f4c78-173">Remarks</span></span>

<span data-ttu-id="f4c78-174">**JetBeginExternalBackup**) 所啟動的外部備份程式 (，其設計目的是要讓整個實例的模糊交易線上備份成為串流的目標裝置。</span><span class="sxs-lookup"><span data-stu-id="f4c78-174">The external backup process (as started by **JetBeginExternalBackup**) is designed to allow a fuzzy transaction online backup of the entire instance to a target device as a stream.</span></span> <span data-ttu-id="f4c78-175">備份將會包含所有附加至實例的資料庫檔案，其使用 [JetAttachDatabase](./jetattachdatabase-function.md) (進行完整備份) ，後面接著其相關聯的資料庫修補檔案 (如果支援) ，最後是備份程式期間產生的交易記錄檔。</span><span class="sxs-lookup"><span data-stu-id="f4c78-175">The backup will contain all the database files that are attached to the instance using [JetAttachDatabase](./jetattachdatabase-function.md) (for a full backup), followed by their associated database patch files (if supported), and finally by the transaction log files that were generated during the backup process.</span></span> <span data-ttu-id="f4c78-176">最終結果將會是一組可從資料流程還原的檔案，可能會與現有的資料庫和記錄檔結合，最後會復原到一致的狀態。</span><span class="sxs-lookup"><span data-stu-id="f4c78-176">The end result will be a set of files that can be restored from the stream, possibly combined with existing database and log files, and finally recovered to a consistent state.</span></span>

<span data-ttu-id="f4c78-177">完整備份的一般作業順序是由下列呼叫所組成。</span><span class="sxs-lookup"><span data-stu-id="f4c78-177">The general order of operations for a full backup consists of the following calls.</span></span> <span data-ttu-id="f4c78-178">首先，呼叫 **JetBeginExternalBackup** 以開始備份程式。</span><span class="sxs-lookup"><span data-stu-id="f4c78-178">First, **JetBeginExternalBackup** is called to start the backup process.</span></span> <span data-ttu-id="f4c78-179">然後，呼叫 [JetGetAttachInfo](./jetgetattachinfo-function.md) 以取得附加至需要備份之實例的資料庫清單。</span><span class="sxs-lookup"><span data-stu-id="f4c78-179">Then, [JetGetAttachInfo](./jetgetattachinfo-function.md) is called to get the list of databases that are attached to the instance that needs to be backed up.</span></span> <span data-ttu-id="f4c78-180">針對每個資料庫，會呼叫 [JetOpenFile](./jetopenfile-function.md) ，後面接著幾個 [JetReadFile](./jetreadfile-function.md) 呼叫，然後呼叫 [JetCloseFile](./jetclosefile-function.md)。</span><span class="sxs-lookup"><span data-stu-id="f4c78-180">For each of these databases, [JetOpenFile](./jetopenfile-function.md) is called, followed by a number of [JetReadFile](./jetreadfile-function.md) calls, and then by a call to [JetCloseFile](./jetclosefile-function.md).</span></span> <span data-ttu-id="f4c78-181">然後，呼叫 [JetGetLogInfo](./jetgetloginfo-function.md) 以取得要備份之資料庫修補和記錄檔的清單。</span><span class="sxs-lookup"><span data-stu-id="f4c78-181">Then, [JetGetLogInfo](./jetgetloginfo-function.md) is called to get a list of database patch and log files to be backed up.</span></span> <span data-ttu-id="f4c78-182">針對每個檔案，會進行另一個 [JetOpenFile](./jetopenfile-function.md)、 [JetReadFile](./jetreadfile-function.md)和 [JetCloseFile](./jetclosefile-function.md) 呼叫順序。</span><span class="sxs-lookup"><span data-stu-id="f4c78-182">For each of these files, another sequence of [JetOpenFile](./jetopenfile-function.md), [JetReadFile](./jetreadfile-function.md), and [JetCloseFile](./jetclosefile-function.md) calls are made.</span></span> <span data-ttu-id="f4c78-183">然後，會使用 [JetTruncateLog](./jettruncatelog-function.md)刪除任何不想要的交易記錄檔。</span><span class="sxs-lookup"><span data-stu-id="f4c78-183">Then, any undesired transaction log files are deleted using [JetTruncateLog](./jettruncatelog-function.md).</span></span> <span data-ttu-id="f4c78-184">最後，會呼叫 [JetEndExternalBackup](./jetendexternalbackup-function.md)來結束備份。</span><span class="sxs-lookup"><span data-stu-id="f4c78-184">Finally, the backup is ended by a call to [JetEndExternalBackup](./jetendexternalbackup-function.md).</span></span>

<span data-ttu-id="f4c78-185">您也可以修改這組步驟，以執行實例的增量備份。</span><span class="sxs-lookup"><span data-stu-id="f4c78-185">It is also possible to modify this set of steps to perform an incremental backup of the instance.</span></span> <span data-ttu-id="f4c78-186">增量備份會列舉和備份記錄檔。</span><span class="sxs-lookup"><span data-stu-id="f4c78-186">An incremental backup enumerates and backs up log files.</span></span> <span data-ttu-id="f4c78-187">只有在未啟用迴圈記錄的情況下，才可以進行增量備份。</span><span class="sxs-lookup"><span data-stu-id="f4c78-187">Incremental backups are only possible if circular logging is not enabled.</span></span>

<span data-ttu-id="f4c78-188">您也可以修改這組步驟，以允許執行實例的後續差異備份。</span><span class="sxs-lookup"><span data-stu-id="f4c78-188">It is also possible to modify this set of steps to allow subsequent differential backups of the instance to be performed.</span></span> <span data-ttu-id="f4c78-189">若要執行差異備份，請勿在先前的完整或增量備份中呼叫 [JetTruncateLog](./jettruncatelog-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="f4c78-189">To perform a differential backup, do not call [JetTruncateLog](./jettruncatelog-function.md) in the previous full or incremental backup.</span></span> <span data-ttu-id="f4c78-190">藉由不呼叫 [JetTruncateLog](./jettruncatelog-function.md)，您可以讓後續的備份與最後一個完整或增量備份有關。</span><span class="sxs-lookup"><span data-stu-id="f4c78-190">By not calling [JetTruncateLog](./jettruncatelog-function.md), you enable subsequent backups to be differential with respect to the last full or incremental backup.</span></span> <span data-ttu-id="f4c78-191">只有在未啟用迴圈記錄的情況下，才可以進行差異備份。</span><span class="sxs-lookup"><span data-stu-id="f4c78-191">Differential backups are only possible if circular logging is not enabled.</span></span>

<span data-ttu-id="f4c78-192">資料庫修補檔是特殊的輔助檔案，用於在備份期間于特定情況下儲存資料庫頁面映射。</span><span class="sxs-lookup"><span data-stu-id="f4c78-192">The database patch file is a special auxiliary file that is used to store database page images under certain circumstances during the backup.</span></span> <span data-ttu-id="f4c78-193">在還原作業期間，此檔案必須存在於與其相關聯資料庫相同的位置。</span><span class="sxs-lookup"><span data-stu-id="f4c78-193">This file must be present in the same location as its associated database during a restore operation.</span></span> <span data-ttu-id="f4c78-194">這個檔案只會在 Windows 2000 中使用。</span><span class="sxs-lookup"><span data-stu-id="f4c78-194">This file is only used in Windows 2000.</span></span> <span data-ttu-id="f4c78-195">因此，任何針對 Windows 2000 和其他版本所撰寫的應用程式都必須支援資料庫修補檔案（如果存在的話），但如果不存在，也不能失敗。</span><span class="sxs-lookup"><span data-stu-id="f4c78-195">As a result, any application that is written to work against Windows 2000 and other releases must support database patch files, if they are present, but also must not fail if they are not present.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f4c78-196">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4c78-196">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4c78-197"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="f4c78-197"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f4c78-198">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="f4c78-198">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4c78-199"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="f4c78-199"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f4c78-200">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="f4c78-200">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4c78-201"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="f4c78-201"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f4c78-202">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="f4c78-202">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4c78-203"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="f4c78-203"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f4c78-204">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="f4c78-204">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4c78-205"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f4c78-205"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f4c78-206">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="f4c78-206">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f4c78-207">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4c78-207">See Also</span></span>

[<span data-ttu-id="f4c78-208">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f4c78-208">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f4c78-209">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="f4c78-209">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="f4c78-210">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="f4c78-210">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="f4c78-211">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="f4c78-211">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="f4c78-212">JetBeginExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="f4c78-212">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="f4c78-213">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="f4c78-213">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="f4c78-214">JetEndExternalBackup</span><span class="sxs-lookup"><span data-stu-id="f4c78-214">JetEndExternalBackup</span></span>](./jetendexternalbackup-function.md)  
[<span data-ttu-id="f4c78-215">JetEndExternalBackupInstance2</span><span class="sxs-lookup"><span data-stu-id="f4c78-215">JetEndExternalBackupInstance2</span></span>](./jetendexternalbackupinstance2-function.md)  
[<span data-ttu-id="f4c78-216">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="f4c78-216">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="f4c78-217">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="f4c78-217">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="f4c78-218">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="f4c78-218">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="f4c78-219">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="f4c78-219">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="f4c78-220">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="f4c78-220">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="f4c78-221">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="f4c78-221">JetTruncateLog</span></span>](./jettruncatelog-function.md)
