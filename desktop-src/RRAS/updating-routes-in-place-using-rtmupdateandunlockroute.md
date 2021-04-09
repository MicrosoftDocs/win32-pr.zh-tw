---
title: 使用 RtmUpdateAndUnlockRoute 就地更新路由
description: 就地更新通常比以間接方法（例如，RtmAddRouteToDest 函式所使用的）更新路由表更有效率。
ms.assetid: d4b0b14e-957a-43d5-bacc-8eee4512e2ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d76d2af5d60172b890eefa1041a08d47a5221b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021607"
---
# <a name="updating-routes-in-place-using-rtmupdateandunlockroute"></a><span data-ttu-id="d1356-103">使用 RtmUpdateAndUnlockRoute 就地更新路由</span><span class="sxs-lookup"><span data-stu-id="d1356-103">Updating Routes In Place Using RtmUpdateAndUnlockRoute</span></span>

<span data-ttu-id="d1356-104">就地更新通常比以間接方法（例如， [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) 函式所使用的）更新路由表更有效率。</span><span class="sxs-lookup"><span data-stu-id="d1356-104">Updating in place is generally more efficient than updating the routing table with an indirect method such as that used by the [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) function.</span></span> <span data-ttu-id="d1356-105">這個方法更有效率，因為用戶端不需要取得控制碼，也不需要在路由表管理員之間傳遞 [**RTM \_ 路由 \_ 資訊**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) 結構。</span><span class="sxs-lookup"><span data-stu-id="d1356-105">This method is more efficient because the client is not required to obtain a handle, nor to pass the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure to and from the routing table manager.</span></span> <span data-ttu-id="d1356-106">這個方法也會花費較少的時間。</span><span class="sxs-lookup"><span data-stu-id="d1356-106">This method also takes less time.</span></span> <span data-ttu-id="d1356-107">不過，直接更新路由表可能會有風險，因為路由表管理員並不是以媒介的形式運作。</span><span class="sxs-lookup"><span data-stu-id="d1356-107">However, directly updating the routing table can be risky, since the routing table manager is not functioning as an intermediary.</span></span>

<span data-ttu-id="d1356-108">如需示範如何使用這些函數的範例程式碼，請參閱 [使用 RtmUpdateAndUnlockRoute 就地更新路由](update-a-route-in-place-using-rtmupdateandunlockroute.md)。</span><span class="sxs-lookup"><span data-stu-id="d1356-108">For sample code that shows how to use these functions, see [Update a Route In Place Using RtmUpdateAndUnlockRoute](update-a-route-in-place-using-rtmupdateandunlockroute.md).</span></span>

 

 




