---
title: 路由及遠端存取服務架構
description: 下圖顯示 Windows 2000 路由器的一般架構觀點。
ms.assetid: 599435e2-e2f3-4632-8a79-441172aacf13
keywords:
- 路由及遠端存取服務 RRAS、路由及遠端存取服務架構 RRAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3e72f7c61bc9cb558b020c3470718a7f419c04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462344"
---
# <a name="routing-and-remote-access-services-architecture"></a><span data-ttu-id="196f6-104">路由及遠端存取服務架構</span><span class="sxs-lookup"><span data-stu-id="196f6-104">Routing and Remote Access Services Architecture</span></span>

<span data-ttu-id="196f6-105">下圖顯示 Windows 2000 路由器的一般架構觀點。</span><span class="sxs-lookup"><span data-stu-id="196f6-105">The following illustration presents a general architectural view of the Windows 2000 router.</span></span>

<span data-ttu-id="196f6-106">IP 通訊協定系列特定的元件會以淺灰色顯示。</span><span class="sxs-lookup"><span data-stu-id="196f6-106">Components that are specific to the IP protocol family are shown in light gray.</span></span> <span data-ttu-id="196f6-107">IPX 通訊協定系列特定的元件會以暗灰色顯示。</span><span class="sxs-lookup"><span data-stu-id="196f6-107">Components that are specific to the IPX protocol family are shown in dark gray.</span></span> <span data-ttu-id="196f6-108">所有通訊協定系列通用的元件都是 unshaded。</span><span class="sxs-lookup"><span data-stu-id="196f6-108">Components that are general to all protocol families are unshaded.</span></span>

<span data-ttu-id="196f6-109">「路由及遠端存取」服務提供用來管理和設定服務的 Api。</span><span class="sxs-lookup"><span data-stu-id="196f6-109">The Routing and Remote Access Service provides APIs for administering and configuring the service.</span></span> <span data-ttu-id="196f6-110">這些 Api 包括 IP 和 IPX 的 SNMP 代理程式。</span><span class="sxs-lookup"><span data-stu-id="196f6-110">These APIs include SNMP agents for both IP and IPX.</span></span>

<span data-ttu-id="196f6-111">RRAS 包含 IP 和 IPX 的路由通訊協定。</span><span class="sxs-lookup"><span data-stu-id="196f6-111">RRAS includes routing protocols for both IP and IPX.</span></span> <span data-ttu-id="196f6-112">針對 IP，RRAS 會提供路由資訊通訊協定 (RIP) 和開放式最短路徑 First (OSPF) 路由通訊協定。</span><span class="sxs-lookup"><span data-stu-id="196f6-112">For IP, RRAS provides the Routing Information Protocol (RIP) and Open Shortest Path First (OSPF) routing protocols.</span></span> <span data-ttu-id="196f6-113">針對 IPX，RRAS 提供 (SAP) 的 IPX RIP 和服務廣告通訊協定。</span><span class="sxs-lookup"><span data-stu-id="196f6-113">For IPX, RRAS provides IPX RIP and Service Advertising Protocol (SAP).</span></span>

<span data-ttu-id="196f6-114">RRAS 會針對 IP 和 IPX 使用一個路由表管理員 (RTM) 。</span><span class="sxs-lookup"><span data-stu-id="196f6-114">RRAS uses one Routing Table Manager (RTM) for both IP and IPX.</span></span> <span data-ttu-id="196f6-115">不過，每個通訊協定系列都有自己的路由器管理員。</span><span class="sxs-lookup"><span data-stu-id="196f6-115">However, each protocol family has its own Router Manager.</span></span> <span data-ttu-id="196f6-116">RRAS 也有個別的元件，可用於管理多播群組。</span><span class="sxs-lookup"><span data-stu-id="196f6-116">RRAS also has separate component for managing Multicast Groups.</span></span>

<span data-ttu-id="196f6-117">動態介面管理員 (將) 介面與 PPP 和 TAPI 服務互動，以便管理某些路由所使用的 PPP 介面。</span><span class="sxs-lookup"><span data-stu-id="196f6-117">The Dynamic Interface Manager (DIM) interfaces with PPP and TAPI services in order to manage PPP interfaces used by some routes.</span></span>

![windows 2000 路由器的一般架構視圖](images/rtarch.png)

 

 




