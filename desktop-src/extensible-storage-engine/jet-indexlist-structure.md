---
description: 深入瞭解： JET_INDEXLIST 結構
title: JET_INDEXLIST 結構
TOCTitle: JET_INDEXLIST Structure
ms:assetid: 0c092b48-e583-49f3-8f5e-1428a84d9265
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269185(v=EXCHG.10)
ms:contentKeyID: 32765488
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
ms.openlocfilehash: a696d1c52a42cad2b3b67b047984b48d77637a1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319775"
---
# <a name="jet_indexlist-structure"></a><span data-ttu-id="7e2e3-103">JET_INDEXLIST 結構</span><span class="sxs-lookup"><span data-stu-id="7e2e3-103">JET_INDEXLIST Structure</span></span>


<span data-ttu-id="7e2e3-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7e2e3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_indexlist-structure"></a><span data-ttu-id="7e2e3-105">JET_INDEXLIST 結構</span><span class="sxs-lookup"><span data-stu-id="7e2e3-105">JET_INDEXLIST Structure</span></span>

<span data-ttu-id="7e2e3-106">**JET_INDEXLIST** 結構包含了 [JetGetIndexInfo](./jetgetindexinfo-function.md)或 [JetGetTableIndexInfo](./jetgettableindexinfo-function.md)函數所建立之臨時表的遍歷所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-106">The **JET_INDEXLIST** structure contains the necessary information to traverse a temporary table that is created by the [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) functions.</span></span> <span data-ttu-id="7e2e3-107">臨時表中的每個資料列都會描述索引的資料行。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-107">Each row in the temporary table describes a column of an index.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      gned long cRecord;
      JET_COLUMNID columnidindexname;
      JET_COLUMNID columnidgrbitIndex;
      JET_COLUMNID columnidcKey;
      JET_COLUMNID columnidcEntry;
      JET_COLUMNID columnidcPage;
      JET_COLUMNID columnidcColumn;
      JET_COLUMNID columnidiColumn;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidgrbitColumn;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidLCMapFlags;
    } JET_INDEXLIST;
