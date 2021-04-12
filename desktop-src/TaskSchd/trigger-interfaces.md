---
title: 觸發程式介面
description: 用來管理觸發程式的 Api 會根據工作排程器的版本而有所不同。 不過，在這兩種情況下，這些 Api 可讓您建立新的觸發程式、取出和更新現有的觸發程式，以及刪除不再需要的觸發程式。
ms.assetid: 94c11f11-72e2-404f-b396-ab7b1be71942
keywords:
- 觸發程式工作排程器、介面
- 觸發程式工作排程器、介面、描述
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5357bb745b43c51707d9571c7582a44c9225a7fe
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316816"
---
# <a name="trigger-interfaces"></a><span data-ttu-id="ba75b-106">觸發程式介面</span><span class="sxs-lookup"><span data-stu-id="ba75b-106">Trigger Interfaces</span></span>

<span data-ttu-id="ba75b-107">用來管理觸發程式的 Api 會根據工作排程器的版本而有所不同。</span><span class="sxs-lookup"><span data-stu-id="ba75b-107">The APIs that are used to manage triggers vary depending on the version of the Task Scheduler.</span></span> <span data-ttu-id="ba75b-108">不過，在這兩種情況下，這些 Api 可讓您建立新的觸發程式、取出和更新現有的觸發程式，以及刪除不再需要的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="ba75b-108">However, in both cases these APIs enable you to create new triggers, retrieve and update existing triggers, and delete triggers that are no longer required.</span></span>


<span data-ttu-id="ba75b-109">使用工作排程器2.0 開發的應用程式可以使用物件和介面，來建立、取出、修改和刪除工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="ba75b-109">Applications that are developed using Task Scheduler 2.0 can use objects and interfaces to create, retrieve, modify, and delete the triggers for a task.</span></span>

<span data-ttu-id="ba75b-110">在下圖中，工作會使用觸發程式屬性來指定觸發程式的集合。</span><span class="sxs-lookup"><span data-stu-id="ba75b-110">In the following illustration, a task specifies a collection of triggers using its Triggers property.</span></span> <span data-ttu-id="ba75b-111">此集合包含一個或多個個別的觸發程式 Api，其中每個 API 指定了特定的觸發程式類型。</span><span class="sxs-lookup"><span data-stu-id="ba75b-111">This collection contains one or more individual trigger APIs with each API specifying a specific trigger type.</span></span> <span data-ttu-id="ba75b-112">例如，在下圖中，觸發程式集合包含開機觸發程式、登入觸發程式和每日觸發程式。</span><span class="sxs-lookup"><span data-stu-id="ba75b-112">For example, in the illustration below the trigger collection contains a boot trigger, logon trigger, and a daily trigger.</span></span>

![工作排程器2.0 觸發程式介面](images/tsktri4.png)

### <a name="object-apis-for-scripting-development"></a><span data-ttu-id="ba75b-114">腳本開發的物件 Api</span><span class="sxs-lookup"><span data-stu-id="ba75b-114">Object APIs for Scripting Development</span></span>

<span data-ttu-id="ba75b-115">如需有關用來指定觸發程式之物件的方法和屬性的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="ba75b-115">For more information about the methods and properties of the objects that are used to specify triggers, see:</span></span>

