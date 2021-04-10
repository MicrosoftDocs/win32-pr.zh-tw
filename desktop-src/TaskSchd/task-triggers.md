---
title: 工作觸發程式
description: 觸發程序就是一組條件，當符合那些條件時，就會啟動工作執行。
ms.assetid: 8b4dff8b-9dc3-4856-aed6-648588a089be
keywords:
- 建立觸發程式工作排程器
- 觸發程式工作排程器
- 觸發程式工作排程器，說明
- 以時間為基礎的觸發程式工作排程器
- 以事件為基礎的觸發程式工作排程器
- 以事件為基礎的觸發程式工作排程器
- 以時間為基礎的觸發程式工作排程器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d465dfa015be19ff220a77d3c85f0cbb223c4899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183149"
---
# <a name="task-triggers"></a><span data-ttu-id="47b9a-110">工作觸發程式</span><span class="sxs-lookup"><span data-stu-id="47b9a-110">Task Triggers</span></span>

<span data-ttu-id="47b9a-111">觸發程序就是一組條件，當符合那些條件時，就會啟動工作執行。</span><span class="sxs-lookup"><span data-stu-id="47b9a-111">A trigger is a set of criteria that, when met, starts the execution of a task.</span></span> <span data-ttu-id="47b9a-112">工作排程器提供以時間為基礎和以事件為基礎的觸發程式，可以用數種不同的方式來啟動工作。</span><span class="sxs-lookup"><span data-stu-id="47b9a-112">Task Scheduler provides both time-based and event-based triggers that can start a task in several different ways.</span></span> <span data-ttu-id="47b9a-113">一或多個觸發程式可以啟動指定的工作。</span><span class="sxs-lookup"><span data-stu-id="47b9a-113">A given task can be started by one or more triggers.</span></span> <span data-ttu-id="47b9a-114">工作最多可有48個觸發程式。</span><span class="sxs-lookup"><span data-stu-id="47b9a-114">A task can have a maximum of 48 triggers.</span></span>

## <a name="time-based-triggers"></a><span data-ttu-id="47b9a-115">以時間為基礎的觸發程式</span><span class="sxs-lookup"><span data-stu-id="47b9a-115">Time-based Triggers</span></span>

<span data-ttu-id="47b9a-116">以時間為基礎的觸發程式會在指定的時間啟動工作。</span><span class="sxs-lookup"><span data-stu-id="47b9a-116">Time-based triggers start tasks at specified times.</span></span> <span data-ttu-id="47b9a-117">這包括每日、每週、每月或每月星期幾排程，在特定時間啟動一次工作，或多次啟動工作。</span><span class="sxs-lookup"><span data-stu-id="47b9a-117">This includes starting the task once at a specific time or starting the task multiple times on a daily, weekly, monthly, or monthly day-of-week schedule.</span></span>

## <a name="event-based-triggers"></a><span data-ttu-id="47b9a-118">以事件為基礎的觸發程式</span><span class="sxs-lookup"><span data-stu-id="47b9a-118">Event-based Triggers</span></span>

<span data-ttu-id="47b9a-119">以事件為基礎的觸發程序可啟動工作來回應特定的系統事件。</span><span class="sxs-lookup"><span data-stu-id="47b9a-119">Event-based triggers start a task in response to certain system events.</span></span> <span data-ttu-id="47b9a-120">例如，您可以設定以事件為基礎的觸發程式，以便在系統啟動時、使用者登入本機電腦時，或系統變成閒置時啟動工作。</span><span class="sxs-lookup"><span data-stu-id="47b9a-120">For example, event-based triggers can be set to start a task when the system starts up, when a user logs on to the local computer, or when the system becomes idle.</span></span>

## <a name="multiple-triggers"></a><span data-ttu-id="47b9a-121">多重觸發程序</span><span class="sxs-lookup"><span data-stu-id="47b9a-121">Multiple Triggers</span></span>

<span data-ttu-id="47b9a-122">每項工作都可以透過一個或多個觸發程式來啟動，讓工作以任何數目的方式啟動。</span><span class="sxs-lookup"><span data-stu-id="47b9a-122">Each task can be started by one or more triggers, allowing the task to be started in any number of ways.</span></span> <span data-ttu-id="47b9a-123">不過，在工作排程器1.0 和工作排程器2.0 中，會以不同的方式來執行多個觸發程式。</span><span class="sxs-lookup"><span data-stu-id="47b9a-123">However, multiple triggers are implemented differently in Task Scheduler 1.0 and Task Scheduler 2.0.</span></span>

<span data-ttu-id="47b9a-124">在工作排程器2.0 中，每個觸發程式都是由透過觸發程式集合與工作相關聯的個別觸發程式 API 所定義。</span><span class="sxs-lookup"><span data-stu-id="47b9a-124">In Task Scheduler 2.0, each trigger is defined by a separate trigger API that is associated with the task through the trigger collection.</span></span>

<span data-ttu-id="47b9a-125">在工作排程器1.0 中，可以將多個觸發程式視為排程，也就是工作開始的一組時間。</span><span class="sxs-lookup"><span data-stu-id="47b9a-125">In Task Scheduler 1.0, multiple triggers can be thought of as a schedule, a set of times at which the task starts.</span></span> <span data-ttu-id="47b9a-126">在此情況下，排程是一組時間 (由與工作專案所執行之工作專案) 相關聯之所有觸發程式的聯集來指定。</span><span class="sxs-lookup"><span data-stu-id="47b9a-126">In this case, the schedule is the set of times (specified by the union of all of the triggers associated with the work item) at which a work item will execute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47b9a-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="47b9a-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47b9a-128">重複工作</span><span class="sxs-lookup"><span data-stu-id="47b9a-128">Repeating A Task</span></span>](repeating-a-task.md)
</dt> <dt>

[<span data-ttu-id="47b9a-129">觸發程式類型</span><span class="sxs-lookup"><span data-stu-id="47b9a-129">Trigger Types</span></span>](trigger-types.md)
</dt> <dt>

[<span data-ttu-id="47b9a-130">觸發程式介面</span><span class="sxs-lookup"><span data-stu-id="47b9a-130">Trigger Interfaces</span></span>](trigger-interfaces.md)
</dt> <dt>

[<span data-ttu-id="47b9a-131">關於工作排程器</span><span class="sxs-lookup"><span data-stu-id="47b9a-131">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 




