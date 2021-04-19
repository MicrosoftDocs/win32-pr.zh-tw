---
title: Windows Web 服務範例
description: 下列範例示範如何使用 Windows Web 服務 API。
ms.assetid: 8a557ef0-a88a-4257-a181-57f2dca9022f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e74aec03c4822fb9ba270076b5127dd37d145fb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966786"
---
# <a name="windows-web-services-examples"></a>Windows Web 服務範例

下列範例示範如何使用 Windows Web 服務 API。

-   [服務模型範例](service-model-examples.md)
-   [TCP 通道層範例](tcp-channel-layer-examples.md)
-   [HTTP 通道層範例](http-channel-layer-examples.md)
-   [UDP 通道層範例](udp-channel-layer-examples.md)
-   [具名管道通道層範例](named-pipes-channel-layer-examples.md)
-   [訊息範例](message-examples.md)
-   [XML 範例](xml-examples.md)
-   [非同步模型範例](async-model-examples.md)
-   [安全性通道層範例](security-channel-layer-examples.md)
-   [檔案複寫範例](file-replication-examples.md)

## <a name="service-model-examples"></a>服務模型範例

計算機服務：用戶端： [HttpCalculatorClientExample](httpcalculatorclientexample.md)，伺服器： [HttpCalculatorServiceExample](httpcalculatorserviceexample.md)。

具有 SSL 傳輸安全性的計算機服務：用戶端： [HttpCalculatorWithSslClientExample](httpcalculatorwithsslclientexample.md)、伺服器： [HttpCalculatorWithSslServiceExample](httpcalculatorwithsslserviceexample.md)。

具有使用者名稱（SSL 混合模式安全性）的計算機服務：用戶端： [HttpCalculatorWithUsernameOverSslClientExample](httpcalculatorwithusernameoversslclientexample.md)，伺服器： [HttpCalculatorWithUserNameOverSslServiceExample](httpcalculatorwithusernameoversslserviceexample.md)。

具有 Kerberos over SSL 混合模式安全性的計算機服務：用戶端： [HttpCalculatorWithKerberosOverSslClientExample](httpcalculatorwithkerberosoversslclientexample.md)、伺服器： [HttpCalculatorWithKerberosOverSslServiceExample](httpcalculatorwithkerberosoversslserviceexample.md)。

採購單服務：用戶端： [HttpPurchaseOrderClientExample](httppurchaseorderclientexample.md)，伺服器： [HttpPurchaseOrderServiceExample](httppurchaseorderserviceexample.md)。

具有 SSL 傳輸安全性的採購訂單服務：用戶端： [HttpPurchaseOrderWithSslClientExample](httppurchaseorderwithsslclientexample.md)、伺服器： [HttpPurchaseOrderWithSslServiceExample](httppurchaseorderwithsslserviceexample.md)。

具有透過 SSL 混合模式安全性之使用者名稱的訂單服務：用戶端： [HttpPurchaseOrderWithUsernameOverSslClientExample](httppurchaseorderwithusernameoversslclientexample.md)、伺服器： [HttpPurchaseOrderWithUserNameOverSslServiceExample](httppurchaseorderwithusernameoversslserviceexample.md)。

具有 Kerberos over SSL 混合模式安全性的訂單服務：用戶端： [HttpPurchaseOrderWithKerberosOverSslClientExample](httppurchaseorderwithkerberosoversslclientexample.md)、伺服器： [HttpPurchaseOrderWithKerberosOverSslServiceExample](httppurchaseorderwithkerberosoversslserviceexample.md)。

不具類型的訂單服務：伺服器： [UnTypedServiceExample](untypedserviceexample.md)。 用戶端： [UnTypedClientExample](untypedclientexample.md)

會話計算機： Server： [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md)。 用戶端：[SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md)。

使用自訂通道和接聽程式執行的計算機：伺服器：[HttpCalculatorWithLayeredChannelServiceExample](httpcalculatorwithlayeredchannelserviceexample.md)。 用戶端：[HttpCalculatorWithLayeredChannelClientExample](httpcalculatorwithlayeredchannelclientexample.md)。

