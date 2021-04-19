---
description: 深入瞭解： JetDeleteColumn2 函數
title: JetDeleteColumn2 函式
TOCTitle: JetDeleteColumn2 Function
ms:assetid: 840b5acd-8bbf-4524-9741-5d74e3427329
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269320(v=EXCHG.10)
ms:contentKeyID: 32765610
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumn2
- JetDeleteColumn2A
- JetDeleteColumn2W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 35e19eb7ac7b133bb690b268426fec9822efefea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981890"
---
# <a name="jetdeletecolumn2-function"></a><span data-ttu-id="68068-103">JetDeleteColumn2 函式</span><span class="sxs-lookup"><span data-stu-id="68068-103">JetDeleteColumn2 Function</span></span>


<span data-ttu-id="68068-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="68068-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeletecolumn2-function"></a><span data-ttu-id="68068-105">JetDeleteColumn2 函式</span><span class="sxs-lookup"><span data-stu-id="68068-105">JetDeleteColumn2 Function</span></span>

<span data-ttu-id="68068-106">**JetDeleteColumn2** 函式會從 ESE 資料庫資料表中刪除資料行，並啟用 *grbit* 選項的設定。</span><span class="sxs-lookup"><span data-stu-id="68068-106">The **JetDeleteColumn2** function deletes a column from an ESE database table and enables a *grbit* option to be set.</span></span>

<span data-ttu-id="68068-107">**Windows xp： JetDeleteColumn2** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="68068-107">**Windows XP:  JetDeleteColumn2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetDeleteColumn2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          const tchar* szColumnName,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="68068-108">參數</span><span class="sxs-lookup"><span data-stu-id="68068-108">Parameters</span></span>

<span data-ttu-id="68068-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="68068-109">*sesid*</span></span>

<span data-ttu-id="68068-110">要用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="68068-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="68068-111">*tableid*</span><span class="sxs-lookup"><span data-stu-id="68068-111">*tableid*</span></span>

<span data-ttu-id="68068-112">包含要刪除之資料行的資料表。</span><span class="sxs-lookup"><span data-stu-id="68068-112">The table that contains the column to be deleted.</span></span>

<span data-ttu-id="68068-113">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="68068-113">*szColumnName*</span></span>

<span data-ttu-id="68068-114">要刪除的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="68068-114">The name of the column to be deleted.</span></span>

<span data-ttu-id="68068-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="68068-115">*grbit*</span></span>

<span data-ttu-id="68068-116">指定零或多個下列選項的位群組。</span><span class="sxs-lookup"><span data-stu-id="68068-116">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="68068-117">值</span><span class="sxs-lookup"><span data-stu-id="68068-117">Value</span></span></p></th>
<th><p><span data-ttu-id="68068-118">意義</span><span class="sxs-lookup"><span data-stu-id="68068-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="68068-119">JET_bitDeleteColumnIgnoreTemplateColumns</span><span class="sxs-lookup"><span data-stu-id="68068-119">JET_bitDeleteColumnIgnoreTemplateColumns</span></span></p></td>
<td><p><span data-ttu-id="68068-120">設定 JET_bitDeleteColumIgnoreTemplateColumns 將導致 API 只會嘗試刪除衍生資料表中的資料行。</span><span class="sxs-lookup"><span data-stu-id="68068-120">Setting JET_bitDeleteColumIgnoreTemplateColumns will cause the API to only attempt to delete columns in the derived table.</span></span> <span data-ttu-id="68068-121">如果基表中有該名稱的資料行，則會忽略該名稱的資料行。</span><span class="sxs-lookup"><span data-stu-id="68068-121">If a column of that name exists in the base table it will be ignored.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="68068-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="68068-122">Return Value</span></span>

<span data-ttu-id="68068-123">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="68068-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="68068-124">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="68068-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="68068-125">傳回碼</span><span class="sxs-lookup"><span data-stu-id="68068-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="68068-126">Description</span><span class="sxs-lookup"><span data-stu-id="68068-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="68068-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="68068-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="68068-128">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="68068-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68068-129">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="68068-129">JET_errColumnInUse</span></span></p></td>
<td><p><span data-ttu-id="68068-130">資料行目前正在使用中。</span><span class="sxs-lookup"><span data-stu-id="68068-130">The column is currently in use.</span></span> <span data-ttu-id="68068-131">索引目前可能會使用它。</span><span class="sxs-lookup"><span data-stu-id="68068-131">It may be currently used by an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="68068-132">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="68068-132">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="68068-133">嘗試修改固定的 DDL。</span><span class="sxs-lookup"><span data-stu-id="68068-133">An attempt was made to modify the fixed DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68068-134">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="68068-134">JET_errFixedInheritedDDL</span></span></p></td>
<td><p><span data-ttu-id="68068-135">在 <em>szColumnName</em> 中名為的資料行存在於樣板資料表中，且無法修改範本資料表的 DDL。</span><span class="sxs-lookup"><span data-stu-id="68068-135">The column named in <em>szColumnName</em> exists in the template table, and the DDL of a template table cannot be modified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="68068-136">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="68068-136">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="68068-137">如果指定了 <em>szColumnName</em> 的錯誤名稱，則可能會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="68068-137">This may be returned if a bad name for <em>szColumnName</em> was given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68068-138">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="68068-138">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="68068-139">資料表無法寫入。</span><span class="sxs-lookup"><span data-stu-id="68068-139">The table is not writable.</span></span> <span data-ttu-id="68068-140">如果資料庫是以唯讀模式開啟，可能會傳回此情況。</span><span class="sxs-lookup"><span data-stu-id="68068-140">This may get returned if the database was opened in read-only mode.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="68068-141">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="68068-141">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="68068-142">交易是唯讀交易。</span><span class="sxs-lookup"><span data-stu-id="68068-142">The transaction is a read-only transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="68068-143">備註</span><span class="sxs-lookup"><span data-stu-id="68068-143">Remarks</span></span>

<span data-ttu-id="68068-144">呼叫 [JetDeleteColumn](./jetdeletecolumn-function.md) 等同于呼叫 **JetDeleteColumn2** ，並將 *grbit* 設定為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="68068-144">Calling [JetDeleteColumn](./jetdeletecolumn-function.md) is identical to calling **JetDeleteColumn2** with *grbit* set to zero (0).</span></span>

#### <a name="requirements"></a><span data-ttu-id="68068-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="68068-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="68068-146"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="68068-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="68068-147">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="68068-147">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68068-148"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="68068-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="68068-149">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="68068-149">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="68068-150"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="68068-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="68068-151">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="68068-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68068-152"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="68068-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="68068-153">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="68068-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="68068-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="68068-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="68068-155">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="68068-155">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68068-156"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="68068-156"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="68068-157">實作為 <strong>JetDeleteColumn2W</strong> (Unicode) 和 <strong>JetDeleteColumn2A</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="68068-157">Implemented as <strong>JetDeleteColumn2W</strong> (Unicode) and <strong>JetDeleteColumn2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="68068-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68068-158">See Also</span></span>

[<span data-ttu-id="68068-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="68068-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="68068-160">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="68068-160">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="68068-161">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="68068-161">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="68068-162">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="68068-162">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="68068-163">JetDeleteColumn</span><span class="sxs-lookup"><span data-stu-id="68068-163">JetDeleteColumn</span></span>](./jetdeletecolumn-function.md)
