---
title: 正在抓取觸發字串範例
description: 您可以使用 IScheduledWorkItem 或 ITaskTrigger 介面，根據您正在使用的物件類型，取得已知觸發程式的觸發程式字串。
ms.assetid: adfa95b1-54f0-4bcd-a260-ca76fd77d43e
keywords:
- 正在抓取觸發字串工作排程器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44708fdbb4025f5d99409297dda65504a909aec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968294"
---
# <a name="retrieving-trigger-strings-example"></a><span data-ttu-id="a3569-104">正在抓取觸發字串範例</span><span class="sxs-lookup"><span data-stu-id="a3569-104">Retrieving Trigger Strings Example</span></span>

<span data-ttu-id="a3569-105">您可以使用 [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) 或 [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) 介面，根據您正在使用的物件類型，取得已知觸發程式的觸發程式字串。</span><span class="sxs-lookup"><span data-stu-id="a3569-105">You can retrieve the trigger strings of a known trigger using the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) or [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface, depending on the type of object you are working with.</span></span>

<span data-ttu-id="a3569-106">使用工作 [*物件*](t.md)時，請使用 [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) 介面的方法來取得工作專案的觸發程式字串。</span><span class="sxs-lookup"><span data-stu-id="a3569-106">When working with a [*task object*](t.md), use the methods of the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface to retrieve the trigger strings of a work item.</span></span>

<span data-ttu-id="a3569-107">當您使用工作觸發程式 [*物件*](t.md)時，請使用 [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) 介面的方法來取出觸發程式的觸發程式字串。</span><span class="sxs-lookup"><span data-stu-id="a3569-107">When you are working with a [*task trigger object*](t.md), use the methods of the [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface to retrieve the trigger string of the trigger.</span></span>

<span data-ttu-id="a3569-108">下列範例示範如何使用 [**IScheduledWorkItem：： GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) 來顯示與已知工作相關聯之所有觸發程式的字串。</span><span class="sxs-lookup"><span data-stu-id="a3569-108">The following example shows how to use [**IScheduledWorkItem::GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) to display the strings of all triggers associated with a known task.</span></span>

<span data-ttu-id="a3569-109">下列程式描述如何取出工作的觸發程式字串。</span><span class="sxs-lookup"><span data-stu-id="a3569-109">The following procedure describes how to retrieve the trigger strings of a task.</span></span>

<span data-ttu-id="a3569-110">**取得工作的觸發程式字串**</span><span class="sxs-lookup"><span data-stu-id="a3569-110">**To retrieve the trigger strings of a task**</span></span>

1.  <span data-ttu-id="a3569-111">呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得工作排程器物件。</span><span class="sxs-lookup"><span data-stu-id="a3569-111">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="a3569-112"> (此範例假設工作排程器服務正在執行。 ) </span><span class="sxs-lookup"><span data-stu-id="a3569-112">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="a3569-113">呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以取得 task 物件的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面。</span><span class="sxs-lookup"><span data-stu-id="a3569-113">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="a3569-114"> (請注意，此範例會取得 "Test Task" 工作。 ) </span><span class="sxs-lookup"><span data-stu-id="a3569-114">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="a3569-115">呼叫 **ITask：： GetTriggerCount** ，找出與工作相關聯的觸發程式數目。</span><span class="sxs-lookup"><span data-stu-id="a3569-115">Call **ITask::GetTriggerCount** to find out how many triggers are associated with a task.</span></span> <span data-ttu-id="a3569-116"> (請注意， [**GetTriggerCount**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggercount)是 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)所繼承的 [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)方法 ) 。</span><span class="sxs-lookup"><span data-stu-id="a3569-116">(Note that [**GetTriggerCount**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggercount) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>
4.  <span data-ttu-id="a3569-117">顯示觸發字串，針對與工作相關聯的每個觸發程式呼叫 **ITask：： GetTriggerString** 。</span><span class="sxs-lookup"><span data-stu-id="a3569-117">Display the trigger strings, calling **ITask::GetTriggerString** for each trigger associated with the task.</span></span> <span data-ttu-id="a3569-118"> (請注意， [**GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring)是 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)所繼承的 [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)方法 ) 。</span><span class="sxs-lookup"><span data-stu-id="a3569-118">(Note that [**GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>
5.  <span data-ttu-id="a3569-119">釋放所有資源。</span><span class="sxs-lookup"><span data-stu-id="a3569-119">Release all resources.</span></span> <span data-ttu-id="a3569-120">呼叫 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 來釋放觸發字串和 **ITask：： release** 以釋出 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面。</span><span class="sxs-lookup"><span data-stu-id="a3569-120">Call [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the trigger strings and **ITask::Release** to release the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span> <span data-ttu-id="a3569-121"> (請注意，[**版本**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)是 **ITask** 所繼承的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)方法 ) </span><span class="sxs-lookup"><span data-stu-id="a3569-121">(Note that [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by **ITask**.)</span></span>



| <span data-ttu-id="a3569-122">如需的程式碼範例</span><span class="sxs-lookup"><span data-stu-id="a3569-122">For a code example of</span></span>                                                         | <span data-ttu-id="a3569-123">請參閱</span><span class="sxs-lookup"><span data-stu-id="a3569-123">See</span></span>                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3569-124">針對與已知工作相關聯的所有觸發程式抓取觸發字串</span><span class="sxs-lookup"><span data-stu-id="a3569-124">Retrieving a trigger string for all the triggers associated with a known task</span></span> | [<span data-ttu-id="a3569-125">程式碼範例：正在抓取觸發字串</span><span class="sxs-lookup"><span data-stu-id="a3569-125">Code Example: Retrieving Trigger Strings</span></span>](c-c-code-example-retrieving-trigger-strings.md) |



 

## <a name="related-topics"></a><span data-ttu-id="a3569-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="a3569-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3569-127">工作排程器1.0 範例</span><span class="sxs-lookup"><span data-stu-id="a3569-127">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 