---
description: 深入瞭解： JetSetSessionParameter 函數
title: JetSetSessionParameter 函式
TOCTitle: JetSetSessionParameter Function
ms:assetid: 11aecf42-22ef-4bea-a3d7-961a7bdc85aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835038(v=EXCHG.10)
ms:contentKeyID: 49894660
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 926ae0db2e47ce571f441ab5836c4ddbe6f8bcc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943289"
---
# <a name="jetsetsessionparameter-function"></a><span data-ttu-id="5cbcb-103">JetSetSessionParameter 函式</span><span class="sxs-lookup"><span data-stu-id="5cbcb-103">JetSetSessionParameter Function</span></span>


<span data-ttu-id="5cbcb-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5cbcb-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="5cbcb-105">**JetSetSessionParameter** 函數會設定 database engine。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-105">The **JetSetSessionParameter** function configures the database engine.</span></span>

``` c++
JET_ERR JET_API JetSetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __in_read_bytes_opt_(cbParam)  void* pvParam,
  __in          unsigned long cbParam
);
```

### <a name="parameters"></a><span data-ttu-id="5cbcb-106">參數</span><span class="sxs-lookup"><span data-stu-id="5cbcb-106">Parameters</span></span>

<span data-ttu-id="5cbcb-107">*sesid*</span><span class="sxs-lookup"><span data-stu-id="5cbcb-107">*sesid*</span></span>

<span data-ttu-id="5cbcb-108">指定此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-108">Specifies the session to use for this call.</span></span>

<span data-ttu-id="5cbcb-109">指定時，會忽略指定的實例，並使用與會話相關聯的實例。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-109">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="5cbcb-110">*sesparamid*</span><span class="sxs-lookup"><span data-stu-id="5cbcb-110">*sesparamid*</span></span>

<span data-ttu-id="5cbcb-111">要設定之會話參數的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-111">The ID of the session parameter to set.</span></span>

<span data-ttu-id="5cbcb-112">*pvParam*</span><span class="sxs-lookup"><span data-stu-id="5cbcb-112">*pvParam*</span></span>

<span data-ttu-id="5cbcb-113">要在此會話參數中設定的資料。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-113">The data to set in this session parameter.</span></span>

<span data-ttu-id="5cbcb-114">*cbParam*</span><span class="sxs-lookup"><span data-stu-id="5cbcb-114">*cbParam*</span></span>

<span data-ttu-id="5cbcb-115">所提供資料的大小。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-115">The size of the data provided.</span></span>

### <a name="return-value"></a><span data-ttu-id="5cbcb-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="5cbcb-116">Return value</span></span>

