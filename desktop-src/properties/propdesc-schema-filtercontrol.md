---
description: 指定要在標頭篩選功能表中使用的控制項。
ms.assetid: a3117e16-20d0-4637-b726-9fa49516ad5c
title: filterControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac7424cf281c08f1d8de87686e95a38be3f4f3a
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627544"
---
# <a name="filtercontrol"></a>filterControl

指定要在標頭篩選功能表中使用的控制項。 每個[displayInfo](./propdesc-schema-displayinfo.md)專案都只能有一個[filterControl]()元素。

如果有多個元素，則會使用最後一個元素。 如果未提供任何 [filterControl]() 元素，則會將預設屬性設定套用至屬性描述。

## <a name="syntax"></a>Syntax


```
      <!-- filterControl -->
      <xs:element name="filterControl"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="control">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="Default"/>
                <xs:enumeration value="Calendar"/>
                <xs:enumeration value="Rating"/>
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
<col  />
<col  />
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
<td>預設值。 根據屬性使用預設控制項 <typeInfo type=&quot;&quot;> 。 預設類型為 &quot; DateTime &quot; ，預設控制項為行事 &quot; 曆 &quot; 。 任何其他類型都不會產生特殊的篩選控制項。</td>
</tr>
<tr class="even">
<td>Calendar</td>
<td>使用行事曆控制項。</td>
</tr>
<tr class="odd">
<td>分級</td>
<td>使用5顆星的評等控制項。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
