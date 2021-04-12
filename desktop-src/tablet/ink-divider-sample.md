---
description: 這個範例是以筆墨集合範例為基礎。 它會顯示如何使用分隔物件來分析筆墨輸入。
ms.assetid: 3350b643-11b3-4474-8dd0-bc3eb1b7121e
title: 筆墨分割範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a272d6a5530938e6fecfeefc9f46ffdd0835d045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468776"
---
# <a name="ink-divider-sample"></a><span data-ttu-id="d2b57-104">筆墨分割範例</span><span class="sxs-lookup"><span data-stu-id="d2b57-104">Ink Divider Sample</span></span>

<span data-ttu-id="d2b57-105">這個範例是以 [筆墨集合範例](ink-collection-sample.md)為基礎。</span><span class="sxs-lookup"><span data-stu-id="d2b57-105">This sample is based on the [Ink Collection Sample](ink-collection-sample.md).</span></span> <span data-ttu-id="d2b57-106">它會顯示如何使用 [分隔](/previous-versions/ms839398(v=msdn.10)) 物件來分析筆墨輸入。</span><span class="sxs-lookup"><span data-stu-id="d2b57-106">It shows how to use the [Divider](/previous-versions/ms839398(v=msdn.10)) object to analyze ink input.</span></span>

<span data-ttu-id="d2b57-107">如需 [分隔線](/previous-versions/ms839398(v=msdn.10))的詳細概念資訊，請參閱 [分割物件](the-divider-object.md)。</span><span class="sxs-lookup"><span data-stu-id="d2b57-107">For detailed conceptual information about [Divider](/previous-versions/ms839398(v=msdn.10)), see [The Divider Object](the-divider-object.md).</span></span>

<span data-ttu-id="d2b57-108">當表單更新時，此範例會在每個分析單位周圍繪製周框，並分成單字、線條、段落和繪圖。</span><span class="sxs-lookup"><span data-stu-id="d2b57-108">When the form is updated, the sample draws a bounding rectangle around each analyzed unit, broken into words, lines, paragraphs, and drawings.</span></span> <span data-ttu-id="d2b57-109">除了使用不同的色彩之外，這些矩形會依不同的數量放大，以確保其他矩形不會遮蔽。</span><span class="sxs-lookup"><span data-stu-id="d2b57-109">Besides using different colors, these rectangles are enlarged by different amounts to ensure that none of the rectangles is obscured by others.</span></span> <span data-ttu-id="d2b57-110">下表指定每個已分析單位的色彩和放大。</span><span class="sxs-lookup"><span data-stu-id="d2b57-110">The following table specifies the color and enlargement for each analyzed unit.</span></span>



| <span data-ttu-id="d2b57-111">已分析的單位</span><span class="sxs-lookup"><span data-stu-id="d2b57-111">analyzed Unit</span></span>        | <span data-ttu-id="d2b57-112">Color</span><span class="sxs-lookup"><span data-stu-id="d2b57-112">Color</span></span>              | <span data-ttu-id="d2b57-113">圖元放大</span><span class="sxs-lookup"><span data-stu-id="d2b57-113">Pixel Enlargement</span></span> |
|----------------------|--------------------|-------------------|
| <span data-ttu-id="d2b57-114">Word</span><span class="sxs-lookup"><span data-stu-id="d2b57-114">Word</span></span><br/>      | <span data-ttu-id="d2b57-115">綠色</span><span class="sxs-lookup"><span data-stu-id="d2b57-115">Green</span></span><br/>   | <span data-ttu-id="d2b57-116">1</span><span class="sxs-lookup"><span data-stu-id="d2b57-116">1</span></span><br/>      |
| <span data-ttu-id="d2b57-117">線條</span><span class="sxs-lookup"><span data-stu-id="d2b57-117">Line</span></span><br/>      | <span data-ttu-id="d2b57-118">桃紅色</span><span class="sxs-lookup"><span data-stu-id="d2b57-118">Magenta</span></span><br/> | <span data-ttu-id="d2b57-119">3</span><span class="sxs-lookup"><span data-stu-id="d2b57-119">3</span></span><br/>      |
| <span data-ttu-id="d2b57-120">Paragraph</span><span class="sxs-lookup"><span data-stu-id="d2b57-120">Paragraph</span></span><br/> | <span data-ttu-id="d2b57-121">藍色</span><span class="sxs-lookup"><span data-stu-id="d2b57-121">Blue</span></span><br/>    | <span data-ttu-id="d2b57-122">5</span><span class="sxs-lookup"><span data-stu-id="d2b57-122">5</span></span><br/>      |
| <span data-ttu-id="d2b57-123">繪圖</span><span class="sxs-lookup"><span data-stu-id="d2b57-123">Drawing</span></span><br/>   | <span data-ttu-id="d2b57-124">紅色</span><span class="sxs-lookup"><span data-stu-id="d2b57-124">Red</span></span><br/>     | <span data-ttu-id="d2b57-125">1</span><span class="sxs-lookup"><span data-stu-id="d2b57-125">1</span></span><br/>      |



 

