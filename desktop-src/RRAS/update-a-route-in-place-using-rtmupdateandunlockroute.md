---
title: 使用 RtmUpdateAndUnlockRoute 就地更新路由
description: 下列程式概述用來就地更新路由的步驟。 下列範例程式碼顯示如何執行程式。
ms.assetid: 3598a28f-8ade-4b3f-9d31-4f2c84df2dd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb79b86645d77f0ee44ffd06b8ef6f403dbd8ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372357"
---
# <a name="update-a-route-in-place-using-rtmupdateandunlockroute"></a><span data-ttu-id="209dd-104">使用 RtmUpdateAndUnlockRoute 就地更新路由</span><span class="sxs-lookup"><span data-stu-id="209dd-104">Update a Route In Place Using RtmUpdateAndUnlockRoute</span></span>

<span data-ttu-id="209dd-105">下列程式概述用來就地更新路由的步驟。</span><span class="sxs-lookup"><span data-stu-id="209dd-105">The following procedure outlines the steps used to update a route in place.</span></span> <span data-ttu-id="209dd-106">下列範例程式碼顯示如何執行程式。</span><span class="sxs-lookup"><span data-stu-id="209dd-106">The sample code that follows shows how to implement the procedure.</span></span>

<span data-ttu-id="209dd-107">**若要就地更新路由，用戶端應採取下列步驟**</span><span class="sxs-lookup"><span data-stu-id="209dd-107">**To update a route in place, the client should take the following steps**</span></span>

1.  <span data-ttu-id="209dd-108">藉由呼叫 [**RtmLockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockroute)來鎖定路由。</span><span class="sxs-lookup"><span data-stu-id="209dd-108">Lock the route by calling [**RtmLockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockroute).</span></span> <span data-ttu-id="209dd-109">目前，此函式會實際鎖定路由的目的地。</span><span class="sxs-lookup"><span data-stu-id="209dd-109">Currently, this function actually locks the route's destination.</span></span> <span data-ttu-id="209dd-110">路由表管理員會傳回路由的指標。</span><span class="sxs-lookup"><span data-stu-id="209dd-110">The routing table manager returns a pointer to the route.</span></span>
2.  <span data-ttu-id="209dd-111">使用路由表管理員的 [**RTM \_ 路由 \_ 資訊**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) 結構（在步驟1中取得）的指標，對路由進行必要的變更。</span><span class="sxs-lookup"><span data-stu-id="209dd-111">Use the pointer to the routing table manager's [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure, obtained in step 1, to make the necessary changes to the route.</span></span> <span data-ttu-id="209dd-112">就地更新時，只有 **RTM \_ 路由 \_ 資訊** 結構的特定成員可以修改。</span><span class="sxs-lookup"><span data-stu-id="209dd-112">Only certain members of the **RTM\_ROUTE\_INFO** structure can be modified when updating in place.</span></span> <span data-ttu-id="209dd-113">這些成員包括： **Neighbour**、 **PrefInfo**、 **EntitySpecificInfo**、 **BelongsToViews** 和 **NextHopsList**。</span><span class="sxs-lookup"><span data-stu-id="209dd-113">These members are: **Neighbour**, **PrefInfo**, **EntitySpecificInfo**, **BelongsToViews**, and **NextHopsList**.</span></span>
    > [!Note]  
    > <span data-ttu-id="209dd-114">如果用戶端將資訊新增至 **Neighbour** 或 **NextHopsList** 成員，用戶端必須呼叫 [**RtmReferenceHandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) ，以明確遞增路由表管理員在下一個躍點物件上保留的參考計數。</span><span class="sxs-lookup"><span data-stu-id="209dd-114">If the client adds information to either the **Neighbour** or **NextHopsList** members, the client must call [**RtmReferenceHandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) to explicitly increment the reference count that the routing table manager keeps on the next-hop object.</span></span> <span data-ttu-id="209dd-115">同樣地，如果用戶端移除 **NextHopsList** 成員的資訊，則用戶端必須呼叫 [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) 來遞減參考計數。</span><span class="sxs-lookup"><span data-stu-id="209dd-115">Similarly, if the client removes information from the **NextHopsList** member, the client must call [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) to decrement the reference count.</span></span>

     

3.  <span data-ttu-id="209dd-116">呼叫 [**RtmUpdateAndUnlockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmupdateandunlockroute) 以通知路由表管理員已發生變更。</span><span class="sxs-lookup"><span data-stu-id="209dd-116">Call [**RtmUpdateAndUnlockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmupdateandunlockroute) to notify the routing table manager that a change has taken place.</span></span> <span data-ttu-id="209dd-117">路由表管理員會認可變更、更新目的地以反映新的資訊，然後將路由解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="209dd-117">The routing table manager commits the changes, updates the destination to reflect the new information, and then unlocks the route.</span></span>

<span data-ttu-id="209dd-118">下列範例程式碼顯示如何使用路由表中實際路由資訊的指標，直接更新路由。</span><span class="sxs-lookup"><span data-stu-id="209dd-118">The following sample code shows how to update a route directly, using a pointer to the actual route information in the routing table.</span></span>


```C++
Status = RtmLockRoute(RtmRegHandle,
                      RouteHandle,
                      TRUE,
                      TRUE,
                      &RoutePointer);

if (Status == NO_ERROR)
{
        // Update route parameters in place (i.e., directly on 
// the routing table manager's copy)
    
    // Update the metric and views of the route
    RoutePointer->PrefInfo.Metric = 16;

    // Change the views so that the route belongs to only the multicast view
    RoutePointer->BelongsToViews = RTM_VIEW_MASK_MCAST;

    // Set the entity-specific information to X
    RoutePointer->EntitySpecificInfo = X;

    // Note that the following manipulation of
    // next-hop references is not needed when
    // using RtmAddRouteToDest, as it is done
    // by the routing table manager automatically
    
    // Change next hop from NextHop1 to NextHop2
    NextHop1 = RoutePointer->NextHopsList.NextHop[0];

    // Explicitly dereference the old next hop
    RtmReleaseNextHops(RtmRegHandle, 1, &NextHop1);

    RoutePointer->NextHopsList.NextHop[0] = NextHop2;

    // Explicitly reference next hop being added
    RtmReferenceHandles(RtmRegHandle, 1, &NextHop2);

    // Call the routing table manager to indicate that route information
    // has changed, and that its position might
    // have to be rearranged and the corresponding destination
    // needs to be updated to reflect this change.
    
    Status = RtmUpdateAndUnlockRoute(RtmRegHandle,
                                     RouteHandle,
                                     INFINITE, // Keep forever
                                     NULL,
                                     0,
                                     NULL,
                                     &ChangeFlags);
    ASSERT(Status == NO_ERROR);
}
```



 

 




