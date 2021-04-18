---
description: 深入瞭解： JetComputeStats 函數
title: JetComputeStats 函式
TOCTitle: JetComputeStats Function
ms:assetid: 142f6ab0-715f-493a-a762-7a83854498d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269192(v=EXCHG.10)
ms:contentKeyID: 32765495
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetComputeStats
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 77c6856a50ae2f1c01b1cfde0666d0c535ad37e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195334"
---
# <a name="jetcomputestats-function"></a><span data-ttu-id="6393b-103">JetComputeStats 函式</span><span class="sxs-lookup"><span data-stu-id="6393b-103">JetComputeStats Function</span></span>


<span data-ttu-id="6393b-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6393b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcomputestats-function"></a><span data-ttu-id="6393b-105">JetComputeStats 函式</span><span class="sxs-lookup"><span data-stu-id="6393b-105">JetComputeStats Function</span></span>

<span data-ttu-id="6393b-106">**JetComputeStats** 函式會逐步解說資料表的每個索引，以精確計算索引中的專案數，以及索引中的相異索引鍵數目。</span><span class="sxs-lookup"><span data-stu-id="6393b-106">The **JetComputeStats** function walks each index of a table to exactly compute the number of entries in an index, and the number of distinct keys in an index.</span></span> <span data-ttu-id="6393b-107">這項資訊，以及配置給索引的資料庫頁面數目和目前的計算時間，都會儲存在資料庫的索引中繼資料中。</span><span class="sxs-lookup"><span data-stu-id="6393b-107">This information, together with the number of database pages allocated for an index and the current time of the computation is stored in index metadata in the database.</span></span> <span data-ttu-id="6393b-108">之後可以使用資訊作業來抓取此資料。</span><span class="sxs-lookup"><span data-stu-id="6393b-108">This data can be subsequently retrieved with information operations.</span></span>

```cpp
    JET_ERR JET_API JetComputeStats(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a><span data-ttu-id="6393b-109">參數</span><span class="sxs-lookup"><span data-stu-id="6393b-109">Parameters</span></span>

<span data-ttu-id="6393b-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="6393b-110">*sesid*</span></span>

<span data-ttu-id="6393b-111">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="6393b-111">The session to use for this call.</span></span>

<span data-ttu-id="6393b-112">*tableid*</span><span class="sxs-lookup"><span data-stu-id="6393b-112">*tableid*</span></span>

<span data-ttu-id="6393b-113">將用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="6393b-113">The cursor that will be used for this call.</span></span> <span data-ttu-id="6393b-114">描述要計算統計資料的資料表。</span><span class="sxs-lookup"><span data-stu-id="6393b-114">Describes the table to compute statistics on.</span></span>

### <a name="return-value"></a><span data-ttu-id="6393b-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="6393b-115">Return Value</span></span>

<span data-ttu-id="6393b-116">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="6393b-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6393b-117">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="6393b-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6393b-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6393b-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="6393b-119">Description</span><span class="sxs-lookup"><span data-stu-id="6393b-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6393b-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6393b-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6393b-121">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="6393b-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6393b-122">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="6393b-122">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="6393b-123">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="6393b-123">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6393b-124">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="6393b-124">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="6393b-125">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="6393b-125">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="6393b-126">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="6393b-126">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6393b-127">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="6393b-127">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="6393b-128">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="6393b-128">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6393b-129">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="6393b-129">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="6393b-130">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="6393b-130">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6393b-131">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="6393b-131">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="6393b-132">要求此作業回復所有變更時發生錯誤，但交易回復本身失敗。</span><span class="sxs-lookup"><span data-stu-id="6393b-132">An error occurred requiring this operation to rollback all changes, but the transaction rollback itself failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6393b-133">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="6393b-133">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="6393b-134">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="6393b-134">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="6393b-135">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="6393b-135">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6393b-136">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="6393b-136">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="6393b-137">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="6393b-137">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6393b-138">成功時，最新的統計資料會儲存在與指定資料指標所描述之資料表的資料庫目錄中。</span><span class="sxs-lookup"><span data-stu-id="6393b-138">On success, up-to-date statistics are stored in the database catalogs for the table described with the given cursor.</span></span>

<span data-ttu-id="6393b-139">失敗時，不會對資料庫進行任何類型的更新。</span><span class="sxs-lookup"><span data-stu-id="6393b-139">On failure, no updates of any kind are made to the database.</span></span>

#### <a name="remarks"></a><span data-ttu-id="6393b-140">備註</span><span class="sxs-lookup"><span data-stu-id="6393b-140">Remarks</span></span>

<span data-ttu-id="6393b-141">這項作業可能會耗用資源，因為資料表中的每個索引都必須完整地進行。</span><span class="sxs-lookup"><span data-stu-id="6393b-141">This operation can be resource consuming since each index in a table must be walked in its entirety.</span></span> <span data-ttu-id="6393b-142">[JetGetRecordPosition](./jetgetrecordposition-function.md) 可以用來取得索引中專案數目的粗略估計值，但無法自行估計索引中的相異值數目。</span><span class="sxs-lookup"><span data-stu-id="6393b-142">[JetGetRecordPosition](./jetgetrecordposition-function.md) can be used to get a rough estimate of the number of entries in an index, but it cannot by itself estimate the number of distinct values in an index.</span></span>

<span data-ttu-id="6393b-143">這項作業所計算的資料會開始過期，並在後續更新資料表。</span><span class="sxs-lookup"><span data-stu-id="6393b-143">The data computed by this operation begins to become out of date and the table is subsequently updated.</span></span>

<span data-ttu-id="6393b-144">**JetComputeStats** 對資料庫所做的更新會以延遲的方式進行。</span><span class="sxs-lookup"><span data-stu-id="6393b-144">Updates to the database made by **JetComputeStats** are made in a lazy fashion.</span></span> <span data-ttu-id="6393b-145">這表示沒有任何記錄排清會伴隨此作業，而且 **JetComputeStats** 傳回 JET_errSuccess 後的系統損毀仍會導致這些更新遺失。</span><span class="sxs-lookup"><span data-stu-id="6393b-145">This means that no log flush will be accompanied by this operation and a system crash subsequent to a return of JET_errSuccess by **JetComputeStats** can still cause these updates to be lost.</span></span>

#### <a name="requirements"></a><span data-ttu-id="6393b-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="6393b-146">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6393b-147"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="6393b-147"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6393b-148">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="6393b-148">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6393b-149"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="6393b-149"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6393b-150">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="6393b-150">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6393b-151"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="6393b-151"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6393b-152">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="6393b-152">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6393b-153"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="6393b-153"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6393b-154">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="6393b-154">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6393b-155"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6393b-155"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6393b-156">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="6393b-156">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6393b-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6393b-157">See Also</span></span>

[<span data-ttu-id="6393b-158">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6393b-158">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6393b-159">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="6393b-159">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="6393b-160">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="6393b-160">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="6393b-161">JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="6393b-161">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)  
[<span data-ttu-id="6393b-162">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="6393b-162">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)  
[<span data-ttu-id="6393b-163">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="6393b-163">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="6393b-164">JetStopService</span><span class="sxs-lookup"><span data-stu-id="6393b-164">JetStopService</span></span>](./jetstopservice-function.md)
