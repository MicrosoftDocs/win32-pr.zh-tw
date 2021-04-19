---
title: 設定影片串流
description: 設定影片串流
ms.assetid: caffdfc1-3c35-4b7b-8643-5a9095cc11f6
keywords:
- 串流，設定影片串流
- 編解碼器，設定影片串流
- 影片串流，設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d2389026dc1061064c5e687da60c3350ad94a4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106966841"
---
# <a name="configuring-video-streams"></a><span data-ttu-id="45f3d-106">設定影片串流</span><span class="sxs-lookup"><span data-stu-id="45f3d-106">Configuring Video Streams</span></span>

<span data-ttu-id="45f3d-107">影片串流的設定比音訊串流更有彈性。</span><span class="sxs-lookup"><span data-stu-id="45f3d-107">Video streams are more flexible in their configuration than audio streams.</span></span> <span data-ttu-id="45f3d-108">這是因為組成影片的框架屬性可能會與下一個檔案有很大的差異。</span><span class="sxs-lookup"><span data-stu-id="45f3d-108">This is because the properties of the frames that make up the video can vary widely from one file to the next.</span></span> <span data-ttu-id="45f3d-109">當您針對所使用的編解碼器取得編解碼器格式時，您必須設定影片串流設定物件的下列值。</span><span class="sxs-lookup"><span data-stu-id="45f3d-109">When you retrieve the codec format for the codec you are using, you must set the following values for video stream configuration objects.</span></span>



| <span data-ttu-id="45f3d-110">值</span><span class="sxs-lookup"><span data-stu-id="45f3d-110">Value</span></span>                                 | <span data-ttu-id="45f3d-111">描述</span><span class="sxs-lookup"><span data-stu-id="45f3d-111">Description</span></span>                                                                                                                                                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45f3d-112">位元速率</span><span class="sxs-lookup"><span data-stu-id="45f3d-112">Bit rate</span></span>                              | <span data-ttu-id="45f3d-113">呼叫 [**IWMStreamConfig：： SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate) ，將設定為所需的值。</span><span class="sxs-lookup"><span data-stu-id="45f3d-113">Call [**IWMStreamConfig::SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate) to set to the desired value.</span></span> <span data-ttu-id="45f3d-114">影片編解碼器將會嘗試壓縮媒體以符合您的規格。</span><span class="sxs-lookup"><span data-stu-id="45f3d-114">The video codec will try to compress the media to meet your specifications.</span></span> <span data-ttu-id="45f3d-115">如果您的值太低，則產生的壓縮影片將會變得很差。</span><span class="sxs-lookup"><span data-stu-id="45f3d-115">If your values are too low, the resulting compressed video will be very degraded.</span></span>           |
| <span data-ttu-id="45f3d-116">緩衝區視窗</span><span class="sxs-lookup"><span data-stu-id="45f3d-116">Buffer window</span></span>                         | <span data-ttu-id="45f3d-117">呼叫 [**IWMStreamConfig：： SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow) ，將設定為所需的值。</span><span class="sxs-lookup"><span data-stu-id="45f3d-117">Call [**IWMStreamConfig::SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow) to set to the desired value.</span></span> <span data-ttu-id="45f3d-118">影片編解碼器將會嘗試壓縮媒體以符合您的規格。</span><span class="sxs-lookup"><span data-stu-id="45f3d-118">The video codec will try to compress the media to meet your specifications.</span></span> <span data-ttu-id="45f3d-119">如果您的值太低，則產生的壓縮影片將會變得很差。</span><span class="sxs-lookup"><span data-stu-id="45f3d-119">If your values are too low, the resulting compressed video will be very degraded.</span></span> |
| <span data-ttu-id="45f3d-120">**WMVIDEOINFOHEADER.rcSource**</span><span class="sxs-lookup"><span data-stu-id="45f3d-120">**WMVIDEOINFOHEADER.rcSource**</span></span>        | <span data-ttu-id="45f3d-121">左上角必須設定為0、0。</span><span class="sxs-lookup"><span data-stu-id="45f3d-121">The upper left corner must be set to 0,0.</span></span> <span data-ttu-id="45f3d-122">右下角必須設定為框架維度。</span><span class="sxs-lookup"><span data-stu-id="45f3d-122">The lower right corner must be set to the frame dimensions.</span></span> <span data-ttu-id="45f3d-123">例如，在640x480 資料流程中，這些設定會是0、0640480。</span><span class="sxs-lookup"><span data-stu-id="45f3d-123">For example, in a 640x480 stream, these settings would be 0,0,640,480.</span></span>                                                                                                |
| <span data-ttu-id="45f3d-124">**WMVIDEOINFOHEADER.rcTarget**</span><span class="sxs-lookup"><span data-stu-id="45f3d-124">**WMVIDEOINFOHEADER.rcTarget**</span></span>        | <span data-ttu-id="45f3d-125">必須符合 **rcSource**。</span><span class="sxs-lookup"><span data-stu-id="45f3d-125">Must match **rcSource**.</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="45f3d-126">**WMVIDEOINFOHEADER.dwBitRate**</span><span class="sxs-lookup"><span data-stu-id="45f3d-126">**WMVIDEOINFOHEADER.dwBitRate**</span></span>       | <span data-ttu-id="45f3d-127">必須符合為數據流設定的位元速率。</span><span class="sxs-lookup"><span data-stu-id="45f3d-127">Must match the bit rate set for the stream.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="45f3d-128">**WMVIDEOINFOHEADER.AvgTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="45f3d-128">**WMVIDEOINFOHEADER.AvgTimePerFrame**</span></span> | <span data-ttu-id="45f3d-129">設定為每個畫面格的大約時間。</span><span class="sxs-lookup"><span data-stu-id="45f3d-129">Set to the approximate time per frame.</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="45f3d-130">**BITMAPINFOHEADER.biWidth**</span><span class="sxs-lookup"><span data-stu-id="45f3d-130">**BITMAPINFOHEADER.biWidth**</span></span>          | <span data-ttu-id="45f3d-131">設定為所需框架大小的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="45f3d-131">Set to the width, in pixels, of the desired frame size.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="45f3d-132">**BITMAPINFOHEADER.biHeight**</span><span class="sxs-lookup"><span data-stu-id="45f3d-132">**BITMAPINFOHEADER.biHeight**</span></span>         | <span data-ttu-id="45f3d-133">設定為所需框架大小的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="45f3d-133">Set to the height, in pixels, of the desired frame size.</span></span>                                                                                                                                                                                                                    |



 

