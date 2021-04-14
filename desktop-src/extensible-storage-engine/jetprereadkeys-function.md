---
description: 深入瞭解： JetPrereadKeys 函數
title: JetPrereadKeys 函式
TOCTitle: JetPrereadKeys Function
ms:assetid: fc2f46bc-1f81-4af2-aa63-9757e819efc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294143(v=EXCHG.10)
ms:contentKeyID: 32765757
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrereadKeys
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d35407c171bdcd54eb44e9830f382c08a1e6c6c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469024"
---
# <a name="jetprereadkeys-function"></a><span data-ttu-id="9422b-103">JetPrereadKeys 函式</span><span class="sxs-lookup"><span data-stu-id="9422b-103">JetPrereadKeys Function</span></span>


<span data-ttu-id="9422b-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9422b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetprereadkeys-function"></a><span data-ttu-id="9422b-105">JetPrereadKeys 函式</span><span class="sxs-lookup"><span data-stu-id="9422b-105">JetPrereadKeys Function</span></span>

<span data-ttu-id="9422b-106">**JetPrereadKeys** 函式會讀取索引鍵值，以改善版本存放區清除的效能。</span><span class="sxs-lookup"><span data-stu-id="9422b-106">The **JetPrereadKeys** function reads key values to improve the performance of version store cleanup.</span></span>

<span data-ttu-id="9422b-107">**Windows 7： PrereadKeys** 函數是在 windows 7 中引進的。</span><span class="sxs-lookup"><span data-stu-id="9422b-107">**Windows 7:  PrereadKeys** function is introduced in Windows 7.</span></span>

```cpp
    JET_ERR JET_API JetPrereadKeys(
      __in JET_SESID sesid,
      __in JET_TABLEID tableid,
      __in_ecount(ckeys) const void ** rgpvKeys,
      __in_ecount(ckeys) const unsigned long * rgcbKeys,
      __in long ckeys,
      __out_opt long * pckeysPreread,
      __in JET_GRBIT grbit
     );
```

### <a name="parameters"></a><span data-ttu-id="9422b-108">參數</span><span class="sxs-lookup"><span data-stu-id="9422b-108">Parameters</span></span>

<span data-ttu-id="9422b-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="9422b-109">*sesid*</span></span>

<span data-ttu-id="9422b-110">要用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="9422b-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="9422b-111">*tableid*</span><span class="sxs-lookup"><span data-stu-id="9422b-111">*tableid*</span></span>

<span data-ttu-id="9422b-112">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="9422b-112">The cursor to use for this call.</span></span>

<span data-ttu-id="9422b-113">*rgpvKeys*</span><span class="sxs-lookup"><span data-stu-id="9422b-113">*rgpvKeys*</span></span>

<span data-ttu-id="9422b-114">索引鍵指標的陣列。</span><span class="sxs-lookup"><span data-stu-id="9422b-114">An array of pointers to keys.</span></span> <span data-ttu-id="9422b-115">您可以使用 [JetMakeKey](./jetmakekey-function.md) 或使用 [JetGetBookmark](./jetgetbookmark-function.md)來取得金鑰。</span><span class="sxs-lookup"><span data-stu-id="9422b-115">Keys can be made with [JetMakeKey](./jetmakekey-function.md) or retrieved with [JetGetBookmark](./jetgetbookmark-function.md).</span></span> <span data-ttu-id="9422b-116">索引鍵必須依照傳遞的 grbit，以遞增或遞減順序排序。</span><span class="sxs-lookup"><span data-stu-id="9422b-116">The keys must be sorted in ascending or descending order, depending on the grbit passed.</span></span> <span data-ttu-id="9422b-117">您可以使用 memcmp 來排序索引鍵。</span><span class="sxs-lookup"><span data-stu-id="9422b-117">Keys can be sorted with memcmp.</span></span>

<span data-ttu-id="9422b-118">*rgcbKeys*</span><span class="sxs-lookup"><span data-stu-id="9422b-118">*rgcbKeys*</span></span>

<span data-ttu-id="9422b-119">金鑰長度的陣列。</span><span class="sxs-lookup"><span data-stu-id="9422b-119">An array of key lengths.</span></span> <span data-ttu-id="9422b-120">rgpvKeys \[ n \] 應指向長度為 rgcbKeys n 的索引鍵 \[\]</span><span class="sxs-lookup"><span data-stu-id="9422b-120">rgpvKeys\[n\] should point to a key of length rgcbKeys\[n\]</span></span>

<span data-ttu-id="9422b-121">*ckeys*</span><span class="sxs-lookup"><span data-stu-id="9422b-121">*ckeys*</span></span>

<span data-ttu-id="9422b-122">索引鍵數目。</span><span class="sxs-lookup"><span data-stu-id="9422b-122">The number of keys.</span></span> <span data-ttu-id="9422b-123">rgpvKeys 和 rgcbKeys 都必須指向至少具有 ckeys 元素的陣列。</span><span class="sxs-lookup"><span data-stu-id="9422b-123">rgpvKeys and rgcbKeys must each point to an array with at least ckeys elements.</span></span>

