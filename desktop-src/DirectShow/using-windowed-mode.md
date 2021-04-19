---
description: 使用視窗模式
ms.assetid: 09ee4568-348b-4cf9-bb38-dada291cdef9
title: 使用視窗模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95309f5546ce4f00a8dde029390b2edf48544f1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987665"
---
# <a name="using-windowed-mode"></a><span data-ttu-id="94133-103">使用視窗模式</span><span class="sxs-lookup"><span data-stu-id="94133-103">Using Windowed Mode</span></span>

> [!Note]  
> <span data-ttu-id="94133-104">舊版 [影片轉譯器篩選準則](video-renderer-filter.md) 一律使用視窗模式。</span><span class="sxs-lookup"><span data-stu-id="94133-104">The legacy [Video Renderer Filter](video-renderer-filter.md) always uses windowed mode.</span></span> <span data-ttu-id="94133-105">VMR-7 和 VMR-9 篩選器預設會使用視窗型模式，但也支援無視窗模式。</span><span class="sxs-lookup"><span data-stu-id="94133-105">The VMR-7 and VMR-9 filters use windowed mode by default, but also support windowless mode.</span></span>

 

<span data-ttu-id="94133-106">在視窗模式中，影片轉譯器會建立自己的視窗，以繪製影片畫面。</span><span class="sxs-lookup"><span data-stu-id="94133-106">In windowed mode, the video renderer creates its own window where it paints the video frames.</span></span> <span data-ttu-id="94133-107">除非您另外指定，否則這個視窗會是具有自己的框線和標題列的最上層視窗。</span><span class="sxs-lookup"><span data-stu-id="94133-107">Unless you specify otherwise, this window is a top-level window with its own borders and title bar.</span></span> <span data-ttu-id="94133-108">不過大部分的時候，您會將影片視窗附加至應用程式視窗，讓影片整合到您的應用程式 UI 中。</span><span class="sxs-lookup"><span data-stu-id="94133-108">Most of the time, however, you will attach the video window to an application window, so that the video is integrated into your application UI.</span></span> <span data-ttu-id="94133-109">此時，您需要進行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="94133-109">This requires the following steps:</span></span>

1.  <span data-ttu-id="94133-110">**IVideoWindow** 的查詢。</span><span class="sxs-lookup"><span data-stu-id="94133-110">Query for **IVideoWindow**.</span></span>
2.  <span data-ttu-id="94133-111">設定父視窗。</span><span class="sxs-lookup"><span data-stu-id="94133-111">Set the parent window.</span></span>
3.  <span data-ttu-id="94133-112">設定新的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="94133-112">Set new window styles.</span></span>
4.  <span data-ttu-id="94133-113">將影片視窗置於擁有者視窗內。</span><span class="sxs-lookup"><span data-stu-id="94133-113">Position the video window inside the owner window.</span></span>
5.  <span data-ttu-id="94133-114">通知 WM 移動訊息的影片視窗 \_ 。</span><span class="sxs-lookup"><span data-stu-id="94133-114">Notify the video window of WM\_MOVE messages.</span></span>

<span data-ttu-id="94133-115">**IVideoWindow 的查詢**</span><span class="sxs-lookup"><span data-stu-id="94133-115">**Query for IVideoWindow**</span></span>

<span data-ttu-id="94133-116">開始播放之前，請查詢 **IVideoWindow** 介面的篩選圖形管理員：</span><span class="sxs-lookup"><span data-stu-id="94133-116">Before starting playback, query the Filter Graph Manager for the **IVideoWindow** interface:</span></span>


```C++
IVideoWindow *pVidWin = NULL;
pGraph->QueryInterface(IID_IVideoWindow, (void **)&pVidWin);
```



<span data-ttu-id="94133-117">**設定父視窗**</span><span class="sxs-lookup"><span data-stu-id="94133-117">**Set the Parent Window**</span></span>

