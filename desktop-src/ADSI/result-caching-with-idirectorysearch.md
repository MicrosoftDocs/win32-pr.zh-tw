---
title: 使用 >idirectorysearch 的結果快取
description: ADS SEARCHPREF 快取 \_ \_ 結果喜好設定會快取 \_ 用戶端上的結果集。
ms.assetid: bb286879-7d84-4085-88e1-600c848b8af8
ms.tgt_platform: multiple
keywords:
- 使用 >idirectorysearch ADSI 的結果快取
- ADSI、搜尋、>idirectorysearch、其他搜尋選項、結果快取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95016699eb4de36344b7e40f35e1a4a9cce761b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300064"
---
# <a name="result-caching-with-idirectorysearch"></a><span data-ttu-id="dc80d-105">使用 >idirectorysearch 的結果快取</span><span class="sxs-lookup"><span data-stu-id="dc80d-105">Result Caching with IDirectorySearch</span></span>

<span data-ttu-id="dc80d-106">**ADS SEARCHPREF 快取 \_ \_ \_ 結果** 喜好設定會快取用戶端上的結果集。</span><span class="sxs-lookup"><span data-stu-id="dc80d-106">The **ADS\_SEARCHPREF\_CACHE\_RESULTS** preference caches the result set on the client.</span></span> <span data-ttu-id="dc80d-107">結果快取可讓應用程式保留抓取的結果集，並再次流覽抓取過的資料列。</span><span class="sxs-lookup"><span data-stu-id="dc80d-107">Result caching enables an application to retain a retrieved result set and go through the retrieved rows again.</span></span> <span data-ttu-id="dc80d-108">它也會啟用資料指標支援，其中 [**>idirectorysearch：： GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) 和 [**>idirectorysearch：： GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) 方法可以用來向上和向下移動結果集。</span><span class="sxs-lookup"><span data-stu-id="dc80d-108">It also enables cursor support where the [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) and [**IDirectorySearch::GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) methods can be used to move up and down the result set.</span></span>

<span data-ttu-id="dc80d-109">預設會停用結果快取。</span><span class="sxs-lookup"><span data-stu-id="dc80d-109">By default, result caching is disabled.</span></span> <span data-ttu-id="dc80d-110">如果下列任何一個條件成立，則應該啟用結果快取：</span><span class="sxs-lookup"><span data-stu-id="dc80d-110">Result caching should be enabled if any one of the following is true:</span></span>

-   <span data-ttu-id="dc80d-111">如果相同的結果集必須列舉多次，而不在伺服器上再次執行搜尋。</span><span class="sxs-lookup"><span data-stu-id="dc80d-111">If the same result set must be enumerated multiple times without performing the search again on the server.</span></span>
-   <span data-ttu-id="dc80d-112">如果執行搜尋需要耗用大量資源的伺服器 (慢速連線、大型結果集或複雜查詢) 。</span><span class="sxs-lookup"><span data-stu-id="dc80d-112">If performing the search is resource-intensive on the server (slow connection, large result set, or complex query).</span></span>
-   <span data-ttu-id="dc80d-113">如果需要資料指標支援。</span><span class="sxs-lookup"><span data-stu-id="dc80d-113">If cursor support is required.</span></span>

<span data-ttu-id="dc80d-114">如果您的應用程式必須減少在用戶端快取大型結果集的記憶體需求，請關閉快取。</span><span class="sxs-lookup"><span data-stu-id="dc80d-114">Turn off caching if your application must reduce memory requirements for caching a large result set at the client.</span></span>

<span data-ttu-id="dc80d-115">結果快取會增加用戶端的記憶體需求，因此，如果這是問題，則應該停用結果快取。</span><span class="sxs-lookup"><span data-stu-id="dc80d-115">Result caching increases the memory requirements on the client, so result caching should be disabled if this is a concern.</span></span>

<span data-ttu-id="dc80d-116">若要啟用結果快取，請在傳遞給 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)方法的 [**ads \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)陣列中，設定 SEARCHPREF 快取 **\_ \_ \_ 結果** 搜尋選項 **ADSTYPE \_ 布林** 值為 **TRUE** 的 ads。</span><span class="sxs-lookup"><span data-stu-id="dc80d-116">To enable result caching, set an **ADS\_SEARCHPREF\_CACHE\_RESULTS** search option with an **ADSTYPE\_BOOLEAN** value of **TRUE** in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="dc80d-117">下列程式碼範例顯示如何啟用結果快取。</span><span class="sxs-lookup"><span data-stu-id="dc80d-117">The following code example shows how to enable result caching.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CACHE_RESULTS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




