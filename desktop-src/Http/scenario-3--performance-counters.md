---
title: 案例3效能計數器
description: 效能計數器會根據所要求或接收的資料量、大小、持續時間和速率來測量資訊或資料的數量。
ms.assetid: 1b264144-7600-402e-86f8-674a2d02f9f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de90607cbda0542ee385b83f44bec878927d509f
ms.sourcegitcommit: fc3f2a28a55e590ac38846048f10b64ba527a98d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "107001092"
---
# <a name="scenario-3-performance-counters"></a><span data-ttu-id="74b6d-103">案例3：效能計數器</span><span class="sxs-lookup"><span data-stu-id="74b6d-103">Scenario 3: Performance Counters</span></span>

<span data-ttu-id="74b6d-104">效能計數器會根據所要求或接收的資料量、大小、持續時間和速率來測量資訊或資料的數量。</span><span class="sxs-lookup"><span data-stu-id="74b6d-104">Performance counters measure quantities of information or data, according to the number, size, duration, and rate of data being requested or received.</span></span> <span data-ttu-id="74b6d-105">您不應該預期會取得計數器的詳細資料清單，例如錯誤訊息的清單。</span><span class="sxs-lookup"><span data-stu-id="74b6d-105">You should not expect to get a list of details from a counter, such as a list of error messages.</span></span> <span data-ttu-id="74b6d-106">相反地，請使用效能計數器來取得數量，例如啟動後的錯誤訊息數目，或產生錯誤訊息的速率。</span><span class="sxs-lookup"><span data-stu-id="74b6d-106">Instead, use performance counters to get quantities, such as the number of error message since startup or the rate at which error messages are being generated.</span></span>

## <a name="performance-counters-for-httpsys"></a><span data-ttu-id="74b6d-107">HTTP.sys 的效能計數器</span><span class="sxs-lookup"><span data-stu-id="74b6d-107">Performance Counters for HTTP.sys</span></span>

<span data-ttu-id="74b6d-108">從 Windows Vista 和 Windows Server 2008 開始，HTTP.sys 具有下列效能計量計數器，可協助您監視、診斷和規劃網頁伺服器的容量： HTTP 伺服器 API 元件具有下列效能計數器，可協助您監視、診斷和規劃 Web 服務器的容量：</span><span class="sxs-lookup"><span data-stu-id="74b6d-108">Starting with Windows Vista and Windows Server 2008, HTTP.sys has the following performance metric counters to help you with monitoring, diagnosing, and capacity planning for Web servers: The HTTP Server API component has the following performance counters to help you with monitoring, diagnosing, and capacity planning for Web servers:</span></span>

- <span data-ttu-id="74b6d-109">HTTP 服務計數器：</span><span class="sxs-lookup"><span data-stu-id="74b6d-109">HTTP Service Counters:</span></span>
  - <span data-ttu-id="74b6d-110">快取中的 Uri 數目，自啟動後新增、自啟動後刪除，以及快取排清數目</span><span class="sxs-lookup"><span data-stu-id="74b6d-110">Number of URIs in the cache, added since startup, deleted since startup, and number of cache flushes</span></span>
  - <span data-ttu-id="74b6d-111">每秒快取點擊次數和快取遺漏數/秒</span><span class="sxs-lookup"><span data-stu-id="74b6d-111">Cache hits/second and Cache misses/second</span></span>
- <span data-ttu-id="74b6d-112">HTTP 服務 URL 群組：</span><span class="sxs-lookup"><span data-stu-id="74b6d-112">HTTP Service URL Groups:</span></span>
  - <span data-ttu-id="74b6d-113">資料傳送速率、資料接收速率、傳送和接收的位元組 (傳送) </span><span class="sxs-lookup"><span data-stu-id="74b6d-113">Data send rate, data receive rate, bytes transferred (sent and received)</span></span>
  - <span data-ttu-id="74b6d-114">連線數目上限、連接嘗試率、GET 和 HEAD 要求的速率，以及要求總數</span><span class="sxs-lookup"><span data-stu-id="74b6d-114">Maximum number of connections, connection attempts rate, rate for GET and HEAD requests, and total number of requests</span></span>
