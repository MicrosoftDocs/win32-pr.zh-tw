---
description: 影片混合轉譯器篩選器9
ms.assetid: 3885cca2-74b1-4066-8ecb-84c9841f9e66
title: 影片混合轉譯器篩選器9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b2576f8c5f1b0f262b83141c14ce4836eecb4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693756"
---
# <a name="video-mixing-renderer-filter-9"></a><span data-ttu-id="c68f4-103">影片混合轉譯器篩選器9</span><span class="sxs-lookup"><span data-stu-id="c68f4-103">Video Mixing Renderer Filter 9</span></span>

<span data-ttu-id="c68f4-104">在 DirectX 9 中，影片混合轉譯器 9 (VMR-9) 篩選器提供 DirectX 支援的所有平臺上的先進影片轉譯功能。</span><span class="sxs-lookup"><span data-stu-id="c68f4-104">In DirectX 9, the Video Mixing Renderer 9 (VMR-9) filter offers advanced video rendering capabilities on all platforms supported by DirectX.</span></span> <span data-ttu-id="c68f4-105">它與 DirectX 9 3D 功能完全整合。</span><span class="sxs-lookup"><span data-stu-id="c68f4-105">It is fully integrated with DirectX 9 3D capabilities.</span></span> <span data-ttu-id="c68f4-106">例如，您可以輕鬆地將影片新增至遊戲和其他3D 環境，或使用 Direct3D 圖元著色器和其他效果來轉換影片影像。</span><span class="sxs-lookup"><span data-stu-id="c68f4-106">For example, that you can easily add video to games and other 3D environments or transform video images using the Direct3D pixel shaders and other effects.</span></span>

<span data-ttu-id="c68f4-107">此篩選器不支援視訊連接埠。</span><span class="sxs-lookup"><span data-stu-id="c68f4-107">This filter does not support video ports.</span></span>

<span data-ttu-id="c68f4-108">為了維持回溯相容性，VMR 不是任何系統上的預設轉譯器。</span><span class="sxs-lookup"><span data-stu-id="c68f4-108">To maintain backward compatibility, the VMR-9 is not the default renderer on any system.</span></span> <span data-ttu-id="c68f4-109">若要使用此篩選，請明確地將它新增至篩選圖形，然後在連接任何輸入圖釘之前加以設定。</span><span class="sxs-lookup"><span data-stu-id="c68f4-109">To use this filter, add it to the filter graph explicitly and configure it before connecting any of its input pins.</span></span> <span data-ttu-id="c68f4-110">VMR-9 使用自己的介面、結構和列舉集合，這些介面與 VMR-7 的對應資料類型不一定相同。</span><span class="sxs-lookup"><span data-stu-id="c68f4-110">The VMR-9 uses its own set of interfaces, structures, and enumerations, which are not always identical to the corresponding data types used with the VMR-7.</span></span>

