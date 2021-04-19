---
description: 深入瞭解： JetRegisterCallback 函數
title: JetRegisterCallback 函式
TOCTitle: JetRegisterCallback Function
ms:assetid: 04c82fac-ffa2-477f-b4dd-59bbf1dde3c8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269175(v=EXCHG.10)
ms:contentKeyID: 32765478
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRegisterCallback
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 26ca7559488182f2d687d5c678639e108792f413
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972213"
---
# <a name="jetregistercallback-function"></a><span data-ttu-id="c5a82-103">JetRegisterCallback 函式</span><span class="sxs-lookup"><span data-stu-id="c5a82-103">JetRegisterCallback Function</span></span>


<span data-ttu-id="c5a82-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c5a82-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetregistercallback-function"></a><span data-ttu-id="c5a82-105">JetRegisterCallback 函式</span><span class="sxs-lookup"><span data-stu-id="c5a82-105">JetRegisterCallback Function</span></span>

<span data-ttu-id="c5a82-106">**JetRegisterCallback** 函式可讓應用程式設定 database engine，以對應用程式發出特定事件的通知。</span><span class="sxs-lookup"><span data-stu-id="c5a82-106">The **JetRegisterCallback** function allows the application to configure the database engine to issue notifications to the application for specific events.</span></span> <span data-ttu-id="c5a82-107">這些通知會與特定的資料表相關聯，而且只有在包含資料表的實例使用 [JetTerm](./jetterm-function.md)關閉時，才會維持有效。</span><span class="sxs-lookup"><span data-stu-id="c5a82-107">These notifications are associated with a specific table and remain in effect only until the instance containing the table is shut down using [JetTerm](./jetterm-function.md).</span></span>

<span data-ttu-id="c5a82-108">**Windows xp： JetRegisterCallback** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="c5a82-108">**Windows XP:  JetRegisterCallback** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetRegisterCallback(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_CBTYP cbtyp,
      __in          JET_CALLBACK pCallback,
      __in          void* pvContext,
      __out         JET_HANDLE* phCallbackId
    );
