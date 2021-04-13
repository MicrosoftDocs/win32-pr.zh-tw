---
title: 路由表管理員架構如何搭配在一起
description: 下圖顯示路由器的不同元件之間的關聯性。
ms.assetid: 862566ce-47c4-424a-84c2-99f4c92efcc0
keywords:
- RTM，架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc36c339ac89f01d5ba14c00857b3ced9c29414c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311594"
---
# <a name="how-the-routing-table-manager-architecture-fits-together"></a><span data-ttu-id="36e85-104">路由表管理員架構如何搭配在一起</span><span class="sxs-lookup"><span data-stu-id="36e85-104">How the Routing Table Manager Architecture Fits Together</span></span>

<span data-ttu-id="36e85-105">下圖顯示路由器的不同元件之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="36e85-105">The following illustration shows the relationship between the different components of a router.</span></span>

![路由器元件之間的關聯性](images/rtsrvarch.png)

<span data-ttu-id="36e85-107">啟動路由器時，會啟動路由器管理員服務，以及一或多個路由通訊協定。</span><span class="sxs-lookup"><span data-stu-id="36e85-107">When the router is bootstrapped, the router manager service is started, as well as one or more routing protocols.</span></span> <span data-ttu-id="36e85-108">路由通訊協定與路由器上的各種介面相關聯。</span><span class="sxs-lookup"><span data-stu-id="36e85-108">Routing protocols are associated with the various interfaces on the router.</span></span> <span data-ttu-id="36e85-109">路由器管理員也會啟動路由表管理員。</span><span class="sxs-lookup"><span data-stu-id="36e85-109">The router manager also starts the routing table manager.</span></span>

<span data-ttu-id="36e85-110">下圖顯示用戶端與路由表管理員的不同元件之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="36e85-110">The following illustration shows the relationship between clients and the different components of the routing table manager.</span></span>

![用戶端與路由表管理員元件之間的關聯性](images/rtmentrel.png)

<span data-ttu-id="36e85-112">路由器管理員會啟動路由表管理員的一或多個實例。</span><span class="sxs-lookup"><span data-stu-id="36e85-112">The router manager starts one or more instances of the routing table manager.</span></span> <span data-ttu-id="36e85-113">當路由表管理員的多個實例啟動時，路由器已設定為可作為一或多個虛擬路由器。</span><span class="sxs-lookup"><span data-stu-id="36e85-113">When multiple instances of the routing table manager are started, the router has been configured to act as one or more virtual routers.</span></span> <span data-ttu-id="36e85-114">路由表管理員的每個實例都擁有一或多個介面;每一個介面只能由一個路由表管理員的實例所擁有。</span><span class="sxs-lookup"><span data-stu-id="36e85-114">Each instance of the routing table manager owns one or more interfaces; each interface can only be owned by one instance of the routing table manager.</span></span>

<span data-ttu-id="36e85-115">路由表管理員的每個實例都與其他實例無關;實例之間不會交換任何資訊。</span><span class="sxs-lookup"><span data-stu-id="36e85-115">Each instance of the routing table manager is independent from the others; no information is exchanged between the instances.</span></span>

<span data-ttu-id="36e85-116">路由表管理員的每個實例都包含一或多個路由表。</span><span class="sxs-lookup"><span data-stu-id="36e85-116">Each instance of the routing table manager contains one or more routing tables.</span></span> <span data-ttu-id="36e85-117">每個路由表都與位址系列相關聯。</span><span class="sxs-lookup"><span data-stu-id="36e85-117">Each routing table is associated with an address family.</span></span>

<span data-ttu-id="36e85-118">每個路由表都包含一或多個視圖。</span><span class="sxs-lookup"><span data-stu-id="36e85-118">Each routing table contains one or more views.</span></span> <span data-ttu-id="36e85-119">在此範例中，路由表會顯示為單播和多播的觀點。</span><span class="sxs-lookup"><span data-stu-id="36e85-119">In this example, the routing table is shown with a unicast and multicast view.</span></span> <span data-ttu-id="36e85-120">每個視圖都是路由表的子集。</span><span class="sxs-lookup"><span data-stu-id="36e85-120">Each view is a subset of the routing table.</span></span>

<span data-ttu-id="36e85-121">下圖顯示用戶端與路由表管理員的多個實例之間的關聯性、路由表和 views。</span><span class="sxs-lookup"><span data-stu-id="36e85-121">The following illustration shows the relationship between clients and multiple instances of the routing table manager, routing tables, and views.</span></span>

![關聯性用戶端，路由表管理員，路由表，視圖](images/multrtabrel.png)

<span data-ttu-id="36e85-123">用戶端的實例可以使用路由表管理員的實例多次註冊（每個位址系列一次）。</span><span class="sxs-lookup"><span data-stu-id="36e85-123">An instance of the client can register multiple times with an instance of the routing table manager — once per address family.</span></span> <span data-ttu-id="36e85-124">用戶端可以註冊每個路由表管理員的實例。</span><span class="sxs-lookup"><span data-stu-id="36e85-124">A client can register with each instance of the routing table manager.</span></span>

<span data-ttu-id="36e85-125">下圖顯示路由表專案的關聯方式。</span><span class="sxs-lookup"><span data-stu-id="36e85-125">The following illustration shows how the routing table entries are related.</span></span> <span data-ttu-id="36e85-126">如需路由表專案的詳細資訊，請參閱 [路由表專案](routing-table-entries.md)。</span><span class="sxs-lookup"><span data-stu-id="36e85-126">For more information on routing table entries, see [Routing Table Entries](routing-table-entries.md).</span></span>

![路由表專案之間的關聯性](images/nexthop.png)

<span data-ttu-id="36e85-128">路由表包含目的地。</span><span class="sxs-lookup"><span data-stu-id="36e85-128">The routing table contains destinations.</span></span> <span data-ttu-id="36e85-129">每個目的地都與一或多個路由相關。</span><span class="sxs-lookup"><span data-stu-id="36e85-129">Each destination is related to one or more routes.</span></span> <span data-ttu-id="36e85-130">每個路由都有零個、一個或多個指標指向與路由相關聯的下一個躍點。</span><span class="sxs-lookup"><span data-stu-id="36e85-130">Each route has zero, one, or more pointers to next hops that are associated with the route.</span></span> <span data-ttu-id="36e85-131">每個指標都會參考下一個躍點清單中的實際下一個躍點。</span><span class="sxs-lookup"><span data-stu-id="36e85-131">Each pointer refers to the actual next hop in the list of next hops.</span></span> <span data-ttu-id="36e85-132">使用路由表管理員註冊的每個用戶端都會建立用戶端所擁有的下一個躍點清單。</span><span class="sxs-lookup"><span data-stu-id="36e85-132">Each client that registers with the routing table manager creates a list of next hops that the client owns.</span></span>

<span data-ttu-id="36e85-133">路由只能包含與擁有路由之用戶端相關聯的下一個躍點清單的指標。</span><span class="sxs-lookup"><span data-stu-id="36e85-133">Routes can only contain pointers to the next-hop list associated with the client that owns the route.</span></span>

 

 




