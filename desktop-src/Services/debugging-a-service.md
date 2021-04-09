---
description: 您可以使用下列任何一種方法來對服務進行 debug。
ms.assetid: 6f4ae117-2120-4c1e-b69f-641ce2e633fa
title: 對服務進行偵錯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebd99acfc6ad0e436b7f726c96af9e5d1c58442
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690076"
---
# <a name="debugging-a-service"></a><span data-ttu-id="b41fc-103">對服務進行偵錯</span><span class="sxs-lookup"><span data-stu-id="b41fc-103">Debugging a Service</span></span>

<span data-ttu-id="b41fc-104">您可以使用下列任何一種方法來對服務進行 debug。</span><span class="sxs-lookup"><span data-stu-id="b41fc-104">You can use any one of the following methods to debug your service.</span></span>

-   <span data-ttu-id="b41fc-105">使用您的偵錯工具，在服務執行時進行偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="b41fc-105">Use your debugger to debug the service while it is running.</span></span> <span data-ttu-id="b41fc-106">首先，取得服務進程 (PID) 的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="b41fc-106">First, obtain the process identifier (PID) of the service process.</span></span> <span data-ttu-id="b41fc-107">取得 PID 之後，請附加至正在執行的進程。</span><span class="sxs-lookup"><span data-stu-id="b41fc-107">After you have obtained the PID, attach to the running process.</span></span> <span data-ttu-id="b41fc-108">如需語法資訊，請參閱偵錯工具隨附的檔。</span><span class="sxs-lookup"><span data-stu-id="b41fc-108">For syntax information, see the documentation included with your debugger.</span></span>
-   <span data-ttu-id="b41fc-109">呼叫 [**DebugBreak**](/windows/desktop/api/debugapi/nf-debugapi-debugbreak) 函式來叫用偵錯工具，以進行即時的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="b41fc-109">Call the [**DebugBreak**](/windows/desktop/api/debugapi/nf-debugapi-debugbreak) function to invoke the debugger for just-in-time debugging.</span></span>
-   <span data-ttu-id="b41fc-110">指定啟動程式時要使用的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="b41fc-110">Specify a debugger to use when starting a program.</span></span> <span data-ttu-id="b41fc-111">若要這樣做，請在下列登錄位置中建立名為 **影像檔執行選項** 的金鑰：</span><span class="sxs-lookup"><span data-stu-id="b41fc-111">To do so, create a key called **Image File Execution Options** in the following registry location:</span></span>

    <span data-ttu-id="b41fc-112">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows NT \\ CurrentVersion**</span><span class="sxs-lookup"><span data-stu-id="b41fc-112">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion**</span></span>

    <span data-ttu-id="b41fc-113">使用與服務相同的名稱建立子機碼 (例如 MYSERV.EXE) 。</span><span class="sxs-lookup"><span data-stu-id="b41fc-113">Create a subkey with the same name as your service (for example, MYSERV.EXE).</span></span> <span data-ttu-id="b41fc-114">若要使用這個子機碼，請新增名為 **[偵錯工具**] 的 **REG \_ SZ** 類型值。</span><span class="sxs-lookup"><span data-stu-id="b41fc-114">To this subkey, add a value of type **REG\_SZ**, named **Debugger**.</span></span> <span data-ttu-id="b41fc-115">使用偵錯工具的完整路徑做為字串值。</span><span class="sxs-lookup"><span data-stu-id="b41fc-115">Use the full path to the debugger as the string value.</span></span> <span data-ttu-id="b41fc-116">在 [服務控制台] 小程式中，選取您的服務，按一下 [ **啟動** ]，然後核取 [ **允許服務與桌面互動]**。</span><span class="sxs-lookup"><span data-stu-id="b41fc-116">In the Services control panel applet, select your service, click **Startup** and check **Allow Service to Interact with Desktop**.</span></span> <span data-ttu-id="b41fc-117">服務必須是互動式服務，否則偵錯工具無法在預設桌面上執行。</span><span class="sxs-lookup"><span data-stu-id="b41fc-117">The service must be an interactive service, or else the debugger cannot run on the default desktop.</span></span> <span data-ttu-id="b41fc-118">請注意，Windows Vista 不再支援這項技術，因為所有服務都是在專為服務保留的會話中執行，而且不支援顯示使用者介面。</span><span class="sxs-lookup"><span data-stu-id="b41fc-118">Note that this technique is no longer supported as of Windows Vista because all services are run in session that is reserved exclusively for services and does not support displaying a user interface.</span></span>

-   <span data-ttu-id="b41fc-119">使用 [事件追蹤](/windows/desktop/ETW/event-tracing-portal) 來記錄資訊。</span><span class="sxs-lookup"><span data-stu-id="b41fc-119">Use [Event Tracing](/windows/desktop/ETW/event-tracing-portal) to log information.</span></span>

<span data-ttu-id="b41fc-120">若要將自動啟動服務的初始化程式碼進行偵錯工具，您必須以隨選啟動服務的方式暫時安裝和執行服務。</span><span class="sxs-lookup"><span data-stu-id="b41fc-120">To debug the initialization code of an auto-start service, you will have to temporarily install and run the service as a demand-start service.</span></span>

<span data-ttu-id="b41fc-121">有時候，可能需要以主控台應用程式的形式執行服務，以進行偵測。</span><span class="sxs-lookup"><span data-stu-id="b41fc-121">At times, it may be necessary to run a service as a console application for debugging purposes.</span></span> <span data-ttu-id="b41fc-122">在此案例中， [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) 函式會傳回 **錯誤的 \_ \_ SERVICE \_ CONTROLLER \_ CONNECT**。</span><span class="sxs-lookup"><span data-stu-id="b41fc-122">In this scenario, the [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) function will return **ERROR\_FAILED\_SERVICE\_CONTROLLER\_CONNECT**.</span></span> <span data-ttu-id="b41fc-123">因此，請務必將您的程式碼結構，使其不會在傳回此錯誤時呼叫服務特定程式碼。</span><span class="sxs-lookup"><span data-stu-id="b41fc-123">Therefore, be sure to structure your code such that service-specific code is not called when this error is returned.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b41fc-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="b41fc-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b41fc-125">將服務應用程式偵錯工具</span><span class="sxs-lookup"><span data-stu-id="b41fc-125">Debugging a Service Application</span></span>](https://msdn.microsoft.com/library/cc267835.aspx)
</dt> <dt>

[<span data-ttu-id="b41fc-126">Windows 的偵錯工具</span><span class="sxs-lookup"><span data-stu-id="b41fc-126">Debugging Tools for Windows</span></span>](https://msdn.microsoft.com/library/cc267445.aspx)
</dt> </dl>

 

 
