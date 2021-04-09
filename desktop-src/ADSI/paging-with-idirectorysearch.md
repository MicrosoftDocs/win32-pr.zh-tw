---
title: 使用 >idirectorysearch 進行分頁
description: 分頁會指定伺服器傳回給用戶端的資料列數目。
ms.assetid: cf4aa56a-c6f7-47c8-956d-512a5cffbf22
ms.tgt_platform: multiple
keywords:
- 使用 >idirectorysearch ADSI 進行分頁
- ADSI、搜尋、>idirectorysearch、其他搜尋選項、分頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e9fdf001f5908f6c3fc7321c8c94cda09f1b96
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931834"
---
# <a name="paging-with-idirectorysearch"></a><span data-ttu-id="4c2f0-105">使用 >idirectorysearch 進行分頁</span><span class="sxs-lookup"><span data-stu-id="4c2f0-105">Paging with IDirectorySearch</span></span>

<span data-ttu-id="4c2f0-106">分頁會指定伺服器傳回給用戶端的資料列數目。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-106">Paging specifies how many rows that the server returns to the client.</span></span> <span data-ttu-id="4c2f0-107">您可以使用資料列數或時間限制來定義頁面。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-107">A page can be defined by the number of rows or a time limit.</span></span> <span data-ttu-id="4c2f0-108">ADSI COM 物件會根據下表所列的值，抓取每個結果頁面。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-108">The ADSI COM object retrieves each page of results based on the values listed in the following table.</span></span> <span data-ttu-id="4c2f0-109">當呼叫端到達頁面結尾時，呼叫端會呼叫 [**>idirectorysearch：： GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) ，且 ADSI COM 物件會抓取下一頁。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-109">The caller calls [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) when it has reached the page end, and the ADSI COM object retrieves the next page.</span></span>



| <span data-ttu-id="4c2f0-110">值</span><span class="sxs-lookup"><span data-stu-id="4c2f0-110">Value</span></span>                                   | <span data-ttu-id="4c2f0-111">描述</span><span class="sxs-lookup"><span data-stu-id="4c2f0-111">Description</span></span>                                                                                                                                                                                                                                          |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c2f0-112">**ADS \_ SEARCHPREF \_ PAGESIZE**</span><span class="sxs-lookup"><span data-stu-id="4c2f0-112">**ADS\_SEARCHPREF\_PAGESIZE**</span></span>           | <span data-ttu-id="4c2f0-113">指定要在頁面中傳回的最大資料列數目。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-113">Specifies the maximum number of rows to return in a page.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="4c2f0-114">**ADS \_ SEARCHPREF \_ 分頁 \_ 時間 \_ 限制**</span><span class="sxs-lookup"><span data-stu-id="4c2f0-114">**ADS\_SEARCHPREF\_PAGED\_TIME\_LIMIT**</span></span> | <span data-ttu-id="4c2f0-115">指定伺服器在將頁面傳回至用戶端之前，應該花在收集結果頁面的最長時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-115">Specifies the maximum time, in seconds, that the server should spend collecting a page of results before returning the page to the client.</span></span> <span data-ttu-id="4c2f0-116">如果達到限制，伺服器會停止搜尋，並傳回已針對頁面取得的資料列。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-116">If the limit is reached, the server stops the search and returns the rows already retrieved for the page.</span></span> |



 

<span data-ttu-id="4c2f0-117">如果未設定這些搜尋喜好設定，則預設為不分頁。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-117">If neither of these search preferences is set, the default is no paging.</span></span> <span data-ttu-id="4c2f0-118">在不使用分頁的情況下搜尋 Active Directory，只會傳回前1000筆記錄的最大值，因此，如果結果集有可能包含1000個以上的專案，您就必須使用分頁式搜尋。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-118">Searches of the Active Directory performed without paging are limited to returning a maximum of the first 1000 records, so you must use a paged search if there is the possibility that the result set will contain more than 1000 items.</span></span>

<span data-ttu-id="4c2f0-119">搜尋作業可能會導致傳回大量的物件。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-119">A search operation may result in a large number of objects being returned.</span></span> <span data-ttu-id="4c2f0-120">如果伺服器在一個集合中傳回結果，它可能會降低用戶端和伺服器的效能，並影響網路負載。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-120">If the server returns the result in one set, it could decrease the performance of the client and server, as well as affect the network load.</span></span> <span data-ttu-id="4c2f0-121">分頁搜尋可用來防止這種情況。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-121">Paged searches can be used to prevent this.</span></span> <span data-ttu-id="4c2f0-122">在分頁搜尋中，用戶端可以接受較小封包中的結果。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-122">In a paged search, the client can accept results in smaller packets.</span></span> <span data-ttu-id="4c2f0-123">封包的大小稱為搜尋頁面大小。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-123">The size of a packet is known as the search page size.</span></span>

