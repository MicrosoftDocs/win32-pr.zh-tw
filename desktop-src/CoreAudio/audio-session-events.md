---
description: 音訊會話事件
ms.assetid: 6943b405-0807-412b-a149-fc3a8ece1b48
title: 音訊會話事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ec5de18c883f817c2f650ccfc48ad0149ac84e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936298"
---
# <a name="audio-session-events"></a><span data-ttu-id="5d639-103">音訊會話事件</span><span class="sxs-lookup"><span data-stu-id="5d639-103">Audio Session Events</span></span>

<span data-ttu-id="5d639-104">管理共用模式音訊串流的應用程式可以註冊，以便在會話事件發生時收到通知。</span><span class="sxs-lookup"><span data-stu-id="5d639-104">An application that manages shared-mode audio streams can register to receive notifications when session events occur.</span></span> <span data-ttu-id="5d639-105">如先前所述，每個串流都屬於 [音訊會話](audio-sessions.md)。</span><span class="sxs-lookup"><span data-stu-id="5d639-105">As explained previously, each stream belongs to an [audio session](audio-sessions.md).</span></span> <span data-ttu-id="5d639-106">會話事件是由音訊會話的狀態變更所起始。</span><span class="sxs-lookup"><span data-stu-id="5d639-106">A session event is initiated by a change in the status of an audio session.</span></span>

<span data-ttu-id="5d639-107">用戶端應用程式可以註冊以接收下列會話事件種類的通知：</span><span class="sxs-lookup"><span data-stu-id="5d639-107">A client application can register to receive notifications of the following types of session events:</span></span>

-   <span data-ttu-id="5d639-108">會話 submix 的主要磁片區層級或靜音狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="5d639-108">The master volume level or muting state of the session submix has changed.</span></span>
-   <span data-ttu-id="5d639-109">會話 submix 中一或多個通道的音量層級已變更。</span><span class="sxs-lookup"><span data-stu-id="5d639-109">The volume level of one or more channels of the session submix has changed.</span></span>
-   <span data-ttu-id="5d639-110">會話已中斷連線。</span><span class="sxs-lookup"><span data-stu-id="5d639-110">The session has been disconnected.</span></span>
-   <span data-ttu-id="5d639-111">會話的活動狀態已變更為 [作用中]、[非使用中] 或 [已過期]。</span><span class="sxs-lookup"><span data-stu-id="5d639-111">The activity state of the session has changed to active, inactive, or expired.</span></span>
-   <span data-ttu-id="5d639-112">已為會話指派新的群組參數。</span><span class="sxs-lookup"><span data-stu-id="5d639-112">The session has been assigned a new grouping parameter.</span></span>
-   <span data-ttu-id="5d639-113">會話的使用者介面屬性 (圖示或顯示名稱) 已變更。</span><span class="sxs-lookup"><span data-stu-id="5d639-113">A user-interface property of the session (icon or display name) has changed.</span></span>

