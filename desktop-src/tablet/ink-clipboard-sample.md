---
description: 此程式示範如何將筆墨複製並貼到另一個應用程式。 它也可讓使用者複製選取的筆劃，然後將結果貼入現有的筆跡物件中。
ms.assetid: a0c42f1c-543d-44f8-83d9-fe810de410ff
title: 筆墨剪貼簿範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95c5da0bc0ba9a7e3a1b4e1a5c52784f10fb2023
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511308"
---
# <a name="ink-clipboard-sample"></a><span data-ttu-id="b6743-104">筆墨剪貼簿範例</span><span class="sxs-lookup"><span data-stu-id="b6743-104">Ink Clipboard Sample</span></span>

<span data-ttu-id="b6743-105">此程式示範如何將筆墨複製並貼到另一個應用程式。</span><span class="sxs-lookup"><span data-stu-id="b6743-105">This program demonstrates how to copy and paste ink into another application.</span></span> <span data-ttu-id="b6743-106">它也可讓使用者複製選取的筆劃，然後將結果貼入現有的筆跡物件中。</span><span class="sxs-lookup"><span data-stu-id="b6743-106">It also enables the user to copy a selection of strokes and paste the result into the existing ink object.</span></span>

<span data-ttu-id="b6743-107">可用的剪貼簿模式如下：</span><span class="sxs-lookup"><span data-stu-id="b6743-107">The following clipboard modes are available:</span></span>

-   <span data-ttu-id="b6743-108"> (ISF 的筆墨序列化格式) </span><span class="sxs-lookup"><span data-stu-id="b6743-108">Ink serialized format (ISF)</span></span>
-   <span data-ttu-id="b6743-109"> 中繼檔</span><span class="sxs-lookup"><span data-stu-id="b6743-109">Metafile</span></span>
-   <span data-ttu-id="b6743-110">加強型中繼檔 (EMF) </span><span class="sxs-lookup"><span data-stu-id="b6743-110">Enhanced Metafile (EMF)</span></span>
-   <span data-ttu-id="b6743-111">點陣圖</span><span class="sxs-lookup"><span data-stu-id="b6743-111">Bitmap</span></span>
-   <span data-ttu-id="b6743-112">文字筆墨</span><span class="sxs-lookup"><span data-stu-id="b6743-112">Text Ink</span></span>
-   <span data-ttu-id="b6743-113">草圖筆墨</span><span class="sxs-lookup"><span data-stu-id="b6743-113">Sketch Ink</span></span>

<span data-ttu-id="b6743-114">文字筆跡和草圖筆墨是兩種類型的筆墨控制項，分別用來做為文字或繪圖。</span><span class="sxs-lookup"><span data-stu-id="b6743-114">Text ink and sketch ink are two types of ink controls used as text or drawing respectively.</span></span> <span data-ttu-id="b6743-115">您可以貼上 ISF、文字筆墨，然後將筆墨草圖至現有筆跡。</span><span class="sxs-lookup"><span data-stu-id="b6743-115">It is possible to paste ISF, text ink, and sketch ink into existing ink.</span></span>

<span data-ttu-id="b6743-116">除了剪貼簿之外，此範例也會說明如何使用「套索」工具來選取筆觸。</span><span class="sxs-lookup"><span data-stu-id="b6743-116">In addition to the clipboard, this sample also illustrates how to select strokes with the lasso tool.</span></span> <span data-ttu-id="b6743-117">使用者可以移動選取的筆劃並修改其繪製屬性。</span><span class="sxs-lookup"><span data-stu-id="b6743-117">The user can move selected strokes and modify their drawing attributes.</span></span> <span data-ttu-id="b6743-118">這項功能是筆墨重迭控制項已提供的選取功能的子集;它是在這裡執行，以供說明之用。</span><span class="sxs-lookup"><span data-stu-id="b6743-118">This functionality is a subset of the selection functionality already provided by the ink overlay control; it is implemented here for illustrative purposes.</span></span>

