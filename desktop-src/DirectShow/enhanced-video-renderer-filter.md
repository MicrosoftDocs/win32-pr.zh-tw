---
description: 增強型影片轉譯器 (EVR) 濾波器是16通道的視頻混音器和轉譯器。 它具有與媒體基礎 EVR 媒體接收相同的核心功能和外掛程式模型。
ms.assetid: ead99cb3-2be2-42c6-ac22-be0c2ddf28d5
title: 增強的影片轉譯器篩選
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ba6e7c14386ea37424364274263859844182ed7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025702"
---
# <a name="enhanced-video-renderer-filter"></a><span data-ttu-id="952e0-104">增強的影片轉譯器篩選</span><span class="sxs-lookup"><span data-stu-id="952e0-104">Enhanced Video Renderer Filter</span></span>

> [!Note]  
> <span data-ttu-id="952e0-105">本主題適用于 Windows Vista 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="952e0-105">This topic applies to Windows Vista and later.</span></span>

 

<span data-ttu-id="952e0-106">增強型影片轉譯器 (EVR) 濾波器是16通道的視頻混音器和轉譯器。</span><span class="sxs-lookup"><span data-stu-id="952e0-106">The Enhanced Video Renderer (EVR) filter is a 16-channel video mixer and renderer.</span></span> <span data-ttu-id="952e0-107">它具有與媒體基礎 EVR 媒體接收相同的核心功能和外掛程式模型。</span><span class="sxs-lookup"><span data-stu-id="952e0-107">It has the same core functionality and plug-in model as the Media Foundation EVR media sink.</span></span>

