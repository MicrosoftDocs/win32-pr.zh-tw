---
title: WSDL 和服務合約
description: Wsutil.exe 公用程式會根據提供的 WSDL 中繼資料來產生 C 語言存根，以及使用者撰寫之 XML 架構所描述之資料類型的資料類型定義和描述。
ms.assetid: d3c147d6-e370-4e8a-96d8-6660f3a2b996
keywords:
- WSDL 支援
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b273bd97d30aca185f35f31d385e6ab5a0bef4e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882291"
---
# <a name="wsdl-and-service-contracts"></a>WSDL 和服務合約

[Wsutil.exe](web-service-compiler-tool.md)公用程式會根據提供的 WSDL 中繼資料來產生 C 語言存根，以及使用者撰寫之 XML 架構所描述之資料類型的資料類型定義和描述。


以下是範例 WSDL 檔案和 XML 架構，作為後續討論的基礎：

``` syntax
<?xml version="1.0" encoding="utf-8"?>
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:types>
  <xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
  targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
   <xs:element name="SimpleMethod">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="a" type="xs:int" />
      <xs:element name="b" type="xs:int" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
   <xs:element name="SimpleMethodResponse">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="b" type="xs:int" />
      <xs:element name="c" type="xs:int" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
  </xs:schema>
 </wsdl:types>
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
 <wsdl:portType name="ISimpleService">
  <wsdl:operation name="SimpleMethod">
   <wsdl:input wsaw:Action="http://Example.org/ISimpleService/SimpleMethod" 
   message="tns:ISimpleService_SimpleMethod_InputMessage" />
   <wsdl:output wsaw:Action="http://Example.org/ISimpleService/SimpleMethodResponse" 
   message="tns:ISimpleService_SimpleMethod_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
 <wsdl:binding name="DefaultBinding_ISimpleService" type="tns:ISimpleService">
  <soap:binding transport="http://schemas.xmlsoap.org/soap/http" />
  <wsdl:operation name="SimpleMethod">
   <soap:operation soapAction="http://Example.org/ISimpleService/SimpleMethod" 
   style="document" />
   <wsdl:input>
    <soap:body use="literal" />
   </wsdl:input>
   <wsdl:output>
    <soap:body use="literal" />
   </wsdl:output>
  </wsdl:operation>
 </wsdl:binding>
 <wsdl:service name="SimpleService">
  <wsdl:port name="ISimpleService" binding="tns:DefaultBinding_ISimpleService">
   <soap:address location="http://Example.org/ISimpleService" />
  </wsdl:port>
 </wsdl:service>
</wsdl:definitions>
```

這個範例會提供合約 ISimpleService，具有單一方法 SimpleMethod。 「SimpleMethod」有兩個類型為 **integer**、 *a* 和 *b* 的輸入參數，會從用戶端傳送至服務。 同樣地，SimpleMethod 有兩個類型為 **integer**、 *b* 和 *c* 的輸出參數，會在成功完成之後傳回給用戶端。 在 SAL 批註的 C 語法中，方法定義顯示如下：

``` syntax
void SimpleMethod(__in int a, __inout int *  b, __out int * c );
```

在此定義中，ISimpleService 是具有單一服務作業的服務合約： SimpleMethod。

輸出標頭檔包含外部參考的定義和描述。 這包括：

-   全域元素類型的 C 結構定義。
-   目前檔案中定義的作業原型。
-   WSDL 檔案中指定之合約的函數資料表原型。
-   目前檔案中指定之所有函式的用戶端 proxy 和服務存根原型。
-   目前檔案中定義之全域架構元素的 [**WS \_ 元素 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) 資料結構。
-   目前檔案中指定之所有訊息的 [**WS \_ 訊息 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) 資料結構。
-   目前檔案中指定之所有合約的 [**WS \_ 合約 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) 資料結構。

產生一個全域結構來封裝架構類型的所有全域描述，以及應用程式可以參考的服務模型類型。 結構是使用正規化的檔案名來命名。 在此範例中，Wsutil.exe 會產生名為「範例 wsdl」的全域定義結構 \_ ，其中包含所有 web 服務描述。 結構定義是在存根檔案中產生的。

``` syntax
typedef struct _example_wsdl
{
  struct {
    WS_ELEMENT_DESCRIPTION SimpleMethod;
    WS_ELEMENT_DESCRIPTION SimpleMethodResponse;
  } elements;
  struct {
    WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_InputMessage;
    WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_OutputMessage;
  } messages;
  struct {
    WS_CONTRACT_DESCRIPTION DefaultBinding_ISimpleService;
  } contracts;
} _example_wsdl;

extern const _stockquote_wsdl stockquote_wsdl;
```

