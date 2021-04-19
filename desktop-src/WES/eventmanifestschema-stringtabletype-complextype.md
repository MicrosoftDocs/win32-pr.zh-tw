---
title: StringTableType 複雜類型
description: 定義您可以在資訊清單中參考的當地語系化字串清單。 |StringTableType 複雜類型
ms.assetid: 47a59ff7-aaf6-4200-805b-0a8b5f57f101
keywords:
- StringTableType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- StringTableType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9964c51524f7401afdfdd8a2da10cf43326bcae
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106981787"
---
# <a name="stringtabletype-complex-type"></a>StringTableType 複雜類型

定義您可以在資訊清單中參考的當地語系化字串清單。

``` syntax
<xs:complexType name="StringTableType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="string">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="id"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="value"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="stringType"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
    </xs:choice>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                              | 類型 | Description                            |
|----------------------------------------------------------------------|------|----------------------------------------|
| [**字串**](eventmanifestschema-string-stringtabletype-element.md) |      | 定義當地語系化的字串。<br/> |



## <a name="attributes"></a>屬性



| 名稱       | 類型   | 描述                                                                                                              |
|------------|--------|--------------------------------------------------------------------------------------------------------------------------|
| id         | 字串 | 唯一識別字串資料表內之字串的識別碼。 例如，「印表機連接」。<br/> |
| stringType | 字串 | 未使用。<br/>                                                                                                     |
| value      | 字串 | 當地語系化字串。<br/>                                                                                         |



## <a name="remarks"></a>備註

您可以參考任何包含 message 屬性之資訊清單類型的字串。 若要參考 stringType 為 "string" 且識別碼為 "Printer" 的字串，請使用 $ (字串。[連接) ] 作為 [訊息屬性] 的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





