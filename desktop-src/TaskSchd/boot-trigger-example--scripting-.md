---
title: " (腳本) 的開機觸發程式範例"
description: 這個腳本範例示範如何建立在系統開機時排程執行「記事本」的工作。
ms.assetid: 73ae9cc4-ef89-4390-ac05-8a773f45fa46
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72b7735c607dfc39b848532a70e4d24b1a14d346
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021461"
---
# <a name="boot-trigger-example-scripting"></a><span data-ttu-id="55bb7-103"> (腳本) 的開機觸發程式範例</span><span class="sxs-lookup"><span data-stu-id="55bb7-103">Boot Trigger Example (Scripting)</span></span>

<span data-ttu-id="55bb7-104">這個腳本範例示範如何建立在系統開機時排程執行「記事本」的工作。</span><span class="sxs-lookup"><span data-stu-id="55bb7-104">This scripting example shows how to create a task that is scheduled to execute Notepad when the system is booted.</span></span> <span data-ttu-id="55bb7-105">此工作包含開機觸發程式，可指定啟動系統之後工作啟動的開始界限和延遲時間。</span><span class="sxs-lookup"><span data-stu-id="55bb7-105">The task contains a boot trigger that specifies a start boundary and delay time for the task to start after the system is booted.</span></span> <span data-ttu-id="55bb7-106">此工作也包含指定工作以執行 [記事本] 的動作。</span><span class="sxs-lookup"><span data-stu-id="55bb7-106">The task also contains an action that specifies the task to execute Notepad.</span></span> <span data-ttu-id="55bb7-107">此工作是使用本地服務帳戶註冊，以做為執行工作的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="55bb7-107">The task is registered using the Local Service account as a security context to run the task.</span></span>

<span data-ttu-id="55bb7-108">下列程式說明如何排程可執行檔（例如 [記事本]），以便在系統開機時啟動。</span><span class="sxs-lookup"><span data-stu-id="55bb7-108">The following procedure describes how to schedule an executable such as Notepad to start when the system is booted.</span></span>

<span data-ttu-id="55bb7-109">**排定在系統開機時啟動「記事本」**</span><span class="sxs-lookup"><span data-stu-id="55bb7-109">**To schedule Notepad to start when the system is booted**</span></span>

