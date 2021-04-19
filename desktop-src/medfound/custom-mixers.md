---
description: 自訂 Mixers
ms.assetid: a0af318d-9ac2-43f9-8934-f28c472256a6
title: 自訂 Mixers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac7e56c578a7081de7c71ae3abaf9fc45d085827
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999842"
---
# <a name="custom-mixers"></a><span data-ttu-id="a916f-103">自訂 Mixers</span><span class="sxs-lookup"><span data-stu-id="a916f-103">Custom Mixers</span></span>

<span data-ttu-id="a916f-104">本主題說明如何撰寫增強型影片轉譯器的自訂混音器 (EVR) 。</span><span class="sxs-lookup"><span data-stu-id="a916f-104">This topic describes how to write a custom mixer for the enhanced video renderer (EVR).</span></span> <span data-ttu-id="a916f-105">您可以使用自訂混音器搭配媒體基礎 EVR 媒體接收器或 DirectShow EVR 篩選器。</span><span class="sxs-lookup"><span data-stu-id="a916f-105">You can use a custom mixer with either the Media Foundation EVR media sink, or the DirectShow EVR filter.</span></span> <span data-ttu-id="a916f-106">如需 mixers 和展示者的詳細資訊，請參閱 [增強型影片](enhanced-video-renderer.md)轉譯器。</span><span class="sxs-lookup"><span data-stu-id="a916f-106">For more information about mixers and presenters, see [Enhanced Video Renderer](enhanced-video-renderer.md).</span></span>

