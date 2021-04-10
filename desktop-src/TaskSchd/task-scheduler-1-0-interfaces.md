---
title: 工作排程器1.0 介面
description: 下列主題中所述的介面，可讓您以程式設計方式存取 Windows 2000、Windows XP 及 Windows Server 2003 作業系統中使用的工作排程器功能。
ms.assetid: 25f9c1ad-1859-4788-a876-6f4faa6e556e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bab12b59d4b4561ecbe46c09a76c69209574c9d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104186651"
---
# <a name="task-scheduler-10-interfaces"></a><span data-ttu-id="79bb6-103">工作排程器1.0 介面</span><span class="sxs-lookup"><span data-stu-id="79bb6-103">Task Scheduler 1.0 Interfaces</span></span>

<span data-ttu-id="79bb6-104">\[\[此 API 可能會在後續版本的作業系統或產品中變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="79bb6-104">\[\[This API may be altered or unavailable in subsequent versions of the operating system or product.</span></span> <span data-ttu-id="79bb6-105">請改用[工作排程器2.0 介面](task-scheduler-2-0-interfaces.md)或[工作排程器2.0 列舉類型](task-scheduler-2-0-enumerated-types.md)。 \]\]</span><span class="sxs-lookup"><span data-stu-id="79bb6-105">Please use the [Task Scheduler 2.0 Interfaces](task-scheduler-2-0-interfaces.md) or [Task Scheduler 2.0 Enumerated Types](task-scheduler-2-0-enumerated-types.md) instead.\] \]</span></span>

<span data-ttu-id="79bb6-106">下列主題中所述的介面，可讓您以程式設計方式存取 Windows 2000、Windows XP 及 Windows Server 2003 作業系統中使用的工作排程器功能。</span><span class="sxs-lookup"><span data-stu-id="79bb6-106">The interfaces that are described in the following topics provide programmatic access to the functionality that is available within the Task Scheduler that is used in the Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="79bb6-107">這些主題包含介面的描述、介面所定義之屬性和方法的清單，以及使用介面時應注意的任何特殊情況的備註。</span><span class="sxs-lookup"><span data-stu-id="79bb6-107">These topics contain a description of the interface, a list of the properties and methods defined by the interface, and remarks about any special circumstances that should be noted when using the interface.</span></span>


<span data-ttu-id="79bb6-108">下列是工作排程器1.0 引進的介面。</span><span class="sxs-lookup"><span data-stu-id="79bb6-108">The following interfaces are introduced by Task Scheduler 1.0.</span></span>



| <span data-ttu-id="79bb6-109">介面</span><span class="sxs-lookup"><span data-stu-id="79bb6-109">Interface</span></span>                                        | <span data-ttu-id="79bb6-110">描述</span><span class="sxs-lookup"><span data-stu-id="79bb6-110">Description</span></span>                                                                                                                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79bb6-111">**IEnumWorkItems**</span><span class="sxs-lookup"><span data-stu-id="79bb6-111">**IEnumWorkItems**</span></span>](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems)         | <span data-ttu-id="79bb6-112">提供列舉 [排定的工作] [*資料夾*](s.md)中之工作的方法。</span><span class="sxs-lookup"><span data-stu-id="79bb6-112">Provides the methods for enumerating the tasks in the [*Scheduled Tasks folder*](s.md).</span></span>                                                                                                              |
| [<span data-ttu-id="79bb6-113">**IProvideTaskPage**</span><span class="sxs-lookup"><span data-stu-id="79bb6-113">**IProvideTaskPage**</span></span>](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage)     | <span data-ttu-id="79bb6-114">提供方法來存取工作的屬性工作表設定。</span><span class="sxs-lookup"><span data-stu-id="79bb6-114">Provides the methods to access the property sheet settings of a task.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="79bb6-115">**IScheduledWorkItem**</span><span class="sxs-lookup"><span data-stu-id="79bb6-115">**IScheduledWorkItem**</span></span>](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) | <span data-ttu-id="79bb6-116">提供管理特定 [*工作專案*](w.md)的方法。</span><span class="sxs-lookup"><span data-stu-id="79bb6-116">Provides the methods for managing specific [*work items*](w.md).</span></span>                                                                                                                                                 |
| [<span data-ttu-id="79bb6-117">**ITask**</span><span class="sxs-lookup"><span data-stu-id="79bb6-117">**ITask**</span></span>](/windows/desktop/api/Mstask/nn-mstask-itask)                           | <span data-ttu-id="79bb6-118">提供執行工作、取得或設定工作資訊，以及終止工作的方法。</span><span class="sxs-lookup"><span data-stu-id="79bb6-118">Provides the methods for running tasks, getting or setting task information, and terminating tasks.</span></span> <span data-ttu-id="79bb6-119">它衍生自 [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) 介面，並繼承該介面的所有方法。</span><span class="sxs-lookup"><span data-stu-id="79bb6-119">It is derived from the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface and inherits all the methods of that interface.</span></span> |
| [<span data-ttu-id="79bb6-120">**ITaskScheduler**</span><span class="sxs-lookup"><span data-stu-id="79bb6-120">**ITaskScheduler**</span></span>](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler)         | <span data-ttu-id="79bb6-121">提供排程工作的方法。</span><span class="sxs-lookup"><span data-stu-id="79bb6-121">Provides the methods for scheduling tasks.</span></span>                                                                                                                                                                                            |
| [<span data-ttu-id="79bb6-122">**ITaskTrigger**</span><span class="sxs-lookup"><span data-stu-id="79bb6-122">**ITaskTrigger**</span></span>](/windows/desktop/api/Mstask/nn-mstask-itasktrigger)             | <span data-ttu-id="79bb6-123">提供用來存取和設定工作觸發程式的方法。</span><span class="sxs-lookup"><span data-stu-id="79bb6-123">Provides the methods for accessing and setting triggers for a task.</span></span> <span data-ttu-id="79bb6-124">觸發程式會指定工作開始時間、重複準則，以及控制工作執行時間的其他參數。</span><span class="sxs-lookup"><span data-stu-id="79bb6-124">Triggers specify task start times, repetition criteria, and other parameters that control when a task is run.</span></span>                                                     |



 

 

 




