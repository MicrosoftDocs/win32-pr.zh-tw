---
description: 此核心音訊 SDK 的程式設計參考包含下列介面：
ms.assetid: b18e2094-e974-4c23-b70b-ace5a168132d
title: 核心音訊介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eed875bad93bed1625a175bd74b849f139a0140
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110017"
---
# <a name="core-audio-interfaces"></a>核心音訊介面

此核心音訊 SDK 的程式設計參考包含下列介面：

## <a name="mmdevice-api"></a>MMDevice API

Windows 多媒體裝置 (MMDevice) API 可讓音訊用戶端探索 [音訊端點裝置](audio-endpoint-devices.md)、判斷其功能，以及為這些裝置建立驅動程式實例。標頭檔 Mmdeviceapi 會定義 MMDevice API 中的介面。 如需詳細資訊，請參閱 [關於 MMDEVICE API](mmdevice-api.md)。

下表列出適用于 Windows Vista 的 Core Audio SDK 所提供的 MMDevice 介面。



| 介面                                              | 描述                                                                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)                         | 代表音訊裝置。                                                                                                                                                                    |
| [**IMMDeviceCollection**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection)     | 代表音訊裝置的集合。                                                                                                                                                      |
| [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)     | 提供列舉音訊裝置的方法。                                                                                                                                                |
| [**IMMEndpoint**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)                     | 代表音訊端點裝置。                                                                                                                                                           |
| [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) | 當新增或移除音訊端點裝置、裝置的狀態或屬性變更時，或指派給裝置的預設角色變更時，會提供通知。 |



 

## <a name="wasapi"></a>WASAPI

Windows 音訊會話 API (WASAPI) 可讓用戶端應用程式管理應用程式和 [音訊端點裝置](audio-endpoint-devices.md)之間的音訊資料流程程。 標頭檔 Audioclient .h 和 Audiopolicy 定義 WASAPI 介面。 如需詳細資訊，請參閱 [關於 WASAPI](wasapi.md)。

下表列出適用于 Windows Vista 和更新版本的 Core Audio SDK 所提供的 WASAPI 介面。



| 介面                                                                                    | 描述                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IActivateAudioInterfaceAsyncOperation**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfaceasyncoperation)       | 代表啟動 [WASAPI](wasapi.md) 介面的非同步作業，並提供方法來取得啟用的結果。<br/> 適用于 Windows 8 開頭。<br/> |
| [**IActivateAudioInterfaceCompletionHandler**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfacecompletionhandler) | 提供回呼，表示 [WASAPI](wasapi.md) 介面的啟用已完成。<br/> 適用于 Windows 8 開頭。<br/>                                                  |
| [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)                                           | 可讓用戶端從 capture 端點緩衝區讀取輸入資料。                                                                                                                                       |
| [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)                                                         | 可讓用戶端在音訊應用程式與音訊引擎或音訊端點裝置的硬體緩衝區之間，建立及初始化音訊串流。                                           |
| [**IAudioClock**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)                                                           | 讓用戶端監視資料流程的資料速率，以及資料流程中的目前位置。                                                                                                                  |
| [**IAudioClock2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclock2)<br/>                                              | 讓用戶端取得目前的裝置位置。<br/>                                                                                                                                           |
| [**IAudioClockAdjustment**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment)<br/>                            | 可讓用戶端設定資料流程的取樣率。<br/>                                                                                                                                           |
| [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)                                             | 讓用戶端將輸出資料寫入轉譯端點緩衝區。                                                                                                                                     |
| [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)                                         | 可讓用戶端設定音訊會話的控制參數，以及監視會話中的事件。                                                                                           |
| [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2)<br/>                            | 可讓用戶端取得音訊會話的相關資訊。<br/>                                                                                                                                   |
| [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager)                                         | 讓用戶端能夠存取跨進程和進程專屬音訊會話的會話控制項和磁片區控制項。                                                                           |
| [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2)<br/>                            | 管理所有 submixes，包括 submixes 的列舉和通知。 它也提供回避通知的支援。<br/>                                                                   |
| [**IAudioSessionEnumerator**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionenumerator)<br/>                        | 可讓用戶端列舉音訊會話。<br/>                                                                                                                                                  |
| [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)                                             | 可讓用戶端控制及監視音訊串流中所有通道的音量層級。                                                                                                     |
| [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)                                           | 可讓用戶端控制串流所屬音訊會話中所有通道的磁片區層級。                                                                                    |
| [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)                                             | 可讓用戶端控制音訊會話的主要磁片區層級。                                                                                                                                  |
| [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)                                           | 提供會話相關事件的通知，例如磁片區層級、顯示名稱和會話狀態的變更。                                                                                    |
| [**IAudioSessionNotification**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification)<br/>                    | 在發生會話變更時傳送通知。 <br/>                                                                                                                                               |
| [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification)<br/>              | 傳送有關暫止系統回避變更的通知。<br/>                                                                                                                                      |



 