```

### <a name="parameters"></a><span data-ttu-id="c5a82-109">參數</span><span class="sxs-lookup"><span data-stu-id="c5a82-109">Parameters</span></span>

<span data-ttu-id="c5a82-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="c5a82-110">*sesid*</span></span>

<span data-ttu-id="c5a82-111">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="c5a82-111">The session to use for this call.</span></span>

<span data-ttu-id="c5a82-112">*tableid*</span><span class="sxs-lookup"><span data-stu-id="c5a82-112">*tableid*</span></span>

<span data-ttu-id="c5a82-113">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="c5a82-113">The cursor to use for this call.</span></span>

<span data-ttu-id="c5a82-114">*cbtyp*</span><span class="sxs-lookup"><span data-stu-id="c5a82-114">*cbtyp*</span></span>

<span data-ttu-id="c5a82-115">由應用程式希望接收通知的回呼原因所組成的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="c5a82-115">A bit mask composed of the callback reasons for which the application wishes to receive notifications.</span></span>

<span data-ttu-id="c5a82-116">若要建立此位元遮罩，請將 [JET_CBTYP](./jet-cbtyp.md) 列舉中的有效回呼原因直接或一起建立。</span><span class="sxs-lookup"><span data-stu-id="c5a82-116">To create this bit mask, simply or together valid callback reasons from the [JET_CBTYP](./jet-cbtyp.md) enumeration.</span></span>

<span data-ttu-id="c5a82-117">*pCallback*</span><span class="sxs-lookup"><span data-stu-id="c5a82-117">*pCallback*</span></span>

<span data-ttu-id="c5a82-118">應用程式回呼函數的函式指標。</span><span class="sxs-lookup"><span data-stu-id="c5a82-118">The function pointer to the callback function for the application.</span></span>

<span data-ttu-id="c5a82-119">*pvCoNtext*</span><span class="sxs-lookup"><span data-stu-id="c5a82-119">*pvContext*</span></span>

<span data-ttu-id="c5a82-120">指定將給予應用程式回呼函式的內容指標。</span><span class="sxs-lookup"><span data-stu-id="c5a82-120">Specifies a context pointer that will be given to the callback function for the application.</span></span>

<span data-ttu-id="c5a82-121">*phCallbackId*</span><span class="sxs-lookup"><span data-stu-id="c5a82-121">*phCallbackId*</span></span>

<span data-ttu-id="c5a82-122">傳回可稍後用來取消註冊使用 [JetUnregisterCallback](./jetunregistercallback-function.md)之指定回呼函數的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c5a82-122">Returns a handle that can later be used to cancel the registration of the given callback function using [JetUnregisterCallback](./jetunregistercallback-function.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="c5a82-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5a82-123">Return Value</span></span>

<span data-ttu-id="c5a82-124">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="c5a82-124">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c5a82-125">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="c5a82-125">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5a82-126">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c5a82-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="c5a82-127">Description</span><span class="sxs-lookup"><span data-stu-id="c5a82-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5a82-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c5a82-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c5a82-129">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="c5a82-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5a82-130">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c5a82-130">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c5a82-131">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="c5a82-131">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5a82-132">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c5a82-132">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c5a82-133">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="c5a82-133">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="c5a82-134">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c5a82-134">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5a82-135">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c5a82-135">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="c5a82-136">提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="c5a82-136">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="c5a82-137"><strong>JetRegisterCallback</strong>會在下列情況傳回此錯誤：</span><span class="sxs-lookup"><span data-stu-id="c5a82-137">This error will be returned by <strong>JetRegisterCallback</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="c5a82-138"><em>cbtyp</em> 為零，</span><span class="sxs-lookup"><span data-stu-id="c5a82-138"><em>cbtyp</em> is zero,</span></span></p></li>
<li><p><span data-ttu-id="c5a82-139"><em>pCallback</em> 為 Null。</span><span class="sxs-lookup"><span data-stu-id="c5a82-139"><em>pCallback</em> is NULL.</span></span></p></li>
<li><p><span data-ttu-id="c5a82-140"><em>phCallbackId</em> 為 Null。</span><span class="sxs-lookup"><span data-stu-id="c5a82-140"><em>phCallbackId</em> is NULL.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5a82-141">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c5a82-141">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c5a82-142">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="c5a82-142">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5a82-143">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c5a82-143">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c5a82-144">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="c5a82-144">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5a82-145">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="c5a82-145">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="c5a82-146">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="c5a82-146">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="c5a82-147">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c5a82-147">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5a82-148">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c5a82-148">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c5a82-149">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="c5a82-149">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c5a82-150">成功時，會使用與指定資料指標相關聯的資料表，針對給定的回呼原因註冊指定的回呼。</span><span class="sxs-lookup"><span data-stu-id="c5a82-150">On success, the specified callback will be registered for the given callback reasons with the table associated with the given cursor.</span></span> <span data-ttu-id="c5a82-151">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="c5a82-151">No change to the database state will occur.</span></span>

<span data-ttu-id="c5a82-152">失敗時，將不會註冊回呼。</span><span class="sxs-lookup"><span data-stu-id="c5a82-152">On failure, the callback will not be registered.</span></span> <span data-ttu-id="c5a82-153">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="c5a82-153">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c5a82-154">備註</span><span class="sxs-lookup"><span data-stu-id="c5a82-154">Remarks</span></span>

<span data-ttu-id="c5a82-155">這個方法提供一種方法，讓應用程式將 volatile 回呼與資料庫中的資料表產生關聯。</span><span class="sxs-lookup"><span data-stu-id="c5a82-155">This method provides a means for the application to associate volatile callbacks with a table in a database.</span></span> <span data-ttu-id="c5a82-156">如果應用程式希望將保存的回呼與資料庫中的資料表產生關聯，則應該使用[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)將回呼傳遞給[JET_TABLECREATE](./jet-tablecreate-structure.md) 。</span><span class="sxs-lookup"><span data-stu-id="c5a82-156">If the application wishes to associate persisted callbacks with a table in the database then it should pass the callback to [JET_TABLECREATE](./jet-tablecreate-structure.md) using [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="c5a82-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5a82-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5a82-158"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="c5a82-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a82-159">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="c5a82-159">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5a82-160"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="c5a82-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a82-161">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="c5a82-161">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5a82-162"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="c5a82-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a82-163">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="c5a82-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5a82-164"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="c5a82-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a82-165">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="c5a82-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5a82-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c5a82-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c5a82-167">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="c5a82-167">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c5a82-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5a82-168">See Also</span></span>

[<span data-ttu-id="c5a82-169">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="c5a82-169">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="c5a82-170">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="c5a82-170">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="c5a82-171">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c5a82-171">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c5a82-172">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="c5a82-172">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="c5a82-173">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c5a82-173">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c5a82-174">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c5a82-174">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c5a82-175">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="c5a82-175">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="c5a82-176">JetTerm</span><span class="sxs-lookup"><span data-stu-id="c5a82-176">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="c5a82-177">JetUnregisterCallback</span><span class="sxs-lookup"><span data-stu-id="c5a82-177">JetUnregisterCallback</span></span>](./jetunregistercallback-function.md)
