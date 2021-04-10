---
description: 只要系統判斷有使用者或應用程式活動，它就不會進入睡眠狀態。
ms.assetid: 83c9394a-1813-405a-802a-0623e5de50d3
title: 系統睡眠準則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90950b980ec1e0fa06171d7a57d76b410534f96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103693019"
---
# <a name="system-sleep-criteria"></a><span data-ttu-id="ba304-103">系統睡眠準則</span><span class="sxs-lookup"><span data-stu-id="ba304-103">System Sleep Criteria</span></span>

<span data-ttu-id="ba304-104">只要系統判斷有使用者或應用程式活動，它就不會進入睡眠狀態。</span><span class="sxs-lookup"><span data-stu-id="ba304-104">As long as the system determines that there is user or application activity, it will not enter sleep.</span></span> <span data-ttu-id="ba304-105">系統可以偵測到某些活動，例如使用者輸入或網路通訊。</span><span class="sxs-lookup"><span data-stu-id="ba304-105">The system can detect certain activities, such as user input or network communications.</span></span> <span data-ttu-id="ba304-106">但是，系統無法偵測到其他活動。</span><span class="sxs-lookup"><span data-stu-id="ba304-106">However, there are other activities that the system cannot detect.</span></span> <span data-ttu-id="ba304-107">例如，簡報應用程式需要畫面才能顯示。</span><span class="sxs-lookup"><span data-stu-id="ba304-107">For example, a presentation application requires the screen for display.</span></span> <span data-ttu-id="ba304-108">不過，可能會顯示應用程式在簡報期間閒置，導致系統關閉顯示。</span><span class="sxs-lookup"><span data-stu-id="ba304-108">However, it may appear that the application is idle during the presentation, causing the system to turn off the display.</span></span>

<span data-ttu-id="ba304-109">若要通知系統您的應用程式忙碌中，請使用 [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) 函數。</span><span class="sxs-lookup"><span data-stu-id="ba304-109">To notify the system that your application is busy, use the [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) function.</span></span> <span data-ttu-id="ba304-110">此函式可防止系統進入睡眠狀態，或在應用程式執行時關閉顯示。</span><span class="sxs-lookup"><span data-stu-id="ba304-110">This function prevents the system from entering sleep or turning off the display while the application is running.</span></span>

<span data-ttu-id="ba304-111">簡報和多媒體應用程式必須以 **\_ \_ 所需的 ES 顯示** 呼叫 [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate)函式，這樣系統才能知道它不應該讓顯示器裝置進入睡眠狀態。</span><span class="sxs-lookup"><span data-stu-id="ba304-111">Presentation and multimedia applications must call the [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) function with **ES\_DISPLAY\_REQUIRED** so that the system will know that it should not put the display device to sleep.</span></span> <span data-ttu-id="ba304-112">事件處理應用程式（例如用來管理傳入傳真的工具）必須以 **需要的 \_ ES \_ 系統** 呼叫 **SetThreadExecutionState** 、處理事件，然後清除旗標，讓系統可以回到睡眠狀態。</span><span class="sxs-lookup"><span data-stu-id="ba304-112">Event-handling applications, such as tools for managing incoming faxes, must call **SetThreadExecutionState** with **ES\_SYSTEM\_REQUIRED**, handle the event, and then clear the flag so the system can return to sleep.</span></span> <span data-ttu-id="ba304-113">請注意，大部分的生產力應用程式都不需要使用 **SetThreadExecutionState** ，因為系統通常可以根據使用者輸入來決定活動。</span><span class="sxs-lookup"><span data-stu-id="ba304-113">Note that most productivity applications do not need to use **SetThreadExecutionState** because the system can usually determine activity by user input.</span></span>

<span data-ttu-id="ba304-114">為了維護最後一次使用者輸入的時間，系統會使用「顯示閒置計時器」和「系統閒置計時器」。</span><span class="sxs-lookup"><span data-stu-id="ba304-114">To maintain the time since the last user input, the system uses a display idle timer and a system idle timer.</span></span> <span data-ttu-id="ba304-115">系統會將閒置計時器與電源計劃中所設定的值進行比較。</span><span class="sxs-lookup"><span data-stu-id="ba304-115">The system compares the idle timers to the values configured in the power plan.</span></span> <span data-ttu-id="ba304-116">如果顯示閒置計時器值大於顯示超時值，而且沒有任何執行緒透過呼叫 [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) 和 **\_ \_ 所需的 ES 顯示** 來要求顯示，則系統會關閉顯示器的電源。</span><span class="sxs-lookup"><span data-stu-id="ba304-116">If the display idle timer value is greater than the display time-out value, and no threads have requested the display by calling [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) with **ES\_DISPLAY\_REQUIRED**, the system powers off the display.</span></span> <span data-ttu-id="ba304-117">同樣地，如果系統閒置計時器大於系統超時值，而且沒有任何應用程式透過呼叫 **\_ \_ 需要 ES 系統** 的 **SetThreadExecutionState** 來要求系統，系統就會進入睡眠狀態。</span><span class="sxs-lookup"><span data-stu-id="ba304-117">Similarly, if the system idle timer is greater than the system time-out value and no applications have requested the system by calling **SetThreadExecutionState** with **ES\_SYSTEM\_REQUIRED**, the system enters sleep.</span></span>

