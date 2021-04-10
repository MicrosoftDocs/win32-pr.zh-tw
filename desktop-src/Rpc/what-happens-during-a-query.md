---
title: 查詢期間發生的情況
description: 本節說明當32位用戶端在其自己的網域中搜尋名稱時，網路如何處理查詢。
ms.assetid: a8a88743-a245-4258-af05-9261c214ab50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e26fb9aaef0aac2ff66260d51f756725566dee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183562"
---
# <a name="what-happens-during-a-query"></a><span data-ttu-id="00972-103">查詢期間發生的情況</span><span class="sxs-lookup"><span data-stu-id="00972-103">What Happens During a Query</span></span>

<span data-ttu-id="00972-104">本節說明當32位用戶端在其自己的網域中搜尋名稱時，網路如何處理查詢。</span><span class="sxs-lookup"><span data-stu-id="00972-104">This section describes how the network handles the query when a 32-bit client searches for a name in its own domain.</span></span>

<span data-ttu-id="00972-105">當您的用戶端應用程式呼叫 [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)時，位於用戶端電腦上的定位器將會嘗試滿足此要求。</span><span class="sxs-lookup"><span data-stu-id="00972-105">When your client application calls [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina), the locator residing on your client computer will try to satisfy this request.</span></span> <span data-ttu-id="00972-106">如果快取中沒有任何專案，則會將 RPC 的要求轉寄至主要定位器。</span><span class="sxs-lookup"><span data-stu-id="00972-106">If there is nothing in the cache, it will forward the request by RPC to a master locator.</span></span> <span data-ttu-id="00972-107">如果主要定位器在其快取中找不到任何專案，則會使用郵件位置廣播將要求傳送至網域中的所有電腦。</span><span class="sxs-lookup"><span data-stu-id="00972-107">If the master locator finds nothing in its cache, it sends the request to all the computers in the domain using a mail-slot broadcast.</span></span> <span data-ttu-id="00972-108">如果有相符的，每台電腦上的定位器都會以導向的郵件位置回應。</span><span class="sxs-lookup"><span data-stu-id="00972-108">If there is a match, the locator on each computer will respond by a directed mail slot.</span></span> <span data-ttu-id="00972-109"> (例如，如果該電腦上的進程已匯出介面。 ) 回應會進行定序，而且 RPC 會從用戶端的進程定位器完成，而這將會回復用戶端進程本身。</span><span class="sxs-lookup"><span data-stu-id="00972-109">(For example, if a process on that computer has exported the interface.) The responses are collated and the RPC is completed from the client's process locator, which will reply to the client process itself.</span></span>

<span data-ttu-id="00972-110">在網域中，用戶端定位器會在下列位置中搜尋主要定位器：</span><span class="sxs-lookup"><span data-stu-id="00972-110">In a domain, the client locator searches for a master locator in the following places:</span></span>

-   <span data-ttu-id="00972-111">在網域主控站上</span><span class="sxs-lookup"><span data-stu-id="00972-111">On the primary domain controller</span></span>
-   <span data-ttu-id="00972-112">在每個備份網域控制站上</span><span class="sxs-lookup"><span data-stu-id="00972-112">On each backup domain controller</span></span>

<span data-ttu-id="00972-113">如果找不到相符項，用戶端定位器會將本身宣告為主要定位器。</span><span class="sxs-lookup"><span data-stu-id="00972-113">If a match is not found, the client locator declares itself to be the master locator.</span></span> <span data-ttu-id="00972-114">因此，如果無法在本機滿足查詢，它就會廣播查詢。</span><span class="sxs-lookup"><span data-stu-id="00972-114">As such, it will broadcast queries if they cannot be satisfied locally.</span></span>

<span data-ttu-id="00972-115">在工作組中，用戶端定位器會維護其定位器已廣播之電腦的快取。</span><span class="sxs-lookup"><span data-stu-id="00972-115">In a workgroup, the client locator maintains a cache of the computers whose locators have broadcast.</span></span> <span data-ttu-id="00972-116">它會使用已執行最長的主機定位器。</span><span class="sxs-lookup"><span data-stu-id="00972-116">It uses the one that has been running the longest as the master locator.</span></span> <span data-ttu-id="00972-117">如果該電腦無法使用，則會使用下一個、最長的廣播電腦等等。</span><span class="sxs-lookup"><span data-stu-id="00972-117">If that computer is unavailable, the next, longest-broadcasting computer is used, and so on.</span></span> <span data-ttu-id="00972-118">如果用戶端需要主要定位器，且快取是空的，則會傳送要求主要定位器回應的特殊郵件位置廣播來 replenishes 快取。</span><span class="sxs-lookup"><span data-stu-id="00972-118">If the client needs a master locator and the cache is empty, it replenishes the cache by sending a special mail-slot broadcast that requests master locators to respond.</span></span> <span data-ttu-id="00972-119">如果沒有回應，用戶端定位器會將本身宣告為主要定位器，並在無法在本機滿足查詢時廣播查詢。</span><span class="sxs-lookup"><span data-stu-id="00972-119">If there are no responses, the client locator declares itself to be the master locator and will broadcast queries if they cannot be satisfied locally.</span></span>

