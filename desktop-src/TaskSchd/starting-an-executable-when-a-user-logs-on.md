---
title: 當使用者登入時啟動可執行檔
description: 藉由定義登入觸發程式和可執行檔動作，寫入在使用者登入時啟動可執行檔的工作。
ms.assetid: 0c5912aa-913d-42ce-a01b-b1359b49bb2f
keywords:
- 工作排程器範例工作排程器，登入觸發程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ffa758546dbd08b6ccf27412f38891589cb9643
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371833"
---
# <a name="starting-an-executable-when-a-user-logs-on"></a><span data-ttu-id="9feab-104">當使用者登入時啟動可執行檔</span><span class="sxs-lookup"><span data-stu-id="9feab-104">Starting an Executable When a User Logs On</span></span>

<span data-ttu-id="9feab-105">藉由定義登入觸發程式和可執行檔動作，寫入在使用者登入時啟動可執行檔的工作。</span><span class="sxs-lookup"><span data-stu-id="9feab-105">Writing a task that starts an executable when a user logs on is done by defining a logon trigger and an executable action.</span></span>

## <a name="logon-trigger"></a><span data-ttu-id="9feab-106">登入觸發程式</span><span class="sxs-lookup"><span data-stu-id="9feab-106">Logon Trigger</span></span>

<span data-ttu-id="9feab-107">登入觸發程式是由其開始界限啟動，但在指定的使用者登入之前，不會啟動可執行檔。</span><span class="sxs-lookup"><span data-stu-id="9feab-107">Logon triggers are activated by their start boundary but they do not start the executable until a specified user logs on.</span></span> <span data-ttu-id="9feab-108">您可以指定在特定使用者登入時啟動登入觸發程式，方法是在 [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger)介面的 [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid)屬性中指定使用者， ([**LogonTrigger**](logontrigger.md)腳本) 。</span><span class="sxs-lookup"><span data-stu-id="9feab-108">You can specify the logon trigger to start when a certain user logs on by specifying the user in the [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) property of the [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) interface ([**LogonTrigger**](logontrigger.md) for scripting).</span></span>

## <a name="logontrigger-examples"></a><span data-ttu-id="9feab-109">LogonTrigger 範例</span><span class="sxs-lookup"><span data-stu-id="9feab-109">LogonTrigger Examples</span></span>

<span data-ttu-id="9feab-110">下列範例會在使用者登入之後啟動 [記事本]。</span><span class="sxs-lookup"><span data-stu-id="9feab-110">The following examples start Notepad after a user logs on.</span></span>

-   [<span data-ttu-id="9feab-111">登入觸發程式範例 (腳本) </span><span class="sxs-lookup"><span data-stu-id="9feab-111">Logon Trigger Example (Scripting)</span></span>](logon-trigger-example--scripting-.md)
-   [<span data-ttu-id="9feab-112"> (c + +) 的登入觸發程式範例 </span><span class="sxs-lookup"><span data-stu-id="9feab-112">Logon Trigger Example (C++)</span></span>](logon-trigger-example--c---.md)
-   [<span data-ttu-id="9feab-113"> (XML) 的登入觸發程式範例 </span><span class="sxs-lookup"><span data-stu-id="9feab-113">Logon Trigger Example (XML)</span></span>](logon-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="9feab-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="9feab-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9feab-115">使用工作排程器</span><span class="sxs-lookup"><span data-stu-id="9feab-115">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




