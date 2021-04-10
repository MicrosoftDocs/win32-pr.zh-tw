---
title: 在用戶端上使用 Transport-Level 安全性
description: 用戶端會指定當用戶端建立字串系結時，伺服器模擬用戶端的方式。
ms.assetid: 0d02b7f2-4dcb-41e8-829c-6942dfdcd4c6
keywords:
- 在用戶端上使用傳輸層級安全性的遠端程序呼叫 RPC、工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10360d5b8d11640803e31ee1d1d0490a6edfdf7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933535"
---
# <a name="using-transport-level-security-on-the-client"></a><span data-ttu-id="cf212-104">在用戶端上使用 Transport-Level 安全性</span><span class="sxs-lookup"><span data-stu-id="cf212-104">Using Transport-Level Security on the Client</span></span>

<span data-ttu-id="cf212-105">用戶端會指定當用戶端建立字串系結時，伺服器模擬用戶端的方式。</span><span class="sxs-lookup"><span data-stu-id="cf212-105">The client specifies how the server impersonates the client when the client establishes the string binding.</span></span> <span data-ttu-id="cf212-106">這項 QOS 資訊是在字串系結中以端點選項的形式提供。</span><span class="sxs-lookup"><span data-stu-id="cf212-106">This QOS information is provided as an endpoint option in the string binding.</span></span> <span data-ttu-id="cf212-107">用戶端可以指定模擬、動態或靜態追蹤的層級，以及僅限有效的旗標。</span><span class="sxs-lookup"><span data-stu-id="cf212-107">The client can specify the level of impersonation, dynamic or static tracking, and the effective-only flag.</span></span>

<span data-ttu-id="cf212-108">**提供伺服器的服務品質資訊**</span><span class="sxs-lookup"><span data-stu-id="cf212-108">**To supply quality-of-service information for the server**</span></span>

1.  <span data-ttu-id="cf212-109">用戶端會呼叫 [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) ，以在正確的字串系結內容中建立元件字串，包括端點選項。</span><span class="sxs-lookup"><span data-stu-id="cf212-109">The client calls [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) to create the component strings, including endpoint options, in the correct string-binding context.</span></span>
2.  <span data-ttu-id="cf212-110">用戶端會呼叫 [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) 來取得新的系結控制碼，並套用用戶端的服務品質資訊。</span><span class="sxs-lookup"><span data-stu-id="cf212-110">The client calls [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) to obtain a new binding handle and to apply the quality-of-service information for the client.</span></span>
3.  <span data-ttu-id="cf212-111">用戶端會使用控制碼進行遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="cf212-111">The client makes remote procedure calls using the handle.</span></span>

<span data-ttu-id="cf212-112">Microsoft RPC 只支援 [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np) 和 [**ncalrpc**](/windows/desktop/Midl/ncalrpc)上的 Windows 安全性功能。</span><span class="sxs-lookup"><span data-stu-id="cf212-112">Microsoft RPC supports Windows security features only on [**ncacn\_np**](/windows/desktop/Midl/ncacn-np) and [**ncalrpc**](/windows/desktop/Midl/ncalrpc).</span></span> <span data-ttu-id="cf212-113">其他傳輸的安全性選項會被忽略。</span><span class="sxs-lookup"><span data-stu-id="cf212-113">Security options for other transports are ignored.</span></span>

<span data-ttu-id="cf212-114">用戶端可以將下列安全性參數與具名管道傳輸 [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np) 或 [**ncalrpc**](/windows/desktop/Midl/ncalrpc)的系結產生關聯：</span><span class="sxs-lookup"><span data-stu-id="cf212-114">The client can associate the following security parameters to the binding for the named-pipe transport [**ncacn\_np**](/windows/desktop/Midl/ncacn-np) or [**ncalrpc**](/windows/desktop/Midl/ncalrpc):</span></span>

-   <span data-ttu-id="cf212-115">識別、模擬或匿名。</span><span class="sxs-lookup"><span data-stu-id="cf212-115">Identification, Impersonation, or Anonymous.</span></span> <span data-ttu-id="cf212-116">指定使用的安全性類型。</span><span class="sxs-lookup"><span data-stu-id="cf212-116">Specifies the type of security used.</span></span> <span data-ttu-id="cf212-117">預設值是模擬。</span><span class="sxs-lookup"><span data-stu-id="cf212-117">The default is Impersonation.</span></span>
-   <span data-ttu-id="cf212-118">動態或靜態。</span><span class="sxs-lookup"><span data-stu-id="cf212-118">Dynamic or Static.</span></span> <span data-ttu-id="cf212-119">判斷與執行緒相關聯的安全性資訊是否為遠端程序呼叫 (靜態) 時所建立之安全性資訊的複本，或 (動態) 之安全性資訊的指標。</span><span class="sxs-lookup"><span data-stu-id="cf212-119">Determines whether security information associated with a thread is a copy of the security information created at the time the remote procedure call is made (static) or a pointer to the security information (dynamic).</span></span>

    <span data-ttu-id="cf212-120">靜態安全性資訊不會變更。</span><span class="sxs-lookup"><span data-stu-id="cf212-120">Static security information does not change.</span></span> <span data-ttu-id="cf212-121">動態設定會反映目前的安全性設定，包括在進行遠端程序呼叫之後所做的變更。</span><span class="sxs-lookup"><span data-stu-id="cf212-121">The dynamic setting reflects the current security settings, including changes made after the remote procedure call is made.</span></span> <span data-ttu-id="cf212-122">針對 [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np)，遠端具名管道連線的預設值是靜態的，針對本機具名管道連線，預設為動態。</span><span class="sxs-lookup"><span data-stu-id="cf212-122">For [**ncacn\_np**](/windows/desktop/Midl/ncacn-np), the default for remote named pipe connections is static, for local named pipe connections the default is dynamic.</span></span>

-   <span data-ttu-id="cf212-123">**TRUE** 或 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="cf212-123">**TRUE** or **FALSE**.</span></span> <span data-ttu-id="cf212-124">指定僅限有效旗標的值。</span><span class="sxs-lookup"><span data-stu-id="cf212-124">Specifies the value of the effective-only flag.</span></span> <span data-ttu-id="cf212-125">**TRUE** 值表示在呼叫時，只有在上設定為 on 的權杖許可權有效。</span><span class="sxs-lookup"><span data-stu-id="cf212-125">A value of **TRUE** indicates that only token privileges set to on at the time of the call are effective.</span></span> <span data-ttu-id="cf212-126">值為 **FALSE** 表示擁有權限都可使用，而且應用程式可以修改它們。</span><span class="sxs-lookup"><span data-stu-id="cf212-126">A value of **FALSE** indicates that all privileges are available and that the application can modify them.</span></span>

<span data-ttu-id="cf212-127">這些設定的任何組合都可以指派給系結，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="cf212-127">Any combination of these settings can be assigned to the binding, as shown in the following example:</span></span>

``` syntax
"Security=Identification Dynamic True"
"Security=Anonymous Static True"
"Security=Impersonation Static False"
```

<span data-ttu-id="cf212-128">預設安全性參數設定會根據傳輸通訊協定而有所不同。</span><span class="sxs-lookup"><span data-stu-id="cf212-128">Default security-parameter settings vary according to the transport protocol.</span></span>

<span data-ttu-id="cf212-129">如需端點選項語法的詳細資訊，請參閱 [端點](/windows/desktop/Midl/endpoint)。</span><span class="sxs-lookup"><span data-stu-id="cf212-129">For additional information about the syntax of the endpoint options, see [endpoint](/windows/desktop/Midl/endpoint).</span></span>

 

 