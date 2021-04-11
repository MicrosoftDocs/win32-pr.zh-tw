---
description: 深入瞭解： JetPrereadIndexRanges 函數
title: JetPrereadIndexRanges 函式
TOCTitle: JetPrereadIndexRanges Function
ms:assetid: ab49abcc-eaeb-438f-8e6d-b08bc94d7bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835045(v=EXCHG.10)
ms:contentKeyID: 49894667
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetPrereadIndexRanges
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7cfdd8d25f7008f5fa854cbee32b54fa01942ce2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112048"
---
# <a name="jetprereadindexranges-function"></a><span data-ttu-id="28639-103">JetPrereadIndexRanges 函式</span><span class="sxs-lookup"><span data-stu-id="28639-103">JetPrereadIndexRanges Function</span></span>


<span data-ttu-id="28639-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="28639-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="28639-105">**JetPrereadIndexRanges** 函式會 prereads 索引以改善效能。</span><span class="sxs-lookup"><span data-stu-id="28639-105">The **JetPrereadIndexRanges** function prereads indexes to improve the performance.</span></span>

<span data-ttu-id="28639-106">**JetPrereadIndexRanges** 函式是在 Windows 8 作業系統中引進的。</span><span class="sxs-lookup"><span data-stu-id="28639-106">The **JetPrereadIndexRanges** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JetPrereadIndexRanges(
  __in          const JET_SESID sesid,
  __in          const JET_TABLEID tableid,
  __in_ecount(cIndexRanges)  const JET_INDEX_RANGE* const rgIndexRanges,
  __in          const unsigned long cIndexRanges,
  __out_opt     unsigned long* const pcRangesPreread,
  __in_ecount(ccolumnidPreread)  const JET_COLUMNID* const rgcolumnidPreread,
  __in          const unsigned long ccolumnidPreread,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="28639-107">參數</span><span class="sxs-lookup"><span data-stu-id="28639-107">Parameters</span></span>

<span data-ttu-id="28639-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="28639-108">*sesid*</span></span>

<span data-ttu-id="28639-109">要用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="28639-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="28639-110">*tableid*</span><span class="sxs-lookup"><span data-stu-id="28639-110">*tableid*</span></span>

<span data-ttu-id="28639-111">要針對其發出 prereads 的資料表。</span><span class="sxs-lookup"><span data-stu-id="28639-111">The table to issue the prereads against.</span></span>

<span data-ttu-id="28639-112">*rgIndexRanges*</span><span class="sxs-lookup"><span data-stu-id="28639-112">*rgIndexRanges*</span></span>

<span data-ttu-id="28639-113">要 preread 的索引鍵範圍。</span><span class="sxs-lookup"><span data-stu-id="28639-113">The key ranges to preread.</span></span>

<span data-ttu-id="28639-114">*cIndexRanges*</span><span class="sxs-lookup"><span data-stu-id="28639-114">*cIndexRanges*</span></span>

<span data-ttu-id="28639-115">要 preread 的索引鍵範圍數目，取決於 *rgIndexRanges* 中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="28639-115">The number of key ranges to preread, determined by the number of elements in *rgIndexRanges*.</span></span>

<span data-ttu-id="28639-116">*pcRangesPreread*</span><span class="sxs-lookup"><span data-stu-id="28639-116">*pcRangesPreread*</span></span>

<span data-ttu-id="28639-117">實際 preread 的索引鍵範圍數目。</span><span class="sxs-lookup"><span data-stu-id="28639-117">The number of key ranges that were actually preread.</span></span>

<span data-ttu-id="28639-118">*rgcolumnidPreread*</span><span class="sxs-lookup"><span data-stu-id="28639-118">*rgcolumnidPreread*</span></span>

<span data-ttu-id="28639-119">要 preread 之 long 值資料行的資料行識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="28639-119">List of column IDs for long value columns to preread.</span></span> <span data-ttu-id="28639-120">依預設，只會 preread 頁面記錄。</span><span class="sxs-lookup"><span data-stu-id="28639-120">By default, only the on-page record is preread.</span></span> <span data-ttu-id="28639-121">如果需要 preread 非 page long 值資料行，則必須透過此參數傳遞其資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="28639-121">If Off-page long value columns need to be preread, their column IDs need to be passed via this parameter.</span></span>

<span data-ttu-id="28639-122">*ccolumnidPreread*</span><span class="sxs-lookup"><span data-stu-id="28639-122">*ccolumnidPreread*</span></span>

<span data-ttu-id="28639-123">要 preread 之 long 值資料行的資料行識別碼數目，取決於 *rgcolumnidPreread* 中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="28639-123">The number of column IDs for long value columns to preread, determined by the number of elements in *rgcolumnidPreread*.</span></span>

<span data-ttu-id="28639-124">*grbit*</span><span class="sxs-lookup"><span data-stu-id="28639-124">*grbit*</span></span>

<span data-ttu-id="28639-125">一組位，指定下表所列的零或多個 preread 方向值。</span><span class="sxs-lookup"><span data-stu-id="28639-125">A group of bits that specifies zero or more of the preread direction values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="28639-126">值</span><span class="sxs-lookup"><span data-stu-id="28639-126">Value</span></span></p></th>
<th><p><span data-ttu-id="28639-127">意義</span><span class="sxs-lookup"><span data-stu-id="28639-127">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28639-128">轉寄</span><span class="sxs-lookup"><span data-stu-id="28639-128">Forward</span></span></p></td>
<td><p><span data-ttu-id="28639-129">向前 Preread。</span><span class="sxs-lookup"><span data-stu-id="28639-129">Preread forward.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28639-130">向後</span><span class="sxs-lookup"><span data-stu-id="28639-130">Backwards</span></span></p></td>
<td><p><span data-ttu-id="28639-131">向後 Preread。</span><span class="sxs-lookup"><span data-stu-id="28639-131">Preread backward.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28639-132">FirstPageOnly</span><span class="sxs-lookup"><span data-stu-id="28639-132">FirstPageOnly</span></span></p></td>
<td><p><span data-ttu-id="28639-133">只 Preread 任何長資料行的第一頁。</span><span class="sxs-lookup"><span data-stu-id="28639-133">Preread only the first page of any long column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28639-134">NormalizedKey</span><span class="sxs-lookup"><span data-stu-id="28639-134">NormalizedKey</span></span></p></td>
<td><p><span data-ttu-id="28639-135">提供正規化的索引鍵/書簽，而不是資料行值。</span><span class="sxs-lookup"><span data-stu-id="28639-135">Normalized key/bookmark provided instead of column value.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="28639-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="28639-136">Return value</span></span>

<span data-ttu-id="28639-137">此函數會傳回 [JET_ERR](./jet-err.md) 資料類型，其中包含下表所列的其中一個傳回碼。</span><span class="sxs-lookup"><span data-stu-id="28639-137">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="28639-138">如需可能的可延伸儲存引擎 (ESE) 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="28639-138">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="28639-139">傳回碼</span><span class="sxs-lookup"><span data-stu-id="28639-139">Return code</span></span></p></th>
<th><p><span data-ttu-id="28639-140">Description</span><span class="sxs-lookup"><span data-stu-id="28639-140">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28639-141">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="28639-141">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="28639-142">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="28639-142">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="28639-143">備註</span><span class="sxs-lookup"><span data-stu-id="28639-143">Remarks</span></span>

<span data-ttu-id="28639-144">如果具有指定索引鍵範圍的記錄不在緩衝區快取中，您應該啟動非同步讀取，以將記錄帶入資料庫緩衝區快取。</span><span class="sxs-lookup"><span data-stu-id="28639-144">If the records with the specified key ranges are not in the buffer cache, you should start asynchronous reads to bring the records into the database buffer cache.</span></span>

#### <a name="requirements"></a><span data-ttu-id="28639-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="28639-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28639-146"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="28639-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="28639-147">需要 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="28639-147">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28639-148"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="28639-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="28639-149">需要 Windows Server 2012。</span><span class="sxs-lookup"><span data-stu-id="28639-149">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28639-150"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="28639-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="28639-151">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="28639-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28639-152"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="28639-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="28639-153">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="28639-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28639-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="28639-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="28639-155">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="28639-155">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="28639-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28639-156">See also</span></span>

[<span data-ttu-id="28639-157">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="28639-157">JET_ERR</span></span>](./jet-err.md)
