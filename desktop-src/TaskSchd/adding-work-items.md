---
title: 加入工作專案
description: 有兩種方式可以將工作專案加入至已排程的 Tasksfolder。 您可以在資料夾內建立新的工作專案，也可以將現有的工作專案加入至資料夾。
ms.assetid: fad5e813-a2e9-40af-97a9-4f92debf1808
keywords:
- 工作排程器的工作專案，加入
- 工作工作排程器，加入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 722f776fd36933995cfd9b5a85612b52dae63f7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968851"
---
# <a name="adding-work-items"></a><span data-ttu-id="1dbfb-106">加入工作專案</span><span class="sxs-lookup"><span data-stu-id="1dbfb-106">Adding Work Items</span></span>

<span data-ttu-id="1dbfb-107">有兩種方式可以將 [*工作專案*](w.md) 加入至已 [*排程的 Tasksfolder*](s.md)。</span><span class="sxs-lookup"><span data-stu-id="1dbfb-107">There are two ways to add [*work items*](w.md) to the [*Scheduled Tasksfolder*](s.md).</span></span> <span data-ttu-id="1dbfb-108">您可以在資料夾內建立新的工作專案，也可以將現有的工作專案加入至資料夾。</span><span class="sxs-lookup"><span data-stu-id="1dbfb-108">You can create a new work item within the folder, or you can add an existing work item to the folder.</span></span>

> [!Note]  
> <span data-ttu-id="1dbfb-109">目前，只有工作物件可以新增至 [排程工作] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="1dbfb-109">Currently, only task objects can be added to the Scheduled Tasks folder.</span></span> <span data-ttu-id="1dbfb-110">新增工作時，您必須知道工作類別的識別碼和工作介面 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)。</span><span class="sxs-lookup"><span data-stu-id="1dbfb-110">When adding a task, you must know the identifiers for the task class and the task interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span></span>

 

<span data-ttu-id="1dbfb-111">您可以藉由呼叫 [**ITaskScheduler：： NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) 方法來建立新的工作專案。</span><span class="sxs-lookup"><span data-stu-id="1dbfb-111">You create new work items by calling the [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) method.</span></span> <span data-ttu-id="1dbfb-112">這個方法會使用您提供的名稱建立新的工作專案物件，並將工作專案加入至 [排程工作] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="1dbfb-112">This method creates a new work item object using the name that you provide and adds the work item to the Scheduled Tasks folder.</span></span> <span data-ttu-id="1dbfb-113">當您建立新的工作專案時，工作排程器會配置新物件所需的記憶體。</span><span class="sxs-lookup"><span data-stu-id="1dbfb-113">When you create a new work item, the Task Scheduler allocates the memory that is required for the new object.</span></span>

<span data-ttu-id="1dbfb-114">若要將現有的工作專案加入至 [排程工作] 資料夾，請呼叫 [**ITaskScheduler：： azuretasks**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) 方法。</span><span class="sxs-lookup"><span data-stu-id="1dbfb-114">To add existing work items to the Scheduled Tasks folder, call the [**ITaskScheduler::AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) method.</span></span> <span data-ttu-id="1dbfb-115">當您呼叫這個方法時，您必須建立物件。</span><span class="sxs-lookup"><span data-stu-id="1dbfb-115">When you call this method, you must create the object.</span></span>

<span data-ttu-id="1dbfb-116">您為工作專案提供的名稱在 [排定的工作] 資料夾中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="1dbfb-116">The names you supply for work items must be unique within the Scheduled Tasks folder.</span></span> <span data-ttu-id="1dbfb-117">當您呼叫 [**ITaskScheduler：： NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) 方法或 [**ITaskScheduler：： azuretasks**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) 方法時，如果已有相同名稱的工作專案，則方法會傳回 **錯誤檔案 \_ \_ 存在** 的錯誤。</span><span class="sxs-lookup"><span data-stu-id="1dbfb-117">If a work item with the same name already exists when you call either the [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) method or the [**ITaskScheduler::AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) method, the method returns an **ERROR\_FILE\_EXISTS** error.</span></span> <span data-ttu-id="1dbfb-118">如需詳細資訊，請參閱 [使用 NewWorkItem 建立工作範例](creating-a-task-using-newworkitem-example.md)。</span><span class="sxs-lookup"><span data-stu-id="1dbfb-118">For more information, see [Creating a Task Using NewWorkItem Example](creating-a-task-using-newworkitem-example.md).</span></span>

 

 




