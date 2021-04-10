---
title: 執行緒安全性
description: 此 API 中的所有函數都可以安全地從不同的執行緒呼叫。 不過，以參數形式傳遞給函式的每個物件都有特定的執行緒行為，如下所述。
ms.assetid: 712d6750-884e-421a-8ecf-efcd4ec9b21d
keywords:
- 適用于 Windows 的執行緒安全 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fed84cac9634148742c92f1b0d4b4ecdb905ac42
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103684245"
---
# <a name="thread-safety"></a><span data-ttu-id="92738-107">執行緒安全性</span><span class="sxs-lookup"><span data-stu-id="92738-107">Thread Safety</span></span>

<span data-ttu-id="92738-108">此 API 中的所有函數都可以安全地從不同的執行緒呼叫。</span><span class="sxs-lookup"><span data-stu-id="92738-108">All functions in this API are safe to call concurrently from different threads.</span></span> <span data-ttu-id="92738-109">不過，以參數形式傳遞給函式的每個物件都有特定的執行緒行為，如下所述。</span><span class="sxs-lookup"><span data-stu-id="92738-109">However, each object passed as a parameter to the functions have specific threading behavior, as described below.</span></span>


<span data-ttu-id="92738-110">下列控制碼為單一執行緒，且不支援特定實例的並行作業：</span><span class="sxs-lookup"><span data-stu-id="92738-110">The following handles are single threaded and do not support concurrent operations for a particular instance:</span></span>

-   [<span data-ttu-id="92738-111">WS \_ 堆積</span><span class="sxs-lookup"><span data-stu-id="92738-111">WS\_HEAP</span></span>](ws-heap.md)
-   [<span data-ttu-id="92738-112">WS \_ 訊息</span><span class="sxs-lookup"><span data-stu-id="92738-112">WS\_MESSAGE</span></span>](ws-message.md)
-   [<span data-ttu-id="92738-113">WS \_ XML \_ 緩衝區</span><span class="sxs-lookup"><span data-stu-id="92738-113">WS\_XML\_BUFFER</span></span>](ws-xml-buffer.md)
-   [<span data-ttu-id="92738-114">WS \_ XML \_ 讀取器</span><span class="sxs-lookup"><span data-stu-id="92738-114">WS\_XML\_READER</span></span>](ws-xml-reader.md)
-   [<span data-ttu-id="92738-115">WS \_ XML \_ 寫入器</span><span class="sxs-lookup"><span data-stu-id="92738-115">WS\_XML\_WRITER</span></span>](ws-xml-writer.md)
-   [<span data-ttu-id="92738-116">WS \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="92738-116">WS\_ERROR</span></span>](ws-error.md)
-   [<span data-ttu-id="92738-117">WS \_ 操作 \_ 內容</span><span class="sxs-lookup"><span data-stu-id="92738-117">WS\_OPERATION\_CONTEXT</span></span>](ws-operation-context.md)
-   [<span data-ttu-id="92738-118">WS \_ 原則</span><span class="sxs-lookup"><span data-stu-id="92738-118">WS\_POLICY</span></span>](ws-policy.md)
-   [<span data-ttu-id="92738-119">WS \_ 中繼資料</span><span class="sxs-lookup"><span data-stu-id="92738-119">WS\_METADATA</span></span>](ws-metadata.md)
-   [<span data-ttu-id="92738-120">WS \_ 安全性 \_ 權杖</span><span class="sxs-lookup"><span data-stu-id="92738-120">WS\_SECURITY\_TOKEN</span></span>](ws-security-token.md)
-   [<span data-ttu-id="92738-121">WS \_ 安全性 \_ 內容</span><span class="sxs-lookup"><span data-stu-id="92738-121">WS\_SECURITY\_CONTEXT</span></span>](ws-security-context.md)

<span data-ttu-id="92738-122">下列控制碼是無限制執行緒，可支援特定實例的並行作業：</span><span class="sxs-lookup"><span data-stu-id="92738-122">The following handles are free threaded and do support concurrent operations for a particular instance:</span></span>

-   [<span data-ttu-id="92738-123">WS \_ 通道</span><span class="sxs-lookup"><span data-stu-id="92738-123">WS\_CHANNEL</span></span>](ws-channel.md)
-   [<span data-ttu-id="92738-124">WS \_ 接聽程式</span><span class="sxs-lookup"><span data-stu-id="92738-124">WS\_LISTENER</span></span>](ws-listener.md)
-   [<span data-ttu-id="92738-125">WS \_ 服務 \_ 主機</span><span class="sxs-lookup"><span data-stu-id="92738-125">WS\_SERVICE\_HOST</span></span>](ws-service-host.md)
-   [<span data-ttu-id="92738-126">WS \_ 服務 \_ PROXY</span><span class="sxs-lookup"><span data-stu-id="92738-126">WS\_SERVICE\_PROXY</span></span>](ws-service-proxy.md)

<span data-ttu-id="92738-127">針對所有這些控制碼，執行緒是以作業的方式定義， (不) 函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="92738-127">For all these handles, threading is defined in terms of operations (not function calls).</span></span> <span data-ttu-id="92738-128">以同步方式叫用的函式與非同步叫用的函式會有不同的定義作業：</span><span class="sxs-lookup"><span data-stu-id="92738-128">An operation is defined differently for functions invoked synchronously versus functions invoked asynchronously:</span></span>

-   <span data-ttu-id="92738-129">如果是以同步方式叫用的函式，則作業會在函數執行期間暫止。</span><span class="sxs-lookup"><span data-stu-id="92738-129">For functions invoked synchronously, the operation is pending during the execution of the function.</span></span>
-   <span data-ttu-id="92738-130">針對以非同步方式叫用的函式，如果函式傳回 **非 \_ \_ ASYNC** 的傳回碼，則作業會在函數執行期間暫止。</span><span class="sxs-lookup"><span data-stu-id="92738-130">For functions invoked asynchronously, if the function returns a return code other than **WS\_S\_ASYNC** the operation is pending during the execution of the function.</span></span> <span data-ttu-id="92738-131">但是，如果函式傳回 **ws \_ S \_ async** ，則作業會暫止，直到 [**叫用 WS \_ ASYNC \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) 為止。</span><span class="sxs-lookup"><span data-stu-id="92738-131">If the function returns **WS\_S\_ASYNC** , however, the operation is pending until the [**WS\_ASYNC\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) is invoked.</span></span> <span data-ttu-id="92738-132">如需非同步叫用函數的詳細資訊，請參閱 [非同步模型](asynchronous-model.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="92738-132">For more information about invoking functions asynchronously, see the [Asynchronous Model](asynchronous-model.md) topic.</span></span> <span data-ttu-id="92738-133">如需錯誤碼，請參閱 [Windows Web 服務傳回值](windows-web-services-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="92738-133">For error codes, see [Windows Web Services Return Values](windows-web-services-return-values.md).</span></span>

<span data-ttu-id="92738-134">若無法追蹤物件的執行緒合約，將會導致未定義的行為。</span><span class="sxs-lookup"><span data-stu-id="92738-134">Failure to follow the threading contract for an object will result in undefined behavior.</span></span>

 

 




