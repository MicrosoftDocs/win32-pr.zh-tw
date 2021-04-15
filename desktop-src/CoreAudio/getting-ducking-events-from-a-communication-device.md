---
description: 如果媒體應用程式想要提供可定制的回避體驗，則必須在系統中開啟或關閉通訊資料流程時接聽事件通知。
ms.assetid: 709ad912-6b03-4ad3-bc47-ad8b6bd6de45
title: 取得回避事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e45557c25570a89452a39683a0b6732b9632129
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510592"
---
# <a name="getting-ducking-events"></a><span data-ttu-id="60773-103">取得回避事件</span><span class="sxs-lookup"><span data-stu-id="60773-103">Getting Ducking Events</span></span>

<span data-ttu-id="60773-104">如果媒體應用程式想要提供可定制的回避體驗，則必須在系統中開啟或關閉通訊資料流程時接聽事件通知。</span><span class="sxs-lookup"><span data-stu-id="60773-104">A media application that wants to provide a customised ducking experience must listen for the event notifications when a communication stream is opened or closed in the system.</span></span> <span data-ttu-id="60773-105">您可以使用 MediaFoundation、DirectShow 或 DirectSound （使用核心音訊 Api）來提供自訂執行。</span><span class="sxs-lookup"><span data-stu-id="60773-105">The custom implementation can be provided by using MediaFoundation, DirectShow, or DirectSound, which use the Core Audio APIs.</span></span> <span data-ttu-id="60773-106">直接 WASAPI 用戶端也可以覆寫通訊會話開始和結束時的預設處理。</span><span class="sxs-lookup"><span data-stu-id="60773-106">A direct WASAPI client can also override the default handling if it knows when the communication session starts and ends.</span></span>

<span data-ttu-id="60773-107">若要提供自訂的執行，媒體應用程式必須在通訊應用程式啟動或結束通訊串流時，從系統取得通知。</span><span class="sxs-lookup"><span data-stu-id="60773-107">To provide a custom implementation, a media application needs to get notifications from the system when a communication application starts or ends a communication stream.</span></span> <span data-ttu-id="60773-108">媒體應用程式必須執行 [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) 介面，並向音訊系統註冊執行。</span><span class="sxs-lookup"><span data-stu-id="60773-108">The media application must implement the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) interface and register the implementation with the audio system.</span></span> <span data-ttu-id="60773-109">成功註冊之後，媒體應用程式會透過介面中的方法，以回呼的形式接收事件通知。</span><span class="sxs-lookup"><span data-stu-id="60773-109">Upon successful registration, the media application receives event notifications in the form of callbacks through the methods in the interface.</span></span> <span data-ttu-id="60773-110">如需詳細資訊，請參閱 [回避通知的執行考慮](handling-audio-ducking-events-from-communication-devices.md)。</span><span class="sxs-lookup"><span data-stu-id="60773-110">For more information, see [Implementation Considerations for Ducking Notifications](handling-audio-ducking-events-from-communication-devices.md).</span></span>

<span data-ttu-id="60773-111">若要傳送回避通知，音訊系統必須知道哪一個音訊會話正在接聽回避事件。</span><span class="sxs-lookup"><span data-stu-id="60773-111">To send ducking notifications, the audio system must know which audio session is listening for the ducking events.</span></span> <span data-ttu-id="60773-112">每個音訊會話都會使用 GUID （會話實例識別碼）來唯一識別。</span><span class="sxs-lookup"><span data-stu-id="60773-112">Each audio session is uniquely identified with a GUID—session instance identifier.</span></span> <span data-ttu-id="60773-113">會話管理員可讓應用程式取得會話的相關資訊，例如音訊會話的標題、轉譯狀態和會話實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="60773-113">The session manager allows an application to get information about the session such as title of audio session, the rendering state, and the session instance identifier.</span></span> <span data-ttu-id="60773-114">您可以使用原則控制介面 [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2)來取出識別碼。</span><span class="sxs-lookup"><span data-stu-id="60773-114">The identifier can be retrieved by using the policy control interface, [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2).</span></span>

<span data-ttu-id="60773-115">下列步驟摘要說明取得媒體應用程式之會話實例識別碼的流程：</span><span class="sxs-lookup"><span data-stu-id="60773-115">The following steps summarize the process of getting the session instance identifier of the media application:</span></span>

