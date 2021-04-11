---
description: CONTAINS 述詞是 WHERE 子句的一部分，而且支援在文字資料行中搜尋單字和片語。
ms.assetid: 53083966-54cc-4a16-a161-caa663bea7ea
title: CONTAINS 述詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 908f4c67d5c1d5bcf00c60bd8cb271928682a907
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847809"
---
# <a name="contains-predicate"></a><span data-ttu-id="f5364-103">CONTAINS 述詞</span><span class="sxs-lookup"><span data-stu-id="f5364-103">CONTAINS Predicate</span></span>

<span data-ttu-id="f5364-104">CONTAINS 述詞是 WHERE 子句的一部分，而且支援在文字資料行中搜尋單字和片語。</span><span class="sxs-lookup"><span data-stu-id="f5364-104">The CONTAINS predicate is part of the WHERE clause and supports searching for words and phrases in text columns.</span></span> <span data-ttu-id="f5364-105">CONTAINS 述詞具有可比對單字的功能、符合字形變化形式的單字、使用萬用字元搜尋，以及使用相近程度搜尋。</span><span class="sxs-lookup"><span data-stu-id="f5364-105">The CONTAINS predicate has features for matching words, matching inflectional forms of words, searching using wildcard characters, and searching using proximity.</span></span> <span data-ttu-id="f5364-106">您也可以在 CONTAINS 述詞中套用權數，以設定找到搜尋字詞之資料行的重要性。</span><span class="sxs-lookup"><span data-stu-id="f5364-106">You can also apply weights in a CONTAINS predicate to set the importance of the columns where the search term is found.</span></span> <span data-ttu-id="f5364-107">CONTAINS 述詞較適用于完全相符的專案，相對於 [FREETEXT](-search-sql-freetext.md) 述詞，更適合用來尋找包含在整個資料行中散佈之搜尋字組組合的檔。</span><span class="sxs-lookup"><span data-stu-id="f5364-107">The CONTAINS predicate is better suited for exact matches, in contrast to the [FREETEXT](-search-sql-freetext.md) predicate, which is better suited to finding documents containing combinations of the search words spread throughout the column.</span></span> <span data-ttu-id="f5364-108">搜尋不會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="f5364-108">Searches are not case-sensitive.</span></span>

<span data-ttu-id="f5364-109">以下是 CONTAINS 述詞的基本語法：</span><span class="sxs-lookup"><span data-stu-id="f5364-109">The following is the basic syntax of the CONTAINS predicate:</span></span>

```SQL
...CONTAINS(["<fulltext_column>",]'<contains_condition>'[,<LCID>])...
```

<span data-ttu-id="f5364-110">全文檢索資料 \_ 行參考是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="f5364-110">The fulltext\_column reference is optional.</span></span> <span data-ttu-id="f5364-111">您可以使用它來限制搜尋單一資料行，或將包含述詞測試的資料行群組。</span><span class="sxs-lookup"><span data-stu-id="f5364-111">With it, you can limit the search to a single column or a column group against which the CONTAINS predicate is tested.</span></span> <span data-ttu-id="f5364-112">當全文檢索資料行指定為 "ALL" 或 " \* " 時，就會搜尋所有已編制索引的 text 屬性。</span><span class="sxs-lookup"><span data-stu-id="f5364-112">When the fulltext column is specified as "ALL" or "\*", all indexed text properties are searched.</span></span> <span data-ttu-id="f5364-113">雖然資料行不需要是文字屬性，但如果資料行是其他資料類型，則結果可能沒有意義。</span><span class="sxs-lookup"><span data-stu-id="f5364-113">Although the column is not required to be a text property, the results might be meaningless if the column is some other data type.</span></span> <span data-ttu-id="f5364-114">資料行名稱可以是一般或分隔的 [識別碼](-search-sql-identifiers.md)，而且您必須將它與條件分隔（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="f5364-114">The column name can be either a regular or delimited [identifier](-search-sql-identifiers.md), and you must separate it from the condition by a comma.</span></span> <span data-ttu-id="f5364-115">如果未指定全文檢索資料行，則會使用 [system.string] 資料行，這是檔的主體。</span><span class="sxs-lookup"><span data-stu-id="f5364-115">If no fulltext column is specified, the System.Search.Contents column, which is the body of the document, is used.</span></span>

