---
title: XML 節點
description: XML 節點代表單一的 XML 片段，例如，start 元素及其屬性、end 元素、text 或 \ 0034，類型為 \ 0034;文字內容，例如整數或位元組陣列。 節點中的資料會根據 WS \_ XML \_ 節點類型而有所不同 \_ 。
ms.assetid: c514c542-029b-46d1-a796-1f132a41b2ad
keywords:
- 適用于 Windows 的 XML 節點 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac212205fac02db0ee87d8acbe0b123ffcead921
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "106999806"
---
# <a name="xml-node"></a><span data-ttu-id="95bbb-107">XML 節點</span><span class="sxs-lookup"><span data-stu-id="95bbb-107">XML Node</span></span>

<span data-ttu-id="95bbb-108">XML 節點代表單一的 XML 片段，例如，開始專案和其屬性、end 元素、文字或「具類型」的文字內容，例如整數或位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="95bbb-108">An XML Node represents a single piece of XML, for example, a start element and its attributes, an end element, text, or "typed" text content such as an integer or byte array.</span></span> <span data-ttu-id="95bbb-109">節點中的資料會根據 [**WS \_ XML \_ 節點 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type)而有所不同。</span><span class="sxs-lookup"><span data-stu-id="95bbb-109">The data in a node varies according to the [**WS\_XML\_NODE\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type).</span></span>


<span data-ttu-id="95bbb-110">以下顯示以編碼獨立結構表示的編碼特定 xml 檔的範例。</span><span class="sxs-lookup"><span data-stu-id="95bbb-110">The following shows an example of an encoding specific xml document represented with encoding independent structures.</span></span>

``` syntax
<p:PurchaseOrder xmlns:p="http://tempuri.org" p:id="3891">
    <p:Buyer>Joe</p:Buyer>
</p:PurchaseOrder>
```

``` syntax
WS_XML_STRING purchaseOrder = WS_XML_STRING_VALUE("PurchaseOrder");
WS_XML_STRING id            = WS_XML_STRING_VALUE("id");
WS_XML_STRING prefix        = WS_XML_STRING_VALUE("p");
WS_XML_STRING ns            = WS_XML_STRING_VALUE("http://tempuri.org");

WS_XML_ATTRIBUTE xmlnsAttribute =
{
    /* singleQuote */ FALSE,
    /* isXmlNs     */ TRUE,
    /* prefix      */ &prefix,
    /* localName   */ NULL,
    /* ns          */ &ns,
    /* value       */ NULL
};
WS_XML_INT32_TEXT idText =
{
    /* text  */ { WS_XML_TEXT_TYPE_INT32 },
    /* value */ 3891
};
WS_XML_ATTRIBUTE idAttribute =
{
    /* singleQuote */ FALSE,
    /* isXmlNs     */ FALSE,
    /* prefix      */ &prefix,
    /* localName   */ &id,
    /* ns          */ &ns,
    /* value       */ &idText.text,
};
WS_XML_ATTRIBUTE* attributes[2] =
{
    &xmlnsAttribute,
    &idAttribute
};
WS_XML_ELEMENT_NODE elementNode =
{
    /* node           */ { WS_XML_NODE_TYPE_ELEMENT },
    /* prefix         */ &prefix,
    /* localName      */ &purchaseOrder,
    /* ns             */ &ns,
    /* attributeCount */ 2,
    /* attributes     */ attributes,
    /* isEmpty        */ FALSE,
    /* array          */ NULL,
};
WS_XML_UTF8_TEXT joeText =
{
    /* text  */ { WS_XML_TEXT_TYPE_UTF8 },
    /* value */ WS_XML_STRING_VALUE("Joe")
};
WS_XML_TEXT_NODE textNode =
{
    /* node */ { WS_XML_NODE_TYPE_TEXT },
    /* text */ &joeText.text
};
WS_XML_NODE endElementNode =
{
    WS_XML_NODE_TYPE_END_ELEMENT
};
WS_XML_NODE* nodes[3] =
{
    &elementNode.node,
    &textNode.node,
    &endElementNode
};
```

<span data-ttu-id="95bbb-111">下列列舉適用于 XML 節點：</span><span class="sxs-lookup"><span data-stu-id="95bbb-111">The following enumerations are used with XML nodes:</span></span>