針對 XML 架構檔中的全域元素定義 (XSD) ，會針對每個專案產生一個 [**WS \_ 元素 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) 原型，以及對應的 C 類型定義。 SimpleMethod 和 SimpleMethodResponse 之元素描述的原型會以上述結構中的成員來產生。 C 結構的產生方式如下：

``` syntax
typedef struct SimpleMethod
{
  int   a;
  int   b;
} SimpleMethod;

typedef struct SimpleMethodResponse
{
  int   b;
  int   c;
} SimpleMethodResponse;
```

類似于全域複雜型別，Wsutil.exe 會產生類似上述的類型 C 結構定義，而不會有相符的元素描述。

針對 WSDL 輸入，Wsutil.exe 會產生下列原型和定義：

-   訊息描述會產生 [**WS \_ 訊息 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) 原型。 這項描述可供服務模型以及訊息層使用。 訊息描述結構是全域結構中名稱為 "messagename" 的欄位。 在此範例中，訊息描述會產生為 \_ \_ ISimpleService SimpleMethod InputMessage 結構中的 ISimpleService SimpleMethod InputMessage 欄位 \_ \_ （如同 WSDL 檔案中所指定）。
-   [**WS \_合約 \_ 描述原型是**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) 針對合約描述產生的。 服務模型會使用此描述。 合約描述結構是全域結構中名稱為 "contractname" 的欄位。 在此範例中，合約描述會以「 \_ 範例 wsdl」結構中的 Binder.defaultbinding ISimpleService 欄位形式產生 \_ \_ 。

作業和類型規格通用於 proxy 和存根，兩者都是在這兩個檔案中產生的。 只有當相同檔案中同時產生 proxy 和存根時，Wsutil.exe 才會產生一個複本。

## <a name="identifier-generation"></a>識別碼產生

上面所列的自動產生 C 結構會根據 WSDL 檔案中指定的名稱建立。 XML NCName 通常不會被視為有效的 C 識別碼，並且會視需要將名稱正規化。 十六進位值不會轉換，而且像是 '： '、'/' 和 '. ' 的一般字母都會轉換成底線 ' \_ ' 字元，以改善可讀性。

## <a name="header-for-the-stub"></a>存根的標頭

針對服務合約中的每個作業，會產生一個名為 " &lt; operationname 回呼" 的回呼常式 &gt; 。  (例如，範例服務合約中的「SimpleMethod」作業會有一個名為 "SimpleMethodCallback" 的回撥。 ) 

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT * context,
  int a, int *b, int *c,
  const WS_ASYNC_CONTEXT *asyncContext,
  WS_ERROR * error);
```

針對每個 WSDL **portType** Wsutil.exe 會產生代表 **portType** 的函式資料表。 **PortType** 上的每個作業都有對應的函式指標，可指向函式資料表中存在的回呼。

``` syntax
struct ISimpleServiceMethodTable
{
  ISimpleService_SimpleMethodCallback SimpleMethod;
};
```

所有作業都會產生 Proxy 原型。 原型名稱是在此案例中 (的作業名稱，) 在服務合約的 WSDL 檔案中指定 "SimpleMethod"。

``` syntax
HRESULT WINAPI SimpleMethod(WS_CHANNEL *channel,
  WS_HEAP *heap,
  int a,
  int *b,
  int *c,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR * error );
```

## <a name="local-only-description-prototype-generation"></a>僅限本機描述原型產生

Proxy andstub 檔包含全域定義結構的定義，包括包含僅限本機描述和用戶端 proxy/服務存根執行之結構的原型和定義。

存根檔案的本機所有原型和定義都會產生成封裝結構的一部分。 這個整體的本機描述結構提供了序列化層和服務模型所需之描述的清楚階層。 本機描述結構的原型類似如下所示：

``` syntax
struct _filenameLocalDefinitions
{
  struct {
  // schema related output for all the embedded 
  // descriptions that needs to describe global complex types.
  } globalTypes;
  // global elements.
  struct {
  // schema related output, like field description
  // structure description, element description etc.
  ...
  } globalElements;
  struct {
  // messages and related descriptions
  } messages;
  struct {
  // contract and related descriptions.
  } contracts;
  struct {
  // XML dictionary entries.
  } dictionary;
} _filenameLocalDefinitions;
```

## <a name="referencing-definitions-from-other-files"></a>參考其他檔案的定義

本機定義可以參考另一個檔案中產生的描述。 例如，訊息可能會定義在從 WSDL 檔案產生的 C 程式碼檔案中，但可以在 XSD 檔案所產生的 C 程式碼檔案中的其他地方定義 message 元素。 在此情況下，Wsutil.exe 會從包含訊息定義的檔案產生全域元素的參考，如下所示：

``` syntax
{  // WS_MESSAGE_DESCRIPTION
...
(WS_ELEMENT_DESRIPTION *)b_xsd.globalElement.<elementname>
  };
