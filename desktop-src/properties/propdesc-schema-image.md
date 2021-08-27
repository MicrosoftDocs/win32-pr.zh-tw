---
description: image
ms.assetid: 89893C4E-4F4E-4d85-9623-08607B4383E5
title: '影像元素 (屬性描述架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39145ebf4db2bab4ffffeeec31db15e26a881a5bf63b752096a5732522ff8d9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011498"
---
# <a name="image"></a>image

每個父元素只能有一個 [image]() 元素。

## <a name="syntax"></a>Syntax


```
<!-- image -->
<xs:element name="image">
    <xs:complexType>
        <xs:attribute name="res" use="required">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:maxLength value="260"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>項目資訊



| 父項目                                                                  | 子元素 |
|----------------------------------------------------------------------------------|----------------|
| [enum](./propdesc-schema-enum.md)、 [enumRange](./propdesc-schema-enumrange.md) | 無           |



 

## <a name="attributes"></a>屬性



| 屬性 | 描述       |
|-----------|-------------------|
| res       | 公用。 必要。 |



 

 

 
