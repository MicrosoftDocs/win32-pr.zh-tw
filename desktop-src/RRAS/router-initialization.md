---
title: 路由器初始化
description: 路由器、路由器管理員和路由通訊協定/用戶端的設定資訊會劃分為全域資訊和每個介面資訊，並且儲存在登錄和路由器的電話簿檔案（node.js）中。
ms.assetid: c54541c1-6508-448a-a211-5fca634a184a
keywords:
- 路由器 RRAS，初始化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f4d45c10ef7b44b6dfe9d2d84149c77c81c5752
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103670899"
---
# <a name="router-initialization"></a><span data-ttu-id="15420-104">路由器初始化</span><span class="sxs-lookup"><span data-stu-id="15420-104">Router Initialization</span></span>

<span data-ttu-id="15420-105">路由器、路由器管理員和路由通訊協定/用戶端的設定資訊會劃分為全域資訊和每個介面資訊，並且儲存在登錄和路由器的電話簿檔案（node.js）中。</span><span class="sxs-lookup"><span data-stu-id="15420-105">Configuration information for the router, the router managers and the routing protocols/clients is divided into global information and per interface information and is stored in the registry and the router's phone-book file, Router.pbk.</span></span>

<span data-ttu-id="15420-106">當路由器進程啟動時，DIM (動態介面管理員) 從登錄讀取路由器設定。</span><span class="sxs-lookup"><span data-stu-id="15420-106">When the router process starts, DIM (Dynamic Interface Manager) reads the router configuration from the registry.</span></span> <span data-ttu-id="15420-107">DIM 會建立介面資訊所指定的介面。</span><span class="sxs-lookup"><span data-stu-id="15420-107">DIM creates the interfaces that are specified by the interface information.</span></span>

<span data-ttu-id="15420-108">DIM 也會捕獲全域路由器管理員資訊。</span><span class="sxs-lookup"><span data-stu-id="15420-108">DIM also retrieves the global router manager information.</span></span> <span data-ttu-id="15420-109">DIM 會啟動對應至此資訊的路由器管理員，並將資訊傳遞給它們。</span><span class="sxs-lookup"><span data-stu-id="15420-109">DIM starts the router managers that correspond to this information, and passes them the information.</span></span> <span data-ttu-id="15420-110">例如，如果 DIM 在登錄中找到 IP 路由器管理員的全域資訊，則 DIM 會啟動 IP 路由器管理員，並將全域資訊傳遞給它。</span><span class="sxs-lookup"><span data-stu-id="15420-110">For example, if DIM finds global information for the IP router manager in the registry, DIM starts the IP router manager and passes it the global information.</span></span> <span data-ttu-id="15420-111">如果特定路由器管理員的登錄中沒有任何全域資訊，則 DIM 不會啟動該路由器管理員。</span><span class="sxs-lookup"><span data-stu-id="15420-111">If no global information is present in the registry for a particular router manager, DIM does not start that router manager.</span></span>

<span data-ttu-id="15420-112">路由器管理員會檢查從 DIM 接收的全域資訊。</span><span class="sxs-lookup"><span data-stu-id="15420-112">The router managers examine the global information received from DIM.</span></span> <span data-ttu-id="15420-113">如果路由器管理員在全域資訊中找到特定用戶端的特定資訊，則路由器管理員會載入用戶端的 DLL (例如 IpNAT.dll) ，並藉由呼叫用戶端的 [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol) 和 [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) 函式來初始化用戶端。</span><span class="sxs-lookup"><span data-stu-id="15420-113">If the router manager finds information specific to a particular client within the global information, the router manager loads the DLL for the client (for example IpNAT.dll) and initializes the client by calling the client's [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol) and [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) functions.</span></span> <span data-ttu-id="15420-114">路由器管理員會在呼叫 [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol)時，將用戶端特定的全域資訊傳遞給用戶端。</span><span class="sxs-lookup"><span data-stu-id="15420-114">The router manager passes the client-specific global information to the client in the call to [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol).</span></span>

<span data-ttu-id="15420-115">在每個階段，傳遞給下一個實體的資訊對其前面的實體而言是不透明的。</span><span class="sxs-lookup"><span data-stu-id="15420-115">At each stage, the information being passed to the next entity is opaque to the entity preceding it.</span></span> <span data-ttu-id="15420-116">也就是說，DIM 不會解讀 IP 路由器管理員的全域資訊，而是要讓 IP 路由器管理員知道這項資訊。</span><span class="sxs-lookup"><span data-stu-id="15420-116">That is, DIM does not interpret the global information for the IP Router Manager, beyond the fact that the information is meant for the IP Router Manager.</span></span> <span data-ttu-id="15420-117">同樣地，「IP 路由器管理員」並不會解讀 OSPF 的特定資訊，因為它是 OSPF 資訊。</span><span class="sxs-lookup"><span data-stu-id="15420-117">Similarly, the IP Router Manager does not interpret the OSPF specific information beyond the fact that it is OSPF information.</span></span>

 

 




