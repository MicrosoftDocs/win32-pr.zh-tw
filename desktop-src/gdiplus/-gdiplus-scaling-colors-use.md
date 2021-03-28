---
description: 縮放轉換會將四個色彩元件中的一或多個數位相乘。 下表提供代表縮放的色彩矩陣專案。
ms.assetid: 08347831-7100-4220-a83b-693bb7b98ccb
title: 調整色彩
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 370155306f7b1a177358d7cf28d329ebb0d75f8c
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104195656"
---
# <a name="scaling-colors"></a><span data-ttu-id="44cad-104">調整色彩</span><span class="sxs-lookup"><span data-stu-id="44cad-104">Scaling Colors</span></span>

<span data-ttu-id="44cad-105">縮放轉換會將四個色彩元件中的一或多個數位相乘。</span><span class="sxs-lookup"><span data-stu-id="44cad-105">A scaling transformation multiplies one or more of the four color components by a number.</span></span> <span data-ttu-id="44cad-106">下表提供代表縮放的色彩矩陣專案。</span><span class="sxs-lookup"><span data-stu-id="44cad-106">The color matrix entries that represent scaling are given in the following table.</span></span>



| <span data-ttu-id="44cad-107">要調整的元件</span><span class="sxs-lookup"><span data-stu-id="44cad-107">Component to be scaled</span></span> | <span data-ttu-id="44cad-108">矩陣專案</span><span class="sxs-lookup"><span data-stu-id="44cad-108">Matrix entry</span></span> |
|------------------------|--------------|
| <span data-ttu-id="44cad-109">紅色</span><span class="sxs-lookup"><span data-stu-id="44cad-109">Red</span></span>                    | <span data-ttu-id="44cad-110">\[0 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="44cad-110">\[0\]\[0\]</span></span>   |
| <span data-ttu-id="44cad-111">綠色</span><span class="sxs-lookup"><span data-stu-id="44cad-111">Green</span></span>                  | <span data-ttu-id="44cad-112">\[1 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="44cad-112">\[1\]\[1\]</span></span>   |
| <span data-ttu-id="44cad-113">藍色</span><span class="sxs-lookup"><span data-stu-id="44cad-113">Blue</span></span>                   | <span data-ttu-id="44cad-114">\[2 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="44cad-114">\[2\]\[2\]</span></span>   |
| <span data-ttu-id="44cad-115">Alpha</span><span class="sxs-lookup"><span data-stu-id="44cad-115">Alpha</span></span>                  | <span data-ttu-id="44cad-116">\[3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="44cad-116">\[3\]\[3\]</span></span>   |



 

<span data-ttu-id="44cad-117">下列範例會從檔案 ColorBars2.bmp 中，建立 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件。</span><span class="sxs-lookup"><span data-stu-id="44cad-117">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars2.bmp.</span></span> <span data-ttu-id="44cad-118">然後，程式碼會將影像中每個圖元的藍色元件調整為2倍。</span><span class="sxs-lookup"><span data-stu-id="44cad-118">Then the code scales the blue component of each pixel in the image by a factor of 2.</span></span> <span data-ttu-id="44cad-119">原始影像會與已轉換的影像一起繪製。</span><span class="sxs-lookup"><span data-stu-id="44cad-119">The original image is drawn alongside the transformed image.</span></span>


```
Image            image(L"ColorBars2.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 2.0f, 0.0f, 0.0f,
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



<span data-ttu-id="44cad-120">下圖顯示左邊的原始影像和右邊的縮放影像。</span><span class="sxs-lookup"><span data-stu-id="44cad-120">The following illustration shows the original image on the left and the scaled image on the right.</span></span>

![顯示四個彩色橫條圖，然後顯示具有不同色彩的相同橫條。](images/colortrans3.png)

<span data-ttu-id="44cad-122">下表顯示藍色縮放前後四個橫條的色彩向量。</span><span class="sxs-lookup"><span data-stu-id="44cad-122">The following table shows the color vectors for the four bars before and after the blue scaling.</span></span> <span data-ttu-id="44cad-123">請注意，第四個色軸中的藍色元件是從0.8 到0.6。</span><span class="sxs-lookup"><span data-stu-id="44cad-123">Note that the blue component in the fourth color bar went from 0.8 to 0.6.</span></span> <span data-ttu-id="44cad-124">這是因為 GDI + 只保留結果的小數部分。</span><span class="sxs-lookup"><span data-stu-id="44cad-124">That is because GDI+ retains only the fractional part of the result.</span></span> <span data-ttu-id="44cad-125">例如， (2)  (0.8) = 1.6，1.6 的小數部分則是0.6。</span><span class="sxs-lookup"><span data-stu-id="44cad-125">For example, (2)(0.8) = 1.6, and the fractional part of 1.6 is 0.6.</span></span> <span data-ttu-id="44cad-126">只保留小數部分可確保結果一律為間隔 \[ 0，1 \] 。</span><span class="sxs-lookup"><span data-stu-id="44cad-126">Retaining only the fractional part ensures that the result is always in the interval \[0, 1\].</span></span>



| <span data-ttu-id="44cad-127">原始</span><span class="sxs-lookup"><span data-stu-id="44cad-127">Original</span></span>           | <span data-ttu-id="44cad-128">規模</span><span class="sxs-lookup"><span data-stu-id="44cad-128">Scaled</span></span>             |
|--------------------|--------------------|
| <span data-ttu-id="44cad-129">(0.4, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="44cad-129">(0.4, 0.4, 0.4, 1)</span></span> | <span data-ttu-id="44cad-130">(0.4, 0.4, 0.8, 1)</span><span class="sxs-lookup"><span data-stu-id="44cad-130">(0.4, 0.4, 0.8, 1)</span></span> |
| <span data-ttu-id="44cad-131">(0.4, 0.2, 0.2, 1)</span><span class="sxs-lookup"><span data-stu-id="44cad-131">(0.4, 0.2, 0.2, 1)</span></span> | <span data-ttu-id="44cad-132">(0.4, 0.2, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="44cad-132">(0.4, 0.2, 0.4, 1)</span></span> |
| <span data-ttu-id="44cad-133">(0.2, 0.4, 0.2, 1)</span><span class="sxs-lookup"><span data-stu-id="44cad-133">(0.2, 0.4, 0.2, 1)</span></span> | <span data-ttu-id="44cad-134">(0.2, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="44cad-134">(0.2, 0.4, 0.4, 1)</span></span> |
| <span data-ttu-id="44cad-135">(0.4, 0.4, 0.8, 1)</span><span class="sxs-lookup"><span data-stu-id="44cad-135">(0.4, 0.4, 0.8, 1)</span></span> | <span data-ttu-id="44cad-136">(0.4, 0.4, 0.6, 1)</span><span class="sxs-lookup"><span data-stu-id="44cad-136">(0.4, 0.4, 0.6, 1)</span></span> |



 

<span data-ttu-id="44cad-137">下列範例會從檔案 ColorBars2.bmp 中，建立 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件。</span><span class="sxs-lookup"><span data-stu-id="44cad-137">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars2.bmp.</span></span> <span data-ttu-id="44cad-138">然後，程式碼會調整影像中每個圖元的紅色、綠色和藍色元件。</span><span class="sxs-lookup"><span data-stu-id="44cad-138">Then the code scales the red, green, and blue components of each pixel in the image.</span></span> <span data-ttu-id="44cad-139">紅色的元件會相應減少25%，綠色的元件會相應減少35%，而且藍色的元件會相應減少50%。</span><span class="sxs-lookup"><span data-stu-id="44cad-139">The red components are scaled down 25 percent, the green components are scaled down 35 percent, and the blue components are scaled down 50 percent.</span></span>


```
Image            image(L"ColorBars.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   0.75f, 0.0f,  0.0f, 0.0f, 0.0f,
   0.0f,  0.65f, 0.0f, 0.0f, 0.0f,
   0.0f,  0.0f,  0.5f, 0.0f, 0.0f,
   0.0f,  0.0f,  0.0f, 1.0f, 0.0f,
   0.0f,  0.0f,  0.0f, 0.0f, 1.0f};
   
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



<span data-ttu-id="44cad-140">下圖顯示左邊的原始影像和右邊的縮放影像。</span><span class="sxs-lookup"><span data-stu-id="44cad-140">The following illustration shows the original image on the left and the scaled image on the right.</span></span>

![顯示四個彩色橫條圖，然後顯示具有不同色彩的橫條](images/colortrans4.png)

<span data-ttu-id="44cad-142">下表顯示紅色、綠色和藍色調整前後四個橫條的色彩向量。</span><span class="sxs-lookup"><span data-stu-id="44cad-142">The following table shows the color vectors for the four bars before and after the red, green and blue scaling.</span></span>



| <span data-ttu-id="44cad-143">原始</span><span class="sxs-lookup"><span data-stu-id="44cad-143">Original</span></span>           | <span data-ttu-id="44cad-144">規模</span><span class="sxs-lookup"><span data-stu-id="44cad-144">Scaled</span></span>               |
|--------------------|----------------------|
| <span data-ttu-id="44cad-145">(0.6, 0.6, 0.6, 1)</span><span class="sxs-lookup"><span data-stu-id="44cad-145">(0.6, 0.6, 0.6, 1)</span></span> | <span data-ttu-id="44cad-146">(0.45, 0.39, 0.3, 1)</span><span class="sxs-lookup"><span data-stu-id="44cad-146">(0.45, 0.39, 0.3, 1)</span></span> |
| <span data-ttu-id="44cad-147">(0, 1, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="44cad-147">(0, 1, 1, 1)</span></span>       | <span data-ttu-id="44cad-148">(0, 0.65, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="44cad-148">(0, 0.65, 0.5, 1)</span></span>    |
| <span data-ttu-id="44cad-149">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="44cad-149">(1, 1, 0, 1)</span></span>       | <span data-ttu-id="44cad-150">(0.75, 0.65, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="44cad-150">(0.75, 0.65, 0, 1)</span></span>   |
| <span data-ttu-id="44cad-151">(1, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="44cad-151">(1, 0, 1, 1)</span></span>       | <span data-ttu-id="44cad-152">(0.75, 0, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="44cad-152">(0.75, 0, 0.5, 1)</span></span>    |



 

 

 



