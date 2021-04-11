---
description: 系統所提供的預設回避體驗會 ducks 通訊串流開啟時，系統中所有可用的非通訊串流。
ms.assetid: 1b92574e-7cde-49c0-a68e-223492412361
title: 回避通知的執行考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3de07ea23b7cdc8d726ab68a5a6554bf1713a921
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110937"
---
# <a name="implementation-considerations-for-ducking-notifications"></a><span data-ttu-id="c4315-103">回避通知的執行考慮</span><span class="sxs-lookup"><span data-stu-id="c4315-103">Implementation Considerations for Ducking Notifications</span></span>

<span data-ttu-id="c4315-104">系統所提供的 [預設回避體驗](stream-attenuation.md) 會 ducks 通訊串流開啟時，系統中所有可用的非通訊串流。</span><span class="sxs-lookup"><span data-stu-id="c4315-104">The [Default Ducking Experience](stream-attenuation.md) provided by the system ducks all non-communication streams available in the system when a communication stream opens.</span></span> <span data-ttu-id="c4315-105">如果媒體應用程式知道通訊會話的開始和結束時間，就可以覆寫預設處理。</span><span class="sxs-lookup"><span data-stu-id="c4315-105">A media application can override the default handling if it knows when the communication session starts and ends.</span></span>

<span data-ttu-id="c4315-106">請考慮 [DuckingMediaPlayer](duckingmediaplayer.md) 範例中的媒體應用程式所執行的案例。</span><span class="sxs-lookup"><span data-stu-id="c4315-106">Consider the scenario implemented by the media application in the [DuckingMediaPlayer](duckingmediaplayer.md) sample.</span></span> <span data-ttu-id="c4315-107">應用程式會在收到未發出通知時，暫停現正播放的音訊串流，並在收到 unduck 通知時繼續播放。</span><span class="sxs-lookup"><span data-stu-id="c4315-107">The application pauses the audio stream that it is playing when it receives a duck notification and continues playback when it receives an unduck notification.</span></span> <span data-ttu-id="c4315-108">暫停和繼續事件會反映在媒體應用程式的使用者介面中。</span><span class="sxs-lookup"><span data-stu-id="c4315-108">The pause and continue events are reflected in the media application's user interface.</span></span> <span data-ttu-id="c4315-109">您可以透過兩個應用程式定義的視窗訊息、WM \_ 應用程式 \_ 會話 \_ DUCKED 和 wm \_ 應用程式 \_ 會話 \_ UNDUCKED 來支援此功能。</span><span class="sxs-lookup"><span data-stu-id="c4315-109">This is supported through two application-defined window messages, WM\_APP\_SESSION\_DUCKED and WM\_APP\_SESSION\_UNDUCKED.</span></span> <span data-ttu-id="c4315-110">回避通知會在背景中以非同步方式接收，而媒體應用程式不得封鎖通知執行緒來處理視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="c4315-110">The ducking notifications are received asynchronously in the background and the media application must not block the notification thread to process the window messages.</span></span> <span data-ttu-id="c4315-111">視窗訊息必須在使用者介面執行緒上處理。</span><span class="sxs-lookup"><span data-stu-id="c4315-111">The window messages must be processed on the user interface thread.</span></span>

<span data-ttu-id="c4315-112">回避行為會透過通知機制運作。</span><span class="sxs-lookup"><span data-stu-id="c4315-112">The ducking behavior works through a notification mechanism.</span></span> <span data-ttu-id="c4315-113">為了提供自訂的體驗，媒體應用程式必須執行 [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) 介面，並向音訊系統註冊執行。</span><span class="sxs-lookup"><span data-stu-id="c4315-113">To provide a customized experience, the media application must implement the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) interface and register the implementation with the audio system.</span></span> <span data-ttu-id="c4315-114">成功註冊之後，媒體應用程式會透過介面中的方法，以回呼的形式接收事件通知。</span><span class="sxs-lookup"><span data-stu-id="c4315-114">Upon successful registration, the media application receives event notifications in the form of callbacks through the methods in the interface.</span></span> <span data-ttu-id="c4315-115">處理通訊會話的會話管理員會在通訊串流開啟時呼叫 [**IAudioVolumeDuckNotification：： OnVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeducknotification) ，然後在通訊裝置上關閉資料流程時呼叫 [**IAudioVolumeDuckNotification：： OnVolumeUnduckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeunducknotification) 。</span><span class="sxs-lookup"><span data-stu-id="c4315-115">The session manager handling the communication session calls [**IAudioVolumeDuckNotification::OnVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeducknotification) when the communication stream opens and then calls [**IAudioVolumeDuckNotification::OnVolumeUnduckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeunducknotification) when the stream is closed on the communication device.</span></span>

