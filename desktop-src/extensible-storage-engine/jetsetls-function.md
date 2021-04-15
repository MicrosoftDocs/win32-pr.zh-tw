---
description: 深入瞭解： JetSetLS 函數
title: JetSetLS 函式
TOCTitle: JetSetLS Function
ms:assetid: 4fc77e09-7173-42e8-9dfd-9a8d8de2fb9b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269243(v=EXCHG.10)
ms:contentKeyID: 32765545
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetLS
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ae1c68a039c11cd8a3f9b1299494c5057513caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511114"
---
# <a name="jetsetls-function"></a><span data-ttu-id="a665a-103">JetSetLS 函式</span><span class="sxs-lookup"><span data-stu-id="a665a-103">JetSetLS Function</span></span>


<span data-ttu-id="a665a-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a665a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetls-function"></a><span data-ttu-id="a665a-105">JetSetLS 函式</span><span class="sxs-lookup"><span data-stu-id="a665a-105">JetSetLS Function</span></span>

<span data-ttu-id="a665a-106">**JetSetLS** 函數可讓應用程式將稱為本機儲存的內容控制碼與資料指標或與該資料指標相關聯的資料表產生關聯。</span><span class="sxs-lookup"><span data-stu-id="a665a-106">The **JetSetLS** function enables the application to associate a context handle known as Local Storage with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="a665a-107">應用程式可以使用此內容控制碼來儲存與資料指標或資料表相關聯的輔助資料。</span><span class="sxs-lookup"><span data-stu-id="a665a-107">This context handle can be used by the application to store auxiliary data that is associated with a cursor or table.</span></span> <span data-ttu-id="a665a-108">當內容控制碼必須釋放時，應用程式稍後會使用執行時間回呼來通知。</span><span class="sxs-lookup"><span data-stu-id="a665a-108">The application is later notified using a runtime callback when the context handle must be released.</span></span> <span data-ttu-id="a665a-109">這樣就可以將動態配置的狀態與資料指標或資料表產生關聯。</span><span class="sxs-lookup"><span data-stu-id="a665a-109">This makes it possible to associate dynamically allocated state with a cursor or table.</span></span>

<span data-ttu-id="a665a-110">**Windows xp：**  **JetSetLS** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="a665a-110">**Windows XP:**  **JetSetLS** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetSetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_LS ls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="a665a-111">參數</span><span class="sxs-lookup"><span data-stu-id="a665a-111">Parameters</span></span>

<span data-ttu-id="a665a-112">*sesid*</span><span class="sxs-lookup"><span data-stu-id="a665a-112">*sesid*</span></span>

<span data-ttu-id="a665a-113">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="a665a-113">The session to use for this call.</span></span>

<span data-ttu-id="a665a-114">*tableid*</span><span class="sxs-lookup"><span data-stu-id="a665a-114">*tableid*</span></span>

<span data-ttu-id="a665a-115">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="a665a-115">The cursor to use for this call.</span></span>

<span data-ttu-id="a665a-116">*ls*</span><span class="sxs-lookup"><span data-stu-id="a665a-116">*ls*</span></span>

<span data-ttu-id="a665a-117">要與資料指標或資料表相關聯的內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="a665a-117">The context handle to be associated with the cursor or table.</span></span>

<span data-ttu-id="a665a-118">當指定 JET_bitLSReset 時，會忽略這個參數的實際值，並使用 JET_LSNil。</span><span class="sxs-lookup"><span data-stu-id="a665a-118">When JET_bitLSReset is specified then the actual value of this parameter is ignored and JET_LSNil is used.</span></span>

<span data-ttu-id="a665a-119">*grbit*</span><span class="sxs-lookup"><span data-stu-id="a665a-119">*grbit*</span></span>

