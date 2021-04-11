---
title: 非同步 RPC
description: 非同步遠端程序呼叫 (RPC) 是 Microsoft 擴充功能，可解決 Open Software Foundation \ 8211; 分散式運算環境 (憑證-DCE) 所定義的傳統 RPC 模型的數項限制。
ms.assetid: 2586c10e-8284-419f-a200-4f6b11953688
keywords:
- 遠端程序呼叫 RPC、說明、非同步 RPC
- 非同步 RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36ac79a30fd01aeba1efb3cbd2b7cc741f26238
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093087"
---
# <a name="asynchronous-rpc"></a><span data-ttu-id="c229b-105">非同步 RPC</span><span class="sxs-lookup"><span data-stu-id="c229b-105">Asynchronous RPC</span></span>

<span data-ttu-id="c229b-106">非同步遠端程序呼叫 (RPC) 是 Microsoft 擴充功能，可解決開放式 Software Foundation –分散式運算環境 (憑證-DCE) 所定義的傳統 RPC 模型的數項限制。</span><span class="sxs-lookup"><span data-stu-id="c229b-106">Asynchronous Remote Procedure Call (RPC) is a Microsoft extension that addresses several limitations of the traditional RPC model as defined by the Open Software Foundation–Distributed Computing Environment (OSF-DCE).</span></span> <span data-ttu-id="c229b-107">非同步 RPC 會將遠端程序呼叫與其傳回值分隔開來，以解析傳統、同步 RPC 的下列限制：</span><span class="sxs-lookup"><span data-stu-id="c229b-107">Asynchronous RPC separates a remote procedure call from its return value, which resolves the following limitations of traditional, synchronous RPC:</span></span>

-   <span data-ttu-id="c229b-108">**單一執行緒用戶端的多個未完成呼叫。**</span><span class="sxs-lookup"><span data-stu-id="c229b-108">**Multiple outstanding calls from a single-threaded client.**</span></span> <span data-ttu-id="c229b-109">在傳統的 RPC 模型中，遠端程序呼叫會封鎖用戶端，直到呼叫傳回為止。</span><span class="sxs-lookup"><span data-stu-id="c229b-109">In the traditional RPC model, a client is blocked in a remote procedure call until the call returns.</span></span> <span data-ttu-id="c229b-110">這可防止用戶端有多個未完成的呼叫，同時仍然讓執行緒可以執行其他工作。</span><span class="sxs-lookup"><span data-stu-id="c229b-110">This prevents a client from having multiple outstanding calls, while still having its thread available to do other work.</span></span>
-   <span data-ttu-id="c229b-111">**較慢或延遲的用戶端。**</span><span class="sxs-lookup"><span data-stu-id="c229b-111">**Slow or delayed clients.**</span></span> <span data-ttu-id="c229b-112">產生資料緩慢的用戶端可能會想要使用初始資料進行遠端程序呼叫，然後在產生時提供其他資料。</span><span class="sxs-lookup"><span data-stu-id="c229b-112">A client that is slow to produce data may want to make a remote procedure call with initial data and then supply additional data as it is produced.</span></span> <span data-ttu-id="c229b-113">這與傳統的 (同步) RPC 不可行。</span><span class="sxs-lookup"><span data-stu-id="c229b-113">This is not possible with conventional (synchronous) RPC.</span></span>
-   <span data-ttu-id="c229b-114">**慢或延遲的伺服器。**</span><span class="sxs-lookup"><span data-stu-id="c229b-114">**Slow or delayed servers.**</span></span> <span data-ttu-id="c229b-115">需要很長時間才能完成的遠端程序呼叫，將會在工作的持續時間內結合分派執行緒。</span><span class="sxs-lookup"><span data-stu-id="c229b-115">A remote procedure call that takes a long time to complete will tie up the dispatch thread for the duration of the task.</span></span> <span data-ttu-id="c229b-116">使用非同步 RPC 時，伺服器可以啟動個別的 (非同步) 作業來處理要求，並在有可用的回復時將其傳回。</span><span class="sxs-lookup"><span data-stu-id="c229b-116">With asynchronous RPC, the server can start a separate (asynchronous) operation to process the request and send back the reply when it is available.</span></span> <span data-ttu-id="c229b-117">伺服器也可以在結果變成可用時，以累加方式傳送回復，而不需要在遠端呼叫期間系結分派執行緒。</span><span class="sxs-lookup"><span data-stu-id="c229b-117">The server can also send the reply incrementally as results become available without having to tie up a dispatch thread for the duration of the remote call.</span></span> <span data-ttu-id="c229b-118">藉由讓用戶端應用程式變成非同步，您可以防止較慢的伺服器不必要地將用戶端應用程式上傳。</span><span class="sxs-lookup"><span data-stu-id="c229b-118">By making the client application asynchronous, you can prevent a slow server from unnecessarily tying up a client application.</span></span>
-   <span data-ttu-id="c229b-119">**傳輸大量資料。**</span><span class="sxs-lookup"><span data-stu-id="c229b-119">**Transfer of large amounts of data.**</span></span> <span data-ttu-id="c229b-120">在用戶端與伺服器之間傳輸大量資料（尤其是透過低速連結）會在傳輸期間，結合用戶端執行緒和伺服器管理員執行緒。</span><span class="sxs-lookup"><span data-stu-id="c229b-120">Transferring large amounts of data between the client and server, especially over slow links, ties up both the client thread and the server manager thread for the duration of the transfer.</span></span> <span data-ttu-id="c229b-121">使用非同步 RPC 和管道時，資料傳輸可以累加方式進行，而不會封鎖用戶端或伺服器執行其他工作。</span><span class="sxs-lookup"><span data-stu-id="c229b-121">With asynchronous RPC and pipes, data transfer can take place incrementally, and without blocking the client or server from performing other tasks.</span></span>

