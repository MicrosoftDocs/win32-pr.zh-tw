---
description: 關於 WASAPI
ms.assetid: 452b9725-b0b9-4888-bbb5-a23e0067e840
title: 關於 WASAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3effb34ec0cde0a53d0eb6f6e9718aa13fc308417b33427f168364afc32086ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088178"
---
# <a name="about-wasapi"></a>關於 WASAPI

Windows 音訊會話 API (WASAPI) 可讓用戶端應用程式管理應用程式和[音訊端點裝置](audio-endpoint-devices.md)之間的音訊資料流程程。

標頭檔 Audioclient .h 和 Audiopolicy 定義 WASAPI 介面。

每個音訊串流都是 [音訊會話](audio-sessions.md)的成員。 透過會話抽象，WASAPI 用戶端可以將音訊串流識別為相關音訊串流群組的成員。 系統可以將會話中的所有資料流程當作單一單位來管理。

音訊引擎是 [使用者模式的音訊元件](user-mode-audio-components.md) ，應用程式可透過此元件共用音訊端點裝置的存取權。 音訊引擎會在端點緩衝區和端點裝置之間傳輸音訊資料。 若要透過呈現端點裝置播放音訊串流，應用程式會定期將音訊資料寫入轉譯端點緩衝區。 音訊引擎混合不同應用程式的資料流程。 若要從「捕獲端點」裝置錄製音訊串流，應用程式會定期從「捕獲端點」緩衝區讀取音訊資料。

WASAPI 包含數個介面。 其中第一個是 [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) 介面。 若要存取 WASAPI 介面，用戶端會先呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)方法，並將參數 *Iid* 設定為 **REFIID** iid IAudioClient，以取得音訊端點裝置之 **IAudioClient** 介面的參考 \_ 。 用戶端會呼叫 [**IAudioClient：： initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) 方法，以初始化端點裝置上的資料流程。 在初始化資料流程之後，用戶端可以藉由呼叫 [**IAudioClient：： GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) 方法，取得其他 WASAPI 介面的參考。

\_ \_ \_ 如果用戶端應用程式使用的音訊端點裝置變得無效，WASAPI 中的許多方法會傳回錯誤碼 AUDCLNT E 裝置失效。 通常，應用程式可以從這個錯誤中復原。 如需詳細資訊，請參閱 [從 Invalid-Device 錯誤中復原](recovering-from-an-invalid-device-error.md)。

WASAPI 會執行下列介面。



| 介面                                            | 描述                                                                                                                                                     |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)   | 可讓用戶端從 capture 端點緩衝區讀取輸入資料。                                                                                             |
| [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)                 | 可讓用戶端在音訊應用程式與音訊引擎或音訊端點裝置的硬體緩衝區之間，建立及初始化音訊串流。 |
| [**IAudioClock**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)                   | 讓用戶端監視資料流程的資料速率，以及資料流程中的目前位置。                                                                        |
| [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)     | 讓用戶端將輸出資料寫入轉譯端點緩衝區。                                                                                           |
| [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) | 可讓用戶端設定音訊會話的控制參數，以及監視會話中的事件。                                                 |
| [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) | 讓用戶端能夠存取跨進程和進程專屬音訊會話的會話控制項和磁片區控制項。                                 |
| [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)     | 可讓用戶端控制及監視音訊串流中所有通道的音量層級。                                                           |
| [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)   | 可讓用戶端控制串流所屬音訊會話中所有通道的磁片區層級。                                          |
| [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)     | 可讓用戶端控制音訊會話的主要磁片區層級。                                                                                        |



 

需要會話相關事件通知的 WASAPI 用戶端應該執行下列介面。



| 介面                                          | 描述                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) | 提供會話相關事件的通知，例如磁片區層級、顯示名稱和會話狀態的變更。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[串流管理](stream-management.md)
</dt> <dt>

[**程式設計參考**](programming-reference.md)
</dt> </dl>

 

 



