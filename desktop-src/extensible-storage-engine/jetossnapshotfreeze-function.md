---
description: 深入瞭解： JetOSSnapshotFreeze 函數
title: JetOSSnapshotFreeze 函式
TOCTitle: JetOSSnapshotFreeze Function
ms:assetid: 8dfbff20-199e-4d89-a33c-ae8e39b11ec1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269332(v=EXCHG.10)
ms:contentKeyID: 32765622
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotFreezeA
- JetOSSnapshotFreezeW
- JetOSSnapshotFreeze
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cb6ea9a4a3145c0c4b3c3caeb3214b299ea1be85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193979"
---
# <a name="jetossnapshotfreeze-function"></a><span data-ttu-id="edab9-103">JetOSSnapshotFreeze 函式</span><span class="sxs-lookup"><span data-stu-id="edab9-103">JetOSSnapshotFreeze Function</span></span>


<span data-ttu-id="edab9-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="edab9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotfreeze-function"></a><span data-ttu-id="edab9-105">JetOSSnapshotFreeze 函式</span><span class="sxs-lookup"><span data-stu-id="edab9-105">JetOSSnapshotFreeze Function</span></span>

<span data-ttu-id="edab9-106">**JetOSSnapshotFreeze** 函式會啟動快照集。</span><span class="sxs-lookup"><span data-stu-id="edab9-106">The **JetOSSnapshotFreeze** function starts a snapshot.</span></span> <span data-ttu-id="edab9-107">當快照集進行中時，引擎無法進行寫入磁片的活動。</span><span class="sxs-lookup"><span data-stu-id="edab9-107">While the snapshot is in progress, no write-to-disk activity by the engine can take place.</span></span>

