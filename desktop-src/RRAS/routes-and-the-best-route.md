---
title: 路由和最佳路由
description: 路由是 \ 0034; 網路路徑 \ 0034;目的地與特定成本相關聯的目的地。 成本是以其系統管理喜好設定和其通訊協定特定度量來表示。 成本較低的路由優先于所有其他路由。
ms.assetid: c5a75308-42da-4ef9-a712-9987c87eef84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afd55ec1188383f4cdef55511aae7a9c2cf59303
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968260"
---
# <a name="routes-and-the-best-route"></a><span data-ttu-id="4c22a-105">路由和最佳路由</span><span class="sxs-lookup"><span data-stu-id="4c22a-105">Routes and the Best Route</span></span>

<span data-ttu-id="4c22a-106">路由是目的地的「網路路徑」，具有與它相關聯的特定成本。</span><span class="sxs-lookup"><span data-stu-id="4c22a-106">A route is a "network path" to a destination that has a certain cost associated with it.</span></span> <span data-ttu-id="4c22a-107">成本是以其系統管理喜好設定和其通訊協定特定度量來表示。</span><span class="sxs-lookup"><span data-stu-id="4c22a-107">The cost is represented by its administrative preference and its protocol-specific metric.</span></span> <span data-ttu-id="4c22a-108">成本較低的路由優先于所有其他路由。</span><span class="sxs-lookup"><span data-stu-id="4c22a-108">Routes with lower costs are preferred over all other routes.</span></span>

<span data-ttu-id="4c22a-109">路由表中的路由專案包括：</span><span class="sxs-lookup"><span data-stu-id="4c22a-109">A route entry in the routing table includes:</span></span>

-   <span data-ttu-id="4c22a-110">目的地的控制碼</span><span class="sxs-lookup"><span data-stu-id="4c22a-110">A handle to the destination</span></span>
-   <span data-ttu-id="4c22a-111">此路由的擁有者</span><span class="sxs-lookup"><span data-stu-id="4c22a-111">The owner of this route</span></span>
-   <span data-ttu-id="4c22a-112">提供路由資訊的鄰近 (對等) </span><span class="sxs-lookup"><span data-stu-id="4c22a-112">The neighbor (peer) that provided the route information</span></span>
-   <span data-ttu-id="4c22a-113">與路由狀態相關聯的旗標</span><span class="sxs-lookup"><span data-stu-id="4c22a-113">Flags associated with the state of the route</span></span>
-   <span data-ttu-id="4c22a-114">與路由相關聯的旗標</span><span class="sxs-lookup"><span data-stu-id="4c22a-114">Flags associated with the route</span></span>
-   <span data-ttu-id="4c22a-115">路由的喜好設定和度量</span><span class="sxs-lookup"><span data-stu-id="4c22a-115">The preference and metric for the route</span></span>
-   <span data-ttu-id="4c22a-116">路由所屬的視圖清單</span><span class="sxs-lookup"><span data-stu-id="4c22a-116">The list of views to which the route belongs</span></span>
-   <span data-ttu-id="4c22a-117">路由擁有者私用的資訊</span><span class="sxs-lookup"><span data-stu-id="4c22a-117">Information that is private to the owner of the route</span></span>
-   <span data-ttu-id="4c22a-118">用來到達目的地的下一個躍點清單</span><span class="sxs-lookup"><span data-stu-id="4c22a-118">A list of next hops used to reach the destination</span></span>

<span data-ttu-id="4c22a-119">下列值會結合在一起，以唯一的方式識別路由表中的路由：</span><span class="sxs-lookup"><span data-stu-id="4c22a-119">The following values, taken together, uniquely identify a route in the routing table:</span></span>

-   <span data-ttu-id="4c22a-120">目的地網路</span><span class="sxs-lookup"><span data-stu-id="4c22a-120">The destination network</span></span>
-   <span data-ttu-id="4c22a-121">路由的擁有者</span><span class="sxs-lookup"><span data-stu-id="4c22a-121">The owner of the route</span></span>
-   <span data-ttu-id="4c22a-122">提供路由的鄰居</span><span class="sxs-lookup"><span data-stu-id="4c22a-122">The neighbor who supplied the route</span></span>

## <a name="metrics-and-preference"></a><span data-ttu-id="4c22a-123">計量和喜好設定</span><span class="sxs-lookup"><span data-stu-id="4c22a-123">Metrics and Preference</span></span>

<span data-ttu-id="4c22a-124">每個路由都有一個管理喜好設定 (由路由原則) 指定，以及與用戶端相依的度量。</span><span class="sxs-lookup"><span data-stu-id="4c22a-124">Each route has an administrative preference (specified by the routing policy), and a client-dependent metric.</span></span> <span data-ttu-id="4c22a-125">路由表管理員會使用這項資訊來判斷哪個路由是目的地的較佳路由。</span><span class="sxs-lookup"><span data-stu-id="4c22a-125">The routing table manager uses this information to determine which route is the better route to a destination.</span></span> <span data-ttu-id="4c22a-126">較低喜好設定的路由是較佳的路由， (一個較低的路由，因此最適合) 。</span><span class="sxs-lookup"><span data-stu-id="4c22a-126">Routes with lower preference are better routes (one being lowest, and therefore best).</span></span> <span data-ttu-id="4c22a-127">如果兩個路由具有相同的喜好設定，則具有較低計量的路由會是較佳的路由。</span><span class="sxs-lookup"><span data-stu-id="4c22a-127">If two routes have the same preference, the route with the lower metric is the better route.</span></span>

<span data-ttu-id="4c22a-128">一般來說，路由的喜好設定取決於新增路由之用戶端的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="4c22a-128">Normally, the preference of a route is determined by the preference of the client that added the route.</span></span> <span data-ttu-id="4c22a-129">不過，對於使用 Netsh.exe 管理工具新增的任何路由，可以根據每個路由來指定喜好設定值。</span><span class="sxs-lookup"><span data-stu-id="4c22a-129">However, for any routes added using the Netsh.exe management tool, a preference value can be specified on a per-route basis.</span></span>

<span data-ttu-id="4c22a-130">喜好設定通常用來指出用戶端之間的優先順序。</span><span class="sxs-lookup"><span data-stu-id="4c22a-130">Preference is normally used to indicate priority between clients.</span></span> <span data-ttu-id="4c22a-131">例如，系統管理員可以將較低的 () 喜好設定指派為較 RIP 更低的版本。</span><span class="sxs-lookup"><span data-stu-id="4c22a-131">For example, an administrator can assign OSPF a lower (better) preference than RIP.</span></span> <span data-ttu-id="4c22a-132">在此情況下，適用于 RIP 路由的 OSPF 路由比較理想。</span><span class="sxs-lookup"><span data-stu-id="4c22a-132">In this case, OSPF routes are preferable to RIP routes.</span></span>

 

 




