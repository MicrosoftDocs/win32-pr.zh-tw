---
description: 影片穩定的 MFT 是在影片串流上執行影像穩定的 Microsoft 媒體基礎轉換 (MFT) 。
ms.assetid: BBC42190-08E4-4C3B-972A-FD30621A6CC1
title: '影片防震 MFT (Camerauicontrol) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65eb64b05e41842b1f7b3ad2e49a6c064be08f0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999505"
---
# <a name="video-stabilization-mft"></a><span data-ttu-id="8a11d-103">影片防震 MFT</span><span class="sxs-lookup"><span data-stu-id="8a11d-103">Video Stabilization MFT</span></span>

<span data-ttu-id="8a11d-104">影片穩定的 MFT 是在影片串流上執行影像穩定的 Microsoft 媒體基礎轉換 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="8a11d-104">The video stabilization MFT is a Microsoft Media Foundation transform (MFT) that performs image stabilization on a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="8a11d-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="8a11d-105">CLSID</span></span>

<span data-ttu-id="8a11d-106">CLSID \_ CMSVideoDSPMFT</span><span class="sxs-lookup"><span data-stu-id="8a11d-106">CLSID\_CMSVideoDSPMFT</span></span>

## <a name="interfaces"></a><span data-ttu-id="8a11d-107">介面</span><span class="sxs-lookup"><span data-stu-id="8a11d-107">Interfaces</span></span>

