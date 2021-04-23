---
description: 影片埠管理員
ms.assetid: d70558a5-9820-432a-b4f3-ccf7bb2a34d5
title: 影片埠管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db4f030e6be9035432207dc608a775a0e1d30b09
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909196"
---
# <a name="video-port-manager"></a><span data-ttu-id="04192-103">影片埠管理員</span><span class="sxs-lookup"><span data-stu-id="04192-103">Video Port Manager</span></span>

<span data-ttu-id="04192-104">影片埠管理員篩選器 (VPM) 可讓影片混合轉譯器篩選器 7 (VMR-7) 使用影片捕獲裝置或使用影片埠的硬體解碼器。</span><span class="sxs-lookup"><span data-stu-id="04192-104">The Video Port Manager filter (VPM) enables the Video Mixing Renderer Filter 7 (VMR-7) to work with video capture devices or hardware decoders that use a video port.</span></span> <span data-ttu-id="04192-105">影片埠是圖形晶片的直接硬體連接。</span><span class="sxs-lookup"><span data-stu-id="04192-105">A video port is a direct hardware connection to the graphics chip.</span></span> <span data-ttu-id="04192-106">它可讓影片直接傳送到圖形晶片，而不需要經過系統匯流排。</span><span class="sxs-lookup"><span data-stu-id="04192-106">It enables video to be transferred directly to the graphics chip without going over the system bus.</span></span>

> [!Note]  
> <span data-ttu-id="04192-107">影片埠管理員與 VMR 9 不相容，因為 VMR-9 不支援影片埠。</span><span class="sxs-lookup"><span data-stu-id="04192-107">The Video Port Manager is not compatible with the VMR-9, because the VMR-9 does not support video ports.</span></span>

 



