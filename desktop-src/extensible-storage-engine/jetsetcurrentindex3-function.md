---
description: 深入瞭解： JetSetCurrentIndex3 函數
title: JetSetCurrentIndex3 函式
TOCTitle: JetSetCurrentIndex3 Function
ms:assetid: 50050bd3-4b74-4be7-985c-754ced8aded1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269244(v=EXCHG.10)
ms:contentKeyID: 32765546
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex3A
- JetSetCurrentIndex3W
- JetSetCurrentIndex3
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8b97aa356d44ab72f7cd240a42351d9962777ef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971367"
---
# <a name="jetsetcurrentindex3-function"></a><span data-ttu-id="0de7c-103">JetSetCurrentIndex3 函式</span><span class="sxs-lookup"><span data-stu-id="0de7c-103">JetSetCurrentIndex3 Function</span></span>


<span data-ttu-id="0de7c-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0de7c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcurrentindex3-function"></a><span data-ttu-id="0de7c-105">JetSetCurrentIndex3 函式</span><span class="sxs-lookup"><span data-stu-id="0de7c-105">JetSetCurrentIndex3 Function</span></span>

<span data-ttu-id="0de7c-106">**JetSetCurrentIndex3** 函數是用來設定資料指標的目前索引。</span><span class="sxs-lookup"><span data-stu-id="0de7c-106">The **JetSetCurrentIndex3** function is used to set the current index of a cursor.</span></span> <span data-ttu-id="0de7c-107">資料指標的目前索引會定義資料表中的哪些記錄可以顯示在該資料指標，以及選取一組要用來公開這些記錄的索引項目目順序。</span><span class="sxs-lookup"><span data-stu-id="0de7c-107">The current index of a cursor defines which records in a table are visible to that cursor and the order in which they appear by selecting the set of index entries to use to expose those records.</span></span>

```cpp
    JET_ERR JET_API JetSetCurrentIndex3(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit,
      __in          unsigned long itagSequence
    );
```

### <a name="parameters"></a><span data-ttu-id="0de7c-108">參數</span><span class="sxs-lookup"><span data-stu-id="0de7c-108">Parameters</span></span>

<span data-ttu-id="0de7c-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="0de7c-109">*sesid*</span></span>

<span data-ttu-id="0de7c-110">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="0de7c-110">The session to use for this call.</span></span>

<span data-ttu-id="0de7c-111">*tableid*</span><span class="sxs-lookup"><span data-stu-id="0de7c-111">*tableid*</span></span>

<span data-ttu-id="0de7c-112">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="0de7c-112">The cursor to use for this call.</span></span>

<span data-ttu-id="0de7c-113">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="0de7c-113">*szIndexName*</span></span>

<span data-ttu-id="0de7c-114">要為數據指標選取的索引名稱。</span><span class="sxs-lookup"><span data-stu-id="0de7c-114">The name of the index to be selected for the cursor.</span></span>