<span data-ttu-id="4c2f0-124">分頁搜尋提供用戶端和伺服器的優點。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-124">Paged searches offer benefits to both the client and the server.</span></span> <span data-ttu-id="4c2f0-125">用戶端可能會在向使用者呈現結果時更具回應性。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-125">The client can be more responsive in presenting the results to users.</span></span> <span data-ttu-id="4c2f0-126">這與圖形化使用者介面工具特別相關，這些工具可以在其他執行緒同時接收資料時，開始視窗顯示進程。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-126">This is especially relevant to graphical user interface tools that can begin the window display process while the other thread concurrently receives the data.</span></span>

<span data-ttu-id="4c2f0-127">在伺服器端，分頁搜尋可讓作業變成可調整的。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-127">On the server side, paged searches make the operation scalable.</span></span> <span data-ttu-id="4c2f0-128">例如，如果100用戶端同時發出搜尋要求，且平均每個用戶端都會收到200物件。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-128">For example, if one hundred clients issue search requests simultaneously and, on the average, each client receives two hundred objects.</span></span> <span data-ttu-id="4c2f0-129">如果未指定頁面大小，則在最糟的情況下，伺服器必須有足夠的記憶體來保存20000物件。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-129">If no page size is specified, in the worst-case scenario, the server must have sufficient memory to hold 20,000 objects.</span></span> <span data-ttu-id="4c2f0-130">相反地，如果每個用戶端指定要做為10個物件的頁面大小，伺服器上的記憶體需求就會降低20倍。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-130">Conversely, if each client specifies a page size to be, for example, ten objects, the memory requirement on the server is thus reduced by a factor of 20.</span></span>

<span data-ttu-id="4c2f0-131">此外，使用分頁搜尋時，用戶端可能會放棄進行中的作業。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-131">In addition, using a paged search, a client can abandon the operation in progress.</span></span> <span data-ttu-id="4c2f0-132">相反地，在非分頁的搜尋中，用戶端會接收一個封包中的結果集。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-132">In contrast, in a non-paged search, the client receives a result set in one packet.</span></span> <span data-ttu-id="4c2f0-133">這可能會降低網路效能。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-133">This can decrease network performance.</span></span>

<span data-ttu-id="4c2f0-134">ADSI 會處理用戶端的頁面大小。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-134">ADSI handles the page size for the client.</span></span> <span data-ttu-id="4c2f0-135">用戶端不需要計算正在進行中的物件數目。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-135">The client does not have to count the number of objects in progress.</span></span> <span data-ttu-id="4c2f0-136">ADSI 會封裝用戶端的伺服器互動。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-136">ADSI encapsulates the server interaction for the client.</span></span> <span data-ttu-id="4c2f0-137">從用戶端的觀點來看，搜尋會傳回完整的結果集。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-137">From the client perspective, the search returns a complete result set.</span></span>

<span data-ttu-id="4c2f0-138">建議使用分頁。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-138">It is recommended that paging is used.</span></span>

<span data-ttu-id="4c2f0-139">若要指定最大頁面大小，請將 [ads **\_ SEARCHPREF \_ PAGESIZE** ] 搜尋 **選項 \_ 設定為 [** [**ads \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) ] 陣列中的每個頁面最大資料列數，並傳遞至 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) 方法。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-139">To specify a maximum page size, set an **ADS\_SEARCHPREF\_PAGESIZE** search option with an **ADSTYPE\_INTEGER** value set to the maximum number of rows per page in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="4c2f0-140">下列程式碼範例顯示如何設定頁面大小上限。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-140">The following code example shows how to set the maximum page size.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



<span data-ttu-id="4c2f0-141">若要指定頁面時間，請設定 **ads \_ SEARCHPREF \_ 分頁 \_ 時間 \_ 限制** 搜尋選項，並將 **ADSTYPE \_ 整數** 值設定為伺服器在傳遞給 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)方法的 [**ADS \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)陣列中，應花費的最大秒數。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-141">To specify a page time, set an **ADS\_SEARCHPREF\_PAGED\_TIME\_LIMIT** search option with an **ADSTYPE\_INTEGER** value set to the maximum number of seconds that the server should spend retrieving a page in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="4c2f0-142">下列程式碼範例顯示如何指定頁面時間。</span><span class="sxs-lookup"><span data-stu-id="4c2f0-142">The following code example shows how to specify page time.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGED_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 60;
```



 

 




