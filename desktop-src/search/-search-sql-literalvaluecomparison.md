---
description: 常值比較會使用標準比較運算子來比對單一值資料行與常值。
ms.assetid: 941298b4-d703-4b3f-8bde-0e6e158560df
title: 常值比較
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d8577e5a97dcc92131658c325f175efa1d0c3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997079"
---
# <a name="literal-value-comparison"></a><span data-ttu-id="51b85-103">常值比較</span><span class="sxs-lookup"><span data-stu-id="51b85-103">Literal Value Comparison</span></span>

<span data-ttu-id="51b85-104">常值比較會使用標準比較運算子來比對單一值資料行與 [常](-search-sql-literals.md) 值。</span><span class="sxs-lookup"><span data-stu-id="51b85-104">The literal value comparison uses standard comparison operators for matching a single-valued column to a [literal](-search-sql-literals.md) value.</span></span> <span data-ttu-id="51b85-105">如需有關比較多值資料行的詳細資訊，請參閱 [多重值 (陣列) 比較](-search-sql-multivaluedcomparisons.md)。</span><span class="sxs-lookup"><span data-stu-id="51b85-105">For information about comparing multivalued columns, see [Multi-Valued (ARRAY) Comparisons](-search-sql-multivaluedcomparisons.md).</span></span>

<span data-ttu-id="51b85-106">常值比較述詞具有下列語法：</span><span class="sxs-lookup"><span data-stu-id="51b85-106">The literal value comparison predicate has the following syntax:</span></span>


```
...WHERE <column> <comparison operator> <literal>
```



> [!Note]  
> <span data-ttu-id="51b85-107">比較的右側必須是常值。</span><span class="sxs-lookup"><span data-stu-id="51b85-107">The right side of the comparison must be a literal.</span></span> <span data-ttu-id="51b85-108">您無法將資料行與計算的值相比較，也無法將資料行與另一個資料行進行比較。</span><span class="sxs-lookup"><span data-stu-id="51b85-108">You cannot compare a column against a computed value, and you cannot compare a column against another column.</span></span>

 

<span data-ttu-id="51b85-109">資料行部分是任何有效的屬性資料行，如有必要，可以轉換成另一種類型。</span><span class="sxs-lookup"><span data-stu-id="51b85-109">The column part is any valid property column and can be cast to another type if necessary.</span></span> <span data-ttu-id="51b85-110">（選擇性）您可以用雙引號括住資料行名稱，以利可讀性，而不會影響功能。</span><span class="sxs-lookup"><span data-stu-id="51b85-110">Optionally, you can enclose the column name in double quotes for readability without affecting functionality.</span></span> <span data-ttu-id="51b85-111">如需詳細資訊，請參閱 [轉換資料行的資料類型](-search-sql-castingdatacolumntype.md)。</span><span class="sxs-lookup"><span data-stu-id="51b85-111">For more information, see [Casting the Data Type of a Column](-search-sql-castingdatacolumntype.md).</span></span>

<span data-ttu-id="51b85-112">常值可以是任何字串、數值、十六進位、布林值或日期常值（以單引號括住）。</span><span class="sxs-lookup"><span data-stu-id="51b85-112">The literal can be any string, numeric, hexadecimal, Boolean, or date literal, enclosed in single quotation marks.</span></span> <span data-ttu-id="51b85-113">只會辨識完全相符的專案，而且會忽略萬用字元。</span><span class="sxs-lookup"><span data-stu-id="51b85-113">Only exact matches are recognized, and wildcard characters are ignored.</span></span> <span data-ttu-id="51b85-114">常值也可以轉換成另一種類型。</span><span class="sxs-lookup"><span data-stu-id="51b85-114">The literal can also be cast to another type.</span></span>

## <a name="comparison-operators"></a><span data-ttu-id="51b85-115">比較運算子</span><span class="sxs-lookup"><span data-stu-id="51b85-115">Comparison Operators</span></span>

<span data-ttu-id="51b85-116">下表描述支援的比較運算子。</span><span class="sxs-lookup"><span data-stu-id="51b85-116">The following table describes the supported comparison operators.</span></span>



