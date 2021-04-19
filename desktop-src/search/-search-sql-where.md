---
description: 判斷檔是否包含在查詢所傳回之結果中的條件是由 WHERE 子句所指定。
ms.assetid: e3b5ee92-e817-49b8-aa8b-5d68254bb819
title: 'WHERE 子句 (Windows Search) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45a37334d656b0a321abdcdd4a5d045eb9d4985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001661"
---
# <a name="where-clause-windows-search"></a><span data-ttu-id="810cb-103">WHERE 子句 (Windows Search) </span><span class="sxs-lookup"><span data-stu-id="810cb-103">WHERE Clause (Windows Search)</span></span>

<span data-ttu-id="810cb-104">判斷檔是否包含在查詢所傳回之結果中的條件是由 WHERE 子句所指定。</span><span class="sxs-lookup"><span data-stu-id="810cb-104">The conditions that determine whether a document is included in the results returned by the query are specified by the WHERE clause.</span></span> <span data-ttu-id="810cb-105">在最高層級，WHERE 子句語法有兩個部分：</span><span class="sxs-lookup"><span data-stu-id="810cb-105">At the highest level, there are two parts to the WHERE clause syntax:</span></span>


```
...WHERE [<group_aliases>] <search_condition>
...WHERE ReuseWhere(<WHEREID>)
```



<span data-ttu-id="810cb-106">選擇性的 <群組 \_ 別名> 部分子句會將別名指派給一或多個資料行的群組，以簡化複雜的查詢。</span><span class="sxs-lookup"><span data-stu-id="810cb-106">The optional <group\_alias> portion of the clause simplifies complex queries by assigning an alias to a group of one or more columns.</span></span> <span data-ttu-id="810cb-107">這可以改善在 Url 指定的多個資料行中搜尋相同資訊的複雜查詢可讀性。</span><span class="sxs-lookup"><span data-stu-id="810cb-107">This can improve the readability of complex queries that search for the same information across multiple columns specified by URLs.</span></span> <span data-ttu-id="810cb-108">如需群組別名的詳細資訊，請參閱 [WITH--AS Group Alias 述](-search-sql-with-as.md)詞。</span><span class="sxs-lookup"><span data-stu-id="810cb-108">For more information about group aliases, see [WITH -- AS Group Alias Predicate](-search-sql-with-as.md).</span></span>

<span data-ttu-id="810cb-109"><search condition>WHERE 子句的部分是一或多個搜尋述詞，可指定搜尋的相符準則。</span><span class="sxs-lookup"><span data-stu-id="810cb-109">The <search condition> portion of the WHERE clause is one or more search predicates that specify matching criteria for the search.</span></span> <span data-ttu-id="810cb-110">搜尋述詞是判斷某個值某些事實的運算式。</span><span class="sxs-lookup"><span data-stu-id="810cb-110">Search predicates are expressions that assert some fact about some value.</span></span>

<span data-ttu-id="810cb-111">搜尋條件的結果為布林值，如果檔符合指定的搜尋條件， **則為 TRUE** ; 如果不符合指定的搜尋條件，則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="810cb-111">The result of a search condition is a Boolean value, either **TRUE** if the document meets the specified search conditions, or **FALSE** if it does not.</span></span> <span data-ttu-id="810cb-112">如果結果為 **TRUE**，則會傳回檔。</span><span class="sxs-lookup"><span data-stu-id="810cb-112">If the result is **TRUE**, the document is returned.</span></span> <span data-ttu-id="810cb-113">如果結果為 **FALSE**，則不會傳回檔。</span><span class="sxs-lookup"><span data-stu-id="810cb-113">If the result is **FALSE**, the document is not returned.</span></span> <span data-ttu-id="810cb-114">Microsoft Windows Search 查詢中所傳回的檔，會根據符合搜尋條件的程度，指派等級值。</span><span class="sxs-lookup"><span data-stu-id="810cb-114">Documents returned in a Microsoft Windows Search query are assigned rank values according to how well they match the search conditions.</span></span> <span data-ttu-id="810cb-115">每個查詢搜尋條件都可以包含 [RANKBY](-search-sql-rankby.md) 子句，以支援修改傳回的排名值。</span><span class="sxs-lookup"><span data-stu-id="810cb-115">Each of the query search conditions can include a [RANKBY](-search-sql-rankby.md) clause that supports modifying the returned rank values.</span></span>

