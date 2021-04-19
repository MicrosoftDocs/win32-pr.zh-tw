---
description: 本文包含使用 Direct3D 11 或 12 video Api 來解碼影片時產生長條圖的指引。
ms.assetid: ''
title: Direct3D video 解碼長條圖
ms.topic: article
ms.date: 08/19/2019
ms.openlocfilehash: 6e25abd39ba95b669c2d76ced5f825ea80c4e3c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999841"
---
# <a name="direct3d-video-decode-histograms"></a><span data-ttu-id="d67f3-103">Direct3D video 解碼長條圖</span><span class="sxs-lookup"><span data-stu-id="d67f3-103">Direct3D video decode histograms</span></span>

<span data-ttu-id="d67f3-104">本文包含使用 Direct3D 11 或 12 video Api 來解碼影片時產生長條圖的指引。</span><span class="sxs-lookup"><span data-stu-id="d67f3-104">This article contains guidance for generating histograms while decoding video using Direct3D 11 or 12 video APIs.</span></span>

## <a name="checking-the-video-device-for-histogram-capabilities"></a><span data-ttu-id="d67f3-105">檢查影片裝置的長條圖功能</span><span class="sxs-lookup"><span data-stu-id="d67f3-105">Checking the video device for histogram capabilities</span></span>

<span data-ttu-id="d67f3-106">嘗試產生長條圖之前，您必須先檢查目前的影片裝置是否支援影片解碼長條圖功能。</span><span class="sxs-lookup"><span data-stu-id="d67f3-106">Before attempting to generated histograms, you must check to see if the current video device supports the video decode histogram feature.</span></span>

### <a name="direct3d-12"></a><span data-ttu-id="d67f3-107">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="d67f3-107">Direct3D 12</span></span>

<span data-ttu-id="d67f3-108">呼叫 [ID3D12VideoDevice：： CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) ，以檢查 Direct3D 12 影片解碼作業的支援詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d67f3-108">Call [ID3D12VideoDevice::CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) to check for the support details for Direct3D 12 video decoding operations.</span></span> <span data-ttu-id="d67f3-109">從 [D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video)列舉傳遞 **D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM** 值，以指定您要求支援影片解碼長條圖。</span><span class="sxs-lookup"><span data-stu-id="d67f3-109">Pass the **D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM** value from the [D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) enumeration to specify that you are requesting support for video decode histograms.</span></span>

### <a name="direct3d-11"></a><span data-ttu-id="d67f3-110">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="d67f3-110">Direct3D 11</span></span>

<span data-ttu-id="d67f3-111">呼叫 [ID3D11VideoDevice2：： CheckFeatureSupport](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videodevice2-checkfeaturesupport) ，並傳入 [D3D11_FEATURE_VIDEO](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_feature_video)的 **D3D11_FEATURE_VIDEO_DECODER_HISTOGRAM** 值，以判斷目前裝置是否支援長條圖。</span><span class="sxs-lookup"><span data-stu-id="d67f3-111">Call [ID3D11VideoDevice2::CheckFeatureSupport](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videodevice2-checkfeaturesupport) and pass in the **D3D11_FEATURE_VIDEO_DECODER_HISTOGRAM** value of the [D3D11_FEATURE_VIDEO](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_feature_video) to determine if histograms are supported for the current device.</span></span>

## <a name="enabling-histogram-during-decode"></a><span data-ttu-id="d67f3-112">在解碼期間啟用長條圖</span><span class="sxs-lookup"><span data-stu-id="d67f3-112">Enabling histogram during decode</span></span>

<span data-ttu-id="d67f3-113">提供長條圖資料儲存所在之緩衝區的呼叫端會啟用長條圖資料的集合。</span><span class="sxs-lookup"><span data-stu-id="d67f3-113">The collection of histogram data is enabled by the caller providing the buffers in which the histogram data is stored.</span></span>  <span data-ttu-id="d67f3-114">指定元件的 null 長條圖輸出緩衝區表示長條圖集合已停用。</span><span class="sxs-lookup"><span data-stu-id="d67f3-114">A null histogram output buffer for a given component indicates that histogram collection is disabled.</span></span>

### <a name="direct3d-12"></a><span data-ttu-id="d67f3-115">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="d67f3-115">Direct3D 12</span></span>

<span data-ttu-id="d67f3-116">為了提供輸出緩衝區以使用 Direct3D 12 接收長條圖資料，您應該使用 [ID3D12VideoDecodeCommandList1：:D ecodeframe1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist1-decodeframe1) 方法來建立解碼命令清單。</span><span class="sxs-lookup"><span data-stu-id="d67f3-116">In order to provide output buffers to receive histogram data using Direct3D 12, you should create your decode command list using the [ID3D12VideoDecodeCommandList1::DecodeFrame1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist1-decodeframe1) method.</span></span> <span data-ttu-id="d67f3-117">這個方法會採用 [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments1) 結構作為引數。</span><span class="sxs-lookup"><span data-stu-id="d67f3-117">This method takes a [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments1) structure as an argument.</span></span> <span data-ttu-id="d67f3-118">**D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1** 具有 [D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_histogram)類型的欄位，可讓您指定要輸出長條圖資料的 [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) 。</span><span class="sxs-lookup"><span data-stu-id="d67f3-118">**D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1** has a field of type [D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_histogram), which allows you to specify an [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) into which histogram data is output.</span></span>

