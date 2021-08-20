---
description: 此程式示範如何將筆墨複製並貼到另一個應用程式。 它也可讓使用者複製選取的筆劃，然後將結果貼入現有的筆跡物件中。
ms.assetid: a0c42f1c-543d-44f8-83d9-fe810de410ff
title: 筆墨剪貼簿範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73aa8acdf785321dc01706d4a4de50e0a2673a31250edbfa4316a27aecd0ce3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032326"
---
# <a name="ink-clipboard-sample"></a>筆墨剪貼簿範例

此程式示範如何將筆墨複製並貼到另一個應用程式。 它也可讓使用者複製選取的筆劃，然後將結果貼入現有的筆跡物件中。

可用的剪貼簿模式如下：

-    (ISF 的筆墨序列化格式) 
-    中繼檔
-   加強型中繼檔 (EMF) 
-   點陣圖
-   文字筆墨
-   草圖筆墨

文字筆跡和草圖筆墨是兩種類型的筆墨控制項，分別用來做為文字或繪圖。 您可以貼上 ISF、文字筆墨，然後將筆墨草圖至現有筆跡。

除了剪貼簿之外，此範例也會說明如何使用「套索」工具來選取筆觸。 使用者可以移動選取的筆劃並修改其繪製屬性。 這項功能是筆墨重迭控制項已提供的選取功能的子集;它是在這裡執行，以供說明之用。

此範例使用下列功能：

-   [InkCollector](/previous-versions/ms583683(v=vs.100))物件。
-   筆墨剪貼簿支援。
-   搭配使用 [system.windows.media.visualtreehelper.hittest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) 方法與套索的用法。

這個範例會示範如何轉譯筆墨、複製該筆墨，然後將筆墨貼到另一個應用程式（例如 Microsoft 小畫家）。

## <a name="collecting-ink-and-setting-up-the-form"></a>收集筆墨並設定表單

首先，請參考隨 Microsoft Windows <entity type="reg"/> XP Tablet pc Edition 軟體發展工具組 (SDK) 一起安裝的 Tablet pc 自動化介面。


```C++
using Microsoft.Ink;
```



接下來，此表單會宣告一些常數和欄位，此範例稍後會加以注明。


```C++
// Declare constant for the size of the border around selected strokes
private const int SelectedInkWidthIncrease = 105;

// Declare constant for the size of a lasso point
private const int DotSize = 6;

// Declare constant for the spacing between lasso points
private const int DotSpacing = 7;

// Declare constant for the selection rectangle padding
private const int SelectionRectBuffer = 8;

// Declare constant for the lasso hit test percent (specifies how much
// of the stoke must fall within the lasso in order to be selected).
private const float LassoPercent = 50;
...
// Declare the InkCollector object
private InkCollector myInkCollector = null;

// The points in the selection lasso
private ArrayList lassoPoints = null;

// The array of rectangle selection handles
private PictureBox[] selectionHandles;

// The rectangle that bounds the selected strokes
private Rectangle selectionRect = Rectangle.Empty;

// The strokes that have been selected by the lasso
private Strokes selectedStrokes = null;
...
// Declare the colors used in the selection lasso
private Color dotEdgeColor = Color.White;
private Color dotColor = SystemColors.Highlight;
private Color connectorColor = Color.Black;

// Declare the pens used to draw the selection lasso
private Pen connectorPen = null;
private Pen dotEdgePen = null;
private Pen dotPen = null;
```



最後，在表單的 [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) 事件處理常式中，會將表單初始化、建立表單的 [InkCollector](/previous-versions/ms583683(v=vs.100)) 物件，並啟用筆墨收集器。


```C++
// Create an ink collector and assign it to this form's window
myInkCollector = new InkCollector(this.Handle);

// Turn the ink collector on
myInkCollector.Enabled = true;
```



## <a name="handling-menu-events"></a>處理功能表事件

功能表項目事件處理常式主要會更新表單的狀態。

Clear 命令會移除選取矩形，並從筆墨收集器的 [筆墨](/previous-versions/ms583670(v=vs.100)) 物件刪除筆觸。

Exit 命令會在結束應用程式之前停用筆墨收集器。

[編輯] 功能表會根據表單的選取狀態來啟用剪下和複製命令，並根據 [剪貼簿] 的內容啟用 [貼上] 命令（使用 [筆墨](/previous-versions/ms583670(v=vs.100)) 物件的 [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) 方法來判斷）。

