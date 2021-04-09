---
title: VML Path 屬性
description: VML Path 屬性
ms.assetid: ecb64a2f-65f7-4eb9-8d67-d7909bf52d9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e43e453e982327549475de4643cc0ad21bc0b4db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842695"
---
# <a name="vml-path-attribute"></a>VML Path 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

指定組成圖形邊緣的線。 讀取/寫入 **字串**。

**適用於**

[形狀](shape-element--vml.md)

**標記語法**

<v： *element* path = " *expression* " >

**指令碼語法**

*元素* 。 path = "*expression*"

*運算式* =*元素*。路徑

**備註**

如果圖形包含 [path](msdn-online-vml-path-element.md) 元素，path 元素的 path 命令會優先于 shape 屬性值。 如需路徑所用命令集的詳細資訊，請參閱 **Path** 元素主題。

*VML 標準屬性*

**範例**

封閉的正方形路徑是在 path 屬性的字串中定義。 初始點是使用用於 `m` **moveto** 命令的 () （1，1），並使用 `l` (字母 "L"，用於命令 **lineto**) 從起始位置 (1，1) 至其他三個點，順序 (： 1200; 200200;200、1。 行已關閉， `x` (**關閉**) ，並以 `e` (**end**) 結束。 請注意，座標是在相對座標空間中提供，而實際大小是由 **寬度** 和 **高度** 所決定。


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[路徑屬性範例](/previous-versions/bb264089(v=vs.85))。  (需要 Microsoft Internet Explorer 5 或更高版本。 ) 

 

 