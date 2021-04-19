---
description: 深入瞭解： JET_COLUMNBASE 結構
title: JET_COLUMNBASE 結構
TOCTitle: JET_COLUMNBASE Structure
ms:assetid: 171275c3-966d-409d-ad20-a8f240f7500d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269194(v=EXCHG.10)
ms:contentKeyID: 32765497
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
ms.openlocfilehash: 9276c36a08a429f44568b3a909af77f5ae038c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989993"
---
# <a name="jet_columnbase-structure"></a><span data-ttu-id="1ed7d-103">JET_COLUMNBASE 結構</span><span class="sxs-lookup"><span data-stu-id="1ed7d-103">JET_COLUMNBASE Structure</span></span>


<span data-ttu-id="1ed7d-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1ed7d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columnbase-structure"></a><span data-ttu-id="1ed7d-105">JET_COLUMNBASE 結構</span><span class="sxs-lookup"><span data-stu-id="1ed7d-105">JET_COLUMNBASE Structure</span></span>

<span data-ttu-id="1ed7d-106">**JET_COLUMNBASE** 結構描述基底資料行的參數。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-106">The **JET_COLUMNBASE** structure describes the parameters of a base column.</span></span> <span data-ttu-id="1ed7d-107">[JetGetColumnInfo](./jetgetcolumninfo-function.md)和 [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)函數會使用 **JET_COLUMNBASE** 結構。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-107">The [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) functions use the **JET_COLUMNBASE** structure.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wFiller;
      unsigned long cbMax;
      JET_GRBIT grbit;
      tchar szBaseTableName[256];
      tchar szBaseColumnName[256];
    } JET_COLUMNBASE;
