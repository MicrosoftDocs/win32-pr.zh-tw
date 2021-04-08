---
title: 工作排程器1.0 範例
description: 本節中的範例會使用工作排程器1.0 中引進的 API。
ms.assetid: 424d0892-a9c2-4f36-8cb3-5e637641b1e7
keywords:
- 工作排程器範例工作排程器，工作排程器1.0 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746c8c44648359f269d61fd27fc57b1fd90932da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671051"
---
# <a name="task-scheduler-10-examples"></a><span data-ttu-id="5e766-104">工作排程器1.0 範例</span><span class="sxs-lookup"><span data-stu-id="5e766-104">Task Scheduler 1.0 Examples</span></span>

<span data-ttu-id="5e766-105">本節中的範例會使用工作排程器1.0 中引進的 API。</span><span class="sxs-lookup"><span data-stu-id="5e766-105">The examples in this section use the API introduced in Task Scheduler 1.0.</span></span>

> [!Note]  
> <span data-ttu-id="5e766-106">若為 Windows Server 2003、Windows XP 或 Windows 2000 電腦，可在 Windows Vista 電腦上建立、監視或控制工作，則必須在 Windows Vista 電腦上完成某些作業。</span><span class="sxs-lookup"><span data-stu-id="5e766-106">For a Windows Server 2003, Windows XP, or Windows 2000 computer to create, monitor, or control tasks on a Windows Vista computer, certain operations must be completed on the Windows Vista computer.</span></span> <span data-ttu-id="5e766-107">如需詳細資訊，請參閱[工作](tasks.md)。</span><span class="sxs-lookup"><span data-stu-id="5e766-107">For more information, see [Tasks](tasks.md).</span></span>

 

<span data-ttu-id="5e766-108">下列主題提供的範例會示範如何使用工作排程器1.0 中引進的函式。</span><span class="sxs-lookup"><span data-stu-id="5e766-108">The following topics provide examples that show how to use the functions introduced in Task Scheduler 1.0.</span></span>



