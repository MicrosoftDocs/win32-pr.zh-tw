---
title: 啟用 DirectX Video 加速
description: 啟用 DirectX Video 加速
ms.assetid: 5cb2f564-88e3-4b60-bde3-6ccf69c97c48
keywords:
- Windows Media Format SDK，啟用 DXVA
- 'Windows Media Format SDK、DirectX Video 加速 (DXVA) '
- Windows Media Format SDK，影片加速
- Advanced Systems Format (ASF) ，啟用 DXVA
- ASF (Advanced Systems Format) ，啟用 DXVA
- 'Advanced Systems Format (ASF) 、DirectX Video 加速 (DXVA) '
- 'ASF (Advanced Systems Format) 、DirectX Video 加速 (DXVA) '
- Advanced Systems Format (ASF) 、影片加速
- ASF (Advanced Systems Format) 、影片加速
- DirectX Video 加速 (DXVA) ，啟用
- DXVA (DirectX Video 加速) ，啟用
- DirectX Video 加速 (DXVA) 、作業順序
- DXVA (DirectX Video 加速) 、營運順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896147fe11b4b7f5fb91d8dc288e616b643bd5ce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374394"
---
# <a name="enabling-directx-video-acceleration"></a><span data-ttu-id="1f858-116">啟用 DirectX Video 加速</span><span class="sxs-lookup"><span data-stu-id="1f858-116">Enabling DirectX Video Acceleration</span></span>

<span data-ttu-id="1f858-117">本節說明在自訂播放流程中播放串流內容時，如何啟用 Microsoft® DirectX®影片加速。</span><span class="sxs-lookup"><span data-stu-id="1f858-117">This section describes how to enable Microsoft® DirectX® Video Acceleration when playing streamed content in a custom player.</span></span>

## <a name="background"></a><span data-ttu-id="1f858-118">背景</span><span class="sxs-lookup"><span data-stu-id="1f858-118">Background</span></span>

<span data-ttu-id="1f858-119">DirectX Video 加速 (DirectX VA) 是一種 API 規格，適用于進行2D 解碼作業的硬體加速。</span><span class="sxs-lookup"><span data-stu-id="1f858-119">DirectX Video Acceleration (DirectX VA) is an API specification for hardware acceleration of 2-D decoding operations.</span></span> <span data-ttu-id="1f858-120">它可讓軟體解碼器將某些需要大量 CPU 的作業卸載至圖形配接器進行處理。</span><span class="sxs-lookup"><span data-stu-id="1f858-120">It enables software decoders to offload certain CPU-intensive operations to the graphics card for processing.</span></span> <span data-ttu-id="1f858-121">針對終端使用者，這可讓您在配備 DirectX VA 相容圖形配接器的舊電腦上，進行全螢幕 DVD 播放這類高比率的影片。</span><span class="sxs-lookup"><span data-stu-id="1f858-121">For end users, this makes possible high-bit-rate video such as full-screen DVD playback on older computers equipped with DirectX VA-compatible graphics cards.</span></span>

<span data-ttu-id="1f858-122">從 Windows Media Format 9 系列 SDK 開始，SQL-DMO 包裝函式篩選器支援 DirectX VA。</span><span class="sxs-lookup"><span data-stu-id="1f858-122">Beginning with the Windows Media Format 9 Series SDK, the DMO Wrapper filter supports DirectX VA.</span></span> <span data-ttu-id="1f858-123">這表示，在本機播放中，應用程式可以使用 WM ASF 讀取器篩選器來播放 Windows Media 內容，而且如果圖形配接器支援 DirectX VA 硬體加速，將會自動叫用。</span><span class="sxs-lookup"><span data-stu-id="1f858-123">This means that, for local playback, applications can use the WM ASF Reader filter to play Windows Media-based content and DirectX VA hardware acceleration will be invoked automatically if the graphics card supports it.</span></span> <span data-ttu-id="1f858-124">但是，「WM ASF 讀取器」篩選器不支援播放資料流程內容。</span><span class="sxs-lookup"><span data-stu-id="1f858-124">However, the WM ASF Reader filter does not support playback of streamed content.</span></span> <span data-ttu-id="1f858-125">因此，如果您想要在自訂播放程式中播放資料流程處理的內容時支援 DirectX VA，您必須使用替代機制，也就是 Windows Media Player 從 Windows Media 9 系列開始使用的機制。</span><span class="sxs-lookup"><span data-stu-id="1f858-125">Therefore, if you want to support DirectX VA when playing streamed content in a custom player, you must use an alternate mechanism, which is the one used by Windows Media Player beginning with the Windows Media 9 Series.</span></span>

