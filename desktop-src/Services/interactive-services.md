---
description: 一般來說，服務是設計來在沒有圖形化使用者介面的情況下自動執行的主控台應用程式 (GUI) 。
ms.assetid: 3d6e090a-00b1-47d8-a4fb-620f3db8ba9c
title: 互動式服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57dda3018b4b37e8c5ee56d67cd1db2c56da9b67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851495"
---
# <a name="interactive-services"></a><span data-ttu-id="6ba11-103">互動式服務</span><span class="sxs-lookup"><span data-stu-id="6ba11-103">Interactive Services</span></span>

<span data-ttu-id="6ba11-104">一般來說，服務是設計來在沒有圖形化使用者介面的情況下自動執行的主控台應用程式 (GUI) 。</span><span class="sxs-lookup"><span data-stu-id="6ba11-104">Typically, services are console applications that are designed to run unattended without a graphical user interface (GUI).</span></span> <span data-ttu-id="6ba11-105">不過，某些服務可能需要與使用者偶爾進行互動。</span><span class="sxs-lookup"><span data-stu-id="6ba11-105">However, some services may require occasional interaction with a user.</span></span> <span data-ttu-id="6ba11-106">本頁面會討論從服務與使用者互動的最佳方式。</span><span class="sxs-lookup"><span data-stu-id="6ba11-106">This page discusses the best ways to interact with the user from a service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6ba11-107">從 Windows Vista 開始，服務無法直接與使用者互動。</span><span class="sxs-lookup"><span data-stu-id="6ba11-107">Services cannot directly interact with a user as of Windows Vista.</span></span> <span data-ttu-id="6ba11-108">因此，不應在新的程式碼中使用標題為使用互動式服務的章節中所述的技術。</span><span class="sxs-lookup"><span data-stu-id="6ba11-108">Therefore, the techniques mentioned in the section titled Using an Interactive Service should not be used in new code.</span></span>

 

## <a name="interacting-with-a-user-from-a-service-indirectly"></a><span data-ttu-id="6ba11-109">間接與來自服務的使用者互動</span><span class="sxs-lookup"><span data-stu-id="6ba11-109">Interacting with a User from a Service Indirectly</span></span>

<span data-ttu-id="6ba11-110">您可以使用下列技術，從所有支援的 Windows 版本上的服務與使用者互動：</span><span class="sxs-lookup"><span data-stu-id="6ba11-110">You can use the following techniques to interact with the user from a service on all supported versions of Windows:</span></span>

