---
description: 深入瞭解： JetIndexRecordCount 函數
title: JetIndexRecordCount 函式
TOCTitle: JetIndexRecordCount Function
ms:assetid: 62d39738-cd91-4cfb-9483-f4a2dd845d9a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269267(v=EXCHG.10)
ms:contentKeyID: 32765569
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIndexRecordCount
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3324ad2fe68d106c7f4d2dcdcd1c3dd6ddefd608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510917"
---
# <a name="jetindexrecordcount-function"></a><span data-ttu-id="f931e-103">JetIndexRecordCount 函式</span><span class="sxs-lookup"><span data-stu-id="f931e-103">JetIndexRecordCount Function</span></span>


<span data-ttu-id="f931e-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f931e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetindexrecordcount-function"></a><span data-ttu-id="f931e-105">JetIndexRecordCount 函式</span><span class="sxs-lookup"><span data-stu-id="f931e-105">JetIndexRecordCount Function</span></span>

<span data-ttu-id="f931e-106">**JetIndexRecordCount** 函式會計算目前索引中的專案數，從目前的位置向前算起。</span><span class="sxs-lookup"><span data-stu-id="f931e-106">The **JetIndexRecordCount** function counts the number of entries in the current index from the current position forward.</span></span> <span data-ttu-id="f931e-107">目前的位置會包含在計數中。</span><span class="sxs-lookup"><span data-stu-id="f931e-107">The current position is included in the count.</span></span> <span data-ttu-id="f931e-108">如果目前索引超過多重值資料行，而且資料行的實例具有多個值，則計數可以大於資料表中的記錄總數。</span><span class="sxs-lookup"><span data-stu-id="f931e-108">The count can be greater than the total number of records in the table if the current index is over a multi-valued column and instances of the column have multiple-values.</span></span> <span data-ttu-id="f931e-109">如果資料表是空的，則會傳回計數的0。</span><span class="sxs-lookup"><span data-stu-id="f931e-109">If the table is empty, then 0 will be returned for the count.</span></span>

```cpp
    JET_ERR JET_API JetIndexRecordCount(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         unsigned long* pcrec,
      __in          unsigned long crecMax
    );
```

### <a name="parameters"></a><span data-ttu-id="f931e-110">參數</span><span class="sxs-lookup"><span data-stu-id="f931e-110">Parameters</span></span>

<span data-ttu-id="f931e-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="f931e-111">*sesid*</span></span>

<span data-ttu-id="f931e-112">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="f931e-112">The session to use for this call.</span></span>

<span data-ttu-id="f931e-113">*tableid*</span><span class="sxs-lookup"><span data-stu-id="f931e-113">*tableid*</span></span>

<span data-ttu-id="f931e-114">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="f931e-114">The cursor to use for this call.</span></span>

<span data-ttu-id="f931e-115">*pcrec*</span><span class="sxs-lookup"><span data-stu-id="f931e-115">*pcrec*</span></span>

<span data-ttu-id="f931e-116">要接收計數之不帶正負號的完整值指標。</span><span class="sxs-lookup"><span data-stu-id="f931e-116">The pointer to an unsigned long value to receive the count.</span></span>

<span data-ttu-id="f931e-117">*crecMax*</span><span class="sxs-lookup"><span data-stu-id="f931e-117">*crecMax*</span></span>

<span data-ttu-id="f931e-118">要計算的記錄數目上限。</span><span class="sxs-lookup"><span data-stu-id="f931e-118">The maximum number of records to count.</span></span> <span data-ttu-id="f931e-119">*CrecMax* 值為0表示計數是無限制的。</span><span class="sxs-lookup"><span data-stu-id="f931e-119">A *crecMax* value of 0 indicates that the count is unlimited.</span></span>

### <a name="return-value"></a><span data-ttu-id="f931e-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="f931e-120">Return Value</span></span>