<span data-ttu-id="1f858-126">由於 Windows Media Player 是在開發 QASF 篩選之前設計的，因此 Windows Media Player 有自己的來源篩選器（以 Windows Media Format SDK 為基礎）來播放 Windows Media 格式的內容。</span><span class="sxs-lookup"><span data-stu-id="1f858-126">Because Windows Media Player was designed before the QASF filters had been developed, Windows Media Player has its own source filter, based on the Windows Media Format SDK, for playing Windows Media-based content.</span></span> <span data-ttu-id="1f858-127">WMP Windows Media 來源篩選器會將解壓縮的資料直接提供給音訊和影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="1f858-127">The WMP Windows Media Source Filter delivers decompressed data downstream directly to the audio and video renderers.</span></span> <span data-ttu-id="1f858-128">相較之下，WM 的 ASF 讀取器會將壓縮的內容傳遞至 Windows Media 解碼器 DirectX 媒體物件 (DMOs) ，而這些物件是裝載于 SQL-DMO 包裝函式中。</span><span class="sxs-lookup"><span data-stu-id="1f858-128">By contrast, the WM ASF Reader delivers compressed content downstream to the Windows Media Decoder DirectX Media Objects (DMOs), which are hosted inside the DMO Wrapper.</span></span> <span data-ttu-id="1f858-129">下圖說明 WM ASF 讀取器和 WMP Windows Media 來源篩選器之間的差異。</span><span class="sxs-lookup"><span data-stu-id="1f858-129">The following diagrams illustrate the differences between the WM ASF Reader and the WMP Windows Media Source Filter.</span></span>

![自訂來源篩選輸出未壓縮的範例](images/wmp-dxva-graph.png)

![qasf 來源篩選輸出壓縮的範例](images/qasf-dxva-graph.png)

<span data-ttu-id="1f858-132">若要啟用串流內容的 DirectX VA，您必須建立自訂來源篩選器，例如頂端圖表中的篩選器。</span><span class="sxs-lookup"><span data-stu-id="1f858-132">To enable DirectX VA for streamed content, you must create a custom source filter like the one in the top diagram.</span></span> <span data-ttu-id="1f858-133">基本上，此篩選器會使用 Windows Media Format SDK 來具現化 WM 讀取器物件、解壓縮範例，並在其輸出圖釘上將它們傳送至下游。</span><span class="sxs-lookup"><span data-stu-id="1f858-133">Basically, this filter will use the Windows Media Format SDK to instantiate a WM Reader object, decompress the samples, and send them downstream on its output pins.</span></span> <span data-ttu-id="1f858-134">本文假設您已建立來源篩選器，現在已準備好執行 DirectX VA 支援。</span><span class="sxs-lookup"><span data-stu-id="1f858-134">This discussion assumes that you have created the source filter already and are now ready to implement the DirectX VA support.</span></span>

<span data-ttu-id="1f858-135">若要啟用 DirectX VA，來源篩選器的基本工作是提供影片轉譯器和 WMV 解碼，以及用來協調 DirectX VA 連線所需的介面。</span><span class="sxs-lookup"><span data-stu-id="1f858-135">To enable DirectX VA, the basic task of the source filter is to provide the Video Renderer and the WMV Decoder DMO with the interfaces they will need to negotiate the DirectX VA connection.</span></span> <span data-ttu-id="1f858-136">來源篩選不會參與這些協商。</span><span class="sxs-lookup"><span data-stu-id="1f858-136">The source filter does not participate in those negotiations.</span></span> <span data-ttu-id="1f858-137">串流開始之後，來源篩選器唯一可以執行的 DirectX VA 相關工作，是在 WMV 解碼將它們傳遞給影片轉譯器之前，修改影片範例上的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="1f858-137">After streaming starts, the only DirectX VA-related task that the source filter can perform is to modify the time stamps on the video samples before the WMV decoder delivers them to the Video Renderer.</span></span> <span data-ttu-id="1f858-138">這麼做的主要原因是要提供自訂的時間軸控制項，超過標準的 DirectShow®介面啟用的範圍。</span><span class="sxs-lookup"><span data-stu-id="1f858-138">The primary reason for doing this is to provide custom timeline control beyond what the standard DirectShow® interfaces enable.</span></span>

