---
title: 適用于開發人員的工作排程器
description: 此工作排程器可讓您在選擇的電腦上自動執行例行工作。 工作排程器藉由監視您所選擇的任何準則 (稱為「觸發程式」) 然後在符合這些準則時執行這些工作。
ms.assetid: 15970a51-c139-48b8-b82b-605728d0f386
keywords:
- 適用于開發人員的工作排程器
- 適用于開發的工作排程器
- 使用工作排程器開發
- 工作排程器，入口網站頁面
ms.topic: article
ms.date: 10/18/2019
ms.openlocfilehash: dfbfb76145e38003e7c501b98c817f4aaca3ff09
ms.sourcegitcommit: 087843ef08ddcd8bce9ed647b610035925da2b3e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/19/2019
ms.locfileid: "104092325"
---
# <a name="task-scheduler-for-developers"></a><span data-ttu-id="a0d73-108">適用于開發人員的工作排程器</span><span class="sxs-lookup"><span data-stu-id="a0d73-108">Task Scheduler for developers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a0d73-109">本主題和本節中的其他主題適用于開發人員物件。</span><span class="sxs-lookup"><span data-stu-id="a0d73-109">This topic and the other topics in this section are for a developer audience.</span></span> <span data-ttu-id="a0d73-110">如果您想要以系統管理員或 IT 專業人員的容量使用工作排程器元件，請參閱 [工作排程器](/dynamics365/business-central/dev-itpro/developer/devenv-task-scheduler)。</span><span class="sxs-lookup"><span data-stu-id="a0d73-110">If you're wishing to use the the Task Scheduler component in your capacity as an administrator, or an IT Professional, then see [Task Scheduler](/dynamics365/business-central/dev-itpro/developer/devenv-task-scheduler).</span></span>

## <a name="about-the-task-scheduler"></a><span data-ttu-id="a0d73-111">關於工作排程器</span><span class="sxs-lookup"><span data-stu-id="a0d73-111">About the Task Scheduler</span></span>

<span data-ttu-id="a0d73-112">此工作排程器可讓您在選擇的電腦上自動執行例行工作。</span><span class="sxs-lookup"><span data-stu-id="a0d73-112">The Task Scheduler enables you to automatically perform routine tasks on a chosen computer.</span></span> <span data-ttu-id="a0d73-113">工作排程器藉由監視您所選擇的任何準則 (稱為「觸發程式」) 然後在符合這些準則時執行這些工作。</span><span class="sxs-lookup"><span data-stu-id="a0d73-113">Task Scheduler does this by monitoring whatever criteria you choose (referred to as triggers) and then executing the tasks when those criteria are met.</span></span>

<span data-ttu-id="a0d73-114">您可以使用工作排程器來執行工作，例如啟動應用程式、傳送電子郵件訊息，或顯示訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="a0d73-114">You can use the Task Scheduler to execute tasks such as starting an application, sending an email message, or showing a message box.</span></span> <span data-ttu-id="a0d73-115">您可以排程工作來執行，以回應這些事件或觸發程式。</span><span class="sxs-lookup"><span data-stu-id="a0d73-115">Tasks can be scheduled to execute in response to these events, or triggers.</span></span> 

- <span data-ttu-id="a0d73-116">當發生特定的系統事件時。</span><span class="sxs-lookup"><span data-stu-id="a0d73-116">When a specific system event occurs.</span></span>
- <span data-ttu-id="a0d73-117">在特定時間。</span><span class="sxs-lookup"><span data-stu-id="a0d73-117">At a specific time.</span></span>
- <span data-ttu-id="a0d73-118">在每日排程的特定時間。</span><span class="sxs-lookup"><span data-stu-id="a0d73-118">At a specific time on a daily schedule.</span></span>
- <span data-ttu-id="a0d73-119">在每週排程的特定時間。</span><span class="sxs-lookup"><span data-stu-id="a0d73-119">At a specific time on a weekly schedule.</span></span>
- <span data-ttu-id="a0d73-120">每月排程的特定時間。</span><span class="sxs-lookup"><span data-stu-id="a0d73-120">At a specific time on a monthly schedule.</span></span>
- <span data-ttu-id="a0d73-121">在每一周的特定時間排程。</span><span class="sxs-lookup"><span data-stu-id="a0d73-121">At a specific time on a monthly day-of-week schedule.</span></span>
- <span data-ttu-id="a0d73-122">當電腦進入閒置狀態時。</span><span class="sxs-lookup"><span data-stu-id="a0d73-122">When the computer enters an idle state.</span></span>
- <span data-ttu-id="a0d73-123">當工作已註冊時。</span><span class="sxs-lookup"><span data-stu-id="a0d73-123">When the task is registered.</span></span>
- <span data-ttu-id="a0d73-124">系統啟動時。</span><span class="sxs-lookup"><span data-stu-id="a0d73-124">When the system is booted.</span></span>
- <span data-ttu-id="a0d73-125">當使用者登入時。</span><span class="sxs-lookup"><span data-stu-id="a0d73-125">When a user logs on.</span></span>
- <span data-ttu-id="a0d73-126">當終端機伺服器會話變更狀態時。</span><span class="sxs-lookup"><span data-stu-id="a0d73-126">When a Terminal Server session changes state.</span></span>

