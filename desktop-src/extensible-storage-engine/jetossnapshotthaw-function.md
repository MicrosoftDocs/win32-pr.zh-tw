---
description: 深入瞭解： JetOSSnapshotThaw 函數
title: JetOSSnapshotThaw 函式
TOCTitle: JetOSSnapshotThaw Function
ms:assetid: 3b001113-6299-4082-ab15-461f2e33e996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269229(v=EXCHG.10)
ms:contentKeyID: 32765531
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotThaw
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: da7d5037cfc6b9a5f001dede57581127e4de60b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852824"
---
# <a name="jetossnapshotthaw-function"></a><span data-ttu-id="d18f7-103">JetOSSnapshotThaw 函式</span><span class="sxs-lookup"><span data-stu-id="d18f7-103">JetOSSnapshotThaw Function</span></span>


<span data-ttu-id="d18f7-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d18f7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotthaw-function"></a><span data-ttu-id="d18f7-105">JetOSSnapshotThaw 函式</span><span class="sxs-lookup"><span data-stu-id="d18f7-105">JetOSSnapshotThaw Function</span></span>

<span data-ttu-id="d18f7-106">**JetOSSnapshotThaw** 函式會通知引擎，它可以在凍結期間和成功的快照集之後繼續正常 IO 作業。</span><span class="sxs-lookup"><span data-stu-id="d18f7-106">The **JetOSSnapshotThaw** function notifies the engine that it can resume normal IO operations after a freeze period and a successful snapshot.</span></span>

<span data-ttu-id="d18f7-107">**Windows xp：**  **JetOSSnapshotThaw** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="d18f7-107">**Windows XP:**  **JetOSSnapshotThaw** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotThaw(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="d18f7-108">參數</span><span class="sxs-lookup"><span data-stu-id="d18f7-108">Parameters</span></span>

<span data-ttu-id="d18f7-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="d18f7-109">*snapId*</span></span>

<span data-ttu-id="d18f7-110">快照集會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d18f7-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="d18f7-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="d18f7-111">*grbit*</span></span>

<span data-ttu-id="d18f7-112">此參數已保留供日後使用，且唯一支援的有效值為0。</span><span class="sxs-lookup"><span data-stu-id="d18f7-112">This parameter is reserved for future use and the only valid value supported is 0.</span></span>

### <a name="return-value"></a><span data-ttu-id="d18f7-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d18f7-113">Return Value</span></span>

<span data-ttu-id="d18f7-114">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="d18f7-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d18f7-115">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="d18f7-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d18f7-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d18f7-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="d18f7-117">Description</span><span class="sxs-lookup"><span data-stu-id="d18f7-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d18f7-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d18f7-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d18f7-119">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="d18f7-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d18f7-120">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="d18f7-120">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="d18f7-121">快照集會話無效，或 <em>grbit</em> 參數無效。</span><span class="sxs-lookup"><span data-stu-id="d18f7-121">The snapshot session is invalid or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d18f7-122">JET_errOSSnapshotTimeOut</span><span class="sxs-lookup"><span data-stu-id="d18f7-122">JET_errOSSnapshotTimeOut</span></span></p></td>
<td><p><span data-ttu-id="d18f7-123">快照會話發生此呼叫之前的內部超時時間。</span><span class="sxs-lookup"><span data-stu-id="d18f7-123">The snapshot session had an internal timeout before this call occurred.</span></span> <span data-ttu-id="d18f7-124">因此，在進行此呼叫之前，IO 作業會恢復正常。</span><span class="sxs-lookup"><span data-stu-id="d18f7-124">Consequently, IO operations returned to normal before this call was made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d18f7-125">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="d18f7-125">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="d18f7-126">快照集會話的識別碼無效。</span><span class="sxs-lookup"><span data-stu-id="d18f7-126">The identifier for snapshot session is not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d18f7-127">如果此函式成功，快照集會話就會結束，而且會繼續正常的引擎行為。</span><span class="sxs-lookup"><span data-stu-id="d18f7-127">If this function succeeds, a snapshot session ends and the normal engine behavior resumes.</span></span> <span data-ttu-id="d18f7-128">新的快照集會話稍後可以啟動。</span><span class="sxs-lookup"><span data-stu-id="d18f7-128">A new snapshot session can be started later.</span></span>

<span data-ttu-id="d18f7-129">如果此函式失敗，則目前的快照會話會結束，但在快照集期間，不會在內部遵守 IOs 的凍結。</span><span class="sxs-lookup"><span data-stu-id="d18f7-129">If this function fails, the current snapshot session ends but the freeze of IOs during the snapshot period was not respected internally.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d18f7-130">備註</span><span class="sxs-lookup"><span data-stu-id="d18f7-130">Remarks</span></span>

<span data-ttu-id="d18f7-131">將會產生快照集不同步驟的事件記錄檔專案。</span><span class="sxs-lookup"><span data-stu-id="d18f7-131">Event log entries will be generated for the different steps of the snapshot.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d18f7-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="d18f7-132">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d18f7-133"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="d18f7-133"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d18f7-134">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="d18f7-134">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d18f7-135"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="d18f7-135"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d18f7-136">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="d18f7-136">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d18f7-137"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="d18f7-137"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d18f7-138">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="d18f7-138">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d18f7-139"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="d18f7-139"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d18f7-140">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="d18f7-140">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d18f7-141"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d18f7-141"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d18f7-142">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="d18f7-142">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d18f7-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d18f7-143">See Also</span></span>

[<span data-ttu-id="d18f7-144">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d18f7-144">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d18f7-145">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="d18f7-145">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="d18f7-146">JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="d18f7-146">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="d18f7-147">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="d18f7-147">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="d18f7-148">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="d18f7-148">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)
