---
title: 'T (工作排程器) '
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d4c6d7ba-7bca-420d-a4dc-4daea816f99c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2730cdbe3a13456aed0e613a614d43a0e56e6673
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104508244"
---
# <a name="t-task-scheduler"></a><span data-ttu-id="2d287-103">T (工作排程器) </span><span class="sxs-lookup"><span data-stu-id="2d287-103">T (Task Scheduler)</span></span>

<span data-ttu-id="2d287-104">B C D [E](e.md) F G H [I](i.md) J K L M N O [P](p.md) Q R [S](s.md) T [W](w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="2d287-104">A B C D [E](e.md) F G H [I](i.md) J K L M N O [P](p.md) Q R [S](s.md) T U V [W](w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="2d287-105"><span id="_msb_task_objects_gly"></span><span id="_MSB_TASK_OBJECTS_GLY"></span>**工作物件**</span><span class="sxs-lookup"><span data-stu-id="2d287-105"><span id="_msb_task_objects_gly"></span><span id="_MSB_TASK_OBJECTS_GLY"></span>**task objects**</span></span>
</dt> <dd>

<span data-ttu-id="2d287-106">物件的實例，提供管理工作的方法。</span><span class="sxs-lookup"><span data-stu-id="2d287-106">Instances of an object that provides methods for managing tasks.</span></span> <span data-ttu-id="2d287-107">這包括設定和抓取屬性的方法;執行、終止和刪除工作;以及建立新的觸發程式並抓取舊的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="2d287-107">This includes methods for setting and retrieving properties; running, terminating, and deleting tasks; and creating new triggers and retrieving old triggers.</span></span>

<span data-ttu-id="2d287-108">工作物件是由呼叫 [**IScheduledWorkItem：： CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) 和 [**IScheduledWorkItem：： GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger)所建立。</span><span class="sxs-lookup"><span data-stu-id="2d287-108">The task object is created by calls to [**IScheduledWorkItem::CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) and [**IScheduledWorkItem::GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).</span></span>

</dd> <dt>

<span data-ttu-id="2d287-109"><span id="_msb_task_scheduler_objects_gly"></span><span id="_MSB_TASK_SCHEDULER_OBJECTS_GLY"></span>**工作排程器物件**</span><span class="sxs-lookup"><span data-stu-id="2d287-109"><span id="_msb_task_scheduler_objects_gly"></span><span id="_MSB_TASK_SCHEDULER_OBJECTS_GLY"></span>**task scheduler objects**</span></span>
</dt> <dd>

<span data-ttu-id="2d287-110">物件的實例，代表工作排程器服務。</span><span class="sxs-lookup"><span data-stu-id="2d287-110">Instances of an object the represents the Task Scheduler service.</span></span> <span data-ttu-id="2d287-111">此物件支援兩個介面： **IUnknown** 和 [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) (目前的工作是工作排程器服務) 所支援的唯一工作專案類型。</span><span class="sxs-lookup"><span data-stu-id="2d287-111">This object supports two interfaces: **IUnknown** and [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) (currently tasks are the only type of work items supported by the Task Scheduler service).</span></span>

<span data-ttu-id="2d287-112">工作排程器物件是由對 **CoCreateInstance** 的呼叫所建立。</span><span class="sxs-lookup"><span data-stu-id="2d287-112">Task scheduler objects are created by calls to **CoCreateInstance**.</span></span>

</dd> <dt>

<span data-ttu-id="2d287-113"><span id="_msb_task_trigger_objects_gly"></span><span id="_MSB_TASK_TRIGGER_OBJECTS_GLY"></span>**工作觸發程式物件**</span><span class="sxs-lookup"><span data-stu-id="2d287-113"><span id="_msb_task_trigger_objects_gly"></span><span id="_MSB_TASK_TRIGGER_OBJECTS_GLY"></span>**task trigger objects**</span></span>
</dt> <dd>

<span data-ttu-id="2d287-114">物件的實例，提供用來設定和抓取工作觸發程式的方法。</span><span class="sxs-lookup"><span data-stu-id="2d287-114">Instances of an object the provides methods for setting and retrieving task triggers.</span></span> <span data-ttu-id="2d287-115">此物件支援兩個介面： **IUnknown** 和 [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger)。</span><span class="sxs-lookup"><span data-stu-id="2d287-115">This object supports two interfaces: **IUnknown** and [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger).</span></span>

<span data-ttu-id="2d287-116">工作觸發程式物件是由呼叫 [**IScheduledWorkItem：： CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) 和 [**IScheduledWorkItem：： GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger)所建立。</span><span class="sxs-lookup"><span data-stu-id="2d287-116">Task trigger objects are created by calls to [**IScheduledWorkItem::CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) and [**IScheduledWorkItem::GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).</span></span>

<span data-ttu-id="2d287-117">另請參閱： *觸發* 程式。</span><span class="sxs-lookup"><span data-stu-id="2d287-117">See also: *triggers*.</span></span>

</dd> <dt>

<span data-ttu-id="2d287-118"><span id="_msb_tasks_gly"></span><span id="_MSB_TASKS_GLY"></span>**任務**</span><span class="sxs-lookup"><span data-stu-id="2d287-118"><span id="_msb_tasks_gly"></span><span id="_MSB_TASKS_GLY"></span>**tasks**</span></span>
</dt> <dd>

<span data-ttu-id="2d287-119">工作排程器可以執行的任何專案。</span><span class="sxs-lookup"><span data-stu-id="2d287-119">Any item that the Task Scheduler can execute.</span></span> <span data-ttu-id="2d287-120">這些專案可能包含工作將執行的作業系統所支援的下列任何 () ： Win32®應用程式、Win16 應用程式、OS/2 應用程式、MS-DOS®應用程式、批次檔 (\* .bat) 、命令檔 (\* .cmd) ，或任何正確註冊的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="2d287-120">These items may include any of the following (as supported by the operating system on which the task will execute): Win32® applications, Win16 applications, OS/2 applications, MS-DOS® applications, batch files (\*.bat), command files (\*.cmd), or any properly registered file type.</span></span>

</dd> <dt>

<span data-ttu-id="2d287-121"><span id="_msb_tasks_folder_gly"></span><span id="_MSB_TASKS_FOLDER_GLY"></span>**Tasks 資料夾**</span><span class="sxs-lookup"><span data-stu-id="2d287-121"><span id="_msb_tasks_folder_gly"></span><span id="_MSB_TASKS_FOLDER_GLY"></span>**Tasks folder**</span></span>
</dt> <dd>

<span data-ttu-id="2d287-122">列出所有工作檔案 (目前的資料夾，工作是唯一可用的工作專案) 。</span><span class="sxs-lookup"><span data-stu-id="2d287-122">The folder that lists all task files (currently, tasks are the only work items available).</span></span> <span data-ttu-id="2d287-123">這些檔案包含工作的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2d287-123">These files contain the information about the task.</span></span> <span data-ttu-id="2d287-124">這些檔案的名稱會反映工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d287-124">The name of these files reflects the name of the task.</span></span>

<span data-ttu-id="2d287-125">您可以藉由取得下列值的資料，從登錄取出 Tasks 資料夾的位置：</span><span class="sxs-lookup"><span data-stu-id="2d287-125">You can retrieve the location of the Tasks folder from the registry by getting data for the following value:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         SchedulingAgent
            TasksFolder
```

</dd> <dt>

<span data-ttu-id="2d287-126"><span id="_msb_triggers_gly"></span><span id="_MSB_TRIGGERS_GLY"></span>**觸發器**</span><span class="sxs-lookup"><span data-stu-id="2d287-126"><span id="_msb_triggers_gly"></span><span id="_MSB_TRIGGERS_GLY"></span>**triggers**</span></span>
</dt> <dd>

<span data-ttu-id="2d287-127">當符合時，會造成工作執行的一組準則。</span><span class="sxs-lookup"><span data-stu-id="2d287-127">A set of criteria that, when met, will cause a task to be executed.</span></span> <span data-ttu-id="2d287-128">工作排程器提供以時間為基礎和以事件為基礎的觸發程式，可指定工作開始時間、重複條件及其他參數。</span><span class="sxs-lookup"><span data-stu-id="2d287-128">Task Scheduler provides time-based and event-based triggers that can specify task start times, repetition criteria, and other parameters.</span></span>

</dd> <dt>

<span data-ttu-id="2d287-129"><span id="_msb_trigger_strings_gly"></span><span id="_MSB_TRIGGER_STRINGS_GLY"></span>**觸發字串**</span><span class="sxs-lookup"><span data-stu-id="2d287-129"><span id="_msb_trigger_strings_gly"></span><span id="_MSB_TRIGGER_STRINGS_GLY"></span>**trigger strings**</span></span>
</dt> <dd>

<span data-ttu-id="2d287-130">描述觸發程式的字串。</span><span class="sxs-lookup"><span data-stu-id="2d287-130">A string that describes the trigger.</span></span> <span data-ttu-id="2d287-131">這個字串是由工作排程器服務所建立，並出現在工作排程器的使用者介面中，其格式類似于「每日下午2：5/11/97」。</span><span class="sxs-lookup"><span data-stu-id="2d287-131">This string is created by the Task Scheduler service, and appears in the Task Scheduler user interface in a form similar to "At 2PM every day, starting 5/11/97."</span></span>

</dd> <dt>

<span data-ttu-id="2d287-132"><span id="_msb_trigger_structures_gly"></span><span id="_MSB_TRIGGER_STRUCTURES_GLY"></span>**觸發程式結構**</span><span class="sxs-lookup"><span data-stu-id="2d287-132"><span id="_msb_trigger_structures_gly"></span><span id="_MSB_TRIGGER_STRUCTURES_GLY"></span>**trigger structures**</span></span>
</dt> <dd>

<span data-ttu-id="2d287-133">在設定或抓取定義觸發程式的準則時，所使用的工作 [**\_ 觸發**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) 程式結構。</span><span class="sxs-lookup"><span data-stu-id="2d287-133">The [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure used when setting or retrieving the criteria that defines the trigger.</span></span> <span data-ttu-id="2d287-134">準則包括觸發程式的觸發時間，以及觸發程式的類型。</span><span class="sxs-lookup"><span data-stu-id="2d287-134">The criteria includes when the trigger will fire, and the type of the trigger.</span></span>

</dd> </dl>

 

 




