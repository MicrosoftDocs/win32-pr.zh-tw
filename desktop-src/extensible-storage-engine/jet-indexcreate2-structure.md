---
description: 深入瞭解： JET_INDEXCREATE2 結構
title: JET_INDEXCREATE2 結構
TOCTitle: JET_INDEXCREATE2 Structure
ms:assetid: c574500e-8695-4f29-8e9d-6dff987af2a2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294082(v=EXCHG.10)
ms:contentKeyID: 32765697
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
ms.openlocfilehash: ac0d9a40e159a8aa5054228d18e431cee8d0319f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945463"
---
# <a name="jet_indexcreate2-structure"></a><span data-ttu-id="75ca1-103">JET_INDEXCREATE2 結構</span><span class="sxs-lookup"><span data-stu-id="75ca1-103">JET_INDEXCREATE2 Structure</span></span>


<span data-ttu-id="75ca1-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="75ca1-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="75ca1-105">**JET_INDEXCREATE2** 結構包含對可延伸儲存引擎中的資料建立索引所需的資訊， (ESE) 資料庫。</span><span class="sxs-lookup"><span data-stu-id="75ca1-105">The **JET_INDEXCREATE2** structure contains the information that is required to create an index over data in an Extensible Storage Engine (ESE) database.</span></span> <span data-ttu-id="75ca1-106">結構是由函式（例如 [JetCreateIndex2](./jetcreateindex2-function.md)）和結構（例如 [JET_TABLECREATE](./jet-tablecreate-structure.md) 和 [JET_TABLECREATE2](./jet-tablecreate2-structure.md)）所使用。</span><span class="sxs-lookup"><span data-stu-id="75ca1-106">The structure is used by functions such as [JetCreateIndex2](./jetcreateindex2-function.md), and in structures such as [JET_TABLECREATE](./jet-tablecreate-structure.md) and [JET_TABLECREATE2](./jet-tablecreate2-structure.md).</span></span>

<span data-ttu-id="75ca1-107">在 Windows 7 作業系統中引進了 **JET_INDEXCREATE2** 結構。</span><span class="sxs-lookup"><span data-stu-id="75ca1-107">The **JET_INDEXCREATE2** structure was introduced in the Windows 7 operating system.</span></span>

```cpp
typedef struct tagJET_INDEXCREATE2 {
  unsigned long cbStruct;
  tchar* szIndexName;
  tchar* szKey;
  unsigned long cbKey;
  JET_GRBIT grbit;
  unsigned long ulDensity;
  union {
    unsigned long lcid;
    JET_UNICODEINDEX* pidxunicode;
  };
  union {
    unsigned long cbVarSegMac;
    JET_TUPLELIMITS* ptuplelimits;
  };
  JET_CONDITIONALCOLUMN* rgconditionalcolumn;
  unsigned long cConditionalColumn;
  JET_ERR err;
    unsigned long cbKeyMost;
  JET_SPACEHINTS* pSpacehints;
} JET_INDEXCREATE;
```

### <a name="members"></a><span data-ttu-id="75ca1-108">成員</span><span class="sxs-lookup"><span data-stu-id="75ca1-108">Members</span></span>

<span data-ttu-id="75ca1-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="75ca1-109">**cbStruct**</span></span>

<span data-ttu-id="75ca1-110">此結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="75ca1-110">The size, in bytes, of this structure.</span></span> <span data-ttu-id="75ca1-111">將這個成員設定為 sizeof ( JET_INDEXCREATE2 ) 。</span><span class="sxs-lookup"><span data-stu-id="75ca1-111">Set this member to sizeof( JET_INDEXCREATE2 ).</span></span>

<span data-ttu-id="75ca1-112">**szIndexName**</span><span class="sxs-lookup"><span data-stu-id="75ca1-112">**szIndexName**</span></span>

<span data-ttu-id="75ca1-113">要建立之索引的名稱。</span><span class="sxs-lookup"><span data-stu-id="75ca1-113">The name of the index to create.</span></span>

<span data-ttu-id="75ca1-114">此名稱應符合下列條件：</span><span class="sxs-lookup"><span data-stu-id="75ca1-114">The name should meet the following conditions:</span></span>

  - <span data-ttu-id="75ca1-115">它應該小於 JET_cbNameMost，不包括終止的 null。</span><span class="sxs-lookup"><span data-stu-id="75ca1-115">It should be less than JET_cbNameMost, not including the terminating null.</span></span>

  - <span data-ttu-id="75ca1-116">它必須由下列一組字元組成： 0 (零) 到9、A 到 Z、a 到 z，以及 "" 以外的所有其他標點符號 \!</span><span class="sxs-lookup"><span data-stu-id="75ca1-116">It must consist of the following set of characters: 0 (zero) through 9, A through Z, a through z, and all other punctuation except for "\!"</span></span> <span data-ttu-id="75ca1-117"> (驚嘆號) 、"、" (逗號) 、" \[ " (左括弧) 和 " \] " (右括弧) ，也就是 ASCII 字元0x20、0x22 至0x2d、0x2f 至0x5a、0x5c 和0x5d 至0x7f。</span><span class="sxs-lookup"><span data-stu-id="75ca1-117">(exclamation point), "," (comma), "\[" (opening bracket), and "\]" (closing bracket) — that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="75ca1-118">不得以空格開頭。</span><span class="sxs-lookup"><span data-stu-id="75ca1-118">It must not begin with a space.</span></span>

  - <span data-ttu-id="75ca1-119">它至少必須包含一個非空白字元。</span><span class="sxs-lookup"><span data-stu-id="75ca1-119">It must contain at least one non-space character.</span></span>

<span data-ttu-id="75ca1-120">**szKey**</span><span class="sxs-lookup"><span data-stu-id="75ca1-120">**szKey**</span></span>

