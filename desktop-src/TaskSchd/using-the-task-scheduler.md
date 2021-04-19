---
title: 使用工作排程器
description: 本節包含的程式碼範例說明如何使用工作排程器 API，以及示範如何在工作排程器架構中定義工作的 XML 範例。
ms.assetid: 6346cbd3-b584-47b4-8313-7830f7fd77b3
keywords:
- 觸發程式工作排程器、範例
- 啟動工作工作排程器
- 建立工作工作排程器
- 工作排程器工作排程器，使用
- 工作排程器範例工作排程器
- 工作排程器工作排程器範例，請參閱工作排程器範例工作排程器
- 範例工作排程器請參閱工作排程器範例工作排程器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f81dda9551917b8f6345248a316bd5941de53f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965964"
---
# <a name="using-the-task-scheduler"></a><span data-ttu-id="9644e-110">使用工作排程器</span><span class="sxs-lookup"><span data-stu-id="9644e-110">Using the Task Scheduler</span></span>

<span data-ttu-id="9644e-111">本節包含的程式碼範例說明如何使用工作排程器 API，以及示範如何在工作排程器架構中定義工作的 XML 範例。</span><span class="sxs-lookup"><span data-stu-id="9644e-111">This section contains code examples that illustrate how the Task Scheduler API is used and XML examples that show how tasks are defined in the Task Scheduler schema.</span></span> <span data-ttu-id="9644e-112">大部分的範例都是獨立程式碼，可以獨立執行，或貼入較大的應用程式，並修改為應用程式的需求。</span><span class="sxs-lookup"><span data-stu-id="9644e-112">Most of these examples are stand-alone code that can be run independently, or pasted into a larger application and modified to the requirements of the application.</span></span>

<span data-ttu-id="9644e-113">下表列出本節中包含工作排程器2.0 範例。</span><span class="sxs-lookup"><span data-stu-id="9644e-113">The following table lists Task Scheduler 2.0 examples included in this section.</span></span>



| <span data-ttu-id="9644e-114">範例</span><span class="sxs-lookup"><span data-stu-id="9644e-114">Example</span></span>                                                                                                    | <span data-ttu-id="9644e-115">描述</span><span class="sxs-lookup"><span data-stu-id="9644e-115">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="9644e-116">在特定時間啟動可執行檔</span><span class="sxs-lookup"><span data-stu-id="9644e-116">Starting an Executable at a Specific Time</span></span>](starting-an-executable-at-a-spcific-time.md)                  | <span data-ttu-id="9644e-117">定義在指定的時間啟動 [記事本] 的工作。</span><span class="sxs-lookup"><span data-stu-id="9644e-117">Defines a task that starts Notepad at a specified time.</span></span>                                |
| [<span data-ttu-id="9644e-118">每天啟動可執行檔</span><span class="sxs-lookup"><span data-stu-id="9644e-118">Starting an Executable Daily</span></span>](starting-an-executable-daily.md)                                           | <span data-ttu-id="9644e-119">定義每天啟動「記事本」的工作。</span><span class="sxs-lookup"><span data-stu-id="9644e-119">Defines a task that starts Notepad daily.</span></span>                                              |
| [<span data-ttu-id="9644e-120">在系統開機時啟動可執行檔</span><span class="sxs-lookup"><span data-stu-id="9644e-120">Starting an Executable on System Boot</span></span>](starting-an-executable-on-system-boot.md)                         | <span data-ttu-id="9644e-121">定義啟動系統時啟動「記事本」的工作。</span><span class="sxs-lookup"><span data-stu-id="9644e-121">Defines a task that starts Notepad when the system is booted.</span></span>                          |
| [<span data-ttu-id="9644e-122">每週啟動可執行檔</span><span class="sxs-lookup"><span data-stu-id="9644e-122">Starting an Executable Weekly</span></span>](starting-an-executable-weekly.md)                                         | <span data-ttu-id="9644e-123">定義每週啟動「記事本」的工作。</span><span class="sxs-lookup"><span data-stu-id="9644e-123">Defines a task that starts Notepad on a weekly basis.</span></span>                                  |
| [<span data-ttu-id="9644e-124">在工作註冊時啟動可執行檔</span><span class="sxs-lookup"><span data-stu-id="9644e-124">Starting an Executable When a Task is Registered</span></span>](starting-an-executable-when-a-task-is-registered.md)   | <span data-ttu-id="9644e-125">定義工作在註冊時啟動 [記事本]。</span><span class="sxs-lookup"><span data-stu-id="9644e-125">Defines a task that starts Notepad when the task is registered.</span></span>                        |
| [<span data-ttu-id="9644e-126">當使用者登入時啟動可執行檔</span><span class="sxs-lookup"><span data-stu-id="9644e-126">Starting an Executable When a User Logs On</span></span>](starting-an-executable-when-a-user-logs-on.md)               | <span data-ttu-id="9644e-127">定義在使用者登入時啟動「記事本」的工作。</span><span class="sxs-lookup"><span data-stu-id="9644e-127">Defines a task that starts Notepad when a user logs on.</span></span>                                |
| [<span data-ttu-id="9644e-128">列舉工作和顯示工作資訊</span><span class="sxs-lookup"><span data-stu-id="9644e-128">Enumerating Tasks and Displaying Task Information</span></span>](enumerating-tasks-and-displaying-task-information.md) | <span data-ttu-id="9644e-129">列舉本機電腦上的所有工作，並顯示每個工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="9644e-129">Enumerates through all the tasks on the local computer and displays each task's state.</span></span> |



 

