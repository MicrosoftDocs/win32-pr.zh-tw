---
title: 在系統開機時啟動可執行檔
description: 藉由定義開機觸發程式和可執行檔動作，來撰寫在系統啟動時啟動可執行檔的工作。
ms.assetid: 9e2359df-a223-4a0c-9051-01b73a83c1f7
keywords:
- 工作排程器範例工作排程器、開機觸發程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d41c39e9c80d3fc8f14c0bc9b9d9305de38e16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674584"
---
# <a name="starting-an-executable-on-system-boot"></a><span data-ttu-id="8ed71-104">在系統開機時啟動可執行檔</span><span class="sxs-lookup"><span data-stu-id="8ed71-104">Starting an Executable on System Boot</span></span>

<span data-ttu-id="8ed71-105">藉由定義開機觸發程式和可執行檔動作，來撰寫在系統啟動時啟動可執行檔的工作。</span><span class="sxs-lookup"><span data-stu-id="8ed71-105">Writing a task that starts an executable when a system is booted is done by defining a boot trigger and an executable action.</span></span>

## <a name="boot-trigger"></a><span data-ttu-id="8ed71-106">開機觸發程式</span><span class="sxs-lookup"><span data-stu-id="8ed71-106">Boot Trigger</span></span>

<span data-ttu-id="8ed71-107">開機觸發程式是由其開始界限啟動，但是在系統開機之前，它們不會啟動可執行檔。</span><span class="sxs-lookup"><span data-stu-id="8ed71-107">Boot triggers are activated by their start boundary but they do not start the executable until the system is booted.</span></span> <span data-ttu-id="8ed71-108">您也可以在開機觸發程式中指定延遲時間，以指定系統開機和啟動工作之間的時間長度。</span><span class="sxs-lookup"><span data-stu-id="8ed71-108">You can also specify a delay time in the boot trigger that specifies the amount of time between when the system is booted and when the task is started.</span></span> <span data-ttu-id="8ed71-109">這是由 [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger)介面中的 [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay)屬性所定義， ([**BootTrigger**](boottrigger.md)物件來撰寫腳本) 。</span><span class="sxs-lookup"><span data-stu-id="8ed71-109">This is defined by the [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) property in the [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) interface ([**BootTrigger**](boottrigger.md) object for scripting).</span></span>

## <a name="boot-trigger-examples"></a><span data-ttu-id="8ed71-110">開機觸發程式範例</span><span class="sxs-lookup"><span data-stu-id="8ed71-110">Boot Trigger Examples</span></span>

<span data-ttu-id="8ed71-111">下列範例會在系統開機之後啟動「記事本」：</span><span class="sxs-lookup"><span data-stu-id="8ed71-111">The following examples start Notepad after the system is booted:</span></span>

-   [<span data-ttu-id="8ed71-112"> (腳本) 的開機觸發程式範例 </span><span class="sxs-lookup"><span data-stu-id="8ed71-112">Boot Trigger Example (Scripting)</span></span>](boot-trigger-example--scripting-.md)
-   [<span data-ttu-id="8ed71-113"> (c + +) 的開機觸發程式範例 </span><span class="sxs-lookup"><span data-stu-id="8ed71-113">Boot Trigger Example (C++)</span></span>](boot-trigger-example--c---.md)
-   [<span data-ttu-id="8ed71-114"> (XML) 的開機觸發程式範例 </span><span class="sxs-lookup"><span data-stu-id="8ed71-114">Boot Trigger Example (XML)</span></span>](boot-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="8ed71-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="8ed71-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ed71-116">使用工作排程器</span><span class="sxs-lookup"><span data-stu-id="8ed71-116">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




