---
description: 繪圖物件的插補模式會影響 Windows GDI + 縮放 (擴充和縮小) 影像的方式。
ms.assetid: 3aeead47-78da-4ab3-9126-2fbe9e341e48
title: 在縮放期間使用插補模式控制影像品質
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34a829f2edf2f341f50bee771d909f7c4eef98e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972137"
---
# <a name="using-interpolation-mode-to-control-image-quality-during-scaling"></a><span data-ttu-id="86c19-103">在縮放期間使用插補模式控制影像品質</span><span class="sxs-lookup"><span data-stu-id="86c19-103">Using Interpolation Mode to Control Image Quality During Scaling</span></span>

<span data-ttu-id="86c19-104">[**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件的插補模式會影響 Windows gdi + 縮放 (擴充和縮小) 影像的方式。</span><span class="sxs-lookup"><span data-stu-id="86c19-104">The interpolation mode of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object influences the way Windows GDI+ scales (stretches and shrinks) images.</span></span> <span data-ttu-id="86c19-105">Gdiplusenums 中的 [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) 列舉定義了數個插補模式，其中有些會顯示在下列清單中：</span><span class="sxs-lookup"><span data-stu-id="86c19-105">The [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) enumeration in Gdiplusenums.h defines several interpolation modes, some of which are shown in the following list:</span></span>

-   <span data-ttu-id="86c19-106">InterpolationModeNearestNeighbor</span><span class="sxs-lookup"><span data-stu-id="86c19-106">InterpolationModeNearestNeighbor</span></span>
-   <span data-ttu-id="86c19-107">InterpolationModeBilinear</span><span class="sxs-lookup"><span data-stu-id="86c19-107">InterpolationModeBilinear</span></span>
-   <span data-ttu-id="86c19-108">InterpolationModeHighQualityBilinear</span><span class="sxs-lookup"><span data-stu-id="86c19-108">InterpolationModeHighQualityBilinear</span></span>
-   <span data-ttu-id="86c19-109">InterpolationModeBicubic</span><span class="sxs-lookup"><span data-stu-id="86c19-109">InterpolationModeBicubic</span></span>
-   <span data-ttu-id="86c19-110">InterpolationModeHighQualityBicubic</span><span class="sxs-lookup"><span data-stu-id="86c19-110">InterpolationModeHighQualityBicubic</span></span>

<span data-ttu-id="86c19-111">若要延展影像，原始影像中的每個圖元都必須對應至較大影像中的圖元群組。</span><span class="sxs-lookup"><span data-stu-id="86c19-111">To stretch an image, each pixel in the original image must be mapped to a group of pixels in the larger image.</span></span> <span data-ttu-id="86c19-112">若要壓縮影像，原始影像中的圖元群組必須對應至較小影像中的單一圖元。</span><span class="sxs-lookup"><span data-stu-id="86c19-112">To shrink an image, groups of pixels in the original image must be mapped to single pixels in the smaller image.</span></span> <span data-ttu-id="86c19-113">執行這些對應的演算法效果可決定縮放影像的品質。</span><span class="sxs-lookup"><span data-stu-id="86c19-113">The effectiveness of the algorithms that perform these mappings determines the quality of a scaled image.</span></span> <span data-ttu-id="86c19-114">產生品質較高之影像的演算法通常需要更多的處理時間。</span><span class="sxs-lookup"><span data-stu-id="86c19-114">Algorithms that produce higher-quality scaled images tend to require more processing time.</span></span> <span data-ttu-id="86c19-115">在上述清單中，InterpolationModeNearestNeighbor 是最低品質的模式，而 InterpolationModeHighQualityBicubic 則是最高品質的模式。</span><span class="sxs-lookup"><span data-stu-id="86c19-115">In the preceding list, InterpolationModeNearestNeighbor is the lowest-quality mode and InterpolationModeHighQualityBicubic is the highest-quality mode.</span></span>

<span data-ttu-id="86c19-116">若要設定插補模式，請將 [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode)列舉的其中一個成員傳遞至 [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件的 **SetInterpolationMode** 方法。</span><span class="sxs-lookup"><span data-stu-id="86c19-116">To set the interpolation mode, pass one of the members of the [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) enumeration to the **SetInterpolationMode** method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

<span data-ttu-id="86c19-117">下列範例會繪製影像，然後以三種不同的插補模式壓縮影像：</span><span class="sxs-lookup"><span data-stu-id="86c19-117">The following example draws an image and then shrinks the image with three different interpolation modes:</span></span>


```
Image image(L"GrapeBunch.bmp");
UINT width = image.GetWidth();
UINT height = image.GetHeight();
// Draw the image with no shrinking or stretching.
graphics.DrawImage(
   &image,
   Rect(10, 10, width, height),  // destination rectangle  
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using low-quality interpolation. 
graphics.SetInterpolationMode(InterpolationModeNearestNeighbor);
graphics.DrawImage(
   &image,
   Rect(10, 250, 0.6*width, 0.6*height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using medium-quality interpolation.
graphics.SetInterpolationMode(InterpolationModeHighQualityBilinear);
graphics.DrawImage(
   &image,
   Rect(150, 250, 0.6 * width, 0.6 * height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using high-quality interpolation.
graphics.SetInterpolationMode(InterpolationModeHighQualityBicubic);
graphics.DrawImage(
   &image,
   Rect(290, 250, 0.6 * width, 0.6 * height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
```



<span data-ttu-id="86c19-118">下圖顯示原始影像和三個較小的影像。</span><span class="sxs-lookup"><span data-stu-id="86c19-118">The following illustration shows the original image and the three smaller images.</span></span>

![顯示大型原始影像的圖例，以及具有不同品質的三個小型影像](images/grapes1.png)

 

 



