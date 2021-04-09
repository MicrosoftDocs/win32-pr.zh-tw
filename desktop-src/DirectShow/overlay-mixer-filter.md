---
description: 重疊 Mixer 篩選器
ms.assetid: e80938b7-31f0-467b-a3fa-c4511d14758d
title: 重疊 Mixer 篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26ad8ba8a41a1cdb94eec0f4406c4845f25cda5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845744"
---
# <a name="overlay-mixer-filter"></a><span data-ttu-id="f8955-103">重疊 Mixer 篩選器</span><span class="sxs-lookup"><span data-stu-id="f8955-103">Overlay Mixer Filter</span></span>

<span data-ttu-id="f8955-104">覆迭混音器篩選器是一種影片轉譯器，專為 DVD 播放和廣播影片串流（具有第21行的隱藏式輔助字幕）所設計。</span><span class="sxs-lookup"><span data-stu-id="f8955-104">The Overlay Mixer filter is a video renderer designed specifically for DVD playback and broadcast video streams with line-21 closed captioning.</span></span> <span data-ttu-id="f8955-105">重迭混音器也支援 (VPEs) 的影片埠擴充功能，讓它能夠使用硬體 MPEG-2 解碼器或類比 TV 調諧器，直接將影片傳送至圖形配接器，而不是透過 PCI 匯流排。</span><span class="sxs-lookup"><span data-stu-id="f8955-105">The Overlay Mixer also supports Video Port Extensions (VPEs), enabling it to work with hardware MPEG-2 decoders or analog TV tuners that send video directly to the graphics card, rather than over the PCI bus.</span></span>

> [!Note]  
> <span data-ttu-id="f8955-106">除非在 VPE 案例中，否則混合轉譯器 [9 的影片](video-mixing-renderer-filter-9.md) 現在優先于覆蓋混音器篩選器。</span><span class="sxs-lookup"><span data-stu-id="f8955-106">The [Video Mixing Renderer 9](video-mixing-renderer-filter-9.md) is now preferred over the Overlay Mixer filter, except in VPE scenarios.</span></span>

 

<span data-ttu-id="f8955-107">重迭混音器會使用 DirectDraw 來呈現。</span><span class="sxs-lookup"><span data-stu-id="f8955-107">The Overlay Mixer uses DirectDraw for rendering.</span></span> <span data-ttu-id="f8955-108">圖形配接器上需要有重迭表面。</span><span class="sxs-lookup"><span data-stu-id="f8955-108">It requires an overlay surface on the graphics card.</span></span> <span data-ttu-id="f8955-109">主要影片資料流程應連接到 pin 0。</span><span class="sxs-lookup"><span data-stu-id="f8955-109">The primary video stream should be connected to pin 0.</span></span> <span data-ttu-id="f8955-110">次要串流 (隱藏式輔助字幕圖形或 DVD subpictures) 連接到圖釘1和更新版本。</span><span class="sxs-lookup"><span data-stu-id="f8955-110">Secondary streams (closed caption graphics or DVD subpictures) are connected to pins 1 and higher.</span></span> <span data-ttu-id="f8955-111">重迭混音器會將次要資料流程直接 blits 至主要 suface;它不會混搭或使用 Alpha blend。</span><span class="sxs-lookup"><span data-stu-id="f8955-111">The Overlay Mixer blits the secondary streams directly onto the primary suface; it does not mix or alpha blend them.</span></span>

<span data-ttu-id="f8955-112">重迭混音器使用影片轉譯器進行視窗管理。</span><span class="sxs-lookup"><span data-stu-id="f8955-112">The Overlay Mixer uses the Video Renderer for window management.</span></span> <span data-ttu-id="f8955-113">影片轉譯器會連接到重迭混音器的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="f8955-113">The Video Renderer connects to the Overlay Mixer's output pin.</span></span>

