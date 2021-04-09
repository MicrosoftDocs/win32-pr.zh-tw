---
title: 列舉所有目的地
description: 下列範例程式碼顯示如何列舉路由表中的所有目的地。
ms.assetid: 0dced1f8-5dc3-4233-aeb9-35c81c34b345
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c2e202c1dec9c55aeeef6cead7cf0984d2beae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021502"
---
# <a name="enumerate-all-destinations"></a><span data-ttu-id="05e04-103">列舉所有目的地</span><span class="sxs-lookup"><span data-stu-id="05e04-103">Enumerate All Destinations</span></span>

<span data-ttu-id="05e04-104">下列範例程式碼顯示如何列舉路由表中的所有目的地。</span><span class="sxs-lookup"><span data-stu-id="05e04-104">The following sample code shows how to enumerate all destinations in the routing table.</span></span>


```C++
#include <windows.h>


#define ALLOC_RTM_DEST_INFO(NumViews, NumInfos) (PRTM_DEST_INFO) _alloca(RTM_SIZE_OF_DEST_INFO(NumViews) * NumInfos)

void main()
{
    // Macro to allocate a RTM_DEST_INFO on the stack

    // Code to enumerate destinations in the table
    MaxHandles = RegnProfile.MaxHandlesInEnum;
    DestInfos = ALLOC_RTM_DEST_INFO(NumViews, MaxHandles);
    DestInfoSize = RTM_SIZE_OF_DEST_INFO(NumViews);

    // Enumerate all destinations in the subtree (0 / 0)
    // (basically the whole tree; you can
    // also achieve this by using RTM_ENUM_START)
    RTM_IPV4_MAKE_NET_ADDRESS(&NetAddress,0x00000000,0);

    Status = RtmCreateDestEnum(RtmRegHandle, RTM_VIEW_MASK_UCAST | RTM_VIEW_MASK_MCAST, RTM_ENUM_RANGE, &NetAddress, RTM_BEST_PROTOCOL, &EnumHandle1);
    if (Status == NO_ERROR)
    {
        do {
            NumInfos = MaxHandles;
            Status = RtmGetEnumDests(RtmRegHandle, EnumHandle1, &NumInfos, DestInfos);
            for (i = 0; i < NumInfos; i++)
            {
                DestInfo = (PRTM_DEST_INFO) ((PUCHAR)DestInfos+(i*DestInfoSize));

                // Process the current destination information
                ASSERT(DestInfo->ViewInfo[0].ViewId == RTM_VIEW_ID_UCAST);
                BestUnicastRoute = DestInfo->ViewInfo[0].Route;

                // Advertise the best unicast route for the destination
                ...

                // You can enumerate all routes for a destination by
                // creating a route enumeration using
                // RtmCreateRouteEnum ( .. DestInfo->DestHandle .. );
            }
            RtmReleaseDests(RtmRegHandle, NumInfos, DestInfos);

        } while (Status == NO_ERROR)

        // Close the enumeration and release its resources
        RtmDeleteEnumHandle(RtmRegHandle, EnumHandle1);
    }
}
```



 

 




