---
description: 指定 IPropertyDescription：： FormatForDisplay 應該如何將 booleanFormat 屬性的值格式化為字串。
ms.assetid: f6384910-4411-4ac2-884d-3476c1b6ff96
title: booleanFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9df8c7d2a72f7229c99fb13244aae2b6bc1d4ec63c272f10aa2d35a81740f5d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460048"
---
# <a name="booleanformat"></a>booleanFormat

指定 [**IPropertyDescription：： FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) 應該如何將屬性的值格式化為字串。 這僅適用于 <displayInfo displayType="String"> 。 每個[displayInfo](./propdesc-schema-displayinfo.md)專案都只能有一個[booleanFormat]()元素。

如果有多個元素，則會使用最後一個元素。 如果未提供任何 [booleanFormat]() 元素，則會將預設屬性設定套用至屬性描述。

## <a name="syntax"></a>Syntax


```
      <!-- booleanFormat -->
      <xs:element name="booleanFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="YesNo"/>
                <xs:enumeration value="OnOff"/>
                <xs:enumeration value="TrueFalse"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a>項目資訊



| Parent 項目                                   | 子元素 |
|--------------------------------------------------|----------------|
| [displayInfo](./propdesc-schema-displayinfo.md) | 無           |



 

## <a name="attributes"></a>屬性



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>屬性</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>formatAs</td>
<td>公用。 選擇性。 預設值為 &quot; YesNo &quot; 。 以下是有效的值。 
<table>
<thead>
<tr class="header">
<th>值</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>YesNo</td>
<td>預設值。 將值格式化為 &quot; [是] &quot; 或 [否] &quot; &quot; 。 要求屬性類型必須是布林值。</td>
</tr>
<tr class="even">
<td>OnOff</td>
<td>將值格式化為 &quot; On &quot; 或 &quot; Off &quot; 。 要求屬性類型必須是布林值。</td>
</tr>
<tr class="odd">
<td>TrueFalse</td>
<td>將值格式化為 &quot; True &quot; 或 &quot; False &quot; 。 要求屬性類型必須是布林值。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
