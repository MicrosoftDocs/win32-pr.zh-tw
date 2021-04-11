---
description: 應用程式可以選擇不使用系統所處理的預設回避體驗，並將其取代為自訂的執行。
ms.assetid: 18290d05-b114-476b-8365-6bbb5fe6cffc
title: 提供自訂回避行為
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4051dc7b79f698f10d007beaafa97e90d79f3b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111309"
---
# <a name="providing-a-custom-ducking-behavior"></a><span data-ttu-id="649fe-103">提供自訂回避行為</span><span class="sxs-lookup"><span data-stu-id="649fe-103">Providing a Custom Ducking Behavior</span></span>

<span data-ttu-id="649fe-104">應用程式可以選擇不使用系統所處理的 [預設回避體驗](stream-attenuation.md) ，並將其取代為自訂的執行。</span><span class="sxs-lookup"><span data-stu-id="649fe-104">An application can opt out of the [Default Ducking Experience](stream-attenuation.md) handled by the system and replace it with a custom implementation.</span></span>

<span data-ttu-id="649fe-105">應用程式可以提供自訂的回避體驗。</span><span class="sxs-lookup"><span data-stu-id="649fe-105">An application can provide a custom ducking experience.</span></span> <span data-ttu-id="649fe-106">例如，Windows Media Player 藉由在通訊會話期間暫停目前的媒體串流，並在會話關閉時繼續播放，來提供自己的回避體驗。</span><span class="sxs-lookup"><span data-stu-id="649fe-106">For example, Windows Media Player provides its own ducking experience by pausing the current media stream during a communication session and resuming playback when the session is closed.</span></span> <span data-ttu-id="649fe-107">Windows SDK 範例中包含了可實回避的範例媒體應用程式;如需詳細資訊，請參閱 [DuckingMediaPlayer](duckingmediaplayer.md)。</span><span class="sxs-lookup"><span data-stu-id="649fe-107">A sample media application that implements ducking is included with Windows SDK samples; for more information, see [DuckingMediaPlayer](duckingmediaplayer.md).</span></span> <span data-ttu-id="649fe-108">若要模擬開啟和關閉通訊資料流程的體驗，以及產生回避事件，請參閱 [DuckingCaptureSample](duckingcapturesample.md)，其中也包含 Windows SDK 範例中。</span><span class="sxs-lookup"><span data-stu-id="649fe-108">To simulate the experience of opening and closing communication streams, and generating ducking events, see [DuckingCaptureSample](duckingcapturesample.md), which is also included with Windows SDK samples.</span></span>

<span data-ttu-id="649fe-109">播放衰減音效的媒體應用程式，必須留意到在系統中開啟和關閉的通訊資料流程。</span><span class="sxs-lookup"><span data-stu-id="649fe-109">A media application that plays sounds to be attenuated must be aware of the communication streams, when they are opened and closed in the system.</span></span> <span data-ttu-id="649fe-110">您可以使用 MediaFoundation、DirectShow 或 DirectSound （使用核心音訊 Api）來提供自訂執行。</span><span class="sxs-lookup"><span data-stu-id="649fe-110">The custom implementation can be provided by using MediaFoundation, DirectShow, or DirectSound, which use the Core Audio APIs.</span></span> <span data-ttu-id="649fe-111">直接 WASAPI 用戶端也可以覆寫通訊會話開始和結束時的預設處理。</span><span class="sxs-lookup"><span data-stu-id="649fe-111">A direct WASAPI client can also override the default handling if it knows when the communication session starts and ends.</span></span>

<span data-ttu-id="649fe-112">**若要提供自訂的回避體驗，WASAPI 用戶端必須執行下列工作：**</span><span class="sxs-lookup"><span data-stu-id="649fe-112">**To provide a custom ducking experience, a WASAPI client must perform the following tasks:**</span></span>

1.  <span data-ttu-id="649fe-113">註冊以接收來自 *回避 manager* 的回避事件，此為音訊系統的元件，可處理與通訊流變更相關的通知。</span><span class="sxs-lookup"><span data-stu-id="649fe-113">Register to receive ducking events from the *ducking manager*—a component of the audio system that handles notifications related to communication stream changes.</span></span> <span data-ttu-id="649fe-114">如需詳細資訊，請 [取得回避事件](handling-audio-ducking-events-from-communication-devices.md)。</span><span class="sxs-lookup"><span data-stu-id="649fe-114">For more information, [Getting Ducking Events](handling-audio-ducking-events-from-communication-devices.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="649fe-115">如果用戶端已註冊接收回避通知，則回避管理員會停用系統所提供的預設行為。</span><span class="sxs-lookup"><span data-stu-id="649fe-115">If the client is gets registered to receive ducking notifications, the ducking manager disables the default behavior provided by the system.</span></span> <span data-ttu-id="649fe-116">如果停用預設行為明確 (請參閱 [停用預設回避體驗](disabling-the-ducking-experience.md)) 而用戶端未提供替代行為，則應用程式不會遇到任何回避行為。</span><span class="sxs-lookup"><span data-stu-id="649fe-116">If the default behavior is disabled explictly (see [Disabling the Default Ducking Experience](disabling-the-ducking-experience.md)) and the client does not provide a substitute behavior, the application does not experience any ducking behavior.</span></span>

     

2.  <span data-ttu-id="649fe-117">接聽回避管理員所傳送的「操作事件」通知，並執行所需的回避行為。</span><span class="sxs-lookup"><span data-stu-id="649fe-117">Listen for the duck event notifications sent by the ducking manager and perform the desired ducking behavior.</span></span> <span data-ttu-id="649fe-118">如需有關如何執行回避行為的詳細資訊，請參閱 [回避通知的執行考慮](handling-audio-ducking-events-from-communication-devices.md)。</span><span class="sxs-lookup"><span data-stu-id="649fe-118">For more information about implementing a ducking behavior, see [Implementation Considerations for Ducking Notifications](handling-audio-ducking-events-from-communication-devices.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="649fe-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="649fe-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="649fe-120">使用通訊裝置</span><span class="sxs-lookup"><span data-stu-id="649fe-120">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="649fe-121">預設回避體驗</span><span class="sxs-lookup"><span data-stu-id="649fe-121">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="649fe-122">停用預設的回避體驗</span><span class="sxs-lookup"><span data-stu-id="649fe-122">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="649fe-123">回避通知的執行考慮</span><span class="sxs-lookup"><span data-stu-id="649fe-123">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[<span data-ttu-id="649fe-124">取得回避事件</span><span class="sxs-lookup"><span data-stu-id="649fe-124">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



