---
description: GDI + 提供水準、垂直和對角線的線性漸層。 依預設，線性漸層中的色彩會以一致的方式變更。 不過，您可以自訂線性漸層，讓色彩以非一致的方式變更。
ms.assetid: 9b0236b2-be6b-4918-a106-5b0e6c3dd5ff
title: 建立線性漸層
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d66b9f5a3a07061e8b3d19140c25a9f3a33052a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550529"
---
# <a name="creating-a-linear-gradient"></a>建立線性漸層

GDI + 提供水準、垂直和對角線的線性漸層。 依預設，線性漸層中的色彩會以一致的方式變更。 不過，您可以自訂線性漸層，讓色彩以非一致的方式變更。

-   [水平線性漸層](#horizontal-linear-gradients)
-   [自訂線性漸層](#customizing-linear-gradients)
-   [對角線的線性漸層](#diagonal-linear-gradients)

## <a name="horizontal-linear-gradients"></a>水平線性漸層

下列範例會使用水平線性漸層筆刷來填滿線條、橢圓形和矩形：


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 255, 0, 0),   // opaque red
   Color(255, 0, 0, 255));  // opaque blue

Pen pen(&linGrBrush);

graphics.DrawLine(&pen, 0, 10, 200, 10);
graphics.FillEllipse(&linGrBrush, 0, 30, 200, 100);
graphics.FillRectangle(&linGrBrush, 0, 155, 500, 30);
```



[**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)的函式會接收四個引數：兩個點和兩個色彩。 第一個點 (0、10) 會與第一個色彩 (紅色) 相關聯，而第二個點 (200，10) 會與第二個色彩 (藍色) 相關聯。 如您所預期，從 (0、10) 到 (200）繪製的線條，10) 變更從紅色逐漸變成藍色。

點中的 10s (50、10) 和 (200，10) 並不重要。 重要的是，兩個點都有相同的第二個座標，也就是將它們連接的線條是水準的。 由於水準座標是從0到200，因此橢圓形和矩形也會從紅色逐漸變更為藍色。

下圖顯示線條、橢圓形和矩形。 請注意，色彩漸層會在水準座標增加超過200的情況下自行重複。

![圖例顯示水準漸層，其填滿線條和橢圓形，以及長度超過橢圓形的矩形](images/lineargradient1.png)

## <a name="customizing-linear-gradients"></a>自訂線性漸層

在上述範例中，當您從水準座標0移至200的水準座標時，色彩元件會呈線性變化。 例如，其第一個座標是介於0到200的中間點，會有一個藍色元件，介於0到255的中間。

GDI + 可讓您調整從漸層的某個邊緣到另一個邊緣的色彩變化方式。 假設您想要根據下表建立從黑色變更為紅色的漸層筆刷。



| 水準座標 | RGB 元件 |
|-----------------------|----------------|
| 0                     | (0, 0, 0)      |
| 40                    | (128, 0, 0)    |
| 200                   | (255, 0, 0)    |



 

請注意，當水準座標只是從0到200的20% 時，紅色元件的一半濃度。

下列範例會呼叫 [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)物件的 [**LinearGradientBrush：： SetBlend**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setblend)方法，將三個相對濃度與三個相對位置產生關聯。 如上表所示，0.5 的相對濃度與0.2 的相對位置相關聯。 程式碼會以漸層筆刷填滿橢圓形和矩形。


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 0, 0, 0),     // opaque black 
   Color(255, 255, 0, 0));  // opaque red

REAL relativeIntensities[] = {0.0f, 0.5f, 1.0f};
REAL relativePositions[]   = {0.0f, 0.2f, 1.0f};

linGrBrush.SetBlend(relativeIntensities, relativePositions, 3);

graphics.FillEllipse(&linGrBrush, 0, 30, 200, 100);
graphics.FillRectangle(&linGrBrush, 0, 155, 500, 30);
```



下圖顯示產生的橢圓形和矩形。

![圖例顯示水準漸層，其會填滿小於橢圓形的橢圓形和矩形](images/lineargradient2.png)

## <a name="diagonal-linear-gradients"></a>對角線的線性漸層

上述範例中的漸層是水準的;也就是說，當您沿著任何水平線移動時，色彩會逐漸變更。 您也可以定義垂直漸層和對角線漸層。 下列程式碼會將 (0、0) 和 (200，100) 的點傳遞至 [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) 的函式。 藍色的色彩與 (0、0) ，而綠色的色彩則與 (200，100) 相關聯。 具有畫筆寬度 10) 的線條 (，並以線性漸層筆刷填滿橢圓形。


```
LinearGradientBrush linGrBrush(
   Point(0, 0),
   Point(200, 100),
   Color(255, 0, 0, 255),   // opaque blue
   Color(255, 0, 255, 0));  // opaque green

Pen pen(&linGrBrush, 10);

graphics.DrawLine(&pen, 0, 0, 600, 300);
graphics.FillEllipse(&linGrBrush, 10, 100, 200, 100);
```



下圖顯示線條和橢圓形。 請注意，當您沿著任何直線移動到直線，而該線條與通過 (0、0) 和 (200，100) 之間的任何直線移動時，橢圓形中的色彩會逐漸變更。

![圖例顯示填滿橢圓形和對角線的對角線漸層](images/lineargradient3.png)

 

 



