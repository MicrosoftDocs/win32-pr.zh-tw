---
title: 使用 RtmAddRouteToDest 更新路由
description: 如果用戶端在新增路由時不需要效率，則應該使用下列方法來更新路由。
ms.assetid: bfa914ea-5d54-4ce9-a97c-903c497d135b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c7972b2d5ec0996cafc1dd32a8a4056a6aeb0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932493"
---
# <a name="updating-routes-using-rtmaddroutetodest"></a><span data-ttu-id="4517e-103">使用 RtmAddRouteToDest 更新路由</span><span class="sxs-lookup"><span data-stu-id="4517e-103">Updating Routes Using RtmAddRouteToDest</span></span>

<span data-ttu-id="4517e-104">如果用戶端在新增路由時不需要效率，則應該使用下列方法來更新路由。</span><span class="sxs-lookup"><span data-stu-id="4517e-104">If the client does not require efficiency when adding a route, it should use the following method of updating routes.</span></span> <span data-ttu-id="4517e-105">這種方法的效率較低，因為它需要取得路由的控制碼，並將 [**RTM \_ 路由 \_ 資訊**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) 結構傳遞到路由表管理員。</span><span class="sxs-lookup"><span data-stu-id="4517e-105">This method is less efficient since it requires obtaining a handle to the route and passing the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure to and from the routing table manager.</span></span> <span data-ttu-id="4517e-106">此方法也需要更多時間。</span><span class="sxs-lookup"><span data-stu-id="4517e-106">This method also takes more time.</span></span> <span data-ttu-id="4517e-107">由於 [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) 並不會直接操作路由表，因此使用此方法會以簡單的方式來交易效率。</span><span class="sxs-lookup"><span data-stu-id="4517e-107">Since [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) does not manipulate the routing table directly, using this method trades efficiency for simplicity.</span></span>

<span data-ttu-id="4517e-108">如需示範如何使用這些函數的範例程式碼，請參閱 [使用 RtmAddRouteToDest 新增和更新路由](add-and-update-routes-using-rtmaddroutetodest.md)。</span><span class="sxs-lookup"><span data-stu-id="4517e-108">For sample code that shows how to use these functions, see [Add and Update Routes Using RtmAddRouteToDest](add-and-update-routes-using-rtmaddroutetodest.md).</span></span>

 

 




