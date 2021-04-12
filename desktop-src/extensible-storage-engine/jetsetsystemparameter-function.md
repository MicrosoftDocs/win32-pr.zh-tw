---
description: 深入瞭解： JetSetSystemParameter 函數
title: JetSetSystemParameter 函式
TOCTitle: JetSetSystemParameter Function
ms:assetid: a244b5c9-6f6e-49d1-a6f7-9248feb9b92d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294044(v=EXCHG.10)
ms:contentKeyID: 32765643
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSystemParameterA
- JetSetSystemParameterW
- JetSetSystemParameter
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bbb57a1b50f3ad39525b894932f7111b56c3a076
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191498"
---
# <a name="jetsetsystemparameter-function"></a><span data-ttu-id="84642-103">JetSetSystemParameter 函式</span><span class="sxs-lookup"><span data-stu-id="84642-103">JetSetSystemParameter Function</span></span>


<span data-ttu-id="84642-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="84642-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetsystemparameter-function"></a><span data-ttu-id="84642-105">JetSetSystemParameter 函式</span><span class="sxs-lookup"><span data-stu-id="84642-105">JetSetSystemParameter Function</span></span>

<span data-ttu-id="84642-106">**JetSetSystemParameter** 函式是用來設定資料庫引擎的許多設定。</span><span class="sxs-lookup"><span data-stu-id="84642-106">The **JetSetSystemParameter** function is used to set the numerous configuration settings of the database engine.</span></span>

```cpp
    JET_ERR JET_API JetSetSystemParameter(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in          JET_API_PTR lParam,
      __in_opt      JET_PCSTR szParam
    );
```

### <a name="parameters"></a><span data-ttu-id="84642-107">參數</span><span class="sxs-lookup"><span data-stu-id="84642-107">Parameters</span></span>

<span data-ttu-id="84642-108">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="84642-108">*pinstance*</span></span>

<span data-ttu-id="84642-109">指定要用於此呼叫的實例。</span><span class="sxs-lookup"><span data-stu-id="84642-109">Specifies the instance to use for this call.</span></span>

<span data-ttu-id="84642-110">**Windows 2000：**  若為 Windows 2000，則會忽略此參數，且應一律為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="84642-110">**Windows 2000:**  For Windows 2000, this parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="84642-111">**WINDOWS XP：**  在 Windows XP 和更新版本中，這個參數有點多載。</span><span class="sxs-lookup"><span data-stu-id="84642-111">**Windows XP:**  For Windows XP and later releases, this parameter is somewhat overloaded.</span></span> <span data-ttu-id="84642-112">如果引擎在舊版模式下運作 (Windows 2000 相容性模式) 只支援一個實例，此參數可能是 **Null** ，或可能包含 [JetInit](./jetinit-function.md)所傳回的實際實例。</span><span class="sxs-lookup"><span data-stu-id="84642-112">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, then this parameter may be **NULL** or may contain the actual instance returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="84642-113">無論是哪一種情況，所有系統參數設定都是從一個實例讀取的。</span><span class="sxs-lookup"><span data-stu-id="84642-113">In either case, all system parameter settings are read from that one instance.</span></span> <span data-ttu-id="84642-114">如果引擎以多重實例模式運作，則此參數可以是 **Null** 或使用 [JetInit](./jetinit-function.md) 或 [JetCreateIndex](./jetcreateindex-function.md)所建立之實例的指標。</span><span class="sxs-lookup"><span data-stu-id="84642-114">If the engine is operating in multi-instance mode, then this parameter may be **NULL** or a pointer to an instance created using [JetInit](./jetinit-function.md) or [JetCreateIndex](./jetcreateindex-function.md).</span></span> <span data-ttu-id="84642-115">當此參數為 **Null** 時，會讀取全域系統參數設定 (或預設) 。</span><span class="sxs-lookup"><span data-stu-id="84642-115">When this parameter is **NULL** then the global system parameter setting (or default) is read.</span></span> <span data-ttu-id="84642-116">如果這個參數是實例，則會讀取該實例的系統參數設定。</span><span class="sxs-lookup"><span data-stu-id="84642-116">When this parameter is an instance then the system parameter setting for that instance is read.</span></span>

