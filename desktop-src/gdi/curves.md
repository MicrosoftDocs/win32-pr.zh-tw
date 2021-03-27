---
description: 一般曲線是一組在點陣顯示器上反白顯示的圖元 (或列印頁面上的點) ，定義圓周 (或圓錐區段的周邊) 部分。
ms.assetid: b7a1b544-8b50-45ba-918c-17472c46c8b8
title: 曲線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e694edeb535dbc7dbd4191a5a2b0b44556b810e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848568"
---
# <a name="curves"></a><span data-ttu-id="8bb71-103">曲線</span><span class="sxs-lookup"><span data-stu-id="8bb71-103">Curves</span></span>

<span data-ttu-id="8bb71-104">一般曲線是一組在點陣顯示器上反白顯示的圖元 (或列印頁面上的點) ，定義圓周 (或圓錐區段的周邊) 部分。</span><span class="sxs-lookup"><span data-stu-id="8bb71-104">A regular curve is a set of highlighted pixels on a raster display (or dots on a printed page) that define the perimeter (or part of the perimeter) of a conic section.</span></span> <span data-ttu-id="8bb71-105">不規則曲線是一組圖元，用來定義不符合圓錐區段周邊的曲線。</span><span class="sxs-lookup"><span data-stu-id="8bb71-105">An irregular curve is a set of pixels that define a curve that does not fit the perimeter of a conic section.</span></span> <span data-ttu-id="8bb71-106">結束點會從曲線中排除，就如同從一行排除一樣。</span><span class="sxs-lookup"><span data-stu-id="8bb71-106">The ending point is excluded from a curve just as it is excluded from a line.</span></span>

<span data-ttu-id="8bb71-107">當應用程式呼叫其中一個曲線繪圖函式時，GDI 會將曲線分成數個極小、離散的線段。</span><span class="sxs-lookup"><span data-stu-id="8bb71-107">When an application calls one of the curve-drawing functions, GDI breaks the curve into a number of extremely small, discrete line segments.</span></span> <span data-ttu-id="8bb71-108">在判斷端點 (開始點和結束點) 每個這些線段時，GDI 會透過套用其 DDA 來決定) 定義每一行的圖元 (或點。</span><span class="sxs-lookup"><span data-stu-id="8bb71-108">After determining the endpoints (starting point and ending point) for each of these line segments, GDI determines which pixels (or dots) define each line by applying its DDA.</span></span>

<span data-ttu-id="8bb71-109">應用程式可以藉由呼叫 [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc) 函數來繪製橢圓形或橢圓形的一部分。</span><span class="sxs-lookup"><span data-stu-id="8bb71-109">An application can draw an ellipse or part of an ellipse by calling the [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc) function.</span></span> <span data-ttu-id="8bb71-110">此函式會在不可見矩形的周邊（稱為周框矩形）中繪製曲線。</span><span class="sxs-lookup"><span data-stu-id="8bb71-110">This function draws the curve within the perimeter of an invisible rectangle called a bounding rectangle.</span></span> <span data-ttu-id="8bb71-111">橢圓形的大小是由兩個不可見的 radials 所指定，從矩形的中心延伸至矩形的側邊。</span><span class="sxs-lookup"><span data-stu-id="8bb71-111">The size of the ellipse is specified by two invisible radials extending from the center of the rectangle to the sides of the rectangle.</span></span> <span data-ttu-id="8bb71-112">下圖顯示的弧形 (部分) 使用 **arc** 函數繪製的橢圓形。</span><span class="sxs-lookup"><span data-stu-id="8bb71-112">The following illustration shows an arc (part of an ellipse) drawn by using the **Arc** function.</span></span>

![顯示代表完整圓形三季的弧線的圖表](images/cslcv-03.png)

<span data-ttu-id="8bb71-114">呼叫 [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc) 函式時，應用程式會指定周框和 radials 的座標。</span><span class="sxs-lookup"><span data-stu-id="8bb71-114">When calling the [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc) function, an application specifies the coordinates of the bounding rectangle and radials.</span></span> <span data-ttu-id="8bb71-115">上圖顯示以虛線繪製的矩形和 radials，而使用實線繪製實際的弧形。</span><span class="sxs-lookup"><span data-stu-id="8bb71-115">The preceding illustration shows the rectangle and radials with dashed lines while the actual arc was drawn using a solid line.</span></span>

<span data-ttu-id="8bb71-116">繪製另一個物件的弧線時，應用程式可以呼叫 [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) 和 [**GetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-getarcdirection) 函式，以控制繪製物件時 (順時針或逆時針) 方向。</span><span class="sxs-lookup"><span data-stu-id="8bb71-116">When drawing the arc of another object, the application can call the [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) and [**GetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-getarcdirection) functions to control the direction (clockwise or counterclockwise) in which the object is drawn.</span></span> <span data-ttu-id="8bb71-117">繪製弧形和其他物件的預設方向是以逆時針表示。</span><span class="sxs-lookup"><span data-stu-id="8bb71-117">The default direction for drawing arcs and other objects is counterclockwise.</span></span>

<span data-ttu-id="8bb71-118">除了繪製省略號或橢圓形的部分，應用程式也可以繪製稱為貝茲曲線的不規則曲線。</span><span class="sxs-lookup"><span data-stu-id="8bb71-118">In addition to drawing ellipses or parts of ellipses, applications can draw irregular curves called Bézier curves.</span></span> <span data-ttu-id="8bb71-119">*貝茲曲線* 是一種不規則曲線，其曲率是由四個控制點所定義 (p1、p2、p3 和 p4) 。</span><span class="sxs-lookup"><span data-stu-id="8bb71-119">A *Bézier curve* is an irregular curve whose curvature is defined by four control points (p1, p2, p3, and p4).</span></span> <span data-ttu-id="8bb71-120">控制點 p1 和 p4 會定義曲線的開始和結束點，而控制點 p2 和 p3 會藉由標示曲線反轉方向的點來定義曲線的形狀，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="8bb71-120">The control points p1 and p4 define the starting and ending points of the curve, and the control points p2 and p3 define the shape of the curve by marking points where the curve reverses orientation, as shown in the following diagram.</span></span>

![顯示兩個貝茲曲線的圖，每個曲線都介於起始點和結束點之間，而每個曲線都有兩個控制點](images/cslcv-04.png)

<span data-ttu-id="8bb71-122">應用程式可以藉由呼叫 [**PolyBezier**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier) 函式來繪製不規則曲線，以提供適當的控制點。</span><span class="sxs-lookup"><span data-stu-id="8bb71-122">An application can draw irregular curves by calling the [**PolyBezier**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier) function, supplying the appropriate control points.</span></span>

 

 