<span data-ttu-id="1f858-139">定義了三個介面，以啟用 Windows Media 格式 SDK、播放機的來源篩選器、Windows Media 視訊的解碼器，以及重迭混音器或影片混合轉譯器之間的必要通訊。</span><span class="sxs-lookup"><span data-stu-id="1f858-139">Three interfaces are defined to enable the necessary communications between the Windows Media Format SDK, the player's source filter, the Windows Media Video decoder DMO, and the Overlay Mixer or Video Mixing Renderer.</span></span> <span data-ttu-id="1f858-140">下表將說明這些介面。</span><span class="sxs-lookup"><span data-stu-id="1f858-140">These interfaces are described in the following table.</span></span>



| <span data-ttu-id="1f858-141">介面</span><span class="sxs-lookup"><span data-stu-id="1f858-141">Interface</span></span>                                                        | <span data-ttu-id="1f858-142">描述</span><span class="sxs-lookup"><span data-stu-id="1f858-142">Description</span></span>                                                                                                                                                                                        |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f858-143">**IWMCodecAMVideoAccelerator**</span><span class="sxs-lookup"><span data-stu-id="1f858-143">**IWMCodecAMVideoAccelerator**</span></span>](/previous-versions/windows/desktop/api/wmdxva/nn-wmdxva-iwmcodecamvideoaccelerator) | <span data-ttu-id="1f858-144">由 Windows Media 解碼（由媒體播放機的來源篩選器）所公開，並由媒體播放機的來源篩選器所呼叫，以設定啟用 DirectX VA 以解碼 Windows Media 視訊內容所需的各種連接。</span><span class="sxs-lookup"><span data-stu-id="1f858-144">Exposed by the Windows Media Decoder DMO and called by a media player's source filter to set up the various connections required to enable DirectX VA for decoding of Windows Media Video content.</span></span> |
| [<span data-ttu-id="1f858-145">**IWMPlayerTimestampHook**</span><span class="sxs-lookup"><span data-stu-id="1f858-145">**IWMPlayerTimestampHook**</span></span>](/previous-versions/windows/desktop/api/wmdxva/nn-wmdxva-iwmplayertimestamphook)         | <span data-ttu-id="1f858-146">在播放程式的來源篩選器上執行。</span><span class="sxs-lookup"><span data-stu-id="1f858-146">Implemented on the player's source filter.</span></span> <span data-ttu-id="1f858-147">它可讓篩選準則修改影片範例上的時間戳記，然後再將它們傳遞給下游。</span><span class="sxs-lookup"><span data-stu-id="1f858-147">It enables the filter to modify the time stamps on the video samples before delivering them downstream.</span></span>                                                 |
| [<span data-ttu-id="1f858-148">**IWMReaderAccelerator**</span><span class="sxs-lookup"><span data-stu-id="1f858-148">**IWMReaderAccelerator**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderaccelerator)             | <span data-ttu-id="1f858-149">在 WM 讀取器物件上執行。</span><span class="sxs-lookup"><span data-stu-id="1f858-149">Implemented on the WM Reader object.</span></span> <span data-ttu-id="1f858-150">它是由播放程式來源篩選器呼叫，以取得來自解碼器的介面。</span><span class="sxs-lookup"><span data-stu-id="1f858-150">It is called by a player source filter to obtain interfaces from the decoder DMO.</span></span>                                                                             |



 

## <a name="order-of-operations-in-directx-vaenabled-playback"></a><span data-ttu-id="1f858-151">DirectX VA 中的作業順序-已啟用播放</span><span class="sxs-lookup"><span data-stu-id="1f858-151">Order of Operations in DirectX VA–enabled Playback</span></span>

<span data-ttu-id="1f858-152">本節說明在執行時間，針對已啟用 DirectX VA 的播放程式及其來源篩選作業的一般作業順序。</span><span class="sxs-lookup"><span data-stu-id="1f858-152">This section describes the general order of operations at run time for a DirectX VA-enabled player and its source filter.</span></span> <span data-ttu-id="1f858-153">本節提及的元件包括：</span><span class="sxs-lookup"><span data-stu-id="1f858-153">The components referred to in this section are:</span></span>

