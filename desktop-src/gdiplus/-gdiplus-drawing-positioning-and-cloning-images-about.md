---
description: 您可以使用 Image 類別， (點陣圖) 和向量影像 (中繼檔) ，來載入和顯示點陣影像。
ms.assetid: 0ad2a132-6db6-4099-81a2-10e1cd1b1f61
title: 繪製、定位和複製影像
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e37e53ce3937d4f10b91a92e64feec57c6b39e718e7b551e4e4130569d4dd90d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015148"
---
# <a name="drawing-positioning-and-cloning-images"></a>繪製、定位和複製影像

您可以使用 [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) 類別， (點陣圖) 和向量影像 (中繼檔) ，來載入和顯示點陣影像。 若要顯示影像，您需要 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件和 **image** 物件。 **Graphics** 物件提供 [**圖形：:D rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint))方法，它會接收 **影像** 物件的位址做為引數。

下列範例會從檔案中建立 [**影像**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) 物件 Climber.jpg 然後顯示影像。 影像左上角的目的點（ (10，10) ）是在圖形的第二個和第三個參數中指定 [**：:D rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) 方法。


```
Image myImage(L"Climber.jpg");
myGraphics.DrawImage(&myImage, 10, 10);
```



上述程式碼和特定檔案 Climber.jpg，會產生下列輸出。

![包含相片之視窗的螢幕擷取畫面](images/aboutgdip03-art04.png)

您可以從各種圖形檔案格式來建立 [**影像**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) 物件： BMP、GIF、JPEG、EXIF、PNG、TIFF、WMF、EMF 和圖示。

下列範例會根據各種檔案類型來建立 [**影像**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) 物件，然後顯示影像。


```
Image myBMP(L"SpaceCadet.bmp");
Image myEMF(L"Metafile1.emf");
Image myGIF(L"Soda.gif");
Image myJPEG(L"Mango.jpg");
Image myPNG(L"Flowers.png");
Image myTIFF(L"MS.tif");

myGraphics.DrawImage(&myBMP, 10, 10);
myGraphics.DrawImage(&myEMF, 220, 10);
myGraphics.DrawImage(&myGIF, 320, 10);
myGraphics.DrawImage(&myJPEG, 380, 10);
myGraphics.DrawImage(&myPNG, 150, 200);
myGraphics.DrawImage(&myTIFF, 300, 200);
```



[**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)類別提供 [**Image：： Clone**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-image-clone)方法，可讓您用來建立現有 **影像**、[**中繼檔**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile)或 [**點陣圖**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap)物件的複本。 [Clone](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-bitmap-clone(inconstrectf__inpixelformat))方法在 **Bitmap** 類別中多載，其中一個變化具有來源矩形參數，您可以用來指定要複製的原始影像部分。 下列範例會藉由複製現有 **點陣圖** 物件的上半部來建立 **點陣圖** 物件。 然後會顯示這兩個影像。


```
Bitmap* originalBitmap = new Bitmap(L"Spiral.png");
RectF sourceRect(
   0.0f,
   0.0f, 
   (REAL)(originalBitmap->GetWidth()), 
   (REAL)(originalBitmap->GetHeight())/2.0f);

Bitmap* secondBitmap = originalBitmap->Clone(sourceRect, PixelFormatDontCare);

myGraphics.DrawImage(originalBitmap, 10, 10);
myGraphics.DrawImage(secondBitmap, 100, 10);
```



上述程式碼和特定檔案 Spiral.png，會產生下列輸出。

![影像的圖例，後面接著原始影像的上半部](images/aboutgdip03-art05.png)

 

 
