---
title: 在特定時間啟動可執行檔
description: 撰寫可在特定時間啟動可執行檔的工作，是藉由定義時間觸發程式和可執行檔動作來完成。
ms.assetid: a45a403d-5a54-4648-b517-41e01a0745c9
keywords:
- 工作排程器範例工作排程器、時間觸發程式
- 工作排程器範例工作排程器，啟動可執行檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c0ce5a1be1586e12399f1dd5d6969170bffa92f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840384"
---
# <a name="starting-an-executable-at-a-specific-time"></a><span data-ttu-id="14729-105">在特定時間啟動可執行檔</span><span class="sxs-lookup"><span data-stu-id="14729-105">Starting an Executable at a Specific Time</span></span>

<span data-ttu-id="14729-106">撰寫可在特定時間啟動可執行檔的工作，是藉由定義時間觸發程式和可執行檔動作來完成。</span><span class="sxs-lookup"><span data-stu-id="14729-106">Writing a task that starts an executable at a specific time is done by defining a time trigger and an executable action.</span></span>

## <a name="start-boundary"></a><span data-ttu-id="14729-107">開始界限</span><span class="sxs-lookup"><span data-stu-id="14729-107">Start Boundary</span></span>

<span data-ttu-id="14729-108">請務必注意，時間觸發程式與其他以時間為基礎的觸發程式不同，因為觸發程式是由其開始界限啟動時所引發。</span><span class="sxs-lookup"><span data-stu-id="14729-108">It is important to note that a time trigger is different from other time-based triggers in that it is fired when the trigger is activated by its start boundary.</span></span> <span data-ttu-id="14729-109">其他以時間為基礎的觸發程式是由其開始界限啟動，但是它們不會開始執行其動作 (在此案例中，啟動可執行檔) ，直到達到排程的日期為止。</span><span class="sxs-lookup"><span data-stu-id="14729-109">Other time-based triggers are activated by their start boundary, but they do not start performing their actions (in this case starting an executable) until a scheduled date is reached.</span></span>

## <a name="time-trigger-examples"></a><span data-ttu-id="14729-110">時間觸發程式範例</span><span class="sxs-lookup"><span data-stu-id="14729-110">Time Trigger Examples</span></span>

<span data-ttu-id="14729-111">下列範例會在工作啟動後的30秒內啟動「記事本」：</span><span class="sxs-lookup"><span data-stu-id="14729-111">The following examples start Notepad 30 seconds after the task is activated:</span></span>

-   [<span data-ttu-id="14729-112">時間觸發程式範例 (c + +) </span><span class="sxs-lookup"><span data-stu-id="14729-112">Time Trigger Example (C++)</span></span>](time-trigger-example--c---.md)
-   [<span data-ttu-id="14729-113">腳本)  (時間觸發程式範例 </span><span class="sxs-lookup"><span data-stu-id="14729-113">Time Trigger Example (Scripting)</span></span>](time-trigger-example--scripting-.md)
-   [<span data-ttu-id="14729-114"> (XML) 的時間觸發程式範例 </span><span class="sxs-lookup"><span data-stu-id="14729-114">Time Trigger Example (XML)</span></span>](time-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="14729-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="14729-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14729-116">使用工作排程器</span><span class="sxs-lookup"><span data-stu-id="14729-116">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




