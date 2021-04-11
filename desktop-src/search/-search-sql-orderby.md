---
description: 深入瞭解： ORDER BY 子句
ms.assetid: e720cf0d-b034-48e2-a13e-e97dd23b2beb
title: ORDER BY 子句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eaa3c834ca2fe04222ef2ae452a0119bf391b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112420"
---
# <a name="order-by-clause"></a><span data-ttu-id="94bb0-103">ORDER BY 子句</span><span class="sxs-lookup"><span data-stu-id="94bb0-103">ORDER BY Clause</span></span>

<span data-ttu-id="94bb0-104">ORDER BY 子句會根據您指定的一或多個資料行的值來排序結果。</span><span class="sxs-lookup"><span data-stu-id="94bb0-104">The ORDER BY clause sorts the results based on the value of one or more columns you specify.</span></span> <span data-ttu-id="94bb0-105">以下是 ORDER BY 子句的語法：</span><span class="sxs-lookup"><span data-stu-id="94bb0-105">Following is the syntax of the ORDER BY clause:</span></span>


```
ORDER BY <column> [<direction>] [,<column> [<direction>]]
```



<span data-ttu-id="94bb0-106">資料行規范必須是有效的資料行。</span><span class="sxs-lookup"><span data-stu-id="94bb0-106">The column specifier must be a valid column.</span></span> <span data-ttu-id="94bb0-107">您可以使用資料行規范，依照查詢中出現的順序來參考資料行。</span><span class="sxs-lookup"><span data-stu-id="94bb0-107">You can use the column specifier to refer to columns by the order that they appear in the query.</span></span> <span data-ttu-id="94bb0-108">查詢中的第一個資料行編號為1。</span><span class="sxs-lookup"><span data-stu-id="94bb0-108">The first column in the query is numbered 1.</span></span> <span data-ttu-id="94bb0-109">您可以在 ORDER BY 子句中包含一個以上的資料行，並以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="94bb0-109">You can include more than one column in the ORDER BY clause, separated by commas.</span></span>

<span data-ttu-id="94bb0-110">選擇性的方向規範可以是 "ASC" （表示遞增 (低至高) 或 "DESC"），以遞減 (高至低) 。</span><span class="sxs-lookup"><span data-stu-id="94bb0-110">The optional direction specifier can be either "ASC" for ascending (low to high) or "DESC" for descending (high to low).</span></span> <span data-ttu-id="94bb0-111">如果您未提供方向規範，則會使用預設值 [遞增]。</span><span class="sxs-lookup"><span data-stu-id="94bb0-111">If you do not provide a direction specifier, the default, ascending, is used.</span></span> <span data-ttu-id="94bb0-112">如果您指定一個以上的資料行，但未指定所有方向，則您指定的最後一個方向會套用至每個資料行，直到您明確變更方向為止。</span><span class="sxs-lookup"><span data-stu-id="94bb0-112">If you specify more than one column, but do not specify all directions, the direction you specify last is applied to each column until you explicitly change the direction.</span></span>

<span data-ttu-id="94bb0-113">例如，在下列 ORDER BY 子句中，A、B、C 和 G 資料行是以遞增順序排序，而資料行 D、E 和 F 則是以遞減順序排序。</span><span class="sxs-lookup"><span data-stu-id="94bb0-113">For example, in the following ORDER BY clause, the columns A, B, C, and G are sorted in ascending order, while columns D, E, and F are sorted in descending order.</span></span>


```
ORDER BY A ASC, B, C, D DESC, E, F, G ASC
```



## <a name="related-topics"></a><span data-ttu-id="94bb0-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="94bb0-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="94bb0-115">**參考**</span><span class="sxs-lookup"><span data-stu-id="94bb0-115">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="94bb0-116">FROM 子句</span><span class="sxs-lookup"><span data-stu-id="94bb0-116">FROM Clause</span></span>](-search-sql-from.md)
</dt> <dt>

[<span data-ttu-id="94bb0-117">RANK BY 子句</span><span class="sxs-lookup"><span data-stu-id="94bb0-117">RANK BY Clause</span></span>](-search-sql-rankby.md)
</dt> <dt>

[<span data-ttu-id="94bb0-118">SELECT 語句</span><span class="sxs-lookup"><span data-stu-id="94bb0-118">SELECT Statement</span></span>](-search-sql-select.md)
</dt> <dt>

<span data-ttu-id="94bb0-119">**概念**</span><span class="sxs-lookup"><span data-stu-id="94bb0-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="94bb0-120">全文檢索述詞</span><span class="sxs-lookup"><span data-stu-id="94bb0-120">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="94bb0-121">非全文檢索述詞</span><span class="sxs-lookup"><span data-stu-id="94bb0-121">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



