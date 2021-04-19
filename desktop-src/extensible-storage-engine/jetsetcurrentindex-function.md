---
description: 深入瞭解： JetSetCurrentIndex 函數
title: JetSetCurrentIndex 函式
TOCTitle: JetSetCurrentIndex Function
ms:assetid: a2a15eab-b8bf-4a67-a63a-830ed1fdb3d9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294046(v=EXCHG.10)
ms:contentKeyID: 32765645
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex
- JetSetCurrentIndexA
- JetSetCurrentIndexW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7698a12f470fadd5c43dc2afe23f95f8e51bdf66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971184"
---
# <a name="jetsetcurrentindex-function"></a><span data-ttu-id="66e3b-103">JetSetCurrentIndex 函式</span><span class="sxs-lookup"><span data-stu-id="66e3b-103">JetSetCurrentIndex Function</span></span>


<span data-ttu-id="66e3b-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="66e3b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcurrentindex-function"></a><span data-ttu-id="66e3b-105">JetSetCurrentIndex 函式</span><span class="sxs-lookup"><span data-stu-id="66e3b-105">JetSetCurrentIndex Function</span></span>

<span data-ttu-id="66e3b-106">**JetSetCurrentIndex** 函數可以用來設定資料指標目前的索引。</span><span class="sxs-lookup"><span data-stu-id="66e3b-106">The **JetSetCurrentIndex** function can be used to set the current index of a cursor.</span></span> <span data-ttu-id="66e3b-107">資料指標的目前索引會定義資料表中的哪些記錄可以顯示在該資料指標，以及選取一組要用來公開這些記錄的索引項目目順序。</span><span class="sxs-lookup"><span data-stu-id="66e3b-107">The current index of a cursor defines which records in a table are visible to that cursor and the order in which they appear by selecting the set of index entries to use to expose those records.</span></span>

```cpp
    JET_ERR JET_API JetSetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      const tchar* szIndexName
    );
```

### <a name="parameters"></a><span data-ttu-id="66e3b-108">參數</span><span class="sxs-lookup"><span data-stu-id="66e3b-108">Parameters</span></span>

<span data-ttu-id="66e3b-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="66e3b-109">*sesid*</span></span>

<span data-ttu-id="66e3b-110">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="66e3b-110">The session to use for this call.</span></span>

<span data-ttu-id="66e3b-111">*tableid*</span><span class="sxs-lookup"><span data-stu-id="66e3b-111">*tableid*</span></span>

<span data-ttu-id="66e3b-112">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="66e3b-112">The cursor to use for this call.</span></span>

<span data-ttu-id="66e3b-113">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="66e3b-113">*szIndexName*</span></span>

<span data-ttu-id="66e3b-114">要為數據指標選取的索引名稱。</span><span class="sxs-lookup"><span data-stu-id="66e3b-114">The name of the index to be selected for the cursor.</span></span>

