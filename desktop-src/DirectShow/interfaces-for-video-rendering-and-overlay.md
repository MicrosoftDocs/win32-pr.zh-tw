---
description: 影片轉譯和重迭的介面
ms.assetid: e4d4e456-61fb-492b-b817-30629681e270
title: 影片轉譯和重迭的介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cfa8a94765671e38c48418d37b929215e84b2fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688228"
---
# <a name="interfaces-for-video-rendering-and-overlay"></a><span data-ttu-id="54728-103">影片轉譯和重迭的介面</span><span class="sxs-lookup"><span data-stu-id="54728-103">Interfaces for Video Rendering and Overlay</span></span>

<span data-ttu-id="54728-104">這些介面支援應用程式控制影片轉譯。</span><span class="sxs-lookup"><span data-stu-id="54728-104">These interfaces support application control over video rendering.</span></span> <span data-ttu-id="54728-105">請注意，其中一些介面現在已被取代，因為影片混合轉譯器篩選器提供了絕佳的轉譯和重迭控制項。</span><span class="sxs-lookup"><span data-stu-id="54728-105">Note that some of these interfaces are now deprecated, because the Video Mixing Renderer filter provides superior rendering and overlay control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54728-106">介面</span><span class="sxs-lookup"><span data-stu-id="54728-106">Interface</span></span></th>
<th><span data-ttu-id="54728-107">描述</span><span class="sxs-lookup"><span data-stu-id="54728-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="54728-108"><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-108"><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a></span></span></td>
<td><span data-ttu-id="54728-109">提供存取已關閉的標題資訊和設定。</span><span class="sxs-lookup"><span data-stu-id="54728-109">Provides access to closed-captioned information and settings.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54728-110"><a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-110"><a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX</strong></a></span></span></td>
<td><span data-ttu-id="54728-111">將重迭效果套用至視頻界面。</span><span class="sxs-lookup"><span data-stu-id="54728-111">Apply overlay effects to the video surface.</span></span> <span data-ttu-id="54728-112">(已取代。)</span><span class="sxs-lookup"><span data-stu-id="54728-112">(Deprecated.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54728-113"><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-113"><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties</strong></a></span></span></td>
<td><span data-ttu-id="54728-114">控制如果影片視窗小於影片的原生大小，DirectShow 如何調整影片影像。</span><span class="sxs-lookup"><span data-stu-id="54728-114">Control how DirectShow scales a video image if the video window is smaller than the native size of the video.</span></span> <span data-ttu-id="54728-115">(已取代。)</span><span class="sxs-lookup"><span data-stu-id="54728-115">(Deprecated.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54728-116"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-116"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></span></span></td>
<td><span data-ttu-id="54728-117">設定影片內容。</span><span class="sxs-lookup"><span data-stu-id="54728-117">Set video properties.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54728-118"><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-118"><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a></span></span></td>
<td><span data-ttu-id="54728-119">以 Microsoft DirectDraw 專屬全螢幕模式轉譯影片。</span><span class="sxs-lookup"><span data-stu-id="54728-119">Render video in Microsoft DirectDraw exclusive full-screen mode.</span></span> <span data-ttu-id="54728-120">(已取代。)</span><span class="sxs-lookup"><span data-stu-id="54728-120">(Deprecated.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54728-121"><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideocallback"><strong>IDDrawExclModeVideoCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-121"><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideocallback"><strong>IDDrawExclModeVideoCallback</strong></a></span></span></td>
<td><span data-ttu-id="54728-122">回呼介面，可接收關於重迭位置、大小和可見度之變更的通知。</span><span class="sxs-lookup"><span data-stu-id="54728-122">Callback interface to receive notification about changes to the overlay position, size, and visibility.</span></span> <span data-ttu-id="54728-123">(已取代。)</span><span class="sxs-lookup"><span data-stu-id="54728-123">(Deprecated.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54728-124"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo"><strong>IDirectDrawVideo</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-124"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo"><strong>IDirectDrawVideo</strong></a></span></span></td>
<td><span data-ttu-id="54728-125">停用指定的 DirectDraw 功能。</span><span class="sxs-lookup"><span data-stu-id="54728-125">Disable specified DirectDraw capabilities.</span></span> <span data-ttu-id="54728-126">(已取代。)</span><span class="sxs-lookup"><span data-stu-id="54728-126">(Deprecated.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54728-127"><a href="/previous-versions/windows/desktop/api/Amstream/nn-amstream-idirectdrawmediasample"><strong>IDirectDrawMediaSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-127"><a href="/previous-versions/windows/desktop/api/Amstream/nn-amstream-idirectdrawmediasample"><strong>IDirectDrawMediaSample</strong></a></span></span></td>
<td><span data-ttu-id="54728-128">存取覆迭 <a href="overlay-mixer-filter.md">混音</a> 器所配置的 DirectDraw 介面。 (已淘汰。 ) </span><span class="sxs-lookup"><span data-stu-id="54728-128">Access a DirectDraw surface allocated by the <a href="overlay-mixer-filter.md">Overlay Mixer</a> filter.(Deprecated.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54728-129"><a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-129"><a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a></span></span></td>
<td><span data-ttu-id="54728-130">在重迭混音器上執行。</span><span class="sxs-lookup"><span data-stu-id="54728-130">Implemented on the Overlay Mixer.</span></span> <span data-ttu-id="54728-131">啟用無視窗用戶端（例如 ActiveX®控制項）來取得和設定影片矩形的屬性，以及建議事件篩選。</span><span class="sxs-lookup"><span data-stu-id="54728-131">Enables windowless clients such as ActiveX® controls to get and set properties of the video rectangle and advise the filter of events.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54728-132"><a href="/previous-versions/windows/desktop/api/mixerocx/nn-mixerocx-imixerocxnotify"><strong>IMixerOCXNotify</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-132"><a href="/previous-versions/windows/desktop/api/mixerocx/nn-mixerocx-imixerocxnotify"><strong>IMixerOCXNotify</strong></a></span></span></td>
<td><span data-ttu-id="54728-133">由「無視窗」用戶端執行，並由重迭混音器呼叫，以傳送影響影片顯示矩形的事件通知。</span><span class="sxs-lookup"><span data-stu-id="54728-133">Implemented by windowless clients and called by the Overlay Mixer to send notifications of events affecting the video display rectangle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54728-134"><a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-134"><a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a></span></span></td>
<td><span data-ttu-id="54728-135">在混合多個影片串流時，設定覆迭混音器篩選器上的影片色彩控制項。</span><span class="sxs-lookup"><span data-stu-id="54728-135">Set video color controls on the Overlay Mixer filter when mixing multiple video streams.</span></span> <span data-ttu-id="54728-136">(已取代。)</span><span class="sxs-lookup"><span data-stu-id="54728-136">(Deprecated.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54728-137"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-137"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span></span></td>
<td><span data-ttu-id="54728-138">查詢影片轉譯器以取得效能資訊。</span><span class="sxs-lookup"><span data-stu-id="54728-138">Query a video renderer for performance information.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54728-139"><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-139"><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></span></span></td>
<td><span data-ttu-id="54728-140">設定影片視窗屬性。</span><span class="sxs-lookup"><span data-stu-id="54728-140">Set video window properties.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="54728-141"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-141"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a></span></span></li>
<li><span data-ttu-id="54728-142"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-142"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a></span></span></li>
<li><span data-ttu-id="54728-143"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-143"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a></span></span></li>
<li><span data-ttu-id="54728-144"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9"><strong>IVMRImageCompositor9</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-144"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9"><strong>IVMRImageCompositor9</strong></a></span></span></li>
<li><span data-ttu-id="54728-145"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9"><strong>IVMRImagePresenter9</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-145"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9"><strong>IVMRImagePresenter9</strong></a></span></span></li>
<li><span data-ttu-id="54728-146"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9"><strong>IVMRImagePresenterConfig9</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-146"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9"><strong>IVMRImagePresenterConfig9</strong></a></span></span></li>
<li><span data-ttu-id="54728-147"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-147"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a></span></span></li>
<li><span data-ttu-id="54728-148"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-148"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></span></span></li>
<li><span data-ttu-id="54728-149"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-149"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></span></span></li>
<li><span data-ttu-id="54728-150"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurface9"><strong>IVMRSurface9</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-150"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurface9"><strong>IVMRSurface9</strong></a></span></span></li>
<li><span data-ttu-id="54728-151"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9"><strong>IVMRSurfaceAllocator9</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-151"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9"><strong>IVMRSurfaceAllocator9</strong></a></span></span></li>
<li><span data-ttu-id="54728-152"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9"><strong>IVMRSurfaceAllocatorEx9</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-152"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9"><strong>IVMRSurfaceAllocatorEx9</strong></a></span></span></li>
<li><span data-ttu-id="54728-153"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-153"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></span></span></li>
<li><span data-ttu-id="54728-154"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-154"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="54728-155">影片混合轉譯器9介面。</span><span class="sxs-lookup"><span data-stu-id="54728-155">Video Mixing Renderer 9 interfaces.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="54728-156"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-156"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></span></span></li>
<li><span data-ttu-id="54728-157"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-157"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></span></span></li>
<li><span data-ttu-id="54728-158"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-158"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></span></span></li>
<li><span data-ttu-id="54728-159"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor"><strong>IVMRImageCompositor</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-159"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor"><strong>IVMRImageCompositor</strong></a></span></span></li>
<li><span data-ttu-id="54728-160"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter"><strong>IVMRImagePresenter</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-160"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter"><strong>IVMRImagePresenter</strong></a></span></span></li>
<li><span data-ttu-id="54728-161"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig"><strong>IVMRImagePresenterConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-161"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig"><strong>IVMRImagePresenterConfig</strong></a></span></span></li>
<li><span data-ttu-id="54728-162"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-162"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></span></span></li>
<li><span data-ttu-id="54728-163"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-163"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></span></span></li>
<li><span data-ttu-id="54728-164"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator"><strong>IVMRSurfaceAllocator</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-164"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator"><strong>IVMRSurfaceAllocator</strong></a></span></span></li>
<li><span data-ttu-id="54728-165"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-165"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></span></span></li>
<li><span data-ttu-id="54728-166"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="54728-166"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="54728-167">影片混合轉譯器7介面。</span><span class="sxs-lookup"><span data-stu-id="54728-167">Video Mixing Renderer 7 interfaces.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="54728-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="54728-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54728-169">使用影片混合轉譯器</span><span class="sxs-lookup"><span data-stu-id="54728-169">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 



