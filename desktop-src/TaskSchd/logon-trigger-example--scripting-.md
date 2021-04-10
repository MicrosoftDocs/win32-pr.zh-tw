---
title: '登入觸發程式範例 (腳本) '
description: 這個腳本範例會示範如何建立排定在使用者登入時執行「記事本」的工作。
ms.assetid: f25e105f-9439-4646-bdfd-609ee99a5d55
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72a8c4b5d0d67b59160eb3ed0b13885ee7e0eb51
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183281"
---
# <a name="logon-trigger-example-scripting"></a><span data-ttu-id="74110-103">登入觸發程式範例 (腳本) </span><span class="sxs-lookup"><span data-stu-id="74110-103">Logon Trigger Example (Scripting)</span></span>

<span data-ttu-id="74110-104">這個腳本範例會示範如何建立排定在使用者登入時執行「記事本」的工作。</span><span class="sxs-lookup"><span data-stu-id="74110-104">This scripting example shows how to create a task that is scheduled to execute Notepad when a user logs on.</span></span> <span data-ttu-id="74110-105">此工作包含登入觸發程式，可指定開始工作的開始界限，以及指定使用者的使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="74110-105">The task contains a logon trigger that specifies a start boundary for the task to start and a user identifier that specifies the user.</span></span> <span data-ttu-id="74110-106">此工作會使用 Administrators 群組作為安全性內容來執行工作，以進行註冊。</span><span class="sxs-lookup"><span data-stu-id="74110-106">The task is registered using the Administrators group as a security context to run the task.</span></span>

<span data-ttu-id="74110-107">下列程式描述如何排程可執行檔（例如 [記事本]），以便在指定的使用者登入時啟動。</span><span class="sxs-lookup"><span data-stu-id="74110-107">The following procedure describes how to schedule an executable such as Notepad to start when a specified user logs on.</span></span>

<span data-ttu-id="74110-108">**排定在使用者登入時啟動 [記事本]**</span><span class="sxs-lookup"><span data-stu-id="74110-108">**To schedule Notepad to start when a user logs on**</span></span>

1.  <span data-ttu-id="74110-109">建立 [**TaskService**](taskservice.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="74110-109">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="74110-110">此物件可讓您在指定的資料夾中建立工作。</span><span class="sxs-lookup"><span data-stu-id="74110-110">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="74110-111">取得工作資料夾並建立工作。</span><span class="sxs-lookup"><span data-stu-id="74110-111">Get a task folder and create a task.</span></span> <span data-ttu-id="74110-112">使用 [**TaskService. GetFolder**](taskservice-getfolder.md) 方法取得儲存工作的資料夾，以及使用 [**TaskService. NewTask**](taskservice-newtask.md) 方法來建立代表工作的 [**TaskDefinition**](taskdefinition.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="74110-112">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="74110-113">使用 [**TaskDefinition**](taskdefinition.md) 物件定義工作的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="74110-113">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="74110-114">您可以使用 [ [**TaskDefinition**](taskdefinition-settings.md) ] 屬性來定義決定工作排程器服務如何執行工作的設定，以及使用 [**TaskDefinition RegistrationInfo**](taskdefinition-registrationinfo.md) 屬性來定義描述工作的資訊。</span><span class="sxs-lookup"><span data-stu-id="74110-114">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="74110-115">使用 [**TaskDefinition**](taskdefinition-triggers.md) 屬性建立登入觸發程式。</span><span class="sxs-lookup"><span data-stu-id="74110-115">Create a logon trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="74110-116">這個屬性會提供 [**TriggerCollection**](triggercollection.md) 物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="74110-116">This property provides access to the [**TriggerCollection**](triggercollection.md) object.</span></span> <span data-ttu-id="74110-117">使用 [**TriggerCollection**](triggercollection-create.md) 方法 (指定您要建立的觸發程式類型) 建立登入觸發程式。</span><span class="sxs-lookup"><span data-stu-id="74110-117">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger that you want to create) to create a logon trigger.</span></span> <span data-ttu-id="74110-118">當您建立觸發程式時，請設定觸發程式的開始界限和結束界限，以啟動並停用觸發程式。</span><span class="sxs-lookup"><span data-stu-id="74110-118">As you create the trigger, set the start boundary and end boundary of the trigger to activate and deactivate the trigger.</span></span> <span data-ttu-id="74110-119">您必須設定觸發程式的 [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) 屬性，如此一來，當指定的使用者在開始界限之後登入時，就會排定工作的動作執行。</span><span class="sxs-lookup"><span data-stu-id="74110-119">You must set the [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) property for the trigger so that the task's actions will be scheduled to execute when the specified user logs on after the start boundary.</span></span>
5.  <span data-ttu-id="74110-120">使用 [ [**TaskDefinition**](taskdefinition-actions.md) ] 屬性，建立要執行之工作的動作。</span><span class="sxs-lookup"><span data-stu-id="74110-120">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="74110-121">這個屬性會提供 [**actioncollection 動作**](actioncollection.md) 物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="74110-121">This property provides access to the [**ActionCollection**](actioncollection.md) object.</span></span> <span data-ttu-id="74110-122">使用 [**actioncollection 動作**](actioncollection-create.md) 方法來指定您要建立的動作類型。</span><span class="sxs-lookup"><span data-stu-id="74110-122">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="74110-123">這個範例會使用 [**ExecAction**](execaction.md) 物件，此物件代表啟動可執行檔的動作。</span><span class="sxs-lookup"><span data-stu-id="74110-123">This example uses an [**ExecAction**](execaction.md) object, which represents an action that starts an executable.</span></span>
6.  <span data-ttu-id="74110-124">使用 [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) 方法註冊工作。</span><span class="sxs-lookup"><span data-stu-id="74110-124">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="74110-125">此範例會註冊工作，讓它使用系統管理員群組做為執行工作的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="74110-125">This example registers the task so that it uses the Administrators group as a security context to run the task.</span></span>

<span data-ttu-id="74110-126">下列 VBScript 範例示範如何排程工作，以在使用者登入時執行 [記事本]。</span><span class="sxs-lookup"><span data-stu-id="74110-126">The following VBScript example shows how to schedule a task to execute Notepad when a user logs on.</span></span>


```VB
'---------------------------------------------------------
' This sample schedules a task to start notepad.exe when a user logs on.
'---------------------------------------------------------

' A constant that specifies a logon trigger.
const TriggerTypeLogon = 9
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
regInfo.Description = "Task will execute Notepad when a " & _
    "specified user logs on."
regInfo.Author = "Author Name"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.StartWhenAvailable = True

'********************************************************
' Create a logon trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeLogon)

' Trigger variables that define when the trigger is active.
Dim startTime, endTime
startTime = "2006-05-02T10:49:02"
endTime = "2006-05-02T10:52:02"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.ExecutionTimeLimit = "PT5M"    ' Five minutes
trigger.Id = "LogonTriggerId"
trigger.UserId = "DOMAIN\UserName"   ' Must be a valid user account   

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
    "Test Logon Trigger", taskDefinition, createOrUpdateTask, _
    "Builtin\Administrators", , 4)

WScript.Echo "Task submitted."
```



## <a name="related-topics"></a><span data-ttu-id="74110-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="74110-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74110-128">使用工作排程器</span><span class="sxs-lookup"><span data-stu-id="74110-128">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




