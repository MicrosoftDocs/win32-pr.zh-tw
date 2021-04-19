---
title: 服務主機
description: 服務主機是在進程中裝載服務的執行時間環境。
ms.assetid: 42e4d24d-5611-4561-b874-6dc3f3f88c73
keywords:
- 適用于 Windows 的服務主機 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0170f7dc0dfda99887b7d11d68d073517e0eb85f
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "106982136"
---
# <a name="service-host"></a><span data-ttu-id="b9ac9-106">服務主機</span><span class="sxs-lookup"><span data-stu-id="b9ac9-106">Service Host</span></span>

<span data-ttu-id="b9ac9-107">服務主機是在進程中裝載服務的執行時間環境。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-107">The service host is the runtime environment for hosting a service within a process.</span></span>


<span data-ttu-id="b9ac9-108">服務可以設定服務主機內的一或多個端點。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-108">A service can configure one or more endpoints inside a service host.</span></span>

![顯示服務主機之結構的圖表，其中包含服務端點。](images/servicehost.png)

## <a name="creating-a-service-host"></a><span data-ttu-id="b9ac9-110">建立服務主機</span><span class="sxs-lookup"><span data-stu-id="b9ac9-110">Creating a service host</span></span>

<span data-ttu-id="b9ac9-111">在建立服務主機之前，服務必須定義其端點。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-111">Before creating a service host, a service needs to define its endpoints.</span></span> <span data-ttu-id="b9ac9-112">服務主機中的端點是在 [**WS \_ 服務 \_ 端點**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) 結構中指定，而且是由下列資訊所定義：</span><span class="sxs-lookup"><span data-stu-id="b9ac9-112">An endpoint in service host is specified in the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) structure and it is defined by the following information:</span></span>

-   <span data-ttu-id="b9ac9-113">位址，也就是用來裝載服務的實體 URI。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-113">An address, which is the physical URI on which the service will be hosted.</span></span>
-   <span data-ttu-id="b9ac9-114">[**WS \_ 通道 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)結構，指定端點的基礎通道型別。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-114">A [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) structure that specifies the type of the underlying channel for the endpoint.</span></span>
-   <span data-ttu-id="b9ac9-115">指定通道系結的 [**WS \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) 系結結構。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-115">A [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) structure that specifies the binding of the channel.</span></span>
-   <span data-ttu-id="b9ac9-116">[**WS \_ 安全性 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description)結構，其中包含端點的安全性描述。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-116">A [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) structure that contains the security description for the endpoint.</span></span>
-   <span data-ttu-id="b9ac9-117">[**WS \_ 服務 \_ 合約**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract)結構，表示端點的 [服務合約](contract.md)。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-117">A [**WS\_SERVICE\_CONTRACT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) structure that represents the [service contract](contract.md) for the endpoint.</span></span>
-   <span data-ttu-id="b9ac9-118">[**WS \_ 服務 \_ 安全性 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback)結構，指定端點的授權回呼函數。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-118">A [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) structure that specifies an authorization callback function for the endpoint.</span></span>
-   <span data-ttu-id="b9ac9-119">[**WS \_ 服務 \_ 端點 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property)結構，其中包含服務端點屬性的陣列。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-119">A [**WS\_SERVICE\_ENDPOINT\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property) structure that contains an array of service endpoint properties.</span></span>

``` syntax
WS_SERVICE_ENDPOINT serviceEndpoint = {0};
const WS_SERVICE_ENDPOINT* serviceEndpoints[1];
serviceEndpoints[0] = &serviceEndpoint;
WS_STRING url = WS_STRING_VALUE(L"net.tcp://+/Example");

// Method based service contract for the service
static WS_SERVICE_CONTRACT calculatorContract = 
{
    &calculatorContractDescription, // comes from a generated header.
    NULL,
    &calculatorFunctions, // specified by the application
};

serviceEndpoint.address.url = &url;
serviceEndpoint.binding.channelBinding =  WS_TCP_CHANNEL_BINDING; 
serviceEndpoint.contract = &calculatorContract;  
serviceEndpoint.channelType = WS_CHANNEL_TYPE_DUPLEX_SESSION; 
serviceEndpoint.authorizationCallback = AuthorizationCallback; // Authorization callback.
```

<span data-ttu-id="b9ac9-120">SOAP over UDP 只支援單向合約（由 **ws \_ \_ 通道** 系結列舉中的 [**ws \_ UDP \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)系結所表示）。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-120">Only one-way contracts are supported for SOAP over UDP, represented by [**WS\_UDP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) in the **WS\_CHANNEL\_BINDING** enumeration.</span></span>

