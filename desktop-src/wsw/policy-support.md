---
title: 原則支援
description: Wsutil 會處理在輸入中繼資料中指定的原則，並產生服務模型支援的 helper 常式。
ms.assetid: 9c4fb485-2392-4117-b4a7-7a51786d60b9
keywords:
- Windows 的原則支援 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 347265d4081216a227b5040fc73f272181bdccfe09ca7500b81078a6a57ed7bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838638"
---
# <a name="policy-support"></a>原則支援

Wsutil 會處理在輸入中繼資料中指定的原則，並產生服務模型支援的 helper 常式。

## <a name="how-to-use-policy-support-in-wsutil"></a>如何在 wsutil 中使用原則支援

開發人員應該遵循下列步驟來使用 wsutil 編譯器中的原則支援：

-   收集目標 web 服務所需的所有輸入中繼資料檔案。
-   使用 wsutil.exe 編譯所有收集的 WSDL/XSD/原則檔案。 Wsutil 會為每個輸入 WSDL 和 XSD 檔案產生一組存根檔和標頭檔。
-   檢查產生的標頭檔，所有原則協助程式常式名稱都會列在標頭檔開頭的 [批註] 區段中。
-   使用 bindingName \_ CreateServiceProxy helper 常式來建立服務 proxy。
-   使用 bindingName \_ CreateServiceEndpoint helper 常式來建立服務端點。
-   填入方法簽章中指定的 WS bindingTemplateType 系結 \_ \_ \_ 範本結構。 開發人員可以視需要提供其他通道屬性和/或安全性屬性。
-   在成功傳回服務 proxy 或服務端點時，呼叫 helper 常式。

下列各節將詳細說明相關的主題。

## <a name="handle-policy-input"></a>處理原則輸入

以下是與原則處理相關的 [編譯器選項](web-service-compiler-tool.md) 。

根據預設，除非使用 "/nopolicy" 選項來呼叫，否則 wsutil 一律會產生原則範本。 原則可以內嵌為 WSDL 檔案的一部分，也可以另外建立為 wsutil 做為輸入的原則中繼資料檔案。 編譯器選項 "/wsp：" 可用來指出指定的輸入中繼資料是原則檔。 Wsutil 會使用下列編譯來產生潛在的原則相關協助程式：

**wsutil/wsdl：受信任的 .wsdl/wsdl： trusted1 .wsdl**

**wstuil/wsdl：輸入 .wsdl/wsp： policy .wsp**

使用 "/nopolicy" 選項時，不會產生任何原則協助程式，如下列範例所示。

**wsutil/nopolicy/wsdl：受信任的 .wsdl/wsdl： trusted1 .wsdl**

## <a name="policy-related-code-generated-by-the-wsutil-compiler"></a>Wsutil 編譯器所產生的原則相關程式碼

[中繼資料對應](metadata-mapping.md) 頁面詳細說明元資料結構與不同系結類型之間的對應。

您可以在原則設定中指定三種原則設定類別：

-   通道屬性。 目前僅支援下列通道屬性： [**ws \_ 通道 \_ 屬性 \_ 編碼**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)、 **Ws \_ 通道 \_ 屬性 \_ 定址 \_ 版本** 和 **ws \_ 通道 \_ 屬性 \_ 信封 \_ 版本**。
-   安全性屬性。 目前僅支援下列安全性屬性： [**ws \_ 安全性 \_ 屬性 \_ 時間戳記 \_ 使用**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)方式、 **ws \_ 安全性 \_ 屬性 \_ 安全性 \_ 標 \_ 頭** 配置、 **ws \_ 安全性 \_ 屬性 \_ 傳輸 \_ 保護 \_ 等級** 和 **ws 安全性屬性 \_ \_ \_ 安全性 \_ 標頭 \_ 版本**。
-   安全性系結。 目前僅支援下列安全性系結： [**ws \_ HTTP \_ 標頭 \_ 驗證 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)系結、 [**ws \_ SSL \_ 傳輸 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)系結、ws [**\_ TCP \_ SSPI \_ 傳輸 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)系結、ws 使用者 [**\_ 名稱 \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)系結、 [**ws \_ KERBEROS \_ APREQ \_ 訊息 \_ \_ 安全性**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)系結，以及 [**ws \_ 安全性 \_ 內容 \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)系結。

