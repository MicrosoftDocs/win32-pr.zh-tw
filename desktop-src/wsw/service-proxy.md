---
title: 服務 Proxy
description: 服務 proxy 是服務的用戶端 proxy。
ms.assetid: e1a5bf5e-dbc1-43e3-981b-7db4caa08bdc
keywords:
- 適用于 Windows 的服務 Proxy Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac82509fa155084cbb4ca3e6b9437728c6f853a
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "106988092"
---
# <a name="service-proxy"></a><span data-ttu-id="6b443-106">服務 Proxy</span><span class="sxs-lookup"><span data-stu-id="6b443-106">Service Proxy</span></span>

<span data-ttu-id="6b443-107">服務 proxy 是服務的用戶端 proxy。</span><span class="sxs-lookup"><span data-stu-id="6b443-107">A service proxy is the client side proxy for a service.</span></span> <span data-ttu-id="6b443-108">服務 proxy 可讓應用程式透過[通道](channel.md)傳送和接收[訊息](message.md)，做為方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="6b443-108">The service proxy enables applications to send and receive [messages](message.md) over a [channel](channel.md) as method calls.</span></span>

<span data-ttu-id="6b443-109">服務 proxy 會視需要建立、開啟、用來呼叫服務，並在不再需要時關閉。</span><span class="sxs-lookup"><span data-stu-id="6b443-109">Service proxies are created as needed, opened, used to call a service, and closed when no longer needed.</span></span> <span data-ttu-id="6b443-110">或者，應用程式可以重複使用服務 proxy 來重複連接至相同的服務，而不需支付 initialising 服務 proxy 所需的時間和資源。</span><span class="sxs-lookup"><span data-stu-id="6b443-110">Alternatively, an application may reuse a service proxy to connect repeatedly to the same service without the expenditure of time and resources required for initialising a service proxy more than once.</span></span> <span data-ttu-id="6b443-111">下圖說明服務 proxy 可能狀態的流程，以及從某個狀態到另一個狀態的函式呼叫或事件的流程。</span><span class="sxs-lookup"><span data-stu-id="6b443-111">The following diagram illustrates the flow of the possible states of the service proxy and the function calls or events that lead from one state to another.</span></span>

![顯示服務 proxy 狀態的圖表，以及從某個狀態到另一個狀態的函式呼叫或事件。](images/serviceproxystates.png)

<span data-ttu-id="6b443-113">這些服務 proxy 狀態是以 [**WS \_ 服務 \_ proxy \_ 狀態**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) 列舉來列舉。</span><span class="sxs-lookup"><span data-stu-id="6b443-113">These service proxy states are enumerated in the [**WS\_SERVICE\_PROXY\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) enumeration.</span></span>

<span data-ttu-id="6b443-114">如先前的圖表和下列程式碼所示，服務 proxy 是透過呼叫 [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) 函式來建立。</span><span class="sxs-lookup"><span data-stu-id="6b443-114">As the preceding diagram and the following code illustrate, a service proxy is created by a call to the [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) function.</span></span> <span data-ttu-id="6b443-115">作為此呼叫的參數，WWSAPI 提供下列列舉：</span><span class="sxs-lookup"><span data-stu-id="6b443-115">As parameters for this call, WWSAPI provides the following enumerations:</span></span>

-   [<span data-ttu-id="6b443-116">**WS \_ 通道 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="6b443-116">**WS\_CHANNEL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)
-   [<span data-ttu-id="6b443-117">**WS \_ 通道系結 \_**</span><span class="sxs-lookup"><span data-stu-id="6b443-117">**WS\_CHANNEL\_BINDING**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)

<span data-ttu-id="6b443-118">它也接受使用下列資料類型的選擇性參數：</span><span class="sxs-lookup"><span data-stu-id="6b443-118">It also accepts optional parameters using the following data types:</span></span>

