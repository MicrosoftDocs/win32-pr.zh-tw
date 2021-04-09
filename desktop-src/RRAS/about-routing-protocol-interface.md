---
title: 關於路由通訊協定介面
description: 下列檔說明如何將協力廠商路由通訊協定整合到 (RRAS) 的「路由及遠端存取」服務。
ms.assetid: 593e3b8a-6f26-47c6-aa93-520d36db7a6f
keywords:
- 路由及遠端存取服務 RRAS，路由通訊協定介面
- 路由及遠端存取服務 RRAS，路由通訊協定介面，說明
- 路由通訊協定介面 RRAS
- 路由通訊協定介面 RRAS，說明
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bc663f249ca42ebbae509c164a828d603a9b968
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674092"
---
# <a name="about-routing-protocol-interface"></a><span data-ttu-id="5eee4-107">關於路由通訊協定介面</span><span class="sxs-lookup"><span data-stu-id="5eee4-107">About Routing Protocol Interface</span></span>

<span data-ttu-id="5eee4-108">下列檔說明如何將協力廠商路由通訊協定整合到 (RRAS) 的「路由及遠端存取」服務。</span><span class="sxs-lookup"><span data-stu-id="5eee4-108">The following documentation describes the integration of third-party routing protocols into the Routing and Remote Access Service (RRAS).</span></span> <span data-ttu-id="5eee4-109">RRAS 是 Windows 的一項功能，可做為多通訊協定路由器。</span><span class="sxs-lookup"><span data-stu-id="5eee4-109">RRAS is a feature of Windows that acts as a multi-protocol router.</span></span> <span data-ttu-id="5eee4-110">RRAS 會定義路由器管理員和路由通訊協定之間的介面。</span><span class="sxs-lookup"><span data-stu-id="5eee4-110">RRAS defines the interface between the router manager and the routing protocol.</span></span> <span data-ttu-id="5eee4-111">路由通訊協定是在動態連結程式庫中執行， (DLL) 。</span><span class="sxs-lookup"><span data-stu-id="5eee4-111">The routing protocol is implemented in a dynamic link library (DLL).</span></span>

<span data-ttu-id="5eee4-112">使用此介面可將路由通訊協定（例如 IGRP、NLSP 和 BGP）作為使用 RRAS 的使用者模式 Dll 來執行。</span><span class="sxs-lookup"><span data-stu-id="5eee4-112">Use this interface to implement routing protocols, such as IGRP, NLSP, and BGP, as user-mode DLLs that work with RRAS.</span></span>

<span data-ttu-id="5eee4-113">本檔將說明下列主題：</span><span class="sxs-lookup"><span data-stu-id="5eee4-113">This documentation describes the following topics:</span></span>

-   [<span data-ttu-id="5eee4-114">配接器</span><span class="sxs-lookup"><span data-stu-id="5eee4-114">Adapters</span></span>](adapters.md)
-   [<span data-ttu-id="5eee4-115">介面</span><span class="sxs-lookup"><span data-stu-id="5eee4-115">Interfaces</span></span>](interfaces.md)
-   [<span data-ttu-id="5eee4-116">靜態和 Autostatic 路由</span><span class="sxs-lookup"><span data-stu-id="5eee4-116">Static and Autostatic Routes</span></span>](static-and-autostatic-routes.md)

 

 




