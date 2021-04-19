---
description: 深入瞭解： JetOSSnapshotGetFreezeInfo 函數
title: JetOSSnapshotGetFreezeInfo 函式
TOCTitle: JetOSSnapshotGetFreezeInfo Function
ms:assetid: b94eaf91-7407-4c62-ab1e-3249ad076c1a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294070(v=EXCHG.10)
ms:contentKeyID: 32765685
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotGetFreezeInfo
- JetOSSnapshotGetFreezeInfoA
- JetOSSnapshotGetFreezeInfoW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2fbfd3fb31567ea73b8266b5aeba506d62be7714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987282"
---
# <a name="jetossnapshotgetfreezeinfo-function"></a><span data-ttu-id="baa6c-103">JetOSSnapshotGetFreezeInfo 函式</span><span class="sxs-lookup"><span data-stu-id="baa6c-103">JetOSSnapshotGetFreezeInfo Function</span></span>


<span data-ttu-id="baa6c-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="baa6c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotgetfreezeinfo-function"></a><span data-ttu-id="baa6c-105">JetOSSnapshotGetFreezeInfo 函式</span><span class="sxs-lookup"><span data-stu-id="baa6c-105">JetOSSnapshotGetFreezeInfo Function</span></span>

<span data-ttu-id="baa6c-106">**JetOSSnapshotGetFreezeInfo** 函式會在任何指定的時間，取得屬於快照會話一部分的實例和資料庫清單。</span><span class="sxs-lookup"><span data-stu-id="baa6c-106">The **JetOSSnapshotGetFreezeInfo** function retrieves the list of instances and databases that are part of the snapshot session at any given moment.</span></span>

<span data-ttu-id="baa6c-107">**Windows vista：**  **JetOSSnapshotGetFreezeInfo** 是在 windows vista 中引進的。</span><span class="sxs-lookup"><span data-stu-id="baa6c-107">**Windows Vista:**  **JetOSSnapshotGetFreezeInfo** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotGetFreezeInfo(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="baa6c-108">參數</span><span class="sxs-lookup"><span data-stu-id="baa6c-108">Parameters</span></span>

<span data-ttu-id="baa6c-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="baa6c-109">*snapId*</span></span>

<span data-ttu-id="baa6c-110">要啟動之快照集會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="baa6c-110">The identifier of the snapshot session to be started.</span></span>

<span data-ttu-id="baa6c-111">*pcInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="baa6c-111">*pcInstanceInfo*</span></span>

<span data-ttu-id="baa6c-112">目前正在執行的實例數目，這些實例是快照集會話的一部分。</span><span class="sxs-lookup"><span data-stu-id="baa6c-112">The number of instances currently running that are part of the snapshot session.</span></span>

<span data-ttu-id="baa6c-113">*paInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="baa6c-113">*paInstanceInfo*</span></span>

<span data-ttu-id="baa6c-114">結構的陣列，每個執行中的實例各一個，描述其所屬的實例和資料庫。</span><span class="sxs-lookup"><span data-stu-id="baa6c-114">An array of structures, one for each running instance, describing the instance and the databases that are part of it.</span></span>

<span data-ttu-id="baa6c-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="baa6c-115">*grbit*</span></span>

<span data-ttu-id="baa6c-116">此呼叫的選項。</span><span class="sxs-lookup"><span data-stu-id="baa6c-116">The options for this call.</span></span> <span data-ttu-id="baa6c-117">這個參數保留給未來使用。</span><span class="sxs-lookup"><span data-stu-id="baa6c-117">This parameter is reserved for future use.</span></span> <span data-ttu-id="baa6c-118">唯一有效的值為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="baa6c-118">The only valid value is 0 (zero).</span></span>

### <a name="return-value"></a><span data-ttu-id="baa6c-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="baa6c-119">Return Value</span></span>

<span data-ttu-id="baa6c-120">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="baa6c-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="baa6c-121">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="baa6c-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="baa6c-122">傳回碼</span><span class="sxs-lookup"><span data-stu-id="baa6c-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="baa6c-123">Description</span><span class="sxs-lookup"><span data-stu-id="baa6c-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="baa6c-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="baa6c-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="baa6c-125">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="baa6c-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa6c-126">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="baa6c-126">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="baa6c-127">因為記憶體不足，所以函數失敗。</span><span class="sxs-lookup"><span data-stu-id="baa6c-127">The function failed due to an out-of-memory condition.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa6c-128">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="baa6c-128">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="baa6c-129"><em>pcInstanceInfo</em> 或 <em>paInstanceInfo</em> 為 <strong>Null</strong>。</span><span class="sxs-lookup"><span data-stu-id="baa6c-129"><em>pcInstanceInfo</em> or <em>paInstanceInfo</em> is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa6c-130">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="baa6c-130">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="baa6c-131">快照集會話的識別碼無效。</span><span class="sxs-lookup"><span data-stu-id="baa6c-131">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa6c-132">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="baa6c-132">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="baa6c-133">快照集會話不在進行中。</span><span class="sxs-lookup"><span data-stu-id="baa6c-133">A snapshot session is not in progress.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="baa6c-134">如果此函式成功，則會正確填滿實例資訊，而且必須在稍後使用傳回的實例資訊陣列的指標呼叫 [JetFreeBuffer](./jetfreebuffer-function.md) 來釋放。</span><span class="sxs-lookup"><span data-stu-id="baa6c-134">If this function succeeds, the instance information is properly filled and it must be freed later by calling [JetFreeBuffer](./jetfreebuffer-function.md) with the pointer to the instance info array that was returned.</span></span>

<span data-ttu-id="baa6c-135">如果此函式失敗，則不會發生引擎狀態的變更。</span><span class="sxs-lookup"><span data-stu-id="baa6c-135">If this function fails, no change in the engine state occurs.</span></span>

#### <a name="requirements"></a><span data-ttu-id="baa6c-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="baa6c-136">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="baa6c-137"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="baa6c-137"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="baa6c-138">需要 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="baa6c-138">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa6c-139"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="baa6c-139"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="baa6c-140">需要 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="baa6c-140">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa6c-141"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="baa6c-141"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="baa6c-142">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="baa6c-142">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa6c-143"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="baa6c-143"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="baa6c-144">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="baa6c-144">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baa6c-145"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="baa6c-145"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="baa6c-146">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="baa6c-146">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa6c-147"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="baa6c-147"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="baa6c-148">實作為 <strong>JetOSSnapshotGetFreezeInfoW</strong> (Unicode) 和 <strong>JetOSSnapshotGetFreezeInfoA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="baa6c-148">Implemented as <strong>JetOSSnapshotGetFreezeInfoW</strong> (Unicode) and <strong>JetOSSnapshotGetFreezeInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="baa6c-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="baa6c-149">See Also</span></span>

[<span data-ttu-id="baa6c-150">錯誤處理參數</span><span class="sxs-lookup"><span data-stu-id="baa6c-150">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="baa6c-151">可擴充儲存引擎錯誤</span><span class="sxs-lookup"><span data-stu-id="baa6c-151">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="baa6c-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="baa6c-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="baa6c-153">JetFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="baa6c-153">JetFreeBuffer</span></span>](./jetfreebuffer-function.md)  
[<span data-ttu-id="baa6c-154">JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="baa6c-154">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="baa6c-155">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="baa6c-155">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="baa6c-156">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="baa6c-156">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