```

### <a name="members"></a><span data-ttu-id="1ed7d-108">成員</span><span class="sxs-lookup"><span data-stu-id="1ed7d-108">Members</span></span>

<span data-ttu-id="1ed7d-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="1ed7d-109">**cbStruct**</span></span>

<span data-ttu-id="1ed7d-110">此結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-110">The size of this structure, in bytes.</span></span> <span data-ttu-id="1ed7d-111">將 **cbStruct** 設定為 sizeof ( JET_COLUMNBASE ) 。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-111">Set **cbStruct** to sizeof( JET_COLUMNBASE ).</span></span>

<span data-ttu-id="1ed7d-112">**columnid**</span><span class="sxs-lookup"><span data-stu-id="1ed7d-112">**columnid**</span></span>

<span data-ttu-id="1ed7d-113">保留的。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-113">Reserved.</span></span> <span data-ttu-id="1ed7d-114">將 **columnid** 設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-114">Set **columnid** to 0 (zero).</span></span>

<span data-ttu-id="1ed7d-115">**coltyp**</span><span class="sxs-lookup"><span data-stu-id="1ed7d-115">**coltyp**</span></span>

<span data-ttu-id="1ed7d-116">資料行的類型 (例如，文字、二進位或數值) 。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-116">The type of the column (for example, text, binary, or numerical).</span></span> <span data-ttu-id="1ed7d-117">如需詳細資訊，請參閱 [JET_COLTYP](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-117">For more information, see [JET_COLTYP](./jet-coltyp.md).</span></span>

<span data-ttu-id="1ed7d-118">**wCountry**</span><span class="sxs-lookup"><span data-stu-id="1ed7d-118">**wCountry**</span></span>

<span data-ttu-id="1ed7d-119">保留的。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-119">Reserved.</span></span> <span data-ttu-id="1ed7d-120">設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-120">Set to 0 (zero).</span></span>

<span data-ttu-id="1ed7d-121">**langid**</span><span class="sxs-lookup"><span data-stu-id="1ed7d-121">**langid**</span></span>

<span data-ttu-id="1ed7d-122">保留的。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-122">Reserved.</span></span> <span data-ttu-id="1ed7d-123">設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-123">Set to 0 (zero).</span></span>

<span data-ttu-id="1ed7d-124">**cp**</span><span class="sxs-lookup"><span data-stu-id="1ed7d-124">**cp**</span></span>

<span data-ttu-id="1ed7d-125">資料行的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-125">The code page for the column.</span></span> <span data-ttu-id="1ed7d-126">Text 資料行的唯一有效值是英文 (1252) 和 Unicode (1200) 。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-126">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="1ed7d-127">值為零表示預設將會使用 (英文、1252) 。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-127">A value of zero means the default will be used (English, 1252).</span></span> <span data-ttu-id="1ed7d-128">如果資料行不是文字資料行，則字碼頁會自動設為零。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-128">If the column is not a text column, the code page is automatically set to zero.</span></span>

<span data-ttu-id="1ed7d-129">**wFiller**</span><span class="sxs-lookup"><span data-stu-id="1ed7d-129">**wFiller**</span></span>

<span data-ttu-id="1ed7d-130">保留的。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-130">Reserved.</span></span> <span data-ttu-id="1ed7d-131">設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-131">Set to 0 (zero).</span></span>

<span data-ttu-id="1ed7d-132">**cbMax**</span><span class="sxs-lookup"><span data-stu-id="1ed7d-132">**cbMax**</span></span>

<span data-ttu-id="1ed7d-133">可變長度資料行的最大長度（以位元組為單位），或固定長度資料行的實際長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-133">The maximum length, in bytes, of a variable-length column, or the actual length, in bytes, of a fixed-length column.</span></span>

<span data-ttu-id="1ed7d-134">**grbit**</span><span class="sxs-lookup"><span data-stu-id="1ed7d-134">**grbit**</span></span>

<span data-ttu-id="1ed7d-135">包含零或多個下列值的資料行選項。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-135">Options for the column, including zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ed7d-136">值</span><span class="sxs-lookup"><span data-stu-id="1ed7d-136">Value</span></span></p></th>
<th><p><span data-ttu-id="1ed7d-137">意義</span><span class="sxs-lookup"><span data-stu-id="1ed7d-137">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ed7d-138">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="1ed7d-138">JET_bitColumnFixed</span></span></p></td>
<td><p><span data-ttu-id="1ed7d-139">資料行是固定的，而且會佔用資料列中相同數量的空間，不論它包含多少資料。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-139">The column is fixed and occupies the same amount of space in a row regardless of how much data it contains.</span></span> <span data-ttu-id="1ed7d-140">JET_bitColumnFixed 無法與 JET_bitColumnTagged 合併，且當 <strong>coltyp</strong> 成員設定為 <strong>JET_coltypLongText</strong> 或 <strong>JET_coltypLongBinary</strong>時無法使用。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-140">JET_bitColumnFixed cannot be combined with JET_bitColumnTagged, and cannot be used when the <strong>coltyp</strong> member is set to <strong>JET_coltypLongText</strong> or <strong>JET_coltypLongBinary</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ed7d-141">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="1ed7d-141">JET_bitColumnTagged</span></span></p></td>
<td><p><span data-ttu-id="1ed7d-142">只有當資料行包含資料時，資料行才會被標記並在資料庫中佔用空間。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-142">The column is tagged and occupies space in the database only if it contains data.</span></span> <span data-ttu-id="1ed7d-143">JET_bitColumnTagged 無法與 JET_bitColumnFixed、JET_bitColumnVersion 或 JET_bitColumnEscrowUpdate 合併。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-143">JET_bitColumnTagged cannot be combined with JET_bitColumnFixed, JET_bitColumnVersion, or JET_bitColumnEscrowUpdate.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ed7d-144">JET_bitColumnNotNull</span><span class="sxs-lookup"><span data-stu-id="1ed7d-144">JET_bitColumnNotNULL</span></span></p></td>
<td><p><span data-ttu-id="1ed7d-145">資料行不得設定為 <strong>Null</strong> 值。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-145">The column must not be set to a <strong>NULL</strong> value.</span></span></p>
<p><span data-ttu-id="1ed7d-146">JET_bitColumnNotNull 無法與 JET_bitColumnUserDefinedDefault 結合。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-146">JET_bitColumnNotNULL cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ed7d-147">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="1ed7d-147">JET_bitColumnVersion</span></span></p></td>
<td><p><span data-ttu-id="1ed7d-148">此資料行是版本資料行，可指定資料列的版本。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-148">The column is a version column that specifies the version of the row.</span></span> <span data-ttu-id="1ed7d-149">此資料行的值從零開始，而且會針對每個資料列更新自動遞增。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-149">The value of this column starts at zero and is automatically incremented for each update of the row.</span></span></p>
<p><span data-ttu-id="1ed7d-150">只有當 <strong>coltyp</strong> 成員設定為 <strong>JET_coltypLong</strong> ，而且無法與 JET_bitColumnAutoincrement、JET_bitColumnEscrowUpdate、JET_bitColumnTagged 或 JET_bitColumnUserDefinedDefault 合併時，才可以使用 JET_bitColumnVersion。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-150">JET_bitColumnVersion can be used only when the <strong>coltyp</strong> member is set to <strong>JET_coltypLong</strong> and cannot be combined with JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, JET_bitColumnTagged, or JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ed7d-151">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="1ed7d-151">JET_bitColumnAutoincrement</span></span></p></td>
<td><p><span data-ttu-id="1ed7d-152">資料行會自動遞增。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-152">The column is automatically incremented.</span></span> <span data-ttu-id="1ed7d-153">此數位是遞增的數位，而且在資料表中保證是唯一的。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-153">The number is an increasing number, and is guaranteed to be unique within a table.</span></span> <span data-ttu-id="1ed7d-154">不過，數位可能不是連續的。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-154">The numbers, however, may not be sequential.</span></span> <span data-ttu-id="1ed7d-155">例如，如果將五個數據列插入資料表中，自動遞增的資料行會包含值 {1，2，6，7，8}。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-155">For example, if five rows are inserted into a table, the automatically incremented column could contain the values { 1, 2, 6, 7, 8 }.</span></span></p>
<p><span data-ttu-id="1ed7d-156">只有當 <strong>coltyp</strong> 成員設定為 <strong>JET_coltypLong</strong> 或 <strong>JET_coltypCurrency</strong> ，且不能與 JET_bitColumnEscrowUpdate、JET_bitColumnUserDefinedDefault 或 JET_bitColumnVersion 合併時，才可以使用 JET_bitColumnAutoincrement。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-156">JET_bitColumnAutoincrement can be used only when the <strong>coltyp</strong> member is set to <strong>JET_coltypLong</strong> or <strong>JET_coltypCurrency</strong> and cannot be combined with JET_bitColumnEscrowUpdate, JET_bitColumnUserDefinedDefault, or JET_bitColumnVersion.</span></span></p>
<p><span data-ttu-id="1ed7d-157"><strong>Windows 2000：  </strong>只有當 <strong>coltyp</strong> 成員設定為 <strong>JET_coltypLong</strong>時，才可以使用 JET_bitColumnVersion。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-157"><strong>Windows 2000:  </strong>JET_bitColumnVersion can be used only when the <strong>coltyp</strong> member is set to <strong>JET_coltypLong</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ed7d-158">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="1ed7d-158">JET_bitColumnUpdatable</span></span></p></td>
<td><p><span data-ttu-id="1ed7d-159">只對 <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>的呼叫有效。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-159">Valid only for calls to <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span></span> <span data-ttu-id="1ed7d-160">JET_bitColumnUpdatable 無法與 JET_bitColumnUserDefinedDefault 結合。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-160">JET_bitColumnUpdatable cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ed7d-161">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="1ed7d-161">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="1ed7d-162">只對 <a href="gg294118(v=exchg.10).md">JetOpenTable</a>的呼叫有效。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-162">Valid only on calls to <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ed7d-163">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="1ed7d-163">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="1ed7d-164">只對 <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>的呼叫有效。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-164">Valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ed7d-165">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="1ed7d-165">JET_bitColumnMultiValued</span></span></p></td>
<td><p><span data-ttu-id="1ed7d-166">此資料行可以是多重值。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-166">The column can be multi-valued.</span></span> <span data-ttu-id="1ed7d-167">多重值資料行可以有零個、一個或多個相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-167">A multi-valued column can have zero, one, or more values associated with it.</span></span> <span data-ttu-id="1ed7d-168">多重值資料行中的各種值是由各種結構之 <strong>itagSequence</strong> 成員中的數位所識別，例如 <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>、 <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>、 <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>、 <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a> <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-168">The various values in a multi-valued column are identified by a number in the <strong>itagSequence</strong> member of various structures, for example, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="1ed7d-169">多重值資料行必須是標記的資料行;也就是說，它們可能不是固定長度或可變長度的資料行。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-169">Multi-valued columns must be tagged columns; that is, they may not be fixed-length or variable-length columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ed7d-170">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="1ed7d-170">JET_bitColumnEscrowUpdate</span></span></p></td>
<td><p><span data-ttu-id="1ed7d-171">指定資料行是一種可由不同會話與 <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> 同時更新的交易式更新資料行，而且將具有交易一致性。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-171">Specifies that a column is an escrow update column that can be updated concurrently by different sessions with <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> and will have transactional consistency.</span></span></p>
<ul>
<li><p><span data-ttu-id="1ed7d-172">只有當資料表是空的時，才可以建立「正在進行」的更新資料行。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-172">An escrow update column can be created only when the table is empty.</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="1ed7d-173">若為使用中的更新資料行， <strong>coltyp</strong> 成員必須設定為 <strong>JET_coltypLong。</strong></span><span class="sxs-lookup"><span data-stu-id="1ed7d-173">For an escrow update column, the <strong>coltyp</strong> member must be set to <strong>JET_coltypLong.</strong></span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="1ed7d-174">「正在進行」的更新資料行必須有預設值 (<strong>cbDefault</strong> 必須是正數) 。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-174">An escrow update column must have a default value (that is <strong>cbDefault</strong> must be positive).</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="1ed7d-175">JET_bitColumnEscrowUpdate 無法與 JET_bitColumnTagged、JET_bitColumnVersion 或 JET_bitColumnAutoincrement 合併。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-175">JET_bitColumnEscrowUpdate cannot be combined with JET_bitColumnTagged, JET_bitColumnVersion, or JET_bitColumnAutoincrement.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ed7d-176">JET_bitColumnUnversioned</span><span class="sxs-lookup"><span data-stu-id="1ed7d-176">JET_bitColumnUnversioned</span></span></p></td>
<td><p><span data-ttu-id="1ed7d-177">建立資料行時沒有版本號碼。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-177">The column is created without a version number.</span></span> <span data-ttu-id="1ed7d-178">這表示嘗試加入具有相同名稱之資料行的其他交易將會失敗。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-178">This means that other transactions attempting to add a column with the same name will fail.</span></span> <span data-ttu-id="1ed7d-179">JET_bitColumnUnversioned 只能與 <a href="gg294122(v=exchg.10).md">JetAddColumn</a>搭配使用。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-179">JET_bitColumnUnversioned is used only with <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span></span> <span data-ttu-id="1ed7d-180">它不能用在交易內。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-180">It cannot be used within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ed7d-181">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="1ed7d-181">JET_bitColumnMaybeNull</span></span></p></td>
<td><p><span data-ttu-id="1ed7d-182">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-182">Reserved for future use.</span></span></p>
<p><span data-ttu-id="1ed7d-183">JET_bitColumnMaybeNull 無法與 JET_bitColumnUserDefinedDefault 結合。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-183">JET_bitColumnMaybeNull cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ed7d-184">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="1ed7d-184">JET_bitColumnFinalize</span></span></p></td>
<td><p><span data-ttu-id="1ed7d-185">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-185">Do not use.</span></span> <span data-ttu-id="1ed7d-186">請改用 JET_bitColumnDeleteOnZero。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-186">Use JET_bitColumnDeleteOnZero instead.</span></span></p>
<p><span data-ttu-id="1ed7d-187">可以完成資料行。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-187">The column can be finalized.</span></span> <span data-ttu-id="1ed7d-188">可以完成的資料行是一種可在資料行到達零時，會刪除資料列的「正在進行的」更新資料行。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-188">A column that can be finalized is an escrow update column that causes the row to be deleted when the column reaches zero.</span></span> <span data-ttu-id="1ed7d-189">未來的版本可能會改為叫用回呼函式 (請參閱 <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>) 。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-189">Future versions may invoke a callback function instead (See <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>).</span></span> <span data-ttu-id="1ed7d-190">可以完成的資料行必須是「託管更新」資料行。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-190">A column that can be finalized must be an escrow update column.</span></span> <span data-ttu-id="1ed7d-191">JET_bitColumnFinalize 無法與 JET_bitColumnUserDefinedDefault 結合。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-191">JET_bitColumnFinalize cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ed7d-192">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="1ed7d-192">JET_bitColumnUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="1ed7d-193">資料行的預設值將由回呼函數提供。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-193">The default value for a column will be provided by a callback function.</span></span> <span data-ttu-id="1ed7d-194">請參閱 <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-194">See <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="1ed7d-195">具有使用者定義預設值的資料行必須是標記的資料行。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-195">A column that has a user-defined default must be a tagged column.</span></span> <span data-ttu-id="1ed7d-196">如果指定 JET_bitColumnUserDefinedDefault， <strong>pvDefault</strong> 必須指向 <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> 結構，而且 <strong>cbDefault</strong> 必須設定為 sizeof ( JET_USERDEFINEDDEFAULT ) 。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-196">If JET_bitColumnUserDefinedDefault is specified, the <strong>pvDefault</strong> must point to a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure, and <strong>cbDefault</strong> must be set to sizeof( JET_USERDEFINEDDEFAULT ).</span></span></p>
<p><span data-ttu-id="1ed7d-197">JET_bitColumnUserDefinedDefault 無法與 JET_bitColumnFixed、JET_bitColumnNotNull、JET_bitColumnVersion、JET_bitColumnAutoincrement、JET_bitColumnUpdatable、JET_bitColumnEscrowUpdate、JET_bitColumnFinalize、JET_bitColumnDeleteOnZero 或 JET_bitColumnMaybeNull 合併。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-197">JET_bitColumnUserDefinedDefault cannot be combined with JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero, or JET_bitColumnMaybeNull.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ed7d-198">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="1ed7d-198">JET_bitColumnDeleteOnZero</span></span></p></td>
<td><p><span data-ttu-id="1ed7d-199">此資料行是「正在進行的更新」資料行，當它到達零時，將會刪除記錄。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-199">The column is an escrow update column and when it reaches zero, the record will be deleted.</span></span> <span data-ttu-id="1ed7d-200">零刪除資料行的常見用法是參考計數位段。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-200">A common use for delete-on-zero columns is as reference count fields.</span></span> <span data-ttu-id="1ed7d-201">當參考的數目落為零時，就會刪除記錄。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-201">When the number of references fall to zero, the record is deleted.</span></span> <span data-ttu-id="1ed7d-202">零刪除資料行必須是「託管更新」資料行。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-202">A delete-on-zero column must be an escrow update column.</span></span></p>
<p><span data-ttu-id="1ed7d-203">JET_bitColumnDeleteOnZero 取代 JET_bitColumnFinalize。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-203">JET_bitColumnDeleteOnZero replaces JET_bitColumnFinalize.</span></span></p>
<p><span data-ttu-id="1ed7d-204">JET_bitColumnDeleteOnZero 無法與 JET_bitColumnFinalize 或 JET_bitColumnUserDefinedDefault 結合，也不能與使用者定義的預設資料行一起使用。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-204">JET_bitColumnDeleteOnZero cannot be combined with JET_bitColumnFinalize or JET_bitColumnUserDefinedDefault, and cannot be used with user-defined default columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1ed7d-205">**szBaseTableName**</span><span class="sxs-lookup"><span data-stu-id="1ed7d-205">**szBaseTableName**</span></span>

<span data-ttu-id="1ed7d-206">目前資料表從中繼承其 DDL 的資料表。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-206">The table from which the current table inherits its DDL.</span></span>

<span data-ttu-id="1ed7d-207">**szBaseColumnName**</span><span class="sxs-lookup"><span data-stu-id="1ed7d-207">**szBaseColumnName**</span></span>

<span data-ttu-id="1ed7d-208">範本資料表中的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-208">The name of the column in the template table.</span></span>

### <a name="remarks"></a><span data-ttu-id="1ed7d-209">備註</span><span class="sxs-lookup"><span data-stu-id="1ed7d-209">Remarks</span></span>

<span data-ttu-id="1ed7d-210">**JET_COLUMNBASE** 包含與 [JET_COLUMNDEF](./jet-columndef-structure.md)大部分相同的資訊，但它會在) 使用階層式 DDL 時，加入字串欄位來描述基表 (。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-210">**JET_COLUMNBASE** contains much of the same information as [JET_COLUMNDEF](./jet-columndef-structure.md), but it adds string fields to describe the base table (if a hierarchical DDL was used).</span></span>

### <a name="requirements"></a><span data-ttu-id="1ed7d-211">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ed7d-211">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ed7d-212"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="1ed7d-212"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1ed7d-213">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-213">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ed7d-214"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="1ed7d-214"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1ed7d-215">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-215">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ed7d-216"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="1ed7d-216"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1ed7d-217">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-217">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ed7d-218"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="1ed7d-218"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="1ed7d-219">實作為 <strong>JET_COLUMNBASE_W</strong> (Unicode) 和 <strong>JET_COLUMNBASE_A</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="1ed7d-219">Implemented as <strong>JET_COLUMNBASE_W</strong> (Unicode) and <strong>JET_COLUMNBASE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="1ed7d-220">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ed7d-220">See Also</span></span>

[<span data-ttu-id="1ed7d-221">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="1ed7d-221">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="1ed7d-222">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="1ed7d-222">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="1ed7d-223">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="1ed7d-223">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="1ed7d-224">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="1ed7d-224">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="1ed7d-225">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="1ed7d-225">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="1ed7d-226">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="1ed7d-226">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="1ed7d-227">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="1ed7d-227">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="1ed7d-228">JET_USERDEFINEDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="1ed7d-228">JET_USERDEFINEDDEFAULT</span></span>](./jet-userdefineddefault-structure.md)  
[<span data-ttu-id="1ed7d-229">JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="1ed7d-229">JetGetColumnInfo</span></span>](./jetgetcolumninfo-function.md)  
[<span data-ttu-id="1ed7d-230">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="1ed7d-230">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)  
[<span data-ttu-id="1ed7d-231">JetRenameColumn</span><span class="sxs-lookup"><span data-stu-id="1ed7d-231">JetRenameColumn</span></span>](./jetrenamecolumn-function.md)