使用編碼通道的計算機：伺服器：[HttpCalculatorWithEncodedChannelServiceExample](httpcalculatorwithencodedchannelserviceexample.md)。 用戶端：[HttpCalculatorWithEncodedChannelClientExample](httpcalculatorwithencodedchannelclientexample.md)。

處理原始 (非 SOAP) HTTP 要求的服務：用戶端：[HttpRawClientExample](httprawclientexample.md)。 伺服器：[HttpRawServiceExample](httprawserviceexample.md)。

服務操作中止通知：伺服器： [BlockingServiceExample](blockingserviceexample.md)。 用戶端：[ServiceCancellationExample](servicecancellationexample.md)。

呼叫取消：伺服器： [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md)。 用戶端：[CallAbandonExample](callabandonexample.md)。

手動建立原則描述，並用它來建立服務 proxy： [PolicyTemplateExample](policytemplateexample.md)。

## <a name="tcp-channel-layer-examples"></a>TCP 通道層範例

使用單向模式傳送訊息的 TCP 範例：用戶端： [OneWayTcpClientExample](onewaytcpclientexample.md)、伺服器： [OneWayTcpServerExample](onewaytcpserverexample.md)

使用要求-回復模式傳送訊息的 TCP 範例：用戶端： [RequestReplyTcpClientExample](requestreplytcpclientexample.md)，伺服器： [RequestReplyTcpServerExample](requestreplytcpserverexample.md)

串流 TCP 範例：用戶端： [StreamingTcpClientExample](streamingtcpclientexample.md)，伺服器： [StreamingTcpServerExample](streamingtcpserverexample.md)

非同步資料流程 TCP 範例： Client： [AsyncStreamingTcpClientExample](asyncstreamingtcpclientexample.md)，Server： [AsyncStreamingTcpServerExample](asyncstreamingtcpserverexample.md)

## <a name="http-channel-layer-examples"></a>HTTP 通道層範例

HTTP 範例： Client： [HttpClientExample](httpclientexample.md)，Server： [HttpServerExample](httpserverexample.md)

使用串流 Api 的 HTTP 範例： Client： [StreamingHttpClientExample](streaminghttpclientexample.md)，Server： [StreamingHttpServerExample](streaminghttpserverexample.md)

## <a name="udp-channel-layer-examples"></a>UDP 通道層範例

使用單向模式傳送訊息的 UDP 範例：用戶端： [OneWayUdpClientExample](onewayudpclientexample.md)、伺服器： [OneWayUdpServerExample](onewayudpserverexample.md)

使用多播要求回應模式傳送訊息的 UDP 範例：用戶端： [MulticastUdpClientExample](multicastudpclientexample.md)、伺服器： [MulticastUdpServerExample](multicastudpserverexample.md) 以下是相同的範例，但使用 IPv6 位址： Client： [MulticastUdpClientExample6](multicastudpclientexample6.md)，Server： [MulticastUdpServerExample6](multicastudpserverexample6.md)

## <a name="named-pipes-channel-layer-examples"></a>具名管道通道層範例

使用要求-回復模式傳送訊息的具名管道範例：用戶端： [RequestReplyNamedPipesClientExample](requestreplynamedpipesclientexample.md)，伺服器： [RequestReplyNamedPipesServerExample](requestreplynamedpipesserverexample.md)

串流具名管道範例： Client： [StreamingNamedPipesClientExample](streamingnamedpipesclientexample.md)，Server： [StreamingNamedPipesServerExample](streamingnamedpipesserverexample.md)

## <a name="message-examples"></a>訊息範例

使用自訂訊息標頭的範例： [CustomHeaderExample](customheaderexample.md)

編碼和解碼訊息的範例： [MessageEncodingExample](messageencodingexample.md)

轉送訊息的範例： [ForwardMessageExample](forwardmessageexample.md)

## <a name="xml-examples"></a>XML 範例

使用 XML 緩衝區來寫入和讀取 xml 的範例 [ReadWriteXmlExample](readwritexmlexample.md)

使用 MTOM、WsWriteBytes、WsPushBytes 和 WsPullBytes 寫入和讀取二進位資料的範例 [ReadWriteBytesXmlExample](readwritebytesxmlexample.md)

