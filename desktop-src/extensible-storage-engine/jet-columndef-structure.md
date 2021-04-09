---
description: 深入瞭解： JET_COLUMNDEF 結構
title: JET_COLUMNDEF 結構
TOCTitle: JET_COLUMNDEF Structure
ms:assetid: ee1fc473-bff5-438e-98ae-247de12e76f9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294130(v=EXCHG.10)
ms:contentKeyID: 32765744
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
ms.openlocfilehash: c541b5801c95f4b269e33360f5ffa2404ff8fc06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945365"
---
# <a name="jet_columndef-structure"></a><span data-ttu-id="83f29-103">JET_COLUMNDEF 結構</span><span class="sxs-lookup"><span data-stu-id="83f29-103">JET_COLUMNDEF Structure</span></span>


<span data-ttu-id="83f29-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="83f29-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columndef-structure"></a><span data-ttu-id="83f29-105">JET_COLUMNDEF 結構</span><span class="sxs-lookup"><span data-stu-id="83f29-105">JET_COLUMNDEF Structure</span></span>

<span data-ttu-id="83f29-106">**JET_COLUMNDEF** 結構會定義可以儲存在資料行中的資料。</span><span class="sxs-lookup"><span data-stu-id="83f29-106">The **JET_COLUMNDEF** structure defines the data that can be stored in a column.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wCollate;
      unsigned long cbMax;
      JET_GRBIT grbit;
    } JET_COLUMNDEF;
