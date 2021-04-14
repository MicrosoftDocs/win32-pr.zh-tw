---
title: 搜尋最佳路線
description: 下列範例程式碼顯示如何在路由表中搜尋最佳路由。
ms.assetid: 559459e9-8446-4f37-8123-7d01f8ed427b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d56330ccc88904a173ae116ddd5513cd9c13d99a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371924"
---
# <a name="search-for-the-best-route"></a><span data-ttu-id="79aee-103">搜尋最佳路線</span><span class="sxs-lookup"><span data-stu-id="79aee-103">Search For the Best Route</span></span>

<span data-ttu-id="79aee-104">下列範例程式碼顯示如何在路由表中搜尋最佳路由。</span><span class="sxs-lookup"><span data-stu-id="79aee-104">The following sample code shows how to search the routing table for the best route.</span></span>


```C++
// Search for a best matching route to a network 
// given (address,mask) for this destination network

// First get the best matching destination

RTM_IPV4_SET_ADDR_AND_MASK(NetAddress, Addr, Mask);

Status = RtmGetMostSpecificDestination(RtmRegHandle,
                                       &NetAddress,
                                       RTM_BEST_PROTOCOL,   // Determines which route information is returned.
                                       RTM_VIEW_MASK_UCAST, // Give the information for the best unicast route
                                       DestInfo);
if (Status == NO_ERROR)
{
    ASSERT(DestInfo->ViewInfo[0].ViewId == RTM_VIEW_ID_UCAST);

    // Get the best unicast route for the destination
    NewBestRoute = DestInfo.ViewInfo[0].Route;

    // Call RtmGetRouteInfo using the handle for information
    //...

    // Release information from RtmGetMostSpecificDestination
    RtmReleaseDestInfo(RtmRegHandle, DestInfo);
}

// To search for an exact match, use RtmGetExactMatchDestionation
```



 

 




