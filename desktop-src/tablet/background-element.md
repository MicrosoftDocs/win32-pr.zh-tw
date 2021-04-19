---
description: 包含 JournalDocument 元素或 JournalPage 元素的背景。
ms.assetid: 48527c4e-50fb-4800-ac87-1646234783ba
title: Background 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e58a836c7cfd13130779c1cd6b017105bcaa6321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980418"
---
# <a name="background-element"></a>Background 元素

包含 [**JournalDocument**](journaldocument-element.md) 元素或 [**JournalPage**](journalpage-element.md) 元素的背景。

## <a name="definition"></a>定義

``` syntax
<xs:element name="Background" type="BackgroundType" minOccurs="0" />
```

## <a name="parent-elements"></a>父項目

[**信箋**](stationery-element.md)

## <a name="child-elements"></a>子元素

[**Image**](image-element.md)

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
<td>指定背景的樣式。</td>
<td><ul>
<li>無</li>
<li>實線</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>色彩</strong></td>
<td><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</td>
<td>選擇性</td>
<td>指定背景的色彩。</td>
<td>請參閱 <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType。</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>項目資訊



|              |                                                                   |
|--------------|-------------------------------------------------------------------|
| 項目類型 | [**BackgroundType**](backgroundtype-complex-type.md) complexType |
| 命名空間    | urn：架構-microsoft-com：平板電腦： richink                        |
| 結構描述名稱  | 日誌讀者                                                    |



 

 

 



