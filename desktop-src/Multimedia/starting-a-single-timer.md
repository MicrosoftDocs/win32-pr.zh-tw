---
title: 啟動單一計時器事件
description: 啟動單一計時器事件
ms.assetid: 56010877-1a02-4a7b-b58c-9f96b169acb2
keywords:
- 多媒體計時器，事件
- 計時器，事件
- 多媒體計時器，啟動事件
- 計時器，啟動事件
- timeSetEvent 函式
- 啟動計時器事件
- 單一計時器事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9d0024e3dfa9b0bda79f209abd9b81e89ad11c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375072"
---
# <a name="starting-a-single-timer-event"></a><span data-ttu-id="2d3ba-110">啟動單一計時器事件</span><span class="sxs-lookup"><span data-stu-id="2d3ba-110">Starting a Single Timer Event</span></span>

> [!Note]  
> <span data-ttu-id="2d3ba-111">本主題說明過時的函式。</span><span class="sxs-lookup"><span data-stu-id="2d3ba-111">This topic describes an obsolete function.</span></span> <span data-ttu-id="2d3ba-112">新的應用程式應該使用 [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) 函式來建立計時器。</span><span class="sxs-lookup"><span data-stu-id="2d3ba-112">New applications should use the [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) function to create timers.</span></span>

 

<span data-ttu-id="2d3ba-113">若要啟動單一計時器事件，請呼叫 [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) 函式，並指定回呼發生之前的時間量、解析度、回呼函式的位址 (查看 [**TimeProc**](/previous-versions//dd757631(v=vs.85))) ，以及要提供給回呼函數的使用者資料。</span><span class="sxs-lookup"><span data-stu-id="2d3ba-113">To start a single timer event, call the [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) function, specifying the amount of time before the callback occurs, the resolution, the address of the callback function (see [**TimeProc**](/previous-versions//dd757631(v=vs.85))), and the user data to supply with the callback function.</span></span> <span data-ttu-id="2d3ba-114">應用程式可以使用類似下列的函式來啟動單一計時器事件。</span><span class="sxs-lookup"><span data-stu-id="2d3ba-114">An application can use a function like the following to start a single timer event.</span></span>


```C++
UINT SetTimerCallback(NPSEQ npSeq,  // sequencer data
    UINT msInterval)                // event interval
{ 
    npSeq->wTimerID = timeSetEvent(
        msInterval,                    // delay
        wTimerRes,                     // resolution (global variable)
        OneShotCallback,               // callback function
        (DWORD)npSeq,                  // user data
        TIME_ONESHOT );                // single timer event
    if(! npSeq->wTimerID)
        return ERR_TIMER;
    else
        return ERR_NOERROR;
} 

```



<span data-ttu-id="2d3ba-115">如需回呼函式 OneShotCallback 的範例，請參閱 [撰寫計時器回呼函數](writing-a-timer-callback-function.md)。</span><span class="sxs-lookup"><span data-stu-id="2d3ba-115">For an example of the callback function OneShotCallback, see [Writing a Timer Callback Function](writing-a-timer-callback-function.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d3ba-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="2d3ba-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d3ba-117">使用多媒體計時器</span><span class="sxs-lookup"><span data-stu-id="2d3ba-117">Using Multimedia Timers</span></span>](using-multimedia-timers.md)
</dt> </dl>

 

 