## <a name="devicetopology-api"></a>DeviceTopology API

DeviceTopology API 可讓用戶端應用程式能夠跨越音訊轉譯和捕獲裝置的功能性硬體拓撲。 標頭檔 Devicetopology 會定義 DeviceTopology API 中的介面。 如需詳細資訊，請參閱 [裝置拓撲](device-topologies.md) 和 [**DeviceTopology API**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology)。

下表列出適用于 Windows Vista 和更新版本的 Core Audio SDK 所提供的 DeviceTopology 介面。



| 介面                                                           | 描述                                                                                                                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)              | 提供硬體自動增益控制 (AGC) 的存取權。                                                                                                                                                               |
| [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                                    | 提供硬體低音等級控制項的存取權。                                                                                                                                                                         |
| [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)                  | 提供硬體通道配置控制項的存取權。                                                                                                                                                              |
| [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)                  | 提供硬體多工器控制項 (輸入選取器) 的存取權。                                                                                                                                                       |
| [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                            | 提供對 "音量" 補償控制項的存取。                                                                                                                                                                     |
| [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                            | 提供硬體中型層級控制項的存取權。                                                                                                                                                                     |
| [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                                    | 提供硬體靜音控制項的存取。                                                                                                                                                                               |
| [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)                | 提供硬體信號信號控制 (輸出選取器) 的存取權。                                                                                                                                                    |
| [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                          | 提供硬體尖峰計量控制項的存取權。                                                                                                                                                                         |
| [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                                | 提供硬體高音層級控制項的存取。                                                                                                                                                                       |
| [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)                      | 提供硬體磁片區控制項的存取權。                                                                                                                                                                             |
| [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector)                                    | 表示元件之間的連接點。                                                                                                                                                                      |
| [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface)                      | 代表元件上的控制項介面， (子或連接器) 。                                                                                                                                                          |
| [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty)          | 代表連接器或子單位的裝置特定屬性。                                                                                                                                                          |
| [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology)                          | 提供對音訊裝置拓撲的存取。                                                                                                                                                                       |
| [**IKsFormatSupport**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)                        | 提供有關軟體設定的 i/o 連線所支援之音訊資料格式的資訊 (通常是音訊裝置和系統記憶體之間) DMA 通道。                                        |
| [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)                    | 提供有關插座或內部連接器的資訊，這些連接器會提供音訊介面卡上裝置與外部或內部端點裝置之間的實體連線 (例如麥克風或 CD 播放機) 。 |
| [**IKsJackDescription2**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2)<br/>       | 提供對端點裝置之連接器的 **KSPROPERTY \_ 插座 \_ DESCRIPTION2** 屬性方便的存取。<br/>                                                                                            |
| [**IKsJackSinkInformation**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjacksinkinformation)<br/> | 提供硬體支援的插座時，有關插座接收器的資訊。<br/>                                                                                                                             |
| [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart)                                              | 代表裝置拓撲的部分 (連接器或次級) 。                                                                                                                                                            |
| [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist)                                    | 代表 (連接器和次單元連接) 的部分清單。                                                                                                                                                                     |
| [**IPerChannelDbLevel**](/windows/desktop/api/Devicetopology/nn-devicetopology-iperchanneldblevel)                    | 代表泛型次級控制項介面，可針對音訊串流的音量層級或音訊串流中的頻率寬線，提供每個通道的控制。                                        |
| [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit)                                        | 代表硬體子單位 (例如，位於用戶端和音訊端點裝置之間的資料路徑中的磁片區層級控制) 。                                                                             |
| [**IControlChangeNotify**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolchangenotify)                | 當元件 (連接器或子) 的狀態變更時，會提供通知。                                                                                                                                          |



 

## <a name="endpointvolume-api"></a>EndpointVolume API

EndpointVolume API 可讓特製化用戶端控制及監視 [音訊端點裝置](audio-endpoint-devices.md)的音量層級。 標頭檔 Endpointvolume 會定義 EndpointVolume API 中的介面。 如需詳細資訊，請參閱 [**ENDPOINTVOLUME API**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) 。

下表列出適用于 Windows Vista 的 Core Audio SDK 所提供的 EndpointVolume 介面。



| **介面**                                                        | **說明**                                                                                   |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)                 | 代表音訊串流上或音訊端點裝置的音量控制項。           |
| [**IAudioEndpointVolumeEx**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumeex)<br/>  | 將音訊串流上的音量控制項提供給裝置端點。<br/>             |
| [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation)             | 表示音訊串流上或音訊端點裝置的尖峰計量。                  |
| [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) | 當音訊端點裝置的音量層級或靜音狀態變更時，會提供通知。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式設計參考](programming-reference.md)
</dt> </dl>

 

