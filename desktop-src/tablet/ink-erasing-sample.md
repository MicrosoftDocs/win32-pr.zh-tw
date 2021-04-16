---
description: 此應用程式是以筆跡集合範例範例為基礎，藉由示範筆跡筆劃刪除來建立。 此範例會為使用者提供有四種模式可供選擇的功能表：啟用筆墨、在尖點清除、在交集處清除，以及清除筆觸。
ms.assetid: cec912ee-1645-47e1-8988-626719549e55
title: 筆跡清除範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46040781d778f936815e57ba96b4ca516617d9a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511026"
---
# <a name="ink-erasing-sample"></a><span data-ttu-id="5d1a6-104">筆跡清除範例</span><span class="sxs-lookup"><span data-stu-id="5d1a6-104">Ink Erasing Sample</span></span>

<span data-ttu-id="5d1a6-105">此應用程式是以 [筆跡集合範例](ink-collection-sample.md) 範例為基礎，藉由示範筆跡筆劃刪除來建立。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-105">This application builds on the [Ink Collection Sample](ink-collection-sample.md) sample by demonstrating ink strokes deletion.</span></span> <span data-ttu-id="5d1a6-106">此範例會為使用者提供有四種模式可供選擇的功能表：啟用筆墨、在尖點清除、在交集處清除，以及清除筆觸。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-106">The sample provides the user with a menu that has four modes to choose from: ink-enabled, erasing at cusp, erasing at intersections, and erasing strokes.</span></span>

<span data-ttu-id="5d1a6-107">在啟用筆墨的模式中， [InkCollector](/previous-versions/ms836493(v=msdn.10)) 物件會收集筆墨，如 [筆墨收集範例](ink-collection-sample.md)所示。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-107">In ink-enabled mode, the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object collects ink as shown in [Ink Collection Sample](ink-collection-sample.md).</span></span>

<span data-ttu-id="5d1a6-108">在清除模式中，會清除使用者與游標接觸的現有筆墨筆劃區段。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-108">In an erasing mode, segments of existing ink strokes that the user touches with the cursor are erased.</span></span> <span data-ttu-id="5d1a6-109">此外，cusps 或交集可能會以紅色圓圈標記。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-109">Also, the cusps or intersections may be marked with a red circle.</span></span>

<span data-ttu-id="5d1a6-110">此範例最有趣的部分是在表單的 `InkErase` `OnPaint` 事件處理常式中，以及從表單的 `OnMouseMove` 事件處理常式呼叫的清除函式中。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-110">The most interesting parts of this sample lie in the `InkErase` form's `OnPaint` event handler and in the erasing functions that are called from the form's `OnMouseMove` event handler.</span></span>

## <a name="circling-the-cusps-and-intersections"></a><span data-ttu-id="5d1a6-111">圈 Cusps 和交集</span><span class="sxs-lookup"><span data-stu-id="5d1a6-111">Circling the Cusps and Intersections</span></span>

<span data-ttu-id="5d1a6-112">表單的 `OnPaint` 事件處理常式會先繪製筆劃，視應用程式模式而定，可能會找出所有的 cusps 或交集，並將其標示為一個小的紅色圓圈。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-112">The form's `OnPaint` event handler first paints the strokes, and depending on the application mode, may find and mark all of the cusps or intersections with a small red circle.</span></span> <span data-ttu-id="5d1a6-113">尖點會標示筆劃的方向突然變更。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-113">A cusp marks the point where a stroke changes direction abruptly.</span></span> <span data-ttu-id="5d1a6-114">交集會標示一個筆劃與本身或另一個筆劃相交的點。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-114">An intersection marks a point where one stroke intersects with itself or another stroke.</span></span>

<span data-ttu-id="5d1a6-115">每當重新繪製控制項時，就會發生 [繪製](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) 事件。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-115">The [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) event occurs whenever a control is redrawn.</span></span>

> [!Note]  
> <span data-ttu-id="5d1a6-116">此範例會強制表單在每次刪除筆劃時重繪自己，或在應用程式模式變更時，使用表單的 [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) 方法。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-116">The sample forces the form to redraw itself whenever a stroke is erased, or when the application mode changes, using the form's [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) method.</span></span>

 


```C++
private void InkErase_OnPaint(object sender, PaintEventArgs e)
{
    Strokes strokesToPaint = myInkCollector.Ink.Strokes;

    myInkCollector.Renderer.Draw(e.Graphics, strokesToPaint);

    switch (mode)
    {
        case ApplicationMode.CuspErase:
            PaintCusps(e.Graphics, strokesToPaint);
            break;
        case ApplicationMode.IntersectErase:
            PaintIntersections(e.Graphics, strokesToPaint);
            break;
    }
}
```