<span data-ttu-id="5cbcb-117">此函數會傳回 [JET_ERR](./jet-err.md) 資料類型，其中包含下表所列的其中一個傳回碼。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-117">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="5cbcb-118">如需可能的可延伸儲存引擎 (ESE) 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-118">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5cbcb-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5cbcb-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="5cbcb-120">Description</span><span class="sxs-lookup"><span data-stu-id="5cbcb-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cbcb-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5cbcb-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5cbcb-122">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcb-123">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="5cbcb-123">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="5cbcb-124">已使用 <a href="gg294068(v=exchg.10).md">JetInit</a> 函式的呼叫來初始化實例，因此無法執行此作業。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-124">The instance has been initialized by using a call to the <a href="gg294068(v=exchg.10).md">JetInit</a> function and this operation cannot be performed as a result.</span></span> <span data-ttu-id="5cbcb-125">當您嘗試在參數值變更之後設定系統參數，不會再影響資料庫引擎的狀態時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-125">This can happen when an attempt is made to configure a system parameter after a change in the parameter value can no longer affect the state of the database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcb-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="5cbcb-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="5cbcb-127">無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因為呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a> 函數。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcb-128">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="5cbcb-128">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="5cbcb-129">指定的元組索引參數不合法。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-129">The specified tuple index parameters were illegal.</span></span> <span data-ttu-id="5cbcb-130">只有當 <em>JET_paramIndexTuplesLengthMin</em>、 <em>JET_paramIndexTuplesLengthMax</em>或 <em>JET_paramIndexTuplesToIndexMax</em> 參數設定為不合法的值時，才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-130">This error is returned only when the <em>JET_paramIndexTuplesLengthMin</em>, <em>JET_paramIndexTuplesLengthMax</em>, or <em>JET_paramIndexTuplesToIndexMax</em> parameter is set to an illegal value.</span></span> <span data-ttu-id="5cbcb-131">如需這些參數的詳細資訊，請參閱 <a href="gg294119(v=exchg.10).md">索引參數</a>。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-131">For information about these parameters, see <a href="gg294119(v=exchg.10).md">Index Parameters</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcb-132">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="5cbcb-132">JET_errInitInProgress</span></span></p></td>
<td><p><span data-ttu-id="5cbcb-133">無法完成作業，因為與會話相關聯的實例正在初始化。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-133">It is not possible to complete the operation because the instance associated with the session is being initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcb-134">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="5cbcb-134">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="5cbcb-135">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-135">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcb-136">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="5cbcb-136">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="5cbcb-137">提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-137">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="5cbcb-138">發生下列情況時可能會發生這種情況：</span><span class="sxs-lookup"><span data-stu-id="5cbcb-138">This can happen when the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="5cbcb-139">指定的系統參數識別碼無效或不受支援。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-139">The specified system parameter ID is invalid or unsupported.</span></span></p></li>
<li><p><span data-ttu-id="5cbcb-140">嘗試以字串的長度設定字串值系統參數，其長度超出參數的合法範圍。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-140">An attempt was made to set a string-valued system parameter with a string the length of which was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="5cbcb-141">嘗試以檔案路徑設定字串值系統參數，其絕對路徑表示的長度超出該參數的合法範圍。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-141">An attempt was made to set a string-valued system parameter with a file path where the length of its absolute path representation was outside the legal range for that parameter.</span></span></p></li>
<li><p><span data-ttu-id="5cbcb-142">嘗試以參數的合法範圍以外的整數來設定整數值系統參數。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-142">An attempt was made to set an integer-valued system parameter with an integer that was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="5cbcb-143">嘗試使用 null <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> 指標、不正確 LCID 或一組不支援的 <strong>LCMapString</strong> 旗標來設定 JET_paramUnicodeIndexDefault。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-143">An attempt was made to set JET_paramUnicodeIndexDefault with a null <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> pointer, an invalid LCID, or an unsupported set of <strong>LCMapString</strong> flags.</span></span></p></li>
<li><p><span data-ttu-id="5cbcb-144">無法設定指定的系統參數，因為它是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-144">The specified system parameter cannot be set because it is read-only.</span></span></p></li>
<li><p><span data-ttu-id="5cbcb-145">嘗試在呼叫 <a href="gg294068(v=exchg.10).md">JetInit</a> 函數之後設定系統參數、資料庫引擎處於單一實例模式，且未指定會話。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-145">An attempt was made to set a system parameter after the <a href="gg294068(v=exchg.10).md">JetInit</a> function was called, the database engine is in single-instance mode, and a session was not specified.</span></span></p></li>
<li><p><span data-ttu-id="5cbcb-146">指定的系統參數是全域的，且已嘗試為該系統參數設定實例特定的值。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-146">The specified system parameter is global only and an attempt was made to set an instance-specific value for that system parameter.</span></span></p></li>
<li><p><span data-ttu-id="5cbcb-147">指定的系統參數僅供每個實例使用，並嘗試設定該系統參數的全域值。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-147">The specified system parameter is per-instance only and an attempt was made to set the global value for that system parameter.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcb-148">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="5cbcb-148">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="5cbcb-149">指定的檔案系統路徑無效。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-149">The specified file system path was invalid.</span></span> <span data-ttu-id="5cbcb-150">只有在設定代表檔案系統路徑的系統參數時， <strong>JetSetSessionParameter</strong> 才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-150">This error may be returned by <strong>JetSetSessionParameter</strong> only when setting system parameters that represent file system paths.</span></span> <span data-ttu-id="5cbcb-151">例如， <em>JET_paramSystemPath</em> 參數可能會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-151">For example, the <em>JET_paramSystemPath</em> parameter may return this error.</span></span> <span data-ttu-id="5cbcb-152">如需這個參數的詳細資訊，請參閱 <a href="gg269235(v=exchg.10).md">交易記錄參數</a>。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-152">For information about this parameter, see <a href="gg269235(v=exchg.10).md">Transaction Log Parameters</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcb-153">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="5cbcb-153">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="5cbcb-154">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-154">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcb-155">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="5cbcb-155">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="5cbcb-156">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-156">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcb-157">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="5cbcb-157">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="5cbcb-158">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-158">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcb-159">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="5cbcb-159">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="5cbcb-160">會話控制碼無效或參考已關閉的會話。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-160">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="5cbcb-161">在所有情況下，都不會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-161">This error is not returned under all circumstances.</span></span> <span data-ttu-id="5cbcb-162">控制碼只會根據最大努力進行驗證。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-162">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcb-163">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="5cbcb-163">JET_errInvalidInstance</span></span></p></td>
<td><p><span data-ttu-id="5cbcb-164">實例控制碼無效，或參考已關閉的實例。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-164">The instance handle is invalid or refers to an instance that has been shut down.</span></span></p>
<p><span data-ttu-id="5cbcb-165">在所有情況下，都不會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-165">This error is not returned under all circumstances.</span></span> <span data-ttu-id="5cbcb-166">控制碼只會根據最大努力進行驗證。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-166">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5cbcb-167">成功時，系統參數將會設定為提供的值。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-167">On success, the system parameter will be set to the provided value.</span></span>

<span data-ttu-id="5cbcb-168">失敗時，系統參數值會維持不變。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-168">On failure, the system parameter value will remain unchanged.</span></span>

#### <a name="requirements"></a><span data-ttu-id="5cbcb-169">規格需求</span><span class="sxs-lookup"><span data-stu-id="5cbcb-169">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cbcb-170"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="5cbcb-170"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5cbcb-171">需要 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-171">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcb-172"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="5cbcb-172"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5cbcb-173">需要 Windows Server 2012。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-173">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcb-174"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="5cbcb-174"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5cbcb-175">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-175">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbcb-176"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="5cbcb-176"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5cbcb-177">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-177">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cbcb-178"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5cbcb-178"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5cbcb-179">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="5cbcb-179">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5cbcb-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5cbcb-180">See also</span></span>

[<span data-ttu-id="5cbcb-181">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="5cbcb-181">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="5cbcb-182">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5cbcb-182">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5cbcb-183">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="5cbcb-183">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="5cbcb-184">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="5cbcb-184">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="5cbcb-185">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="5cbcb-185">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="5cbcb-186">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="5cbcb-186">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="5cbcb-187">JetInit</span><span class="sxs-lookup"><span data-stu-id="5cbcb-187">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="5cbcb-188">系統參數</span><span class="sxs-lookup"><span data-stu-id="5cbcb-188">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
