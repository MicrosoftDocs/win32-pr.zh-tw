---
title: 建立新的觸發程式
description: 若要建立觸發程式，您必須使用三個介面。
ms.assetid: c0f121ff-d0a5-4b6c-935c-6f47b4ea26d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f48ecb7b06e5bade6d5ad80e4c9a82794f6a17e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376040"
---
# <a name="creating-a-new-trigger"></a><span data-ttu-id="3e311-103">建立新的觸發程式</span><span class="sxs-lookup"><span data-stu-id="3e311-103">Creating a New Trigger</span></span>

<span data-ttu-id="3e311-104">若要建立觸發程式，您必須使用三個介面。</span><span class="sxs-lookup"><span data-stu-id="3e311-104">To create a trigger you must use three interfaces.</span></span> <span data-ttu-id="3e311-105">[**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) 提供 [**IScheduledWorkItem：： CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) 方法來建立觸發程式物件、 [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) 提供 [**ITaskTrigger：： SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) 方法來設定觸發程式的準則，而 COM 介面 [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) 提供儲存新觸發程式至磁片的 **儲存** 方法。</span><span class="sxs-lookup"><span data-stu-id="3e311-105">[**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) provides the [**IScheduledWorkItem::CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) method for creating the trigger object, [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) provides the [**ITaskTrigger::SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) method for setting the criteria for the trigger, and the COM interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) provides a **Save** method for saving the new trigger to disk.</span></span>

<span data-ttu-id="3e311-106">下列程式說明如何建立新的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="3e311-106">The following procedure describes how to create a new trigger.</span></span>

<span data-ttu-id="3e311-107">**建立新的觸發程式**</span><span class="sxs-lookup"><span data-stu-id="3e311-107">**To create a new trigger**</span></span>

1.  <span data-ttu-id="3e311-108">呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得工作排程器物件。</span><span class="sxs-lookup"><span data-stu-id="3e311-108">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="3e311-109"> (此範例假設工作排程器服務正在執行。 ) </span><span class="sxs-lookup"><span data-stu-id="3e311-109">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="3e311-110">呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以取得 task 物件的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面。</span><span class="sxs-lookup"><span data-stu-id="3e311-110">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="3e311-111"> (請注意，此範例會取得 "Test Task" 工作。 ) </span><span class="sxs-lookup"><span data-stu-id="3e311-111">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="3e311-112">呼叫 [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) 來建立觸發程式物件。</span><span class="sxs-lookup"><span data-stu-id="3e311-112">Call [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) to create a trigger object.</span></span> <span data-ttu-id="3e311-113"> (請注意， [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) 繼承自 [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)。 ) </span><span class="sxs-lookup"><span data-stu-id="3e311-113">(Note that [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) is inherited from [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span></span>
4.  <span data-ttu-id="3e311-114">定義工作 [**\_ 觸發**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) 程式結構。</span><span class="sxs-lookup"><span data-stu-id="3e311-114">Define a [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure.</span></span> <span data-ttu-id="3e311-115">請注意，工作 **\_ 觸發** 程式的 wBeginDay、wBeginMonth 和 wBeginYear 成員必須分別設定為有效的日、月和年。</span><span class="sxs-lookup"><span data-stu-id="3e311-115">Note that wBeginDay, wBeginMonth, and wBeginYear members of **TASK\_TRIGGER** must be set to a valid day, month, and year respectively.</span></span>
5.  <span data-ttu-id="3e311-116">呼叫 [**ITaskTrigger：： SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) 來設定觸發準則。</span><span class="sxs-lookup"><span data-stu-id="3e311-116">Call [**ITaskTrigger::SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) to set the trigger criteria.</span></span>
6.  <span data-ttu-id="3e311-117">使用 [**IPersistFile：： save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save)，將新的觸發程式儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="3e311-117">Save the task with the new trigger to disk using [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="3e311-118">[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)介面 (是 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)介面所支援的標準 COM 介面。 ) </span><span class="sxs-lookup"><span data-stu-id="3e311-118">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface supported by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.)</span></span>
7.  <span data-ttu-id="3e311-119">呼叫 [**release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 以釋出所有資源。</span><span class="sxs-lookup"><span data-stu-id="3e311-119">Call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release all resources.</span></span> <span data-ttu-id="3e311-120"> (請注意，**版本** 是 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)所繼承的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)方法 ) </span><span class="sxs-lookup"><span data-stu-id="3e311-120">(Note that **Release** is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="3e311-121">如需的程式碼範例</span><span class="sxs-lookup"><span data-stu-id="3e311-121">For a code example of</span></span>                       | <span data-ttu-id="3e311-122">請參閱</span><span class="sxs-lookup"><span data-stu-id="3e311-122">See</span></span>                                                                                         |
|---------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e311-123">為現有的工作建立新的觸發程式</span><span class="sxs-lookup"><span data-stu-id="3e311-123">Creating a new trigger for an existing task</span></span> | [<span data-ttu-id="3e311-124">C/c + + 程式碼範例：建立工作觸發程式</span><span class="sxs-lookup"><span data-stu-id="3e311-124">C/C++ Code Example: Creating a Task Trigger</span></span>](c-c-code-example-creating-a-task-trigger.md) |



 

## <a name="related-topics"></a><span data-ttu-id="3e311-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="3e311-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e311-126">工作排程器1.0 範例</span><span class="sxs-lookup"><span data-stu-id="3e311-126">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 