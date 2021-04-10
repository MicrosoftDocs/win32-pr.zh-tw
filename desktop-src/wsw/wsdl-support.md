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
ms.openlocfilehash: 19661e487c1a0dde871333376336bede239f9825
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103684242"
---
# <a name="wsdl-and-service-contracts"></a><span data-ttu-id="ab769-106">WSDL 和服務合約</span><span class="sxs-lookup"><span data-stu-id="ab769-106">WSDL and Service Contracts</span></span>

<span data-ttu-id="ab769-107">[Wsutil.exe](web-service-compiler-tool.md)公用程式會根據提供的 WSDL 中繼資料來產生 C 語言存根，以及使用者撰寫之 XML 架構所描述之資料類型的資料類型定義和描述。</span><span class="sxs-lookup"><span data-stu-id="ab769-107">The [Wsutil.exe](web-service-compiler-tool.md) utility generates a C language stub according to supplied WSDL metadata, as well as data type definitions and descriptions for data types described by user-authored XML schemas.</span></span>


<span data-ttu-id="ab769-108">以下是範例 WSDL 檔案和 XML 架構，作為後續討論的基礎：</span><span class="sxs-lookup"><span data-stu-id="ab769-108">The following is an example WSDL document and XML schema that serves as a basis for the discussion that follows:</span></span>

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

<span data-ttu-id="ab769-109">這個範例會提供合約 ISimpleService，具有單一方法 SimpleMethod。</span><span class="sxs-lookup"><span data-stu-id="ab769-109">This example provides a contract, ISimpleService, with a single method, SimpleMethod.</span></span> <span data-ttu-id="ab769-110">「SimpleMethod」有兩個類型為 **integer**、 *a* 和 *b* 的輸入參數，會從用戶端傳送至服務。</span><span class="sxs-lookup"><span data-stu-id="ab769-110">"SimpleMethod" has two input parameters of type **integer**, *a* and *b*, that are sent from the client to the service.</span></span> <span data-ttu-id="ab769-111">同樣地，SimpleMethod 有兩個類型為 **integer**、 *b* 和 *c* 的輸出參數，會在成功完成之後傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="ab769-111">Likewise, SimpleMethod has two output parameters of type **integer**, *b* and *c*, which are returned to the client after successful completion.</span></span> <span data-ttu-id="ab769-112">在 SAL 批註的 C 語法中，方法定義顯示如下：</span><span class="sxs-lookup"><span data-stu-id="ab769-112">In SAL-annotated C syntax, the method definition appears as follows:</span></span>

``` syntax
void SimpleMethod(__in int a, __inout int *  b, __out int * c );
```

<span data-ttu-id="ab769-113">在此定義中，ISimpleService 是具有單一服務作業的服務合約： SimpleMethod。</span><span class="sxs-lookup"><span data-stu-id="ab769-113">In this definition, ISimpleService is a service contract with a single service operation: SimpleMethod.</span></span>

<span data-ttu-id="ab769-114">輸出標頭檔包含外部參考的定義和描述。</span><span class="sxs-lookup"><span data-stu-id="ab769-114">The output header file contains definitions and descriptions for external reference.</span></span> <span data-ttu-id="ab769-115">這包括：</span><span class="sxs-lookup"><span data-stu-id="ab769-115">This includes:</span></span>

-   <span data-ttu-id="ab769-116">全域元素類型的 C 結構定義。</span><span class="sxs-lookup"><span data-stu-id="ab769-116">C structure definitions for global element types.</span></span>
-   <span data-ttu-id="ab769-117">目前檔案中定義的作業原型。</span><span class="sxs-lookup"><span data-stu-id="ab769-117">An operation prototype as defined in current file.</span></span>
-   <span data-ttu-id="ab769-118">WSDL 檔案中指定之合約的函數資料表原型。</span><span class="sxs-lookup"><span data-stu-id="ab769-118">A function table prototype for the contracts specified in the WSDL file.</span></span>
-   <span data-ttu-id="ab769-119">目前檔案中指定之所有函式的用戶端 proxy 和服務存根原型。</span><span class="sxs-lookup"><span data-stu-id="ab769-119">Client proxy and service stub prototypes for all the functions specified in current file.</span></span>
-   <span data-ttu-id="ab769-120">目前檔案中定義之全域架構元素的 [**WS \_ 元素 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) 資料結構。</span><span class="sxs-lookup"><span data-stu-id="ab769-120">A [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) data structure for the global schema elements defined in current file.</span></span>
-   <span data-ttu-id="ab769-121">目前檔案中指定之所有訊息的 [**WS \_ 訊息 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) 資料結構。</span><span class="sxs-lookup"><span data-stu-id="ab769-121">A [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) data structure for all the messages specified in current file.</span></span>
-   <span data-ttu-id="ab769-122">目前檔案中指定之所有合約的 [**WS \_ 合約 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) 資料結構。</span><span class="sxs-lookup"><span data-stu-id="ab769-122">A [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) data structure for all the contracts specified in current file.</span></span>

<span data-ttu-id="ab769-123">產生一個全域結構來封裝架構類型的所有全域描述，以及應用程式可以參考的服務模型類型。</span><span class="sxs-lookup"><span data-stu-id="ab769-123">One global structure is generated to encapsulate all the global descriptions for the schema types and service model types to which the application can refer.</span></span> <span data-ttu-id="ab769-124">結構是使用正規化的檔案名來命名。</span><span class="sxs-lookup"><span data-stu-id="ab769-124">The structure is named using a normalized file name.</span></span> <span data-ttu-id="ab769-125">在此範例中，Wsutil.exe 會產生名為「範例 wsdl」的全域定義結構 \_ ，其中包含所有 web 服務描述。</span><span class="sxs-lookup"><span data-stu-id="ab769-125">In this example, Wsutil.exe generates a global definitions structure named "example\_wsdl" that contains all the web service descriptions.</span></span> <span data-ttu-id="ab769-126">結構定義是在存根檔案中產生的。</span><span class="sxs-lookup"><span data-stu-id="ab769-126">The structure definition is generated in the stub file.</span></span>

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

<span data-ttu-id="ab769-127">針對 XML 架構檔中的全域元素定義 (XSD) ，會針對每個專案產生一個 [**WS \_ 元素 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) 原型，以及對應的 C 類型定義。</span><span class="sxs-lookup"><span data-stu-id="ab769-127">For global element definitions in the XML schema document (XSD), one [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) prototype, as well as the corresponding C type definition, are generated for each of the elements.</span></span> <span data-ttu-id="ab769-128">SimpleMethod 和 SimpleMethodResponse 之元素描述的原型會以上述結構中的成員來產生。</span><span class="sxs-lookup"><span data-stu-id="ab769-128">The prototypes for the element descriptions for SimpleMethod and SimpleMethodResponse are generated as members in the structure above.</span></span> <span data-ttu-id="ab769-129">C 結構的產生方式如下：</span><span class="sxs-lookup"><span data-stu-id="ab769-129">The C structures are generated as follows:</span></span>

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

<span data-ttu-id="ab769-130">類似于全域複雜型別，Wsutil.exe 會產生類似上述的類型 C 結構定義，而不會有相符的元素描述。</span><span class="sxs-lookup"><span data-stu-id="ab769-130">Similarly for global complex types, Wsutil.exe generates type C structure definitions like above, without matching element descriptions.</span></span>

<span data-ttu-id="ab769-131">針對 WSDL 輸入，Wsutil.exe 會產生下列原型和定義：</span><span class="sxs-lookup"><span data-stu-id="ab769-131">For WSDL input, Wsutil.exe generates the following prototypes and definitions:</span></span>