<span data-ttu-id="c229b-122">您可以利用 async 屬性來宣告函式，以利用非同步 RPC 機制 \[ [](/windows/desktop/Midl/async) \] 。</span><span class="sxs-lookup"><span data-stu-id="c229b-122">You take advantage of asynchronous RPC mechanisms by declaring functions with the \[[**async**](/windows/desktop/Midl/async)\] attribute.</span></span> <span data-ttu-id="c229b-123">因為您會在屬性設定檔中進行此宣告 (ACF) ，所以不需要對介面定義語言進行任何變更 (IDL) 檔;非同步 RPC 對網路通訊協定沒有任何影響， (在用戶端和伺服器) 之間傳輸資料的方式。</span><span class="sxs-lookup"><span data-stu-id="c229b-123">Because you make this declaration in an attribute configuration file (ACF), you do not have to make any changes to the Interface Definition Language (IDL) file; asynchronous RPC has no effect on the wire protocol (how the data is transmitted between client and server).</span></span> <span data-ttu-id="c229b-124">這表示同步和非同步用戶端都可以與非同步伺服器應用程式進行通訊。</span><span class="sxs-lookup"><span data-stu-id="c229b-124">This means that both synchronous and asynchronous clients can communicate with an asynchronous server application.</span></span>

<span data-ttu-id="c229b-125">本節提供如何使用非同步 RPC 開發分散式應用程式的總覽。</span><span class="sxs-lookup"><span data-stu-id="c229b-125">This section presents an overview of how to develop distributed applications using asynchronous RPC.</span></span> <span data-ttu-id="c229b-126">下列各節會提供總覽：</span><span class="sxs-lookup"><span data-stu-id="c229b-126">The overview is presented in the following sections:</span></span>

-   [<span data-ttu-id="c229b-127">宣告非同步函式</span><span class="sxs-lookup"><span data-stu-id="c229b-127">Declaring Asynchronous Functions</span></span>](declaring-asynchronous-functions.md)
-   [<span data-ttu-id="c229b-128">用戶端非同步 RPC</span><span class="sxs-lookup"><span data-stu-id="c229b-128">Client-side Asynchronous RPC</span></span>](client-side-asynchronous-rpc.md)
-   [<span data-ttu-id="c229b-129">伺服器端非同步 RPC</span><span class="sxs-lookup"><span data-stu-id="c229b-129">Server-side Asynchronous RPC</span></span>](server-side-asynchronous-rpc.md)
-   [<span data-ttu-id="c229b-130">非同步呼叫的因果順序</span><span class="sxs-lookup"><span data-stu-id="c229b-130">Causal Ordering of Asynchronous Calls</span></span>](causal-ordering-of-asynchronous-calls.md)
-   [<span data-ttu-id="c229b-131">錯誤處理</span><span class="sxs-lookup"><span data-stu-id="c229b-131">Error Handling</span></span>](error-handling.md)
-   [<span data-ttu-id="c229b-132">具名管道通訊協定上的非同步 RPC</span><span class="sxs-lookup"><span data-stu-id="c229b-132">Asynchronous RPC Over the Named Pipe Protocol</span></span>](asynchronous-rpc-over-the-named-pipe-protocol.md)
-   [<span data-ttu-id="c229b-133">使用具有 DCE 管道的非同步 RPC</span><span class="sxs-lookup"><span data-stu-id="c229b-133">Using Asynchronous RPC with DCE Pipes</span></span>](using-asynchronous-rpc-with-dce-pipes.md)
-   [<span data-ttu-id="c229b-134">非同步 DCOM</span><span class="sxs-lookup"><span data-stu-id="c229b-134">Asynchronous DCOM</span></span>](asynchronous-dcom.md)

 

 