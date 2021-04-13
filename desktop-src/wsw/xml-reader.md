---
title: XML 讀取器
description: XML 讀取器是 XML 輸入來源的資料指標。 在其核心中，XML 讀取器一次會讀取一個 XML 節點，但有其他協助程式 Api 可讓您更輕鬆地讀取一系列節點。
ms.assetid: 1f99e45c-64ba-42fb-9bf0-35e27f1c5ef2
keywords:
- 適用于 Windows 的 XML 讀取器 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9d9c91b6594ec569536751751a3efca4c32e08
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104463933"
---
# <a name="xml-reader"></a>XML 讀取器

XML 讀取器是 XML 輸入來源的資料指標。 在其核心中，XML 讀取器一次會讀取一個 [XML 節點](xml-node.md) ，但有其他協助程式 api 可讓您更輕鬆地讀取一系列節點。


以下是支援的讀取器輸入類型：

-   [**編碼位元組的記憶體中緩衝區**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [**資料流程**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   [XML 緩衝區](xml-buffer.md)

### <a name="security"></a>安全性

讀取器將確認元素上的屬性是否為唯一的。 執行這項驗證所需的時間，是元素上的屬性數目的函式，可以和 [**WS \_ XML \_ 讀取器屬性的 \_ \_ 最大值 \_ 屬性**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id)一樣大。 因此，當 **WS \_ XML \_ 讀取器 \_ 屬性 \_ 最大值 \_ 屬性** 設定為大數值時，處理大型檔可能會造成阻絕服務攻擊的機會。

讀取器會將前置詞對應至每個元素和屬性的命名空間。 執行此對應所需的時間，是範圍中 xmlns 屬性數目的函式，可能會與 [**WS \_ XML \_ 讀取器屬性的 \_ \_ 最大 \_ 命名空間**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id)相同。 因此，當這個屬性設定為大數值時，處理大型檔可能會造成阻絕服務攻擊的機會。

雖然讀取器會確定檔遵循 xml 的語法規格，而且其層面是在指定的配額內，但在來自不受信任的來源時，檔的內容仍然必須被視為不受信任。 讀者的使用者應該使用 [**WsReadToStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement)、 [**WsFindAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)或手動檢查 [**節點**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node)來檢查所有專案和屬性名稱和命名空間。

還有一些其他需要考慮的情況包括（但不限於）：

-   可能遺漏了預期的元素
-   可能出現未預期的元素
-   可能遺漏了預期的屬性
-   可能會出現非預期的屬性
-   元素可能會顯示為空白元素
-   空白字元可能出現在非預期的位置

讀者的使用者不應該只根據從檔讀取的值來配置記憶體。 例如，請考慮下列 xml 檔：

``` syntax
<array count='1000000'>
   <!-- malicious document provider didn't actually provide 1000000 array items -->
</array>
```

配置以陣列為基礎的 soley 時，假設有一些元素將會是潛在的攻擊向量。 在此情況下，讀取器的使用者應該改為在專案出現時以累加方式配置記憶體。

XML 讀取器不支援 DTD。 讀者的使用者不需要考慮 DTD 驗證。

下列回呼適用于 XML 讀取器：

-   [**WS \_ 讀取 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)

下列列舉適用于 XML 讀取器：

-   [**WS \_ XML \_ 讀取器 \_ 編碼 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_encoding_type)
-   [**WS \_ XML \_ 讀取器 \_ 輸入 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_input_type)
-   [**WS \_ XML \_ 讀取器 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id)

下列函式適用于 XML 讀取器：

-   [**WsCreateReader**](/windows/desktop/api/WebServices/nf-webservices-wscreatereader)
-   [**WsFillReader**](/windows/desktop/api/WebServices/nf-webservices-wsfillreader)
-   [**WsFindAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)
-   [**WsFreeReader**](/windows/desktop/api/WebServices/nf-webservices-wsfreereader)
-   [**WsGetNamespaceFromPrefix**](/windows/desktop/api/WebServices/nf-webservices-wsgetnamespacefromprefix)
-   [**WsGetReaderNode**](/windows/desktop/api/WebServices/nf-webservices-wsgetreadernode)
-   [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition)
-   [**WsGetReaderProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderproperty)
-   [**WsGetXmlAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute)
-   [**WsMoveReader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader)
-   [**WsReadArray**](/windows/desktop/api/WebServices/nf-webservices-wsreadarray)
-   [**WsReadBytes**](/windows/desktop/api/WebServices/nf-webservices-wsreadbytes)
-   [**WsReadChars**](/windows/desktop/api/WebServices/nf-webservices-wsreadchars)
-   [**WsReadCharsUtf8**](/windows/desktop/api/WebServices/nf-webservices-wsreadcharsutf8)
-   [**WsReadEndAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadendattribute)
-   [**WsReadEndElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement)
-   [**WsReadNode**](/windows/desktop/api/WebServices/nf-webservices-wsreadnode)
-   [**WsReadQualifiedName**](/windows/desktop/api/WebServices/nf-webservices-wsreadqualifiedname)
-   [**WsReadStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartattribute)
-   [**WsReadStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement)
-   [**WsReadToStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement)
-   [**WsReadValue**](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue)
-   [**WsSetInput**](/windows/desktop/api/WebServices/nf-webservices-wssetinput)
-   [**WsSetInputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer)
-   [**WsSetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition)
-   [**WsSkipNode**](/windows/desktop/api/WebServices/nf-webservices-wsskipnode)

下列控制碼會搭配 XML 讀取器使用：

-   [WS \_ XML \_ 讀取器](ws-xml-reader.md)

下列結構適用于 XML 讀取器：

-   [**WS \_ XML \_ 讀取器 \_ 二進位 \_ 編碼**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_binary_encoding)
-   [**WS \_ XML \_ 讀取器 \_ 緩衝區 \_ 輸入**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [**WS \_ XML \_ 讀取器 \_ 編碼**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_encoding)
-   [**WS \_ XML \_ 讀取器 \_ 輸入**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_input)
-   [**WS \_ XML \_ 讀取器 \_ MTOM \_ 編碼**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_mtom_encoding)
-   [**WS \_ XML \_ 讀取器 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_properties)
-   [**WS \_ XML \_ 讀取器 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_property)
-   [**WS \_ XML \_ 讀取器 \_ 資料流程 \_ 輸入**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   [**WS \_ XML \_ 讀取器 \_ 文字 \_ 編碼**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_text_encoding)

 

 




