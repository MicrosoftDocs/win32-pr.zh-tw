---
description: 深入瞭解： JET_TABLECREATE 結構
title: JET_TABLECREATE 結構
TOCTitle: JET_TABLECREATE Structure
ms:assetid: ff06325c-d61e-4239-b2d4-868f557f5f76
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294146(v=EXCHG.10)
ms:contentKeyID: 32765760
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
ms.openlocfilehash: f96b73daaf446023a7fe3a5729dcb1c90b5f14e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112068"
---
# <a name="jet_tablecreate-structure"></a><span data-ttu-id="8eafb-103">JET_TABLECREATE 結構</span><span class="sxs-lookup"><span data-stu-id="8eafb-103">JET_TABLECREATE Structure</span></span>


<span data-ttu-id="8eafb-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8eafb-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tablecreate-structure"></a><span data-ttu-id="8eafb-105">JET_TABLECREATE 結構</span><span class="sxs-lookup"><span data-stu-id="8eafb-105">JET_TABLECREATE Structure</span></span>

<span data-ttu-id="8eafb-106">**JET_TABLECREATE** 結構所包含的資訊，必須用來建立在 ESE 資料庫中填入資料行和索引的資料表。</span><span class="sxs-lookup"><span data-stu-id="8eafb-106">The **JET_TABLECREATE** structure contains the information that is necessary to create a table populated with columns and indexes in an ESE database.</span></span> <span data-ttu-id="8eafb-107">[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)會使用 **JET_TABLECREATE** 結構。</span><span class="sxs-lookup"><span data-stu-id="8eafb-107">The **JET_TABLECREATE** structure is used by [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)</span></span>

```cpp
    typedef struct tagJET_TABLECREATE {
      unsigned long cbStruct;
      tchar* szTableName;
      tchar* szTemplateTableName;
      unsigned long ulPages;
      unsigned long ulDensity;
      JET_COLUMNCREATE* rgcolumncreate;
      unsigned long cColumns;
      JET_INDEXCREATE* rgindexcreate;
      unsigned long cIndexes;
      JET_GRBIT grbit;
      JET_TABLEID tableid;
      unsigned long cCreated;
    } JET_TABLECREATE;
```

### <a name="members"></a><span data-ttu-id="8eafb-108">成員</span><span class="sxs-lookup"><span data-stu-id="8eafb-108">Members</span></span>

<span data-ttu-id="8eafb-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="8eafb-109">**cbStruct**</span></span>

<span data-ttu-id="8eafb-110">此結構的大小，以位元組為單位， (未來的擴充) 。</span><span class="sxs-lookup"><span data-stu-id="8eafb-110">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="8eafb-111">它必須設定為 sizeof ( JET_TABLECREATE ) （以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="8eafb-111">It must be set to sizeof( JET_TABLECREATE ) in bytes.</span></span>

<span data-ttu-id="8eafb-112">**szTableName**</span><span class="sxs-lookup"><span data-stu-id="8eafb-112">**szTableName**</span></span>

<span data-ttu-id="8eafb-113">要建立之資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="8eafb-113">The name of the table to create.</span></span>

<span data-ttu-id="8eafb-114">名稱必須使用符合下列條件：</span><span class="sxs-lookup"><span data-stu-id="8eafb-114">The name must use meet the following conditions:</span></span>

  - <span data-ttu-id="8eafb-115">值小於 JET_cbNameMost，不包括終止的 Null。</span><span class="sxs-lookup"><span data-stu-id="8eafb-115">Have a value less than JET_cbNameMost, not including the terminating NULL.</span></span>

<!-- end list -->

  - <span data-ttu-id="8eafb-116">包含下列一組字元：0到9、A 到 Z、a 到 z，以及除了驚嘆號以外的所有其他標點符號 (\!) 、逗點 (、) 、左括弧 (\[) 和右括弧 () \] ，也就是 ASCII 字元0x20、0x22 至0x2d、0x2f 至0x5a、0x5c 和0x5d 至0x7f。</span><span class="sxs-lookup"><span data-stu-id="8eafb-116">Consist of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]), that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

<!-- end list -->

  - <span data-ttu-id="8eafb-117">不是以空格開頭。</span><span class="sxs-lookup"><span data-stu-id="8eafb-117">Not begin with a space.</span></span>

<!-- end list -->

  - <span data-ttu-id="8eafb-118">至少包含一個非空白字元。</span><span class="sxs-lookup"><span data-stu-id="8eafb-118">Consist of at least one non-space character.</span></span>

<span data-ttu-id="8eafb-119">**szTemplateTableName**</span><span class="sxs-lookup"><span data-stu-id="8eafb-119">**szTemplateTableName**</span></span>

