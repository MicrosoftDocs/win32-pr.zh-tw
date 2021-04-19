---
description: IPv6 路由器公告的內容會自動從路由表中已發佈的路由衍生。 Nonpublished 路由是用於路由傳送，但在建立路由器公告時則會忽略。
ms.assetid: 27b735db-4e87-497b-b39c-e464cf44f09e
title: IPv6 路由器公告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a75b31a988595cba85d23dbafc1bd93ffff4ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992442"
---
# <a name="ipv6-router-advertisements"></a><span data-ttu-id="81284-104">IPv6 路由器公告</span><span class="sxs-lookup"><span data-stu-id="81284-104">IPv6 Router Advertisements</span></span>

<span data-ttu-id="81284-105">IPv6 路由器公告的內容會自動從路由表中已發佈的路由衍生。</span><span class="sxs-lookup"><span data-stu-id="81284-105">The content of IPv6 router advertisements is automatically derived from the published routes in the routing table.</span></span> <span data-ttu-id="81284-106">Nonpublished 路由是用於路由傳送，但在建立路由器公告時則會忽略。</span><span class="sxs-lookup"><span data-stu-id="81284-106">Nonpublished routes are used for routing but are ignored when constructing router advertisements.</span></span>

<span data-ttu-id="81284-107">IPv6 的路由器公告一律包含來源連結層位址選項和 MTU 選項。</span><span class="sxs-lookup"><span data-stu-id="81284-107">Router advertisements for IPv6 always contain a source link-layer address option and an MTU option.</span></span> <span data-ttu-id="81284-108">MTU 選項的值取自傳送介面的目前連結 MTU。</span><span class="sxs-lookup"><span data-stu-id="81284-108">The value for the MTU option is taken from the sending interface's current link MTU.</span></span> <span data-ttu-id="81284-109">您可以使用 ipv6 ifc mtu 命令來變更這個值。</span><span class="sxs-lookup"><span data-stu-id="81284-109">This value can be changed with the ipv6 ifc mtu command.</span></span>

<span data-ttu-id="81284-110">如果有已發佈的預設路由，則路由器通告只有非零的路由器存留期。</span><span class="sxs-lookup"><span data-stu-id="81284-110">The router advertisement only has a nonzero router lifetime if there is a published default route.</span></span> <span data-ttu-id="81284-111">預設路由是零長度首碼的路由。</span><span class="sxs-lookup"><span data-stu-id="81284-111">A default route is a route for the zero-length prefix.</span></span>

<span data-ttu-id="81284-112">發佈的連結路由會導致路由器公告中的前置詞資訊選項。</span><span class="sxs-lookup"><span data-stu-id="81284-112">Published on-link routes result in prefix information options in router advertisements.</span></span> <span data-ttu-id="81284-113">如果連結前置詞有64位，首碼資訊選項會同時設定 L 和 bits，而接收它的主機將會 autoconfigure 位址。</span><span class="sxs-lookup"><span data-stu-id="81284-113">If the on-link prefix has 64 bits, the prefix information option has both the L and A bits set and hosts receiving it will autoconfigure addresses.</span></span>

<span data-ttu-id="81284-114">傳送路由器公告的介面也會根據它所傳送的首碼資訊選項來 autoconfigure 自己的位址。</span><span class="sxs-lookup"><span data-stu-id="81284-114">An interface that sends router advertisements will also autoconfigure addresses for itself based on the prefix information options that it sends.</span></span>

<span data-ttu-id="81284-115">所有已發佈路由上的有限 nonaging 存留期 (例如，建議使用30分鐘) 。</span><span class="sxs-lookup"><span data-stu-id="81284-115">A finite nonaging lifetime on all published routes (for example, 30 minutes) is recommended.</span></span> <span data-ttu-id="81284-116">如果您決定要撤銷路由，可以將路由變更為具有過時存留期。</span><span class="sxs-lookup"><span data-stu-id="81284-116">If you decide to retract a route, you can change the route to have an aging lifetime.</span></span> <span data-ttu-id="81284-117">路由將在數個路由器公告的過程中存留，然後從路由器和接收路由器通告的任何主機中消失。</span><span class="sxs-lookup"><span data-stu-id="81284-117">The route will age over the course of several router advertisements and then disappear from both the router and any hosts receiving the router advertisements.</span></span>

<span data-ttu-id="81284-118">主機透過路由器公告存留期找出的路由，且不會發佈。</span><span class="sxs-lookup"><span data-stu-id="81284-118">Routes that hosts find through router advertisements age and are not published.</span></span> <span data-ttu-id="81284-119">從路由器公告的存留期，也能解決這種情況。</span><span class="sxs-lookup"><span data-stu-id="81284-119">Addresses autoconfigured from router advertisements age as well.</span></span>

 

 



