---
title: xmlType (XmlTypeListType) 元素
description: 定義 XML 類型。
ms.assetid: 4443963f-f47a-4371-87d8-58f508ba15d6
keywords:
- xmlType 元素 EventLog
topic_type:
- apiref
api_name:
- xmlType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5aa37214c5efc0dee9e788ad10ed2f437e3df19f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969780"
---
# <a name="xmltype-xmltypelisttype-element"></a>xmlType (XmlTypeListType) 元素

定義 XML 類型。

``` syntax
<xs:element name="xmlType">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="XmlType"
            >
                <xs:attribute name="name"
                    type="QName"
                    use="required"
                 />
                <xs:attribute name="value"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="symbol"
                    type="string"
                    use="required"
                 />
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

**XmlType** 元素是由 [**XmlTypeListType**](eventmanifestschema-xmltypelisttype-complextype.md)複雜型別定義。

## <a name="attributes"></a>屬性



| 名稱   | 類型      | 描述                                                                                                                                                                                                                                                |
|--------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NAME   | **QName** | 輸出類型的名稱。<br/>                                                                                                                                                                                                                    |
| 符號 | 字串    | 用來參考應用程式中輸出類型的符號。 [**訊息編譯器 (MC.exe)**](message-compiler--mc-exe-.md)會使用符號，在編譯器產生的標頭檔中建立輸出類型的常數。<br/> |
| value  | 字串    | 整數值，可唯一識別您定義之輸出類型清單中的輸出類型。<br/>                                                                                                                                          |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**父元素**
</dt> <dt>

[**xmlTypes (TypeListType)**](eventmanifestschema-xmltypes-typelisttype-element.md)
</dt> </dl>

 

 