<span data-ttu-id="810cb-116">[ReuseWhere](-search-sql-reusewhere.md)函式會讓多個使用相同搜尋條件的查詢更有效率。</span><span class="sxs-lookup"><span data-stu-id="810cb-116">The [ReuseWhere function](-search-sql-reusewhere.md) makes multiple queries that use the some of the same search conditions more efficient.</span></span> <span data-ttu-id="810cb-117">查詢中的 WHERE 子句會指定在查詢中相符的專案集合。</span><span class="sxs-lookup"><span data-stu-id="810cb-117">The WHERE clause in a query specifies the set of items that match in a query.</span></span> <span data-ttu-id="810cb-118">後續的查詢可以在新的查詢 WHERE 子句中使用 ReuseWhere 函數，以共用針對先前 evalution 執行的工作。</span><span class="sxs-lookup"><span data-stu-id="810cb-118">Subsequent queries can share the work performed for the previous evalution by using the ReuseWhere function in the new query WHERE clause.</span></span>

## <a name="search-predicates"></a><span data-ttu-id="810cb-119">搜尋述詞</span><span class="sxs-lookup"><span data-stu-id="810cb-119">Search Predicates</span></span>

<span data-ttu-id="810cb-120">搜尋條件是由一或多個述詞或搜尋條件所組成，可描述使用者搜尋的內容 (例如，DateCreated > ' 2006-04-19 ' ) 。</span><span class="sxs-lookup"><span data-stu-id="810cb-120">A search condition consists of one or more predicates or search conditions that describe what the user is searching for (for example, WHERE System.DateCreated >'2006-04-19').</span></span> <span data-ttu-id="810cb-121">您可以使用邏輯運算子 **AND**、 **or** 或 **NOT** 來合併搜尋述詞。</span><span class="sxs-lookup"><span data-stu-id="810cb-121">Search predicates can be combined using the logical operators **AND**, **OR**, or **NOT**.</span></span> <span data-ttu-id="810cb-122">選擇性的一元運算子 **不** 可以搭配 **和** 使用，而且只能用來否定述詞或搜尋條件的邏輯值。</span><span class="sxs-lookup"><span data-stu-id="810cb-122">The optional unary operator **NOT** can be used only with **AND** and only to negate the logical value of a predicate or search condition.</span></span> <span data-ttu-id="810cb-123">您可以使用括弧來分組及嵌套邏輯詞彙。</span><span class="sxs-lookup"><span data-stu-id="810cb-123">You can use parentheses to group and nest logical terms.</span></span>

<span data-ttu-id="810cb-124">下表顯示邏輯運算子的優先順序順序。</span><span class="sxs-lookup"><span data-stu-id="810cb-124">The following table shows the order of precedence for the logical operators.</span></span>



| <span data-ttu-id="810cb-125">順序 (優先順序) </span><span class="sxs-lookup"><span data-stu-id="810cb-125">Order (precedence)</span></span> | <span data-ttu-id="810cb-126">邏輯運算子</span><span class="sxs-lookup"><span data-stu-id="810cb-126">Logical operator</span></span> |
|--------------------|------------------|
| <span data-ttu-id="810cb-127">第一個 (最高) </span><span class="sxs-lookup"><span data-stu-id="810cb-127">First (highest)</span></span>    | <span data-ttu-id="810cb-128">**NOT**</span><span class="sxs-lookup"><span data-stu-id="810cb-128">**NOT**</span></span>          |
| <span data-ttu-id="810cb-129">Second</span><span class="sxs-lookup"><span data-stu-id="810cb-129">Second</span></span>             | <span data-ttu-id="810cb-130">**AND**</span><span class="sxs-lookup"><span data-stu-id="810cb-130">**AND**</span></span>          |
| <span data-ttu-id="810cb-131">第三 (最低) </span><span class="sxs-lookup"><span data-stu-id="810cb-131">Third (lowest)</span></span>     | <span data-ttu-id="810cb-132">**OR**</span><span class="sxs-lookup"><span data-stu-id="810cb-132">**OR**</span></span>           |



 