<span data-ttu-id="66e3b-115">如果此參數為 Null 或空字串，則會選取叢集索引。</span><span class="sxs-lookup"><span data-stu-id="66e3b-115">If this parameter is NULL or an empty string then the clustered index will be selected.</span></span> <span data-ttu-id="66e3b-116">如果定義了資料表的主要索引，則會選取該索引，因為它與叢集索引相同。</span><span class="sxs-lookup"><span data-stu-id="66e3b-116">If a primary index is defined for the table then that index will be selected because it is the same as the clustered index.</span></span> <span data-ttu-id="66e3b-117">如果未定義資料表的主要索引，則會選取連續索引。</span><span class="sxs-lookup"><span data-stu-id="66e3b-117">If no primary index is defined for the table then the sequential index will be selected.</span></span> <span data-ttu-id="66e3b-118">順序索引沒有索引定義。</span><span class="sxs-lookup"><span data-stu-id="66e3b-118">The sequential index has no index definition.</span></span> <span data-ttu-id="66e3b-119">如需詳細資訊，請參閱 [JetCreateIndex](./jetcreateindex-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="66e3b-119">See [JetCreateIndex](./jetcreateindex-function.md) for more information.</span></span>

<span data-ttu-id="66e3b-120">如果 *pindexid* 不是 Null，則會忽略索引名稱，並且會依索引識別碼來選取索引。</span><span class="sxs-lookup"><span data-stu-id="66e3b-120">If *pindexid* is not NULL then the index name will be ignored and the index will be selected by its index ID.</span></span>

### <a name="return-value"></a><span data-ttu-id="66e3b-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="66e3b-121">Return Value</span></span>

<span data-ttu-id="66e3b-122">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="66e3b-122">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="66e3b-123">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="66e3b-123">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="66e3b-124">傳回碼</span><span class="sxs-lookup"><span data-stu-id="66e3b-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="66e3b-125">Description</span><span class="sxs-lookup"><span data-stu-id="66e3b-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66e3b-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="66e3b-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="66e3b-127">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="66e3b-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66e3b-128">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="66e3b-128">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="66e3b-129">正在使用 JET_bitNoMove 選項來選取次要索引，且新索引定義中的第一個多重值索引鍵資料行沒有對應至指定序號的值。</span><span class="sxs-lookup"><span data-stu-id="66e3b-129">A secondary index is being selected with the JET_bitNoMove option and there is no value for the first multi-valued key column in the new index's definition that corresponds to the specified sequence number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66e3b-130">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="66e3b-130">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="66e3b-131">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="66e3b-131">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66e3b-132">JET_errInvalidIndexId</span><span class="sxs-lookup"><span data-stu-id="66e3b-132">JET_errInvalidIndexId</span></span></p></td>
<td><p><span data-ttu-id="66e3b-133">索引識別碼的內容無效或已過期，需要重新整理。</span><span class="sxs-lookup"><span data-stu-id="66e3b-133">The contents of the index ID were not valid or have expired and need to be refreshed.</span></span> <span data-ttu-id="66e3b-134">在下列情況下， <strong>JetSetCurrentIndex</strong> 可能會發生：</span><span class="sxs-lookup"><span data-stu-id="66e3b-134">This can happen for <strong>JetSetCurrentIndex</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="66e3b-135">pindexid- &gt; cbStruct 不是 (Windows Server 2003 和更新版本) 的預期大小。</span><span class="sxs-lookup"><span data-stu-id="66e3b-135">pindexid-&gt;cbStruct is not of the expected size (Windows Server 2003 and later releases).</span></span></p></li>
<li><p><span data-ttu-id="66e3b-136">引擎已在提取索引識別碼之後關閉。</span><span class="sxs-lookup"><span data-stu-id="66e3b-136">The engine has been shut down since the index ID was fetched.</span></span></p></li>
<li><p><span data-ttu-id="66e3b-137">所有參考資料表的資料指標（包含對應至索引識別碼的索引）已關閉，且引擎已從架構快取中收回該索引的定義。</span><span class="sxs-lookup"><span data-stu-id="66e3b-137">All cursors referencing the table containing the index corresponding to the index ID have been closed and the engine has evicted that index's definition from the schema cache.</span></span></p></li>
<li><p><span data-ttu-id="66e3b-138">索引識別碼正在搭配在錯誤資料表上開啟的資料指標使用。</span><span class="sxs-lookup"><span data-stu-id="66e3b-138">The index ID is being used with a cursor opened on the wrong table.</span></span></p></li>
<li><p><span data-ttu-id="66e3b-139">索引已卸載或尚未顯示在會話中。</span><span class="sxs-lookup"><span data-stu-id="66e3b-139">The index has been dropped or is not yet visible to the session.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66e3b-140">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="66e3b-140">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="66e3b-141">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="66e3b-141">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="66e3b-142">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="66e3b-142">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66e3b-143">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="66e3b-143">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="66e3b-144">其中一個指定的物件名稱無效。</span><span class="sxs-lookup"><span data-stu-id="66e3b-144">One of the specified object names was invalid.</span></span> <span data-ttu-id="66e3b-145">所有物件名稱都必須符合同一組規則。</span><span class="sxs-lookup"><span data-stu-id="66e3b-145">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="66e3b-146">這些規則如下：</span><span class="sxs-lookup"><span data-stu-id="66e3b-146">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="66e3b-147">物件名稱必須由 ASCII 字元組成。</span><span class="sxs-lookup"><span data-stu-id="66e3b-147">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="66e3b-148">物件名稱的長度必須至少有一個字元。</span><span class="sxs-lookup"><span data-stu-id="66e3b-148">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="66e3b-149">物件名稱的長度不得超過 JET_cbNameMost (64) 個字元。</span><span class="sxs-lookup"><span data-stu-id="66e3b-149">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="66e3b-150">物件名稱不能以空格開頭。</span><span class="sxs-lookup"><span data-stu-id="66e3b-150">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="66e3b-151">物件名稱不能包含 ASCII 控制字元 (0x00 到 0x1F) 。</span><span class="sxs-lookup"><span data-stu-id="66e3b-151">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="66e3b-152">物件名稱不能包含驚嘆號 (！ ) 、句號 (. ) 、左括弧 ( [) 或右括弧 (] ) 字元。</span><span class="sxs-lookup"><span data-stu-id="66e3b-152">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="66e3b-153">一旦經過驗證之後，就只會將字串的部分寫入第一個空格 (如果有任何) 將用於物件名稱。</span><span class="sxs-lookup"><span data-stu-id="66e3b-153">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="66e3b-154">這實際上是指物件名稱不能包含空格。</span><span class="sxs-lookup"><span data-stu-id="66e3b-154">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66e3b-155">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="66e3b-155">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="66e3b-156">提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="66e3b-156">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="66e3b-157">當<em>pindexid</em>不是 Null，且 pindexid cbStruct 的大小不是 (Windows XP 和舊版) 的預期大小<strong>時，就</strong>可能會發生這種情況 &gt; 。</span><span class="sxs-lookup"><span data-stu-id="66e3b-157">This can happen for <strong>JetSetCurrentIndex</strong> when <em>pindexid</em> is not NULL and pindexid-&gt;cbStruct is not of the expected size (Windows XP and earlier releases).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66e3b-158">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="66e3b-158">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="66e3b-159">正在使用 JET_bitNoMove 選項來選取次要索引，而新的索引中沒有索引項目對應至在舊索引上目前的資料指標位置與索引項目目相關聯的記錄。</span><span class="sxs-lookup"><span data-stu-id="66e3b-159">A secondary index is being selected with the JET_bitNoMove option and there is no index entry in the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66e3b-160">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="66e3b-160">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="66e3b-161">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="66e3b-161">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66e3b-162">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="66e3b-162">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="66e3b-163">引擎已用盡用來開啟資料指標的資源集區。</span><span class="sxs-lookup"><span data-stu-id="66e3b-163">The engine has exhausted its pool of resources used to open cursors.</span></span> <span data-ttu-id="66e3b-164">可以在任何時間開啟的資料指標數目上限是使用 <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>來控制。</span><span class="sxs-lookup"><span data-stu-id="66e3b-164">The maximum number of cursors that can be opened at any one time is controlled using <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span> <span data-ttu-id="66e3b-165">如需詳細資訊，請參閱 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 。</span><span class="sxs-lookup"><span data-stu-id="66e3b-165">See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for more information.</span></span> <span data-ttu-id="66e3b-166">當選取次要索引，且引擎無法開啟內部資料指標來使用該索引時， <strong>JetSetCurrentIndex</strong> 就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="66e3b-166">This can happen for <strong>JetSetCurrentIndex</strong> when a secondary index has been selected and the engine cannot open an internal cursor to use that index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66e3b-167">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="66e3b-167">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="66e3b-168">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="66e3b-168">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66e3b-169">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="66e3b-169">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="66e3b-170">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="66e3b-170">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="66e3b-171">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="66e3b-171">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66e3b-172">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="66e3b-172">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="66e3b-173">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="66e3b-173">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="66e3b-174">成功時，會將資料指標的目前索引設定為要求的索引。</span><span class="sxs-lookup"><span data-stu-id="66e3b-174">On success, the current index of the cursor is set to the requested index.</span></span> <span data-ttu-id="66e3b-175">根據所要求索引的索引定義，現在可以使用 [JetSeek](./jetseek-function.md) 來搜尋索引項目。</span><span class="sxs-lookup"><span data-stu-id="66e3b-175">Index entries may now be sought using [JetSeek](./jetseek-function.md) according to the index definition of the requested index.</span></span> <span data-ttu-id="66e3b-176">您也可以使用 [JetMove](./jetmove-function.md) ，以該索引定義所指定的順序來列舉索引項目。</span><span class="sxs-lookup"><span data-stu-id="66e3b-176">Index entries may also be enumerated using [JetMove](./jetmove-function.md) in the order specified by that index definition.</span></span> <span data-ttu-id="66e3b-177">資料指標的目前位置是設定為索引上的第一個索引項目目 (JET_bitMoveFirst) 或與舊索引 (JET_bitNoMove) 上目前的資料指標位置相關的特定索引項目。</span><span class="sxs-lookup"><span data-stu-id="66e3b-177">The current position of the cursor is either set to the first index entry on the index (JET_bitMoveFirst) or to a specific index entry that is related to the current position of the cursor on the old index (JET_bitNoMove).</span></span> <span data-ttu-id="66e3b-178">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="66e3b-178">No change to the database state will occur.</span></span>

<span data-ttu-id="66e3b-179">失敗時，目前的索引和目前的資料指標位置處於未定義狀態。</span><span class="sxs-lookup"><span data-stu-id="66e3b-179">On failure, the current index and current position of the cursor are in an undefined state.</span></span> <span data-ttu-id="66e3b-180">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="66e3b-180">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="66e3b-181">備註</span><span class="sxs-lookup"><span data-stu-id="66e3b-181">Remarks</span></span>

<span data-ttu-id="66e3b-182">如果索引識別碼提示已過時，則 API 只會失敗。</span><span class="sxs-lookup"><span data-stu-id="66e3b-182">If the index ID hint is stale then the API simply fails.</span></span> <span data-ttu-id="66e3b-183">在此情況下，不會回復到索引的文字名稱。</span><span class="sxs-lookup"><span data-stu-id="66e3b-183">There is no fallback to the text name of the index in this case as one might expect.</span></span> <span data-ttu-id="66e3b-184">此回復必須由 API 的呼叫端手動完成。</span><span class="sxs-lookup"><span data-stu-id="66e3b-184">This fallback must be done manually by the caller of the API.</span></span>

#### <a name="requirements"></a><span data-ttu-id="66e3b-185">規格需求</span><span class="sxs-lookup"><span data-stu-id="66e3b-185">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66e3b-186"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="66e3b-186"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="66e3b-187">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="66e3b-187">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66e3b-188"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="66e3b-188"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="66e3b-189">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="66e3b-189">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66e3b-190"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="66e3b-190"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="66e3b-191">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="66e3b-191">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66e3b-192"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="66e3b-192"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="66e3b-193">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="66e3b-193">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66e3b-194"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="66e3b-194"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="66e3b-195">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="66e3b-195">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66e3b-196"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="66e3b-196"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="66e3b-197">實作為 <strong>JetSetCurrentIndexW</strong> (Unicode) 和 <strong>JetSetCurrentIndexA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="66e3b-197">Implemented as <strong>JetSetCurrentIndexW</strong> (Unicode) and <strong>JetSetCurrentIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="66e3b-198">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66e3b-198">See Also</span></span>

[<span data-ttu-id="66e3b-199">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="66e3b-199">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="66e3b-200">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="66e3b-200">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="66e3b-201">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="66e3b-201">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="66e3b-202">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="66e3b-202">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="66e3b-203">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="66e3b-203">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="66e3b-204">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="66e3b-204">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="66e3b-205">JetGetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="66e3b-205">JetGetCurrentIndex</span></span>](./jetgetcurrentindex-function.md)  
[<span data-ttu-id="66e3b-206">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="66e3b-206">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="66e3b-207">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="66e3b-207">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="66e3b-208">JetMove</span><span class="sxs-lookup"><span data-stu-id="66e3b-208">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="66e3b-209">JetSeek</span><span class="sxs-lookup"><span data-stu-id="66e3b-209">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="66e3b-210">JetSetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="66e3b-210">JetSetCurrentIndex</span></span>]()  
[<span data-ttu-id="66e3b-211">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="66e3b-211">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="66e3b-212">JetStopService</span><span class="sxs-lookup"><span data-stu-id="66e3b-212">JetStopService</span></span>](./jetstopservice-function.md)
