---
description: FREETEXT 述詞是 WHERE 子句的一部分，而且支援在文字資料行中搜尋單字和片語。
ms.assetid: 8afc95d1-25cd-4448-8bee-d132c2da22b3
title: FREETEXT 述詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc78be4d5ac75f892c82c6dad390e4583876856f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689871"
---
# <a name="freetext-predicate"></a><span data-ttu-id="4e96a-103">FREETEXT 述詞</span><span class="sxs-lookup"><span data-stu-id="4e96a-103">FREETEXT Predicate</span></span>

<span data-ttu-id="4e96a-104">FREETEXT 述詞是 [WHERE](-search-sql-where.md) 子句的一部分，而且支援在文字資料行中搜尋單字和片語。</span><span class="sxs-lookup"><span data-stu-id="4e96a-104">The FREETEXT predicate is part of the [WHERE](-search-sql-where.md) clause and supports searching for words and phrases in text columns.</span></span> <span data-ttu-id="4e96a-105">使用 FREETEXT 述詞來尋找檔，其中包含在指定的內容或資料行中散佈之搜尋文字的組合。</span><span class="sxs-lookup"><span data-stu-id="4e96a-105">Use the FREETEXT predicate to find documents containing combinations of the search words spread throughout the content or columns specified.</span></span> <span data-ttu-id="4e96a-106">若要取得等級值，請將相關的排名視為 SELECT 語句中的資料行。</span><span class="sxs-lookup"><span data-stu-id="4e96a-106">To get the rank value, include System.Search.Rank, which is a ranking of relevence, as a column in the SELECT statment.</span></span>

<span data-ttu-id="4e96a-107">FREETEXT 述詞具有下列語法：</span><span class="sxs-lookup"><span data-stu-id="4e96a-107">The FREETEXT predicate has the following syntax:</span></span>


```
FREETEXT
(["<fulltext_column>",]'<freetext_condition>'[,<LCID>])...
```



<span data-ttu-id="4e96a-108">全文檢索資料行參考是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="4e96a-108">The fulltext column reference is optional.</span></span> <span data-ttu-id="4e96a-109">您可以使用它來指定單一資料行，或針對 FREETEXT 述詞進行測試的資料 [行群組別名](-search-sql-with-as.md) 。</span><span class="sxs-lookup"><span data-stu-id="4e96a-109">With it, you can specify a single column, or a [column grouping alias](-search-sql-with-as.md) against which the FREETEXT predicate is tested.</span></span> <span data-ttu-id="4e96a-110">當全文檢索資料行指定為 "ALL" 或 " \* " 時，就會搜尋所有已編制索引的 text 屬性。</span><span class="sxs-lookup"><span data-stu-id="4e96a-110">When the fulltext column is specified as "ALL" or "\*", all indexed text properties are searched.</span></span> <span data-ttu-id="4e96a-111">雖然資料行不需要是文字屬性，但如果資料行是其他資料類型，則結果可能沒有意義。</span><span class="sxs-lookup"><span data-stu-id="4e96a-111">Although the column is not required to be a text property, the results might be meaningless if the column is some other data type.</span></span> <span data-ttu-id="4e96a-112">資料行名稱可以是一般或分隔的 [識別碼](-search-sql-identifiers.md)，而且您必須將它與條件分隔（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="4e96a-112">The column name can be either a regular or delimited [identifier](-search-sql-identifiers.md), and you must separate it from the condition by a comma.</span></span> <span data-ttu-id="4e96a-113">如果未提供任何全文檢索條件，則會使用 [內容] 資料行，也就是檔的主體。</span><span class="sxs-lookup"><span data-stu-id="4e96a-113">If no fulltext condition is supplied, the Contents column, which is the body of the document, is used.</span></span>

<span data-ttu-id="4e96a-114">您可以指定搜尋地區設定，以識別搜尋查詢的適當斷詞工具和字形變化表單。</span><span class="sxs-lookup"><span data-stu-id="4e96a-114">You can specify a search locale to identify the appropriate word breaker and inflectional forms for the search query.</span></span> <span data-ttu-id="4e96a-115">有效的地區設定值是 (LCID) 的 Windows standard 語言代碼識別碼。</span><span class="sxs-lookup"><span data-stu-id="4e96a-115">Valid locale values are a Windows standard language code identifier (LCID).</span></span> <span data-ttu-id="4e96a-116">例如，1033是美國的 LCID （英文）。</span><span class="sxs-lookup"><span data-stu-id="4e96a-116">For example, 1033 is the LCID for United States-English.</span></span> <span data-ttu-id="4e96a-117">將 LCID 放在 FREETEXT 子句括弧內的最後一個專案。</span><span class="sxs-lookup"><span data-stu-id="4e96a-117">Place the LCID as the last item inside the parentheses of the FREETEXT clause.</span></span> <span data-ttu-id="4e96a-118">如需搜尋和語言的重要資訊，請參閱 [使用當地語系化的搜尋](-search-sql-usinglocsearches.md)。</span><span class="sxs-lookup"><span data-stu-id="4e96a-118">For important information about searching and languages, see [Using Localized Searches](-search-sql-usinglocsearches.md).</span></span>

