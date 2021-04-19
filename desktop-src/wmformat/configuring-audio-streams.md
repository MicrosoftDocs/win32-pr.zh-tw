---
title: 設定音訊串流
description: 設定音訊串流
ms.assetid: 6ddd9bc1-3fde-4098-afce-fdda461ced62
keywords:
- 串流，設定音訊串流
- 編解碼器，設定音訊串流
- 音訊串流，設定
- 編解碼器，格式
- 資料流程，IWMCodecInfo 介面
- IWMCodecInfo，音訊串流
- 資料流程，A/V 同步處理
- 音訊串流，A/V 同步處理
- A/V 同步處理
- 資料流程，同步處理 A/V
- 音訊串流，同步處理 A/V
- 串流，低延遲音訊格式
- 音訊串流，低延遲音訊格式
- 編解碼器、低延遲音訊格式
- '資料流程、變數位元速率 (VBR) '
- '音訊串流，變數位元速率 (VBR) '
- '編解碼器、變數位元速率 (VBR) '
- 變數位元速率 (VBR) ，設定
- VBR (變數位速率) ，設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad3931ec41e73c125417d39cdd177dc16056e9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106979670"
---
# <a name="configuring-audio-streams"></a><span data-ttu-id="1eb2c-122">設定音訊串流</span><span class="sxs-lookup"><span data-stu-id="1eb2c-122">Configuring Audio Streams</span></span>

<span data-ttu-id="1eb2c-123">音訊串流通常是最直接的設定。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-123">Audio streams are generally the most straightforward to configure.</span></span> <span data-ttu-id="1eb2c-124">使用 [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo) 的方法取得編解碼器的串流設定，如 [從編解碼器取得串流設定資訊](getting-stream-configuration-information-from-codecs.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-124">Get a stream configuration from the codec using the methods of [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo) as described in [Getting Stream Configuration Information from Codecs](getting-stream-configuration-information-from-codecs.md).</span></span> <span data-ttu-id="1eb2c-125">在大多數情況下，您不應該從抓取的設定改變設定。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-125">Under most circumstances, you should not alter the settings from those retrieved.</span></span>

