---
description: 必須先建立搜尋查詢，應用程式才能在分散式路由表 (的 DRT) 中搜尋。
ms.assetid: b3403a64-128c-461e-9384-8e62c03322e1
title: 搜尋分散式路由表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9977ca395393cef09198182fb8790738d2b00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985260"
---
# <a name="searching-a-distributed-routing-table"></a><span data-ttu-id="7c269-103">搜尋分散式路由表</span><span class="sxs-lookup"><span data-stu-id="7c269-103">Searching a Distributed Routing Table</span></span>

<span data-ttu-id="7c269-104">必須先建立搜尋查詢，應用程式才能在分散式路由表 (的 DRT) 中搜尋。</span><span class="sxs-lookup"><span data-stu-id="7c269-104">Before an application can search the Distributed Routing Table (DRT), a search query must be created.</span></span> <span data-ttu-id="7c269-105">呼叫 [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch) 函數時，應用程式會指定所需的索引鍵值。</span><span class="sxs-lookup"><span data-stu-id="7c269-105">The desired key value is specified by the application when the [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch) function is called.</span></span> <span data-ttu-id="7c269-106">搜尋的行為是由應用程式在 [**DRT \_ 搜尋 \_ 資訊**](/windows/desktop/api/drt/ns-drt-drt_search_info) 結構中指定的資訊來決定。</span><span class="sxs-lookup"><span data-stu-id="7c269-106">The behavior of the search is determined by information specified by the application in the [**DRT\_SEARCH\_INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info) structure.</span></span>

<span data-ttu-id="7c269-107">一般來說，當搜尋結果和搜尋結束時，會通知應用程式事件。</span><span class="sxs-lookup"><span data-stu-id="7c269-107">Typically, an application event is signaled when the search discovers results and another at the conclusion of the search.</span></span> <span data-ttu-id="7c269-108">但是，如果 **fIterative** 是設定在 [ [**DRT \_ 搜尋 \_ 資訊**](/windows/desktop/api/drt/ns-drt-drt_search_info)] 中，當您在每個節點上進行 contact 時，就可以發出應用程式事件的信號。</span><span class="sxs-lookup"><span data-stu-id="7c269-108">However, if **fIterative** is set in [**DRT\_SEARCH\_INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info), an application event can be signaled when contact is made with each node along the way.</span></span>

<span data-ttu-id="7c269-109">當事件收到信號之後，應用程式就會針對結果呼叫 [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult) 函式。</span><span class="sxs-lookup"><span data-stu-id="7c269-109">After an event is signaled, the application then calls the [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult) function for the results.</span></span> <span data-ttu-id="7c269-110">如果傳回的程式碼 **為 \_ [確定]**，則會在 API 傳回的 [**DRT \_ 搜尋 \_ 結果**](/windows/desktop/api/drt/ns-drt-drt_search_result) 結構中指向結果。</span><span class="sxs-lookup"><span data-stu-id="7c269-110">If the returned code is **S\_OK**, the results are pointed to in the [**DRT\_SEARCH\_RESULT**](/windows/desktop/api/drt/ns-drt-drt_search_result) structure returned by the API.</span></span> <span data-ttu-id="7c269-111">傳回的結果會落在 [**DRT \_ 搜尋 \_ 資訊**](/windows/desktop/api/drt/ns-drt-drt_search_info)中指定的值範圍內。</span><span class="sxs-lookup"><span data-stu-id="7c269-111">The returned results fall into the range of values specified in [**DRT\_SEARCH\_INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info).</span></span> <span data-ttu-id="7c269-112">如果搜尋找不到任何相符專案，則在結果傳回的結果中，只會傳回「 **DRT \_ E \_ 沒有 \_ 其他** 值」。</span><span class="sxs-lookup"><span data-stu-id="7c269-112">In the event that the search finds no matches, only the **DRT\_E\_NO\_MORE** value will be returned at the conclusion of result returns.</span></span>

<span data-ttu-id="7c269-113">下列資訊會詳細說明在 [**drt \_ 搜尋 \_ 資訊**](/windows/desktop/api/drt/ns-drt-drt_search_info) 中包含的成員如何允許應用程式明確地規定 drt 基礎結構的搜尋行為：</span><span class="sxs-lookup"><span data-stu-id="7c269-113">The following information details how the members contained in [**DRT\_SEARCH\_INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info) allow an application to specifically dictate the search behavior of the DRT infrastructure:</span></span>

## <a name="fallowcurrentinstancematch"></a><span data-ttu-id="7c269-114">fAllowCurrentInstanceMatch</span><span class="sxs-lookup"><span data-stu-id="7c269-114">fAllowCurrentInstanceMatch</span></span>