流覽 XML 緩衝區的範例 [NavigateXmlExample](navigatexmlexample.md)

依節點[ReadXmlExample](readxmlexample.md)讀取 XML 檔節點的範例

尋找並顯示 XML 屬性的範例 [ReadAttributeExample](readattributeexample.md)

寫入和讀取元素陣列的範例 [ReadWriteArrayExample](readwritearrayexample.md)

將元素插入至 XML 緩衝區的範例 [InsertElementExample](insertelementexample.md)

示範如何使用某些 XML 緩衝區 helper 函數的範例 [XmlBufferExample](xmlbufferexample.md)

使用 wsutil 產生的 helper 函式來寫入和讀取衍生類型的範例 [DerivedTypeExample](derivedtypeexample.md)

## <a name="async-model-examples"></a>非同步模型範例

說明非同步函式之模型的範例。 [AsyncModelExample](asyncmodelexample.md)

## <a name="security-channel-layer-examples"></a>安全性通道層範例

透過 TCP 的 Windows 傳輸安全性：用戶端： [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md)，伺服器： [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md)。

具名管道上的 Windows 傳輸安全性：用戶端： [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md)，伺服器： [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md)。

SSL 傳輸安全性：用戶端： [HttpClientWithSslExample](httpclientwithsslexample.md)，伺服器： [HttpServerWithSslExample](httpserverwithsslexample.md)。

透過 SSL 混合模式安全性的使用者名稱：用戶端： [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md)，伺服器： [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md)。

透過 SSL 混合模式安全性的使用者名稱：用戶端： [HttpClientWithKerberosOverSslExample](httpclientwithkerberosoversslexample.md)，伺服器： [HttpServerWithKerberosOverSslExample](httpserverwithkerberosoversslexample.md)。

## <a name="metadata-example"></a>中繼資料範例

下列範例顯示如何處理 WSDL 和原則檔，其目標是將端點所支援的通訊協定相關資訊解壓縮。

透過 SSL 混合模式安全性的使用者名稱： [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md)。 透過 SSL 混合模式安全性發出的權杖： [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md)。 透過 SSL 混合模式安全性的 X509 憑證： [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md)。

## <a name="ws-metadata-exchange-example"></a>WS-Metadata Exchange 範例

下列範例示範如何在 [WS \_ 服務 \_ 主機](ws-service-host.md)上啟用 WS-MetadataExchange。

啟用 WS-MetadataExchange 的 TCP 服務： [MetadataExchangeSample](metadataexchangesample.md)。 WCF 服務的標記用戶端，其會呼叫已啟用 WS-MetadataExchange 的 TCP 服務： [ServiceMonikerSample](servicemonikersample.md)。

## <a name="custom-headers-and-service-model"></a>自訂標頭和服務模型

下列範例示範如何將自訂標頭分別搭配 [ws \_ 服務 \_ PROXY](ws-service-proxy.md) 和 [ws \_ 服務 \_ 主機](ws-service-host.md) 使用。

Client： [HttpCustomHeaderPurchaseOrderClientExample](httpcustomheaderpurchaseorderclientexample.md)，Server： [HttpCustomHeaderPurchaseOrderServiceExample](httpcustomheaderpurchaseorderserviceexample.md)。

## <a name="file-replication-sample"></a>檔案複寫範例

示範如何執行檔案複寫服務的完整範例：工具： [FileRepToolExample](filereptoolexample.md)、服務： [FileRepServiceExample](filerepserviceexample.md)。

## <a name="wcf-public-service-interoperation"></a>WCF 公用服務交互操作

Windows Web 服務用戶端與 WCF 服務用戶端通訊： [WcfPublicServiceSample](wcfpublicservicesample.md)。

## <a name="custom-http-proxy"></a>自訂 HTTP Proxy

Windows Web 服務用戶端與使用自訂 proxy 用戶端的 .ASMX TerraService 服務通訊： [AsmxTerraServiceSampleWithCustomProxy](asmxterraservicesamplewithcustomproxy.md)

 

 




