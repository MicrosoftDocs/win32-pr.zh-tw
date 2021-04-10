---
description: 指定只顯示內容時要使用的控制項。
ms.assetid: 0fb8afc4-d16b-4c2e-80b3-da9935b11bb5
title: drawControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5318fdebc995ff45932f75b4000ceda6e74068e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026520"
---
# <a name="drawcontrol"></a>drawControl

指定只顯示內容時要使用的控制項。 每個[displayInfo](./propdesc-schema-displayinfo.md)專案都只能有一個[drawControl]()元素。

如果有多個元素，則會使用最後一個元素。 如果未提供任何 [drawControl]() 元素，則會將預設屬性設定套用至屬性描述。

這種形式的控制項不允許編輯屬性。

## <a name="syntax"></a>Syntax


```
<!-- drawControl -->
<xs:element name="drawControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="MultiLineText"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="PercentBar"/>
                    <xs:enumeration value="ProgressBar"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="StaticText"/>
                    <xs:enumeration value="IconList"/>
                    <xs:enumeration value="BooleanCheckMark"/>
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
<td>控制</td>
<td>公用。 選擇性。 預設值為預設值 &quot; &quot; 。 以下是有效的值。 
<table>
<thead>
<tr class="header">
<th>值</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>預設</td>
<td>預設值。 根據屬性使用預設控制項 <typeInfo type=&quot;&quot;> 。 預設類型為 &quot; 字串 &quot; (多重值) ，而且預設控制項為 &quot; MultiValueText &quot; 。 任何其他類型都會導致使用 &quot; StaticText &quot; 控制項。</td>
</tr>
<tr class="even">
<td>MultiLineText</td>
<td>使用多行文字控制項。</td>
</tr>
<tr class="odd">
<td>MultiValueText</td>
<td>使用多重值文字控制項。</td>
</tr>
<tr class="even">
<td>PercentBar</td>
<td>使用百分比 bar 控制項。</td>
</tr>
<tr class="odd">
<td>進度列</td>
<td>使用進度列控制項。</td>
</tr>
<tr class="even">
<td>分級</td>
<td>使用5顆星的評等控制項。</td>
</tr>
<tr class="odd">
<td>StaticText</td>
<td>使用 <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay"><strong>IPropertyDescription：： FormatForDisplay</strong></a> 來顯示內容值。</td>
</tr>
<tr class="even">
<td>IconList</td>
<td><strong>Windows 7 和更新版本。</strong> 圖示的列舉。</td>
</tr>
<tr class="odd">
<td>BooleanCheckMark</td>
<td><strong>Windows 7 和更新版本。</strong></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
