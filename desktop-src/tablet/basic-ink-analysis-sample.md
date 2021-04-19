---
description: 基本筆墨分析範例顯示 InkAnalyzer 類別如何將筆墨分割成不同的單字和繪圖區段。此範例是筆墨分割範例的更新版本。
ms.assetid: cb9a28d9-f8c6-478e-ae43-2d30106edc7b
title: 基本筆墨分析範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94ac73ca9049169c6e406059665a66e8eaa6f3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966662"
---
# <a name="basic-ink-analysis-sample"></a><span data-ttu-id="ebd28-103">基本筆墨分析範例</span><span class="sxs-lookup"><span data-stu-id="ebd28-103">Basic Ink Analysis Sample</span></span>

<span data-ttu-id="ebd28-104">基本筆墨分析範例顯示 [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) 類別如何將筆墨分割成不同的單字和繪圖區段。</span><span class="sxs-lookup"><span data-stu-id="ebd28-104">The Basic Ink Analysis sample shows how the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) class divides ink into various word and drawing segments.</span></span>

<span data-ttu-id="ebd28-105">此範例是 [筆墨分割範例](ink-divider-sample.md)的更新版本。</span><span class="sxs-lookup"><span data-stu-id="ebd28-105">This sample is an updated version of the [Ink Divider Sample](ink-divider-sample.md).</span></span> <span data-ttu-id="ebd28-106">雖然筆墨分割範例會使用 [分界線](/previous-versions/ms839398(v=msdn.10)) 類別，但此範例會使用較新和慣用的 InkAnalysis API。</span><span class="sxs-lookup"><span data-stu-id="ebd28-106">Whereas the Ink Divider Sample uses the [Divider](/previous-versions/ms839398(v=msdn.10)) class, this sample uses the newer and preferred InkAnalysis API.</span></span> <span data-ttu-id="ebd28-107">InkAnalysis API 將 [RecognizerCoNtext](/previous-versions/ms828542(v=msdn.10)) 和分隔組合成一個 API，並擴充兩者的功能。</span><span class="sxs-lookup"><span data-stu-id="ebd28-107">The InkAnalysis API combines the [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) and Divider into one API and expands on the functionality of both.</span></span>

<span data-ttu-id="ebd28-108">當您更新表單時，此範例會在每個分析單元周圍繪製一個矩形：單字、線條、段落、書寫區域、繪圖和專案符號。</span><span class="sxs-lookup"><span data-stu-id="ebd28-108">When you update the form, the sample draws a rectangle around each analyzed unit: words, lines, paragraphs, writing regions, drawings and bullets.</span></span> <span data-ttu-id="ebd28-109">表單針對不同的單位使用不同的色彩。</span><span class="sxs-lookup"><span data-stu-id="ebd28-109">The form uses different colors for the different units.</span></span> <span data-ttu-id="ebd28-110">矩形也會放大不同的數量，以確保任何其他矩形不會遮蔽。</span><span class="sxs-lookup"><span data-stu-id="ebd28-110">The rectangles are also enlarged by different amounts to ensure that no one rectangle is obscured by any others.</span></span>

<span data-ttu-id="ebd28-111">下表指定每個已分析單位的色彩和放大。</span><span class="sxs-lookup"><span data-stu-id="ebd28-111">The following table specifies the color and enlargement for each analyzed unit.</span></span>



