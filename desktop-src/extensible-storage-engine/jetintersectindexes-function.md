---
description: 深入瞭解： JetIntersectIndexes 函數
title: JetIntersectIndexes 函式
TOCTitle: JetIntersectIndexes Function
ms:assetid: 6e111d10-6882-46ac-a70b-7896662d3b5d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269289(v=EXCHG.10)
ms:contentKeyID: 32765581
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIntersectIndexes
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bdffa6f21a65ae7f438f87ea0d8d2adf4aed6a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970131"
---
# <a name="jetintersectindexes-function"></a><span data-ttu-id="eb67e-103">JetIntersectIndexes 函式</span><span class="sxs-lookup"><span data-stu-id="eb67e-103">JetIntersectIndexes Function</span></span>


<span data-ttu-id="eb67e-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="eb67e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetintersectindexes-function"></a><span data-ttu-id="eb67e-105">JetIntersectIndexes 函式</span><span class="sxs-lookup"><span data-stu-id="eb67e-105">JetIntersectIndexes Function</span></span>

<span data-ttu-id="eb67e-106">**JetIntersectIndexes** 函式會計算相同資料表上不同次要索引的多個索引項目目集合之間的交集。</span><span class="sxs-lookup"><span data-stu-id="eb67e-106">The **JetIntersectIndexes** function computes the intersection between multiple sets of index entries from different secondary indices over the same table.</span></span> <span data-ttu-id="eb67e-107">這項作業適用于在資料表中尋找符合可使用索引範圍表示之兩個或多個準則的一組記錄。</span><span class="sxs-lookup"><span data-stu-id="eb67e-107">This operation is useful for finding the set of records in a table that match two or more criteria that can be expressed using index ranges.</span></span>

