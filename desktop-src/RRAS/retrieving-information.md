---
title: 擷取資訊
description: RTMv2 可讓用戶端使用 RtmGetEntityInfo、RtmGetDestInfo、RtmGetRouteInfo 和 RtmGetNextHopInfo 函式，來取得指定控制碼所參考的資訊。
ms.assetid: a3fc2020-eac4-40a1-9a6e-6eaa2bcc582c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058a87c9463011aec55b0c6c8c0574ff1e013f23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183101"
---
# <a name="retrieving-information"></a><span data-ttu-id="2d05e-103">擷取資訊</span><span class="sxs-lookup"><span data-stu-id="2d05e-103">Retrieving Information</span></span>

<span data-ttu-id="2d05e-104">RTMv2 可讓用戶端使用 [**RtmGetEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo)、 [**RtmGetDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo)、 [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo)和 [**RtmGetNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) 函式，來取得指定控制碼所參考的資訊。</span><span class="sxs-lookup"><span data-stu-id="2d05e-104">RTMv2 allows a client to retrieve the information referred to by a given handle using the [**RtmGetEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**RtmGetDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo), [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo), and [**RtmGetNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) functions.</span></span>

<span data-ttu-id="2d05e-105">這些函式呼叫具有對應的函數 ([**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo)、 [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo)、 [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo)、 [**RtmReleaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)) 來釋出與路由表管理員所傳回之資訊結構相關聯的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2d05e-105">These function calls have corresponding functions ([**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo), [**RtmReleaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)) to release the handles associated with the information structure returned by the routing table manager.</span></span>

> [!Note]  
> <span data-ttu-id="2d05e-106">用戶端的資訊僅適用于目前的實例和位址系列。</span><span class="sxs-lookup"><span data-stu-id="2d05e-106">Information for clients is available only in the current instance and address family.</span></span>

 

<span data-ttu-id="2d05e-107">如需示範如何使用這些函式的範例程式碼，請參閱 [搜尋最佳路由](search-for-the-best-route.md)。</span><span class="sxs-lookup"><span data-stu-id="2d05e-107">For sample code that shows how to use these functions, see [Search For the Best Route](search-for-the-best-route.md).</span></span>

## <a name="using-rtmgetexactmatchroute-and-rtmgetexactmatchdestination"></a><span data-ttu-id="2d05e-108">使用 RtmGetExactMatchRoute 和 RtmGetExactMatchDestination</span><span class="sxs-lookup"><span data-stu-id="2d05e-108">Using RtmGetExactMatchRoute and RtmGetExactMatchDestination</span></span>

<span data-ttu-id="2d05e-109">用戶端會使用 [**RtmGetExactMatchRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute) 和 [**RtmGetExactMatchDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination) 函數來尋找特定的路由或目的地。</span><span class="sxs-lookup"><span data-stu-id="2d05e-109">The [**RtmGetExactMatchRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute) and [**RtmGetExactMatchDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination) functions are used by clients to find a specific route or destination.</span></span> <span data-ttu-id="2d05e-110">這些函式會藉由執行用戶端的比較工作來節省時間。</span><span class="sxs-lookup"><span data-stu-id="2d05e-110">These functions save time by doing the comparison work for the client.</span></span>

<span data-ttu-id="2d05e-111">例如，當 RIP 更新路由時，RIP 必須保留舊的度量資訊。</span><span class="sxs-lookup"><span data-stu-id="2d05e-111">For example, when RIP updates a route, RIP must retain the old metric information.</span></span> <span data-ttu-id="2d05e-112">RIP 會搜尋路由及其資訊。</span><span class="sxs-lookup"><span data-stu-id="2d05e-112">RIP searches for the route and its information.</span></span> <span data-ttu-id="2d05e-113">然後，RIP 可以複製資訊並更新路由。</span><span class="sxs-lookup"><span data-stu-id="2d05e-113">Then RIP can copy the information and update the route.</span></span>

## <a name="using-rtmgetmostspecificdestination"></a><span data-ttu-id="2d05e-114">使用 RtmGetMostSpecificDestination</span><span class="sxs-lookup"><span data-stu-id="2d05e-114">Using RtmGetMostSpecificDestination</span></span>