<span data-ttu-id="b9ac9-121">定義端點之後，可以將它傳遞至 [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) 函式，此函式會採用 [**WS \_ 服務 \_ 端點**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) 結構的指標陣列。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-121">After an endpoint is defined, it can be passed to the [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) function, which takes an array of pointers to [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) structures.</span></span>

``` syntax
HRESULT hr = WsCreateServiceHost (serviceEndpoints, 1, NULL, 0, &host, error);
```

<span data-ttu-id="b9ac9-122">應用程式可以選擇性地提供 [**服務屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) 陣列給 [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) ，以設定服務主機上的自訂設定。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-122">An application can optionally provide an array of [**service properties**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) to [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) to configure custom settings on the service host.</span></span>

<span data-ttu-id="b9ac9-123">應用程式會開啟服務主機，以開始接受用戶端要求。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-123">An application opens the service host to start accepting client requests.</span></span>

``` syntax
WsOpenServiceHost(serviceHost, NULL, NULL);
```

<span data-ttu-id="b9ac9-124">開啟服務主機之後，如果沒有其他需要的作業，應用程式可以將它關閉。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-124">After opening the service host, the application can close it if there are no more operations that require it.</span></span> <span data-ttu-id="b9ac9-125">請注意，這不會釋出其資源，而且可以使用後續的 [**WsResetServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost)呼叫來重新開啟。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-125">Note that this does not release its resources, and that it can be reopened with a subsequent call to [**WsResetServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost).</span></span>

``` syntax
WsCloseServiceHost(serviceHost, NULL, NULL);
```

<span data-ttu-id="b9ac9-126">關閉服務主機之後，應用程式可能會重設服務主機以供重複使用。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-126">After closing the service host, an application may reset the service host for reuse.</span></span>

``` syntax
WsResetServiceHost(serviceHost, NULL);
```

<span data-ttu-id="b9ac9-127">當應用程式使用服務主機完成時，它可以藉由呼叫 [**WsFreeServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost) 函式來釋放與服務主機相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-127">When the application is done with the service host it can free the resources associated with the service host by calling the [**WsFreeServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost) function.</span></span> <span data-ttu-id="b9ac9-128">請注意，呼叫此函式之前，必須先呼叫 [**WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost) 。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-128">Note that [**WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost) must be called before calling this function.</span></span>

``` syntax
WsFreeServiceHost(serviceHost, NULL);
```

<span data-ttu-id="b9ac9-129">如需將自訂狀態附加至服務主機的詳細資訊，請參閱 [使用者主機狀態](user-host-state.md)</span><span class="sxs-lookup"><span data-stu-id="b9ac9-129">For information on attaching a custom state to the service host, see [User Host State](user-host-state.md)</span></span>

<span data-ttu-id="b9ac9-130">如需有關指定端點的服務主機中授權的詳細資訊，請參閱 [服務授權](service-authorization.md)。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-130">For information on authorization in a service host for a given endpoint, see [Service Authorization](service-authorization.md).</span></span>

<span data-ttu-id="b9ac9-131">如需針對服務執行服務作業和服務合約的 iinformation，請參閱 [服務作業](server-side-service-operations.md) 和 [服務合約](contract.md)主題。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-131">For iinformation on implementing service operations and service contracts for a service, see the [service operations](server-side-service-operations.md) and [service contract](contract.md)topics.</span></span>

## <a name="security"></a><span data-ttu-id="b9ac9-132">安全性</span><span class="sxs-lookup"><span data-stu-id="b9ac9-132">Security</span></span>

<span data-ttu-id="b9ac9-133">應用程式可以使用下列屬性來控制服務主機代表應用程式佈建的資源數量：</span><span class="sxs-lookup"><span data-stu-id="b9ac9-133">An application can use the followin properties to control the amount of resources the service host allocates on behalf of the application:</span></span>

