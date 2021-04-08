---
title: 結構描述支援
description: WsUtil.exe 支援 XML 架構所指定的 XSD 架構。
ms.assetid: 33096cda-9dbe-44d2-8d08-410bc33ae81c
keywords:
- 適用于 Windows 的架構支援 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dcf9d192c999333ee8b4e341e7722cd6bd59ff5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "103932965"
---
# <a name="schema-support"></a><span data-ttu-id="9cfdd-106">結構描述支援</span><span class="sxs-lookup"><span data-stu-id="9cfdd-106">Schema support</span></span>

<span data-ttu-id="9cfdd-107">WsUtil.exe 支援 [XML 架構](https://www.w3.org/XML/Schema)所指定的 XSD 架構。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-107">WsUtil.exe supports the XSD schema specified at [XML Schema](https://www.w3.org/XML/Schema).</span></span> <span data-ttu-id="9cfdd-108">xsd 檔案和 wsdl： type 應該在相同的類別中處理，而當全域專案可以是參數清單時，wsdl： type 中的例外狀況除外。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-108">xsd file and wsdl:type should be treated in the same category, with the exception in wsdl:type when a global element could be a parameter list.</span></span> <span data-ttu-id="9cfdd-109">Wsutil.exe 會產生可在序列化程式中使用之所有全域專案定義的元素描述，以及 [WSDL 支援](wsdl-support.md)中指定之參數結構的額外輸出。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-109">Wsutil.exe generates element descriptions for all global element definitions that can be used in serializer, with additional output for parameter structure specified in [WSDL support](wsdl-support.md).</span></span>

## <a name="xsd-schema-support-level"></a><span data-ttu-id="9cfdd-110">XSD 架構支援層級</span><span class="sxs-lookup"><span data-stu-id="9cfdd-110">XSD Schema Support Level</span></span>

<span data-ttu-id="9cfdd-111">WsUtil.exe 不支援 XSD 架構的完整範圍。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-111">WsUtil.exe does not support the full extent of XSD schema.</span></span> <span data-ttu-id="9cfdd-112">目前的支援層級是在 [架構支援層級](schema-support-level.md)中定義。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-112">The current support level is defined in [Schema support level](schema-support-level.md).</span></span>

<span data-ttu-id="9cfdd-113">識別碼產生</span><span class="sxs-lookup"><span data-stu-id="9cfdd-113">Identifier generation</span></span>

<span data-ttu-id="9cfdd-114">架構中的元素名稱或類型名稱可能不是有效的 C 識別碼，而且名稱會正規化為產生的有效 C 名稱。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-114">Element name or type name in the schema might not be valid C identifier, and the names are normalized to generated valid C names.</span></span> <span data-ttu-id="9cfdd-115">不正確 C 識別碼字元會轉換成十六進位名稱，而且在必要時，底線 ' \_ ' 可能會加上名稱的前置詞。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-115">Invalid C identifier characters are converted to the hex name, and a underscore '\_' might be prefixed to the name if necessary.</span></span> <span data-ttu-id="9cfdd-116">匿名型別是以封入專案名稱命名，但前面加上底線 " \_ "，以避免發生名稱衝突。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-116">Anonymous types are named after the enclosing element name but prefixed with underscore "\_" to avoid name collision.</span></span> <span data-ttu-id="9cfdd-117">全域型別名稱會保留，就像是在不正確字元正規化之後一樣。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-117">Global type names are preserved as it is after invalid characters are normalized.</span></span> <span data-ttu-id="9cfdd-118">嵌套匿名型別前面會加上父型別名稱。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-118">Nested anonymous types are prefixed with the parent type name.</span></span>

<span data-ttu-id="9cfdd-119">針對每個全域元素定義，wsutil.exe 會在全域描述結構中產生 [**WS \_ 元素 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) 。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-119">For every global element definition, wsutil.exe generates a [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) in the global description structure.</span></span> <span data-ttu-id="9cfdd-120">針對每一個全域類型定義，wsutil.exe 會在全域描述結構中產生要由應用程式參考的類型描述。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-120">For every global type definition, wsutil.exe generates a type description in the global description structure to be referenced by application.</span></span>

<span data-ttu-id="9cfdd-121">針對結構中的每個欄位，wsutil.exe 會產生內嵌為主機殼結構一部分的 [**WS \_ 欄位 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_field_description) 。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-121">For each field in the structure, wsutil.exe generates a [**WS\_FIELD\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_field_description) embedded as part of the enclosure structure.</span></span>

## <a name="simple-types"></a><span data-ttu-id="9cfdd-122">簡單型別</span><span class="sxs-lookup"><span data-stu-id="9cfdd-122">Simple Types</span></span>

<span data-ttu-id="9cfdd-123">實值型別（如 [**WS 實 \_ 值 \_ 型**](/windows/desktop/api/WebServices/ne-webservices-ws_value_type)別中所列）會被視為簡單類型。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-123">Value types, as listed in [**WS\_VALUE\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_value_type), are treated as simple types.</span></span> <span data-ttu-id="9cfdd-124">請注意， \_ ws \_ 實數值型別其實是 [**ws \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_type)的子集。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-124">Notice that WS\_VALUE\_TYPE is really a subset of [**WS\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type).</span></span> <span data-ttu-id="9cfdd-125">它包含基本整數和浮點數資料類型，以及 DECIMAL、WS \_ DATETIME 和 UUID。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-125">It includes basic integral and float data types, as well as DECIMAL, WS\_DATETIME, and UUID.</span></span>

<span data-ttu-id="9cfdd-126">在服務模型中，簡單類型會以傳值方式傳遞，而 out 和 in 會以傳址方式傳遞簡單類型。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-126">In service model, in simple types are passed by value, while out and in,out simple types are passed by reference.</span></span>

<span data-ttu-id="9cfdd-127">Wsutil 為包含簡單類型的 global 元素建立如下的簡單元素描述。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-127">Wsutil create simple element description like below for global element containing simple types.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="helloworld" type="xs:int"></xs:element>
</xs:schema>
```

<span data-ttu-id="9cfdd-128">Wsutil 會產生下列元素描述：</span><span class="sxs-lookup"><span data-stu-id="9cfdd-128">Wsutil generates the element description below:</span></span>

``` syntax
...  // global elements
{ // helloworld
{
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.helloworldTypeName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.helloworldTypeNamespace,
WS_INT32_TYPE,
0,
},
}, // helloworld
... 
```

<span data-ttu-id="9cfdd-129">此結構會產生為標頭檔中所產生全域描述結構的一部分：</span><span class="sxs-lookup"><span data-stu-id="9cfdd-129">This structure is generated as part of the global description structure generated in header file:</span></span>

``` syntax
typedef struct _example_wsdl
{
WS_ELEMENT_DESCRIPTION helloworld;
} _example_wsdl;
```

## <a name="arrays"></a><span data-ttu-id="9cfdd-130">陣列</span><span class="sxs-lookup"><span data-stu-id="9cfdd-130">Arrays</span></span>

<span data-ttu-id="9cfdd-131">MaxOccurs 大於1的元素，或只有一個專案的序列，而子專案的 maxOccurs 大於1，則會被視為陣列。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-131">Element with maxOccurs larger than 1, or sequence with only one item, and the child element has maxOccurs larger than 1, is treated as array.</span></span> <span data-ttu-id="9cfdd-132">若為架構中的陣列元素，wsutil.exe 會產生兩個欄位：一個不在網路上的計數位段，以及一個包含陣列類型的指標欄位。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-132">For an array element in schema, wsutil.exe generates two fields: one count field that does not go on wire, and one pointer field containing the array type.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="SimpleArray">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" maxOccurs="50" name="a" nillable="true" type="xs:int" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
</xs:schema>
```

<span data-ttu-id="9cfdd-133">標頭檔包含陣列的 C 結構定義，以及指定陣列計數的欄位帳戶。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-133">Header file contains the C structure definition for the array, with field aCount specifying the count of the array.</span></span>

``` syntax
typedef struct SimpleArray
{
  unsigned int  aCount ;
  int  * a;
} SimpleArray;
```

<span data-ttu-id="9cfdd-134">以下是描述陣列的 LocalDefinition 原型的一部分：</span><span class="sxs-lookup"><span data-stu-id="9cfdd-134">Following is part of the LocalDefinition prototype describing the array:</span></span>

``` syntax
... // globalElement part of the LocalDefinitions.
struct // SimpleArray
{
  struct // SimpleArray
  {
    WS_FIELD_DESCRIPTION a;
    WS_FIELD_DESCRIPTION * SimpleArrayFields [1];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleArraydescs; // SimpleArray
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleArray;

// Method with array parameters.
  typedef HRESULT (CALLBACK *SimpleMethodCallback)(
    const WS_OPERATION_CONTEXT* context,
    unsigned int aCount,
    int* a,
    unsigned int *bCount,
    int** b,
    unsigned int* cCount,
    int** c,
    const WS_ASYNC_CONTEXT* asyncContext,
    WS_ERROR* error);

  HRESULT CALLBACK SimpleMethod (
    WS_SERVICE_PROXY* serviceProxy,
    WS_HEAP* heap,
    unsigned int aCount,
    int* a,
    unsigned int *bCount,
    int** b,
    unsigned int* cCount,
    int** c,
    const WS_ASYNC_CONTEXT* asyncContext,
    WS_ERROR* error);
```

<span data-ttu-id="9cfdd-135">以下是上述描述所產生的定義，請注意 WS \_ 重複專案 \_ 欄位對應，其會將 \_ \_ 欄位指出為數組欄位。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-135">Following is the generated definitions of the above descriptions, notice the WS\_REPEATING\_ELEMENT\_FIELD\_MAPPING which indicates the field as an array field.</span></span>

``` syntax
...
{ // SimpleArray
  {   // SimpleArray
    { // field description for a
      WS_REPEATING_ELEMENT_FIELD_MAPPING,
      0,
      0,
      WS_INT32_TYPE,
      0,
      WsOffsetOf(SimpleArray, a),
      0,
      0,
      WsOffsetOf(SimpleArray, aCount),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    },    // end of field description for a
    {    // fields description for SimpleArray
      (WS_FIELD_DESCRIPTION*)&example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.a,
    },
    {
      sizeof(SimpleArray),
      __alignof(SimpleArray),
      (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.
      SimpleArrayFields,
      WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.SimpleArrayFields),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayTypeName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    },   // struct description for SimpleArray
  },    // SimpleArray
  {
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    WS_STRUCT_TYPE,
    (void *)&example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.structDesc,
  },
}, // SimpleArray
...
```

<span data-ttu-id="9cfdd-136">如果陣列是輸入/輸出訊息中的參數欄位，則會為方法產生兩個實際參數。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-136">If the array is a parameter field in input/output message, there would be two actual parameters generated for the method.</span></span> <span data-ttu-id="9cfdd-137">如果陣列是 out 或 in、out 參數，paramStruct 中的兩個欄位都會有一個額外的間接取值層級。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-137">If the array is an out or in,out parameter, there would be one additional level of indirection for both fields in paramStruct.</span></span>

## <a name="range-on-array"></a><span data-ttu-id="9cfdd-138">陣列上的範圍</span><span class="sxs-lookup"><span data-stu-id="9cfdd-138">Range on Array</span></span>

<span data-ttu-id="9cfdd-139">我們建議您不要針對陣列指定 maxOccur = "未系結" 的最佳作法。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-139">We recommend the best practice of not specifying maxOccur="unbounded" for arrays.</span></span> <span data-ttu-id="9cfdd-140">相反地，您應該指定固定的整數，以設定允許的陣列計數上限。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-140">Instead, a fixed integer number should be specified to set a upper bound of array counts allowed.</span></span> <span data-ttu-id="9cfdd-141">整數類資料類型以及字串、位元組陣列和泛型陣列都支援範圍。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-141">range is supported for integral types, as well as strings, byte arrays, and generic arrays.</span></span>

## <a name="heuristic-for-wrapped-as-opposed-to-unwrapped-array"></a><span data-ttu-id="9cfdd-142">適用于包裝而非解除包裝陣列的啟發式</span><span class="sxs-lookup"><span data-stu-id="9cfdd-142">Heuristic for Wrapped as Opposed to Unwrapped array</span></span>

<span data-ttu-id="9cfdd-143">有時候陣列會包裝在另一個結構內，以內嵌在最上層結構中。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-143">Sometimes arrays are wrapped inside another structure to be embedded in a top level structure.</span></span> <span data-ttu-id="9cfdd-144">在這種情況下，我們應該移除中繼包裝函式層。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-144">In that case, we should remove the intermediate wrapper layer.</span></span> <span data-ttu-id="9cfdd-145">WsUtil.exe 會產生與上述 SimpleArray 相同的原型和描述。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-145">WsUtil.exe generates the same prototype and descriptions as SimpleArray described above.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:complexType name="SimpleArray">
  <xs:sequence>
   <xs:element minOccurs="0" maxOccurs="50" name="aa" type="xs:int" />
  </xs:sequence>
 </xs:complexType>
 <xs:element name="SimpleArrayWrapper">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="SimpleArray" type="tns:SimpleArray" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
</xs:schema>
```

<span data-ttu-id="9cfdd-146">Wsutil 會偵測到 SimpleArrayWrapper 是 SimpleArray 的包裝函式，而且只會產生下列結構，並使用不同的結構來 SimpleArray</span><span class="sxs-lookup"><span data-stu-id="9cfdd-146">Wsutil detects that SimpleArrayWrapper is a wrapper around SimpleArray, and generates following structures only, with separate structure for SimpleArray</span></span>

``` syntax
typedef struct SimpleArrayWrapper
{
  unsigned int  SimpleArrayCount ;
  int  * SimpleArray;
} SimpleArrayWrapper;

.. // global element inside the LocalDefinitions prototype
struct // SimpleArrayWrapper
{
  struct // SimpleArrayWrapper
  {
    WS_FIELD_DESCRIPTION SimpleArray;
    WS_FIELD_DESCRIPTION * SimpleArrayWrapperFields [1];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleArrayWrapperdescs; // SimpleArrayWrapper
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleArrayWrapper;
...
```

<span data-ttu-id="9cfdd-147">wsutil.exe 會為上述的相符原型產生下列定義，請注意，在欄位描述中，會填入包裝函式名稱和包裝函式命名空間欄位</span><span class="sxs-lookup"><span data-stu-id="9cfdd-147">wsutil.exe generates the following definitions for the matching prototype above, notices that in the field description, the wrapper name and wrapper namespace fields are filled in</span></span>

``` syntax
... // global element part of the LocalDefinitions structure:
{ // SimpleArrayWrapper
  {   // SimpleArrayWrapper
    { // WS_FIELD_DESCRIPTION  for SimpleArray
      WS_REPEATING_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayWrapperName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
      WS_INT32_TYPE,
      0,
      WsOffsetOf(SimpleArrayWrapper, SimpleArray),
      0,
      0,
      WsOffsetOf(SimpleArrayWrapper, SimpleArrayCount),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
    },    // end of field description for SimpleArray
    {    // array of field descriptions for SimpleArrayWrapper
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.SimpleArray,
    },
    {  // WS_STRUCT_DESCRIPTION for SimpleArrayWrapper
      sizeof(SimpleArrayWrapper),
      __alignof(SimpleArrayWrapper),
      (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.SimpleArrayWrapperFields,
      WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.SimpleArrayWrapperFields),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayWrapperTypeName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
    },   // struct description for SimpleArrayWrapper
    },    // SimpleArrayWrapper
  {  // WS_ELEMENT_DESCRIPTION for SimpleArrayWrapper
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayWrapperTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
    WS_STRUCT_TYPE,
    (void *)&example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.structDesc,
  },
}, // SimpleArrayWrapper
```

## <a name="structures"></a><span data-ttu-id="9cfdd-148">結構</span><span class="sxs-lookup"><span data-stu-id="9cfdd-148">Structures</span></span>

<span data-ttu-id="9cfdd-149">序列中具有多個元素的 complexType 是一個結構。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-149">A complexType with multiple elements in a sequence is a structure.</span></span> <span data-ttu-id="9cfdd-150">例如，</span><span class="sxs-lookup"><span data-stu-id="9cfdd-150">For example,</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:complexType name="StructType">
  <xs:sequence>
   <xs:element minOccurs="0" name="FirstName" nillable="true" type="xs:string" />
   <xs:element minOccurs="0" name="LastName" nillable="true" type="xs:string" />
  </xs:sequence>
 </xs:complexType>
 <xs:element name="StructType" nillable="true" type="tns:StructType" />
</xs:schema>
```

<span data-ttu-id="9cfdd-151">Wsutil.exe 會產生結構原型，如下所示：</span><span class="sxs-lookup"><span data-stu-id="9cfdd-151">Wsutil.exe generates a structure prototype as:</span></span>

``` syntax
struct StructType
{
  WS_STRING FirstName;
  WS_STRING LastName;
};

// methods using structure parameters.
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT* context,
  StructType* a,
  StructType** b,
  StructType** c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);

HRESULT CALLBACK SimpleMethod (WS_SERVICE_PROXY* serviceProxy,
  WS_HEAP* heap,
  StructType* a,
  StructType** b,
  StructType** c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);
```

<span data-ttu-id="9cfdd-152">wsutil 會為 LocalDefinition 產生下列原型：</span><span class="sxs-lookup"><span data-stu-id="9cfdd-152">wsutil generates the following prototype for LocalDefinition:</span></span>

``` syntax
struct // StructType
{
  struct // StructType
  {
    WS_FIELD_DESCRIPTION FirstName;
    WS_FIELD_DESCRIPTION LastName;
    WS_FIELD_DESCRIPTION * StructTypeFields [2];
    WS_STRUCT_DESCRIPTION structDesc;
  } StructTypedescs; // StructType
WS_ELEMENT_DESCRIPTION elementDesc;
}
```

<span data-ttu-id="9cfdd-153">結構的定義如下所示，結構中有兩個欄位描述。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-153">The definition for the structure looks like below, with two field descriptions in the structure.</span></span>

``` syntax
// global element inside LocalDefinitions.
{ // StructType
  {   // StructType
    { // field description for FirstName
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
      WS_STRING_TYPE,
      0,
      WsOffsetOf(StructType, FirstName),
      0,
      0,
    },    // end of field description for FirstName
    { // field description for LastName
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.LastNameLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
      WS_STRING_TYPE,
      0,
      WsOffsetOf(StructType, LastName),
      0,
      0,
    },    // end of field description for LastName
    {    // fields description for StructType
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.FirstName,
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.LastName,
    },
    { // WS_STRUCT_DESCRIPTION for StructType
      sizeof(StructType),
      __alignof(StructType),
      (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.StructTypeFields,
      WsCountOf(example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.StructTypeFields),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.StructTypeTypeName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
    },   // struct description for StructType
  },    // StructType
  {
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.StructTypeTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
    WS_STRUCT_TYPE,
    (void *)&example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.structDesc,
  },
}, // StructType
```

<span data-ttu-id="9cfdd-154">為了支援擴充性，內嵌結構一律會以傳址方式來定義。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-154">To support extensibility, embedded structures are always defined passed by reference.</span></span> <span data-ttu-id="9cfdd-155">在服務中，所有 out 或 in、out 結構都會以雙重指標傳遞，以允許未來的結構延伸，以及允許 nillable 結構。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-155">In service, all out or in,out structures are passed by double pointer to allow future extension of the structure, as well as allowing nillable structure.</span></span>

## <a name="recursive-structures"></a><span data-ttu-id="9cfdd-156">遞迴結構</span><span class="sxs-lookup"><span data-stu-id="9cfdd-156">Recursive Structures</span></span>

<span data-ttu-id="9cfdd-157">支援遞迴結構，並以傳址方式傳遞內嵌類型。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-157">Recursive structures are supported, and the embedded types is passed by reference.</span></span> <span data-ttu-id="9cfdd-158">針對下列 wsdl：</span><span class="sxs-lookup"><span data-stu-id="9cfdd-158">For the following wsdl:</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="SimpleMethod">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="a" type="xs:int" />
    <xs:element minOccurs="0" name="b" type="tns:example" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
 <xs:complexType name="example">
  <xs:sequence>
   <xs:element minOccurs="0" name="d" type="tns:example" />
   <xs:element minOccurs="0" name="c" type="xs:int" />
  </xs:sequence>
 </xs:complexType>
</xs:schema>
```

<span data-ttu-id="9cfdd-159">Wsutil 會產生下列型別定義以及型別描述：</span><span class="sxs-lookup"><span data-stu-id="9cfdd-159">Wsutil generates the follow type definitions, as well as the type descriptions:</span></span>

``` syntax
typedef struct example
{
  struct example  * d;
  int32   c;
} example;

typedef struct SimpleMethod
{
  unsigned __int32   a;
  struct example  * b;
} SimpleMethod;

// global element part of the LocalDefinitions.
...
struct // SimpleMethod
{
  struct // SimpleMethod
  {
    WS_FIELD_DESCRIPTION a;
    struct // example
    {
      WS_FIELD_DESCRIPTION d;
      WS_FIELD_DESCRIPTION c;
      WS_FIELD_DESCRIPTION * exampleFields [2];
      WS_STRUCT_DESCRIPTION structDesc;
    } exampledescs; // example
    WS_FIELD_DESCRIPTION b;
    WS_FIELD_DESCRIPTION * SimpleMethodFields [2];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleMethoddescs; // SimpleMethod
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleMethod;
...
```

<span data-ttu-id="9cfdd-160">定義的產生方式如下：</span><span class="sxs-lookup"><span data-stu-id="9cfdd-160">The definition is generated as below:</span></span>

``` syntax
{   // SimpleMethod
  { // field description for a
    WS_ELEMENT_FIELD_MAPPING,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aLocalName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    WS_INT32_TYPE,
    0,
    WsOffsetOf(SimpleMethod, a),
    0,
    0,
  },    // end of field description for a
  {   // example
    { // field description for d
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.dLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
      WS_STRUCT_TYPE,
      (WS_STRUCT_DESCRIPTION*)&example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.structDesc,
      WsOffsetOf(example, d),
      WS_FIELD_POINTER,
      0,
    },    // end of field description for d
    { // field description for c
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.cLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
      WS_INT32_TYPE,
      0,
      WsOffsetOf(example, c),
      0,
      0,
    },    // end of field description for c
    {    // fields description for example
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.d,
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.c,
    },
  {
    sizeof(example),
    __alignof(example),
    (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.exampleFields,
    WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.exampleFields),
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.exampleTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  },   // struct description for example
}
```

## <a name="structure-inheritence"></a><span data-ttu-id="9cfdd-161">結構繼承</span><span class="sxs-lookup"><span data-stu-id="9cfdd-161">Structure inheritence</span></span>

<span data-ttu-id="9cfdd-162">wsutil 支援複雜類型延伸，其中一個複雜類型是另一個複雜類型的延伸。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-162">wsutil supports complex type extension where one complex type is an extension to another complex type.</span></span>

``` syntax
<s:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:s="http://www.w3.org/2001/XMLSchema">
 <s:complexType name="LinkList">
  <s:sequence>
   <s:element minOccurs="0" name="d" type="tns:LinkList" />
   <s:element minOccurs="0" name="c" type="s:int" />
  </s:sequence>
 </s:complexType> 
 <s:element name="DerivedLinkList">
  <s:complexType>
   <s:complexContent>
    <s:extension base="tns:LinkList">
     <s:sequence>
      <s:element name="derive1" type="s:int" />
     </s:sequence>
    </s:extension>
   </s:complexContent>
  </s:complexType>
 </s:element>
</s:schema>
```

<span data-ttu-id="9cfdd-163">上述 xsd 片段表示 DerivedLinkList 衍生自 .Linklist。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-163">The above xsd fragment indicates that DerivedLinkList derives from LinkList.</span></span>

<span data-ttu-id="9cfdd-164">Wsutil.exe 會產生 C 和 c + + 的 helper 常式，讓應用程式更容易設定基底類型和衍生類型的類型資訊。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-164">Wsutil.exe generates helper routines for both C and C++ to make it easier for application to set up the type information of base type and derived types.</span></span> <span data-ttu-id="9cfdd-165">在下列程式碼中 \_ ， \_ 會使用 WS >cplusplus 宏來區分 C 和 c + + 語言的定義：</span><span class="sxs-lookup"><span data-stu-id="9cfdd-165">In the following code, \_WS\_CPLUSPLUS macro is used to differentiate definition for C and C++ language:</span></span>

``` syntax
#if defined(_WS_CPLUSPLUS)
typedef struct LinkList
{
  LinkList();
  LinkList(WS_STRUCT_DESCRIPTION*);
  struct _DerivedLinkList* WINAPI As_DerivedLinkList();
  const struct _WS_STRUCT_DESCRIPTION* _type;
  struct LinkList * d;
  int  c;
} LinkList;
#endif

#if !defined(_WS_CPLUSPLUS)
typedef struct LinkList
{
  const struct _WS_STRUCT_DESCRIPTION* _type;
  struct LinkList * d;
  int  c;
} LinkList;

void WINAPI LinkList_Init(LinkList*);
#endif

#if defined(_WS_CPLUSPLUS)
typedef struct _DerivedLinkList:LinkList
{
  _DerivedLinkList();
  int  derive1;
} _DerivedLinkList;
#endif

#if !defined(_WS_CPLUSPLUS)
typedef struct _DerivedLinkList
{
  struct LinkList _base;
  int  derive1;
} _DerivedLinkList;

struct _DerivedLinkList* WINAPI LinkList_As_DerivedLinkList(LinkList*);
#endif
```

<span data-ttu-id="9cfdd-166">在 C 樣式協助程式中，在 serialiation 之前，應用程式會呼叫 wsutil 產生的常式 .Linklist \_ Init 來初始化結構，並將型別描述設定為 .linklist 型別描述。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-166">In C style helper, before serialiation, application calls wsutil generated routine LinkList\_Init to initialize the structure and set the type description to LinkList type description.</span></span> <span data-ttu-id="9cfdd-167">在還原序列化之後，應用程式可以呼叫 .Linklist \_ 做為 \_ DerivedLinkList 來取得衍生型別。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-167">After deserialization, application can call LinkList\_As\_DerivedLinkList to get the derived type.</span></span>

<span data-ttu-id="9cfdd-168">若要在執行時間中取出型別資訊，wsutil 會產生基底類型的第一個欄位，其中含有 [**WS \_ 結構 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description) \* 型別和 [**ws \_ type \_ ATTRIBUTE \_ field field \_**](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping)對應欄位對應來描述 xsi： type 資訊。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-168">To retrieve type information in runtime, wsutil generates the first field of base type with [**WS\_STRUCT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description)\* type and [**WS\_TYPE\_ATTRIBUTE\_FIELD\_MAPPING**](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping) field mapping to describe the xsi:type information.</span></span> <span data-ttu-id="9cfdd-169">應用程式可以直接設定或檢查欄位，以判斷實際的結構類型。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-169">Application can directly set or check the field to determine the actual type of structures.</span></span> <span data-ttu-id="9cfdd-170">例如，下列程式碼會設定要 DrivedLinkList 的結構類型：</span><span class="sxs-lookup"><span data-stu-id="9cfdd-170">For example, the following code set the type of the structure to be DrivedLinkList:</span></span>

``` syntax
_DerivedLinkList derivedLinkList;
derivedLinkList._base._type = (WS_STRUCT_DESCRIPTION*)test_xsd.globalElements.DerivedLinkList.typeDescription;
WsWriteType(
    writer,
    WS_ELEMENT_TYPE_MAPPING,
    WS_STRUCT_TYPE,
    (WS_STRUCT_DESCRIPTION*)test_xsd.globalElements.DerivedLinkList.typeDescription,
    ...);
```

<span data-ttu-id="9cfdd-171">在還原序列化結構之後，應用程式可以直接比較型別描述，以判斷還原序列化的型別：</span><span class="sxs-lookup"><span data-stu-id="9cfdd-171">After the structure is deserialized, application can directly compares the type description to determine the deserialized type:</span></span>

``` syntax
if (derviedLinkList._base._type == (WS_STRUCT_DESCRIPTION*)test_xsd.globalElements.DerivedLinkList.typeDescription)
{
    // the deserialized type is of type _DerivedLinkList
    ...
}
```

<span data-ttu-id="9cfdd-172">wsutil 會產生基底結構和衍生結構的類別。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-172">wsutil generate class for both base structure and derived structure.</span></span> <span data-ttu-id="9cfdd-173">預設的函式會初始化型別和相符的型別描述。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-173">The default constructor initialize the type and matching type description.</span></span> <span data-ttu-id="9cfdd-174">AsDerivedType 常式有助於在類型之間進行安全類型轉換。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-174">The AsDerivedType routine helps to do safe type casting between types.</span></span>

``` syntax
  { // field description for typeOfLinkList
  WS_TYPE_ATTRIBUTE_FIELD_MAPPING,
  0,
  0,
  WS_DESCRIPTION_TYPE,
  0,
  WsOffsetOf(LinkList, typeOfLinkList),
  0,
  0,
  },    // end of field description for typeOfLinkList        ...
  {
  sizeof(LinkList),
  __alignof(LinkList),
  (WS_FIELD_DESCRIPTION**)&test_xsdLocalDefinitions.globalTypes.LinkListdescs.LinkListFields,
WsCountOf(test_xsdLocalDefinitions.globalTypes.LinkListdescs.LinkListFields),
(WS_XML_STRING*)&test_xsdLocalDefinitions.dictionary.xmlStrings.LinkListTypeName,
(WS_XML_STRING*)&test_xsdLocalDefinitions.dictionary.xmlStrings.LinkListTypeNamespace,
0,
(WS_STRUCT_DESCRIPTION**)&test_xsdLocalDefinitions.globalTypes.LinkListdescs.SubTypes,
  1,
  },   // struct description for LinkList
```

## <a name="nillable"></a><span data-ttu-id="9cfdd-175">nillable</span><span class="sxs-lookup"><span data-stu-id="9cfdd-175">nillable</span></span>

<span data-ttu-id="9cfdd-176">字串、結構和位元組陣列都支援 nillable 屬性。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-176">nillable attribute is supported for strings, structs, and byte arrays.</span></span> <span data-ttu-id="9cfdd-177">WS \_ FIELD \_ NILLABLE 屬性將會新增至具有 NILLABLE 屬性的欄位。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-177">WS\_FIELD\_NILLABLE attribute will be added to fields with nillable attribute.</span></span> <span data-ttu-id="9cfdd-178">如果元素為 nillable，指標將設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-178">The pointer will be set to **NULL** if an element is nillable.</span></span> <span data-ttu-id="9cfdd-179">結構中的 nillable 欄位會被視為指標。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-179">A nillable field in a structure is treated as a pointer.</span></span> <span data-ttu-id="9cfdd-180">具有 nillable 屬性的參數結構將以傳址方式傳遞。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-180">A parameter structure with nillable attribute will be passed by reference.</span></span>

## <a name="pointers"></a><span data-ttu-id="9cfdd-181">指標</span><span class="sxs-lookup"><span data-stu-id="9cfdd-181">pointers</span></span>

<span data-ttu-id="9cfdd-182">實值型別必須以傳值方式或傳址方式傳遞給 out 參數。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-182">Value type must be passed by value or by reference for out parameters.</span></span> <span data-ttu-id="9cfdd-183">除了 out 結構以外，不允許使用 Double 指標。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-183">Double pointer is not allowed except for out only structures.</span></span>

## <a name="parameterless"></a><span data-ttu-id="9cfdd-184">依據</span><span class="sxs-lookup"><span data-stu-id="9cfdd-184">Parameterless</span></span>

<span data-ttu-id="9cfdd-185">回想一下先前的訊息部分「參數」名稱討論。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-185">Recall our prior discussion for the "parameters" name for the message part.</span></span> <span data-ttu-id="9cfdd-186">如果指定此項，我們會嘗試為產生的服務作業產生輸入和輸出訊息的合併框架。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-186">If this is specified we will attempt to generate a combined frame for input and output message for the resulting service operation.</span></span> <span data-ttu-id="9cfdd-187">如果未指定此項，則產生的服務作業將會包含輸入和輸出訊息作為結構作為參數。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-187">If this is not specified the resulting service operation would then contain input and output messages as structs as parameters.</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" 
xmlns:soapenc="http://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="http://Sapphire.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="http://schemas.xmlsoap.org/ws/2004/09/policy" 
xmlns:wsap="http://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" 
xmlns:soap12="http://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="http://www.w3.org/2005/08/addressing" 
xmlns:wsx="http://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="http://Sapphire.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="noparameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="noparameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
</wsdl:definitions>
```

<span data-ttu-id="9cfdd-188">因此，在我們的 SimpleMethod 作業中，服務和用戶端的簽章看起來會像這樣。</span><span class="sxs-lookup"><span data-stu-id="9cfdd-188">Thus for our SimpleMethod operation the signature for the service and the client will look like.</span></span>

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback)
  (const WS_OPERATION_CONTEXT* context,
  SimpleMethodRequest* inMessage,
  SimpleMethodResponse** outMessage,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);

HRESULT CALLBACK SimpleMethod (
  WS_SERVICE_PROXY* serviceProxy,
  WS_HEAP* heap,
  SimpleMethodRequest* inMessage,
  SimpleMethodResponse** outMessage,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);
```

## <a name="security"></a><span data-ttu-id="9cfdd-189">安全性</span><span class="sxs-lookup"><span data-stu-id="9cfdd-189">Security</span></span>

<span data-ttu-id="9cfdd-190">請參閱[Wsutil 編譯器工具](wsutil-compiler-tool.md)和[序列化](serialization.md)中的安全性一節</span><span class="sxs-lookup"><span data-stu-id="9cfdd-190">See security section in [Wsutil Compiler tool](wsutil-compiler-tool.md) as well as [Serialization](serialization.md)</span></span>

 

 




