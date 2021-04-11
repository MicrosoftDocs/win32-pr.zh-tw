---
description: 深入瞭解： JetGetTableIndexInfo 函數
title: JetGetTableIndexInfo 函式
TOCTitle: JetGetTableIndexInfo Function
ms:assetid: d250d254-2b10-4fe7-bbb1-72bb967f22dd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294102(v=EXCHG.10)
ms:contentKeyID: 32765717
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableIndexInfoW
- JetGetTableIndexInfoA
- JetGetTableIndexInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 904391218fbd073cd273655ce74fdec116b6a22e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195332"
---
# <a name="jetgettableindexinfo-function"></a><span data-ttu-id="3584c-103">JetGetTableIndexInfo 函式</span><span class="sxs-lookup"><span data-stu-id="3584c-103">JetGetTableIndexInfo Function</span></span>


<span data-ttu-id="3584c-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3584c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettableindexinfo-function"></a><span data-ttu-id="3584c-105">JetGetTableIndexInfo 函式</span><span class="sxs-lookup"><span data-stu-id="3584c-105">JetGetTableIndexInfo Function</span></span>

<span data-ttu-id="3584c-106">**JetGetTableIndexInfo** 函式會捕獲索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3584c-106">The **JetGetTableIndexInfo** function retrieves information about an index.</span></span>

