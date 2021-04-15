---
title: VML CropRight 屬性
description: VML CropRight 屬性
ms.assetid: 1e2bd8e8-3d56-435d-bfaf-fb07f6b6fba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21604fb341840847690e9e086386d46f7124908a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463193"
---
# <a name="vml-cropright-attribute"></a>VML CropRight 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義從右邊移除圖片的百分比。 讀取/寫入 **VgNumber**。

**適用於**

[ImageData](msdn-online-vml-imagedata-element.md)

**標記語法**

<v： *element* cropright = " *expression* " >

**指令碼語法**

 cropright = "*expression*"

*運算式* =** cropright

**備註**

裁剪量的範圍可以從-1.0 到1.0。 預設值為 0。 請注意，值1不會顯示任何圖片。 負數值會導致圖片從正在裁剪的邊緣中擠壓， (圖片和裁剪邊緣之間的空格會以圖形) 填滿色彩填滿。 小於1的正值會導致剩餘的圖片伸展，以符合圖形。

*VML 標準屬性*

**範例**

圖片將會從右邊算出20% 的寬度來擠壓。 圖片與右邊緣之間的空白空間將會以圖形的填滿色彩填滿。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="blue"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropright="-.2" src="kids.jpg"/>
   </v:shape>
```





 

 