<span data-ttu-id="1eb2c-126">您從列舉所選取的編解碼器格式，取決於使用設定檔所建立之 ASF 檔案的用途。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-126">The codec format that you select from those enumerated depends upon the intended use of the ASF files made with the profile.</span></span> <span data-ttu-id="1eb2c-127">[**IWMCodecInfo2：： GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc)所取出的編解碼器格式描述會摘要說明格式的特性。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-127">The codec format description retrieved by [**IWMCodecInfo2::GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc) summarizes the characteristics of the format.</span></span> <span data-ttu-id="1eb2c-128">如果您的應用程式未顯示在它們之間選擇的描述，您可以在編解碼器格式的 [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)介面上呼叫 **QueryInterface** ，以取得 [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)介面。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-128">If your application does not display the descriptions to choose between them, you can call **QueryInterface** on the [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) interface of the codec format to get the [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) interface.</span></span> <span data-ttu-id="1eb2c-129">然後，您可以藉由呼叫 [**IWMMediaProps：： GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)來取出 [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)結構。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-129">Then you can retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure by calling [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span></span> <span data-ttu-id="1eb2c-130">藉由檢查 **WM \_ 媒體 \_ 類型** 結構和其指向的 [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) 結構，您可以判斷編解碼器格式的設定，並將其與您的需求進行比較。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-130">By examining the **WM\_MEDIA\_TYPE** structure and the [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) structure it points to, you can determine the settings of the codec format and compare them to your requirements.</span></span>

## <a name="getting-audio-formats-for-av-synchronization"></a><span data-ttu-id="1eb2c-131">取得/V 同步處理的音訊格式</span><span class="sxs-lookup"><span data-stu-id="1eb2c-131">Getting Audio Formats for A/V Synchronization</span></span>

<span data-ttu-id="1eb2c-132">Windows Media 音訊編解碼器和 Windows Media 音訊 Professional 編解碼器都支援僅限音訊檔案和音訊/影片檔案的格式。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-132">The Windows Media Audio codec and Windows Media Audio Professional codec both support formats for audio-only files and for audio/video files.</span></span> <span data-ttu-id="1eb2c-133">僅限音訊格式可針對只包含音訊資料的檔案進行優化，而音訊/影片格式則是針對具有影片串流之檔案中的音訊進行優化。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-133">The audio-only formats are optimized for files containing only audio data, while the audio/video formats are optimized for audio that is in a file with a video stream.</span></span> <span data-ttu-id="1eb2c-134">列舉這些編解碼器的編解碼器格式時，音訊/影片格式會出現在僅限音訊格式的之後。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-134">When enumerating codec formats for these codecs, the audio/video formats come after the audio-only formats.</span></span> <span data-ttu-id="1eb2c-135">音訊/影片格式描述全都包含 " (A/V) " 字串。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-135">The audio/video format descriptions all contain the string "(A/V)".</span></span> <span data-ttu-id="1eb2c-136">您可以藉由檢查每秒的封包數，以程式設計方式識別針對音訊/影片同步處理設計的格式。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-136">You can identify the formats designed for audio/video synchronization programmatically by checking the number of packets per second.</span></span> <span data-ttu-id="1eb2c-137">如果位元速率大於或等於每秒32000位，則同步處理的格式有5個或更多的封包。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-137">Formats for synchronization have 5 or more packets per second if the bit rate is greater than or equal to 32,000 bits per second.</span></span> <span data-ttu-id="1eb2c-138">位元速率小於每秒32000位的格式，如果每秒使用3個或更多封包，則可以搭配同步處理的影片使用。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-138">Formats with bit rates less than 32,000 bits per second can be used with synchronized video if they use 3 or more packets per second.</span></span> <span data-ttu-id="1eb2c-139">[ [尋找音訊格式](to-find-audio-formats.md) ] 主題中的程式碼範例包含進行這項檢查所需的程式碼：</span><span class="sxs-lookup"><span data-stu-id="1eb2c-139">The code example in the [To Find Audio Formats](to-find-audio-formats.md) topic contains the code required to make this check:</span></span>


```C++
if((pWave->nAvgBytesPerSec / pWave->nBlockAlign) >= 
       ((pWave->nAvgBytesPerSec >= 4000) ? 5.0 : 3.0))
{
    // Set this stream configuration as the new best match.
}
```



## <a name="getting-low-delay-audio-formats"></a><span data-ttu-id="1eb2c-140">取得 Low-Delay 的音訊格式</span><span class="sxs-lookup"><span data-stu-id="1eb2c-140">Getting Low-Delay Audio Formats</span></span>

<span data-ttu-id="1eb2c-141">Windows Media 9.1 編解碼器和 Windows Media 音訊 9.1 Professional 編解碼器都支援低延遲格式。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-141">The Windows Media 9.1 codec and the Windows Media Audio 9.1 Professional codec both support low-delay formats.</span></span> <span data-ttu-id="1eb2c-142">這些格式的緩衝區視窗比其他音訊格式小。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-142">These formats have a smaller buffer window than other audio formats.</span></span> <span data-ttu-id="1eb2c-143">低延遲音訊的目的在於改善檔案或資料流程經常切換的案例中的效能;例如，應用程式會列出在使用者介面中進行串流處理的許多歌曲，並允許使用者在兩者之間進行切換。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-143">Low-delay audio is intended to improve performance in scenarios where files or streams will be switched frequently; for example, an application that lists a number of songs for streaming in the user interface and allows users to arbitrarily switch between them.</span></span>

<span data-ttu-id="1eb2c-144">低延遲格式只能在 CBR 模式下使用， (一次或兩次傳遞) 。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-144">Low-delay formats are available only in CBR mode (one-pass or two-pass).</span></span> <span data-ttu-id="1eb2c-145">低延遲格式的描述全都包含「低延遲」字串。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-145">The low-delay format descriptions all contain the string "Low Delay".</span></span> <span data-ttu-id="1eb2c-146">您可以藉由檢查格式的位元速率值，以程式設計方式識別格式。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-146">You can identify the formats programmatically by checking the bit-rate value of the format.</span></span> <span data-ttu-id="1eb2c-147">低延遲格式的指派位速率為1，小於相等一般格式的位元速率。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-147">The low-delay formats are assigned bit rates that are 1 kilobit less than the bit rates of the equivalent normal format.</span></span> <span data-ttu-id="1eb2c-148">例如，Windows Media 音訊9.1 編解碼器支援使用位元速率為 192 kbps 的單一傳遞 CBR 格式。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-148">For example, the Windows Media Audio 9.1 codec supports a single-pass CBR format with a bit rate of 192 kbps.</span></span> <span data-ttu-id="1eb2c-149">相等的低延遲格式的位元速率為 191 kbps。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-149">The equivalent low-delay format has a bit rate of 191 kbps.</span></span> <span data-ttu-id="1eb2c-150">此外，除了 Windows Media 音訊9.1 編解碼器所支援的 5 kbps mono 格式之外，低延遲格式是具有奇數位元速率值的唯一格式。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-150">In addition, with the exception of the 5 kbps mono format supported by the Windows Media Audio 9.1 codec, the low-delay formats are the only formats that have an odd bit-rate value.</span></span>

## <a name="configuring-variable-bit-rate-audio"></a><span data-ttu-id="1eb2c-151">設定變數位元速率音訊</span><span class="sxs-lookup"><span data-stu-id="1eb2c-151">Configuring Variable Bit Rate Audio</span></span>

<span data-ttu-id="1eb2c-152">當您的其中一個 Windows Media 音訊編解碼器需要變數位元速率 (VBR) 格式時，您可以在 [**IWMCodecInfo3：： SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) 方法中設定列舉設定來取得它。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-152">When you need a variable bit rate (VBR) format for one of the Windows Media audio codecs, you can get it by setting the enumeration settings in the [**IWMCodecInfo3::SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) method.</span></span> <span data-ttu-id="1eb2c-153">將 g \_ wszVBREnabled 設為 True，並針對以品質為基礎的 vbr 將 g wszNumPasses 設定為1，並將 \_ 兩個進行 vbr (受限或未受限制的) 設定為2。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-153">Set g\_wszVBREnabled to True, and set g\_wszNumPasses to 1 for quality-based VBR or 2 for two-pass VBR (constrained or unconstrained).</span></span> <span data-ttu-id="1eb2c-154">如果您使用受限制的雙向 VBR，您必須使用 [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) 的方法（如設定 [VBR 資料流程](configuring-vbr-streams.md)中所述），手動設定資料流程的最大位元速率和緩衝區視窗。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-154">If you are using constrained two-pass VBR, you must manually set the maximum bit rate and buffer window for the stream using the methods of [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) as described in [Configuring VBR Streams](configuring-vbr-streams.md).</span></span>

<span data-ttu-id="1eb2c-155">在以品質為基礎的 VBR 設定檔中， **WAVEFORMATEX** 結構的 **nAvgBytesPerSec** 成員會包含低序位位元組 (1 到 100) 的品質層級，而三個高序位的位元組則會設定為0x7fffff。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-155">In quality-based VBR profiles, the **nAvgBytesPerSec** member of the **WAVEFORMATEX** structure contains the quality level (1 through 100) in the low-order byte and the three high-order bytes are set to 0x7fffff.</span></span> <span data-ttu-id="1eb2c-156">請勿嘗試手動修改此值以修改品質設定;您必須使用從編解碼器取出的格式。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-156">Do not attempt to modify the quality setting by modifying this value manually; you must use the format as it is retrieved from the codec.</span></span> <span data-ttu-id="1eb2c-157">若要使用不同的品質值，您必須列舉格式，直到找到符合您需求的格式為止。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-157">To use a different quality value, you must enumerate formats until you find one that meets your needs.</span></span> <span data-ttu-id="1eb2c-158">此外， **nAvgBytesPerSec** 不會保留在 ASF 檔案中;當您取得使用 reader 物件開啟之檔案的 **WAVEFORMATEX** 結構時， **nAvgBytesPerSec** 會包含代表每秒位元組平均位元組數的近似值。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-158">Also, **nAvgBytesPerSec** will not be preserved in the ASF file; when you obtain the **WAVEFORMATEX** structure for a file that has been opened with the reader object, **nAvgBytesPerSec** contains an approximate value representing the average number of bytes per second.</span></span>

> [!Note]  
> <span data-ttu-id="1eb2c-159">設定音訊串流時，您的音訊緩衝區視窗值絕對不能大於檔案中任何影片資料流程的值。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-159">When configuring audio streams, you should never have an audio buffer window value that is greater than the value for any video streams in the file.</span></span> <span data-ttu-id="1eb2c-160">通常這並不成問題，因為音訊緩衝區視窗值的範圍應介於1.5 到3秒之間，而影片值的範圍應介於3到5秒之間。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-160">Normally this is not an issue, as audio buffer window values should range between 1.5 and 3 seconds and video values should range between 3 and 5 seconds.</span></span> <span data-ttu-id="1eb2c-161">如果 [音訊緩衝區] 視窗大於 [影片緩衝區] 視窗，檔案將會播放到與同步處理稍微不同的資料流程。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-161">If an audio buffer window is greater than a video buffer window, the file will play back with the streams slightly out of synchronization.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1eb2c-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="1eb2c-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1eb2c-163">**所有資料流程通用的設定**</span><span class="sxs-lookup"><span data-stu-id="1eb2c-163">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="1eb2c-164">**設定資料流程**</span><span class="sxs-lookup"><span data-stu-id="1eb2c-164">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="1eb2c-165">**尋找音訊格式**</span><span class="sxs-lookup"><span data-stu-id="1eb2c-165">**To Find Audio Formats**</span></span>](to-find-audio-formats.md)
</dt> </dl>

 

 