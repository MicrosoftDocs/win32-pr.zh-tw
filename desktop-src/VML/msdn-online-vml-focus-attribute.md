---
title: VML 焦點屬性
description: VML 焦點屬性
ms.assetid: 9ed52203-4142-47cd-851f-74230aac934d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062b2900c2f980c9a1433e5e790a34d463def9be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024071"
---
# <a name="vml-focus-attribute"></a>VML 焦點屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義線性漸層填滿的中心。 讀取/寫入 **VgFraction**。

**適用於**

[填滿](msdn-online-vml-fill-element.md)

**標記語法**

<v： *element* focus = " *expression* " >

**指令碼語法**

*element* 。 focus = "*expression*"

*運算式* =*元素*。焦點

**備註**

定義 blend 的中心開始位置。 值的範圍從100% 到-100%。 預設值為 0。 值為 100% (或-100% ) 將會轉移焦點，讓 blend 的方向會反轉 (效果反轉 **色彩** 和 **Color2**) 。 50% 的值將會變更 blend，讓 **色彩** 在兩端，且 **Color2** 在中間。 值為-50% 將會變更 blend，讓 **Color2** 同時在結尾，而 **色彩** 則在中間。

*VML 標準屬性*

**範例**

填滿填滿的漸層焦點，如此紅色的 (**色彩**) 就會是圖形中央的一個寬線，而頂端和底部會是藍色 (**Color2**) 。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   method="linear" focus="-50%"/>
   </v:shape>
```



 

 