---
title: 操作工作專案
description: IScheduledWorkItem 介面提供了用來取得和設定工作專案屬性的方法; (設定觸發程式時，必須使用 ITaskTrigger SetTrigger 方法) ，來建立、取出和刪除工作專案的觸發程式。以及執行、終止和刪除工作專案。請注意，針對特定工作專案類型的屬性，請參閱該物件類型的介面。 例如，您無法設定工作專案的優先權層級;不過，您可以使用 ITask 介面的方法來取得和設定工作的優先順序。
ms.assetid: 8aedf96d-e43d-4aac-ad8c-860379209f95
keywords:
- 工作排程器的工作專案，管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33680d04da9d34f54085d182ed61edda9e8b232f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682669"
---
# <a name="manipulating-work-items"></a><span data-ttu-id="e7a47-105">操作工作專案</span><span class="sxs-lookup"><span data-stu-id="e7a47-105">Manipulating Work Items</span></span>

<span data-ttu-id="e7a47-106">[**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)介面提供了用來取得和設定工作專案屬性的方法;您必須使用 [**ITaskTrigger：： SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger)方法 (設定觸發程式，才能建立、取出和刪除工作專案的觸發程式) ;以及執行、終止和刪除工作專案。</span><span class="sxs-lookup"><span data-stu-id="e7a47-106">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface provides methods for retrieving and setting work item properties; creating, retrieving, and deleting triggers for work items (setting the trigger must be done with the [**ITaskTrigger::SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) method); and for running, terminating, and deleting the work item.</span></span>

> [!Note]  
> <span data-ttu-id="e7a47-107">針對特定工作專案類型的屬性，請參閱該物件類型的介面。</span><span class="sxs-lookup"><span data-stu-id="e7a47-107">For the properties of a specific type of work item, refer to the interface for that type of object.</span></span> <span data-ttu-id="e7a47-108">例如，您無法設定工作專案的優先權層級;不過，您可以使用 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面的方法來取得和設定工作的優先順序。</span><span class="sxs-lookup"><span data-stu-id="e7a47-108">For example, you cannot set the priority level of a work item; however, you can use the methods of the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface to retrieve and set the priority of a task.</span></span>

 

<span data-ttu-id="e7a47-109">當您修改工作專案時，您必須呼叫 [**IPersistFile：： save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) 物件將修改過的工作專案儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="e7a47-109">Whenever you modify a work item, you must call the [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) object to save the modified work item to disk.</span></span> <span data-ttu-id="e7a47-110">[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)介面是 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)介面所支援的標準 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="e7a47-110">The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface that is supported by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span>

| <span data-ttu-id="e7a47-111">範例</span><span class="sxs-lookup"><span data-stu-id="e7a47-111">For examples of</span></span>                                                            | <span data-ttu-id="e7a47-112">請參閱</span><span class="sxs-lookup"><span data-stu-id="e7a47-112">See</span></span>                                                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e7a47-113">正在抓取適用于所有工作專案類型的屬性</span><span class="sxs-lookup"><span data-stu-id="e7a47-113">Retrieving properties that apply to all types of work items</span></span>                | [<span data-ttu-id="e7a47-114">正在抓取工作專案屬性範例</span><span class="sxs-lookup"><span data-stu-id="e7a47-114">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md) |
| <span data-ttu-id="e7a47-115">設定適用于所有工作專案類型的屬性</span><span class="sxs-lookup"><span data-stu-id="e7a47-115">Setting properties that apply to all types of work items</span></span>                   | [<span data-ttu-id="e7a47-116">設定工作專案屬性範例</span><span class="sxs-lookup"><span data-stu-id="e7a47-116">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)       |
| <span data-ttu-id="e7a47-117">執行已知的工作</span><span class="sxs-lookup"><span data-stu-id="e7a47-117">Running a known task</span></span>                                                       | [<span data-ttu-id="e7a47-118">啟動工作範例</span><span class="sxs-lookup"><span data-stu-id="e7a47-118">Starting a Task Example</span></span>](starting-a-task-example.md)                               |
| <span data-ttu-id="e7a47-119">終止正在執行的工作</span><span class="sxs-lookup"><span data-stu-id="e7a47-119">Terminating a running task</span></span>                                                 | [<span data-ttu-id="e7a47-120">終止工作範例</span><span class="sxs-lookup"><span data-stu-id="e7a47-120">Terminating a Task Example</span></span>](terminating-a-task-example.md)                         |
| <span data-ttu-id="e7a47-121">為已知的工作建立新的觸發程式</span><span class="sxs-lookup"><span data-stu-id="e7a47-121">Creating a new trigger for a known task</span></span>                                    | [<span data-ttu-id="e7a47-122">建立新的觸發程式</span><span class="sxs-lookup"><span data-stu-id="e7a47-122">Creating a New Trigger</span></span>](creating-a-new-trigger.md)                                 |
| <span data-ttu-id="e7a47-123">為已知的工作建立事件型閒置觸發程式</span><span class="sxs-lookup"><span data-stu-id="e7a47-123">Creating an event-based idle trigger for a known task</span></span>                      | [<span data-ttu-id="e7a47-124">建立閒置觸發程式範例</span><span class="sxs-lookup"><span data-stu-id="e7a47-124">Creating an Idle Trigger Example</span></span>](creating-an-idle-trigger-example.md)             |
| <span data-ttu-id="e7a47-125">抓取與已知工作相關聯之所有觸發程式的觸發程式字串</span><span class="sxs-lookup"><span data-stu-id="e7a47-125">Retrieving the trigger string of all triggers associated with a known task</span></span> | [<span data-ttu-id="e7a47-126">正在抓取觸發字串範例</span><span class="sxs-lookup"><span data-stu-id="e7a47-126">Retrieving Trigger Strings Example</span></span>](retrieving-trigger-strings-example.md)         |



 

 

 