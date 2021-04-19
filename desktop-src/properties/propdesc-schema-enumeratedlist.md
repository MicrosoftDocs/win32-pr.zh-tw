---
description: 指定 IPropertyDescription：： FormatForDisplay 應該如何將屬性的值格式化為字串。
ms.assetid: 49ba57b8-3e08-425f-98b2-52ed2c41a488
title: enumeratedList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d098b47463b65c483be68eb7750da929df43cee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001718"
---
# <a name="enumeratedlist"></a>enumeratedList

指定 [**IPropertyDescription：： FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) 應該如何將屬性的值格式化為字串。 它也會影響屬性的分組方式，或者，如果 "editControl" 是 listblox，則會顯示要在清單中顯示的值。 這僅適用于 <displayInfo displayType="Enumerated"> 。 每個[displayInfo](./propdesc-schema-displayinfo.md)專案都只能有一個[enumeratedList]()元素。

如果有多個元素，則會使用最後一個元素。 如果未提供任何 [enumeratedList]() 元素，則會將預設屬性設定套用至屬性描述。

## <a name="syntax"></a>Syntax


```
<!-- enumeratedList -->
<xs:element name="enumeratedList"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="value" type="xs:string" use="required"/>
                    <xs:attribute name="text" type="xs:string" use="required"/>
                </xs:complexType>
            </xs:element>
            <xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="minValue" type="xs:integer" use="required"/>
                    <xs:attribute name="setValue" type="xs:integer"/>
                    <xs:attribute name="text" type="xs:string"/>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
        <xs:attribute name="defaultText" type="xs:string"/>
        <xs:attribute name="useValueForDefault" type="xs:boolean"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>項目資訊



| Parent 項目                                   | 子元素                               |
|--------------------------------------------------|----------------------------------------------|
| [displayInfo](./propdesc-schema-displayinfo.md) | [枚舉](./propdesc-schema-enum.md)           |
|                                                  | [enumRange](./propdesc-schema-enumrange.md) |



 

## <a name="attributes"></a>屬性



| 屬性          | 描述                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| defaultText        | 公用。 選擇性。 如果將值指定給 [**IPropertyDescription：： FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) ，但未對應至清單中的其中一個列舉元素，請指定要使用的預設文字。 語法允許直接顯示字串或間接顯示字串參考;使用參考，讓它可以當地語系化。                              |
| useValueForDefault | 公用。 選擇性。 將此值設定為 "true" 會通知 IPropertyDescription：： FormatForDisplay 如果值未對應到清單中的其中一個列舉元素，則會通知 [**：：**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) 使用此值。 若為 **IPropertyDescription：： FormatForDisplay**，將此值設定為 "true" 會優先于設定 "defaultText"。 預設值為 "false"。 |



 

 

 