<span data-ttu-id="f8955-114">當應用程式使用 [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) 和 [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) 介面建立圖形時，會自動將此篩選新增至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="f8955-114">This filter is added to the filter graph automatically when applications use the [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) and [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interfaces to create the graph.</span></span> <span data-ttu-id="f8955-115">篩選圖形管理員不會自動將重迭混音器新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="f8955-115">The Filter Graph Manager will not automatically add the Overlay Mixer to the graph.</span></span>

> [!Note]  
> <span data-ttu-id="f8955-116">在下表中，輸入 pin 0 上接受的媒體子類型與硬體相依。</span><span class="sxs-lookup"><span data-stu-id="f8955-116">In the following table, the media subtypes accepted on input pin 0 are hardware dependent.</span></span> <span data-ttu-id="f8955-117">覆迭混音器無法判斷是否支援特定的子類型，直到它建立 DirectDraw 介面為止。</span><span class="sxs-lookup"><span data-stu-id="f8955-117">The Overlay Mixer cannot determine whether a particular subtype is supported until it creates the DirectDraw surface.</span></span> <span data-ttu-id="f8955-118">因此，上游篩選器用來判斷是否支援子類型的唯一方法，是嘗試與該子類型的連接。</span><span class="sxs-lookup"><span data-stu-id="f8955-118">Therefore, the only way for an upstream filter to determine whether a subtype is supported is to attempt a connection with that subtype.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f8955-119">篩選介面</span><span class="sxs-lookup"><span data-stu-id="f8955-119">Filter Interfaces</span></span></td>
<td><span data-ttu-id="f8955-120"><a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a>、 <a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a>、 <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a>、 <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>、 <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify</strong></a>、 <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a></span><span class="sxs-lookup"><span data-stu-id="f8955-120"><a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a>, <a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify</strong></a>, <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8955-121">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="f8955-121">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="f8955-122">主要類型： MEDIATYPE_Video</span><span class="sxs-lookup"><span data-stu-id="f8955-122">Major Type: MEDIATYPE_Video</span></span><br/> <span data-ttu-id="f8955-123">亞：</span><span class="sxs-lookup"><span data-stu-id="f8955-123">Subtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="f8955-124">MEDIASUBTYPE_Overlay 只 (針腳 0) </span><span class="sxs-lookup"><span data-stu-id="f8955-124">MEDIASUBTYPE_Overlay (pin 0 only)</span></span></li>
<li><span data-ttu-id="f8955-125">DirectDraw YUV 格式 (僅限針腳 0) </span><span class="sxs-lookup"><span data-stu-id="f8955-125">DirectDraw YUV formats (pin 0 only)</span></span></li>
<li><span data-ttu-id="f8955-126">DirectDraw 影片加速格式 (僅限針腳 0) </span><span class="sxs-lookup"><span data-stu-id="f8955-126">DirectDraw Video Acceleration formats (pin 0 only)</span></span></li>
<li><span data-ttu-id="f8955-127"> (所有輸入圖釘的 DirectDraw RGB 格式) </span><span class="sxs-lookup"><span data-stu-id="f8955-127">DirectDraw RGB formats (all input pins)</span></span></li>
</ul>
<span data-ttu-id="f8955-128">格式類型：</span><span class="sxs-lookup"><span data-stu-id="f8955-128">Format Types:</span></span><br/>
<ul>
<li><span data-ttu-id="f8955-129">Format_VIDEOINFO</span><span class="sxs-lookup"><span data-stu-id="f8955-129">Format_VIDEOINFO</span></span></li>
<li><span data-ttu-id="f8955-130">Format_VIDEOINFO2</span><span class="sxs-lookup"><span data-stu-id="f8955-130">Format_VIDEOINFO2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8955-131">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="f8955-131">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="f8955-132"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>、 <a href="ikspin.md"><strong>IKsPin</strong></a>、 <a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig"><strong>IMixerPinConfig</strong></a>、 <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (引腳 0 only) 、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>、 <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify</strong></a>、 <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a></span><span class="sxs-lookup"><span data-stu-id="f8955-132"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>, <a href="ikspin.md"><strong>IKsPin</strong></a>, <a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig"><strong>IMixerPinConfig</strong></a>, <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (pin 0 only), <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify</strong></a>, <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8955-133">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="f8955-133">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="f8955-134">MEDIATYPE_Video，MEDIASUBTYPE_Overlay</span><span class="sxs-lookup"><span data-stu-id="f8955-134">MEDIATYPE_Video, MEDIASUBTYPE_Overlay</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8955-135">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="f8955-135">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="f8955-136"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="f8955-136"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8955-137">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="f8955-137">Filter CLSID</span></span></td>
<td><span data-ttu-id="f8955-138">CLSID_OverlayMixer</span><span class="sxs-lookup"><span data-stu-id="f8955-138">CLSID_OverlayMixer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8955-139">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="f8955-139">Property Page CLSID</span></span></td>
<td><span data-ttu-id="f8955-140">沒有屬性頁。</span><span class="sxs-lookup"><span data-stu-id="f8955-140">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8955-141">可執行檔</span><span class="sxs-lookup"><span data-stu-id="f8955-141">Executable</span></span></td>
<td><span data-ttu-id="f8955-142">qdvd.dll</span><span class="sxs-lookup"><span data-stu-id="f8955-142">qdvd.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8955-143"><a href="merit.md">優點</a></span><span class="sxs-lookup"><span data-stu-id="f8955-143"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="f8955-144">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="f8955-144">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8955-145"><a href="filter-categories.md">篩選準則分類</a></span><span class="sxs-lookup"><span data-stu-id="f8955-145"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="f8955-146">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="f8955-146">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="remarks"></a><span data-ttu-id="f8955-147">備註</span><span class="sxs-lookup"><span data-stu-id="f8955-147">Remarks</span></span>

<span data-ttu-id="f8955-148">重迭混音器會使用目的色彩金鑰組合來混合具有重迭的影片表面。</span><span class="sxs-lookup"><span data-stu-id="f8955-148">The Overlay Mixer uses destination color keying to mix video surfaces with overlays.</span></span> <span data-ttu-id="f8955-149">它會將色彩索引鍵和次要影片 blits 至主要表面，並將主要影片傳送至重迭表面。</span><span class="sxs-lookup"><span data-stu-id="f8955-149">It blits the color key and the secondary video to the primary surface, and sends the primary video to the overlay surface.</span></span> <span data-ttu-id="f8955-150">然後，圖形配接器會將這兩個表面合成至其框架緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f8955-150">The graphics card then composites the two surfaces into its frame buffer.</span></span>

<span data-ttu-id="f8955-151">若要測試圖形驅動程式是否支援硬體重迭，請呼叫 **IDirectDraw7：： GetCaps**。</span><span class="sxs-lookup"><span data-stu-id="f8955-151">To test whether the graphics driver supports hardware overlay, call **IDirectDraw7::GetCaps**.</span></span> <span data-ttu-id="f8955-152">如果 **DDCAPS** 結構中的 **dwMaxVisibleOverlays** 欄位大於零，驅動程式就會支援硬體重迭。</span><span class="sxs-lookup"><span data-stu-id="f8955-152">If the **dwMaxVisibleOverlays** field in the **DDCAPS** structure is greater than zero, the driver supports hardware overlay.</span></span>

<span data-ttu-id="f8955-153">應用程式可以透過 [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2) 介面控制重迭混音器上的一些行為。</span><span class="sxs-lookup"><span data-stu-id="f8955-153">Applications can control some behaviors on the Overlay Mixer through the [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2) interface.</span></span> <span data-ttu-id="f8955-154">遊戲開發人員可以使用重迭混音器，以 DirectDraw 獨佔模式顯示影片，如本節稍後所述。</span><span class="sxs-lookup"><span data-stu-id="f8955-154">Game developers can use the Overlay Mixer to display video in DirectDraw Exclusive Mode, as described later in this section.</span></span> <span data-ttu-id="f8955-155">不過， [影片混合轉譯器篩選器 9](video-mixing-renderer-filter-9.md) (VMR-9) 現在可為遊戲中的影片提供更好的支援。</span><span class="sxs-lookup"><span data-stu-id="f8955-155">The [Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9) now provides better support for video in games, however.</span></span> <span data-ttu-id="f8955-156">如需詳細資訊，請參閱 [使用影片混合](using-the-video-mixing-renderer.md)轉譯器。</span><span class="sxs-lookup"><span data-stu-id="f8955-156">For more information, see [Using the Video Mixing Renderer](using-the-video-mixing-renderer.md).</span></span>

<span data-ttu-id="f8955-157">下列資訊提供給篩選開發人員的優點，以及想要在 DirectDraw 獨佔模式中使用重迭混音器的遊戲開發人員。</span><span class="sxs-lookup"><span data-stu-id="f8955-157">The following information is provided for the benefit of filter developers, and game developers who want to use the Overlay Mixer in DirectDraw Exclusive Mode.</span></span>

<span data-ttu-id="f8955-158">**覆蓋混音器內部作業**</span><span class="sxs-lookup"><span data-stu-id="f8955-158">**Overlay Mixer Internal Operations**</span></span>

<span data-ttu-id="f8955-159">覆迭混音器會為每個傳入串流公開輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="f8955-159">The Overlay Mixer exposes an input pin for each incoming stream.</span></span> <span data-ttu-id="f8955-160">通常有三個輸入圖釘：適用于影片資料的 pin 0，以及第21行和 DVD 子圖片資料的針腳1和2。</span><span class="sxs-lookup"><span data-stu-id="f8955-160">Typically, there are three input pins: pin 0 for video data, and pins 1 and 2 for line 21 and DVD subpicture data.</span></span> <span data-ttu-id="f8955-161">就內部而言，重迭混音器會建立包含整個桌面之主要介面的 DirectDraw 物件，再加上矩形是由 Pin 0 上的影片資料流程大小定義的重迭表面。</span><span class="sxs-lookup"><span data-stu-id="f8955-161">Internally, the Overlay Mixer creates a DirectDraw object with a primary surface comprising the entire desktop, plus an overlay surface whose rectangle is defined by the size of the video stream on Pin 0.</span></span> <span data-ttu-id="f8955-162">如果此解碼器未指定色彩索引鍵，則重迭混音器會使用預設的色彩索引鍵：較新的圖形配接器為暗灰色，而針對較舊的256色卡則使用洋紅。</span><span class="sxs-lookup"><span data-stu-id="f8955-162">If the decoder does not specify a color key, the Overlay Mixer uses default color keys: dark gray for more recent graphics cards and magenta for older 256-color cards.</span></span>

> [!Note]  
> <span data-ttu-id="f8955-163">如果解碼器在重迭表面上的相同位置同時提供兩個次要影片串流，則結果為未定義。</span><span class="sxs-lookup"><span data-stu-id="f8955-163">The results are undefined if the decoder delivers two secondary video streams simultaneously in the same place on the overlay surface.</span></span> <span data-ttu-id="f8955-164"> (這種情況有時會發生在包含子圖片和第21行串流的 Dvd 中。 ) 影片可能會閃爍，或只顯示其中一個串流。</span><span class="sxs-lookup"><span data-stu-id="f8955-164">(This sometimes occurs with DVDs that contain subpicture and line 21 streams.) The video might flicker, or display only one of the streams.</span></span>

 

<span data-ttu-id="f8955-165">在 Windows Vista 或更新版本上，如果顯示器驅動程式支援硬體重迭，重迭混音器會停用桌面視窗管理員 (DWM) 組合。</span><span class="sxs-lookup"><span data-stu-id="f8955-165">On Windows Vista or later, the Overlay Mixer disables Desktop Window Manager (DWM) composition if the display driver supports hardware overlay.</span></span> <span data-ttu-id="f8955-166">應用程式應該避免使用覆迭混音器篩選;改為使用 VMR-9 或增強型影片轉譯器 (EVR) 。</span><span class="sxs-lookup"><span data-stu-id="f8955-166">Applications should avoid using the Overlay Mixer filter; use the VMR-9 or the Enhanced Video Renderer (EVR) instead.</span></span>

<span data-ttu-id="f8955-167">**使用影片解碼的上游連線**</span><span class="sxs-lookup"><span data-stu-id="f8955-167">**Upstream Connection with the Video Decoder**</span></span>

<span data-ttu-id="f8955-168">覆迭混音器的輸入接點通常會連接到上游視頻解碼器。</span><span class="sxs-lookup"><span data-stu-id="f8955-168">Typically the Overlay Mixer's input pins connect to an upstream video decoder.</span></span> <span data-ttu-id="f8955-169">主要影片串流必須連接到 pin 0。</span><span class="sxs-lookup"><span data-stu-id="f8955-169">The primary video stream must connect to the pin 0.</span></span> <span data-ttu-id="f8955-170">第21行或子圖片資料流程連接到 pin 1 或更大。</span><span class="sxs-lookup"><span data-stu-id="f8955-170">The line 21 or subpicture streams connect to pin 1 or greater.</span></span> <span data-ttu-id="f8955-171">如果解碼器是僅使用主機 CPU 的軟體解碼器，則解碼器與 Pin 0 之間的連接是 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 連接。</span><span class="sxs-lookup"><span data-stu-id="f8955-171">If the decoder is a software decoder that uses the host CPU exclusively, the connection between the decoder and the Pin 0 is an [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) connection.</span></span> <span data-ttu-id="f8955-172">如果此解碼器使用硬體加速，則 Pin 0 的連接必須使用 [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) 介面。</span><span class="sxs-lookup"><span data-stu-id="f8955-172">If the decoder uses hardware acceleration, the connection to Pin 0 must use the [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) inferface.</span></span> <span data-ttu-id="f8955-173">這兩種連線類型互斥。</span><span class="sxs-lookup"><span data-stu-id="f8955-173">These two types of connections are mutually exclusive.</span></span>

<span data-ttu-id="f8955-174">如果此解碼器直接繪製在重迭表面上，它應該使用 pin 0 上的 [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) 介面，並執行 [**IOverlayNotify**](/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify) 介面。</span><span class="sxs-lookup"><span data-stu-id="f8955-174">If the decoder draws directly onto the overlay surface, it should use the [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) interface on pin 0 and implement the [**IOverlayNotify**](/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify) interface.</span></span>

<span data-ttu-id="f8955-175">透過影片埠包裝硬體解碼器並聯機到重迭混音器的篩選器，必須執行 [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) 介面。</span><span class="sxs-lookup"><span data-stu-id="f8955-175">Filters that wrap a hardware decoder and connect to the Overlay Mixer through a video port must implement the [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) interface.</span></span> <span data-ttu-id="f8955-176">覆迭混音器會實 [**IVPNotify**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) 介面。</span><span class="sxs-lookup"><span data-stu-id="f8955-176">The Overlay Mixer implements the [**IVPNotify**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) interface.</span></span> <span data-ttu-id="f8955-177">這兩個介面可讓您指定所需的重迭表面，並可讓重迭混音器將這些表面的位置，告知其在視訊記憶體中的位置。</span><span class="sxs-lookup"><span data-stu-id="f8955-177">These two interfaces enable the decoder to specify the overlay surfaces it requires, and they enable the Overlay Mixer to inform the decoder of the location of those surfaces in video memory.</span></span>

<span data-ttu-id="f8955-178">重迭混音器也可確保正確地縮放影片矩形。</span><span class="sxs-lookup"><span data-stu-id="f8955-178">The Overlay Mixer also ensures that the video rectangle is scaled correctly.</span></span> <span data-ttu-id="f8955-179">影片捕獲牽涉到調整預覽影像和捕捉交錯的影片畫面方面的特定問題。</span><span class="sxs-lookup"><span data-stu-id="f8955-179">Video capture involves certain issues with respect to scaling the preview image and capturing interleaved video frames.</span></span> <span data-ttu-id="f8955-180">如果您正在開發硬體影片捕獲裝置的篩選或 WDM 驅動程式，請參閱 [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) 和 [**IVPNotify**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) 參考頁面，以取得有關這些主題的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f8955-180">If you are developing a filter or WDM driver for a hardware video capture device, refer to the [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) and [**IVPNotify**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) reference pages for more information on these topics.</span></span>

<span data-ttu-id="f8955-181">1394或 USB 捕獲案例中不會使用覆迭混音器。</span><span class="sxs-lookup"><span data-stu-id="f8955-181">The Overlay Mixer is not used in 1394 or USB capture scenarios.</span></span> <span data-ttu-id="f8955-182">它會透過 PCI 匯流排在影片捕獲中使用。</span><span class="sxs-lookup"><span data-stu-id="f8955-182">It is used in video capture over the PCI bus.</span></span>

<span data-ttu-id="f8955-183">**使用影片轉譯器的下游連接**</span><span class="sxs-lookup"><span data-stu-id="f8955-183">**Downstream Connection with the Video Renderer**</span></span>

<span data-ttu-id="f8955-184">重迭混音器有連接到 [影片](video-renderer-filter.md) 轉譯器篩選器的輸出 pin。</span><span class="sxs-lookup"><span data-stu-id="f8955-184">The Overlay Mixer has an output pin that connects to the [Video Renderer](video-renderer-filter.md) filter.</span></span> <span data-ttu-id="f8955-185">在此情況下，影片轉譯器不會轉譯影片;它只會管理影片視窗。</span><span class="sxs-lookup"><span data-stu-id="f8955-185">The Video Renderer in this case does not render the video; it simply manages the video window.</span></span>

<span data-ttu-id="f8955-186">Pin 連接會使用 [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) 介面，而不是 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面。</span><span class="sxs-lookup"><span data-stu-id="f8955-186">The pin connection uses the [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) interface rather than the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span> <span data-ttu-id="f8955-187">影片轉譯器會透過重迭混音器，將其視窗控制碼傳遞至 DirectDraw，以管理矩形剪輯。</span><span class="sxs-lookup"><span data-stu-id="f8955-187">The Video Renderer passes its window handle through the Overlay Mixer to DirectDraw, which manages the rectangle clipping.</span></span> <span data-ttu-id="f8955-188">應用程式可以透過篩選圖形管理員上的 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 和 [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2) 介面，控制影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="f8955-188">Applications can control the Video Renderer through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) and [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2) interfaces on the Filter Graph Manager.</span></span>

