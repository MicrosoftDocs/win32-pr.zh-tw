---
title: 正在抓取大型結果集
description: 有可能傳回的結果集將包含超過1000個專案時，您必須使用分頁搜尋。
ms.assetid: 1439d6b8-50dd-4d37-bcc9-dd0f63af865f
ms.tgt_platform: multiple
keywords:
- 正在抓取大型結果集 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f8902d25010690953cfae8a03ff9e500b4ebda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106978559"
---
# <a name="retrieving-large-results-sets"></a><span data-ttu-id="cfdf8-104">正在抓取大型結果集</span><span class="sxs-lookup"><span data-stu-id="cfdf8-104">Retrieving Large Results Sets</span></span>

<span data-ttu-id="cfdf8-105">有可能傳回的結果集將包含超過1000個專案時，您必須使用分頁搜尋。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-105">When there is the possibility that the result set that will be returned will contain more than 1000 items, you must use a paged search.</span></span> <span data-ttu-id="cfdf8-106">在不使用分頁的情況下搜尋 Active Directory，只會傳回最多前1000筆記錄。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-106">Searches of Active Directory performed without paging are limited to returning a maximum of the first 1000 records.</span></span> <span data-ttu-id="cfdf8-107">使用分頁搜尋時，結果集會顯示為個別頁面，每個頁面都包含預定數量的結果專案。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-107">With a paged search, the result set is presented as individual pages, each containing a predetermined number of result entries.</span></span> <span data-ttu-id="cfdf8-108">使用這種搜尋時，會傳回結果專案的新頁面，直到到達結果集的結尾為止。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-108">With this type of search, new pages of result entries are returned until the end of the result set is reached.</span></span>

<span data-ttu-id="cfdf8-109">根據預設，回應查詢要求的伺服器會完全計算結果集，然後才傳回資料。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-109">By default, the server that responds to a query request completely calculates a result set before returning data.</span></span> <span data-ttu-id="cfdf8-110">在大型結果集中，這會在取得結果集時需要伺服器記憶體，並在傳回大型結果時使用網路頻寬。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-110">In a large result set, this requires server memory as the result set is acquired, and network bandwidth when the large result is returned.</span></span> <span data-ttu-id="cfdf8-111">設定頁面大小可讓伺服器在建立頁面時傳送頁面中的資料。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-111">Setting a page size allows the server to send the data in pages as the pages are being built.</span></span> <span data-ttu-id="cfdf8-112">然後，用戶端會快取此資料，並將資料指標提供至應用程式層級程式碼。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-112">The client then caches this data and provides a cursor to the application level code.</span></span> <span data-ttu-id="cfdf8-113">分頁的設定方式是定義伺服器在透過網路將資料傳回給用戶端之前所計算的資料列數目。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-113">Paging is set by defining how many rows the server calculates before the data is returned over the network to the client.</span></span>

<span data-ttu-id="cfdf8-114">分頁搜尋提供用戶端和伺服器的優點。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-114">Paged searching offers benefits to both the client and the server.</span></span> <span data-ttu-id="cfdf8-115">例如，將結果呈現給使用者時，用戶端可能會更有回應。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-115">For example, the client can be more responsive in presenting the results to end users.</span></span> <span data-ttu-id="cfdf8-116">這特別適用于可顯示資料的圖形化使用者介面工具，而另一個執行緒同時從伺服器接收更多資料。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-116">This is especially relevant for graphical user interface tools that can display data while another thread concurrently receives more data from the server.</span></span>

<span data-ttu-id="cfdf8-117">當您設定查詢時，如果您指定結果集的排序次序，則伺服器必須在將資料傳回給用戶端之前，先完整計算結果集，這會影響查詢的回應時間。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-117">When you set up your query, if you specify a sort order for your result set, then the server must completely calculate the result set before returning the data to the client, which impacts the response time for the query.</span></span>

<span data-ttu-id="cfdf8-118">在伺服器端，分頁搜尋可調整作業。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-118">On the server side, paged searching makes the operation scalable.</span></span> <span data-ttu-id="cfdf8-119">例如，如果100用戶端同時發出搜尋要求，且平均每個用戶端傳回200個物件，則如果未指定頁面大小，伺服器必須有足夠的記憶體來保存完整的20000專案結果集。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-119">For example, if one hundred clients issue search requests simultaneously and, on the average, each client is returned two hundred objects, if page size is not specified, the server must have sufficient memory to hold the complete result set of 20,000 entries.</span></span> <span data-ttu-id="cfdf8-120">或者，如果每個用戶端都指定了10個物件的頁面大小，伺服器上的記憶體需求將會以20倍來減少。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-120">Alternately, if each client specified a page size of ten objects, the memory requirements on the server would be reduced by a factor of 20.</span></span>

