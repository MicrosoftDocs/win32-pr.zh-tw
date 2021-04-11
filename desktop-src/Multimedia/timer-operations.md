---
title: 計時器事件作業
description: 計時器事件作業
ms.assetid: a2b75e84-4da8-449f-b02a-4ffc4846eef5
keywords:
- 多媒體計時器，事件
- 計時器，事件
- timeSetEvent 函式
- timeKillEvent 函式
- 啟動計時器事件
- 單一計時器事件
- 定期計時器事件
- 取消計時器事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1d4329a6d6c55e9e8dd6c56fab5d1e3ca938833
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681732"
---
# <a name="timer-event-operations"></a><span data-ttu-id="56e22-111">計時器事件作業</span><span class="sxs-lookup"><span data-stu-id="56e22-111">Timer Event Operations</span></span>

<span data-ttu-id="56e22-112">建立應用程式的計時器解析度之後，您可以使用 [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) 函式來啟動計時器事件。</span><span class="sxs-lookup"><span data-stu-id="56e22-112">After you have established your application's timer resolution, you can start timer events by using the [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) function.</span></span> <span data-ttu-id="56e22-113">此函數會傳回可用來停止或識別計時器事件的計時器識別碼。</span><span class="sxs-lookup"><span data-stu-id="56e22-113">This function returns a timer identifier that can be used to stop or identify timer events.</span></span> <span data-ttu-id="56e22-114">函式的其中一個參數是發生計時器事件時所呼叫之 [**TimeProc**](/previous-versions//dd757631(v=vs.85)) 回呼函式的位址。</span><span class="sxs-lookup"><span data-stu-id="56e22-114">One of the function's parameters is the address of a [**TimeProc**](/previous-versions//dd757631(v=vs.85)) callback function that is called when the timer event takes place.</span></span>

<span data-ttu-id="56e22-115">計時器事件有兩種類型： *單一* 和 *定期*。</span><span class="sxs-lookup"><span data-stu-id="56e22-115">There are two types of timer events: *single* and *periodic*.</span></span> <span data-ttu-id="56e22-116">單一計時器事件只會在指定的毫秒數之後發生一次。</span><span class="sxs-lookup"><span data-stu-id="56e22-116">A single timer event occurs once, after a specified number of milliseconds.</span></span> <span data-ttu-id="56e22-117">每次經過指定的毫秒數時，就會發生定期計時器事件。</span><span class="sxs-lookup"><span data-stu-id="56e22-117">A periodic timer event occurs every time a specified number of milliseconds elapses.</span></span> <span data-ttu-id="56e22-118">定期事件之間的間隔稱為 *事件延遲*。</span><span class="sxs-lookup"><span data-stu-id="56e22-118">The interval between periodic events is called an *event delay*.</span></span> <span data-ttu-id="56e22-119">事件延遲為10毫秒或更低的定期計時器事件會耗用大量的 CPU 資源。</span><span class="sxs-lookup"><span data-stu-id="56e22-119">Periodic timer events with an event delay of 10 milliseconds or less consume a significant portion of CPU resources.</span></span>

<span data-ttu-id="56e22-120">計時器事件的解析度和事件延遲的長度之間的關聯性，對於計時器事件而言很重要。</span><span class="sxs-lookup"><span data-stu-id="56e22-120">The relationship between the resolution of a timer event and the length of the event delay is important in timer events.</span></span> <span data-ttu-id="56e22-121">例如，如果您指定的解決方式為5，而事件延遲為100，則計時器服務會在從95到105毫秒的間隔之後通知回呼函式。</span><span class="sxs-lookup"><span data-stu-id="56e22-121">For example, if you specify a resolution of 5 and an event delay of 100, the timer services notify the callback function after an interval ranging from 95 to 105 milliseconds.</span></span>

<span data-ttu-id="56e22-122">您可以使用 [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) 函式，隨時取消作用中的計時器事件。</span><span class="sxs-lookup"><span data-stu-id="56e22-122">You can cancel an active timer event at any time by using the [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) function.</span></span> <span data-ttu-id="56e22-123">釋放包含回呼函式的記憶體之前，請務必取消任何未處理的計時器。</span><span class="sxs-lookup"><span data-stu-id="56e22-123">Be sure to cancel any outstanding timers before freeing the memory containing the callback function.</span></span>

> [!Note]  
> <span data-ttu-id="56e22-124">多媒體計時器會在自己的執行緒中執行。</span><span class="sxs-lookup"><span data-stu-id="56e22-124">The multimedia timer runs in its own thread.</span></span>

 

 

 