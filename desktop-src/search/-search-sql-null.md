---
description: Null 述詞指出檔是否有指定之資料行的值。
ms.assetid: 078ffd99-2020-4da2-8968-301dba8cc436
title: Null 述詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea02a04313ac2b86afe809633bee5ad2cbcf764e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972179"
---
# <a name="null-predicate"></a><span data-ttu-id="7fbd0-103">Null 述詞</span><span class="sxs-lookup"><span data-stu-id="7fbd0-103">NULL Predicate</span></span>

<span data-ttu-id="7fbd0-104">**Null** 述詞指出檔是否有指定之資料行的值。</span><span class="sxs-lookup"><span data-stu-id="7fbd0-104">The **NULL** predicate indicates whether the document has a value for the indicated column.</span></span>

<span data-ttu-id="7fbd0-105">**Null** 述詞具有下列語法：</span><span class="sxs-lookup"><span data-stu-id="7fbd0-105">The **NULL** predicate has the following syntax:</span></span>


```
...WHERE <column> IS [NOT] NULL
```



<span data-ttu-id="7fbd0-106">選擇性的 NOT 關鍵字會否定結果。</span><span class="sxs-lookup"><span data-stu-id="7fbd0-106">The optional NOT keyword negates the result.</span></span> <span data-ttu-id="7fbd0-107">此資料行可以是一般或分隔的 [識別碼](-search-sql-identifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="7fbd0-107">The column can be a regular or delimited [identifier](-search-sql-identifiers.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7fbd0-108">若要測試資料行是否有 **null** 值，您必須使用 **null** 述詞。</span><span class="sxs-lookup"><span data-stu-id="7fbd0-108">To test whether a column has the **NULL** value, you must use the **NULL** predicate.</span></span> <span data-ttu-id="7fbd0-109">在比較述詞中使用 **Null** 值是不正確。</span><span class="sxs-lookup"><span data-stu-id="7fbd0-109">It is not valid to use the **NULL** value in a comparison predicate.</span></span> <span data-ttu-id="7fbd0-110">「WHERE 資料行是 **Null**」是正確的。</span><span class="sxs-lookup"><span data-stu-id="7fbd0-110">"WHERE column IS **NULL**" is correct.</span></span> <span data-ttu-id="7fbd0-111">"WHERE column = **Null**" 無效。</span><span class="sxs-lookup"><span data-stu-id="7fbd0-111">"WHERE column = **NULL**" is not valid.</span></span>

 

## <a name="example"></a><span data-ttu-id="7fbd0-112">範例</span><span class="sxs-lookup"><span data-stu-id="7fbd0-112">Example</span></span>

<span data-ttu-id="7fbd0-113">下列範例會傳回沒有 System.object 值的檔。</span><span class="sxs-lookup"><span data-stu-id="7fbd0-113">The following example returns documents that do not have a System.Video.Director value.</span></span>


```
...WHERE System.Video.Director IS NULL
```



## <a name="related-topics"></a><span data-ttu-id="7fbd0-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="7fbd0-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7fbd0-115">**參考**</span><span class="sxs-lookup"><span data-stu-id="7fbd0-115">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7fbd0-116">LIKE 述詞</span><span class="sxs-lookup"><span data-stu-id="7fbd0-116">LIKE Predicate</span></span>](-search-sql-like.md)
</dt> <dt>

[<span data-ttu-id="7fbd0-117">常值比較</span><span class="sxs-lookup"><span data-stu-id="7fbd0-117">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="7fbd0-118">多重值 (陣列) 比較</span><span class="sxs-lookup"><span data-stu-id="7fbd0-118">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

<span data-ttu-id="7fbd0-119">**概念**</span><span class="sxs-lookup"><span data-stu-id="7fbd0-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7fbd0-120">全文檢索述詞</span><span class="sxs-lookup"><span data-stu-id="7fbd0-120">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="7fbd0-121">非全文檢索述詞</span><span class="sxs-lookup"><span data-stu-id="7fbd0-121">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



