---
description: 深入瞭解： JET_OBJECTINFO 結構
title: JET_OBJECTINFO 結構
TOCTitle: JET_OBJECTINFO Structure
ms:assetid: 9d348ab3-d453-4316-9233-681f165e8ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269353(v=EXCHG.10)
ms:contentKeyID: 32765640
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd1f8a876153b5b457cfb153cbf35fa2d388b0f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027147"
---
# <a name="jet_objectinfo-structure"></a><span data-ttu-id="a81ed-103">JET_OBJECTINFO 結構</span><span class="sxs-lookup"><span data-stu-id="a81ed-103">JET_OBJECTINFO Structure</span></span>


<span data-ttu-id="a81ed-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a81ed-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_objectinfo-structure"></a><span data-ttu-id="a81ed-105">JET_OBJECTINFO 結構</span><span class="sxs-lookup"><span data-stu-id="a81ed-105">JET_OBJECTINFO Structure</span></span>

<span data-ttu-id="a81ed-106">**JET_OBJECTINFO** 結構會保存物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a81ed-106">The **JET_OBJECTINFO** structure holds information about an object.</span></span> <span data-ttu-id="a81ed-107">資料表是目前唯一支援的物件類型。</span><span class="sxs-lookup"><span data-stu-id="a81ed-107">Tables are the only object types that are currently supported.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_OBJTYP objtyp;
      JET_DATESERIAL dtCreate;
      JET_DATESERIAL dtUpdate;
      JET_GRBIT grbit;
      unsigned long flags;
      unsigned long cRecord;
      unsigned long cPage;
    } JET_OBJECTINFO;
