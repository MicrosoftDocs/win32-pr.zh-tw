---
description: Windows GDI+ 提供可讓您用來在繪圖物件中暫時取代或增強部分狀態的容器。
ms.assetid: f3fce8ef-903a-4b9d-b76c-562739d02eb3
title: 巢狀圖形容器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d88b3a768e5b156eb5d28410ad69d58227e9660618764ca4b084b5e35662b839
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114978"
---
# <a name="nested-graphics-containers"></a>巢狀圖形容器

Windows GDI+ 提供可讓您用來在 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件中暫時取代或增強部分狀態的容器。 您可以藉由呼叫 **graphics** 物件的 [**Graphics：： BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit))方法來建立容器。 您可以重複呼叫 **Graphics：： BeginContainer** 來形成嵌套的容器。

## <a name="transformations-in-nested-containers"></a>嵌套容器中的轉換

下列範例會在該 **圖形** 物件中建立 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件和容器。 **圖形** 物件的世界轉換是 x 方向的平移100單位和 y 方向的80單位。 容器的世界轉換是30度的旋轉。 程式碼會進行呼叫


```
DrawRectangle(&pen, -60, -30, 120, 60)
```



兩次。 第一次呼叫 [**圖形：:D rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) 在 *容器內*;也就是說，呼叫 [**圖形：： BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) 與 [**Graphics：： EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)之間的呼叫。 第二次呼叫 **圖形：:D rawrectangle** 在呼叫 **Graphics：： EndContainer** 之後。


```
Graphics           graphics(hdc);
Pen                pen(Color(255, 255, 0, 0));
GraphicsContainer  graphicsContainer;

graphics.TranslateTransform(100.0f, 80.0f);

graphicsContainer = graphics.BeginContainer();
   graphics.RotateTransform(30.0f);
   graphics.DrawRectangle(&pen, -60, -30, 120, 60);
graphics.EndContainer(graphicsContainer);

graphics.DrawRectangle(&pen, -60, -30, 120, 60);
```



在上述程式碼中，從容器內繪製的矩形會先由容器的世界轉換 (旋轉) ，然後由 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件的世界轉換 (轉譯) 進行轉換。 從容器外部繪製的矩形只會在 **圖形** 物件的世界轉換 (轉譯) 轉換。 下圖顯示兩個矩形。

![視窗的螢幕擷取畫面，其中有兩個紅色矩形位於相同的點，但有不同的旋轉](images/nestedcontainers1.png)

 

## <a name="clipping-in-nested-containers"></a>在嵌套容器中裁剪

