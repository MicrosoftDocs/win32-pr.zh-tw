---
description: 深入瞭解： JET_TABLECREATE3 結構
title: JET_TABLECREATE3 結構
TOCTitle: JET_TABLECREATE3 Structure
ms:assetid: 61909569-e704-494b-a56d-b64d1a2ee157
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269264(v=EXCHG.10)
ms:contentKeyID: 32765566
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 587649b592f2b0d213a481c3bfbecc723240e486
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991680"
---
# <a name="jet_tablecreate3-structure"></a><span data-ttu-id="02a8d-103">JET_TABLECREATE3 結構</span><span class="sxs-lookup"><span data-stu-id="02a8d-103">JET_TABLECREATE3 Structure</span></span>


<span data-ttu-id="02a8d-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="02a8d-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="02a8d-105">**JET_TABLECREATE3** 結構包含建立資料表時所需的資訊，此資料表會填入可延伸儲存引擎中的資料行和索引， (ESE) 資料庫，並指定回呼函數。</span><span class="sxs-lookup"><span data-stu-id="02a8d-105">The **JET_TABLECREATE3** structure contains the information that is needed to create a table populated with columns and indexes in an Extensible Storage Engine (ESE) database, and that designates a callback function.</span></span> <span data-ttu-id="02a8d-106">[JetCreateTableColumnIndex3](./jetcreatetablecolumnindex3-function.md)函數會使用 **JET_TABLECREATE3** 結構。</span><span class="sxs-lookup"><span data-stu-id="02a8d-106">The **JET_TABLECREATE3** structure is used by the [JetCreateTableColumnIndex3](./jetcreatetablecolumnindex3-function.md) function.</span></span>

<span data-ttu-id="02a8d-107">在 Windows 7 作業系統中引進了 **JET_TABLECREATE3** 結構。</span><span class="sxs-lookup"><span data-stu-id="02a8d-107">The **JET_TABLECREATE3** structure was introduced in the Windows 7 operating system.</span></span>

``` cpp
typedef struct tagJET_TABLECREATE3 {
  unsigned long cbStruct;
  tchar* szTableName;
  tchar* szTemplateTableName;
  unsigned long ulPages;
  unsigned long ulDensity;
  JET_COLUMNCREATE* rgcolumncreate;
  unsigned long cColumns;
    JET_INDEXCREATE2* rgindexcreate;
  unsigned long cIndexes;
  tchar* szCallback;
  JET_CBTYP cbtyp;
  JET_GRBIT grbit;
  JET_TABLEID tableid;
  un  JET_GRBIT grbit;
  JET_SPACEHINTS* pSeqSpacehints;
  JET_SPACEHINTS* pLVSpacehints;
  unsigned long cbSeparateLV;
  JET_TABLEID tableid;
  unsigned long cCreated;
} JET_TABLECREATE3;>
```

### <a name="members"></a><span data-ttu-id="02a8d-108">成員</span><span class="sxs-lookup"><span data-stu-id="02a8d-108">Members</span></span>

<span data-ttu-id="02a8d-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="02a8d-109">**cbStruct**</span></span>

<span data-ttu-id="02a8d-110">此結構的大小，以位元組為單位， (未來的擴充) 。</span><span class="sxs-lookup"><span data-stu-id="02a8d-110">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="02a8d-111">它必須設定為 sizeof ( JET_TABLECREATE3 ) （以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="02a8d-111">It must be set to sizeof( JET_TABLECREATE3 ) in bytes.</span></span>

<span data-ttu-id="02a8d-112">**szTableName**</span><span class="sxs-lookup"><span data-stu-id="02a8d-112">**szTableName**</span></span>

<span data-ttu-id="02a8d-113">要建立之資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="02a8d-113">The name of the table to create.</span></span>

