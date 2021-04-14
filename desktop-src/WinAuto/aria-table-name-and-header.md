---
title: ARIA 資料表錯誤
description: ARIA 資料表錯誤
ms.assetid: 3D0448BB-50DC-4C85-93BD-D8E626475AB0
keywords:
- AriaDataTableErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3286f88a0b3a0d962fd6ac45581f94bc351cb507
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383102"
---
# <a name="aria-data-table-error"></a>ARIA 資料表錯誤

## <a name="text"></a>Text

資料表包含資料，但沒有透過 **aria 標籤**、 **aria-labelledby**、 **title**、 **caption** 或 **th** 元素所定義的可存取標記。

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

此錯誤適用于具有一個以上資料格的 HTML 資料表。 此錯誤不會套用至資料表， `role="presentation"` 因為這些會被視為版面配置資料表。

此錯誤表示資料表格沒有可存取的名稱或標頭資訊。

若要修正這個錯誤，請使用 [**CAPTION**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) 標記或 [**aria labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)、 [**aria 標籤**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)或 [**標題**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) 屬性來定義可存取的名稱。 如果資料表缺少標頭資訊，請使用 [**THead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) 標記來標示標頭儲存格。

## <a name="example"></a>範例


```HTML
<!-- Data tables must contain an accessibile name and header information. -->
<table>
  <caption>ARIA Examples</caption>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      ...
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>Accessible tables</td>
      <td>This example illustrates how to make data tables accessible using ARIA</td>
      ...
    </tr>
  </tbody>
</table>
```



 

 




