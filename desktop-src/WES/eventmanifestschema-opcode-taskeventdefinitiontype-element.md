---
title: opcode (TaskEventDefinitionType) 元素
description: 包含事件的工作特定作業碼。 所有的 opcode 定義都假設為包含事件定義之工作的特定工作。
ms.assetid: c7192772-401b-4602-918d-0e0bc4b65ca7
keywords:
- opcode 元素 EventLog
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f3923e0a42375ac7d926d418943af81cc0264e111e6bdc4be56919780dfacf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652148"
---
# <a name="opcode-taskeventdefinitiontype-element"></a>opcode (TaskEventDefinitionType) 元素

\[從 Windows SDK Windows 7 版隨附的訊息編譯器開始，此專案已無法再使用。\]

包含事件的工作特定作業碼。 所有的 opcode 定義都假設為包含事件定義之工作的特定工作。

``` syntax
<xs:element name="opcode">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="event"
                type="EventDefinitionType"
                maxOccurs="unbounded"
             />
        </xs:sequence>
        <xs:attribute name="name"
            type="QName"
            use="required"
         />
    </xs:complexType>
</xs:element>
```

**Opcode** 元素是由 [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md)複雜型別定義。

## <a name="child-elements"></a>子元素



| 元素                                                   | 類型                                                                               | 描述                                        |
|-----------------------------------------------------------|------------------------------------------------------------------------------------|----------------------------------------------------|
| [**事件**](eventmanifestschema-event-opcode-element.md) | [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md) | 與工作一起發行的事件。<br/> |



## <a name="attributes"></a>屬性



| 名稱 | 類型      | 描述                                      |
|------|-----------|--------------------------------------------------|
| NAME | **QName** | 工作特定作業碼的名稱。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**父元素**
</dt> <dt>

[**task (DefinitionType)**](eventmanifestschema-task-definitiontype-element.md)
</dt> </dl>

 

 