<span data-ttu-id="0de7c-115">如果此參數為 Null 或空字串，則會選取叢集索引。</span><span class="sxs-lookup"><span data-stu-id="0de7c-115">If this parameter is NULL or an empty string then the clustered index will be selected.</span></span> <span data-ttu-id="0de7c-116">如果定義了資料表的主要索引，則會選取該索引，因為它與叢集索引相同。</span><span class="sxs-lookup"><span data-stu-id="0de7c-116">If a primary index is defined for the table then that index will be selected because it is the same as the clustered index.</span></span> <span data-ttu-id="0de7c-117">如果未定義資料表的主要索引，則會選取連續索引。</span><span class="sxs-lookup"><span data-stu-id="0de7c-117">If no primary index is defined for the table then the sequential index will be selected.</span></span> <span data-ttu-id="0de7c-118">順序索引沒有索引定義。</span><span class="sxs-lookup"><span data-stu-id="0de7c-118">The sequential index has no index definition.</span></span> <span data-ttu-id="0de7c-119">如需詳細資訊，請參閱 [JetCreateIndex](./jetcreateindex-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="0de7c-119">See [JetCreateIndex](./jetcreateindex-function.md) for more information.</span></span>

<span data-ttu-id="0de7c-120">如果 *pindexid* 不是 Null，則會忽略索引名稱，並且會依索引識別碼來選取索引。</span><span class="sxs-lookup"><span data-stu-id="0de7c-120">If *pindexid* is not NULL then the index name will be ignored and the index will be selected by its index ID.</span></span>

<span data-ttu-id="0de7c-121">*grbit*</span><span class="sxs-lookup"><span data-stu-id="0de7c-121">*grbit*</span></span>

<span data-ttu-id="0de7c-122">位群組，其中包含要用於此呼叫的選項，包括下列零或多個。</span><span class="sxs-lookup"><span data-stu-id="0de7c-122">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0de7c-123">值</span><span class="sxs-lookup"><span data-stu-id="0de7c-123">Value</span></span></p></th>
<th><p><span data-ttu-id="0de7c-124">意義</span><span class="sxs-lookup"><span data-stu-id="0de7c-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0de7c-125">JET_bitMoveFirst</span><span class="sxs-lookup"><span data-stu-id="0de7c-125">JET_bitMoveFirst</span></span></p></td>
<td><p><span data-ttu-id="0de7c-126">此選項表示資料指標應放置在指定之索引的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="0de7c-126">This option indicates that the cursor should be positioned on the first entry of the specified index.</span></span> <span data-ttu-id="0de7c-127">如果選取叢集索引 (主要索引或連續索引) ，而且目前的索引是次要索引，則會假設 JET_bitMoveFirst。</span><span class="sxs-lookup"><span data-stu-id="0de7c-127">If the clustered index is being selected (primary index or sequential index) and the current index is a secondary index then JET_bitMoveFirst is assumed.</span></span> <span data-ttu-id="0de7c-128">如果正在選取目前的索引，則會忽略此選項，且不會變更資料指標的位置。</span><span class="sxs-lookup"><span data-stu-id="0de7c-128">If the current index is being selected then this option is ignored and no change to the cursor position is made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0de7c-129">JET_bitNoMove</span><span class="sxs-lookup"><span data-stu-id="0de7c-129">JET_bitNoMove</span></span></p></td>
<td><p><span data-ttu-id="0de7c-130">此選項表示資料指標應放置在新索引的索引項目上，此索引會對應到與舊索引上之資料指標目前位置的索引項目目相關聯的記錄。</span><span class="sxs-lookup"><span data-stu-id="0de7c-130">This option indicates that the cursor should be positioned on the index entry of the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p>
<p><span data-ttu-id="0de7c-131">如果新索引的定義至少包含一個多重值索引鍵資料行，則目的地索引項目不明確。</span><span class="sxs-lookup"><span data-stu-id="0de7c-131">If the definition for the new index contains at least one multi-valued key column then the destination index entry is ambiguous.</span></span> <span data-ttu-id="0de7c-132">在此情況下，會使用指定的 <em>itagSequence</em> 來選取最重要的多重值索引鍵資料行用來放置資料指標的多重值。</span><span class="sxs-lookup"><span data-stu-id="0de7c-132">In this case, the specified <em>itagSequence</em> is used to select which multi-value of the most significant multi-valued key column is used to position the cursor.</span></span> <span data-ttu-id="0de7c-133">即使在多個多重值索引鍵資料行的情況下，只需要傳遞單一 <em>itagSequence</em> ，因為引擎只會展開最重要多重值索引鍵資料行的所有值。</span><span class="sxs-lookup"><span data-stu-id="0de7c-133">It is only necessary to pass a single <em>itagSequence</em> even in the case of multiple multi-valued key columns because the engine only expands all values for the most significant multi-valued key column.</span></span> <span data-ttu-id="0de7c-134">如需詳細資訊，請參閱 <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> 。</span><span class="sxs-lookup"><span data-stu-id="0de7c-134">See <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> for more details.</span></span></p>
<p><span data-ttu-id="0de7c-135">如果指定 JET_bitMoveFirst，則會忽略此選項。</span><span class="sxs-lookup"><span data-stu-id="0de7c-135">If JET_bitMoveFirst is specified then this option is ignored.</span></span></p>
<p><span data-ttu-id="0de7c-136">如果正在選取目前的索引，則會忽略此選項，且不會變更資料指標的位置。</span><span class="sxs-lookup"><span data-stu-id="0de7c-136">If the current index is being selected then this option is ignored and no change to the cursor position is made.</span></span> <span data-ttu-id="0de7c-137">如果這個參數不存在，則會假設其值為 JET_bitMoveFirst。</span><span class="sxs-lookup"><span data-stu-id="0de7c-137">When this parameter is not present, its value is presumed to be JET_bitMoveFirst.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0de7c-138">*itagSequence*</span><span class="sxs-lookup"><span data-stu-id="0de7c-138">*itagSequence*</span></span>

<span data-ttu-id="0de7c-139">多值資料行值的序號，此值會用來將資料指標放置在新的索引上。</span><span class="sxs-lookup"><span data-stu-id="0de7c-139">Sequence number of the multi-valued column value which will be used to position the cursor on the new index.</span></span>

<span data-ttu-id="0de7c-140">此參數只會搭配 JET_bitNoMove 使用。</span><span class="sxs-lookup"><span data-stu-id="0de7c-140">This parameter is only used in conjunction with JET_bitNoMove.</span></span> <span data-ttu-id="0de7c-141">如需詳細資訊，請參閱此選項的描述。</span><span class="sxs-lookup"><span data-stu-id="0de7c-141">See the description of this option for more details.</span></span>

<span data-ttu-id="0de7c-142">當這個參數不存在或設為零時，其值會假設為1。</span><span class="sxs-lookup"><span data-stu-id="0de7c-142">When this parameter is not present or is set to zero, its value is presumed to be 1.</span></span>

### <a name="return-value"></a><span data-ttu-id="0de7c-143">傳回值</span><span class="sxs-lookup"><span data-stu-id="0de7c-143">Return Value</span></span>

<span data-ttu-id="0de7c-144">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="0de7c-144">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="0de7c-145">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="0de7c-145">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0de7c-146">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0de7c-146">Return code</span></span></p></th>
<th><p><span data-ttu-id="0de7c-147">Description</span><span class="sxs-lookup"><span data-stu-id="0de7c-147">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0de7c-148">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="0de7c-148">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="0de7c-149">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="0de7c-149">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0de7c-150">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="0de7c-150">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="0de7c-151">正在使用 JET_bitNoMove 選項來選取次要索引，且新索引定義中的第一個多重值索引鍵資料行沒有對應至指定序號的值。</span><span class="sxs-lookup"><span data-stu-id="0de7c-151">A secondary index is being selected with the JET_bitNoMove option and there is no value for the first multi-valued key column in the new index's definition that corresponds to the specified sequence number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0de7c-152">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="0de7c-152">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="0de7c-153">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="0de7c-153">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0de7c-154">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="0de7c-154">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="0de7c-155">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="0de7c-155">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="0de7c-156">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="0de7c-156">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0de7c-157">JET_errInvalidIndexId</span><span class="sxs-lookup"><span data-stu-id="0de7c-157">JET_errInvalidIndexId</span></span></p></td>
<td><p><span data-ttu-id="0de7c-158">索引識別碼的內容無效或已過期，需要重新整理。</span><span class="sxs-lookup"><span data-stu-id="0de7c-158">The contents of the index ID were not valid or have expired and need to be refreshed.</span></span> <span data-ttu-id="0de7c-159">在下列情況下， <strong>JetSetCurrentIndex3</strong> 可能會發生：</span><span class="sxs-lookup"><span data-stu-id="0de7c-159">This can happen for <strong>JetSetCurrentIndex3</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="0de7c-160">pindexid- &gt; cbStruct 不是 (Windows Server 2003 和更新版本) 的預期大小。</span><span class="sxs-lookup"><span data-stu-id="0de7c-160">pindexid-&gt;cbStruct is not of the expected size (Windows Server 2003 and later releases).</span></span></p></li>
<li><p><span data-ttu-id="0de7c-161">引擎已在提取索引識別碼之後關閉。</span><span class="sxs-lookup"><span data-stu-id="0de7c-161">The engine has been shut down since the index ID was fetched.</span></span></p></li>
<li><p><span data-ttu-id="0de7c-162">所有參考資料表的資料指標（包含對應至索引識別碼的索引）已關閉，且引擎已從架構快取中收回該索引的定義。</span><span class="sxs-lookup"><span data-stu-id="0de7c-162">All cursors referencing the table containing the index corresponding to the index ID have been closed and the engine has evicted the definition for that index from the schema cache.</span></span></p></li>
<li><p><span data-ttu-id="0de7c-163">索引識別碼正在搭配在錯誤資料表上開啟的資料指標使用。</span><span class="sxs-lookup"><span data-stu-id="0de7c-163">The index ID is being used with a cursor opened on the wrong table.</span></span></p></li>
<li><p><span data-ttu-id="0de7c-164">索引已卸載或尚未顯示在會話中。</span><span class="sxs-lookup"><span data-stu-id="0de7c-164">The index has been dropped or is not yet visible to the session.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0de7c-165">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="0de7c-165">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="0de7c-166">其中一個指定的物件名稱無效。</span><span class="sxs-lookup"><span data-stu-id="0de7c-166">One of the specified object names was invalid.</span></span> <span data-ttu-id="0de7c-167">所有物件名稱都必須符合同一組規則。</span><span class="sxs-lookup"><span data-stu-id="0de7c-167">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="0de7c-168">這些規則如下：</span><span class="sxs-lookup"><span data-stu-id="0de7c-168">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="0de7c-169">物件名稱必須由 ASCII 字元組成。</span><span class="sxs-lookup"><span data-stu-id="0de7c-169">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="0de7c-170">物件名稱的長度必須至少有一個字元。</span><span class="sxs-lookup"><span data-stu-id="0de7c-170">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="0de7c-171">物件名稱的長度不得超過 JET_cbNameMost (64) 個字元。</span><span class="sxs-lookup"><span data-stu-id="0de7c-171">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="0de7c-172">物件名稱不能以空格開頭。</span><span class="sxs-lookup"><span data-stu-id="0de7c-172">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="0de7c-173">物件名稱不能包含 ASCII 控制字元 (0x00 到 0x1F) 。</span><span class="sxs-lookup"><span data-stu-id="0de7c-173">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="0de7c-174">物件名稱不能包含驚嘆號 (！ ) 、句號 (. ) 、左括弧 ( [) 或右括弧 (] ) 字元。</span><span class="sxs-lookup"><span data-stu-id="0de7c-174">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="0de7c-175">一旦經過驗證之後，就只會將字串的部分寫入第一個空格 (如果有任何) 將用於物件名稱。</span><span class="sxs-lookup"><span data-stu-id="0de7c-175">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="0de7c-176">這實際上是指物件名稱不能包含空格。</span><span class="sxs-lookup"><span data-stu-id="0de7c-176">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0de7c-177">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="0de7c-177">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="0de7c-178">提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="0de7c-178">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="0de7c-179">當<em>pindexid</em>不是 Null，且 pindexid cbStruct 的大小不是 (Windows XP 和舊版) 的預期大小<strong>時，就</strong>可能會發生這種情況 &gt; 。</span><span class="sxs-lookup"><span data-stu-id="0de7c-179">This can happen for <strong>JetSetCurrentIndex3</strong> when <em>pindexid</em> is not NULL and pindexid-&gt;cbStruct is not of the expected size (Windows XP and earlier releases).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0de7c-180">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="0de7c-180">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="0de7c-181">正在使用 JET_bitNoMove 選項來選取次要索引，而新的索引中沒有索引項目對應至在舊索引上目前的資料指標位置與索引項目目相關聯的記錄。</span><span class="sxs-lookup"><span data-stu-id="0de7c-181">A secondary index is being selected with the JET_bitNoMove option and there is no index entry in the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0de7c-182">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="0de7c-182">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="0de7c-183">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="0de7c-183">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0de7c-184">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="0de7c-184">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="0de7c-185">引擎已用盡用來開啟資料指標的資源集區。</span><span class="sxs-lookup"><span data-stu-id="0de7c-185">The engine has exhausted its pool of resources used to open cursors.</span></span> <span data-ttu-id="0de7c-186">可以在任何時間開啟的資料指標數目上限是使用 <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>來控制。</span><span class="sxs-lookup"><span data-stu-id="0de7c-186">The maximum number of cursors that can be opened at any one time is controlled using <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span> <span data-ttu-id="0de7c-187">如需詳細資訊，請參閱 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 。</span><span class="sxs-lookup"><span data-stu-id="0de7c-187">See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for more information.</span></span> <span data-ttu-id="0de7c-188">當選取次要索引，且引擎無法開啟內部資料指標來使用該索引時， <strong>JetSetCurrentIndex3</strong> 就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="0de7c-188">This can happen for <strong>JetSetCurrentIndex3</strong> when a secondary index has been selected and the engine cannot open an internal cursor to use that index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0de7c-189">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="0de7c-189">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="0de7c-190">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="0de7c-190">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0de7c-191">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="0de7c-191">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="0de7c-192">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="0de7c-192">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="0de7c-193">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="0de7c-193">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0de7c-194">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="0de7c-194">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="0de7c-195">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="0de7c-195">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0de7c-196">成功時，會將資料指標的目前索引設定為要求的索引。</span><span class="sxs-lookup"><span data-stu-id="0de7c-196">On success, the current index of the cursor is set to the requested index.</span></span> <span data-ttu-id="0de7c-197">根據所要求索引的索引定義，現在可以使用 [JetSeek](./jetseek-function.md) 來搜尋索引項目。</span><span class="sxs-lookup"><span data-stu-id="0de7c-197">Index entries may now be sought using [JetSeek](./jetseek-function.md) according to the index definition of the requested index.</span></span> <span data-ttu-id="0de7c-198">您也可以使用 [JetMove](./jetmove-function.md) ，以該索引定義所指定的順序來列舉索引項目。</span><span class="sxs-lookup"><span data-stu-id="0de7c-198">Index entries may also be enumerated using [JetMove](./jetmove-function.md) in the order specified by that index definition.</span></span> <span data-ttu-id="0de7c-199">資料指標的目前位置是設定為索引上的第一個索引項目目 (JET_bitMoveFirst) 或與舊索引 (JET_bitNoMove) 上目前的資料指標位置相關的特定索引項目。</span><span class="sxs-lookup"><span data-stu-id="0de7c-199">The current position of the cursor is either set to the first index entry on the index (JET_bitMoveFirst) or to a specific index entry that is related to the current position of the cursor on the old index (JET_bitNoMove).</span></span> <span data-ttu-id="0de7c-200">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="0de7c-200">No change to the database state will occur.</span></span>

<span data-ttu-id="0de7c-201">失敗時，目前的索引和目前的資料指標位置處於未定義狀態。</span><span class="sxs-lookup"><span data-stu-id="0de7c-201">On failure, the current index and current position of the cursor are in an undefined state.</span></span> <span data-ttu-id="0de7c-202">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="0de7c-202">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="0de7c-203">備註</span><span class="sxs-lookup"><span data-stu-id="0de7c-203">Remarks</span></span>

<span data-ttu-id="0de7c-204">如果索引識別碼提示已過時，則 API 只會失敗。</span><span class="sxs-lookup"><span data-stu-id="0de7c-204">If the index ID hint is stale then the API simply fails.</span></span> <span data-ttu-id="0de7c-205">在此情況下，不會回復到索引的文字名稱。</span><span class="sxs-lookup"><span data-stu-id="0de7c-205">There is no fallback to the text name of the index in this case as one might expect.</span></span> <span data-ttu-id="0de7c-206">此回復必須由 API 的呼叫端手動完成。</span><span class="sxs-lookup"><span data-stu-id="0de7c-206">This fallback must be done manually by the caller of the API.</span></span>

#### <a name="requirements"></a><span data-ttu-id="0de7c-207">規格需求</span><span class="sxs-lookup"><span data-stu-id="0de7c-207">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0de7c-208"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="0de7c-208"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0de7c-209">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="0de7c-209">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0de7c-210"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="0de7c-210"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0de7c-211">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="0de7c-211">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0de7c-212"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="0de7c-212"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0de7c-213">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="0de7c-213">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0de7c-214"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="0de7c-214"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="0de7c-215">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="0de7c-215">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0de7c-216"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="0de7c-216"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="0de7c-217">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="0de7c-217">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0de7c-218"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="0de7c-218"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="0de7c-219">實作為 <strong>JetSetCurrentIndex3W</strong> (Unicode) 和 <strong>JetSetCurrentIndex3A</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="0de7c-219">Implemented as <strong>JetSetCurrentIndex3W</strong> (Unicode) and <strong>JetSetCurrentIndex3A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="0de7c-220">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0de7c-220">See Also</span></span>

[<span data-ttu-id="0de7c-221">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0de7c-221">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0de7c-222">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="0de7c-222">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="0de7c-223">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="0de7c-223">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="0de7c-224">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="0de7c-224">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="0de7c-225">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="0de7c-225">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="0de7c-226">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="0de7c-226">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="0de7c-227">JetGetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="0de7c-227">JetGetCurrentIndex</span></span>](./jetgetcurrentindex-function.md)  
[<span data-ttu-id="0de7c-228">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="0de7c-228">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="0de7c-229">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="0de7c-229">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="0de7c-230">JetMove</span><span class="sxs-lookup"><span data-stu-id="0de7c-230">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="0de7c-231">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="0de7c-231">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="0de7c-232">JetSeek</span><span class="sxs-lookup"><span data-stu-id="0de7c-232">JetSeek</span></span>](./jetseek-function.md)
