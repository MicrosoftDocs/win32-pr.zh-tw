---
title: 命名的要求佇列
description: 命名的要求佇列
ms.assetid: d0686a9b-fc3d-4b69-b083-d04b35ce5b50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4aca045f84fe9f9e4b57365ba8831456f2dc1ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311096"
---
# <a name="named-request-queue"></a><span data-ttu-id="908db-103">命名的要求佇列</span><span class="sxs-lookup"><span data-stu-id="908db-103">Named Request Queue</span></span>

<span data-ttu-id="908db-104">名為「要求佇列」功能的 HTTP Server 2.0 版 API 可讓多個應用程式在不同的進程和使用者帳戶下運作，以存取要求佇列。</span><span class="sxs-lookup"><span data-stu-id="908db-104">The HTTP Server version 2.0 API named request queue feature allows multiple applications, operating under separate processes and user accounts, access to the request queue.</span></span> <span data-ttu-id="908db-105">要求佇列是依名稱開啟，並使用存取控制清單 (Acl) 來確保應用程式無法存取其他資料。</span><span class="sxs-lookup"><span data-stu-id="908db-105">The request queue is opened by name, and secured using Access Control Lists (ACLs) to ensure that applications are not able to access each others data.</span></span> <span data-ttu-id="908db-106">單一進程會建立要求佇列，並將許可權授與其他進程，以使用要求佇列。</span><span class="sxs-lookup"><span data-stu-id="908db-106">A single process creates the request queue, and grants permission to other processes to use the request queue.</span></span> <span data-ttu-id="908db-107">因此，電腦上的其他進程會使用服務要求所需的最低許可權來存取要求佇列。</span><span class="sxs-lookup"><span data-stu-id="908db-107">Thus, other processes on the computer access the request queue with the least privilege necessary to service requests.</span></span> <span data-ttu-id="908db-108">當應用程式在最低許可權下執行時，HTTP 服務可能會損毀，因為協力廠商程式碼中的弱點會降至最低。</span><span class="sxs-lookup"><span data-stu-id="908db-108">Possible damage to the HTTP service, due to vulnerabilities in third party code, is minimized when applications are running under least privileges.</span></span>

<span data-ttu-id="908db-109">已命名的要求佇列是使用 [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) 函式所建立。</span><span class="sxs-lookup"><span data-stu-id="908db-109">The named request queue is created with the [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) function.</span></span> <span data-ttu-id="908db-110">建立要求佇列時，應用程式會在 *pSecurityAttribute* 參數中指定 ACL。</span><span class="sxs-lookup"><span data-stu-id="908db-110">When the request queue is created, the application specifies the ACL in the *pSecurityAttribute* parameter.</span></span> <span data-ttu-id="908db-111">只有在建立要求佇列時才能設定 ACL，可讓工作者進程開啟要求佇列、接收要求和傳送回應。</span><span class="sxs-lookup"><span data-stu-id="908db-111">The ACL, which can only be set when the request queue is created, allows worker processes to open the request queue, receive requests, and send responses.</span></span> <span data-ttu-id="908db-112">依預設，除非已在 ACL 中授與許可權，否則不允許處理常式開啟要求佇列。</span><span class="sxs-lookup"><span data-stu-id="908db-112">By default, processes are not allowed to open a request queue unless they have been granted permission in the ACL.</span></span> <span data-ttu-id="908db-113">應用程式不需要系統管理許可權，就能建立要求佇列。</span><span class="sxs-lookup"><span data-stu-id="908db-113">Applications do not require administrative privileges to create the request queue.</span></span>

<span data-ttu-id="908db-114">您必須使用 [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue)的 *pName* 參數中所指定的名稱來建立要求佇列，以供其他進程開啟要求佇列。</span><span class="sxs-lookup"><span data-stu-id="908db-114">The request queue must be created with a name specified in the *pName* parameter of [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) for other processes to open the request queue.</span></span> <span data-ttu-id="908db-115">如果 *pName* 為 **Null**，則會建立未命名的要求佇列，而且沒有其他進程可以開啟它。</span><span class="sxs-lookup"><span data-stu-id="908db-115">If *pName* is **NULL**, an unnamed request queue is created and no other processes can open it.</span></span>

## <a name="creator-and-controller-processes"></a><span data-ttu-id="908db-116">建立者與控制器進程</span><span class="sxs-lookup"><span data-stu-id="908db-116">Creator and Controller Processes</span></span>

<span data-ttu-id="908db-117">建立要求佇列時，應用程式可以將它開啟為控制器進程或建立者進程。</span><span class="sxs-lookup"><span data-stu-id="908db-117">When the request queue is created, the application can open it as a controller process or a creator process.</span></span> <span data-ttu-id="908db-118">控制器和建立者程式都是做為要求佇列的系統管理員，但控制器不會在其上執行 i/o 作業。</span><span class="sxs-lookup"><span data-stu-id="908db-118">The controller and creator processes both act as administrators for the request queue, but the controller does not perform I/O operations on it.</span></span> <span data-ttu-id="908db-119">應用程式會在建立要求佇列時，藉由在 [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue)的 *Flags* 參數中指定 **HTTP \_ CREATE \_ request \_ queue \_ 旗標 \_ 控制器** 來指出它是控制器進程。</span><span class="sxs-lookup"><span data-stu-id="908db-119">The application indicates that it is a controller process when the request queue is created by specifying **HTTP\_CREATE\_REQUEST\_QUEUE\_FLAG\_CONTROLLER** in the *Flags* parameter of [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue).</span></span> <span data-ttu-id="908db-120">如果未設定 **HTTP \_ CREATE \_ REQUEST \_ QUEUE 旗標 \_ \_ 控制器** 旗標，則應用程式是建立者進程。</span><span class="sxs-lookup"><span data-stu-id="908db-120">If the **HTTP\_CREATE\_REQUEST\_QUEUE\_FLAG\_CONTROLLER** flag is not set, the application is a creator process.</span></span>

