---
description: .
ms.assetid: 89893C4E-4F4E-4d85-9623-08607B4383E5
title: '影像元素 (屬性描述架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7bb519d5f8104d114734e1f12676f213312e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969293"
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



 

 

 
