---
title: 字串 (StringTableType) 元素
description: 定義當地語系化的字串。
ms.assetid: 845476a9-bcf4-4821-824c-06c9a9f64649
keywords:
- string 元素 EventLog
topic_type:
- apiref
api_name:
- string
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 82eae0fa7007790995617b2c26bc5aff2bca720fb689b9ac468ef551d3400e05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136171"
---
# <a name="string-stringtabletype-element"></a>字串 (StringTableType) 元素

定義當地語系化的字串。

``` syntax
<xs:element name="string">
    <xs:complexType>
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
```

**String** 元素是由 [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md)複雜型別定義。

## <a name="attributes"></a>屬性



| 名稱       | 類型   | 描述                                                                           |
|------------|--------|---------------------------------------------------------------------------------------|
| id         | 字串 | 唯一識別字串資料表內之字串的識別碼。<br/> |
| stringType | 字串 | 未使用。<br/>                                                                  |
| value      | 字串 | 當地語系化字串。<br/>                                                      |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**父元素**
</dt> <dt>

[**stringTable (LocalizationType)**](eventmanifestschema-stringtable-localizationtype-element.md)
</dt> </dl>

 

 