```

## <a name="global-element-descriptions"></a>全域元素描述

針對 wsdl： type 或 XSD 檔中定義的每個全域元素， **GlobalElement** 欄位內都有一個名為 **elementName** 的相符欄位。 在此範例中，會產生名為 SimpleMethod 的結構：

``` syntax
typedef struct _SimpleServiceLocal
{
  struct  // global elements
  {
    struct // SimpleMethod
    {
    ...
    WS_ELEMENT_DESCRIPTION SimpleMethod;
    } SimpleMethod;
    ...
  } globalElements;
}
```

元素描述所需的其他描述會產生為包含結構的一部分。 如果元素是簡單類型專案，則只有一個 [**WS \_ 元素 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) 欄位。 如果元素類型是結構，則所有相關的欄位和結構描述都會產生為元素結構的一部分。 在此範例中，SimpleMethod 元素是包含兩個欄位 **a** 和 **b** 的結構。 Wsutil.exe 會產生結構，如下所示：

``` syntax
...
struct // SimpleMethod
{
  struct // SimpleMethod structure
  {
    WS_FIELD_DESCRIPTION a;
    WS_FIELD_DESCRIPTION b;
    WS_FIELD_DESCRIPTION * SimpleMethodFields [2];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleMethoddescs; // SimpleMethod
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleMethod;
...
```

內嵌結構和內嵌元素會視需要產生為子結構。

## <a name="wsdl-related-definitions"></a>WSDL 相關定義

Wsutil.exe 會針對指定的 wsdl：服務下定義的每個 **portType** 值，在 WSDL 區段下產生欄位。

``` syntax
...
struct { // WSDL
    struct { // portTypeName
        struct { // operationName
        } operationName;
    ...
    WS_OPERATION_DESCRIPTION* operations[numOperations];
    WS_CONTRACT_DESCRIPTION contractDesc;
    } portTypeName;
}
...
```

Wsutil.exe 會產生一個 f 欄位，其中包含作業所需的所有描述、每個方法的每個作業描述的指標單一陣列，以及指定之 **portType** 的一個 [**WS \_ 合約 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)。

作業所需的所有描述都會在指定的 **portType** 下的 **operationName** 欄位內產生。 這些包括 [**WS \_ 元素 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) 欄位，以及輸入和輸出參數 s 的子結構。 同樣地，輸入訊息和選擇性輸出訊息的 [**WS \_ 訊息 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) 欄位也會與一起包含： [**WS \_作業 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description) 本身的所有作業參數和 [**WS \_ 操作 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) 欄位的參數描述清單欄位。 在此範例中，會產生 SimpleMethod 描述的程式碼結構，如下所示：

``` syntax
...
struct // messages
{
  WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_InputMessage;
  WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_OutputMessage;
} messages;
struct // contracts
{
  struct // DefaultBinding_ISimpleService
  {
    struct // SimpleMethod
    {
      WS_PARAMETER_DESCRIPTION params[3];
      WS_OPERATION_DESCRIPTION SimpleMethod;
    } SimpleMethod;
    WS_OPERATION_DESCRIPTION* operations[1];
    WS_CONTRACT_DESCRIPTION contractDesc;
  } DefaultBinding_ISimpleService;
} contracts;
...
```

## <a name="xml-dictionary-related-definitions"></a>XML 字典相關定義

在各種描述中使用的名稱和命名空間會產生為類型為 [**WS \_ XML \_ 字串**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)的欄位。 所有這些字串都會產生為每個檔案常數位典的一部分。 下列範例中 (名為 **dict** 的字串清單和 [**WS \_ XML \_ 字典**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary)欄位) 會產生為 **fileNameLocal** 結構的 DICTIONARY 欄位的一部分。

``` syntax
struct { // fileNameLocal
...
  struct { // dictionary
    struct { // XML string list
      WS_XML_STRING firstFieldName;
      WS_XML_STRING firstFieldNS;
      ...
    } xmlStrings;
  WS_XML_DICTIONARY dict;
  } dictionary;
}; // fileNameLocal;
```

[**Ws \_ xml \_ 字串**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)的陣列會產生為類型為 **ws \_ xml \_ 字串** 的一數列欄位，並以使用者易記名稱命名。 產生的存根會在各種描述中使用易記的名稱，以提供更好的可讀性。

適用于 WSDL 作業的用戶端 proxy

Wsutil.exe 會針對所有作業產生用戶端 proxy。 應用程式可以使用前置詞命令列選項來覆寫方法簽章。

``` syntax
HRESULT WINAPI bindingName_SimpleMethod(WS_SERVICE_PROXY *serviceProxy,
  WS_HEAP *heap,
  int a,
  int *b,
  int *c,
  const WS_CALL_PROPERTY* callProperties,
  ULONG callPropertyCount,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR * error )
{
  void* argList[] = {&a, &b, &c};
  return WsCall(_serviceProxy,
    (WS_OPERATION_DESCRIPTION*)&example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.SimpleMethod.SimpleMethod,
    (void **)&_argList,
    callProperties,
    callPropertyCount,
    heap,
    asyncContext,
    error
  );      
}
```

作業呼叫端必須傳入有效的 *堆積* 參數。 輸出參數會使用 \_ *堆積* 參數中指定的 WS 堆積值進行配置。 呼叫的函式可以重設或釋放堆積，以釋放所有輸出參數的記憶體。 如果作業失敗，則可以從選擇性的錯誤物件中取出其他詳細資訊（如果有的話）。

Wsutil.exe 會針對系結中所述的所有作業產生服務存根。

``` syntax
HRESULT CALLBACK ISimpleService_SimpleMethodStub(
  const WS_OPERATION_CONTEXT *context,
  void * stackStruct,
  void * callback,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR *error )
{
  SimpleMethodParamStruct *pstack = (SimpleMethodParamStruct *) stackstruct;
  SimpleMethodOperation operation = (SimpleMethodOperation)callback;
  return operation(context, pstack->a, &(pstack->b), &(pstack->c ), asyncContext, error );
}
```

上一節描述本機結構的原型，其中包含僅限存根檔案本機的所有定義。 後續各節將說明描述的定義。

## <a name="wsdl-definition-generation"></a>WSDL 定義產生

Wsutil.exe 會產生一個常數靜態 (**const 靜態**) 結構，名為 *<檔案名 \_*>local，其中包含所有僅限本機定義的<*服務 \_ 名稱*>。

``` syntax
const static _SimpleServiceLocal example_wsdlLocalDefinitions =
{
  {  // global types
  ...
  }, // global types
  {  // global elements
  ...
  }, // global elements
  {  // messages
  ...
  }, //messages
  ...
  {  // dictionary
  ...
  }, // dictionary
},
```

以下是支援的 WSDL 描述：

-   wsdl：服務
-   wsdl： binding
-   wsdl： portType
-   wsdl： operation
-   wsdl： message

## <a name="processing-wsdloperation-and-wsdlmessage"></a>處理 wsdl： operation 和 wsdl： message

在 WSDL 檔案中指定的每個作業都會 [Wsutil.exe](web-service-compiler-tool.md)對應至服務作業。 此工具會為伺服器和用戶端產生個別的服務作業定義。

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ISimpleService">
  <wsdl:operation name="SimpleMethod">
   <wsdl:input wsaw:Action="http://Example.org/ISimpleService/SimpleMethod" 
   message="tns:ISimpleService_SimpleMethod_InputMessage" />
   <wsdl:output wsaw:Action="http://Example.org/ISimpleService/SimpleMethodResponse" 
   message="tns:ISimpleService_SimpleMethod_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
</wsdl:definitions>
```

此工具會評估輸入 andoutput 訊息資料項目的版面配置，以產生基礎結構的序列化中繼資料，以及與輸入和輸出訊息相關聯之結果服務作業的實際簽章。

特定 **portType** 內每項作業的中繼資料都具有輸入和選擇性的輸出訊息，而每個訊息都會對應到 [**WS \_ 訊息 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description)。 在此範例中，會將 portType 中作業的輸入和輸出訊息對應至 inputMessageDescription，並選擇性地對應至 [**WS 作業 \_ \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) 上的 outputMessageDescription。

此工具會針對每個 WSDL 訊息產生參考 [**ws \_ 元素 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)定義的 [**ws \_ 訊息 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description)，如下所示：

``` syntax
... 
{    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

訊息描述會參考輸入元素描述。 因為元素是全域定義的，所以訊息描述會參考全域定義，而不是本機靜態元素。 同樣地，如果元素定義在另一個檔案中，Wsutil.exe 會在該檔案中產生全域定義結構的參考。 例如，如果 SimpleMethodResponse 定義在另一個範例 .xsd 檔中，Wsutil.exe 會改為產生下列內容：

``` syntax
...
{    // message description for ISimpleService_SimpleMethod_InputMessage
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
(WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_xsd.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

每個訊息描述都會包含動作和特定的專案描述， (所有訊息資料元素之類型 [**WS \_ 元素 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)) 的欄位。 如果是 RPC 樣式的訊息或具有多個部分的訊息，則會建立包裝函式專案來封裝額外的資訊。

## <a name="rpc-style-support"></a>RPC 樣式支援

Wsutil.exe 根據適用于 SOAP 1.2 規格的 WSDL 1.1 系結延伸模組，支援檔樣式和 RPC 樣式的作業。 RPC 和常值樣式的作業會標示為 WS \_ RPC \_ 常值 \_ 運算。 服務模型會忽略 RPC/常值作業中回應主體包裝函式專案的名稱。

Wsutil.exe 原本就不支援編碼樣式的作業。 \_ \_ 會產生用於編碼訊息的 WS XML 緩衝區參數，而開發人員必須直接填入不透明的緩衝區。

## <a name="multiple-message-parts-support"></a>多個訊息部分支援

Wsutil.exe 支援一個訊息中的多個訊息部分。 您可以依照下列方式指定多部分訊息：

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:message name="ISimpleService_MutipleParts_InputMessage">
  <wsdl:part name="part1" element="tns:SimpleElement1" />
  <wsdl:part name="part2" element="tns:SimpleElement2" />
 </wsdl:message>
</wsdl:definitions>
```

如果訊息包含多個部分，Wsutil.exe 會為 message 元素產生 [**WS \_ 結構 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_type) 欄位。 如果訊息是以檔樣式表示，Wsutil.exe 會產生具有結構類型的包裝函式元素。 包裝函式元素沒有名稱或特定命名空間，而且包裝函式結構包含所有部分中的所有元素做為欄位。 包裝函式元素僅供內部使用，且不會在訊息本文中序列化。

如果訊息使用 RPC 或常值樣式表示法，Wsutil.exe 會根據 WSDL SOAP 擴充功能規格，以專案名稱和指定的命名空間做為服務命名空間來建立包裝函式元素。 元素的結構包含欄位陣列，這些欄位代表訊息部分中指定的類型。 包裝函式專案會對應至訊息主體中的實際最上層專案，如 SOAP 規格中所示。

在伺服器端，每個作業都會產生產生之伺服器服務作業的 typedef。 這個 typedef 可用來參考函式資料表中的作業（如先前所述）。 每項作業也會產生存根函式，而該函式會將委派 nfrastructure 呼叫給實際方法。

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT* context,
  unsigned int  a,
  unsigned int * b,
  unsigned int * c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error
  );
```

針對 SimpleMethod 作業，會在上面定義 SimpleMethodOperation typedef。 請注意，產生的方法具有展開的引數 listwith SimpleMethod 作業的輸入和輸出訊息的訊息部分，做為具名引數。

在用戶端上，每項作業都會對應至 proxy 服務作業。

``` syntax
HRESULT WINAPI SimpleMethod (
  WS_SERVICE_PROXY* serviceProxy,
  ws_heap *heap,
  unsigned int  a,
  unsigned int * b,
  unsigned int * c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);
```

## <a name="processing-wsdlbinding"></a>處理 wsdl： binding

WWSAPI 服務模型支援 theSOAP 系結延伸模組。 每個系結都有相關聯的 **portType**。

Soap 系結延伸中指定的傳輸只是諮詢。 建立通道時，應用程式必須提供傳輸資訊。 目前我們支援 WS HTTP 系結 \_ \_ 和 ws \_ TCP 系結系結 \_ 。

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:binding name="DefaultBinding_ISimpleService" type="tns:ISimpleService">
  <soap:binding transport="http://schemas.xmlsoap.org/soap/http" />
  <wsdl:operation name="SimpleMethod">
   <soap:operation soapAction="http://Example.org/ISimpleService/SimpleMethod" 
   style="document" />
   <wsdl:input>
    <soap:body use="literal" />
   </wsdl:input>
   <wsdl:output>
    <soap:body use="literal" />
   </wsdl:output>
  </wsdl:operation>
 </wsdl:binding>
</wsdl:definitions>
```

在我們的範例 WSDL 檔案中，我們只有一個適用于 ISimpleService 的 **portType** 。 提供的 SOAP 系結會指出 HTTP 傳輸，這會指定為 WS HTTP 系結 \_ \_ 。 請注意，此結構沒有靜態裝飾，因為此結構必須可供應用程式使用。

處理 wsdl： portType

WSDL 中的每個 **portType** 都是由一或多個作業所組成。 作業應該與 wsdl： binding 中指出的 SOAP 系結延伸模組一致。

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ISimpleService">
  <wsdl:operation name="SimpleMethod">
   ...
  </wsdl:operation>
 </wsdl:portType>
</wsdl:definitions>
```

在此範例中，ISimpleService **portType** 只包含 SimpleMethod 作業。 這與系結區段一致，其中只有一個 WSDL 作業對應至 SOAP 動作。

因為 ISimpleService **portType** 只有一個作業（SimpleMethod），所以對應的函式資料表只會包含 SimpleMethod 即服務作業。

就中繼資料而言，每個 **portType** 都會 Wsutil.exe 到 [**WS \_ 合約 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)來對應。 **PortType** 內的每個作業都會對應至 [**WS \_ 作業 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)。

在此範例中 **，此** 工具會產生 ISimpleService 的 [**WS \_ 合約 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) 。 此合約描述包含 ISimpleService **portType** 上可用的特定作業數目以及 [**WS 作業 \_ \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) 的陣列，代表在 ISimpleService 上針對 portType 定義的個別作業。 由於 ISimpleService 的 ISimpleService portType 上只有一項作業，因此也只有一個 WS 作業 **\_ \_ 描述** 定義。

``` syntax
...  part of LocalDefinitions structure
{    // array of operations for DefaultBinding_ISimpleService
(WS_OPERATION_DESCRIPTION*)&example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.SimpleMethod.SimpleMethod,
},    // array of operations for DefaultBinding_ISimpleService
{    // contract description for DefaultBinding_ISimpleService
1,
(WS_OPERATION_DESCRIPTION**)example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.operations,
WS_HTTP_CHANNEL_BINDING,
},  // end of contract description for DefaultBinding_ISimpleService
},    // DefaultBinding_ISimpleService       ...
```

## <a name="processing-wsdlservice"></a>處理 wsdl：服務

WsUtil.exe 使用服務來尋找系結/porttypes，並產生描述類型、訊息、porttype 定義等的合約結構。 合約描述可從外部存取，而且會產生為透過產生的標頭所指定之全域定義結構的一部分。

WsUtil.exe 支援在 wsdl： port 中定義的 EndpointReference 延伸模組。 端點參考是以 WS-ADDRESSING 定義，做為描述服務 [端點](endpoint-address.md) 資訊的方式。 以 [**ws \_ XML \_ 字串**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)形式儲存的輸入端點參考延伸模組文字連同相符的 [**WS \_ 端點 \_ 位址 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description) ，會在全域結構的 endpointReferences 區段中產生。

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:service name="SimpleService">
  <wsdl:port name="ISimpleService" binding="tns:DefaultBinding_ISimpleService">
   <soap:address location="http://Example.org/ISimpleService" />
   <wsa:EndpointReference>
    <wsa:Address>http://example.org/wcfmetadata/WSHttpNon</wsa:Address>
   </wsa:EndpointReference> 
  </wsdl:port>
 </wsdl:service>
</wsdl:definitions>
```

``` syntax
  const _example_wsdl example_wsdl =
  {
  ... // global element description
  {// messages
  {    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.ISimpleService_SimpleMethod_InputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethod,
},    // message description for ISimpleService_SimpleMethod_InputMessage
{    // message description for ISimpleService_SimpleMethod_OutputMessage
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.ISimpleService_SimpleMethod_OutputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethodResponse,
},    // message description for ISimpleService_SimpleMethod_OutputMessage
}, // messages
{// contracts
{   // DefaultBinding_ISimpleService
1,
(WS_OPERATION_DESCRIPTION**)example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.operations,
WS_HTTP_CHANNEL_BINDING,
},    // end of DefaultBinding_ISimpleService
    }, // contracts
    {
        {
            {   // endpointAddressDescription
                WS_ADDRESSING_VERSION_0_9,
            },                    
            (WS_XML_STRING*)&xml_string_generated_in_stub // endpointReferenceString
        }, //DefaultBinding_ISimpleService
    }, // endpointReferences
}
```

若要使用 WsUtil 產生的中繼資料來建立 [**WS \_ 端點 \_ 位址**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) ：

``` syntax
WsCreateReader      // Create a WS_XML_READER
Initialize a WS_XML_READER_BUFFER_INPUT
WsSetInput          // Set the encoding and input of the reader to generated endpointReferenceString
WsReadType        // Read WS_ENDPOINT_ADDRESS from the reader
    // Using WS_ELEMENT_TYPE_MAPPING, WS_ENDPOINT_ADDRESS_TYPE and generated endpointAddressDescription, 
```

用戶端 proxy 或服務 stub 中的常數位符串會產生為類型為 WS \_ XML \_ 字串的欄位，而且 proxy 或存根檔案中的所有字串都有常數位典。 字典中的每個字串都會以區域結構的字典部分中的欄位形式產生，以提供更好的可讀性。

``` syntax
... // dictionary part of LocalDefinitions structure
{    // xmlStrings
  { // xmlStrings
    WS_XML_STRING_DICTIONARY_VALUE("a",&example_wsdlLocalDefinitions.dictionary.dict, 0), 
    WS_XML_STRING_DICTIONARY_VALUE("http://Sapphire.org",&example_wsdlLocalDefinitions.dictionary.dict, 1), 
    WS_XML_STRING_DICTIONARY_VALUE("b",&example_wsdlLocalDefinitions.dictionary.dict, 2), 
    WS_XML_STRING_DICTIONARY_VALUE("SimpleMethod",&example_wsdlLocalDefinitions.dictionary.dict, 3),
    ...
  },  // end of xmlStrings
  {   // SimpleServicedictionary
    // 45026280-d5dc-4570-8195-4d66d13bfa34
    { 0x45026280, 0xd5dc, 0x4570, { 0x81, 0x95, 0x4d,0x66, 0xd1, 0x3b, 0xfa, 0x34 } },
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings,
    stringCount,
    TRUE,
  },
}
...
```

## <a name="processing-wsdltype"></a>處理 wsdl：類型

Wsutil.exe 僅支援 wsdl： type 規格中的 XML 架構 (XSD) 檔。 其中一個特殊案例是當訊息埠指定全域元素定義時。 請參閱下一節，以取得在這些案例中使用之啟發學習法的詳細資料。

## <a name="parameter-processing-heuristics"></a>參數處理啟發學習法

在服務模型中，WSDL 訊息會對應至方法中的特定參數。 Wsutil.exe 有兩種類型的參數產生：在第一個樣式中，作業的輸入訊息有一個參數，而輸出訊息的一個參數 (必要) ;在第二個樣式中，Wsutil.exe 使用啟發學習法，將輸入訊息和輸出訊息的結構中的欄位對應和展開至作業中的不同參數。 輸入和輸出訊息都必須具有結構類型訊息元素，才能產生第二個方法。

從輸入和輸出訊息產生作業參數時，Wsutil.exe 會使用下列規則：

-   針對具有多個訊息部分的輸入和輸出訊息，每個訊息部分都是作業中的個別參數，並以訊息部分名稱做為參數名稱。
-   針對具有一個訊息部分的 RPC 樣式訊息，訊息部分是作業中的參數，並以訊息部分名稱做為參數名稱。
-   針對檔樣式的輸入和輸出訊息，其中包含一個訊息部分：
    -   如果訊息部分的名稱是「參數」，而專案類型是一個結構，則結構中的每個欄位都會被視為個別的參數，且功能變數名稱為參數名稱。
    -   如果訊息部分名稱不是 "parameters"，則訊息會是作業中的參數，並使用訊息名稱做為對應的參數名稱。
-   若為具有 nillable 元素的檔樣式輸入和輸出訊息，訊息會對應到一個參數，並以訊息部分名稱做為參數名稱。 加入一個額外的間接取值層級，表示指標可以是 **Null**。
-   如果欄位只出現在輸入訊息元素中，則會將此欄位視為 \[ in \] 參數。
-   如果欄位只出現在輸出訊息元素中，則會將此欄位視為 \[ out \] 參數。
-   如果輸入訊息和輸出訊息中有相同名稱和相同類型的欄位，則會將此欄位視為 \[ in、out \] 參數。

下列工具可用來判斷參數的方向：

-   如果欄位只出現在輸入訊息元素中，則會將此欄位視為僅限參數。
-   如果欄位只出現在輸出訊息元素中，則會將此欄位視為僅限輸出參數。
-   如果輸入訊息和輸出訊息中有相同名稱和相同類型的欄位，則會將此欄位視為 in、out 參數。

Wsutil.exe 僅支援已排序的元素。 \[ \] 如果 Wsutil.exe 無法將 in 參數和 out 參數合併為單一參數清單，則會拒絕對 in、out 參數的無效排序。 可能會將尾碼新增至參數名稱，以避免名稱衝突。

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
</wsdl:definitions>
```

Wsutil.exe 將 tns： SimpleMethod 和 tns： SimpleMethodResponse ato 中的欄位視為參數，如以下的參數定義所示：

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:types>
  <xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
  targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
   <xs:import namespace="http://Example.org" />
   <xs:element name="SimpleMethod">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="a" type="xs:unsignedInt" />
      <xs:element name="b" type="xs:unsignedInt" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
   <xs:element name="SimpleMethodResponse">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="b" type="xs:unsignedInt" />
      <xs:element name="c" type="xs:unsignedInt" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
  </xs:schema>
 </wsdl:types>
</wsdl:definitions>
```

Wsutil.exe 會從上列清單中的欄位展開參數清單，並在下列程式碼範例中產生 **ParamStruct** 結構。 服務模型執行時間可以使用此結構，將引數傳遞至用戶端和伺服器 stub。

``` syntax
typedef struct SimpleMethodParamStruct {
  unsigned int   a;  
  unsigned int   b;
  unsigned int   c;
} ;
```

此結構僅用來描述用戶端和伺服器端上的堆疊框架。 訊息描述不會變更，也不會變更訊息描述所參考的元素描述。

``` syntax
  // following are local definitions for the complex type
  { // field description for a
  WS_ELEMENT_FIELD_MAPPING,
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aLocalName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  WS_INT32_TYPE,
  0,
  WsOffsetOf(_SimpleMethod, a),
  0,
  0,
  },    // end of field description for a
  { // field description for b
  WS_ELEMENT_FIELD_MAPPING,
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.bLocalName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  WS_INT32_TYPE,
  0,
  WsOffsetOf(_SimpleMethod, b),
  0,
  0,
  },    // end of field description for b
  {    // fields description for _SimpleMethod
  (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs.a,
  (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs.b,
  },
  {  // structure definition
  sizeof(_SimpleMethod),
  __alignof(_SimpleMethod),
  (WS_FIELD_DESCRIPTION**)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs._SimpleMethodFields,
  WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs._SimpleMethodFields),
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings._SimpleMethodTypeName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  0,
  },   // struct description for _SimpleMethod
  // following are global definitions for the out parameter
  ...
  {  // element description
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings._SimpleMethodTypeName,
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  WS_STRUCT_TYPE,
  (void *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs.structDesc,
  },
  {    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.ISimpleService_SimpleMethod_InputMessageactionName,
(WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethod,
  },    // message description for ISimpleService_SimpleMethod_InputMessage
```

一般來說，會為所有 \[ out \] 和 \[ in、out 參數新增一個間接取值層級 \] 。

## <a name="parameterless-operation"></a>無參數操作

針對檔和常值作業，Wsutil.exe 會將作業視為具有一個輸入參數和一個輸出參數（如果有的話）：

-   輸入或輸出訊息有一個以上的部分。
-   只有一個訊息部分，而訊息部分名稱並非「參數」。

.. 在上述範例中，假設訊息部分的名稱為 *ParamIn*"and *ParamOut*，方法簽章會變成下列程式碼：

``` syntax
typedef struct SimpleMethod{
unsigned int a;
unsigned int b;
};

typedef struct SimpleMethodResponse {
unsigned int b;
unsigned int c;
};

typedef  struct ISimpleService_SimpleMethodParamStruct
{
SimpleMethod  * SimpleMethod;
SimpleMethodResponse  * SimpleMethodResponse;
} ISimpleService_SimpleMethodParamStruct;
```

Wsutil.exe 會產生作業描述的版本簽章，讓 WsCall 和伺服器端服務模型引擎可以檢查產生的描述是否適用于目前的平臺。

此版本資訊會產生為 [**WS \_ 操作 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) 結構的一部分。 版本號碼可以視為聯集 arm 選取器，讓結構成為可擴充的。 目前， **versionID** 是設定 to1，沒有後續的欄位。 未來的 versiosn 可能會遞增版本號碼，並視需要加入更多欄位。 例如，Wsutil.exe 目前根據版本識別碼產生下列程式碼：

``` syntax
{ // SimpleMethod
{ // parameter descriptions for SimpleMethod
{ WS_PARAMETER_TYPE_NORMAL, (USHORT)0, (USHORT)-1 },
{ WS_PARAMETER_TYPE_NORMAL, (USHORT)1, (USHORT)-1 },
{ WS_PARAMETER_TYPE_NORMAL, (USHORT)-1, (USHORT)1 },
},    // parameter descriptions for SimpleMethod
{    // operation description for SimpleMethod
1,
(WS_MESSAGE_DESCRIPTION*)&example_wsdl.messages.ISimpleService_SimpleMethod_InputMessage,
(WS_MESSAGE_DESCRIPTION*)&example_wsdl.messages.ISimpleService_SimpleMethod_OutputMessage,
3,
(WS_PARAMETER_DESCRIPTION*)example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.SimpleMethod.params,
SimpleMethodOperationStub
}, //operation description for SimpleMethod
},  // SimpleMethod
```

未來可將其擴充如下：

``` syntax
WS_OPERATION_DESCRIPTION simpleMethodOperationDesc =
{
  2,
  &ISimpleService_SimpleMethod_InputputMessageDesc,
  &ISimpleService_SimpleMethod_OutputMessageDesc,
  WsCountOf(SimpleMethodParameters),
  SimpleMethodParameters,
  ISimpleService_SimpleMethod_Stub,
  &forwardToString;   // just as an example.
};
```

## <a name="security"></a>安全性

請參閱 [Wsutil 編譯器工具](wsutil-compiler-tool.md) 主題中的安全性一節。

 

 




