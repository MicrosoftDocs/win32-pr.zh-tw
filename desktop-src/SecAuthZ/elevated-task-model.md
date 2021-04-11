---
description: 以標準使用者身分執行的應用程式會啟動排程工作，以執行需要系統管理員許可權的作業。
ms.assetid: cd7485b3-6be5-4163-9a86-7892dbc59181
title: 提高許可權的工作模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27006e32210cfea05de5c2b3b9adf36613dc4f5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320548"
---
# <a name="elevated-task-model"></a><span data-ttu-id="56434-103">提高許可權的工作模型</span><span class="sxs-lookup"><span data-stu-id="56434-103">Elevated Task Model</span></span>

<span data-ttu-id="56434-104">在提高許可權的工作模型中，以標準使用者身分執行的應用程式會藉由啟動排程工作來執行需要系統管理員許可權的作業。</span><span class="sxs-lookup"><span data-stu-id="56434-104">In the elevated task model, an application running as a standard user performs operations that require administrator privilege by starting a scheduled task.</span></span>

<span data-ttu-id="56434-105">**Windows Server 2003 和 WINDOWS XP：** 不支援提高許可權的工作模型。</span><span class="sxs-lookup"><span data-stu-id="56434-105">**Windows Server 2003 and Windows XP:** The elevated task model is not supported.</span></span>

<span data-ttu-id="56434-106">工作不會耗用許多系統資源做為服務，而工作會在完成時自動關閉。</span><span class="sxs-lookup"><span data-stu-id="56434-106">Tasks do not consume as many system resources as services, and tasks automatically close when finished.</span></span> <span data-ttu-id="56434-107">除非需要與舊版作業系統的回溯相容性，否則請考慮使用此模型，而不是 [作業系統服務模型](operating-system-service-model.md) 。</span><span class="sxs-lookup"><span data-stu-id="56434-107">Consider using this model instead of the [Operating System Service Model](operating-system-service-model.md) unless backward compatibility with earlier operating systems is necessary.</span></span>

<span data-ttu-id="56434-108">若要使用工作來執行標準使用者應用程式的特殊許可權作業，必須符合下列條件：</span><span class="sxs-lookup"><span data-stu-id="56434-108">To use a task to perform privileged operations for a standard user application, the following conditions must be met:</span></span>

-   <span data-ttu-id="56434-109">工作必須設定為以 **系統** 的形式執行。</span><span class="sxs-lookup"><span data-stu-id="56434-109">The task must be set to run as **SYSTEM**.</span></span>
-   <span data-ttu-id="56434-110">與工作相關聯的 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 必須設定為允許標準使用者啟動工作。</span><span class="sxs-lookup"><span data-stu-id="56434-110">The [*security descriptor*](/windows/desktop/SecGloss/s-gly) associated with the task must be configured to allow standard users to start the task.</span></span>
-   <span data-ttu-id="56434-111">工作排程器服務必須正在執行。</span><span class="sxs-lookup"><span data-stu-id="56434-111">The task scheduler service must be running.</span></span>

<span data-ttu-id="56434-112">如需有關如何建立和啟動工作的詳細資訊，請參閱 [工作排程器](/windows/desktop/TaskSchd/task-scheduler-start-page)。</span><span class="sxs-lookup"><span data-stu-id="56434-112">For information about how to create and start tasks, see [Task Scheduler](/windows/desktop/TaskSchd/task-scheduler-start-page).</span></span>

## <a name="related-topics"></a><span data-ttu-id="56434-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="56434-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56434-114">開發需要系統管理員許可權的應用程式</span><span class="sxs-lookup"><span data-stu-id="56434-114">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="56434-115">系統管理員訊息代理程式模型</span><span class="sxs-lookup"><span data-stu-id="56434-115">Administrator Broker Model</span></span>](administrator-broker-model.md)
</dt> <dt>

[<span data-ttu-id="56434-116">系統管理員 COM 物件模型</span><span class="sxs-lookup"><span data-stu-id="56434-116">Administrator COM Object Model</span></span>](administrator-com-object-model.md)
</dt> <dt>

[<span data-ttu-id="56434-117">作業系統服務模型</span><span class="sxs-lookup"><span data-stu-id="56434-117">Operating System Service Model</span></span>](operating-system-service-model.md)
</dt> </dl>

 

 
