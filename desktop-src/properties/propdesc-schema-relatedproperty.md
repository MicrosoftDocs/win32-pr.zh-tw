---
description: 適用于 Windows 7 的新。 識別與屬性描述檔案中定義之屬性相關的屬性。
ms.assetid: 30167942-141A-4f37-B019-0811BA654124
title: relatedProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cabde093a47a25834598659d3ad38e0847c1351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318896"
---
# <a name="relatedproperty"></a>relatedProperty

適用于 Windows 7 的新。 識別與屬性描述檔案中定義之屬性相關的屬性。 您可以視需要在[relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md)中有任意數量的[relatedProperty]()元素。

## <a name="syntax"></a>Syntax


```
<!-- relatedPropertyInfo -->
<xs:element name="relatedProperty" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:attribute name="relationshipName" type="canonical-name" use="required"/>
        <xs:attribute name="propertyName" type="canonical-name" use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>項目資訊



| Parent 項目                                                   | 子元素 |
|------------------------------------------------------------------|----------------|
| [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) | 無           |



 

## <a name="attributes"></a>屬性



| 屬性        | 描述                                                        |
|------------------|--------------------------------------------------------------------|
| relationshipName | 公用。 必要。 屬性關聯性的正式名稱。 |
| propertyName     | 公用。 必要。 相關屬性的標準名稱。      |



 

## <a name="remarks"></a>備註

此元素可讓您將一個屬性對應至另一個屬性。 例如，您可以將自訂屬性（StorageCapacity）的文字對應至 [系統]：


```
<!-- relatedPropertyInfo -->
<propertyDescription name="Fabrikam.StorageCapacity" ... >
    ...
    <relatedPropertyInfo>
        <relatedProperty relationshipName="System.RelatedProperty.Text" propertyName="System.Capacity"/>
    </relatedPropertyInfo>
</propertyDescription>
```



 

 
