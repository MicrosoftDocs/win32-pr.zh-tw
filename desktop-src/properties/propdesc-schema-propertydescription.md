---
description: 描述單一唯一的標準屬性。
ms.assetid: 1a36ec83-5d8a-4fc5-be3d-a8c2f0983057
title: propertyDescription
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233f6d9b1242a9f02b2edbb2bb29cefaef625c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943853"
---
# <a name="propertydescription"></a>propertyDescription

描述單一唯一的標準屬性。 要在系統中使用的每個這類屬性都必須有對應的 [propertyDescription]() 元素。

## <a name="syntax-for-windows-7"></a>Windows 7 的語法


```
<!-- propertyDescription for Windows 7-->
<xs:element name="propertyDescription">
    <xs:complexType>
        <xs:all>
            <xs:element ref="searchInfo"          minOccurs="0" maxOccurs="1"/>
            <xs:element ref="labelInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="typeInfo"            minOccurs="0" maxOccurs="1"/>
            <xs:element ref="aliasInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="displayInfo"         minOccurs="0" maxOccurs="1"/>
            <xs:element ref="relatedPropertyInfo" minOccurs="0" maxOccurs="1"/>
        </xs:all>

        <xs:attribute name="formatID"  type="uuid" use="required"/>
        <xs:attribute name="propID"    type="propid" use="required"/>
        <xs:attribute name="name"      type="canonical-name"        use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="syntax-for-vista"></a>Vista 的語法


```
<!-- propertyDescription for Windows Vista-->
<xs:element name="propertyDescription">
    <xs:complexType>
        <xs:all>
            <xs:element ref="searchInfo"          minOccurs="0" maxOccurs="1"/>
            <xs:element ref="labelInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="typeInfo"            minOccurs="0" maxOccurs="1"/>
            <xs:element ref="aliasInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="displayInfo"         minOccurs="0" maxOccurs="1"/>
        </xs:all>

        <xs:attribute name="formatID"  type="uuid" use="required"/>
        <xs:attribute name="propID"    type="xs:nonNegativeInteger" use="required"/>
        <xs:attribute name="name"      type="canonical-name"        use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>項目資訊



| Parent 項目                                                           | 子元素                                                   |
|--------------------------------------------------------------------------|------------------------------------------------------------------|
| [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) | [searchInfo](./propdesc-schema-searchinfo.md)                   |
|                                                                          | [labelInfo](./propdesc-schema-labelinfo.md)                     |
|                                                                          | [typeInfo](./propdesc-schema-typeinfo.md)                       |
|                                                                          | [System.management.automation.aliasinfo](./propdesc-schema-aliasinfo.md)                     |
|                                                                          | [displayInfo](./propdesc-schema-displayinfo.md)                 |
|                                                                          | [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) |



 

## <a name="attributes"></a>屬性



| 屬性 | 描述                                                                                                                                                                                                                                                                                                                                                                         |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NAME      | 必要。 標準屬性名稱，對系統而言是唯一的;例如， `System.Rating` 。 這個字串的型別是標準型別，而且限制為64個字元。 名稱區分大小寫，而且應該使用下列語法： PropertyName。 [**IPropertyDescription：： GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname) 會傳回這個值。 |
| formatID  | 必要。 屬性的格式識別碼 (FMTID) 。 值必須包含括住的括弧;例如， `{64440492-4C8B-11D1-8B70-080036B11A03}` 。 [**IPropertyDescription：： GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) 會傳回這個值。                                                                                                                       |
| propID    | 必要。 屬性識別碼 (PID) ;例如， `9` 。 [**IPropertyDescription：： GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) 會傳回這個值。 此值必須大於或等於2。 值0和1是由系統所保留。                                                                                                                  |



 

 

 
