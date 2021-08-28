---
description: 使用色彩矩陣設定影像中的 Alpha 值的主題，會顯示變更影像 Alpha 值的非破壞性方法。
ms.assetid: 38c6254d-5191-4948-804a-1a4427aab7c6
title: 設定個別圖元的 Alpha 值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c88c7ef8cc343b99f7a50c3fad012b62ef2a8d79ab38de6988efb6b5643e0a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830728"
---
# <a name="setting-the-alpha-values-of-individual-pixels"></a>設定個別圖元的 Alpha 值

[使用色彩矩陣設定影像中的 Alpha 值](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md)的主題，會顯示變更影像 Alpha 值的非破壞性方法。 該主題中的範例會轉譯影像 semitransparently，但是點陣圖中的圖元資料並不會變更。 Alpha 值只會在轉譯期間改變。

下列範例顯示如何變更個別圖元的 Alpha 值。 範例中的程式碼實際上會變更 [**點陣圖**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) 物件中的 Alpha 資訊。 這種方法比使用色矩陣和 [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) 物件慢很多，但可讓您控制點陣圖中的個別圖元。


```
INT iWidth = bitmap.GetWidth();
INT iHeight = bitmap.GetHeight();
Color color, colorTemp;
for(INT iRow = 0; iRow < iHeight; iRow++)
{
   for(INT iColumn = 0; iColumn < iWidth; iColumn++)
   {
      bitmap.GetPixel(iColumn, iRow, &color);
      colorTemp.SetValue(color.MakeARGB(
         (BYTE)(255 * iColumn / iWidth), 
         color.GetRed(),
         color.GetGreen(),
         color.GetBlue()));
      bitmap.SetPixel(iColumn, iRow, colorTemp);
   }
}
// First draw a wide black line.
Pen pen(Color(255, 0, 0, 0), 25);
graphics.DrawLine(&pen, 10, 35, 200, 35);
// Now draw the modified bitmap.
graphics.DrawImage(&bitmap, 30, 0, iWidth, iHeight);
```



下圖顯示產生的影像。

![圖例顯示在黑色矩形上從左至右取得較不透明的影像](images/image3.png)

上述程式碼範例會使用嵌套迴圈來變更點陣圖中每個圖元的 Alpha 值。 針對每個圖元， [**bitmap：： GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) 會取得現有的色彩， [**Color：： SetValue**](/windows/desktop/api/Gdipluscolor/nf-gdipluscolor-color-setvalue) 會建立包含新 Alpha 值的暫存色彩，然後 [**bitmap：： bitmap.setpixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) 會設定新的色彩。 Alpha 值是根據點陣圖的資料行來設定。 在第一個資料行中，Alpha 設定為0。 在最後一個資料行中，Alpha 設定為255。 因此，產生的影像會從左邊緣的完全透明 () 到右邊邊緣) 的完全不透明 (。

[**Bitmap：： GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) 和 [**Bitmap：： bitmap.setpixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) 可讓您控制個別圖元值。 不過，使用 **bitmap：： GetPixel** 和 **Bitmap：： bitmap.setpixel** 並不像使用 [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) 類別和 [**ColorMatrix**](/windows/desktop/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) 結構一樣快。

 

 



