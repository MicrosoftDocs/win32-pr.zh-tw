---
title: RPC 訊息佇列
description: 訊息佇列 (MSMQ) 可讓使用者在網路和系統之間進行通訊，而不論目前的通訊應用程式和系統狀態為何。
ms.assetid: f1c8665b-3754-4c2e-b3ac-bba1f4b329e1
keywords:
- 遠端程序呼叫 RPC、描述、訊息佇列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b72e9e35ec2aa1cc440c0d0356c681c4fe8548c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021862"
---
# <a name="rpc-message-queuing"></a><span data-ttu-id="febdd-104">RPC 訊息佇列</span><span class="sxs-lookup"><span data-stu-id="febdd-104">RPC Message Queuing</span></span>

<span data-ttu-id="febdd-105">訊息佇列 (MSMQ) 可讓使用者在網路和系統之間進行通訊，而不論目前的通訊應用程式和系統狀態為何。</span><span class="sxs-lookup"><span data-stu-id="febdd-105">Message Queuing (MSMQ) lets users communicate across networks and systems regardless of the current state of the communicating applications and systems.</span></span> <span data-ttu-id="febdd-106">應用程式會透過 MSMQ 維護的訊息佇列來傳送和接收訊息。</span><span class="sxs-lookup"><span data-stu-id="febdd-106">Applications send and receive messages through message queues that MSMQ maintains.</span></span> <span data-ttu-id="febdd-107">即使用戶端或伺服器應用程式不在執行中，訊息佇列仍會繼續運作。</span><span class="sxs-lookup"><span data-stu-id="febdd-107">The message queues continue to function even when the client or server application is not running.</span></span> <span data-ttu-id="febdd-108">訊息佇列提供：</span><span class="sxs-lookup"><span data-stu-id="febdd-108">Message queuing provides:</span></span>

-   <span data-ttu-id="febdd-109">**非同步通訊。**</span><span class="sxs-lookup"><span data-stu-id="febdd-109">**Asynchronous messaging.**</span></span> <span data-ttu-id="febdd-110">透過 MSMQ 非同步通訊，用戶端應用程式可以將訊息傳送至伺服器，並立即傳回，即使目的電腦或伺服器程式沒有回應。</span><span class="sxs-lookup"><span data-stu-id="febdd-110">With MSMQ asynchronous messaging, a client application can send a message to a server and return immediately, even if the target computer or server program is not responding.</span></span>
-   <span data-ttu-id="febdd-111">**保證訊息傳遞。**</span><span class="sxs-lookup"><span data-stu-id="febdd-111">**Guaranteed message delivery.**</span></span> <span data-ttu-id="febdd-112">當應用程式透過 MSMQ 傳送訊息時，即使目的地應用程式未同時執行，或者網路和系統離線，訊息還是會到達其目的地。</span><span class="sxs-lookup"><span data-stu-id="febdd-112">When an application sends a message through MSMQ, the message will reach its destination even if the destination application is not running at the same time or the networks and systems are offline.</span></span>
-   <span data-ttu-id="febdd-113">**路由及動態設定。**</span><span class="sxs-lookup"><span data-stu-id="febdd-113">**Routing and dynamic configuration.**</span></span> <span data-ttu-id="febdd-114">MSMQ 可透過異類網路提供彈性的路由。</span><span class="sxs-lookup"><span data-stu-id="febdd-114">MSMQ provides flexible routing over heterogeneous networks.</span></span> <span data-ttu-id="febdd-115">您可以動態變更這類網路的設定，而不需要對系統和網路本身進行任何重大變更。</span><span class="sxs-lookup"><span data-stu-id="febdd-115">The configuration of such networks can be changed dynamically without any major changes to systems and networks themselves.</span></span>
-   <span data-ttu-id="febdd-116">**未連接的訊息。**</span><span class="sxs-lookup"><span data-stu-id="febdd-116">**Connectionless messaging.**</span></span> <span data-ttu-id="febdd-117">使用 MSMQ 的應用程式不需要設定目標應用程式的直接會話。</span><span class="sxs-lookup"><span data-stu-id="febdd-117">Applications using MSMQ do not need to set up direct sessions with target applications.</span></span>
-   <span data-ttu-id="febdd-118">[安全性](security.md)。</span><span class="sxs-lookup"><span data-stu-id="febdd-118">[Security](security.md).</span></span> <span data-ttu-id="febdd-119">MSMQ 提供以 Windows 安全性為基礎的安全通訊，以及加密和數位簽章 (CryptoAPI) 的密碼編譯 API。</span><span class="sxs-lookup"><span data-stu-id="febdd-119">MSMQ provides secure communication based on Windows security and the Cryptographic API (CryptoAPI) for encryption and digital signatures.</span></span>
-   <span data-ttu-id="febdd-120">**排定優先順序的訊息。**</span><span class="sxs-lookup"><span data-stu-id="febdd-120">**Prioritized Messaging.**</span></span> <span data-ttu-id="febdd-121">MSMQ 會根據優先順序將訊息傳送到網路上，讓重要的應用程式更快進行通訊。</span><span class="sxs-lookup"><span data-stu-id="febdd-121">MSMQ transfers messages across networks based on priority, allowing faster communication for critical applications.</span></span>

