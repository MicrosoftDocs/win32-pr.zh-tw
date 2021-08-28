---
description: 指定 IPropertyDescription：： FormatForDisplay 應該如何將屬性的值格式化為字串。 這僅適用于 <displayInfo displayType=&\#0034;Number&\#0034;> 。
ms.assetid: 9e8cfe5c-e17a-40d6-958f-a1bd1130c699
title: '>cultureinfo.numberformat'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6601e6647d8fa1ac8b8cb262d47192810583c93f
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622684"
---
# <a name="numberformat"></a>>cultureinfo.numberformat

指定 [**IPropertyDescription：： FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) 應該如何將屬性的值格式化為字串。 這僅適用于 <displayInfo displayType="Number"> 。 每個[displayInfo](./propdesc-schema-displayinfo.md)專案都只能有一個[>cultureinfo.numberformat]()元素。

如果有多個元素，則會使用最後一個元素。 如果未提供任何 [>cultureinfo.numberformat]() 元素，則會將預設屬性設定套用至屬性描述。

## <a name="syntax"></a>Syntax


```
      <!-- numberFormat -->
      <xs:element name="numberFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="General"/>
                <xs:enumeration value="Percentage"/>
                <xs:enumeration value="ByteSize"/>
                <xs:enumeration value="KBSize"/>
                <xs:enumeration value="SampleSize"/>
                <xs:enumeration value="Bitrate"/>
                <xs:enumeration value="SampleRate"/>
                <xs:enumeration value="FrameRate"/>
                <xs:enumeration value="Pixels"/>
                <xs:enumeration value="DPI"/>
                <xs:enumeration value="Duration"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatDurationAs">
              <xs:restriction base="xs:string">
                <xs:enumeration value="hh:mm"/>
                <xs:enumeration value="hh:mm:ss"/>
                <xs:enumeration value="hh:mm:ss.fff"/>
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
<td>formatAs</td>
<td>公用。 選擇性。 預設值為 &quot; [一般] &quot; 。 指定顯示格式。 以下是有效的值。 
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
<td>預設值。 將值顯示為未格式化的數位。</td>
</tr>
<tr class="even">
<td>百分比</td>
<td>將值格式化為百分比。 需要屬性為 UInt32。</td>
</tr>
<tr class="odd">
<td>ByteSize</td>
<td>適當地將值格式化為位元組、 &quot; KB &quot; 、 &quot; MB &quot; 或 &quot; GB &quot; 。 要求屬性必須是 UInt64。</td>
</tr>
<tr class="even">
<td>KBSize</td>
<td>&quot; &quot; 不論值為何，都會將值格式化為 KB。 要求屬性必須是 UInt64。</td>
</tr>
<tr class="odd">
<td>SampleSize</td>
<td>將值格式化為位數。 需要屬性為 UInt32。</td>
</tr>
<tr class="even">
<td>位元速率</td>
<td>以 Kbps 為單位格式化值 &quot; &quot; 。 需要屬性為 UInt32。 此值必須以 &quot; 每秒位數的 &quot; 單位儲存。</td>
</tr>
<tr class="odd">
<td>SampleRate</td>
<td>將值格式化為 &quot; KHz &quot; 。 需要屬性為 UInt32。 此值必須以 &quot; 赫茲單位儲存 &quot; 。</td>
</tr>
<tr class="even">
<td>FrameRate</td>
<td>將畫面格/秒的值格式化。 需要屬性為 UInt32。 此值必須以 &quot; 每秒 kb 的 &quot; 單位儲存。</td>
</tr>
<tr class="odd">
<td>阻擋的</td>
<td>以圖元單位格式化值。 需要屬性為 UInt32。</td>
</tr>
<tr class="even">
<td>DPI</td>
<td>將值格式化為每英寸點。 需要屬性為 UInt32。</td>
</tr>
<tr class="odd">
<td>持續時間</td>
<td>將值格式化為持續時間。 使用 <formatDurationAs> 指定持續時間格式。 要求屬性必須是 UInt64。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>formatDurationAs</td>
<td>公用。 選擇性。 預設值為 &quot; hh： mm： ss &quot; 。 只有在<em>formatAs = &quot; Duration &quot; </em>時才適用。 要求屬性必須是 UInt64。 以下是有效的值。 
<table>
<thead>
<tr class="header">
<th>值</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>hh:mm</td>
<td>將值格式化，以小時和分鐘為單位。</td>
</tr>
<tr class="even">
<td>hh:mm:ss</td>
<td>預設值。 以小時、分鐘和秒為單位來格式化值。</td>
</tr>
<tr class="odd">
<td>hh： mm： ss. fff</td>
<td>以小時、分鐘、秒和毫秒為值格式化。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
