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
# <a name="use-a-client-specific-route-list"></a>使用 Client-Specific 路由清單

下列程式概述使用用戶端特定路由清單的步驟。 下列範例程式碼顯示如何執行程式。

**若要使用這項功能，用戶端應該採取下列步驟：**

1.  呼叫 [**RtmCreateRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelist) 以從路由表管理員取得控制碼。
2.  只要用戶端必須在此清單中新增路由，就會呼叫 [**RtmInsertInRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminsertinroutelist) 。
3.  當用戶端不再需要此清單時，它應該呼叫 [**RtmDeleteRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutelist) 來移除清單。

**如果用戶端必須列舉清單上的路由，用戶端應該採取下列步驟：**

1.  呼叫 [**RtmCreateRouteListEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelistenum) 以從路由表管理員取得列舉控制碼。
2.  呼叫 [**RtmGetListEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlistenumroutes) 以取得清單中路由的控制碼。
3.  當不再需要時，請呼叫 [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) 來釋放控制碼。

下列範例程式碼示範如何建立和使用用戶端特定的路由清單。


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



 

 




