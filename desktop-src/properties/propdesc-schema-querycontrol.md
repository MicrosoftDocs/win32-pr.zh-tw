---
description: Windows 7 和更新版本不支援。 指定要在查詢產生器中使用的控制項。
ms.assetid: 7d79c2fe-c63d-4ac5-8dd6-1a6103e53245
title: queryControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f05800fc026c61a4ea50098fb1d8f4deb98d971c9eecfed478d71bd3c01033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823558"
---
# <a name="querycontrol"></a>queryControl

Windows 7 和更新版本不支援。 指定要在查詢產生器中使用的控制項。 每個[displayInfo](./propdesc-schema-displayinfo.md)專案都只能有一個[queryControl]()元素。

如果有多個元素，則會使用最後一個元素。 如果未提供任何 [queryControl]() 元素，則會將預設屬性設定套用至屬性描述。

## <a name="syntax"></a>Syntax


```
<!-- queryControl -->
<xs:element name="queryControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Calendar"/>
                    <xs:enumeration value="CheckboxDropList"/>
                    <xs:enumeration value="DropList"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="NumericText"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Text"/>
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
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>預設</td>
<td>預設值。 根據屬性使用預設控制項 <typeInfo type=&quot;&quot;> 。 預設類型如下所示。 任何其他類型都會導致使用 &quot; 文字 &quot; 控制項。 
<table>
<thead>
<tr class="header">
<th>ConditionType</th>
<th>控制</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>String</td>
<td>Text</td>
</tr>
<tr class="even">
<td>字串 (多重值) </td>
<td>MultiValueText</td>
</tr>
<tr class="odd">
<td>數位或大小</td>
<td>NumericText</td>
</tr>
<tr class="even">
<td> (列舉) 的數目或大小</td>
<td>List</td>
</tr>
<tr class="odd">
<td>Datetime</td>
<td>Calendar</td>
</tr>
<tr class="even">
<td>布林值</td>
<td>布林值</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>布林值</td>
<td>使用布林值控制項。</td>
</tr>
<tr class="odd">
<td>Calendar</td>
<td>使用下拉式月曆控制項。</td>
</tr>
<tr class="even">
<td>CheckboxDropList</td>
<td>使用具有核取方塊的清單控制項。</td>
</tr>
<tr class="odd">
<td>DropList</td>
<td>使用下拉式清單控制項。</td>
</tr>
<tr class="even">
<td>MultiValueText</td>
<td>使用多重值的文字編輯控制項。</td>
</tr>
<tr class="odd">
<td>NumericText</td>
<td>使用數值文字編輯控制項。</td>
</tr>
<tr class="even">
<td>分級</td>
<td>使用5顆星的評等控制項。</td>
</tr>
<tr class="odd">
<td>Text</td>
<td>使用文字編輯控制項。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
