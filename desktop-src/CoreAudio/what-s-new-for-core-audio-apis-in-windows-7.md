---
description: 核心音訊 api 是在 Windows Vista 中引進，它提供了一組新的使用者模式音訊元件，用戶端應用程式可以使用這些元件來轉譯或抓住具有改良音訊功能的音訊串流。
ms.assetid: eb99c266-16d2-4a14-bc1d-059a0a94db13
title: Windows 7 中 Core Audio api 的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6160b275512a7efbd3b795e263f2ce8ae01be965
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474704"
---
# <a name="whats-new-for-core-audio-apis-in-windows-7"></a>Windows 7 中 Core Audio api 的新功能

核心音訊 api 是在 Windows Vista 中引進，它提供了一組新的使用者模式音訊元件，用戶端應用程式可以使用這些元件來轉譯或抓住具有改良音訊功能的音訊串流。 如需此 API 集的一般總覽，請參閱[關於 Windows Core 音訊 api](about-the-windows-core-audio-apis.md)。

Windows 7 中的核心音訊 api 已獲得改良。 下表摘要說明核心音訊 Api 的新功能和增強功能：




| 功能 | 描述 | 
|---------|-------------|
| 一般改善 | 下列功能已在 Windows 7 中獲得改良：<ul><li>在 Windows 7 的共用模式資料流程會在<em>低延遲模式</em>中執行。 音訊引擎會在提取模式中執行，並大幅降低延遲。 對於需要低音訊串流延遲以加快串流速度的通訊應用程式而言，這非常有用。</li><li>當新的裝置新增至系統時，Windows 7 提供更佳的裝置角色偵測。 如需詳細資訊，請參閱 <a href="device-roles-in-windows-vista.md">使用裝置角色</a>。</li><li>在 Windows 7 中，您可以透過電腦喇叭聆聽便攜媒體播放機的音樂。 您可以藉由將便攜媒體播放機插入電腦上的類比音訊纜線，來使用此捕捉監視功能。 在過去，某些 Oem 會使用硬體回送，在音訊驅動程式中提供這項功能。 在 Windows 7 中，這項功能已新增至作業系統。 由於這是在系統中，而不是驅動程式，因此您可以將它用於任何其他連線到系統的裝置，例如 USB 耳機。</li><li>已增強 Windows 7 中的 HDMI 音訊，可提供高位速率格式的支援。 透過這種改進，您可以透過 HDMI 連接器支援多頻道音訊和壓縮的音訊格式給音訊接收器。</li><li>在 Windows Vista 中，Windows Media Player 只會透過預設音訊裝置（無法由使用者變更）來播放音樂。 針對 Windows Media Player 將音訊轉譯為特定裝置，您必須<strong>在 [音效</strong>] 控制台中變更預設裝置。 在 Windows 7 中，Windows Media Player 提供可讓應用程式轉譯為使用者所選取之任何裝置的 api，而不只是預設裝置。</li><li>在 Windows Vista 中，如果播放音訊的電腦切換到省電模式，電腦會被鎖定，而且如果使用者想要中斷播放，則使用者必須登入，然後按下停止鍵來停止播放。 在 Windows 7 中，如果電腦已鎖定，您仍然可以使用鍵盤上的 [隱藏] 控制項來控制播放。</li><li>Windows 7 可減少使用 DirectSound 和 DirectShow 轉譯媒體的任何應用程式耗電量。 此外，多媒體類別排程器服務可提供有問題的復原音訊，並在產生音訊樣本時使用較少的電源。</li></ul> | 
|  (新) 的通訊裝置 | 在此版本中，已將新的裝置類型新增 <strong>至 [音效</strong> 控制台： <strong>通訊</strong> 裝置]。 此裝置主要用於通訊，也就是在電腦上撥打或接收電話。 通訊應用程式可以使用核心音訊元件來取得預設通訊裝置端點的參考，以及基於通訊目的轉譯音訊串流。 作業系統會將通訊裝置上開啟的串流視為通訊串流。 通訊串流上的 WASAPI 作業類似于任何其他音訊串流。 如需詳細資訊，請參閱 <a href="device-roles-in-windows-vista.md">使用裝置角色</a>。 | 
|  (新) 的串流衰減或音訊回避 | 自動回避或<a href="stream-attenuation.md">串流衰減</a>是 Windows 7 的新功能，適用于 VoIP 和整合通訊應用程式。 根據預設，作業系統會在透過電腦在通訊裝置上收到通訊串流（例如通話）時，減少音訊串流的強度。 磁片區選項是由使用者在 <strong>音效</strong> 控制台中設定。 已在 Windows SDK 中加入新的 api，可讓應用程式取代預設的回避行為。 如需有關如何執行自訂回避功能的詳細資訊，請參閱 <a href="providing-a-custom-ducking-experience.md">提供自訂回避行為</a>。 <br /> | 
|  (新) 的串流路由 | 在 Windows 7 中，已改善核心音訊 api，以從現有裝置順暢地將音訊串流傳輸至新的預設音訊端點。 使用核心音訊 Api （例如媒體基礎、DirectSound 和 WAVE Api）的高階音訊 API 集會執行串流路由功能。 使用這些 API 集來播放或捕捉資料流程的媒體應用程式會使用預設的執行，而不需要修改應用程式。 但是，如果您的媒體應用程式直接使用核心音訊 Api，應用程式必須提供資料流程路由執行。 若要這樣做，應用程式必須處理已新增的新事件，此事件會在連線或移除預設裝置時通知 WASAPI 用戶端。 如需這項功能的詳細資訊，請參閱 <a href="stream-routing.md">串流路由</a>。 | 
| 受保護的使用者模式音訊 (PUMA)  (改善)  | PUMA 已更新為 Windows 7，以提供下列功能：<ul><li>在) 的多媒體介面 High-Definition HDMI (端點上，設定序號複製管理系統 (SCMS) 位於 S/PDIF 端點和高頻寬數位內容保護 (HDCP) 位。</li><li>在受保護的環境以外啟用 SCMS 和 HDMI 保護控制項， (PE) 。</li></ul>如需改善的詳細資訊，請參閱 <a href="protected-user-mode-audio--puma-.md">受保護的使用者模式音訊 (PUMA) </a>。<br /> | 
| <strong>WAVEFORMATEXTENSIBLE</strong>結構已擴充至<strong>WAVEFORMATEXTENSIBLE_IEC61937</strong>結構 (新)  | 在 Windows 7 中，已加入新的結構以支援 IEC 61937 傳輸。 <strong>WAVEFORMATEXTENSIBLE_IEC61937</strong> 會擴充 <strong>WAVEFORMATEXTENSIBLE</strong> 結構來儲存兩組音訊串流特性：編碼的音訊格式在音訊串流經過解碼之後傳輸和特性。 新的結構會明確指定非 PCM 格式的通道、樣本大小和資料速率的有效數目。 利用這項資訊，應用程式可以在解壓縮並播放非 PCM 串流之後，推斷其品質層級。 如需詳細資訊，請參閱 <a href="representing-formats-for-iec-61937-transmissions.md">代表 IEC 61937 傳輸的格式</a>。<br /> | 
| <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize"><strong>IAudioClient：： Initialize</strong></a> (改良)  | <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize"><strong>IAudioClient：： Initialize</strong></a>方法已經過改良，指出開啟音訊串流時可能發生的特定錯誤。 新的錯誤碼如下：<ul><li>AUDCLNT_E_BUFFER_SIZE_NOT_ALIGNED</li><li>AUDCLNT_E_BUFFER_SIZE_ERROR</li><li>AUDCLNT_E_INVALID_DEVICE_PERIOD</li></ul>如需有關這些錯誤的詳細資訊，請參閱 <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize"><strong>IAudioClient：： Initialize</strong></a>中的傳回值一節。<br /> | 
| <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer"><strong>IAudioCaptureClient：： GetBuffer</strong></a> 和 <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer"><strong>IAudioRenderClient：： GetBuffer</strong></a> (改良)  | <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer"><strong>IAudioCaptureClient：： GetBuffer</strong></a> 和 <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer"><strong>IAudioRenderClient：： GetBuffer</strong></a> 方法已經過改良，可傳回 AUDCLNT_E_BUFFER_ERROR 錯誤碼，指出未抓取獨佔模式中的端點緩衝區。 如需詳細資訊，請參閱 <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer"><strong>IAudioCaptureClient：： GetBuffer</strong></a> 和 <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer"><strong>IAudioRenderClient：： GetBuffer</strong></a>中的備註。 | 
|  (改良) 的插座偵測功能 | Windows 7 <a href="/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2"><strong>IKsJackDescription2</strong></a>中的新介面可擴充<a href="/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription"><strong>IKsJackDescription</strong></a>。 藉由使用新的介面，音訊堆疊或應用程式可以取得額外的插座資訊。 這包括插孔的偵測功能，以及裝置的格式是否已動態變更。 | 
| Windows新)  (範例 | 示範如何使用核心音訊 api 的 Windows SDK 已新增範例。 如需詳細資訊，請參閱 <a href="sdk-samples-that-use-the-core-audio-apis.md">使用核心音訊 Api 的 SDK 範例</a>。 | 




 

## <a name="major-new-interfaces"></a>主要新介面

以下是 Windows 7 的新介面：

-   [**IAudioClock2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclock2)
-   [**IAudioClockAdjustment**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment)
-   [**IAudioEndpointVolumeEx**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumeex)
-   [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2)
-   [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2)
-   [**IAudioSessionEnumerator**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionenumerator)
-   [**IAudioSessionNotification**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification)
-   [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification)
-   [**IKsJackDescription2**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2)
-   [**IKsJackSinkInformation**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjacksinkinformation)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Windows Core 音訊 api](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




