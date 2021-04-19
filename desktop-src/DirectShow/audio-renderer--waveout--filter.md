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
# <a name="audio-renderer-waveout-filter"></a>音訊轉譯器 (WaveOut) 篩選

此篩選器會使用 waveOut \* API 來呈現波形音訊。 不過， [DirectSound 轉譯器篩選器](directsound-renderer-filter.md) 會使用 DirectSound 來提供相同的功能。 依預設，篩選圖形管理員會使用 DirectSound 轉譯器，而不是此篩選器。 音訊混合在 waveOut 音訊轉譯器中已停用，因此，如果您需要在播放期間混合多個音訊串流，請使用 DirectSound 轉譯器。

此篩選準則不會檢查音訊資料流程的子類型。 以格式傳遞的 [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) 或 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構包含連接所需的資訊。

此篩選器支援相依于音訊驅動程式的一系列樣本速率。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>篩選介面</td>
<td><ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li>
<li><a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a></li>
<li><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></li>
<li>IPersistPropertyBag</li>
<li>IPersistStream</li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>輸入 Pin 媒體類型</td>
<td><strong>MEDIATYPE_Audio</strong></td>
</tr>
<tr class="odd">
<td>輸入 Pin 介面</td>
<td><ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>輸出 Pin 媒體類型</td>
<td>不適用。</td>
</tr>
<tr class="odd">
<td>輸出 Pin 介面</td>
<td>不適用。</td>
</tr>
<tr class="even">
<td>篩選 CLSID</td>
<td><strong>CLSID_AudioRender</strong></td>
</tr>
<tr class="odd">
<td>屬性頁 CLSID</td>
<td><strong>CLSID_AudioProperties</strong>， <strong>CLSID_AudioRendererAdvancedProperties</strong></td>
</tr>
<tr class="even">
<td>可執行檔</td>
<td>quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">優點</a></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">篩選準則分類</a></td>
<td><strong>CLSID_AudioRendererCategory</strong></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> </dl>

 

 
