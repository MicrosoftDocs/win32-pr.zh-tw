---
description: 應用程式分成兩個程式。 其中一個程式是以標準使用者身分執行，另一個則以系統管理員許可權執行。
ms.assetid: 1e661915-5797-421d-b96f-72949f441aba
title: 系統管理員訊息代理程式模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299d35c995fb56f969fc5983864cfc93b25b6c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849883"
---
# <a name="administrator-broker-model"></a><span data-ttu-id="494a3-104">系統管理員訊息代理程式模型</span><span class="sxs-lookup"><span data-stu-id="494a3-104">Administrator Broker Model</span></span>

<span data-ttu-id="494a3-105">在系統管理員訊息代理程式模型中，應用程式分成兩個程式。</span><span class="sxs-lookup"><span data-stu-id="494a3-105">In the administrator broker model, the application is divided into two programs.</span></span> <span data-ttu-id="494a3-106">其中一個程式是以標準使用者身分執行，另一個則以系統管理員許可權執行。</span><span class="sxs-lookup"><span data-stu-id="494a3-106">One of the programs runs as a standard user, and the other runs with administrator privilege.</span></span>

<span data-ttu-id="494a3-107">使用應用程式資訊清單，將標準使用者程式標示為 **asInvoker** 的 **並無 requestedexecutionlevel** ，並將系統管理程式標示為並無 requestedexecutionlevel **requireAdministrator**。</span><span class="sxs-lookup"><span data-stu-id="494a3-107">Using an application manifest, mark the standard user program with a **requestedExecutionLevel** of **asInvoker** and mark the administrative program with a **requestedExecutionLevel** of **requireAdministrator**.</span></span> <span data-ttu-id="494a3-108">使用者會先啟動標準使用者程式。</span><span class="sxs-lookup"><span data-stu-id="494a3-108">A user launches the standard user program first.</span></span> <span data-ttu-id="494a3-109">當使用者嘗試執行需要完整系統管理員存取權杖的作業時，標準使用者程式會呼叫 [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) 函數來啟動系統管理程式。</span><span class="sxs-lookup"><span data-stu-id="494a3-109">When the user attempts to perform an operation that requires a full administrator access token, the standard user program calls the [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) function to launch the administrative program.</span></span> <span data-ttu-id="494a3-110">**ShellExecute** 函式會在使用使用者的完整系統管理員存取權杖執行應用程式之前，提示使用者進行核准。</span><span class="sxs-lookup"><span data-stu-id="494a3-110">The **ShellExecute** function prompts the user for approval before running the application with the user's full administrator access token.</span></span> <span data-ttu-id="494a3-111">然後，系統管理程式可以執行需要系統管理員許可權的工作。</span><span class="sxs-lookup"><span data-stu-id="494a3-111">The administrative program can then perform tasks that require administrator privilege.</span></span>

<span data-ttu-id="494a3-112">系統管理程式未完全與標準使用者程式隔離。</span><span class="sxs-lookup"><span data-stu-id="494a3-112">The administrative program is not completely isolated from the standard user program.</span></span> <span data-ttu-id="494a3-113">系統管理程式可以啟用與標準使用者程式之間的處理序間通訊。</span><span class="sxs-lookup"><span data-stu-id="494a3-113">The administrative program can enable interprocess communication with the standard user program.</span></span> <span data-ttu-id="494a3-114">不過，這類通訊會受限於預設的強制完整性原則。</span><span class="sxs-lookup"><span data-stu-id="494a3-114">However, such communication is limited by the default mandatory integrity policy.</span></span> <span data-ttu-id="494a3-115">如需強制完整性考慮的詳細資訊，請參閱將 [應用程式設計成以低完整性層級執行](/previous-versions/dotnet/articles/bb625960(v=msdn.10))。</span><span class="sxs-lookup"><span data-stu-id="494a3-115">For information about mandatory integrity considerations, see [Designing Applications to Run at a Low Integrity Level](/previous-versions/dotnet/articles/bb625960(v=msdn.10)).</span></span>