| <span data-ttu-id="ebd28-112">已分析的單位</span><span class="sxs-lookup"><span data-stu-id="ebd28-112">Analyzed unit</span></span>             | <span data-ttu-id="ebd28-113">矩形的色彩</span><span class="sxs-lookup"><span data-stu-id="ebd28-113">Color of rectangle</span></span> | <span data-ttu-id="ebd28-114">矩形放大 (圖元) </span><span class="sxs-lookup"><span data-stu-id="ebd28-114">Rectangle enlargement (pixels)</span></span> |
|---------------------------|--------------------|--------------------------------|
| <span data-ttu-id="ebd28-115">Word</span><span class="sxs-lookup"><span data-stu-id="ebd28-115">Word</span></span><br/>           | <span data-ttu-id="ebd28-116">綠色</span><span class="sxs-lookup"><span data-stu-id="ebd28-116">Green</span></span><br/>   | <span data-ttu-id="ebd28-117">1</span><span class="sxs-lookup"><span data-stu-id="ebd28-117">1</span></span><br/>                   |
| <span data-ttu-id="ebd28-118">線條</span><span class="sxs-lookup"><span data-stu-id="ebd28-118">Line</span></span><br/>           | <span data-ttu-id="ebd28-119">桃紅色</span><span class="sxs-lookup"><span data-stu-id="ebd28-119">Magenta</span></span><br/> | <span data-ttu-id="ebd28-120">3</span><span class="sxs-lookup"><span data-stu-id="ebd28-120">3</span></span><br/>                   |
| <span data-ttu-id="ebd28-121">Paragraph</span><span class="sxs-lookup"><span data-stu-id="ebd28-121">Paragraph</span></span><br/>      | <span data-ttu-id="ebd28-122">藍色</span><span class="sxs-lookup"><span data-stu-id="ebd28-122">Blue</span></span><br/>    | <span data-ttu-id="ebd28-123">5</span><span class="sxs-lookup"><span data-stu-id="ebd28-123">5</span></span><br/>                   |
| <span data-ttu-id="ebd28-124">寫入區域</span><span class="sxs-lookup"><span data-stu-id="ebd28-124">Writing region</span></span><br/> | <span data-ttu-id="ebd28-125">黃色</span><span class="sxs-lookup"><span data-stu-id="ebd28-125">Yellow</span></span><br/>  | <span data-ttu-id="ebd28-126">7</span><span class="sxs-lookup"><span data-stu-id="ebd28-126">7</span></span><br/>                   |
| <span data-ttu-id="ebd28-127">繪圖</span><span class="sxs-lookup"><span data-stu-id="ebd28-127">Drawing</span></span><br/>        | <span data-ttu-id="ebd28-128">紅色</span><span class="sxs-lookup"><span data-stu-id="ebd28-128">Red</span></span><br/>     | <span data-ttu-id="ebd28-129">1</span><span class="sxs-lookup"><span data-stu-id="ebd28-129">1</span></span><br/>                   |
| <span data-ttu-id="ebd28-130">子彈</span><span class="sxs-lookup"><span data-stu-id="ebd28-130">Bullet</span></span><br/>         | <span data-ttu-id="ebd28-131">橙色</span><span class="sxs-lookup"><span data-stu-id="ebd28-131">Orange</span></span><br/>  | <span data-ttu-id="ebd28-132">1</span><span class="sxs-lookup"><span data-stu-id="ebd28-132">1</span></span><br/>                   |



 

<span data-ttu-id="ebd28-133">您可以在表單中清除筆觸。</span><span class="sxs-lookup"><span data-stu-id="ebd28-133">You can erase strokes in the form.</span></span> <span data-ttu-id="ebd28-134">在範例應用程式中，您可以在筆跡和清除模式之間切換，以變更畫筆的功能。</span><span class="sxs-lookup"><span data-stu-id="ebd28-134">In the sample application, you can toggle between Ink and Erase mode to change the function of the pen.</span></span>


```C++
        private void miInk_Click(object sender, System.EventArgs e)
        {
            // Turn on the inking mode
            myInkOverlay.EditingMode = InkOverlayEditingMode.Ink;

            // Update the state of the Ink and Erase menu items
            miInk.Checked = true;
            miErase.Checked = false;

            // Update the UI
            this.Refresh();
        }

        private void miErase_Click(object sender, System.EventArgs e)
        {
            // Turn on the ink deletion mode
            myInkOverlay.EditingMode = InkOverlayEditingMode.Delete;

            // Update the state of the Ink and Erase menu items
            miInk.Checked = false;
            miErase.Checked = true;

            // Update the UI
            this.Refresh();
        }
```



<span data-ttu-id="ebd28-135">當您新增或刪除筆劃時，範例會更新 [InkAnalyzer](/previous-versions/ms583671(v=vs.100))。</span><span class="sxs-lookup"><span data-stu-id="ebd28-135">When you add or delete strokes, the samples updates the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)).</span></span>


