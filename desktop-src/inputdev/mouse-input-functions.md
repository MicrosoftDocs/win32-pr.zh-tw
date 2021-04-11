---
title: 滑鼠輸入功能
description: .
ms.assetid: a666b25b-a75c-4500-8077-fabe07589a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47437458cc8ad2bf85ecfa0d8676af8d26c67b89
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103684276"
---
# <a name="mouse-input-functions"></a><span data-ttu-id="b4800-103">滑鼠輸入功能</span><span class="sxs-lookup"><span data-stu-id="b4800-103">Mouse Input Functions</span></span>


## <a name="in-this-section"></a><span data-ttu-id="b4800-104">本節內容</span><span class="sxs-lookup"><span data-stu-id="b4800-104">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4800-105">主題</span><span class="sxs-lookup"><span data-stu-id="b4800-105">Topic</span></span></th>
<th><span data-ttu-id="b4800-106">描述</span><span class="sxs-lookup"><span data-stu-id="b4800-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b4800-107"><a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4800-107"><a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4800-108">當滑鼠指標離開視窗，或將滑鼠停留在視窗上一段指定的時間時張貼訊息。</span><span class="sxs-lookup"><span data-stu-id="b4800-108">Posts messages when the mouse pointer leaves a window or hovers over a window for a specified amount of time.</span></span> <span data-ttu-id="b4800-109">此函數會呼叫 <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> （如果存在），否則會模擬它。</span><span class="sxs-lookup"><span data-stu-id="b4800-109">This function calls <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> if it exists, otherwise it emulates it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4800-110"><a href="/windows/desktop/api/winuser/nf-winuser-dragdetect"><strong>DragDetect</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4800-110"><a href="/windows/desktop/api/winuser/nf-winuser-dragdetect"><strong>DragDetect</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4800-111">擷取滑鼠並追蹤其移動，直到使用者放開左側按鈕、按下 ESC 鍵，或將滑鼠移到指定點周圍的拖曳矩形外。</span><span class="sxs-lookup"><span data-stu-id="b4800-111">Captures the mouse and tracks its movement until the user releases the left button, presses the ESC key, or moves the mouse outside the drag rectangle around the specified point.</span></span> <span data-ttu-id="b4800-112">拖曳矩形的寬度和高度是由<a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics"><strong>GetSystemMetrics</strong></a>函數所傳回的<strong>SM_CXDRAG</strong>和<strong>SM_CYDRAG</strong>值所指定。</span><span class="sxs-lookup"><span data-stu-id="b4800-112">The width and height of the drag rectangle are specified by the <strong>SM_CXDRAG</strong> and <strong>SM_CYDRAG</strong> values returned by the <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics"><strong>GetSystemMetrics</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4800-113"><a href="/windows/desktop/api/winuser/nf-winuser-getcapture"><strong>GetCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4800-113"><a href="/windows/desktop/api/winuser/nf-winuser-getcapture"><strong>GetCapture</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4800-114">抓取視窗的控制碼 (是否有任何) 已捕捉到滑鼠。</span><span class="sxs-lookup"><span data-stu-id="b4800-114">Retrieves a handle to the window (if any) that has captured the mouse.</span></span> <span data-ttu-id="b4800-115">一次只能有一個視窗可捕獲滑鼠;無論游標是否在其框線內，此視窗都會收到滑鼠輸入。</span><span class="sxs-lookup"><span data-stu-id="b4800-115">Only one window at a time can capture the mouse; this window receives mouse input whether or not the cursor is within its borders.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4800-116"><a href="/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime"><strong>GetDoubleClickTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4800-116"><a href="/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime"><strong>GetDoubleClickTime</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4800-117">抓取滑鼠目前的按兩下時間。</span><span class="sxs-lookup"><span data-stu-id="b4800-117">Retrieves the current double-click time for the mouse.</span></span> <span data-ttu-id="b4800-118">按兩下是按兩下滑鼠按鍵的一連串，第二個是在指定的時間內發生第二個點。</span><span class="sxs-lookup"><span data-stu-id="b4800-118">A double-click is a series of two clicks of the mouse button, the second occurring within a specified time after the first.</span></span> <span data-ttu-id="b4800-119">按兩下時間是在按兩下的第一次和第二次按一下時，可能發生的最大毫秒數。</span><span class="sxs-lookup"><span data-stu-id="b4800-119">The double-click time is the maximum number of milliseconds that may occur between the first and second click of a double-click.</span></span> <span data-ttu-id="b4800-120">最大的按兩下時間是5000毫秒。</span><span class="sxs-lookup"><span data-stu-id="b4800-120">The maximum double-click time is 5000 milliseconds.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4800-121"><a href="/windows/desktop/api/winuser/nf-winuser-getmousemovepointsex"><strong>GetMouseMovePointsEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4800-121"><a href="/windows/desktop/api/winuser/nf-winuser-getmousemovepointsex"><strong>GetMouseMovePointsEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4800-122">抓取滑鼠或畫筆之前最多64個座標的歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="b4800-122">Retrieves a history of up to 64 previous coordinates of the mouse or pen.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4800-123"><a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4800-123"><a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4800-124"><a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>Mouse_event</strong></a>函式會會合成滑鼠動作並按一下按鈕。</span><span class="sxs-lookup"><span data-stu-id="b4800-124">The <a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a> function synthesizes mouse motion and button clicks.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b4800-125">此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="b4800-125">This function has been superseded.</span></span> <span data-ttu-id="b4800-126">請改用 <a href="/windows/desktop/api/winuser/nf-winuser-sendinput"><strong>SendInput</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="b4800-126">Use <a href="/windows/desktop/api/winuser/nf-winuser-sendinput"><strong>SendInput</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4800-127"><a href="/windows/desktop/api/winuser/nf-winuser-releasecapture"><strong>ReleaseCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4800-127"><a href="/windows/desktop/api/winuser/nf-winuser-releasecapture"><strong>ReleaseCapture</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4800-128">從目前線程中的視窗釋放滑鼠捕捉，並還原一般滑鼠輸入處理。</span><span class="sxs-lookup"><span data-stu-id="b4800-128">Releases the mouse capture from a window in the current thread and restores normal mouse input processing.</span></span> <span data-ttu-id="b4800-129">不論游標的位置為何，已捕捉到滑鼠的視窗都會收到所有的滑鼠輸入，但在游標作用點位於另一個執行緒的視窗中，但在按下滑鼠按鍵時除外。</span><span class="sxs-lookup"><span data-stu-id="b4800-129">A window that has captured the mouse receives all mouse input, regardless of the position of the cursor, except when a mouse button is clicked while the cursor hot spot is in the window of another thread.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4800-130"><a href="/windows/desktop/api/winuser/nf-winuser-setcapture"><strong>SetCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4800-130"><a href="/windows/desktop/api/winuser/nf-winuser-setcapture"><strong>SetCapture</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4800-131">將滑鼠捕捉設定為屬於目前線程的指定視窗。</span><span class="sxs-lookup"><span data-stu-id="b4800-131">Sets the mouse capture to the specified window belonging to the current thread.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4800-132"><a href="/windows/desktop/api/winuser/nf-winuser-setdoubleclicktime"><strong>SetDoubleClickTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4800-132"><a href="/windows/desktop/api/winuser/nf-winuser-setdoubleclicktime"><strong>SetDoubleClickTime</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4800-133">設定滑鼠的按兩下時間。</span><span class="sxs-lookup"><span data-stu-id="b4800-133">Sets the double-click time for the mouse.</span></span> <span data-ttu-id="b4800-134">按兩下是按兩下滑鼠按鍵的一連串，第二個是在指定的時間內發生第二個點。</span><span class="sxs-lookup"><span data-stu-id="b4800-134">A double-click is a series of two clicks of a mouse button, the second occurring within a specified time after the first.</span></span> <span data-ttu-id="b4800-135">按兩下時間是在按兩下的第一個和第二個點之間可能發生的最大毫秒數。</span><span class="sxs-lookup"><span data-stu-id="b4800-135">The double-click time is the maximum number of milliseconds that may occur between the first and second clicks of a double-click.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4800-136"><a href="/windows/desktop/api/winuser/nf-winuser-swapmousebutton"><strong>SwapMouseButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4800-136"><a href="/windows/desktop/api/winuser/nf-winuser-swapmousebutton"><strong>SwapMouseButton</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4800-137">反轉或還原左右滑鼠按鍵的意義。</span><span class="sxs-lookup"><span data-stu-id="b4800-137">Reverses or restores the meaning of the left and right mouse buttons.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4800-138"><a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4800-138"><a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4800-139">當滑鼠指標離開視窗，或將滑鼠停留在視窗上一段指定的時間時張貼訊息。</span><span class="sxs-lookup"><span data-stu-id="b4800-139">Posts messages when the mouse pointer leaves a window or hovers over a window for a specified amount of time.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b4800-140"><a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a>函式會呼叫<a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> （如果存在），否則<strong>_TrackMouseEvent</strong>模擬<strong>TrackMouseEvent</strong>。</span><span class="sxs-lookup"><span data-stu-id="b4800-140">The <a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a> function calls <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> if it exists, otherwise <strong>_TrackMouseEvent</strong> emulates <strong>TrackMouseEvent</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

