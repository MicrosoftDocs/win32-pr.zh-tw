---
title: messageTable (EventsType) 元素
description: 包含資訊清單當地語系化區段中之字串的參考。 |messageTable (EventsType) 元素
ms.assetid: 4dcc1afe-8f2b-4baf-b40b-406f60368575
keywords:
- messageTable 元素 EventLog
topic_type:
- apiref
api_name:
- messageTable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5a2bcf374e336047deaa1339ac749fde3fa7c4f27b38e046f6c9bc651c0e0ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120886"
---
# <a name="messagetable-eventstype-element"></a>messageTable (EventsType) 元素

包含資訊清單當地語系化區段中之字串的參考。

``` syntax
<xs:element name="messageTable">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="message"
                minOccurs="0"
                maxOccurs="unbounded"
            >
                <xs:complexType>
                    <xs:attribute name="value"
                        type="string"
                        use="required"
                     />
                    <xs:attribute name="mid"
                        type="string"
                        use="optional"
                     />
                    <xs:attribute name="message"
                        type="string"
                        use="required"
                     />
                    <xs:attribute name="symbol"
                        type="string"
                        use="optional"
                     />
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

**MessageTable** 元素是由 [**EventsType**](eventmanifestschema-eventstype-complextype.md)複雜型別定義。

## <a name="child-elements"></a>子元素



| 元素                                                             | 類型 | 描述                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [**message**](eventmanifestschema-message-messagetable-element.md) |      | 指定資訊清單當地語系化區段中字串的參考。<br/> |



## <a name="attributes"></a>屬性



| 名稱    | 類型   | 描述                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| message | 字串 | 字串資料表中當地語系化字串的參考。<br/>                                |
| mid     | 字串 | 未使用。<br/>                                                                               |
| 符號  | 字串 | 您希望訊息編譯器為此訊息字串建立的符號名稱。<br/> |
| value   | 字串 | 要用來做為此訊息之訊息識別碼的數位。<br/>                           |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**父元素**
</dt> <dt>

[**事件 (Instrumentationtype.event) 元素**](eventmanifestschema-events-instrumentationtype-element.md)
</dt> </dl>

 

 





