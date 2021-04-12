---
title: 服務模型層總覽
description: WWSAPI 服務模型 API 會將用戶端與服務之間的通訊模型為方法呼叫，而不是資料訊息。
ms.assetid: a1ed1e3c-94ae-4383-9251-83caf2e3ebf3
keywords:
- 適用于 Windows 的服務模型層總覽 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c74861f0e2ed13b35e308d1314aec2a33dc28c31
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "104321423"
---
# <a name="service-model-layer-overview"></a>服務模型層總覽

WWSAPI 服務模型 API 會將用戶端與服務之間的通訊模型為方法呼叫，而不是資料訊息。 相較于在用戶端與服務之間支援更傳統[訊息](message.md)交換的[通道層](channel-layer-overview.md)，服務模型會透過用戶端上的服務 proxy 和服務上的服務主機，自動管理通訊。 這表示用戶端會呼叫產生的函式，而伺服器會執行回呼。


例如，假設有一個計算機服務，其會在兩個數字上執行加法和減法。 加法和減法是自然表示為方法呼叫的作業。

![顯示計算機服務如何使用方法呼叫來與用戶端通訊的圖表，以進行加法和減法。](images/servicemodelintro.png)

服務模型表示用戶端與服務之間的通訊是宣告方法呼叫，因此會從應用程式中隱藏基礎通道層的通訊詳細資料，讓服務更容易執行。

## <a name="specifying-a-service"></a>指定服務

您必須根據訊息交換模式以及其網路資料標記法來指定服務。 針對服務，此規格通常會以 WSDL 和 XML 架構檔的形式提供。

WSDL 檔案是一份 XML 檔，其中包含通道系結和服務的訊息交換模式，而 XML 架構檔則是一種 XML 檔，可定義個別訊息的資料標記法。

針對計算機服務及其加法和減法運算，WSDL 檔案看起來可能如下列範例所示：

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

同樣地，其 XML 架構可以定義如下：

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="Add">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="a" type="xs:int" />
    <xs:element minOccurs="0" name="b" type="xs:int" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
 <xs:element name="AddResponse">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="result" type="xs:int" 
    />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
</xs:schema> 
```

## <a name="converting-metadata-to-code"></a>將中繼資料轉換為程式碼

服務模型提供 [WsUtil.exe](web-service-compiler-tool.md) 做為處理這些元資料檔案的工具，將 WSDL 檔案轉換成 C 標頭和原始程式檔。

![此圖顯示 WsUtil.exe 如何將 WSDL 檔案轉換成 C 標頭和來源檔案。](images/doctotool.png)

[WsUtil.exe](web-service-compiler-tool.md)會產生服務的標頭和來源，以及用戶端的用戶端服務作業。

## <a name="calling-the-calculator-service-from-a-client&quot;></a>從用戶端呼叫計算機服務

如同服務的執行，用戶端必須包含產生的標頭或標頭。

``` syntax
#include &quot;CalculatorProxyStub.h&quot;
```

現在，用戶端應用程式可以建立並開啟服務 proxy，以開始與計算機服務進行通訊。

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
WS_STRING uri= WS_STRING_VALUE(L&quot;http://localhost/example");
address.uri = uri;

if (FAILED (hr = WsCreateServiceProxy(WS_CHANNEL_TYPE_REQUEST, WS_HTTP_CHANNEL_BINDING, NULL, NULL, 0, &serviceProxy, error)))
    goto Error;

if (FAILED (hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error)))
    goto Error;
```

應用程式可以使用下列程式碼，在計算機服務上呼叫 Add 作業：

``` syntax
if (FAILED (hr = DefaultBinding_ICalculator_Add(serviceProxy, heap, 1, 2, &result, NULL, 0, NULL, error)))
    goto Error;
```

請參閱 [HttpCalculatorClientExample](httpcalculatorclientexample.md) 中的程式碼範例，以取得計算機服務的完整執行。

## <a name="service-model-components"></a>服務模型元件

在計算機範例中，個別 WWSAPI 服務模型元件的互動如下所示：

-   用戶端會建立 [服務 proxy](service-proxy.md) 並加以開啟。
-   用戶端會呼叫服務的新增函式，並傳入服務 proxy。
-   訊息會根據中繼資料工具所產生的標頭和原始程式檔中的序列化中繼資料進行序列化， ([WsUtil.exe](web-service-compiler-tool.md)) 。
-   訊息會寫入至通道，並透過網路傳送至服務。
-   在伺服器端，此服務會裝載于服務主機內，並有接聽 ICalculator 合約的端點。
-   在存根中使用服務模型中繼資料時，服務會將來自用戶端的訊息還原序列化，並將其分派給存根。
-   伺服器端服務會呼叫 Add 方法，並將作業內容傳遞給它。 此操作內容包含內送訊息的參考。

![顯示個別 WWSAPI 服務模型元件互動的圖表。](images/servicemodellayout.png)

單元

-   [服務主機](service-host.md)：裝載服務。
-   [服務 proxy](service-proxy.md)：定義用戶端與服務通訊的方式。
-   [CoNtext](context.md)：讓特定狀態資訊可供服務作業使用的屬性包。
-   [合約](contract.md)：服務的介面定義。 例如，在我們的範例程式碼中，ICalculator 代表計算機服務的合約。
-   [WsUtil.exe](web-service-compiler-tool.md)：用來產生 proxy 和存根的服務模型中繼資料工具。

 

 




