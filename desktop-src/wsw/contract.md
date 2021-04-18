---
title: 合約
description: 服務合約會攜帶中繼資料來定義服務處理通道訊息的方式。
ms.assetid: 670530bf-344b-4480-8357-8984d80c0c68
keywords:
- 適用于 Windows 的合約 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7120346dac4d11c21955cd2430ed0a7dc277e88c
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "104555640"
---
# <a name="contract"></a>合約

服務合約會攜帶中繼資料來定義服務處理通道訊息的方式。


[**Ws \_ 服務 \_ 合約**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract)會攜帶服務的中繼資料來處理 [WS \_ 訊息](ws-message.md)。

![顯示訊息中 WS_SERVICE_CONTRACT 服務端點之中繼資料的圖表。](images/servicecontractintro.png)

它有 [**WS \_ 合約 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) 和函式資料表。 應用程式可以選擇性地指定 [**WS \_ 服務 \_ 訊息 \_ 接收 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)。

如果未指定 [**ws \_ 合約 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) 和函式資料表，則需要應用程式來指定 [**ws \_ 服務 \_ 訊息 \_ 接收 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)。

![此圖顯示 ICalculator 服務合約中的「新增」和「減少」服務作業。](images/servicecontract.png)


``` syntax
static WS_SERVICE_CONTRACT calculatorContract = 
{
    &calculatorContractDescription, 
    NULL, 
    &calculatorFunctions, 
};
```

如需詳細資訊，請參閱 [計算機](httpcalculatorserviceexample.md) 範例。

合約描述

[**WS \_合約 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) 是定義服務類型合約的中繼資料。 由 [wsutil.exe](web-service-compiler-tool.md)產生。

就 WSDL 而言， [**WS \_ 合約 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) 會對應到 wsdl： portType。 針對 WSDL 檔案中的每個 wsdl： portType，將會產生個別的 **WS \_ 合約 \_ 描述** 。

合約描述是由一或多個 [服務作業](service-operation.md)所組成。 這些作業會以 [**WS \_ 操作 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)的陣列形式提供。

![顯示 WS_CONTRACT_DESCRIPTION 為 WS_OPERATION_DESCRIPTIONs 陣列的圖表。](images/porttypetocontract.png)

``` syntax
<wsdl:definitions xmlns:soap="https://schemas.xmlsoap.org/wsdl/soap/" 
xmlns:wsu="https://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" 
xmlns:soapenc="https://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="https://Example.org" 
xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="https://schemas.xmlsoap.org/ws/2004/09/policy" 
xmlns:wsap="https://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xsd="https://www.w3.org/2001/XMLSchema" 
xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="https://www.w3.org/2006/05/addressing/wsdl" 
xmlns:soap12="https://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="https://www.w3.org/2005/08/addressing" 
xmlns:wsx="https://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="https://Example.org" 
xmlns:wsdl="https://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ICalculator">
  <wsdl:operation name="Add">
   <wsdl:input wsaw:Action="https://Example.org/ICalculator/Add" 
   message="tns:ICalculator_Add_InputMessage" />
   <wsdl:output wsaw:Action="https://Example.org/ICalculator/AddResponse" 
   message="tns:ICalculator_Add_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
</wsdl:definitions>
```

如需 wsdl： portType to [**WS \_ CONTRACT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) 轉換的詳細資訊，請參閱 [wsdl 輸出一節](wsdl-support.md)。

範例： [ **WS \_ 合約 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)

``` syntax
static WS_CONTRACT_DESCRIPTION contractDescriptionICalculator =
{
    WsCountOf(serviceOperationsICalculator),
    serviceOperationsICalculator
};
```

函數資料表

函數資料表是函式指標的結構，代表服務合約中的每個 [服務作業](service-operation.md) 。 [wsutil.exe](web-service-compiler-tool.md)也會產生函數表定義。

範例：函數資料表

``` syntax
 // Function Table
struct CalculatorServiceFunctionTable
{
      AddOperation Add;
      SubtractOperation Subtract;
};

// Populate the Function Table
static const CalculatorServiceFunctionTable calculatorFunctions = {Add, Subtract};
```

使用 [ **WS \_ 服務 \_ 訊息 \_ 接收 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)

[**WS \_服務 \_ 訊息 \_ 接收 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback) 有雙重互斥角色。

如果 [**ws \_ 服務 \_ 合約**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract)上指定了 [**ws \_ 合約 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)，這會成為指定的 **WS \_ 合約 \_ 描述** 不支援之所有動作的預設訊息處理常式。 否則，如果 ws **\_ 服務 \_ 合約** 上未指定 **ws \_ 合約 \_ 描述**，而且 ws 服務 [**\_ \_ 訊息 \_ 接收 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)是在 **ws \_ 服務 \_ 合約** 上指定，則所有的 [訊息](ws-message.md)都會傳遞至此回呼。

如需更多範例，請參閱

-   [不具類型的服務範例](untypedserviceexample.md)
-   [計算機服務範例](httpcalculatorserviceexample.md)
-   [服務作業](service-operation.md)

下列回呼是合約的一部分：

-   [**WS \_ 服務 \_ 訊息 \_ 接收 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)
-   [**WS \_ 服務 \_ 存根 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_service_stub_callback)

下列結構是合約的一部分：

-   [**WS \_ 合約 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)
-   [**WS \_ 服務 \_ 合約**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract)

 

 




