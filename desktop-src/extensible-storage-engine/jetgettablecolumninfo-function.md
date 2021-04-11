---
description: 深入瞭解： JetGetTableColumnInfo 函數
title: JetGetTableColumnInfo 函式
TOCTitle: JetGetTableColumnInfo Function
ms:assetid: b1c1df22-ad33-4320-9f08-baf2a3e7bd7d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294061(v=EXCHG.10)
ms:contentKeyID: 32765676
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableColumnInfoW
- JetGetTableColumnInfoA
- JetGetTableColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f8c7b073ca9be90e89a1c6b99c010707e6405323
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104196483"
---
# <a name="jetgettablecolumninfo-function"></a><span data-ttu-id="23333-103">JetGetTableColumnInfo 函式</span><span class="sxs-lookup"><span data-stu-id="23333-103">JetGetTableColumnInfo Function</span></span>


<span data-ttu-id="23333-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="23333-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettablecolumninfo-function"></a><span data-ttu-id="23333-105">JetGetTableColumnInfo 函式</span><span class="sxs-lookup"><span data-stu-id="23333-105">JetGetTableColumnInfo Function</span></span>

<span data-ttu-id="23333-106">**JetGetTableColumnInfo** 函數會抓取資料表資料行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="23333-106">The **JetGetTableColumnInfo** function retrieves information about a table column.</span></span>

```cpp
JET_ERR JET_API JetGetTableColumnInfo(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName,
  __out         void* pvResult,
  __in          unsigned long cbMax,
  __in          unsigned long InfoLevel
);
```

### <a name="parameters"></a><span data-ttu-id="23333-107">參數</span><span class="sxs-lookup"><span data-stu-id="23333-107">Parameters</span></span>

<span data-ttu-id="23333-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="23333-108">*sesid*</span></span>

<span data-ttu-id="23333-109">要用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="23333-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="23333-110">*tableid*</span><span class="sxs-lookup"><span data-stu-id="23333-110">*tableid*</span></span>

<span data-ttu-id="23333-111">包含要提取資訊之資料行的資料表。</span><span class="sxs-lookup"><span data-stu-id="23333-111">The table that contains the column to fetch information for.</span></span>

<span data-ttu-id="23333-112">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="23333-112">*szColumnName*</span></span>

<span data-ttu-id="23333-113">要提取資訊的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="23333-113">The name of the column to fetch information for.</span></span>

<span data-ttu-id="23333-114">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="23333-114">*pvResult*</span></span>

<span data-ttu-id="23333-115">將接收資訊的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="23333-115">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="23333-116">緩衝區的類型取決於 *InfoLevel*。</span><span class="sxs-lookup"><span data-stu-id="23333-116">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="23333-117">呼叫端必須設定為適當地對齊緩衝區。</span><span class="sxs-lookup"><span data-stu-id="23333-117">The caller must be configured to align the buffer appropriately.</span></span>

<span data-ttu-id="23333-118">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="23333-118">*cbMax*</span></span>

<span data-ttu-id="23333-119">在 *pvResult* 中傳遞的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="23333-119">The size, in bytes, of the buffer that was passed in *pvResult*.</span></span>

<span data-ttu-id="23333-120">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="23333-120">*InfoLevel*</span></span>

