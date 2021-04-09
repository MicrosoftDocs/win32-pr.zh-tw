---
title: 建立服務
description: 服務模型 API 和 WsUtil.exe 工具在 WWSAPI 中大幅簡化了建立 Web 服務。
ms.assetid: 3536d1c6-6179-4f69-9cc8-27fe6ae30826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4700324a84962047f403ca7ad090adc3e9f4e99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840780"
---
# <a name="creating-a-service"></a><span data-ttu-id="9ca9d-103">建立服務</span><span class="sxs-lookup"><span data-stu-id="9ca9d-103">Creating a Service</span></span>

<span data-ttu-id="9ca9d-104">[服務模型](service-model-layer-overview.md)API 和[WsUtil.exe](wsutil-compiler-tool.md)工具在 WWSAPI 中大幅簡化了建立 Web 服務。</span><span class="sxs-lookup"><span data-stu-id="9ca9d-104">Creating a Web service is greatly simplified in WWSAPI by the [Service Model](service-model-layer-overview.md) API and the [WsUtil.exe](wsutil-compiler-tool.md) tool.</span></span> <span data-ttu-id="9ca9d-105">服務模型提供的 API 可讓服務和用戶端透過[通道](channel.md)傳送和接收[訊息](message.md)，作為 C 方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="9ca9d-105">The Service Model provides an API that enables the service and client to send and receive [messages](message.md) over a [channel](channel.md) as C method calls.</span></span> <span data-ttu-id="9ca9d-106">WsUtil 工具會產生用來執行服務的存根和標頭。</span><span class="sxs-lookup"><span data-stu-id="9ca9d-106">The WsUtil tool generates stubs and headers for implementing the service.</span></span>

## <a name="implementing-a-calculator-service-using-wwsapi"></a><span data-ttu-id="9ca9d-107">使用 WWSAPI 來執行計算機服務</span><span class="sxs-lookup"><span data-stu-id="9ca9d-107">Implementing a Calculator Service using WWSAPI</span></span>

<span data-ttu-id="9ca9d-108">使用 [Wsutil.exe](wsutil-compiler-tool.md) 工具產生的來源，執行下列步驟來執行此服務。</span><span class="sxs-lookup"><span data-stu-id="9ca9d-108">Using the generated sources from the [Wsutil.exe](wsutil-compiler-tool.md) tool, implement the service by the following steps.</span></span>

<span data-ttu-id="9ca9d-109">將標頭包含在應用程式來源中。</span><span class="sxs-lookup"><span data-stu-id="9ca9d-109">Include the headers in your application source.</span></span>

``` syntax
#include "CalculatorProxyStub.h"
```

<span data-ttu-id="9ca9d-110">執行服務作業。</span><span class="sxs-lookup"><span data-stu-id="9ca9d-110">Implement the service operations.</span></span> <span data-ttu-id="9ca9d-111">在此範例中，服務作業是計算機服務的「新增」和「減去」函數。</span><span class="sxs-lookup"><span data-stu-id="9ca9d-111">In this example, the service operations are the Add and Subtract functions of the calculator service.</span></span>

``` syntax
HRESULT CALLBACK Add (const WS_OPERATION_CONTEXT* context, 
                  int a, int b, int* result, 
                  const WS_ASYNC_CONTEXT* asyncContext, 
                  WS_ERROR* error)
{
    *result = a + b;
    printf ("%d + %d = %d\n", a, b, *result);
    return NOERROR;
}

HRESULT CALLBACK Subtract (const WS_OPERATION_CONTEXT* context, 
                  int a, int b, int* result, 
                  const WS_ASYNC_CONTEXT* asyncContext, 
                  WS_ERROR* error)
{
    *result = a - b;
    printf ("%d - %d = %d\n", a, b, *result);
    return NOERROR;
}
```

<span data-ttu-id="9ca9d-112">藉由設定 [**WS \_ 服務 \_ 合約**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) 結構的欄位來定義服務合約。</span><span class="sxs-lookup"><span data-stu-id="9ca9d-112">Define the service contract by setting the fields of a [**WS\_SERVICE\_CONTRACT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) structure.</span></span>

``` syntax
static const DefaultBinding_ICalculatorFunctionTable calculatorFunctions = {Add, Subtract};
static const WS_SERVICE_CONTRACT calculatorContract = 
{
    &DefaultBinding_ICalculatorContractDesc, // comes from the generated header.
    NULL, // for not specifying the default contract
    &calculatorFunctions // specified by the user
};
```

<span data-ttu-id="9ca9d-113">現在，請建立服務主機，並將它開啟以進行通訊。</span><span class="sxs-lookup"><span data-stu-id="9ca9d-113">Now, create a service host and open it for communication.</span></span>

``` syntax
WS_SERVICE_ENDPOINT serviceEndpoint = {0};
serviceEndpoint.uri.chars = L"https://+:80/example"; // address given as uri
serviceEndpoint.binding.channelBinding =  WS_HTTP_CHANNEL_BINDING; // channel binding for the endpoint
serviceEndpoint.channelType = WS_CHANNEL_TYPE_REPLY; // the channel type
serviceEndpoint.uri.length = (ULONG)wcslen(serviceEndpoint.uri.chars);
serviceEndpoint.contract = (WS_SERVICE_CONTRACT*)&calculatorContract;  // the contract
serviceEndpoint.properties = serviceProperties;
serviceEndpoint.propertyCount = WsCountOf(serviceProperties);

if (FAILED (hr = WsCreateServiceHost (&serviceEndpoint, 1, NULL, 0, &host, error)))
    goto Error;

// WsOpenServiceHost  to start the listeners in the service host 
if (FAILED (hr = WsOpenServiceHost (host, NULL, error)))
    goto Error;
```

<span data-ttu-id="9ca9d-114">請參閱 [HttpCalculatorServiceExample](httpcalculatorserviceexample.md) 的程式碼範例，以取得計算機服務的完整執行。</span><span class="sxs-lookup"><span data-stu-id="9ca9d-114">Please refer to the code example at [HttpCalculatorServiceExample](httpcalculatorserviceexample.md) for a full implementation of the calculator service.</span></span>

 

 




