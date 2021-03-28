---
description: 您可以藉由將 TRUE 傳遞給該筆刷的 PathGradientBrush：： SetGammaCorrection 方法，為漸層筆刷啟用 gamma 校正。
ms.assetid: 47472e41-f469-44f4-8b39-cf3982b79f9e
title: 將 Gamma 修正套用至漸層
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e51673e8be4fd289286ce5e4e3e8f7c5469724
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115272"
---
# <a name="applying-gamma-correction-to-a-gradient"></a>將 Gamma 修正套用至漸層

您可以藉由將 **TRUE** 傳遞給該筆刷的 [**PathGradientBrush：： SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) 方法，為漸層筆刷啟用 gamma 校正。 您可以將 **FALSE** 傳遞給 **PathGradientBrush：： SetGammaCorrection** 方法，以停用 gamma 修正。 預設會停用 Gamma 修正。

下列範例會建立線性漸層筆刷，並使用該筆刷來填滿兩個矩形。 第一個矩形會在沒有 gamma 校正的情況下填滿，而第二個矩形則填滿 gamma 校正。


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 255, 0, 0),   // Opaque red
   Color(255, 0, 0, 255));  // Opaque blue

graphics.FillRectangle(&linGrBrush, 0, 0, 200, 50);
linGrBrush.SetGammaCorrection(TRUE);
graphics.FillRectangle(&linGrBrush, 0, 60, 200, 50); 
```



下圖顯示兩個填滿的矩形。 上方的矩形（沒有 gamma 更正）在中間出現深色。 底部的矩形（具有 gamma 更正）似乎具有更一致的濃度。

![顯示兩個矩形的圖例：第一個的色彩填滿會因濃度而異，而第二個的填滿會變少](images/gammagradient1.png)

下列範例會根據星形形路徑建立路徑漸層筆刷。 程式碼會使用已停用 gamma 修正的路徑漸層筆刷 (預設) 來填滿路徑。 然後，程式碼會將 **TRUE** 傳遞給 [**PathGradientBrush：： SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) 方法，以針對路徑漸層筆刷啟用 gamma 校正。 對 [**graphics：： TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) 的呼叫會設定 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件的世界轉換，讓 [**圖形**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) 物件的後續呼叫會填滿位於第一個星星右邊的星星。


```
// Put the points of a polygon in an array.
Point points[] = {Point(75, 0), Point(100, 50), 
                  Point(150, 50), Point(112, 75),
                  Point(150, 150), Point(75, 100), 
                  Point(0, 150), Point(37, 75), 
                  Point(0, 50), Point(50, 50)};

// Use the array of points to construct a path.
GraphicsPath path;
path.AddLines(points, 10);

// Use the path to construct a path gradient brush.
PathGradientBrush pthGrBrush(&path);

// Set the color at the center of the path to red.
pthGrBrush.SetCenterColor(Color(255, 255, 0, 0));

// Set the colors of the points in the array.
Color colors[] = {Color(255, 0, 0, 0),   Color(255, 0, 255, 0),
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255), 
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0), 
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255),
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0)};

int count = 10;
pthGrBrush.SetSurroundColors(colors, &count);

// Fill the path with the path gradient brush.
graphics.FillPath(&pthGrBrush, &path);
pthGrBrush.SetGammaCorrection(TRUE);
graphics.TranslateTransform(200.0f, 0.0f);
graphics.FillPath(&pthGrBrush, &path);
```



下圖顯示上述程式碼的輸出。 右邊的星星具有 gamma 校正。 請注意，左邊的星星（沒有 gamma 校正）有顯示深色的區域。

![2 5-指向的圖例會以彩色漸層填滿開始：第一個具有暗區，第二個則不是](images/gammagradient2.png)

 

 



