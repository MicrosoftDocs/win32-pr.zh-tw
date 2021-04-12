---
description: 指定 IPropertyDescription：： FormatForDisplay 應該如何將屬性的值格式化為字串。 這僅適用于 <displayInfo displayType=&\#0034;DateTime&\#0034;> 。
ms.assetid: c290fb2e-ef5b-4dea-ba42-7c9e273a89dc
title: dateTimeFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 091898f77f4dcc37bbe65515f8606104a4d968bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192143"
---
# <a name="datetimeformat"></a>dateTimeFormat

指定 [**IPropertyDescription：： FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) 應該如何將屬性的值格式化為字串。 這僅適用于 <displayInfo displayType="DateTime"> 。 每個[displayInfo](./propdesc-schema-displayinfo.md)專案都只能有一個[dateTimeFormat]()元素。

如果有多個元素，則會使用最後一個元素。 如果未提供任何 [dateTimeFormat]() 元素，則會將預設屬性設定套用至屬性描述。

## <a name="syntax"></a>Syntax


```
      <!-- dateTimeFormat -->
      <xs:element name="dateTimeFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="General"/>
                <xs:enumeration value="Month"/>
                <xs:enumeration value="YearMonth"/>
                <xs:enumeration value="Year"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatTimeAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="ShortTime"/>
                <xs:enumeration value="LongTime"/>
                <xs:enumeration value="HideTime"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatDateAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="ShortDate"/>
                <xs:enumeration value="LongDate"/>
                <xs:enumeration value="HideDate"/>
                <xs:enumeration value="RelativeShortDate"/>
                <xs:enumeration value="RelativeLongDate"/>
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
<td>預設值。 使用 <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shformatdatetimea"><strong>SHFormatDateTime</strong></a>格式化日期時間值。 您可以使用 <em>formatTimeAs</em> 和 <em>formatDateAs</em> 屬性來指定時間和日期的格式。 需要屬性類型為 DateTime。</td>
</tr>
<tr class="even">
<td>Month</td>
<td>將值格式化為年份的其中一個月份。 要求屬性類型必須是 Int32。 值必須儲存為數值，1代表當年的第一個月。</td>
</tr>
<tr class="odd">
<td>YearMonth</td>
<td>將值格式化為 &quot; 年月 &quot; 。 要求屬性類型必須是 Int32。 您必須儲存此值，讓兩個最高的位元組指定年份，而較低的兩個位元組指定月份。</td>
</tr>
<tr class="even">
<td>Year</td>
<td>將值格式化為簡單字串。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>formatTimeAs</td>
<td>公用。 選擇性。 預設值為 &quot; ShortTime &quot; 。 指定要在其中顯示時間的格式。 適用于<strong>formatAs = &quot; General &quot; </strong>。 以下是有效的值。 
<table>
<thead>
<tr class="header">
<th>值</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ShortTime</td>
<td>預設值。 顯示如下的時間 &quot; ：下午 7:48 &quot; 。</td>
</tr>
<tr class="even">
<td>長期</td>
<td>顯示如下的時間 &quot; ：下午 7:48:33 &quot; 。</td>
</tr>
<tr class="odd">
<td>HideTime</td>
<td>不要顯示日期的時間部分。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>formatDateAs</td>
<td>公用。 選擇性。 預設值為 &quot; >shortdate &quot; 。 指定要在其中顯示日期的格式。 適用于<strong>formatAs = &quot; General &quot; </strong>。 以下是有效的值。 
<table>
<thead>
<tr class="header">
<th>值</th>
<th>範例</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>>shortdate</td>
<td>預設值。 顯示日期，例如 &quot; 5/13/59 &quot; 。</td>
</tr>
<tr class="even">
<td>>longdate</td>
<td>顯示日期，例如 &quot; 星期三、5月13日、1959 &quot; 。</td>
</tr>
<tr class="odd">
<td>HideDate</td>
<td>不要顯示日期部分。</td>
</tr>
<tr class="even">
<td>RelativeShortDate</td>
<td>顯示日期（如 &quot; >shortdate &quot; ），但盡可能使用相對描述（例如 &quot; 昨天 &quot; ）。</td>
</tr>
<tr class="odd">
<td>RelativeLongDate</td>
<td>顯示日期（如 &quot; >longdate &quot; ），但盡可能使用相對描述（例如 &quot; 昨天 &quot; ）。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