下列範例說明嵌套容器如何處理裁剪區域。 程式碼會建立 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件和該 **圖形** 物件內的容器。 **圖形** 物件的裁剪區域是一個矩形，而容器的裁剪區域則是一個橢圓形。 此程式碼會對圖形進行兩個呼叫 [**：:D rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) 方法。 第一次呼叫 **圖形：:D rawline** 在容器內，而第二次呼叫圖形 **：:D rawline** 是在呼叫 [**Graphics：： EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)) 之後 (容器之外。 這兩個裁剪區域的交集會裁剪第一行。 第二行只會由 **圖形** 物件的矩形裁剪區域裁剪。


```
Graphics           graphics(hdc);
GraphicsContainer  graphicsContainer;
Pen                redPen(Color(255, 255, 0, 0), 2);
Pen                bluePen(Color(255, 0, 0, 255), 2);
SolidBrush         aquaBrush(Color(255, 180, 255, 255));
SolidBrush         greenBrush(Color(255, 150, 250, 130));

graphics.SetClip(Rect(50, 65, 150, 120));
graphics.FillRectangle(&aquaBrush, 50, 65, 150, 120);

graphicsContainer = graphics.BeginContainer();
   // Create a path that consists of a single ellipse.
   GraphicsPath path;
   path.AddEllipse(75, 50, 100, 150);

  // Construct a region based on the path.
   Region region(&path);
   graphics.FillRegion(&greenBrush, &region);

   graphics.SetClip(&region);
   graphics.DrawLine(&redPen, 50, 0, 350, 300);
graphics.EndContainer(graphicsContainer);

graphics.DrawLine(&bluePen, 70, 0, 370, 300);
```



下圖顯示兩個剪下的行。

![矩形內橢圓形的圖例，其中有一個線條由橢圓形剪下，另一個線條由矩形裁剪](images/nestedcontainers2.png)

如同上述兩個範例所示，轉換和裁剪區域在嵌套的容器中是累計的。 如果您設定容器和 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件的世界轉換，則這兩種轉換將會套用至從容器內繪製的專案。 容器的轉換將會先套用，而 **圖形** 物件的轉換將會第二個套用。 如果您設定容器和 **圖形** 物件的裁剪區域，則從容器內繪製的專案將會被兩個裁剪區域的交集所修剪。

## <a name="quality-settings-in-nested-containers"></a>嵌套容器中的品質設定

在嵌套容器中 ( [**SmoothingMode**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)、 [**TextRenderingHint**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)和 like) 的品質設定不是累積的;相反地，容器的品質設定會暫時取代 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件的品質設定。 當您建立新的容器時，該容器的品質設定會設定為預設值。 例如，假設您有一個具有平滑模式 [* * * * SmoothingModeAntiAlias *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)* * 的 **圖形** 物件。 當您建立容器時，容器內的平滑模式是預設的平滑模式。 您可以自由設定容器的平滑模式，而從容器內繪製的任何專案都會根據您設定的模式繪製。 在呼叫 [**圖形：： EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)之後繪製的專案，將會根據在 [**圖形：： BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit))的呼叫之前所處的平滑模式 ([* * * * SmoothingModeAntiAlias * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) *) 繪製。

## <a name="several-layers-of-nested-containers"></a>多層的嵌套容器

您不受限於 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件中的一個容器。 您可以建立一系列的容器，每個都在上述各嵌套，而且您可以指定每個這些嵌套容器的世界轉換、剪下區域和品質設定。 如果您從最內層的容器內呼叫繪圖方法，轉換將依序套用，從最內層的容器開始，並以最外層的容器結束。 從最內層容器內繪製的專案，將會由所有裁剪區域的交集來裁剪。

下列範例會建立 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件，並將其文字轉譯提示設定為 [* * * * TextRenderingHintAntiAlias * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)* *。 程式碼會建立兩個容器，一個在另一個容器內。 外部容器的文字轉譯提示會設定為 [* * * * TextRenderingHintSingleBitPerPixel *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)* *，而內部容器的文字轉譯提示會設定為 [* * * * TextRenderingHintAntiAlias * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)* *。 此程式碼會繪製三個字串：一個來自內部容器、一個來自外部容器，另一個來自 **圖形** 物件本身。


```
Graphics graphics(hdc);
GraphicsContainer innerContainer;
GraphicsContainer outerContainer;
SolidBrush brush(Color(255, 0, 0, 255));
FontFamily fontFamily(L"Times New Roman");
Font font(&fontFamily, 36, FontStyleRegular, UnitPixel);

graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);

outerContainer = graphics.BeginContainer();

   graphics.SetTextRenderingHint(TextRenderingHintSingleBitPerPixel);

   innerContainer = graphics.BeginContainer();
      graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
      graphics.DrawString(L"Inner Container", 15, &font,
         PointF(20, 10), &brush);
   graphics.EndContainer(innerContainer);

   graphics.DrawString(L"Outer Container", 15, &font, PointF(20, 50), &brush);

graphics.EndContainer(outerContainer);

graphics.DrawString(L"Graphics Object", 15, &font, PointF(20, 90), &brush);
```



下圖顯示三個字串。 從內部容器和 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件繪製的字串會透過消除鋸齒來進行平滑處理。 因為 TextRenderingHintSingleBitPerPixel 設定，所以從外部容器繪製的字串不會因消除鋸齒而經過平滑處理。

![矩形的圖例，其中包含相同的字串。只有第一行和最後一行的字元是平滑的](images/nestedcontainers3.png)

 

 
