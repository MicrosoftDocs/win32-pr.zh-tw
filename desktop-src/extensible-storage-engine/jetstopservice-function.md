---
description: 深入瞭解： JetStopService 函數
title: JetStopService 函式
TOCTitle: JetStopService Function
ms:assetid: 46aeb9ed-ee72-49cc-99e3-791a51a55b02
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269240(v=EXCHG.10)
ms:contentKeyID: 32765542
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopService
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1e66b4e5242710c89ca7e7964ecd0a72774b719d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106995823"
---
# <a name="jetstopservice-function"></a><span data-ttu-id="585c3-103">JetStopService 函式</span><span class="sxs-lookup"><span data-stu-id="585c3-103">JetStopService Function</span></span>


<span data-ttu-id="585c3-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="585c3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetstopservice-function"></a><span data-ttu-id="585c3-105">JetStopService 函式</span><span class="sxs-lookup"><span data-stu-id="585c3-105">JetStopService Function</span></span>

<span data-ttu-id="585c3-106">**JetStopService** 函式會準備實例以進行終止。</span><span class="sxs-lookup"><span data-stu-id="585c3-106">The **JetStopService** function prepares an instance for termination.</span></span>

<span data-ttu-id="585c3-107">**JetStopService** 是僅允許一個實例時的舊版呼叫。</span><span class="sxs-lookup"><span data-stu-id="585c3-107">**JetStopService** is the legacy call when only one instance is allowed.</span></span> <span data-ttu-id="585c3-108">在此情況下，唯一的作用中實例是準備進行終止的實例。</span><span class="sxs-lookup"><span data-stu-id="585c3-108">In this case, the only active instance is the one being prepared for termination.</span></span>

```cpp
    JET_ERR JET_API JetStopService(void);
```

### <a name="parameters"></a><span data-ttu-id="585c3-109">參數</span><span class="sxs-lookup"><span data-stu-id="585c3-109">Parameters</span></span>

<span data-ttu-id="585c3-110">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="585c3-110">This function has no parameters.</span></span>

### <a name="return-value"></a><span data-ttu-id="585c3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="585c3-111">Return Value</span></span>

<span data-ttu-id="585c3-112">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="585c3-112">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="585c3-113">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="585c3-113">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="585c3-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="585c3-114">Return code</span></span></p></th>
<th><p><span data-ttu-id="585c3-115">Description</span><span class="sxs-lookup"><span data-stu-id="585c3-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="585c3-116">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="585c3-116">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="585c3-117">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="585c3-117">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="585c3-118">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="585c3-118">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="585c3-119">使用具有多個實例模式的 <strong>JetStopService</strong> 時，不會清除要準備終止的實例。</span><span class="sxs-lookup"><span data-stu-id="585c3-119">It is not clear which instance to prepare for termination when using <strong>JetStopService</strong> with multiple instance mode.</span></span></p>
<p><span data-ttu-id="585c3-120"><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="585c3-120"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="585c3-121">如果此函式成功，它會準備未來終止。</span><span class="sxs-lookup"><span data-stu-id="585c3-121">If this function succeeds, it prepares for a future termination.</span></span> <span data-ttu-id="585c3-122">針對終止進行準備所採取的步驟如下：</span><span class="sxs-lookup"><span data-stu-id="585c3-122">The steps taken to prepare for a termination include the following:</span></span>

  - <span data-ttu-id="585c3-123">如果正在執行，請停止線上磁碟重組。</span><span class="sxs-lookup"><span data-stu-id="585c3-123">Stop online defragmentation if it is running.</span></span>

  - <span data-ttu-id="585c3-124">啟動版本存放區清除。</span><span class="sxs-lookup"><span data-stu-id="585c3-124">Start a version store clean-up.</span></span>

  - <span data-ttu-id="585c3-125">藉由開始排清緩衝區管理員中的中途分頁，以降低檢查點深度。</span><span class="sxs-lookup"><span data-stu-id="585c3-125">Reduce the checkpoint depth by starting to flush dirty pages in the buffer manager.</span></span>

  - <span data-ttu-id="585c3-126">避免未來對該實例的大部分函式進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="585c3-126">Prevent future calls to most functions for that instance.</span></span>

<span data-ttu-id="585c3-127">如果此函式失敗，則不會執行準備實例終止的任何步驟，因此不會對實例狀態進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="585c3-127">If this function fails, none of the steps to prepare for an instance termination will be taken, so no change to the instance state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="585c3-128">備註</span><span class="sxs-lookup"><span data-stu-id="585c3-128">Remarks</span></span>

<span data-ttu-id="585c3-129">此函式會減少實例終止時必須執行的工作，但不會終止實例。</span><span class="sxs-lookup"><span data-stu-id="585c3-129">This function reduces the work the instance will have to do when terminated, but will not terminate the instance.</span></span> <span data-ttu-id="585c3-130">如此一來，此函式只是優化，而且不一定要使用。</span><span class="sxs-lookup"><span data-stu-id="585c3-130">As a result, this function is just an optimization and is not mandatory to use.</span></span> <span data-ttu-id="585c3-131">請注意，在 Windows 2000 和 Windows XP 中進行準備所需的工作量較小。</span><span class="sxs-lookup"><span data-stu-id="585c3-131">Note that the amount of work done in preparation was less in Windows 2000 and Windows XP.</span></span> <span data-ttu-id="585c3-132">一旦函式成功，呼叫不再允許的函式將會傳回 JET_errClientRequestToStopJetService。</span><span class="sxs-lookup"><span data-stu-id="585c3-132">Once the function succeeds, calling functions that are no longer allowed will return JET_errClientRequestToStopJetService.</span></span> <span data-ttu-id="585c3-133">此呼叫之後仍允許的函式為： [JetRollback](./jetrollback-function.md)、 [JetCloseTable](./jetclosetable-function.md)、 [JetEndSession](./jetendsession-function.md)、 [JetCloseDatabase](./jetclosedatabase-function.md)、 [JetDetachDatabase](./jetdetachdatabase-function.md) 和 [JetResetSessionCoNtext](./jetresetsessioncontext-function.md)。</span><span class="sxs-lookup"><span data-stu-id="585c3-133">Functions that are still allowed after this call are: [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) and [JetResetSessionContext](./jetresetsessioncontext-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="585c3-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="585c3-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="585c3-135"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="585c3-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="585c3-136">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="585c3-136">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="585c3-137"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="585c3-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="585c3-138">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="585c3-138">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="585c3-139"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="585c3-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="585c3-140">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="585c3-140">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="585c3-141"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="585c3-141"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="585c3-142">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="585c3-142">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="585c3-143"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="585c3-143"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="585c3-144">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="585c3-144">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="585c3-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="585c3-145">See Also</span></span>

[<span data-ttu-id="585c3-146">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="585c3-146">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="585c3-147">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="585c3-147">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="585c3-148">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="585c3-148">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="585c3-149">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="585c3-149">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="585c3-150">JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="585c3-150">JetDetachDatabase</span></span>](./jetdetachdatabase-function.md)  
[<span data-ttu-id="585c3-151">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="585c3-151">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="585c3-152">JetResetSessionCoNtext</span><span class="sxs-lookup"><span data-stu-id="585c3-152">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="585c3-153">JetRollback</span><span class="sxs-lookup"><span data-stu-id="585c3-153">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="585c3-154">JetTerm</span><span class="sxs-lookup"><span data-stu-id="585c3-154">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="585c3-155">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="585c3-155">JetTerm2</span></span>](./jetterm2-function.md)
