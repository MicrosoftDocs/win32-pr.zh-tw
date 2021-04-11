---
description: 深入瞭解： JetTerm2 函數
title: JetTerm2 函式
TOCTitle: JetTerm2 Function
ms:assetid: 36464e24-1cc0-4cda-9d7a-f64555c622bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269223(v=EXCHG.10)
ms:contentKeyID: 32765525
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dc8b0c768e981b88e8759c30d349caa8e5575a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113601"
---
# <a name="jetterm2-function"></a><span data-ttu-id="20b32-103">JetTerm2 函式</span><span class="sxs-lookup"><span data-stu-id="20b32-103">JetTerm2 Function</span></span>


<span data-ttu-id="20b32-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="20b32-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetterm2-function"></a><span data-ttu-id="20b32-105">JetTerm2 函式</span><span class="sxs-lookup"><span data-stu-id="20b32-105">JetTerm2 Function</span></span>

<span data-ttu-id="20b32-106">**JetTerm2** 函式會起始由 [JetInit](./jetinit-function.md)初始化之實例的關機。</span><span class="sxs-lookup"><span data-stu-id="20b32-106">The **JetTerm2** function initiates the shutdown of an instance that has been initialized by [JetInit](./jetinit-function.md).</span></span>

<span data-ttu-id="20b32-107">**JetTerm2** 也可以終結由 [JetCreateInstance](./jetcreateinstance-function.md)所建立的未初始化實例。</span><span class="sxs-lookup"><span data-stu-id="20b32-107">**JetTerm2** can also destroy an uninitialized instance that was created by [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

```cpp
    JET_ERR JET_API JetTerm2(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="20b32-108">參數</span><span class="sxs-lookup"><span data-stu-id="20b32-108">Parameters</span></span>

<span data-ttu-id="20b32-109">*實例*</span><span class="sxs-lookup"><span data-stu-id="20b32-109">*instance*</span></span>

<span data-ttu-id="20b32-110">此呼叫所要使用的實例。</span><span class="sxs-lookup"><span data-stu-id="20b32-110">The instance to use for this call.</span></span>

<span data-ttu-id="20b32-111">**Windows 2000：**  此參數會被忽略，且應一律為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="20b32-111">**Windows 2000:**  This parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="20b32-112">**WINDOWS XP 和更新版本：**  此參數已多載。</span><span class="sxs-lookup"><span data-stu-id="20b32-112">**Windows XP and later releases:**  This parameter is overloaded.</span></span> <span data-ttu-id="20b32-113">如果引擎在舊版模式下運作 (Windows 2000 相容性模式) 只支援一個實例，此參數可能是 **Null** 或包含 [JetInit](./jetinit-function.md)所傳回的實際實例。</span><span class="sxs-lookup"><span data-stu-id="20b32-113">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, then this parameter might be **NULL** or might contain the actual instance that is returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="20b32-114">如果引擎以多重實例模式運作，則此參數必須是使用 [JetCreateInstance](./jetcreateinstance-function.md)建立之實例的指標。</span><span class="sxs-lookup"><span data-stu-id="20b32-114">If the engine is operating in multi-instance mode, then this parameter must be a pointer to an instance that was created using [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

<span data-ttu-id="20b32-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="20b32-115">*grbit*</span></span>

<span data-ttu-id="20b32-116">位群組，其中包含要用於此呼叫的選項，其中包含零或多個下列值。</span><span class="sxs-lookup"><span data-stu-id="20b32-116">A group of bits that contain the options to be used for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="20b32-117">值</span><span class="sxs-lookup"><span data-stu-id="20b32-117">Value</span></span></p></th>
<th><p><span data-ttu-id="20b32-118">意義</span><span class="sxs-lookup"><span data-stu-id="20b32-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20b32-119">JET_bitTermComplete</span><span class="sxs-lookup"><span data-stu-id="20b32-119">JET_bitTermComplete</span></span></p></td>
<td><p><span data-ttu-id="20b32-120">要求完全關閉實例。</span><span class="sxs-lookup"><span data-stu-id="20b32-120">Requests that the instance be shut down cleanly.</span></span> <span data-ttu-id="20b32-121">通常會在執行時間于背景中完成的任何選擇性清除工作會立即完成。</span><span class="sxs-lookup"><span data-stu-id="20b32-121">Any optional cleanup work that would ordinarily be done in the background at run time is completed immediately.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20b32-122">JET_bitTermAbrupt</span><span class="sxs-lookup"><span data-stu-id="20b32-122">JET_bitTermAbrupt</span></span></p></td>
<td><p><span data-ttu-id="20b32-123">要求實例盡可能快速關閉。</span><span class="sxs-lookup"><span data-stu-id="20b32-123">Requests that the instance be shut down as quickly as possible.</span></span> <span data-ttu-id="20b32-124">在執行時間，通常會在背景中完成的任何選擇性工作都會被放棄。</span><span class="sxs-lookup"><span data-stu-id="20b32-124">Any optional work that would ordinarily be done in the background at run time is abandoned.</span></span></p>
<p><span data-ttu-id="20b32-125"><strong>注意</strong>  此選項可能會在資料庫中造成暫存或永久的空間遺失。</span><span class="sxs-lookup"><span data-stu-id="20b32-125"><strong>Note</strong>  This option can cause temporary or permanent space loss in the database.</span></span> <span data-ttu-id="20b32-126">這個遺失的空間隨時都可以透過資料庫的離線磁碟重組來復原。</span><span class="sxs-lookup"><span data-stu-id="20b32-126">This lost space can always be recovered through an offline defragmentation of the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20b32-127">JET_bitTermStopBackup</span><span class="sxs-lookup"><span data-stu-id="20b32-127">JET_bitTermStopBackup</span></span></p></td>
<td><p><span data-ttu-id="20b32-128">要求即使目前正在進行備份，也會關閉實例。</span><span class="sxs-lookup"><span data-stu-id="20b32-128">Requests that the instance be shut down even if there is currently a backup in progress.</span></span> <span data-ttu-id="20b32-129">一般來說，暫止的備份會導致 <a href="gg269298(v=exchg.10).md">JetTerm</a> 失敗，並 JET_errBackupInProgress。</span><span class="sxs-lookup"><span data-stu-id="20b32-129">Ordinarily, a pending backup would cause <a href="gg269298(v=exchg.10).md">JetTerm</a> to fail with JET_errBackupInProgress.</span></span> <span data-ttu-id="20b32-130">如果這個參數不存在，則會假設其值為 JET_bitTermAbrupt。</span><span class="sxs-lookup"><span data-stu-id="20b32-130">When this parameter is not present, its value is presumed to be JET_bitTermAbrupt.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20b32-131">JET_bitTermDirty</span><span class="sxs-lookup"><span data-stu-id="20b32-131">JET_bitTermDirty</span></span></p></td>
<td><p><span data-ttu-id="20b32-132">要求將所有附加的資料庫都保持在中途狀態時，關閉實例。</span><span class="sxs-lookup"><span data-stu-id="20b32-132">Requests that the instance be shut down with all the attached databases left in a dirty state.</span></span></p>
<p><span data-ttu-id="20b32-133">Windows 7： JET_bitTermDirty 是在 Windows 7 中引進的。</span><span class="sxs-lookup"><span data-stu-id="20b32-133">Windows 7: JET_bitTermDirty is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="20b32-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="20b32-134">Return Value</span></span>

<span data-ttu-id="20b32-135">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="20b32-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="20b32-136">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="20b32-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="20b32-137">傳回碼</span><span class="sxs-lookup"><span data-stu-id="20b32-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="20b32-138">Description</span><span class="sxs-lookup"><span data-stu-id="20b32-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20b32-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="20b32-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="20b32-140">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="20b32-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20b32-141">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="20b32-141">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="20b32-142">作業無法完成，因為實例上的備份作業正在進行中。</span><span class="sxs-lookup"><span data-stu-id="20b32-142">The operation cannot complete because a backup operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20b32-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="20b32-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="20b32-144">提供的其中一個參數包含未預期的值，或數個參數的組合產生了非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="20b32-144">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="20b32-145">當引擎處於多重實例模式時，以及<em>pinstance</em>參考不正確實例時， <a href="gg269298(v=exchg.10).md">JetTerm</a>會傳回這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="20b32-145">This error will be returned by <a href="gg269298(v=exchg.10).md">JetTerm</a> when the engine is in multi-instance mode and when <em>pinstance</em> refers to an invalid instance.</span></span></p>
<p><span data-ttu-id="20b32-146"><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="20b32-146"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20b32-147">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="20b32-147">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="20b32-148">無法完成作業，因為尚未初始化實例。</span><span class="sxs-lookup"><span data-stu-id="20b32-148">The operation cannot complete because the instance has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20b32-149">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="20b32-149">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="20b32-150">無法完成操作，因為正在關閉實例。</span><span class="sxs-lookup"><span data-stu-id="20b32-150">The operation cannot complete because the instance is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20b32-151">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="20b32-151">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="20b32-152">無法完成作業，因為實例上的還原作業正在進行中。</span><span class="sxs-lookup"><span data-stu-id="20b32-152">It is not possible to complete the operation because a restore operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20b32-153">JET_errTooManyActiveUsers</span><span class="sxs-lookup"><span data-stu-id="20b32-153">JET_errTooManyActiveUsers</span></span></p></td>
<td><p><span data-ttu-id="20b32-154">因為目前的會話具有指定實例的使用中交易，所以無法關閉實例。</span><span class="sxs-lookup"><span data-stu-id="20b32-154">The instance cannot be shut down because there are currently sessions with active transactions for the specified instance.</span></span> <span data-ttu-id="20b32-155">只有使用 JET_bitTermComplete 時，才會發生此錯誤。</span><span class="sxs-lookup"><span data-stu-id="20b32-155">This error occurs only if the JET_bitTermComplete is used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="20b32-156">如果此函數成功，將會關閉指定的實例。</span><span class="sxs-lookup"><span data-stu-id="20b32-156">If this function succeeds, the specified instance will be shut down.</span></span> <span data-ttu-id="20b32-157">實例控制碼也將會關閉，並且可供任何採用實例控制碼的 API 使用。</span><span class="sxs-lookup"><span data-stu-id="20b32-157">The instance handle will also be closed and made unavailable to any API that takes an instance handle.</span></span> <span data-ttu-id="20b32-158">與實例相關聯的所有其他物件（例如會話）也會關閉。</span><span class="sxs-lookup"><span data-stu-id="20b32-158">All other objects that are associated with the instance, such as sessions, will also be closed.</span></span> <span data-ttu-id="20b32-159">檢查點檔案、交易記錄檔和附加至實例的資料庫檔案的狀態，會在關閉程式期間進行修改。</span><span class="sxs-lookup"><span data-stu-id="20b32-159">The state of the checkpoint file, transaction log files, and the database files attached to the instance will be modified during the shutdown process.</span></span>

<span data-ttu-id="20b32-160">如果此函式因使用錯誤而失敗，則實例會維持在初始化狀態，而且不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="20b32-160">If this function fails as a result of a usage error, then the instance remains in an initialized state and nothing changes.</span></span> <span data-ttu-id="20b32-161">否則，實例仍會依照成功案例的規定關閉。</span><span class="sxs-lookup"><span data-stu-id="20b32-161">Otherwise, the instance is still shut down as stated for the success case.</span></span> <span data-ttu-id="20b32-162">不同之處在于實例在下次初始化時，必須經歷損毀復原。</span><span class="sxs-lookup"><span data-stu-id="20b32-162">The difference is that the instance will need to go through crash recovery when it is next initialized.</span></span> <span data-ttu-id="20b32-163">引擎會嘗試盡可能將最多的資料排清，以將所需的復原量降至最低。</span><span class="sxs-lookup"><span data-stu-id="20b32-163">The engine will try to flush as much data as possible to minimize the amount of recovery that is required.</span></span> <span data-ttu-id="20b32-164">就概念而言， [JetTerm](./jetterm-function.md) 失敗與進程損毀並無不同。</span><span class="sxs-lookup"><span data-stu-id="20b32-164">Conceptually, such a failure of [JetTerm](./jetterm-function.md) is no different than a process crash.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20b32-165">備註</span><span class="sxs-lookup"><span data-stu-id="20b32-165">Remarks</span></span>

<span data-ttu-id="20b32-166">請參閱 [JetTerm](./jetterm-function.md)。</span><span class="sxs-lookup"><span data-stu-id="20b32-166">See [JetTerm](./jetterm-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="20b32-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="20b32-167">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20b32-168"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="20b32-168"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="20b32-169">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="20b32-169">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20b32-170"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="20b32-170"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="20b32-171">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="20b32-171">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20b32-172"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="20b32-172"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="20b32-173">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="20b32-173">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20b32-174"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="20b32-174"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="20b32-175">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="20b32-175">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20b32-176"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="20b32-176"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="20b32-177">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="20b32-177">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="20b32-178">另請參閱</span><span class="sxs-lookup"><span data-stu-id="20b32-178">See Also</span></span>

[<span data-ttu-id="20b32-179">可擴充儲存引擎檔案</span><span class="sxs-lookup"><span data-stu-id="20b32-179">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="20b32-180">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="20b32-180">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="20b32-181">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="20b32-181">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="20b32-182">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="20b32-182">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="20b32-183">JetInit</span><span class="sxs-lookup"><span data-stu-id="20b32-183">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="20b32-184">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="20b32-184">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="20b32-185">JetTerm</span><span class="sxs-lookup"><span data-stu-id="20b32-185">JetTerm</span></span>](./jetterm-function.md)