```

### <a name="members"></a><span data-ttu-id="a81ed-108">成員</span><span class="sxs-lookup"><span data-stu-id="a81ed-108">Members</span></span>

<span data-ttu-id="a81ed-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="a81ed-109">**cbStruct**</span></span>

<span data-ttu-id="a81ed-110">**JET_OBJECTINFO** 結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a81ed-110">The size, in bytes, of the **JET_OBJECTINFO** structure.</span></span>

<span data-ttu-id="a81ed-111">**objtyp**</span><span class="sxs-lookup"><span data-stu-id="a81ed-111">**objtyp**</span></span>

<span data-ttu-id="a81ed-112">保存結構的 [JET_OBJTYP](./jet-objtyp.md) 。</span><span class="sxs-lookup"><span data-stu-id="a81ed-112">Holds the [JET_OBJTYP](./jet-objtyp.md) of the structure.</span></span> <span data-ttu-id="a81ed-113">目前只有資料表會傳回 (也就是 JET_objtypTable) 。</span><span class="sxs-lookup"><span data-stu-id="a81ed-113">Currently only tables will be returned (that is, JET_objtypTable).</span></span>

<span data-ttu-id="a81ed-114">**dtCreate**</span><span class="sxs-lookup"><span data-stu-id="a81ed-114">**dtCreate**</span></span>

<span data-ttu-id="a81ed-115">已過時。</span><span class="sxs-lookup"><span data-stu-id="a81ed-115">Obsolete.</span></span> <span data-ttu-id="a81ed-116">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="a81ed-116">Do not use.</span></span>

<span data-ttu-id="a81ed-117">**dtUpdate**</span><span class="sxs-lookup"><span data-stu-id="a81ed-117">**dtUpdate**</span></span>

<span data-ttu-id="a81ed-118">已過時。</span><span class="sxs-lookup"><span data-stu-id="a81ed-118">Obsolete.</span></span> <span data-ttu-id="a81ed-119">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="a81ed-119">Do not use.</span></span>

<span data-ttu-id="a81ed-120">**grbit**</span><span class="sxs-lookup"><span data-stu-id="a81ed-120">**grbit**</span></span>

<span data-ttu-id="a81ed-121">位群組，其中包含可用於此呼叫的選項，包括下列零或多個。</span><span class="sxs-lookup"><span data-stu-id="a81ed-121">A group of bits that contain the options that are available for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a81ed-122">值</span><span class="sxs-lookup"><span data-stu-id="a81ed-122">Value</span></span></p></th>
<th><p><span data-ttu-id="a81ed-123">意義</span><span class="sxs-lookup"><span data-stu-id="a81ed-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a81ed-124">JET_bitTableInfoBookmark</span><span class="sxs-lookup"><span data-stu-id="a81ed-124">JET_bitTableInfoBookmark</span></span></p></td>
<td><p><span data-ttu-id="a81ed-125">資料表可以有書簽。</span><span class="sxs-lookup"><span data-stu-id="a81ed-125">The table can have bookmarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a81ed-126">JET_bitTableInfoRollback</span><span class="sxs-lookup"><span data-stu-id="a81ed-126">JET_bitTableInfoRollback</span></span></p></td>
<td><p><span data-ttu-id="a81ed-127">資料表可以復原。</span><span class="sxs-lookup"><span data-stu-id="a81ed-127">The table can be rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a81ed-128">JET_bitTableInfoUpdatable</span><span class="sxs-lookup"><span data-stu-id="a81ed-128">JET_bitTableInfoUpdatable</span></span></p></td>
<td><p><span data-ttu-id="a81ed-129">您可以更新資料表。</span><span class="sxs-lookup"><span data-stu-id="a81ed-129">The table can be updated.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a81ed-130">**flags**</span><span class="sxs-lookup"><span data-stu-id="a81ed-130">**flags**</span></span>

<span data-ttu-id="a81ed-131">包含零或多個下列旗標的位欄位。</span><span class="sxs-lookup"><span data-stu-id="a81ed-131">A bit field that contains zero or more of the following flags.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a81ed-132">值</span><span class="sxs-lookup"><span data-stu-id="a81ed-132">Value</span></span></p></th>
<th><p><span data-ttu-id="a81ed-133">意義</span><span class="sxs-lookup"><span data-stu-id="a81ed-133">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a81ed-134">JET_bitObjectSystem</span><span class="sxs-lookup"><span data-stu-id="a81ed-134">JET_bitObjectSystem</span></span></p></td>
<td><p><span data-ttu-id="a81ed-135">資料表是系統資料表，僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="a81ed-135">The table is a System Table and is for internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a81ed-136">JET_bitObjectTableDerived</span><span class="sxs-lookup"><span data-stu-id="a81ed-136">JET_bitObjectTableDerived</span></span></p></td>
<td><p><span data-ttu-id="a81ed-137">資料表繼承自範本資料表的 DDL。</span><span class="sxs-lookup"><span data-stu-id="a81ed-137">The table inherited DDL from a template table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a81ed-138">JET_bitObjectTableFixedDDL</span><span class="sxs-lookup"><span data-stu-id="a81ed-138">JET_bitObjectTableFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="a81ed-139">無法修改資料表的 DDL。</span><span class="sxs-lookup"><span data-stu-id="a81ed-139">The DDL for the table cannot be modified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a81ed-140">JET_bitObjectTableNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="a81ed-140">JET_bitObjectTableNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="a81ed-141">搭配 JET_bitObjectTableTemplate 使用，以不允許衍生資料表中的固定或變數資料行 (因此，在未來的) 中，可以將固定或變數資料行新增至範本。</span><span class="sxs-lookup"><span data-stu-id="a81ed-141">Used in conjunction with JET_bitObjectTableTemplate to disallow fixed or variable columns in derived tables (so that fixed or variable columns can be added to the template in the future).</span></span></p>
<p><span data-ttu-id="a81ed-142"><strong>WINDOWS XP：  </strong>此值是在 Windows XP 中引進。</span><span class="sxs-lookup"><span data-stu-id="a81ed-142"><strong>Windows XP:  </strong>This value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a81ed-143">JET_bitObjectTableTemplate</span><span class="sxs-lookup"><span data-stu-id="a81ed-143">JET_bitObjectTableTemplate</span></span></p></td>
<td><p><span data-ttu-id="a81ed-144">資料表是範本資料表。</span><span class="sxs-lookup"><span data-stu-id="a81ed-144">The table is a template table.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a81ed-145">**cRecord**</span><span class="sxs-lookup"><span data-stu-id="a81ed-145">**cRecord**</span></span>

<span data-ttu-id="a81ed-146">資料表中的記錄數目。</span><span class="sxs-lookup"><span data-stu-id="a81ed-146">The number of records in the table.</span></span>

<span data-ttu-id="a81ed-147">只有當 **JET_OBJECTINFO** 已傳遞至 [JetGetObjectInfo](./jetgetobjectinfo-function.md)時，才會抓取此值。</span><span class="sxs-lookup"><span data-stu-id="a81ed-147">This value is retrieved only if **JET_OBJECTINFO** was passed to [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span></span>

<span data-ttu-id="a81ed-148">**cPage**</span><span class="sxs-lookup"><span data-stu-id="a81ed-148">**cPage**</span></span>

<span data-ttu-id="a81ed-149">資料表正在使用的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="a81ed-149">The number of pages that are being used by the table.</span></span>

<span data-ttu-id="a81ed-150">只有當 **JET_OBJECTINFO** 已傳遞至 [JetGetObjectInfo](./jetgetobjectinfo-function.md)時，才會抓取此值。</span><span class="sxs-lookup"><span data-stu-id="a81ed-150">This value is retrieved only if **JET_OBJECTINFO** was passed to [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="a81ed-151">備註</span><span class="sxs-lookup"><span data-stu-id="a81ed-151">Remarks</span></span>

<span data-ttu-id="a81ed-152">[JetGetObjectInfo](./jetgetobjectinfo-function.md)或 [JetGetTableInfo](./jetgettableinfo-function.md)的呼叫會填入 **JET_OBJECTINFO** 結構。</span><span class="sxs-lookup"><span data-stu-id="a81ed-152">A **JET_OBJECTINFO** structure gets populated by a call to [JetGetObjectInfo](./jetgetobjectinfo-function.md) or [JetGetTableInfo](./jetgettableinfo-function.md).</span></span> <span data-ttu-id="a81ed-153">如果 API 呼叫不成功，則結構的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="a81ed-153">If the API call does not succeed, the contents of the structure are undefined.</span></span>

<span data-ttu-id="a81ed-154">如果適用的話，資料表統計資料會包含記錄的數目以及叢集索引中的頁面數目 (也就是包含記錄資料) 的索引。</span><span class="sxs-lookup"><span data-stu-id="a81ed-154">If applicable, the table statistics include the number of records and the number of pages that are in the clustered index (that is, the index containing the record data).</span></span> <span data-ttu-id="a81ed-155">索引統計資料是使用 [JetGetIndexInfo](./jetgetindexinfo-function.md) 或 [JetGetTableIndexInfo](./jetgettableindexinfo-function.md)，依名稱個別存取。</span><span class="sxs-lookup"><span data-stu-id="a81ed-155">The index statistics are accessed separately by name, using [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="a81ed-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="a81ed-156">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a81ed-157"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="a81ed-157"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a81ed-158">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="a81ed-158">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a81ed-159"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="a81ed-159"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a81ed-160">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="a81ed-160">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a81ed-161"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="a81ed-161"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a81ed-162">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="a81ed-162">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="a81ed-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a81ed-163">See Also</span></span>

[<span data-ttu-id="a81ed-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a81ed-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a81ed-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="a81ed-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="a81ed-166">JET_OBJTYP</span><span class="sxs-lookup"><span data-stu-id="a81ed-166">JET_OBJTYP</span></span>](./jet-objtyp.md)  
[<span data-ttu-id="a81ed-167">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a81ed-167">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a81ed-168">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="a81ed-168">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="a81ed-169">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="a81ed-169">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="a81ed-170">JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="a81ed-170">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)  
[<span data-ttu-id="a81ed-171">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="a81ed-171">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="a81ed-172">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="a81ed-172">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)