<span data-ttu-id="f931e-121">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="f931e-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f931e-122">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="f931e-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f931e-123">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f931e-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="f931e-124">Description</span><span class="sxs-lookup"><span data-stu-id="f931e-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f931e-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f931e-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f931e-126">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="f931e-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f931e-127">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="f931e-127">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="f931e-128">無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</span><span class="sxs-lookup"><span data-stu-id="f931e-128">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f931e-129">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="f931e-129">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="f931e-130">作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="f931e-130">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="f931e-131"><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="f931e-131"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f931e-132">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="f931e-132">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="f931e-133">資料指標目前不在記錄上，且資料表不是空的。</span><span class="sxs-lookup"><span data-stu-id="f931e-133">The cursor is not currently on a record and the table is not empty.</span></span></p>
<p><span data-ttu-id="f931e-134"><strong>WINDOWS XP、Windows Server 2003、windows 2000 Server 及 windows 2000 Professional：</strong>  如果資料指標位於空的索引或索引範圍上， <strong>JetIndexRecordCount</strong> 會錯誤地傳回 JET_errNoCurrentRecord。</span><span class="sxs-lookup"><span data-stu-id="f931e-134"><strong>Windows XP, Windows Server 2003, Windows 2000 Server, and Windows 2000 Professional:</strong>  If the cursor is positioned on an empty index or index range then <strong>JetIndexRecordCount</strong> erroneously returns JET_errNoCurrentRecord.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f931e-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="f931e-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="f931e-136">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="f931e-136">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f931e-137">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="f931e-137">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="f931e-138">作業無法完成，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="f931e-138">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f931e-139">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="f931e-139">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="f931e-140">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="f931e-140">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="f931e-141"><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="f931e-141"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f931e-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="f931e-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="f931e-143">無法完成作業，因為與會話相關聯的實例正在關閉中。</span><span class="sxs-lookup"><span data-stu-id="f931e-143">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f931e-144">如果此函式成功，則包含目前位置和最高 *crecMax* (索引項目的確切數目（如果不是 0) ）會以 *pcrec* 所指向的不帶正負號的長整數格式傳回。</span><span class="sxs-lookup"><span data-stu-id="f931e-144">If this function succeeds, the exact number of index entries including the current position and up to *crecMax* (if it is not 0), is returned in the unsigned long pointed to by *pcrec*.</span></span>

<span data-ttu-id="f931e-145">如果此函式失敗，則不會對在 *precpos* 配置的記憶體進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="f931e-145">If this function fails, no changes are made to memory allocated at *precpos*.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f931e-146">備註</span><span class="sxs-lookup"><span data-stu-id="f931e-146">Remarks</span></span>

<span data-ttu-id="f931e-147">如果資料表不是空的，則資料指標應放置於開始計數的記錄上。</span><span class="sxs-lookup"><span data-stu-id="f931e-147">If the table is not empty, then the cursor should be positioned onto the record from which to begin the count.</span></span> <span data-ttu-id="f931e-148">計數將會包含此記錄，並在 *crecMax* 中向前算到指定的限制。</span><span class="sxs-lookup"><span data-stu-id="f931e-148">The count will include this record, and count forward up to the given limit in *crecMax*.</span></span> <span data-ttu-id="f931e-149">如果 *crecMax* 為0，則作業會繼續計算到索引結尾。</span><span class="sxs-lookup"><span data-stu-id="f931e-149">If *crecMax* is 0 then the operation will continue counting until the end of the index.</span></span>

<span data-ttu-id="f931e-150">索引範圍可以用來為計數建立人工索引的結尾限制。</span><span class="sxs-lookup"><span data-stu-id="f931e-150">Index ranges can be used to construct artificial end-of-index limitations for the count.</span></span> <span data-ttu-id="f931e-151">如此一來，就可以精確地計算索引的子範圍。</span><span class="sxs-lookup"><span data-stu-id="f931e-151">In this way, subranges of an index can be counted exactly.</span></span> <span data-ttu-id="f931e-152">資料指標應該定位至範圍中的第一個資料列。</span><span class="sxs-lookup"><span data-stu-id="f931e-152">The cursor should be positioned to the first row in the range.</span></span> <span data-ttu-id="f931e-153">應該建立範圍索引鍵的結尾，然後 [JetSetIndexRange](./jetsetindexrange-function.md) 應該用來設定以上的範圍（包括或僅限）。</span><span class="sxs-lookup"><span data-stu-id="f931e-153">The end of the range key should be made and then [JetSetIndexRange](./jetsetindexrange-function.md) should be used to set the upper range, either inclusively or exclusively.</span></span> <span data-ttu-id="f931e-154">最後，應呼叫 **JetIndexRecordCount** 來精確計算範圍。</span><span class="sxs-lookup"><span data-stu-id="f931e-154">Lastly, **JetIndexRecordCount** should be called to exactly count the range.</span></span>

