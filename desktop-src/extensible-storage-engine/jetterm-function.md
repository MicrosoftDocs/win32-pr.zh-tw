---
description: 深入瞭解： JetTerm 函數
title: JetTerm 函式
TOCTitle: JetTerm Function
ms:assetid: 7711c960-98f4-4134-b8ae-8ddf7b26b6b0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269298(v=EXCHG.10)
ms:contentKeyID: 32765590
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6ce78ea12dfa61265a12b3858cc1e859adcae6e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972184"
---
# <a name="jetterm-function"></a><span data-ttu-id="b7c0b-103">JetTerm 函式</span><span class="sxs-lookup"><span data-stu-id="b7c0b-103">JetTerm Function</span></span>


<span data-ttu-id="b7c0b-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b7c0b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetterm-function"></a><span data-ttu-id="b7c0b-105">JetTerm 函式</span><span class="sxs-lookup"><span data-stu-id="b7c0b-105">JetTerm Function</span></span>

<span data-ttu-id="b7c0b-106">**JetTerm** 函式會起始由 [JetInit](./jetinit-function.md)初始化之實例的關機。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-106">The **JetTerm** function initiates the shutdown of an instance that has been initialized by [JetInit](./jetinit-function.md).</span></span>

<span data-ttu-id="b7c0b-107">**JetTerm** 也可用來終結 [JetCreateInstance](./jetcreateinstance-function.md)所建立的未初始化實例。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-107">**JetTerm** can also be used to destroy an uninitialized instance that was created by [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

