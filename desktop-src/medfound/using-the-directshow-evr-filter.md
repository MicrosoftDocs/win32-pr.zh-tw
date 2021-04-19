---
description: 使用 DirectShow EVR 篩選器
ms.assetid: 4d85aed0-4b11-4c5f-bfc0-cad0a7d2f490
title: 使用 DirectShow EVR 篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02568a5ea9cbaa0310409a5a0966a2bea1bbfffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993068"
---
# <a name="using-the-directshow-evr-filter"></a><span data-ttu-id="92098-103">使用 DirectShow EVR 篩選器</span><span class="sxs-lookup"><span data-stu-id="92098-103">Using the DirectShow EVR Filter</span></span>

<span data-ttu-id="92098-104">若要建立增強型影片轉譯器 (EVR) 篩選器，請呼叫 **CoCreateInstance**。</span><span class="sxs-lookup"><span data-stu-id="92098-104">To create the enhanced video renderer (EVR) filter, call **CoCreateInstance**.</span></span> <span data-ttu-id="92098-105">CLSID 是 CLSID \_ EnhancedVideoRenderer，定義于 uuid. h 中。</span><span class="sxs-lookup"><span data-stu-id="92098-105">The CLSID is CLSID\_EnhancedVideoRenderer, defined in uuids.h.</span></span> <span data-ttu-id="92098-106">您不必呼叫 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) 或 [**MFSHUTDOWN**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) 來使用 EVR 篩選器。</span><span class="sxs-lookup"><span data-stu-id="92098-106">You do not have to call [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) or [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) to use the EVR filter.</span></span>

<span data-ttu-id="92098-107">如需在 DirectShow 應用程式中使用 EVR 篩選的詳細資訊，請參閱 [directshow 中的音訊/影片播放](../directshow/audio-video-playback-in-directshow.md)。</span><span class="sxs-lookup"><span data-stu-id="92098-107">For more information about using the EVR filter in a DirectShow application, see [Audio/Video Playback in DirectShow](../directshow/audio-video-playback-in-directshow.md).</span></span>

<span data-ttu-id="92098-108">EVR 篩選準則會以一個輸入的 pin （對應至參考資料流）開始。</span><span class="sxs-lookup"><span data-stu-id="92098-108">The EVR filter starts with one input pin, which corresponds to the reference stream.</span></span> <span data-ttu-id="92098-109">若要加入子串流的 pin，請查詢 [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig) 介面的篩選準則，然後呼叫 [**IEVRFilterConfig：： SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams)。</span><span class="sxs-lookup"><span data-stu-id="92098-109">To add pins for substreams, query the filter for the [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig) interface and call [**IEVRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams).</span></span> <span data-ttu-id="92098-110">連接任何輸入圖釘之前，請先呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="92098-110">Call this method before connecting any input pins.</span></span> <span data-ttu-id="92098-111">Pin 0 一律是參考資料流。</span><span class="sxs-lookup"><span data-stu-id="92098-111">Pin 0 is always the reference stream.</span></span> <span data-ttu-id="92098-112">請在任何其他 pin 之前連接此 pin，因為參考資料流的格式可能會限制可用的子資料流程格式。</span><span class="sxs-lookup"><span data-stu-id="92098-112">Connect this pin before any other pins, because the format of the reference stream might limit which substream formats are available.</span></span>

