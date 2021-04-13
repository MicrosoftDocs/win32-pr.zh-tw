---
title: 每天啟動可執行檔
description: 撰寫每日啟動可執行檔的工作，是藉由定義每日觸發程式和可執行檔動作來完成。
ms.assetid: 3ceea4a6-0052-4831-a3b0-76d84ab4e1ed
keywords:
- 工作排程器範例工作排程器，每日觸發程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebb5b11e1942f342437347f1aa4a510e101c56df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301343"
---
# <a name="starting-an-executable-daily"></a><span data-ttu-id="e09e7-104">每天啟動可執行檔</span><span class="sxs-lookup"><span data-stu-id="e09e7-104">Starting an Executable Daily</span></span>

<span data-ttu-id="e09e7-105">撰寫每日啟動可執行檔的工作，是藉由定義每日觸發程式和可執行檔動作來完成。</span><span class="sxs-lookup"><span data-stu-id="e09e7-105">Writing a task that starts an executable on a daily basis is done by defining a daily trigger and an executable action.</span></span>

## <a name="daily-triggers"></a><span data-ttu-id="e09e7-106">每日觸發程式</span><span class="sxs-lookup"><span data-stu-id="e09e7-106">Daily Triggers</span></span>

<span data-ttu-id="e09e7-107">每日觸發程式會使用其開始界限來啟動觸發程式，並指定執行工作的當日時間。</span><span class="sxs-lookup"><span data-stu-id="e09e7-107">Daily triggers use their start boundary to activate the trigger and to specify the time of day that the task is run.</span></span> <span data-ttu-id="e09e7-108">啟動觸發程式之後，就會使用觸發程式間隔來指出工作每天、每天、每隔三天執行一次。</span><span class="sxs-lookup"><span data-stu-id="e09e7-108">Once the trigger is activated, the triggers interval is used to indicate if the task runs daily, every other day, every third day, or so on.</span></span>

## <a name="daily-trigger-examples"></a><span data-ttu-id="e09e7-109">每日觸發程式範例</span><span class="sxs-lookup"><span data-stu-id="e09e7-109">Daily Trigger Examples</span></span>

<span data-ttu-id="e09e7-110">下列範例示範如何建立每天啟動「記事本」的工作。</span><span class="sxs-lookup"><span data-stu-id="e09e7-110">The following examples show how to create tasks that start Notepad on a daily basis.</span></span>

-   [<span data-ttu-id="e09e7-111"> (腳本) 的每日觸發程式範例 </span><span class="sxs-lookup"><span data-stu-id="e09e7-111">Daily Trigger Example (Scripting)</span></span>](daily-trigger-example--scripting-.md)
-   [<span data-ttu-id="e09e7-112"> (c + +) 的每日觸發程式範例 </span><span class="sxs-lookup"><span data-stu-id="e09e7-112">Daily Trigger Example (C++)</span></span>](daily-trigger-example--c---.md)
-   [<span data-ttu-id="e09e7-113"> (XML) 的每日觸發程式範例 </span><span class="sxs-lookup"><span data-stu-id="e09e7-113">Daily Trigger Example (XML)</span></span>](daily-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="e09e7-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="e09e7-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e09e7-115">使用工作排程器</span><span class="sxs-lookup"><span data-stu-id="e09e7-115">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




