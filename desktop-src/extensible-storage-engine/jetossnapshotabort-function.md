---
description: 深入瞭解： JetOSSnapshotAbort 函數
title: JetOSSnapshotAbort 函式
TOCTitle: JetOSSnapshotAbort Function
ms:assetid: 629455af-b526-4366-9b9a-112757f72c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269265(v=EXCHG.10)
ms:contentKeyID: 32765567
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotAbort
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d976f027a940bcf0199016d0e617d515273183ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975812"
---
# <a name="jetossnapshotabort-function"></a><span data-ttu-id="52a8c-103">JetOSSnapshotAbort 函式</span><span class="sxs-lookup"><span data-stu-id="52a8c-103">JetOSSnapshotAbort Function</span></span>


<span data-ttu-id="52a8c-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="52a8c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotabort-function"></a><span data-ttu-id="52a8c-105">JetOSSnapshotAbort 函式</span><span class="sxs-lookup"><span data-stu-id="52a8c-105">JetOSSnapshotAbort Function</span></span>

<span data-ttu-id="52a8c-106">**JetOSSnapshotAbort** 函式會通知引擎，在凍結期間結束為失敗的快照集之後，它可以繼續正常 IO 作業。</span><span class="sxs-lookup"><span data-stu-id="52a8c-106">The **JetOSSnapshotAbort** function notifies the engine that it can resume normal IO operations after a freeze period ended with a failed snapshot.</span></span>

<span data-ttu-id="52a8c-107">**Windows server 2003：**  **JetOSSnapshotAbort** 是在 windows server 2003 中引進。</span><span class="sxs-lookup"><span data-stu-id="52a8c-107">**Windows Server 2003:**  **JetOSSnapshotAbort** is introduced in Windows Server 2003.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotAbort(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="52a8c-108">參數</span><span class="sxs-lookup"><span data-stu-id="52a8c-108">Parameters</span></span>

<span data-ttu-id="52a8c-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="52a8c-109">*snapId*</span></span>

<span data-ttu-id="52a8c-110">快照集會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="52a8c-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="52a8c-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="52a8c-111">*grbit*</span></span>

<span data-ttu-id="52a8c-112">此呼叫的選項。</span><span class="sxs-lookup"><span data-stu-id="52a8c-112">The options for this call.</span></span> <span data-ttu-id="52a8c-113">此參數已保留供日後使用，且唯一支援的有效值為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="52a8c-113">This parameter is reserved for future use and the only valid value supported is 0 (zero).</span></span>

### <a name="return-value"></a><span data-ttu-id="52a8c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="52a8c-114">Return Value</span></span>

<span data-ttu-id="52a8c-115">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="52a8c-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="52a8c-116">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="52a8c-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="52a8c-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="52a8c-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="52a8c-118">Description</span><span class="sxs-lookup"><span data-stu-id="52a8c-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52a8c-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="52a8c-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="52a8c-120">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="52a8c-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52a8c-121">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="52a8c-121">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="52a8c-122">快照集會話無效，或 grbit 參數無效。</span><span class="sxs-lookup"><span data-stu-id="52a8c-122">The snapshot session is invalid or the grbit parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52a8c-123">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="52a8c-123">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="52a8c-124">快照集會話的識別碼無效。</span><span class="sxs-lookup"><span data-stu-id="52a8c-124">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="52a8c-125">如果此函式成功，則快照集會話將會結束，而且會繼續正常的引擎行為。</span><span class="sxs-lookup"><span data-stu-id="52a8c-125">If this function succeeds, the snapshot session will end and the normal engine behavior will resume.</span></span> <span data-ttu-id="52a8c-126">新的快照集會話可以在稍後的時間點啟動。</span><span class="sxs-lookup"><span data-stu-id="52a8c-126">A new snapshot session can be started at a later point.</span></span>

<span data-ttu-id="52a8c-127">如果此函式失敗，快照集會話將不會中止。</span><span class="sxs-lookup"><span data-stu-id="52a8c-127">If this function fails, the snapshot session will not be aborted.</span></span>

#### <a name="remarks"></a><span data-ttu-id="52a8c-128">備註</span><span class="sxs-lookup"><span data-stu-id="52a8c-128">Remarks</span></span>

<span data-ttu-id="52a8c-129">應該呼叫此函式，而不是 [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) ，以通知引擎快照集已因與引擎無關的原因而中止。</span><span class="sxs-lookup"><span data-stu-id="52a8c-129">This function should be called instead of [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) to inform the engine that the snapshot was aborted for reasons that don't relate to the engine.</span></span> <span data-ttu-id="52a8c-130">稍後可以使用此資訊來協助發出快照會話的事件記錄檔訊息，或協助判斷其他適當的動作。</span><span class="sxs-lookup"><span data-stu-id="52a8c-130">This information can be used later to help issue event log messages about the snapshot session or to help determine other appropriate actions.</span></span>

#### <a name="requirements"></a><span data-ttu-id="52a8c-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="52a8c-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52a8c-132"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="52a8c-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="52a8c-133">需要 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="52a8c-133">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52a8c-134"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="52a8c-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="52a8c-135">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="52a8c-135">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52a8c-136"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="52a8c-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="52a8c-137">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="52a8c-137">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52a8c-138"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="52a8c-138"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="52a8c-139">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="52a8c-139">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52a8c-140"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="52a8c-140"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="52a8c-141">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="52a8c-141">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="52a8c-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52a8c-142">See Also</span></span>

[<span data-ttu-id="52a8c-143">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="52a8c-143">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="52a8c-144">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="52a8c-144">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="52a8c-145">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="52a8c-145">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="52a8c-146">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="52a8c-146">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="52a8c-147">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="52a8c-147">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
