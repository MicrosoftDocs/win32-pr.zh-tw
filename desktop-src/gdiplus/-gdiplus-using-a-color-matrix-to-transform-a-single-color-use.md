---
description: Windows GDI + 提供用來儲存和操作影像的影像和點陣圖類別。
ms.assetid: fcd7f3d9-8bad-44f8-8c9c-c2f5df4a7241
title: 使用色彩矩陣轉換單一色彩
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db56d0a64c36c08a5415d76e3fb184158d473268
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560435"
---
# <a name="using-a-color-matrix-to-transform-a-single-color"></a>使用色彩矩陣轉換單一色彩

Windows GDI + 提供用來儲存和操作影像的 [**影像**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) 和 [**點陣圖**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) 類別。 **影像** 和 **點陣圖** 物件會將每個圖元的色彩儲存為32位數位：紅色、綠色、藍色和 Alpha 各有8位。 四個元件的每一個都是從0到255的數位，0代表沒有濃度，而255代表完整強度。 Alpha 元件會指定色彩的透明度：0是完全透明的，而255則完全不透明。

色彩向量是表單的4個元組， (紅色、綠色、藍色、Alpha) 。 例如，色彩向量 (0、255、0、255) 代表沒有紅色或藍色的不透明色彩，但具有全強度的綠色。

表示色彩的另一個慣例會使用數位1來表示最大強度，並使用數位0表示最小強度。 使用該慣例時，上一段所述的色彩會以向量 (0、1、0、1) 表示。 GDI + 在執行色彩轉換時，會使用1的慣例作為完整強度。

您可以將線性轉換 (旋轉、縮放和類似的) ，藉由使用4×4矩陣來乘以色彩向量。 不過，您無法使用4×4矩陣來執行 (非線性) 的轉譯。 如果您新增了虛擬的第五座標 (例如，數位 1) 至每個色彩向量，則可以使用5×5矩陣來套用線性轉換和翻譯的任何組合。 由線性轉換所組成的轉換，後面接著平移，稱為仿射轉換。 代表仿射轉換的5×5矩陣稱為4個空間轉換的同質矩陣。 5×5同質矩陣的第五個數據列和第五個數據行中的元素必須是1，而第五個數據行中的所有其他專案都必須是0。

例如，假設您想要從色彩 (0.2、0.0、0.4、1.0) 開始，並套用下列轉換：

1.  兩倍的紅色元件
2.  將0.2 新增至紅色、綠色和藍色的元件

下列矩陣乘法將依列出的循序執行一組轉換。

![圖例顯示數位的5x1 矩陣乘以5x5 矩陣，以建立新的5x1 矩陣](images/recoloring01.png)

色彩矩陣的元素會根據 (以零為基礎的) 依資料列和資料行來編制索引。 例如，第五個數據列和第三個數據行中的專案會以 M \[ 4 \] \[ 2 表示 \] 。

下圖中所示的5×5識別矩陣 (，) 在對角線上具有1s，其他地方則為0。 如果您將色彩向量乘以標識矩陣，色彩向量不會變更。 形成色彩轉換矩陣的方便方式，就是從標識矩陣開始著手，然後再進行一項小變更來產生所需的轉換。

![顯示5x5 身分識別矩陣的圖例;從左上角到右下角的 1-10，其他地方則為0](images/recoloring02.png)

如需矩陣和轉換的詳細討論，請參閱 [座標系統和轉換](-gdiplus-coordinate-systems-and-transformations-about.md)。

下列範例會取得全為一種色彩 (0.2、0.0、0.4、1.0) 的影像，並套用先前段落中所述的轉換。


```
Image            image(L"InputColor.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   2.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 1.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 1.0f, 0.0f,
   0.2f, 0.2f, 0.2f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10);

graphics.DrawImage(
   &image, 
   Rect(120, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



下圖顯示左邊的原始影像，以及右邊的已轉換影像。

![圖例顯示以深色純色填滿的矩形，然後以較淺的純色填滿一個 ](images/colortrans1.png)

上述範例中的程式碼會使用下列步驟來執行重新著色：

1.  初始化 [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) 結構。
2.  建立 [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes)物件，並將 [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix)結構的位址傳遞至 **ImageAttributes** 物件的 [**ImageAttributes：： SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix)方法。
3.  將 [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes)物件的位址傳遞至 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件的 [DrawImage 方法](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint))方法。

 

 