-   [<span data-ttu-id="8a11d-108">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="8a11d-108">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="8a11d-109">**IMFAttributes**</span><span class="sxs-lookup"><span data-stu-id="8a11d-109">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [<span data-ttu-id="8a11d-110">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="8a11d-110">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="8a11d-111">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="8a11d-111">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="8a11d-112">**IMediaExtension**</span><span class="sxs-lookup"><span data-stu-id="8a11d-112">**IMediaExtension**</span></span>](/uwp/api/Windows.Media.IMediaExtension?view=winrt-19041)

## <a name="input-formats"></a><span data-ttu-id="8a11d-113">輸入格式</span><span class="sxs-lookup"><span data-stu-id="8a11d-113">Input Formats</span></span>

<span data-ttu-id="8a11d-114">影片穩定 MFT 針對未壓縮影片所接受的輸入媒體類型和子類型組合如下：</span><span class="sxs-lookup"><span data-stu-id="8a11d-114">The input media type and sub-type combinations accepted by the video stabilization MFT for uncompressed video are:</span></span>

-   <span data-ttu-id="8a11d-115">**媒體 \_ 媒體**</span><span class="sxs-lookup"><span data-stu-id="8a11d-115">**MEDIATYPE\_VIDEO**</span></span>
-   <span data-ttu-id="8a11d-116">**MEDIASUBTYPE \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="8a11d-116">**MEDIASUBTYPE\_NV12**</span></span>
-   <span data-ttu-id="8a11d-117">**MEDIASUBTYPE \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="8a11d-117">**MEDIASUBTYPE\_YUY2**</span></span>

## <a name="output-formats"></a><span data-ttu-id="8a11d-118">輸出格式</span><span class="sxs-lookup"><span data-stu-id="8a11d-118">Output Formats</span></span>

<span data-ttu-id="8a11d-119">影片穩定 MFT 接受的輸出媒體類型和子類型組合如下：</span><span class="sxs-lookup"><span data-stu-id="8a11d-119">The output media type and sub-type combinations accepted by the video stabilization MFT are:</span></span>

-   <span data-ttu-id="8a11d-120">**媒體 \_ 媒體**</span><span class="sxs-lookup"><span data-stu-id="8a11d-120">**MEDIATYPE\_VIDEO**</span></span>
-   <span data-ttu-id="8a11d-121">**MEDIASUBTYPE \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="8a11d-121">**MEDIASUBTYPE\_NV12**</span></span>

<span data-ttu-id="8a11d-122">輸入媒體類型必須在輸出媒體類型之前設定。</span><span class="sxs-lookup"><span data-stu-id="8a11d-122">The input media type must be set before the output media type.</span></span> <span data-ttu-id="8a11d-123">在大多數情況下，有限的格式支援不會造成問題，因為管線會自動插入必要的色彩轉換。</span><span class="sxs-lookup"><span data-stu-id="8a11d-123">In most situations, the limited format support is not an issue because the pipeline automatically inserts the necessary color conversions.</span></span>

<span data-ttu-id="8a11d-124">影片穩定的 MFT 元件能夠在輸入變更時進行動態格式變更。</span><span class="sxs-lookup"><span data-stu-id="8a11d-124">The video stabilization MFT component is capable of dynamic format change when input changes.</span></span> <span data-ttu-id="8a11d-125">當輸入圖片大小變更或子類型變更時，它會觸發輸出資料流程的動態格式變更。</span><span class="sxs-lookup"><span data-stu-id="8a11d-125">When the input picture size changes or the subtype changes, it will trigger a dynamic format change on the output stream.</span></span>

<span data-ttu-id="8a11d-126">影片穩定的 MFT 在下列情況下將會進行色彩轉換：</span><span class="sxs-lookup"><span data-stu-id="8a11d-126">The video stabilization MFT will do color conversion in the following cases:</span></span>

-   <span data-ttu-id="8a11d-127">當輸入格式為 **MEDIASUBTYPE \_ YUY2** 時。</span><span class="sxs-lookup"><span data-stu-id="8a11d-127">When the input format is **MEDIASUBTYPE\_YUY2**.</span></span>
-   <span data-ttu-id="8a11d-128">使用 Microsoft DirectX 9.0 相容性模式時。</span><span class="sxs-lookup"><span data-stu-id="8a11d-128">When Microsoft DirectX 9.0 compatibility mode is used.</span></span>

### <a name="attributes"></a><span data-ttu-id="8a11d-129">屬性</span><span class="sxs-lookup"><span data-stu-id="8a11d-129">Attributes</span></span>

<span data-ttu-id="8a11d-130">影片穩定 MFT 透過 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="8a11d-130">The following attributes are supported by the video stabilization MFT through the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

-   <span data-ttu-id="8a11d-131">屬性 [MF \_ VIDEODSP \_ 模式](mf-videodsp-mode.md) 會將影片穩定的 MFT 置於穩定模式或通過模式。</span><span class="sxs-lookup"><span data-stu-id="8a11d-131">The attribute [MF\_VIDEODSP\_MODE](mf-videodsp-mode.md) puts the video stabilization MFT into either stabilization mode or pass-through mode.</span></span> <span data-ttu-id="8a11d-132">應用程式應該針對 GUID **MF \_ VIDEODSP \_ 類型** 呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) ，並使用對應到下列其中一個有效值的整數： **MFVideoDSPMode \_ 穩定化**= 4， **MFVideoDSPMode \_ 傳遞**= 1。</span><span class="sxs-lookup"><span data-stu-id="8a11d-132">The application should call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) on the GUID **MF\_VIDEODSP\_TYPE** with an integer corresponding to one of the following valid values: **MFVideoDSPMode\_Stabilization** = 4, **MFVideoDSPMode\_Passthrough** = 1.</span></span> <span data-ttu-id="8a11d-133">您 \_ \_ 可以在播放期間隨時變更 MF VIDEODSP 模式。</span><span class="sxs-lookup"><span data-stu-id="8a11d-133">MF\_VIDEODSP\_MODE can be changed at any time during playback.</span></span> <span data-ttu-id="8a11d-134">這會導致動態模式變更。</span><span class="sxs-lookup"><span data-stu-id="8a11d-134">This causes a dynamic mode change.</span></span> <span data-ttu-id="8a11d-135">輸出會切換至穩定或在16或2個框架之後傳遞 (，視延遲模式在屬性變更之後) 而定。</span><span class="sxs-lookup"><span data-stu-id="8a11d-135">The output will switch to either stabilized or pass through after either 16 or 2 frames (depending on the latency mode) after the attribute is changed.</span></span>
-   <span data-ttu-id="8a11d-136">[ [MF \_ 低 \_ 延遲](mf-low-latency.md) ] 屬性可將影片穩定的 MFT 置於低延遲模式或高品質模式。</span><span class="sxs-lookup"><span data-stu-id="8a11d-136">The attribute [MF\_LOW\_LATENCY](mf-low-latency.md) puts the video stabilization MFT into either low latency mode or high quality mode.</span></span> <span data-ttu-id="8a11d-137">應用程式應該針對 GUID **MF \_ 低 \_ 延遲**，以對應到下列其中一個有效值的整數來呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) ：低延遲 = 1 高品質 = 0</span><span class="sxs-lookup"><span data-stu-id="8a11d-137">The application should call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) on the GUID **MF\_LOW\_LATENCY** with an integer corresponding to one of the following valid values: Low latency = 1 High Quality = 0</span></span>
-   <span data-ttu-id="8a11d-138">管線使用屬性 [MF \_ SA \_ D3D11 \_ BINDFLAGS](mf-sa-d3d11-bindflags.md) 來指定 D3D11 系結旗標，以使用建立輸出範例。</span><span class="sxs-lookup"><span data-stu-id="8a11d-138">The attribute [MF\_SA\_D3D11\_BINDFLAGS](mf-sa-d3d11-bindflags.md) is used by the pipeline to specify the D3D11 bind flags to create the output samples with.</span></span> <span data-ttu-id="8a11d-139">D3D11 系結 [**\_ \_ 旗**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) 標列舉中值的任何組合都是有效的。</span><span class="sxs-lookup"><span data-stu-id="8a11d-139">Any combination of values from the [**D3D11\_BIND\_FLAG**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) enumeration is valid.</span></span>
-   <span data-ttu-id="8a11d-140">管線會使用屬性 **MF \_ SA 的 \_ 最小 \_ 輸出 \_ 範例 \_ 計數** ，來指定此元件在輸出時必須支援的樣本數目下限。</span><span class="sxs-lookup"><span data-stu-id="8a11d-140">The attribute **MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT** is used by the pipeline to specify the minimum number of samples that this component must support on output.</span></span>
-   <span data-ttu-id="8a11d-141">每個由穩定產生的範例都會設定屬性 [MFSampleExtension \_ VideoDSPMode](mfsampleextension-videodspmode.md) ，以指出套用至該範例的有效 [MF \_ VIDEODSP \_ 模式](mf-videodsp-mode.md) ， (範例是否穩定) 。</span><span class="sxs-lookup"><span data-stu-id="8a11d-141">The attribute [MFSampleExtension\_VideoDSPMode](mfsampleextension-videodspmode.md) is set on every sample produced by stabilization to indicate the effective [MF\_VIDEODSP\_MODE](mf-videodsp-mode.md) applied to that sample (whether or not the sample was stabilized).</span></span> <span data-ttu-id="8a11d-142">在某些情況下， (可能因為系統負載過高或使用者) 的要求，而無法穩定。</span><span class="sxs-lookup"><span data-stu-id="8a11d-142">Under certain conditions, samples may not be stabilized (due to high system load, or requests by the user).</span></span> <span data-ttu-id="8a11d-143">這個屬性的值與 MF \_ VIDEODSP 模式屬性的值相同 \_ (**MFVideoDSPMode \_ 穩定** 和 **MFVideoDSPMode \_ 傳遞**) 。</span><span class="sxs-lookup"><span data-stu-id="8a11d-143">This attribute has the same values as the MF\_VIDEODSP\_MODE attribute (**MFVideoDSPMode\_Stabilization** and **MFVideoDSPMode\_Passthrough**).</span></span> <span data-ttu-id="8a11d-144">若要取得這個屬性的值，應用程式應該在 GUID **MFSampleExtension \_ VideoDSPMode** 上呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) 。</span><span class="sxs-lookup"><span data-stu-id="8a11d-144">To get the value of this attribute applications should call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) on GUID **MFSampleExtension\_VideoDSPMode**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a11d-145">備註</span><span class="sxs-lookup"><span data-stu-id="8a11d-145">Remarks</span></span>

