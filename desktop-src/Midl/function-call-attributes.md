---
title: 函式呼叫屬性
description: 程式可以在介面內的個別函式上使用這些屬性，而且只會影響該函數。
ms.assetid: c54dbcd9-46c9-4755-b4a8-0f78068920b7
keywords:
- IDL MIDL、屬性、函式呼叫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d53407abf464d7b201c49d9cb2b1d3f3625b9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675588"
---
# <a name="function-call-attributes"></a><span data-ttu-id="c1f78-104">函式呼叫屬性</span><span class="sxs-lookup"><span data-stu-id="c1f78-104">Function Call Attributes</span></span>

<span data-ttu-id="c1f78-105">程式可以在介面內的個別函式上使用這些屬性，而且只會影響該函數。</span><span class="sxs-lookup"><span data-stu-id="c1f78-105">Programs can use these attributes on individual functions within the interface, and affect only that function.</span></span>



| <span data-ttu-id="c1f78-106">屬性</span><span class="sxs-lookup"><span data-stu-id="c1f78-106">Attribute</span></span>                        | <span data-ttu-id="c1f78-107">使用方式</span><span class="sxs-lookup"><span data-stu-id="c1f78-107">Usage</span></span>                                                                                                                                                                                                                                                      |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1f78-108">**消息**</span><span class="sxs-lookup"><span data-stu-id="c1f78-108">**message**</span></span>](message.md)       | <span data-ttu-id="c1f78-109">遠端程序呼叫會被視為從用戶端到伺服器的非同步訊息。</span><span class="sxs-lookup"><span data-stu-id="c1f78-109">The remote procedure call is to be treated as an asynchronous message from the client to the server.</span></span> <span data-ttu-id="c1f78-110">用戶端會進行呼叫，並立即傳回，而實際的呼叫是由訊息佇列傳輸 ([**ncadg \_ mq**](ncadg-mq.md)) 處理。</span><span class="sxs-lookup"><span data-stu-id="c1f78-110">The client makes the call and returns immediately, while the actual call is handled by the message-queuing transport ([**ncadg\_mq**](ncadg-mq.md)).</span></span> |
| [<span data-ttu-id="c1f78-111">**也許**</span><span class="sxs-lookup"><span data-stu-id="c1f78-111">**maybe**</span></span>](maybe.md)           | <span data-ttu-id="c1f78-112">進行此遠端程序呼叫的用戶端不會預期會有任何回應，指出呼叫的傳遞或完成。</span><span class="sxs-lookup"><span data-stu-id="c1f78-112">The client making this remote procedure call does not expect any response indicating delivery or completion of the call.</span></span> <span data-ttu-id="c1f78-113">這與未預期回應但保證傳遞的 [**訊息**](message.md) 作業不同。</span><span class="sxs-lookup"><span data-stu-id="c1f78-113">This is in contrast to [**message**](message.md) operations where no response is expected but the delivery is guaranteed.</span></span>        |
| [<span data-ttu-id="c1f78-114">**廣播**</span><span class="sxs-lookup"><span data-stu-id="c1f78-114">**broadcast**</span></span>](broadcast.md)   | <span data-ttu-id="c1f78-115">遠端程序呼叫會傳送至網路上的所有伺服器。</span><span class="sxs-lookup"><span data-stu-id="c1f78-115">The remote procedure call is to be sent to all of the servers on the network.</span></span> <span data-ttu-id="c1f78-116">用戶端接受第一次傳回，則會捨棄其他伺服器的後續回復。</span><span class="sxs-lookup"><span data-stu-id="c1f78-116">The client accepts the first return, subsequent replies from other servers are discarded.</span></span>                                                                                    |
| [<span data-ttu-id="c1f78-117">**idempotent**</span><span class="sxs-lookup"><span data-stu-id="c1f78-117">**idempotent**</span></span>](idempotent.md) | <span data-ttu-id="c1f78-118">呼叫不會變更狀態，而且每次使用相同的輸入參數呼叫時，都會傳回相同的資訊。</span><span class="sxs-lookup"><span data-stu-id="c1f78-118">The call does not change state and returns the same information each time it is called with the same input parameters.</span></span>                                                                                                                                     |
| [<span data-ttu-id="c1f78-119">**回撥**</span><span class="sxs-lookup"><span data-stu-id="c1f78-119">**callback**</span></span>](callback.md)     | <span data-ttu-id="c1f78-120">指定位於用戶端應用程式中的函式，伺服器可呼叫該函式來取得用戶端的資訊。</span><span class="sxs-lookup"><span data-stu-id="c1f78-120">Designates a function that resides in the client application, which the server can call to obtain information from the client.</span></span>                                                                                                                             |
| [<span data-ttu-id="c1f78-121">**呼叫 \_ as**</span><span class="sxs-lookup"><span data-stu-id="c1f78-121">**call\_as**</span></span>](call-as.md)      | <span data-ttu-id="c1f78-122">將不可遠端處理函數對應至遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="c1f78-122">Maps a nonremotable function to a remote procedure call.</span></span>                                                                                                                                                                                                   |
| [<span data-ttu-id="c1f78-123">**當地**</span><span class="sxs-lookup"><span data-stu-id="c1f78-123">**local**</span></span>](local.md)           | <span data-ttu-id="c1f78-124">指定 MIDL 不會產生 stub 程式碼的本機程式。</span><span class="sxs-lookup"><span data-stu-id="c1f78-124">Designates a local procedure for which MIDL does not generate stub code.</span></span>                                                                                                                                                                                   |



 

<span data-ttu-id="c1f78-125">在非 [**物件**](object.md) 介面上，您也可以將 [**內容 \_ 控制碼**](context-handle.md) 屬性套用至函數，以指定傳回值的特性。</span><span class="sxs-lookup"><span data-stu-id="c1f78-125">On non-[**object**](object.md) interfaces, you can also apply the [**context\_handle**](context-handle.md) attribute to a function to specify characteristics of the return value.</span></span>

 

 




