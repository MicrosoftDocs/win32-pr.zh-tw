---
description: DirectSound 轉譯器篩選
ms.assetid: ec6cc790-8c1f-4de4-a7ca-a7073894380e
title: DirectSound 轉譯器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e754c81ba9ac6d22141735ac1488218461d9ea63ef81f7bb947cb3e72fd81d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966318"
---
# <a name="directsound-renderer-filter"></a>DirectSound 轉譯器篩選

此篩選器會使用 DirectSound 來呈現音訊。 此篩選器目前為波形音效的預設音訊轉譯器。

除了其基本的音效轉譯功能之外，此篩選器還可以處理 DirectSound API 呼叫。 您可以使用 [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) 方法來設定和取出將處理音效播放的視窗。 DirectSound 音訊轉譯器是 DirectShow 的預設音訊轉譯篩選。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>篩選介面</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a>、 <a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、 <a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a>、 <strong>IDirectSound3DBuffer</strong>、 <strong>IDirectSound3dListener</strong>、 <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></td>
</tr>
<tr class="even">
<td>輸入 Pin 媒體類型</td>
<td>主要類型： MEDIATYPE_AudioSubtypes：<br/>
<ul>
<li>MEDIASUBTYPE_PCM</li>
<li>MEDIASUBTYPE_IEEE_FLOAT</li>
<li>MEDIASUBTYPE_DOLBY_AC3_SPDIF</li>
<li>MEDIASUBTYPE_RAW_SPORT</li>
<li>MEDIASUBTYPE_SPDIF_TAG_241h</li>
<li>MEDIASUBTYPE_DRM_Audio</li>
</ul>
格式類型： FORMAT_WaveFormatEx<br/></td>
</tr>
<tr class="odd">
<td>輸入 Pin 介面</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
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
<td>CLSID_DSoundRender</td>
</tr>
<tr class="odd">
<td>屬性頁 CLSID</td>
<td>CLSID_AudioProperties，CLSID_AudioRendererAdvancedProperties</td>
</tr>
<tr class="even">
<td>可執行檔</td>
<td>quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">優點</a></td>
<td>MERIT_PREFERRED</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">篩選準則分類</a></td>
<td>CLSID_AudioRendererCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>備註

此篩選準則會作為音訊裝置的包裝函式。 若要列舉使用者系統上可用的音訊裝置，請使用 [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) 介面搭配音訊轉譯器類別 (CLSID \_ AudioRendererCategory) 。 針對每個音訊裝置，音訊轉譯器類別包含兩個篩選準則實例。 其中一個對應至 DirectSound 轉譯器，另一個對應至音訊轉譯器 [ (WaveOut) ](audio-renderer--waveout--filter.md) 篩選。 DirectSound 實例的易記名稱為 "DirectSound： *DeviceName*"，其中 *DeviceName* 是裝置的名稱。 WaveOut 實例的易記名稱為 *DeviceName*。

音訊轉譯器類別包含兩個額外的篩選實例，名為「預設 DirectSound 裝置」和「預設 WaveOut 裝置」。 這些會對應至預設音效裝置，如使用者透過主控台所選擇。 它們實際上是對應到上一段所述的其中一組。 例如，如果系統有兩個音訊裝置（裝置 A 和裝置 B），音訊轉譯器類別會包含下列內容：

-   裝置 A
-   DirectSound：裝置 A
-   裝置 B
-   DirectSound：裝置 B
-   預設 DirectSound 裝置
-   預設 WaveOut 裝置

如果使用者選取裝置 A 作為預設裝置，則「預設 DirectSound 裝置」相當於「DirectSound：裝置 A」和「預設 WaveOut 裝置」相當於「裝置 A」。 如果使用者選取裝置 B 作為預設裝置，這些對應將會變更。

「預設 DirectSound 裝置」已獲派慣用的業績 \_ 。 其他人則不會使用您的業績 \_ \_ \_ 。 因此，智慧型連線一律會選擇預設的 DirectSound 裝置。

DirectSound 轉譯器篩選器可透過 DirectSound **IDirectSound3DBuffer** 和 **IDirectSound3dListener** 介面支援3d 音效。 您也可以查詢這些介面的目前版本（ **IDirectSound3DBuffer8** 和 **IDirectSound3dListener8**）的篩選準則。 在這些介面上呼叫方法之前，請先執行圖形。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

 

 




