---
title: 使用 >idirectorysearch 指定其他搜尋選項
description: '>idirectorysearch 介面可讓您透過使用搜尋選項來進一步控制搜尋的執行方式。'
ms.assetid: 91b7ba90-99b3-4137-8e4e-8d0ccfb0ec13
ms.tgt_platform: multiple
keywords:
- 使用 >idirectorysearch ADSI 指定其他搜尋選項
- ADSI、搜尋、>idirectorysearch、其他搜尋選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7064a291c3a299a5435ec454a17b1a666f20d0a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931824"
---
# <a name="specifying-other-search-options-with-idirectorysearch"></a><span data-ttu-id="17f38-105">使用 >idirectorysearch 指定其他搜尋選項</span><span class="sxs-lookup"><span data-stu-id="17f38-105">Specifying Other Search Options with IDirectorySearch</span></span>

<span data-ttu-id="17f38-106">[**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)介面可讓您透過使用搜尋選項來進一步控制搜尋的執行方式。</span><span class="sxs-lookup"><span data-stu-id="17f38-106">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface provide additional control over how the search is performed through the use of search options.</span></span> <span data-ttu-id="17f38-107">這些搜尋選項的設定方式是填入 [**ADS \_ SEARCHPREF \_ 資訊**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) 結構的陣列，然後呼叫 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) 方法。</span><span class="sxs-lookup"><span data-stu-id="17f38-107">These search options are set by filling in an array of [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) structures and calling the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="17f38-108">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="17f38-108">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="17f38-109">使用 SetSearchPreference 方法</span><span class="sxs-lookup"><span data-stu-id="17f38-109">Using the SetSearchPreference Method</span></span>](using-the-setsearchpreference-method.md)
-   [<span data-ttu-id="17f38-110">使用 >idirectorysearch 進行同步和非同步搜尋</span><span class="sxs-lookup"><span data-stu-id="17f38-110">Synchronous and Asynchronous Searches with IDirectorySearch</span></span>](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [<span data-ttu-id="17f38-111">使用 >idirectorysearch 進行分頁</span><span class="sxs-lookup"><span data-stu-id="17f38-111">Paging with IDirectorySearch</span></span>](paging-with-idirectorysearch.md)
-   [<span data-ttu-id="17f38-112">使用 >idirectorysearch 的結果快取</span><span class="sxs-lookup"><span data-stu-id="17f38-112">Result Caching with IDirectorySearch</span></span>](result-caching-with-idirectorysearch.md)
-   [<span data-ttu-id="17f38-113">執行屬性範圍查詢</span><span class="sxs-lookup"><span data-stu-id="17f38-113">Performing an Attribute Scope Query</span></span>](performing-an-attribute-scoped-query.md)
-   [<span data-ttu-id="17f38-114">使用 >idirectorysearch 排序搜尋結果</span><span class="sxs-lookup"><span data-stu-id="17f38-114">Sorting the Search Results with IDirectorySearch</span></span>](sorting-the-search-results-with-idirectorysearch.md)
-   [<span data-ttu-id="17f38-115">使用 >idirectorysearch 的參考追蹤</span><span class="sxs-lookup"><span data-stu-id="17f38-115">Referral Chasing with IDirectorySearch</span></span>](referral-chasing-with-idirectorysearch.md)
-   [<span data-ttu-id="17f38-116">使用 >idirectorysearch 的大小限制</span><span class="sxs-lookup"><span data-stu-id="17f38-116">Size Limit with IDirectorySearch</span></span>](size-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="17f38-117">使用 >idirectorysearch 的伺服器時間限制</span><span class="sxs-lookup"><span data-stu-id="17f38-117">Server Time Limit with IDirectorySearch</span></span>](server-time-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="17f38-118">使用 >idirectorysearch 的用戶端時間限制</span><span class="sxs-lookup"><span data-stu-id="17f38-118">Client Time Limit with IDirectorySearch</span></span>](client-time-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="17f38-119">使用 >idirectorysearch 只傳回屬性名稱</span><span class="sxs-lookup"><span data-stu-id="17f38-119">Returning Only Attribute Names with IDirectorySearch</span></span>](returning-only-attribute-names-with-idirectorysearch.md)

 

 