-   <span data-ttu-id="ab769-132">訊息描述會產生 [**WS \_ 訊息 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) 原型。</span><span class="sxs-lookup"><span data-stu-id="ab769-132">A [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) prototype is generated for the message description.</span></span> <span data-ttu-id="ab769-133">這項描述可供服務模型以及訊息層使用。</span><span class="sxs-lookup"><span data-stu-id="ab769-133">This description can be used by the service model as well as the message layer.</span></span> <span data-ttu-id="ab769-134">訊息描述結構是全域結構中名稱為 "messagename" 的欄位。</span><span class="sxs-lookup"><span data-stu-id="ab769-134">Message description structures are fields named "messagename" in the global structure.</span></span> <span data-ttu-id="ab769-135">在此範例中，訊息描述會產生為 \_ \_ ISimpleService SimpleMethod InputMessage 結構中的 ISimpleService SimpleMethod InputMessage 欄位 \_ \_ （如同 WSDL 檔案中所指定）。</span><span class="sxs-lookup"><span data-stu-id="ab769-135">In this example, the message description is generated as the ISimpleService\_SimpleMethod\_InputMessage field in the ISimpleService\_SimpleMethod\_InputMessage structure as specified in the WSDL file.</span></span>
-   <span data-ttu-id="ab769-136">[**WS \_合約 \_ 描述原型是**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) 針對合約描述產生的。</span><span class="sxs-lookup"><span data-stu-id="ab769-136">[**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) prototype is generated for the contract description.</span></span> <span data-ttu-id="ab769-137">服務模型會使用此描述。</span><span class="sxs-lookup"><span data-stu-id="ab769-137">This description is used by service model.</span></span> <span data-ttu-id="ab769-138">合約描述結構是全域結構中名稱為 "contractname" 的欄位。</span><span class="sxs-lookup"><span data-stu-id="ab769-138">Contract description structures are fields named "contractname" in the global structure.</span></span> <span data-ttu-id="ab769-139">在此範例中，合約描述會以「 \_ 範例 wsdl」結構中的 Binder.defaultbinding ISimpleService 欄位形式產生 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="ab769-139">In this example, the contract description is generated as the DefaultBinding\_ISimpleService field in the structure "\_example\_wsdl".</span></span>

<span data-ttu-id="ab769-140">作業和類型規格通用於 proxy 和存根，兩者都是在這兩個檔案中產生的。</span><span class="sxs-lookup"><span data-stu-id="ab769-140">Operation and type specifications are common to both proxy and stub and they are generated in both files.</span></span> <span data-ttu-id="ab769-141">只有當相同檔案中同時產生 proxy 和存根時，Wsutil.exe 才會產生一個複本。</span><span class="sxs-lookup"><span data-stu-id="ab769-141">Wsutil.exe generates one copy only if both the proxy and stub are generated in the same file.</span></span>

## <a name="identifier-generation"></a><span data-ttu-id="ab769-142">識別碼產生</span><span class="sxs-lookup"><span data-stu-id="ab769-142">Identifier generation</span></span>

<span data-ttu-id="ab769-143">上面所列的自動產生 C 結構會根據 WSDL 檔案中指定的名稱建立。</span><span class="sxs-lookup"><span data-stu-id="ab769-143">The autogenerated C structures listed above are created based on the name specified in WSDL file.</span></span> <span data-ttu-id="ab769-144">XML NCName 通常不會被視為有效的 C 識別碼，並且會視需要將名稱正規化。</span><span class="sxs-lookup"><span data-stu-id="ab769-144">An XML NCName is not commonly considered a valid C identifier, and the names are normalized as needed.</span></span> <span data-ttu-id="ab769-145">十六進位值不會轉換，而且像是 '： '、'/' 和 '. ' 的一般字母都會轉換成底線 ' \_ ' 字元，以改善可讀性。</span><span class="sxs-lookup"><span data-stu-id="ab769-145">Hex values are not converted, and common letters like ':', '/' and '.' are converted to the underscore '\_' character to improve readability.</span></span>

## <a name="header-for-the-stub"></a><span data-ttu-id="ab769-146">存根的標頭</span><span class="sxs-lookup"><span data-stu-id="ab769-146">Header for the stub</span></span>

<span data-ttu-id="ab769-147">服務合約中的每個作業都會產生一個名為 " <operationname> callback" 的回呼常式。</span><span class="sxs-lookup"><span data-stu-id="ab769-147">For each operation in the service contract, one callback routine named "<operationname>Callback" is generated.</span></span> <span data-ttu-id="ab769-148"> (例如，範例服務合約中的「SimpleMethod」作業會有一個名為 "SimpleMethodCallback" 的回撥。 ) </span><span class="sxs-lookup"><span data-stu-id="ab769-148">(For example, the operation "SimpleMethod" in the example service contract has a generated callback named "SimpleMethodCallback".)</span></span>

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT * context,
  int a, int *b, int *c,
  const WS_ASYNC_CONTEXT *asyncContext,
  WS_ERROR * error);
```

<span data-ttu-id="ab769-149">針對每個 WSDL **portType** Wsutil.exe 會產生代表 **portType** 的函式資料表。</span><span class="sxs-lookup"><span data-stu-id="ab769-149">For each WSDL **portType** Wsutil.exe generates a function table representing **portType**.</span></span> <span data-ttu-id="ab769-150">**PortType** 上的每個作業都有對應的函式指標，可指向函式資料表中存在的回呼。</span><span class="sxs-lookup"><span data-stu-id="ab769-150">Each operation on the **portType** has a corresponding function pointer to the callback present in the function table.</span></span>

``` syntax
struct ISimpleServiceMethodTable
{
  ISimpleService_SimpleMethodCallback SimpleMethod;
};
```

<span data-ttu-id="ab769-151">所有作業都會產生 Proxy 原型。</span><span class="sxs-lookup"><span data-stu-id="ab769-151">Proxy prototypes are generated for all operations.</span></span> <span data-ttu-id="ab769-152">原型名稱是在此案例中 (的作業名稱，) 在服務合約的 WSDL 檔案中指定 "SimpleMethod"。</span><span class="sxs-lookup"><span data-stu-id="ab769-152">The prototype name is the operation name (in this case, "SimpleMethod") specified in WSDL file for the service contract.</span></span>

``` syntax
HRESULT WINAPI SimpleMethod(WS_CHANNEL *channel,
  WS_HEAP *heap,
  int a,
  int *b,
  int *c,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR * error );
