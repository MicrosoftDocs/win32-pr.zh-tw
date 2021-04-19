---
description: 深入瞭解： JetResetTableSequential 函數
title: JetResetTableSequential 函式
TOCTitle: JetResetTableSequential Function
ms:assetid: 5fe9daf2-5ef1-46d6-b0c3-ef92fb57d8bb
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269261(v=EXCHG.10)
ms:contentKeyID: 32765563
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetResetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 86de80ac935af81fd2b4e8fdfef8b20dbb8d27d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988842"
---
# <a name="jetresettablesequential-function"></a><span data-ttu-id="ce221-103">JetResetTableSequential 函式</span><span class="sxs-lookup"><span data-stu-id="ce221-103">JetResetTableSequential Function</span></span>


<span data-ttu-id="ce221-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ce221-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetresettablesequential-function"></a><span data-ttu-id="ce221-105">JetResetTableSequential 函式</span><span class="sxs-lookup"><span data-stu-id="ce221-105">JetResetTableSequential Function</span></span>

<span data-ttu-id="ce221-106">**JetResetTableSequential** 函式會通知資料庫引擎，應用程式不會再掃描包含指定資料指標的整個目前索引。</span><span class="sxs-lookup"><span data-stu-id="ce221-106">The **JetResetTableSequential** function notifies the database engine that the application is no longer scanning the entire current index containing a given cursor.</span></span> <span data-ttu-id="ce221-107">此呼叫會反轉 [JetSetTableSequential](./jetsettablesequential-function.md)所傳送的通知。</span><span class="sxs-lookup"><span data-stu-id="ce221-107">This call reverses a notification sent by [JetSetTableSequential](./jetsettablesequential-function.md).</span></span>

<span data-ttu-id="ce221-108">**Windows xp：**   **JetResetTableSequential** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="ce221-108">**Windows XP:**   **JetResetTableSequential** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetResetTableSequential(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="ce221-109">參數</span><span class="sxs-lookup"><span data-stu-id="ce221-109">Parameters</span></span>

<span data-ttu-id="ce221-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="ce221-110">*sesid*</span></span>

<span data-ttu-id="ce221-111">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="ce221-111">The session to use for this call.</span></span>

<span data-ttu-id="ce221-112">*tableid*</span><span class="sxs-lookup"><span data-stu-id="ce221-112">*tableid*</span></span>

<span data-ttu-id="ce221-113">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="ce221-113">The cursor to use for this call.</span></span>

<span data-ttu-id="ce221-114">*grbit*</span><span class="sxs-lookup"><span data-stu-id="ce221-114">*grbit*</span></span>

<span data-ttu-id="ce221-115">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="ce221-115">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="ce221-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="ce221-116">Return Value</span></span>

<span data-ttu-id="ce221-117">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="ce221-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ce221-118">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="ce221-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ce221-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ce221-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="ce221-120">Description</span><span class="sxs-lookup"><span data-stu-id="ce221-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ce221-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ce221-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ce221-122">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="ce221-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce221-123">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="ce221-123">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="ce221-124">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="ce221-124">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce221-125">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="ce221-125">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="ce221-126">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="ce221-126">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="ce221-127">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="ce221-127">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce221-128">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="ce221-128">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="ce221-129">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="ce221-129">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce221-130">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="ce221-130">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="ce221-131">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="ce221-131">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce221-132">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="ce221-132">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="ce221-133">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="ce221-133">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ce221-134">成功時，目前的資料指標索引已不再針對整個索引的連續掃描進行優化。</span><span class="sxs-lookup"><span data-stu-id="ce221-134">On success, the current index of the cursor is no longer optimized for a sequential scan of the entire index.</span></span> <span data-ttu-id="ce221-135">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="ce221-135">No change to the database state will occur.</span></span>

<span data-ttu-id="ce221-136">失敗時，將不會變更資料指標的設定。</span><span class="sxs-lookup"><span data-stu-id="ce221-136">On failure, no change to the configuration of the cursor will occur.</span></span> <span data-ttu-id="ce221-137">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="ce221-137">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ce221-138">備註</span><span class="sxs-lookup"><span data-stu-id="ce221-138">Remarks</span></span>

<span data-ttu-id="ce221-139">您可以安全地針對之前未透過呼叫 [JetSetTableSequential](./jetsettablesequential-function.md)設定的資料指標進行此呼叫。</span><span class="sxs-lookup"><span data-stu-id="ce221-139">It is safe to make this call against a cursor that has not been previously configured by a call to [JetSetTableSequential](./jetsettablesequential-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="ce221-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce221-140">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ce221-141"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="ce221-141"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ce221-142">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="ce221-142">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce221-143"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="ce221-143"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ce221-144">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="ce221-144">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce221-145"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="ce221-145"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ce221-146">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="ce221-146">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce221-147"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="ce221-147"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ce221-148">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="ce221-148">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce221-149"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ce221-149"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ce221-150">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="ce221-150">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ce221-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce221-151">See Also</span></span>

[<span data-ttu-id="ce221-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ce221-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ce221-153">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="ce221-153">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="ce221-154">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ce221-154">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="ce221-155">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="ce221-155">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="ce221-156">JetSetTableSequential</span><span class="sxs-lookup"><span data-stu-id="ce221-156">JetSetTableSequential</span></span>](./jetsettablesequential-function.md)  
[<span data-ttu-id="ce221-157">JetStopService</span><span class="sxs-lookup"><span data-stu-id="ce221-157">JetStopService</span></span>](./jetstopservice-function.md)
