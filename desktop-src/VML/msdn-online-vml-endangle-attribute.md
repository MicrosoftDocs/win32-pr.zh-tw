---
title: VML EndAngle 屬性
description: VML EndAngle 屬性
ms.assetid: fc8276dc-8f61-42f4-b405-e92ca31e4637
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b22f157a1ccfc2337baa0bb5de747332bb78d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316360"
---
# <a name="vml-endangle-attribute"></a>VML EndAngle 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義弧線的端點。讀取/寫入。 [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md) 。

**適用於**

[Arc](msdn-online-vml-arc-element.md)

**標記語法**

<v： *element* endangle = " *expression* " >

**指令碼語法**

 endAngle = "*expression*"

*運算式* =** endAngle

**備註**

弧線定義為沿著圖形的 **樣式** 屬性所系結的橢圓所繪製的筆劃。 筆劃末端的定義是以水準向上 (12 點鐘) 順時針測量的角度來定義。 預設值為90度。

*VML 標準屬性*

**範例**

弧線是微笑的。 起點是在圖形周框方塊內的橢圓的90度點。 端點位於橢圓的270度點。


```HTML
   <v:arc id="myarc"
   style="position:relative;top:10;left:10;width:200;height:200"
   startangle="90" endangle="270">
   </v:arc>
```



 

 