> [!Note]  
> <span data-ttu-id="cfdf8-121">並非所有目錄服務都支援分頁搜尋。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-121">Not all directory services support paged searches.</span></span> <span data-ttu-id="cfdf8-122">Active Directory 實行頁面大小架構。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-122">Active Directory implements page size architecture.</span></span>

 

<span data-ttu-id="cfdf8-123">如果用戶端未指定頁面大小，許多目錄伺服器會指定可傳回的最大物件數目的管理限制。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-123">Many directory servers specify an Administrative Limit for the maximum number of objects they can return if a client does not specify the page size.</span></span> <span data-ttu-id="cfdf8-124">當達到系統管理限制時，ADSI 會產生 **錯誤 \_ DS 系統 \_ 管理員 \_ 限制 \_ 超過** Win32 錯誤。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-124">When the Administrative Limit is reached, ADSI generates the **ERROR\_DS\_ADMIN\_LIMIT\_EXCEEDED** Win32 error.</span></span>

<span data-ttu-id="cfdf8-125">在用戶端上，分頁搜尋可讓用戶端在作業仍在進行時停止作業。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-125">On the client side, a paged search allows a client to stop the operation while it is still in progress.</span></span> <span data-ttu-id="cfdf8-126">相反地，在非分頁的搜尋中，用戶端會被封鎖，直到資料完全傳回，否則會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-126">By contrast, in a non-paged search, the client is blocked until the data is completely returned, or an error occurs.</span></span> <span data-ttu-id="cfdf8-127">如果結果集變得較大且花費的時間超出預期，這可能會影響網路效能。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-127">This could impact network performance if the result set turns out to be larger and takes more time than expected.</span></span>

<span data-ttu-id="cfdf8-128">ADSI 會代表用戶端以透明的方式處理頁面大小。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-128">On behalf of the client, ADSI handles the page size transparently.</span></span> <span data-ttu-id="cfdf8-129">用戶端不需要計算正在進行中的物件數目。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-129">The client does not have to count the number of objects in progress.</span></span> <span data-ttu-id="cfdf8-130">ADSI 會封裝用戶端的伺服器互動。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-130">ADSI encapsulates the server interaction for the client.</span></span> <span data-ttu-id="cfdf8-131">從用戶端的觀點來看，搜尋會傳回完整的結果集。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-131">From the client perspective, the search returns a complete result set.</span></span>

<span data-ttu-id="cfdf8-132">如需搭配特定搜尋介面使用 [搜尋超時] 選項的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="cfdf8-132">For more information about using the search time out option with a specific search interface, see:</span></span>

-   [<span data-ttu-id="cfdf8-133">使用 >idirectorysearch 進行分頁</span><span class="sxs-lookup"><span data-stu-id="cfdf8-133">Paging with IDirectorySearch</span></span>](paging-with-idirectorysearch.md)
-   [<span data-ttu-id="cfdf8-134">使用 ActiveX Data Objects 搜尋</span><span class="sxs-lookup"><span data-stu-id="cfdf8-134">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="cfdf8-135">使用 OLE DB 搜尋</span><span class="sxs-lookup"><span data-stu-id="cfdf8-135">Searching with OLE DB</span></span>](searching-with-ole-db.md)

<span data-ttu-id="cfdf8-136">分頁搜尋對您的應用程式而言是透明的，因為 ADSI 會自動繼續抓取其他頁面的結果，直到到達結果集的結尾或您設定的時間限制結束為止。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-136">A paged search is transparent to your application because ADSI automatically continues to retrieve additional pages of results until it reaches the end of the result set or the end of the time limit that you set.</span></span> <span data-ttu-id="cfdf8-137">當您使用分頁搜尋時，大小限制不會覆寫頁面大小。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-137">When you use a paged search, the size limit does not override page size.</span></span> <span data-ttu-id="cfdf8-138">只有在您抓取包含少於1000個專案的結果集時，才能使用大小限制。</span><span class="sxs-lookup"><span data-stu-id="cfdf8-138">Size limit can only be used when you retrieve a result set that contains fewer than 1000 entries.</span></span>

 

 




