---
description: 資料行群組別名提供一種方式，可讓您使用較短的名稱來取代資料行或資料行群組的名稱。 選擇性群組別名述詞是 WHERE 子句的一部分。
ms.assetid: 7782ac24-ea6c-4a97-b1b6-982f276fcefc
title: WITH--AS Group Alias 述詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29218e11fbffe5f47128eeefba3a7fe847a5b21d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689860"
---
# <a name="with----as-group-alias-predicate"></a><span data-ttu-id="479fc-104">WITH--AS Group Alias 述詞</span><span class="sxs-lookup"><span data-stu-id="479fc-104">WITH -- AS Group Alias Predicate</span></span>

<span data-ttu-id="479fc-105">資料行群組別名提供一種方式，可讓您使用較短的名稱來取代資料行或資料行群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="479fc-105">Column group aliases provide a way to use shorter names in place of the name of a column or a group of columns.</span></span> <span data-ttu-id="479fc-106">選擇性群組別名述詞是 WHERE 子句的一部分。</span><span class="sxs-lookup"><span data-stu-id="479fc-106">The optional group alias predicate is part of the WHERE clause.</span></span> <span data-ttu-id="479fc-107">其語法如下：</span><span class="sxs-lookup"><span data-stu-id="479fc-107">Its syntax follows:</span></span>


```
...WHERE[ WITH(<columns>) AS #<alias_name>]
[,WITH(<columns>) AS #<alias_name>]
```



<span data-ttu-id="479fc-108">您可以指定一個以上的群組別名，並以 .。。做為逗號的述詞。</span><span class="sxs-lookup"><span data-stu-id="479fc-108">You can specify more than one group alias, separating the WITH...AS predicates by commas.</span></span>

<span data-ttu-id="479fc-109">在 WHERE 子句述詞中參考群組別名時，此條件會套用至群組中的每個資料行。</span><span class="sxs-lookup"><span data-stu-id="479fc-109">When a group alias is referred to in a WHERE clause predicate, the condition is applied to each column in the group.</span></span> <span data-ttu-id="479fc-110">使用邏輯 **OR** 運算子結合每個資料行所產生的邏輯值。</span><span class="sxs-lookup"><span data-stu-id="479fc-110">The logical values resulting from matching each column are combined by using the logical **OR** operator.</span></span>

<span data-ttu-id="479fc-111">必須先定義別名，才能使用它，而且只能在 WHERE 子句中使用。</span><span class="sxs-lookup"><span data-stu-id="479fc-111">An alias must be defined before it can be used, and it can be used only within the WHERE clause.</span></span> <span data-ttu-id="479fc-112">別名名稱必須是一般識別碼，前面加上必要的井字型大小 (\#) 。</span><span class="sxs-lookup"><span data-stu-id="479fc-112">The alias name must be a regular identifier preceded by a required pound sign (\#).</span></span>

<span data-ttu-id="479fc-113">資料行規范可包含一或多個以逗號分隔的資料行指定名稱。</span><span class="sxs-lookup"><span data-stu-id="479fc-113">The column specifier can contain one or more column specifiers, separated by commas.</span></span> <span data-ttu-id="479fc-114">資料行清單必須以括弧括住，而且可以將加權指派給每個資料行。</span><span class="sxs-lookup"><span data-stu-id="479fc-114">The list of columns must be enclosed in parentheses and weighting can be assigned to each.</span></span> <span data-ttu-id="479fc-115">每個資料行都有下列語法：</span><span class="sxs-lookup"><span data-stu-id="479fc-115">Each column has the following syntax:</span></span>


```
<column_identifier> [<weight_assignment>]
```



<span data-ttu-id="479fc-116">如需指定資料行加權的詳細資訊，請參閱 [FREETEXT](-search-sql-freetext.md) 述詞和 [CONTAINS](-search-sql-contains.md)述詞。</span><span class="sxs-lookup"><span data-stu-id="479fc-116">For information on specifying column weights, see [FREETEXT Predicate](-search-sql-freetext.md) and [CONTAINS Predicate](-search-sql-contains.md).</span></span>

<span data-ttu-id="479fc-117">資料行識別碼可以是一般或分隔的。</span><span class="sxs-lookup"><span data-stu-id="479fc-117">The column identifier can be regular or delimited.</span></span>

## <a name="examples"></a><span data-ttu-id="479fc-118">範例</span><span class="sxs-lookup"><span data-stu-id="479fc-118">Examples</span></span>

<span data-ttu-id="479fc-119">下列 WHERE 子句範例會示範何時以及如何使用群組別名述詞。</span><span class="sxs-lookup"><span data-stu-id="479fc-119">The following WHERE clause examples demonstrate when and how you can use the group alias predicate.</span></span> <span data-ttu-id="479fc-120">第一個範例顯示更重複的 WHERE 子句，而不使用群組別名。</span><span class="sxs-lookup"><span data-stu-id="479fc-120">The first example shows a more repetitive WHERE clause that does not use group aliasing.</span></span>


```
...WHERE
    FREETEXT("System.ItemNameDisplay",'"computer software"')
    OR
    FREETEXT("System.Title",'"computer software"')
    OR 
    FREETEXT("System.Keywords",'"computer software"')
```



<span data-ttu-id="479fc-121">您可以使用群組別名來簡化上述範例，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="479fc-121">The preceding example can be simplified by using a group alias, as shown in the following example.</span></span>


```
...WHERE
    WITH("System.ItemNameDisplay","System.Title","System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



<span data-ttu-id="479fc-122">以下是正數加權的範例，其中 **Title** 屬性會在決定相對排名時獲得更多加權。</span><span class="sxs-lookup"><span data-stu-id="479fc-122">The following is an example of positive weighting where the **Title** property is given more weight in determining the relative rank.</span></span>


```
...WHERE
    WITH("System.Title":0.8,*:0.5,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



<span data-ttu-id="479fc-123">以下是負加權的範例，其中不會考慮權數為0的 **標題** 屬性。</span><span class="sxs-lookup"><span data-stu-id="479fc-123">The following is an example of negative weighting where the **Title** property with weight of 0 is not considered.</span></span>


```
...WHERE
    WITH("System.Title":0,*:1.0,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



## <a name="related-topics"></a><span data-ttu-id="479fc-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="479fc-124">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="479fc-125">**參考**</span><span class="sxs-lookup"><span data-stu-id="479fc-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="479fc-126">FREETEXT 述詞</span><span class="sxs-lookup"><span data-stu-id="479fc-126">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

<span data-ttu-id="479fc-127">**概念**</span><span class="sxs-lookup"><span data-stu-id="479fc-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="479fc-128">全文檢索述詞</span><span class="sxs-lookup"><span data-stu-id="479fc-128">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="479fc-129">非全文檢索述詞</span><span class="sxs-lookup"><span data-stu-id="479fc-129">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



