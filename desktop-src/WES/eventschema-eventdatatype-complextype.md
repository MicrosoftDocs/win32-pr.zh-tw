---
title: EventDataType 複雜類型
description: 定義事件資料項目和包含事件資料的結構。
ms.assetid: 9531163f-34ce-4673-b2d8-636042915c73
keywords:
- EventDataType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- EventDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 424f7f5f6472859a06605467c427fc7b9f210a960f0920fb8593778bd757fc06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589021"
---
# <a name="eventdatatype-complex-type"></a>EventDataType 複雜類型

定義事件資料項目和包含事件資料的結構。

``` syntax
<xs:complexType name="EventDataType">
    <xs:sequence>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="Data"
                type="DataType"
             />
            <xs:element name="ComplexData"
                type="ComplexDataType"
             />
        </xs:choice>
        <xs:element name="Binary"
            type="hexBinary"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                              | 類型                                                               | 描述                                                                                          |
|----------------------------------------------------------------------|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**二 進 制**](eventschema-binary-eventdatatype-element.md)           | hexBinary                                                          | 使用 [事件記錄](/windows/desktop/EventLog/event-logging)撰寫之事件的二進位資料 blob。<br/> |
| [**ComplexData**](eventschema-complexdata-eventdatatype-element.md) | [**ComplexDataType**](eventschema-complexdatatype-complextype.md) | 在事件的範本中定義的結構。<br/>                                |
| [**資料**](eventschema-data-eventdatatype-element.md)               | [**資料類型**](eventschema-datafieldtype-complextype.md)          | 在事件的範本中定義的最上層資料項目。<br/>                      |



## <a name="attributes"></a>屬性



| 名稱 | 類型   | 描述                                                       |
|------|--------|-------------------------------------------------------------------|
| 名稱 | 字串 | 包含資料項目的範本名稱。<br/> |



## <a name="remarks"></a>備註

[**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender)函式會以二進位 blob 的形式呈現陣列和結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

