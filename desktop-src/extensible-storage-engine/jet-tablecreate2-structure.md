---
description: 深入瞭解： JET_TABLECREATE2 結構
title: JET_TABLECREATE2 結構
TOCTitle: JET_TABLECREATE2 Structure
ms:assetid: 2029e684-0d10-44e7-8033-d9cdbdffd7a4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269203(v=EXCHG.10)
ms:contentKeyID: 32765506
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
ms.openlocfilehash: d7ce983d393954c0d82f0d4e43108ff845d31571
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853020"
---
# <a name="jet_tablecreate2-structure"></a><span data-ttu-id="7a485-103">JET_TABLECREATE2 結構</span><span class="sxs-lookup"><span data-stu-id="7a485-103">JET_TABLECREATE2 Structure</span></span>


<span data-ttu-id="7a485-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7a485-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tablecreate2-structure"></a><span data-ttu-id="7a485-105">JET_TABLECREATE2 結構</span><span class="sxs-lookup"><span data-stu-id="7a485-105">JET_TABLECREATE2 Structure</span></span>

<span data-ttu-id="7a485-106">**JET_TABLECREATE2** 結構所包含的資訊，需要用來建立在 ESE 資料庫中填入資料行和索引的資料表，並指定回呼函數。</span><span class="sxs-lookup"><span data-stu-id="7a485-106">The **JET_TABLECREATE2** structure contains the information that is needed to create a table populated with columns and indexes in an ESE database, and that designates a callback function.</span></span> <span data-ttu-id="7a485-107">[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)會使用 **JET_TABLECREATE2** 結構。</span><span class="sxs-lookup"><span data-stu-id="7a485-107">The **JET_TABLECREATE2** structure is used by [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).</span></span>

<span data-ttu-id="7a485-108">**WINDOWS XP：** 在 Windows XP 中引進 **JET_TABLECREATE2** 結構。</span><span class="sxs-lookup"><span data-stu-id="7a485-108">**Windows XP:** The **JET_TABLECREATE2** structure is introduced in Windows XP.</span></span>

```cpp
    typedef struct tagJET_TABLECREATE2 {
      unsigned long cbStruct;
      tchar* szTableName;
      tchar* szTemplateTableName;
      unsigned long ulPages;
      unsigned long ulDensity;
      JET_COLUMNCREATE* rgcolumncreate;
      unsigned long cColumns;
      JET_INDEXCREATE* rgindexcreate;
      unsigned long cIndexes;
      tchar* szCallback;
      JET_CBTYP cbtyp;
      JET_GRBIT grbit;
      JET_TABLEID tableid;
      unsigned long cCreated;
    } JET_TABLECREATE2;
```

### <a name="members"></a><span data-ttu-id="7a485-109">成員</span><span class="sxs-lookup"><span data-stu-id="7a485-109">Members</span></span>

<span data-ttu-id="7a485-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="7a485-110">**cbStruct**</span></span>

<span data-ttu-id="7a485-111">此結構的大小，以位元組為單位， (未來的擴充) 。</span><span class="sxs-lookup"><span data-stu-id="7a485-111">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="7a485-112">它必須設定為 sizeof ( JET_TABLECREATE2 ) （以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7a485-112">It must be set to sizeof( JET_TABLECREATE2 ) in bytes.</span></span>

<span data-ttu-id="7a485-113">**szTableName**</span><span class="sxs-lookup"><span data-stu-id="7a485-113">**szTableName**</span></span>

<span data-ttu-id="7a485-114">要建立之資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a485-114">The name of table to create.</span></span>

<span data-ttu-id="7a485-115">名稱必須使用符合下列條件：</span><span class="sxs-lookup"><span data-stu-id="7a485-115">The name must use meet the following conditions:</span></span>

  - <span data-ttu-id="7a485-116">值小於 JET_cbNameMost，不包括終止的 Null。</span><span class="sxs-lookup"><span data-stu-id="7a485-116">Have a value less than JET_cbNameMost, not including the terminating NULL.</span></span>

<!-- end list -->

  - <span data-ttu-id="7a485-117">包含下列一組字元：0到9、A 到 Z、a 到 z，以及除了驚嘆號以外的所有其他標點符號 (\!) 、逗點 (、) 、左括弧 (\[) 和右括弧 () \] ，也就是 ASCII 字元0x20、0x22 至0x2d、0x2f 至0x5a、0x5c 和0x5d 至0x7f。</span><span class="sxs-lookup"><span data-stu-id="7a485-117">Consist of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]), that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

