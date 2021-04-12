---
description: 建立 DVD 篩選圖形
ms.assetid: 1d2f8284-2deb-4207-b067-24a54d6b286c
title: 建立 DVD 篩選圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96d15c7d84ec138771e1f5da8be4270faae049cc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109709"
---
# <a name="building-the-dvd-filter-graph"></a><span data-ttu-id="1ad91-103">建立 DVD 篩選圖形</span><span class="sxs-lookup"><span data-stu-id="1ad91-103">Building the DVD Filter Graph</span></span>

<span data-ttu-id="1ad91-104">就像任何 DirectShow 應用程式一樣，DVD 播放應用程式一開始會先建立一個篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="1ad91-104">As with any DirectShow application, a DVD playback application starts by building a filter graph.</span></span> <span data-ttu-id="1ad91-105">DirectShow 提供下列元件來播放 DVD：</span><span class="sxs-lookup"><span data-stu-id="1ad91-105">DirectShow provides the following components for DVD playback:</span></span>

-   <span data-ttu-id="1ad91-106">[DVD Graph Builder](dvd-graph-builder.md)。</span><span class="sxs-lookup"><span data-stu-id="1ad91-106">[DVD Graph Builder](dvd-graph-builder.md).</span></span> <span data-ttu-id="1ad91-107">建立篩選圖形的 helper 物件。</span><span class="sxs-lookup"><span data-stu-id="1ad91-107">A helper object that constructs the filter graph.</span></span> <span data-ttu-id="1ad91-108">它會公開 [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) 介面。</span><span class="sxs-lookup"><span data-stu-id="1ad91-108">It exposes the [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) interface.</span></span>
-   <span data-ttu-id="1ad91-109">[DVD 流覽](dvd-navigator-filter.md) 器篩選。</span><span class="sxs-lookup"><span data-stu-id="1ad91-109">[DVD Navigator](dvd-navigator-filter.md) filter.</span></span> <span data-ttu-id="1ad91-110">可處理 DVD 播放、流覽和其他命令的 DirectShow 篩選。</span><span class="sxs-lookup"><span data-stu-id="1ad91-110">A DirectShow filter that handles DVD playback, navigation, and other commands.</span></span>

<span data-ttu-id="1ad91-111">DVD 播放也需要 MPEG-2 解碼器。</span><span class="sxs-lookup"><span data-stu-id="1ad91-111">DVD playback also requires an MPEG-2 decoder.</span></span> <span data-ttu-id="1ad91-112">硬體和軟體 MPEG-2 解碼器可從協力廠商取得。</span><span class="sxs-lookup"><span data-stu-id="1ad91-112">Hardware and software MPEG-2 decoders are available from third parties.</span></span> <span data-ttu-id="1ad91-113">首先，建立 DVD Graph Builder 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="1ad91-113">First, create an instance of the DVD Graph Builder object.</span></span>


```C++
IDvdGraphBuilder *pBuild = NULL;
hr = CoCreateInstance(CLSID_DvdGraphBuilder, NULL, 
    CLSCTX_INPROC_SERVER, IID_IDvdGraphBuilder, (void **)&pBuild);
```



<span data-ttu-id="1ad91-114">至此，您可以在建立圖形的其餘部分之前，先選取並設定影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="1ad91-114">At this point, you can select and configure the video renderer before you build the rest of the graph.</span></span> <span data-ttu-id="1ad91-115">此步驟是選擇性的，在下一節中會更詳細地說明。</span><span class="sxs-lookup"><span data-stu-id="1ad91-115">This step, which is optional, is described in more detail in the next section.</span></span> <span data-ttu-id="1ad91-116">如果您省略這個步驟，DVD 圖形產生器會選取預設轉譯器。</span><span class="sxs-lookup"><span data-stu-id="1ad91-116">If you omit this step, the DVD Graph Builder selects a default renderer.</span></span> <span data-ttu-id="1ad91-117">接下來，藉由呼叫 [**IDvdGraphBuilder：： RenderDvdVideoVolume**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume) 方法來建立圖形。</span><span class="sxs-lookup"><span data-stu-id="1ad91-117">Next, build the graph by calling the [**IDvdGraphBuilder::RenderDvdVideoVolume**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume) method.</span></span>


