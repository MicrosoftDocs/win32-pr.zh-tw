---
description: 深入瞭解： JET_INDEXCREATE 結構
title: JET_INDEXCREATE 結構
TOCTitle: JET_INDEXCREATE Structure
ms:assetid: 0c55f25c-d42a-49ba-a1fe-549850fdc9a6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269186(v=EXCHG.10)
ms:contentKeyID: 32765489
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
ms.openlocfilehash: 4c465d81dce628497b1b9210fb08b37a3003e2e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693932"
---
# <a name="jet_indexcreate-structure"></a><span data-ttu-id="1f917-103">JET_INDEXCREATE 結構</span><span class="sxs-lookup"><span data-stu-id="1f917-103">JET_INDEXCREATE Structure</span></span>


<span data-ttu-id="1f917-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1f917-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="1f917-105">**JET_INDEXCREATE** 結構包含對可延伸儲存引擎中的資料建立索引所需的資訊， (ESE) 資料庫。</span><span class="sxs-lookup"><span data-stu-id="1f917-105">The **JET_INDEXCREATE** structure contains the information needed to create an index over data in an Extensible Storage Engine (ESE) database.</span></span> <span data-ttu-id="1f917-106">結構是由函式（例如 [JetCreateIndex2](./jetcreateindex2-function.md)）和結構（例如 [JET_TABLECREATE](./jet-tablecreate-structure.md) 和 [JET_TABLECREATE2](./jet-tablecreate2-structure.md)）所使用。</span><span class="sxs-lookup"><span data-stu-id="1f917-106">The structure is used by functions such as [JetCreateIndex2](./jetcreateindex2-function.md), and in structures such as [JET_TABLECREATE](./jet-tablecreate-structure.md) and [JET_TABLECREATE2](./jet-tablecreate2-structure.md).</span></span>

``` c++
typedef struct tagJET_INDEXCREATE {
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
} JET_INDEXCREATE;
```

### <a name="members"></a><span data-ttu-id="1f917-107">成員</span><span class="sxs-lookup"><span data-stu-id="1f917-107">Members</span></span>

<span data-ttu-id="1f917-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="1f917-108">**cbStruct**</span></span>

<span data-ttu-id="1f917-109">此結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1f917-109">The size, in bytes, of this structure.</span></span> <span data-ttu-id="1f917-110">將這個成員設定為 sizeof ( JET_INDEXCREATE ) 。</span><span class="sxs-lookup"><span data-stu-id="1f917-110">Set this member to sizeof( JET_INDEXCREATE ).</span></span>

<span data-ttu-id="1f917-111">**szIndexName**</span><span class="sxs-lookup"><span data-stu-id="1f917-111">**szIndexName**</span></span>

<span data-ttu-id="1f917-112">要建立之索引的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f917-112">The name of the index to create.</span></span>

<span data-ttu-id="1f917-113">索引的名稱必須符合下列條件：</span><span class="sxs-lookup"><span data-stu-id="1f917-113">The name of the index must meet the following conditions:</span></span>

  - <span data-ttu-id="1f917-114">它必須小於 JET_cbNameMost，不包括終止的 null。</span><span class="sxs-lookup"><span data-stu-id="1f917-114">It must be less than JET_cbNameMost, not including the terminating null.</span></span>

  - <span data-ttu-id="1f917-115">它必須包含下列字元： 0 (零) 到9、A 到 Z、a 到 z，以及 "" 以外的所有其他標點符號 \!</span><span class="sxs-lookup"><span data-stu-id="1f917-115">It must consist of the following characters: 0 (zero) through 9, A through Z, a through z, and all other punctuation except for "\!"</span></span> <span data-ttu-id="1f917-116"> (驚嘆號) 、"、" (逗號) 、" \[ " (左括弧) 和 " \] " (右括弧) —也就是 ASCII 字元0x20、0x22 至0x2d、0x2f 至0x5a、0x5c、0x5d 到0x7f。</span><span class="sxs-lookup"><span data-stu-id="1f917-116">(exclamation point), "," (comma), "\[" (opening bracket), and "\]" (closing bracket) — that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="1f917-117">不得以空格開頭。</span><span class="sxs-lookup"><span data-stu-id="1f917-117">It must not begin with a space.</span></span>

  - <span data-ttu-id="1f917-118">它必須包含至少一個 nonspace 字元。</span><span class="sxs-lookup"><span data-stu-id="1f917-118">It must consist of at least one nonspace character.</span></span>

<span data-ttu-id="1f917-119">**szKey**</span><span class="sxs-lookup"><span data-stu-id="1f917-119">**szKey**</span></span>

<span data-ttu-id="1f917-120">以 null 分隔之標記的雙 null 結束字串指標。</span><span class="sxs-lookup"><span data-stu-id="1f917-120">A pointer to a double-null-terminated string of null-delimited tokens.</span></span>

