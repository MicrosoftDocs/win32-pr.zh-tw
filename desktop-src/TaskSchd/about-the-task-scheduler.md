---
title: 關於工作排程器
description: 工作排程器服務可讓您在所選電腦上執行自動化工作。
ms.assetid: 13816b8b-3090-4d17-86bb-8e632ca0cd37
keywords:
- 工作排程器工作排程器，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6022546550efe32504dd0a3d12c94163e78214f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965593"
---
# <a name="about-the-task-scheduler"></a><span data-ttu-id="15a5a-104">關於工作排程器</span><span class="sxs-lookup"><span data-stu-id="15a5a-104">About the Task Scheduler</span></span>

<span data-ttu-id="15a5a-105">工作排程器服務可讓您在所選電腦上執行自動化工作。</span><span class="sxs-lookup"><span data-stu-id="15a5a-105">The Task Scheduler service allows you to perform automated tasks on a chosen computer.</span></span> <span data-ttu-id="15a5a-106">使用此服務時，您可以將任何程式排程在方便的時間執行，或是在發生特定事件時執行。</span><span class="sxs-lookup"><span data-stu-id="15a5a-106">With this service, you can schedule any program to run at a convenient time for you or when a specific event occurs.</span></span> <span data-ttu-id="15a5a-107">工作排程器會監視您所選擇的時間或事件準則，然後在符合這些準則時執行工作。</span><span class="sxs-lookup"><span data-stu-id="15a5a-107">The Task Scheduler monitors the time or event criteria that you choose and then executes the task when those criteria are met.</span></span>

## <a name="where-task-scheduler-is-installed"></a><span data-ttu-id="15a5a-108">安裝工作排程器的位置</span><span class="sxs-lookup"><span data-stu-id="15a5a-108">Where Task Scheduler is Installed</span></span>

<span data-ttu-id="15a5a-109">系統會自動安裝數個 Microsoft 作業系統的工作排程器。</span><span class="sxs-lookup"><span data-stu-id="15a5a-109">The Task Scheduler is automatically installed with several Microsoft operating systems.</span></span>

<span data-ttu-id="15a5a-110">工作排程器1.0 安裝于 Windows Server 2003、Windows XP 及 Windows 2000 作業系統中。</span><span class="sxs-lookup"><span data-stu-id="15a5a-110">Task Scheduler 1.0 is installed with the Windows Server 2003, Windows XP, and Windows 2000 operating systems.</span></span>

<span data-ttu-id="15a5a-111">Windows Vista 和 Windows Server 2008 安裝了工作排程器2.0。</span><span class="sxs-lookup"><span data-stu-id="15a5a-111">Task Scheduler 2.0 is installed with Windows Vista and Windows Server 2008.</span></span>

<span data-ttu-id="15a5a-112">工作排程器 2.0 API 應該用於開發在 Windows Vista 上使用工作排程器服務的應用程式。</span><span class="sxs-lookup"><span data-stu-id="15a5a-112">The Task Scheduler 2.0 API should be used in developing applications that use the Task Scheduler service on Windows Vista.</span></span> <span data-ttu-id="15a5a-113">如需詳細資訊，請參閱 [工作排程器參考](task-scheduler-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="15a5a-113">For more information, see [Task Scheduler Reference](task-scheduler-reference.md).</span></span>

<span data-ttu-id="15a5a-114">每次啟動作業系統時，就會啟動工作排程器。</span><span class="sxs-lookup"><span data-stu-id="15a5a-114">Task Scheduler is started each time the operating system is started.</span></span> <span data-ttu-id="15a5a-115">您可以透過工作排程器的圖形化使用者介面 (GUI) 或透過此 SDK 中所述的工作排程器 API 來執行它。</span><span class="sxs-lookup"><span data-stu-id="15a5a-115">It can be run either through the Task Scheduler graphical user interface (GUI) or through the Task Scheduler API described in this SDK.</span></span>

## <a name="information-about-tasks"></a><span data-ttu-id="15a5a-116">工作的相關資訊</span><span class="sxs-lookup"><span data-stu-id="15a5a-116">Information about Tasks</span></span>

<span data-ttu-id="15a5a-117">工作是工作排程器的主要元件。</span><span class="sxs-lookup"><span data-stu-id="15a5a-117">Tasks are the main component of the Task Scheduler.</span></span> <span data-ttu-id="15a5a-118">如需哪些工作及其元件的相關資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="15a5a-118">For information on what tasks are and what their components are, see the following topics:</span></span>

-   [<span data-ttu-id="15a5a-119">工作</span><span class="sxs-lookup"><span data-stu-id="15a5a-119">Tasks</span></span>](tasks.md)
-   [<span data-ttu-id="15a5a-120">工作動作</span><span class="sxs-lookup"><span data-stu-id="15a5a-120">Task Actions</span></span>](task-actions.md)
-   [<span data-ttu-id="15a5a-121">工作觸發程式</span><span class="sxs-lookup"><span data-stu-id="15a5a-121">Task Triggers</span></span>](task-triggers.md)
-   [<span data-ttu-id="15a5a-122">工作註冊資訊</span><span class="sxs-lookup"><span data-stu-id="15a5a-122">Task Registration Information</span></span>](task-registration-information.md)
-   [<span data-ttu-id="15a5a-123">工作閒置條件</span><span class="sxs-lookup"><span data-stu-id="15a5a-123">Task Idle Conditions</span></span>](task-idle-conditions.md)
-   [<span data-ttu-id="15a5a-124">工作的安全性內容</span><span class="sxs-lookup"><span data-stu-id="15a5a-124">Security Contexts for Tasks</span></span>](security-contexts-for-running-tasks.md)
-   [<span data-ttu-id="15a5a-125">重複工作</span><span class="sxs-lookup"><span data-stu-id="15a5a-125">Repeating A Task</span></span>](repeating-a-task.md)
-   [<span data-ttu-id="15a5a-126">自動維護</span><span class="sxs-lookup"><span data-stu-id="15a5a-126">Automatic Maintenance</span></span>](task-maintenence.md)

<span data-ttu-id="15a5a-127">如需有關如何使用工作排程器介面、腳本物件和 XML 的詳細資訊和範例，請參閱 [使用工作排程器](using-the-task-scheduler.md)。</span><span class="sxs-lookup"><span data-stu-id="15a5a-127">For more information and examples about how to use the Task Scheduler interfaces, scripting objects, and XML, see [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="15a5a-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="15a5a-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15a5a-129">工作排程器</span><span class="sxs-lookup"><span data-stu-id="15a5a-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 