-   [<span data-ttu-id="95bbb-112">**WS \_ 值 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="95bbb-112">**WS\_VALUE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_value_type)
-   [<span data-ttu-id="95bbb-113">**WS \_ XML \_ 節點 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="95bbb-113">**WS\_XML\_NODE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type)
-   [<span data-ttu-id="95bbb-114">**WS \_ XML \_ 文字 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="95bbb-114">**WS\_XML\_TEXT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_text_type)

<span data-ttu-id="95bbb-115">下列函式適用于 XML 節點：</span><span class="sxs-lookup"><span data-stu-id="95bbb-115">The following functions are used with XML nodes:</span></span>

-   [<span data-ttu-id="95bbb-116">**WsTrimXmlWhitespace**</span><span class="sxs-lookup"><span data-stu-id="95bbb-116">**WsTrimXmlWhitespace**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wstrimxmlwhitespace)
-   [<span data-ttu-id="95bbb-117">**WsVerifyXmlNCName**</span><span class="sxs-lookup"><span data-stu-id="95bbb-117">**WsVerifyXmlNCName**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsverifyxmlncname)
-   [<span data-ttu-id="95bbb-118">**WsXmlStringEquals**</span><span class="sxs-lookup"><span data-stu-id="95bbb-118">**WsXmlStringEquals**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsxmlstringequals)

<span data-ttu-id="95bbb-119">下列宏適用于 XML 節點：</span><span class="sxs-lookup"><span data-stu-id="95bbb-119">The following macros are used with XML nodes:</span></span>

