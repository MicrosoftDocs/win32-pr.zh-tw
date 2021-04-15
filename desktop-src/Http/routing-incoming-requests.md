---
title: 路由傳送連入要求
description: HTTP 伺服器 API 會維護路由資料庫，以判斷哪個應用程式會接收傳入要求。
ms.assetid: 7c613137-66bd-4375-93cb-b5562823bc12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da483030441f3a9239eef153da59212166bce9eb
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104383209"
---
# <a name="routing-incoming-requests"></a><span data-ttu-id="3250e-103">路由傳送連入要求</span><span class="sxs-lookup"><span data-stu-id="3250e-103">Routing Incoming Requests</span></span>

<span data-ttu-id="3250e-104">HTTP 伺服器 API 會維護路由資料庫，以判斷哪個應用程式會接收傳入要求。</span><span class="sxs-lookup"><span data-stu-id="3250e-104">The HTTP Server API maintains a routing database to determine which application receives an incoming request.</span></span> <span data-ttu-id="3250e-105">路由表是由保留資料庫所建立，其中包含保留專案以及目前的註冊。</span><span class="sxs-lookup"><span data-stu-id="3250e-105">The routing table is built from the reservation database and contains reservation entries as well as current registrations.</span></span> <span data-ttu-id="3250e-106">進行註冊或保留時，會將它放入對應至主機類型的路由資料庫值區中，如下所示：</span><span class="sxs-lookup"><span data-stu-id="3250e-106">When a registration or reservation is made, it is placed into the routing database bucket that corresponds to the host type as follows:</span></span>

-   <span data-ttu-id="3250e-107">\+ ：埠註冊會放在「強式萬用字元」 bucket 中</span><span class="sxs-lookup"><span data-stu-id="3250e-107">\+ : port registrations are placed in the "Strong Wildcard" bucket</span></span>

-   <span data-ttu-id="3250e-108">主機：埠註冊會放在「明確」 bucket 中</span><span class="sxs-lookup"><span data-stu-id="3250e-108">host : port registrations are placed in the "Explicit" bucket</span></span>

-   <span data-ttu-id="3250e-109">IP：埠註冊會放在「IP 系結弱式萬用字元」 bucket 中</span><span class="sxs-lookup"><span data-stu-id="3250e-109">IP : port registrations are placed in the "IP-bound Weak Wildcard" bucket</span></span>

-   <span data-ttu-id="3250e-110">\* ：埠註冊會放在「弱式萬用字元」 bucket 中</span><span class="sxs-lookup"><span data-stu-id="3250e-110">\* : port registrations are placed in the "Weak Wildcard" bucket</span></span>

<span data-ttu-id="3250e-111">這些步驟也會參考傳入 HTTP 要求的處理順序。</span><span class="sxs-lookup"><span data-stu-id="3250e-111">These steps also refer to the order incoming HTTP requests are processed.</span></span> <span data-ttu-id="3250e-112">強式萬用字元保留專案會先檢查明確的保留，後面接著 IP 系結的弱式萬用字元和弱式萬用字元。</span><span class="sxs-lookup"><span data-stu-id="3250e-112">The strong wildcard reservations first, then the explicit reservation are checked followed by the IP-bound weak wildcard and weak wildcard.</span></span> <span data-ttu-id="3250e-113">找到相符的情況時，就會停止搜尋，因此找不到任何剩餘 bucket 中的註冊。</span><span class="sxs-lookup"><span data-stu-id="3250e-113">The search stops when a match is found so that registrations in any of the remaining buckets are not found.</span></span>

<span data-ttu-id="3250e-114">HTTP 伺服器 API 路由演算法會藉由搜尋路由資料庫的註冊專案和保留專案，從強式萬用字元值區開始，並以弱式萬用字元值區結尾，來找出最符合 [UrlPrefix](urlprefix-strings.md) 的專案。</span><span class="sxs-lookup"><span data-stu-id="3250e-114">The HTTP Server API routing algorithm locates the best match for the [UrlPrefix](urlprefix-strings.md) by searching both the registration entries and the reservation entries of the routing database, starting with the strong wildcard bucket and ending with the weak wildcard bucket.</span></span> <span data-ttu-id="3250e-115">在值區中，最符合的是在 UrlPrefix (的相對 URI 部分中的最長相符項（假設 URL) 的主機、埠和配置部分完全相符）。</span><span class="sxs-lookup"><span data-stu-id="3250e-115">The best match, within a bucket, is the longest match in the relative URI portion of the UrlPrefix (assuming an exact match for the host, port and scheme portions of the URL).</span></span> <span data-ttu-id="3250e-116">在值區中找到相符項之後，路由演算法會停止其搜尋並略過所有較低優先順序的 bucket。</span><span class="sxs-lookup"><span data-stu-id="3250e-116">After a match is found in a bucket, the routing algorithm stops its search and skips all lower priority buckets.</span></span>

