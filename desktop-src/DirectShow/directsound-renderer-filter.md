---
description: DirectSound 轉譯器篩選
ms.assetid: ec6cc790-8c1f-4de4-a7ca-a7073894380e
title: DirectSound 轉譯器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae932340ea22213e0f9d7234599742d74208f632
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108504"
---
# <a name="directsound-renderer-filter"></a><span data-ttu-id="015f6-103">DirectSound 轉譯器篩選</span><span class="sxs-lookup"><span data-stu-id="015f6-103">DirectSound Renderer Filter</span></span>

<span data-ttu-id="015f6-104">此篩選器會使用 DirectSound 來呈現音訊。</span><span class="sxs-lookup"><span data-stu-id="015f6-104">This filter renders audio using DirectSound.</span></span> <span data-ttu-id="015f6-105">此篩選器目前為波形音效的預設音訊轉譯器。</span><span class="sxs-lookup"><span data-stu-id="015f6-105">This filter is currently the default audio renderer for waveform sound.</span></span>

<span data-ttu-id="015f6-106">除了其基本的音效轉譯功能之外，此篩選器還可以處理 DirectSound API 呼叫。</span><span class="sxs-lookup"><span data-stu-id="015f6-106">In addition to its basic sound-rendering capabilities, this filter can process DirectSound API calls.</span></span> <span data-ttu-id="015f6-107">您可以使用 [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) 方法來設定和取出將處理音效播放的視窗。</span><span class="sxs-lookup"><span data-stu-id="015f6-107">Use the [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) methods to set and retrieve the window that will handle the sound playback.</span></span> <span data-ttu-id="015f6-108">DirectSound 音訊轉譯器是適用于 DirectShow 的預設音訊轉譯篩選器。</span><span class="sxs-lookup"><span data-stu-id="015f6-108">The DirectSound Audio Renderer is the default audio rendering filter for DirectShow.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="015f6-109">篩選介面</span><span class="sxs-lookup"><span data-stu-id="015f6-109">Filter Interfaces</span></span></td>
<td><span data-ttu-id="015f6-110"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a>、 <a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、 <a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a>、 <strong>IDirectSound3DBuffer</strong>、 <strong>IDirectSound3dListener</strong>、 <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span><span class="sxs-lookup"><span data-stu-id="015f6-110"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a>, <a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a>, <strong>IDirectSound3DBuffer</strong>, <strong>IDirectSound3dListener</strong>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="015f6-111">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="015f6-111">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="015f6-112">主要類型： MEDIATYPE_AudioSubtypes：</span><span class="sxs-lookup"><span data-stu-id="015f6-112">Major Type: MEDIATYPE_AudioSubtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="015f6-113">MEDIASUBTYPE_PCM</span><span class="sxs-lookup"><span data-stu-id="015f6-113">MEDIASUBTYPE_PCM</span></span></li>
<li><span data-ttu-id="015f6-114">MEDIASUBTYPE_IEEE_FLOAT</span><span class="sxs-lookup"><span data-stu-id="015f6-114">MEDIASUBTYPE_IEEE_FLOAT</span></span></li>
<li><span data-ttu-id="015f6-115">MEDIASUBTYPE_DOLBY_AC3_SPDIF</span><span class="sxs-lookup"><span data-stu-id="015f6-115">MEDIASUBTYPE_DOLBY_AC3_SPDIF</span></span></li>
<li><span data-ttu-id="015f6-116">MEDIASUBTYPE_RAW_SPORT</span><span class="sxs-lookup"><span data-stu-id="015f6-116">MEDIASUBTYPE_RAW_SPORT</span></span></li>
<li><span data-ttu-id="015f6-117">MEDIASUBTYPE_SPDIF_TAG_241h</span><span class="sxs-lookup"><span data-stu-id="015f6-117">MEDIASUBTYPE_SPDIF_TAG_241h</span></span></li>
<li><span data-ttu-id="015f6-118">MEDIASUBTYPE_DRM_Audio</span><span class="sxs-lookup"><span data-stu-id="015f6-118">MEDIASUBTYPE_DRM_Audio</span></span></li>
</ul>
<span data-ttu-id="015f6-119">格式類型： FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="015f6-119">Format type: FORMAT_WaveFormatEx</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="015f6-120">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="015f6-120">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="015f6-121"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="015f6-121"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="015f6-122">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="015f6-122">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="015f6-123">不適用。</span><span class="sxs-lookup"><span data-stu-id="015f6-123">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="015f6-124">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="015f6-124">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="015f6-125">不適用。</span><span class="sxs-lookup"><span data-stu-id="015f6-125">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="015f6-126">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="015f6-126">Filter CLSID</span></span></td>
<td><span data-ttu-id="015f6-127">CLSID_DSoundRender</span><span class="sxs-lookup"><span data-stu-id="015f6-127">CLSID_DSoundRender</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="015f6-128">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="015f6-128">Property Page CLSID</span></span></td>
<td><span data-ttu-id="015f6-129">CLSID_AudioProperties，CLSID_AudioRendererAdvancedProperties</span><span class="sxs-lookup"><span data-stu-id="015f6-129">CLSID_AudioProperties, CLSID_AudioRendererAdvancedProperties</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="015f6-130">可執行檔</span><span class="sxs-lookup"><span data-stu-id="015f6-130">Executable</span></span></td>
<td><span data-ttu-id="015f6-131">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="015f6-131">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="015f6-132"><a href="merit.md">優點</a></span><span class="sxs-lookup"><span data-stu-id="015f6-132"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="015f6-133">MERIT_PREFERRED</span><span class="sxs-lookup"><span data-stu-id="015f6-133">MERIT_PREFERRED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="015f6-134"><a href="filter-categories.md">篩選準則分類</a></span><span class="sxs-lookup"><span data-stu-id="015f6-134"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="015f6-135">CLSID_AudioRendererCategory</span><span class="sxs-lookup"><span data-stu-id="015f6-135">CLSID_AudioRendererCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="015f6-136">備註</span><span class="sxs-lookup"><span data-stu-id="015f6-136">Remarks</span></span>

