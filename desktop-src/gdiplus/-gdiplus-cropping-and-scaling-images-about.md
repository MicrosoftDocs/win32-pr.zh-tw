---
title: 關於裁剪和縮放 GDI+ 影像
description: 您可以使用 Graphics 類別的 DrawImage 方法來繪製和放置影像。
ms.assetid: 81d20adc-0481-4b1b-80aa-ae218fdecd84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9e69adb7f817c36b955ed313290cf0b762c279b4296e06ad52aa6175ff2c467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036836"
---
# <a name="about-cropping-and-scaling-gdi-images"></a>關於裁剪和縮放 GDI+ 影像

您可以使用 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的 [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_))方法來繪製和放置影像。 DrawImage 是一種多載的方法，因此您可以透過數種方式提供引數給它。 圖形的一個變化 [**：:D rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) 方法會接收 [**影像**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) 物件的位址和 [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) 物件的參考。 矩形會指定繪圖作業的目的地;也就是說，它會指定要在其中繪製影像的矩形。 如果目的地矩形的大小與原始影像的大小不同，則影像會縮放以符合目的地矩形。 下列範例會繪製相同的影像三次：一次沒有調整、一次展開，以及一次壓縮。


```
Bitmap myBitmap(L"Spiral.png");
Rect expansionRect(80, 10, 2 * myBitmap.GetWidth(), myBitmap.GetHeight());
Rect compressionRect(210, 10, myBitmap.GetWidth() / 2, 
   myBitmap.GetHeight() / 2);

myGraphics.DrawImage(&myBitmap, 10, 10);
myGraphics.DrawImage(&myBitmap, expansionRect);
myGraphics.DrawImage(&myBitmap, compressionRect);
```



上述程式碼和特定檔案 Spiral.png，會產生下列輸出。

![顯示影像的三個版本的圖例：標準、延伸寬，以及壓縮成原始大小的一半](images/aboutgdip03-art06.png)

圖形的部分變化 [**：:D rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) 方法具有來源矩形參數，以及目的地矩形參數。 來源矩形會指定將繪製的原始影像部分。 目的地矩形會指定將繪製影像部分的位置。 如果目的地矩形的大小與來源矩形的大小不同，則影像會縮放以符合目的地矩形。

下列範例會從檔案 Runner.jpg 中，建立 [**點陣圖**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) 物件。 在 (0、0) 的情況下繪製整個影像，而不會進行縮放。 然後，影像的一小部分會繪製兩次：一次使用壓縮，一次進行擴充。


```
Bitmap myBitmap(L"Runner.jpg"); 

// The rectangle (in myBitmap) with upper-left corner (80, 70), 
// width 80, and height 45, encloses one of the runner's hands.

// Small destination rectangle for compressed hand.
Rect destRect1(200, 10, 20, 16);

// Large destination rectangle for expanded hand.
Rect destRect2(200, 40, 200, 160);

// Draw the original image at (0, 0).
myGraphics.DrawImage(&myBitmap, 0, 0);

// Draw the compressed hand.
myGraphics.DrawImage(
   &myBitmap, destRect1, 80, 70, 80, 45, UnitPixel);

// Draw the expanded hand. 
myGraphics.DrawImage(
   &myBitmap, destRect2, 80, 70, 80, 45, UnitPixel);
```



下圖顯示未縮放的影像，以及壓縮和展開的影像部分。

![顯示影像的螢幕擷取畫面，其中已壓縮影像的一部分，然後展開相同部分](images/aboutgdip03-art07.png)

 

 



