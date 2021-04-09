---
title: 'Angle 屬性 (填滿)  (的 VML) '
description: 'Angle 屬性 (填滿)  (的 VML) '
ms.assetid: 97203e73-4dae-40c5-bb3d-127110525cff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4167c52d82fabc5804143966b13f9d24ff7b39d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024004"
---
# <a name="angle-attribute-fillvml"></a>Angle 屬性 (填滿)  (的 VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義漸層填滿的角度。 讀取/寫入 [VgAngle](msdn-online-vml-vgangleindegrees-data-type.md) 。

**適用於**

[填滿](msdn-online-vml-fill-element.md)

**標記語法**

<v： *element* angle = " *expression* " >

**指令碼語法**

*element* . angle = "*expression*"

*運算式* =*元素*. 角度

**備註**

漸層的向量會與 blend 方向的向量（從某種色彩到另一種色彩）垂直。 預設值為 0 (零) 度，也就是由左至右的水準向量。 正面角度以逆時針方向旋轉漸層。

*VML 標準屬性*

**範例**

圖形的填滿是由兩個色彩的漸層所組成，在45度的角度從藍色到紅色。 左上角會顯示紅色，而藍色將會位於右下角。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="blue" color2="red" angle="45"/>
   </v:shape>
```



 

 