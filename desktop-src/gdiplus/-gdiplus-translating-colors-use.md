---
description: 轉譯會將值加入至四個色彩元件中的一或多個。 下表提供代表翻譯的色彩矩陣專案。
ms.assetid: a0d89989-9b98-42fb-8d87-206581e3c91e
title: 翻譯色彩
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c769a24c02e977c3e32ff913852d4b6b8d54441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551688"
---
# <a name="translating-colors"></a><span data-ttu-id="d95bf-104">翻譯色彩</span><span class="sxs-lookup"><span data-stu-id="d95bf-104">Translating Colors</span></span>

<span data-ttu-id="d95bf-105">轉譯會將值加入至四個色彩元件中的一或多個。</span><span class="sxs-lookup"><span data-stu-id="d95bf-105">A translation adds a value to one or more of the four color components.</span></span> <span data-ttu-id="d95bf-106">下表提供代表翻譯的色彩矩陣專案。</span><span class="sxs-lookup"><span data-stu-id="d95bf-106">The color matrix entries that represent translations are given in the following table.</span></span>



| <span data-ttu-id="d95bf-107">要轉譯的元件</span><span class="sxs-lookup"><span data-stu-id="d95bf-107">Component to be translated</span></span> | <span data-ttu-id="d95bf-108">矩陣專案</span><span class="sxs-lookup"><span data-stu-id="d95bf-108">Matrix entry</span></span> |
|----------------------------|--------------|
| <span data-ttu-id="d95bf-109">紅色</span><span class="sxs-lookup"><span data-stu-id="d95bf-109">Red</span></span>                        | <span data-ttu-id="d95bf-110">\[4 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="d95bf-110">\[4\]\[0\]</span></span>   |
| <span data-ttu-id="d95bf-111">綠色</span><span class="sxs-lookup"><span data-stu-id="d95bf-111">Green</span></span>                      | <span data-ttu-id="d95bf-112">\[4 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="d95bf-112">\[4\]\[1\]</span></span>   |
| <span data-ttu-id="d95bf-113">藍色</span><span class="sxs-lookup"><span data-stu-id="d95bf-113">Blue</span></span>                       | <span data-ttu-id="d95bf-114">\[4 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="d95bf-114">\[4\]\[2\]</span></span>   |
| <span data-ttu-id="d95bf-115">Alpha</span><span class="sxs-lookup"><span data-stu-id="d95bf-115">Alpha</span></span>                      | <span data-ttu-id="d95bf-116">\[4 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="d95bf-116">\[4\]\[3\]</span></span>   |



 

<span data-ttu-id="d95bf-117">下列範例會從檔案 ColorBars.bmp 中，建立 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件。</span><span class="sxs-lookup"><span data-stu-id="d95bf-117">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars.bmp.</span></span> <span data-ttu-id="d95bf-118">然後，程式碼會將0.75 新增至影像中每個圖元的紅色元件。</span><span class="sxs-lookup"><span data-stu-id="d95bf-118">Then the code adds 0.75 to the red component of each pixel in the image.</span></span> <span data-ttu-id="d95bf-119">原始影像會與已轉換的影像一起繪製。</span><span class="sxs-lookup"><span data-stu-id="d95bf-119">The original image is drawn alongside the transformed image.</span></span>


```
Image            image(L"ColorBars.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f,  0.0f, 0.0f, 0.0f, 0.0f,
   0.0f,  1.0f, 0.0f, 0.0f, 0.0f,
   0.0f,  0.0f, 1.0f, 0.0f, 0.0f,
   0.0f,  0.0f, 0.0f, 1.0f, 0.0f,
   0.75f, 0.0f, 0.0f, 0.0f, 1.0f};
   
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



<span data-ttu-id="d95bf-120">下圖顯示左邊的原始影像，以及右邊的已轉換影像。</span><span class="sxs-lookup"><span data-stu-id="d95bf-120">The following illustration shows the original image on the left and the transformed image on the right.</span></span>

![顯示四個彩色橫條圖，然後具有不同色彩的相同橫條圖](images/colortrans2.png)

<span data-ttu-id="d95bf-122">下表列出紅轉譯前後四個橫條的色彩向量。</span><span class="sxs-lookup"><span data-stu-id="d95bf-122">The following table lists the color vectors for the four bars before and after the red translation.</span></span> <span data-ttu-id="d95bf-123">請注意，因為色彩元件的最大值為1，所以第二個數據列中的紅色元件不會變更。</span><span class="sxs-lookup"><span data-stu-id="d95bf-123">Note that because the maximum value for a color component is 1, the red component in the second row does not change.</span></span> <span data-ttu-id="d95bf-124"> (同樣地，色彩元件的最小值是0。 ) </span><span class="sxs-lookup"><span data-stu-id="d95bf-124">(Similarly, the minimum value for a color component is 0.)</span></span>



| <span data-ttu-id="d95bf-125">原始</span><span class="sxs-lookup"><span data-stu-id="d95bf-125">Original</span></span>           | <span data-ttu-id="d95bf-126">已轉譯</span><span class="sxs-lookup"><span data-stu-id="d95bf-126">Translated</span></span>      |
|--------------------|-----------------|
| <span data-ttu-id="d95bf-127">黑色 (0、0、0、1) </span><span class="sxs-lookup"><span data-stu-id="d95bf-127">Black (0, 0, 0, 1)</span></span> | <span data-ttu-id="d95bf-128">(0.75, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="d95bf-128">(0.75, 0, 0, 1)</span></span> |
| <span data-ttu-id="d95bf-129">紅色 (1、0、0、1) </span><span class="sxs-lookup"><span data-stu-id="d95bf-129">Red (1, 0, 0, 1)</span></span>   | <span data-ttu-id="d95bf-130">(1, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="d95bf-130">(1, 0, 0, 1)</span></span>    |
| <span data-ttu-id="d95bf-131">綠色 (0、1、0、1) </span><span class="sxs-lookup"><span data-stu-id="d95bf-131">Green (0, 1, 0, 1)</span></span> | <span data-ttu-id="d95bf-132">(0.75, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="d95bf-132">(0.75, 1, 0, 1)</span></span> |
| <span data-ttu-id="d95bf-133">藍色 (0、0、1、1) </span><span class="sxs-lookup"><span data-stu-id="d95bf-133">Blue (0, 0, 1, 1)</span></span>  | <span data-ttu-id="d95bf-134">(0.75, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="d95bf-134">(0.75, 0, 1, 1)</span></span> |



 

 

 



