---
title: 服務模型層總覽
description: WWSAPI 服務模型 API 會將用戶端與服務之間的通訊模型為方法呼叫，而不是資料訊息。
ms.assetid: a1ed1e3c-94ae-4383-9251-83caf2e3ebf3
keywords:
- 適用于 Windows 的服務模型層總覽 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c74861f0e2ed13b35e308d1314aec2a33dc28c31
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "104321423"
---
# <a name="service-model-layer-overview"></a><span data-ttu-id="a3a95-106">服務模型層總覽</span><span class="sxs-lookup"><span data-stu-id="a3a95-106">Service Model Layer Overview</span></span>

<span data-ttu-id="a3a95-107">WWSAPI 服務模型 API 會將用戶端與服務之間的通訊模型為方法呼叫，而不是資料訊息。</span><span class="sxs-lookup"><span data-stu-id="a3a95-107">The WWSAPI Service Model API models the communication between a client and a service as method calls, rather than as data messages.</span></span> <span data-ttu-id="a3a95-108">相較于在用戶端與服務之間支援更傳統[訊息](message.md)交換的[通道層](channel-layer-overview.md)，服務模型會透過用戶端上的服務 proxy 和服務上的服務主機，自動管理通訊。</span><span class="sxs-lookup"><span data-stu-id="a3a95-108">In contrast to the [channel layer](channel-layer-overview.md), which supports more traditional [message](message.md) exchanges between client and service, the Service Model automatically manages communication by means of a service proxy on the client and a service host on the service.</span></span> <span data-ttu-id="a3a95-109">這表示用戶端會呼叫產生的函式，而伺服器會執行回呼。</span><span class="sxs-lookup"><span data-stu-id="a3a95-109">This means that the client calls generated functions and the server implements callbacks.</span></span>


<span data-ttu-id="a3a95-110">例如，假設有一個計算機服務，其會在兩個數字上執行加法和減法。</span><span class="sxs-lookup"><span data-stu-id="a3a95-110">For example, consider a calculator service which performs addition and subtraction on two numbers.</span></span> <span data-ttu-id="a3a95-111">加法和減法是自然表示為方法呼叫的作業。</span><span class="sxs-lookup"><span data-stu-id="a3a95-111">Addition and subtraction are operations naturally represented as method calls.</span></span>

![顯示計算機服務如何使用方法呼叫來與用戶端通訊的圖表，以進行加法和減法。](images/servicemodelintro.png)

<span data-ttu-id="a3a95-113">服務模型表示用戶端與服務之間的通訊是宣告方法呼叫，因此會從應用程式中隱藏基礎通道層的通訊詳細資料，讓服務更容易執行。</span><span class="sxs-lookup"><span data-stu-id="a3a95-113">The service model represents the communication between client and the service as declared method calls, and so conceals the communication details of the underlying channel layer from the application, making the service easier to implement.</span></span>

## <a name="specifying-a-service"></a><span data-ttu-id="a3a95-114">指定服務</span><span class="sxs-lookup"><span data-stu-id="a3a95-114">Specifying a Service</span></span>

<span data-ttu-id="a3a95-115">您必須根據訊息交換模式以及其網路資料標記法來指定服務。</span><span class="sxs-lookup"><span data-stu-id="a3a95-115">A service must be specified in terms of its message exchange patterns as well as its network data representation.</span></span> <span data-ttu-id="a3a95-116">針對服務，此規格通常會以 WSDL 和 XML 架構檔的形式提供。</span><span class="sxs-lookup"><span data-stu-id="a3a95-116">For services, this specification is usually provided as WSDL and XML schema documents.</span></span>

<span data-ttu-id="a3a95-117">WSDL 檔案是一份 XML 檔，其中包含通道系結和服務的訊息交換模式，而 XML 架構檔則是一種 XML 檔，可定義個別訊息的資料標記法。</span><span class="sxs-lookup"><span data-stu-id="a3a95-117">The WSDL document is an XML document which contains the channel binding and the message exchange patterns of the service, whereas the XML schema document is an XML document that defines the data representation of the individual messages.</span></span>

<span data-ttu-id="a3a95-118">針對計算機服務及其加法和減法運算，WSDL 檔案看起來可能如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="a3a95-118">For the calculator service and its addition and subtraction operations, the WSDL document might look like the following example:</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" 
xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" 
xmlns:soapenc="http://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="http://schemas.xmlsoap.org/ws/2004/09/policy" 
xmlns:wsap="http://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" 
xmlns:soap12="http://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="http://www.w3.org/2005/08/addressing" 
xmlns:wsx="http://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ICalculator">
  <wsdl:operation name="Add">
   <wsdl:input wsaw:Action="http://Example.org/ICalculator/Add" 
   message="tns:ICalculator_Add_InputMessage" />
   <wsdl:output wsaw:Action="http://Example.org/ICalculator/AddResponse" 
   message="tns:ICalculator_Add_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
