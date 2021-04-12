---
title: " (腳本) 的每週觸發程式範例"
description: 此腳本範例示範如何在每週星期一的上午 8 00 建立執行「記事本」的工作。
ms.assetid: 68ef73b0-3780-480e-90fe-940b6e8a5340
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4d9cf627591250c341008ba3a5129c4cc10cad6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372012"
---
# <a name="weekly-trigger-example-scripting"></a><span data-ttu-id="b32d3-103"> (腳本) 的每週觸發程式範例</span><span class="sxs-lookup"><span data-stu-id="b32d3-103">Weekly Trigger Example (Scripting)</span></span>

<span data-ttu-id="b32d3-104">此腳本範例示範如何在每週星期一的上午8:00 建立執行「記事本」的工作。</span><span class="sxs-lookup"><span data-stu-id="b32d3-104">This scripting example shows how to create a task that runs Notepad at 8:00 AM on Monday of every week.</span></span> <span data-ttu-id="b32d3-105">此工作包含每日觸發程式，以指定工作執行的時間，以及執行「記事本」的可執行動作。</span><span class="sxs-lookup"><span data-stu-id="b32d3-105">The task contains a daily trigger that specifies when the task runs and an executable action that runs Notepad.</span></span>

<span data-ttu-id="b32d3-106">下列程式描述如何排程工作，以在每週星期一的上午8:00 啟動可執行檔。</span><span class="sxs-lookup"><span data-stu-id="b32d3-106">The following procedure describes how to schedule a task to start an executable at 8:00 AM on Monday of every week.</span></span>

<span data-ttu-id="b32d3-107">**將 [記事本] 排定在每週星期一上午8:00 開始**</span><span class="sxs-lookup"><span data-stu-id="b32d3-107">**To schedule Notepad to start at 8:00 AM on Monday of every week**</span></span>

