---
description: 深入瞭解： JetGetTableInfo 函數
title: JetGetTableInfo 函式
TOCTitle: JetGetTableInfo Function
ms:assetid: 0602186c-b5c3-44b5-87df-482680442afd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269177(v=EXCHG.10)
ms:contentKeyID: 32765480
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableInfoW
- JetGetTableInfo
- JetGetTableInfoA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3362b5da8c6a79d78782e37920b9761b9888b15f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945176"
---
# <a name="jetgettableinfo-function"></a><span data-ttu-id="fdc62-103">JetGetTableInfo 函式</span><span class="sxs-lookup"><span data-stu-id="fdc62-103">JetGetTableInfo Function</span></span>


<span data-ttu-id="fdc62-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="fdc62-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettableinfo-function"></a><span data-ttu-id="fdc62-105">JetGetTableInfo 函式</span><span class="sxs-lookup"><span data-stu-id="fdc62-105">JetGetTableInfo Function</span></span>

<span data-ttu-id="fdc62-106">**JetGetTableInfo** 函數會抓取資料庫中資料表的各種相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fdc62-106">The **JetGetTableInfo** function retrieves various pieces of information about a table in a database.</span></span>

```cpp
    JET_ERR JET_API JetGetTableInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="fdc62-107">參數</span><span class="sxs-lookup"><span data-stu-id="fdc62-107">Parameters</span></span>

<span data-ttu-id="fdc62-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="fdc62-108">*sesid*</span></span>

<span data-ttu-id="fdc62-109">要用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="fdc62-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="fdc62-110">*tableid*</span><span class="sxs-lookup"><span data-stu-id="fdc62-110">*tableid*</span></span>

<span data-ttu-id="fdc62-111">適用資訊的資料表。</span><span class="sxs-lookup"><span data-stu-id="fdc62-111">The table that the information applies to.</span></span>

<span data-ttu-id="fdc62-112">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="fdc62-112">*pvResult*</span></span>

<span data-ttu-id="fdc62-113">將接收資訊的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="fdc62-113">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="fdc62-114">緩衝區的類型取決於 *InfoLevel*。</span><span class="sxs-lookup"><span data-stu-id="fdc62-114">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="fdc62-115">呼叫端必須負責適當地對齊緩衝區。</span><span class="sxs-lookup"><span data-stu-id="fdc62-115">It is the responsibility of the caller to align the buffer appropriately.</span></span>

<span data-ttu-id="fdc62-116">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="fdc62-116">*cbMax*</span></span>

<span data-ttu-id="fdc62-117">在 *pvResult* 中傳遞的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="fdc62-117">The size, in bytes, of the buffer that was passed in *pvResult*.</span></span>

<span data-ttu-id="fdc62-118">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="fdc62-118">*InfoLevel*</span></span>

<span data-ttu-id="fdc62-119">針對 *tableid* 所指定之資料表將抓取的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="fdc62-119">The type of information that will be retrieved for the table that is specified by *tableid*.</span></span> <span data-ttu-id="fdc62-120">儲存在 *pvResult* 中的資料格式取決於 *InfoLevel*。</span><span class="sxs-lookup"><span data-stu-id="fdc62-120">The format of the data that is stored in *pvResult* is dependent on *InfoLevel*.</span></span>

<span data-ttu-id="fdc62-121">您可以為此參數設定下列選項：</span><span class="sxs-lookup"><span data-stu-id="fdc62-121">The following options can be set for this parameter:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fdc62-122">值</span><span class="sxs-lookup"><span data-stu-id="fdc62-122">Value</span></span></p></th>
<th><p><span data-ttu-id="fdc62-123">意義</span><span class="sxs-lookup"><span data-stu-id="fdc62-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fdc62-124">JET_TblInfo</span><span class="sxs-lookup"><span data-stu-id="fdc62-124">JET_TblInfo</span></span></p></td>
<td><p><span data-ttu-id="fdc62-125"><em>pvResult</em> 會被視為 <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> 結構。</span><span class="sxs-lookup"><span data-stu-id="fdc62-125"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure.</span></span> <span data-ttu-id="fdc62-126">如果方法成功，則會以適當的資料填入 <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> 結構。</span><span class="sxs-lookup"><span data-stu-id="fdc62-126">If the method succeeds, the <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure is filled in with the appropriate data.</span></span> <span data-ttu-id="fdc62-127">如果失敗，則內容為未定義。</span><span class="sxs-lookup"><span data-stu-id="fdc62-127">If it fails, the contents are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdc62-128">JET_TblInfoDbid</span><span class="sxs-lookup"><span data-stu-id="fdc62-128">JET_TblInfoDbid</span></span></p></td>
<td><p><span data-ttu-id="fdc62-129"><em>pvResult</em> 會被視為兩個 <a href="gg269248(v=exchg.10).md">JET_DBID</a> 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="fdc62-129"><em>pvResult</em> is treated as an array of two <a href="gg269248(v=exchg.10).md">JET_DBID</a> objects.</span></span> <span data-ttu-id="fdc62-130">擁有資料表之資料庫的資料庫識別碼會儲存在這個陣列中兩次。</span><span class="sxs-lookup"><span data-stu-id="fdc62-130">The database identifier of the database that owns the table is stored in this array twice.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fdc62-131">JET_TblInfoDumpTable</span><span class="sxs-lookup"><span data-stu-id="fdc62-131">JET_TblInfoDumpTable</span></span></p></td>
<td><p><span data-ttu-id="fdc62-132">JET_TblInfoDumpTable 已被取代。</span><span class="sxs-lookup"><span data-stu-id="fdc62-132">JET_TblInfoDumpTable is deprecated.</span></span> <span data-ttu-id="fdc62-133">API 會傳回 JET_errFeatureNotAvailable。</span><span class="sxs-lookup"><span data-stu-id="fdc62-133">The API will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdc62-134">JET_TblInfoName</span><span class="sxs-lookup"><span data-stu-id="fdc62-134">JET_TblInfoName</span></span></p></td>
<td><p><span data-ttu-id="fdc62-135">JET_TblInfoName 會抓取資料表的名稱，並將其儲存在 <em>pvResult</em>中。</span><span class="sxs-lookup"><span data-stu-id="fdc62-135">JET_TblInfoName retrieves the name of the table and stores it in <em>pvResult</em>.</span></span> <span data-ttu-id="fdc62-136">如果緩衝區太小，則行為是未定義的。</span><span class="sxs-lookup"><span data-stu-id="fdc62-136">If the buffer is too small, the behavior is undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fdc62-137">JET_TblInfoMostMany</span><span class="sxs-lookup"><span data-stu-id="fdc62-137">JET_TblInfoMostMany</span></span></p></td>
<td><p><span data-ttu-id="fdc62-138">JET_TblInfoMostMany 會抓取資料表的名稱，並將其儲存在 <em>pvResult</em>中。</span><span class="sxs-lookup"><span data-stu-id="fdc62-138">JET_TblInfoMostMany retrieves the name of the table and stores it in <em>pvResult</em>.</span></span> <span data-ttu-id="fdc62-139">如果緩衝區太小，則行為是未定義的。</span><span class="sxs-lookup"><span data-stu-id="fdc62-139">If the buffer is too small, the behavior is undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdc62-140">JET_TblInfoOLC</span><span class="sxs-lookup"><span data-stu-id="fdc62-140">JET_TblInfoOLC</span></span></p></td>
<td><p><span data-ttu-id="fdc62-141">JET_TblInfoOLC 已被取代。</span><span class="sxs-lookup"><span data-stu-id="fdc62-141">JET_TblInfoOLC is deprecated.</span></span> <span data-ttu-id="fdc62-142">API 會傳回 JET_errFeatureNotAvailable。</span><span class="sxs-lookup"><span data-stu-id="fdc62-142">The API will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fdc62-143">JET_TblInfoRvt</span><span class="sxs-lookup"><span data-stu-id="fdc62-143">JET_TblInfoRvt</span></span></p></td>
<td><p><span data-ttu-id="fdc62-144">JET_TblInfoRvt 已被取代。</span><span class="sxs-lookup"><span data-stu-id="fdc62-144">JET_TblInfoRvt is deprecated.</span></span> <span data-ttu-id="fdc62-145">API 會傳回 JET_errQueryNotSupported。</span><span class="sxs-lookup"><span data-stu-id="fdc62-145">The API will return JET_errQueryNotSupported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdc62-146">JET_TblInfoResetOLC</span><span class="sxs-lookup"><span data-stu-id="fdc62-146">JET_TblInfoResetOLC</span></span></p></td>
<td><p><span data-ttu-id="fdc62-147">JET_TblInfoResetOLC 已被取代。</span><span class="sxs-lookup"><span data-stu-id="fdc62-147">JET_TblInfoResetOLC is deprecated.</span></span> <span data-ttu-id="fdc62-148">API 會傳回 JET_errFeatureNotAvailable。</span><span class="sxs-lookup"><span data-stu-id="fdc62-148">The API will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fdc62-149">JET_TblInfoSpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="fdc62-149">JET_TblInfoSpaceAlloc</span></span></p></td>
<td><p><span data-ttu-id="fdc62-150"><em>pvResult</em> 會被視為兩個 ulong 的陣列：</span><span class="sxs-lookup"><span data-stu-id="fdc62-150"><em>pvResult</em> is interpreted as an array of two ULONGs:</span></span></p>
<ul>
<li><p><span data-ttu-id="fdc62-151">第一個 <strong>ULONG</strong> 是資料表中的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="fdc62-151">The first <strong>ULONG</strong> is the number of pages in the table.</span></span></p></li>
<li><p><span data-ttu-id="fdc62-152">第二個 <strong>ULONG</strong> 是資料表頁面的目標密度。</span><span class="sxs-lookup"><span data-stu-id="fdc62-152">The second <strong>ULONG</strong> is the target density of pages for the table.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdc62-153">JET_TblInfoSpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="fdc62-153">JET_TblInfoSpaceAvailable</span></span></p></td>
<td><p><span data-ttu-id="fdc62-154"><em>pvResult</em> 會被解釋為 <strong>ULONG</strong>。</span><span class="sxs-lookup"><span data-stu-id="fdc62-154"><em>pvResult</em> is interpreted as a <strong>ULONG</strong>.</span></span> <span data-ttu-id="fdc62-155"><strong>ULONG</strong>是資料表中可用的頁數、其索引和 long 值樹狀目錄的總和。</span><span class="sxs-lookup"><span data-stu-id="fdc62-155">The <strong>ULONG</strong> is the sum of the number of pages that are available in the table, its indexes, and the long value tree.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fdc62-156">JET_TblInfoSpaceOwned</span><span class="sxs-lookup"><span data-stu-id="fdc62-156">JET_TblInfoSpaceOwned</span></span></p></td>
<td><p><span data-ttu-id="fdc62-157"><em>pvResult</em> 會被解釋為 <strong>ULONG</strong>。</span><span class="sxs-lookup"><span data-stu-id="fdc62-157"><em>pvResult</em> is interpreted as a <strong>ULONG</strong>.</span></span> <span data-ttu-id="fdc62-158"><strong>ULONG</strong>是資料表所擁有的頁面數目總和 (包括其索引，以及) 的完整值樹狀目錄和任何可用頁面。</span><span class="sxs-lookup"><span data-stu-id="fdc62-158">The <strong>ULONG</strong> is the sum of the number of pages that are owned by the table (including its indexes, and the long value tree and any available pages therein).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdc62-159">JET_TblInfoSpaceUsage</span><span class="sxs-lookup"><span data-stu-id="fdc62-159">JET_TblInfoSpaceUsage</span></span></p></td>
<td><p><span data-ttu-id="fdc62-160">API 的行為取決於傳遞給 API 的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="fdc62-160">The behavior of the API depends on how large the buffer that is passed to the API is.</span></span> <span data-ttu-id="fdc62-161">兩個 <em>cbMax</em> 值至少必須是 ( 2 \* SIZEOF ( ULONG ) ) 。</span><span class="sxs-lookup"><span data-stu-id="fdc62-161">Two <em>cbMax</em> values must be at least ( 2 \* sizeof( ULONG ) ).</span></span></p>
<ul>
<li><p><span data-ttu-id="fdc62-162">如果 <em>cbMax</em> 是 ( 2 \* SIZEOF ( ULONG ) ) ，則會將 <em>pvResult</em> 解釋為兩個 ulong 的陣列：</span><span class="sxs-lookup"><span data-stu-id="fdc62-162">If <em>cbMax</em> is ( 2 \* sizeof( ULONG ) ), <em>pvResult</em> is interpreted as an array of two ULONGs:</span></span></p>
<ul>
<li><p><span data-ttu-id="fdc62-163">第一個 <strong>ULONG</strong> 是資料表的擁有範圍數目。</span><span class="sxs-lookup"><span data-stu-id="fdc62-163">The first <strong>ULONG</strong> is the number of Owned Extents of the table.</span></span></p></li>
<li><p><span data-ttu-id="fdc62-164">第二個 <strong>ULONG</strong> 是資料表的可用範圍數目。</span><span class="sxs-lookup"><span data-stu-id="fdc62-164">The second <strong>ULONG</strong> is the number of Available Extents of the table.</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="fdc62-165"><em>pvResult</em> 會被解釋為的陣列：</span><span class="sxs-lookup"><span data-stu-id="fdc62-165"><em>pvResult</em> is interpreted as an array of:</span></span></p>
<ul>
<li><p><span data-ttu-id="fdc62-166">第一個 <strong>ULONG</strong> 是資料表的擁有範圍數目。</span><span class="sxs-lookup"><span data-stu-id="fdc62-166">The first <strong>ULONG</strong> is the number of Owned Extents of the table.</span></span></p></li>
<li><p><span data-ttu-id="fdc62-167">第二個 <strong>ULONG</strong> 是資料表的可用範圍數目。</span><span class="sxs-lookup"><span data-stu-id="fdc62-167">The second <strong>ULONG</strong> is the number of Available Extents of the table.</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fdc62-168">JET_TblInfoTemplateTableName</span><span class="sxs-lookup"><span data-stu-id="fdc62-168">JET_TblInfoTemplateTableName</span></span></p></td>
<td><p><span data-ttu-id="fdc62-169"><em>pvResult</em> 會被視為字串緩衝區。</span><span class="sxs-lookup"><span data-stu-id="fdc62-169"><em>pvResult</em> is interpreted as a string buffer.</span></span> <span data-ttu-id="fdc62-170">緩衝區至少必須是 JET_cbNameMost + 1，包括終止的 <strong>Null</strong>。</span><span class="sxs-lookup"><span data-stu-id="fdc62-170">The buffer must be at least JET_cbNameMost + 1, including the terminating <strong>NULL</strong>.</span></span> <span data-ttu-id="fdc62-171">如果資料表是衍生的資料表，則會使用衍生資料表繼承其 DDL 的資料表名稱填入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="fdc62-171">If the table is a derived table, the buffer will be filled in with the name of the table from which the derived table inherited its DDL.</span></span> <span data-ttu-id="fdc62-172">如果資料表不是衍生的資料表，則緩衝區將會是空字串。</span><span class="sxs-lookup"><span data-stu-id="fdc62-172">If the table is not a derived table, the buffer will an empty string.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="fdc62-173">傳回值</span><span class="sxs-lookup"><span data-stu-id="fdc62-173">Return Value</span></span>

<span data-ttu-id="fdc62-174">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="fdc62-174">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="fdc62-175">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="fdc62-175">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fdc62-176">傳回碼</span><span class="sxs-lookup"><span data-stu-id="fdc62-176">Return code</span></span></p></th>
<th><p><span data-ttu-id="fdc62-177">Description</span><span class="sxs-lookup"><span data-stu-id="fdc62-177">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fdc62-178">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="fdc62-178">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="fdc62-179">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="fdc62-179">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdc62-180">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="fdc62-180">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="fdc62-181">緩衝區太小。</span><span class="sxs-lookup"><span data-stu-id="fdc62-181">The buffer was too small.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fdc62-182">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="fdc62-182">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="fdc62-183">指定了已被取代的 <em>InfoLevel</em> 。</span><span class="sxs-lookup"><span data-stu-id="fdc62-183">A deprecated <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdc62-184">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="fdc62-184">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="fdc62-185">緩衝區的大小不正確。</span><span class="sxs-lookup"><span data-stu-id="fdc62-185">The buffer was not the right size.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fdc62-186">JET_errInvalidOperation</span><span class="sxs-lookup"><span data-stu-id="fdc62-186">JET_errInvalidOperation</span></span></p></td>
<td><p><span data-ttu-id="fdc62-187">傳入的資料表是臨時表，而且無法針對臨時表抓取要求的 <em>InfoLevel</em> 。</span><span class="sxs-lookup"><span data-stu-id="fdc62-187">The table that was passed in was a temporary table, and the requested <em>InfoLevel</em> cannot be retrieved for a temporary table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdc62-188">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="fdc62-188">JET_errObjectNotFound</span></span></p></td>
<td><p><span data-ttu-id="fdc62-189">傳入的資料表是臨時表，而且無法針對臨時表抓取要求的 <em>InfoLevel</em> 。</span><span class="sxs-lookup"><span data-stu-id="fdc62-189">The table that was passed in was a temporary table, and the requested <em>InfoLevel</em> cannot be retrieved for a temporary table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fdc62-190">JET_errQueryNotSupported</span><span class="sxs-lookup"><span data-stu-id="fdc62-190">JET_errQueryNotSupported</span></span></p></td>
<td><p><span data-ttu-id="fdc62-191">不支援 <em>InfoLevel</em> 。</span><span class="sxs-lookup"><span data-stu-id="fdc62-191">The <em>InfoLevel</em> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdc62-192">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="fdc62-192">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="fdc62-193">資料表正由另一個資料庫作業使用中。</span><span class="sxs-lookup"><span data-stu-id="fdc62-193">The table is being used by another database operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fdc62-194">JET_errTableLocked</span><span class="sxs-lookup"><span data-stu-id="fdc62-194">JET_errTableLocked</span></span></p></td>
<td><p><span data-ttu-id="fdc62-195">資料表已由另一個資料庫操作鎖定。</span><span class="sxs-lookup"><span data-stu-id="fdc62-195">The table is locked by another database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdc62-196">JET_wrnTableInUseBySystem</span><span class="sxs-lookup"><span data-stu-id="fdc62-196">JET_wrnTableInUseBySystem</span></span></p></td>
<td><p><span data-ttu-id="fdc62-197">系統正在使用資料表。</span><span class="sxs-lookup"><span data-stu-id="fdc62-197">The table is being used by the system.</span></span> <span data-ttu-id="fdc62-198">這個警告不是嚴重的。</span><span class="sxs-lookup"><span data-stu-id="fdc62-198">This warning is nonfatal.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="fdc62-199">備註</span><span class="sxs-lookup"><span data-stu-id="fdc62-199">Remarks</span></span>

<span data-ttu-id="fdc62-200">某些資訊片段對臨時表而言是不正確 (請參閱 [JetOpenTempTable](./jetopentemptable-function.md)) 。</span><span class="sxs-lookup"><span data-stu-id="fdc62-200">Some pieces of information are not valid for temporary tables (See [JetOpenTempTable](./jetopentemptable-function.md)).</span></span>

<span data-ttu-id="fdc62-201">資料表統計資料包括記錄的數目以及叢集索引中的頁面數目 (也就是包含記錄資料) 的索引。</span><span class="sxs-lookup"><span data-stu-id="fdc62-201">The table statistics include the number of records and the number of pages in the clustered index (that is, the index containing the record data).</span></span> <span data-ttu-id="fdc62-202">索引統計資料是使用 [JetGetIndexInfo](./jetgetindexinfo-function.md) 或 [JetGetTableIndexInfo](./jetgettableindexinfo-function.md)，依名稱個別存取。</span><span class="sxs-lookup"><span data-stu-id="fdc62-202">The index statistics are accessed separately by name, using [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="fdc62-203">規格需求</span><span class="sxs-lookup"><span data-stu-id="fdc62-203">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fdc62-204"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="fdc62-204"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fdc62-205">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="fdc62-205">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdc62-206"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="fdc62-206"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fdc62-207">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="fdc62-207">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fdc62-208"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="fdc62-208"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fdc62-209">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="fdc62-209">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdc62-210"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="fdc62-210"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="fdc62-211">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="fdc62-211">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fdc62-212"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="fdc62-212"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="fdc62-213">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="fdc62-213">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdc62-214"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="fdc62-214"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="fdc62-215">實作為 <strong>JetGetTableInfoW</strong> (Unicode) 和 <strong>JetGetTableInfoA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="fdc62-215">Implemented as <strong>JetGetTableInfoW</strong> (Unicode) and <strong>JetGetTableInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="fdc62-216">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fdc62-216">See Also</span></span>

[<span data-ttu-id="fdc62-217">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="fdc62-217">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="fdc62-218">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="fdc62-218">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="fdc62-219">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="fdc62-219">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="fdc62-220">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="fdc62-220">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="fdc62-221">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="fdc62-221">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="fdc62-222">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="fdc62-222">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="fdc62-223">JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="fdc62-223">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)  
[<span data-ttu-id="fdc62-224">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="fdc62-224">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="fdc62-225">JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="fdc62-225">JetOpenTempTable</span></span>](./jetopentemptable-function.md)