剪下和複製命令都使用 helper 方法將筆墨複製到剪貼簿。 剪下命令會使用 helper 方法來刪除選取的筆劃。

[貼上] 命令會先檢查 [筆墨](/previous-versions/ms583670(v=vs.100)) 物件的 [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) 方法，以查看是否可以貼上剪貼簿上的物件。 然後，貼上命令會計算貼上區域的左上角，將座標從圖元轉換成筆墨空間，然後將剪貼簿中的筆觸貼到筆墨收集器。 最後，選取方塊也會更新。


```C++
if (myInkCollector.Ink.CanPaste())
{
   // Compute the location where the ink should be pasted;
    // this location should be shifted from the origin
    // to account for the width of the selection rectangle's handle.
    Point offset = new Point(leftTopHandle.Width+1,leftTopHandle.Height+1);
    using (Graphics g = CreateGraphics())
    {
        myInkCollector.Renderer.PixelToInkSpace(g, ref offset);
    }
    // Use Ink API to paste the clipboard data into the Ink
    Strokes pastedStrokes = myInkCollector.Ink.ClipboardPaste(offset);

    // If the contents of the clipboard were a valid format 
    // (Ink Serialized Format or Embeddable OLE Object) and at
    // least one stroke was pasted into the ink, use a helper 
    // method to update the stroke selection.  Otherwise,
    // the result is null and this paste becomes a no-op.  
    if (null != pastedStrokes)
    {
        SetSelection(pastedStrokes);
    }
}
```



Select 和 Ink 命令會更新應用程式模式和預設的繪圖屬性、清除目前的選取專案、更新功能表狀態，以及重新整理表單。 其他處理常式會依賴應用程式狀態來執行正確的函式，也就是 lassoing 或配置筆墨。 此外，Select 命令會將 [NewPackets](/previous-versions/ms567621(v=vs.100)) 和 [筆觸](/previous-versions/ms567622(v=vs.100)) 事件處理常式加入至筆墨收集器，而筆墨命令會將這些事件處理常式從筆墨收集器中移除。

複製筆劃時，剪貼簿上可用的格式會列在 [格式] 功能表上，而使用者則會選取從這份清單複製筆墨的格式。 可用格式的類型包括筆跡序列化格式 (ISF) 、中繼檔、增強的中繼檔和點陣圖。 草圖筆墨和文字筆墨格式互斥，而且會依賴將筆墨複製到剪貼簿作為 OLE 物件。

樣式功能表可讓使用者變更畫筆的色彩和寬度屬性，以及任何選取的筆劃。

例如，紅色的命令會將筆墨收集器的[system.windows.controls.inkcanvas.defaultdrawingattributes](/previous-versions/ms571711(v=vs.100))屬性[色彩](/previous-versions/ms582103(v=vs.100))屬性設為紅色。 因為資料[指標](/previous-versions/ms552104(v=vs.100))物件的[DrawingAttributes](/previous-versions/ms581965(v=vs.100))屬性尚未設定，所以繪製至筆墨收集器的任何新筆墨都會繼承至預設繪圖色彩。 此外，如果目前已選取任何筆劃，則也會更新每個筆劃的繪圖屬性色彩屬性。


```C++
private void SetColor(Color newColor)
{
    myInkCollector.DefaultDrawingAttributes.Color = newColor;

    // In addition to updating the ink collector, also update
    // the drawing attributes of all selected strokes.
    if (HasSelection())
    {
        foreach (Stroke s in selectedStrokes)
        {
            s.DrawingAttributes.Color = newColor;
        }
    }

    Refresh();
}
```



## <a name="handling-mouse-events"></a>處理滑鼠事件

[MouseMove](/previous-versions/ms567617(v=vs.100))事件處理常式會檢查應用程式模式。 如果模式為 MoveInk，而滑鼠按鍵已關閉，則處理常式會使用 [筆觸](/previous-versions/ms552701(v=vs.100)) 集合的 Move 方法來移動筆劃，並更新選取方塊。 否則，處理常式會檢查以判斷選取範圍矩形是否包含游標、是否啟用筆跡收集，以及據以設定游標。

