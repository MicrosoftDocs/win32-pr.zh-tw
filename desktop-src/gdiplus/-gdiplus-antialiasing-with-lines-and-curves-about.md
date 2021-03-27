---
description: 當您使用 Windows GDI + 來繪製線條時，可以提供線條的起點和結束點，但不需要提供該行上個別圖元的任何相關資訊。
ms.assetid: 7c4869c1-76ff-42d1-abf1-387121943b2a
title: 線條和曲線的反鋸齒功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c817d3e11b4699c9fc892b41dcc827c0861f192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692564"
---
# <a name="antialiasing-with-lines-and-curves"></a><span data-ttu-id="0dc30-103">線條和曲線的反鋸齒功能</span><span class="sxs-lookup"><span data-stu-id="0dc30-103">Antialiasing with Lines and Curves</span></span>

<span data-ttu-id="0dc30-104">當您使用 Windows GDI + 來繪製線條時，可以提供線條的起點和結束點，但不需要提供該行上個別圖元的任何相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0dc30-104">When you use Windows GDI+ to draw a line, you provide the starting point and ending point of the line, but you don't have to provide any information about the individual pixels on the line.</span></span> <span data-ttu-id="0dc30-105">GDI + 會與顯示驅動程式軟體一起運作，以判斷要開啟哪些圖元來顯示特定顯示裝置上的線條。</span><span class="sxs-lookup"><span data-stu-id="0dc30-105">GDI+ works in conjunction with the display driver software to determine which pixels will be turned on to show the line on a particular display device.</span></span>

<span data-ttu-id="0dc30-106">請考慮從點 (4，2) 到 (16，10) 的點的紅線。</span><span class="sxs-lookup"><span data-stu-id="0dc30-106">Consider a straight red line that goes from the point (4, 2) to the point (16, 10).</span></span> <span data-ttu-id="0dc30-107">假設座標系統的原點位於左上角，而量值的單位是圖元。</span><span class="sxs-lookup"><span data-stu-id="0dc30-107">Assume the coordinate system has its origin in the upper-left corner and that the unit of measure is the pixel.</span></span> <span data-ttu-id="0dc30-108">也假設 X 軸指向右邊，y 軸則指向向下。</span><span class="sxs-lookup"><span data-stu-id="0dc30-108">Also assume that the x-axis points to the right and the y-axis points down.</span></span> <span data-ttu-id="0dc30-109">下圖顯示在彩色背景上繪製的紅線放大視圖。</span><span class="sxs-lookup"><span data-stu-id="0dc30-109">The following illustration shows an enlarged view of the red line drawn on a multicolored background.</span></span>

![圖例顯示彩色彩色背景上的純色紅色圖元](images/aboutgdip02-art33.png)

<span data-ttu-id="0dc30-111">請注意，用來呈現線條的紅色圖元不是透明的。</span><span class="sxs-lookup"><span data-stu-id="0dc30-111">Note that the red pixels used to render the line are opaque.</span></span> <span data-ttu-id="0dc30-112">沒有部分透明的圖元可顯示線條。</span><span class="sxs-lookup"><span data-stu-id="0dc30-112">There are no partially transparent pixels involved in displaying the line.</span></span> <span data-ttu-id="0dc30-113">這種類型的線條轉譯讓線條具有不規則外觀，而線條看起來有點像樓梯。</span><span class="sxs-lookup"><span data-stu-id="0dc30-113">This type of line rendering gives the line a jagged appearance, and the line looks a bit like a staircase.</span></span> <span data-ttu-id="0dc30-114">這項技術代表具有樓梯的線，稱為別名;樓梯是理論線的別名。</span><span class="sxs-lookup"><span data-stu-id="0dc30-114">This technique of representing a line with a staircase is called aliasing; the staircase is an alias for the theoretical line.</span></span>

<span data-ttu-id="0dc30-115">更精密的轉譯線條技巧牽涉到使用部分透明的圖元以及純紅色圖元。</span><span class="sxs-lookup"><span data-stu-id="0dc30-115">A more sophisticated technique for rendering a line involves using partially transparent pixels along with pure red pixels.</span></span> <span data-ttu-id="0dc30-116">圖元會設定為純紅色或某些混合的紅色和背景色彩，視它們與線條的接近程度而定。</span><span class="sxs-lookup"><span data-stu-id="0dc30-116">Pixels are set to pure red or to some blend of red and the background color depending on how close they are to the line.</span></span> <span data-ttu-id="0dc30-117">這種類型的轉譯稱為消除鋸齒，並導致人類眼睛感覺更平滑的線條。</span><span class="sxs-lookup"><span data-stu-id="0dc30-117">This type of rendering is called antialiasing and results in a line that the human eye perceives as more smooth.</span></span> <span data-ttu-id="0dc30-118">下圖顯示特定圖元如何與背景混合，以產生反鋸齒線條。</span><span class="sxs-lookup"><span data-stu-id="0dc30-118">The following illustration shows how certain pixels are blended with the background to produce an antialiased line.</span></span>

![圖例顯示在相同背景的紅色圖元](images/aboutgdip02-art34.png)

<span data-ttu-id="0dc30-120"> (平滑) 的消除鋸齒也可以套用至曲線。</span><span class="sxs-lookup"><span data-stu-id="0dc30-120">Antialiasing (smoothing) can also be applied to curves.</span></span> <span data-ttu-id="0dc30-121">下圖顯示平滑橢圓形的放大視圖。</span><span class="sxs-lookup"><span data-stu-id="0dc30-121">The following illustration shows an enlarged view of a smoothed ellipse.</span></span>

![在白色背景上由不同的藍色圖元陰影組成的橢圓形圖例](images/aboutgdip02-art35.png)

<span data-ttu-id="0dc30-123">下圖顯示實際大小的相同橢圓形，一次沒有消除鋸齒，一次是消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="0dc30-123">The following illustration shows the same ellipse in its actual size, once without antialiasing and once with antialiasing.</span></span>

![兩個省略號的螢幕擷取畫面：具有消除鋸齒功能的 noticably 會更平滑](images/aboutgdip02-art36.png)

<span data-ttu-id="0dc30-125">若要繪製使用消除鋸齒的線條和曲線，請建立 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件，並將 *SmoothingModeAntiAlias* 傳遞至其 [**graphics：： SetSmoothingMode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode) 方法。</span><span class="sxs-lookup"><span data-stu-id="0dc30-125">To draw lines and curves that use antialiasing, create a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and pass *SmoothingModeAntiAlias* to its [**Graphics::SetSmoothingMode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode) method.</span></span> <span data-ttu-id="0dc30-126">然後，呼叫相同 **圖形** 物件的其中一個繪圖方法。</span><span class="sxs-lookup"><span data-stu-id="0dc30-126">Then call one of the drawing methods of that same **Graphics** object.</span></span>


```
myGraphics.SetSmoothingMode(SmoothingModeAntiAlias);
myGraphics.DrawLine(&myPen, 0, 0, 12, 8);
```



<span data-ttu-id="0dc30-127">**SmoothingModeAntiAlias** 是 [**SmoothingMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) 列舉的元素。</span><span class="sxs-lookup"><span data-stu-id="0dc30-127">**SmoothingModeAntiAlias** is an element of the [**SmoothingMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) enumeration.</span></span>

 

 



