---
title: 事件架構元素
description: 以下是事件架構定義的元素。
ms.assetid: 972c0a78-32d5-45b3-bcc3-6423b60bfa6f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 34149fae8ac273565f98c3f39adb31b61b406ade
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682467"
---
# <a name="event-schema-elements"></a>事件架構元素

以下是事件架構定義的元素。 此區段包含您會在記錄的事件中尋找的元素名稱;不過，若要取得每個專案的詳細資料，請參閱包含元素的複雜類型。



| 元素                                                                                                    | 描述                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BinaryEventData (的事件)**](eventschema-binaryeventdata-eventtype-element.md)                       | 以二進位 blob 的形式包含事件資料。<br/>                                                                                                                                                   |
| [**二元 (EventDataType)**](eventschema-binary-eventdatatype-element.md)                                 | 使用 [事件記錄](/windows/desktop/EventLog/event-logging)撰寫之事件的二進位資料 blob。<br/>                                                                                                   |
| [**Channel (RenderingInfoType)**](eventschema-channel-renderinginfotype-element.md)                       | 事件中指定之通道的呈現訊息字串。<br/>                                                                                                                          |
| [**Channel (SystemPropertiesType)**](eventschema-channel-systempropertiestype-element.md)                 | 要記錄事件的通道。<br/>                                                                                                                                                  |
| [**ComplexData (EventDataType)**](eventschema-complexdata-eventdatatype-element.md)                       | 在事件的範本中定義的結構。<br/>                                                                                                                                  |
| [**元件 (DebugDataType)**](eventschema-component-debugdatatype-element.md)                           | 記錄追蹤訊息的元件名稱。<br/>                                                                                                                                    |
| [**電腦 (SystemPropertiesType)**](eventschema-computer-systempropertiestype-element.md)               | 發生事件之電腦的名稱。<br/>                                                                                                                                       |
| [**相互關聯 (SystemPropertiesType)**](eventschema-correlation-systempropertiestype-element.md)         | 取用者可用來將相關事件群組在一起的活動識別碼。<br/>                                                                                                           |
| [**DataItemName (ProcessingErrorDataType)**](eventschema-dataitemname-processingerrordatatype-element.md) | 包含處理事件資料時，造成錯誤之事件資料項目的名稱。<br/>                                                                                            |
| [**資料 (ComplexDataType)**](eventschema-data-complexdatatype-element.md)                                 | 結構中資料項目的清單。 專案清單的順序與範本中所定義的順序相同。<br/>                                                                                |
| [**資料 (EventDataType)**](eventschema-data-eventdatatype-element.md)                                     | 在事件的範本中定義的最上層資料項目。<br/>                                                                                                                        |
| [**DebugData (的事件)**](eventschema-debugdata-eventtype-element.md)                                   | 包含可針對 Windows 軟體追蹤預處理器 (WPP) 事件記錄的資料。<br/>                                                                                                  |
| [**ErrorCode (ProcessingErrorDataType)**](eventschema-errorcode-processingerrordatatype-element.md)       | 包含處理事件資料時發生錯誤時所引發的錯誤碼。 <br/>                                                                                                     |
| [**事件**](eventschema-event-element.md)                                                                 | 這是轉譯的事件資料的根節點。<br/>                                                                                                                                           |
| [**EventData (的事件)**](eventschema-eventdata-eventtype-element.md)                                   | 包含事件資料。<br/>                                                                                                                                                                    |
| [**EventID (SystemPropertiesType)**](eventschema-eventid-systempropertiestype-element.md)                 | 提供者用來識別事件的識別碼。<br/>                                                                                                                                |
| [**EventPayload (ProcessingErrorDataType)**](eventschema-eventpayload-processingerrordatatype-element.md) | 包含事件的二進位事件資料，此事件會在處理事件資料時造成錯誤。 <br/>                                                                                           |
| [**EventRecordID (SystemPropertiesType)**](eventschema-eventrecordid-systempropertiestype-element.md)     | 記錄時指派給事件的記錄號碼。<br/>                                                                                                                                 |
| [**執行 (SystemPropertiesType)**](eventschema-execution-systempropertiestype-element.md)             | 包含記錄事件之進程和執行緒的相關資訊。<br/>                                                                                                                    |
| [**FileLine (DebugDataType)**](eventschema-fileline-debugdatatype-element.md)                             | 來源檔案的名稱，以及記錄追蹤訊息之原始程式檔內的行。<br/>                                                                                              |
| [**FlagName (DebugDataType)**](eventschema-flagname-debugdatatype-element.md)                             | 啟用時傳遞給提供者的旗標值。<br/>                                                                                                                                  |
| [**函數 (DebugDataType)**](eventschema-function-debugdatatype-element.md)                             | 記錄追蹤訊息的函數名稱。<br/>                                                                                                                                     |
| [**關鍵字 (關鍵字)**](eventschema-keyword-keywords-element.md)                                         | 包含轉譯的關鍵字。<br/>                                                                                                                                                                |
| [**關鍵字 (RenderingInfoType)**](eventschema-keywords-renderingtype-element.md)                         | 已轉譯關鍵字的清單。<br/>                                                                                                                                                                |
| [**關鍵字 (SystemPropertiesType)**](eventschema-keywords-systempropertiestype-element.md)               | 事件中所定義關鍵字的位元遮罩。<br/>                                                                                                                                             |
| [**LevelName (DebugDataType)**](eventschema-levelname-debugdatatype-element.md)                           | 啟用時傳遞給提供者的層級值。<br/>                                                                                                                                 |
| [**層級 (RenderingInfoType)**](eventschema-level-renderingtype-element.md)                               | 事件中指定之層級的轉譯訊息字串。<br/>                                                                                                                            |
| [**層級 (SystemPropertiesType)**](eventschema-level-systempropertiestype-element.md)                     | 包含事件的嚴重性層級。<br/>                                                                                                                                                   |
| [**Message (DebugDataType)**](eventschema-message-debugdatatype-element.md)                               | 訊息字串。 如果 WPP 事件指定了 FormattedString 欄位，XML 就會包含這個元素。<br/>                                                                                     |
| [**Message (RenderingInfoType)**](eventschema-message-renderingtype-element.md)                           | 包含針對事件呈現的事件訊息。<br/>                                                                                                                                  |
| [**Opcode (RenderingInfoType)**](eventschema-opcode-renderingtype-element.md)                             | 事件中指定之 opcode 的轉譯訊息字串。<br/>                                                                                                                           |
| [**Opcode (SystemPropertiesType)**](eventschema-opcode-systempropertiestype-element.md)                   | 事件中定義的操作碼。<br/>                                                                                                                                                            |
| [**ProcessingErrorData (的事件)**](eventschema-processingerrordata-eventtype-element.md)               | 包含嘗試呈現事件時所發生之錯誤的詳細資料。<br/>                                                                                                               |
| [**提供者 (SystemPropertiesType)**](eventschema-provider-systempropertiestype-element.md)               | 識別記錄事件的提供者。<br/>                                                                                                                                              |
| [**提供者 (RenderingInfoType)**](eventschema-publisher-renderinginfotype-element.md)                    | 提供者的呈現訊息字串。<br/>                                                                                                                                               |
| [**RenderingInfo (的事件)**](eventschema-renderinginfo-eventtype-element.md)                           | 包含事件的已轉譯訊息字串 (包含事件的訊息字串，以及任何事件屬性的訊息字串，例如層級、工作和 opcode) 。<br/>        |
| [**安全性 (SystemPropertiesType)**](eventschema-security-systempropertiestype-element.md)               | 識別記錄事件的使用者。<br/>                                                                                                                                                  |
| [**SequenceNumber (DebugDataType)**](eventschema-sequencenumber-debugdatatype-element.md)                 | 追蹤訊息的本機或全域序號。<br/>                                                                                                                                   |
| [**子元件 (DebugDataType)**](eventschema-subcomponent-debugdatatype-element.md)                     | 指定在 debug 通道的 debug 事件中使用的 SubComponentName WPP debug 追蹤欄位。                                                                                                 |
| [**系統 (的系統事件)**](eventschema-system-eventtype-element.md)                                         | 包含識別提供者及其啟用方式、事件、寫入事件之通道的資訊，以及處理常式和執行緒識別碼之類的系統資訊。<br/> |
| [**Task (RenderingInfoType)**](eventschema-task-renderingtype-element.md)                                 | 事件中指定之工作的轉譯訊息字串。<br/>                                                                                                                             |
| [**Task (SystemPropertiesType)**](eventschema-task-systempropertiestype-element.md)                       | 事件中定義的工作。<br/>                                                                                                                                                              |
| [**TimeCreated (SystemPropertiesType)**](eventschema-timecreated-systempropertiestype-element.md)         | 識別事件記錄時間的時間戳記。<br/>                                                                                                                                   |
| [**UserData (的事件)**](eventschema-userdata-eventtype-element.md)                                     | 包含事件資料。<br/>                                                                                                                                                                    |
| [**版本 (SystemPropertiesType)**](schema-version-systempropertiestype-element.md)                      | 包含事件定義的版本號碼。<br/>                                                                                                                                      |



 

 