<span data-ttu-id="ba304-118">系統會維護已呼叫 [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate)的應用程式計數。</span><span class="sxs-lookup"><span data-stu-id="ba304-118">The system maintains a count of applications that have called [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate).</span></span> <span data-ttu-id="ba304-119">系統會追蹤呼叫 **SetThreadExecutionState** 的每個執行緒，並據以調整計數器。</span><span class="sxs-lookup"><span data-stu-id="ba304-119">The system tracks each thread that calls **SetThreadExecutionState** and adjusts the counter accordingly.</span></span> <span data-ttu-id="ba304-120">如果此計數器到達零，而且沒有任何使用者輸入，系統就會進入睡眠狀態。</span><span class="sxs-lookup"><span data-stu-id="ba304-120">If this counter reaches zero and there has not been any user input, the system enters sleep.</span></span>

<span data-ttu-id="ba304-121">如果電力不足，應用程式可以要求使用者介入，或要求系統暫停本身。</span><span class="sxs-lookup"><span data-stu-id="ba304-121">If power is low, an application can request user intervention or request that the system suspend itself.</span></span> <span data-ttu-id="ba304-122">您可以使用 [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) 函數來暫停系統作業。</span><span class="sxs-lookup"><span data-stu-id="ba304-122">You can suspend system operation by using the [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) function.</span></span>

<span data-ttu-id="ba304-123">如果系統自動喚醒 ([PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)) ，就不會有任何計時器相關。</span><span class="sxs-lookup"><span data-stu-id="ba304-123">If the system wakes automatically ([PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)), none of the timers are relevant.</span></span> <span data-ttu-id="ba304-124">如需詳細資訊，請參閱 [系統喚醒事件](system-wake-up-events.md)。</span><span class="sxs-lookup"><span data-stu-id="ba304-124">For more information, see [System Wake-up Events](system-wake-up-events.md).</span></span>

## <a name="entering-sleep"></a><span data-ttu-id="ba304-125">進入睡眠狀態</span><span class="sxs-lookup"><span data-stu-id="ba304-125">Entering Sleep</span></span>

<span data-ttu-id="ba304-126">當系統進入睡眠狀態時，會自動保留整個系統和所有應用程式的狀態。</span><span class="sxs-lookup"><span data-stu-id="ba304-126">When the system enters sleep, it will automatically preserve the state of the entire system and all applications.</span></span> <span data-ttu-id="ba304-127">因此，大部分的應用程式都不需要採取任何特殊動作。</span><span class="sxs-lookup"><span data-stu-id="ba304-127">Therefore, most applications do not need to take any special action.</span></span> <span data-ttu-id="ba304-128">需要在系統轉換之前執行特定動作的應用程式可以註冊電源事件。</span><span class="sxs-lookup"><span data-stu-id="ba304-128">Applications that need to perform specific actions before the system transitions can register for power events.</span></span>

<span data-ttu-id="ba304-129">當系統傳送 [PBT \_ APMSUSPEND](pbt-apmsuspend.md) 事件時，每個應用程式都有兩秒鐘的時間來執行任何必要的動作，然後系統才會開始轉換到睡眠狀態。</span><span class="sxs-lookup"><span data-stu-id="ba304-129">When the system sends a [PBT\_APMSUSPEND](pbt-apmsuspend.md) event, each application has two seconds to perform any necessary actions before the system starts the transition to sleep.</span></span> <span data-ttu-id="ba304-130">應用程式必須限制在回應此事件時所採取的動作，以確保它們會在分配的時間內完成所有作業。</span><span class="sxs-lookup"><span data-stu-id="ba304-130">Applications must limit what action they take in response to this event to ensure that they complete all operations in the time allotted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba304-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="ba304-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba304-132">關於電源管理</span><span class="sxs-lookup"><span data-stu-id="ba304-132">About Power Management</span></span>](about-power-management.md)
</dt> <dt>

[<span data-ttu-id="ba304-133">系統喚醒事件</span><span class="sxs-lookup"><span data-stu-id="ba304-133">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> </dl>

 

 



