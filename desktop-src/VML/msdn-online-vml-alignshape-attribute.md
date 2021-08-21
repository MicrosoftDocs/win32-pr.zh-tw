---
title: VML AlignShape 屬性
description: VML AlignShape 屬性
ms.assetid: 427e5969-4545-47b2-80f8-0e8783c52d65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e00e1fe8d07fb04c198ced2e2eb50d6ef0e6c020984d2d8cf12a3ca37cf09d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125311"
---
# <a name="vml-alignshape-attribute"></a>VML AlignShape 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

判斷影像是否要與圖形對齊。 讀取/寫入 **VgTriState**。

**適用於**

[填滿](msdn-online-vml-fill-element.md)

**標記語法**

<v： *element* alignshape = " *expression* " >

**指令碼語法**

 alignshape = "*expression*"

*運算式* =** alignshape

**備註**

若為 **True**，用來建立填滿的影像會與圖形對齊。 如果為 **False**，用來建立填滿的影像會與視窗對齊。 預設值為 **True**。

*VML 標準屬性*

**範例**

從 myimage.gif 建立的磚填滿影像會與視窗對齊，而不是圖形。雖然圖形是旋轉的，但影像並不是。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50;rotation:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill alignshape="False" type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 