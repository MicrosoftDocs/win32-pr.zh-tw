---
description: 深入瞭解： JET_COLUMNLIST 結構
title: JET_COLUMNLIST 結構
TOCTitle: JET_COLUMNLIST Structure
ms:assetid: 3899676f-c96e-4f15-9089-4faea6808bc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269228(v=EXCHG.10)
ms:contentKeyID: 32765530
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
ms.openlocfilehash: 9bce36c818dd35408d95c770540ff4865bdf639b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973890"
---
# <a name="jet_columnlist-structure"></a><span data-ttu-id="51ce8-103">JET_COLUMNLIST 結構</span><span class="sxs-lookup"><span data-stu-id="51ce8-103">JET_COLUMNLIST Structure</span></span>


<span data-ttu-id="51ce8-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="51ce8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columnlist-structure"></a><span data-ttu-id="51ce8-105">JET_COLUMNLIST 結構</span><span class="sxs-lookup"><span data-stu-id="51ce8-105">JET_COLUMNLIST Structure</span></span>

<span data-ttu-id="51ce8-106">**JET_COLUMNLIST** 結構包含了遍歷 [JetGetColumnInfo](./jetgetcolumninfo-function.md)和 [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)函數所建立之臨時表所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="51ce8-106">The **JET_COLUMNLIST** structure contains the information necessary to traverse the temporary table that is created by the [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) functions.</span></span> <span data-ttu-id="51ce8-107">臨時表中的每個資料列都會描述 API 呼叫中所指定資料表中的資料行。</span><span class="sxs-lookup"><span data-stu-id="51ce8-107">Each row in the temporary table describes a column in the table given in the API call.</span></span> <span data-ttu-id="51ce8-108">此結構只搭配 [JetGetColumnInfo](./jetgetcolumninfo-function.md) 和 [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)使用。</span><span class="sxs-lookup"><span data-stu-id="51ce8-108">This structure is used with only with [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidPresentationOrder;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidcbMax;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidDefault;
      JET_COLUMNID columnidBaseTableName;
      JET_COLUMNID columnidBaseColumnName;
      JET_COLUMNID columnidDefinitionName;
    } JET_COLUMNLIST;
