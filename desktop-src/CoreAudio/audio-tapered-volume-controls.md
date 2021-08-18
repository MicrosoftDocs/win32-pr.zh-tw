---
description: Audio-Tapered 的音量控制項
ms.assetid: 3b1adef5-40e9-4527-aa79-5a71f201fdfc
title: Audio-Tapered 的音量控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb4856b4f25ad33ae61e9cb250a6b84f0e8799bb9d11d33c1770593bcf3714a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750783"
---
# <a name="audio-tapered-volume-controls"></a>Audio-Tapered 的音量控制項

[**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)介面會管理音訊錐形的音量控制項。 這些控制項很適合用來 Windows 顯示音量滑杆的應用程式。 針對系結至音訊錐形音量控制項的音量滑杆，滑杆位置中的每個變更都會產生觀察音量的變更，與滑杆移動的距離成正比。 針對特定的旅遊距離，不論滑杆的移動是否出現在滑杆的移動範圍的下半部或中間部分，觀察音量增加或減少的數量大約相同。 觀察到的音量會隨著音訊信號電力的對數以線性方式大幅變化。

「 *音訊* 」一詞最初指的是 potentiometer 中電阻式元素的錐形圖形，用來做為音訊電器裝置中的音量控制項。 音訊錐形電阻式元素最寬于零磁片區的位置，最少則是最大的音量位置。 Potentiometer 會控制裝置透過其喇叭播放之音訊信號的電壓層級。 Tapering 的設計目的是要產生 potentiometer 雨刷啟動位置與喇叭上認知音量之間的大約線性關聯性。 雨刷啟動位置與喇叭的電壓之間的關聯性是非線性的。

相反地，具有線性錐度的電阻式元素在 potentiometer 雨刷啟動的移動範圍上具有統一的寬度。 如此一來，喇叭的電壓就會隨著雨刷啟動位置呈線性變化。 雨刷啟動位置與音量之間的關聯性是非線性的。

同樣地，顯示音量滑杆的 Windows 應用程式，會定義喇叭位置與喇叭之間的輸出信號層級之間的關聯性。 關聯性實際上可以是線性錐形或音訊錐形。

下圖顯示滑杆位置與輸出電壓的對應，以及線性錐形音量控制項的認知音量。

![線性錐形音量控制項的輸出圖表](images/taper1.jpg)

在上圖的左邊，音訊數位轉類比轉換器的輸出電壓層級 (DAC) 會以線性方式增加，因為音量滑杆會從其最小位置 () 標示為最大值的位置， (標示的最大) 。 垂直軸上的標籤 V<sub>FS</sub> 代表完整規模的 DAC 輸出電壓。

不過，觀察到的音量會隨著音訊信號的耗電量而有大約的對數，如先前圖表的右側所示。 因此，在接近最小值設定的間隔中，移動滑杆會導致觀察音量中有相當大的變更，但在相同寬度接近最大值的間隔中移動滑杆會導致觀察音量的變更變得相對較小。

在上圖的右側，垂直軸上的音量會以分貝 (dB) 相對於全形電源設定 (以0分貝) 。 音量曲線與垂直軸相交于減號無限大，但只有從0分貝到–96分貝的曲線部分才會出現在圖表中。 決定只顯示曲線的這個部分是很任意的，但96分貝可方便地代表16位 DAC 的最下層輸出層級（相對於完整規模的電源）的電源。 此值的計算方式為 20<sup>。</sup>記錄₁₀ (1/65535) 。

由於上圖中接近最小設定的滑杆位置較小變更會導致音量中的大型變更，因此使用者可能會發現該磁片區難以控制此區域。 相對較小的滑杆移動可以將磁片區的上方或低於所需的層級。 改良的音量控制項可提供滑杆位置和音量之間更線性的關聯性。

下圖顯示滑杆位置與輸出電壓的對應，以及音訊錐形音量控制項的認知音量。

![音訊-錐形音量控制的輸出圖表](images/taper2.jpg)

如上圖右邊所示，觀察到的音量會隨著滑杆位置的變更而以線性方式變化。 若要這樣做，DAC 電壓必須隨著位置而改變 nonlinearly，如圖左邊所示。 [曲線] asymptotically 會將0伏的方法，從最大值設定往左移動。 最小滑杆位置的電壓很小，但可能不會剛好為零。

**IAudioEndpointVolume** 介面中的下列方法會使用以分貝測量的磁片區設定：

-   [**IAudioEndpointVolume::GetChannelVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelvolumelevel)
-   [**IAudioEndpointVolume::GetMasterVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getmastervolumelevel)
-   [**IAudioEndpointVolume::SetChannelVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel)
-   [**IAudioEndpointVolume::SetMasterVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel)

這些方法會產生大量設定和認知音量之間的大約線性關聯性。 這些方法所管理之磁片區控制項的磁片區範圍以分貝為單位，視音訊端點裝置而定。 若要判斷特定裝置的磁片區範圍，請呼叫 [**IAudioEndpointVolume：： GetVolumeRange**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumerange) 方法。

相較之下， **IAudioEndpointVolume** 介面中下列方法的磁片區設定，會在磁片區範圍上以更輕輕的錐形曲線為：

-   [**IAudioEndpointVolume::GetChannelVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelvolumelevelscalar)
-   [**IAudioEndpointVolume::GetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getmastervolumelevelscalar)
-   [**IAudioEndpointVolume::SetChannelVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar)
-   [**IAudioEndpointVolume::SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar)
-   [**IAudioEndpointVolume::VolumeStepDown**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown)
-   [**IAudioEndpointVolume::VolumeStepUp**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup)

在 Windows Vista 中，這些方法會使用在上圖中顯示的音訊-錐形曲線與線性錐形曲線之間的中間曲線。 請注意，在未來的 Windows 版本中，曲線的形狀可能會變更。 上述清單中的前四個方法是以正規化值的形式從 0.0 (最小磁片區) 到 1.0 (最大磁片區) 。 針對清單中的最後兩個方法，呼叫 [**IAudioEndpointVolume：： GetVolumeStepInfo**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumestepinfo) 方法，以取得磁片區範圍中的步驟數目。

下列介面會針對其音量設定使用線性錐形曲線：

-   [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)
-   [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)
-   [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)

如需這些介面的詳細資訊，請參閱 [會話磁片區控制項](session-volume-controls.md)。 如需磁片區範圍的詳細資訊，以及各種 Windows 版本中的預設磁片區層級，請參閱[預設音訊磁片區設定](/windows-hardware/drivers/audio/default-audio-volume-settings)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音量控制項](volume-controls.md)
</dt> </dl>

 

 
