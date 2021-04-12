---
description: 深入瞭解： JetOSSnapshotPrepareInstance 函數
title: JetOSSnapshotPrepareInstance 函式
TOCTitle: JetOSSnapshotPrepareInstance Function
ms:assetid: b4f06342-633f-47c6-be32-64ec058920fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294064(v=EXCHG.10)
ms:contentKeyID: 32765679
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepareInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8cc5179a55aabfa3324e3caab7005f4abe437a6d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104386536"
---
# <a name="jetossnapshotprepareinstance-function"></a><span data-ttu-id="77033-103">JetOSSnapshotPrepareInstance 函式</span><span class="sxs-lookup"><span data-stu-id="77033-103">JetOSSnapshotPrepareInstance Function</span></span>


<span data-ttu-id="77033-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="77033-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotprepareinstance-function"></a><span data-ttu-id="77033-105">JetOSSnapshotPrepareInstance 函式</span><span class="sxs-lookup"><span data-stu-id="77033-105">JetOSSnapshotPrepareInstance Function</span></span>

<span data-ttu-id="77033-106">**JetOSSnapshotPrepareInstance** 函式會選取要成為快照會話一部分的特定實例。</span><span class="sxs-lookup"><span data-stu-id="77033-106">The **JetOSSnapshotPrepareInstance** function selects a specific instance to be part of the snapshot session.</span></span>

<span data-ttu-id="77033-107">**Windows vista：** **JetOSSnapshotPrepareInstance** 是在 windows vista 中引進的。</span><span class="sxs-lookup"><span data-stu-id="77033-107">**Windows Vista:** **JetOSSnapshotPrepareInstance** was introduced in Windows Vista.</span></span>