> [!Note]  
> <span data-ttu-id="4e96a-119">預設搜尋地區設定是系統預設的地區設定。</span><span class="sxs-lookup"><span data-stu-id="4e96a-119">The default search locale is the system default locale.</span></span>

 

<span data-ttu-id="4e96a-120">您必須將 freetext 條件部分以單引號括住，而且必須由一或多個搜尋詞彙組成。</span><span class="sxs-lookup"><span data-stu-id="4e96a-120">You must enclose the freetext condition portion in single quotation marks, and it must consist of one or more search terms.</span></span> <span data-ttu-id="4e96a-121">FREETEXT 述詞不支援邏輯運算。</span><span class="sxs-lookup"><span data-stu-id="4e96a-121">The FREETEXT predicate does not support logical operations.</span></span> <span data-ttu-id="4e96a-122">若要搜尋片語，就像是單一單字一樣，請用雙引號括住該片語。</span><span class="sxs-lookup"><span data-stu-id="4e96a-122">To search for a phrase as if it were a single word, enclose the phrase in double quotation marks.</span></span>

<span data-ttu-id="4e96a-123">當您使用 FREETEXT 述詞時，搜尋查詢結果會傳回包含所有搜尋字詞的檔。</span><span class="sxs-lookup"><span data-stu-id="4e96a-123">When you use the FREETEXT predicate, the search query results return documents containing all of the search terms.</span></span> <span data-ttu-id="4e96a-124">這些條款不需要以任何特定順序顯示。</span><span class="sxs-lookup"><span data-stu-id="4e96a-124">The terms do not need to appear in any particular order.</span></span> <span data-ttu-id="4e96a-125">包含更多搜尋詞彙的檔具有較高等級的資料行值。</span><span class="sxs-lookup"><span data-stu-id="4e96a-125">Documents that contain more of the search terms have higher rank column values.</span></span>

## <a name="examples"></a><span data-ttu-id="4e96a-126">範例</span><span class="sxs-lookup"><span data-stu-id="4e96a-126">Examples</span></span>

<span data-ttu-id="4e96a-127">下列範例會搜尋包含「電腦」、「軟體」、「硬體」或這些字組組合的檔：</span><span class="sxs-lookup"><span data-stu-id="4e96a-127">The following example searches for documents containing "computer", "software", "hardware", or combinations of those words:</span></span>


```
WHERE FREETEXT('computer software hardware')
```



> [!Note]  
> <span data-ttu-id="4e96a-128">您無法在相同的 FREETEXT 述詞中同時使用單字相符和片語比對。</span><span class="sxs-lookup"><span data-stu-id="4e96a-128">You cannot use both single-word matching and phrase matching in the same FREETEXT predicate.</span></span>

 

<span data-ttu-id="4e96a-129">使用縮寫執行查詢時，您必須在使用 FREETEXT 時，在縮減中將引號換用，但在使用 CONTAINS 時則否。</span><span class="sxs-lookup"><span data-stu-id="4e96a-129">When performing queries with contractions, you must escape the quotation mark in the contraction when using FREETEXT, but not when using CONTAINS.</span></span>

<span data-ttu-id="4e96a-130">例如，下列語法會失敗：</span><span class="sxs-lookup"><span data-stu-id="4e96a-130">For example, the following syntax fails:</span></span>


```
WHERE FREETEXT(*,'"We'll meet next week"')
```



<span data-ttu-id="4e96a-131">正確的語法包括兩個單引號，而不是雙引號。</span><span class="sxs-lookup"><span data-stu-id="4e96a-131">The correct syntax includes two single quotation marks, not a double quotation mark.</span></span>

<span data-ttu-id="4e96a-132">下列語法會成功：</span><span class="sxs-lookup"><span data-stu-id="4e96a-132">The following syntax succeeds:</span></span>


```
WHERE FREETEXT(*,'"We''ll meet next week"')
```



## <a name="related-topics"></a><span data-ttu-id="4e96a-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="4e96a-133">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4e96a-134">**參考**</span><span class="sxs-lookup"><span data-stu-id="4e96a-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4e96a-135">CONTAINS 述詞</span><span class="sxs-lookup"><span data-stu-id="4e96a-135">CONTAINS Predicate</span></span>](-search-sql-contains.md)
</dt> <dt>

[<span data-ttu-id="4e96a-136">WHERE 子句</span><span class="sxs-lookup"><span data-stu-id="4e96a-136">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

<span data-ttu-id="4e96a-137">**概念**</span><span class="sxs-lookup"><span data-stu-id="4e96a-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4e96a-138">非全文檢索述詞</span><span class="sxs-lookup"><span data-stu-id="4e96a-138">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



