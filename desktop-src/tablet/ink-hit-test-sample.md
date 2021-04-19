---
description: 此範例說明在給定螢幕位置的情況下，用來尋找筆墨的兩種方法。
ms.assetid: fc581da4-0a7b-4c31-8f73-0784066fcc56
title: 筆墨點擊測試範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d25e6cbc0ed471384bea0cc1977dd38d3ae4830
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991819"
---
# <a name="ink-hit-test-sample"></a><span data-ttu-id="713cb-103">筆墨點擊測試範例</span><span class="sxs-lookup"><span data-stu-id="713cb-103">Ink Hit Test Sample</span></span>

<span data-ttu-id="713cb-104">此範例說明在給定螢幕位置的情況下，用來尋找筆墨的兩種方法。</span><span class="sxs-lookup"><span data-stu-id="713cb-104">This sample illustrates two methods to find ink, given a screen location.</span></span>

<span data-ttu-id="713cb-105">此範例使用下列功能：</span><span class="sxs-lookup"><span data-stu-id="713cb-105">The following features are used in this sample:</span></span>

-   <span data-ttu-id="713cb-106">使用筆墨收集器</span><span class="sxs-lookup"><span data-stu-id="713cb-106">Using an ink collector</span></span>
-   <span data-ttu-id="713cb-107">執行點擊測試</span><span class="sxs-lookup"><span data-stu-id="713cb-107">Performing a hit test</span></span>
-   <span data-ttu-id="713cb-108">找出最接近的點</span><span class="sxs-lookup"><span data-stu-id="713cb-108">Locating the nearest point</span></span>

## <a name="accessing-the-ink-api"></a><span data-ttu-id="713cb-109">存取筆墨 API</span><span class="sxs-lookup"><span data-stu-id="713cb-109">Accessing the Ink API</span></span>

<span data-ttu-id="713cb-110">首先，參考位於 Windows Vista 或 Windows XP Tablet PC Edition 軟體發展工具組中的 Tablet PC 類別 (SDK) 。</span><span class="sxs-lookup"><span data-stu-id="713cb-110">First, reference the Tablet PC classes, located in the Windows Vista or Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
using Microsoft.Ink;
```



## <a name="handling-form-load-and-paint-events"></a><span data-ttu-id="713cb-111">處理表單載入和繪製事件</span><span class="sxs-lookup"><span data-stu-id="713cb-111">Handling Form Load and Paint Events</span></span>

<span data-ttu-id="713cb-112">表單的 Load 事件處理常式：</span><span class="sxs-lookup"><span data-stu-id="713cb-112">The form's Load event handler:</span></span>

-   <span data-ttu-id="713cb-113">建立表單的 [InkCollector](/previous-versions/ms583683(v=vs.100)) 物件（ic）。</span><span class="sxs-lookup"><span data-stu-id="713cb-113">Creates an [InkCollector](/previous-versions/ms583683(v=vs.100)) object, ic, for the form.</span></span>
-   <span data-ttu-id="713cb-114">將 [InkCollector](/previous-versions/ms583683(v=vs.100)) 物件的 [CollectionMode](/previous-versions/ms836497(v=msdn.10)) 屬性設定為忽略手勢。</span><span class="sxs-lookup"><span data-stu-id="713cb-114">Sets the [InkCollector](/previous-versions/ms583683(v=vs.100)) object's [CollectionMode](/previous-versions/ms836497(v=msdn.10)) property to ignore gestures.</span></span>
-   <span data-ttu-id="713cb-115">啟用 [InkCollector](/previous-versions/ms583683(v=vs.100))。</span><span class="sxs-lookup"><span data-stu-id="713cb-115">Enables the [InkCollector](/previous-versions/ms583683(v=vs.100)).</span></span>
-   <span data-ttu-id="713cb-116">將 [InkCollector](/previous-versions/ms583683(v=vs.100)) 物件的 [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) 屬性設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="713cb-116">Sets the [InkCollector](/previous-versions/ms583683(v=vs.100)) object's [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) property to **TRUE**.</span></span>


```C++
// Create the InkCollector, and turn it on
ic = new InkCollector(Handle);  // attach it to the form's frame window