<span data-ttu-id="f8955-189">**DirectDraw 獨佔模式**</span><span class="sxs-lookup"><span data-stu-id="f8955-189">**DirectDraw Exclusive Mode**</span></span>

<span data-ttu-id="f8955-190">覆迭混音器的 DirectDraw 獨佔模式可讓遊戲在螢幕的某個部分顯示影片。</span><span class="sxs-lookup"><span data-stu-id="f8955-190">The Overlay Mixer's DirectDraw exclusive mode enables games to display video on some part of the screen.</span></span> <span data-ttu-id="f8955-191">在此模式中，重迭混音器會將影片直接轉譯為遊戲應用程式所建立的 DirectDraw 介面，而不是影片轉譯器所提供的視窗。</span><span class="sxs-lookup"><span data-stu-id="f8955-191">In this mode, the Overlay Mixer renders the video directly to a DirectDraw surface created by the game application, rather than to a window provided by the Video Renderer.</span></span> <span data-ttu-id="f8955-192">這可讓遊戲控制色彩索引鍵。</span><span class="sxs-lookup"><span data-stu-id="f8955-192">This enables games to control the color key.</span></span> <span data-ttu-id="f8955-193">覆迭混音器只會在 DirectDraw 獨佔模式中公開一個輸入 pin，這表示無法在此模式下執行行21或 DVD 子圖片。</span><span class="sxs-lookup"><span data-stu-id="f8955-193">The Overlay Mixer exposes only one input pin in DirectDraw exclusive mode, which means that no mixing of Line 21 or DVD subpicture can be performed in this mode.</span></span>

