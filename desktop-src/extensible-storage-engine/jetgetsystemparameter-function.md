---
description: 深入瞭解： JetGetSystemParameter 函數
title: JetGetSystemParameter 函式
TOCTitle: JetGetSystemParameter Function
ms:assetid: 6e6ddb49-702c-4c45-ac9f-35ae817696dd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269291(v=EXCHG.10)
ms:contentKeyID: 32765583
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSystemParameter
- JetGetSystemParameterA
- JetGetSystemParameterW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 80005be47037bade1f22e8125d4633c5dac45f8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194596"
---
# <a name="jetgetsystemparameter-function"></a><span data-ttu-id="5c032-103">JetGetSystemParameter 函式</span><span class="sxs-lookup"><span data-stu-id="5c032-103">JetGetSystemParameter Function</span></span>


<span data-ttu-id="5c032-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5c032-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetsystemparameter-function"></a><span data-ttu-id="5c032-105">JetGetSystemParameter 函式</span><span class="sxs-lookup"><span data-stu-id="5c032-105">JetGetSystemParameter Function</span></span>

<span data-ttu-id="5c032-106">**JetGetSystemParameter** 函式會讀取資料庫引擎的許多設定。</span><span class="sxs-lookup"><span data-stu-id="5c032-106">The **JetGetSystemParameter** function reads the numerous configuration settings of the database engine.</span></span>

