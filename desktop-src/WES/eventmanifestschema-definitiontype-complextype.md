---
title: DefinitionType 複雜類型
description: 定義提供者可記錄的事件清單。
ms.assetid: 6d401ced-be1a-409a-8f4d-2d977a33ff8d
keywords:
- DefinitionType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- DefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f62ab040f57fdeb4e4208554c642e9b0bc2fb1135512d1c512f0b0ef90b69e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589633"
---
# <a name="definitiontype-complex-type"></a>DefinitionType 複雜類型

定義提供者可記錄的事件清單。

``` syntax
<xs:complexType name="DefinitionType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="event"
            type="EventDefinitionType"
         />
        <xs:element name="task"
            type="TaskEventDefinitionType"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                           | 類型                                                                                       | 描述                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**事件**](eventmanifestschema-event-definitiontype-element.md) | [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md)         | 定義您的提供者可以記錄的事件。<br/>                                                                                                                                                                                                                                 |
| [**任務**](eventmanifestschema-task-definitiontype-element.md)   | [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) | 不支援。<br/> **Windows Server 2008 和 Windows Vista：** 定義您的提供者可以記錄的工作特定事件。  (從 Windows SDK Windows 7 版隨附的訊息編譯器開始，不再支援工作特定事件。 ) <br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