## <a name="developers"></a><span data-ttu-id="a0d73-127">開發人員</span><span class="sxs-lookup"><span data-stu-id="a0d73-127">Developers</span></span>

<span data-ttu-id="a0d73-128">工作排程器提供這些形式的 Api。</span><span class="sxs-lookup"><span data-stu-id="a0d73-128">The Task Scheduler provides APIs in these forms.</span></span>

- <span data-ttu-id="a0d73-129">工作排程器2.0：針對 c + + 和腳本開發分別提供介面和物件。</span><span class="sxs-lookup"><span data-stu-id="a0d73-129">Task Scheduler 2.0: interfaces and objects are provided for C++, and for scripting development, respectively.</span></span>
- <span data-ttu-id="a0d73-130">工作排程器1.0：提供 c + + 開發的介面。</span><span class="sxs-lookup"><span data-stu-id="a0d73-130">Task Scheduler 1.0: interfaces are provided for C++ development.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="a0d73-131">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="a0d73-131">Run-time requirements</span></span>

<span data-ttu-id="a0d73-132">工作排程器需要下列作業系統。</span><span class="sxs-lookup"><span data-stu-id="a0d73-132">The Task Scheduler requires the following operating systems.</span></span>

- <span data-ttu-id="a0d73-133">工作排程器2.0：用戶端需要 Windows Vista 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="a0d73-133">Task Scheduler 2.0: Client requires Windows Vista, or above.</span></span> <span data-ttu-id="a0d73-134">伺服器需要 Windows Server 2008 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="a0d73-134">Server requires Windows Server 2008, or above.</span></span>
- <span data-ttu-id="a0d73-135">工作排程器1.0：用戶端需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="a0d73-135">Task Scheduler 1.0: Client requires Windows Vista, or Windows XP.</span></span> <span data-ttu-id="a0d73-136">伺服器需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="a0d73-136">Server requires Windows Server 2008, or Windows Server 2003.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a0d73-137">本節內容</span><span class="sxs-lookup"><span data-stu-id="a0d73-137">In this section</span></span>

| <span data-ttu-id="a0d73-138">主題</span><span class="sxs-lookup"><span data-stu-id="a0d73-138">Topic</span></span> | <span data-ttu-id="a0d73-139">描述</span><span class="sxs-lookup"><span data-stu-id="a0d73-139">Description</span></span> |
|-|-|
| [<span data-ttu-id="a0d73-140">工作排程器的新功能</span><span class="sxs-lookup"><span data-stu-id="a0d73-140">What's new in Task Scheduler</span></span>](what-s-new-in-task-scheduler.md) | <span data-ttu-id="a0d73-141">工作排程器所引進之新功能的摘要。</span><span class="sxs-lookup"><span data-stu-id="a0d73-141">Summary of new functionality introduced by the Task Scheduler.</span></span> |
| [<span data-ttu-id="a0d73-142">關於工作排程器</span><span class="sxs-lookup"><span data-stu-id="a0d73-142">About the Task Scheduler</span></span>](about-the-task-scheduler.md) | <span data-ttu-id="a0d73-143">工作排程器 API 的一般概念資訊。</span><span class="sxs-lookup"><span data-stu-id="a0d73-143">General conceptual information about the Task Scheduler API.</span></span> |
| [<span data-ttu-id="a0d73-144">使用工作排程器</span><span class="sxs-lookup"><span data-stu-id="a0d73-144">Using the Task Scheduler</span></span>](using-the-task-scheduler.md) | <span data-ttu-id="a0d73-145">示範如何使用工作排程器 Api 的程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="a0d73-145">Code examples that show how to use the Task Scheduler APIs.</span></span> |
| [<span data-ttu-id="a0d73-146">工作排程器參考</span><span class="sxs-lookup"><span data-stu-id="a0d73-146">Task Scheduler reference</span></span>](task-scheduler-reference.md) | <span data-ttu-id="a0d73-147">工作排程器 Api 和工作排程器架構的詳細參考資訊。</span><span class="sxs-lookup"><span data-stu-id="a0d73-147">Detailed reference information for Task Scheduler APIs and the Task Scheduler schema.</span></span> |