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
# <a name="service-proxy"></a>服務 Proxy

服務 proxy 是服務的用戶端 proxy。 服務 proxy 可讓應用程式透過[通道](channel.md)傳送和接收[訊息](message.md)，做為方法呼叫。

服務 proxy 會視需要建立、開啟、用來呼叫服務，並在不再需要時關閉。 或者，應用程式可以重複使用服務 proxy 來重複連接至相同的服務，而不需支付 initialising 服務 proxy 所需的時間和資源。 下圖說明服務 proxy 可能狀態的流程，以及從某個狀態到另一個狀態的函式呼叫或事件的流程。

![顯示服務 proxy 狀態的圖表，以及從某個狀態到另一個狀態的函式呼叫或事件。](images/serviceproxystates.png)

這些服務 proxy 狀態是以 [**WS \_ 服務 \_ proxy \_ 狀態**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) 列舉來列舉。

如先前的圖表和下列程式碼所示，服務 proxy 是透過呼叫 [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) 函式來建立。 作為此呼叫的參數，WWSAPI 提供下列列舉：

-   [**WS \_ 通道 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)
-   [**WS \_ 通道系結 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)

它也接受使用下列資料類型的選擇性參數：

-   [**WS \_ PROXY \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)
-   [**WS \_ 安全性 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description)

建立服務 proxy 時， **WsCreateServiceProxy** 函式會透過 out 參數，傳回服務 proxy [Ws-management （WS \_ 服務 \_](ws-service-proxy.md)proxy）的參考。

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

建立服務 proxy 之後，應用程式可以藉由呼叫 [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) 函式來開啟服務 proxy 來與服務通訊，並傳遞包含要連接之服務端點網路位址的 [**位址**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) 結構。

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
address.uri.chars = "net.tcp://localhost/example";
address.uri.length = wcslen("net.tcp://localhost/example";);
hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error);
```

開啟服務 proxy 之後，應用程式就可以使用它來對服務進行呼叫。

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

當應用程式不再需要服務 proxy 時，它會藉由呼叫 [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) 函數來關閉服務 proxy。 它也會藉由呼叫 [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy)來釋出相關聯的記憶體。

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

## <a name="reusing-the-service-proxy"></a>重複使用服務 Proxy

或者，在呼叫 [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) 之後，應用程式可以藉由呼叫 [**WsResetServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy) 函數來重複使用服務 proxy。

``` syntax
hr = WsResetServiceProxy(
    serviceProxy, 
    error);
```

如需有關如何在不同的環境中使用服務 proxy 的詳細資訊，請參閱下列主題：

-   [服務 Proxy 和會話](service-proxy-and-sessions.md)
-   [服務作業](service-operation.md)
-   [用戶端服務作業](client-side-service-operations.md)
-   [HttpCalculatorClientExample](httpcalculatorclientexample.md)

### <a name="security"></a>安全性

當您使用 WWSAPI 服務 proxy API 時，應謹慎注意下列應用程式設計考慮：

-   服務 proxy 將不會對基本設定檔2.0 驗證和 XML 序列化以外的資料執行任何驗證。 應用程式必須負責驗證它在呼叫過程中收到的參數所包含的資料。
-   使用 [**ws \_ proxy \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) 列舉值 **ws \_ proxy \_ 屬性 \_ 最大 \_ 暫 \_** 止的呼叫，在服務 proxy 上設定暫止呼叫的最大數目，針對執行緩慢的伺服器提供保護。 預設的最大值為100。 應用程式必須謹慎修改預設值。
-   除了用來與伺服器通訊的 [**WS \_ 安全性 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) 結構中指定的以外，服務 proxy 不提供任何安全性保證。
-   當您修改服務 proxy 上的 [訊息](message.md) 和 [通道](channel.md) 預設值時，請務必小心。 在修改任何相關屬性之前，請先閱讀與訊息和通道相關聯的安全性考慮。
-   服務 proxy 會加密其保留在記憶體中的所有認證。

下列 API 元素與服務 proxy 相關。

| 回呼                                                          | Description                                                                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**WS \_ PROXY \_ 訊息 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback) | 當輸入訊息的標頭即將透過傳送，或只接收輸出訊息標頭時叫用。 |



 



| 列舉型別                                                 | 描述                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**WS \_ 呼叫 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id)       | 列舉選擇性參數，以設定用戶端服務作業的呼叫。 |
| [**WS \_ PROXY \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)     | 列舉用來設定服務 proxy 的選擇性參數。                         |
| [**WS \_ 服務 \_ PROXY \_ 狀態**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) | 服務 proxy 的狀態。                                                           |



 



| 函式                                                       | 描述                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)                         | 放棄指定服務 proxy 上的指定呼叫。                           |
| [**WsAbortServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy)             | 取消指定的服務 proxy 上所有暫止的輸入和輸出。                |
| [**WsCall**](/windows/desktop/api/WebServices/nf-webservices-wscall)                                       | 僅供內部使用。 將引數序列化為訊息，並透過通道傳送。 |
| [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy)             | 關閉服務 proxy 以進行通訊。                                         |
| [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)           | 建立服務 proxy。                                                          |
| [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy)               | 釋放與服務 proxy 相關聯的記憶體。                              |
| [**WsGetServiceProxyProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetserviceproxyproperty) | 抓取指定的服務 proxy 屬性。                                     |
| [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy)               | 開啟服務端點的服務 proxy。                                      |
| [**WsResetServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy)             | 重設服務 proxy。                                                             |



 



| Handle                                     | Description                                       |
|--------------------------------------------|---------------------------------------------------|
| [WS \_ 服務 \_ PROXY](ws-service-proxy.md) | 用來參考服務 proxy 的不透明類型。 |



 



| 結構                                         | Description                 |
|---------------------------------------------------|-----------------------------|
| [**WS \_ CALL \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property)    | 指定呼叫屬性。  |
| [**WS \_PROXY \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_proxy_property)。 | 指定 proxy 屬性。 |



 

 

 




