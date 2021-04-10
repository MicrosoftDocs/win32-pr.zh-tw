---
title: '設定 WM ASF 寫入器 (QASF) '
description: '設定 WM ASF 寫入器 (QASF) '
ms.assetid: 0f49ed5a-c228-456a-9551-8d277adccd0e
keywords:
- 'Windows Media 格式 SDK，設定 WM ASF 寫入器 (QASF) '
- Windows Media Format SDK、DirectShow
- Windows Media Format SDK，WM ASF 寫入器
- Windows Media Format SDK、QASF
- 'Advanced Systems Format (ASF) 、設定 WM ASF 寫入器 (QASF) '
- 'ASF (Advanced Systems Format) 、設定 WM ASF 寫入器 (QASF) '
- Advanced Systems Format (ASF) 、WM ASF 寫入器
- ASF (Advanced Systems Format) ，WM ASF 寫入器
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- Advanced Systems Format (ASF) ，QASF
- ASF (Advanced Systems Format) ，QASF
- 'DirectShow，設定 WM ASF 寫入器 (QASF) '
- DirectShow、WM ASF 寫入器
- DirectShow、QASF
- WM ASF 寫入器，設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72f954522c4acae89e6f6dd001561811088c2a9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093107"
---
# <a name="configuring-the-wm-asf-writer-qasf"></a><span data-ttu-id="73ce2-119">設定 WM ASF 寫入器 (QASF) </span><span class="sxs-lookup"><span data-stu-id="73ce2-119">Configuring the WM ASF Writer (QASF)</span></span>

<span data-ttu-id="73ce2-120">當您建立了 [WM ASF 寫入](wm-asf-writer-filter.md) 器篩選器時，它會自動使用 WMProfile \_ V80 \_ 256Video 設定檔來設定為預設值。</span><span class="sxs-lookup"><span data-stu-id="73ce2-120">When the [WM ASF Writer](wm-asf-writer-filter.md) filter is created, it is configured automatically with the WMProfile\_V80\_256Video profile as a default.</span></span> <span data-ttu-id="73ce2-121">因為此設定檔使用 Windows Media 音訊和 Windows Media 視訊第8版編解碼器，建議您建立使用 Windows Media 9 系列編解碼器的自訂設定檔，然後使用 [**IConfigAsfWriter：： ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md)方法將其 [**IWMProfile**](iwmprofile.md)指標傳遞至篩選。</span><span class="sxs-lookup"><span data-stu-id="73ce2-121">Because this profile uses the Windows Media Audio and Windows Media Video version 8 codecs, it is recommended that you create a custom profile that uses the Windows Media 9 Series codecs, and then pass its [**IWMProfile**](iwmprofile.md) pointer to the filter using the [**IConfigAsfWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) method.</span></span> <span data-ttu-id="73ce2-122">必須先將篩選新增至圖形，才能設定篩選，而且必須先設定篩選器，才能連接到上游篩選器。</span><span class="sxs-lookup"><span data-stu-id="73ce2-122">The filter must be added to the graph before the filter can be configured, and it must be configured before it can be connected to upstream filters.</span></span> <span data-ttu-id="73ce2-123">此篩選器會使用設定檔來決定要寫入的 Windows Media 格式檔案類型、要設定的輸入釘選數目，以及 pin 可以接受的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="73ce2-123">The filter uses the profile to determine what kind of Windows Media Format file to write, how many input pins to set up, and what media types the pins can accept.</span></span>

<span data-ttu-id="73ce2-124">當新的設定檔不需要任何額外的輸入 pin 時，篩選器可讓設定檔在其輸入 pin 連線時重設。</span><span class="sxs-lookup"><span data-stu-id="73ce2-124">The filter allows profiles to be reset while its input pins are connected, as long as the new profile does not require any additional input pins.</span></span> <span data-ttu-id="73ce2-125">例如，如果您將設定檔從單一輸入的僅限音訊設定檔變更為雙輸入音訊和影片設定檔，則只需要將音訊 pin reconnectedAll 輸入資料必須加上時間戳記，而且必須先連接所有輸入圖釘，才能執行或暫停篩選。</span><span class="sxs-lookup"><span data-stu-id="73ce2-125">For example, if you change the profile from a one-input audio-only profile to a two-input audio and video profile, just the audio pin will be reconnectedAll input data must be time-stamped, and all input pins must be connected before the filter can be run or paused.</span></span> <span data-ttu-id="73ce2-126">這表示，如果您使用具有音訊串流和影片串流的設定檔來設定篩選準則，則篩選準則會建立音訊和影片輸入的 pin，而且必須先連接這兩個 pin，然後才能執行篩選。</span><span class="sxs-lookup"><span data-stu-id="73ce2-126">This means that if you configure the filter with a profile that has an audio stream and a video stream, the filter will create an audio and a video input pin, and both pins must be connected before the filter can be run.</span></span>