<span data-ttu-id="00972-120">如果您的用戶端應用程式是16位或 MS-DOS 型程式，則這會有所變更。</span><span class="sxs-lookup"><span data-stu-id="00972-120">This changes if your client application is a 16-bit or MS-DOS-based program.</span></span> <span data-ttu-id="00972-121">在此情況下，用戶端電腦上沒有執行定位器，Rpcns1.dll 或 Rpcnslm 包含用來尋找主要定位器的程式碼。</span><span class="sxs-lookup"><span data-stu-id="00972-121">In this case, there is no locator running on the client computer, and Rpcns1.dll or Rpcnslm.rpc contains the code to find a master locator.</span></span> <span data-ttu-id="00972-122">所有要求都會直接轉送至主要定位器。</span><span class="sxs-lookup"><span data-stu-id="00972-122">All requests are forwarded directly to the master locator.</span></span>

<span data-ttu-id="00972-123">這些指導方針適用于用戶端網域中的名稱，例如 "/.：/" 的名稱。entryname".</span><span class="sxs-lookup"><span data-stu-id="00972-123">These guidelines are valid for names in the client's domain, such as names for "/.:/entryname".</span></span> <span data-ttu-id="00972-124">如果用戶端透過使用 "/.../DOMAIN/entryname;" 從另一個網域要求名稱，則用戶端定位器會將要求轉送到指定的網域，如果沒有回應，就會廣播該要求。</span><span class="sxs-lookup"><span data-stu-id="00972-124">If the client requests a name from another domain through the use of "/.../DOMAIN/entryname;" the client locator forwards the request to the specified domain which will broadcast it if it does not have the answer.</span></span> <span data-ttu-id="00972-125">如果網域已關閉或實際上是工作組，則要求將會失敗。</span><span class="sxs-lookup"><span data-stu-id="00972-125">If the domain is down or is actually a workgroup, the request will fail.</span></span>

> [!Note]  
> <span data-ttu-id="00972-126">使用名稱服務中的專案時，請記住下列事項：</span><span class="sxs-lookup"><span data-stu-id="00972-126">Remember the following when working with entries in the name service:</span></span>

 

-   <span data-ttu-id="00972-127">用戶端無法使用 "/.../DOMAIN/entryname" 語法在它自己的網域中尋找專案。</span><span class="sxs-lookup"><span data-stu-id="00972-127">A client cannot use the "/.../DOMAIN/entryname" syntax to find an entry in its own domain.</span></span> <span data-ttu-id="00972-128">使用語法 "/.：/entryname".</span><span class="sxs-lookup"><span data-stu-id="00972-128">Use the syntax "/.:/entryname".</span></span> <span data-ttu-id="00972-129">不過，您可以使用 "/.../DOMAIN/entryname" 來尋找另一個網域中的專案。</span><span class="sxs-lookup"><span data-stu-id="00972-129">However, you can use "/.../DOMAIN/entryname" to find an entry in another domain.</span></span>
-   <span data-ttu-id="00972-130">"/.../DOMAIN/entryname" 中的功能變數名稱必須為大寫。</span><span class="sxs-lookup"><span data-stu-id="00972-130">The domain name in "/.../DOMAIN/entryname" must be uppercase.</span></span> <span data-ttu-id="00972-131">尋找相符項時，定位器會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="00972-131">When looking for a match, the locator is case-sensitive.</span></span>
-   <span data-ttu-id="00972-132">定位器專案名稱也會區分大小寫，但不需要為大寫。</span><span class="sxs-lookup"><span data-stu-id="00972-132">Locator entry names are also case-sensitive, but need not be uppercase.</span></span>
-   <span data-ttu-id="00972-133">當用戶端使用 "/.：/entryname "語法，定位器將不會搜尋其他網域中的專案，即使它們與登入網域具有信任關係也一樣。</span><span class="sxs-lookup"><span data-stu-id="00972-133">When the client uses the "/.:/entryname" syntax, the locator will not search for entries in other domains, even if they have a trust relationship with the logon domain.</span></span>
-   <span data-ttu-id="00972-134">廣播不會跨區域網路區段 (例如，子網) 。</span><span class="sxs-lookup"><span data-stu-id="00972-134">Broadcasts do not cross LAN segments (for example, subnets).</span></span> <span data-ttu-id="00972-135">因此，定位器的實用性在具有多個子網的組織中有所限制。</span><span class="sxs-lookup"><span data-stu-id="00972-135">Thus, the usefulness of the locator is limited in an organization with multiple subnets.</span></span>

 

 




