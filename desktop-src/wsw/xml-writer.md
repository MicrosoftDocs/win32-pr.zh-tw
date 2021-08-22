---
title: XML 寫入器
description: XML 寫入器是發出 XML 的 API。 在其核心中，XML 寫入器會一次寫入一個 XML 節點，但還有其他協助程式 Api 可讓您更輕鬆地撰寫一系列節點。
ms.assetid: 69d50793-1d5b-4fc7-bf69-128f8e23a98d
keywords:
- Windows 的 XML 寫入器 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75b7937ac6d8f6e9daff40289dd34729eaf235f203a02b91b5d1af3632049b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026056"
---
# <a name="xml-writer"></a>XML 寫入器

XML 寫入器是發出 XML 的 API。 在其核心中，XML 寫入器會一次寫入一個 [XML 節點](xml-node.md) ，但還有其他協助程式 api 可讓您更輕鬆地撰寫一系列節點。


支援下列類型的寫入器輸出：

-   [**編碼位元組的記憶體中緩衝區**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [**資料流程**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   [XML 緩衝區](xml-buffer.md)

下列回呼適用于 XML 寫入器：

-   [**WS \_ 動態 \_ 字串 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [**WS \_ 提取 \_ 位元組 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [**WS \_ PUSH \_ BYTES \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [**WS \_ 寫入 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)

下列列舉適用于 XML 寫入器：

-   [**WS \_ 字元集**](/windows/desktop/api/WebServices/ne-webservices-ws_charset)
-   [**WS \_ XML \_ 寫入器 \_ 編碼 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_encoding_type)
-   [**WS \_ XML \_ 寫入器 \_ 輸出 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_output_type)
-   [**WS \_ XML \_ 寫入器 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id)

下列函式會搭配 XML 寫入器使用：

-   [**WsCopyNode**](/windows/desktop/api/WebServices/nf-webservices-wscopynode)
-   [**WsCreateWriter**](/windows/desktop/api/WebServices/nf-webservices-wscreatewriter)
-   [**WsFlushWriter**](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter)
-   [**WsFreeWriter**](/windows/desktop/api/WebServices/nf-webservices-wsfreewriter)
-   [**WsGetPrefixFromNamespace**](/windows/desktop/api/WebServices/nf-webservices-wsgetprefixfromnamespace)
-   [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition)
-   [**WsGetWriterProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterproperty)
-   [**WsMoveWriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter)
-   [**WsPullBytes**](/windows/desktop/api/WebServices/nf-webservices-wspullbytes)
-   [**WsPushBytes**](/windows/desktop/api/WebServices/nf-webservices-wspushbytes)
-   [**WsSetOutput**](/windows/desktop/api/WebServices/nf-webservices-wssetoutput)
-   [**WsSetOutputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer)
-   [**WsSetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition)
-   [**WsWriteArray**](/windows/desktop/api/WebServices/nf-webservices-wswritearray)
-   [**WsWriteBytes**](/windows/desktop/api/WebServices/nf-webservices-wswritebytes)
-   [**WsWriteChars**](/windows/desktop/api/WebServices/nf-webservices-wswritechars)
-   [**WsWriteCharsUtf8**](/windows/desktop/api/WebServices/nf-webservices-wswritecharsutf8)
-   [**WsWriteEndAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteendattribute)
-   [**WsWriteEndCData**](/windows/desktop/api/WebServices/nf-webservices-wswriteendcdata)
-   [**WsWriteEndElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteendelement)
-   [**WsWriteNode**](/windows/desktop/api/WebServices/nf-webservices-wswritenode)
-   [**WsWriteQualifiedName**](/windows/desktop/api/WebServices/nf-webservices-wswritequalifiedname)
-   [**WsWriteStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute)
-   [**WsWriteStartCData**](/windows/desktop/api/WebServices/nf-webservices-wswritestartcdata)
-   [**WsWriteStartElement**](/windows/desktop/api/WebServices/nf-webservices-wswritestartelement)
-   [**WsWriteText**](/windows/desktop/api/WebServices/nf-webservices-wswritetext)
-   [**WsWriteValue**](/windows/desktop/api/WebServices/nf-webservices-wswritevalue)
-   [**WsWriteXmlnsAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritexmlnsattribute)

下列控制碼會搭配 XML 寫入器使用：

-   [WS \_ XML \_ 寫入器](ws-xml-writer.md)

下列結構適用于 XML 寫入器：

-   [**WS \_ XML \_ 寫入器 \_ 二進位 \_ 編碼**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_binary_encoding)
-   [**WS \_ XML \_ 寫入器 \_ 緩衝區 \_ 輸出**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [**WS \_ XML \_ 寫入器 \_ 編碼**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_encoding)
-   [**WS \_ XML \_ 寫入器 \_ MTOM \_ 編碼**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_mtom_encoding)
-   [**WS \_ XML \_ 寫入器 \_ 輸出**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_output)
-   [**WS \_ XML \_ 寫入器 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_properties)
-   [**WS \_ XML \_ 寫入器 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_property)
-   [**WS \_ XML \_ 寫入器 \_ 資料流程 \_ 輸出**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   [**WS \_ XML \_ 寫入器 \_ 文字 \_ 編碼**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_text_encoding)

 

 




