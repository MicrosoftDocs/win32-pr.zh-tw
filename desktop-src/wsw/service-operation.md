---
title: 服務作業
description: 服務作業是與服務的特定作業相關聯的程式碼和中繼資料。
ms.assetid: 788940a0-b1d9-45d7-a4b5-6f0926026c7d
keywords:
- Windows 的服務操作 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5acde0c2151dea483a3e82f45c7031fa201614076f7a5ea624926fbe08e7588b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026259"
---
# <a name="service-operation"></a>服務作業

服務作業是與服務的特定作業相關聯的程式碼和中繼資料。


就 WSDL 而言，指定 portType 的 WSDL 檔案中定義的每個 wsdl： operation 都是服務作業。

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

服務模型內的每個服務作業都會被指定為 [**WS 作業 \_ \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)。 WS \_ 操作 \_ 描述是由 [wsutil.exe](web-service-compiler-tool.md)產生。

針對每個 wsdl： operation，此工具會產生個別的 [**WS 作業 \_ \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)。

![顯示 wsutil.exe 如何產生 WS_CONTRACT_DESCRIPTION 的圖表。](images/porttypetocontract.png)

``` syntax
static WS_OPERATION_DESCRIPTION serviceOperationsICalculator[] =
{
    {
        // Add Method
        &messageDescriptionAddICalculator,
        &messageDescriptionAddResponseICalculator,
        WsCountOf(parametersAddICalculator),
        ICalculator_Add_Stub 
    }
};
```

就程式碼而言，每個服務作業都有相關聯的函式。 用戶端和伺服器的此函式定義不同。

服務作業會分類為

-   [用戶端服務作業](client-side-service-operations.md)
-   [伺服器端服務作業](server-side-service-operations.md)

這項分類主要是根據伺服器的簽章配置和服務作業的用戶端執行。

另請參閱 [WSDL 支援區段](wsdl-support.md)。

下列列舉會搭配服務作業使用：

-   [**WS \_ 參數 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_parameter_type)
-   [**WS \_ 服務 \_ 取消 \_ 原因**](/windows/desktop/api/WebServices/ne-webservices-ws_service_cancel_reason)
-   [**WS \_ 服務 \_ 操作 \_ 訊息 \_ 選項**](/windows/win32/api/webservices/ne-webservices-ws_charset)

下列結構會搭配服務作業使用：

-   [**WS \_ 訊息 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description)
-   [**WS \_ 操作 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)
-   [**WS \_ 參數 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description)

 

 




