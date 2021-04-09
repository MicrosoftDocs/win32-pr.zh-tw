---
description: ISABOUT 字詞符合一或多個搜尋詞彙群組的資料行。
ms.assetid: e2629c4c-4b44-4427-ac1d-17f55fd969e3
title: ISABOUT 字詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f79fc2fa4a56b3ca6b3b412141f096b282e3aa9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689868"
---
# <a name="isabout-term"></a>ISABOUT 字詞

**廢棄**

從 Windows 8 移除這項功能。 如果您撰寫新的應用程式，請避免使用這項已淘汰的功能。 如果您修改現有的應用程式，強烈建議您移除這項功能的任何相依性。

ISABOUT 字詞符合一或多個搜尋詞彙群組的資料行。 它具有下列語法：


```
ISABOUT(<components>) [RANKMETHOD <method>]
```



選擇性的 RANKMETHOD 字詞會指定用來排名符合一或多個元件之檔的計算方法。 如果未指定任何 RANKMETHOD，則會使用預設的 Jaccard 係數排名方法。

ISABOUT 字詞可以有一或多個元件。 在 [CONTAINS](-search-sql-contains.md) 述詞中指定的資料行會針對每個元件進行測試。 如果至少有一個元件相符，則檔會包含在結果中。 逗點分隔多個元件。

元件部分具有下列語法：


```
<match_term> [<weight_term>]
```



您可以使用選擇性權數詞彙來變更 ISABOUT 詞彙內每個詞彙的相對重要性。 如果未套用加權詞彙，則會隱含預設的1.0 權數。

下表描述可能的 match 詞彙類型。



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
<td>沒有空格或其他標點符號的單一單字。</td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
 (&#39;ISABOUT (&quot;computer&quot;,&quot;software&quot;)&#39;)</code></pre></td>
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
 (&#39;ISABOUT (&quot;computer software&quot;,&quot;hardware&quot;)&#39;)</code></pre></td>
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
 (&#39;ISABOUT (&quot;compu*&quot;,&quot;soft*&quot;)&#39;)

Matches &quot;computer&quot;, &quot;computers&quot;, &quot;computation&quot;, 
and &quot;compulsory&quot;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="isabout-column-weighting"></a>ISABOUT 資料行加權

ISABOUT 字詞會根據每份檔與查詢中的比對字片語相符的程度，來排列相符的檔。 您可以使用資料行加權，以比其他比對字詞更具重要性。 ISABOUT 詞彙中的每個相符詞彙都可以套用加權值。 權數會套用至單一比對字詞，並以關鍵字「權數」表示。 權數詞彙有兩種替代語法：


```
<match_term> WEIGHT(<weight_value>)
<match_term>:(<weight_value>)
```



權數值必須介於0到1.0 之間，且不能超過三位數。 指定超出此範圍的加權值會產生錯誤訊息。 詞彙的加權排名值會乘以詞彙的加權值。

如果未指定符合詞彙的權數，則會隱含預設值1.0。

### <a name="example"></a>範例

下列範例會針對加權值使用 long 和 short 語法，以將權數套用至兩個 ISABOUT 相符詞彙。


```
WHERE CONTAINS( System.FileName,
      'ISABOUT("computer" WEIGHT (0.75),"software":0.25)')
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[FREETEXT 述詞](-search-sql-freetext.md)
</dt> <dt>

[WHERE 子句](-search-sql-where.md)
</dt> </dl>

 

 