```cpp
JET_ERR JET_API JetOSSnapshotPrepareInstance(
  __in          JET_OSSNAPID snapId,
  __in          JET_INSTANCE instance,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="77033-108">參數</span><span class="sxs-lookup"><span data-stu-id="77033-108">Parameters</span></span>

<span data-ttu-id="77033-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="77033-109">*snapId*</span></span>

<span data-ttu-id="77033-110">快照集會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="77033-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="77033-111">*實例*</span><span class="sxs-lookup"><span data-stu-id="77033-111">*instance*</span></span>

<span data-ttu-id="77033-112">此呼叫將使用的實例。</span><span class="sxs-lookup"><span data-stu-id="77033-112">The instance that will be used for this call.</span></span>

<span data-ttu-id="77033-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="77033-113">*grbit*</span></span>

<span data-ttu-id="77033-114">此呼叫的選項。</span><span class="sxs-lookup"><span data-stu-id="77033-114">The options for this call.</span></span> <span data-ttu-id="77033-115">這個參數保留給未來使用。</span><span class="sxs-lookup"><span data-stu-id="77033-115">This parameter is reserved for future use.</span></span> <span data-ttu-id="77033-116">唯一有效的值為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="77033-116">The only valid value is 0 (zero).</span></span>

### <a name="return-value"></a><span data-ttu-id="77033-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="77033-117">Return Value</span></span>

<span data-ttu-id="77033-118">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="77033-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="77033-119">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="77033-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="77033-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="77033-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="77033-121">Description</span><span class="sxs-lookup"><span data-stu-id="77033-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77033-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="77033-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="77033-123">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="77033-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77033-124">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="77033-124">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="77033-125">快照集識別碼指標為 <strong>Null</strong> 或 <em>grbit</em> 參數無效。</span><span class="sxs-lookup"><span data-stu-id="77033-125">The snapshot id pointer is <strong>NULL</strong> or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77033-126">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="77033-126">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="77033-127">快照會話已在進行中。</span><span class="sxs-lookup"><span data-stu-id="77033-127">A snapshot session is already in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77033-128">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="77033-128">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="77033-129">快照集會話的識別碼無效。</span><span class="sxs-lookup"><span data-stu-id="77033-129">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="77033-130">如果此函式成功，則指定的實例將會是快照集會話的一部分。</span><span class="sxs-lookup"><span data-stu-id="77033-130">If this function succeeds, the specified instance will be part of the snapshot session.</span></span>

<span data-ttu-id="77033-131">如果此函式失敗，則不會發生引擎狀態的變更。</span><span class="sxs-lookup"><span data-stu-id="77033-131">If this function fails, no change in the engine state occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="77033-132">備註</span><span class="sxs-lookup"><span data-stu-id="77033-132">Remarks</span></span>

<span data-ttu-id="77033-133">一般 API 順序呼叫是： [JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)，並選擇性地接著一或多個 **JetOSSnapshotPrepareInstance** 呼叫，然後再接著 [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)。</span><span class="sxs-lookup"><span data-stu-id="77033-133">The normal API sequence call is: [JetOSSnapshotPrepare](./jetossnapshotprepare-function.md), optionally followed by one or more calls to **JetOSSnapshotPrepareInstance**, then followed by [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md).</span></span> <span data-ttu-id="77033-134">當凍結開始之後，就可以使用 [JetOSSnapshotThaw](./jetossnapshotthaw-function.md)來終止。</span><span class="sxs-lookup"><span data-stu-id="77033-134">Once the freeze is started, it can be terminated using [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span></span> <span data-ttu-id="77033-135">在準備之後的任何時間，快照集會話都可以使用 [JetOSSnapshotAbort](./jetossnapshotabort-function.md)突然終止。</span><span class="sxs-lookup"><span data-stu-id="77033-135">At any time after the prepare, the snapshot session can be abruptly terminated with [JetOSSnapshotAbort](./jetossnapshotabort-function.md).</span></span> <span data-ttu-id="77033-136">將會產生快照集不同步驟的事件記錄檔專案。</span><span class="sxs-lookup"><span data-stu-id="77033-136">Event log entries will be generated for the different steps of the snapshot.</span></span>

<span data-ttu-id="77033-137">如果在會話開始 ([JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)) 和凍結時間 ([JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)) 之間沒有呼叫 **JetOSSnapshotPrepareInstance** ，則引擎中所有執行中的實例都會凍結，並且成為快照會話的一部分。</span><span class="sxs-lookup"><span data-stu-id="77033-137">If **JetOSSnapshotPrepareInstance** is not called between the start of the session ([JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)) and the freeze moment ([JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)), all the running instances in the engine will freeze and become part of the snapshot session.</span></span> <span data-ttu-id="77033-138">發生這種情況的原因有兩種：</span><span class="sxs-lookup"><span data-stu-id="77033-138">This occurs for two reasons:</span></span>

  - <span data-ttu-id="77033-139">它可為想要所有實例的使用者簡化程式碼。</span><span class="sxs-lookup"><span data-stu-id="77033-139">It simplifies the code for users who want all instances.</span></span>

  - <span data-ttu-id="77033-140">它允許快照集 Api 的呼叫端回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="77033-140">It allows backward compatibility for the callers of the snapshot APIs.</span></span>

#### <a name="requirements"></a><span data-ttu-id="77033-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="77033-141">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77033-142"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="77033-142"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="77033-143">需要 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="77033-143">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77033-144"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="77033-144"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="77033-145">需要 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="77033-145">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77033-146"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="77033-146"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="77033-147">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="77033-147">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77033-148"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="77033-148"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="77033-149">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="77033-149">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77033-150"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="77033-150"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="77033-151">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="77033-151">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="77033-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77033-152">See Also</span></span>

[<span data-ttu-id="77033-153">錯誤處理參數</span><span class="sxs-lookup"><span data-stu-id="77033-153">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="77033-154">可擴充儲存引擎錯誤</span><span class="sxs-lookup"><span data-stu-id="77033-154">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="77033-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="77033-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="77033-156">JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="77033-156">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="77033-157">JetOSSnapshotEnd</span><span class="sxs-lookup"><span data-stu-id="77033-157">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="77033-158">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="77033-158">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="77033-159">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="77033-159">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="77033-160">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="77033-160">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