1.  <span data-ttu-id="55bb7-110">建立 [**TaskService**](taskservice.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="55bb7-110">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="55bb7-111">此物件可讓您在指定的資料夾中建立工作。</span><span class="sxs-lookup"><span data-stu-id="55bb7-111">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="55bb7-112">取得工作資料夾並建立工作。</span><span class="sxs-lookup"><span data-stu-id="55bb7-112">Get a task folder and create a task.</span></span> <span data-ttu-id="55bb7-113">使用 [**TaskService. GetFolder**](taskservice-getfolder.md) 方法取得儲存工作的資料夾，以及使用 [**TaskService. NewTask**](taskservice-newtask.md) 方法來建立代表工作的 [**TaskDefinition**](taskdefinition.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="55bb7-113">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="55bb7-114">使用 [**TaskDefinition**](taskdefinition.md) 物件定義工作的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="55bb7-114">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="55bb7-115">您可以使用 [ [**TaskDefinition**](taskdefinition-settings.md) ] 屬性來定義決定工作排程器服務如何執行工作的設定，以及使用 [**TaskDefinition RegistrationInfo**](taskdefinition-registrationinfo.md) 屬性來定義描述工作的資訊。</span><span class="sxs-lookup"><span data-stu-id="55bb7-115">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="55bb7-116">使用 [**TaskDefinition**](taskdefinition-triggers.md) 屬性建立登入觸發程式。</span><span class="sxs-lookup"><span data-stu-id="55bb7-116">Create a logon trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="55bb7-117">這個屬性會提供 [**TriggerCollection**](triggercollection.md) 物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="55bb7-117">This property provides access to the [**TriggerCollection**](triggercollection.md) object.</span></span> <span data-ttu-id="55bb7-118">使用 [**TriggerCollection**](triggercollection-create.md) 方法 (指定您要建立的觸發程式類型) 建立開機觸發程式。</span><span class="sxs-lookup"><span data-stu-id="55bb7-118">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger that you want to create) to create a boot trigger.</span></span> <span data-ttu-id="55bb7-119">當您建立觸發程式時，請設定觸發程式的 [**StartBoundary**](trigger-startboundary.md) 和 [**EndBoundary**](trigger-endboundary.md) 屬性，以啟動並停用觸發程式。</span><span class="sxs-lookup"><span data-stu-id="55bb7-119">As you create the trigger, set the [**StartBoundary**](trigger-startboundary.md) and [**EndBoundary**](trigger-endboundary.md) properties of the trigger to activate and deactivate the trigger.</span></span> <span data-ttu-id="55bb7-120">您也可以針對開機觸發程式的 [**Delay**](boottrigger-delay.md) 屬性指定值。</span><span class="sxs-lookup"><span data-stu-id="55bb7-120">You can also specify a value for the [**Delay**](boottrigger-delay.md) property of the boot trigger.</span></span>
5.  <span data-ttu-id="55bb7-121">使用 [ [**TaskDefinition**](taskdefinition-actions.md) ] 屬性，建立要執行之工作的動作。</span><span class="sxs-lookup"><span data-stu-id="55bb7-121">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="55bb7-122">這個屬性會提供 [**actioncollection 動作**](actioncollection.md) 物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="55bb7-122">This property provides access to the [**ActionCollection**](actioncollection.md) object.</span></span> <span data-ttu-id="55bb7-123">使用 [**actioncollection 動作**](actioncollection-create.md) 方法來指定您要建立的動作類型。</span><span class="sxs-lookup"><span data-stu-id="55bb7-123">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="55bb7-124">這個範例會使用 [**ExecAction**](execaction.md) 物件，此物件代表啟動可執行檔的動作。</span><span class="sxs-lookup"><span data-stu-id="55bb7-124">This example uses an [**ExecAction**](execaction.md) object, which represents an action that starts an executable.</span></span>
6.  <span data-ttu-id="55bb7-125">使用 [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) 方法註冊工作。</span><span class="sxs-lookup"><span data-stu-id="55bb7-125">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="55bb7-126">此工作是使用本地服務帳戶註冊，以做為執行工作的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="55bb7-126">The task is registered using the Local Service account as a security context to run the task.</span></span>

<span data-ttu-id="55bb7-127">下列 VBScript 範例示範如何排程工作在系統開機後30秒內執行「記事本」。</span><span class="sxs-lookup"><span data-stu-id="55bb7-127">The following VBScript example shows how to schedule a task to execute Notepad 30 seconds after the system is booted.</span></span>


```VB
'---------------------------------------------------------
' This sample schedules a task to start notepad.exe 30 seconds after
' the system is booted.
'---------------------------------------------------------

' A constant that specifies a boot trigger.
const TriggerTypeBoot = 8
' A constant that specifies an executable action.
const ActionTypeExecutable = 0   

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
regInfo.Description = "Task will execute Notepad when " & _
    "the computer is booted."
regInfo.Author = "Author Name"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.StartWhenAvailable = True

'********************************************************
' Create a boot trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeBoot)

' Trigger variables that define when the trigger is active.
Dim startTime, endTime
startTime = "2006-05-02T10:49:02"
endTime = "2006-05-02T10:52:02"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.ExecutionTimeLimit = "PT5M"    ' Five minutes
trigger.Id = "BootTriggerId"
trigger.Delay = "PT30S"                ' 30 Seconds   

'***********************************************************
' Create the action for the task to execute.

' Add an action to the task. The action executes notepad.
Dim Action
Set Action = taskDefinition.Actions.Create( ActionTypeExecutable )
Action.Path = "C:\Windows\System32\notepad.exe"

WScript.Echo "Task definition created. About to submit the task..."

'***********************************************************
' Register (create) the task.
const createOrUpdateTask = 6
call rootFolder.RegisterTaskDefinition( _
    "Test Boot Trigger", taskDefinition, createOrUpdateTask, _
    "Local Service", , 5)

WScript.Echo "Task submitted."
```



## <a name="related-topics"></a><span data-ttu-id="55bb7-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="55bb7-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55bb7-129">使用工作排程器</span><span class="sxs-lookup"><span data-stu-id="55bb7-129">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




