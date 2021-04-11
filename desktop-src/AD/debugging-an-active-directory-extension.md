---
title: Active Directory 擴充功能的偵錯工具
description: 本主題中記載的 Microsoft Active Directory Directory 服務屬性工作表、內容功能表和物件建立嚮導延伸模組會實作為 COM 的內部進程伺服器。
ms.assetid: 8c280084-fd2f-4d34-a119-d4e925a68a5c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc8d9646f4ccc2e8c740a81ddb48422881744f5
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023262"
---
# <a name="debugging-an-active-directory-extension"></a><span data-ttu-id="d79bc-103">Active Directory 擴充功能的偵錯工具</span><span class="sxs-lookup"><span data-stu-id="d79bc-103">Debugging an Active Directory Extension</span></span>

<span data-ttu-id="d79bc-104">本主題中記載的 Microsoft Active Directory Directory 服務屬性工作表、內容功能表和物件建立嚮導延伸模組會實作為 COM 的內部進程伺服器。</span><span class="sxs-lookup"><span data-stu-id="d79bc-104">The Microsoft Active Directory directory service property sheet, context menu, and object creation wizard extensions documented in this topic are implemented as COM in-proc servers.</span></span> <span data-ttu-id="d79bc-105">也就是說，每個延伸模組都是在主機進程內容中執行的 DLL。</span><span class="sxs-lookup"><span data-stu-id="d79bc-105">That is, each extension is a DLL that runs in the context of the host process.</span></span> <span data-ttu-id="d79bc-106">若要對延伸模組進行偵錯工具，必須將擴充功能與應用程式建立關聯，並在偵錯工具中執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="d79bc-106">To debug the extension, it is necessary to associate the extension with an application and run the application in a debugger.</span></span>

## <a name="debugging-active-directory-extensions-displayed-in-the-windows-shell"></a><span data-ttu-id="d79bc-107">在 Windows Shell 中顯示 Active Directory 擴充功能的偵錯工具</span><span class="sxs-lookup"><span data-stu-id="d79bc-107">Debugging Active Directory Extensions Displayed in the Windows Shell</span></span>

<span data-ttu-id="d79bc-108">在 Explorer.exe 進程的內容中，會載入 Windows shell 中顯示的 Active Directory 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="d79bc-108">Active Directory extensions displayed in the Windows shell are loaded in the context of the Explorer.exe process.</span></span> <span data-ttu-id="d79bc-109">這些擴充功能可以像標準 shell 擴充功能一樣地進行調試。</span><span class="sxs-lookup"><span data-stu-id="d79bc-109">These extensions can be debugged like a standard shell extension.</span></span> <span data-ttu-id="d79bc-110">如需有關偵錯工具擴充功能的詳細資訊，請參閱 [使用 shell 進行的調試](/previous-versions/windows/desktop/legacy/cc144064(v=vs.85))程式。</span><span class="sxs-lookup"><span data-stu-id="d79bc-110">For more information about debugging shell extensions, see [Debugging with the Shell](/previous-versions/windows/desktop/legacy/cc144064(v=vs.85)).</span></span>

## <a name="debugging-active-directory-extensions-displayed-in-the-active-directory-mmc-snap-ins"></a><span data-ttu-id="d79bc-111">Active Directory MMC 中所顯示 Active Directory 擴充功能的調試 Snap-Ins</span><span class="sxs-lookup"><span data-stu-id="d79bc-111">Debugging Active Directory Extensions Displayed in the Active Directory MMC Snap-Ins</span></span>

<span data-ttu-id="d79bc-112">Active Directory 系統管理 MMC 嵌入式管理單元中顯示的 Active Directory 延伸模組會載入 Microsoft Management Console 的內容中。</span><span class="sxs-lookup"><span data-stu-id="d79bc-112">Active Directory extensions displayed in the Active Directory administrative MMC snap-ins are loaded in the context of the Microsoft Management Console.</span></span> <span data-ttu-id="d79bc-113">若要 debug 擴充功能，請在本機系統上找出 Mmc.exe，並將偵錯工具設定為使用此應用程式來進行偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="d79bc-113">To debug an extension, locate Mmc.exe on the local system and set the debugger to use this as the application for debugging.</span></span> <span data-ttu-id="d79bc-114">在大部分的系統上，Mmc.exe 位於 Windows 系統目錄中，例如 C： \\ WINNT \\ System32。</span><span class="sxs-lookup"><span data-stu-id="d79bc-114">On most systems, Mmc.exe is located in the Windows system directory, for example, C:\\WINNT\\System32.</span></span> <span data-ttu-id="d79bc-115">視偵錯工具而定，您可能也不需要將擴充 DLL 設定為也要由偵錯工具載入。</span><span class="sxs-lookup"><span data-stu-id="d79bc-115">Depending on the debugger, you may or may not have to set the extension DLL to also be loaded by the debugger.</span></span> <span data-ttu-id="d79bc-116">許多偵錯工具也可讓您將偵錯工具附加至執行中的 MMC 進程。</span><span class="sxs-lookup"><span data-stu-id="d79bc-116">Many debuggers also allow you to attach the debugger to a running MMC process.</span></span> <span data-ttu-id="d79bc-117">如需詳細資訊，請參閱您的偵錯工具使用者指南。</span><span class="sxs-lookup"><span data-stu-id="d79bc-117">For more information, see your debugger User's Guide.</span></span>