<span data-ttu-id="494a3-116">以下是系統管理員 broker 模型的可能用途：</span><span class="sxs-lookup"><span data-stu-id="494a3-116">The following are possible uses for the administrator broker model:</span></span>

-   <span data-ttu-id="494a3-117">開發嚮導。</span><span class="sxs-lookup"><span data-stu-id="494a3-117">Developing wizards.</span></span> <span data-ttu-id="494a3-118">當硬體 wizard 判定電腦上未安裝必要的驅動程式，或位於企業的核准位置時，它會呼叫提高許可權的應用程式，並將驅動程式移至電腦存放區。</span><span class="sxs-lookup"><span data-stu-id="494a3-118">When a hardware wizard determines that a required driver is not installed on the computer or located in the enterprise's approved location, it calls an elevated application with the ability to move a driver into the computer store.</span></span>
-   <span data-ttu-id="494a3-119">Autorun.exe 呼叫 Setup.exe。</span><span class="sxs-lookup"><span data-stu-id="494a3-119">Autorun.exe calling Setup.exe.</span></span> <span data-ttu-id="494a3-120">當使用者從 CD 執行軟體時，Autorun.exe 是以標準使用者身分執行，則會啟動以系統管理員身分執行的 Setup.exe，以將軟體安裝在電腦上。</span><span class="sxs-lookup"><span data-stu-id="494a3-120">When a user runs software from a CD, Autorun.exe, which runs as a standard user, starts Setup.exe, which runs as an administrator, to install the software onto the computer.</span></span>

<span data-ttu-id="494a3-121">以下是使用系統管理員訊息代理程式模型的缺點：</span><span class="sxs-lookup"><span data-stu-id="494a3-121">The following are drawbacks to using the administrator broker model:</span></span>

-   <span data-ttu-id="494a3-122">從應用程式到應用程式的轉換可能會對使用者造成混淆。</span><span class="sxs-lookup"><span data-stu-id="494a3-122">The transitions from application to application can be confusing to the user.</span></span> <span data-ttu-id="494a3-123">將新應用程式顯示在監視器上的原因可能很難通知使用者。</span><span class="sxs-lookup"><span data-stu-id="494a3-123">It can be difficult to inform the user why a new application appears on the monitor.</span></span>
-   <span data-ttu-id="494a3-124">可能很難在兩個應用程式之間傳遞狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="494a3-124">It can be difficult to pass state information between the two applications.</span></span> <span data-ttu-id="494a3-125">例如，您不會使用此模型在標準使用者控制台之間傳遞狀態資訊 (CPL) 與其系統管理員對應，只是讓相同的 CPL 具有系統管理和標準使用者功能。</span><span class="sxs-lookup"><span data-stu-id="494a3-125">For example, you would not use this model to pass state information between a standard user control panel (CPL) and its administrator counterpart simply to allow the same CPL to have administrative and standard user functionality.</span></span> <span data-ttu-id="494a3-126">標準使用者 CPL 必須將其狀態儲存在某個位置。</span><span class="sxs-lookup"><span data-stu-id="494a3-126">The standard user CPL would have to store its state somewhere.</span></span>
-   <span data-ttu-id="494a3-127">分割兩個程式之間的功能時，可能會有許多已複寫的程式碼。</span><span class="sxs-lookup"><span data-stu-id="494a3-127">There can be a lot of replicated code when splitting the functionality between two programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="494a3-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="494a3-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="494a3-129">開發需要系統管理員許可權的應用程式</span><span class="sxs-lookup"><span data-stu-id="494a3-129">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="494a3-130">系統管理員 COM 物件模型</span><span class="sxs-lookup"><span data-stu-id="494a3-130">Administrator COM Object Model</span></span>](administrator-com-object-model.md)
</dt> <dt>

[<span data-ttu-id="494a3-131">作業系統服務模型</span><span class="sxs-lookup"><span data-stu-id="494a3-131">Operating System Service Model</span></span>](operating-system-service-model.md)
</dt> <dt>

[<span data-ttu-id="494a3-132">提高許可權的工作模型</span><span class="sxs-lookup"><span data-stu-id="494a3-132">Elevated Task Model</span></span>](elevated-task-model.md)
</dt> </dl>

 

 
