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
# <a name="manually-creating-a-service-proxy-for-a-wcf-service"></a>手動建立 WCF 服務的服務 Proxy

針對 Windows Communication Foundation (WCF) 服務建立用戶端服務 proxy 的最簡單方式，就是在 [服務模型](service-model-layer-overview.md) 層與 WsUtil 工具（如 [建立用戶端](creating-a-client.md) 主題所述）。 不過，如有必要，您也可以手動建立服務 proxy。 此 API 包含用於建立服務 proxy 以及結構、列舉等的 [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) 函式，以設定與 WCF 交互操作所需的屬性。

WCF 提供數個標準系結，每個都以特定使用案例為目標。 這會將您嘗試連接的服務系結至，進而決定您需要自訂哪些通道屬性，以便服務 proxy 與服務通訊。

## <a name="creating-a-service-proxy-for-wcfs-wshttpbinding"></a>建立 WCF WSHttpBinding 的服務 Proxy

WSHttpBinding 適用于主線網際網路 web 服務案例。 它會使用較新的 SOAP 1.2 版和 WS-Addressing 版的1.0，並透過公用 HTTP 和 HTTPS 傳輸來啟用各式各樣的安全性設定。 WWSAPI 對於 WSHttpBinding (或任何 WCF 標準系結都沒有同等的) ，但由於其預設 SOAP 版本、WS-Addressing 版本和編碼格式符合 WSHttpBinding 中的值，因此為使用 WSHttpBinding 的服務建立服務 proxy 很簡單。 例如，若要建立服務 proxy 來與沒有安全性的 WSHttpBinding 端點進行通訊，您可以直接使用類似下列程式碼片段 (變數宣告的程式碼，並) 省略建立堆積和錯誤。 請注意， [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) 函式的呼叫中並未指定任何通道屬性或安全性描述。


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



此函式會建立服務 proxy，並在) 上述函式呼叫的 *serviceProxy* 參數中，將其指標傳回給它 (&proxy。

## <a name="creating-a-service-proxy-for-wcfs-basichttpbinding"></a>建立 WCF BasicHttpBinding 的服務 Proxy

但是，當您針對使用 BasicHttpBinding 系結的 WCF 服務手動建立服務 proxy 時，必須設定該通道的 SOAP 版本和 WS-Addressing 屬性。 這是因為 WWSAPI 預設為 SOAP 1.2 版和 WS-Addressing 1.0。 另一方面，WCF 的 BasicHttpBinding 會使用 SOAP 版本1.1，而不是 WS-ADDRESSING。

若要設定通道的 SOAP 版本和 WS-Addrssing 屬性，請宣告 [**WS \_ 通道 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) 結構的陣列來保存通道屬性和相關資訊。


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



然後，將通道屬性的陣列 (channelProperties) 和 (channelPropertyCount) 的屬性計數傳遞至 [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (或 [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) （如果您是在通道層) 工作）。


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



您宣告用來保存屬性的陣列會複製在 **WsCreateServiceProxy** 中，因此，您可以在呼叫函式之後，立即釋放屬性陣列的記憶體。 此外，如果您從堆疊配置記憶體 (如) 上述的程式碼片段，您也可以在呼叫後立即從函式傳回。

## <a name="other-bindings"></a>其他系結

此外，WWSAPI 提供了使用其他系結（例如 NetTcpBinding 和 WSFederationHttpBinding）來建立服務 proxy 以與 WCF 服務進行通訊的機制。 其中許多系結都需要設定其他通道屬性，例如安全描述項。 如需說明如何使用其他系結的範例，請參閱 [Windows Web 服務範例](windows-web-services-examples.md)，特別是 [TCP 通道層範例](tcp-channel-layer-examples.md)、 [HTTP 通道層範例](http-channel-layer-examples.md)和 [安全性通道層範例](security-channel-layer-examples.md) 小節。

 

 