<span data-ttu-id="9644e-130">下表列出本節中包含工作排程器1.0 範例。</span><span class="sxs-lookup"><span data-stu-id="9644e-130">The following table lists Task Scheduler 1.0 examples included in this section.</span></span> 

| <span data-ttu-id="9644e-131">範例</span><span class="sxs-lookup"><span data-stu-id="9644e-131">Example</span></span>                                                                                    | <span data-ttu-id="9644e-132">描述</span><span class="sxs-lookup"><span data-stu-id="9644e-132">Description</span></span>                                                                                   |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9644e-133">使用 NewWorkItem 範例建立工作</span><span class="sxs-lookup"><span data-stu-id="9644e-133">Creating a Task Using NewWorkItem Example</span></span>](creating-a-task-using-newworkitem-example.md) | <span data-ttu-id="9644e-134">建立新的工作。</span><span class="sxs-lookup"><span data-stu-id="9644e-134">Creates a new task.</span></span>                                                                           |
| [<span data-ttu-id="9644e-135">列舉工作範例</span><span class="sxs-lookup"><span data-stu-id="9644e-135">Enumerating Tasks Example</span></span>](enumerating-tasks-example.md)                                 | <span data-ttu-id="9644e-136">列舉本機電腦上的所有工作。</span><span class="sxs-lookup"><span data-stu-id="9644e-136">Enumerates all the tasks on the local computer.</span></span>                                               |
| [<span data-ttu-id="9644e-137">啟動工作範例</span><span class="sxs-lookup"><span data-stu-id="9644e-137">Starting a Task Example</span></span>](starting-a-task-example.md)                                     | <span data-ttu-id="9644e-138">啟動已知的工作。</span><span class="sxs-lookup"><span data-stu-id="9644e-138">Starts a known task.</span></span>                                                                          |
| [<span data-ttu-id="9644e-139">使用屬性頁編輯工作專案</span><span class="sxs-lookup"><span data-stu-id="9644e-139">Editing a Work Item using Property Pages</span></span>](editing-a-work-item-using-property-pages.md)   | <span data-ttu-id="9644e-140">顯示要編輯之工作的屬性頁。</span><span class="sxs-lookup"><span data-stu-id="9644e-140">Displays the property pages of a task for editing.</span></span>                                            |
| [<span data-ttu-id="9644e-141">正在抓取工作專案屬性範例</span><span class="sxs-lookup"><span data-stu-id="9644e-141">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md)       | <span data-ttu-id="9644e-142">一組範例，示範如何取得套用至所有工作專案類型的屬性。</span><span class="sxs-lookup"><span data-stu-id="9644e-142">A set of examples that show how to retrieve properties that apply to all types of work items.</span></span> |
| [<span data-ttu-id="9644e-143">設定工作專案屬性範例</span><span class="sxs-lookup"><span data-stu-id="9644e-143">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)             | <span data-ttu-id="9644e-144">一組範例，示範如何設定套用至所有工作專案類型的屬性。</span><span class="sxs-lookup"><span data-stu-id="9644e-144">A set of examples that show how to set properties that apply to all types of work items.</span></span>      |
| [<span data-ttu-id="9644e-145">正在抓取工作屬性範例</span><span class="sxs-lookup"><span data-stu-id="9644e-145">Retrieving Task Property Examples</span></span>](retrieving-task-property-examples.md)                 | <span data-ttu-id="9644e-146">一組範例，示範如何抓取工作的唯一屬性。</span><span class="sxs-lookup"><span data-stu-id="9644e-146">A set of examples that show how to retrieve properties unique to tasks.</span></span>                       |
| [<span data-ttu-id="9644e-147">設定工作屬性範例</span><span class="sxs-lookup"><span data-stu-id="9644e-147">Setting Task Property Examples</span></span>](setting-task-property-examples.md)                       | <span data-ttu-id="9644e-148">一組範例，示範如何設定工作的唯一屬性。</span><span class="sxs-lookup"><span data-stu-id="9644e-148">A set of examples that show how to set properties unique to tasks.</span></span>                            |
| [<span data-ttu-id="9644e-149">正在抓取工作頁面範例</span><span class="sxs-lookup"><span data-stu-id="9644e-149">Retrieving a Task Page Example</span></span>](retrieving-a-task-page-example.md)                       | <span data-ttu-id="9644e-150">捕獲並顯示已知工作的一般工作頁面。</span><span class="sxs-lookup"><span data-stu-id="9644e-150">Retrieves and displays the general task page of a known task.</span></span>                                 |
| [<span data-ttu-id="9644e-151">建立新的觸發程式</span><span class="sxs-lookup"><span data-stu-id="9644e-151">Creating a New Trigger</span></span>](creating-a-new-trigger.md)                                       | <span data-ttu-id="9644e-152">為已知的工作建立新的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="9644e-152">Creates a new trigger for a known task.</span></span>                                                       |
| [<span data-ttu-id="9644e-153">建立閒置觸發程式範例</span><span class="sxs-lookup"><span data-stu-id="9644e-153">Creating an Idle Trigger Example</span></span>](creating-an-idle-trigger-example.md)                   | <span data-ttu-id="9644e-154">為已知的工作建立以事件為基礎的閒置觸發程式。</span><span class="sxs-lookup"><span data-stu-id="9644e-154">Creates an event-based idle trigger for a known task.</span></span>                                         |
| [<span data-ttu-id="9644e-155">終止工作範例</span><span class="sxs-lookup"><span data-stu-id="9644e-155">Terminating a Task Example</span></span>](terminating-a-task-example.md)                               | <span data-ttu-id="9644e-156">當工作正在執行時終止。</span><span class="sxs-lookup"><span data-stu-id="9644e-156">Terminates a task while it is running.</span></span>                                                        |
| [<span data-ttu-id="9644e-157">正在抓取觸發字串範例</span><span class="sxs-lookup"><span data-stu-id="9644e-157">Retrieving Trigger Strings Example</span></span>](retrieving-trigger-strings-example.md)               | <span data-ttu-id="9644e-158">抓取與已知工作相關聯之所有觸發程式的觸發程式字串。</span><span class="sxs-lookup"><span data-stu-id="9644e-158">Retrieves the trigger string of all triggers associated with a known task.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="9644e-159">相關主題</span><span class="sxs-lookup"><span data-stu-id="9644e-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9644e-160">工作排程器</span><span class="sxs-lookup"><span data-stu-id="9644e-160">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="9644e-161">關於工作排程器</span><span class="sxs-lookup"><span data-stu-id="9644e-161">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 




