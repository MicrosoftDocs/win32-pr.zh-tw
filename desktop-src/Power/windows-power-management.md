---
description: Windows 電源管理可讓使用者隨時接觸按鈕或按鍵，以立即存取電腦。
ms.assetid: 388dadb9-b722-43f8-ab2b-a9bbd96600a3
title: Windows 電源管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8abb3a040f8da8e2deb242a2aa607a9448d31c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849264"
---
# <a name="windows-power-management"></a><span data-ttu-id="d2739-103">Windows 電源管理</span><span class="sxs-lookup"><span data-stu-id="d2739-103">Windows Power Management</span></span>

<span data-ttu-id="d2739-104">Windows 電源管理可讓使用者隨時接觸按鈕或按鍵，以立即存取電腦。</span><span class="sxs-lookup"><span data-stu-id="d2739-104">Windows power management makes computers instantly accessible to users at the touch of a button or key.</span></span> <span data-ttu-id="d2739-105">它也可確保系統的所有元素（應用程式、裝置和使用者介面）都能充分利用電源管理技術與功能的強大改良功能。</span><span class="sxs-lookup"><span data-stu-id="d2739-105">It also ensures that all elements of the system—applications, devices, and user interface—can take advantage of the vast improvements in power management technology and capabilities.</span></span>

<span data-ttu-id="d2739-106">Windows 作業系統使用電源管理硬體使電腦進入低電源 *睡眠狀態* ，而不是完全關閉，讓系統可以快速繼續運作。</span><span class="sxs-lookup"><span data-stu-id="d2739-106">The Windows operating system uses power-management hardware to put the computer into a low-power *sleep state* instead of shutting down completely, so that the system can quickly resume working.</span></span> <span data-ttu-id="d2739-107">當電腦處於閒置狀態時，或當使用者按下按鈕來指出目前的工作會話已結束時，作業系統會自動進入睡眠狀態。</span><span class="sxs-lookup"><span data-stu-id="d2739-107">The operating system will automatically enter the sleep state when the computer is idle or when the user presses a button to indicate that the current work session is over.</span></span> <span data-ttu-id="d2739-108">對使用者而言，系統似乎已關閉。</span><span class="sxs-lookup"><span data-stu-id="d2739-108">To the user, the system appears to be off.</span></span> <span data-ttu-id="d2739-109">處於睡眠狀態時，電腦的處理器不會執行程式碼，也不會為使用者完成任何工作。</span><span class="sxs-lookup"><span data-stu-id="d2739-109">While in the sleep state, the computer's processor is not executing code and no work is being accomplished for the user.</span></span> <span data-ttu-id="d2739-110">不過，您可以啟用系統中來自兩個硬體裝置和系統時鐘的事件，讓系統結束睡眠狀態 (也就是「喚醒」 ) 並快速返回工作狀態。</span><span class="sxs-lookup"><span data-stu-id="d2739-110">However, events in the system from both hardware devices and the real-time clock can be enabled to cause the system to exit the sleep state (that is, "wake up") and quickly return to the working state.</span></span>

<span data-ttu-id="d2739-111">當電腦處於睡眠狀態時，電腦硬體、系統和電腦上執行的應用程式必須能夠立即回應電源交換器、通訊事件和其他動作。</span><span class="sxs-lookup"><span data-stu-id="d2739-111">When the computer is in the sleep state, the computer hardware, the system, and applications running on the computer must be capable of responding immediately to the power switch, communications events, and other actions.</span></span> <span data-ttu-id="d2739-112">如果所有應用程式都能正常地處理電源狀態轉換，則使用者會察覺到更精緻且整合的系統。</span><span class="sxs-lookup"><span data-stu-id="d2739-112">If all applications handle power state transitions gracefully, the user will perceive a more elegant and integrated system.</span></span> <span data-ttu-id="d2739-113">未處理這些轉換的應用程式可能會在電源關閉時失敗，然後因為資料遺失或可能已移除之裝置的相依性而失敗。</span><span class="sxs-lookup"><span data-stu-id="d2739-113">Applications that do not handle these transitions can fail when the power is turned off and then on, because of data loss or a dependency on a device that may have been removed.</span></span>

<span data-ttu-id="d2739-114">以下是 Windows 電源管理的優點：</span><span class="sxs-lookup"><span data-stu-id="d2739-114">The following are benefits of Windows power management:</span></span>