| <span data-ttu-id="5e766-109">範例</span><span class="sxs-lookup"><span data-stu-id="5e766-109">Example</span></span>                                                                                    | <span data-ttu-id="5e766-110">描述</span><span class="sxs-lookup"><span data-stu-id="5e766-110">Description</span></span>                                                                                   |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e766-111">使用 NewWorkItem 範例建立工作</span><span class="sxs-lookup"><span data-stu-id="5e766-111">Creating a Task Using NewWorkItem Example</span></span>](creating-a-task-using-newworkitem-example.md) | <span data-ttu-id="5e766-112">建立新的工作。</span><span class="sxs-lookup"><span data-stu-id="5e766-112">Creates a new task.</span></span>                                                                           |
| [<span data-ttu-id="5e766-113">列舉工作範例</span><span class="sxs-lookup"><span data-stu-id="5e766-113">Enumerating Tasks Example</span></span>](enumerating-tasks-example.md)                                 | <span data-ttu-id="5e766-114">列舉本機電腦上的所有工作。</span><span class="sxs-lookup"><span data-stu-id="5e766-114">Enumerates all the tasks on the local computer.</span></span>                                               |
| [<span data-ttu-id="5e766-115">啟動工作範例</span><span class="sxs-lookup"><span data-stu-id="5e766-115">Starting a Task Example</span></span>](starting-a-task-example.md)                                     | <span data-ttu-id="5e766-116">啟動已知的工作。</span><span class="sxs-lookup"><span data-stu-id="5e766-116">Starts a known task.</span></span>                                                                          |
| [<span data-ttu-id="5e766-117">使用屬性頁編輯工作專案</span><span class="sxs-lookup"><span data-stu-id="5e766-117">Editing a Work Item using Property Pages</span></span>](editing-a-work-item-using-property-pages.md)   | <span data-ttu-id="5e766-118">顯示要編輯之工作的屬性頁。</span><span class="sxs-lookup"><span data-stu-id="5e766-118">Displays the property pages of a task for editing.</span></span>                                            |
| [<span data-ttu-id="5e766-119">正在抓取工作專案屬性範例</span><span class="sxs-lookup"><span data-stu-id="5e766-119">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md)       | <span data-ttu-id="5e766-120">一組範例，示範如何取得套用至所有工作專案類型的屬性。</span><span class="sxs-lookup"><span data-stu-id="5e766-120">A set of examples that show how to retrieve properties that apply to all types of work items.</span></span> |
| [<span data-ttu-id="5e766-121">設定工作專案屬性範例</span><span class="sxs-lookup"><span data-stu-id="5e766-121">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)             | <span data-ttu-id="5e766-122">一組範例，示範如何設定套用至所有工作專案類型的屬性。</span><span class="sxs-lookup"><span data-stu-id="5e766-122">A set of examples that show how to set properties that apply to all types of work items.</span></span>      |
| [<span data-ttu-id="5e766-123">正在抓取工作屬性範例</span><span class="sxs-lookup"><span data-stu-id="5e766-123">Retrieving Task Property Examples</span></span>](retrieving-task-property-examples.md)                 | <span data-ttu-id="5e766-124">一組範例，示範如何抓取工作的唯一屬性。</span><span class="sxs-lookup"><span data-stu-id="5e766-124">A set of examples that show how to retrieve properties unique to tasks.</span></span>                       |
| [<span data-ttu-id="5e766-125">設定工作屬性範例</span><span class="sxs-lookup"><span data-stu-id="5e766-125">Setting Task Property Examples</span></span>](setting-task-property-examples.md)                       | <span data-ttu-id="5e766-126">一組範例，示範如何設定工作的唯一屬性。</span><span class="sxs-lookup"><span data-stu-id="5e766-126">A set of examples that show how to set properties unique to tasks.</span></span>                            |
| [<span data-ttu-id="5e766-127">正在抓取工作頁面範例</span><span class="sxs-lookup"><span data-stu-id="5e766-127">Retrieving a Task Page Example</span></span>](retrieving-a-task-page-example.md)                       | <span data-ttu-id="5e766-128">捕獲並顯示已知工作的一般工作頁面。</span><span class="sxs-lookup"><span data-stu-id="5e766-128">Retrieves and displays the general task page of a known task.</span></span>                                 |
| [<span data-ttu-id="5e766-129">建立新的觸發程式</span><span class="sxs-lookup"><span data-stu-id="5e766-129">Creating a New Trigger</span></span>](creating-a-new-trigger.md)                                       | <span data-ttu-id="5e766-130">為已知的工作建立新的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="5e766-130">Creates a new trigger for a known task.</span></span>                                                       |
| [<span data-ttu-id="5e766-131">建立閒置觸發程式範例</span><span class="sxs-lookup"><span data-stu-id="5e766-131">Creating an Idle Trigger Example</span></span>](creating-an-idle-trigger-example.md)                   | <span data-ttu-id="5e766-132">為已知的工作建立以事件為基礎的閒置觸發程式。</span><span class="sxs-lookup"><span data-stu-id="5e766-132">Creates an event-based idle trigger for a known task.</span></span>                                         |
| [<span data-ttu-id="5e766-133">正在抓取觸發字串範例</span><span class="sxs-lookup"><span data-stu-id="5e766-133">Retrieving Trigger Strings Example</span></span>](retrieving-trigger-strings-example.md)               | <span data-ttu-id="5e766-134">抓取與已知工作相關聯之所有觸發程式的觸發程式字串。</span><span class="sxs-lookup"><span data-stu-id="5e766-134">Retrieves the trigger string of all triggers associated with a known task.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="5e766-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="5e766-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e766-136">使用工作排程器</span><span class="sxs-lookup"><span data-stu-id="5e766-136">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




