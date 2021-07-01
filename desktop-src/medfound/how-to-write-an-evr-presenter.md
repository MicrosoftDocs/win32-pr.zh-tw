---
description: 本文說明如何撰寫增強型影片轉譯器的自訂展示者 (EVR) 。
ms.assetid: 1135b309-b158-4b70-9f76-5c93d0ad3250
title: 如何撰寫 EVR 展示者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505ba7ec225ac5f1316ad4343a4e1058ff0b6cb8
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118773"
---
# <a name="how-to-write-an-evr-presenter"></a><span data-ttu-id="d94d8-103">如何撰寫 EVR 展示者</span><span class="sxs-lookup"><span data-stu-id="d94d8-103">How to Write an EVR Presenter</span></span>

<span data-ttu-id="d94d8-104">本文說明如何撰寫增強型影片轉譯器的自訂展示者 (EVR) 。</span><span class="sxs-lookup"><span data-stu-id="d94d8-104">This article describes how to write a custom presenter for the enhanced video renderer (EVR).</span></span> <span data-ttu-id="d94d8-105">自訂的簡報者可以與 DirectShow 和媒體基礎搭配使用;這兩種技術的介面和物件模型都相同，雖然作業的確切順序可能不同。</span><span class="sxs-lookup"><span data-stu-id="d94d8-105">A custom presenter can be used with both DirectShow and Media Foundation; the interfaces and object model are the same for both technologies, although the exact sequence of operations might vary.</span></span>

<span data-ttu-id="d94d8-106">本主題中的範例程式碼是從 Windows SDK 中提供的 [EVRPresenter 範例](evrpresenter-sample.md)來調整。</span><span class="sxs-lookup"><span data-stu-id="d94d8-106">The example code in this topic is adapted from the [EVRPresenter Sample](evrpresenter-sample.md), which is provided in the Windows SDK.</span></span>