// default to ink-enabled mode
mode = ApplicationMode.Ink;
ic.CollectionMode = CollectionMode.InkOnly;

// turn the collector on
ic.Enabled = true;ic.AutoRedraw = true;
```



<span data-ttu-id="713cb-117">表單的繪製事件處理常式會檢查應用程式模式：</span><span class="sxs-lookup"><span data-stu-id="713cb-117">The form's Paint event handler checks the application mode:</span></span>

-   <span data-ttu-id="713cb-118">在 System.windows.media.visualtreehelper.hittest 模式中，它會繪製圍繞游標的圓形。</span><span class="sxs-lookup"><span data-stu-id="713cb-118">In the HitTest mode, it paints a circle around the cursor.</span></span> <span data-ttu-id="713cb-119">現用畫筆是在應用程式的 handleHitTest 方法中設定。</span><span class="sxs-lookup"><span data-stu-id="713cb-119">The active pen is set in the application's handleHitTest method.</span></span>
-   <span data-ttu-id="713cb-120">在 NearestPoint 模式中，它會在游標和最接近資料指標的點之間繪製紅線。</span><span class="sxs-lookup"><span data-stu-id="713cb-120">In the NearestPoint mode, it paints a red line between the cursor and the point nearest the cursor.</span></span> <span data-ttu-id="713cb-121">最接近的點會在應用程式的 handleNearestPoint 方法中計算。</span><span class="sxs-lookup"><span data-stu-id="713cb-121">The nearest point is calculated in the application's handleNearestPoint method.</span></span>


```C++
if( mode == ApplicationMode.HitTest)
{
    e.Graphics.DrawEllipse(activepen, penPt.X - HitSize/2, penPt.Y - HitSize/2, HitSize, HitSize);
}
else if( mode == ApplicationMode.NearestPoint )
{
    e.Graphics.DrawLine(redPen, penPt, nearestPt);
}
```



<span data-ttu-id="713cb-122">此範例具有非常簡單的重新繪製演算法。</span><span class="sxs-lookup"><span data-stu-id="713cb-122">This sample has a very straightforward repaint algorithm.</span></span> <span data-ttu-id="713cb-123">當其 [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) 屬性設定為 **TRUE** 時，筆墨收集器會在重繪表單時自行重新繪製。</span><span class="sxs-lookup"><span data-stu-id="713cb-123">With its [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) property set to **TRUE**, the ink collector repaints itself when the form is redrawn.</span></span> <span data-ttu-id="713cb-124">為了簡化重新繪製表單的工作，應用程式會追蹤一個周框方塊（invalidateRect 成員變數），以瞭解加入繪圖的區域，這會在每次重繪表單時失效。</span><span class="sxs-lookup"><span data-stu-id="713cb-124">To simplify redrawing the form, the application tracks a bounding box, the invalidateRect member variable, for the area where paint is added, which is invalidated each time the form is redrawn.</span></span>

## <a name="handling-menu-events"></a><span data-ttu-id="713cb-125">處理功能表事件</span><span class="sxs-lookup"><span data-stu-id="713cb-125">Handling Menu Events</span></span>

<span data-ttu-id="713cb-126">Exit 命令會在結束應用程式之前停用 [InkCollector](/previous-versions/ms583683(v=vs.100)) 。</span><span class="sxs-lookup"><span data-stu-id="713cb-126">The Exit command disables the [InkCollector](/previous-versions/ms583683(v=vs.100)) before exiting the application.</span></span>

<span data-ttu-id="713cb-127">筆墨命令會更新應用程式模式和功能表狀態、啟用筆墨收集器，並讓先前繪製的表單區域失效。</span><span class="sxs-lookup"><span data-stu-id="713cb-127">The Ink command updates the application mode and menu status, enables the ink collector, and invalidates the previously painted region of the form.</span></span>

<span data-ttu-id="713cb-128">點擊測試和最接近的點命令都會變更游標、更新應用程式模式和功能表狀態、停用筆墨收集器，並讓先前繪製的表單區域失效。</span><span class="sxs-lookup"><span data-stu-id="713cb-128">Both the Hit Test and Nearest Point commands change the cursor, update the application mode and menu status, disable the ink collector, and invalidate the previously painted region of the form.</span></span>

<span data-ttu-id="713cb-129">清楚！</span><span class="sxs-lookup"><span data-stu-id="713cb-129">The Clear!</span></span> <span data-ttu-id="713cb-130">命令會停用[InkCollector](/previous-versions/ms583683(v=vs.100)) ，同時以新的[筆墨](/previous-versions/ms571716(v=vs.100))物件取代 InkCollector 物件的[筆墨](/previous-versions/ms836505(v=msdn.10))屬性、產生筆墨命令事件，然後強制重新整理控制項。</span><span class="sxs-lookup"><span data-stu-id="713cb-130">command disables the [InkCollector](/previous-versions/ms583683(v=vs.100)) while replacing InkCollector object's [Ink](/previous-versions/ms836505(v=msdn.10)) property with a new [Ink](/previous-versions/ms571716(v=vs.100)) object, generates an Ink command event, and forces a refresh on the control.</span></span>

## <a name="handling-mouse-events"></a><span data-ttu-id="713cb-131">處理滑鼠事件</span><span class="sxs-lookup"><span data-stu-id="713cb-131">Handling Mouse Events</span></span>

<span data-ttu-id="713cb-132">[MouseMove](/previous-versions/ms567617(v=vs.100))事件處理常式會檢查應用程式模式：</span><span class="sxs-lookup"><span data-stu-id="713cb-132">The [MouseMove](/previous-versions/ms567617(v=vs.100)) event handler checks the application mode:</span></span>

-   <span data-ttu-id="713cb-133">在筆墨模式中，它不會執行任何動作，讓筆墨收集器可以正常地收集筆跡。</span><span class="sxs-lookup"><span data-stu-id="713cb-133">In Ink mode, it does nothing, allowing ink to be collected normally by the ink collector.</span></span>
-   <span data-ttu-id="713cb-134">在 System.windows.media.visualtreehelper.hittest 模式中，它會將事件引數傳送至應用程式的 handleHitTest 方法。</span><span class="sxs-lookup"><span data-stu-id="713cb-134">In HitTest mode, it sends the event arguments to the application's handleHitTest method.</span></span>
-   <span data-ttu-id="713cb-135">在 NearestPoint 模式中，它會將事件引數傳送至應用程式的 handleNearestPoint 方法。</span><span class="sxs-lookup"><span data-stu-id="713cb-135">In NearestPoint mode, it sends the event arguments to the application's handleNearestPoint method.</span></span>

## <a name="performing-a-hit-test"></a><span data-ttu-id="713cb-136">執行點擊測試</span><span class="sxs-lookup"><span data-stu-id="713cb-136">Performing a Hit Test</span></span>

<span data-ttu-id="713cb-137">應用程式的 handleHitTest 方法會建立兩個點、游標位置和點 HitSize 距離游標的距離，然後將這兩個點從圖元轉換成筆墨空間座標。</span><span class="sxs-lookup"><span data-stu-id="713cb-137">The application's handleHitTest method creates two points, the cursor location and a point HitSize pixels distant from the cursor, and then converts these two points from pixels to ink space coordinates.</span></span>


```C++
penPt = new Point(e.X, e.Y);
Point pt2 = new Point(e.X, e.Y);
Point pt3 = new Point(e.X + HitSize/2, e.Y);

