---
description: 深入瞭解： JetDeleteIndex 函數
title: JetDeleteIndex 函式
TOCTitle: JetDeleteIndex Function
ms:assetid: c540503b-d5a6-47f2-9113-9650891c4b6d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294081(v=EXCHG.10)
ms:contentKeyID: 32765696
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteIndexW
- JetDeleteIndexA
- JetDeleteIndex
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 52a29e619d6643df4984bd7f296dcef4ef0a5ccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985135"
---
# <a name="jetdeleteindex-function"></a><span data-ttu-id="641c9-103">JetDeleteIndex 函式</span><span class="sxs-lookup"><span data-stu-id="641c9-103">JetDeleteIndex Function</span></span>


<span data-ttu-id="641c9-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="641c9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeleteindex-function"></a><span data-ttu-id="641c9-105">JetDeleteIndex 函式</span><span class="sxs-lookup"><span data-stu-id="641c9-105">JetDeleteIndex Function</span></span>

<span data-ttu-id="641c9-106">**JetDeleteIndex** 函數會從資料表中刪除索引。</span><span class="sxs-lookup"><span data-stu-id="641c9-106">The **JetDeleteIndex** function deletes an index from a table.</span></span>

```cpp
    JET_ERR JET_API JetDeleteIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName
    );
```

### <a name="parameters"></a><span data-ttu-id="641c9-107">參數</span><span class="sxs-lookup"><span data-stu-id="641c9-107">Parameters</span></span>

<span data-ttu-id="641c9-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="641c9-108">*sesid*</span></span>

<span data-ttu-id="641c9-109">要用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="641c9-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="641c9-110">*tableid*</span><span class="sxs-lookup"><span data-stu-id="641c9-110">*tableid*</span></span>

<span data-ttu-id="641c9-111">包含要刪除之資料行的資料表。</span><span class="sxs-lookup"><span data-stu-id="641c9-111">The table that contains the column that is to be deleted.</span></span>

<span data-ttu-id="641c9-112">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="641c9-112">*szIndexName*</span></span>

<span data-ttu-id="641c9-113">要刪除的索引名稱。</span><span class="sxs-lookup"><span data-stu-id="641c9-113">The name of the index to be deleted.</span></span>

### <a name="return-value"></a><span data-ttu-id="641c9-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="641c9-114">Return Value</span></span>

<span data-ttu-id="641c9-115">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="641c9-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="641c9-116">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="641c9-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="641c9-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="641c9-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="641c9-118">Description</span><span class="sxs-lookup"><span data-stu-id="641c9-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="641c9-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="641c9-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="641c9-120">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="641c9-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="641c9-121">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="641c9-121">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="641c9-122">嘗試刪除固定資料表中的索引 (例如，一個是以 JET_bitTableCreateFixedDDL) 所建立的。</span><span class="sxs-lookup"><span data-stu-id="641c9-122">An attempt was made to delete an index from a fixed table (for example, one created with JET_bitTableCreateFixedDDL).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="641c9-123">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="641c9-123">JET_errFixedInheritedDDL</span></span></p></td>
<td><p><span data-ttu-id="641c9-124">嘗試刪除範本資料表中的索引。</span><span class="sxs-lookup"><span data-stu-id="641c9-124">An attempt was made to delete an index from a template table.</span></span> <span data-ttu-id="641c9-125">範本資料表具有固定的 DDL。</span><span class="sxs-lookup"><span data-stu-id="641c9-125">A template table has fixed DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="641c9-126">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="641c9-126">JET_errIndexNotFound</span></span></p></td>
<td><p><span data-ttu-id="641c9-127">在 <em>szIndexName</em> 中找不到名為的索引。</span><span class="sxs-lookup"><span data-stu-id="641c9-127">The index named in <em>szIndexName</em> was not found.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="641c9-128">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="641c9-128">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="641c9-129">因為資料表是以唯讀方式開啟，所以無法更新。</span><span class="sxs-lookup"><span data-stu-id="641c9-129">The table cannot be updated because it was opened read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="641c9-130">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="641c9-130">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="641c9-131">多個執行緒嘗試使用相同的資料庫會話。</span><span class="sxs-lookup"><span data-stu-id="641c9-131">Multiple threads attempted to use the same database session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="641c9-132">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="641c9-132">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="641c9-133">交易已開啟為唯讀交易。</span><span class="sxs-lookup"><span data-stu-id="641c9-133">The transaction was opened as a read-only transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="641c9-134">備註</span><span class="sxs-lookup"><span data-stu-id="641c9-134">Remarks</span></span>

<span data-ttu-id="641c9-135">成功時，會刪除索引，因此無法再使用。</span><span class="sxs-lookup"><span data-stu-id="641c9-135">When successful, the index is deleted and therefore cannot be used subsequently.</span></span> <span data-ttu-id="641c9-136">使用索引時，不能有任何使用中的交易。</span><span class="sxs-lookup"><span data-stu-id="641c9-136">There must not be any active transaction using the index.</span></span>

<span data-ttu-id="641c9-137">成功時，會在第一筆記錄之前設定貨幣。</span><span class="sxs-lookup"><span data-stu-id="641c9-137">On success, the currency is set before the first record.</span></span>

#### <a name="requirements"></a><span data-ttu-id="641c9-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="641c9-138">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="641c9-139"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="641c9-139"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="641c9-140">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="641c9-140">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="641c9-141"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="641c9-141"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="641c9-142">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="641c9-142">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="641c9-143"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="641c9-143"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="641c9-144">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="641c9-144">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="641c9-145"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="641c9-145"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="641c9-146">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="641c9-146">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="641c9-147"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="641c9-147"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="641c9-148">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="641c9-148">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="641c9-149"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="641c9-149"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="641c9-150">實作為 <strong>JetDeleteIndexW</strong> (Unicode) 和 <strong>JetDeleteIndexA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="641c9-150">Implemented as <strong>JetDeleteIndexW</strong> (Unicode) and <strong>JetDeleteIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="641c9-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="641c9-151">See Also</span></span>

[<span data-ttu-id="641c9-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="641c9-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="641c9-153">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="641c9-153">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="641c9-154">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="641c9-154">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="641c9-155">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="641c9-155">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="641c9-156">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="641c9-156">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="641c9-157">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="641c9-157">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)
