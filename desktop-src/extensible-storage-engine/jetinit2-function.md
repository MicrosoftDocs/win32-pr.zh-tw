---
description: 深入瞭解： JetInit2 函數
title: JetInit2 函式
TOCTitle: JetInit2 Function
ms:assetid: b5541429-6ce6-457b-88cf-673d267f6209
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294065(v=EXCHG.10)
ms:contentKeyID: 32765680
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit2
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 00cc3402567a7c1342e78d3c84a1d6cfca8ab4d8
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "103946284"
---
# <a name="jetinit2-function"></a><span data-ttu-id="34a21-103">JetInit2 函式</span><span class="sxs-lookup"><span data-stu-id="34a21-103">JetInit2 Function</span></span>


<span data-ttu-id="34a21-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="34a21-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetinit2-function"></a><span data-ttu-id="34a21-105">JetInit2 函式</span><span class="sxs-lookup"><span data-stu-id="34a21-105">JetInit2 Function</span></span>

<span data-ttu-id="34a21-106">**JetInit2** 函式會將資料庫引擎置於可支援資料庫檔案之應用程式使用的狀態。</span><span class="sxs-lookup"><span data-stu-id="34a21-106">The **JetInit2** function puts the database engine into a state where it can support application use of database files.</span></span> <span data-ttu-id="34a21-107">引擎必須已正確設定，才能使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md)進行初始化。</span><span class="sxs-lookup"><span data-stu-id="34a21-107">The engine must already be properly configured for initialization using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="34a21-108">資料庫損毀復原會在初始化過程中自動執行。</span><span class="sxs-lookup"><span data-stu-id="34a21-108">Database crash recovery is performed automatically as a part of the initialization process.</span></span>

<span data-ttu-id="34a21-109">**Windows xp：**  **JetInit2** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="34a21-109">**Windows XP:**  **JetInit2** is introduced in Windows XP.</span></span>