<span data-ttu-id="edab9-108">**Windows xp：**  **JetOSSnapshotFreeze** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="edab9-108">**Windows XP:**  **JetOSSnapshotFreeze** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotFreeze(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="edab9-109">參數</span><span class="sxs-lookup"><span data-stu-id="edab9-109">Parameters</span></span>

<span data-ttu-id="edab9-110">*snapId*</span><span class="sxs-lookup"><span data-stu-id="edab9-110">*snapId*</span></span>

<span data-ttu-id="edab9-111">快照集會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="edab9-111">The identifier of the snapshot session.</span></span>

<span data-ttu-id="edab9-112">*pcInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="edab9-112">*pcInstanceInfo*</span></span>

<span data-ttu-id="edab9-113">目前正在引擎中執行的實例數目，這些實例是快照集會話的一部分。</span><span class="sxs-lookup"><span data-stu-id="edab9-113">The number of instances currently running in the engine that are part of the snapshot session.</span></span>

<span data-ttu-id="edab9-114">*paInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="edab9-114">*paInstanceInfo*</span></span>

<span data-ttu-id="edab9-115">結構的陣列，每個正在執行的實例（屬於快照會話的一部分）都有一個，描述實例和所屬的資料庫。</span><span class="sxs-lookup"><span data-stu-id="edab9-115">An array of structures, one for each running instance that is part of the snapshot session, describing the instance and the databases that are part of it.</span></span>

<span data-ttu-id="edab9-116">*grbit*</span><span class="sxs-lookup"><span data-stu-id="edab9-116">*grbit*</span></span>

<span data-ttu-id="edab9-117">此呼叫的選項。</span><span class="sxs-lookup"><span data-stu-id="edab9-117">The options for this call.</span></span> <span data-ttu-id="edab9-118">此參數已保留供日後使用，且唯一支援的有效值為0。</span><span class="sxs-lookup"><span data-stu-id="edab9-118">This parameter is reserved for future use and the only valid value supported is 0.</span></span>

### <a name="return-value"></a><span data-ttu-id="edab9-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="edab9-119">Return Value</span></span>

<span data-ttu-id="edab9-120">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="edab9-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="edab9-121">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="edab9-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="edab9-122">傳回碼</span><span class="sxs-lookup"><span data-stu-id="edab9-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="edab9-123">Description</span><span class="sxs-lookup"><span data-stu-id="edab9-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="edab9-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="edab9-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="edab9-125">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="edab9-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edab9-126">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="edab9-126">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="edab9-127">提供給輸出參數的指標為 Null、快照集會話無效，或 <em>grbit</em> 參數無效。</span><span class="sxs-lookup"><span data-stu-id="edab9-127">The pointers provided for the output parameters are NULL, the snapshot session is invalid, or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edab9-128">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="edab9-128">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="edab9-129">快照會話不是處於適當的狀態，無法開始凍結 (例如，在) 之前，此會話上先前的凍結失敗。</span><span class="sxs-lookup"><span data-stu-id="edab9-129">The snapshot session is not in the appropriate state to start a freeze (for example, a previous freeze failed on this session before).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edab9-130">JET_errOSSnapshotNotAllowed</span><span class="sxs-lookup"><span data-stu-id="edab9-130">JET_errOSSnapshotNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="edab9-131">引擎未處於可以執行快照集的狀態。</span><span class="sxs-lookup"><span data-stu-id="edab9-131">The engine is not in a state in which a snapshot can be performed.</span></span> <span data-ttu-id="edab9-132">有一或多個串流備份已在進行中，或有一或多個實例正在進行復原步驟或正在終止。</span><span class="sxs-lookup"><span data-stu-id="edab9-132">Either one or more streaming backups is already in progress, or one or more instances are going through recovery steps or terminating.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edab9-133">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="edab9-133">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="edab9-134">快照集會話的識別碼無效。</span><span class="sxs-lookup"><span data-stu-id="edab9-134">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edab9-135">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="edab9-135">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="edab9-136">因為記憶體不足，所以函數失敗。</span><span class="sxs-lookup"><span data-stu-id="edab9-136">The function failed due to an out-of-memory condition.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edab9-137">JET_errOutOfThreads</span><span class="sxs-lookup"><span data-stu-id="edab9-137">JET_errOutOfThreads</span></span></p></td>
<td><p><span data-ttu-id="edab9-138">函數失敗，因為執行凍結的新執行緒無法啟動。</span><span class="sxs-lookup"><span data-stu-id="edab9-138">The function failed because a new thread doing the freeze failed to start.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="edab9-139">如果此函式成功，則不會有針對資料庫檔案或屬於已凍結實例一部分的記錄檔發出的任何寫入 Io。</span><span class="sxs-lookup"><span data-stu-id="edab9-139">If this function succeeds, there will not be any write IOs issued for the database files or for the log files that are part of instances that are frozen.</span></span> <span data-ttu-id="edab9-140">此外，系統會適當地填滿實例資訊，而且必須在稍後透過呼叫 [JetFreeBuffer](./jetfreebuffer-function.md) 以及傳回之實例資訊陣列的指標來釋放。</span><span class="sxs-lookup"><span data-stu-id="edab9-140">Also, the instance information will be properly filled and it must be freed later on by calling [JetFreeBuffer](./jetfreebuffer-function.md) with the pointer to the instance info array that was returned.</span></span>

<span data-ttu-id="edab9-141">如果此函式失敗，則引擎會正常運作，而 IOs 會正常運作。</span><span class="sxs-lookup"><span data-stu-id="edab9-141">If this function fails, the engine will keep running normally with the IOs occurring as usual.</span></span> <span data-ttu-id="edab9-142">如果凍結失敗，就不需要呼叫 [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="edab9-142">There is no need to call [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) if the freeze fails.</span></span> <span data-ttu-id="edab9-143">此外，將不會填入實例資訊，因此不需要釋放此資源。</span><span class="sxs-lookup"><span data-stu-id="edab9-143">Also, the instance information will not be filled so there is no need to free this resource.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edab9-144">備註</span><span class="sxs-lookup"><span data-stu-id="edab9-144">Remarks</span></span>

<span data-ttu-id="edab9-145">在凍結期間，將不會有任何發行至附加資料庫或交易記錄的寫入 Io，雖然可能會有寫入的 IOs 發行至暫存資料庫或串流檔案。</span><span class="sxs-lookup"><span data-stu-id="edab9-145">During the freeze period, there will not be any write IOs issued to the attached databases or the transaction logs, although there might be write IOs issued to the temporary databases or streaming files.</span></span>

<span data-ttu-id="edab9-146">資料庫和記錄檔在凍結期間的狀態 () 磁片區快照集映射中的檔案狀態，這樣一來，如果稍後再還原這些檔案，就可以正常復原。</span><span class="sxs-lookup"><span data-stu-id="edab9-146">The state in which the databases and the log files will be during the freeze (the state in which the files would be in a Volume Snapshot image) will be such that a normal recovery will be possible if those files are restored later.</span></span>

<span data-ttu-id="edab9-147">因為在凍結期間內沒有寫入作業，所以對引擎的一般 API 呼叫可能會在該間隔內停止。</span><span class="sxs-lookup"><span data-stu-id="edab9-147">Because there are no write operations during the freeze period, normal API calls into the engine might be stalled for that interval.</span></span> <span data-ttu-id="edab9-148">如果發生凍結，用戶端應用程式必須能夠處理可能需要較長時間的 API 呼叫。</span><span class="sxs-lookup"><span data-stu-id="edab9-148">The client application must be able to handle API calls that might take longer then normal if a freeze occurs.</span></span>

<span data-ttu-id="edab9-149">由於上述的可能效果，有一個內部的超時時間，在此時間之後，即使未呼叫執行解凍或中止的 Api，快照會話仍會停止凍結階段。</span><span class="sxs-lookup"><span data-stu-id="edab9-149">Due to the possible effects described above, there is an internal timeout after which the snapshot session will stop the freeze phase even if the APIs doing the thaw or abort were not called.</span></span> <span data-ttu-id="edab9-150">您可以使用 [JET_paramOSSnapshotTimeout](./backup-and-restore-parameters.md) 系統參數變更超時的值。</span><span class="sxs-lookup"><span data-stu-id="edab9-150">The value of the timeout can be changed using the [JET_paramOSSnapshotTimeout](./backup-and-restore-parameters.md) system parameter.</span></span> <span data-ttu-id="edab9-151">請注意，一般凍結間隔的範圍為10秒，預設超時時間大約是60秒。</span><span class="sxs-lookup"><span data-stu-id="edab9-151">Note that the typical freeze interval is in the range of 10 seconds with the default timeout somewhere around 60 seconds.</span></span>

#### <a name="requirements"></a><span data-ttu-id="edab9-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="edab9-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="edab9-153"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="edab9-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="edab9-154">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="edab9-154">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edab9-155"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="edab9-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="edab9-156">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="edab9-156">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edab9-157"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="edab9-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="edab9-158">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="edab9-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edab9-159"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="edab9-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="edab9-160">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="edab9-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edab9-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="edab9-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="edab9-162">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="edab9-162">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edab9-163"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="edab9-163"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="edab9-164">實作為 <strong>JetOSSnapshotFreezeW</strong> (Unicode) 和 <strong>JetOSSnapshotFreezeA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="edab9-164">Implemented as <strong>JetOSSnapshotFreezeW</strong> (Unicode) and <strong>JetOSSnapshotFreezeA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="edab9-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="edab9-165">See Also</span></span>

[<span data-ttu-id="edab9-166">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="edab9-166">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="edab9-167">JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="edab9-167">JET_INSTANCE_INFO</span></span>](./jet-instance-info-structure.md)  
[<span data-ttu-id="edab9-168">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="edab9-168">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="edab9-169">JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="edab9-169">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="edab9-170">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="edab9-170">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="edab9-171">JetOSSnapshotPrepareInstance</span><span class="sxs-lookup"><span data-stu-id="edab9-171">JetOSSnapshotPrepareInstance</span></span>](./jetossnapshotprepareinstance-function.md)  
[<span data-ttu-id="edab9-172">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="edab9-172">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