```

## <a name="local-only-description-prototype-generation"></a><span data-ttu-id="ab769-153">僅限本機描述原型產生</span><span class="sxs-lookup"><span data-stu-id="ab769-153">Local-only Description Prototype Generation</span></span>

<span data-ttu-id="ab769-154">Proxy andstub 檔包含全域定義結構的定義，包括包含僅限本機描述和用戶端 proxy/服務存根執行之結構的原型和定義。</span><span class="sxs-lookup"><span data-stu-id="ab769-154">The proxy andstub files contain the definition for the global definitions structure, including prototypes and definitions for the structures containing local-only descriptions and client proxy/service stub implementations.</span></span>

<span data-ttu-id="ab769-155">存根檔案的本機所有原型和定義都會產生成封裝結構的一部分。</span><span class="sxs-lookup"><span data-stu-id="ab769-155">All prototypes and definitions that are local to the stub file are generated as part of an encapsulating structure.</span></span> <span data-ttu-id="ab769-156">這個整體的本機描述結構提供了序列化層和服務模型所需之描述的清楚階層。</span><span class="sxs-lookup"><span data-stu-id="ab769-156">This overarching local description structure provides a clear hierarchy of the descriptions required by the serialization layer and the service model.</span></span> <span data-ttu-id="ab769-157">本機描述結構的原型類似如下所示：</span><span class="sxs-lookup"><span data-stu-id="ab769-157">The local description structure has prototypes similar to the one shown below:</span></span>

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

## <a name="referencing-definitions-from-other-files"></a><span data-ttu-id="ab769-158">參考其他檔案的定義</span><span class="sxs-lookup"><span data-stu-id="ab769-158">Referencing definitions from other files</span></span>

<span data-ttu-id="ab769-159">本機定義可以參考另一個檔案中產生的描述。</span><span class="sxs-lookup"><span data-stu-id="ab769-159">Local definitions can reference descriptions generated in another file.</span></span> <span data-ttu-id="ab769-160">例如，訊息可能會定義在從 WSDL 檔案產生的 C 程式碼檔案中，但可以在 XSD 檔案所產生的 C 程式碼檔案中的其他地方定義 message 元素。</span><span class="sxs-lookup"><span data-stu-id="ab769-160">For example, the message may be defined in the C code file generated from the WSDL file but the message element may be defined elsewhere in the C code file generated from the XSD file.</span></span> <span data-ttu-id="ab769-161">在此情況下，Wsutil.exe 會從包含訊息定義的檔案產生全域元素的參考，如下所示：</span><span class="sxs-lookup"><span data-stu-id="ab769-161">In this case, Wsutil.exe generates reference to the global element from the file that contains the message definition, as demonstrated below:</span></span>

``` syntax
{  // WS_MESSAGE_DESCRIPTION
...
(WS_ELEMENT_DESRIPTION *)b_xsd.globalElement.<elementname>
  };
