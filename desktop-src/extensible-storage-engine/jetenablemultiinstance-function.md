---
description: 深入瞭解： JetEnableMultiInstance 函數
title: JetEnableMultiInstance 函式
TOCTitle: JetEnableMultiInstance Function
ms:assetid: d88a7b2a-c0d1-47de-9239-3631150d92da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294107(v=EXCHG.10)
ms:contentKeyID: 32765722
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnableMultiInstanceW
- JetEnableMultiInstanceA
- JetEnableMultiInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61fb058b14d9a8abeb282d4227b110ba50304a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989090"
---
# <a name="jetenablemultiinstance-function"></a><span data-ttu-id="4441c-103">JetEnableMultiInstance 函式</span><span class="sxs-lookup"><span data-stu-id="4441c-103">JetEnableMultiInstance Function</span></span>


<span data-ttu-id="4441c-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4441c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetenablemultiinstance-function"></a><span data-ttu-id="4441c-105">JetEnableMultiInstance 函式</span><span class="sxs-lookup"><span data-stu-id="4441c-105">JetEnableMultiInstance Function</span></span>

<span data-ttu-id="4441c-106">**JetEnableMultiInstance** 函式會設定資料庫引擎，以便在相同的進程中搭配多個實例使用。</span><span class="sxs-lookup"><span data-stu-id="4441c-106">The **JetEnableMultiInstance** function configures the database engine for use with multiple instances in the same process.</span></span> <span data-ttu-id="4441c-107">第一個呼叫端可以使用全域系統參數的選擇性陣列，以允許變更多重實例模式。</span><span class="sxs-lookup"><span data-stu-id="4441c-107">An optional array of global system parameters is available to the first caller allowing for the change to multi-instance mode.</span></span>

<span data-ttu-id="4441c-108">**Windows xp： JetEnableMultiInstance** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="4441c-108">**Windows XP:  JetEnableMultiInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetEnableMultiInstance(
      __in_opt      JET_SETSYSPARAM* psetsysparam,
      __in_opt      unsigned long csetsysparam,
      __out_opt     unsigned long* pcsetsucceed
    );
