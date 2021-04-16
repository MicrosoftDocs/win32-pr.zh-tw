---
description: 佇列處理的優點
ms.assetid: dc1fc03f-1e2c-481c-95a7-f8d7b1e06bb0
title: 佇列處理的優點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a0d2068d70ecf611ec334632c8b8f819319ef3
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "104568262"
---
# <a name="benefits-of-queued-processing"></a><span data-ttu-id="fd19b-103">佇列處理的優點</span><span class="sxs-lookup"><span data-stu-id="fd19b-103">Benefits of Queued Processing</span></span>

<span data-ttu-id="fd19b-104">設計新的應用程式時，開發人員必須考慮程式碼撰寫元件的影響，以進行即時 (同步) 處理，與佇列 (非同步) 處理。</span><span class="sxs-lookup"><span data-stu-id="fd19b-104">When designing new applications, developers must consider the implications of coding components for real-time (synchronous) processing versus queued (asynchronous) processing.</span></span> <span data-ttu-id="fd19b-105">選擇取決於基礎商務邏輯所決定的特定應用程式需求。</span><span class="sxs-lookup"><span data-stu-id="fd19b-105">The choice depends on the requirements of the specific application as determined by the underlying business logic.</span></span> <span data-ttu-id="fd19b-106">作為指導方針，佇列處理可提供下列優於即時處理的優點：</span><span class="sxs-lookup"><span data-stu-id="fd19b-106">As a guideline, queued processing offers the following advantages over real-time processing:</span></span>

-   <span data-ttu-id="fd19b-107">降低元件可用性的相依性</span><span class="sxs-lookup"><span data-stu-id="fd19b-107">Reduced dependency on component availability</span></span>
-   <span data-ttu-id="fd19b-108">較短的元件存留期</span><span class="sxs-lookup"><span data-stu-id="fd19b-108">Shorter component lifetimes</span></span>
-   <span data-ttu-id="fd19b-109">使用已中斷連線的應用程式時的生產力不中斷</span><span class="sxs-lookup"><span data-stu-id="fd19b-109">Uninterrupted productivity when using disconnected applications</span></span>
-   <span data-ttu-id="fd19b-110">訊息可靠性</span><span class="sxs-lookup"><span data-stu-id="fd19b-110">Message reliability</span></span>
-   <span data-ttu-id="fd19b-111">有效率的伺服器排程</span><span class="sxs-lookup"><span data-stu-id="fd19b-111">Efficient server scheduling</span></span>

## <a name="component-availability"></a><span data-ttu-id="fd19b-112">元件可用性</span><span class="sxs-lookup"><span data-stu-id="fd19b-112">Component Availability</span></span>

<span data-ttu-id="fd19b-113">在即時處理應用程式中，如果交易的某個元件無法使用（也許是因為伺服器多載或網路問題），整個程式會遭到封鎖而無法完成。</span><span class="sxs-lookup"><span data-stu-id="fd19b-113">In a real-time processing application, if just one component of the transaction is not available—perhaps because of server overload or networking problems—the entire process is blocked and cannot complete.</span></span> <span data-ttu-id="fd19b-114">相反地，使用 COM + 佇列元件服務的應用程式會將交易區分為必須立即完成的活動，以及稍後可以完成的活動。</span><span class="sxs-lookup"><span data-stu-id="fd19b-114">In contrast, an application using the COM+ queued components service separates the transaction into activities that must be completed now and those that can be completed at a later time.</span></span> <span data-ttu-id="fd19b-115">例如，您可以將訊息排入佇列以供稍後處理，讓提出要求的元件在其他工作中都是免費的。</span><span class="sxs-lookup"><span data-stu-id="fd19b-115">For example, messages can be queued for later processing so that the requesting component is free for other tasks.</span></span>

## <a name="component-lifetimes"></a><span data-ttu-id="fd19b-116">元件存留期</span><span class="sxs-lookup"><span data-stu-id="fd19b-116">Component Lifetimes</span></span>

<span data-ttu-id="fd19b-117">使用佇列元件服務的應用程式可讓伺服器元件獨立于用戶端運作。</span><span class="sxs-lookup"><span data-stu-id="fd19b-117">An application using the queued components service allows the server component to operate independently of the client.</span></span> <span data-ttu-id="fd19b-118">因此，伺服器元件可以更快完成。</span><span class="sxs-lookup"><span data-stu-id="fd19b-118">As a result, server components can complete more quickly.</span></span> <span data-ttu-id="fd19b-119">在即時系統中，伺服器元件是從建立時開始，到最後釋放物件為止。</span><span class="sxs-lookup"><span data-stu-id="fd19b-119">In a real-time system, the server component exists from the time it is created until the object is finally released.</span></span> <span data-ttu-id="fd19b-120">伺服器會等候用戶端進行方法呼叫，並傳回結果，這會使伺服器物件快速迴圈，並限制伺服器的擴充性。</span><span class="sxs-lookup"><span data-stu-id="fd19b-120">The server waits for the client to make method calls and for results to be returned, which negates the rapid cycling of server objects and limits server scalability.</span></span>

