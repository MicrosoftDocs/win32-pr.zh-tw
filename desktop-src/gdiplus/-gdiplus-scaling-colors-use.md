---
description: 縮放轉換會將四個色彩元件中的一或多個數位相乘。 下表提供代表縮放的色彩矩陣專案。
ms.assetid: 08347831-7100-4220-a83b-693bb7b98ccb
title: 調整色彩
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7877db07ff1a11dcb985f8b0ca8ec3cc017f25fe45f00e989c9108891f8ff1ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036366"
---
# <a name="scaling-colors"></a>調整色彩

縮放轉換會將四個色彩元件中的一或多個數位相乘。 下表提供代表縮放的色彩矩陣專案。



| 要調整的元件 | 矩陣專案 |
|------------------------|--------------|
| 紅色                    | \[0 \] \[ 0\]   |
| 綠色                  | \[1 \] \[ 1\]   |
| 藍色                   | \[2 \] \[ 2\]   |
| Alpha                  | \[3 \] \[ 3\]   |



 

下列範例會從檔案 ColorBars2.bmp 中，建立 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件。 然後，程式碼會將影像中每個圖元的藍色元件調整為2倍。 原始影像會與已轉換的影像一起繪製。


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



下圖顯示左邊的原始影像和右邊的縮放影像。

![顯示四個彩色橫條圖，然後顯示具有不同色彩的相同橫條。](images/colortrans3.png)

下表顯示藍色縮放前後四個橫條的色彩向量。 請注意，第四個色軸中的藍色元件是從0.8 到0.6。 這是因為 GDI+ 只保留結果的小數部分。 例如， (2)  (0.8) = 1.6，1.6 的小數部分則是0.6。 只保留小數部分可確保結果一律為間隔 \[ 0，1 \] 。



| 原始           | 規模             |
|--------------------|--------------------|
| (0.4, 0.4, 0.4, 1) | (0.4, 0.4, 0.8, 1) |
| (0.4, 0.2, 0.2, 1) | (0.4, 0.2, 0.4, 1) |
| (0.2, 0.4, 0.2, 1) | (0.2, 0.4, 0.4, 1) |
| (0.4, 0.4, 0.8, 1) | (0.4, 0.4, 0.6, 1) |



 

下列範例會從檔案 ColorBars2.bmp 中，建立 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件。 然後，程式碼會調整影像中每個圖元的紅色、綠色和藍色元件。 紅色的元件會相應減少25%，綠色的元件會相應減少35%，而且藍色的元件會相應減少50%。


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



下圖顯示左邊的原始影像和右邊的縮放影像。

![顯示四個彩色橫條圖，然後顯示具有不同色彩的橫條](images/colortrans4.png)

下表顯示紅色、綠色和藍色調整前後四個橫條的色彩向量。



| 原始           | 規模               |
|--------------------|----------------------|
| (0.6, 0.6, 0.6, 1) | (0.45, 0.39, 0.3, 1) |
| (0, 1, 1, 1)       | (0, 0.65, 0.5, 1)    |
| (1, 1, 0, 1)       | (0.75, 0.65, 0, 1)   |
| (1, 0, 1, 1)       | (0.75, 0, 0.5, 1)    |



 

 

 



