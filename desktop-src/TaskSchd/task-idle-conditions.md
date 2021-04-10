---
title: 工作閒置條件
description: 當電腦進入閒置狀態時，可以透過數種方式來處理工作。 這包括定義閒置觸發程式，或在工作啟動時設定閒置條件。
ms.assetid: 1e480681-b77a-48fe-a732-dd1591eaa08d
keywords:
- 閒置條件工作排程器
- 閒置條件工作排程器、討論
- 建立閒置觸發程式工作排程器
- 閒置觸發程式工作排程器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501be9b73e3ec355b998697fb5e87c5163224b71
ms.sourcegitcommit: 857e701bbd35004661bb047e1f24622af9ff1dd7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/19/2020
ms.locfileid: "103684199"
---
# <a name="task-idle-conditions"></a><span data-ttu-id="13181-108">工作閒置條件</span><span class="sxs-lookup"><span data-stu-id="13181-108">Task idle conditions</span></span>

<span data-ttu-id="13181-109">當電腦進入閒置狀態時，可以透過數種方式來處理工作。</span><span class="sxs-lookup"><span data-stu-id="13181-109">A task can be handled in several ways when the computer enters an idle state.</span></span> <span data-ttu-id="13181-110">這包括定義閒置觸發程式，或在工作啟動時設定閒置條件。</span><span class="sxs-lookup"><span data-stu-id="13181-110">This includes defining an idle trigger or setting the idle conditions for when the task starts.</span></span>

## <a name="detecting-the-idle-state"></a><span data-ttu-id="13181-111">偵測閒置狀態</span><span class="sxs-lookup"><span data-stu-id="13181-111">Detecting the idle state</span></span>

<span data-ttu-id="13181-112">在 Windows 7 中，工作排程器會每隔15分鐘確認電腦處於閒置狀態。</span><span class="sxs-lookup"><span data-stu-id="13181-112">In Windows 7, the Task Scheduler verifies that the computer is in an idle state every 15 minutes.</span></span> <span data-ttu-id="13181-113">工作排程器會使用兩個準則檢查閒置狀態：使用者不存在，且缺少資源耗用量。</span><span class="sxs-lookup"><span data-stu-id="13181-113">Task Scheduler checks for an idle state using two criteria: user absence, and a lack of resource consumption.</span></span> <span data-ttu-id="13181-114">如果在這段時間內沒有鍵盤或滑鼠輸入，就會將使用者視為不存在。</span><span class="sxs-lookup"><span data-stu-id="13181-114">The user is considered absent if there is no keyboard or mouse input during this period of time.</span></span> <span data-ttu-id="13181-115">如果所有處理器和所有磁片都閒置超過上一個偵測間隔的90%，則會將電腦視為閒置。</span><span class="sxs-lookup"><span data-stu-id="13181-115">The computer is considered idle if all the processors and all the disks were idle for more than 90% of the last detection interval.</span></span> <span data-ttu-id="13181-116"> (設定 ES \_ 顯示所需旗標的任何簡報類型應用程式時，會發生例外狀況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="13181-116">(An exception would be for any presentation type application that sets the ES\_DISPLAY\_REQUIRED flag.</span></span> <span data-ttu-id="13181-117">無論使用者活動或資源耗用量為何，此旗標都會強制工作排程不要將系統視為閒置。 ) </span><span class="sxs-lookup"><span data-stu-id="13181-117">This flag forces Task Schedule to not consider the system as being idle, regardless of user activity or resource consumption.)</span></span>

<span data-ttu-id="13181-118">在 Windows 7 中，即使低優先順序執行緒 (執行緒優先順序 < 正常) 執行，工作排程器也會將處理器視為閒置。</span><span class="sxs-lookup"><span data-stu-id="13181-118">In Windows 7, Task Scheduler considers a processor as idle even when low priority threads (thread priority < normal) execute.</span></span>

<span data-ttu-id="13181-119">在 Windows 7 中，當工作排程器偵測到電腦閒置時，服務只會等待使用者輸入標示閒置狀態的結尾。</span><span class="sxs-lookup"><span data-stu-id="13181-119">In Windows 7, when the Task Scheduler detects that the computer is idle, the service waits only for user input to mark the end of the idle state.</span></span>