<span data-ttu-id="45f3d-134">如果影片內容的大小為四個的寬度和高度的倍數，則無法正確播放影片內容。</span><span class="sxs-lookup"><span data-stu-id="45f3d-134">Video content does not play correctly unless it is encoded to a size that is a multiple of four for both width and height.</span></span> <span data-ttu-id="45f3d-135">例外狀況是 [*RGB*](wmformat-glossary.md) 未壓縮影片，可能是任何大小。</span><span class="sxs-lookup"><span data-stu-id="45f3d-135">The exception is [*RGB*](wmformat-glossary.md) uncompressed video, which can be any size.</span></span> <span data-ttu-id="45f3d-136">如果您嘗試設定的大小不是4的倍數，則寫入器會傳回下列其中一個錯誤：</span><span class="sxs-lookup"><span data-stu-id="45f3d-136">If you try to set a size that is not a multiple of four, one of the following errors will be returned by the writer:</span></span>

-   <span data-ttu-id="45f3d-137">NS \_ E \_ 不正確 \_ 輸入 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="45f3d-137">NS\_E\_INVALID\_INPUT\_FORMAT</span></span>
-   <span data-ttu-id="45f3d-138">NS \_ E \_ 不正確 \_ 輸出 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="45f3d-138">NS\_E\_INVALID\_OUTPUT\_FORMAT</span></span>
-   <span data-ttu-id="45f3d-139">NS \_ E \_ INVALIDPROFILE</span><span class="sxs-lookup"><span data-stu-id="45f3d-139">NS\_E\_INVALIDPROFILE</span></span>

<span data-ttu-id="45f3d-140">如果您使用變數位元速率編碼，則可能需要進行其他調整。</span><span class="sxs-lookup"><span data-stu-id="45f3d-140">If you are using variable bit rate encoding, you may need to make other adjustments.</span></span> <span data-ttu-id="45f3d-141">如需詳細資訊，請參閱設定 [VBR 資料流程](configuring-vbr-streams.md)。</span><span class="sxs-lookup"><span data-stu-id="45f3d-141">For more information, see [Configuring VBR Streams](configuring-vbr-streams.md).</span></span>

