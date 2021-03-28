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
# <a name="applying-gamma-correction-to-a-gradient"></a><span data-ttu-id="348dd-103">將 Gamma 修正套用至漸層</span><span class="sxs-lookup"><span data-stu-id="348dd-103">Applying Gamma Correction to a Gradient</span></span>

<span data-ttu-id="348dd-104">您可以藉由將 **TRUE** 傳遞給該筆刷的 [**PathGradientBrush：： SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) 方法，為漸層筆刷啟用 gamma 校正。</span><span class="sxs-lookup"><span data-stu-id="348dd-104">You can enable gamma correction for a gradient brush by passing **TRUE** to the [**PathGradientBrush::SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) method of that brush.</span></span> <span data-ttu-id="348dd-105">您可以將 **FALSE** 傳遞給 **PathGradientBrush：： SetGammaCorrection** 方法，以停用 gamma 修正。</span><span class="sxs-lookup"><span data-stu-id="348dd-105">You can disable gamma correction by passing **FALSE** to the **PathGradientBrush::SetGammaCorrection** method.</span></span> <span data-ttu-id="348dd-106">預設會停用 Gamma 修正。</span><span class="sxs-lookup"><span data-stu-id="348dd-106">Gamma correction is disabled by default.</span></span>

<span data-ttu-id="348dd-107">下列範例會建立線性漸層筆刷，並使用該筆刷來填滿兩個矩形。</span><span class="sxs-lookup"><span data-stu-id="348dd-107">The following example creates a linear gradient brush and uses that brush to fill two rectangles.</span></span> <span data-ttu-id="348dd-108">第一個矩形會在沒有 gamma 校正的情況下填滿，而第二個矩形則填滿 gamma 校正。</span><span class="sxs-lookup"><span data-stu-id="348dd-108">The first rectangle is filled without gamma correction and the second rectangle is filled with gamma correction.</span></span>


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



<span data-ttu-id="348dd-109">下圖顯示兩個填滿的矩形。</span><span class="sxs-lookup"><span data-stu-id="348dd-109">The following illustration shows the two filled rectangles.</span></span> <span data-ttu-id="348dd-110">上方的矩形（沒有 gamma 更正）在中間出現深色。</span><span class="sxs-lookup"><span data-stu-id="348dd-110">The top rectangle, which does not have gamma correction, appears dark in the middle.</span></span> <span data-ttu-id="348dd-111">底部的矩形（具有 gamma 更正）似乎具有更一致的濃度。</span><span class="sxs-lookup"><span data-stu-id="348dd-111">The bottom rectangle, which has gamma correction, appears to have more uniform intensity.</span></span>

![顯示兩個矩形的圖例：第一個的色彩填滿會因濃度而異，而第二個的填滿會變少](images/gammagradient1.png)

<span data-ttu-id="348dd-113">下列範例會根據星形形路徑建立路徑漸層筆刷。</span><span class="sxs-lookup"><span data-stu-id="348dd-113">The following example creates a path gradient brush based on a star-shaped path.</span></span> <span data-ttu-id="348dd-114">程式碼會使用已停用 gamma 修正的路徑漸層筆刷 (預設) 來填滿路徑。</span><span class="sxs-lookup"><span data-stu-id="348dd-114">The code uses the path gradient brush with gamma correction disabled (the default) to fill the path.</span></span> <span data-ttu-id="348dd-115">然後，程式碼會將 **TRUE** 傳遞給 [**PathGradientBrush：： SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) 方法，以針對路徑漸層筆刷啟用 gamma 校正。</span><span class="sxs-lookup"><span data-stu-id="348dd-115">Then the code passes **TRUE** to the [**PathGradientBrush::SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) method to enable gamma correction for the path gradient brush.</span></span> <span data-ttu-id="348dd-116">對 [**graphics：： TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) 的呼叫會設定 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件的世界轉換，讓 [**圖形**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) 物件的後續呼叫會填滿位於第一個星星右邊的星星。</span><span class="sxs-lookup"><span data-stu-id="348dd-116">The call to [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) sets the world transformation of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object so that the subsequent call to [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) fills a star that sits to the right of the first star.</span></span>


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



<span data-ttu-id="348dd-117">下圖顯示上述程式碼的輸出。</span><span class="sxs-lookup"><span data-stu-id="348dd-117">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="348dd-118">右邊的星星具有 gamma 校正。</span><span class="sxs-lookup"><span data-stu-id="348dd-118">The star on the right has gamma correction.</span></span> <span data-ttu-id="348dd-119">請注意，左邊的星星（沒有 gamma 校正）有顯示深色的區域。</span><span class="sxs-lookup"><span data-stu-id="348dd-119">Note that the star on the left, which does not have gamma correction, has areas that appear dark.</span></span>

![2 5-指向的圖例會以彩色漸層填滿開始：第一個具有暗區，第二個則不是](images/gammagradient2.png)

 

 



