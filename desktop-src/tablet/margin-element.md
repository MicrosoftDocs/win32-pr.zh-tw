---
description: 定義在頁面上繪製的邊界線。
ms.assetid: c3047706-affd-4feb-9d48-cfb4c7dd6fa0
title: Margin 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0500d4db165012393cb600c1e118089b68c76695
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195105"
---
# <a name="margin-element"></a>Margin 元素

定義在頁面上繪製的邊界線。

## <a name="definition"></a>定義

``` syntax
<xs:complexType name="MarginType">
   <xs:attribute name="Style" use="required" type="LineLayoutStyleType" />
   <xs:attribute name="Color" type="ColorType" />
   <xs:attribute name="Type" type="MarginTypeType" />
   <xs:attribute name="Spacing" type="xs:positiveInteger" />
</xs:complexType>
```

## <a name="parent-elements"></a>父項目

無。

## <a name="child-elements"></a>子元素

沒有。。

## <a name="attributes"></a>屬性



<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th>屬性</th>
<th>類型</th>
<th>必要</th>
<th>描述</th>
<th>可能的值</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Style</strong></td>
<td><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</td>
<td>必要</td>
<td>指定要繪製的線條類型。</td>
<td><ul>
<li>無</li>
<li>實線</li>
<li>虛線</li>
<li>點</li>
<li>DashDot</li>
<li>DashDotDot</li>
<li>Double</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>色彩</strong></td>
<td><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</td>
<td>選擇性</td>
<td>元素的色彩。</td>
<td>十六進位的 RGB 值。 符合下列正則運算式： # [0-9a-南非-Z] {6} 。 例如，#4a79B5。<br/></td>
</tr>
<tr class="odd">
<td><strong>型別</strong></td>
<td><a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a> simpleType</td>
<td>選擇性</td>
<td>表示左邊界或右邊界。</td>
<td><ul>
<li>Left</li>
<li>Right</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>間距</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>選擇性</td>
<td>頁面邊緣和邊界之間的間距。</td>
<td>任何非負整數。</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>項目資訊



|              |                                                           |
|--------------|-----------------------------------------------------------|
| 項目類型 | [**MarginType**](margintype-complex-type.md) complexType |
| 命名空間    | urn：架構-microsoft-com：平板電腦： richink                |
| 結構描述名稱  | 日誌讀者                                            |



 

 

 