<span data-ttu-id="a665a-120">位群組，其中包含要用於此呼叫的選項，包括下列零或多個。</span><span class="sxs-lookup"><span data-stu-id="a665a-120">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a665a-121">值</span><span class="sxs-lookup"><span data-stu-id="a665a-121">Value</span></span></p></th>
<th><p><span data-ttu-id="a665a-122">意義</span><span class="sxs-lookup"><span data-stu-id="a665a-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a665a-123">JET_bitLSCursor</span><span class="sxs-lookup"><span data-stu-id="a665a-123">JET_bitLSCursor</span></span></p></td>
<td><p><span data-ttu-id="a665a-124">此選項表示內容控制碼應該與指定的資料指標相關聯。</span><span class="sxs-lookup"><span data-stu-id="a665a-124">This option indicates that the context handle should be associated with the given cursor.</span></span></p>
<p><span data-ttu-id="a665a-125">如果沒有指定 JET_bitLSCursor 或 JET_bitLSTable，則會假設 JET_bitLSCursor。</span><span class="sxs-lookup"><span data-stu-id="a665a-125">If neither JET_bitLSCursor nor JET_bitLSTable is specified then JET_bitLSCursor is presumed.</span></span></p>
<p><span data-ttu-id="a665a-126">搭配 JET_bitLSTable 使用此選項是不合法的。</span><span class="sxs-lookup"><span data-stu-id="a665a-126">It is illegal to use this option with JET_bitLSTable.</span></span> <span data-ttu-id="a665a-127">如果嘗試這麼做，則作業將會失敗，並出現 JET_errInvalidgrbit。</span><span class="sxs-lookup"><span data-stu-id="a665a-127">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a665a-128">JET_bitLSReset</span><span class="sxs-lookup"><span data-stu-id="a665a-128">JET_bitLSReset</span></span></p></td>
<td><p><span data-ttu-id="a665a-129">此選項表示應該忽略指定的內容控制碼，並將所選物件的內容控制碼重設為 JET_LSNil。</span><span class="sxs-lookup"><span data-stu-id="a665a-129">This option indicates that the specified context handle should be ignored and that the context handle for the chosen object should be reset to JET_LSNil.</span></span></p>
<p><span data-ttu-id="a665a-130">請務必注意，此動作不會導致回呼清除所選物件的先前內容控制碼值。</span><span class="sxs-lookup"><span data-stu-id="a665a-130">It is important to note that this action will not result in a callback to cleanup the previous value of the context handle for the chosen object.</span></span> <span data-ttu-id="a665a-131">您可以使用 <a href="gg269234(v=exchg.10).md">JetGetLS</a> 搭配 JET_bitLSReset 來完成先前內容控制碼的適當清除。</span><span class="sxs-lookup"><span data-stu-id="a665a-131">Proper cleanup of the previous context handle can be achieved using <a href="gg269234(v=exchg.10).md">JetGetLS</a> with JET_bitLSReset.</span></span> <span data-ttu-id="a665a-132">如需詳細資訊，請參閱 <a href="gg269234(v=exchg.10).md">JetGetLS</a> 。</span><span class="sxs-lookup"><span data-stu-id="a665a-132">See <a href="gg269234(v=exchg.10).md">JetGetLS</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a665a-133">JET_bitLSTable</span><span class="sxs-lookup"><span data-stu-id="a665a-133">JET_bitLSTable</span></span></p></td>
<td><p><span data-ttu-id="a665a-134">此選項表示內容控制碼應該與指定資料指標相關聯的資料表相關聯。</span><span class="sxs-lookup"><span data-stu-id="a665a-134">This option indicates that the context handle should be associated with the table associated with the given cursor.</span></span></p>
<p><span data-ttu-id="a665a-135">搭配 JET_bitLSCursor 使用此選項是不合法的。</span><span class="sxs-lookup"><span data-stu-id="a665a-135">It is illegal to use this option with JET_bitLSCursor.</span></span> <span data-ttu-id="a665a-136">如果嘗試這麼做，則作業將會失敗，並出現 JET_errInvalidgrbit。</span><span class="sxs-lookup"><span data-stu-id="a665a-136">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="a665a-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="a665a-137">Return Value</span></span>

