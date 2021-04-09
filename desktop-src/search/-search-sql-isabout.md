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
# <a name="isabout-term"></a><span data-ttu-id="6d10c-103">ISABOUT 字詞</span><span class="sxs-lookup"><span data-stu-id="6d10c-103">ISABOUT Term</span></span>

<span data-ttu-id="6d10c-104">**廢棄**</span><span class="sxs-lookup"><span data-stu-id="6d10c-104">**Deprecated**</span></span>

<span data-ttu-id="6d10c-105">從 Windows 8 移除這項功能。</span><span class="sxs-lookup"><span data-stu-id="6d10c-105">This feature has been removed as of Windows 8.</span></span> <span data-ttu-id="6d10c-106">如果您撰寫新的應用程式，請避免使用這項已淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="6d10c-106">If you write new applications, avoid using this deprecated feature.</span></span> <span data-ttu-id="6d10c-107">如果您修改現有的應用程式，強烈建議您移除這項功能的任何相依性。</span><span class="sxs-lookup"><span data-stu-id="6d10c-107">If you modify existing applications, you are strongly encouraged to remove any dependency on this feature.</span></span>

<span data-ttu-id="6d10c-108">ISABOUT 字詞符合一或多個搜尋詞彙群組的資料行。</span><span class="sxs-lookup"><span data-stu-id="6d10c-108">The ISABOUT term matches columns against a group of one or more search terms.</span></span> <span data-ttu-id="6d10c-109">它具有下列語法：</span><span class="sxs-lookup"><span data-stu-id="6d10c-109">It has the following syntax:</span></span>


```
ISABOUT(<components>) [RANKMETHOD <method>]
```



<span data-ttu-id="6d10c-110">選擇性的 RANKMETHOD 字詞會指定用來排名符合一或多個元件之檔的計算方法。</span><span class="sxs-lookup"><span data-stu-id="6d10c-110">The optional RANKMETHOD term specifies the calculation method used to rank the documents that match one or more of the components.</span></span> <span data-ttu-id="6d10c-111">如果未指定任何 RANKMETHOD，則會使用預設的 Jaccard 係數排名方法。</span><span class="sxs-lookup"><span data-stu-id="6d10c-111">If no RANKMETHOD is specified, the default Jaccard Coefficient ranking method is used.</span></span>

<span data-ttu-id="6d10c-112">ISABOUT 字詞可以有一或多個元件。</span><span class="sxs-lookup"><span data-stu-id="6d10c-112">The ISABOUT term can have one or more components.</span></span> <span data-ttu-id="6d10c-113">在 [CONTAINS](-search-sql-contains.md) 述詞中指定的資料行會針對每個元件進行測試。</span><span class="sxs-lookup"><span data-stu-id="6d10c-113">The columns specified in the [CONTAINS](-search-sql-contains.md) predicate are tested against each component.</span></span> <span data-ttu-id="6d10c-114">如果至少有一個元件相符，則檔會包含在結果中。</span><span class="sxs-lookup"><span data-stu-id="6d10c-114">The document is included in the results if at least one of the components matches.</span></span> <span data-ttu-id="6d10c-115">逗點分隔多個元件。</span><span class="sxs-lookup"><span data-stu-id="6d10c-115">Commas separate multiple components.</span></span>

<span data-ttu-id="6d10c-116">元件部分具有下列語法：</span><span class="sxs-lookup"><span data-stu-id="6d10c-116">The component part has the following syntax:</span></span>


```
<match_term> [<weight_term>]
```



<span data-ttu-id="6d10c-117">您可以使用選擇性權數詞彙來變更 ISABOUT 詞彙內每個詞彙的相對重要性。</span><span class="sxs-lookup"><span data-stu-id="6d10c-117">You can use the optional WEIGHT term to change the relative importance of each term within the ISABOUT term.</span></span> <span data-ttu-id="6d10c-118">如果未套用加權詞彙，則會隱含預設的1.0 權數。</span><span class="sxs-lookup"><span data-stu-id="6d10c-118">If no weight term is applied, the default 1.0 weight is implied.</span></span>

