---
description: 用來將列舉的文字指派給離散值。
ms.assetid: c8cc040e-fcce-43a0-98c1-db2b2c616ac3
title: 列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1336a690fe7ac1e19a8606912a4f7d538d3842ab6a490d17b89f90f64bbfbc13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118970977"
---
# <a name="enum"></a>列舉

用來將列舉的文字指派給離散值。 這些元素的任意數目可能會存在於 [enumeratedList](./propdesc-schema-enumeratedlist.md)下。 以程式設計的方式，這些會表示為 IPropertyEnumType 物件，其 [**IPropertyEnumType：： GetEnumType**](/windows/win32/api/propsys/nf-propsys-ipropertyenumtype-getenumtype) 方法會傳回寵物 \_ DISCRETEVALUE。

## <a name="syntax"></a>Syntax


```
<!-- enum -->
<xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="image" minOccurs="0" maxOccurs="1"/>
        </xs:sequence>
        <xs:attribute name="value" type="xs:string" use="required"/>
        <xs:attribute name="text" type="xs:string" use="required"/>
        <xs:attribute name="mnemonics" type="xs:string"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>項目資訊



| Parent 項目                                         | 子元素 |
|--------------------------------------------------------|----------------|
| [enumeratedList](./propdesc-schema-enumeratedlist.md) | 無           |



 

## <a name="attributes"></a>屬性



| 屬性 | 描述                                                                                                                                                                                                          |
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| value     | 公用。 必要。 要指派列舉文字給的離散值 (字串或數位) 。                                                                                                                           |
| text      | 公用。 必要。 用來顯示列舉值的文字。 語法允許直接顯示字串或間接顯示字串參考;使用間接顯示字串，使其可以當地語系化。 |
| 助憶鍵 | **Windows 7 和更新版本。** 公用。 選擇性。 助憶鍵值的清單，可用來參考搜尋查詢中的屬性。 此清單以 ' \| ' 字元分隔。                                     |



 

 

 