<span data-ttu-id="952e0-108">DirectShow EVR 篩選器記載于媒體基礎 SDK 檔;如需詳細資訊，請參閱 [增強型影片](../medfound/enhanced-video-renderer.md)轉譯器。</span><span class="sxs-lookup"><span data-stu-id="952e0-108">The DirectShow EVR filter is documented in the Media Foundation SDK documentation; for more information, see [Enhanced Video Renderer](../medfound/enhanced-video-renderer.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="952e0-109">透過 <strong>QueryInterface</strong> (篩選介面) </span><span class="sxs-lookup"><span data-stu-id="952e0-109">Filter Interfaces (through <strong>QueryInterface</strong>)</span></span></td>
<td><span data-ttu-id="952e0-110">DirectShow 介面：</span><span class="sxs-lookup"><span data-stu-id="952e0-110">DirectShow interfaces:</span></span>
<ul>
<li><span data-ttu-id="952e0-111"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></span><span class="sxs-lookup"><span data-stu-id="952e0-111"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></span></span></li>
<li><span data-ttu-id="952e0-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span><span class="sxs-lookup"><span data-stu-id="952e0-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span></span></li>
<li><span data-ttu-id="952e0-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="952e0-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="952e0-114"><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></span><span class="sxs-lookup"><span data-stu-id="952e0-114"><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></span></span></li>
<li><span data-ttu-id="952e0-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>IMediaEventSink</strong></a></span><span class="sxs-lookup"><span data-stu-id="952e0-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>IMediaEventSink</strong></a></span></span></li>
<li><span data-ttu-id="952e0-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="952e0-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></li>
<li><span data-ttu-id="952e0-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="952e0-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="952e0-118"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="952e0-118"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span></span></li>
</ul>
<span data-ttu-id="952e0-119">媒體基礎介面：</span><span class="sxs-lookup"><span data-stu-id="952e0-119">Media Foundation interfaces:</span></span><br/>
<ul>
<li><span data-ttu-id="952e0-120"><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>IEVRFilterConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="952e0-120"><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>IEVRFilterConfig</strong></a></span></span></li>
<li><span data-ttu-id="952e0-121"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></span><span class="sxs-lookup"><span data-stu-id="952e0-121"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></span></span></li>
<li><span data-ttu-id="952e0-122"><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>IMFVideoPositionMapper</strong></a></span><span class="sxs-lookup"><span data-stu-id="952e0-122"><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>IMFVideoPositionMapper</strong></a></span></span></li>
<li><span data-ttu-id="952e0-123"><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>IMFVideoRenderer</strong></a></span><span class="sxs-lookup"><span data-stu-id="952e0-123"><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>IMFVideoRenderer</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="952e0-124">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="952e0-124">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="952e0-125">變數，視圖形驅動程式而定。</span><span class="sxs-lookup"><span data-stu-id="952e0-125">Variable, depending on the graphics driver.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="952e0-126">輸入 Pin 介面 (透過 <strong>QueryInterface</strong>) </span><span class="sxs-lookup"><span data-stu-id="952e0-126">Input Pin Interfaces (through <strong>QueryInterface</strong>)</span></span></td>
<td><span data-ttu-id="952e0-127">DirectShow 介面：</span><span class="sxs-lookup"><span data-stu-id="952e0-127">DirectShow interfaces:</span></span>
<ul>
<li><span data-ttu-id="952e0-128"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="952e0-128"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
<li><span data-ttu-id="952e0-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="952e0-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="952e0-130"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="952e0-130"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
</ul>
<span data-ttu-id="952e0-131">媒體基礎介面：</span><span class="sxs-lookup"><span data-stu-id="952e0-131">Media Foundation interfaces:</span></span><br/>
<ul>
<li><span data-ttu-id="952e0-132"><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>IDirectXVideoMemoryConfiguration</strong></a></span><span class="sxs-lookup"><span data-stu-id="952e0-132"><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>IDirectXVideoMemoryConfiguration</strong></a></span></span></li>
<li><span data-ttu-id="952e0-133"><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>IEVRVideoStreamControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="952e0-133"><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>IEVRVideoStreamControl</strong></a></span></span></li>
<li><span data-ttu-id="952e0-134"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></span><span class="sxs-lookup"><span data-stu-id="952e0-134"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="952e0-135">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="952e0-135">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="952e0-136">不適用。</span><span class="sxs-lookup"><span data-stu-id="952e0-136">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="952e0-137">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="952e0-137">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="952e0-138">不適用。</span><span class="sxs-lookup"><span data-stu-id="952e0-138">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="952e0-139">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="952e0-139">Filter CLSID</span></span></td>
<td><span data-ttu-id="952e0-140">CLSID_EnhancedVideoRenderer</span><span class="sxs-lookup"><span data-stu-id="952e0-140">CLSID_EnhancedVideoRenderer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="952e0-141">可執行檔</span><span class="sxs-lookup"><span data-stu-id="952e0-141">Executable</span></span></td>
<td><span data-ttu-id="952e0-142">evr.dll</span><span class="sxs-lookup"><span data-stu-id="952e0-142">evr.dll</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="952e0-143"><a href="merit.md">優點</a></span><span class="sxs-lookup"><span data-stu-id="952e0-143"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="952e0-144">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="952e0-144">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="952e0-145"><a href="filter-categories.md">篩選準則分類</a></span><span class="sxs-lookup"><span data-stu-id="952e0-145"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="952e0-146">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="952e0-146">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="952e0-147">備註</span><span class="sxs-lookup"><span data-stu-id="952e0-147">Remarks</span></span>

<span data-ttu-id="952e0-148">除了透過 **QueryInterface** 公開的介面之外，EVR 還會透過 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 方法公開其他介面。</span><span class="sxs-lookup"><span data-stu-id="952e0-148">In addition to the interfaces exposed through **QueryInterface**, the EVR exposes other interfaces through the [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) method.</span></span> <span data-ttu-id="952e0-149">其中一些介面是由 EVR 展示者或 EVR 混音器所執行，而不是 EVR 本身。</span><span class="sxs-lookup"><span data-stu-id="952e0-149">Some of these interfaces are implemented by the EVR presenter or the EVR mixer, rather than the EVR itself.</span></span> <span data-ttu-id="952e0-150">如果應用程式在 EVR 上設定自訂的簡報者或混音器，自訂版本可能會公開一組不同的介面。</span><span class="sxs-lookup"><span data-stu-id="952e0-150">If the application sets a custom presenter or mixer on the EVR, the custom versions might expose a different set of interfaces.</span></span>



| <span data-ttu-id="952e0-151">Object</span><span class="sxs-lookup"><span data-stu-id="952e0-151">Object</span></span>     | <span data-ttu-id="952e0-152">服務識別碼</span><span class="sxs-lookup"><span data-stu-id="952e0-152">Service Identifier</span></span>                                              | <span data-ttu-id="952e0-153">介面</span><span class="sxs-lookup"><span data-stu-id="952e0-153">Interfaces</span></span>                                                                                                                                                                                                                                                                                                     |
|------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="952e0-154">EVR 篩選</span><span class="sxs-lookup"><span data-stu-id="952e0-154">EVR filter</span></span> | <span data-ttu-id="952e0-155">MR \_ 影片 \_ 轉譯 \_ 服務 (查詢 EVR 或簡報者) </span><span class="sxs-lookup"><span data-stu-id="952e0-155">MR\_VIDEO\_RENDER\_SERVICE(Queries EVR or presenter)</span></span><br/> | [<span data-ttu-id="952e0-156">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="952e0-156">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [<span data-ttu-id="952e0-157">**IMFVideoDisplayControl**</span><span class="sxs-lookup"><span data-stu-id="952e0-157">**IMFVideoDisplayControl**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)<br/> [<span data-ttu-id="952e0-158">**IMFVideoPositionMapper**</span><span class="sxs-lookup"><span data-stu-id="952e0-158">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [<span data-ttu-id="952e0-159">**IMFVideoPresenter**</span><span class="sxs-lookup"><span data-stu-id="952e0-159">**IMFVideoPresenter**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopresenter)<br/>                                                          |
| <span data-ttu-id="952e0-160">EVR 篩選</span><span class="sxs-lookup"><span data-stu-id="952e0-160">EVR filter</span></span> | <span data-ttu-id="952e0-161">MR \_ 影片 \_ 加速 \_ 服務 (查詢展示者) </span><span class="sxs-lookup"><span data-stu-id="952e0-161">MR\_VIDEO\_ACCELERATION\_SERVICE(Queries presenter)</span></span><br/>  | [<span data-ttu-id="952e0-162">**IDirect3DDeviceManager9**</span><span class="sxs-lookup"><span data-stu-id="952e0-162">**IDirect3DDeviceManager9**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)                                                                                                                                                                                                                                                      |
| <span data-ttu-id="952e0-163">EVR 篩選</span><span class="sxs-lookup"><span data-stu-id="952e0-163">EVR filter</span></span> | <span data-ttu-id="952e0-164">MR \_ 影片 \_ 混音器 \_ 服務 (查詢混音器) </span><span class="sxs-lookup"><span data-stu-id="952e0-164">MR\_VIDEO\_MIXER\_SERVICE(Queries mixer)</span></span><br/>             | [<span data-ttu-id="952e0-165">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="952e0-165">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [<span data-ttu-id="952e0-166">**IMFVideoMixerBitmap**</span><span class="sxs-lookup"><span data-stu-id="952e0-166">**IMFVideoMixerBitmap**</span></span>](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)<br/> [<span data-ttu-id="952e0-167">**IMFVideoMixerControl**</span><span class="sxs-lookup"><span data-stu-id="952e0-167">**IMFVideoMixerControl**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)<br/> [<span data-ttu-id="952e0-168">**IMFVideoPositionMapper**</span><span class="sxs-lookup"><span data-stu-id="952e0-168">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [<span data-ttu-id="952e0-169">**IMFVideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="952e0-169">**IMFVideoProcessor**</span></span>](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)<br/> |
| <span data-ttu-id="952e0-170">輸入 pin</span><span class="sxs-lookup"><span data-stu-id="952e0-170">Input pins</span></span> | <span data-ttu-id="952e0-171">MR \_ 影片 \_ 加速 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="952e0-171">MR\_VIDEO\_ACCELERATION\_SERVICE</span></span>                                | [<span data-ttu-id="952e0-172">**IDirectXVideoMemoryConfiguration**</span><span class="sxs-lookup"><span data-stu-id="952e0-172">**IDirectXVideoMemoryConfiguration**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                                                                                                                                                                                                    |



 

<span data-ttu-id="952e0-173">EVR 最多可以混合16個影片串流。</span><span class="sxs-lookup"><span data-stu-id="952e0-173">The EVR can mix up to 16 video streams.</span></span> <span data-ttu-id="952e0-174">第一個輸入資料流程 (針腳 0) 稱為 *參考資料流*。</span><span class="sxs-lookup"><span data-stu-id="952e0-174">The first input stream (pin 0) is called the *reference stream*.</span></span> <span data-ttu-id="952e0-175">參考資料流一律會先出現在 z 順序中。</span><span class="sxs-lookup"><span data-stu-id="952e0-175">The reference stream always appears first in the z-order.</span></span> <span data-ttu-id="952e0-176">任何額外的資料流程都稱為子串流，而且會在參考資料流上方混合。</span><span class="sxs-lookup"><span data-stu-id="952e0-176">Any additional streams are called substreams, and are mixed on top of the reference stream.</span></span> <span data-ttu-id="952e0-177">應用程式可以變更子串流的迭置順序，但不能先以迭置順序來進行子流。</span><span class="sxs-lookup"><span data-stu-id="952e0-177">The application can change the z-order of the substreams, but no substream can be first in the z-order.</span></span>

<span data-ttu-id="952e0-178">圖形驅動程式會決定支援的影片格式，但通常僅限於下列各項：</span><span class="sxs-lookup"><span data-stu-id="952e0-178">The graphics driver determines which video formats are supported, but typically they are limited to the following:</span></span>

-   <span data-ttu-id="952e0-179">參考資料流：不含每圖元 Alpha (（例如 NV12 或 YUY2) ;）的漸進式或交錯式 YUV或漸進式 RGB。</span><span class="sxs-lookup"><span data-stu-id="952e0-179">Reference stream: Progressive or interlaced YUV with no per-pixel alpha (such as NV12 or YUY2); or progressive RGB.</span></span>
-   <span data-ttu-id="952e0-180">子串流：每圖元 Alpha 的漸進 YUV，例如 AYUV 或 AI44。</span><span class="sxs-lookup"><span data-stu-id="952e0-180">Substreams: Progressive YUV with per-pixel-alpha, such as AYUV or AI44.</span></span>

<span data-ttu-id="952e0-181">可用的子資料流程格式可能取決於參考資料流的格式。</span><span class="sxs-lookup"><span data-stu-id="952e0-181">The available substream formats might depend on the format of the reference stream.</span></span>

<span data-ttu-id="952e0-182">EVR 會透過 pin 0 轉送向上游搜尋命令。</span><span class="sxs-lookup"><span data-stu-id="952e0-182">The EVR forwards seek commands upstream through pin 0.</span></span> <span data-ttu-id="952e0-183">子流釘選不會轉寄搜尋命令。</span><span class="sxs-lookup"><span data-stu-id="952e0-183">The substream pins do not forward seek commands.</span></span> <span data-ttu-id="952e0-184">來源或分隔器篩選準則的責任是讓子串流與參考資料流保持同步。</span><span class="sxs-lookup"><span data-stu-id="952e0-184">It is the responsibility of the source or splitter filter to keep the substreams synchronized with the reference stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="952e0-185">規格需求</span><span class="sxs-lookup"><span data-stu-id="952e0-185">Requirements</span></span>



| <span data-ttu-id="952e0-186">需求</span><span class="sxs-lookup"><span data-stu-id="952e0-186">Requirement</span></span> | <span data-ttu-id="952e0-187">值</span><span class="sxs-lookup"><span data-stu-id="952e0-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="952e0-188">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="952e0-188">Minimum supported client</span></span><br/> | <span data-ttu-id="952e0-189">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="952e0-189">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="952e0-190">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="952e0-190">Minimum supported server</span></span><br/> | <span data-ttu-id="952e0-191">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="952e0-191">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="952e0-192">另請參閱</span><span class="sxs-lookup"><span data-stu-id="952e0-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="952e0-193">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="952e0-193">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