<span data-ttu-id="908db-121">下列清單包含控制器進程和建立者進程所執行的工作：</span><span class="sxs-lookup"><span data-stu-id="908db-121">The following list contains tasks performed by the controller process and the creator process:</span></span>

-   <span data-ttu-id="908db-122">建立要求佇列並指定名稱。</span><span class="sxs-lookup"><span data-stu-id="908db-122">Create the request queue and specify the name.</span></span>
-   <span data-ttu-id="908db-123">使用 [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) 函數設定要求佇列。</span><span class="sxs-lookup"><span data-stu-id="908db-123">Configure the request queue using the [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) function.</span></span>
-   <span data-ttu-id="908db-124">使用 [**HttpQueryRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty) 函數來查詢要求佇列設定參數。</span><span class="sxs-lookup"><span data-stu-id="908db-124">Query the request queue configuration parameters using the [**HttpQueryRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty) function.</span></span>
-   <span data-ttu-id="908db-125">建立 URL 群組，並將它們與要求佇列產生關聯。</span><span class="sxs-lookup"><span data-stu-id="908db-125">Create URL Groups and associates them with a request queue.</span></span>
-   <span data-ttu-id="908db-126">設定 ACL，以指定允許在要求佇列上接收 i/o 的工作者進程。</span><span class="sxs-lookup"><span data-stu-id="908db-126">Set the ACL specifying the worker processes that are allowed to receive I/O on the request queue.</span></span>
-   <span data-ttu-id="908db-127">呼叫 [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) 來延遲工作者進程的具現化，直到第一個要求抵達要求佇列為止。</span><span class="sxs-lookup"><span data-stu-id="908db-127">Call [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) to delay the instantiation of worker processes until the first request arrives on the request queue.</span></span>

<span data-ttu-id="908db-128">除了這些工作以外，建立者進程也可以在要求佇列上執行 i/o 作業。</span><span class="sxs-lookup"><span data-stu-id="908db-128">In addition to these tasks, the creator process can also perform I/O operations on the request queue.</span></span>

## <a name="worker-processes"></a><span data-ttu-id="908db-129">工作者處理序</span><span class="sxs-lookup"><span data-stu-id="908db-129">Worker Processes</span></span>

<span data-ttu-id="908db-130">只有在背景工作進程已被授與 ACL 的存取權時，才能開啟現有的要求佇列。</span><span class="sxs-lookup"><span data-stu-id="908db-130">A worker process can open an existing request queue only if they have been granted access to it in the ACL.</span></span> <span data-ttu-id="908db-131">以最低許可權運作的工作者進程可以開啟要求佇列，並在其上執行 i/o。</span><span class="sxs-lookup"><span data-stu-id="908db-131">Worker processes operating under least privileges can open a request queue and perform I/O on it.</span></span> <span data-ttu-id="908db-132">應用程式會藉由呼叫 [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue)和在 *旗標* 參數中 **\_ \_ \_ \_ \_ 開啟 \_ 現有的 HTTP CREATE request queue 旗** 標，以及 *pName* 參數中的要求佇列名稱，來開啟現有的要求佇列。</span><span class="sxs-lookup"><span data-stu-id="908db-132">Applications open an existing request queue by calling [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) with the **HTTP\_CREATE\_REQUEST\_QUEUE\_FLAG\_OPEN\_EXISTING** in the *Flags* parameter, and the name of the request queue in the *pName* parameter.</span></span>

<span data-ttu-id="908db-133">背景工作進程會執行下列功能：</span><span class="sxs-lookup"><span data-stu-id="908db-133">The worker process performs the following functions:</span></span>

-   <span data-ttu-id="908db-134">在要求佇列上接收要求並傳送回應。</span><span class="sxs-lookup"><span data-stu-id="908db-134">Receive requests and send responses on the request queue.</span></span>
-   <span data-ttu-id="908db-135">依名稱開啟現有的要求佇列。</span><span class="sxs-lookup"><span data-stu-id="908db-135">Open an existing request queue by name.</span></span> <span data-ttu-id="908db-136">傳回給背景工作進程之要求佇列的控制碼，無法用來設定要求佇列。</span><span class="sxs-lookup"><span data-stu-id="908db-136">The handle to the request queue returned to the worker process cannot be used to configure the request queue.</span></span>
-   <span data-ttu-id="908db-137">查詢要求佇列設定參數。</span><span class="sxs-lookup"><span data-stu-id="908db-137">Query the request queue configuration parameters.</span></span>

<span data-ttu-id="908db-138">下圖顯示要求佇列的背景工作進程模型。</span><span class="sxs-lookup"><span data-stu-id="908db-138">The following diagram shows the worker process model for request queues.</span></span> <span data-ttu-id="908db-139">要求佇列可以有數個處理 i/o 的工作者進程，以及一個可設定要求佇列的建立者程式。</span><span class="sxs-lookup"><span data-stu-id="908db-139">The request queue can have several worker processes that process I/O, and one creator processes that configures the request queue.</span></span>

![要求佇列的背景工作進程模型](images/namedrequestqueue.png)

 

 




