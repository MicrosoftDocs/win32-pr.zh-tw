---
description: Graphics 類別是 Windows GDI + 的核心。 若要繪製任何內容，您可以建立繪圖物件、設定其屬性，以及呼叫其方法 ( DrawLine、DrawImage、DrawString 和 like) 。
ms.assetid: 7d70f9fe-c0b2-4d65-815d-483d06df96ad
title: 圖形物件的狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661733f944b08633b5df84eed3ac488e612d9e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550626"
---
# <a name="the-state-of-a-graphics-object"></a>圖形物件的狀態

[**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別是 WINDOWS gdi + 的核心。 若要繪製任何內容，您可以建立 **圖形** 物件、設定其屬性，以及呼叫其方法 ( [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))、 [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint))、 [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))和 like) 。

下列範例會建立 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件和 [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen)物件，然後呼叫 **graphics 物件** 的 [**graphics：:D rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint))方法：


```
HDC          hdc;
PAINTSTRUCT  ps;

hdc = BeginPaint(hWnd, &ps);
{
   Graphics graphics(hdc);
   Pen pen(Color(255, 0, 0, 255));  // opaque blue
   graphics.DrawRectangle(&pen, 10, 10, 200, 100);
}
EndPaint(hWnd, &ps);
```



在上述程式碼中， [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) 方法會將控制碼傳回至裝置內容，並將該控制碼傳遞給 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 的函式。 裝置內容是由 Windows) 所維護的結構 (，其中保存所使用之特定顯示裝置的相關資訊。

## <a name="graphics-state"></a>圖形狀態

[**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件會比提供繪圖方法更多，例如 [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))和 [graphicswindow.drawrectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint))。 **圖形** 物件也會維持圖形狀態，可分為下列類別：

-   裝置內容的連結
-   品質設定
-   轉換
-   裁剪區域

### <a name="device-context"></a>裝置內容

作為應用程式的程式設計人員，您不需要考慮 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件與其裝置內容之間的互動。 這項互動是由 GDI + 在幕後處理。

### <a name="quality-settings"></a>品質設定

[**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件有數個屬性，會影響在螢幕上繪製的專案品質。 您可以藉由呼叫 get 和 set 方法來查看和操作這些屬性。 例如，您可以呼叫 [**Graphics：： SetTextRenderingHint**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) 方法來指定要套用至文字的任何) 的消除鋸齒類型 (。 影響品質的其他 set 方法如下 [**： graphics：： SetSmoothingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode)、 [**Graphics：： SetCompositingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingmode)、 [**Graphics：： SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality)和 [**Graphics：： SetInterpolationMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setinterpolationmode)。

下列範例會繪製兩個省略號，一個將平滑模式設定為 [* * * * SmoothingModeAntiAlias *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) * *，另一個則將平滑模式設定為 [* * * * SmoothingModeHighSpeed *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)* * *：


```
Graphics graphics(hdc);
Pen pen(Color(255, 0, 255, 0));  // opaque green

graphics.SetSmoothingMode(SmoothingModeAntiAlias);
graphics.DrawEllipse(&pen, 0, 0, 200, 100);
graphics.SetSmoothingMode(SmoothingModeHighSpeed);
graphics.DrawEllipse(&pen, 0, 150, 200, 100);
```



### <a name="transformations"></a>轉換

[**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件會維護兩個轉換 (世界和頁面) ，並套用至該 **圖形** 物件所繪製的所有專案。 任何仿射轉換都可以儲存在全球轉換中。 仿射轉換包括調整、旋轉、反映、扭曲和轉譯。 頁面轉換可用於調整規模，以及變更單位 (例如，圖元到英寸) 。 如需轉換的詳細資訊，請參閱 [座標系統和轉換](-gdiplus-coordinate-systems-and-transformations-about.md)。

下列範例會設定 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件的世界和頁面轉換。 「世界」轉換是設定為30度的旋轉。 已設定頁面轉換，以便將座標傳遞給第二個 [**圖形：:D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) 會被視為毫米而不是圖元。 此程式碼會對圖形進行兩個相同的呼叫 **：:D rawellipse** 方法。 全球轉換會套用至第一個 **圖形：:D rawellipse** 呼叫，而 (世界和頁面) 的轉換都會套用至第二個 **圖形：:D rawellipse** 呼叫。


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0));

graphics.ResetTransform();
graphics.RotateTransform(30.0f);            // World transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
graphics.SetPageUnit(UnitMillimeter);       // Page transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
```



下圖顯示兩個省略號。 請注意，30度的旋轉是關於座標系統的原點 (工作區) 的左上角，而非省略號的中心。 另請注意，畫筆寬度1表示第一個橢圓形為1圖元，第二個橢圓形則為1毫米。

![視窗的螢幕擷取畫面，其中包含小型、細橢圓形和大型、較粗的橢圓形](images/graphicsascon1.png)

 

### <a name="clipping-region"></a>裁剪區域

[**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件會維護套用至該 **圖形** 物件所繪製之所有專案的裁剪區域。 您可以藉由呼叫 [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) 方法來設定裁剪區域。

下列範例會建立兩個矩形的聯集，藉以建立一個形狀區域。 該區域會指定為 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件的裁剪區域。 然後，程式碼會繪製兩行，限制為裁剪區域的內部。


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0), 5);  // opaque red, width 5
SolidBrush brush(Color(255, 180, 255, 255));  // opaque aqua

// Create a plus-shaped region by forming the union of two rectangles.
Region region(Rect(50, 0, 50, 150));
region.Union(Rect(0, 50, 150, 50));
graphics.FillRegion(&brush, &region);

// Set the clipping region.
graphics.SetClip(&region);

// Draw two clipped lines.
graphics.DrawLine(&pen, 0, 30, 150, 160);
graphics.DrawLine(&pen, 40, 20, 190, 150);
```



下圖顯示已裁剪的行。

![圖例顯示以兩條對角線（紅線）交叉的彩色形狀](images/graphicsascon2.png)

 

 