<span data-ttu-id="810cb-133">相同類型的邏輯運算子是關聯性，而且沒有指定的計算順序。</span><span class="sxs-lookup"><span data-stu-id="810cb-133">Logical operators of the same type are associative, and there is no specified calculation order.</span></span> <span data-ttu-id="810cb-134">例如， (A **和** B) **，而且** (C **和** d) 可以計算 (A **和** d) **，** (B **和** C) ，但邏輯結果不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="810cb-134">For example, (A **AND** B) **AND** (C **AND** D) can be calculated (A **AND** D) **AND** (B **AND** C) with no change in the logical result.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="810cb-135">不正確：其中 **不** 包含 ( ' computer ' ) </span><span class="sxs-lookup"><span data-stu-id="810cb-135">Incorrect: WHERE **NOT** CONTAINS ('computer')</span></span>
>
> <span data-ttu-id="810cb-136">正確：其中包含 ( ' software ' ) **且不** 包含 ( ' computer ' ) </span><span class="sxs-lookup"><span data-stu-id="810cb-136">Correct: WHERE CONTAINS ('software') **AND NOT** CONTAINS ('computer')</span></span>

 

<span data-ttu-id="810cb-137">在複雜的查詢中，您可能會想要特別強調某些資料行中比其他資料行的相符專案。</span><span class="sxs-lookup"><span data-stu-id="810cb-137">In complex queries, you might want to place more emphasis on matches in some columns than in others.</span></span> <span data-ttu-id="810cb-138">例如，在搜尋討論「軟體設計」的檔時，尋找檔標題中的搜尋詞彙比在檔的文字中尋找個別單字更可能是很好的相符專案。</span><span class="sxs-lookup"><span data-stu-id="810cb-138">For example, when searching for documents that discuss "software design", finding the search term in the document title is more likely to be a good match than finding the individual words in the text of the document.</span></span> <span data-ttu-id="810cb-139">若要以這種方式影響檔的排名，Microsoft Windows Search 查詢語言支援搜尋條件的加權。</span><span class="sxs-lookup"><span data-stu-id="810cb-139">To influence the ranking of documents in this manner, the Microsoft Windows Search query language supports weighting the search conditions.</span></span> <span data-ttu-id="810cb-140">如需資料行加權的詳細資訊，請參閱 [CONTAINS](-search-sql-contains.md) 述詞和 [FREETEXT](-search-sql-freetext.md)述詞。</span><span class="sxs-lookup"><span data-stu-id="810cb-140">For more information about column weighting, see [CONTAINS Predicate](-search-sql-contains.md) and [FREETEXT Predicate](-search-sql-freetext.md).</span></span>

<span data-ttu-id="810cb-141">Windows Search 中有三個搜尋述詞群組：全文檢索、非全文檢索和資料夾深度搜尋。</span><span class="sxs-lookup"><span data-stu-id="810cb-141">There are three groups of search predicates in Windows Search: full-text, non-full-text, and folder depth searches.</span></span> <span data-ttu-id="810cb-142">全文檢索搜尋述詞通常符合內容、標題和其他資料行的意義，並支援語言比對 (例如，替代字組表單、片語和鄰近搜尋) 。</span><span class="sxs-lookup"><span data-stu-id="810cb-142">Full-text search predicates typically match the meaning of the content, title, and other columns, and support linguistic matching (for example, alternative word forms, phrases, and proximity searching).</span></span> <span data-ttu-id="810cb-143">相反地，非全文檢索搜尋述詞會比對指定資料行的值，但不包含任何特殊的語言處理，但在許多情況下，會提供以字元為基礎的模式比對。</span><span class="sxs-lookup"><span data-stu-id="810cb-143">In contrast, non-full-text search predicates match the value of the specified columns and do not include any special linguistic processing, but in several cases offer character-based pattern matching.</span></span> <span data-ttu-id="810cb-144">資料夾深度述詞會將搜尋範圍限制為指定的路徑。</span><span class="sxs-lookup"><span data-stu-id="810cb-144">Folder depth predicates restrict the search scope to a specified path.</span></span>

> [!Note]  
> <span data-ttu-id="810cb-145">如果查詢傳回檔，因為該檔的非全文檢索述詞評估為 **TRUE** ，則 rank 值會計算為1000。</span><span class="sxs-lookup"><span data-stu-id="810cb-145">If the query returns a document because a non-full-text predicate evaluates to **TRUE** for that document, the rank value is calculated as 1000.</span></span> <span data-ttu-id="810cb-146">使用 [rank 強制函數](-search-sql-rankby.md) 可以修改 rank 值。</span><span class="sxs-lookup"><span data-stu-id="810cb-146">Using the [rank coercion function](-search-sql-rankby.md) can modify the rank value.</span></span>

 