<span data-ttu-id="8eafb-120">現有資料表的名稱，要從此資料表繼承基底 DDL (資料定義語言) 。</span><span class="sxs-lookup"><span data-stu-id="8eafb-120">The name of an already-existing table from which to inherit base DDL (Data Definition Language).</span></span> <span data-ttu-id="8eafb-121">使用範本資料表可讓您輕鬆地建立具有相同資料行和索引的多個資料表。</span><span class="sxs-lookup"><span data-stu-id="8eafb-121">Use of a template table allows for the easy creation of many tables with identical columns and indexes.</span></span>

<span data-ttu-id="8eafb-122">**ulPages**</span><span class="sxs-lookup"><span data-stu-id="8eafb-122">**ulPages**</span></span>

<span data-ttu-id="8eafb-123">要配置給資料表的初始資料庫頁面數目。</span><span class="sxs-lookup"><span data-stu-id="8eafb-123">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="8eafb-124">如果有多個資料列插入此資料表中，指定大於1的數位可以減少片段。</span><span class="sxs-lookup"><span data-stu-id="8eafb-124">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="8eafb-125">**ulDensity**</span><span class="sxs-lookup"><span data-stu-id="8eafb-125">**ulDensity**</span></span>

<span data-ttu-id="8eafb-126">資料表密度（以百分比為單位）。</span><span class="sxs-lookup"><span data-stu-id="8eafb-126">The table density, in percentage points.</span></span> <span data-ttu-id="8eafb-127">此數位必須是0或20到100的範圍。</span><span class="sxs-lookup"><span data-stu-id="8eafb-127">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="8eafb-128">傳遞0表示應該使用預設值。</span><span class="sxs-lookup"><span data-stu-id="8eafb-128">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="8eafb-129">預設值為80。</span><span class="sxs-lookup"><span data-stu-id="8eafb-129">The default is 80.</span></span>

<span data-ttu-id="8eafb-130">**rgcolumncreate**</span><span class="sxs-lookup"><span data-stu-id="8eafb-130">**rgcolumncreate**</span></span>

<span data-ttu-id="8eafb-131">[JET_COLUMNCREATE](./jet-columncreate-structure.md)結構的陣列，其中每一個都對應到要在新資料表中建立的資料行。</span><span class="sxs-lookup"><span data-stu-id="8eafb-131">An array of [JET_COLUMNCREATE](./jet-columncreate-structure.md) structures, each of which corresponds to a column to be created in the new table.</span></span>

<span data-ttu-id="8eafb-132">**cColumns**</span><span class="sxs-lookup"><span data-stu-id="8eafb-132">**cColumns**</span></span>

<span data-ttu-id="8eafb-133">**Rgcolumncreate** 中 [JET_COLUMNCREATE](./jet-columncreate-structure.md)元素的數目。</span><span class="sxs-lookup"><span data-stu-id="8eafb-133">The number of [JET_COLUMNCREATE](./jet-columncreate-structure.md) elements in **rgcolumncreate**.</span></span>

<span data-ttu-id="8eafb-134">**rgindexcreate**</span><span class="sxs-lookup"><span data-stu-id="8eafb-134">**rgindexcreate**</span></span>

<span data-ttu-id="8eafb-135">[JET_INDEXCREATE](./jet-indexcreate-structure.md)結構的陣列，其中每一個都對應至要在新資料表中建立的索引。</span><span class="sxs-lookup"><span data-stu-id="8eafb-135">An array of [JET_INDEXCREATE](./jet-indexcreate-structure.md) structures, each of which corresponds to an index to be created in the new table.</span></span>

<span data-ttu-id="8eafb-136">**cIndexes**</span><span class="sxs-lookup"><span data-stu-id="8eafb-136">**cIndexes**</span></span>

<span data-ttu-id="8eafb-137">**Rgindexcreate** 中 [JET_INDEXCREATE](./jet-indexcreate-structure.md)元素的數目。</span><span class="sxs-lookup"><span data-stu-id="8eafb-137">The number of [JET_INDEXCREATE](./jet-indexcreate-structure.md) elements in **rgindexcreate**.</span></span>

<span data-ttu-id="8eafb-138">**grbit**</span><span class="sxs-lookup"><span data-stu-id="8eafb-138">**grbit**</span></span>

