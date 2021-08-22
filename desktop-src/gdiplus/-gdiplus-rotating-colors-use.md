---
description: 四維色彩空間中的旋轉很難視覺化。
ms.assetid: 099f76a3-2da3-4f2b-8f8d-557d144451dc
title: 旋轉色彩
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc09a84c4c51181c672c549369783ac476fa1d3c79f1598c1c29ca14604429d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036426"
---
# <a name="rotating-colors"></a>旋轉色彩

四維色彩空間中的旋轉很難視覺化。 我們可以藉由同意保持固定的其中一個色彩元件，讓您更輕鬆地將旋轉視覺化。 假設我們同意將 Alpha 元件固定在 1 (完全不透明) 。 然後我們可以使用紅色、綠色和藍色軸來視覺化三維色彩空間，如下圖所示。

![以紅色、綠色和藍色軸標示之三維色彩空間的觀點視圖圖例](images/recoloring03.png)

您可以將色彩視為立體空間中的點。 例如，點 (1，0，0) 空間代表紅色，而點 (0，1，0) 在空間中代表綠色。

下圖顯示在 Red-Green 平面中，將色彩 (1、0、0) 旋轉為60度的意義。 平行至 Red-Green 平面的平面旋轉可以視為與藍色軸有關的旋轉。

![圖例顯示點 (1、0、0) 旋轉60度到 (0.5、0.866、0) ](images/recoloring04.png)

下圖顯示如何初始化色彩矩陣，以執行三個座標軸的旋轉 (紅色、綠色、藍色) 。

![圖例顯示可執行每個座標軸之旋轉的色彩矩陣](images/recoloring05.png)

下列範例會取得全部為1、0、0.6)  (1、0、的影像，並套用60度的旋轉（關於藍色軸）。 旋轉的角度會在與 Red-Green 平面平行的平面中掃除。


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



下圖顯示左邊的原始影像和右邊的彩色旋轉影像。

![圖例顯示填滿原始影像的矩形 (紫羅蘭紅) 和彩色旋轉影像 (海綠色) ](images/colortrans5.png)

上述程式碼範例中執行的色彩旋轉可以視覺化方式呈現，如下所示。

![顯示3-d 色彩空間的圖例，以及 (1，0，0.6) 旋轉60度的點， (0.5、0.866、0.6) ](images/recoloring06.png)

 

 



