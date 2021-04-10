---
description: Windows Search 結構化查詢語言 (SQL)  (SQL) 類似于標準的 SQL 查詢。
ms.assetid: 7d992fa2-4606-46ca-904c-b45056a9bbc2
title: SQL 語法 Windows Search 總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ff6a755312e4358dc2eaa9ea7ae97f22ef783f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026117"
---
# <a name="overview-of-windows-search-sql-syntax"></a><span data-ttu-id="add9a-103">SQL 語法 Windows Search 總覽</span><span class="sxs-lookup"><span data-stu-id="add9a-103">Overview of Windows Search SQL Syntax</span></span>

<span data-ttu-id="add9a-104">Windows Search 結構化查詢語言 (SQL)  (SQL) 類似于標準的 SQL 查詢。</span><span class="sxs-lookup"><span data-stu-id="add9a-104">The Windows Search Structured Query Language (SQL) is similar to a standard SQL query.</span></span> <span data-ttu-id="add9a-105">它會顯示在下列兩個語法中：</span><span class="sxs-lookup"><span data-stu-id="add9a-105">It is shown in the following two syntaxes:</span></span>


```SQL
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>]
```

```SQL
GROUP ON <column> [<ranges>]
[AGGREGATE <aggregate_list>]
[ORDER BY <column> [ASC/DESC]]
OVER (<GROUP ON ...> | <SELECT...>) 
```

<span data-ttu-id="add9a-106">在下列查詢範例中，會針對擁有50個以上頁面的所有檔傳回頁面計數和日期的值，並以頁面計數的遞增順序排序。</span><span class="sxs-lookup"><span data-stu-id="add9a-106">In the following query example, the page count and date created values are returned for all documents which have more than 50 pages, sorted is ascending order of page count.</span></span>

```SQL
SELECT System.Document.PageCount, System.DateCreated
FROM SystemIndex
WHERE (System.Document.PageCount > 50)
ORDER BY System.Document.PageCount
```

<span data-ttu-id="add9a-107">Windows Search 查詢語法支援許多選項，可啟用更複雜的查詢。</span><span class="sxs-lookup"><span data-stu-id="add9a-107">The Windows Search query syntax supports many options, enabling more complicated queries.</span></span>

<span data-ttu-id="add9a-108">下表描述 SELECT 或 GROUP ON 語句中的每個子句，以及支援的功能。</span><span class="sxs-lookup"><span data-stu-id="add9a-108">The following table describes each clause in the SELECT or GROUP ON statements and the features supported.</span></span>

| <span data-ttu-id="add9a-109">子句</span><span class="sxs-lookup"><span data-stu-id="add9a-109">Clause</span></span>                                              | <span data-ttu-id="add9a-110">描述</span><span class="sxs-lookup"><span data-stu-id="add9a-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="add9a-111">分組依據 .。。OVER .。。</span><span class="sxs-lookup"><span data-stu-id="add9a-111">GROUP ON...OVER...</span></span>](-search-sql-group-on-over.md) | <span data-ttu-id="add9a-112">指定如何將查詢所傳回的結果群組。</span><span class="sxs-lookup"><span data-stu-id="add9a-112">Specifies how to group results returned by the query.</span></span> <span data-ttu-id="add9a-113">您可以指定要用來分組的範圍，並指定一個以上的資料行進行分組。</span><span class="sxs-lookup"><span data-stu-id="add9a-113">You can specify the ranges by which to group and specify more than one column for grouping.</span></span> <span data-ttu-id="add9a-114">例如，您可以將檔案大小範圍的結果群組 (大小 < 100、100 <= 大小 < 1000;1000 <= 大小) 和嵌套群組。</span><span class="sxs-lookup"><span data-stu-id="add9a-114">For example, you can group results over a range of file sizes (size < 100, 100 <= size < 1000; 1000 <= size) and nest groupings.</span></span>                                                                                                       |
| [<span data-ttu-id="add9a-115">SELECT</span><span class="sxs-lookup"><span data-stu-id="add9a-115">SELECT</span></span>](-search-sql-select.md)                    | <span data-ttu-id="add9a-116">指定查詢所傳回的資料行。</span><span class="sxs-lookup"><span data-stu-id="add9a-116">Specifies the columns returned by the query.</span></span>                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="add9a-117">FROM</span><span class="sxs-lookup"><span data-stu-id="add9a-117">FROM</span></span>](-search-sql-from.md)                        | <span data-ttu-id="add9a-118">指定要搜尋的電腦和目錄。</span><span class="sxs-lookup"><span data-stu-id="add9a-118">Specifies the machine and catalog to search.</span></span>                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="add9a-119">WHERE</span><span class="sxs-lookup"><span data-stu-id="add9a-119">WHERE</span></span>](-search-sql-where.md)                      | <span data-ttu-id="add9a-120">指定構成相符檔的內容。</span><span class="sxs-lookup"><span data-stu-id="add9a-120">Specifies what constitutes a matching document.</span></span> <span data-ttu-id="add9a-121">這個子句有許多選項，可以讓您在搜尋條件中提供豐富的控制權。</span><span class="sxs-lookup"><span data-stu-id="add9a-121">This clause has many options, enabling rich control over the search conditions.</span></span> <span data-ttu-id="add9a-122">例如，您可以比對單字、片語、字形變化 word 表單、字串、數值和位值，以及多重值陣列。</span><span class="sxs-lookup"><span data-stu-id="add9a-122">For example, you can match against words, phrases, inflectional word forms, strings, numeric and bitwise values, and multi-valued arrays.</span></span> <span data-ttu-id="add9a-123">您也可以將統計權數套用至比對條件，並結合符合條件與布林運算子。</span><span class="sxs-lookup"><span data-stu-id="add9a-123">You can also apply statistical weights to the matching conditions, and combine matching conditions with Boolean operators.</span></span> |
| [<span data-ttu-id="add9a-124">ORDER BY</span><span class="sxs-lookup"><span data-stu-id="add9a-124">ORDER BY</span></span>](-search-sql-orderby.md)                 | <span data-ttu-id="add9a-125">指定查詢所傳回之結果的排序次序。</span><span class="sxs-lookup"><span data-stu-id="add9a-125">Specifies the sort order for the results returned by the query.</span></span> <span data-ttu-id="add9a-126">您可以指定一個以上的欄位來排序結果，而且可以使用遞增或遞減順序。</span><span class="sxs-lookup"><span data-stu-id="add9a-126">You can specify more than one field on which the results are sorted, and you can use ascending or descending ordering.</span></span>                                                                                                                                                                                                               |

