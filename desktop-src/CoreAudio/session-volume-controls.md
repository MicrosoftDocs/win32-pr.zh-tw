---
description: 會話磁片區控制項
ms.assetid: e6d112f9-08c9-4d95-b37b-267beebd0d7f
title: 會話磁片區控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe45dce825dedd116c8f9c65684ac665eb6483f95dec3d247071f66408e8ed2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758888"
---
# <a name="session-volume-controls"></a>會話磁片區控制項

如先前所述，WASAPI 用戶端可以個別控制每個 [音訊會話](audio-sessions.md)的音量層級。 WASAPI 會將會話的磁片區設定一致地套用到會話中的所有資料流程。 每個磁片區層級都是0.0 到1.0 範圍的值，其中0.0 表示無回應，而1.0 表示完整磁片區 (沒有衰減) 。

用戶端會將第一個資料流程指派給該會話，以隱含方式建立會話。 新會話的預設磁片區層級為1.0。 如先前所述，使用者可以透過控制項程式的使用者介面來調整會話的音量層級 (例如，Sndvol) 是 WASAPI 用戶端。 控制項設定是持續性的。

除了用戶端控制的磁片區設定以外，系統也會將自己的磁片區設定套用至會話。 這些設定是以音訊原則為基礎，而且會動態變更，以回應組成全域音訊混合的資料流程變更。 如需有關音訊原則的詳細資訊，請參閱 [使用者模式音訊元件](user-mode-audio-components.md)。

針對每個串流執行磁片區控制的系統軟體會將串流中的 PCM 樣本與有效的磁片區層級相乘。 有效的磁片區層級是將用戶端和系統磁片區設定相乘的結果。 因此，信號波幅的結果變更是用戶端和系統磁片區層級的線性組合。 例如，如果用戶端磁片區層級是0.8，而系統磁碟區層級是0.5，則有效磁片區層級 (0.8) <sup>。</sup> (0.5) = 0.4。

請注意，觀察到的音量對信號波幅而言並非線性的。 相反地，音量的變化大約是磁片區層級 v 的對數：

音量（分貝 = 20）<sup>。</sup>記錄₁₀ (v) 

因此，設定 v = 0.5 會 attenuates 原始信號的音量， (在將磁片區層級套用) 6 分貝之前的信號、設定 v = 0.25 attenuates 信號乘以12分貝等等。 磁片區層級 v = 1.0 （對應至0分貝）不會改變原始信號等級。

具有用來控制音量層級之使用者介面的音訊應用程式，通常會顯示在認知音量中產生變更的滑杆，並以線性方式與滑杆位置的變化呈正比。 若要產生觀察到的音量和滑杆位置之間的線性關聯性，應用程式必須定義磁片區層級 v 和滑杆位置之間的非線性關聯性。 如需詳細資訊，請參閱 [音訊-錐音量控制項](audio-tapered-volume-controls.md)。

如先前所述，系統音量控制程式 Sndvol 會顯示每個音訊轉譯裝置上播放之音訊會話的音量滑杆。 這些滑杆會顯示在 [SndVol] 視窗中標示為 [ **應用程式** ] 的群組方塊中。 一般而言，每個會話都會包含特定應用程式視窗中的所有播放資料流程。 透過 Sndvol 視窗中的滑杆，使用者控制個別音訊應用程式的音量層級。

一般來說，應用程式應該將所有的播放串流指派給相同的音訊會話。 WASAPI 不會防止應用程式在多個會話之間散發其播放資料流程。 不過，在 Sndvol 中產生的大量滑杆可能會使使用者混淆。

應用程式視窗可以選擇顯示音量滑杆。 應用程式滑杆應該隨時反映對應 Sndvol 滑杆的狀態。 因此，如果使用者在應用程式視窗中移動滑杆來變更音量層級，則 [Sndvol] 視窗中對應的滑杆應該與應用程式滑杆一致地移動。 同樣地，如果使用者移動 Sndvol 滑杆，則應用程式滑杆應該與 Sndvol 滑杆一致地移動。

