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
# <a name="service-host"></a>服務主機

服務主機是在進程中裝載服務的執行時間環境。


服務可以設定服務主機內的一或多個端點。

![顯示服務主機之結構的圖表，其中包含服務端點。](images/servicehost.png)

## <a name="creating-a-service-host"></a>建立服務主機

在建立服務主機之前，服務必須定義其端點。 服務主機中的端點是在 [**WS \_ 服務 \_ 端點**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) 結構中指定，而且是由下列資訊所定義：

-   位址，也就是用來裝載服務的實體 URI。
-   [**WS \_ 通道 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)結構，指定端點的基礎通道型別。
-   指定通道系結的 [**WS \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) 系結結構。
-   [**WS \_ 安全性 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description)結構，其中包含端點的安全性描述。
-   [**WS \_ 服務 \_ 合約**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract)結構，表示端點的 [服務合約](contract.md)。
-   [**WS \_ 服務 \_ 安全性 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback)結構，指定端點的授權回呼函數。
-   [**WS \_ 服務 \_ 端點 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property)結構，其中包含服務端點屬性的陣列。

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

SOAP over UDP 只支援單向合約（由 **ws \_ \_ 通道** 系結列舉中的 [**ws \_ UDP \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)系結所表示）。

定義端點之後，可以將它傳遞至 [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) 函式，此函式會採用 [**WS \_ 服務 \_ 端點**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) 結構的指標陣列。

``` syntax
HRESULT hr = WsCreateServiceHost (serviceEndpoints, 1, NULL, 0, &host, error);
```

應用程式可以選擇性地提供 [**服務屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) 陣列給 [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) ，以設定服務主機上的自訂設定。

應用程式會開啟服務主機，以開始接受用戶端要求。

``` syntax
WsOpenServiceHost(serviceHost, NULL, NULL);
```

開啟服務主機之後，如果沒有其他需要的作業，應用程式可以將它關閉。 請注意，這不會釋出其資源，而且可以使用後續的 [**WsResetServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost)呼叫來重新開啟。

``` syntax
WsCloseServiceHost(serviceHost, NULL, NULL);
```

關閉服務主機之後，應用程式可能會重設服務主機以供重複使用。

``` syntax
WsResetServiceHost(serviceHost, NULL);
```

當應用程式使用服務主機完成時，它可以藉由呼叫 [**WsFreeServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost) 函式來釋放與服務主機相關聯的資源。 請注意，呼叫此函式之前，必須先呼叫 [**WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost) 。

``` syntax
WsFreeServiceHost(serviceHost, NULL);
```

如需將自訂狀態附加至服務主機的詳細資訊，請參閱 [使用者主機狀態](user-host-state.md)

如需有關指定端點的服務主機中授權的詳細資訊，請參閱 [服務授權](service-authorization.md)。

如需針對服務執行服務作業和服務合約的 iinformation，請參閱 [服務作業](server-side-service-operations.md) 和 [服務合約](contract.md)主題。

## <a name="security"></a>安全性

應用程式可以使用下列屬性來控制服務主機代表應用程式佈建的資源數量：

-   [**WS \_服務 \_ 端點 \_ 屬性 \_ 最大 \_ 接受 \_ 通道**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)，
-   [**WS \_服務 \_ 端點 \_ 屬性 \_ 最大 \_ 並行**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)，
-   [**WS \_服務 \_ 端點 \_ 屬性 \_ 最大 \_ 通道**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)，
-   [**WS \_服務 \_ 端點 \_ 屬性 \_ 主體 \_ 堆積 \_ \_ 大小上限**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)，
-   [**WS \_服務 \_ 端點 \_ 屬性的 \_ 最大 \_ 呼叫 \_ 集區 \_ 大小**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)，
-   [**WS \_服務 \_ 端點 \_ 屬性 \_ 最大 \_ 通道 \_ 集區 \_ 大小**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)。

系統會為每個屬性選擇安全的預設值; 如果應用程式想要修改這些屬性，則必須小心。 除了上述屬性之外，應用程式也可以修改 [通道](channel.md) [、接聽](listener.md) 程式和 [訊息](message.md) 特定屬性。 修改這些設定之前，請參閱這些元件的安全性考慮。

