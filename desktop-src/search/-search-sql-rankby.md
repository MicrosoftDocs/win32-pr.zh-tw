---
description: 查詢的結果包含查詢所傳回的資料列，以及每個資料列的次序值（如果 SELECT 子句中包含 rank 資料行的話）。
ms.assetid: 8655eec4-5151-4f82-b485-4dbef947df0d
title: RANK BY 子句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5de7f7a63e33f43ba6387cbcea44a5f5b5ae8f99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191201"
---
# <a name="rank-by-clause"></a><span data-ttu-id="f9bcb-103">RANK BY 子句</span><span class="sxs-lookup"><span data-stu-id="f9bcb-103">RANK BY Clause</span></span>

<span data-ttu-id="f9bcb-104">查詢的結果包含查詢所傳回的資料列，以及每個資料列的次序值（如果 SELECT 子句中包含 rank 資料行的話）。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-104">The results from a query include both the rows returned by the query and a rank value for each row if the rank column is included in the SELECT clause.</span></span> <span data-ttu-id="f9bcb-105">排名值是由搜尋引擎計算，並傳回為0到1000範圍內的整數。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-105">The rank values are calculated by the Search engine and are returned as integers in the range zero to 1000.</span></span> <span data-ttu-id="f9bcb-106">為了讓排名結果更有意義，查詢可以控制如何在 RANK BY 子句中計算原始排名值。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-106">To make the rank results more meaningful, the query can control how raw rank values are calculated in the RANK BY clause.</span></span>

