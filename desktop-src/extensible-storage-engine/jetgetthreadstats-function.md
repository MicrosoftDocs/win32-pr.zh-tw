---
description: 深入瞭解： JetGetThreadStats 函數
title: JetGetThreadStats 函式
TOCTitle: JetGetThreadStats Function
ms:assetid: 1b8df8cd-fc61-44fe-a15c-a166f7097c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269196(v=EXCHG.10)
ms:contentKeyID: 32765499
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetThreadStats
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 85d45021910f818f297cd0bc9829580a18b7a296
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971347"
---
# <a name="jetgetthreadstats-function"></a><span data-ttu-id="6136e-103">JetGetThreadStats 函式</span><span class="sxs-lookup"><span data-stu-id="6136e-103">JetGetThreadStats Function</span></span>


<span data-ttu-id="6136e-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6136e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetthreadstats-function"></a><span data-ttu-id="6136e-105">JetGetThreadStats 函式</span><span class="sxs-lookup"><span data-stu-id="6136e-105">JetGetThreadStats Function</span></span>

<span data-ttu-id="6136e-106">**JetGetThreadStats** 函式會從資料庫引擎取得目前線程的效能資訊。</span><span class="sxs-lookup"><span data-stu-id="6136e-106">The **JetGetThreadStats** function retrieves performance information from the database engine for the current thread.</span></span> <span data-ttu-id="6136e-107">您可以使用多個呼叫來收集統計資料，以反映這些呼叫之間的資料庫引擎在此執行緒上的活動。</span><span class="sxs-lookup"><span data-stu-id="6136e-107">Multiple calls can be used to collect statistics that reflect the activity of the database engine on this thread between those calls.</span></span>

