---
description: 深入瞭解： JetGotoPosition 函數
title: JetGotoPosition 函式
TOCTitle: JetGotoPosition Function
ms:assetid: 77b099f1-4a21-4ddb-b269-83ca74219b4d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269300(v=EXCHG.10)
ms:contentKeyID: 32765592
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aae5148431ad46c5a75bbd804f2c0d777b279561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689536"
---
# <a name="jetgotoposition-function"></a><span data-ttu-id="4f2bc-103">JetGotoPosition 函式</span><span class="sxs-lookup"><span data-stu-id="4f2bc-103">JetGotoPosition Function</span></span>


<span data-ttu-id="4f2bc-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4f2bc-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgotoposition-function"></a><span data-ttu-id="4f2bc-105">JetGotoPosition 函式</span><span class="sxs-lookup"><span data-stu-id="4f2bc-105">JetGotoPosition Function</span></span>

<span data-ttu-id="4f2bc-106">**JetGotoPosition** 函式會將游標移至新的位置，這是透過目前索引的一小部分。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-106">The **JetGotoPosition** function moves a cursor to a new location that is a fraction of the way through the current index.</span></span> <span data-ttu-id="4f2bc-107">分數大約等於下列各項：</span><span class="sxs-lookup"><span data-stu-id="4f2bc-107">The fraction is approximately equal to the following:</span></span>

<span data-ttu-id="4f2bc-108">precpos- \> centriesLT/precpos- \> centriesTotal</span><span class="sxs-lookup"><span data-stu-id="4f2bc-108">precpos-\>centriesLT/precpos-\>centriesTotal</span></span>

<span data-ttu-id="4f2bc-109">當使用者嘗試顯示透過資料集開始部分的資料時，會執行這項作業來回應使用者的捲動方塊輸入。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-109">This operation is performed in response to user scroll box input that is received when the user attempts to show data that starts part way through a data set.</span></span>

```cpp
    JET_ERR JET_API JetGotoPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_RECPOS* precpos
    );
```

### <a name="parameters"></a><span data-ttu-id="4f2bc-110">參數</span><span class="sxs-lookup"><span data-stu-id="4f2bc-110">Parameters</span></span>

<span data-ttu-id="4f2bc-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="4f2bc-111">*sesid*</span></span>

<span data-ttu-id="4f2bc-112">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-112">The session to use for this call.</span></span>

<span data-ttu-id="4f2bc-113">*tableid*</span><span class="sxs-lookup"><span data-stu-id="4f2bc-113">*tableid*</span></span>

<span data-ttu-id="4f2bc-114">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-114">The cursor to use for this call.</span></span>

<span data-ttu-id="4f2bc-115">*precpos*</span><span class="sxs-lookup"><span data-stu-id="4f2bc-115">*precpos*</span></span>

<span data-ttu-id="4f2bc-116">用來將游標放在目前索引中的分數描述。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-116">The description of the fraction to use in positioning the cursor in the current index.</span></span>

### <a name="return-value"></a><span data-ttu-id="4f2bc-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="4f2bc-117">Return Value</span></span>

<span data-ttu-id="4f2bc-118">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="4f2bc-119">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4f2bc-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4f2bc-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="4f2bc-121">Description</span><span class="sxs-lookup"><span data-stu-id="4f2bc-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f2bc-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="4f2bc-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="4f2bc-123">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f2bc-124">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="4f2bc-124">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="4f2bc-125">無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-125">The operation could not complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f2bc-126">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="4f2bc-126">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="4f2bc-127">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-127">The operation could not complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="4f2bc-128"><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-128"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f2bc-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="4f2bc-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="4f2bc-130">給定的 precpos- &gt; cbStruct 不是 <a href="gg269308(v=exchg.10).md">JET_RECPOS</a> 結構的有效大小，或 precpos &gt; centriesLT 大於 precpos- &gt; centriesTotal。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-130">The given precpos-&gt;cbStruct is not a valid size for the <a href="gg269308(v=exchg.10).md">JET_RECPOS</a> structure, or precpos-&gt;centriesLT is greater than precpos-&gt;centriesTotal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f2bc-131">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="4f2bc-131">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="4f2bc-132">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-132">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f2bc-133">JET_errRecordNotFound</span><span class="sxs-lookup"><span data-stu-id="4f2bc-133">JET_errRecordNotFound</span></span></p></td>
<td><p><span data-ttu-id="4f2bc-134">如果索引是空的，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-134">This error will be returned if the index is empty.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f2bc-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="4f2bc-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="4f2bc-136">作業無法完成，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-136">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f2bc-137">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="4f2bc-137">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="4f2bc-138">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-138">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="4f2bc-139"><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-139"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f2bc-140">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="4f2bc-140">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="4f2bc-141">無法完成作業，因為與會話相關聯的實例正在關閉中。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-141">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4f2bc-142">如果此函式成功，則會將資料指標移至目前的記錄，此記錄的分數為 precpos- \> centriesLT 除以 precpos-centriesTotal 的索引 \> 。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-142">If this function succeeds, the cursor is moved to a current record that is a fraction of the way through the index where the fraction is precpos-\>centriesLT divided by precpos-\>centriesTotal.</span></span>