<span data-ttu-id="84642-117">雖然這在技術上是 out 參數，但此 API 永遠不會修改所提供緩衝區的內容。</span><span class="sxs-lookup"><span data-stu-id="84642-117">Even though this is technically an out parameter, this API never modifies the contents of the provided buffer.</span></span>

<span data-ttu-id="84642-118">*sesid*</span><span class="sxs-lookup"><span data-stu-id="84642-118">*sesid*</span></span>

<span data-ttu-id="84642-119">指定此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="84642-119">Specifies the session to use for this call.</span></span>

<span data-ttu-id="84642-120">指定時，會忽略指定的實例，並使用與會話相關聯的實例。</span><span class="sxs-lookup"><span data-stu-id="84642-120">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="84642-121">*paramid*</span><span class="sxs-lookup"><span data-stu-id="84642-121">*paramid*</span></span>

<span data-ttu-id="84642-122">將設定之系統參數的識別碼。</span><span class="sxs-lookup"><span data-stu-id="84642-122">The ID of the system parameter that will be set.</span></span> <span data-ttu-id="84642-123">請參閱 [系統參數](./extensible-storage-engine-system-parameters.md) ，以取得系統參數及其屬性的完整清單。</span><span class="sxs-lookup"><span data-stu-id="84642-123">See [System Parameters](./extensible-storage-engine-system-parameters.md) for a complete list of system parameters and their properties.</span></span>

<span data-ttu-id="84642-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="84642-124">*lParam*</span></span>

<span data-ttu-id="84642-125">如果系統參數是整數類型，則提供要為選取的系統參數設定的值。</span><span class="sxs-lookup"><span data-stu-id="84642-125">Provides the value to be set for the selected system parameter if that system parameter is of an integer type.</span></span>

<span data-ttu-id="84642-126">*szParam*</span><span class="sxs-lookup"><span data-stu-id="84642-126">*szParam*</span></span>

<span data-ttu-id="84642-127">如果系統參數是字串類型，則提供所選取系統參數的值。</span><span class="sxs-lookup"><span data-stu-id="84642-127">Provides the value for the selected system parameter if that system parameter is of a string type.</span></span>

### <a name="return-value"></a><span data-ttu-id="84642-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="84642-128">Return Value</span></span>