<span data-ttu-id="94133-118">若要設定父視窗，請使用應用程式視窗的控制碼來呼叫 [**IVideoWindow：:p \_**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) 的使用者的擁有者方法。</span><span class="sxs-lookup"><span data-stu-id="94133-118">To set the parent window, call the [**IVideoWindow::put\_Owner**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) method with a handle to your application window.</span></span> <span data-ttu-id="94133-119">這個方法會接受 [**OAHWND**](oahwnd.md)型別的變數，所以請將控制碼轉換成這個型別：</span><span class="sxs-lookup"><span data-stu-id="94133-119">This method takes a variable of type [**OAHWND**](oahwnd.md), so cast the handle to this type:</span></span>


```C++
pVidWin->put_Owner((OAHWND)hwnd);
```



<span data-ttu-id="94133-120">**設定新的視窗樣式**</span><span class="sxs-lookup"><span data-stu-id="94133-120">**Set New Window Styles**</span></span>

<span data-ttu-id="94133-121">藉由呼叫 [**IVideoWindow：:p \_ system.windows.window.windowstyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) 方法來變更影片視窗的樣式：</span><span class="sxs-lookup"><span data-stu-id="94133-121">Change the style of the video window by calling the [**IVideoWindow::put\_WindowStyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) method:</span></span>


```C++
pVidWin->put_WindowStyle(WS_CHILD | WS_CLIPSIBLINGS);
```



<span data-ttu-id="94133-122">WS \_ 子旗標會將視窗設定為子視窗，而 ws \_ CLIPSIBLINGS 旗標會防止視窗繪製在另一個子視窗的工作區中。</span><span class="sxs-lookup"><span data-stu-id="94133-122">The WS\_CHILD flag sets the window to be a child window, and the WS\_CLIPSIBLINGS flag prevents the window from drawing inside the client area of another child window.</span></span>

<span data-ttu-id="94133-123">**放置影片視窗**</span><span class="sxs-lookup"><span data-stu-id="94133-123">**Position the Video Window**</span></span>

<span data-ttu-id="94133-124">若要設定影片相對於應用程式視窗的工作區的位置，請呼叫 [**IVideoWindow：： SetWindowPosition**](/windows/desktop/api/Control/nf-control-ivideowindow-setwindowposition) 方法。</span><span class="sxs-lookup"><span data-stu-id="94133-124">To set the position of the video relative to the application window's client area, call the [**IVideoWindow::SetWindowPosition**](/windows/desktop/api/Control/nf-control-ivideowindow-setwindowposition) method.</span></span> <span data-ttu-id="94133-125">這個方法會使用矩形來指定影片視窗的左邊緣、上邊緣、寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="94133-125">This method takes a rectangle that specifies the left edge, top edge, width, and height of the video window.</span></span> <span data-ttu-id="94133-126">例如，下列程式碼會將影片視窗伸展，以符合父視窗的整個工作區：</span><span class="sxs-lookup"><span data-stu-id="94133-126">For example, the following code stretches the video window to fit the entire client area of the parent window:</span></span>


```C++
RECT rc;
GetClientRect(hwnd, &rc);
pVidWin->SetWindowPosition(0, 0, rc.right, rc.bottom);
```



<span data-ttu-id="94133-127">若要取得影片的原生大小，請在篩選圖形管理員上呼叫 [**IBasicVideo：： GetVideoSize**](/windows/desktop/api/Control/nf-control-ibasicvideo-getvideosize) 方法。</span><span class="sxs-lookup"><span data-stu-id="94133-127">To get the native size of the video, call the [**IBasicVideo::GetVideoSize**](/windows/desktop/api/Control/nf-control-ibasicvideo-getvideosize) method on the Filter Graph Manager.</span></span> <span data-ttu-id="94133-128">您可以使用該資訊來調整影片，並保持正確的外觀比例。</span><span class="sxs-lookup"><span data-stu-id="94133-128">You can use that information to scale the video and keep the correct aspect ratio.</span></span>

