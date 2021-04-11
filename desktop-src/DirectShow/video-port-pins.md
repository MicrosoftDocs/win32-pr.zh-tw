---
description: 影片埠釘選
ms.assetid: a6be24e5-7937-48f1-abeb-3f29c3deeafd
title: 影片埠釘選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d13ab4ad63995dd38460bf29064035c9c1802dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850319"
---
# <a name="video-port-pins"></a><span data-ttu-id="3b5d9-103">影片埠釘選</span><span class="sxs-lookup"><span data-stu-id="3b5d9-103">Video Port Pins</span></span>

<span data-ttu-id="3b5d9-104">具有硬體視訊連接埠的 capture 裝置，可能會在 Microsoft® DirectX®中使用 (VPE) 的影片埠擴充功能。</span><span class="sxs-lookup"><span data-stu-id="3b5d9-104">A capture device with a hardware video port might use the video port extensions (VPE) in Microsoft® DirectX®.</span></span> <span data-ttu-id="3b5d9-105">如果是的話，capture 篩選器將會有一個影片埠 (VP) pin。</span><span class="sxs-lookup"><span data-stu-id="3b5d9-105">If so, the capture filter will have a video port (VP) pin.</span></span> <span data-ttu-id="3b5d9-106">從 VP 釘選到篩選圖形都沒有影片資料。</span><span class="sxs-lookup"><span data-stu-id="3b5d9-106">No video data travels from the VP pin through the filter graph.</span></span> <span data-ttu-id="3b5d9-107">相反地，會在硬體中產生影片畫面，並直接傳送至視訊記憶體。</span><span class="sxs-lookup"><span data-stu-id="3b5d9-107">Instead, video frames are produced in hardware and sent directly to video memory.</span></span> <span data-ttu-id="3b5d9-108">VP pin 允許將控制訊息傳送至硬體。</span><span class="sxs-lookup"><span data-stu-id="3b5d9-108">The VP pin allows control messages to be sent to the hardware.</span></span>

<span data-ttu-id="3b5d9-109">即使您的應用程式只執行沒有預覽的檔案捕獲，也請務必連接 VP pin 碼。</span><span class="sxs-lookup"><span data-stu-id="3b5d9-109">It is important to connect the VP pin, even if your application only performs file capture with no preview.</span></span> <span data-ttu-id="3b5d9-110">如果您讓 pin 不連線，圖形將無法正確執行。</span><span class="sxs-lookup"><span data-stu-id="3b5d9-110">If you leave the pin unconnected, the graph will not run correctly.</span></span> <span data-ttu-id="3b5d9-111">這與不需要連線的預覽 pin 不同。</span><span class="sxs-lookup"><span data-stu-id="3b5d9-111">This is different from preview pins, which do not have to be connected.</span></span>

<span data-ttu-id="3b5d9-112">不同的 DirectShow 影片轉譯器提供了 VP 釘選的不同支援：</span><span class="sxs-lookup"><span data-stu-id="3b5d9-112">The different DirectShow video renderers provide varying support for VP pins:</span></span>

-   <span data-ttu-id="3b5d9-113">影片轉譯器：在重迭 [混音](overlay-mixer-filter.md) 器篩選器上將 VP 釘選到針腳0，並將覆迭混音器篩選器連線到影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="3b5d9-113">Video Renderer: Connect the VP pin to pin 0 on the [Overlay Mixer](overlay-mixer-filter.md) filter, and connect the Overlay Mixer filter to the Video Renderer.</span></span>
-   <span data-ttu-id="3b5d9-114">VMR-7：將 VP 釘選到 [影片埠管理員](video-port-manager.md) 篩選器，並將影片埠管理員連接到 VMR-7。</span><span class="sxs-lookup"><span data-stu-id="3b5d9-114">VMR-7: Connect the VP pin to the [Video Port Manager](video-port-manager.md) filter, and connect the Video Port Manager to the VMR-7.</span></span>
-   <span data-ttu-id="3b5d9-115">VMR-9：如果裝置具有 VP 釘選，您就無法使用 VMR-9，因為 Direct3D 9 不支援影片埠。</span><span class="sxs-lookup"><span data-stu-id="3b5d9-115">VMR-9: You cannot use the VMR-9 if the device has a VP pin, because Direct3D 9 does not support video ports.</span></span> <span data-ttu-id="3b5d9-116">請使用影片轉譯器或 VMR-7。</span><span class="sxs-lookup"><span data-stu-id="3b5d9-116">Use either the Video Renderer or the VMR-7.</span></span>

<span data-ttu-id="3b5d9-117">針對影片埠案例，建議使用重迭混音器和影片轉譯器，而不是所有的驅動程式都支援影片埠管理員，因為並非所有驅動程式都支援視訊連接埠管理員。</span><span class="sxs-lookup"><span data-stu-id="3b5d9-117">For video port scenarios, the Overlay Mixer and Video Renderer are recommended over the Video Port Manager and VMR-7, because not all drivers support the Video Port Manager.</span></span> <span data-ttu-id="3b5d9-118">一般而言，重迭混音器是影片埠最可靠的選項。</span><span class="sxs-lookup"><span data-stu-id="3b5d9-118">In general, the Overlay Mixer is the most reliable option for video ports.</span></span>