-   <span data-ttu-id="1f858-154">協力廠商媒體播放機，稱為 player。</span><span class="sxs-lookup"><span data-stu-id="1f858-154">A third-party media player, referred to as the player.</span></span>
-   <span data-ttu-id="1f858-155">由播放程式具現化的自訂來源篩選器，它會使用 Windows Media Format SDK 來解壓縮 Windows Media 內容。</span><span class="sxs-lookup"><span data-stu-id="1f858-155">A custom source filter, instantiated by the player, that uses the Windows Media Format SDK to decompress Windows Media-based content.</span></span>
-   <span data-ttu-id="1f858-156">播放程式來源篩選的影片輸出釘選，稱為輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="1f858-156">The video output pin of the player's source filter, referred to as the output pin.</span></span>
-   <span data-ttu-id="1f858-157">DirectShow 影片播放篩選圖形，稱為圖形。</span><span class="sxs-lookup"><span data-stu-id="1f858-157">The DirectShow video playback filter graph, referred to as the graph.</span></span>
-   <span data-ttu-id="1f858-158">影片混合轉譯器，稱為 VMR。</span><span class="sxs-lookup"><span data-stu-id="1f858-158">The Video Mixing Renderer, referred to as the VMR.</span></span>
-   <span data-ttu-id="1f858-159">Windows Media Format SDK 非同步讀取器物件，稱為「讀取器」。</span><span class="sxs-lookup"><span data-stu-id="1f858-159">The Windows Media Format SDK Asynchronous Reader object, referred to as the reader.</span></span>
-   <span data-ttu-id="1f858-160">Windows Media 視訊的解碼器 DirectX 媒體物件，稱為「解碼器」。</span><span class="sxs-lookup"><span data-stu-id="1f858-160">The Windows Media Video Decoder DirectX Media Object, referred to as the decoder DMO.</span></span>

<span data-ttu-id="1f858-161">作業的順序如下所示：</span><span class="sxs-lookup"><span data-stu-id="1f858-161">The order of operations is as follows:</span></span>

1.  <span data-ttu-id="1f858-162">播放程式會將其來源篩選器和讀取器物件具現化。</span><span class="sxs-lookup"><span data-stu-id="1f858-162">The player instantiates its source filter and a reader object.</span></span> <span data-ttu-id="1f858-163">讀取器會建立一個 video 解碼，並在其上設定 (壓縮的) 輸入類型。</span><span class="sxs-lookup"><span data-stu-id="1f858-163">The reader creates a video decoder DMO and sets the (compressed) input type on it.</span></span> <span data-ttu-id="1f858-164">在播放程式嘗試設定其影片播放圖形之前，必須先進行這項作業，因為 SDK 和解碼器 SQL-DMO 必須參與圖形的協商程式，而在步驟9中，則必須知道輸入格式。</span><span class="sxs-lookup"><span data-stu-id="1f858-164">This must happen before the player attempts to configure its video playback graph because the SDK and the decoder DMO must be involved in the negotiation process with the graph, and the DMO must know the input format during step 9.</span></span>
2.  <span data-ttu-id="1f858-165">播放程式會呼叫 **IGraphBuilder：： Render**，提供影片來源篩選器的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="1f858-165">The player calls **IGraphBuilder::Render**, providing it the video source filter's output pin.</span></span> <span data-ttu-id="1f858-166">此時，DirectShow 篩選圖形管理員會嘗試將 VMR 連接到播放程式的影片來源篩選。</span><span class="sxs-lookup"><span data-stu-id="1f858-166">At this point, the DirectShow filter graph manager tries to connect the VMR to the player's video source filter.</span></span>
3.  <span data-ttu-id="1f858-167">篩選圖形管理員會在播放程式影片來源篩選器的輸出圖釘上呼叫 **IPin：： Connect** 。</span><span class="sxs-lookup"><span data-stu-id="1f858-167">The filter graph manager calls **IPin::Connect** on the output pin of the player's video source filter.</span></span>

<span data-ttu-id="1f858-168">**IPin：： Connect** 內會發生步驟4到10。</span><span class="sxs-lookup"><span data-stu-id="1f858-168">Steps 4 through 10 occur inside of **IPin::Connect**.</span></span>

