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
# <a name="shearing-colors"></a>剪色彩

切變會依據另一個色彩元件的比例增加或減少色彩元件。 例如，請考慮將紅色元件增加到藍色元件值一半的轉換。 在這類轉換下， (0.2、0.5、1) 的色彩會變成 (0.7、0.5、1) 。 新的 red 元件為 0.2 + (1/2)  (1) = 0.7。

下列範例會從檔案 ColorBars4.bmp 中，建立 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件。 然後，程式碼會將上一段所述的剪轉轉換套用至影像中的每個圖元。


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



下圖顯示左邊的原始影像，以及右邊的剪切影像。

![顯示四個彩色橫條圖，然後具有不同色彩的相同橫條圖](images/colortrans6.png)

下表顯示剪下轉換前後四個橫條的色彩向量。



| 原始           | 剪切            |
|--------------------|--------------------|
| (0, 0, 1, 1)       | (0.5, 0, 1, 1)     |
| (0.5, 1, 0.5, 1)   | (0.75, 1, 0.5, 1)  |
| (1, 1, 0, 1)       | (1, 1, 0, 1)       |
| (0.4, 0.4, 0.4, 1) | (0.6, 0.4, 0.4, 1) |



 

 

 



