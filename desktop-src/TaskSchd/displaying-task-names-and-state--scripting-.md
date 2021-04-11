---
title: '顯示工作名稱和狀態 (腳本) '
description: 此腳本範例示範如何列舉工作資料夾中的工作，並顯示每項工作的屬性值。
ms.assetid: 2a84a752-fbf3-4041-8b0a-304f89a49354
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e7a8f22977f8cfd2d40b3c37a1cc8d7bcb5259e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372347"
---
# <a name="displaying-task-names-and-states-scripting"></a><span data-ttu-id="1eccd-103">顯示工作名稱和狀態 (腳本) </span><span class="sxs-lookup"><span data-stu-id="1eccd-103">Displaying Task Names and States (Scripting)</span></span>

<span data-ttu-id="1eccd-104">此腳本範例示範如何列舉工作資料夾中的工作，並顯示每項工作的屬性值。</span><span class="sxs-lookup"><span data-stu-id="1eccd-104">This scripting example shows how to enumerate tasks in a task folder and display property values from each task.</span></span>

<span data-ttu-id="1eccd-105">下列程式說明如何顯示工作資料夾中所有工作的工作名稱和狀態。</span><span class="sxs-lookup"><span data-stu-id="1eccd-105">The following procedure describes how to display task names and states for all the tasks in a task folder.</span></span>

<span data-ttu-id="1eccd-106">**顯示工作資料夾中所有工作的工作名稱和狀態**</span><span class="sxs-lookup"><span data-stu-id="1eccd-106">**To display task names and state for all the tasks in a task folder**</span></span>

1.  <span data-ttu-id="1eccd-107">建立 [**TaskService**](taskservice.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="1eccd-107">Create the [**TaskService**](taskservice.md) object.</span></span>

    <span data-ttu-id="1eccd-108">此物件可讓您連接到工作排程器服務，並存取特定的工作資料夾。</span><span class="sxs-lookup"><span data-stu-id="1eccd-108">This object allows you to connect to the Task Scheduler service and access a specific task folder.</span></span>

2.  <span data-ttu-id="1eccd-109">取得工作資料夾，其中包含您想要的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1eccd-109">Get a task folder that holds the tasks you want information about.</span></span>

    <span data-ttu-id="1eccd-110">使用 [**TaskService. GetFolder**](taskservice-getfolder.md) 方法來取得資料夾。</span><span class="sxs-lookup"><span data-stu-id="1eccd-110">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder.</span></span>

3.  <span data-ttu-id="1eccd-111">從資料夾中取得工作的集合。</span><span class="sxs-lookup"><span data-stu-id="1eccd-111">Get the collection of tasks from the folder.</span></span>

    <span data-ttu-id="1eccd-112">您可以使用 [**TaskFolder GetTasks**](taskfolder-gettasks.md) 方法，取得工作 ([**RegisteredTaskCollection**](registeredtaskcollection.md)) 的集合。</span><span class="sxs-lookup"><span data-stu-id="1eccd-112">Use the [**TaskFolder.GetTasks**](taskfolder-gettasks.md) method to get the collection of tasks ([**RegisteredTaskCollection**](registeredtaskcollection.md)).</span></span>

4.  <span data-ttu-id="1eccd-113">取得集合中的工作數目，並列舉集合中的每個工作。</span><span class="sxs-lookup"><span data-stu-id="1eccd-113">Get the number of tasks in the collection and enumerate through each task in the collection.</span></span>

    <span data-ttu-id="1eccd-114">使用物件的 [**RegisteredTaskCollection**](registeredtaskcollection.md) 集合來取得 [**RegisteredTask**](registeredtask.md) 物件實例。</span><span class="sxs-lookup"><span data-stu-id="1eccd-114">Use the [**RegisteredTaskCollection**](registeredtaskcollection.md) collection of objects to get a [**RegisteredTask**](registeredtask.md) object instance.</span></span> <span data-ttu-id="1eccd-115">每個實例都會包含集合中的工作。</span><span class="sxs-lookup"><span data-stu-id="1eccd-115">Each instance will contain a task in the collection.</span></span> <span data-ttu-id="1eccd-116">然後，您可以從每個已註冊的工作中，顯示 (屬性值) 的資訊。</span><span class="sxs-lookup"><span data-stu-id="1eccd-116">You can then display the information (property values) from each registered task.</span></span>

<span data-ttu-id="1eccd-117">下列 VBScript 範例顯示如何列舉根工作資料夾中已註冊的工作集合，並顯示每項工作的名稱和狀態。</span><span class="sxs-lookup"><span data-stu-id="1eccd-117">The following VBScript example shows how to enumerate through a collection of registered tasks in the root task folder and display the name and state for each task.</span></span>


```VB
'---------------------------------------------------------
' This sample enumerates through the tasks on the local computer and
' displays their name and state.
'---------------------------------------------------------


' Create the TaskService object.
Set service = CreateObject("Schedule.Service")
call service.Connect()

' Get the task folder that contains the tasks. 
Dim rootFolder
Set rootFolder = service.GetFolder("\")
 
Dim taskCollection
Set taskCollection = rootFolder.GetTasks(0)

Dim numberOfTasks
numberOfTasks = taskCollection.Count

If numberOfTasks = 0 Then 
    Wscript.Echo "No tasks are registered."
Else
    WScript.Echo "Number of tasks registered: " & numberOfTasks
    
    Dim registeredTask
    For Each registeredTask In taskCollection
        WScript.Echo "Task Name: " & registeredTask.Name
    
        Dim taskState 
        Select Case registeredTask.State 
            Case "0"
                taskState = "Unknown"
            Case "1"
                taskState = "Disabled"
            Case "2"
                taskState = "Queued"
            Case "3"
                taskState = "Ready"
            Case "4"
                taskState = "Running"
        End Select

        WScript.Echo "    Task State: " & taskState
    Next
End If

```



## <a name="related-topics"></a><span data-ttu-id="1eccd-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="1eccd-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1eccd-119">使用工作排程器</span><span class="sxs-lookup"><span data-stu-id="1eccd-119">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




