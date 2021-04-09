---
title: 2.0 版要求佇列的要求開始
description: .
ms.assetid: 84a744b7-1b0e-4fa7-8015-4840251aa856
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d618ea3fa38a856eba743d2bf60bfbfec9a633
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933251"
---
# <a name="demand-start-on-version-20-request-queues"></a><span data-ttu-id="df827-103">2.0 版要求佇列的要求開始</span><span class="sxs-lookup"><span data-stu-id="df827-103">Demand Start on Version 2.0 Request Queues</span></span>

<span data-ttu-id="df827-104">HTTP 伺服器版本 2.0 API 要求佇列的需求啟動功能，可讓控制器應用程式延遲工作者進程具現化，直到第一個要求抵達要求佇列為止。</span><span class="sxs-lookup"><span data-stu-id="df827-104">The demand start feature of the HTTP Server version 2.0 API request queues allows controller application to delay worker process instantiation until the first request arrives on the request queue.</span></span> <span data-ttu-id="df827-105">因此，應用程式可以避免耗用資源，直到需要它們為止。</span><span class="sxs-lookup"><span data-stu-id="df827-105">Thus, the applications can avoid consuming resources until they are required.</span></span> <span data-ttu-id="df827-106">如需控制器應用程式的詳細資訊，請參閱「 [命名要求佇列](named-request-queue.md) 」主題。</span><span class="sxs-lookup"><span data-stu-id="df827-106">For more information about the controller application, see the [Named Request Queue](named-request-queue.md) topic.</span></span>

## <a name="asynchronous-demand-start"></a><span data-ttu-id="df827-107">非同步需求開始</span><span class="sxs-lookup"><span data-stu-id="df827-107">Asynchronous Demand Start</span></span>

<span data-ttu-id="df827-108">控制器應用程式會使用要求佇列的控制碼來呼叫 [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) ，以起始需求開始通知。</span><span class="sxs-lookup"><span data-stu-id="df827-108">The controller application calls [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) with the handle to the request queue to initiate a demand start notification.</span></span> <span data-ttu-id="df827-109">在非同步完成的情況下，應用程式會在 *pOverlapped* 參數中提供重迭的結構。</span><span class="sxs-lookup"><span data-stu-id="df827-109">For asynchronous completion, the application supplies the overlapped structure in the *pOverlapped* parameter.</span></span> <span data-ttu-id="df827-110">以非同步方式呼叫 **HttpWaitForDemandStart** 時，會在第一個要求抵達要求佇列時通知控制器應用程式。</span><span class="sxs-lookup"><span data-stu-id="df827-110">When **HttpWaitForDemandStart** is called asynchronously, the controller application is notified when the first request arrives on the request queue.</span></span> <span data-ttu-id="df827-111">當需求開始通知完成之後，控制器應用程式可以在要求佇列上註冊另一個需求開始通知。</span><span class="sxs-lookup"><span data-stu-id="df827-111">After the demand start notification completes, the controller application can register for another demand start notification on the request queue.</span></span>

<span data-ttu-id="df827-112">HTTP 伺服器 API 不允許要求佇列有一個以上的同時需求開始通知。</span><span class="sxs-lookup"><span data-stu-id="df827-112">The HTTP Server API does not allow more than one simultaneous demand start notification for a request queue.</span></span> <span data-ttu-id="df827-113">不過，當未完成的要求開始通知完成時，應用程式會再次呼叫 [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) ，以在要求佇列上啟動多個背景工作進程。</span><span class="sxs-lookup"><span data-stu-id="df827-113">However, when the outstanding demand start notification completes, the application calls [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) again to start multiple worker processes on the request queue.</span></span> <span data-ttu-id="df827-114">HTTP 不會強制執行要求佇列上操作的要求開始通知數目或背景工作進程數目的限制。</span><span class="sxs-lookup"><span data-stu-id="df827-114">HTTP does not enforce limitations on the number of demand start notifications or the number of worker processes operating on the request queue.</span></span> <span data-ttu-id="df827-115">但是，控制器應用程式可以強制執行要求佇列上允許的工作者進程數目。</span><span class="sxs-lookup"><span data-stu-id="df827-115">The controller applications can, however, enforce the number of worker processes allowed on a request queue.</span></span>

<span data-ttu-id="df827-116">HTTP 伺服器 API 支援取消非同步 [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="df827-116">The HTTP Server API supports canceling asynchronous [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) calls.</span></span> <span data-ttu-id="df827-117">應用程式可以使用 [**CancelIoEx**](/windows/desktop/FileIO/cancelioex-func) 搭配 *pOverlapped* 中提供的重迭結構，以取消未完成的 **HttpWaitForDemandStart** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="df827-117">Applications can use [**CancelIoEx**](/windows/desktop/FileIO/cancelioex-func) with the overlapped structure supplied in *pOverlapped*, to cancel an outstanding **HttpWaitForDemandStart** call.</span></span>

## <a name="synchronous-demand-start"></a><span data-ttu-id="df827-118">同步需求開始</span><span class="sxs-lookup"><span data-stu-id="df827-118">Synchronous Demand Start</span></span>

<span data-ttu-id="df827-119">不建議啟動同步需求，因為應用程式會封鎖，直到要求抵達要求佇列為止。</span><span class="sxs-lookup"><span data-stu-id="df827-119">Synchronous demand start is not recommended because the application blocks until a request arrives on the request queue.</span></span>

 

 