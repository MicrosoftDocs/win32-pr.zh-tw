---
title: LocalizationType 複雜類型
description: 定義您在資訊清單中參考的當地語系化資源群組。 |LocalizationType 複雜類型
ms.assetid: fecab4e0-7136-4b13-8c24-bebbad0812e6
keywords:
- LocalizationType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- LocalizationType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 09a596ff981944943c193fb158f14aa04eafb0b0b3d4df660d2034c5b5d281be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055946"
---
# <a name="localizationtype-complex-type"></a>LocalizationType 複雜類型

定義您在資訊清單中參考的當地語系化資源群組。

``` syntax
<xs:complexType name="LocalizationType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="resources">
            <xs:complexType>
                <xs:choice
                    minOccurs="0"
                    maxOccurs="unbounded"
                >
                    <xs:element name="stringTable"
                        type="StringTableType"
                     />
                </xs:choice>
                <xs:attribute name="culture"
                    type="string"
                    use="required"
                 />
                <xs:anyAttribute
                    processContents="lax"
                    namespace="##other"
                 />
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            namespace="##other"
         />
    </xs:choice>
    <xs:attribute name="fallbackCulture"
        type="string"
        default="en-us"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                         | 類型                                                                       | 描述                                                                                                         |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**資源**](eventmanifestschema-resources-localizationtype-element.md)     |                                                                            | 定義字串資料表的群組，其中包含您在資訊清單中參考的當地語系化字串。<br/> |
| [**stringTable**](eventmanifestschema-stringtable-localizationtype-element.md) | [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) | 定義您可以在資訊清單中參考的當地語系化字串清單。<br/>                             |



## <a name="attributes"></a>屬性



| 名稱            | 類型   | 描述                                                                                                                                            |
|-----------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| culture         | 字串 | 用來識別字串資料表中當地語系化字串文化特性的語言名稱。 例如，"en-us" 代表英文 (美國) 。<br/> |
| fallbackCulture | 字串 | 未使用。<br/>                                                                                                                                   |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





