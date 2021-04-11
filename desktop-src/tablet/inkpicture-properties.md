---
description: 此區段包含 InkPicture 控制項的屬性。
ms.assetid: d724c177-af57-4c99-94f2-c70904910b49
title: InkPicture 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ae8149098b34a70af5e088814e2a5258b0fa0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694992"
---
# <a name="inkpicture-properties"></a><span data-ttu-id="d3cc3-103">InkPicture 屬性</span><span class="sxs-lookup"><span data-stu-id="d3cc3-103">InkPicture Properties</span></span>

<span data-ttu-id="d3cc3-104">此區段包含 InkPicture 控制項的屬性。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-104">This section contains Properties for the InkPicture Control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d3cc3-105">屬性</span><span class="sxs-lookup"><span data-stu-id="d3cc3-105">Property</span></span></th>
<th><span data-ttu-id="d3cc3-106">描述</span><span class="sxs-lookup"><span data-stu-id="d3cc3-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d3cc3-107"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>AutoRedraw 屬性</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3cc3-107"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>AutoRedraw Property</strong></a></span></span></td>
<td><span data-ttu-id="d3cc3-108">取得或設定值，這個值會指定 <a href="inkpicture-control-reference.md">InkPicture</a> 控制項是否會在視窗失效時重新繪製 (是否會在與 InkPicture 相關聯的視窗收到) 的 WM_PAINT 訊息時，自動重新繪製目前與 InkPicture 控制項相關聯的 <a href="inkdisp-class.md"><strong>InkDisp</strong></a> 物件。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-108">Gets or sets a value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control repaints when the window is invalidated (whether the <a href="inkdisp-class.md"><strong>InkDisp</strong></a> object currently associated with InkPicture control is automatically redrawn when the window associated with the InkPicture receives a WM_PAINT message).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3cc3-109"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>顏色</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3cc3-109"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>BackColor</strong></a></span></span></td>
<td><span data-ttu-id="d3cc3-110">取得或設定 <a href="inkpicture-control-reference.md">InkPicture</a> 控制項的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-110">Gets or sets the background color for the <a href="inkpicture-control-reference.md">InkPicture</a> control.</span></span> <span data-ttu-id="d3cc3-111">預設的背景色彩是系統視窗背景色彩，通常是白色。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-111">The default background color is the system window background color, which is typically white.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3cc3-112"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>CollectingInk 屬性</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3cc3-112"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>CollectingInk Property</strong></a></span></span></td>
<td><span data-ttu-id="d3cc3-113">取得值，這個值會指定 <a href="inkpicture-control-reference.md">InkPicture</a> 控制項是否只 (執行時間) 收集筆跡。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-113">Gets the value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control is collecting ink (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3cc3-114"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>CollectionMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3cc3-114"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>CollectionMode</strong></a></span></span></td>
<td><span data-ttu-id="d3cc3-115">取得或設定收集模式，這個模式會決定是否要將筆墨、手勢或筆跡和手勢辨識為使用者寫入。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-115">Gets or sets the collection mode that determines whether ink, gestures, or ink and gestures are recognized as the user writes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3cc3-116"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Cursor 屬性</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3cc3-116"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Cursors Property</strong></a></span></span></td>
<td><span data-ttu-id="d3cc3-117">取得可在<a href="inkpicture-control-reference.md">InkPicture</a>控制項的筆墨區域中使用的<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>IInkCursors</strong></a>集合。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-117">Gets the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>IInkCursors</strong></a> collection available for use in the <a href="inkpicture-control-reference.md">InkPicture</a> control's inking region.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3cc3-118"><a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>CustomStrokes</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3cc3-118"><a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>CustomStrokes</strong></a></span></span></td>
<td><span data-ttu-id="d3cc3-119">取得要使用筆墨來保存的 <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>IInkCustomStrokes</strong></a> 集合 (設計階段) 。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-119">Gets the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>IInkCustomStrokes</strong></a> collection to be persisted with the ink (design-time only).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3cc3-120"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>System.windows.controls.inkcanvas.defaultdrawingattributes 屬性</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3cc3-120"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>DefaultDrawingAttributes Property</strong></a></span></span></td>
<td><span data-ttu-id="d3cc3-121">取得或設定預設的 <a href="inkdrawingattributes-class.md"><strong>InkDrawingAttributes</strong></a> 集合，以在只) 繪製和顯示筆墨 (執行時間時使用。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-121">Gets or sets the default <a href="inkdrawingattributes-class.md"><strong>InkDrawingAttributes</strong></a> collection to use when drawing and displaying ink (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3cc3-122"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>DesiredPacketDescription 屬性</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3cc3-122"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>DesiredPacketDescription Property</strong></a></span></span></td>
<td><span data-ttu-id="d3cc3-123">取得或設定 <a href="inkpicture-control-reference.md">InkPicture</a> 控制項的封包描述， (執行時間) 。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-123">Gets or sets the packet description of the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3cc3-124"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>DynamicRendering 屬性</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3cc3-124"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>DynamicRendering Property</strong></a></span></span></td>
<td><span data-ttu-id="d3cc3-125">取得或設定值，這個值會指定 <a href="inkpicture-control-reference.md">InkPicture</a> 控制項是否在收集時動態呈現筆墨。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-125">Gets or sets the value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control dynamically renders the ink as it is collected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3cc3-126"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>System.windows.controls.inkcanvas.editingmode</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3cc3-126"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>EditingMode</strong></a></span></span></td>
<td><span data-ttu-id="d3cc3-127">取得或設定值，這個值會指定 <a href="inkpicture-control-reference.md">InkPicture</a> 控制項是否處於筆墨模式、刪除模式或選取/編輯模式。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-127">Gets or sets a value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control is in ink mode, deletion mode, or selecting/editing mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3cc3-128"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>啟用</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3cc3-128"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>Enabled</strong></a></span></span></td>
<td><span data-ttu-id="d3cc3-129">取得或設定值，這個值會決定 <a href="inkpicture-control-reference.md">InkPicture</a> 控制項是否可以回應使用者產生的事件。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-129">Gets or sets a value that determines whether the <a href="inkpicture-control-reference.md">InkPicture</a> control can respond to user-generated events.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d3cc3-130">這個屬性就相當於 <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a> 屬性。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-130">This property is equivalent to the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a> property.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3cc3-131"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>EraserMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3cc3-131"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>EraserMode</strong></a></span></span></td>
<td><span data-ttu-id="d3cc3-132">取得或設定值，這個值會指定是否以筆劃或點抹除筆墨。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-132">Gets or sets the value that specifies whether ink is erased by stroke or by point.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3cc3-133"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>EraserWidth</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3cc3-133"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>EraserWidth</strong></a></span></span></td>
<td><span data-ttu-id="d3cc3-134">取得或設定值，這個值會指定橡皮擦畫筆提示的寬度。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-134">Gets or sets the value that specifies the width of the eraser pen tip.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3cc3-135"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>hWnd</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3cc3-135"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>hWnd</strong></a></span></span></td>
<td><span data-ttu-id="d3cc3-136">取得 <a href="inkpicture-control-reference.md">InkPicture</a> 控制項所系結的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-136">Gets the window handle to which the <a href="inkpicture-control-reference.md">InkPicture</a> control is bound.</span></span> <span data-ttu-id="d3cc3-137"> (僅限執行時間) </span><span class="sxs-lookup"><span data-stu-id="d3cc3-137">(run time only)</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3cc3-138"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>筆跡</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3cc3-138"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Ink</strong></a></span></span></td>
<td><span data-ttu-id="d3cc3-139">取得或設定與<a href="inkpicture-control-reference.md">InkPicture</a>控制項相關聯的<a href="inkdisp-class.md"><strong>InkDisp</strong></a>物件 (執行時間僅) 。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-139">Gets or sets the <a href="inkdisp-class.md"><strong>InkDisp</strong></a> object that is associated with the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3cc3-140"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3cc3-140"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a></span></span></td>
<td><span data-ttu-id="d3cc3-141">取得或設定值，這個值會指定 <a href="inkpicture-control-reference.md">InkPicture</a> 控制項是否會收集 (的輸入、範圍事件中的資料指標，以及) 中的畫筆輸入。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-141">Gets or sets a value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control collects pen input (in-air packets, cursor in range events, and so on).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3cc3-142"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>MarginX 屬性</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3cc3-142"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>MarginX Property</strong></a></span></span></td>
<td><span data-ttu-id="d3cc3-143">取得或設定以螢幕座標表示的視窗矩形周圍的 X 軸邊界。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-143">Gets or sets the x-axis margin around the window rectangle in screen coordinates.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3cc3-144"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>MarginY 屬性</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3cc3-144"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>MarginY Property</strong></a></span></span></td>
<td><span data-ttu-id="d3cc3-145">取得或設定以螢幕座標表示的視窗矩形周圍的 y 軸邊界。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-145">Gets or sets the y-axis margin around the window rectangle in screen coordinates.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3cc3-146"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>MouseIcon 屬性</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3cc3-146"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>MouseIcon Property</strong></a></span></span></td>
<td><span data-ttu-id="d3cc3-147">取得或設定目前的自訂滑鼠圖示。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-147">Gets or sets the current custom mouse icon.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3cc3-148"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>MousePointer 屬性</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3cc3-148"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>MousePointer Property</strong></a></span></span></td>
<td><span data-ttu-id="d3cc3-149">取得或設定值，這個值表示當滑鼠停留在 <a href="inkpicture-control-reference.md">InkPicture</a> 控制項的特定部分時，所顯示的滑鼠指標類型。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-149">Gets or sets a value that indicates the type of mouse pointer that appears when the mouse is over a particular part of the <a href="inkpicture-control-reference.md">InkPicture</a> control.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3cc3-150"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Picture</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3cc3-150"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Picture</strong></a></span></span></td>
<td><span data-ttu-id="d3cc3-151">取得要顯示在 <a href="inkpicture-control-reference.md">InkPicture</a> 控制項上的圖形檔案。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-151">Gets the graphics file to appear on the <a href="inkpicture-control-reference.md">InkPicture</a> control.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3cc3-152"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>轉譯器屬性</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3cc3-152"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Renderer Property</strong></a></span></span></td>
<td><span data-ttu-id="d3cc3-153">取得或設定 <a href="inkrenderer-class.md"><strong>InkRenderer</strong></a> 物件，這個物件是用來在 <a href="inkpicture-control-reference.md">InkPicture</a> 控制項上繪製筆墨 (只) 的執行時間。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-153">Gets or sets the <a href="inkrenderer-class.md"><strong>InkRenderer</strong></a> object that is used to draw ink on the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3cc3-154"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>選取</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3cc3-154"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Selection</strong></a></span></span></td>
<td><span data-ttu-id="d3cc3-155">取得目前在<a href="inkpicture-control-reference.md">InkPicture</a>控制項內選取的<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a>集合 (執行時間) 。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-155">Gets the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection currently selected inside the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3cc3-156"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>SizeMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3cc3-156"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>SizeMode</strong></a></span></span></td>
<td><span data-ttu-id="d3cc3-157">取得或設定控制項如何處理影像放置和調整大小。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-157">Gets or sets how the control handles image placement and sizing.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3cc3-158"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>SupportHighContrastInk 屬性</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3cc3-158"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>SupportHighContrastInk Property</strong></a></span></span></td>
<td><span data-ttu-id="d3cc3-159">取得值，這個值會指定當系統處於高對比模式時，是否只將筆墨轉譯為一種色彩，Color = COLOR_WINDOWTEXT (從 GetSystemMetrics 呼叫) 。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-159">Gets a value that specifies whether ink is rendered as just one color, Color = COLOR_WINDOWTEXT (from the GetSystemMetrics call) when the system is in High Contrast mode.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3cc3-160"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>SupportHighContrastSelectionUI</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3cc3-160"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>SupportHighContrastSelectionUI</strong></a></span></span></td>
<td><span data-ttu-id="d3cc3-161">取得或設定值，這個值會指定當系統處於高對比模式時，是否將所有選取範圍的使用者介面 (選取範圍方塊和選取控點) 會以高對比繪製。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-161">Gets or sets a value that specifies whether all selection user interfaces (selection bounding box and selection handles) are drawn in high contrast when the system is in High Contrast mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3cc3-162"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>平板電腦屬性</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3cc3-162"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>Tablet Property</strong></a></span></span></td>
<td><span data-ttu-id="d3cc3-163">取得<a href="inkpicture-control-reference.md">InkPicture</a>控制項目前用來收集輸入的<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>IInkTablet</strong></a>物件。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-163">Gets the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>IInkTablet</strong></a> object that the <a href="inkpicture-control-reference.md">InkPicture</a> control is currently using to collect input.</span></span><br/></td>
</tr>
</tbody>
</table>



 

