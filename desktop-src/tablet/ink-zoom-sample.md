---
description: 這個範例程式示範如何縮放和滾動筆跡。
ms.assetid: d3b5668a-29bf-4846-8ab0-1bda7b6160f9
title: 筆墨縮放範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f20253a3f56b2a03b5a6dad45ab9a8b72090b5ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511024"
---
# <a name="ink-zoom-sample"></a><span data-ttu-id="8b194-103">筆墨縮放範例</span><span class="sxs-lookup"><span data-stu-id="8b194-103">Ink Zoom Sample</span></span>

<span data-ttu-id="8b194-104">這個範例程式示範如何縮放和滾動筆跡。</span><span class="sxs-lookup"><span data-stu-id="8b194-104">This sample program demonstrates how to zoom and scroll ink.</span></span> <span data-ttu-id="8b194-105">尤其是，它可讓使用者以增量方式放大和縮小墨水。</span><span class="sxs-lookup"><span data-stu-id="8b194-105">In particular, it enables the user to zoom in and out of ink in increments.</span></span> <span data-ttu-id="8b194-106">它也會示範如何使用縮放矩形來放大特定區域。</span><span class="sxs-lookup"><span data-stu-id="8b194-106">It also demonstrates how to zoom into a particular region using a zoom rectangle.</span></span> <span data-ttu-id="8b194-107">最後，此範例說明如何以不同的縮放比例收集筆跡，以及如何在縮放的繪圖區域內設定滾動。</span><span class="sxs-lookup"><span data-stu-id="8b194-107">Finally, this sample illustrates how to collect ink at different zoom ratios and how to set up scrolling within the zoomed drawing area.</span></span>

<span data-ttu-id="8b194-108">在範例中，轉譯 [器物件的](/previous-versions/ms828481(v=msdn.10)) 視圖和物件轉換是用來執行縮放和滾動。</span><span class="sxs-lookup"><span data-stu-id="8b194-108">In the sample, the [Renderer](/previous-versions/ms828481(v=msdn.10)) object's view and object transforms are used to perform zooming and scrolling.</span></span> <span data-ttu-id="8b194-109">視圖轉換適用于點和畫筆寬度。</span><span class="sxs-lookup"><span data-stu-id="8b194-109">The view transform applies to the points and the pen width.</span></span> <span data-ttu-id="8b194-110">物件轉換只適用于點。</span><span class="sxs-lookup"><span data-stu-id="8b194-110">The object transform applies only to the points.</span></span> <span data-ttu-id="8b194-111">使用者可以在 [模式] 功能表上變更 [尺規畫筆寬度] 專案，以控制要使用的轉換。</span><span class="sxs-lookup"><span data-stu-id="8b194-111">The user can control which transform is used by changing the Scale Pen Width item on the Mode menu.</span></span>

> [!Note]  
> <span data-ttu-id="8b194-112">在某些介面方法上執行某些 COM 呼叫會有問題， ([**InkRenderer SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform) 和 [**InkRenderer SetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)，例如在傳送訊息時) 。</span><span class="sxs-lookup"><span data-stu-id="8b194-112">It is problematic to perform some COM calls on certain interface methods ([**InkRenderer.SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform) and [**InkRenderer.SetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform), for example) when a message has been SENT.</span></span> <span data-ttu-id="8b194-113">傳送訊息時，必須將訊息封送處理至 POST 訊息佇列。</span><span class="sxs-lookup"><span data-stu-id="8b194-113">When messages are SENT, they need to be marshalled to the POST message queue.</span></span> <span data-ttu-id="8b194-114">若要解決此案例，請測試您是否要從 POST 處理訊息，方法是呼叫 [**InSendMesssageEx**](/windows/desktop/api/winuser/nf-winuser-insendmessageex) ，並在傳送訊息時將訊息張貼給自己。</span><span class="sxs-lookup"><span data-stu-id="8b194-114">To address this scenario, test whether you are handling a message from POST by calling [**InSendMesssageEx**](/windows/desktop/api/winuser/nf-winuser-insendmessageex) and POST the message to yourself if the message was SENT.</span></span>

 

<span data-ttu-id="8b194-115">此範例使用下列功能：</span><span class="sxs-lookup"><span data-stu-id="8b194-115">The following features are used in this sample:</span></span>

