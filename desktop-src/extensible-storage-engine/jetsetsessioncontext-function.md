---
description: 深入瞭解： JetSetSessionCoNtext 函數
title: JetSetSessionCoNtext 函式
TOCTitle: JetSetSessionContext Function
ms:assetid: e44efadf-a5c7-408a-ad68-56646b6ea650
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294124(v=EXCHG.10)
ms:contentKeyID: 32765738
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSessionContext
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4aafafa17499b76282599586f7477ac1ef6f878d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967158"
---
# <a name="jetsetsessioncontext-function"></a><span data-ttu-id="8c0cc-103">JetSetSessionCoNtext 函式</span><span class="sxs-lookup"><span data-stu-id="8c0cc-103">JetSetSessionContext Function</span></span>


<span data-ttu-id="8c0cc-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8c0cc-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetsessioncontext-function"></a><span data-ttu-id="8c0cc-105">JetSetSessionCoNtext 函式</span><span class="sxs-lookup"><span data-stu-id="8c0cc-105">JetSetSessionContext Function</span></span>

<span data-ttu-id="8c0cc-106">**JetSetSessionCoNtext** 函式會使用指定的內容控制碼，將會話與目前的執行緒產生關聯。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-106">The **JetSetSessionContext** function associates a session with the current thread using the given context handle.</span></span> <span data-ttu-id="8c0cc-107">此關聯會覆寫指定會話的交易必須完全在相同執行緒上執行的預設引擎需求。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-107">This association overrides the default engine requirement that a transaction for a given session must occur entirely on the same thread.</span></span>

```cpp
    JET_ERR JET_API JetSetSessionContext(
      __in          JET_SESID sesid,
      __in          JET_API_PTR ulContext
    );
```

### <a name="parameters"></a><span data-ttu-id="8c0cc-108">參數</span><span class="sxs-lookup"><span data-stu-id="8c0cc-108">Parameters</span></span>

<span data-ttu-id="8c0cc-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="8c0cc-109">*sesid*</span></span>

<span data-ttu-id="8c0cc-110">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-110">The session to use for this call.</span></span>

<span data-ttu-id="8c0cc-111">*ulCoNtext*</span><span class="sxs-lookup"><span data-stu-id="8c0cc-111">*ulContext*</span></span>

<span data-ttu-id="8c0cc-112">將與此會話相關聯的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-112">A unique identifier to which this session will be associated.</span></span>

### <a name="return-value"></a><span data-ttu-id="8c0cc-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="8c0cc-113">Return Value</span></span>

<span data-ttu-id="8c0cc-114">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="8c0cc-115">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8c0cc-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8c0cc-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="8c0cc-117">Description</span><span class="sxs-lookup"><span data-stu-id="8c0cc-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c0cc-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="8c0cc-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="8c0cc-119">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c0cc-120">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="8c0cc-120">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="8c0cc-121">無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-121">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c0cc-122">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="8c0cc-122">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="8c0cc-123">作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-123">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="8c0cc-124"><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-124"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c0cc-125">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="8c0cc-125">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="8c0cc-126">提供的其中一個參數包含未預期的值，或多個參數值的組合產生了非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-126">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span> <span data-ttu-id="8c0cc-127"><strong>JetSetSessionCoNtext</strong>會在下列情況下傳回此錯誤：</span><span class="sxs-lookup"><span data-stu-id="8c0cc-127">This error will be returned by <strong>JetSetSessionContext</strong> under the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="8c0cc-128"><em>ulCoNtext</em> 為 Null</span><span class="sxs-lookup"><span data-stu-id="8c0cc-128"><em>ulContext</em> is NULL</span></span></p></li>
<li><p><span data-ttu-id="8c0cc-129"><em>ulCoNtext</em> 為-1</span><span class="sxs-lookup"><span data-stu-id="8c0cc-129"><em>ulContext</em> is -1</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c0cc-130">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="8c0cc-130">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="8c0cc-131">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-131">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c0cc-132">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="8c0cc-132">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="8c0cc-133">作業無法完成，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-133">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c0cc-134">JET_errSessionCoNtextAlreadySet</span><span class="sxs-lookup"><span data-stu-id="8c0cc-134">JET_errSessionContextAlreadySet</span></span></p></td>
<td><p><span data-ttu-id="8c0cc-135">會話無法與目前的執行緒建立關聯，因為它已經與執行緒相關聯。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-135">The session could not be associated with the current thread because it has already been associated with a thread.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c0cc-136">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="8c0cc-136">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="8c0cc-137">無法完成作業，因為與會話相關聯的實例正在關閉中。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-137">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8c0cc-138">如果此函式成功，會話將會與目前的執行緒相關聯。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-138">If this function succeeds, the session will be associated with the current thread.</span></span> <span data-ttu-id="8c0cc-139">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-139">No change to the database state will occur.</span></span>

<span data-ttu-id="8c0cc-140">如果此函式失敗，會話狀態會維持不變。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-140">If this function fails, the session state will remain unchanged.</span></span> <span data-ttu-id="8c0cc-141">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-141">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="8c0cc-142">備註</span><span class="sxs-lookup"><span data-stu-id="8c0cc-142">Remarks</span></span>