-   <span data-ttu-id="b9ac9-134">[**WS \_服務 \_ 端點 \_ 屬性 \_ 最大 \_ 接受 \_ 通道**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)，</span><span class="sxs-lookup"><span data-stu-id="b9ac9-134">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_ACCEPTING\_CHANNELS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="b9ac9-135">[**WS \_服務 \_ 端點 \_ 屬性 \_ 最大 \_ 並行**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)，</span><span class="sxs-lookup"><span data-stu-id="b9ac9-135">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CONCURRENCY**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="b9ac9-136">[**WS \_服務 \_ 端點 \_ 屬性 \_ 最大 \_ 通道**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)，</span><span class="sxs-lookup"><span data-stu-id="b9ac9-136">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CHANNELS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="b9ac9-137">[**WS \_服務 \_ 端點 \_ 屬性 \_ 主體 \_ 堆積 \_ \_ 大小上限**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)，</span><span class="sxs-lookup"><span data-stu-id="b9ac9-137">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_BODY\_HEAP\_MAX\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="b9ac9-138">[**WS \_服務 \_ 端點 \_ 屬性的 \_ 最大 \_ 呼叫 \_ 集區 \_ 大小**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)，</span><span class="sxs-lookup"><span data-stu-id="b9ac9-138">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CALL\_POOL\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="b9ac9-139">[**WS \_服務 \_ 端點 \_ 屬性 \_ 最大 \_ 通道 \_ 集區 \_ 大小**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-139">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CHANNEL\_POOL\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id).</span></span>

<span data-ttu-id="b9ac9-140">系統會為每個屬性選擇安全的預設值; 如果應用程式想要修改這些屬性，則必須小心。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-140">Secure defaults are chosen for each of these properties, an application must be careful if it wishes to modify these properties.</span></span> <span data-ttu-id="b9ac9-141">除了上述屬性之外，應用程式也可以修改 [通道](channel.md) [、接聽](listener.md) 程式和 [訊息](message.md) 特定屬性。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-141">Beyond the above-mentioned properties, [channel](channel.md), [listener](listener.md) and [message](message.md) specific properties can also be modified by the application.</span></span> <span data-ttu-id="b9ac9-142">修改這些設定之前，請參閱這些元件的安全性考慮。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-142">Refer to the security considerations of these components before modifying any of these settings.</span></span>

<span data-ttu-id="b9ac9-143">此外，使用 WWSAPI service host API 時，應謹慎評估下列應用程式設計考慮：</span><span class="sxs-lookup"><span data-stu-id="b9ac9-143">In addition, the following application design considerations should be carefully evaluated when using WWSAPI service host API:</span></span>

-   <span data-ttu-id="b9ac9-144">使用 MEX 時，應用程式應該小心不要洩漏任何敏感性資料。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-144">When using MEX, applications should be careful not to disclose any sensitive data.</span></span> <span data-ttu-id="b9ac9-145">作為緩和措施，如果透過 MEX 公開的資料本質是敏感的，應用程式可能會選擇使用安全系結來設定 MEX 端點，且該系結至少需要驗證，並且使用 [**WS \_ 服務 \_ 安全性 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback)將授權實作為端點的一部分。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-145">As a mitigation, if the nature of the data being exposed through MEX is sensitive, applications may choose to configure the MEX endpoint with a secure binding requiring authentication at the very least and implement authorization as part of the endpoint using the [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).</span></span>
-   <span data-ttu-id="b9ac9-146">依預設，在服務主機上，透過 [**WS \_ 服務 \_ 屬性 \_ 錯誤 \_ 洩漏**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) 屬性停用了豐富的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-146">By default rich error information through faults is disabled on service host by [**WS\_SERVICE\_PROPERTY\_FAULT\_DISCLOSURE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) property.</span></span> <span data-ttu-id="b9ac9-147">應用程式會自行決定是否要傳送豐富的錯誤資訊做為錯誤的一部分。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-147">It is upon the discretion of the application to send rich error information as part of the fault.</span></span> <span data-ttu-id="b9ac9-148">不過，這可能會導致資訊洩漏，因此建議只在進行偵錯工具時變更此設定。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-148">However, this can result in information disclosure and thus it is recommended that this setting is only changed for debugging scenarios.</span></span>
-   <span data-ttu-id="b9ac9-149">除了針對基本設定檔2.0 和 XML 序列化所執行的驗證之外，服務主機不會針對服務作業參數所收到的資料內容執行驗證。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-149">Beyond validation performed for Basic Profile 2.0 and XML serialization, service host performs no validation on the data content received as part of service operation parameters.</span></span> <span data-ttu-id="b9ac9-150">應用程式必須負責自行執行所有參數驗證。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-150">It is the responsibility of the application to perform all parameter validations on its own.</span></span>
-   <span data-ttu-id="b9ac9-151">授權不會作為服務主機的一部分來執行。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-151">Authorization is not implemented as part of service host.</span></span> <span data-ttu-id="b9ac9-152">不過，應用程式可以使用 [**ws \_ 安全性 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) 和 [**ws \_ 服務 \_ 安全性 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback)來執行自己的授權配置。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-152">However, applications can implement their own authorization scheme using [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) and the [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).</span></span>
-   <span data-ttu-id="b9ac9-153">應用程式必須負責在其端點上使用安全系結。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-153">It is the responsibility of the application to use secure bindings on its endpoint.</span></span> <span data-ttu-id="b9ac9-154">服務主機不會在端點上設定的任何安全性之外提供任何安全性。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-154">Service host does not provide any security beyond what is configured on the endpoint.</span></span>

<span data-ttu-id="b9ac9-155">下列 API 專案會搭配服務主機使用。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-155">The following API elements are used with the service host.</span></span>

| <span data-ttu-id="b9ac9-156">回呼</span><span class="sxs-lookup"><span data-stu-id="b9ac9-156">Callback</span></span>                                                                             | <span data-ttu-id="b9ac9-157">Description</span><span class="sxs-lookup"><span data-stu-id="b9ac9-157">Description</span></span>                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="b9ac9-158">**WS \_ 服務 \_ 接受 \_ 通道 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="b9ac9-158">**WS\_SERVICE\_ACCEPT\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback) | <span data-ttu-id="b9ac9-159">在服務主機的端點接聽程式接受通道時叫用。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-159">Invoked when a channel is accepted on an endpoint listener by the service host.</span></span> |
| [<span data-ttu-id="b9ac9-160">**WS \_ 服務 \_ 關閉 \_ 通道 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="b9ac9-160">**WS\_SERVICE\_CLOSE\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)   | <span data-ttu-id="b9ac9-161">在端點上關閉或中止通道時叫用。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-161">Invoked when a channel is closed or aborted on an endpoint.</span></span>                     |



 