<span data-ttu-id="34a21-110">此函式已過時。</span><span class="sxs-lookup"><span data-stu-id="34a21-110">This function is obsolete.</span></span> <span data-ttu-id="34a21-111">請改用 [JetInit3](./jetinit3-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="34a21-111">Use [JetInit3](./jetinit3-function.md) instead.</span></span>

```cpp
JET_ERR JET_API JetInit2(
  __in_out_opt  JET_INSTANCE* pinstance,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="34a21-112">參數</span><span class="sxs-lookup"><span data-stu-id="34a21-112">Parameters</span></span>

<span data-ttu-id="34a21-113">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="34a21-113">*pinstance*</span></span>

<span data-ttu-id="34a21-114">此呼叫所要使用的實例。</span><span class="sxs-lookup"><span data-stu-id="34a21-114">The instance to use for this call.</span></span>

<span data-ttu-id="34a21-115">若為 Windows 2000，則會忽略此參數，且應一律為 Null。</span><span class="sxs-lookup"><span data-stu-id="34a21-115">For Windows 2000, this parameter is ignored and should always be NULL.</span></span>

<span data-ttu-id="34a21-116">若為 Windows XP 和更新版本，則使用這個參數取決於引擎的操作模式。</span><span class="sxs-lookup"><span data-stu-id="34a21-116">For Windows XP and later releases, the use of this parameter depends on the operating mode of the engine.</span></span> <span data-ttu-id="34a21-117">如果引擎是在舊版模式下運作 (Windows 2000 相容性模式) 只支援一個實例，此參數可能是 Null 或設定為包含 Null 或 JET_instanceNil 的有效輸出緩衝區，它會傳回做為初始化的副作用所建立的全域實例控制碼。</span><span class="sxs-lookup"><span data-stu-id="34a21-117">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, this parameter may either be NULL or it may be set to a valid output buffer containing NULL or JET_instanceNil which returns the global instance handle created as a side effect of the initialization.</span></span> <span data-ttu-id="34a21-118">然後，這個實例控制碼可以傳遞給任何其他接受實例的 API。</span><span class="sxs-lookup"><span data-stu-id="34a21-118">This instance handle can then be passed to any other API that takes an instance.</span></span> <span data-ttu-id="34a21-119">如果引擎是在多重實例模式中作業，這個參數必須設定為有效的輸入緩衝區，其中包含正在初始化的 [JetCreateInstance](./jetcreateinstance-function.md) 所傳回的實例控制碼。</span><span class="sxs-lookup"><span data-stu-id="34a21-119">If the engine is operating in multi-instance mode, this parameter must be set to a valid input buffer that contains the instance handle returned by the [JetCreateInstance](./jetcreateinstance-function.md) that is being initialized.</span></span>

<span data-ttu-id="34a21-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="34a21-120">*grbit*</span></span>

<span data-ttu-id="34a21-121">指定零或多個下列選項的位群組。</span><span class="sxs-lookup"><span data-stu-id="34a21-121">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="34a21-122">值</span><span class="sxs-lookup"><span data-stu-id="34a21-122">Value</span></span></p></th>
<th><p><span data-ttu-id="34a21-123">意義</span><span class="sxs-lookup"><span data-stu-id="34a21-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34a21-124">JET_bitReplayReplicatedLogFiles</span><span class="sxs-lookup"><span data-stu-id="34a21-124">JET_bitReplayReplicatedLogFiles</span></span></p></td>
<td><p><span data-ttu-id="34a21-125">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="34a21-125">Reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34a21-126">JET_bitCreateSFSVolumeIfNotExist</span><span class="sxs-lookup"><span data-stu-id="34a21-126">JET_bitCreateSFSVolumeIfNotExist</span></span></p></td>
<td><p><span data-ttu-id="34a21-127">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="34a21-127">Reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34a21-128">JET_bitReplayIgnoreMissingDB</span><span class="sxs-lookup"><span data-stu-id="34a21-128">JET_bitReplayIgnoreMissingDB</span></span></p></td>
<td><p><span data-ttu-id="34a21-129">此選項可讓使用者在一組記錄檔上執行復原，而不會有所有資料庫都在記錄集的某個點附加。</span><span class="sxs-lookup"><span data-stu-id="34a21-129">This option allows the user to run recovery on a set of log files, without all of the databases being present, that were attached at one point of the log set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34a21-130">JET_bitRecoveryWithoutUndo</span><span class="sxs-lookup"><span data-stu-id="34a21-130">JET_bitRecoveryWithoutUndo</span></span></p></td>
<td><p><span data-ttu-id="34a21-131">執行復原，但在恢復階段停止。</span><span class="sxs-lookup"><span data-stu-id="34a21-131">Perform recovery, but halt at the Undo phase.</span></span> <span data-ttu-id="34a21-132">這可讓您在中複製及套用其他交易記錄。</span><span class="sxs-lookup"><span data-stu-id="34a21-132">This allows additional transaction logs to copied in and applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34a21-133">JET_bitTruncateLogsAfterRecovery</span><span class="sxs-lookup"><span data-stu-id="34a21-133">JET_bitTruncateLogsAfterRecovery</span></span></p></td>
<td><p><span data-ttu-id="34a21-134">在成功的軟修復上，截斷記錄檔。</span><span class="sxs-lookup"><span data-stu-id="34a21-134">On successful soft recovery, truncate log files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34a21-135">JET_bitReplayMissingMapEntryDB</span><span class="sxs-lookup"><span data-stu-id="34a21-135">JET_bitReplayMissingMapEntryDB</span></span></p></td>
<td><p><span data-ttu-id="34a21-136">遺漏資料庫對應專案預設為相同的位置。</span><span class="sxs-lookup"><span data-stu-id="34a21-136">Missing database map entry default to same location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34a21-137">JET_bitReplayIgnoreLostLogs</span><span class="sxs-lookup"><span data-stu-id="34a21-137">JET_bitReplayIgnoreLostLogs</span></span></p></td>
<td><p><span data-ttu-id="34a21-138">略過記錄資料流程結尾遺失的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="34a21-138">Ignore logs lost from the end of the log stream.</span></span></p>
<p><span data-ttu-id="34a21-139"><strong>Windows 7： JET_bitReplayIgnoreLostLogs</strong> 是在 windows 7 中引進的。</span><span class="sxs-lookup"><span data-stu-id="34a21-139"><strong>Windows 7:JET_bitReplayIgnoreLostLogs</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="34a21-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="34a21-140">Return Value</span></span>

<span data-ttu-id="34a21-141">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="34a21-141">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="34a21-142">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="34a21-142">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>


#### <a name="remarks"></a><span data-ttu-id="34a21-143">備註</span><span class="sxs-lookup"><span data-stu-id="34a21-143">Remarks</span></span>

<span data-ttu-id="34a21-144">必須先使用 **JetInit2** 的呼叫來初始化實例，才能由 [JetSetSystemParameter](./jetsetsystemparameter-function.md)以外的任何人使用。</span><span class="sxs-lookup"><span data-stu-id="34a21-144">An instance must be initialized with a call to **JetInit2** before it can be used by anything other than [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="34a21-145">實例會透過呼叫 [JetTerm](./jetterm-function.md) 函式終結，即使該實例從未使用 [JetInit](./jetinit-function.md)初始化也是一樣。</span><span class="sxs-lookup"><span data-stu-id="34a21-145">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized using [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="34a21-146">實例是 database engine 的復原單位。</span><span class="sxs-lookup"><span data-stu-id="34a21-146">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="34a21-147">它會控制所有檔案的生命週期，用來保護一組資料庫檔案中資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="34a21-147">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="34a21-148">這些檔案包括檢查點檔案和交易記錄檔。</span><span class="sxs-lookup"><span data-stu-id="34a21-148">These files include the checkpoint file and the transaction log files.</span></span>

<span data-ttu-id="34a21-149">如果復原是在一組記錄檔上執行，但並非所有資料庫都存在 (這會在正常情況下傳回錯誤 JET_errAttachedDatabaseMismatch，而且用戶端希望復原在一般) 情況下仍繼續使用，而用戶端則會使用 JET_ bitReplayIgnoreMissingDB 來繼續復原可用的資料庫。</span><span class="sxs-lookup"><span data-stu-id="34a21-149">If recovery is running on a set of logs, for which not all databases is present (which will return the error JET_errAttachedDatabaseMismatch under normal circumstances), and the client wishes recovery to continue despite missing databases, the JET_ bitReplayIgnoreMissingDB is used to continue recovery for the available databases.</span></span>

<span data-ttu-id="34a21-150">如需詳細資訊，請參閱 [JetInit](./jetinit-function.md) 中的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="34a21-150">See the Remarks section in [JetInit](./jetinit-function.md) for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="34a21-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="34a21-151">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34a21-152"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="34a21-152"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="34a21-153">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="34a21-153">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34a21-154"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="34a21-154"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="34a21-155">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="34a21-155">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34a21-156"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="34a21-156"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="34a21-157">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="34a21-157">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34a21-158"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="34a21-158"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="34a21-159">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="34a21-159">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34a21-160"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="34a21-160"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="34a21-161">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="34a21-161">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="34a21-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="34a21-162">See Also</span></span>

[<span data-ttu-id="34a21-163">可擴充儲存引擎檔案</span><span class="sxs-lookup"><span data-stu-id="34a21-163">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="34a21-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="34a21-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="34a21-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="34a21-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="34a21-166">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="34a21-166">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="34a21-167">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="34a21-167">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="34a21-168">JetInit</span><span class="sxs-lookup"><span data-stu-id="34a21-168">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="34a21-169">JetInit3</span><span class="sxs-lookup"><span data-stu-id="34a21-169">JetInit3</span></span>](./jetinit3-function.md)  
[<span data-ttu-id="34a21-170">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="34a21-170">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="34a21-171">資源參數</span><span class="sxs-lookup"><span data-stu-id="34a21-171">Resource Parameters</span></span>](./resource-parameters.md)
