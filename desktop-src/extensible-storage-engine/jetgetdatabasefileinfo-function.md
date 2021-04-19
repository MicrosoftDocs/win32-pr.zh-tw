---
description: 深入瞭解： JetGetDatabaseFileInfo 函數
title: JetGetDatabaseFileInfo 函式
TOCTitle: JetGetDatabaseFileInfo Function
ms:assetid: 457079d9-46c9-4da0-a35b-0c11fca7ed5b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269239(v=EXCHG.10)
ms:contentKeyID: 32765541
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetDatabaseFileInfo
- JetGetDatabaseFileInfoW
- JetGetDatabaseFileInfoA
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2ac94dd6f088a82c932aaca5b60ec16f49644f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971663"
---
# <a name="jetgetdatabasefileinfo-function"></a><span data-ttu-id="6378c-103">JetGetDatabaseFileInfo 函式</span><span class="sxs-lookup"><span data-stu-id="6378c-103">JetGetDatabaseFileInfo Function</span></span>


<span data-ttu-id="6378c-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6378c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetdatabasefileinfo-function"></a><span data-ttu-id="6378c-105">JetGetDatabaseFileInfo 函式</span><span class="sxs-lookup"><span data-stu-id="6378c-105">JetGetDatabaseFileInfo Function</span></span>

