---
description: B&\# 233; zier 曲線是由四個點所定義：起點、兩個控制點和一個結束點。
ms.assetid: af19e82b-0d13-4fb0-981e-8d5dd1bbfb36
title: 繪圖貝茲曲線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ea97d25f482372c387239e8f9083b31e3b2d912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692535"
---
# <a name="drawing-bezier-splines"></a>繪圖貝茲曲線

貝茲曲線是由四個點所定義：起點、兩個控制點和一個結束點。 下列範例會繪製具有起點的貝茲曲線 (10、100) 和結束點 (200，100) 。 控制點為 (100、10) 和 (150、150) ：


```
Point p1(10, 100);   // start point
Point c1(100, 10);   // first control point
Point c2(150, 150);  // second control point
Point p2(200, 100);  // end point
Pen pen(Color(255, 0, 0, 255));
graphics.DrawBezier(&pen, p1, c1, c2, p2);
```



下圖顯示產生的貝茲曲線以及其開始點、控制點和結束點。 此圖也會顯示曲線的凸殼，也就是以直線線連接四個點來形成的多邊形。

![圖例顯示具有兩個端點和兩個控制點的貝茲曲線](images/bezierspline1.png)

您可以使用 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的 [DrawBeziers](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbeziers(inconstpen_inconstpoint_inint))方法來繪製一連串連接的貝茲曲線。 下列範例會繪製由兩個連接的貝茲曲線組成的曲線。 第一個貝茲曲線的結束點是第二個貝茲曲線的起點。


```
Point p[] = {
   Point(10, 100),   // start point of first spline
   Point(75, 10),    // first control point of first spline
   Point(80, 50),    // second control point of first spline
   Point(100, 150),  // end point of first spline and 
                     // start point of second spline
   Point(125, 80),   // first control point of second spline
   Point(175, 200),  // second control point of second spline
   Point(200, 80)};  // end point of second spline
Pen pen(Color(255, 0, 0, 255));
graphics.DrawBeziers(&pen, p, 7);
```



下圖顯示連接的曲線以及七個點。

![此圖顯示兩個曲線的端點和控制點，這些曲線共用其中一個端點](images/bezierspline2.png)

 

 



