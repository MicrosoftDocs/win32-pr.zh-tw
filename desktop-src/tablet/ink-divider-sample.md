---
description: 這個範例是以筆墨集合範例為基礎。 它會顯示如何使用分隔物件來分析筆墨輸入。
ms.assetid: 3350b643-11b3-4474-8dd0-bc3eb1b7121e
title: 筆墨分割範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c74592606ba98ec913dd419deda1b2b766066e17545e95f18a14980f36dafde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452095"
---
# <a name="ink-divider-sample"></a>筆墨分割範例

這個範例是以 [筆墨集合範例](ink-collection-sample.md)為基礎。 它會顯示如何使用 [分隔](/previous-versions/ms839398(v=msdn.10)) 物件來分析筆墨輸入。

如需 [分隔線](/previous-versions/ms839398(v=msdn.10))的詳細概念資訊，請參閱 [分割物件](the-divider-object.md)。

當表單更新時，此範例會在每個分析單位周圍繪製周框，並分成單字、線條、段落和繪圖。 除了使用不同的色彩之外，這些矩形會依不同的數量放大，以確保其他矩形不會遮蔽。 下表指定每個已分析單位的色彩和放大。



| 已分析的單位        | Color              | 圖元放大 |
|----------------------|--------------------|-------------------|
| Word<br/>      | 綠色<br/>   | 1<br/>      |
| 折線圖<br/>      | 桃紅色<br/> | 3<br/>      |
| Paragraph<br/> | 藍色<br/>    | 5<br/>      |
| 繪圖<br/>   | 紅色<br/>     | 1<br/>      |



 

## <a name="setting-up-the-form"></a>設定表單

當表單載入時，會建立 [分隔](/previous-versions/ms839398(v=msdn.10)) 物件。 系統會建立 [InkOverlay](/previous-versions/ms833057(v=msdn.10)) 物件，並與表單上的面板建立關聯。 接著，事件處理常式會附加至 InkOverlay 物件，以追蹤何時新增和刪除筆劃。 接著，如果辨識器可用，預設辨識器的 [RecognizerCoNtext](/previous-versions/ms828542(v=msdn.10)) 物件就會指派給分隔線。 接著會設定分隔物件的 [LineHeight](/previous-versions/ms839409(v=msdn.10)) 屬性，並將來自 InkOverlay 物件的 [筆劃](/previous-versions/ms827799(v=msdn.10)) 集合指派給分隔線。 最後，會啟用 InkOverlay 物件。


```C++
// Create the ink overlay and associate it with the form
myInkOverlay = new Microsoft.Ink.InkOverlay(DrawArea.Handle);

// Set the erasing mode to stroke erase.
myInkOverlay.EraserMode = InkOverlayEraserMode.StrokeErase;

// Hook event handler for the Stroke event to myInkOverlay_Stroke.
// This is necessary since the application needs to pass the strokes 
// to the ink divider.
myInkOverlay.Stroke += new InkCollectorStrokeEventHandler(myInkOverlay_Stroke); 

// Hook the event handler for StrokeDeleting event to myInkOverlay_StrokeDeleting.
// This is necessary as the application needs to remove the strokes from 
// ink divider object as well.
myInkOverlay.StrokesDeleting += new InkOverlayStrokesDeletingEventHandler(myInkOverlay_StrokeDeleting);

// Hook the event handler for StrokeDeleted event to myInkOverlay_StrokeDeleted.
// This is necessary to update the layout analysis result when automatic layout analysis
// option is selected.
myInkOverlay.StrokesDeleted += new InkOverlayStrokesDeletedEventHandler(myInkOverlay_StrokeDeleted);

// Create the ink divider object
myInkDivider = new Divider();

// Add a default recognizer context to the divider object
// without adding the recognizer context, the divider would
// not use a recognizer to do its word segmentation and would
// have less accurate results.
// Adding the recognizer context slows down the call to 
// myInkDivider.Divide though.
// It is possible that there is no recognizer installed on the
// machine for this language. In that case the divider does
// not use a recognizer to improve its accuracy.
// Get the default recognizer if any
try
{
    Recognizers recognizers = new Recognizers();
     myInkDivider.RecognizerContext = recognizers.GetDefaultRecognizer().CreateRecognizerContext();
}
catch (InvalidOperationException)
{
     //We are in the case where no default recognizers can be found
}

    // The LineHeight property helps the InkDivider distinguish between 
    // drawing and handwriting. The value should be the expected height 
    // of the user's handwriting in ink space units (0.01mm).
    // Here we set the LineHeight to 840, which is about 1/3 of an inch.
    myInkDivider.LineHeight = 840;

// Assign ink overlay's strokes collection to the ink divider
// This strokes collection is updated in the event handler
myInkDivider.Strokes = myInkOverlay.Ink.Strokes;

// Enable ink collection
myInkOverlay.Enabled = true;
```



[分割](/previous-versions/ms839398(v=msdn.10))物件的[筆劃](/previous-versions/ms839422(v=msdn.10))集合必須與[inkoverlay](/previous-versions/ms833057(v=msdn.10))物件的[筆劃](/previous-versions/ms827799(v=msdn.10))集合保持同步， (透過 inkoverlay 物件的[筆墨](/previous-versions/ms833110(v=msdn.10))屬性) 來存取。 為了確保發生此情況，會以下列方式撰寫 InkOverlay 物件的 [筆觸](/previous-versions/ms835344(v=msdn.10)) 事件處理常式。 請注意，事件處理常式會先測試是否將 [system.windows.controls.inkcanvas.editingmode](/previous-versions/ms833105(v=msdn.10)) 設定為 **筆墨** ，以篩選出橡皮擦筆劃。 如果使用者已要求自動版面配置分析，則應用程式會呼叫表單的 DivideInk 方法，並重新整理繪圖區域。