```C++
        private void myInkOverlay_Stroke(object sender, InkCollectorStrokeEventArgs e)
        {
            // Filter out the eraser stroke.
            if (InkOverlayEditingMode.Ink == myInkOverlay.EditingMode)
            {

                // Add the new stroke to the InkAnalyzer's stroke collection
                myInkAnalyzer.AddStroke(e.Stroke);

                if (miAutomaticLayoutAnalysis.Checked)
                {
                    // Invoke an analysis operation on the background thread
                    myInkAnalyzer.BackgroundAnalyze();
                }
            }
        }

        void myInkOverlay_StrokeDeleting(object sender, InkOverlayStrokesDeletingEventArgs e)
        {
            // Remove the strokes to be deleted from the InkAnalyzer's stroke collection
            myInkAnalyzer.RemoveStrokes(e.StrokesToDelete);

            // If automatic layout analysis is turned on, analyze the ink on the background thread
            if ( miAutomaticLayoutAnalysis.Checked )
            {
                // Invoke an analysis operation on the background thread
                myInkAnalyzer.BackgroundAnalyze ( );
            }
        }
```



<span data-ttu-id="ebd28-136">請注意，在 [模式] 功能表中，[自動版面配置分析] 預設為 [開啟]。</span><span class="sxs-lookup"><span data-stu-id="ebd28-136">Notice that in the Mode menu, Automatic Layout Analysis is on by default.</span></span> <span data-ttu-id="ebd28-137">選取此選項時，會在每次建立或刪除筆劃時， [InkOverlay](/previous-versions/ms833057(v=msdn.10)) 物件的 [stroke](/previous-versions/ms835344(v=msdn.10)) 和 [StrokesDeleting](/previous-versions/ms835360(v=msdn.10)) 事件處理常式會呼叫 [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) 方法。</span><span class="sxs-lookup"><span data-stu-id="ebd28-137">With this option selected, the [InkOverlay](/previous-versions/ms833057(v=msdn.10)) object's [Stroke](/previous-versions/ms835344(v=msdn.10)) and [StrokesDeleting](/previous-versions/ms835360(v=msdn.10)) event handlers call the [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) method every time a stroke is created or deleted.</span></span>

> [!Note]  
> <span data-ttu-id="ebd28-138">使用多個筆劃來呼叫 [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) 物件的 [分析](/previous-versions/ms568971(v=vs.100)) 方法，會在應用程式中產生明顯的延遲。</span><span class="sxs-lookup"><span data-stu-id="ebd28-138">Calling the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) object's [Analyze](/previous-versions/ms568971(v=vs.100)) method with more than a few strokes present creates a noticeable delay in an application.</span></span> <span data-ttu-id="ebd28-139">這是因為分析是同步的筆墨分析作業。</span><span class="sxs-lookup"><span data-stu-id="ebd28-139">This is because Analyze is a synchronous ink analysis operation.</span></span> <span data-ttu-id="ebd28-140">在實務上，只有在您需要結果時，才呼叫分析方法。</span><span class="sxs-lookup"><span data-stu-id="ebd28-140">In practice, call the Analyze method only when you need the result.</span></span> <span data-ttu-id="ebd28-141">否則，請使用非同步 [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) 方法，如範例中所示。</span><span class="sxs-lookup"><span data-stu-id="ebd28-141">Otherwise use the asynchronous [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) method, as shown in the sample.</span></span>

 

## <a name="handling-the-analysis-results"></a><span data-ttu-id="ebd28-142">處理分析結果</span><span class="sxs-lookup"><span data-stu-id="ebd28-142">Handling the Analysis Results</span></span>