<span data-ttu-id="84642-129">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="84642-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="84642-130">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="84642-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="84642-131">傳回碼</span><span class="sxs-lookup"><span data-stu-id="84642-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="84642-132">Description</span><span class="sxs-lookup"><span data-stu-id="84642-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84642-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="84642-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="84642-134">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="84642-134">The operation completed successfully.</span></span></p>
<p><span data-ttu-id="84642-135"><strong>Windows Vista：</strong>  在 Windows Vista 和更新版本中，可以在不變更系統參數值的情況下傳回成功。</span><span class="sxs-lookup"><span data-stu-id="84642-135"><strong>Windows Vista:</strong>  On Windows Vista and later releases, success can be returned without a change to the system parameter's value.</span></span> <span data-ttu-id="84642-136">如需詳細資訊，請參閱 <a href="gg269346(v=exchg.10).md">中繼參數</a> 主題中的 JET_paramEnableAdvanced 系統參數。</span><span class="sxs-lookup"><span data-stu-id="84642-136">See the JET_paramEnableAdvanced system parameter in the <a href="gg269346(v=exchg.10).md">Meta Parameters</a> topic for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84642-137">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="84642-137">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="84642-138">此實例已使用 <a href="gg294068(v=exchg.10).md">JetInit</a> 呼叫初始化，因此無法執行此作業。</span><span class="sxs-lookup"><span data-stu-id="84642-138">The instance has been initialized using a call to <a href="gg294068(v=exchg.10).md">JetInit</a> and this operation cannot be performed as a result.</span></span> <span data-ttu-id="84642-139">當您嘗試在值的變更之後設定系統參數，而不影響資料庫引擎的狀態時，就會發生這種情況 <strong>JetSetSystemParameter</strong> 。</span><span class="sxs-lookup"><span data-stu-id="84642-139">This can happen for <strong>JetSetSystemParameter</strong> when an attempt is made to configure a system parameter after a change in its value cannot affect the state of the database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84642-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="84642-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="84642-141">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="84642-141">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84642-142">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="84642-142">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="84642-143">指定的元組索引參數不合法。</span><span class="sxs-lookup"><span data-stu-id="84642-143">The specified tuple index parameters were illegal.</span></span> <span data-ttu-id="84642-144">只有將<a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>、 <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>或<a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a>設定為不合法的值時， <strong>JetSetSystemParameter</strong>才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="84642-144">This error may be returned by <strong>JetSetSystemParameter</strong> only when setting <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>, or <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> to an illegal value.</span></span></p>
<p><span data-ttu-id="84642-145"><strong>WINDOWS XP 和 Windows Server 2003：</strong>  這只會發生在 Windows XP 與 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="84642-145"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84642-146">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="84642-146">JET_errInitInProgress</span></span></p></td>
<td><p><span data-ttu-id="84642-147">無法完成作業，因為與會話相關聯的實例正在初始化。</span><span class="sxs-lookup"><span data-stu-id="84642-147">It is not possible to complete the operation because the instance associated with the session is being initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84642-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="84642-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="84642-149">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="84642-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="84642-150"><strong>WINDOWS XP：</strong>  只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="84642-150"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84642-151">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="84642-151">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="84642-152">提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="84642-152">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="84642-153">在下列情況下， <strong>JetSetSystemParameter</strong> 可能會發生：</span><span class="sxs-lookup"><span data-stu-id="84642-153">This can happen for <strong>JetSetSystemParameter</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="84642-154">指定的系統參數識別碼無效或不受支援。</span><span class="sxs-lookup"><span data-stu-id="84642-154">The specified system parameter ID is invalid or unsupported.</span></span></p></li>
<li><p><span data-ttu-id="84642-155">已嘗試使用長度超出參數合法範圍的字串來設定字串值系統參數。</span><span class="sxs-lookup"><span data-stu-id="84642-155">An attempt was made to set a string-valued system parameter with a string whose length was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="84642-156">嘗試以檔案路徑設定字串值系統參數，其絕對路徑表示的長度超出該參數的合法範圍。</span><span class="sxs-lookup"><span data-stu-id="84642-156">An attempt was made to set a string-valued system parameter with a file path where the length of its absolute path representation was outside the legal range for that parameter.</span></span></p>
<p><span data-ttu-id="84642-157"><strong>Windows Vista：</strong>  只有在 Windows Vista 和更新的版本上才會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="84642-157"><strong>Windows Vista:</strong>  This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="84642-158">嘗試以參數的合法範圍以外的整數來設定整數值系統參數。</span><span class="sxs-lookup"><span data-stu-id="84642-158">An attempt was made to set an integer-valued system parameter with an integer that was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="84642-159">嘗試使用 <strong>Null</strong> <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> 指標、不正確 LCID 或一組不支援的 LCMapString 旗標來設定 JET_paramUnicodeIndexDefault。</span><span class="sxs-lookup"><span data-stu-id="84642-159">An attempt was made to set JET_paramUnicodeIndexDefault with a <strong>NULL</strong> <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> pointer, an invalid LCID, or an unsupported set of LCMapString flags.</span></span></p>
<p><span data-ttu-id="84642-160"><strong>Windows Vista：</strong>  只有在 Windows Vista 和更新的版本上才會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="84642-160"><strong>Windows Vista:</strong>  This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="84642-161">無法設定指定的系統參數，因為它是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="84642-161">The specified system parameter cannot be set because it is read-only.</span></span></p></li>
<li><p><span data-ttu-id="84642-162">嘗試在呼叫 <a href="gg294068(v=exchg.10).md">JetInit</a> 之後設定系統參數、資料庫引擎處於單一實例模式，且未指定會話。</span><span class="sxs-lookup"><span data-stu-id="84642-162">An attempt was made to set a system parameter after <a href="gg294068(v=exchg.10).md">JetInit</a> was called, the database engine is in single-instance mode, and a session was not specified.</span></span></p>
<p><span data-ttu-id="84642-163"><strong>WINDOWS XP 和 Windows Server 2003：</strong>  這只會發生在 Windows XP 與 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="84642-163"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></li>
<li><p><span data-ttu-id="84642-164">指定的系統參數是全域的，且已嘗試為該系統參數設定實例的特定值。</span><span class="sxs-lookup"><span data-stu-id="84642-164">The specified system parameter is global only and an attempt was made to set an instance specific value for that system parameter.</span></span></p>
<p><span data-ttu-id="84642-165"><strong>WINDOWS XP 和 Windows Server 2003：</strong>  這只會發生在 Windows XP 與 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="84642-165"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></li>
<li><p><span data-ttu-id="84642-166">指定的系統參數僅供每個實例使用，並嘗試設定該系統參數的全域值。</span><span class="sxs-lookup"><span data-stu-id="84642-166">The specified system parameter is per-instance only and an attempt was made to set the global value for that system parameter.</span></span></p>
<p><span data-ttu-id="84642-167"><strong>WINDOWS XP 和 Windows Server 2003：</strong>  這只會發生在 Windows XP 與 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="84642-167"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84642-168">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="84642-168">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="84642-169">指定的檔案系統路徑無效。</span><span class="sxs-lookup"><span data-stu-id="84642-169">The specified file system path was invalid.</span></span> <span data-ttu-id="84642-170">只有在設定代表檔案系統路徑的系統參數時， <strong>JetSetSystemParameter</strong> 才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="84642-170">This error may be returned by <strong>JetSetSystemParameter</strong> only when setting system parameters that represent file system paths.</span></span> <span data-ttu-id="84642-171">例如， <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> 可能會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="84642-171">For example, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> may return this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84642-172">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="84642-172">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="84642-173">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="84642-173">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84642-174">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="84642-174">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="84642-175">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="84642-175">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84642-176">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="84642-176">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="84642-177">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="84642-177">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84642-178">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="84642-178">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="84642-179">會話控制碼無效或參考已關閉的會話。</span><span class="sxs-lookup"><span data-stu-id="84642-179">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="84642-180">在所有情況下，都不會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="84642-180">This error is not returned under all circumstances.</span></span> <span data-ttu-id="84642-181">控制碼只會根據最大努力進行驗證。</span><span class="sxs-lookup"><span data-stu-id="84642-181">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84642-182">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="84642-182">JET_errInvalidInstance</span></span></p></td>
<td><p><span data-ttu-id="84642-183">實例控制碼無效，或參考已經關閉的實例。</span><span class="sxs-lookup"><span data-stu-id="84642-183">The instance handle is invalid or refers to an instance that has been shutdown.</span></span></p>
<p><span data-ttu-id="84642-184">在所有情況下，都不會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="84642-184">This error is not returned under all circumstances.</span></span> <span data-ttu-id="84642-185">控制碼只會根據最大努力進行驗證。</span><span class="sxs-lookup"><span data-stu-id="84642-185">Handles are validated on a best effort basis only.</span></span></p>
<p><span data-ttu-id="84642-186"><strong>Windows Vista：</strong>  只有 Windows Vista 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="84642-186"><strong>Windows Vista:</strong>  This error will only be returned by Windows Vista and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="84642-187">成功時，系統參數的設定將會設定為提供的值。</span><span class="sxs-lookup"><span data-stu-id="84642-187">On success, the setting for the system parameter will be set to the provided value.</span></span>

