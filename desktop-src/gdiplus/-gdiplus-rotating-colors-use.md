---
description: 四維色彩空間中的旋轉很難視覺化。
ms.assetid: 099f76a3-2da3-4f2b-8f8d-557d144451dc
title: 旋轉色彩
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea322179bd4a46021d181abedd1797d6bdda7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847996"
---
# <a name="rotating-colors"></a><span data-ttu-id="848b6-103">旋轉色彩</span><span class="sxs-lookup"><span data-stu-id="848b6-103">Rotating Colors</span></span>

<span data-ttu-id="848b6-104">四維色彩空間中的旋轉很難視覺化。</span><span class="sxs-lookup"><span data-stu-id="848b6-104">Rotation in a four-dimensional color space is difficult to visualize.</span></span> <span data-ttu-id="848b6-105">我們可以藉由同意保持固定的其中一個色彩元件，讓您更輕鬆地將旋轉視覺化。</span><span class="sxs-lookup"><span data-stu-id="848b6-105">We can make it easier to visualize rotation by agreeing to keep one of the color components fixed.</span></span> <span data-ttu-id="848b6-106">假設我們同意將 Alpha 元件固定在 1 (完全不透明) 。</span><span class="sxs-lookup"><span data-stu-id="848b6-106">Suppose we agree to keep the alpha component fixed at 1 (fully opaque).</span></span> <span data-ttu-id="848b6-107">然後我們可以使用紅色、綠色和藍色軸來視覺化三維色彩空間，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="848b6-107">Then we can visualize a three-dimensional color space with red, green, and blue axes as shown in the following illustration.</span></span>

![以紅色、綠色和藍色軸標示之三維色彩空間的觀點視圖圖例](images/recoloring03.png)

<span data-ttu-id="848b6-109">您可以將色彩視為立體空間中的點。</span><span class="sxs-lookup"><span data-stu-id="848b6-109">A color can be thought of as a point in 3-D space.</span></span> <span data-ttu-id="848b6-110">例如，點 (1，0，0) 空間代表紅色，而點 (0，1，0) 在空間中代表綠色。</span><span class="sxs-lookup"><span data-stu-id="848b6-110">For example, the point (1, 0, 0) in space represents the color red, and the point (0, 1, 0) in space represents the color green.</span></span>

<span data-ttu-id="848b6-111">下圖顯示在 Red-Green 平面中，將色彩 (1、0、0) 旋轉為60度的意義。</span><span class="sxs-lookup"><span data-stu-id="848b6-111">The following illustration shows what it means to rotate the color (1, 0, 0) through an angle of 60 degrees in the Red-Green plane.</span></span> <span data-ttu-id="848b6-112">平行至 Red-Green 平面的平面旋轉可以視為與藍色軸有關的旋轉。</span><span class="sxs-lookup"><span data-stu-id="848b6-112">Rotation in a plane parallel to the Red-Green plane can be thought of as rotation about the blue axis.</span></span>

![圖例顯示點 (1、0、0) 旋轉60度到 (0.5、0.866、0) ](images/recoloring04.png)

<span data-ttu-id="848b6-114">下圖顯示如何初始化色彩矩陣，以執行三個座標軸的旋轉 (紅色、綠色、藍色) 。</span><span class="sxs-lookup"><span data-stu-id="848b6-114">The following illustration shows how to initialize a color matrix to perform rotations about each of the three coordinate axes (red, green, blue).</span></span>

![圖例顯示可執行每個座標軸之旋轉的色彩矩陣](images/recoloring05.png)

<span data-ttu-id="848b6-116">下列範例會取得全部為1、0、0.6)  (1、0、的影像，並套用60度的旋轉（關於藍色軸）。</span><span class="sxs-lookup"><span data-stu-id="848b6-116">The following example takes an image that is all one color (1, 0, 0.6) and applies a 60-degree rotation about the blue axis.</span></span> <span data-ttu-id="848b6-117">旋轉的角度會在與 Red-Green 平面平行的平面中掃除。</span><span class="sxs-lookup"><span data-stu-id="848b6-117">The angle of the rotation is swept out in a plane that is parallel to the Red-Green plane.</span></span>


```
Image            image(L"RotationInput.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();
REAL             degrees = 60;
REAL             pi = acos(-1);  // the angle whose cosine is -1.
REAL             r = degrees * pi / 180;  // degrees to radians

ColorMatrix colorMatrix = {
   cos(r),  sin(r), 0.0f, 0.0f, 0.0f,
   -sin(r), cos(r), 0.0f, 0.0f, 0.0f,
   0.0f,    0.0f,   1.0f, 0.0f, 0.0f,
   0.0f,    0.0f,   0.0f, 1.0f, 0.0f,
   0.0f,    0.0f,   0.0f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(130, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



<span data-ttu-id="848b6-118">下圖顯示左邊的原始影像和右邊的彩色旋轉影像。</span><span class="sxs-lookup"><span data-stu-id="848b6-118">The following illustration shows the original image on the left and the color-rotated image on the right.</span></span>

![圖例顯示填滿原始影像的矩形 (紫羅蘭紅) 和彩色旋轉影像 (海綠色) ](images/colortrans5.png)

<span data-ttu-id="848b6-120">上述程式碼範例中執行的色彩旋轉可以視覺化方式呈現，如下所示。</span><span class="sxs-lookup"><span data-stu-id="848b6-120">The color rotation performed in the preceding code example can be visualized as follows.</span></span>

![顯示3-d 色彩空間的圖例，以及 (1，0，0.6) 旋轉60度的點， (0.5、0.866、0.6) ](images/recoloring06.png)

 

 



