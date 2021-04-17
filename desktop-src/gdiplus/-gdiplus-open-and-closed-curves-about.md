---
description: 下圖顯示兩個曲線：一個開啟，另一個已關閉。
ms.assetid: e0fb8ba1-1783-4b36-93d8-f1242425d8bd
title: 開啟與關閉的曲線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7587ec950f8a0abc21f8c9cfb000a7333e87297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558153"
---
# <a name="open-and-closed-curves"></a><span data-ttu-id="34275-103">開啟與關閉的曲線</span><span class="sxs-lookup"><span data-stu-id="34275-103">Open and Closed Curves</span></span>

<span data-ttu-id="34275-104">下圖顯示兩個曲線：一個開啟，另一個已關閉。</span><span class="sxs-lookup"><span data-stu-id="34275-104">The following illustration shows two curves: one open and one closed.</span></span>

![開啟曲線 (曲線) 和封閉曲線 (圖形大綱的圖例) ](images/aboutgdip02-art24.png)

<span data-ttu-id="34275-106">封閉曲線有內部，因此可以使用筆刷填滿。</span><span class="sxs-lookup"><span data-stu-id="34275-106">Closed curves have an interior and therefore can be filled with a brush.</span></span> <span data-ttu-id="34275-107">Windows GDI + 中的 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 類別提供下列方法來填寫封閉的圖形和曲線： [graphicswindow.fillrectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(constbrush_constrect_))、 [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(constbrush_constrect_))、 [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal))、 [FillPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpolygon(inconstbrush_inconstpoint_inint))、 [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint))、 [**graphics：： FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath)和 [**graphics：： FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion)。</span><span class="sxs-lookup"><span data-stu-id="34275-107">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class in Windows GDI+ provides the following methods for filling closed figures and curves: [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(constbrush_constrect_)), [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(constbrush_constrect_)), [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)), [FillPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpolygon(inconstbrush_inconstpoint_inint)), [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)), [**Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath), and [**Graphics::FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion).</span></span> <span data-ttu-id="34275-108">每當您呼叫其中一個方法時，您必須將其中一個特定筆刷型別的位址傳遞 ([**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush)、 [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush)、 [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)、 [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)或 [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush)) 做為引數。</span><span class="sxs-lookup"><span data-stu-id="34275-108">Whenever you call one of these methods, you must pass the address of one of the specific brush types ([**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush), or [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush)) as an argument.</span></span>

<span data-ttu-id="34275-109">[FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal))方法是[DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal))方法的隨附。</span><span class="sxs-lookup"><span data-stu-id="34275-109">The [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)) method is a companion to the [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) method.</span></span> <span data-ttu-id="34275-110">如同 DrawArc 方法繪製橢圓形外框的一部分，FillPie 方法會填滿橢圓形內部的部分。</span><span class="sxs-lookup"><span data-stu-id="34275-110">Just as the DrawArc method draws a portion of the outline of an ellipse, the FillPie method fills a portion of the interior of an ellipse.</span></span> <span data-ttu-id="34275-111">下列範例會繪製弧形並填滿橢圓內部的對應部分。</span><span class="sxs-lookup"><span data-stu-id="34275-111">The following example draws an arc and fills the corresponding portion of the interior of the ellipse.</span></span>


```
myGraphics.FillPie(&mySolidBrush, 0, 0, 140, 70, 0, 120);
myGraphics.DrawArc(&myPen, 0, 0, 140, 70, 0, 120);
```



<span data-ttu-id="34275-112">下圖顯示弧線和填滿的圓形圖。</span><span class="sxs-lookup"><span data-stu-id="34275-112">The following illustration shows the arc and the filled pie.</span></span>

![顯示填滿橢圓形區段的圖例](images/aboutgdip02-art25.png)

<span data-ttu-id="34275-114">[FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint))方法是[DrawClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint))方法的隨附。</span><span class="sxs-lookup"><span data-stu-id="34275-114">The [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)) method is a companion to the [DrawClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint)) method.</span></span> <span data-ttu-id="34275-115">這兩種方法都會藉由將結束點連接到起點，來自動關閉曲線。</span><span class="sxs-lookup"><span data-stu-id="34275-115">Both methods automatically close the curve by connecting the ending point to the starting point.</span></span> <span data-ttu-id="34275-116">下列範例繪製的曲線會通過 (0、0) 、 (60、20) 和 (40、50) 。</span><span class="sxs-lookup"><span data-stu-id="34275-116">The following example draws a curve that passes through (0, 0), (60, 20), and (40, 50).</span></span> <span data-ttu-id="34275-117">然後，會將 (40、50) 連接至起點 (0、0) ，然後將內部填滿純色，以自動關閉曲線。</span><span class="sxs-lookup"><span data-stu-id="34275-117">Then, the curve is automatically closed by connecting (40, 50) to the starting point (0, 0), and the interior is filled with a solid color.</span></span>


```
Point myPointArray[] =
   {Point(10, 10), Point(60, 20),Point(40, 50)};
myGraphics.DrawClosedCurve(&myPen, myPointArray, 3);
myGraphics.FillClosedCurve(&mySolidBrush, myPointArray, 3, FillModeAlternate)
```



<span data-ttu-id="34275-118">路徑可以包含數個圖形 (子路徑) 。</span><span class="sxs-lookup"><span data-stu-id="34275-118">A path can consist of several figures (subpaths).</span></span> <span data-ttu-id="34275-119">[**Graphics：： FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath)方法會填滿每個圖形的內部。</span><span class="sxs-lookup"><span data-stu-id="34275-119">The [**Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method fills the interior of each figure.</span></span> <span data-ttu-id="34275-120">如果未關閉圖表， **Graphics：： FillPath** 方法會填滿在圖形關閉時所要括住的區域。</span><span class="sxs-lookup"><span data-stu-id="34275-120">If a figure is not closed, the **Graphics::FillPath** method fills the area that would be enclosed if the figure were closed.</span></span> <span data-ttu-id="34275-121">下列範例會繪製和填滿由弧線、基線曲線、字串和圓形圖組成的路徑。</span><span class="sxs-lookup"><span data-stu-id="34275-121">The following example draws and fills a path that consists of an arc, a cardinal spline, a string, and a pie.</span></span>


```
myGraphics.FillPath(&mySolidBrush, &myGraphicsPath);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



<span data-ttu-id="34275-122">下圖顯示以純色筆刷填滿之前和之後的路徑。</span><span class="sxs-lookup"><span data-stu-id="34275-122">The following illustration shows the path before and after it is filled with a solid brush.</span></span> <span data-ttu-id="34275-123">請注意，字串中的文字是由 [**圖形：:D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) 方法所組成，但是未填滿。</span><span class="sxs-lookup"><span data-stu-id="34275-123">Note that the text in the string is outlined, but not filled, by the [**Graphics::DrawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method.</span></span> <span data-ttu-id="34275-124">它是繪製字串中字元內部的 [**Graphics：： FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) 方法。</span><span class="sxs-lookup"><span data-stu-id="34275-124">It is the [**Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method that paints the interiors of the characters in the string.</span></span>

![圖例：兩次顯示文字和開啟和封閉曲線;這些是第一次是空的，而且會填滿第二次](images/aboutgdip02-art26.png)

 

 