<span data-ttu-id="015f6-137">此篩選準則會作為音訊裝置的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="015f6-137">This filter acts as a wrapper for an audio device.</span></span> <span data-ttu-id="015f6-138">若要列舉使用者系統上可用的音訊裝置，請使用 [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) 介面搭配音訊轉譯器類別 (CLSID \_ AudioRendererCategory) 。</span><span class="sxs-lookup"><span data-stu-id="015f6-138">To enumerate the audio devices available on the user's system, use the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface with the audio renderer category (CLSID\_AudioRendererCategory).</span></span> <span data-ttu-id="015f6-139">針對每個音訊裝置，音訊轉譯器類別包含兩個篩選準則實例。</span><span class="sxs-lookup"><span data-stu-id="015f6-139">For each audio device, the audio renderer category contains two filter instances.</span></span> <span data-ttu-id="015f6-140">其中一個對應至 DirectSound 轉譯器，另一個對應至音訊轉譯器 [ (WaveOut) ](audio-renderer--waveout--filter.md) 篩選。</span><span class="sxs-lookup"><span data-stu-id="015f6-140">One of these corresponds to the DirectSound Renderer, and the other corresponds to the [Audio Renderer (WaveOut)](audio-renderer--waveout--filter.md) filter.</span></span> <span data-ttu-id="015f6-141">DirectSound 實例的易記名稱為 "DirectSound： *DeviceName*"，其中 *DeviceName* 是裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="015f6-141">The DirectSound instance has the friendly name "DirectSound: *DeviceName*," where *DeviceName* is the name of the device.</span></span> <span data-ttu-id="015f6-142">WaveOut 實例的易記名稱為 *DeviceName*。</span><span class="sxs-lookup"><span data-stu-id="015f6-142">The WaveOut instance has the friendly name *DeviceName*.</span></span>

