---
description: 深入瞭解： JetOSSnapshotEnd 函數
title: JetOSSnapshotEnd 函式
TOCTitle: JetOSSnapshotEnd Function
ms:assetid: f7f4db8b-8e40-48d7-bc7b-0c80d0d0f77f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294136(v=EXCHG.10)
ms:contentKeyID: 32765750
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotEnd
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de1237de9af0b1b75f645346fc30a128a1b8e907
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112053"
---
# <a name="jetossnapshotend-function"></a><span data-ttu-id="56a79-103">JetOSSnapshotEnd 函式</span><span class="sxs-lookup"><span data-stu-id="56a79-103">JetOSSnapshotEnd Function</span></span>


<span data-ttu-id="56a79-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="56a79-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotend-function"></a><span data-ttu-id="56a79-105">JetOSSnapshotEnd 函式</span><span class="sxs-lookup"><span data-stu-id="56a79-105">JetOSSnapshotEnd Function</span></span>

<span data-ttu-id="56a79-106">**JetOSSnapshotEnd** 函數會通知引擎快照會話已完成。</span><span class="sxs-lookup"><span data-stu-id="56a79-106">The **JetOSSnapshotEnd** function notifies the engine that the snapshot session finished.</span></span>

<span data-ttu-id="56a79-107">**Windows vista：**  **JetOSSnapshotEnd** 是在 windows vista 中引進：</span><span class="sxs-lookup"><span data-stu-id="56a79-107">**Windows Vista:**  **JetOSSnapshotEnd** is introduced in Windows Vista:.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotEnd(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="56a79-108">參數</span><span class="sxs-lookup"><span data-stu-id="56a79-108">Parameters</span></span>

<span data-ttu-id="56a79-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="56a79-109">*snapId*</span></span>

<span data-ttu-id="56a79-110">快照集會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="56a79-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="56a79-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="56a79-111">*grbit*</span></span>

<span data-ttu-id="56a79-112">此呼叫的選項。</span><span class="sxs-lookup"><span data-stu-id="56a79-112">The options for this call.</span></span> <span data-ttu-id="56a79-113">這個參數可以有下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="56a79-113">This parameter can have a combination of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="56a79-114">值</span><span class="sxs-lookup"><span data-stu-id="56a79-114">Value</span></span></p></th>
<th><p><span data-ttu-id="56a79-115">意義</span><span class="sxs-lookup"><span data-stu-id="56a79-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56a79-116">0</span><span class="sxs-lookup"><span data-stu-id="56a79-116">0</span></span></p></td>
<td><p><span data-ttu-id="56a79-117">快照集會話的成功結束。</span><span class="sxs-lookup"><span data-stu-id="56a79-117">The successful end of the snapshot session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56a79-118">JET_bitAbortSnapshot</span><span class="sxs-lookup"><span data-stu-id="56a79-118">JET_bitAbortSnapshot</span></span></p></td>
<td><p><span data-ttu-id="56a79-119">快照會話已中止。</span><span class="sxs-lookup"><span data-stu-id="56a79-119">The snapshot session aborted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="56a79-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="56a79-120">Return Value</span></span>

<span data-ttu-id="56a79-121">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="56a79-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="56a79-122">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="56a79-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="56a79-123">傳回碼</span><span class="sxs-lookup"><span data-stu-id="56a79-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="56a79-124">Description</span><span class="sxs-lookup"><span data-stu-id="56a79-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56a79-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="56a79-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="56a79-126">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="56a79-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56a79-127">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="56a79-127">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="56a79-128">其中一個要求的選項無效、使用不正確或未執行。</span><span class="sxs-lookup"><span data-stu-id="56a79-128">One of the options requested is invalid, used incorrectly, or not implemented.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56a79-129">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="56a79-129">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="56a79-130">快照會話已在進行中。</span><span class="sxs-lookup"><span data-stu-id="56a79-130">A snapshot session is already in progress.</span></span> <span data-ttu-id="56a79-131">這是不允許的。</span><span class="sxs-lookup"><span data-stu-id="56a79-131">This is not allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56a79-132">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="56a79-132">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="56a79-133">快照集會話的識別碼無效。</span><span class="sxs-lookup"><span data-stu-id="56a79-133">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56a79-134">JET_errOSSnapshotTimeOut</span><span class="sxs-lookup"><span data-stu-id="56a79-134">JET_errOSSnapshotTimeOut</span></span></p></td>
<td><p><span data-ttu-id="56a79-135">快照會話發生此呼叫之前的內部超時時間。</span><span class="sxs-lookup"><span data-stu-id="56a79-135">The snapshot session had an internal timeout before this call occurred.</span></span> <span data-ttu-id="56a79-136">如此一來，在進行此呼叫之前，IO 作業會恢復正常。</span><span class="sxs-lookup"><span data-stu-id="56a79-136">As a result, the IO operations returned to normal before this call was made.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="56a79-137">如果此函式成功，則快照集會話將會完成，而且會繼續正常的引擎行為。</span><span class="sxs-lookup"><span data-stu-id="56a79-137">If this function succeeds, a snapshot session will complete and the normal engine behavior will resume.</span></span> <span data-ttu-id="56a79-138">新的快照集會話稍後可以啟動。</span><span class="sxs-lookup"><span data-stu-id="56a79-138">A new snapshot session can be started later.</span></span>

<span data-ttu-id="56a79-139">如果此函式失敗，則會傳回 JET_errOSSnapshotTimeOut 傳回碼，而且目前的快照會話會結束，但在快照集期間，不會在內部遵守 IOs 的凍結。</span><span class="sxs-lookup"><span data-stu-id="56a79-139">If this function fails, the JET_errOSSnapshotTimeOut return code returns and the current snapshot session ends but the freeze of IOs during the snapshot period was not respected internally.</span></span> <span data-ttu-id="56a79-140">若為所有其他錯誤，則不會變更快照集會話狀態。</span><span class="sxs-lookup"><span data-stu-id="56a79-140">For all other errors, the snapshot session state will not be changed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="56a79-141">備註</span><span class="sxs-lookup"><span data-stu-id="56a79-141">Remarks</span></span>

<span data-ttu-id="56a79-142">只有在使用 JET_bitContinueAfterThaw 呼叫 [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) 時，才會呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="56a79-142">This function is called only if [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) was called with JET_bitContinueAfterThaw.</span></span>

<span data-ttu-id="56a79-143">您必須完成快照集會話，快照集驗證和記錄截斷才會發生。</span><span class="sxs-lookup"><span data-stu-id="56a79-143">The snapshot session must complete for the snapshot verification and log truncation to take place.</span></span> <span data-ttu-id="56a79-144">將會產生快照集不同步驟的事件記錄檔專案。</span><span class="sxs-lookup"><span data-stu-id="56a79-144">Event log entries will be generated for the different steps of the snapshot.</span></span>

#### <a name="requirements"></a><span data-ttu-id="56a79-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="56a79-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56a79-146"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="56a79-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="56a79-147">需要 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="56a79-147">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56a79-148"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="56a79-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="56a79-149">需要 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="56a79-149">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56a79-150"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="56a79-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="56a79-151">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="56a79-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56a79-152"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="56a79-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="56a79-153">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="56a79-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56a79-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="56a79-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="56a79-155">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="56a79-155">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="56a79-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="56a79-156">See Also</span></span>

[<span data-ttu-id="56a79-157">錯誤處理參數</span><span class="sxs-lookup"><span data-stu-id="56a79-157">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="56a79-158">可擴充儲存引擎錯誤</span><span class="sxs-lookup"><span data-stu-id="56a79-158">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="56a79-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="56a79-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="56a79-160">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="56a79-160">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
