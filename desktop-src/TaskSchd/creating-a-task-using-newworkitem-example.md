---
title: 使用 NewWorkItem 範例建立工作
description: 建立工作時，您將會使用兩個工作排程器介面 ITaskScheduler 和 ITask。
ms.assetid: 1cbdba6a-e017-4f00-87cb-970686a69e0a
keywords:
- 工作排程器建立工作專案
- 工作專案工作排程器，建立工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4e0f05e76ea54b57a101e31515fe089c5f445c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315820"
---
# <a name="creating-a-task-using-newworkitem-example"></a><span data-ttu-id="795fe-105">使用 NewWorkItem 範例建立工作</span><span class="sxs-lookup"><span data-stu-id="795fe-105">Creating a Task Using NewWorkItem Example</span></span>

<span data-ttu-id="795fe-106">建立工作時，您將使用兩個工作排程器介面： [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) 和 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)。</span><span class="sxs-lookup"><span data-stu-id="795fe-106">When creating a task, you will use two Task Scheduler interfaces: [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) and [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span></span> <span data-ttu-id="795fe-107">您必須為工作提供唯一的名稱、工作物件的類別識別碼，以及 **ITask** 的介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="795fe-107">You must provide a unique name for the task, the class identifier of the task object, and the interface identifier of **ITask**.</span></span> <span data-ttu-id="795fe-108">本主題後面的程式碼範例會顯示類別識別碼和介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="795fe-108">The class identifier and interface identifier are shown in the code example following this topic.</span></span>

> [!Note]  
> <span data-ttu-id="795fe-109">您也可以藉由呼叫 [**ITaskScheduler：： azuretasks**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem)來建立工作。</span><span class="sxs-lookup"><span data-stu-id="795fe-109">You can also create a task by calling [**ITaskScheduler::AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem).</span></span> <span data-ttu-id="795fe-110">當您採用此路由時，您必須負責建立 **(的工作物件實例** ，以支援 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面) 然後使用您提供的名稱來新增工作。</span><span class="sxs-lookup"><span data-stu-id="795fe-110">When you take this route, it is your responsibility to create an instance of the **Task** object (which supports the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface) and then add the task with the name you supply.</span></span>

 

> [!Note]  
> <span data-ttu-id="795fe-111">依預設，只有 Administrators、Backup Operators 或 Server Operators 群組的成員可以在 Windows Server 2003 上建立工作。</span><span class="sxs-lookup"><span data-stu-id="795fe-111">By default, only a member of the Administrators, Backup Operators, or Server Operators group can create tasks on Windows Server 2003.</span></span> <span data-ttu-id="795fe-112">Administrators 群組的成員可以變更 Windows 工作資料夾的安全描述項， \\ 讓其他人可以建立工作。</span><span class="sxs-lookup"><span data-stu-id="795fe-112">A member of the Administrators group may change the security descriptor of the Windows\\Task folder to let others create tasks.</span></span>

 

<span data-ttu-id="795fe-113">您為工作提供的名稱在 [排程工作] 資料夾中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="795fe-113">The name you supply for the task must be unique within the Scheduled Tasks folder.</span></span> <span data-ttu-id="795fe-114">如果已經存在具有相同名稱的工作， [**ITaskScheduler：： NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) 會傳回錯誤 \_ 檔案 \_ 。</span><span class="sxs-lookup"><span data-stu-id="795fe-114">If a task with the same name already exists, [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) returns ERROR\_FILE\_EXISTS.</span></span> <span data-ttu-id="795fe-115">如果您收到此傳回值，您應該指定不同的名稱，然後再次嘗試建立工作。</span><span class="sxs-lookup"><span data-stu-id="795fe-115">If you get this return value, you should specify a different name and attempt to create the task again.</span></span>

<span data-ttu-id="795fe-116">下列程式描述如何建立新的工作專案工作。</span><span class="sxs-lookup"><span data-stu-id="795fe-116">The following procedure describes how to create a new work item task.</span></span>

<span data-ttu-id="795fe-117">**若要建立新的工作專案工作**</span><span class="sxs-lookup"><span data-stu-id="795fe-117">**To create a new work item task**</span></span>

1.  <span data-ttu-id="795fe-118">呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得工作排程器物件。</span><span class="sxs-lookup"><span data-stu-id="795fe-118">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="795fe-119"> (此範例假設工作排程器服務正在執行。 ) </span><span class="sxs-lookup"><span data-stu-id="795fe-119">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="795fe-120">呼叫 [**ITaskScheduler：： NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) 來建立新的工作。</span><span class="sxs-lookup"><span data-stu-id="795fe-120">Call [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) to create a new task.</span></span> <span data-ttu-id="795fe-121"> (這個方法會傳回 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面的指標。 ) </span><span class="sxs-lookup"><span data-stu-id="795fe-121">(This method returns a pointer to an [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.)</span></span>
3.  <span data-ttu-id="795fe-122">藉由呼叫 [**IPersistFile：： save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save)，將新的工作儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="795fe-122">Save the new task to disk by calling [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="795fe-123">[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)介面 (是 **ITask** 介面所支援的標準 COM 介面。 ) </span><span class="sxs-lookup"><span data-stu-id="795fe-123">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface supported by the **ITask** interface.)</span></span>
4.  <span data-ttu-id="795fe-124">呼叫 **ITask：： release** 以釋放所有資源。</span><span class="sxs-lookup"><span data-stu-id="795fe-124">Call **ITask::Release** to release all resources.</span></span> <span data-ttu-id="795fe-125"> (請注意，[**版本**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)是 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)所繼承的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)方法 ) </span><span class="sxs-lookup"><span data-stu-id="795fe-125">(Note that [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="795fe-126">如需的程式碼範例</span><span class="sxs-lookup"><span data-stu-id="795fe-126">For a code example of</span></span>  | <span data-ttu-id="795fe-127">請參閱</span><span class="sxs-lookup"><span data-stu-id="795fe-127">See</span></span>                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="795fe-128">建立單一工作</span><span class="sxs-lookup"><span data-stu-id="795fe-128">Creating a single task</span></span> | [<span data-ttu-id="795fe-129">C/c + + 程式碼範例：使用 NewWorkItem 建立工作</span><span class="sxs-lookup"><span data-stu-id="795fe-129">C/C++ Code Example: Creating a Task Using NewWorkItem</span></span>](c-c-code-example-creating-a-task-using-newworkitem.md) |



 

## <a name="related-topics"></a><span data-ttu-id="795fe-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="795fe-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="795fe-131">工作排程器1.0 範例</span><span class="sxs-lookup"><span data-stu-id="795fe-131">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 