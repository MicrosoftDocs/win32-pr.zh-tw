---
description: 當您填滿圖形時，您必須將筆刷物件的位址傳遞至 Graphics 類別的其中一個 fill 方法。
ms.assetid: 42e36c32-ed20-4c5f-bcba-004d795babe3
title: 使用不透明和半透明筆刷繪製
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877f922fff21f964349afbe1762cc458e60391b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115233"
---
# <a name="drawing-with-opaque-and-semitransparent-brushes"></a><span data-ttu-id="fdb9b-103">使用不透明和半透明筆刷繪製</span><span class="sxs-lookup"><span data-stu-id="fdb9b-103">Drawing with Opaque and Semitransparent Brushes</span></span>

<span data-ttu-id="fdb9b-104">當您填滿圖形時，您必須將 [**筆刷**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) 物件的位址傳遞至 [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 類別的其中一個 fill 方法。</span><span class="sxs-lookup"><span data-stu-id="fdb9b-104">When you fill a shape, you must pass the address of a [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object to one of the fill methods of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="fdb9b-105">[**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush)函式的一個參數是 [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color)物件。</span><span class="sxs-lookup"><span data-stu-id="fdb9b-105">The one parameter of the [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) constructor is a [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="fdb9b-106">若要填滿不透明的圖形，請設定色彩的 Alpha 元件為 255。</span><span class="sxs-lookup"><span data-stu-id="fdb9b-106">To fill an opaque shape, set the alpha component of the color to 255.</span></span> <span data-ttu-id="fdb9b-107">若要填滿半透明的圖案，請設定 Alpha 元件為從 1 到 254 的任何值。</span><span class="sxs-lookup"><span data-stu-id="fdb9b-107">To fill a semitransparent shape, set the alpha component to any value from 1 through 254.</span></span>

<span data-ttu-id="fdb9b-108">當您填滿半透明的圖案時，圖案的色彩會與背景的色彩混合。</span><span class="sxs-lookup"><span data-stu-id="fdb9b-108">When you fill a semitransparent shape, the color of the shape is blended with the colors of the background.</span></span> <span data-ttu-id="fdb9b-109">Alpha 元件指定如何混合形狀和背景色彩;接近0的 Alpha 值會在背景色彩上放置更多權數，而接近255的 Alpha 值則會在形狀色彩上有更多的衡量。</span><span class="sxs-lookup"><span data-stu-id="fdb9b-109">The alpha component specifies how the shape and background colors are mixed; alpha values near 0 place more weight on the background colors, and alpha values near 255 place more weigh on the shape color.</span></span>

<span data-ttu-id="fdb9b-110">下列範例會繪製影像，然後填滿三個重迭影像的省略號。</span><span class="sxs-lookup"><span data-stu-id="fdb9b-110">The following example draws an image and then fills three ellipses that overlap the image.</span></span> <span data-ttu-id="fdb9b-111">第一個橢圓形使用的 Alpha 元件為 255，所以是不透明的。</span><span class="sxs-lookup"><span data-stu-id="fdb9b-111">The first ellipse uses an alpha component of 255, so it is opaque.</span></span> <span data-ttu-id="fdb9b-112">第二個和第三個橢圓形使用的 Alpha 元件為 128，因此是半透明的；您可以看到穿透橢圓形的背景影像。</span><span class="sxs-lookup"><span data-stu-id="fdb9b-112">The second and third ellipses use an alpha component of 128, so they are semitransparent; you can see the background image through the ellipses.</span></span> <span data-ttu-id="fdb9b-113">對 [**Graphics：： SetCompositingQuality**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) 的呼叫會導致第三個橢圓形的混色與 gamma 校正一起進行。</span><span class="sxs-lookup"><span data-stu-id="fdb9b-113">The call to [**Graphics::SetCompositingQuality**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) causes the blending for the third ellipse to be done in conjunction with gamma correction.</span></span>


```
Image image(L"Texture1.jpg");
graphics.DrawImage(&image, 50, 50, image.GetWidth(), image.GetHeight());
SolidBrush opaqueBrush(Color(255, 0, 0, 255));
SolidBrush semiTransBrush(Color(128, 0, 0, 255));
graphics.FillEllipse(&opaqueBrush, 35, 45, 45, 30);
graphics.FillEllipse(&semiTransBrush, 86, 45, 45, 30);
graphics.SetCompositingQuality(CompositingQualityGammaCorrected);
graphics.FillEllipse(&semiTransBrush, 40, 90, 86, 30);
```



<span data-ttu-id="fdb9b-114">下圖顯示上述程式碼的輸出。</span><span class="sxs-lookup"><span data-stu-id="fdb9b-114">The following illustration shows the output of the preceding code.</span></span>

![圖例顯示由三個省略號重迭的影像：一個不透明、稍微透明、一個非常透明](images/compqualellipse.png)

 

 



