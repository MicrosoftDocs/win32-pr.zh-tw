---
title: EventManifest 架構複雜類型
description: 以下是 EventManifest 架構所定義的複雜類型。
ms.assetid: 25facfdd-3846-4215-9b84-a833d86c39ef
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 69200d90253b27f9e73035a14ba5817917b24e1367d3bc4a54fff37e15d112ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590056"
---
# <a name="eventmanifest-schema-complex-types"></a>EventManifest 架構複雜類型

以下是 EventManifest 架構所定義的複雜類型。



| 複雜類型                                                                                       | 描述                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BitMapType**](eventmanifestschema-bitmaptype-complextype.md)                                   | 定義位值與字串值之間的名稱/值對應清單。<br/>                                                                                                                                                  |
| [**BitMapValueType**](eventmanifestschema-bitmapvaluetype-complextype.md)                         | 定義位值與字串值之間的對應。<br/>                                                                                                                                                                  |
| [**ChannelListType**](eventmanifestschema-channellisttype-complextype.md)                         | 定義提供者可以記錄事件的通道清單。<br/>                                                                                                                                                                |
| [**ChannelLoggingType**](eventmanifestschema-channelloggingtype-complextype.md)                   | 定義支援通道之記錄檔的屬性，例如其容量，以及是否為連續或迴圈。<br/>                                                                                                |
| [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md)             | 為通道所使用的會話定義記錄屬性。<br/>                                                                                                                                                        |
| [**ChannelType**](eventmanifestschema-channeltype-complextype.md)                                 | 定義提供者可以記錄事件的通道。<br/>                                                                                                                                                                         |
| [**DataDefinitionType**](eventmanifestschema-datadefinitiontype-complextype.md)                   | 定義您想要包含在事件中的資料項目。<br/>                                                                                                                                                                 |
| [**DefinitionType**](eventmanifestschema-definitiontype-complextype.md)                           | 定義提供者可記錄的事件清單。<br/>                                                                                                                                                                         |
| [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md)                 | 定義您的提供者可以撰寫的事件。<br/>                                                                                                                                                                               |
| [**EventsType**](eventmanifestschema-eventstype-complextype.md)                                   | 包含資訊清單中所定義之提供者的清單。<br/>                                                                                                                                                               |
| [**FilterType**](eventmanifestschema-filtertype-complextype.md)                                   | 定義會話用來根據事件資料篩選事件的資料篩選。<br/>                                                                                                                                              |
| [**FilterListType**](eventmanifestschema-filterlisttype-complextype.md)                           | 定義 ETW 控制器可傳遞給提供者的篩選清單，以進一步限制它所寫入的事件。<br/>                                                                                                       |
| [**ImportChannelType**](eventmanifestschema-importchanneltype-complextype.md)                     | 識別已由另一個提供者定義或包含中繼資料區段之資訊清單中的通道。<br/>                                                                                                            |
| [**InputType**](eventmanifestschema-inputtype-complextype.md)                                     | 定義輸入資料類型。<br/>                                                                                                                                                                                                  |
| [**InputTypeListType**](eventmanifestschema-inputtypelisttype-complextype.md)                     | 定義輸入類型的清單。<br/>                                                                                                                                                                                               |
| [**InstrumentationManifestType**](eventmanifestschema-instrumentationmanifesttype-complextype.md) | 定義 [**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md) 元素的基底類型。<br/>                                                                                                |
| [**Instrumentationtype.event**](eventmanifestschema-instrumentationtype-complextype.md)                 | 定義資訊清單之檢測區段的內容。<br/>                                                                                                                                                         |
| [**KeywordListType**](eventmanifestschema-keywordlisttype-complextype.md)                         | 定義分類事件的關鍵字清單。<br/>                                                                                                                                                                           |
| [**KeywordType**](eventmanifestschema-keywordtype-complextype.md)                                 | 定義可識別事件類別目錄的關鍵字。<br/>                                                                                                                                                                      |
| [**LevelListType**](eventmanifestschema-levellisttype-complextype.md)                             | 定義嚴重性層級的清單，以指定事件的詳細程度。<br/>                                                                                                                                                    |
| [**LevelType**](eventmanifestschema-leveltype-complextype.md)                                     | 定義嚴重性值，判斷所記錄事件的詳細程度。<br/>                                                                                                                                           |
| [**LocalizationType**](eventmanifestschema-localizationtype-complextype.md)                       | 定義您在資訊清單中參考的當地語系化資源群組。<br/>                                                                                                                                                  |
| [**MapType**](eventmanifestschema-maptype-complextype.md)                                         | 定義成對名稱/值的清單。<br/>                                                                                                                                                                                          |
| [**MetadataType**](eventmanifestschema-metadatatype-complextype.md)                               | 定義您可以在資訊清單的 metadata 區段中定義的元資料類型。<br/>                                                                                                                                      |
| [**NamedQueryType**](eventmanifestschema-namedquerytype-complextype.md)                           | 定義已命名查詢的清單，這些查詢會查詢事件訊息字串中的值，並執行指定的動作（如果找到的話）。<br/>                                                                                                     |
| [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md)                           | 定義用來識別應用程式元件之作業的操作碼清單。<br/>                                                                                                                        |
| [**OpcodeType**](eventmanifestschema-opcodetype-complextype.md)                                   | 定義應用程式元件內的作業。<br/>                                                                                                                                                                  |
| [**OutputType**](eventmanifestschema-outputtype-complextype.md)                                   | 定義輸出資料類型，以決定如何呈現資料。<br/>                                                                                                                                                        |
| [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md)                   | 定義用來改變訊息字串的正則運算式組清單。<br/>                                                                                                                                        |
| [**PatternMapType**](eventmanifestschema-patternmaptype-complextype.md)                           | 定義兩個正則運算式之間的對應。 其中一個運算式可用來在訊息字串中尋找相符的字串，而另一個運算式則是用來在服務將字串放回訊息字串之前變更字串。<br/> |
| [**PatternMapValueType**](eventmanifestschema-patternmapvaluetype-complextype.md)                 | 定義用來在訊息字串中尋找相符字串的正則運算式，並加以修改。<br/>                                                                                                                           |
| [**ProviderType**](eventmanifestschema-providertype-complextype.md)                               | 定義提供者及其用來定義其事件的中繼資料。<br/>                                                                                                                                                       |
| [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md)                         | 定義您可以在資訊清單中參考的當地語系化字串清單。<br/>                                                                                                                                                 |
| [**StructDefinitionType**](eventmanifestschema-structdefinitiontype-complextype.md)               | 定義結構，其中包含一個或多個您想要包含在事件中的資料項目。<br/>                                                                                                                            |
| [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md)         | 定義您的提供者可以記錄的工作特定事件。<br/>                                                                                                                                                                    |
| [**TaskListType**](eventmanifestschema-tasklisttype-complextype.md)                               | 定義用來識別應用程式元件的工作清單。<br/>                                                                                                                                          |
| [**TaskType**](eventmanifestschema-tasktype-complextype.md)                                       | 定義應用程式的元件或子元件。<br/>                                                                                                                                                                       |
| [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md)                       | 此範本會定義要包含在事件中的資料。<br/>                                                                                                                                                                   |
| [**TemplateListType**](eventmanifestschema-templatelisttype-complextype.md)                       | 定義範本清單，以指定要包含在事件中的資料。<br/>                                                                                                                                                |
| [**TypeListType**](eventmanifestschema-typelisttype-complextype.md)                               | 定義在資訊清單中使用的類型。<br/>                                                                                                                                                                             |
| [**ValueMapType**](eventmanifestschema-valuemaptype-complextype.md)                               | 定義整數值與字串值之間的名稱/值對應清單。<br/>                                                                                                                                              |
| [**ValueMapValueType**](eventmanifestschema-valuemapvaluetype-complextype.md)                     | 定義整數值與字串值之間的對應。<br/>                                                                                                                                                             |
| [**XmlType**](eventmanifestschema-xmltype-complextype.md)                                         | 定義 XML 片段。<br/>                                                                                                                                                                                                     |
| [**XmlTypeListType**](eventmanifestschema-xmltypelisttype-complextype.md)                         | 定義清單輸出類型，服務會使用此類型來判斷如何轉譯輸入資料類型。<br/>                                                                                                                             |



 

 

 