1.  <span data-ttu-id="1f858-169">來源篩選器會從讀取器的 **IWMReaderAccelerator：： GetCodecInterface** 方法取得 **IWMCodecAMVideoAccelerator** 介面。</span><span class="sxs-lookup"><span data-stu-id="1f858-169">The source filter obtains the **IWMCodecAMVideoAccelerator** interface from the reader's **IWMReaderAccelerator::GetCodecInterface** method.</span></span> <span data-ttu-id="1f858-170">如果編解碼器不支援 DirectX VA，呼叫 **GetCodecInterface** 可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="1f858-170">If the codec does not support DirectX VA, the call to **GetCodecInterface** may fail.</span></span> <span data-ttu-id="1f858-171">在此情況下，會如往常般進行協調，而不支援 DirectX VA。</span><span class="sxs-lookup"><span data-stu-id="1f858-171">In this case, negotiation proceeds as usual, without DirectX VA support.</span></span>
2.  <span data-ttu-id="1f858-172">來源篩選器會透過 IWMCodecAMVideoAccelerator：： SetAcceleratorInterface，將 **IAMVideoAccelerator** 指標從傳入的 pin **傳遞至** **：：**。</span><span class="sxs-lookup"><span data-stu-id="1f858-172">The source filter passes the **IAMVideoAccelerator** pointer from the pin passed into **Connect** to the decoder DMO through **IWMCodecAMVideoAccelerator::SetAcceleratorInterface**.</span></span>
3.  <span data-ttu-id="1f858-173">然後，來源篩選器會將 **IPin：： connect** 作業的其餘部分委派給 **CBaseOutputPin：： connect** 方法。</span><span class="sxs-lookup"><span data-stu-id="1f858-173">The source filter then delegates the remainder of the **IPin::Connect** operation to the **CBaseOutputPin::Connect** method.</span></span> <span data-ttu-id="1f858-174">使用 SDK 的格式列舉會依照目前的方式繼續進行。</span><span class="sxs-lookup"><span data-stu-id="1f858-174">The format enumeration with the SDK proceeds as it does today.</span></span> <span data-ttu-id="1f858-175">如果編解碼器支援所連接內容的 DirectX VA，則編解碼器會先顯示這些 DirectX VA 子類型，然後再支援 YUV 和 RGB 類型。</span><span class="sxs-lookup"><span data-stu-id="1f858-175">If the codec supports DirectX VA for the content being connected, the codec DMO presents those DirectX VA subtypes first, prior to the YUV and RGB types supported.</span></span> <span data-ttu-id="1f858-176">如果有 DirectX VA 支援，則會嘗試在 DirectX VA 子類型的內容中進行步驟7到11。</span><span class="sxs-lookup"><span data-stu-id="1f858-176">If DirectX VA support is available, steps 7 through 11 are attempted in the context of a DirectX VA subtype.</span></span> <span data-ttu-id="1f858-177">下列程式碼片段說明如何識別 DirectX VA 媒體子類型。</span><span class="sxs-lookup"><span data-stu-id="1f858-177">The following code snippet shows how to identify a DirectX VA media subtype.</span></span>
    ```C++
    bool IsDXVASubtype( AM_MEDIA_TYPE * pmt )
    {
        // All DXVA types have the same last 3 DWORDs.
        // guidDXVA is the base GUID for all DXVA subtypes.

        GUID guidDXVA = { 0x00000000, 0xa0c7, 0x11d3, { 0xb9,0x84,0x00,0xc0,0x4f,0x2e,0x73,0xc5 } };

        unsigned long const * plguid;
        unsigned long const * plguidDXVA;
        plguid = (unsigned long const *)&pmt->subtype;
        plguidDXVA = (unsigned long *)&guidDXVA;

        if( ( plguid[1] == plguidDXVA[1] ) &&
            ( plguid[2] == plguidDXVA[2] ) &&
            ( plguid[3] == plguidDXVA[3] ) )
        {
            return true;
        }

        return false;
    }
    
    ```

    

