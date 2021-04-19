---
title: 使用 RtmAddRouteToDest 新增和更新路由
description: 函數 RtmAddRouteToDest 可用來加入新的路由，並更新目的地的現有路由。 下列程式說明這兩種情況。 下列範例程式碼顯示如何執行第一個程式。
ms.assetid: 17a04511-69f8-4e50-993c-0e558ee72184
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd3594aee054e6815094834bedbc1aae158fc4e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106990878"
---
# <a name="add-and-update-routes-using-rtmaddroutetodest"></a><span data-ttu-id="e91b0-105">使用 RtmAddRouteToDest 新增和更新路由</span><span class="sxs-lookup"><span data-stu-id="e91b0-105">Add and Update Routes Using RtmAddRouteToDest</span></span>

<span data-ttu-id="e91b0-106">函數 [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) 可用來加入新的路由，並更新目的地的現有路由。</span><span class="sxs-lookup"><span data-stu-id="e91b0-106">The function [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) is used to add new routes and update existing routes for a destination.</span></span> <span data-ttu-id="e91b0-107">下列程式說明這兩種情況。</span><span class="sxs-lookup"><span data-stu-id="e91b0-107">The following procedures explain both cases.</span></span> <span data-ttu-id="e91b0-108">下列範例程式碼顯示如何執行第一個程式。</span><span class="sxs-lookup"><span data-stu-id="e91b0-108">The sample code that follows shows how to implement the first procedure.</span></span>

<span data-ttu-id="e91b0-109">**若要新增路由，用戶端應該採取下列步驟：**</span><span class="sxs-lookup"><span data-stu-id="e91b0-109">**To add a route, the client should take the following steps**</span></span>

