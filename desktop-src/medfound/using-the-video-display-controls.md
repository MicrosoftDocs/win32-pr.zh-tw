---
description: 使用影片顯示控制項
ms.assetid: 09501d67-effb-41ce-a7b7-d2415acdf3ac
title: 使用影片顯示控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbb9c83485faebc873b3e92502122c5497b4bb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691591"
---
# <a name="using-the-video-display-controls"></a><span data-ttu-id="c6041-103">使用影片顯示控制項</span><span class="sxs-lookup"><span data-stu-id="c6041-103">Using the Video Display Controls</span></span>

<span data-ttu-id="c6041-104">[**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)介面可控制增強型影片轉譯器 (EVR) 在應用程式視窗內顯示影片。</span><span class="sxs-lookup"><span data-stu-id="c6041-104">The [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface controls how the enhanced video renderer (EVR) displays video inside an application window.</span></span> <span data-ttu-id="c6041-105">此介面可用於 DirectShow 或媒體基礎。</span><span class="sxs-lookup"><span data-stu-id="c6041-105">This interface can be used in either DirectShow or Media Foundation.</span></span> <span data-ttu-id="c6041-106">就內部而言，影片顯示控制項是由 EVR 的預設展示者所提供。</span><span class="sxs-lookup"><span data-stu-id="c6041-106">Internally, the video display controls are provided by the EVR's default presenter.</span></span> <span data-ttu-id="c6041-107">如果您撰寫自訂的簡報者，就可以提供相同的介面或定義自訂介面。</span><span class="sxs-lookup"><span data-stu-id="c6041-107">If you write a custom presenter, you can provide the same interface or define a custom interface.</span></span>

<span data-ttu-id="c6041-108">取得 [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) 介面指標的正確方式，取決於您使用的是 EVR 的 DirectShow 版本或媒體基礎版本。</span><span class="sxs-lookup"><span data-stu-id="c6041-108">The correct way to get a pointer to the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface depends on whether you are using the DirectShow version of the EVR or the Media Foundation version.</span></span> <span data-ttu-id="c6041-109">針對媒體基礎 EVR，它也取決於您是直接使用 EVR，還是透過媒體會話使用它， (這是較常見的) 。</span><span class="sxs-lookup"><span data-stu-id="c6041-109">For the Media Foundation EVR, it also depends on whether you are using the EVR directly or using it through the Media Session (which is more typical).</span></span>

<span data-ttu-id="c6041-110">若要取得 [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) 介面的指標，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="c6041-110">To get a pointer to the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface, do the following:</span></span>

1.  <span data-ttu-id="c6041-111">取得 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c6041-111">Get a pointer to the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>

    -   <span data-ttu-id="c6041-112">如果您使用的是 DirectShow EVR 篩選器，請在篩選器上呼叫 **QueryInterface** 。</span><span class="sxs-lookup"><span data-stu-id="c6041-112">If you are using the DirectShow EVR filter, call **QueryInterface** on the filter.</span></span>

    -   <span data-ttu-id="c6041-113">如果您直接使用 EVR 媒體接收，請在媒體接收器上呼叫 **QueryInterface** 。</span><span class="sxs-lookup"><span data-stu-id="c6041-113">If you are using the EVR media sink directly, call **QueryInterface** on the media sink.</span></span>

    -   <span data-ttu-id="c6041-114">如果您使用媒體會話，請呼叫媒體會話上的 **QueryInterface** 。</span><span class="sxs-lookup"><span data-stu-id="c6041-114">If you are using the Media Session, call **QueryInterface** on the Media Session.</span></span>

2.  <span data-ttu-id="c6041-115">如果您使用媒體會話，請等候媒體會話傳送 [MESessionTopologyStatus](mesessiontopologystatus.md) 事件，其狀態值為 [已就緒的 MF TOPOSTATUS] \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="c6041-115">If you are using the Media Session, wait for the Media Session to send the [MESessionTopologyStatus](mesessiontopologystatus.md) event with a status value of MF\_TOPOSTATUS\_READY.</span></span> <span data-ttu-id="c6041-116"> (略過此步驟，否則請 ) </span><span class="sxs-lookup"><span data-stu-id="c6041-116">(Skip this step otherwise.)</span></span>

3.  <span data-ttu-id="c6041-117">呼叫 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 來取得 [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) 介面。</span><span class="sxs-lookup"><span data-stu-id="c6041-117">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface.</span></span> <span data-ttu-id="c6041-118">服務識別碼是 MR \_ 影片轉譯 \_ \_ 服務。</span><span class="sxs-lookup"><span data-stu-id="c6041-118">The service identifier is MR\_VIDEO\_RENDER\_SERVICE.</span></span>

<span data-ttu-id="c6041-119">您可以使用 [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) 介面來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="c6041-119">You can use the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface to perform the following tasks:</span></span>

-   <span data-ttu-id="c6041-120">設定裁剪視窗。</span><span class="sxs-lookup"><span data-stu-id="c6041-120">Set the clipping window.</span></span>

-   <span data-ttu-id="c6041-121">設定來源和目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="c6041-121">Set the source and destination rectangles.</span></span>

-   <span data-ttu-id="c6041-122">更新影片視窗以回應視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="c6041-122">Update the video window in response to window messages.</span></span>

-   <span data-ttu-id="c6041-123">啟用或停用全螢幕模式。</span><span class="sxs-lookup"><span data-stu-id="c6041-123">Enable or disable full-screen mode.</span></span>

## <a name="clipping-window"></a><span data-ttu-id="c6041-124">裁剪視窗</span><span class="sxs-lookup"><span data-stu-id="c6041-124">Clipping Window</span></span>

<span data-ttu-id="c6041-125">應用程式必須提供 EVR 繪製影片的視窗。</span><span class="sxs-lookup"><span data-stu-id="c6041-125">The application must provide a window where the EVR draws the video.</span></span> <span data-ttu-id="c6041-126">若要設定裁剪視窗，請以應用程式視窗的控制碼呼叫 [**IMFVideoDisplayControl：： SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) 。</span><span class="sxs-lookup"><span data-stu-id="c6041-126">To set the clipping window, call [**IMFVideoDisplayControl::SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) with a handle to the application window.</span></span>

<span data-ttu-id="c6041-127">如果您透過其啟用物件建立 EVR 媒體接收，則不需要執行此步驟。</span><span class="sxs-lookup"><span data-stu-id="c6041-127">If you create the EVR media sink through its activation object, this step is not required.</span></span> <span data-ttu-id="c6041-128">啟用物件會使用您在 [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate)函數中提供的視窗控制碼，自動呼叫 [**SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow)。</span><span class="sxs-lookup"><span data-stu-id="c6041-128">The activation object automatically calls [**SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow), using the window handle that you provided in the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function.</span></span>

## <a name="source-and-destination-rectangles"></a><span data-ttu-id="c6041-129">來源和目的地矩形</span><span class="sxs-lookup"><span data-stu-id="c6041-129">Source and Destination Rectangles</span></span>

<span data-ttu-id="c6041-130">在播放期間，展示者會取得局部影片影像的一部分，並將其繪製至影片視窗的區域。</span><span class="sxs-lookup"><span data-stu-id="c6041-130">During playback, the presenter takes a portion of the composited video image and draws it onto an area of the video window.</span></span> <span data-ttu-id="c6041-131">複合影像的部分是 *來源矩形*，而影片視窗的區域是 *目的地矩形*。</span><span class="sxs-lookup"><span data-stu-id="c6041-131">The portion of the composited image is the *source rectangle*, and the area of the video window is the *destination rectangle*.</span></span>

<span data-ttu-id="c6041-132">來源矩形是使用標準化座標定義的，其中 point (0.0、0.0) 對應至影片的左上角，而 (1.0，1.0) 對應到影片的右下角。</span><span class="sxs-lookup"><span data-stu-id="c6041-132">The source rectangle is defined using normalized coordinates where the point (0.0, 0.0) corresponds to the upper left corner of the video, and (1.0, 1.0) corresponds to the lower right corner of the video.</span></span> <span data-ttu-id="c6041-133">來源矩形可以是此矩形內的任何區域。</span><span class="sxs-lookup"><span data-stu-id="c6041-133">The source rectangle can be any region within this rectangle.</span></span> <span data-ttu-id="c6041-134">相對於視窗的工作區，目的矩形會以圖元為單位來指定。</span><span class="sxs-lookup"><span data-stu-id="c6041-134">The destination rectangle is specified in pixels, relative to the client area of the window.</span></span> <span data-ttu-id="c6041-135">預設的來源矩形是整個影像，而預設的目的地矩形是空的矩形。</span><span class="sxs-lookup"><span data-stu-id="c6041-135">The default source rectangle is the entire image, and the default destination rectangle is an empty rectangle.</span></span>

<span data-ttu-id="c6041-136">若要設定來源和目的地矩形，請呼叫 [**IMFVideoDisplayControl：： SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition)。</span><span class="sxs-lookup"><span data-stu-id="c6041-136">To set the source and destination rectangles, call [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>

<span data-ttu-id="c6041-137">如果您透過其啟用物件建立 EVR 媒體接收，則不需要執行此步驟。</span><span class="sxs-lookup"><span data-stu-id="c6041-137">If you create the EVR media sink through its activation object, this step is not required.</span></span> <span data-ttu-id="c6041-138">啟用物件會自動將目的地矩形設定為等於視窗的整個工作區。</span><span class="sxs-lookup"><span data-stu-id="c6041-138">The activation object automatically sets the destination rectangle equal to the entire client area of the window.</span></span> <span data-ttu-id="c6041-139">但是，如果您想要變更來源矩形或設定不同的目的地矩形，您應該呼叫 [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) 。</span><span class="sxs-lookup"><span data-stu-id="c6041-139">However, you should call [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) if you want to change the source rectangle or set a different destination rectangle.</span></span>

## <a name="window-messages"></a><span data-ttu-id="c6041-140">視窗訊息</span><span class="sxs-lookup"><span data-stu-id="c6041-140">Window Messages</span></span>

<span data-ttu-id="c6041-141">在播放期間，您的應用程式應該回應特定的視窗訊息，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c6041-141">During playback, your application should respond to certain window messages, as follows:</span></span>

-   <span data-ttu-id="c6041-142">WM \_ 油漆：呼叫 [**IMFVideoDisplayControl：： RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) 來重新繪製影片。</span><span class="sxs-lookup"><span data-stu-id="c6041-142">WM\_PAINT: Call [**IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) to repaint the video.</span></span> <span data-ttu-id="c6041-143">此外，請避免在播放影片時，在目的地矩形上進行繪製，因為這可能會導致閃爍。</span><span class="sxs-lookup"><span data-stu-id="c6041-143">Also, avoid painting over the destination rectangle while video is playing, because this can cause flickering.</span></span>

-   <span data-ttu-id="c6041-144">WM \_ 大小：您可能需要呼叫 [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) 來調整目的地矩形的大小。</span><span class="sxs-lookup"><span data-stu-id="c6041-144">WM\_SIZE: You might need to call [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) to resize the destination rectangle.</span></span>

<span data-ttu-id="c6041-145">不同于視頻混合轉譯器 (VMR 中) 篩選器，當您收到 WM DISPLAYCHANGE 訊息時，不需要通知 EVR \_ 。</span><span class="sxs-lookup"><span data-stu-id="c6041-145">Unlike the Video Mixing Renderer (VMR) filter in DirectShow, you do not have to notify the EVR when you receive a WM\_DISPLAYCHANGE message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6041-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="c6041-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6041-147">增強的影片轉譯器</span><span class="sxs-lookup"><span data-stu-id="c6041-147">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> </dl>

 

 