<span data-ttu-id="92098-113">開始圖形之前，請先設定影片裁剪視窗和目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="92098-113">Before starting the graph, set the video clipping window and the destination rectangle.</span></span> <span data-ttu-id="92098-114">如需詳細資訊，請參閱 [使用影片顯示控制項](using-the-video-display-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="92098-114">For more information, see [Using the Video Display Controls](using-the-video-display-controls.md).</span></span>

<span data-ttu-id="92098-115">不同于 (VMR) 的影片混合轉譯器，EVR 不會有運作模式 (視窗化、無視窗等等) 。</span><span class="sxs-lookup"><span data-stu-id="92098-115">Unlike the Video Mixing Renderer (VMR), the EVR does not have operational modes (windowed, windowless, and so forth).</span></span> <span data-ttu-id="92098-116">尤其是：</span><span class="sxs-lookup"><span data-stu-id="92098-116">In particular:</span></span>

-   <span data-ttu-id="92098-117">EVR 不支援視窗模式。</span><span class="sxs-lookup"><span data-stu-id="92098-117">The EVR does not support windowed mode.</span></span> <span data-ttu-id="92098-118">應用程式必須提供裁剪視窗。</span><span class="sxs-lookup"><span data-stu-id="92098-118">The application must provide the clipping window.</span></span>
-   <span data-ttu-id="92098-119">EVR 沒有 renderless 模式。</span><span class="sxs-lookup"><span data-stu-id="92098-119">The EVR does not have a renderless mode.</span></span> <span data-ttu-id="92098-120">若要取代預設的展示者，請呼叫 [**IMFVideoRenderer：： InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer)。</span><span class="sxs-lookup"><span data-stu-id="92098-120">To replace the default presenter, call [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span></span>
-   <span data-ttu-id="92098-121">EVR 沒有混合模式。</span><span class="sxs-lookup"><span data-stu-id="92098-121">The EVR does not have a mixing mode.</span></span> <span data-ttu-id="92098-122">EVR 一律會建立混音器。</span><span class="sxs-lookup"><span data-stu-id="92098-122">The EVR always creates the mixer.</span></span> <span data-ttu-id="92098-123">如果您有一個輸入資料流程，就不需要呼叫 [**SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams) 來強制 EVR 使用混音器。</span><span class="sxs-lookup"><span data-stu-id="92098-123">If you have one input stream, it is not necessary to call [**SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams) to force the EVR to use the mixer.</span></span>

## <a name="filter-interfaces"></a><span data-ttu-id="92098-124">篩選介面</span><span class="sxs-lookup"><span data-stu-id="92098-124">Filter Interfaces</span></span>

<span data-ttu-id="92098-125">EVR 篩選器會公開下列介面。</span><span class="sxs-lookup"><span data-stu-id="92098-125">The EVR filter exposes the following interfaces.</span></span> <span data-ttu-id="92098-126">其中一些介面記載于 DirectShow SDK 中。</span><span class="sxs-lookup"><span data-stu-id="92098-126">Some of these interfaces are documented in the DirectShow SDK.</span></span> <span data-ttu-id="92098-127">使用 **QueryInterface** 來取得這些介面的指標：</span><span class="sxs-lookup"><span data-stu-id="92098-127">Use **QueryInterface** to retrieve pointers to these interfaces:</span></span>

-   <span data-ttu-id="92098-128">[**IAMCertifiedOutputProtection**](/windows/win32/api/strmif/nn-strmif-iamcertifiedoutputprotection) (DirectShow) </span><span class="sxs-lookup"><span data-stu-id="92098-128">[**IAMCertifiedOutputProtection**](/windows/win32/api/strmif/nn-strmif-iamcertifiedoutputprotection) (DirectShow)</span></span>
-   <span data-ttu-id="92098-129">[**IAMFilterMiscFlags**](/windows/win32/api/strmif/nn-strmif-iamfiltermiscflags) (DirectShow) </span><span class="sxs-lookup"><span data-stu-id="92098-129">[**IAMFilterMiscFlags**](/windows/win32/api/strmif/nn-strmif-iamfiltermiscflags) (DirectShow)</span></span>
-   <span data-ttu-id="92098-130">[**IBaseFilter**](/windows/win32/api/strmif/nn-strmif-ibasefilter) (DirectShow) </span><span class="sxs-lookup"><span data-stu-id="92098-130">[**IBaseFilter**](/windows/win32/api/strmif/nn-strmif-ibasefilter) (DirectShow)</span></span>
-   [<span data-ttu-id="92098-131">**IEVRFilterConfig**</span><span class="sxs-lookup"><span data-stu-id="92098-131">**IEVRFilterConfig**</span></span>](/windows/desktop/api/evr/nn-evr-ievrfilterconfig)
-   <span data-ttu-id="92098-132">[**IKsPropertySet**](../directshow/ikspropertyset.md) (DirectShow) </span><span class="sxs-lookup"><span data-stu-id="92098-132">[**IKsPropertySet**](../directshow/ikspropertyset.md) (DirectShow)</span></span>
-   <span data-ttu-id="92098-133">[**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) (DirectShow) </span><span class="sxs-lookup"><span data-stu-id="92098-133">[**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) (DirectShow)</span></span>
-   [<span data-ttu-id="92098-134">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="92098-134">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="92098-135">**IMFVideoPositionMapper**</span><span class="sxs-lookup"><span data-stu-id="92098-135">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)
-   [<span data-ttu-id="92098-136">**IMFVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="92098-136">**IMFVideoRenderer**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideorenderer)
-   <span data-ttu-id="92098-137">**IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="92098-137">**IPersistStream**</span></span>
-   <span data-ttu-id="92098-138">[**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow) </span><span class="sxs-lookup"><span data-stu-id="92098-138">[**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)</span></span>
-   <span data-ttu-id="92098-139">[**IQualProp**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop) (DirectShow) </span><span class="sxs-lookup"><span data-stu-id="92098-139">[**IQualProp**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop) (DirectShow)</span></span>
-   <span data-ttu-id="92098-140">**ISpecifyPropertyPages**</span><span class="sxs-lookup"><span data-stu-id="92098-140">**ISpecifyPropertyPages**</span></span>

## <a name="input-pin-interfaces"></a><span data-ttu-id="92098-141">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="92098-141">Input Pin Interfaces</span></span>

<span data-ttu-id="92098-142">EVR 篩選器上的輸入圖釘會公開下列介面。</span><span class="sxs-lookup"><span data-stu-id="92098-142">The input pins on the EVR filter expose the following interfaces.</span></span> <span data-ttu-id="92098-143">使用 **QueryInterface** 來取得這些介面的指標：</span><span class="sxs-lookup"><span data-stu-id="92098-143">Use **QueryInterface** to retrieve pointers to these interfaces:</span></span>

-   [<span data-ttu-id="92098-144">**IEVRVideoStreamControl**</span><span class="sxs-lookup"><span data-stu-id="92098-144">**IEVRVideoStreamControl**</span></span>](/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol)
-   <span data-ttu-id="92098-145">[**IMemInputPin**](/windows/win32/api/strmif/nn-strmif-imeminputpin) (DirectShow) </span><span class="sxs-lookup"><span data-stu-id="92098-145">[**IMemInputPin**](/windows/win32/api/strmif/nn-strmif-imeminputpin) (DirectShow)</span></span>
-   [<span data-ttu-id="92098-146">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="92098-146">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   <span data-ttu-id="92098-147">[**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) (DirectShow) </span><span class="sxs-lookup"><span data-stu-id="92098-147">[**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) (DirectShow)</span></span>
-   <span data-ttu-id="92098-148">[**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow) </span><span class="sxs-lookup"><span data-stu-id="92098-148">[**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)</span></span>

<span data-ttu-id="92098-149">此外，您可以使用 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) 介面來取出下列介面：</span><span class="sxs-lookup"><span data-stu-id="92098-149">In addition, you can use the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface to retrieve the following interface:</span></span>

-   [<span data-ttu-id="92098-150">**IDirectXVideoMemoryConfiguration**</span><span class="sxs-lookup"><span data-stu-id="92098-150">**IDirectXVideoMemoryConfiguration**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)

## <a name="related-topics"></a><span data-ttu-id="92098-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="92098-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92098-152">在 DirectShow 播放音訊/影片</span><span class="sxs-lookup"><span data-stu-id="92098-152">Audio/Video Playback in DirectShow</span></span>](../directshow/audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="92098-153">增強的影片轉譯器</span><span class="sxs-lookup"><span data-stu-id="92098-153">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> </dl>

 

 
