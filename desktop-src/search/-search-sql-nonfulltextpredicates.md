---
description: Microsoft Windows Search 查詢語言支援六個非全文檢索搜尋述詞。 下表列出本節所述的述詞。
ms.assetid: 74aa6dbc-5c0d-433e-96d9-a8db63907342
title: 非全文檢索述詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d41076ebc61aa56ed547f13f717ac40bed35959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970576"
---
# <a name="non-full-text-predicates"></a><span data-ttu-id="0569c-104">非全文檢索述詞</span><span class="sxs-lookup"><span data-stu-id="0569c-104">Non-Full-Text Predicates</span></span>

<span data-ttu-id="0569c-105">Microsoft Windows Search 查詢語言支援六個非全文檢索搜尋述詞。</span><span class="sxs-lookup"><span data-stu-id="0569c-105">The Microsoft Windows Search query language supports six non-full-text search predicates.</span></span> <span data-ttu-id="0569c-106">下表列出本節所述的述詞。</span><span class="sxs-lookup"><span data-stu-id="0569c-106">The predicates described in this section are listed in the following table.</span></span>



| <span data-ttu-id="0569c-107">非全文檢索述詞</span><span class="sxs-lookup"><span data-stu-id="0569c-107">Non-full-text predicate</span></span>                                                    | <span data-ttu-id="0569c-108">Description</span><span class="sxs-lookup"><span data-stu-id="0569c-108">Description</span></span>                                                                                                                                                                             |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0569c-109">全部位 and 部分位</span><span class="sxs-lookup"><span data-stu-id="0569c-109">ALL BITWISE and SOME BITWISE</span></span>](all-bitwise.md)                            | <span data-ttu-id="0569c-110">這是一組關鍵字，與測試整數類資料型別中的位有關。</span><span class="sxs-lookup"><span data-stu-id="0569c-110">Is a set of keywords that are about testing the bits in an integral type.</span></span>                                                                                                               |
| [<span data-ttu-id="0569c-111">DATEADD 函數</span><span class="sxs-lookup"><span data-stu-id="0569c-111">DATEADD Function</span></span>](-search-sql-dateadd.md)                                | <span data-ttu-id="0569c-112">針對具有日期類型的相符屬性，執行時間和日期計算。</span><span class="sxs-lookup"><span data-stu-id="0569c-112">Performs time and date calculations for matching properties having date types.</span></span> <span data-ttu-id="0569c-113">使用 DATEADD 函數，取得目前的指定時間量內的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="0569c-113">Use the DATEADD function to obtain dates and times in a specified amount of time before the present.</span></span>     |
| [<span data-ttu-id="0569c-114">LIKE 述詞</span><span class="sxs-lookup"><span data-stu-id="0569c-114">LIKE Predicate</span></span>](-search-sql-like.md)                                     | <span data-ttu-id="0569c-115">使用簡單的模式比對與萬用字元來比較資料行值。</span><span class="sxs-lookup"><span data-stu-id="0569c-115">Compares column values using simple pattern matching with wildcard characters.</span></span>                                                                                                          |
| [<span data-ttu-id="0569c-116">常值比較</span><span class="sxs-lookup"><span data-stu-id="0569c-116">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)         | <span data-ttu-id="0569c-117">比較資料行值與字串、日期、時間戳記、數值和其他常值。</span><span class="sxs-lookup"><span data-stu-id="0569c-117">Compares column values against string, date, time stamp, numeric, and other literal values.</span></span> <span data-ttu-id="0569c-118">此述詞支援大於 ( ' > ' ) ，且小於 ( ' < ' ) 的到差異。</span><span class="sxs-lookup"><span data-stu-id="0569c-118">This predicate supports inequalities such as greater than ('>'), and less than ('<').</span></span> |
| [<span data-ttu-id="0569c-119">多重值 (陣列) 比較</span><span class="sxs-lookup"><span data-stu-id="0569c-119">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md) | <span data-ttu-id="0569c-120">比較多值資料行與常值陣列的常值。</span><span class="sxs-lookup"><span data-stu-id="0569c-120">Compares multivalued columns against a multivalued array of literals.</span></span>                                                                                                                   |
| [<span data-ttu-id="0569c-121">Null 述詞</span><span class="sxs-lookup"><span data-stu-id="0569c-121">NULL Predicate</span></span>](-search-sql-null.md)                                     | <span data-ttu-id="0569c-122">偵測檔未定義的資料行值。</span><span class="sxs-lookup"><span data-stu-id="0569c-122">Detects column values that are undefined for the document.</span></span>                                                                                                                              |



 

> [!IMPORTANT]
> <span data-ttu-id="0569c-123">使用 **Null** 述詞的搜尋查詢可能需要 Windows Search 掃描整個目錄，這可能會使查詢的效能變慢。</span><span class="sxs-lookup"><span data-stu-id="0569c-123">Search queries using the **NULL** predicate can require that Windows Search scan the entire catalog, which might slow down the query's performance.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0569c-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="0569c-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0569c-125">全文檢索述詞</span><span class="sxs-lookup"><span data-stu-id="0569c-125">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> </dl>

 

 