<span data-ttu-id="13181-120">在 Windows 8 中，工作排程器會執行相同的一般使用者缺少和資源耗用量檢查。</span><span class="sxs-lookup"><span data-stu-id="13181-120">In Windows 8, Task Scheduler performs the same general user absence and resource consumption checks.</span></span> <span data-ttu-id="13181-121">不過，工作排程器會依賴作業系統電源子系統來偵測使用者的狀態。</span><span class="sxs-lookup"><span data-stu-id="13181-121">However, Task Scheduler relies on the operating system power subsystem to detect user presence.</span></span> <span data-ttu-id="13181-122">依預設，在沒有鍵盤或滑鼠輸入的四分鐘之後，使用者會被視為不存在。</span><span class="sxs-lookup"><span data-stu-id="13181-122">By default, the user is considered absent after four minutes of no keyboard or mouse input.</span></span> <span data-ttu-id="13181-123">當使用者存在時，資源耗用量驗證時間會縮短為10分鐘間隔。</span><span class="sxs-lookup"><span data-stu-id="13181-123">The resource consumption verification time is shortened to 10 minute intervals when the user is present.</span></span> <span data-ttu-id="13181-124">當使用者離開時，驗證時間會縮短為30秒的間隔。</span><span class="sxs-lookup"><span data-stu-id="13181-124">When the user is away, the verification time is shortened to 30 second intervals.</span></span> <span data-ttu-id="13181-125">工作排程器會針對下列事件進行額外的資源耗用量檢查：</span><span class="sxs-lookup"><span data-stu-id="13181-125">Task Scheduler makes additional resource consumption checks for the following events:</span></span>

-   <span data-ttu-id="13181-126">使用者狀態變更</span><span class="sxs-lookup"><span data-stu-id="13181-126">User presence state changed</span></span>
-   <span data-ttu-id="13181-127">AC/DC 電源來源已變更</span><span class="sxs-lookup"><span data-stu-id="13181-127">AC/DC power source changed</span></span>
-   <span data-ttu-id="13181-128">電池計量 (只有在電池) 上變更</span><span class="sxs-lookup"><span data-stu-id="13181-128">Battery level changed (only when on batteries)</span></span>

<span data-ttu-id="13181-129">當上述任何事件發生時，工作排程器會在上次驗證時間之後，測試電腦的閒置。</span><span class="sxs-lookup"><span data-stu-id="13181-129">When any of the events above happens, Task Scheduler tests the computer for idleness since the last verification time.</span></span> <span data-ttu-id="13181-130">在實務上，這表示如果在上次驗證時間之後已符合其他條件，工作排程器可能會在偵測到使用者不存在的情況下，立即將系統宣告為閒置。</span><span class="sxs-lookup"><span data-stu-id="13181-130">In practice, this means that Task Scheduler may declare the system as idle immediately after user absence is detected, if the other conditions have been met since the last verification time.</span></span>

<span data-ttu-id="13181-131">在 Windows 8 中，CPU 和 IO 閾值會設定為80%。</span><span class="sxs-lookup"><span data-stu-id="13181-131">In Windows 8, the CPU and IO thresholds are set to 80%.</span></span>

<span data-ttu-id="13181-132">偵測 Windows 8 Server 中的閒置狀態時，工作排程器不會將使用者的目前狀態或缺勤帳戶列入考慮。</span><span class="sxs-lookup"><span data-stu-id="13181-132">When detecting the idle state in Windows 8 Server, Task Scheduler does not take user presence or absence into account.</span></span> <span data-ttu-id="13181-133">為了標示閒置狀態的結尾，工作排程器在90分鐘內修改資源耗用量一次。</span><span class="sxs-lookup"><span data-stu-id="13181-133">To mark the end of the idle state, Task Scheduler revises the resource consumption once in 90 minutes.</span></span>

## <a name="defining-an-idle-trigger"></a><span data-ttu-id="13181-134">定義閒置觸發程式</span><span class="sxs-lookup"><span data-stu-id="13181-134">Defining an idle trigger</span></span>

<span data-ttu-id="13181-135">當電腦進入閒置狀態時，您可以藉由定義閒置觸發程式來啟動工作。</span><span class="sxs-lookup"><span data-stu-id="13181-135">A task can be started when the computer enters an idle state by defining an idle trigger.</span></span>

<span data-ttu-id="13181-136">閒置觸發程式只會在電腦進入觸發程式的起始界限之後進入閒置狀態時，才會觸發工作動作。</span><span class="sxs-lookup"><span data-stu-id="13181-136">An idle trigger will only trigger a task action if the computer enters an idle state after the start boundary of the trigger.</span></span>

