---
title: 使用屬性頁編輯工作專案
description: 您可以使用工作排程器服務所提供的圖形使用者介面，來編輯工作專案的屬性。
ms.assetid: 2d7992ce-fa70-41cc-a8e7-74687171537f
keywords:
- 編輯工作專案工作排程器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0958c361f1c076e8ebed6a7e645bf67694a1d01
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682529"
---
# <a name="editing-a-work-item-using-property-pages"></a><span data-ttu-id="480e5-104">使用屬性頁編輯工作專案</span><span class="sxs-lookup"><span data-stu-id="480e5-104">Editing a Work Item using Property Pages</span></span>

<span data-ttu-id="480e5-105">您可以使用工作排程器服務所提供的圖形使用者介面，來編輯工作專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="480e5-105">You can edit the properties of a work item by using the graphic user interface provided by the Task Scheduler Service.</span></span> <span data-ttu-id="480e5-106"> (目前唯一有效的工作專案是 tasks。 ) </span><span class="sxs-lookup"><span data-stu-id="480e5-106">(Currently, the only valid work items are tasks.)</span></span>

<span data-ttu-id="480e5-107">下列程式描述如何使用其屬性頁來編輯工作。</span><span class="sxs-lookup"><span data-stu-id="480e5-107">The following procedure describes how to edit a task using its property pages.</span></span>

<span data-ttu-id="480e5-108">**若要使用其屬性頁編輯工作**</span><span class="sxs-lookup"><span data-stu-id="480e5-108">**To edit a task using its property pages**</span></span>

1.  <span data-ttu-id="480e5-109">呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得工作排程器物件。</span><span class="sxs-lookup"><span data-stu-id="480e5-109">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="480e5-110"> (這些範例假設工作排程器服務正在執行。 ) </span><span class="sxs-lookup"><span data-stu-id="480e5-110">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="480e5-111">呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以取得 task 物件的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面。</span><span class="sxs-lookup"><span data-stu-id="480e5-111">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="480e5-112"> (請注意，工作是目前唯一有效的工作專案類型。 ) </span><span class="sxs-lookup"><span data-stu-id="480e5-112">(Note that tasks are currently the only valid type of work item.)</span></span>
3.  <span data-ttu-id="480e5-113">呼叫 [**IScheduledWorkItem：： EditWorkItem**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-editworkitem) 來顯示工作的屬性頁。</span><span class="sxs-lookup"><span data-stu-id="480e5-113">Call [**IScheduledWorkItem::EditWorkItem**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-editworkitem) to display the property pages for the task.</span></span>
4.  <span data-ttu-id="480e5-114">視需要編輯工作的屬性，然後按一下 [確定] 以接受新的值，並移除顯示的屬性頁。</span><span class="sxs-lookup"><span data-stu-id="480e5-114">Edit the properties of the task as needed, then click OK to accept the new values and remove the displayed property pages.</span></span>



| <span data-ttu-id="480e5-115">如需的程式碼範例</span><span class="sxs-lookup"><span data-stu-id="480e5-115">For a code example of</span></span>                                                                                      | <span data-ttu-id="480e5-116">請參閱</span><span class="sxs-lookup"><span data-stu-id="480e5-116">See</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="480e5-117">顯示已知工作的屬性頁，並允許使用者編輯工作專案的屬性</span><span class="sxs-lookup"><span data-stu-id="480e5-117">Displaying the property pages for a known task and allowing a user to edit the properties of the work item</span></span> | [<span data-ttu-id="480e5-118">C/c + + 程式碼範例：編輯工作專案</span><span class="sxs-lookup"><span data-stu-id="480e5-118">C/C++ Code Example: Editing a Work Item</span></span>](c-c-code-example-editing-a-work-item.md) |



 

## <a name="related-topics"></a><span data-ttu-id="480e5-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="480e5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="480e5-120">工作排程器1.0 範例</span><span class="sxs-lookup"><span data-stu-id="480e5-120">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 