<span data-ttu-id="015f6-143">音訊轉譯器類別包含兩個額外的篩選實例，名為「預設 DirectSound 裝置」和「預設 WaveOut 裝置」。</span><span class="sxs-lookup"><span data-stu-id="015f6-143">The audio renderer category contains two additional filter instances, named "Default DirectSound Device" and "Default WaveOut Device."</span></span> <span data-ttu-id="015f6-144">這些會對應至預設音效裝置，如使用者透過主控台所選擇。</span><span class="sxs-lookup"><span data-stu-id="015f6-144">These correspond to the default sound device, as chosen by the user through the Control Panel.</span></span> <span data-ttu-id="015f6-145">它們實際上是對應到上一段所述的其中一組。</span><span class="sxs-lookup"><span data-stu-id="015f6-145">They are actually mappings to one of the pairs described in the previous paragraph.</span></span> <span data-ttu-id="015f6-146">例如，如果系統有兩個音訊裝置（裝置 A 和裝置 B），音訊轉譯器類別會包含下列內容：</span><span class="sxs-lookup"><span data-stu-id="015f6-146">For example, if the system has two audio devices, Device A and Device B, the audio renderer category will contain the following:</span></span>

-   <span data-ttu-id="015f6-147">裝置 A</span><span class="sxs-lookup"><span data-stu-id="015f6-147">Device A</span></span>
-   <span data-ttu-id="015f6-148">DirectSound：裝置 A</span><span class="sxs-lookup"><span data-stu-id="015f6-148">DirectSound: Device A</span></span>
-   <span data-ttu-id="015f6-149">裝置 B</span><span class="sxs-lookup"><span data-stu-id="015f6-149">Device B</span></span>
-   <span data-ttu-id="015f6-150">DirectSound：裝置 B</span><span class="sxs-lookup"><span data-stu-id="015f6-150">DirectSound: Device B</span></span>
-   <span data-ttu-id="015f6-151">預設 DirectSound 裝置</span><span class="sxs-lookup"><span data-stu-id="015f6-151">Default DirectSound Device</span></span>
-   <span data-ttu-id="015f6-152">預設 WaveOut 裝置</span><span class="sxs-lookup"><span data-stu-id="015f6-152">Default WaveOut Device</span></span>

<span data-ttu-id="015f6-153">如果使用者選取裝置 A 作為預設裝置，則「預設 DirectSound 裝置」相當於「DirectSound：裝置 A」和「預設 WaveOut 裝置」相當於「裝置 A」。</span><span class="sxs-lookup"><span data-stu-id="015f6-153">If the user selected Device A as the default device, then "Default DirectSound Device" is equivalent to "DirectSound: Device A," and "Default WaveOut Device" is equivalent to "Device A."</span></span> <span data-ttu-id="015f6-154">如果使用者選取裝置 B 作為預設裝置，這些對應將會變更。</span><span class="sxs-lookup"><span data-stu-id="015f6-154">If the user selects Device B as the default device, these mappings will change.</span></span>

<span data-ttu-id="015f6-155">「預設 DirectSound 裝置」已獲派慣用的業績 \_ 。</span><span class="sxs-lookup"><span data-stu-id="015f6-155">"Default DirectSound Device" is assigned a merit of MERIT\_PREFERRED.</span></span> <span data-ttu-id="015f6-156">其他人則不會使用您的業績 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="015f6-156">The others have merit MERIT\_DO\_NOT\_USE.</span></span> <span data-ttu-id="015f6-157">因此，智慧型 Connect 一律會選擇預設的 DirectSound 裝置。</span><span class="sxs-lookup"><span data-stu-id="015f6-157">Therefore, Intelligent Connect will always choose the default DirectSound device.</span></span>

<span data-ttu-id="015f6-158">DirectSound 轉譯器篩選器可透過 DirectSound **IDirectSound3DBuffer** 和 **IDirectSound3dListener** 介面支援3d 音效。</span><span class="sxs-lookup"><span data-stu-id="015f6-158">The DirectSound Renderer filter supports 3D sound through the DirectSound **IDirectSound3DBuffer** and **IDirectSound3dListener** interfaces.</span></span> <span data-ttu-id="015f6-159">您也可以查詢這些介面的目前版本（ **IDirectSound3DBuffer8** 和 **IDirectSound3dListener8**）的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="015f6-159">You can also query the filter for the current versions of these interfaces, **IDirectSound3DBuffer8** and **IDirectSound3dListener8**.</span></span> <span data-ttu-id="015f6-160">在這些介面上呼叫方法之前，請先執行圖形。</span><span class="sxs-lookup"><span data-stu-id="015f6-160">Run the graph before calling methods on these interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="015f6-161">相關主題</span><span class="sxs-lookup"><span data-stu-id="015f6-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="015f6-162">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="015f6-162">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




