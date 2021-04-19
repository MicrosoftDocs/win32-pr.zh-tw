---
description: 深入瞭解： JetGetColumnInfo 函數
title: JetGetColumnInfo 函式
TOCTitle: JetGetColumnInfo Function
ms:assetid: 2db024e9-2784-4fb2-84b2-fef7ae518938
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269215(v=EXCHG.10)
ms:contentKeyID: 32765518
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetColumnInfoA
- JetGetColumnInfoW
- JetGetColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d96d5860f4b10f9294ab210e4e41d78cede202f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985248"
---
# <a name="jetgetcolumninfo-function"></a><span data-ttu-id="fb0b1-103">JetGetColumnInfo 函式</span><span class="sxs-lookup"><span data-stu-id="fb0b1-103">JetGetColumnInfo Function</span></span>


<span data-ttu-id="fb0b1-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="fb0b1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetcolumninfo-function"></a><span data-ttu-id="fb0b1-105">JetGetColumnInfo 函式</span><span class="sxs-lookup"><span data-stu-id="fb0b1-105">JetGetColumnInfo Function</span></span>

<span data-ttu-id="fb0b1-106">**JetGetColumnInfo** 函數會抓取資料行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-106">The **JetGetColumnInfo** function retrieves information about a column.</span></span>

