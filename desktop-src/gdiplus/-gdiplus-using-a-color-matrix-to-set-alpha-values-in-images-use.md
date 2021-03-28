---
description: Bitmap 類別 (繼承自 Image 類別) ，而 ImageAttributes 類別則提供取得和設定圖元值的功能。
ms.assetid: e3d67431-6098-4b2a-8910-5695a8473216
title: 使用色彩矩陣設定影像中的 Alpha 值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81180b1f09b11e37b322e37106dab1879a00bbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511368"
---
# <a name="using-a-color-matrix-to-set-alpha-values-in-images"></a>使用色彩矩陣設定影像中的 Alpha 值

[**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap)類別 (繼承自 [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)類別) ，而 [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes)類別則提供取得和設定圖元值的功能。 您可以使用 **ImageAttributes** 類別來修改整個影像的 Alpha 值，也可以呼叫 **Bitmap** 類別的 [**bitmap：： bitmap.setpixel**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel)方法來修改個別圖元值。 如需設定個別圖元值的詳細資訊，請參閱 [設定個別圖元的 Alpha 值](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md)。

下列範例會繪製寬黑色的線條，然後顯示包含該行一部分的不透明影像。


```
Bitmap bitmap(L"Texture1.jpg");
Pen pen(Color(255, 0, 0, 0), 25);
// First draw a wide black line.
graphics.DrawLine(&pen, Point(10, 35), Point(200, 35));
// Now draw an image that covers part of the black line.
graphics.DrawImage(&bitmap,
   Rect(30, 0, bitmap.GetWidth(), bitmap.GetHeight()));
```



下圖顯示產生的影像，其繪製在 (30，0) 。 請注意，寬黑色線不會透過影像顯示。

![顯示不透明影像重迭黑色矩形的圖例](images/image1.png)

[**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes)類別有許多屬性，可讓您在轉譯期間用來修改影像。 在下列範例中， **ImageAttributes** 物件是用來將所有 Alpha 值設定為其目前值的80%。 這是藉由初始化色彩矩陣，並將矩陣中的 Alpha 縮放比例值設定為0.8 來完成。 色彩矩陣的位址會傳遞至 **ImageAttributes** 物件的 [**ImageAttributes：： SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix)方法，而 **ImageAttributes** 物件的位址會傳遞給 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件的 [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_))方法。


```
// Create a Bitmap object and load it with the texture image.
Bitmap bitmap(L"Texture1.jpg");
Pen pen(Color(255, 0, 0, 0), 25);
// Initialize the color matrix.
// Notice the value 0.8 in row 4, column 4.
ColorMatrix colorMatrix = {1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
                           0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
                           0.0f, 0.0f, 1.0f, 0.0f, 0.0f,
                           0.0f, 0.0f, 0.0f, 0.8f, 0.0f,
                           0.0f, 0.0f, 0.0f, 0.0f, 1.0f};
// Create an ImageAttributes object and set its color matrix.
ImageAttributes imageAtt;
imageAtt.SetColorMatrix(&colorMatrix, ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
// First draw a wide black line.
graphics.DrawLine(&pen, Point(10, 35), Point(200, 35));
// Now draw the semitransparent bitmap image.
INT iWidth = bitmap.GetWidth();
INT iHeight = bitmap.GetHeight();
graphics.DrawImage(
   &bitmap, 
   Rect(30, 0, iWidth, iHeight),  // Destination rectangle
   0,                             // Source rectangle X 
   0,                             // Source rectangle Y
   iWidth,                        // Source rectangle width
   iHeight,                       // Source rectangle height
   UnitPixel, 
   &imageAtt);
```



在轉譯期間，點陣圖中的 Alpha 值會轉換成其所處的80%。 這會產生與背景混合的影像。 如下圖所示，點陣圖影像看起來是透明的;您可以在上面看到實心黑色線條。

![類似于前一個圖例的圖例，但影像是 sem 透明的](images/image2.png)

影像在背景的白色部分上，影像已與白色色彩混合。 影像與黑色線相交時，影像會與黑色色彩混合。

 

 