<span data-ttu-id="13181-137">應用程式可以使用 [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) 介面來定義閒置觸發程式。</span><span class="sxs-lookup"><span data-stu-id="13181-137">An application can define an idle trigger by using the [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) interface.</span></span>

<span data-ttu-id="13181-138">如果讀取或寫入 XML，閒置觸發程式是由工作排程器架構的 [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) 元素所指定。</span><span class="sxs-lookup"><span data-stu-id="13181-138">If reading or writing XML, the idle trigger is specified by the [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="task-settings-for-idle-conditions"></a><span data-ttu-id="13181-139">閒置條件的工作設定</span><span class="sxs-lookup"><span data-stu-id="13181-139">Task settings for idle conditions</span></span>

<span data-ttu-id="13181-140">工作設定可以用來定義當電腦進入閒置狀態時，工作排程器處理工作的方式。</span><span class="sxs-lookup"><span data-stu-id="13181-140">The task settings can be used to define how the Task Scheduler handles the task when the computer enters an idle state.</span></span>

<span data-ttu-id="13181-141">下圖提供三個可能的時程表，顯示這些不同的閒置條件如何相互關聯。</span><span class="sxs-lookup"><span data-stu-id="13181-141">The following illustrations provide three possible timelines that show how these different idle conditions relate to each other.</span></span> <span data-ttu-id="13181-142">請注意，當工作觸發程式啟動時，或工作視需要啟動時，就會啟動圖例 (而不會要求 [忽略現有的工作限制](/windows/win32/api/taskschd/ne-taskschd-task_run_flags)) 。</span><span class="sxs-lookup"><span data-stu-id="13181-142">Be aware that the illustrations start when the task trigger is activated or when the task is started on demand (without requesting to [ignore the existing task constraints](/windows/win32/api/taskschd/ne-taskschd-task_run_flags)).</span></span>

> [!NOTE]
> <span data-ttu-id="13181-143">*持續時間* 和 *WaitTimeout* 設定已淘汰。</span><span class="sxs-lookup"><span data-stu-id="13181-143">The *Duration* and *WaitTimeout* settings are deprecated.</span></span> <span data-ttu-id="13181-144">它們仍然存在於工作排程器的使用者介面中，而且其介面方法可能仍會傳回有效值，但不再使用這些值。</span><span class="sxs-lookup"><span data-stu-id="13181-144">They're still present in the Task Scheduler user interface, and their interface methods may still return valid values, but they're no longer used.</span></span>

![閒置條件時間軸](images/idle-conditions2.png)

<span data-ttu-id="13181-146">下列清單說明閒置條件。</span><span class="sxs-lookup"><span data-stu-id="13181-146">The following list describes the idle conditions.</span></span>
- <span data-ttu-id="13181-147">閒置開始：電腦進入閒置狀態的時間。</span><span class="sxs-lookup"><span data-stu-id="13181-147">Idle start: The time when the computer enters the idle state.</span></span>
- <span data-ttu-id="13181-148">閒置結束：電腦轉換為閒置狀態的時間。</span><span class="sxs-lookup"><span data-stu-id="13181-148">Idle end: The time when the computer transitions out of the idle state.</span></span> <span data-ttu-id="13181-149">請注意，電腦處於閒置狀態的時間量與先前所述的閒置持續時間時間無關。</span><span class="sxs-lookup"><span data-stu-id="13181-149">Be aware that the amount of time the computer is in the idle state is independent of the idle duration time that was described previously.</span></span>

<span data-ttu-id="13181-150">閒置等候和閒置持續時間已淘汰。</span><span class="sxs-lookup"><span data-stu-id="13181-150">Idle wait and Idle duration have been deprecated.</span></span>
- <span data-ttu-id="13181-151">閒置等候：當工作觸發程式啟動之後，或在視需要啟動工作之後，工作排程器將等待閒置狀態發生的時間量。</span><span class="sxs-lookup"><span data-stu-id="13181-151">Idle wait: The amount of time that the Task Scheduler will wait for an idle state to occur after a task trigger is activated or after the task is started on demand.</span></span>
- <span data-ttu-id="13181-152">閒置持續時間：您希望電腦在啟動工作之前閒置的時間長度。</span><span class="sxs-lookup"><span data-stu-id="13181-152">Idle duration: The amount of time you want the computer to have been idle before starting the task.</span></span>

<span data-ttu-id="13181-153">例如，如果工作設定為 [只有在電腦閒置30分鐘的時間才會啟動]，且工作等候電腦閒置10分鐘，則只有在啟動觸發程式之前，電腦已閒置25分鐘，工作才會在5分鐘內啟動。</span><span class="sxs-lookup"><span data-stu-id="13181-153">For example, if a task is set to start only if the computer is idle for 30 minutes, and the task waits for the computer to be idle for 10 minutes, then the task will launch in 5 minutes only if the computer has been idle for 25 minutes prior to the time the trigger was activated.</span></span> <span data-ttu-id="13181-154">如果電腦在啟動觸發程式後進入閒置狀態5分鐘，工作將不會啟動。</span><span class="sxs-lookup"><span data-stu-id="13181-154">The task will not start if the computer enters an idle state 5 minutes after the trigger is activated.</span></span>

<span data-ttu-id="13181-155">依預設，task [**DisallowStartIfOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) 屬性設定為 true，這表示工作排程器服務將不會執行閒置觸發程式所觸發的工作 (或具有閒置條件的觸發程式) 當電腦以電池電源執行時。</span><span class="sxs-lookup"><span data-stu-id="13181-155">By default, a task [**DisallowStartIfOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) property is set to true, which means the Task Scheduler service will not run tasks that are triggered by an idle trigger (or a trigger with idle conditions) when a computer is running on battery power.</span></span> <span data-ttu-id="13181-156">您可以藉由將 **DisallowStartIfOnBatteries** 屬性設定為 false，來變更此行為。</span><span class="sxs-lookup"><span data-stu-id="13181-156">You can change this behavior by setting the **DisallowStartIfOnBatteries** property to false.</span></span>

<span data-ttu-id="13181-157">如果工作是由閒置觸發程式觸發，則會忽略 [**IIdleSettings**](/windows/desktop/api/taskschd/nn-taskschd-iidlesettings)介面 ([**IdleSettings**](idlesettings.md)的腳本) 的 [**WaitTimeout**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout)屬性。</span><span class="sxs-lookup"><span data-stu-id="13181-157">If a task is triggered by an idle trigger, then the [**WaitTimeout**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout) property of the [**IIdleSettings**](/windows/desktop/api/taskschd/nn-taskschd-iidlesettings) interface ([**IdleSettings**](idlesettings.md) for scripting) is ignored.</span></span>

<span data-ttu-id="13181-158">應用程式可以藉由設定 [**IIdleSettings**](/windows/desktop/api/taskschd/nn-taskschd-iidlesettings) 和 [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) 介面中的屬性來控制閒置條件。</span><span class="sxs-lookup"><span data-stu-id="13181-158">Applications can control the idle conditions by setting the properties in the [**IIdleSettings**](/windows/desktop/api/taskschd/nn-taskschd-iidlesettings) and [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) interfaces.</span></span>

<span data-ttu-id="13181-159">如果讀取或寫入 XML，這些條件會在工作排程器架構的 [**Settings**](taskschedulerschema-settings-tasktype-element.md) 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="13181-159">If reading or writing XML, these conditions are specified in the [**Settings**](taskschedulerschema-settings-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="cycling-idle-condition"></a><span data-ttu-id="13181-160">迴圈閒置條件</span><span class="sxs-lookup"><span data-stu-id="13181-160">Cycling idle condition</span></span>

<span data-ttu-id="13181-161">如果電腦處於閒置狀態，則您可以使用下列閒置條件來終止和重新開機工作。</span><span class="sxs-lookup"><span data-stu-id="13181-161">If the computer is cycling in and out of the idle state, you can terminate and restart the task using the following idle conditions.</span></span> <span data-ttu-id="13181-162">若要終止和重新開機工作，必須將屬性和元素都設為 True：</span><span class="sxs-lookup"><span data-stu-id="13181-162">To terminate and restart a task, both properties and elements must be set to True:</span></span>

-   <span data-ttu-id="13181-163">若要在閒置條件結束時終止工作，請將 [ [**StopOnIdleEnd**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend) ] 屬性或 [ [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) ] 元素設定為 [True]。</span><span class="sxs-lookup"><span data-stu-id="13181-163">To terminate the task when the idle condition ends, set the [**StopOnIdleEnd**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend) property or the [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) element to True.</span></span>
-   <span data-ttu-id="13181-164">若要在電腦再次進入閒置狀態時重新開機工作，請將 [ [**RestartOnIdle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) ] 屬性或 [ [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) ] 元素設定為 [True]。</span><span class="sxs-lookup"><span data-stu-id="13181-164">To restart the task when the computer cycles into the idle condition again, set the [**RestartOnIdle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) property or the [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) element to True.</span></span>