[MouseDown](/previous-versions/ms567616(v=vs.100))事件處理常式會檢查資料指標的設定。 如果資料指標設定為 [SizeAll](/dotnet/api/system.windows.forms.cursors.sizeall?view=netcore-3.1)，則處理常式會將應用程式模式設定為 MoveInk，並記錄資料指標的位置。 否則，如果有目前的選取範圍，請清除它。

[MouseUp](/previous-versions/ms567618(v=vs.100))事件處理常式會檢查應用程式模式。 如果模式為 MoveInk，則處理常式會根據選取的命令核取狀態來設定應用程式模式。

當筆墨收集器收到新的封包資料時， [NewPackets](/previous-versions/ms567621(v=vs.100)) 事件會在選取模式中引發。 如果應用程式處於選取模式，則必須攔截新的封包，並使用它們來繪製選取的套索。

每個封包的座標都會轉換成圖元（受限於繪圖區域），並加入至套索的點集合。 接著會呼叫 helper 方法，以在表單上繪製套索。

## <a name="handling-a-new-stroke"></a>處理新的筆劃

繪製新的筆劃時，會在選取模式中引發 [筆劃](/previous-versions/ms567622(v=vs.100)) 事件。 如果應用程式處於選取模式，此筆觸會對應至套索，而且必須更新所選筆劃的資訊。

處理常式會取消 [筆劃](/previous-versions/ms567622(v=vs.100)) 事件、檢查兩個以上的套索點、將點集合複製到 [Point](/dotnet/api/system.drawing.point?view=netcore-3.1) 物件陣列，並將陣列中點的座標從圖元轉換成筆墨空間。 然後，此處理程式會使用 [筆墨](/previous-versions/ms583670(v=vs.100)) 物件的 [system.windows.media.visualtreehelper.hittest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) 方法來取得套索點選取的筆觸，並更新表單的選取狀態。 最後，引發事件的筆劃會從所選筆劃的集合中移除，而套索點集合會清空，而 helper 方法會繪製選取矩形。


```C++
// This stroke corresponds to the lasso - 
// cancel it so that it is not added into the ink
e.Cancel = true;  

Strokes hitStrokes = null;

// If there are enough lasso points, perform a hit test
// to determine which strokes were selected. 
if (lassoPoints.Count > 2)
{

    // Convert the lasso points from pixels to ink space
    Point[] inkLassoPoints = (Point[])lassoPoints.ToArray(typeof(Point));
    using (Graphics g = CreateGraphics())
    {
        myInkCollector.Renderer.PixelToInkSpace(g, ref inkLassoPoints);
    }
    // Perform a hit test on this ink collector's ink to
    // determine which points were selected by the lasso stroke.
    //
    // Note that there is a slight inefficiency here since the
    // lasso stroke is part of the ink and, therefore, part of the
    // hit test - even though we don't need it.   It would have 
    // been more efficient to remove the stroke from the ink before 
    // calling HitTest.  However, it is not good practice to modify 
    // the stroke inside of its own event handler.
    hitStrokes = myInkCollector.Ink.HitTest(inkLassoPoints, LassoPercent);
    hitStrokes.Remove(e.Stroke);
}

// Reset the lasso points
lassoPoints.Clear();
lastDrawnLassoDot = Point.Empty;

// Use helper method to set the selection
SetSelection(hitStrokes);
```



## <a name="copying-ink-to-the-clipboard"></a>將筆墨複製到剪貼簿

CopyInkToClipboard helper 方法會建立 [InkClipboardFormats](/previous-versions/ms583681(v=vs.100)) 值、檢查格式功能表的狀態，以更新要放在剪貼簿上的格式，並使用 [筆墨](/previous-versions/ms583670(v=vs.100)) 物件的 [ClipboardCopy](/previous-versions/dotnet/netframework-3.5/ms571316(v=vs.90)) 方法將筆觸複製到剪貼簿。


```C++
// Declare the ink clipboard formats to put on the clipboard
InkClipboardFormats formats = new InkClipboardFormats();

// Use selected format menu items to set the clipboard 
// formats
...

// If at least one format was selected, invoke the Ink
// API's ClipboardCopy method.  Note that selectedStrokes
// could be null, but that this is ok - if selectedStrokes
// is null, all of the ink is copied.
if (formats != InkClipboardFormats.None)
{
    myInkCollector.Ink.ClipboardCopy(selectedStrokes,formats,clipboardModes);
}
else
{
    MessageBox.Show("No clipboard formats selected");
}
```