<span data-ttu-id="5d1a6-117">在中 `PaintCusps` ，程式碼會逐一查看每個筆劃中的每個尖點，並在其周圍繪製紅色圓圈。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-117">In `PaintCusps`, the code iterates through each cusp in each stroke, and draws a red circle around it.</span></span> <span data-ttu-id="5d1a6-118">筆劃的 [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) 屬性會傳回對應至 cusps 之搧風內的點索引。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-118">The stroke's [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) property returns the indices of the points within a stoke that correspond to cusps.</span></span> <span data-ttu-id="5d1a6-119">此外，請注意轉譯 [器物件的](/previous-versions/ms828481(v=msdn.10)) [InkSpaceToPixel](/previous-versions/ms828495(v=msdn.10)) 方法，它會將點轉換成與 DrawEllipse 方法相關的座標。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-119">Also, note the [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [InkSpaceToPixel](/previous-versions/ms828495(v=msdn.10)) method, which converts the point to coordinates relevant to the DrawEllipse method.</span></span>


```C++
private void PaintCusps(Graphics g, Strokes strokesToPaint)
{
    foreach (Stroke currentStroke in strokesToPaint)
    {
        int[] cusps = currentStroke.PolylineCusps;

        foreach (int i in cusps)
        {
            Point pt = currentStroke.GetPoint(i);

            // Convert the X, Y position to Window based pixel coordinates
            myInkCollector.Renderer.InkSpaceToPixel(g, ref pt);

            // Draw a red circle as the cusp position
            g.DrawEllipse(Pens.Red, pt.X-3, pt.Y-3, 6, 6);
        }
    }
}
```



<span data-ttu-id="5d1a6-120">在中 `PaintIntersections` ，程式碼會逐一查看每個筆劃，以找出與整個筆劃組合的交集。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-120">In `PaintIntersections`, the code iterates through each stroke to find its intersections with the entire set of strokes.</span></span> <span data-ttu-id="5d1a6-121">請注意，筆劃的 [FindIntersections](/previous-versions/ms827856(v=msdn.10)) 方法會傳遞 [筆劃](/previous-versions/ms827799(v=msdn.10)) 集合，並傳回代表交集的浮點索引值陣列。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-121">Note that the stroke's [FindIntersections](/previous-versions/ms827856(v=msdn.10)) method is passed a [Strokes](/previous-versions/ms827799(v=msdn.10)) collection and returns an array of floating point index values representing the intersections.</span></span> <span data-ttu-id="5d1a6-122">然後，程式碼會計算每個交集的 X-y 座標，並在其周圍繪製紅色圓圈。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-122">The code then calculates an X-Y coordinate for each intersection, and draws a red circle around it.</span></span>


```C++
private void PaintIntersections(Graphics g, Strokes strokesToPaint)
{
    foreach (Stroke currentStroke in strokesToPaint)
    {
        float[] intersections =            currentStroke.FindIntersections(strokesToPaint);
    }
}
```



## <a name="handling-a-pen-that-has-two-ends"></a><span data-ttu-id="5d1a6-123">處理具有兩個端點的畫筆</span><span class="sxs-lookup"><span data-stu-id="5d1a6-123">Handling a Pen That Has Two Ends</span></span>

<span data-ttu-id="5d1a6-124">針對[CursorDown](/previous-versions/ms567611(v=vs.100))、 [NewPackets](/previous-versions/ms567621(v=vs.100))和[筆觸](/previous-versions/ms567622(v=vs.100))事件的[InkCollector](/previous-versions/ms836493(v=msdn.10))物件，會定義三個事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-124">Three event handlers are defined for the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object for the [CursorDown](/previous-versions/ms567611(v=vs.100)), [NewPackets](/previous-versions/ms567621(v=vs.100)), and [Stroke](/previous-versions/ms567622(v=vs.100)) events.</span></span> <span data-ttu-id="5d1a6-125">每個事件處理常式都會檢查資料 [指標](/previous-versions/ms839521(v=msdn.10)) 物件的 [反向](/previous-versions/ms839525(v=msdn.10)) 屬性，以查看正在使用的畫筆端點。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-125">Each event handler checks the [Cursor](/previous-versions/ms839521(v=msdn.10)) object's [Inverted](/previous-versions/ms839525(v=msdn.10)) property to see which end of the pen is being used.</span></span> <span data-ttu-id="5d1a6-126">當畫筆反轉時：</span><span class="sxs-lookup"><span data-stu-id="5d1a6-126">When the pen is inverted:</span></span>

