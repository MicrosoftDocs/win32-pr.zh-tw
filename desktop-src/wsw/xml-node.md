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
# <a name="xml-node"></a>XML 節點

XML 節點代表單一的 XML 片段，例如，開始專案和其屬性、end 元素、文字或「具類型」的文字內容，例如整數或位元組陣列。 節點中的資料會根據 [**WS \_ XML \_ 節點 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type)而有所不同。


以下顯示以編碼獨立結構表示的編碼特定 xml 檔的範例。

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

下列列舉適用于 XML 節點：

-   [**WS \_ 值 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_value_type)
-   [**WS \_ XML \_ 節點 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type)
-   [**WS \_ XML \_ 文字 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_text_type)

下列函式適用于 XML 節點：

-   [**WsTrimXmlWhitespace**](/windows/desktop/api/WebServices/nf-webservices-wstrimxmlwhitespace)
-   [**WsVerifyXmlNCName**](/windows/desktop/api/WebServices/nf-webservices-wsverifyxmlncname)
-   [**WsXmlStringEquals**](/windows/desktop/api/WebServices/nf-webservices-wsxmlstringequals)

下列宏適用于 XML 節點：

-   [**WS \_ XML \_ 字串 \_ 字典 \_ 值**](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_dictionary_value)
-   [**WS \_ XML \_ 字串 \_ Null**](/previous-versions/windows/desktop/legacy/dd323562(v=vs.85))
-   [**WS \_ XML \_ 字串 \_ 值**](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_value)

下列結構適用于 XML 節點：

-   [**WS \_ XML \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_attribute)
-   [**WS \_ XML \_ BASE64 \_ 文字**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_base64_text)
-   [**WS \_ XML \_ BOOL \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_bool_text)
-   [**WS \_ XML \_ 批註 \_ 節點**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_comment_node)
-   [**WS \_ XML \_ DATETIME \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_datetime_text)
-   [**WS \_ XML \_ DECIMAL \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_decimal_text)
-   [**WS \_ XML \_ 字典**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary)
-   [**WS \_ XML \_ DOUBLE \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_double_text)
-   [**WS \_ XML \_ 元素 \_ 節點**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_element_node)
-   [**WS \_ XML \_ FLOAT \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_float_text)
-   [**WS \_ XML \_ GUID \_ 文字**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_guid_text)
-   [**WS \_ XML \_ INT32 \_ 文字**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int32_text)
-   [**WS \_ XML \_ INT64 \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int64_text)
-   [**WS \_ XML \_ 清單 \_ 文字**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_list_text)
-   [**WS \_ XML \_ 節點**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node)
-   [**WS \_ XML \_ QNAME**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname)
-   [**WS \_ XML \_ QNAME \_ 文字**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_text)
-   [**WS \_ XML \_ 字串**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)
-   [**WS \_ XML \_ 文字**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text)
-   [**WS \_ XML \_ 文字 \_ 節點**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text_node)
-   [**WS \_ XML \_ TIMESPAN \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_timespan_text)
-   [**WS \_ XML \_ UINT64 \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_uint64_text)
-   [**WS \_ XML \_ 唯一 \_ 識別碼 \_ 文字**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_unique_id_text)
-   [**WS \_ XML \_ UTF16 \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf16_text)
-   [**WS \_ XML \_ UTF8 \_ 文字**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf8_text)

 

 