```

### <a name="members"></a><span data-ttu-id="83f29-107">成員</span><span class="sxs-lookup"><span data-stu-id="83f29-107">Members</span></span>

<span data-ttu-id="83f29-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="83f29-108">**cbStruct**</span></span>

<span data-ttu-id="83f29-109">結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="83f29-109">The size of the structure, in bytes.</span></span> <span data-ttu-id="83f29-110">它必須設定為 sizeof ( JET_COLUMNDEF) 。</span><span class="sxs-lookup"><span data-stu-id="83f29-110">It must be set to sizeof( JET_COLUMNDEF).</span></span>

<span data-ttu-id="83f29-111">**columnid**</span><span class="sxs-lookup"><span data-stu-id="83f29-111">**columnid**</span></span>

<span data-ttu-id="83f29-112">保留的。</span><span class="sxs-lookup"><span data-stu-id="83f29-112">Reserved.</span></span> <span data-ttu-id="83f29-113">**columnid** 必須設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="83f29-113">**columnid** must be set to 0 (zero).</span></span>

<span data-ttu-id="83f29-114">**coltyp**</span><span class="sxs-lookup"><span data-stu-id="83f29-114">**coltyp**</span></span>

<span data-ttu-id="83f29-115">資料行的類型 (例如，文字、二進位或數值) 。</span><span class="sxs-lookup"><span data-stu-id="83f29-115">The type of the column (for example, text, binary, or numerical).</span></span> <span data-ttu-id="83f29-116">如需詳細資訊，請參閱 [JET_COLTYP](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="83f29-116">For more information, see [JET_COLTYP](./jet-coltyp.md).</span></span>

<span data-ttu-id="83f29-117">**wCountry**</span><span class="sxs-lookup"><span data-stu-id="83f29-117">**wCountry**</span></span>

<span data-ttu-id="83f29-118">保留的。</span><span class="sxs-lookup"><span data-stu-id="83f29-118">Reserved.</span></span> <span data-ttu-id="83f29-119">**wCountry** 必須設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="83f29-119">**wCountry** must be set to 0 (zero).</span></span>

<span data-ttu-id="83f29-120">**langid**</span><span class="sxs-lookup"><span data-stu-id="83f29-120">**langid**</span></span>

<span data-ttu-id="83f29-121">已過時。</span><span class="sxs-lookup"><span data-stu-id="83f29-121">Obsolete.</span></span> <span data-ttu-id="83f29-122">**langid** 應該設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="83f29-122">**langid** should be set to 0 (zero).</span></span>

<span data-ttu-id="83f29-123">**cp**</span><span class="sxs-lookup"><span data-stu-id="83f29-123">**cp**</span></span>

<span data-ttu-id="83f29-124">資料行的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="83f29-124">The code page for the column.</span></span> <span data-ttu-id="83f29-125">Text 資料行的唯一有效值是英文 (1252) 和 Unicode (1200) 。</span><span class="sxs-lookup"><span data-stu-id="83f29-125">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="83f29-126">值為零表示預設將會使用 (英文、1252) 。</span><span class="sxs-lookup"><span data-stu-id="83f29-126">A value of zero means the default will be used (English, 1252).</span></span> <span data-ttu-id="83f29-127">如果資料行不是文字資料行，則字碼頁會自動設為零。</span><span class="sxs-lookup"><span data-stu-id="83f29-127">If the column is not a text column, the code page automatically gets set to zero.</span></span>

<span data-ttu-id="83f29-128">**wCollate**</span><span class="sxs-lookup"><span data-stu-id="83f29-128">**wCollate**</span></span>

<span data-ttu-id="83f29-129">保留的。</span><span class="sxs-lookup"><span data-stu-id="83f29-129">Reserved.</span></span> <span data-ttu-id="83f29-130">**wCollate** 必須設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="83f29-130">**wCollate** must be set to 0 (zero).</span></span>

<span data-ttu-id="83f29-131">**cbMax**</span><span class="sxs-lookup"><span data-stu-id="83f29-131">**cbMax**</span></span>

<span data-ttu-id="83f29-132">可變長度資料行的最大長度（以位元組為單位），或固定長度資料行的長度。</span><span class="sxs-lookup"><span data-stu-id="83f29-132">The maximum length, in bytes, of a variable-length column, or the length of a fixed-length column.</span></span>

<span data-ttu-id="83f29-133">**grbit**</span><span class="sxs-lookup"><span data-stu-id="83f29-133">**grbit**</span></span>

<span data-ttu-id="83f29-134">位群組，其中包含要用於此呼叫的選項，其中包含零或多個下列值。</span><span class="sxs-lookup"><span data-stu-id="83f29-134">A group of bits that contain the options to be used for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="83f29-135">值</span><span class="sxs-lookup"><span data-stu-id="83f29-135">Value</span></span></p></th>
<th><p><span data-ttu-id="83f29-136">意義</span><span class="sxs-lookup"><span data-stu-id="83f29-136">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="83f29-137">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="83f29-137">JET_bitColumnFixed</span></span></p></td>
<td><p><span data-ttu-id="83f29-138">將會修正此資料行。</span><span class="sxs-lookup"><span data-stu-id="83f29-138">The column will be fixed.</span></span> <span data-ttu-id="83f29-139">無論資料儲存在資料行中的資料量為何，它一律會使用資料列中相同數量的空間。</span><span class="sxs-lookup"><span data-stu-id="83f29-139">It will always use the same amount of space in a row, regardless of how much data is being stored in the column.</span></span> <span data-ttu-id="83f29-140">JET_bitColumnFixed 不能與 JET_bitColumnTagged 一起使用。</span><span class="sxs-lookup"><span data-stu-id="83f29-140">JET_bitColumnFixed cannot be used with JET_bitColumnTagged.</span></span> <span data-ttu-id="83f29-141">這個位不能搭配 <strong>JET_coltypLongText</strong> 和 <strong>JET_coltypLongBinary</strong>) 的 long 值 (使用。</span><span class="sxs-lookup"><span data-stu-id="83f29-141">This bit cannot be used with long values (that is <strong>JET_coltypLongText</strong> and <strong>JET_coltypLongBinary</strong>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83f29-142">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="83f29-142">JET_bitColumnTagged</span></span></p></td>
<td><p><span data-ttu-id="83f29-143">將會標記資料行。</span><span class="sxs-lookup"><span data-stu-id="83f29-143">The column will be tagged.</span></span> <span data-ttu-id="83f29-144">如果標記的資料行不包含資料，就不會佔用資料庫中的任何空間。</span><span class="sxs-lookup"><span data-stu-id="83f29-144">Tagged columns do not take up any space in the database if they do not contain data.</span></span> <span data-ttu-id="83f29-145">此位無法搭配 JET_bitColumnFixed 使用。</span><span class="sxs-lookup"><span data-stu-id="83f29-145">This bit cannot be used with JET_bitColumnFixed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83f29-146">JET_bitColumnNotNull</span><span class="sxs-lookup"><span data-stu-id="83f29-146">JET_bitColumnNotNULL</span></span></p></td>
<td><p><span data-ttu-id="83f29-147">資料行絕對不能設定為 Null 值。</span><span class="sxs-lookup"><span data-stu-id="83f29-147">The column must never be set to a NULL value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83f29-148">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="83f29-148">JET_bitColumnVersion</span></span></p></td>
<td><p><span data-ttu-id="83f29-149">此資料行是版本資料行，可指定資料列的版本。</span><span class="sxs-lookup"><span data-stu-id="83f29-149">The column is a version column that specifies the version of the row.</span></span> <span data-ttu-id="83f29-150">此資料行的值從零開始，而且會針對資料列上的每個更新自動遞增。</span><span class="sxs-lookup"><span data-stu-id="83f29-150">The value of this column starts at zero and will be automatically incremented for each update on the row.</span></span></p>
<p><span data-ttu-id="83f29-151">這個位只能套用至 <strong>JET_coltypLong</strong> 資料行。</span><span class="sxs-lookup"><span data-stu-id="83f29-151">This bit can only be applied to <strong>JET_coltypLong</strong> columns.</span></span> <span data-ttu-id="83f29-152">此位無法搭配 JET_bitColumnAutoincrement、JET_bitColumnEscrowUpdate 或 JET_bitColumnTagged 使用。</span><span class="sxs-lookup"><span data-stu-id="83f29-152">This bit cannot be used with JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, or JET_bitColumnTagged.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83f29-153">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="83f29-153">JET_bitColumnAutoincrement</span></span></p></td>
<td><p><span data-ttu-id="83f29-154">將會自動遞增資料行。</span><span class="sxs-lookup"><span data-stu-id="83f29-154">The column will automatically be incremented.</span></span> <span data-ttu-id="83f29-155">此數位是遞增的數位，而且在資料表中保證是唯一的。</span><span class="sxs-lookup"><span data-stu-id="83f29-155">The number is an increasing number, and is guaranteed to be unique within a table.</span></span> <span data-ttu-id="83f29-156">不過，數位可能不是連續的。</span><span class="sxs-lookup"><span data-stu-id="83f29-156">The numbers, however, might not be continuous.</span></span> <span data-ttu-id="83f29-157">例如，如果將五個數據列插入資料表中， &quot; 自動遞增 &quot; 資料行可以包含值 {1，2，6，7，8}。</span><span class="sxs-lookup"><span data-stu-id="83f29-157">For example, if five rows are inserted into a table, the &quot;autoincrement&quot; column could contain the values { 1, 2, 6, 7, 8 }.</span></span> <span data-ttu-id="83f29-158">這個位只能用在 <strong>JET_coltypLong</strong> 或 <strong>JET_coltypCurrency</strong>類型的資料行上。</span><span class="sxs-lookup"><span data-stu-id="83f29-158">This bit can only be used on columns of type <strong>JET_coltypLong</strong> or <strong>JET_coltypCurrency</strong>.</span></span></p>
<p><span data-ttu-id="83f29-159"><strong>Windows 2000：  </strong>在 Windows 2000 中，此位只能用在 <strong>JET_coltypLong</strong>類型的資料行上。</span><span class="sxs-lookup"><span data-stu-id="83f29-159"><strong>Windows 2000:  </strong>In Windows 2000, this bit can only be used on columns of type <strong>JET_coltypLong</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83f29-160">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="83f29-160">JET_bitColumnUpdatable</span></span></p></td>
<td><p><span data-ttu-id="83f29-161">只有對 <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>的呼叫才會有此位有效。</span><span class="sxs-lookup"><span data-stu-id="83f29-161">This bit is valid only on calls to <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83f29-162">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="83f29-162">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="83f29-163">只有對 <a href="gg294118(v=exchg.10).md">JetOpenTable</a>的呼叫才會有此位有效。</span><span class="sxs-lookup"><span data-stu-id="83f29-163">This bit is valid only on calls to <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83f29-164">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="83f29-164">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="83f29-165">只有對 <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>的呼叫才會有此位有效。</span><span class="sxs-lookup"><span data-stu-id="83f29-165">This bit is valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83f29-166">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="83f29-166">JET_bitColumnMultiValued</span></span></p></td>
<td><p><span data-ttu-id="83f29-167">此資料行可以是多重值。</span><span class="sxs-lookup"><span data-stu-id="83f29-167">The column can be multi-valued.</span></span> <span data-ttu-id="83f29-168">多重值資料行可以有零個、一個或多個相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="83f29-168">A multi-valued column can have zero, one, or more values associated with it.</span></span> <span data-ttu-id="83f29-169">多重值資料行中的各種值是由稱為 <strong>itagSequence</strong> 成員的數位所識別，其屬於各種結構，包括： <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>、 <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>、 <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>、 <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>和 <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>。</span><span class="sxs-lookup"><span data-stu-id="83f29-169">The various values in a multi-valued column are identified by a number called the <strong>itagSequence</strong> member, which belongs to various structures, including: <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, and <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="83f29-170">多重值資料行必須是標記的資料行;也就是說，它們不能是固定長度或可變長度的資料行。</span><span class="sxs-lookup"><span data-stu-id="83f29-170">Multi-valued columns must be tagged columns; that is, they cannot be fixed-length or variable-length columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83f29-171">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="83f29-171">JET_bitColumnEscrowUpdate</span></span></p></td>
<td><p><span data-ttu-id="83f29-172">指定資料行是「正在託管」更新資料行。</span><span class="sxs-lookup"><span data-stu-id="83f29-172">Specifies that a column is an escrow update column.</span></span> <span data-ttu-id="83f29-173">您可以透過 <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> 的不同會話同時更新交易的更新資料行，並將維持交易一致性。</span><span class="sxs-lookup"><span data-stu-id="83f29-173">An escrow update column can be updated concurrently by different sessions with <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> and will maintain transactional consistency.</span></span> <span data-ttu-id="83f29-174">[保管更新] 資料行也必須符合下列條件：</span><span class="sxs-lookup"><span data-stu-id="83f29-174">An escrow update column must also meet the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="83f29-175">只有當資料表是空的時，才可以建立「正在進行」的更新資料行。</span><span class="sxs-lookup"><span data-stu-id="83f29-175">An escrow update column can be created only when the table is empty.</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="83f29-176">「使用中」更新資料行的類型必須是 <strong>JET_coltypLong</strong>。</span><span class="sxs-lookup"><span data-stu-id="83f29-176">An escrow update column must be of type <strong>JET_coltypLong</strong>.</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="83f29-177">「正在進行」的更新資料行必須有預設值 (<strong>cbDefault</strong> 必須是正數) 。</span><span class="sxs-lookup"><span data-stu-id="83f29-177">An escrow update column must have a default value (that is <strong>cbDefault</strong> must be positive).</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="83f29-178">JET_bitColumnEscrowUpdate 不能與 JET_bitColumnTagged、JET_bitColumnVersion 或 JET_bitColumnAutoincrement 一起使用。</span><span class="sxs-lookup"><span data-stu-id="83f29-178">JET_bitColumnEscrowUpdate cannot be used in conjunction with JET_bitColumnTagged, JET_bitColumnVersion, or JET_bitColumnAutoincrement.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83f29-179">JET_bitColumnUnversioned</span><span class="sxs-lookup"><span data-stu-id="83f29-179">JET_bitColumnUnversioned</span></span></p></td>
<td><p><span data-ttu-id="83f29-180">將在中建立資料行，而不含版本資訊。</span><span class="sxs-lookup"><span data-stu-id="83f29-180">The column will be created in an without version information.</span></span> <span data-ttu-id="83f29-181">這表示嘗試加入具有相同名稱之資料行的其他交易將會失敗。</span><span class="sxs-lookup"><span data-stu-id="83f29-181">This means that other transactions that attempt to add a column with the same name will fail.</span></span> <span data-ttu-id="83f29-182">這個位只對 <a href="gg294122(v=exchg.10).md">JetAddColumn</a>很有用。</span><span class="sxs-lookup"><span data-stu-id="83f29-182">This bit is only useful with <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span></span> <span data-ttu-id="83f29-183">它不能用在交易內。</span><span class="sxs-lookup"><span data-stu-id="83f29-183">It cannot be used within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83f29-184">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="83f29-184">JET_bitColumnMaybeNull</span></span></p></td>
<td><p><span data-ttu-id="83f29-185">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="83f29-185">Reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83f29-186">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="83f29-186">JET_bitColumnFinalize</span></span></p></td>
<td><p><span data-ttu-id="83f29-187">使用 JET_bitColumnDeleteOnZero 而不是 JET_bitColumnFinalize。</span><span class="sxs-lookup"><span data-stu-id="83f29-187">Use JET_bitColumnDeleteOnZero instead of JET_bitColumnFinalize.</span></span> <span data-ttu-id="83f29-188">JET_bitColumnFinalize 可以完成資料行。</span><span class="sxs-lookup"><span data-stu-id="83f29-188">JET_bitColumnFinalize that a column can be finalized.</span></span> <span data-ttu-id="83f29-189">當可以完成的資料行具有到達零的「保管更新」資料行時，將會刪除該資料列。</span><span class="sxs-lookup"><span data-stu-id="83f29-189">When a column that can be finalized has an escrow update column that reaches zero, the row will be deleted.</span></span> <span data-ttu-id="83f29-190">未來的版本可能會改為叫用回呼函數 (如需詳細資訊，請參閱 <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>) 。</span><span class="sxs-lookup"><span data-stu-id="83f29-190">Future versions might invoke a callback function instead (For more information, see <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>).</span></span> <span data-ttu-id="83f29-191">可以完成的資料行必須是「託管更新」資料行。</span><span class="sxs-lookup"><span data-stu-id="83f29-191">A column that can be finalized must be an escrow update column.</span></span> <span data-ttu-id="83f29-192">JET_bitColumnFinalize 不能與 JET_bitColumnUserDefinedDefault 一起使用。</span><span class="sxs-lookup"><span data-stu-id="83f29-192">JET_bitColumnFinalize cannot be used with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83f29-193">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="83f29-193">JET_bitColumnUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="83f29-194">資料行的預設值將由回呼函數提供。</span><span class="sxs-lookup"><span data-stu-id="83f29-194">The default value for a column will be provided by a callback function.</span></span> <span data-ttu-id="83f29-195">請參閱 <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>。</span><span class="sxs-lookup"><span data-stu-id="83f29-195">See <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="83f29-196">具有使用者定義預設值的資料行必須是標記的資料行。</span><span class="sxs-lookup"><span data-stu-id="83f29-196">A column that has a user-defined default must be a tagged column.</span></span> <span data-ttu-id="83f29-197">指定 JET_bitColumnUserDefinedDefault 表示 <strong>pvDefault</strong> 必須指向 <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> 結構，而且 <strong>cbDefault</strong> 必須設定為 sizeof ( <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> ) 。</span><span class="sxs-lookup"><span data-stu-id="83f29-197">Specifying JET_bitColumnUserDefinedDefault means that <strong>pvDefault</strong> must point to a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure, and <strong>cbDefault</strong> must be set to sizeof( <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> ).</span></span></p>
<ul>
<li><p><span data-ttu-id="83f29-198">JET_bitColumnUserDefinedDefault 不能與 JET_bitColumnFixed、JET_bitColumnNotNull、JET_bitColumnVersion、JET_bitColumnAutoincrement、JET_bitColumnUpdatable、JET_bitColumnEscrowUpdate、JET_bitColumnFinalize、JET_bitColumnDeleteOnZero 或 JET_bitColumnMaybeNull 一起使用。</span><span class="sxs-lookup"><span data-stu-id="83f29-198">JET_bitColumnUserDefinedDefault cannot be used in conjunction with JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero, or JET_bitColumnMaybeNull.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83f29-199">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="83f29-199">JET_bitColumnDeleteOnZero</span></span></p></td>
<td><p><span data-ttu-id="83f29-200">此資料行是「正在進行的更新」資料行，當它到達零時，將會刪除記錄。</span><span class="sxs-lookup"><span data-stu-id="83f29-200">The column is an escrow update column, and when it reaches zero, the record will be deleted.</span></span> <span data-ttu-id="83f29-201">可以完成之資料行的常見用法是使用它做為參考計數位段，而且當欄位到達零時，就會刪除記錄。</span><span class="sxs-lookup"><span data-stu-id="83f29-201">A common use for a column that can be finalized is to use it as a reference count field, and when the field reaches zero the record gets deleted.</span></span> <span data-ttu-id="83f29-202">JET_bitColumnDeleteOnZero 與 JET_bitColumnFinalize 相關。</span><span class="sxs-lookup"><span data-stu-id="83f29-202">JET_bitColumnDeleteOnZero is related to JET_bitColumnFinalize.</span></span> <span data-ttu-id="83f29-203">零刪除資料行必須是「託管更新」資料行。</span><span class="sxs-lookup"><span data-stu-id="83f29-203">A Delete-on-zero column must be an escrow update column.</span></span> <span data-ttu-id="83f29-204">JET_bitColumnDeleteOnZero 不能與 JET_bitColumnFinalize 一起使用。</span><span class="sxs-lookup"><span data-stu-id="83f29-204">JET_bitColumnDeleteOnZero cannot be used with JET_bitColumnFinalize.</span></span> <span data-ttu-id="83f29-205">JET_bitColumnDeleteOnZero 不能與使用者定義的預設資料行一起使用。</span><span class="sxs-lookup"><span data-stu-id="83f29-205">JET_bitColumnDeleteOnZero cannot be used with user defined default columns.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="83f29-206">規格需求</span><span class="sxs-lookup"><span data-stu-id="83f29-206">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="83f29-207"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="83f29-207"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="83f29-208">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="83f29-208">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83f29-209"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="83f29-209"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="83f29-210">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="83f29-210">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83f29-211"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="83f29-211"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="83f29-212">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="83f29-212">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="83f29-213">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83f29-213">See Also</span></span>

[<span data-ttu-id="83f29-214">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="83f29-214">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="83f29-215">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="83f29-215">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="83f29-216">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="83f29-216">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="83f29-217">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="83f29-217">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="83f29-218">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="83f29-218">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="83f29-219">JET_USERDEFINEDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="83f29-219">JET_USERDEFINEDDEFAULT</span></span>](./jet-userdefineddefault-structure.md)  
[<span data-ttu-id="83f29-220">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="83f29-220">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="83f29-221">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="83f29-221">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)  
[<span data-ttu-id="83f29-222">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="83f29-222">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)  
[<span data-ttu-id="83f29-223">JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="83f29-223">JetOpenTempTable</span></span>](./jetopentemptable-function.md)  
[<span data-ttu-id="83f29-224">JetOpenTempTable2</span><span class="sxs-lookup"><span data-stu-id="83f29-224">JetOpenTempTable2</span></span>](./jetopentemptable2-function.md)  
[<span data-ttu-id="83f29-225">JetOpenTempTable3</span><span class="sxs-lookup"><span data-stu-id="83f29-225">JetOpenTempTable3</span></span>](./jetopentemptable3-function.md)  
[<span data-ttu-id="83f29-226">JetRenameColumn</span><span class="sxs-lookup"><span data-stu-id="83f29-226">JetRenameColumn</span></span>](./jetrenamecolumn-function.md)
