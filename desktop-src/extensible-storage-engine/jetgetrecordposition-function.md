---
description: 深入瞭解： JetGetRecordPosition 函數
title: JetGetRecordPosition 函式
TOCTitle: JetGetRecordPosition Function
ms:assetid: 811d9e68-0594-4f70-b854-c3ec966b2705
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269316(v=EXCHG.10)
ms:contentKeyID: 32765606
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d4301b25ca111228b742ce7b35ab9ae28e170526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026844"
---
# <a name="jetgetrecordposition-function"></a><span data-ttu-id="0e390-103">JetGetRecordPosition 函式</span><span class="sxs-lookup"><span data-stu-id="0e390-103">JetGetRecordPosition Function</span></span>


<span data-ttu-id="0e390-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0e390-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetrecordposition-function"></a><span data-ttu-id="0e390-105">JetGetRecordPosition 函式</span><span class="sxs-lookup"><span data-stu-id="0e390-105">JetGetRecordPosition Function</span></span>

<span data-ttu-id="0e390-106">**JetGetRecordPosition** 函數會以 [JET_RECPOS](./jet-recpos-structure.md)結構的形式，傳回目前索引中目前記錄的小數位置。</span><span class="sxs-lookup"><span data-stu-id="0e390-106">The **JetGetRecordPosition** function returns the fractional position of the current record in the current index in the form of a [JET_RECPOS](./jet-recpos-structure.md) structure.</span></span> <span data-ttu-id="0e390-107">此結構描述的是在目前記錄之前的索引項目目大約數量的小數位置，以及索引中專案的大約總數目。</span><span class="sxs-lookup"><span data-stu-id="0e390-107">This structure describes fractional positions in terms of an approximate number of index entries before the current record and an approximate total number of entries in the index.</span></span>

```cpp
    JET_ERR JET_API JetGetRecordPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECPOS* precpos,
      __in          unsigned long cbRecpos
    );
```

### <a name="parameters"></a><span data-ttu-id="0e390-108">參數</span><span class="sxs-lookup"><span data-stu-id="0e390-108">Parameters</span></span>

<span data-ttu-id="0e390-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="0e390-109">*sesid*</span></span>

<span data-ttu-id="0e390-110">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="0e390-110">The session to use for this call.</span></span>

<span data-ttu-id="0e390-111">*tableid*</span><span class="sxs-lookup"><span data-stu-id="0e390-111">*tableid*</span></span>

<span data-ttu-id="0e390-112">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="0e390-112">The cursor to use for this call.</span></span>

<span data-ttu-id="0e390-113">*precpos*</span><span class="sxs-lookup"><span data-stu-id="0e390-113">*precpos*</span></span>

<span data-ttu-id="0e390-114">用來取得目前索引中目前記錄位置的分數描述。</span><span class="sxs-lookup"><span data-stu-id="0e390-114">The description of the fraction to use in getting the position of the current record in the current index.</span></span>

<span data-ttu-id="0e390-115">*cbRecpos*</span><span class="sxs-lookup"><span data-stu-id="0e390-115">*cbRecpos*</span></span>

<span data-ttu-id="0e390-116">配置於 *precpos* 的記憶體大小。</span><span class="sxs-lookup"><span data-stu-id="0e390-116">The size of memory allocated at *precpos*.</span></span>

### <a name="return-value"></a><span data-ttu-id="0e390-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="0e390-117">Return Value</span></span>

