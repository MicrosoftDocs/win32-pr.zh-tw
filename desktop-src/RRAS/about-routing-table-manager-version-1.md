---
title: 關於路由表管理員第1版
description: 路由表管理員是路由資訊的中央存放庫，適用于在 [路由及遠端存取服務] (RRAS) 下運作的所有路由通訊協定。
ms.assetid: 6d0e7697-5c52-4a69-b2a1-9c893600191b
keywords:
- 路由及遠端存取服務 RRAS，路由表管理員第1版
- 路由及遠端存取服務 RRAS，路由表管理員第1版，描述
- 路由表管理員第1版 RRAS
- 路由表管理員第1版 RRAS，說明
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b99f913230db6e6882a36b414914c3924181a221
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021571"
---
# <a name="about-routing-table-manager-version-1"></a><span data-ttu-id="e8ce5-107">關於路由表管理員第1版</span><span class="sxs-lookup"><span data-stu-id="e8ce5-107">About Routing Table Manager Version 1</span></span>

<span data-ttu-id="e8ce5-108">**Windows Server 2003：** 此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。</span><span class="sxs-lookup"><span data-stu-id="e8ce5-108">**Windows Server 2003:** This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="e8ce5-109">新的應用程式應該使用路由表管理員第2版 API。</span><span class="sxs-lookup"><span data-stu-id="e8ce5-109">New applications should use the Routing Table Manager Version 2 API.</span></span>

<span data-ttu-id="e8ce5-110">路由表管理員是路由資訊的中央存放庫，適用于在 [路由及遠端存取服務] (RRAS) 下運作的所有路由通訊協定。</span><span class="sxs-lookup"><span data-stu-id="e8ce5-110">The routing table manager is a central repository of routing information for all routing protocols that operate under Routing and Remote Access Service (RRAS).</span></span> <span data-ttu-id="e8ce5-111">路由表管理員會提供路由資訊給所有感興趣的元件，例如路由通訊協定、管理代理程式和監視代理程式。</span><span class="sxs-lookup"><span data-stu-id="e8ce5-111">The routing table manager provides routing information to all interested components, such as routing protocols, management agents, and monitoring agents.</span></span> <span data-ttu-id="e8ce5-112">路由表管理員也會決定路由通訊協定已知的每個目的地網路的最佳路由。</span><span class="sxs-lookup"><span data-stu-id="e8ce5-112">The routing table manager also determines the best route to each destination network known to the routing protocols.</span></span> <span data-ttu-id="e8ce5-113">它會根據路由通訊協定優先順序以及與路由相關聯的計量來決定此路由。</span><span class="sxs-lookup"><span data-stu-id="e8ce5-113">It determines this route based on routing protocol priorities and on metrics associated with the routes.</span></span> <span data-ttu-id="e8ce5-114">請注意，系統管理員可以設定路由通訊協定優先順序。</span><span class="sxs-lookup"><span data-stu-id="e8ce5-114">Note that the administrator is able to configure routing protocol priorities.</span></span> <span data-ttu-id="e8ce5-115">路由表管理員接著會將最佳路由資訊傳遞至轉寄站，並傳回路由通訊協定。</span><span class="sxs-lookup"><span data-stu-id="e8ce5-115">The routing table manager then passes the best-route information on to the forwarders and back to the routing protocols.</span></span>

<span data-ttu-id="e8ce5-116">每個路由通訊協定都會呼叫 [**RtmRegisterClient**](rtmregisterclient.md) 來向路由表管理員註冊。</span><span class="sxs-lookup"><span data-stu-id="e8ce5-116">Each routing protocol calls [**RtmRegisterClient**](rtmregisterclient.md) to register with the routing table manager.</span></span> <span data-ttu-id="e8ce5-117">**RtmRegisterClient** 會傳回路由通訊協定用來新增或刪除路由專案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e8ce5-117">**RtmRegisterClient** returns a handle that is used by the routing protocol to add or delete route entries.</span></span> <span data-ttu-id="e8ce5-118">**RtmRegisterClient** 也可讓路由通訊協定向路由表管理員註冊事件物件。</span><span class="sxs-lookup"><span data-stu-id="e8ce5-118">**RtmRegisterClient** also allows the routing protocol to register an event object with the routing table manager.</span></span> <span data-ttu-id="e8ce5-119">路由表管理員會通知此事件物件，以通知路由通訊協定中的最佳路由資訊變更。</span><span class="sxs-lookup"><span data-stu-id="e8ce5-119">The routing table manager signals this event object to notify the routing protocol of changes in best-route information.</span></span> <span data-ttu-id="e8ce5-120">所有其他元件都可以透過路由列舉來取得路由表管理員中儲存的資訊。</span><span class="sxs-lookup"><span data-stu-id="e8ce5-120">All other components can obtain information stored in the routing table manager through route enumeration.</span></span>

 

 




