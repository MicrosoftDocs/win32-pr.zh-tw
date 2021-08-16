---
title: 建立服務
description: 服務模型 API 和 WsUtil.exe 工具在 WWSAPI 中大幅簡化了建立 Web 服務。
ms.assetid: 3536d1c6-6179-4f69-9cc8-27fe6ae30826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f6daadbfcd1d06f76bf5bef97559214e36015d3f72ff440e77f4293a47ea57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805738"
---
# <a name="creating-a-service"></a>建立服務

[服務模型](service-model-layer-overview.md)API 和[WsUtil.exe](wsutil-compiler-tool.md)工具在 WWSAPI 中大幅簡化了建立 Web 服務。 服務模型提供的 API 可讓服務和用戶端透過[通道](channel.md)傳送和接收[訊息](message.md)，作為 C 方法呼叫。 WsUtil 工具會產生用來執行服務的存根和標頭。

## <a name="implementing-a-calculator-service-using-wwsapi"></a>使用 WWSAPI 來執行計算機服務

使用 [Wsutil.exe](wsutil-compiler-tool.md) 工具產生的來源，執行下列步驟來執行此服務。

將標頭包含在應用程式來源中。

``` syntax
#include "CalculatorProxyStub.h"
```

執行服務作業。 在此範例中，服務作業是計算機服務的「新增」和「減去」函數。

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

藉由設定 [**WS \_ 服務 \_ 合約**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) 結構的欄位來定義服務合約。

``` syntax
static const DefaultBinding_ICalculatorFunctionTable calculatorFunctions = {Add, Subtract};
static const WS_SERVICE_CONTRACT calculatorContract = 
{
    &DefaultBinding_ICalculatorContractDesc, // comes from the generated header.
    NULL, // for not specifying the default contract
    &calculatorFunctions // specified by the user
};
```

現在，請建立服務主機，並將它開啟以進行通訊。

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

請參閱 [HttpCalculatorServiceExample](httpcalculatorserviceexample.md) 的程式碼範例，以取得計算機服務的完整執行。

 

 




