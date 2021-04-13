---
description: 深入瞭解： JetInit3 函數
title: JetInit3 函式
TOCTitle: JetInit3 Function
ms:assetid: 752589b6-1b8f-4b6f-a14a-00f4b1405db5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269296(v=EXCHG.10)
ms:contentKeyID: 32765588
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit3
- JetInit3A
- JetInit3W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c96171920b7538e71e822eaf0879e476fb2fd31e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321144"
---
# <a name="jetinit3-function"></a><span data-ttu-id="fe0ae-103">JetInit3 函式</span><span class="sxs-lookup"><span data-stu-id="fe0ae-103">JetInit3 Function</span></span>


<span data-ttu-id="fe0ae-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="fe0ae-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetinit3-function"></a><span data-ttu-id="fe0ae-105">JetInit3 函式</span><span class="sxs-lookup"><span data-stu-id="fe0ae-105">JetInit3 Function</span></span>

<span data-ttu-id="fe0ae-106">**JetInit3** 函式會將資料庫引擎置於可支援資料庫檔案應用程式使用的狀態。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-106">The **JetInit3** function puts the database engine into a state in which it can support application use of database files.</span></span> <span data-ttu-id="fe0ae-107">引擎必須已正確設定初始化，您可以使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 函數完成此操作。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-107">The engine must already be properly configured for initialization, which you accomplish by using the [JetSetSystemParameter](./jetsetsystemparameter-function.md) function.</span></span> <span data-ttu-id="fe0ae-108">請注意，資料庫損毀復原會在初始化過程中自動進行。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-108">Note that database crash recovery occurs automatically as a part of the initialization process.</span></span>

<span data-ttu-id="fe0ae-109">**Windows vista：**  **JetInit3** 是在 windows vista 中引進的。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-109">**Windows Vista:**  **JetInit3** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetInit3(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in_opt      JET_RSTINFO* prstInfo,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="fe0ae-110">參數</span><span class="sxs-lookup"><span data-stu-id="fe0ae-110">Parameters</span></span>

<span data-ttu-id="fe0ae-111">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="fe0ae-111">*pinstance*</span></span>

<span data-ttu-id="fe0ae-112">用於特定呼叫的實例。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-112">The instance that you use for a particular call.</span></span> <span data-ttu-id="fe0ae-113">此參數的使用取決於引擎的操作模式。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-113">The use of this parameter depends on the operating mode of the engine.</span></span> <span data-ttu-id="fe0ae-114">如果引擎是在舊版模式下運作 (Windows 2000 相容性模式) ，其中只支援一個實例，您可以將此參數設定為 **null** 或包含 **null** 或 JET_instanceNil 的有效輸出緩衝區，這會傳回建立為初始化副作用的全域實例控制碼。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-114">If the engine is operating in legacy mode (Windows 2000 compatibility mode), in which only one instance is supported, you can set this parameter either to **NULL** or to a valid output buffer containing either **NULL** or JET_instanceNil, which returns the global instance handle created as a side-effect of the initialization.</span></span> <span data-ttu-id="fe0ae-115">然後，這個實例控制碼可以傳遞給任何其他接受實例的 API。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-115">This instance handle can then be passed to any other API that takes an instance.</span></span> <span data-ttu-id="fe0ae-116">如果引擎是在多重實例模式中作業，您必須將此參數設定為有效的輸入緩衝區，其中包含正在初始化的 [JetCreateInstance](./jetcreateinstance-function.md) 函數所傳回的實例控制碼。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-116">If the engine is operating in multi-instance mode, you must set this parameter to a valid input buffer that contains the instance handle returned by the [JetCreateInstance](./jetcreateinstance-function.md) function that is being initialized.</span></span>

<span data-ttu-id="fe0ae-117">*prstInfo*</span><span class="sxs-lookup"><span data-stu-id="fe0ae-117">*prstInfo*</span></span>

<span data-ttu-id="fe0ae-118">在復原期間用來重新對應資料庫的其他修復參數，用於設定復原將停止的位置，或用來判斷目前的復原狀態。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-118">Additional recovery parameters used for remapping databases during recovery, for setting the position where recovery will stop, or for determining the current recovery status.</span></span>

