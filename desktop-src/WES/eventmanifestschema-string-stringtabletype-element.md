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
ms.openlocfilehash: c46fc43366d6472e8047b529d847eefd5369c263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934563"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**父元素**
</dt> <dt>

[**stringTable (LocalizationType)**](eventmanifestschema-stringtable-localizationtype-element.md)
</dt> </dl>

 

 