<span data-ttu-id="f931e-155">**JetIndexRecordCount** 會遵守交易語義，並傳回在其目前交易狀態下，此特定會話精確的計數。</span><span class="sxs-lookup"><span data-stu-id="f931e-155">**JetIndexRecordCount** obeys transaction semantics and returns a count that is accurate for this particular session in its current transactional state.</span></span>

<span data-ttu-id="f931e-156">**JetIndexRecordCount** 會存取索引分葉頁面，以便精確地計算專案。</span><span class="sxs-lookup"><span data-stu-id="f931e-156">**JetIndexRecordCount** accesses index leaf pages in order to exactly count entries.</span></span> <span data-ttu-id="f931e-157">因此，它可以執行大量 i/o，而且可能很慢。</span><span class="sxs-lookup"><span data-stu-id="f931e-157">Consequently, it can perform a great deal of I/O and can be slow.</span></span> <span data-ttu-id="f931e-158">*CrecMax* 限制應該用來防止過度負載。</span><span class="sxs-lookup"><span data-stu-id="f931e-158">The *crecMax* limitation should be used to prevent excessive load.</span></span> <span data-ttu-id="f931e-159">如果範圍很大，則可能使用 [JetGetRecordPosition](./jetgetrecordposition-function.md)以近似值的方式計算範圍。</span><span class="sxs-lookup"><span data-stu-id="f931e-159">If a range is large, then it might be possible to count the range in an approximated fashion using [JetGetRecordPosition](./jetgetrecordposition-function.md).</span></span>

<span data-ttu-id="f931e-160">**WINDOWS XP、Windows Server 2003、windows 2000 Server 及 windows 2000 Professional：**  如果資料指標位於空的索引或索引範圍上， **JetIndexRecordCount** 會錯誤地傳回 JET_errNoCurrentRecord 而不是傳回零的記錄計數。</span><span class="sxs-lookup"><span data-stu-id="f931e-160">**Windows XP, Windows Server 2003, Windows 2000 Server, and Windows 2000 Professional:**  If the cursor is positioned on an empty index or index range then **JetIndexRecordCount** erroneously returns JET_errNoCurrentRecord rather than returning a record count of zero.</span></span> <span data-ttu-id="f931e-161">在此情況下，應用程式應該查看索引或索引範圍是否為空白。</span><span class="sxs-lookup"><span data-stu-id="f931e-161">The application should check to see if the index or index range is empty in this case.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f931e-162">規格需求</span><span class="sxs-lookup"><span data-stu-id="f931e-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f931e-163"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="f931e-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f931e-164">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="f931e-164">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f931e-165"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="f931e-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f931e-166">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="f931e-166">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f931e-167"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="f931e-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f931e-168">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="f931e-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f931e-169"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="f931e-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f931e-170">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="f931e-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f931e-171"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f931e-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f931e-172">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="f931e-172">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f931e-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f931e-173">See Also</span></span>

[<span data-ttu-id="f931e-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f931e-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f931e-175">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="f931e-175">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="f931e-176">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="f931e-176">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="f931e-177">JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="f931e-177">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)  
[<span data-ttu-id="f931e-178">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="f931e-178">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)  
[<span data-ttu-id="f931e-179">JetStopService</span><span class="sxs-lookup"><span data-stu-id="f931e-179">JetStopService</span></span>](./jetstopservice-function.md)