<span data-ttu-id="9422b-124">*pckeysPreread*</span><span class="sxs-lookup"><span data-stu-id="9422b-124">*pckeysPreread*</span></span>

<span data-ttu-id="9422b-125">傳回 prereads 實際發出的索引鍵數目。</span><span class="sxs-lookup"><span data-stu-id="9422b-125">Returns the number of keys that prereads were actually issued for.</span></span> <span data-ttu-id="9422b-126">此參數可以是 Null。</span><span class="sxs-lookup"><span data-stu-id="9422b-126">This parameter can be NULL.</span></span>

<span data-ttu-id="9422b-127">*grbit*</span><span class="sxs-lookup"><span data-stu-id="9422b-127">*grbit*</span></span>

<span data-ttu-id="9422b-128">這必須是 JET_bitPrereadForward 或 JET_bitPrereadBackward。</span><span class="sxs-lookup"><span data-stu-id="9422b-128">This must be either JET_bitPrereadForward or JET_bitPrereadBackward.</span></span> <span data-ttu-id="9422b-129">如果 JET_bitPrereadForward grbit，索引鍵必須以遞增順序排序。</span><span class="sxs-lookup"><span data-stu-id="9422b-129">If grbit is JET_bitPrereadForward, the keys must be sorted in ascending order.</span></span> <span data-ttu-id="9422b-130">如果 JET_bitPrereadBackward grbit，索引鍵必須以遞減順序排序。</span><span class="sxs-lookup"><span data-stu-id="9422b-130">If grbit is JET_bitPrereadBackward, the keys must be sorted in descending order.</span></span>

### <a name="return-value"></a><span data-ttu-id="9422b-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="9422b-131">Return Value</span></span>

<span data-ttu-id="9422b-132">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="9422b-132">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9422b-133">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="9422b-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<span data-ttu-id="9422b-134">可能會傳回各種 i/o 錯誤以及這些 API 使用錯誤：</span><span class="sxs-lookup"><span data-stu-id="9422b-134">Various I/O errors can be returned along with these API usage errors:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9422b-135">傳回碼</span><span class="sxs-lookup"><span data-stu-id="9422b-135">Return code</span></span></p></th>
<th><p><span data-ttu-id="9422b-136">Description</span><span class="sxs-lookup"><span data-stu-id="9422b-136">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9422b-137">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="9422b-137">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="9422b-138">Grbit 不是 JET_bitPrereadForward 也不 JET_bitPrereadBackward。</span><span class="sxs-lookup"><span data-stu-id="9422b-138">Grbit was neither JET_bitPrereadForward nor JET_bitPrereadBackward.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9422b-139">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="9422b-139">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="9422b-140">傳入了不正確的金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="9422b-140">An incorrect key size has been passed in.</span></span> <span data-ttu-id="9422b-141">索引鍵不可以是0，也不能超過資料表的最大索引鍵長度。</span><span class="sxs-lookup"><span data-stu-id="9422b-141">Keys can neither be 0 nor longer than the maximum key length for the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9422b-142">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="9422b-142">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="9422b-143">傳入了不正確參數。</span><span class="sxs-lookup"><span data-stu-id="9422b-143">An invalid parameter has been passed in.</span></span> <span data-ttu-id="9422b-144">這可能是因為必要參數的 null 值，或可能表示金鑰陣列未正確排序。</span><span class="sxs-lookup"><span data-stu-id="9422b-144">This can be caused by a null value for a required parameter or can indicate that the key array is not sorted properly.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9422b-145">**JetPrereadKeys** 會遍歷 b 型樹狀目錄的內部頁面，以判斷哪些分葉頁面包含 RgpvKeys/rgcbKeys 所指定的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="9422b-145">**JetPrereadKeys** traverses the internal pages of the b-tree to determine which leaf pages contain the keys specified by rgpvKeys/rgcbKeys.</span></span> <span data-ttu-id="9422b-146">分葉頁面清單會排序，然後針對頁面的範圍發出 prereads。</span><span class="sxs-lookup"><span data-stu-id="9422b-146">The list of leaf pages is sorted and then prereads are issued for the ranges of pages.</span></span> <span data-ttu-id="9422b-147">可以 preread 的頁面數目有限，因此可能不會 preread 所有索引鍵。</span><span class="sxs-lookup"><span data-stu-id="9422b-147">The number of pages that can be preread is limited so it is possible that not all keys may be preread.</span></span> <span data-ttu-id="9422b-148">在此情況下，會在 pckeysPreread 中傳回實際 preread 的索引鍵數目。</span><span class="sxs-lookup"><span data-stu-id="9422b-148">In that case, the number of keys actually preread is returned in pckeysPreread.</span></span>

#### <a name="requirements"></a><span data-ttu-id="9422b-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="9422b-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9422b-150"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="9422b-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9422b-151">需要 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="9422b-151">Requires Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9422b-152"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="9422b-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9422b-153">需要 Windows Server 2008 R2。</span><span class="sxs-lookup"><span data-stu-id="9422b-153">Requires Windows Server 2008 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9422b-154"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="9422b-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9422b-155">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="9422b-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9422b-156"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="9422b-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9422b-157">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="9422b-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9422b-158"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="9422b-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9422b-159">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="9422b-159">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>