<!-- end list -->

  - <span data-ttu-id="7a485-118">不是以空格開頭。</span><span class="sxs-lookup"><span data-stu-id="7a485-118">Not begin with a space.</span></span>

<!-- end list -->

  - <span data-ttu-id="7a485-119">至少包含一個非空白字元。</span><span class="sxs-lookup"><span data-stu-id="7a485-119">Consist of at least one non-space character.</span></span>

<span data-ttu-id="7a485-120">**szTemplateTableName**</span><span class="sxs-lookup"><span data-stu-id="7a485-120">**szTemplateTableName**</span></span>

<span data-ttu-id="7a485-121">現有資料表的名稱，要從此資料表繼承基底 DDL (資料定義語言) 。</span><span class="sxs-lookup"><span data-stu-id="7a485-121">The name of an already-existing table from which to inherit base DDL (Data Definition Language).</span></span> <span data-ttu-id="7a485-122">使用範本資料表可讓您輕鬆地建立具有相同資料行和索引的多個資料表。</span><span class="sxs-lookup"><span data-stu-id="7a485-122">Using a template table allows easy creation of many tables with identical columns and indexes.</span></span>

<span data-ttu-id="7a485-123">**ulPages**</span><span class="sxs-lookup"><span data-stu-id="7a485-123">**ulPages**</span></span>

<span data-ttu-id="7a485-124">要配置給資料表的初始資料庫頁面數目。</span><span class="sxs-lookup"><span data-stu-id="7a485-124">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="7a485-125">如果有多個資料列插入此資料表中，指定大於1的數位可以減少片段。</span><span class="sxs-lookup"><span data-stu-id="7a485-125">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="7a485-126">**ulDensity**</span><span class="sxs-lookup"><span data-stu-id="7a485-126">**ulDensity**</span></span>

<span data-ttu-id="7a485-127">資料表密度（以百分比為單位）。</span><span class="sxs-lookup"><span data-stu-id="7a485-127">The table density, in percentage points.</span></span> <span data-ttu-id="7a485-128">此數位必須是0或20到100的範圍。</span><span class="sxs-lookup"><span data-stu-id="7a485-128">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="7a485-129">傳遞0表示應該使用預設值。</span><span class="sxs-lookup"><span data-stu-id="7a485-129">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="7a485-130">預設值為80。</span><span class="sxs-lookup"><span data-stu-id="7a485-130">The default is 80.</span></span>

<span data-ttu-id="7a485-131">**rgcolumncreate**</span><span class="sxs-lookup"><span data-stu-id="7a485-131">**rgcolumncreate**</span></span>

<span data-ttu-id="7a485-132">[JET_COLUMNCREATE](./jet-columncreate-structure.md)結構的陣列，其中每一個都對應到要在新資料表中建立的資料行。</span><span class="sxs-lookup"><span data-stu-id="7a485-132">An array of [JET_COLUMNCREATE](./jet-columncreate-structure.md) structures, each of which corresponds to a column to be created in the new table.</span></span>

<span data-ttu-id="7a485-133">**cColumns**</span><span class="sxs-lookup"><span data-stu-id="7a485-133">**cColumns**</span></span>

<span data-ttu-id="7a485-134">**rgcolumncreate** 中 [JET_COLUMNCREATE](./jet-columncreate-structure.md)元素的數目。</span><span class="sxs-lookup"><span data-stu-id="7a485-134">the number of [JET_COLUMNCREATE](./jet-columncreate-structure.md) elements in **rgcolumncreate**.</span></span>

<span data-ttu-id="7a485-135">**rgindexcreate**</span><span class="sxs-lookup"><span data-stu-id="7a485-135">**rgindexcreate**</span></span>

<span data-ttu-id="7a485-136">[JET_INDEXCREATE](./jet-indexcreate-structure.md)結構的陣列，其中每一個都對應至要在新資料表中建立的索引。</span><span class="sxs-lookup"><span data-stu-id="7a485-136">An array of [JET_INDEXCREATE](./jet-indexcreate-structure.md) structures, each of which corresponds to an index to be created in the new table.</span></span>

<span data-ttu-id="7a485-137">**cIndexes**</span><span class="sxs-lookup"><span data-stu-id="7a485-137">**cIndexes**</span></span>

