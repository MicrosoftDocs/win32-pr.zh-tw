---
description: 這個範例程式示範如何縮放和滾動筆跡。
ms.assetid: d3b5668a-29bf-4846-8ab0-1bda7b6160f9
title: 筆墨縮放範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d786fe502e1510a44df39049e845f05694a1befae0d4a21bcfa2ba2bd2b19b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939438"
---
# <a name="ink-zoom-sample"></a>筆墨縮放範例

這個範例程式示範如何縮放和滾動筆跡。 尤其是，它可讓使用者以增量方式放大和縮小墨水。 它也會示範如何使用縮放矩形來放大特定區域。 最後，此範例說明如何以不同的縮放比例收集筆跡，以及如何在縮放的繪圖區域內設定滾動。

在範例中，轉譯 [器物件的](/previous-versions/ms828481(v=msdn.10)) 視圖和物件轉換是用來執行縮放和滾動。 視圖轉換適用于點和畫筆寬度。 物件轉換只適用于點。 使用者可以在 [模式] 功能表上變更 [尺規畫筆寬度] 專案，以控制要使用的轉換。

> [!Note]  
> 在某些介面方法上執行某些 COM 呼叫會有問題， ([**InkRenderer SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform) 和 [**InkRenderer SetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)，例如在傳送訊息時) 。 傳送訊息時，必須將訊息封送處理至 POST 訊息佇列。 若要解決此案例，請測試您是否要從 POST 處理訊息，方法是呼叫 [**InSendMesssageEx**](/windows/desktop/api/winuser/nf-winuser-insendmessageex) ，並在傳送訊息時將訊息張貼給自己。

 

此範例使用下列功能：

-   [InkCollector](/previous-versions/ms583683(v=vs.100))物件
-   轉譯 [器物件](/previous-versions/ms828481(v=msdn.10)) 的 [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) 方法
-   轉譯 [器物件](/previous-versions/ms828481(v=msdn.10)) 的 [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) 方法

## <a name="initializing-the-form"></a>初始化表單

首先，此範例會參考 Windows Vista 或 Windows XP Tablet PC Edition 軟體發展工具組 (SDK) 所提供的 Tablet pc 自動化介面。


```C++
using Microsoft.Ink;
```



此範例會宣告 [InkCollector](/previous-versions/ms583683(v=vs.100))、 `myInkCollector` 和一些私用成員來協助進行調整。


```C++
// Declare the Ink Collector object
private InkCollector myInkCollector = null;
...
// The starting and ending points of the zoom rectangle
private Rectangle zoomRectangle = Rectangle.Empty;

// The current zoom factor (1 = 100% zoom level)
private float zoomFactor = 1;

// Declare constants for the width and height of the 
// drawing area (in ink space coordinates).
private const int InkSpaceWidth = 50000;
private const int InkSpaceHeight = 50000;
...
// Declare constant for the pen width used by this application
private const float MediumInkWidth = 100;
```



然後，此範例會在表單的[Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1)事件處理常式中建立並啟用[InkCollector](/previous-versions/ms583683(v=vs.100)) 。 此外，也會設定 InkCollector 物件之[system.windows.controls.inkcanvas.defaultdrawingattributes](/previous-versions/ms836500(v=msdn.10))屬性的[Width](/previous-versions/ms837941(v=msdn.10))屬性。 最後，會定義捲軸範圍，並呼叫應用程式的 `UpdateZoomAndScroll` 方法。


```C++
private void InkZoom_Load(object sender, System.EventArgs e)
{
   // Create the pen used to draw the zoom rectangle
    blackPen = new Pen(Color.Black, 1);

    // Create the ink collector and associate it with the form
    myInkCollector = new InkCollector(pnlDrawingArea.Handle);

    // Set the pen width
    myInkCollector.DefaultDrawingAttributes.Width = MediumInkWidth;

    // Enable ink collection
    myInkCollector.Enabled = true;

    // Define ink space size - note that the scroll bars
    // map directly to ink space
    hScrollBar.Minimum = 0;
    hScrollBar.Maximum = InkSpaceWidth;
    vScrollBar.Minimum = 0;
    vScrollBar.Maximum = InkSpaceHeight;

    // Set the scroll bars to map to the current zoom level
    UpdateZoomAndScroll();
}
```



## <a name="updating-the-zoom-and-scroll-values"></a>更新縮放和滾動值

筆墨收集器的繪圖區域會受到許多事件的影響。 在 `UpdateZoomAndScroll` 方法中，會使用轉換矩陣來調整和轉譯視窗內的筆墨收集器。