<span data-ttu-id="c4315-116">下列程式碼顯示 [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) 介面的範例執行。</span><span class="sxs-lookup"><span data-stu-id="c4315-116">The following code shows a sample implementation of the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) interface.</span></span> <span data-ttu-id="c4315-117">如需 CMediaPlayer 的定義：:D uckingOptOut，請參閱從通訊裝置取得回避事件。</span><span class="sxs-lookup"><span data-stu-id="c4315-117">For the definition of CMediaPlayer::DuckingOptOut, see Getting Ducking Events from a Communication Device.</span></span>


```C++
class CMediaPlayer : public IAudioVolumeDuckNotification
{
    LONG _refCount;

    HWND _AppWindow;

    ~CMediaPlayer();

    STDMETHOD(OnVolumeDuckNotification) (LPCWSTR sessionID, 
                  UINT32 countCommunicationSessions);
    STDMETHOD(OnVolumeUnduckNotification) (LPCWSTR sessionID);

public:
    CDuckingImpl(HWND hWnd);
    HRESULT DuckingOptOut(bool GetDuckEvents);

    // IUnknown
    IFACEMETHODIMP QueryInterface(__in REFIID riid, __deref_out void **ppv);
    IFACEMETHODIMP_(ULONG) AddRef();
    IFACEMETHODIMP_(ULONG) Release();
};

CMediaPlayer::CMediaPlayer(HWND AppWindow) :
        _AppWindow(AppWindow),
        _refCount(1)
{
}
CMediaPlayer::~CMediaPlayer()
{
}

// When we receive a duck notification, 
// post a "Session Ducked" message to the application window.

STDMETHODIMP CMediaPlayer::OnVolumeDuckNotification(LPCWSTR SessionID, 
                                                    UINT32 CountCommunicationsSessions)
{
    PostMessage(_AppWindow, WM_APP_SESSION_DUCKED, 0, 0);
    return 0;
}


// When we receive an unduck notification, 
// post a "Session Unducked" message to the application window.

STDMETHODIMP CMediaPlayer::OnVolumeUnduckNotification(LPCWSTR SessionID)
{
    PostMessage(_AppWindow, WM_APP_SESSION_UNDUCKED, 0, 0);
    return 0;
}

IFACEMETHODIMP CMediaPlayer::QueryInterface(REFIID iid, void **pvObject)
{
    if (pvObject == NULL)
    {
        return E_POINTER;
    }
    *pvObject = NULL;
    if (iid == IID_IUnknown)
    {
        *pvObject = static_cast<IUnknown *>(static_cast<IAudioVolumeDuckNotification *>
                                                                              (this));
        AddRef();
    }
    else if (iid == __uuidof(IAudioVolumeDuckNotification))
    {
        *pvObject = static_cast<IAudioVolumeDuckNotification *>(this);
        AddRef();
    }
    else
    {
        return E_NOINTERFACE;
    }
    return S_OK;
}

IFACEMETHODIMP_(ULONG) CMediaPlayer::AddRef()
{
    return InterlockedIncrement(&_refCount);
}

IFACEMETHODIMP_(ULONG) CMediaPlayer::Release()
{
    LONG refs = InterlockedDecrement(&_refCount);

    if (refs == 0)
    {
        delete this; 
    }

    return refs;   
}
```



## <a name="related-topics"></a><span data-ttu-id="c4315-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="c4315-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4315-119">使用通訊裝置</span><span class="sxs-lookup"><span data-stu-id="c4315-119">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="c4315-120">預設回避體驗</span><span class="sxs-lookup"><span data-stu-id="c4315-120">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="c4315-121">停用預設的回避體驗</span><span class="sxs-lookup"><span data-stu-id="c4315-121">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="c4315-122">提供自訂回避行為</span><span class="sxs-lookup"><span data-stu-id="c4315-122">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="c4315-123">取得回避事件</span><span class="sxs-lookup"><span data-stu-id="c4315-123">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



