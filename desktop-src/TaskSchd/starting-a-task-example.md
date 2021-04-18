---
title: 啟動工作範例
description: 若要啟動工作，請呼叫 ITask 介面的 Run 方法。 Run 是一個非同步方法，它會嘗試執行工作，並在工作啟動時立即傳回。 工作排程器服務必須執行，這個方法才能成功。
ms.assetid: 90f197de-7a32-4e4b-b4c0-d3f706e47de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 325d8d990367a810351ec4eea8b03b7dc0240cd5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966262"
---
# <a name="starting-a-task-example"></a><span data-ttu-id="0bab1-105">啟動工作範例</span><span class="sxs-lookup"><span data-stu-id="0bab1-105">Starting a Task Example</span></span>

<span data-ttu-id="0bab1-106">若要啟動工作，請呼叫 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)介面的 [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run)方法。</span><span class="sxs-lookup"><span data-stu-id="0bab1-106">To start a task, call the [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) method of the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span> <span data-ttu-id="0bab1-107">**Run** 是一個非同步方法，它會嘗試執行工作，並在工作啟動時立即傳回。</span><span class="sxs-lookup"><span data-stu-id="0bab1-107">**Run** is an asynchronous method that attempts to execute the task and returns as soon as the task has started.</span></span> <span data-ttu-id="0bab1-108">工作排程器服務必須執行，這個方法才能成功。</span><span class="sxs-lookup"><span data-stu-id="0bab1-108">The Task Scheduler service must be running for this method to succeed.</span></span>

<span data-ttu-id="0bab1-109">下列程式說明如何啟動工作。</span><span class="sxs-lookup"><span data-stu-id="0bab1-109">The following procedure describes how to start a task.</span></span>

<span data-ttu-id="0bab1-110">**若要啟動工作**</span><span class="sxs-lookup"><span data-stu-id="0bab1-110">**To start a task**</span></span>

1.  <span data-ttu-id="0bab1-111">呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得工作排程器物件。</span><span class="sxs-lookup"><span data-stu-id="0bab1-111">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="0bab1-112"> (此範例假設工作排程器服務正在執行。 ) </span><span class="sxs-lookup"><span data-stu-id="0bab1-112">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="0bab1-113">呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以取得 task 物件的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面。</span><span class="sxs-lookup"><span data-stu-id="0bab1-113">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="0bab1-114"> (請注意，此範例會取得 "Test Task" 工作。 ) </span><span class="sxs-lookup"><span data-stu-id="0bab1-114">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="0bab1-115">呼叫 [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) 來啟動工作。</span><span class="sxs-lookup"><span data-stu-id="0bab1-115">Call [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) to start the task.</span></span> <span data-ttu-id="0bab1-116">請注意，這個方法是由 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面所繼承。</span><span class="sxs-lookup"><span data-stu-id="0bab1-116">Note that this method is inherited by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span>
4.  <span data-ttu-id="0bab1-117">視需要繼續處理。</span><span class="sxs-lookup"><span data-stu-id="0bab1-117">Continue processing as needed.</span></span>
5.  <span data-ttu-id="0bab1-118">呼叫 **ITask：： Release** 可釋放資源和 [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) ，以將 COM 解除初始化。</span><span class="sxs-lookup"><span data-stu-id="0bab1-118">Call **ITask::Release** to free resources and [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) to uninitialize COM.</span></span> <span data-ttu-id="0bab1-119">此範例會呼叫 [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 以釋放 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="0bab1-119">This example calls [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to free the pointer to the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span> <span data-ttu-id="0bab1-120"> (請注意，**版本** 是 **ITask** 所繼承的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)方法 ) </span><span class="sxs-lookup"><span data-stu-id="0bab1-120">(Note that **Release** is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by **ITask**.)</span></span>



| <span data-ttu-id="0bab1-121">如需的程式碼範例</span><span class="sxs-lookup"><span data-stu-id="0bab1-121">For a code example of</span></span>    | <span data-ttu-id="0bab1-122">請參閱</span><span class="sxs-lookup"><span data-stu-id="0bab1-122">See</span></span>                                                                         |
|--------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="0bab1-123">執行現有的工作</span><span class="sxs-lookup"><span data-stu-id="0bab1-123">Running an existing task</span></span> | [<span data-ttu-id="0bab1-124">C/c + + 程式碼範例：啟動工作</span><span class="sxs-lookup"><span data-stu-id="0bab1-124">C/C++ Code Example: Starting a Task</span></span>](c-c-code-example-starting-a-task.md) |



 

## <a name="related-topics"></a><span data-ttu-id="0bab1-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="0bab1-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bab1-126">工作排程器1.0 範例</span><span class="sxs-lookup"><span data-stu-id="0bab1-126">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 