-   <span data-ttu-id="6ba11-111">使用 [**WTSSendMessage**](/windows/desktop/api/wtsapi32/nf-wtsapi32-wtssendmessagea) 函數在使用者的會話中顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="6ba11-111">Display a dialog box in the user's session using the [**WTSSendMessage**](/windows/desktop/api/wtsapi32/nf-wtsapi32-wtssendmessagea) function.</span></span>
-   <span data-ttu-id="6ba11-112">建立個別隱藏的 GUI 應用程式，並使用 [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 函式在互動式使用者的內容中執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="6ba11-112">Create a separate hidden GUI application and use the [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function to run the application within the context of the interactive user.</span></span> <span data-ttu-id="6ba11-113">設計 GUI 應用程式，透過一些處理序間通訊的方法與服務通訊， (IPC) ，例如具名管道。</span><span class="sxs-lookup"><span data-stu-id="6ba11-113">Design the GUI application to communicate with the service through some method of interprocess communication (IPC), for example, named pipes.</span></span> <span data-ttu-id="6ba11-114">服務會與 GUI 應用程式通訊，以告訴它何時顯示 GUI。</span><span class="sxs-lookup"><span data-stu-id="6ba11-114">The service communicates with the GUI application to tell it when to display the GUI.</span></span> <span data-ttu-id="6ba11-115">應用程式會將使用者互動的結果傳達給服務，讓服務可以採取適當的動作。</span><span class="sxs-lookup"><span data-stu-id="6ba11-115">The application communicates the results of the user interaction back to the service so that the service can take the appropriate action.</span></span> <span data-ttu-id="6ba11-116">請注意，除非您 (ACL) 使用適當的存取控制清單，否則 IPC 可以透過網路公開您的服務介面。</span><span class="sxs-lookup"><span data-stu-id="6ba11-116">Note that IPC can expose your service interfaces over the network unless you use an appropriate access control list (ACL).</span></span>

    <span data-ttu-id="6ba11-117">如果此服務在多使用者的系統上執行，請將應用程式新增至下列機碼，以便在每個會話中執行： **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows \\ CurrentVersion \\ run**。</span><span class="sxs-lookup"><span data-stu-id="6ba11-117">If this service runs on a multiuser system, add the application to the following key so that it is run in each session: **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Run**.</span></span> <span data-ttu-id="6ba11-118">如果應用程式使用具名管道進行 IPC，伺服器可以根據會話識別碼為每個管道提供唯一的名稱，以區別多個使用者進程。</span><span class="sxs-lookup"><span data-stu-id="6ba11-118">If the application uses named pipes for IPC, the server can distinguish between multiple user processes by giving each pipe a unique name based on the session ID.</span></span>

<span data-ttu-id="6ba11-119">Windows Server 2003 和 Windows XP 也提供下列技術：</span><span class="sxs-lookup"><span data-stu-id="6ba11-119">The following technique is also available for Windows Server 2003 and Windows XP:</span></span>

-   <span data-ttu-id="6ba11-120">藉由呼叫 [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) 函式與 **MB \_ 服務 \_ 通知** 來顯示訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="6ba11-120">Display a message box by calling the [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) function with **MB\_SERVICE\_NOTIFICATION**.</span></span> <span data-ttu-id="6ba11-121">這是顯示簡單狀態訊息的建議。</span><span class="sxs-lookup"><span data-stu-id="6ba11-121">This is recommended for displaying simple status messages.</span></span> <span data-ttu-id="6ba11-122">除非您是從不同的執行緒呼叫 MessageBox，否則請勿在服務初始化期間或從 [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex)常式呼叫 **MessageBox** ，如此您就可以及時返回 SCM。</span><span class="sxs-lookup"><span data-stu-id="6ba11-122">Do not call **MessageBox** during service initialization or from the [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) routine, unless you call it from a separate thread, so that you return to the SCM in a timely manner.</span></span>

## <a name="using-an-interactive-service"></a><span data-ttu-id="6ba11-123">使用互動式服務</span><span class="sxs-lookup"><span data-stu-id="6ba11-123">Using an Interactive Service</span></span>

<span data-ttu-id="6ba11-124">依預設，服務會使用非互動式 [視窗站](/windows/desktop/winstation/window-stations) ，而且無法與使用者互動。</span><span class="sxs-lookup"><span data-stu-id="6ba11-124">By default, services use a noninteractive [window station](/windows/desktop/winstation/window-stations) and cannot interact with the user.</span></span> <span data-ttu-id="6ba11-125">不過， *互動式服務* 可以顯示使用者介面，並接收使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="6ba11-125">However, an *interactive service* can display a user interface and receive user input.</span></span>

> [!Caution]  
> <span data-ttu-id="6ba11-126">在較高的安全性內容中執行的服務（例如 LocalSystem 帳戶），不應該在互動式桌面上建立視窗，因為在互動式桌面上執行的任何其他應用程式都可以與此視窗互動。</span><span class="sxs-lookup"><span data-stu-id="6ba11-126">Services running in an elevated security context, such as the LocalSystem account, should not create a window on the interactive desktop because any other application that is running on the interactive desktop can interact with this window.</span></span> <span data-ttu-id="6ba11-127">這會將服務公開給登入使用者執行的任何應用程式。</span><span class="sxs-lookup"><span data-stu-id="6ba11-127">This exposes the service to any application that a logged-on user executes.</span></span> <span data-ttu-id="6ba11-128">此外，以 LocalSystem 身分執行的服務不應藉由呼叫 [**OpenWindowStation**](/windows/desktop/api/winuser/nf-winuser-openwindowstationa) 或 [**GetThreadDesktop**](/windows/desktop/api/winuser/nf-winuser-getthreaddesktop) 函數來存取互動式桌面。</span><span class="sxs-lookup"><span data-stu-id="6ba11-128">Also, services that are running as LocalSystem should not access the interactive desktop by calling the [**OpenWindowStation**](/windows/desktop/api/winuser/nf-winuser-openwindowstationa) or [**GetThreadDesktop**](/windows/desktop/api/winuser/nf-winuser-getthreaddesktop) function.</span></span>

 

<span data-ttu-id="6ba11-129">若要建立互動式服務，請在呼叫 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) 函式時執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="6ba11-129">To create an interactive service, do the following when calling the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function:</span></span>

1.  <span data-ttu-id="6ba11-130">針對 *lpServiceStartName* 參數指定 Null，以在 [LocalSystem 帳戶](localsystem-account.md)內容中執行服務。</span><span class="sxs-lookup"><span data-stu-id="6ba11-130">Specify NULL for the *lpServiceStartName* parameter to run the service in the context of the [LocalSystem account](localsystem-account.md).</span></span>
2.  <span data-ttu-id="6ba11-131">指定 **服務 \_ 互動式 \_ 進程** 旗標。</span><span class="sxs-lookup"><span data-stu-id="6ba11-131">Specify the **SERVICE\_INTERACTIVE\_PROCESS** flag.</span></span>

<span data-ttu-id="6ba11-132">若要判斷服務是否以互動式服務的形式執行，請呼叫 [**GetProcessWindowStation**](/windows/desktop/api/winuser/nf-winuser-getprocesswindowstation) 函式以抓取視窗工作站的控制碼，並使用 [**GetUserObjectInformation**](/windows/desktop/api/winuser/nf-winuser-getuserobjectinformationa) 函式來測試視窗工作站是否具有 **w2kmiguser.wsf \_ 可見** 的屬性。</span><span class="sxs-lookup"><span data-stu-id="6ba11-132">To determine whether a service is running as an interactive service, call the [**GetProcessWindowStation**](/windows/desktop/api/winuser/nf-winuser-getprocesswindowstation) function to retrieve a handle to the window station, and the [**GetUserObjectInformation**](/windows/desktop/api/winuser/nf-winuser-getuserobjectinformationa) function to test whether the window station has the **WSF\_VISIBLE** attribute.</span></span>

<span data-ttu-id="6ba11-133">不過請注意，下列登錄機碼包含值 **NoInteractiveServices**，可控制服務 \_ 互動式進程的效果 \_ ：</span><span class="sxs-lookup"><span data-stu-id="6ba11-133">However, note that the following registry key contains a value, **NoInteractiveServices**, that controls the effect of SERVICE\_INTERACTIVE\_PROCESS:</span></span>

<span data-ttu-id="6ba11-134">**HKEY \_ 本機 \_ 電腦 \\ 系統 \\ CurrentControlSet \\ 控制 \\ 視窗**</span><span class="sxs-lookup"><span data-stu-id="6ba11-134">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\Windows**</span></span>

<span data-ttu-id="6ba11-135">**NoInteractiveServices** 值預設為1，表示不允許任何服務以互動方式執行，不論它是否有 **服務 \_ 互動式 \_ 進程**。</span><span class="sxs-lookup"><span data-stu-id="6ba11-135">The **NoInteractiveServices** value defaults to 1, which means that no service is allowed to run interactively, regardless of whether it has **SERVICE\_INTERACTIVE\_PROCESS**.</span></span> <span data-ttu-id="6ba11-136">當 **NoInteractiveServices** 設為0時，會允許具有 **服務 \_ 互動式 \_ 進程** 的服務以互動方式執行。</span><span class="sxs-lookup"><span data-stu-id="6ba11-136">When **NoInteractiveServices** is set to a 0, services with **SERVICE\_INTERACTIVE\_PROCESS** are allowed to run interactively.</span></span>

<span data-ttu-id="6ba11-137">**Windows 7、Windows server 2008 R2、WINDOWS XP 及 Windows server 2003：\*\*\*\*NoInteractiveServices** 值的預設值為0，這表示具有 **服務 \_ 互動式 \_ 進程** 的服務允許以互動方式執行。</span><span class="sxs-lookup"><span data-stu-id="6ba11-137">**Windows 7, Windows Server 2008 R2, Windows XP and Windows Server 2003:** The **NoInteractiveServices** value defaults to 0, which means that services with **SERVICE\_INTERACTIVE\_PROCESS** are allowed to run interactively.</span></span> <span data-ttu-id="6ba11-138">當 **NoInteractiveServices** 設定為非零值時，就不會在之後啟動任何服務，不論它是否有 **服務 \_ 互動式 \_ 進程**。</span><span class="sxs-lookup"><span data-stu-id="6ba11-138">When **NoInteractiveServices** is set to a nonzero value, no service started thereafter is allowed to run interactively, regardless of whether it has **SERVICE\_INTERACTIVE\_PROCESS**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6ba11-139">所有服務都會在終端機服務會話0中執行。</span><span class="sxs-lookup"><span data-stu-id="6ba11-139">All services run in Terminal Services session 0.</span></span> <span data-ttu-id="6ba11-140">因此，如果互動式服務顯示使用者介面，只有連接到會話0的使用者才會看到它。</span><span class="sxs-lookup"><span data-stu-id="6ba11-140">Therefore, if an interactive service displays a user interface, it is visible only to the user who connected to session 0.</span></span> <span data-ttu-id="6ba11-141">因為無法保證互動式使用者已連線到會話0，所以請勿將服務設定為在終端機服務或支援快速切換使用者的系統上以互動式服務的形式執行， (使用終端機服務) 來執行快速使用者切換。</span><span class="sxs-lookup"><span data-stu-id="6ba11-141">Because there is no way to guarantee that the interactive user is connected to session 0, do not configure a service to run as an interactive service under Terminal Services or on a system that supports fast user switching (fast user switching is implemented using Terminal Services).</span></span>

 

 

 
