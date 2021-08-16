---
title: XML 緩衝區
description: XML 緩衝區可為任意 XML 資料提供有效率的記憶體內部儲存體。
ms.assetid: e379628b-c6f8-48b1-8109-59fb604f2bcb
keywords:
- Windows 的 XML 緩衝區 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcd4e4725f2ad3345dcef7c33b694a8e327f4d8a6c43fbce39f9c57babfa467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118192334"
---
# <a name="xml-buffer"></a>XML 緩衝區

XML 緩衝區可為任意 XML 資料提供有效率的記憶體內部儲存體。


若要從 XML 緩衝區讀取資料，請使用 [Xml 讀取器](xml-reader.md) ，並使用 xml 緩衝區來呼叫 [**WsSetInputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer) 。 讀取器將位於檔的開頭。

若要將資料插入緩衝區，請使用 [Xml 寫入器](xml-writer.md) ，並使用 xml 緩衝區來呼叫 [**WsSetOutputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer) 。 寫入器將位於檔結尾。

一旦將讀取器設定為 XML 緩衝區，除了所有的 XML 讀取器 Api 之外， [**WsMoveReader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader) 可以用來透過檔流覽讀取器。 [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) 和 [**WsSetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition) 也可以用來記錄檔中的位置，並于稍後返回。

一旦將寫入器設定為 XML 緩衝區，除了所有的 XML 寫入器 Api 之外， [**WsMoveWriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter) 可以用來透過檔導覽寫入器。 [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) 和 [**WsSetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition) 也可以用來記錄檔中的位置，並于稍後返回。 寫入器一律會在其所在的節點之前插入資料。

您可以從 XML 緩衝區中刪除節點，方法是取得使用 [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) 或 [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) 的節點位置，然後使用該位置來呼叫 [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode) 。 若為元素，這將會刪除專案（其所有子系，包括其相符的 end 元素）。

位置由值 [**WS \_ XML \_ 節點 \_ 位置**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position)表示。 位置是特定 XML 緩衝區專屬的，而且只要 XML 緩衝區有效，就會有效。

下列列舉適用于 XML 緩衝區：

-   [**WS \_ 移 \_ 至**](/windows/desktop/api/WebServices/ne-webservices-ws_move_to)
-   [**WS \_ XML \_ 緩衝區 \_ 屬性 \_ 識別碼**](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_property_id)

下列函式適用于 XML 緩衝區：

-   [**WsCreateXmlBuffer**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlbuffer)
-   [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode)

下列控制碼用於 XML 緩衝區：

-   [WS \_ XML \_ 緩衝區](ws-xml-buffer.md)

下列結構適用于 XML 緩衝區：

-   [**WS \_ XML \_ 緩衝區 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_buffer_property)
-   [**WS \_ XML \_ 節點 \_ 位置**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position)

 

 




