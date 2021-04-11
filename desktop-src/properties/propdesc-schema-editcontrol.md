---
description: 指定編輯屬性時所要使用的控制項。
ms.assetid: cef6d76f-664a-4808-a224-e82a5adb2d70
title: editControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 966f9742082fd6b5f939941a956eaae1ac4e427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944328"
---
# <a name="editcontrol"></a>editControl

指定編輯屬性時所要使用的控制項。 每個[displayInfo](./propdesc-schema-displayinfo.md)專案都只能有一個[editControl]()元素。

如果有多個元素，則會使用最後一個元素。 如果未提供任何 [editControl]() 元素，則會將預設屬性設定套用至屬性描述。

如果為 <typeInfo isInnate="true"> ，則會忽略這個元素，因為無法編輯固有屬性。

## <a name="syntax"></a>Syntax


```
<!-- editControl -->
<xs:element name="editControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="Calendar"/>
                    <xs:enumeration value="CheckboxDropList"/>
                    <xs:enumeration value="DropList"/>
                    <xs:enumeration value="MultiLineText"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Text"/>
                    <xs:enumeration value="IconList"/>
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
<th>類型</th>
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
<td>Datetime</td>
<td>Calendar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Calendar</td>
<td>使用行事曆控制項。</td>
</tr>
<tr class="odd">
<td>CheckboxDropList</td>
<td>使用具有核取方塊的清單控制項。</td>
</tr>
<tr class="even">
<td>DropList</td>
<td>使用下拉式清單控制項。</td>
</tr>
<tr class="odd">
<td>MultiLineText</td>
<td>使用多行文字編輯控制項。</td>
</tr>
<tr class="even">
<td>MultiValueText</td>
<td>使用多重值的文字編輯控制項。</td>
</tr>
<tr class="odd">
<td>分級</td>
<td>使用5顆星的評等控制項。</td>
</tr>
<tr class="even">
<td>Text</td>
<td>使用文字編輯控制項。</td>
</tr>
<tr class="odd">
<td>IconList</td>
<td><strong>Windows 7 和更新版本。</strong></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
