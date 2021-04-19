---
description: 深入瞭解： JetSetTableSequential 函數
title: JetSetTableSequential 函式
TOCTitle: JetSetTableSequential Function
ms:assetid: 874ddd3c-0d69-4d48-b61a-e9e0457426ef
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269323(v=EXCHG.10)
ms:contentKeyID: 32765613
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b633b348b712e446535054c5a39d2768236b7705
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966689"
---
# <a name="jetsettablesequential-function"></a><span data-ttu-id="803e9-103">JetSetTableSequential 函式</span><span class="sxs-lookup"><span data-stu-id="803e9-103">JetSetTableSequential Function</span></span>


<span data-ttu-id="803e9-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="803e9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsettablesequential-function"></a><span data-ttu-id="803e9-105">JetSetTableSequential 函式</span><span class="sxs-lookup"><span data-stu-id="803e9-105">JetSetTableSequential Function</span></span>

<span data-ttu-id="803e9-106">**JetSetTableSequential** 函式會通知資料庫引擎應用程式正在掃描包含指定資料指標的整個目前索引。</span><span class="sxs-lookup"><span data-stu-id="803e9-106">The **JetSetTableSequential** function notifies the database engine that the application is scanning the entire current index that contains a given cursor.</span></span> <span data-ttu-id="803e9-107">因此，用來存取索引資料的方法將會進行微調，使此案例的速度越快越好。</span><span class="sxs-lookup"><span data-stu-id="803e9-107">Consequently, the methods that are used to access the index data will be tuned to make this scenario as fast as possible.</span></span>