<span data-ttu-id="7a485-138">**Rgindexcreate** 中 [JET_INDEXCREATE](./jet-indexcreate-structure.md)元素的數目。</span><span class="sxs-lookup"><span data-stu-id="7a485-138">The number of [JET_INDEXCREATE](./jet-indexcreate-structure.md) elements in **rgindexcreate**.</span></span>

<span data-ttu-id="7a485-139">**szCallback**</span><span class="sxs-lookup"><span data-stu-id="7a485-139">**szCallback**</span></span>

<span data-ttu-id="7a485-140">在特定事件期間呼叫的函式。</span><span class="sxs-lookup"><span data-stu-id="7a485-140">The function that gets called during certain events.</span></span> <span data-ttu-id="7a485-141">**cbtyp** 會判斷呼叫回呼函式的時間。</span><span class="sxs-lookup"><span data-stu-id="7a485-141">**cbtyp** determines when the callback function will be called.</span></span>

<span data-ttu-id="7a485-142">**SzCallback** 的格式必須是 "module \! function"，例如 "Alpha \! Beta" 指的是名為 "Alpha" 的模組中的搶鮮版（Beta）函數。</span><span class="sxs-lookup"><span data-stu-id="7a485-142">The format of **szCallback** must be "module\!function"—for example, "alpha\!beta" refers to the beta function in the module named "alpha".</span></span> <span data-ttu-id="7a485-143">函數的原型必須符合 [JET_CALLBACK](./jet-callback-callback-function.md)。</span><span class="sxs-lookup"><span data-stu-id="7a485-143">The prototype of the function must match [JET_CALLBACK](./jet-callback-callback-function.md).</span></span> <span data-ttu-id="7a485-144">如需詳細資訊，請參閱 [JET_CALLBACK](./jet-callback-callback-function.md)。</span><span class="sxs-lookup"><span data-stu-id="7a485-144">For more information, see [JET_CALLBACK](./jet-callback-callback-function.md).</span></span>

<span data-ttu-id="7a485-145">**cbtyp**</span><span class="sxs-lookup"><span data-stu-id="7a485-145">**cbtyp**</span></span>