<span data-ttu-id="a665a-138">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="a665a-138">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a665a-139">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="a665a-139">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a665a-140">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a665a-140">Return code</span></span></p></th>
<th><p><span data-ttu-id="a665a-141">Description</span><span class="sxs-lookup"><span data-stu-id="a665a-141">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a665a-142">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a665a-142">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a665a-143">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="a665a-143">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a665a-144">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a665a-144">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a665a-145">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="a665a-145">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a665a-146">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="a665a-146">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="a665a-147">其中一個要求的選項無效、使用不正確或未執行。</span><span class="sxs-lookup"><span data-stu-id="a665a-147">One of the options requested was invalid, used incorrectly, or not implemented.</span></span> <span data-ttu-id="a665a-148">當同時指定 JET_bitLSCursor 和 JET_bitLSTable 時， <strong>JetSetLS</strong> 可能會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="a665a-148">This can happen for <strong>JetSetLS</strong> when JET_bitLSCursor and JET_bitLSTable are both specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a665a-149">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a665a-149">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a665a-150">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="a665a-150">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="a665a-151">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="a665a-151">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a665a-152">JET_errLSAlreadySet</span><span class="sxs-lookup"><span data-stu-id="a665a-152">JET_errLSAlreadySet</span></span></p></td>
<td><p><span data-ttu-id="a665a-153">給定的內容控制碼無法與要求的物件建立關聯，因為它已經有與其相關聯的內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="a665a-153">The given context handle could not be associated with the requested object because it already had a context handle associated with it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a665a-154">JET_errLSCallbackNotSpecified</span><span class="sxs-lookup"><span data-stu-id="a665a-154">JET_errLSCallbackNotSpecified</span></span></p></td>
<td><p><span data-ttu-id="a665a-155">給定的內容控制碼無法與要求的物件建立關聯，因為尚未針對與會話相關聯的實例設定執行時間回呼。</span><span class="sxs-lookup"><span data-stu-id="a665a-155">The given context handle could not be associated with the requested object because the runtime callback has not been configured for the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a665a-156">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a665a-156">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a665a-157">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="a665a-157">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a665a-158">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a665a-158">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a665a-159">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="a665a-159">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a665a-160">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a665a-160">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a665a-161">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="a665a-161">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a665a-162">成功時，指定的內容控制碼已成功與要求的物件相關聯。</span><span class="sxs-lookup"><span data-stu-id="a665a-162">On success, the given context handle was successfully associated with the requested object.</span></span> <span data-ttu-id="a665a-163">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="a665a-163">No change to the database state will occur.</span></span>

<span data-ttu-id="a665a-164">失敗時，不會變更所要求物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="a665a-164">On failure, no change to the state of the requested object has occurred.</span></span> <span data-ttu-id="a665a-165">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="a665a-165">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a665a-166">備註</span><span class="sxs-lookup"><span data-stu-id="a665a-166">Remarks</span></span>