<span data-ttu-id="b6743-119">此範例使用下列功能：</span><span class="sxs-lookup"><span data-stu-id="b6743-119">The following features are used in this sample:</span></span>

-   <span data-ttu-id="b6743-120">[InkCollector](/previous-versions/ms583683(v=vs.100))物件。</span><span class="sxs-lookup"><span data-stu-id="b6743-120">The [InkCollector](/previous-versions/ms583683(v=vs.100)) object.</span></span>
-   <span data-ttu-id="b6743-121">筆墨剪貼簿支援。</span><span class="sxs-lookup"><span data-stu-id="b6743-121">Ink clipboard support.</span></span>
-   <span data-ttu-id="b6743-122">搭配使用 [system.windows.media.visualtreehelper.hittest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) 方法與套索的用法。</span><span class="sxs-lookup"><span data-stu-id="b6743-122">The use of the lasso with the [Microsoft.Ink.Ink.HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) method.</span></span>

<span data-ttu-id="b6743-123">這個範例會示範如何轉譯筆墨、複製該筆墨，然後將筆墨貼到另一個應用程式（例如 Microsoft 小畫家）。</span><span class="sxs-lookup"><span data-stu-id="b6743-123">This sample demonstrates rendering ink, copying that ink, and then pasting the ink into another application such as Microsoft Paint.</span></span>

## <a name="collecting-ink-and-setting-up-the-form"></a><span data-ttu-id="b6743-124">收集筆墨並設定表單</span><span class="sxs-lookup"><span data-stu-id="b6743-124">Collecting Ink and Setting Up the Form</span></span>

<span data-ttu-id="b6743-125">首先，請參考隨 Microsoft Windows <entity type="reg"/> XP TABLET PC Edition 軟體發展工具組一起安裝的 TABLET Pc 自動化介面 (SDK) 。</span><span class="sxs-lookup"><span data-stu-id="b6743-125">First, reference the Tablet PC Automation interfaces, which are installed with the Microsoft Windows<entity type="reg"/> XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
using Microsoft.Ink;
```



<span data-ttu-id="b6743-126">接下來，此表單會宣告一些常數和欄位，此範例稍後會加以注明。</span><span class="sxs-lookup"><span data-stu-id="b6743-126">Next, the form declares some constants and fields that are noted later in this sample.</span></span>


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



<span data-ttu-id="b6743-127">最後，在表單的 [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) 事件處理常式中，會將表單初始化、建立表單的 [InkCollector](/previous-versions/ms583683(v=vs.100)) 物件，並啟用筆墨收集器。</span><span class="sxs-lookup"><span data-stu-id="b6743-127">Finally, in the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler, the form is initialized, an [InkCollector](/previous-versions/ms583683(v=vs.100)) object for the form is created and the ink collector is enabled.</span></span>


```C++
// Create an ink collector and assign it to this form's window
myInkCollector = new InkCollector(this.Handle);

