---
title: 建立閒置觸發程式範例
description: 若要建立閒置觸發程式，您必須在建立觸發程式時指定閒置觸發程式，而且必須設定工作的閒置時間。 如需有關閒置條件的詳細資訊，請參閱工作閒置條件。
ms.assetid: d36a621c-4011-4c3d-b6f4-b56d1f50983c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a7f8333c79d05dfade609f028f93a816e61adf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315925"
---
# <a name="creating-an-idle-trigger-example"></a><span data-ttu-id="8d5b7-104">建立閒置觸發程式範例</span><span class="sxs-lookup"><span data-stu-id="8d5b7-104">Creating an Idle Trigger Example</span></span>

<span data-ttu-id="8d5b7-105">若要建立閒置觸發程式，您必須在建立觸發程式時指定閒置觸發程式，而且必須設定工作的閒置時間。</span><span class="sxs-lookup"><span data-stu-id="8d5b7-105">To create an idle trigger, you must specify an idle trigger when you create the trigger, and you must set the idle time for the task.</span></span> <span data-ttu-id="8d5b7-106">如需有關閒置條件的詳細資訊，請參閱工作 [閒置條件](task-idle-conditions.md)。</span><span class="sxs-lookup"><span data-stu-id="8d5b7-106">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

<span data-ttu-id="8d5b7-107">建立閒置觸發程式之後，請呼叫 [**IPersistFile：： save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) ，以將新的觸發程式儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="8d5b7-107">After creating the idle trigger, call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to save the new trigger to disk.</span></span>

<span data-ttu-id="8d5b7-108">下列程式描述如何建立已知工作的閒置觸發程式。</span><span class="sxs-lookup"><span data-stu-id="8d5b7-108">The following procedure describes how to create an idle trigger for a known task.</span></span>

<span data-ttu-id="8d5b7-109">**若要建立已知工作的閒置觸發程式**</span><span class="sxs-lookup"><span data-stu-id="8d5b7-109">**To create an idle trigger for a known task**</span></span>

1.  <span data-ttu-id="8d5b7-110">呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得工作排程器物件。</span><span class="sxs-lookup"><span data-stu-id="8d5b7-110">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="8d5b7-111"> (此範例假設工作排程器服務正在執行。 ) </span><span class="sxs-lookup"><span data-stu-id="8d5b7-111">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="8d5b7-112">呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以取得 task 物件的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面。</span><span class="sxs-lookup"><span data-stu-id="8d5b7-112">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="8d5b7-113"> (請注意，此範例會取得 "Test Task" 工作。 ) </span><span class="sxs-lookup"><span data-stu-id="8d5b7-113">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="8d5b7-114">呼叫 [**SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) 可設定系統必須保持閒置多久的時間，才會引發觸發程式。</span><span class="sxs-lookup"><span data-stu-id="8d5b7-114">Call [**SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) to set how long the system must remain idle before the trigger will fire.</span></span> <span data-ttu-id="8d5b7-115"> (請注意， **SetIdleWait** 繼承自 [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)。 ) </span><span class="sxs-lookup"><span data-stu-id="8d5b7-115">(Note that **SetIdleWait** is inherited from [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span></span>
4.  <span data-ttu-id="8d5b7-116">定義工作 [**\_ 觸發**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) 程式結構，並呼叫 [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) 來建立閒置觸發程式。</span><span class="sxs-lookup"><span data-stu-id="8d5b7-116">Define the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure and call [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) to create the idle trigger.</span></span> <span data-ttu-id="8d5b7-117"> (請注意， **CreateTrigger** 繼承自 [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)。 ) </span><span class="sxs-lookup"><span data-stu-id="8d5b7-117">(Note that **CreateTrigger** is inherited from [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span></span>
5.  <span data-ttu-id="8d5b7-118">使用 [**IPersistFile：： save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save)，將新的閒置觸發程式儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="8d5b7-118">Save the task with the new idle trigger to disk using [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="8d5b7-119">[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)介面 (是 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)介面所支援的標準 COM 介面。 ) </span><span class="sxs-lookup"><span data-stu-id="8d5b7-119">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface supported by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.)</span></span>
6.  <span data-ttu-id="8d5b7-120">呼叫 **ITask：： release** 以釋放所有資源。</span><span class="sxs-lookup"><span data-stu-id="8d5b7-120">Call **ITask::Release** to release all resources.</span></span> <span data-ttu-id="8d5b7-121"> (請注意，[**版本**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)是 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)所繼承的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)方法 ) </span><span class="sxs-lookup"><span data-stu-id="8d5b7-121">(Note that [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="8d5b7-122">如需的程式碼範例</span><span class="sxs-lookup"><span data-stu-id="8d5b7-122">For a code example of</span></span>                         | <span data-ttu-id="8d5b7-123">請參閱</span><span class="sxs-lookup"><span data-stu-id="8d5b7-123">See</span></span>                                                                                           |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d5b7-124">建立現有工作的閒置觸發程式</span><span class="sxs-lookup"><span data-stu-id="8d5b7-124">Creating an idle trigger for an existing task</span></span> | [<span data-ttu-id="8d5b7-125">C/c + + 程式碼範例：建立閒置觸發程式</span><span class="sxs-lookup"><span data-stu-id="8d5b7-125">C/C++ Code Example: Creating an Idle Trigger</span></span>](c-c-code-example-creating-an-idle-trigger.md) |



 

## <a name="related-topics"></a><span data-ttu-id="8d5b7-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="8d5b7-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d5b7-127">工作排程器1.0 範例</span><span class="sxs-lookup"><span data-stu-id="8d5b7-127">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 