| <span data-ttu-id="b9ac9-162">列舉型別</span><span class="sxs-lookup"><span data-stu-id="b9ac9-162">Enumeration</span></span>                                                                    | <span data-ttu-id="b9ac9-163">描述</span><span class="sxs-lookup"><span data-stu-id="b9ac9-163">Description</span></span>                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9ac9-164">**WS \_ 服務 \_ 端點 \_ 屬性 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="b9ac9-164">**WS\_SERVICE\_ENDPOINT\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) | <span data-ttu-id="b9ac9-165">用於設定 [**WS \_ 服務 \_ 端點**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)的選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-165">Optional parameters for configuring a [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span> |
| [<span data-ttu-id="b9ac9-166">**WS-MANAGEMENT \_ 服務 \_ 主機 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="b9ac9-166">**WS\_SERVICE\_HOST\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_host_state)                      | <span data-ttu-id="b9ac9-167">服務主機可以處於的狀態。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-167">The states that a service host can be in.</span></span>                                                   |
| [<span data-ttu-id="b9ac9-168">**WS \_ 服務 \_ 屬性 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="b9ac9-168">**WS\_SERVICE\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id)                    | <span data-ttu-id="b9ac9-169">用來設定服務主機的選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-169">Optional parameters for configuring the service host.</span></span>                                       |



 



| <span data-ttu-id="b9ac9-170">函式</span><span class="sxs-lookup"><span data-stu-id="b9ac9-170">Function</span></span>                                                     | <span data-ttu-id="b9ac9-171">描述</span><span class="sxs-lookup"><span data-stu-id="b9ac9-171">Description</span></span>                                                                                  |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9ac9-172">**WsAbortServiceHost**</span><span class="sxs-lookup"><span data-stu-id="b9ac9-172">**WsAbortServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)             | <span data-ttu-id="b9ac9-173">中斷並中止服務主機上的目前作業。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-173">Interrupts and discontinues current operations on the service host.</span></span>                          |
| [<span data-ttu-id="b9ac9-174">**WsCloseServiceHost**</span><span class="sxs-lookup"><span data-stu-id="b9ac9-174">**WsCloseServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost)             | <span data-ttu-id="b9ac9-175">關閉所有接聽程式，讓用戶端不會接受任何新的通道。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-175">Closes all listeners so that no new channels are accepted from the client.</span></span>                   |
| [<span data-ttu-id="b9ac9-176">**WsCreateServiceHost**</span><span class="sxs-lookup"><span data-stu-id="b9ac9-176">**WsCreateServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost)           | <span data-ttu-id="b9ac9-177">建立服務主機。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-177">Creates a service host.</span></span>                                                                      |
| [<span data-ttu-id="b9ac9-178">**WsFreeServiceHost**</span><span class="sxs-lookup"><span data-stu-id="b9ac9-178">**WsFreeServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost)               | <span data-ttu-id="b9ac9-179">釋放與服務主機物件相關聯的記憶體。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-179">Releases the memory associated with a service host object.</span></span>                                   |
| [<span data-ttu-id="b9ac9-180">**WsGetServiceHostProperty**</span><span class="sxs-lookup"><span data-stu-id="b9ac9-180">**WsGetServiceHostProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetservicehostproperty) | <span data-ttu-id="b9ac9-181">抓取指定的服務主機屬性。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-181">Retrieves a specified Service Host property.</span></span>                                                 |
| [<span data-ttu-id="b9ac9-182">**WsOpenServiceHost**</span><span class="sxs-lookup"><span data-stu-id="b9ac9-182">**WsOpenServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsopenservicehost)               | <span data-ttu-id="b9ac9-183">開啟服務主機進行通訊，並在所有端點上啟動接聽程式。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-183">Opens a service host for communication and starts the listeners on all the endpoints.</span></span>        |
| [<span data-ttu-id="b9ac9-184">**WsResetServiceHost**</span><span class="sxs-lookup"><span data-stu-id="b9ac9-184">**WsResetServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost)             | <span data-ttu-id="b9ac9-185">重設服務主機以供重複使用，並重設基礎通道和接聽程式以供重複使用。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-185">Resets the service host for reuse and resets the underlying channel and listeners for reuse.</span></span> |



 



| <span data-ttu-id="b9ac9-186">Handle</span><span class="sxs-lookup"><span data-stu-id="b9ac9-186">Handle</span></span>                                       | <span data-ttu-id="b9ac9-187">Description</span><span class="sxs-lookup"><span data-stu-id="b9ac9-187">Description</span></span>                                      |
|----------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="b9ac9-188">**WS \_ 服務 \_ 主機**</span><span class="sxs-lookup"><span data-stu-id="b9ac9-188">**WS\_SERVICE\_HOST**</span></span>](ws-service-host.md) | <span data-ttu-id="b9ac9-189">用來參考服務主機的不透明類型。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-189">An opaque type used to reference a service host.</span></span> |



 



