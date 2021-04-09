---
title: 關於路由表管理員第2版
description: 下列檔說明路由表管理員第2版 (RTMv2) 技術。
ms.assetid: 9f84863e-45ed-49d1-8df4-3b59b1b5f3c9
keywords:
- 路由及遠端存取服務 RRAS，路由表管理員第2版
- 路由及遠端存取服務 RRAS，路由表管理員第2版，描述
- 路由表管理員第2版 RRAS
- 路由表管理員第2版 RRAS，說明
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5014dc894c4a517bfdfac8478e520658a4987d4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021570"
---
# <a name="about-routing-table-manager-version-2"></a><span data-ttu-id="28078-107">關於路由表管理員第2版</span><span class="sxs-lookup"><span data-stu-id="28078-107">About Routing Table Manager Version 2</span></span>

<span data-ttu-id="28078-108">下列檔說明路由表管理員第2版 (RTMv2) 技術。</span><span class="sxs-lookup"><span data-stu-id="28078-108">The following documentation describes the Routing Table Manager Version 2 (RTMv2) technology.</span></span> <span data-ttu-id="28078-109">RTMv2 API 是 Windows 2000 和更新版本作業系統的一項功能，可用來撰寫與路由表管理員互動的路由通訊協定。</span><span class="sxs-lookup"><span data-stu-id="28078-109">The RTMv2 API is a feature of Windows 2000 and later operating systems that you can use to write routing protocols that interact with the routing table manager.</span></span>

<span data-ttu-id="28078-110">路由表管理員是路由資訊的中央存放庫，適用于在 [路由及遠端存取服務] (RRAS) 下運作的所有路由通訊協定。</span><span class="sxs-lookup"><span data-stu-id="28078-110">The routing table manager is the central repository of routing information for all routing protocols that operate under the Routing and Remote Access Service (RRAS).</span></span>

<span data-ttu-id="28078-111">Windows NT 4.0 版無法使用 RTMv2。</span><span class="sxs-lookup"><span data-stu-id="28078-111">RTMv2 is not available for Windows NT version 4.0.</span></span> <span data-ttu-id="28078-112">此外，RTMv2 不能用於在 Windows NT 4.0 或 Windows 2000 上執行的 IPX 路由通訊協定。</span><span class="sxs-lookup"><span data-stu-id="28078-112">Additionally, RTMv2 cannot be used for IPX routing protocols that run on Windows NT 4.0 or Windows 2000.</span></span> <span data-ttu-id="28078-113">如果您使用的是 IPX 或正在撰寫 Windows NT 4.0 的路由通訊協定，請參閱 [關於路由表管理員第1版](about-routing-table-manager-version-1.md)。</span><span class="sxs-lookup"><span data-stu-id="28078-113">If you are using IPX or writing routing protocols for Windows NT 4.0, please refer to [About Routing Table Manager Version 1](about-routing-table-manager-version-1.md).</span></span>

<span data-ttu-id="28078-114">本總覽將說明下列主題：</span><span class="sxs-lookup"><span data-stu-id="28078-114">This overview describes the following topics:</span></span>

-   [<span data-ttu-id="28078-115">路由表管理員架構的元件</span><span class="sxs-lookup"><span data-stu-id="28078-115">Components of the Routing Table Manager Architecture</span></span>](components-of-the-routing-table-manager-architecture.md)
-   [<span data-ttu-id="28078-116">向路由表管理員註冊</span><span class="sxs-lookup"><span data-stu-id="28078-116">Registering with the Routing Table Manager</span></span>](registering-with-the-routing-table-manager.md)
-   [<span data-ttu-id="28078-117">列舉已註冊的實體</span><span class="sxs-lookup"><span data-stu-id="28078-117">Enumerating Registered Entities</span></span>](enumerating-registered-entities.md)
-   [<span data-ttu-id="28078-118">使用方法</span><span class="sxs-lookup"><span data-stu-id="28078-118">Using Methods</span></span>](using-methods.md)
-   [<span data-ttu-id="28078-119">使用不透明的指標</span><span class="sxs-lookup"><span data-stu-id="28078-119">Using Opaque Pointers</span></span>](using-opaque-pointers.md)
-   [<span data-ttu-id="28078-120">標示 Hold-Down 狀態的路由</span><span class="sxs-lookup"><span data-stu-id="28078-120">Marking Routes for the Hold-Down State</span></span>](marking-routes-for-the-hold-down-state.md)
-   [<span data-ttu-id="28078-121">新增路由</span><span class="sxs-lookup"><span data-stu-id="28078-121">Adding Routes</span></span>](adding-routes.md)
-   [<span data-ttu-id="28078-122">正在抓取路由資訊</span><span class="sxs-lookup"><span data-stu-id="28078-122">Retrieving Route Information</span></span>](retrieving-route-information.md)
-   [<span data-ttu-id="28078-123">更新路由</span><span class="sxs-lookup"><span data-stu-id="28078-123">Updating Routes</span></span>](updating-routes.md)
-   [<span data-ttu-id="28078-124">接收變更的通知</span><span class="sxs-lookup"><span data-stu-id="28078-124">Receiving Notification of Changes</span></span>](receiving-notification-of-changes.md)
-   [<span data-ttu-id="28078-125">使用下一個躍點</span><span class="sxs-lookup"><span data-stu-id="28078-125">Working with Next Hops</span></span>](working-with-next-hops.md)
-   [<span data-ttu-id="28078-126">列舉路由表專案</span><span class="sxs-lookup"><span data-stu-id="28078-126">Enumerating Routing Table Entries</span></span>](enumerating-routing-table-entries.md)
-   [<span data-ttu-id="28078-127">尋找路由表中的特定資訊</span><span class="sxs-lookup"><span data-stu-id="28078-127">Finding Specific Information in the Routing Table</span></span>](finding-specific-information-in-the-routing-table.md)
-   [<span data-ttu-id="28078-128">維護 Client-Specific 清單</span><span class="sxs-lookup"><span data-stu-id="28078-128">Maintaining Client-Specific Lists</span></span>](maintaining-client-specific-lists.md)
-   [<span data-ttu-id="28078-129">管理控制碼</span><span class="sxs-lookup"><span data-stu-id="28078-129">Managing Handles</span></span>](managing-handles.md)

 

 




