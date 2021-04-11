---
title: 多播架構如何搭配
description: 本節說明範例設定，以及主要元件如何彼此配合。
ms.assetid: 1fa0b343-0276-402b-8c3d-5ca114ad43cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc82178568bac01e89eb0a4d6ea9222d45e7f5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183749"
---
# <a name="how-the-multicast-architecture-fits-together"></a><span data-ttu-id="4e080-103">多播架構如何搭配</span><span class="sxs-lookup"><span data-stu-id="4e080-103">How the Multicast Architecture Fits Together</span></span>

<span data-ttu-id="4e080-104">本節說明範例設定，以及主要元件如何彼此配合。</span><span class="sxs-lookup"><span data-stu-id="4e080-104">This section describes a sample configuration and how the major components fit together.</span></span>

<span data-ttu-id="4e080-105">下圖顯示路由器各元件之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="4e080-105">The following illustration shows the relationship between the various components of a router.</span></span>

![windows 2000 路由器元件之間的關聯性](images/mrarch1.png)

<span data-ttu-id="4e080-107">多播群組管理員是在以路由器運作的伺服器上執行之 RRAS 服務的一部分。</span><span class="sxs-lookup"><span data-stu-id="4e080-107">The multicast group manager is a part of the RRAS service that runs on a server that is operating as a router.</span></span>

<span data-ttu-id="4e080-108">顯示的路由器有三個多播路由通訊協定， (Protocol 1、Protocol 2、Protocol 3) 在其上執行。</span><span class="sxs-lookup"><span data-stu-id="4e080-108">The router shown has three multicast routing protocols (Protocol 1, Protocol 2, Protocol 3) running on it.</span></span> <span data-ttu-id="4e080-109">每個通訊協定都可以擁有一或多個介面 (在此圖中，通訊協定1擁有介面1、Protocol 2 擁有介面2，而通訊協定3擁有介面 3) 。</span><span class="sxs-lookup"><span data-stu-id="4e080-109">Each protocol can own one or more interfaces (in this illustration, Protocol 1 owns Interface 1, Protocol 2 owns Interface 2, and Protocol 3 owns Interface 3).</span></span> <span data-ttu-id="4e080-110">除了 IGMP 之外，每個介面都只能擁有一個路由通訊協定 (，這是) 的特殊案例。</span><span class="sxs-lookup"><span data-stu-id="4e080-110">Each interface can be owned by only one routing protocol (in addition to IGMP, which is a special case).</span></span>

<span data-ttu-id="4e080-111">多播群組管理員會在路由器上執行，並在路由通訊協定之間協調群組資訊的散發。</span><span class="sxs-lookup"><span data-stu-id="4e080-111">The multicast group manager runs on the router and coordinates the distribution of group information between the routing protocols.</span></span>

<span data-ttu-id="4e080-112">下圖顯示多播架構中兩個路由器之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="4e080-112">The following illustration shows the relationship between two routers in a multicast architecture.</span></span>

![多播架構中的兩個路由器之間的關聯性](images/mrarch2.png)

<span data-ttu-id="4e080-114">在上圖中，路由器2會將多播訊息傳送至介面3上的網路2。</span><span class="sxs-lookup"><span data-stu-id="4e080-114">In the previous illustration, Router 2 sends a multicast message to Network 2 on Interface 3.</span></span> <span data-ttu-id="4e080-115">路由器1會在介面3接收來自網路2的多播訊息。</span><span class="sxs-lookup"><span data-stu-id="4e080-115">Router 1 receives the multicast message from Network 2 on Interface 3.</span></span> <span data-ttu-id="4e080-116">在這兩個路由器上，通訊協定3擁有各自的介面3。</span><span class="sxs-lookup"><span data-stu-id="4e080-116">On both routers, Protocol 3 owns the respective Interface 3.</span></span>

<span data-ttu-id="4e080-117">下圖顯示從多播來源 (到多播群組之訊息的路徑，) 會到達已加入多播群組的主機。</span><span class="sxs-lookup"><span data-stu-id="4e080-117">The following illustration shows the path a message from a multicast source (to a multicast group) takes to reach the host that has joined the multicast group.</span></span> <span data-ttu-id="4e080-118">圖中的路由器會使用與上圖相同的設定;但是，不會顯示介面和通訊協定詳細資料，以便讓圖表保持簡單。</span><span class="sxs-lookup"><span data-stu-id="4e080-118">The routers in the illustration use the same configuration as previous illustrations; however, the interface and protocol details are not shown in order to keep the figure simple.</span></span>