</wsdl:definitions>
```

<span data-ttu-id="a3a95-119">同樣地，其 XML 架構可以定義如下：</span><span class="sxs-lookup"><span data-stu-id="a3a95-119">Likewise, its XML schema can be defined as follows:</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="Add">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="a" type="xs:int" />
    <xs:element minOccurs="0" name="b" type="xs:int" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
 <xs:element name="AddResponse">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="result" type="xs:int" 
    />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
</xs:schema> 
```

## <a name="converting-metadata-to-code"></a><span data-ttu-id="a3a95-120">將中繼資料轉換為程式碼</span><span class="sxs-lookup"><span data-stu-id="a3a95-120">Converting Metadata to Code</span></span>

<span data-ttu-id="a3a95-121">服務模型提供 [WsUtil.exe](web-service-compiler-tool.md) 做為處理這些元資料檔案的工具，將 WSDL 檔案轉換成 C 標頭和原始程式檔。</span><span class="sxs-lookup"><span data-stu-id="a3a95-121">The service model provides the [WsUtil.exe](web-service-compiler-tool.md) as a tool to process these metadata documents, converting a WSDL file into a C header and source files.</span></span>

![此圖顯示 WsUtil.exe 如何將 WSDL 檔案轉換成 C 標頭和來源檔案。](images/doctotool.png)

<span data-ttu-id="a3a95-123">[WsUtil.exe](web-service-compiler-tool.md)會產生服務的標頭和來源，以及用戶端的用戶端服務作業。</span><span class="sxs-lookup"><span data-stu-id="a3a95-123">The [WsUtil.exe](web-service-compiler-tool.md) generates header and sources for service implementation as well as client-side service operations for the client .</span></span>

## <a name="calling-the-calculator-service-from-a-client"></a><span data-ttu-id="a3a95-124">從用戶端呼叫計算機服務</span><span class="sxs-lookup"><span data-stu-id="a3a95-124">Calling the Calculator Service From a Client</span></span>

<span data-ttu-id="a3a95-125">如同服務的執行，用戶端必須包含產生的標頭或標頭。</span><span class="sxs-lookup"><span data-stu-id="a3a95-125">As with the service implementation, the client must include the generated header or headers.</span></span>

``` syntax
#include "CalculatorProxyStub.h"
```

<span data-ttu-id="a3a95-126">現在，用戶端應用程式可以建立並開啟服務 proxy，以開始與計算機服務進行通訊。</span><span class="sxs-lookup"><span data-stu-id="a3a95-126">Now, The client application can create and open a service proxy to begin communication with the calculator service.</span></span>

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
WS_STRING uri= WS_STRING_VALUE(L"http://localhost/example");
address.uri = uri;

if (FAILED (hr = WsCreateServiceProxy(WS_CHANNEL_TYPE_REQUEST, WS_HTTP_CHANNEL_BINDING, NULL, NULL, 0, &serviceProxy, error)))
    goto Error;

if (FAILED (hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error)))
    goto Error;
```

<span data-ttu-id="a3a95-127">應用程式可以使用下列程式碼，在計算機服務上呼叫 Add 作業：</span><span class="sxs-lookup"><span data-stu-id="a3a95-127">The application can call the Add operation on the calculator service with the following code:</span></span>

``` syntax
if (FAILED (hr = DefaultBinding_ICalculator_Add(serviceProxy, heap, 1, 2, &result, NULL, 0, NULL, error)))
    goto Error;