<span data-ttu-id="ebd28-143">此範例會建立兩個數組，以保存各種不同的矩形，不論是水準或旋轉。</span><span class="sxs-lookup"><span data-stu-id="ebd28-143">The sample creates two arrays to hold the various rectangles, either horizontal or rotated.</span></span> <span data-ttu-id="ebd28-144">使用旋轉周框方塊來取得要在其中寫入文字行的角度。</span><span class="sxs-lookup"><span data-stu-id="ebd28-144">Use a rotated bounding box to get the angle on which a line of words is written.</span></span> <span data-ttu-id="ebd28-145">此範例會顯示 [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) 所傳回的屬性，並根據功能表選取專案)  (顯示周框方塊或旋轉周框方塊。</span><span class="sxs-lookup"><span data-stu-id="ebd28-145">The sample shows the properties returned by the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) and displays the bounding box or the rotated bounding box (depending on the menu selection).</span></span>


```C++
      private Rectangle[] GetHorizontalBBoxes(Guid nodeType, int inflate)
        {
            // Declare the array of rectangles to hold the result
            Rectangle[] analysisRects;

            // Get the division units from the division result of division type
            ContextNodeCollection nodes = myInkAnalyzer.FindNodesOfType(nodeType);

            // If there is at least one unit, we construct the rectangles
            if ((null != nodes) && (0 < nodes.Count))
            {
                // We need to convert rectangles from ink units to
                // pixel units. For that, we need Graphics object
                // to pass to InkRenderer.InkSpaceToPixel method
                using (Graphics g = drawArea.CreateGraphics())
                {
                    // Construct the rectangles
                    analysisRects = new Rectangle[nodes.Count];

                    // InkRenderer.InkSpaceToPixel takes Point as parameter. 
                    // Create two Point objects to point to (Top, Left) and
                    // (Width, Height) properties of rectangle. (Width, Height)
                    // is used instead of (Right, Bottom) because (Right, Bottom)
                    // are read-only properties on Rectangle
                    Point ptLocation = new Point();
                    Point ptSize = new Point();

                    // Index into the bounding boxes
                    int i = 0;

                    // Iterate through the collection of division units to obtain the bounding boxes
                    foreach (ContextNode node in nodes)
                    {
                        // Get the bounding box of the strokes of the division unit
                        analysisRects[i] = node.Location.GetBounds();

                        // The bounding box is in ink space unit. Convert them into pixel unit. 
                        ptLocation = analysisRects[i].Location;
                        ptSize.X = analysisRects[i].Width;
                        ptSize.Y = analysisRects[i].Height;

                        // Convert the Location from Ink Space to Pixel Space
                        myInkOverlay.Renderer.InkSpaceToPixel(g, ref ptLocation);

                        // Convert the Size from Ink Space to Pixel Space
                        myInkOverlay.Renderer.InkSpaceToPixel(g, ref ptSize);

                        // Assign the result back to the corresponding properties
                        analysisRects[i].Location = ptLocation;
                        analysisRects[i].Width = ptSize.X;
                        analysisRects[i].Height = ptSize.Y;

                        // Inflate the rectangle by inflate pixels in both directions
                        analysisRects[i].Inflate(inflate, inflate);

                        // Increment the index
                        ++i;
                    }

                } // Relinquish the Graphics object
            }
            else
            {
                // Otherwise we return null
                analysisRects = null;
            }

            // Return the Rectangle[] object
            return analysisRects;
        }

        private System.Collections.ArrayList GetRotatedBBoxes(Guid nodeType, int inflate)
        {
            //Find the correct collection of results nodes.
            ContextNodeCollection Nodes = myInkAnalyzer.FindNodesOfType(nodeType);

            // Declare the array list to hold the results; 
            // This array represents the four points of a rectangle, with the first point
            // copied again to complete the cycle of points.

            ArrayList polygonPoints = new ArrayList(Nodes.Count);

            // Cycle through each results node, get and convert the
            // rotated bounding box points
            foreach (ContextNode node in Nodes)
            {
                //Declare the point array
                Point[] rotatedBoundingBox = null;

                //Switch on the type of ContextNode to cast into the
                //appropriate type.  This is required to access the 
                //type specific property "RotatedBoundingBox" which
                //is not found on all ContextNode types.
                if (nodeType == ContextNodeType.InkWord)
                {
                    rotatedBoundingBox = ((InkWordNode)node).GetRotatedBoundingBox();
                }
                else if (nodeType == ContextNodeType.Line)
                {
                    rotatedBoundingBox = ((LineNode)node).GetRotatedBoundingBox();
                }
                else if (nodeType == ContextNodeType.Paragraph)
                {
                    rotatedBoundingBox = ((ParagraphNode)node).GetRotatedBoundingBox();
                }
                else if (nodeType == ContextNodeType.WritingRegion ||
                         nodeType == ContextNodeType.InkDrawing ||
                         nodeType == ContextNodeType.InkBullet )
                {

                    // Rotated Bounding Boxes are not a supported option for 
                    // Writing Regions or Drawings.  We return the axis aligned 
                    // bounding box instead
                    Rectangle rect = node.Location.GetBounds();

                    // We need to create a looped list of 4 points to be consistent
                    // with the way InkAnalysis represents rotated bounding boxes.  
                    rotatedBoundingBox = new Point[4];

                    rotatedBoundingBox[0] = new Point(rect.X, rect.Y);
                    rotatedBoundingBox[1] = new Point(rect.Right, rect.Y);
                    rotatedBoundingBox[2] = new Point(rect.Right, rect.Bottom);
                    rotatedBoundingBox[3] = new Point(rect.X, rect.Bottom);

                }


                if (null != rotatedBoundingBox)
                {
                    // We need to convert rectangles from ink units to
                    // pixel units. For that, we need Graphics object
                    // to pass to InkRenderer.InkSpaceToPixel method
                    using (Graphics g = drawArea.CreateGraphics())
                    {
                        // convert each of the points from ink space to pixel space
                        for (int i = 0; i < rotatedBoundingBox.Length; i++)
                        {
                            myInkOverlay.Renderer.InkSpaceToPixel(g, ref rotatedBoundingBox[i]);
                        }

                        //inflate the points by calling helper method
                        InflateHelperMethod(ref rotatedBoundingBox, inflate);

                        // increment the node portion of the polygonPoints array
                        polygonPoints.Add(rotatedBoundingBox);
                    }
                }
            }
            //Return the results
            return polygonPoints;
        }
```