![從多播來源到目的地主機的訊息路徑](images/mrarch3.png)

<span data-ttu-id="4e080-120">下列案例描述當主機加入多播群組時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="4e080-120">The following scenario describes the events that take place when a host joins a multicast group.</span></span> <span data-ttu-id="4e080-121">請參閱上圖，以瞭解各種實體之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="4e080-121">Refer to the previous illustration for relationships between the various entities.</span></span>

1.  <span data-ttu-id="4e080-122">主機1：在網路3上加入多播群組 G。</span><span class="sxs-lookup"><span data-stu-id="4e080-122">Host 1 joins the multicast group G on Network 3.</span></span>
2.  <span data-ttu-id="4e080-123">路由器3透過 IGMP 學習 G。</span><span class="sxs-lookup"><span data-stu-id="4e080-123">Router 3 learns about G via IGMP.</span></span>
3.  <span data-ttu-id="4e080-124">路由器3上的多播群組管理員會通知路由器3上有 G 的新接收器的通訊協定3。</span><span class="sxs-lookup"><span data-stu-id="4e080-124">The multicast group manager on Router 3 notifies Protocol 3 on Router 3 that there are new receivers for G.</span></span>
4.  <span data-ttu-id="4e080-125">路由器3上的通訊協定3接著會在路由器1上通知 G 的通訊協定3。</span><span class="sxs-lookup"><span data-stu-id="4e080-125">Protocol 3 on Router 3 then notifies Protocol 3 on Router 1 about G.</span></span>
5.  <span data-ttu-id="4e080-126">接著，路由器1上的通訊協定3會通知路由器1上的多播群組管理員約 G。</span><span class="sxs-lookup"><span data-stu-id="4e080-126">In turn, Protocol 3 on Router 1 notifies the multicast group manager on Router 1 about G.</span></span>
6.  <span data-ttu-id="4e080-127">路由器1上的多播群組管理員接著會向通訊協定1和通訊協定2通知 G。</span><span class="sxs-lookup"><span data-stu-id="4e080-127">The multicast group manager on Router 1 then notifies Protocol 1 and Protocol 2 about G.</span></span>
7.  <span data-ttu-id="4e080-128">如果通訊協定是設計來這麼做，通訊協定2可能會通知路由器2。</span><span class="sxs-lookup"><span data-stu-id="4e080-128">Protocol 2 may inform Router 2 about G, if the protocol is designed to do so.</span></span>

<span data-ttu-id="4e080-129">下列案例描述將訊息傳送至多播群組時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="4e080-129">The following scenario describes the events that take place when a message is sent to a multicast group.</span></span> <span data-ttu-id="4e080-130">請參閱上圖，以瞭解各種實體之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="4e080-130">Refer to the previous illustration for the relationships between the various entities.</span></span>

1.  <span data-ttu-id="4e080-131">網路1上的來源會將訊息傳送至群組 G。</span><span class="sxs-lookup"><span data-stu-id="4e080-131">A source on Network 1 sends a message to Group G.</span></span>
2.  <span data-ttu-id="4e080-132">從來源 S 傳送的訊息會先傳送到路由器2，然後使用介面2將它轉送到路由器 1 (因為路由器2已經由通訊協定2告知，接收者會出現下游) 。</span><span class="sxs-lookup"><span data-stu-id="4e080-132">The message sent from Source S goes first to Router 2, which then forwards it to Router 1 using Interface 2 (since Router 2 has been informed by Protocol 2 that receivers are present downstream).</span></span>
3.  <span data-ttu-id="4e080-133">路由器1會將訊息轉送到路由器 3 (，因為通訊協定2已通知路由器1，表示接收者存在於下游) 。</span><span class="sxs-lookup"><span data-stu-id="4e080-133">Router 1 forwards the message to Router 3 (since Router 1 has been informed by Protocol 2 that receivers are present downstream).</span></span>
4.  <span data-ttu-id="4e080-134">路由器3會將訊息轉送到網路3，因此抵達主機1。</span><span class="sxs-lookup"><span data-stu-id="4e080-134">Router 3 forwards the message to Network 3, and therefore it arrives at Host 1.</span></span>

<span data-ttu-id="4e080-135">如需多播路由通訊協定互動的詳細資訊，請參閱 [RFC 2715](routing-protocols-request-for-comments.md)、多播路由通訊協定的互通性規則。</span><span class="sxs-lookup"><span data-stu-id="4e080-135">For further information on multicast routing protocol interaction, see [RFC 2715](routing-protocols-request-for-comments.md), Interoperability Rules for Multicast Routing Protocols.</span></span>

 

 




