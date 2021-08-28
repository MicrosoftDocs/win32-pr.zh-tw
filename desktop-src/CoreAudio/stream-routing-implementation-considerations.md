---
description: 瞭解串流路由的執行考慮。 Api 會藉由處理切換至新預設音訊端點的資料流程來執行串流路由。
ms.assetid: ecda0b5b-6583-43b4-a9b4-f12a95f09452
title: 串流路由的執行考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e440fed0035838eff18c3a93bca7271fcc484a8ce37a11ad4afd3931f357f76a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088241"
---
# <a name="stream-routing-implementation-considerations"></a>串流路由的執行考慮

在 Windows 7 中，使用核心音訊 api 的高階平臺 api （例如媒體基礎、DirectSound 和 Wave api）會處理從現有裝置切換至新的預設音訊端點的串流，以執行串流路由功能。 使用這些 Api 的媒體應用程式會使用串流路由行為，而不會對來源進行任何修改。 Direct WASAPI 用戶端可以使用核心音訊元件所傳送的通知，並執行串流路由功能。

直接 WASAPI 用戶端 (直接使用 WASAPI 的媒體應用程式) 接收核心音訊元件所傳送的新裝置和音訊會話通知。 資料流程路由功能的行為是由應用程式處理這些通知的方式定義。

MMDevice API 和音訊會話會將裝置狀態變更和會話變更的相關通知傳送給以回呼形式 WASAPI 的用戶端。 若要取得這些通知，用戶端必須註冊其 [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) 和 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)的實作為。 如需詳細資訊，請參閱 [資料流程路由的相關通知](relevant-device-notifications-for-stream-routing.md)。

在 [串流路由](stream-routing.md)中所述的 USB 耳機案例中，應用程式會播放音訊串流，並使用 MMDEVICEAPI 和 WASAPI，在預設轉譯裝置（ **講師**）上呈現資料流程。 變更預設裝置時，應用程式會收到 [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) 通知。 應用程式也會收到 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) 通知，指出使用者已移除音訊端點裝置，或音訊會話所連接之裝置的串流格式已變更。 收到通知後，應用程式會停止串流至說話者端點，然後重新開啟串流以在目前的預設端點（耳機）上呈現。

![裝置通知的資料流程圖。](images/stream-routing.gif)

為了回應這類通知，用戶端可能會以使用者選取的新格式，重新開啟新預設裝置上的資料流程。

## <a name="stream-managment"></a>串流管理

下列清單摘要說明 WASAPI 用戶端必須執行以提供資料流程切換功能的步驟。

1.  等候相關的 [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) 通知。 如果裝置是預設裝置，則會收到 [**IMMNotificationClient：： OnDefaultDeviceChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged) 通知。
2.  如果有新的裝置可用，請取得新裝置端點的參考。 針對新的預設裝置呼叫 [**IMMDeviceEnumerator：： GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) 。 如果新的裝置不是預設的裝置，您可以藉由呼叫 [**IMMDeviceEnumerator：： GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)來取得裝置。 如需詳細資訊，請參閱 [取得串流路由的裝置端點](getting-the-default-device-endpoint-for-stream-routing.md)。
3.  使用 reason 值等候 [**IAudioSessionEvents：： OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) 。
    > [!Note]  
    > 因為所有這些作業都是非同步，所以無法預測應用程式接收裝置變更和會話中斷連線通知的順序。 應用程式必須執行通知處理，以依任何順序接收這些通知。 不過，應用程式通常會在預設裝置變更通知之前收到 **AudioSessionDisconnect** 值。

     

4.  評估原因值，並判斷資料流程是否需要傳送到另一個音訊端點，或必須使用新的格式重新初始化資料流程。
5.  如果原因指出資料流程應重新路由傳送至新的預設裝置，請停止串流至舊的預設裝置。
6.  執行位置對應計算。
7.  開啟新裝置上的資料流程，並傳輸所有狀態資訊。
8.  在新的預設裝置上繼續串流。
9.  處理舊預設裝置的起飛。

若要讓串流切換作業順暢地出現，必須儘快完成。 這取決於在新裝置上重新開機資料流程時所牽涉到的元件效能。

## <a name="position-mapping-considerations"></a>位置對應考慮

當應用程式取得 [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) 和 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) 通知時，它可以將現有的串流路由傳送至新的預設裝置。 當現有的音訊串流在新裝置上中斷並開啟時，在新裝置上的轉譯必須從在舊裝置上停止串流的位置開始。 若要這樣做，應用程式必須有最近的已知裝置位置，才能計算新裝置上的開始位置。 例如，這個位置可以用來做為後續位置對應的差異位移。 當資料流程開始呈現時，新的裝置位置可以重新對應到快取的裝置位置。

下列步驟摘要說明進行順暢串流轉換的流程。

1.  快取舊裝置上資料流程的最後一個裝置位置。
2.  停止舊裝置上的資料流程。
3.  執行重新對應計算以取得新的位置。
4.  開始在新裝置上轉譯資料流程。
5.  釋放舊的資料流程。

在轉換期間，應用程式必須確定時鐘不會離開同步處理，而導致同步處理中的音訊和影片串流。 如果影片範例在音訊串流路由傳送至新裝置時繼續轉譯，就會發生這種情況。 應用程式必須快取重新對應計算的時鐘位置，並確定在新裝置上重新開啟音訊串流之前，不會轉譯影片範例，因此當剪輯繼續轉譯時，音訊和影片串流會進行同步處理。 在某些情況下，轉譯影片畫面的呈現時間是以音訊時鐘為基礎，在串流切換完成之前就已足夠停止音訊串流，而且音訊影片同步處理不需要影片串流的其他位置對應執行。

如果在轉譯時， [**IAudioRenderClient：： GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) 會傳回錯誤，因為舊的裝置會遺失，因此應用程式不需要停止舊的資料流程，因為串流作業已終止。 如需有關處理此錯誤的詳細資訊，請參閱 [從 Invalid-Device 錯誤中復原](recovering-from-an-invalid-device-error.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 MMDevice API](mmdevice-api.md)
</dt> <dt>

[關於 WASAPI](wasapi.md)
</dt> <dt>

[串流路由](stream-routing.md)
</dt> </dl>

 

 