-   [<span data-ttu-id="ba75b-116">**TaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="ba75b-116">**TaskDefinition**</span></span>](taskdefinition.md)
-   [<span data-ttu-id="ba75b-117">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="ba75b-117">**TriggerCollection**</span></span>](triggercollection.md)
-   [<span data-ttu-id="ba75b-118">**觸發**</span><span class="sxs-lookup"><span data-stu-id="ba75b-118">**Trigger**</span></span>](trigger.md)
-   [<span data-ttu-id="ba75b-119">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="ba75b-119">**BootTrigger**</span></span>](boottrigger.md)
-   [<span data-ttu-id="ba75b-120">**DailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="ba75b-120">**DailyTrigger**</span></span>](dailytrigger.md)
-   [<span data-ttu-id="ba75b-121">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="ba75b-121">**EventTrigger**</span></span>](eventtrigger.md)
-   [<span data-ttu-id="ba75b-122">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="ba75b-122">**IdleTrigger**</span></span>](idletrigger.md)
-   [<span data-ttu-id="ba75b-123">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="ba75b-123">**LogonTrigger**</span></span>](logontrigger.md)
-   [<span data-ttu-id="ba75b-124">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="ba75b-124">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
-   [<span data-ttu-id="ba75b-125">**MonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="ba75b-125">**MonthlyTrigger**</span></span>](monthlytrigger.md)
-   [<span data-ttu-id="ba75b-126">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="ba75b-126">**RegistrationTrigger**</span></span>](registrationtrigger.md)
-   [<span data-ttu-id="ba75b-127">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="ba75b-127">**TimeTrigger**</span></span>](timetrigger.md)
-   [<span data-ttu-id="ba75b-128">**WeeklyTrigger**</span><span class="sxs-lookup"><span data-stu-id="ba75b-128">**WeeklyTrigger**</span></span>](weeklytrigger.md)

### <a name="interfaces-apis-for-c-development"></a><span data-ttu-id="ba75b-129">適用于 c + + 開發的介面 Api</span><span class="sxs-lookup"><span data-stu-id="ba75b-129">Interfaces APIs for C++ Development</span></span>

<span data-ttu-id="ba75b-130">如需有關用來指定觸發程式之介面的方法和屬性的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="ba75b-130">For more information about the methods and properties of the interfaces that are used to specify triggers, see:</span></span>

-   [<span data-ttu-id="ba75b-131">**ITaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="ba75b-131">**ITaskDefinition**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
-   [<span data-ttu-id="ba75b-132">**ITriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="ba75b-132">**ITriggerCollection**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection)
-   [<span data-ttu-id="ba75b-133">**ITrigger**</span><span class="sxs-lookup"><span data-stu-id="ba75b-133">**ITrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itrigger)
-   [<span data-ttu-id="ba75b-134">**IBootTrigger**</span><span class="sxs-lookup"><span data-stu-id="ba75b-134">**IBootTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger)
-   [<span data-ttu-id="ba75b-135">**IDailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="ba75b-135">**IDailyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [<span data-ttu-id="ba75b-136">**IEventTrigger**</span><span class="sxs-lookup"><span data-stu-id="ba75b-136">**IEventTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger)
-   [<span data-ttu-id="ba75b-137">**IIdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="ba75b-137">**IIdleTrigger**</span></span>](/windows/win32/api/taskschd/nn-taskschd-iidletrigger)
-   [<span data-ttu-id="ba75b-138">**ILogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="ba75b-138">**ILogonTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger)
-   [<span data-ttu-id="ba75b-139">**IMonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="ba75b-139">**IMonthlyDOWTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)
-   [<span data-ttu-id="ba75b-140">**IMonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="ba75b-140">**IMonthlyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [<span data-ttu-id="ba75b-141">**IRegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="ba75b-141">**IRegistrationTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger)
-   [<span data-ttu-id="ba75b-142">**ITimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="ba75b-142">**ITimeTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger)
-   [<span data-ttu-id="ba75b-143">**IWeeklyTrigger**</span><span class="sxs-lookup"><span data-stu-id="ba75b-143">**IWeeklyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)

## <a name="task-scheduler-10-trigger-interfaces"></a><span data-ttu-id="ba75b-144">工作排程器1.0 觸發程式介面</span><span class="sxs-lookup"><span data-stu-id="ba75b-144">Task Scheduler 1.0 Trigger Interfaces</span></span>

<span data-ttu-id="ba75b-145">使用工作排程器1.0 開發的現有應用程式，可以使用工作排程器1.0 介面中可用的方法，來建立、抓取、修改及刪除 [*工作專案*](w.md)的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="ba75b-145">Existing applications that are developed using Task Scheduler 1.0 can use the methods that are available from the Task Scheduler 1.0 interfaces to create, retrieve, modify, and delete the triggers for a [*work item*](w.md).</span></span> <span data-ttu-id="ba75b-146">不過，請注意，所有工作排程器1.0 介面、列舉和結構都已過時，不應該用於開發新的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ba75b-146">However, note that all Task Scheduler 1.0 interfaces, enumerations, and structures are obsolete and should not be used for the development of new applications.</span></span>

<span data-ttu-id="ba75b-147">下圖顯示用來執行這項操作的兩個介面。</span><span class="sxs-lookup"><span data-stu-id="ba75b-147">The two interfaces that are used to do this are shown in the following illustration.</span></span> <span data-ttu-id="ba75b-148">[**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)介面可用來管理與工作專案相關聯的所有觸發程式 (這類管理包括為工作專案) 建立新的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="ba75b-148">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface is used to manage all the triggers that are associated with a work item (such management includes creating a new trigger for the work item).</span></span> <span data-ttu-id="ba75b-149">[**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger)介面可用來管理特定的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="ba75b-149">The [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface is used to manage a specific trigger.</span></span>

![工作排程器1.0 觸發程式介面](images/tsktri2.png)

<span data-ttu-id="ba75b-151">[**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)介面提供的方法可為工作專案建立新的觸發程式、抓取與工作專案相關聯的觸發程式數目、抓取與工作專案相關聯的觸發程式 [*結構*](t.md)、取得與工作專案相關聯的觸發程式 [*字串*](t.md)，以及刪除觸發程式。</span><span class="sxs-lookup"><span data-stu-id="ba75b-151">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface provides methods for creating a new trigger for a work item, retrieving the number of triggers that are associated with a work item, retrieving the [*trigger structures*](t.md) that are associated with the work item, retrieving [*trigger strings*](t.md) that are associated with the work item, and for deleting triggers.</span></span>

<span data-ttu-id="ba75b-152">一旦觸發程式物件可供使用，您就可以使用 [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) 介面來抓取觸發程式結構和觸發程式的字串，並設定用來引發觸發程式的準則。</span><span class="sxs-lookup"><span data-stu-id="ba75b-152">Once the trigger object is available, you can use the [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface to retrieve the trigger structure and the string of the trigger and to set the criteria that is used to fire the trigger.</span></span> <span data-ttu-id="ba75b-153">只有當您使用工作 [*觸發程式物件*](t.md)時，才會使用此介面。</span><span class="sxs-lookup"><span data-stu-id="ba75b-153">This interface is used only when you are working with a [*task trigger object*](t.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba75b-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="ba75b-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba75b-155">工作觸發程式</span><span class="sxs-lookup"><span data-stu-id="ba75b-155">Task Triggers</span></span>](task-triggers.md)
</dt> <dt>

[<span data-ttu-id="ba75b-156">觸發程式類型</span><span class="sxs-lookup"><span data-stu-id="ba75b-156">Trigger Types</span></span>](trigger-types.md)
</dt> <dt>

[<span data-ttu-id="ba75b-157">觸發程式結構</span><span class="sxs-lookup"><span data-stu-id="ba75b-157">Trigger Structures</span></span>](trigger-structures.md)
</dt> </dl>

 

 