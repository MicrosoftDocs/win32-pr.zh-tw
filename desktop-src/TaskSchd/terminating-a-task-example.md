---
title: 終止工作範例
description: 您可以藉由呼叫 IScheduledWorkItem Terminate 來終止執行中的工作。
ms.assetid: f8401650-e196-4959-8f23-3d649a55f73d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e632b00a9e957849a5735d31018e3444113190
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186046"
---
# <a name="terminating-a-task-example"></a><span data-ttu-id="a65e0-103">終止工作範例</span><span class="sxs-lookup"><span data-stu-id="a65e0-103">Terminating a Task Example</span></span>

<span data-ttu-id="a65e0-104">您可以藉由呼叫 [**IScheduledWorkItem：： terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate)來終止正在執行的工作。</span><span class="sxs-lookup"><span data-stu-id="a65e0-104">You can terminate a task while it is running by calling [**IScheduledWorkItem::Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate).</span></span>

<span data-ttu-id="a65e0-105">下列程式說明如何在工作正在執行時終止工作。</span><span class="sxs-lookup"><span data-stu-id="a65e0-105">The following procedure describes how to terminate a task if it is running.</span></span>

<span data-ttu-id="a65e0-106">**若要終止執行中的工作**</span><span class="sxs-lookup"><span data-stu-id="a65e0-106">**To terminate a task if it is running**</span></span>

1.  <span data-ttu-id="a65e0-107">呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得工作排程器物件。</span><span class="sxs-lookup"><span data-stu-id="a65e0-107">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="a65e0-108"> (此範例假設工作排程器服務正在執行。 ) </span><span class="sxs-lookup"><span data-stu-id="a65e0-108">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="a65e0-109">呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以取得 task 物件的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面。</span><span class="sxs-lookup"><span data-stu-id="a65e0-109">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="a65e0-110"> (請注意，此範例會取得 "Test Task" 工作。 ) </span><span class="sxs-lookup"><span data-stu-id="a65e0-110">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="a65e0-111">呼叫 **ITask：： GetStatus** ，以找出工作是否正在執行。</span><span class="sxs-lookup"><span data-stu-id="a65e0-111">Call **ITask::GetStatus** to find out if the task is running.</span></span> <span data-ttu-id="a65e0-112"> (請注意， [**GetStatus**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getstatus)是 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)所繼承的 [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)方法 ) 。</span><span class="sxs-lookup"><span data-stu-id="a65e0-112">(Note that [**GetStatus**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getstatus) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>
4.  <span data-ttu-id="a65e0-113">檢查工作的狀態，然後呼叫 **ITask：： Terminate** （如果工作正在執行中）。</span><span class="sxs-lookup"><span data-stu-id="a65e0-113">Check the status of the task and then call **ITask::Terminate** if the task is running.</span></span> <span data-ttu-id="a65e0-114"> (請注意， [**Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate)是 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)所繼承的 [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)方法。 ) </span><span class="sxs-lookup"><span data-stu-id="a65e0-114">(Note that [**Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="a65e0-115">如需的程式碼範例</span><span class="sxs-lookup"><span data-stu-id="a65e0-115">For a code example of</span></span>                | <span data-ttu-id="a65e0-116">請參閱</span><span class="sxs-lookup"><span data-stu-id="a65e0-116">See</span></span>                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a65e0-117">驗證已知工作的狀態</span><span class="sxs-lookup"><span data-stu-id="a65e0-117">Verifying the status of a known task</span></span> | [<span data-ttu-id="a65e0-118">C/c + + 程式碼範例：終止工作</span><span class="sxs-lookup"><span data-stu-id="a65e0-118">C/C++ Code Example: Terminating a Task</span></span>](c-c-code-example-terminating-a-task.md) |



 

## <a name="related-topics"></a><span data-ttu-id="a65e0-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="a65e0-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a65e0-120">工作排程器1.0 範例</span><span class="sxs-lookup"><span data-stu-id="a65e0-120">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 