<span data-ttu-id="7a485-146">描述 **szCallback** 所指定之回呼函式的類型。</span><span class="sxs-lookup"><span data-stu-id="7a485-146">Describes the type of callback function designated by **szCallback**.</span></span> <span data-ttu-id="7a485-147">如需詳細資訊，請參閱 [JET_CBTYP](./jet-cbtyp.md)。</span><span class="sxs-lookup"><span data-stu-id="7a485-147">For more information, see [JET_CBTYP](./jet-cbtyp.md).</span></span> <span data-ttu-id="7a485-148">此位位由下列一或多個位組成。</span><span class="sxs-lookup"><span data-stu-id="7a485-148">This bitfield is composed of one or more of the following bits.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7a485-149">值</span><span class="sxs-lookup"><span data-stu-id="7a485-149">Value</span></span></p></th>
<th><p><span data-ttu-id="7a485-150">意義</span><span class="sxs-lookup"><span data-stu-id="7a485-150">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7a485-151">JET_cbtypFinalize</span><span class="sxs-lookup"><span data-stu-id="7a485-151">JET_cbtypFinalize</span></span></p></td>
<td><p><span data-ttu-id="7a485-152">當可以完成的資料行已消失時，就會呼叫回呼函數。</span><span class="sxs-lookup"><span data-stu-id="7a485-152">The callback function will be called when a column that can be finalized has gone to zero.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a485-153">JET_cbtypBeforeInsert</span><span class="sxs-lookup"><span data-stu-id="7a485-153">JET_cbtypBeforeInsert</span></span></p></td>
<td><p><span data-ttu-id="7a485-154">回呼函式會在插入記錄之前呼叫。</span><span class="sxs-lookup"><span data-stu-id="7a485-154">The callback function will be called prior to record insertion.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a485-155">JET_cbtypAfterInsert</span><span class="sxs-lookup"><span data-stu-id="7a485-155">JET_cbtypAfterInsert</span></span></p></td>
<td><p><span data-ttu-id="7a485-156">一旦資料庫引擎完成插入記錄之後，就會呼叫回呼函數。</span><span class="sxs-lookup"><span data-stu-id="7a485-156">The callback function will be called once the database engine has finished inserting a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a485-157">JET_cbtypBeforeReplace</span><span class="sxs-lookup"><span data-stu-id="7a485-157">JET_cbtypBeforeReplace</span></span></p></td>
<td><p><span data-ttu-id="7a485-158">回呼函數將在修改記錄之前呼叫。</span><span class="sxs-lookup"><span data-stu-id="7a485-158">The callback function will be called prior to modification of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a485-159">JET_cbtypAfterReplace</span><span class="sxs-lookup"><span data-stu-id="7a485-159">JET_cbtypAfterReplace</span></span></p></td>
<td><p><span data-ttu-id="7a485-160">完成記錄修改之後，將會呼叫回呼函式。</span><span class="sxs-lookup"><span data-stu-id="7a485-160">The callback function will be called after finishing modification of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a485-161">JET_cbtypBeforeDelete</span><span class="sxs-lookup"><span data-stu-id="7a485-161">JET_cbtypBeforeDelete</span></span></p></td>
<td><p><span data-ttu-id="7a485-162">回呼函數將在刪除記錄之前呼叫。</span><span class="sxs-lookup"><span data-stu-id="7a485-162">The callback function will be called prior to deletion of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a485-163">JET_cbtypAfterDelete</span><span class="sxs-lookup"><span data-stu-id="7a485-163">JET_cbtypAfterDelete</span></span></p></td>
<td><p><span data-ttu-id="7a485-164">刪除記錄之後，將會呼叫回呼函數。</span><span class="sxs-lookup"><span data-stu-id="7a485-164">The callback function will be called after a record has been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a485-165">JET_cbtypUserDefinedDefaultValue</span><span class="sxs-lookup"><span data-stu-id="7a485-165">JET_cbtypUserDefinedDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="7a485-166">系統會呼叫回呼函式來計算使用者定義的預設值。</span><span class="sxs-lookup"><span data-stu-id="7a485-166">The callback function will be called to calculate a user-defined default.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a485-167">JET_cbtypOnlineDefragCompleted</span><span class="sxs-lookup"><span data-stu-id="7a485-167">JET_cbtypOnlineDefragCompleted</span></span></p></td>
<td><p><span data-ttu-id="7a485-168">呼叫 <a href="gg294095(v=exchg.10).md">JetDefragment2</a> 完成之後，就會呼叫回呼函式。</span><span class="sxs-lookup"><span data-stu-id="7a485-168">The callback function will be called after a call to <a href="gg294095(v=exchg.10).md">JetDefragment2</a> has completed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a485-169">JET_cbtypFreeCursorLS</span><span class="sxs-lookup"><span data-stu-id="7a485-169">JET_cbtypFreeCursorLS</span></span></p></td>
<td><p><span data-ttu-id="7a485-170">當必須釋放與資料指標相關聯的本機儲存體時，就會呼叫回呼函數。</span><span class="sxs-lookup"><span data-stu-id="7a485-170">The callback function will be called when the local storage that is associated with a cursor must be freed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a485-171">JET_cbtypFreeTableLS</span><span class="sxs-lookup"><span data-stu-id="7a485-171">JET_cbtypFreeTableLS</span></span></p></td>
<td><p><span data-ttu-id="7a485-172">當必須釋放與資料表相關聯的本機儲存體時，就會呼叫回呼函數。</span><span class="sxs-lookup"><span data-stu-id="7a485-172">The callback function will be called when the local storage that is associated with a table must be freed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7a485-173">**grbit**</span><span class="sxs-lookup"><span data-stu-id="7a485-173">**grbit**</span></span>