<span data-ttu-id="7c269-115">根據預設，DRT 搜尋結果只會包含在本機節點之外找到的相符專案。</span><span class="sxs-lookup"><span data-stu-id="7c269-115">By default, DRT search results include only matches found outside of the local node.</span></span> <span data-ttu-id="7c269-116">設定 **fAllowCurrentInstanceMatch** 會指定搜尋結果也會包含在本機 DRT 實例中找到的相符專案。</span><span class="sxs-lookup"><span data-stu-id="7c269-116">Setting **fAllowCurrentInstanceMatch** specifies that the search results also include matches found in the local DRT instance.</span></span>

## <a name="cmaxendpoints"></a><span data-ttu-id="7c269-117">cMaxEndpoints</span><span class="sxs-lookup"><span data-stu-id="7c269-117">cMaxEndpoints</span></span>

<span data-ttu-id="7c269-118">搜尋所傳回的結果數量和範圍是由具有 **cMaxEndpoints** (quantity) 和 **pMinimumKey** 和 **pMaximumKey** (範圍) 值的應用程式所指定，並由 [**DRT \_ 搜尋 \_ 資訊**](/windows/desktop/api/drt/ns-drt-drt_search_info)參考。</span><span class="sxs-lookup"><span data-stu-id="7c269-118">The quantity and range of the results returned by the search are specified by the application with the **cMaxEndpoints** (quantity) and the **pMinimumKey** and **pMaximumKey** (range) values, and referenced by [**DRT\_SEARCH\_INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info).</span></span>

<span data-ttu-id="7c269-119">當 **cMaxEndpoints = 1** 時，drt 基礎結構會搜尋索引鍵，然後在 [ [**DRT \_ 搜尋 \_ 資訊**](/windows/desktop/api/drt/ns-drt-drt_search_info)] 中的 **pMinimumKey** 和 **pMaximumKey** 值所指定的範圍內傳回一個相符項。</span><span class="sxs-lookup"><span data-stu-id="7c269-119">When **cMaxEndpoints = 1**, the DRT infrastructure searches for a key, returning one match within the range specified by the **pMinimumKey** and **pMaximumKey** values in [**DRT\_SEARCH\_INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info).</span></span> <span data-ttu-id="7c269-120">此比對可能是完全相符或範圍內最接近的相符項。</span><span class="sxs-lookup"><span data-stu-id="7c269-120">This match can be either an exact match or the nearest match within range.</span></span> <span data-ttu-id="7c269-121">如果找不到相符項，則不會再傳回「 **DRT \_ E \_ \_** 」。</span><span class="sxs-lookup"><span data-stu-id="7c269-121">If a match is not found, **DRT\_E\_NO\_MORE** is returned.</span></span>

<span data-ttu-id="7c269-122">如果 **cMaxEndpoints > 1**，則 DRT 基礎結構會傳回範圍內的相符專案，直到 **cMaxEndpoints** 的值為止。</span><span class="sxs-lookup"><span data-stu-id="7c269-122">If **cMaxEndpoints > 1**, the DRT infrastructure will return matches within the range up to the value of **cMaxEndpoints**.</span></span> <span data-ttu-id="7c269-123">傳回的相符專案可以包含完全相符或範圍內最接近的相符結果。</span><span class="sxs-lookup"><span data-stu-id="7c269-123">The returned matches can contain an exact match or the nearest match results within range.</span></span> <span data-ttu-id="7c269-124">此外，如果 **pMinimumKey** 和 **pMaximumKey** 設定為相同的值，則只會針對該值執行搜尋，如果找不到，則會傳回不 **\_ \_ 含 \_ 其他的 DRT E** 。</span><span class="sxs-lookup"><span data-stu-id="7c269-124">Additionally, if **pMinimumKey** and **pMaximumKey** are set to the same value, a search is carried out only for that value, returning **DRT\_E\_NO\_MORE** if it is not found.</span></span>

## <a name="fanymatchinrange"></a><span data-ttu-id="7c269-125">fAnyMatchInRange</span><span class="sxs-lookup"><span data-stu-id="7c269-125">fAnyMatchInRange</span></span>

<span data-ttu-id="7c269-126">**FAnyMatchInRange** 成員會指出搜尋是否會在第一個相符範圍位於指定的範圍內時停止，或是如果搜尋將繼續進行最符合 [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch) API 中所指定之索引鍵的相符項。</span><span class="sxs-lookup"><span data-stu-id="7c269-126">The **fAnyMatchInRange** member indicates whether the search will stop after the first match is located within the specified range, or if the search will continue for the closest match to the key specified in the [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch) API.</span></span> <span data-ttu-id="7c269-127">設定 **fAnyMatchInRange** 時，無論在 [**DRT \_ 搜尋 \_ 資訊**](/windows/desktop/api/drt/ns-drt-drt_search_info)中指定的 **cMaxEndpoints** 值為何，都會使用 **cMaxEndpoints = 1** 執行搜尋。</span><span class="sxs-lookup"><span data-stu-id="7c269-127">When **fAnyMatchInRange** is set, the search is carried out with **cMaxEndpoints = 1** regardless of the specified value of **cMaxEndpoints** in [**DRT\_SEARCH\_INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info).</span></span>