## <a name="setting-up-the-form"></a><span data-ttu-id="d2b57-126">設定表單</span><span class="sxs-lookup"><span data-stu-id="d2b57-126">Setting Up the Form</span></span>

<span data-ttu-id="d2b57-127">當表單載入時，會建立 [分隔](/previous-versions/ms839398(v=msdn.10)) 物件。</span><span class="sxs-lookup"><span data-stu-id="d2b57-127">When the form loads, a [Divider](/previous-versions/ms839398(v=msdn.10)) object is created.</span></span> <span data-ttu-id="d2b57-128">系統會建立 [InkOverlay](/previous-versions/ms833057(v=msdn.10)) 物件，並與表單上的面板建立關聯。</span><span class="sxs-lookup"><span data-stu-id="d2b57-128">An [InkOverlay](/previous-versions/ms833057(v=msdn.10)) object is created and associated with a panel on the form.</span></span> <span data-ttu-id="d2b57-129">接著，事件處理常式會附加至 InkOverlay 物件，以追蹤何時新增和刪除筆劃。</span><span class="sxs-lookup"><span data-stu-id="d2b57-129">Then event handlers are attached to the InkOverlay object to track when strokes are added and deleted.</span></span> <span data-ttu-id="d2b57-130">接著，如果辨識器可用，預設辨識器的 [RecognizerCoNtext](/previous-versions/ms828542(v=msdn.10)) 物件就會指派給分隔線。</span><span class="sxs-lookup"><span data-stu-id="d2b57-130">Then if recognizers are available, a [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) object for the default recognizer is assigned to the Divider.</span></span> <span data-ttu-id="d2b57-131">接著會設定分隔物件的 [LineHeight](/previous-versions/ms839409(v=msdn.10)) 屬性，並將來自 InkOverlay 物件的 [筆劃](/previous-versions/ms827799(v=msdn.10)) 集合指派給分隔線。</span><span class="sxs-lookup"><span data-stu-id="d2b57-131">Then the Divider object's [LineHeight](/previous-versions/ms839409(v=msdn.10)) property is set and the [Strokes](/previous-versions/ms827799(v=msdn.10)) collection from the InkOverlay object is assigned to the Divider.</span></span> <span data-ttu-id="d2b57-132">最後，會啟用 InkOverlay 物件。</span><span class="sxs-lookup"><span data-stu-id="d2b57-132">Finally, the InkOverlay object is enabled.</span></span>


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



