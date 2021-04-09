---
title: VML 類別屬性
description: VML 類別屬性
ms.assetid: 4030b8b7-fcc9-4153-8004-81935a347a09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94bdc723ba9be335afc43023ab89b88834c55474
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933403"
---
# <a name="vml-class-attribute"></a>VML 類別屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

參考 CSS 樣式的定義。 讀取/寫入 **字串**。

**適用於**

[形狀](shape-element--vml.md)

**標記語法**

<v： *element* class = " *expression* " >

**指令碼語法**

*element* 。 classname = "*expression*"

*運算式* =*元素*。 classname

**備註**

**類別** 屬性類似于 CSS 樣式表單所使用的標準 HTML **類別** 屬性。

請注意，您可以使用 **classname** 來取代腳本的 **類別** 。 也請注意，若要撰寫腳本，只能讀取 **classname** ;變更 **classname** 的值並不會變更圖形的呈現。

*VML 標準屬性*

**另請參閱**

[形狀](shape-element--vml.md)

**範例**

使用樣式建立 **寬度** 的類別


```HTML
   .narrowstyle {width:50;height:100}
```



然後藉由包含樣式來參考寬度。 請注意，[寬度] andheight 並未在 **樣式** 屬性中定義，但會由樣式定義。


```HTML
   <v:shape id="rect01" class="narrowstyle"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



請注意， **類別** 僅適用于 CSS 型別屬性。

 

 