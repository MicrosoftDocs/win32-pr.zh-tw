---
title: 'Position 屬性 (圖形)  (VML) '
description: 'Position 屬性 (圖形)  (VML) '
ms.assetid: 64ffe754-298b-4cf1-a236-6a4bdcd27123
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0ffede6653fd865c254392ffbab0bc3feac2f5e0bf51046fc85398306842dfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475072"
---
# <a name="position-attribute-shapevml"></a>Position 屬性 (圖形)  (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義用來放置元素的定位類型。 讀取/寫入 **字串**。

**適用於**

[圖形](shape-element--vml.md)

**標記語法**

<v： *element* style = "position： *expression* " >

**指令碼語法**

*element* . style. position = "*expression*"

*運算式* =*元素*。 style. position

**備註**

**Position** 屬性類似于樣式表單所使用的標準 HTML **Position** 屬性。

數值包括：



| 值    | 描述                                                                                                                                                                                                               |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static   | 預設值。 根據頁面的一般流程來定位元素。 **Top** 和 **Left** 屬性都會被忽略。 如果物件是錨定的，而這只會發生在 Microsoft Word 中，則會使用這個值。 |
| 絕對 | 使用 **Top** 和 **Left** 屬性，以相對於父代的位置來定位元素。 Microsoft Word 和 Microsoft Excel 浮動物件，以及 Microsoft PowerPoint 投影片會使用這個值。                  |
| relative | 根據頁面的一般流程來定位元素，但會使用 **Top** 和 **Left** 屬性。 重迭的元素是由 **Z 索引** 屬性所控管。                       |



 

*VML 標準屬性*

**範例**

矩形的位置會使用 *相對* 樣式來顯示。


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Position 屬性範例](/previous-versions/bb264090(v=vs.85))。  (需要 Microsoft Internet Explorer 5 或更高版本。 ) 

 

 