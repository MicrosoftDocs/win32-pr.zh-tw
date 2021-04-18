---
description: 深入瞭解： JetOSSnapshotPrepare 函數
title: JetOSSnapshotPrepare 函式
TOCTitle: JetOSSnapshotPrepare Function
ms:assetid: 364cbcba-7ddb-4748-8417-e885a5984b0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269224(v=EXCHG.10)
ms:contentKeyID: 32765526
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepare
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 67ccf9a5b21ccb9a4f94ba5aa4f995e4bb9017bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971510"
---
# <a name="jetossnapshotprepare-function"></a><span data-ttu-id="f7528-103">JetOSSnapshotPrepare 函式</span><span class="sxs-lookup"><span data-stu-id="f7528-103">JetOSSnapshotPrepare Function</span></span>


<span data-ttu-id="f7528-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f7528-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotprepare-function"></a><span data-ttu-id="f7528-105">JetOSSnapshotPrepare 函式</span><span class="sxs-lookup"><span data-stu-id="f7528-105">JetOSSnapshotPrepare Function</span></span>

<span data-ttu-id="f7528-106">**JetOSSnapshotPrepare** 函式會開始快照集會話的準備工作。</span><span class="sxs-lookup"><span data-stu-id="f7528-106">The **JetOSSnapshotPrepare** function begins the preparations for a snapshot session.</span></span> <span data-ttu-id="f7528-107">快照集會話是一個短暫的時間間隔，在此時間間隔中，引擎不會將任何寫入 Io 發出至磁片，因此引擎可以在由快照寫入器驅動) 時，參與磁片區快照集會話 (。</span><span class="sxs-lookup"><span data-stu-id="f7528-107">A snapshot session is a short time interval in which the engine does not issue any write IOs to disk, so that the engine can participate in a volume snapshot session (when driven by a snapshot writer).</span></span>

<span data-ttu-id="f7528-108">**Windows xp：**  **JetOSSnapshotPrepare** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="f7528-108">**Windows XP:**  **JetOSSnapshotPrepare** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotPrepare(
      __out         JET_OSSNAPID* psnapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="f7528-109">參數</span><span class="sxs-lookup"><span data-stu-id="f7528-109">Parameters</span></span>

<span data-ttu-id="f7528-110">*psnapId*</span><span class="sxs-lookup"><span data-stu-id="f7528-110">*psnapId*</span></span>

<span data-ttu-id="f7528-111">要啟動之快照集會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f7528-111">The identifier of the snapshot session to be started.</span></span>

<span data-ttu-id="f7528-112">*grbit*</span><span class="sxs-lookup"><span data-stu-id="f7528-112">*grbit*</span></span>

<span data-ttu-id="f7528-113">此呼叫的選項。</span><span class="sxs-lookup"><span data-stu-id="f7528-113">The options for this call.</span></span> <span data-ttu-id="f7528-114">這個參數可以有下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="f7528-114">This parameter can have a combination of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f7528-115">值</span><span class="sxs-lookup"><span data-stu-id="f7528-115">Value</span></span></p></th>
<th><p><span data-ttu-id="f7528-116">意義</span><span class="sxs-lookup"><span data-stu-id="f7528-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7528-117">0</span><span class="sxs-lookup"><span data-stu-id="f7528-117">0</span></span></p></td>
<td><p><span data-ttu-id="f7528-118">一般快照集。</span><span class="sxs-lookup"><span data-stu-id="f7528-118">Normal snapshot.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7528-119">JET_bitIncrementalSnapshot</span><span class="sxs-lookup"><span data-stu-id="f7528-119">JET_bitIncrementalSnapshot</span></span></p></td>
<td><p><span data-ttu-id="f7528-120">只會取得記錄檔。</span><span class="sxs-lookup"><span data-stu-id="f7528-120">Only log files will be taken.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7528-121">JET_bitCopySnapshot</span><span class="sxs-lookup"><span data-stu-id="f7528-121">JET_bitCopySnapshot</span></span></p></td>
<td><p><span data-ttu-id="f7528-122">複製快照集 (一般或累加) ，而不會截斷記錄。</span><span class="sxs-lookup"><span data-stu-id="f7528-122">A copy snapshot (normal or incremental) with no log truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7528-123">JET_bitContinueAfterThaw</span><span class="sxs-lookup"><span data-stu-id="f7528-123">JET_bitContinueAfterThaw</span></span></p></td>
<td><p><span data-ttu-id="f7528-124">快照會話會在 <a href="gg269229(v=exchg.10).md">JetOSSnapshotThaw</a> 之後發生，而且需要 <a href="gg294136(v=exchg.10).md">JetOSSnapshotEnd</a> 函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="f7528-124">The snapshot session occurs after <a href="gg269229(v=exchg.10).md">JetOSSnapshotThaw</a> and will require a <a href="gg294136(v=exchg.10).md">JetOSSnapshotEnd</a> function call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7528-125">JET_bitExplicitPrepare</span><span class="sxs-lookup"><span data-stu-id="f7528-125">JET_bitExplicitPrepare</span></span></p></td>
<td><p><span data-ttu-id="f7528-126">預設不會準備任何實例。</span><span class="sxs-lookup"><span data-stu-id="f7528-126">No instances will be prepared by default.</span></span></p>
<p><span data-ttu-id="f7528-127"><strong>Windows 7：</strong>  JET_bitExplicitPrepare 是在 Windows 7 中引進的。</span><span class="sxs-lookup"><span data-stu-id="f7528-127"><strong>Windows 7:</strong>  JET_bitExplicitPrepare is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="f7528-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="f7528-128">Return Value</span></span>

<span data-ttu-id="f7528-129">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="f7528-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f7528-130">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="f7528-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f7528-131">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f7528-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="f7528-132">Description</span><span class="sxs-lookup"><span data-stu-id="f7528-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7528-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f7528-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f7528-134">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="f7528-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7528-135">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="f7528-135">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="f7528-136">快照集識別碼指標為 Null 或 <em>grbit</em> 參數無效。</span><span class="sxs-lookup"><span data-stu-id="f7528-136">The snapshot ID pointer is NULL or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7528-137">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="f7528-137">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="f7528-138">快照集會話已在進行中，而且在任何指定的時間，作業不允許有多個快照集會話。</span><span class="sxs-lookup"><span data-stu-id="f7528-138">A snapshot session is already in progress and the operation is not allowed to have more then one snapshot session at any given time.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f7528-139">如果此函式成功，則快照集會話將能夠在任何時間與 IO 凍結階段啟動。</span><span class="sxs-lookup"><span data-stu-id="f7528-139">If this function succeeds, a snapshot session will be able to start at any time with the IO freeze phase.</span></span> <span data-ttu-id="f7528-140">將會傳回會話的識別碼，而且必須在快照集會話的後續呼叫中使用。</span><span class="sxs-lookup"><span data-stu-id="f7528-140">The identifier for the session will be returned and must be used in the subsequent calls for the snapshot session.</span></span>

<span data-ttu-id="f7528-141">現在會將執行中的引擎實例視為快照會話的一部分。</span><span class="sxs-lookup"><span data-stu-id="f7528-141">The running instances of the engine will now be considered part of the snapshot session.</span></span>

<span data-ttu-id="f7528-142">**Windows Vista：**  若要指定不同的實例子集，可以呼叫 [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="f7528-142">**Windows Vista:**  To specify a different subset of instances, the [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md) can be called.</span></span>

<span data-ttu-id="f7528-143">一般 API 順序呼叫是： **JetOSSnapshotPrepare**，並選擇性地接著一或多個 [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)呼叫，然後再接著 [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)。</span><span class="sxs-lookup"><span data-stu-id="f7528-143">The normal API sequence call is: **JetOSSnapshotPrepare**, optionally followed by one or more calls to [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md), then followed by [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md).</span></span> <span data-ttu-id="f7528-144">當凍結開始之後，就可以使用 [JetOSSnapshotThaw](./jetossnapshotthaw-function.md)來終止。</span><span class="sxs-lookup"><span data-stu-id="f7528-144">Once the freeze is started, it can be terminated using [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span></span> <span data-ttu-id="f7528-145">在準備之後的任何時間，快照集會話都可以使用 [JetOSSnapshotAbort](./jetossnapshotabort-function.md)突然終止。</span><span class="sxs-lookup"><span data-stu-id="f7528-145">At any time after the prepare, the snapshot session can be abruptly terminated with [JetOSSnapshotAbort](./jetossnapshotabort-function.md).</span></span>

<span data-ttu-id="f7528-146">如果在 [JetOSSnapshotThaw](./jetossnapshotthaw-function.md)之後指定了 JET_bitContinueAfterThaw，快照會話將維持 (，不過 i/o 將繼續) 。</span><span class="sxs-lookup"><span data-stu-id="f7528-146">If JET_bitContinueAfterThaw is specified after [JetOSSnapshotThaw](./jetossnapshotthaw-function.md), the snapshot session will remain (although the I/O will resume).</span></span> <span data-ttu-id="f7528-147">這會啟用快照集的驗證，並在需要時，使用 [JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md) 啟用記錄截斷，而且需要呼叫 [JetOSSnapshotEnd](./jetossnapshotend-function.md)。</span><span class="sxs-lookup"><span data-stu-id="f7528-147">This will enable a verification of the snapshot, and if needed, will enable log truncation using [JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md) and will require a call to [JetOSSnapshotEnd](./jetossnapshotend-function.md).</span></span>

<span data-ttu-id="f7528-148">如果此函式失敗，則不會發生引擎狀態的變更。</span><span class="sxs-lookup"><span data-stu-id="f7528-148">If this function fails, no change in the engine state occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7528-149">備註</span><span class="sxs-lookup"><span data-stu-id="f7528-149">Remarks</span></span>

<span data-ttu-id="f7528-150">將會產生快照集不同步驟的事件記錄檔專案。</span><span class="sxs-lookup"><span data-stu-id="f7528-150">Event log entries will be generated for the different steps of the snapshot.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f7528-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7528-151">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7528-152"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="f7528-152"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f7528-153">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="f7528-153">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7528-154"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="f7528-154"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f7528-155">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="f7528-155">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7528-156"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="f7528-156"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f7528-157">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="f7528-157">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7528-158"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="f7528-158"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f7528-159">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="f7528-159">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7528-160"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f7528-160"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f7528-161">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="f7528-161">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f7528-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7528-162">See Also</span></span>

[<span data-ttu-id="f7528-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f7528-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f7528-164">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="f7528-164">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="f7528-165">JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="f7528-165">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="f7528-166">JetOSSnapshotEnd</span><span class="sxs-lookup"><span data-stu-id="f7528-166">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="f7528-167">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="f7528-167">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="f7528-168">JetOSSnapshotPrepareInstance</span><span class="sxs-lookup"><span data-stu-id="f7528-168">JetOSSnapshotPrepareInstance</span></span>](./jetossnapshotprepareinstance-function.md)  
[<span data-ttu-id="f7528-169">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="f7528-169">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)  
[<span data-ttu-id="f7528-170">JetOSSnapshotTruncateLog</span><span class="sxs-lookup"><span data-stu-id="f7528-170">JetOSSnapshotTruncateLog</span></span>](./jetossnapshottruncatelog-function.md)
