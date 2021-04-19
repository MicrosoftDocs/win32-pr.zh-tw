---
description: 深入瞭解： JetOSSnapshotTruncateLog 函數
title: JetOSSnapshotTruncateLog 函式
TOCTitle: JetOSSnapshotTruncateLog Function
ms:assetid: 3df8f5b2-8083-49b7-a325-fd13187f785c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269231(v=EXCHG.10)
ms:contentKeyID: 32765533
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLog
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0a3cebd743a3c8cd9a3d86f1f637dcb5b2c9c91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977089"
---
# <a name="jetossnapshottruncatelog-function"></a><span data-ttu-id="91d18-103">JetOSSnapshotTruncateLog 函式</span><span class="sxs-lookup"><span data-stu-id="91d18-103">JetOSSnapshotTruncateLog Function</span></span>


<span data-ttu-id="91d18-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="91d18-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshottruncatelog-function"></a><span data-ttu-id="91d18-105">JetOSSnapshotTruncateLog 函式</span><span class="sxs-lookup"><span data-stu-id="91d18-105">JetOSSnapshotTruncateLog Function</span></span>

<span data-ttu-id="91d18-106">**JetOSSnapshotTruncateLog** 函數會針對屬於快照會話一部分的所有實例啟用記錄截斷。</span><span class="sxs-lookup"><span data-stu-id="91d18-106">The **JetOSSnapshotTruncateLog** function enables log truncation for all instances that are part of the snapshot session.</span></span>

<span data-ttu-id="91d18-107">**Windows vista：**  **JetOSSnapshotTruncateLog** 是在 windows vista 中引進的。</span><span class="sxs-lookup"><span data-stu-id="91d18-107">**Windows Vista:**  **JetOSSnapshotTruncateLog** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLog(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="91d18-108">參數</span><span class="sxs-lookup"><span data-stu-id="91d18-108">Parameters</span></span>

<span data-ttu-id="91d18-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="91d18-109">*snapId*</span></span>

<span data-ttu-id="91d18-110">快照集會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="91d18-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="91d18-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="91d18-111">*grbit*</span></span>

<span data-ttu-id="91d18-112">此呼叫的選項。</span><span class="sxs-lookup"><span data-stu-id="91d18-112">The options for this call.</span></span> <span data-ttu-id="91d18-113">這個參數可以有下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="91d18-113">This parameter can have a combination of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="91d18-114">值</span><span class="sxs-lookup"><span data-stu-id="91d18-114">Value</span></span></p></th>
<th><p><span data-ttu-id="91d18-115">意義</span><span class="sxs-lookup"><span data-stu-id="91d18-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91d18-116">JET_bitAllDatabasesSnapshot</span><span class="sxs-lookup"><span data-stu-id="91d18-116">JET_bitAllDatabasesSnapshot</span></span></p></td>
<td><p><span data-ttu-id="91d18-117">附加所有資料庫，讓儲存引擎可以計算並進行記錄截斷。</span><span class="sxs-lookup"><span data-stu-id="91d18-117">All the databases are attached so the storage engine can compute and do the log truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91d18-118">0 (零)</span><span class="sxs-lookup"><span data-stu-id="91d18-118">0 (zero)</span></span></p></td>
<td><p><span data-ttu-id="91d18-119">不會發生截斷。</span><span class="sxs-lookup"><span data-stu-id="91d18-119">No truncation will occur.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="91d18-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="91d18-120">Return Value</span></span>

<span data-ttu-id="91d18-121">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="91d18-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="91d18-122">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="91d18-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="91d18-123">傳回碼</span><span class="sxs-lookup"><span data-stu-id="91d18-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="91d18-124">Description</span><span class="sxs-lookup"><span data-stu-id="91d18-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91d18-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="91d18-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="91d18-126">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="91d18-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91d18-127">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="91d18-127">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="91d18-128"><em>Grbit</em>參數無效。</span><span class="sxs-lookup"><span data-stu-id="91d18-128">The <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91d18-129">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="91d18-129">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="91d18-130">快照會話不是處於截斷可能發生的狀態。</span><span class="sxs-lookup"><span data-stu-id="91d18-130">The snapshot session is not in the state in which a truncation can occur.</span></span> <span data-ttu-id="91d18-131">可能的原因包括：</span><span class="sxs-lookup"><span data-stu-id="91d18-131">Possible causes are:</span></span></p>
<ul>
<li><p><span data-ttu-id="91d18-132">呼叫是在快照集會話超時之後完成</span><span class="sxs-lookup"><span data-stu-id="91d18-132">the call is done after the snapshot session timed-out</span></span></p></li>
<li><p><span data-ttu-id="91d18-133">此會話已指定為複製快照集</span><span class="sxs-lookup"><span data-stu-id="91d18-133">the session was specified as a copy snapshot</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="91d18-134">成功時，如果可能的話，會截斷快照會話中一個或所有實例的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="91d18-134">On success, the log files for one or all the instances part of the snapshot session will be truncated, if possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="91d18-135">備註</span><span class="sxs-lookup"><span data-stu-id="91d18-135">Remarks</span></span>

<span data-ttu-id="91d18-136">只有在使用 JET_bitContinueAfterThaw 選項建立快照集時，才應該呼叫這個函數。</span><span class="sxs-lookup"><span data-stu-id="91d18-136">This function should be called only if the snapshot was created with the JET_bitContinueAfterThaw option.</span></span> <span data-ttu-id="91d18-137">否則，在 [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) 呼叫之後，快照集會話就會結束。</span><span class="sxs-lookup"><span data-stu-id="91d18-137">Otherwise, the snapshot session would have ended after the [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) call.</span></span>

#### <a name="requirements"></a><span data-ttu-id="91d18-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="91d18-138">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91d18-139"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="91d18-139"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="91d18-140">需要 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="91d18-140">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91d18-141"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="91d18-141"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="91d18-142">需要 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="91d18-142">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91d18-143"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="91d18-143"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="91d18-144">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="91d18-144">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91d18-145"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="91d18-145"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="91d18-146">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="91d18-146">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91d18-147"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="91d18-147"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="91d18-148">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="91d18-148">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="91d18-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91d18-149">See Also</span></span>

[<span data-ttu-id="91d18-150">錯誤處理參數</span><span class="sxs-lookup"><span data-stu-id="91d18-150">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="91d18-151">可擴充儲存引擎錯誤</span><span class="sxs-lookup"><span data-stu-id="91d18-151">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="91d18-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="91d18-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="91d18-153">JetOSSnapshotEnd</span><span class="sxs-lookup"><span data-stu-id="91d18-153">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="91d18-154">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="91d18-154">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="91d18-155">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="91d18-155">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="91d18-156">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="91d18-156">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
