---
description: 重新對應是根據色彩重新對應表來轉換影像中色彩的程式。 色彩重新對應表是 ColorMap 結構的陣列。 陣列中的每個 ColorMap 結構都有 oldColor 成員和 newColor 成員。
ms.assetid: 2b56ccd5-b9f3-4c5e-8a0b-4b3d1f2b7122
title: 使用色彩重新對應表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a00f36c493bbdc696fa672b2899d4d7c6d3231a9e40c0e4162b5113d78a67164
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036296"
---
# <a name="using-a-color-remap-table"></a>使用色彩重新對應表

重新對應是根據色彩重新對應表來轉換影像中色彩的程式。 色彩重新對應表是 [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) 結構的陣列。 陣列中的每個 **ColorMap** 結構都有 **OldColor** 成員和 **newColor** 成員。

當 GDI+ 繪製影像時，影像的每個圖元都會與舊色彩的陣列進行比較。 如果圖元的色彩符合舊色彩，其色彩會變更為對應的新色彩。 色彩只會針對轉譯而變更，影像本身 (儲存在 [**影像**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) 或 [**點陣圖**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) 物件中的色彩值) 不會變更。

若要繪製重新對應的映射，請將 [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) 結構的陣列初始化。 將該陣列的位址傳遞至 [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes)物件的 [**ImageAttributes：： SetRemapTable**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable)方法，然後將 **ImageAttributes** 物件的位址傳遞至 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件的 [DrawImage 方法](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint))方法。

下列範例會從檔案 RemapInput.bmp 建立 [**映射**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) 物件。 程式碼會建立包含單一 [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) 結構的色彩重新對應表。 **ColorMap** 結構的 **oldColor** 成員為紅色，而 **newColor** 成員為藍色。 影像會繪製一次，而不需要重新對應，而且會重新對應。 重新對應程式會將所有的紅色圖元變更為藍色。


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



下圖顯示左邊的原始影像和右邊的重新對應影像。

![圖例顯示彩色影像的兩個版本;第一個版本中的紅色區域是第二個版本中的藍色](images/colortrans7.png)

 

 



