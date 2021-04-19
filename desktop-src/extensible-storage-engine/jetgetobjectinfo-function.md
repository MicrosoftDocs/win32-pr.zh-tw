---
description: 深入瞭解： JetGetObjectInfo 函數
title: JetGetObjectInfo 函式
TOCTitle: JetGetObjectInfo Function
ms:assetid: 3e069c61-6dab-4b79-8bf2-7844d017598f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269232(v=EXCHG.10)
ms:contentKeyID: 32765534
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetObjectInfo
- JetGetObjectInfoA
- JetGetObjectInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf4c3c9806d4dcf898d6daeb903eb6fc4322fee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980892"
---
# <a name="jetgetobjectinfo-function"></a><span data-ttu-id="ac597-103">JetGetObjectInfo 函式</span><span class="sxs-lookup"><span data-stu-id="ac597-103">JetGetObjectInfo Function</span></span>


<span data-ttu-id="ac597-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ac597-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetobjectinfo-function"></a><span data-ttu-id="ac597-105">JetGetObjectInfo 函式</span><span class="sxs-lookup"><span data-stu-id="ac597-105">JetGetObjectInfo Function</span></span>

<span data-ttu-id="ac597-106">**JetGetObjectInfo** 函式會捕獲資料庫物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ac597-106">The **JetGetObjectInfo** function retrieves information about database objects.</span></span> <span data-ttu-id="ac597-107">目前只支援資料表。</span><span class="sxs-lookup"><span data-stu-id="ac597-107">Currently, only tables are supported.</span></span> <span data-ttu-id="ac597-108">[JetGetTableInfo](./jetgettableinfo-function.md) 可以用來提取比 **JetGetObjectInfo** 更多的資訊。</span><span class="sxs-lookup"><span data-stu-id="ac597-108">[JetGetTableInfo](./jetgettableinfo-function.md) can be used to fetch more information than **JetGetObjectInfo**.</span></span>