### <a name="direct3d-11"></a><span data-ttu-id="d67f3-119">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="d67f3-119">Direct3D 11</span></span>

<span data-ttu-id="d67f3-120">[ID3D11VideoCoNtext3](/windows/win32/api/d3d11_4/nn-d3d11_4-id3d11videocontext3)介面提供[DecoderBeginFrame1](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videocontext3-decoderbeginframe1)方法，可讓您提供一或多個[ID3D11Buffer](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer)介面，以將長條圖資料輸出至其中。</span><span class="sxs-lookup"><span data-stu-id="d67f3-120">The [ID3D11VideoContext3](/windows/win32/api/d3d11_4/nn-d3d11_4-id3d11videocontext3) interface provides the [DecoderBeginFrame1](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videocontext3-decoderbeginframe1) method, which allows you to provide one or more [ID3D11Buffer](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer) interfaces into which the histogram data will be output.</span></span> <span data-ttu-id="d67f3-121">[D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_video_decoder_histogram_component)指定要產生長條圖資料的元件。</span><span class="sxs-lookup"><span data-stu-id="d67f3-121">The [D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_video_decoder_histogram_component) to specify the components for which you want histogram data to be generated.</span></span>


## <a name="buffer-format"></a><span data-ttu-id="d67f3-122">緩衝區格式</span><span class="sxs-lookup"><span data-stu-id="d67f3-122">Buffer format</span></span>

<span data-ttu-id="d67f3-123">解碼長條圖輸出會寫入緩衝區，作為每個元件的整數計數器。</span><span class="sxs-lookup"><span data-stu-id="d67f3-123">The decode histogram output is written to a buffer as an integer counter per component.</span></span>  <span data-ttu-id="d67f3-124">緩衝區格式為每個 bin 32 位的值。</span><span class="sxs-lookup"><span data-stu-id="d67f3-124">The buffer format is a 32-bit value per bin.</span></span>  <span data-ttu-id="d67f3-125">裝置可使用小於32位的整數計數器位深度，但必須是16、24或32位。</span><span class="sxs-lookup"><span data-stu-id="d67f3-125">A device may use an integer counter bit depth that is smaller than 32 bits, but must be 16, 24, or 32 bits.</span></span>  <span data-ttu-id="d67f3-126">如果是，計數器值會儲存在較低的位，而未使用的位則為零。</span><span class="sxs-lookup"><span data-stu-id="d67f3-126">If so, the counter value is stored in the lower bits and the upper unused bits are zero.</span></span>  <span data-ttu-id="d67f3-127">當 bin 的計數超過最大值時，裝置會改為設定最大值。</span><span class="sxs-lookup"><span data-stu-id="d67f3-127">When the count for a bin would exceed the max value, the device sets the max value instead.</span></span> <span data-ttu-id="d67f3-128">裝置會報告支援的 bin 數目，其值必須是2的乘冪。</span><span class="sxs-lookup"><span data-stu-id="d67f3-128">Devices report the number of bins supported, which must be a value that is a power of 2.</span></span>  <span data-ttu-id="d67f3-129">支援這項功能的裝置所需的最少 bin 數目是64。</span><span class="sxs-lookup"><span data-stu-id="d67f3-129">The minimum number of bins required for devices that support this feature is 64.</span></span> 

<span data-ttu-id="d67f3-130">您必須提供具有256位元組對齊位移的緩衝區，以及支援的 bin 數目乘以 (4 個位元組) 為每個所要求元件所要求的大小。</span><span class="sxs-lookup"><span data-stu-id="d67f3-130">You must supply a buffer with a 256-byte aligned offset and a size that is the supported number of bins multiplied by the bin size (4 bytes) for each component requested.</span></span>  <span data-ttu-id="d67f3-131">Bin 放置是由下列各項所決定：</span><span class="sxs-lookup"><span data-stu-id="d67f3-131">Bin placement is determined by:</span></span>

`binIndex = floor(value / [max value of channel + 1] * (countBins))`


<span data-ttu-id="d67f3-132">當格式定義的元件的有用位小於儲存區的數目時 (例如，P010 會使用16位元件儲存體) 的前10位，只會將 (P010 視為10位值) 。</span><span class="sxs-lookup"><span data-stu-id="d67f3-132">When a format defines the useful bits of a component as less than the number of storage bits (for example, P010 uses the top 10 bits of 16 bits of component storage), only the useful bits are considered (P010 is treated as a 10 bit value).</span></span> 