1.  <span data-ttu-id="60773-116">將裝置列舉值具現化，並使用它來取得媒體應用程式用來呈現非通訊資料流程之裝置端點的參考。</span><span class="sxs-lookup"><span data-stu-id="60773-116">Instantiate the device enumerator and use it to get a reference to the endpoint of the device that the media application is using to render the non-communication stream.</span></span>
2.  <span data-ttu-id="60773-117">從裝置端點啟用會話管理員，並取得會話管理員的 [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) 介面參考。</span><span class="sxs-lookup"><span data-stu-id="60773-117">Activate the session manager from the device endpoint and get a reference to the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) interface of the session manager.</span></span>
3.  <span data-ttu-id="60773-118">藉由使用 [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) 指標，取得會話管理員之 [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) 介面的參考。</span><span class="sxs-lookup"><span data-stu-id="60773-118">By using the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) pointer, get a reference to the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface of the session manager.</span></span>
4.  <span data-ttu-id="60773-119">從 [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)介面查詢 [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) 。</span><span class="sxs-lookup"><span data-stu-id="60773-119">Query for the [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) from the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface.</span></span>
5.  <span data-ttu-id="60773-120">呼叫 [**IAudioSessionControl2：： GetSessionInstanceIdentifier**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier) ，並取出包含目前音訊會話之會話識別碼的字串。</span><span class="sxs-lookup"><span data-stu-id="60773-120">Call [**IAudioSessionControl2::GetSessionInstanceIdentifier**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier) and retrieve a string that contains the session identifier for the current audio session.</span></span>

<span data-ttu-id="60773-121">為了取得有關通訊串流的回避通知，媒體應用程式會呼叫 [**IAudioSessionManager2：： RegisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification)。</span><span class="sxs-lookup"><span data-stu-id="60773-121">To get ducking notifications about communication streams, the media application calls [**IAudioSessionManager2::RegisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification).</span></span> <span data-ttu-id="60773-122">媒體應用程式會將其會話實例識別碼提供給音訊系統，並將指標提供給 [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) 的執行。</span><span class="sxs-lookup"><span data-stu-id="60773-122">The media application supplies its session instance identifier to the audio system and a pointer to the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) implementation.</span></span> <span data-ttu-id="60773-123">應用程式現在可以在通訊裝置上開啟串流時，接收事件通知。</span><span class="sxs-lookup"><span data-stu-id="60773-123">The application can now receive event notification when a stream opened on the communication device.</span></span> <span data-ttu-id="60773-124">若要停止取得通知，媒體應用程式必須呼叫 [**IAudioSessionManager2：： UnregisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregisterducknotification)。</span><span class="sxs-lookup"><span data-stu-id="60773-124">To stop getting notification, the media application must call [**IAudioSessionManager2::UnregisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregisterducknotification).</span></span>

<span data-ttu-id="60773-125">下列程式碼顯示應用程式如何註冊以取得回避通知。</span><span class="sxs-lookup"><span data-stu-id="60773-125">The following code shows how an application can register to get ducking notifications.</span></span> <span data-ttu-id="60773-126">CMediaPlayer 類別是在 [回避通知的執行考慮](handling-audio-ducking-events-from-communication-devices.md)中定義。</span><span class="sxs-lookup"><span data-stu-id="60773-126">The CMediaPlayer class is defined in [Implementation Considerations for Ducking Notifications](handling-audio-ducking-events-from-communication-devices.md).</span></span> <span data-ttu-id="60773-127">[DuckingMediaPlayer](duckingmediaplayer.md)範例會實行此功能。</span><span class="sxs-lookup"><span data-stu-id="60773-127">The [DuckingMediaPlayer](duckingmediaplayer.md) sample implements this functionality.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="60773-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="60773-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60773-129">使用通訊裝置</span><span class="sxs-lookup"><span data-stu-id="60773-129">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="60773-130">預設回避體驗</span><span class="sxs-lookup"><span data-stu-id="60773-130">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="60773-131">停用預設的回避體驗</span><span class="sxs-lookup"><span data-stu-id="60773-131">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="60773-132">提供自訂回避行為</span><span class="sxs-lookup"><span data-stu-id="60773-132">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="60773-133">回避通知的執行考慮</span><span class="sxs-lookup"><span data-stu-id="60773-133">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> </dl>

 

 



