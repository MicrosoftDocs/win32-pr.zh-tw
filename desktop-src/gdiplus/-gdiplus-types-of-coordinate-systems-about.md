---
description: Windows GDI + 會使用三個座標空間：世界、頁面和裝置。
ms.assetid: eb20f5e9-25f5-4f27-8ea5-83f6819425ed
title: 座標系統類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e259f43d4fc0d6a74021f3a6125f85652f51ac95
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120623"
---
# <a name="types-of-coordinate-systems"></a>座標系統類型

Windows GDI + 會使用三個座標空間：世界、頁面和裝置。 當您進行呼叫時 `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` ，您傳遞給圖形的點 [**：:D rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) 方法（ (0、0) 和 (160、80) ）位於全局座標空間中。 在 GDI + 可以在螢幕上繪製線條之前，座標會傳遞一連串的轉換。 一個轉換會將全局座標轉換成頁面座標，而另一個轉換會將頁面座標轉換成裝置座標。

假設您想要使用在用戶端區域主體中，而不是左上角的座標系統。 例如，假設您想要原點從工作區的左邊緣到100圖元，並從工作區的最上方取得50圖元。 下圖顯示這類座標系統。

![包含標示座標軸之視窗的螢幕擷取畫面](images/aboutgdip05-art01.png)

當您進行呼叫時 `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` ，會取得下圖所示的行。

![上一個視窗的螢幕擷取畫面，但具有從原點對角線擴充的藍線](images/aboutgdip05-art02.png)

在三個座標空間中，線條的端點座標如下所示：



| Space       |  端點座標                       |
|--------|-------------------------|
| World  |  (0、0)  (160、80)      |
| 頁面   |  (100、50)  (260、130)  |
| 裝置 |  (100、50)  (260、130)  |



 

請注意，頁面座標空間的原點位於工作區的左上角;這一律會是這種情況。 另請注意，由於測量單位是圖元，因此裝置座標與頁面座標相同。 如果您將量值的單位設定為圖元以外的某個值 (例如，[英寸]) ，則裝置座標將會與頁面座標不同。

將全局座標對應到頁面座標的轉換稱為「 *世界」轉換* ，而且是由 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件所維護。 在上述範例中，全球轉換是 x 方向的平移100單位和 y 方向的50單位。 下列範例會設定 **圖形** 物件的世界轉換，然後使用該 **圖形** 物件來繪製上圖所示的線條。


```
myGraphics.TranslateTransform(100.0f, 50.0f);

myGraphics.DrawLine(&myPen, 0, 0, 160, 80);
```



將頁面座標對應至裝置座標的轉換稱為「 *頁面」轉換*。 [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別提供四種方法來操作和檢查頁面轉換： [**Graphics：： SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit)、 [**graphics：： GetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit)、 [**graphics：： SetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale)和 [**Graphics：： GetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale)。 **Graphics** 類別也提供兩種方法，也就是 [**圖形：： GetDpiX**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix)和 [**Graphics：： GetDpiY**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy)，用於檢查顯示裝置的每英寸水準和垂直點。

您可以使用 [**graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的 [**Graphics：： SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit)方法來指定測量單位。 下列範例會從 (0、0) 到 (2、1) ，其中 point (2，1) 是2英寸左右，1英寸從點 (0，0) 。


```
myGraphics.SetPageUnit(UnitInch);

myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



> [!Note]
> 如果您在建立畫筆時未指定畫筆寬度，則上一個範例會繪製寬度為一的線條。 您可以將第二個引數中的畫筆寬度指定為 [**畫筆**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) 的函式：
> <br/><br/>
> `Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.

 

如果我們假設顯示裝置的水準方向有96個點，而垂直方向的96點為每英寸，則上一個範例中的線條端點在三個座標空間中具有下列座標：



| Space       | 端點座標                    |
|--------|---------------------|
| World  |  (0、0) 至 (2、1)     |
| 頁面   |  (0、0) 至 (2、1)     |
| 裝置 |  (0、0、 (192、96)  |



 

您可以結合世界和頁面轉換來達成各種效果。 例如，假設您想要使用英寸作為度量單位，而您想要將座標系統的原點從工作區的左邊緣到2英寸，從工作區的最上方開始為1/2 英寸。 下列範例會設定 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件的世界和頁面轉換，然後從 (0，0) 到 (2，1) 繪製線條。


```
myGraphics.TranslateTransform(2.0f, 0.5f);
myGraphics.SetPageUnit(UnitInch);
myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



下圖顯示線條和座標系統。

![上一個視窗的螢幕擷取畫面，但範圍較寬，且軸位於左方且標示不同](images/aboutgdip05-art03.png)

如果我們假設顯示裝置的水準方向有96個點，而垂直方向的96點為每英寸，則上一個範例中的線條端點在三個座標空間中具有下列座標：



| Space       | 端點座標                        |
|--------|-------------------------|
| World  |  (0、0) 至 (2、1)         |
| 頁面   |  (2、0.5) 至 (4、1.5)     |
| 裝置 |  (192、48)  (384、144)  |



 

 

 
