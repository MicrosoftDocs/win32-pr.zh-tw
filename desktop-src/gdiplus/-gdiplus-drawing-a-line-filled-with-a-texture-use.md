---
description: 您可以使用材質繪製，而不是以純色繪製線條或曲線。
ms.assetid: 326170a5-d21f-49d6-9f60-10b9bc8d97b4
title: 繪製填滿材質的線條
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13cc8f93adee4792836c4166d5787e20d9c54040448d3a7efde36ff6a580d8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467030"
---
# <a name="drawing-a-line-filled-with-a-texture"></a>繪製填滿材質的線條

您可以使用材質繪製，而不是以純色繪製線條或曲線。 若要使用材質繪製線條和曲線，請建立 [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) 物件，並將該 **TextureBrush** 物件的位址傳遞給 [**畫筆**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) 的函式。 與材質筆刷相關聯的影像會用來將平面 (為不可見的) ，而且當畫筆繪製線條或曲線時，畫筆的筆觸會顯示磚材質的特定圖元。

下列範例會從檔案 Texture1.jpg 建立 [**映射**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件。 該映射是用來建立 [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) 物件，而 **TextureBrush** 物件則是用來建立 [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) 物件。 圖形的呼叫 [**：:D rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint_inint_inint)) 會繪製影像，其左上角為 (0，0) 。 對圖形的呼叫 [**：:D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) 使用 **Pen** 物件來繪製有紋理的橢圓形。


```
Image         image(L"Texture1.jpg");
TextureBrush  tBrush(&image);
Pen           texturedPen(&tBrush, 30);

graphics.DrawImage(&image, 0, 0, image.GetWidth(), image.GetHeight());
graphics.DrawEllipse(&texturedPen, 100, 20, 200, 100);
```



下圖顯示影像和紋理橢圓形。

![顯示小型矩形影像的圖例，以及填滿原始影像的橢圓線條區段](images/pens7.png)

 

 
