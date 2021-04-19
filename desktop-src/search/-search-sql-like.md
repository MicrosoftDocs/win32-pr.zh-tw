---
description: LIKE 述詞會針對指定的資料行執行模式比對比較。
ms.assetid: d4bcf406-1253-4e56-b770-79edd4a98205
title: LIKE 述詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba042fb2fe3005e062e7961a048a81a64c0c144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970144"
---
# <a name="like-predicate"></a><span data-ttu-id="a21a3-103">LIKE 述詞</span><span class="sxs-lookup"><span data-stu-id="a21a3-103">LIKE Predicate</span></span>

<span data-ttu-id="a21a3-104">LIKE 述詞會針對指定的資料行執行模式比對比較。</span><span class="sxs-lookup"><span data-stu-id="a21a3-104">The LIKE predicate performs pattern-matching comparison on the specified column.</span></span> <span data-ttu-id="a21a3-105">其使用下列語法：</span><span class="sxs-lookup"><span data-stu-id="a21a3-105">It uses the following syntax:</span></span>


```
...WHERE <column> LIKE '<wildcard_literal>'
```



<span data-ttu-id="a21a3-106"><column>可以是一般或分隔的[識別碼](-search-sql-identifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="a21a3-106">The <column> can be a regular or delimited [identifier](-search-sql-identifiers.md).</span></span> <span data-ttu-id="a21a3-107">此資料行受限於屬性存放區中的屬性。</span><span class="sxs-lookup"><span data-stu-id="a21a3-107">The column is limited to the properties in the property store.</span></span>

<span data-ttu-id="a21a3-108"><萬用字元 \_ 常值> 是字串常值。</span><span class="sxs-lookup"><span data-stu-id="a21a3-108">The <wildcard\_literal> is a string literal.</span></span> <span data-ttu-id="a21a3-109">它會以引號括住，並且可以選擇性地包含萬用字元。</span><span class="sxs-lookup"><span data-stu-id="a21a3-109">It is enclosed in quotation marks and optionally can contain wildcard characters.</span></span> <span data-ttu-id="a21a3-110">如有需要，相符字串可以包含多個萬用字元。</span><span class="sxs-lookup"><span data-stu-id="a21a3-110">The match string can contain multiple wildcard characters if needed.</span></span> <span data-ttu-id="a21a3-111">下表描述 LIKE 述詞可辨識的萬用字元。</span><span class="sxs-lookup"><span data-stu-id="a21a3-111">The following table describes the wildcard characters that the LIKE predicate recognizes.</span></span>



| <span data-ttu-id="a21a3-112">萬用字元</span><span class="sxs-lookup"><span data-stu-id="a21a3-112">Wildcard</span></span>                | <span data-ttu-id="a21a3-113">描述</span><span class="sxs-lookup"><span data-stu-id="a21a3-113">Description</span></span>                                                                                                                                                                                     | <span data-ttu-id="a21a3-114">範例</span><span class="sxs-lookup"><span data-stu-id="a21a3-114">Example</span></span>                                                                                                                                                                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a21a3-115">% (百分比) </span><span class="sxs-lookup"><span data-stu-id="a21a3-115">% (percent)</span></span>             | <span data-ttu-id="a21a3-116">符合零或多個字元。</span><span class="sxs-lookup"><span data-stu-id="a21a3-116">Matches zero or more of any characters.</span></span>                                                                                                                                                         | <span data-ttu-id="a21a3-117">' comp% r ' 符合 ' comp '，後面接著零或多個字元，以 r 結尾。</span><span class="sxs-lookup"><span data-stu-id="a21a3-117">'comp%r' matches 'comp' followed by zero or more of any characters, ending in an r.</span></span>                                                                                                                                  |
| <span data-ttu-id="a21a3-118">\_ (底線) </span><span class="sxs-lookup"><span data-stu-id="a21a3-118">\_ (underscore)</span></span>         | <span data-ttu-id="a21a3-119">符合任何單一字元。</span><span class="sxs-lookup"><span data-stu-id="a21a3-119">Matches any single character.</span></span>                                                                                                                                                                   | <span data-ttu-id="a21a3-120">' comp \_ 終端 ' 會比對 ' comp '，後面接著剛好一個字元，後面接著 ' 終端 '。</span><span class="sxs-lookup"><span data-stu-id="a21a3-120">'comp\_ter' matches 'comp' followed by exactly one of any character, followed by 'ter'.</span></span>                                                                                                                              |
| <span data-ttu-id="a21a3-121">\[\] (方括弧) </span><span class="sxs-lookup"><span data-stu-id="a21a3-121">\[ \] (square brackets)</span></span> | <span data-ttu-id="a21a3-122">符合指定範圍或集合內的任何單一字元。</span><span class="sxs-lookup"><span data-stu-id="a21a3-122">Matches any single character within the specified range or set.</span></span> <span data-ttu-id="a21a3-123">例如， \[ -z \] 指定範圍; \[aeiou \] 指定一組母音。</span><span class="sxs-lookup"><span data-stu-id="a21a3-123">For example, \[a-z\] specifies a range; \[aeiou\] specifies the set of vowels.</span></span>                                                  | <span data-ttu-id="a21a3-124">' comp \[ a-z \] re ' 會比對 ' comp '，後面接著範圍 a 至 z 的單一字元，後面接著是 '。</span><span class="sxs-lookup"><span data-stu-id="a21a3-124">'comp\[a-z\]re' matches 'comp' followed by a single character in the range of a through z, followed by 're'.</span></span> <span data-ttu-id="a21a3-125">' comp \[ ao \] ' 符合 ' comp '，後面接著一個必須是或 o 的單一字元。</span><span class="sxs-lookup"><span data-stu-id="a21a3-125">'comp\[ao\]' matches 'comp' followed by a single character that must be either an a or an o.</span></span><br/> |
| <span data-ttu-id="a21a3-126">\[^ \] (插入號) </span><span class="sxs-lookup"><span data-stu-id="a21a3-126">\[^ \] (caret)</span></span>          | <span data-ttu-id="a21a3-127">符合不在指定範圍或集合內的任何單一字元。</span><span class="sxs-lookup"><span data-stu-id="a21a3-127">Matches any single character that is not within the specified range or set.</span></span> <span data-ttu-id="a21a3-128">例如， \[ ^ a-z \] 會指定排除 a 到 z 的範圍; \[^ aeiou \] 指定排除母音的集合。</span><span class="sxs-lookup"><span data-stu-id="a21a3-128">For example, \[^a-z\] specifies a range that excludes a through z; \[^aeiou\] specifies a set that excludes vowels.</span></span> | <span data-ttu-id="a21a3-129">' comp \[ ^ u \] ' 符合 ' comp '，後面接著任何不是 u 的單一字元。</span><span class="sxs-lookup"><span data-stu-id="a21a3-129">'comp\[^u\]' matches 'comp' followed by any single character that is not a u.</span></span>                                                                                                                                        |



 

<span data-ttu-id="a21a3-130">如果您建立具有多個範圍的述詞，則範圍必須是順序。</span><span class="sxs-lookup"><span data-stu-id="a21a3-130">If you create predicates with multiple ranges, the ranges must be in order.</span></span>

> [!Note]  
> <span data-ttu-id="a21a3-131">若要比對萬用字元做為比對的常值字元，而不是萬用字元，請將字元放在方括弧內。</span><span class="sxs-lookup"><span data-stu-id="a21a3-131">To match the wildcard characters as literal characters for matching and not as wildcard characters, place the character inside square brackets.</span></span> <span data-ttu-id="a21a3-132">例如，若要與百分比符號相符，請使用 ' \[ % \] '</span><span class="sxs-lookup"><span data-stu-id="a21a3-132">For example, to match the percent sign, use '\[%\]'</span></span>

 

## <a name="examples"></a><span data-ttu-id="a21a3-133">範例</span><span class="sxs-lookup"><span data-stu-id="a21a3-133">Examples</span></span>


```
...WHERE System.ItemNameDisplay LIKE 'financ%'
```



## <a name="related-topics"></a><span data-ttu-id="a21a3-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="a21a3-134">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a21a3-135">**參考**</span><span class="sxs-lookup"><span data-stu-id="a21a3-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a21a3-136">常值比較</span><span class="sxs-lookup"><span data-stu-id="a21a3-136">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="a21a3-137">多重值 (陣列) 比較</span><span class="sxs-lookup"><span data-stu-id="a21a3-137">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

[<span data-ttu-id="a21a3-138">Null 述詞</span><span class="sxs-lookup"><span data-stu-id="a21a3-138">NULL Predicate</span></span>](-search-sql-null.md)
</dt> <dt>

<span data-ttu-id="a21a3-139">**概念**</span><span class="sxs-lookup"><span data-stu-id="a21a3-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a21a3-140">全文檢索述詞</span><span class="sxs-lookup"><span data-stu-id="a21a3-140">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="a21a3-141">非全文檢索述詞</span><span class="sxs-lookup"><span data-stu-id="a21a3-141">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 




