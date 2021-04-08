---
title: 路由旗標
description: 路由旗標
ms.assetid: 17deae88-573f-48ec-887e-521549b39c32
keywords:
- 路由
- 路由旗標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1711ef4ed621d55cc00302cca181676a3892c030
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931945"
---
# <a name="route-flags"></a><span data-ttu-id="c7609-105">路由旗標</span><span class="sxs-lookup"><span data-stu-id="c7609-105">Route Flags</span></span>

## <a name="state-of-the-route-constants"></a><span data-ttu-id="c7609-106">路由常數的狀態</span><span class="sxs-lookup"><span data-stu-id="c7609-106">State of the Route Constants</span></span>



| <span data-ttu-id="c7609-107">常數</span><span class="sxs-lookup"><span data-stu-id="c7609-107">Constant</span></span>                    | <span data-ttu-id="c7609-108">值</span><span class="sxs-lookup"><span data-stu-id="c7609-108">Value</span></span> | <span data-ttu-id="c7609-109">描述</span><span class="sxs-lookup"><span data-stu-id="c7609-109">Description</span></span>             |
|-----------------------------|-------|-------------------------|
| <span data-ttu-id="c7609-110">RTM \_ 路由 \_ 狀態已 \_ 建立</span><span class="sxs-lookup"><span data-stu-id="c7609-110">RTM\_ROUTE\_STATE\_CREATED</span></span>  | <span data-ttu-id="c7609-111">0</span><span class="sxs-lookup"><span data-stu-id="c7609-111">0</span></span>     | <span data-ttu-id="c7609-112">已建立路由。</span><span class="sxs-lookup"><span data-stu-id="c7609-112">Route has been created.</span></span> |
| <span data-ttu-id="c7609-113">RTM \_ 路由 \_ 狀態 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="c7609-113">RTM\_ROUTE\_STATE\_DELETING</span></span> | <span data-ttu-id="c7609-114">1</span><span class="sxs-lookup"><span data-stu-id="c7609-114">1</span></span>     | <span data-ttu-id="c7609-115">正在刪除路由。</span><span class="sxs-lookup"><span data-stu-id="c7609-115">Route is being deleted.</span></span> |
| <span data-ttu-id="c7609-116">RTM \_ 路由 \_ 狀態 \_ 已刪除</span><span class="sxs-lookup"><span data-stu-id="c7609-116">RTM\_ROUTE\_STATE\_DELETED</span></span>  | <span data-ttu-id="c7609-117">2</span><span class="sxs-lookup"><span data-stu-id="c7609-117">2</span></span>     | <span data-ttu-id="c7609-118">已刪除路由。</span><span class="sxs-lookup"><span data-stu-id="c7609-118">Route has been deleted.</span></span> |



 

## <a name="route-update-flags"></a><span data-ttu-id="c7609-119">路由更新旗標</span><span class="sxs-lookup"><span data-stu-id="c7609-119">Route Update Flags</span></span>



| <span data-ttu-id="c7609-120">常數</span><span class="sxs-lookup"><span data-stu-id="c7609-120">Constant</span></span>                  | <span data-ttu-id="c7609-121">值</span><span class="sxs-lookup"><span data-stu-id="c7609-121">Value</span></span>      | <span data-ttu-id="c7609-122">描述</span><span class="sxs-lookup"><span data-stu-id="c7609-122">Description</span></span>                                                                                                                                                                                |
|---------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7609-123">RTM \_ 路由 \_ \_ 先變更</span><span class="sxs-lookup"><span data-stu-id="c7609-123">RTM\_ROUTE\_CHANGE\_FIRST</span></span> | <span data-ttu-id="c7609-124">0x01</span><span class="sxs-lookup"><span data-stu-id="c7609-124">0x01</span></span>       | <span data-ttu-id="c7609-125">指出當判斷兩個路由是否相等時，路由表管理員不應該檢查 [**RTM \_ 路由 \_ 資訊**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info)結構的 **Neighbour** 成員。</span><span class="sxs-lookup"><span data-stu-id="c7609-125">Indicates that the routing table manager should not check the **Neighbour** member of the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure when determining when two routes are equal.</span></span> |
| <span data-ttu-id="c7609-126">RTM \_ 路由 \_ 變更 \_ 新增</span><span class="sxs-lookup"><span data-stu-id="c7609-126">RTM\_ROUTE\_CHANGE\_NEW</span></span>   | <span data-ttu-id="c7609-127">0x02</span><span class="sxs-lookup"><span data-stu-id="c7609-127">0x02</span></span>       | <span data-ttu-id="c7609-128">由路由表管理員傳回，表示已建立新的路由。</span><span class="sxs-lookup"><span data-stu-id="c7609-128">Returned by the routing table manager to indicate a new route was created.</span></span>                                                                                                                 |
| <span data-ttu-id="c7609-129">RTM \_ 路由 \_ 變更 \_ 最佳</span><span class="sxs-lookup"><span data-stu-id="c7609-129">RTM\_ROUTE\_CHANGE\_BEST</span></span>  | <span data-ttu-id="c7609-130">0x00010000</span><span class="sxs-lookup"><span data-stu-id="c7609-130">0x00010000</span></span> | <span data-ttu-id="c7609-131">路由表管理員傳回，表示已新增或更新的路由是最佳路由，或由於變更，而導致新的路由成為最佳路由。</span><span class="sxs-lookup"><span data-stu-id="c7609-131">Returned by the routing table manager to indicate that the route that was added or updated was the best route, or that because of the change, a new route became the best route.</span></span>           |



 