```cpp
    JET_ERR JET_API JetGetObjectInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_OBJTYP objtyp,
      __in_opt      const tchar* szContainerName,
      __in_opt      const tchar* szObjectName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="ac597-109">參數</span><span class="sxs-lookup"><span data-stu-id="ac597-109">Parameters</span></span>

<span data-ttu-id="ac597-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="ac597-110">*sesid*</span></span>

<span data-ttu-id="ac597-111">要使用的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="ac597-111">The database session context to use.</span></span>

<span data-ttu-id="ac597-112">*dbid*</span><span class="sxs-lookup"><span data-stu-id="ac597-112">*dbid*</span></span>

<span data-ttu-id="ac597-113">從中抓取資訊的資料庫。</span><span class="sxs-lookup"><span data-stu-id="ac597-113">The database from which the information is retrieved.</span></span>

<span data-ttu-id="ac597-114">*objtyp*</span><span class="sxs-lookup"><span data-stu-id="ac597-114">*objtyp*</span></span>

<span data-ttu-id="ac597-115">物件，包含要取出的資訊。</span><span class="sxs-lookup"><span data-stu-id="ac597-115">The objects that contain information to be retrieved.</span></span> <span data-ttu-id="ac597-116">目前只支援 JET_objtypNil 和 JET_objtypTable，兩者的行為相同。</span><span class="sxs-lookup"><span data-stu-id="ac597-116">Currently, only JET_objtypNil and JET_objtypTable are supported, both of which behave identically.</span></span> <span data-ttu-id="ac597-117">只會取出資料表。</span><span class="sxs-lookup"><span data-stu-id="ac597-117">Only tables will be retrieved.</span></span>

<span data-ttu-id="ac597-118">*szContainerName*</span><span class="sxs-lookup"><span data-stu-id="ac597-118">*szContainerName*</span></span>

<span data-ttu-id="ac597-119">此參數會保留供日後使用，並傳遞 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ac597-119">This parameter is reserved for future use and passes **NULL**.</span></span> <span data-ttu-id="ac597-120">要取得其資訊之物件的類型名稱。</span><span class="sxs-lookup"><span data-stu-id="ac597-120">The name of the types of objects about which to retrieve information.</span></span>

<span data-ttu-id="ac597-121">*szObjectName*</span><span class="sxs-lookup"><span data-stu-id="ac597-121">*szObjectName*</span></span>

<span data-ttu-id="ac597-122">物件的名稱，其中包含要取出的資訊。</span><span class="sxs-lookup"><span data-stu-id="ac597-122">The name of the object that contains information to retrieve.</span></span> <span data-ttu-id="ac597-123">當 *InfoLevel* 使用 JET_ObjInfoList 或 JET_ObjInfoListNoStats 選項來取出所有物件的清單時，此值應該是 **Null** 或空字串。</span><span class="sxs-lookup"><span data-stu-id="ac597-123">When *InfoLevel* uses the JET_ObjInfoList or JET_ObjInfoListNoStats options to retrieve a list of all objects, this value should be **NULL** or an empty string.</span></span>

<span data-ttu-id="ac597-124">目前只支援資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="ac597-124">Only table names are currently supported.</span></span>

<span data-ttu-id="ac597-125">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="ac597-125">*pvResult*</span></span>

<span data-ttu-id="ac597-126">接收指定資訊之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="ac597-126">Pointer to a buffer which receives the specified information.</span></span>

<span data-ttu-id="ac597-127">緩衝區的大小（以位元組為單位）會以 *cbMax* 傳遞。</span><span class="sxs-lookup"><span data-stu-id="ac597-127">The size of the buffer, in bytes, is passed in *cbMax*.</span></span> <span data-ttu-id="ac597-128">失敗時， *pvResult* 的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="ac597-128">On failure the contents of *pvResult* are undefined.</span></span>

<span data-ttu-id="ac597-129">儲存在 *pvResult* 中的資訊取決於 *InfoLevel*。</span><span class="sxs-lookup"><span data-stu-id="ac597-129">The information that is stored in *pvResult* depends on *InfoLevel*.</span></span>

<span data-ttu-id="ac597-130">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="ac597-130">*cbMax*</span></span>

<span data-ttu-id="ac597-131">傳入 *pvResult* 的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ac597-131">The size, in bytes, of the buffer passed in *pvResult*.</span></span>

<span data-ttu-id="ac597-132">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="ac597-132">*InfoLevel*</span></span>

<span data-ttu-id="ac597-133">指定要為指定物件取出的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="ac597-133">Specifies which type of information to retrieve for the specified object.</span></span> <span data-ttu-id="ac597-134">它會影響 *pvResult* 的解讀方式。</span><span class="sxs-lookup"><span data-stu-id="ac597-134">It affects how *pvResult* is interpreted.</span></span>

<span data-ttu-id="ac597-135">您可以針對此參數設定下列選項。</span><span class="sxs-lookup"><span data-stu-id="ac597-135">The following options are available to set for this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ac597-136">值</span><span class="sxs-lookup"><span data-stu-id="ac597-136">Value</span></span></p></th>
<th><p><span data-ttu-id="ac597-137">意義</span><span class="sxs-lookup"><span data-stu-id="ac597-137">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ac597-138">JET_ObjInfo</span><span class="sxs-lookup"><span data-stu-id="ac597-138">JET_ObjInfo</span></span></p></td>
<td><p><span data-ttu-id="ac597-139"><em>pvResult</em> 會被視為 <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> 結構。</span><span class="sxs-lookup"><span data-stu-id="ac597-139"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure.</span></span></p>
<p><span data-ttu-id="ac597-140"><a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>結構會填入<em>szObjectName</em>中所命名物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ac597-140">The <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure is populated with information pertaining to the object that is named in <em>szObjectName</em>.</span></span></p>
<p><span data-ttu-id="ac597-141">如果呼叫者不想知道物件的記錄和頁面數目，請考慮使用 JET_ObjInfoNoStats 資訊層級，因為不包含統計資料，所以可能更快。</span><span class="sxs-lookup"><span data-stu-id="ac597-141">If the caller does not want to know the number of records and pages for the object, consider using JET_ObjInfoNoStats information level, which might be faster since statistics are not included.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac597-142">JET_ObjInfoList</span><span class="sxs-lookup"><span data-stu-id="ac597-142">JET_ObjInfoList</span></span></p></td>
<td><p><span data-ttu-id="ac597-143"><em>pvResult</em> 會被視為 <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> 結構。</span><span class="sxs-lookup"><span data-stu-id="ac597-143"><em>pvResult</em> is interpreted as a <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="ac597-144">會抓取所有物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ac597-144">Information about all objects is retrieved.</span></span> <span data-ttu-id="ac597-145">系統將會建立臨時表，並在 <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> 結構中描述遍歷臨時表所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="ac597-145">A temporary table will be created, and the information that is necessary to traverse the temporary table is described in the <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="ac597-146">如需詳細資訊，請參閱 <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>。</span><span class="sxs-lookup"><span data-stu-id="ac597-146">For more information, see <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>.</span></span> <span data-ttu-id="ac597-147">如果呼叫者不想知道物件的記錄和頁面數目，請考慮使用 JET_ObjInfoListNoStats，這樣可能會更快。</span><span class="sxs-lookup"><span data-stu-id="ac597-147">If the caller does not want to know the number of records and pages for the object, consider using JET_ObjInfoListNoStats, which might be faster.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac597-148">JET_ObjInfoListACM</span><span class="sxs-lookup"><span data-stu-id="ac597-148">JET_ObjInfoListACM</span></span></p></td>
<td><p><span data-ttu-id="ac597-149">已淘汰，目前不支援。</span><span class="sxs-lookup"><span data-stu-id="ac597-149">Deprecated and not currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac597-150">JET_ObjInfoListNoStats</span><span class="sxs-lookup"><span data-stu-id="ac597-150">JET_ObjInfoListNoStats</span></span></p></td>
<td><p><span data-ttu-id="ac597-151"><em>pvResult</em> 會被視為 <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> 結構。</span><span class="sxs-lookup"><span data-stu-id="ac597-151"><em>pvResult</em> is interpreted as a <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="ac597-152">會抓取所有物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ac597-152">Information about all objects is retrieved.</span></span> <span data-ttu-id="ac597-153">系統將會建立臨時表，並在 <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> 結構中描述遍歷臨時表所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="ac597-153">A temporary table will be created, and the information that is necessary to traverse the temporary table is described in the <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="ac597-154">如需詳細資訊，請參閱 <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>。</span><span class="sxs-lookup"><span data-stu-id="ac597-154">For more information, see <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>.</span></span> <span data-ttu-id="ac597-155">JET_ObjInfoListNoStats 與 JET_ObjInfoList 相同，不同之處在于報告記錄數目 (<em>columnidcRecord</em>) 和頁面 (<em>columnidcPage</em>) 的資料行將不會更新。</span><span class="sxs-lookup"><span data-stu-id="ac597-155">JET_ObjInfoListNoStats is identical to JET_ObjInfoList, except that the columns that report the number of records (<em>columnidcRecord</em>) and pages (<em>columnidcPage</em>) will not be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac597-156">JET_ObjInfoMax</span><span class="sxs-lookup"><span data-stu-id="ac597-156">JET_ObjInfoMax</span></span></p></td>
<td><p><span data-ttu-id="ac597-157"><em>pvResult</em> 會被解釋為 <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>。</span><span class="sxs-lookup"><span data-stu-id="ac597-157"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>.</span></span> <span data-ttu-id="ac597-158">物件的大小上限為頁面。</span><span class="sxs-lookup"><span data-stu-id="ac597-158">The maximum size of the object is in pages.</span></span> <span data-ttu-id="ac597-159">目前只會傳回資料表。</span><span class="sxs-lookup"><span data-stu-id="ac597-159">Currently only tables will be returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac597-160">JET_ObjInfoNoStats</span><span class="sxs-lookup"><span data-stu-id="ac597-160">JET_ObjInfoNoStats</span></span></p></td>
<td><p><span data-ttu-id="ac597-161"><em>pvResult</em> 會被解釋為 <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>。</span><span class="sxs-lookup"><span data-stu-id="ac597-161"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>.</span></span> <span data-ttu-id="ac597-162">只會抓取 <em>szObjectName</em> 中指定之物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ac597-162">Information about only the object given in <em>szObjectName</em> will be retrieved.</span></span></p>
<p><span data-ttu-id="ac597-163"><a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>結構將會填入與<em>szObjectName</em>中所命名物件相關的資訊。</span><span class="sxs-lookup"><span data-stu-id="ac597-163">The <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure will be populated with information pertaining to the object that is named in <em>szObjectName</em>.</span></span></p>
<p><span data-ttu-id="ac597-164">JET_ObjInfoNoStats 與 JET_ObjInfo 相同，不同之處在于報告記錄和頁面數目的欄位會設定為零。</span><span class="sxs-lookup"><span data-stu-id="ac597-164">JET_ObjInfoNoStats is identical to JET_ObjInfo, except that the fields that report the number of records and pages are set to zero.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac597-165">JET_ObjInfoRulesLoaded</span><span class="sxs-lookup"><span data-stu-id="ac597-165">JET_ObjInfoRulesLoaded</span></span></p></td>
<td><p><span data-ttu-id="ac597-166">已淘汰，目前不支援。</span><span class="sxs-lookup"><span data-stu-id="ac597-166">Deprecated and not currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac597-167">JET_ObjInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="ac597-167">JET_ObjInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="ac597-168">已淘汰，目前不支援。</span><span class="sxs-lookup"><span data-stu-id="ac597-168">Deprecated and not currently supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac597-169">JET_ObjInfoSysTabReadOnly</span><span class="sxs-lookup"><span data-stu-id="ac597-169">JET_ObjInfoSysTabReadOnly</span></span></p></td>
<td><p><span data-ttu-id="ac597-170">已淘汰，目前不支援。</span><span class="sxs-lookup"><span data-stu-id="ac597-170">Deprecated and not currently supported.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="ac597-171">傳回值</span><span class="sxs-lookup"><span data-stu-id="ac597-171">Return Value</span></span>

<span data-ttu-id="ac597-172">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="ac597-172">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ac597-173">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="ac597-173">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ac597-174">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ac597-174">Return code</span></span></p></th>
<th><p><span data-ttu-id="ac597-175">Description</span><span class="sxs-lookup"><span data-stu-id="ac597-175">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ac597-176">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ac597-176">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ac597-177">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="ac597-177">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac597-178">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="ac597-178">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="ac597-179"><em>CbMax</em>中提供的緩衝區大小太小，無法容納所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="ac597-179">The size of the buffer given in <em>cbMax</em> was too small to hold the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac597-180">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="ac597-180">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="ac597-181"><em>SzObjectName</em>或<em>szContainerName</em>中提供了不正確名稱。</span><span class="sxs-lookup"><span data-stu-id="ac597-181">An invalid name was given in <em>szObjectName</em> or <em>szContainerName</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac597-182">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="ac597-182">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="ac597-183">指定了不正確的參數。</span><span class="sxs-lookup"><span data-stu-id="ac597-183">A bad parameter was given.</span></span> <span data-ttu-id="ac597-184">可能會有不正確的層級傳遞至 <em>InfoLevel</em>。</span><span class="sxs-lookup"><span data-stu-id="ac597-184">It is possible that a bad level was passed in to <em>InfoLevel</em>.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="ac597-185">備註</span><span class="sxs-lookup"><span data-stu-id="ac597-185">Remarks</span></span>

<span data-ttu-id="ac597-186">如果 **JetGetObjectInfo** 成功建立臨時表 (例如，JET_ObjInfoList 或 JET_ObjInfoNoStats) ，則呼叫端會負責以 [JetCloseTable](./jetclosetable-function.md)關閉臨時表。</span><span class="sxs-lookup"><span data-stu-id="ac597-186">If **JetGetObjectInfo** successfully creates a temporary table (for example, JET_ObjInfoList or JET_ObjInfoNoStats), the caller is responsible for closing the temporary table with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="ac597-187">**JetGetObjectInfo** 目前僅支援抓取資料表的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ac597-187">**JetGetObjectInfo** currently only supports retrieving information about tables.</span></span>

#### <a name="requirements"></a><span data-ttu-id="ac597-188">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac597-188">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ac597-189"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="ac597-189"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ac597-190">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="ac597-190">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac597-191"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="ac597-191"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ac597-192">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="ac597-192">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac597-193"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="ac597-193"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ac597-194">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="ac597-194">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac597-195"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="ac597-195"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ac597-196">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="ac597-196">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac597-197"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ac597-197"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ac597-198">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="ac597-198">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac597-199"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="ac597-199"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="ac597-200">實作為 <strong>JetGetObjectInfoW</strong> (Unicode) 和 <strong>JetGetObjectInfoA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="ac597-200">Implemented as <strong>JetGetObjectInfoW</strong> (Unicode) and <strong>JetGetObjectInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ac597-201">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac597-201">See Also</span></span>

[<span data-ttu-id="ac597-202">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ac597-202">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ac597-203">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="ac597-203">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="ac597-204">JET_OBJTYP</span><span class="sxs-lookup"><span data-stu-id="ac597-204">JET_OBJTYP</span></span>](./jet-objtyp.md)  
[<span data-ttu-id="ac597-205">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ac597-205">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="ac597-206">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="ac597-206">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="ac597-207">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="ac597-207">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="ac597-208">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="ac597-208">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="ac597-209">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="ac597-209">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="ac597-210">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="ac597-210">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)