<span data-ttu-id="d2b57-133">[分割](/previous-versions/ms839398(v=msdn.10))物件的[筆劃](/previous-versions/ms839422(v=msdn.10))集合必須與[inkoverlay](/previous-versions/ms833057(v=msdn.10))物件的[筆劃](/previous-versions/ms827799(v=msdn.10))集合保持同步， (透過 inkoverlay 物件的[筆墨](/previous-versions/ms833110(v=msdn.10))屬性) 來存取。</span><span class="sxs-lookup"><span data-stu-id="d2b57-133">The [Divider](/previous-versions/ms839398(v=msdn.10)) object's [Strokes](/previous-versions/ms839422(v=msdn.10)) collection must be kept in sync with the [InkOverlay](/previous-versions/ms833057(v=msdn.10)) object's [Strokes](/previous-versions/ms827799(v=msdn.10)) collection (accessed through the InkOverlay object's [Ink](/previous-versions/ms833110(v=msdn.10)) property).</span></span> <span data-ttu-id="d2b57-134">為了確保發生此情況，會以下列方式撰寫 InkOverlay 物件的 [筆觸](/previous-versions/ms835344(v=msdn.10)) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="d2b57-134">To ensure that this happens, the [Stroke](/previous-versions/ms835344(v=msdn.10)) event handler for the InkOverlay object is written as follows.</span></span> <span data-ttu-id="d2b57-135">請注意，事件處理常式會先測試是否將 [system.windows.controls.inkcanvas.editingmode](/previous-versions/ms833105(v=msdn.10)) 設定為 **筆墨** ，以篩選出橡皮擦筆劃。</span><span class="sxs-lookup"><span data-stu-id="d2b57-135">Note that the event handler first tests to see if the [EditingMode](/previous-versions/ms833105(v=msdn.10)) is set to **Ink** to filter out eraser strokes.</span></span> <span data-ttu-id="d2b57-136">如果使用者已要求自動版面配置分析，則應用程式會呼叫表單的 DivideInk 方法，並重新整理繪圖區域。</span><span class="sxs-lookup"><span data-stu-id="d2b57-136">If the user has requested automatic layout analysis, then the application calls the form's DivideInk method and refreshes the drawing area.</span></span>


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



## <a name="dividing-the-ink"></a><span data-ttu-id="d2b57-137">分割筆墨</span><span class="sxs-lookup"><span data-stu-id="d2b57-137">Dividing the Ink</span></span>

<span data-ttu-id="d2b57-138">當使用者按一下 [檔案] 功能表上的 [分割] 時，會在 [[分隔](/previous-versions/ms839398(v=msdn.10))] 物件上呼叫[除](/previous-versions/ms839461(v=msdn.10))方法。</span><span class="sxs-lookup"><span data-stu-id="d2b57-138">When the user clicks Divide on the File menu, the [Divide](/previous-versions/ms839461(v=msdn.10)) method is called on the [Divider](/previous-versions/ms839398(v=msdn.10)) object.</span></span> <span data-ttu-id="d2b57-139">如果有的話，則會使用預設辨識器。</span><span class="sxs-lookup"><span data-stu-id="d2b57-139">The default recognizer is used, if available.</span></span>


```C++
DivisionResult divResult = myInkDivider.Divide();
```



<span data-ttu-id="d2b57-140">變數所參考之產生的 [DivisionResult](/previous-versions/ms839371(v=msdn.10)) 物件 `divResult` 會傳遞至公用程式函數 `getUnitBBBoxes()` 。</span><span class="sxs-lookup"><span data-stu-id="d2b57-140">The resulting [DivisionResult](/previous-versions/ms839371(v=msdn.10)) object, referenced by the variable `divResult`, is passed to a utility function, `getUnitBBBoxes()`.</span></span> <span data-ttu-id="d2b57-141">公用程式函式會針對要求的任何除法類型，傳回矩形的陣列：區段、線條、段落或繪圖。</span><span class="sxs-lookup"><span data-stu-id="d2b57-141">The utility function returns an array of rectangles for whatever division type is requested: segments, lines, paragraphs, or drawings.</span></span>


```C++
myWordBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Segment, 1);
myLineBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Line, 3);
myParagraphBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Paragraph, 5);
myDrawingBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Drawing, 1);
```



<span data-ttu-id="d2b57-142">最後，[表單] 面板會強制重新繪製，以顯示周框矩形。</span><span class="sxs-lookup"><span data-stu-id="d2b57-142">Finally, the form panel is forced to redraw so that the bounding rectangles appear.</span></span>


```C++
DrawArea.Refresh();
```



## <a name="ink-analysis-results"></a><span data-ttu-id="d2b57-143">筆墨分析結果</span><span class="sxs-lookup"><span data-stu-id="d2b57-143">Ink Analysis Results</span></span>

<span data-ttu-id="d2b57-144">在公用程式函式中，會根據呼叫端所要求的除法類型，使用[ResultByType](/previous-versions/ms839388(v=msdn.10))方法來查詢[DivisionResult](/previous-versions/ms839371(v=msdn.10))物件的結果。</span><span class="sxs-lookup"><span data-stu-id="d2b57-144">In the utility function, the [DivisionResult](/previous-versions/ms839371(v=msdn.10)) object is queried for its results by using the [ResultByType](/previous-versions/ms839388(v=msdn.10)) method, based on the division type requested by the caller.</span></span> <span data-ttu-id="d2b57-145">ResultByType 方法會傳回 [DivisionUnits](/previous-versions/ms837954(v=msdn.10)) 集合。</span><span class="sxs-lookup"><span data-stu-id="d2b57-145">The ResultByType method returns a [DivisionUnits](/previous-versions/ms837954(v=msdn.10)) collection.</span></span> <span data-ttu-id="d2b57-146">集合中的每個 [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) 都代表一個繪圖、一個手寫的單一辨識區段、一行手寫，或是一組手寫，視呼叫公用程式函式時所指定的內容而定。</span><span class="sxs-lookup"><span data-stu-id="d2b57-146">Each [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) in the collection represents a drawing, a single recognition segment of handwriting, a line of handwriting, or a block of handwriting, depending upon what was specified when the utility function was called.</span></span>


```C++
DivisionUnits units = divResult.ResultByType(divType);
```



<span data-ttu-id="d2b57-147">如果至少有一個 [DivisionUnit](/previous-versions/ms837976(v=msdn.10))，則會建立矩形陣列，其中每個單位都包含一個周框矩形。</span><span class="sxs-lookup"><span data-stu-id="d2b57-147">If there is at least one [DivisionUnit](/previous-versions/ms837976(v=msdn.10)), an array of rectangles is created containing one bounding rectangle per unit.</span></span> <span data-ttu-id="d2b57-148"> (矩形會依每個單位類型的不同數量擴大，並保留在擴充變數中，以避免重迭。 ) </span><span class="sxs-lookup"><span data-stu-id="d2b57-148">(The rectangles are inflated by differing amounts for each type of unit, held in the inflate variable, to prevent overlapping.)</span></span>


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



## <a name="redrawing-the-form"></a><span data-ttu-id="d2b57-149">重繪表單</span><span class="sxs-lookup"><span data-stu-id="d2b57-149">Redrawing the Form</span></span>

<span data-ttu-id="d2b57-150">當強制重新繪製時，下列程式碼會執行以針對筆墨周圍表單上的每個 [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) 繪製周框方塊。</span><span class="sxs-lookup"><span data-stu-id="d2b57-150">When the redraw is forced above, the following code executes to paint the bounding boxes for each [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) on the form around the ink.</span></span>


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



## <a name="closing-the-form"></a><span data-ttu-id="d2b57-151">關閉表單</span><span class="sxs-lookup"><span data-stu-id="d2b57-151">Closing the Form</span></span>

<span data-ttu-id="d2b57-152">表單的 [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) 方法會處置範例中所使用的 [InkOverlay](/previous-versions/ms833057(v=msdn.10))、 [分隔](/previous-versions/ms839398(v=msdn.10))、 [RecognizerCoNtext](/previous-versions/ms828542(v=msdn.10)) 物件和 [筆劃](/previous-versions/ms827799(v=msdn.10)) 集合。</span><span class="sxs-lookup"><span data-stu-id="d2b57-152">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkOverlay](/previous-versions/ms833057(v=msdn.10)), [Divider](/previous-versions/ms839398(v=msdn.10)), [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) objects and the [Strokes](/previous-versions/ms827799(v=msdn.10)) collection used in the sample.</span></span>

 