```cpp
    JET_ERR JET_API JetGetSystemParameter(
      __in          JET_INSTANCE instance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in_out_opt  JET_API_PTR* plParam,
      __out_opt     JET_PSTR szParam,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a><span data-ttu-id="5c032-107">參數</span><span class="sxs-lookup"><span data-stu-id="5c032-107">Parameters</span></span>

<span data-ttu-id="5c032-108">*實例*</span><span class="sxs-lookup"><span data-stu-id="5c032-108">*instance*</span></span>

<span data-ttu-id="5c032-109">此呼叫所要使用的實例。</span><span class="sxs-lookup"><span data-stu-id="5c032-109">The instance to use for this call.</span></span>

<span data-ttu-id="5c032-110">若為 Windows 2000，則會忽略此參數，且應一律為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="5c032-110">For Windows 2000, this parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="5c032-111">在 Windows XP 和更新版本中，這個參數有點多載。</span><span class="sxs-lookup"><span data-stu-id="5c032-111">For Windows XP and later releases, this parameter is somewhat overloaded.</span></span> <span data-ttu-id="5c032-112">如果引擎在舊版模式下運作 (Windows 2000 相容性模式) 只支援一個實例，此參數可能是 **Null** 或包含 [JetInit](./jetinit-function.md)所傳回的實際實例。</span><span class="sxs-lookup"><span data-stu-id="5c032-112">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, this parameter may be **NULL** or may contain the actual instance returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="5c032-113">無論是哪一種情況，所有系統參數設定都是從一個實例讀取的。</span><span class="sxs-lookup"><span data-stu-id="5c032-113">In either case, all system parameter settings are read from that one instance.</span></span> <span data-ttu-id="5c032-114">如果引擎是在多重實例模式中作業，這個參數可以是 **Null** 或使用 [JetInit](./jetinit-function.md) 或 [JetCreateInstance](./jetcreateinstance-function.md)所建立之實例的指標。</span><span class="sxs-lookup"><span data-stu-id="5c032-114">If the engine is operating in multi-instance mode, this parameter may be **NULL** or a pointer to an instance created using [JetInit](./jetinit-function.md) or [JetCreateInstance](./jetcreateinstance-function.md).</span></span> <span data-ttu-id="5c032-115">當此參數為 **Null** 時，會讀取全域系統參數設定 (或預設) 。</span><span class="sxs-lookup"><span data-stu-id="5c032-115">When this parameter is **NULL** then the global system parameter setting (or default) is read.</span></span> <span data-ttu-id="5c032-116">如果這個參數是實例，則會讀取該實例的系統參數設定。</span><span class="sxs-lookup"><span data-stu-id="5c032-116">When this parameter is an instance then the system parameter setting for that instance is read.</span></span>

<span data-ttu-id="5c032-117">*sesid*</span><span class="sxs-lookup"><span data-stu-id="5c032-117">*sesid*</span></span>

<span data-ttu-id="5c032-118">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="5c032-118">The session to use for this call.</span></span>

<span data-ttu-id="5c032-119">指定時，會忽略指定的實例，並使用與會話相關聯的實例。</span><span class="sxs-lookup"><span data-stu-id="5c032-119">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="5c032-120">*paramid*</span><span class="sxs-lookup"><span data-stu-id="5c032-120">*paramid*</span></span>

<span data-ttu-id="5c032-121">將讀取之系統參數的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5c032-121">The ID of the system parameter that will be read.</span></span>

<span data-ttu-id="5c032-122">請參閱 [系統參數](./extensible-storage-engine-system-parameters.md) ，以取得系統參數及其屬性的完整清單。</span><span class="sxs-lookup"><span data-stu-id="5c032-122">See [System Parameters](./extensible-storage-engine-system-parameters.md) for a complete list of system parameters and their properties.</span></span>

<span data-ttu-id="5c032-123">*plParam*</span><span class="sxs-lookup"><span data-stu-id="5c032-123">*plParam*</span></span>

<span data-ttu-id="5c032-124">輸出緩衝區，如果該系統參數是整數類型，則會接收所選系統參數的值。</span><span class="sxs-lookup"><span data-stu-id="5c032-124">The output buffer that receives the value of the selected system parameter if that system parameter is of an integer type.</span></span>

<span data-ttu-id="5c032-125">*szParam*</span><span class="sxs-lookup"><span data-stu-id="5c032-125">*szParam*</span></span>

<span data-ttu-id="5c032-126">輸出緩衝區，如果系統參數是字串類型，則會接收所選系統參數的值。</span><span class="sxs-lookup"><span data-stu-id="5c032-126">The output buffer that receives the value of the selected system parameter if that system parameter is of a string type.</span></span>

<span data-ttu-id="5c032-127">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="5c032-127">*cbMax*</span></span>

<span data-ttu-id="5c032-128">字串輸出緩衝區的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5c032-128">The maximum size in bytes of the string output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="5c032-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="5c032-129">Return Value</span></span>

<span data-ttu-id="5c032-130">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="5c032-130">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="5c032-131">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="5c032-131">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5c032-132">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5c032-132">Return code</span></span></p></th>
<th><p><span data-ttu-id="5c032-133">Description</span><span class="sxs-lookup"><span data-stu-id="5c032-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c032-134">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5c032-134">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5c032-135">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="5c032-135">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c032-136">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="5c032-136">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="5c032-137">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="5c032-137">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c032-138">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="5c032-138">JET_errInitInProgress</span></span></p></td>
<td><p><span data-ttu-id="5c032-139">無法完成作業，因為與會話相關聯的實例正在初始化。</span><span class="sxs-lookup"><span data-stu-id="5c032-139">It is not possible to complete the operation because the instance associated with the session is being initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c032-140">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="5c032-140">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="5c032-141">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="5c032-141">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="5c032-142">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="5c032-142">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c032-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="5c032-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="5c032-144">提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="5c032-144">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span></p>
<p><span data-ttu-id="5c032-145">在下列情況下， <strong>JetGetSystemParameter</strong> 可能會發生：</span><span class="sxs-lookup"><span data-stu-id="5c032-145">This can happen for <strong>JetGetSystemParameter</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="5c032-146">指定的系統參數識別碼無效或不受支援。</span><span class="sxs-lookup"><span data-stu-id="5c032-146">The specified system parameter ID is invalid or unsupported.</span></span></p></li>
<li><p><span data-ttu-id="5c032-147">指定的系統參數需要提供整數輸出緩衝區，而且輸出緩衝區指標為 <strong>Null</strong>。</span><span class="sxs-lookup"><span data-stu-id="5c032-147">The specified system parameter requires the integer output buffer to be provided and that output buffer pointer was <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="5c032-148">指定的系統參數需要提供字串輸出緩衝區，而且輸出緩衝區指標為 <strong>Null</strong>。</span><span class="sxs-lookup"><span data-stu-id="5c032-148">The specified system parameter requires a string output buffer to be provided and that output buffer pointer was <strong>NULL</strong>.</span></span></p>
<p><span data-ttu-id="5c032-149"><strong>Windows Vista：  </strong>只有在 Windows Vista 和更新的版本上才會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="5c032-149"><strong>Windows Vista:  </strong>This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="5c032-150">指定的系統參數需要提供字串輸出緩衝區，而且輸出緩衝區的大小太小，無法接受以 null 結尾的字串。</span><span class="sxs-lookup"><span data-stu-id="5c032-150">The specified system parameter requires a string output buffer to be provided and the size of that output buffer is too small to accept a null terminated string.</span></span></p>
<p><span data-ttu-id="5c032-151"><strong>Windows Vista：  </strong>只有在 Windows Vista 和更新的版本上才會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="5c032-151"><strong>Windows Vista:  </strong>This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="5c032-152">無法讀取指定的系統參數，因為它是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="5c032-152">The specified system parameter cannot be read because it is write-only.</span></span></p></li>
<li><p><span data-ttu-id="5c032-153">指定的系統參數是全域的，而且嘗試讀取該系統參數的實例特定值。</span><span class="sxs-lookup"><span data-stu-id="5c032-153">The specified system parameter is global only and an attempt was made to read an instance specific value for that system parameter.</span></span> <span data-ttu-id="5c032-154">這只會發生在 Windows XP 和更新版本上。</span><span class="sxs-lookup"><span data-stu-id="5c032-154">This can only happen on Windows XP and later releases.</span></span></p></li>
<li><p><span data-ttu-id="5c032-155">指定的系統參數僅供每個實例使用，並嘗試讀取該系統參數的全域值。</span><span class="sxs-lookup"><span data-stu-id="5c032-155">The specified system parameter is per-instance only and an attempt was made to read the global value for that system parameter.</span></span> <span data-ttu-id="5c032-156">這只會發生在 Windows XP 和更新版本上。</span><span class="sxs-lookup"><span data-stu-id="5c032-156">This can only happen on Windows XP and later releases.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c032-157">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="5c032-157">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="5c032-158">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="5c032-158">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c032-159">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="5c032-159">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="5c032-160">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="5c032-160">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c032-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="5c032-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="5c032-162">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="5c032-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c032-163">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="5c032-163">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="5c032-164">會話控制碼無效或參考已關閉的會話。</span><span class="sxs-lookup"><span data-stu-id="5c032-164">The session handle is invalid or refers to a closed session.</span></span> <span data-ttu-id="5c032-165">在所有情況下，都不會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="5c032-165">This error is not returned under all circumstances.</span></span> <span data-ttu-id="5c032-166">控制碼只會根據最大努力進行驗證。</span><span class="sxs-lookup"><span data-stu-id="5c032-166">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c032-167">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="5c032-167">JET_errInvalidInstance</span></span></p></td>
<td><p><span data-ttu-id="5c032-168">實例控制碼無效，或參考已經關閉的實例。</span><span class="sxs-lookup"><span data-stu-id="5c032-168">The instance handle is invalid or refers to an instance that has been shutdown.</span></span> <span data-ttu-id="5c032-169">在所有情況下，都不會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="5c032-169">This error is not returned under all circumstances.</span></span> <span data-ttu-id="5c032-170">控制碼只會根據最大努力進行驗證。</span><span class="sxs-lookup"><span data-stu-id="5c032-170">Handles are validated on a best effort basis only.</span></span></p>
<p><span data-ttu-id="5c032-171"><strong>Windows Vista：  </strong>只有 Windows Vista 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="5c032-171"><strong>Windows Vista:  </strong>This error will only be returned by Windows Vista and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c032-172">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="5c032-172">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="5c032-173">作業已順利完成，但輸出緩衝區太小，無法接收整個系統參數設定。</span><span class="sxs-lookup"><span data-stu-id="5c032-173">The operation completed successfully, but the output buffer was too small to receive the entire system parameter setting.</span></span></p>
<p><span data-ttu-id="5c032-174">輸出緩衝區已填滿系統參數設定的大小。</span><span class="sxs-lookup"><span data-stu-id="5c032-174">The output buffer has been filled with as much of the system parameter setting as would fit.</span></span> <span data-ttu-id="5c032-175">如果輸出緩衝區的長度至少要有一個字元，則該輸出緩衝區中的字串會以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="5c032-175">If the output buffer is at least one character in length then the string in that output buffer will be null terminated.</span></span></p>
<p><span data-ttu-id="5c032-176"><strong>注意  </strong>所有版本都不會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="5c032-176"><strong>Note  </strong>This error is not returned by all releases.</span></span> <span data-ttu-id="5c032-177">如需詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="5c032-177">Please see the Remarks section for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c032-178">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="5c032-178">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="5c032-179">因為輸出緩衝區太小而無法接收整個系統參數設定，所以操作失敗。</span><span class="sxs-lookup"><span data-stu-id="5c032-179">The operation failed because the output buffer was too small to receive the entire system parameter setting.</span></span></p>
<p><span data-ttu-id="5c032-180"><strong>注意  </strong>在某些情況下不會傳回此錯誤，以保留應用程式相容性。</span><span class="sxs-lookup"><span data-stu-id="5c032-180"><strong>Note  </strong>This error is not returned in some cases to preserve application compatibility.</span></span> <span data-ttu-id="5c032-181">如需詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="5c032-181">Please see the Remarks section for more information.</span></span></p>
<p><span data-ttu-id="5c032-182"><strong>Windows Vista：  </strong>只有 Windows Vista 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="5c032-182"><strong>Windows Vista:  </strong>This error will only be returned by Windows Vista and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5c032-183">成功時，適用于所要求系統參數的輸出緩衝區將會設定為該系統參數的值。</span><span class="sxs-lookup"><span data-stu-id="5c032-183">On success, the output buffer appropriate for the requested system parameter will be set to the value of that system parameter.</span></span>

<span data-ttu-id="5c032-184">失敗時，輸出緩衝區的狀態將會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="5c032-184">On failure, the state of the output buffers will be undefined.</span></span>

#### <a name="remarks"></a><span data-ttu-id="5c032-185">備註</span><span class="sxs-lookup"><span data-stu-id="5c032-185">Remarks</span></span>

<span data-ttu-id="5c032-186">此 API 存在所有版本中的重要問題。</span><span class="sxs-lookup"><span data-stu-id="5c032-186">There is an important problem in this API that is present in all releases.</span></span> <span data-ttu-id="5c032-187">如果要求具有字串值的系統參數，而且輸出緩衝區太小而無法接收整個系統參數設定，則不會傳回 JET_wrnBufferTruncated。</span><span class="sxs-lookup"><span data-stu-id="5c032-187">If a system parameter with a string value is requested and the output buffer is too small to receive the entire system parameter setting, JET_wrnBufferTruncated will NOT be returned.</span></span> <span data-ttu-id="5c032-188">改為傳回 JET_errSuccess。</span><span class="sxs-lookup"><span data-stu-id="5c032-188">JET_errSuccess is returned instead.</span></span> <span data-ttu-id="5c032-189">如果傳回字串的長度等於輸出緩衝區的大小，但不是 **Null** 結束字元，則呼叫端應該會像是傳回 JET_wrnBufferTruncated 一樣回應。</span><span class="sxs-lookup"><span data-stu-id="5c032-189">If the length of the returned string is equal to the size of the output buffer less the **NULL** terminator, the caller should react as if JET_wrnBufferTruncated were returned.</span></span> <span data-ttu-id="5c032-190">如果指定了零大小的字串輸出緩衝區，呼叫端應該會像是傳回 JET_errInvalidParameter 一樣回應。</span><span class="sxs-lookup"><span data-stu-id="5c032-190">If a zero-sized string output buffer is specified, the caller should react as if JET_errInvalidParameter were returned.</span></span>

#### <a name="requirements"></a><span data-ttu-id="5c032-191">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c032-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c032-192"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="5c032-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5c032-193">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="5c032-193">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c032-194"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="5c032-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5c032-195">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="5c032-195">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c032-196"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="5c032-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5c032-197">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="5c032-197">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c032-198"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="5c032-198"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5c032-199">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="5c032-199">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c032-200"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5c032-200"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5c032-201">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="5c032-201">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c032-202"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="5c032-202"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="5c032-203">實作為 <strong>JetGetSystemParameterW</strong> (Unicode) 和 <strong>JetGetSystemParameterA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="5c032-203">Implemented as <strong>JetGetSystemParameterW</strong> (Unicode) and <strong>JetGetSystemParameterA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5c032-204">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c032-204">See Also</span></span>

[<span data-ttu-id="5c032-205">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="5c032-205">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="5c032-206">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5c032-206">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5c032-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="5c032-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="5c032-208">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="5c032-208">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="5c032-209">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="5c032-209">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="5c032-210">JetInit</span><span class="sxs-lookup"><span data-stu-id="5c032-210">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="5c032-211">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="5c032-211">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="5c032-212">JetStopService</span><span class="sxs-lookup"><span data-stu-id="5c032-212">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="5c032-213">系統參數</span><span class="sxs-lookup"><span data-stu-id="5c032-213">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