<span data-ttu-id="3b5d9-119">如果有 VP 釘選， [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) 方法會自動插入重迭混音器。</span><span class="sxs-lookup"><span data-stu-id="3b5d9-119">The [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method automatically inserts the Overlay Mixer if there is a VP pin.</span></span> <span data-ttu-id="3b5d9-120">如果您要在不使用這個方法的情況下建立圖形，您應該檢查 capture 篩選器上是否有影片埠 pin，如果有的話，請將它連接到覆迭混音器篩選器，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="3b5d9-120">If you are building the graph without using this method, you should check for a video port pin on the capture filter, and if one is present, connect it to the Overlay Mixer filter, as shown in the following diagram.</span></span>

![將影片埠 pin 連接到重迭混音器篩選器。](images/vidcap11.png)

<span data-ttu-id="3b5d9-122">您可以使用 [**ICaptureGraphBuilder2：： FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) 方法，在 capture 篩選器上搜尋 VP 釘選：</span><span class="sxs-lookup"><span data-stu-id="3b5d9-122">You can use the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method to search for a VP pin on the capture filter:</span></span>


```C++
hr = pBuild->FindPin(
    pCap,                    // Pointer to the capture filter.
    PINDIR_OUTPUT,           // Look for an output pin.
    &PIN_CATEGORY_VIDEOPORT, // Look for a video port pin.
    NULL,                    // Any media type.
    FALSE,                   // Pin can be connected.
    0,                       // Retrieve the first matching pin.
    &pVPPin                  // Receives a pointer to the pin.
);
```



<span data-ttu-id="3b5d9-123">將重迭混音器新增至圖形之後，再次呼叫 **FindPin** ，以在重迭混音器上尋找針腳0。</span><span class="sxs-lookup"><span data-stu-id="3b5d9-123">After you add the Overlay Mixer to the graph, call **FindPin** again to find pin 0 on the Overlay Mixer.</span></span> <span data-ttu-id="3b5d9-124">Pin 0 一律是篩選上的第一個輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="3b5d9-124">Pin 0 is always the first input pin on the filter.</span></span>


```C++
pBuild->FindPin(pOvMix, PINDIR_INPUT, NULL, NULL, TRUE, 0, &pOVPin);
```



<span data-ttu-id="3b5d9-125">藉由呼叫 [**IGraphBuilder：： connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect)來連接兩個 pin。</span><span class="sxs-lookup"><span data-stu-id="3b5d9-125">Connect the two pins by calling [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect).</span></span>


```C++
pGraph->Connect(pVPPin, pOvPin);
```



<span data-ttu-id="3b5d9-126">然後將重迭混音器的輸出釘選到影片轉譯器篩選器。</span><span class="sxs-lookup"><span data-stu-id="3b5d9-126">Then connect the Overlay Mixer's output pin to the Video Renderer filter.</span></span> <span data-ttu-id="3b5d9-127">您可以藉由在篩選圖形管理員上呼叫 [**IVideoWindow：:p 的 [內容 \_**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) ]、[自動顯示] 和 [ [**IVideoWindow:p： \_**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) ]，來隱藏影片。</span><span class="sxs-lookup"><span data-stu-id="3b5d9-127">You can hide the video by calling the [**IVideoWindow::put\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) and [**IVideoWindow::put\_Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) methods on the Filter Graph Manager.</span></span>

<span data-ttu-id="3b5d9-128">針對 TV 調諧器，capture 篩選器可能也會有影片埠 VBI 釘選 [ \_ \_ VIDEOPORT) VBI] (釘選類別 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3b5d9-128">For TV tuners, the capture filter might also have a video port VBI pin (PIN\_CATEGORY\_VIDEOPORT\_VBI).</span></span> <span data-ttu-id="3b5d9-129">若是如此，請將該釘選到 [VBI Surface](vbi-surface-allocator.md) 配置器篩選器。</span><span class="sxs-lookup"><span data-stu-id="3b5d9-129">If so, connect that pin to the [VBI Surface Allocator](vbi-surface-allocator.md) filter.</span></span> <span data-ttu-id="3b5d9-130">如需詳細資訊，請參閱 [觀看隱藏](viewing-closed-captions.md)式輔助字幕。</span><span class="sxs-lookup"><span data-stu-id="3b5d9-130">For more information, see [Viewing Closed Captions](viewing-closed-captions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b5d9-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="3b5d9-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b5d9-132">Advanced Capture 主題</span><span class="sxs-lookup"><span data-stu-id="3b5d9-132">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="3b5d9-133">使用影片捕獲中的重迭混音器</span><span class="sxs-lookup"><span data-stu-id="3b5d9-133">Using the Overlay Mixer in Video Capture</span></span>](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