<span data-ttu-id="75ca1-121">以 null 分隔之標記的雙 null 結束字串指標。</span><span class="sxs-lookup"><span data-stu-id="75ca1-121">A pointer to a double-null-terminated string of null-delimited tokens.</span></span>

<span data-ttu-id="75ca1-122">每個權杖的格式為 " \<direction-specifier\> \<column-name\> "，其中的方向規格為 "+" 或 "-"。</span><span class="sxs-lookup"><span data-stu-id="75ca1-122">Each token is of the form "\<direction-specifier\>\<column-name\>", where direction-specification is either "+" or "-".</span></span> <span data-ttu-id="75ca1-123">例如，"+  abc \\ 0-def \\ 0 + Ghi 0" 的 szKey \\ 會以遞增順序來編制三個數據行 "abc" (的索引) 、"def" (以遞減順序) 和 "ghi" (遞增順序) 。</span><span class="sxs-lookup"><span data-stu-id="75ca1-123">For example, a **szKey** of "+abc\\0-def\\0+ghi\\0" will index over the three columns "abc" (in ascending order), "def" (in descending order), and "ghi" (in ascending order).</span></span> <span data-ttu-id="75ca1-124">在 C 語言中，字串常值具有隱含的 **Null** 結束字元，因此上述字串將以雙 Null 結束。</span><span class="sxs-lookup"><span data-stu-id="75ca1-124">In the C language, string literals have an implied **NULL** terminator, so the above string will be terminated by a double-NULL.</span></span>

