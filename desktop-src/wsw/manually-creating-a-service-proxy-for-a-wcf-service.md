---
title: 手動建立 WCF 服務的服務 Proxy
description: 針對 Windows Communication Foundation (WCF) 服務建立用戶端服務 proxy 的最簡單方式，就是在服務模型層與 WsUtil 工具（如建立用戶端主題所述）。
ms.assetid: ef545090-382b-44bd-b7ab-f5a285b6e202
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e061fda95298986ee6336dee0662d80c89a0a5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965381"
---
# <a name="manually-creating-a-service-proxy-for-a-wcf-service"></a><span data-ttu-id="bbf08-103">手動建立 WCF 服務的服務 Proxy</span><span class="sxs-lookup"><span data-stu-id="bbf08-103">Manually Creating a Service Proxy for a WCF Service</span></span>

<span data-ttu-id="bbf08-104">針對 Windows Communication Foundation (WCF) 服務建立用戶端服務 proxy 的最簡單方式，就是在 [服務模型](service-model-layer-overview.md) 層與 WsUtil 工具（如 [建立用戶端](creating-a-client.md) 主題所述）。</span><span class="sxs-lookup"><span data-stu-id="bbf08-104">The easiest way to create a client service proxy for a Windows Communication Foundation (WCF) service is at the [Service Model](service-model-layer-overview.md) layer with the WsUtil tool, as described in the [Creating a Client](creating-a-client.md) topic.</span></span> <span data-ttu-id="bbf08-105">不過，如有必要，您也可以手動建立服務 proxy。</span><span class="sxs-lookup"><span data-stu-id="bbf08-105">However, if necessary, you can also create a service proxy manually.</span></span> <span data-ttu-id="bbf08-106">此 API 包含用於建立服務 proxy 以及結構、列舉等的 [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) 函式，以設定與 WCF 交互操作所需的屬性。</span><span class="sxs-lookup"><span data-stu-id="bbf08-106">This API includes a [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) function for creating the service proxy as well as structures, enumerations, and so on for setting the properties necessary to interoperate with WCF.</span></span>

<span data-ttu-id="bbf08-107">WCF 提供數個標準系結，每個都以特定使用案例為目標。</span><span class="sxs-lookup"><span data-stu-id="bbf08-107">WCF provides a number of standard bindings, each targeting a specific usage scenario.</span></span> <span data-ttu-id="bbf08-108">這會將您嘗試連接的服務系結至，進而決定您需要自訂哪些通道屬性，以便服務 proxy 與服務通訊。</span><span class="sxs-lookup"><span data-stu-id="bbf08-108">Which binding the service you are trying to connect to uses, in turn, determines which channel properties you need to customize for your service proxy to communicate with the service.</span></span>

## <a name="creating-a-service-proxy-for-wcfs-wshttpbinding"></a><span data-ttu-id="bbf08-109">建立 WCF WSHttpBinding 的服務 Proxy</span><span class="sxs-lookup"><span data-stu-id="bbf08-109">Creating a Service Proxy for WCF's WSHttpBinding</span></span>

<span data-ttu-id="bbf08-110">WSHttpBinding 適用于主線網際網路 web 服務案例。</span><span class="sxs-lookup"><span data-stu-id="bbf08-110">WSHttpBinding is for the mainline Internet web services scenario.</span></span> <span data-ttu-id="bbf08-111">它會使用較新的 SOAP 1.2 版和 WS-Addressing 版的1.0，並透過公用 HTTP 和 HTTPS 傳輸來啟用各式各樣的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="bbf08-111">It uses the newer SOAP version 1.2 and WS-Addressing version 1.0 and enables a wide range of security settings over the public HTTP and HTTPS transports.</span></span> <span data-ttu-id="bbf08-112">WWSAPI 對於 WSHttpBinding (或任何 WCF 標準系結都沒有同等的) ，但由於其預設 SOAP 版本、WS-Addressing 版本和編碼格式符合 WSHttpBinding 中的值，因此為使用 WSHttpBinding 的服務建立服務 proxy 很簡單。</span><span class="sxs-lookup"><span data-stu-id="bbf08-112">WWSAPI does not have an equivalent of the WSHttpBinding (or any of the WCF standard bindings, for that matter), but since its default SOAP version, WS-Addressing version, and encoding format match those in WSHttpBinding, creating a service proxy for a service that uses the WSHttpBinding is straightforward.</span></span> <span data-ttu-id="bbf08-113">例如，若要建立服務 proxy 來與沒有安全性的 WSHttpBinding 端點進行通訊，您可以直接使用類似下列程式碼片段 (變數宣告的程式碼，並) 省略建立堆積和錯誤。</span><span class="sxs-lookup"><span data-stu-id="bbf08-113">For example, to create a service proxy to talk to a WSHttpBinding endpoint without security, you can simply use code like following snippet (variable declaration, and heap and error creation are omitted).</span></span> <span data-ttu-id="bbf08-114">請注意， [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) 函式的呼叫中並未指定任何通道屬性或安全性描述。</span><span class="sxs-lookup"><span data-stu-id="bbf08-114">Notice that no channel properties or security description is specified in the call to the [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) function.</span></span>


