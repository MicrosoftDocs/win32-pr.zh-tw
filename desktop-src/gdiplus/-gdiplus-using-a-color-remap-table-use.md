---
description: 重新對應是根據色彩重新對應表來轉換影像中色彩的程式。 色彩重新對應表是 ColorMap 結構的陣列。 陣列中的每個 ColorMap 結構都有 oldColor 成員和 newColor 成員。
ms.assetid: 2b56ccd5-b9f3-4c5e-8a0b-4b3d1f2b7122
title: 使用色彩重新對應表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1c07bc0a67a02ea07aeaa3931e661af5665e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112940"
---
# <a name="using-a-color-remap-table"></a><span data-ttu-id="81904-105">使用色彩重新對應表</span><span class="sxs-lookup"><span data-stu-id="81904-105">Using a Color Remap Table</span></span>

<span data-ttu-id="81904-106">重新對應是根據色彩重新對應表來轉換影像中色彩的程式。</span><span class="sxs-lookup"><span data-stu-id="81904-106">Remapping is the process of converting the colors in an image according to a color remap table.</span></span> <span data-ttu-id="81904-107">色彩重新對應表是 [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="81904-107">The color remap table is an array of [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) structures.</span></span> <span data-ttu-id="81904-108">陣列中的每個 **ColorMap** 結構都有 **OldColor** 成員和 **newColor** 成員。</span><span class="sxs-lookup"><span data-stu-id="81904-108">Each **ColorMap** structure in the array has an **oldColor** member and a **newColor** member.</span></span>

<span data-ttu-id="81904-109">當 GDI + 繪製影像時，影像的每個圖元都會與舊色彩的陣列進行比較。</span><span class="sxs-lookup"><span data-stu-id="81904-109">When GDI+ draws an image, each pixel of the image is compared to the array of old colors.</span></span> <span data-ttu-id="81904-110">如果圖元的色彩符合舊色彩，其色彩會變更為對應的新色彩。</span><span class="sxs-lookup"><span data-stu-id="81904-110">If a pixel's color matches an old color, its color is changed to the corresponding new color.</span></span> <span data-ttu-id="81904-111">色彩只會針對轉譯而變更，影像本身 (儲存在 [**影像**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) 或 [**點陣圖**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) 物件中的色彩值) 不會變更。</span><span class="sxs-lookup"><span data-stu-id="81904-111">The colors are changed only for rendering — the color values of the image itself (stored in an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) or [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object) are not changed.</span></span>

<span data-ttu-id="81904-112">若要繪製重新對應的映射，請將 [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) 結構的陣列初始化。</span><span class="sxs-lookup"><span data-stu-id="81904-112">To draw a remapped image, initialize an array of [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) structures.</span></span> <span data-ttu-id="81904-113">將該陣列的位址傳遞至 [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes)物件的 [**ImageAttributes：： SetRemapTable**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable)方法，然後將 **ImageAttributes** 物件的位址傳遞至 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件的 [DrawImage 方法](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint))方法。</span><span class="sxs-lookup"><span data-stu-id="81904-113">Pass the address of that array to the [**ImageAttributes::SetRemapTable**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable) method of an [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object, and then pass the address of the **ImageAttributes** object to the [DrawImage Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) method of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

<span data-ttu-id="81904-114">下列範例會從檔案 RemapInput.bmp 建立 [**映射**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) 物件。</span><span class="sxs-lookup"><span data-stu-id="81904-114">The following example creates an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file RemapInput.bmp.</span></span> <span data-ttu-id="81904-115">程式碼會建立包含單一 [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) 結構的色彩重新對應表。</span><span class="sxs-lookup"><span data-stu-id="81904-115">The code creates a color remap table that consists of a single [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) structure.</span></span> <span data-ttu-id="81904-116">**ColorMap** 結構的 **oldColor** 成員為紅色，而 **newColor** 成員為藍色。</span><span class="sxs-lookup"><span data-stu-id="81904-116">The **oldColor** member of the **ColorMap** structure is red, and the **newColor** member is blue.</span></span> <span data-ttu-id="81904-117">影像會繪製一次，而不需要重新對應，而且會重新對應。</span><span class="sxs-lookup"><span data-stu-id="81904-117">The image is drawn once without remapping and once with remapping.</span></span> <span data-ttu-id="81904-118">重新對應程式會將所有的紅色圖元變更為藍色。</span><span class="sxs-lookup"><span data-stu-id="81904-118">The remapping process changes all the red pixels to blue.</span></span>


```
Image            image(L"RemapInput.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();
ColorMap         colorMap[1];

colorMap[0].oldColor = Color(255, 255, 0, 0);  // opaque red
colorMap[0].newColor = Color(255, 0, 0, 255);  // opaque blue

imageAttributes.SetRemapTable(1, colorMap, ColorAdjustTypeBitmap);

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



<span data-ttu-id="81904-119">下圖顯示左邊的原始影像和右邊的重新對應影像。</span><span class="sxs-lookup"><span data-stu-id="81904-119">The following illustration shows the original image on the left and the remapped image on the right.</span></span>

![圖例顯示彩色影像的兩個版本;第一個版本中的紅色區域是第二個版本中的藍色](images/colortrans7.png)

 

 