## <a name="unicast-flags"></a><span data-ttu-id="c7609-132">單播旗標</span><span class="sxs-lookup"><span data-stu-id="c7609-132">Unicast Flags</span></span>



| <span data-ttu-id="c7609-133">常數</span><span class="sxs-lookup"><span data-stu-id="c7609-133">Constant</span></span>                  | <span data-ttu-id="c7609-134">值</span><span class="sxs-lookup"><span data-stu-id="c7609-134">Value</span></span>  | <span data-ttu-id="c7609-135">描述</span><span class="sxs-lookup"><span data-stu-id="c7609-135">Description</span></span>                                                            |
|---------------------------|--------|------------------------------------------------------------------------|
| <span data-ttu-id="c7609-136">RTM \_ 路由 \_ 旗標 \_ 本機</span><span class="sxs-lookup"><span data-stu-id="c7609-136">RTM\_ROUTE\_FLAGS\_LOCAL</span></span>  | <span data-ttu-id="c7609-137">0x0010</span><span class="sxs-lookup"><span data-stu-id="c7609-137">0x0010</span></span> | <span data-ttu-id="c7609-138">指出目的地位於可直接連線的網路上。</span><span class="sxs-lookup"><span data-stu-id="c7609-138">Indicates a destination is on a directly reachable network.</span></span>            |
| <span data-ttu-id="c7609-139">RTM \_ 路由 \_ 旗標 \_ 遠端</span><span class="sxs-lookup"><span data-stu-id="c7609-139">RTM\_ROUTE\_FLAGS\_REMOTE</span></span> | <span data-ttu-id="c7609-140">0x0020</span><span class="sxs-lookup"><span data-stu-id="c7609-140">0x0020</span></span> | <span data-ttu-id="c7609-141">指出目的地不在可直接連線的網路上。</span><span class="sxs-lookup"><span data-stu-id="c7609-141">Indicates that the destination is not on a directly reachable network.</span></span> |
| <span data-ttu-id="c7609-142">RTM \_ 路由 \_ 旗標本身 \_</span><span class="sxs-lookup"><span data-stu-id="c7609-142">RTM\_ROUTE\_FLAGS\_MYSELF</span></span> | <span data-ttu-id="c7609-143">0x0040</span><span class="sxs-lookup"><span data-stu-id="c7609-143">0x0040</span></span> | <span data-ttu-id="c7609-144">指出目的地是路由器的其中一個位址。</span><span class="sxs-lookup"><span data-stu-id="c7609-144">Indicates the destination is one of the router's addresses.</span></span>            |



 

## <a name="broadcast-and-multicast-flags"></a><span data-ttu-id="c7609-145">廣播和多播旗標</span><span class="sxs-lookup"><span data-stu-id="c7609-145">Broadcast and Multicast Flags</span></span>



