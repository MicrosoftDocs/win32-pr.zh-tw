---
description: 近端詞彙是用來指定兩個內容搜尋詞彙必須相對接近另一個，才能辨識為包含述詞的相符項。
ms.assetid: cbc449b1-9f1d-42a2-b39e-d5cd69c052df
title: 近乎長遠
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4676ec8af80f674ca0b8124d8b4f941d0d6f4936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318159"
---
# <a name="near-term"></a>近乎長遠

近端詞彙是用來指定兩個內容搜尋詞彙必須相對接近另一個，才能辨識為 [包含](-search-sql-contains.md) 述詞的相符項。

NEAR 的語法如下：


```
<content_search_term> NEAR | ~ <content_search_term>
```



近端詞彙可以「NEAR」或以波狀符號 (~) 來表示。

當您在所搜尋的資料行內，在大約50個單字內找到所聯結的單字時，NEAR 詞彙會傳回相符的結果。 這兩個字越接近，就越接近長期的計算次序。 這兩個字的距離越低，排名就越低。

> [!Note]  
> 找到的搜尋字詞之間的單字數目是近似值，視非搜尋字的外觀而定（例如 "a" 或 "a"），以及文字分隔 token 化文字的外觀。 可能小於50。

 


下表描述可在 CONTAINS 述詞中搭配 NEAR 詞彙使用的內容搜尋詞彙類型。



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
<td><pre><code>...WHERE CONTAINS(&#39;computer NEAR software)&#39;)</code></pre></td>
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
<td><pre><code>...WHERE CONTAINS(&#39;&quot;computer software&quot; NEAR hardware)&#39;</code></pre></td>
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
<td><pre><code>...WHERE CONTAINS(&#39;&quot;compu*&quot; NEAR &quot;soft*&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>

> [!Note]  
> 如果在所50搜尋的資料行中找到與 NEAR 相符的比對字，則結果仍會傳回，但順 [位](-search-sql-understandingrelevancevalues.md) 為0。

 

### <a name="example"></a>範例

下列範例會使用詞彙的簡短和完整形式來顯示接近詞彙的連結：


```
...WHERE CONTAINS('computer NEAR software ~ "setup application"')
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[WHERE 子句](-search-sql-where.md)
</dt> <dt>

**概念**
</dt> <dt>

[全文檢索述詞](-search-sql-fulltextpredicates.md)
</dt> <dt>

[在 CONTAINS 述詞中使用萬用字元](-search-sql-wildcards.md)
</dt> </dl>

 

 



