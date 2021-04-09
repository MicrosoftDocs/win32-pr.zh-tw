---
title: 標示 Hold-Down 狀態的路由
description: 某些用戶端（例如 RIP 和 DVMRP 等距離向量通訊協定）要求在刪除目的地的最後一個路由之後，將目的地公告為無法連線。
ms.assetid: 2a86c092-d8a6-4fd4-8b2e-451c160f743f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af10832452a3a0b9ca851c209d240c97998ef519
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932307"
---
# <a name="marking-routes-for-the-hold-down-state"></a><span data-ttu-id="7a277-103">標示 Hold-Down 狀態的路由</span><span class="sxs-lookup"><span data-stu-id="7a277-103">Marking Routes for the Hold-Down State</span></span>

<span data-ttu-id="7a277-104">某些用戶端（例如 RIP 和 DVMRP 等距離向量通訊協定）要求在刪除目的地的最後一個路由之後，將目的地公告為無法連線。</span><span class="sxs-lookup"><span data-stu-id="7a277-104">Some clients, such as distance vector protocols like RIP and DVMRP, require that destinations be advertised as unreachable for a certain time after the last route to the destination is deleted.</span></span> <span data-ttu-id="7a277-105">最後一個刪除的路由必須公告為無法存取，即使較新的路由同時抵達也是一樣。</span><span class="sxs-lookup"><span data-stu-id="7a277-105">The last route that is deleted must be advertised as unreachable even if newer routes arrive in the meantime.</span></span> <span data-ttu-id="7a277-106">最後一個刪除的路由會標示為處於 *按住狀態*。</span><span class="sxs-lookup"><span data-stu-id="7a277-106">The last route deleted is marked as being in a *hold-down state*.</span></span> <span data-ttu-id="7a277-107">按住進程可防止路由迴圈的構成。</span><span class="sxs-lookup"><span data-stu-id="7a277-107">The hold-down process prevents the formation of routing loops.</span></span> <span data-ttu-id="7a277-108">路由通訊協定通告過時的路由資訊時，會導致路由迴圈。</span><span class="sxs-lookup"><span data-stu-id="7a277-108">Routing loops are caused when a routing protocol advertises obsolete routing information.</span></span> <span data-ttu-id="7a277-109">當保留期限到期時，這些通訊協定會以新的最佳路由繼續其廣告。</span><span class="sxs-lookup"><span data-stu-id="7a277-109">When the hold-down expires, these protocols resume their advertisement with the new best route.</span></span>

<span data-ttu-id="7a277-110">採用 [**RtmHoldDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination) 函式的通訊協定，會指出目的地處于「按住」狀態。</span><span class="sxs-lookup"><span data-stu-id="7a277-110">A protocol that implements hold-down states indicates that a destination is in a hold-down state by using the [**RtmHoldDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination) function.</span></span> <span data-ttu-id="7a277-111">當用戶端通告此目的地的最佳路由時，會呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="7a277-111">The client calls this function when it advertises the best route to this destination.</span></span> <span data-ttu-id="7a277-112">如果稍後刪除此目的地的所有路由，則會在先前呼叫 **RtmHoldDestination** 所指定的時間期間，將刪除的最後一個路由保留在按住狀態。</span><span class="sxs-lookup"><span data-stu-id="7a277-112">If all routes to this destination are later deleted, the last route that is deleted is kept in a hold-down state for the period of time specified in the earlier call to **RtmHoldDestination**.</span></span>

<span data-ttu-id="7a277-113">當通訊協定通告目的地時，所使用的路由資訊取決於通訊協定是否使用「保留」狀態，以及目的地是否存在「保留中斷」狀態的路由。</span><span class="sxs-lookup"><span data-stu-id="7a277-113">When a protocol advertises a destination, the route information that is used depends on whether the protocol uses hold-down states and if a route in the hold-down state exists for the destination.</span></span>

<span data-ttu-id="7a277-114">未使用「保留」狀態的通訊協定可以忽略與目的地保持狀態相關的路由資訊，並且一律通告最佳路由。</span><span class="sxs-lookup"><span data-stu-id="7a277-114">Protocols that do not use hold-down states can ignore route information that relates to hold-down states for a destination, and always advertise the best route.</span></span>

<span data-ttu-id="7a277-115">如需顯示如何使用這些函式的範例程式碼，請參閱 [使用路由 Hold-Down 狀態](use-the-route-hold-down-state.md)。</span><span class="sxs-lookup"><span data-stu-id="7a277-115">For sample code that shows how to use these functions, see [Use the Route Hold-Down State](use-the-route-hold-down-state.md).</span></span>

 

 