```

## <a name="global-element-descriptions"></a><span data-ttu-id="ab769-162">全域元素描述</span><span class="sxs-lookup"><span data-stu-id="ab769-162">Global element descriptions</span></span>

<span data-ttu-id="ab769-163">針對 wsdl： type 或 XSD 檔中定義的每個全域元素， **GlobalElement** 欄位內都有一個名為 **elementName** 的相符欄位。</span><span class="sxs-lookup"><span data-stu-id="ab769-163">For each global element defined in a wsdl:type or XSD file, there is a matching field named **elementName** inside the **GlobalElement** field.</span></span> <span data-ttu-id="ab769-164">在此範例中，會產生名為 SimpleMethod 的結構：</span><span class="sxs-lookup"><span data-stu-id="ab769-164">In this example, a structure named SimpleMethod is generated:</span></span>

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

<span data-ttu-id="ab769-165">元素描述所需的其他描述會產生為包含結構的一部分。</span><span class="sxs-lookup"><span data-stu-id="ab769-165">Other descriptions required by the element description are generated as part of the containing structure.</span></span> <span data-ttu-id="ab769-166">如果元素是簡單類型專案，則只有一個 [**WS \_ 元素 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) 欄位。</span><span class="sxs-lookup"><span data-stu-id="ab769-166">If the element is a simple type element, there is only one [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) field.</span></span> <span data-ttu-id="ab769-167">如果元素類型是結構，則所有相關的欄位和結構描述都會產生為元素結構的一部分。</span><span class="sxs-lookup"><span data-stu-id="ab769-167">If the element type is a structure, all of the related fields and structure descriptions are generated as part of the element structure.</span></span> <span data-ttu-id="ab769-168">在此範例中，SimpleMethod 元素是包含兩個欄位 **a** 和 **b** 的結構。</span><span class="sxs-lookup"><span data-stu-id="ab769-168">In this example, SimpleMethod element is a structure containing two fields, **a** and **b**.</span></span> <span data-ttu-id="ab769-169">Wsutil.exe 會產生結構，如下所示：</span><span class="sxs-lookup"><span data-stu-id="ab769-169">Wsutil.exe generates the structure as follows:</span></span>

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

<span data-ttu-id="ab769-170">內嵌結構和內嵌元素會視需要產生為子結構。</span><span class="sxs-lookup"><span data-stu-id="ab769-170">Embedded structures and embedded elements are generated as sub-structures as needed.</span></span>

## <a name="wsdl-related-definitions"></a><span data-ttu-id="ab769-171">WSDL 相關定義</span><span class="sxs-lookup"><span data-stu-id="ab769-171">WSDL related definitions</span></span>

<span data-ttu-id="ab769-172">Wsutil.exe 會針對指定的 wsdl：服務下定義的每個 **portType** 值，在 WSDL 區段下產生欄位。</span><span class="sxs-lookup"><span data-stu-id="ab769-172">Wsutil.exe generates a field under WSDL section for each of the **portType** values defined under the specified wsdl:service.</span></span>

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

<span data-ttu-id="ab769-173">Wsutil.exe 會產生一個 f 欄位，其中包含作業所需的所有描述、每個方法的每個作業描述的指標單一陣列，以及指定之 **portType** 的一個 [**WS \_ 合約 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)。</span><span class="sxs-lookup"><span data-stu-id="ab769-173">Wsutil.exe generates one field f that contains all the descriptions needed for the operation, a signle array of pointers to each of the operation descriptions for each method, and one [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) for the specified **portType**.</span></span>

<span data-ttu-id="ab769-174">作業所需的所有描述都會在指定的 **portType** 下的 **operationName** 欄位內產生。</span><span class="sxs-lookup"><span data-stu-id="ab769-174">All the descriptions needed by operations are generated inside the **operationName** field under the specified **portType**.</span></span> <span data-ttu-id="ab769-175">這些包括 [**WS \_ 元素 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) 欄位，以及輸入和輸出參數 s 的子結構。</span><span class="sxs-lookup"><span data-stu-id="ab769-175">These include the [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) field as well as the sub-structure for input and output parameter s.</span></span> <span data-ttu-id="ab769-176">同樣地，輸入訊息和選擇性輸出訊息的 [**WS \_ 訊息 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) 欄位也會與一起包含： [**WS \_作業 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description) 本身的所有作業參數和 [**WS \_ 操作 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) 欄位的參數描述清單欄位。</span><span class="sxs-lookup"><span data-stu-id="ab769-176">Likewise, the [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) fields for the input message and the optional output message are included along with the; [**WS\_PARAMETER\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description) list field for all of the operation parameters and the [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) field for the operation itself.</span></span> <span data-ttu-id="ab769-177">在此範例中，會產生 SimpleMethod 描述的程式碼結構，如下所示：</span><span class="sxs-lookup"><span data-stu-id="ab769-177">In this example, the code structure for the SimpleMethod description is generated as seen below:</span></span>

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

## <a name="xml-dictionary-related-definitions"></a><span data-ttu-id="ab769-178">XML 字典相關定義</span><span class="sxs-lookup"><span data-stu-id="ab769-178">XML dictionary related definitions</span></span>

<span data-ttu-id="ab769-179">在各種描述中使用的名稱和命名空間會產生為類型為 [**WS \_ XML \_ 字串**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)的欄位。</span><span class="sxs-lookup"><span data-stu-id="ab769-179">Names and namespaces used in various descriptions are generated as fields of type [**WS\_XML\_STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string).</span></span> <span data-ttu-id="ab769-180">所有這些字串都會產生為每個檔案常數位典的一部分。</span><span class="sxs-lookup"><span data-stu-id="ab769-180">All of these strings are generated as part a per-file constant dictionary.</span></span> <span data-ttu-id="ab769-181">下列範例中 (名為 **dict** 的字串清單和 [**WS \_ XML \_ 字典**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary)欄位) 會產生為 **fileNameLocal** 結構的 DICTIONARY 欄位的一部分。</span><span class="sxs-lookup"><span data-stu-id="ab769-181">The list of strings and the [**WS\_XML\_DICTIONARY**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary) field (named **dict** in the example below) are generated as part of the dictionary field of the **fileNameLocal** structure.</span></span>

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

<span data-ttu-id="ab769-182">[**Ws \_ xml \_ 字串**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)的陣列會產生為類型為 **ws \_ xml \_ 字串** 的一數列欄位，並以使用者易記名稱命名。</span><span class="sxs-lookup"><span data-stu-id="ab769-182">The array of [**WS\_XML\_STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)s are generated as a series of fields of type **WS\_XML\_STRING**, named with with user-friendly names.</span></span> <span data-ttu-id="ab769-183">產生的存根會在各種描述中使用易記的名稱，以提供更好的可讀性。</span><span class="sxs-lookup"><span data-stu-id="ab769-183">The generated stub uses the user-friendly names in various descriptions for better readability.</span></span>

<span data-ttu-id="ab769-184">適用于 WSDL 作業的用戶端 proxy</span><span class="sxs-lookup"><span data-stu-id="ab769-184">Client proxy for WSDL operations</span></span>

<span data-ttu-id="ab769-185">Wsutil.exe 會針對所有作業產生用戶端 proxy。</span><span class="sxs-lookup"><span data-stu-id="ab769-185">Wsutil.exe generates a client proxy for all of the operations.</span></span> <span data-ttu-id="ab769-186">應用程式可以使用前置詞命令列選項來覆寫方法簽章。</span><span class="sxs-lookup"><span data-stu-id="ab769-186">Applications can overwrite the method signature using a prefix command-line option.</span></span>

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

<span data-ttu-id="ab769-187">作業呼叫端必須傳入有效的 *堆積* 參數。</span><span class="sxs-lookup"><span data-stu-id="ab769-187">The operation caller must pass in a valid *heap* parameter.</span></span> <span data-ttu-id="ab769-188">輸出參數會使用 \_ *堆積* 參數中指定的 WS 堆積值進行配置。</span><span class="sxs-lookup"><span data-stu-id="ab769-188">Output parameters are allocated using the WS\_HEAP value specified in the *heap* parameter.</span></span> <span data-ttu-id="ab769-189">呼叫的函式可以重設或釋放堆積，以釋放所有輸出參數的記憶體。</span><span class="sxs-lookup"><span data-stu-id="ab769-189">The calling function can reset or free the heap to release memory for all of the output parameters.</span></span> <span data-ttu-id="ab769-190">如果作業失敗，則可以從選擇性的錯誤物件中取出其他詳細資訊（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="ab769-190">If the operation fails, additional detail error information can be retrieved from the optional error object if it is available.</span></span>

<span data-ttu-id="ab769-191">Wsutil.exe 會針對系結中所述的所有作業產生服務存根。</span><span class="sxs-lookup"><span data-stu-id="ab769-191">Wsutil.exe generates a service stub for all of the operations described in binding.</span></span>

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

<span data-ttu-id="ab769-192">上一節描述本機結構的原型，其中包含僅限存根檔案本機的所有定義。</span><span class="sxs-lookup"><span data-stu-id="ab769-192">The above section describes the prototype of the local structure containing all of the definitions local to the stub file only.</span></span> <span data-ttu-id="ab769-193">後續各節將說明描述的定義。</span><span class="sxs-lookup"><span data-stu-id="ab769-193">Subsequent sections describe the definitions of the descriptions.</span></span>

## <a name="wsdl-definition-generation"></a><span data-ttu-id="ab769-194">WSDL 定義產生</span><span class="sxs-lookup"><span data-stu-id="ab769-194">WSDL Definition Generation</span></span>

<span data-ttu-id="ab769-195">Wsutil.exe 會產生一個常數靜態 (**const 靜態**) 結構，名為 *<檔案名 \_*>local，其中包含所有僅限本機定義的<*服務 \_ 名稱*>。</span><span class="sxs-lookup"><span data-stu-id="ab769-195">Wsutil.exe generates a constant static (**const static**) structure named *<file\_name>* LocalDefinitions of type *<service\_name>* Local that contains all the local only definitions.</span></span>

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

<span data-ttu-id="ab769-196">以下是支援的 WSDL 描述：</span><span class="sxs-lookup"><span data-stu-id="ab769-196">The following WSDL descriptions are supported:</span></span>

-   <span data-ttu-id="ab769-197">wsdl：服務</span><span class="sxs-lookup"><span data-stu-id="ab769-197">wsdl:service</span></span>
-   <span data-ttu-id="ab769-198">wsdl： binding</span><span class="sxs-lookup"><span data-stu-id="ab769-198">wsdl:binding</span></span>
-   <span data-ttu-id="ab769-199">wsdl： portType</span><span class="sxs-lookup"><span data-stu-id="ab769-199">wsdl:portType</span></span>
-   <span data-ttu-id="ab769-200">wsdl： operation</span><span class="sxs-lookup"><span data-stu-id="ab769-200">wsdl:operation</span></span>
-   <span data-ttu-id="ab769-201">wsdl： message</span><span class="sxs-lookup"><span data-stu-id="ab769-201">wsdl:message</span></span>

## <a name="processing-wsdloperation-and-wsdlmessage"></a><span data-ttu-id="ab769-202">處理 wsdl： operation 和 wsdl： message</span><span class="sxs-lookup"><span data-stu-id="ab769-202">Processing wsdl:operation and wsdl:message</span></span>

<span data-ttu-id="ab769-203">在 WSDL 檔案中指定的每個作業都會 [Wsutil.exe](web-service-compiler-tool.md)對應至服務作業。</span><span class="sxs-lookup"><span data-stu-id="ab769-203">Each operation specified in the WSDL document is mapped to a service operation by [Wsutil.exe](web-service-compiler-tool.md).</span></span> <span data-ttu-id="ab769-204">此工具會為伺服器和用戶端產生個別的服務作業定義。</span><span class="sxs-lookup"><span data-stu-id="ab769-204">The tool generates separate definitions of the service operations for both the server and the client.</span></span>

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

<span data-ttu-id="ab769-205">此工具會評估輸入 andoutput 訊息資料項目的版面配置，以產生基礎結構的序列化中繼資料，以及與輸入和輸出訊息相關聯之結果服務作業的實際簽章。</span><span class="sxs-lookup"><span data-stu-id="ab769-205">The layout of the input andoutput message data elements is evaluated by the tool to generate the serialization metadata for the infrastructure along with the actual signature of the resulting service operation to which the input and output messages are associated.</span></span>

<span data-ttu-id="ab769-206">特定 **portType** 內每項作業的中繼資料都具有輸入和選擇性的輸出訊息，而每個訊息都會對應到 [**WS \_ 訊息 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description)。</span><span class="sxs-lookup"><span data-stu-id="ab769-206">The metadata for each operation within a specific **portType** has input and optionally an output message, each of these messages is mapped to a [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description).</span></span> <span data-ttu-id="ab769-207">在此範例中，會將 portType 中作業的輸入和輸出訊息對應至 inputMessageDescription，並選擇性地對應至 [**WS 作業 \_ \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) 上的 outputMessageDescription。</span><span class="sxs-lookup"><span data-stu-id="ab769-207">In this example, the input and the output message on the operation in the portType mapped to inputMessageDescription and optionally the outputMessageDescription on the [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) respectively.</span></span>

<span data-ttu-id="ab769-208">此工具會針對每個 WSDL 訊息產生參考 [**ws \_ 元素 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)定義的 [**ws \_ 訊息 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description)，如下所示：</span><span class="sxs-lookup"><span data-stu-id="ab769-208">For each WSDL message the tool generates [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) that references the [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) definition, as demonstrated below:</span></span>

``` syntax
... 
{    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

<span data-ttu-id="ab769-209">訊息描述會參考輸入元素描述。</span><span class="sxs-lookup"><span data-stu-id="ab769-209">The message description refers to the input element description.</span></span> <span data-ttu-id="ab769-210">因為元素是全域定義的，所以訊息描述會參考全域定義，而不是本機靜態元素。</span><span class="sxs-lookup"><span data-stu-id="ab769-210">Because the element is globally defined, the message description references the global definition instead of the local static element.</span></span> <span data-ttu-id="ab769-211">同樣地，如果元素定義在另一個檔案中，Wsutil.exe 會在該檔案中產生全域定義結構的參考。</span><span class="sxs-lookup"><span data-stu-id="ab769-211">Similarly, if the element is defined in another file, Wsutil.exe generates a reference to the globally-defined structure in that file.</span></span> <span data-ttu-id="ab769-212">例如，如果 SimpleMethodResponse 定義在另一個範例 .xsd 檔中，Wsutil.exe 會改為產生下列內容：</span><span class="sxs-lookup"><span data-stu-id="ab769-212">For example, if SimpleMethodResponse is defined in another example.xsd file, Wsutil.exe generates the following instead:</span></span>

``` syntax
...
{    // message description for ISimpleService_SimpleMethod_InputMessage
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
(WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_xsd.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

<span data-ttu-id="ab769-213">每個訊息描述都會包含動作和特定的專案描述， (所有訊息資料元素之類型 [**WS \_ 元素 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)) 的欄位。</span><span class="sxs-lookup"><span data-stu-id="ab769-213">Each message description contains the action and the specific element description (a field of type [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)) for all the message data elements.</span></span> <span data-ttu-id="ab769-214">如果是 RPC 樣式的訊息或具有多個部分的訊息，則會建立包裝函式專案來封裝額外的資訊。</span><span class="sxs-lookup"><span data-stu-id="ab769-214">In the case of an RPC-style message or a message with multiple parts, a wrapper element is created to encapsulate the additional information.</span></span>

## <a name="rpc-style-support"></a><span data-ttu-id="ab769-215">RPC 樣式支援</span><span class="sxs-lookup"><span data-stu-id="ab769-215">RPC style support</span></span>

<span data-ttu-id="ab769-216">Wsutil.exe 根據適用于 SOAP 1.2 規格的 WSDL 1.1 系結延伸模組，支援檔樣式和 RPC 樣式的作業。</span><span class="sxs-lookup"><span data-stu-id="ab769-216">Wsutil.exe supports document-style as well as RPC-style operations according to the WSDL 1.1 Binding Extension for SOAP 1.2 specification.</span></span> <span data-ttu-id="ab769-217">RPC 和常值樣式的作業會標示為 WS \_ RPC \_ 常值 \_ 運算。</span><span class="sxs-lookup"><span data-stu-id="ab769-217">RPC- and literal-style operations are marked as WS\_RPC\_LITERAL\_OPERATION.</span></span> <span data-ttu-id="ab769-218">服務模型會忽略 RPC/常值作業中回應主體包裝函式專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="ab769-218">The service model ignores the name for the response body wrapper element in RPC/literal operations.</span></span>

<span data-ttu-id="ab769-219">Wsutil.exe 原本就不支援編碼樣式的作業。</span><span class="sxs-lookup"><span data-stu-id="ab769-219">Wsutil.exe does not natively support encoding-style operations.</span></span> <span data-ttu-id="ab769-220">\_ \_ 會產生用於編碼訊息的 WS XML 緩衝區參數，而開發人員必須直接填入不透明的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ab769-220">The WS\_XML\_BUFFER parameter is generated for encoding messages, and developers must populate the opaque buffer directly.</span></span>

## <a name="multiple-message-parts-support"></a><span data-ttu-id="ab769-221">多個訊息部分支援</span><span class="sxs-lookup"><span data-stu-id="ab769-221">Multiple message parts support</span></span>

<span data-ttu-id="ab769-222">Wsutil.exe 支援一個訊息中的多個訊息部分。</span><span class="sxs-lookup"><span data-stu-id="ab769-222">Wsutil.exe supports multiple message parts in one message.</span></span> <span data-ttu-id="ab769-223">您可以依照下列方式指定多部分訊息：</span><span class="sxs-lookup"><span data-stu-id="ab769-223">A multi-part message can be specified as follows:</span></span>

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

<span data-ttu-id="ab769-224">如果訊息包含多個部分，Wsutil.exe 會為 message 元素產生 [**WS \_ 結構 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_type) 欄位。</span><span class="sxs-lookup"><span data-stu-id="ab769-224">Wsutil.exe generates a [**WS\_STRUCT\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type) field for the message element if the message contains multiple parts.</span></span> <span data-ttu-id="ab769-225">如果訊息是以檔樣式表示，Wsutil.exe 會產生具有結構類型的包裝函式元素。</span><span class="sxs-lookup"><span data-stu-id="ab769-225">If the message is represented using the document style, Wsutil.exe generates a wrapper element with struct type.</span></span> <span data-ttu-id="ab769-226">包裝函式元素沒有名稱或特定命名空間，而且包裝函式結構包含所有部分中的所有元素做為欄位。</span><span class="sxs-lookup"><span data-stu-id="ab769-226">The wrapper element does not have a name or a specific namespace, and the wrapper structure contains all of the elements in all of the parts as fields.</span></span> <span data-ttu-id="ab769-227">包裝函式元素僅供內部使用，且不會在訊息本文中序列化。</span><span class="sxs-lookup"><span data-stu-id="ab769-227">The wrapper element is for internal use only and it will not be serialized in the message body.</span></span>

<span data-ttu-id="ab769-228">如果訊息使用 RPC 或常值樣式表示法，Wsutil.exe 會根據 WSDL SOAP 擴充功能規格，以專案名稱和指定的命名空間做為服務命名空間來建立包裝函式元素。</span><span class="sxs-lookup"><span data-stu-id="ab769-228">If the message is using RPC or literal style representation , Wsutil.exe creates a wrapper element with the operation name as the element name and the specified namespace as service namespace according to WSDL SOAP extension specification.</span></span> <span data-ttu-id="ab769-229">元素的結構包含欄位陣列，這些欄位代表訊息部分中指定的類型。</span><span class="sxs-lookup"><span data-stu-id="ab769-229">The structure of the element contains an array of fields representing the types specified in the message parts.</span></span> <span data-ttu-id="ab769-230">包裝函式專案會對應至訊息主體中的實際最上層專案，如 SOAP 規格中所示。</span><span class="sxs-lookup"><span data-stu-id="ab769-230">The wrapper element is mapped to the actual top element in message body as indicated in the SOAP specification.</span></span>

<span data-ttu-id="ab769-231">在伺服器端，每個作業都會產生產生之伺服器服務作業的 typedef。</span><span class="sxs-lookup"><span data-stu-id="ab769-231">On the server side, each operation results in a typedef of the resulting server service operation.</span></span> <span data-ttu-id="ab769-232">這個 typedef 可用來參考函式資料表中的作業（如先前所述）。</span><span class="sxs-lookup"><span data-stu-id="ab769-232">This typedef is used to refer to the operation in the function table as described previously.</span></span> <span data-ttu-id="ab769-233">每項作業也會產生存根函式，而該函式會將委派 nfrastructure 呼叫給實際方法。</span><span class="sxs-lookup"><span data-stu-id="ab769-233">Every operation also results in the generation of a stub function which nfrastructure calls on behalf of the delegate to the actual method.</span></span>

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

<span data-ttu-id="ab769-234">針對 SimpleMethod 作業，會在上面定義 SimpleMethodOperation typedef。</span><span class="sxs-lookup"><span data-stu-id="ab769-234">For the SimpleMethod operation, the SimpleMethodOperation typedef is defined above.</span></span> <span data-ttu-id="ab769-235">請注意，產生的方法具有展開的引數 listwith SimpleMethod 作業的輸入和輸出訊息的訊息部分，做為具名引數。</span><span class="sxs-lookup"><span data-stu-id="ab769-235">Note that the generated method has an expanded argument listwith the message part for the input and output message for SimpleMethod operation as named parameters.</span></span>

<span data-ttu-id="ab769-236">在用戶端上，每項作業都會對應至 proxy 服務作業。</span><span class="sxs-lookup"><span data-stu-id="ab769-236">On the client side each operation is mapped to a proxy service operation.</span></span>

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

## <a name="processing-wsdlbinding"></a><span data-ttu-id="ab769-237">處理 wsdl： binding</span><span class="sxs-lookup"><span data-stu-id="ab769-237">Processing wsdl:binding</span></span>

<span data-ttu-id="ab769-238">WWSAPI 服務模型支援 theSOAP 系結延伸模組。</span><span class="sxs-lookup"><span data-stu-id="ab769-238">The WWSAPI service model supports theSOAP binding extension.</span></span> <span data-ttu-id="ab769-239">每個系結都有相關聯的 **portType**。</span><span class="sxs-lookup"><span data-stu-id="ab769-239">For each binding there is an associated **portType**.</span></span>

<span data-ttu-id="ab769-240">Soap 系結延伸中指定的傳輸只是諮詢。</span><span class="sxs-lookup"><span data-stu-id="ab769-240">The transport specified in soap binding extension is advisory only.</span></span> <span data-ttu-id="ab769-241">建立通道時，應用程式必須提供傳輸資訊。</span><span class="sxs-lookup"><span data-stu-id="ab769-241">Application needs to provide transport information when creating a channel.</span></span> <span data-ttu-id="ab769-242">目前我們支援 WS HTTP 系結 \_ \_ 和 ws \_ TCP 系結系結 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ab769-242">Currently we support the WS\_HTTP\_BINDING and WS\_TCP\_BINDING bindings.</span></span>

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

<span data-ttu-id="ab769-243">在我們的範例 WSDL 檔案中，我們只有一個適用于 ISimpleService 的 **portType** 。</span><span class="sxs-lookup"><span data-stu-id="ab769-243">In our example WSDL document we only have one **portType** for ISimpleService.</span></span> <span data-ttu-id="ab769-244">提供的 SOAP 系結會指出 HTTP 傳輸，這會指定為 WS HTTP 系結 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="ab769-244">The provided SOAP binding indicates the HTTP transport, which is specified as WS\_HTTP\_BINDING.</span></span> <span data-ttu-id="ab769-245">請注意，此結構沒有靜態裝飾，因為此結構必須可供應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="ab769-245">Notice that this structure does not have static decoration as this structure needs to be available to the application.</span></span>

<span data-ttu-id="ab769-246">處理 wsdl： portType</span><span class="sxs-lookup"><span data-stu-id="ab769-246">Processing wsdl:portType</span></span>

<span data-ttu-id="ab769-247">WSDL 中的每個 **portType** 都是由一或多個作業所組成。</span><span class="sxs-lookup"><span data-stu-id="ab769-247">Each **portType** in WSDL is made up of one or more operations.</span></span> <span data-ttu-id="ab769-248">作業應該與 wsdl： binding 中指出的 SOAP 系結延伸模組一致。</span><span class="sxs-lookup"><span data-stu-id="ab769-248">The operation should be consistent with the SOAP binding extension indicated in wsdl:binding.</span></span>

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

<span data-ttu-id="ab769-249">在此範例中，ISimpleService **portType** 只包含 SimpleMethod 作業。</span><span class="sxs-lookup"><span data-stu-id="ab769-249">In this example, the ISimpleService **portType** only contains the SimpleMethod operation.</span></span> <span data-ttu-id="ab769-250">這與系結區段一致，其中只有一個 WSDL 作業對應至 SOAP 動作。</span><span class="sxs-lookup"><span data-stu-id="ab769-250">This is consistent with the binding section where there is only one WSDL operation that maps to a SOAP action.</span></span>

<span data-ttu-id="ab769-251">因為 ISimpleService **portType** 只有一個作業（SimpleMethod），所以對應的函式資料表只會包含 SimpleMethod 即服務作業。</span><span class="sxs-lookup"><span data-stu-id="ab769-251">Since the ISimpleService **portType** only has one operation -- SimpleMethod -- the corresponding function table only contains SimpleMethod as a service operation.</span></span>

<span data-ttu-id="ab769-252">就中繼資料而言，每個 **portType** 都會 Wsutil.exe 到 [**WS \_ 合約 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)來對應。</span><span class="sxs-lookup"><span data-stu-id="ab769-252">In terms of metadata each **portType** is mapped by Wsutil.exe to a [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description).</span></span> <span data-ttu-id="ab769-253">**PortType** 內的每個作業都會對應至 [**WS \_ 作業 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)。</span><span class="sxs-lookup"><span data-stu-id="ab769-253">Each operation within a **portType** is mapped to a [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).</span></span>

<span data-ttu-id="ab769-254">在此範例中 **，此** 工具會產生 ISimpleService 的 [**WS \_ 合約 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) 。</span><span class="sxs-lookup"><span data-stu-id="ab769-254">In this example, **portType** the tool generates [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) for ISimpleService.</span></span> <span data-ttu-id="ab769-255">此合約描述包含 ISimpleService **portType** 上可用的特定作業數目以及 [**WS 作業 \_ \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) 的陣列，代表在 ISimpleService 上針對 portType 定義的個別作業。</span><span class="sxs-lookup"><span data-stu-id="ab769-255">This contract description contains the specific number of operations available on the ISimpleService **portType** along with an array of [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) representing the individual operations defined on the portType for ISimpleService.</span></span> <span data-ttu-id="ab769-256">由於 ISimpleService 的 ISimpleService portType 上只有一項作業，因此也只有一個 WS 作業 **\_ \_ 描述** 定義。</span><span class="sxs-lookup"><span data-stu-id="ab769-256">Since there is only one operation on ISimpleService portType for ISimpleService, there is also only one **WS\_OPERATION\_DESCRIPTION** definition.</span></span>

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

## <a name="processing-wsdlservice"></a><span data-ttu-id="ab769-257">處理 wsdl：服務</span><span class="sxs-lookup"><span data-stu-id="ab769-257">Processing wsdl:service</span></span>

<span data-ttu-id="ab769-258">WsUtil.exe 使用服務來尋找系結/porttypes，並產生描述類型、訊息、porttype 定義等的合約結構。</span><span class="sxs-lookup"><span data-stu-id="ab769-258">WsUtil.exe uses the services to find binding/porttypes, and generates contract structure that describes types, message, porttype definitions, and so on.</span></span> <span data-ttu-id="ab769-259">合約描述可從外部存取，而且會產生為透過產生的標頭所指定之全域定義結構的一部分。</span><span class="sxs-lookup"><span data-stu-id="ab769-259">Contract descriptions are externally accessible, and they are generated as part of the global definition structure specified through generated header.</span></span>

<span data-ttu-id="ab769-260">WsUtil.exe 支援在 wsdl： port 中定義的 EndpointReference 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="ab769-260">WsUtil.exe supports EndpointReference extensions defined in wsdl:port.</span></span> <span data-ttu-id="ab769-261">端點參考是以 WS-ADDRESSING 定義，做為描述服務 [端點](endpoint-address.md) 資訊的方式。</span><span class="sxs-lookup"><span data-stu-id="ab769-261">Endpoint reference is defined in WS-ADDRESSING as a way to describe [endpoint](endpoint-address.md) information of a service.</span></span> <span data-ttu-id="ab769-262">以 [**ws \_ XML \_ 字串**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)形式儲存的輸入端點參考延伸模組文字連同相符的 [**WS \_ 端點 \_ 位址 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description) ，會在全域結構的 endpointReferences 區段中產生。</span><span class="sxs-lookup"><span data-stu-id="ab769-262">The input endpoint reference extension text saved as [**WS\_XML\_STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string), together with matching [**WS\_ENDPOINT\_ADDRESS\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description) are generated in endpointReferences section in the global structure.</span></span>

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

<span data-ttu-id="ab769-263">若要使用 WsUtil 產生的中繼資料來建立 [**WS \_ 端點 \_ 位址**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) ：</span><span class="sxs-lookup"><span data-stu-id="ab769-263">To Create [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) using the WsUtil generated metadata:</span></span>

``` syntax
WsCreateReader      // Create a WS_XML_READER
Initialize a WS_XML_READER_BUFFER_INPUT
WsSetInput          // Set the encoding and input of the reader to generated endpointReferenceString
WsReadType        // Read WS_ENDPOINT_ADDRESS from the reader
    // Using WS_ELEMENT_TYPE_MAPPING, WS_ENDPOINT_ADDRESS_TYPE and generated endpointAddressDescription, 
```

<span data-ttu-id="ab769-264">用戶端 proxy 或服務 stub 中的常數位符串會產生為類型為 WS \_ XML \_ 字串的欄位，而且 proxy 或存根檔案中的所有字串都有常數位典。</span><span class="sxs-lookup"><span data-stu-id="ab769-264">Constant strings in the client proxy or service stub are generated as fields of type WS\_XML\_STRING, and there is a constant dictionary for all the strings in the proxy or stub file.</span></span> <span data-ttu-id="ab769-265">字典中的每個字串都會以區域結構的字典部分中的欄位形式產生，以提供更好的可讀性。</span><span class="sxs-lookup"><span data-stu-id="ab769-265">Each string in the dictionary is generated as a field in the dictionary part of the local structure for better readability.</span></span>

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

## <a name="processing-wsdltype"></a><span data-ttu-id="ab769-266">處理 wsdl：類型</span><span class="sxs-lookup"><span data-stu-id="ab769-266">Processing wsdl:type</span></span>

<span data-ttu-id="ab769-267">Wsutil.exe 僅支援 wsdl： type 規格中的 XML 架構 (XSD) 檔。</span><span class="sxs-lookup"><span data-stu-id="ab769-267">Wsutil.exe only supports XML schema (XSD) documents in wsdl:type specification.</span></span> <span data-ttu-id="ab769-268">其中一個特殊案例是當訊息埠指定全域元素定義時。</span><span class="sxs-lookup"><span data-stu-id="ab769-268">One special case is when a message port specifies a global element definition.</span></span> <span data-ttu-id="ab769-269">請參閱下一節，以取得在這些案例中使用之啟發學習法的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ab769-269">See the following section for more details of the heuristics used in these cases.</span></span>

## <a name="parameter-processing-heuristics"></a><span data-ttu-id="ab769-270">參數處理啟發學習法</span><span class="sxs-lookup"><span data-stu-id="ab769-270">Parameter Processing Heuristics</span></span>

<span data-ttu-id="ab769-271">在服務模型中，WSDL 訊息會對應至方法中的特定參數。</span><span class="sxs-lookup"><span data-stu-id="ab769-271">In the service model, WSDL messages are mapped to specific parameters in a method.</span></span> <span data-ttu-id="ab769-272">Wsutil.exe 有兩種類型的參數產生：在第一個樣式中，作業的輸入訊息有一個參數，而輸出訊息的一個參數 (必要) ;在第二個樣式中，Wsutil.exe 使用啟發學習法，將輸入訊息和輸出訊息的結構中的欄位對應和展開至作業中的不同參數。</span><span class="sxs-lookup"><span data-stu-id="ab769-272">Wsutil.exe has two styles of parameter generation: in first style, the operation has one parameter for input message, and one parameter for output message (if necessary); in the second style, Wsutil.exe uses a heuristic to map and expand fields in the structures for both input messages and output messages to different parameters in the operation.</span></span> <span data-ttu-id="ab769-273">輸入和輸出訊息都必須具有結構類型訊息元素，才能產生第二個方法。</span><span class="sxs-lookup"><span data-stu-id="ab769-273">Both input and output messages need to have structure type message elements to generate this second approach.</span></span>

<span data-ttu-id="ab769-274">從輸入和輸出訊息產生作業參數時，Wsutil.exe 會使用下列規則：</span><span class="sxs-lookup"><span data-stu-id="ab769-274">Wsutil.exe uses the following rules when generating operation parameters from the input and output messages:</span></span>

-   <span data-ttu-id="ab769-275">針對具有多個訊息部分的輸入和輸出訊息，每個訊息部分都是作業中的個別參數，並以訊息部分名稱做為參數名稱。</span><span class="sxs-lookup"><span data-stu-id="ab769-275">For input and output messages with multiple message parts, each message part is a separate parameter in the operation, with the message part name as parameter name.</span></span>
-   <span data-ttu-id="ab769-276">針對具有一個訊息部分的 RPC 樣式訊息，訊息部分是作業中的參數，並以訊息部分名稱做為參數名稱。</span><span class="sxs-lookup"><span data-stu-id="ab769-276">For RPC style message with one message part, the message part is a parameter in the operation, with message part name as parameter name.</span></span>
-   <span data-ttu-id="ab769-277">針對檔樣式的輸入和輸出訊息，其中包含一個訊息部分：</span><span class="sxs-lookup"><span data-stu-id="ab769-277">For document-style input and output messages with one message part:</span></span>
    -   <span data-ttu-id="ab769-278">如果訊息部分的名稱是「參數」，而專案類型是一個結構，則結構中的每個欄位都會被視為個別的參數，且功能變數名稱為參數名稱。</span><span class="sxs-lookup"><span data-stu-id="ab769-278">If the name of a message part is "parameters" and the element type is a structure, each field in the structure is treated as a separate parameter with the field name being the parameter name.</span></span>
    -   <span data-ttu-id="ab769-279">如果訊息部分名稱不是 "parameters"，則訊息會是作業中的參數，並使用訊息名稱做為對應的參數名稱。</span><span class="sxs-lookup"><span data-stu-id="ab769-279">If the message part name is not "parameters", the message is a parameter in the operation with the message name used as the corresponding parameter name.</span></span>
-   <span data-ttu-id="ab769-280">若為具有 nillable 元素的檔樣式輸入和輸出訊息，訊息會對應到一個參數，並以訊息部分名稱做為參數名稱。</span><span class="sxs-lookup"><span data-stu-id="ab769-280">For document style input and output message with nillable element, the message is mapped to one parameter, with message part name as parameter name.</span></span> <span data-ttu-id="ab769-281">加入一個額外的間接取值層級，表示指標可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ab769-281">One additional level of indirection is added to indicate the pointer can be **NULL**.</span></span>
-   <span data-ttu-id="ab769-282">如果欄位只出現在輸入訊息元素中，則會將此欄位視為 \[ in \] 參數。</span><span class="sxs-lookup"><span data-stu-id="ab769-282">If a field appears in the input message element only, the field is treated as an \[in\] parameter.</span></span>
-   <span data-ttu-id="ab769-283">如果欄位只出現在輸出訊息元素中，則會將此欄位視為 \[ out \] 參數。</span><span class="sxs-lookup"><span data-stu-id="ab769-283">If a field appears in the output message element only, the field is treated as an \[out\] parameter.</span></span>
-   <span data-ttu-id="ab769-284">如果輸入訊息和輸出訊息中有相同名稱和相同類型的欄位，則會將此欄位視為 \[ in、out \] 參數。</span><span class="sxs-lookup"><span data-stu-id="ab769-284">If there is a field with the same name and same type that appears in both the input message and the output message, the field is treated as an \[in,out\] parameter.</span></span>

<span data-ttu-id="ab769-285">下列工具可用來判斷參數的方向：</span><span class="sxs-lookup"><span data-stu-id="ab769-285">Following tools are used to determine the direction of parameters:</span></span>

-   <span data-ttu-id="ab769-286">如果欄位只出現在輸入訊息元素中，則會將此欄位視為僅限參數。</span><span class="sxs-lookup"><span data-stu-id="ab769-286">If a field appears in input message element only, the field is treated as in only parameter.</span></span>
-   <span data-ttu-id="ab769-287">如果欄位只出現在輸出訊息元素中，則會將此欄位視為僅限輸出參數。</span><span class="sxs-lookup"><span data-stu-id="ab769-287">If a field appears in output message element only, the field is treated as out only parameter.</span></span>
-   <span data-ttu-id="ab769-288">如果輸入訊息和輸出訊息中有相同名稱和相同類型的欄位，則會將此欄位視為 in、out 參數。</span><span class="sxs-lookup"><span data-stu-id="ab769-288">If there is a field with the same name and same type that appears in both input message and output message, the field is treated as an in,out parameter.</span></span>

<span data-ttu-id="ab769-289">Wsutil.exe 僅支援已排序的元素。</span><span class="sxs-lookup"><span data-stu-id="ab769-289">Wsutil.exe only supports sequenced elements.</span></span> <span data-ttu-id="ab769-290">\[ \] 如果 Wsutil.exe 無法將 in 參數和 out 參數合併為單一參數清單，則會拒絕對 in、out 參數的無效排序。</span><span class="sxs-lookup"><span data-stu-id="ab769-290">It rejects invalid ordering with regard to \[in,out\] parameters if Wsutil.exe cannot combine the in parameters and out parameters into a single parameter list.</span></span> <span data-ttu-id="ab769-291">可能會將尾碼新增至參數名稱，以避免名稱衝突。</span><span class="sxs-lookup"><span data-stu-id="ab769-291">Suffixes might be added to parameter names to avoid name collision.</span></span>

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

<span data-ttu-id="ab769-292">Wsutil.exe 將 tns： SimpleMethod 和 tns： SimpleMethodResponse ato 中的欄位視為參數，如以下的參數定義所示：</span><span class="sxs-lookup"><span data-stu-id="ab769-292">Wsutil.exe considers fields in tns:SimpleMethod and tns:SimpleMethodResponse ato be parameters, as seen in the parameter definitions below:</span></span>

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

<span data-ttu-id="ab769-293">Wsutil.exe 會從上列清單中的欄位展開參數清單，並在下列程式碼範例中產生 **ParamStruct** 結構。</span><span class="sxs-lookup"><span data-stu-id="ab769-293">Wsutil.exe expands the parameter list from the fields in the list above, and generates the **ParamStruct** structure in the following code example.</span></span> <span data-ttu-id="ab769-294">服務模型執行時間可以使用此結構，將引數傳遞至用戶端和伺服器 stub。</span><span class="sxs-lookup"><span data-stu-id="ab769-294">The service model run-time can use this structure to pass arguments to the client and server stubs.</span></span>

``` syntax
typedef struct SimpleMethodParamStruct {
  unsigned int   a;  
  unsigned int   b;
  unsigned int   c;
} ;
```

<span data-ttu-id="ab769-295">此結構僅用來描述用戶端和伺服器端上的堆疊框架。</span><span class="sxs-lookup"><span data-stu-id="ab769-295">This structure is only used to describe the stack frame on the client and server side.</span></span> <span data-ttu-id="ab769-296">訊息描述不會變更，也不會變更訊息描述所參考的元素描述。</span><span class="sxs-lookup"><span data-stu-id="ab769-296">There is no change to the message description, or to the element descriptions referenced by the message description.</span></span>

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

<span data-ttu-id="ab769-297">一般來說，會為所有 \[ out \] 和 \[ in、out 參數新增一個間接取值層級 \] 。</span><span class="sxs-lookup"><span data-stu-id="ab769-297">As a general rule, one level of indirection is added for all the \[out\] and \[in,out\] parameters.</span></span>

## <a name="parameterless-operation"></a><span data-ttu-id="ab769-298">無參數操作</span><span class="sxs-lookup"><span data-stu-id="ab769-298">Parameterless operation</span></span>

<span data-ttu-id="ab769-299">針對檔和常值作業，Wsutil.exe 會將作業視為具有一個輸入參數和一個輸出參數（如果有的話）：</span><span class="sxs-lookup"><span data-stu-id="ab769-299">For document and literal operations, Wsutil.exe treats the operation as having one input parameter and one output parameter if:</span></span>

-   <span data-ttu-id="ab769-300">輸入或輸出訊息有一個以上的部分。</span><span class="sxs-lookup"><span data-stu-id="ab769-300">The input or output message has more than one part.</span></span>
-   <span data-ttu-id="ab769-301">只有一個訊息部分，而訊息部分名稱並非「參數」。</span><span class="sxs-lookup"><span data-stu-id="ab769-301">There is only one message part and the message part name is not "parameters".</span></span>

<span data-ttu-id="ab769-302">..</span><span class="sxs-lookup"><span data-stu-id="ab769-302">..</span></span> <span data-ttu-id="ab769-303">在上述範例中，假設訊息部分的名稱為 *ParamIn*"and *ParamOut*，方法簽章會變成下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="ab769-303">In the example above, assuming the message parts are named *ParamIn*" and *ParamOut*, the method signature becomes the following code:</span></span>

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

<span data-ttu-id="ab769-304">Wsutil.exe 會產生作業描述的版本簽章，讓 WsCall 和伺服器端服務模型引擎可以檢查產生的描述是否適用于目前的平臺。</span><span class="sxs-lookup"><span data-stu-id="ab769-304">Wsutil.exe generates a version signature for the operation description such that the WsCall and server-side service model engine can check if the generated description is applicable for the current platform.</span></span>

<span data-ttu-id="ab769-305">此版本資訊會產生為 [**WS \_ 操作 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) 結構的一部分。</span><span class="sxs-lookup"><span data-stu-id="ab769-305">This version info is generated as part of the [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) structure.</span></span> <span data-ttu-id="ab769-306">版本號碼可以視為聯集 arm 選取器，讓結構成為可擴充的。</span><span class="sxs-lookup"><span data-stu-id="ab769-306">The version number can be treated as a union arm selector to make the structure extensible.</span></span> <span data-ttu-id="ab769-307">目前， **versionID** 是設定 to1，沒有後續的欄位。</span><span class="sxs-lookup"><span data-stu-id="ab769-307">Currently, the **versionID** is set to1 with no subsequent fields.</span></span> <span data-ttu-id="ab769-308">未來的 versiosn 可能會遞增版本號碼，並視需要加入更多欄位。</span><span class="sxs-lookup"><span data-stu-id="ab769-308">Future versiosn may increment the version number and include more fields as needed.</span></span> <span data-ttu-id="ab769-309">例如，Wsutil.exe 目前根據版本識別碼產生下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="ab769-309">For example, Wsutil.exe currently generates the following code based on the version ID:</span></span>

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

<span data-ttu-id="ab769-310">未來可將其擴充如下：</span><span class="sxs-lookup"><span data-stu-id="ab769-310">In the future, it could be expanded as follows:</span></span>

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

## <a name="security"></a><span data-ttu-id="ab769-311">安全性</span><span class="sxs-lookup"><span data-stu-id="ab769-311">Security</span></span>

<span data-ttu-id="ab769-312">請參閱 [Wsutil 編譯器工具](wsutil-compiler-tool.md) 主題中的安全性一節。</span><span class="sxs-lookup"><span data-stu-id="ab769-312">See the security section in the [Wsutil Compiler tool](wsutil-compiler-tool.md) topic.</span></span>

 

 