> [!Note]  
> 轉譯 [器物件](/previous-versions/ms828481(v=msdn.10)) 的 [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) 方法會將轉換套用至筆劃和畫筆寬度，而 [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) 方法只會將轉換套用至筆觸。

 

最後，會呼叫應用程式的 `UpdateScrollBars` 方法，並強制重新整理表單。


```C++
// Create a transformation matrix
Matrix m = new Matrix();

// Apply the current scale factor
m.Scale(zoomFactor,zoomFactor);

// Apply the current translation factor - note that since 
// the scroll bars map directly to ink space, their values
// can be used directly.
m.Translate(-hScrollBar.Value, -vScrollBar.Value);

// ...
if (miScalePenWidth.Checked)
{
    myInkCollector.Renderer.SetViewTransform(m);
}
else
{
    myInkCollector.Renderer.SetObjectTransform(m);
}

// Set the scroll bars to map to the current zoom level
UpdateScrollBars();

Refresh();
```



## <a name="managing-the-scroll-bars"></a>管理捲軸

`UpdateScrollBars`方法會設定捲軸，以在[InkCollector](/previous-versions/ms583683(v=vs.100))內的目前視窗大小、縮放設定和捲軸位置正常運作。 這個方法會計算垂直和水準捲軸的大型變更和小變更值。 它也會計算捲軸的目前值，以及是否應顯示捲軸。 轉譯 [器物件](/previous-versions/ms828481(v=msdn.10)) 的 [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) 方法會處理從圖元到縮放座標空間的轉換，以及透過視圖和物件轉換套用的任何縮放和滾動的帳戶。


```C++
// Create a point representing the top left of the drawing area (in pixels)
Point ptUpperLeft = new Point(0, 0);

// Create a point representing the size of a small change
Point ptSmallChange = new Point(SmallChangeSize, SmallChangeSize);

// Create a point representing the lower right of the drawing area (in pixels)
Point ptLowerRight = new Point(hScrollBar.Width, vScrollBar.Height);

using (Graphics g = CreateGraphics())
{
    // Convert each of the points to ink space
    myInkCollector.Renderer.PixelToInkSpace(g, ref ptUpperLeft);
    myInkCollector.Renderer.PixelToInkSpace(g, ref ptLowerRight);
    myInkCollector.Renderer.PixelToInkSpace(g, ref ptSmallChange);
}

// Set the SmallChange values (in ink space)
// Note that it is necessary to subract the upper-left point
// value to account for scrolling.
hScrollBar.SmallChange = ptSmallChange.X - ptUpperLeft.X;
vScrollBar.SmallChange = ptSmallChange.Y - ptUpperLeft.Y;

// Set the LargeChange values to the drawing area width (in ink space)
// Note that it is necessary to subract the upper-left point
// value to account for scrolling.
hScrollBar.LargeChange = ptLowerRight.X - ptUpperLeft.X;
vScrollBar.LargeChange = ptLowerRight.Y - ptUpperLeft.Y;

// If the scroll bars are not needed, hide them
hScrollBar.Visible = hScrollBar.LargeChange < hScrollBar.Maximum;
vScrollBar.Visible = vScrollBar.LargeChange < vScrollBar.Maximum;

// If the horizontal scroll bar value would run off of the drawing area, 
// adjust it
if(hScrollBar.Visible && (hScrollBar.Value + hScrollBar.LargeChange > hScrollBar.Maximum)) 
{
    hScrollBar.Value = hScrollBar.Maximum - hScrollBar.LargeChange;
}

// If the vertical scroll bar value would run off of the drawing area, 
// adjust it
if(vScrollBar.Visible && (vScrollBar.Value + vScrollBar.LargeChange > vScrollBar.Maximum))
{
    vScrollBar.Value = vScrollBar.Maximum - vScrollBar.LargeChange;
}
```



## <a name="zooming-to-a-rectangle"></a>縮放至矩形

`pnlDrawingArea`面板事件處理常式可管理將矩形繪製至視窗。 如果在 [模式] 功能表上選取 [縮放至 Rect] 命令，則 [MouseUp](/previous-versions/ms567618(v=vs.100)) 事件處理常式會呼叫應用程式的 `ZoomToRectangle` 方法。 `ZoomToRectangle`方法會計算矩形的寬度和高度、檢查界限條件、更新捲軸值和縮放因數，然後呼叫應用程式的 `UpdateZoomAndScroll` 方法以套用新的設定。

## <a name="closing-the-form"></a>關閉表單

表單的 [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) 方法會處置 [InkCollector](/previous-versions/ms583683(v=vs.100)) 物件。

 

 