```cpp
    JET_ERR JET_API JetIntersectIndexes(
      __in          JET_SESID sesid,
      __in          JET_INDEXRANGE* rgindexrange,
      __in          unsigned long cindexrange,
      __in_out      JET_RECORDLIST* precordlist,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="eb67e-108">參數</span><span class="sxs-lookup"><span data-stu-id="eb67e-108">Parameters</span></span>

<span data-ttu-id="eb67e-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="eb67e-109">*sesid*</span></span>

<span data-ttu-id="eb67e-110">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="eb67e-110">The session to use for this call.</span></span>

<span data-ttu-id="eb67e-111">*rgindexrange*</span><span class="sxs-lookup"><span data-stu-id="eb67e-111">*rgindexrange*</span></span>

<span data-ttu-id="eb67e-112">[JET_IndexRange](./jet-indexrange-structure.md)結構陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="eb67e-112">A pointer to an array of [JET_IndexRange](./jet-indexrange-structure.md) structures.</span></span> <span data-ttu-id="eb67e-113">每個結構都包含已設定的 [JET_TABLEID](./jet-tableid.md) ，以保存其中一個要交集的索引範圍。</span><span class="sxs-lookup"><span data-stu-id="eb67e-113">Each structure includes a [JET_TABLEID](./jet-tableid.md) that has been set up to hold one of the index ranges to be intersected.</span></span> <span data-ttu-id="eb67e-114">如需詳細資訊，請參閱 [JET_IndexRange](./jet-indexrange-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="eb67e-114">For more information, see [JET_IndexRange](./jet-indexrange-structure.md).</span></span>

<span data-ttu-id="eb67e-115">*cindexrange*</span><span class="sxs-lookup"><span data-stu-id="eb67e-115">*cindexrange*</span></span>

<span data-ttu-id="eb67e-116">包含在 *rgindexrange* 參數中的陣列中 [JET_IndexRange](./jet-indexrange-structure.md)結構的數目。</span><span class="sxs-lookup"><span data-stu-id="eb67e-116">The number of [JET_IndexRange](./jet-indexrange-structure.md) structures in the array that is contained in the *rgindexrange* parameter.</span></span>

<span data-ttu-id="eb67e-117">*precordlist*</span><span class="sxs-lookup"><span data-stu-id="eb67e-117">*precordlist*</span></span>

<span data-ttu-id="eb67e-118">[JET_RECORDLIST](./jet-recordlist-structure.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="eb67e-118">Pointer to a [JET_RECORDLIST](./jet-recordlist-structure.md) structure.</span></span> <span data-ttu-id="eb67e-119">此結構將會填入足夠的資訊，以使用 **JetIntersectIndexes** 的結果來進行臨時表的往返。</span><span class="sxs-lookup"><span data-stu-id="eb67e-119">This structure will be populated with enough information to traverse the temporary table with the results from **JetIntersectIndexes**.</span></span>

<span data-ttu-id="eb67e-120">接收 [JET_RECORDLIST](./jet-recordlist-structure.md) 結構的輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="eb67e-120">The output buffer that receives a [JET_RECORDLIST](./jet-recordlist-structure.md) structure.</span></span> <span data-ttu-id="eb67e-121">結構包含交集之結果集的描述。</span><span class="sxs-lookup"><span data-stu-id="eb67e-121">The structure contains a description of the result set of the intersection.</span></span>

<span data-ttu-id="eb67e-122">*grbit*</span><span class="sxs-lookup"><span data-stu-id="eb67e-122">*grbit*</span></span>

<span data-ttu-id="eb67e-123">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="eb67e-123">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="eb67e-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="eb67e-124">Return Value</span></span>

<span data-ttu-id="eb67e-125">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="eb67e-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="eb67e-126">如需 ESE 錯誤的詳細資訊，請參閱 [可擴充儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="eb67e-126">For more information about ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eb67e-127">傳回碼</span><span class="sxs-lookup"><span data-stu-id="eb67e-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="eb67e-128">Description</span><span class="sxs-lookup"><span data-stu-id="eb67e-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb67e-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="eb67e-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="eb67e-130">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="eb67e-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb67e-131">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="eb67e-131">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="eb67e-132">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="eb67e-132">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb67e-133">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="eb67e-133">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="eb67e-134">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="eb67e-134">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="eb67e-135"><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="eb67e-135"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb67e-136">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="eb67e-136">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="eb67e-137">其中一個要求的選項無效、使用不正確或未執行。</span><span class="sxs-lookup"><span data-stu-id="eb67e-137">One of the options requested was invalid, used incorrectly, or not implemented.</span></span></p>
<p><span data-ttu-id="eb67e-138"><strong>JetIntersectIndexes</strong>會在下列情況傳回此錯誤：</span><span class="sxs-lookup"><span data-stu-id="eb67e-138">This error is returned by <strong>JetIntersectIndexes</strong> when:</span></span></p>
<p><span data-ttu-id="eb67e-139">由<em>rgindexrange</em>陣列中的任何元素所指向<a href="gg269335(v=exchg.10).md">JET_IndexRange</a>結構中所包含的<em>grbit</em> ，不等於 JET_bitRecordInIndex。</span><span class="sxs-lookup"><span data-stu-id="eb67e-139">The <em>grbit</em> contained in the <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> structure pointed to by any element in the <em>rgindexrange</em> array is not equal to JET_bitRecordInIndex.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb67e-140">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="eb67e-140">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="eb67e-141">提供的其中一個參數包含未預期的值，或與另一個參數的值結合時不一致的值。</span><span class="sxs-lookup"><span data-stu-id="eb67e-141">One of the parameters provided contains an unexpected value or a value that is inconsistent when combined with the value of another parameter.</span></span></p>
<p><span data-ttu-id="eb67e-142"><strong>JetIntersectIndexes</strong>會傳回此錯誤，原因如下：</span><span class="sxs-lookup"><span data-stu-id="eb67e-142">This error is returned by <strong>JetIntersectIndexes</strong> for of the following reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="eb67e-143"><em>Precordlist</em>參數為 Null。</span><span class="sxs-lookup"><span data-stu-id="eb67e-143">The <em>precordlist</em> parameter is NULL.</span></span></p></li>
<li><p><span data-ttu-id="eb67e-144">在<em>precordlist</em>參數中指定之<a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a>結構的<strong>cbStruct</strong>成員不等於<a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a>結構的大小。</span><span class="sxs-lookup"><span data-stu-id="eb67e-144">The <strong>cbStruct</strong> member of the <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> structure specified in the <em>precordlist</em> parameter is not equal to size of the <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> structure.</span></span></p></li>
<li><p><span data-ttu-id="eb67e-145"><em>Cindexrange</em>參數為零。</span><span class="sxs-lookup"><span data-stu-id="eb67e-145">The <em>cindexrange</em> parameter is zero.</span></span></p></li>
<li><p><span data-ttu-id="eb67e-146"><em>Cindexrange</em>參數大於64。</span><span class="sxs-lookup"><span data-stu-id="eb67e-146">The <em>cindexrange</em> parameter is greater than 64.</span></span></p></li>
<li><p><span data-ttu-id="eb67e-147"><em>Rgindexrange</em>參數所指定之陣列中任何元素的<strong>cbStruct</strong>成員，都不等於<a href="gg269335(v=exchg.10).md">JET_IndexRange</a>結構的大小。</span><span class="sxs-lookup"><span data-stu-id="eb67e-147">The <strong>cbStruct</strong> member for any element in the array specified by the <em>rgindexrange</em> parameter is not equal to the size of the <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> structure.</span></span></p></li>
<li><p><span data-ttu-id="eb67e-148"><em>Rgindexrange</em>陣列中的元素包含來自不同資料表的<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s。</span><span class="sxs-lookup"><span data-stu-id="eb67e-148">The elements in the <em>rgindexrange</em> array contain <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s from different tables.</span></span></p></li>
<li><p><span data-ttu-id="eb67e-149"><em>Rgindexrange</em>陣列中的元素包含不在次要索引上的<a href="gg269182(v=exchg.10).md">JET_TABLEID</a> 。</span><span class="sxs-lookup"><span data-stu-id="eb67e-149">An element in the <em>rgindexrange</em> array contains a <a href="gg269182(v=exchg.10).md">JET_TABLEID</a> that is not positioned on a secondary index.</span></span></p></li>
<li><p><span data-ttu-id="eb67e-150"><em>Rgindexrange</em>陣列中的一或多個元素包含位於相同次要索引的<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s。</span><span class="sxs-lookup"><span data-stu-id="eb67e-150">One or more of the elements in the <em>rgindexrange</em> array contain <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s positioned on the same secondary index.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb67e-151">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="eb67e-151">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="eb67e-152">會話控制碼無效或參考已關閉的會話。</span><span class="sxs-lookup"><span data-stu-id="eb67e-152">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="eb67e-153">在所有情況下，都不會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="eb67e-153">This error is not returned under all circumstances.</span></span> <span data-ttu-id="eb67e-154">控制碼只會根據最大努力進行驗證。</span><span class="sxs-lookup"><span data-stu-id="eb67e-154">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb67e-155">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="eb67e-155">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="eb67e-156">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="eb67e-156">It is not possible to complete the operation because the instance associated with the session has not been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb67e-157">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="eb67e-157">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="eb67e-158">因為引擎無法配置開啟新資料指標所需的資源，所以操作失敗。</span><span class="sxs-lookup"><span data-stu-id="eb67e-158">The operation failed because the engine could not allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="eb67e-159">您可以使用<em>paramid</em>參數中指定的<em>JET_paramMaxCursors</em>呼叫<a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>來設定資料指標資源。</span><span class="sxs-lookup"><span data-stu-id="eb67e-159">Cursor resources are configured by calling <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <em>JET_paramMaxCursors</em> specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb67e-160">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="eb67e-160">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="eb67e-161">作業失敗，因為無法配置足夠的記憶體來完成。</span><span class="sxs-lookup"><span data-stu-id="eb67e-161">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="eb67e-162">如果主機進程的位址空間變得太分散， <strong>JetIntersectIndexes</strong>可能會傳回 JET_errOutOfMemory。</span><span class="sxs-lookup"><span data-stu-id="eb67e-162"><strong>JetIntersectIndexes</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="eb67e-163">無論要儲存的資料量為何，臨時表管理員一律會為每個建立的臨時表配置1MB 的位址空間區塊。</span><span class="sxs-lookup"><span data-stu-id="eb67e-163">The temporary table manager will always allocate a 1MB chunk of address space for every temporary table created regardless of the amount of data to be stored.</span></span> <span data-ttu-id="eb67e-164"><strong>JetIntersectIndexes</strong>會為<em>rgindexrange</em>參數中指定的每個<a href="gg269335(v=exchg.10).md">JET_IndexRange</a>建立一個臨時表，並為<a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a>的輸出建立一個臨時表。</span><span class="sxs-lookup"><span data-stu-id="eb67e-164"><strong>JetIntersectIndexes</strong> will create one temporary table for each <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> specified in the <em>rgindexrange</em> parameter, and one temporary table for the output in <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb67e-165">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="eb67e-165">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="eb67e-166">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="eb67e-166">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb67e-167">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="eb67e-167">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="eb67e-168">同時從一個以上的執行緒使用相同的會話是不合法的。</span><span class="sxs-lookup"><span data-stu-id="eb67e-168">It is illegal to use the same session from more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="eb67e-169"><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="eb67e-169"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb67e-170">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="eb67e-170">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="eb67e-171">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="eb67e-171">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb67e-172">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="eb67e-172">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="eb67e-173">因為引擎無法配置快取資料表索引所需的資源，所以操作失敗。</span><span class="sxs-lookup"><span data-stu-id="eb67e-173">The operation failed because the engine could not allocate the resources required to cache the indices of the table.</span></span> <span data-ttu-id="eb67e-174">您可以使用<a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>搭配<em>paramid</em>參數中指定的<em>JET_paramMaxOpenTables</em> ，來設定可以快取其架構的索引數目。</span><span class="sxs-lookup"><span data-stu-id="eb67e-174">The number of indices whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <em>JET_paramMaxOpenTables</em> specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb67e-175">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="eb67e-175">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="eb67e-176">作業失敗，因為引擎無法配置快取資料表架構所需的資源。</span><span class="sxs-lookup"><span data-stu-id="eb67e-176">The operation failed because the engine could not allocate the resources required to cache the schema of the table.</span></span> <span data-ttu-id="eb67e-177">您可以使用<a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>搭配<em>paramid</em>參數中指定的<em>JET_paramMaxOpenTables</em> ，來設定可以快取其架構的資料表數目。</span><span class="sxs-lookup"><span data-stu-id="eb67e-177">The number of tables whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <em>JET_paramMaxOpenTables</em> specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb67e-178">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="eb67e-178">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="eb67e-179">因為引擎無法配置建立臨時表所需的資源，所以操作失敗。</span><span class="sxs-lookup"><span data-stu-id="eb67e-179">The operation failed because the engine could not allocate the resources required to create a temporary table.</span></span> <span data-ttu-id="eb67e-180">臨時表資源是使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 與 <em>paramid</em> 參數中指定的 JET_paramMaxTemporaryTables 來設定。</span><span class="sxs-lookup"><span data-stu-id="eb67e-180">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with JET_paramMaxTemporaryTables specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="eb67e-181">成功時，會傳回新的臨時表，其中包含符合每個輸入索引範圍描述所代表準則的記錄的書簽。</span><span class="sxs-lookup"><span data-stu-id="eb67e-181">On success, a new temporary table is returned that contains the bookmarks of the records that match the criteria represented by each of the input index range descriptions.</span></span>

<span data-ttu-id="eb67e-182">失敗時，將不會建立包含結果的臨時表。</span><span class="sxs-lookup"><span data-stu-id="eb67e-182">On failure, the temporary table containing the results will not be created.</span></span> <span data-ttu-id="eb67e-183">暫存資料庫的狀態可能會變更。</span><span class="sxs-lookup"><span data-stu-id="eb67e-183">The state of the temporary database may be changed.</span></span> <span data-ttu-id="eb67e-184">資料庫引擎所使用之任何一般資料庫的狀態將保持不變。</span><span class="sxs-lookup"><span data-stu-id="eb67e-184">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span> <span data-ttu-id="eb67e-185">提供給此函式之 [JET_TABLEID](./jet-tableid.md)的目前位置可能會變更。</span><span class="sxs-lookup"><span data-stu-id="eb67e-185">The current position of the [JET_TABLEID](./jet-tableid.md)s provided to this function may be changed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="eb67e-186">備註</span><span class="sxs-lookup"><span data-stu-id="eb67e-186">Remarks</span></span>

<span data-ttu-id="eb67e-187">**JetIntersectIndexes** 可以用來以多個準則有效率地篩選資料表中的記錄，如果這些準則是以該資料表的次要索引來表示。</span><span class="sxs-lookup"><span data-stu-id="eb67e-187">**JetIntersectIndexes** can be used to efficiently filter the records in a table by multiple criteria if those criteria can be expressed in terms of the secondary indices over that table.</span></span> <span data-ttu-id="eb67e-188">例如，假設您有一個非常大的資料表包含人員。</span><span class="sxs-lookup"><span data-stu-id="eb67e-188">For example, consider that you have a very large table containing people.</span></span> <span data-ttu-id="eb67e-189">資料表可以有資料行做為其使用者識別碼、名字、姓氏等等。</span><span class="sxs-lookup"><span data-stu-id="eb67e-189">The table can have columns for their user id, first name, last name, and so on.</span></span> <span data-ttu-id="eb67e-190">假設每個資料行都是分開編制索引，而且資料表的主要索引是超過使用者識別碼。如果您想要尋找名字開頭為且其姓氏開頭為 G 的每個人，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="eb67e-190">Suppose that each of these columns is indexed separately and that the primary index of the table is over user id. If you wanted to find everyone whose first name starts with an A and whose last name starts with G, you would perform the following steps:</span></span>

1.  <span data-ttu-id="eb67e-191">開啟資料表上的新資料指標，並將該資料指標設定為使用「名字」資料行的索引。</span><span class="sxs-lookup"><span data-stu-id="eb67e-191">Open a new cursor on the table, and set that cursor to use the index over the "first name" column.</span></span> <span data-ttu-id="eb67e-192">然後為其 "first name" 以 ' A ' 開頭的所有人設定索引範圍，然後建立包含此資料指標的 [JET_IndexRange](./jet-indexrange-structure.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="eb67e-192">Then setup an index range for all people whose "first name" started with 'A', and build a [JET_IndexRange](./jet-indexrange-structure.md) struct that contains this cursor.</span></span>

2.  <span data-ttu-id="eb67e-193">針對「姓氏」以 ' G ' 開頭的所有使用者，在「姓氏」索引上重複步驟1。</span><span class="sxs-lookup"><span data-stu-id="eb67e-193">Repeat step 1 with a new cursor on the "last name" index for all people whose "last name" started with 'G'.</span></span>

3.  <span data-ttu-id="eb67e-194">將這些準則傳遞給 **JetIntersectIndexes** ，以將結果計算到臨時表中。</span><span class="sxs-lookup"><span data-stu-id="eb67e-194">Pass these criteria to **JetIntersectIndexes** to compute the result into a temporary table.</span></span>

4.  <span data-ttu-id="eb67e-195">遍歷臨時表，並取得以書簽傳遞準則的每個記錄。</span><span class="sxs-lookup"><span data-stu-id="eb67e-195">Traverse the temporary table and retrieve each of the records that pass the criteria by bookmark.</span></span>

<span data-ttu-id="eb67e-196">包含結果集的臨時表是一個簡單的資料表，其中包含每筆記錄的書簽，而這些記錄會通過所有用來計算交集的條件。</span><span class="sxs-lookup"><span data-stu-id="eb67e-196">The temporary table containing the result set is a simple table with one column that contains the bookmark of each record that passed all the criteria used to compute the intersection.</span></span> <span data-ttu-id="eb67e-197">結果集的排序次序與主要索引相同，而且不包含重複的專案。</span><span class="sxs-lookup"><span data-stu-id="eb67e-197">The result set is sorted in the same order as the primary index and contains no duplicate entries.</span></span> <span data-ttu-id="eb67e-198">應用程式可以藉由列舉臨時表中的資料列、使用 [JetRetrieveColumn](./jetretrievecolumn-function.md)來取得每個結果的書簽，然後流覽資料庫中的記錄，藉由在位於主要索引的資料指標上使用該書簽來呼叫 [JetGotoBookmark](./jetgotobookmark-function.md) ，以列舉交集的結果。</span><span class="sxs-lookup"><span data-stu-id="eb67e-198">The application can enumerate the results of the intersection by enumerating the rows in the temporary table, retrieving the bookmark for each result using [JetRetrieveColumn](./jetretrievecolumn-function.md), and then visiting the record in the database by calling [JetGotoBookmark](./jetgotobookmark-function.md) with that bookmark on a cursor positioned on the primary index.</span></span>

<span data-ttu-id="eb67e-199">**JetIntersectIndexes** 所傳回的臨時表只能以正向方向掃描。</span><span class="sxs-lookup"><span data-stu-id="eb67e-199">The temporary table returned by **JetIntersectIndexes** can only be scanned in a forward direction.</span></span> <span data-ttu-id="eb67e-200">當掃描完成時，也應該透過 [JetCloseTable](./jetclosetable-function.md) 來關閉它。</span><span class="sxs-lookup"><span data-stu-id="eb67e-200">It should also be closed via [JetCloseTable](./jetclosetable-function.md) when the scan has been completed.</span></span> <span data-ttu-id="eb67e-201">如需臨時表和其運作方式的詳細資訊，請參閱 [JetOpenTemporaryTable](./jetopentemporarytable-function.md)。</span><span class="sxs-lookup"><span data-stu-id="eb67e-201">For more information about temporary tables and how they work, see [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span></span>

<span data-ttu-id="eb67e-202">**JetIntersectIndexes** 通常是根據多個索引準則來篩選記錄的有效率且方便的方式。</span><span class="sxs-lookup"><span data-stu-id="eb67e-202">**JetIntersectIndexes** is generally an efficient and convenient way to filter records based on multiple indexed criteria.</span></span> <span data-ttu-id="eb67e-203">不過，您應該遵循一些重要的秘訣，以充分發揮這項功能的實用性。</span><span class="sxs-lookup"><span data-stu-id="eb67e-203">However, there are some important tips that should be followed to maximize the usefulness of this feature.</span></span> <span data-ttu-id="eb67e-204">如果您知道其中一個條件的限制是，所產生的索引範圍有極少的記錄，則只需要在應用層級上流覽索引範圍並篩選記錄，可能會比較好。</span><span class="sxs-lookup"><span data-stu-id="eb67e-204">If you know that one of the criteria is so restrictive that the resulting index range has very few records then it is probably better to simply walk that index range and filter the records at the application level.</span></span> <span data-ttu-id="eb67e-205">此外，如果您知道您的準則比交集的其他準則還低，那麼您可能會考慮從交集中卸載那些限制較少的準則。</span><span class="sxs-lookup"><span data-stu-id="eb67e-205">Further, if you know that you have criteria that are much less restrictive than other criteria in your intersection then you might consider dropping those much less restrictive criteria from the intersection.</span></span> <span data-ttu-id="eb67e-206">最後，如果您知道其中一個準則不會有任何限制，使產生的索引範圍幾乎與主要索引一樣大，則不太可能與該索引範圍有交集的優點 (將) 結果集的大小減少。</span><span class="sxs-lookup"><span data-stu-id="eb67e-206">Finally, if you know that one of the criteria is not at all restrictive such that the resulting index range is almost as large as the primary index then it is unlikely that intersecting with that index range will benefit (reduce the size of) the result set.</span></span> <span data-ttu-id="eb67e-207">在所有情況下，您應該以最少的輸入索引項目目來選取準則，並在輸出上產生最特定的書簽集合，以取得最大效能。</span><span class="sxs-lookup"><span data-stu-id="eb67e-207">In all cases, you should be selecting criteria in a manner that will take the fewest possible index entries on input and generate the most specific set of bookmarks on output for maximum performance.</span></span>

#### <a name="requirements"></a><span data-ttu-id="eb67e-208">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb67e-208">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb67e-209"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="eb67e-209"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="eb67e-210">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="eb67e-210">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb67e-211"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="eb67e-211"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="eb67e-212">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="eb67e-212">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb67e-213"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="eb67e-213"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="eb67e-214">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="eb67e-214">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb67e-215"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="eb67e-215"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="eb67e-216">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="eb67e-216">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb67e-217"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="eb67e-217"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="eb67e-218">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="eb67e-218">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="eb67e-219">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb67e-219">See Also</span></span>

[<span data-ttu-id="eb67e-220">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="eb67e-220">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="eb67e-221">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="eb67e-221">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="eb67e-222">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="eb67e-222">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="eb67e-223">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="eb67e-223">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="eb67e-224">JET_IndexRange</span><span class="sxs-lookup"><span data-stu-id="eb67e-224">JET_IndexRange</span></span>](./jet-indexrange-structure.md)  
[<span data-ttu-id="eb67e-225">JET_RECORDLIST</span><span class="sxs-lookup"><span data-stu-id="eb67e-225">JET_RECORDLIST</span></span>](./jet-recordlist-structure.md)  
[<span data-ttu-id="eb67e-226">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="eb67e-226">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)  
[<span data-ttu-id="eb67e-227">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="eb67e-227">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="eb67e-228">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="eb67e-228">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)
