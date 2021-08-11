---
description: 當您填滿圖形時，您必須將筆刷物件的位址傳遞至 Graphics 類別的其中一個 fill 方法。
ms.assetid: 42e36c32-ed20-4c5f-bcba-004d795babe3
title: 使用不透明和半透明筆刷繪製
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce5bb89c460c9769f805fb33af9eb91e9d8207448e702476aff4d25dec33a18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118248872"
---
# <a name="drawing-with-opaque-and-semitransparent-brushes"></a>使用不透明和半透明筆刷繪製

當您填滿圖形時，您必須將 [**筆刷**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) 物件的位址傳遞至 [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 類別的其中一個 fill 方法。 [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush)函式的一個參數是 [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color)物件。 若要填滿不透明的圖形，請設定色彩的 Alpha 元件為 255。 若要填滿半透明的圖案，請設定 Alpha 元件為從 1 到 254 的任何值。

當您填滿半透明的圖案時，圖案的色彩會與背景的色彩混合。 Alpha 元件指定如何混合形狀和背景色彩;接近0的 Alpha 值會在背景色彩上放置更多權數，而接近255的 Alpha 值則會在形狀色彩上有更多的衡量。

下列範例會繪製影像，然後填滿三個重迭影像的省略號。 第一個橢圓形使用的 Alpha 元件為 255，所以是不透明的。 第二個和第三個橢圓形使用的 Alpha 元件為 128，因此是半透明的；您可以看到穿透橢圓形的背景影像。 對 [**Graphics：： SetCompositingQuality**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) 的呼叫會導致第三個橢圓形的混色與 gamma 校正一起進行。


```
Image image(L"Texture1.jpg");
graphics.DrawImage(&image, 50, 50, image.GetWidth(), image.GetHeight());
SolidBrush opaqueBrush(Color(255, 0, 0, 255));
SolidBrush semiTransBrush(Color(128, 0, 0, 255));
graphics.FillEllipse(&opaqueBrush, 35, 45, 45, 30);
graphics.FillEllipse(&semiTransBrush, 86, 45, 45, 30);
graphics.SetCompositingQuality(CompositingQualityGammaCorrected);
graphics.FillEllipse(&semiTransBrush, 40, 90, 86, 30);
```



下圖顯示上述程式碼的輸出。

![圖例顯示由三個省略號重迭的影像：一個不透明、稍微透明、一個非常透明](images/compqualellipse.png)

 

 



