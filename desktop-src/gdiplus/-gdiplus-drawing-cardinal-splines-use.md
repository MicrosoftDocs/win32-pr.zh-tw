---
description: 基本曲線是透過一組指定的點順暢傳遞的曲線。
ms.assetid: 0bb84f55-18d0-4a4c-bc5b-7803aa807954
title: 繪製基本曲線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c780cb4486f579acb57170a8eda4fd187a421ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566068"
---
# <a name="drawing-cardinal-splines"></a><span data-ttu-id="d5a27-103">繪製基本曲線</span><span class="sxs-lookup"><span data-stu-id="d5a27-103">Drawing Cardinal Splines</span></span>

<span data-ttu-id="d5a27-104">基本曲線是透過一組指定的點順暢傳遞的曲線。</span><span class="sxs-lookup"><span data-stu-id="d5a27-104">A cardinal spline is a curve that passes smoothly through a given set of points.</span></span> <span data-ttu-id="d5a27-105">若要繪製基本曲線，請建立 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件，並將點陣列的位址傳遞給 [**圖形：:D rawcurve**](/previous-versions//ms536070(v=vs.85)) 方法。</span><span class="sxs-lookup"><span data-stu-id="d5a27-105">To draw a cardinal spline, create a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and pass the address of an array of points to the [**Graphics::DrawCurve**](/previous-versions//ms536070(v=vs.85)) method.</span></span> <span data-ttu-id="d5a27-106">下列範例會繪製鐘狀的基線曲線，該曲線會通過五個指定的點：</span><span class="sxs-lookup"><span data-stu-id="d5a27-106">The following example draws a bell-shaped cardinal spline that passes through five designated points:</span></span>


```
Point points[] = {Point(0, 100),
                  Point(50, 80),
                  Point(100, 20),
                  Point(150, 80),
                  Point(200, 100)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawCurve(&pen, points, 5);
```



<span data-ttu-id="d5a27-107">下圖顯示曲線和五個點。</span><span class="sxs-lookup"><span data-stu-id="d5a27-107">The following illustration shows the curve and five points.</span></span>

![一組五個點通過的基本曲線圖例](images/cardinalspline1.png)

<span data-ttu-id="d5a27-109">您可以使用 [**graphics 類別的**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) [**Graphics：:D rawclosedcurve**](/previous-versions//ms536143(v=vs.85))方法來繪製封閉的基本曲線。</span><span class="sxs-lookup"><span data-stu-id="d5a27-109">You can use the [**Graphics::DrawClosedCurve**](/previous-versions//ms536143(v=vs.85)) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to draw a closed cardinal spline.</span></span> <span data-ttu-id="d5a27-110">在封閉的基線曲線中，曲線會繼續進行陣列中的最後一個點，並連接到陣列中的第一個點。</span><span class="sxs-lookup"><span data-stu-id="d5a27-110">In a closed cardinal spline, the curve continues through the last point in the array and connects with the first point in the array.</span></span>

<span data-ttu-id="d5a27-111">下列範例會繪製經過六個指定點的封閉基本曲線。</span><span class="sxs-lookup"><span data-stu-id="d5a27-111">The following example draws a closed cardinal spline that passes through six designated points.</span></span>


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



<span data-ttu-id="d5a27-112">下圖顯示已關閉的曲線以及六個點：</span><span class="sxs-lookup"><span data-stu-id="d5a27-112">The following illustration shows the closed spline along with the six points:</span></span>

![經過六個點組合的封閉基本曲線圖例](images/cardinalspline1a.png)

<span data-ttu-id="d5a27-114">您可以藉由將張力引數傳遞給 [**圖形：:D rawcurve**](/previous-versions//ms536070(v=vs.85)) 方法，來變更基線曲線的彎曲方式。</span><span class="sxs-lookup"><span data-stu-id="d5a27-114">You can change the way a cardinal spline bends by passing a tension argument to the [**Graphics::DrawCurve**](/previous-versions//ms536070(v=vs.85)) method.</span></span> <span data-ttu-id="d5a27-115">下列範例會繪製三個透過相同點集合傳遞的基本曲線：</span><span class="sxs-lookup"><span data-stu-id="d5a27-115">The following example draws three cardinal splines that pass through the same set of points:</span></span>


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



<span data-ttu-id="d5a27-116">下圖顯示三個曲線及其張力值。</span><span class="sxs-lookup"><span data-stu-id="d5a27-116">The following illustration shows the three splines along with their tension values.</span></span> <span data-ttu-id="d5a27-117">請注意，當張力為0時，點會以直線連接。</span><span class="sxs-lookup"><span data-stu-id="d5a27-117">Note that when the tension is 0, the points are connected by straight lines.</span></span>

![三個基本曲線的圖，通過相同的一組點但在不同的懂得性](images/cardinalspline2.png)

 

 
