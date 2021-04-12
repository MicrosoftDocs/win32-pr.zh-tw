---
title: 建立用戶端
description: 服務模型 API 和 WsUtil.exe 工具的 WWSAPI，可大幅簡化為 Web 服務建立用戶端。
ms.assetid: 09f489e8-958d-4bc5-a232-aa59bd75333a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606a68f574a9ad79d15f3ddd48247f93a5414250
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372624"
---
# <a name="creating-a-client"></a>建立用戶端

[服務模型](service-model-layer-overview.md)API 和[WsUtil.exe](wsutil-compiler-tool.md)工具的 WWSAPI，可大幅簡化為 Web 服務建立用戶端。 服務模型提供的 API 可讓用戶端透過[通道](channel.md)傳送和接收[訊息](message.md)，作為 C 方法呼叫。 WsUtil 工具會產生用來執行用戶端的標頭和協助程式。 這些標頭包含代表目標 Web 服務所提供之服務的 C 函式類型和函式原型。 協助程式是用來建立服務 proxy，其中包含服務的系結資訊和 [端點位址](endpoint-address.md) 。

## <a name="using-wsutil-to-generate-headers-and-helpers"></a>使用 WsUtil 來產生標頭和協助程式

為了產生標頭和協助程式，WsUtil 會開啟並讀取目標服務（wsdl 和 xsd 檔案）的中繼資料檔案，並將它們轉換成標頭;因此，您必須事先取得目標服務的中繼資料檔案，例如，使用 SvcUtil Windows Communication Foundation 部分。 基於安全考慮，您必須將這些檔案的複本都值得信任。  (需詳細資訊，請參閱 [WsUtil 編譯器工具](wsutil-compiler-tool.md) 主題的「安全性」一節。 ) 

若要執行 WsUtil，如果服務的 WSDL 和 XSD 檔案位於自己的目錄中，請使用下列命令列語法： `WsUtil.exe *.wsdl *.xsd` 。 或者，您也可以使用完整名稱來指定檔案。

WsUtil 通常會為每個中繼資料檔案產生兩個檔案：標頭和 C 檔案。 將這些檔案新增至您的程式碼專案，並使用 \# include 語句將它們包含在您的用戶端的程式碼中。  (XSD 檔案代表型別，而 WSDL 檔案代表作業。 ) 

## <a name="creating-the-service-proxy"></a>建立服務 Proxy

WsUtil 所產生的標頭包含 helper 常式，可使用必要的系結來建立服務 proxy。 此常式包含在產生的標頭檔的 [原則協助程式常式] 區段中。 例如， [HTTPcalculatorclientexample](httpcalculatorclientexample.md) 範例中所示的計算機服務產生的標頭將包含下列函式原型。


```
HRESULT BasicHttpBinding_ICalculator_CreateServiceProxy(
    __in_opt WS_HTTP_BINDING_TEMPLATE* templateValue,
    __in_ecount_opt(proxyPropertyCount) const WS_PROXY_PROPERTY* proxyProperties,
    __in const ULONG proxyPropertyCount,
    __deref_out_opt WS_SERVICE_PROXY** _serviceProxy,
    __in_opt WS_ERROR* error);
```



將此協助程式併入您的程式碼，並傳遞 [WS \_ 服務 \_ proxy](ws-service-proxy.md) 控制碼，以接收已建立服務 proxy 的控制碼。 在最簡單的案例中，只會將服務 proxy 控制碼和錯誤物件傳遞給函式，因此呼叫看起來如下所示。


```C++
hr = BasicHttpBinding_ICalculator_CreateServiceProxy(
            NULL,
            NULL,
            0,
            &serviceProxy,
            error);
```



若要建立服務 proxy 的位址部分，請使用服務 proxy 的控制碼來呼叫 [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) ，並使用包含您想要連接之服務端點位址的 [**WS \_ 端點 \_ 位址**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) 指標。

## <a name="implementing-the-client-with-function-prototypes"></a>使用函式原型來執行用戶端

從服務 WSDL 檔案產生的標頭也包含 C 函式原型，代表可從 Web 服務取得的服務，以及所需的系結特定。 例如，針對 HttpCalculatorServiceExample 中所示的計算機服務所產生的標頭，將會包含該服務的乘法運算的下列原型。

``` syntax
HRESULT BasicHttpBinding_ICalculator_Multiply(
    __in WS_SERVICE_PROXY* _serviceProxy,
    __in double n1,
    __in double n2,
    __out double* MultiplyResult,
    __in WS_HEAP* _heap,
    __in_ecount_opt(_callPropertyCount) const WS_CALL_PROPERTY* _callProperties,
    __in const ULONG _callPropertyCount,
    __in_opt const WS_ASYNC_CONTEXT* _asyncContext,
    __in_opt WS_ERROR* _error);
```

您可以複製原型，並使用它們做為範本，在您的用戶端中撰寫函式呼叫的程式碼，每個案例都會將控制碼傳遞給服務 proxy。 當您完成服務 proxy 時，請呼叫 [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy)。

 

 




