---
description: 當您繪製線條時，您必須將 Pen 物件的位址傳遞至 Graphics 類別的 DrawLine 方法。
ms.assetid: 4524908f-f9c2-4807-b045-eb9e43a6668b
title: 繪製不透明和半透明線條
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14cdf31a80be9ac2a0cf61a2a8eb82f530dc3558c876cba9190a79f42ac35baa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036756"
---
# <a name="drawing-opaque-and-semitransparent-lines"></a>繪製不透明和半透明線條

當您繪製線條時，您必須將 [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen)物件的位址傳遞至 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的 [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))方法。 **畫筆** 參數的其中一個參數是 [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color)物件。 若要繪製不透明的線條，請將色彩的 Alpha 元件設為 255。 若要繪製半透明線條，請將 Alpha 元件設為從 1 到 254 的任何值。

當您在背景上繪製半透明線條時，線條的色彩會與背景的色彩混合。 Alpha 元件指定如何混合線條和背景色彩;接近0的 Alpha 值會在背景色彩上放置更多權數，而接近255的 Alpha 值則會線上條色彩上放置更多的衡量。

下列範例會繪製影像，然後繪製使用影像做為背景的三行。 第一條線使用的 Alpha 元件為 255，所以是不透明的。 第二和第三條線使用的 Alpha 元件為 128，因此是半透明的；您可以透過線條看到背景影像。 對 [**Graphics：： SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) 的呼叫會導致第三行的混合與 gamma 校正一起進行。


```
Image image(L"Texture1.jpg");
graphics.DrawImage(&image, 10, 5, image.GetWidth(), image.GetHeight());
Pen opaquePen(Color(255, 0, 0, 255), 15);
Pen semiTransPen(Color(128, 0, 0, 255), 15);
graphics.DrawLine(&opaquePen, 0, 20, 100, 20);
graphics.DrawLine(&semiTransPen, 0, 40, 100, 40);
graphics.SetCompositingQuality(CompositingQualityGammaCorrected);
graphics.DrawLine(&semiTransPen, 0, 60, 100, 60);
```



下圖顯示上述程式碼的輸出。

![圖例顯示由三個寬線覆迭的影像：一個不透明、一個稍微透明，還有一個非常透明](images/compqualline.png)

 

 