- <span data-ttu-id="74b6d-115">HTTP 服務要求佇列：</span><span class="sxs-lookup"><span data-stu-id="74b6d-115">HTTP Service Request Queues:</span></span>
  - <span data-ttu-id="74b6d-116">佇列中的要求數、佇列中最舊要求的存留期 (佇列中最後一個要求的存留期) </span><span class="sxs-lookup"><span data-stu-id="74b6d-116">Number of requests in queue, age of oldest requests in queue (age of the last request in the queue)</span></span>
  - <span data-ttu-id="74b6d-117">要求抵達佇列的速率、拒絕的速率、拒絕的要求總數、快取點擊率</span><span class="sxs-lookup"><span data-stu-id="74b6d-117">Rate of request arrivals into the queue, rate of rejection, total number of rejected requests, rate of cache hits</span></span>

<span data-ttu-id="74b6d-118">**存取效能計數器**</span><span class="sxs-lookup"><span data-stu-id="74b6d-118">**Accessing Performance Counters**</span></span>

1.  <span data-ttu-id="74b6d-119">在命令提示字元中輸入 **perfmon** ，以啟動效能診斷主控台。</span><span class="sxs-lookup"><span data-stu-id="74b6d-119">Type **perfmon** at the command prompt to start the Performance Diagnostic Console.</span></span>
2.  <span data-ttu-id="74b6d-120">選取樹狀目錄控制項中的 **效能監視器** ，然後按一下以開啟 [ **新增計數器** ] **+** 。</span><span class="sxs-lookup"><span data-stu-id="74b6d-120">Select **Performance Monitor** in the tree control and then open the **Add Counters** by clicking **+**.</span></span>
3.  <span data-ttu-id="74b6d-121">從「 **新增計數器** 」中，選取三個效能計數器集合： **HTTP 服務**、 **Http 服務要求佇列** 或 **HTTP 服務 Url 群組**。</span><span class="sxs-lookup"><span data-stu-id="74b6d-121">From **Add Counters** select from the three Performance Counters sets: **HTTP Service**, **HTTP Service Request Queues** , or **HTTP Service Url Groups**.</span></span>
4.  <span data-ttu-id="74b6d-122">若要從 **Http 服務要求佇列** 和 **Http 服務 Url 群組** 計數器集合中查看計數器，請選取 [ **實例 (s])** 然後按一下 [ **新增**]，再按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="74b6d-122">To view counters from the **HTTP Service Request Queues** and **HTTP Service Url Groups** counter sets, select **instance(s)** and click **Add**, and then click **OK**.</span></span> <span data-ttu-id="74b6d-123">若要查看 HTTP 服務計數器，請選取左窗格中的計數器集合，然後按一下 [ **新增**]。</span><span class="sxs-lookup"><span data-stu-id="74b6d-123">To view the HTTP Service counters, select the counter set in the left pane and click **Add**.</span></span>

> [!Note]  
> <span data-ttu-id="74b6d-124">每一部電腦只能有一個 HTTP 伺服器 API 計數器實例，因為這些計數器代表全元件的狀態。</span><span class="sxs-lookup"><span data-stu-id="74b6d-124">Only one instance of the HTTP Server API counters exists per machine, as these counters represent the component-wide state.</span></span> <span data-ttu-id="74b6d-125">使用 Url 群組效能計數器的實例時，效能計數器的實例識別碼 () 將會符合 Url 群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="74b6d-125">With instances of Url Group performance counters, the instance ID (for the performance counter) will match the Url Group ID.</span></span> <span data-ttu-id="74b6d-126">您可以藉由執行 **netsh HTTP show servicestate** 來查看 URL 群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="74b6d-126">The Url Group ID can be viewed by running **netsh http show servicestate**.</span></span> <span data-ttu-id="74b6d-127">使用要求佇列效能計數器的實例，實例名稱會對應至要求佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="74b6d-127">With instances of Request Queues performance counters, the instance name corresponds to Request Queue Name.</span></span> <span data-ttu-id="74b6d-128">要求佇列名稱 (（如果有的話）) 可由相同的 **netsh HTTP show servicestate** 來顯示。</span><span class="sxs-lookup"><span data-stu-id="74b6d-128">The Request Queue Name (if one exists) can be shown by the same **netsh http show servicestate**.</span></span> <span data-ttu-id="74b6d-129">不過，某些伺服器應用程式可能會有無法與效能計數器實例識別碼相符的未命名要求佇列。</span><span class="sxs-lookup"><span data-stu-id="74b6d-129">However, some server applications may have unnamed Request Queues that cannot be matched to a performance counter instance ID.</span></span>

 

 

 




