---
title: message (messageTable) 元素
description: 包含資訊清單當地語系化區段中之字串的參考。 |message (messageTable) 元素
ms.assetid: 0988cf99-c7e1-446b-869e-9ac4a0976ac5
keywords:
- message 元素 EventLog
topic_type:
- apiref
api_name:
- message
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79020fa18717a3a2338a8ac243bb95e0fa14de47f0e434fb52c475c956afa101
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865668"
---
# <a name="message-messagetable-element"></a>message (messageTable) 元素

包含資訊清單當地語系化區段中之字串的參考。

``` syntax
<xs:element name="message">
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
```

**Message** 元素是由 [**messageTable**](eventmanifestschema-messagetable-instrumentationtype-element.md)元素所定義。

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

[**messageTable (EventsType)**](eventmanifestschema-messagetable-instrumentationtype-element.md)
</dt> <dt>

[**messageTable (MetadataType)**](eventmanifestschema-messagetable-metadatatype-element.md)
</dt> </dl>

 

 