| <span data-ttu-id="b9ac9-190">結構</span><span class="sxs-lookup"><span data-stu-id="b9ac9-190">Structure</span></span>                                                                              | <span data-ttu-id="b9ac9-191">Description</span><span class="sxs-lookup"><span data-stu-id="b9ac9-191">Description</span></span>                                                                     |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="b9ac9-192">**WS \_ 服務 \_ 端點**</span><span class="sxs-lookup"><span data-stu-id="b9ac9-192">**WS\_SERVICE\_ENDPOINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)                                   | <span data-ttu-id="b9ac9-193">代表服務主機上的個別端點。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-193">Represents an individual endpoint on a service host.</span></span>                            |
| [<span data-ttu-id="b9ac9-194">**WS \_ 服務 \_ 端點 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="b9ac9-194">**WS\_SERVICE\_ENDPOINT\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property)                | <span data-ttu-id="b9ac9-195">指定服務特定的設定。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-195">Specifies a service-specific setting.</span></span>                                           |
| [<span data-ttu-id="b9ac9-196">**WS \_ 服務 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="b9ac9-196">**WS\_SERVICE\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_property)                                   | <span data-ttu-id="b9ac9-197">指定服務特定的設定。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-197">Specifies a service-specific setting.</span></span>                                           |
| [<span data-ttu-id="b9ac9-198">**WS \_ 服務 \_ 屬性 \_ 接受 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="b9ac9-198">**WS\_SERVICE\_PROPERTY\_ACCEPT\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_accept_callback) | <span data-ttu-id="b9ac9-199">指定成功接受通道時所呼叫的回呼。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-199">Specifies the callback which is called when a channel is successfully accepted.</span></span> |
| [<span data-ttu-id="b9ac9-200">**WS \_ 服務 \_ 屬性 \_ 關閉 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="b9ac9-200">**WS\_SERVICE\_PROPERTY\_CLOSE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_close_callback)   | <span data-ttu-id="b9ac9-201">指定當通道即將關閉時，所呼叫的回呼。</span><span class="sxs-lookup"><span data-stu-id="b9ac9-201">Specifies the callback which is called when a channel is about to be closed.</span></span>    |



 

 

 




