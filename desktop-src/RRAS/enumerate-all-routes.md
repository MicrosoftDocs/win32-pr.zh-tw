---
title: 列舉所有路由
description: 下列程式概述用來列舉 RTMv2 API 所使用之任何實體的步驟。 下列範例程式碼顯示如何列舉所有路由。
ms.assetid: 78a50e4a-f3c7-4a0d-a528-18d35b66369d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c927665cab8d4db492d3a2c5f8e9363fc1fe7be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673760"
---
# <a name="enumerate-all-routes"></a>列舉所有路由

下列程式概述用來列舉 RTMv2 API 所使用之任何實體的步驟。 下列範例程式碼顯示如何列舉所有路由。

**每個列舉的基本進程如下所示**

1.  從路由表管理員取得控制碼，以啟動列舉。 呼叫 [**RtmCreateDestEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatedestenum)、 [**RtmCreateRouteEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreaterouteenum) 和 [**RtmCreateNextHopEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatenexthopenum) ，以提供指定要列舉之資訊類型的準則。 此準則包含但不限於某範圍的目的地、特定介面，以及資訊所在的視圖。
2.  呼叫 [**RtmGetEnumDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumdests)、 [**RtmGetEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumroutes) 和 [**RtmGetEnumNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumnexthops) 一或多次來取出資料，直到路由表管理員傳回錯誤 \_ \_ \_ 的專案為止。 路由、目的地和下個躍點資料會依位址資訊 (和喜好設定和計量值的順序傳回，如果路由是) 列舉。
3.  當不再需要與列舉相關聯的控制碼或資訊結構時，呼叫 [**RtmReleaseDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests)、 [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) 和 [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) 。
4.  呼叫 [**RtmDeleteEnumHandle**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteenumhandle) ，釋放建立列舉時所傳回的列舉控制碼。 此函數是用來釋出所有列舉類型的控制碼。

> [!Note]  
> 只有在用戶端使用 RTM 視圖遮罩的所有視圖要求資料時，才會列舉處於保留狀態的 \_ 路由 \_ \_ 。

 

下列範例程式碼顯示如何列舉路由表中的所有路由。


```C++
MaxHandles = RegnProfile.MaxHandlesInEnum;

RouteHandles = _alloca(MaxHandles * sizeof(HANDLE));

// Do a "route enumeration" over the whole table
// by passing a NULL DestHandle in this function.

DestHandle = NULL; // Give a valid handle to enumerate over a particular destination

Status = RtmCreateRouteEnum(RtmRegHandle,
                            DestHandle,
                            RTM_VIEW_MASK_UCAST|RTM_VIEW_MASK_MCAST,
                            RTM_ENUM_OWN_ROUTES, // Get only your own routes
                            NULL,
                            0,
                            NULL,
                            0,
                            &EnumHandle2);
if (Status == NO_ERROR)
{
    do
    {
        NumHandles = MaxHandles;

        Status = RtmGetEnumRoutes(RtmRegHandle
                                  EnumHandle2,
                                  &NumHandles,
                                  RouteHandles);

        for (k = 0; k < NumHandles; k++)
        {
            wprintf("Route %d: %p\n", l++, RouteHandles[k]);

            // Get route information using the route's handle
            Status = RtmGetRouteInfo(...RouteHandles[k]...);

            if (Status == NO_ERROR)
            {
                // Do whatever you want with the route info
                //...

                // Release the route information once you are done
                RtmReleaseRouteInfo(...);
            }
        }

        RtmReleaseRoutes(RtmRegHandle, NumHandles, RouteHandles);
    }
    while (Status == NO_ERROR)

    // Close the enumeration and release its resources
    RtmDeleteEnumHandle(RtmRegHandle, EnumHandle2);
}
```



 

 