<span data-ttu-id="8a11d-146">您可以使用下列其中一種方式來建立影片穩定 DSP 的實例：</span><span class="sxs-lookup"><span data-stu-id="8a11d-146">An instance of the video stabilization DSP can be created in one of the following ways:</span></span>

-   <span data-ttu-id="8a11d-147">藉由呼叫 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)。</span><span class="sxs-lookup"><span data-stu-id="8a11d-147">By calling [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span> <span data-ttu-id="8a11d-148">影片穩定的 DSP 會在 [ **MFT \_ 類別] \_ 影片 \_ 效果** 類別下註冊。</span><span class="sxs-lookup"><span data-stu-id="8a11d-148">The video stabilization DSP is registered under the **MFT\_CATEGORY\_VIDEO\_EFFECT** category.</span></span>
-   <span data-ttu-id="8a11d-149">藉由呼叫 COM 函式， **CoCreateInstance** 將 clsid **clsid \_ CMSVideoDSPMFT** 傳遞給它。</span><span class="sxs-lookup"><span data-stu-id="8a11d-149">By calling the COM function **CoCreateInstance** passing it the CLSID **CLSID\_CMSVideoDSPMFT**.</span></span> <span data-ttu-id="8a11d-150">若要使用這個方法，您必須包含 wmcodecdsp 和 wmcodecdspuuid 的連結。</span><span class="sxs-lookup"><span data-stu-id="8a11d-150">To use this method, you must include wmcodecdsp.h and link against wmcodecdspuuid.lib.</span></span>

<span data-ttu-id="8a11d-151">此外，video 穩定的 DSP 支援使用 Windows 執行階段作為 Windows Media 擴充功能來進行具現化。</span><span class="sxs-lookup"><span data-stu-id="8a11d-151">Additionally, the video stabilization DSP supports instantiation using Windows Runtime as a Windows Media Extension.</span></span> <span data-ttu-id="8a11d-152">它是在 [**VideoEffects**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041)上定義，其完整名稱是 "VideoEffects. VideoStabilization"。</span><span class="sxs-lookup"><span data-stu-id="8a11d-152">It is defined on the [**Windows.Media.VideoEffects**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041), and its full name is "Windows.Media.VideoEffects.VideoStabilization".</span></span>

## <a name="requirements"></a><span data-ttu-id="8a11d-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a11d-153">Requirements</span></span>



| <span data-ttu-id="8a11d-154">需求</span><span class="sxs-lookup"><span data-stu-id="8a11d-154">Requirement</span></span> | <span data-ttu-id="8a11d-155">值</span><span class="sxs-lookup"><span data-stu-id="8a11d-155">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a11d-156">標頭</span><span class="sxs-lookup"><span data-stu-id="8a11d-156">Header</span></span><br/> | <dl> <span data-ttu-id="8a11d-157"><dt>Camerauicontrol。h</dt></span><span class="sxs-lookup"><span data-stu-id="8a11d-157"><dt>Camerauicontrol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a11d-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a11d-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a11d-159">數位訊號處理器</span><span class="sxs-lookup"><span data-stu-id="8a11d-159">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> <dt>

[<span data-ttu-id="8a11d-160">**Windows.Media.VideoEffects**</span><span class="sxs-lookup"><span data-stu-id="8a11d-160">**Windows.Media.VideoEffects**</span></span>](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041)
</dt> </dl>

 

 
