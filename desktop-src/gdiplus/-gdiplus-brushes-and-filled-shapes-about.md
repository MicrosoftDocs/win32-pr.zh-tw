---
description: 封閉的圖形（例如矩形或橢圓形）包含外框和內部。
ms.assetid: 889558d5-9181-43ff-b862-e92966324208
title: 筆刷和填滿的圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eb772be88ce26325337fd9c88fc0319631895e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558427"
---
# <a name="brushes-and-filled-shapes"></a>筆刷和填滿的圖形

封閉的圖形（例如矩形或橢圓形）包含外框和內部。 大綱是以 [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 物件繪製，而內部則填滿筆 [**刷**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) 物件。 Windows GDI + 提供數個筆刷類別來填滿封閉的圖形： [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush)、 [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush)、 [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)、 [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)和 [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush)。 所有這些類別都是繼承自 **筆刷** 類別。 下圖顯示填滿實心筆刷的矩形，以及填滿影線筆刷的橢圓形。

![顯示藍色矩形的圖例，以及填滿藍色影線圖樣的洋紅橢圓形](images/aboutgdip02-art17.png)

 

-   [實心筆刷](#solid-brushes)
-   [影線筆刷](#hatch-brushes)
-   [材質筆刷](#texture-brushes)
-   [漸層筆刷](#gradient-brushes)

## <a name="solid-brushes"></a>實心筆刷

若要填滿封閉的圖形，您需要 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件和 [**筆刷**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) 物件。 **Graphics** 物件提供方法（例如 [graphicswindow.fillrectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_))和 [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inconstrectf_))），而 **筆刷** 物件會儲存填滿的屬性，例如色彩和模式。 **筆刷** 物件的位址會做為 fill 方法的其中一個引數傳遞。 下列範例會以紅色的紅色色彩填滿橢圓形。


```
SolidBrush mySolidBrush(Color(255, 255, 0, 0));
myGraphics.FillEllipse(&mySolidBrush, 0, 0, 60, 40);
```



請注意，在上述範例中，筆刷的型別為 [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush)，其繼承自 [**筆刷**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush)。

## <a name="hatch-brushes"></a>影線筆刷

當您填滿具有影線筆刷的圖形時，您會指定前景色彩、背景色彩和影線樣式。 前景色彩是影線的色彩。


```
HatchBrush myHatchBrush(
   HatchStyleVertical, 
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0));
```



GDI + 提供超過50的影線樣式，在 [**HatchStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-hatchstyle)中指定。 下圖顯示的三種樣式為水準、ForwardDiagonal 和交叉。

![顯示三個青灰色橢圓形的圖例，各有不同的影線樣式](images/aboutgdip02-art18.png)

 

## <a name="texture-brushes"></a>材質筆刷

您可以使用紋理筆刷，以點陣圖中儲存的模式來填滿圖形。 例如，假設下圖儲存在名為 MyTexture.bmp 的磁片檔中。

![以各種色彩填滿之小方塊的螢幕擷取畫面](images/aboutgdip02-art19.png)

下列範例會藉由重複儲存在 MyTexture.bmp 中的圖片來填滿橢圓形。


```
Image myImage(L"MyTexture.bmp");
TextureBrush myTextureBrush(&myImage);
myGraphics.FillEllipse(&myTextureBrush, 0, 0, 100, 50);
```



下圖顯示已填滿的橢圓形。

![顯示填滿先前定義之模式的省略號的圖例](images/aboutgdip02-art20.png)

 

## <a name="gradient-brushes"></a>漸層筆刷

您可以使用漸層筆刷來填滿圖形，其色彩會從圖形的某個部分逐漸變更為另一個部分。 例如，當您從圖表的左邊移至右側時，水準漸層筆刷將會變更色彩。 下列範例會填滿具有水準漸層筆刷的橢圓形，當您從橢圓形的左邊移至右側時，會從藍色變更為綠色。


```
LinearGradientBrush myLinearGradientBrush(
   myRect,
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0),
   LinearGradientModeHorizontal);
myGraphics.FillEllipse(&myLinearGradientBrush, myRect); 
```



下圖顯示已填滿的橢圓形。

![圖例顯示具有漸層填滿的橢圓形：左邊的藍色靠右至綠色](images/aboutgdip02-art21.png)

路徑漸層筆刷可以設定為當您從圖表的中心移到界限時變更色彩。

![ilustration 置中為深藍色的橢圓形，邊緣的陰影至淺藍色](images/aboutgdip02-art22.png)

路徑漸層筆刷相當有彈性。 用來填滿下圖中三角形的漸層筆刷，會從中間的紅色逐漸變成頂點的三種不同色彩。

![在中間以紅色表示的三角形圖例，每個頂點的色彩為不同的色彩](images/aboutgdip02-art23.png)

 

 