<span data-ttu-id="810cb-147">下表說明全文檢索、非全文檢索和資料夾深度搜尋述詞。</span><span class="sxs-lookup"><span data-stu-id="810cb-147">The following tables describe the full-text, non-full-text, and folder depth search predicates.</span></span>



| <span data-ttu-id="810cb-148">全文檢索述詞</span><span class="sxs-lookup"><span data-stu-id="810cb-148">Full-text predicate</span></span>                  | <span data-ttu-id="810cb-149">描述</span><span class="sxs-lookup"><span data-stu-id="810cb-149">Description</span></span>                                                                                                                                                                                                                                                      |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="810cb-150">CONTAINS</span><span class="sxs-lookup"><span data-stu-id="810cb-150">CONTAINS</span></span>](-search-sql-contains.md) | <span data-ttu-id="810cb-151">支援檔文字資料行中詞彙的複雜搜尋 (例如，標題、內容) 。</span><span class="sxs-lookup"><span data-stu-id="810cb-151">Supports complex searches for terms in document text columns (for example, title, contents).</span></span> <span data-ttu-id="810cb-152">可以搜尋搜尋詞彙的屈折變化形式、測試字詞的相近度，以及執行邏輯比較。</span><span class="sxs-lookup"><span data-stu-id="810cb-152">Can search for inflected forms of the search terms, test for proximity of the terms, and perform logical comparisons.</span></span> <span data-ttu-id="810cb-153">搜尋詞彙可以包含萬用字元。</span><span class="sxs-lookup"><span data-stu-id="810cb-153">Search terms can include wildcard characters.</span></span> |
| [<span data-ttu-id="810cb-154">FREETEXT</span><span class="sxs-lookup"><span data-stu-id="810cb-154">FREETEXT</span></span>](-search-sql-freetext.md) | <span data-ttu-id="810cb-155">搜尋符合搜尋片語意義的檔。</span><span class="sxs-lookup"><span data-stu-id="810cb-155">Searches for documents that match the meaning of the search phrase.</span></span> <span data-ttu-id="810cb-156">相關的單字和類似的片語會相符，並根據檔與搜尋片語的緊密程度計算出排名資料行。</span><span class="sxs-lookup"><span data-stu-id="810cb-156">Related words and similar phrases will match, with the rank column calculated based on how closely the document matches the search phrase.</span></span> <span data-ttu-id="810cb-157">搜尋字詞不能包含萬用字元。</span><span class="sxs-lookup"><span data-stu-id="810cb-157">Search terms cannot include wildcard characters.</span></span>  |



 



| <span data-ttu-id="810cb-158">非全文檢索述詞</span><span class="sxs-lookup"><span data-stu-id="810cb-158">Non-full-text predicate</span></span>                                                    | <span data-ttu-id="810cb-159">Description</span><span class="sxs-lookup"><span data-stu-id="810cb-159">Description</span></span>                                                                                                                                                                           |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="810cb-160">LIKE</span><span class="sxs-lookup"><span data-stu-id="810cb-160">LIKE</span></span>](-search-sql-like.md)                                               | <span data-ttu-id="810cb-161">資料行值會使用簡單的模式比對與萬用字元進行比較。</span><span class="sxs-lookup"><span data-stu-id="810cb-161">Column values are compared using simple pattern matching with wildcard characters.</span></span>                                                                                                    |
| [<span data-ttu-id="810cb-162">常值比較</span><span class="sxs-lookup"><span data-stu-id="810cb-162">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)         | <span data-ttu-id="810cb-163">資料行值會與字串、日期、時間戳記、數值和其他常值進行比較。</span><span class="sxs-lookup"><span data-stu-id="810cb-163">Column values are compared against string, date, time stamp, numeric, and other literal values.</span></span> <span data-ttu-id="810cb-164">這個述詞支援相等和到差異，例如大於和小於。</span><span class="sxs-lookup"><span data-stu-id="810cb-164">This predicate supports equality and inequalities such as greater than and less than.</span></span> |
| [<span data-ttu-id="810cb-165">多重值 (陣列) 比較</span><span class="sxs-lookup"><span data-stu-id="810cb-165">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md) | <span data-ttu-id="810cb-166">多值資料行會與常值陣列的常值進行比較。</span><span class="sxs-lookup"><span data-stu-id="810cb-166">Multivalued columns are compared against a multivalued array of literals.</span></span>                                                                                                             |
| [<span data-ttu-id="810cb-167">NULL</span><span class="sxs-lookup"><span data-stu-id="810cb-167">NULL</span></span>](-search-sql-null.md)                                               | <span data-ttu-id="810cb-168">您可以使用 **Null** 述詞來偵測為檔定義的資料行值。</span><span class="sxs-lookup"><span data-stu-id="810cb-168">Column values that are undefined for the document can be detected by using the **NULL** predicate.</span></span>                                                                                    |



 



