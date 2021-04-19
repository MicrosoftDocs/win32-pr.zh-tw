---
description: 包含筆記本便箋的標題資訊。
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Title 項目
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2362e286482b329c50788b8eae4b4a30cbd1a125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981214"
---
# <a name="title-element"></a>Title 項目

包含筆記本便箋的標題資訊。

## <a name="definition"></a>定義

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a>父項目

[**信箋**](stationery-element.md)

## <a name="child-elements"></a>子元素

[**TitleArea**](titlearea-element.md)

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
<td><strong>xs:string</strong></td>
<td>必要</td>
<td>指定附注標題周圍的框線類型。</td>
<td><ul>
<li>無</li>
<li>SolidSquare</li>
<li>OutlineSquare</li>
<li>SolidRoundRect</li>
<li>OutlineRoundRect</li>
<li>SolidRoundRectDottedBaseline</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>DateStyle</strong></td>
<td><strong>xs:string</strong></td>
<td>必要</td>
<td>定義標題是否包含日期。</td>
<td><ul>
<li>無</li>
<li>Short</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>色彩</strong></td>
<td><a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a></td>
<td>選擇性</td>
<td>指定背景的色彩。</td>
<td>請參閱 <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>。</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>項目資訊



|              |                                                         |
|--------------|---------------------------------------------------------|
| 項目類型 | [**TitleType**](titletype-complex-type.md) complexType |
| 命名空間    | urn：架構-microsoft-com：平板電腦： richink              |
| 結構描述名稱  | 日誌讀者                                          |



 

 

 