-   <span data-ttu-id="5d1a6-127">`myInkCollector_CursorDown`方法會讓筆觸變成透明。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-127">The `myInkCollector_CursorDown` method makes the stroke transparent.</span></span>
-   <span data-ttu-id="5d1a6-128">`myInkCollector_NewPackets`方法會清除筆觸。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-128">The `myInkCollector_NewPackets` method erases strokes.</span></span>
-   <span data-ttu-id="5d1a6-129">`myInkCollector_Stroke`方法會取消事件。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-129">The `myInkCollector_Stroke` method cancels the event.</span></span> <span data-ttu-id="5d1a6-130">[NewPackets](/previous-versions/ms567621(v=vs.100)) 事件會在 [筆觸](/previous-versions/ms567622(v=vs.100)) 事件之前產生。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-130">[NewPackets](/previous-versions/ms567621(v=vs.100)) events are generated prior to the [Stroke](/previous-versions/ms567622(v=vs.100)) event.</span></span>

## <a name="tracking-the-cursor"></a><span data-ttu-id="5d1a6-131">追蹤資料指標</span><span class="sxs-lookup"><span data-stu-id="5d1a6-131">Tracking the Cursor</span></span>

<span data-ttu-id="5d1a6-132">無論使用者是使用畫筆或滑鼠，都會產生 [MouseMove](/previous-versions/ms567617(v=vs.100)) 事件。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-132">Whether the user is using a pen or a mouse, [MouseMove](/previous-versions/ms567617(v=vs.100)) events are generated.</span></span> <span data-ttu-id="5d1a6-133">MouseMove 事件處理常式會先進行檢查，以判斷目前的模式是否為清除模式，如果按下任何滑鼠按鍵，則會忽略該事件（如果這些狀態不存在的話）。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-133">The MouseMove event handler first checks to determine whether the current mode is an erase mode and if any mouse button is pressed, and ignores the event if these states are not present.</span></span> <span data-ttu-id="5d1a6-134">然後，事件處理常式會使用轉譯 [器物件的](/previous-versions/ms828481(v=msdn.10)) [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) 方法，將游標的圖元座標轉換成筆墨空間座標，並根據目前的清除模式呼叫其中一個程式碼的清除方法。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-134">Then, the event handler converts the pixel coordinates for the cursor into ink space coordinates by using the [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) method, and calls one of the code's erase methods depending on the current erase mode.</span></span>

## <a name="erasing-strokes"></a><span data-ttu-id="5d1a6-135">清除筆觸</span><span class="sxs-lookup"><span data-stu-id="5d1a6-135">Erasing Strokes</span></span>

<span data-ttu-id="5d1a6-136">`EraseStrokes`方法會採用筆墨空間中的游標位置，並產生單位內的筆劃集合 `HitTestRadius` 。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-136">The `EraseStrokes` method takes the cursor's location in ink space and generates a collection of strokes that are within `HitTestRadius` units.</span></span> <span data-ttu-id="5d1a6-137">`currentStroke`參數指定不應刪除的[筆觸](/previous-versions/ms827842(v=msdn.10))物件。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-137">The `currentStroke` parameter specifies a [Stroke](/previous-versions/ms827842(v=msdn.10)) object that should not be deleted.</span></span> <span data-ttu-id="5d1a6-138">然後，會從收集器中刪除筆劃集合，然後重新繪製表單。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-138">Then the strokes collection is deleted from the collector, and the form is redrawn.</span></span>


```C++
private void EraseStrokes(Point pt, Stroke currentStroke)
{
    Strokes strokesHit = myInkCollector.Ink.HitTest(pt, HitTestRadius);

    if (null!=currentStroke && strokesHit.Contains(currentStroke))
    {
        strokesHit.Remove(currentStroke);
    }

    myInkCollector.Ink.DeleteStrokes(strokesHit);

    if (strokesHit.Count > 0)
    {
        this.Refresh();
    }
}
```



## <a name="erasing-at-intersections"></a><span data-ttu-id="5d1a6-139">在交集處清除</span><span class="sxs-lookup"><span data-stu-id="5d1a6-139">Erasing at Intersections</span></span>

<span data-ttu-id="5d1a6-140">`EraseAtIntersections`方法會反復查看落在測試半徑內的每個筆劃，並產生該筆劃和集合中所有其他筆劃之間的交集陣列。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-140">The `EraseAtIntersections` method iterates over each stroke that falls within the test radius and generates an array of intersections between that stroke and all the other strokes in the collection.</span></span> <span data-ttu-id="5d1a6-141">如果找不到任何交集，則會刪除整個筆劃;否則，在指向測試點的筆劃上，最接近的點會位於該點的任一邊，並描述要移除的區段。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-141">If no intersections are found, then that entire stroke is deleted; otherwise, the nearest point on the stroke to the test point is located, and from that, the intersections on either side of the point are located, describing the segment to be removed.</span></span>

