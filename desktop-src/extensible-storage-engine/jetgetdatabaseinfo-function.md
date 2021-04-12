---
description: 深入瞭解： JetGetDatabaseInfo 函數
title: JetGetDatabaseInfo 函式
TOCTitle: JetGetDatabaseInfo Function
ms:assetid: bd3f92d0-7e98-4aa6-87c5-1c2760cbd1b5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294076(v=EXCHG.10)
ms:contentKeyID: 32765691
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81c414a1dd38f621ba86bf7b1c9ce87710801446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193040"
---
# <a name="jetgetdatabaseinfo-function"></a><span data-ttu-id="b64b1-103">JetGetDatabaseInfo 函式</span><span class="sxs-lookup"><span data-stu-id="b64b1-103">JetGetDatabaseInfo Function</span></span>


<span data-ttu-id="b64b1-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b64b1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetdatabaseinfo-function"></a><span data-ttu-id="b64b1-105">JetGetDatabaseInfo 函式</span><span class="sxs-lookup"><span data-stu-id="b64b1-105">JetGetDatabaseInfo Function</span></span>

<span data-ttu-id="b64b1-106">**JetGetDatabaseInfo** 函式會抓取與資料庫相關的各種資訊類型。</span><span class="sxs-lookup"><span data-stu-id="b64b1-106">The **JetGetDatabaseInfo** function retrieves various types of information about the database.</span></span> <span data-ttu-id="b64b1-107">當資料庫已附加或線上 (使用 **JetGetDatabaseInfo**) ，或資料庫或資料庫引擎離線 ([JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)) 時，可以呼叫這個 API。</span><span class="sxs-lookup"><span data-stu-id="b64b1-107">This API can be called while a database is attached or online (with **JetGetDatabaseInfo**) or while the database or database engine is offline (with [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)).</span></span>