<span data-ttu-id="75ca1-125">在 **szKey** 中指定的資料行數目不能超過與版本相依的常數)  (JET_ccolKeyMost。</span><span class="sxs-lookup"><span data-stu-id="75ca1-125">The number of columns specified in **szKey** must not exceed JET_ccolKeyMost (a version-dependent constant).</span></span>

<span data-ttu-id="75ca1-126">至少必須在 **szKey** 中命名一個資料行。</span><span class="sxs-lookup"><span data-stu-id="75ca1-126">At least one column must be named in **szKey**.</span></span>

<span data-ttu-id="75ca1-127">過時行為：在雙 Null 結束字元之後，您可以指定語言識別項， (傳遞到 MAKELCID ( langid 中的文字，SORT_DEFAULT ) ) 做為指定索引之 LCID 的方式。</span><span class="sxs-lookup"><span data-stu-id="75ca1-127">Obsolete behavior: After the double-NULL terminator, it is possible to specify a language ID (a WORD which gets passed into MAKELCID( langid, SORT_DEFAULT ) ) as a way to specify the LCID for the index.</span></span> <span data-ttu-id="75ca1-128">在 *grbit*) 中設定 JET_bitIndexUnicode，在 **szKey** 中指定語言識別項和 [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (中的 LCID 是不合法的。</span><span class="sxs-lookup"><span data-stu-id="75ca1-128">It is illegal to specify both a language ID in **szKey** and an LCID in [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (by setting JET_bitIndexUnicode in *grbit*).</span></span>

<span data-ttu-id="75ca1-129">已淘汰：在語言識別項之後，可以將 **cbVarSegMac** 傳遞為 **USHORT** 資料類型。</span><span class="sxs-lookup"><span data-stu-id="75ca1-129">Deprecated: After the language ID, it is possible to pass **cbVarSegMac** as a **USHORT** data type.</span></span> <span data-ttu-id="75ca1-130">如果在 **szKey** 中同時設定 USHORT，以及在結構中設定 **cbVarSegMac** ，則行為會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="75ca1-130">The behavior is undefined if the USHORT is set both in **szKey** and if **cbVarSegMac** is set in the structure.</span></span>

<span data-ttu-id="75ca1-131">**cbKey**</span><span class="sxs-lookup"><span data-stu-id="75ca1-131">**cbKey**</span></span>

<span data-ttu-id="75ca1-132">**SzKey** 的長度（以位元組為單位），包括兩個終止的 null。</span><span class="sxs-lookup"><span data-stu-id="75ca1-132">The length, in bytes, of **szKey**, including the two terminating nulls.</span></span>

<span data-ttu-id="75ca1-133">**grbit**</span><span class="sxs-lookup"><span data-stu-id="75ca1-133">**grbit**</span></span>

<span data-ttu-id="75ca1-134">包含零或多個值選項的位群組，這些選項列于下表中。</span><span class="sxs-lookup"><span data-stu-id="75ca1-134">A group of bits that contain zero or more of the value options that are listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="75ca1-135">值</span><span class="sxs-lookup"><span data-stu-id="75ca1-135">Value</span></span></p></th>
<th><p><span data-ttu-id="75ca1-136">意義</span><span class="sxs-lookup"><span data-stu-id="75ca1-136">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75ca1-137">JET_bitIndexUnique</span><span class="sxs-lookup"><span data-stu-id="75ca1-137">JET_bitIndexUnique</span></span></p></td>
<td><p><span data-ttu-id="75ca1-138">不允許有重複的索引項目 (索引鍵) 。</span><span class="sxs-lookup"><span data-stu-id="75ca1-138">Duplicate index entries (keys) are disallowed.</span></span> <span data-ttu-id="75ca1-139">呼叫 <a href="gg269288(v=exchg.10).md">JetUpdate</a> 時，不會強制執行這項功能，而不是在呼叫 <a href="gg294137(v=exchg.10).md">JetSetColumn</a> 時強制執行。</span><span class="sxs-lookup"><span data-stu-id="75ca1-139">This is enforced when <a href="gg269288(v=exchg.10).md">JetUpdate</a> is called, not when <a href="gg294137(v=exchg.10).md">JetSetColumn</a> is called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75ca1-140">JET_bitIndexPrimary</span><span class="sxs-lookup"><span data-stu-id="75ca1-140">JET_bitIndexPrimary</span></span></p></td>
<td><p><span data-ttu-id="75ca1-141">索引是主要 (叢集) 索引。</span><span class="sxs-lookup"><span data-stu-id="75ca1-141">The index is a primary (clustered) index.</span></span> <span data-ttu-id="75ca1-142">每個資料表都必須只有一個主要索引。</span><span class="sxs-lookup"><span data-stu-id="75ca1-142">Every table must have exactly one primary index.</span></span> <span data-ttu-id="75ca1-143">如果未在資料表上明確定義主要索引，database engine 將會建立自己的主要索引。</span><span class="sxs-lookup"><span data-stu-id="75ca1-143">If no primary index is explicitly defined over a table, the database engine will create its own primary index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75ca1-144">JET_bitIndexDisallowNull</span><span class="sxs-lookup"><span data-stu-id="75ca1-144">JET_bitIndexDisallowNull</span></span></p></td>
<td><p><span data-ttu-id="75ca1-145">建立索引的資料行都不能包含 <strong>Null</strong> 值。</span><span class="sxs-lookup"><span data-stu-id="75ca1-145">None of the columns over which the index is created may contain a <strong>NULL</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75ca1-146">JET_bitIndexIgnoreNull</span><span class="sxs-lookup"><span data-stu-id="75ca1-146">JET_bitIndexIgnoreNull</span></span></p></td>
<td><p><span data-ttu-id="75ca1-147">如果要編制索引的所有資料行都是 <strong>Null</strong>，請勿加入資料列的索引項目。</span><span class="sxs-lookup"><span data-stu-id="75ca1-147">Do not add an index entry for a row if all of the columns being indexed are <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75ca1-148">JET_bitIndexIgnoreAnyNull</span><span class="sxs-lookup"><span data-stu-id="75ca1-148">JET_bitIndexIgnoreAnyNull</span></span></p></td>
<td><p><span data-ttu-id="75ca1-149">如果要編制索引的任何資料行都是 <strong>Null</strong>，請勿加入資料列的索引項目。</span><span class="sxs-lookup"><span data-stu-id="75ca1-149">Do not add an index entry for a row if any of the columns being indexed are <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75ca1-150">JET_bitIndexIgnoreFirstNull</span><span class="sxs-lookup"><span data-stu-id="75ca1-150">JET_bitIndexIgnoreFirstNull</span></span></p></td>
<td><p><span data-ttu-id="75ca1-151">如果要編制索引的第一個資料行是 <strong>Null</strong>，請勿加入資料列的索引項目。</span><span class="sxs-lookup"><span data-stu-id="75ca1-151">Do not add an index entry for a row if the first column being indexed is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75ca1-152">JET_bitIndexLazyFlush</span><span class="sxs-lookup"><span data-stu-id="75ca1-152">JET_bitIndexLazyFlush</span></span></p></td>
<td><p><span data-ttu-id="75ca1-153">指定將延遲記錄索引作業。</span><span class="sxs-lookup"><span data-stu-id="75ca1-153">Specifies that the index operations will be logged lazily.</span></span></p>
<p><span data-ttu-id="75ca1-154">JET_bitIndexLazyFlush 不會影響資料更新的酷。</span><span class="sxs-lookup"><span data-stu-id="75ca1-154">JET_bitIndexLazyFlush does not affect the laziness of data updates.</span></span> <span data-ttu-id="75ca1-155">如果處理常式終止時，索引作業中斷，軟復原仍能讓資料庫處於一致的狀態，但索引可能不存在。</span><span class="sxs-lookup"><span data-stu-id="75ca1-155">If the indexing operation is interrupted by process termination, Soft Recovery will still be able to able to get the database to a consistent state, but the index may not be present.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75ca1-156">JET_bitIndexEmpty</span><span class="sxs-lookup"><span data-stu-id="75ca1-156">JET_bitIndexEmpty</span></span></p></td>
<td><p><span data-ttu-id="75ca1-157">請勿嘗試建立索引，因為所有專案都會評估為 <strong>Null</strong>。</span><span class="sxs-lookup"><span data-stu-id="75ca1-157">Do not try to build the index, because all entries would evaluate to <strong>NULL</strong>.</span></span> <span data-ttu-id="75ca1-158"><strong>grbit</strong> 傳遞 JET_bitIndexEmpty 時，也必須指定 JET_bitIgnoreAnyNull。</span><span class="sxs-lookup"><span data-stu-id="75ca1-158"><strong>grbit</strong> MUST also specify JET_bitIgnoreAnyNull when JET_bitIndexEmpty is passed.</span></span> <span data-ttu-id="75ca1-159">這是一項效能增強功能。</span><span class="sxs-lookup"><span data-stu-id="75ca1-159">This is a performance enhancement.</span></span> <span data-ttu-id="75ca1-160">例如，如果新的資料行加入至資料表，然後在這個新加入的資料行上建立索引，則會掃描資料表中的所有記錄，即使這些記錄未加入至索引也一樣。</span><span class="sxs-lookup"><span data-stu-id="75ca1-160">For example, if a new column is added to a table, and then an index is created over this newly added column, all the records in the table are scanned even though they are not added to the index.</span></span> <span data-ttu-id="75ca1-161">指定 JET_bitIndexEmpty 會略過資料表掃描，這可能會花費很長的時間。</span><span class="sxs-lookup"><span data-stu-id="75ca1-161">Specifying JET_bitIndexEmpty skips the scanning of the table, which could potentially take a long time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75ca1-162">JET_bitIndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="75ca1-162">JET_bitIndexUnversioned</span></span></p></td>
<td><p><span data-ttu-id="75ca1-163">JET_bitIndexUnversioned 會導致其他交易看到索引建立。</span><span class="sxs-lookup"><span data-stu-id="75ca1-163">JET_bitIndexUnversioned causes index creation to be visible to other transactions.</span></span> <span data-ttu-id="75ca1-164">一般來說，交易中的會話將無法在另一個會話中看到索引建立作業。</span><span class="sxs-lookup"><span data-stu-id="75ca1-164">Ordinarily, a session in a transaction will not be able to see an index creation operation in another session.</span></span> <span data-ttu-id="75ca1-165">如果另一個交易可能建立相同的索引，則此旗標很有用。</span><span class="sxs-lookup"><span data-stu-id="75ca1-165">This flag can be useful if another transaction is likely to create the same index.</span></span> <span data-ttu-id="75ca1-166">第二個索引建立將會失敗，而不是可能導致許多不必要的資料庫作業。</span><span class="sxs-lookup"><span data-stu-id="75ca1-166">The second index-create will simply fail instead of potentially causing many unnecessary database operations.</span></span> <span data-ttu-id="75ca1-167">第二筆交易可能無法立即使用索引。</span><span class="sxs-lookup"><span data-stu-id="75ca1-167">The second transaction may not be able to use the index immediately.</span></span> <span data-ttu-id="75ca1-168">索引建立作業必須先完成，才可供使用。</span><span class="sxs-lookup"><span data-stu-id="75ca1-168">The index creation operation has to complete before it is usable.</span></span> <span data-ttu-id="75ca1-169">會話目前不能在交易中建立索引，而不需要版本資訊。</span><span class="sxs-lookup"><span data-stu-id="75ca1-169">The session must not currently be in a transaction to create an index without version information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75ca1-170">JET_bitIndexSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="75ca1-170">JET_bitIndexSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="75ca1-171">指定此旗標會在索引中的所有資料行資料之後，將 <strong>Null</strong> 值排序。</span><span class="sxs-lookup"><span data-stu-id="75ca1-171">Specifying this flag causes <strong>NULL</strong> values to be sorted after data for all columns in the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75ca1-172">JET_bitIndexUnicode</span><span class="sxs-lookup"><span data-stu-id="75ca1-172">JET_bitIndexUnicode</span></span></p></td>
<td><p><span data-ttu-id="75ca1-173">指定此旗標會影響結構中 lcid/pidxunicde 聯集欄位的解釋。</span><span class="sxs-lookup"><span data-stu-id="75ca1-173">Specifying this flag affects the interpretation of the lcid/pidxunicde union field in the structure.</span></span> <span data-ttu-id="75ca1-174">設定位表示 pidxunicode 欄位實際上會指向 <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> 結構。</span><span class="sxs-lookup"><span data-stu-id="75ca1-174">Setting the bit means that the pidxunicode field actually points to a <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure.</span></span> <span data-ttu-id="75ca1-175">不需要 JET_bitIndexUnicode 來編制 Unicode 資料的索引。</span><span class="sxs-lookup"><span data-stu-id="75ca1-175">JET_bitIndexUnicode is not required to index Unicode data.</span></span> <span data-ttu-id="75ca1-176">只需要自訂 Unicode 資料的正規化。</span><span class="sxs-lookup"><span data-stu-id="75ca1-176">It is only needed to customize the normalization of Unicode data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75ca1-177">JET_bitIndexTuples</span><span class="sxs-lookup"><span data-stu-id="75ca1-177">JET_bitIndexTuples</span></span></p></td>
<td><p><span data-ttu-id="75ca1-178">指定索引為元組索引。</span><span class="sxs-lookup"><span data-stu-id="75ca1-178">Specifies that the index is a tuple index.</span></span> <span data-ttu-id="75ca1-179">如需元組索引的描述，請參閱 <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> 。</span><span class="sxs-lookup"><span data-stu-id="75ca1-179">See <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> for a description of a tuple index.</span></span></p>
<p><span data-ttu-id="75ca1-180">JET_bitIndexTuples 的值是在 Windows XP 作業系統中引進的。</span><span class="sxs-lookup"><span data-stu-id="75ca1-180">The JET_bitIndexTuples value was introduced in the Windows XP operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75ca1-181">JET_bitIndexTupleLimits</span><span class="sxs-lookup"><span data-stu-id="75ca1-181">JET_bitIndexTupleLimits</span></span></p></td>
<td><p><span data-ttu-id="75ca1-182">指定此旗標會影響結構中 <strong>cbVarSegMac/ptuplelimits</strong> 聯集欄位的解釋。</span><span class="sxs-lookup"><span data-stu-id="75ca1-182">Specifying this flag affects the interpretation of the <strong>cbVarSegMac/ptuplelimits</strong> union field in the structure.</span></span> <span data-ttu-id="75ca1-183">設定此位表示 <strong>ptuplelimits</strong> 欄位實際上會指向 <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> 結構，以允許自訂元組索引限制 (暗示 JET_bitIndexTuples) 。</span><span class="sxs-lookup"><span data-stu-id="75ca1-183">Setting this bit means that the <strong>ptuplelimits</strong> field actually points to a <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure to allow custom tuple index limits (implies JET_bitIndexTuples).</span></span></p>
<p><span data-ttu-id="75ca1-184"><strong>JET_bitIndexTupleLimits</strong>值是在 Windows Server 2003 作業系統中引進。</span><span class="sxs-lookup"><span data-stu-id="75ca1-184">The <strong>JET_bitIndexTupleLimits</strong> value was introduced in the Windows Server 2003 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75ca1-185">JET_bitIndexCrossProduct</span><span class="sxs-lookup"><span data-stu-id="75ca1-185">JET_bitIndexCrossProduct</span></span><br />
<span data-ttu-id="75ca1-186">0x00004000</span><span class="sxs-lookup"><span data-stu-id="75ca1-186">0x00004000</span></span></p></td>
<td><p><span data-ttu-id="75ca1-187">針對具有多值資料行之多個索引鍵資料行的索引指定此旗標，會導致針對這些索引鍵資料行中的所有值交叉乘積的每個結果建立索引項目。</span><span class="sxs-lookup"><span data-stu-id="75ca1-187">Specifying this flag for an index that has more than one key column that is a multivalued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="75ca1-188">否則，索引在最重要的索引鍵資料行中，每個多重值都只會有一個專案，這是多值資料行，而每個索引項目會使用任何其他索引鍵資料行中的第一個多重值資料行值。</span><span class="sxs-lookup"><span data-stu-id="75ca1-188">Otherwise, the index would only have one entry for each multivalue in the most significant key column that is a multivalued column and each of those index entries would use the first multivalue from any other key columns that are multi valued columns.</span></span></p>
<p><span data-ttu-id="75ca1-189">例如，如果您在資料行 A 上為索引指定了這個旗標，其值為 &quot; 紅色 &quot; 和 &quot; 藍色， &quot; 而資料行 B 的值為 &quot; 1 &quot; 和 &quot; 2 &quot; ，則會建立下列索引項目： &quot; 紅色 &quot; 、 &quot; 1 &quot; ; &quot;紅色 &quot; 、 &quot; 2 &quot; ; &quot;藍色 &quot; 、 &quot; 1 &quot; ; &quot;藍色 &quot; 、 &quot; 2 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="75ca1-189">For example, if you specified this flag for an index over column A that has the values &quot;red&quot; and &quot;blue&quot; and over column B that has the values &quot;1&quot; and &quot;2&quot;, the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;red&quot;, &quot;2&quot;; &quot;blue&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;2&quot;.</span></span> <span data-ttu-id="75ca1-190">否則，將會建立下列索引項目： &quot; 紅色 &quot; 、 &quot; 1 &quot; ; &quot;藍色 &quot; 、 &quot; 1 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="75ca1-190">Otherwise, the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;1&quot;.</span></span></p>
<p><span data-ttu-id="75ca1-191">在 Windows Vista 中引進了 <strong>JET_bitIndexCrossProduct</strong> 的值。</span><span class="sxs-lookup"><span data-stu-id="75ca1-191">The <strong>JET_bitIndexCrossProduct</strong> value was introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75ca1-192">JET_bitIndexKeyMost</span><span class="sxs-lookup"><span data-stu-id="75ca1-192">JET_bitIndexKeyMost</span></span><br />
<span data-ttu-id="75ca1-193">0x00008000</span><span class="sxs-lookup"><span data-stu-id="75ca1-193">0x00008000</span></span></p></td>
<td><p><span data-ttu-id="75ca1-194">指定此旗標將會導致索引使用結構中 <strong>cbKeyMost</strong> 欄位指定的最大索引鍵大小。</span><span class="sxs-lookup"><span data-stu-id="75ca1-194">Specifying this flag will cause the index to use the maximum key size specified in the <strong>cbKeyMost</strong> field in the structure.</span></span> <span data-ttu-id="75ca1-195">否則，索引會使用 JET_cbKeyMost (255) 做為其最大索引鍵大小。</span><span class="sxs-lookup"><span data-stu-id="75ca1-195">Otherwise, the index will use JET_cbKeyMost (255) as its maximum key size.</span></span></p>
<p><span data-ttu-id="75ca1-196">在 Windows Vista 中引進了 <strong>JET_bitIndexKeyMost</strong> 的值。</span><span class="sxs-lookup"><span data-stu-id="75ca1-196">The <strong>JET_bitIndexKeyMost</strong> value was introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75ca1-197">JET_bitIndexDisallowTruncation</span><span class="sxs-lookup"><span data-stu-id="75ca1-197">JET_bitIndexDisallowTruncation</span></span><br />
<span data-ttu-id="75ca1-198">0x00010000</span><span class="sxs-lookup"><span data-stu-id="75ca1-198">0x00010000</span></span></p></td>
<td><p><span data-ttu-id="75ca1-199">指定此旗標會導致索引的任何更新會導致截斷的金鑰失敗，並產生 JET_errKeyTruncated 的回應碼。</span><span class="sxs-lookup"><span data-stu-id="75ca1-199">Specifying this flag will cause any update to the index that would result in a truncated key to fail with the JET_errKeyTruncated response code.</span></span> <span data-ttu-id="75ca1-200">否則，將會以無訊息方式截斷金鑰。</span><span class="sxs-lookup"><span data-stu-id="75ca1-200">Otherwise, keys will be silently truncated.</span></span> <span data-ttu-id="75ca1-201">如需有關金鑰截斷的詳細資訊，請參閱 <a href="gg269329(v=exchg.10).md">JetMakeKey</a>。</span><span class="sxs-lookup"><span data-stu-id="75ca1-201">For more information about key truncation, see <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</span></span></p>
<p><span data-ttu-id="75ca1-202">在 Windows Vista 中引進了 <strong>JET_bitIndexDisallowTruncation</strong> 的值。</span><span class="sxs-lookup"><span data-stu-id="75ca1-202">The <strong>JET_bitIndexDisallowTruncation</strong> value was introduced in Windows Vista.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="75ca1-203">**ulDensity**</span><span class="sxs-lookup"><span data-stu-id="75ca1-203">**ulDensity**</span></span>

<span data-ttu-id="75ca1-204">初始索引 B + 樹狀結構的百分比密度。</span><span class="sxs-lookup"><span data-stu-id="75ca1-204">The percentage density of the initial index B+ tree.</span></span> <span data-ttu-id="75ca1-205">指定小於100的數位，一開始就會使用較多的空間來建立索引，但允許未來的索引成長，進而避免發生內部片段。</span><span class="sxs-lookup"><span data-stu-id="75ca1-205">Specifying a number less than 100 uses up more space to create the index initially, but allows future growth of the index to be in place, thus avoiding internal fragmentation.</span></span>

<span data-ttu-id="75ca1-206">**lcid**</span><span class="sxs-lookup"><span data-stu-id="75ca1-206">**lcid**</span></span>

<span data-ttu-id="75ca1-207">地區設定識別碼 (LCID) 在 *grbit* 參數中未指定 JET_bitIndexUnicode 值時正規化資料時所要使用的值。</span><span class="sxs-lookup"><span data-stu-id="75ca1-207">The locale identifier (LCID) to use when normalizing the data when the JET_bitIndexUnicode value is not specified in the *grbit* parameter.</span></span> <span data-ttu-id="75ca1-208">如果索引是透過 Unicode 資料行，則 LCID 會影響正規化。</span><span class="sxs-lookup"><span data-stu-id="75ca1-208">The LCID affects the normalization if the index is over Unicode columns.</span></span>

<span data-ttu-id="75ca1-209">**pidxunicode**</span><span class="sxs-lookup"><span data-stu-id="75ca1-209">**pidxunicode**</span></span>

<span data-ttu-id="75ca1-210">如果在 *grbit* 參數中指定了 JET_bitIndexUnicode 值，則為 [JET_UNICODEINDEX](./jet-unicodeindex-structure.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="75ca1-210">A pointer to a [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) structure if the JET_bitIndexUnicode value is specified in the *grbit* parameter.</span></span> <span data-ttu-id="75ca1-211">這可讓使用者指定在 Unicode 正規化期間傳遞至 [LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) 函數的自訂旗標。</span><span class="sxs-lookup"><span data-stu-id="75ca1-211">This allows the user to specify custom flags that get passed to the [LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) function during Unicode normalization.</span></span>

<span data-ttu-id="75ca1-212">**cbVarSegMac**</span><span class="sxs-lookup"><span data-stu-id="75ca1-212">**cbVarSegMac**</span></span>

<span data-ttu-id="75ca1-213">*Grbit* 參數中未指定 JET_bitIndexTupleLimits 值時，每個資料行要儲存在索引中的最大長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="75ca1-213">The maximum length, in bytes, of each column to store in the index when the JET_bitIndexTupleLimits value is not specified in the *grbit* parameter.</span></span>

<span data-ttu-id="75ca1-214">將此欄位的值指定為 0 (零) 相當於下列專案：</span><span class="sxs-lookup"><span data-stu-id="75ca1-214">Specifying a value of 0 (zero) for this field is equivalent to the following:</span></span>

  - <span data-ttu-id="75ca1-215">指定主要索引的 JET_cbPrimaryKeyMost。</span><span class="sxs-lookup"><span data-stu-id="75ca1-215">Specifying JET_cbPrimaryKeyMost for a primary index.</span></span>

  - <span data-ttu-id="75ca1-216">指定次要索引的 JET_cbSecondaryKeyMost。</span><span class="sxs-lookup"><span data-stu-id="75ca1-216">Specifying JET_cbSecondaryKeyMost for a secondary index.</span></span>

<span data-ttu-id="75ca1-217">**ptuplelimits**</span><span class="sxs-lookup"><span data-stu-id="75ca1-217">**ptuplelimits**</span></span>

<span data-ttu-id="75ca1-218">如果在 *grbit* 參數中指定了 JET_bitIndexTupleLimits 值，則為 [JET_TUPLELIMITS](./jet-tuplelimits-structure.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="75ca1-218">A pointer to a [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure if the JET_bitIndexTupleLimits value is specified in the *grbit* parameter.</span></span>

<span data-ttu-id="75ca1-219">**ptuplelimits** 是在 Windows Server 2003 中引進。</span><span class="sxs-lookup"><span data-stu-id="75ca1-219">**ptuplelimits** was introduced in Windows Server 2003.</span></span>

<span data-ttu-id="75ca1-220">**rgconditionalcolumn**</span><span class="sxs-lookup"><span data-stu-id="75ca1-220">**rgconditionalcolumn**</span></span>

<span data-ttu-id="75ca1-221">[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)結構陣列的選擇性參數，用來指定索引中的條件資料行。</span><span class="sxs-lookup"><span data-stu-id="75ca1-221">An optional parameter to an array of [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) structures, which are used to specify the conditional columns in the index.</span></span>

<span data-ttu-id="75ca1-222">**cConditionalColumn**</span><span class="sxs-lookup"><span data-stu-id="75ca1-222">**cConditionalColumn**</span></span>

<span data-ttu-id="75ca1-223">**Rgconditionalcolumn** 陣列中的結構計數。</span><span class="sxs-lookup"><span data-stu-id="75ca1-223">The count of structures in the **rgconditionalcolumn** array.</span></span>

<span data-ttu-id="75ca1-224">**犯 錯**</span><span class="sxs-lookup"><span data-stu-id="75ca1-224">**err**</span></span>

<span data-ttu-id="75ca1-225">包含用來建立此索引的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="75ca1-225">Contains the return code for creating this index.</span></span>

<span data-ttu-id="75ca1-226">**cbKeyMost**</span><span class="sxs-lookup"><span data-stu-id="75ca1-226">**cbKeyMost**</span></span>

<span data-ttu-id="75ca1-227">針對索引中的索引鍵，指定允許的最大大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="75ca1-227">Specifies the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="75ca1-228">如果未在 *grbit* 參數中指定 JET_bitIndexKeyMost，則會忽略此參數。</span><span class="sxs-lookup"><span data-stu-id="75ca1-228">This parameter is ignored if JET_bitIndexKeyMost is not specified in *grbit* parameter.</span></span> <span data-ttu-id="75ca1-229">如果這個參數設定為零，且 *grbit* 成員中指定了 JET_bitIndexKeyMost，呼叫的函式將會失敗併發生 JET_err_InvalidDef。</span><span class="sxs-lookup"><span data-stu-id="75ca1-229">If this parameter is set to zero, and JET_bitIndexKeyMost is specified in the *grbit* member, the calling function will fail with JET_err_InvalidDef.</span></span>

<span data-ttu-id="75ca1-230">最小支援的金鑰大小為 JET_cbKeyMostMin (255) ，也就是舊版的最大索引鍵大小。</span><span class="sxs-lookup"><span data-stu-id="75ca1-230">The minimum supported maximum key size is JET_cbKeyMostMin (255), which is the legacy maximum key size.</span></span>

<span data-ttu-id="75ca1-231">金鑰大小上限取決於資料庫頁面大小 (JET_paramDatabasePageSize) 如下所示：</span><span class="sxs-lookup"><span data-stu-id="75ca1-231">The maximum key size is dependent on the database page size (JET_paramDatabasePageSize) as follows:</span></span>

  - <span data-ttu-id="75ca1-232">如果 JET_paramDatabasePageSize = 2048，則 JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost2KBytePage (500) </span><span class="sxs-lookup"><span data-stu-id="75ca1-232">If JET_paramDatabasePageSize = 2048 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost2KBytePage (500)</span></span>

  - <span data-ttu-id="75ca1-233">如果 JET_paramDatabasePageSize = 4096，則 JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost4KBytePage (1000) </span><span class="sxs-lookup"><span data-stu-id="75ca1-233">If JET_paramDatabasePageSize = 4096 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost4KBytePage (1000)</span></span>

  - <span data-ttu-id="75ca1-234">如果 JET_paramDatabasePageSize = 8192，則 JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost8KBytePage (2000) </span><span class="sxs-lookup"><span data-stu-id="75ca1-234">If JET_paramDatabasePageSize = 8192 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost8KBytePage (2000)</span></span>

<span data-ttu-id="75ca1-235">您也可以從 JET_paramKeyMost 系統參數讀取實例的最大支援索引鍵大小上限。</span><span class="sxs-lookup"><span data-stu-id="75ca1-235">The maximum supported maximum key size for the instance can also be read from the JET_paramKeyMost system parameter.</span></span>

<span data-ttu-id="75ca1-236">**cbKeyMost** 是在 Windows Vista 中引進的。</span><span class="sxs-lookup"><span data-stu-id="75ca1-236">**cbKeyMost** was introduced in Windows Vista.</span></span>

<span data-ttu-id="75ca1-237">**pSpacehints**</span><span class="sxs-lookup"><span data-stu-id="75ca1-237">**pSpacehints**</span></span>

<span data-ttu-id="75ca1-238">[JET_SPACEHINTS](./jet-spacehints-structure.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="75ca1-238">A pointer to a [JET_SPACEHINTS](./jet-spacehints-structure.md) structure.</span></span>

<span data-ttu-id="75ca1-239">**pSpacehints** 是在 Windows 7 中引進的。</span><span class="sxs-lookup"><span data-stu-id="75ca1-239">**pSpacehints** was introduced in Windows 7.</span></span>

### <a name="remarks"></a><span data-ttu-id="75ca1-240">備註</span><span class="sxs-lookup"><span data-stu-id="75ca1-240">Remarks</span></span>

<span data-ttu-id="75ca1-241">ESE 支援在包含多個值的索引鍵資料行上編制索引。</span><span class="sxs-lookup"><span data-stu-id="75ca1-241">ESE supports indexing over key columns containing multiple values.</span></span> <span data-ttu-id="75ca1-242">若要使用這項功能，資料行必須是標記的資料行類型 (JET_bitColumnTagged) ，且必須加上旗標，以 JET_bitColumnMultiValued 為其建立多個值。</span><span class="sxs-lookup"><span data-stu-id="75ca1-242">To use this feature, the column must be a tagged column type (JET_bitColumnTagged), and it must be flagged to have its multiple values indexed with JET_bitColumnMultiValued.</span></span> <span data-ttu-id="75ca1-243">在 Windows Vista 之前的 Windows 版本中，只有索引中的第一個多重值索引鍵資料行會在索引中展開其值。</span><span class="sxs-lookup"><span data-stu-id="75ca1-243">In versions of Windows earlier than Windows Vista, only the first multivalued key column in the index will have its values expanded in the index.</span></span> <span data-ttu-id="75ca1-244">所有其他多值和標記的資料行只會在索引中展開其第一個值。</span><span class="sxs-lookup"><span data-stu-id="75ca1-244">All other multivalued and tagged columns will only have their first values expanded in the index.</span></span>

<span data-ttu-id="75ca1-245">假設資料表中有下列資料列 (資料行 Alpha 不是多重值，而資料行 Beta、Gamma 和 Delta 是多重值) ，而且索引建立為 "+ Alpha \\ 0 + Beta \\ 0 + Gamma \\ 0 + Delta \\ 0 \\ 0"：</span><span class="sxs-lookup"><span data-stu-id="75ca1-245">Assuming the following rows exist in a table (column Alpha is not multivalued, while columns Beta, Gamma, and Delta are multivalued), and an index is created as "+Alpha\\0+Beta\\0+Gamma\\0+Delta\\0\\0":</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="75ca1-246">Alpha</span><span class="sxs-lookup"><span data-stu-id="75ca1-246">Alpha</span></span></p></th>
<th><p><span data-ttu-id="75ca1-247">Beta</span><span class="sxs-lookup"><span data-stu-id="75ca1-247">Beta</span></span></p></th>
<th><p><span data-ttu-id="75ca1-248">色差補正</span><span class="sxs-lookup"><span data-stu-id="75ca1-248">Gamma</span></span></p></th>
<th><p><span data-ttu-id="75ca1-249">差異</span><span class="sxs-lookup"><span data-stu-id="75ca1-249">Delta</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75ca1-250">1</span><span class="sxs-lookup"><span data-stu-id="75ca1-250">1</span></span></p></td>
<td><p><span data-ttu-id="75ca1-251">ABC</span><span class="sxs-lookup"><span data-stu-id="75ca1-251">ABC</span></span><br />
<span data-ttu-id="75ca1-252">GHI</span><span class="sxs-lookup"><span data-stu-id="75ca1-252">GHI</span></span><br />
<span data-ttu-id="75ca1-253">JKL</span><span class="sxs-lookup"><span data-stu-id="75ca1-253">JKL</span></span></p></td>
<td><p><span data-ttu-id="75ca1-254">MNO</span><span class="sxs-lookup"><span data-stu-id="75ca1-254">MNO</span></span><br />
<span data-ttu-id="75ca1-255">PQR</span><span class="sxs-lookup"><span data-stu-id="75ca1-255">PQR</span></span><br />
<span data-ttu-id="75ca1-256">斯圖</span><span class="sxs-lookup"><span data-stu-id="75ca1-256">STU</span></span></p></td>
<td><p><span data-ttu-id="75ca1-257">VWX</span><span class="sxs-lookup"><span data-stu-id="75ca1-257">VWX</span></span><br />
<span data-ttu-id="75ca1-258">YZ</span><span class="sxs-lookup"><span data-stu-id="75ca1-258">YZ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75ca1-259">2</span><span class="sxs-lookup"><span data-stu-id="75ca1-259">2</span></span></p></td>
<td><p><span data-ttu-id="75ca1-260">，</span><span class="sxs-lookup"><span data-stu-id="75ca1-260">THE</span></span></p></td>
<td><p><span data-ttu-id="75ca1-261">雨</span><span class="sxs-lookup"><span data-stu-id="75ca1-261">RAIN</span></span><br />
<span data-ttu-id="75ca1-262">西班牙</span><span class="sxs-lookup"><span data-stu-id="75ca1-262">SPAIN</span></span></p></td>
<td><p><span data-ttu-id="75ca1-263">IN</span><span class="sxs-lookup"><span data-stu-id="75ca1-263">IN</span></span><br />
<span data-ttu-id="75ca1-264">瀑布</span><span class="sxs-lookup"><span data-stu-id="75ca1-264">FALLS</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="75ca1-265">將會儲存下列索引元組：</span><span class="sxs-lookup"><span data-stu-id="75ca1-265">The following index-tuples will be stored:</span></span>

<span data-ttu-id="75ca1-266">{1，ABC，MNO，VWX}</span><span class="sxs-lookup"><span data-stu-id="75ca1-266">{1,ABC,MNO,VWX}</span></span>  
<span data-ttu-id="75ca1-267">{1，GHI，MNO，VWX}</span><span class="sxs-lookup"><span data-stu-id="75ca1-267">{1,GHI,MNO,VWX}</span></span>  
<span data-ttu-id="75ca1-268">{1，JKL，MNO，VWX}</span><span class="sxs-lookup"><span data-stu-id="75ca1-268">{1,JKL,MNO,VWX}</span></span>  
<span data-ttu-id="75ca1-269">{2，，雨，IN}</span><span class="sxs-lookup"><span data-stu-id="75ca1-269">{2,THE,RAIN,IN}</span></span>

<span data-ttu-id="75ca1-270">請注意，雖然第二個數據列中的 Alpha 資料行會有單一多重值，但不會儲存 {2，，西班牙，IN}。</span><span class="sxs-lookup"><span data-stu-id="75ca1-270">Note that {2,THE,SPAIN,IN} is not stored, even though the Alpha column in the second row happens to have a single multivalue.</span></span>

<span data-ttu-id="75ca1-271">從 Windows Vista 開始的 Windows 版本中，您可以藉由指定 JET_bitIndexCrossProduct，在索引中展開所有多重值資料行。</span><span class="sxs-lookup"><span data-stu-id="75ca1-271">In versions of Windows starting with Windows Vista, all multivalued columns can be expanded in the index by specifying JET_bitIndexCrossProduct.</span></span>

### <a name="requirements"></a><span data-ttu-id="75ca1-272">規格需求</span><span class="sxs-lookup"><span data-stu-id="75ca1-272">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75ca1-273"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="75ca1-273"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="75ca1-274">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="75ca1-274">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75ca1-275"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="75ca1-275"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="75ca1-276">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="75ca1-276">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75ca1-277"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="75ca1-277"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="75ca1-278">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="75ca1-278">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75ca1-279"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="75ca1-279"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="75ca1-280">實作為 <strong>JET_ INDEXCREATE2_W</strong> (Unicode) 和 <strong>JET_</strong> INDEXCREATE2_A (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="75ca1-280">Implemented as <strong>JET_ INDEXCREATE2_W</strong> (Unicode) and <strong>JET_ INDEXCREATE2_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="75ca1-281">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75ca1-281">See also</span></span>

[<span data-ttu-id="75ca1-282">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="75ca1-282">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="75ca1-283">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="75ca1-283">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="75ca1-284">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="75ca1-284">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="75ca1-285">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="75ca1-285">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="75ca1-286">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="75ca1-286">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="75ca1-287">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="75ca1-287">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="75ca1-288">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="75ca1-288">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="75ca1-289">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="75ca1-289">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="75ca1-290">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="75ca1-290">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="75ca1-291">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="75ca1-291">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="75ca1-292">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="75ca1-292">JetUpdate</span></span>](./jetupdate-function.md)