## <a name="updating-a-selection"></a>更新選取專案

SetSelection helper 方法會更新 selectedStrokes 欄位，如果集合是 **Null** 或 **空白**，則選取矩形會設定為空的矩形。 如果選取的 [筆觸](/previous-versions/ms552701(v=vs.100)) 集合不是空的，SetSelection 方法會執行下列步驟：

-   使用筆劃集合的 [GetBoundingBox](/previous-versions/dotnet/netframework-3.5/ms571376(v=vs.90)) 方法來決定周框
-   將矩形座標從筆墨空間轉換成圖元
-   擴大矩形，以提供其與所選筆劃之間的一些視覺空間
-   建立目前選取方塊的選取控點

最後，SetSelection 方法會設定選取控點的可見度，並將筆墨收集器的 [AutoRedraw](/previous-versions/ms571706(v=vs.100)) 屬性設定為 **FALSE**（如果已選取筆劃）。


```C++
// Tracks whether the rectangle that bounds the selected
// strokes should be displayed
bool isSelectionVisible = false;

// Update the selected strokes collection
selectedStrokes = strokes;

// If no strokes are selected, set the selection rectangle
// to empty
if (!HasSelection())
{
    selectionRect = Rectangle.Empty;
}
    // Otherwise, at least one stroke is selected and it is necessary
    // to display the selection rectangle.
else
{
    isSelectionVisible = true;

    // Retrieve the bounding box of the strokes
    selectionRect = selectedStrokes.GetBoundingBox();
    using (Graphics g = CreateGraphics())
    {
        InkSpaceToPixel(g, ref selectionRect);
    }

    // Pad the selection rectangle so that the selected ink 
    // doesn't overlap with the selection rectangle's handles.
    selectionRect.Inflate(SelectionRectBuffer, SelectionRectBuffer);

    // compute the center of the rectangle that bounds the 
    // selected strokes
    int xAvg = (selectionRect.Right+selectionRect.Left)/2;
    int yAvg = (selectionRect.Top+selectionRect.Bottom)/2;

    // Draw the resize handles
    // top left
    SetLocation(selectionHandles[0],selectionRect.Left, selectionRect.Top);
    // top
    SetLocation(selectionHandles[1],xAvg, selectionRect.Top);
    // top right 
    SetLocation(selectionHandles[2],selectionRect.Right, selectionRect.Top);

    // left 
    SetLocation(selectionHandles[3],selectionRect.Left, yAvg);
    // right
    SetLocation(selectionHandles[4],selectionRect.Right, yAvg);

    // bottom left
    SetLocation(selectionHandles[5],selectionRect.Left, selectionRect.Bottom);
    // bottom
    SetLocation(selectionHandles[6],xAvg, selectionRect.Bottom);
    // bottom right
    SetLocation(selectionHandles[7],selectionRect.Right, selectionRect.Bottom);
}

// Set the visibility of each selection handle in the 
// selection rectangle.  If there is no selection, all 
// handles should be hidden.  Otherwise, all handles should
// be visible.
foreach(PictureBox pb in selectionHandles)
{
    pb.Visible = isSelectionVisible;
}

// Turn off autoredrawing if there is a selection - otherwise,
// the selected ink is not displayed as selected.
myInkCollector.AutoRedraw = !isSelectionVisible;

// Since the selection has changed, repaint the screen.
Refresh();
```



## <a name="drawing-the-lasso"></a>繪製套索

套索會繪製成一系列的開放式點，這些點會沿著套索筆劃的路徑，以及兩端之間的虛線接點線。 [NewPackets](/previous-versions/ms567621(v=vs.100))事件是在繪製套索時引發，而且事件處理常式會將筆劃資訊傳遞給 DrawLasso 方法。

DrawLasso helper 方法會先移除舊的連接線，然後逐一查看筆劃中的點。 然後，DrawLasso 會計算將點沿著筆劃放置的位置，然後繪製它們。 最後，它會繪製新的連接線。

## <a name="closing-the-form"></a>關閉表單

表單的 [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) 方法會處置 [InkCollector](/previous-versions/ms583683(v=vs.100)) 物件 myInkCollector。

 

 
