---
title: 路由表管理員
description: 路由表管理員是路由資訊的中央存放庫，適用于在 [路由及遠端存取服務] (RRAS) 下運作的所有路由通訊協定。
ms.assetid: 7b01704e-c1fb-40e3-89cf-1206fdf9fd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98094eb34c8575e0c24854813fc7458c98749568
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966177"
---
# <a name="routing-table-manager"></a><span data-ttu-id="6af09-103">路由表管理員</span><span class="sxs-lookup"><span data-stu-id="6af09-103">Routing Table Manager</span></span>

<span data-ttu-id="6af09-104">路由表管理員是路由資訊的中央存放庫，適用于在 [路由及遠端存取服務] (RRAS) 下運作的所有路由通訊協定。</span><span class="sxs-lookup"><span data-stu-id="6af09-104">The routing table manager is the central repository of routing information for all routing protocols that operate under the Routing and Remote Access Service (RRAS).</span></span> <span data-ttu-id="6af09-105">它會在發生變更時通知用戶端，並允許用戶端交換私用資訊。</span><span class="sxs-lookup"><span data-stu-id="6af09-105">It notifies clients when changes have occurred, and allows clients to exchange private information.</span></span>

<span data-ttu-id="6af09-106">路由表管理員會提供路由資訊給所有感興趣的用戶端，例如路由通訊協定、管理程式和監視程式。</span><span class="sxs-lookup"><span data-stu-id="6af09-106">The routing table manager provides routing information to all interested clients, such as routing protocols, management programs, and monitoring programs.</span></span> <span data-ttu-id="6af09-107">路由表管理員也會決定路由通訊協定已知的每個目的地網路的最佳路由。</span><span class="sxs-lookup"><span data-stu-id="6af09-107">The routing table manager also determines the best route to each destination network that is known to the routing protocols.</span></span> <span data-ttu-id="6af09-108">路由表管理員會根據路由通訊協定優先順序以及與路由相關聯的計量來決定此路由。</span><span class="sxs-lookup"><span data-stu-id="6af09-108">The routing table manager determines this route based on routing protocol priorities and on the metrics associated with the routes.</span></span> <span data-ttu-id="6af09-109">管理路由器的人員可以使用 RRAS 管理主控台設定路由通訊協定優先順序。</span><span class="sxs-lookup"><span data-stu-id="6af09-109">The person administering the router can configure routing protocol priorities using the RRAS management console.</span></span>

<span data-ttu-id="6af09-110">路由表管理員會將最佳路由資訊傳遞至轉寄站 (每個位址系列，或每個介面) 和所有感興趣用戶端的轉寄站。</span><span class="sxs-lookup"><span data-stu-id="6af09-110">The routing table manager passes the best-route information to the forwarders (one per address family, or one per interface) and to all interested clients.</span></span>

<span data-ttu-id="6af09-111">每個用戶端都會使用路由表管理員進行註冊，而傳回的會接收用戶端用來新增或刪除路由的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6af09-111">Each client registers with the routing table manager, and in return receives a handle that the client uses to add or delete routes.</span></span> <span data-ttu-id="6af09-112">用戶端可以取出儲存在路由表中的資訊。</span><span class="sxs-lookup"><span data-stu-id="6af09-112">Clients can retrieve information stored in the routing table.</span></span> <span data-ttu-id="6af09-113">此外，用戶端可以向路由表管理員註冊，以接收目的地最佳路由變更的通知。</span><span class="sxs-lookup"><span data-stu-id="6af09-113">Additionally, clients can register with the routing table manager to receive notification of changes to the best route to a destination.</span></span>

 

 