<span data-ttu-id="6d10c-119">下表描述可能的 match 詞彙類型。</span><span class="sxs-lookup"><span data-stu-id="6d10c-119">The following table describes possible match term types.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6d10c-120">類型</span><span class="sxs-lookup"><span data-stu-id="6d10c-120">Type</span></span></th>
<th><span data-ttu-id="6d10c-121">描述</span><span class="sxs-lookup"><span data-stu-id="6d10c-121">Description</span></span></th>
<th><span data-ttu-id="6d10c-122">範例</span><span class="sxs-lookup"><span data-stu-id="6d10c-122">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6d10c-123">Word</span><span class="sxs-lookup"><span data-stu-id="6d10c-123">Word</span></span></td>
<td><span data-ttu-id="6d10c-124">沒有空格或其他標點符號的單一單字。</span><span class="sxs-lookup"><span data-stu-id="6d10c-124">A single word without spaces or other punctuation.</span></span></td>
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
<td><span data-ttu-id="6d10c-125">片語</span><span class="sxs-lookup"><span data-stu-id="6d10c-125">Phrase</span></span></td>
<td><span data-ttu-id="6d10c-126">多個單字或包含空格。</span><span class="sxs-lookup"><span data-stu-id="6d10c-126">Multiple words or included spaces.</span></span></td>
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
<td><span data-ttu-id="6d10c-127">萬用字元</span><span class="sxs-lookup"><span data-stu-id="6d10c-127">Wildcard</span></span></td>
<td><span data-ttu-id="6d10c-128">在結尾加上星號 ( \* ) 的單字或片語。</span><span class="sxs-lookup"><span data-stu-id="6d10c-128">Words or phrases with the asterisk (\*) added to the end.</span></span> <span data-ttu-id="6d10c-129">如需詳細資訊，請參閱在 <a href="-search-sql-wildcards.md">CONTAINS 述詞中使用萬用字元</a>。</span><span class="sxs-lookup"><span data-stu-id="6d10c-129">For more information, see <a href="-search-sql-wildcards.md">Using Wildcards in the CONTAINS Predicate</a>.</span></span></td>
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



 

## <a name="isabout-column-weighting"></a><span data-ttu-id="6d10c-130">ISABOUT 資料行加權</span><span class="sxs-lookup"><span data-stu-id="6d10c-130">ISABOUT Column Weighting</span></span>

<span data-ttu-id="6d10c-131">ISABOUT 字詞會根據每份檔與查詢中的比對字片語相符的程度，來排列相符的檔。</span><span class="sxs-lookup"><span data-stu-id="6d10c-131">The ISABOUT term ranks matching documents based on how closely each document matches the set of match terms in the query.</span></span> <span data-ttu-id="6d10c-132">您可以使用資料行加權，以比其他比對字詞更具重要性。</span><span class="sxs-lookup"><span data-stu-id="6d10c-132">You can use column weighting to place more importance on matching some match terms than others.</span></span> <span data-ttu-id="6d10c-133">ISABOUT 詞彙中的每個相符詞彙都可以套用加權值。</span><span class="sxs-lookup"><span data-stu-id="6d10c-133">Each match term in the ISABOUT term can have a weight value applied.</span></span> <span data-ttu-id="6d10c-134">權數會套用至單一比對字詞，並以關鍵字「權數」表示。</span><span class="sxs-lookup"><span data-stu-id="6d10c-134">The weight is applied to a single match term and is indicated by the keyword "WEIGHT".</span></span> <span data-ttu-id="6d10c-135">權數詞彙有兩種替代語法：</span><span class="sxs-lookup"><span data-stu-id="6d10c-135">The WEIGHT term has two alternative syntaxes:</span></span>


```
<match_term> WEIGHT(<weight_value>)
<match_term>:(<weight_value>)
```



<span data-ttu-id="6d10c-136">權數值必須介於0到1.0 之間，且不能超過三位數。</span><span class="sxs-lookup"><span data-stu-id="6d10c-136">The weight value must be between 0 and 1.0, with no more than three decimal places.</span></span> <span data-ttu-id="6d10c-137">指定超出此範圍的加權值會產生錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="6d10c-137">Specifying a weight value outside this range results in an error message.</span></span> <span data-ttu-id="6d10c-138">詞彙的加權排名值會乘以詞彙的加權值。</span><span class="sxs-lookup"><span data-stu-id="6d10c-138">The unweighted ranking value for a term is multiplied by the weight value for the term.</span></span>

<span data-ttu-id="6d10c-139">如果未指定符合詞彙的權數，則會隱含預設值1.0。</span><span class="sxs-lookup"><span data-stu-id="6d10c-139">If no weight is specified for a match term, the default value, 1.0, is implied.</span></span>

### <a name="example"></a><span data-ttu-id="6d10c-140">範例</span><span class="sxs-lookup"><span data-stu-id="6d10c-140">Example</span></span>

<span data-ttu-id="6d10c-141">下列範例會針對加權值使用 long 和 short 語法，以將權數套用至兩個 ISABOUT 相符詞彙。</span><span class="sxs-lookup"><span data-stu-id="6d10c-141">The following example applies weights to the two ISABOUT match terms, using both the long and short syntax for weight values.</span></span>


```
WHERE CONTAINS( System.FileName,
      'ISABOUT("computer" WEIGHT (0.75),"software":0.25)')
```



## <a name="related-topics"></a><span data-ttu-id="6d10c-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="6d10c-142">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6d10c-143">**參考**</span><span class="sxs-lookup"><span data-stu-id="6d10c-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6d10c-144">FREETEXT 述詞</span><span class="sxs-lookup"><span data-stu-id="6d10c-144">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

[<span data-ttu-id="6d10c-145">WHERE 子句</span><span class="sxs-lookup"><span data-stu-id="6d10c-145">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 



