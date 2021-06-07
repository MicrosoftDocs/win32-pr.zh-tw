---
description: 包含在筆記本便箋中用於信紙的水平線格式資訊。
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: 水準元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50de08008d0243d27f8a8c5f64d6aeac5ddbcc1c
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432372"
---
# <a name="horizontal-element"></a>水準元素

包含在筆記本便箋中用於信紙的水平線格式資訊。

## <a name="definition"></a>定義

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
```

## <a name="parent-elements"></a>父項目

[**LineLayout**](linelayout-element.md)

## <a name="child-elements"></a>子元素

無。

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
<li>None</li>
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
<td>選用</td>
<td>元素的色彩。</td>
<td>十六進位的 RGB 值。 符合下列正則運算式： # [0-9a-南非-Z] {6} 。 例如，#4a79B5。<br/></td>
</tr>
<tr class="odd">
<td><strong>SpacingBefore</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>選用</td>
<td>元素之前的間距。</td>
<td>任何非負整數。</td>
</tr>
<tr class="even">
<td><strong>SpacingBetween</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>選用</td>
<td>此元素與周圍元素之間的間距。</td>
<td>任何非負整數。</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>項目資訊



|  元素     | 值                                                     |
|--------------|-------------------------------------------------------------------|
| 項目類型 | [**HorizontalType complexType**](horizontaltype-complex-type.md) |
| 命名空間    | urn：架構-microsoft-com：平板電腦： richink                        |
| 結構描述名稱  | 日誌讀者                                                    |



 

 

 