<span data-ttu-id="803e9-108">**Windows xp：**  **JetSetTableSequential** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="803e9-108">**Windows XP:**  **JetSetTableSequential** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetSetTableSequential(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="803e9-109">參數</span><span class="sxs-lookup"><span data-stu-id="803e9-109">Parameters</span></span>

<span data-ttu-id="803e9-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="803e9-110">*sesid*</span></span>

<span data-ttu-id="803e9-111">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="803e9-111">The session to use for this call.</span></span>

<span data-ttu-id="803e9-112">*tableid*</span><span class="sxs-lookup"><span data-stu-id="803e9-112">*tableid*</span></span>

<span data-ttu-id="803e9-113">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="803e9-113">The cursor to use for this call.</span></span>

<span data-ttu-id="803e9-114">*grbit*</span><span class="sxs-lookup"><span data-stu-id="803e9-114">*grbit*</span></span>

<span data-ttu-id="803e9-115">指定零或多個下列選項的位群組。</span><span class="sxs-lookup"><span data-stu-id="803e9-115">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="803e9-116">值</span><span class="sxs-lookup"><span data-stu-id="803e9-116">Value</span></span></p></th>
<th><p><span data-ttu-id="803e9-117">意義</span><span class="sxs-lookup"><span data-stu-id="803e9-117">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="803e9-118">JET_bitPrereadForward</span><span class="sxs-lookup"><span data-stu-id="803e9-118">JET_bitPrereadForward</span></span></p></td>
<td><p><span data-ttu-id="803e9-119">此選項是用來以正向方向編制索引。</span><span class="sxs-lookup"><span data-stu-id="803e9-119">This option is used to index in the forward direction.</span></span></p>
<p><span data-ttu-id="803e9-120"><strong>Windows 7：</strong>  <strong>JET_bitPrereadForward</strong> 是在 windows 7 中引進的。</span><span class="sxs-lookup"><span data-stu-id="803e9-120"><strong>Windows 7:</strong>  <strong>JET_bitPrereadForward</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="803e9-121">JET_bitPrereadBackward</span><span class="sxs-lookup"><span data-stu-id="803e9-121">JET_bitPrereadBackward</span></span></p></td>
<td><p><span data-ttu-id="803e9-122">此選項可用來在反向方向編制索引。</span><span class="sxs-lookup"><span data-stu-id="803e9-122">This option is used to index in the backward direction.</span></span></p>
<p><span data-ttu-id="803e9-123"><strong>Windows 7：</strong>  <strong>JET_bitPrereadBackward</strong> 是在 windows 7 中引進的。</span><span class="sxs-lookup"><span data-stu-id="803e9-123"><strong>Windows 7:</strong>  <strong>JET_bitPrereadBackward</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="803e9-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="803e9-124">Return Value</span></span>

<span data-ttu-id="803e9-125">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="803e9-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="803e9-126">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="803e9-126">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="803e9-127">傳回碼</span><span class="sxs-lookup"><span data-stu-id="803e9-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="803e9-128">Description</span><span class="sxs-lookup"><span data-stu-id="803e9-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="803e9-129">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="803e9-129">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="803e9-130">作業無法完成，因為呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>時，與會話相關聯之實例上的所有活動都已停止。</span><span class="sxs-lookup"><span data-stu-id="803e9-130">The operation cannot complete because all activity on the instance that is associated with the session has been quiesced as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="803e9-131">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="803e9-131">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="803e9-132">作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="803e9-132">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="803e9-133"><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="803e9-133"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="803e9-134">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="803e9-134">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="803e9-135">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="803e9-135">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="803e9-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="803e9-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="803e9-137">作業無法完成，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="803e9-137">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="803e9-138">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="803e9-138">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="803e9-139">無法完成作業，因為與會話相關聯的實例正在關閉中。</span><span class="sxs-lookup"><span data-stu-id="803e9-139">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="803e9-140">如果此函式成功，則資料指標的目前索引會針對整個索引的連續掃描進行優化。</span><span class="sxs-lookup"><span data-stu-id="803e9-140">If this function succeeds, the current index of the cursor is optimized for a sequential scan of the entire index.</span></span> <span data-ttu-id="803e9-141">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="803e9-141">No change to the database state will occur.</span></span>

<span data-ttu-id="803e9-142">如果此函式失敗，將不會變更資料指標的設定。</span><span class="sxs-lookup"><span data-stu-id="803e9-142">If this function fails, no change to the configuration of the cursor will occur.</span></span> <span data-ttu-id="803e9-143">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="803e9-143">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="803e9-144">備註</span><span class="sxs-lookup"><span data-stu-id="803e9-144">Remarks</span></span>

<span data-ttu-id="803e9-145">如果應用程式需要有效率地掃描索引的已知子集，則在使用 [JetSetIndexRange](./jetsetindexrange-function.md)建立索引範圍時也會執行類似的優化。</span><span class="sxs-lookup"><span data-stu-id="803e9-145">If the application needs to efficiently scan a known subset of an index, a similar optimization is also performed whenever an index range is established by using [JetSetIndexRange](./jetsetindexrange-function.md).</span></span> <span data-ttu-id="803e9-146">這項優化只適用于 Windows XP 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="803e9-146">This optimization is only available on Windows XP and later releases.</span></span>

<span data-ttu-id="803e9-147">如果應用程式需要有效率地掃描索引的未知子集，則不應採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="803e9-147">If the application needs to efficiently scan an unknown subset of an index, no action should be taken.</span></span> <span data-ttu-id="803e9-148">引擎可以自動偵測掃描行為，而且會事先提取資料。</span><span class="sxs-lookup"><span data-stu-id="803e9-148">The engine can automatically detect scanning behavior and will fetch data ahead of time.</span></span> <span data-ttu-id="803e9-149">不過，這種行為並不是積極的。</span><span class="sxs-lookup"><span data-stu-id="803e9-149">This behavior is not as aggressive, however.</span></span>

<span data-ttu-id="803e9-150">這項優化可讓您有效率地掃描主要索引，並讓您只在次要索引中以有效率的方式掃描索引項目目資料。</span><span class="sxs-lookup"><span data-stu-id="803e9-150">This optimization will make scanning the primary index efficient and will make scanning just the index entry data in a secondary index efficient.</span></span> <span data-ttu-id="803e9-151">它不會在您有效率地抓取記錄資料時，掃描次要索引。</span><span class="sxs-lookup"><span data-stu-id="803e9-151">It will not make scanning a secondary index while retrieving record data efficient.</span></span> <span data-ttu-id="803e9-152">這是因為引擎不會在記錄資料上執行預先讀取。</span><span class="sxs-lookup"><span data-stu-id="803e9-152">This is because the engine does not perform a read-ahead on the record data.</span></span>

#### <a name="requirements"></a><span data-ttu-id="803e9-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="803e9-153">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="803e9-154"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="803e9-154"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="803e9-155">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="803e9-155">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="803e9-156"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="803e9-156"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="803e9-157">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="803e9-157">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="803e9-158"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="803e9-158"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="803e9-159">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="803e9-159">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="803e9-160"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="803e9-160"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="803e9-161">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="803e9-161">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="803e9-162"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="803e9-162"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="803e9-163">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="803e9-163">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="803e9-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="803e9-164">See Also</span></span>

[<span data-ttu-id="803e9-165">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="803e9-165">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="803e9-166">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="803e9-166">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="803e9-167">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="803e9-167">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="803e9-168">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="803e9-168">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="803e9-169">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="803e9-169">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)  
[<span data-ttu-id="803e9-170">JetStopService</span><span class="sxs-lookup"><span data-stu-id="803e9-170">JetStopService</span></span>](./jetstopservice-function.md)