<span data-ttu-id="f9bcb-107">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="f9bcb-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="f9bcb-108">RANK BY 子句</span><span class="sxs-lookup"><span data-stu-id="f9bcb-108">RANK BY Clause</span></span>](#rank-by-clause)
-   [<span data-ttu-id="f9bcb-109">權數函數</span><span class="sxs-lookup"><span data-stu-id="f9bcb-109">WEIGHT Function</span></span>](#weight-function)
-   [<span data-ttu-id="f9bcb-110">強制函式</span><span class="sxs-lookup"><span data-stu-id="f9bcb-110">COERCION Function</span></span>](#coercion-function)

## <a name="rank-by-clause"></a><span data-ttu-id="f9bcb-111">RANK BY 子句</span><span class="sxs-lookup"><span data-stu-id="f9bcb-111">RANK BY Clause</span></span>

<span data-ttu-id="f9bcb-112">RANK BY 子句的語法如下所示：</span><span class="sxs-lookup"><span data-stu-id="f9bcb-112">The syntax for the RANK BY clause is as follows:</span></span>


```
WHERE ( <search_condition> ) 
RANK BY [ ( ] <rank_specification> [ ) ]
```



<span data-ttu-id="f9bcb-113">RANK BY 子句會套用至 \_ 緊接在其前面的搜尋條件，有效地為該搜尋條件所傳回的資料列指定較低或更高的排名，而不是另一個搜尋條件所傳回的資料列。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-113">The RANK BY clause is applied to the search\_condition immediately preceding it, effectively specifying a lower or higher rank for rows returned by that search condition than rows returned by another search condition.</span></span> <span data-ttu-id="f9bcb-114">搜尋條件周圍的括弧 \_ 是必要的。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-114">The parentheses surrounding the search\_condition are required.</span></span> <span data-ttu-id="f9bcb-115">排名規格周圍的括弧是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-115">The parentheses surrounding the rank specification are optional.</span></span>

<span data-ttu-id="f9bcb-116">單一條件可以套用一個以上的 RANK BY 子句。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-116">More than one RANK BY clause can be applied to a single condition.</span></span> <span data-ttu-id="f9bcb-117">您可以使用括弧將其他順位 BY 子句加入至另一個。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-117">You can include additional RANK BY clauses one after the other using parentheses.</span></span>

> [!Note]  
> <span data-ttu-id="f9bcb-118">全文檢索述詞會傳回範圍0到1000的排名值。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-118">Full-text predicates return rank values in the range 0 to 1000.</span></span> <span data-ttu-id="f9bcb-119">非全文檢索述詞所比對之所有檔的等級值為1000。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-119">Rank values for all documents matched by a non-full-text predicate are 1000.</span></span> <span data-ttu-id="f9bcb-120">對排名值的修改應將此資訊納入考慮。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-120">Modifications to the rank values should take this information into account.</span></span>

 

<span data-ttu-id="f9bcb-121">\_RANKBY 子句的排名規格部分會識別要套用至排名值的一或多個函數。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-121">The rank\_specification portion of the RANKBY clause identifies one or more functions to apply to the rank values.</span></span> <span data-ttu-id="f9bcb-122">權數函數會針對傳回的資料列，將乘數套用至原始排名值。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-122">The WEIGHT function applies a multiplier to the raw rank value for a returned row.</span></span> <span data-ttu-id="f9bcb-123">乘數越小，所產生的排名值就越低。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-123">The smaller the multiplier, the lower the resulting rank value.</span></span> <span data-ttu-id="f9bcb-124">強制函式可以用來將傳回的資料列相乘、加入或設定特定的等級值。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-124">The COERCION function can be used to multiply, add to, or set a specific rank value for a returned row.</span></span> <span data-ttu-id="f9bcb-125">每個排名規格都可以包含零個或一個加權函數，以及零或多個強制函式。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-125">Each rank specification can include either zero or one WEIGHT function and zero or more COERCION functions.</span></span> <span data-ttu-id="f9bcb-126">如果加權和強制函式都包含在 RANK BY 子句中，加權函數必須是 first。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-126">If both WEIGHT and COERCION functions are included in a RANK BY clause, the WEIGHT function must be first.</span></span>

## <a name="weight-function"></a><span data-ttu-id="f9bcb-127">權數函數</span><span class="sxs-lookup"><span data-stu-id="f9bcb-127">WEIGHT Function</span></span>

<span data-ttu-id="f9bcb-128">權數函數的語法為：</span><span class="sxs-lookup"><span data-stu-id="f9bcb-128">The syntax of the WEIGHT function is:</span></span>


```
WEIGHT ( <weight_multipler> ) 
```



<span data-ttu-id="f9bcb-129">乘數必須是從0.001 到1.000 的十進位數。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-129">The multiplier must be a decimal from 0.001 to 1.000.</span></span> <span data-ttu-id="f9bcb-130">搜尋條件述詞所傳回的原始排名值會乘以加權乘數來設定新的排名值。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-130">The raw rank value returned by the search condition predicate is multiplied by the weight multiplier to set a new rank value.</span></span>

<span data-ttu-id="f9bcb-131">在下列範例中，權數函數會在 System.Doc>ument 中提供 "Theresa" 一字的檔。LastAuthor 欄位在 [Author] 欄位中有 "Theresa" 的檔排名值一半：</span><span class="sxs-lookup"><span data-stu-id="f9bcb-131">In the following example, the WEIGHT function gives documents with the word "Theresa" in the System.Document.LastAuthor field half the rank value of documents with "Theresa" in the System.Author field:</span></span>


```
WHERE CONTAINS ( System.Author,'"Theresa"' ) 
         RANK BY WEIGHT ( 1.000 )
      OR
      CONTAINS ( System.Document.LastAuthor,'"Theresa"' ) 
         RANK BY WEIGHT ( 0.500 ) 
```



 

> [!Note]  
> <span data-ttu-id="f9bcb-132">CONTAINS 和 FREETEXT 述詞資料行加權功能支援使用在搜尋詞彙和乘數 ( "software"： 0.25) 之間的冒號格式的速記格式。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-132">The CONTAINS and FREETEXT predicate column weighting features support a shorthand format using a colon between the search term and the multiplier ("software":0.25).</span></span> <span data-ttu-id="f9bcb-133">RANK BY 子句不支援縮寫形式。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-133">The RANK BY clause does not support the shortened form.</span></span>

 

<span data-ttu-id="f9bcb-134">使用依權數的等級時有限制：它無法搭配使用布林值條件的 CONTAINS 子句使用;例如，不允許下列範例：</span><span class="sxs-lookup"><span data-stu-id="f9bcb-134">There is a limitation when using RANK BY WEIGHT: it does not work with CONTAINS clauses that use Boolean conditions; for example, the following example is not permitted:</span></span>


```
CONTAINS ( System.Author,'"Theresa" OR "Teresa"' ) RANK BY WEIGHT ( 0.400 )
```



## <a name="coercion-function"></a><span data-ttu-id="f9bcb-135">強制函式</span><span class="sxs-lookup"><span data-stu-id="f9bcb-135">COERCION Function</span></span>

<span data-ttu-id="f9bcb-136">Rank 強制函式可以用來變更傳回的等級值（藉由加法或乘法），或指派特定值給它。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-136">The rank coercion function can be used to change the returned rank value by addition or multiplication or by assigning it a specific value.</span></span>

<span data-ttu-id="f9bcb-137">強制函式的語法為：</span><span class="sxs-lookup"><span data-stu-id="f9bcb-137">The syntax of the COERCION function is:</span></span>


```
COERCION ( <coercion_operation> , <coercion_value> )
```



<span data-ttu-id="f9bcb-138">強制值是整數值。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-138">The coercion value is an integer value.</span></span>

<span data-ttu-id="f9bcb-139">下表描述可用的強制操作設定。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-139">The following table describes the available coercion operation settings.</span></span>



| <span data-ttu-id="f9bcb-140">強制操作</span><span class="sxs-lookup"><span data-stu-id="f9bcb-140">Coercion operation</span></span> | <span data-ttu-id="f9bcb-141">Description</span><span class="sxs-lookup"><span data-stu-id="f9bcb-141">Description</span></span>                                                                                    | <span data-ttu-id="f9bcb-142">數值範圍</span><span class="sxs-lookup"><span data-stu-id="f9bcb-142">Value range</span></span>  |
|--------------------|------------------------------------------------------------------------------------------------|--------------|
| <span data-ttu-id="f9bcb-143">ABSOLUTE</span><span class="sxs-lookup"><span data-stu-id="f9bcb-143">ABSOLUTE</span></span>           | <span data-ttu-id="f9bcb-144">傳回的排名值是在強制值中指定的值。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-144">The rank value returned is the value specified in the coercion value.</span></span>                          | <span data-ttu-id="f9bcb-145">0到1000</span><span class="sxs-lookup"><span data-stu-id="f9bcb-145">0 to 1000</span></span>    |
| <span data-ttu-id="f9bcb-146">ADD</span><span class="sxs-lookup"><span data-stu-id="f9bcb-146">ADD</span></span>                | <span data-ttu-id="f9bcb-147">傳回的排名值是原始排名值和指定強制值的總和。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-147">The rank value returned is the sum of the raw rank value and the specified coercion value.</span></span>     | <span data-ttu-id="f9bcb-148">0.001 至1。0</span><span class="sxs-lookup"><span data-stu-id="f9bcb-148">0.001 to 1.0</span></span> |
| <span data-ttu-id="f9bcb-149">MULTIPLY</span><span class="sxs-lookup"><span data-stu-id="f9bcb-149">MULTIPLY</span></span>           | <span data-ttu-id="f9bcb-150">傳回的排名值是原始排名值和指定強制值的乘積。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-150">The rank value returned is the product of the raw rank value and the specified coercion value.</span></span> | <span data-ttu-id="f9bcb-151">0.001 至1。0</span><span class="sxs-lookup"><span data-stu-id="f9bcb-151">0.001 to 1.0</span></span> |



 

 

> [!IMPORTANT]
> <span data-ttu-id="f9bcb-152">搜尋只能傳回0到1000範圍內的等級值。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-152">Search can return rank values only in the range of 0 to 1000.</span></span>

 

 

<span data-ttu-id="f9bcb-153">下列範例會使用強制函式，將標題中有 "computer" 的所有檔設定為1000的順位，同時減少標題中包含 "computer" 和 "software" 的檔排名一季。</span><span class="sxs-lookup"><span data-stu-id="f9bcb-153">The following example uses the COERCION function to set all documents with "computer" in the title to have a rank of 1000, while reducing by one-quarter the rank of documents containing both "computer" and "software" in the title.</span></span>


```
WHERE CONTAINS ( System.Title, 'computer' )
        RANK BY COERCION ( ABSOLUTE , 1000 )
        OR 
       CONTAINS ( System.Title, '"computer" AND "software"' )
        RANK BY COERCION ( MULTIPLY, 0.750 ) 
```



 

 