<span data-ttu-id="fe0ae-119">*grbit*</span><span class="sxs-lookup"><span data-stu-id="fe0ae-119">*grbit*</span></span>

<span data-ttu-id="fe0ae-120">一組位，指定下表所列和定義的零或多個選項。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-120">A group of bits that specifies zero or more of the options listed and defined in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fe0ae-121">值</span><span class="sxs-lookup"><span data-stu-id="fe0ae-121">Value</span></span></p></th>
<th><p><span data-ttu-id="fe0ae-122">意義</span><span class="sxs-lookup"><span data-stu-id="fe0ae-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe0ae-123">JET_bitReplayReplicatedLogFiles</span><span class="sxs-lookup"><span data-stu-id="fe0ae-123">JET_bitReplayReplicatedLogFiles</span></span></p></td>
<td><p><span data-ttu-id="fe0ae-124">這個值已保留供未來使用</span><span class="sxs-lookup"><span data-stu-id="fe0ae-124">This value is reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe0ae-125">JET_bitCreateSFSVolumeIfNotExist</span><span class="sxs-lookup"><span data-stu-id="fe0ae-125">JET_bitCreateSFSVolumeIfNotExist</span></span></p></td>
<td><p><span data-ttu-id="fe0ae-126">這個值已保留供未來使用</span><span class="sxs-lookup"><span data-stu-id="fe0ae-126">This value is reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe0ae-127">JET_bitReplayIgnoreMissingDB</span><span class="sxs-lookup"><span data-stu-id="fe0ae-127">JET_bitReplayIgnoreMissingDB</span></span></p></td>
<td><p><span data-ttu-id="fe0ae-128">此值可讓使用者在一組記錄檔上執行復原，即使在某個時間點沒有附加至記錄檔的資料庫也一樣。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-128">This value enables the user to run recovery on a set of log files, even in the absence of the databases that were attached to the log file set at some point.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe0ae-129">JET_bitRecoveryWithoutUndo</span><span class="sxs-lookup"><span data-stu-id="fe0ae-129">JET_bitRecoveryWithoutUndo</span></span></p></td>
<td><p><span data-ttu-id="fe0ae-130">此值可讓使用者執行復原，但最多隻能 (且不包括) 的復原階段。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-130">This value enables the user to perform recovery, but only up to (and not including) the Undo phase.</span></span> <span data-ttu-id="fe0ae-131">使用這個值，可以在中複製及套用其他交易記錄。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-131">Using this value, additional transaction logs can be copied in and applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe0ae-132">JET_bitTruncateLogsAfterRecovery</span><span class="sxs-lookup"><span data-stu-id="fe0ae-132">JET_bitTruncateLogsAfterRecovery</span></span></p></td>
<td><p><span data-ttu-id="fe0ae-133">此值會在成功的軟復原期間，讓記錄檔被截斷。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-133">This value causes log files to be truncated during a successful soft recovery.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe0ae-134">JET_bitReplayMissingMapEntryDB</span><span class="sxs-lookup"><span data-stu-id="fe0ae-134">JET_bitReplayMissingMapEntryDB</span></span></p></td>
<td><p><span data-ttu-id="fe0ae-135">此值會導致遺失的資料庫對應專案預設為相同的位置。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-135">This value causes a missing database map entry to default to the same location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe0ae-136">JET_bitReplayIgnoreLostLogs</span><span class="sxs-lookup"><span data-stu-id="fe0ae-136">JET_bitReplayIgnoreLostLogs</span></span></p></td>
<td><p><span data-ttu-id="fe0ae-137">此值會導致復原期間遺失記錄資料流程結尾的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-137">This value causes logs lost from the end of the log stream to be ignored during a recovery.</span></span></p>
<p><span data-ttu-id="fe0ae-138"><strong>Windows 7： JET_bitReplayIgnoreLostLogs</strong> 是在 windows 7 中引進的。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-138"><strong>Windows 7:JET_bitReplayIgnoreLostLogs</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="fe0ae-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe0ae-139">Return Value</span></span>

