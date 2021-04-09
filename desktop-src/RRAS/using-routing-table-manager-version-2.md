---
title: 使用路由表管理員第2版
description: 在您開始開發使用 RTMv2 Api 的用戶端之前，請先參閱 RTMv2 程式設計問題。
ms.assetid: c0187b65-3cb2-4ab0-8d5f-ca37e8bc0ad7
keywords:
- 路由及遠端存取服務 RRAS，路由表管理員第2版，工作
- 路由表管理員第2版 RRAS，工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29bc7acab213325a0683de215995eeb2f635b102
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932318"
---
# <a name="using-routing-table-manager-version-2"></a><span data-ttu-id="01461-105">使用路由表管理員第2版</span><span class="sxs-lookup"><span data-stu-id="01461-105">Using Routing Table Manager Version 2</span></span>

<span data-ttu-id="01461-106">在您開始開發使用 RTMv2 Api 的用戶端之前，請先參閱 [RTMv2 程式設計問題](rtmv2-programming-issues.md)。</span><span class="sxs-lookup"><span data-stu-id="01461-106">Before you begin developing clients that use the RTMv2 APIs, review the [RTMv2 Programming Issues](rtmv2-programming-issues.md).</span></span>

<span data-ttu-id="01461-107">本節包含開發用戶端（例如路由通訊協定）時可使用的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="01461-107">This section contains sample code that can be used when developing clients such as routing protocols.</span></span>

-   [<span data-ttu-id="01461-108">RTMv2 程式設計問題</span><span class="sxs-lookup"><span data-stu-id="01461-108">RTMv2 Programming Issues</span></span>](rtmv2-programming-issues.md)
-   [<span data-ttu-id="01461-109">向路由表管理員註冊</span><span class="sxs-lookup"><span data-stu-id="01461-109">Register with the Routing Table Manager</span></span>](register-with-the-routing-table-manager.md)
-   [<span data-ttu-id="01461-110">列舉已註冊的實體</span><span class="sxs-lookup"><span data-stu-id="01461-110">Enumerate the Registered Entities</span></span>](enumerate-the-registered-entities.md)
-   [<span data-ttu-id="01461-111">取得並呼叫用戶端的匯出方法</span><span class="sxs-lookup"><span data-stu-id="01461-111">Obtain and Call the Exported Methods for a Client</span></span>](obtain-and-call-the-exported-methods-for-a-client.md)
-   [<span data-ttu-id="01461-112">註冊變更通知</span><span class="sxs-lookup"><span data-stu-id="01461-112">Register for Change Notification</span></span>](register-for-change-notification.md)
-   [<span data-ttu-id="01461-113">使用 RtmAddRouteToDest 新增和更新路由</span><span class="sxs-lookup"><span data-stu-id="01461-113">Add and Update Routes Using RtmAddRouteToDest</span></span>](add-and-update-routes-using-rtmaddroutetodest.md)
-   [<span data-ttu-id="01461-114">使用 RtmUpdateAndUnlockRoute 就地更新路由</span><span class="sxs-lookup"><span data-stu-id="01461-114">Update a Route In Place Using RtmUpdateAndUnlockRoute</span></span>](update-a-route-in-place-using-rtmupdateandunlockroute.md)
-   [<span data-ttu-id="01461-115">使用路由 Hold-Down 狀態</span><span class="sxs-lookup"><span data-stu-id="01461-115">Use the Route Hold-Down State</span></span>](use-the-route-hold-down-state.md)
-   [<span data-ttu-id="01461-116">列舉所有目的地</span><span class="sxs-lookup"><span data-stu-id="01461-116">Enumerate All Destinations</span></span>](enumerate-all-destinations.md)
-   [<span data-ttu-id="01461-117">列舉所有路由</span><span class="sxs-lookup"><span data-stu-id="01461-117">Enumerate All Routes</span></span>](enumerate-all-routes.md)
-   [<span data-ttu-id="01461-118">搜尋最佳路線</span><span class="sxs-lookup"><span data-stu-id="01461-118">Search for the Best Route</span></span>](search-for-the-best-route.md)
-   [<span data-ttu-id="01461-119">使用前置詞樹狀目錄搜尋路由</span><span class="sxs-lookup"><span data-stu-id="01461-119">Search for Routes Using a Prefix Tree</span></span>](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md)
-   [<span data-ttu-id="01461-120">存取目的地中的不透明指標</span><span class="sxs-lookup"><span data-stu-id="01461-120">Access the Opaque Pointer in a Destination</span></span>](access-the-opaque-pointer-in-a-destination.md)
-   [<span data-ttu-id="01461-121">使用 Client-Specific 路由清單</span><span class="sxs-lookup"><span data-stu-id="01461-121">Use a Client-Specific Route List</span></span>](use-a-client-specific-route-list.md)
-   [<span data-ttu-id="01461-122">使用事件通知回呼</span><span class="sxs-lookup"><span data-stu-id="01461-122">Use the Event Notification Callback</span></span>](use-the-event-notification-callback.md)

 

 




