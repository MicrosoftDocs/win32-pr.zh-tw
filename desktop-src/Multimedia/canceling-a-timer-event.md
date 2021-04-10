---
title: 取消計時器事件
description: 取消計時器事件
ms.assetid: 4c1be031-e3d5-4d7c-b197-c40c61fc4e2f
keywords:
- 多媒體計時器，事件
- 計時器，事件
- timeKillEvent 函式
- 取消計時器事件
- 多媒體計時器，取消事件
- 計時器，取消事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1380b2868596e0177e806f5df5217bb839abe61c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023439"
---
# <a name="canceling-a-timer-event"></a><span data-ttu-id="3e32e-109">取消計時器事件</span><span class="sxs-lookup"><span data-stu-id="3e32e-109">Canceling a Timer Event</span></span>

> [!Note]  
> <span data-ttu-id="3e32e-110">本主題說明過時的函式。</span><span class="sxs-lookup"><span data-stu-id="3e32e-110">This topic describes an obsolete function.</span></span> <span data-ttu-id="3e32e-111">新的應用程式應該使用 [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) 函式來建立計時器。</span><span class="sxs-lookup"><span data-stu-id="3e32e-111">New applications should use the [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) function to create timers.</span></span>

 

<span data-ttu-id="3e32e-112">針對透過呼叫 [**timeSetEvent**](/previous-versions//dd757634(v=vs.85))來建立的每個定期計時器，應用程式必須在釋放包含回呼函式的記憶體之前，先呼叫 [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) 函數來取消計時器。</span><span class="sxs-lookup"><span data-stu-id="3e32e-112">For every periodic timer creating by calling [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)), the application must cancel the timer by calling the [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) function before it frees the memory that contains the callback function.</span></span> <span data-ttu-id="3e32e-113">若要取消計時器事件，它可能會呼叫下列函數。</span><span class="sxs-lookup"><span data-stu-id="3e32e-113">To cancel a timer event, it might call the following function.</span></span>


```C++
void DestroyTimer(NPSEQ npSeq)
{
    if(npSeq->wTimerID) {                // is timer event pending?
        timeKillEvent(npSeq->wTimerID);  // cancel the event
        npSeq->wTimerID = 0;
    }
} 
```



## <a name="related-topics"></a><span data-ttu-id="3e32e-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="3e32e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e32e-115">使用多媒體計時器</span><span class="sxs-lookup"><span data-stu-id="3e32e-115">Using Multimedia Timers</span></span>](using-multimedia-timers.md)
</dt> </dl>

 

 