```C++
private void myInkOverlay_Stroke(object sender, InkCollectorStrokeEventArgs e )
{
    // Filter out the eraser stroke.
    if(InkOverlayEditingMode.Ink == myInkOverlay.EditingMode)
    {
        // Add the new stroke to the ink divider's strokes collection
        myInkDivider.Strokes.Add(e.Stroke);
        
        if(miAutomaticLayoutAnalysis.Checked)
        {
            // Call DivideInk
            DivideInk();

            // Repaint the screen to reflect the change
            DrawArea.Refresh();
        }
    }
}
```



## <a name="dividing-the-ink"></a>分割筆墨

當使用者按一下 [檔案] 功能表上的 [分割] 時，會在 [[分隔](/previous-versions/ms839398(v=msdn.10))] 物件上呼叫[除](/previous-versions/ms839461(v=msdn.10))方法。 如果有的話，則會使用預設辨識器。


```C++
DivisionResult divResult = myInkDivider.Divide();
```



變數所參考之產生的 [DivisionResult](/previous-versions/ms839371(v=msdn.10)) 物件 `divResult` 會傳遞至公用程式函數 `getUnitBBBoxes()` 。 公用程式函式會針對要求的任何除法類型，傳回矩形的陣列：區段、線條、段落或繪圖。


```C++
myWordBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Segment, 1);
myLineBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Line, 3);
myParagraphBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Paragraph, 5);
myDrawingBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Drawing, 1);
```



最後，[表單] 面板會強制重新繪製，以顯示周框矩形。


```C++
DrawArea.Refresh();
```



## <a name="ink-analysis-results"></a>筆墨分析結果

在公用程式函式中，會根據呼叫端所要求的除法類型，使用[ResultByType](/previous-versions/ms839388(v=msdn.10))方法來查詢[DivisionResult](/previous-versions/ms839371(v=msdn.10))物件的結果。 ResultByType 方法會傳回 [DivisionUnits](/previous-versions/ms837954(v=msdn.10)) 集合。 集合中的每個 [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) 都代表一個繪圖、一個手寫的單一辨識區段、一行手寫，或是一組手寫，視呼叫公用程式函式時所指定的內容而定。


```C++
DivisionUnits units = divResult.ResultByType(divType);
```



如果至少有一個 [DivisionUnit](/previous-versions/ms837976(v=msdn.10))，則會建立矩形陣列，其中每個單位都包含一個周框矩形。  (矩形會依每個單位類型的不同數量擴大，並保留在擴充變數中，以避免重迭。 ) 


```C++
// If there is at least one unit, we construct the rectangles
if((null != units) && (0 < units.Count))
{
    // We need to convert rectangles from ink units to
    // pixel units. For that, we need Graphics object
    // to pass to InkRenderer.InkSpaceToPixel method
    using (Graphics g = DrawArea.CreateGraphics())
    {

    // InkSpace to Pixel Space conversion setup done here. 
    // Not shown for brevity.

        // Iterate through the collection of division units to obtain the bounding boxes
        foreach(DivisionUnit unit in units)
        {
            // Get the bounding box of the strokes of the division unit
            divRects[i] = unit.Strokes.GetBoundingBox();

            // Div unit rect Ink space to Pixel space conversion done here. 
            // Not shown for brevity.

            // Inflate the rectangle by inflate pixels in both directions
            divRects[i].Inflate(inflate, inflate);

            // Increment the index
            ++i;
        }

    } // Relinquish the Graphics object
}
```



## <a name="redrawing-the-form"></a>重繪表單

當強制重新繪製時，下列程式碼會執行以針對筆墨周圍表單上的每個 [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) 繪製周框方塊。


```C++
private void DrawArea_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
        {
            // Create the Pen used to draw bounding boxes.
            // First set of bounding boxes drawn here are 
            // the bounding boxes of paragraphs.
            // These boxes are drawn with Blue pen.
            Pen penBox = new Pen(Color.Blue, 2);

            // First, draw the bounding boxes for Paragraphs
            if(null != myParagraphBoundingBoxes)
            {
                // Draw bounding boxes for Paragraphs
                e.Graphics.DrawRectangles(penBox, myParagraphBoundingBoxes);
            }

            // Next, draw the bounding boxes for Lines
            if(null != myLineBoundingBoxes)
            {
                // Color is Magenta pen
                penBox.Color = Color.Magenta;
                // Draw the bounding boxes for Lines
                e.Graphics.DrawRectangles(penBox, myLineBoundingBoxes);
            }
            
            // Then, draw the bounding boxes for Words
            if(null != myWordBoundingBoxes)
            {
                // Color is Green
                penBox.Color = Color.Green;
                // Draw bounding boxes for Words
                e.Graphics.DrawRectangles(penBox, myWordBoundingBoxes);
            }
            
            // Finally, draw the boxes for Drawings
            if(null != myDrawingBoundingBoxes)
            {
                // Color is Red pen
                penBox.Color = Color.Red;
                // Draw bounding boxes for Drawings
                e.Graphics.DrawRectangles(penBox, myDrawingBoundingBoxes);
            }
        }
```



## <a name="closing-the-form"></a>關閉表單

表單的 [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) 方法會處置範例中所使用的 [InkOverlay](/previous-versions/ms833057(v=msdn.10))、 [分隔](/previous-versions/ms839398(v=msdn.10))、 [RecognizerCoNtext](/previous-versions/ms828542(v=msdn.10)) 物件和 [筆劃](/previous-versions/ms827799(v=msdn.10)) 集合。

 