<span data-ttu-id="a916f-107">混音器是一種媒體基礎轉換 (MFT) ，其中包含一或多個輸入 (參考資料流以及子串流) 和一個輸出。</span><span class="sxs-lookup"><span data-stu-id="a916f-107">The mixer is a Media Foundation transform (MFT) with one or more inputs (the reference stream plus the substreams) and one output.</span></span> <span data-ttu-id="a916f-108">輸入資料流程從上游接收樣本。</span><span class="sxs-lookup"><span data-stu-id="a916f-108">The input stream receives samples from upstream.</span></span> <span data-ttu-id="a916f-109">輸出資料流程會將範例提供給展示者。</span><span class="sxs-lookup"><span data-stu-id="a916f-109">The output stream delivers samples to the presenter.</span></span> <span data-ttu-id="a916f-110">EVR 負責呼叫混音器上的 [**IMFTransform：:P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) ，而展示者負責呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)。</span><span class="sxs-lookup"><span data-stu-id="a916f-110">The EVR is responsible for calling [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) on the mixer, and the presenter is responsible for calling [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span></span>

<span data-ttu-id="a916f-111">EVR 混音器至少必須執行下列介面：</span><span class="sxs-lookup"><span data-stu-id="a916f-111">At a minimum, an EVR mixer must implement the following interfaces:</span></span>



| <span data-ttu-id="a916f-112">介面</span><span class="sxs-lookup"><span data-stu-id="a916f-112">Interface</span></span>                                                                | <span data-ttu-id="a916f-113">描述</span><span class="sxs-lookup"><span data-stu-id="a916f-113">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a916f-114">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="a916f-114">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                                     | <span data-ttu-id="a916f-115">提供基底 MFT 功能。</span><span class="sxs-lookup"><span data-stu-id="a916f-115">Provides base MFT functionality.</span></span>                                                                 |
| [<span data-ttu-id="a916f-116">**IMFTopologyServiceLookupClient**</span><span class="sxs-lookup"><span data-stu-id="a916f-116">**IMFTopologyServiceLookupClient**</span></span>](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | <span data-ttu-id="a916f-117">讓混音器從 EVR 取得介面。</span><span class="sxs-lookup"><span data-stu-id="a916f-117">Enables the mixer to get interfaces from the EVR.</span></span>                                                |
| [<span data-ttu-id="a916f-118">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="a916f-118">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | <span data-ttu-id="a916f-119">讓混音器從 EVR 取得介面。</span><span class="sxs-lookup"><span data-stu-id="a916f-119">Enables the mixer to get interfaces from the EVR.</span></span>                                                |
| [<span data-ttu-id="a916f-120">**IMFAttributes**</span><span class="sxs-lookup"><span data-stu-id="a916f-120">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)                                   | <span data-ttu-id="a916f-121">用來將 [**MF \_ SA \_ D3D \_ 感知**](mf-sa-d3d-aware-attribute.md) 屬性公開給 EVR。</span><span class="sxs-lookup"><span data-stu-id="a916f-121">Used to expose the [**MF\_SA\_D3D\_AWARE**](mf-sa-d3d-aware-attribute.md) attribute to the EVR.</span></span> |



 

<span data-ttu-id="a916f-122">（選擇性） MFT 可以執行下列任何介面：</span><span class="sxs-lookup"><span data-stu-id="a916f-122">Optionally, an MFT can implement any of the following interfaces:</span></span>



| <span data-ttu-id="a916f-123">介面</span><span class="sxs-lookup"><span data-stu-id="a916f-123">Interface</span></span>                                                | <span data-ttu-id="a916f-124">描述</span><span class="sxs-lookup"><span data-stu-id="a916f-124">Description</span></span>                                                                                                                                          |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a916f-125">**IEVRTrustedVideoPlugin**</span><span class="sxs-lookup"><span data-stu-id="a916f-125">**IEVRTrustedVideoPlugin**</span></span>](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | <span data-ttu-id="a916f-126">播放受保護的內容時需要。</span><span class="sxs-lookup"><span data-stu-id="a916f-126">Required to play protected content.</span></span>                                                                                                                  |
| [<span data-ttu-id="a916f-127">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="a916f-127">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                   | <span data-ttu-id="a916f-128">將介面（例如 [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap) 和 [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor) ）公開給應用程式。</span><span class="sxs-lookup"><span data-stu-id="a916f-128">Exposes interfaces such as [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap) and [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor) to the application.</span></span> |
| [<span data-ttu-id="a916f-129">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="a916f-129">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)             | <span data-ttu-id="a916f-130">可讓品質管制員調整影片品質。</span><span class="sxs-lookup"><span data-stu-id="a916f-130">Enables the quality manager to adjust the video quality.</span></span>                                                                                             |
| [<span data-ttu-id="a916f-131">**IMFVideoMixerBitmap**</span><span class="sxs-lookup"><span data-stu-id="a916f-131">**IMFVideoMixerBitmap**</span></span>](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)       | <span data-ttu-id="a916f-132">讓應用程式將靜態點陣圖混合到影片上。</span><span class="sxs-lookup"><span data-stu-id="a916f-132">Enables the application to mix a static bitmap onto the video.</span></span>                                                                                       |
| [<span data-ttu-id="a916f-133">**IMFVideoPositionMapper**</span><span class="sxs-lookup"><span data-stu-id="a916f-133">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | <span data-ttu-id="a916f-134">將輸出影片畫面上的座標組應到輸入影片畫面上的座標。</span><span class="sxs-lookup"><span data-stu-id="a916f-134">Maps coordinates on the output video frame to coordinates on the input video frame.</span></span>                                                                  |
| [<span data-ttu-id="a916f-135">**IMFVideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="a916f-135">**IMFVideoProcessor**</span></span>](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)           | <span data-ttu-id="a916f-136">將部分 DXVA 的影片處理功能公開給應用程式。</span><span class="sxs-lookup"><span data-stu-id="a916f-136">Exposes some DXVA video processing features to the application.</span></span>                                                                                      |



 

<span data-ttu-id="a916f-137">使用混音器的格式協調運作方式如下：</span><span class="sxs-lookup"><span data-stu-id="a916f-137">Format negotiation with the mixer works as follows:</span></span>

1.  <span data-ttu-id="a916f-138">EVR 會設定參考資料流上的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="a916f-138">The EVR sets the media type on the reference stream.</span></span>
2.  <span data-ttu-id="a916f-139">EVR 會使用 **MFVP \_ MESSAGE \_ INVALIDATEMEDIATYPE** 訊息來呼叫展示者上的 [**IMFVideoPresenter：:P rocessmessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) 。</span><span class="sxs-lookup"><span data-stu-id="a916f-139">The EVR calls [**IMFVideoPresenter::ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) on the presenter with the **MFVP\_MESSAGE\_INVALIDATEMEDIATYPE** message.</span></span>

3.  <span data-ttu-id="a916f-140">展示者會設定混音器輸出資料流程上的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="a916f-140">The presenter sets the media type on the mixer's output stream.</span></span>
4.  <span data-ttu-id="a916f-141">EVR 會設定子串流上的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="a916f-141">The EVR sets the media type on the substreams.</span></span>

<span data-ttu-id="a916f-142">如果參考資料流上的媒體類型變更，則混音器的其他媒體類型將不再有效。</span><span class="sxs-lookup"><span data-stu-id="a916f-142">If the media type on the reference stream changes, the mixer's other media types are no longer valid.</span></span> <span data-ttu-id="a916f-143">混音器的 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 方法將會失敗，並傳回 **MF \_ E \_ 轉換 \_ 資料流程 \_ 變更**。</span><span class="sxs-lookup"><span data-stu-id="a916f-143">The mixer's [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method will then fail and return **MF\_E\_TRANSFORM\_STREAM\_CHANGE**.</span></span> <span data-ttu-id="a916f-144">目前，展示者不應該在此時進行任何動作。</span><span class="sxs-lookup"><span data-stu-id="a916f-144">The presenter should not do anything at this point.</span></span> <span data-ttu-id="a916f-145">EVR 會再次起始格式的協商處理。</span><span class="sxs-lookup"><span data-stu-id="a916f-145">The EVR will initiate the format negotiation process again.</span></span>

<span data-ttu-id="a916f-146">當任何輸入資料流程到達資料流程的結尾時，EVR 會在 rocessMessage 上呼叫 [**IMFTransform：:P**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) ，並以 [**MFT \_ 訊息 \_ 通知 \_ 結尾 \_ \_**](mft-message-notify-end-of-stream.md)。</span><span class="sxs-lookup"><span data-stu-id="a916f-146">When any input stream reaches the end of the stream, the EVR calls [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) on the mixer with [**MFT\_MESSAGE\_NOTIFY\_END\_OF\_STREAM**](mft-message-notify-end-of-stream.md).</span></span>

<span data-ttu-id="a916f-147">混音器會使用 EVR 的 [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) 介面，將下列事件傳送至 EVR。</span><span class="sxs-lookup"><span data-stu-id="a916f-147">The mixer sends the following events to the EVR, using the EVR's [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) interface.</span></span> <span data-ttu-id="a916f-148">此介面記載于 DirectShow SDK 檔中。</span><span class="sxs-lookup"><span data-stu-id="a916f-148">This interface is documented in the DirectShow SDK documentation.</span></span>



| <span data-ttu-id="a916f-149">事件</span><span class="sxs-lookup"><span data-stu-id="a916f-149">Event</span></span>                                            | <span data-ttu-id="a916f-150">描述</span><span class="sxs-lookup"><span data-stu-id="a916f-150">Description</span></span>                            |
|--------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="a916f-151">**\_需要 EC 範例 \_**</span><span class="sxs-lookup"><span data-stu-id="a916f-151">**EC\_SAMPLE\_NEEDED**</span></span>](../directshow/ec-sample-needed.md) | <span data-ttu-id="a916f-152">混音器需要新的輸入範例。</span><span class="sxs-lookup"><span data-stu-id="a916f-152">The mixer requires a new input sample.</span></span> |



 

<span data-ttu-id="a916f-153">EVR 可能會在串流處理開始之前，于混音器上呼叫 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 。</span><span class="sxs-lookup"><span data-stu-id="a916f-153">The EVR might call [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer before streaming starts.</span></span> <span data-ttu-id="a916f-154">混音器不應該讓這些呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="a916f-154">The mixer should not fail these calls.</span></span> <span data-ttu-id="a916f-155">相反地，它應該以黑色圖元填滿輸出介面。</span><span class="sxs-lookup"><span data-stu-id="a916f-155">Instead, it should fill the output surface with black pixels.</span></span> <span data-ttu-id="a916f-156">混音器應該會繼續以色彩填滿輸出範例，直到它收到 [**MFT \_ 訊息 \_ 通知 \_ 開始 \_ 串流**](mft-message-notify-begin-streaming.md) 訊息或呼叫 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 方法為止。</span><span class="sxs-lookup"><span data-stu-id="a916f-156">The mixer should continue to color-fill output samples until it receives an [**MFT\_MESSAGE\_NOTIFY\_BEGIN\_STREAMING**](mft-message-notify-begin-streaming.md) message or the [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) method is called.</span></span> <span data-ttu-id="a916f-157">如果混音器收到 [**MFT \_ 訊息 \_ 通知 \_ 結束 \_ 串流**](mft-message-notify-end-streaming.md) 訊息，則應該切換回色彩填滿模式。</span><span class="sxs-lookup"><span data-stu-id="a916f-157">If the mixer receives an [**MFT\_MESSAGE\_NOTIFY\_END\_STREAMING**](mft-message-notify-end-streaming.md) message, it should switch back to color-fill mode.</span></span>

## <a name="implementing-imfvideodeviceid"></a><span data-ttu-id="a916f-158">執行 IMFVideoDeviceID</span><span class="sxs-lookup"><span data-stu-id="a916f-158">Implementing IMFVideoDeviceID</span></span>

<span data-ttu-id="a916f-159">[**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)介面包含一個方法 [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid)，它會傳回裝置 GUID。</span><span class="sxs-lookup"><span data-stu-id="a916f-159">The [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) interface contains one method, [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid), which returns a device GUID.</span></span> <span data-ttu-id="a916f-160">裝置 GUID 可確保展示者和混音器使用相容的技術。</span><span class="sxs-lookup"><span data-stu-id="a916f-160">The device GUID ensures that the presenter and the mixer use compatible technologies.</span></span> <span data-ttu-id="a916f-161">如果裝置 Guid 不符，EVR 將無法初始化。</span><span class="sxs-lookup"><span data-stu-id="a916f-161">If the device GUIDs do not match, the EVR fails to initialize.</span></span>

<span data-ttu-id="a916f-162">標準混音器和展示者都使用 Direct3D 9，且裝置 GUID 等於 IID \_ IDirect3DDevice9。</span><span class="sxs-lookup"><span data-stu-id="a916f-162">The standard mixer and presenter both use Direct3D 9, with the device GUID equal to IID\_IDirect3DDevice9.</span></span> <span data-ttu-id="a916f-163">如果您想要將您的自訂展示者與標準混音器搭配使用，則展示者的裝置 GUID 必須是 IID \_ IDirect3DDevice9。</span><span class="sxs-lookup"><span data-stu-id="a916f-163">If you intend to use your custom presenter with the standard mixer, the presenter's device GUID must be IID\_IDirect3DDevice9.</span></span> <span data-ttu-id="a916f-164">如果您取代這兩個元件，則可以定義新的裝置 GUID。</span><span class="sxs-lookup"><span data-stu-id="a916f-164">If you replace both components, you could define a new device GUID.</span></span>

## <a name="implementing-imftopologyservicelookupclient"></a><span data-ttu-id="a916f-165">執行 IMFTopologyServiceLookupClient</span><span class="sxs-lookup"><span data-stu-id="a916f-165">Implementing IMFTopologyServiceLookupClient</span></span>

<span data-ttu-id="a916f-166">混音器必須執行 [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) 介面。</span><span class="sxs-lookup"><span data-stu-id="a916f-166">The mixer must implement the [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) interface.</span></span> <span data-ttu-id="a916f-167">開始串流之前，EVR 會呼叫 [**IMFTopologyServiceLookupClient：： InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) ，並將指標傳入 EVR 的 [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) 介面。</span><span class="sxs-lookup"><span data-stu-id="a916f-167">Before streaming begins, the EVR calls [**IMFTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) and passes in a pointer to the EVR's [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) interface.</span></span> <span data-ttu-id="a916f-168">混音器會使用這個指標從 EVR 取得介面指標。</span><span class="sxs-lookup"><span data-stu-id="a916f-168">The mixer uses this pointer to get interface pointers from the EVR.</span></span>

<span data-ttu-id="a916f-169">混音器至少必須查詢下列介面：</span><span class="sxs-lookup"><span data-stu-id="a916f-169">At a minimum, the mixer must query for the following interface:</span></span>

-   [<span data-ttu-id="a916f-170">**IMediaEventSink**</span><span class="sxs-lookup"><span data-stu-id="a916f-170">**IMediaEventSink**</span></span>](/windows/win32/api/strmif/nn-strmif-imediaeventsink)

<span data-ttu-id="a916f-171">當 EVR 呼叫 [**IMFTopologyServiceLookupClient：： ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers)時，混音器必須釋放從呼叫取得的任何指標至 [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers)。</span><span class="sxs-lookup"><span data-stu-id="a916f-171">When the EVR calls [**IMFTopologyServiceLookupClient::ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers), the mixer must release any pointers obtained from the call to [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers).</span></span>

## <a name="mixer-attributes"></a><span data-ttu-id="a916f-172">混音器屬性</span><span class="sxs-lookup"><span data-stu-id="a916f-172">Mixer Attributes</span></span>

<span data-ttu-id="a916f-173">混音器應該支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="a916f-173">A mixer should support the following attributes.</span></span>



| <span data-ttu-id="a916f-174">屬性</span><span class="sxs-lookup"><span data-stu-id="a916f-174">Attribute</span></span>                                                                        | <span data-ttu-id="a916f-175">描述</span><span class="sxs-lookup"><span data-stu-id="a916f-175">Description</span></span>                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a916f-176">**MF \_ SA \_ D3D \_ 感知**</span><span class="sxs-lookup"><span data-stu-id="a916f-176">**MF\_SA\_D3D\_AWARE**</span></span>](mf-sa-d3d-aware-attribute.md)                          | <span data-ttu-id="a916f-177">指定混音器是否支援 (DXVA) 的 DirectX Video 加速。</span><span class="sxs-lookup"><span data-stu-id="a916f-177">Specifies whether the mixer supports DirectX Video Acceleration (DXVA).</span></span>                                                                                                                                                                               |
| [<span data-ttu-id="a916f-178">**MF \_ SA \_ 需求 \_ 範例 \_ 計數**</span><span class="sxs-lookup"><span data-stu-id="a916f-178">**MF\_SA\_REQUIRED\_SAMPLE\_COUNT**</span></span>](mf-sa-required-sample-count-attribute.md) | <span data-ttu-id="a916f-179">EVR 應該為每個混音器串流配置的影片樣本數。</span><span class="sxs-lookup"><span data-stu-id="a916f-179">The number of video samples the EVR should allocate for each mixer stream.</span></span> <span data-ttu-id="a916f-180">這個屬性會套用至個別資料流程;使用 [**IMFTransform：： GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes)所傳回的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="a916f-180">This attribute applies to individual streams; use the attribute store returned by [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes).</span></span> |



 

## <a name="setting-the-mixer-on-the-evr"></a><span data-ttu-id="a916f-181">在 EVR 上設定混音器</span><span class="sxs-lookup"><span data-stu-id="a916f-181">Setting the Mixer on the EVR</span></span>

<span data-ttu-id="a916f-182">若要在 EVR 上設定自訂混音器，請呼叫 [**IMFVideoRenderer：： InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer)。</span><span class="sxs-lookup"><span data-stu-id="a916f-182">To set a custom mixer on the EVR, call [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span></span> <span data-ttu-id="a916f-183">DirectShow EVR 濾波器和 EVR 媒體接收器都會執行此方法。</span><span class="sxs-lookup"><span data-stu-id="a916f-183">Both the DirectShow EVR filter and the EVR media sink implement this method.</span></span>

<span data-ttu-id="a916f-184">**EVR 啟用物件**。</span><span class="sxs-lookup"><span data-stu-id="a916f-184">**EVR Activation Object**.</span></span> <span data-ttu-id="a916f-185">如果您使用 EVR 啟始物件，您可以在 EVR 啟用物件上設定下列其中一個屬性，以提供自訂混音器：</span><span class="sxs-lookup"><span data-stu-id="a916f-185">If you are using the EVR activation object, you can provide a custom mixer by setting one of the following attributes on the EVR activation object:</span></span>



| <span data-ttu-id="a916f-186">屬性</span><span class="sxs-lookup"><span data-stu-id="a916f-186">Attribute</span></span>                                                                                                 | <span data-ttu-id="a916f-187">描述</span><span class="sxs-lookup"><span data-stu-id="a916f-187">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a916f-188">**MF \_ 啟用 \_ 自訂 \_ 視頻 \_ 混音器 \_ 啟用**</span><span class="sxs-lookup"><span data-stu-id="a916f-188">**MF\_ACTIVATE\_CUSTOM\_VIDEO\_MIXER\_ACTIVATE**</span></span>](mf-activate-custom-video-mixer-activate-attribute.md) | <span data-ttu-id="a916f-189">混音器之啟用物件的指標。</span><span class="sxs-lookup"><span data-stu-id="a916f-189">Pointer to an activation object for the mixer.</span></span> <span data-ttu-id="a916f-190">啟用物件必須執行 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面。</span><span class="sxs-lookup"><span data-stu-id="a916f-190">The activation object must implement the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span> |
| [<span data-ttu-id="a916f-191">**MF \_ 啟用 \_ 自訂 \_ 視頻 \_ 混音器 \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="a916f-191">**MF\_ACTIVATE\_CUSTOM\_VIDEO\_MIXER\_CLSID**</span></span>](mf-activate-custom-video-mixer-clsid-attribute.md)       | <span data-ttu-id="a916f-192">混音器的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="a916f-192">CLSID of the mixer.</span></span>                                                                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="a916f-193">相關主題</span><span class="sxs-lookup"><span data-stu-id="a916f-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a916f-194">增強的影片轉譯器</span><span class="sxs-lookup"><span data-stu-id="a916f-194">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> </dl>

 

 
