---
description: 查詢中的 WHERE 子句會指定一組要與結果比對的專案。
ms.assetid: ed51edd5-6edc-4fcd-a69b-cb48c399ba7c
title: ReuseWhere 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16bb5af4c3acd4637b27a2b3c9c7e14436eabb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972384"
---
# <a name="reusewhere-function"></a><span data-ttu-id="adf28-103">ReuseWhere 函式</span><span class="sxs-lookup"><span data-stu-id="adf28-103">ReuseWhere Function</span></span>

<span data-ttu-id="adf28-104">查詢中的 [WHERE](-search-sql-where.md) 子句會指定一組要與結果比對的專案。</span><span class="sxs-lookup"><span data-stu-id="adf28-104">The [WHERE](-search-sql-where.md) clause in a query specifies a set of items to match results against.</span></span> <span data-ttu-id="adf28-105">後續查詢可以在新的查詢 WHERE 子句中使用 ReuseWhere 函式，來共用先前查詢所執行的工作。</span><span class="sxs-lookup"><span data-stu-id="adf28-105">Subsequent queries can share the work performed for a previous query by using the ReuseWhere function in a new query WHERE clause.</span></span> <span data-ttu-id="adf28-106">利用此函式的查詢執行速度更快。</span><span class="sxs-lookup"><span data-stu-id="adf28-106">Queries that take advantage of this function execute faster.</span></span>

## <a name="examples"></a><span data-ttu-id="adf28-107">範例</span><span class="sxs-lookup"><span data-stu-id="adf28-107">Examples</span></span>

<span data-ttu-id="adf28-108">下列案例顯示如何使用 ReuseWhere 函數：</span><span class="sxs-lookup"><span data-stu-id="adf28-108">The following scenario shows how to use the ReuseWhere function:</span></span>

1.  <span data-ttu-id="adf28-109">您發出下列查詢：</span><span class="sxs-lookup"><span data-stu-id="adf28-109">You issue the following query:</span></span>
    ```
    SELECT System.ItemName FROM SystemIndex 
    WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5'
    ```

    

2.  <span data-ttu-id="adf28-110">從傳回的資料列集，您可以取得 [WHERE 識別碼](-search-sql-rowset-properties.md) *Query1WhereID*。</span><span class="sxs-lookup"><span data-stu-id="adf28-110">From the returned rowset, you get a [Where ID](-search-sql-rowset-properties.md), *Query1WhereID*.</span></span>

    <span data-ttu-id="adf28-111">Where ID 是具有 PROPSET {aa6ee6b0-e828-11d0-b2-3e-00-aa-00-47-fc-01}、PROPID 8 和 type UI4 的資料列集屬性。</span><span class="sxs-lookup"><span data-stu-id="adf28-111">The Where ID is a rowset property with PROPSET {aa6ee6b0-e828-11d0-b2-3e-00-aa-00-47-fc-01 }, PROPID 8, and type UI4.</span></span>

3.  <span data-ttu-id="adf28-112">您可以使用 ReuseWhere 函式發出第二個查詢，並傳入步驟2的 *Query1WhereID* ：</span><span class="sxs-lookup"><span data-stu-id="adf28-112">You issue a second query with the ReuseWhere function, passing in the *Query1WhereID* from step 2:</span></span>
    ```
    SELECT System.ItemUrl FROM SystemIndex 
    WHERE ReuseWhere(Query1WhereID) AND SCOPE='file:'
    ```

    

<span data-ttu-id="adf28-113">第二個查詢相當於下列專案：</span><span class="sxs-lookup"><span data-stu-id="adf28-113">The second query is equivalent to the following:</span></span>


```
SELECT System.ItemUrl, System.ItemName FROM SystemIndex 
WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5' AND Scope='file:'
```



<span data-ttu-id="adf28-114">ReuseWhere 函數可以在 [WHERE](-search-sql-where.md) 子句中 anwhere 使用。</span><span class="sxs-lookup"><span data-stu-id="adf28-114">The ReuseWhere function can be used anwhere in the [WHERE](-search-sql-where.md) clause.</span></span>

## <a name="related-topics"></a><span data-ttu-id="adf28-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="adf28-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="adf28-116">**參考**</span><span class="sxs-lookup"><span data-stu-id="adf28-116">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="adf28-117">WHERE 子句</span><span class="sxs-lookup"><span data-stu-id="adf28-117">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

[<span data-ttu-id="adf28-118">資料列集屬性</span><span class="sxs-lookup"><span data-stu-id="adf28-118">Rowset Properties</span></span>](-search-sql-rowset-properties.md)
</dt> </dl>

 

 