-   <span data-ttu-id="8b194-116">[InkCollector](/previous-versions/ms583683(v=vs.100))物件</span><span class="sxs-lookup"><span data-stu-id="8b194-116">The [InkCollector](/previous-versions/ms583683(v=vs.100)) object</span></span>
-   <span data-ttu-id="8b194-117">轉譯 [器物件](/previous-versions/ms828481(v=msdn.10)) 的 [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) 方法</span><span class="sxs-lookup"><span data-stu-id="8b194-117">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) method</span></span>
-   <span data-ttu-id="8b194-118">轉譯 [器物件](/previous-versions/ms828481(v=msdn.10)) 的 [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) 方法</span><span class="sxs-lookup"><span data-stu-id="8b194-118">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) method</span></span>

## <a name="initializing-the-form"></a><span data-ttu-id="8b194-119">初始化表單</span><span class="sxs-lookup"><span data-stu-id="8b194-119">Initializing the Form</span></span>

<span data-ttu-id="8b194-120">首先，此範例參照的是 Windows Vista 或 Windows XP Tablet PC Edition 軟體發展工具組中提供的 Tablet PC 自動化介面 (SDK) 。</span><span class="sxs-lookup"><span data-stu-id="8b194-120">First, the sample references the Tablet PC Automation interfaces, which are provided in the Windows Vista or Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
using Microsoft.Ink;
```



<span data-ttu-id="8b194-121">此範例會宣告 [InkCollector](/previous-versions/ms583683(v=vs.100))、 `myInkCollector` 和一些私用成員來協助進行調整。</span><span class="sxs-lookup"><span data-stu-id="8b194-121">The sample declares an [InkCollector](/previous-versions/ms583683(v=vs.100)), `myInkCollector`, and some private members to help with scaling.</span></span>


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



<span data-ttu-id="8b194-122">然後，此範例會在表單的[Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1)事件處理常式中建立並啟用[InkCollector](/previous-versions/ms583683(v=vs.100)) 。</span><span class="sxs-lookup"><span data-stu-id="8b194-122">Then the sample creates and enables the [InkCollector](/previous-versions/ms583683(v=vs.100)) in the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler.</span></span> <span data-ttu-id="8b194-123">此外，也會設定 InkCollector 物件之[system.windows.controls.inkcanvas.defaultdrawingattributes](/previous-versions/ms836500(v=msdn.10))屬性的[Width](/previous-versions/ms837941(v=msdn.10))屬性。</span><span class="sxs-lookup"><span data-stu-id="8b194-123">Also, the [Width](/previous-versions/ms837941(v=msdn.10)) property of the InkCollector object's [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property is set.</span></span> <span data-ttu-id="8b194-124">最後，會定義捲軸範圍，並呼叫應用程式的 `UpdateZoomAndScroll` 方法。</span><span class="sxs-lookup"><span data-stu-id="8b194-124">Finally, the scroll bar ranges are defined and the application's `UpdateZoomAndScroll` method is called.</span></span>


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



## <a name="updating-the-zoom-and-scroll-values"></a><span data-ttu-id="8b194-125">更新縮放和滾動值</span><span class="sxs-lookup"><span data-stu-id="8b194-125">Updating the Zoom and Scroll Values</span></span>

<span data-ttu-id="8b194-126">筆墨收集器的繪圖區域會受到許多事件的影響。</span><span class="sxs-lookup"><span data-stu-id="8b194-126">The drawing area of the ink collector is affected by many events.</span></span> <span data-ttu-id="8b194-127">在 `UpdateZoomAndScroll` 方法中，會使用轉換矩陣來調整和轉譯視窗內的筆墨收集器。</span><span class="sxs-lookup"><span data-stu-id="8b194-127">In the `UpdateZoomAndScroll` method, a transformation matrix is used to both scale and translate the ink collector within the window.</span></span>

> [!Note]  
> <span data-ttu-id="8b194-128">轉譯 [器物件](/previous-versions/ms828481(v=msdn.10)) 的 [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) 方法會將轉換套用至筆劃和畫筆寬度，而 [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) 方法只會將轉換套用至筆觸。</span><span class="sxs-lookup"><span data-stu-id="8b194-128">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) method applies the transform to both the strokes and the pen width, while the [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) method only applies the transform to the strokes.</span></span>

 

<span data-ttu-id="8b194-129">最後，會呼叫應用程式的 `UpdateScrollBars` 方法，並強制重新整理表單。</span><span class="sxs-lookup"><span data-stu-id="8b194-129">Finally, the application's `UpdateScrollBars` method is called and the form is forced to refresh.</span></span>


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



## <a name="managing-the-scroll-bars"></a><span data-ttu-id="8b194-130">管理捲軸</span><span class="sxs-lookup"><span data-stu-id="8b194-130">Managing the Scroll Bars</span></span>

<span data-ttu-id="8b194-131">`UpdateScrollBars`方法會設定捲軸，以在[InkCollector](/previous-versions/ms583683(v=vs.100))內的目前視窗大小、縮放設定和捲軸位置正常運作。</span><span class="sxs-lookup"><span data-stu-id="8b194-131">The `UpdateScrollBars` method sets up the scroll bars to work correctly with the current window size, zoom setting, and scroll location within the [InkCollector](/previous-versions/ms583683(v=vs.100)).</span></span> <span data-ttu-id="8b194-132">這個方法會計算垂直和水準捲軸的大型變更和小變更值。</span><span class="sxs-lookup"><span data-stu-id="8b194-132">This method calculates the large change and small change values for the vertical and horizontal scroll bars.</span></span> <span data-ttu-id="8b194-133">它也會計算捲軸的目前值，以及是否應顯示捲軸。</span><span class="sxs-lookup"><span data-stu-id="8b194-133">It also calculates the current value of the scroll bars and whether they should be visible.</span></span> <span data-ttu-id="8b194-134">轉譯 [器物件](/previous-versions/ms828481(v=msdn.10)) 的 [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) 方法會處理從圖元到縮放座標空間的轉換，以及透過視圖和物件轉換套用的任何縮放和滾動的帳戶。</span><span class="sxs-lookup"><span data-stu-id="8b194-134">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) method handles the conversion from pixels to the zoomed coordinate space and accounts for any scaling and scrolling that is applied through the view and object transforms.</span></span>


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



## <a name="zooming-to-a-rectangle"></a><span data-ttu-id="8b194-135">縮放至矩形</span><span class="sxs-lookup"><span data-stu-id="8b194-135">Zooming to a Rectangle</span></span>

<span data-ttu-id="8b194-136">`pnlDrawingArea`面板事件處理常式可管理將矩形繪製至視窗。</span><span class="sxs-lookup"><span data-stu-id="8b194-136">The `pnlDrawingArea` panel event handlers manage drawing the rectangle to the window.</span></span> <span data-ttu-id="8b194-137">如果在 [模式] 功能表上選取 [縮放至 Rect] 命令，則 [MouseUp](/previous-versions/ms567618(v=vs.100)) 事件處理常式會呼叫應用程式的 `ZoomToRectangle` 方法。</span><span class="sxs-lookup"><span data-stu-id="8b194-137">If the Zoom To Rect command is checked on the Mode menu, then the [MouseUp](/previous-versions/ms567618(v=vs.100)) event handler calls the application's `ZoomToRectangle` method.</span></span> <span data-ttu-id="8b194-138">`ZoomToRectangle`方法會計算矩形的寬度和高度、檢查界限條件、更新捲軸值和縮放因數，然後呼叫應用程式的 `UpdateZoomAndScroll` 方法以套用新的設定。</span><span class="sxs-lookup"><span data-stu-id="8b194-138">The `ZoomToRectangle` method calculates the width and height of the rectangle, checks for boundary conditions, updates the scroll bar values and the scale factor, and then calls the application's `UpdateZoomAndScroll` method to apply the new settings.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="8b194-139">關閉表單</span><span class="sxs-lookup"><span data-stu-id="8b194-139">Closing the Form</span></span>

<span data-ttu-id="8b194-140">表單的 [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) 方法會處置 [InkCollector](/previous-versions/ms583683(v=vs.100)) 物件。</span><span class="sxs-lookup"><span data-stu-id="8b194-140">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms583683(v=vs.100)) object.</span></span>

 

 