<span data-ttu-id="a665a-167">資料指標或資料表的本機儲存區應視為暫時性快取。</span><span class="sxs-lookup"><span data-stu-id="a665a-167">The Local Storage for a cursor or table should be viewed as a volatile cache.</span></span> <span data-ttu-id="a665a-168">應用程式應該會先嘗試使用 [JetGetLS](./jetgetls-function.md)來取出內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="a665a-168">The application should first try to retrieve the context handle using [JetGetLS](./jetgetls-function.md).</span></span> <span data-ttu-id="a665a-169">如果未將值設定 (也就是 JET_LSNil) 則應用程式應該建立新的內容，並使用 **JetSetLS** 將它載入至快取。</span><span class="sxs-lookup"><span data-stu-id="a665a-169">If the value is not set (that is it is JET_LSNil) then the application should create a new context and load it into the cache using **JetSetLS**.</span></span> <span data-ttu-id="a665a-170">應用程式可以使用 JET_bitLSReset 呼叫 [JetGetLS](./jetgetls-function.md) 來清除快取。</span><span class="sxs-lookup"><span data-stu-id="a665a-170">The application can purge the cache using a call to [JetGetLS](./jetgetls-function.md) with JET_bitLSReset.</span></span> <span data-ttu-id="a665a-171">如果資料庫引擎清除快取，則會產生執行時間回呼，讓應用程式有機會清除該內容。</span><span class="sxs-lookup"><span data-stu-id="a665a-171">If the database engine purges the cache then a runtime callback will be generated to give the application a chance to cleanup that context.</span></span> <span data-ttu-id="a665a-172">回呼型別會針對與資料指標相關聯的內容控制碼 JET_cbtypFreeCursorLS，以及與資料表相關聯之內容控制碼的 JET_cbtypFreeTableLS。</span><span class="sxs-lookup"><span data-stu-id="a665a-172">The callback type will be JET_cbtypFreeCursorLS for a context handle associated with a cursor and JET_cbtypFreeTableLS for a context handle associated with a table.</span></span> <span data-ttu-id="a665a-173">無論是哪一種情況，內容控制碼都會以 pvArg1 的形式傳遞。</span><span class="sxs-lookup"><span data-stu-id="a665a-173">In either case, the context handle will be passed as pvArg1.</span></span> <span data-ttu-id="a665a-174">如需詳細資訊，請參閱 [JET_CALLBACK](./jet-callback-callback-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="a665a-174">See [JET_CALLBACK](./jet-callback-callback-function.md) for more information.</span></span>

<span data-ttu-id="a665a-175">在可以使用本機儲存體之前，必須為與指定會話相關聯的實例正確設定執行時間回呼。</span><span class="sxs-lookup"><span data-stu-id="a665a-175">The runtime callback must be properly configured for the instance associated with the given session before Local Storage can be used.</span></span> <span data-ttu-id="a665a-176">您可以使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 搭配 [JET_paramRuntimeCallback](./callback-parameters.md)來設定此回呼。</span><span class="sxs-lookup"><span data-stu-id="a665a-176">This callback can be set using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramRuntimeCallback](./callback-parameters.md).</span></span> <span data-ttu-id="a665a-177">如需詳細資訊，請參閱系統參數中的 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 和 [JET_paramRuntimeCallback](./callback-parameters.md) 。</span><span class="sxs-lookup"><span data-stu-id="a665a-177">See [JetSetSystemParameter](./jetsetsystemparameter-function.md) and [JET_paramRuntimeCallback](./callback-parameters.md) in System Parameters for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a665a-178">規格需求</span><span class="sxs-lookup"><span data-stu-id="a665a-178">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a665a-179"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="a665a-179"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a665a-180">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="a665a-180">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a665a-181"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="a665a-181"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a665a-182">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="a665a-182">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a665a-183"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="a665a-183"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a665a-184">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="a665a-184">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a665a-185"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="a665a-185"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a665a-186">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="a665a-186">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a665a-187"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a665a-187"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a665a-188">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="a665a-188">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a665a-189">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a665a-189">See Also</span></span>

[<span data-ttu-id="a665a-190">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="a665a-190">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="a665a-191">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a665a-191">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a665a-192">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="a665a-192">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="a665a-193">JET_LS</span><span class="sxs-lookup"><span data-stu-id="a665a-193">JET_LS</span></span>](./jet-ls.md)  
[<span data-ttu-id="a665a-194">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a665a-194">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a665a-195">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="a665a-195">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="a665a-196">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="a665a-196">JetGetLS</span></span>](./jetgetls-function.md)  
[<span data-ttu-id="a665a-197">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="a665a-197">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="a665a-198">系統參數</span><span class="sxs-lookup"><span data-stu-id="a665a-198">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
