---
description: 深入瞭解： JetEndSession 函數
title: JetEndSession 函式
TOCTitle: JetEndSession Function
ms:assetid: a9a8f98a-258e-4fbb-bed0-657581984a07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294054(v=EXCHG.10)
ms:contentKeyID: 32765660
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndSession
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46bea6f5db745252a5e0ac6e8e03550dfead1b43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319643"
---
# <a name="jetendsession-function"></a><span data-ttu-id="c752b-103">JetEndSession 函式</span><span class="sxs-lookup"><span data-stu-id="c752b-103">JetEndSession Function</span></span>


<span data-ttu-id="c752b-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c752b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetendsession-function"></a><span data-ttu-id="c752b-105">JetEndSession 函式</span><span class="sxs-lookup"><span data-stu-id="c752b-105">JetEndSession Function</span></span>

<span data-ttu-id="c752b-106">**JetEndSession** 函式會結束會話，並清除和解除配置與指定會話相關聯的任何資源。</span><span class="sxs-lookup"><span data-stu-id="c752b-106">The **JetEndSession** function ends the session, and cleans up and deallocates any resources associated with the specified session.</span></span>

```cpp
    JET_ERR JET_API JetEndSession(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="c752b-107">參數</span><span class="sxs-lookup"><span data-stu-id="c752b-107">Parameters</span></span>

<span data-ttu-id="c752b-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="c752b-108">*sesid*</span></span>

<span data-ttu-id="c752b-109">要結束的會話。</span><span class="sxs-lookup"><span data-stu-id="c752b-109">The session to end.</span></span> <span data-ttu-id="c752b-110">當會話結束時，會釋放相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="c752b-110">Associated resources are released when the session ends.</span></span>

<span data-ttu-id="c752b-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="c752b-111">*grbit*</span></span>

<span data-ttu-id="c752b-112">保留的。</span><span class="sxs-lookup"><span data-stu-id="c752b-112">Reserved.</span></span> <span data-ttu-id="c752b-113">此參數可包含 JET_bitForceSessionClosed 旗標，但此旗標已保留，且設定不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="c752b-113">This parameter can contain the JET_bitForceSessionClosed flag, but this flag is reserved and setting it has no effect.</span></span>

### <a name="return-value"></a><span data-ttu-id="c752b-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c752b-114">Return Value</span></span>

<span data-ttu-id="c752b-115">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="c752b-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c752b-116">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="c752b-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c752b-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c752b-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="c752b-118">Description</span><span class="sxs-lookup"><span data-stu-id="c752b-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c752b-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c752b-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c752b-120">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="c752b-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c752b-121">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c752b-121">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c752b-122">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="c752b-122">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c752b-123">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c752b-123">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="c752b-124">提供的其中一個參數包含未預期的值，或多個參數值的組合產生了非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="c752b-124">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c752b-125">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="c752b-125">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="c752b-126">會話不是有效的 JET 會話。</span><span class="sxs-lookup"><span data-stu-id="c752b-126">The session was not a valid JET session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c752b-127">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c752b-127">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c752b-128">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="c752b-128">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c752b-129">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="c752b-129">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="c752b-130">因為無法配置記憶體，所以操作失敗。</span><span class="sxs-lookup"><span data-stu-id="c752b-130">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c752b-131">JET_errSessionInUse</span><span class="sxs-lookup"><span data-stu-id="c752b-131">JET_errSessionInUse</span></span></p></td>
<td><p><span data-ttu-id="c752b-132">這表示會話已在另一個執行緒上使用，或未正確設定或重設會話。</span><span class="sxs-lookup"><span data-stu-id="c752b-132">This means the session was in use on another thread, or the session was not set or reset properly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c752b-133">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c752b-133">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c752b-134">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="c752b-134">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="c752b-135">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c752b-135">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c752b-136">JET_errOutOfBuffers</span><span class="sxs-lookup"><span data-stu-id="c752b-136">JET_errOutOfBuffers</span></span></p></td>
<td><p><span data-ttu-id="c752b-137">指出沒有其他緩衝區的系統錯誤。</span><span class="sxs-lookup"><span data-stu-id="c752b-137">System error that indicates that there are no more buffers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c752b-138">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c752b-138">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c752b-139">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="c752b-139">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c752b-140">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c752b-140">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c752b-141">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="c752b-141">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c752b-142">成功時，會話控制碼已關閉且無法使用，而且與此會話相關的所有資源都會清除。</span><span class="sxs-lookup"><span data-stu-id="c752b-142">On success, the session handle is closed, and unavailable, and all resources related to this session are cleaned up.</span></span>

<span data-ttu-id="c752b-143">失敗時，有數個額外的錯誤可能會在排序表關閉、資料指標關閉和交易回復時發生。</span><span class="sxs-lookup"><span data-stu-id="c752b-143">On failure, there are several additional errors that could occur as part of sort table close, cursor close, and transaction rollback.</span></span> <span data-ttu-id="c752b-144">這些錯誤不太可能發生，而且如果在呼叫 **JetEndSession** 時，您的會話完全不在使用中，則不太可能發生。</span><span class="sxs-lookup"><span data-stu-id="c752b-144">These errors are fairly unlikely, and extremely unlikely if your sessions are completely not in use when **JetEndSession** is called.</span></span> <span data-ttu-id="c752b-145">如果無法正確清除會話的某些部分，將會傳回這些錯誤。</span><span class="sxs-lookup"><span data-stu-id="c752b-145">These errors will be returned if some part of the session was unable to be cleaned up properly.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c752b-146">備註</span><span class="sxs-lookup"><span data-stu-id="c752b-146">Remarks</span></span>

<span data-ttu-id="c752b-147">此 API 會復原任何開啟的交易 (未認可至層級 0) 。</span><span class="sxs-lookup"><span data-stu-id="c752b-147">This API will rollback any open transactions (not committed to level 0).</span></span> <span data-ttu-id="c752b-148">此外，也會清除與此會話相關聯的所有資料指標，以及已建立或開啟的任何排序表。</span><span class="sxs-lookup"><span data-stu-id="c752b-148">Also all cursors associated with this session, and any sort tables that have been created or opened will be cleaned up.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c752b-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="c752b-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c752b-150"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="c752b-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c752b-151">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="c752b-151">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c752b-152"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="c752b-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c752b-153">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="c752b-153">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c752b-154"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="c752b-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c752b-155">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="c752b-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c752b-156"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="c752b-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c752b-157">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="c752b-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c752b-158"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c752b-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c752b-159">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="c752b-159">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c752b-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c752b-160">See Also</span></span>

[<span data-ttu-id="c752b-161">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="c752b-161">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="c752b-162">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c752b-162">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c752b-163">JetBeginSession</span><span class="sxs-lookup"><span data-stu-id="c752b-163">JetBeginSession</span></span>](./jetbeginsession-function.md)  
[<span data-ttu-id="c752b-164">JetRollback</span><span class="sxs-lookup"><span data-stu-id="c752b-164">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="c752b-165">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="c752b-165">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="c752b-166">JetStopService</span><span class="sxs-lookup"><span data-stu-id="c752b-166">JetStopService</span></span>](./jetstopservice-function.md)
