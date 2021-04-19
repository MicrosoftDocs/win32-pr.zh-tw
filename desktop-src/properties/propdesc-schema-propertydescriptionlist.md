---
description: 一個或多個個別 propertyDescription 元素的容器。
ms.assetid: b54aaa85-6928-470e-9630-44b094205106
title: propertyDescriptionList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cd0beaf4dbbd8b71c7f4b3335c169754c704d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982346"
---
# <a name="propertydescriptionlist"></a>propertyDescriptionList

一個或多個個別 [propertyDescription](./propdesc-schema-propertydescription.md) 元素的容器。 Propdesc 屬性描述架構檔案至少應包含一個 [propertyDescriptionList]() 元素。

## <a name="syntax"></a>Syntax


```
<!-- propertyDescriptionList -->
<xs:element name="propertyDescriptionList">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="s:propertyDescription" minOccurs="1" maxOccurs="unbounded"/>
        </xs:sequence>
        <xs:attribute name="publisher" type="xs:string" use="required"/>
        <xs:attribute name="product"   type="xs:string" use="required"/>
    </xs:complexType>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_formatid_and_propid">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@formatID"/>
        <xs:field    xpath="@propID"/>
    </xs:unique>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_canonical_name">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@name"/>
    </xs:unique>
</xs:element>
```



## <a name="element-information"></a>項目資訊



| Parent 項目                        | 子元素                                                   |
|---------------------------------------|------------------------------------------------------------------|
| [schema](./propdesc-schema-entry.md) | [propertyDescription](./propdesc-schema-propertydescription.md) |



 

## <a name="attributes"></a>屬性



| 屬性 | 描述                                                               |
|-----------|---------------------------------------------------------------------------|
| publisher | 公用。 必要。 提供架構之發行者的顯示名稱。 |
| product   | 公用。 必要。 提供架構的產品顯示名稱。   |



 

## <a name="remarks"></a>備註

[PropertyDescriptionList]()不應該與「屬性清單」和 [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist)（完全分開）混淆。

 

 