## <a name="fiterative"></a><span data-ttu-id="7c269-128">fIterative</span><span class="sxs-lookup"><span data-stu-id="7c269-128">fIterative</span></span>

<span data-ttu-id="7c269-129">**FIterative** 成員會指定在搜尋期間，由 DRT 基礎結構聯繫的每個節點是否都有與其相關聯的金鑰/端點資料，可透過 [**DRT \_ 搜尋 \_ 結果**](/windows/desktop/api/drt/ns-drt-drt_search_result)提供給應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="7c269-129">The **fIterative** member specifies if each node contacted by the DRT infrastructure during the search will have the key/endpoint data associated with it made available to the application via [**DRT\_SEARCH\_RESULT**](/windows/desktop/api/drt/ns-drt-drt_search_result).</span></span> <span data-ttu-id="7c269-130">將 **fIterative** 設為 **TRUE**，就會強制 **cMaxEndpoints = 1** 的值。</span><span class="sxs-lookup"><span data-stu-id="7c269-130">By setting **fIterative** to **TRUE**, the value of **cMaxEndpoints = 1** will be forced.</span></span> <span data-ttu-id="7c269-131">當 **fIterative** 在 DRT 的搜尋查詢中設定為 **TRUE** 時，會在與每個節點或「躍點」聯繫之後，將應用程式呼叫回來。</span><span class="sxs-lookup"><span data-stu-id="7c269-131">When **fIterative** is set to **TRUE** within a search query for the DRT, the application is called back after contact with each node or "hop."</span></span> <span data-ttu-id="7c269-132">每個躍點結果都包含一個索引鍵，指出 DRT 將在下一個節點搜尋的節點。</span><span class="sxs-lookup"><span data-stu-id="7c269-132">Each hop result contains a key indicating which node the DRT will search next.</span></span> <span data-ttu-id="7c269-133">躍點結果會透過 [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult) 傳回，以作為 **DRT \_ 相符 \_ 中繼** 結果。</span><span class="sxs-lookup"><span data-stu-id="7c269-133">A hop result is returned via [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult) as a **DRT\_MATCH\_INTERMEDIATE** result.</span></span>

## <a name="pminimumkey-and-pmaximumkey"></a><span data-ttu-id="7c269-134">pMinimumKey 和 pMaximumKey</span><span class="sxs-lookup"><span data-stu-id="7c269-134">pMinimumKey and pMaximumKey</span></span>

<span data-ttu-id="7c269-135">**PMinimumKey** 和 **pMaximumKey** 成員可以用來搜尋範圍內的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="7c269-135">The **pMinimumKey** and **pMaximumKey** members can be used to search for keys falling within a range.</span></span> <span data-ttu-id="7c269-136">如果 **fAnyMatchInRange** 成員設為 **FALSE**，則會將最接近的 (s) 的金鑰傳回給搜尋目標 (使用 [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch) 函數中傳遞的 pKey 引數) 落在範圍內。</span><span class="sxs-lookup"><span data-stu-id="7c269-136">If the **fAnyMatchInRange** member is set to **FALSE**, the DRT will return the closest key(s) to the search target (specified using the pKey argument passed in the [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch) function) falling within the range.</span></span> <span data-ttu-id="7c269-137">請注意，傳遞至 **DrtStartSearch** 的 *pKey* 引數必須落在 **pMinimumKey** 和 **pMaximumKey** 所定義的範圍內。</span><span class="sxs-lookup"><span data-stu-id="7c269-137">Note that the *pKey* argument passed to **DrtStartSearch** must fall within the range defined by **pMinimumKey** and **pMaximumKey**.</span></span> <span data-ttu-id="7c269-138">若要搜尋精確的索引鍵，請將 **pMinimumKey**、 **pMaximumKey** 和 *pKey* 設定為相同的值。</span><span class="sxs-lookup"><span data-stu-id="7c269-138">To search for a precise key, set **pMinimumKey**, **pMaximumKey** and *pKey* to the same value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c269-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="7c269-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c269-140">註冊和取消註冊金鑰</span><span class="sxs-lookup"><span data-stu-id="7c269-140">Registering and Deregistering Keys</span></span>](registering-and-deregistering-keys.md)
</dt> <dt>

[<span data-ttu-id="7c269-141">關於分散式路由表</span><span class="sxs-lookup"><span data-stu-id="7c269-141">About Distributed Routing Tables</span></span>](about-distributed-routing-tables.md)
</dt> <dt>

[<span data-ttu-id="7c269-142">分散式路由資料表 API 參考</span><span class="sxs-lookup"><span data-stu-id="7c269-142">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



