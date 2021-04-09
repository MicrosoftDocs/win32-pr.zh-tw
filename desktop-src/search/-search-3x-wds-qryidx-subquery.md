---
description: 子查詢是已儲存的搜尋檔案 (\* . 搜尋-ms) ，您可以用來作為新查詢的篩選準則。
ms.assetid: a92c774f-310b-4c40-be1c-0c2b0cac907b
title: " (Windows Search) 的子查詢引數"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f673cf9c2a9867593fd6c8fdac83b5901f531257
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943281"
---
# <a name="subquery-argument-windows-search"></a><span data-ttu-id="287f2-103"> (Windows Search) 的子查詢引數</span><span class="sxs-lookup"><span data-stu-id="287f2-103">SUBQUERY Argument (Windows Search)</span></span>

<span data-ttu-id="287f2-104">子查詢是已儲存的搜尋檔案 (\* . 搜尋-ms) ，您可以用來作為新查詢的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="287f2-104">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="287f2-105">子查詢的結果會用來作為新查詢的來源。</span><span class="sxs-lookup"><span data-stu-id="287f2-105">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="287f2-106">例如，假設您有數個儲存的搜尋檔案，這些檔案會根據電子郵件通訊群組清單來限制查詢： mydepartment。搜尋-ms、j 和 corporatewide。搜尋-毫秒。</span><span class="sxs-lookup"><span data-stu-id="287f2-106">For example, let's say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="287f2-107">使用 `subquery` 引數可讓您將電子郵件搜尋限制在這些儲存的所有搜尋中。</span><span class="sxs-lookup"><span data-stu-id="287f2-107">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

<span data-ttu-id="287f2-108">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="287f2-108">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="287f2-109">範例</span><span class="sxs-lookup"><span data-stu-id="287f2-109">Example</span></span>](#example)
-   [<span data-ttu-id="287f2-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="287f2-110">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="287f2-111">範例</span><span class="sxs-lookup"><span data-stu-id="287f2-111">Example</span></span>


```
 search-ms:query=vacation&subquery=mydepartment.search-ms
```



## <a name="related-topics"></a><span data-ttu-id="287f2-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="287f2-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="287f2-113">具有 Parameter-Value 引數的開始使用</span><span class="sxs-lookup"><span data-stu-id="287f2-113">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="287f2-114">地區設定識別碼引數</span><span class="sxs-lookup"><span data-stu-id="287f2-114">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[<span data-ttu-id="287f2-115">連結引數</span><span class="sxs-lookup"><span data-stu-id="287f2-115">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[<span data-ttu-id="287f2-116">語法引數</span><span class="sxs-lookup"><span data-stu-id="287f2-116">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="287f2-117">STACKEDBY 引數</span><span class="sxs-lookup"><span data-stu-id="287f2-117">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> </dl>

 

 



