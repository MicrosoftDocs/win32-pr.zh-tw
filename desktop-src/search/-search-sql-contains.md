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
# <a name="contains-predicate"></a>CONTAINS 述詞

CONTAINS 述詞是 WHERE 子句的一部分，而且支援在文字資料行中搜尋單字和片語。 CONTAINS 述詞具有可比對單字的功能、符合字形變化形式的單字、使用萬用字元搜尋，以及使用相近程度搜尋。 您也可以在 CONTAINS 述詞中套用權數，以設定找到搜尋字詞之資料行的重要性。 CONTAINS 述詞較適用于完全相符的專案，相對於 [FREETEXT](-search-sql-freetext.md) 述詞，更適合用來尋找包含在整個資料行中散佈之搜尋字組組合的檔。 搜尋不會區分大小寫。

以下是 CONTAINS 述詞的基本語法：

```SQL
...CONTAINS(["<fulltext_column>",]'<contains_condition>'[,<LCID>])...
```

全文檢索資料 \_ 行參考是選擇性的。 您可以使用它來限制搜尋單一資料行，或將包含述詞測試的資料行群組。 當全文檢索資料行指定為 "ALL" 或 " \* " 時，就會搜尋所有已編制索引的 text 屬性。 雖然資料行不需要是文字屬性，但如果資料行是其他資料類型，則結果可能沒有意義。 資料行名稱可以是一般或分隔的 [識別碼](-search-sql-identifiers.md)，而且您必須將它與條件分隔（以逗號分隔）。 如果未指定全文檢索資料行，則會使用 [system.string] 資料行，這是檔的主體。

述詞的 LCID 部分會指定搜尋地區設定。 這會指示搜尋引擎針對搜尋查詢使用適當的斷詞工具和字形變化表單。 若要指定地區設定，請提供 Windows standard language code 識別碼 (LCID) 。 例如，1033是美國的 LCID （英文）。 將 LCID 放在 CONTAINS 子句括弧內的最後一個專案。 如需搜尋和語言的重要資訊，請參閱 [使用當地語系化的搜尋](-search-sql-usinglocsearches.md)。

> [!NOTE]  
> 預設搜尋地區設定是系統預設的地區設定。

Contains \_ 條件部分必須以單引號括住，以用於片語的單引號或雙引號，並包含一或多個使用邏輯運算子 **和** 或 **或** 的內容搜尋詞彙。 您可以使用 **不** 在 **AND** 運算子之後的選擇性一元運算子來消除內容搜尋詞彙的邏輯值。

> [!NOTE]  
> **NOT** 運算子只能在 **和** 之後發生。 如果只有一個比對條件，或在 **or** 運算子之後，您就無法使用 **NOT** 運算子。

您可以使用括弧來群組和嵌入內容搜尋詞彙。 下表描述邏輯運算子的優先順序順序。

| 順序 (優先順序)  | 邏輯運算子 |
|--------------------|------------------|
| 第一個 (最高)     | **NOT**          |
| Second             | **AND**          |
| 第三 (最低)      | **OR**           |

相同類型的邏輯運算子是關聯性，而且沒有指定的計算順序。 例如， (A **和** B) **，而且** (C **和** d) 可以計算 (B **和** C) **，以及** (A **和** d) ，但邏輯結果不會有任何變更。

下表說明內容搜尋詞彙的類型。

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>類型</th>
<th>描述</th>
<th>範例</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Word</td>
<td>沒有空格或其他標點符號的單一單字。 雙引號不是必要的。</td>
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
<td>片語</td>
<td>多個單字或包含空格。</td>
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
<td>萬用字元</td>
<td>在結尾加上星號 ( * ) 的單字或片語。 如需詳細資訊，請參閱在 <a href="-search-sql-wildcards.md">CONTAINS 述詞中使用萬用字元</a>。</td>
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
<td>全文檢索資料行</td>
<td>要與其余查詢比對的屬性資料行名稱。</td>
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
<td>Boolean</td>
<td>使用布林運算子 <strong>and</strong>、 <strong>or 或</strong> <strong>NOT</strong>結合的單字、片語和萬用字元字串。 以雙引號括住布林詞彙。</td>
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
<td>Near</td>
<td>以接近函數分隔的單字、片語或萬用字元。 如需詳細資訊，請參閱 <a href="-search-sql-near.md">近乎長遠</a>。</td>
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
<td>FormsOf</td>
<td>符合該單字的單字與字形變化版本。 如需詳細資訊，請參閱 <a href="-search-sql-formsof.md">FORMSOF 字詞</a>。</td>
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
<td>IsAbout</td>
<td>結合多個單字、片語或萬用字元搜尋詞彙的相符結果。 每個搜尋字詞都可以選擇性地加權。 您可以選擇性地指定排名計算方法，其結合了加權以及檔所符合的專案數目。 如需詳細資訊，請參閱 <a href="-search-sql-isabout.md">ISABOUT 字詞</a>。</td>
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

本節包含下列主題：

- [在 CONTAINS 述詞中使用萬用字元](-search-sql-wildcards.md)
- [FORMSOF 字詞](-search-sql-formsof.md)
- [ISABOUT 字詞](-search-sql-isabout.md)
- [近乎長遠](-search-sql-near.md)

## <a name="related-topics"></a>相關主題

### <a name="reference"></a>參考

[WHERE 子句](-search-sql-where.md)

### <a name="conceptual"></a>概念

[全文檢索述詞](-search-sql-fulltextpredicates.md)

[非全文檢索述詞](-search-sql-nonfulltextpredicates.md)