<span data-ttu-id="02a8d-114">此名稱必須符合下列條件：</span><span class="sxs-lookup"><span data-stu-id="02a8d-114">The name must meet the following conditions:</span></span>

  - <span data-ttu-id="02a8d-115">它必須有小於 JET_cbNameMost 的值，不包括終止的 null。</span><span class="sxs-lookup"><span data-stu-id="02a8d-115">It must have a value that is less than JET_cbNameMost, not including the terminating null.</span></span>

  - <span data-ttu-id="02a8d-116">它必須包含下列字元組：0到9、A 到 Z、a 到 z，以及除了驚嘆號以外的所有其他標點符號 (\!) 、逗點 (、) 、左括弧 (\[) 和右括弧 () \] ; 也就是說，ASCII 字元0x20、0x22 至0x2d、0x2f 至0x5a、0x5c 和0x5d 至0x7f。</span><span class="sxs-lookup"><span data-stu-id="02a8d-116">It must consist of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]); that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="02a8d-117">不得以空格開頭。</span><span class="sxs-lookup"><span data-stu-id="02a8d-117">It must not begin with a space.</span></span>

  - <span data-ttu-id="02a8d-118">它必須包含至少一個非空白字元。</span><span class="sxs-lookup"><span data-stu-id="02a8d-118">It must consist of at least one non-space character.</span></span>

<span data-ttu-id="02a8d-119">**szTemplateTableName**</span><span class="sxs-lookup"><span data-stu-id="02a8d-119">**szTemplateTableName**</span></span>

<span data-ttu-id="02a8d-120">要從中繼承基底資料定義語言 (DDL) 的現有資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="02a8d-120">The name of an existing table from which to inherit the base data definition language (DDL).</span></span> <span data-ttu-id="02a8d-121">使用範本資料表可讓您輕鬆地建立具有相同資料行和索引的多個資料表。</span><span class="sxs-lookup"><span data-stu-id="02a8d-121">Use of a template table allows for the easy creation of many tables with identical columns and indexes.</span></span>

<span data-ttu-id="02a8d-122">**ulPages**</span><span class="sxs-lookup"><span data-stu-id="02a8d-122">**ulPages**</span></span>

<span data-ttu-id="02a8d-123">要配置給資料表的初始資料庫頁面數目。</span><span class="sxs-lookup"><span data-stu-id="02a8d-123">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="02a8d-124">如果有多個資料列插入此資料表中，指定大於1的數位可以減少片段。</span><span class="sxs-lookup"><span data-stu-id="02a8d-124">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="02a8d-125">**ulDensity**</span><span class="sxs-lookup"><span data-stu-id="02a8d-125">**ulDensity**</span></span>

<span data-ttu-id="02a8d-126">資料表密度（以百分比為單位）。</span><span class="sxs-lookup"><span data-stu-id="02a8d-126">The table density, in percentage points.</span></span> <span data-ttu-id="02a8d-127">此數位必須是0或20到100的範圍。</span><span class="sxs-lookup"><span data-stu-id="02a8d-127">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="02a8d-128">傳遞0表示應該使用預設值。</span><span class="sxs-lookup"><span data-stu-id="02a8d-128">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="02a8d-129">預設值是 80。</span><span class="sxs-lookup"><span data-stu-id="02a8d-129">The default value is 80.</span></span>

<span data-ttu-id="02a8d-130">**rgcolumncreate**</span><span class="sxs-lookup"><span data-stu-id="02a8d-130">**rgcolumncreate**</span></span>

<span data-ttu-id="02a8d-131">[JET_COLUMNCREATE](./jet-columncreate-structure.md)結構的陣列，其中每一個都對應到要在新資料表中建立的資料行。</span><span class="sxs-lookup"><span data-stu-id="02a8d-131">An array of [JET_COLUMNCREATE](./jet-columncreate-structure.md) structures, each of which corresponds to a column to be created in the new table.</span></span>

<span data-ttu-id="02a8d-132">**cColumns**</span><span class="sxs-lookup"><span data-stu-id="02a8d-132">**cColumns**</span></span>

<span data-ttu-id="02a8d-133">*Rgcolumncreate* 參數中 [JET_COLUMNCREATE](./jet-columncreate-structure.md)元素的數目。</span><span class="sxs-lookup"><span data-stu-id="02a8d-133">The number of [JET_COLUMNCREATE](./jet-columncreate-structure.md) elements in the *rgcolumncreate* parameter.</span></span>