<span data-ttu-id="23333-121">針對 *szColumnName* 所指定的資料行，將抓取的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="23333-121">The type of information that will be retrieved for the column that is specified by *szColumnName*.</span></span> <span data-ttu-id="23333-122">儲存在 *pvResult* 中的資料格式取決於 *InfoLevel*。</span><span class="sxs-lookup"><span data-stu-id="23333-122">The format of the data that is stored in *pvResult* is dependent on *InfoLevel*.</span></span> <span data-ttu-id="23333-123">如需臨時表的架構，請參閱 [JET_COLUMNLIST](./jet-columnlist-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="23333-123">For the schema of the temporary table, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

  - <span data-ttu-id="23333-124">JET_ColInfoListSortColumnid 會依 *columnid* 排序臨時表。</span><span class="sxs-lookup"><span data-stu-id="23333-124">JET_ColInfoListSortColumnid will sort the temporary table by *columnid*.</span></span>

  - <span data-ttu-id="23333-125">JET_ColInfoListCompact 將壓縮輸出。</span><span class="sxs-lookup"><span data-stu-id="23333-125">JET_ColInfoListCompact will compact the output.</span></span> <span data-ttu-id="23333-126">如需 compact 輸出的詳細資訊，請參閱 [JET_COLUMNLIST](./jet-columnlist-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="23333-126">For more information about the compact output, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

<span data-ttu-id="23333-127">您可以為此參數設定下列選項：</span><span class="sxs-lookup"><span data-stu-id="23333-127">The following options can be set for this parameter:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="23333-128">值</span><span class="sxs-lookup"><span data-stu-id="23333-128">Value</span></span></p></th>
<th><p><span data-ttu-id="23333-129">意義</span><span class="sxs-lookup"><span data-stu-id="23333-129">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23333-130">JET_ColInfo</span><span class="sxs-lookup"><span data-stu-id="23333-130">JET_ColInfo</span></span></p></td>
<td><p><span data-ttu-id="23333-131"><em>pvResult</em> 會被視為 <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>，而 <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> 結構的欄位會適當地填入。</span><span class="sxs-lookup"><span data-stu-id="23333-131"><em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, and the fields of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure are filled in appropriately.</span></span> <span data-ttu-id="23333-132">JET_ColInfo 和 JET_ColInfoByColid 都會取得相同的資訊。</span><span class="sxs-lookup"><span data-stu-id="23333-132">JET_ColInfo and JET_ColInfoByColid both retrieve the same information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23333-133">JET_ColInfoBase</span><span class="sxs-lookup"><span data-stu-id="23333-133">JET_ColInfoBase</span></span></p></td>
<td><p><span data-ttu-id="23333-134"><em>pvResult</em> 會被視為 <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> 結構。</span><span class="sxs-lookup"><span data-stu-id="23333-134"><em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> structure.</span></span> <span data-ttu-id="23333-135">這類似于 <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> 結構。</span><span class="sxs-lookup"><span data-stu-id="23333-135">This is similar to a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure.</span></span> <span data-ttu-id="23333-136">如果此函式成功，則會以適當的值填入結構。</span><span class="sxs-lookup"><span data-stu-id="23333-136">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="23333-137">如果此函式失敗，結構會包含未定義的資料。</span><span class="sxs-lookup"><span data-stu-id="23333-137">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23333-138">JET_ColInfoByColid</span><span class="sxs-lookup"><span data-stu-id="23333-138">JET_ColInfoByColid</span></span></p></td>
<td><p><span data-ttu-id="23333-139"><em>pvResult</em> 會被解釋為 <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>，但此 <em>InfoLevel</em> 表示所要求的資料行 (<em>szColumName</em>) 不是字串資料行名稱，而是指向 <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>的指標。</span><span class="sxs-lookup"><span data-stu-id="23333-139"><em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, except this <em>InfoLevel</em> indicates that the requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span> <span data-ttu-id="23333-140">JET_ColInfo 和 JET_ColInfoByColid 都會取得相同的資訊。</span><span class="sxs-lookup"><span data-stu-id="23333-140">JET_ColInfo and JET_ColInfoByColid both retrieve the same information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23333-141">JET_ColInfoList</span><span class="sxs-lookup"><span data-stu-id="23333-141">JET_ColInfoList</span></span></p></td>
<td><p><span data-ttu-id="23333-142"><em>pvResult</em> 會被視為 <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> 結構。</span><span class="sxs-lookup"><span data-stu-id="23333-142"><em>pvResult</em> is interpreted as a <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="23333-143">如果此函式成功，則會以適當的值填入結構。</span><span class="sxs-lookup"><span data-stu-id="23333-143">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="23333-144">臨時表會開啟，並由<a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>的<em>tableid</em>成員識別。</span><span class="sxs-lookup"><span data-stu-id="23333-144">A temporary table is opened and is identified by the <em>tableid</em> member of <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>.</span></span> <span data-ttu-id="23333-145">資料表必須以 <a href="gg294087(v=exchg.10).md">JetCloseTable</a>關閉。</span><span class="sxs-lookup"><span data-stu-id="23333-145">The table must be closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span> <span data-ttu-id="23333-146">如果此函式失敗，結構會包含未定義的資料。</span><span class="sxs-lookup"><span data-stu-id="23333-146">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23333-147">JET_ColInfoListCompact</span><span class="sxs-lookup"><span data-stu-id="23333-147">JET_ColInfoListCompact</span></span></p></td>
<td><p><span data-ttu-id="23333-148"><em>pvResult</em> 會被視為 <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> 結構。</span><span class="sxs-lookup"><span data-stu-id="23333-148"><em>pvResult</em> is interpreted as a <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="23333-149">如果此函式成功，則會以適當的值填入結構。</span><span class="sxs-lookup"><span data-stu-id="23333-149">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="23333-150">臨時表會開啟，並由<a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>的<em>tableid</em>成員識別。</span><span class="sxs-lookup"><span data-stu-id="23333-150">A temporary table is opened and is identified by the <em>tableid</em> member of <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>.</span></span> <span data-ttu-id="23333-151">資料表必須以 <a href="gg294087(v=exchg.10).md">JetCloseTable</a>關閉。</span><span class="sxs-lookup"><span data-stu-id="23333-151">The table must be closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span> <span data-ttu-id="23333-152">如果此函式失敗，結構會包含未定義的資料。</span><span class="sxs-lookup"><span data-stu-id="23333-152">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23333-153">JET_ColInfoListSortColumnid</span><span class="sxs-lookup"><span data-stu-id="23333-153">JET_ColInfoListSortColumnid</span></span></p></td>
<td><p><span data-ttu-id="23333-154">相同于 JET_ColInfoList，但產生的資料表會依 <em>columnid</em>排序，而不是資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="23333-154">Same as JET_ColInfoList, however the resulting table is sorted by <em>columnid</em>, instead of column name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23333-155">JET_ColInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="23333-155">JET_ColInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="23333-156">JET_ColInfoSysTabCursor 已被取代，而且使用它將會傳回 JET_errFeatureNotAvailable。</span><span class="sxs-lookup"><span data-stu-id="23333-156">JET_ColInfoSysTabCursor is deprecated, and use of it will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23333-157">JET_ColInfoBaseByColId</span><span class="sxs-lookup"><span data-stu-id="23333-157">JET_ColInfoBaseByColId</span></span></p></td>
<td><p><span data-ttu-id="23333-158">如同 JET_ColInfoBase， <em>pvResult</em> 會被視為 <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>，但此 <em>InfoLevel</em> 表示要求的資料行 (<em>szColumName</em>) 不是字串資料行名稱，而是指向 <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>的指標。</span><span class="sxs-lookup"><span data-stu-id="23333-158">Same as JET_ColInfoBase, <em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, except this <em>InfoLevel</em> indicates that requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span></p>
<p><span data-ttu-id="23333-159"><strong>Windows Vista：  </strong>這可在 Windows Vista 和更新版本中使用。</span><span class="sxs-lookup"><span data-stu-id="23333-159"><strong>Windows Vista:  </strong>This is available in Windows Vista and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23333-160">JET_ColInfoGrbitNonDerivedColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="23333-160">JET_ColInfoGrbitNonDerivedColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="23333-161">只有當資料表衍生自範本) 時，才會傳回非衍生的資料行 (。</span><span class="sxs-lookup"><span data-stu-id="23333-161">Only return non-derived columns (if the table is derived from a template).</span></span></p>
<p><span data-ttu-id="23333-162">當基底<em>InfoLevel</em> JET_ColInfoList 時，此值可以邏輯或進入<em>InfoLevel</em>。</span><span class="sxs-lookup"><span data-stu-id="23333-162">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="23333-163"><strong>Windows Vista：  </strong>此值是在 Windows Vista 中引進。</span><span class="sxs-lookup"><span data-stu-id="23333-163"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23333-164">JET_ColInfoGrbitMinimalInfo</span><span class="sxs-lookup"><span data-stu-id="23333-164">JET_ColInfoGrbitMinimalInfo</span></span></p></td>
<td><p><span data-ttu-id="23333-165">只傳回資料行名稱和每個資料行的 columnid。</span><span class="sxs-lookup"><span data-stu-id="23333-165">Only return the column name and columnid of each column.</span></span></p>
<p><span data-ttu-id="23333-166">當基底<em>InfoLevel</em> JET_ColInfoList 時，此值可以邏輯或進入<em>InfoLevel</em>。</span><span class="sxs-lookup"><span data-stu-id="23333-166">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="23333-167"><strong>Windows Vista：  </strong>此值是在 Windows Vista 中引進。</span><span class="sxs-lookup"><span data-stu-id="23333-167"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23333-168">JET_ColInfoGrbitSortByColumnid</span><span class="sxs-lookup"><span data-stu-id="23333-168">JET_ColInfoGrbitSortByColumnid</span></span></p></td>
<td><p><span data-ttu-id="23333-169">依 columnid 排序傳回的資料行清單 (預設為依資料行名稱排序清單) 。</span><span class="sxs-lookup"><span data-stu-id="23333-169">Sort returned column list by columnid (default is to sort list by column name).</span></span></p>
<p><span data-ttu-id="23333-170">當基底<em>InfoLevel</em> JET_ColInfoList 時，此值可以邏輯或進入<em>InfoLevel</em>。</span><span class="sxs-lookup"><span data-stu-id="23333-170">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="23333-171"><strong>Windows Vista：  </strong>此值是在 Windows Vista 中引進。</span><span class="sxs-lookup"><span data-stu-id="23333-171"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="23333-172">傳回值</span><span class="sxs-lookup"><span data-stu-id="23333-172">Return Value</span></span>

<span data-ttu-id="23333-173">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="23333-173">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="23333-174">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="23333-174">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="23333-175">傳回碼</span><span class="sxs-lookup"><span data-stu-id="23333-175">Return code</span></span></p></th>
<th><p><span data-ttu-id="23333-176">Description</span><span class="sxs-lookup"><span data-stu-id="23333-176">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23333-177">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="23333-177">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="23333-178">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="23333-178">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23333-179">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="23333-179">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="23333-180">在資料表中找不到名為 <em>szColumnName</em> 的資料行。</span><span class="sxs-lookup"><span data-stu-id="23333-180">The column named <em>szColumnName</em> was not found in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23333-181">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="23333-181">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="23333-182">指定了不正確的 <em>InfoLevel</em> 。</span><span class="sxs-lookup"><span data-stu-id="23333-182">A bad <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23333-183">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="23333-183">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="23333-184">下列情況可能會傳回此錯誤：</span><span class="sxs-lookup"><span data-stu-id="23333-184">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="23333-185">指定了 <em>szTableName</em> 的錯誤名稱。</span><span class="sxs-lookup"><span data-stu-id="23333-185">A bad name for <em>szTableName</em> was given.</span></span></p></li>
<li><p><span data-ttu-id="23333-186">指定了 <em>szColumnName</em> 的錯誤名稱。</span><span class="sxs-lookup"><span data-stu-id="23333-186">A bad name for <em>szColumnName</em> was given.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23333-187">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="23333-187">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="23333-188">下列情況可能會傳回此錯誤：</span><span class="sxs-lookup"><span data-stu-id="23333-188">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="23333-189">指定了不正確的 <em>InfoLevel</em> 。</span><span class="sxs-lookup"><span data-stu-id="23333-189">A bad <em>InfoLevel</em> was specified.</span></span></p></li>
<li><p><span data-ttu-id="23333-190">傳入的是 Null <em>szTableName</em> 。</span><span class="sxs-lookup"><span data-stu-id="23333-190">A NULL <em>szTableName</em> was passed in.</span></span></p></li>
<li><p><span data-ttu-id="23333-191">緩衝區太小。</span><span class="sxs-lookup"><span data-stu-id="23333-191">The buffer is too small.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="23333-192">備註</span><span class="sxs-lookup"><span data-stu-id="23333-192">Remarks</span></span>

<span data-ttu-id="23333-193">**JetGetTableColumnInfo** 和 [JetGetColumnInfo](./jetgetcolumninfo-function.md) 都能取出資料行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="23333-193">**JetGetTableColumnInfo** and [JetGetColumnInfo](./jetgetcolumninfo-function.md) both retrieve information about a column.</span></span> <span data-ttu-id="23333-194">它們之間的差異在於如何識別資料表：</span><span class="sxs-lookup"><span data-stu-id="23333-194">The difference between them is how the table is identified:</span></span>

  - <span data-ttu-id="23333-195">**JetGetTableColumnInfo** 會依 *tableid* 識別資料表。</span><span class="sxs-lookup"><span data-stu-id="23333-195">**JetGetTableColumnInfo** identifies a table by *tableid*.</span></span>

  - <span data-ttu-id="23333-196">[JetGetColumnInfo](./jetgetcolumninfo-function.md) 會依 *dbid* 和 *szTableName* 組合來識別資料表。</span><span class="sxs-lookup"><span data-stu-id="23333-196">[JetGetColumnInfo](./jetgetcolumninfo-function.md) identifies a table by *dbid* and *szTableName* combination.</span></span>

<span data-ttu-id="23333-197">使用 JET_ColInfoList、JET_ColInfoListSortColumnid 或 JET_ColInfoListCompact 來抓取資料時，將會開啟臨時表。</span><span class="sxs-lookup"><span data-stu-id="23333-197">When retrieving data with JET_ColInfoList, JET_ColInfoListSortColumnid, or JET_ColInfoListCompact, a temporary table will be opened.</span></span> <span data-ttu-id="23333-198">臨時表包含資料，而 [JET_COLUMNLIST](./jet-columnlist-structure.md) 結構包含足夠的資訊來跨越臨時表。</span><span class="sxs-lookup"><span data-stu-id="23333-198">The temporary table contains data, and the [JET_COLUMNLIST](./jet-columnlist-structure.md) structure contains sufficient information to traverse the temporary table.</span></span> <span data-ttu-id="23333-199">臨時表必須以 [JetCloseTable](./jetclosetable-function.md)關閉。</span><span class="sxs-lookup"><span data-stu-id="23333-199">The temporary table must be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="23333-200">規格需求</span><span class="sxs-lookup"><span data-stu-id="23333-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23333-201"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="23333-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="23333-202">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="23333-202">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23333-203"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="23333-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="23333-204">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="23333-204">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23333-205"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="23333-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="23333-206">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="23333-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23333-207"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="23333-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="23333-208">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="23333-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23333-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="23333-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="23333-210">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="23333-210">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23333-211"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="23333-211"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="23333-212">實作為 <strong>JetGetTableColumnInfoW</strong> (Unicode) 和 <strong>JetGetTableColumnInfoA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="23333-212">Implemented as <strong>JetGetTableColumnInfoW</strong> (Unicode) and <strong>JetGetTableColumnInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="23333-213">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23333-213">See Also</span></span>

[<span data-ttu-id="23333-214">可擴充儲存引擎錯誤</span><span class="sxs-lookup"><span data-stu-id="23333-214">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="23333-215">錯誤處理參數</span><span class="sxs-lookup"><span data-stu-id="23333-215">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="23333-216">JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="23333-216">JET_COLUMNBASE</span></span>](./jet-columnbase-structure.md)  
[<span data-ttu-id="23333-217">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="23333-217">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="23333-218">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="23333-218">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="23333-219">JET_COLUMNLIST</span><span class="sxs-lookup"><span data-stu-id="23333-219">JET_COLUMNLIST</span></span>](./jet-columnlist-structure.md)  
[<span data-ttu-id="23333-220">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="23333-220">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="23333-221">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="23333-221">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="23333-222">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="23333-222">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="23333-223">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="23333-223">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="23333-224">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="23333-224">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="23333-225">JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="23333-225">JetGetColumnInfo</span></span>](./jetgetcolumninfo-function.md)  
[<span data-ttu-id="23333-226">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="23333-226">JetGetTableColumnInfo</span></span>]()
