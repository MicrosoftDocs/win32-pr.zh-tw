---
title: 裁剪和縮放 GDI + 影像
description: Graphics 類別提供數個 DrawImage 方法，其中有些具有來源和目的地矩形參數，可讓您用來裁剪和縮放影像。
ms.assetid: cad64615-d8e6-4c03-a6c7-c98267a8f159
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c70a7b4f7aa0374602326ab856a01bbadc0047
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988012"
---
# <a name="cropping-and-scaling-gdi-images"></a>裁剪和縮放 GDI + 影像

[**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別提供數個 **DrawImage** 方法，其中有些具有來源和目的地矩形參數，可讓您用來裁剪和縮放影像。

下列範例會從檔案 Apple.gif 中，建立 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件。 程式碼會以原始大小繪製整個 apple 影像。 然後，程式碼會呼叫 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件的 **DrawImage** 方法，以在大於原始 apple 影像的目的矩形中繪製 apple 影像的一部分。

**DrawImage** 方法會藉由查看來源矩形（由第三個、第四個、第五個和第六個引數指定）來判斷要繪製的 apple 部分。 在此情況下，apple 會裁剪為其寬度的75% 和其高度的75%。

**DrawImage** 方法會藉由查看目的地矩形（由第二個引數指定）來決定要在何處繪製裁剪的 apple，以及要如何建立裁剪的 apple。 在此情況下，目的地矩形的寬度為30%，而高於原始影像的高度為30%。


```
Image image(L"Apple.gif");
UINT width = image.GetWidth();
UINT height = image.GetHeight();
// Make the destination rectangle 30 percent wider and
// 30 percent taller than the original image.
// Put the upper-left corner of the destination
// rectangle at (150, 20).
Rect destinationRect(150, 20, 1.3 * width, 1.3 * height);
// Draw the image unaltered with its upper-left corner at (0, 0).
graphics.DrawImage(&image, 0, 0);
// Draw a portion of the image. Scale that portion of the image
// so that it fills the destination rectangle.
graphics.DrawImage(
   &image,
   destinationRect,
   0, 0,              // upper-left corner of source rectangle
   0.75 * width,      // width of source rectangle
   0.75 * height,     // height of source rectangle
   UnitPixel);
```



下圖顯示原始的 apple 和已調整的已裁剪 apple。

![顯示 apple 的圖例，然後是原始 apple 的放大部分](images/cropscale1.png)

 

 



