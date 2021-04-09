---
title: 管理控制碼
description: 路由表管理員會維護它所維護之所有資訊的參考計數。
ms.assetid: bcd02881-b021-414f-8a40-14baac5baac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f24653dd98db9b0427e5a3bee3f2f6613a68ce41
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932308"
---
# <a name="managing-handles"></a><span data-ttu-id="55ff0-103">管理控制碼</span><span class="sxs-lookup"><span data-stu-id="55ff0-103">Managing Handles</span></span>

<span data-ttu-id="55ff0-104">路由表管理員會維護它所維護之所有資訊的參考計數。</span><span class="sxs-lookup"><span data-stu-id="55ff0-104">The routing table manager maintains a reference count for all the information that it maintains.</span></span> <span data-ttu-id="55ff0-105">這可防止路由表管理員將任何已釋放記憶體的控制碼傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="55ff0-105">This prevents the routing table manager from returning to a client any handles to memory that has been freed.</span></span> <span data-ttu-id="55ff0-106">每次將控制碼傳回給呼叫端時，會以明確控制碼或資訊結構的一部分（例如 [**RTM \_ DEST \_ 資訊**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_dest_info)）傳回給呼叫者，對應至控制碼之物件的參考計數會遞增。</span><span class="sxs-lookup"><span data-stu-id="55ff0-106">Each time a handle is returned to the caller, either as an explicit handle or as part of an information structure, such as [**RTM\_DEST\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_dest_info), the reference count for the object that corresponds to the handle is incremented.</span></span> <span data-ttu-id="55ff0-107">釋放控制碼或資訊結構時，會減少適當的參考計數。</span><span class="sxs-lookup"><span data-stu-id="55ff0-107">When the handle or the information structure is released, the appropriate reference count is decremented.</span></span> <span data-ttu-id="55ff0-108">如果參考計數變成零，則會釋放物件。</span><span class="sxs-lookup"><span data-stu-id="55ff0-108">When the reference count becomes zero, the object is freed.</span></span>

<span data-ttu-id="55ff0-109">[**RtmGetDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo)、 [**RtmGetEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo)、 [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo)和 [**RtmGetNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo)函數會傳回信息結構。</span><span class="sxs-lookup"><span data-stu-id="55ff0-109">The [**RtmGetDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo), [**RtmGetEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) and [**RtmGetNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) functions return information structures.</span></span> <span data-ttu-id="55ff0-110">這些函式分別對應至 [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo)、 [**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo)、 [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo) 和 [**RtmRelaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo) 函數。</span><span class="sxs-lookup"><span data-stu-id="55ff0-110">These functions correspond to [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo) and [**RtmRelaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo) functions, respectively.</span></span>

> [!Note]  
> <span data-ttu-id="55ff0-111">[**RtmReleaseChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasechangeddests)函式應該用來釋放呼叫 [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests)所傳回的控制碼。</span><span class="sxs-lookup"><span data-stu-id="55ff0-111">The [**RtmReleaseChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasechangeddests) function should be used to release handles that have been returned by a call to [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests).</span></span> <span data-ttu-id="55ff0-112">請勿針對已變更的目的結構使用 [**RtmReleaseDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests) 。</span><span class="sxs-lookup"><span data-stu-id="55ff0-112">Do not use [**RtmReleaseDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests) for changed destination structures.</span></span>

 

<span data-ttu-id="55ff0-113">如果用戶端必須在釋放其餘部分時，將特定的控制碼保留在資訊結構中，則用戶端可以使用該控制碼呼叫 [**RtmReferenceHandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) ，然後再釋放資訊結構。</span><span class="sxs-lookup"><span data-stu-id="55ff0-113">If a client must keep a specific handle in an information structure while releasing the rest, the client can call [**RtmReferenceHandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) with that handle before releasing the information structure.</span></span> <span data-ttu-id="55ff0-114">然後，您可以呼叫 [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo)、 [**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo)、 [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo) 和 [**RtmRelaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo) 函式來釋放控制碼。</span><span class="sxs-lookup"><span data-stu-id="55ff0-114">The handle can then be released by a call to the [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo) and [**RtmRelaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo) functions.</span></span>

 

 