系結範本類型

Wsutil 支援的系結數目有限。 這些系結所支援的所有組合都會列在 WS 系結 [**\_ \_ 範本 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) 定義中。 例如，在 wsdl 中的下列系結

``` syntax
<soap:binding style="document" transport="http://schemas.xmlsoap.org/soap/http" />
```

Wsutil 會產生這個系結的 [**WS HTTP 系結 \_ \_ \_ 範本 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) 型別系結範本型別。

原則描述

使用輸入原則設定時，wsutil 會產生一組描述輸入原則的原則描述，包括範本類型，以及原則中指定的值。 例如，針對輸入

``` syntax
<wsdl:binding...>
  <soap11:binding.../> =< WS_ENVELOPE_VERSION_SOAP_1_1
</wsdl:binding>
```

wsutil 會產生如下的通道屬性描述：

``` syntax
WS_ENVELOPE_VERSION_SOAP_1_1,
{
  WS_CHANNEL_PROPERTY_ENVELOPE_VERSION,
  (void*)&locaDefinitions.policies.bindHostedClientSoap.envelopeVersion, //points to the WS_ENVELOPE_VERSION_SOAP_1_1 value above
  sizeof(&localDefinitions.policies.bindHostedClientSoap.envelopeVersion),
},
```

在一個系結中) 的所有原則設定 (通道屬性、安全性屬性和安全性系結屬性，都會匯總成一個 WS \_ bindingTemplateType \_ 原則 \_ 描述結構。 [**WS \_系結 \_ 範本 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) 指定 wsutil 支援的不同系結原則組合。

要在應用程式中填入的範本結構

原則描述包含指定系結的輸入中繼資料中指定的所有原則資訊，但在使用這些原則設定來建立服務 proxy 和/或服務端點時，原則中仍需要使用者輸入的資訊。 例如，應用程式必須提供 HTTP 標頭驗證的認證。

應用程式需要在 \_ \_ webservices 中 \_ 定義的每個不同系結範本類型的範本結構（名稱為 WS bindingTemplateType 系結範本）中填入範本結構：

``` syntax
struct WS_bindingTemplateType_BINDING_TEMPLATE
{
  WS_CHANNEL_PROPERTIES channelProperties;
  WS_SECURITY_PROPERTIES securityProperties;
  possible_list_of_SECURITY_BINDING_TEMPLATEs;
  ...
};
```

安全性系結範本的清單是選擇性的，取決於相符的安全性系結。 例如，ws [**\_ ssl \_ 傳輸 \_ 安全性 \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_template) 系結範本欄位會顯示在應用程式的 [**ws \_ HTTP SSL 系結 \_ \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template) 中，以提供 SSL 相關的安全性系結資訊，包括認證資訊。

在呼叫 webservices 範本 Api 之前，應用程式必須填入此結構中的所有欄位。 額外的安全性屬性以及無法在原則中表示的安全性系結屬性必須填入，而 webservices Api 則會在執行時間中合併這兩組屬性。 如果不適用，欄位可能會被清空。 例如，如果不需要額外的安全性屬性，securityProperties 可能會清空。

標頭檔中的 Helper 常式和原則描述宣告

wsutil 會建立 helper 常式，以加速服務模型層級的支援，讓應用程式可以更輕鬆地建立服務 proxy 和服務端點。 原則描述也會公開，讓應用程式可以直接使用它們。 CreateSerivceProxy 的說明常式看起來像這樣：

``` syntax
HRESULT bindingName_CreateServiceProxy(
  __in_ecount_opt(propertyCount) const WS_PROXY_PROPERTY* properties,
  __in const ULONG propertyCount,
  __in WS_constraintName_BINDING_TEMPLATE* templateValue,
  __deref_out WS_SERVICE_PROXY** serviceProxy,
  __in_opt WS_ERROR* error);
```

雖然開發人員也可以直接使用 webservices.dll 所提供的下一個執行時間常式，但仍可使用這些 helper 常式。 開發人員在使用 [服務模型](service-model-layer-overview.md) 層進行程式設計時，不建議直接使用原則描述。

原則描述參考也會在標頭中為 advanced user 產生。 如果開發人員未使用服務模型功能，則可以直接使用原則描述。

``` syntax
struct {
  ...
  struct {
    ...
    } contracts;
  struct {
    WS_bindingTemplateType_POLICY_DESCRIPTION bindingName;
    ...
    } policies;
  }
```

存根檔案中的定義原型

系統會在本機原型結構中建立每個系結的單一原則描述結構欄位，以及其內部參考的 helper 描述。 原則描述會在產生 [**WS \_ 合約 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) 的檔案中產生。 一般來說，開發人員不需要在開發期間檢查存根檔案，但是存根檔案包含有關原則規格的所有詳細資料。

``` syntax
struct {
  ...
  struct {
  ... } contracts;
  ...
 struct {
      struct {
        hierarchy of policy template descriptions;
        } bindingName;
      ...
      list of bindings in the input wsdl file.
  } policies;
} fileNameLocalDefinitions;
```

Stub 檔案中的 Helper 常式執行

Wsutil 會產生 helper 常式，以簡化應用程式呼叫，以根據原則設定中提供的資訊來 [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) 和建立 [**WS \_ 服務 \_ 端點**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) 基底。

取決於針對指定埠指定的系結條件約束，第一個引數會根據範本結構而有所不同。 下列範例假設 HTTP 傳輸，服務 proxy 建立的簽章類似于一個額外的通道類型參數。

``` syntax
HRESULT bindingName_CreateServiceProxy(
    __in WS_bindingTemplateType_BINDING_TEMPLATE* templateValue,
    __in_ecount_opt(propertyCount) const WS_PROXY_PROPERTY* properties,
    __in const ULONG propertyCount,
    __deref_out WS_SERVICE_PROXY** serviceProxy,
    __in_opt WS_ERROR* error)
{
    return WsCreateServiceProxyFromTemplate(
      WS_CHANNEL_TYPE_REQUEST,    // this is fixed for http, requires input for TCP
      properties,     
      propertyCount, 
      WS_bindingTemplateType_BINDING_TEMPLATE_TYPE,
      templateValue,
      sizeof(WS_bindingTemplateType_BINDING_TEMPLATE),  
      &fileName.policies.bindingName,   // template description as generated in the stub file
      sizeof(WS_constraintName_POLICY_DESCRIPTION),
      serviceProxy,     
      error);     
}
```

``` syntax
HRESULT bindingName_CreateServiceEndpoint(
__in WS_bindingTemplateType_BINDING_TEMPLATE* templateValue,
__in_opt const WS_STRING* addressUrl,
__in bindingNameFunctionTable* functionTable,
__in WS_SERVICE_SECURITY_CALLBACK authorizationCallback,
__in const WS_SERVICE_ENDPOINT_PROPERTY* properties,
__in ULONG propertyCount,
__in WS_HEAP* heap,
  __deref_out WS_SERVICE_ENDPOINT** serviceEndpoint,
  __in_opt WS_ERROR* error)
{
  WS_SERVICE_CONTRACT serviceContract;
  serviceContract.contractDescription = &fileName.contracts.bindingName;
  serviceContract.defaultMessageHandlerCallback = NULL;
  serviceContract.methodTable = (const void *)functionTable;

  return WsCreateServiceEndpointFromTemplate(
      properties,
      propertyCount,
      addressUrl,    // service endpoint address
      WS_CHANNEL_TYPE_RESPONSE,    // this is fixed for http, requires input for TCP
      &serviceContract,
      authorizationCallback,
      heap,
      WS_bindingTemplateType_BINDING_TEMPLATE_TYPE,
      templateValue,
      sizeof(WS_bindingTemplateType_BINDING_TEMPLATE),
      &fileName.policies.bindingName,   // template description as generated in the stub file
      sizeof(WS_bindingTemplateType_POLICY_DESCRIPTION),
      serviceEndpoint,
      error);
}
```

## <a name="supported-policy-settings"></a>支援的原則設定

下表列出所有支援的系結範本類型、類型中所需的相符安全性系結、類型的應用程式所要填入的範本結構，以及相符的描述類型。 應用程式必須填入範本結構，而應用程式開發人員應該瞭解指定原則中所需的安全性系結。



| [**WS 系結 \_ \_ 範本 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                                | 安全性系結組合                                                                                                                                                                                                                                                                                                               | 要在應用程式中填入的範本結構                                                                                            | 原則描述                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WS \_ HTTP 系結 \_ \_ 範本 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                          |                                                                                                                                                                                                                                                                                                                                             | [**WS \_ HTTP 系結 \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_http_binding_template)                                                                              | [**WS \_ HTTP \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_http_policy_description)                                                                              |
| [**WS \_ HTTP \_ SSL 系結 \_ \_ 範本 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                     | [**WS \_ SSL \_ 傳輸 \_ 安全性 \_ 系結**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)                                                                                                                                                                                                                                                          | [**WS \_ HTTP \_ SSL 系結 \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template)                                                                     | [**WS \_ HTTP \_ SSL \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description)                                                                     |
| [**WS \_ HTTP \_ 標頭驗證系結 \_ \_ \_ 範本 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                            | [**WS \_ HTTP \_ 標頭 \_ 驗證 \_ 安全性 \_ 系結**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)                                                                                                                                                                                                                                                   | [**WS \_ HTTP \_ 標頭驗證系結 \_ \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_binding_template)                                                    | [**WS \_ HTTP \_ 標頭 \_ 驗證 \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_policy_description)                                                    |
| [**WS \_ HTTP \_ SSL \_ 標頭驗證系結 \_ \_ \_ 範本 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                       | [**WS \_SSL \_ 傳輸 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)系結和 [ **WS \_ HTTP \_ 標頭 \_ 驗證 \_ 安全性 \_** 系結](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)                                                                                                                                                            | [**WS \_ HTTP \_ SSL \_ 標頭驗證系結 \_ \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_binding_template)                                           | [**WS \_ HTTP \_ SSL \_ 標頭 \_ 驗證 \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_policy_description)                                           |
| [**WS \_ HTTP \_ SSL 使用者名稱系結 \_ \_ \_ 範本 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                           | [**WS \_SSL \_ 傳輸 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)系結和 [ **WS 使用者 \_ 名稱 \_ 訊息 \_ 安全性 \_** 系結](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)                                                                                                                                                             | [**WS \_ HTTP \_ SSL 使用者名稱系結 \_ \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_binding_template)                                                  | [**WS \_ HTTP \_ SSL 使用者 \_ 名稱 \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_policy_description)                                                  |
| [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ 系結 \_ \_ 範本 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                    | [**WS \_SSL \_ 傳輸 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)系結和 [ **WS \_ KERBEROS \_ APREQ \_ 訊息 \_ 安全性 \_** 系結](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)                                                                                                                                                | [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ 系結 \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_binding_template)                                     | [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_policy_description)                                     |
| [**WS \_ TCP 系結 \_ \_ 範本 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                           |                                                                                                                                                                                                                                                                                                                                             | [**WS \_ TCP 系結 \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_binding_template)                                                                                | [**WS \_ TCP \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_policy_description)                                                                                |
| [**WS \_ TCP \_ SSPI 系結 \_ \_ 範本 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                     | [**WS \_ TCP \_ SSPI \_ 傳輸 \_ 安全性 \_ 系結**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)                                                                                                                                                                                                                                               | [**WS \_ TCP \_ SSPI 系結 \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_binding_template)                                                                     | [**WS \_ TCP \_ SSPI \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_policy_description)                                                                     |
| [**WS \_ TCP \_ SSPI \_ USERNAME \_ BINDING \_ 範本 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                           | [**WS \_TCP \_ SSPI \_ 傳輸 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)系結和 [ **WS 使用者 \_ 名稱 \_ 訊息 \_ 安全性 \_** 系結](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)                                                                                                                                                  | [**WS \_ TCP \_ SSPI 使用者名稱系結 \_ \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_binding_template)                                                  | [**WS \_ TCP \_ SSPI 使用者 \_ 名稱 \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_policy_description)                                                  |
| [**WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ 系結 \_ \_ 範本 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                    | [**WS \_TCP \_ SSPI \_ 傳輸 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)系結和 [ **WS \_ KERBEROS \_ APREQ \_ 訊息 \_ 安全性 \_** 系結](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)                                                                                                                                     | [**WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ 系結 \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_binding_template)                                     | [**WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_policy_description)                                     |
| [**WS \_ HTTP \_ SSL 使用者 \_ 名稱 \_ 安全性內容系結 \_ \_ \_ 範本 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)        | [**WS \_啟動程式通道中的 SSL \_ 傳輸 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) 系結和 [**ws \_ 安全性 \_ 內容 \_ 訊息 \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) 安全性系結與 [**ws 使用者 \_ 名稱 \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) 系結                         | [**WS \_ HTTP \_ SSL 使用者 \_ 名稱 \_ 安全性 \_ 內容 \_ \_ 系結範本**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_binding_template)              | [**WS \_ HTTP \_ SSL 使用者 \_ 名稱 \_ 安全性 \_ 內容 \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_policy_description)              |
| [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ 安全性 \_ 內容系結 \_ \_ 範本 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) | [**WS \_在 \_ 啟動 \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)程式通道中使用 [**ws \_ KERBEROS \_ APREQ \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)系結的 SSL 傳輸安全性系結和 [**ws \_ 安全性 \_ 內容 \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)系結            | [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ 安全性 \_ 內容 \_ \_ 系結範本**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_binding_template) | [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ 安全性 \_ 內容 \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_policy_description) |
| [**WS \_ TCP \_ SSPI 使用者 \_ 名稱 \_ 安全性內容系結 \_ \_ \_ 範本 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)        | [**WS \_在啟動程式通道中使用 Ws 使用者 \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) [**\_ 名稱 \_ 訊息 \_ \_ 安全性**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)系結的 TCP SSPI 傳輸安全性系結和 [**ws \_ 安全性 \_ 內容 \_ 訊息 \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)安全性系結              | [**WS \_ TCP \_ SSPI 使用者 \_ 名稱 \_ 安全性 \_ 內容 \_ \_ 系結範本**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_binding_template)              | [**WS \_ TCP \_ SSPI 使用者 \_ 名稱 \_ 安全性 \_ 內容 \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_policy_description)              |
| [**WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ 安全性 \_ 內容系結 \_ \_ 範本 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) | [**WS \_在啟動程式通道中 \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)使用 [**ws \_ KERBEROS \_ APREQ \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)系結的 TCP SSPI 傳輸安全性系結和 [**ws \_ 安全性 \_ 內容 \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)系結 | [**WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ 安全性 \_ 內容 \_ \_ 系結範本**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_binding_template) | [**WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ 安全性 \_ 內容 \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_policy_description) |



 

例如， [**ws \_ HTTP SSL 系結 \_ \_ \_ 範本 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) 指出系結的輸入原則會指定 HTTP 傳輸和 [**WS \_ SSL \_ 傳輸 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)系結。 應用程式必須在呼叫 helper 常式之前填入 [**ws \_ HTTP ssl 系結 \_ \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template) 結構，而比對原則描述為 [**WS \_ HTTP \_ ssl \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description)。 更具體來說，WSDL 中的系結區段包含下列區段：

``` syntax
<wsp:Policy...>
  <sp:TransportBinding...>
    <wsp:Policy...>
      <sp:TransportToken...>
        <wsp:Policy...>
          <sp:HttpsToken.../>
        </wsp:Policy...>
      </sp:TransportToken...>
    </wsp:Policy>
  </sp:TransportBinding...>
</wsp:Policy>
```

``` syntax
<wsdl:binding...>
<soap11:binding.../> => WS_ENVELOPE_VERSION_SOAP_1_1
</wsdl:binding>
```

## <a name="security-context-support"></a>安全性內容支援

在 [安全性內容](security-context.md)中，會建立啟動程式通道來建立服務通道中的安全交談。 Wsutil 只支援使用相同通道屬性和安全性屬性的啟動程式通道與服務通道相同的案例。 安全性內容訊息系結需要傳輸安全性;wsutil 支援啟動程式通道與其他訊息安全性系結，但僅支援在服務通道中作為唯一訊息安全性系結的安全性內容，而不結合其他訊息安全性系結。 開發人員可以支援原則範本支援以外的組合。

下列列舉是原則支援的一部分：

-   [**WS 系結 \_ \_ 範本 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)

下列函數是原則支援的一部分：

-   [**WsCreateServiceEndpointFromTemplate**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceendpointfromtemplate)
-   [**WsCreateServiceProxyFromTemplate**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxyfromtemplate)

下列結構是原則支援的一部分：

-   [**WS \_ HTTP 系結 \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_http_binding_template)
-   [**WS \_ HTTP \_ 標頭驗證系結 \_ \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_binding_template)
-   [**WS \_ HTTP \_ 標頭 \_ 驗證 \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_policy_description)
-   [**WS \_ HTTP \_ 標頭 \_ 驗證安全性系結 \_ \_ \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_policy_description)
-   [**WS \_ HTTP \_ 標頭 \_ 驗證 \_ 安全性 \_ \_ 系結範本**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_template)
-   [**WS \_ HTTP \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_http_policy_description)
-   [**WS \_ HTTP \_ SSL 系結 \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template)
-   [**WS \_ HTTP \_ SSL \_ 標頭驗證系結 \_ \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_binding_template)
-   [**WS \_ HTTP \_ SSL \_ 標頭 \_ 驗證 \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_policy_description)
-   [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ 系結 \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_binding_template)
-   [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_policy_description)
-   [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ 安全性 \_ 內容 \_ \_ 系結範本**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_binding_template)
-   [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ 安全性 \_ 內容 \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_policy_description)
-   [**WS \_ HTTP \_ SSL \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description)
-   [**WS \_ HTTP \_ SSL 使用者名稱系結 \_ \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_binding_template)
-   [**WS \_ HTTP \_ SSL 使用者 \_ 名稱 \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_policy_description)
-   [**WS \_ HTTP \_ SSL 使用者 \_ 名稱 \_ 安全性 \_ 內容 \_ \_ 系結範本**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_binding_template)
-   [**WS \_ HTTP \_ SSL 使用者 \_ 名稱 \_ 安全性 \_ 內容 \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_policy_description)
-   [**WS \_ KERBEROS \_ APREQ \_ 訊息 \_ 安全性系結 \_ \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_policy_description)
-   [**WS \_ KERBEROS \_ APREQ \_ 訊息 \_ 安全性系結 \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_template)
-   [**WS \_ 安全性 \_ 內容 \_ 訊息 \_ 安全性系結 \_ \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_policy_description)
-   [**WS \_ 安全性 \_ 內容 \_ 訊息 \_ 安全性系結 \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_template)
-   [**WS \_ 安全性 \_ 內容 \_ 安全性系結 \_ \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_security_binding_policy_description)
-   [**WS \_ 安全性 \_ 內容 \_ 安全性系結 \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_security_binding_template)
-   [**WS \_ SSL \_ 傳輸 \_ 安全性系結 \_ \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_policy_description)
-   [**WS \_ SSL \_ 傳輸 \_ 安全性系結 \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_template)
-   [**WS \_ SSPI \_ 傳輸 \_ 安全性系結 \_ \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_sspi_transport_security_binding_policy_description)
-   [**WS \_ TCP 系結 \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_binding_template)
-   [**WS \_ TCP \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_policy_description)
-   [**WS \_ TCP \_ SSPI 系結 \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_binding_template)
-   [**WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ 系結 \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_binding_template)
-   [**WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_policy_description)
-   [**WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ 安全性 \_ 內容 \_ \_ 系結範本**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_binding_template)
-   [**WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ 安全性 \_ 內容 \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_policy_description)
-   [**WS \_ TCP \_ SSPI \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_policy_description)
-   [**WS \_ TCP \_ SSPI \_ 傳輸 \_ 安全性系結 \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_template)
-   [**WS \_ TCP \_ SSPI 使用者名稱系結 \_ \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_binding_template)
-   [**WS \_ TCP \_ SSPI 使用者 \_ 名稱 \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_policy_description)
-   [**WS \_ TCP \_ SSPI 使用者 \_ 名稱 \_ 安全性 \_ 內容 \_ \_ 系結範本**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_binding_template)
-   [**WS \_ TCP \_ SSPI 使用者 \_ 名稱 \_ 安全性 \_ 內容 \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_policy_description)
-   [**WS 使用者 \_ 名稱 \_ 訊息安全性系結 \_ \_ \_ 原則 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_policy_description)
-   [**WS 使用者 \_ 名稱 \_ 訊息安全性系結 \_ \_ \_ 範本**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_template)

 

 