<span data-ttu-id="8c0cc-143">在交易期間，會話通常會系結至特定的執行緒。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-143">A session is usually bound to a specific thread for the duration of a transaction.</span></span> <span data-ttu-id="8c0cc-144">此行為的設計目的是協助應用程式偵測和防止在多個執行緒之間共用單一會話的概念不良。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-144">This behavior is designed to help applications detect and prevent the conceptually ill-advised sharing of a single session amongst multiple threads.</span></span> <span data-ttu-id="8c0cc-145">有時候，這種簡單的檢查無法用於應用程式的架構。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-145">Sometimes, this simple check does not work with the application's architecture.</span></span> <span data-ttu-id="8c0cc-146">例如，如果應用程式使用執行緒集區來裝載伺服器端物件，而且交易跨越對指定物件的多個伺服器呼叫，則這項保護可能會導致某些呼叫失敗，但 JET_errSessionSharingViolation 即使使用模式正確也一樣。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-146">For example, if the application is hosting server-side objects using a thread pool and transactions span multiple server calls to a given object then this protection may cause some of those calls to fail with JET_errSessionSharingViolation even though the usage pattern is correct.</span></span> <span data-ttu-id="8c0cc-147">這種情況常見於 COM 物件伺服器。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-147">This situation is common for COM object servers.</span></span>

<span data-ttu-id="8c0cc-148">**JetSetSessionCoNtext** 和 [JetResetSessionCoNtext](./jetresetsessioncontext-function.md) 藉由讓此會話共用檢查更有彈性，來解決此問題。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-148">**JetSetSessionContext** and [JetResetSessionContext](./jetresetsessioncontext-function.md) solve this problem by making this session sharing check a little more flexible.</span></span> <span data-ttu-id="8c0cc-149">當應用程式開始使用特定會話進行一連串的 ESE API 呼叫時，它會先將會話內容設定為指定的值。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-149">When the application starts to make a series of ESE API calls using a particular session, it first sets the session context to a given value.</span></span> <span data-ttu-id="8c0cc-150">此動作會將會話與呼叫執行緒產生關聯。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-150">This action associates the session to the calling thread.</span></span> <span data-ttu-id="8c0cc-151">在給定的範例中，此內容可以是包含 JET 會話控制碼之物件的位址。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-151">In the given example, this context could be the address of the object that contains the JET session handle.</span></span> <span data-ttu-id="8c0cc-152">一旦進行了 ESE API 呼叫，應用程式就會重設會話內容。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-152">Once the ESE API calls have been made, the application resets the session context.</span></span> <span data-ttu-id="8c0cc-153">此動作會解除會話與呼叫執行緒的之間的操作。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-153">This action disassociates the session from the calling thread.</span></span> <span data-ttu-id="8c0cc-154">即使會話有使用中的交易，也可以由另一個執行緒使用物件和其會話。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-154">The object and its session can then be used by another thread even if the session has an active transaction.</span></span>

<span data-ttu-id="8c0cc-155">請務必注意，必須先呼叫 **JetSetSessionCoNtext** ，才能在該會話上開啟交易，否則關聯將無法運作。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-155">It is important to note that **JetSetSessionContext** must be called prior to opening a transaction on that session or the association will not work.</span></span>

<span data-ttu-id="8c0cc-156">**JetSetSessionCoNtext** 具備執行緒安全。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-156">**JetSetSessionContext** is thread safe.</span></span> <span data-ttu-id="8c0cc-157">多個執行緒可以嘗試同時在相同的會話上設定執行緒內容，而且只有一個會獲勝。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-157">Multiple threads can try to set a thread context on the same session at the same time and only one will win.</span></span> <span data-ttu-id="8c0cc-158">此事實可供應用程式用來從集區配置會話，而不會儲存其配置的外部狀態。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-158">This fact can be used by the application as a means to allocate a session from a pool without storing external state about its allocation.</span></span>

#### <a name="requirements"></a><span data-ttu-id="8c0cc-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c0cc-159">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c0cc-160"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="8c0cc-160"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8c0cc-161">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-161">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c0cc-162"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="8c0cc-162"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8c0cc-163">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-163">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c0cc-164"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="8c0cc-164"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8c0cc-165">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-165">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c0cc-166"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="8c0cc-166"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="8c0cc-167">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-167">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c0cc-168"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="8c0cc-168"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="8c0cc-169">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="8c0cc-169">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="8c0cc-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c0cc-170">See Also</span></span>

[<span data-ttu-id="8c0cc-171">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="8c0cc-171">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="8c0cc-172">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="8c0cc-172">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="8c0cc-173">JetResetSessionCoNtext</span><span class="sxs-lookup"><span data-stu-id="8c0cc-173">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="8c0cc-174">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="8c0cc-174">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="8c0cc-175">JetStopService</span><span class="sxs-lookup"><span data-stu-id="8c0cc-175">JetStopService</span></span>](./jetstopservice-function.md)