```C++
// Create the proxy

hr = WsCreateServiceProxy(
        WS_CHANNEL_TYPE_REQUEST, 
        WS_HTTP_CHANNEL_BINDING, 
        NULL, // security description
        NULL, // proxy properties
        0, // proxy property count
        NULL, // channel properties
        0, // channel property count
        &proxy, 
        error);
```



<span data-ttu-id="bbf08-115">此函式會建立服務 proxy，並在) 上述函式呼叫的 *serviceProxy* 參數中，將其指標傳回給它 (&proxy。</span><span class="sxs-lookup"><span data-stu-id="bbf08-115">The function creates the service proxy and returns a pointer to it in the *serviceProxy* parameter (&proxy in the function call above).</span></span>

## <a name="creating-a-service-proxy-for-wcfs-basichttpbinding"></a><span data-ttu-id="bbf08-116">建立 WCF BasicHttpBinding 的服務 Proxy</span><span class="sxs-lookup"><span data-stu-id="bbf08-116">Creating a Service Proxy for WCF's BasicHttpBinding</span></span>

<span data-ttu-id="bbf08-117">但是，當您針對使用 BasicHttpBinding 系結的 WCF 服務手動建立服務 proxy 時，必須設定該通道的 SOAP 版本和 WS-Addressing 屬性。</span><span class="sxs-lookup"><span data-stu-id="bbf08-117">When you manually create a service proxy for a WCF service that uses a BasicHttpBinding binding, however, it is necessary to set the SOAP version and WS-Addressing properties of the channel.</span></span> <span data-ttu-id="bbf08-118">這是因為 WWSAPI 預設為 SOAP 1.2 版和 WS-Addressing 1.0。</span><span class="sxs-lookup"><span data-stu-id="bbf08-118">This is because WWSAPI defaults to SOAP version 1.2 and WS-Addressing 1.0.</span></span> <span data-ttu-id="bbf08-119">另一方面，WCF 的 BasicHttpBinding 會使用 SOAP 版本1.1，而不是 WS-ADDRESSING。</span><span class="sxs-lookup"><span data-stu-id="bbf08-119">WCF's BasicHttpBinding, on the other hand, uses SOAP version 1.1 and no WS-Addressing.</span></span>

<span data-ttu-id="bbf08-120">若要設定通道的 SOAP 版本和 WS-Addrssing 屬性，請宣告 [**WS \_ 通道 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) 結構的陣列來保存通道屬性和相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bbf08-120">To set the SOAP version and WS-Addrssing properties of the channel, declare an array of [**WS\_CHANNEL\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) structures to hold the channel properties and related information.</span></span>


```
WS_CHANNEL_PROPERTY channelProperties[4]; // Array to hold up to 4 channel properties

ULONG channelPropertyCount = 0; // Count of properties set
 
WS_ENVELOPE_VERSION soapVersion = WS_ENVELOPE_VERSION_SOAP_1_1; // Set required SOAP version
channelProperties[channelPropertyCount].id = WS_CHANNEL_PROPERTY_ENVELOPE_VERSION; // Type of first channel property
channelProperties[channelPropertyCount].value = &soapVersion; // Address of the SOAP version value
channelProperties[channelPropertyCount].valueSize = sizeof(soapVersion); // Size of the value
channelPropertyCount++; // Increment property count
 
WS_ADDRESSING_VERSION addressingVersion = WS_ADDRESSING_VERSION_TRANSPORT; // Set required WS-Addressing value
channelProperties[channelPropertyCount].id = WS_CHANNEL_PROPERTY_ADDRESSING_VERSION; // Type of second channel property
channelProperties[channelPropertyCount].value = &addressingVersion ; // Address of the WS-Addressing value
channelProperties[channelPropertyCount].valueSize = sizeof(addressingVersion ); // Size of the value
channelPropertyCount++; // Increment property count
 
// add more channel properties here

```



<span data-ttu-id="bbf08-121">然後，將通道屬性的陣列 (channelProperties) 和 (channelPropertyCount) 的屬性計數傳遞至 [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (或 [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) （如果您是在通道層) 工作）。</span><span class="sxs-lookup"><span data-stu-id="bbf08-121">Then pass the array of channel properties (channelProperties) and the count of properties (channelPropertyCount) to the [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (or [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) if you are working at channel layer).</span></span>


```
// Create the proxy

hr = WsCreateServiceProxy(
        WS_CHANNEL_TYPE_REQUEST, 
        WS_HTTP_CHANNEL_BINDING, 
        NULL, // security description
        NULL, // proxy properties
        0, // proxy property count
        channelProperties, // channel properties
        channelPropertyCount, // channel property count
        &proxy, 
        error);
```



<span data-ttu-id="bbf08-122">您宣告用來保存屬性的陣列會複製在 **WsCreateServiceProxy** 中，因此，您可以在呼叫函式之後，立即釋放屬性陣列的記憶體。</span><span class="sxs-lookup"><span data-stu-id="bbf08-122">The array you declared to hold the properties is copied in **WsCreateServiceProxy**, and as a result, you can free the memory for the property array immediately after calling the function.</span></span> <span data-ttu-id="bbf08-123">此外，如果您從堆疊配置記憶體 (如) 上述的程式碼片段，您也可以在呼叫後立即從函式傳回。</span><span class="sxs-lookup"><span data-stu-id="bbf08-123">Also, if you allocate the memory from the stack (like the code snippet above), you can also return from the function immediately after the call.</span></span>

## <a name="other-bindings"></a><span data-ttu-id="bbf08-124">其他系結</span><span class="sxs-lookup"><span data-stu-id="bbf08-124">Other Bindings</span></span>

<span data-ttu-id="bbf08-125">此外，WWSAPI 提供了使用其他系結（例如 NetTcpBinding 和 WSFederationHttpBinding）來建立服務 proxy 以與 WCF 服務進行通訊的機制。</span><span class="sxs-lookup"><span data-stu-id="bbf08-125">In addition, WWSAPI provides mechanisms for creating service proxies to communicate with WCF services using other bindings, such as NetTcpBinding and WSFederationHttpBinding.</span></span> <span data-ttu-id="bbf08-126">其中許多系結都需要設定其他通道屬性，例如安全描述項。</span><span class="sxs-lookup"><span data-stu-id="bbf08-126">Many of these binding require setting additional channel properties, such as security descriptors.</span></span> <span data-ttu-id="bbf08-127">如需說明如何使用其他系結的範例，請參閱 [Windows Web 服務範例](windows-web-services-examples.md)，特別是 [TCP 通道層範例](tcp-channel-layer-examples.md)、 [HTTP 通道層範例](http-channel-layer-examples.md)和 [安全性通道層範例](security-channel-layer-examples.md) 小節。</span><span class="sxs-lookup"><span data-stu-id="bbf08-127">For examples that illustrate using other bindings, see the [Windows Web Services Examples](windows-web-services-examples.md), section, in particular the [TCP Channel Layer Examples](tcp-channel-layer-examples.md), [HTTP Channel Layer Examples](http-channel-layer-examples.md), and [Security Channel Layer Examples](security-channel-layer-examples.md) subsections.</span></span>

 

 