| <span data-ttu-id="04192-108">標籤</span><span class="sxs-lookup"><span data-stu-id="04192-108">Label</span></span> | <span data-ttu-id="04192-109">值</span><span class="sxs-lookup"><span data-stu-id="04192-109">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04192-110">篩選介面</span><span class="sxs-lookup"><span data-stu-id="04192-110">Filter Interfaces</span></span>                        | <span data-ttu-id="04192-111">[**IAMVideoDecimationProperties**](/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties)、 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [**IKsPropertySet**](ikspropertyset.md)、 [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop)、 [**IVPManager**](/windows/desktop/api/Strmif/nn-strmif-ivpmanager)</span><span class="sxs-lookup"><span data-stu-id="04192-111">[**IAMVideoDecimationProperties**](/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IKsPropertySet**](ikspropertyset.md), [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop), [**IVPManager**](/windows/desktop/api/Strmif/nn-strmif-ivpmanager)</span></span> |
| <span data-ttu-id="04192-112">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="04192-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="04192-113">媒體媒體 \_ 、MEDIASUBTYPE \_ VPVIDEO 或 MEDIASUBTYPE \_ VPVBI、FORMAT \_ None</span><span class="sxs-lookup"><span data-stu-id="04192-113">MEDIATYPE\_Video, MEDIASUBTYPE\_VPVideo or MEDIASUBTYPE\_VPVBI, FORMAT\_None</span></span>                                                                                                                                         |
| <span data-ttu-id="04192-114">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="04192-114">Input Pin Interfaces</span></span>                     | <span data-ttu-id="04192-115">[**IKsPin**](ikspin.md)、 [**IKsPropertySet**](ikspropertyset.md)、 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="04192-115">[**IKsPin**](ikspin.md), [**IKsPropertySet**](ikspropertyset.md), [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="04192-116">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="04192-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="04192-117">媒體媒體 \_ ，格式 \_ VideoInfo2</span><span class="sxs-lookup"><span data-stu-id="04192-117">MEDIATYPE\_Video, FORMAT\_VideoInfo2</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="04192-118">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="04192-118">Output Pin Interfaces</span></span>                    | <span data-ttu-id="04192-119">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="04192-119">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                                     |
| <span data-ttu-id="04192-120">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="04192-120">Filter CLSID</span></span>                             | <span data-ttu-id="04192-121">CLSID \_ VideoPortManager</span><span class="sxs-lookup"><span data-stu-id="04192-121">CLSID\_VideoPortManager</span></span>                                                                                                                                                                                              |
| [<span data-ttu-id="04192-122">優點</span><span class="sxs-lookup"><span data-stu-id="04192-122">Merit</span></span>](merit.md)                       | <span data-ttu-id="04192-123">一般的業績 \_</span><span class="sxs-lookup"><span data-stu-id="04192-123">MERIT\_NORMAL</span></span>                                                                                                                                                                                                        |
| [<span data-ttu-id="04192-124">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="04192-124">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="04192-125">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="04192-125">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="04192-126">備註</span><span class="sxs-lookup"><span data-stu-id="04192-126">Remarks</span></span>

<span data-ttu-id="04192-127">影片埠管理員會結合覆迭 [混音器篩選器](overlay-mixer-filter.md) 的影片埠功能，以及 [VBI 介面](vbi-surface-allocator.md)配置器的功能。</span><span class="sxs-lookup"><span data-stu-id="04192-127">The Video Port Manager combines the video port functionality of the [Overlay Mixer Filter](overlay-mixer-filter.md) and the functionality of the [VBI Surface Allocator](vbi-surface-allocator.md).</span></span> <span data-ttu-id="04192-128">VPM 會配置影片埠和表面，並從影片埠同步處理資料捕獲。</span><span class="sxs-lookup"><span data-stu-id="04192-128">The VPM allocates video ports and surfaces, and synchronizes data capture from the video port.</span></span> <span data-ttu-id="04192-129">它允許獨立于轉譯的影片埠型捕捉。</span><span class="sxs-lookup"><span data-stu-id="04192-129">It allows video port-based capture that is independent of rendering.</span></span> <span data-ttu-id="04192-130">如果需要預覽，VPM 會與 VMR-7 協調以顯示已捕獲的影片埠資料。</span><span class="sxs-lookup"><span data-stu-id="04192-130">If preview is desired, the VPM coordinates with the VMR-7 to display captured video port data.</span></span> <span data-ttu-id="04192-131">當系統上有影片埠時，capture 篩選器需要額外的緩衝區，才能從影片串流中解壓縮 VBI 資料。</span><span class="sxs-lookup"><span data-stu-id="04192-131">When a video port is present on the system, the capture filter requires additional buffers to extract VBI data from the video stream.</span></span> <span data-ttu-id="04192-132">這些緩衝區是由 VPM 所提供。</span><span class="sxs-lookup"><span data-stu-id="04192-132">These buffers are provided by the VPM.</span></span> <span data-ttu-id="04192-133">一旦 capture 篩選器解壓縮了 VBI 資料之後，它就會在個別的 pin 上傳遞給像是 CC 解碼器的篩選。</span><span class="sxs-lookup"><span data-stu-id="04192-133">Once the capture filter has extracted the VBI data, it delivers it on a separate pin to filters such as the CC Decoder.</span></span> <span data-ttu-id="04192-134">下圖顯示篩選圖形中的 VPM 和其連接。</span><span class="sxs-lookup"><span data-stu-id="04192-134">The following illustration shows the VPM and its connections in a filter graph.</span></span>

![影片埠管理員篩選圖形區段](images/vpm.png)

<span data-ttu-id="04192-136">當系統上偵測到影片埠時，DVD 圖形產生器會自動將 VPM 新增至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="04192-136">The DVD Graph Builder adds the VPM to the filter graph automatically when a video port is detected on the system.</span></span> <span data-ttu-id="04192-137">新增至圖形後，VPM 會使用由影片混合轉譯器所提供的 DirectDraw 物件來配置兩個或三個表面。</span><span class="sxs-lookup"><span data-stu-id="04192-137">Once added to the graph, the VPM uses a DirectDraw object provided by the Video Mixing Renderer to allocate two or three surfaces.</span></span> <span data-ttu-id="04192-138">這些表面會從上游捕捉篩選器接收數位化的框架。</span><span class="sxs-lookup"><span data-stu-id="04192-138">These surfaces receive the digitized frames from the upstream capture filter.</span></span> <span data-ttu-id="04192-139">當介面中有資料時，為了回應傳送的使用者模式事件通知，VPM 會自動 array.blit 至 VMR 提供的螢幕外介面。</span><span class="sxs-lookup"><span data-stu-id="04192-139">In response to user-mode event notifications sent when data is present in the surface, the VPM performs an automatic blit to an offscreen surface provided by the VMR.</span></span>

<span data-ttu-id="04192-140">VPM 針對輸入緩衝區使用多個介面的事實，表示它需要比上一個 DirectShow 影片埠執行更多的 VRAM。</span><span class="sxs-lookup"><span data-stu-id="04192-140">The fact that the VPM uses multiple surfaces for its input buffers means that it requires more VRAM than the previous DirectShow video port implementation.</span></span> <span data-ttu-id="04192-141">從 VPM 到 VMR-7 的額外 array.blit 需要額外的視訊記憶體頻寬。</span><span class="sxs-lookup"><span data-stu-id="04192-141">The extra blit from the VPM to the VMR-7 requires additional video memory bandwidth.</span></span> <span data-ttu-id="04192-142">由於硬體自動翻轉未再使用，因此理論上可能會捨棄框架，但經驗辨識項建議您不會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="04192-142">And since hardware auto-flipping is not used any longer, there is a theoretical potential for dropped frames, but the empirical evidence suggests that this does not occur.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04192-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="04192-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04192-144">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="04192-144">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="04192-145">**IVPManager 介面**</span><span class="sxs-lookup"><span data-stu-id="04192-145">**IVPManager Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivpmanager)
</dt> </dl>

 

 