using (Graphics g = CreateGraphics())
{
    ic.Renderer.PixelToInkSpace(g, ref pt1);
    ic.Renderer.PixelToInkSpace(g, ref pt2);
}
```



<span data-ttu-id="713cb-138">然後， [InkCollector](/previous-versions/ms583683(v=vs.100)) 物件會使用 [system.windows.media.visualtreehelper.hittest () ](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) 方法來尋找 pt3 內的任何筆觸。X-pt2。資料指標的 X 筆墨空間單位，pt2。</span><span class="sxs-lookup"><span data-stu-id="713cb-138">Then, the [InkCollector](/previous-versions/ms583683(v=vs.100)) object uses the [Microsoft.Ink.Ink.HitTest()](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) method to find any strokes that are within pt3.X - pt2.X ink space units of the cursor, pt2.</span></span>


```C++
Strokes strokes = ic.Ink.HitTest(pt2, (float)(pt3.X - pt2.X));
```



<span data-ttu-id="713cb-139">HandleHitTest 方法接著會根據是否找到筆劃來設定畫筆色彩、使 invalidateRect 區域失效、計算點擊測試圓形繪製所在的新區域，然後使新區域失效。</span><span class="sxs-lookup"><span data-stu-id="713cb-139">The handleHitTest method then sets the pen color based on whether strokes were found, invalidates the invalidateRect region, calculates a new region that the hit test circle is drawn in, and then invalidates the new region.</span></span>

## <a name="locating-the-nearest-point"></a><span data-ttu-id="713cb-140">找出最接近的點</span><span class="sxs-lookup"><span data-stu-id="713cb-140">Locating the Nearest Point</span></span>

<span data-ttu-id="713cb-141">應用程式的 handleNearestPoint 方法會建立兩個兩個點，兩者都等於游標的位置，其中一個點 pt，會轉換成筆墨空間，並用於[InkCollector](/previous-versions/ms583683(v=vs.100))[筆墨](/previous-versions/ms836505(v=msdn.10))物件的 NearestPoint 方法呼叫中。</span><span class="sxs-lookup"><span data-stu-id="713cb-141">The application's handleNearestPoint method creates two points both equal to the cursor's location, one of these points, pt, is converted to ink space and used in the call to the NearestPoint method of the [InkCollector](/previous-versions/ms583683(v=vs.100))'s [Ink](/previous-versions/ms836505(v=msdn.10)) object.</span></span> <span data-ttu-id="713cb-142">NearestPoint 方法會傳回最接近該點的 [Stroke](/previous-versions/ms827842(v=msdn.10)) 物件，並設定浮點索引輸出參數。</span><span class="sxs-lookup"><span data-stu-id="713cb-142">The NearestPoint method returns the [Stroke](/previous-versions/ms827842(v=msdn.10)) object closest to the point, and sets the floating point index output parameter.</span></span>


```C++
using (Graphics g = CreateGraphics())
{

   // Remeber pen location
    Point inkPenPt = new Point(e.X, e.Y);

    // Convert the pen location into a location in ink space
    ic.Renderer.PixelToInkSpace(g, ref inkPenPt);

    // ...

    float fIndex;
    Stroke stroke = ic.Ink.NearestPoint(inkPenPt, out fIndex);
```



<span data-ttu-id="713cb-143">如果沒有任何筆觸，NearestPoint 方法會傳回 **Null**，而資料指標位置會當做最接近的點使用。</span><span class="sxs-lookup"><span data-stu-id="713cb-143">If no strokes are present, the NearestPoint method returns **NULL**, and the cursor location is used as the nearest point.</span></span> <span data-ttu-id="713cb-144">否則，會計算對應至浮點數索引之筆劃上的位置。</span><span class="sxs-lookup"><span data-stu-id="713cb-144">Otherwise, the location on the stroke that corresponds to the floating point index is calculated.</span></span>

<span data-ttu-id="713cb-145">最接近的點座標接著會轉換成從筆墨空間算出的圖元，handleNearestPoint 方法接著會使 invalidateRect 區域失效、計算新的區域，該行指向最接近的點，並使新的區域失效。</span><span class="sxs-lookup"><span data-stu-id="713cb-145">The nearest point coordinates are then converted to pixels from ink space, The handleNearestPoint method then invalidates the invalidateRect region, calculates a new region the line to the nearest point is drawn in, and invalidates the new region, too.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="713cb-146">關閉表單</span><span class="sxs-lookup"><span data-stu-id="713cb-146">Closing the Form</span></span>

<span data-ttu-id="713cb-147">表單的 Dispose 方法會處置 [InkCollector](/previous-versions/ms583683(v=vs.100)) 物件。</span><span class="sxs-lookup"><span data-stu-id="713cb-147">The form's Dispose method disposes the [InkCollector](/previous-versions/ms583683(v=vs.100)) object.</span></span>

 

 