```

### <a name="members"></a><span data-ttu-id="7e2e3-108">成員</span><span class="sxs-lookup"><span data-stu-id="7e2e3-108">Members</span></span>

<span data-ttu-id="7e2e3-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="7e2e3-109">**cbStruct**</span></span>

<span data-ttu-id="7e2e3-110">結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-110">The size of the structure in bytes.</span></span> <span data-ttu-id="7e2e3-111">API 呼叫會更新此欄位，因此呼叫端應確定此值符合 sizeof ( JET_INDEXLIST ) 。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-111">The API call will update this field, so the caller should ensure that this value matches sizeof( JET_INDEXLIST ).</span></span>

<span data-ttu-id="7e2e3-112">**tableid**</span><span class="sxs-lookup"><span data-stu-id="7e2e3-112">**tableid**</span></span>

<span data-ttu-id="7e2e3-113">所建立之臨時表的資料表識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-113">The table identifier of the temporary table that was created.</span></span> <span data-ttu-id="7e2e3-114">呼叫端必須負責關閉資料表。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-114">It is the responsibility of the caller to close the table.</span></span>

<span data-ttu-id="7e2e3-115">**cRecord**</span><span class="sxs-lookup"><span data-stu-id="7e2e3-115">**cRecord**</span></span>

<span data-ttu-id="7e2e3-116">已建立之臨時表中的記錄數目。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-116">The number of records in the temporary table that was created.</span></span>

<span data-ttu-id="7e2e3-117">**columnidindexname**</span><span class="sxs-lookup"><span data-stu-id="7e2e3-117">**columnidindexname**</span></span>

<span data-ttu-id="7e2e3-118">索引名稱的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-118">The column identifier of the name of the index.</span></span>

<span data-ttu-id="7e2e3-119">此資料行是 [JET_coltypText](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-119">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="7e2e3-120">**columnidgrbitIndex**</span><span class="sxs-lookup"><span data-stu-id="7e2e3-120">**columnidgrbitIndex**</span></span>

<span data-ttu-id="7e2e3-121">用於索引的 *grbits* 資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-121">The column identifier of the *grbits* used on the index.</span></span> <span data-ttu-id="7e2e3-122">如需有效位清單，請參閱 [JET_INDEXCREATE](./jet-indexcreate-structure.md) 。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-122">See [JET_INDEXCREATE](./jet-indexcreate-structure.md) for a list of valid bits.</span></span>

<span data-ttu-id="7e2e3-123">此資料行是 [JET_coltypLong](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-123">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="7e2e3-124">**columnidcKey**</span><span class="sxs-lookup"><span data-stu-id="7e2e3-124">**columnidcKey**</span></span>

<span data-ttu-id="7e2e3-125">索引中索引鍵數目的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-125">The column identifier of the number of keys in the index.</span></span>

<span data-ttu-id="7e2e3-126">此資料行是 [JET_coltypLong](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-126">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="7e2e3-127">**columnidcEntry**</span><span class="sxs-lookup"><span data-stu-id="7e2e3-127">**columnidcEntry**</span></span>

<span data-ttu-id="7e2e3-128">索引中專案數目的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-128">The column identifier of the number of entries in the index.</span></span>

<span data-ttu-id="7e2e3-129">此資料行是 [JET_coltypLong](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-129">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="7e2e3-130">**columnidcPage**</span><span class="sxs-lookup"><span data-stu-id="7e2e3-130">**columnidcPage**</span></span>

<span data-ttu-id="7e2e3-131">索引所使用之頁面數目的資料行識別碼。此資料行是 [JET_coltypLong](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-131">The column identifier of the number of pages the index uses.This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="7e2e3-132">**columnidcColumn**</span><span class="sxs-lookup"><span data-stu-id="7e2e3-132">**columnidcColumn**</span></span>

<span data-ttu-id="7e2e3-133">索引所跨越的資料行總數的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-133">The column identifier of the total number of columns that the index spans.</span></span>

<span data-ttu-id="7e2e3-134">此資料行是 [JET_coltypLong](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-134">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="7e2e3-135">**columnidiColumn**</span><span class="sxs-lookup"><span data-stu-id="7e2e3-135">**columnidiColumn**</span></span>

<span data-ttu-id="7e2e3-136">索引中資料行數目的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-136">The column identifier of the number of the columns in the index.</span></span> <span data-ttu-id="7e2e3-137">如需詳細資訊，請參閱本主題的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-137">For more information, see the Remarks section of this topic.</span></span>

<span data-ttu-id="7e2e3-138">此資料行是 [JET_coltypLong](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-138">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7e2e3-139">值</span><span class="sxs-lookup"><span data-stu-id="7e2e3-139">Value</span></span></p></th>
<th><p><span data-ttu-id="7e2e3-140">意義</span><span class="sxs-lookup"><span data-stu-id="7e2e3-140">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e2e3-141">cIndexInfoCols</span><span class="sxs-lookup"><span data-stu-id="7e2e3-141">cIndexInfoCols</span></span><br />
<span data-ttu-id="7e2e3-142">15</span><span class="sxs-lookup"><span data-stu-id="7e2e3-142">15</span></span></p></td>
<td><p><span data-ttu-id="7e2e3-143">指定允許15個數據行。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-143">Specifies that 15 columns are allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e2e3-144">cColumnInfoCols</span><span class="sxs-lookup"><span data-stu-id="7e2e3-144">cColumnInfoCols</span></span><br />
<span data-ttu-id="7e2e3-145">14</span><span class="sxs-lookup"><span data-stu-id="7e2e3-145">14</span></span></p></td>
<td><p><span data-ttu-id="7e2e3-146">指定允許14個數據行。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-146">Specifies that 14 columns are allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e2e3-147">cObjectInfoCols</span><span class="sxs-lookup"><span data-stu-id="7e2e3-147">cObjectInfoCols</span></span><br />
<span data-ttu-id="7e2e3-148">9</span><span class="sxs-lookup"><span data-stu-id="7e2e3-148">9</span></span></p></td>
<td><p><span data-ttu-id="7e2e3-149">指定允許9個數據行。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-149">Specifies that 9 columns are allowed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7e2e3-150">**columnidcolumnid**</span><span class="sxs-lookup"><span data-stu-id="7e2e3-150">**columnidcolumnid**</span></span>

<span data-ttu-id="7e2e3-151">已編制索引之資料行的資料行識別碼。如需詳細資訊，請參閱本主題的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-151">The column identifier of the column that is indexed.For more information, see the Remarks section of this topic.</span></span> <span data-ttu-id="7e2e3-152">此資料行是 [JET_coltypLong](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-152">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="7e2e3-153">**columnidcoltyp**</span><span class="sxs-lookup"><span data-stu-id="7e2e3-153">**columnidcoltyp**</span></span>

<span data-ttu-id="7e2e3-154">已編制索引之資料行的 coltyp 資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-154">The column identifier of the coltyp of the column which is indexed.</span></span> <span data-ttu-id="7e2e3-155">如需詳細資訊，請參閱本主題的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-155">For more information, see the Remarks section of this topic.</span></span> <span data-ttu-id="7e2e3-156">此資料行是 [JET_coltypLong](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-156">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="7e2e3-157">**columnidCountry**</span><span class="sxs-lookup"><span data-stu-id="7e2e3-157">**columnidCountry**</span></span>

<span data-ttu-id="7e2e3-158">已編制索引之資料行的國家/地區代碼資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-158">The column identifier of the country code of the column that is indexed.</span></span> <span data-ttu-id="7e2e3-159">國家/地區代碼已淘汰。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-159">The country code is deprecated.</span></span>

<span data-ttu-id="7e2e3-160">此資料行是 [JET_coltypShort](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-160">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="7e2e3-161">**columnidLangid**</span><span class="sxs-lookup"><span data-stu-id="7e2e3-161">**columnidLangid**</span></span>

<span data-ttu-id="7e2e3-162">用來建立索引的語言識別項 (LCID) 的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-162">The column identifier of the language identifier (LCID) under which the index was created.</span></span> <span data-ttu-id="7e2e3-163">如需詳細資訊，請參閱 [JET_INDEXCREATE](./jet-indexcreate-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-163">For more information, see [JET_INDEXCREATE](./jet-indexcreate-structure.md).</span></span>

<span data-ttu-id="7e2e3-164">此資料行是 [JET_coltypShort](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-164">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="7e2e3-165">**columnidCp**</span><span class="sxs-lookup"><span data-stu-id="7e2e3-165">**columnidCp**</span></span>

<span data-ttu-id="7e2e3-166">用來建立索引之字碼頁的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-166">The column identifier of the code page under which the index was created.</span></span> <span data-ttu-id="7e2e3-167">如需詳細資訊，請參閱 [JET_COLUMNCREATE](./jet-columncreate-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-167">For more information, see [JET_COLUMNCREATE](./jet-columncreate-structure.md).</span></span>

<span data-ttu-id="7e2e3-168">此資料行是 [JET_coltypShort](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-168">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="7e2e3-169">**columnidCollate**</span><span class="sxs-lookup"><span data-stu-id="7e2e3-169">**columnidCollate**</span></span>

<span data-ttu-id="7e2e3-170">建立索引時所依據之定序順序的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-170">The column identifier of the collation sequence under which the index was created.</span></span> <span data-ttu-id="7e2e3-171">定序順序已淘汰。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-171">The collation sequence is deprecated.</span></span>

<span data-ttu-id="7e2e3-172">此資料行是 [JET_coltypShort](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-172">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="7e2e3-173">**columnidgrbitColumn**</span><span class="sxs-lookup"><span data-stu-id="7e2e3-173">**columnidgrbitColumn**</span></span>

<span data-ttu-id="7e2e3-174">*Grbits* 的資料行識別碼，適用于索引中的資料行順序。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-174">The column identifier of the *grbits* that apply to the order of the column in the index.</span></span>

<span data-ttu-id="7e2e3-175">此資料行的資料可以 JET_bitKeyAscending 或 JET_bitKeyDescending 排序。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-175">The data for this column can be ordered as JET_bitKeyAscending or JET_bitKeyDescending.</span></span> <span data-ttu-id="7e2e3-176">此資料行是 [JET_coltypLong](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-176">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span> <span data-ttu-id="7e2e3-177">例如，定義為 "-column1 \\ 0 + column2 \\ 0" 的索引將會有 "column1" 的 JET_bitKeyDescending，而 "column2" 的 JET_bitKeyAscending。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-177">For example, an index defined as "-column1\\0+column2\\0" will have JET_bitKeyDescending for "column1", and JET_bitKeyAscending for "column2".</span></span>

<span data-ttu-id="7e2e3-178">下列選項對此成員有效。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-178">The following options are valid for this member.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7e2e3-179">值</span><span class="sxs-lookup"><span data-stu-id="7e2e3-179">Value</span></span></p></th>
<th><p><span data-ttu-id="7e2e3-180">意義</span><span class="sxs-lookup"><span data-stu-id="7e2e3-180">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e2e3-181">JET_bitKeyAscending</span><span class="sxs-lookup"><span data-stu-id="7e2e3-181">JET_bitKeyAscending</span></span></p></td>
<td><p><span data-ttu-id="7e2e3-182">以遞增順序的索引區段。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-182">An index segment in ascending order.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e2e3-183">JET_bitKeyDescending</span><span class="sxs-lookup"><span data-stu-id="7e2e3-183">JET_bitKeyDescending</span></span></p></td>
<td><p><span data-ttu-id="7e2e3-184">以遞減順序排序的索引區段。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-184">An index segment in descending order.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7e2e3-185">**columnidcolumnname**</span><span class="sxs-lookup"><span data-stu-id="7e2e3-185">**columnidcolumnname**</span></span>

<span data-ttu-id="7e2e3-186">資料行名稱的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-186">The column identifier of the name of the column.</span></span>

<span data-ttu-id="7e2e3-187">此資料行是 [JET_coltypText](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-187">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="7e2e3-188">**columnidLCMapFlags**</span><span class="sxs-lookup"><span data-stu-id="7e2e3-188">**columnidLCMapFlags**</span></span>

<span data-ttu-id="7e2e3-189">用來建立索引之旗標的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-189">The column identifier of the flags that are used to create the index.</span></span> <span data-ttu-id="7e2e3-190">如需詳細資訊，請參閱 [JET_UNICODEINDEX](./jet-unicodeindex-structure.md)的 **dwMapFlags** 一節。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-190">For more information, see the **dwMapFlags** section of [JET_UNICODEINDEX](./jet-unicodeindex-structure.md).</span></span>

<span data-ttu-id="7e2e3-191">此資料行是 [JET_coltypLong](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-191">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="7e2e3-192">備註</span><span class="sxs-lookup"><span data-stu-id="7e2e3-192">Remarks</span></span>

<span data-ttu-id="7e2e3-193">臨時表中的每個資料列都會對應至特定索引中的資料行。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-193">Each row in the temporary table corresponds to a column in a particular index.</span></span>

<span data-ttu-id="7e2e3-194">例如，索引 "+ A \\ 0 + B \\ 0 + C \\ 0 + D \\ 0 + E \\ 0" 為五個以上的資料行，而且會佔用臨時表中的五個數據列。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-194">For example, the index "+A\\0+B\\0+C\\0+D\\0+E\\0" is more than five columns, and it will occupy five rows in the temporary table.</span></span> <span data-ttu-id="7e2e3-195">在 columnid 資料行所識別的資料行中，這五個數據列的值都是5。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-195">Each of these five rows will have a value of 5 in the column that is identified by columnid column.</span></span> <span data-ttu-id="7e2e3-196">但是，每個資料列會有不同的 columnid 資料行值，範圍介於0到4之間。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-196">But each row will have a different value for columnid column, ranging from 0 to 4.</span></span>

<span data-ttu-id="7e2e3-197">特定索引中的索引鍵數目，會對應至呼叫端可以搜尋並取得完全相符的唯一值數目。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-197">The number of keys in a particular index corresponds to the number of unique values for which a caller can seek and get an exact match.</span></span> <span data-ttu-id="7e2e3-198">專案數目是索引符合的資料列數目。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-198">The number of entries is the number of rows that an index matches.</span></span> <span data-ttu-id="7e2e3-199">如果索引具有唯一性條件約束，則索引鍵的數目等於專案的數目。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-199">If an index has a uniqueness constraint, then the number of keys is equal to the number of entries.</span></span> <span data-ttu-id="7e2e3-200">例如，如果資料表包含下列資訊，並且在名為 "key" 的資料行上建立索引，則會有三個索引鍵 (100、200和 500) ，但有四個專案 ( "this"、"是"、"a" 和 "example" ) 。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-200">For example, if a table contains the following information and an index is created over the column named "key", then there are three keys (100, 200, and 500), but there are four entries ("this", "is", "an", and "example").</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7e2e3-201">答案</span><span class="sxs-lookup"><span data-stu-id="7e2e3-201">Key</span></span></p></th>
<th><p><span data-ttu-id="7e2e3-202">進入</span><span class="sxs-lookup"><span data-stu-id="7e2e3-202">Entry</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e2e3-203">100</span><span class="sxs-lookup"><span data-stu-id="7e2e3-203">100</span></span></p></td>
<td><p><span data-ttu-id="7e2e3-204">&quot;this&quot;</span><span class="sxs-lookup"><span data-stu-id="7e2e3-204">&quot;this&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e2e3-205">100</span><span class="sxs-lookup"><span data-stu-id="7e2e3-205">100</span></span></p></td>
<td><p><span data-ttu-id="7e2e3-206">&quot;is&quot;</span><span class="sxs-lookup"><span data-stu-id="7e2e3-206">&quot;is&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e2e3-207">200</span><span class="sxs-lookup"><span data-stu-id="7e2e3-207">200</span></span></p></td>
<td><p><span data-ttu-id="7e2e3-208">&quot;以&quot;</span><span class="sxs-lookup"><span data-stu-id="7e2e3-208">&quot;an&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e2e3-209">500</span><span class="sxs-lookup"><span data-stu-id="7e2e3-209">500</span></span></p></td>
<td><p><span data-ttu-id="7e2e3-210">&quot;example&quot;</span><span class="sxs-lookup"><span data-stu-id="7e2e3-210">&quot;example&quot;</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="7e2e3-211">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e2e3-211">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e2e3-212"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="7e2e3-212"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7e2e3-213">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-213">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e2e3-214"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="7e2e3-214"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7e2e3-215">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-215">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e2e3-216"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="7e2e3-216"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7e2e3-217">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="7e2e3-217">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="7e2e3-218">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e2e3-218">See Also</span></span>

[<span data-ttu-id="7e2e3-219">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="7e2e3-219">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="7e2e3-220">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="7e2e3-220">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="7e2e3-221">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="7e2e3-221">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="7e2e3-222">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7e2e3-222">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7e2e3-223">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="7e2e3-223">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="7e2e3-224">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="7e2e3-224">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="7e2e3-225">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="7e2e3-225">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="7e2e3-226">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="7e2e3-226">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="7e2e3-227">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="7e2e3-227">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="7e2e3-228">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="7e2e3-228">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="7e2e3-229">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="7e2e3-229">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)
