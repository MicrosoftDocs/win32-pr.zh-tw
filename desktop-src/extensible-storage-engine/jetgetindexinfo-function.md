---
description: 深入瞭解： JetGetIndexInfo 函數
title: JetGetIndexInfo 函式
TOCTitle: JetGetIndexInfo Function
ms:assetid: c6235281-e208-4966-bc66-ec1ab27333c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294084(v=EXCHG.10)
ms:contentKeyID: 32765699
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetIndexInfoW
- JetGetIndexInfoA
- JetGetIndexInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a0fd506390ba9f228c115d0b9142baffdbe1587
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997835"
---
# <a name="jetgetindexinfo-function"></a><span data-ttu-id="31d6b-103">JetGetIndexInfo 函式</span><span class="sxs-lookup"><span data-stu-id="31d6b-103">JetGetIndexInfo Function</span></span>


<span data-ttu-id="31d6b-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="31d6b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetindexinfo-function"></a><span data-ttu-id="31d6b-105">JetGetIndexInfo 函式</span><span class="sxs-lookup"><span data-stu-id="31d6b-105">JetGetIndexInfo Function</span></span>

<span data-ttu-id="31d6b-106">**JetGetIndexInfo** 函式會捕獲索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="31d6b-106">The **JetGetIndexInfo** function retrieves information about an index.</span></span>

