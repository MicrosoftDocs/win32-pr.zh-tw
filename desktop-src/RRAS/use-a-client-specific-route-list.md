---
title: 使用 Client-Specific 路由清單
description: 下列程式概述使用用戶端特定路由清單的步驟。 下列範例程式碼顯示如何執行程式。
ms.assetid: aa9b7b2a-259f-4ce1-afb6-c04875e8ffe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77cfa893bda9e850527c7ebe35590dbe2d08a490
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969068"
---
# <a name="use-a-client-specific-route-list"></a><span data-ttu-id="0a59f-104">使用 Client-Specific 路由清單</span><span class="sxs-lookup"><span data-stu-id="0a59f-104">Use a Client-Specific Route List</span></span>

<span data-ttu-id="0a59f-105">下列程式概述使用用戶端特定路由清單的步驟。</span><span class="sxs-lookup"><span data-stu-id="0a59f-105">The following procedures outlines the steps to use the client-specific route lists.</span></span> <span data-ttu-id="0a59f-106">下列範例程式碼顯示如何執行程式。</span><span class="sxs-lookup"><span data-stu-id="0a59f-106">The sample code that follows shows how to implement the procedure.</span></span>

<span data-ttu-id="0a59f-107">**若要使用這項功能，用戶端應該採取下列步驟：**</span><span class="sxs-lookup"><span data-stu-id="0a59f-107">**To use this feature, a client should take the following steps**</span></span>

1.  <span data-ttu-id="0a59f-108">呼叫 [**RtmCreateRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelist) 以從路由表管理員取得控制碼。</span><span class="sxs-lookup"><span data-stu-id="0a59f-108">Call [**RtmCreateRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelist) to obtain a handle from the routing table manager.</span></span>
2.  <span data-ttu-id="0a59f-109">只要用戶端必須在此清單中新增路由，就會呼叫 [**RtmInsertInRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminsertinroutelist) 。</span><span class="sxs-lookup"><span data-stu-id="0a59f-109">Call [**RtmInsertInRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminsertinroutelist) whenever the client must add a route to this list.</span></span>
3.  <span data-ttu-id="0a59f-110">當用戶端不再需要此清單時，它應該呼叫 [**RtmDeleteRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutelist) 來移除清單。</span><span class="sxs-lookup"><span data-stu-id="0a59f-110">When the client no longer requires the list, it should call [**RtmDeleteRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutelist) to remove the list.</span></span>

<span data-ttu-id="0a59f-111">**如果用戶端必須列舉清單上的路由，用戶端應該採取下列步驟：**</span><span class="sxs-lookup"><span data-stu-id="0a59f-111">**If the client must enumerate the routes on the list, the client should take the following steps**</span></span>

1.  <span data-ttu-id="0a59f-112">呼叫 [**RtmCreateRouteListEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelistenum) 以從路由表管理員取得列舉控制碼。</span><span class="sxs-lookup"><span data-stu-id="0a59f-112">Call [**RtmCreateRouteListEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelistenum) to obtain an enumeration handle from the routing table manager.</span></span>
2.  <span data-ttu-id="0a59f-113">呼叫 [**RtmGetListEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlistenumroutes) 以取得清單中路由的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0a59f-113">Call [**RtmGetListEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlistenumroutes) to obtain the handles to the routes in the list.</span></span>
3.  <span data-ttu-id="0a59f-114">當不再需要時，請呼叫 [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) 來釋放控制碼。</span><span class="sxs-lookup"><span data-stu-id="0a59f-114">Call [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) to release the handles when no longer required.</span></span>

<span data-ttu-id="0a59f-115">下列範例程式碼示範如何建立和使用用戶端特定的路由清單。</span><span class="sxs-lookup"><span data-stu-id="0a59f-115">The following sample code shows how to create and use a client-specific route list.</span></span>


```C++
HANDLE RouteListHandle1;
HANDLE RouteListHandle2;

// Create two entity-specific lists to add routes to

Status = RtmCreateRouteList(RtmRegHandle,
                            &RouteListHandle1);
// Check Status
//...

Status = RtmCreateRouteList(RtmRegHandle,
                            &RouteListHandle2);
// Check Status
//...

// Assume you have added a bunch of routes
// by calling RtmAddRouteToDest many times
// with 'RouteListHandle1' specified similar to
// Status = RtmAddRouteToDest(RtmRegHandle,
//                            ...
//                            RouteListHandle1,
//                            ...
//                            &ChangeFlags);

// Enumerate routes in RouteListHandle1 list

// Create an enumeration on the route list

Status = RtmCreateRouteListEnum(RtmRegHandle,
                                RouteListHandle1,
                                &EnumHandle);

if (Status == NO_ERROR)
{
        // Allocate space on the top of the stack
        
    MaxHandles = RegnProfile.MaxHandlesInEnum;

    RouteHandles = _alloca(MaxHandles * sizeof(HANDLE));

    // Note how the termination condition is different
    // from other enumerations - the call to the function
    // RtmGetListEnumRoutes always returns NO_ERROR
    // Quit when you get fewer handles than requested
    
    do
    {
                // Get next set of routes from the list enumeration
        
        NumHandles = MaxHandles;

        Status = RtmGetListEnumRoutes(RtmRegHandle,
                                      EnumHandle,
                                      &NumHandles,
                                      RouteHandles);

        for (i = 0; i < NumHandles; i++)
        {
            Print("Route Handle %5lu: %p\n", i, RouteHandles[i]);
        }

        // Move all these routes to another route list
        // They are automatically removed from the old one
        
        Status = RtmInsertInRouteList(RtmRegHandle,
                                      RouteListHandle2,
                                      NumHandles,
                                      RouteHandles);
        // Check Status...
        
                // Release the routes that have been enumerated
        
        RtmReleaseRoutes(RtmRegHandle, NumHandles, RouteHandles);
    }
    while (NumHandles == MaxHandles);

    RtmDeleteEnumHandle(RtmRegHandle, EnumHandle);
}

// Destroy all the entity-specific route lists 
// after removing all routes from these lists;
// the routes themselves are not deleted

Status = RtmDeleteRouteList(RtmRegHandle, RouteListHandle1);
ASSERT(Status == NO_ERROR);


Status = RtmDeleteRouteList(RtmRegHandle, RouteListHandle2);
ASSERT(Status == NO_ERROR);
```



 

 




