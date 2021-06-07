---
description: 包含日誌頁面的內容。
ms.assetid: 1df78a17-1cd4-4e98-aed1-b09d2b357703
title: Content 元素 [筆記本讀取器]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fec59601a91d63b09c703557b7c6cd28fd11620
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432150"
---
# <a name="content-element-journal-reader"></a>Content 元素 \[ 日誌讀取器\]

包含日誌頁面的內容。

## <a name="definition"></a>定義

``` syntax
<xs:element name="Content" type="ContentType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>父項目

[**JournalPage**](journalpage-element.md)

## <a name="child-elements"></a>子元素

[**GroupNode**](groupnode-element.md)

[**Paragraph**](paragraph-element.md)

[**繪圖**](drawing-element.md)

[**Text**](text-element.md)

[**Image**](image-element.md)

[**旗標**](flag-element.md)

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
<th>PossibleValues</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>類型</strong></td>
<td><a href="contenttype-complex-type.md"><strong>ContentType complexType</strong></a></td>
<td>必要</td>
<td>如果類型為 &quot; 惰性 &quot; ，則無法修改內容。<br/></td>
<td><ul>
<li>正常</li>
<li>惰性</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>項目資訊



|  元素     | 值                                                     |
|--------------|-------------------------------------------------------------|
| 項目類型 | [**ContentType**](contenttype-complex-type.md) complexType |
| 命名空間    | urn：架構-microsoft-com：平板電腦： richink                  |
| 結構描述名稱  | 日誌讀者                                              |



 

 

 




