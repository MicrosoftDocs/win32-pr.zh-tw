---
description: 影片混合轉譯器篩選器7
ms.assetid: c83e6c50-76f2-4aeb-944b-5b244c6bf776
title: 影片混合轉譯器篩選器7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e396e15189e89dcebde69fb513419df340ab09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512536"
---
# <a name="video-mixing-renderer-filter-7"></a><span data-ttu-id="af7e5-103">影片混合轉譯器篩選器7</span><span class="sxs-lookup"><span data-stu-id="af7e5-103">Video Mixing Renderer Filter 7</span></span>

<span data-ttu-id="af7e5-104">本主題適用于 Windows XP 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="af7e5-104">This topic applies to Windows XP or later.</span></span>

<span data-ttu-id="af7e5-105">在 Windows XP 和更新版本中，混合轉譯器 7 (VMR-7) 的影片是預設的影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="af7e5-105">In Windows XP and later, the Video Mixing Renderer 7 (VMR-7) is the default video renderer.</span></span> <span data-ttu-id="af7e5-106">這稱為 VMR-7，因為它會在內部使用 DirectDraw 7。</span><span class="sxs-lookup"><span data-stu-id="af7e5-106">It is called the VMR-7 because internally it uses DirectDraw 7.</span></span> <span data-ttu-id="af7e5-107">在 DirectX 9 中，您可以在非 XP 系統上轉散發類似但個別的篩選器，也就是 VMR-9。</span><span class="sxs-lookup"><span data-stu-id="af7e5-107">In DirectX 9, a similar but separate filter, the VMR-9, is available for redistribution on non-XP systems.</span></span> <span data-ttu-id="af7e5-108">VMR-9 使用 Direct3D 9。</span><span class="sxs-lookup"><span data-stu-id="af7e5-108">The VMR-9 uses Direct3D 9.</span></span>

> [!Note]  
> <span data-ttu-id="af7e5-109">VMR 可在 Windows XP 和更新版本上取得。</span><span class="sxs-lookup"><span data-stu-id="af7e5-109">The VMR is available on Windows XP and later.</span></span> <span data-ttu-id="af7e5-110">它無法透過 DirectX 可轉散發套件或舊版 Windows 使用。</span><span class="sxs-lookup"><span data-stu-id="af7e5-110">It is not available through the DirectX redistributable, or on previous versions of Windows.</span></span> <span data-ttu-id="af7e5-111">在大部分的情況下，應用程式應該使用 [影片混合](video-mixing-renderer-filter-9.md)轉譯器9。</span><span class="sxs-lookup"><span data-stu-id="af7e5-111">For most scenarios, applications should use the [Video Mixing Renderer 9](video-mixing-renderer-filter-9.md).</span></span>

 

<span data-ttu-id="af7e5-112">VMR 的功能包括：</span><span class="sxs-lookup"><span data-stu-id="af7e5-112">Features of the VMR include:</span></span>

-   <span data-ttu-id="af7e5-113">真正的 Alpha 混合，最多16個輸入資料流程</span><span class="sxs-lookup"><span data-stu-id="af7e5-113">True alpha blending of up to 16 input streams</span></span>
-   <span data-ttu-id="af7e5-114">轉譯之前的合成影像存取</span><span class="sxs-lookup"><span data-stu-id="af7e5-114">Access to the composited image before it is rendered</span></span>
-   <span data-ttu-id="af7e5-115">可讓協力廠商執行自訂影片效果的外掛程式模型。</span><span class="sxs-lookup"><span data-stu-id="af7e5-115">A plug-in model that enables third-parties to implement custom video effects.</span></span>
-   <span data-ttu-id="af7e5-116">最多可支援15個監視器。</span><span class="sxs-lookup"><span data-stu-id="af7e5-116">Support for up to 15 monitors.</span></span>

<span data-ttu-id="af7e5-117">在 Windows XP 和更新版本的圖表建立期間，除非應用程式明確建立並新增至圖形，否則篩選圖形管理員將不會使用較舊的影片轉譯器或覆迭混音器篩選。</span><span class="sxs-lookup"><span data-stu-id="af7e5-117">During graph building on Windows XP and later, the Filter Graph Manager will not use the older Video Renderer or Overlay Mixer filters, unless the application explicitly creates them and adds to the graph.</span></span>