```

### <a name="members"></a><span data-ttu-id="51ce8-109">成員</span><span class="sxs-lookup"><span data-stu-id="51ce8-109">Members</span></span>

<span data-ttu-id="51ce8-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="51ce8-110">**cbStruct**</span></span>

<span data-ttu-id="51ce8-111">結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="51ce8-111">The size of the structure in bytes.</span></span> <span data-ttu-id="51ce8-112">API 呼叫會更新此欄位，因此呼叫端應確定此值符合 sizeof ( JET_COLUMNLIST ) 。</span><span class="sxs-lookup"><span data-stu-id="51ce8-112">The API call will update this field, so the caller should ensure that this value matches sizeof( JET_COLUMNLIST ).</span></span>

<span data-ttu-id="51ce8-113">**tableid**</span><span class="sxs-lookup"><span data-stu-id="51ce8-113">**tableid**</span></span>

<span data-ttu-id="51ce8-114">所建立之臨時表的資料表識別碼。</span><span class="sxs-lookup"><span data-stu-id="51ce8-114">The table identifier of the temporary table that was created.</span></span> <span data-ttu-id="51ce8-115">呼叫端必須負責關閉資料表。</span><span class="sxs-lookup"><span data-stu-id="51ce8-115">It is the responsibility of the caller to close the table.</span></span>

<span data-ttu-id="51ce8-116">**cRecord**</span><span class="sxs-lookup"><span data-stu-id="51ce8-116">**cRecord**</span></span>

<span data-ttu-id="51ce8-117">API 呼叫所建立之臨時表中的記錄數目。</span><span class="sxs-lookup"><span data-stu-id="51ce8-117">The number of records in the temporary table that was created by the API call.</span></span>

<span data-ttu-id="51ce8-118">**columnidPresentationOrder**</span><span class="sxs-lookup"><span data-stu-id="51ce8-118">**columnidPresentationOrder**</span></span>

<span data-ttu-id="51ce8-119">展示順序的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="51ce8-119">The column identifier of the presentation order.</span></span>

<span data-ttu-id="51ce8-120">展示順序是用來排序臨時表的資料列。</span><span class="sxs-lookup"><span data-stu-id="51ce8-120">The presentation order is used to sort the rows of the temporary table.</span></span> <span data-ttu-id="51ce8-121">展示順序是固定的 [JET_coltypLong](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="51ce8-121">The presentation order is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span> <span data-ttu-id="51ce8-122">如果指定的資訊層級不是精簡層級，則它也會標示為 JET_bitColumnTTKey。</span><span class="sxs-lookup"><span data-stu-id="51ce8-122">If the information level that was specified was not a compact level, then it is also marked as JET_bitColumnTTKey.</span></span>

<span data-ttu-id="51ce8-123">**columnidcolumnname**</span><span class="sxs-lookup"><span data-stu-id="51ce8-123">**columnidcolumnname**</span></span>

<span data-ttu-id="51ce8-124">資料行名稱的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="51ce8-124">The column identifier of the name of the column.</span></span>

<span data-ttu-id="51ce8-125">如果指定的資訊層級不是 compact，則它也會標示為 JET_bitColumnTTKey。</span><span class="sxs-lookup"><span data-stu-id="51ce8-125">If the information level specified was not compact, then it is also marked as JET_bitColumnTTKey.</span></span>

<span data-ttu-id="51ce8-126">**columnidcolumnid**</span><span class="sxs-lookup"><span data-stu-id="51ce8-126">**columnidcolumnid**</span></span>

<span data-ttu-id="51ce8-127">資料行識別碼的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="51ce8-127">The column identifier of the column identifier.</span></span>

<span data-ttu-id="51ce8-128">資料行識別碼是固定的 [JET_coltypLong](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="51ce8-128">The column identifier is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="51ce8-129">**columnidcoltyp**</span><span class="sxs-lookup"><span data-stu-id="51ce8-129">**columnidcoltyp**</span></span>

<span data-ttu-id="51ce8-130">資料行類型的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="51ce8-130">The column identifier of the column type.</span></span>

<span data-ttu-id="51ce8-131">資料行類型是固定的 [JET_coltypLong](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="51ce8-131">The column type is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="51ce8-132">**columnidCountry**</span><span class="sxs-lookup"><span data-stu-id="51ce8-132">**columnidCountry**</span></span>

<span data-ttu-id="51ce8-133">國家/地區代碼的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="51ce8-133">The column identifier of the country code.</span></span>

<span data-ttu-id="51ce8-134">國家/地區代碼是固定的 [JET_coltypShort](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="51ce8-134">The country code is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="51ce8-135">**columnidLangid**</span><span class="sxs-lookup"><span data-stu-id="51ce8-135">**columnidLangid**</span></span>

<span data-ttu-id="51ce8-136">語言識別項的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="51ce8-136">The column identifier of the language identifier.</span></span>

<span data-ttu-id="51ce8-137">語言識別項是固定的 [JET_coltypShort](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="51ce8-137">The language identifier is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="51ce8-138">**columnidCp**</span><span class="sxs-lookup"><span data-stu-id="51ce8-138">**columnidCp**</span></span>

<span data-ttu-id="51ce8-139">字碼頁的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="51ce8-139">The column identifier of the code page.</span></span>

<span data-ttu-id="51ce8-140">字碼頁是固定的 [JET_coltypShort](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="51ce8-140">The code page is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="51ce8-141">**columnidCollate**</span><span class="sxs-lookup"><span data-stu-id="51ce8-141">**columnidCollate**</span></span>

<span data-ttu-id="51ce8-142">定序順序的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="51ce8-142">The column identifier of the collation sequence.</span></span>

<span data-ttu-id="51ce8-143">定序順序是固定的 [JET_coltypShort](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="51ce8-143">The collation sequence is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="51ce8-144">**columnidcbMax**</span><span class="sxs-lookup"><span data-stu-id="51ce8-144">**columnidcbMax**</span></span>

<span data-ttu-id="51ce8-145">**CbMax** 欄位的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="51ce8-145">The column identifier of the **cbMax** field.</span></span>

<span data-ttu-id="51ce8-146">**CbMax** 是固定的 [JET_coltypLong](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="51ce8-146">The **cbMax** is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="51ce8-147">**columnidgrbit**</span><span class="sxs-lookup"><span data-stu-id="51ce8-147">**columnidgrbit**</span></span>

<span data-ttu-id="51ce8-148">資料行之 *grbits* 的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="51ce8-148">The column identifier of the *grbits* of the column.</span></span> <span data-ttu-id="51ce8-149">*Grbit* 欄位是固定的 [JET_coltypLong](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="51ce8-149">The *grbit* field is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span> <span data-ttu-id="51ce8-150">如需這些位的詳細資訊，請參閱 [JET_COLUMNDEF](./jet-columndef-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="51ce8-150">For more information about these bits, see [JET_COLUMNDEF](./jet-columndef-structure.md).</span></span>

<span data-ttu-id="51ce8-151">以下是 **columnidgrbit** 的可能值：</span><span class="sxs-lookup"><span data-stu-id="51ce8-151">The following are possible values for **columnidgrbit**:</span></span>

<span data-ttu-id="51ce8-152">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="51ce8-152">JET_bitColumnTagged</span></span>

<span data-ttu-id="51ce8-153">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="51ce8-153">JET_bitColumnFixed</span></span>

<span data-ttu-id="51ce8-154">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="51ce8-154">JET_bitColumnUpdatable</span></span>

<span data-ttu-id="51ce8-155">JET_bitColumnNotNull</span><span class="sxs-lookup"><span data-stu-id="51ce8-155">JET_bitColumnNotNULL</span></span>

<span data-ttu-id="51ce8-156">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="51ce8-156">JET_bitColumnAutoincrement</span></span>

<span data-ttu-id="51ce8-157">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="51ce8-157">JET_bitColumnVersion</span></span>

<span data-ttu-id="51ce8-158">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="51ce8-158">JET_bitColumnMultiValued</span></span>

<span data-ttu-id="51ce8-159">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="51ce8-159">JET_bitColumnEscrowUpdate</span></span>

<span data-ttu-id="51ce8-160">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="51ce8-160">JET_bitColumnFinalize</span></span>

<span data-ttu-id="51ce8-161">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="51ce8-161">JET_bitColumnDeleteOnZero</span></span>

<span data-ttu-id="51ce8-162">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="51ce8-162">JET_bitColumnUserDefinedDefault</span></span>

<span data-ttu-id="51ce8-163">**columnidDefault**</span><span class="sxs-lookup"><span data-stu-id="51ce8-163">**columnidDefault**</span></span>

<span data-ttu-id="51ce8-164">資料行預設值的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="51ce8-164">The column identifier of the default value of the column.</span></span>

<span data-ttu-id="51ce8-165">預設值為 [JET_coltypLongBinary](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="51ce8-165">The default value is a [JET_coltypLongBinary](./jet-coltyp.md).</span></span>

<span data-ttu-id="51ce8-166">**columnidBaseTableName**</span><span class="sxs-lookup"><span data-stu-id="51ce8-166">**columnidBaseTableName**</span></span>

<span data-ttu-id="51ce8-167">從中衍生資料表之資料表名稱的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="51ce8-167">The column identifier of the name of the table from which the table was derived.</span></span>

<span data-ttu-id="51ce8-168">資料表名稱是 [JET_coltypText](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="51ce8-168">The table name is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="51ce8-169">**columnidBaseColumnName**</span><span class="sxs-lookup"><span data-stu-id="51ce8-169">**columnidBaseColumnName**</span></span>

<span data-ttu-id="51ce8-170">從中衍生資料行之資料行名稱的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="51ce8-170">The column identifier of the name of the column from which the column was derived.</span></span>

<span data-ttu-id="51ce8-171">資料行名稱是 [JET_coltypText](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="51ce8-171">The column name is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="51ce8-172">**columnidDefinitionName**</span><span class="sxs-lookup"><span data-stu-id="51ce8-172">**columnidDefinitionName**</span></span>

<span data-ttu-id="51ce8-173">資料行定義的名稱資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="51ce8-173">The column identifier of the name of the column definition.</span></span>

<span data-ttu-id="51ce8-174">資料行定義名稱是 [JET_coltypText](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="51ce8-174">The column definition name is a [JET_coltypText](./jet-coltyp.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="51ce8-175">備註</span><span class="sxs-lookup"><span data-stu-id="51ce8-175">Remarks</span></span>

<span data-ttu-id="51ce8-176">依預設，臨時表中的資料列順序會依資料行的名稱排序。</span><span class="sxs-lookup"><span data-stu-id="51ce8-176">By default, the order of the rows in the temporary table is sorted by the name of the column.</span></span> <span data-ttu-id="51ce8-177">也可以依資料行識別碼進行排序。</span><span class="sxs-lookup"><span data-stu-id="51ce8-177">It can also be sorted by column identifier.</span></span> <span data-ttu-id="51ce8-178">如需如何依資料行識別碼排序的詳細資訊，請參閱 [JetGetColumnInfo](./jetgetcolumninfo-function.md) 和 [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)。</span><span class="sxs-lookup"><span data-stu-id="51ce8-178">For more information about how to sort by column identifier, see [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).</span></span>

<span data-ttu-id="51ce8-179">對 [JetGetColumnInfo](./jetgetcolumninfo-function.md) 或 [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) 的呼叫可能會指定精簡形式的結果。</span><span class="sxs-lookup"><span data-stu-id="51ce8-179">The call to [JetGetColumnInfo](./jetgetcolumninfo-function.md) or [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) might specify a compact form of results.</span></span> <span data-ttu-id="51ce8-180">如果有任何資料行已從範本資料表繼承，壓縮結果將不會儲存它們。</span><span class="sxs-lookup"><span data-stu-id="51ce8-180">If any columns have been inherited from a template table, the compact results will not store them.</span></span>

### <a name="requirements"></a><span data-ttu-id="51ce8-181">規格需求</span><span class="sxs-lookup"><span data-stu-id="51ce8-181">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51ce8-182"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="51ce8-182"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="51ce8-183">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="51ce8-183">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51ce8-184"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="51ce8-184"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="51ce8-185">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="51ce8-185">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51ce8-186"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="51ce8-186"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="51ce8-187">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="51ce8-187">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="51ce8-188">另請參閱</span><span class="sxs-lookup"><span data-stu-id="51ce8-188">See Also</span></span>

[<span data-ttu-id="51ce8-189">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="51ce8-189">JET_COLTYP</span></span>](./jet-coltyp.md)

[<span data-ttu-id="51ce8-190">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="51ce8-190">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)

[<span data-ttu-id="51ce8-191">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="51ce8-191">JET_COLUMNID</span></span>](./jet-columnid.md)

[<span data-ttu-id="51ce8-192">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="51ce8-192">JET_ERR</span></span>](./jet-err.md)

[<span data-ttu-id="51ce8-193">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="51ce8-193">JET_GRBIT</span></span>](./jet-grbit.md)

[<span data-ttu-id="51ce8-194">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="51ce8-194">JET_SESID</span></span>](./jet-sesid.md)

[<span data-ttu-id="51ce8-195">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="51ce8-195">JET_TABLEID</span></span>](./jet-tableid.md)

[<span data-ttu-id="51ce8-196">JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="51ce8-196">JetGetColumnInfo</span></span>](./jetgetcolumninfo-function.md)

[<span data-ttu-id="51ce8-197">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="51ce8-197">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)
