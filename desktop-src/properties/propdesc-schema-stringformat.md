---
description: 指定 IPropertyDescription：： FormatForDisplay 應該如何將 stringFormat 屬性的值格式化為字串。
ms.assetid: 7c38bc15-be86-4260-b2e4-13afc90de6d7
title: stringFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e76c72865c3a0f327657d3d97cda55d57ebae1023793dabcad03db513319c004
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117867454"
---
# <a name="stringformat"></a>stringFormat

指定 [**IPropertyDescription：： FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) 應該如何將屬性的值格式化為字串。 這僅適用于 <displayInfo displayType="String"> 。 每個[displayInfo](./propdesc-schema-displayinfo.md)專案都只能有一個[stringFormat]()元素。

如果有多個元素，則會使用最後一個元素。 如果未提供任何 [stringFormat]() 元素，則會將預設屬性設定套用至屬性描述。

## <a name="syntax"></a>Syntax


```
<!-- stringFormat -->
<xs:element name="stringFormat"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="formatAs">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="FileName"/>
                    <xs:enumeration value="FilePath"/>
                    <xs:enumeration value="Hyperlink"/>
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
<td>公用。 選擇性。 預設值為 &quot; [一般] &quot; 。 以下是有效的值。 
<table>
<thead>
<tr class="header">
<th>值</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>一般</td>
<td>預設值。 以未格式化的字串形式傳回值。</td>
</tr>
<tr class="even">
<td>FileName</td>
<td>將值格式化為檔案名。 根據使用者設定隱藏延伸模組。 要求屬性類型必須是字串。</td>
</tr>
<tr class="odd">
<td>FilePath</td>
<td>將值格式化為檔案路徑。 根據使用者設定隱藏延伸模組。 要求屬性類型必須是字串。</td>
</tr>
<tr class="even">
<td>Hyperlink</td>
<td>將值格式化為超連結。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
