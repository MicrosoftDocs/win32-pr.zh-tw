---
description: 基本曲線是透過一組指定的點順暢傳遞的曲線。
ms.assetid: 0bb84f55-18d0-4a4c-bc5b-7803aa807954
title: 繪製基本曲線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9124e27254fc77135d265d9bab98d2332c02d345e60add1fcd96fc68c814df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036816"
---
# <a name="drawing-cardinal-splines"></a>繪製基本曲線

基本曲線是透過一組指定的點順暢傳遞的曲線。 若要繪製基本曲線，請建立 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件，並將點陣列的位址傳遞給 [**圖形：:D rawcurve**](/previous-versions//ms536070(v=vs.85)) 方法。 下列範例會繪製鐘狀的基線曲線，該曲線會通過五個指定的點：


```
Point points[] = {Point(0, 100),
                  Point(50, 80),
                  Point(100, 20),
                  Point(150, 80),
                  Point(200, 100)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawCurve(&pen, points, 5);
```



下圖顯示曲線和五個點。

![一組五個點通過的基本曲線圖例](images/cardinalspline1.png)

您可以使用 [**graphics 類別的**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) [**Graphics：:D rawclosedcurve**](/previous-versions//ms536143(v=vs.85))方法來繪製封閉的基本曲線。 在封閉的基線曲線中，曲線會繼續進行陣列中的最後一個點，並連接到陣列中的第一個點。

下列範例會繪製經過六個指定點的封閉基本曲線。


```
Point points[] = {Point(60, 60),
   Point(150, 80),
   Point(200, 40),
   Point(180, 120),
   Point(120, 100),
   Point(80, 160)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawClosedCurve(&pen, points, 6);
```



下圖顯示已關閉的曲線以及六個點：

![經過六個點組合的封閉基本曲線圖例](images/cardinalspline1a.png)

您可以藉由將張力引數傳遞給 [**圖形：:D rawcurve**](/previous-versions//ms536070(v=vs.85)) 方法，來變更基線曲線的彎曲方式。 下列範例會繪製三個透過相同點集合傳遞的基本曲線：


```
Point points[] = {Point(20, 50),
                  Point(100, 10),
                  Point(200, 100),
                  Point(300, 50),
                  Point(400, 80)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawCurve(&pen, points, 5, 0.0f);  // tension 0.0
graphics.DrawCurve(&pen, points, 5, 0.6f);  // tension 0.6
graphics.DrawCurve(&pen, points, 5, 1.0f);  // tension 1.0
```



下圖顯示三個曲線及其張力值。 請注意，當張力為0時，點會以直線連接。

![三個基本曲線的圖，通過相同的一組點但在不同的懂得性](images/cardinalspline2.png)

 

 