<span data-ttu-id="4f2bc-143">如果此函式失敗，資料指標位置會保持不變。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-143">If this function fails, the cursor location is left unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="4f2bc-144">備註</span><span class="sxs-lookup"><span data-stu-id="4f2bc-144">Remarks</span></span>

<span data-ttu-id="4f2bc-145">這項作業會將資料指標移至下一個近似值的位置： precpos- \> centriesLT 除以 precpos- \> centriesTotal。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-145">This operation moves the cursor through the table to a position at the following approximate point: precpos-\>centriesLT divided by precpos-\>centriesTotal.</span></span>

<span data-ttu-id="4f2bc-146">當資料表持續發生更新時，使用相同 [JET_RECPOS](./jet-recpos-structure.md) 的後續呼叫可以將資料指標移至索引中的不同位置，在先前的位置之前和之後。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-146">When updates are occurring continuously on the table, subsequent calls with the same [JET_RECPOS](./jet-recpos-structure.md) can move the cursor to different positions in the index, both before and after the previous position.</span></span> <span data-ttu-id="4f2bc-147">交易式隔離不會套用到 [JET_RECPOS](./jet-recpos-structure.md) 的位置，因為它相依于非交易隔離之索引的實體屬性。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-147">Transactional isolation does not apply to positioning through [JET_RECPOS](./jet-recpos-structure.md) since it depends on physical properties of the index that are not transaction isolated.</span></span>

<span data-ttu-id="4f2bc-148">[JET_RECPOS](./jet-recpos-structure.md) 不能用來描述資料表內的記錄，或將記錄重新放置到接近現有記錄的位置。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-148">[JET_RECPOS](./jet-recpos-structure.md) should not be used to describe a record within a table or to reposition a record close to an existing record.</span></span> <span data-ttu-id="4f2bc-149">相反地，應該在初始 **JetGotoPosition** 之後取出現有記錄的書簽，然後用來重新放置相同的記錄。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-149">Instead, bookmarks for an existing record should be retrieved after an initial **JetGotoPosition** and then used to reposition the same record.</span></span>

#### <a name="requirements"></a><span data-ttu-id="4f2bc-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f2bc-150">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f2bc-151"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="4f2bc-151"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4f2bc-152">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-152">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f2bc-153"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="4f2bc-153"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4f2bc-154">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-154">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f2bc-155"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="4f2bc-155"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4f2bc-156">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-156">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f2bc-157"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="4f2bc-157"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="4f2bc-158">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-158">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f2bc-159"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="4f2bc-159"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="4f2bc-160">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="4f2bc-160">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4f2bc-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4f2bc-161">See Also</span></span>

[<span data-ttu-id="4f2bc-162">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="4f2bc-162">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="4f2bc-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4f2bc-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4f2bc-164">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="4f2bc-164">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="4f2bc-165">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="4f2bc-165">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="4f2bc-166">JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="4f2bc-166">JET_RECPOS</span></span>](./jet-recpos-structure.md)  
[<span data-ttu-id="4f2bc-167">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="4f2bc-167">JET_SETINFO</span></span>](./jet-setinfo-structure.md)
