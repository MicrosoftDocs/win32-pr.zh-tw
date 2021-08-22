---
description: 從 Invalid-Device 錯誤中復原
ms.assetid: 1f5c3458-70ca-45ba-ac33-5c7b9f092320
title: 從 Invalid-Device 錯誤中復原
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9f56972aeeae5cfb370a656a621c6b6e206f8caa115bec33203cab7eded3e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318558"
---
# <a name="recovering-from-an-invalid-device-error"></a>從 Invalid-Device 錯誤中復原

WASAPI 中的許多方法會傳回錯誤碼 AUDCLNT \_ E \_ 裝置 \_ 如果用戶端應用程式所使用的音訊端點裝置變得無效，則會使其失效。 此錯誤碼表示端點裝置已卸載，或音訊硬體或相關聯的硬體資源已重新設定、停用、移除或無法使用。 通常，應用程式可以從這個錯誤中復原。

>[!NOTE]
> 如需使用空間音訊 Api 時，從無效裝置錯誤中復原 (ISAC) 的相關資訊，請參閱 [從 Invalid-Device 錯誤中復原 (空間音效) ](recovering-from-an-invalid-device-error-spatial-sound.md)

應用程式應該用來從 AUDCLNT E 裝置中復原的 \_ 策略 \_ \_ 失效錯誤，取決於應用程式用來選取音訊端點裝置的下列技術：

-   一律選取預設音訊轉譯或捕獲裝置。
-   選取特定的音訊端點裝置。

在第二個案例中，應用程式會根據內部需求自動選取特定的裝置，或允許使用者從可用裝置清單中明確選取裝置。

使用預設裝置的應用程式可以嘗試從 AUDCLNT \_ E \_ 裝置的失效錯誤中復原，如下所示 \_ ：

1.  釋放 [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) 介面，以及它在裝置上取得的任何其他 WASAPI 介面。
2.  呼叫 [**IMMDeviceEnumerator：： GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) 方法，以取得目前的預設音訊裝置。
3.  嘗試在預設音訊裝置上啟用 [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) 。

遵循上述步驟，不論 AUDCLNT E 裝置發生不正確錯誤，應用程式往往會適當地 \_ 回應 \_ \_ 。 如果預設裝置的重新設定造成錯誤 (例如，如果使用者變更了裝置) 所使用的串流格式，則這些步驟會在成功時，讓應用程式繼續使用相同的裝置。 如果使用者停用或移除應用程式所使用的裝置，而另一部裝置可用來擔任預設裝置的角色，則應用程式可以使用新的預設裝置繼續進行。 無論是哪一種情況，應用程式都會自動調整，而不需要使用者介入。

選取特定裝置的應用程式可以嘗試從 AUDCLNT \_ E \_ 裝置的失效錯誤中復原，如下所示 \_ ：

1.  釋放 [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) 介面，以及它在裝置上取得的任何其他 WASAPI 介面。
2.  嘗試啟用相同裝置上的 [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) 介面。
3.  如果步驟2失敗，則應用程式可以選擇提示使用者選取其他裝置。

如果應用程式所使用的裝置已重新設定但未停用或移除，步驟2就會成功。 如果成功，步驟2可讓應用程式自動繼續使用相同的裝置，而不需要使用者介入。 如果應用程式允許使用者在使用者停用或移除先前使用的裝置之後明確地選取另一部裝置，則適用步驟3。

應用程式可以藉由註冊在會話中斷裝置與裝置的連線時收到通知，來更精確地判斷出無效裝置錯誤的原因。 若要啟用此通知，應用程式會執行 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) 介面，並呼叫 [**IAudioSessionControl：： RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) 方法來註冊介面。 當無效裝置錯誤導致會話中斷連接時，WASAPI 會在已註冊的介面中呼叫 [**IAudioSessionEvents：： OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) 方法。 透過這個方法，WASAPI 會通知應用程式中斷連接的原因。 在 Windows Vista 中， **OnSessionDisconnected** 呼叫會識別下列原因：

-   使用者已移除音訊端點裝置。
-   Windows 的音訊服務已關閉。
-   針對音訊會話所連接的裝置，慣用的資料流程格式已變更。
-   使用者登出 Windows 終端機服務 (WTS 執行音訊會話的) 會話。 如需 WTS 會話的詳細資訊，請參閱 Windows SDK 檔。
-   正在執行音訊會話的 WTS 會話已中斷連線。
-    (的共用模式) 音訊會話已中斷連線，讓音訊端點裝置可供獨佔模式連線使用。

為了回應中斷連接事件，WASAPI 會關閉屬於會話的所有資料流程。 如果應用程式後續嘗試透過 WASAPI 方法（例如 [**IAudioClient：： GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding)）存取已關閉的資料流程，則該方法會失敗，並傳回錯誤碼 AUDCLNT \_ E \_ 裝置 \_ 無效。

透過 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) 介面接收通知的另一個好處是，通知會以非同步方式抵達。 因此，即使串流未執行，應用程式仍會及時收到無效裝置錯誤的及時通知，以防止串流執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[串流管理](stream-management.md)
</dt> </dl>

 

 



