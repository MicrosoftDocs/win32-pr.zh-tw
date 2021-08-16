---
description: 如果媒體應用程式想要提供可定制的回避體驗，則必須在系統中開啟或關閉通訊資料流程時接聽事件通知。
ms.assetid: 709ad912-6b03-4ad3-bc47-ad8b6bd6de45
title: 取得回避事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5869aa02a64ef3b7d035743b9bee3c91d295448c4d89d659862c5efc81d89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828259"
---
# <a name="getting-ducking-events"></a>取得回避事件

如果媒體應用程式想要提供可定制的回避體驗，則必須在系統中開啟或關閉通訊資料流程時接聽事件通知。 您可以使用 MediaFoundation、DirectShow 或 DirectSound （使用核心音訊 api）來提供自訂執行。 直接 WASAPI 用戶端也可以覆寫通訊會話開始和結束時的預設處理。

若要提供自訂的執行，媒體應用程式必須在通訊應用程式啟動或結束通訊串流時，從系統取得通知。 媒體應用程式必須執行 [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) 介面，並向音訊系統註冊執行。 成功註冊之後，媒體應用程式會透過介面中的方法，以回呼的形式接收事件通知。 如需詳細資訊，請參閱 [回避通知的執行考慮](handling-audio-ducking-events-from-communication-devices.md)。

若要傳送回避通知，音訊系統必須知道哪一個音訊會話正在接聽回避事件。 每個音訊會話都會使用 GUID （會話實例識別碼）來唯一識別。 會話管理員可讓應用程式取得會話的相關資訊，例如音訊會話的標題、轉譯狀態和會話實例識別碼。 您可以使用原則控制介面 [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2)來取出識別碼。

下列步驟摘要說明取得媒體應用程式之會話實例識別碼的流程：

1.  將裝置列舉值具現化，並使用它來取得媒體應用程式用來呈現非通訊資料流程之裝置端點的參考。
2.  從裝置端點啟用會話管理員，並取得會話管理員的 [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) 介面參考。
3.  藉由使用 [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) 指標，取得會話管理員之 [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) 介面的參考。
4.  從 [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)介面查詢 [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) 。
5.  呼叫 [**IAudioSessionControl2：： GetSessionInstanceIdentifier**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier) ，並取出包含目前音訊會話之會話識別碼的字串。

為了取得有關通訊串流的回避通知，媒體應用程式會呼叫 [**IAudioSessionManager2：： RegisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification)。 媒體應用程式會將其會話實例識別碼提供給音訊系統，並將指標提供給 [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) 的執行。 應用程式現在可以在通訊裝置上開啟串流時，接收事件通知。 若要停止取得通知，媒體應用程式必須呼叫 [**IAudioSessionManager2：： UnregisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregisterducknotification)。

下列程式碼顯示應用程式如何註冊以取得回避通知。 CMediaPlayer 類別是在 [回避通知的執行考慮](handling-audio-ducking-events-from-communication-devices.md)中定義。 [DuckingMediaPlayer](duckingmediaplayer.md)範例會實行此功能。


```C++
////////////////////////////////////////////////////////////////////
//Description: Registers for duck notifications depending on the 
//             the ducking options specified by the caller.
//Parameters: 
//    If DuckingOptOutChecked is TRUE, the client is registered for
//    to receive ducking notifications; 
//    FALSE, the client's registration is deleted.
////////////////////////////////////////////////////////////////////

HRESULT CMediaPlayer::DuckingOptOut(bool DuckingOptOutChecked)
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator* pDeviceEnumerator NULL;
    IMMDevice* pEndpoint = NULL;
    IAudioSessionManager2* pSessionManager2 = NULL;
    IAudioSessionControl* pSessionControl = NULL;
    IAudioSessionControl2* pSessionControl2 = NULL;

    LPWSTR sessionId = NULL;

    //  Start with the default endpoint.

    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), 
                          NULL, 
                          CLSCTX_INPROC_SERVER, 
                          IID_PPV_ARGS(&pDeviceEnumerator));
    
    if (SUCCEEDED(hr))
    {
        hr = pDeviceEnumerator>GetDefaultAudioEndpoint(
              eRender, eConsole, &pEndpoint);

        pDeviceEnumerator>Release();
        pDeviceEnumerator = NULL;
    }

    // Activate the session manager.
    if (SUCCEEDED(hr))
    {
        hr = pEndpoint->Activate(__uuidof(IAudioSessionManager2), 
                                 CLSCTX_INPROC_SERVER,
                                 NULL, 
                                 reinterpret_cast<void **>
                                 (&pSessionManager2));
        pEndpoint->Release();
        pEndpoint = NULL;
    }
    if (SUCCEEDED(hr))
    {
        hr = pSessionManager2->GetAudioSessionControl(
                                  NULL, 0, &pSessionControl);
        
    }

    if (SUCCEEDED(hr))
    {
        hr = pSessionControl->QueryInterface(
                               IID_PPV_ARGS(&pSessionControl2));
                
        pSessionControl->Release();
        pSessionControl = NULL;
    }

    // Get the session instance identifier.
    
    if (SUCCEEDED(hr))
    {
        hr = pSessionControl2->GetSessionInstanceIdentifier(
                                 sessionId);
                
        pSessionControl2->Release();
        pSessionControl2 = NULL;
    }

    //  Register for ducking events depending on 
    //  the specified preference.

    if (SUCCEEDED(hr))
    {
        if (DuckingOptOutChecked)
        {
            hr = pSessionManager2->RegisterDuckNotification(
                                    sessionId, this);
        }
        else
        {
            hr = pSessionManager2->UnregisterDuckNotification
                                      (FALSE);
        }
        pSessionManager2->Release();
        pSessionManager2 = NULL;
    }
    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用通訊裝置](using-the-communication-device.md)
</dt> <dt>

[預設回避體驗](stream-attenuation.md)
</dt> <dt>

[停用預設的回避體驗](disabling-the-ducking-experience.md)
</dt> <dt>

[提供自訂回避行為](providing-a-custom-ducking-experience.md)
</dt> <dt>

[回避通知的執行考慮](handling-audio-ducking-events-from-communication-devices.md)
</dt> </dl>

 

 