<span data-ttu-id="d94d8-107">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="d94d8-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="d94d8-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="d94d8-108">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="d94d8-109">展示者物件模型</span><span class="sxs-lookup"><span data-stu-id="d94d8-109">Presenter Object Model</span></span>](#presenter-object-model)
    -   [<span data-ttu-id="d94d8-110">EVR 內的資料流程</span><span class="sxs-lookup"><span data-stu-id="d94d8-110">Data Flow Inside the EVR</span></span>](#data-flow-inside-the-evr)
    -   [<span data-ttu-id="d94d8-111">展示者狀態</span><span class="sxs-lookup"><span data-stu-id="d94d8-111">Presenter States</span></span>](#presenter-states)
    -   [<span data-ttu-id="d94d8-112">展示者介面</span><span class="sxs-lookup"><span data-stu-id="d94d8-112">Presenter Interfaces</span></span>](#presenter-interfaces)
    -   [<span data-ttu-id="d94d8-113">執行 IMFVideoDeviceID</span><span class="sxs-lookup"><span data-stu-id="d94d8-113">Implementing IMFVideoDeviceID</span></span>](#implementing-imfvideodeviceid)
    -   [<span data-ttu-id="d94d8-114">執行 IMFTopologyServiceLookupClient</span><span class="sxs-lookup"><span data-stu-id="d94d8-114">Implementing IMFTopologyServiceLookupClient</span></span>](#implementing-imftopologyservicelookupclient)
    -   [<span data-ttu-id="d94d8-115">執行 IMFVideoPresenter</span><span class="sxs-lookup"><span data-stu-id="d94d8-115">Implementing IMFVideoPresenter</span></span>](#implementing-imfvideopresenter)
    -   [<span data-ttu-id="d94d8-116">執行 IMFClockStateSink</span><span class="sxs-lookup"><span data-stu-id="d94d8-116">Implementing IMFClockStateSink</span></span>](#implementing-imfclockstatesink)
    -   [<span data-ttu-id="d94d8-117">執行 IMFRateSupport</span><span class="sxs-lookup"><span data-stu-id="d94d8-117">Implementing IMFRateSupport</span></span>](#implementing-imfratesupport)
    -   [<span data-ttu-id="d94d8-118">將事件傳送至 EVR</span><span class="sxs-lookup"><span data-stu-id="d94d8-118">Sending Events to the EVR</span></span>](#sending-events-to-the-evr)
-   [<span data-ttu-id="d94d8-119">協商格式</span><span class="sxs-lookup"><span data-stu-id="d94d8-119">Negotiating Formats</span></span>](#negotiating-formats)
-   [<span data-ttu-id="d94d8-120">管理 Direct3D 裝置</span><span class="sxs-lookup"><span data-stu-id="d94d8-120">Managing the Direct3D Device</span></span>](#managing-the-direct3d-device)
    -   [<span data-ttu-id="d94d8-121">配置 Direct3D 表面</span><span class="sxs-lookup"><span data-stu-id="d94d8-121">Allocating Direct3D Surfaces</span></span>](#allocating-direct3d-surfaces)
    -   [<span data-ttu-id="d94d8-122">追蹤範例</span><span class="sxs-lookup"><span data-stu-id="d94d8-122">Tracking Samples</span></span>](#tracking-samples)
-   [<span data-ttu-id="d94d8-123">處理輸出</span><span class="sxs-lookup"><span data-stu-id="d94d8-123">Processing Output</span></span>](#processing-output)
    -   [<span data-ttu-id="d94d8-124">重新繪製框架</span><span class="sxs-lookup"><span data-stu-id="d94d8-124">Repainting Frames</span></span>](#repainting-frames)
    -   [<span data-ttu-id="d94d8-125">排程範例</span><span class="sxs-lookup"><span data-stu-id="d94d8-125">Scheduling Samples</span></span>](#scheduling-samples)
    -   [<span data-ttu-id="d94d8-126">呈現範例</span><span class="sxs-lookup"><span data-stu-id="d94d8-126">Presenting Samples</span></span>](#presenting-samples)
    -   [<span data-ttu-id="d94d8-127">來源和目的地矩形</span><span class="sxs-lookup"><span data-stu-id="d94d8-127">Source and Destination Rectangles</span></span>](#source-and-destination-rectangles)
    -   [<span data-ttu-id="d94d8-128">資料流程結尾</span><span class="sxs-lookup"><span data-stu-id="d94d8-128">End of Stream</span></span>](#end-of-stream)
-   [<span data-ttu-id="d94d8-129">畫面逐步執行</span><span class="sxs-lookup"><span data-stu-id="d94d8-129">Frame Stepping</span></span>](#frame-stepping)
    -   [<span data-ttu-id="d94d8-130">執行框架逐步執行</span><span class="sxs-lookup"><span data-stu-id="d94d8-130">Implementing Frame Stepping</span></span>](#implementing-frame-stepping)
-   [<span data-ttu-id="d94d8-131">在 EVR 上設定展示者</span><span class="sxs-lookup"><span data-stu-id="d94d8-131">Setting the Presenter on the EVR</span></span>](#setting-the-presenter-on-the-evr)
    -   [<span data-ttu-id="d94d8-132">在 DirectShow 中設定展示者</span><span class="sxs-lookup"><span data-stu-id="d94d8-132">Setting the Presenter in DirectShow</span></span>](#setting-the-presenter-in-directshow)
    -   [<span data-ttu-id="d94d8-133">在媒體基礎中設定展示者</span><span class="sxs-lookup"><span data-stu-id="d94d8-133">Setting the Presenter in Media Foundation</span></span>](#setting-the-presenter-in-media-foundation)
-   [<span data-ttu-id="d94d8-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="d94d8-134">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="d94d8-135">必要條件</span><span class="sxs-lookup"><span data-stu-id="d94d8-135">Prerequisites</span></span>

<span data-ttu-id="d94d8-136">撰寫自訂的簡報者之前，您應該先熟悉下列技術：</span><span class="sxs-lookup"><span data-stu-id="d94d8-136">Before writing a custom presenter, you should be familiar with the following technologies:</span></span>

-   <span data-ttu-id="d94d8-137">增強型影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="d94d8-137">The enhanced video renderer.</span></span> <span data-ttu-id="d94d8-138">請參閱 [增強型影片](enhanced-video-renderer.md)轉譯器。</span><span class="sxs-lookup"><span data-stu-id="d94d8-138">See [Enhanced Video Renderer](enhanced-video-renderer.md).</span></span>
-   <span data-ttu-id="d94d8-139">Direct3D 圖形。</span><span class="sxs-lookup"><span data-stu-id="d94d8-139">Direct3D graphics.</span></span> <span data-ttu-id="d94d8-140">您不需要瞭解3D 圖形來撰寫簡報者，但您必須知道如何建立 Direct3D 裝置並管理 Direct3D 介面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-140">You don't need to understand 3-D graphics to write a presenter, but you must know how to create a Direct3D device and manage Direct3D surfaces.</span></span> <span data-ttu-id="d94d8-141">如果您不熟悉 Direct3D，請閱讀 DirectX 圖形 SDK 檔中的「Direct3D 裝置」和「Direct3D 資源」章節。</span><span class="sxs-lookup"><span data-stu-id="d94d8-141">If you aren't familiar with Direct3D, read the sections "Direct3D Devices" and "Direct3D Resources" in the DirectX Graphics SDK documentation.</span></span>
-   <span data-ttu-id="d94d8-142">DirectShow 篩選圖形或媒體基礎管線，取決於您的應用程式將用來呈現影片的技術。</span><span class="sxs-lookup"><span data-stu-id="d94d8-142">DirectShow filter graphs or the Media Foundation pipeline, depending on which technology your application will use to render video.</span></span>
-   <span data-ttu-id="d94d8-143">[媒體基礎轉換](media-foundation-transforms.md)。</span><span class="sxs-lookup"><span data-stu-id="d94d8-143">[Media Foundation Transforms](media-foundation-transforms.md).</span></span> <span data-ttu-id="d94d8-144">EVR 混音器是媒體基礎的轉換，而展示者會直接在混音器上呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="d94d8-144">The EVR mixer is a Media Foundation transform, and the presenter calls methods directly on the mixer.</span></span>
-   <span data-ttu-id="d94d8-145">執行 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="d94d8-145">Implementing COM objects.</span></span> <span data-ttu-id="d94d8-146">展示者是同進程的無線程 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="d94d8-146">The presenter is an in-process, free-threaded COM object.</span></span>

## <a name="presenter-object-model"></a><span data-ttu-id="d94d8-147">展示者物件模型</span><span class="sxs-lookup"><span data-stu-id="d94d8-147">Presenter Object Model</span></span>

<span data-ttu-id="d94d8-148">本節包含展示者物件模型和介面的總覽。</span><span class="sxs-lookup"><span data-stu-id="d94d8-148">This section contains an overview the presenter object model and interfaces.</span></span>

### <a name="data-flow-inside-the-evr"></a><span data-ttu-id="d94d8-149">EVR 內的資料流程</span><span class="sxs-lookup"><span data-stu-id="d94d8-149">Data Flow Inside the EVR</span></span>

<span data-ttu-id="d94d8-150">EVR 會使用兩個外掛程式元件來呈現影片： *混音* 器和展示 *者*。</span><span class="sxs-lookup"><span data-stu-id="d94d8-150">The EVR uses two plug-in components to render video: the *mixer* and the *presenter*.</span></span> <span data-ttu-id="d94d8-151">如有需要，混音器會混合影片串流並 deinterlaces 影片。</span><span class="sxs-lookup"><span data-stu-id="d94d8-151">The mixer blends the video streams and deinterlaces the video if needed.</span></span> <span data-ttu-id="d94d8-152">展示者會繪製 (*，或在* 繪製每個畫面時，將影片) 顯示和排程。</span><span class="sxs-lookup"><span data-stu-id="d94d8-152">The presenter draws (or *presents*) the video onto the display and schedules when each frame is drawn.</span></span> <span data-ttu-id="d94d8-153">應用程式可以將其中一個物件取代為自訂的執行。</span><span class="sxs-lookup"><span data-stu-id="d94d8-153">Applications can replace either of these objects with a custom implementation.</span></span>

<span data-ttu-id="d94d8-154">EVR 有一或多個輸入資料流程，且混音器有對應的輸入資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="d94d8-154">The EVR has one or more input streams, and the mixer has a corresponding number of input streams.</span></span> <span data-ttu-id="d94d8-155">資料流程0一律是 *參考資料流*。</span><span class="sxs-lookup"><span data-stu-id="d94d8-155">Stream 0 is always the *reference stream*.</span></span> <span data-ttu-id="d94d8-156">其他資料流程是 *子串流*，混音器 Alpha 會混合到參考資料流上。</span><span class="sxs-lookup"><span data-stu-id="d94d8-156">The other streams are *substreams*, which the mixer alpha-blends onto the reference stream.</span></span> <span data-ttu-id="d94d8-157">參考資料流會決定合成影片的主畫面格速率。</span><span class="sxs-lookup"><span data-stu-id="d94d8-157">The reference stream determines the master frame-rate for the composited video.</span></span> <span data-ttu-id="d94d8-158">針對每個參考框架，混音器會從每個子串流取得最新的畫面格，並將其混合到參考框架，然後輸出單一複合框架。</span><span class="sxs-lookup"><span data-stu-id="d94d8-158">For each reference frame, the mixer takes the most recent frame from each substream, alpha-blends them onto the reference frame, and outputs a single composited frame.</span></span> <span data-ttu-id="d94d8-159">如果有需要，混音器也會執行從 YUV 到 RGB 的去交錯和色彩轉換。</span><span class="sxs-lookup"><span data-stu-id="d94d8-159">The mixer also performs deinterlacing and color conversion from YUV to RGB if needed.</span></span> <span data-ttu-id="d94d8-160">無論輸入資料流程的數目或影片格式為何，EVR 一律會將混音器插入影片管線中。</span><span class="sxs-lookup"><span data-stu-id="d94d8-160">The EVR always inserts the mixer into the video pipeline, regardless of the number of input streams or the video format.</span></span> <span data-ttu-id="d94d8-161">下圖說明此程式。</span><span class="sxs-lookup"><span data-stu-id="d94d8-161">The following image illustrates this process.</span></span>

![顯示指向混音器之參考資料流和子資料流程的圖表，指向顯示](images/459338c4-cff8-4d20-bffd-ff1cbbe6f332.gif)

<span data-ttu-id="d94d8-163">展示者會執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="d94d8-163">The presenter performs the following tasks:</span></span>

-   <span data-ttu-id="d94d8-164">設定混音器上的輸出格式。</span><span class="sxs-lookup"><span data-stu-id="d94d8-164">Sets the output format on the mixer.</span></span> <span data-ttu-id="d94d8-165">開始串流之前，展示者會在混音器的輸出資料流程上設定媒體類型。</span><span class="sxs-lookup"><span data-stu-id="d94d8-165">Before streaming begins, the presenter sets a media type on the mixer's output stream.</span></span> <span data-ttu-id="d94d8-166">此媒體類型會定義複合映射的格式。</span><span class="sxs-lookup"><span data-stu-id="d94d8-166">This media type defines the format of the composited image.</span></span>
-   <span data-ttu-id="d94d8-167">建立 Direct3D 裝置。</span><span class="sxs-lookup"><span data-stu-id="d94d8-167">Creates the Direct3D device.</span></span>
-   <span data-ttu-id="d94d8-168">配置 Direct3D 表面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-168">Allocates Direct3D surfaces.</span></span> <span data-ttu-id="d94d8-169">混音器會將複合框架 blits 至這些表面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-169">The mixer blits the composited frames onto these surfaces.</span></span>
-   <span data-ttu-id="d94d8-170">取得混音器的輸出。</span><span class="sxs-lookup"><span data-stu-id="d94d8-170">Gets the output from the mixer.</span></span>
-   <span data-ttu-id="d94d8-171">排定畫面格的顯示時間。</span><span class="sxs-lookup"><span data-stu-id="d94d8-171">Schedules when the frames are presented.</span></span> <span data-ttu-id="d94d8-172">EVR 會提供簡報時鐘，而展示者會根據此時鐘來排程畫面格。</span><span class="sxs-lookup"><span data-stu-id="d94d8-172">The EVR provides the presentation clock, and the presenter schedules frames according to this clock.</span></span>
-   <span data-ttu-id="d94d8-173">使用 Direct3D 顯示每個畫面格。</span><span class="sxs-lookup"><span data-stu-id="d94d8-173">Presents each frame using Direct3D.</span></span>
-   <span data-ttu-id="d94d8-174">執行畫面格逐步執行和清除。</span><span class="sxs-lookup"><span data-stu-id="d94d8-174">Performs frame stepping and scrubbing.</span></span>

### <a name="presenter-states"></a><span data-ttu-id="d94d8-175">展示者狀態</span><span class="sxs-lookup"><span data-stu-id="d94d8-175">Presenter States</span></span>

<span data-ttu-id="d94d8-176">在任何時間，展示者都處於下列其中一種狀態：</span><span class="sxs-lookup"><span data-stu-id="d94d8-176">At any time, the presenter is in one of following states:</span></span>

-   <span data-ttu-id="d94d8-177">*已啟動*。</span><span class="sxs-lookup"><span data-stu-id="d94d8-177">*Started*.</span></span> <span data-ttu-id="d94d8-178">EVR 的簡報時鐘正在執行。</span><span class="sxs-lookup"><span data-stu-id="d94d8-178">The EVR's presentation clock is running.</span></span> <span data-ttu-id="d94d8-179">展示者會在呈現時安排影片畫面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-179">The presenter schedules video frames for presentation as they arrive.</span></span>
-   <span data-ttu-id="d94d8-180">已 *暫停*。</span><span class="sxs-lookup"><span data-stu-id="d94d8-180">*Paused*.</span></span> <span data-ttu-id="d94d8-181">簡報時鐘已暫止。</span><span class="sxs-lookup"><span data-stu-id="d94d8-181">The presentation clock is suspended.</span></span> <span data-ttu-id="d94d8-182">展示者不會顯示任何新的範例，但會維護其排程範例的佇列。</span><span class="sxs-lookup"><span data-stu-id="d94d8-182">The presenter does not present any new samples but maintains its queue of scheduled samples.</span></span> <span data-ttu-id="d94d8-183">如果收到新的範例，則展示者會將它們新增至佇列。</span><span class="sxs-lookup"><span data-stu-id="d94d8-183">If new samples are received, the presenter adds them to the queue.</span></span>
-   <span data-ttu-id="d94d8-184">*已停止*。</span><span class="sxs-lookup"><span data-stu-id="d94d8-184">*Stopped*.</span></span> <span data-ttu-id="d94d8-185">表示時鐘已停止。</span><span class="sxs-lookup"><span data-stu-id="d94d8-185">The presentation clock is stopped.</span></span> <span data-ttu-id="d94d8-186">展示者會捨棄已排程的任何範例。</span><span class="sxs-lookup"><span data-stu-id="d94d8-186">The presenter discards any samples that were scheduled.</span></span>
-   <span data-ttu-id="d94d8-187">*關機*。</span><span class="sxs-lookup"><span data-stu-id="d94d8-187">*Shut down*.</span></span> <span data-ttu-id="d94d8-188">展示者會釋放與串流相關的任何資源，例如 Direct3D 介面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-188">The presenter releases any resources related to streaming, such as Direct3D surfaces.</span></span> <span data-ttu-id="d94d8-189">這是展示者的初始狀態，以及呈現者終結之前的最終狀態。</span><span class="sxs-lookup"><span data-stu-id="d94d8-189">This is the presenter's initial state, and the final state before the presenter is destroyed.</span></span>

<span data-ttu-id="d94d8-190">在本主題的範例程式碼中，展示者狀態是以列舉表示：</span><span class="sxs-lookup"><span data-stu-id="d94d8-190">In the example code in this topic, the presenter state is represented by an enumeration:</span></span>


```C++
enum RENDER_STATE
{
    RENDER_STATE_STARTED = 1,
    RENDER_STATE_STOPPED,
    RENDER_STATE_PAUSED,
    RENDER_STATE_SHUTDOWN,  // Initial state.
};
```



<span data-ttu-id="d94d8-191">當展示者處於關閉狀態時，某些作業無效。</span><span class="sxs-lookup"><span data-stu-id="d94d8-191">Some operations are not valid while the presenter is in the shutdown state.</span></span> <span data-ttu-id="d94d8-192">範例程式碼會藉由呼叫 helper 方法來檢查此狀態：</span><span class="sxs-lookup"><span data-stu-id="d94d8-192">The example code checks for this state by calling a helper method:</span></span>


```C++
    HRESULT CheckShutdown() const
    {
        if (m_RenderState == RENDER_STATE_SHUTDOWN)
        {
            return MF_E_SHUTDOWN;
        }
        else
        {
            return S_OK;
        }
    }
```



### <a name="presenter-interfaces"></a><span data-ttu-id="d94d8-193">展示者介面</span><span class="sxs-lookup"><span data-stu-id="d94d8-193">Presenter Interfaces</span></span>

<span data-ttu-id="d94d8-194">需要展示者才能執行下列介面：</span><span class="sxs-lookup"><span data-stu-id="d94d8-194">A presenter is required to implement the following interfaces:</span></span>



| <span data-ttu-id="d94d8-195">介面</span><span class="sxs-lookup"><span data-stu-id="d94d8-195">Interface</span></span>                                                                | <span data-ttu-id="d94d8-196">描述</span><span class="sxs-lookup"><span data-stu-id="d94d8-196">Description</span></span>                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d94d8-197">**IMFClockStateSink**</span><span class="sxs-lookup"><span data-stu-id="d94d8-197">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)                           | <span data-ttu-id="d94d8-198">當 EVR 的時鐘變更狀態時，通知簡報者。</span><span class="sxs-lookup"><span data-stu-id="d94d8-198">Notifies the presenter when the EVR's clock changes state.</span></span> <span data-ttu-id="d94d8-199">請參閱 [執行 IMFClockStateSink](#implementing-imfclockstatesink)。</span><span class="sxs-lookup"><span data-stu-id="d94d8-199">See [Implementing IMFClockStateSink](#implementing-imfclockstatesink).</span></span>                                   |
| [<span data-ttu-id="d94d8-200">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="d94d8-200">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                   | <span data-ttu-id="d94d8-201">提供方法，讓管線中的應用程式和其他元件從展示者取得介面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-201">Provides a way for the application and other components in the pipeline to get interfaces from the presenter.</span></span>                                                       |
| [<span data-ttu-id="d94d8-202">**IMFTopologyServiceLookupClient**</span><span class="sxs-lookup"><span data-stu-id="d94d8-202">**IMFTopologyServiceLookupClient**</span></span>](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | <span data-ttu-id="d94d8-203">讓展示者從 EVR 或混音器取得介面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-203">Enables the presenter to get interfaces from the EVR or the mixer.</span></span> <span data-ttu-id="d94d8-204">請參閱 [執行 IMFTopologyServiceLookupClient](#implementing-imftopologyservicelookupclient)。</span><span class="sxs-lookup"><span data-stu-id="d94d8-204">See [Implementing IMFTopologyServiceLookupClient](#implementing-imftopologyservicelookupclient).</span></span> |
| [<span data-ttu-id="d94d8-205">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="d94d8-205">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | <span data-ttu-id="d94d8-206">確保展示者和混音器使用相容的技術。</span><span class="sxs-lookup"><span data-stu-id="d94d8-206">Ensures that the presenter and the mixer use compatible technologies.</span></span> <span data-ttu-id="d94d8-207">請參閱 [執行 IMFVideoDeviceID](#implementing-imfvideodeviceid)。</span><span class="sxs-lookup"><span data-stu-id="d94d8-207">See [Implementing IMFVideoDeviceID](#implementing-imfvideodeviceid).</span></span>                          |
| [<span data-ttu-id="d94d8-208">**IMFVideoPresenter**</span><span class="sxs-lookup"><span data-stu-id="d94d8-208">**IMFVideoPresenter**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopresenter)                           | <span data-ttu-id="d94d8-209">處理來自 EVR 的訊息。</span><span class="sxs-lookup"><span data-stu-id="d94d8-209">Processes messages from the EVR.</span></span> <span data-ttu-id="d94d8-210">請參閱 [執行 IMFVideoPresenter](#implementing-imfvideopresenter)。</span><span class="sxs-lookup"><span data-stu-id="d94d8-210">See [Implementing IMFVideoPresenter](#implementing-imfvideopresenter).</span></span>                                                             |



 

<span data-ttu-id="d94d8-211">以下是選用介面：</span><span class="sxs-lookup"><span data-stu-id="d94d8-211">The following interfaces are optional:</span></span>



| <span data-ttu-id="d94d8-212">介面</span><span class="sxs-lookup"><span data-stu-id="d94d8-212">Interface</span></span>                                                | <span data-ttu-id="d94d8-213">描述</span><span class="sxs-lookup"><span data-stu-id="d94d8-213">Description</span></span>                                                                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d94d8-214">**IEVRTrustedVideoPlugin**</span><span class="sxs-lookup"><span data-stu-id="d94d8-214">**IEVRTrustedVideoPlugin**</span></span>](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | <span data-ttu-id="d94d8-215">讓展示者能夠使用受保護的媒體。</span><span class="sxs-lookup"><span data-stu-id="d94d8-215">Enables the presenter to work with protected media.</span></span> <span data-ttu-id="d94d8-216">如果您的展示者是受信任的元件，其設計目的是要在受保護的媒體路徑中 (PMP) ，請執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-216">Implement this interface if your presenter is a trusted component designed to work in the protected media path (PMP).</span></span> |
| [<span data-ttu-id="d94d8-217">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="d94d8-217">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | <span data-ttu-id="d94d8-218">報告展示者支援的播放率範圍。</span><span class="sxs-lookup"><span data-stu-id="d94d8-218">Reports the range of playback rates that the presenter supports.</span></span> <span data-ttu-id="d94d8-219">請參閱 [執行 IMFRateSupport](#implementing-imfratesupport)。</span><span class="sxs-lookup"><span data-stu-id="d94d8-219">See [Implementing IMFRateSupport](#implementing-imfratesupport).</span></span>                                         |
| [<span data-ttu-id="d94d8-220">**IMFVideoPositionMapper**</span><span class="sxs-lookup"><span data-stu-id="d94d8-220">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | <span data-ttu-id="d94d8-221">將輸出影片畫面上的座標組應到輸入影片畫面上的座標。</span><span class="sxs-lookup"><span data-stu-id="d94d8-221">Maps coordinates on the output video frame to coordinates on the input video frame.</span></span>                                                                                       |
| [<span data-ttu-id="d94d8-222">**IQualProp**</span><span class="sxs-lookup"><span data-stu-id="d94d8-222">**IQualProp**</span></span>](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop)                         | <span data-ttu-id="d94d8-223">報告效能資訊。</span><span class="sxs-lookup"><span data-stu-id="d94d8-223">Reports performance information.</span></span> <span data-ttu-id="d94d8-224">EVR 會使用此資訊來進行品質控制管理。</span><span class="sxs-lookup"><span data-stu-id="d94d8-224">The EVR uses this information for quality-control management.</span></span> <span data-ttu-id="d94d8-225">此介面記載于 DirectShow SDK 中。</span><span class="sxs-lookup"><span data-stu-id="d94d8-225">This interface is documented in the DirectShow SDK.</span></span>                        |



 

<span data-ttu-id="d94d8-226">您也可以提供介面讓應用程式與展示者進行通訊。</span><span class="sxs-lookup"><span data-stu-id="d94d8-226">You can also provide interfaces for the application to communicate with the presenter.</span></span> <span data-ttu-id="d94d8-227">標準展示者會針對此用途來實行 [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) 介面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-227">The standard presenter implements the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface for this purpose.</span></span> <span data-ttu-id="d94d8-228">您可以執行這個介面或定義自己的介面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-228">You can implement this interface or define your own.</span></span> <span data-ttu-id="d94d8-229">應用程式會在 EVR 上呼叫 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) ，以從展示者取得介面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-229">The application obtains interfaces from the presenter by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the EVR.</span></span> <span data-ttu-id="d94d8-230">當 **MR_VIDEO_RENDER_SERVICE** 服務 GUID 時，EVR 會將 **GetService** 要求傳遞給展示者。</span><span class="sxs-lookup"><span data-stu-id="d94d8-230">When the service GUID is **MR_VIDEO_RENDER_SERVICE**, the EVR passes the **GetService** request to the presenter.</span></span>

### <a name="implementing-imfvideodeviceid"></a><span data-ttu-id="d94d8-231">執行 IMFVideoDeviceID</span><span class="sxs-lookup"><span data-stu-id="d94d8-231">Implementing IMFVideoDeviceID</span></span>

<span data-ttu-id="d94d8-232">[**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)介面包含一個方法 [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid)，它會傳回裝置 GUID。</span><span class="sxs-lookup"><span data-stu-id="d94d8-232">The [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) interface contains one method, [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid), which returns a device GUID.</span></span> <span data-ttu-id="d94d8-233">裝置 GUID 可確保展示者和混音器使用相容的技術。</span><span class="sxs-lookup"><span data-stu-id="d94d8-233">The device GUID ensures that the presenter and the mixer use compatible technologies.</span></span> <span data-ttu-id="d94d8-234">如果裝置 Guid 不符，EVR 將無法初始化。</span><span class="sxs-lookup"><span data-stu-id="d94d8-234">If the device GUIDs do not match, the EVR fails to initialize.</span></span>

<span data-ttu-id="d94d8-235">標準混音器和展示者都使用 Direct3D 9，其裝置 GUID 等於 **IID_IDirect3DDevice9**。</span><span class="sxs-lookup"><span data-stu-id="d94d8-235">The standard mixer and presenter both use Direct3D 9, with the device GUID equal to **IID_IDirect3DDevice9**.</span></span> <span data-ttu-id="d94d8-236">如果您想要搭配使用您的自訂展示者與標準混音器，則必須 **IID_IDirect3DDevice9** 簡報者的裝置 GUID。</span><span class="sxs-lookup"><span data-stu-id="d94d8-236">If you intend to use your custom presenter with the standard mixer, the presenter's device GUID must be **IID_IDirect3DDevice9**.</span></span> <span data-ttu-id="d94d8-237">如果您取代這兩個元件，則可以定義新的裝置 GUID。</span><span class="sxs-lookup"><span data-stu-id="d94d8-237">If you replace both components, you could define a new device GUID.</span></span> <span data-ttu-id="d94d8-238">本文的其餘部分將假設展示者使用 Direct3D 9。</span><span class="sxs-lookup"><span data-stu-id="d94d8-238">For the remainder of this article, it is assumed that the presenter uses Direct3D 9.</span></span> <span data-ttu-id="d94d8-239">以下是 [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid)的標準實作為：</span><span class="sxs-lookup"><span data-stu-id="d94d8-239">Here is the standard implementation of [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid):</span></span>


```C++
HRESULT EVRCustomPresenter::GetDeviceID(IID* pDeviceID)
{
    if (pDeviceID == NULL)
    {
        return E_POINTER;
    }

    *pDeviceID = __uuidof(IDirect3DDevice9);
    return S_OK;
}
```



<span data-ttu-id="d94d8-240">即使在展示者關閉的情況下，方法應該會成功。</span><span class="sxs-lookup"><span data-stu-id="d94d8-240">The method should succeed even when the presenter is shut down.</span></span>

### <a name="implementing-imftopologyservicelookupclient"></a><span data-ttu-id="d94d8-241">執行 IMFTopologyServiceLookupClient</span><span class="sxs-lookup"><span data-stu-id="d94d8-241">Implementing IMFTopologyServiceLookupClient</span></span>

<span data-ttu-id="d94d8-242">[**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient)介面可讓展示者從 EVR 和混音器取得介面指標，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d94d8-242">The [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) interface enables the presenter to get interface pointers from the EVR and from the mixer as follows:</span></span>

1.  <span data-ttu-id="d94d8-243">當 EVR 初始化展示者時，它會呼叫展示者的 [**IMFTopologyServiceLookupClient：： InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) 方法。</span><span class="sxs-lookup"><span data-stu-id="d94d8-243">When the EVR initializes the presenter, it calls the presenter's [**IMFTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) method.</span></span> <span data-ttu-id="d94d8-244">引數是指向 EVR 之 [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="d94d8-244">The argument is a pointer to the EVR's [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) interface.</span></span>
2.  <span data-ttu-id="d94d8-245">展示者會呼叫 [**IMFTopologyServiceLookup：： LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) ，以從 EVR 或混音器取得介面指標。</span><span class="sxs-lookup"><span data-stu-id="d94d8-245">The presenter calls [**IMFTopologyServiceLookup::LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) to get interface pointers from either the EVR or the mixer.</span></span>

<span data-ttu-id="d94d8-246">[**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice)方法類似于 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice)方法。</span><span class="sxs-lookup"><span data-stu-id="d94d8-246">The [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) method is similar to the [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) method.</span></span> <span data-ttu-id="d94d8-247">這兩種方法都會將服務 GUID 和介面識別碼 (IID) 做為輸入，但 **LookupService** 會傳回介面指標的陣列，而 **GetService** 會傳回單一指標。</span><span class="sxs-lookup"><span data-stu-id="d94d8-247">Both methods take a service GUID and an interface identifier (IID) as input, but **LookupService** returns an array of interface pointers, while **GetService** returns a single pointer.</span></span> <span data-ttu-id="d94d8-248">不過在實務上，您一律可以將陣列大小設定為1。</span><span class="sxs-lookup"><span data-stu-id="d94d8-248">In practice, however, you can always set the array size to 1.</span></span> <span data-ttu-id="d94d8-249">查詢的物件取決於服務 GUID：</span><span class="sxs-lookup"><span data-stu-id="d94d8-249">The object queried depends on the service GUID:</span></span>

-   <span data-ttu-id="d94d8-250">如果 **MR_VIDEO_RENDER_SERVICE** 服務 GUID，則會查詢 EVR。</span><span class="sxs-lookup"><span data-stu-id="d94d8-250">If the service GUID is **MR_VIDEO_RENDER_SERVICE**, the EVR is queried.</span></span>
-   <span data-ttu-id="d94d8-251">如果 **MR_VIDEO_MIXER_SERVICE** 服務 GUID，則會查詢混音器。</span><span class="sxs-lookup"><span data-stu-id="d94d8-251">If the service GUID is **MR_VIDEO_MIXER_SERVICE**, the mixer is queried.</span></span>

<span data-ttu-id="d94d8-252">在 [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers)的執行中，從 EVR 取得下列介面：</span><span class="sxs-lookup"><span data-stu-id="d94d8-252">In your implementation of [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers), get the following interfaces from the EVR:</span></span>



| <span data-ttu-id="d94d8-253">EVR 介面</span><span class="sxs-lookup"><span data-stu-id="d94d8-253">EVR Interface</span></span>                                | <span data-ttu-id="d94d8-254">描述</span><span class="sxs-lookup"><span data-stu-id="d94d8-254">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d94d8-255">**IMediaEventSink**</span><span class="sxs-lookup"><span data-stu-id="d94d8-255">**IMediaEventSink**</span></span>](/windows/win32/api/strmif/nn-strmif-imediaeventsink) | <span data-ttu-id="d94d8-256">提供方法讓展示者將訊息傳送至 EVR。</span><span class="sxs-lookup"><span data-stu-id="d94d8-256">Provides a way for the presenter to send messages to the EVR.</span></span> <span data-ttu-id="d94d8-257">此介面定義于 DirectShow SDK 中，因此訊息會遵循 DirectShow 事件的模式，而不是媒體基礎事件。</span><span class="sxs-lookup"><span data-stu-id="d94d8-257">This interface is defined in the DirectShow SDK, so the messages follow the pattern for DirectShow events, not Media Foundation events.</span></span><br/>                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="d94d8-258">**IMFClock**</span><span class="sxs-lookup"><span data-stu-id="d94d8-258">**IMFClock**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclock)                 | <span data-ttu-id="d94d8-259">表示 EVR 的時鐘。</span><span class="sxs-lookup"><span data-stu-id="d94d8-259">Represents the EVR's clock.</span></span> <span data-ttu-id="d94d8-260">展示者會使用此介面來排程簡報的範例。</span><span class="sxs-lookup"><span data-stu-id="d94d8-260">The presenter uses this interface to schedule samples for presentation.</span></span> <span data-ttu-id="d94d8-261">EVR 可在沒有時鐘的情況下執行，因此可能無法使用此介面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-261">The EVR can run without a clock, so this interface might not be available.</span></span> <span data-ttu-id="d94d8-262">如果沒有，請忽略 [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice)中的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d94d8-262">If not, ignore the error code from [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice).</span></span><br/> <span data-ttu-id="d94d8-263">時鐘也會實 [**IMFTimer**](/windows/desktop/api/mfidl/nn-mfidl-imftimer) 介面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-263">The clock also implements the [**IMFTimer**](/windows/desktop/api/mfidl/nn-mfidl-imftimer) interface.</span></span> <span data-ttu-id="d94d8-264">在媒體基礎管線中，時鐘會實 [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) 介面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-264">In the Media Foundation pipeline, the clock implements the [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) interface.</span></span> <span data-ttu-id="d94d8-265">它不會在 DirectShow 中執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-265">It does not implement this interface in DirectShow.</span></span><br/> |



 

<span data-ttu-id="d94d8-266">從混音器取得下列介面：</span><span class="sxs-lookup"><span data-stu-id="d94d8-266">Get the following interfaces from the mixer:</span></span>



| <span data-ttu-id="d94d8-267">混音器介面</span><span class="sxs-lookup"><span data-stu-id="d94d8-267">Mixer Interface</span></span>                              | <span data-ttu-id="d94d8-268">描述</span><span class="sxs-lookup"><span data-stu-id="d94d8-268">Description</span></span>                                                |
|----------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="d94d8-269">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="d94d8-269">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)         | <span data-ttu-id="d94d8-270">讓展示者與混音器進行通訊。</span><span class="sxs-lookup"><span data-stu-id="d94d8-270">Enables the presenter to communicate with the mixer.</span></span>       |
| [<span data-ttu-id="d94d8-271">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="d94d8-271">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) | <span data-ttu-id="d94d8-272">讓展示者可以驗證混音器的裝置 GUID。</span><span class="sxs-lookup"><span data-stu-id="d94d8-272">Enables the presenter to validate the mixer's device GUID.</span></span> |



 

<span data-ttu-id="d94d8-273">下列程式碼會實行 [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) 方法：</span><span class="sxs-lookup"><span data-stu-id="d94d8-273">The following code implements the [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) method :</span></span>


```C++
HRESULT EVRCustomPresenter::InitServicePointers(
    IMFTopologyServiceLookup *pLookup
    )
{
    if (pLookup == NULL)
    {
        return E_POINTER;
    }

    HRESULT             hr = S_OK;
    DWORD               dwObjectCount = 0;

    EnterCriticalSection(&m_ObjectLock);

    // Do not allow initializing when playing or paused.
    if (IsActive())
    {
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    // Ask for the clock. Optional, because the EVR might not have a clock.
    dwObjectCount = 1;

    (void)pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL,   // Not used.
        0,                          // Reserved.
        MR_VIDEO_RENDER_SERVICE,    // Service to look up.
        IID_PPV_ARGS(&m_pClock),    // Interface to retrieve.
        &dwObjectCount              // Number of elements retrieved.
        );

    // Ask for the mixer. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_MIXER_SERVICE, IID_PPV_ARGS(&m_pMixer), &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Make sure that we can work with this mixer.
    hr = ConfigureMixer(m_pMixer);
    if (FAILED(hr))
    {
        goto done;
    }

    // Ask for the EVR's event-sink interface. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_RENDER_SERVICE, IID_PPV_ARGS(&m_pMediaEventSink),
        &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Successfully initialized. Set the state to "stopped."
    m_RenderState = RENDER_STATE_STOPPED;

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



<span data-ttu-id="d94d8-274">當從 [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) 取得的介面指標不再有效時，EVR 會呼叫 [**IMFTopologyServiceLookupClient：： ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers)。</span><span class="sxs-lookup"><span data-stu-id="d94d8-274">When the interface pointers obtained from [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) are no longer valid, the EVR calls [**IMFTopologyServiceLookupClient::ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers).</span></span> <span data-ttu-id="d94d8-275">在這個方法內，釋出所有介面指標，並將展示者狀態設定為 [已關閉]：</span><span class="sxs-lookup"><span data-stu-id="d94d8-275">Inside this method, release all interface pointers and set the presenter state to shut down:</span></span>


```C++
HRESULT EVRCustomPresenter::ReleaseServicePointers()
{
    // Enter the shut-down state.
    EnterCriticalSection(&m_ObjectLock);

    m_RenderState = RENDER_STATE_SHUTDOWN;

    LeaveCriticalSection(&m_ObjectLock);

    // Flush any samples that were scheduled.
    Flush();

    // Clear the media type and release related resources.
    SetMediaType(NULL);

    // Release all services that were acquired from InitServicePointers.
    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    return S_OK;
}
```



<span data-ttu-id="d94d8-276">由於各種原因，EVR 會呼叫 [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) ，包括：</span><span class="sxs-lookup"><span data-stu-id="d94d8-276">The EVR calls [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) for various reasons, including:</span></span>

-   <span data-ttu-id="d94d8-277">中斷連接或重新連接 (DirectShow) 的 pin，或 (媒體基礎) 新增或移除串流接收器。</span><span class="sxs-lookup"><span data-stu-id="d94d8-277">Disconnecting or reconnecting pins (DirectShow), or adding or removing stream sinks (Media Foundation).</span></span>
-   <span data-ttu-id="d94d8-278">變更格式。</span><span class="sxs-lookup"><span data-stu-id="d94d8-278">Changing format.</span></span>
-   <span data-ttu-id="d94d8-279">設定新的時鐘。</span><span class="sxs-lookup"><span data-stu-id="d94d8-279">Setting a new clock.</span></span>
-   <span data-ttu-id="d94d8-280">EVR 的最終關機。</span><span class="sxs-lookup"><span data-stu-id="d94d8-280">Final shutdown of the EVR.</span></span>

<span data-ttu-id="d94d8-281">在展示者的存留期內，EVR 可能會呼叫 [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) 和 [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) 數次。</span><span class="sxs-lookup"><span data-stu-id="d94d8-281">During the lifetime of the presenter, the EVR might call [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) and [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) several times.</span></span>

### <a name="implementing-imfvideopresenter"></a><span data-ttu-id="d94d8-282">執行 IMFVideoPresenter</span><span class="sxs-lookup"><span data-stu-id="d94d8-282">Implementing IMFVideoPresenter</span></span>

<span data-ttu-id="d94d8-283">[**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)介面會繼承 [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)並新增兩個方法：</span><span class="sxs-lookup"><span data-stu-id="d94d8-283">The [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) interface inherits [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) and adds two methods:</span></span>



| <span data-ttu-id="d94d8-284">方法</span><span class="sxs-lookup"><span data-stu-id="d94d8-284">Method</span></span>                                                               | <span data-ttu-id="d94d8-285">描述</span><span class="sxs-lookup"><span data-stu-id="d94d8-285">Description</span></span>                                            |
|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="d94d8-286">**GetCurrentMediaType**</span><span class="sxs-lookup"><span data-stu-id="d94d8-286">**GetCurrentMediaType**</span></span>](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) | <span data-ttu-id="d94d8-287">傳回復合影片框架的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="d94d8-287">Returns the media type of the composited video frames.</span></span> |
| [<span data-ttu-id="d94d8-288">**ProcessMessage**</span><span class="sxs-lookup"><span data-stu-id="d94d8-288">**ProcessMessage**</span></span>](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage)           | <span data-ttu-id="d94d8-289">指示展示者執行各種動作。</span><span class="sxs-lookup"><span data-stu-id="d94d8-289">Signals the presenter to perform various actions.</span></span>      |



 

<span data-ttu-id="d94d8-290">[**GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype)方法會傳回展示者的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="d94d8-290">The [**GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) method returns the presenter's media type.</span></span> <span data-ttu-id="d94d8-291"> (如需設定媒體類型的詳細資訊，請參閱 [協商格式](#negotiating-formats)。 ) 媒體類型會以 [**IMFVideoMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype) 介面指標的形式傳回。</span><span class="sxs-lookup"><span data-stu-id="d94d8-291">(For details about setting the media type, see [Negotiating Formats](#negotiating-formats).) The media type is returned as an [**IMFVideoMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype) interface pointer.</span></span> <span data-ttu-id="d94d8-292">下列範例假設展示者將媒體類型儲存為 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 指標。</span><span class="sxs-lookup"><span data-stu-id="d94d8-292">The following example assumes that the presenter stores the media type as an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) pointer.</span></span> <span data-ttu-id="d94d8-293">若要從媒體類型取得 **IMFVideoMediaType** 介面，請呼叫 **QueryInterface**：</span><span class="sxs-lookup"><span data-stu-id="d94d8-293">To get the **IMFVideoMediaType** interface from the media type, call **QueryInterface**:</span></span>


```C++
HRESULT EVRCustomPresenter::GetCurrentMediaType(
    IMFVideoMediaType** ppMediaType
    )
{
    HRESULT hr = S_OK;

    if (ppMediaType == NULL)
    {
        return E_POINTER;
    }

    *ppMediaType = NULL;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    if (m_pMediaType == NULL)
    {
        hr = MF_E_NOT_INITIALIZED;
        goto done;
    }

    hr = m_pMediaType->QueryInterface(IID_PPV_ARGS(ppMediaType));

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



<span data-ttu-id="d94d8-294">[**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage)方法是 EVR 與展示者通訊的主要機制。</span><span class="sxs-lookup"><span data-stu-id="d94d8-294">The [**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) method is the primary mechanism for the EVR to communicate with the presenter.</span></span> <span data-ttu-id="d94d8-295">已定義下列訊息。</span><span class="sxs-lookup"><span data-stu-id="d94d8-295">The following messages are defined.</span></span> <span data-ttu-id="d94d8-296">本主題的其餘部分會提供執行每個訊息的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d94d8-296">The details of implementing each message are given in the remainder of this topic.</span></span>



| <span data-ttu-id="d94d8-297">訊息</span><span class="sxs-lookup"><span data-stu-id="d94d8-297">Message</span></span>                                | <span data-ttu-id="d94d8-298">描述</span><span class="sxs-lookup"><span data-stu-id="d94d8-298">Description</span></span>                                                                                                                                                                                                                                        |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d94d8-299">**MFVP_MESSAGE_INVALIDATEMEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="d94d8-299">**MFVP_MESSAGE_INVALIDATEMEDIATYPE**</span></span> | <span data-ttu-id="d94d8-300">混音器的輸出媒體類型無效。</span><span class="sxs-lookup"><span data-stu-id="d94d8-300">The mixer's output media type is invalid.</span></span> <span data-ttu-id="d94d8-301">展示者應該使用混音器來協商新的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="d94d8-301">The presenter should negotiate a new media type with the mixer.</span></span> <span data-ttu-id="d94d8-302">請參閱 [協商格式](#negotiating-formats)。</span><span class="sxs-lookup"><span data-stu-id="d94d8-302">See [Negotiating Formats](#negotiating-formats).</span></span>                                                                                         |
| <span data-ttu-id="d94d8-303">**MFVP_MESSAGE_BEGINSTREAMING**</span><span class="sxs-lookup"><span data-stu-id="d94d8-303">**MFVP_MESSAGE_BEGINSTREAMING**</span></span>      | <span data-ttu-id="d94d8-304">串流已開始。</span><span class="sxs-lookup"><span data-stu-id="d94d8-304">Streaming has started.</span></span> <span data-ttu-id="d94d8-305">此訊息不需要任何特定動作，但您可以使用它來配置資源。</span><span class="sxs-lookup"><span data-stu-id="d94d8-305">No particular action is required by this message, but you can use it to allocate resources.</span></span>                                                                                                                                 |
| <span data-ttu-id="d94d8-306">**MFVP_MESSAGE_ENDSTREAMING**</span><span class="sxs-lookup"><span data-stu-id="d94d8-306">**MFVP_MESSAGE_ENDSTREAMING**</span></span>        | <span data-ttu-id="d94d8-307">串流已經結束。</span><span class="sxs-lookup"><span data-stu-id="d94d8-307">Streaming has ended.</span></span> <span data-ttu-id="d94d8-308">釋放您為了回應 **MFVP_MESSAGE_BEGINSTREAMING** 訊息所配置的任何資源。</span><span class="sxs-lookup"><span data-stu-id="d94d8-308">Release any resources that you allocated in response to the **MFVP_MESSAGE_BEGINSTREAMING** message.</span></span>                                                                                                                        |
| <span data-ttu-id="d94d8-309">**MFVP_MESSAGE_PROCESSINPUTNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="d94d8-309">**MFVP_MESSAGE_PROCESSINPUTNOTIFY**</span></span>  | <span data-ttu-id="d94d8-310">混音器已收到新的輸入範例，而且可能會產生新的輸出框架。</span><span class="sxs-lookup"><span data-stu-id="d94d8-310">The mixer has received a new input sample and might be able to generate a new output frame.</span></span> <span data-ttu-id="d94d8-311">展示者應該在混音器上呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 。</span><span class="sxs-lookup"><span data-stu-id="d94d8-311">The presenter should call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span> <span data-ttu-id="d94d8-312">請參閱 [處理輸出](#processing-output)。</span><span class="sxs-lookup"><span data-stu-id="d94d8-312">See [Processing Output](#processing-output).</span></span> |
| <span data-ttu-id="d94d8-313">**MFVP_MESSAGE_ENDOFSTREAM**</span><span class="sxs-lookup"><span data-stu-id="d94d8-313">**MFVP_MESSAGE_ENDOFSTREAM**</span></span>         | <span data-ttu-id="d94d8-314">簡報已經結束。</span><span class="sxs-lookup"><span data-stu-id="d94d8-314">The presentation has ended.</span></span> <span data-ttu-id="d94d8-315">請參閱 [資料流程的結尾](#end-of-stream)。</span><span class="sxs-lookup"><span data-stu-id="d94d8-315">See [End of Stream](#end-of-stream).</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="d94d8-316">**MFVP_MESSAGE_FLUSH**</span><span class="sxs-lookup"><span data-stu-id="d94d8-316">**MFVP_MESSAGE_FLUSH**</span></span>               | <span data-ttu-id="d94d8-317">EVR 正在清除其轉譯管線中的資料。</span><span class="sxs-lookup"><span data-stu-id="d94d8-317">The EVR is flushing the data in its rendering pipeline.</span></span> <span data-ttu-id="d94d8-318">展示者應該捨棄任何已排程進行簡報的影片畫面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-318">The presenter should discard any video frames that are scheduled for presentation.</span></span>                                                                                                         |
| <span data-ttu-id="d94d8-319">**MFVP_MESSAGE_STEP**</span><span class="sxs-lookup"><span data-stu-id="d94d8-319">**MFVP_MESSAGE_STEP**</span></span>                | <span data-ttu-id="d94d8-320">要求展示者逐步執行 N 個畫面格。</span><span class="sxs-lookup"><span data-stu-id="d94d8-320">Requests the presenter to step forward N frames.</span></span> <span data-ttu-id="d94d8-321">展示者應該捨棄下一個 N-1 的框架，並顯示第 n 個框架。</span><span class="sxs-lookup"><span data-stu-id="d94d8-321">The presenter should discard the next N-1 frames and display the Nth frame.</span></span> <span data-ttu-id="d94d8-322">查看 [框架逐步執行](#frame-stepping)。</span><span class="sxs-lookup"><span data-stu-id="d94d8-322">See [Frame Stepping](#frame-stepping).</span></span>                                                                                |
| <span data-ttu-id="d94d8-323">**MFVP_MESSAGE_CANCELSTEP**</span><span class="sxs-lookup"><span data-stu-id="d94d8-323">**MFVP_MESSAGE_CANCELSTEP**</span></span>          | <span data-ttu-id="d94d8-324">取消框架逐步執行。</span><span class="sxs-lookup"><span data-stu-id="d94d8-324">Cancels frame stepping.</span></span>                                                                                                                                                                                                                            |



 

### <a name="implementing-imfclockstatesink"></a><span data-ttu-id="d94d8-325">執行 IMFClockStateSink</span><span class="sxs-lookup"><span data-stu-id="d94d8-325">Implementing IMFClockStateSink</span></span>

<span data-ttu-id="d94d8-326">展示者必須在其 [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)的實 [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)介面中執行，以繼承 **IMFClockStateSink**。</span><span class="sxs-lookup"><span data-stu-id="d94d8-326">The presenter must implement the [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) interface as part of its implementation of [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter), which inherits **IMFClockStateSink**.</span></span> <span data-ttu-id="d94d8-327">EVR 會使用此介面，在 EVR 的時鐘變更狀態時通知演講者。</span><span class="sxs-lookup"><span data-stu-id="d94d8-327">The EVR uses this interface to notify the presenter whenever the EVR's clock changes state.</span></span> <span data-ttu-id="d94d8-328">如需有關時鐘狀態的詳細資訊，請參閱 [呈現頻率](presentation-clock.md)。</span><span class="sxs-lookup"><span data-stu-id="d94d8-328">For more information about the clock states, see [Presentation Clock](presentation-clock.md).</span></span>

<span data-ttu-id="d94d8-329">以下是在此介面中執行方法的一些指導方針。</span><span class="sxs-lookup"><span data-stu-id="d94d8-329">Here are some guidelines for implementing the methods in this interface.</span></span> <span data-ttu-id="d94d8-330">如果展示者已關閉，所有方法都應該會失敗。</span><span class="sxs-lookup"><span data-stu-id="d94d8-330">All of the methods should fail if the presenter is shut down.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d94d8-331"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="d94d8-331"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="d94d8-332">將展示者狀態設定為 [已啟動]。</span><span class="sxs-lookup"><span data-stu-id="d94d8-332">Set the presenter state to started.</span></span></li>
<li><span data-ttu-id="d94d8-333">如果未<strong>PRESENTATION_CURRENT_POSITION</strong> <em>llClockStartOffset</em> ，請清除展示者的範例佇列。</span><span class="sxs-lookup"><span data-stu-id="d94d8-333">If the <em>llClockStartOffset</em> is not <strong>PRESENTATION_CURRENT_POSITION</strong>, flush the presenter's queue of samples.</span></span> <span data-ttu-id="d94d8-334"> (這相當於接收 <strong>MFVP_MESSAGE_FLUSH</strong> 訊息。 ) </span><span class="sxs-lookup"><span data-stu-id="d94d8-334">(This is equivalent to receiving an <strong>MFVP_MESSAGE_FLUSH</strong> message.)</span></span></li>
<li><span data-ttu-id="d94d8-335">如果先前的框架步驟要求仍在擱置中，請處理要求 (查看 <a href="#frame-stepping">畫面格逐步執行</a>) 。</span><span class="sxs-lookup"><span data-stu-id="d94d8-335">If a previous frame-step request is still pending, process the request (see <a href="#frame-stepping">Frame Stepping</a>).</span></span> <span data-ttu-id="d94d8-336">否則，請嘗試處理混音器的輸出 (查看 <a href="#processing-output">處理輸出</a>。</span><span class="sxs-lookup"><span data-stu-id="d94d8-336">Otherwise, try to process output from the mixer (see <a href="#processing-output">Processing Output</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d94d8-337"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop"><strong>OnClockStop</strong></a></span><span class="sxs-lookup"><span data-stu-id="d94d8-337"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop"><strong>OnClockStop</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="d94d8-338">將展示者狀態設定為 [已停止]。</span><span class="sxs-lookup"><span data-stu-id="d94d8-338">Set the presenter state to stopped.</span></span></li>
<li><span data-ttu-id="d94d8-339">清除展示者的範例佇列。</span><span class="sxs-lookup"><span data-stu-id="d94d8-339">Flush the presenter's queue of samples.</span></span></li>
<li><span data-ttu-id="d94d8-340">取消任何暫止的框架步驟操作。</span><span class="sxs-lookup"><span data-stu-id="d94d8-340">Cancel any pending frame-step operation.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d94d8-341"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause"><strong>OnClockPause</strong></a></span><span class="sxs-lookup"><span data-stu-id="d94d8-341"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause"><strong>OnClockPause</strong></a></span></span></td>
<td><span data-ttu-id="d94d8-342">將展示者狀態設定為 [已暫停]。</span><span class="sxs-lookup"><span data-stu-id="d94d8-342">Set the presenter state to paused.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d94d8-343"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart"><strong>OnClockRestart</strong></a></span><span class="sxs-lookup"><span data-stu-id="d94d8-343"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart"><strong>OnClockRestart</strong></a></span></span></td>
<td><span data-ttu-id="d94d8-344">視為與 <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a> 相同，但不會排清範例的佇列。</span><span class="sxs-lookup"><span data-stu-id="d94d8-344">Treat the same as <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a> but do not flush the queue of samples.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d94d8-345"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate"><strong>OnClockSetRate</strong></a></span><span class="sxs-lookup"><span data-stu-id="d94d8-345"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate"><strong>OnClockSetRate</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="d94d8-346">如果速率從0變更為非零值，則取消框架逐步執行。</span><span class="sxs-lookup"><span data-stu-id="d94d8-346">If the rate is changing from zero to nonzero, cancel frame stepping.</span></span></li>
<li><span data-ttu-id="d94d8-347">儲存新的時脈速率。</span><span class="sxs-lookup"><span data-stu-id="d94d8-347">Store the new clock rate.</span></span> <span data-ttu-id="d94d8-348">顯示樣本時，頻率會受到影響。</span><span class="sxs-lookup"><span data-stu-id="d94d8-348">The clock rate affects when samples are presented.</span></span> <span data-ttu-id="d94d8-349">如需詳細資訊，請參閱 <a href="#scheduling-samples">排程範例</a>。</span><span class="sxs-lookup"><span data-stu-id="d94d8-349">For more information, see <a href="#scheduling-samples">Scheduling Samples</a>.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="implementing-imfratesupport"></a><span data-ttu-id="d94d8-350">執行 IMFRateSupport</span><span class="sxs-lookup"><span data-stu-id="d94d8-350">Implementing IMFRateSupport</span></span>

<span data-ttu-id="d94d8-351">若要支援1×速度以外的播放率，展示者必須執行 [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) 介面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-351">To support playback rates other than 1× speed, the presenter must implement the [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) interface.</span></span> <span data-ttu-id="d94d8-352">以下是在此介面中執行方法的一些指導方針。</span><span class="sxs-lookup"><span data-stu-id="d94d8-352">Here are some guidelines for implementing the methods in this interface.</span></span> <span data-ttu-id="d94d8-353">在展示者關閉之後，所有方法都應該會失敗。</span><span class="sxs-lookup"><span data-stu-id="d94d8-353">All of the methods should fail after the presenter is shut down.</span></span> <span data-ttu-id="d94d8-354">如需此介面的詳細資訊，請參閱 [速率控制](rate-control.md)。</span><span class="sxs-lookup"><span data-stu-id="d94d8-354">For more information about this interface, see [Rate Control](rate-control.md).</span></span>



| <span data-ttu-id="d94d8-355">值</span><span class="sxs-lookup"><span data-stu-id="d94d8-355">Value</span></span>                                                          | <span data-ttu-id="d94d8-356">描述</span><span class="sxs-lookup"><span data-stu-id="d94d8-356">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d94d8-357">**GetSlowestRate**</span><span class="sxs-lookup"><span data-stu-id="d94d8-357">**GetSlowestRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate)   | <span data-ttu-id="d94d8-358">傳回零以指出沒有最小的播放速率。</span><span class="sxs-lookup"><span data-stu-id="d94d8-358">Return zero to indicate no minimum playback rate.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="d94d8-359">**GetFastestRate**</span><span class="sxs-lookup"><span data-stu-id="d94d8-359">**GetFastestRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)   | <span data-ttu-id="d94d8-360">若為非 thinned 播放，播放速率不應超過監視器的重新整理頻率：*最大速率* 重新整理  =  *頻率* (Hz) /*影片畫面播放速率* (fps) 。</span><span class="sxs-lookup"><span data-stu-id="d94d8-360">For non-thinned playback, the playback rate should not exceed the refresh rate of the monitor: *maximum rate* = *refresh rate* (Hz) / *video frame rate* (fps).</span></span> <span data-ttu-id="d94d8-361">影片畫面播放速率是在展示者的媒體類型中指定。</span><span class="sxs-lookup"><span data-stu-id="d94d8-361">The video frame rate is specified in the presenter's media type.</span></span> <br/> <span data-ttu-id="d94d8-362">針對 thinned 播放，播放速率為未系結;傳回 **FLT_MAX** 的值。</span><span class="sxs-lookup"><span data-stu-id="d94d8-362">For thinned playback, the playback rate is unbounded; return the value **FLT_MAX**.</span></span> <span data-ttu-id="d94d8-363">在實務上，來源和解碼器將會是 thinned 播放期間的限制因素。</span><span class="sxs-lookup"><span data-stu-id="d94d8-363">In practice, the source and the decoder will be the limiting factors during thinned playback.</span></span> <br/> <span data-ttu-id="d94d8-364">針對反向播放，傳回最大速率的負數。</span><span class="sxs-lookup"><span data-stu-id="d94d8-364">For reverse playback, return the negative of the maximum rate.</span></span><br/> |
| [<span data-ttu-id="d94d8-365">**IsRateSupported**</span><span class="sxs-lookup"><span data-stu-id="d94d8-365">**IsRateSupported**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) | <span data-ttu-id="d94d8-366">如果 *flRate* 的絕對值超過展示者的播放速率上限，則傳回 **MF_E_UNSUPPORTED_RATE** 。</span><span class="sxs-lookup"><span data-stu-id="d94d8-366">Return **MF_E_UNSUPPORTED_RATE** if the absolute value of *flRate* exceeds the presenter's maximum playback rate.</span></span> <span data-ttu-id="d94d8-367">計算 [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)所述的最大播放速率。</span><span class="sxs-lookup"><span data-stu-id="d94d8-367">Calculate the maximum playback rate as described for [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate).</span></span>                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="d94d8-368">下列範例顯示如何執行 [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate) 方法：</span><span class="sxs-lookup"><span data-stu-id="d94d8-368">The following example shows how to implement the [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate) method:</span></span>


```C++
float EVRCustomPresenter::GetMaxRate(BOOL bThin)
{
    // Non-thinned:
    // If we have a valid frame rate and a monitor refresh rate, the maximum
    // playback rate is equal to the refresh rate. Otherwise, the maximum rate
    // is unbounded (FLT_MAX).

    // Thinned: The maximum rate is unbounded.

    float   fMaxRate = FLT_MAX;
    MFRatio fps = { 0, 0 };
    UINT    MonitorRateHz = 0;

    if (!bThin && (m_pMediaType != NULL))
    {
        GetFrameRate(m_pMediaType, &fps);
        MonitorRateHz = m_pD3DPresentEngine->RefreshRate();

        if (fps.Denominator && fps.Numerator && MonitorRateHz)
        {
            // Max Rate = Refresh Rate / Frame Rate
            fMaxRate = (float)MulDiv(
                MonitorRateHz, fps.Denominator, fps.Numerator);
        }
    }

    return fMaxRate;
}
```



<span data-ttu-id="d94d8-369">先前的範例會呼叫 helper 方法 GetMaxRate，以計算最大的向前播放速率：</span><span class="sxs-lookup"><span data-stu-id="d94d8-369">The previous example calls a helper method, GetMaxRate, to calculate the maximum forward playback rate:</span></span>

<span data-ttu-id="d94d8-370">下列範例顯示如何執行 [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) 方法：</span><span class="sxs-lookup"><span data-stu-id="d94d8-370">The following example shows how to implement the [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) method:</span></span>


```C++
HRESULT EVRCustomPresenter::IsRateSupported(
    BOOL bThin,
    float fRate,
    float *pfNearestSupportedRate
    )
{
    EnterCriticalSection(&m_ObjectLock);

    float   fMaxRate = 0.0f;
    float   fNearestRate = fRate;  // If we support fRate, that is the nearest.

    HRESULT hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    // Find the maximum forward rate.
    // Note: We have no minimum rate (that is, we support anything down to 0).
    fMaxRate = GetMaxRate(bThin);

    if (fabsf(fRate) > fMaxRate)
    {
        // The (absolute) requested rate exceeds the maximum rate.
        hr = MF_E_UNSUPPORTED_RATE;

        // The nearest supported rate is fMaxRate.
        fNearestRate = fMaxRate;
        if (fRate < 0)
        {
            // Negative for reverse playback.
            fNearestRate = -fNearestRate;
        }
    }

    // Return the nearest supported rate.
    if (pfNearestSupportedRate != NULL)
    {
        *pfNearestSupportedRate = fNearestRate;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



### <a name="sending-events-to-the-evr"></a><span data-ttu-id="d94d8-371">將事件傳送至 EVR</span><span class="sxs-lookup"><span data-stu-id="d94d8-371">Sending Events to the EVR</span></span>

<span data-ttu-id="d94d8-372">展示者必須通知 EVR 各種事件。</span><span class="sxs-lookup"><span data-stu-id="d94d8-372">The presenter must notify the EVR of various events.</span></span> <span data-ttu-id="d94d8-373">若要這樣做，它會使用 EVR 的 [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) 介面，此介面會在 EVR 呼叫展示者的 [**IMFTopologyServiceLookupClient：： InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) 方法時取得。</span><span class="sxs-lookup"><span data-stu-id="d94d8-373">To do so, it uses the EVR's [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) interface, obtained when the EVR calls the presenter's [**IMFTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) method.</span></span> <span data-ttu-id="d94d8-374"> (**IMediaEventSink** 介面最初是一個 directshow 介面，但用於 directshow EVR 和媒體基礎。 ) 下列程式碼示範如何將事件傳送到 EVR：</span><span class="sxs-lookup"><span data-stu-id="d94d8-374">(The **IMediaEventSink** interface is originally a DirectShow interface, but is used in both the DirectShow EVR and the Media Foundation.) The following code shows how to send an event to the EVR:</span></span>


```C++
    // NotifyEvent: Send an event to the EVR through its IMediaEventSink interface.
    void NotifyEvent(long EventCode, LONG_PTR Param1, LONG_PTR Param2)
    {
        if (m_pMediaEventSink)
        {
            m_pMediaEventSink->Notify(EventCode, Param1, Param2);
        }
    }
```



<span data-ttu-id="d94d8-375">下表列出展示者所傳送的事件，以及事件參數。</span><span class="sxs-lookup"><span data-stu-id="d94d8-375">The following table lists the events that the presenter sends, along with the event parameters.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d94d8-376">事件</span><span class="sxs-lookup"><span data-stu-id="d94d8-376">Event</span></span></th>
<th><span data-ttu-id="d94d8-377">描述</span><span class="sxs-lookup"><span data-stu-id="d94d8-377">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d94d8-378"><a href="/windows/desktop/DirectShow/ec-complete"><strong>EC_COMPLETE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d94d8-378"><a href="/windows/desktop/DirectShow/ec-complete"><strong>EC_COMPLETE</strong></a></span></span></td>
<td><span data-ttu-id="d94d8-379">展示者已完成 MFVP_MESSAGE_ENDOFSTREAM 訊息之後的所有畫面格轉譯。</span><span class="sxs-lookup"><span data-stu-id="d94d8-379">The presenter has finished rendering all frames after the MFVP_MESSAGE_ENDOFSTREAM message.</span></span><br/>
<ul>
<li><span data-ttu-id="d94d8-380"><em>Param1</em>： HRESULT，指出作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="d94d8-380"><em>Param1</em>: HRESULT indicating the status of the operation.</span></span></li>
<li><span data-ttu-id="d94d8-381"><em>Param2</em>：未使用。</span><span class="sxs-lookup"><span data-stu-id="d94d8-381"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="d94d8-382">如需詳細資訊，請參閱 <a href="#end-of-stream">資料流程的結尾</a>。</span><span class="sxs-lookup"><span data-stu-id="d94d8-382">For more information, see <a href="#end-of-stream">End of Stream</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d94d8-383"><a href="/windows/desktop/DirectShow/ec-display-changed"><strong>EC_DISPLAY_CHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="d94d8-383"><a href="/windows/desktop/DirectShow/ec-display-changed"><strong>EC_DISPLAY_CHANGED</strong></a></span></span></td>
<td><span data-ttu-id="d94d8-384">Direct3D 裝置已變更。</span><span class="sxs-lookup"><span data-stu-id="d94d8-384">The Direct3D device has changed.</span></span><br/>
<ul>
<li><span data-ttu-id="d94d8-385"><em>Param1</em>：未使用。</span><span class="sxs-lookup"><span data-stu-id="d94d8-385"><em>Param1</em>: Not used.</span></span></li>
<li><span data-ttu-id="d94d8-386"><em>Param2</em>：未使用。</span><span class="sxs-lookup"><span data-stu-id="d94d8-386"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="d94d8-387">如需詳細資訊，請參閱 <a href="#managing-the-direct3d-device">管理 Direct3D 裝置</a>。</span><span class="sxs-lookup"><span data-stu-id="d94d8-387">For more information, see <a href="#managing-the-direct3d-device">Managing the Direct3D Device</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d94d8-388"><a href="/windows/desktop/DirectShow/ec-errorabort"><strong>EC_ERRORABORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d94d8-388"><a href="/windows/desktop/DirectShow/ec-errorabort"><strong>EC_ERRORABORT</strong></a></span></span></td>
<td><span data-ttu-id="d94d8-389">發生錯誤，需要串流處理停止。</span><span class="sxs-lookup"><span data-stu-id="d94d8-389">An error has occurred that requires streaming to stop.</span></span><br/>
<ul>
<li><span data-ttu-id="d94d8-390"><em>Param1</em>： <strong>HRESULT</strong> ，表示發生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="d94d8-390"><em>Param1</em>: <strong>HRESULT</strong> indicating the error that occurred.</span></span></li>
<li><span data-ttu-id="d94d8-391"><em>Param2</em>：未使用。</span><span class="sxs-lookup"><span data-stu-id="d94d8-391"><em>Param2</em>: Not used.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d94d8-392"><a href="/windows/desktop/DirectShow/ec-processing-latency"><strong>EC_PROCESSING_LATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="d94d8-392"><a href="/windows/desktop/DirectShow/ec-processing-latency"><strong>EC_PROCESSING_LATENCY</strong></a></span></span></td>
<td><span data-ttu-id="d94d8-393">指定展示者花在轉譯每個畫面格的時間量。</span><span class="sxs-lookup"><span data-stu-id="d94d8-393">Specifies the amount of time that the presenter is taking to render each frame.</span></span> <span data-ttu-id="d94d8-394">(選擇性。)</span><span class="sxs-lookup"><span data-stu-id="d94d8-394">(Optional.)</span></span><br/>
<ul>
<li><span data-ttu-id="d94d8-395"><em>Param1</em>：常數 <strong>LONGLONG</strong> 值的指標，其中包含處理框架的時間長度（以 100-毫微秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d94d8-395"><em>Param1</em>: Pointer to a constant <strong>LONGLONG</strong> value that contains the amount of time to process the frame, in 100-nanosecond units.</span></span></li>
<li><span data-ttu-id="d94d8-396"><em>Param2</em>：未使用。</span><span class="sxs-lookup"><span data-stu-id="d94d8-396"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="d94d8-397">如需詳細資訊，請參閱 <a href="#processing-output">處理輸出</a>。</span><span class="sxs-lookup"><span data-stu-id="d94d8-397">For more information, see <a href="#processing-output">Processing Output</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d94d8-398"><a href="/windows/desktop/DirectShow/ec-sample-latency"><strong>EC_SAMPLE_LATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="d94d8-398"><a href="/windows/desktop/DirectShow/ec-sample-latency"><strong>EC_SAMPLE_LATENCY</strong></a></span></span></td>
<td><span data-ttu-id="d94d8-399">在轉譯範例中指定目前的延隔時間。</span><span class="sxs-lookup"><span data-stu-id="d94d8-399">Specifies the current lag time in rendering samples.</span></span> <span data-ttu-id="d94d8-400">如果此值為正數，則樣本會落後排程。</span><span class="sxs-lookup"><span data-stu-id="d94d8-400">If the value is positive, samples are behind schedule.</span></span> <span data-ttu-id="d94d8-401">如果值為負數，則範例會提前排程。</span><span class="sxs-lookup"><span data-stu-id="d94d8-401">If the value is negative, samples are ahead of schedule.</span></span> <span data-ttu-id="d94d8-402">(選擇性。)</span><span class="sxs-lookup"><span data-stu-id="d94d8-402">(Optional.)</span></span><br/>
<ul>
<li><span data-ttu-id="d94d8-403"><em>Param1</em>：常數 <strong>LONGLONG</strong> 值的指標，其中包含延隔時間（100-毫微秒單位）。</span><span class="sxs-lookup"><span data-stu-id="d94d8-403"><em>Param1</em>: Pointer to a constant <strong>LONGLONG</strong> value that contains the lag time, in 100-nanosecond units.</span></span></li>
<li><span data-ttu-id="d94d8-404"><em>Param2</em>：未使用。</span><span class="sxs-lookup"><span data-stu-id="d94d8-404"><em>Param2</em>: Not used.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d94d8-405"><a href="/windows/desktop/DirectShow/ec-scrub-time"><strong>EC_SCRUB_TIME</strong></a></span><span class="sxs-lookup"><span data-stu-id="d94d8-405"><a href="/windows/desktop/DirectShow/ec-scrub-time"><strong>EC_SCRUB_TIME</strong></a></span></span></td>
<td><span data-ttu-id="d94d8-406">如果播放率為零，則會在 <strong>EC_STEP_COMPLETE</strong> 後立即傳送。</span><span class="sxs-lookup"><span data-stu-id="d94d8-406">Sent immediately after <strong>EC_STEP_COMPLETE</strong> if the playback rate is zero.</span></span> <span data-ttu-id="d94d8-407">此事件包含所顯示框架的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="d94d8-407">This event contains the time stamp of the frame that was displayed.</span></span><br/>
<ul>
<li><span data-ttu-id="d94d8-408"><em>Param1</em>：時間戳記的較低32位。</span><span class="sxs-lookup"><span data-stu-id="d94d8-408"><em>Param1</em>: Lower 32 bits of the time stamp.</span></span></li>
<li><span data-ttu-id="d94d8-409"><em>Param2</em>：時間戳記的上方32位。</span><span class="sxs-lookup"><span data-stu-id="d94d8-409"><em>Param2</em>: Upper 32 bits of the time stamp.</span></span></li>
</ul>
<span data-ttu-id="d94d8-410">如需詳細資訊，請參閱 <a href="#frame-stepping">框架逐步執行</a>。</span><span class="sxs-lookup"><span data-stu-id="d94d8-410">For more information, see <a href="#frame-stepping">Frame Stepping</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d94d8-411"><a href="/windows/desktop/DirectShow/ec-step-complete"><strong>EC_STEP_COMPLETE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d94d8-411"><a href="/windows/desktop/DirectShow/ec-step-complete"><strong>EC_STEP_COMPLETE</strong></a></span></span></td>
<td><span data-ttu-id="d94d8-412">展示者已完成或取消框架步驟。</span><span class="sxs-lookup"><span data-stu-id="d94d8-412">The presenter has completed or canceled a frame step.</span></span><br/>
<ul>
<li><span data-ttu-id="d94d8-413"><em>Param1</em>：未使用。</span><span class="sxs-lookup"><span data-stu-id="d94d8-413"><em>Param1</em>: Not used.</span></span></li>
<li><span data-ttu-id="d94d8-414"><em>Param2</em>：未使用。</span><span class="sxs-lookup"><span data-stu-id="d94d8-414"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="d94d8-415">如需詳細資訊，請參閱 <a href="#frame-stepping">框架逐步執行</a>。</span><span class="sxs-lookup"><span data-stu-id="d94d8-415">For more information, see <a href="#frame-stepping">Frame Stepping</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d94d8-416">先前版本的檔所述的 <em>Param1</em> 不正確。</span><span class="sxs-lookup"><span data-stu-id="d94d8-416">A previous version of the documentation described <em>Param1</em> incorrectly.</span></span> <span data-ttu-id="d94d8-417">此參數不適用於此事件。</span><span class="sxs-lookup"><span data-stu-id="d94d8-417">This parameter is not used for this event.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="negotiating-formats"></a><span data-ttu-id="d94d8-418">協商格式</span><span class="sxs-lookup"><span data-stu-id="d94d8-418">Negotiating Formats</span></span>

<span data-ttu-id="d94d8-419">每當展示者收到來自 EVR 的 **MFVP_MESSAGE_INVALIDATEMEDIATYPE** 訊息時，就必須在混音器上設定輸出格式，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d94d8-419">Whenever the presenter receives an **MFVP_MESSAGE_INVALIDATEMEDIATYPE** message from the EVR, it must set the output format on the mixer, as follows:</span></span>

1.  <span data-ttu-id="d94d8-420">在混音器上呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) ，以取得可能的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="d94d8-420">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) on the mixer to get a possible output type.</span></span> <span data-ttu-id="d94d8-421">此類型描述混音器可產生的格式，並提供圖形裝置的輸入資料流程和影片處理功能。</span><span class="sxs-lookup"><span data-stu-id="d94d8-421">This type describes a format that the mixer can produce given the input streams and the video processing capabilities of the graphics device.</span></span>
2.  <span data-ttu-id="d94d8-422">檢查展示者是否可以使用此媒體類型作為轉譯格式。</span><span class="sxs-lookup"><span data-stu-id="d94d8-422">Check whether the presenter can use this media type as its rendering format.</span></span> <span data-ttu-id="d94d8-423">以下是要檢查的一些事項，雖然您的執行可能有自己的需求：</span><span class="sxs-lookup"><span data-stu-id="d94d8-423">Here are some things to check, although your implementation might have its own requirements:</span></span>

    -   <span data-ttu-id="d94d8-424">影片必須未壓縮。</span><span class="sxs-lookup"><span data-stu-id="d94d8-424">The video must be uncompressed.</span></span>
    -   <span data-ttu-id="d94d8-425">影片必須只有漸進式框架。</span><span class="sxs-lookup"><span data-stu-id="d94d8-425">The video must have progressive frames only.</span></span> <span data-ttu-id="d94d8-426">檢查 [**MF_MT_INTERLACE_MODE**](mf-mt-interlace-mode-attribute.md) 屬性是否等於 **MFVideoInterlace_Progressive**。</span><span class="sxs-lookup"><span data-stu-id="d94d8-426">Check that the [**MF_MT_INTERLACE_MODE**](mf-mt-interlace-mode-attribute.md) attribute equals **MFVideoInterlace_Progressive**.</span></span>
    -   <span data-ttu-id="d94d8-427">格式必須與 Direct3D 裝置相容。</span><span class="sxs-lookup"><span data-stu-id="d94d8-427">The format must be compatible with the Direct3D device.</span></span>

    <span data-ttu-id="d94d8-428">如果類型無法接受，請返回步驟1，並取得混音器下一個建議的類型。</span><span class="sxs-lookup"><span data-stu-id="d94d8-428">If the type is not acceptable, return to step 1 and get the mixer's next proposed type.</span></span>

3.  <span data-ttu-id="d94d8-429">建立新的媒體類型，它是原始類型的複製，然後變更下列屬性：</span><span class="sxs-lookup"><span data-stu-id="d94d8-429">Create a new media type that is a clone of the original type and then change the following attributes:</span></span>

    -   <span data-ttu-id="d94d8-430">將 [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) 屬性設定為等於您要配置之 Direct3D 介面的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="d94d8-430">Set the [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) attribute equal to the width and height that you want for the Direct3D surfaces you will allocate.</span></span>
    -   <span data-ttu-id="d94d8-431">將 [ [**MF_MT_PAN_SCAN_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) ] 屬性設定為 [ **FALSE**]。</span><span class="sxs-lookup"><span data-stu-id="d94d8-431">Set the [**MF_MT_PAN_SCAN_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) attribute to **FALSE**.</span></span>
    -   <span data-ttu-id="d94d8-432">將 [**MF_MT_PIXEL_ASPECT_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) 屬性設定為等於顯示 (通常是 1:1) 。</span><span class="sxs-lookup"><span data-stu-id="d94d8-432">Set the [**MF_MT_PIXEL_ASPECT_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) attribute equal to the PAR of the display (typically 1:1).</span></span>
    -   <span data-ttu-id="d94d8-433">將幾何光圈 ([**MF_MT_GEOMETRIC_APERTURE**](mf-mt-geometric-aperture-attribute.md) 屬性) 等於 Direct3D 介面內的矩形。</span><span class="sxs-lookup"><span data-stu-id="d94d8-433">Set the geometric aperture ([**MF_MT_GEOMETRIC_APERTURE**](mf-mt-geometric-aperture-attribute.md) attribute) equal to a rectangle within the Direct3D surface.</span></span> <span data-ttu-id="d94d8-434">當混音器產生輸出框架時，它會 blits 來源影像至此矩形。</span><span class="sxs-lookup"><span data-stu-id="d94d8-434">When the mixer generates an output frame, it blits the source image onto this rectangle.</span></span> <span data-ttu-id="d94d8-435">幾何光圈可以像表面一樣大，也可以是表面內的 subrectangle。</span><span class="sxs-lookup"><span data-stu-id="d94d8-435">The geometric aperture can be as large as the surface, or it can be a subrectangle within the surface.</span></span> <span data-ttu-id="d94d8-436">如需詳細資訊，請參閱 [來源和目的地矩形](#source-and-destination-rectangles)。</span><span class="sxs-lookup"><span data-stu-id="d94d8-436">For more information, see [Source and Destination Rectangles](#source-and-destination-rectangles).</span></span>

4.  <span data-ttu-id="d94d8-437">若要測試混音器是否會接受修改過的輸出類型，請使用 **MFT_SET_TYPE_TEST_ONLY** 旗標來呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) 。</span><span class="sxs-lookup"><span data-stu-id="d94d8-437">To test whether the mixer will accept the modified output type, call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) with the **MFT_SET_TYPE_TEST_ONLY** flag.</span></span> <span data-ttu-id="d94d8-438">如果混音器拒絕該類型，請返回步驟1，並取得下一個類型。</span><span class="sxs-lookup"><span data-stu-id="d94d8-438">If the mixer rejects the type, go back to step 1 and get the next type.</span></span>
5.  <span data-ttu-id="d94d8-439">配置 direct3d 表面的集區，如配置 [direct3d](#allocating-direct3d-surfaces)介面中所述。</span><span class="sxs-lookup"><span data-stu-id="d94d8-439">Allocate a pool of Direct3D surfaces, as described in [Allocating Direct3D Surfaces](#allocating-direct3d-surfaces).</span></span> <span data-ttu-id="d94d8-440">混音器會在繪製合成的影片框架時使用這些表面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-440">The mixer will use these surfaces when it draws the composited video frames.</span></span>
6.  <span data-ttu-id="d94d8-441">藉由呼叫 [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) （沒有旗標）來設定混音器上的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="d94d8-441">Set the output type on the mixer by calling [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) with no flags.</span></span> <span data-ttu-id="d94d8-442">如果在步驟4中第一次呼叫 **SetOutputType** 成功，此方法應該會再次成功。</span><span class="sxs-lookup"><span data-stu-id="d94d8-442">If the first call to **SetOutputType** succeeded in step 4, the method should succeed again.</span></span>

<span data-ttu-id="d94d8-443">如果混音器的類型不足， [**GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) 方法會傳回 **MF_E_NO_MORE_TYPES**。</span><span class="sxs-lookup"><span data-stu-id="d94d8-443">If the mixer runs out of types, the [**GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method returns **MF_E_NO_MORE_TYPES**.</span></span> <span data-ttu-id="d94d8-444">如果展示器找不到適合混音器的輸出類型，就無法轉譯資料流程。</span><span class="sxs-lookup"><span data-stu-id="d94d8-444">If the presenter cannot find a suitable output type for the mixer, the stream cannot be rendered.</span></span> <span data-ttu-id="d94d8-445">在該情況下，DirectShow 或媒體基礎可能會嘗試另一個串流格式。</span><span class="sxs-lookup"><span data-stu-id="d94d8-445">In that case, DirectShow or Media Foundation might try another stream format.</span></span> <span data-ttu-id="d94d8-446">因此，在找到有效的型別之前，展示者可能會在一個資料列中接收數 **MFVP_MESSAGE_INVALIDATEMEDIATYPE** 的訊息。</span><span class="sxs-lookup"><span data-stu-id="d94d8-446">Therefore, the presenter might receive several **MFVP_MESSAGE_INVALIDATEMEDIATYPE** messages in a row until a valid type is found.</span></span>

<span data-ttu-id="d94d8-447">混音器會自動 letterboxes 影片，將圖元外觀比例納入 (等同于來源和目的地的) 。</span><span class="sxs-lookup"><span data-stu-id="d94d8-447">The mixer automatically letterboxes the video, taking into account the pixel aspect ratio (PAR) of the source and destination.</span></span> <span data-ttu-id="d94d8-448">為了獲得最佳結果，表面寬度和高度和幾何光圈應等於您希望影片顯示在顯示器上的實際大小。</span><span class="sxs-lookup"><span data-stu-id="d94d8-448">For best results, the surface width and height and the geometric aperture should be equal to the actual size that you want the video to appear on the display.</span></span> <span data-ttu-id="d94d8-449">下圖說明此程式。</span><span class="sxs-lookup"><span data-stu-id="d94d8-449">The following image illustrates this process.</span></span>

![此圖顯示的複合 fram 會導致 direct3d 介面，此介面會導致視窗](images/b746edca-8830-4c88-aa59-0067b020d4af.gif)

<span data-ttu-id="d94d8-451">下列程式碼顯示程式的大綱。</span><span class="sxs-lookup"><span data-stu-id="d94d8-451">The following code shows the outline of the process.</span></span> <span data-ttu-id="d94d8-452">某些步驟會放在 helper 函式中，而其確切詳細資料將取決於您的展示者需求。</span><span class="sxs-lookup"><span data-stu-id="d94d8-452">Some of the steps are placed in helper functions, the exact details of which will depend on the requirements of your presenter.</span></span>


```C++
HRESULT EVRCustomPresenter::RenegotiateMediaType()
{
    HRESULT hr = S_OK;
    BOOL bFoundMediaType = FALSE;

    IMFMediaType *pMixerType = NULL;
    IMFMediaType *pOptimalType = NULL;
    IMFVideoMediaType *pVideoType = NULL;

    if (!m_pMixer)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Loop through all of the mixer's proposed output types.
    DWORD iTypeIndex = 0;
    while (!bFoundMediaType && (hr != MF_E_NO_MORE_TYPES))
    {
        SafeRelease(&pMixerType);
        SafeRelease(&pOptimalType);

        // Step 1. Get the next media type supported by mixer.
        hr = m_pMixer->GetOutputAvailableType(0, iTypeIndex++, &pMixerType);
        if (FAILED(hr))
        {
            break;
        }

        // From now on, if anything in this loop fails, try the next type,
        // until we succeed or the mixer runs out of types.

        // Step 2. Check if we support this media type.
        if (SUCCEEDED(hr))
        {
            // Note: None of the modifications that we make later in CreateOptimalVideoType
            // will affect the suitability of the type, at least for us. (Possibly for the mixer.)
            hr = IsMediaTypeSupported(pMixerType);
        }

        // Step 3. Adjust the mixer's type to match our requirements.
        if (SUCCEEDED(hr))
        {
            hr = CreateOptimalVideoType(pMixerType, &pOptimalType);
        }

        // Step 4. Check if the mixer will accept this media type.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, MFT_SET_TYPE_TEST_ONLY);
        }

        // Step 5. Try to set the media type on ourselves.
        if (SUCCEEDED(hr))
        {
            hr = SetMediaType(pOptimalType);
        }

        // Step 6. Set output media type on mixer.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, 0);

            assert(SUCCEEDED(hr)); // This should succeed unless the MFT lied in the previous call.

            // If something went wrong, clear the media type.
            if (FAILED(hr))
            {
                SetMediaType(NULL);
            }
        }

        if (SUCCEEDED(hr))
        {
            bFoundMediaType = TRUE;
        }
    }

    SafeRelease(&pMixerType);
    SafeRelease(&pOptimalType);
    SafeRelease(&pVideoType);

    return hr;
}
```



<span data-ttu-id="d94d8-453">如需影片媒體類型的詳細資訊，請參閱 [影片媒體類型](video-media-types.md)。</span><span class="sxs-lookup"><span data-stu-id="d94d8-453">For more information about video media types, see [Video Media Types](video-media-types.md).</span></span>

## <a name="managing-the-direct3d-device"></a><span data-ttu-id="d94d8-454">管理 Direct3D 裝置</span><span class="sxs-lookup"><span data-stu-id="d94d8-454">Managing the Direct3D Device</span></span>

<span data-ttu-id="d94d8-455">展示者會建立 Direct3D 裝置，並處理串流期間的任何裝置遺失。</span><span class="sxs-lookup"><span data-stu-id="d94d8-455">The presenter creates the Direct3D device and handles any device loss during streaming.</span></span> <span data-ttu-id="d94d8-456">展示者也裝載了 Direct3D 裝置管理員，可讓其他元件使用相同的裝置。</span><span class="sxs-lookup"><span data-stu-id="d94d8-456">The presenter also hosts the Direct3D device manager, which provides a way for other components to use the same device.</span></span> <span data-ttu-id="d94d8-457">例如，混音器會使用 Direct3D 裝置來混合子串流、逐行和執行色彩調整。</span><span class="sxs-lookup"><span data-stu-id="d94d8-457">For example, the mixer uses the Direct3D device to mix substreams, deinterlace, and perform color adjustments.</span></span> <span data-ttu-id="d94d8-458">您可以使用 Direct3D 裝置來進行影片加速解碼。</span><span class="sxs-lookup"><span data-stu-id="d94d8-458">Decoders can use the Direct3D device for video-accelerated decoding.</span></span> <span data-ttu-id="d94d8-459"> (如需影片加速的詳細資訊，請參閱 [DirectX Video 加速 2.0](directx-video-acceleration-2-0.md). ) </span><span class="sxs-lookup"><span data-stu-id="d94d8-459">(For more information about video acceleration, see [DirectX Video Acceleration 2.0](directx-video-acceleration-2-0.md).)</span></span>

<span data-ttu-id="d94d8-460">若要設定 Direct3D 裝置，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="d94d8-460">To set up the Direct3D device, perform the following steps:</span></span>

1.  <span data-ttu-id="d94d8-461">藉由呼叫 **Direct3DCreate9** 或 **Direct3DCreate9Ex** 來建立 Direct3D 物件。</span><span class="sxs-lookup"><span data-stu-id="d94d8-461">Create the Direct3D object by calling **Direct3DCreate9** or **Direct3DCreate9Ex**.</span></span>
2.  <span data-ttu-id="d94d8-462">藉由呼叫 **IDirect3D9：： CreateDevice** 或 **IDirect3D9Ex：： CreateDevice** 來建立裝置。</span><span class="sxs-lookup"><span data-stu-id="d94d8-462">Create the device by calling **IDirect3D9::CreateDevice** or **IDirect3D9Ex::CreateDevice**.</span></span>
3.  <span data-ttu-id="d94d8-463">藉由呼叫 [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9)來建立裝置管理員。</span><span class="sxs-lookup"><span data-stu-id="d94d8-463">Create the device manager by calling [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).</span></span>
4.  <span data-ttu-id="d94d8-464">藉由呼叫 [**IDirect3DDeviceManager9：： ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice)，在裝置管理員上設定裝置。</span><span class="sxs-lookup"><span data-stu-id="d94d8-464">Set the device on the device manager by calling [**IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span></span>

<span data-ttu-id="d94d8-465">如果另一個管線元件需要裝置管理員，它會在 EVR 上呼叫 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) ，並指定服務 GUID 的 **MR_VIDEO_ACCELERATION_SERVICE** 。</span><span class="sxs-lookup"><span data-stu-id="d94d8-465">If another pipeline component needs the device manager, it calls [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the EVR, specifying **MR_VIDEO_ACCELERATION_SERVICE** for the service GUID.</span></span> <span data-ttu-id="d94d8-466">EVR 會將要求傳送給展示者。</span><span class="sxs-lookup"><span data-stu-id="d94d8-466">The EVR passes the request to the presenter.</span></span> <span data-ttu-id="d94d8-467">物件取得 [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) 指標之後，就可以呼叫 [**IDirect3DDeviceManager9：： OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle)來取得裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d94d8-467">After the object gets the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) pointer, it can get a handle to the device by calling [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle).</span></span> <span data-ttu-id="d94d8-468">當物件需要使用裝置時，它會將裝置控制碼傳遞給 [**IDirect3DDeviceManager9：： LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) 方法，以傳回 **IDirect3DDevice9** 指標。</span><span class="sxs-lookup"><span data-stu-id="d94d8-468">When the object needs to use the device, it passes the device handle to the [**IDirect3DDeviceManager9::LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) method, which returns an **IDirect3DDevice9** pointer.</span></span>

<span data-ttu-id="d94d8-469">建立裝置之後，如果簡報者終結裝置並建立新裝置，則展示者必須再次呼叫 [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) 。</span><span class="sxs-lookup"><span data-stu-id="d94d8-469">After the device is created, if the presenter destroys the device and creates a new one, the presenter must call [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) again.</span></span> <span data-ttu-id="d94d8-470">**ResetDevice** 方法會使任何現有的裝置控制碼失效，而導致 [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice)傳回 **DXVA2_E_NEW_VIDEO_DEVICE**。</span><span class="sxs-lookup"><span data-stu-id="d94d8-470">The **ResetDevice** method invalidates any existing device handles, which causes [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) to return **DXVA2_E_NEW_VIDEO_DEVICE**.</span></span> <span data-ttu-id="d94d8-471">此錯誤碼會向其他物件發出信號，而這些物件應該會開啟新的裝置控制碼。</span><span class="sxs-lookup"><span data-stu-id="d94d8-471">This error code signals to other objects using the device that they should open a new device handle.</span></span> <span data-ttu-id="d94d8-472">如需使用 [裝置管理員] 的詳細資訊，請參閱 [Direct3D 裝置管理員](direct3d-device-manager.md)。</span><span class="sxs-lookup"><span data-stu-id="d94d8-472">For more information about using the device manager, see [Direct3D Device Manager](direct3d-device-manager.md).</span></span>

<span data-ttu-id="d94d8-473">展示者可以在視窗模式或全螢幕獨佔模式中建立裝置。</span><span class="sxs-lookup"><span data-stu-id="d94d8-473">The presenter can create the device in windowed mode or full-screen exclusive mode.</span></span> <span data-ttu-id="d94d8-474">針對視窗型模式，您應該提供方法讓應用程式指定影片視窗。</span><span class="sxs-lookup"><span data-stu-id="d94d8-474">For windowed mode, you should provide a way for the application to specify the video window.</span></span> <span data-ttu-id="d94d8-475">標準展示者會針對此用途來實行 [**IMFVideoDisplayControl：： SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) 方法。</span><span class="sxs-lookup"><span data-stu-id="d94d8-475">The standard presenter implements the [**IMFVideoDisplayControl::SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) method for this purpose.</span></span> <span data-ttu-id="d94d8-476">第一次建立展示者時，您必須建立裝置。</span><span class="sxs-lookup"><span data-stu-id="d94d8-476">You must create the device when the presenter is first created.</span></span> <span data-ttu-id="d94d8-477">一般來說，您不會知道所有的裝置參數，例如視窗或背景緩衝區格式。</span><span class="sxs-lookup"><span data-stu-id="d94d8-477">Typically, you won't know all of the device parameters at this time, such as the window or the back buffer format.</span></span> <span data-ttu-id="d94d8-478">您可以建立暫存裝置，並在稍後將它取代&\# ; 只要記得在裝置管理員上呼叫 [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) 。</span><span class="sxs-lookup"><span data-stu-id="d94d8-478">You can create a temporary device and replace it later&\#;just remember to call [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) on the device manager.</span></span>

<span data-ttu-id="d94d8-479">如果您建立新的裝置，或在現有裝置上呼叫 **IDirect3DDevice9：： Reset** 或 **IDirect3DDevice9Ex：： ResetEx** ，請將 [**EC_DISPLAY_CHANGED**](../directshow/ec-display-changed.md) 事件傳送至 EVR。</span><span class="sxs-lookup"><span data-stu-id="d94d8-479">If you create a new device, or if you call **IDirect3DDevice9::Reset** or **IDirect3DDevice9Ex::ResetEx** on an existing device, send an [**EC_DISPLAY_CHANGED**](../directshow/ec-display-changed.md) event to the EVR.</span></span> <span data-ttu-id="d94d8-480">此事件會通知 EVR 重新協商媒體類型。</span><span class="sxs-lookup"><span data-stu-id="d94d8-480">This event notifies the EVR to renegotiate the media type.</span></span> <span data-ttu-id="d94d8-481">EVR 會忽略這個事件的事件參數。</span><span class="sxs-lookup"><span data-stu-id="d94d8-481">The EVR ignores the event parameters for this event.</span></span>

### <a name="allocating-direct3d-surfaces"></a><span data-ttu-id="d94d8-482">配置 Direct3D 表面</span><span class="sxs-lookup"><span data-stu-id="d94d8-482">Allocating Direct3D Surfaces</span></span>

<span data-ttu-id="d94d8-483">在展示者設定媒體類型之後，它就可以配置用來寫入影片畫面的 Direct3D 表面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-483">After the presenter sets the media type, it can allocate the Direct3D surfaces, which the mixer will use to write the video frames.</span></span> <span data-ttu-id="d94d8-484">介面必須符合展示者的媒體類型：</span><span class="sxs-lookup"><span data-stu-id="d94d8-484">The surface must match the presenter's media type:</span></span>

-   <span data-ttu-id="d94d8-485">介面格式必須符合媒體子類型。</span><span class="sxs-lookup"><span data-stu-id="d94d8-485">The surface format must match the media subtype.</span></span> <span data-ttu-id="d94d8-486">例如，如果 **MFVideoFormat_RGB24** 子類型，則必須將介面格式 **D3DFMT_X8R8G8B8**。</span><span class="sxs-lookup"><span data-stu-id="d94d8-486">For example, if the subtype is **MFVideoFormat_RGB24**, the surface format must be **D3DFMT_X8R8G8B8**.</span></span> <span data-ttu-id="d94d8-487">如需子類型和 Direct3D 格式的詳細資訊，請參閱 [影片子類型 guid](video-subtype-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="d94d8-487">For more information about subtypes and Direct3D formats, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>
-   <span data-ttu-id="d94d8-488">介面寬度和高度必須符合媒體類型的 [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) 屬性中所提供的尺寸。</span><span class="sxs-lookup"><span data-stu-id="d94d8-488">The surface width and height must match the dimensions given in the [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) attribute of the media type.</span></span>

<span data-ttu-id="d94d8-489">配置介面的建議方式，取決於簡報者是否以視窗方式執行或全螢幕。</span><span class="sxs-lookup"><span data-stu-id="d94d8-489">The recommended way to allocate surfaces depends on whether the presenter runs windowed or full-screen.</span></span>

<span data-ttu-id="d94d8-490">如果 Direct3D 裝置在視窗中，您可以建立數個交換鏈，每個都有一個返回緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d94d8-490">If the Direct3D device is windowed, you can create several swap chains, each with a single back buffer.</span></span> <span data-ttu-id="d94d8-491">使用這種方法，您可以單獨呈現每個介面，因為呈現一個交換鏈不會干擾其他交換鏈。</span><span class="sxs-lookup"><span data-stu-id="d94d8-491">Using this approach, you can present each surface independently, because presenting one swap chain will not interfere with the other swap chains.</span></span> <span data-ttu-id="d94d8-492">混音器可以將資料寫入介面，而另一個表面則是針對簡報進行排程。</span><span class="sxs-lookup"><span data-stu-id="d94d8-492">The mixer can write data to a surface while another surface is scheduled for presentation.</span></span>

<span data-ttu-id="d94d8-493">首先，決定要建立多少個交換鏈。</span><span class="sxs-lookup"><span data-stu-id="d94d8-493">First, decide how many swap chains to create.</span></span> <span data-ttu-id="d94d8-494">建議最少3個。</span><span class="sxs-lookup"><span data-stu-id="d94d8-494">A minimum of three is recommended.</span></span> <span data-ttu-id="d94d8-495">針對每個交換鏈，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="d94d8-495">For each swap chain, do the following:</span></span>

1.  <span data-ttu-id="d94d8-496">呼叫 **IDirect3DDevice9：： CreateAdditionalSwapChain** 來建立交換鏈。</span><span class="sxs-lookup"><span data-stu-id="d94d8-496">Call **IDirect3DDevice9::CreateAdditionalSwapChain** to create the swap chain.</span></span>
2.  <span data-ttu-id="d94d8-497">呼叫 **IDirect3DSwapChain9：： GetBackBuffer** ，以取得交換鏈的背景緩衝區介面指標。</span><span class="sxs-lookup"><span data-stu-id="d94d8-497">Call **IDirect3DSwapChain9::GetBackBuffer** to get a pointer to the swap chain's back buffer surface.</span></span>
3.  <span data-ttu-id="d94d8-498">呼叫 [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) 並傳入介面指標。</span><span class="sxs-lookup"><span data-stu-id="d94d8-498">Call [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) and pass in a pointer to the surface.</span></span> <span data-ttu-id="d94d8-499">此函式會傳回影片範例物件的指標。</span><span class="sxs-lookup"><span data-stu-id="d94d8-499">This function returns a pointer to a video sample object.</span></span> <span data-ttu-id="d94d8-500">影片範例物件會實 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面，而展示者會使用這個介面，在展示者呼叫混音器的 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 方法時，將表面傳遞給混音器。</span><span class="sxs-lookup"><span data-stu-id="d94d8-500">The video sample object implements the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, and the presenter uses this interface to deliver the surface to the mixer when the presenter calls the mixer's [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method.</span></span> <span data-ttu-id="d94d8-501">如需影片範例物件的詳細資訊，請參閱 [影片範例](video-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="d94d8-501">For more information about the video sample object, see [Video Samples](video-samples.md).</span></span>
4.  <span data-ttu-id="d94d8-502">將 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 指標儲存在佇列中。</span><span class="sxs-lookup"><span data-stu-id="d94d8-502">Store the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointer in a queue.</span></span> <span data-ttu-id="d94d8-503">在處理期間，展示者會從這個佇列提取範例，如 [處理輸出](#processing-output)中所述。</span><span class="sxs-lookup"><span data-stu-id="d94d8-503">The presenter will pull samples from this queue during processing as described in [Processing Output](#processing-output).</span></span>
5.  <span data-ttu-id="d94d8-504">保留 **IDirect3DSwapChain9** 指標的參考，因此不會釋放交換鏈。</span><span class="sxs-lookup"><span data-stu-id="d94d8-504">Keep a reference to the **IDirect3DSwapChain9** pointer so the swap chain is not released.</span></span>

<span data-ttu-id="d94d8-505">在全螢幕專屬模式中，裝置不能有一個以上的交換鏈。</span><span class="sxs-lookup"><span data-stu-id="d94d8-505">In full-screen exclusive mode, the device cannot have more than one swap chain.</span></span> <span data-ttu-id="d94d8-506">當您建立全螢幕裝置時，會隱含地建立此交換鏈。</span><span class="sxs-lookup"><span data-stu-id="d94d8-506">This swap chain is created implicitly when you create the full-screen device.</span></span> <span data-ttu-id="d94d8-507">交換鏈可以有一個以上的背景緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d94d8-507">The swap chain can have more than one back buffer.</span></span> <span data-ttu-id="d94d8-508">但是，如果您在相同的交換鏈中寫入至另一個背景緩衝區時顯示一個後置緩衝區，則沒有任何簡單的方法可協調這兩個作業。</span><span class="sxs-lookup"><span data-stu-id="d94d8-508">Unfortunately, however, if you present one back buffer while you write to another back buffer in the same swap chain, there is no easy way to coordinate the two operations.</span></span> <span data-ttu-id="d94d8-509">這是因為 Direct3D 執行介面翻轉的方式。</span><span class="sxs-lookup"><span data-stu-id="d94d8-509">This is because of the way Direct3D implements surface flipping.</span></span> <span data-ttu-id="d94d8-510">當您呼叫存在時，圖形驅動程式會更新圖形記憶體中的介面指標。</span><span class="sxs-lookup"><span data-stu-id="d94d8-510">When you call Present, the graphics driver updates the surface pointers in graphics memory.</span></span> <span data-ttu-id="d94d8-511">如果您在呼叫時保留任何 **IDirect3DSurface9** 指標，則會在 **目前\*\*\*\*的呼叫傳回** 之後，指向不同的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d94d8-511">If you are holding any **IDirect3DSurface9** pointers when you call **Present**, they will point to different buffers after the **Present** call returns.</span></span>

<span data-ttu-id="d94d8-512">最簡單的選項是建立一個交換鏈的影片範例。</span><span class="sxs-lookup"><span data-stu-id="d94d8-512">The simplest option is to create one video sample for the swap chain.</span></span> <span data-ttu-id="d94d8-513">如果您選擇此選項，請遵循針對視窗型模式所提供的相同步驟。</span><span class="sxs-lookup"><span data-stu-id="d94d8-513">If you choose this option, follow the same steps given for windowed mode.</span></span> <span data-ttu-id="d94d8-514">唯一的差別在於範例佇列包含單一影片範例。</span><span class="sxs-lookup"><span data-stu-id="d94d8-514">The only difference is that the sample queue contains a single video sample.</span></span> <span data-ttu-id="d94d8-515">另一個選項是建立螢幕上的介面，然後將它們 array.blit 至背景緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d94d8-515">Another option is to create offscreen surfaces and then blit them to the back buffer.</span></span> <span data-ttu-id="d94d8-516">您所建立的表面必須支援 [**IDirectXVideoProcessor：： VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) 方法，混音器會使用此方法來複合輸出畫面格。</span><span class="sxs-lookup"><span data-stu-id="d94d8-516">The surfaces that you create must support the [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) method, which the mixer uses to composite the output frames.</span></span>

### <a name="tracking-samples"></a><span data-ttu-id="d94d8-517">追蹤範例</span><span class="sxs-lookup"><span data-stu-id="d94d8-517">Tracking Samples</span></span>

<span data-ttu-id="d94d8-518">當展示者第一次配置影片範例時，它會將它們放在佇列中。</span><span class="sxs-lookup"><span data-stu-id="d94d8-518">When the presenter first allocates the video samples, it places them in a queue.</span></span> <span data-ttu-id="d94d8-519">當展示者需要從混音器取得新的框架時，就會從此佇列中繪製。</span><span class="sxs-lookup"><span data-stu-id="d94d8-519">The presenter draws from this queue whenever it needs to get a new frame from the mixer.</span></span> <span data-ttu-id="d94d8-520">在混音器輸出框架之後，展示者會將範例移至第二個佇列。</span><span class="sxs-lookup"><span data-stu-id="d94d8-520">After the mixer outputs the frame, the presenter moves the sample into a second queue.</span></span> <span data-ttu-id="d94d8-521">第二個佇列適用于等待排程的呈現時間的範例。</span><span class="sxs-lookup"><span data-stu-id="d94d8-521">The second queue is for samples that are waiting for their scheduled presentation times.</span></span>

<span data-ttu-id="d94d8-522">為了讓您更輕鬆地追蹤每個範例的狀態，影片範例物件會執行 [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) 介面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-522">To make it easier to track the status of each sample, the video sample object implements the [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) interface.</span></span> <span data-ttu-id="d94d8-523">您可以使用此介面，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d94d8-523">You can use this interface as follows:</span></span>

1.  <span data-ttu-id="d94d8-524">在您的展示者中執行 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-524">Implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface in your presenter.</span></span>
2.  <span data-ttu-id="d94d8-525">在排程的佇列中放置範例之前，請查詢 [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) 介面的影片範例物件。</span><span class="sxs-lookup"><span data-stu-id="d94d8-525">Before you place a sample in the scheduled queue, query the video sample object for the [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) interface.</span></span>

3.  <span data-ttu-id="d94d8-526">以您的回呼介面指標呼叫 [**IMFTrackedSample：： SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) 。</span><span class="sxs-lookup"><span data-stu-id="d94d8-526">Call [**IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) with a pointer to your callback interface.</span></span>
4.  <span data-ttu-id="d94d8-527">當範例準備好進行簡報時，請將它從排程的佇列中移除、呈現，然後釋放範例的所有參考。</span><span class="sxs-lookup"><span data-stu-id="d94d8-527">When the sample is ready for presentation, remove it from the scheduled queue, present it, and release all references to the sample.</span></span>
5.  <span data-ttu-id="d94d8-528">此範例會叫用回呼。</span><span class="sxs-lookup"><span data-stu-id="d94d8-528">The sample invokes the callback.</span></span> <span data-ttu-id="d94d8-529">在此情況下，不會刪除範例物件，因為在叫用回呼之前，它本身會保存參考計數。 )  (</span><span class="sxs-lookup"><span data-stu-id="d94d8-529">(The sample object is not deleted in this case because it holds a reference count on itself until the callback is invoked.)</span></span>
6.  <span data-ttu-id="d94d8-530">在回呼中，將範例傳回到可用的佇列。</span><span class="sxs-lookup"><span data-stu-id="d94d8-530">Inside the callback, return the sample to the available queue.</span></span>

<span data-ttu-id="d94d8-531">展示者不需要使用 [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) 來追蹤範例;您可以實行任何最適合您設計的技術。</span><span class="sxs-lookup"><span data-stu-id="d94d8-531">A presenter is not required to use [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) to track samples; you can implement any technique that works best for your design.</span></span> <span data-ttu-id="d94d8-532">**IMFTrackedSample** 的其中一個優點是，您可以將展示者的排程和轉譯功能移至 helper 物件中，而這些物件不需要任何特殊機制，就能在發行影片範例時回呼給展示者，因為範例物件提供了該機制。</span><span class="sxs-lookup"><span data-stu-id="d94d8-532">One advantage of **IMFTrackedSample** is that you can move the presenter's scheduling and rendering functions into helper objects, and these objects do not need any special mechanism for calling back to the presenter when they release video samples because the sample object provides that mechanism.</span></span>

<span data-ttu-id="d94d8-533">下列程式碼顯示如何設定回呼：</span><span class="sxs-lookup"><span data-stu-id="d94d8-533">The following code shows how to set the callback:</span></span>


```C++
HRESULT EVRCustomPresenter::TrackSample(IMFSample *pSample)
{
    IMFTrackedSample *pTracked = NULL;

    HRESULT hr = pSample->QueryInterface(IID_PPV_ARGS(&pTracked));

    if (SUCCEEDED(hr))
    {
        hr = pTracked->SetAllocator(&m_SampleFreeCB, NULL);
    }

    SafeRelease(&pTracked);
    return hr;
}
```



<span data-ttu-id="d94d8-534">在回呼中，呼叫非同步結果物件上的 [**IMFAsyncResult：： GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject) 以取出範例的指標：</span><span class="sxs-lookup"><span data-stu-id="d94d8-534">In the callback, call [**IMFAsyncResult::GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject) on the asynchronous result object to retrieve a pointer to the sample:</span></span>


```C++
HRESULT EVRCustomPresenter::OnSampleFree(IMFAsyncResult *pResult)
{
    IUnknown *pObject = NULL;
    IMFSample *pSample = NULL;
    IUnknown *pUnk = NULL;

    // Get the sample from the async result object.
    HRESULT hr = pResult->GetObject(&pObject);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pObject->QueryInterface(IID_PPV_ARGS(&pSample));
    if (FAILED(hr))
    {
        goto done;
    }

    // If this sample was submitted for a frame-step, the frame step operation
    // is complete.

    if (m_FrameStep.state == FRAMESTEP_SCHEDULED)
    {
        // Query the sample for IUnknown and compare it to our cached value.
        hr = pSample->QueryInterface(IID_PPV_ARGS(&pUnk));
        if (FAILED(hr))
        {
            goto done;
        }

        if (m_FrameStep.pSampleNoRef == (DWORD_PTR)pUnk)
        {
            // Notify the EVR.
            hr = CompleteFrameStep(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        // Note: Although pObject is also an IUnknown pointer, it is not
        // guaranteed to be the exact pointer value returned through
        // QueryInterface. Therefore, the second QueryInterface call is
        // required.
    }

    /*** Begin lock ***/

    EnterCriticalSection(&m_ObjectLock);

    UINT32 token = MFGetAttributeUINT32(
        pSample, MFSamplePresenter_SampleCounter, (UINT32)-1);

    if (token == m_TokenCounter)
    {
        // Return the sample to the sample pool.
        hr = m_SamplePool.ReturnSample(pSample);
        if (SUCCEEDED(hr))
        {
            // A free sample is available. Process more data if possible.
            (void)ProcessOutputLoop();
        }
    }

    LeaveCriticalSection(&m_ObjectLock);

    /*** End lock ***/

done:
    if (FAILED(hr))
    {
        NotifyEvent(EC_ERRORABORT, hr, 0);
    }
    SafeRelease(&pObject);
    SafeRelease(&pSample);
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="processing-output"></a><span data-ttu-id="d94d8-535">處理輸出</span><span class="sxs-lookup"><span data-stu-id="d94d8-535">Processing Output</span></span>

<span data-ttu-id="d94d8-536">只要混音器收到新的輸入範例，EVR 就會將 **MFVP_MESSAGE_PROCESSINPUTNOTIFY** 訊息傳送給展示者。</span><span class="sxs-lookup"><span data-stu-id="d94d8-536">Whenever the mixer receives a new input sample, the EVR sends an **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message to the presenter.</span></span> <span data-ttu-id="d94d8-537">此訊息表示混音器可能會有新的影片框架可供傳遞。</span><span class="sxs-lookup"><span data-stu-id="d94d8-537">This message indicates that the mixer might have a new video frame to deliver.</span></span> <span data-ttu-id="d94d8-538">在回應中，展示者會在混音器上呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 。</span><span class="sxs-lookup"><span data-stu-id="d94d8-538">In response, the presenter calls [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span> <span data-ttu-id="d94d8-539">如果方法成功，則展示者會排定展示的範例。</span><span class="sxs-lookup"><span data-stu-id="d94d8-539">If the method succeeds, the presenter schedules the sample for presentation.</span></span>

<span data-ttu-id="d94d8-540">若要從混音器取得輸出，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="d94d8-540">To get output from the mixer, perform the following steps:</span></span>

1.  <span data-ttu-id="d94d8-541">檢查時鐘狀態。</span><span class="sxs-lookup"><span data-stu-id="d94d8-541">Check the clock state.</span></span> <span data-ttu-id="d94d8-542">如果時鐘已暫停，除非這是第一個影片畫面，否則請忽略 **MFVP_MESSAGE_PROCESSINPUTNOTIFY** 的訊息。</span><span class="sxs-lookup"><span data-stu-id="d94d8-542">If the clock is paused, ignore the **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message unless this is the first video frame.</span></span> <span data-ttu-id="d94d8-543">如果時鐘正在執行，或這是第一個影片畫面，請繼續。</span><span class="sxs-lookup"><span data-stu-id="d94d8-543">If the clock is running, or if this is the first video frame, continue.</span></span>
2.  <span data-ttu-id="d94d8-544">從可用範例的佇列取得範例。</span><span class="sxs-lookup"><span data-stu-id="d94d8-544">Get a sample from the queue of available samples.</span></span> <span data-ttu-id="d94d8-545">如果佇列是空的，則表示目前已排程所有配置的樣本進行呈現。</span><span class="sxs-lookup"><span data-stu-id="d94d8-545">If the queue is empty, it means that all allocated samples are currently scheduled for presenting.</span></span> <span data-ttu-id="d94d8-546">在這種情況下，請忽略目前的 **MFVP_MESSAGE_PROCESSINPUTNOTIFY** 訊息。</span><span class="sxs-lookup"><span data-stu-id="d94d8-546">In that case, ignore the **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message at this time.</span></span> <span data-ttu-id="d94d8-547">當下一個範例變成可用時，請重複此處所列的步驟。</span><span class="sxs-lookup"><span data-stu-id="d94d8-547">When the next sample becomes available, repeat the steps listed here.</span></span>
3.  <span data-ttu-id="d94d8-548"> (選擇項。 ) 如果有可用的時鐘，請呼叫 [**IMFClock：： GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime)取得目前的時鐘時間 (*T1*) 。</span><span class="sxs-lookup"><span data-stu-id="d94d8-548">(Optional.) If the clock is available, get the current clock time (*T1*) by calling [**IMFClock::GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span></span>
4.  <span data-ttu-id="d94d8-549">在混音器上呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 。</span><span class="sxs-lookup"><span data-stu-id="d94d8-549">Call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span> <span data-ttu-id="d94d8-550">如果 **ProcessOutput** 成功，範例就會包含影片畫面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-550">If **ProcessOutput** succeeds, the sample contains a video frame.</span></span> <span data-ttu-id="d94d8-551">如果方法失敗，請檢查傳回碼。</span><span class="sxs-lookup"><span data-stu-id="d94d8-551">If the method fails, check the return code.</span></span> <span data-ttu-id="d94d8-552">**ProcessOutput** 中的下列錯誤碼不是嚴重失敗：</span><span class="sxs-lookup"><span data-stu-id="d94d8-552">The following error codes from **ProcessOutput** are not critical failures:</span></span>

    

    | <span data-ttu-id="d94d8-553">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="d94d8-553">Error code</span></span>                              | <span data-ttu-id="d94d8-554">描述</span><span class="sxs-lookup"><span data-stu-id="d94d8-554">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
    |-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="d94d8-555">**MF_E_TRANSFORM_NEED_MORE_INPUT**</span><span class="sxs-lookup"><span data-stu-id="d94d8-555">**MF_E_TRANSFORM_NEED_MORE_INPUT**</span></span> | <span data-ttu-id="d94d8-556">混音器需要更多輸入，才能產生新的輸出框架。</span><span class="sxs-lookup"><span data-stu-id="d94d8-556">The mixer needs more input before it can produce a new output frame.</span></span><br/> <span data-ttu-id="d94d8-557">如果您收到此錯誤碼，請檢查 EVR 是否已到達資料流程的結尾並據以回應，如 [資料流程結尾](#end-of-stream)所述。</span><span class="sxs-lookup"><span data-stu-id="d94d8-557">If you get this error code, check whether the EVR has reached the end of the stream and respond accordingly, as described in [End of Stream](#end-of-stream).</span></span> <span data-ttu-id="d94d8-558">否則，請忽略此 **MF_E_TRANSFORM_NEED_MORE_INPUT** 訊息。</span><span class="sxs-lookup"><span data-stu-id="d94d8-558">Otherwise, ignore this **MF_E_TRANSFORM_NEED_MORE_INPUT** message.</span></span> <span data-ttu-id="d94d8-559">當混音器取得更多輸入時，EVR 會傳送另一個。</span><span class="sxs-lookup"><span data-stu-id="d94d8-559">The EVR will send another one when the mixer gets more input.</span></span><br/> |
    | <span data-ttu-id="d94d8-560">**MF_E_TRANSFORM_STREAM_CHANGE**</span><span class="sxs-lookup"><span data-stu-id="d94d8-560">**MF_E_TRANSFORM_STREAM_CHANGE**</span></span>    | <span data-ttu-id="d94d8-561">混音器的輸出類型已變成無效，可能是因為格式變更上游。</span><span class="sxs-lookup"><span data-stu-id="d94d8-561">The mixer's output type has become invalid, possibly due to a format change upstream.</span></span><br/> <span data-ttu-id="d94d8-562">如果您收到此錯誤碼，請將展示者的媒體類型設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d94d8-562">If you get this error code, set the presenter's media type to **NULL**.</span></span> <span data-ttu-id="d94d8-563">EVR 會要求新的格式。</span><span class="sxs-lookup"><span data-stu-id="d94d8-563">The EVR will request a new format.</span></span><br/>                                                                                                                                                                         |
    | <span data-ttu-id="d94d8-564">**MF_E_TRANSFORM_TYPE_NOT_SET**</span><span class="sxs-lookup"><span data-stu-id="d94d8-564">**MF_E_TRANSFORM_TYPE_NOT_SET**</span></span>    | <span data-ttu-id="d94d8-565">混音器需要新的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="d94d8-565">The mixer requires a new media type.</span></span><br/> <span data-ttu-id="d94d8-566">如果您收到此錯誤碼，請重新協商混音器的輸出類型，如 [協商格式](#negotiating-formats)所述。</span><span class="sxs-lookup"><span data-stu-id="d94d8-566">If you get this error code, renegotiate the mixer's output type as described in [Negotiating Formats](#negotiating-formats).</span></span><br/>                                                                                                                                                                                                        |

    

     

    <span data-ttu-id="d94d8-567">如果 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 成功，請繼續。</span><span class="sxs-lookup"><span data-stu-id="d94d8-567">If [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) succeeds, continue.</span></span>

5.  <span data-ttu-id="d94d8-568"> (選擇項。 ) 如果有可用的時鐘，請 (*T2*) 取得目前的時鐘時間。</span><span class="sxs-lookup"><span data-stu-id="d94d8-568">(Optional.) If the clock is available, get the current clock time (*T2*).</span></span> <span data-ttu-id="d94d8-569">混音器引進的延遲量是 (*T2*  -  *T1*) 。</span><span class="sxs-lookup"><span data-stu-id="d94d8-569">The amount of latency introduced by the mixer is (*T2* - *T1*).</span></span> <span data-ttu-id="d94d8-570">將具有此值的 **EC_PROCESSING_LATENCY** 事件傳送至 EVR。</span><span class="sxs-lookup"><span data-stu-id="d94d8-570">Send an **EC_PROCESSING_LATENCY** event with this value to the EVR.</span></span> <span data-ttu-id="d94d8-571">EVR 會使用此值來進行品質控制。</span><span class="sxs-lookup"><span data-stu-id="d94d8-571">The EVR uses this value for quality control.</span></span> <span data-ttu-id="d94d8-572">如果沒有可用的時鐘，就沒有理由傳送 **EC_PROCESSING_LATENCY** 事件。</span><span class="sxs-lookup"><span data-stu-id="d94d8-572">If no clock is available, there is no reason to send the **EC_PROCESSING_LATENCY** event.</span></span>
6.  <span data-ttu-id="d94d8-573"> (選擇項。 ) 查詢範例以 [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) ，並呼叫 [**IMFTrackedSample：： SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) ，如 [追蹤範例](#tracking-samples)中所述。</span><span class="sxs-lookup"><span data-stu-id="d94d8-573">(Optional.) Query the sample for [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) and call [**IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) as described in [Tracking Samples](#tracking-samples).</span></span>
7.  <span data-ttu-id="d94d8-574">排程簡報的範例。</span><span class="sxs-lookup"><span data-stu-id="d94d8-574">Schedule the sample for presentation.</span></span>

<span data-ttu-id="d94d8-575">在展示器取得混音器的任何輸出之前，這一系列的步驟都可以終止。</span><span class="sxs-lookup"><span data-stu-id="d94d8-575">This sequence of steps can terminate before the presenter gets any output from the mixer.</span></span> <span data-ttu-id="d94d8-576">為確保不會卸載任何要求，您應該在發生下列情況時重複相同的步驟：</span><span class="sxs-lookup"><span data-stu-id="d94d8-576">To ensure that no requests are dropped, you should repeat the same steps when the following occur:</span></span>

-   <span data-ttu-id="d94d8-577">會呼叫展示者的 [**IMFClockStateSink：： OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) 或 **IMFClockStateSink：： OnClockStart** 方法。</span><span class="sxs-lookup"><span data-stu-id="d94d8-577">The presenter's [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) or **IMFClockStateSink::OnClockStart** method is called.</span></span> <span data-ttu-id="d94d8-578">這會處理混音器忽略輸入的情況，因為時鐘是在步驟 1)  (暫停。</span><span class="sxs-lookup"><span data-stu-id="d94d8-578">This handles the case where the mixer ignores input because the clock is paused (step 1).</span></span>
-   <span data-ttu-id="d94d8-579">叫用 [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) 回呼。</span><span class="sxs-lookup"><span data-stu-id="d94d8-579">The [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) callback is invoked.</span></span> <span data-ttu-id="d94d8-580">這會處理混音器收到輸入的情況，但 (步驟 2) 使用所有顯示者的影片範例。</span><span class="sxs-lookup"><span data-stu-id="d94d8-580">This handles the case where the mixer receives input but all of the presenter's video samples are in use (step 2).</span></span>

<span data-ttu-id="d94d8-581">接下來的幾個程式碼範例會更詳細地顯示這些步驟。</span><span class="sxs-lookup"><span data-stu-id="d94d8-581">The next several code examples show these steps in more detail.</span></span> <span data-ttu-id="d94d8-582">展示者會在 `ProcessInputNotify` 取得 **MFVP_MESSAGE_PROCESSINPUTNOTIFY** 訊息時，呼叫方法 (下列範例所示) 。</span><span class="sxs-lookup"><span data-stu-id="d94d8-582">The presenter calls the `ProcessInputNotify` method (shown in the following example) when it gets the **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message.</span></span>


```C++
//-----------------------------------------------------------------------------
// ProcessInputNotify
//
// Attempts to get a new output sample from the mixer.
//
// This method is called when the EVR sends an MFVP_MESSAGE_PROCESSINPUTNOTIFY
// message, which indicates that the mixer has a new input sample.
//
// Note: If there are multiple input streams, the mixer might not deliver an
// output sample for every input sample.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessInputNotify()
{
    HRESULT hr = S_OK;

    // Set the flag that says the mixer has a new sample.
    m_bSampleNotify = TRUE;

    if (m_pMediaType == NULL)
    {
        // We don't have a valid media type yet.
        hr = MF_E_TRANSFORM_TYPE_NOT_SET;
    }
    else
    {
        // Try to process an output sample.
        ProcessOutputLoop();
    }
    return hr;
}
```



<span data-ttu-id="d94d8-583">這個 `ProcessInputNotify` 方法會設定布林值旗標，以記錄混音器有新輸入的事實。</span><span class="sxs-lookup"><span data-stu-id="d94d8-583">This `ProcessInputNotify` method sets a Boolean flag to record the fact that the mixer has new input.</span></span> <span data-ttu-id="d94d8-584">然後，它會呼叫 `ProcessOutputLoop` 方法，如下一個範例所示。</span><span class="sxs-lookup"><span data-stu-id="d94d8-584">Then it calls the `ProcessOutputLoop` method, shown in the next example.</span></span> <span data-ttu-id="d94d8-585">這個方法會嘗試從混音器提取盡可能多的樣本：</span><span class="sxs-lookup"><span data-stu-id="d94d8-585">This method attempts to pull as many samples as possible from the mixer:</span></span>


```C++
void EVRCustomPresenter::ProcessOutputLoop()
{
    HRESULT hr = S_OK;

    // Process as many samples as possible.
    while (hr == S_OK)
    {
        // If the mixer doesn't have a new input sample, break from the loop.
        if (!m_bSampleNotify)
        {
            hr = MF_E_TRANSFORM_NEED_MORE_INPUT;
            break;
        }

        // Try to process a sample.
        hr = ProcessOutput();

        // NOTE: ProcessOutput can return S_FALSE to indicate it did not
        // process a sample. If so, break out of the loop.
    }

    if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
    {
        // The mixer has run out of input data. Check for end-of-stream.
        CheckEndOfStream();
    }
}
```



<span data-ttu-id="d94d8-586">`ProcessOutput`下一個範例所示的方法會嘗試從混音器取得單一的影片畫面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-586">The `ProcessOutput` method, shown in the next example, attempts to get a single video frame from the mixer.</span></span> <span data-ttu-id="d94d8-587">如果沒有可用的影片畫面，會傳回 `ProcessSample` S_FALSE 或錯誤碼，而這兩個程式碼都會中斷中的迴圈 `ProcessOutputLoop` 。</span><span class="sxs-lookup"><span data-stu-id="d94d8-587">If no video frame is available, `ProcessSample` returns S_FALSE or an error code, either of which interrupts the loop in `ProcessOutputLoop`.</span></span> <span data-ttu-id="d94d8-588">大部分的工作都是在方法中完成 `ProcessOutput` ：</span><span class="sxs-lookup"><span data-stu-id="d94d8-588">Most of the work is done inside the `ProcessOutput` method:</span></span>


```C++
//-----------------------------------------------------------------------------
// ProcessOutput
//
// Attempts to get a new output sample from the mixer.
//
// Called in two situations:
// (1) ProcessOutputLoop, if the mixer has a new input sample.
// (2) Repainting the last frame.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessOutput()
{
    assert(m_bSampleNotify || m_bRepaint);  // See note above.

    HRESULT     hr = S_OK;
    DWORD       dwStatus = 0;
    LONGLONG    mixerStartTime = 0, mixerEndTime = 0;
    MFTIME      systemTime = 0;
    BOOL        bRepaint = m_bRepaint; // Temporarily store this state flag.

    MFT_OUTPUT_DATA_BUFFER dataBuffer;
    ZeroMemory(&dataBuffer, sizeof(dataBuffer));

    IMFSample *pSample = NULL;

    // If the clock is not running, we present the first sample,
    // and then don't present any more until the clock starts.

    if ((m_RenderState != RENDER_STATE_STARTED) &&  // Not running.
         !m_bRepaint &&             // Not a repaint request.
         m_bPrerolled               // At least one sample has been presented.
         )
    {
        return S_FALSE;
    }

    // Make sure we have a pointer to the mixer.
    if (m_pMixer == NULL)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Try to get a free sample from the video sample pool.
    hr = m_SamplePool.GetSample(&pSample);
    if (hr == MF_E_SAMPLEALLOCATOR_EMPTY)
    {
        // No free samples. Try again when a sample is released.
        return S_FALSE;
    }
    else if (FAILED(hr))
    {
        return hr;
    }

    // From now on, we have a valid video sample pointer, where the mixer will
    // write the video data.
    assert(pSample != NULL);

    // (If the following assertion fires, it means we are not managing the sample pool correctly.)
    assert(MFGetAttributeUINT32(pSample, MFSamplePresenter_SampleCounter, (UINT32)-1) == m_TokenCounter);

    if (m_bRepaint)
    {
        // Repaint request. Ask the mixer for the most recent sample.
        SetDesiredSampleTime(
            pSample,
            m_scheduler.LastSampleTime(),
            m_scheduler.FrameDuration()
            );

        m_bRepaint = FALSE; // OK to clear this flag now.
    }
    else
    {
        // Not a repaint request. Clear the desired sample time; the mixer will
        // give us the next frame in the stream.
        ClearDesiredSampleTime(pSample);

        if (m_pClock)
        {
            // Latency: Record the starting time for ProcessOutput.
            (void)m_pClock->GetCorrelatedTime(0, &mixerStartTime, &systemTime);
        }
    }

    // Now we are ready to get an output sample from the mixer.
    dataBuffer.dwStreamID = 0;
    dataBuffer.pSample = pSample;
    dataBuffer.dwStatus = 0;

    hr = m_pMixer->ProcessOutput(0, 1, &dataBuffer, &dwStatus);

    if (FAILED(hr))
    {
        // Return the sample to the pool.
        HRESULT hr2 = m_SamplePool.ReturnSample(pSample);
        if (FAILED(hr2))
        {
            hr = hr2;
            goto done;
        }
        // Handle some known error codes from ProcessOutput.
        if (hr == MF_E_TRANSFORM_TYPE_NOT_SET)
        {
            // The mixer's format is not set. Negotiate a new format.
            hr = RenegotiateMediaType();
        }
        else if (hr == MF_E_TRANSFORM_STREAM_CHANGE)
        {
            // There was a dynamic media type change. Clear our media type.
            SetMediaType(NULL);
        }
        else if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
        {
            // The mixer needs more input.
            // We have to wait for the mixer to get more input.
            m_bSampleNotify = FALSE;
        }
    }
    else
    {
        // We got an output sample from the mixer.

        if (m_pClock && !bRepaint)
        {
            // Latency: Record the ending time for the ProcessOutput operation,
            // and notify the EVR of the latency.

            (void)m_pClock->GetCorrelatedTime(0, &mixerEndTime, &systemTime);

            LONGLONG latencyTime = mixerEndTime - mixerStartTime;
            NotifyEvent(EC_PROCESSING_LATENCY, (LONG_PTR)&latencyTime, 0);
        }

        // Set up notification for when the sample is released.
        hr = TrackSample(pSample);
        if (FAILED(hr))
        {
            goto done;
        }

        // Schedule the sample.
        if ((m_FrameStep.state == FRAMESTEP_NONE) || bRepaint)
        {
            hr = DeliverSample(pSample, bRepaint);
            if (FAILED(hr))
            {
                goto done;
            }
        }
        else
        {
            // We are frame-stepping (and this is not a repaint request).
            hr = DeliverFrameStepSample(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        m_bPrerolled = TRUE; // We have presented at least one sample now.
    }

done:
    SafeRelease(&pSample);

    // Important: Release any events returned from the ProcessOutput method.
    SafeRelease(&dataBuffer.pEvents);
    return hr;
}
```



<span data-ttu-id="d94d8-589">關於此範例的一些備註：</span><span class="sxs-lookup"><span data-stu-id="d94d8-589">Some remarks about this example:</span></span>

-   <span data-ttu-id="d94d8-590">*M_SamplePool* 變數會假設為包含可用影片範例佇列的集合物件。</span><span class="sxs-lookup"><span data-stu-id="d94d8-590">The *m_SamplePool* variable is assumed to be a collection object that holds the queue of available video samples.</span></span> <span data-ttu-id="d94d8-591">如果佇列是空的，則物件的 `GetSample` 方法會傳回 **MF_E_SAMPLEALLOCATOR_EMPTY** 。</span><span class="sxs-lookup"><span data-stu-id="d94d8-591">The object's `GetSample` method returns **MF_E_SAMPLEALLOCATOR_EMPTY** if the queue is empty.</span></span>
-   <span data-ttu-id="d94d8-592">如果混音器的 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 方法傳回 MF_E_TRANSFORM_NEED_MORE_INPUT，則表示混音器無法產生任何輸出，因此展示者會清除 *m_fSampleNotify* 旗標。</span><span class="sxs-lookup"><span data-stu-id="d94d8-592">If the mixer's [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method returns MF_E_TRANSFORM_NEED_MORE_INPUT, it means the mixer cannot produce any more output, so the presenter clears the *m_fSampleNotify* flag.</span></span>
-   <span data-ttu-id="d94d8-593">`TrackSample`設定 [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)回呼的方法會顯示在「[追蹤範例](#tracking-samples)」一節中。</span><span class="sxs-lookup"><span data-stu-id="d94d8-593">The `TrackSample` method, which sets the [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) callback, is shown in the section [Tracking Samples](#tracking-samples).</span></span>

### <a name="repainting-frames"></a><span data-ttu-id="d94d8-594">重新繪製框架</span><span class="sxs-lookup"><span data-stu-id="d94d8-594">Repainting Frames</span></span>

<span data-ttu-id="d94d8-595">有時候，顯示者可能需要重新繪製最新的影片畫面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-595">Occasionally the presenter might need to repaint the most recent video frame.</span></span> <span data-ttu-id="d94d8-596">例如，標準展示者會在下列情況中重新繪製框架：</span><span class="sxs-lookup"><span data-stu-id="d94d8-596">For example, the standard presenter repaints the frame in the following situations:</span></span>

-   <span data-ttu-id="d94d8-597">在視窗模式下，回應應用程式視窗所接收的 **WM_PAINT** 訊息。</span><span class="sxs-lookup"><span data-stu-id="d94d8-597">In windowed mode, in response to **WM_PAINT** messages received by the application's window.</span></span> <span data-ttu-id="d94d8-598">請參閱 [**IMFVideoDisplayControl：： RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo)。</span><span class="sxs-lookup"><span data-stu-id="d94d8-598">See [**IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span></span>
-   <span data-ttu-id="d94d8-599">當應用程式呼叫 [**IMFVideoDisplayControl：： SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition)時，如果目的地矩形變更。</span><span class="sxs-lookup"><span data-stu-id="d94d8-599">If the destination rectangle changes when the application calls [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>

<span data-ttu-id="d94d8-600">使用下列步驟來要求混音器重新建立最新的框架：</span><span class="sxs-lookup"><span data-stu-id="d94d8-600">Use the following steps to request the mixer to re-create the most recent frame:</span></span>

1.  <span data-ttu-id="d94d8-601">從佇列取得影片範例。</span><span class="sxs-lookup"><span data-stu-id="d94d8-601">Get a video sample from the queue.</span></span>
2.  <span data-ttu-id="d94d8-602">查詢 [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample) 介面的範例。</span><span class="sxs-lookup"><span data-stu-id="d94d8-602">Query the sample for the [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample) interface.</span></span>
3.  <span data-ttu-id="d94d8-603">呼叫 [**IMFDesiredSample：： SetDesiredSampleTimeAndDuration**](/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration)。</span><span class="sxs-lookup"><span data-stu-id="d94d8-603">Call [**IMFDesiredSample::SetDesiredSampleTimeAndDuration**](/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration).</span></span> <span data-ttu-id="d94d8-604">指定最新影片畫面的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="d94d8-604">Specify the time stamp of the most recent video frame.</span></span> <span data-ttu-id="d94d8-605"> (您將需要快取此值，並為每個畫面格進行更新。 ) </span><span class="sxs-lookup"><span data-stu-id="d94d8-605">(You will need to cache this value and update it for each frame.)</span></span>
4.  <span data-ttu-id="d94d8-606">在混音器上呼叫 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 。</span><span class="sxs-lookup"><span data-stu-id="d94d8-606">Call [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span>

<span data-ttu-id="d94d8-607">重新繪製框架時，您可以忽略簡報時鐘並立即呈現畫面格。</span><span class="sxs-lookup"><span data-stu-id="d94d8-607">When repainting a frame, you can ignore the presentation clock and present the frame immediately.</span></span>

### <a name="scheduling-samples"></a><span data-ttu-id="d94d8-608">排程範例</span><span class="sxs-lookup"><span data-stu-id="d94d8-608">Scheduling Samples</span></span>

<span data-ttu-id="d94d8-609">影片框架隨時都可以觸及 EVR。</span><span class="sxs-lookup"><span data-stu-id="d94d8-609">Video frames can reach the EVR at any time.</span></span> <span data-ttu-id="d94d8-610">展示者負責根據框架的時間戳記，以正確的時間呈現每個畫面格。</span><span class="sxs-lookup"><span data-stu-id="d94d8-610">The presenter is responsible for presenting each frame at the correct time, based on the time stamp of the frame.</span></span> <span data-ttu-id="d94d8-611">當展示者從混音器取得新的範例時，它會將範例放在已排程的佇列上。</span><span class="sxs-lookup"><span data-stu-id="d94d8-611">When the presenter gets a new sample from the mixer, it puts the sample on the scheduled queue.</span></span> <span data-ttu-id="d94d8-612">在不同的執行緒上，展示者會持續從佇列的標頭取得第一個範例，並決定是否要：</span><span class="sxs-lookup"><span data-stu-id="d94d8-612">On a separate thread, the presenter continually gets the first sample from the head of the queue and determines whether to:</span></span>

-   <span data-ttu-id="d94d8-613">顯示範例。</span><span class="sxs-lookup"><span data-stu-id="d94d8-613">Present the sample.</span></span>
-   <span data-ttu-id="d94d8-614">將範例保留在佇列中，因為它是早期的。</span><span class="sxs-lookup"><span data-stu-id="d94d8-614">Keep the sample on the queue because it is early.</span></span>
-   <span data-ttu-id="d94d8-615">捨棄範例，因為它已延遲。</span><span class="sxs-lookup"><span data-stu-id="d94d8-615">Discard the sample because it is late.</span></span> <span data-ttu-id="d94d8-616">雖然您應該盡可能避免卸載畫面格，但您可能需要在展示者持續落後的情況下。</span><span class="sxs-lookup"><span data-stu-id="d94d8-616">Although you should avoid dropping frames if possible, you might need to if the presenter is continually falling behind.</span></span>

<span data-ttu-id="d94d8-617">若要取得影片框架的時間戳記，請在影片範例上呼叫 [**IMFSample：： GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) 。</span><span class="sxs-lookup"><span data-stu-id="d94d8-617">To get the time stamp for a video frame, call [**IMFSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) on the video sample.</span></span> <span data-ttu-id="d94d8-618">時間戳記相對於 EVR 的簡報時鐘。</span><span class="sxs-lookup"><span data-stu-id="d94d8-618">The time stamp is relative to the EVR's presentation clock.</span></span> <span data-ttu-id="d94d8-619">若要取得目前的時鐘時間，請呼叫 [**IMFClock：： GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime)。</span><span class="sxs-lookup"><span data-stu-id="d94d8-619">To get the current clock time, call [**IMFClock::GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span></span> <span data-ttu-id="d94d8-620">如果 EVR 沒有呈現時鐘，或是範例沒有時間戳記，您可以在取得範例之後立即提出範例。</span><span class="sxs-lookup"><span data-stu-id="d94d8-620">If the EVR does not have a presentation clock, or if a sample does not have a time stamp, you can present the sample immediately after you get it.</span></span>

<span data-ttu-id="d94d8-621">若要取得每個範例的持續時間，請呼叫 [**IMFSample：： GetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration)。</span><span class="sxs-lookup"><span data-stu-id="d94d8-621">To get the duration of each sample, call [**IMFSample::GetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration).</span></span> <span data-ttu-id="d94d8-622">如果範例沒有持續時間，您可以使用 [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) 函式來計算畫面播放速率的持續時間。</span><span class="sxs-lookup"><span data-stu-id="d94d8-622">If the sample does not have a duration, you can use the [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) function to calculate the duration from the frame rate.</span></span>

<span data-ttu-id="d94d8-623">當您排程範例時，請記住下列事項：</span><span class="sxs-lookup"><span data-stu-id="d94d8-623">When you schedule samples, keep in mind the following:</span></span>

-   <span data-ttu-id="d94d8-624">如果播放速率比正常速度快或慢很多，則會以較快或較慢的速率執行時鐘。</span><span class="sxs-lookup"><span data-stu-id="d94d8-624">If the playback rate is faster or slower than normal speed, the clock runs at a faster or slower rate.</span></span> <span data-ttu-id="d94d8-625">這表示樣本上的時間戳記一律會提供相對於呈現時鐘的正確目標時間。</span><span class="sxs-lookup"><span data-stu-id="d94d8-625">That means the time stamp on a sample always gives the correct target time relative to the presentation clock.</span></span> <span data-ttu-id="d94d8-626">但是，如果您將簡報時間轉譯為一些其他的時鐘時間 (例如，高解析度效能計數器) ，您就必須根據頻率速度來調整時間。</span><span class="sxs-lookup"><span data-stu-id="d94d8-626">However, if you translate presentation times into some other clock time (for example, the high-resolution performace counter), then you must scale the times based on the clock speed.</span></span> <span data-ttu-id="d94d8-627">如果頻率速度變更，EVR 會呼叫展示者的 [**IMFClockStateSink：： OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) 方法。</span><span class="sxs-lookup"><span data-stu-id="d94d8-627">If the clock speed changes, the EVR calls the presenter's [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) method.</span></span>
-   <span data-ttu-id="d94d8-628">播放速率可以是反向播放的負數。</span><span class="sxs-lookup"><span data-stu-id="d94d8-628">The playback rate can be negative for reverse playback.</span></span> <span data-ttu-id="d94d8-629">當播放速率為負數時，標記法會往後執行。</span><span class="sxs-lookup"><span data-stu-id="d94d8-629">When the playback rate is negative, the presentation clock runs backward.</span></span> <span data-ttu-id="d94d8-630">換句話說，在時間 *n* 前發生時間 *n* + 1。</span><span class="sxs-lookup"><span data-stu-id="d94d8-630">In other words, time *N* + 1 occurs before time *N*.</span></span>

<span data-ttu-id="d94d8-631">下列範例會計算樣本的初期或晚期（相對於簡報時鐘）：</span><span class="sxs-lookup"><span data-stu-id="d94d8-631">The following example calculates how early or late a sample is, relative to the presentation clock:</span></span>


```C++
    LONGLONG hnsPresentationTime = 0;
    LONGLONG hnsTimeNow = 0;
    MFTIME   hnsSystemTime = 0;

    BOOL bPresentNow = TRUE;
    LONG lNextSleep = 0;

    if (m_pClock)
    {
        // Get the sample's time stamp. It is valid for a sample to
        // have no time stamp.
        hr = pSample->GetSampleTime(&hnsPresentationTime);

        // Get the clock time. (But if the sample does not have a time stamp,
        // we don't need the clock time.)
        if (SUCCEEDED(hr))
        {
            hr = m_pClock->GetCorrelatedTime(0, &hnsTimeNow, &hnsSystemTime);
        }

        // Calculate the time until the sample's presentation time.
        // A negative value means the sample is late.
        LONGLONG hnsDelta = hnsPresentationTime - hnsTimeNow;
        if (m_fRate < 0)
        {
            // For reverse playback, the clock runs backward. Therefore, the
            // delta is reversed.
            hnsDelta = - hnsDelta;
        }
```



<span data-ttu-id="d94d8-632">簡報時鐘通常是由系統時鐘或音訊轉譯器驅動。</span><span class="sxs-lookup"><span data-stu-id="d94d8-632">The presentation clock is usually driven by the system clock or the audio renderer.</span></span> <span data-ttu-id="d94d8-633"> (音訊轉譯器會從音效卡耗用音訊的速率衍生時間。 ) 一般情況下，簡報時鐘不會與監視器的重新整理頻率同步。</span><span class="sxs-lookup"><span data-stu-id="d94d8-633">(The audio renderer derives the time from the rate at which the sound card consumes audio.) In general, the presentation clock is not synchronized with the refresh rate of the monitor.</span></span>

<span data-ttu-id="d94d8-634">如果您的 Direct3D 展示參數指定表示間隔 **D3DPRESENT_INTERVAL_DEFAULT** 或 **D3DPRESENT_INTERVAL_ONE** ，則 **目前** 的作業會等待監視器的垂直回溯。</span><span class="sxs-lookup"><span data-stu-id="d94d8-634">If your Direct3D presentation parameters specify **D3DPRESENT_INTERVAL_DEFAULT** or **D3DPRESENT_INTERVAL_ONE** for the presentation interval, the **Present** operation waits for the monitor's vertical retrace.</span></span> <span data-ttu-id="d94d8-635">這是防止破壞的簡單方法，但會降低排程演算法的精確度。</span><span class="sxs-lookup"><span data-stu-id="d94d8-635">This is an easy way to prevent tearing, but reduces the accuracy of your scheduling algorithm.</span></span> <span data-ttu-id="d94d8-636">相反地，如果呈現間隔是 **D3DPRESENT_INTERVAL_IMMEDIATE**，則 **目前** 的方法會立即執行，這會導致卸載，除非您的排程演算法精確地指出 **您只在** 垂直回溯期間內呼叫。</span><span class="sxs-lookup"><span data-stu-id="d94d8-636">Conversely, if the presentation interval is **D3DPRESENT_INTERVAL_IMMEDIATE**, the **Present** method executes immediately, which causes tearing unless your scheduling algorithm is accurate enough that you call **Present** only during the vertical retrace period.</span></span>

<span data-ttu-id="d94d8-637">下列函數可協助您取得準確的計時資訊：</span><span class="sxs-lookup"><span data-stu-id="d94d8-637">The following functions can help you get accurate timing information:</span></span>

-   <span data-ttu-id="d94d8-638">**IDirect3DDevice9：： GetRasterStatus** 會傳回有關點陣的資訊，包括目前的掃描行，以及點陣是否在垂直空白期間內。</span><span class="sxs-lookup"><span data-stu-id="d94d8-638">**IDirect3DDevice9::GetRasterStatus** returns information about the raster, including the current scan line and whether the raster is in the vertical blank period.</span></span>
-   <span data-ttu-id="d94d8-639">**DwmGetCompositionTimingInfo** 會傳回桌面視窗管理員的計時資訊。</span><span class="sxs-lookup"><span data-stu-id="d94d8-639">**DwmGetCompositionTimingInfo** returns timing information for the desktop window manager.</span></span> <span data-ttu-id="d94d8-640">如果啟用桌面組合，這項資訊會很有用。</span><span class="sxs-lookup"><span data-stu-id="d94d8-640">This information is useful if desktop composition is enabled.</span></span>

### <a name="presenting-samples"></a><span data-ttu-id="d94d8-641">呈現範例</span><span class="sxs-lookup"><span data-stu-id="d94d8-641">Presenting Samples</span></span>

<span data-ttu-id="d94d8-642">本節假設您已針對每個介面建立個別的交換鏈，如配置 [Direct3D](#allocating-direct3d-surfaces)介面中所述。</span><span class="sxs-lookup"><span data-stu-id="d94d8-642">This section assumes that you created a separate swap chain for each surface as described in [Allocating Direct3D Surfaces](#allocating-direct3d-surfaces).</span></span> <span data-ttu-id="d94d8-643">若要呈現範例，請從影片範例取得交換鏈，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d94d8-643">To present a sample, get the swap chain from the video sample as follows:</span></span>

1.  <span data-ttu-id="d94d8-644">在影片範例上呼叫 [**IMFSample：： GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) ，以取得緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d94d8-644">Call [**IMFSample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) on the video sample to get the buffer.</span></span>
2.  <span data-ttu-id="d94d8-645">查詢緩衝區以取得 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) 介面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-645">Query the buffer for the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
3.  <span data-ttu-id="d94d8-646">呼叫 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 來取得 Direct3D 介面的 **IDirect3DSurface9** 介面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-646">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get the **IDirect3DSurface9** interface of the Direct3D surface.</span></span> <span data-ttu-id="d94d8-647"> (您可以藉由呼叫 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)，將此步驟和前一個步驟結合在一起。 ) </span><span class="sxs-lookup"><span data-stu-id="d94d8-647">(You can combine this step and the previous step into one by calling [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).)</span></span>
4.  <span data-ttu-id="d94d8-648">在介面上呼叫 **IDirect3DSurface9：： GetContainer** ，以取得交換鏈的指標。</span><span class="sxs-lookup"><span data-stu-id="d94d8-648">Call **IDirect3DSurface9::GetContainer** on the surface to get a pointer to the swap chain.</span></span>
5.  <span data-ttu-id="d94d8-649">呼叫 **IDirect3DSwapChain9：:P** 在交換鏈上重新傳送。</span><span class="sxs-lookup"><span data-stu-id="d94d8-649">Call **IDirect3DSwapChain9::Present** on the swap chain.</span></span>

<span data-ttu-id="d94d8-650">下列程式碼顯示這些步驟：</span><span class="sxs-lookup"><span data-stu-id="d94d8-650">The following code shows these steps:</span></span>


```C++
HRESULT D3DPresentEngine::PresentSample(IMFSample* pSample, LONGLONG llTarget)
{
    HRESULT hr = S_OK;

    IMFMediaBuffer* pBuffer = NULL;
    IDirect3DSurface9* pSurface = NULL;
    IDirect3DSwapChain9* pSwapChain = NULL;

    if (pSample)
    {
        // Get the buffer from the sample.
        hr = pSample->GetBufferByIndex(0, &pBuffer);
        if (FAILED(hr))
        {
            goto done;
        }

        // Get the surface from the buffer.
        hr = MFGetService(pBuffer, MR_BUFFER_SERVICE, IID_PPV_ARGS(&pSurface));
        if (FAILED(hr))
        {
            goto done;
        }
    }
    else if (m_pSurfaceRepaint)
    {
        // Redraw from the last surface.
        pSurface = m_pSurfaceRepaint;
        pSurface->AddRef();
    }

    if (pSurface)
    {
        // Get the swap chain from the surface.
        hr = pSurface->GetContainer(IID_PPV_ARGS(&pSwapChain));
        if (FAILED(hr))
        {
            goto done;
        }

        // Present the swap chain.
        hr = PresentSwapChain(pSwapChain, pSurface);
        if (FAILED(hr))
        {
            goto done;
        }

        // Store this pointer in case we need to repaint the surface.
        CopyComPointer(m_pSurfaceRepaint, pSurface);
    }
    else
    {
        // No surface. All we can do is paint a black rectangle.
        PaintFrameWithGDI();
    }

done:
    SafeRelease(&pSwapChain);
    SafeRelease(&pSurface);
    SafeRelease(&pBuffer);

    if (FAILED(hr))
    {
        if (hr == D3DERR_DEVICELOST || hr == D3DERR_DEVICENOTRESET || hr == D3DERR_DEVICEHUNG)
        {
            // We failed because the device was lost. Fill the destination rectangle.
            PaintFrameWithGDI();

            // Ignore. We need to reset or re-create the device, but this method
            // is probably being called from the scheduler thread, which is not the
            // same thread that created the device. The Reset(Ex) method must be
            // called from the thread that created the device.

            // The presenter will detect the state when it calls CheckDeviceState()
            // on the next sample.
            hr = S_OK;
        }
    }
    return hr;
}
```



### <a name="source-and-destination-rectangles"></a><span data-ttu-id="d94d8-651">來源和目的地矩形</span><span class="sxs-lookup"><span data-stu-id="d94d8-651">Source and Destination Rectangles</span></span>

<span data-ttu-id="d94d8-652">*來源矩形* 是要顯示的影片畫面部分。</span><span class="sxs-lookup"><span data-stu-id="d94d8-652">The *source rectangle* is the portion of the video frame to display.</span></span> <span data-ttu-id="d94d8-653">它是相對於正規化座標系統所定義，在此系統中，整個影片框架都會佔用座標為 {0，0，1，1} 的矩形。</span><span class="sxs-lookup"><span data-stu-id="d94d8-653">It is defined relative to a normalized coordinate system, in which the entire video frame occupies a rectangle with coordinates {0, 0, 1, 1}.</span></span> <span data-ttu-id="d94d8-654">*目的地矩形* 是在繪製影片畫面的目的介面內的區域。</span><span class="sxs-lookup"><span data-stu-id="d94d8-654">The *destination rectangle* is the area within the destination surface where the video frame is drawn.</span></span> <span data-ttu-id="d94d8-655">標準展示者可讓應用程式藉由呼叫 [**IMFVideoDisplayControl：： SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition)來設定這些矩形。</span><span class="sxs-lookup"><span data-stu-id="d94d8-655">The standard presenter enables an application to set these rectangles by calling [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>

<span data-ttu-id="d94d8-656">有幾個選項可套用來源和目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="d94d8-656">There are several options for applying source and destination rectangles.</span></span> <span data-ttu-id="d94d8-657">第一個選項是讓混音器適用：</span><span class="sxs-lookup"><span data-stu-id="d94d8-657">The first option is to let the mixer apply them:</span></span>

-   <span data-ttu-id="d94d8-658">使用 [**VIDEO_ZOOM_RECT**](video-zoom-rect-attribute.md) 屬性設定來源矩形。</span><span class="sxs-lookup"><span data-stu-id="d94d8-658">Set the source rectangle using the [**VIDEO_ZOOM_RECT**](video-zoom-rect-attribute.md) attribute.</span></span> <span data-ttu-id="d94d8-659">混音器會在 blits 影片至目的地介面時套用來源矩形。</span><span class="sxs-lookup"><span data-stu-id="d94d8-659">The mixer will apply the source rectangle when it blits the video to the destination surface.</span></span> <span data-ttu-id="d94d8-660">混音器的預設來源矩形是整個框架。</span><span class="sxs-lookup"><span data-stu-id="d94d8-660">The mixer's default source rectangle is the entire frame.</span></span>
-   <span data-ttu-id="d94d8-661">將目的地矩形設定為混音器輸出類型中的幾何光圈。</span><span class="sxs-lookup"><span data-stu-id="d94d8-661">Set the destination rectangle as the geometric aperture in the mixer's output type.</span></span> <span data-ttu-id="d94d8-662">如需詳細資訊，請參閱 [協商格式](#negotiating-formats)。</span><span class="sxs-lookup"><span data-stu-id="d94d8-662">For more information, see [Negotiating Formats](#negotiating-formats).</span></span>

<span data-ttu-id="d94d8-663">第二個選項是在 IDirect3DSwapChain9 時套用矩形 **：:P** ，方法是在 **目前** 的方法中指定 *pSourceRect* 和 *pDestRect* 參數。</span><span class="sxs-lookup"><span data-stu-id="d94d8-663">The second option is to apply the rectangles when you **IDirect3DSwapChain9::Present** by specifying the *pSourceRect* and *pDestRect* parameters in the **Present** method.</span></span> <span data-ttu-id="d94d8-664">您可以結合這些選項。</span><span class="sxs-lookup"><span data-stu-id="d94d8-664">You can combine these options.</span></span> <span data-ttu-id="d94d8-665">例如，您可以在混音器上設定來源矩形，但在 **目前** 的方法中套用目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="d94d8-665">For example, you could set the source rectangle on the mixer but apply the destination rectangle in the **Present** method.</span></span>

<span data-ttu-id="d94d8-666">如果應用程式變更目的地矩形或調整視窗大小，您可能需要配置新的表面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-666">If the application changes the destination rectangle or resizes the window, you might need to allocate new surfaces.</span></span> <span data-ttu-id="d94d8-667">如果是，您必須小心將此作業與排程執行緒同步處理。</span><span class="sxs-lookup"><span data-stu-id="d94d8-667">If so, you must be careful to synchronize this operation with your scheduling thread.</span></span> <span data-ttu-id="d94d8-668">在配置新的表面之前，先排清排程佇列並捨棄舊的範例。</span><span class="sxs-lookup"><span data-stu-id="d94d8-668">Flush the scheduling queue and discard the old samples before allocating new surfaces.</span></span>

### <a name="end-of-stream"></a><span data-ttu-id="d94d8-669">資料流程結尾</span><span class="sxs-lookup"><span data-stu-id="d94d8-669">End of Stream</span></span>

<span data-ttu-id="d94d8-670">當 EVR 上的每個輸入資料流程都已結束時，EVR 會將 **MFVP_MESSAGE_ENDOFSTREAM** 訊息傳送給展示者。</span><span class="sxs-lookup"><span data-stu-id="d94d8-670">When every input stream on the EVR has ended, the EVR sends an **MFVP_MESSAGE_ENDOFSTREAM** message to the presenter.</span></span> <span data-ttu-id="d94d8-671">但是，當您收到訊息時，可能會有一些要處理的影片畫面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-671">At the point when you receive the message, however, there might be a few video frames remaining to be processed.</span></span> <span data-ttu-id="d94d8-672">在您回應資料流程結束之前，您必須先清空混音器的所有輸出，並呈現所有其餘的畫面格。</span><span class="sxs-lookup"><span data-stu-id="d94d8-672">Before you respond to the end-of-stream message, you must drain all of the output from the mixer and present all of the remaining frames.</span></span> <span data-ttu-id="d94d8-673">顯示最後一個畫面格之後，將 **EC_COMPLETE** 事件傳送至 EVR。</span><span class="sxs-lookup"><span data-stu-id="d94d8-673">After the last frame is presented, send an **EC_COMPLETE** event to the EVR.</span></span>

<span data-ttu-id="d94d8-674">下一個範例顯示在符合各種條件時傳送 **EC_COMPLETE** 事件的方法。</span><span class="sxs-lookup"><span data-stu-id="d94d8-674">The next example shows a method that sends the **EC_COMPLETE** event if various conditions are met.</span></span> <span data-ttu-id="d94d8-675">否則，它會傳回 S_OK 而不傳送事件：</span><span class="sxs-lookup"><span data-stu-id="d94d8-675">Otherwise, it returns S_OK without sending the event:</span></span>


```C++
HRESULT EVRCustomPresenter::CheckEndOfStream()
{
    if (!m_bEndStreaming)
    {
        // The EVR did not send the MFVP_MESSAGE_ENDOFSTREAM message.
        return S_OK;
    }

    if (m_bSampleNotify)
    {
        // The mixer still has input.
        return S_OK;
    }

    if (m_SamplePool.AreSamplesPending())
    {
        // Samples are still scheduled for rendering.
        return S_OK;
    }

    // Everything is complete. Now we can tell the EVR that we are done.
    NotifyEvent(EC_COMPLETE, (LONG_PTR)S_OK, 0);
    m_bEndStreaming = FALSE;
    return S_OK;
}
```



<span data-ttu-id="d94d8-676">這個方法會檢查下列狀態：</span><span class="sxs-lookup"><span data-stu-id="d94d8-676">This method checks the following states:</span></span>

-   <span data-ttu-id="d94d8-677">如果 *m_fSampleNotify* 變數為 **TRUE**，則表示混音器有一或多個尚未處理過的框架。</span><span class="sxs-lookup"><span data-stu-id="d94d8-677">If the *m_fSampleNotify* variable is **TRUE**, it means the mixer has one or more frames that have not been processed yet.</span></span> <span data-ttu-id="d94d8-678"> (需詳細資訊，請參閱 [處理輸出](#processing-output)) 。</span><span class="sxs-lookup"><span data-stu-id="d94d8-678">(For details, see [Processing Output](#processing-output).)</span></span>
-   <span data-ttu-id="d94d8-679">*M_fEndStreaming* 變數是布林值旗標，其初始值 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="d94d8-679">The *m_fEndStreaming* variable is a Boolean flag whose initial value **FALSE**.</span></span> <span data-ttu-id="d94d8-680">當 EVR 傳送 **MFVP_MESSAGE_ENDOFSTREAM** 訊息時，展示者會將旗標設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="d94d8-680">The presenter sets the flag to **TRUE** when the EVR sends the **MFVP_MESSAGE_ENDOFSTREAM** message.</span></span>
-   <span data-ttu-id="d94d8-681">只要有 `AreSamplesPending` 一或多個框架在已排程的佇列中等待，方法會假設為傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="d94d8-681">The `AreSamplesPending` method is assumed to return **TRUE** as long as one or more frames are waiting in the scheduled queue.</span></span>

<span data-ttu-id="d94d8-682">在 [**IMFVideoPresenter：:P rocessmessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) 方法中，將 *M_fEndStreaming* 設定為 **TRUE** ，並在 `CheckEndOfStream` EVR 傳送 **MFVP_MESSAGE_ENDOFSTREAM** 訊息時呼叫：</span><span class="sxs-lookup"><span data-stu-id="d94d8-682">In the [**IMFVideoPresenter::ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) method, set *m_fEndStreaming* to **TRUE** and call `CheckEndOfStream` when the EVR sends the **MFVP_MESSAGE_ENDOFSTREAM** message:</span></span>


```C++
HRESULT EVRCustomPresenter::ProcessMessage(
    MFVP_MESSAGE_TYPE eMessage,
    ULONG_PTR ulParam
    )
{
    HRESULT hr = S_OK;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    switch (eMessage)
    {
    // Flush all pending samples.
    case MFVP_MESSAGE_FLUSH:
        hr = Flush();
        break;

    // Renegotiate the media type with the mixer.
    case MFVP_MESSAGE_INVALIDATEMEDIATYPE:
        hr = RenegotiateMediaType();
        break;

    // The mixer received a new input sample.
    case MFVP_MESSAGE_PROCESSINPUTNOTIFY:
        hr = ProcessInputNotify();
        break;

    // Streaming is about to start.
    case MFVP_MESSAGE_BEGINSTREAMING:
        hr = BeginStreaming();
        break;

    // Streaming has ended. (The EVR has stopped.)
    case MFVP_MESSAGE_ENDSTREAMING:
        hr = EndStreaming();
        break;

    // All input streams have ended.
    case MFVP_MESSAGE_ENDOFSTREAM:
        // Set the EOS flag.
        m_bEndStreaming = TRUE;
        // Check if it's time to send the EC_COMPLETE event to the EVR.
        hr = CheckEndOfStream();
        break;

    // Frame-stepping is starting.
    case MFVP_MESSAGE_STEP:
        hr = PrepareFrameStep(LODWORD(ulParam));
        break;

    // Cancels frame-stepping.
    case MFVP_MESSAGE_CANCELSTEP:
        hr = CancelFrameStep();
        break;

    default:
        hr = E_INVALIDARG; // Unknown message. This case should never occur.
        break;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



<span data-ttu-id="d94d8-683">此外， `CheckEndOfStream` 如果混音器的 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 方法傳回 **MF_E_TRANSFORM_NEED_MORE_INPUT**，則呼叫。</span><span class="sxs-lookup"><span data-stu-id="d94d8-683">In addition, call `CheckEndOfStream` if the mixer's [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method returns **MF_E_TRANSFORM_NEED_MORE_INPUT**.</span></span> <span data-ttu-id="d94d8-684">此錯誤碼表示混音器沒有其他輸入範例 (請參閱 [處理輸出](#processing-output)) 。</span><span class="sxs-lookup"><span data-stu-id="d94d8-684">This error code indicates that the mixer has no more input samples (see [Processing Output](#processing-output)).</span></span>

## <a name="frame-stepping"></a><span data-ttu-id="d94d8-685">畫面逐步執行</span><span class="sxs-lookup"><span data-stu-id="d94d8-685">Frame Stepping</span></span>

<span data-ttu-id="d94d8-686">EVR 的設計是為了支援在 DirectShow 中逐步執行，並在媒體基礎中進行清理。</span><span class="sxs-lookup"><span data-stu-id="d94d8-686">The EVR is designed to support frame stepping in DirectShow and scrubbing in Media Foundation.</span></span> <span data-ttu-id="d94d8-687">框架逐步執行和清除在概念上類似。</span><span class="sxs-lookup"><span data-stu-id="d94d8-687">Frame stepping and scrubbing are conceptually similar.</span></span> <span data-ttu-id="d94d8-688">在這兩種情況下，應用程式一次都會要求一個影片畫面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-688">In both cases, the application requests one video frame at a time.</span></span> <span data-ttu-id="d94d8-689">在內部，展示者會使用相同的機制來執行這兩項功能。</span><span class="sxs-lookup"><span data-stu-id="d94d8-689">Internally, the presenter uses the same mechanism to implement both features.</span></span>

<span data-ttu-id="d94d8-690">DirectShow 中的框架逐步執行方式如下：</span><span class="sxs-lookup"><span data-stu-id="d94d8-690">Frame stepping in DirectShow works as follows:</span></span>

-   <span data-ttu-id="d94d8-691">應用程式會呼叫 [**IVideoFrameStep：： Step**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-step)。</span><span class="sxs-lookup"><span data-stu-id="d94d8-691">The application calls [**IVideoFrameStep::Step**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-step).</span></span> <span data-ttu-id="d94d8-692">*DwSteps* 參數中提供的步驟數目。</span><span class="sxs-lookup"><span data-stu-id="d94d8-692">The number of steps is given in the *dwSteps* parameter.</span></span> <span data-ttu-id="d94d8-693">EVR 會將 **MFVP_MESSAGE_STEP** 訊息傳送給展示者，其中 (*ulParam*) 的訊息參數是步驟數目。</span><span class="sxs-lookup"><span data-stu-id="d94d8-693">The EVR sends an **MFVP_MESSAGE_STEP** message to the presenter, where the message parameter (*ulParam*) is the number of steps.</span></span>
-   <span data-ttu-id="d94d8-694">如果應用程式呼叫 [**IVideoFrameStep：： CancelStep**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-cancelstep) 或變更圖形狀態 (執行中、已暫停或已停止) ，EVR 就會傳送 **MFVP_MESSAGE_CANCELSTEP** 訊息。</span><span class="sxs-lookup"><span data-stu-id="d94d8-694">If the application calls [**IVideoFrameStep::CancelStep**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-cancelstep) or changes the graph state (running, paused, or stopped), the EVR sends an **MFVP_MESSAGE_CANCELSTEP** message.</span></span>

<span data-ttu-id="d94d8-695">媒體基礎中的清除作業的運作方式如下：</span><span class="sxs-lookup"><span data-stu-id="d94d8-695">Scrubbing in Media Foundation works as follows:</span></span>

-   <span data-ttu-id="d94d8-696">應用程式會藉由呼叫 [**IMFRateControl：： SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)，將播放速率設定為零。</span><span class="sxs-lookup"><span data-stu-id="d94d8-696">The application sets the playback rate to zero by calling [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate).</span></span>
-   <span data-ttu-id="d94d8-697">若要呈現新的框架，應用程式會以所需的位置呼叫 [**IMFMediaSession：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) 。</span><span class="sxs-lookup"><span data-stu-id="d94d8-697">To render a new frame, the application calls [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) with the desired position.</span></span> <span data-ttu-id="d94d8-698">EVR 會傳送 *ulParam* 等於1的 **MFVP_MESSAGE_STEP** 訊息。</span><span class="sxs-lookup"><span data-stu-id="d94d8-698">The EVR sends an **MFVP_MESSAGE_STEP** message with *ulParam* equal to 1.</span></span>
-   <span data-ttu-id="d94d8-699">若要停止清除，應用程式會將播放速率設定為非零值。</span><span class="sxs-lookup"><span data-stu-id="d94d8-699">To stop scrubbing, the application sets the playback rate to a nonzero value.</span></span> <span data-ttu-id="d94d8-700">EVR 會傳送 **MFVP_MESSAGE_CANCELSTEP** 訊息。</span><span class="sxs-lookup"><span data-stu-id="d94d8-700">The EVR sends the **MFVP_MESSAGE_CANCELSTEP** message.</span></span>

<span data-ttu-id="d94d8-701">收到 **MFVP_MESSAGE_STEP** 訊息之後，展示者會等待目標框架到達。</span><span class="sxs-lookup"><span data-stu-id="d94d8-701">After receiving the **MFVP_MESSAGE_STEP** message, the presenter waits for the target frame to arrive.</span></span> <span data-ttu-id="d94d8-702">如果步驟數目為 *N*，則展示者會捨棄下一個 (*n* -1) 範例，並提供 *N* 個範例。</span><span class="sxs-lookup"><span data-stu-id="d94d8-702">If the number of steps is *N*, the presenter discards the next (*N* - 1) samples and presents the *N* th sample.</span></span> <span data-ttu-id="d94d8-703">當展示者完成框架步驟時，會將 [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) 事件傳送至 EVR，並將 *LParam1* 設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="d94d8-703">When the presenter completes the frame step, it sends an [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) event to the EVR with *lParam1* set to **FALSE**.</span></span> <span data-ttu-id="d94d8-704">此外，如果播放率為零，則展示者會傳送 [**EC_SCRUB_TIME**](../directshow/ec-scrub-time.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="d94d8-704">In addition, if the playback rate is zero, the presenter sends an [**EC_SCRUB_TIME**](../directshow/ec-scrub-time.md) event.</span></span> <span data-ttu-id="d94d8-705">如果 EVR 在畫面格步驟作業仍處於暫止狀態時取消框架逐步執行，則展示者會傳送將 *lParam1* 設為 **TRUE** 的 **EC_STEP_COMPLETE** 事件。</span><span class="sxs-lookup"><span data-stu-id="d94d8-705">If the EVR cancels frame stepping while a frame-step operation is still pending, the presenter sends an **EC_STEP_COMPLETE** event with *lParam1* set to **TRUE**.</span></span>

<span data-ttu-id="d94d8-706">應用程式可以執行多個步驟或清除多次，讓展示者在取得 **MFVP_MESSAGE_CANCELSTEP** 訊息之前，可能會收到多 **MFVP_MESSAGE_STEP** 的訊息。</span><span class="sxs-lookup"><span data-stu-id="d94d8-706">The application can frame step or scrub multiple times, so the presenter might receive multiple **MFVP_MESSAGE_STEP** messages before it gets an **MFVP_MESSAGE_CANCELSTEP** message.</span></span> <span data-ttu-id="d94d8-707">此外，展示者也可以在時鐘開始之前或時鐘正在執行時，接收 **MFVP_MESSAGE_STEP** 訊息。</span><span class="sxs-lookup"><span data-stu-id="d94d8-707">Also, the presenter can receive the **MFVP_MESSAGE_STEP** message before the clock starts or while the clock is running.</span></span>

### <a name="implementing-frame-stepping"></a><span data-ttu-id="d94d8-708">執行框架逐步執行</span><span class="sxs-lookup"><span data-stu-id="d94d8-708">Implementing Frame Stepping</span></span>

<span data-ttu-id="d94d8-709">本節說明用來執行框架逐步執行的演算法。</span><span class="sxs-lookup"><span data-stu-id="d94d8-709">This section describes an algorithm to implement frame stepping.</span></span> <span data-ttu-id="d94d8-710">畫面逐步執行演算法使用下列變數：</span><span class="sxs-lookup"><span data-stu-id="d94d8-710">The frame stepping algorithm uses the following variables:</span></span>

-   <span data-ttu-id="d94d8-711">*step_count*。</span><span class="sxs-lookup"><span data-stu-id="d94d8-711">*step_count*.</span></span> <span data-ttu-id="d94d8-712">不帶正負號的整數，指定目前畫面執行作業中的步驟數目。</span><span class="sxs-lookup"><span data-stu-id="d94d8-712">An unsigned integer that specifies the number of steps in the current frame stepping operation.</span></span>
-   <span data-ttu-id="d94d8-713">*step_queue*。</span><span class="sxs-lookup"><span data-stu-id="d94d8-713">*step_queue*.</span></span> <span data-ttu-id="d94d8-714">[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)指標的佇列。</span><span class="sxs-lookup"><span data-stu-id="d94d8-714">A queue of [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointers.</span></span>
-   <span data-ttu-id="d94d8-715">*step_state*。</span><span class="sxs-lookup"><span data-stu-id="d94d8-715">*step_state*.</span></span> <span data-ttu-id="d94d8-716">在任何時候，展示者都可以是下列其中一種狀態，與畫面格逐步執行有關：</span><span class="sxs-lookup"><span data-stu-id="d94d8-716">At any time, the presenter can be in one of the following states with respect to frame stepping:</span></span> 

    | <span data-ttu-id="d94d8-717">州</span><span class="sxs-lookup"><span data-stu-id="d94d8-717">State</span></span>         | <span data-ttu-id="d94d8-718">描述</span><span class="sxs-lookup"><span data-stu-id="d94d8-718">Description</span></span>                                                                                                                                                                                                     |
    |---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="d94d8-719">NOT_STEPPING</span><span class="sxs-lookup"><span data-stu-id="d94d8-719">NOT_STEPPING</span></span> | <span data-ttu-id="d94d8-720">不是畫面的逐步執行。</span><span class="sxs-lookup"><span data-stu-id="d94d8-720">Not frame stepping.</span></span>                                                                                                                                                                                             |
    | <span data-ttu-id="d94d8-721">等候</span><span class="sxs-lookup"><span data-stu-id="d94d8-721">WAITING</span></span>       | <span data-ttu-id="d94d8-722">展示者已收到 **MFVP_MESSAGE_STEP** 的訊息，但時鐘尚未啟動。</span><span class="sxs-lookup"><span data-stu-id="d94d8-722">The presenter has received the **MFVP_MESSAGE_STEP** message, but the clock has not started.</span></span>                                                                                                                  |
    | <span data-ttu-id="d94d8-723">PENDING</span><span class="sxs-lookup"><span data-stu-id="d94d8-723">PENDING</span></span>       | <span data-ttu-id="d94d8-724">展示者已收到 **MFVP_MESSAGE_STEP** 的訊息，而且時鐘已開始，但展示者正在等候接收目標框架。</span><span class="sxs-lookup"><span data-stu-id="d94d8-724">The presenter has received the **MFVP_MESSAGE_STEP** message and the clock has started, but the presenter is waiting to receive the target frame.</span></span>                                                             |
    | <span data-ttu-id="d94d8-725">計畫</span><span class="sxs-lookup"><span data-stu-id="d94d8-725">SCHEDULED</span></span>     | <span data-ttu-id="d94d8-726">展示者已收到目標框架，並已將它排程為展示，但尚未呈現畫面格。</span><span class="sxs-lookup"><span data-stu-id="d94d8-726">The presenter has received the target frame and has scheduled it for presentation, but the frame has not been presented.</span></span>                                                                                        |
    | <span data-ttu-id="d94d8-727">完成</span><span class="sxs-lookup"><span data-stu-id="d94d8-727">COMPLETE</span></span>      | <span data-ttu-id="d94d8-728">展示者已顯示目標框架並傳送 [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) 事件，並且正在等候下一個 **MFVP_MESSAGE_STEP** 或 **MFVP_MESSAGE_CANCELSTEP** 訊息。</span><span class="sxs-lookup"><span data-stu-id="d94d8-728">The presenter has presented the target frame and sent the [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) event, and is waiting for the next **MFVP_MESSAGE_STEP** or **MFVP_MESSAGE_CANCELSTEP** message.</span></span> |

    

     

    <span data-ttu-id="d94d8-729">這些狀態與展示 [者狀態](#presenter-states)中所列的展示者狀態無關。</span><span class="sxs-lookup"><span data-stu-id="d94d8-729">These states are independent of the presenter states listed in the section [Presenter States](#presenter-states).</span></span>

<span data-ttu-id="d94d8-730">下列程式是針對框架逐步執行演算法所定義：</span><span class="sxs-lookup"><span data-stu-id="d94d8-730">The following procedures are defined for the frame-stepping algorithm:</span></span>

<span data-ttu-id="d94d8-731">PrepareFrameStep 程式</span><span class="sxs-lookup"><span data-stu-id="d94d8-731">PrepareFrameStep Procedure</span></span>

1.  <span data-ttu-id="d94d8-732">遞增 *step_count*。</span><span class="sxs-lookup"><span data-stu-id="d94d8-732">Increment *step_count*.</span></span>
2.  <span data-ttu-id="d94d8-733">將 *step_state* 設定為 [等待中]。</span><span class="sxs-lookup"><span data-stu-id="d94d8-733">Set *step_state* to WAITING.</span></span>
3.  <span data-ttu-id="d94d8-734">如果時鐘正在執行，請呼叫 StartFrameStep。</span><span class="sxs-lookup"><span data-stu-id="d94d8-734">If the clock is running, call StartFrameStep.</span></span>

<span data-ttu-id="d94d8-735">StartFrameStep 程式</span><span class="sxs-lookup"><span data-stu-id="d94d8-735">StartFrameStep Procedure</span></span>

1.  <span data-ttu-id="d94d8-736">如果 *step_state* 等於等候，請將 *STEP_STATE* 設定為擱置中。</span><span class="sxs-lookup"><span data-stu-id="d94d8-736">If *step_state* equals WAITING, set *step_state* to PENDING.</span></span> <span data-ttu-id="d94d8-737">針對 *step_queue* 中的每個範例，呼叫 DeliverFrameStepSample。</span><span class="sxs-lookup"><span data-stu-id="d94d8-737">For each sample in *step_queue*, call DeliverFrameStepSample.</span></span>
2.  <span data-ttu-id="d94d8-738">如果 *step_state* 等於 NOT_STEPPING，請從 *step_queue* 中移除任何範例，並針對簡報進行排程。</span><span class="sxs-lookup"><span data-stu-id="d94d8-738">If *step_state* equals NOT_STEPPING, remove any samples from *step_queue* and schedule them for presentation.</span></span>

<span data-ttu-id="d94d8-739">CompleteFrameStep 程式</span><span class="sxs-lookup"><span data-stu-id="d94d8-739">CompleteFrameStep Procedure</span></span>

1.  <span data-ttu-id="d94d8-740">將 *step_state* 設定為 [完成]。</span><span class="sxs-lookup"><span data-stu-id="d94d8-740">Set *step_state* to COMPLETE.</span></span>
2.  <span data-ttu-id="d94d8-741">傳送具有 *lParam1*  =  **FALSE** 的 EC_STEP_COMPLETE 事件。</span><span class="sxs-lookup"><span data-stu-id="d94d8-741">Send the EC_STEP_COMPLETE event with *lParam1* = **FALSE**.</span></span>
3.  <span data-ttu-id="d94d8-742">如果頻率為零，請傳送 **EC_SCRUB_TIME** 事件與取樣時間。</span><span class="sxs-lookup"><span data-stu-id="d94d8-742">If the clock rate is zero, send the **EC_SCRUB_TIME** event with the sample time.</span></span>

<span data-ttu-id="d94d8-743">DeliverFrameStepSample 程式</span><span class="sxs-lookup"><span data-stu-id="d94d8-743">DeliverFrameStepSample Procedure</span></span>

1.  <span data-ttu-id="d94d8-744">如果頻率為零，且 *取樣時間*  +  *範例持續時間長度* 為零  <  \*\*，請捨棄範例。</span><span class="sxs-lookup"><span data-stu-id="d94d8-744">If the clock rate is zero and *sample time* + *sample duration* < *clock time*, discard the sample.</span></span> <span data-ttu-id="d94d8-745">結束。</span><span class="sxs-lookup"><span data-stu-id="d94d8-745">Exit.</span></span>
2.  <span data-ttu-id="d94d8-746">如果 *step_state* 等於 [已排程] 或 [已完成]，請將範例新增至 *step_queue*。</span><span class="sxs-lookup"><span data-stu-id="d94d8-746">If *step_state* equals SCHEDULED or COMPLETE, add the sample to *step_queue*.</span></span> <span data-ttu-id="d94d8-747">結束。</span><span class="sxs-lookup"><span data-stu-id="d94d8-747">Exit.</span></span>
3.  <span data-ttu-id="d94d8-748">遞減 *step_count*。</span><span class="sxs-lookup"><span data-stu-id="d94d8-748">Decrement *step_count*.</span></span>
4.  <span data-ttu-id="d94d8-749">如果 *step_count* > 0，請捨棄範例。</span><span class="sxs-lookup"><span data-stu-id="d94d8-749">If *step_count* > 0, discard the sample.</span></span> <span data-ttu-id="d94d8-750">結束。</span><span class="sxs-lookup"><span data-stu-id="d94d8-750">Exit.</span></span>
5.  <span data-ttu-id="d94d8-751">如果 *step_state* 等於等候，請將範例新增至 *step_queue*。</span><span class="sxs-lookup"><span data-stu-id="d94d8-751">If *step_state* equals WAITING, add the sample to *step_queue*.</span></span> <span data-ttu-id="d94d8-752">結束。</span><span class="sxs-lookup"><span data-stu-id="d94d8-752">Exit.</span></span>
6.  <span data-ttu-id="d94d8-753">排程簡報的範例。</span><span class="sxs-lookup"><span data-stu-id="d94d8-753">Schedule the sample for presentation.</span></span>
7.  <span data-ttu-id="d94d8-754">將 *step_state* 設定為 [已排程]。</span><span class="sxs-lookup"><span data-stu-id="d94d8-754">Set *step_state* to SCHEDULED.</span></span>

<span data-ttu-id="d94d8-755">CancelFrameStep 程式</span><span class="sxs-lookup"><span data-stu-id="d94d8-755">CancelFrameStep Procedure</span></span>

1.  <span data-ttu-id="d94d8-756">將 *step_state* 設定為 NOT_STEPPING</span><span class="sxs-lookup"><span data-stu-id="d94d8-756">Set *step_state* to NOT_STEPPING</span></span>
2.  <span data-ttu-id="d94d8-757">將 *step_count* 重設為零。</span><span class="sxs-lookup"><span data-stu-id="d94d8-757">Reset *step_count* to zero.</span></span>
3.  <span data-ttu-id="d94d8-758">如果先前的 *step_state* 值為「等待中」、「擱置中」或「已排程」，則傳送具有 *lParam1*  =  **TRUE** 的 EC_STEP_COMPLETE。</span><span class="sxs-lookup"><span data-stu-id="d94d8-758">If the previous value of *step_state* was WAITING, PENDING, or SCHEDULED, send EC_STEP_COMPLETE with *lParam1* = **TRUE**.</span></span>

<span data-ttu-id="d94d8-759">呼叫這些程式，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d94d8-759">Call these procedures as follows:</span></span>



| <span data-ttu-id="d94d8-760">展示者訊息或方法</span><span class="sxs-lookup"><span data-stu-id="d94d8-760">Presenter message or method</span></span>                                                   | <span data-ttu-id="d94d8-761">程序</span><span class="sxs-lookup"><span data-stu-id="d94d8-761">Procedure</span></span>           |
|-------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="d94d8-762">**MFVP_MESSAGE_STEP** 訊息</span><span class="sxs-lookup"><span data-stu-id="d94d8-762">**MFVP_MESSAGE_STEP** message</span></span>                                               | `PrepareFrameStep`  |
| <span data-ttu-id="d94d8-763">**MFVP_MESSAGE_STEP** 訊息</span><span class="sxs-lookup"><span data-stu-id="d94d8-763">**MFVP_MESSAGE_STEP** message</span></span>                                               | `CancelStep`        |
| [<span data-ttu-id="d94d8-764">**IMFClockStateSink::OnClockStart**</span><span class="sxs-lookup"><span data-stu-id="d94d8-764">**IMFClockStateSink::OnClockStart**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)     | `StartFrameStep`    |
| [<span data-ttu-id="d94d8-765">**IMFClockStateSink::OnClockRestart**</span><span class="sxs-lookup"><span data-stu-id="d94d8-765">**IMFClockStateSink::OnClockRestart**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) | `StartFrameStep`    |
| <span data-ttu-id="d94d8-766">[**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) 回呼</span><span class="sxs-lookup"><span data-stu-id="d94d8-766">[**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) callback</span></span>                         | `CompleteFrameStep` |
| [<span data-ttu-id="d94d8-767">**IMFClockStateSink::OnClockStop**</span><span class="sxs-lookup"><span data-stu-id="d94d8-767">**IMFClockStateSink::OnClockStop**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop)       | `CancelFrameStep`   |
| [<span data-ttu-id="d94d8-768">**IMFClockStateSink::OnClockSetRate**</span><span class="sxs-lookup"><span data-stu-id="d94d8-768">**IMFClockStateSink::OnClockSetRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) | `CancelFrameStep`   |



 

<span data-ttu-id="d94d8-769">下列流程圖顯示畫面的逐步執行程式。</span><span class="sxs-lookup"><span data-stu-id="d94d8-769">The following flow chart shows the frame-stepping procedures.</span></span>

![顯示路徑的流程圖，其開頭為 mfvp \- message \- step and mfvp \- message \- processinputnotify and end at "state = complete"](images/d9baaa67-a9b1-4e27-9a32-08a45b0677d3.gif)

## <a name="setting-the-presenter-on-the-evr"></a><span data-ttu-id="d94d8-771">在 EVR 上設定展示者</span><span class="sxs-lookup"><span data-stu-id="d94d8-771">Setting the Presenter on the EVR</span></span>

<span data-ttu-id="d94d8-772">完成展示者後，下一個步驟是設定 EVR 來使用它。</span><span class="sxs-lookup"><span data-stu-id="d94d8-772">After implementing the presenter, the next step is to configure the EVR to use it.</span></span>

### <a name="setting-the-presenter-in-directshow"></a><span data-ttu-id="d94d8-773">在 DirectShow 中設定展示者</span><span class="sxs-lookup"><span data-stu-id="d94d8-773">Setting the Presenter in DirectShow</span></span>

<span data-ttu-id="d94d8-774">在 DirectShow 應用程式中，在 EVR 上設定展示者，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d94d8-774">In a DirectShow application, set the presenter on the EVR as follows:</span></span>

1.  <span data-ttu-id="d94d8-775">藉由呼叫 **CoCreateInstance** 來建立 EVR 篩選。</span><span class="sxs-lookup"><span data-stu-id="d94d8-775">Create the EVR filter by calling **CoCreateInstance**.</span></span> <span data-ttu-id="d94d8-776">**CLSID_ENHANCEDVIDEORENDERER** CLSID。</span><span class="sxs-lookup"><span data-stu-id="d94d8-776">The CLSID is **CLSID_EnhancedVideoRenderer**.</span></span>
2.  <span data-ttu-id="d94d8-777">將 EVR 新增至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="d94d8-777">Add the EVR to the filter graph.</span></span>
3.  <span data-ttu-id="d94d8-778">建立您的展示者實例。</span><span class="sxs-lookup"><span data-stu-id="d94d8-778">Create an instance of your presenter.</span></span> <span data-ttu-id="d94d8-779">您的展示者可以透過 **IClassFactory** 支援標準 COM 物件建立，但這並不是必要的。</span><span class="sxs-lookup"><span data-stu-id="d94d8-779">Your presenter can support standard COM object creation through **IClassFactory**, but this is not mandatory.</span></span>
4.  <span data-ttu-id="d94d8-780">查詢 [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) 介面的 EVR 篩選準則。</span><span class="sxs-lookup"><span data-stu-id="d94d8-780">Query the EVR filter for the [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) interface.</span></span>
5.  <span data-ttu-id="d94d8-781">呼叫 [**IMFVideoRenderer：： InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer)。</span><span class="sxs-lookup"><span data-stu-id="d94d8-781">Call [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span></span>

### <a name="setting-the-presenter-in-media-foundation"></a><span data-ttu-id="d94d8-782">在媒體基礎中設定展示者</span><span class="sxs-lookup"><span data-stu-id="d94d8-782">Setting the Presenter in Media Foundation</span></span>

<span data-ttu-id="d94d8-783">在媒體基礎中，您有數個選項，取決於您是建立 EVR 媒體接收器或 EVR 啟用物件。</span><span class="sxs-lookup"><span data-stu-id="d94d8-783">In Media Foundation, you have several options, depending on whether you create the EVR media sink or the EVR activation object.</span></span> <span data-ttu-id="d94d8-784">如需啟用物件的詳細資訊，請參閱 [啟用物件](activation-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="d94d8-784">For more information about activation objects, see [Activation Objects](activation-objects.md).</span></span>

<span data-ttu-id="d94d8-785">針對 EVR 媒體接收器，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="d94d8-785">For the EVR media sink, do the following:</span></span>

1.  <span data-ttu-id="d94d8-786">呼叫 [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) 來建立媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="d94d8-786">Call [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) to create the media sink.</span></span>
2.  <span data-ttu-id="d94d8-787">建立您的展示者實例。</span><span class="sxs-lookup"><span data-stu-id="d94d8-787">Create an instance of your presenter.</span></span>
3.  <span data-ttu-id="d94d8-788">查詢 EVR 媒體接收器中的 [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) 介面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-788">Query the EVR media sink for the [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) interface.</span></span>
4.  <span data-ttu-id="d94d8-789">呼叫 [**IMFVideoRenderer：： InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer)。</span><span class="sxs-lookup"><span data-stu-id="d94d8-789">Call [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span></span>

<span data-ttu-id="d94d8-790">針對 EVR 啟用物件，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="d94d8-790">For the EVR activation object, do the following:</span></span>

1.  <span data-ttu-id="d94d8-791">呼叫 [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) 來建立啟用物件。</span><span class="sxs-lookup"><span data-stu-id="d94d8-791">Call [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) to create the activation object.</span></span>
2.  <span data-ttu-id="d94d8-792">在啟用物件上設定下列其中一個屬性：</span><span class="sxs-lookup"><span data-stu-id="d94d8-792">Set one of the following attributes on the activation object:</span></span> 

    | <span data-ttu-id="d94d8-793">屬性</span><span class="sxs-lookup"><span data-stu-id="d94d8-793">Attribute</span></span>                                                                                                         | <span data-ttu-id="d94d8-794">描述</span><span class="sxs-lookup"><span data-stu-id="d94d8-794">Description</span></span>                                                                                                                                                                                                                               |
    |-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="d94d8-795">**MF_ACTI加值稅E_CUSTOM_VIDEO_PRESENTER_ACTI加值稅E**</span><span class="sxs-lookup"><span data-stu-id="d94d8-795">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE**</span></span>](mf-activate-custom-video-presenter-activate-attribute.md) | <span data-ttu-id="d94d8-796">展示者的啟用物件指標。</span><span class="sxs-lookup"><span data-stu-id="d94d8-796">Pointer to an activation object for the presenter.</span></span><br/> <span data-ttu-id="d94d8-797">使用這個旗標時，您必須為您的展示者提供啟用物件。</span><span class="sxs-lookup"><span data-stu-id="d94d8-797">With this flag, you must provide an activation object for your presenter.</span></span> <span data-ttu-id="d94d8-798">啟用物件必須執行 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面。</span><span class="sxs-lookup"><span data-stu-id="d94d8-798">The activation object must implement the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span><br/> |
    | [<span data-ttu-id="d94d8-799">**MF_ACTI加值稅E_CUSTOM_VIDEO_PRESENTER_CLSID**</span><span class="sxs-lookup"><span data-stu-id="d94d8-799">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID**</span></span>](mf-activate-custom-video-presenter-clsid-attribute.md)       | <span data-ttu-id="d94d8-800">展示者的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="d94d8-800">CLSID of the presenter.</span></span><br/> <span data-ttu-id="d94d8-801">使用這個旗標時，您的展示者必須支援透過 **IClassFactory** 建立標準 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="d94d8-801">With this flag, your presenter must support standard COM object creation through **IClassFactory**.</span></span><br/>                                                                                         |

    

     

3.  <span data-ttu-id="d94d8-802">（選擇性）在啟用物件上設定 [**MF_ACTI加值稅E_CUSTOM_VIDEO_PRESENTER_FLAGS**](mf-activate-custom-video-presenter-flags-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="d94d8-802">Optionally, set the [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS**](mf-activate-custom-video-presenter-flags-attribute.md) attribute on the activation object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d94d8-803">相關主題</span><span class="sxs-lookup"><span data-stu-id="d94d8-803">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d94d8-804">增強的影片轉譯器</span><span class="sxs-lookup"><span data-stu-id="d94d8-804">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="d94d8-805">EVRPresenter 範例</span><span class="sxs-lookup"><span data-stu-id="d94d8-805">EVRPresenter Sample</span></span>](evrpresenter-sample.md)
</dt> </dl>

 

 