-   [<span data-ttu-id="95bbb-120">**WS \_ XML \_ 字串 \_ 字典 \_ 值**</span><span class="sxs-lookup"><span data-stu-id="95bbb-120">**WS\_XML\_STRING\_DICTIONARY\_VALUE**</span></span>](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_dictionary_value)
-   <span data-ttu-id="95bbb-121">[**WS \_ XML \_ 字串 \_ Null**](/previous-versions/windows/desktop/legacy/dd323562(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="95bbb-121">[**WS\_XML\_STRING\_NULL**](/previous-versions/windows/desktop/legacy/dd323562(v=vs.85))</span></span>
-   [<span data-ttu-id="95bbb-122">**WS \_ XML \_ 字串 \_ 值**</span><span class="sxs-lookup"><span data-stu-id="95bbb-122">**WS\_XML\_STRING\_VALUE**</span></span>](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_value)

<span data-ttu-id="95bbb-123">下列結構適用于 XML 節點：</span><span class="sxs-lookup"><span data-stu-id="95bbb-123">The following structures are used with XML nodes:</span></span>

-   [<span data-ttu-id="95bbb-124">**WS \_ XML \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="95bbb-124">**WS\_XML\_ATTRIBUTE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_attribute)
-   [<span data-ttu-id="95bbb-125">**WS \_ XML \_ BASE64 \_ 文字**</span><span class="sxs-lookup"><span data-stu-id="95bbb-125">**WS\_XML\_BASE64\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_base64_text)
-   [<span data-ttu-id="95bbb-126">**WS \_ XML \_ BOOL \_ TEXT**</span><span class="sxs-lookup"><span data-stu-id="95bbb-126">**WS\_XML\_BOOL\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_bool_text)
-   [<span data-ttu-id="95bbb-127">**WS \_ XML \_ 批註 \_ 節點**</span><span class="sxs-lookup"><span data-stu-id="95bbb-127">**WS\_XML\_COMMENT\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_comment_node)
-   [<span data-ttu-id="95bbb-128">**WS \_ XML \_ DATETIME \_ TEXT**</span><span class="sxs-lookup"><span data-stu-id="95bbb-128">**WS\_XML\_DATETIME\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_datetime_text)
-   [<span data-ttu-id="95bbb-129">**WS \_ XML \_ DECIMAL \_ TEXT**</span><span class="sxs-lookup"><span data-stu-id="95bbb-129">**WS\_XML\_DECIMAL\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_decimal_text)
-   [<span data-ttu-id="95bbb-130">**WS \_ XML \_ 字典**</span><span class="sxs-lookup"><span data-stu-id="95bbb-130">**WS\_XML\_DICTIONARY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary)
-   [<span data-ttu-id="95bbb-131">**WS \_ XML \_ DOUBLE \_ TEXT**</span><span class="sxs-lookup"><span data-stu-id="95bbb-131">**WS\_XML\_DOUBLE\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_double_text)
-   [<span data-ttu-id="95bbb-132">**WS \_ XML \_ 元素 \_ 節點**</span><span class="sxs-lookup"><span data-stu-id="95bbb-132">**WS\_XML\_ELEMENT\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_element_node)
-   [<span data-ttu-id="95bbb-133">**WS \_ XML \_ FLOAT \_ TEXT**</span><span class="sxs-lookup"><span data-stu-id="95bbb-133">**WS\_XML\_FLOAT\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_float_text)
-   [<span data-ttu-id="95bbb-134">**WS \_ XML \_ GUID \_ 文字**</span><span class="sxs-lookup"><span data-stu-id="95bbb-134">**WS\_XML\_GUID\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_guid_text)
-   [<span data-ttu-id="95bbb-135">**WS \_ XML \_ INT32 \_ 文字**</span><span class="sxs-lookup"><span data-stu-id="95bbb-135">**WS\_XML\_INT32\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int32_text)
-   [<span data-ttu-id="95bbb-136">**WS \_ XML \_ INT64 \_ TEXT**</span><span class="sxs-lookup"><span data-stu-id="95bbb-136">**WS\_XML\_INT64\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int64_text)
-   [<span data-ttu-id="95bbb-137">**WS \_ XML \_ 清單 \_ 文字**</span><span class="sxs-lookup"><span data-stu-id="95bbb-137">**WS\_XML\_LIST\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_list_text)
-   [<span data-ttu-id="95bbb-138">**WS \_ XML \_ 節點**</span><span class="sxs-lookup"><span data-stu-id="95bbb-138">**WS\_XML\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node)
-   [<span data-ttu-id="95bbb-139">**WS \_ XML \_ QNAME**</span><span class="sxs-lookup"><span data-stu-id="95bbb-139">**WS\_XML\_QNAME**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname)
-   [<span data-ttu-id="95bbb-140">**WS \_ XML \_ QNAME \_ 文字**</span><span class="sxs-lookup"><span data-stu-id="95bbb-140">**WS\_XML\_QNAME\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_text)
-   [<span data-ttu-id="95bbb-141">**WS \_ XML \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="95bbb-141">**WS\_XML\_STRING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)
-   [<span data-ttu-id="95bbb-142">**WS \_ XML \_ 文字**</span><span class="sxs-lookup"><span data-stu-id="95bbb-142">**WS\_XML\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text)
-   [<span data-ttu-id="95bbb-143">**WS \_ XML \_ 文字 \_ 節點**</span><span class="sxs-lookup"><span data-stu-id="95bbb-143">**WS\_XML\_TEXT\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text_node)
-   [<span data-ttu-id="95bbb-144">**WS \_ XML \_ TIMESPAN \_ TEXT**</span><span class="sxs-lookup"><span data-stu-id="95bbb-144">**WS\_XML\_TIMESPAN\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_timespan_text)
-   [<span data-ttu-id="95bbb-145">**WS \_ XML \_ UINT64 \_ TEXT**</span><span class="sxs-lookup"><span data-stu-id="95bbb-145">**WS\_XML\_UINT64\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_uint64_text)
-   [<span data-ttu-id="95bbb-146">**WS \_ XML \_ 唯一 \_ 識別碼 \_ 文字**</span><span class="sxs-lookup"><span data-stu-id="95bbb-146">**WS\_XML\_UNIQUE\_ID\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_unique_id_text)
-   [<span data-ttu-id="95bbb-147">**WS \_ XML \_ UTF16 \_ TEXT**</span><span class="sxs-lookup"><span data-stu-id="95bbb-147">**WS\_XML\_UTF16\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf16_text)
-   [<span data-ttu-id="95bbb-148">**WS \_ XML \_ UTF8 \_ 文字**</span><span class="sxs-lookup"><span data-stu-id="95bbb-148">**WS\_XML\_UTF8\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf8_text)

 

 