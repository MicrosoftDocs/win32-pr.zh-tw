---
description: 深入瞭解： JET_COLUMNCREATE 結構
title: JET_COLUMNCREATE 結構
TOCTitle: JET_COLUMNCREATE Structure
ms:assetid: 553263a9-7d2c-4bd7-ad77-1dfb6d21ef2c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269252(v=EXCHG.10)
ms:contentKeyID: 32765554
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
ms.openlocfilehash: ee2d9d194a03cf575eb0296163526c1c50301cf4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988891"
---
# <a name="jet_columncreate-structure"></a><span data-ttu-id="04bef-103">JET_COLUMNCREATE 結構</span><span class="sxs-lookup"><span data-stu-id="04bef-103">JET_COLUMNCREATE Structure</span></span>


<span data-ttu-id="04bef-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="04bef-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columncreate-structure"></a><span data-ttu-id="04bef-105">JET_COLUMNCREATE 結構</span><span class="sxs-lookup"><span data-stu-id="04bef-105">JET_COLUMNCREATE Structure</span></span>

<span data-ttu-id="04bef-106">**JET_COLUMNCREATE** 結構描述要在資料庫中建立的資料行。</span><span class="sxs-lookup"><span data-stu-id="04bef-106">The **JET_COLUMNCREATE** structure describes a column to create in a database.</span></span>

```cpp
    typedef struct tag_JET_COLUMNCREATE {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_COLTYP coltyp;
      unsigned long cbMax;
      JET_GRBIT grbit;
      void* pvDefault;
      unsigned long cbDefault;
      unsigned long cp;
      JET_COLUMNID columnid;
      JET_ERR err;
    } JET_COLUMNCREATE;
```

### <a name="members"></a><span data-ttu-id="04bef-107">成員</span><span class="sxs-lookup"><span data-stu-id="04bef-107">Members</span></span>

<span data-ttu-id="04bef-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="04bef-108">**cbStruct**</span></span>

<span data-ttu-id="04bef-109">結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="04bef-109">The size of the structure, in bytes.</span></span> <span data-ttu-id="04bef-110">此欄位必須初始化為 **sizeof ( JET_COLUMNCREATE )**。</span><span class="sxs-lookup"><span data-stu-id="04bef-110">This field must be initialized to **sizeof( JET_COLUMNCREATE )**.</span></span>

<span data-ttu-id="04bef-111">**szColumnName**</span><span class="sxs-lookup"><span data-stu-id="04bef-111">**szColumnName**</span></span>

<span data-ttu-id="04bef-112">要建立之資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="04bef-112">The name of the column to create.</span></span> <span data-ttu-id="04bef-113">此名稱必須符合下列準則：</span><span class="sxs-lookup"><span data-stu-id="04bef-113">The name must meet the following criteria:</span></span>

  - <span data-ttu-id="04bef-114">長度必須少於 JET_cbNameMost 個字元，不包括終止的 Null。</span><span class="sxs-lookup"><span data-stu-id="04bef-114">It must be fewer than JET_cbNameMost characters in length, not including the terminating NULL.</span></span>

<!-- end list -->

  - <span data-ttu-id="04bef-115">它必須只包含下列集合中的字元：0到9、A 到 Z、a 到 z，以及除了驚嘆號以外的所有其他標點符號 (\!) 、逗點 (、) 、左括弧 (\[) 和右括弧 () \] ，也就是 ASCII 字元0x20、0x22 至0x2d、0x2f 至0x5a、0x5c、0x5d 至0x7f。</span><span class="sxs-lookup"><span data-stu-id="04bef-115">It must contain characters only from the following sets: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]), that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, 0x5d through 0x7f.</span></span>

<!-- end list -->

  - <span data-ttu-id="04bef-116">它不能以空格開頭。</span><span class="sxs-lookup"><span data-stu-id="04bef-116">It cannot begin with a space.</span></span>

