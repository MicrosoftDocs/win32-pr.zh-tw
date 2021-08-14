---
description: 音訊會話事件
ms.assetid: 6943b405-0807-412b-a149-fc3a8ece1b48
title: 音訊會話事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf0c3441a7f6f6835070a530c4ebb8985354b2701f312f2f085c5e449f12cbf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407222"
---
# <a name="audio-session-events"></a>音訊會話事件

管理共用模式音訊串流的應用程式可以註冊，以便在會話事件發生時收到通知。 如先前所述，每個串流都屬於 [音訊會話](audio-sessions.md)。 會話事件是由音訊會話的狀態變更所起始。

用戶端應用程式可以註冊以接收下列會話事件種類的通知：

-   會話 submix 的主要磁片區層級或靜音狀態已變更。
-   會話 submix 中一或多個通道的音量層級已變更。
-   會話已中斷連線。
-   會話的活動狀態已變更為 [作用中]、[非使用中] 或 [已過期]。
-   已為會話指派新的群組參數。
-   會話的使用者介面屬性 (圖示或顯示名稱) 已變更。

用戶端會透過其 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) 介面執行中的方法，接收這些事件的通知。 不同于 WASAPI 中由 WASAPI 系統模組所執行的其他介面，用戶端會執行 **IAudioSessionEvents**。 當會話事件發生時，此介面中的方法會接收來自 WASAPI 系統模組的回呼。

若要開始接收通知，用戶端會呼叫 [**IAudioSessionControl：： RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) 方法來註冊其 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) 介面。 當用戶端不再需要通知時，它會呼叫 [**IAudioSessionControl：： UnregisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-unregisteraudiosessionnotification) 方法來刪除註冊。

下列程式碼範例顯示 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) 介面的可能實作為：


```C++
//-----------------------------------------------------------
// Client implementation of IAudioSessionEvents interface.
// WASAPI calls these methods to notify the application when
// a parameter or property of the audio session changes.
//-----------------------------------------------------------
class CAudioSessionEvents : public IAudioSessionEvents
{
    LONG _cRef;

public:
    CAudioSessionEvents() :
        _cRef(1)
    {
    }

    ~CAudioSessionEvents()
    {
    }

    // IUnknown methods -- AddRef, Release, and QueryInterface

    ULONG STDMETHODCALLTYPE AddRef()
    {
        return InterlockedIncrement(&_cRef);
    }

    ULONG STDMETHODCALLTYPE Release()
    {
        ULONG ulRef = InterlockedDecrement(&_cRef);
        if (0 == ulRef)
        {
            delete this;
        }
        return ulRef;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(
                                REFIID  riid,
                                VOID  **ppvInterface)
    {
        if (IID_IUnknown == riid)
        {
            AddRef();
            *ppvInterface = (IUnknown*)this;
        }
        else if (__uuidof(IAudioSessionEvents) == riid)
        {
            AddRef();
            *ppvInterface = (IAudioSessionEvents*)this;
        }
        else
        {
            *ppvInterface = NULL;
            return E_NOINTERFACE;
        }
        return S_OK;
    }

    // Notification methods for audio session events

    HRESULT STDMETHODCALLTYPE OnDisplayNameChanged(
                                LPCWSTR NewDisplayName,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnIconPathChanged(
                                LPCWSTR NewIconPath,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnSimpleVolumeChanged(
                                float NewVolume,
                                BOOL NewMute,
                                LPCGUID EventContext)
    {
        if (NewMute)
        {
            printf("MUTE\n");
        }
        else
        {
            printf("Volume = %d percent\n",
                   (UINT32)(100*NewVolume + 0.5));
        }

        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnChannelVolumeChanged(
                                DWORD ChannelCount,
                                float NewChannelVolumeArray[],
                                DWORD ChangedChannel,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnGroupingParamChanged(
                                LPCGUID NewGroupingParam,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnStateChanged(
                                AudioSessionState NewState)
    {
        char *pszState = "?????";

        switch (NewState)
        {
        case AudioSessionStateActive:
            pszState = "active";
            break;
        case AudioSessionStateInactive:
            pszState = "inactive";
            break;
        }
        printf("New session state = %s\n", pszState);

        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnSessionDisconnected(
              AudioSessionDisconnectReason DisconnectReason)
    {
        char *pszReason = "?????";

        switch (DisconnectReason)
        {
        case DisconnectReasonDeviceRemoval:
            pszReason = "device removed";
            break;
        case DisconnectReasonServerShutdown:
            pszReason = "server shut down";
            break;
        case DisconnectReasonFormatChanged:
            pszReason = "format changed";
            break;
        case DisconnectReasonSessionLogoff:
            pszReason = "user logged off";
            break;
        case DisconnectReasonSessionDisconnected:
            pszReason = "session disconnected";
            break;
        case DisconnectReasonExclusiveModeOverride:
            pszReason = "exclusive-mode override";
            break;
        }
        printf("Audio session disconnected (reason: %s)\n",
               pszReason);

        return S_OK;
    }
};
```



上述程式碼範例中的 CAudioSessionEvents 類別是 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) 介面的實作為。 這種特定的執行可能是主控台應用程式的一部分，會將會話事件的相關資訊列印到 [命令提示字元] 視窗。 由於 **IAudioSessionEvents** 繼承自 [**iunknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)，因此類別定義包含 **iunknown** 方法 [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref)、 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)和 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))的實作為。 類別定義中其餘的公用方法是 **IAudioSessionEvents** 介面專用的。

某些用戶端可能不會想要監視所有類型的會話事件。 在上述程式碼範例中，CAudioSessionEvents 類別中的數個通知方法不會執行任何動作。 例如， [**OnChannelVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged) 方法不會執行任何動作，除了傳回狀態碼「 \_ 確定」。 此應用程式不會監視通道磁片區，因為它不會藉由呼叫 [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) 介面中的方法來變更通道磁片區 () ，且它不會與其他可能變更通道磁片區的應用程式共用會話。

CAudioSessionEvents 類別中唯一會通知使用者會話事件的三個方法為 [**OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged)、 [**OnStateChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onstatechanged)和 [**OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected)。 例如，如果使用者執行系統音量控制項程式 Sndvol，並使用 Sndvol 中的音量控制項來變更應用程式的磁片區層級，則會 `OnSimpleVolumeChanged` 立即列印新的磁片區層級。

如需註冊及取消註冊用戶端 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) 介面的程式碼範例，請參閱 [舊版音訊應用程式的音訊事件](audio-events-for-legacy-audio-applications.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊會話](audio-sessions.md)
</dt> </dl>

 

 
