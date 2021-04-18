---
title: 非同步屬性
description: 當程式叫用介面中的程式時，程式可能會以同步或非同步方式執行。
ms.assetid: 3e6c6c13-1524-41b2-96dc-3885eadb847c
keywords:
- IDL MIDL，屬性 MIDL，非同步
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00aca2276bf1fa5178f1dca3ae4803544066d983
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106966031"
---
# <a name="asynchronous-attributes"></a><span data-ttu-id="9b49f-104">非同步屬性</span><span class="sxs-lookup"><span data-stu-id="9b49f-104">Asynchronous Attributes</span></span>

<span data-ttu-id="9b49f-105">當程式叫用介面中的程式時，程式可能會以同步或非同步方式執行。</span><span class="sxs-lookup"><span data-stu-id="9b49f-105">When a program invokes a procedure in an interface, the procedure may execute synchronously or asynchronously.</span></span> <span data-ttu-id="9b49f-106">同步程式會導致呼叫程式等候，直到程式傳回，程式才能繼續進行。</span><span class="sxs-lookup"><span data-stu-id="9b49f-106">A synchronous procedure causes the calling program to wait until the procedure returns before the program can proceed.</span></span> <span data-ttu-id="9b49f-107">非同步程式會立即傳回，而不會等待結果。</span><span class="sxs-lookup"><span data-stu-id="9b49f-107">An asynchronous procedure returns immediately without waiting for results.</span></span> <span data-ttu-id="9b49f-108">呼叫程式稍後必須重新同步處理以接收資料的介面程式。</span><span class="sxs-lookup"><span data-stu-id="9b49f-108">The calling program must later resynchronize with the interface procedure to receive data.</span></span> <span data-ttu-id="9b49f-109">如需詳細資訊，請參閱 [非同步 RPC](/windows/desktop/Rpc/asynchronous-rpc)。</span><span class="sxs-lookup"><span data-stu-id="9b49f-109">For more information, see [Asynchronous RPC](/windows/desktop/Rpc/asynchronous-rpc).</span></span>

<span data-ttu-id="9b49f-110">您可以使用下列屬性來提供非同步遠端程序呼叫的支援。</span><span class="sxs-lookup"><span data-stu-id="9b49f-110">You can use the following attributes to provide support for asynchronous remote procedure calls.</span></span>



| <span data-ttu-id="9b49f-111">屬性</span><span class="sxs-lookup"><span data-stu-id="9b49f-111">Attribute</span></span>                         | <span data-ttu-id="9b49f-112">使用方式</span><span class="sxs-lookup"><span data-stu-id="9b49f-112">Usage</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9b49f-113">**async**</span><span class="sxs-lookup"><span data-stu-id="9b49f-113">**async**</span></span>](async.md)            | <span data-ttu-id="9b49f-114">套用至函式參數時，會定義一個控制碼，讓呼叫端能夠立即進行非同步呼叫，並在不等待結果的情況下立即傳回，並于稍後再重新同步處理被呼叫的函式，以在呼叫完成之後接收資料。</span><span class="sxs-lookup"><span data-stu-id="9b49f-114">When applied to a function parameter, defines a handle that allows the caller to make an asynchronous call and return immediately without waiting for results, and later resynchronize with the called function to receive data after the call completes.</span></span> <span data-ttu-id="9b49f-115">[**Async**](async.md)屬性也會用在 ACF 檔中，以定義程式或整個介面的非同步控制碼。</span><span class="sxs-lookup"><span data-stu-id="9b49f-115">The [**async**](async.md) attribute is also used in ACF files to define an asynchronous handle for a procedure or an entire interface.</span></span> <span data-ttu-id="9b49f-116">針對 COM 介面，這個介面已過時，無法用於新的介面。</span><span class="sxs-lookup"><span data-stu-id="9b49f-116">For COM interfaces, this interface is obsolete and cannot be used for new interfaces.</span></span> |
| [<span data-ttu-id="9b49f-117">**非同步 \_ uuid**</span><span class="sxs-lookup"><span data-stu-id="9b49f-117">**async\_uuid**</span></span>](async-uuid.md) | <span data-ttu-id="9b49f-118">指示 MIDL 編譯器定義 COM 介面的同步和非同步版本。</span><span class="sxs-lookup"><span data-stu-id="9b49f-118">Directs the MIDL compiler to define both synchronous and asynchronous versions of a COM interface.</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="9b49f-119">**也許**</span><span class="sxs-lookup"><span data-stu-id="9b49f-119">**maybe**</span></span>](maybe.md)            | <span data-ttu-id="9b49f-120">進行此遠端程序呼叫的用戶端不會預期任何指出來電傳遞或完成的回應，也不保證傳遞。</span><span class="sxs-lookup"><span data-stu-id="9b49f-120">The client making this remote procedure call does not expect any response indicating delivery or completion of the call, and delivery is not guaranteed.</span></span> <span data-ttu-id="9b49f-121">這與未預期回應但保證傳遞的 **訊息** 作業不同。</span><span class="sxs-lookup"><span data-stu-id="9b49f-121">This is in contrast to **message** operations where no response is expected but the delivery is guaranteed.</span></span>                                                                                                                                                                                                                    |
| [<span data-ttu-id="9b49f-122">**消息**</span><span class="sxs-lookup"><span data-stu-id="9b49f-122">**message**</span></span>](message.md)        | <span data-ttu-id="9b49f-123">遠端程序呼叫會被視為從用戶端到伺服器的非同步訊息。</span><span class="sxs-lookup"><span data-stu-id="9b49f-123">The remote procedure call is to be treated as an asynchronous message from the client to the server.</span></span> <span data-ttu-id="9b49f-124">用戶端會進行呼叫，並立即傳回，而實際的呼叫是由訊息佇列傳輸 ([**ncadg \_ mq**](ncadg-mq.md)) 處理。</span><span class="sxs-lookup"><span data-stu-id="9b49f-124">The client makes the call and returns immediately, while the actual call is handled by the message-queuing transport ([**ncadg\_mq**](ncadg-mq.md)).</span></span>                                                                                                                                                                                                                              |



 

 

 