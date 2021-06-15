---
description: 瞭解串流路由的通知。 Api 會藉由處理切換至新預設音訊端點的資料流程來執行串流路由。
ms.assetid: caf831bb-b8de-467f-bdb4-f9f8991dc7a8
title: 串流路由的相關通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1a843c1d8b5cfd740ada5049cb9428e7745072d
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068524"
---
# <a name="relevant-notifications-for-stream-routing"></a>串流路由的相關通知

在 Windows 7 中，使用核心音訊 Api 的高階平臺 Api （例如媒體基礎、DirectSound 和 Wave Api）會藉由處理從現有裝置切換至新的預設音訊端點來執行串流路由功能。 使用這些 Api 的媒體應用程式會使用串流路由行為，而不會對來源進行任何修改。 Direct WASAPI 用戶端可以使用核心音訊元件所傳送的通知，並執行串流路由功能。

若要執行串流路由功能，用戶端必須接聽兩種類型的事件：裝置變更通知和會話中斷連線通知。 在高階 Api 提供的執行中，會針對藉由呼叫 [**IMMDeviceEnumerator：： GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint)建立的預設裝置端點傳送這些事件。 如需詳細資訊，請參閱 [取得串流路由的裝置端點](getting-the-default-device-endpoint-for-stream-routing.md)。

新增、移除或修改音訊裝置時，核心音訊元件 MMDeviceAPI 會提供通知回呼。 格式和音訊會話變更會透過 WASAPI 回報為事件。

## <a name="device-change-notifications"></a>裝置變更通知

新增、移除或修改音訊裝置時，MMDeviceAPI 會引發事件。 如果用戶端是提供資料流程路由功能，則必須執行 [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) 介面，並使用 MMDeviceAPI 註冊其實作為。

若要取得裝置變更通知，用戶端必須執行下列工作：

-   執行 [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) 介面來處理 MMDeviceAPI 所傳送的裝置變更通知。
-   藉由呼叫 [**IMMDeviceEnumerator：： RegisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback)方法，透過 MMDeviceAPI 註冊 [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient)執行。

在用戶端執行這些介面的程式之後，用戶端會透過這些介面的方法以回呼形式接收通知。 當 MMDeviceAPI 引發端點層級事件 (端點狀態變更、新的端點抵達、端點刪除、預設端點變更和端點屬性變更) 時，會呼叫 [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient)方法。

如果用戶端想要提供預設裝置的串流路由，用戶端必須在透過 [**IMMNotificationClient：： OnDefaultDeviceChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged) 回呼接收通知時，執行裝置變更行為。

## <a name="audio-session-change-notifications"></a>音訊會話變更通知

音訊會話變更和格式變更會透過 WASAPI 回報為音訊會話事件。 WASAPI 用戶端會執行 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) 介面，並向 WASAPI 註冊該執行。

若要取得音訊會話變更通知，用戶端必須執行下列工作：

-   執行 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) 介面來處理 WASAPI 所傳送的格式變更通知。
-   藉由呼叫 [**IAudioSessionControl：： RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification)方法，透過 WASAPI 註冊 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)執行。

當音訊會話發生變更時，WASAPI 會呼叫 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)方法。 當會話的顯示名稱、圖示路徑、磁片區、群組參數或狀態變更時，就會引發這些事件。

若要執行串流路由功能，用戶端必須等候會話中斷連線通知。 當音訊會話中斷連線或裝置的格式變更時，WASAPI 會透過 [**IAudioSessionEvents：： OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected)以回呼的形式傳送用戶端通知。 在中斷連線通知的情況下，WASAPI 也會傳送一個值，指出會話中斷連接的原因。 發生這種情況的原因有好幾種，例如裝置已移除、伺服器已停止等等。 如需完整的原因清單，請參閱 AudioPolicy 中定義的 **AudioSessionDisconnectReason** 列舉。 如果預設裝置變更，用戶端必須等待通知 (如果尚未收到與 **DisconnectReasonDeviceRemoval** 值相關的) 。 為了回應這類通知，用戶端可能會重新開啟新預設裝置上的資料流程。

因為所有這些作業都是非同步，所以無法預測應用程式接收通知的順序。 不過，應用程式通常會在預設裝置變更通知之前收到 **AudioSessionDisconnect** 值。

### <a name="format-change-notifications"></a>格式化變更通知

當資料流程的格式變更時，就會發生音訊格式變更。 當使用者在 [ **音效** 控制台] 中選取新格式，或新的預設裝置支援新的格式時，就會發生這種情況 (例如，HDMI 或特定的專業音訊介面與手動取樣率調整) 。 為了通知用戶端這些類型的格式變更，WASAPI 由 [**IAudioSessionEvents：： OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) 的已註冊實作為 **DisconnectReasonFormatChanged** 的中斷連接原因傳送會話通知。 用戶端可以重新開啟新格式的資料流程來處理通知。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 MMDevice API](mmdevice-api.md)
</dt> <dt>

[關於 WASAPI](wasapi.md)
</dt> <dt>

[串流路由](stream-routing.md)
</dt> </dl>

 

 