<span data-ttu-id="6378c-106">**JetGetDatabaseFileInfo** 函式會抓取與資料庫相關的各種資訊類型。</span><span class="sxs-lookup"><span data-stu-id="6378c-106">The **JetGetDatabaseFileInfo** function retrieves various types of information about the database.</span></span> <span data-ttu-id="6378c-107">當資料庫已附加或線上 (使用 [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) ，或資料庫或資料庫引擎離線 (**JetGetDatabaseFileInfo**) 時，可以呼叫這個 API。</span><span class="sxs-lookup"><span data-stu-id="6378c-107">This API can be called while a database is attached or online (with [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) or while the database or database engine is offline (with **JetGetDatabaseFileInfo**).</span></span>

```cpp
    JET_ERR JET_API JetGetDatabaseFileInfo(
      __in          const tchar* szDatabaseName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="6378c-108">參數</span><span class="sxs-lookup"><span data-stu-id="6378c-108">Parameters</span></span>

<span data-ttu-id="6378c-109">*szDatabaseName*</span><span class="sxs-lookup"><span data-stu-id="6378c-109">*szDatabaseName*</span></span>

<span data-ttu-id="6378c-110">從中取得資訊的資料庫路徑。</span><span class="sxs-lookup"><span data-stu-id="6378c-110">The path of the database from which to retrieve the information.</span></span>

<span data-ttu-id="6378c-111">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="6378c-111">*pvResult*</span></span>

<span data-ttu-id="6378c-112">將接收指定資訊之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="6378c-112">Pointer to a buffer that will receive the specified information.</span></span> <span data-ttu-id="6378c-113">緩衝區的大小（以位元組為單位）會以 *cbMax* 傳遞。</span><span class="sxs-lookup"><span data-stu-id="6378c-113">The size of the buffer, in bytes, is passed in *cbMax*.</span></span>

<span data-ttu-id="6378c-114">如果此函式失敗， *pvResult* 的內容會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="6378c-114">If this function fails, the contents of *pvResult* are undefined.</span></span>

<span data-ttu-id="6378c-115">儲存在 *pvResult* 中的資訊取決於 *InfoLevel*。</span><span class="sxs-lookup"><span data-stu-id="6378c-115">The information stored in *pvResult* depends on *InfoLevel*.</span></span>

<span data-ttu-id="6378c-116">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="6378c-116">*cbMax*</span></span>

<span data-ttu-id="6378c-117">傳入 *pvResult* 的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6378c-117">The size, in bytes, of the buffer passed in *pvResult*.</span></span>

<span data-ttu-id="6378c-118">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="6378c-118">*InfoLevel*</span></span>

<span data-ttu-id="6378c-119">*InfoLevel* 指定應該針對指定的資料庫抓取何種類型的資訊。</span><span class="sxs-lookup"><span data-stu-id="6378c-119">*InfoLevel* specifies which type of information should be retrieved about the specified database.</span></span> <span data-ttu-id="6378c-120">它會影響 *pvResult* 的解讀方式。</span><span class="sxs-lookup"><span data-stu-id="6378c-120">It affects how *pvResult* is interpreted.</span></span> <span data-ttu-id="6378c-121">某些 *InfoLevel* 物件僅適用于離線 (**JetGetDatabaseFileInfo**) 或線上 ([JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) 版本的 API。</span><span class="sxs-lookup"><span data-stu-id="6378c-121">Some *InfoLevel* objects are available only in the offline (**JetGetDatabaseFileInfo**) or online ([JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) version of the API.</span></span>

<span data-ttu-id="6378c-122">如果提供的 *pvResult* 緩衝區太小，可能會傳回 JET_errInvalidBufferSize 或 JET_errBufferTooSmall，視 *InfoLevel* 而定。</span><span class="sxs-lookup"><span data-stu-id="6378c-122">If the *pvResult* buffer provided is too small, either JET_errInvalidBufferSize or JET_errBufferTooSmall will be returned, depending on the *InfoLevel*.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6378c-123">值</span><span class="sxs-lookup"><span data-stu-id="6378c-123">Value</span></span></p></th>
<th><p><span data-ttu-id="6378c-124">意義</span><span class="sxs-lookup"><span data-stu-id="6378c-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6378c-125">JET_DbInfoFilesize</span><span class="sxs-lookup"><span data-stu-id="6378c-125">JET_DbInfoFilesize</span></span></p></td>
<td><p><span data-ttu-id="6378c-126"><em>pvResult</em> 將會被視為 QWORD (8 個位元組) 。</span><span class="sxs-lookup"><span data-stu-id="6378c-126"><em>pvResult</em> will be interpreted as a QWORD (8 bytes).</span></span> <span data-ttu-id="6378c-127">傳回資料庫的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6378c-127">Returns the size of the database in bytes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6378c-128">JET_DbInfoUpgrade</span><span class="sxs-lookup"><span data-stu-id="6378c-128">JET_DbInfoUpgrade</span></span></p></td>
<td><p><span data-ttu-id="6378c-129"><em>pvResult</em> 將會被視為 <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a>。</span><span class="sxs-lookup"><span data-stu-id="6378c-129"><em>pvResult</em> will be interpreted as a <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a>.</span></span> <span data-ttu-id="6378c-130"><a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a>結構將會填入與指定資料庫相關的資訊。</span><span class="sxs-lookup"><span data-stu-id="6378c-130">The <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a> structure will be populated with information pertaining to the specified database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6378c-131">JET_DbInfoMisc</span><span class="sxs-lookup"><span data-stu-id="6378c-131">JET_DbInfoMisc</span></span></p></td>
<td><p><span data-ttu-id="6378c-132"><em>pvResult</em> 將會被視為 <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>。</span><span class="sxs-lookup"><span data-stu-id="6378c-132"><em>pvResult</em> will be interpreted as a <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>.</span></span> <span data-ttu-id="6378c-133"><a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>結構將會填入與指定資料庫相關的資訊。</span><span class="sxs-lookup"><span data-stu-id="6378c-133">The <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> structure will be populated with information pertaining to the specified database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6378c-134">JET_DbInfoDBInUse</span><span class="sxs-lookup"><span data-stu-id="6378c-134">JET_DbInfoDBInUse</span></span></p></td>
<td><p><span data-ttu-id="6378c-135"><em>pvResult</em> 將會被視為 BOOL (4 個位元組) 。</span><span class="sxs-lookup"><span data-stu-id="6378c-135"><em>pvResult</em> will be interpreted as a BOOL (4 bytes).</span></span> <span data-ttu-id="6378c-136">這會傳回資料庫引擎目前是否有任何開啟或附加的資料庫。</span><span class="sxs-lookup"><span data-stu-id="6378c-136">This will return whether the database engine currently has any open or attached databases.</span></span></p>
<p><span data-ttu-id="6378c-137"><strong>WINDOWS XP：  </strong>此值是在 Windows XP 中引進。</span><span class="sxs-lookup"><span data-stu-id="6378c-137"><strong>Windows XP:  </strong>This value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6378c-138">JET_DbInfoPageSize</span><span class="sxs-lookup"><span data-stu-id="6378c-138">JET_DbInfoPageSize</span></span></p></td>
<td><p><span data-ttu-id="6378c-139"><em>pvResult</em> 將會被視為不帶正負號的 long。</span><span class="sxs-lookup"><span data-stu-id="6378c-139"><em>pvResult</em> will be interpreted as a unsigned long.</span></span> <span data-ttu-id="6378c-140">這會傳回資料庫的頁面大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6378c-140">This will return the page size of the database in bytes.</span></span></p>
<p><span data-ttu-id="6378c-141"><strong>WINDOWS XP：  </strong>此值是在 Windows XP 中引進。</span><span class="sxs-lookup"><span data-stu-id="6378c-141"><strong>Windows XP:  </strong>This value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6378c-142">JET_DbInfoCp</span><span class="sxs-lookup"><span data-stu-id="6378c-142">JET_DbInfoCp</span></span></p></td>
<td><p><span data-ttu-id="6378c-143">這些 <em>InfoLevels</em> 尚未受到支援，並會傳回預設值。</span><span class="sxs-lookup"><span data-stu-id="6378c-143">These <em>InfoLevels</em> are not yet supported and return default values.</span></span> <span data-ttu-id="6378c-144">請勿使用這些 <em>InfoLevels</em>。</span><span class="sxs-lookup"><span data-stu-id="6378c-144">Do not use these <em>InfoLevels</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6378c-145">JET_DbInfoCountry</span><span class="sxs-lookup"><span data-stu-id="6378c-145">JET_DbInfoCountry</span></span></p></td>
<td><p><span data-ttu-id="6378c-146">這些 <em>InfoLevels</em> 尚未受到支援，並會傳回預設值。</span><span class="sxs-lookup"><span data-stu-id="6378c-146">These <em>InfoLevels</em> are not yet supported and return default values.</span></span> <span data-ttu-id="6378c-147">請勿使用這些 <em>InfoLevels</em>。</span><span class="sxs-lookup"><span data-stu-id="6378c-147">Do not use these <em>InfoLevels</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6378c-148">JET_DbInfoCollate</span><span class="sxs-lookup"><span data-stu-id="6378c-148">JET_DbInfoCollate</span></span></p></td>
<td><p><span data-ttu-id="6378c-149">與 JET_DbInfoCp 相同。</span><span class="sxs-lookup"><span data-stu-id="6378c-149">Same as JET_DbInfoCp.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6378c-150">JET_DbInfoIsam</span><span class="sxs-lookup"><span data-stu-id="6378c-150">JET_DbInfoIsam</span></span></p></td>
<td><p><span data-ttu-id="6378c-151">這些 <em>InfoLevels</em> 已被取代，目前不受支援。</span><span class="sxs-lookup"><span data-stu-id="6378c-151">These <em>InfoLevels</em> are deprecated and are not currently supported.</span></span> <span data-ttu-id="6378c-152">請勿使用這些 <em>InfoLevels</em>。</span><span class="sxs-lookup"><span data-stu-id="6378c-152">Do not use these <em>InfoLevels</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6378c-153">JET_DbInfoConnect</span><span class="sxs-lookup"><span data-stu-id="6378c-153">JET_DbInfoConnect</span></span></p></td>
<td><p><span data-ttu-id="6378c-154">與 JET_DbInfoIsam 相同。</span><span class="sxs-lookup"><span data-stu-id="6378c-154">Same as JET_DbInfoIsam.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6378c-155">JET_DbInfoFileType</span><span class="sxs-lookup"><span data-stu-id="6378c-155">JET_DbInfoFileType</span></span></p></td>
<td><p><span data-ttu-id="6378c-156"><strong>Windows Vista：  </strong>這個 <em>InfoLevel</em> 值是在 Windows Vista 中引進的。</span><span class="sxs-lookup"><span data-stu-id="6378c-156"><strong>Windows Vista:  </strong>This <em>InfoLevel</em> value is introduced in Windows Vista.</span></span></p>
<p><span data-ttu-id="6378c-157"><em>pvResult</em> 會被視為 DWORD 指標。</span><span class="sxs-lookup"><span data-stu-id="6378c-157"><em>pvResult</em> will be treated as a pointer to a DWORD.</span></span> <span data-ttu-id="6378c-158">傳回列舉值，這個值表示引擎將此視為何種檔案類型。</span><span class="sxs-lookup"><span data-stu-id="6378c-158">Returns an enumeration value, indicating what kind of file the engine considers this to be.</span></span> <span data-ttu-id="6378c-159">下表列出檔案類型。</span><span class="sxs-lookup"><span data-stu-id="6378c-159">File types are listed in the following table.</span></span> <span data-ttu-id="6378c-160">如需這些檔案類型及其使用方式的詳細資訊，請參閱 <a href="gg294069(v=exchg.10).md">可擴充儲存引擎</a>檔案。</span><span class="sxs-lookup"><span data-stu-id="6378c-160">For more information about these types of files and their usage to the engine, see <a href="gg294069(v=exchg.10).md">Extensible Storage Engine Files</a>.</span></span></p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6378c-161">值</span><span class="sxs-lookup"><span data-stu-id="6378c-161">Value</span></span></p></th>
<th><p><span data-ttu-id="6378c-162">意義</span><span class="sxs-lookup"><span data-stu-id="6378c-162">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6378c-163">JET_filetypeUnknown</span><span class="sxs-lookup"><span data-stu-id="6378c-163">JET_filetypeUnknown</span></span></p></td>
<td><p><span data-ttu-id="6378c-164">檔案類型未知，或不是 ESE 檔案類型。</span><span class="sxs-lookup"><span data-stu-id="6378c-164">The type of file is unknown, or not an ESE file type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6378c-165">JET_filetypeDatabase</span><span class="sxs-lookup"><span data-stu-id="6378c-165">JET_filetypeDatabase</span></span></p></td>
<td><p><span data-ttu-id="6378c-166">檔案是資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="6378c-166">The file is a database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6378c-167">JET_filetypeLog</span><span class="sxs-lookup"><span data-stu-id="6378c-167">JET_filetypeLog</span></span></p></td>
<td><p><span data-ttu-id="6378c-168">檔案是交易記錄檔。</span><span class="sxs-lookup"><span data-stu-id="6378c-168">The file is a transaction log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6378c-169">JET_filetypeCheckpoint</span><span class="sxs-lookup"><span data-stu-id="6378c-169">JET_filetypeCheckpoint</span></span></p></td>
<td><p><span data-ttu-id="6378c-170">檔案是檢查點檔案。</span><span class="sxs-lookup"><span data-stu-id="6378c-170">The file is a checkpoint file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6378c-171">JET_filetypeTempDatabase</span><span class="sxs-lookup"><span data-stu-id="6378c-171">JET_filetypeTempDatabase</span></span></p></td>
<td><p><span data-ttu-id="6378c-172">檔案是暫存的資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="6378c-172">The file is a temporary database file.</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="6378c-173">傳回值</span><span class="sxs-lookup"><span data-stu-id="6378c-173">Return Value</span></span>

<span data-ttu-id="6378c-174">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="6378c-174">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6378c-175">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="6378c-175">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6378c-176">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6378c-176">Return code</span></span></p></th>
<th><p><span data-ttu-id="6378c-177">Description</span><span class="sxs-lookup"><span data-stu-id="6378c-177">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6378c-178">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6378c-178">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6378c-179">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="6378c-179">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6378c-180">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="6378c-180">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="6378c-181">JET_DbInfoIsam 要求的 <em>InfoLevel</em> 。</span><span class="sxs-lookup"><span data-stu-id="6378c-181">The <em>InfoLevel</em> requested was JET_DbInfoIsam.</span></span> <span data-ttu-id="6378c-182">不支援此連結方式。</span><span class="sxs-lookup"><span data-stu-id="6378c-182">This is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6378c-183">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="6378c-183">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="6378c-184"><em>CbMax</em>中提供的緩衝區太小，無法取得所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="6378c-184">The buffer that is given in <em>cbMax</em> is too small for the desired information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6378c-185">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="6378c-185">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="6378c-186"><em>CbMax</em>中提供的緩衝區不是所需資訊的正確大小。</span><span class="sxs-lookup"><span data-stu-id="6378c-186">The buffer that is given in <em>cbMax</em> is not the correct size for the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6378c-187">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="6378c-187">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="6378c-188">提供的其中一個參數包含未預期的值，或多個參數值的組合產生了非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="6378c-188">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span> <span data-ttu-id="6378c-189">當提供的 DBID 不是附加) 資料庫的有效 (時， <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> 會傳回這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="6378c-189">This error will be returned by <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> when the DBID provided is not a valid (attached) database.</span></span> <span data-ttu-id="6378c-190">當該版本的函式不支援要求的<em>InfoLevel</em>時， <strong>JetGetDatabaseFileInfo</strong>和<a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a>會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="6378c-190">This error will be returned by <strong>JetGetDatabaseFileInfo</strong> and <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> when an <em>InfoLevel</em> requested is not supported by that version of the function.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6378c-191">如果此函式成功，則會在輸出緩衝區中傳回所要求的資料。</span><span class="sxs-lookup"><span data-stu-id="6378c-191">If this function succeeds, the requested data will be returned in the output buffer.</span></span>

<span data-ttu-id="6378c-192">如果此函式失敗，輸出緩衝區將會處於未定義狀態。</span><span class="sxs-lookup"><span data-stu-id="6378c-192">If this function fails, the output buffer will be in an undefined state.</span></span>

#### <a name="requirements"></a><span data-ttu-id="6378c-193">規格需求</span><span class="sxs-lookup"><span data-stu-id="6378c-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6378c-194"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="6378c-194"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6378c-195">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="6378c-195">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6378c-196"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="6378c-196"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6378c-197">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="6378c-197">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6378c-198"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="6378c-198"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6378c-199">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="6378c-199">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6378c-200"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="6378c-200"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6378c-201">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="6378c-201">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6378c-202"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6378c-202"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6378c-203">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="6378c-203">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6378c-204"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="6378c-204"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="6378c-205">實作為 <strong>JetGetDatabaseFileInfoW</strong> (Unicode) 和 <strong>JetGetDatabaseFileInfoA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="6378c-205">Implemented as <strong>JetGetDatabaseFileInfoW</strong> (Unicode) and <strong>JetGetDatabaseFileInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6378c-206">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6378c-206">See Also</span></span>

[<span data-ttu-id="6378c-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6378c-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6378c-208">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="6378c-208">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)  
[<span data-ttu-id="6378c-209">JET_DBINFOUPGRADE</span><span class="sxs-lookup"><span data-stu-id="6378c-209">JET_DBINFOUPGRADE</span></span>](./jet-dbinfoupgrade-structure.md)  
[<span data-ttu-id="6378c-210">JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="6378c-210">JetGetDatabaseInfo</span></span>](./jetgetdatabaseinfo-function.md)