<span data-ttu-id="45f3d-142">某些 Windows Media 視訊編解碼器支援多個複雜度層級。</span><span class="sxs-lookup"><span data-stu-id="45f3d-142">Some Windows Media Video codecs support multiple complexity levels.</span></span> <span data-ttu-id="45f3d-143">複雜性層級會決定編解碼器在編碼影片資料流程時所要使用的演算法。</span><span class="sxs-lookup"><span data-stu-id="45f3d-143">Complexity levels determine the algorithms that the codec will use when encoding a video stream.</span></span> <span data-ttu-id="45f3d-144">使用高複雜性層級需要更多處理能力才能進行編碼和解碼。</span><span class="sxs-lookup"><span data-stu-id="45f3d-144">Using a high complexity level will require more processing power for encoding and decoding.</span></span>

<span data-ttu-id="45f3d-145">每個支援複雜性設定的編解碼器都會公開下列設定，您可以使用 [**IWMCodecInfo3：： GetCodecProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecprop) 方法來取得這些設定。</span><span class="sxs-lookup"><span data-stu-id="45f3d-145">Each codec that supports complexity settings exposes the following settings that you can retrieve with the [**IWMCodecInfo3::GetCodecProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecprop) method.</span></span>



| <span data-ttu-id="45f3d-146">設定</span><span class="sxs-lookup"><span data-stu-id="45f3d-146">Setting</span></span>                 | <span data-ttu-id="45f3d-147">Description</span><span class="sxs-lookup"><span data-stu-id="45f3d-147">Description</span></span>                                         |
|-------------------------|-----------------------------------------------------|
| <span data-ttu-id="45f3d-148">g \_ wszComplexityMax</span><span class="sxs-lookup"><span data-stu-id="45f3d-148">g\_wszComplexityMax</span></span>     | <span data-ttu-id="45f3d-149">編解碼器支援的最高品質層級。</span><span class="sxs-lookup"><span data-stu-id="45f3d-149">The maximum quality level supported by the codec.</span></span>   |
| <span data-ttu-id="45f3d-150">g \_ wszComplexityOffline</span><span class="sxs-lookup"><span data-stu-id="45f3d-150">g\_wszComplexityOffline</span></span> | <span data-ttu-id="45f3d-151">離線播放的建議品質層級。</span><span class="sxs-lookup"><span data-stu-id="45f3d-151">The suggested quality level for offline playback.</span></span>   |
| <span data-ttu-id="45f3d-152">g \_ wszComplexityLive</span><span class="sxs-lookup"><span data-stu-id="45f3d-152">g\_wszComplexityLive</span></span>    | <span data-ttu-id="45f3d-153">串流播放的建議品質層級。</span><span class="sxs-lookup"><span data-stu-id="45f3d-153">The suggested quality level for streaming playback.</span></span> |



 

<span data-ttu-id="45f3d-154">若要在設定檔中設定影片串流的複雜度，請使用 [**IWMPropertyVault：： SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) 方法，並使用 g \_ wszComplexity 屬性。</span><span class="sxs-lookup"><span data-stu-id="45f3d-154">To set the complexity for a video stream in a profile, use the [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) method using the property g\_wszComplexity.</span></span> <span data-ttu-id="45f3d-155">您設定的值必須小於或等於編解碼器支援的最大複雜度。</span><span class="sxs-lookup"><span data-stu-id="45f3d-155">The value you set must be less than or equal to the maximum supported complexity for the codec.</span></span>

## <a name="related-topics"></a><span data-ttu-id="45f3d-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="45f3d-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45f3d-157">**所有資料流程通用的設定**</span><span class="sxs-lookup"><span data-stu-id="45f3d-157">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="45f3d-158">**設定資料流程**</span><span class="sxs-lookup"><span data-stu-id="45f3d-158">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="45f3d-159">**影片複雜性設定**</span><span class="sxs-lookup"><span data-stu-id="45f3d-159">**Video Complexity Settings**</span></span>](video-complexity-settings.md)
</dt> </dl>

 

 




