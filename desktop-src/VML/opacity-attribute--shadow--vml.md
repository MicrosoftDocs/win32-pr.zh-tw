---
title: '不透明度屬性 (陰影)  (VML) '
description: '不透明度屬性 (陰影)  (VML) '
ms.assetid: 394d755c-72cf-46f5-a258-1844b07a97bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d09ca038a187c4a4ed1f914f5d05bcfd63e4a4a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375580"
---
# <a name="opacity-attribute-shadowvml"></a>不透明度屬性 (陰影)  (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

決定陰影的透明度。 讀取/寫入 [VgFraction](msdn-online-vml-vgfraction-data-type.md) 。

**適用於**

[Shadow](msdn-online-vml-shadow-element.md)

**標記語法**

<v： *element* opacity = " *expression* " >

**指令碼語法**

*元素* 。不透明度 = "*expression*"

*運算式* =*元素*。不透明度

**備註**

預設值為 1。 值為0會產生完全透明的陰影。

*VML 標準屬性*

**範例**

圖形的陰影有50% 的透明。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor= "red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m  1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" opacity="50%"/>
   </v:shape>
```



 

 