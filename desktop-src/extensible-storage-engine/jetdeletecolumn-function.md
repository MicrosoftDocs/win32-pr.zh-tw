---
description: 深入瞭解： JetDeleteColumn 函數
title: JetDeleteColumn 函式
TOCTitle: JetDeleteColumn Function
ms:assetid: b2f4be8c-7ea9-4f66-925b-4e9c14d9d475
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294062(v=EXCHG.10)
ms:contentKeyID: 32765677
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumnA
- JetDeleteColumnW
- JetDeleteColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d7d577447942e36cd49763727473d3f6ddc659b4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "103946273"
---
# <a name="jetdeletecolumn-function"></a><span data-ttu-id="671cc-103">JetDeleteColumn 函式</span><span class="sxs-lookup"><span data-stu-id="671cc-103">JetDeleteColumn Function</span></span>


<span data-ttu-id="671cc-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="671cc-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeletecolumn-function"></a><span data-ttu-id="671cc-105">JetDeleteColumn 函式</span><span class="sxs-lookup"><span data-stu-id="671cc-105">JetDeleteColumn Function</span></span>

<span data-ttu-id="671cc-106">**JetDeleteColumn** 函數會從 ESE 資料庫資料表中刪除資料行。</span><span class="sxs-lookup"><span data-stu-id="671cc-106">The **JetDeleteColumn** function deletes a column from an ESE database table.</span></span>

```cpp
JET_ERR JET_API JetDeleteColumn(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName
);
```

### <a name="parameters"></a><span data-ttu-id="671cc-107">參數</span><span class="sxs-lookup"><span data-stu-id="671cc-107">Parameters</span></span>

<span data-ttu-id="671cc-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="671cc-108">*sesid*</span></span>

<span data-ttu-id="671cc-109">要用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="671cc-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="671cc-110">*tableid*</span><span class="sxs-lookup"><span data-stu-id="671cc-110">*tableid*</span></span>

<span data-ttu-id="671cc-111">要從中刪除資料行的資料表。</span><span class="sxs-lookup"><span data-stu-id="671cc-111">The table from which to delete the column.</span></span>

<span data-ttu-id="671cc-112">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="671cc-112">*szColumnName*</span></span>

<span data-ttu-id="671cc-113">要刪除的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="671cc-113">The name of the column to be deleted.</span></span>

### <a name="return-value"></a><span data-ttu-id="671cc-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="671cc-114">Return Value</span></span>

<span data-ttu-id="671cc-115">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="671cc-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="671cc-116">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="671cc-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="671cc-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="671cc-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="671cc-118">Description</span><span class="sxs-lookup"><span data-stu-id="671cc-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="671cc-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="671cc-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="671cc-120">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="671cc-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="671cc-121">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="671cc-121">JET_errColumnInUse</span></span></p></td>
<td><p><span data-ttu-id="671cc-122">資料行目前正在使用中。</span><span class="sxs-lookup"><span data-stu-id="671cc-122">The column is currently in use.</span></span> <span data-ttu-id="671cc-123">索引目前可能會使用它。</span><span class="sxs-lookup"><span data-stu-id="671cc-123">It may be currently used by an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="671cc-124">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="671cc-124">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="671cc-125">嘗試修改固定的 DDL。</span><span class="sxs-lookup"><span data-stu-id="671cc-125">An attempt was made to modify the fixed DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="671cc-126">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="671cc-126">JET_errFixedInheritedDDL</span></span></p></td>
<td><p><span data-ttu-id="671cc-127">在 <em>szColumnName</em> 中名為的資料行存在於樣板資料表中，且無法修改範本資料表的 DDL。</span><span class="sxs-lookup"><span data-stu-id="671cc-127">The column named in <em>szColumnName</em> exists in the template table, and the DDL of a template table cannot be modified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="671cc-128">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="671cc-128">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="671cc-129">如果指定了 <em>szColumnName</em> 的錯誤名稱，則可能會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="671cc-129">This may be returned if a bad name for <em>szColumnName</em> was given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="671cc-130">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="671cc-130">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="671cc-131">資料表無法寫入。</span><span class="sxs-lookup"><span data-stu-id="671cc-131">The table is not writable.</span></span> <span data-ttu-id="671cc-132">如果資料庫是以唯讀模式開啟，可能會傳回此情況。</span><span class="sxs-lookup"><span data-stu-id="671cc-132">This may get returned if the database was opened in read-only mode.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="671cc-133">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="671cc-133">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="671cc-134">交易是唯讀交易。</span><span class="sxs-lookup"><span data-stu-id="671cc-134">The transaction is a read-only transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="671cc-135">備註</span><span class="sxs-lookup"><span data-stu-id="671cc-135">Remarks</span></span>

<span data-ttu-id="671cc-136">呼叫 **JetDeleteColumn** 等同于呼叫 [JetDeleteColumn2](./jetdeletecolumn2-function.md) ，並將 *grbit* 設定為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="671cc-136">Calling **JetDeleteColumn** is identical to calling [JetDeleteColumn2](./jetdeletecolumn2-function.md) with *grbit* set to zero (0).</span></span>

#### <a name="requirements"></a><span data-ttu-id="671cc-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="671cc-137">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="671cc-138"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="671cc-138"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="671cc-139">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="671cc-139">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="671cc-140"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="671cc-140"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="671cc-141">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="671cc-141">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="671cc-142"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="671cc-142"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="671cc-143">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="671cc-143">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="671cc-144"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="671cc-144"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="671cc-145">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="671cc-145">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="671cc-146"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="671cc-146"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="671cc-147">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="671cc-147">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="671cc-148"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="671cc-148"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="671cc-149">實作為 <strong>JetDeleteColumnW</strong> (Unicode) 和 <strong>JetDeleteColumnA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="671cc-149">Implemented as <strong>JetDeleteColumnW</strong> (Unicode) and <strong>JetDeleteColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="671cc-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="671cc-150">See Also</span></span>

[<span data-ttu-id="671cc-151">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="671cc-151">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="671cc-152">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="671cc-152">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="671cc-153">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="671cc-153">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="671cc-154">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="671cc-154">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="671cc-155">JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="671cc-155">JetDeleteColumn2</span></span>](./jetdeletecolumn2-function.md)