<span data-ttu-id="ebd28-146">剖析器會在分析期間計算 [GetRotatedBoundingBox](/previous-versions/ms569544(v=vs.100)) 。</span><span class="sxs-lookup"><span data-stu-id="ebd28-146">The parser calculates [GetRotatedBoundingBox](/previous-versions/ms569544(v=vs.100)) during analysis.</span></span> <span data-ttu-id="ebd28-147">您可以從應用程式中的旋轉周框方塊存取訊號，有許多有用的原因：</span><span class="sxs-lookup"><span data-stu-id="ebd28-147">You can access the information from the rotated bounding boxes in your application for a number of useful reasons:</span></span>

-   <span data-ttu-id="ebd28-148">偵測或繪製單一線條、段落或其他單位的範圍。</span><span class="sxs-lookup"><span data-stu-id="ebd28-148">Detect or draw the bounds of a single line, paragraph, or other unit.</span></span>
-   <span data-ttu-id="ebd28-149">決定線條或段落的寫入角度。</span><span class="sxs-lookup"><span data-stu-id="ebd28-149">Determine the angle at which a line or paragraph is written.</span></span>
-   <span data-ttu-id="ebd28-150">針對線條、段落或其他單位來執行選取的功能。</span><span class="sxs-lookup"><span data-stu-id="ebd28-150">Implement features such as selection for a line, paragraph, or other unit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebd28-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="ebd28-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebd28-152">基本辨識和筆墨分析</span><span class="sxs-lookup"><span data-stu-id="ebd28-152">Basic Recognition and Ink Analysis</span></span>](basic-recognition-and-ink-analysis.md)
</dt> <dt>

[<span data-ttu-id="ebd28-153">掃描的紙張表單範例</span><span class="sxs-lookup"><span data-stu-id="ebd28-153">Scanned Paper Form Sample</span></span>](scanned-paper-form-sample.md)
</dt> <dt>

[<span data-ttu-id="ebd28-154">筆墨分割範例</span><span class="sxs-lookup"><span data-stu-id="ebd28-154">Ink Divider Sample</span></span>](ink-divider-sample.md)
</dt> </dl>

 