4.  <span data-ttu-id="1f858-178">**CBaseOutputPin：： Connect** 執行會在步驟3期間呼叫 **IPin：： CompleteConnect** 。</span><span class="sxs-lookup"><span data-stu-id="1f858-178">The **CBaseOutputPin::Connect** implementation calls **IPin::CompleteConnect** during step 3.</span></span> <span data-ttu-id="1f858-179">如果考慮到 DirectX VA 子類型，則會嘗試 DirectX VA 協商。</span><span class="sxs-lookup"><span data-stu-id="1f858-179">If a DirectX VA subtype is being considered, the DirectX VA negotiation is attempted.</span></span> <span data-ttu-id="1f858-180">輸出圖釘會呼叫 **IWMCodecAMVideoAccelerator：： NegotiateConnection**，並將目前的輸出媒體類型傳遞給它。</span><span class="sxs-lookup"><span data-stu-id="1f858-180">The output pin calls **IWMCodecAMVideoAccelerator::NegotiateConnection**, passing it the current output media type.</span></span>
5.  <span data-ttu-id="1f858-181">在 IAMVideoAccelerator 介面中，VMR 會透過介面執行必要的協商，並傳回兩個已同意的影片子類型 GUID。</span><span class="sxs-lookup"><span data-stu-id="1f858-181">The decoder DMO performs the required negotiation with the VMR through the **IAMVideoAccelerator** interface, and returns the video subtype GUID that the two have agreed on.</span></span> <span data-ttu-id="1f858-182">輸出圖釘會將在此處理過程中收到的所有 **IAMVideoAcceleratorNotify** 呼叫委派給 **IAMVideoAcceleratorNotify** 介面，也可以透過 **IWMReaderAccelerator：： GetCodecInterface** 方法取得。</span><span class="sxs-lookup"><span data-stu-id="1f858-182">The output pin delegates all **IAMVideoAcceleratorNotify** calls received during this process to the decoder DMO's **IAMVideoAcceleratorNotify** interface, which can also be obtained through the **IWMReaderAccelerator::GetCodecInterface** method.</span></span>
6.  <span data-ttu-id="1f858-183">如果 **NegotiateConnection** 成功，輸出圖釘會呼叫 **IWMCodecAMVideoAccelerator：： SetPlayerNotify** 和 **IWMPlayerTimestampHook** 介面。</span><span class="sxs-lookup"><span data-stu-id="1f858-183">If **NegotiateConnection** succeeds, the output pin calls **IWMCodecAMVideoAccelerator::SetPlayerNotify** with an **IWMPlayerTimestampHook** interface.</span></span> <span data-ttu-id="1f858-184">此攔截器可讓來源篩選器先更新範例上的時間戳記，然後再將它們交給轉譯器。</span><span class="sxs-lookup"><span data-stu-id="1f858-184">This hook allows the source filter to update the time stamps on the samples before they are handed to the renderer.</span></span>
7.  <span data-ttu-id="1f858-185">來源篩選準則會以協商的媒體類型呼叫 **IWMReaderAccelerator：： Notify** 。</span><span class="sxs-lookup"><span data-stu-id="1f858-185">The source filter calls **IWMReaderAccelerator::Notify** with the negotiated media type.</span></span> <span data-ttu-id="1f858-186">這可讓讀取器更新其內部變數，並認可至 DirectX VA。</span><span class="sxs-lookup"><span data-stu-id="1f858-186">This allows the reader to update its internal variables and commit to DirectX VA.</span></span> <span data-ttu-id="1f858-187">這是編解碼器或讀取器可能失敗的最後一個位置。</span><span class="sxs-lookup"><span data-stu-id="1f858-187">This is the last place the codec or reader can fail.</span></span> <span data-ttu-id="1f858-188">如果上述任何一個步驟失敗，來源篩選應該會返回步驟3，並嘗試由讀取器列舉的下一個型別。</span><span class="sxs-lookup"><span data-stu-id="1f858-188">If any of the above steps fail, the source filter should return to step 3 and try the next type enumerated by the reader.</span></span>
8.  <span data-ttu-id="1f858-189">播放開始。</span><span class="sxs-lookup"><span data-stu-id="1f858-189">Playback starts.</span></span> <span data-ttu-id="1f858-190">如果連線輸出類型為 DirectX VA，讀取器會忽略來自解碼器的輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1f858-190">The reader ignores output buffers from the decoder DMO if the connection output type is DirectX VA.</span></span>
9.  <span data-ttu-id="1f858-191">當 **IPin：:D isconnect** 時，來源篩選會使用 **Null** 來呼叫 **IWMCodecAMVideoAccelerator：： SetAcceleratorInterface** 。</span><span class="sxs-lookup"><span data-stu-id="1f858-191">When **IPin::Disconnect** occurs, the source filter calls **IWMCodecAMVideoAccelerator::SetAcceleratorInterface** with a **NULL**.</span></span> <span data-ttu-id="1f858-192">這會中斷編解碼器與轉譯器之間的 DirectX VA 連接。</span><span class="sxs-lookup"><span data-stu-id="1f858-192">This breaks the DirectX VA connection between the codec and the renderer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f858-193">相關主題</span><span class="sxs-lookup"><span data-stu-id="1f858-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f858-194">**讀取 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="1f858-194">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