<span data-ttu-id="d67f3-133">影片裝置會報告支援哪些元件。</span><span class="sxs-lookup"><span data-stu-id="d67f3-133">The video device reports which components are supported.</span></span>  <span data-ttu-id="d67f3-134">如果呼叫端不需要指定元件的長條圖，則會指定 nullptr。</span><span class="sxs-lookup"><span data-stu-id="d67f3-134">If the caller does not want a histogram for a given component, they specify nullptr.</span></span>  <span data-ttu-id="d67f3-135">如果驅動程式不支援指定元件的長條圖，該元件的長條圖緩衝區必須是 nullptr。</span><span class="sxs-lookup"><span data-stu-id="d67f3-135">If the driver does not support a histogram for a given component, that component's histogram buffer must be nullptr.</span></span>

<span data-ttu-id="d67f3-136">當支援多個元件時，應用程式可能會要求每個畫面格解碼的元件組合。</span><span class="sxs-lookup"><span data-stu-id="d67f3-136">When multiple components are supported, the application may request any combination of components per frame decode.</span></span>  <span data-ttu-id="d67f3-137">例如，如果硬體報表支援 Y、U 和 V 元件，則應用程式可能只會要求框架1的 Y 長條圖、第二個畫面格2的 U 長條圖，以及僅針對框架3的 V 長條圖。</span><span class="sxs-lookup"><span data-stu-id="d67f3-137">For example,if the hardware reports support for Y, U, and V components, the application may request the Y histogram only for frame one, the U histogram only for frame two, and the V histogram only for frame 3.</span></span>  <span data-ttu-id="d67f3-138">它們也可能會要求兩個元件的任意組合，或三個元件的組合。</span><span class="sxs-lookup"><span data-stu-id="d67f3-138">They may also request any combination of two components or all three components.</span></span>

<span data-ttu-id="d67f3-139">應用程式會為每個要求的元件提供個別的位移和緩衝區指標/控制碼。</span><span class="sxs-lookup"><span data-stu-id="d67f3-139">Applications supply a separate offset and buffer pointer/handle for each component requested.</span></span>  <span data-ttu-id="d67f3-140">此指標可能會指向與另一個元件或個別資源相同的資源。</span><span class="sxs-lookup"><span data-stu-id="d67f3-140">This pointer may point to the same resource as another component or a separate resource.</span></span>  <span data-ttu-id="d67f3-141">位移可將多個元件放在相同的緩衝區中，但是位移和長條圖大小所指定的輸出區域不得與另一個長條圖元件輸出重迭。</span><span class="sxs-lookup"><span data-stu-id="d67f3-141">The offset allows placing multiple components in the same buffer, but the output region specified by the offset and the histogram size must not overlap another histogram component output.</span></span>  <span data-ttu-id="d67f3-142">長條圖也可以寫入與其他不相關的內容相同的緩衝區，例如在資源子配置策略中使用時。</span><span class="sxs-lookup"><span data-stu-id="d67f3-142">The histogram may also be written to the same buffer as other unrelated content such as when being used in a resource sub-allocation strategy.</span></span>


<span data-ttu-id="d67f3-143">D3D 執行時間會驗證呼叫端只針對支援的元件啟用長條圖、調整緩衝區位移的對齊，而且緩衝區大小足以滿足所報告的 bin 數量。</span><span class="sxs-lookup"><span data-stu-id="d67f3-143">The D3D runtime validates that callers only enable histogram for supported components, that the buffer offset is aligned, and that buffer size is sufficient for the reported number of bins.</span></span>


## <a name="protected-content"></a><span data-ttu-id="d67f3-144">受保護內容</span><span class="sxs-lookup"><span data-stu-id="d67f3-144">Protected content</span></span>

<span data-ttu-id="d67f3-145">長條圖緩衝區必須與解碼輸出介面具有相同的介面保護。</span><span class="sxs-lookup"><span data-stu-id="d67f3-145">The Histogram buffers are required to have the same surface protection as the decode output surface.</span></span> <span data-ttu-id="d67f3-146">如果解碼輸出介面不是受保護的資源，則長條圖緩衝區必須不是受保護的資源。</span><span class="sxs-lookup"><span data-stu-id="d67f3-146">If the decode output surface is not a protected resource, the histogram buffer must not be a protected resource.</span></span> <span data-ttu-id="d67f3-147">如果解碼輸出介面是受保護的資源，則長條圖必須是受保護的資源。</span><span class="sxs-lookup"><span data-stu-id="d67f3-147">If the decode output surface is protected resource, the histogram must be a protected resource.</span></span>








## <a name="related-topics"></a><span data-ttu-id="d67f3-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="d67f3-148">Related topics</span></span>

<dl> <span data-ttu-id="d67f3-149"><dt>
[Direct3D 12 影片 api](direct3d-12-video-apis.md) 
[媒體基礎程式設計指南](media-foundation-programming-guide.md)
</dt> </span><span class="sxs-lookup"><span data-stu-id="d67f3-149"><dt>
[Direct3D 12 Video APIs](direct3d-12-video-apis.md)
[Media Foundation Programming Guide](media-foundation-programming-guide.md)
</dt> </span></span></dl>

 

 