<span data-ttu-id="f5364-116">述詞的 LCID 部分會指定搜尋地區設定。</span><span class="sxs-lookup"><span data-stu-id="f5364-116">The LCID portion of the predicate specifies the search locale.</span></span> <span data-ttu-id="f5364-117">這會指示搜尋引擎針對搜尋查詢使用適當的斷詞工具和字形變化表單。</span><span class="sxs-lookup"><span data-stu-id="f5364-117">This instructs the search engine to use the appropriate word breaker and inflectional forms for the search query.</span></span> <span data-ttu-id="f5364-118">若要指定地區設定，請提供 Windows standard language code 識別碼 (LCID) 。</span><span class="sxs-lookup"><span data-stu-id="f5364-118">To specify the locale, provide the Windows standard language code identifier (LCID).</span></span> <span data-ttu-id="f5364-119">例如，1033是美國的 LCID （英文）。</span><span class="sxs-lookup"><span data-stu-id="f5364-119">For example, 1033 is the LCID for United States-English.</span></span> <span data-ttu-id="f5364-120">將 LCID 放在 CONTAINS 子句括弧內的最後一個專案。</span><span class="sxs-lookup"><span data-stu-id="f5364-120">Place the LCID as the last item inside the parentheses of the CONTAINS clause.</span></span> <span data-ttu-id="f5364-121">如需搜尋和語言的重要資訊，請參閱 [使用當地語系化的搜尋](-search-sql-usinglocsearches.md)。</span><span class="sxs-lookup"><span data-stu-id="f5364-121">For important information about searching and languages, see [Using Localized Searches](-search-sql-usinglocsearches.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="f5364-122">預設搜尋地區設定是系統預設的地區設定。</span><span class="sxs-lookup"><span data-stu-id="f5364-122">The default search locale is the system default locale.</span></span>

<span data-ttu-id="f5364-123">Contains \_ 條件部分必須以單引號括住，以用於片語的單引號或雙引號，並包含一或多個使用邏輯運算子 **和** 或 **或** 的內容搜尋詞彙。</span><span class="sxs-lookup"><span data-stu-id="f5364-123">The contains\_condition portion must be enclosed in single quotation marks for single words or double quotation marks for phrases, and consists of one or more content search terms that are combined using the logical operators **AND** or **OR**.</span></span> <span data-ttu-id="f5364-124">您可以使用 **不** 在 **AND** 運算子之後的選擇性一元運算子來消除內容搜尋詞彙的邏輯值。</span><span class="sxs-lookup"><span data-stu-id="f5364-124">You can use the optional unary operator **NOT** after an **AND** operator to negate the logical value of a content search term.</span></span>

> [!NOTE]  
> <span data-ttu-id="f5364-125">**NOT** 運算子只能在 **和** 之後發生。</span><span class="sxs-lookup"><span data-stu-id="f5364-125">The **NOT** operator can occur only after **AND**.</span></span> <span data-ttu-id="f5364-126">如果只有一個比對條件，或在 **or** 運算子之後，您就無法使用 **NOT** 運算子。</span><span class="sxs-lookup"><span data-stu-id="f5364-126">You cannot use the **NOT** operator if there is only one match condition, or after the **OR** operator.</span></span>

<span data-ttu-id="f5364-127">您可以使用括弧來群組和嵌入內容搜尋詞彙。</span><span class="sxs-lookup"><span data-stu-id="f5364-127">You can use parentheses to group and nest content search terms.</span></span> <span data-ttu-id="f5364-128">下表描述邏輯運算子的優先順序順序。</span><span class="sxs-lookup"><span data-stu-id="f5364-128">The following table describes the order of precedence for the logical operators.</span></span>

| <span data-ttu-id="f5364-129">順序 (優先順序) </span><span class="sxs-lookup"><span data-stu-id="f5364-129">Order (precedence)</span></span> | <span data-ttu-id="f5364-130">邏輯運算子</span><span class="sxs-lookup"><span data-stu-id="f5364-130">Logical operator</span></span> |
|--------------------|------------------|
| <span data-ttu-id="f5364-131">第一個 (最高) </span><span class="sxs-lookup"><span data-stu-id="f5364-131">First (highest)</span></span>    | <span data-ttu-id="f5364-132">**NOT**</span><span class="sxs-lookup"><span data-stu-id="f5364-132">**NOT**</span></span>          |
| <span data-ttu-id="f5364-133">Second</span><span class="sxs-lookup"><span data-stu-id="f5364-133">Second</span></span>             | <span data-ttu-id="f5364-134">**AND**</span><span class="sxs-lookup"><span data-stu-id="f5364-134">**AND**</span></span>          |
| <span data-ttu-id="f5364-135">第三 (最低) </span><span class="sxs-lookup"><span data-stu-id="f5364-135">Third (lowest)</span></span>     | <span data-ttu-id="f5364-136">**OR**</span><span class="sxs-lookup"><span data-stu-id="f5364-136">**OR**</span></span>           |

<span data-ttu-id="f5364-137">相同類型的邏輯運算子是關聯性，而且沒有指定的計算順序。</span><span class="sxs-lookup"><span data-stu-id="f5364-137">Logical operators of the same type are associative, and there is no specified calculation order.</span></span> <span data-ttu-id="f5364-138">例如， (A **和** B) **，而且** (C **和** d) 可以計算 (B **和** C) **，以及** (A **和** d) ，但邏輯結果不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="f5364-138">For example, (A **AND** B) **AND** (C **AND** D) can be calculated (B **AND** C) **AND** (A **AND** D) with no change in the logical result.</span></span>

<span data-ttu-id="f5364-139">下表說明內容搜尋詞彙的類型。</span><span class="sxs-lookup"><span data-stu-id="f5364-139">The following table describes the types of content search terms.</span></span>

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f5364-140">類型</span><span class="sxs-lookup"><span data-stu-id="f5364-140">Type</span></span></th>
<th><span data-ttu-id="f5364-141">描述</span><span class="sxs-lookup"><span data-stu-id="f5364-141">Description</span></span></th>
<th><span data-ttu-id="f5364-142">範例</span><span class="sxs-lookup"><span data-stu-id="f5364-142">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f5364-143">Word</span><span class="sxs-lookup"><span data-stu-id="f5364-143">Word</span></span></td>
<td><span data-ttu-id="f5364-144">沒有空格或其他標點符號的單一單字。</span><span class="sxs-lookup"><span data-stu-id="f5364-144">A single word without spaces or other punctuation.</span></span> <span data-ttu-id="f5364-145">雙引號不是必要的。</span><span class="sxs-lookup"><span data-stu-id="f5364-145">Double quotation marks are not necessary.</span></span></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS (&#39;computer&#39;)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5364-146">片語</span><span class="sxs-lookup"><span data-stu-id="f5364-146">Phrase</span></span></td>
<td><span data-ttu-id="f5364-147">多個單字或包含空格。</span><span class="sxs-lookup"><span data-stu-id="f5364-147">Multiple words or included spaces.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer software&quot;&#39;)

Or, to use a double quote mark:

... WHERE CONTAINS
(&#39;&quot;computer &quot;&quot;science&quot;&quot; &quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f5364-148">萬用字元</span><span class="sxs-lookup"><span data-stu-id="f5364-148">Wildcard</span></span></td>
<td><span data-ttu-id="f5364-149">在結尾加上星號 ( \* ) 的單字或片語。</span><span class="sxs-lookup"><span data-stu-id="f5364-149">Words or phrases with the asterisk (\*) added to the end.</span></span> <span data-ttu-id="f5364-150">如需詳細資訊，請參閱在 <a href="-search-sql-wildcards.md">CONTAINS 述詞中使用萬用字元</a>。</span><span class="sxs-lookup"><span data-stu-id="f5364-150">For more information, see <a href="-search-sql-wildcards.md">Using Wildcards in the CONTAINS Predicate</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;compu*&quot;&#39;)

Matches &quot;computer&quot;, &quot;computers&quot;,
&quot;computation&quot;, and &quot;compulsory&quot;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5364-151">全文檢索資料行</span><span class="sxs-lookup"><span data-stu-id="f5364-151">Full-text Column</span></span></td>
<td><span data-ttu-id="f5364-152">要與其余查詢比對的屬性資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="f5364-152">A property column name against which to match the remaining query.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS (System.Author,&#39;&quot;James&quot; OR &quot;Juan&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f5364-153">Boolean</span><span class="sxs-lookup"><span data-stu-id="f5364-153">Boolean</span></span></td>
<td><span data-ttu-id="f5364-154">使用布林運算子 <strong>and</strong>、 <strong>or 或</strong> <strong>NOT</strong>結合的單字、片語和萬用字元字串。</span><span class="sxs-lookup"><span data-stu-id="f5364-154">Words, phrases, and wildcard strings combined by using the Boolean operators <strong>AND</strong>, <strong>OR</strong>, or <strong>NOT</strong>.</span></span> <span data-ttu-id="f5364-155">以雙引號括住布林詞彙。</span><span class="sxs-lookup"><span data-stu-id="f5364-155">Enclose the Boolean terms in double quotation marks.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer monitor&quot; AND
  &quot;software program&quot; AND
  &quot;install component&quot;&#39;)

...WHERE CONTAINS
 (&#39; &quot;computer&quot; AND
  &quot;software&quot; AND
  &quot;install&quot; &#39; )

...WHERE CONTAINS
(&#39;&quot;computer software install&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5364-156">Near</span><span class="sxs-lookup"><span data-stu-id="f5364-156">Near</span></span></td>
<td><span data-ttu-id="f5364-157">以接近函數分隔的單字、片語或萬用字元。</span><span class="sxs-lookup"><span data-stu-id="f5364-157">Words, phrases, or wildcards separated by the function NEAR.</span></span> <span data-ttu-id="f5364-158">如需詳細資訊，請參閱 <a href="-search-sql-near.md">近乎長遠</a>。</span><span class="sxs-lookup"><span data-stu-id="f5364-158">For more information, see <a href="-search-sql-near.md">NEAR Term</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer&quot; NEAR &quot;software&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f5364-159">FormsOf</span><span class="sxs-lookup"><span data-stu-id="f5364-159">FormsOf</span></span></td>
<td><span data-ttu-id="f5364-160">符合該單字的單字與字形變化版本。</span><span class="sxs-lookup"><span data-stu-id="f5364-160">Matches a word and the inflectional versions of that word.</span></span> <span data-ttu-id="f5364-161">如需詳細資訊，請參閱 <a href="-search-sql-formsof.md">FORMSOF 字詞</a>。</span><span class="sxs-lookup"><span data-stu-id="f5364-161">For more information, see <a href="-search-sql-formsof.md">FORMSOF Term</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;FORMSOF
 (INFLECTIONAL, &quot;happy&quot;))

Matches &quot;happy&quot;, &quot;happier&quot;,
&quot;happiest&quot;, &quot;happily&quot;, and so on.</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5364-162">IsAbout</span><span class="sxs-lookup"><span data-stu-id="f5364-162">IsAbout</span></span></td>
<td><span data-ttu-id="f5364-163">結合多個單字、片語或萬用字元搜尋詞彙的相符結果。</span><span class="sxs-lookup"><span data-stu-id="f5364-163">Combines matching results over multiple word, phrase, or wildcard search terms.</span></span> <span data-ttu-id="f5364-164">每個搜尋字詞都可以選擇性地加權。</span><span class="sxs-lookup"><span data-stu-id="f5364-164">Each search term can optionally be weighted.</span></span> <span data-ttu-id="f5364-165">您可以選擇性地指定排名計算方法，其結合了加權以及檔所符合的專案數目。</span><span class="sxs-lookup"><span data-stu-id="f5364-165">You can optionally specify the rank calculation method, which combines the weights and how many of the items the document matches.</span></span> <span data-ttu-id="f5364-166">如需詳細資訊，請參閱 <a href="-search-sql-isabout.md">ISABOUT 字詞</a>。</span><span class="sxs-lookup"><span data-stu-id="f5364-166">For more information, see <a href="-search-sql-isabout.md">ISABOUT Term</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;ISABOUT ( &quot;computer&quot; WEIGHT (0.75) ,
    &quot;software&quot; WEIGHT (0.25) ,
    &quot;development&quot; WEIGHT (0.255)
 ) RANKMETHOD INNER PRODUCT
&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>
<!-- markdownlint-enable MD033 -->

<span data-ttu-id="f5364-167">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="f5364-167">This section includes the following topics:</span></span>

- [<span data-ttu-id="f5364-168">在 CONTAINS 述詞中使用萬用字元</span><span class="sxs-lookup"><span data-stu-id="f5364-168">Using Wildcards in the CONTAINS Predicate</span></span>](-search-sql-wildcards.md)
- [<span data-ttu-id="f5364-169">FORMSOF 字詞</span><span class="sxs-lookup"><span data-stu-id="f5364-169">FORMSOF Term</span></span>](-search-sql-formsof.md)
- [<span data-ttu-id="f5364-170">ISABOUT 字詞</span><span class="sxs-lookup"><span data-stu-id="f5364-170">ISABOUT Term</span></span>](-search-sql-isabout.md)
- [<span data-ttu-id="f5364-171">近乎長遠</span><span class="sxs-lookup"><span data-stu-id="f5364-171">NEAR Term</span></span>](-search-sql-near.md)

## <a name="related-topics"></a><span data-ttu-id="f5364-172">相關主題</span><span class="sxs-lookup"><span data-stu-id="f5364-172">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="f5364-173">參考</span><span class="sxs-lookup"><span data-stu-id="f5364-173">Reference</span></span>

[<span data-ttu-id="f5364-174">WHERE 子句</span><span class="sxs-lookup"><span data-stu-id="f5364-174">WHERE Clause</span></span>](-search-sql-where.md)

### <a name="conceptual"></a><span data-ttu-id="f5364-175">概念</span><span class="sxs-lookup"><span data-stu-id="f5364-175">Conceptual</span></span>

[<span data-ttu-id="f5364-176">全文檢索述詞</span><span class="sxs-lookup"><span data-stu-id="f5364-176">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)

[<span data-ttu-id="f5364-177">非全文檢索述詞</span><span class="sxs-lookup"><span data-stu-id="f5364-177">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
