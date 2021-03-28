---
description: 下列各節說明使用 Windows GDI + 進行程式設計的幾種方式，與 Windows 圖形裝置介面 (GDI) 的程式設計不同。
ms.assetid: 89a154c1-6a49-45d6-a73c-94b0b1567408
title: 程式設計模型中的變更
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a90cd6f1c3a6ebab1e55562e67cb4926f0ffedf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026600"
---
# <a name="changes-in-the-programming-model"></a>程式設計模型中的變更

下列各節說明使用 Windows GDI + 進行程式設計的幾種方式，與 Windows 圖形裝置介面 (GDI) 的程式設計不同。

-   [裝置內容、控制碼和繪圖物件](#device-contexts-handles-and-graphics-objects)
-   [繪製線條的兩種方式](#two-ways-to-draw-a-line)
    -   [使用 GDI 繪製線條](#drawing-a-line-with-gdi)
    -   [使用 GDI + 和 c + + 類別介面繪製線條](#drawing-a-line-with-gdi-and-the-c-class-interface)
-   [畫筆、筆刷、路徑、影像和字型作為參數](#pens-brushes-paths-images-and-fonts-as-parameters)
-   [方法多載](#method-overloading)
-   [目前沒有最新位置](#no-more-current-position)
-   [個別繪製和填滿方法](#separate-methods-for-draw-and-fill)
-   [建立區域](#constructing-regions)

## <a name="device-contexts-handles-and-graphics-objects"></a>裝置內容、控制碼和繪圖物件

如果您已經使用 GDI 撰寫程式 (舊版 Windows) 中所包含的圖形裝置介面，您就會熟悉裝置內容 (DC) 的概念。 裝置內容是 Windows 用來儲存特定顯示裝置功能相關資訊的結構，以及指定如何在該裝置上繪製專案的屬性。 影片顯示器的裝置內容也會與顯示畫面上的特定視窗相關聯。 首先，您會取得 (HDC) 的裝置內容控制碼，然後將該控制碼當作引數傳遞至實際進行繪圖的 GDI 函數。 您也會將控制碼當作引數傳遞至 GDI 函數，以取得或設定裝置內容的屬性。

當您使用 GDI + 時，您不必擔心控制碼和裝置內容，就像使用 GDI 一樣。 您只需建立 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件，然後使用熟悉的物件導向樣式（MyGraphicsObject. *DrawLine ()* 中的方法來叫用其方法。 **圖形** 物件是 gdi + 的核心，就像裝置內容是 gdi 的核心一樣。 裝置內容和 **圖形** 物件會扮演類似的角色，但搭配裝置內容使用的以控制碼為基礎的程式設計模型之間有一些基本差異 (gdi) 以及與 **圖形** 物件搭配使用的面向物件模型 (gdi +) 。

[**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件（例如裝置內容）會與畫面上的特定視窗相關聯，並包含屬性 (例如，平滑模式和文字轉譯提示) ，指定如何繪製專案。 不過， **圖形** 物件不會系結至畫筆、筆刷、路徑、影像或字型，因為裝置內容是。 例如，在 GDI 中，您必須先呼叫 [SelectObject](/windows/win32/api/wingdi/nf-wingdi-selectobject) ，以將畫筆物件與裝置內容產生關聯，才能使用裝置內容來繪製線條。 這稱為在裝置內容中選取畫筆。 在裝置內容中繪製的所有線條都將使用該畫筆，直到您選取不同的畫筆為止。 使用 GDI + 時，您會將 [**畫筆**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen)物件當作引數傳遞至 **Graphics** 類別的 [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal))方法。 您可以在每一系列的 DrawLine 呼叫中使用不同的 **畫筆** 物件，而不需要將指定的 **畫筆** 物件與 **圖形** 物件產生關聯。

## <a name="two-ways-to-draw-a-line"></a>繪製線條的兩種方式

下列兩個範例都會從位置 (20、10) 到位置 (200100) ，繪製一個寬度為3的紅線。 第一個範例會呼叫 GDI，而第二個範例會透過 c + + 類別介面呼叫 GDI +。

-   [使用 GDI 繪製線條](#drawing-a-line-with-gdi)
-   [使用 GDI + 和 c + + 類別介面繪製線條](#drawing-a-line-with-gdi-and-the-c-class-interface)

### <a name="drawing-a-line-with-gdi"></a>使用 GDI 繪製線條

若要使用 GDI 來繪製線條，您需要兩個物件：裝置內容和畫筆。 您可以藉由呼叫 [**BeginPaint**](/windows/win32/api/winuser/nf-winuser-beginpaint)來取得裝置內容的控制碼，並藉由呼叫 [CreatePen](/windows/win32/api/wingdi/nf-wingdi-createpen)來取得畫筆的控制碼。 接下來，您會呼叫 [SelectObject](/windows/win32/api/wingdi/nf-wingdi-selectobject) ，以在裝置內容中選取畫筆。 您可以藉由呼叫 [MoveToEx](/windows/win32/api/wingdi/nf-wingdi-movetoex) ，將畫筆位置設定為 (20，10) ，然後藉由呼叫 **LineTo**，從畫筆位置將線條拖曳至 (200，100) 。 請注意，MoveToEx 和 [LineTo](/windows/win32/api/wingdi/nf-wingdi-lineto) 都是以引數的形式接收 **hdc** 。


```
HDC          hdc;
PAINTSTRUCT  ps;
HPEN         hPen;
HPEN         hPenOld;
hdc = BeginPaint(hWnd, &ps);
   hPen = CreatePen(PS_SOLID, 3, RGB(255, 0, 0));
   hPenOld = (HPEN)SelectObject(hdc, hPen);
   MoveToEx(hdc, 20, 10, NULL);
   LineTo(hdc, 200, 100);
   SelectObject(hdc, hPenOld);
   DeleteObject(hPen);
EndPaint(hWnd, &ps);
```



### <a name="drawing-a-line-with-gdi-and-the-c-class-interface"></a>使用 GDI + 和 c + + 類別介面繪製線條

若要繪製具有 GDI + 和 c + + 類別介面的線條，您需要 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件和 [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 物件。 請注意，您不會要求 Windows 提供這些物件的控制碼。 相反地，您會使用函式來建立圖形 **類別的實例， (** **圖形** 物件) ，而 **畫筆類別的** 實例 () 的 **畫筆** 物件。 繪製線條需要呼叫 **圖形類別的**[**圖形：:D rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal))方法。 **Graphics：:D rawline** 方法的第一個參數是您的 **Pen** 物件的指標。 這是較簡單且更有彈性的配置，比在裝置內容中選取畫筆更簡單且更有彈性，如先前的 GDI 範例所示。


```
HDC          hdc;
PAINTSTRUCT  ps;
Pen*         myPen;
Graphics*    myGraphics;
hdc = BeginPaint(hWnd, &ps);
   myPen = new Pen(Color(255, 255, 0, 0), 3);
   myGraphics = new Graphics(hdc);
   myGraphics->DrawLine(myPen, 20, 10, 200, 100);
   delete myGraphics;
   delete myPen;
EndPaint(hWnd, &ps);
```



## <a name="pens-brushes-paths-images-and-fonts-as-parameters"></a>畫筆、筆刷、路徑、影像和字型作為參數

上述範例顯示 [**畫筆**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 物件可以與提供繪圖方法的 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件分開建立和維護。 [**筆刷**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush)、 [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath)、 [**影像**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)和 [**字型**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) 物件也可以與 **圖形** 物件分開建立和維護。 **圖形** 類別所提供的許多繪圖方法都會接收 **筆刷**、 **GraphicsPath**、**影像** 或 **字型** 物件做為引數。 例如， **筆刷** 物件的位址會做為引數傳遞至 [graphicswindow.fillrectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) 方法，並將 **GraphicsPath** 物件的位址當作引數傳遞給 [**圖形：:D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) 方法。 同樣地，會將 **影像** 和 **字型** 物件的位址傳遞給 [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_)) 和 [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) 方法。 這與您在裝置內容中選取筆刷、路徑、影像或字型，然後將控制碼傳遞給裝置內容以做為繪圖函式引數的 GDI 相反。

## <a name="method-overloading"></a>方法多載

許多 GDI + 方法都有多載;也就是說，有數個方法共用相同名稱，但有不同的參數清單。 例如， [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的 [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal))方法有下列形式：


```
Status DrawLine(IN const Pen* pen,
                IN REAL x1,
                IN REAL y1,
                IN REAL x2,
                IN REAL y2);
Status DrawLine(IN const Pen* pen,
                IN const PointF& pt1,
                IN const PointF& pt2);
Status DrawLine(IN const Pen* pen,
                IN INT x1,
                IN INT y1,
                IN INT x2,
                IN INT y2);
    
Status DrawLine(IN const Pen* pen,
                IN const Point& pt1,
                IN const Point& pt2);
```



上方的四個 [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) 變化都會收到 [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 物件的指標、起點的座標，以及結束點的座標。 前兩個變化會以浮點數的形式接收座標，最後兩個變化會以整數的形式接收座標。 第一個和第三個變化會以四個不同數位的清單來接收座標，而第二個和第四個變化會以一對 [**點**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) (或 [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)) 物件的方式接收座標。

## <a name="no-more-current-position"></a>目前沒有最新位置

請注意，在先前顯示的 [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) 方法中，會以引數的形式接收該行的起始點和結束點。 這是來自 GDI 配置的 MoveToEx，您可以在其中呼叫來設定目前的畫筆位置 **和 LineTo** ，以便繪製從 (**x1** 開始的線條、 **y1**) ，並在 (**x2**， **y2**) 結束。 以 GDI + 作為整體，已放棄目前位置的概念。

## <a name="separate-methods-for-draw-and-fill"></a>個別繪製和填滿方法

當您繪製外框和填滿矩形的內部形狀時，GDI + 比 GDI 更有彈性。 GDI 有一個 [矩形](/windows/win32/api/wingdi/nf-wingdi-rectangle) 函式，可在一個步驟中繪製輪廓並填滿矩形的內部。 大綱會以目前選取的畫筆繪製，而內部會填入目前選取的筆刷。


```
hBrush = CreateHatchBrush(HS_CROSS, RGB(0, 0, 255));
hPen = CreatePen(PS_SOLID, 3, RGB(255, 0, 0));
SelectObject(hdc, hBrush);
SelectObject(hdc, hPen);
Rectangle(hdc, 100, 50, 200, 80);
```



GDI + 有個別的方法來繪製外框，並填滿矩形的內部。 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的 [Graphicswindow.drawrectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inreal_inreal_inreal_inreal))方法具有 Pen 物件的位址做為它的其中一個參數，而 [graphicswindow.fillrectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal))方法將 [**筆**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen)[**刷**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush)物件的位址當作其中一個參數。


```
HatchBrush* myHatchBrush = new HatchBrush(
   HatchStyleCross,
   Color(255, 0, 255, 0),
   Color(255, 0, 0, 255));
Pen* myPen = new Pen(Color(255, 255, 0, 0), 3);
myGraphics.FillRectangle(myHatchBrush, 100, 50, 100, 30);
myGraphics.DrawRectangle(myPen, 100, 50, 100, 30);
```



請注意，GDI + 中的 [graphicswindow.fillrectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) 和 [graphicswindow.drawrectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inreal_inreal_inreal_inreal)) 方法會接收引數，以指定矩形的左邊緣、頂端、寬度和高度。 這與 GDI[矩形](/windows/win32/api/wingdi/nf-wingdi-rectangle) 函式相反，它接受的引數會指定矩形的左邊緣、右邊緣、頂端和底部。 另請注意，GDI + 中 [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) 類別的函式有四個參數。 最後三個參數是一般的紅色、綠色和藍色值;第一個參數是 Alpha 值，指定要繪製的色彩與背景色彩混合的範圍。

## <a name="constructing-regions"></a>建立區域

GDI 提供數個功能來建立區域： CreateRectRgn、CreateEllpticRgn、CreateRoundRectRgn、CreatePolygonRgn 和 CreatePolyPolygonRgn。 您可能預期 GDI + 中的 [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) 類別具有類似的函式，可採用矩形、橢圓形、圓角矩形和多邊形做為引數，但並非如此。 GDI + 中的 **Region** 類別會提供一個函式，此函式會接收 [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) 物件參考，而另一個則是接收 [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) 物件位址的函數。 如果您想要根據橢圓形、圓角矩形或多邊形來建立區域，您可以輕鬆地建立包含橢圓形的 **GraphicsPath** 物件 (，例如) ，然後將該 **GraphicsPath** 物件的位址傳遞至 **區域** 的函式。

GDI + 可結合圖形和路徑，讓您輕鬆形成複雜的區域。 [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region)類別具有聯 [集](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-union(inconstrectf_))和 [交集](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-intersect(inconstgraphicspath))方法，可讓您用來以路徑或其他區域增強現有的區域。 GDI + 配置有一項不錯的功能，就是當 [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) 物件做為引數傳遞至 **區域** 的函式時，不會終結該物件。 在 GDI 中，您可以使用 [PathToRegion](/windows/win32/api/wingdi/nf-wingdi-pathtoregion) 函式來轉換區域的路徑，但在進程中終結路徑。 此外，當 **GraphicsPath** 物件的位址做為引數傳遞至 Union 或 Intersect 方法時，不會終結該物件，因此您可以使用指定的路徑作為數個不同區域的建立區塊。 下列範例會顯示這一點。 假設 **onePath** 是 **GraphicsPath** 物件的指標， (已初始化的簡單或複雜) 。


```
Region  region1(rect1);
Region  region2(rect2);
region1.Union(onePath);
region2.Intersect(onePath);
```



 

 