<span data-ttu-id="02a8d-134">**rgindexcreate**</span><span class="sxs-lookup"><span data-stu-id="02a8d-134">**rgindexcreate**</span></span>

<span data-ttu-id="02a8d-135">[JET_INDEXCREATE2](./jet-indexcreate2-structure.md)結構的陣列，其中每一個都對應至要在新資料表中建立的索引。</span><span class="sxs-lookup"><span data-stu-id="02a8d-135">An array of [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structures, each of which corresponds to an index to be created in the new table.</span></span>

<span data-ttu-id="02a8d-136">**cIndexes**</span><span class="sxs-lookup"><span data-stu-id="02a8d-136">**cIndexes**</span></span>

<span data-ttu-id="02a8d-137">*Rgindexcreate* 參數中 [JET_INDEXCREATE2](./jet-indexcreate2-structure.md)元素的數目。</span><span class="sxs-lookup"><span data-stu-id="02a8d-137">The number of [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) elements in the *rgindexcreate* parameter.</span></span>

<span data-ttu-id="02a8d-138">**szCallback**</span><span class="sxs-lookup"><span data-stu-id="02a8d-138">**szCallback**</span></span>

<span data-ttu-id="02a8d-139">在特定事件期間呼叫的函式。</span><span class="sxs-lookup"><span data-stu-id="02a8d-139">The function that gets called during certain events.</span></span> <span data-ttu-id="02a8d-140">**cbtyp** 會判斷呼叫回呼函式的時間。</span><span class="sxs-lookup"><span data-stu-id="02a8d-140">**cbtyp** determines when the callback function will be called.</span></span>

<span data-ttu-id="02a8d-141">**SzCallback** 的格式必須是 "module \! function"，例如 "Alpha \! Beta" 指的是名為 "Alpha" 的模組中的搶鮮版（Beta）函數。</span><span class="sxs-lookup"><span data-stu-id="02a8d-141">The format of **szCallback** must be "module\!function" — for example, "alpha\!beta" refers to the beta function in the module named "alpha".</span></span>

<span data-ttu-id="02a8d-142">函數的原型必須符合 [JET_CALLBACK](./jet-callback-callback-function.md) 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="02a8d-142">The prototype of the function must match the [JET_CALLBACK](./jet-callback-callback-function.md) callback function.</span></span>

<span data-ttu-id="02a8d-143">**cbtyp**</span><span class="sxs-lookup"><span data-stu-id="02a8d-143">**cbtyp**</span></span>

<span data-ttu-id="02a8d-144">描述 **szCallback** 所指定之回呼函式的類型。</span><span class="sxs-lookup"><span data-stu-id="02a8d-144">Describes the type of callback function designated by **szCallback**.</span></span> <span data-ttu-id="02a8d-145">如需詳細資訊，請參閱 [JET_CBTYP](./jet-cbtyp.md)。</span><span class="sxs-lookup"><span data-stu-id="02a8d-145">For more information, see [JET_CBTYP](./jet-cbtyp.md).</span></span>

<span data-ttu-id="02a8d-146">此位位由下表所列的一或多個位值所組成。</span><span class="sxs-lookup"><span data-stu-id="02a8d-146">This bitfield is composed of one or more of the bit values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="02a8d-147">值</span><span class="sxs-lookup"><span data-stu-id="02a8d-147">Value</span></span></p></th>
<th><p><span data-ttu-id="02a8d-148">意義</span><span class="sxs-lookup"><span data-stu-id="02a8d-148">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02a8d-149">JET_cbtypFinalize</span><span class="sxs-lookup"><span data-stu-id="02a8d-149">JET_cbtypFinalize</span></span></p></td>
<td><p><span data-ttu-id="02a8d-150">當可以完成的資料行已消失時，就會呼叫回呼函數。</span><span class="sxs-lookup"><span data-stu-id="02a8d-150">The callback function will be called when a column that can be finalized has gone to zero.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02a8d-151">JET_cbtypBeforeInsert</span><span class="sxs-lookup"><span data-stu-id="02a8d-151">JET_cbtypBeforeInsert</span></span></p></td>
<td><p><span data-ttu-id="02a8d-152">回呼函式會在插入記錄之前呼叫。</span><span class="sxs-lookup"><span data-stu-id="02a8d-152">The callback function will be called prior to record insertion.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02a8d-153">JET_cbtypAfterInsert</span><span class="sxs-lookup"><span data-stu-id="02a8d-153">JET_cbtypAfterInsert</span></span></p></td>
<td><p><span data-ttu-id="02a8d-154">在資料庫引擎完成插入記錄之後，將會呼叫回呼函數。</span><span class="sxs-lookup"><span data-stu-id="02a8d-154">The callback function will be called after the database engine has finished inserting a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02a8d-155">JET_cbtypBeforeReplace</span><span class="sxs-lookup"><span data-stu-id="02a8d-155">JET_cbtypBeforeReplace</span></span></p></td>
<td><p><span data-ttu-id="02a8d-156">回呼函數將在修改記錄之前呼叫。</span><span class="sxs-lookup"><span data-stu-id="02a8d-156">The callback function will be called prior to the modification of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02a8d-157">JET_cbtypAfterReplace</span><span class="sxs-lookup"><span data-stu-id="02a8d-157">JET_cbtypAfterReplace</span></span></p></td>
<td><p><span data-ttu-id="02a8d-158">完成記錄修改之後，將會呼叫回呼函數。</span><span class="sxs-lookup"><span data-stu-id="02a8d-158">The callback function will be called after finishing the modification of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02a8d-159">JET_cbtypBeforeDelete</span><span class="sxs-lookup"><span data-stu-id="02a8d-159">JET_cbtypBeforeDelete</span></span></p></td>
<td><p><span data-ttu-id="02a8d-160">回呼函數將在刪除記錄之前呼叫。</span><span class="sxs-lookup"><span data-stu-id="02a8d-160">The callback function will be called prior to the deletion of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02a8d-161">JET_cbtypAfterDelete</span><span class="sxs-lookup"><span data-stu-id="02a8d-161">JET_cbtypAfterDelete</span></span></p></td>
<td><p><span data-ttu-id="02a8d-162">刪除記錄之後，將會呼叫回呼函數。</span><span class="sxs-lookup"><span data-stu-id="02a8d-162">The callback function will be called after a record has been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02a8d-163">JET_cbtypUserDefinedDefaultValue</span><span class="sxs-lookup"><span data-stu-id="02a8d-163">JET_cbtypUserDefinedDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="02a8d-164">系統會呼叫回呼函式來計算使用者定義的預設值。</span><span class="sxs-lookup"><span data-stu-id="02a8d-164">The callback function will be called to calculate a user-defined default.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02a8d-165">JET_cbtypFreeCursorLS</span><span class="sxs-lookup"><span data-stu-id="02a8d-165">JET_cbtypFreeCursorLS</span></span></p></td>
<td><p><span data-ttu-id="02a8d-166">當必須釋放與資料指標相關聯的本機儲存體時，就會呼叫回呼函數。</span><span class="sxs-lookup"><span data-stu-id="02a8d-166">The callback function will be called when the local storage that is associated with a cursor must be freed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02a8d-167">JET_cbtypFreeTableLS</span><span class="sxs-lookup"><span data-stu-id="02a8d-167">JET_cbtypFreeTableLS</span></span></p></td>
<td><p><span data-ttu-id="02a8d-168">當必須釋放與資料表相關聯的本機儲存體時，就會呼叫回呼函數。</span><span class="sxs-lookup"><span data-stu-id="02a8d-168">The callback function will be called when the local storage that is associated with a table must be freed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="02a8d-169">**grbit**</span><span class="sxs-lookup"><span data-stu-id="02a8d-169">**grbit**</span></span>

<span data-ttu-id="02a8d-170">位群組，其中包含下表所列的零或多個呼叫選項值。</span><span class="sxs-lookup"><span data-stu-id="02a8d-170">A group of bits that contains zero or more of the call option values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="02a8d-171">值</span><span class="sxs-lookup"><span data-stu-id="02a8d-171">Value</span></span></p></th>
<th><p><span data-ttu-id="02a8d-172">意義</span><span class="sxs-lookup"><span data-stu-id="02a8d-172">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02a8d-173">JET_bitTableCreateFixedDDL</span><span class="sxs-lookup"><span data-stu-id="02a8d-173">JET_bitTableCreateFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="02a8d-174">防止資料表上的 DDL 作業 (例如新增或移除) 的資料行。</span><span class="sxs-lookup"><span data-stu-id="02a8d-174">Prevents DDL operations on the table (such as adding or removing columns).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02a8d-175">JET_bitTableCreateTemplateTable</span><span class="sxs-lookup"><span data-stu-id="02a8d-175">JET_bitTableCreateTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="02a8d-176">使資料表成為範本資料表。</span><span class="sxs-lookup"><span data-stu-id="02a8d-176">Causes the table to be a template table.</span></span> <span data-ttu-id="02a8d-177">然後，新的資料表可將此資料表的名稱指定為其範本資料表。</span><span class="sxs-lookup"><span data-stu-id="02a8d-177">New tables can then specify the name of this table as their template table.</span></span> <span data-ttu-id="02a8d-178">設定 JET_bitTableCreateTemplateTable 意指 JET_bitTableCreateFixedDDL。</span><span class="sxs-lookup"><span data-stu-id="02a8d-178">Setting JET_bitTableCreateTemplateTable implies JET_bitTableCreateFixedDDL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02a8d-179">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="02a8d-179">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="02a8d-180">必須搭配 JET_bitTableCreateTemplateTable 使用。</span><span class="sxs-lookup"><span data-stu-id="02a8d-180">Must be used in conjunction with JET_bitTableCreateTemplateTable.</span></span> <span data-ttu-id="02a8d-181">已取代。</span><span class="sxs-lookup"><span data-stu-id="02a8d-181">Deprecated.</span></span> <span data-ttu-id="02a8d-182">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="02a8d-182">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="02a8d-183">**pSeqSpacehints**</span><span class="sxs-lookup"><span data-stu-id="02a8d-183">**pSeqSpacehints**</span></span>

<span data-ttu-id="02a8d-184">預設連續索引的 [JET_SPACEHINTS](./jet-spacehints-structure.md) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="02a8d-184">A pointer to a [JET_SPACEHINTS](./jet-spacehints-structure.md) structure for default sequential index.</span></span>

<span data-ttu-id="02a8d-185">**pSeqSpacehints** 是在 Windows 7 中引進的。</span><span class="sxs-lookup"><span data-stu-id="02a8d-185">**pSeqSpacehints** was introduced in Windows 7.</span></span>

<span data-ttu-id="02a8d-186">**pLVSpacehints**</span><span class="sxs-lookup"><span data-stu-id="02a8d-186">**pLVSpacehints**</span></span>

<span data-ttu-id="02a8d-187">分隔 Long 值樹狀結構的 [JET_SPACEHINTS](./jet-spacehints-structure.md) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="02a8d-187">A pointer to a [JET_SPACEHINTS](./jet-spacehints-structure.md) structure for a Separated Long Value tree.</span></span>

<span data-ttu-id="02a8d-188">**pLVSpacehints** 是在 Windows 7 中引進的。</span><span class="sxs-lookup"><span data-stu-id="02a8d-188">**pLVSpacehints** was introduced in Windows 7.</span></span>

<span data-ttu-id="02a8d-189">**cbSeparateLV**</span><span class="sxs-lookup"><span data-stu-id="02a8d-189">**cbSeparateLV**</span></span>

<span data-ttu-id="02a8d-190">將內建的 LV 與主要記錄分開的大小。</span><span class="sxs-lookup"><span data-stu-id="02a8d-190">The size to separate an intrinsic LV from the primary record.</span></span> <span data-ttu-id="02a8d-191">分隔的 LV 樹狀結構的任何 long 值 c 結構。</span><span class="sxs-lookup"><span data-stu-id="02a8d-191">Any long-value c structure for a Separated LV tree.</span></span> <span data-ttu-id="02a8d-192">如需詳細資訊，請參閱 ng- [JET_SPACEHINTS](./jet-spacehints-structure.md)中的值。</span><span class="sxs-lookup"><span data-stu-id="02a8d-192">For more information, see ng-value in [JET_SPACEHINTS](./jet-spacehints-structure.md).</span></span> <span data-ttu-id="02a8d-193">如果記錄變得太大，則小於此值的 Long 值資料行可能會分開。</span><span class="sxs-lookup"><span data-stu-id="02a8d-193">Long-value columns smaller than this value may be separated if the record becomes too large.</span></span>

<span data-ttu-id="02a8d-194">**cbSeparateLV** 是在 Windows 7 中引進的。</span><span class="sxs-lookup"><span data-stu-id="02a8d-194">**cbSeparateLV** was introduced in Windows 7.</span></span>

<span data-ttu-id="02a8d-195">**tableid**</span><span class="sxs-lookup"><span data-stu-id="02a8d-195">**tableid**</span></span>

<span data-ttu-id="02a8d-196">如果 API 呼叫成功，則為包含新資料表之 [JET_TABLEID](./jet-tableid.md) 的輸出欄位。</span><span class="sxs-lookup"><span data-stu-id="02a8d-196">An output field that holds the [JET_TABLEID](./jet-tableid.md) of the new table if the API call succeeds.</span></span> <span data-ttu-id="02a8d-197">如果 API 呼叫失敗，則值為未定義。</span><span class="sxs-lookup"><span data-stu-id="02a8d-197">If the API call fails, the value is undefined.</span></span> <span data-ttu-id="02a8d-198">此資料表會以獨佔方式開啟。</span><span class="sxs-lookup"><span data-stu-id="02a8d-198">This table is opened exclusively.</span></span>

<span data-ttu-id="02a8d-199">**到尚未建立**</span><span class="sxs-lookup"><span data-stu-id="02a8d-199">**cCreated**</span></span>

<span data-ttu-id="02a8d-200">輸出欄位，其中包含 API 呼叫成功時所建立的物件計數。</span><span class="sxs-lookup"><span data-stu-id="02a8d-200">An output field that contains the count of objects that are created if the API call succeeds.</span></span> <span data-ttu-id="02a8d-201">如果 API 呼叫失敗，則值為未定義。</span><span class="sxs-lookup"><span data-stu-id="02a8d-201">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="02a8d-202">所建立的物件計數等於已成功建立之資料行、資料表和索引的總和。</span><span class="sxs-lookup"><span data-stu-id="02a8d-202">The count of objects that are created is equal to the sum of columns, tables, and indexes that are successfully created.</span></span>

### <a name="requirements"></a><span data-ttu-id="02a8d-203">規格需求</span><span class="sxs-lookup"><span data-stu-id="02a8d-203">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02a8d-204"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="02a8d-204"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="02a8d-205">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="02a8d-205">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02a8d-206"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="02a8d-206"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="02a8d-207">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="02a8d-207">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02a8d-208"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="02a8d-208"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="02a8d-209">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="02a8d-209">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02a8d-210"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="02a8d-210"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="02a8d-211">實作為 <strong>JET_TABLECREATE3_W</strong> (Unicode) 和 <strong>JET_TABLECREATE3_A</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="02a8d-211">Implemented as <strong>JET_TABLECREATE3_W</strong> (Unicode) and <strong>JET_TABLECREATE3_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="02a8d-212">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02a8d-212">See also</span></span>

[<span data-ttu-id="02a8d-213">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="02a8d-213">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="02a8d-214">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="02a8d-214">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="02a8d-215">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="02a8d-215">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="02a8d-216">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="02a8d-216">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="02a8d-217">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="02a8d-217">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="02a8d-218">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="02a8d-218">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="02a8d-219">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="02a8d-219">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="02a8d-220">JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="02a8d-220">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="02a8d-221">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="02a8d-221">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="02a8d-222">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="02a8d-222">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="02a8d-223">JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="02a8d-223">JetDefragment2</span></span>](./jetdefragment2-function.md)
