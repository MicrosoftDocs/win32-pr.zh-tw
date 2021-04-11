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
# <a name="disabling-the-default-ducking-experience"></a><span data-ttu-id="6c14e-103">停用預設的回避體驗</span><span class="sxs-lookup"><span data-stu-id="6c14e-103">Disabling the Default Ducking Experience</span></span>

<span data-ttu-id="6c14e-104">使用者可以使用 [Windows 多媒體] 控制台的 [**通訊**] 索引標籤上可用的選項，來停用系統提供的 [預設回避體驗](stream-attenuation.md)，Mmsys.cpl。</span><span class="sxs-lookup"><span data-stu-id="6c14e-104">A user can disable the [Default Ducking Experience](stream-attenuation.md) provided by the system by using the options that are available on the **Communications** tab of the Windows multimedia control panel, Mmsys.cpl.</span></span>

<span data-ttu-id="6c14e-105">套用回避時，淡出和淡入效果的使用時間為1秒。</span><span class="sxs-lookup"><span data-stu-id="6c14e-105">When ducking is applied, a fade-out and fade-in effect is used for a period of 1 second.</span></span> <span data-ttu-id="6c14e-106">遊戲應用程式可能不希望通訊串流干擾遊戲音訊。</span><span class="sxs-lookup"><span data-stu-id="6c14e-106">A game application might not want the communication stream to interfere with the game audio.</span></span> <span data-ttu-id="6c14e-107">有些媒體應用程式可能會發現播放體驗會在音樂淡入時 jarring。</span><span class="sxs-lookup"><span data-stu-id="6c14e-107">Some media applications might find that the playback experience is jarring when music fades back in.</span></span> <span data-ttu-id="6c14e-108">這些類型的應用程式可以選擇不參與回避體驗。</span><span class="sxs-lookup"><span data-stu-id="6c14e-108">These types of applications can choose not to participate in the ducking experience.</span></span>

<span data-ttu-id="6c14e-109">直接 WASAPI 用戶端可以透過程式設計的方式，使用針對非通訊資料流程提供音量控制之音訊會話的會話管理員，退出宣告。</span><span class="sxs-lookup"><span data-stu-id="6c14e-109">Programmatically, a direct WASAPI client can opt out by using the session manager for the audio session that provides volume control for the non-communication streams.</span></span> <span data-ttu-id="6c14e-110">請注意，即使用戶端退出宣告回避，它仍會接收來自系統的回避通知。</span><span class="sxs-lookup"><span data-stu-id="6c14e-110">Note that even if an client opts out of ducking, it still receives ducking notifications from the system.</span></span>

<span data-ttu-id="6c14e-111">若要退出宣告回避，用戶端必須取得會話管理員的 [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) 介面參考。</span><span class="sxs-lookup"><span data-stu-id="6c14e-111">To opt out of ducking, the client must get a reference to the [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) interface of the session manager.</span></span> <span data-ttu-id="6c14e-112">若要退出回避體驗，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="6c14e-112">To opt out of the ducking experience, use the following steps:</span></span>

1.  <span data-ttu-id="6c14e-113">將裝置列舉值具現化，並使用它來取得媒體應用程式用來呈現非通訊資料流程之裝置端點的參考。</span><span class="sxs-lookup"><span data-stu-id="6c14e-113">Instantiate the device enumerator and use it to get a reference to the endpoint of the device that the media application is using to render the non-communication stream.</span></span>
2.  <span data-ttu-id="6c14e-114">從裝置端點啟用會話管理員，並取得會話管理員的 [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) 介面參考。</span><span class="sxs-lookup"><span data-stu-id="6c14e-114">Activate the session manager from the device endpoint and get a reference to the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) interface of the session manager.</span></span>
3.  <span data-ttu-id="6c14e-115">藉由使用 [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) 指標，取得會話管理員之 [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) 介面的參考。</span><span class="sxs-lookup"><span data-stu-id="6c14e-115">By using the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) pointer, get a reference to the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface of the session manager.</span></span>
4.  <span data-ttu-id="6c14e-116">從 [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)介面查詢 [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) 。</span><span class="sxs-lookup"><span data-stu-id="6c14e-116">Query for the [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) from the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface.</span></span>
5.  <span data-ttu-id="6c14e-117">呼叫 [**IAudioSessionControl2：： SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference) 並傳遞 **TRUE** 或 **FALSE** ，以指定回避喜好設定。</span><span class="sxs-lookup"><span data-stu-id="6c14e-117">Call [**IAudioSessionControl2::SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference) and pass **TRUE** or **FALSE** to specify the ducking preference.</span></span> <span data-ttu-id="6c14e-118">在會話期間，您可以動態變更指定的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="6c14e-118">The specified preference can be changed dynamically during the session.</span></span> <span data-ttu-id="6c14e-119">請注意，在資料流程停止並重新啟動之前，退出變更不會生效。</span><span class="sxs-lookup"><span data-stu-id="6c14e-119">Note that the opt-out change does not take effect until the stream is stopped and started again.</span></span>

<span data-ttu-id="6c14e-120">下列程式碼顯示應用程式如何指定其回避喜好設定。</span><span class="sxs-lookup"><span data-stu-id="6c14e-120">The following code shows how an application can specify its ducking preference.</span></span> <span data-ttu-id="6c14e-121">函數的呼叫端必須在 DuckingOptOutChecked 參數中傳遞 **TRUE** 或 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="6c14e-121">The caller of the function must pass **TRUE** or **FALSE** in the DuckingOptOutChecked parameter.</span></span> <span data-ttu-id="6c14e-122">根據傳遞的值，回避會透過 [**IAudioSessionControl2：： SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference)啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="6c14e-122">Depending on the value passed, ducking is enabled or disabled through the [**IAudioSessionControl2::SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6c14e-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="6c14e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c14e-124">使用通訊裝置</span><span class="sxs-lookup"><span data-stu-id="6c14e-124">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="6c14e-125">預設回避體驗</span><span class="sxs-lookup"><span data-stu-id="6c14e-125">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="6c14e-126">提供自訂回避行為</span><span class="sxs-lookup"><span data-stu-id="6c14e-126">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="6c14e-127">回避通知的執行考慮</span><span class="sxs-lookup"><span data-stu-id="6c14e-127">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[<span data-ttu-id="6c14e-128">取得回避事件</span><span class="sxs-lookup"><span data-stu-id="6c14e-128">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



