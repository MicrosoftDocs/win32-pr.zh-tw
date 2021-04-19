---
title: 使用 >idirectorysearch 的用戶端時間限制
description: 用戶端可能會強制服務器的時間限制，以傳回結果集。 當伺服器無法在指定的期間內回應查詢時，用戶端可能會放棄搜尋，稍後再試一次。
ms.assetid: fe8a8b08-b34d-4aa5-a925-bcda6e72d437
ms.tgt_platform: multiple
keywords:
- 使用 >idirectorysearch 的用戶端時間限制
- ADSI、搜尋、>idirectorysearch、其他搜尋選項、用戶端時間限制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed25bd8499f7166d7ea494f71e6f78193f9c778a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967185"
---
# <a name="client-time-limit-with-idirectorysearch"></a><span data-ttu-id="e98dc-106">使用 >idirectorysearch 的用戶端時間限制</span><span class="sxs-lookup"><span data-stu-id="e98dc-106">Client Time Limit with IDirectorySearch</span></span>

<span data-ttu-id="e98dc-107">用戶端可能會強制服務器的時間限制，以傳回結果集。</span><span class="sxs-lookup"><span data-stu-id="e98dc-107">A client can impose a time limit for a server to return the result set.</span></span> <span data-ttu-id="e98dc-108">當伺服器無法在指定的期間內回應查詢時，用戶端可能會放棄搜尋，稍後再試一次。</span><span class="sxs-lookup"><span data-stu-id="e98dc-108">When the server fails to respond to a query within the specified time period, the client can abandon the search and try it again later.</span></span>

<span data-ttu-id="e98dc-109">當用戶端要求非同步搜尋時，用戶端時間限制喜好設定會很有用。</span><span class="sxs-lookup"><span data-stu-id="e98dc-109">The client time limit preference is useful when a client requests an asynchronous search.</span></span> <span data-ttu-id="e98dc-110">在非同步搜尋中，用戶端會提出要求，然後在等候伺服器傳回結果時，繼續執行其他工作。</span><span class="sxs-lookup"><span data-stu-id="e98dc-110">In an asynchronous search, the client makes a request and then proceeds with other tasks while waiting for the server to return the results.</span></span> <span data-ttu-id="e98dc-111">伺服器可能會離線，而不會通知用戶端。</span><span class="sxs-lookup"><span data-stu-id="e98dc-111">It is possible that the server can go offline without notifying the client.</span></span> <span data-ttu-id="e98dc-112">在此情況下，用戶端將不會通知伺服器是否仍在處理查詢，或是該查詢已不存在。</span><span class="sxs-lookup"><span data-stu-id="e98dc-112">In this case, the client will have no notification of whether the server is still processing the query, or if it no longer live.</span></span> <span data-ttu-id="e98dc-113">用戶端時間限制喜好設定可讓用戶端控制像這樣的情況。</span><span class="sxs-lookup"><span data-stu-id="e98dc-113">The client time limit preference gives the client some control of situations like this.</span></span>

<span data-ttu-id="e98dc-114">用戶端時間限制的預設值為 [無限制]。</span><span class="sxs-lookup"><span data-stu-id="e98dc-114">The default for the client time limit is no limit.</span></span> <span data-ttu-id="e98dc-115">若要設定用戶端時間限制，請 **將 ads \_ SEARCHPREF \_ TIMEOUT** 搜尋選項設定為 **ADSTYPE \_ 整數** 值，其中包含傳遞給 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)方法的 [**ads \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)陣列中的用戶端時間限制（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e98dc-115">To set a client time limit, set an **ADS\_SEARCHPREF\_TIMEOUT** search option with an **ADSTYPE\_INTEGER** value that contains the client time limit, in seconds, in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="e98dc-116">用戶端時間限制為0表示沒有時間限制。</span><span class="sxs-lookup"><span data-stu-id="e98dc-116">A client time limit of zero indicates no time limit.</span></span>

<span data-ttu-id="e98dc-117">下列程式碼範例顯示如何設定用戶端時間限制。</span><span class="sxs-lookup"><span data-stu-id="e98dc-117">The following code example shows how to set the client time limit.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIMEOUT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