<span data-ttu-id="84642-188">失敗時，系統參數的設定將維持不變。</span><span class="sxs-lookup"><span data-stu-id="84642-188">On failure, the setting for the system parameter will remain unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="84642-189">備註</span><span class="sxs-lookup"><span data-stu-id="84642-189">Remarks</span></span>

<span data-ttu-id="84642-190">**JetSetSystemParameter** 在驗證每個系統參數所選擇的設定時，會執行不佳的作業。</span><span class="sxs-lookup"><span data-stu-id="84642-190">**JetSetSystemParameter** does a poor job of validating the chosen setting for each system parameter.</span></span> <span data-ttu-id="84642-191">請務必小心，不要依賴此驗證來強制執行良好的設定。</span><span class="sxs-lookup"><span data-stu-id="84642-191">Care must be taken to not rely on this validation to enforce good settings.</span></span> <span data-ttu-id="84642-192">請密切注意每個系統參數的描述，並遵循這些指導方針以取得良好的系統參數設定。</span><span class="sxs-lookup"><span data-stu-id="84642-192">Please pay close attention to the description of each system parameter and follow those guidelines for a good system parameter setting.</span></span>

<span data-ttu-id="84642-193">您應該一律設定一組系統參數，以保證資料庫引擎能如預期運作。</span><span class="sxs-lookup"><span data-stu-id="84642-193">There are a set of system parameters that should always be set to guarantee that the database engine works as intended.</span></span> <span data-ttu-id="84642-194">具體而言，您應該一律設定任何會影響 database engine 所使用之檔案實體配置的系統參數。</span><span class="sxs-lookup"><span data-stu-id="84642-194">Specifically, any system parameters that affect the physical layout of the files used by the database engine should always be set.</span></span> <span data-ttu-id="84642-195">如需詳細資訊，請參閱 [系統參數](./extensible-storage-engine-system-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="84642-195">For more information, see [System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="84642-196">每個系統參數都有預設值。</span><span class="sxs-lookup"><span data-stu-id="84642-196">Every system parameter has a default value.</span></span> <span data-ttu-id="84642-197">這些預設值會隨著時間而進化，而且非常任意。</span><span class="sxs-lookup"><span data-stu-id="84642-197">These default values have evolved over time and are quite arbitrary.</span></span> <span data-ttu-id="84642-198">強烈建議應用程式評估所有預設值，以確保它們是適當的。</span><span class="sxs-lookup"><span data-stu-id="84642-198">It is highly recommended that an application evaluate all the default values to ensure that they are appropriate.</span></span> <span data-ttu-id="84642-199">如果不適用，則應該由應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="84642-199">If they are not appropriate, then they should be configured by the application.</span></span> <span data-ttu-id="84642-200">這點很重要，因為許多參數可能會大幅影響資料庫引擎的可靠性、效能和資源使用率。</span><span class="sxs-lookup"><span data-stu-id="84642-200">This is important as many of these parameters can greatly impact the reliability, performance, and resource utilization of the database engine.</span></span>

#### <a name="requirements"></a><span data-ttu-id="84642-201">規格需求</span><span class="sxs-lookup"><span data-stu-id="84642-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84642-202"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="84642-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="84642-203">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="84642-203">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84642-204"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="84642-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="84642-205">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="84642-205">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84642-206"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="84642-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="84642-207">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="84642-207">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84642-208"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="84642-208"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="84642-209">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="84642-209">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84642-210"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="84642-210"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="84642-211">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="84642-211">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84642-212"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="84642-212"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="84642-213">實作為 <strong>JetSetSystemParameterW</strong> (Unicode) 和 <strong>JetSetSystemParameterA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="84642-213">Implemented as <strong>JetSetSystemParameterW</strong> (Unicode) and <strong>JetSetSystemParameterA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="84642-214">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84642-214">See Also</span></span>

[<span data-ttu-id="84642-215">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="84642-215">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="84642-216">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="84642-216">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="84642-217">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="84642-217">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="84642-218">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="84642-218">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="84642-219">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="84642-219">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="84642-220">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="84642-220">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="84642-221">JetInit</span><span class="sxs-lookup"><span data-stu-id="84642-221">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="84642-222">系統參數</span><span class="sxs-lookup"><span data-stu-id="84642-222">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