<span data-ttu-id="2d05e-115">[**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination)函式可用來尋找最符合指定之網路首碼的目的地。</span><span class="sxs-lookup"><span data-stu-id="2d05e-115">The [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination) function is used to locate the destination that best matches the specified network prefix.</span></span>

<span data-ttu-id="2d05e-116">例如，多播群組管理員會使用此函數來執行反向路徑轉送 (RPF) 檢查單一位址。</span><span class="sxs-lookup"><span data-stu-id="2d05e-116">For example, the multicast group manager uses this function to perform a reverse-path-forwarding (RPF) check on a single address.</span></span> <span data-ttu-id="2d05e-117">函數也可以用來尋找指定遠端下一個躍點的本機下一個躍點。</span><span class="sxs-lookup"><span data-stu-id="2d05e-117">The function can also be used to find the local next hop for a given remote next hop.</span></span>

<span data-ttu-id="2d05e-118">如需示範如何使用這些函式的範例程式碼，請參閱 [使用前置詞樹狀目錄搜尋路由](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md) ，並 [搜尋最佳路由](search-for-the-best-route.md)。</span><span class="sxs-lookup"><span data-stu-id="2d05e-118">For sample code that shows how to use these functions, see [Search for Routes Using a Prefix Tree](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md) and [Search For the Best Route](search-for-the-best-route.md).</span></span>

## <a name="using-rtmgetlessspecificdestination"></a><span data-ttu-id="2d05e-119">使用 RtmGetLessSpecificDestination</span><span class="sxs-lookup"><span data-stu-id="2d05e-119">Using RtmGetLessSpecificDestination</span></span>

<span data-ttu-id="2d05e-120">[**RtmGetLessSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination)函式是用來找出下一個最符合指定網路首碼的目的地。</span><span class="sxs-lookup"><span data-stu-id="2d05e-120">The [**RtmGetLessSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination) function is used to locate the destination that is the next-best match for the specified network prefix.</span></span> <span data-ttu-id="2d05e-121">您可以重複呼叫這個函式，以傳回下一次較不相符的相符項，直到沒有其他目的地相符為止。</span><span class="sxs-lookup"><span data-stu-id="2d05e-121">This function can be called repeatedly to return the next successive less-specific match, until no more destinations match.</span></span>

<span data-ttu-id="2d05e-122">呼叫 [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination)之後，會呼叫這個函式。</span><span class="sxs-lookup"><span data-stu-id="2d05e-122">This function is called after a call to [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination).</span></span>

<span data-ttu-id="2d05e-123">如需說明如何使用這些函式的範例程式碼，請參閱 [使用前置詞樹狀目錄搜尋路由](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md)。</span><span class="sxs-lookup"><span data-stu-id="2d05e-123">For sample code that illustrates how to use these functions, see [Search for Routes Using a Prefix Tree](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md).</span></span>

## <a name="using-rtmisbestroute"></a><span data-ttu-id="2d05e-124">使用 RtmIsBestRoute</span><span class="sxs-lookup"><span data-stu-id="2d05e-124">Using RtmIsBestRoute</span></span>

<span data-ttu-id="2d05e-125">[**RtmIsBestRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute)函式可讓用戶端快速找出特定路由是否為目的地的最佳路由。</span><span class="sxs-lookup"><span data-stu-id="2d05e-125">The [**RtmIsBestRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute) function enables a client to quickly find out whether or not a particular route is the best route to a destination.</span></span> <span data-ttu-id="2d05e-126">例如，如果用戶端是最適合的路由，則可能需要儲存特定的路由。</span><span class="sxs-lookup"><span data-stu-id="2d05e-126">For example, a client may need to store a particular route only if it is the best route.</span></span> <span data-ttu-id="2d05e-127">因此，用戶端可以呼叫這個函式，而不是列舉所有路由並進行比較。</span><span class="sxs-lookup"><span data-stu-id="2d05e-127">Therefore, the client can call this function, instead of enumerating all routes and making the comparison itself.</span></span>

 

 




