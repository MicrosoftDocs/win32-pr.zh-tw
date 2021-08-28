---
description: 您可以使用 Image 類別和 TextureBrush 類別，以紋理填滿封閉的圖形。
ms.assetid: 12e1e132-a93f-4438-8a1d-9036a43a8fd8
title: 使用影像材質填滿形狀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 323accd1d9ac7e844566808b9c53586921fa83d33e9453dd50db20c3b15f2519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118067194"
---
# <a name="filling-a-shape-with-an-image-texture"></a>使用影像材質填滿形狀

您可以使用 [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 類別和 [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) 類別，以紋理填滿封閉的圖形。

下列範例會使用影像填滿橢圓形。 程式碼會建立 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件，然後將該 **影像** 物件的位址當作引數傳遞給 [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) 的函式。 第三個程式碼語句會調整影像，而第四個語句會使用縮放影像的重複複本來填滿橢圓形：


```
Image image(L"ImageFile.jpg");
TextureBrush tBrush(&image);
stat = tBrush.SetTransform(&Matrix(75.0/640.0, 0.0f, 0.0f,
   75.0/480.0, 0.0f, 0.0f));
stat = graphics.FillEllipse(&tBrush,Rect(0, 150, 150, 250));
```



在上述程式碼範例中， [**TextureBrush：： SetTransform**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-texturebrush-settransform) 方法會設定在繪製之前套用至影像的轉換。 假設原始影像的寬度為640圖元，高度為480圖元。 轉換會藉由設定水準和垂直縮放比例值，將影像縮減為75×75。

> [!Note]  
> 在上述範例中，影像大小為75×75，而橢圓大小為150×250。 因為影像小於其填滿的橢圓，所以橢圓形會與影像並排顯示。 圖格表示影像會以水準和垂直方式重複，直到達到圖形界限為止。 如需並排顯示的詳細資訊，請參閱 [使用影像將圖形平鋪](-gdiplus-tiling-a-shape-with-an-image-use.md)。

 

 

 



