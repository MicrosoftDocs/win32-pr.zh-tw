---
description: 使用者可以使用 [Windows 多媒體] 控制台的 [通訊] 索引標籤上可用的選項，來停用系統提供的預設回避體驗，Mmsys.cpl。
ms.assetid: 5604b927-99f8-450f-a48c-b38d782584de
title: 停用預設的回避體驗
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed33fa7d9473cb5c68a018b98bff8a826612387e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111552"
---
# <a name="disabling-the-default-ducking-experience"></a>停用預設的回避體驗

使用者可以使用 [Windows 多媒體] 控制台的 [**通訊**] 索引標籤上可用的選項，來停用系統提供的 [預設回避體驗](stream-attenuation.md)，Mmsys.cpl。

套用回避時，淡出和淡入效果的使用時間為1秒。 遊戲應用程式可能不希望通訊串流干擾遊戲音訊。 有些媒體應用程式可能會發現播放體驗會在音樂淡入時 jarring。 這些類型的應用程式可以選擇不參與回避體驗。

直接 WASAPI 用戶端可以透過程式設計的方式，使用針對非通訊資料流程提供音量控制之音訊會話的會話管理員，退出宣告。 請注意，即使用戶端退出宣告回避，它仍會接收來自系統的回避通知。

若要退出宣告回避，用戶端必須取得會話管理員的 [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) 介面參考。 若要退出回避體驗，請使用下列步驟：

1.  將裝置列舉值具現化，並使用它來取得媒體應用程式用來呈現非通訊資料流程之裝置端點的參考。
2.  從裝置端點啟用會話管理員，並取得會話管理員的 [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) 介面參考。
3.  藉由使用 [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) 指標，取得會話管理員之 [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) 介面的參考。
4.  從 [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)介面查詢 [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) 。
5.  呼叫 [**IAudioSessionControl2：： SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference) 並傳遞 **TRUE** 或 **FALSE** ，以指定回避喜好設定。 在會話期間，您可以動態變更指定的喜好設定。 請注意，在資料流程停止並重新啟動之前，退出變更不會生效。

下列程式碼顯示應用程式如何指定其回避喜好設定。 函數的呼叫端必須在 DuckingOptOutChecked 參數中傳遞 **TRUE** 或 **FALSE** 。 根據傳遞的值，回避會透過 [**IAudioSessionControl2：： SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference)啟用或停用。


```C++
////////////////////////////////////////////////////////////////////
//Description: Specifies the ducking options for the application.
//Parameters: 
//    If DuckingOptOutChecked is TRUE system ducking is disabled; 
//    FALSE, system ducking is enabled.
////////////////////////////////////////////////////////////////////

HRESULT DuckingOptOut(bool DuckingOptOutChecked)
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator* pDeviceEnumerator NULL;
    IMMDevice* pEndpoint = NULL;
    IAudioSessionManager2* pSessionManager2 = NULL;
    IAudioSessionControl* pSessionControl = NULL;
    IAudioSessionControl2* pSessionControl2 = NULL;


    //  Start with the default endpoint.

    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), 
                          NULL, 
                          CLSCTX_INPROC_SERVER, 
                          IID_PPV_ARGS(&pDeviceEnumerator));
    
    if (SUCCEEDED(hr))
    {
        hr = pDeviceEnumerator>GetDefaultAudioEndpoint(eRender, eConsole, &pEndpoint);

        pDeviceEnumerator>Release();
        pDeviceEnumerator = NULL;
    }

    // Activate session manager.
    if (SUCCEEDED(hr))
    {
        hr = pEndpoint->Activate(__uuidof(IAudioSessionManager2), 
                                 CLSCTX_INPROC_SERVER,
                                 NULL, 
                                 reinterpret_cast<void **>(&pSessionManager2));
        pEndpoint->Release();
        pEndpoint = NULL;
    }
    if (SUCCEEDED(hr))
    {
        hr = pSessionManager2->GetAudioSessionControl(NULL, 0, &pSessionControl);
        
        pSessionManager2->Release();
        pSessionManager2 = NULL;
    }

    if (SUCCEEDED(hr))
    {
        hr = pSessionControl->QueryInterface(
                  __uuidof(IAudioSessionControl2),
                  (void**)&pSessionControl2);
                
        pSessionControl->Release();
        pSessionControl = NULL;
    }

    //  Sync the ducking state with the specified preference.

    if (SUCCEEDED(hr))
    {
        if (DuckingOptOutChecked)
        {
            hr = pSessionControl2->SetDuckingPreference(TRUE);
        }
        else
        {
            hr = pSessionControl2->SetDuckingPreference(FALSE);
        }
        pSessionControl2->Release();
        pSessionControl2 = NULL;
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

[提供自訂回避行為](providing-a-custom-ducking-experience.md)
</dt> <dt>

[回避通知的執行考慮](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[取得回避事件](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