<span data-ttu-id="af7e5-118">如需詳細資訊，請參閱 [使用影片混合](using-the-video-mixing-renderer.md)轉譯器。</span><span class="sxs-lookup"><span data-stu-id="af7e5-118">For more information, see [Using the Video Mixing Renderer](using-the-video-mixing-renderer.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="af7e5-119">篩選介面</span><span class="sxs-lookup"><span data-stu-id="af7e5-119">Filter Interfaces</span></span></td>
<td><span data-ttu-id="af7e5-120">所有模式：</span><span class="sxs-lookup"><span data-stu-id="af7e5-120">All modes:</span></span>
<ul>
<li><span data-ttu-id="af7e5-121"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></span><span class="sxs-lookup"><span data-stu-id="af7e5-121"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></span></span></li>
<li><span data-ttu-id="af7e5-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span><span class="sxs-lookup"><span data-stu-id="af7e5-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span></span></li>
<li><span data-ttu-id="af7e5-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="af7e5-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="af7e5-124"><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></span><span class="sxs-lookup"><span data-stu-id="af7e5-124"><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></span></span></li>
<li><span data-ttu-id="af7e5-125"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></span><span class="sxs-lookup"><span data-stu-id="af7e5-125"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></span></span></li>
<li><span data-ttu-id="af7e5-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="af7e5-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></li>
<li><span data-ttu-id="af7e5-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="af7e5-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="af7e5-128"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="af7e5-128"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span></span></li>
<li><span data-ttu-id="af7e5-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="af7e5-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></span></span></li>
<li><span data-ttu-id="af7e5-130"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="af7e5-130"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></span></span></li>
<li><span data-ttu-id="af7e5-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="af7e5-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></span></span></li>
<li><span data-ttu-id="af7e5-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></span><span class="sxs-lookup"><span data-stu-id="af7e5-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></span></span></li>
</ul>
<span data-ttu-id="af7e5-133">視窗模式：</span><span class="sxs-lookup"><span data-stu-id="af7e5-133">Windowed mode:</span></span><br/>
<ul>
<li><span data-ttu-id="af7e5-134"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a></span><span class="sxs-lookup"><span data-stu-id="af7e5-134"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a></span></span></li>
<li><span data-ttu-id="af7e5-135"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></span><span class="sxs-lookup"><span data-stu-id="af7e5-135"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></span></span></li>
<li><span data-ttu-id="af7e5-136"><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="af7e5-136"><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></span></span></li>
<li><span data-ttu-id="af7e5-137"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="af7e5-137"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></span></span></li>
</ul>
<span data-ttu-id="af7e5-138">無視窗模式：</span><span class="sxs-lookup"><span data-stu-id="af7e5-138">Windowless mode:</span></span><br/>
<ul>
<li><span data-ttu-id="af7e5-139"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="af7e5-139"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></span></span></li>
<li><span data-ttu-id="af7e5-140"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="af7e5-140"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></span></span></li>
</ul>
<span data-ttu-id="af7e5-141">Renderless 模式：</span><span class="sxs-lookup"><span data-stu-id="af7e5-141">Renderless mode:</span></span><br/>
<ul>
<li><span data-ttu-id="af7e5-142"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></span><span class="sxs-lookup"><span data-stu-id="af7e5-142"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></span></span></li>
</ul>
<span data-ttu-id="af7e5-143">混音器模式：</span><span class="sxs-lookup"><span data-stu-id="af7e5-143">Mixer mode:</span></span><br/>
<ul>
<li><span data-ttu-id="af7e5-144"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="af7e5-144"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></span></span></li>
</ul>
<span data-ttu-id="af7e5-145">如需各種 VMR 7 模式的詳細資訊，請參閱 <a href="vmr-modes-of-operation.md">VMR 作業模式</a>。</span><span class="sxs-lookup"><span data-stu-id="af7e5-145">For information about the various VMR-7 modes, see <a href="vmr-modes-of-operation.md">VMR Modes of Operation</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af7e5-146">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="af7e5-146">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="af7e5-147">主要類型： MEDIATYPE_VideoSubtype：相依于圖形硬體。</span><span class="sxs-lookup"><span data-stu-id="af7e5-147">Major type: MEDIATYPE_VideoSubtype: Depends on the graphics hardware.</span></span> <span data-ttu-id="af7e5-148">必須是未壓縮的影片。</span><span class="sxs-lookup"><span data-stu-id="af7e5-148">Must be uncompressed video.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af7e5-149">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="af7e5-149">Input Pin Interfaces</span></span></td>
<td><ul>
<li><span data-ttu-id="af7e5-150"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a></span><span class="sxs-lookup"><span data-stu-id="af7e5-150"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a></span></span></li>
<li><span data-ttu-id="af7e5-151"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="af7e5-151"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
<li><span data-ttu-id="af7e5-152"><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (請參閱備註) </span><span class="sxs-lookup"><span data-stu-id="af7e5-152"><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (see Remarks)</span></span></li>
<li><span data-ttu-id="af7e5-153"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="af7e5-153"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="af7e5-154"><a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a></span><span class="sxs-lookup"><span data-stu-id="af7e5-154"><a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a></span></span></li>
<li><span data-ttu-id="af7e5-155"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="af7e5-155"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="af7e5-156"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol"><strong>IVMRVideoStreamControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="af7e5-156"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol"><strong>IVMRVideoStreamControl</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af7e5-157">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="af7e5-157">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="af7e5-158">不適用。</span><span class="sxs-lookup"><span data-stu-id="af7e5-158">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af7e5-159">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="af7e5-159">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="af7e5-160">不適用。</span><span class="sxs-lookup"><span data-stu-id="af7e5-160">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af7e5-161">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="af7e5-161">Filter CLSID</span></span></td>
<td><span data-ttu-id="af7e5-162">有兩個與此篩選準則相關聯的 Clsid：</span><span class="sxs-lookup"><span data-stu-id="af7e5-162">There are two CLSIDs associated with this filter:</span></span>
<ul>
<li><span data-ttu-id="af7e5-163">CLSID_VideoMixingRenderer：建立 VMR-7。</span><span class="sxs-lookup"><span data-stu-id="af7e5-163">CLSID_VideoMixingRenderer: Creates the VMR-7.</span></span> <span data-ttu-id="af7e5-164">如果系統資源不足，無法建立 VMR-7，則對 <strong>CoCreateInstance</strong> 的呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="af7e5-164">If there are not enough system resources to create the VMR-7, the call to <strong>CoCreateInstance</strong> fails.</span></span></li>
<li><span data-ttu-id="af7e5-165">CLSID_VideoRendererDefault：如果有可用的系統資源，則建立 VMR-7，否則會建立舊的 <a href="video-renderer-filter.md">影片</a> 轉譯器篩選器。</span><span class="sxs-lookup"><span data-stu-id="af7e5-165">CLSID_VideoRendererDefault: Creates the VMR-7 if system resources are available, or else creates the old <a href="video-renderer-filter.md">Video Renderer</a> filter.</span></span></li>
</ul>
<span data-ttu-id="af7e5-166">如果您需要 VMR-7 的特定功能，請使用 CLSID_VideoMixingRenderer。</span><span class="sxs-lookup"><span data-stu-id="af7e5-166">Use CLSID_VideoMixingRenderer if you need the specific capabilities of the VMR-7.</span></span> <span data-ttu-id="af7e5-167">否則，請使用 CLSID_VideoRendererDefault，這幾乎不會失敗，因為它會切換回舊的影片轉譯器篩選器。</span><span class="sxs-lookup"><span data-stu-id="af7e5-167">Otherwise, use CLSID_VideoRendererDefault, which is almost certain not to fail, because it falls back to the old Video Renderer filter.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af7e5-168">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="af7e5-168">Property Page CLSID</span></span></td>
<td><span data-ttu-id="af7e5-169">不適用。</span><span class="sxs-lookup"><span data-stu-id="af7e5-169">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af7e5-170">可執行檔</span><span class="sxs-lookup"><span data-stu-id="af7e5-170">Executable</span></span></td>
<td><span data-ttu-id="af7e5-171">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="af7e5-171">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af7e5-172"><a href="merit.md">優點</a></span><span class="sxs-lookup"><span data-stu-id="af7e5-172"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="af7e5-173">MERIT_PREFERRED + 1</span><span class="sxs-lookup"><span data-stu-id="af7e5-173">MERIT_PREFERRED + 1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af7e5-174"><a href="filter-categories.md">篩選準則分類</a></span><span class="sxs-lookup"><span data-stu-id="af7e5-174"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="af7e5-175">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="af7e5-175">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="af7e5-176">備註</span><span class="sxs-lookup"><span data-stu-id="af7e5-176">Remarks</span></span>

<span data-ttu-id="af7e5-177">只有當 VMR-7 篩選處於視窗模式時，輸入 pin 才會公開 **IOverlay** 介面。</span><span class="sxs-lookup"><span data-stu-id="af7e5-177">The input pin exposes the **IOverlay** interface only when the VMR-7 filter is in windowed mode.</span></span> <span data-ttu-id="af7e5-178">Pin 所實 **IOverlay** 的唯一方法是 **GetWindowHandle**，這可讓應用程式取得篩選器影片視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="af7e5-178">The only **IOverlay** method that the pin implements is **GetWindowHandle**, which enables an application to obtain a handle to the filter's video window.</span></span> <span data-ttu-id="af7e5-179">所有其他 **IOverlay** 方法都會傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="af7e5-179">All other **IOverlay** methods return E\_NOTIMPL.</span></span> <span data-ttu-id="af7e5-180">在無視窗模式中，篩選不會建立影片視窗，因此 pin 不會公開介面。</span><span class="sxs-lookup"><span data-stu-id="af7e5-180">In windowless mode, the filter does not create a video window, so the pin does not expose the interface.</span></span>

<span data-ttu-id="af7e5-181">應用程式可以提供公開下列介面的自訂配置器展示者物件：</span><span class="sxs-lookup"><span data-stu-id="af7e5-181">An application can provide a custom allocator-presenter object that exposes the following interfaces:</span></span>

-   [<span data-ttu-id="af7e5-182">**IVMRImagePresenter**</span><span class="sxs-lookup"><span data-stu-id="af7e5-182">**IVMRImagePresenter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter)
-   <span data-ttu-id="af7e5-183">[**IVMRImagePresenterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig) (選用) </span><span class="sxs-lookup"><span data-stu-id="af7e5-183">[**IVMRImagePresenterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig) (optional)</span></span>
-   <span data-ttu-id="af7e5-184">[**IVMRMonitorConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig) (選用) </span><span class="sxs-lookup"><span data-stu-id="af7e5-184">[**IVMRMonitorConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig) (optional)</span></span>
-   [<span data-ttu-id="af7e5-185">**IVMRSurfaceAllocator**</span><span class="sxs-lookup"><span data-stu-id="af7e5-185">**IVMRSurfaceAllocator**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator)
-   <span data-ttu-id="af7e5-186">[**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) (選用) </span><span class="sxs-lookup"><span data-stu-id="af7e5-186">[**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) (optional)</span></span>

<span data-ttu-id="af7e5-187">如需自訂配置器-展示者的詳細資訊，請參閱 [為 VMR 提供自訂 Allocator-Presenter-7](supplying-a-custom-allocator-presenter-for-vmr-7.md)。</span><span class="sxs-lookup"><span data-stu-id="af7e5-187">For more information about custom allocator-presenters, see [Supplying a Custom Allocator-Presenter for VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md).</span></span>

<span data-ttu-id="af7e5-188">應用程式也可以提供公開下列介面的自訂外掛程式組合器：</span><span class="sxs-lookup"><span data-stu-id="af7e5-188">An application can also provide a custom plug-in compositor that exposes the following interface:</span></span>

-   [<span data-ttu-id="af7e5-189">**IVMRImageCompositor**</span><span class="sxs-lookup"><span data-stu-id="af7e5-189">**IVMRImageCompositor**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor)

<span data-ttu-id="af7e5-190">若要使用自訂的組合器來設定 VMR，請呼叫 [**IVMRFilterConfig：： SetImageCompositor**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setimagecompositor)。</span><span class="sxs-lookup"><span data-stu-id="af7e5-190">To configure the VMR with a custom compositor, call [**IVMRFilterConfig::SetImageCompositor**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setimagecompositor).</span></span>

## <a name="related-topics"></a><span data-ttu-id="af7e5-191">相關主題</span><span class="sxs-lookup"><span data-stu-id="af7e5-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af7e5-192">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="af7e5-192">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




