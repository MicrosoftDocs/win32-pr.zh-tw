---
title: RenderingInfoType 複雜類型
description: 定義事件的呈現訊息。
ms.assetid: 85a4cfc6-6277-4af8-af4e-cae3bd3aac13
keywords:
- RenderingInfoType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- RenderingInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d4a70c8bc97abc3dea7cd04e9ce491b64cb62dcc892fcde318d69dcdc996e2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118588461"
---
# <a name="renderinginfotype-complex-type"></a>RenderingInfoType 複雜類型

定義事件的呈現訊息。

``` syntax
<xs:complexType name="RenderingInfoType">
    <xs:sequence>
        <xs:element name="Message"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Level"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Opcode"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Task"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Channel"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Provider"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Keywords"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="Keyword"
                        type="string"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:attribute name="Culture"
        type="language"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                             | 類型   | 描述                                                                   |
|---------------------------------------------------------------------|--------|-------------------------------------------------------------------------------|
| [**通道**](eventschema-task-renderingtype-element.md)           | 字串 | 事件中指定之通道的呈現訊息字串。<br/> |
| [**關鍵字**](eventschema-keyword-keywords-element.md)             | 字串 | 事件中指定之關鍵字的轉譯訊息字串。<br/>   |
| [**關鍵字**](eventschema-keywords-renderingtype-element.md)      |        | 已轉譯關鍵字的清單。<br/>                                       |
| [**水準**](eventschema-level-renderingtype-element.md)            | 字串 | 事件中指定之層級的轉譯訊息字串。<br/>   |
| [**消息**](eventschema-message-renderingtype-element.md)        | 字串 | 事件的呈現訊息字串。<br/>                          |
| [**OpCode**](eventschema-opcode-renderingtype-element.md)          | 字串 | 事件中指定之 opcode 的轉譯訊息字串。<br/>  |
| [**提供者**](eventschema-publisher-renderinginfotype-element.md) | 字串 | 提供者的呈現訊息字串。<br/>                      |
| [**工作**](eventschema-task-renderingtype-element.md)              | 字串 | 事件中指定之工作的轉譯訊息字串。<br/>    |



## <a name="attributes"></a>屬性



| 名稱    | 類型     | 描述                                                                                                      |
|---------|----------|------------------------------------------------------------------------------------------------------------------|
| 文化特性 | 語言 |  (的語言名稱，例如，用來識別用來呈現訊息字串之地區設定的 en-us) 。<br/> |



## <a name="remarks"></a>備註

只有使用[Windows 事件收集器](/windows/desktop/WEC/windows-event-collector)服務所收集的事件才會包含此區段。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

