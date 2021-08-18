---
title: VML OnMouseOver 屬性
description: VML OnMouseOver 屬性
ms.assetid: 68f0fa7a-0d22-4ede-8404-e007296960e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d2bb65864987988996cfad710360fd908a5248c11857e8df1eb5a941b1b895b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999128"
---
# <a name="vml-onmouseover-attribute"></a>VML OnMouseOver 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

觸發圖形的滑鼠事件。 讀取/寫入 **字串**。

**適用於**

[圖形](shape-element--vml.md)

**標記語法**

<v： *element* onmouseover = " *expression* " >

**備註**

當滑鼠指標位於圖形上時，就會產生「已懸停」事件。 值的產生方式是使用關鍵字 **this** (做為物件的參考) 後面接著物件模型語法。 例如，若要將填滿色彩變更為紅色，請使用下列程式：

onmouseover = "this. fillcolor = ' red '"

請注意，使用單引號和雙引號來設定運算式。

*VML 標準屬性*

**範例**

當滑鼠指標位於圖形上時，填滿色彩會從紅色變成綠色。


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20"
   onmouseover='this.fillcolor="green"'>
   </v:rect>
```



[OnMouseOver 屬性範例](/previous-versions/bb264088(v=vs.85))。  (需要 Microsoft Internet Explorer 5 或更高版本。 ) 

 

 