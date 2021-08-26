---
title: 使用前置詞樹狀目錄搜尋路由
description: 下列範例程式碼示範如何使用 RtmGetMostSpecificDestination 和 RtmGetLessSpecificDestination 來向上查看路由表中的前置詞樹狀結構。
ms.assetid: 14e8e87f-c76c-48ad-93b5-0d8a711148d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa132946812a5f945c1aca31c1e20518348f3b3140030c631a5f0f9c62b2db19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035598"
---
# <a name="search-for-routes-using-a-prefix-tree"></a>使用前置詞樹狀目錄搜尋路由

下列範例程式碼示範如何使用 [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination) 和 [**RtmGetLessSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination) 來向上查看路由表中的前置詞樹狀結構。


```C++
// Used to walk up the prefix tree, given the destination and mask

// Search for a best matching route to a network
// given (address,mask) for this destination network

// First get the best matching destination

RTM_IPV4_SET_ADDR_AND_MASK(NetAddress, Addr, Mask);

Status = RtmGetMostSpecificDestination(RtmRegHandle,
                                       &NetAddress,
                                       RTM_BEST_PROTOCOL,   // Determines which route information is returned.
                                       RTM_VIEW_MASK_UCAST, // Give the information for best unicast route
                                       DestInfo1);
// Use RtmGetLessSpecificDestination to go up the
// tree until it returns ERROR_NOT_FOUND. Use two
// RTM_DEST_INFO buffers - DestInfo1 & DestInfo2
// alternately to avoid all unnecessary copying.

while (Status == NO_ERROR)
{
    if (DestInfo1->DestAddress.NumBits == NetAddress.NumBits)
    {
        Print("Exact Match of Destination\n");
    }

    Status = RtmGetLessSpecificDestination(RtmRegHandle,
                                           DestInfo1->DestHandle,
                                           RTM_BEST_PROTOCOL,
                                           RTM_VIEW_MASK_UCAST,
                                           DestInfo2);

    // NOTE that the buffer is DestInfo1 and not DestInfo2
    RtmReleaseDestInfo(RtmRegHandle, DestInfo1);

    if (Status != NO_ERROR) 
    {
        break;
    }
    
    // Use any information you want in DestInfo2
    Print("Mask Len: %d\n", DestInfo2->DestAddress.NumBits);

    Status = RtmGetLessSpecificDestination(RtmRegHandle,
                                           DestInfo2->DestHandle,
                                           RTM_BEST_PROTOCOL,
                                           RTM_VIEW_MASK_UCAST,
                                           DestInfo1);

    // NOTE that the buffer is DestInfo2 and not DestInfo1
    RtmReleaseDestInfo(RtmRegHandle, DestInfo2);

    if (Status != NO_ERROR) 
    {
        break;
    }

    // Use any information you want in DestInfo1
    Print("Mask Len: %d\n", DestInfo1->DestAddress.NumBits);
}
```



 

 




