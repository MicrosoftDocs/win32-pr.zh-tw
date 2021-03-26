---
description: 切變會依據另一個色彩元件的比例增加或減少色彩元件。
ms.assetid: 12f83f35-33f1-4ac9-b45d-f8700e54053a
title: 剪色彩
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d632fded9f2b4d1e4682ae9f8ffbfedee85a46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115216"
---
# <a name="shearing-colors"></a><span data-ttu-id="66e1f-103">剪色彩</span><span class="sxs-lookup"><span data-stu-id="66e1f-103">Shearing Colors</span></span>

<span data-ttu-id="66e1f-104">切變會依據另一個色彩元件的比例增加或減少色彩元件。</span><span class="sxs-lookup"><span data-stu-id="66e1f-104">Shearing increases or decreases a color component by an amount proportional to another color component.</span></span> <span data-ttu-id="66e1f-105">例如，請考慮將紅色元件增加到藍色元件值一半的轉換。</span><span class="sxs-lookup"><span data-stu-id="66e1f-105">For example, consider the transformation where the red component is increased by one half the value of the blue component.</span></span> <span data-ttu-id="66e1f-106">在這類轉換下， (0.2、0.5、1) 的色彩會變成 (0.7、0.5、1) 。</span><span class="sxs-lookup"><span data-stu-id="66e1f-106">Under such a transformation, the color (0.2, 0.5, 1) would become (0.7, 0.5, 1).</span></span> <span data-ttu-id="66e1f-107">新的 red 元件為 0.2 + (1/2)  (1) = 0.7。</span><span class="sxs-lookup"><span data-stu-id="66e1f-107">The new red component is 0.2 + (1/2)(1) = 0.7.</span></span>

<span data-ttu-id="66e1f-108">下列範例會從檔案 ColorBars4.bmp 中，建立 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件。</span><span class="sxs-lookup"><span data-stu-id="66e1f-108">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars4.bmp.</span></span> <span data-ttu-id="66e1f-109">然後，程式碼會將上一段所述的剪轉轉換套用至影像中的每個圖元。</span><span class="sxs-lookup"><span data-stu-id="66e1f-109">Then the code applies the shearing transformation described in the preceding paragraph to each pixel in the image.</span></span>


```
Image            image(L"ColorBars4.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.5f, 0.0f, 1.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 1.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(150, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



<span data-ttu-id="66e1f-110">下圖顯示左邊的原始影像，以及右邊的剪切影像。</span><span class="sxs-lookup"><span data-stu-id="66e1f-110">The following illustration shows the original image on the left and the sheared image on the right.</span></span>

![顯示四個彩色橫條圖，然後具有不同色彩的相同橫條圖](images/colortrans6.png)

<span data-ttu-id="66e1f-112">下表顯示剪下轉換前後四個橫條的色彩向量。</span><span class="sxs-lookup"><span data-stu-id="66e1f-112">The following table shows the color vectors for the four bars before and after the shearing transformation.</span></span>



| <span data-ttu-id="66e1f-113">原始</span><span class="sxs-lookup"><span data-stu-id="66e1f-113">Original</span></span>           | <span data-ttu-id="66e1f-114">剪切</span><span class="sxs-lookup"><span data-stu-id="66e1f-114">Sheared</span></span>            |
|--------------------|--------------------|
| <span data-ttu-id="66e1f-115">(0, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="66e1f-115">(0, 0, 1, 1)</span></span>       | <span data-ttu-id="66e1f-116">(0.5, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="66e1f-116">(0.5, 0, 1, 1)</span></span>     |
| <span data-ttu-id="66e1f-117">(0.5, 1, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="66e1f-117">(0.5, 1, 0.5, 1)</span></span>   | <span data-ttu-id="66e1f-118">(0.75, 1, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="66e1f-118">(0.75, 1, 0.5, 1)</span></span>  |
| <span data-ttu-id="66e1f-119">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="66e1f-119">(1, 1, 0, 1)</span></span>       | <span data-ttu-id="66e1f-120">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="66e1f-120">(1, 1, 0, 1)</span></span>       |
| <span data-ttu-id="66e1f-121">(0.4, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="66e1f-121">(0.4, 0.4, 0.4, 1)</span></span> | <span data-ttu-id="66e1f-122">(0.6, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="66e1f-122">(0.6, 0.4, 0.4, 1)</span></span> |



 

 

 



