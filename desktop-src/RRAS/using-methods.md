---
title: 使用方法
description: 當用戶端向路由表管理員註冊時，它可以匯出一組方法。 這些方法可供其他用戶端用來取得用戶端特定的資訊。 方法可在路由表管理員的用戶端之間啟用私人通訊。
ms.assetid: 6d984a02-d005-43ad-81c4-968ae9c1a105
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33bd895fbb3f8f54224522786b5794c5c6c57a9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932295"
---
# <a name="using-methods"></a><span data-ttu-id="f005d-105">使用方法</span><span class="sxs-lookup"><span data-stu-id="f005d-105">Using Methods</span></span>

<span data-ttu-id="f005d-106">當用戶端向路由表管理員註冊時，它可以匯出一組方法。</span><span class="sxs-lookup"><span data-stu-id="f005d-106">When a client registers with the routing table manager, it can export a set of methods.</span></span> <span data-ttu-id="f005d-107">這些方法可供其他用戶端用來取得用戶端特定的資訊。</span><span class="sxs-lookup"><span data-stu-id="f005d-107">These methods are used by other clients to obtain client-specific information.</span></span> <span data-ttu-id="f005d-108">方法可在路由表管理員的用戶端之間啟用私人通訊。</span><span class="sxs-lookup"><span data-stu-id="f005d-108">Methods enable private communication between clients of the routing table manager.</span></span>

<span data-ttu-id="f005d-109">用戶端可以取得其他用戶端所匯出的方法清單。</span><span class="sxs-lookup"><span data-stu-id="f005d-109">A client can obtain the list of methods exported by another client.</span></span> <span data-ttu-id="f005d-110">用戶端會呼叫 [**RtmGetEntityMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods) 函數，並提供目標用戶端的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f005d-110">The client calls the [**RtmGetEntityMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods) function, supplying the target client's handle.</span></span>

<span data-ttu-id="f005d-111">用戶端匯出的每個方法都是由其方法識別碼唯一識別。</span><span class="sxs-lookup"><span data-stu-id="f005d-111">Each method exported by a client is uniquely identified by its method identifier.</span></span> <span data-ttu-id="f005d-112">每個用戶端最多可以匯出32方法。</span><span class="sxs-lookup"><span data-stu-id="f005d-112">Each client can export up to 32 methods.</span></span> <span data-ttu-id="f005d-113">每個方法都會對應到 [**RTM \_ 實體 \_ 匯出 \_ 方法**](/windows/win32/api/rtmv2/nc-rtmv2-_entity_method)結構的 **MethodType** 成員中設定的位。</span><span class="sxs-lookup"><span data-stu-id="f005d-113">Each method corresponds to a bit set in the **MethodType** member of the [**RTM\_ENTITY\_EXPORT\_METHOD**](/windows/win32/api/rtmv2/nc-rtmv2-_entity_method) structure.</span></span> <span data-ttu-id="f005d-114">若要叫用多個方法，用戶端應該針對這些方法執行識別碼的邏輯 OR。</span><span class="sxs-lookup"><span data-stu-id="f005d-114">To invoke multiple methods, the client should perform a logical OR of the identifiers for those methods.</span></span> <span data-ttu-id="f005d-115">當執行通訊協定時，必須指定每個通訊協定的輸入和輸出結構的語法和語義。</span><span class="sxs-lookup"><span data-stu-id="f005d-115">The syntax and semantics of input and output structures for each protocol must be specified when the protocol is implemented.</span></span>

> [!Note]  
> <span data-ttu-id="f005d-116">對應到 **MethodType** 成員下半部所設定之位的方法識別碼值 (較低的16位) 是由 Microsoft 所保留。</span><span class="sxs-lookup"><span data-stu-id="f005d-116">Method identifier values that correspond to a bit set in the lower half of the **MethodType** member (the lower 16 bits) are reserved by Microsoft.</span></span>

 

<span data-ttu-id="f005d-117">若要叫用第二個用戶端的方法，用戶端會呼叫 [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) 函數。</span><span class="sxs-lookup"><span data-stu-id="f005d-117">To invoke a second client's method, a client calls the [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) function.</span></span> <span data-ttu-id="f005d-118">路由表管理員會仲裁所有呼叫用戶端方法的要求。</span><span class="sxs-lookup"><span data-stu-id="f005d-118">The routing table manager arbitrates all requests to invoke a client's methods.</span></span> <span data-ttu-id="f005d-119">路由表管理員在用戶端之間仲裁時，會執行兩個函式：</span><span class="sxs-lookup"><span data-stu-id="f005d-119">The routing table manager performs two functions when it arbitrates between clients:</span></span>

-   <span data-ttu-id="f005d-120">防止第二個用戶端針對正在取消註冊的用戶端叫用方法。</span><span class="sxs-lookup"><span data-stu-id="f005d-120">Preventing the second client from invoking a method for a client that is unregistering.</span></span>
-   <span data-ttu-id="f005d-121">在封鎖方法時保留「叫用」要求，並允許在解除封鎖方法時繼續要求。</span><span class="sxs-lookup"><span data-stu-id="f005d-121">Holding an "invoke" request when methods are blocked, and allowing the request to continue when the methods are unblocked.</span></span>

<span data-ttu-id="f005d-122">如果用戶端必須防止其他用戶端執行其方法，則用戶端可以呼叫 [**RtmBlockMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods)。</span><span class="sxs-lookup"><span data-stu-id="f005d-122">If a client must prevent other clients from executing its methods, the client can call [**RtmBlockMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods).</span></span> <span data-ttu-id="f005d-123">路由表管理員將不允許對 [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) 進行呼叫，直到用戶端再次解除封鎖其方法為止。</span><span class="sxs-lookup"><span data-stu-id="f005d-123">The routing table manager will not allow a call to [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) to be processed until the client unblocks its methods again.</span></span>

<span data-ttu-id="f005d-124">用戶端通常會在對用戶端之間交換的私用資料進行變更時封鎖方法。</span><span class="sxs-lookup"><span data-stu-id="f005d-124">Clients typically block methods when making changes to the private data that is exchanged between clients.</span></span> <span data-ttu-id="f005d-125">封鎖方法是選擇性的動作。</span><span class="sxs-lookup"><span data-stu-id="f005d-125">Blocking methods is an optional action.</span></span> <span data-ttu-id="f005d-126">用戶端也可以使用內部鎖定來防止其他用戶端叫用方法。</span><span class="sxs-lookup"><span data-stu-id="f005d-126">A client can also use internal locks to prevent other clients from invoking methods.</span></span>

<span data-ttu-id="f005d-127">如需示範如何使用這些函數的範例程式碼，請參閱 [取得和呼叫用戶端的匯出方法](obtain-and-call-the-exported-methods-for-a-client.md)。</span><span class="sxs-lookup"><span data-stu-id="f005d-127">For sample code that shows how to use these functions, see [Obtain and Call the Exported Methods for a Client](obtain-and-call-the-exported-methods-for-a-client.md).</span></span>

 

 