| <span data-ttu-id="810cb-169">資料夾深度</span><span class="sxs-lookup"><span data-stu-id="810cb-169">Folder Depth</span></span>                             | <span data-ttu-id="810cb-170">Description</span><span class="sxs-lookup"><span data-stu-id="810cb-170">Description</span></span>                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="810cb-171">範圍</span><span class="sxs-lookup"><span data-stu-id="810cb-171">SCOPE</span></span>](-search-sql-folderdepth.md)     | <span data-ttu-id="810cb-172">執行指定路徑的深度遍歷，包括特定資料夾和所有子資料夾。</span><span class="sxs-lookup"><span data-stu-id="810cb-172">Performs a deep traversal of the specified path, including the specific folder and all subfolders.</span></span> |
| [<span data-ttu-id="810cb-173">目錄</span><span class="sxs-lookup"><span data-stu-id="810cb-173">DIRECTORY</span></span>](-search-sql-folderdepth.md) | <span data-ttu-id="810cb-174">執行指定路徑的淺層遍歷，只搜尋特定資料夾。</span><span class="sxs-lookup"><span data-stu-id="810cb-174">Performs a shallow traversal of the specified path, searching only the specific folder.</span></span>            |



 

## <a name="examples"></a><span data-ttu-id="810cb-175">範例</span><span class="sxs-lookup"><span data-stu-id="810cb-175">Examples</span></span>

<span data-ttu-id="810cb-176">如需 WHERE 子句的範例，請參閱上表中連結的個別述詞主題。</span><span class="sxs-lookup"><span data-stu-id="810cb-176">For examples of the WHERE clause, see the individual predicate topics linked in the preceding table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="810cb-177">相關主題</span><span class="sxs-lookup"><span data-stu-id="810cb-177">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="810cb-178">**參考**</span><span class="sxs-lookup"><span data-stu-id="810cb-178">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="810cb-179">ReuseWhere 函式</span><span class="sxs-lookup"><span data-stu-id="810cb-179">ReuseWhere function</span></span>](-search-sql-reusewhere.md)
</dt> <dt>

[<span data-ttu-id="810cb-180">資料列集屬性</span><span class="sxs-lookup"><span data-stu-id="810cb-180">Rowset Properties</span></span>](-search-sql-rowset-properties.md)
</dt> <dt>

[<span data-ttu-id="810cb-181">FROM 子句</span><span class="sxs-lookup"><span data-stu-id="810cb-181">FROM Clause</span></span>](-search-sql-from.md)
</dt> <dt>

[<span data-ttu-id="810cb-182">搜尋 SQL 語法總覽</span><span class="sxs-lookup"><span data-stu-id="810cb-182">Overview of the Search SQL Syntax</span></span>](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[<span data-ttu-id="810cb-183">WITH--AS Group Alias 述詞</span><span class="sxs-lookup"><span data-stu-id="810cb-183">WITH -- AS Group Alias Predicate</span></span>](-search-sql-with-as.md)
</dt> <dt>

[<span data-ttu-id="810cb-184">範圍和目錄述詞</span><span class="sxs-lookup"><span data-stu-id="810cb-184">SCOPE and DIRECTORY Predicates</span></span>](-search-sql-folderdepth.md)
</dt> <dt>

[<span data-ttu-id="810cb-185">RANK BY 子句</span><span class="sxs-lookup"><span data-stu-id="810cb-185">RANK BY Clause</span></span>](-search-sql-rankby.md)
</dt> <dt>

<span data-ttu-id="810cb-186">**概念**</span><span class="sxs-lookup"><span data-stu-id="810cb-186">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="810cb-187">全文檢索述詞</span><span class="sxs-lookup"><span data-stu-id="810cb-187">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="810cb-188">非全文檢索述詞</span><span class="sxs-lookup"><span data-stu-id="810cb-188">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