```cpp
    JET_ERR JET_API JetGetTableIndexInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          const tchar* szIndexName,
      __out         void* pvResult,
      __in          unsigned long cbResult,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="3584c-107">參數</span><span class="sxs-lookup"><span data-stu-id="3584c-107">Parameters</span></span>

<span data-ttu-id="3584c-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="3584c-108">*sesid*</span></span>

<span data-ttu-id="3584c-109">要用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="3584c-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="3584c-110">*tableid*</span><span class="sxs-lookup"><span data-stu-id="3584c-110">*tableid*</span></span>

<span data-ttu-id="3584c-111">資料庫資料表，包含保存所需資訊的索引。</span><span class="sxs-lookup"><span data-stu-id="3584c-111">The database table that contains the index that holds the needed information.</span></span>

<span data-ttu-id="3584c-112">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="3584c-112">*szIndexName*</span></span>

<span data-ttu-id="3584c-113">包含即將抓取之資訊的索引名稱。</span><span class="sxs-lookup"><span data-stu-id="3584c-113">The name of the index that contains information that will be retrieved.</span></span>

<span data-ttu-id="3584c-114">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="3584c-114">*pvResult*</span></span>

<span data-ttu-id="3584c-115">將接收資訊的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="3584c-115">Pointer to a buffer which will receive the information.</span></span> <span data-ttu-id="3584c-116">緩衝區應該對齊以保存所需的類型。</span><span class="sxs-lookup"><span data-stu-id="3584c-116">The buffer should be aligned to hold the type required.</span></span> <span data-ttu-id="3584c-117">緩衝區的類型取決於 *InfoLevel* 參數。</span><span class="sxs-lookup"><span data-stu-id="3584c-117">The type of the buffer is dependent on the *InfoLevel* parameter.</span></span>

<span data-ttu-id="3584c-118">*cbResult*</span><span class="sxs-lookup"><span data-stu-id="3584c-118">*cbResult*</span></span>

<span data-ttu-id="3584c-119">在 *pvResult* 參數中傳遞的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3584c-119">The size, in bytes, of the buffer passed in the *pvResult* parameter.</span></span>

<span data-ttu-id="3584c-120">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="3584c-120">*InfoLevel*</span></span>

<span data-ttu-id="3584c-121">指定將儲存在 *pvResult* 中的資訊。</span><span class="sxs-lookup"><span data-stu-id="3584c-121">Specifies which information will be stored in *pvResult*.</span></span> <span data-ttu-id="3584c-122">有效值為：</span><span class="sxs-lookup"><span data-stu-id="3584c-122">The valid values are:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3584c-123">值</span><span class="sxs-lookup"><span data-stu-id="3584c-123">Value</span></span></p></th>
<th><p><span data-ttu-id="3584c-124">意義</span><span class="sxs-lookup"><span data-stu-id="3584c-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3584c-125">JET_IdxInfo</span><span class="sxs-lookup"><span data-stu-id="3584c-125">JET_IdxInfo</span></span></p></td>
<td><p><span data-ttu-id="3584c-126"><em>pvResult</em> 會被視為 <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> 結構。</span><span class="sxs-lookup"><span data-stu-id="3584c-126"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="3584c-127">成功時， <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> 結構會接收有關索引的資訊。</span><span class="sxs-lookup"><span data-stu-id="3584c-127">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="3584c-128">失敗時， <em>pvBuffer</em> 的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="3584c-128">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3584c-129">JET_IdxInfoLCID</span><span class="sxs-lookup"><span data-stu-id="3584c-129">JET_IdxInfoLCID</span></span></p></td>
<td><p><span data-ttu-id="3584c-130"><em>pvResult</em> 會被解釋為 LCID。</span><span class="sxs-lookup"><span data-stu-id="3584c-130"><em>pvResult</em> is interpreted as an LCID.</span></span> <span data-ttu-id="3584c-131">成功時，LCID 會保存索引的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="3584c-131">On success, the LCID holds the Locale Identifier of the index.</span></span> <span data-ttu-id="3584c-132">失敗時， <em>pvBuffer</em> 的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="3584c-132">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3584c-133">JET_IdxInfoList</span><span class="sxs-lookup"><span data-stu-id="3584c-133">JET_IdxInfoList</span></span></p></td>
<td><p><span data-ttu-id="3584c-134"><em>pvResult</em> 會被視為 <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> 結構。</span><span class="sxs-lookup"><span data-stu-id="3584c-134"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="3584c-135">成功時， <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> 結構會接收有關索引的資訊。</span><span class="sxs-lookup"><span data-stu-id="3584c-135">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="3584c-136">失敗時， <em>pvBuffer</em> 的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="3584c-136">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3584c-137">JET_IdxInfoOLC</span><span class="sxs-lookup"><span data-stu-id="3584c-137">JET_IdxInfoOLC</span></span></p></td>
<td><p><span data-ttu-id="3584c-138">JET_IdxInfoOLC 已淘汰。</span><span class="sxs-lookup"><span data-stu-id="3584c-138">JET_IdxInfoOLC is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3584c-139">JET_IdxInfoResetOLC</span><span class="sxs-lookup"><span data-stu-id="3584c-139">JET_IdxInfoResetOLC</span></span></p></td>
<td><p><span data-ttu-id="3584c-140">JET_IdxInfoResetOLC 已淘汰。</span><span class="sxs-lookup"><span data-stu-id="3584c-140">JET_IdxInfoResetOLC is obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3584c-141">JET_IdxInfoSpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="3584c-141">JET_IdxInfoSpaceAlloc</span></span></p></td>
<td><p><span data-ttu-id="3584c-142"><em>pvResult</em> 會被解釋為 ULONG。</span><span class="sxs-lookup"><span data-stu-id="3584c-142"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="3584c-143">成功時，ULONG 會保存索引的空間使用量。</span><span class="sxs-lookup"><span data-stu-id="3584c-143">On success, the ULONG holds the space usage of the index.</span></span> <span data-ttu-id="3584c-144">失敗時， <em>pvBuffer</em> 的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="3584c-144">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3584c-145">JET_IdxInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="3584c-145">JET_IdxInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="3584c-146">JET_IdxInfoSysTabCursor 已淘汰。</span><span class="sxs-lookup"><span data-stu-id="3584c-146">JET_IdxInfoSysTabCursor is obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3584c-147">JET_IdxInfoLangid</span><span class="sxs-lookup"><span data-stu-id="3584c-147">JET_IdxInfoLangid</span></span></p></td>
<td><p><span data-ttu-id="3584c-148">JET_IdxInfoLangid 已被取代。</span><span class="sxs-lookup"><span data-stu-id="3584c-148">JET_IdxInfoLangid is deprecated.</span></span> <span data-ttu-id="3584c-149">請改用 JET_IdxInfoLCID 和 <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> 宏。</span><span class="sxs-lookup"><span data-stu-id="3584c-149">Use JET_IdxInfoLCID instead, and the <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> macro instead.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3584c-150">JET_IdxInfoCount</span><span class="sxs-lookup"><span data-stu-id="3584c-150">JET_IdxInfoCount</span></span></p></td>
<td><p><span data-ttu-id="3584c-151"><em>pvResult</em> 會被解釋為 ULONG。</span><span class="sxs-lookup"><span data-stu-id="3584c-151"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="3584c-152">成功時，ULONG 會保存指定資料表上的索引計數。</span><span class="sxs-lookup"><span data-stu-id="3584c-152">On success, the ULONG holds the count of indexes on the specified table.</span></span> <span data-ttu-id="3584c-153"><em>szIndexName</em> 會被忽略。</span><span class="sxs-lookup"><span data-stu-id="3584c-153"><em>szIndexName</em> is ignored.</span></span> <span data-ttu-id="3584c-154">失敗時， <em>pvBuffer</em> 的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="3584c-154">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3584c-155">JET_IdxInfoVarSegMac</span><span class="sxs-lookup"><span data-stu-id="3584c-155">JET_IdxInfoVarSegMac</span></span></p></td>
<td><p><span data-ttu-id="3584c-156"><em>pvResult</em> 會被解釋為 USHORT。</span><span class="sxs-lookup"><span data-stu-id="3584c-156"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="3584c-157">成功時，USHORT 會保存建立索引時所使用的 <em>cbVarSegMac</em> 值。</span><span class="sxs-lookup"><span data-stu-id="3584c-157">On success, the USHORT holds the value of <em>cbVarSegMac</em> used when the index was created.</span></span> <span data-ttu-id="3584c-158">如需<em>cbVarSegMac</em>的說明，請參閱<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 。</span><span class="sxs-lookup"><span data-stu-id="3584c-158">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a description of <em>cbVarSegMac</em>.</span></span> <span data-ttu-id="3584c-159">失敗時， <em>pvBuffer</em> 的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="3584c-159">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3584c-160">JET_IdxInfoIndexId</span><span class="sxs-lookup"><span data-stu-id="3584c-160">JET_IdxInfoIndexId</span></span></p></td>
<td><p><span data-ttu-id="3584c-161"><em>pvResult</em> 會被解釋為 <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>。</span><span class="sxs-lookup"><span data-stu-id="3584c-161"><em>pvResult</em> is interpreted as a <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>.</span></span> <span data-ttu-id="3584c-162">成功時， <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> 結構會接收有關索引的資訊。</span><span class="sxs-lookup"><span data-stu-id="3584c-162">On success, the <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> structure receives information about the index.</span></span> <span data-ttu-id="3584c-163">失敗時， <em>pvBuffer</em> 的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="3584c-163">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3584c-164">JET_IdxInfoKeyMost</span><span class="sxs-lookup"><span data-stu-id="3584c-164">JET_IdxInfoKeyMost</span></span></p></td>
<td><p><span data-ttu-id="3584c-165"><em>pvResult</em> 會被解釋為 USHORT。</span><span class="sxs-lookup"><span data-stu-id="3584c-165"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="3584c-166">成功時，USHORT 會保存建立索引時所使用的 cbKeyMost 值。</span><span class="sxs-lookup"><span data-stu-id="3584c-166">On success, the USHORT holds the value of cbKeyMost used when the index was created.</span></span> <span data-ttu-id="3584c-167">如需 cbKeyMost 的說明，請參閱 <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 結構。</span><span class="sxs-lookup"><span data-stu-id="3584c-167">See the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure for a description of cbKeyMost.</span></span> <span data-ttu-id="3584c-168">失敗時， <em>pvBuffer</em> 的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="3584c-168">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3584c-169">JET_IdxInfoCreateIndex</span><span class="sxs-lookup"><span data-stu-id="3584c-169">JET_IdxInfoCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="3584c-170"><em>pvResult</em> 會被視為 <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 結構。</span><span class="sxs-lookup"><span data-stu-id="3584c-170"><em>pvResult</em> is interpreted as a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="3584c-171">失敗時， <em>pvBuffer</em> 的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="3584c-171">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="3584c-172"><strong>Windows 7：  </strong>JET_IdxInfoCreateIndex 是在 Windows 7 中引進的。</span><span class="sxs-lookup"><span data-stu-id="3584c-172"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3584c-173">JET_IdxInfoCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="3584c-173">JET_IdxInfoCreateIndex2</span></span></p></td>
<td><p><span data-ttu-id="3584c-174"><em>pvResult</em> 會被視為 <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> 結構。</span><span class="sxs-lookup"><span data-stu-id="3584c-174"><em>pvResult</em> is interpreted as a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="3584c-175">失敗時， <em>pvBuffer</em> 的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="3584c-175">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="3584c-176"><strong>Windows 7：  </strong>JET_IdxInfoCreateIndex2 是在 Windows 7 中引進的。</span><span class="sxs-lookup"><span data-stu-id="3584c-176"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex2 is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="3584c-177">傳回值</span><span class="sxs-lookup"><span data-stu-id="3584c-177">Return Value</span></span>

<span data-ttu-id="3584c-178">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="3584c-178">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="3584c-179">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="3584c-179">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3584c-180">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3584c-180">Return code</span></span></p></th>
<th><p><span data-ttu-id="3584c-181">Description</span><span class="sxs-lookup"><span data-stu-id="3584c-181">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3584c-182">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3584c-182">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3584c-183">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="3584c-183">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3584c-184">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="3584c-184">JET_errIndexNotFound</span></span></p></td>
<td><p><span data-ttu-id="3584c-185">在指定的資料表中找不到指定的索引。</span><span class="sxs-lookup"><span data-stu-id="3584c-185">The specified index cannot be found in the specified table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3584c-186">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="3584c-186">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="3584c-187">傳入作為 <em>pvResult</em> 的緩衝區太小。</span><span class="sxs-lookup"><span data-stu-id="3584c-187">The buffer passed in as <em>pvResult</em> was too small.</span></span> <span data-ttu-id="3584c-188">緩衝區的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="3584c-188">The contents of the buffer are undefined.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="3584c-189">備註</span><span class="sxs-lookup"><span data-stu-id="3584c-189">Remarks</span></span>

<span data-ttu-id="3584c-190">[JetGetIndexInfo](./jetgetindexinfo-function.md) 和 **JetGetTableIndexInfo** 會取得有關索引的相同資訊。</span><span class="sxs-lookup"><span data-stu-id="3584c-190">[JetGetIndexInfo](./jetgetindexinfo-function.md) and **JetGetTableIndexInfo** retrieve identical information about an index.</span></span> <span data-ttu-id="3584c-191">不同之處在于如何指定資料表。</span><span class="sxs-lookup"><span data-stu-id="3584c-191">The difference is in how the table is specified.</span></span> <span data-ttu-id="3584c-192">[JetGetIndexInfo](./jetgetindexinfo-function.md) 預期資料庫 (*dbid*) 和資料表名稱 (*szTableName*) ，而 **JetGetTableIndexInfo** 預期資料表識別碼 (*tableid*) 。</span><span class="sxs-lookup"><span data-stu-id="3584c-192">[JetGetIndexInfo](./jetgetindexinfo-function.md) expects a database (*dbid*) and name of a table (*szTableName*), while **JetGetTableIndexInfo** expects a table identifier (*tableid*).</span></span>

#### <a name="requirements"></a><span data-ttu-id="3584c-193">規格需求</span><span class="sxs-lookup"><span data-stu-id="3584c-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3584c-194"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="3584c-194"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3584c-195">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="3584c-195">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3584c-196"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="3584c-196"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3584c-197">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="3584c-197">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3584c-198"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="3584c-198"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3584c-199">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="3584c-199">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3584c-200"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="3584c-200"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3584c-201">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="3584c-201">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3584c-202"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="3584c-202"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3584c-203">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="3584c-203">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3584c-204"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="3584c-204"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="3584c-205">實作為 <strong>JetGetTableIndexInfoW</strong> (Unicode) 和 <strong>JetGetTableIndexInfoA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="3584c-205">Implemented as <strong>JetGetTableIndexInfoW</strong> (Unicode) and <strong>JetGetTableIndexInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3584c-206">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3584c-206">See Also</span></span>

[<span data-ttu-id="3584c-207">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="3584c-207">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="3584c-208">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3584c-208">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3584c-209">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="3584c-209">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="3584c-210">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="3584c-210">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="3584c-211">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="3584c-211">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="3584c-212">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="3584c-212">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="3584c-213">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="3584c-213">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="3584c-214">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="3584c-214">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)
