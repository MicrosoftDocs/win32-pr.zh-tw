---
description: 音訊轉譯器 (WaveOut) 篩選
ms.assetid: a3f2776b-974b-4886-82a3-38e00b607a07
title: 音訊轉譯器 (WaveOut) 篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5f47018d22bcbbdcf884f5eb4356d1d0b3fe60d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971942"
---
# <a name="audio-renderer-waveout-filter"></a><span data-ttu-id="a42fd-103">音訊轉譯器 (WaveOut) 篩選</span><span class="sxs-lookup"><span data-stu-id="a42fd-103">Audio Renderer (WaveOut) Filter</span></span>

<span data-ttu-id="a42fd-104">此篩選器會使用 waveOut \* API 來呈現波形音訊。</span><span class="sxs-lookup"><span data-stu-id="a42fd-104">This filter uses the waveOut\* API to render waveform audio.</span></span> <span data-ttu-id="a42fd-105">不過， [DirectSound 轉譯器篩選器](directsound-renderer-filter.md) 會使用 DirectSound 來提供相同的功能。</span><span class="sxs-lookup"><span data-stu-id="a42fd-105">However, the [DirectSound Renderer Filter](directsound-renderer-filter.md) provides the same functionality using DirectSound.</span></span> <span data-ttu-id="a42fd-106">依預設，篩選圖形管理員會使用 DirectSound 轉譯器，而不是此篩選器。</span><span class="sxs-lookup"><span data-stu-id="a42fd-106">By default, the Filter Graph Manager uses the DirectSound Renderer instead of this filter.</span></span> <span data-ttu-id="a42fd-107">音訊混合在 waveOut 音訊轉譯器中已停用，因此，如果您需要在播放期間混合多個音訊串流，請使用 DirectSound 轉譯器。</span><span class="sxs-lookup"><span data-stu-id="a42fd-107">Audio mixing is disabled in the waveOut Audio Renderer, so if you need to mix multiple audio streams during playback, use the DirectSound renderer.</span></span>

<span data-ttu-id="a42fd-108">此篩選準則不會檢查音訊資料流程的子類型。</span><span class="sxs-lookup"><span data-stu-id="a42fd-108">This filter does not check the audio stream's subtype.</span></span> <span data-ttu-id="a42fd-109">以格式傳遞的 [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) 或 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構包含連接所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="a42fd-109">The [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) or [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure passed in the format contains the information needed for the connection.</span></span>

<span data-ttu-id="a42fd-110">此篩選器支援相依于音訊驅動程式的一系列樣本速率。</span><span class="sxs-lookup"><span data-stu-id="a42fd-110">This filter supports a range of sample rates that depends on the audio driver.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a42fd-111">篩選介面</span><span class="sxs-lookup"><span data-stu-id="a42fd-111">Filter Interfaces</span></span></td>
<td><ul>
<li><span data-ttu-id="a42fd-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a></span><span class="sxs-lookup"><span data-stu-id="a42fd-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a></span></span></li>
<li><span data-ttu-id="a42fd-113"><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a></span><span class="sxs-lookup"><span data-stu-id="a42fd-113"><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a></span></span></li>
<li><span data-ttu-id="a42fd-114"><a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a></span><span class="sxs-lookup"><span data-stu-id="a42fd-114"><a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a></span></span></li>
<li><span data-ttu-id="a42fd-115"><a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="a42fd-115"><a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a></span></span></li>
<li><span data-ttu-id="a42fd-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="a42fd-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="a42fd-117"><a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a></span><span class="sxs-lookup"><span data-stu-id="a42fd-117"><a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a></span></span></li>
<li><span data-ttu-id="a42fd-118"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></span><span class="sxs-lookup"><span data-stu-id="a42fd-118"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></span></span></li>
<li><span data-ttu-id="a42fd-119"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="a42fd-119"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></li>
<li><span data-ttu-id="a42fd-120">IPersistPropertyBag</span><span class="sxs-lookup"><span data-stu-id="a42fd-120">IPersistPropertyBag</span></span></li>
<li><span data-ttu-id="a42fd-121">IPersistStream</span><span class="sxs-lookup"><span data-stu-id="a42fd-121">IPersistStream</span></span></li>
<li><span data-ttu-id="a42fd-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="a42fd-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="a42fd-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span><span class="sxs-lookup"><span data-stu-id="a42fd-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a42fd-124">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="a42fd-124">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="a42fd-125"><strong>MEDIATYPE_Audio</strong></span><span class="sxs-lookup"><span data-stu-id="a42fd-125"><strong>MEDIATYPE_Audio</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a42fd-126">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="a42fd-126">Input Pin Interfaces</span></span></td>
<td><ul>
<li><span data-ttu-id="a42fd-127"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="a42fd-127"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
<li><span data-ttu-id="a42fd-128"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="a42fd-128"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="a42fd-129"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="a42fd-129"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a42fd-130">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="a42fd-130">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="a42fd-131">不適用。</span><span class="sxs-lookup"><span data-stu-id="a42fd-131">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a42fd-132">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="a42fd-132">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="a42fd-133">不適用。</span><span class="sxs-lookup"><span data-stu-id="a42fd-133">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a42fd-134">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="a42fd-134">Filter CLSID</span></span></td>
<td><span data-ttu-id="a42fd-135"><strong>CLSID_AudioRender</strong></span><span class="sxs-lookup"><span data-stu-id="a42fd-135"><strong>CLSID_AudioRender</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a42fd-136">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="a42fd-136">Property Page CLSID</span></span></td>
<td><span data-ttu-id="a42fd-137"><strong>CLSID_AudioProperties</strong>， <strong>CLSID_AudioRendererAdvancedProperties</strong></span><span class="sxs-lookup"><span data-stu-id="a42fd-137"><strong>CLSID_AudioProperties</strong>, <strong>CLSID_AudioRendererAdvancedProperties</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a42fd-138">可執行檔</span><span class="sxs-lookup"><span data-stu-id="a42fd-138">Executable</span></span></td>
<td><span data-ttu-id="a42fd-139">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="a42fd-139">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a42fd-140"><a href="merit.md">優點</a></span><span class="sxs-lookup"><span data-stu-id="a42fd-140"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="a42fd-141"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="a42fd-141"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a42fd-142"><a href="filter-categories.md">篩選準則分類</a></span><span class="sxs-lookup"><span data-stu-id="a42fd-142"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="a42fd-143"><strong>CLSID_AudioRendererCategory</strong></span><span class="sxs-lookup"><span data-stu-id="a42fd-143"><strong>CLSID_AudioRendererCategory</strong></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="a42fd-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="a42fd-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a42fd-145">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="a42fd-145">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 