<span data-ttu-id="5d1a6-142">[筆觸](/previous-versions/ms827842(v=msdn.10))物件的[Split](/previous-versions/ms828477(v=msdn.10))方法是用來將區段與其余筆劃分開，然後刪除區段，讓其餘的筆觸保持不變。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-142">The [Stroke](/previous-versions/ms827842(v=msdn.10)) object's [Split](/previous-versions/ms828477(v=msdn.10)) method is used to separate the segment from the rest of the stroke, and then the segment is deleted, leaving the rest of the stroke intact.</span></span> <span data-ttu-id="5d1a6-143">在中 `EraseStrokes` ，會在方法傳回之前重新繪製表單。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-143">As in `EraseStrokes`, the form is redrawn before the method returns.</span></span>


```C++
private void EraseAtIntersections(Point pt)
{
    Strokes strokesHit = myInkCollector.Ink.HitTest(pt, HitTestRadius);

    foreach (Stroke currentStroke in strokesHit)
    {
        float[] intersections = currentStroke.FindIntersections(myInkCollector.Ink.Strokes);
        ...
        float findex = currentStroke.NearestPoint(pt);
        ...
        strokeToDelete = currentStroke.Split(intersections[i]);
        ...
    }
    ...
}
```



## <a name="erasing-at-cusps"></a><span data-ttu-id="5d1a6-144">在 Cusps 清除</span><span class="sxs-lookup"><span data-stu-id="5d1a6-144">Erasing at Cusps</span></span>

<span data-ttu-id="5d1a6-145">針對落在測試半徑內的每個筆劃， `EraseAtCusps` 方法會從 [stroke](/previous-versions/ms827842(v=msdn.10)) 物件的 [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) 方法中抓取 cusps 陣列。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-145">For each stroke that falls within the test radius, the `EraseAtCusps` method retrieves the array of cusps from the [Stroke](/previous-versions/ms827842(v=msdn.10)) object's [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) method.</span></span> <span data-ttu-id="5d1a6-146">筆劃的每一端也是尖點，因此，如果筆劃只有兩個 cusps，則會刪除整個筆劃;否則，在指向測試點的筆劃上，最接近的點會位於該點的任一邊，並描述要移除的區段。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-146">Each end of the stroke is also a cusp, so if the stroke only has two cusps, then the entire stroke is deleted; otherwise, the nearest point on the stroke to the test point is located, and from that, the intersections on either side of the point are located, describing the segment to be removed.</span></span>

<span data-ttu-id="5d1a6-147">[筆觸](/previous-versions/ms827842(v=msdn.10))物件的[Split](/previous-versions/ms828477(v=msdn.10))方法是用來將區段與其余筆劃分開，然後刪除區段，讓其餘的筆觸保持不變。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-147">The [Stroke](/previous-versions/ms827842(v=msdn.10)) object's [Split](/previous-versions/ms828477(v=msdn.10)) method is used to separate the segment from the rest of the stroke, and then the segment is deleted, leaving the rest of the stroke intact.</span></span> <span data-ttu-id="5d1a6-148">在中 `EraseStrokes` ，會在方法傳回之前重新繪製表單。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-148">As in `EraseStrokes`, the form is redrawn before the method returns.</span></span>


```C++
private void EraseAtCusps(Point pt)
{
    ...
    strokesHit = myInkCollector.Ink.HitTest(pt, HitTestRadius);
    
    foreach (Stroke currentStroke in strokesHit)
    {
        int[] cusps = currentStroke.PolylineCusps;
        ...
        float findex = currentStroke.NearestPoint(pt);
        ...
        strokeToDelete = currentStroke.Split(cusps[i]); 
        myInkCollector.Ink.DeleteStroke(strokeToDelete);
        ...
    }
    ...
}
```



## <a name="closing-the-form"></a><span data-ttu-id="5d1a6-149">關閉表單</span><span class="sxs-lookup"><span data-stu-id="5d1a6-149">Closing the Form</span></span>

<span data-ttu-id="5d1a6-150">表單的 [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) 方法會處置 [InkCollector](/previous-versions/ms836493(v=msdn.10)) 物件 `myInkCollector` 。</span><span class="sxs-lookup"><span data-stu-id="5d1a6-150">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object, `myInkCollector`.</span></span>

 

 