<span data-ttu-id="c68f4-111">VMR-9 最多支援16個監視器。</span><span class="sxs-lookup"><span data-stu-id="c68f4-111">The VMR-9 supports up to 16 monitors.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c68f4-112">篩選介面</span><span class="sxs-lookup"><span data-stu-id="c68f4-112">Filter Interfaces</span></span></td>
<td><span data-ttu-id="c68f4-113">VMR-9 支援數個不同的轉譯模式。</span><span class="sxs-lookup"><span data-stu-id="c68f4-113">The VMR-9 supports several distinct rendering modes.</span></span> <span data-ttu-id="c68f4-114">它支援一組不同的介面，視轉譯模式而定：</span><span class="sxs-lookup"><span data-stu-id="c68f4-114">It supports a different set of interfaces depending on the rendering mode:</span></span><br/>
<ul>
<li><span data-ttu-id="c68f4-115">所有模式： <a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、 <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>、 <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>、 <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a>、 <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a>、 <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a>、 <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a>、 <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="c68f4-115">All modes: <a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></span></span></li>
<li><span data-ttu-id="c68f4-116">Renderless 模式： <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"> <strong>IVMRSurfaceAllocatorNotify9</strong></a></span><span class="sxs-lookup"><span data-stu-id="c68f4-116">Renderless mode: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></span></span></li>
<li><span data-ttu-id="c68f4-117">視窗模式： <a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a>、 <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a>、 <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a>、 <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></span><span class="sxs-lookup"><span data-stu-id="c68f4-117">Windowed mode: <a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></span></span></li>
<li><span data-ttu-id="c68f4-118">無視窗模式： <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a>、 <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="c68f4-118">Windowless mode: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></span></span></li>
</ul>
<span data-ttu-id="c68f4-119">若要設定轉譯模式，請呼叫 <a href="/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode"><strong>IVMRFilterConfig9：： SetRenderingMode</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="c68f4-119">To set the rendering mode, call <a href="/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode"><strong>IVMRFilterConfig9::SetRenderingMode</strong></a>.</span></span> <span data-ttu-id="c68f4-120">如需詳細資訊，請參閱 <a href="vmr-modes-of-operation.md">VMR 操作模式</a>。</span><span class="sxs-lookup"><span data-stu-id="c68f4-120">For more information, see <a href="vmr-modes-of-operation.md">VMR Modes of Operation</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c68f4-121">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="c68f4-121">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="c68f4-122">輸入 pin 將會與基礎視頻硬體所支援的任何類型連接。</span><span class="sxs-lookup"><span data-stu-id="c68f4-122">The input pins will connect with any type supported by the underlying video hardware.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c68f4-123">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="c68f4-123">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="c68f4-124"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>、 <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrvideostreamcontrol9"><strong>IVMRVideoStreamControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="c68f4-124"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrvideostreamcontrol9"><strong>IVMRVideoStreamControl9</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c68f4-125">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="c68f4-125">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="c68f4-126">不適用。</span><span class="sxs-lookup"><span data-stu-id="c68f4-126">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c68f4-127">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="c68f4-127">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="c68f4-128">不適用。</span><span class="sxs-lookup"><span data-stu-id="c68f4-128">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c68f4-129">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="c68f4-129">Filter CLSID</span></span></td>
<td><span data-ttu-id="c68f4-130">CLSID_VideoMixingRenderer9</span><span class="sxs-lookup"><span data-stu-id="c68f4-130">CLSID_VideoMixingRenderer9</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c68f4-131">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="c68f4-131">Property Page CLSID</span></span></td>
<td><span data-ttu-id="c68f4-132">N/A</span><span class="sxs-lookup"><span data-stu-id="c68f4-132">N/A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c68f4-133">可執行檔</span><span class="sxs-lookup"><span data-stu-id="c68f4-133">Executable</span></span></td>
<td><span data-ttu-id="c68f4-134">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="c68f4-134">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c68f4-135"><a href="merit.md">優點</a></span><span class="sxs-lookup"><span data-stu-id="c68f4-135"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="c68f4-136">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="c68f4-136">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c68f4-137"><a href="filter-categories.md">篩選準則分類</a></span><span class="sxs-lookup"><span data-stu-id="c68f4-137"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="c68f4-138">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="c68f4-138">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="c68f4-139">備註</span><span class="sxs-lookup"><span data-stu-id="c68f4-139">Remarks</span></span>

<span data-ttu-id="c68f4-140">應用程式可以提供公開下列介面的自訂配置器展示者物件：</span><span class="sxs-lookup"><span data-stu-id="c68f4-140">An application can provide a custom allocator-presenter object that exposes the following interfaces:</span></span>

-   [<span data-ttu-id="c68f4-141">**IVMRImagePresenter9**</span><span class="sxs-lookup"><span data-stu-id="c68f4-141">**IVMRImagePresenter9**</span></span>](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9)
-   <span data-ttu-id="c68f4-142">[**IVMRImagePresenterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9) (選用) </span><span class="sxs-lookup"><span data-stu-id="c68f4-142">[**IVMRImagePresenterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9) (optional)</span></span>
-   [<span data-ttu-id="c68f4-143">**IVMRSurfaceAllocator9**</span><span class="sxs-lookup"><span data-stu-id="c68f4-143">**IVMRSurfaceAllocator9**</span></span>](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9)
-   <span data-ttu-id="c68f4-144">[**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) (選用) </span><span class="sxs-lookup"><span data-stu-id="c68f4-144">[**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) (optional)</span></span>
-   <span data-ttu-id="c68f4-145">[**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) (選用) </span><span class="sxs-lookup"><span data-stu-id="c68f4-145">[**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) (optional)</span></span>

<span data-ttu-id="c68f4-146">如需自訂配置器-展示者的詳細資訊，請參閱 [提供 VMR 的自訂 Allocator-Presenter-9](supplying-a-custom-allocator-presenter-for-vmr-9.md)。</span><span class="sxs-lookup"><span data-stu-id="c68f4-146">For more information about custom allocator-presenters, see [Supplying a Custom Allocator-Presenter for VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md).</span></span>

<span data-ttu-id="c68f4-147">應用程式也可以提供公開下列介面的自訂外掛程式組合器：</span><span class="sxs-lookup"><span data-stu-id="c68f4-147">An application can also provide a custom plug-in compositor that exposes the following interface:</span></span>

-   [<span data-ttu-id="c68f4-148">**IVMRImageCompositor9**</span><span class="sxs-lookup"><span data-stu-id="c68f4-148">**IVMRImageCompositor9**</span></span>](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9)

<span data-ttu-id="c68f4-149">若要使用自訂的組合器來設定 VMR，請呼叫 [**IVMRFilterConfig9：： SetImageCompositor**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setimagecompositor)。</span><span class="sxs-lookup"><span data-stu-id="c68f4-149">To configure the VMR with a custom compositor, call [**IVMRFilterConfig9::SetImageCompositor**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setimagecompositor).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c68f4-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="c68f4-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c68f4-151">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="c68f4-151">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="c68f4-152">使用影片混合轉譯器</span><span class="sxs-lookup"><span data-stu-id="c68f4-152">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 




