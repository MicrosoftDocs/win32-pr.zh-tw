---
description: 串流管理
ms.assetid: 936d8d69-e86c-418b-b5b0-c4fbbfa1dd49
title: 串流管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669e3be8af4532f9045c08f07400d47c423d507d4e11da4ada0b1a279c52772d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077432"
---
# <a name="stream-management"></a>串流管理

列舉系統中的 [音訊端點裝置](audio-endpoint-devices.md) ，並識別適合的轉譯或捕獲裝置之後，音訊用戶端應用程式的下一項工作就是開啟與端點裝置的連線，並透過該連線管理音訊資料的流程。 [WASAPI](wasapi.md) 可讓用戶端建立及管理音訊串流。

WASAPI 會執行數個介面，以提供串流管理服務給音訊用戶端。 主要介面為 [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)。 用戶端會藉由呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)方法 (，並將參數 *iid* 設定為端點物件上的 **REFIID** iid IAudioClient) ，藉以取得音訊端點裝置的 **IAudioClient** 介面 \_ 。

用戶端會呼叫 [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) 介面中的方法來執行下列作業：

-   探索端點裝置支援的音訊格式。
-   取得端點緩衝區大小。
-   取得資料流程格式和延遲。
-   啟動、停止和重設流經端點裝置的串流。
-   存取其他音訊服務。

若要建立資料流程，用戶端會呼叫 [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) 方法。 透過這個方法，用戶端會指定資料流程的資料格式、端點緩衝區的大小，以及資料流程是否以共用或獨佔模式運作。

[**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)介面中的其餘方法分為兩個群組：

-   只有在 [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)開啟資料流程之後，才能呼叫的方法。
-   可以在 [**Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) 呼叫之前或之後的任何時間呼叫的方法。

只有在呼叫 [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)之後，才能呼叫下列方法：

-   [**IAudioClient::GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize)
-   [**IAudioClient::GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding)
-   [**IAudioClient：： GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)
-   [**IAudioClient::GetStreamLatency**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getstreamlatency)
-   [**IAudioClient：： Reset**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-reset)
-   [**IAudioClient：： Start**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start)
-   [**IAudioClient：： Stop**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop)

您可以在 [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) 呼叫之前或之後呼叫下列方法：

-   [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod)
-   [**IAudioClient::GetMixFormat**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getmixformat)
-   [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported)

若要存取其他音訊用戶端服務，用戶端會呼叫 [**IAudioClient：： GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) 方法。 透過這個方法，用戶端可以取得下列介面的參考：

-   [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)

    將轉譯資料寫入音訊呈現端點緩衝區。

-   [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)

    從音訊捕獲端點緩衝區讀取捕捉到的資料。

-   [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)

    與音訊會話管理員通訊，以設定及管理與資料流程相關聯的音訊會話。

-   [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)

    控制與資料流程相關聯之音訊會話的音量層級。

-   [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)

    控制與資料流程相關聯之音訊會話中個別通道的音量層級。

-   [**IAudioClock**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)

    監視資料流程資料速率和資料流程位置。

此外，需要會話相關事件通知的 WASAPI 用戶端應該會執行下列介面：

-   [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)

    若要接收事件通知，用戶端會將其 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) 介面的指標傳遞至 [**IAudioSessionControl：： RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) 方法，作為呼叫參數。

最後，用戶端可能會使用較高層級的 API 來建立音訊串流，但也需要存取包含該資料流程之會話的會話控制項和磁片區控制項。 較高層級的 API 通常不會提供此存取權。 用戶端可以透過 [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) 介面取得特定會話的控制項。 此介面可讓用戶端取得會話的 [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) 和 [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) 介面，而不需要用戶端使用 [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) 介面來建立資料流程，以及將串流指派給會話。 用戶端會藉由呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)方法 (，並將參數 *iid* 設定為端點物件上的 **REFIID** iid IAudioSessionManager) ，藉以取得音訊端點裝置的 **IAudioSessionManager** 介面 \_ 。

[**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)、 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)和 [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager)介面是在標頭檔 Audiopolicy 中定義。 所有其他 WASAPI 介面都是在標頭檔 Audioclient 中定義。

下列各節說明如何使用 WASAPI 來管理音訊串流：

-   [關於 WASAPI](wasapi.md)
-   [呈現資料流程](rendering-a-stream.md)
-   [捕獲資料流程](capturing-a-stream.md)
-   [回送記錄](loopback-recording.md)
-   [獨佔模式資料流程](exclusive-mode-streams.md)
-   [從 Invalid-Device 錯誤中復原](recovering-from-an-invalid-device-error.md)
-   [使用通訊裝置](using-the-communication-device.md)
-   [串流路由](stream-routing.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式設計指南](programming-guide.md)
</dt> </dl>

 

 