<span data-ttu-id="fe0ae-140">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-140">This function returns the [JET_ERR](./jet-err.md) data type with one of the following return codes.</span></span> <span data-ttu-id="fe0ae-141">如需可能的可延伸儲存引擎 (ESE) 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-141">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>


#### <a name="remarks"></a><span data-ttu-id="fe0ae-142">備註</span><span class="sxs-lookup"><span data-stu-id="fe0ae-142">Remarks</span></span>

<span data-ttu-id="fe0ae-143">您必須使用 **JetInit3** 函式的呼叫來初始化實例，才能將其用於 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 函數以外的任何其他作業。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-143">An instance must be initialized with a call to the **JetInit3** function before it can be used by anything other than the [JetSetSystemParameter](./jetsetsystemparameter-function.md) function.</span></span>

<span data-ttu-id="fe0ae-144">實例會透過呼叫 [JetTerm](./jetterm-function.md) 函式終結，即使該實例從未使用 [JetInit](./jetinit-function.md) 函數初始化也是一樣。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-144">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized by using the [JetInit](./jetinit-function.md) function.</span></span> <span data-ttu-id="fe0ae-145">實例是 database engine 的復原單位。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-145">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="fe0ae-146">它會控制所有檔案的生命週期，用來保護一組資料庫檔案中資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-146">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="fe0ae-147">這些檔案包括檢查點檔案和交易記錄檔。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-147">These files include the checkpoint file and the transaction log files.</span></span> <span data-ttu-id="fe0ae-148">請注意，如果 **JetInit3** 函式失敗，則不應呼叫 [JetTerm](./jetterm-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-148">Note that [JetTerm](./jetterm-function.md) should not be called if the **JetInit3** function fails.</span></span> <span data-ttu-id="fe0ae-149">但是，如果從未呼叫 **JetInit3** 或 **JetInit3** 成功， **JetCreateInstance2** 建立的所有實例仍應呼叫 [JetTerm](./jetterm-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-149">However, [JetTerm](./jetterm-function.md) should still be called for all instances created by **JetCreateInstance2** if **JetInit3** was never called or if **JetInit3** succeeds.</span></span>

<span data-ttu-id="fe0ae-150">如果復原是在一組不是所有相關資料庫的記錄中執行 (這會在正常情況下傳回錯誤 JET_errAttachedDatabaseMismatch，而用戶端想要在遺失資料庫的) 情況下，讓用戶端繼續復原，則會使用 JET_bitReplayIgnoreMissingDB 錯誤來繼續復原可用的資料庫。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-150">If recovery is running on a set of logs for which not all of the related databases are present (which will return the error JET_errAttachedDatabaseMismatch under normal circumstances), and the client wants recovery to continue despite the missing databases, the JET_bitReplayIgnoreMissingDB error is used to continue recovery for the available databases.</span></span>

<span data-ttu-id="fe0ae-151">因為損毀復原通常不會發生在同一部電腦上 (而且具有與當機時相同的設定) ，所以資料庫通常不會變更位置。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-151">Because crash recovery doesn't usually happen on the same machine (and with the same configuration) as at the time of the crash, a database typically doesn't change location.</span></span> <span data-ttu-id="fe0ae-152">在某些情況下，例如將檔案移至不同的電腦，或將快照集備份還原到不同的位置，這已不再成立。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-152">In certain scenarios, such as moving files to a different machine or restoring snapshot backup to different locations, this is no longer true.</span></span> <span data-ttu-id="fe0ae-153">**JetInit3** 函式可讓您指定對應 (使用 [JET_RSTINFO](./jet-rstinfo-structure.md) ，以及在舊的資料庫位置與新位置之間) [JET_RSTMAP](./jet-rstmap-structure.md)結構。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-153">The **JetInit3** function enables you to specify a mapping (using the [JET_RSTINFO](./jet-rstinfo-structure.md) and [JET_RSTMAP](./jet-rstmap-structure.md) structures) between the old database location and its new location.</span></span> <span data-ttu-id="fe0ae-154">事實上，只要資料庫檔案存在於該位置，您就只需要新的位置。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-154">In fact, you need only the new location as long as the database files are present at that location.</span></span> <span data-ttu-id="fe0ae-155">一旦您知道已還原資料庫的位置，資料庫簽章將用來透過還原程式來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-155">As soon as you know the locations of the restored databases, the database signature will be used to identify the database through the restore process.</span></span> <span data-ttu-id="fe0ae-156">只有當您需要重新建立資料庫時，才需要使用原始的資料庫位置，此時就會知道簽章。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-156">You'll need the original database location only if you need to re-create a database, in which case the signature is known.</span></span>

<span data-ttu-id="fe0ae-157">此外，如果您需要在復原作業之後停止復原，則可以指定復原將停止的特定記錄檔位置。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-157">In addition, if you need to stop a recovery after an Undo operation, you can specify a particular log position at which recovery will stop.</span></span> <span data-ttu-id="fe0ae-158">請注意，如果指定的位置是產生的一部分，但超過實際記錄檔的結尾，則這包括在特定記錄產生的結尾處停止的功能。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-158">Note that this includes the ability to stop at the end of a particular log generation if the specified position is part of the generation but past the end of the actual log.</span></span>

<span data-ttu-id="fe0ae-159">如需詳細資訊，請參閱 [JetInit](./jetinit-function.md) 主題中的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-159">For more information, see the "Remarks" section in the [JetInit](./jetinit-function.md) topic.</span></span>

#### <a name="requirements"></a><span data-ttu-id="fe0ae-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe0ae-160">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe0ae-161">用戶端</span><span class="sxs-lookup"><span data-stu-id="fe0ae-161">Client</span></span></p></td>
<td><p><span data-ttu-id="fe0ae-162">需要 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-162">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe0ae-163">伺服器</span><span class="sxs-lookup"><span data-stu-id="fe0ae-163">Server</span></span></p></td>
<td><p><span data-ttu-id="fe0ae-164">需要 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-164">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe0ae-165">標頭</span><span class="sxs-lookup"><span data-stu-id="fe0ae-165">Header</span></span></p></td>
<td><p><span data-ttu-id="fe0ae-166">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-166">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe0ae-167">程式庫</span><span class="sxs-lookup"><span data-stu-id="fe0ae-167">Library</span></span></p></td>
<td><p><span data-ttu-id="fe0ae-168">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-168">Uses ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe0ae-169">DLL</span><span class="sxs-lookup"><span data-stu-id="fe0ae-169">DLL</span></span></p></td>
<td><p><span data-ttu-id="fe0ae-170">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-170">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe0ae-171">Unicode</span><span class="sxs-lookup"><span data-stu-id="fe0ae-171">Unicode</span></span></p></td>
<td><p><span data-ttu-id="fe0ae-172">實作為 <strong>JetInit3W</strong> (Unicode) 和 <strong>JetInit3A</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="fe0ae-172">Implemented as <strong>JetInit3W</strong> (Unicode) and <strong>JetInit3A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="fe0ae-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe0ae-173">See Also</span></span>

[<span data-ttu-id="fe0ae-174">可擴充儲存引擎檔案</span><span class="sxs-lookup"><span data-stu-id="fe0ae-174">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="fe0ae-175">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="fe0ae-175">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="fe0ae-176">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="fe0ae-176">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="fe0ae-177">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="fe0ae-177">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="fe0ae-178">JET_RSTINFO</span><span class="sxs-lookup"><span data-stu-id="fe0ae-178">JET_RSTINFO</span></span>](./jet-rstinfo-structure.md)  
[<span data-ttu-id="fe0ae-179">JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="fe0ae-179">JET_RSTMAP</span></span>](./jet-rstmap-structure.md)  
[<span data-ttu-id="fe0ae-180">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="fe0ae-180">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="fe0ae-181">JetInit</span><span class="sxs-lookup"><span data-stu-id="fe0ae-181">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="fe0ae-182">JetInit2</span><span class="sxs-lookup"><span data-stu-id="fe0ae-182">JetInit2</span></span>](./jetinit2-function.md)  
[<span data-ttu-id="fe0ae-183">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="fe0ae-183">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="fe0ae-184">資源參數</span><span class="sxs-lookup"><span data-stu-id="fe0ae-184">Resource Parameters</span></span>](./resource-parameters.md)
