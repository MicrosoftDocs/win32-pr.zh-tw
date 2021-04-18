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
# <a name="near-term"></a><span data-ttu-id="284d7-103">近乎長遠</span><span class="sxs-lookup"><span data-stu-id="284d7-103">NEAR Term</span></span>

<span data-ttu-id="284d7-104">近端詞彙是用來指定兩個內容搜尋詞彙必須相對接近另一個，才能辨識為 [包含](-search-sql-contains.md) 述詞的相符項。</span><span class="sxs-lookup"><span data-stu-id="284d7-104">The NEAR term is used to specify that two content search terms must be relatively close to one another to be recognized as matching for the [CONTAINS](-search-sql-contains.md) predicate.</span></span>

<span data-ttu-id="284d7-105">NEAR 的語法如下：</span><span class="sxs-lookup"><span data-stu-id="284d7-105">The syntax for the NEAR term is:</span></span>


```
<content_search_term> NEAR | ~ <content_search_term>
```



<span data-ttu-id="284d7-106">近端詞彙可以「NEAR」或以波狀符號 (~) 來表示。</span><span class="sxs-lookup"><span data-stu-id="284d7-106">The NEAR term can be represented by the keyword "NEAR" or by a tilde (~).</span></span>

<span data-ttu-id="284d7-107">當您在所搜尋的資料行內，在大約50個單字內找到所聯結的單字時，NEAR 詞彙會傳回相符的結果。</span><span class="sxs-lookup"><span data-stu-id="284d7-107">When the words joined by NEAR in the query are found within approximately 50 words of each other inside the column being searched, the NEAR term returns a match.</span></span> <span data-ttu-id="284d7-108">這兩個字越接近，就越接近長期的計算次序。</span><span class="sxs-lookup"><span data-stu-id="284d7-108">The closer together the two words are, the higher the calculated rank for the NEAR term.</span></span> <span data-ttu-id="284d7-109">這兩個字的距離越低，排名就越低。</span><span class="sxs-lookup"><span data-stu-id="284d7-109">The farther apart the two words are, the lower the rank.</span></span>

> [!Note]  
> <span data-ttu-id="284d7-110">找到的搜尋字詞之間的單字數目是近似值，視非搜尋字的外觀而定（例如 "a" 或 "a"），以及文字分隔 token 化文字的外觀。</span><span class="sxs-lookup"><span data-stu-id="284d7-110">The number of words between found search terms is approximate and depends on the appearance of noise words, like "a" or "the", and how wordbreakers tokenize text.</span></span> <span data-ttu-id="284d7-111">可能小於50。</span><span class="sxs-lookup"><span data-stu-id="284d7-111">It may be less than 50.</span></span>

 


<span data-ttu-id="284d7-112">下表描述可在 CONTAINS 述詞中搭配 NEAR 詞彙使用的內容搜尋詞彙類型。</span><span class="sxs-lookup"><span data-stu-id="284d7-112">The following table describes content search term types that can be used with a NEAR term in a CONTAINS predicate.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="284d7-113">類型</span><span class="sxs-lookup"><span data-stu-id="284d7-113">Type</span></span></th>
<th><span data-ttu-id="284d7-114">描述</span><span class="sxs-lookup"><span data-stu-id="284d7-114">Description</span></span></th>
<th><span data-ttu-id="284d7-115">範例</span><span class="sxs-lookup"><span data-stu-id="284d7-115">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="284d7-116">Word</span><span class="sxs-lookup"><span data-stu-id="284d7-116">Word</span></span></td>
<td><span data-ttu-id="284d7-117">沒有空格或其他標點符號的單一單字。</span><span class="sxs-lookup"><span data-stu-id="284d7-117">A single word without spaces or other punctuation.</span></span> <span data-ttu-id="284d7-118">雙引號不是必要的。</span><span class="sxs-lookup"><span data-stu-id="284d7-118">Double quotation marks are not necessary.</span></span></td>
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
<td><span data-ttu-id="284d7-119">片語</span><span class="sxs-lookup"><span data-stu-id="284d7-119">Phrase</span></span></td>
<td><span data-ttu-id="284d7-120">多個單字或包含空格。</span><span class="sxs-lookup"><span data-stu-id="284d7-120">Multiple words or included spaces.</span></span></td>
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
<td><span data-ttu-id="284d7-121">萬用字元</span><span class="sxs-lookup"><span data-stu-id="284d7-121">Wildcard</span></span></td>
<td><span data-ttu-id="284d7-122">在結尾加上星號 ( \* ) 的單字或片語。</span><span class="sxs-lookup"><span data-stu-id="284d7-122">Words or phrases with the asterisk (\*) added to the end.</span></span> <span data-ttu-id="284d7-123">如需詳細資訊，請參閱在 <a href="-search-sql-wildcards.md">CONTAINS 述詞中使用萬用字元</a>。</span><span class="sxs-lookup"><span data-stu-id="284d7-123">For more information, see <a href="-search-sql-wildcards.md">Using Wildcards in the CONTAINS Predicate</a>.</span></span></td>
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
> <span data-ttu-id="284d7-124">如果在所50搜尋的資料行中找到與 NEAR 相符的比對字，則結果仍會傳回，但順 [位](-search-sql-understandingrelevancevalues.md) 為0。</span><span class="sxs-lookup"><span data-stu-id="284d7-124">If the match words specified with the NEAR term are both found in the column being searched, but are farther apart than 50 words, the result is still returned, but has a [rank](-search-sql-understandingrelevancevalues.md) of 0.</span></span>

 

### <a name="example"></a><span data-ttu-id="284d7-125">範例</span><span class="sxs-lookup"><span data-stu-id="284d7-125">Example</span></span>

<span data-ttu-id="284d7-126">下列範例會使用詞彙的簡短和完整形式來顯示接近詞彙的連結：</span><span class="sxs-lookup"><span data-stu-id="284d7-126">The following example shows chaining of NEAR terms, using both the short and long forms of the term:</span></span>


```
...WHERE CONTAINS('computer NEAR software ~ "setup application"')
```



## <a name="related-topics"></a><span data-ttu-id="284d7-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="284d7-127">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="284d7-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="284d7-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="284d7-129">WHERE 子句</span><span class="sxs-lookup"><span data-stu-id="284d7-129">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

<span data-ttu-id="284d7-130">**概念**</span><span class="sxs-lookup"><span data-stu-id="284d7-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="284d7-131">全文檢索述詞</span><span class="sxs-lookup"><span data-stu-id="284d7-131">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="284d7-132">在 CONTAINS 述詞中使用萬用字元</span><span class="sxs-lookup"><span data-stu-id="284d7-132">Using Wildcards in the CONTAINS Predicate</span></span>](-search-sql-wildcards.md)
</dt> </dl>

 

 



