---
description: 深入瞭解： JetOSSnapshotTruncateLogInstance 函數
title: JetOSSnapshotTruncateLogInstance 函式
TOCTitle: JetOSSnapshotTruncateLogInstance Function
ms:assetid: ddc51957-5b89-4abf-9193-c34ef626a63e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294115(v=EXCHG.10)
ms:contentKeyID: 32765729
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLogInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cef30d012c28c809bb35d59a82fd596ba69bd175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689528"
---
# <a name="jetossnapshottruncateloginstance-function"></a><span data-ttu-id="83808-103">JetOSSnapshotTruncateLogInstance 函式</span><span class="sxs-lookup"><span data-stu-id="83808-103">JetOSSnapshotTruncateLogInstance Function</span></span>


<span data-ttu-id="83808-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="83808-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshottruncateloginstance-function"></a><span data-ttu-id="83808-105">JetOSSnapshotTruncateLogInstance 函式</span><span class="sxs-lookup"><span data-stu-id="83808-105">JetOSSnapshotTruncateLogInstance Function</span></span>

<span data-ttu-id="83808-106">**JetOSSnapshotTruncateLogInstance** 函式會在快照會話期間截斷指定之實例的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="83808-106">The **JetOSSnapshotTruncateLogInstance** function truncates the log for a specified instance during a snapshot session.</span></span>

<span data-ttu-id="83808-107">**Windows vista：**  **JetOSSnapshotTruncateLogInstance** 是在 windows vista 中引進的。</span><span class="sxs-lookup"><span data-stu-id="83808-107">**Windows Vista:**  **JetOSSnapshotTruncateLogInstance** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLogInstance(
      __in          const JET_OSSNAPID snapId,
      __in          JET_INSTANCE instance,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="83808-108">參數</span><span class="sxs-lookup"><span data-stu-id="83808-108">Parameters</span></span>

<span data-ttu-id="83808-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="83808-109">*snapId*</span></span>

<span data-ttu-id="83808-110">快照集會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="83808-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="83808-111">*實例*</span><span class="sxs-lookup"><span data-stu-id="83808-111">*instance*</span></span>

<span data-ttu-id="83808-112">此呼叫將使用的實例。</span><span class="sxs-lookup"><span data-stu-id="83808-112">The instance that will be used for this call.</span></span>

<span data-ttu-id="83808-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="83808-113">*grbit*</span></span>

<span data-ttu-id="83808-114">此呼叫的選項。</span><span class="sxs-lookup"><span data-stu-id="83808-114">The options for this call.</span></span> <span data-ttu-id="83808-115">這個參數可以有下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="83808-115">This parameter can have a combination of the following values.</span></span>

<span data-ttu-id="83808-116">*grbit* 可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="83808-116">*grbit* can be one of the following values:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="83808-117">值</span><span class="sxs-lookup"><span data-stu-id="83808-117">Value</span></span></p></th>
<th><p><span data-ttu-id="83808-118">意義</span><span class="sxs-lookup"><span data-stu-id="83808-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="83808-119">JET_bitAllDatabasesSnapshot</span><span class="sxs-lookup"><span data-stu-id="83808-119">JET_bitAllDatabasesSnapshot</span></span></p></td>
<td><p><span data-ttu-id="83808-120">附加所有資料庫，讓儲存引擎可以計算並進行記錄截斷。</span><span class="sxs-lookup"><span data-stu-id="83808-120">All the databases are attached so the storage engine can compute and do the log truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83808-121">0 (零)</span><span class="sxs-lookup"><span data-stu-id="83808-121">0 (zero)</span></span></p></td>
<td><p><span data-ttu-id="83808-122">不會發生截斷。</span><span class="sxs-lookup"><span data-stu-id="83808-122">No truncation will occur.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="83808-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="83808-123">Return Value</span></span>

<span data-ttu-id="83808-124">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="83808-124">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="83808-125">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="83808-125">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="83808-126">傳回碼</span><span class="sxs-lookup"><span data-stu-id="83808-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="83808-127">Description</span><span class="sxs-lookup"><span data-stu-id="83808-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="83808-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="83808-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="83808-129">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="83808-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83808-130">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="83808-130">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="83808-131"><em>Grbit</em>參數無效。</span><span class="sxs-lookup"><span data-stu-id="83808-131">The <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83808-132">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="83808-132">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="83808-133">快照會話不是處於截斷可能發生的狀態。</span><span class="sxs-lookup"><span data-stu-id="83808-133">The snapshot session is not in the state in which a truncation can occur.</span></span> <span data-ttu-id="83808-134">可能的原因包括：</span><span class="sxs-lookup"><span data-stu-id="83808-134">Possible causes are:</span></span></p>
<ul>
<li><p><span data-ttu-id="83808-135">呼叫會在快照集會話超時之後完成。</span><span class="sxs-lookup"><span data-stu-id="83808-135">The call completes after the snapshot session timed out.</span></span></p></li>
<li><p><span data-ttu-id="83808-136">此會話已指定為複製快照集。</span><span class="sxs-lookup"><span data-stu-id="83808-136">The session was specified as a copy snapshot.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="83808-137">如果此函式成功，則會截斷屬於快照會話一部分的一個或所有實例的記錄檔（如果可能的話）。</span><span class="sxs-lookup"><span data-stu-id="83808-137">If this function succeeds, the log files for one or all of the instances that are part of the snapshot session will be truncated, if possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="83808-138">備註</span><span class="sxs-lookup"><span data-stu-id="83808-138">Remarks</span></span>

<span data-ttu-id="83808-139">只有在使用 JET_bitContinueAfterThaw 選項建立快照集時，才應該呼叫這個函數。</span><span class="sxs-lookup"><span data-stu-id="83808-139">This function should be called only if the snapshot was created with the JET_bitContinueAfterThaw option.</span></span> <span data-ttu-id="83808-140">否則，快照集會話會在呼叫 [JetOSSnapshotThaw](./jetossnapshotthaw-function.md)之後結束。</span><span class="sxs-lookup"><span data-stu-id="83808-140">Otherwise, the snapshot session ends after the call to [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="83808-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="83808-141">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="83808-142"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="83808-142"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="83808-143">需要 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="83808-143">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83808-144"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="83808-144"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="83808-145">需要 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="83808-145">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83808-146"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="83808-146"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="83808-147">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="83808-147">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83808-148"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="83808-148"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="83808-149">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="83808-149">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83808-150"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="83808-150"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="83808-151">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="83808-151">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="83808-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83808-152">See Also</span></span>

[<span data-ttu-id="83808-153">錯誤處理參數</span><span class="sxs-lookup"><span data-stu-id="83808-153">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="83808-154">可擴充儲存引擎錯誤</span><span class="sxs-lookup"><span data-stu-id="83808-154">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="83808-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="83808-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="83808-156">JetOSSnapshotEnd</span><span class="sxs-lookup"><span data-stu-id="83808-156">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="83808-157">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="83808-157">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="83808-158">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="83808-158">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="83808-159">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="83808-159">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