| <span data-ttu-id="c7609-146">常數</span><span class="sxs-lookup"><span data-stu-id="c7609-146">Constant</span></span>                           | <span data-ttu-id="c7609-147">值</span><span class="sxs-lookup"><span data-stu-id="c7609-147">Value</span></span>  | <span data-ttu-id="c7609-148">描述</span><span class="sxs-lookup"><span data-stu-id="c7609-148">Description</span></span>                                                                                                                                                                                                |
|------------------------------------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7609-149">RTM \_ 路由 \_ 旗標 \_ MCAST</span><span class="sxs-lookup"><span data-stu-id="c7609-149">RTM\_ROUTE\_FLAGS\_MCAST</span></span>           | <span data-ttu-id="c7609-150">0x0100</span><span class="sxs-lookup"><span data-stu-id="c7609-150">0x0100</span></span> | <span data-ttu-id="c7609-151">指出此路由是指向多播位址的路由。</span><span class="sxs-lookup"><span data-stu-id="c7609-151">Indicates that this route is a route to a multicast address.</span></span>                                                                                                                                               |
| <span data-ttu-id="c7609-152">RTM \_ 路由 \_ 旗標 \_ 本機 \_ MCAST</span><span class="sxs-lookup"><span data-stu-id="c7609-152">RTM\_ROUTE\_FLAGS\_LOCAL\_MCAST</span></span>    | <span data-ttu-id="c7609-153">0x0200</span><span class="sxs-lookup"><span data-stu-id="c7609-153">0x0200</span></span> | <span data-ttu-id="c7609-154">指出此路由是指向本機多播位址的路由。</span><span class="sxs-lookup"><span data-stu-id="c7609-154">Indicates that this route is a route to a local multicast address.</span></span>                                                                                                                                         |
| <span data-ttu-id="c7609-155">RTM \_ 路由 \_ 旗標 \_ 有限 \_ BC</span><span class="sxs-lookup"><span data-stu-id="c7609-155">RTM\_ROUTE\_FLAGS\_LIMITED\_BC</span></span>     | <span data-ttu-id="c7609-156">0x0400</span><span class="sxs-lookup"><span data-stu-id="c7609-156">0x0400</span></span> | <span data-ttu-id="c7609-157">指出此路由是限制的廣播位址。</span><span class="sxs-lookup"><span data-stu-id="c7609-157">Indicates that this route is a limited broadcast address.</span></span> <span data-ttu-id="c7609-158">不應轉送此目的地的封包。</span><span class="sxs-lookup"><span data-stu-id="c7609-158">Packets to this destination should not be forwarded.</span></span>                                                                                             |
| <span data-ttu-id="c7609-159">RTM \_ 路由 \_ 旗標 \_ 零 \_ NETBC</span><span class="sxs-lookup"><span data-stu-id="c7609-159">RTM\_ROUTE\_FLAGS\_ZEROS\_NETBC</span></span>    | <span data-ttu-id="c7609-160">0x1000</span><span class="sxs-lookup"><span data-stu-id="c7609-160">0x1000</span></span> | <span data-ttu-id="c7609-161">指出目的地符合介面全為零的廣播位址。</span><span class="sxs-lookup"><span data-stu-id="c7609-161">Indicates that the destination matches an interface's all-zeros broadcast address.</span></span> <span data-ttu-id="c7609-162">如果已啟用廣播轉送，則應該接收封包，並將所有適當的介面重新傳送出去。</span><span class="sxs-lookup"><span data-stu-id="c7609-162">If broadcast forwarding is enabled, packets should be received and resent out all appropriate interfaces.</span></span>               |
| <span data-ttu-id="c7609-163">RTM \_ 路由 \_ 旗標 \_ 零 \_ SUBNETBC</span><span class="sxs-lookup"><span data-stu-id="c7609-163">RTM\_ROUTE\_FLAGS\_ZEROS\_SUBNETBC</span></span> | <span data-ttu-id="c7609-164">0x2000</span><span class="sxs-lookup"><span data-stu-id="c7609-164">0x2000</span></span> | <span data-ttu-id="c7609-165">指出目的地符合介面全為零的子網廣播位址。</span><span class="sxs-lookup"><span data-stu-id="c7609-165">Indicates that the destination matches an interface's all-zeros subnet broadcast address.</span></span> <span data-ttu-id="c7609-166">如果已啟用子網廣播轉送，則應該接收封包，並將所有適當的介面重新傳送出去。</span><span class="sxs-lookup"><span data-stu-id="c7609-166">If subnet broadcast forwarding is enabled, packets should be received and resent out all appropriate interfaces.</span></span> |
| <span data-ttu-id="c7609-167">RTM \_ 路由 \_ 旗 \_ 標 \_ NETBC</span><span class="sxs-lookup"><span data-stu-id="c7609-167">RTM\_ROUTE\_FLAGS\_ONES\_NETBC</span></span>     | <span data-ttu-id="c7609-168">0x4000</span><span class="sxs-lookup"><span data-stu-id="c7609-168">0x4000</span></span> | <span data-ttu-id="c7609-169">指出目的地與介面的所有廣播位址相符。</span><span class="sxs-lookup"><span data-stu-id="c7609-169">Indicates that the destination matches an interface's all-ones broadcast address.</span></span> <span data-ttu-id="c7609-170">如果已啟用廣播轉送，則應該接收封包，並將所有適當的介面重新傳送出去。</span><span class="sxs-lookup"><span data-stu-id="c7609-170">If broadcast forwarding is enabled, packets should be received and resent out all appropriate interfaces.</span></span>                |
| <span data-ttu-id="c7609-171">RTM \_ 路由 \_ 旗 \_ 標 \_ SUBNETBC</span><span class="sxs-lookup"><span data-stu-id="c7609-171">RTM\_ROUTE\_FLAGS\_ONES\_SUBNETBC</span></span>  | <span data-ttu-id="c7609-172">0x8000</span><span class="sxs-lookup"><span data-stu-id="c7609-172">0x8000</span></span> | <span data-ttu-id="c7609-173">指出目的地與介面的所有子網廣播位址相符。</span><span class="sxs-lookup"><span data-stu-id="c7609-173">Indicates that the destination matches an interface's all-ones subnet broadcast address.</span></span> <span data-ttu-id="c7609-174">如果已啟用子網廣播轉送，則應該接收封包，並將所有適當的介面重新傳送出去。</span><span class="sxs-lookup"><span data-stu-id="c7609-174">If subnet broadcast forwarding is enabled, packets should be received and resent out all appropriate interfaces.</span></span>  |



 