-   [<span data-ttu-id="6b443-119">**WS \_ PROXY \_ 屬性 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="6b443-119">**WS\_PROXY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)
-   [<span data-ttu-id="6b443-120">**WS \_ 安全性 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="6b443-120">**WS\_SECURITY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_description)

<span data-ttu-id="6b443-121">建立服務 proxy 時， **WsCreateServiceProxy** 函式會透過 out 參數，傳回服務 proxy [Ws-management （WS \_ 服務 \_](ws-service-proxy.md)proxy）的參考。</span><span class="sxs-lookup"><span data-stu-id="6b443-121">When the service proxy has been created, the **WsCreateServiceProxy** function returns a reference to the service proxy, [WS\_SERVICE\_PROXY](ws-service-proxy.md), through an out parameter.</span></span>

``` syntax
WS_SERVICE_PROXY* serviceProxy = NULL;
hr = WsCreateServiceProxy (
    WS_TCP_CHANNEL_BINDING, 
    WS_CHANNEL_TYPE_DUPLEX_SESSION, 
    NULL, 
    NULL, 
    0, 
    NULL,
    0,
    &serviceProxy, 
    error);
```

<span data-ttu-id="6b443-122">建立服務 proxy 之後，應用程式可以藉由呼叫 [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) 函式來開啟服務 proxy 來與服務通訊，並傳遞包含要連接之服務端點網路位址的 [**位址**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) 結構。</span><span class="sxs-lookup"><span data-stu-id="6b443-122">When the service proxy has been created, the application can open the service proxy for communication to a service by calling the [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) function, passing an [**address**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) structure containing the network address of the service endpoint to connect to.</span></span>

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
address.uri.chars = "net.tcp://localhost/example";
address.uri.length = wcslen("net.tcp://localhost/example";);
hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error);
```

<span data-ttu-id="6b443-123">開啟服務 proxy 之後，應用程式就可以使用它來對服務進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="6b443-123">When the service proxy has been opened, the application can use it to make calls to the service.</span></span>

``` syntax
hr = Add(
    serviceProxy, 
    1, 
    2, 
    &result, 
    NULL, 
    0, 
    NULL, 
    error);
```

<span data-ttu-id="6b443-124">當應用程式不再需要服務 proxy 時，它會藉由呼叫 [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) 函數來關閉服務 proxy。</span><span class="sxs-lookup"><span data-stu-id="6b443-124">When the application no longer needs the service proxy, it closes the service proxy by calling the [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) function.</span></span> <span data-ttu-id="6b443-125">它也會藉由呼叫 [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy)來釋出相關聯的記憶體。</span><span class="sxs-lookup"><span data-stu-id="6b443-125">It also frees the associated memory by calling [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy).</span></span>

``` syntax
hr = WsCloseServiceProxy(
    serviceProxy, 
    NULL, 
    error);
```

``` syntax
hr = WsFreeServiceProxy(
    serviceProxy, 
    error);
```

## <a name="reusing-the-service-proxy"></a><span data-ttu-id="6b443-126">重複使用服務 Proxy</span><span class="sxs-lookup"><span data-stu-id="6b443-126">Reusing the Service Proxy</span></span>

<span data-ttu-id="6b443-127">或者，在呼叫 [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) 之後，應用程式可以藉由呼叫 [**WsResetServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy) 函數來重複使用服務 proxy。</span><span class="sxs-lookup"><span data-stu-id="6b443-127">Alternatively, after calling [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) an application can reuse the service proxy by calling the [**WsResetServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy) function.</span></span>

``` syntax
hr = WsResetServiceProxy(
    serviceProxy, 
    error);
