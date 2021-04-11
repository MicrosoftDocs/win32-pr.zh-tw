---
description: 服務程式包含一或多個服務的可執行程式碼。
ms.assetid: 697db543-6149-46ac-add3-c8c6ca3aadbe
title: 服務程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b5e78574f46549956325bc19ffb6d51f4a114ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852071"
---
# <a name="service-programs"></a><span data-ttu-id="41845-103">服務程式</span><span class="sxs-lookup"><span data-stu-id="41845-103">Service Programs</span></span>

<span data-ttu-id="41845-104">*服務程式* 包含一或多個服務的可執行程式碼。</span><span class="sxs-lookup"><span data-stu-id="41845-104">A *service program* contains executable code for one or more services.</span></span> <span data-ttu-id="41845-105">以類型服務 WIN32 本身的進程建立的服務程式 \_ \_ \_ 只包含一項服務的程式碼。</span><span class="sxs-lookup"><span data-stu-id="41845-105">A service program created with the type SERVICE\_WIN32\_OWN\_PROCESS contains the code for only one service.</span></span> <span data-ttu-id="41845-106">以類型服務 \_ WIN32 共用進程建立的服務 \_ 程式 \_ 包含多項服務的程式碼，讓它們可以共用程式碼。</span><span class="sxs-lookup"><span data-stu-id="41845-106">A service program created with the type SERVICE\_WIN32\_SHARE\_PROCESS contains code for more than one service, enabling them to share code.</span></span> <span data-ttu-id="41845-107">執行這項服務程式的其中一個範例，就是裝載內部 Windows 服務的一般服務主機進程 Svchost.exe。</span><span class="sxs-lookup"><span data-stu-id="41845-107">An example of a service program that does this is the generic service host process, Svchost.exe, which hosts internal Windows services.</span></span> <span data-ttu-id="41845-108">請注意，Svchost.exe 是保留給作業系統使用，不應由非 Windows 服務使用。</span><span class="sxs-lookup"><span data-stu-id="41845-108">Note that Svchost.exe is reserved for use by the operating system and should not be used by non-Windows services.</span></span> <span data-ttu-id="41845-109">相反地，開發人員應該執行自己的服務裝載程式。</span><span class="sxs-lookup"><span data-stu-id="41845-109">Instead, developers should implement their own service hosting programs.</span></span>

<span data-ttu-id="41845-110">服務程式可以設定為從內建 (本機) 、主要或受信任網域的使用者帳戶內容中執行。</span><span class="sxs-lookup"><span data-stu-id="41845-110">A service program can be configured to execute in the context of a user account from either the built-in (local), primary, or trusted domain.</span></span> <span data-ttu-id="41845-111">您也可以將它設定為在特殊的 [服務使用者帳戶](service-user-accounts.md)中執行。</span><span class="sxs-lookup"><span data-stu-id="41845-111">It can also be configured to run in a special [service user account](service-user-accounts.md).</span></span>

<span data-ttu-id="41845-112">下列主題描述服務程式必須包含的 [服務控制管理員](service-control-manager.md) (SCM) 的介面需求：</span><span class="sxs-lookup"><span data-stu-id="41845-112">The following topics describe the interface requirements of the [service control manager](service-control-manager.md) (SCM) that a service program must include:</span></span>

-   [<span data-ttu-id="41845-113">服務進入點</span><span class="sxs-lookup"><span data-stu-id="41845-113">Service Entry Point</span></span>](service-entry-point.md)
-   [<span data-ttu-id="41845-114">服務 ServiceMain 函式</span><span class="sxs-lookup"><span data-stu-id="41845-114">Service ServiceMain Function</span></span>](service-servicemain-function.md)
-   [<span data-ttu-id="41845-115">服務控制處理函式</span><span class="sxs-lookup"><span data-stu-id="41845-115">Service Control Handler Function</span></span>](service-control-handler-function.md)

<span data-ttu-id="41845-116">這些主題並不適用于驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="41845-116">These topics do not apply to driver services.</span></span> <span data-ttu-id="41845-117">如需驅動程式服務的介面需求，請參閱 Windows 驅動程式套件 (WDK) 。</span><span class="sxs-lookup"><span data-stu-id="41845-117">For interface requirements of driver services, see the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="41845-118">服務會以背景進程的形式執行，可能會影響系統效能、回應能力、能源效率和安全性。</span><span class="sxs-lookup"><span data-stu-id="41845-118">A service runs as a background process that can affect system performance, responsiveness, energy efficiency, and security.</span></span> <span data-ttu-id="41845-119">如需服務優化的指導方針，請參閱 [開發適用于 Windows 的有效率背景進程](/windows-hardware/drivers/kernel/implementing-power-management)。</span><span class="sxs-lookup"><span data-stu-id="41845-119">For service optimization guidelines, see [Developing Efficient Background Processes for Windows](/windows-hardware/drivers/kernel/implementing-power-management).</span></span> <span data-ttu-id="41845-120">下列主題將描述其他程式設計考慮：</span><span class="sxs-lookup"><span data-stu-id="41845-120">The following topics describe additional programming considerations:</span></span>

-   [<span data-ttu-id="41845-121">服務狀態轉換</span><span class="sxs-lookup"><span data-stu-id="41845-121">Service State Transitions</span></span>](service-status-transitions.md)
-   [<span data-ttu-id="41845-122">接收服務中的事件</span><span class="sxs-lookup"><span data-stu-id="41845-122">Receiving Events in a Service</span></span>](receiving-events-in-a-service.md)
-   [<span data-ttu-id="41845-123">多執行緒服務</span><span class="sxs-lookup"><span data-stu-id="41845-123">Multithreaded Services</span></span>](multithreaded-services.md)
-   [<span data-ttu-id="41845-124">服務和登錄</span><span class="sxs-lookup"><span data-stu-id="41845-124">Services and the Registry</span></span>](services-and-the-registry.md)
-   [<span data-ttu-id="41845-125">服務和重新導向的磁片磁碟機</span><span class="sxs-lookup"><span data-stu-id="41845-125">Services and Redirected Drives</span></span>](services-and-redirected-drives.md)
-   [<span data-ttu-id="41845-126">服務觸發程式事件</span><span class="sxs-lookup"><span data-stu-id="41845-126">Service Trigger Events</span></span>](service-trigger-events.md)

<span data-ttu-id="41845-127">請注意，如果服務程式是以 RPC 伺服器的方式運作，則應該使用動態端點和相互驗證。</span><span class="sxs-lookup"><span data-stu-id="41845-127">Note that if the service program functions as an RPC server, it should use dynamic endpoints and mutual authentication.</span></span>

 

 
