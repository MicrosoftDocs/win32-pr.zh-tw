---
title: 路由器架構的元件
description: 路由器系統管理檔會經常參考路由器的下列元件。
ms.assetid: 841a5728-39d6-4bd7-a41a-6543b4ed9985
keywords:
- 路由器 RRAS，元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fb0cc69de5402b03550873b3b052f6329b5238
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462220"
---
# <a name="components-of-the-router-architecture"></a><span data-ttu-id="dd1b5-104">路由器架構的元件</span><span class="sxs-lookup"><span data-stu-id="dd1b5-104">Components of the Router Architecture</span></span>

<span data-ttu-id="dd1b5-105">路由器系統管理檔會經常參考路由器的下列元件。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-105">The router administration documentation makes frequent reference to the following components of the router.</span></span>

<span data-ttu-id="dd1b5-106">動態介面管理員 (維度) </span><span class="sxs-lookup"><span data-stu-id="dd1b5-106">Dynamic Interface Manager (DIM)</span></span>

<span data-ttu-id="dd1b5-107">所有的路由器管理功能都會通過 DIM。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-107">All router administration functions pass through DIM.</span></span> <span data-ttu-id="dd1b5-108">根據函數的本質而定，DIM 可能會將呼叫傳遞給其中一個路由器管理員。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-108">Depending on the nature of the function, DIM may pass the call on to one of the router managers.</span></span> <span data-ttu-id="dd1b5-109">只處理介面的函式是由 DIM 處理。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-109">Functions that deal only with interfaces are handled by DIM.</span></span> <span data-ttu-id="dd1b5-110">如果此函式會影響路由通訊協定，則 DIM 會針對對應至該通訊協定的傳輸呼叫路由器管理員。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-110">If the function affects routing protocols, DIM will call into the router manager for the transport corresponding to that protocol.</span></span> <span data-ttu-id="dd1b5-111">例如，如果函式會影響 Open 最短路徑 First (OSPF) protocol，DIM 將會呼叫 IP 路由器管理員，因為 OSPF 是 IP 路由通訊協定。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-111">For example, if the function affects the Open Shortest Path First (OSPF) protocol, DIM will call into the IP Router Manager, since OSPF is an IP routing protocol.</span></span>

<span data-ttu-id="dd1b5-112">路由器管理員</span><span class="sxs-lookup"><span data-stu-id="dd1b5-112">Router Managers</span></span>

<span data-ttu-id="dd1b5-113">每個符合路由器架構的可路由傳輸都有自己的路由器管理員。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-113">Each routable transport that fits into the router architecture has its own router manager.</span></span> <span data-ttu-id="dd1b5-114">目前的路由器管理員存在於 IP 和 IPX 傳輸。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-114">Currently router managers exist for the IP and IPX transports.</span></span> <span data-ttu-id="dd1b5-115">路由器管理員會管理在本機電腦上的介面上執行的路由器通訊協定和其他類型的路由用戶端。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-115">The router managers manage router protocols and other types of routing clients that run on interfaces on the local computer.</span></span>

<span data-ttu-id="dd1b5-116">路由通訊協定和其他用戶端</span><span class="sxs-lookup"><span data-stu-id="dd1b5-116">Routing Protocols and other Clients</span></span>

<span data-ttu-id="dd1b5-117">用戶端是在路由器架構架構內運作的服務提供者。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-117">Clients are service providers that function within the framework of the router architecture.</span></span> <span data-ttu-id="dd1b5-118">路由通訊協定是路由器支援的一種用戶端。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-118">Routing protocols are one type of client that is supported by the router.</span></span>