<span data-ttu-id="94133-129">**回應 WM \_ 移動訊息**</span><span class="sxs-lookup"><span data-stu-id="94133-129">**Respond to WM\_MOVE Messages**</span></span>

<span data-ttu-id="94133-130">為了達到最佳效能，您應該在圖形暫停時，每次視窗移動時通知影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="94133-130">For best performance, you should notify the video renderer whenever the window moves while the graph is paused.</span></span> <span data-ttu-id="94133-131">呼叫 [**IVideoWindow：： NotifyOwnerMessage**](/windows/desktop/api/Control/nf-control-ivideowindow-notifyownermessage) 方法以轉送 WM \_ 移動訊息：</span><span class="sxs-lookup"><span data-stu-id="94133-131">Call the [**IVideoWindow::NotifyOwnerMessage**](/windows/desktop/api/Control/nf-control-ivideowindow-notifyownermessage) method to forward the WM\_MOVE message:</span></span>


```C++
// (Inside your WindowProc)
case WM_MOVE:
    pVidWin->NotifyOwnerMessage((OAHWND)hWnd, msg, wParam, lParam);
    break;
```



<span data-ttu-id="94133-132">如果轉譯器使用硬體重迭，此通知會導致轉譯器更新覆迭位置。</span><span class="sxs-lookup"><span data-stu-id="94133-132">If the renderer is using a hardware overlay, this notification causes the renderer to update the overlay position.</span></span> <span data-ttu-id="94133-133"> (VMR-9 不會使用覆迭，所以如果您使用 VMR-9，就不需要呼叫這個方法。 ) </span><span class="sxs-lookup"><span data-stu-id="94133-133">(The VMR-9 does not use overlays, so you do not need to call this method if you are using the VMR-9.)</span></span>

<span data-ttu-id="94133-134">**清除**</span><span class="sxs-lookup"><span data-stu-id="94133-134">**Clean Up**</span></span>

<span data-ttu-id="94133-135">在應用程式結束之前，停止圖形並將影片視窗的擁有者重設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="94133-135">Before the application exits, stop the graph and reset the video window's owner to **NULL**.</span></span> <span data-ttu-id="94133-136">否則，可能會將視窗訊息傳送至錯誤的視窗，而這可能會造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="94133-136">Otherwise, window messages might be sent to the wrong window, which is likely to cause errors.</span></span> <span data-ttu-id="94133-137">此外，隱藏影片視窗，否則您可能會在螢幕上立即看到影片影像閃爍：</span><span class="sxs-lookup"><span data-stu-id="94133-137">Also, hide video window, or else you might see a video image flicker on the screen momentarily:</span></span>


```C++
pControl->Stop(); 
pVidWin->put_Visible(OAFALSE);
pVidWin->put_Owner(NULL);  
```



> [!Note]  
> <span data-ttu-id="94133-138">如果影片視窗的父系是主應用程式視窗的子系 (換句話說，如果影片視窗是子) 的子系，您應該使用 **CoCreateInstance** 建立影片視窗並將它新增至圖形，而不是讓篩選圖形管理員在 [智慧型連接](intelligent-connect.md)期間新增影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="94133-138">If the parent of the video window is a child of your main application window (in other words, if the video window is a child of a child), you should create the video window using **CoCreateInstance** and add it to the graph, instead of letting the Filter Graph Manager add the video renderer during [Intelligent Connect](intelligent-connect.md).</span></span> <span data-ttu-id="94133-139">這可確保同時重新繪製影片視窗和子視窗。</span><span class="sxs-lookup"><span data-stu-id="94133-139">This ensures that the video window and your child window are repainted at the same time.</span></span> <span data-ttu-id="94133-140">否則，子視窗可能會在影片視窗中繪製。</span><span class="sxs-lookup"><span data-stu-id="94133-140">Otherwise, the child window may paint over the video window.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="94133-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="94133-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94133-142">影片轉譯</span><span class="sxs-lookup"><span data-stu-id="94133-142">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 



