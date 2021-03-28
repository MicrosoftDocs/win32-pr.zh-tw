---
description: 當您繪製線條時，您必須將 Pen 物件的位址傳遞至 Graphics 類別的 DrawLine 方法。
ms.assetid: 4524908f-f9c2-4807-b045-eb9e43a6668b
title: 繪製不透明和半透明線條
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f751e5808440c1051b3cd996f7ebcb2df0ccbcd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571601"
---
# <a name="drawing-opaque-and-semitransparent-lines"></a><span data-ttu-id="e7242-103">繪製不透明和半透明線條</span><span class="sxs-lookup"><span data-stu-id="e7242-103">Drawing Opaque and Semitransparent Lines</span></span>

<span data-ttu-id="e7242-104">當您繪製線條時，您必須將 [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen)物件的位址傳遞至 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的 [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))方法。</span><span class="sxs-lookup"><span data-stu-id="e7242-104">When you draw a line, you must pass the address of a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object to the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="e7242-105">**畫筆** 參數的其中一個參數是 [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color)物件。</span><span class="sxs-lookup"><span data-stu-id="e7242-105">One of the parameters of the **Pen** constructor is a [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="e7242-106">若要繪製不透明的線條，請將色彩的 Alpha 元件設為 255。</span><span class="sxs-lookup"><span data-stu-id="e7242-106">To draw an opaque line, set the alpha component of the color to 255.</span></span> <span data-ttu-id="e7242-107">若要繪製半透明線條，請將 Alpha 元件設為從 1 到 254 的任何值。</span><span class="sxs-lookup"><span data-stu-id="e7242-107">To draw a semitransparent line, set the alpha component to any value from 1 through 254.</span></span>

<span data-ttu-id="e7242-108">當您在背景上繪製半透明線條時，線條的色彩會與背景的色彩混合。</span><span class="sxs-lookup"><span data-stu-id="e7242-108">When you draw a semitransparent line over a background, the color of the line is blended with the colors of the background.</span></span> <span data-ttu-id="e7242-109">Alpha 元件指定如何混合線條和背景色彩;接近0的 Alpha 值會在背景色彩上放置更多權數，而接近255的 Alpha 值則會線上條色彩上放置更多的衡量。</span><span class="sxs-lookup"><span data-stu-id="e7242-109">The alpha component specifies how the line and background colors are mixed; alpha values near 0 place more weight on the background colors, and alpha values near 255 place more weigh on the line color.</span></span>

<span data-ttu-id="e7242-110">下列範例會繪製影像，然後繪製使用影像做為背景的三行。</span><span class="sxs-lookup"><span data-stu-id="e7242-110">The following example draws an image and then draws three lines that use the image as a background.</span></span> <span data-ttu-id="e7242-111">第一條線使用的 Alpha 元件為 255，所以是不透明的。</span><span class="sxs-lookup"><span data-stu-id="e7242-111">The first line uses an alpha component of 255, so it is opaque.</span></span> <span data-ttu-id="e7242-112">第二和第三條線使用的 Alpha 元件為 128，因此是半透明的；您可以透過線條看到背景影像。</span><span class="sxs-lookup"><span data-stu-id="e7242-112">The second and third lines use an alpha component of 128, so they are semitransparent; you can see the background image through the lines.</span></span> <span data-ttu-id="e7242-113">對 [**Graphics：： SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) 的呼叫會導致第三行的混合與 gamma 校正一起進行。</span><span class="sxs-lookup"><span data-stu-id="e7242-113">The call to [**Graphics::SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) causes the blending for the third line to be done in conjunction with gamma correction.</span></span>


```
Image image(L"Texture1.jpg");
graphics.DrawImage(&image, 10, 5, image.GetWidth(), image.GetHeight());
Pen opaquePen(Color(255, 0, 0, 255), 15);
Pen semiTransPen(Color(128, 0, 0, 255), 15);
graphics.DrawLine(&opaquePen, 0, 20, 100, 20);
graphics.DrawLine(&semiTransPen, 0, 40, 100, 40);
graphics.SetCompositingQuality(CompositingQualityGammaCorrected);
graphics.DrawLine(&semiTransPen, 0, 60, 100, 60);
```



<span data-ttu-id="e7242-114">下圖顯示上述程式碼的輸出。</span><span class="sxs-lookup"><span data-stu-id="e7242-114">The following illustration shows the output of the preceding code.</span></span>

![圖例顯示由三個寬線覆迭的影像：一個不透明、一個稍微透明，還有一個非常透明](images/compqualline.png)

 

 