-   <span data-ttu-id="d2739-115">消除啟動和關機延遲。</span><span class="sxs-lookup"><span data-stu-id="d2739-115">Eliminates startup and shutdown delays.</span></span> <span data-ttu-id="d2739-116">當使用者啟動睡眠狀態時，電腦不需要執行完整系統開機，或在使用者起始睡眠狀態時，完全關機。</span><span class="sxs-lookup"><span data-stu-id="d2739-116">The computer need not perform a full system boot when exiting the sleep state or a full system shutdown when the user initiates the sleep state.</span></span>
-   <span data-ttu-id="d2739-117">讓自動化工作在電腦處於睡眠狀態時執行。</span><span class="sxs-lookup"><span data-stu-id="d2739-117">Enables automated tasks to run while the computer is in the sleep state.</span></span> <span data-ttu-id="d2739-118">工作排程器可讓使用者排定要執行的應用程式;即使系統處於睡眠狀態，也可以執行已排程的事件。</span><span class="sxs-lookup"><span data-stu-id="d2739-118">The Task Scheduler enables the user to schedule applications to run; scheduled events can run even when the system is in the sleep state.</span></span> <span data-ttu-id="d2739-119">工作排程器會使用 [可等候計時器](/windows/desktop/Sync/waitable-timer-objects) ，以確保當應用程式已排程執行時，系統已準備就緒。</span><span class="sxs-lookup"><span data-stu-id="d2739-119">The Task Scheduler uses [waitable timers](/windows/desktop/Sync/waitable-timer-objects) to ensure that the system is ready when the application is scheduled to run.</span></span> <span data-ttu-id="d2739-120">如需詳細資訊，請參閱工作排程器隨附的說明檔。</span><span class="sxs-lookup"><span data-stu-id="d2739-120">For more information, see the help file included with the Task Scheduler.</span></span>
-   <span data-ttu-id="d2739-121">啟用每個裝置的電源管理。</span><span class="sxs-lookup"><span data-stu-id="d2739-121">Enables per-device power management.</span></span> <span data-ttu-id="d2739-122">未使用的裝置可進入睡眠狀態以節省電源。</span><span class="sxs-lookup"><span data-stu-id="d2739-122">Devices that are not in use can save power by entering the sleep state.</span></span>
-   <span data-ttu-id="d2739-123">改善電源效率。</span><span class="sxs-lookup"><span data-stu-id="d2739-123">Improves power efficiency.</span></span> <span data-ttu-id="d2739-124">在可攜式電腦上的電源效率特別重要。</span><span class="sxs-lookup"><span data-stu-id="d2739-124">Power efficiency is particularly important on portable computers.</span></span> <span data-ttu-id="d2739-125">減少系統電源耗用量可直接轉譯為較低的能源成本和較長的電池壽命。</span><span class="sxs-lookup"><span data-stu-id="d2739-125">Reducing system power consumption translates directly to lower energy costs and longer battery life.</span></span>
-   <span data-ttu-id="d2739-126">可讓使用者透過主控台中的電源選項應用程式，建立 [電源配置](power-schemes.md)、設定警示，以及指定電池選項。</span><span class="sxs-lookup"><span data-stu-id="d2739-126">Enables users to create [power schemes](power-schemes.md), set alarms, and specify battery options through the Power Options application in Control Panel.</span></span> <span data-ttu-id="d2739-127">作業系統會根據電源原則設定來協調所有電源管理活動。</span><span class="sxs-lookup"><span data-stu-id="d2739-127">The operating system coordinates all power management activities, based on power policy settings.</span></span> <span data-ttu-id="d2739-128">如需詳細資訊，請參閱電源選項應用程式隨附的說明檔。</span><span class="sxs-lookup"><span data-stu-id="d2739-128">For more information, see the help file included with the Power Options application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2739-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="d2739-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2739-130">關於電源管理</span><span class="sxs-lookup"><span data-stu-id="d2739-130">About Power Management</span></span>](about-power-management.md)
</dt> <dt>

[<span data-ttu-id="d2739-131">工作排程器</span><span class="sxs-lookup"><span data-stu-id="d2739-131">Task Scheduler</span></span>](/windows/desktop/TaskSchd/task-scheduler-start-page)
</dt> </dl>

 

 
