---
title: 資源 (LocalizationType) 元素
description: 定義字串資料表的群組，其中包含您在資訊清單中參考的當地語系化字串。
ms.assetid: b984894a-0ae8-49be-af93-3acdcce53ee9
keywords:
- resources 元素 EventLog
topic_type:
- apiref
api_name:
- resources
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3075b2b1741079f80c34e5acf9783b13b74b6973c1d16f2cd323890bcea5d0d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120575"
---
# <a name="resources-localizationtype-element"></a>資源 (LocalizationType) 元素

定義字串資料表的群組，其中包含您在資訊清單中參考的當地語系化字串。

``` syntax
<xs:element name="resources">
    <xs:complexType>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="stringTable"
                type="StringTableType"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                namespace="##other"
             />
        </xs:choice>
        <xs:attribute name="culture"
            type="string"
            default="##fallback"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

**Resources** 元素是由 [**LocalizationType**](eventmanifestschema-localizationtype-complextype.md)複雜型別定義。

## <a name="child-elements"></a>子元素



| 元素                                                                  | 類型                                                                       | 描述                                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**stringTable**](eventmanifestschema-stringtable-resources-element.md) | [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) | 定義您可以在資訊清單中參考的當地語系化字串清單。<br/> |



## <a name="attributes"></a>屬性



| 名稱    | 類型   | 描述                                                                                                                                            |
|---------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| culture | 字串 | 用來識別字串資料表中當地語系化字串文化特性的語言名稱。 例如，"en-us" 代表英文 (美國) 。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**父元素**
</dt> <dt>

[**當地語系化 (instrumentationManifest)**](eventmanifestschema-localization-instrumentationmanifest-element.md)
</dt> </dl>

 

 