<span data-ttu-id="f8955-194">若要在 DirectDraw 獨佔模式中使用覆迭混音器，請建立重迭混音器的實例，並在建立篩選圖形之前，對 [**IDDrawExclModeVideo**](/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo) 介面進行查詢。</span><span class="sxs-lookup"><span data-stu-id="f8955-194">To use the Overlay Mixer in DirectDraw exclusive mode, create an instance of the Overlay Mixer and query it for the [**IDDrawExclModeVideo**](/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo) interface before building the filter graph.</span></span> <span data-ttu-id="f8955-195">然後呼叫 [**IDDrawExclModeVideo：： SetDDrawSurface**](/windows/desktop/api/Strmif/nf-strmif-iddrawexclmodevideo-setddrawsurface) 來指定用於轉譯的 DirectDraw 介面。</span><span class="sxs-lookup"><span data-stu-id="f8955-195">Then call [**IDDrawExclModeVideo::SetDDrawSurface**](/windows/desktop/api/Strmif/nf-strmif-iddrawexclmodevideo-setddrawsurface) to specify the DirectDraw surface for rendering.</span></span> <span data-ttu-id="f8955-196">這種模式的一個重大限制是，遊戲無法存取實際的影片位。</span><span class="sxs-lookup"><span data-stu-id="f8955-196">One significant limitation of this mode is that the game does not get access to the actual video bits.</span></span> <span data-ttu-id="f8955-197">如果您使用 **IDDrawExclModeVideo**，您的應用程式會建立主要介面，而重迭混音器會建立重迭表面。</span><span class="sxs-lookup"><span data-stu-id="f8955-197">If you use **IDDrawExclModeVideo**, your application creates the primary surface, and the Overlay Mixer creates the overlay surface.</span></span>

<span data-ttu-id="f8955-198">您也可以使用 DirectDraw 專屬模式來執行無視窗轉譯（例如，在網頁中），但不建議這樣做，因為覆迭混音器不會在此模式中執行任何混合。</span><span class="sxs-lookup"><span data-stu-id="f8955-198">You can also use DirectDraw exclusive mode to perform windowless rendering—for example, in a Web page—but this is not recommended, because the Overlay Mixer does not perform any mixing in this mode.</span></span> <span data-ttu-id="f8955-199">這表示不會顯示任何行21或子圖片資料。</span><span class="sxs-lookup"><span data-stu-id="f8955-199">This means that no line 21 or subpicture data can be displayed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8955-200">相關主題</span><span class="sxs-lookup"><span data-stu-id="f8955-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8955-201">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="f8955-201">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