<span data-ttu-id="1f917-121">每個權杖的格式為 " \<direction-specifier\> \<column-name\> "，其中的方向規格為 "+" 或 "-"。</span><span class="sxs-lookup"><span data-stu-id="1f917-121">Each token is of the form "\<direction-specifier\>\<column-name\>", where direction-specification is either "+" or "-".</span></span> <span data-ttu-id="1f917-122">例如，"+  abc \\ 0-def \\ 0 + Ghi 0" 的 szKey \\ 會以遞增順序來編制三個數據行 "abc" (的索引) 、"def" (以遞減順序) 和 "ghi" (遞增順序) 。</span><span class="sxs-lookup"><span data-stu-id="1f917-122">For example, a **szKey** of "+abc\\0-def\\0+ghi\\0" will index over the three columns "abc" (in ascending order), "def" (in descending order), and "ghi" (in ascending order).</span></span> <span data-ttu-id="1f917-123">在 C 語言中，字串常值具有隱含的 **Null** 結束字元;因此，上述字串將以雙 Null 結束。</span><span class="sxs-lookup"><span data-stu-id="1f917-123">In the C language, string literals have an implied **NULL** terminator; therefore, the above string will be terminated by a double-NULL.</span></span>

<span data-ttu-id="1f917-124">在 **szKey** 中指定的資料行數目不能超過與版本相依的常數)  (**JET_ccolKeyMost** 的值。</span><span class="sxs-lookup"><span data-stu-id="1f917-124">The number of columns specified in **szKey** may not exceed the value of **JET_ccolKeyMost** (a version-dependent constant).</span></span>

<span data-ttu-id="1f917-125">至少必須在 **szKey** 中命名一個資料行。</span><span class="sxs-lookup"><span data-stu-id="1f917-125">At least one column must be named in **szKey**.</span></span>

<span data-ttu-id="1f917-126">過時行為：在雙 Null 結束字元之後，您可以指定語言識別項， (傳遞到 MAKELCID ( langid 中的文字，SORT_DEFAULT ) ) 做為指定索引之 LCID 的方式。</span><span class="sxs-lookup"><span data-stu-id="1f917-126">Obsolete behavior: After the double-NULL terminator, it is possible to specify a language ID (a WORD which gets passed into MAKELCID( langid, SORT_DEFAULT ) ) as a way to specify the LCID for the index.</span></span> <span data-ttu-id="1f917-127">在 *grbit*) 中設定 JET_bitIndexUnicode，在 **szKey** 中指定語言識別項和 [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (中的 LCID 是不合法的。</span><span class="sxs-lookup"><span data-stu-id="1f917-127">It is illegal to specify both a language ID in **szKey** and an LCID in [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (by setting JET_bitIndexUnicode in *grbit*).</span></span>

<span data-ttu-id="1f917-128">已淘汰：在語言識別項之後，就可以將 **cbVarSegMac** 傳遞為 USHORT。</span><span class="sxs-lookup"><span data-stu-id="1f917-128">Deprecated: After the language ID, it is possible to pass **cbVarSegMac** as a USHORT.</span></span> <span data-ttu-id="1f917-129">如果在 **szKey** 中同時設定 USHORT，以及在結構中設定 **cbVarSegMac** ，則行為會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="1f917-129">The behavior is undefined if the USHORT is set both in **szKey** and if **cbVarSegMac** is set in the structure.</span></span>

<span data-ttu-id="1f917-130">**cbKey**</span><span class="sxs-lookup"><span data-stu-id="1f917-130">**cbKey**</span></span>

<span data-ttu-id="1f917-131">**SzKey** 的長度（以位元組為單位），包括兩個終止的 null。</span><span class="sxs-lookup"><span data-stu-id="1f917-131">The length, in bytes, of **szKey** including the two terminating nulls.</span></span>

<span data-ttu-id="1f917-132">**grbit**</span><span class="sxs-lookup"><span data-stu-id="1f917-132">**grbit**</span></span>

<span data-ttu-id="1f917-133">位群組，其中包含下表所列的零或多個值。</span><span class="sxs-lookup"><span data-stu-id="1f917-133">A group of bits that includes zero or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f917-134">值</span><span class="sxs-lookup"><span data-stu-id="1f917-134">Value</span></span></p></th>
<th><p><span data-ttu-id="1f917-135">意義</span><span class="sxs-lookup"><span data-stu-id="1f917-135">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f917-136">JET_bitIndexUnique</span><span class="sxs-lookup"><span data-stu-id="1f917-136">JET_bitIndexUnique</span></span></p></td>
<td><p><span data-ttu-id="1f917-137">不允許) 的索引項目重複 (索引鍵。</span><span class="sxs-lookup"><span data-stu-id="1f917-137">Duplicate index entries (keys) are not allowed.</span></span> <span data-ttu-id="1f917-138">呼叫 <a href="gg269288(v=exchg.10).md">JetUpdate</a> 時，不會強制執行這項功能，而不是在呼叫 <a href="gg294137(v=exchg.10).md">JetSetColumn</a> 時強制執行。</span><span class="sxs-lookup"><span data-stu-id="1f917-138">This is enforced when <a href="gg269288(v=exchg.10).md">JetUpdate</a> is called, not when <a href="gg294137(v=exchg.10).md">JetSetColumn</a> is called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f917-139">JET_bitIndexPrimary</span><span class="sxs-lookup"><span data-stu-id="1f917-139">JET_bitIndexPrimary</span></span></p></td>
<td><p><span data-ttu-id="1f917-140">索引是主要 (叢集) 索引。</span><span class="sxs-lookup"><span data-stu-id="1f917-140">The index is a primary (clustered) index.</span></span> <span data-ttu-id="1f917-141">每個資料表都必須只有一個主要索引。</span><span class="sxs-lookup"><span data-stu-id="1f917-141">Every table must have exactly one primary index.</span></span> <span data-ttu-id="1f917-142">如果未在資料表上明確定義主要索引，database engine 將會建立自己的主要索引。</span><span class="sxs-lookup"><span data-stu-id="1f917-142">If no primary index is explicitly defined over a table, the database engine will create its own primary index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f917-143">JET_bitIndexDisallowNull</span><span class="sxs-lookup"><span data-stu-id="1f917-143">JET_bitIndexDisallowNull</span></span></p></td>
<td><p><span data-ttu-id="1f917-144">建立索引的資料行都不能包含 <strong>Null</strong> 值。</span><span class="sxs-lookup"><span data-stu-id="1f917-144">None of the columns over which the index is created can contain a <strong>NULL</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f917-145">JET_bitIndexIgnoreNull</span><span class="sxs-lookup"><span data-stu-id="1f917-145">JET_bitIndexIgnoreNull</span></span></p></td>
<td><p><span data-ttu-id="1f917-146">如果要編制索引的所有資料行都是 <strong>Null</strong>，請勿加入資料列的索引項目。</span><span class="sxs-lookup"><span data-stu-id="1f917-146">Do not add an index entry for a row if all of the columns being indexed are <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f917-147">JET_bitIndexIgnoreAnyNull</span><span class="sxs-lookup"><span data-stu-id="1f917-147">JET_bitIndexIgnoreAnyNull</span></span></p></td>
<td><p><span data-ttu-id="1f917-148">如果要編制索引的任何資料行都是 <strong>Null</strong>，請勿加入資料列的索引項目。</span><span class="sxs-lookup"><span data-stu-id="1f917-148">Do not add an index entry for a row if any of the columns being indexed are <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f917-149">JET_bitIndexIgnoreFirstNull</span><span class="sxs-lookup"><span data-stu-id="1f917-149">JET_bitIndexIgnoreFirstNull</span></span></p></td>
<td><p><span data-ttu-id="1f917-150">如果要編制索引的第一個資料行是 <strong>Null</strong>，請勿加入資料列的索引項目。</span><span class="sxs-lookup"><span data-stu-id="1f917-150">Do not add an index entry for a row if the first column being indexed is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f917-151">JET_bitIndexLazyFlush</span><span class="sxs-lookup"><span data-stu-id="1f917-151">JET_bitIndexLazyFlush</span></span></p></td>
<td><p><span data-ttu-id="1f917-152">索引作業將會延遲記錄。</span><span class="sxs-lookup"><span data-stu-id="1f917-152">Index operations will be logged lazily.</span></span></p>
<p><span data-ttu-id="1f917-153">JET_bitIndexLazyFlush 不會影響資料更新的酷。</span><span class="sxs-lookup"><span data-stu-id="1f917-153">JET_bitIndexLazyFlush does not affect the laziness of data updates.</span></span> <span data-ttu-id="1f917-154">如果處理常式終止時，索引作業中斷，軟復原仍能讓資料庫處於一致的狀態，但索引可能不存在。</span><span class="sxs-lookup"><span data-stu-id="1f917-154">If the indexing operation is interrupted by process termination, Soft Recovery will still be able to able to get the database to a consistent state, but the index might not be present.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f917-155">JET_bitIndexEmpty</span><span class="sxs-lookup"><span data-stu-id="1f917-155">JET_bitIndexEmpty</span></span></p></td>
<td><p><span data-ttu-id="1f917-156">請勿嘗試建立索引，因為所有專案都會評估為 <strong>Null</strong>。</span><span class="sxs-lookup"><span data-stu-id="1f917-156">Do not attempt to build the index, because all entries would evaluate to <strong>NULL</strong>.</span></span> <span data-ttu-id="1f917-157">傳遞 JET_bitIndexEmpty 時， <strong>grbit</strong>也必須指定 JET_bitIgnoreAnyNull。</span><span class="sxs-lookup"><span data-stu-id="1f917-157"><strong>grbit</strong> must also specify JET_bitIgnoreAnyNull when JET_bitIndexEmpty is passed.</span></span> <span data-ttu-id="1f917-158">這是一項效能增強功能。</span><span class="sxs-lookup"><span data-stu-id="1f917-158">This is a performance enhancement.</span></span> <span data-ttu-id="1f917-159">例如，如果將新的資料行加入至資料表，就會在這個新加入的資料行上建立索引，並掃描資料表中的所有記錄，即使這些記錄未加入至索引也一樣。</span><span class="sxs-lookup"><span data-stu-id="1f917-159">For example, if a new column is added to a table, an index is created over this newly added column, and all the records in the table are scanned even though they are not added to the index.</span></span> <span data-ttu-id="1f917-160">指定 JET_bitIndexEmpty 會略過資料表掃描，這可能會花費很長的時間。</span><span class="sxs-lookup"><span data-stu-id="1f917-160">Specifying JET_bitIndexEmpty skips the scanning of the table, which could potentially take a long time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f917-161">JET_bitIndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="1f917-161">JET_bitIndexUnversioned</span></span></p></td>
<td><p><span data-ttu-id="1f917-162">導致其他交易可以看到索引建立。</span><span class="sxs-lookup"><span data-stu-id="1f917-162">Causes index creation to be visible to other transactions.</span></span> <span data-ttu-id="1f917-163">一般來說，交易中的會話將無法在另一個會話中看到索引建立作業。</span><span class="sxs-lookup"><span data-stu-id="1f917-163">Typically a session in a transaction will not be able to see an index creation operation in another session.</span></span> <span data-ttu-id="1f917-164">如果另一個交易可能建立相同的索引，則此旗標很有用。</span><span class="sxs-lookup"><span data-stu-id="1f917-164">This flag can be useful if another transaction is likely to create the same index.</span></span> <span data-ttu-id="1f917-165">第二個索引建立將會失敗，而不是可能導致許多不必要的資料庫作業。</span><span class="sxs-lookup"><span data-stu-id="1f917-165">The second index-create will fail instead of potentially causing many unnecessary database operations.</span></span> <span data-ttu-id="1f917-166">第二筆交易可能無法立即使用索引。</span><span class="sxs-lookup"><span data-stu-id="1f917-166">The second transaction might not be able to use the index immediately.</span></span> <span data-ttu-id="1f917-167">索引建立作業必須先完成，才可供使用。</span><span class="sxs-lookup"><span data-stu-id="1f917-167">The index creation operation has to complete before it is usable.</span></span> <span data-ttu-id="1f917-168">會話目前不能在交易中建立索引，而不需要版本資訊。</span><span class="sxs-lookup"><span data-stu-id="1f917-168">The session must not currently be in a transaction to create an index without version information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f917-169">JET_bitIndexSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="1f917-169">JET_bitIndexSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="1f917-170">指定此旗標會在索引中的所有資料行資料之後，將 <strong>Null</strong> 值排序。</span><span class="sxs-lookup"><span data-stu-id="1f917-170">Specifying this flag causes <strong>NULL</strong> values to be sorted after data for all columns in the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f917-171">JET_bitIndexUnicode</span><span class="sxs-lookup"><span data-stu-id="1f917-171">JET_bitIndexUnicode</span></span></p></td>
<td><p><span data-ttu-id="1f917-172">指定此旗標會影響結構中 lcid/pidxunicde 聯集欄位的解釋。</span><span class="sxs-lookup"><span data-stu-id="1f917-172">Specifying this flag affects the interpretation of the lcid/pidxunicde union field in the structure.</span></span> <span data-ttu-id="1f917-173">設定位表示 <strong>pidxunicode</strong> 欄位實際上會指向 <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> 結構。</span><span class="sxs-lookup"><span data-stu-id="1f917-173">Setting the bit means that the <strong>pidxunicode</strong> field actually points to a <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure.</span></span> <span data-ttu-id="1f917-174">需要 JET_bitIndexUnicode，才能編制 Unicode 資料的索引。</span><span class="sxs-lookup"><span data-stu-id="1f917-174">JET_bitIndexUnicode is not required in order to index Unicode data.</span></span> <span data-ttu-id="1f917-175">它僅用來自訂 Unicode 資料的正規化。</span><span class="sxs-lookup"><span data-stu-id="1f917-175">It is only used to customize the normalization of Unicode data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f917-176">JET_bitIndexTuples</span><span class="sxs-lookup"><span data-stu-id="1f917-176">JET_bitIndexTuples</span></span></p></td>
<td><p><span data-ttu-id="1f917-177">指定索引為元組索引。</span><span class="sxs-lookup"><span data-stu-id="1f917-177">Specifies that the index is a tuple index.</span></span> <span data-ttu-id="1f917-178">如需元組索引的描述，請參閱 <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> 。</span><span class="sxs-lookup"><span data-stu-id="1f917-178">See <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> for a description of a tuple index.</span></span></p>
<p><span data-ttu-id="1f917-179">JET_bitIndexTuples 是在 Windows XP 作業系統中引進。</span><span class="sxs-lookup"><span data-stu-id="1f917-179">JET_bitIndexTuples was introduced in the Windows XP operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f917-180">JET_bitIndexTupleLimits</span><span class="sxs-lookup"><span data-stu-id="1f917-180">JET_bitIndexTupleLimits</span></span></p></td>
<td><p><span data-ttu-id="1f917-181">指定此旗標會影響結構中 <strong>cbVarSegMac/ptuplelimits</strong> 聯集欄位的解釋。</span><span class="sxs-lookup"><span data-stu-id="1f917-181">Specifying this flag affects the interpretation of the <strong>cbVarSegMac/ptuplelimits</strong> union field in the structure.</span></span> <span data-ttu-id="1f917-182">設定此位表示 <strong>ptuplelimits</strong> 欄位實際上會指向 <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> 結構，以允許自訂元組索引限制 (暗示 JET_bitIndexTuples) 。</span><span class="sxs-lookup"><span data-stu-id="1f917-182">Setting this bit means that the <strong>ptuplelimits</strong> field actually points to a <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure to allow custom tuple index limits (implies JET_bitIndexTuples).</span></span></p>
<p><span data-ttu-id="1f917-183">Windows Server 2003 作業系統引進了 JET_bitIndexTupleLimits。</span><span class="sxs-lookup"><span data-stu-id="1f917-183">JET_bitIndexTupleLimits was introduced in the Windows Server 2003 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f917-184">JET_bitIndexCrossProduct 0x00004000</span><span class="sxs-lookup"><span data-stu-id="1f917-184">JET_bitIndexCrossProduct 0x00004000</span></span></p></td>
<td><p><span data-ttu-id="1f917-185">針對具有多值資料行之多個索引鍵資料行的索引指定此旗標，會導致針對這些索引鍵資料行中的所有值交叉乘積的每個結果建立索引項目。</span><span class="sxs-lookup"><span data-stu-id="1f917-185">Specifying this flag for an index that has more than one key column that is a multivalued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="1f917-186">否則，索引在最重要的索引鍵資料行中，每個多重值都只會有一個專案，這是多值資料行，而每個索引項目會使用任何其他索引鍵資料行的第一個多值資料行。</span><span class="sxs-lookup"><span data-stu-id="1f917-186">Otherwise, the index would only have one entry for each multivalue in the most significant key column that is a multivalued column and each of those index entries would use the first multivalue from any other key columns that are multivalued columns.</span></span></p>
<p><span data-ttu-id="1f917-187">例如，如果您對資料行 A 的索引指定此旗標，而資料行 A 的值為 &quot; 紅色 &quot; 和 &quot; 藍色， &quot; 而資料行 B 的值為 &quot; 1 &quot; 和2，則 &quot; &quot; 會建立下列索引項目： &quot; 紅色 &quot; 、 &quot; 1 &quot; ; &quot;紅色 &quot; 、 &quot; 2 &quot; ; &quot;藍色 &quot; 、 &quot; 1 &quot; ; &quot;藍色 &quot; 、 &quot; 2 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="1f917-187">For example, if you specified this flag for an index over column A that has the values &quot;red&quot; and &quot;blue&quot; and over column B that has the values &quot;1&quot; and &quot;2&quot; then the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;red&quot;, &quot;2&quot;; &quot;blue&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;2&quot;.</span></span> <span data-ttu-id="1f917-188">否則，將會建立下列索引項目： &quot; 紅色 &quot; 、 &quot; 1 &quot; ; &quot;藍色 &quot; 、 &quot; 1 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="1f917-188">Otherwise, the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;1&quot;.</span></span></p>
<p><span data-ttu-id="1f917-189">Windows Vista 作業系統引進了 JET_bitIndexCrossProduct。</span><span class="sxs-lookup"><span data-stu-id="1f917-189">JET_bitIndexCrossProduct was introduced in the Windows Vista operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f917-190">JET_bitIndexKeyMost 0x00008000</span><span class="sxs-lookup"><span data-stu-id="1f917-190">JET_bitIndexKeyMost 0x00008000</span></span></p></td>
<td><p><span data-ttu-id="1f917-191">指定此旗標將會導致索引使用結構中 <strong>cbKeyMost</strong> 欄位指定的最大索引鍵大小。</span><span class="sxs-lookup"><span data-stu-id="1f917-191">Specifying this flag will cause the index to use the maximum key size specified in the <strong>cbKeyMost</strong> field in the structure.</span></span> <span data-ttu-id="1f917-192">否則，索引會使用 JET_cbKeyMost (255) 做為其最大索引鍵大小。</span><span class="sxs-lookup"><span data-stu-id="1f917-192">Otherwise, the index will use JET_cbKeyMost (255) as its maximum key size.</span></span></p>
<p><span data-ttu-id="1f917-193">JET_bitIndexKeyMost 是在 Windows Vista 中引進的。</span><span class="sxs-lookup"><span data-stu-id="1f917-193">JET_bitIndexKeyMost was introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f917-194">JET_bitIndexDisallowTruncation 0x00010000</span><span class="sxs-lookup"><span data-stu-id="1f917-194">JET_bitIndexDisallowTruncation 0x00010000</span></span></p></td>
<td><p><span data-ttu-id="1f917-195">指定此旗標會導致索引的任何更新會導致截斷的金鑰因 JET_errKeyTruncated 而失敗。</span><span class="sxs-lookup"><span data-stu-id="1f917-195">Specifying this flag will cause any update to the index that would result in a truncated key to fail with JET_errKeyTruncated.</span></span> <span data-ttu-id="1f917-196">否則，將會以無訊息方式截斷金鑰。</span><span class="sxs-lookup"><span data-stu-id="1f917-196">Otherwise, keys will be silently truncated.</span></span> <span data-ttu-id="1f917-197">如需有關金鑰截斷的詳細資訊，請參閱 <a href="gg269329(v=exchg.10).md">JetMakeKey</a> 函數。</span><span class="sxs-lookup"><span data-stu-id="1f917-197">For more information on key truncation, see the <a href="gg269329(v=exchg.10).md">JetMakeKey</a> function.</span></span></p>
<p><span data-ttu-id="1f917-198"><strong>Windows vista： JET_bitIndexDisallowTruncation</strong> 是在 windows vista 中引進。</span><span class="sxs-lookup"><span data-stu-id="1f917-198"><strong>Windows Vista:  JET_bitIndexDisallowTruncation</strong> is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f917-199">JET_bitIndexNestedTable 0x00020000</span><span class="sxs-lookup"><span data-stu-id="1f917-199">JET_bitIndexNestedTable 0x00020000</span></span></p></td>
<td><p><span data-ttu-id="1f917-200">指定此旗標將會更新多個多值資料行的索引，但只會使用相同 <strong>itagSequence</strong>的值。</span><span class="sxs-lookup"><span data-stu-id="1f917-200">Specifying this flag will cause update the index over multiple multivalued columns but only with values of same <strong>itagSequence</strong>.</span></span></p>
<p><span data-ttu-id="1f917-201">JET_bitIndexNestedTable 是在 Windows Vista 中引進的。</span><span class="sxs-lookup"><span data-stu-id="1f917-201">JET_bitIndexNestedTable was introduced in Windows Vista.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1f917-202">**ulDensity**</span><span class="sxs-lookup"><span data-stu-id="1f917-202">**ulDensity**</span></span>

<span data-ttu-id="1f917-203">初始索引 B + 樹狀結構的百分比密度。</span><span class="sxs-lookup"><span data-stu-id="1f917-203">The percentage density of the initial index B+ tree.</span></span> <span data-ttu-id="1f917-204">指定小於100的數位，一開始就會使用較多的空間來建立索引，但允許未來的索引成長，進而避免發生內部片段。</span><span class="sxs-lookup"><span data-stu-id="1f917-204">Specifying a number less than 100 uses up more space to create the index initially, but allows future growth of the index to be in place, thus avoiding internal fragmentation.</span></span>

<span data-ttu-id="1f917-205">**lcid**</span><span class="sxs-lookup"><span data-stu-id="1f917-205">**lcid**</span></span>

<span data-ttu-id="1f917-206">地區設定識別碼 (LCID) 在 *grbit* 參數中未指定 JET_bitIndexUnicode 值時正規化資料時所要使用的值。</span><span class="sxs-lookup"><span data-stu-id="1f917-206">The locale identifier (LCID) to use when normalizing the data when the JET_bitIndexUnicode value is not specified in the *grbit* parameter.</span></span> <span data-ttu-id="1f917-207">如果索引是透過 Unicode 資料行，則 LCID 會影響正規化。</span><span class="sxs-lookup"><span data-stu-id="1f917-207">The LCID affects the normalization if the index is over Unicode columns.</span></span>

<span data-ttu-id="1f917-208">**pidxunicode**</span><span class="sxs-lookup"><span data-stu-id="1f917-208">**pidxunicode**</span></span>

<span data-ttu-id="1f917-209">如果在 *grbit* 參數中指定了 JET_bitIndexUnicode 值，則為 [JET_UNICODEINDEX](./jet-unicodeindex-structure.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="1f917-209">A pointer to a [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) structure if the JET_bitIndexUnicode value is specified in the *grbit* parameter.</span></span> <span data-ttu-id="1f917-210">這可讓使用者指定在 Unicode 正規化期間傳遞至 [LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) 函數的自訂旗標。</span><span class="sxs-lookup"><span data-stu-id="1f917-210">This allows the user to specify custom flags that get passed to the [LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) function during Unicode normalization.</span></span>

<span data-ttu-id="1f917-211">**cbVarSegMac**</span><span class="sxs-lookup"><span data-stu-id="1f917-211">**cbVarSegMac**</span></span>

<span data-ttu-id="1f917-212">*Grbit* 參數中未指定 JET_bitIndexTupleLimits 值時，每個資料行要儲存在索引中的最大長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1f917-212">The maximum length, in bytes, of each column to store in the index when the JET_bitIndexTupleLimits value is not specified in the *grbit* parameter.</span></span>

<span data-ttu-id="1f917-213">將此欄位的值指定為 0 (零) 相當於：</span><span class="sxs-lookup"><span data-stu-id="1f917-213">Specifying a value of 0 (zero) for this field is equivalent to:</span></span>

  - <span data-ttu-id="1f917-214">指定主要索引的 JET_cbPrimaryKeyMost。</span><span class="sxs-lookup"><span data-stu-id="1f917-214">Specifying JET_cbPrimaryKeyMost for a primary index.</span></span>

  - <span data-ttu-id="1f917-215">指定次要索引的 JET_cbSecondaryKeyMost。</span><span class="sxs-lookup"><span data-stu-id="1f917-215">Specifying JET_cbSecondaryKeyMost for a secondary index.</span></span>

<span data-ttu-id="1f917-216">**ptuplelimits**</span><span class="sxs-lookup"><span data-stu-id="1f917-216">**ptuplelimits**</span></span>

<span data-ttu-id="1f917-217">如果在 *grbit* 參數中指定了 JET_bitIndexTupleLimits 值，則為 [JET_TUPLELIMITS](./jet-tuplelimits-structure.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="1f917-217">A pointer to a [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure if the JET_bitIndexTupleLimits value is specified in the *grbit* parameter.</span></span>

<span data-ttu-id="1f917-218">ptuplelimits 是在 Windows Server 2003 中引進。</span><span class="sxs-lookup"><span data-stu-id="1f917-218">ptuplelimits was introduced in Windows Server 2003.</span></span>

<span data-ttu-id="1f917-219">**rgconditionalcolumn**</span><span class="sxs-lookup"><span data-stu-id="1f917-219">**rgconditionalcolumn**</span></span>

<span data-ttu-id="1f917-220">[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)結構陣列的選擇性參數，用來指定索引中的條件資料行。</span><span class="sxs-lookup"><span data-stu-id="1f917-220">An optional parameter to an array of [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) structures, which are used to specify the conditional columns in the index.</span></span>

<span data-ttu-id="1f917-221">**cConditionalColumn**</span><span class="sxs-lookup"><span data-stu-id="1f917-221">**cConditionalColumn**</span></span>

<span data-ttu-id="1f917-222">**Rgconditionalcolumn** 陣列中的結構計數。</span><span class="sxs-lookup"><span data-stu-id="1f917-222">The count of structures in the **rgconditionalcolumn** array.</span></span>

<span data-ttu-id="1f917-223">**犯 錯**</span><span class="sxs-lookup"><span data-stu-id="1f917-223">**err**</span></span>

<span data-ttu-id="1f917-224">包含用來建立此索引的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="1f917-224">Contains the return code for creating this index.</span></span>

<span data-ttu-id="1f917-225">**cbKeyMost**</span><span class="sxs-lookup"><span data-stu-id="1f917-225">**cbKeyMost**</span></span>

<span data-ttu-id="1f917-226">針對索引中的索引鍵，指定允許的最大大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1f917-226">Specifies the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="1f917-227">如果未在 *grbit* 參數中指定 JET_bitIndexKeyMost 值，則會忽略此參數。</span><span class="sxs-lookup"><span data-stu-id="1f917-227">This parameter is ignored if the JET_bitIndexKeyMost value is not specified in the *grbit* parameter.</span></span> <span data-ttu-id="1f917-228">如果這個參數設定為零，而且在 *grbit* 參數中指定 JET_bitIndexKeyMost，則呼叫函式將會失敗並出現 JET_err_InvalidDef。</span><span class="sxs-lookup"><span data-stu-id="1f917-228">If this parameter is set to zero, and JET_bitIndexKeyMost is specified in the *grbit* parameter, the calling function will fail with JET_err_InvalidDef.</span></span>

<span data-ttu-id="1f917-229">最小支援的金鑰大小為 JET_cbKeyMostMin (255) ，也就是舊版的最大索引鍵大小。</span><span class="sxs-lookup"><span data-stu-id="1f917-229">The minimum supported maximum key size is JET_cbKeyMostMin (255), which is the legacy maximum key size.</span></span>

<span data-ttu-id="1f917-230">金鑰大小上限取決於資料庫頁面大小 (JET_paramDatabasePageSize) ，如下所示：</span><span class="sxs-lookup"><span data-stu-id="1f917-230">The maximum key size is dependent on the database page size (JET_paramDatabasePageSize), as follows:</span></span>

  - <span data-ttu-id="1f917-231">如果 JET_paramDatabasePageSize = 2048，則 JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost2KBytePage (500) </span><span class="sxs-lookup"><span data-stu-id="1f917-231">If JET_paramDatabasePageSize = 2048 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost2KBytePage (500)</span></span>

  - <span data-ttu-id="1f917-232">如果 JET_paramDatabasePageSize = 4096，則 JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost4KBytePage (1000) </span><span class="sxs-lookup"><span data-stu-id="1f917-232">If JET_paramDatabasePageSize = 4096 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost4KBytePage (1000)</span></span>

  - <span data-ttu-id="1f917-233">如果 JET_paramDatabasePageSize = 8192，則 JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost8KBytePage (2000) </span><span class="sxs-lookup"><span data-stu-id="1f917-233">If JET_paramDatabasePageSize = 8192 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost8KBytePage (2000)</span></span>

<span data-ttu-id="1f917-234">您也可以從 JET_paramKeyMost 系統參數讀取實例的支援金鑰大小上限。</span><span class="sxs-lookup"><span data-stu-id="1f917-234">The maximum supported key size for the instance can also be read from the JET_paramKeyMost system parameter.</span></span>

<span data-ttu-id="1f917-235">**cbKeyMost** 是在 Windows Vista 中引進的。</span><span class="sxs-lookup"><span data-stu-id="1f917-235">**cbKeyMost** was introduced in Windows Vista.</span></span>

### <a name="remarks"></a><span data-ttu-id="1f917-236">備註</span><span class="sxs-lookup"><span data-stu-id="1f917-236">Remarks</span></span>

<span data-ttu-id="1f917-237">ESE 支援在包含多個值的索引鍵資料行上編制索引。</span><span class="sxs-lookup"><span data-stu-id="1f917-237">ESE supports indexing over key columns containing multiple values.</span></span> <span data-ttu-id="1f917-238">若要使用這項功能，資料行必須是標記的資料行類型 (JET_bitColumnTagged) ，且必須加上旗標，以 JET_bitColumnMultiValued 為其建立多個值。</span><span class="sxs-lookup"><span data-stu-id="1f917-238">To use this feature, the column must be a tagged column type (JET_bitColumnTagged), and it must be flagged to have its multiple values indexed with JET_bitColumnMultiValued.</span></span> <span data-ttu-id="1f917-239">在 Windows Vista 之前的 Windows 版本中，只有索引中的第一個多重值索引鍵資料行會在索引中展開其值。</span><span class="sxs-lookup"><span data-stu-id="1f917-239">In versions of Windows earlier than Windows Vista, only the first multivalued key column in the index will have its values expanded in the index.</span></span> <span data-ttu-id="1f917-240">所有其他多值和標記的資料行只會在索引中展開其第一個值。</span><span class="sxs-lookup"><span data-stu-id="1f917-240">All other multivalued and tagged columns will only have their first values expanded in the index.</span></span>

<span data-ttu-id="1f917-241">假設資料表中有下列資料列 (資料行 Alpha 不是多重值，而資料行 Beta、Gamma 和 Delta 是多重值) ，而且索引建立為 "+ Alpha \\ 0 + Beta \\ 0 + Gamma \\ 0 + Delta \\ 0 \\ 0"：</span><span class="sxs-lookup"><span data-stu-id="1f917-241">Assuming the following rows exist in a table (column Alpha is not multivalued, while columns Beta, Gamma, and Delta are multivalued), and an index is created as "+Alpha\\0+Beta\\0+Gamma\\0+Delta\\0\\0":</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f917-242">Alpha</span><span class="sxs-lookup"><span data-stu-id="1f917-242">Alpha</span></span></p></th>
<th><p><span data-ttu-id="1f917-243">Beta</span><span class="sxs-lookup"><span data-stu-id="1f917-243">Beta</span></span></p></th>
<th><p><span data-ttu-id="1f917-244">色差補正</span><span class="sxs-lookup"><span data-stu-id="1f917-244">Gamma</span></span></p></th>
<th><p><span data-ttu-id="1f917-245">差異</span><span class="sxs-lookup"><span data-stu-id="1f917-245">Delta</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f917-246">1</span><span class="sxs-lookup"><span data-stu-id="1f917-246">1</span></span></p></td>
<td><p><span data-ttu-id="1f917-247">ABC</span><span class="sxs-lookup"><span data-stu-id="1f917-247">ABC</span></span><br />
<span data-ttu-id="1f917-248">GHI</span><span class="sxs-lookup"><span data-stu-id="1f917-248">GHI</span></span><br />
<span data-ttu-id="1f917-249">JKL</span><span class="sxs-lookup"><span data-stu-id="1f917-249">JKL</span></span></p></td>
<td><p><span data-ttu-id="1f917-250">MNO</span><span class="sxs-lookup"><span data-stu-id="1f917-250">MNO</span></span><br />
<span data-ttu-id="1f917-251">PQR</span><span class="sxs-lookup"><span data-stu-id="1f917-251">PQR</span></span><br />
<span data-ttu-id="1f917-252">斯圖</span><span class="sxs-lookup"><span data-stu-id="1f917-252">STU</span></span></p></td>
<td><p><span data-ttu-id="1f917-253">VWX</span><span class="sxs-lookup"><span data-stu-id="1f917-253">VWX</span></span><br />
<span data-ttu-id="1f917-254">YZ</span><span class="sxs-lookup"><span data-stu-id="1f917-254">YZ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f917-255">2</span><span class="sxs-lookup"><span data-stu-id="1f917-255">2</span></span></p></td>
<td><p><span data-ttu-id="1f917-256">，</span><span class="sxs-lookup"><span data-stu-id="1f917-256">THE</span></span></p></td>
<td><p><span data-ttu-id="1f917-257">雨</span><span class="sxs-lookup"><span data-stu-id="1f917-257">RAIN</span></span><br />
<span data-ttu-id="1f917-258">西班牙</span><span class="sxs-lookup"><span data-stu-id="1f917-258">SPAIN</span></span></p></td>
<td><p><span data-ttu-id="1f917-259">IN</span><span class="sxs-lookup"><span data-stu-id="1f917-259">IN</span></span><br />
<span data-ttu-id="1f917-260">瀑布</span><span class="sxs-lookup"><span data-stu-id="1f917-260">FALLS</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1f917-261">即將儲存的索引元組：</span><span class="sxs-lookup"><span data-stu-id="1f917-261">The falling index-tuples will be stored:</span></span>

<span data-ttu-id="1f917-262">{1，ABC，MNO，VWX}</span><span class="sxs-lookup"><span data-stu-id="1f917-262">{1,ABC,MNO,VWX}</span></span>  
<span data-ttu-id="1f917-263">{1，GHI，MNO，VWX}</span><span class="sxs-lookup"><span data-stu-id="1f917-263">{1,GHI,MNO,VWX}</span></span>  
<span data-ttu-id="1f917-264">{1，JKL，MNO，VWX}</span><span class="sxs-lookup"><span data-stu-id="1f917-264">{1,JKL,MNO,VWX}</span></span>  
<span data-ttu-id="1f917-265">{2，，雨，IN}</span><span class="sxs-lookup"><span data-stu-id="1f917-265">{2,THE,RAIN,IN}</span></span>

<span data-ttu-id="1f917-266">請注意，雖然第二個數據列中的 Alpha 資料行會有單一多重值，但不會儲存 {2，，西班牙，IN}。</span><span class="sxs-lookup"><span data-stu-id="1f917-266">Note that {2,THE,SPAIN,IN} is not stored, even though the Alpha column in the second row happens to have a single multivalue.</span></span>

<span data-ttu-id="1f917-267">從 Windows Vista 開始的 Windows 版本中，您可以藉由指定 JET_bitIndexCrossProduct，在索引中展開所有多重值資料行。</span><span class="sxs-lookup"><span data-stu-id="1f917-267">In versions of Windows starting with Windows Vista, all multivalued columns can be expanded in the index by specifying JET_bitIndexCrossProduct.</span></span>

### <a name="requirements"></a><span data-ttu-id="1f917-268">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f917-268">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f917-269"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="1f917-269"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1f917-270">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="1f917-270">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f917-271"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="1f917-271"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1f917-272">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="1f917-272">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f917-273"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="1f917-273"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1f917-274">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="1f917-274">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f917-275"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="1f917-275"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="1f917-276">實作為 <strong>JET_ INDEXCREATE_W</strong> (Unicode) 和 <strong>JET_</strong> INDEXCREATE_A (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="1f917-276">Implemented as <strong>JET_ INDEXCREATE_W</strong> (Unicode) and <strong>JET_ INDEXCREATE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="1f917-277">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f917-277">See also</span></span>

[<span data-ttu-id="1f917-278">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="1f917-278">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="1f917-279">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="1f917-279">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="1f917-280">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1f917-280">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1f917-281">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="1f917-281">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="1f917-282">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="1f917-282">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="1f917-283">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="1f917-283">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="1f917-284">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="1f917-284">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="1f917-285">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="1f917-285">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="1f917-286">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="1f917-286">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="1f917-287">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="1f917-287">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="1f917-288">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="1f917-288">JetUpdate</span></span>](./jetupdate-function.md)