1.  <span data-ttu-id="b32d3-108">建立 [**TaskService**](taskservice.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="b32d3-108">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="b32d3-109">此物件可讓您在指定的資料夾中建立工作。</span><span class="sxs-lookup"><span data-stu-id="b32d3-109">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="b32d3-110">取得工作資料夾並建立工作。</span><span class="sxs-lookup"><span data-stu-id="b32d3-110">Get a task folder and create a task.</span></span> <span data-ttu-id="b32d3-111">使用 [**TaskService. GetFolder**](taskservice-getfolder.md) 方法取得儲存工作的資料夾，以及使用 [**TaskService. NewTask**](taskservice-newtask.md) 方法來建立代表工作的 [**TaskDefinition**](taskdefinition.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="b32d3-111">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="b32d3-112">使用 [**TaskDefinition**](taskdefinition.md) 物件定義工作的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b32d3-112">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="b32d3-113">您可以使用 [ [**TaskDefinition**](taskdefinition-settings.md) ] 屬性來定義決定工作排程器服務如何執行工作的設定，以及使用 [**TaskDefinition RegistrationInfo**](taskdefinition-registrationinfo.md) 屬性來定義描述工作的資訊。</span><span class="sxs-lookup"><span data-stu-id="b32d3-113">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="b32d3-114">使用 [**TaskDefinition**](taskdefinition-triggers.md) 屬性來建立每週觸發程式。</span><span class="sxs-lookup"><span data-stu-id="b32d3-114">Create a weekly trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="b32d3-115">這個屬性會提供用來建立觸發程式之 [**TriggerCollection**](triggercollection.md) 物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="b32d3-115">This property provides access to the [**TriggerCollection**](triggercollection.md) object that is used to create the trigger.</span></span>

    <span data-ttu-id="b32d3-116">使用 [**TriggerCollection**](triggercollection-create.md) 方法 (指定您要建立的觸發程式類型) 建立每週觸發程式。</span><span class="sxs-lookup"><span data-stu-id="b32d3-116">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger you want to create) to create a weekly trigger.</span></span>

    <span data-ttu-id="b32d3-117">設定 [**WeeklyTrigger StartBoundary**](trigger-startboundary.md) 屬性，以指定啟動觸發程式的時間，以及執行工作的當日時間。</span><span class="sxs-lookup"><span data-stu-id="b32d3-117">Set the [**WeeklyTrigger.StartBoundary**](trigger-startboundary.md) property to specify when the trigger is activated and the time of the day when the task is run.</span></span> <span data-ttu-id="b32d3-118">在此範例中，會在2005年1月1日啟動觸發程式，且工作會在上午8:00 執行。</span><span class="sxs-lookup"><span data-stu-id="b32d3-118">In this example the trigger is activated on January 1, 2005 and the task runs at 8:00 AM.</span></span>

    <span data-ttu-id="b32d3-119">設定 [**WeeklyTrigger EndBoundary**](trigger-endboundary.md)屬性，以指定何時停用觸發程式。</span><span class="sxs-lookup"><span data-stu-id="b32d3-119">Set the [**WeeklyTrigger.EndBoundary**](trigger-endboundary.md)property to specify when the trigger is deactivated.</span></span> <span data-ttu-id="b32d3-120">在此範例中，會在2015年1月1日停用觸發程式。</span><span class="sxs-lookup"><span data-stu-id="b32d3-120">In this example the trigger is deactivated on January 1, 2015.</span></span>

    <span data-ttu-id="b32d3-121">設定 [**WeeklyTrigger DaysOfWeek**](weeklytrigger-daysofweek.md) 屬性，以指定工作執行的周間日。</span><span class="sxs-lookup"><span data-stu-id="b32d3-121">Set the [**WeeklyTrigger.DaysOfWeek**](weeklytrigger-daysofweek.md) property to specify the days of the week on which the task runs.</span></span> <span data-ttu-id="b32d3-122">在此範例中，工作會在星期一執行。</span><span class="sxs-lookup"><span data-stu-id="b32d3-122">In this example the task is run on Monday.</span></span>

    <span data-ttu-id="b32d3-123">設定 [**WeeklyTrigger WeeksInterval**](weeklytrigger-weeksinterval.md)屬性，以指定排程中周之間的間隔。</span><span class="sxs-lookup"><span data-stu-id="b32d3-123">Set the [**WeeklyTrigger.WeeksInterval**](weeklytrigger-weeksinterval.md)property to specify the interval between the weeks in the schedule.</span></span> <span data-ttu-id="b32d3-124">在此範例中，工作會每週執行一次。</span><span class="sxs-lookup"><span data-stu-id="b32d3-124">In this example the task runs every week.</span></span>

5.  <span data-ttu-id="b32d3-125">使用 [ [**TaskDefinition**](taskdefinition-actions.md) ] 屬性，建立要執行之工作的動作。</span><span class="sxs-lookup"><span data-stu-id="b32d3-125">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="b32d3-126">這個屬性會提供用來建立動作之 [**actioncollection 動作**](actioncollection.md) 物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="b32d3-126">This property provides access to the [**ActionCollection**](actioncollection.md) object used to create the action.</span></span> <span data-ttu-id="b32d3-127">使用 [**actioncollection 動作**](actioncollection-create.md) 方法來指定您要建立的動作類型。</span><span class="sxs-lookup"><span data-stu-id="b32d3-127">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action you want to create.</span></span> <span data-ttu-id="b32d3-128">這個範例會使用 [**ExecAction**](execaction.md) 物件，代表執行命令列操作的動作。</span><span class="sxs-lookup"><span data-stu-id="b32d3-128">This example uses an [**ExecAction**](execaction.md) object, which represents an action that executes a command-line operation.</span></span>
6.  <span data-ttu-id="b32d3-129">使用 [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) 方法註冊工作。</span><span class="sxs-lookup"><span data-stu-id="b32d3-129">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="b32d3-130">在此範例中，工作會在每週星期一的上午8:00 啟動「記事本」。</span><span class="sxs-lookup"><span data-stu-id="b32d3-130">For this example the task will start Notepad at 8:00 AM on Monday of every week.</span></span>

<span data-ttu-id="b32d3-131">下列 VBScript 範例示範如何排程工作每天上午8:00 執行 [記事本]。</span><span class="sxs-lookup"><span data-stu-id="b32d3-131">The following VBScript example shows how to schedule a task to execute Notepad every day at 8:00 AM.</span></span>


```VB
'------------------------------------------------------------------
' This sample schedules a task to start on a weekly basis.
'------------------------------------------------------------------

' A constant that specifies a weekly trigger.
const TriggerTypeWeekly = 3
' A constant that specifies an executable action.
const ActionTypeExec = 0   


'********************************************************
' Create the TaskService object.
Set service = CreateObject("Schedule.Service")
call service.Connect()

'********************************************************
' Get a folder to create a task definition in. 
Dim rootFolder
Set rootFolder = service.GetFolder("\")

' The taskDefinition variable is the TaskDefinition object.
Dim taskDefinition
' The flags parameter is 0 because it is not supported.
Set taskDefinition = service.NewTask(0) 

'********************************************************
' Define information about the task.

' Set the registration info for the task by 
' creating the RegistrationInfo object.
Dim regInfo
Set regInfo = taskDefinition.RegistrationInfo
regInfo.Description = "Start Notepad weekly."
regInfo.Author = "Administrator"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.Enabled = True
settings.StartWhenAvailable = True
settings.Hidden = False

'********************************************************
' Create a weekly trigger. Note that the start boundary 
' specifies the time of day that the task starts, the 
' day-of-week specfies on what day of the week the task 
' runs, and the interval specifies what weeks the task runs.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeWeekly)

' Trigger variables that define when the trigger is active 
' and the time of day that the task is run. The format of 
' this tims is YYYY-MM-DDTHH:MM:SS
Dim startTime, endTime

Dim time
startTime = "2006-05-02T08:00:00"  'Task runs at 8:00 AM
endTime = "2015-05-02T08:00:00"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.DaysOfWeek = 1
trigger.WeeksInterval = 1    'Task runs every week.
trigger.Id = "WeeklyTriggerId"
trigger.Enabled = True

'***********************************************************
' Create the action for the task to execute.

' Add an action to the task to run notepad.exe.
Dim Action
Set Action = taskDefinition.Actions.Create( ActionTypeExec )
Action.Path = "C:\Windows\System32\notepad.exe"

WScript.Echo "Task definition created. About to submit the task..."

'***********************************************************
' Register (create) the task.

call rootFolder.RegisterTaskDefinition( _
    "Test Weekly Trigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."

```



## <a name="related-topics"></a><span data-ttu-id="b32d3-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="b32d3-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b32d3-133">使用工作排程器</span><span class="sxs-lookup"><span data-stu-id="b32d3-133">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