```

### <a name="parameters"></a><span data-ttu-id="4441c-109">參數</span><span class="sxs-lookup"><span data-stu-id="4441c-109">Parameters</span></span>

<span data-ttu-id="4441c-110">*psetsysparam*</span><span class="sxs-lookup"><span data-stu-id="4441c-110">*psetsysparam*</span></span>

<span data-ttu-id="4441c-111">全域系統參數的陣列，這些參數會在引擎因為此呼叫而進入多重實例模式時進行設定。</span><span class="sxs-lookup"><span data-stu-id="4441c-111">An array of global system parameters to set if and only if the engine enters multi-instance mode as a result of this call.</span></span> <span data-ttu-id="4441c-112">如果 *csetsysparam* 為零，則會忽略 *psetsysparam* 。</span><span class="sxs-lookup"><span data-stu-id="4441c-112">If *csetsysparam* is zero then *psetsysparam* is ignored.</span></span>

<span data-ttu-id="4441c-113">*csetsysparam*</span><span class="sxs-lookup"><span data-stu-id="4441c-113">*csetsysparam*</span></span>

<span data-ttu-id="4441c-114">要設定之全域參數陣列的元素計數（如果引擎因為此呼叫而進入多重實例模式，則為）。</span><span class="sxs-lookup"><span data-stu-id="4441c-114">The count of elements for the array of global parameters to set if and only if the engine enters multi-instance mode as a result of this call.</span></span> <span data-ttu-id="4441c-115">如果 *csetsysparam* 為零，則會忽略 *psetsysparam* 。</span><span class="sxs-lookup"><span data-stu-id="4441c-115">If *csetsysparam* is zero then *psetsysparam* is ignored.</span></span>

<span data-ttu-id="4441c-116">*pcsetsucceed*</span><span class="sxs-lookup"><span data-stu-id="4441c-116">*pcsetsucceed*</span></span>

<span data-ttu-id="4441c-117">全域系統參數計數的指標，這些參數已成功設定為此呼叫的結果。</span><span class="sxs-lookup"><span data-stu-id="4441c-117">A pointer to the count of global system parameters that were successfully configured as a result of this call.</span></span>

### <a name="return-value"></a><span data-ttu-id="4441c-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="4441c-118">Return Value</span></span>

<span data-ttu-id="4441c-119">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="4441c-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="4441c-120">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="4441c-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4441c-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4441c-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="4441c-122">Description</span><span class="sxs-lookup"><span data-stu-id="4441c-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4441c-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="4441c-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="4441c-124">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="4441c-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4441c-125">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="4441c-125">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="4441c-126">不允許指定的元組索引參數。</span><span class="sxs-lookup"><span data-stu-id="4441c-126">The specified tuple index parameters were not allowed.</span></span> <span data-ttu-id="4441c-127">只有將<a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>、 <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>或<a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a>設定為不合法的值時， <strong>JetEnableMultiInstance</strong>才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="4441c-127">This error can be returned by <strong>JetEnableMultiInstance</strong> only when setting <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>, or <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> to an illegal value.</span></span></p>
<p><span data-ttu-id="4441c-128"><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="4441c-128"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4441c-129">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="4441c-129">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="4441c-130">指定的檔案系統路徑無效。</span><span class="sxs-lookup"><span data-stu-id="4441c-130">The specified file system path was invalid.</span></span> <span data-ttu-id="4441c-131">只有在設定代表檔案系統路徑的系統參數時， <strong>JetEnableMultiInstance</strong> 才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="4441c-131">This error can be returned by <strong>JetEnableMultiInstance</strong> only when setting system parameters that represent file system paths.</span></span> <span data-ttu-id="4441c-132">例如， <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> 可能會傳回這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="4441c-132">For example, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> can return this error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4441c-133">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="4441c-133">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="4441c-134">作業失敗，因為當 database engine 在單一實例模式中作業時，它是不合法的 (Windows 2000 相容性模式) 。</span><span class="sxs-lookup"><span data-stu-id="4441c-134">The operation failed because it is illegal when the database engine is operating in single instance mode (Windows 2000 compatibility mode).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4441c-135">JET_errSystemParamsAlreadySet</span><span class="sxs-lookup"><span data-stu-id="4441c-135">JET_errSystemParamsAlreadySet</span></span></p></td>
<td><p><span data-ttu-id="4441c-136"><strong>JetEnableMultiInstance</strong> 失敗，因為引擎已處於多重實例模式。</span><span class="sxs-lookup"><span data-stu-id="4441c-136"><strong>JetEnableMultiInstance</strong> failed because the engine is already in multi-instance mode.</span></span></p>
<p><span data-ttu-id="4441c-137"><strong>注意  </strong>即使未指定任何系統參數，也會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="4441c-137"><strong>Note  </strong>This will happen even if no system parameters are specified.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4441c-138">如果此函式成功，資料庫引擎將設定為在多重實例模式中執行。</span><span class="sxs-lookup"><span data-stu-id="4441c-138">If this function succeeds, the database engine will be configured to run in multi-instance mode.</span></span> <span data-ttu-id="4441c-139">引擎也已使用全域系統參數的選擇性清單成功設定。</span><span class="sxs-lookup"><span data-stu-id="4441c-139">The engine was also successfully configured with the optional list of global system parameters.</span></span>

<span data-ttu-id="4441c-140">如果此函式失敗，database engine 將維持在目前的模式。</span><span class="sxs-lookup"><span data-stu-id="4441c-140">If this function fails, the database engine will remain in the current mode.</span></span> <span data-ttu-id="4441c-141">如果 *pcsetsucceed* 不是零，則系統參數的數目將維持不變。</span><span class="sxs-lookup"><span data-stu-id="4441c-141">If *pcsetsucceed* is non-zero, that number of system parameters will remain set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="4441c-142">備註</span><span class="sxs-lookup"><span data-stu-id="4441c-142">Remarks</span></span>

<span data-ttu-id="4441c-143">只有當應用程式在設定資料庫引擎以在相同進程的多重使用者案例中使用時，必須以不可部分完成的方式設定一組指定的系統參數時，才應該使用此函數。</span><span class="sxs-lookup"><span data-stu-id="4441c-143">This function should only be used if the application must configure a given set of system parameters atomically when setting up the database engine for use in a multi-user scenario in the same process.</span></span> <span data-ttu-id="4441c-144">如果有另一種同步處理方法，最好是分別呼叫 [JetCreateInstance](./jetcreateinstance-function.md) 和 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="4441c-144">If another method of synchronization is available, it is preferable to call [JetCreateInstance](./jetcreateinstance-function.md) and [JetSetSystemParameter](./jetsetsystemparameter-function.md) separately.</span></span>

#### <a name="requirements"></a><span data-ttu-id="4441c-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="4441c-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4441c-146"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="4441c-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4441c-147">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="4441c-147">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4441c-148"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="4441c-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4441c-149">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="4441c-149">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4441c-150"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="4441c-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4441c-151">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="4441c-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4441c-152"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="4441c-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="4441c-153">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="4441c-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4441c-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="4441c-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="4441c-155">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="4441c-155">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4441c-156"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="4441c-156"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="4441c-157">實作為 <strong>JetEnableMultiInstanceW</strong> (Unicode) 和 <strong>JetEnableMultiInstanceA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="4441c-157">Implemented as <strong>JetEnableMultiInstanceW</strong> (Unicode) and <strong>JetEnableMultiInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4441c-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4441c-158">See Also</span></span>

[<span data-ttu-id="4441c-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4441c-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4441c-160">JET_SETSYSPARAM</span><span class="sxs-lookup"><span data-stu-id="4441c-160">JET_SETSYSPARAM</span></span>](./jet-setsysparam-structure.md)  
[<span data-ttu-id="4441c-161">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="4441c-161">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="4441c-162">JetInit</span><span class="sxs-lookup"><span data-stu-id="4441c-162">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="4441c-163">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="4441c-163">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
