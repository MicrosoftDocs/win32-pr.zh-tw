---
title: 列舉工作和顯示工作資訊
description: 若要顯示工作的相關資訊，例如工作名稱、狀態或工作的最後一次執行，則可透過列舉工作資料夾中的執行中工作或工作，並顯示所需的資訊來完成。
ms.assetid: a0305089-89ff-42b7-b3f1-99a6484d2e5e
keywords:
- 列舉工作工作排程器
- 工作排程器範例工作排程器，列舉工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e4c1bbad0a1fa8892e38a001ff54e665f0c144
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671052"
---
# <a name="enumerating-tasks-and-displaying-task-information"></a><span data-ttu-id="cade9-105">列舉工作和顯示工作資訊</span><span class="sxs-lookup"><span data-stu-id="cade9-105">Enumerating Tasks and Displaying Task Information</span></span>

<span data-ttu-id="cade9-106">若要顯示工作的相關資訊，例如工作名稱、狀態或工作的最後一次執行，則可透過列舉工作資料夾中的執行中工作或工作，並顯示所需的資訊來完成。</span><span class="sxs-lookup"><span data-stu-id="cade9-106">Displaying information about a task, such as the task name, state, or the last time the task was run, is done by enumerating through running tasks or the tasks in a task folder and displaying the desired information.</span></span>

## <a name="accessing-properties-of-registered-tasks"></a><span data-ttu-id="cade9-107">存取已註冊工作的屬性</span><span class="sxs-lookup"><span data-stu-id="cade9-107">Accessing Properties of Registered Tasks</span></span>

<span data-ttu-id="cade9-108">若要顯示已註冊工作的屬性值，您必須連接到工作排程器服務，然後取得工作資料夾的實例，其中包含您想要取得相關資訊的工作。</span><span class="sxs-lookup"><span data-stu-id="cade9-108">To display a registered task's property value, you must connect to the Task Scheduler service, and then get an instance of the task folder that contains the tasks you want information about.</span></span> <span data-ttu-id="cade9-109">然後，您可以在工作資料夾中取得所有已註冊工作的集合。</span><span class="sxs-lookup"><span data-stu-id="cade9-109">You then get a collection of all the registered tasks in the task folder.</span></span> <span data-ttu-id="cade9-110">然後，您會列舉每個已註冊的工作，並取得並顯示每個工作的屬性值。</span><span class="sxs-lookup"><span data-stu-id="cade9-110">Then you enumerate through each registered task and get and display a property value for each task.</span></span>

## <a name="accessing-properties-of-running-tasks"></a><span data-ttu-id="cade9-111">存取執行中工作的屬性</span><span class="sxs-lookup"><span data-stu-id="cade9-111">Accessing Properties of Running Tasks</span></span>

<span data-ttu-id="cade9-112">若要顯示執行中工作的屬性值，您必須連接到工作排程器服務，然後取得所有執行中工作的集合 (包括或排除隱藏的工作) 。</span><span class="sxs-lookup"><span data-stu-id="cade9-112">To display a running task's property value, you must connect to the Task Scheduler service, and then get a collection of all the running tasks (including or excluding hidden tasks).</span></span> <span data-ttu-id="cade9-113">然後，您會列舉每個執行中的工作，並取得並顯示每個工作的屬性值。</span><span class="sxs-lookup"><span data-stu-id="cade9-113">Then you enumerate through each running task and get and display a property value for each task.</span></span>

## <a name="example"></a><span data-ttu-id="cade9-114">範例</span><span class="sxs-lookup"><span data-stu-id="cade9-114">Example</span></span>

<span data-ttu-id="cade9-115">下列範例會列舉工作並顯示工作的名稱和狀態：</span><span class="sxs-lookup"><span data-stu-id="cade9-115">The following examples enumerate tasks and display the name and state of the tasks:</span></span>

-   [<span data-ttu-id="cade9-116">顯示工作名稱和狀態 (腳本) </span><span class="sxs-lookup"><span data-stu-id="cade9-116">Displaying Task Names and States (Scripting)</span></span>](displaying-task-names-and-state--scripting-.md)
-   [<span data-ttu-id="cade9-117">顯示工作名稱和狀態 (c + +) </span><span class="sxs-lookup"><span data-stu-id="cade9-117">Displaying Task Names and State (C++)</span></span>](displaying-task-names-and-state--c---.md)

## <a name="related-topics"></a><span data-ttu-id="cade9-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="cade9-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cade9-119">使用工作排程器</span><span class="sxs-lookup"><span data-stu-id="cade9-119">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




