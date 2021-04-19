---
title: TaskEventDefinitionType 複雜類型
description: 定義您的提供者可以記錄的工作特定事件。 |TaskEventDefinitionType 複雜類型
ms.assetid: f0329728-e7b5-4161-a30f-78b81a7b6812
keywords:
- TaskEventDefinitionType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- TaskEventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2ebf752dbaf97ceced84b6bd9698faf7b191c07e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106997352"
---
# <a name="taskeventdefinitiontype-complex-type"></a>TaskEventDefinitionType 複雜類型

\[從 Windows 7 版 Windows SDK 隨附的訊息編譯器開始，就無法再使用 TaskEventDefinitionType 複雜類型。 相反地，請使用工作特定的作業碼來提供相同的功能。\]

定義您的提供者可以記錄的工作特定事件。

``` syntax
<xs:complexType name="TaskEventDefinitionType">
    <xs:sequence>
        <xs:element name="opcode"
            maxOccurs="unbounded"
        >
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
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                      | 類型                                                                               | Description                                             |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------|
| **event**                                                                    | [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md) | 以工作發佈的工作特定事件。<br/> |
| [**opcode**](eventmanifestschema-opcode-taskeventdefinitiontype-element.md) |                                                                                    | 適用于事件的工作特定作業碼。 <br/>   |



## <a name="attributes"></a>屬性



| 名稱 | 類型      | 描述                                      |
|------|-----------|--------------------------------------------------|
| NAME | **QName** | 工作特定作業碼的名稱。<br/> |
| NAME | anyURI    | 工作的名稱。<br/>                 |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