此外，使用 WWSAPI service host API 時，應謹慎評估下列應用程式設計考慮：

-   使用 MEX 時，應用程式應該小心不要洩漏任何敏感性資料。 作為緩和措施，如果透過 MEX 公開的資料本質是敏感的，應用程式可能會選擇使用安全系結來設定 MEX 端點，且該系結至少需要驗證，並且使用 [**WS \_ 服務 \_ 安全性 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback)將授權實作為端點的一部分。
-   依預設，在服務主機上，透過 [**WS \_ 服務 \_ 屬性 \_ 錯誤 \_ 洩漏**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) 屬性停用了豐富的錯誤資訊。 應用程式會自行決定是否要傳送豐富的錯誤資訊做為錯誤的一部分。 不過，這可能會導致資訊洩漏，因此建議只在進行偵錯工具時變更此設定。
-   除了針對基本設定檔2.0 和 XML 序列化所執行的驗證之外，服務主機不會針對服務作業參數所收到的資料內容執行驗證。 應用程式必須負責自行執行所有參數驗證。
-   授權不會作為服務主機的一部分來執行。 不過，應用程式可以使用 [**ws \_ 安全性 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) 和 [**ws \_ 服務 \_ 安全性 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback)來執行自己的授權配置。
-   應用程式必須負責在其端點上使用安全系結。 服務主機不會在端點上設定的任何安全性之外提供任何安全性。

下列 API 專案會搭配服務主機使用。

| 回呼                                                                             | Description                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**WS \_ 服務 \_ 接受 \_ 通道 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback) | 在服務主機的端點接聽程式接受通道時叫用。 |
| [**WS \_ 服務 \_ 關閉 \_ 通道 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)   | 在端點上關閉或中止通道時叫用。                     |



 



| 列舉型別                                                                    | 描述                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**WS \_ 服務 \_ 端點 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) | 用於設定 [**WS \_ 服務 \_ 端點**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)的選擇性參數。 |
| [**WS-MANAGEMENT \_ 服務 \_ 主機 \_ 狀態**](/windows/desktop/api/WebServices/ne-webservices-ws_service_host_state)                      | 服務主機可以處於的狀態。                                                   |
| [**WS \_ 服務 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id)                    | 用來設定服務主機的選擇性參數。                                       |



 



| 函式                                                     | 描述                                                                                  |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)             | 中斷並中止服務主機上的目前作業。                          |
| [**WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost)             | 關閉所有接聽程式，讓用戶端不會接受任何新的通道。                   |
| [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost)           | 建立服務主機。                                                                      |
| [**WsFreeServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost)               | 釋放與服務主機物件相關聯的記憶體。                                   |
| [**WsGetServiceHostProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetservicehostproperty) | 抓取指定的服務主機屬性。                                                 |
| [**WsOpenServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsopenservicehost)               | 開啟服務主機進行通訊，並在所有端點上啟動接聽程式。        |
| [**WsResetServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost)             | 重設服務主機以供重複使用，並重設基礎通道和接聽程式以供重複使用。 |



 



| Handle                                       | Description                                      |
|----------------------------------------------|--------------------------------------------------|
| [**WS \_ 服務 \_ 主機**](ws-service-host.md) | 用來參考服務主機的不透明類型。 |



 



| 結構                                                                              | Description                                                                     |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**WS \_ 服務 \_ 端點**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)                                   | 代表服務主機上的個別端點。                            |
| [**WS \_ 服務 \_ 端點 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property)                | 指定服務特定的設定。                                           |
| [**WS \_ 服務 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property)                                   | 指定服務特定的設定。                                           |
| [**WS \_ 服務 \_ 屬性 \_ 接受 \_ 回呼**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_accept_callback) | 指定成功接受通道時所呼叫的回呼。 |
| [**WS \_ 服務 \_ 屬性 \_ 關閉 \_ 回呼**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_close_callback)   | 指定當通道即將關閉時，所呼叫的回呼。    |



 

 

 