為了支援此行為，WASAPI 會執行 [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) 介面。 當使用者移動應用程式滑杆時，應用程式會呼叫 [**ISimpleAudioVolume：： SetMasterVolume**](/windows/desktop/api/Audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume) 方法，據以調整會話音量層級。 Sndvol 會監視透過此方法所進行的磁片區變更，並反映其顯示的音量滑杆變更。 此外，應用程式也可以接收使用者透過 Sndvol 進行之會話磁片區變更的通知。 基於此目的，應用程式會執行 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) 介面，並向 WASAPI 註冊介面。 之後，每次使用者透過 Sndvol 變更會話磁片區層級時，應用程式就會收到透過 [**IAudioSessionEvents：： OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) 方法發出的通知呼叫。 如需執行 **IAudioSessionEvents** 介面的程式碼範例，請參閱 [音訊會話事件](audio-session-events.md)。 如需註冊 **IAudioSessionEvents** 介面的程式碼範例，請參閱 [舊版音訊應用程式的音訊事件](audio-events-for-legacy-audio-applications.md)。

**ISimpleAudioVolume** 介面會將相同的磁片區層級一致地套用到音訊會話中的所有通道。 雖然這個介面應該滿足大多數應用程式的磁片區控制需求，但有些應用程式可能需要更特製化的磁片區控制功能。 [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)介面會控制會話中的個別資料流程相對於其他資料流程的量。 **IAudioStreamVolume** 也可讓用戶端個別控制串流中所有通道的磁片區層級。 例如，應用程式可能會使用這項功能來達成音訊效果，例如透過從左至右移動來模擬音訊來源的空間移動。 另一個特製化介面 [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)，會控制會話中個別通道的音量層級。 例如，應用程式可能會使用 **IChannelAudioVolume** 來執行 stereophonic 音效系統的平衡控制。

Sndvol 中 [ **應用程式** ] 方塊中的 [音量] 滑杆只會反映透過 **ISimpleAudioVolume** 介面進行的磁片區變更。 它們不會反映透過 **IAudioStreamVolume** 和 **IChannelAudioVolume** 介面進行的磁片區變更。 雖然有些應用程式可讓使用者透過 **IAudioStreamVolume** 和 **IChannelAudioVolume** 直接或間接控制磁片區設定，但開發人員應避免呈現這些大量設定的應用程式滑杆，讓使用者可能會與 Sndvol 中的音量滑杆混淆。 否則，使用者可能會移動預期會看到變更反映在 Sndvol 滑杆中的應用程式滑杆，並在沒有這類變更時變成混淆。 開發人員可以透過謹慎的使用者介面設計來避免這個問題。

會話 submix 中任何頻道的有效磁片區層級（如喇叭所聽到）是下列四個磁片區層級因素的乘積：

-   會話中資料流程的每個通道磁片區層級，用戶端可以透過 **IAudioStreamVolume** 介面中的方法來控制這些層級。
-   會話的每個通道磁片區層級，用戶端可以透過 **IChannelAudioVolume** 介面中的方法來控制。
-   會話的主要磁片區層級，用戶端可以透過 **ISimpleAudioVolume** 介面中的方法來控制。
-   會話的以原則為基礎的磁片區層級，系統會以全域混合變更的方式進行動態修改。

上述清單中四個磁片區層級的每一個都是0.0 到1.0 範圍的值，其中0.0 表示無回應，而1.0 表示完整磁片區 (沒有衰減) 。 有效的磁片區層級也是範圍0.0 到1.0 之間的值。

音訊引擎會將每個通道的有效磁片區層級套用至資料流程中的通道，然後將資料流程與音訊會話中的其他資料流程混合。 如果通道中的任何範例值在音訊引擎乘以有效的磁片區層級後超過0分貝，則引擎會先裁剪範例，再將它們新增至會話 submix。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音量控制項](volume-controls.md)
</dt> </dl>

 

 