<span data-ttu-id="6136e-108">**Windows vista：**  **JetGetThreadStats** 是在 windows vista 中引進的。</span><span class="sxs-lookup"><span data-stu-id="6136e-108">**Windows Vista:**  **JetGetThreadStats** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetGetThreadStats(
      __out         void* pvResult,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a><span data-ttu-id="6136e-109">參數</span><span class="sxs-lookup"><span data-stu-id="6136e-109">Parameters</span></span>

<span data-ttu-id="6136e-110">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="6136e-110">*pvResult*</span></span>

<span data-ttu-id="6136e-111">接收執行緒統計資料的輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6136e-111">The output buffer which receives the thread statistics data.</span></span> <span data-ttu-id="6136e-112">在成功呼叫之後，緩衝區會包含 [JET_THREADSTATS](./jet-threadstats-structure.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="6136e-112">The buffer contains a [JET_THREADSTATS](./jet-threadstats-structure.md) structure after a successful call.</span></span>

<span data-ttu-id="6136e-113">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="6136e-113">*cbMax*</span></span>

<span data-ttu-id="6136e-114">輸出緩衝區的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6136e-114">The maximum size in bytes of the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="6136e-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="6136e-115">Return Value</span></span>

<span data-ttu-id="6136e-116">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="6136e-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6136e-117">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="6136e-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6136e-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6136e-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="6136e-119">Description</span><span class="sxs-lookup"><span data-stu-id="6136e-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6136e-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6136e-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6136e-121">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="6136e-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6136e-122">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="6136e-122">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="6136e-123">因為提供的輸出緩衝區太小而無法包含要求的資料，所以作業失敗。</span><span class="sxs-lookup"><span data-stu-id="6136e-123">The operation failed because the provided output buffer was too small to contain the requested data.</span></span> <span data-ttu-id="6136e-124">當輸出緩衝區太小而無法包含 database engine 所支援之<a href="gg269227(v=exchg.10).md">JET_THREADSTATS</a>結構的最小版本時， <strong>JetGetThreadStats</strong>函數會傳回這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="6136e-124">The <strong>JetGetThreadStats</strong> function will return this error when the output buffer is too small to contain the smallest version of the <a href="gg269227(v=exchg.10).md">JET_THREADSTATS</a> structure supported by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6136e-125">成功時，輸出緩衝區將包含 [JET_THREADSTATS](./jet-threadstats-structure.md) 結構，其中包含目前線程的資料庫引擎統計資料。</span><span class="sxs-lookup"><span data-stu-id="6136e-125">On success, the output buffer will contain a [JET_THREADSTATS](./jet-threadstats-structure.md) structure that contains database engine statistics for the current thread.</span></span>

<span data-ttu-id="6136e-126">失敗時，輸出緩衝區的狀態是未定義的。</span><span class="sxs-lookup"><span data-stu-id="6136e-126">On failure, the state of the output buffer is undefined.</span></span>

#### <a name="remarks"></a><span data-ttu-id="6136e-127">備註</span><span class="sxs-lookup"><span data-stu-id="6136e-127">Remarks</span></span>

<span data-ttu-id="6136e-128">此 API 的兩個連續呼叫所提供的資訊，主要是用來計算目前線程上任何其他資料庫引擎作業的費用。</span><span class="sxs-lookup"><span data-stu-id="6136e-128">The information provided by two consecutive calls of this API are intended to be used to compute the expense of any other database engine operations on the current thread.</span></span> <span data-ttu-id="6136e-129">一般來說，這是藉由在讀取統計資料之前和之後減去，然後從 before count 減去 after count 來取得所執行作業的淨計數來完成。</span><span class="sxs-lookup"><span data-stu-id="6136e-129">Generally, this is done by taking a before and after reading of the statistics and subtracting the after count from the before count to get the net count of operations performed.</span></span>

<span data-ttu-id="6136e-130">例如，應用程式可以呼叫 **JetGetThreadStats** 一次，以取得目前線程之統計資料的初始讀取。</span><span class="sxs-lookup"><span data-stu-id="6136e-130">For example, an application could call **JetGetThreadStats** once to get an initial reading of the statistics for the current thread.</span></span> <span data-ttu-id="6136e-131">然後可以呼叫 [JetMove](./jetmove-function.md) 函式，並將 [ *魚尾紋* ] 參數設定為 JET_MoveNext，以移至索引上的下一個索引項目。</span><span class="sxs-lookup"><span data-stu-id="6136e-131">It could then call the [JetMove](./jetmove-function.md) function with the *cRow* parameter set to JET_MoveNext to move to the next index entry on an index.</span></span> <span data-ttu-id="6136e-132">然後，它可以再次呼叫 **JetGetThreadStats** ，以取得執行緒統計資料的另一個讀取。</span><span class="sxs-lookup"><span data-stu-id="6136e-132">It could then call **JetGetThreadStats** again to get another reading of the thread's statistics.</span></span> <span data-ttu-id="6136e-133">然後，它可以從第一次讀取時減去 cPageReferenced 計數器。</span><span class="sxs-lookup"><span data-stu-id="6136e-133">It could then subtract the cPageReferenced counter from the second reading from the first.</span></span> <span data-ttu-id="6136e-134">結果會是資料庫引擎參考用來執行 [JetMove](./jetmove-function.md) 作業的資料庫頁面數目。</span><span class="sxs-lookup"><span data-stu-id="6136e-134">The result would be the number of database pages referenced by the database engine to perform the [JetMove](./jetmove-function.md) operation.</span></span>

<span data-ttu-id="6136e-135">每個執行緒的統計資料會在該執行緒的存留期內累積。</span><span class="sxs-lookup"><span data-stu-id="6136e-135">The statistics for each thread are accumulated for the lifetime of that thread.</span></span> <span data-ttu-id="6136e-136">如果從主機進程卸載資料庫引擎的 DLL，則會重設統計資料。</span><span class="sxs-lookup"><span data-stu-id="6136e-136">The statistics are reset if the database engine's DLL is unloaded from the host process.</span></span>

<span data-ttu-id="6136e-137">未來可能會展開 [JET_THREADSTATS](./jet-threadstats-structure.md) 結構，以包含更多統計資料。</span><span class="sxs-lookup"><span data-stu-id="6136e-137">The [JET_THREADSTATS](./jet-threadstats-structure.md) structure will likely be expanded in the future to contain more statistics.</span></span> <span data-ttu-id="6136e-138">新的統計資料會加入至結構的結尾，而且可以使用增加的輸出緩衝區大小來抓取。</span><span class="sxs-lookup"><span data-stu-id="6136e-138">New statistics will be added to the end of the structure and can be retrieved with an increased output buffer size.</span></span> <span data-ttu-id="6136e-139">有更多的 cbStruct 值可以推斷出額外的統計資料。</span><span class="sxs-lookup"><span data-stu-id="6136e-139">The presence of additional statistics can be inferred by a larger cbStruct value.</span></span>

#### <a name="requirements"></a><span data-ttu-id="6136e-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="6136e-140">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6136e-141"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="6136e-141"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6136e-142">需要 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="6136e-142">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6136e-143"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="6136e-143"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6136e-144">需要 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="6136e-144">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6136e-145"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="6136e-145"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6136e-146">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="6136e-146">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6136e-147"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="6136e-147"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6136e-148">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="6136e-148">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6136e-149"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6136e-149"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6136e-150">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="6136e-150">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6136e-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6136e-151">See Also</span></span>

[<span data-ttu-id="6136e-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6136e-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6136e-153">JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="6136e-153">JET_THREADSTATS</span></span>](./jet-threadstats-structure.md)  
[<span data-ttu-id="6136e-154">JetMove</span><span class="sxs-lookup"><span data-stu-id="6136e-154">JetMove</span></span>](./jetmove-function.md)