<span data-ttu-id="0e390-118">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="0e390-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="0e390-119">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="0e390-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e390-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0e390-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="0e390-121">Description</span><span class="sxs-lookup"><span data-stu-id="0e390-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e390-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="0e390-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="0e390-123">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="0e390-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e390-124">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="0e390-124">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="0e390-125">無法完成作業，因為與該會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="0e390-125">It is not possible to complete the operation because the instance that is associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e390-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="0e390-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="0e390-127">無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</span><span class="sxs-lookup"><span data-stu-id="0e390-127">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e390-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="0e390-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="0e390-129">因為與會話相關聯的實例發生嚴重錯誤，所以無法完成此操作。</span><span class="sxs-lookup"><span data-stu-id="0e390-129">This operation cannot complete because the instance, associated with the session, encountered a fatal error.</span></span> <span data-ttu-id="0e390-130">必須撤銷所有資料的存取權，才能保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="0e390-130">It is required that access to all data be revoked in order to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="0e390-131"><strong>Windows 2000：</strong>  Windows 2000 作業系統將不會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="0e390-131"><strong>Windows 2000:</strong>  This error will not be returned by the Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e390-132">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="0e390-132">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="0e390-133"><em>Precpos</em>配置的記憶體大小不是足夠的大小。</span><span class="sxs-lookup"><span data-stu-id="0e390-133">The size of the allocated memory at <em>precpos</em> is not a sufficient size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e390-134">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="0e390-134">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="0e390-135">資料指標目前不在記錄中，而且無法傳回位置。</span><span class="sxs-lookup"><span data-stu-id="0e390-135">The cursor is not currently on a record and cannot return a position.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e390-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="0e390-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="0e390-137">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="0e390-137">It is not possible to complete the operation because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e390-138">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="0e390-138">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="0e390-139">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="0e390-139">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="0e390-140"><strong>Windows 2000：</strong>  Windows 2000 作業系統將不會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="0e390-140"><strong>Windows 2000:</strong>  This error will not be returned by the Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e390-141">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="0e390-141">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="0e390-142">無法完成作業，因為與會話相關聯的實例正在關閉中。</span><span class="sxs-lookup"><span data-stu-id="0e390-142">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0e390-143">成功時，會在 precpos-centriesLT 中傳回索引中目前記錄之前的大約索引項目目數 \> 。</span><span class="sxs-lookup"><span data-stu-id="0e390-143">On success, the approximate number of index entries preceding the current record in the index are returned in precpos-\>centriesLT.</span></span> <span data-ttu-id="0e390-144">precpos-centriesInRange 中傳回 1 \> 。</span><span class="sxs-lookup"><span data-stu-id="0e390-144">1 is returned in precpos-\>centriesInRange.</span></span> <span data-ttu-id="0e390-145">索引中的大約專案數會以 precpos- \> centriesTotal 傳回。</span><span class="sxs-lookup"><span data-stu-id="0e390-145">The approximate number of entries in the index is returned in precpos-\>centriesTotal.</span></span>

<span data-ttu-id="0e390-146">失敗時，不會對在 *precpos* 配置的記憶體進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="0e390-146">On failure, no changes are made to memory allocated at *precpos*.</span></span>

#### <a name="remarks"></a><span data-ttu-id="0e390-147">備註</span><span class="sxs-lookup"><span data-stu-id="0e390-147">Remarks</span></span>

<span data-ttu-id="0e390-148">當資料表上持續發生更新時，此作業會傳回不同的資料。</span><span class="sxs-lookup"><span data-stu-id="0e390-148">This operation returns varying data when updates occur continuously on the table.</span></span> <span data-ttu-id="0e390-149">值的變更不一定會根據更新的知識來符合預期，因為這些值是根據索引的實體屬性來近似值。</span><span class="sxs-lookup"><span data-stu-id="0e390-149">The changes in the values will not always match expectations based on knowledge of the updates, since the values are approximations based on physical properties of the index.</span></span> <span data-ttu-id="0e390-150">交易式隔離不會套用至 **JetGetRecordPosition** 的位置，因為這些值相依于非交易隔離之索引的實體屬性。</span><span class="sxs-lookup"><span data-stu-id="0e390-150">Transactional isolation does not apply to positions from **JetGetRecordPosition** since the values depend on physical properties of the index that are not transaction isolated.</span></span>

<span data-ttu-id="0e390-151">[JET_RECPOS](./jet-recpos-structure.md) 不能用來描述資料表內的記錄，或將記錄重新放置到接近現有記錄的位置。</span><span class="sxs-lookup"><span data-stu-id="0e390-151">[JET_RECPOS](./jet-recpos-structure.md) should not be used to describe a record within a table or to reposition a record close to an existing record.</span></span> <span data-ttu-id="0e390-152">相反地，您應該先取出現有記錄的書簽，然後再用它來重新置放相同的記錄。</span><span class="sxs-lookup"><span data-stu-id="0e390-152">Instead, bookmarks for an existing record should be retrieved and then used to reposition the same record.</span></span>

#### <a name="requirements"></a><span data-ttu-id="0e390-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e390-153">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e390-154"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="0e390-154"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0e390-155">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="0e390-155">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e390-156"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="0e390-156"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0e390-157">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="0e390-157">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e390-158"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="0e390-158"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0e390-159">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="0e390-159">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e390-160"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="0e390-160"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="0e390-161">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="0e390-161">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e390-162"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="0e390-162"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="0e390-163">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="0e390-163">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="0e390-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e390-164">See Also</span></span>

[<span data-ttu-id="0e390-165">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="0e390-165">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="0e390-166">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0e390-166">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0e390-167">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="0e390-167">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="0e390-168">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="0e390-168">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="0e390-169">JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="0e390-169">JET_RECPOS</span></span>](./jet-recpos-structure.md)  
[<span data-ttu-id="0e390-170">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="0e390-170">JET_SETINFO</span></span>](./jet-setinfo-structure.md)  
[<span data-ttu-id="0e390-171">JetGotoPosition</span><span class="sxs-lookup"><span data-stu-id="0e390-171">JetGotoPosition</span></span>](./jetgotoposition-function.md)  
[<span data-ttu-id="0e390-172">JetStopService</span><span class="sxs-lookup"><span data-stu-id="0e390-172">JetStopService</span></span>](./jetstopservice-function.md)