// Turn the ink collector on
myInkCollector.Enabled = true;
```



## <a name="handling-menu-events"></a><span data-ttu-id="b6743-128">處理功能表事件</span><span class="sxs-lookup"><span data-stu-id="b6743-128">Handling Menu Events</span></span>

<span data-ttu-id="b6743-129">功能表項目事件處理常式主要會更新表單的狀態。</span><span class="sxs-lookup"><span data-stu-id="b6743-129">The menu item event handlers primarily update the form's state.</span></span>

<span data-ttu-id="b6743-130">Clear 命令會移除選取矩形，並從筆墨收集器的 [筆墨](/previous-versions/ms583670(v=vs.100)) 物件刪除筆觸。</span><span class="sxs-lookup"><span data-stu-id="b6743-130">The Clear command removes the selection rectangle, and deletes the strokes from the ink collector's [Ink](/previous-versions/ms583670(v=vs.100)) object.</span></span>

<span data-ttu-id="b6743-131">Exit 命令會在結束應用程式之前停用筆墨收集器。</span><span class="sxs-lookup"><span data-stu-id="b6743-131">The Exit command disables the ink collector before exiting the application.</span></span>

<span data-ttu-id="b6743-132">[編輯] 功能表會根據表單的選取狀態來啟用剪下和複製命令，並根據 [剪貼簿] 的內容啟用 [貼上] 命令（使用 [筆墨](/previous-versions/ms583670(v=vs.100)) 物件的 [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) 方法來判斷）。</span><span class="sxs-lookup"><span data-stu-id="b6743-132">The Edit menu enables the Cut and Copy commands based on the selection state of the form, and enables the Paste command based on the contents of the clipboard, determined by using the [Ink](/previous-versions/ms583670(v=vs.100)) object's [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) method.</span></span>

<span data-ttu-id="b6743-133">剪下和複製命令都使用 helper 方法將筆墨複製到剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="b6743-133">The Cut and Copy commands both use a helper method to copy ink to the clipboard.</span></span> <span data-ttu-id="b6743-134">剪下命令會使用 helper 方法來刪除選取的筆劃。</span><span class="sxs-lookup"><span data-stu-id="b6743-134">The Cut command uses a helper method to delete the selected strokes.</span></span>

<span data-ttu-id="b6743-135">[貼上] 命令會先檢查 [筆墨](/previous-versions/ms583670(v=vs.100)) 物件的 [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) 方法，以查看是否可以貼上剪貼簿上的物件。</span><span class="sxs-lookup"><span data-stu-id="b6743-135">The Paste command first checks the [Ink](/previous-versions/ms583670(v=vs.100)) object's [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) method to see if the object on the clipboard can be pasted.</span></span> <span data-ttu-id="b6743-136">然後，貼上命令會計算貼上區域的左上角，將座標從圖元轉換成筆墨空間，然後將剪貼簿中的筆觸貼到筆墨收集器。</span><span class="sxs-lookup"><span data-stu-id="b6743-136">The Paste command then computes the upper-left corner for the paste region, converts the coordinates from pixels to ink space, and pastes the strokes from the clipboard to the ink collector.</span></span> <span data-ttu-id="b6743-137">最後，選取方塊也會更新。</span><span class="sxs-lookup"><span data-stu-id="b6743-137">Finally, the selection box is updated.</span></span>


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



<span data-ttu-id="b6743-138">Select 和 Ink 命令會更新應用程式模式和預設的繪圖屬性、清除目前的選取專案、更新功能表狀態，以及重新整理表單。</span><span class="sxs-lookup"><span data-stu-id="b6743-138">The Select and Ink commands update the application mode and the default drawing attributes, clear the current selection, update the menu state, and refresh the form.</span></span> <span data-ttu-id="b6743-139">其他處理常式會依賴應用程式狀態來執行正確的函式，也就是 lassoing 或配置筆墨。</span><span class="sxs-lookup"><span data-stu-id="b6743-139">Other handlers rely on the application state to perform the correct function, either lassoing or laying down ink.</span></span> <span data-ttu-id="b6743-140">此外，Select 命令會將 [NewPackets](/previous-versions/ms567621(v=vs.100)) 和 [筆觸](/previous-versions/ms567622(v=vs.100)) 事件處理常式加入至筆墨收集器，而筆墨命令會將這些事件處理常式從筆墨收集器中移除。</span><span class="sxs-lookup"><span data-stu-id="b6743-140">In addition, the Select command adds the [NewPackets](/previous-versions/ms567621(v=vs.100)) and [Stroke](/previous-versions/ms567622(v=vs.100)) event handlers to the ink collector and the Ink command removes these event handlers from the ink collector.</span></span>

<span data-ttu-id="b6743-141">複製筆劃時，剪貼簿上可用的格式會列在 [格式] 功能表上，而使用者則會選取從這份清單複製筆墨的格式。</span><span class="sxs-lookup"><span data-stu-id="b6743-141">The formats that are available on the Clipboard when strokes are copied are listed on the Format menu, and the user selects the format for copying the ink from this list.</span></span> <span data-ttu-id="b6743-142">可用格式的類型包括筆跡序列化格式 (ISF) 、中繼檔、增強的中繼檔和點陣圖。</span><span class="sxs-lookup"><span data-stu-id="b6743-142">The types of formats available include Ink Serialized Format (ISF), metafile, enhanced metafile, and bitmap.</span></span> <span data-ttu-id="b6743-143">草圖筆墨和文字筆墨格式互斥，而且會依賴將筆墨複製到剪貼簿作為 OLE 物件。</span><span class="sxs-lookup"><span data-stu-id="b6743-143">The sketch ink and text ink formats are mutually exclusive, and rely on the ink being copied to the clipboard as an OLE object.</span></span>

<span data-ttu-id="b6743-144">樣式功能表可讓使用者變更畫筆的色彩和寬度屬性，以及任何選取的筆劃。</span><span class="sxs-lookup"><span data-stu-id="b6743-144">The Style menu enables the user to change the color and width properties of the pen and any selected strokes.</span></span>

<span data-ttu-id="b6743-145">例如，紅色的命令會將筆墨收集器的[system.windows.controls.inkcanvas.defaultdrawingattributes](/previous-versions/ms571711(v=vs.100))屬性[色彩](/previous-versions/ms582103(v=vs.100))屬性設為紅色。</span><span class="sxs-lookup"><span data-stu-id="b6743-145">For example, the Red command sets the [Color](/previous-versions/ms582103(v=vs.100)) property of the ink collector's [DefaultDrawingAttributes](/previous-versions/ms571711(v=vs.100)) property to the color red.</span></span> <span data-ttu-id="b6743-146">因為資料[指標](/previous-versions/ms552104(v=vs.100))物件的[DrawingAttributes](/previous-versions/ms581965(v=vs.100))屬性尚未設定，所以繪製至筆墨收集器的任何新筆墨都會繼承至預設繪圖色彩。</span><span class="sxs-lookup"><span data-stu-id="b6743-146">Because the [DrawingAttributes](/previous-versions/ms581965(v=vs.100)) property of the [Cursor](/previous-versions/ms552104(v=vs.100)) object has not been set, any new ink drawn to the ink collector inherits to default drawing color.</span></span> <span data-ttu-id="b6743-147">此外，如果目前已選取任何筆劃，則也會更新每個筆劃的繪圖屬性色彩屬性。</span><span class="sxs-lookup"><span data-stu-id="b6743-147">Also, if any strokes are currently selected, each stroke's drawing attributes Color property is updated as well.</span></span>


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



## <a name="handling-mouse-events"></a><span data-ttu-id="b6743-148">處理滑鼠事件</span><span class="sxs-lookup"><span data-stu-id="b6743-148">Handling Mouse Events</span></span>

<span data-ttu-id="b6743-149">[MouseMove](/previous-versions/ms567617(v=vs.100))事件處理常式會檢查應用程式模式。</span><span class="sxs-lookup"><span data-stu-id="b6743-149">The [MouseMove](/previous-versions/ms567617(v=vs.100)) event handler checks the application mode.</span></span> <span data-ttu-id="b6743-150">如果模式為 MoveInk，而滑鼠按鍵已關閉，則處理常式會使用 [筆觸](/previous-versions/ms552701(v=vs.100)) 集合的 Move 方法來移動筆劃，並更新選取方塊。</span><span class="sxs-lookup"><span data-stu-id="b6743-150">If the mode is MoveInk and a mouse button is down, then the handler moves the strokes by using the [Strokes](/previous-versions/ms552701(v=vs.100)) collection's Move method and updates the selection box.</span></span> <span data-ttu-id="b6743-151">否則，處理常式會檢查以判斷選取範圍矩形是否包含游標、是否啟用筆跡收集，以及據以設定游標。</span><span class="sxs-lookup"><span data-stu-id="b6743-151">Otherwise, the handler checks to determine whether the selection rectangle contains the cursor, enables ink collection accordingly, and also sets the cursor accordingly.</span></span>

<span data-ttu-id="b6743-152">[MouseDown](/previous-versions/ms567616(v=vs.100))事件處理常式會檢查資料指標的設定。</span><span class="sxs-lookup"><span data-stu-id="b6743-152">The [MouseDown](/previous-versions/ms567616(v=vs.100)) event handler checks the cursor setting.</span></span> <span data-ttu-id="b6743-153">如果資料指標設定為 [SizeAll](/dotnet/api/system.windows.forms.cursors.sizeall?view=netcore-3.1)，則處理常式會將應用程式模式設定為 MoveInk，並記錄資料指標的位置。</span><span class="sxs-lookup"><span data-stu-id="b6743-153">If the cursor is set to [SizeAll](/dotnet/api/system.windows.forms.cursors.sizeall?view=netcore-3.1), then the handler sets the application mode to MoveInk and records the cursor location.</span></span> <span data-ttu-id="b6743-154">否則，如果有目前的選取範圍，請清除它。</span><span class="sxs-lookup"><span data-stu-id="b6743-154">Otherwise, if there is a current selection, clear it.</span></span>

<span data-ttu-id="b6743-155">[MouseUp](/previous-versions/ms567618(v=vs.100))事件處理常式會檢查應用程式模式。</span><span class="sxs-lookup"><span data-stu-id="b6743-155">The [MouseUp](/previous-versions/ms567618(v=vs.100)) event handler checks the application mode.</span></span> <span data-ttu-id="b6743-156">如果模式為 MoveInk，則處理常式會根據選取的命令核取狀態來設定應用程式模式。</span><span class="sxs-lookup"><span data-stu-id="b6743-156">If the mode is MoveInk, then the handler sets the application mode based on the Select command's checked state.</span></span>

<span data-ttu-id="b6743-157">當筆墨收集器收到新的封包資料時， [NewPackets](/previous-versions/ms567621(v=vs.100)) 事件會在選取模式中引發。</span><span class="sxs-lookup"><span data-stu-id="b6743-157">The [NewPackets](/previous-versions/ms567621(v=vs.100)) event is raised in selection mode when the ink collector receives new packet data.</span></span> <span data-ttu-id="b6743-158">如果應用程式處於選取模式，則必須攔截新的封包，並使用它們來繪製選取的套索。</span><span class="sxs-lookup"><span data-stu-id="b6743-158">If the application is in selection mode, it is necessary to intercept the new packets and use them to draw the selection lasso.</span></span>

<span data-ttu-id="b6743-159">每個封包的座標都會轉換成圖元（受限於繪圖區域），並加入至套索的點集合。</span><span class="sxs-lookup"><span data-stu-id="b6743-159">Each packet's coordinate is converted to pixels, constrained to the drawing area, and added to the lasso's collection of points.</span></span> <span data-ttu-id="b6743-160">接著會呼叫 helper 方法，以在表單上繪製套索。</span><span class="sxs-lookup"><span data-stu-id="b6743-160">A helper method is then called to draw the lasso on the form.</span></span>

## <a name="handling-a-new-stroke"></a><span data-ttu-id="b6743-161">處理新的筆劃</span><span class="sxs-lookup"><span data-stu-id="b6743-161">Handling a New Stroke</span></span>

<span data-ttu-id="b6743-162">繪製新的筆劃時，會在選取模式中引發 [筆劃](/previous-versions/ms567622(v=vs.100)) 事件。</span><span class="sxs-lookup"><span data-stu-id="b6743-162">The [Stroke](/previous-versions/ms567622(v=vs.100)) event is raised in the selection mode when a new stroke is drawn.</span></span> <span data-ttu-id="b6743-163">如果應用程式處於選取模式，此筆觸會對應至套索，而且必須更新所選筆劃的資訊。</span><span class="sxs-lookup"><span data-stu-id="b6743-163">If the application is in selection mode, this stroke corresponds to the lasso and it is necessary to update the selected strokes' information.</span></span>

<span data-ttu-id="b6743-164">處理常式會取消 [筆劃](/previous-versions/ms567622(v=vs.100)) 事件、檢查兩個以上的套索點、將點集合複製到 [Point](/dotnet/api/system.drawing.point?view=netcore-3.1) 物件陣列，並將陣列中點的座標從圖元轉換成筆墨空間。</span><span class="sxs-lookup"><span data-stu-id="b6743-164">The handler cancels the [Stroke](/previous-versions/ms567622(v=vs.100)) event, checks for more than two lasso points, copies the Points collection to an array of [Point](/dotnet/api/system.drawing.point?view=netcore-3.1) objects, and converts the coordinates of the points in the array from pixels to ink space.</span></span> <span data-ttu-id="b6743-165">然後，此處理程式會使用 [筆墨](/previous-versions/ms583670(v=vs.100)) 物件的 [system.windows.media.visualtreehelper.hittest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) 方法來取得套索點選取的筆觸，並更新表單的選取狀態。</span><span class="sxs-lookup"><span data-stu-id="b6743-165">Then, the handler uses the [Ink](/previous-versions/ms583670(v=vs.100)) object's [HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) method to get the strokes selected by the lasso points and updates the selection state of the form.</span></span> <span data-ttu-id="b6743-166">最後，引發事件的筆劃會從所選筆劃的集合中移除，而套索點集合會清空，而 helper 方法會繪製選取矩形。</span><span class="sxs-lookup"><span data-stu-id="b6743-166">Finally, the stroke that raised the event is removed from the collection of selected strokes, the lasso Points collection is emptied, and a helper method draws the selection rectangle.</span></span>


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



## <a name="copying-ink-to-the-clipboard"></a><span data-ttu-id="b6743-167">將筆墨複製到剪貼簿</span><span class="sxs-lookup"><span data-stu-id="b6743-167">Copying Ink to the Clipboard</span></span>

<span data-ttu-id="b6743-168">CopyInkToClipboard helper 方法會建立 [InkClipboardFormats](/previous-versions/ms583681(v=vs.100)) 值、檢查格式功能表的狀態，以更新要放在剪貼簿上的格式，並使用 [筆墨](/previous-versions/ms583670(v=vs.100)) 物件的 [ClipboardCopy](/previous-versions/dotnet/netframework-3.5/ms571316(v=vs.90)) 方法將筆觸複製到剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="b6743-168">The CopyInkToClipboard helper method creates an [InkClipboardFormats](/previous-versions/ms583681(v=vs.100)) value, checks the Format menu's state to update the formats to put on the clipboard, and uses the [Ink](/previous-versions/ms583670(v=vs.100)) object's [ClipboardCopy](/previous-versions/dotnet/netframework-3.5/ms571316(v=vs.90)) method to copy the strokes to the clipboard.</span></span>


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



## <a name="updating-a-selection"></a><span data-ttu-id="b6743-169">更新選取專案</span><span class="sxs-lookup"><span data-stu-id="b6743-169">Updating a Selection</span></span>

<span data-ttu-id="b6743-170">SetSelection helper 方法會更新 selectedStrokes 欄位，如果集合是 **Null** 或 **空白**，則選取矩形會設定為空的矩形。</span><span class="sxs-lookup"><span data-stu-id="b6743-170">The SetSelection helper method updates the selectedStrokes filed and if the collection is **NULL** or **EMPTY**, the selection rectangle is set to the empty rectangle.</span></span> <span data-ttu-id="b6743-171">如果選取的 [筆觸](/previous-versions/ms552701(v=vs.100)) 集合不是空的，SetSelection 方法會執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="b6743-171">If the selected [Strokes](/previous-versions/ms552701(v=vs.100)) collection is not empty the SetSelection method performs the following steps:</span></span>

-   <span data-ttu-id="b6743-172">使用筆劃集合的 [GetBoundingBox](/previous-versions/dotnet/netframework-3.5/ms571376(v=vs.90)) 方法來決定周框</span><span class="sxs-lookup"><span data-stu-id="b6743-172">Determines the bounding rectangle by using the [GetBoundingBox](/previous-versions/dotnet/netframework-3.5/ms571376(v=vs.90)) method of the strokes collection</span></span>
-   <span data-ttu-id="b6743-173">將矩形座標從筆墨空間轉換成圖元</span><span class="sxs-lookup"><span data-stu-id="b6743-173">Converts the rectangle coordinates from ink space to pixels</span></span>
-   <span data-ttu-id="b6743-174">擴大矩形，以提供其與所選筆劃之間的一些視覺空間</span><span class="sxs-lookup"><span data-stu-id="b6743-174">Inflates the rectangle to provide some visual space between it and the selected strokes</span></span>
-   <span data-ttu-id="b6743-175">建立目前選取方塊的選取控點</span><span class="sxs-lookup"><span data-stu-id="b6743-175">Creates selection handles for the current selection box</span></span>

<span data-ttu-id="b6743-176">最後，SetSelection 方法會設定選取控點的可見度，並將筆墨收集器的 [AutoRedraw](/previous-versions/ms571706(v=vs.100)) 屬性設定為 **FALSE**（如果已選取筆劃）。</span><span class="sxs-lookup"><span data-stu-id="b6743-176">Finally, the SetSelection method sets the visibility of the selection handles and sets the ink collector's [AutoRedraw](/previous-versions/ms571706(v=vs.100)) property to **FALSE**, if strokes are selected.</span></span>


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



## <a name="drawing-the-lasso"></a><span data-ttu-id="b6743-177">繪製套索</span><span class="sxs-lookup"><span data-stu-id="b6743-177">Drawing the Lasso</span></span>

<span data-ttu-id="b6743-178">套索會繪製成一系列的開放式點，這些點會沿著套索筆劃的路徑，以及兩端之間的虛線接點線。</span><span class="sxs-lookup"><span data-stu-id="b6743-178">The lasso is drawn as a series of open dots that follow the path of the lasso stroke and a dashed connector line between the two ends.</span></span> <span data-ttu-id="b6743-179">[NewPackets](/previous-versions/ms567621(v=vs.100))事件是在繪製套索時引發，而且事件處理常式會將筆劃資訊傳遞給 DrawLasso 方法。</span><span class="sxs-lookup"><span data-stu-id="b6743-179">The [NewPackets](/previous-versions/ms567621(v=vs.100)) event is raised as the lasso is being drawn, and the event handler passes the stroke information to the DrawLasso method.</span></span>

<span data-ttu-id="b6743-180">DrawLasso helper 方法會先移除舊的連接線，然後逐一查看筆劃中的點。</span><span class="sxs-lookup"><span data-stu-id="b6743-180">The DrawLasso helper method first removes the old connector line and then iterates over the points in the stroke.</span></span> <span data-ttu-id="b6743-181">然後，DrawLasso 會計算將點沿著筆劃放置的位置，然後繪製它們。</span><span class="sxs-lookup"><span data-stu-id="b6743-181">Then, DrawLasso calculates where to place the dots along the stroke and draws them.</span></span> <span data-ttu-id="b6743-182">最後，它會繪製新的連接線。</span><span class="sxs-lookup"><span data-stu-id="b6743-182">Finally, it draws a new connector line.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="b6743-183">關閉表單</span><span class="sxs-lookup"><span data-stu-id="b6743-183">Closing the Form</span></span>

<span data-ttu-id="b6743-184">表單的 [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) 方法會處置 [InkCollector](/previous-versions/ms583683(v=vs.100)) 物件 myInkCollector。</span><span class="sxs-lookup"><span data-stu-id="b6743-184">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms583683(v=vs.100)) object, myInkCollector.</span></span>

 

 