<span data-ttu-id="3250e-117">例如，請考慮下列註冊 (根據值區類型以依優先順序遞減的順序列出：</span><span class="sxs-lookup"><span data-stu-id="3250e-117">For example, consider the following registrations (listed in descending order of priority based on bucket types:</span></span>

-   <span data-ttu-id="3250e-118">註冊： `https://+:80/vroot/` 由應用程式1註冊</span><span class="sxs-lookup"><span data-stu-id="3250e-118">Registration: `https://+:80/vroot/` is registered by application 1</span></span>

-   <span data-ttu-id="3250e-119">註冊： `https://adatum.com:80/` 由應用程式2註冊</span><span class="sxs-lookup"><span data-stu-id="3250e-119">Registration: `https://adatum.com:80/` is registered by application 2</span></span>

-   <span data-ttu-id="3250e-120">註冊： `https://\*:80/` 由應用程式3註冊</span><span class="sxs-lookup"><span data-stu-id="3250e-120">Registration: `https://\*:80/` is registered by application 3</span></span>

<span data-ttu-id="3250e-121">的連入要求 `https://adatum.com:80/vroot/subdir/file.htm/` 會傳遞至應用程式1。</span><span class="sxs-lookup"><span data-stu-id="3250e-121">An incoming request for `https://adatum.com:80/vroot/subdir/file.htm/` is delivered to application 1.</span></span> <span data-ttu-id="3250e-122">的連入要求 `https://adatum.com:80/default.htm/` 會傳遞至應用程式2。</span><span class="sxs-lookup"><span data-stu-id="3250e-122">An incoming request for `https://adatum.com:80/default.htm/` is delivered to application 2.</span></span> <span data-ttu-id="3250e-123">的連入要求 `https://otheradatum.com:80/file.htm/` 會傳遞至應用程式3。</span><span class="sxs-lookup"><span data-stu-id="3250e-123">An incoming request for `https://otheradatum.com:80/file.htm/` is delivered to application 3.</span></span>

<span data-ttu-id="3250e-124">如果最符合專案是保留專案，這表示應該接收要求的應用程式不在執行中。</span><span class="sxs-lookup"><span data-stu-id="3250e-124">If the best match is a reservation entry, this means that the application that should receive the request is not running.</span></span> <span data-ttu-id="3250e-125">例如，請考慮下列註冊和保留：</span><span class="sxs-lookup"><span data-stu-id="3250e-125">For example, consider the following registration and reservation:</span></span>

-   <span data-ttu-id="3250e-126">註冊： `https://\*:80/vroot/` 由應用程式1註冊，使用者 A</span><span class="sxs-lookup"><span data-stu-id="3250e-126">Registration: `https://\*:80/vroot/` is registered by application 1, user A</span></span>

-   <span data-ttu-id="3250e-127">保留： `https://adatum.com:80/` 已保留給使用者 B</span><span class="sxs-lookup"><span data-stu-id="3250e-127">Reservation: `https://adatum.com:80/` has been reserved for user B</span></span>

<span data-ttu-id="3250e-128">的連入要求 `https://adatum.com:80/vroot/file.htm/` 未傳遞至應用程式1，因為最符合專案會導致使用者 B 的保留專案。在此情況下，優先順序規則會套用至優先順序較高的保留。</span><span class="sxs-lookup"><span data-stu-id="3250e-128">An incoming request for `https://adatum.com:80/vroot/file.htm/` is not delivered to application 1 because the best match leads to the reservation entry for user B. The precedence rules are applied in this case to the reservation which has a higher priority.</span></span> <span data-ttu-id="3250e-129">如果沒有任何作用中的進程已獲授權，並已向其註冊以取得 URL 的服務要求，則會以400狀態碼 (不正確的要求) 來拒絕該要求。</span><span class="sxs-lookup"><span data-stu-id="3250e-129">If no process is active that is authorized and registered to service requests for the URL received, the request is rejected with a 400 status code (Bad Request).</span></span>

 

 