<!-- end list -->

  - <span data-ttu-id="04bef-117">它至少必須包含一個非空白字元。</span><span class="sxs-lookup"><span data-stu-id="04bef-117">It must contain at least one non-space character.</span></span>

<span data-ttu-id="04bef-118">**coltyp**</span><span class="sxs-lookup"><span data-stu-id="04bef-118">**coltyp**</span></span>

<span data-ttu-id="04bef-119">資料行的類型 (例如，文字、二進位或數值) 。</span><span class="sxs-lookup"><span data-stu-id="04bef-119">The type of the column (for example, text, binary, or numerical).</span></span> <span data-ttu-id="04bef-120">如需詳細資訊，請參閱 [JET_COLTYP](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="04bef-120">For more information, see [JET_COLTYP](./jet-coltyp.md).</span></span>

<span data-ttu-id="04bef-121">**cbMax**</span><span class="sxs-lookup"><span data-stu-id="04bef-121">**cbMax**</span></span>

<span data-ttu-id="04bef-122">可變長度資料行的最大長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="04bef-122">The maximum length, in bytes, of a variable-length column.</span></span> <span data-ttu-id="04bef-123">固定長度資料行的資料行長度。</span><span class="sxs-lookup"><span data-stu-id="04bef-123">The length of the column for fixed-length columns.</span></span>

<span data-ttu-id="04bef-124">**grbit**</span><span class="sxs-lookup"><span data-stu-id="04bef-124">**grbit**</span></span>

<span data-ttu-id="04bef-125">位群組，其中包含此結構的選項，以及包含零或多個下列值的選項。</span><span class="sxs-lookup"><span data-stu-id="04bef-125">A group of bits that contain the options for this structure, and which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="04bef-126">值</span><span class="sxs-lookup"><span data-stu-id="04bef-126">Value</span></span></p></th>
<th><p><span data-ttu-id="04bef-127">意義</span><span class="sxs-lookup"><span data-stu-id="04bef-127">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="04bef-128">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="04bef-128">JET_bitColumnFixed</span></span></p></td>
<td><p><span data-ttu-id="04bef-129">此資料行是固定的。</span><span class="sxs-lookup"><span data-stu-id="04bef-129">The column is fixed.</span></span> <span data-ttu-id="04bef-130">無論資料儲存在資料行中的資料量為何，它一律會使用資料列中相同數量的空間。</span><span class="sxs-lookup"><span data-stu-id="04bef-130">It will always use the same amount of space in a row, regardless of how much data is being stored in the column.</span></span> <span data-ttu-id="04bef-131">JET_bitColumnFixed 不能與 JET_bitColumnTagged 一起使用。</span><span class="sxs-lookup"><span data-stu-id="04bef-131">JET_bitColumnFixed cannot be used with JET_bitColumnTagged.</span></span> <span data-ttu-id="04bef-132">這個位不能用在 long 值，例如 <strong>JET_coltypLongText</strong> 和 <strong>JET_coltypLongBinary</strong>。</span><span class="sxs-lookup"><span data-stu-id="04bef-132">This bit cannot be used with long values such as <strong>JET_coltypLongText</strong> and <strong>JET_coltypLongBinary</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04bef-133">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="04bef-133">JET_bitColumnTagged</span></span></p></td>
<td><p><span data-ttu-id="04bef-134">資料行已標記。</span><span class="sxs-lookup"><span data-stu-id="04bef-134">The column is tagged.</span></span> <span data-ttu-id="04bef-135">如果標記的資料行不包含資料，就不會佔用資料庫中的任何空間。</span><span class="sxs-lookup"><span data-stu-id="04bef-135">Tagged columns do not take up any space in the database if they do not contain data.</span></span> <span data-ttu-id="04bef-136">此位無法搭配 JET_bitColumnFixed 使用。</span><span class="sxs-lookup"><span data-stu-id="04bef-136">This bit cannot be used with JET_bitColumnFixed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04bef-137">JET_bitColumnNotNull</span><span class="sxs-lookup"><span data-stu-id="04bef-137">JET_bitColumnNotNULL</span></span></p></td>
<td><p><span data-ttu-id="04bef-138">資料行絕對不能設定為 Null 值。</span><span class="sxs-lookup"><span data-stu-id="04bef-138">The column must never be set to a NULL value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04bef-139">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="04bef-139">JET_bitColumnAutoincrement</span></span></p></td>
<td><p><span data-ttu-id="04bef-140">資料行會自動遞增。</span><span class="sxs-lookup"><span data-stu-id="04bef-140">The column is automatically incremented.</span></span> <span data-ttu-id="04bef-141">此數位是遞增的數位，而且在資料表中保證是唯一的。</span><span class="sxs-lookup"><span data-stu-id="04bef-141">The number is an increasing number, and is guaranteed to be unique within a table.</span></span> <span data-ttu-id="04bef-142">但數位可能不是連續的。</span><span class="sxs-lookup"><span data-stu-id="04bef-142">The number, however, might not be continuous.</span></span> <span data-ttu-id="04bef-143">例如，如果將五個數據列插入資料表中，自動遞增資料行可以包含值 {1，2，6，7，8}。</span><span class="sxs-lookup"><span data-stu-id="04bef-143">For example, if five rows are inserted into a table, the autoincrement column could contain the values { 1, 2, 6, 7, 8 }.</span></span></p>
<p><span data-ttu-id="04bef-144"><strong>Windows 2000：  </strong>這個位只能用在 <strong>JET_coltypLong</strong>類型的資料行上。</span><span class="sxs-lookup"><span data-stu-id="04bef-144"><strong>Windows 2000:  </strong>This bit can be used only on columns of type <strong>JET_coltypLong</strong>.</span></span></p>
<p><span data-ttu-id="04bef-145"><strong>Windows Server 2003 和更新版本：  </strong>這個位只能用在 <strong>JET_coltypLong</strong> 或 <strong>JET_coltypCurrency</strong>類型的資料行上。</span><span class="sxs-lookup"><span data-stu-id="04bef-145"><strong>Windows Server 2003 and later:  </strong>This bit can only be used on columns of type <strong>JET_coltypLong</strong> or <strong>JET_coltypCurrency</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04bef-146">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="04bef-146">JET_bitColumnUpdatable</span></span></p></td>
<td><p><span data-ttu-id="04bef-147">只有對 <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>的呼叫才會有此位有效。</span><span class="sxs-lookup"><span data-stu-id="04bef-147">This bit is valid only on calls to <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04bef-148">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="04bef-148">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="04bef-149">只有對 <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>的呼叫才會有此位有效。</span><span class="sxs-lookup"><span data-stu-id="04bef-149">This bit is valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04bef-150">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="04bef-150">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="04bef-151">只有對 <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>的呼叫才會有此位有效。</span><span class="sxs-lookup"><span data-stu-id="04bef-151">This bit is valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04bef-152">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="04bef-152">JET_bitColumnMultiValued</span></span></p></td>
<td><p><span data-ttu-id="04bef-153">此資料行可以是多重值。</span><span class="sxs-lookup"><span data-stu-id="04bef-153">The column can be multi-valued.</span></span> <span data-ttu-id="04bef-154">多重值資料行可以有零個、一個或多個相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="04bef-154">A multi-valued column can have zero, one, or more values associated with it.</span></span> <span data-ttu-id="04bef-155">多值資料行中的各種值是由各種結構的 <strong>itagSequence</strong> 成員識別，例如 <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>、 <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>、 <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>、 <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a> <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>。</span><span class="sxs-lookup"><span data-stu-id="04bef-155">The various values in a multi-valued column are identified by the <strong>itagSequence</strong> member of various structures, for example, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="04bef-156">多重值資料行必須是標記的資料行;也就是說，它們不能是固定長度或可變長度的資料行。</span><span class="sxs-lookup"><span data-stu-id="04bef-156">Multi-valued columns must be tagged columns; that is, they cannot be fixed-length or variable-length columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04bef-157">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="04bef-157">JET_bitColumnEscrowUpdate</span></span></p></td>
<td><p><span data-ttu-id="04bef-158">此資料行是「正在託管」更新資料行。</span><span class="sxs-lookup"><span data-stu-id="04bef-158">The column is an escrow update column.</span></span> <span data-ttu-id="04bef-159">交易更新資料行可以透過 <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> 的不同會話同時更新，並維持交易一致性。</span><span class="sxs-lookup"><span data-stu-id="04bef-159">An escrow update column can be updated concurrently by different sessions with <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> and maintain transactional consistency.</span></span></p>
<ul>
<li><p><span data-ttu-id="04bef-160">只有當資料表是空的時，才可以建立「正在進行」的更新資料行。</span><span class="sxs-lookup"><span data-stu-id="04bef-160">An escrow update column can be created only when the table is empty.</span></span></p></li>
<li><p><span data-ttu-id="04bef-161">「使用中」更新資料行的類型必須是 <strong>JET_coltypLong。</strong></span><span class="sxs-lookup"><span data-stu-id="04bef-161">An escrow update column must be of type <strong>JET_coltypLong.</strong></span></span></p></li>
<li><p><span data-ttu-id="04bef-162">「正在進行」的更新資料行必須有預設值 (<strong>cbDefault</strong> 必須是正數) 。</span><span class="sxs-lookup"><span data-stu-id="04bef-162">An escrow update column must have a default value (that is <strong>cbDefault</strong> must be positive).</span></span></p></li>
<li><p><span data-ttu-id="04bef-163">JET_bitColumnEscrowUpdate 不能與下列常數一起使用：</span><span class="sxs-lookup"><span data-stu-id="04bef-163">JET_bitColumnEscrowUpdate cannot be used in conjunction with the following constants:</span></span></p>
<ul>
<li><p><span data-ttu-id="04bef-164">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="04bef-164">JET_bitColumnTagged</span></span></p></li>
<li><p><span data-ttu-id="04bef-165">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="04bef-165">JET_bitColumnVersion</span></span></p></li>
<li><p><span data-ttu-id="04bef-166">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="04bef-166">JET_bitColumnAutoincrement</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04bef-167">JET_bitColumnUnversioned</span><span class="sxs-lookup"><span data-stu-id="04bef-167">JET_bitColumnUnversioned</span></span></p></td>
<td><p><span data-ttu-id="04bef-168">建立沒有版本的資料行。</span><span class="sxs-lookup"><span data-stu-id="04bef-168">The column is created without a version.</span></span> <span data-ttu-id="04bef-169">嘗試加入具有相同名稱之資料行的其他交易將會失敗。</span><span class="sxs-lookup"><span data-stu-id="04bef-169">Other transactions attempting to add a column with the same name will fail.</span></span> <span data-ttu-id="04bef-170">這個位只對 <a href="gg294122(v=exchg.10).md">JetAddColumn</a>很有用。</span><span class="sxs-lookup"><span data-stu-id="04bef-170">This bit is only useful with <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span></span> <span data-ttu-id="04bef-171">它不能用在交易內。</span><span class="sxs-lookup"><span data-stu-id="04bef-171">It cannot be used within a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04bef-172">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="04bef-172">JET_bitColumnMaybeNull</span></span></p></td>
<td><p><span data-ttu-id="04bef-173">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="04bef-173">Reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04bef-174">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="04bef-174">JET_bitColumnFinalize</span></span></p></td>
<td><p><span data-ttu-id="04bef-175">使用 JET_bitColumnDeleteOnZero 而不是 JET_bitColumnFinalize。</span><span class="sxs-lookup"><span data-stu-id="04bef-175">Use JET_bitColumnDeleteOnZero instead of JET_bitColumnFinalize.</span></span> <span data-ttu-id="04bef-176">JET_bitColumnFinalize 指定可以完成資料行。</span><span class="sxs-lookup"><span data-stu-id="04bef-176">JET_bitColumnFinalize specifies that a column can be finalized.</span></span> <span data-ttu-id="04bef-177">當可以完成的資料行具有到達零的「保管更新」資料行時，將會刪除該資料列。</span><span class="sxs-lookup"><span data-stu-id="04bef-177">When a column that can be finalized has an escrow update column that reaches zero, the row will be deleted.</span></span> <span data-ttu-id="04bef-178">未來的版本可以改為叫用回呼函數。</span><span class="sxs-lookup"><span data-stu-id="04bef-178">Future versions can invoke a callback function instead.</span></span> <span data-ttu-id="04bef-179">如需詳細資訊，請參閱 <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>。</span><span class="sxs-lookup"><span data-stu-id="04bef-179">For more information, see <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="04bef-180">可以完成的資料行必須是「託管更新」資料行。</span><span class="sxs-lookup"><span data-stu-id="04bef-180">A column that can be finalized must be an escrow update column.</span></span> <span data-ttu-id="04bef-181">JET_bitColumnFinalize 不能與 JET_bitColumnUserDefinedDefault 一起使用。</span><span class="sxs-lookup"><span data-stu-id="04bef-181">JET_bitColumnFinalize cannot be used with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04bef-182">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="04bef-182">JET_bitColumnUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="04bef-183">資料行的預設值是由回呼函數（ <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>）所提供。</span><span class="sxs-lookup"><span data-stu-id="04bef-183">The default value for a column is provided by the callback function, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="04bef-184">具有使用者定義預設值的資料行必須是標記的資料行。</span><span class="sxs-lookup"><span data-stu-id="04bef-184">A column that has a user-defined default must be a tagged column.</span></span> <span data-ttu-id="04bef-185"><strong>pvDefault</strong> 必須指向 <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> 結構，而且 <strong>cbDefault</strong> 必須設定為 sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>) 。</span><span class="sxs-lookup"><span data-stu-id="04bef-185"><strong>pvDefault</strong> must point to a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure, and <strong>cbDefault</strong> must be set to sizeof(<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</span></span></p>
<p><span data-ttu-id="04bef-186">JET_bitColumnUserDefinedDefault 不能與下列常數一起使用：</span><span class="sxs-lookup"><span data-stu-id="04bef-186">JET_bitColumnUserDefinedDefault cannot be used in conjunction with the following constants:</span></span></p>
<ul>
<li><p><span data-ttu-id="04bef-187">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="04bef-187">JET_bitColumnFixed</span></span></p></li>
<li><p><span data-ttu-id="04bef-188">JET_bitColumnNotNull</span><span class="sxs-lookup"><span data-stu-id="04bef-188">JET_bitColumnNotNULL</span></span></p></li>
<li><p><span data-ttu-id="04bef-189">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="04bef-189">JET_bitColumnVersion</span></span></p></li>
<li><p><span data-ttu-id="04bef-190">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="04bef-190">JET_bitColumnAutoincrement</span></span></p></li>
<li><p><span data-ttu-id="04bef-191">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="04bef-191">JET_bitColumnUpdatable</span></span></p></li>
<li><p><span data-ttu-id="04bef-192">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="04bef-192">JET_bitColumnEscrowUpdate</span></span></p></li>
<li><p><span data-ttu-id="04bef-193">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="04bef-193">JET_bitColumnFinalize</span></span></p></li>
<li><p><span data-ttu-id="04bef-194">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="04bef-194">JET_bitColumnDeleteOnZero</span></span></p></li>
<li><p><span data-ttu-id="04bef-195">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="04bef-195">JET_bitColumnMaybeNull</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04bef-196">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="04bef-196">JET_bitColumnDeleteOnZero</span></span></p></td>
<td><p><span data-ttu-id="04bef-197">此資料行是「正在進行的更新」資料行，當它到達零時，將會刪除記錄。</span><span class="sxs-lookup"><span data-stu-id="04bef-197">The column is an escrow update column, and when it reaches zero, the record will be deleted.</span></span> <span data-ttu-id="04bef-198">可以完成之資料行的常見用法是使用它做為參考計數位段，而且當欄位到達零時，就會刪除記錄。</span><span class="sxs-lookup"><span data-stu-id="04bef-198">A common use for a column that can be finalized is to use it as a reference count field, and when the field reaches zero the record gets deleted.</span></span> <span data-ttu-id="04bef-199">JET_bitColumnDeleteOnZero 與 JET_bitColumnFinalize 相關。</span><span class="sxs-lookup"><span data-stu-id="04bef-199">JET_bitColumnDeleteOnZero is related to JET_bitColumnFinalize.</span></span> <span data-ttu-id="04bef-200">零刪除資料行必須是「託管更新」資料行。</span><span class="sxs-lookup"><span data-stu-id="04bef-200">A delete-on-zero column must be an escrow update column.</span></span> <span data-ttu-id="04bef-201">JET_bitColumnDeleteOnZero 不能與 JET_bitColumnFinalize 一起使用。</span><span class="sxs-lookup"><span data-stu-id="04bef-201">JET_bitColumnDeleteOnZero cannot be used with JET_bitColumnFinalize.</span></span> <span data-ttu-id="04bef-202">JET_bitColumnDeleteOnZero 不能與使用者定義的預設資料行一起使用。</span><span class="sxs-lookup"><span data-stu-id="04bef-202">JET_bitColumnDeleteOnZero cannot be used with user defined default columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="04bef-203">**pvDefault**</span><span class="sxs-lookup"><span data-stu-id="04bef-203">**pvDefault**</span></span>

<span data-ttu-id="04bef-204">指向緩衝區，這會是資料行的預設值。</span><span class="sxs-lookup"><span data-stu-id="04bef-204">Points to a buffer which will be the default value for a column.</span></span> <span data-ttu-id="04bef-205">緩衝區的長度為 **cbDefault**。</span><span class="sxs-lookup"><span data-stu-id="04bef-205">The length of the buffer is **cbDefault**.</span></span> <span data-ttu-id="04bef-206">如果沒有預設值，則應該將 **pvDefault** 設定為 Null，而 **cbDefault** 應該設定為零。</span><span class="sxs-lookup"><span data-stu-id="04bef-206">If there is no default, **pvDefault** should be set to NULL and **cbDefault** should be set to zero.</span></span> <span data-ttu-id="04bef-207">如果 *grbit* 已設定 JET_bitColumnUserDefinedDefault， **pvDefault** 將會被解釋為 JET_USERDEFINEDDEFAULT 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="04bef-207">If *grbit* has JET_bitColumnUserDefinedDefault set, **pvDefault** will be interpreted as a pointer to a JET_USERDEFINEDDEFAULT structure.</span></span> <span data-ttu-id="04bef-208">預設值不能大於255個位元組。</span><span class="sxs-lookup"><span data-stu-id="04bef-208">Default values cannot be larger than 255 bytes.</span></span> <span data-ttu-id="04bef-209">如果預設值大於255個位元組，則會以無訊息模式截斷。</span><span class="sxs-lookup"><span data-stu-id="04bef-209">If a default value is larger than 255 bytes, it will be silently truncated.</span></span>

<span data-ttu-id="04bef-210">**cbDefault**</span><span class="sxs-lookup"><span data-stu-id="04bef-210">**cbDefault**</span></span>

<span data-ttu-id="04bef-211">**PvDefault** 所指定的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="04bef-211">The size, in bytes, of the buffer specified by **pvDefault**.</span></span>

<span data-ttu-id="04bef-212">**cp**</span><span class="sxs-lookup"><span data-stu-id="04bef-212">**cp**</span></span>

<span data-ttu-id="04bef-213">資料行的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="04bef-213">The code page for the column.</span></span> <span data-ttu-id="04bef-214">Text 資料行的唯一有效值是英文 (1252) 和 Unicode (1200) 。</span><span class="sxs-lookup"><span data-stu-id="04bef-214">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="04bef-215">值為零表示預設將會使用 (英文、1252) 。</span><span class="sxs-lookup"><span data-stu-id="04bef-215">A value of zero means the default will be used (English, 1252).</span></span> <span data-ttu-id="04bef-216">如果資料行不是文字資料行，則字碼頁會自動設為零。</span><span class="sxs-lookup"><span data-stu-id="04bef-216">If the column is not a text column, the code page automatically gets set to zero.</span></span>

<span data-ttu-id="04bef-217">**columnid**</span><span class="sxs-lookup"><span data-stu-id="04bef-217">**columnid**</span></span>

<span data-ttu-id="04bef-218">成功時，會在此欄位中傳回新建立之資料行的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="04bef-218">On success, the column identifier of the newly-created column will be passed back in this field.</span></span> <span data-ttu-id="04bef-219">失敗時，值為未定義。</span><span class="sxs-lookup"><span data-stu-id="04bef-219">On failure, the value is undefined.</span></span>

<span data-ttu-id="04bef-220">**犯 錯**</span><span class="sxs-lookup"><span data-stu-id="04bef-220">**err**</span></span>

<span data-ttu-id="04bef-221">**Err** 欄位將包含建立此資料行的狀態。</span><span class="sxs-lookup"><span data-stu-id="04bef-221">The **err** field will contain the status of creating this column.</span></span> <span data-ttu-id="04bef-222">如需可能傳回值的清單，請參閱 [JetAddColumn](./jetaddcolumn-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="04bef-222">See [JetAddColumn](./jetaddcolumn-function.md) for a list of likely return values.</span></span>

### <a name="requirements"></a><span data-ttu-id="04bef-223">規格需求</span><span class="sxs-lookup"><span data-stu-id="04bef-223">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="04bef-224"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="04bef-224"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="04bef-225">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="04bef-225">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04bef-226"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="04bef-226"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="04bef-227">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="04bef-227">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04bef-228"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="04bef-228"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="04bef-229">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="04bef-229">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04bef-230"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="04bef-230"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="04bef-231">實作為 <strong>JET_COLUMNCREATE_W</strong> (Unicode) 和 <strong>JET_COLUMNCREATE_A</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="04bef-231">Implemented as <strong>JET_COLUMNCREATE_W</strong> (Unicode) and <strong>JET_COLUMNCREATE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="04bef-232">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04bef-232">See Also</span></span>

[<span data-ttu-id="04bef-233">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="04bef-233">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="04bef-234">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="04bef-234">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="04bef-235">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="04bef-235">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="04bef-236">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="04bef-236">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="04bef-237">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="04bef-237">JET_RETINFO</span></span>](./jet-retinfo-structure.md)  
[<span data-ttu-id="04bef-238">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="04bef-238">JET_SETINFO</span></span>](./jet-setinfo-structure.md)  
[<span data-ttu-id="04bef-239">JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="04bef-239">JET_SETCOLUMN</span></span>](./jet-setcolumn-structure.md)  
[<span data-ttu-id="04bef-240">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="04bef-240">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)  
[<span data-ttu-id="04bef-241">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="04bef-241">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)  
[<span data-ttu-id="04bef-242">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="04bef-242">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="04bef-243">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="04bef-243">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="04bef-244">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="04bef-244">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="04bef-245">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="04bef-245">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)  
[<span data-ttu-id="04bef-246">JetRenameColumn</span><span class="sxs-lookup"><span data-stu-id="04bef-246">JetRenameColumn</span></span>](./jetrenamecolumn-function.md)  
[<span data-ttu-id="04bef-247">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="04bef-247">JetSetColumns</span></span>](./jetsetcolumns-function.md)
