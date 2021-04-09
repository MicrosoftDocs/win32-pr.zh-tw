---
title: 靜態和 Autostatic 路由
description: 通常會透過路由通訊協定動態取得遠端網路的路由。
ms.assetid: af2f2039-8131-4ca9-98bf-6aeb7a511034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3faa8931e0fee5c75f598b920b7b97a1e0e829d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932495"
---
# <a name="static-and-autostatic-routes"></a><span data-ttu-id="c8ec5-103">靜態和 Autostatic 路由</span><span class="sxs-lookup"><span data-stu-id="c8ec5-103">Static and Autostatic Routes</span></span>

<span data-ttu-id="c8ec5-104">通常會透過路由通訊協定動態取得遠端網路的路由。</span><span class="sxs-lookup"><span data-stu-id="c8ec5-104">Typically, routes to remote networks are obtained dynamically through routing protocols.</span></span> <span data-ttu-id="c8ec5-105">不過，系統管理員也可以藉由手動提供路由來 *植* 入路由表。</span><span class="sxs-lookup"><span data-stu-id="c8ec5-105">However, the administrator can also *seed* the routing table by providing routes manually.</span></span> <span data-ttu-id="c8ec5-106">這些路由稱為 *靜態*。</span><span class="sxs-lookup"><span data-stu-id="c8ec5-106">These routes are referred to as *static*.</span></span> <span data-ttu-id="c8ec5-107">靜態路由與代表遠端網路的介面相關聯。</span><span class="sxs-lookup"><span data-stu-id="c8ec5-107">A static route is associated with an interface that represents the remote network.</span></span> <span data-ttu-id="c8ec5-108">與動態路由不同的是，即使重新開機路由器或停用介面，仍會保留靜態路由。</span><span class="sxs-lookup"><span data-stu-id="c8ec5-108">Unlike dynamic routes, static routes are retained even if the router is restarted or the interface is disabled.</span></span>

<span data-ttu-id="c8ec5-109">*Autostatic* 路由是透過路由通訊協定取得的，但取得的行為就像靜態路由一樣。</span><span class="sxs-lookup"><span data-stu-id="c8ec5-109">An *autostatic* route is obtained through a routing protocol, but once obtained behaves like a static route.</span></span> <span data-ttu-id="c8ec5-110">取得 autostatic 路由的程式如下所示： IP 或 IPX 路由器管理員發出要求，指出路由通訊協定會更新特定介面的路由資訊。</span><span class="sxs-lookup"><span data-stu-id="c8ec5-110">The process for obtaining autostatic routes is as follows: The IP or IPX router manager issues a request that a routing protocol update the routing information for a specific interface.</span></span> <span data-ttu-id="c8ec5-111">然後更新的結果會轉換成靜態路由。</span><span class="sxs-lookup"><span data-stu-id="c8ec5-111">The results of the update are then converted into static routes.</span></span> <span data-ttu-id="c8ec5-112">請注意，只有特定路由通訊協定支援 autostatic 路由更新的要求。</span><span class="sxs-lookup"><span data-stu-id="c8ec5-112">Note that only certain routing protocols support requests for autostatic route updates.</span></span>

 

 