```cpp
    JET_ERR JET_API JetGetDatabaseInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="b64b1-108">參數</span><span class="sxs-lookup"><span data-stu-id="b64b1-108">Parameters</span></span>

<span data-ttu-id="b64b1-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="b64b1-109">*sesid*</span></span>

<span data-ttu-id="b64b1-110">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="b64b1-110">The session to use for this call.</span></span>

<span data-ttu-id="b64b1-111">*dbid*</span><span class="sxs-lookup"><span data-stu-id="b64b1-111">*dbid*</span></span>

<span data-ttu-id="b64b1-112">要從中取得資訊的資料庫 [JET_DBID](./jet-dbid.md) 。</span><span class="sxs-lookup"><span data-stu-id="b64b1-112">The [JET_DBID](./jet-dbid.md) for the database to retrieve the information from.</span></span>

<span data-ttu-id="b64b1-113">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="b64b1-113">*pvResult*</span></span>

<span data-ttu-id="b64b1-114">將接收指定資訊之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="b64b1-114">Pointer to a buffer which will receive the specified information.</span></span> <span data-ttu-id="b64b1-115">緩衝區的大小（以位元組為單位）會以 *cbMax* 傳遞。</span><span class="sxs-lookup"><span data-stu-id="b64b1-115">The size of the buffer, in bytes, is passed in *cbMax*.</span></span>

<span data-ttu-id="b64b1-116">失敗時， *pvResult* 的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="b64b1-116">On failure the contents of *pvResult* are undefined.</span></span>

<span data-ttu-id="b64b1-117">儲存在 *pvResult* 中的資訊取決於 *InfoLevel*。</span><span class="sxs-lookup"><span data-stu-id="b64b1-117">The information stored in *pvResult* depends on *InfoLevel*.</span></span>

<span data-ttu-id="b64b1-118">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="b64b1-118">*cbMax*</span></span>

<span data-ttu-id="b64b1-119">在 *pvResult* 中傳遞的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b64b1-119">The size, in bytes, of the buffer that was passed in *pvResult*.</span></span>

<span data-ttu-id="b64b1-120">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="b64b1-120">*InfoLevel*</span></span>

<span data-ttu-id="b64b1-121">*InfoLevel* 指定應該針對指定的資料庫抓取何種類型的資訊。</span><span class="sxs-lookup"><span data-stu-id="b64b1-121">*InfoLevel* specifies which type of information should be retrieved about the specified database.</span></span> <span data-ttu-id="b64b1-122">它會影響 *pvResult* 的解讀方式。</span><span class="sxs-lookup"><span data-stu-id="b64b1-122">It affects how *pvResult* is interpreted.</span></span> <span data-ttu-id="b64b1-123">某些 *InfoLevel* 僅適用于離線 ([JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)) 或線上 (**JetGetDatabaseInfo**) 版本的 API。</span><span class="sxs-lookup"><span data-stu-id="b64b1-123">Some *InfoLevel* are available only in the offline ([JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)) or online (**JetGetDatabaseInfo**) version of the API.</span></span>

<span data-ttu-id="b64b1-124">如果提供的 *pvResult* 緩衝區太小，可能會根據 *InfoLevel* 傳回 JET_errInvalidBufferSize 或 JET_errBufferTooSmall。</span><span class="sxs-lookup"><span data-stu-id="b64b1-124">If the *pvResult* buffer provided is too small, either JET_errInvalidBufferSize or JET_errBufferTooSmall will be returned depending on the *InfoLevel*.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b64b1-125">值</span><span class="sxs-lookup"><span data-stu-id="b64b1-125">Value</span></span></p></th>
<th><p><span data-ttu-id="b64b1-126">意義</span><span class="sxs-lookup"><span data-stu-id="b64b1-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b64b1-127">JET_DbInfoCollate</span><span class="sxs-lookup"><span data-stu-id="b64b1-127">JET_DbInfoCollate</span></span></p></td>
<td><p><span data-ttu-id="b64b1-128">尚未支援並會傳回預設值。</span><span class="sxs-lookup"><span data-stu-id="b64b1-128">Not yet supported and return default values.</span></span> <span data-ttu-id="b64b1-129">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="b64b1-129">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b64b1-130">JET_DbInfoConnect</span><span class="sxs-lookup"><span data-stu-id="b64b1-130">JET_DbInfoConnect</span></span></p></td>
<td><p><span data-ttu-id="b64b1-131">這些 <em>InfoLevels</em> 已被取代，目前不受支援。</span><span class="sxs-lookup"><span data-stu-id="b64b1-131">These <em>InfoLevels</em> are deprecated and are not currently supported.</span></span> <span data-ttu-id="b64b1-132">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="b64b1-132">Do not use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b64b1-133">JET_DbInfoCountry</span><span class="sxs-lookup"><span data-stu-id="b64b1-133">JET_DbInfoCountry</span></span></p></td>
<td><p><span data-ttu-id="b64b1-134">尚未支援並會傳回預設值。</span><span class="sxs-lookup"><span data-stu-id="b64b1-134">Not yet supported and return default values.</span></span> <span data-ttu-id="b64b1-135">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="b64b1-135">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b64b1-136">JET_DbInfoCp</span><span class="sxs-lookup"><span data-stu-id="b64b1-136">JET_DbInfoCp</span></span></p></td>
<td><p><span data-ttu-id="b64b1-137">尚未支援並會傳回預設值。</span><span class="sxs-lookup"><span data-stu-id="b64b1-137">Not yet supported and return default values.</span></span> <span data-ttu-id="b64b1-138">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="b64b1-138">Do not use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b64b1-139">JET_DbInfoFilename</span><span class="sxs-lookup"><span data-stu-id="b64b1-139">JET_DbInfoFilename</span></span></p></td>
<td><p><span data-ttu-id="b64b1-140"><em>pvResult</em> 將會被視為字串緩衝區 (char \* ) 。</span><span class="sxs-lookup"><span data-stu-id="b64b1-140"><em>pvResult</em> will be interpreted as a string buffer (char \*).</span></span> <span data-ttu-id="b64b1-141">建議使用 MAX_PATH 緩衝區，但不是必要的。</span><span class="sxs-lookup"><span data-stu-id="b64b1-141">A MAX_PATH buffer is suggested, however not required.</span></span> <span data-ttu-id="b64b1-142">如果緩衝區不夠長，則會傳回 JET_errBufferTooSmall。</span><span class="sxs-lookup"><span data-stu-id="b64b1-142">If the buffer is not long enough, JET_errBufferTooSmall will be returned.</span></span> <span data-ttu-id="b64b1-143">字串將會填入此 DBID 的資料庫路徑。</span><span class="sxs-lookup"><span data-stu-id="b64b1-143">The string will be populated with the path of the database for this DBID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b64b1-144">JET_DbInfoFilesize</span><span class="sxs-lookup"><span data-stu-id="b64b1-144">JET_DbInfoFilesize</span></span></p></td>
<td><p><span data-ttu-id="b64b1-145"><em>pvResult</em> 將會被視為 DWORD (4 個位元組) 。</span><span class="sxs-lookup"><span data-stu-id="b64b1-145"><em>pvResult</em> will be interpreted as a DWORD (4 bytes).</span></span> <span data-ttu-id="b64b1-146">傳回頁面中資料庫的大小。</span><span class="sxs-lookup"><span data-stu-id="b64b1-146">Returns the size of the database in pages.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b64b1-147">JET_DbInfoIsam</span><span class="sxs-lookup"><span data-stu-id="b64b1-147">JET_DbInfoIsam</span></span></p></td>
<td><p><span data-ttu-id="b64b1-148">這些 <em>InfoLevels</em> 已被取代，目前不受支援。</span><span class="sxs-lookup"><span data-stu-id="b64b1-148">These <em>InfoLevels</em> are deprecated and are not currently supported.</span></span> <span data-ttu-id="b64b1-149">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="b64b1-149">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b64b1-150">JET_DbInfoLCID</span><span class="sxs-lookup"><span data-stu-id="b64b1-150">JET_DbInfoLCID</span></span></p></td>
<td><p><span data-ttu-id="b64b1-151"> (Windows XP 及更新版本) 此 <em>InfoLevel</em> 最初指定為： JET_DbInfoLangid (Windows 2000) </span><span class="sxs-lookup"><span data-stu-id="b64b1-151">(Windows XP and later) This <em>InfoLevel</em> was originally specified as: JET_DbInfoLangid (Windows 2000)</span></span></p>
<p><span data-ttu-id="b64b1-152"><em>pvResult</em> 將會被解讀為 long。</span><span class="sxs-lookup"><span data-stu-id="b64b1-152"><em>pvResult</em> will be interpreted as a long.</span></span> <span data-ttu-id="b64b1-153">這會傳回與此資料庫相關聯之 (LCID) 的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="b64b1-153">This returns the Locale identifier (LCID) associate with this database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b64b1-154">JET_DbInfoMisc</span><span class="sxs-lookup"><span data-stu-id="b64b1-154">JET_DbInfoMisc</span></span></p></td>
<td><p><span data-ttu-id="b64b1-155"><em>pvResult</em> 將會被視為 <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>。</span><span class="sxs-lookup"><span data-stu-id="b64b1-155"><em>pvResult</em> will be interpreted as a <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>.</span></span> <span data-ttu-id="b64b1-156"><a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>結構將會填入與所指定資料庫有關的資訊。</span><span class="sxs-lookup"><span data-stu-id="b64b1-156">The <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> structure will be populated with information pertaining to the database specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b64b1-157">JET_DbInfoOptions</span><span class="sxs-lookup"><span data-stu-id="b64b1-157">JET_DbInfoOptions</span></span></p></td>
<td><p><span data-ttu-id="b64b1-158"><em>pvResult</em> 將會被視為 <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> 的 (DWORD) 。</span><span class="sxs-lookup"><span data-stu-id="b64b1-158"><em>pvResult</em> will be interpreted as a <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> (DWORD).</span></span> <span data-ttu-id="b64b1-159">這會傳回資料庫是否在獨佔模式中開啟。</span><span class="sxs-lookup"><span data-stu-id="b64b1-159">This returns whether the database is opened in exclusive mode.</span></span> <span data-ttu-id="b64b1-160">如果資料庫處於獨佔模式 JET_bitDbExclusive 將會在提供的 <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> 中設定，否則會設定零。</span><span class="sxs-lookup"><span data-stu-id="b64b1-160">If the database is in exclusive mode JET_bitDbExclusive will be set in the <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> provided, otherwise zero is set.</span></span> <span data-ttu-id="b64b1-161">請注意，不會傳回<a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>和<a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>的其他資料庫<em>grbit</em>選項。</span><span class="sxs-lookup"><span data-stu-id="b64b1-161">Note other database <em>grbit</em> options for <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> and <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a> are not returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b64b1-162">JET_DbInfoPageSize</span><span class="sxs-lookup"><span data-stu-id="b64b1-162">JET_DbInfoPageSize</span></span></p></td>
<td><p><span data-ttu-id="b64b1-163">僅適用于 Windows XP 及更新版本。</span><span class="sxs-lookup"><span data-stu-id="b64b1-163">Available only on Windows XP and later.</span></span> <span data-ttu-id="b64b1-164"><em>pvResult</em> 將會被視為不帶正負號的 long。</span><span class="sxs-lookup"><span data-stu-id="b64b1-164"><em>pvResult</em> will be interpreted as a unsigned long.</span></span> <span data-ttu-id="b64b1-165">這會傳回資料庫的頁面大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b64b1-165">This will return the page size of the database in bytes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b64b1-166">JET_DbInfoSpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="b64b1-166">JET_DbInfoSpaceAvailable</span></span></p></td>
<td><p><span data-ttu-id="b64b1-167"><em>pvResult</em> 將會被解釋為 DWORD。</span><span class="sxs-lookup"><span data-stu-id="b64b1-167"><em>pvResult</em> will be interpreted as a DWORD.</span></span> <span data-ttu-id="b64b1-168">這會傳回資料庫在頁面中的可用空間。</span><span class="sxs-lookup"><span data-stu-id="b64b1-168">This returns the available space for the database in pages.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b64b1-169">JET_DbInfoSpaceOwned</span><span class="sxs-lookup"><span data-stu-id="b64b1-169">JET_DbInfoSpaceOwned</span></span></p></td>
<td><p><span data-ttu-id="b64b1-170"><em>pvResult</em> 將會被解釋為 DWORD。</span><span class="sxs-lookup"><span data-stu-id="b64b1-170"><em>pvResult</em> will be interpreted as a DWORD.</span></span> <span data-ttu-id="b64b1-171">這會傳回資料庫在頁面中所擁有的空間。</span><span class="sxs-lookup"><span data-stu-id="b64b1-171">This returns the owned space for the database in pages.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b64b1-172">JET_DbInfoTransactions</span><span class="sxs-lookup"><span data-stu-id="b64b1-172">JET_DbInfoTransactions</span></span></p></td>
<td><p><span data-ttu-id="b64b1-173"><em>pvResult</em> 將會被解讀為 long。</span><span class="sxs-lookup"><span data-stu-id="b64b1-173"><em>pvResult</em> will be interpreted as a long.</span></span> <span data-ttu-id="b64b1-174">這會傳回一個大於最大層級的交易（可進行交易）。</span><span class="sxs-lookup"><span data-stu-id="b64b1-174">This will return one greater than the maximum level to which transactions can be nested.</span></span> <span data-ttu-id="b64b1-175">如果以嵌套的方式 (呼叫 <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> ，也就是在相同的會話中，如果沒有認可或復原) 的次數與此值相同，則會從 <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a>傳回最後一個呼叫 JET_errTransTooDeep。</span><span class="sxs-lookup"><span data-stu-id="b64b1-175">If <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> is called (in a nesting fashion, that is, on the same session, without a commit or rollback) as many times as this value, on the last call JET_errTransTooDeep will be returned from <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a>.</span></span> <span data-ttu-id="b64b1-176">請注意 Windows 2000、Windows XP 及 Windows Server 2003 中的值是7。</span><span class="sxs-lookup"><span data-stu-id="b64b1-176">Note the value in Windows 2000, Windows XP, and Windows Server 2003 is 7.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b64b1-177">JET_DbInfoVersion</span><span class="sxs-lookup"><span data-stu-id="b64b1-177">JET_DbInfoVersion</span></span></p></td>
<td><p><span data-ttu-id="b64b1-178"><em>pvResult</em> 將會被解讀為 long。</span><span class="sxs-lookup"><span data-stu-id="b64b1-178"><em>pvResult</em> will be interpreted as a long.</span></span> <span data-ttu-id="b64b1-179">這會傳回資料庫引擎的原生主要版本。</span><span class="sxs-lookup"><span data-stu-id="b64b1-179">This returns the database engine's native major version.</span></span> <span data-ttu-id="b64b1-180">此值為 Windows 2000、Windows XP 及 Windows Server 2003 的0x620。</span><span class="sxs-lookup"><span data-stu-id="b64b1-180">This value is 0x620 for Windows 2000, Windows XP, and Windows Server 2003.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="b64b1-181">傳回值</span><span class="sxs-lookup"><span data-stu-id="b64b1-181">Return Value</span></span>

<span data-ttu-id="b64b1-182">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="b64b1-182">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b64b1-183">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="b64b1-183">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b64b1-184">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b64b1-184">Return code</span></span></p></th>
<th><p><span data-ttu-id="b64b1-185">Description</span><span class="sxs-lookup"><span data-stu-id="b64b1-185">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b64b1-186">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b64b1-186">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b64b1-187">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="b64b1-187">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b64b1-188">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="b64b1-188">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="b64b1-189"><em>CbMax</em>中提供的緩衝區大小太小 (或不正確) 來保存所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="b64b1-189">The size of the buffer given in <em>cbMax</em> was too small (or not correct) to hold the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b64b1-190">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="b64b1-190">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="b64b1-191">JET_DbInfoIsam 要求的 <em>InfoLevel</em> 。</span><span class="sxs-lookup"><span data-stu-id="b64b1-191">The <em>InfoLevel</em> requested was JET_DbInfoIsam.</span></span> <span data-ttu-id="b64b1-192">不支援此連結方式。</span><span class="sxs-lookup"><span data-stu-id="b64b1-192">This is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b64b1-193">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="b64b1-193">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="b64b1-194"><em>CbMax</em>中提供的緩衝區大小太小 (或不正確) 來保存所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="b64b1-194">The size of the buffer given in <em>cbMax</em> was too small (or not correct) to hold the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b64b1-195">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="b64b1-195">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="b64b1-196">提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="b64b1-196">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="b64b1-197">當提供的<a href="gg269248(v=exchg.10).md">JET_DBID</a>不是附加) 資料庫的有效 (時， <strong>JetGetDatabaseInfo</strong>會傳回這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="b64b1-197">This error will be returned by <strong>JetGetDatabaseInfo</strong> when the <a href="gg269248(v=exchg.10).md">JET_DBID</a> provided is not a valid (attached) database.</span></span> <span data-ttu-id="b64b1-198">當該版本的函式不支援要求的<em>InfoLevel</em>時， <a href="gg269239(v=exchg.10).md">JetGetDatabaseFileInfo</a>和<strong>JetGetDatabaseInfo</strong>會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="b64b1-198">This error will be returned by <a href="gg269239(v=exchg.10).md">JetGetDatabaseFileInfo</a> and <strong>JetGetDatabaseInfo</strong> when an <em>InfoLevel</em> requested is not supported by that version of the function.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b64b1-199">成功時，會在輸出緩衝區中傳回所要求的資料。</span><span class="sxs-lookup"><span data-stu-id="b64b1-199">On success, the requested data will be returned in the output buffer.</span></span>

<span data-ttu-id="b64b1-200">失敗時，輸出緩衝區會處於未定義狀態。</span><span class="sxs-lookup"><span data-stu-id="b64b1-200">On failure, the output buffer will be in an undefined state.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b64b1-201">規格需求</span><span class="sxs-lookup"><span data-stu-id="b64b1-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b64b1-202"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="b64b1-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b64b1-203">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="b64b1-203">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b64b1-204"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="b64b1-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b64b1-205">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="b64b1-205">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b64b1-206"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="b64b1-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b64b1-207">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="b64b1-207">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b64b1-208"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="b64b1-208"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b64b1-209">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="b64b1-209">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b64b1-210"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b64b1-210"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b64b1-211">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="b64b1-211">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b64b1-212"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="b64b1-212"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="b64b1-213">實作為 <strong>JetGetDatabaseInfoW</strong> (Unicode) 和 <strong>JetGetDatabaseInfoA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="b64b1-213">Implemented as <strong>JetGetDatabaseInfoW</strong> (Unicode) and <strong>JetGetDatabaseInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b64b1-214">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b64b1-214">See Also</span></span>

[<span data-ttu-id="b64b1-215">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="b64b1-215">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="b64b1-216">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b64b1-216">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b64b1-217">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="b64b1-217">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="b64b1-218">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="b64b1-218">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="b64b1-219">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="b64b1-219">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)  
[<span data-ttu-id="b64b1-220">JET_DBINFOUPGRADE</span><span class="sxs-lookup"><span data-stu-id="b64b1-220">JET_DBINFOUPGRADE</span></span>](./jet-dbinfoupgrade-structure.md)  
[<span data-ttu-id="b64b1-221">JetGetDatabaseFileInfo</span><span class="sxs-lookup"><span data-stu-id="b64b1-221">JetGetDatabaseFileInfo</span></span>](./jetgetdatabasefileinfo-function.md)