<span data-ttu-id="dd1b5-119">用戶端是特定可路由傳送的特定： IP 或 IPX。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-119">Clients are specific to a particular routable transport: either IP or IPX.</span></span> <span data-ttu-id="dd1b5-120">IP 傳輸的路由通訊協定包括 Open 最短路徑 First (OSPF) 和路由資訊通訊協定 (RIP) 。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-120">Routing protocols for the IP transport include Open Shortest Path First (OSPF) and Routing Information Protocol (RIP).</span></span> <span data-ttu-id="dd1b5-121">IPX 路由通訊協定的範例是 (SAP) 和適用于 IPX 的 RIP 的服務公告通訊協定。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-121">Examples of IPX routing protocols are Service Advertising Protocol (SAP) and RIP for IPX.</span></span> <span data-ttu-id="dd1b5-122">非路由通訊協定的用戶端範例為 IP (NAT) 的網路位址轉譯。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-122">An example of a client that is not a routing protocol is Network Address Translation (NAT) for IP.</span></span>

<span data-ttu-id="dd1b5-123">路由器管理員和用戶端之間的介面，會在 [路由通訊協定介面](about-routing-protocol-interface.md)一節中說明。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-123">The interface between the router manager and a client is described in the section [Routing Protocol Interface](about-routing-protocol-interface.md).</span></span> <span data-ttu-id="dd1b5-124">所有用戶端都符合這個介面。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-124">All clients conform to this interface.</span></span> <span data-ttu-id="dd1b5-125">使用這個介面時，廠商可以執行自己與路由器相容的用戶端。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-125">Using this interface, vendors can implement their own clients that are compatible with the router.</span></span>

[<span data-ttu-id="dd1b5-126">介面</span><span class="sxs-lookup"><span data-stu-id="dd1b5-126">Interfaces</span></span>](interfaces.md)

<span data-ttu-id="dd1b5-127">介面是與外部網路的連接。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-127">An interface is a connection to an external network.</span></span> <span data-ttu-id="dd1b5-128">每個介面都是由唯一的介面 *索引* 來識別。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-128">Each interface is identified by a unique interface *index*.</span></span> <span data-ttu-id="dd1b5-129">介面是邏輯實體;路由器用戶端（例如 NAT 或 OSPF）會以同樣的方式處理所有類型的介面。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-129">Interfaces are logical entities; router clients such at NAT or OSPF deal with all types of interfaces similarly.</span></span> <span data-ttu-id="dd1b5-130">不過，在執行方面，介面可代表專用連線 (例如區域網路 (LAN) ) 或非專用的撥號連線 (例如，與廣域網路 (的廣域網路連線的 PPP 連線。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-130">In terms of implementation however, an interface can represent a dedicated connection (such as to a Local Area Network (LAN)) or a non-dedicated, dial up connection (such as a PPP connection to a Wide Area Network (WAN)).</span></span>

<span data-ttu-id="dd1b5-131">如果是 LAN 介面，介面會對應到電腦中的實際實體裝置，也就是 LAN 介面卡。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-131">In the case of a LAN interface, the interface corresponds to an actual physical device in the computer, a LAN adapter.</span></span> <span data-ttu-id="dd1b5-132">在 WAN 介面的案例中，介面會在建立連接時對應至埠。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-132">In the case of a WAN interface, the interface is mapped to a port at the time a connection is established.</span></span> <span data-ttu-id="dd1b5-133">埠可以是 COM 埠、平行埠或虛擬埠 (用於通道，例如 PPTP 和 L2TP) 。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-133">The port could be a COM port, a parallel port or a virtual port (for tunnels such as PPTP and L2TP).</span></span>

<span data-ttu-id="dd1b5-134">WAN 介面具有額外的品質，通常只會在建立連線時接收網路位址。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-134">WAN interfaces have the additional quality that they typically receive a network address only at the time that a connection is established.</span></span> <span data-ttu-id="dd1b5-135">例如，使用 PPP 的 WAN 介面會在連線過程中從遠端對等端接收其網路層位址。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-135">For example, a WAN interface using PPP receives its network layer address from the remote peer during the connection process.</span></span> <span data-ttu-id="dd1b5-136">在連接過程中接收網路位址有時稱為 *晚期繫結*。</span><span class="sxs-lookup"><span data-stu-id="dd1b5-136">Receiving a network address as part of the connection process is sometimes referred to as *late-binding*.</span></span>

 

 