<span data-ttu-id="7a485-174">包含此呼叫選項的位群組，其中包含零或多個下列值。</span><span class="sxs-lookup"><span data-stu-id="7a485-174">A group of bits that contain the options for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7a485-175">值</span><span class="sxs-lookup"><span data-stu-id="7a485-175">Value</span></span></p></th>
<th><p><span data-ttu-id="7a485-176">意義</span><span class="sxs-lookup"><span data-stu-id="7a485-176">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7a485-177">JET_bitTableCreateFixedDDL</span><span class="sxs-lookup"><span data-stu-id="7a485-177">JET_bitTableCreateFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="7a485-178">設定 JET_bitTableCreateFixedDDL 可防止資料表上的 DDL 作業 (例如) 加入或移除資料行。</span><span class="sxs-lookup"><span data-stu-id="7a485-178">Setting JET_bitTableCreateFixedDDL prevents DDL operations on the table (such as adding or removing columns).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a485-179">JET_bitTableCreateTemplateTable</span><span class="sxs-lookup"><span data-stu-id="7a485-179">JET_bitTableCreateTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="7a485-180">設定 JET_bitTableCreateTemplateTable 會使資料表成為範本資料表。</span><span class="sxs-lookup"><span data-stu-id="7a485-180">Setting JET_bitTableCreateTemplateTable causes the table to be a template table.</span></span> <span data-ttu-id="7a485-181">然後，新的資料表可將此資料表的名稱指定為其範本資料表。</span><span class="sxs-lookup"><span data-stu-id="7a485-181">New tables can then specify the name of this table as their template table.</span></span> <span data-ttu-id="7a485-182">設定 JET_bitTableCreateTemplateTable 意指 JET_bitTableCreateFixedDDL。</span><span class="sxs-lookup"><span data-stu-id="7a485-182">Setting JET_bitTableCreateTemplateTable implies JET_bitTableCreateFixedDDL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a485-183">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="7a485-183">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="7a485-184">必須搭配 JET_bitTableCreateTemplateTable 使用。</span><span class="sxs-lookup"><span data-stu-id="7a485-184">Must be used in conjunction with JET_bitTableCreateTemplateTable.</span></span> <span data-ttu-id="7a485-185">已取代。</span><span class="sxs-lookup"><span data-stu-id="7a485-185">Deprecated.</span></span> <span data-ttu-id="7a485-186">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="7a485-186">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7a485-187">**tableid**</span><span class="sxs-lookup"><span data-stu-id="7a485-187">**tableid**</span></span>

<span data-ttu-id="7a485-188">如果 API 呼叫成功，則為包含新資料表之 [JET_TABLEID](./jet-tableid.md) 的輸出欄位。</span><span class="sxs-lookup"><span data-stu-id="7a485-188">An output field that holds the [JET_TABLEID](./jet-tableid.md) of the new table if the API call succeeds.</span></span> <span data-ttu-id="7a485-189">如果 API 呼叫失敗，則值為未定義。</span><span class="sxs-lookup"><span data-stu-id="7a485-189">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="7a485-190">**到尚未建立**</span><span class="sxs-lookup"><span data-stu-id="7a485-190">**cCreated**</span></span>

<span data-ttu-id="7a485-191">輸出欄位，其中包含 API 呼叫成功時所建立的物件計數。</span><span class="sxs-lookup"><span data-stu-id="7a485-191">An output field that contains the count of objects that are created if the API call succeeds.</span></span> <span data-ttu-id="7a485-192">如果 API 呼叫失敗，則值為未定義。</span><span class="sxs-lookup"><span data-stu-id="7a485-192">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="7a485-193">所建立的物件計數等於已成功建立之資料行、資料表和索引的總和。</span><span class="sxs-lookup"><span data-stu-id="7a485-193">The count of objects that is created is equal to the sum of columns, tables, and indexes that are successfully created.</span></span>

### <a name="requirements"></a><span data-ttu-id="7a485-194">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a485-194">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7a485-195"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="7a485-195"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7a485-196">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="7a485-196">Requires Windows  Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a485-197"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="7a485-197"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7a485-198">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="7a485-198">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a485-199"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="7a485-199"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7a485-200">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="7a485-200">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a485-201"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="7a485-201"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="7a485-202">實作為 <strong>JET_TABLECREATE2_W</strong> (Unicode) 和 <strong>JET_TABLECREATE2_A</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="7a485-202">Implemented as <strong>JET_TABLECREATE2_W</strong> (Unicode) and <strong>JET_TABLECREATE2_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="7a485-203">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a485-203">See Also</span></span>

[<span data-ttu-id="7a485-204">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="7a485-204">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="7a485-205">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="7a485-205">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="7a485-206">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="7a485-206">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="7a485-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7a485-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7a485-208">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="7a485-208">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="7a485-209">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="7a485-209">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="7a485-210">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="7a485-210">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="7a485-211">JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="7a485-211">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="7a485-212">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="7a485-212">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="7a485-213">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="7a485-213">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="7a485-214">JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="7a485-214">JetDefragment2</span></span>](./jetdefragment2-function.md)