| <span data-ttu-id="51b85-117">比較運算子</span><span class="sxs-lookup"><span data-stu-id="51b85-117">Comparison operator</span></span> | <span data-ttu-id="51b85-118">描述</span><span class="sxs-lookup"><span data-stu-id="51b85-118">Description</span></span>              |
|---------------------|--------------------------|
| =                   | <span data-ttu-id="51b85-119">等於</span><span class="sxs-lookup"><span data-stu-id="51b85-119">Equal to</span></span>                 |
| <span data-ttu-id="51b85-120">！ = 或 <></span><span class="sxs-lookup"><span data-stu-id="51b85-120">!= or <></span></span>      | <span data-ttu-id="51b85-121">不等於</span><span class="sxs-lookup"><span data-stu-id="51b85-121">Not equal to</span></span>             |
| >                | <span data-ttu-id="51b85-122">大於</span><span class="sxs-lookup"><span data-stu-id="51b85-122">Greater than</span></span>             |
| >=               | <span data-ttu-id="51b85-123">大於或等於</span><span class="sxs-lookup"><span data-stu-id="51b85-123">Greater than or equal to</span></span> |
| <                | <span data-ttu-id="51b85-124">小於</span><span class="sxs-lookup"><span data-stu-id="51b85-124">Less than</span></span>                |
| <=               | <span data-ttu-id="51b85-125">小於或等於</span><span class="sxs-lookup"><span data-stu-id="51b85-125">Less than or equal to</span></span>    |



 

 

<span data-ttu-id="51b85-126">使用 "=" 運算子時，Windows Search 結構化查詢語言 (SQL)  (SQL) 支援使用 BEFORE 和 AFTER 關鍵字，以指定查詢是否應該在字典排序次序中，比較指定值之前或之後的資料行值。</span><span class="sxs-lookup"><span data-stu-id="51b85-126">In conjunction with the "=" operator, Windows Search Structured Query Language (SQL) supports the use of BEFORE and AFTER keywords, which specify whether the query should compare column values before or after a specified value, in dictionary sort ordering.</span></span>


```
...WHERE <column> <comparison operator> [BEFORE | AFTER](<https://msdn.microsoft.com/library/Ff637626(v=MSDN.10).aspx>)
```



## <a name="examples"></a><span data-ttu-id="51b85-127">範例</span><span class="sxs-lookup"><span data-stu-id="51b85-127">Examples</span></span>

<span data-ttu-id="51b85-128">以下是常值比較述詞的範例。</span><span class="sxs-lookup"><span data-stu-id="51b85-128">The following are examples of the literal value comparison predicate.</span></span>


```
SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Title = 'Accounting'

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.IsFlagged != TRUE

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Size >= 10000

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Author = BEFORE('m')
```



## <a name="related-topics"></a><span data-ttu-id="51b85-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="51b85-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="51b85-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="51b85-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="51b85-131">LIKE 述詞</span><span class="sxs-lookup"><span data-stu-id="51b85-131">LIKE Predicate</span></span>](-search-sql-like.md)
</dt> <dt>

[<span data-ttu-id="51b85-132">DATEADD 函數</span><span class="sxs-lookup"><span data-stu-id="51b85-132">DATEADD Function</span></span>](-search-sql-dateadd.md)
</dt> <dt>

[<span data-ttu-id="51b85-133">多重值 (陣列) 比較</span><span class="sxs-lookup"><span data-stu-id="51b85-133">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

[<span data-ttu-id="51b85-134">Null 述詞</span><span class="sxs-lookup"><span data-stu-id="51b85-134">NULL Predicate</span></span>](-search-sql-null.md)
</dt> <dt>

<span data-ttu-id="51b85-135">**概念**</span><span class="sxs-lookup"><span data-stu-id="51b85-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="51b85-136">全文檢索述詞</span><span class="sxs-lookup"><span data-stu-id="51b85-136">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="51b85-137">非全文檢索述詞</span><span class="sxs-lookup"><span data-stu-id="51b85-137">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