```cpp
    JET_ERR JET_API JetTerm(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="b7c0b-108">參數</span><span class="sxs-lookup"><span data-stu-id="b7c0b-108">Parameters</span></span>

<span data-ttu-id="b7c0b-109">*實例*</span><span class="sxs-lookup"><span data-stu-id="b7c0b-109">*instance*</span></span>

<span data-ttu-id="b7c0b-110">指定要用於此呼叫的實例。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-110">Specifies the instance to use for this call.</span></span>

<span data-ttu-id="b7c0b-111">**Windows 2000：**  此參數會被忽略，且應一律為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-111">**Windows 2000:**  This parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="b7c0b-112">**WINDOWS XP 和更新版本：**  此參數已多載。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-112">**Windows XP and later releases:**  This parameter is overloaded.</span></span> <span data-ttu-id="b7c0b-113">如果引擎在舊版模式下運作 (Windows 2000 相容性模式) 只支援一個實例，此參數可能是 **Null** 或包含 [JetInit](./jetinit-function.md)所傳回的實際實例。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-113">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, then this parameter might be **NULL** or might contain the actual instance that is returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="b7c0b-114">如果引擎以多重實例模式運作，則此參數必須是使用 [JetCreateInstance](./jetcreateinstance-function.md)建立之實例的指標。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-114">If the engine is operating in multi-instance mode, then this parameter must be a pointer to an instance that was created using [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="b7c0b-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="b7c0b-115">Return Value</span></span>

<span data-ttu-id="b7c0b-116">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b7c0b-117">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b7c0b-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b7c0b-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="b7c0b-119">Description</span><span class="sxs-lookup"><span data-stu-id="b7c0b-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7c0b-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b7c0b-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b7c0b-121">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7c0b-122">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="b7c0b-122">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="b7c0b-123">提供的其中一個參數包含未預期的值，或數個參數的組合產生了非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-123">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="b7c0b-124">當引擎處於多重實例模式時，以及<em>pinstance</em>參考不正確實例時， <strong>JetTerm</strong>會傳回這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-124">This error will be returned by <strong>JetTerm</strong> when the engine is in multi-instance mode and when <em>pinstance</em> refers to an invalid instance.</span></span></p>
<p><span data-ttu-id="b7c0b-125"><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-125"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7c0b-126">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="b7c0b-126">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="b7c0b-127">無法完成作業，因為尚未初始化實例。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-127">The operation cannot complete because the instance has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7c0b-128">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="b7c0b-128">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="b7c0b-129">無法完成操作，因為正在關閉實例。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-129">The operation cannot complete because the instance is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7c0b-130">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="b7c0b-130">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="b7c0b-131">無法完成作業，因為實例上的還原作業正在進行中。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-131">It is not possible to complete the operation because a restore operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7c0b-132">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="b7c0b-132">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="b7c0b-133">作業無法完成，因為實例上的備份作業正在進行中。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-133">The operation cannot complete because a backup operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7c0b-134">JET_errTooManyActiveUsers</span><span class="sxs-lookup"><span data-stu-id="b7c0b-134">JET_errTooManyActiveUsers</span></span></p></td>
<td><p><span data-ttu-id="b7c0b-135">因為目前的會話具有指定實例的使用中交易，所以無法關閉實例。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-135">The instance cannot be shut down because there are currently sessions with active transactions for the specified instance.</span></span> <span data-ttu-id="b7c0b-136">只有使用 JET_bitTermComplete 時，才會發生此錯誤。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-136">This error occurs only if the JET_bitTermComplete is used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b7c0b-137">如果此函數成功，將會關閉指定的實例。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-137">If this function succeeds, the specified instance will be shut down.</span></span> <span data-ttu-id="b7c0b-138">實例控制碼也將會關閉，並且可供任何採用實例控制碼的 API 使用。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-138">The instance handle will also be closed and made unavailable to any API that takes an instance handle.</span></span> <span data-ttu-id="b7c0b-139">與實例相關聯的所有其他物件（例如會話）也會關閉。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-139">All other objects that are associated with the instance, such as sessions, will also be closed.</span></span> <span data-ttu-id="b7c0b-140">檢查點檔案、交易記錄檔和附加至實例的資料庫檔案的狀態，會在關閉程式期間進行修改。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-140">The state of the checkpoint file, transaction log files, and the database files attached to the instance will be modified during the shutdown process.</span></span>

<span data-ttu-id="b7c0b-141">如果使用錯誤的結果導致此函式失敗，則實例會維持在初始化狀態，而且不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-141">If this function fails as the result of a usage error, then the instance remains in an initialized state and nothing changes.</span></span> <span data-ttu-id="b7c0b-142">否則，實例仍會依據成功案例關閉。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-142">Otherwise, the instance is still shut down as per the success case.</span></span> <span data-ttu-id="b7c0b-143">不同之處在于實例在下次初始化時，必須經歷損毀復原。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-143">The difference is that the instance will need to go through crash recovery when it is next initialized.</span></span> <span data-ttu-id="b7c0b-144">引擎會嘗試盡可能將最多的資料排清，以將所需的復原量降至最低。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-144">The engine will try to flush as much data as possible to minimize the amount of recovery that is required.</span></span> <span data-ttu-id="b7c0b-145">就概念而言， **JetTerm** 失敗與進程損毀並無不同。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-145">Conceptually, such a failure of **JetTerm** is no different than a process crash.</span></span>

#### <a name="remarks"></a><span data-ttu-id="b7c0b-146">備註</span><span class="sxs-lookup"><span data-stu-id="b7c0b-146">Remarks</span></span>

<span data-ttu-id="b7c0b-147">如果實例的主機進程基於任何原因而結束，則在該實例上成功呼叫 **JetTerm** 之前，系統會將實例視為處於損毀狀態。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-147">If the host process of an instance quits for any reason before **JetTerm** is successfully called on that instance then the instance is considered to be in a crashed state.</span></span> <span data-ttu-id="b7c0b-148">當您下次嘗試初始化該實例時，將會發生損毀復原。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-148">Crash recovery will occur on the next attempt to initialize that instance.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b7c0b-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7c0b-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7c0b-150"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="b7c0b-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b7c0b-151">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-151">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7c0b-152"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="b7c0b-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b7c0b-153">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-153">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7c0b-154"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="b7c0b-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b7c0b-155">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7c0b-156"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="b7c0b-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b7c0b-157">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7c0b-158"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b7c0b-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b7c0b-159">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="b7c0b-159">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b7c0b-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7c0b-160">See Also</span></span>

[<span data-ttu-id="b7c0b-161">可擴充儲存引擎檔案</span><span class="sxs-lookup"><span data-stu-id="b7c0b-161">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="b7c0b-162">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="b7c0b-162">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="b7c0b-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b7c0b-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b7c0b-164">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="b7c0b-164">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="b7c0b-165">JetInit</span><span class="sxs-lookup"><span data-stu-id="b7c0b-165">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="b7c0b-166">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="b7c0b-166">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="b7c0b-167">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="b7c0b-167">JetTerm2</span></span>](./jetterm2-function.md)