```cpp
    JET_ERR JET_API JetGetIndexInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szIndexName,
      __out         void* pvResult,
      __in          unsigned long cbResult,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="31d6b-107">參數</span><span class="sxs-lookup"><span data-stu-id="31d6b-107">Parameters</span></span>

<span data-ttu-id="31d6b-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="31d6b-108">*sesid*</span></span>

<span data-ttu-id="31d6b-109">要用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="31d6b-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="31d6b-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="31d6b-110">*dbid*</span></span>

<span data-ttu-id="31d6b-111">用於 API 呼叫的資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="31d6b-111">The database identifier to use for the API call.</span></span>

<span data-ttu-id="31d6b-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="31d6b-112">*szTableName*</span></span>

<span data-ttu-id="31d6b-113">包含索引的資料表名稱，其中包含要取出的資訊。</span><span class="sxs-lookup"><span data-stu-id="31d6b-113">The name of the table containing the index with the information to retrieve.</span></span>

<span data-ttu-id="31d6b-114">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="31d6b-114">*szIndexName*</span></span>

<span data-ttu-id="31d6b-115">具有要取出之資訊的索引名稱。</span><span class="sxs-lookup"><span data-stu-id="31d6b-115">The name of the index with the information to retrieve.</span></span>

<span data-ttu-id="31d6b-116">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="31d6b-116">*pvResult*</span></span>

<span data-ttu-id="31d6b-117">將接收所需資訊的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="31d6b-117">Pointer to a buffer that will receive the desired information.</span></span> <span data-ttu-id="31d6b-118">緩衝區應該對齊以保存所需的類型。</span><span class="sxs-lookup"><span data-stu-id="31d6b-118">The buffer should be aligned to hold the type required.</span></span> <span data-ttu-id="31d6b-119">緩衝區的類型取決於 *InfoLevel* 參數。</span><span class="sxs-lookup"><span data-stu-id="31d6b-119">The type of the buffer is dependent on the *InfoLevel* parameter.</span></span>

<span data-ttu-id="31d6b-120">*cbResult*</span><span class="sxs-lookup"><span data-stu-id="31d6b-120">*cbResult*</span></span>

<span data-ttu-id="31d6b-121">傳遞為 *pvResult* 的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="31d6b-121">The size, in bytes, of the buffer passed as *pvResult*.</span></span>

<span data-ttu-id="31d6b-122">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="31d6b-122">*InfoLevel*</span></span>

<span data-ttu-id="31d6b-123">將儲存在 *pvResult* 中的資訊。</span><span class="sxs-lookup"><span data-stu-id="31d6b-123">The information that will be stored in *pvResult*.</span></span> <span data-ttu-id="31d6b-124">下列選項可用於此參數。</span><span class="sxs-lookup"><span data-stu-id="31d6b-124">The following options can be used for this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="31d6b-125">值</span><span class="sxs-lookup"><span data-stu-id="31d6b-125">Value</span></span></p></th>
<th><p><span data-ttu-id="31d6b-126">意義</span><span class="sxs-lookup"><span data-stu-id="31d6b-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31d6b-127">JET_IdxInfo</span><span class="sxs-lookup"><span data-stu-id="31d6b-127">JET_IdxInfo</span></span></p></td>
<td><p><span data-ttu-id="31d6b-128"><em>pvResult</em> 會被視為 <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> 結構。</span><span class="sxs-lookup"><span data-stu-id="31d6b-128"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="31d6b-129">成功時， <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> 結構會接收有關索引的資訊。</span><span class="sxs-lookup"><span data-stu-id="31d6b-129">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="31d6b-130">失敗時， <em>pvBuffer</em> 的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="31d6b-130">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31d6b-131">JET_IdxInfoCount</span><span class="sxs-lookup"><span data-stu-id="31d6b-131">JET_IdxInfoCount</span></span></p></td>
<td><p><span data-ttu-id="31d6b-132"><em>pvResult</em> 會被解釋為 ULONG。</span><span class="sxs-lookup"><span data-stu-id="31d6b-132"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="31d6b-133">成功時，ULONG 會保存指定資料表上的索引計數。</span><span class="sxs-lookup"><span data-stu-id="31d6b-133">On success, the ULONG holds the count of indexes on the specified table.</span></span> <span data-ttu-id="31d6b-134"><em>szIndexName</em> 會被忽略。</span><span class="sxs-lookup"><span data-stu-id="31d6b-134"><em>szIndexName</em> is ignored.</span></span> <span data-ttu-id="31d6b-135">失敗時， <em>pvBuffer</em> 的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="31d6b-135">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31d6b-136">JET_IdxInfoIndexId</span><span class="sxs-lookup"><span data-stu-id="31d6b-136">JET_IdxInfoIndexId</span></span></p></td>
<td><p><span data-ttu-id="31d6b-137"><em>pvResult</em> 會被解釋為 <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>。</span><span class="sxs-lookup"><span data-stu-id="31d6b-137"><em>pvResult</em> is interpreted as a <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>.</span></span> <span data-ttu-id="31d6b-138">成功時， <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> 結構會接收有關索引的資訊。</span><span class="sxs-lookup"><span data-stu-id="31d6b-138">On success, the <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> structure receives information about the index.</span></span> <span data-ttu-id="31d6b-139">失敗時， <em>pvBuffer</em> 的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="31d6b-139">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31d6b-140">JET_IdxInfoLangid</span><span class="sxs-lookup"><span data-stu-id="31d6b-140">JET_IdxInfoLangid</span></span></p></td>
<td><p><span data-ttu-id="31d6b-141">JET_IdxInfoLangid 已被取代。</span><span class="sxs-lookup"><span data-stu-id="31d6b-141">JET_IdxInfoLangid is deprecated.</span></span> <span data-ttu-id="31d6b-142">請改用 JET_IdxInfoLCID 和 <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> 宏。</span><span class="sxs-lookup"><span data-stu-id="31d6b-142">Use JET_IdxInfoLCID and the <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> macro instead.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31d6b-143">JET_IdxInfoLCID</span><span class="sxs-lookup"><span data-stu-id="31d6b-143">JET_IdxInfoLCID</span></span></p></td>
<td><p><span data-ttu-id="31d6b-144"><em>pvResult</em> 會被解釋為 LCID。</span><span class="sxs-lookup"><span data-stu-id="31d6b-144"><em>pvResult</em> is interpreted as an LCID.</span></span> <span data-ttu-id="31d6b-145">成功時，LCID 會保存索引的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="31d6b-145">On success, the LCID holds the Locale Identifier of the index.</span></span> <span data-ttu-id="31d6b-146">失敗時， <em>pvBuffer</em> 的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="31d6b-146">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="31d6b-147"><strong>WINDOWS XP：  </strong>JET_IdxInfoLCID 是在 Windows XP 中引進。</span><span class="sxs-lookup"><span data-stu-id="31d6b-147"><strong>Windows XP:  </strong>JET_IdxInfoLCID is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31d6b-148">JET_IdxInfoList</span><span class="sxs-lookup"><span data-stu-id="31d6b-148">JET_IdxInfoList</span></span></p></td>
<td><p><span data-ttu-id="31d6b-149"><em>pvResult</em> 會被視為 <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> 結構。</span><span class="sxs-lookup"><span data-stu-id="31d6b-149"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="31d6b-150">成功時， <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> 結構會接收有關索引的資訊。</span><span class="sxs-lookup"><span data-stu-id="31d6b-150">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="31d6b-151">失敗時， <em>pvBuffer</em> 的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="31d6b-151">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31d6b-152">JET_IdxInfoOLC</span><span class="sxs-lookup"><span data-stu-id="31d6b-152">JET_IdxInfoOLC</span></span></p></td>
<td><p><span data-ttu-id="31d6b-153">JET_IdxInfoOLC 已淘汰。</span><span class="sxs-lookup"><span data-stu-id="31d6b-153">JET_IdxInfoOLC is obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31d6b-154">JET_IdxInfoResetOLC</span><span class="sxs-lookup"><span data-stu-id="31d6b-154">JET_IdxInfoResetOLC</span></span></p></td>
<td><p><span data-ttu-id="31d6b-155">JET_IdxInfoResetOLC 已淘汰。</span><span class="sxs-lookup"><span data-stu-id="31d6b-155">JET_IdxInfoResetOLC is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31d6b-156">JET_IdxInfoSpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="31d6b-156">JET_IdxInfoSpaceAlloc</span></span></p></td>
<td><p><span data-ttu-id="31d6b-157"><em>pvResult</em> 會被解釋為 ULONG。</span><span class="sxs-lookup"><span data-stu-id="31d6b-157"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="31d6b-158">成功時，ULONG 會保存索引的空間使用量。</span><span class="sxs-lookup"><span data-stu-id="31d6b-158">On success, the ULONG holds the space usage of the index.</span></span> <span data-ttu-id="31d6b-159">失敗時， <em>pvBuffer</em> 的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="31d6b-159">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31d6b-160">JET_IdxInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="31d6b-160">JET_IdxInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="31d6b-161">JET_IdxInfoSysTabCursor 已淘汰。</span><span class="sxs-lookup"><span data-stu-id="31d6b-161">JET_IdxInfoSysTabCursor is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31d6b-162">JET_IdxInfoVarSegMac</span><span class="sxs-lookup"><span data-stu-id="31d6b-162">JET_IdxInfoVarSegMac</span></span></p></td>
<td><p><span data-ttu-id="31d6b-163"><em>pvResult</em> 會被解釋為 USHORT。</span><span class="sxs-lookup"><span data-stu-id="31d6b-163"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="31d6b-164">成功時，USHORT 會保存建立索引時所使用的 <em>cbVarSegMac</em> 值。</span><span class="sxs-lookup"><span data-stu-id="31d6b-164">On success, the USHORT holds the value of <em>cbVarSegMac</em> used when the index was created.</span></span> <span data-ttu-id="31d6b-165">如需<em>cbVarSegMac</em>的說明，請參閱<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 。</span><span class="sxs-lookup"><span data-stu-id="31d6b-165">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a description of <em>cbVarSegMac</em>.</span></span> <span data-ttu-id="31d6b-166">失敗時， <em>pvBuffer</em> 的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="31d6b-166">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31d6b-167">JET_IdxInfoKeyMost</span><span class="sxs-lookup"><span data-stu-id="31d6b-167">JET_IdxInfoKeyMost</span></span></p></td>
<td><p><span data-ttu-id="31d6b-168"><em>pvResult</em> 會被解釋為 USHORT。</span><span class="sxs-lookup"><span data-stu-id="31d6b-168"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="31d6b-169">成功時，USHORT 會保存建立索引時所使用的 <em>cbKeyMost</em> 值。</span><span class="sxs-lookup"><span data-stu-id="31d6b-169">On success, the USHORT holds the value of <em>cbKeyMost</em> used when the index was created.</span></span> <span data-ttu-id="31d6b-170">如需<em>cbKeyMost</em>的說明，請參閱<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 。</span><span class="sxs-lookup"><span data-stu-id="31d6b-170">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a description of <em>cbKeyMost</em>.</span></span> <span data-ttu-id="31d6b-171">失敗時， <em>pvBuffer</em> 的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="31d6b-171">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="31d6b-172"><strong>Windows Vista：  </strong>JET_IdxInfoKeyMost 是在 Windows Vista 中引進。</span><span class="sxs-lookup"><span data-stu-id="31d6b-172"><strong>Windows Vista:  </strong>JET_IdxInfoKeyMost is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31d6b-173">JET_IdxInfoCreateIndex</span><span class="sxs-lookup"><span data-stu-id="31d6b-173">JET_IdxInfoCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="31d6b-174"><em>pvResult</em> 會被視為 <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 結構。</span><span class="sxs-lookup"><span data-stu-id="31d6b-174"><em>pvResult</em> is interpreted as a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="31d6b-175">失敗時， <em>pvBuffer</em> 的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="31d6b-175">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="31d6b-176"><strong>Windows 7：  </strong>JET_IdxInfoCreateIndex 是在 Windows 7 中引進的。</span><span class="sxs-lookup"><span data-stu-id="31d6b-176"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31d6b-177">JET_IdxInfoCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="31d6b-177">JET_IdxInfoCreateIndex2</span></span></p></td>
<td><p><span data-ttu-id="31d6b-178"><em>pvResult</em> 會被視為 <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> 結構。</span><span class="sxs-lookup"><span data-stu-id="31d6b-178"><em>pvResult</em> is interpreted as a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="31d6b-179">失敗時， <em>pvBuffer</em> 的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="31d6b-179">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="31d6b-180"><strong>Windows 7：  </strong>JET_IdxInfoCreateIndex2 是在 Windows 7 中引進的。</span><span class="sxs-lookup"><span data-stu-id="31d6b-180"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex2 is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="31d6b-181">傳回值</span><span class="sxs-lookup"><span data-stu-id="31d6b-181">Return Value</span></span>

<span data-ttu-id="31d6b-182">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="31d6b-182">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="31d6b-183">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="31d6b-183">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="31d6b-184">傳回碼</span><span class="sxs-lookup"><span data-stu-id="31d6b-184">Return code</span></span></p></th>
<th><p><span data-ttu-id="31d6b-185">Description</span><span class="sxs-lookup"><span data-stu-id="31d6b-185">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31d6b-186">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="31d6b-186">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="31d6b-187">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="31d6b-187">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31d6b-188">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="31d6b-188">JET_errIndexNotFound</span></span></p></td>
<td><p><span data-ttu-id="31d6b-189">在指定的資料表中找不到指定的索引。</span><span class="sxs-lookup"><span data-stu-id="31d6b-189">The specified index cannot be found in the specified table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31d6b-190">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="31d6b-190">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="31d6b-191">傳入作為 <em>pvResult</em> 的緩衝區太小。</span><span class="sxs-lookup"><span data-stu-id="31d6b-191">The buffer passed in as <em>pvResult</em> was too small.</span></span> <span data-ttu-id="31d6b-192">緩衝區的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="31d6b-192">The contents of the buffer are undefined.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="31d6b-193">備註</span><span class="sxs-lookup"><span data-stu-id="31d6b-193">Remarks</span></span>

<span data-ttu-id="31d6b-194">**JetGetIndexInfo** 和 [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) 會取得有關索引的相同資訊。</span><span class="sxs-lookup"><span data-stu-id="31d6b-194">**JetGetIndexInfo** and [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) retrieve identical information about an index.</span></span> <span data-ttu-id="31d6b-195">不同之處在于如何指定資料表。</span><span class="sxs-lookup"><span data-stu-id="31d6b-195">The difference is in how the table is specified.</span></span> <span data-ttu-id="31d6b-196">**JetGetIndexInfo** 預期資料庫 (*dbid*) 和資料表名稱 (*szTableName*) ，而 [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) 預期資料表識別碼 (*tableid*) 。</span><span class="sxs-lookup"><span data-stu-id="31d6b-196">**JetGetIndexInfo** expects a database (*dbid*) and name of a table (*szTableName*), while [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) expects a table identifier (*tableid*).</span></span>

#### <a name="requirements"></a><span data-ttu-id="31d6b-197">規格需求</span><span class="sxs-lookup"><span data-stu-id="31d6b-197">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31d6b-198"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="31d6b-198"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="31d6b-199">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="31d6b-199">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31d6b-200"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="31d6b-200"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="31d6b-201">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="31d6b-201">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31d6b-202"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="31d6b-202"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="31d6b-203">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="31d6b-203">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31d6b-204"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="31d6b-204"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="31d6b-205">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="31d6b-205">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31d6b-206"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="31d6b-206"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="31d6b-207">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="31d6b-207">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31d6b-208"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="31d6b-208"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="31d6b-209">實作為 <strong>JetGetIndexInfoW</strong> (Unicode) 和 <strong>JetGetIndexInfoA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="31d6b-209">Implemented as <strong>JetGetIndexInfoW</strong> (Unicode) and <strong>JetGetIndexInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="31d6b-210">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31d6b-210">See Also</span></span>

[<span data-ttu-id="31d6b-211">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="31d6b-211">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="31d6b-212">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="31d6b-212">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="31d6b-213">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="31d6b-213">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="31d6b-214">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="31d6b-214">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="31d6b-215">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="31d6b-215">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="31d6b-216">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="31d6b-216">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="31d6b-217">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="31d6b-217">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="31d6b-218">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="31d6b-218">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)