```

<span data-ttu-id="6b443-128">如需有關如何在不同的環境中使用服務 proxy 的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="6b443-128">For more information on how service proxies are used in different contexts, see the following topics:</span></span>

-   [<span data-ttu-id="6b443-129">服務 Proxy 和會話</span><span class="sxs-lookup"><span data-stu-id="6b443-129">Service Proxy and Sessions</span></span>](service-proxy-and-sessions.md)
-   [<span data-ttu-id="6b443-130">服務作業</span><span class="sxs-lookup"><span data-stu-id="6b443-130">Service Operation</span></span>](service-operation.md)
-   [<span data-ttu-id="6b443-131">用戶端服務作業</span><span class="sxs-lookup"><span data-stu-id="6b443-131">Client Side Service Operations</span></span>](client-side-service-operations.md)
-   [<span data-ttu-id="6b443-132">HttpCalculatorClientExample</span><span class="sxs-lookup"><span data-stu-id="6b443-132">HttpCalculatorClientExample</span></span>](httpcalculatorclientexample.md)

### <a name="security"></a><span data-ttu-id="6b443-133">安全性</span><span class="sxs-lookup"><span data-stu-id="6b443-133">Security</span></span>

<span data-ttu-id="6b443-134">當您使用 WWSAPI 服務 proxy API 時，應謹慎注意下列應用程式設計考慮：</span><span class="sxs-lookup"><span data-stu-id="6b443-134">Following application design considerations should be carefully noted when you use the WWSAPI service proxy API:</span></span>

-   <span data-ttu-id="6b443-135">服務 proxy 將不會對基本設定檔2.0 驗證和 XML 序列化以外的資料執行任何驗證。</span><span class="sxs-lookup"><span data-stu-id="6b443-135">The service proxy will not perform any validation of the data beyond Basic Profile 2.0 validation and XML serialization.</span></span> <span data-ttu-id="6b443-136">應用程式必須負責驗證它在呼叫過程中收到的參數所包含的資料。</span><span class="sxs-lookup"><span data-stu-id="6b443-136">It is the responsibility of the application to validate the data contained in the parameters it receives back as part of the call.</span></span>
-   <span data-ttu-id="6b443-137">使用 [**ws \_ proxy \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) 列舉值 **ws \_ proxy \_ 屬性 \_ 最大 \_ 暫 \_** 止的呼叫，在服務 proxy 上設定暫止呼叫的最大數目，針對執行緩慢的伺服器提供保護。</span><span class="sxs-lookup"><span data-stu-id="6b443-137">Configuring the maximum number of pending calls on the service proxy, by using the [**WS\_PROXY\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) enumeration value **WS\_PROXY\_PROPERTY\_MAX\_PENDING\_CALLS**, provides protection against a slow running server.</span></span> <span data-ttu-id="6b443-138">預設的最大值為100。</span><span class="sxs-lookup"><span data-stu-id="6b443-138">The default maximum is 100.</span></span> <span data-ttu-id="6b443-139">應用程式必須謹慎修改預設值。</span><span class="sxs-lookup"><span data-stu-id="6b443-139">Applications must be careful in modifying the defaults.</span></span>
-   <span data-ttu-id="6b443-140">除了用來與伺服器通訊的 [**WS \_ 安全性 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) 結構中指定的以外，服務 proxy 不提供任何安全性保證。</span><span class="sxs-lookup"><span data-stu-id="6b443-140">The service proxy provides no security guarantees beyond those specified in the [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) structure used to communicate with the server.</span></span>
-   <span data-ttu-id="6b443-141">當您修改服務 proxy 上的 [訊息](message.md) 和 [通道](channel.md) 預設值時，請務必小心。</span><span class="sxs-lookup"><span data-stu-id="6b443-141">Take care when you modifying [message](message.md) and [channel](channel.md) defaults on the service proxy.</span></span> <span data-ttu-id="6b443-142">在修改任何相關屬性之前，請先閱讀與訊息和通道相關聯的安全性考慮。</span><span class="sxs-lookup"><span data-stu-id="6b443-142">Read the security considerations associated with messages and channels before you modify any of the related properties.</span></span>
-   <span data-ttu-id="6b443-143">服務 proxy 會加密其保留在記憶體中的所有認證。</span><span class="sxs-lookup"><span data-stu-id="6b443-143">Service proxy encrypts all credentials that it keeps in memory.</span></span>

<span data-ttu-id="6b443-144">下列 API 元素與服務 proxy 相關。</span><span class="sxs-lookup"><span data-stu-id="6b443-144">The following API elements relate to service proxies.</span></span>

| <span data-ttu-id="6b443-145">回呼</span><span class="sxs-lookup"><span data-stu-id="6b443-145">Callback</span></span>                                                          | <span data-ttu-id="6b443-146">Description</span><span class="sxs-lookup"><span data-stu-id="6b443-146">Description</span></span>                                                                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b443-147">**WS \_ PROXY \_ 訊息 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="6b443-147">**WS\_PROXY\_MESSAGE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback) | <span data-ttu-id="6b443-148">當輸入訊息的標頭即將透過傳送，或只接收輸出訊息標頭時叫用。</span><span class="sxs-lookup"><span data-stu-id="6b443-148">Invoked when the headers of the input message are about to be sent through or when an output message headers are just received.</span></span> |



 



| <span data-ttu-id="6b443-149">列舉型別</span><span class="sxs-lookup"><span data-stu-id="6b443-149">Enumeration</span></span>                                                 | <span data-ttu-id="6b443-150">描述</span><span class="sxs-lookup"><span data-stu-id="6b443-150">Description</span></span>                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b443-151">**WS \_ 呼叫 \_ 屬性 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="6b443-151">**WS\_CALL\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id)       | <span data-ttu-id="6b443-152">列舉選擇性參數，以設定用戶端服務作業的呼叫。</span><span class="sxs-lookup"><span data-stu-id="6b443-152">Enumerates optional parameters for configuring a call on a client side service operation.</span></span> |
| [<span data-ttu-id="6b443-153">**WS \_ PROXY \_ 屬性 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="6b443-153">**WS\_PROXY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)     | <span data-ttu-id="6b443-154">列舉用來設定服務 proxy 的選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="6b443-154">Enumerates optional parameters for configuring the service proxy.</span></span>                         |
| [<span data-ttu-id="6b443-155">**WS \_ 服務 \_ PROXY \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="6b443-155">**WS\_SERVICE\_PROXY\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) | <span data-ttu-id="6b443-156">服務 proxy 的狀態。</span><span class="sxs-lookup"><span data-stu-id="6b443-156">The state of the service proxy.</span></span>                                                           |



 



| <span data-ttu-id="6b443-157">函式</span><span class="sxs-lookup"><span data-stu-id="6b443-157">Function</span></span>                                                       | <span data-ttu-id="6b443-158">描述</span><span class="sxs-lookup"><span data-stu-id="6b443-158">Description</span></span>                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="6b443-159">**WsAbandonCall**</span><span class="sxs-lookup"><span data-stu-id="6b443-159">**WsAbandonCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)                         | <span data-ttu-id="6b443-160">放棄指定服務 proxy 上的指定呼叫。</span><span class="sxs-lookup"><span data-stu-id="6b443-160">Abandons a specified call on a specified service proxy.</span></span>                           |
| [<span data-ttu-id="6b443-161">**WsAbortServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="6b443-161">**WsAbortServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy)             | <span data-ttu-id="6b443-162">取消指定的服務 proxy 上所有暫止的輸入和輸出。</span><span class="sxs-lookup"><span data-stu-id="6b443-162">Cancels all pending input and output on a specified service proxy.</span></span>                |
| [<span data-ttu-id="6b443-163">**WsCall**</span><span class="sxs-lookup"><span data-stu-id="6b443-163">**WsCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscall)                                       | <span data-ttu-id="6b443-164">僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="6b443-164">Internal only.</span></span> <span data-ttu-id="6b443-165">將引數序列化為訊息，並透過通道傳送。</span><span class="sxs-lookup"><span data-stu-id="6b443-165">Serializes arguments into a message and sends it over the channel.</span></span> |
| [<span data-ttu-id="6b443-166">**WsCloseServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="6b443-166">**WsCloseServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy)             | <span data-ttu-id="6b443-167">關閉服務 proxy 以進行通訊。</span><span class="sxs-lookup"><span data-stu-id="6b443-167">Closes a service proxy for communication.</span></span>                                         |
| [<span data-ttu-id="6b443-168">**WsCreateServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="6b443-168">**WsCreateServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)           | <span data-ttu-id="6b443-169">建立服務 proxy。</span><span class="sxs-lookup"><span data-stu-id="6b443-169">Creates a service proxy.</span></span>                                                          |
| [<span data-ttu-id="6b443-170">**WsFreeServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="6b443-170">**WsFreeServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy)               | <span data-ttu-id="6b443-171">釋放與服務 proxy 相關聯的記憶體。</span><span class="sxs-lookup"><span data-stu-id="6b443-171">Releases the memory associated with a service proxy.</span></span>                              |
| [<span data-ttu-id="6b443-172">**WsGetServiceProxyProperty**</span><span class="sxs-lookup"><span data-stu-id="6b443-172">**WsGetServiceProxyProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetserviceproxyproperty) | <span data-ttu-id="6b443-173">抓取指定的服務 proxy 屬性。</span><span class="sxs-lookup"><span data-stu-id="6b443-173">Retrieves a specified service proxy property.</span></span>                                     |
| [<span data-ttu-id="6b443-174">**WsOpenServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="6b443-174">**WsOpenServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy)               | <span data-ttu-id="6b443-175">開啟服務端點的服務 proxy。</span><span class="sxs-lookup"><span data-stu-id="6b443-175">Opens a service proxy to a service endpoint.</span></span>                                      |
| [<span data-ttu-id="6b443-176">**WsResetServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="6b443-176">**WsResetServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy)             | <span data-ttu-id="6b443-177">重設服務 proxy。</span><span class="sxs-lookup"><span data-stu-id="6b443-177">Resets service proxy.</span></span>                                                             |



 



| <span data-ttu-id="6b443-178">Handle</span><span class="sxs-lookup"><span data-stu-id="6b443-178">Handle</span></span>                                     | <span data-ttu-id="6b443-179">Description</span><span class="sxs-lookup"><span data-stu-id="6b443-179">Description</span></span>                                       |
|--------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="6b443-180">WS \_ 服務 \_ PROXY</span><span class="sxs-lookup"><span data-stu-id="6b443-180">WS\_SERVICE\_PROXY</span></span>](ws-service-proxy.md) | <span data-ttu-id="6b443-181">用來參考服務 proxy 的不透明類型。</span><span class="sxs-lookup"><span data-stu-id="6b443-181">An opaque type used to reference a service proxy.</span></span> |



 



| <span data-ttu-id="6b443-182">結構</span><span class="sxs-lookup"><span data-stu-id="6b443-182">Structure</span></span>                                         | <span data-ttu-id="6b443-183">Description</span><span class="sxs-lookup"><span data-stu-id="6b443-183">Description</span></span>                 |
|---------------------------------------------------|-----------------------------|
| [<span data-ttu-id="6b443-184">**WS \_ CALL \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="6b443-184">**WS\_CALL\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_call_property)    | <span data-ttu-id="6b443-185">指定呼叫屬性。</span><span class="sxs-lookup"><span data-stu-id="6b443-185">Specifies a call property.</span></span>  |
| <span data-ttu-id="6b443-186">[**WS \_PROXY \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_proxy_property)。</span><span class="sxs-lookup"><span data-stu-id="6b443-186">[**WS\_PROXY\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_proxy_property).</span></span> | <span data-ttu-id="6b443-187">指定 proxy 屬性。</span><span class="sxs-lookup"><span data-stu-id="6b443-187">Specifies a proxy property.</span></span> |



 

 

 