<span data-ttu-id="73ce2-127">新增資料單位延伸模組</span><span class="sxs-lookup"><span data-stu-id="73ce2-127">Adding Data Unit Extensions</span></span>

<span data-ttu-id="73ce2-128">您可以設定資料單位延伸模組的設定檔串流，例如在連接篩選器之前或之後的 SMPTE 時間代碼，只要遵循此作業順序：</span><span class="sxs-lookup"><span data-stu-id="73ce2-128">You can configure a profile stream for data unit extensions, such as SMPTE time codes, either before or after the filter is connected, as long as you follow this order of operations:</span></span>

1.  <span data-ttu-id="73ce2-129">使用 [**IWMStreamConfig2：： AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension)，將一個或多個資料單位延伸加入至資料流程。</span><span class="sxs-lookup"><span data-stu-id="73ce2-129">Add one or more data unit extensions to the stream using [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).</span></span>
2.  <span data-ttu-id="73ce2-130">呼叫 [**WMProfile：： ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) 來更新設定檔。</span><span class="sxs-lookup"><span data-stu-id="73ce2-130">Call [**WMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) to update the profile.</span></span>
3.  <span data-ttu-id="73ce2-131">以更新的設定檔物件呼叫 [**IConfigAsfWriter：： ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) 。</span><span class="sxs-lookup"><span data-stu-id="73ce2-131">Call [**IConfigAsfWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) with the updated profile object.</span></span>
4.  <span data-ttu-id="73ce2-132">尋找影片輸入 pin，並呼叫其 [**IAMWMBufferPass：： SetNotify**](iamwmbufferpass-setnotify.md) 方法來註冊您的應用程式定義 [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) 介面。</span><span class="sxs-lookup"><span data-stu-id="73ce2-132">Find the video input pin, and call its [**IAMWMBufferPass::SetNotify**](iamwmbufferpass-setnotify.md) method to register your application-defined [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) interface.</span></span>

<span data-ttu-id="73ce2-133">當圖形執行時，將會針對每個框架呼叫 [**IAMWMBufferPassCallback：： Notify**](iamwmbufferpasscallback-notify.md) 方法，而且您將可以使用其 [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) 介面方法來取得和設定範例上的屬性。</span><span class="sxs-lookup"><span data-stu-id="73ce2-133">When the graph runs, your [**IAMWMBufferPassCallback::Notify**](iamwmbufferpasscallback-notify.md) method will be called for each frame, and you will be able to get and set properties on the sample using its [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface methods.</span></span>

> [!Note]  
> <span data-ttu-id="73ce2-134">在某些耗用大量處理器的案例中，例如反向電視的情況下，WM ASF 寫入器可能需要的輸出緩衝區比某些下游篩選器可支援的更多。</span><span class="sxs-lookup"><span data-stu-id="73ce2-134">In some processor-intensive scenarios such as inverse telecine, the WM ASF Writer may require more output buffers than some downstream filters can support.</span></span> <span data-ttu-id="73ce2-135">例如，DV 解碼器將不會接受一個以上的緩衝區作為輸出 pin，而且在某些情況下，AVI 解壓縮程式也是如此。</span><span class="sxs-lookup"><span data-stu-id="73ce2-135">The DV Decoder, for example, will not accept more than one buffer for its output pin and the same is true for the AVI Decompressor in certain conditions.</span></span> <span data-ttu-id="73ce2-136">如果您在嘗試連線至這些篩選器時遇到問題，或在執行圖形時遇到問題，可能需要撰寫可接受其輸出 pin 上任意數目緩衝區的中繼篩選。</span><span class="sxs-lookup"><span data-stu-id="73ce2-136">If you encounter problems when attempting to connect to these filters, or possibly when running the graph, it may be necessary to write an intermediary filter that accepts any number of buffers on its output pin.</span></span>

 

 

 