## <a name="disconnected-applications"></a><span data-ttu-id="fd19b-121">中斷連線的應用程式</span><span class="sxs-lookup"><span data-stu-id="fd19b-121">Disconnected Applications</span></span>

<span data-ttu-id="fd19b-122">膝上型電腦、筆記本電腦和掌上電腦的增加使用，為服務偶爾中斷用戶端或行動使用者的應用程式建立了需求。</span><span class="sxs-lookup"><span data-stu-id="fd19b-122">The increasing use of laptops, notebooks, and palm computers has created a need for applications that service occasionally disconnected clients or mobile users.</span></span> <span data-ttu-id="fd19b-123">在已排入佇列的系統中，這些使用者可以在中斷連線的情況下繼續工作，或在未連接到伺服器時繼續運作，而且稍後可以連接到資料庫或伺服器來處理其要求。</span><span class="sxs-lookup"><span data-stu-id="fd19b-123">In a queued system, these users can continue to work in a disconnected scenario or when not connected to the server, and they can later connect to the databases or servers to process their requests.</span></span> <span data-ttu-id="fd19b-124">例如，銷售人員可以從客戶取得訂單，並于稍後連接到出貨部門來處理這些訂單。</span><span class="sxs-lookup"><span data-stu-id="fd19b-124">For example, a salesperson can take orders from customers and later connect to the shipping department to process those orders.</span></span>

<span data-ttu-id="fd19b-125">如果您有可執行連線或中斷連線的元件，訊息會以單向方式進行，而且很少需要來回切換。</span><span class="sxs-lookup"><span data-stu-id="fd19b-125">If you have a component that can be run either connected or disconnected, messages are traveling in one direction and there is rarely a need to switch back and forth.</span></span> <span data-ttu-id="fd19b-126">例如，在訂單採取案例中，出貨元件會接收訊息並進行處理。</span><span class="sxs-lookup"><span data-stu-id="fd19b-126">For example, in the order-taking scenario, the shipping component receives the message and processes it.</span></span> <span data-ttu-id="fd19b-127">它可能會產生另一個用於計費或審核的元件。</span><span class="sxs-lookup"><span data-stu-id="fd19b-127">It may generate another component for billing or auditing.</span></span> <span data-ttu-id="fd19b-128">用戶端會在伺服器開始之前認可。</span><span class="sxs-lookup"><span data-stu-id="fd19b-128">The client commits before the server ever starts.</span></span> <span data-ttu-id="fd19b-129">在應用程式認可之前，不會傳送訊息。</span><span class="sxs-lookup"><span data-stu-id="fd19b-129">The message isn't sent until the application commits.</span></span>

<span data-ttu-id="fd19b-130">下圖顯示已中斷連線的案例中資訊的流程。</span><span class="sxs-lookup"><span data-stu-id="fd19b-130">The following illustration shows the flow of information in a disconnected scenario.</span></span>

![顯示用戶端與伺服器之間的資訊流程的圖表。](images/b1818188-0294-4bd8-8bbe-9fe8eea9e09a.png)

## <a name="message-reliability"></a><span data-ttu-id="fd19b-132">訊息可靠性</span><span class="sxs-lookup"><span data-stu-id="fd19b-132">Message Reliability</span></span>

<span data-ttu-id="fd19b-133">訊息佇列是一種功能強大的工具，可使用資料庫技術，以健全的方式協助保護資料。</span><span class="sxs-lookup"><span data-stu-id="fd19b-133">Message Queuing is a powerful tool that uses database techniques to help protect data in a robust way.</span></span> <span data-ttu-id="fd19b-134">萬一伺服器失敗，訊息佇列可確保回復交易，讓訊息不會遺失，而且資料也不會損毀。</span><span class="sxs-lookup"><span data-stu-id="fd19b-134">In the event of a server failure, Message Queuing ensures that transactions are rolled back so that messages are not lost and data is not corrupted.</span></span>

## <a name="server-scheduling"></a><span data-ttu-id="fd19b-135">伺服器排程</span><span class="sxs-lookup"><span data-stu-id="fd19b-135">Server Scheduling</span></span>

<span data-ttu-id="fd19b-136">使用已排入佇列之元件的應用程式非常適用于經過時間改變的元件執行，這會將 uncritical 工作延後到離峰時段。</span><span class="sxs-lookup"><span data-stu-id="fd19b-136">An application using queued components is well suited to time-shifted component execution, which defers uncritical work to an off-peak period.</span></span> <span data-ttu-id="fd19b-137">這與傳統的批次模式處理相同，也是相當有用的概念。</span><span class="sxs-lookup"><span data-stu-id="fd19b-137">This is the same useful concept that was applied to traditional batch mode processing.</span></span> <span data-ttu-id="fd19b-138">您可以將類似的要求延後以供伺服器連續執行，而不需要讓伺服器立即回應各式各樣的要求。</span><span class="sxs-lookup"><span data-stu-id="fd19b-138">Similar requests can be deferred for contiguous execution by the server rather than requiring the server to react immediately to a wide variety of requests.</span></span>

 

 



