---
title: messageTable (MetadataType) 元素
description: 包含事件檢測資訊清單中繼資料區段中所使用之字串的參考。 這些字串會儲存在一組訊息元素和識別碼一起的識別碼。
ms.assetid: 868af191-0f9c-435b-878f-ef0584e097d1
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
ms.openlocfilehash: f7c614210a22bc6c6d160a7c161c5b5a89aab85116285822465b43ba75e63095
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865658"
---
# <a name="messagetable-metadatatype-element"></a>messageTable (MetadataType) 元素

包含事件檢測資訊清單中繼資料區段中所使用之字串的參考。 這些字串會儲存在一組 [**訊息**](eventmanifestschema-message-messagetable-element.md) 元素和識別碼一起的識別碼。

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

**MessageTable** 元素是由 [**MetadataType**](eventmanifestschema-metadatatype-complextype.md)複雜型別定義。

## <a name="child-elements"></a>子元素



| 元素                                                             | 類型 | 描述                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [**message**](eventmanifestschema-message-messagetable-element.md) |      | 指定資訊清單當地語系化區段中字串的參考。<br/> |



## <a name="attributes"></a>屬性



| 名稱    | 類型   | 描述                                                              |
|---------|--------|--------------------------------------------------------------------------|
| message | 字串 | 字串資料表中當地語系化字串的參考。<br/>      |
| mid     | 字串 | 未使用。<br/>                                                     |
| 符號  | 字串 | 用來參考訊息的符號。<br/>                     |
| value   | 字串 | 要用來做為此訊息之訊息識別碼的數位。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**MetadataType**](eventmanifestschema-metadatatype-complextype.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**中繼資料 (instrumentationManifest)**](eventmanifestschema-metadata-instrumentationmanifest-element.md)
</dt> </dl>

 

 





