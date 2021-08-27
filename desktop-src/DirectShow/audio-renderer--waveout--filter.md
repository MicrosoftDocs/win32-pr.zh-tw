---
description: 音訊轉譯器 (WaveOut) 篩選
ms.assetid: a3f2776b-974b-4886-82a3-38e00b607a07
title: 音訊轉譯器 (WaveOut) 篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eef79acb21221c1a0b91efc2da67773534fe54ca
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470155"
---
# <a name="audio-renderer-waveout-filter"></a>音訊轉譯器 (WaveOut) 篩選

此篩選器會使用 waveOut \* API 來呈現波形音訊。 不過， [DirectSound 轉譯器篩選器](directsound-renderer-filter.md) 會使用 DirectSound 來提供相同的功能。 根據預設，篩選 Graph 管理員會使用 DirectSound 轉譯器，而不是此篩選器。 音訊混合在 waveOut 音訊轉譯器中已停用，因此，如果您需要在播放期間混合多個音訊串流，請使用 DirectSound 轉譯器。

此篩選準則不會檢查音訊資料流程的子類型。 以格式傳遞的 [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) 或 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構包含連接所需的資訊。

此篩選器支援相依于音訊驅動程式的一系列樣本速率。




| | |篩選介面 | <ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></li><li>IPersistPropertyBag</li><li>IPersistStream</li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></li></ul> | |輸入 Pin 媒體類型 | <strong>MEDIATYPE_Audio</strong> | |輸入 Pin 介面 | <ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li></ul> | |輸出釘選媒體類型 |不適用。 | |輸出 Pin 介面 |不適用。 | |篩選 CLSID |<strong>CLSID_AudioRender</strong> | |屬性頁 CLSID |<strong>CLSID_AudioProperties</strong>， <strong>CLSID_AudioRendererAdvancedProperties</strong> | |可執行檔 |quartz.dll | |<a href="merit.md">業績</a>  | <strong>MERIT_DO_NOT_USE</strong> | |<a href="filter-categories.md">篩選準則分類</a>  | <strong>CLSID_AudioRendererCategory</strong> | 




 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

 

 
