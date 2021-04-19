---
title: 工作排程器1.0 的閒置觸發程式
description: 閒置觸發程式是以事件為基礎的觸發程式，會在電腦閒置之後引發特定次數。 有多個條件會定義電腦何時閒置，例如當沒有鍵盤或滑鼠輸入時。
ms.assetid: f2e0b120-dadc-470f-8349-42843149bb60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d6a19f3f6d474a9463667316e353a4803ab8fa9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968217"
---
# <a name="idle-triggers-for-task-scheduler-10"></a><span data-ttu-id="c1817-104">工作排程器1.0 的閒置觸發程式</span><span class="sxs-lookup"><span data-stu-id="c1817-104">Idle Triggers for Task Scheduler 1.0</span></span>

<span data-ttu-id="c1817-105">閒置觸發程式是以事件為基礎的觸發程式，會在電腦閒置之後引發特定次數。</span><span class="sxs-lookup"><span data-stu-id="c1817-105">An idle trigger is an event-based trigger that is fired a specific number of times after the computer becomes idle.</span></span> <span data-ttu-id="c1817-106">有多個條件會定義電腦何時閒置，例如當沒有鍵盤或滑鼠輸入時。</span><span class="sxs-lookup"><span data-stu-id="c1817-106">There are multiple conditions that define when a computer becomes idle, such as when no keyboard or mouse input occurs.</span></span>

<span data-ttu-id="c1817-107">閒置觸發程式的建立方式，是在工作觸發程式 \_ \_ 結構的 \_ \_ 工作觸發程式 [**\_ \_ 類型**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) 成員 [**\_**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) 中指定閒置的工作事件觸發程式。</span><span class="sxs-lookup"><span data-stu-id="c1817-107">Idle triggers are created by specifying TASK\_EVENT\_TRIGGER\_ON\_IDLE in the [**TASK\_TRIGGER\_TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) member of the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure.</span></span> <span data-ttu-id="c1817-108">當系統閒置了工作專案的閒置等候時間所指定的時間量時，就會引發閒置觸發程式。</span><span class="sxs-lookup"><span data-stu-id="c1817-108">The idle trigger is fired when the system becomes idle for the amount of time that is specified by the idle wait time of the work item.</span></span>

> [!Note]  
> <span data-ttu-id="c1817-109">當 \_ \_ \_ 指定閒置的工作事件觸發程式時 \_ ，會忽略工作 [**\_ 觸發**](/windows/desktop/api/Mstask/ns-mstask-task_trigger)程式結構的 **wStartHour**、 **wStartMinute** 和 **類型** 成員。</span><span class="sxs-lookup"><span data-stu-id="c1817-109">When TASK\_EVENT\_TRIGGER\_ON\_IDLE is specified, the **wStartHour**, **wStartMinute**, and **Type** members of the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure are ignored.</span></span>

 

<span data-ttu-id="c1817-110">您可以藉由呼叫 [**IScheduledWorkItem：： SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) 方法來設定工作專案的空閒等候時間。</span><span class="sxs-lookup"><span data-stu-id="c1817-110">You can set the idle wait time of a work item by calling the [**IScheduledWorkItem::SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) method.</span></span> <span data-ttu-id="c1817-111">這個方法會以分鐘為單位來設定時間 (，) 系統必須保持閒置，才能引發觸發程式和執行工作專案。</span><span class="sxs-lookup"><span data-stu-id="c1817-111">This method sets the amount of time (in minutes) that the system must remain idle before the trigger is fired and the work item is executed.</span></span>

<span data-ttu-id="c1817-112">若要取出工作的閒置時間，請呼叫 [**IScheduledWorkItem：： GetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getidlewait) 方法。</span><span class="sxs-lookup"><span data-stu-id="c1817-112">To retrieve the idle time of a task, call the [**IScheduledWorkItem::GetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getidlewait) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1817-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="c1817-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1817-114">工作觸發程式</span><span class="sxs-lookup"><span data-stu-id="c1817-114">Task Triggers</span></span>](task-triggers.md)
</dt> </dl>

 

 




