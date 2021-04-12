---
title: 服務中繼資料
description: WWSAPI 服務主機支援其端點的 WS-MetadataExchange。
ms.assetid: 5a6feb34-7fff-4000-b3be-63112b22905a
keywords:
- 服務中繼資料原生-Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebf15614ac9e89a4e08fdd19102492d0121e65d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104463948"
---
# <a name="service-metadata"></a>服務中繼資料

WWSAPI 服務主機支援其端點的 WS-MetadataExchange。 您可以使用下列步驟，在服務主機上啟用這類中繼資料交換：

-   在 [ws 服務 \_ \_ 主機](ws-service-host.md)的 [**ws \_ 服務 \_ 中繼資料**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata)屬性中指定元資料檔案。
-   在 [ws 服務 \_ \_ 主機](ws-service-host.md)的 [**ws \_ 服務 \_ 中繼資料**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata)屬性中指定服務名稱。
-   使用 [**ws \_ 服務 \_ 端點**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)上的 [**ws \_ 服務 \_ 端點 \_ 屬性 \_ 中繼資料**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)屬性來指定個別端點的埠。
-   啟用一或多個 [**WS \_ 服務 \_ 端點**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) 結構來服務 WS-MetadataExchange 要求。
-   （選擇性）在 [**ws \_ 服務 \_ 端點 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)列舉中指定 **ws \_ 服務 \_ 端點 \_ 屬性 \_ 中繼資料 \_ 交換 \_ URL \_ 尾碼**，以提供特定位址的服務 Ws-MetadataExchange 要求。


在服務主機上指定元資料檔案/服務名稱

第一個步驟是在服務主機上指定元資料檔案。 做法是將個別檔收集為 WS \_ XML \_ 字串 \* 的陣列。 這些字串可以是 XML 架構、WSDL 或 WS-Policy 檔。 這是透過 [**WS \_ 服務 \_ 屬性 \_ 中繼資料**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) 屬性所指定。

或者，應用程式也可以將服務名稱和命名空間指定為 [**WS \_ 服務 \_ 中繼資料**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata)的一部分。 如果元資料檔案未指定指定服務名稱的服務專案，服務模型會使用服務的對應 WSDL 埠來產生服務元素。

``` syntax
WS_SERVICE_METADATA_DOCUMENT document = {0};
WS_STRING documentName = WS_STRING_VALUE(L&quot;a.wsdl&quot;);
document.name = &documentName;
document.content = &wsdlDocument
WS_SERVICE_METADATA_DOCUMENT** metadataDocuments [] = {&document};
WS_SERVICE_METADATA serviceMetadata = {0};
// Specify Metadata documents
serviceMetadata.count = WsCountOf(metadataDocuments);
serviceMetadata.documents = &metadataDocuments;
// Specify service name
serviceMetadata.serviceName = &serviceName;
serviceMetadata.serviceNs = &serviceNamespace;


WS_SERVICE_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_PROPERTY_METADATA;
serviceProperties[0].value =  &serviceMetadata;
serviceProperties[0].ValueSize = sizeof(serviceMetadata);
```

請注意，不會對檔執行個別元資料檔案的驗證。 應用程式必須負責驗證檔的內容，並確保所有的匯入路徑都是相對指定的。

指定的命名空間是用來尋找服務主機將在其中新增服務專案的檔。

將服務元素新增至 WSDL 檔案

服務主機會為應用程式提供應用程式的功能，以代表尚未指定的服務元素。 為了啟用此行為，應用程式必須在 [**WS \_ 服務 \_ 中繼資料**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) 結構上指定 serivceName 和 serviceNs 欄位。 如果 serviceName 和 serviceNs 都是 **Null** ，則不會將任何服務專案新增至 WSDL 檔案。 這兩種方式都用來識別要加入 serviceElement 的檔。

如果未指定 [**WS \_ SERVICE \_ PROPERTY \_ METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) 屬性，就不會在服務主機上進行中繼資料 exhange。

指定 WS \_ 服務端點上的埠 \_

若要讓 [**WS \_ 服務 \_ 端點**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) 可作為 WSDL 檔案中 SERVICE 元素內的埠，應用程式必須在其上指定 [**ws \_ service \_ endpoint \_ property \_ METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) 屬性。

``` syntax
WS_SERVICE_ENDPOINT_METADATA endpointPort = {0}
endpointPort.name = &portName;
endpointPort.bindingName = &bindingName;
endpointPort.bindingNs = &bindingNs;

WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA;
serviceProperties[0].value =  &endpointPort;
serviceProperties[0].valueSize = sizeof(endpointPort);
```

假設系結名稱和命名空間的參考存在於服務主機上指定的檔中，做為 WS \_ 服務 \_ 屬性 \_ 中繼資料的一部分。 執行時間不會代表應用程式進行驗證。

在 WS \_ 服務端點上啟用 WS-MetadataExchange 服務 \_

為了服務 WS-MetadataExchange 要求，服務主機必須至少有一個端點啟用服務 WS-MetadataExchange 要求。 這是藉由為 [**WS \_ 服務 \_ 端點**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)上的 WS-MetadataExchange 設定適當的版本來完成。

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_MEX;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

在 WS \_ 服務端點上啟用 HTTP GET 服務 \_

為了 serviceHTTP GET 要求，服務主機必須至少有一個端點啟用服務 WS-MetadataExchange 要求。 這是藉由為 [**WS \_ 服務 \_ 端點**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)上的 WS-MetadataExchange 設定適當的版本來完成。

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_HTTP_GET;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

指定 Ws-MetadataExchange 要求的 URL 尾碼

應用程式可以選擇性地只允許在特定路徑上接受 WS-MetadataExchange 的要求。 這是藉由為指定的 WS 服務端點指定尾碼來完成 \_ \_ 。 此後綴會依原樣串連至 WS 服務端點的實際 URL \_ \_ 。 串連的字串會用來作為所收到的 ' to ' 標頭的相符 URL。

``` syntax
const WS_STRING suffix = WS_STRING_VALUE(L&quot;mex&quot;);
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_URL_SUFFIX;
serviceProperties[0].value =  &suffix;
serviceProperties[0].valueSize = sizeof(suffix);
```

下列 API 元素與服務中繼資料相關。

| 列舉型別                                                       | 描述                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**WS \_ 中繼資料 \_ 交換 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_exchange_type) | 啟用或停用端點上的 WS-MetadataExchange 和 HTTP GET 服務。 |



 



| 結構                                                               | Description                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**WS \_ 服務 \_ 端點 \_ 中繼資料**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_metadata) | 表示端點的通訊埠元素。                         |
| [**WS \_ 服務 \_ 中繼資料**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata)                    | 指定服務元資料檔案陣列。                       |
| [**WS \_ 服務 \_ 中繼資料 \_ 檔**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata_document) | 指定組成服務中繼資料的個別檔。 |



 

 

 