1.  <span data-ttu-id="e91b0-110">如果用戶端已經快取下一個躍點控制碼，請移至步驟4。</span><span class="sxs-lookup"><span data-stu-id="e91b0-110">If the client has already cached the next-hop handle, go to step 4.</span></span>
2.  <span data-ttu-id="e91b0-111">建立 [**RTM \_ NEXTHOP \_ 資訊**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) 結構，並填入適當的資訊。</span><span class="sxs-lookup"><span data-stu-id="e91b0-111">Create an [**RTM\_NEXTHOP\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) structure and fill it with the appropriate information.</span></span>
3.  <span data-ttu-id="e91b0-112">藉由呼叫 [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop)，將下一個躍點新增至路由表。</span><span class="sxs-lookup"><span data-stu-id="e91b0-112">Add the next hop to the routing table by calling [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop).</span></span> <span data-ttu-id="e91b0-113">路由表管理員會將控制碼傳回到下一個躍點。</span><span class="sxs-lookup"><span data-stu-id="e91b0-113">The routing table manager returns a handle to the next hop.</span></span> <span data-ttu-id="e91b0-114">如果下一個躍點已經存在，則路由表不會新增下一個躍點;相反地，它會將控制碼傳回至下一個躍點。</span><span class="sxs-lookup"><span data-stu-id="e91b0-114">If the next hop already exists, the routing table does not add the next hop; instead it returns the handle to the next hop.</span></span>
4.  <span data-ttu-id="e91b0-115">建立 [**RTM \_ 路由 \_ 資訊**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) 結構並填入適當的資訊，包括路由表管理員所傳回的下個躍點控制碼。</span><span class="sxs-lookup"><span data-stu-id="e91b0-115">Create an [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure and fill it with the appropriate information, including the next-hop handle returned by the routing table manager.</span></span>
5.  <span data-ttu-id="e91b0-116">藉由呼叫 [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest)，將路由新增至路由表。</span><span class="sxs-lookup"><span data-stu-id="e91b0-116">Add the route to the routing table by calling [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest).</span></span> <span data-ttu-id="e91b0-117">路由表管理員會將新路由與已經在路由表中的路由進行比較。</span><span class="sxs-lookup"><span data-stu-id="e91b0-117">The routing table manager compares the new route to the routes that are already in the routing table.</span></span> <span data-ttu-id="e91b0-118">如果下列所有條件都成立，則兩個路由會相等：</span><span class="sxs-lookup"><span data-stu-id="e91b0-118">Two routes are equal if all of the following conditions are true:</span></span>

    -   <span data-ttu-id="e91b0-119">正在將路由加入至相同的目的地。</span><span class="sxs-lookup"><span data-stu-id="e91b0-119">The route is being added to the same destination.</span></span>
    -   <span data-ttu-id="e91b0-120">此路由是由 [**RTM \_ 路由 \_ 資訊**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info)結構的 **Owner** 成員所指定的相同用戶端所加入。</span><span class="sxs-lookup"><span data-stu-id="e91b0-120">The route is being added by the same client as specified by the **Owner** member of the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure.</span></span>
    -   <span data-ttu-id="e91b0-121">此路由是由 [**RTM \_ 路由 \_ 資訊**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info)結構的 **相鄰** 成員所指定的相同鄰近節點所通告。</span><span class="sxs-lookup"><span data-stu-id="e91b0-121">The route is advertised by the same neighbor as specified by the **Neighbor** member of the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure.</span></span>

    <span data-ttu-id="e91b0-122">如果路由存在，路由表管理員會將控制碼傳回到現有的路由。</span><span class="sxs-lookup"><span data-stu-id="e91b0-122">If the route exists, the routing table manager returns the handle to the existing route.</span></span> <span data-ttu-id="e91b0-123">否則，路由表管理員會新增路由，並將控制碼傳回到新的路由。</span><span class="sxs-lookup"><span data-stu-id="e91b0-123">Otherwise, the routing table manager adds the route and returns the handle to the new route.</span></span>

    <span data-ttu-id="e91b0-124">用戶端可以將 *變更 \_ 旗標* 參數設定為 RTM \_ ROUTE \_ Change \_ NEW，以指示路由表管理員在目的地上新增路由，即使有另一個具有相同擁有者和鄰近欄位的路由存在也一樣。</span><span class="sxs-lookup"><span data-stu-id="e91b0-124">The client can set the *Change\_Flags* parameter to RTM\_ROUTE\_CHANGE\_NEW to instruct the routing table manager to add a new route on the destination, even if another route with the same owner and neighbor fields exists.</span></span>

    <span data-ttu-id="e91b0-125">用戶端可以先將 *變更 \_ 旗標* 參數設定為 RTM \_ 路由 \_ 變更 \_ ，告知路由表管理員更新用戶端所擁有之目的地的第一個路由。</span><span class="sxs-lookup"><span data-stu-id="e91b0-125">The client can set the *Change\_Flags* parameter to RTM\_ROUTE\_CHANGE\_FIRST to tell the routing table manager to update the first route on the destination owned by the client.</span></span> <span data-ttu-id="e91b0-126">如果這類路由存在，即使鄰近欄位不相符，也可以執行這項更新。</span><span class="sxs-lookup"><span data-stu-id="e91b0-126">This update can be performed if such a route exists, even if the neighbor field does not match.</span></span> <span data-ttu-id="e91b0-127">此旗標會由用戶端使用，這些用戶端會維護每個目的地的單一路由。</span><span class="sxs-lookup"><span data-stu-id="e91b0-127">This flag is used by clients that maintain a single route per destination.</span></span>

<span data-ttu-id="e91b0-128">**若要更新路由，用戶端應該採取下列步驟：**</span><span class="sxs-lookup"><span data-stu-id="e91b0-128">**To update a route, the client should take the following steps**</span></span>

1.  <span data-ttu-id="e91b0-129">使用路由的控制碼來呼叫 [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) 。</span><span class="sxs-lookup"><span data-stu-id="e91b0-129">Call [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) with the handle to the route.</span></span> <span data-ttu-id="e91b0-130">控制碼是用戶端先前快取的控制碼，或是由路由表管理員從傳回路由控制碼（例如 **RtmGetRouteInfo**）的呼叫傳回。</span><span class="sxs-lookup"><span data-stu-id="e91b0-130">The handle is either one previously cached by the client, or returned by the routing table manager from a call that returns a route handle such as **RtmGetRouteInfo**.</span></span>
2.  <span data-ttu-id="e91b0-131">進行路由表管理員所傳回之 [**RTM \_ 路由 \_ 資訊**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) 結構的變更。</span><span class="sxs-lookup"><span data-stu-id="e91b0-131">Make the changes to the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure that is returned by the routing table manager.</span></span>
3.  <span data-ttu-id="e91b0-132">使用路由的控制碼和已變更的 [**RTM \_ 路由 \_ 資訊**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info)結構來呼叫 [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) 。</span><span class="sxs-lookup"><span data-stu-id="e91b0-132">Call [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) with the handle to the route and the changed [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure.</span></span>

<span data-ttu-id="e91b0-133">下列範例程式碼示範如何使用路由表管理員作為媒介，將路由新增至目的地。</span><span class="sxs-lookup"><span data-stu-id="e91b0-133">The following sample code shows how to add a route to a destination using the routing table manager as an intermediary.</span></span>


```C++
// Add a route to a destination given by (addr, masklen)
// using a next hop reachable with an interface

RTM_NEXTHOP_INFO NextHopInfo;

// First, create and add a next hop to the caller's
// next-hop tree (if it does not already exist)

ZeroMemory(&NextHopInfo, sizeof(RTM_NEXTHOP_INFO);

RTM_IPV4_MAKE_NET_ADDRESS(&NextHopInfo.NextHopAddress,
                          nexthop, // Address of the next hop
                          32);

NextHopInfo.InterfaceIndex = interface;

NextHopHandle = NULL;

Status = RtmAddNextHop(RtmRegHandle,
                       &NextHopInfo,
                       &NextHopHandle,
                       &ChangeFlags);

if (Status == NO_ERROR)
{
    // Created a new next hop or found an old one

        // Fill in the route information for the route
    
    ZeroMemory(&RouteInfo, sizeof(RTM_ROUTE_INFO);

    // Fill in the destination network's address and mask values
    RTM_IPV4_MAKE_NET_ADDRESS(&NetAddress, addr, masklen);

    // Assume 'neighbour learnt from' is the first next hop
    RouteInfo.Neighbour = NextHopHandle;

    // Set metric for route; Preference set internally
    RouteInfo.PrefInfo.Metric = metric;

    // Adding a route to both the unicast and multicast views
    RouteInfo.BelongsToViews = RTM_VIEW_MASK_UCAST|RTM_VIEW_MASK_MCAST;

    RouteInfo.NextHopsList.NumNextHops = 1;
    RouteInfo.NextHopsList.NextHops[0] = NextHopHandle;

    // If you want to add a new route, regardless of
    // whether a similar route already exists, use the following 
    //     ChangeFlags = RTM_ROUTE_CHANGE_NEW;

    ChangeFlags = 0;

    Status = RtmAddRouteToDest(RtmRegHandle,
                               &RouteHandle,     // Can be NULL if you do not need handle
                               &NetAddress,
                               &RouteInfo,
                               1000,             // Time out route after 1000 ms
                               RouteListHandle1, // Also add the route to this list
                               0,
                               NULL,
                               &ChangeFlags);

    if (Status == NO_ERROR)
    {
        if (ChangeFlags & RTM_ROUTE_CHANGE_NEW)
        {
        ; // A new route has been created
        }
        else
        {
        ; // An existing route is updated
        }

        if (ChangeFlags & RTM_ROUTE_CHANGE_BEST)
        {
        ; // Best route information has changed
        }

        // Release the route handle if you do not need it
        RtmReleaseRoutes(RtmRegHandle, 1, &RouteHandle);
    }

    // Also release the next hop since it is no longer needed 
    RtmReleaseNextHops(RtmRegHandle, 1, &NextHopHandle);
}
```



 

 