## <a name="grouping-of-flags"></a><span data-ttu-id="c7609-175">旗標群組</span><span class="sxs-lookup"><span data-stu-id="c7609-175">Grouping of Flags</span></span>



| <span data-ttu-id="c7609-176">Group</span><span class="sxs-lookup"><span data-stu-id="c7609-176">Group</span></span>                            | <span data-ttu-id="c7609-177">成員</span><span class="sxs-lookup"><span data-stu-id="c7609-177">Members</span></span>                                                                                                                                                                  | <span data-ttu-id="c7609-178">Description</span><span class="sxs-lookup"><span data-stu-id="c7609-178">Description</span></span>                                              |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="c7609-179">RTM \_ 路由 \_ 旗標 \_ 轉送</span><span class="sxs-lookup"><span data-stu-id="c7609-179">RTM\_ROUTE\_FLAGS\_FORWARDING</span></span>    | <span data-ttu-id="c7609-180">RTM \_ 路由 \_ 旗標 \_ MARTIAN、RTM \_ 路由 \_ 旗標 \_ BLACKHOLE、RTM \_ 路由旗標 \_ \_ 捨棄、RTM \_ 路由 \_ 旗標 \_ 非使用中</span><span class="sxs-lookup"><span data-stu-id="c7609-180">RTM\_ROUTE\_FLAGS\_MARTIAN, RTM\_ROUTE\_FLAGS\_BLACKHOLE, RTM\_ROUTE\_FLAGS\_DISCARD, RTM\_ROUTE\_FLAGS\_INACTIVE</span></span>                                                        | <span data-ttu-id="c7609-181">指定任何轉送旗標。</span><span class="sxs-lookup"><span data-stu-id="c7609-181">Specifies any forwarding flags.</span></span>                          |
| <span data-ttu-id="c7609-182">RTM \_ 路由 \_ 旗標 \_ 任何 \_ 單播</span><span class="sxs-lookup"><span data-stu-id="c7609-182">RTM\_ROUTE\_FLAGS\_ANY\_UNICAST</span></span>  | <span data-ttu-id="c7609-183">RTM \_ 路由 \_ 旗標 \_ LOCAL、RTM \_ ROUTE \_ FLAGS \_ REMOTE、RTM \_ ROUTE \_ FLAGS \_</span><span class="sxs-lookup"><span data-stu-id="c7609-183">RTM\_ROUTE\_FLAGS\_LOCAL, RTM\_ROUTE\_FLAGS\_REMOTE, RTM\_ROUTE\_FLAGS\_MYSELF</span></span>                                                                                           | <span data-ttu-id="c7609-184">指定任何單播旗標。</span><span class="sxs-lookup"><span data-stu-id="c7609-184">Specifies any unicast flags.</span></span>                             |
| <span data-ttu-id="c7609-185">RTM \_ 路由 \_ 旗標 \_ 任何 \_ MCAST</span><span class="sxs-lookup"><span data-stu-id="c7609-185">RTM\_ROUTE\_FLAGS\_ANY\_MCAST</span></span>    | <span data-ttu-id="c7609-186">RTM \_ 路由 \_ 旗標 \_ MCAST，RTM \_ 路由 \_ 旗標 \_ 本機 \_ MCAST</span><span class="sxs-lookup"><span data-stu-id="c7609-186">RTM\_ROUTE\_FLAGS\_MCAST, RTM\_ROUTE\_FLAGS\_LOCAL\_MCAST</span></span>                                                                                                                | <span data-ttu-id="c7609-187">指定任何單播旗標。</span><span class="sxs-lookup"><span data-stu-id="c7609-187">Specifies any unicast flags.</span></span>                             |
| <span data-ttu-id="c7609-188">RTM \_ 路由 \_ 旗標 \_ 子網 \_ BCAST</span><span class="sxs-lookup"><span data-stu-id="c7609-188">RTM\_ROUTE\_FLAGS\_SUBNET\_BCAST</span></span> | <span data-ttu-id="c7609-189">RTM \_ 路由 \_ 旗標一個 \_ \_ 子網 \_ BC、RTM \_ ROUTE \_ FLAGS \_ 零 \_ SUBNETBC</span><span class="sxs-lookup"><span data-stu-id="c7609-189">RTM\_ROUTE\_FLAGS\_ONES\_SUBNET\_BC, RTM\_ROUTE\_FLAGS\_ZEROS\_SUBNETBC</span></span>                                                                                                  | <span data-ttu-id="c7609-190">指定任何子網廣播旗標。</span><span class="sxs-lookup"><span data-stu-id="c7609-190">Specifies any subnet broadcast flags.</span></span>                    |
| <span data-ttu-id="c7609-191">RTM \_ 路由 \_ 旗標 \_ 網路 \_ BCAST</span><span class="sxs-lookup"><span data-stu-id="c7609-191">RTM\_ROUTE\_FLAGS\_NET\_BCAST</span></span>    | <span data-ttu-id="c7609-192">RTM \_ 路由 \_ 旗標有一個 \_ \_ NETBC，RTM \_ 路由 \_ 旗標 \_ 零 \_ NETBC</span><span class="sxs-lookup"><span data-stu-id="c7609-192">RTM\_ROUTE\_FLAGS\_ONES\_NETBC, RTM\_ROUTE\_FLAGS\_ZEROS\_NETBC</span></span>                                                                                                          | <span data-ttu-id="c7609-193">指定任何全網路廣播旗標。</span><span class="sxs-lookup"><span data-stu-id="c7609-193">Specifies any net-wide broadcast flags.</span></span>                  |
| <span data-ttu-id="c7609-194">RTM \_ 路由 \_ 旗標 \_ 任何 \_ BCAST</span><span class="sxs-lookup"><span data-stu-id="c7609-194">RTM\_ROUTE\_FLAGS\_ANY\_BCAST</span></span>    | <span data-ttu-id="c7609-195">RTM \_ 路由 \_ 旗標 \_ 受限於 \_ BC、RTM \_ ROUTE \_ FLAGS \_ \_ NETBC、RTM \_ ROUTE FLAGS、 \_ \_ \_ SUBNET \_ BC、RTM \_ ROUTE \_ FLAGS \_ 零 \_ NETBC、RTM \_ ROUTE \_ 旗標 \_ 零 \_ SUBNETBC</span><span class="sxs-lookup"><span data-stu-id="c7609-195">RTM\_ROUTE\_FLAGS\_LIMITED\_BC, RTM\_ROUTE\_FLAGS\_ONES\_NETBC, RTM\_ROUTE\_FLAGS\_ONES\_SUBNET\_BC, RTM\_ROUTE\_FLAGS\_ZEROS\_NETBC, RTM\_ROUTE\_FLAGS\_ZEROS\_SUBNETBC</span></span> | <span data-ttu-id="c7609-196">指定任何子網或全網路廣播旗標。</span><span class="sxs-lookup"><span data-stu-id="c7609-196">Specifies any of the subnet or net-wide broadcast flags.</span></span> |



 

 

 