<span data-ttu-id="5d639-114">用戶端會透過其 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) 介面執行中的方法，接收這些事件的通知。</span><span class="sxs-lookup"><span data-stu-id="5d639-114">The client receives notifications of these events through the methods in its implementation of the [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface.</span></span> <span data-ttu-id="5d639-115">不同于 WASAPI 中由 WASAPI 系統模組所執行的其他介面，用戶端會執行 **IAudioSessionEvents**。</span><span class="sxs-lookup"><span data-stu-id="5d639-115">Unlike the other interfaces in WASAPI, which are implemented by the WASAPI system module, the client implements **IAudioSessionEvents**.</span></span> <span data-ttu-id="5d639-116">當會話事件發生時，此介面中的方法會接收來自 WASAPI 系統模組的回呼。</span><span class="sxs-lookup"><span data-stu-id="5d639-116">The methods in this interface receive callbacks from the WASAPI system module when session events occur.</span></span>

<span data-ttu-id="5d639-117">若要開始接收通知，用戶端會呼叫 [**IAudioSessionControl：： RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) 方法來註冊其 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) 介面。</span><span class="sxs-lookup"><span data-stu-id="5d639-117">To begin receiving notifications, the client calls the [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) method to register its [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface.</span></span> <span data-ttu-id="5d639-118">當用戶端不再需要通知時，它會呼叫 [**IAudioSessionControl：： UnregisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-unregisteraudiosessionnotification) 方法來刪除註冊。</span><span class="sxs-lookup"><span data-stu-id="5d639-118">When the client no longer requires notifications, it calls the [**IAudioSessionControl::UnregisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-unregisteraudiosessionnotification) method to delete the registration.</span></span>

<span data-ttu-id="5d639-119">下列程式碼範例顯示 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) 介面的可能實作為：</span><span class="sxs-lookup"><span data-stu-id="5d639-119">The following code example shows a possible implementation of the [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface:</span></span>


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



<span data-ttu-id="5d639-120">上述程式碼範例中的 CAudioSessionEvents 類別是 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) 介面的實作為。</span><span class="sxs-lookup"><span data-stu-id="5d639-120">The CAudioSessionEvents class in the preceding code example is an implementation of the [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface.</span></span> <span data-ttu-id="5d639-121">這種特定的執行可能是主控台應用程式的一部分，會將會話事件的相關資訊列印到 [命令提示字元] 視窗。</span><span class="sxs-lookup"><span data-stu-id="5d639-121">This particular implementation might be part of a console application that prints information about session events to a Command Prompt window.</span></span> <span data-ttu-id="5d639-122">由於 **IAudioSessionEvents** 繼承自 [**iunknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)，因此類別定義包含 **iunknown** 方法 [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref)、 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)和 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))的實作為。</span><span class="sxs-lookup"><span data-stu-id="5d639-122">Because **IAudioSessionEvents** inherits from [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), the class definition contains implementations of the **IUnknown** methods [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), and [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="5d639-123">類別定義中其餘的公用方法是 **IAudioSessionEvents** 介面專用的。</span><span class="sxs-lookup"><span data-stu-id="5d639-123">The remaining public methods in the class definition are specific to the **IAudioSessionEvents** interface.</span></span>

<span data-ttu-id="5d639-124">某些用戶端可能不會想要監視所有類型的會話事件。</span><span class="sxs-lookup"><span data-stu-id="5d639-124">Some clients might not be interested in monitoring all types of session events.</span></span> <span data-ttu-id="5d639-125">在上述程式碼範例中，CAudioSessionEvents 類別中的數個通知方法不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="5d639-125">In the preceding code example, several notification methods in the CAudioSessionEvents class do nothing.</span></span> <span data-ttu-id="5d639-126">例如， [**OnChannelVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged) 方法不會執行任何動作，除了傳回狀態碼「 \_ 確定」。</span><span class="sxs-lookup"><span data-stu-id="5d639-126">For example, the [**OnChannelVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged) method does nothing except to return status code S\_OK.</span></span> <span data-ttu-id="5d639-127">此應用程式不會監視通道磁片區，因為它不會藉由呼叫 [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) 介面中的方法來變更通道磁片區 () ，且它不會與其他可能變更通道磁片區的應用程式共用會話。</span><span class="sxs-lookup"><span data-stu-id="5d639-127">This application does not monitor channel volumes because it does not change the channel volumes (by calling the methods in the [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) interface), and it does not share the session with other applications that might change the channel volumes.</span></span>

<span data-ttu-id="5d639-128">CAudioSessionEvents 類別中唯一會通知使用者會話事件的三個方法為 [**OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged)、 [**OnStateChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onstatechanged)和 [**OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected)。</span><span class="sxs-lookup"><span data-stu-id="5d639-128">The only three methods in the CAudioSessionEvents class that notify the user of session events are [**OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged), [**OnStateChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onstatechanged), and [**OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected).</span></span> <span data-ttu-id="5d639-129">例如，如果使用者執行系統音量控制項程式 Sndvol，並使用 Sndvol 中的音量控制項來變更應用程式的磁片區層級，則會 `OnSimpleVolumeChanged` 立即列印新的磁片區層級。</span><span class="sxs-lookup"><span data-stu-id="5d639-129">For example, if the user runs the system volume-control program, Sndvol, and uses the volume control in Sndvol to change the application's volume level, `OnSimpleVolumeChanged` immediately prints the new volume level.</span></span>

<span data-ttu-id="5d639-130">如需註冊及取消註冊用戶端 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) 介面的程式碼範例，請參閱 [舊版音訊應用程式的音訊事件](audio-events-for-legacy-audio-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="5d639-130">For a code example that registers and unregisters a client's [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface, see [Audio Events for Legacy Audio Applications](audio-events-for-legacy-audio-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d639-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="5d639-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d639-132">音訊會話</span><span class="sxs-lookup"><span data-stu-id="5d639-132">Audio Sessions</span></span>](audio-sessions.md)
</dt> </dl>

 

 