<span data-ttu-id="d79bc-118">讓 MMC 自動載入特定的嵌入式管理單元是很方便的。</span><span class="sxs-lookup"><span data-stu-id="d79bc-118">It can be convenient to have MMC automatically load a specific snap-in.</span></span> <span data-ttu-id="d79bc-119">若要這樣做，請將應用程式引數設定為 SERVICES.MSC 檔案的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="d79bc-119">To do this, set the application arguments to the path and file name of an MSC file.</span></span> <span data-ttu-id="d79bc-120">這可以是系統安裝的 SERVICES.MSC 檔案，也可以是您建立的檔案。</span><span class="sxs-lookup"><span data-stu-id="d79bc-120">This can either be a system-installed MSC file or one you create.</span></span> <span data-ttu-id="d79bc-121">您可以依照下列步驟來建立 SERVICES.MSC 檔案。</span><span class="sxs-lookup"><span data-stu-id="d79bc-121">An MSC file can be created by following these steps.</span></span>

1.  <span data-ttu-id="d79bc-122">執行 Mmc.exe。</span><span class="sxs-lookup"><span data-stu-id="d79bc-122">Run Mmc.exe.</span></span>
2.  <span data-ttu-id="d79bc-123">**選取**  -  mmc 功能表中的 [檔案 **新增/移除嵌入式管理單元 ...** ]，然後選取所需的嵌入式管理單元，以載入所需的嵌入式管理單元。</span><span class="sxs-lookup"><span data-stu-id="d79bc-123">Load the desired snap-in by selecting **File** - **Add/Remove Snap-in...** in the MMC menu and select the desired snap-in.</span></span>
3.  <span data-ttu-id="d79bc-124">選取 MMC 功能表中的 [   -  **另存** 新檔]，以儲存 services.msc 檔案。</span><span class="sxs-lookup"><span data-stu-id="d79bc-124">Save the MSC file by selecting **File** - **Save As...** in the MMC menu.</span></span>

<span data-ttu-id="d79bc-125">如果您未設定啟動 SERVICES.MSC 檔案，當您在偵錯工具中執行應用程式時，必須手動載入所需的嵌入式管理單元。</span><span class="sxs-lookup"><span data-stu-id="d79bc-125">If you do not set a start-up MSC file, you must manually load the desired snap-in when you run the application in the debugger.</span></span>

<span data-ttu-id="d79bc-126">當主應用程式在偵錯工具中執行時，偵錯工具可能會顯示一則警告訊息，指出正在執行的應用程式不包含任何 debug 符號。</span><span class="sxs-lookup"><span data-stu-id="d79bc-126">When the host application is run in the debugger, the debugger may display a warning message stating that the application being run does not contain any debug symbols.</span></span> <span data-ttu-id="d79bc-127">這是預期的情況，而且可以安全地忽略，因為您實際上是在偵錯工具，而不是主應用程式。</span><span class="sxs-lookup"><span data-stu-id="d79bc-127">This is expected and can safely be ignored because you are actually debugging the DLL, not the host application.</span></span>

<span data-ttu-id="d79bc-128">在大部分的情況下，將不會呼叫擴充功能，直到使用者執行某些動作，而導致載入和初始化擴充功能為止。</span><span class="sxs-lookup"><span data-stu-id="d79bc-128">In most cases, the extension will not be called until the user performs some action that causes the extension to be loaded and initialized.</span></span> <span data-ttu-id="d79bc-129">例如，如果您要對使用者物件所顯示的內容功能表延伸進行偵錯工具，則在第一次顯示使用者物件的內容功能表之前，將不會載入擴充功能。</span><span class="sxs-lookup"><span data-stu-id="d79bc-129">For example, if you are debugging a context menu extension displayed for user objects, the extension will not load until the first time the context menu for a user object is displayed.</span></span>

<span data-ttu-id="d79bc-130">您現在應該能夠設定中斷點並查看調試輸出。</span><span class="sxs-lookup"><span data-stu-id="d79bc-130">You should now be able to set breakpoints and view debug output.</span></span> <span data-ttu-id="d79bc-131">如果延伸模組似乎未載入，請在擴充功能的 [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) 函式中設定中斷點。</span><span class="sxs-lookup"><span data-stu-id="d79bc-131">If the extension does not appear to load, set a breakpoint in the extension's [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) function.</span></span> <span data-ttu-id="d79bc-132">如果未呼叫 **DllGetClassObject** ，可能是因為擴充功能未正確註冊。</span><span class="sxs-lookup"><span data-stu-id="d79bc-132">If **DllGetClassObject** is not called, the extension is probably not registered correctly.</span></span>

<span data-ttu-id="d79bc-133">當偵錯工具完成時，結束 MMC 和偵錯工具應該會正常地卸載。</span><span class="sxs-lookup"><span data-stu-id="d79bc-133">When the debug is complete, exit MMC and the debugger should unload normally.</span></span>

 

 