<span data-ttu-id="febdd-122">Microsoft RPC 將開放式 Software Foundation –資料通訊設備 (憑證-DCE) 模型，藉由允許分散式應用程式使用 MSMQ 做為傳輸，並控制其許多功能，來進行遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="febdd-122">Microsoft RPC extends the Open Software Foundation–Data Communications Equipment (OSF-DCE) model for remote procedure calls by allowing distributed applications to use MSMQ as a transport and to control many of its features.</span></span> <span data-ttu-id="febdd-123">這項功能可用於傳統的 RPC 應用程式，以及透過 **IRPCOptions** 介面，到 COM 應用程式。</span><span class="sxs-lookup"><span data-stu-id="febdd-123">This functionality is available both to conventional RPC applications and, through the **IRPCOptions** interface, to COM applications.</span></span>

> [!Note]  
> <span data-ttu-id="febdd-124">RPC 訊息佇列僅適用于 Windows 2000。</span><span class="sxs-lookup"><span data-stu-id="febdd-124">RPC message queuing is available only on Windows 2000.</span></span> <span data-ttu-id="febdd-125">較新版本的 Windows 不支援 RPC 訊息佇列。</span><span class="sxs-lookup"><span data-stu-id="febdd-125">Later versions of Windows do not support RPC message queuing.</span></span>

 

<span data-ttu-id="febdd-126">下列主題提供訊息佇列的總覽：</span><span class="sxs-lookup"><span data-stu-id="febdd-126">The following topics provide an overview of message queuing:</span></span>

-   [<span data-ttu-id="febdd-127">訊息佇列服務架構總覽</span><span class="sxs-lookup"><span data-stu-id="febdd-127">Overview of Message Queuing Services Architecture</span></span>](overview-of-message-queuing-services-architecture.md)
-   [<span data-ttu-id="febdd-128">訊息和訊息佇列屬性</span><span class="sxs-lookup"><span data-stu-id="febdd-128">Message and Message Queue Properties</span></span>](message-and-message-queue-properties.md)
-   [<span data-ttu-id="febdd-129">使用 MSMQ 做為 RPC 傳輸</span><span class="sxs-lookup"><span data-stu-id="febdd-129">Using MSMQ as an RPC Transport</span></span>](using-msmq-as-an-rpc-transport.md)
-   [<span data-ttu-id="febdd-130">RPC 消息 \_ 佇列應用程式的系統需求</span><span class="sxs-lookup"><span data-stu-id="febdd-130">System Requirements for RPC-Message\_Queuing Applications</span></span>](system-requirements-for-rpc-message-queuing-applications.md)
-   [<span data-ttu-id="febdd-131">開發 RPC-Message 佇列應用程式</span><span class="sxs-lookup"><span data-stu-id="febdd-131">Developing RPC-Message Queuing Applications</span></span>](developing-rpc-message-queuing-applications.md)
-   [<span data-ttu-id="febdd-132">MSMQ 安全性服務</span><span class="sxs-lookup"><span data-stu-id="febdd-132">MSMQ Security Services</span></span>](msmq-security-services.md)

 

 




