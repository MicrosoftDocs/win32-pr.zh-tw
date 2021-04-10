---
title: 在工作註冊時啟動可執行檔
description: 在註冊工作時，撰寫啟動可執行檔的工作是藉由定義註冊觸發程式和可執行檔動作來完成。
ms.assetid: 426fa79d-7f0d-42fb-a8c4-15981d13be71
keywords:
- 工作排程器範例工作排程器、註冊觸發程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8036b8bdff807ded582279e0ba7675bc2160811
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932327"
---
# <a name="starting-an-executable-when-a-task-is-registered"></a><span data-ttu-id="78b59-104">在工作註冊時啟動可執行檔</span><span class="sxs-lookup"><span data-stu-id="78b59-104">Starting an Executable When a Task is Registered</span></span>

<span data-ttu-id="78b59-105">在註冊工作時，撰寫啟動可執行檔的工作是藉由定義註冊觸發程式和可執行檔動作來完成。</span><span class="sxs-lookup"><span data-stu-id="78b59-105">Writing a task that starts an executable when a task is registered is done by defining a registration trigger and an executable action.</span></span>

## <a name="registration-trigger"></a><span data-ttu-id="78b59-106">註冊觸發程式</span><span class="sxs-lookup"><span data-stu-id="78b59-106">Registration Trigger</span></span>

<span data-ttu-id="78b59-107">註冊觸發程式會在註冊後立即啟動工作。</span><span class="sxs-lookup"><span data-stu-id="78b59-107">Registration triggers start a task as soon as it is registered.</span></span> <span data-ttu-id="78b59-108">您也可以指定註冊觸發程式的延遲，這會在一段特定時間之後啟動工作， (在註冊工作之後的延遲) 。</span><span class="sxs-lookup"><span data-stu-id="78b59-108">You can also specify a delay for the registration trigger, which starts a task after a specific amount of time (the delay) after the task is registered.</span></span> <span data-ttu-id="78b59-109">延遲是在 [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger)介面的 [**delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay)屬性中指定， ([**RegistrationTrigger**](registrationtrigger.md)腳本) 。</span><span class="sxs-lookup"><span data-stu-id="78b59-109">The delay is specified in the [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) property of the [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) interface ([**RegistrationTrigger**](registrationtrigger.md) for scripting).</span></span>

> [!Note]  
> <span data-ttu-id="78b59-110">更新註冊觸發程式的工作時，工作會在更新發生之後執行。</span><span class="sxs-lookup"><span data-stu-id="78b59-110">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 

## <a name="registration-trigger-examples"></a><span data-ttu-id="78b59-111">註冊觸發程式範例</span><span class="sxs-lookup"><span data-stu-id="78b59-111">Registration Trigger Examples</span></span>

<span data-ttu-id="78b59-112">下列範例會在工作註冊時啟動「記事本」：</span><span class="sxs-lookup"><span data-stu-id="78b59-112">The following examples start Notepad when a task is registered:</span></span>

-   [<span data-ttu-id="78b59-113"> (腳本) 的註冊觸發程式範例 </span><span class="sxs-lookup"><span data-stu-id="78b59-113">Registration Trigger Example (Scripting)</span></span>](registration-trigger-example--scripting-.md)
-   [<span data-ttu-id="78b59-114"> (c + +) 的註冊觸發程式範例 </span><span class="sxs-lookup"><span data-stu-id="78b59-114">Registration Trigger Example (C++)</span></span>](registration-trigger-example--c---.md)
-   [<span data-ttu-id="78b59-115"> (XML) 的註冊觸發程式範例 </span><span class="sxs-lookup"><span data-stu-id="78b59-115">Registration Trigger Example (XML)</span></span>](registration-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="78b59-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="78b59-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78b59-117">使用工作排程器</span><span class="sxs-lookup"><span data-stu-id="78b59-117">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




