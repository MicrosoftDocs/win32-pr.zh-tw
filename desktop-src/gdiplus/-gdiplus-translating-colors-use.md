---
description: 轉譯會將值加入至四個色彩元件中的一或多個。 下表提供代表翻譯的色彩矩陣專案。
ms.assetid: a0d89989-9b98-42fb-8d87-206581e3c91e
title: 翻譯色彩
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 608a0653423d854e6d77bd624949f24ec03cce6c4ed063d4c740dd142b1dfb3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036336"
---
# <a name="translating-colors"></a>翻譯色彩

轉譯會將值加入至四個色彩元件中的一或多個。 下表提供代表翻譯的色彩矩陣專案。



| 要轉譯的元件 | 矩陣專案 |
|----------------------------|--------------|
| 紅色                        | \[4 \] \[ 0\]   |
| 綠色                      | \[4 \] \[ 1\]   |
| 藍色                       | \[4 \] \[ 2\]   |
| Alpha                      | \[4 \] \[ 3\]   |



 

下列範例會從檔案 ColorBars.bmp 中，建立 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件。 然後，程式碼會將0.75 新增至影像中每個圖元的紅色元件。 原始影像會與已轉換的影像一起繪製。


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



下圖顯示左邊的原始影像，以及右邊的已轉換影像。

![顯示四個彩色橫條圖，然後具有不同色彩的相同橫條圖](images/colortrans2.png)

下表列出紅轉譯前後四個橫條的色彩向量。 請注意，因為色彩元件的最大值為1，所以第二個數據列中的紅色元件不會變更。  (同樣地，色彩元件的最小值是0。 ) 



| 原始           | 已轉譯      |
|--------------------|-----------------|
| 黑色 (0、0、0、1)  | (0.75, 0, 0, 1) |
| 紅色 (1、0、0、1)    | (1, 0, 0, 1)    |
| 綠色 (0、1、0、1)  | (0.75, 1, 0, 1) |
| 藍色 (0、0、1、1)   | (0.75, 0, 1, 1) |



 

 

 