### <a name="code-samples"></a><span data-ttu-id="add9a-127">程式碼範例</span><span class="sxs-lookup"><span data-stu-id="add9a-127">Code samples</span></span>

<span data-ttu-id="add9a-128">WSSQL 程式碼範例會示範如何透過 SQL 在 Microsoft OLE DB 和 Windows Search 之間進行通訊。</span><span class="sxs-lookup"><span data-stu-id="add9a-128">The WSSQL code sample demonstrates how to communicate between Microsoft OLE DB and Windows Search through SQL.</span></span> <span data-ttu-id="add9a-129">WSOleDB 程式碼範例說明 Active Template Library (ATL) OLE DB Windows Search 應用程式的存取權，以及兩種從 Windows Search 抓取結果的額外方法。</span><span class="sxs-lookup"><span data-stu-id="add9a-129">The WSOleDB code sample illustrates Active Template Library (ATL) OLE DB access to Windows Search applications, and two additional methods for retrieving results from Windows Search.</span></span> <span data-ttu-id="add9a-130">這兩個範例都可在 [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)上取得。</span><span class="sxs-lookup"><span data-stu-id="add9a-130">Both samples are available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).</span></span>

## <a name="related-topics"></a><span data-ttu-id="add9a-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="add9a-131">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="add9a-132">參考</span><span class="sxs-lookup"><span data-stu-id="add9a-132">Reference</span></span>

[<span data-ttu-id="add9a-133">常值</span><span class="sxs-lookup"><span data-stu-id="add9a-133">Literals</span></span>](-search-sql-literals.md)

[<span data-ttu-id="add9a-134">使用當地語系化的搜尋</span><span class="sxs-lookup"><span data-stu-id="add9a-134">Using Localized Searches</span></span>](-search-sql-usinglocsearches.md)

[<span data-ttu-id="add9a-135">瞭解相關性值</span><span class="sxs-lookup"><span data-stu-id="add9a-135">Understanding Relevance Values</span></span>](-search-sql-understandingrelevancevalues.md)

[<span data-ttu-id="add9a-136">屬性對應</span><span class="sxs-lookup"><span data-stu-id="add9a-136">Property Mappings</span></span>](-search-3x-wds-propertymappings.md)

[<span data-ttu-id="add9a-137">進階查詢語法</span><span class="sxs-lookup"><span data-stu-id="add9a-137">Advanced Query Syntax</span></span>](-search-3x-advancedquerysyntax.md)

### <a name="conceptual"></a><span data-ttu-id="add9a-138">概念</span><span class="sxs-lookup"><span data-stu-id="add9a-138">Conceptual</span></span>

[<span data-ttu-id="add9a-139">Microsoft Windows Search 中的 SQL 擴充功能</span><span class="sxs-lookup"><span data-stu-id="add9a-139">SQL Extensions in Microsoft Windows Search</span></span>](-search-sql-extensions-sps.md)

[<span data-ttu-id="add9a-140">Microsoft Windows Search 中無法使用 SQL 功能</span><span class="sxs-lookup"><span data-stu-id="add9a-140">SQL Features Unavailable in Microsoft Windows Search</span></span>](-search-sql-featuresunavailableinspssearch.md)

[<span data-ttu-id="add9a-141">識別碼</span><span class="sxs-lookup"><span data-stu-id="add9a-141">Identifiers</span></span>](-search-sql-identifiers.md)

[<span data-ttu-id="add9a-142">搜尋中的區分大小寫</span><span class="sxs-lookup"><span data-stu-id="add9a-142">Case Sensitivity in Searches</span></span>](-search-sql-casesensitivityinsearches.md)

[<span data-ttu-id="add9a-143">搜尋中的變音符號敏感度</span><span class="sxs-lookup"><span data-stu-id="add9a-143">Diacritic Sensitivity in Searches</span></span>](-search-sql-accentinsensitivitysearches.md)

[<span data-ttu-id="add9a-144">轉換資料行的資料類型</span><span class="sxs-lookup"><span data-stu-id="add9a-144">Casting the Data Type of a Column</span></span>](-search-sql-castingdatacolumntype.md)

[<span data-ttu-id="add9a-145">資料類型對應</span><span class="sxs-lookup"><span data-stu-id="add9a-145">Data Type Mappings</span></span>](-search-sql-datatypemappings.md)
