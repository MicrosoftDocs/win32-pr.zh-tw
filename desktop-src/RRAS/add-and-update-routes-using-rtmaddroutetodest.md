---
title: 使用 RtmAddRouteToDest 新增和更新路由
description: 函數 RtmAddRouteToDest 可用來加入新的路由，並更新目的地的現有路由。 下列程式說明這兩種情況。 下列範例程式碼顯示如何執行第一個程式。
ms.assetid: 17a04511-69f8-4e50-993c-0e558ee72184
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64032aa5f73019e08bb82405d85ffa5ef85abd0526cf7748ec8881b97ab900e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030598"
---
# <a name="add-and-update-routes-using-rtmaddroutetodest"></a>使用 RtmAddRouteToDest 新增和更新路由

函數 [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) 可用來加入新的路由，並更新目的地的現有路由。 下列程式說明這兩種情況。 下列範例程式碼顯示如何執行第一個程式。

**若要新增路由，用戶端應該採取下列步驟：**

1.  如果用戶端已經快取下一個躍點控制碼，請移至步驟4。
2.  建立 [**RTM \_ NEXTHOP \_ 資訊**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) 結構，並填入適當的資訊。
3.  藉由呼叫 [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop)，將下一個躍點新增至路由表。 路由表管理員會將控制碼傳回到下一個躍點。 如果下一個躍點已經存在，則路由表不會新增下一個躍點;相反地，它會將控制碼傳回至下一個躍點。
4.  建立 [**RTM \_ 路由 \_ 資訊**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) 結構並填入適當的資訊，包括路由表管理員所傳回的下個躍點控制碼。
5.  藉由呼叫 [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest)，將路由新增至路由表。 路由表管理員會將新路由與已經在路由表中的路由進行比較。 如果下列所有條件都成立，則兩個路由會相等：

    -   正在將路由加入至相同的目的地。
    -   此路由是由 [**RTM \_ 路由 \_ 資訊**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info)結構的 **Owner** 成員所指定的相同用戶端所加入。
    -   此路由是由 [**RTM \_ 路由 \_ 資訊**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info)結構的 **相鄰** 成員所指定的相同鄰近節點所通告。

    如果路由存在，路由表管理員會將控制碼傳回到現有的路由。 否則，路由表管理員會新增路由，並將控制碼傳回到新的路由。

    用戶端可以將 *變更 \_ 旗標* 參數設定為 RTM \_ ROUTE \_ Change \_ NEW，以指示路由表管理員在目的地上新增路由，即使有另一個具有相同擁有者和鄰近欄位的路由存在也一樣。

    用戶端可以先將 *變更 \_ 旗標* 參數設定為 RTM \_ 路由 \_ 變更 \_ ，告知路由表管理員更新用戶端所擁有之目的地的第一個路由。 如果這類路由存在，即使鄰近欄位不相符，也可以執行這項更新。 此旗標會由用戶端使用，這些用戶端會維護每個目的地的單一路由。

**若要更新路由，用戶端應該採取下列步驟：**

1.  使用路由的控制碼來呼叫 [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) 。 控制碼是用戶端先前快取的控制碼，或是由路由表管理員從傳回路由控制碼（例如 **RtmGetRouteInfo**）的呼叫傳回。
2.  進行路由表管理員所傳回之 [**RTM \_ 路由 \_ 資訊**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) 結構的變更。
3.  使用路由的控制碼和已變更的 [**RTM \_ 路由 \_ 資訊**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info)結構來呼叫 [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) 。

下列範例程式碼示範如何使用路由表管理員作為媒介，將路由新增至目的地。


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



 

 




