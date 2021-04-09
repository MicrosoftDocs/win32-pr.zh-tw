---
title: 非同步呼叫的因果順序
description: 在非同步 RPC 應用程式中，用戶端執行緒可能會先在系結控制碼上進行第二次非同步呼叫，才能在該控制碼上進行較早的呼叫完成。
ms.assetid: 69beb3a4-39ae-4e3f-bb7d-31519278334d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 754ae4733e5a3936bdd28fef72b9560fb9c9dfcd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021369"
---
# <a name="causal-ordering-of-asynchronous-calls"></a><span data-ttu-id="5222c-103">非同步呼叫的因果順序</span><span class="sxs-lookup"><span data-stu-id="5222c-103">Causal Ordering of Asynchronous Calls</span></span>

<span data-ttu-id="5222c-104">在非同步 RPC 應用程式中，用戶端執行緒可能會先在系結控制碼上進行第二次非同步呼叫，才能在該控制碼上進行較早的呼叫完成。</span><span class="sxs-lookup"><span data-stu-id="5222c-104">In an asynchronous RPC application, it is possible for a client thread to make a second asynchronous call on a binding handle before an earlier call made on that handle has completed.</span></span> <span data-ttu-id="5222c-105">RPC 執行時間程式庫會處理此情況，如下所示：</span><span class="sxs-lookup"><span data-stu-id="5222c-105">The RPC run-time library handles this situation as follows:</span></span>

-   <span data-ttu-id="5222c-106">非同步 RPC 機制可保證在相同的執行緒上對相同的系結控制碼（在相同的安全性層級上）發出的非同步呼叫，會依其進行順序分派。</span><span class="sxs-lookup"><span data-stu-id="5222c-106">The asynchronous RPC mechanism guarantees that asynchronous calls made on the same binding handle, on the same thread, at the same security level, are dispatched in the order they were made.</span></span> <span data-ttu-id="5222c-107">實際執行的呼叫可能會依順序發生。</span><span class="sxs-lookup"><span data-stu-id="5222c-107">Actual execution of the calls may occur out of order.</span></span>
-   <span data-ttu-id="5222c-108">如同同步呼叫，來自不同用戶端執行緒的非同步遠端程序呼叫會同時執行。</span><span class="sxs-lookup"><span data-stu-id="5222c-108">As with synchronous calls, asynchronous remote procedure calls from different client threads execute simultaneously.</span></span>
-   <span data-ttu-id="5222c-109">如果用戶端應用程式的非同步呼叫後面接著一或多個同步呼叫，則非同步呼叫可以在執行同步呼叫時執行。</span><span class="sxs-lookup"><span data-stu-id="5222c-109">If an asynchronous call from a client application is followed by one or more synchronous calls, the asynchronous call can execute while the synchronous calls are executing.</span></span> <span data-ttu-id="5222c-110">無論非同步呼叫的狀態為何，同步呼叫都會依伺服器接收的順序來執行。</span><span class="sxs-lookup"><span data-stu-id="5222c-110">Regardless of the status of the asynchronous call, the synchronous calls are executed in the order in which they are received by the server.</span></span>
-   <span data-ttu-id="5222c-111">如果用戶端應用程式選取特定系結控制碼的 noncausal 順序，則會停用該控制碼的序列化。</span><span class="sxs-lookup"><span data-stu-id="5222c-111">If a client application selects noncausal ordering for a particular binding handle, it disables serialization for that handle.</span></span> <span data-ttu-id="5222c-112">應用程式會藉由呼叫 [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) 並將 *Option* 參數設定為 [RPC \_ C OPT 系結 noncausal] \_ \_ \_ ，並將 [ *OptionValue* ] 參數設為 **TRUE**，藉以啟用 noncausal 排序</span><span class="sxs-lookup"><span data-stu-id="5222c-112">Applications enable noncausal ordering by calling [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) with the *Option* parameter set to RPC\_C\_OPT\_BINDING\_NONCAUSAL and the *OptionValue* parameter set to **TRUE**.</span></span> <span data-ttu-id="5222c-113">如需詳細資訊，請參閱系結 [選項常數](binding-option-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="5222c-113">For details, see [Binding Option Constants](binding-option-constants.md).</span></span>

 

 