<span data-ttu-id="8eafb-139">包含此呼叫選項的位群組，其中包含零或多個下列值。</span><span class="sxs-lookup"><span data-stu-id="8eafb-139">A group of bits that contain the options for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8eafb-140">值</span><span class="sxs-lookup"><span data-stu-id="8eafb-140">Value</span></span></p></th>
<th><p><span data-ttu-id="8eafb-141">意義</span><span class="sxs-lookup"><span data-stu-id="8eafb-141">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8eafb-142">JET_bitTableCreateFixedDDL</span><span class="sxs-lookup"><span data-stu-id="8eafb-142">JET_bitTableCreateFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="8eafb-143">設定 JET_bitTableCreateFixedDDL 可防止資料表上的 DDL 作業 (例如) 加入或移除資料行。</span><span class="sxs-lookup"><span data-stu-id="8eafb-143">Setting JET_bitTableCreateFixedDDL prevents DDL operations on the table (such as adding or removing columns).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8eafb-144">JET_bitTableCreateTemplateTable</span><span class="sxs-lookup"><span data-stu-id="8eafb-144">JET_bitTableCreateTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="8eafb-145">設定 JET_bitTableCreateTemplateTable 會使資料表成為範本資料表。</span><span class="sxs-lookup"><span data-stu-id="8eafb-145">Setting JET_bitTableCreateTemplateTable causes the table to be a template table.</span></span> <span data-ttu-id="8eafb-146">然後，新的資料表可將此資料表的名稱指定為其範本資料表。</span><span class="sxs-lookup"><span data-stu-id="8eafb-146">New tables can then specify the name of this table as their template table.</span></span> <span data-ttu-id="8eafb-147">設定 JET_bitTableCreateTemplateTable 意指 JET_bitTableCreateFixedDDL。</span><span class="sxs-lookup"><span data-stu-id="8eafb-147">Setting JET_bitTableCreateTemplateTable implies JET_bitTableCreateFixedDDL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8eafb-148">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="8eafb-148">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="8eafb-149">已取代。</span><span class="sxs-lookup"><span data-stu-id="8eafb-149">Deprecated.</span></span> <span data-ttu-id="8eafb-150">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="8eafb-150">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8eafb-151">**tableid**</span><span class="sxs-lookup"><span data-stu-id="8eafb-151">**tableid**</span></span>

<span data-ttu-id="8eafb-152">如果 API 呼叫成功，則為包含新資料表之 [JET_TABLEID](./jet-tableid.md) 的輸出欄位。</span><span class="sxs-lookup"><span data-stu-id="8eafb-152">An output field that holds the [JET_TABLEID](./jet-tableid.md) of the new table if the API call succeeds.</span></span> <span data-ttu-id="8eafb-153">如果 API 呼叫失敗，則值為未定義。</span><span class="sxs-lookup"><span data-stu-id="8eafb-153">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="8eafb-154">**到尚未建立**</span><span class="sxs-lookup"><span data-stu-id="8eafb-154">**cCreated**</span></span>

<span data-ttu-id="8eafb-155">輸出欄位，其中包含 API 呼叫成功時所建立的物件計數。</span><span class="sxs-lookup"><span data-stu-id="8eafb-155">An output field that contains the count of objects created if the API call succeeds.</span></span> <span data-ttu-id="8eafb-156">如果 API 呼叫失敗，則值為未定義。</span><span class="sxs-lookup"><span data-stu-id="8eafb-156">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="8eafb-157">所建立的物件計數等於已成功建立之資料行、資料表和索引的總和。</span><span class="sxs-lookup"><span data-stu-id="8eafb-157">The count of objects that are created is equal to the sum of columns, tables, and indexes that are successfully created.</span></span>

### <a name="requirements"></a><span data-ttu-id="8eafb-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="8eafb-158">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8eafb-159"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="8eafb-159"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8eafb-160">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="8eafb-160">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8eafb-161"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="8eafb-161"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8eafb-162">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="8eafb-162">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8eafb-163"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="8eafb-163"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8eafb-164">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="8eafb-164">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8eafb-165"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="8eafb-165"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="8eafb-166">實作為 <strong>JET_TABLECREATE_W</strong> (Unicode) 和 <strong>JET_TABLECREATE_A</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="8eafb-166">Implemented as <strong>JET_TABLECREATE_W</strong> (Unicode) and <strong>JET_TABLECREATE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="8eafb-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8eafb-167">See Also</span></span>

[<span data-ttu-id="8eafb-168">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="8eafb-168">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="8eafb-169">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="8eafb-169">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="8eafb-170">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="8eafb-170">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="8eafb-171">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="8eafb-171">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="8eafb-172">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="8eafb-172">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="8eafb-173">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="8eafb-173">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="8eafb-174">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="8eafb-174">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="8eafb-175">JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="8eafb-175">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="8eafb-176">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="8eafb-176">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="8eafb-177">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="8eafb-177">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