```

<span data-ttu-id="a3a95-128">請參閱 [HttpCalculatorClientExample](httpcalculatorclientexample.md) 中的程式碼範例，以取得計算機服務的完整執行。</span><span class="sxs-lookup"><span data-stu-id="a3a95-128">Please refer to the code example at [HttpCalculatorClientExample](httpcalculatorclientexample.md) for full implementation of the calculator service.</span></span>

## <a name="service-model-components"></a><span data-ttu-id="a3a95-129">服務模型元件</span><span class="sxs-lookup"><span data-stu-id="a3a95-129">Service Model Components</span></span>

<span data-ttu-id="a3a95-130">在計算機範例中，個別 WWSAPI 服務模型元件的互動如下所示：</span><span class="sxs-lookup"><span data-stu-id="a3a95-130">The interaction of the individual WWSAPI Service Model components within the Calculator example is as follows:</span></span>

-   <span data-ttu-id="a3a95-131">用戶端會建立 [服務 proxy](service-proxy.md) 並加以開啟。</span><span class="sxs-lookup"><span data-stu-id="a3a95-131">The client creates a [service proxy](service-proxy.md) and opens it.</span></span>
-   <span data-ttu-id="a3a95-132">用戶端會呼叫服務的新增函式，並傳入服務 proxy。</span><span class="sxs-lookup"><span data-stu-id="a3a95-132">The client calls the Add function of the service, and passes in the service proxy.</span></span>
-   <span data-ttu-id="a3a95-133">訊息會根據中繼資料工具所產生的標頭和原始程式檔中的序列化中繼資料進行序列化， ([WsUtil.exe](web-service-compiler-tool.md)) 。</span><span class="sxs-lookup"><span data-stu-id="a3a95-133">The message is serialized according to the serialization metadata in the header and source files generated by the metadata tool ([WsUtil.exe](web-service-compiler-tool.md)).</span></span>
-   <span data-ttu-id="a3a95-134">訊息會寫入至通道，並透過網路傳送至服務。</span><span class="sxs-lookup"><span data-stu-id="a3a95-134">The message is written to the channel and is transmitted over the network to the service.</span></span>
-   <span data-ttu-id="a3a95-135">在伺服器端，此服務會裝載于服務主機內，並有接聽 ICalculator 合約的端點。</span><span class="sxs-lookup"><span data-stu-id="a3a95-135">On the server side, the service is hosted inside a service host, and has an endpoint listening for the ICalculator contract.</span></span>
-   <span data-ttu-id="a3a95-136">在存根中使用服務模型中繼資料時，服務會將來自用戶端的訊息還原序列化，並將其分派給存根。</span><span class="sxs-lookup"><span data-stu-id="a3a95-136">Using the Service Model metadata in the stub, the service deserializes the message from the client and dispatches it to the stub.</span></span>
-   <span data-ttu-id="a3a95-137">伺服器端服務會呼叫 Add 方法，並將作業內容傳遞給它。</span><span class="sxs-lookup"><span data-stu-id="a3a95-137">The server-side service calls the Add method, passing it the operation context.</span></span> <span data-ttu-id="a3a95-138">此操作內容包含內送訊息的參考。</span><span class="sxs-lookup"><span data-stu-id="a3a95-138">This operation context contains the reference to the incoming message.</span></span>

![顯示個別 WWSAPI 服務模型元件互動的圖表。](images/servicemodellayout.png)

<span data-ttu-id="a3a95-140">單元</span><span class="sxs-lookup"><span data-stu-id="a3a95-140">Components</span></span>

-   <span data-ttu-id="a3a95-141">[服務主機](service-host.md)：裝載服務。</span><span class="sxs-lookup"><span data-stu-id="a3a95-141">[Service host](service-host.md): Hosts a service.</span></span>
-   <span data-ttu-id="a3a95-142">[服務 proxy](service-proxy.md)：定義用戶端與服務通訊的方式。</span><span class="sxs-lookup"><span data-stu-id="a3a95-142">[Service proxy](service-proxy.md): Defines how a client communicates with a service.</span></span>
-   <span data-ttu-id="a3a95-143">[CoNtext](context.md)：讓特定狀態資訊可供服務作業使用的屬性包。</span><span class="sxs-lookup"><span data-stu-id="a3a95-143">[Context](context.md): Property bag for making state-specific information available to a service operation.</span></span>
-   <span data-ttu-id="a3a95-144">[合約](contract.md)：服務的介面定義。</span><span class="sxs-lookup"><span data-stu-id="a3a95-144">[Contract](contract.md): The interface definition of a service.</span></span> <span data-ttu-id="a3a95-145">例如，在我們的範例程式碼中，ICalculator 代表計算機服務的合約。</span><span class="sxs-lookup"><span data-stu-id="a3a95-145">For example, ICalculator represents a contract for the calculator service in our example code.</span></span>
-   <span data-ttu-id="a3a95-146">[WsUtil.exe](web-service-compiler-tool.md)：用來產生 proxy 和存根的服務模型中繼資料工具。</span><span class="sxs-lookup"><span data-stu-id="a3a95-146">[WsUtil.exe](web-service-compiler-tool.md): The Service Model metadata tool for generating proxies and stubs.</span></span>

 

 




