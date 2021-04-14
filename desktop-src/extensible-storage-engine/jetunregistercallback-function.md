---
description: 深入瞭解： JetUnregisterCallback 函數
title: JetUnregisterCallback 函式
TOCTitle: JetUnregisterCallback Function
ms:assetid: de5c7afa-07e1-4687-989b-b56125a9712e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294116(v=EXCHG.10)
ms:contentKeyID: 32765730
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUnregisterCallback
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b342bab655e3cf1e3c1a5967410edb1c971af87b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386130"
---
# <a name="jetunregistercallback-function"></a><span data-ttu-id="db6a2-103">JetUnregisterCallback 函式</span><span class="sxs-lookup"><span data-stu-id="db6a2-103">JetUnregisterCallback Function</span></span>


<span data-ttu-id="db6a2-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="db6a2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetunregistercallback-function"></a><span data-ttu-id="db6a2-105">JetUnregisterCallback 函式</span><span class="sxs-lookup"><span data-stu-id="db6a2-105">JetUnregisterCallback Function</span></span>

<span data-ttu-id="db6a2-106">**JetUnregisterCallback** 函式可讓應用程式設定 database engine，以在先前透過 [JetRegisterCallback](./jetregistercallback-function.md)要求時停止發出通知給應用程式。</span><span class="sxs-lookup"><span data-stu-id="db6a2-106">The **JetUnregisterCallback** function enables the application to configure the database engine to stop issuing notifications to the application as previously requested through [JetRegisterCallback](./jetregistercallback-function.md).</span></span>

<span data-ttu-id="db6a2-107">**Windows xp：**  **JetUnregisterCallback** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="db6a2-107">**Windows XP:**  **JetUnregisterCallback** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetUnregisterCallback(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_CBTYP cbtyp,
      __in          JET_HANDLE hCallbackId
    );
```

### <a name="parameters"></a><span data-ttu-id="db6a2-108">參數</span><span class="sxs-lookup"><span data-stu-id="db6a2-108">Parameters</span></span>

<span data-ttu-id="db6a2-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="db6a2-109">*sesid*</span></span>

<span data-ttu-id="db6a2-110">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="db6a2-110">The session to use for this call.</span></span>

<span data-ttu-id="db6a2-111">*tableid*</span><span class="sxs-lookup"><span data-stu-id="db6a2-111">*tableid*</span></span>

<span data-ttu-id="db6a2-112">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="db6a2-112">The cursor to use for this call.</span></span>

<span data-ttu-id="db6a2-113">*cbtyp*</span><span class="sxs-lookup"><span data-stu-id="db6a2-113">*cbtyp*</span></span>

<span data-ttu-id="db6a2-114">由應用程式不再希望接收通知的回呼原因所組成的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="db6a2-114">A bitmask composed of the callback reasons that the application no longer wishes to receive notifications.</span></span>

<span data-ttu-id="db6a2-115">若要建立此位元遮罩，請直接或將有效的回呼原因從 [JET_CBTYP](./jet-cbtyp.md) 列舉。</span><span class="sxs-lookup"><span data-stu-id="db6a2-115">To create this bitmask, simply or together valid callback reasons from the [JET_CBTYP](./jet-cbtyp.md) enumeration.</span></span>

<span data-ttu-id="db6a2-116">*hCallbackId*</span><span class="sxs-lookup"><span data-stu-id="db6a2-116">*hCallbackId*</span></span>

<span data-ttu-id="db6a2-117">[JetRegisterCallback](./jetregistercallback-function.md)所傳回之已註冊回呼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="db6a2-117">The handle of the registered callback that was returned by [JetRegisterCallback](./jetregistercallback-function.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="db6a2-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="db6a2-118">Return Value</span></span>

<span data-ttu-id="db6a2-119">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="db6a2-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="db6a2-120">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="db6a2-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="db6a2-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="db6a2-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="db6a2-122">Description</span><span class="sxs-lookup"><span data-stu-id="db6a2-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db6a2-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="db6a2-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="db6a2-124">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="db6a2-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db6a2-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="db6a2-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="db6a2-126">無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</span><span class="sxs-lookup"><span data-stu-id="db6a2-126">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db6a2-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="db6a2-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="db6a2-128">作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="db6a2-128">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="db6a2-129"><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="db6a2-129"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db6a2-130">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="db6a2-130">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="db6a2-131">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="db6a2-131">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db6a2-132">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="db6a2-132">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="db6a2-133">作業無法完成，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="db6a2-133">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db6a2-134">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="db6a2-134">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="db6a2-135">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="db6a2-135">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="db6a2-136"><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="db6a2-136"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db6a2-137">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="db6a2-137">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="db6a2-138">無法完成作業，因為與會話相關聯的實例正在關閉中。</span><span class="sxs-lookup"><span data-stu-id="db6a2-138">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="db6a2-139">如果此函式成功，則會使用與指定資料指標相關聯的資料表，取消註冊指定的回呼，以找出指定的回呼原因。</span><span class="sxs-lookup"><span data-stu-id="db6a2-139">If this function succeeds, the specified callback will be unregistered for the given callback reasons with the table that is associated with the given cursor.</span></span> <span data-ttu-id="db6a2-140">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="db6a2-140">No change to the database state will occur.</span></span>

<span data-ttu-id="db6a2-141">如果此函式失敗，將不會取消註冊指定的回呼。</span><span class="sxs-lookup"><span data-stu-id="db6a2-141">If this function fails, the specified callback will not be unregistered.</span></span> <span data-ttu-id="db6a2-142">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="db6a2-142">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="db6a2-143">備註</span><span class="sxs-lookup"><span data-stu-id="db6a2-143">Remarks</span></span>

<span data-ttu-id="db6a2-144">指定的位元遮罩應該完全符合註冊回呼時所指定的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="db6a2-144">The given bitmask should exactly match the bitmask that is specified when registering the callback.</span></span> <span data-ttu-id="db6a2-145">資料庫引擎目前不支援移除這些通知的子集，而且在嘗試這項功能時不會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="db6a2-145">The database engine does not currently support removing a subset of these notifications and it does not return an error when this is attempted.</span></span>

#### <a name="requirements"></a><span data-ttu-id="db6a2-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="db6a2-146">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db6a2-147"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="db6a2-147"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="db6a2-148">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="db6a2-148">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db6a2-149"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="db6a2-149"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="db6a2-150">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="db6a2-150">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db6a2-151"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="db6a2-151"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="db6a2-152">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="db6a2-152">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db6a2-153"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="db6a2-153"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="db6a2-154">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="db6a2-154">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db6a2-155"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="db6a2-155"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="db6a2-156">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="db6a2-156">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="db6a2-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db6a2-157">See Also</span></span>

[<span data-ttu-id="db6a2-158">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="db6a2-158">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="db6a2-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="db6a2-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="db6a2-160">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="db6a2-160">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="db6a2-161">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="db6a2-161">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="db6a2-162">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="db6a2-162">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="db6a2-163">JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="db6a2-163">JetRegisterCallback</span></span>](./jetregistercallback-function.md)  
[<span data-ttu-id="db6a2-164">JetStopService</span><span class="sxs-lookup"><span data-stu-id="db6a2-164">JetStopService</span></span>](./jetstopservice-function.md)