```C++
AM_DVD_RENDERSTATUS buildStatus;
hr = pBuild->RenderDvdVideoVolume(L"Z:\\video_ts", 0, &buildStatus);
```



<span data-ttu-id="1ad91-118">第一個參數是包含 DVD 檔案的目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="1ad91-118">The first parameter is the name of a directory that contains the DVD files.</span></span> <span data-ttu-id="1ad91-119">在 DVD 光碟上，這些檔案位於名為 VIDEO TS 的目錄中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="1ad91-119">On a DVD disc, these files reside in a directory named VIDEO\_TS.</span></span> <span data-ttu-id="1ad91-120">如果第一個參數為 **Null**，則 dvd 圖形產生器會使用第一個包含 DVD 磁片區的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="1ad91-120">If the first parameter is **NULL**, the DVD Graph Builder uses the first drive that contains a DVD volume.</span></span>

<span data-ttu-id="1ad91-121">第二個參數包含各種選擇性旗標，可用於選擇 (硬體或軟體) 和其他選項的解碼器類型。</span><span class="sxs-lookup"><span data-stu-id="1ad91-121">The second parameter contains various optional flags for choosing the type of decoder (hardware or software) and other options.</span></span>

<span data-ttu-id="1ad91-122">第三個參數是可接收狀態資訊的 [**AM \_ DVD \_ RENDERSTATUS**](/windows/win32/api/strmif/ns-strmif-am_dvd_renderstatus) 結構。</span><span class="sxs-lookup"><span data-stu-id="1ad91-122">The third parameter is an [**AM\_DVD\_RENDERSTATUS**](/windows/win32/api/strmif/ns-strmif-am_dvd_renderstatus) structure that receives status information.</span></span> <span data-ttu-id="1ad91-123">如果 [**RenderDvdVideoVolume**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume) 方法傳回 \_ FALSE，則表示呼叫部分成功 (或部分失敗，如果您是 pessimist) 。</span><span class="sxs-lookup"><span data-stu-id="1ad91-123">If the [**RenderDvdVideoVolume**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume) method returns S\_FALSE, it means the call partially succeeded (or partially failed, if you're a pessimist).</span></span> <span data-ttu-id="1ad91-124">例如，即使已成功轉譯其他資料流程，方法還是可能無法轉譯子圖片資料流程。</span><span class="sxs-lookup"><span data-stu-id="1ad91-124">For example, the method might fail to render the subpicture stream, even though the other streams rendered successfully.</span></span> <span data-ttu-id="1ad91-125">如果 **RenderDvdVideoVolume** 方法傳回錯誤碼或值 \_ FALSE，您可以檢查 **AM \_ DVD \_ RENDERSTATUS** 結構，以取得錯誤的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1ad91-125">If the **RenderDvdVideoVolume** method returns an error code or the value S\_FALSE, you can examine the **AM\_DVD\_RENDERSTATUS** structure for details about the error.</span></span>

<span data-ttu-id="1ad91-126">接下來，藉由呼叫 [**IDvdGraphBuilder：： GetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getfiltergraph)來取得篩選圖形管理員的指標。</span><span class="sxs-lookup"><span data-stu-id="1ad91-126">Next, get a pointer to the Filter Graph Manager by calling [**IDvdGraphBuilder::GetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getfiltergraph).</span></span> <span data-ttu-id="1ad91-127">這個方法會傳回篩選圖形管理員 [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="1ad91-127">This method returns a pointer to the Filter Graph Manager's [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface.</span></span>


```C++
IGraphBuilder *pGraph = NULL;
hr =  pBuild->GetFiltergraph(&m_pGraph);
```



<span data-ttu-id="1ad91-128">使用 [**IDvdGraphBuilder：： GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) 方法來取出 DVD 相關的介面，包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="1ad91-128">Use the [**IDvdGraphBuilder::GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) method to retrieve DVD-related interfaces, including the following:</span></span>

-   <span data-ttu-id="1ad91-129">[**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)。</span><span class="sxs-lookup"><span data-stu-id="1ad91-129">[**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2).</span></span> <span data-ttu-id="1ad91-130">控制播放和 DVD 命令</span><span class="sxs-lookup"><span data-stu-id="1ad91-130">Controls playback and DVD commands</span></span>
-   <span data-ttu-id="1ad91-131">[**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)。</span><span class="sxs-lookup"><span data-stu-id="1ad91-131">[**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2).</span></span> <span data-ttu-id="1ad91-132">傳回 DVD 導覽器目前狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1ad91-132">Returns information about the DVD Navigator's current state.</span></span>
-   <span data-ttu-id="1ad91-133">[**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder)。</span><span class="sxs-lookup"><span data-stu-id="1ad91-133">[**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder).</span></span> <span data-ttu-id="1ad91-134">控制隱藏式輔助字幕顯示。</span><span class="sxs-lookup"><span data-stu-id="1ad91-134">Controls closed caption display.</span></span> <span data-ttu-id="1ad91-135">預設會啟用隱藏式輔助字幕顯示。</span><span class="sxs-lookup"><span data-stu-id="1ad91-135">Closed caption display is enabled by default.</span></span> <span data-ttu-id="1ad91-136">若要停用它[](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) ，請使用 AM \_ L21 \_ CCSTATE \_ Off 旗標來呼叫 IAMLine21Decoder：： SetServiceState。</span><span class="sxs-lookup"><span data-stu-id="1ad91-136">To disable it, call [**IAMLine21Decoder::SetServiceState**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) with the AM\_L21\_CCSTATE\_Off flag.</span></span>
-   <span data-ttu-id="1ad91-137">[**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)。</span><span class="sxs-lookup"><span data-stu-id="1ad91-137">[**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio).</span></span> <span data-ttu-id="1ad91-138">控制音訊音量和餘額。</span><span class="sxs-lookup"><span data-stu-id="1ad91-138">Controls audio volume and balance.</span></span>

<span data-ttu-id="1ad91-139">例如，下列程式碼會傳回 [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) 介面。</span><span class="sxs-lookup"><span data-stu-id="1ad91-139">For example, the following code returns the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface.</span></span>


```C++
IDvdControl2 *pDvdControl = NULL;
hr = pBuild->GetDvdInterface(IID_IDvdControl2, (void**)&pDvdControl);
```



<span data-ttu-id="1ad91-140">建立 DVD 播放篩選圖形的建議方式是讓 [Dvd 圖形](dvd-graph-builder.md) 產生器物件自動為您進行。</span><span class="sxs-lookup"><span data-stu-id="1ad91-140">The recommended way to build the DVD playback filter graph is to have a [DVD Graph Builder](dvd-graph-builder.md) object do it for you automatically.</span></span> <span data-ttu-id="1ad91-141">這種方法在下面和 DVD 範例應用程式中示範。</span><span class="sxs-lookup"><span data-stu-id="1ad91-141">This approach is demonstrated below and in the DVD sample application.</span></span> <span data-ttu-id="1ad91-142">如果您需要手動建立 DVD 篩選圖形，您可以遵循 DirectShow 檔中其他位置所討論之圖形建築物的基本規則來進行。</span><span class="sxs-lookup"><span data-stu-id="1ad91-142">If you need to build your DVD filter graph manually, you can do so by following the basic rules of graph building discussed elsewhere in the DirectShow documentation.</span></span> <span data-ttu-id="1ad91-143">一般而言，您不應該手動新增、移除、連接或中斷 DVD 圖形產生器所建立之圖形中的個別篩選器，因為這樣做可能會使清除程式碼混淆。</span><span class="sxs-lookup"><span data-stu-id="1ad91-143">Generally, you should not manually add, remove, connect, or disconnect individual filters in the graph created by the DVD Graph Builder, because doing so might confuse the cleanup code.</span></span>

<span data-ttu-id="1ad91-144">設定影片轉譯器</span><span class="sxs-lookup"><span data-stu-id="1ad91-144">Configuring the Video Renderer</span></span>

<span data-ttu-id="1ad91-145">DirectShow 提供數個影片轉譯器篩選器。</span><span class="sxs-lookup"><span data-stu-id="1ad91-145">DirectShow provides several video renderer filters.</span></span> <span data-ttu-id="1ad91-146">建立圖形之前，您可以選擇您偏好的影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="1ad91-146">Before you build the graph, you can chose which video renderer you prefer.</span></span> <span data-ttu-id="1ad91-147">藉由呼叫 [**IDvdGraphBuilder：： GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) 並要求該轉譯器的特定介面，來選取轉譯器：</span><span class="sxs-lookup"><span data-stu-id="1ad91-147">Select the renderer by calling [**IDvdGraphBuilder::GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) and requesting an interface that is specific to that renderer:</span></span>

-   <span data-ttu-id="1ad91-148">覆迭混音器篩選： [**IDDrawExclModeVideo**](/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo)。</span><span class="sxs-lookup"><span data-stu-id="1ad91-148">Overlay Mixer Filter: [**IDDrawExclModeVideo**](/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo).</span></span>
-   <span data-ttu-id="1ad91-149">影片混合轉譯器 7 (VMR-7) ： [**IVMRFilterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig)。</span><span class="sxs-lookup"><span data-stu-id="1ad91-149">Video Mixing Renderer 7 (VMR-7): [**IVMRFilterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig).</span></span>
-   <span data-ttu-id="1ad91-150">影片混合轉譯器 9 (VMR-9) ： [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9)。</span><span class="sxs-lookup"><span data-stu-id="1ad91-150">Video Mixing Renderer 9 (VMR-9): [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9).</span></span>
-   <span data-ttu-id="1ad91-151">增強的影片轉譯器 (EVR) ： [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig)。</span><span class="sxs-lookup"><span data-stu-id="1ad91-151">Enhanced Video Renderer (EVR): [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig).</span></span>

<span data-ttu-id="1ad91-152">如果您在建立篩選圖形之前要求這些介面的任何一個，DVD 圖形產生器會建立對應的影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="1ad91-152">If you request any of these interfaces before building the filter graph, the DVD Graph Builder creates the corresponding video renderer.</span></span> <span data-ttu-id="1ad91-153">之後，當您建立圖形時，DVD 圖形產生器將會嘗試使用該轉譯器。</span><span class="sxs-lookup"><span data-stu-id="1ad91-153">Later, when you build the graph, the DVD Graph Builder will try to use that renderer.</span></span> <span data-ttu-id="1ad91-154">但是，如果無法使用您選取的轉譯器來建立圖形，它可能會切換至另一個轉譯器。</span><span class="sxs-lookup"><span data-stu-id="1ad91-154">But if it cannot build the graph using the renderer you selected, it may switch to another renderer.</span></span> <span data-ttu-id="1ad91-155">例如，您的 MPEG-2 解碼器可能與 VMR 篩選器不相容，在這種情況下，DVD 圖形產生器會預設為重迭混音器。</span><span class="sxs-lookup"><span data-stu-id="1ad91-155">For example, your MPEG-2 decoder might not be compatible with the VMR filter, in which case the DVD Graph Builder would default to the Overlay Mixer.</span></span>

<span data-ttu-id="1ad91-156">這些介面也會讓您有機會在連接至解碼器之前，先設定轉譯器。</span><span class="sxs-lookup"><span data-stu-id="1ad91-156">These interfaces also give you a chance to configure the renderer before it is connected to the decoder.</span></span> <span data-ttu-id="1ad91-157">例如，您可以將 VMR 設定為使用無視窗模式，而不是預設的視窗模式。</span><span class="sxs-lookup"><span data-stu-id="1ad91-157">For example, you can set the VMR to use windowless mode instead of the default windowed mode.</span></span> <span data-ttu-id="1ad91-158">如需影片轉譯器的詳細資訊，請參閱 [在 DirectShow 中轉譯影片](about-video-rendering-in-directshow.md)的相關主題。</span><span class="sxs-lookup"><span data-stu-id="1ad91-158">For more information about video renderers, see the topic [About Video Rendering in DirectShow](about-video-rendering-in-directshow.md).</span></span>

<span data-ttu-id="1ad91-159">在 Windows XP 和更新版本上，DVD 圖形產生器一律會使用 [影片混合](video-mixing-renderer-filter-7.md) 轉譯器 7 (VMR-7) ，除非：</span><span class="sxs-lookup"><span data-stu-id="1ad91-159">On Windows XP and later, the DVD Graph Builder always uses the [Video Mixing Renderer 7](video-mixing-renderer-filter-7.md) (VMR-7), unless:</span></span>

-   <span data-ttu-id="1ad91-160">呼叫端查詢介面只找到覆迭 [混音](overlay-mixer-filter.md)器，例如 [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2)。</span><span class="sxs-lookup"><span data-stu-id="1ad91-160">The caller queries interfaces found only the [Overlay Mixer](overlay-mixer-filter.md), such as [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2).</span></span> <span data-ttu-id="1ad91-161">這會將提示傳送給 DVD 圖形產生器，讓應用程式想要使用重迭混音器，而不是 VMR。</span><span class="sxs-lookup"><span data-stu-id="1ad91-161">This sends a hint to the DVD Graph Builder that the application wants to use the Overlay Mixer and not the VMR.</span></span> <span data-ttu-id="1ad91-162">Windows Media Player 也有一個對話方塊選項，可強制使用重迭混音器。</span><span class="sxs-lookup"><span data-stu-id="1ad91-162">Windows Media Player also has a dialog box option to force the use of the Overlay Mixer.</span></span>
-   <span data-ttu-id="1ad91-163">安裝的解碼器與 VMR 不相容。</span><span class="sxs-lookup"><span data-stu-id="1ad91-163">The installed decoder is not VMR-compatible.</span></span> <span data-ttu-id="1ad91-164">在圖形建立期間，會使用新的 [**IAMDecoderCaps**](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps) 介面來檢查解碼器的 VMR 支援。</span><span class="sxs-lookup"><span data-stu-id="1ad91-164">During graph building, the new [**IAMDecoderCaps**](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps) interface is used to check for the decoder's VMR support.</span></span> <span data-ttu-id="1ad91-165">如果不存在，DVD 圖形產生器將會使用重迭混音器。</span><span class="sxs-lookup"><span data-stu-id="1ad91-165">If that is not present, the DVD Graph Builder will use the Overlay Mixer.</span></span>
-   <span data-ttu-id="1ad91-166">使用硬體解碼器時，解碼器無法連線到 [影片埠管理員](video-port-manager.md) (VPM) 。</span><span class="sxs-lookup"><span data-stu-id="1ad91-166">While using a hardware decoder, the decoder cannot connect to the [Video Port Manager](video-port-manager.md) (VPM).</span></span> <span data-ttu-id="1ad91-167">如果硬體解碼器無法使用 VPM，則無法使用 VMR，因此 DVD 圖形產生器會嘗試使用重迭混音器來建立圖形。</span><span class="sxs-lookup"><span data-stu-id="1ad91-167">If a hardware decoder cannot use the VPM, then it cannot use the VMR, and so the DVD Graph Builder then tries to build a graph using the Overlay Mixer.</span></span>
-   <span data-ttu-id="1ad91-168">已知顯示配接器的資源和/或功能不足，無法支援 VMR，但無法在驅動程式中正確地報告。</span><span class="sxs-lookup"><span data-stu-id="1ad91-168">The display card is known to have insufficient resources and/or capabilities to support the VMR but does not correctly report this in the driver.</span></span> <span data-ttu-id="1ad91-169"> (某些已知案例會被 DVD 圖形產生器明確排除。 ) </span><span class="sxs-lookup"><span data-stu-id="1ad91-169">(Some known cases are specifically excluded by the DVD Graph Builder.)</span></span>
-   <span data-ttu-id="1ad91-170">基於任何原因，解碼器與 VMR 之間的連接失敗，通常是因為缺乏 VRAM 來建立必要的表面。</span><span class="sxs-lookup"><span data-stu-id="1ad91-170">The connection between the decoder and the VMR fails for any reason, usually due to a lack of VRAM to create the necessary surfaces.</span></span> <span data-ttu-id="1ad91-171">在這些情況下，DVD 圖形產生器會關閉 VMR 使用，並嘗試使用重迭混音器來建立圖形。</span><span class="sxs-lookup"><span data-stu-id="1ad91-171">In these cases, the DVD Graph Builder switches off VMR use and tries to use the Overlay Mixer to build a graph.</span></span>

<span data-ttu-id="1ad91-172">視窗模式</span><span class="sxs-lookup"><span data-stu-id="1ad91-172">Windowed Mode</span></span>

<span data-ttu-id="1ad91-173">在視窗模式中 (重迭混音器或 VMR) ，轉譯器會建立自己的影片視窗。</span><span class="sxs-lookup"><span data-stu-id="1ad91-173">In windowed mode (Overlay Mixer or VMR), the renderer creates its own video window.</span></span> <span data-ttu-id="1ad91-174">若要將此視窗設為應用程式視窗的子系，請使用應用程式的控制碼來呼叫 [**IVideoWindow：:p 的 ui \_ 擁有**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) 者。</span><span class="sxs-lookup"><span data-stu-id="1ad91-174">To make this window a child of the application window, call [**IVideoWindow::put\_Owner**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) with a handle to the application.</span></span> <span data-ttu-id="1ad91-175">此外，也請呼叫 [**IVideoWindow：:p 的 \_ system.windows.window.windowstyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) ， \_ 在轉譯器的影片視窗上設定 WS 子系和 ws \_ CLIPSIBLINGS 樣式。</span><span class="sxs-lookup"><span data-stu-id="1ad91-175">Also call [**IVideoWindow::put\_WindowStyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) to set the WS\_CHILD and WS\_CLIPSIBLINGS styles on the renderer's video window.</span></span> <span data-ttu-id="1ad91-176">若要從轉譯器的影片視窗取得滑鼠訊息，請使用應用程式視窗的控制碼來呼叫 [**IVideoWindow：:p 的 \_ MessageDrain**](/windows/desktop/api/Control/nf-control-ivideowindow-put_messagedrain) 。</span><span class="sxs-lookup"><span data-stu-id="1ad91-176">To get mouse messages from the renderer's video window, call [**IVideoWindow::put\_MessageDrain**](/windows/desktop/api/Control/nf-control-ivideowindow-put_messagedrain) with a handle to the application window.</span></span> <span data-ttu-id="1ad91-177">這個方法會設定「訊息清空」—影片視窗會將接收到的任何滑鼠訊息轉寄至「訊息清空」視窗。</span><span class="sxs-lookup"><span data-stu-id="1ad91-177">This method sets up a "message drain" — the video window forwards any mouse messages it receives to the message drain window.</span></span>


```C++
pVideoWindow->put_Owner((OAHWND)hwnd);
pVideoWindow->put_WindowStyle(WS_CHILD | WS_CLIPSIBLINGS);
pVideoWindow->put_MessageDrain((OAHWND)hwnd) ;
```



<span data-ttu-id="1ad91-178">郵件清空讓選取 DVD 功能表按鈕稍微複雜一點。</span><span class="sxs-lookup"><span data-stu-id="1ad91-178">The message drain makes selecting DVD menu buttons somewhat complicated.</span></span> <span data-ttu-id="1ad91-179">假設影片視窗未填滿應用程式的整個工作區，則有些滑鼠事件會落在影片視窗之外。</span><span class="sxs-lookup"><span data-stu-id="1ad91-179">Assuming the video window does not fill the application's entire client area, some mouse events will fall outside the video window.</span></span> <span data-ttu-id="1ad91-180">當您從影片視窗 *內* 取得滑鼠事件時，您應該處理它以進行 DVD 功能表導覽。</span><span class="sxs-lookup"><span data-stu-id="1ad91-180">When you get a mouse event from *inside* the video window, you should process it for DVD menu navigation.</span></span> <span data-ttu-id="1ad91-181">不應處理影片視窗 *外* 的滑鼠事件。</span><span class="sxs-lookup"><span data-stu-id="1ad91-181">Mouse events from *outside* the video window should not be processed.</span></span> <span data-ttu-id="1ad91-182">在訊息清空的情況下，沒有辦法區分兩者。</span><span class="sxs-lookup"><span data-stu-id="1ad91-182">With the message drain, there is no way to distinguish between the two.</span></span> <span data-ttu-id="1ad91-183">此外，影片視窗中滑鼠事件的座標是相對於影片視窗的工作區。但從影片視窗外部的滑鼠事件是相對於應用程式的工作區。</span><span class="sxs-lookup"><span data-stu-id="1ad91-183">Furthermore, the coordinates for mouse events from the video window are relative to the video window's client area; but mouse events from outside the video window are relative to the application's client area.</span></span>

<span data-ttu-id="1ad91-184">無視窗模式</span><span class="sxs-lookup"><span data-stu-id="1ad91-184">Windowless Mode</span></span>

<span data-ttu-id="1ad91-185">無視窗模式可避免整個滑鼠訊息的問題。</span><span class="sxs-lookup"><span data-stu-id="1ad91-185">Windowless mode avoids the problems with mouse messages altogether.</span></span> <span data-ttu-id="1ad91-186">因為 VMR (或 EVR) 不會在無視窗模式中建立自己的視窗，所以不需要訊息清空。</span><span class="sxs-lookup"><span data-stu-id="1ad91-186">You do not need a message drain, because the VMR (or EVR) does not create its own window in windowless mode.</span></span> <span data-ttu-id="1ad91-187">相反地，它會直接在您的應用程式視窗上進行繪製。</span><span class="sxs-lookup"><span data-stu-id="1ad91-187">Instead, it draws directly onto your application window.</span></span> <span data-ttu-id="1ad91-188">如果目的地矩形小於應用程式工作區，則在計算 DVD 按鈕位置時，DVD 導覽器會將此納入考慮。</span><span class="sxs-lookup"><span data-stu-id="1ad91-188">If the destination rectangle is smaller than the application client area, the DVD Navigator takes this into account when it calculates the DVD button positions.</span></span> <span data-ttu-id="1ad91-189">因此，當您取得滑鼠訊息時，可以將座標直接傳遞至 DVD 導覽器，如一節的功能表導覽所述。</span><span class="sxs-lookup"><span data-stu-id="1ad91-189">Therefore, when you get a mouse message, you can pass the coordinates directly to the DVD Navigator, as described in the section Menu Navigation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ad91-190">相關主題</span><span class="sxs-lookup"><span data-stu-id="1ad91-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ad91-191">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="1ad91-191">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 