```cpp
    JET_ERR JET_API JetGetColumnInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szColumnName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="fb0b1-107">參數</span><span class="sxs-lookup"><span data-stu-id="fb0b1-107">Parameters</span></span>

<span data-ttu-id="fb0b1-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="fb0b1-108">*sesid*</span></span>

<span data-ttu-id="fb0b1-109">要用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="fb0b1-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="fb0b1-110">*dbid*</span></span>

<span data-ttu-id="fb0b1-111">識別包含從中抓取資訊之資料行的資料表，以及 *szTableName*。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-111">Identifies, along with *szTableName*, the table that contains the column from which the information is retrieved.</span></span>

<span data-ttu-id="fb0b1-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="fb0b1-112">*szTableName*</span></span>

<span data-ttu-id="fb0b1-113">識別包含從中抓取資訊之資料行的資料表，以及 *dbid*。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-113">Identifies, along with *dbid*, the table that contains the column from which the information is retrieved.</span></span>

<span data-ttu-id="fb0b1-114">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="fb0b1-114">*szColumnName*</span></span>

<span data-ttu-id="fb0b1-115">提取資訊所針對的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-115">The name of the column that information is fetched for.</span></span>

<span data-ttu-id="fb0b1-116">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="fb0b1-116">*pvResult*</span></span>

<span data-ttu-id="fb0b1-117">將接收資訊的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-117">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="fb0b1-118">緩衝區的類型取決於 *InfoLevel*。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-118">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="fb0b1-119">呼叫端必須設定為適當地對齊緩衝區。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-119">The caller must be configured to align the buffer appropriately.</span></span>

<span data-ttu-id="fb0b1-120">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="fb0b1-120">*cbMax*</span></span>

<span data-ttu-id="fb0b1-121">在 *pvResult* 中傳遞的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-121">The size, in bytes, of the buffer that is passed in *pvResult*.</span></span>

<span data-ttu-id="fb0b1-122">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="fb0b1-122">*InfoLevel*</span></span>

<span data-ttu-id="fb0b1-123">要針對 *szColumnName* 所指定的資料行取得的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-123">The type of information to retrieve for the column that is specified by *szColumnName*.</span></span> <span data-ttu-id="fb0b1-124">*PvResult* 中儲存的資料格式取決於此參數。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-124">The format of the data stored in *pvResult* is dependent on this parameter.</span></span> <span data-ttu-id="fb0b1-125">如需臨時表的架構，請參閱 [JET_COLUMNLIST](./jet-columnlist-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-125">For the schema of the temporary table, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

<span data-ttu-id="fb0b1-126">這些 *InfoLevels* 的差異如下：</span><span class="sxs-lookup"><span data-stu-id="fb0b1-126">These *InfoLevels* are differentiated by:</span></span>

  - <span data-ttu-id="fb0b1-127">JET_ColInfoListSortColumnid 會依 *columnid* 排序臨時表。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-127">JET_ColInfoListSortColumnid will sort the temporary table by *columnid*.</span></span>

  - <span data-ttu-id="fb0b1-128">JET_ColInfoListCompact 將壓縮輸出。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-128">JET_ColInfoListCompact will compact the output.</span></span> <span data-ttu-id="fb0b1-129">如需 compact 輸出的詳細資訊，請參閱 [JET_COLUMNLIST](./jet-columnlist-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-129">For more information about the compact output, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

<span data-ttu-id="fb0b1-130">下列選項可用於此參數。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-130">The following options are available for use with this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fb0b1-131">值</span><span class="sxs-lookup"><span data-stu-id="fb0b1-131">Value</span></span></p></th>
<th><p><span data-ttu-id="fb0b1-132">意義</span><span class="sxs-lookup"><span data-stu-id="fb0b1-132">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb0b1-133">JET_ColInfo</span><span class="sxs-lookup"><span data-stu-id="fb0b1-133">JET_ColInfo</span></span></p></td>
<td><p><span data-ttu-id="fb0b1-134">JET_ColInfo 和 JET_ColInfoByColid 都會取得相同的資訊。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-134">JET_ColInfo and JET_ColInfoByColid both retrieve the same information.</span></span> <span data-ttu-id="fb0b1-135"><em>pvResult</em> 會被視為 <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>，而 <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> 結構的欄位會適當地填入。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-135"><em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, and the fields of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure are filled in appropriately.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb0b1-136">JET_ColInfoBase</span><span class="sxs-lookup"><span data-stu-id="fb0b1-136">JET_ColInfoBase</span></span></p></td>
<td><p><span data-ttu-id="fb0b1-137"><em>pvResult</em> 會被視為 <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> 結構。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-137"><em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> structure.</span></span> <span data-ttu-id="fb0b1-138">這類似于 <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> 結構。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-138">This is similar to a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure.</span></span> <span data-ttu-id="fb0b1-139">如果此函式成功，則會以適當的值填入結構。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-139">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="fb0b1-140">如果此函式失敗，結構會包含未定義的資料。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-140">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb0b1-141">JET_ColInfoByColid</span><span class="sxs-lookup"><span data-stu-id="fb0b1-141">JET_ColInfoByColid</span></span></p></td>
<td><p><span data-ttu-id="fb0b1-142">就像 JET_ColInfo 一樣， <em>pvResult</em> 會被視為 <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>，但此 <em>InfoLevel</em> 表示要求的資料行 (<em>szColumName</em>) 不是字串資料行名稱，而是指向 <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>的指標。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-142">Like JET_ColInfo, <em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, except this <em>InfoLevel</em> indicates that the requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb0b1-143">JET_ColInfoList</span><span class="sxs-lookup"><span data-stu-id="fb0b1-143">JET_ColInfoList</span></span></p></td>
<td><p><span data-ttu-id="fb0b1-144"><em>pvResult</em> 會被視為 <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> 結構。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-144"><em>pvResult</em> is interpreted as a <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="fb0b1-145">如果此函式成功，則會以適當的值填入結構。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-145">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="fb0b1-146">臨時表會開啟，並由<a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>結構的<strong>tableid</strong>成員識別。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-146">A temporary table is opened and is identified by the <strong>tableid</strong> member of the <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="fb0b1-147">資料表必須以 <a href="gg294087(v=exchg.10).md">JetCloseTable</a>關閉。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-147">The table must be closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span> <span data-ttu-id="fb0b1-148">如果此函式失敗，結構會包含未定義的資料。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-148">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb0b1-149">JET_ColInfoListCompact</span><span class="sxs-lookup"><span data-stu-id="fb0b1-149">JET_ColInfoListCompact</span></span></p></td>
<td><p><span data-ttu-id="fb0b1-150">與 JET_ColInfoList 相同。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-150">Same as JET_ColInfoList.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb0b1-151">JET_ColInfoListSortColumnid</span><span class="sxs-lookup"><span data-stu-id="fb0b1-151">JET_ColInfoListSortColumnid</span></span></p></td>
<td><p><span data-ttu-id="fb0b1-152">等同于 JET_ColInfoList;不過，產生的資料表會依 columnid 排序，而不是資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-152">Same as JET_ColInfoList; however the resulting table is sorted by columnid, instead of column name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb0b1-153">JET_ColInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="fb0b1-153">JET_ColInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="fb0b1-154">JET_ColInfoSysTabCursor 已被取代，而且使用它將會傳回 JET_errFeatureNotAvailable。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-154">JET_ColInfoSysTabCursor is deprecated, and use of it will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb0b1-155">JET_ColInfoBaseByColId</span><span class="sxs-lookup"><span data-stu-id="fb0b1-155">JET_ColInfoBaseByColId</span></span></p></td>
<td><p><span data-ttu-id="fb0b1-156">就像 JET_ColInfoBase 一樣， <em>pvResult</em> 會被視為 <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>，但此 <em>InfoLevel</em> 表示要求的資料行 (<em>szColumName</em>) 不是字串資料行名稱，而是指向 <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>的指標。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-156">Like JET_ColInfoBase, <em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, except this <em>InfoLevel</em> indicates that requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span></p>
<p><span data-ttu-id="fb0b1-157"><strong>Windows Vista：  </strong>此值是在 Windows Vista 中引進。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-157"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb0b1-158">JET_ColInfoGrbitNonDerivedColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="fb0b1-158">JET_ColInfoGrbitNonDerivedColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="fb0b1-159">只有當資料表衍生自範本) 時，才會傳回非衍生的資料行 (。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-159">Only return non-derived columns (if the table is derived from a template).</span></span></p>
<p><span data-ttu-id="fb0b1-160">當基底<em>InfoLevel</em> JET_ColInfoList 時，此值可以邏輯或進入<em>InfoLevel</em>。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-160">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="fb0b1-161"><strong>Windows Vista：  </strong>這個值是 Windows Vista 引進的。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-161"><strong>Windows Vista:  </strong>This value is introduced Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb0b1-162">JET_ColInfoGrbitMinimalInfo</span><span class="sxs-lookup"><span data-stu-id="fb0b1-162">JET_ColInfoGrbitMinimalInfo</span></span></p></td>
<td><p><span data-ttu-id="fb0b1-163">只傳回資料行名稱和每個資料行的 columnid。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-163">Only return the column name and columnid of each column.</span></span></p>
<p><span data-ttu-id="fb0b1-164">當基底<em>InfoLevel</em> JET_ColInfoList 時，此值可以邏輯或進入<em>InfoLevel</em>。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-164">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="fb0b1-165"><strong>Windows Vista：  </strong>此值是在 Windows Vista 中引進。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-165"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb0b1-166">JET_ColInfoGrbitSortByColumnid</span><span class="sxs-lookup"><span data-stu-id="fb0b1-166">JET_ColInfoGrbitSortByColumnid</span></span></p></td>
<td><p><span data-ttu-id="fb0b1-167">依 columnid 排序傳回的資料行清單 (預設為依資料行名稱排序清單) 。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-167">Sort returned column list by columnid (default is to sort list by column name).</span></span></p>
<p><span data-ttu-id="fb0b1-168">當基底<em>InfoLevel</em> JET_ColInfoList 時，此值可以邏輯或進入<em>InfoLevel</em>。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-168">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="fb0b1-169"><strong>Windows Vista：  </strong>此值是在 Windows Vista 中引進。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-169"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="fb0b1-170">傳回值</span><span class="sxs-lookup"><span data-stu-id="fb0b1-170">Return Value</span></span>

<span data-ttu-id="fb0b1-171">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-171">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="fb0b1-172">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-172">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fb0b1-173">傳回碼</span><span class="sxs-lookup"><span data-stu-id="fb0b1-173">Return code</span></span></p></th>
<th><p><span data-ttu-id="fb0b1-174">Description</span><span class="sxs-lookup"><span data-stu-id="fb0b1-174">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb0b1-175">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="fb0b1-175">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="fb0b1-176">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-176">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb0b1-177">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="fb0b1-177">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="fb0b1-178">在資料表中找不到名為 <em>szColumnName</em> 的資料行。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-178">The column named <em>szColumnName</em> was not found in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb0b1-179">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="fb0b1-179">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="fb0b1-180">指定了不正確的 <em>InfoLevel</em> 。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-180">A bad <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb0b1-181">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="fb0b1-181">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="fb0b1-182">下列情況可能會傳回此錯誤：</span><span class="sxs-lookup"><span data-stu-id="fb0b1-182">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="fb0b1-183">指定了 <em>szTableName</em> 的錯誤名稱。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-183">A bad name for <em>szTableName</em> was given.</span></span></p></li>
<li><p><span data-ttu-id="fb0b1-184">指定了 <em>szColumnName</em> 的錯誤名稱。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-184">A bad name for <em>szColumnName</em> was given.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb0b1-185">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="fb0b1-185">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="fb0b1-186">下列情況可能會傳回此錯誤：</span><span class="sxs-lookup"><span data-stu-id="fb0b1-186">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="fb0b1-187">指定了不正確的 <em>InfoLevel</em> 。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-187">A bad <em>InfoLevel</em> was specified.</span></span></p></li>
<li><p><span data-ttu-id="fb0b1-188">傳入的是 Null <em>szTableName</em> 。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-188">A NULL <em>szTableName</em> was passed in.</span></span></p></li>
<li><p><span data-ttu-id="fb0b1-189">緩衝區太小。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-189">The buffer is too small.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="fb0b1-190">備註</span><span class="sxs-lookup"><span data-stu-id="fb0b1-190">Remarks</span></span>

<span data-ttu-id="fb0b1-191">[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) 和 **JetGetColumnInfo** 都能取出資料行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-191">[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) and **JetGetColumnInfo** both retrieve information about a column.</span></span> <span data-ttu-id="fb0b1-192">它們之間的差異在於如何識別資料表：</span><span class="sxs-lookup"><span data-stu-id="fb0b1-192">The difference between them is how the table is identified:</span></span>

  - <span data-ttu-id="fb0b1-193">[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) 會依 *tableid* 識別資料表。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-193">[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) identifies a table by *tableid*.</span></span>

  - <span data-ttu-id="fb0b1-194">**JetGetColumnInfo** 會依 *dbid* 和 *szTableName* 組合來識別資料表。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-194">**JetGetColumnInfo** identifies a table by *dbid* and *szTableName* combination.</span></span>

<span data-ttu-id="fb0b1-195">使用 JET_ColInfoList、JET_ColInfoListSortColumnid 或 JET_ColInfoListCompact 來抓取資料時，將會開啟臨時表。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-195">When retrieving data with JET_ColInfoList, JET_ColInfoListSortColumnid, or JET_ColInfoListCompact, a temporary table will be opened.</span></span> <span data-ttu-id="fb0b1-196">臨時表包含資料，而 [JET_COLUMNLIST](./jet-columnlist-structure.md) 結構包含足夠的資訊來跨越臨時表。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-196">The temporary table contains data, and the [JET_COLUMNLIST](./jet-columnlist-structure.md) structure contains sufficient information to traverse the temporary table.</span></span> <span data-ttu-id="fb0b1-197">臨時表必須以 [JetCloseTable](./jetclosetable-function.md)關閉。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-197">The temporary table must be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="fb0b1-198">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb0b1-198">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb0b1-199"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="fb0b1-199"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fb0b1-200">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-200">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb0b1-201"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="fb0b1-201"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fb0b1-202">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-202">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb0b1-203"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="fb0b1-203"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fb0b1-204">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-204">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb0b1-205"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="fb0b1-205"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="fb0b1-206">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-206">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb0b1-207"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="fb0b1-207"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="fb0b1-208">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-208">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb0b1-209"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="fb0b1-209"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="fb0b1-210">實作為 <strong>JetGetColumnInfoW</strong> (Unicode) 和 <strong>JetGetColumnInfoA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="fb0b1-210">Implemented as <strong>JetGetColumnInfoW</strong> (Unicode) and <strong>JetGetColumnInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="fb0b1-211">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb0b1-211">See Also</span></span>

[<span data-ttu-id="fb0b1-212">錯誤處理參數</span><span class="sxs-lookup"><span data-stu-id="fb0b1-212">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="fb0b1-213">可擴充儲存引擎錯誤</span><span class="sxs-lookup"><span data-stu-id="fb0b1-213">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="fb0b1-214">JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="fb0b1-214">JET_COLUMNBASE</span></span>](./jet-columnbase-structure.md)  
[<span data-ttu-id="fb0b1-215">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="fb0b1-215">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="fb0b1-216">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="fb0b1-216">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="fb0b1-217">JET_COLUMNLIST</span><span class="sxs-lookup"><span data-stu-id="fb0b1-217">JET_COLUMNLIST</span></span>](./jet-columnlist-structure.md)  
[<span data-ttu-id="fb0b1-218">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="fb0b1-218">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="fb0b1-219">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="fb0b1-219">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="fb0b1-220">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="fb0b1-220">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="fb0b1-221">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="fb0b1-221">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="fb0b1-222">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="fb0b1-222">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="fb0b1-223">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="fb0b1-223">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)
