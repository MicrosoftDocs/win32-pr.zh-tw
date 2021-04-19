---
description: 有三種方式可讓應用程式關閉本機或遠端電腦：將 systemshut 向下關閉系統，然後重新開機應用程式的 itshut，關閉並重新啟動系統，然後重新開機任何已註冊要重新開機的應用程式
ms.assetid: acadf58f-3f68-4fa1-bdcf-8f85c8479263
title: 關閉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e436dd9e3b115112e63b0440b4d51de4c7f9f619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994506"
---
# <a name="shutting-down"></a><span data-ttu-id="72f6f-103">關閉</span><span class="sxs-lookup"><span data-stu-id="72f6f-103">Shutting Down</span></span>

<span data-ttu-id="72f6f-104">有三種方式可讓應用程式關閉本機或遠端電腦：</span><span class="sxs-lookup"><span data-stu-id="72f6f-104">There are three ways for an application to shut down local or remote computers:</span></span>

-   <span data-ttu-id="72f6f-105">關閉系統</span><span class="sxs-lookup"><span data-stu-id="72f6f-105">shut down the system</span></span>
-   <span data-ttu-id="72f6f-106">將系統關機並重新啟動</span><span class="sxs-lookup"><span data-stu-id="72f6f-106">shut down the system and restart it</span></span>
-   <span data-ttu-id="72f6f-107">關閉應用程式、關閉並重新啟動系統，然後重新開機任何已註冊要重新開機的應用程式</span><span class="sxs-lookup"><span data-stu-id="72f6f-107">shut down the application, shut down and restart the system, and restart any applications that have been registered for restart</span></span>

<span data-ttu-id="72f6f-108">若要關閉系統，請使用 [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) 函式搭配 EWX \_ 關機旗標。</span><span class="sxs-lookup"><span data-stu-id="72f6f-108">To shut down the system, use the [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) function with the EWX\_SHUTDOWN flag.</span></span> <span data-ttu-id="72f6f-109">如需範例，請參閱 [如何關機系統](how-to-shut-down-the-system.md)。</span><span class="sxs-lookup"><span data-stu-id="72f6f-109">For an example, see [How to Shut Down the System](how-to-shut-down-the-system.md).</span></span> <span data-ttu-id="72f6f-110">若要關閉並重新啟動系統，請使用 EWX \_ 重新開機旗標。</span><span class="sxs-lookup"><span data-stu-id="72f6f-110">To shut down and restart the system, use the EWX\_REBOOT flag.</span></span> <span data-ttu-id="72f6f-111">若要使用 [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) 函式重新開機任何已註冊要重新開機的應用程式，請使用 EXW \_ RESTARTAPPS 旗標。</span><span class="sxs-lookup"><span data-stu-id="72f6f-111">To restart any applications that have been registered for restart using the [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) function, use the EXW\_RESTARTAPPS flag.</span></span>

<span data-ttu-id="72f6f-112">[**InitiateShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiateshutdowna)、 [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna)和 [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)函式會啟動計時器，並顯示會提示使用者登出的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="72f6f-112">The [**InitiateShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiateshutdowna), [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna), and [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) functions start a timer and display a dialog box that prompts the user to log off.</span></span> <span data-ttu-id="72f6f-113">當這個對話方塊顯示時， [**AbortSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna) 函式可以停止計時器，並防止電腦關機。</span><span class="sxs-lookup"><span data-stu-id="72f6f-113">While this dialog box is displayed, the [**AbortSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna) function can stop the timer and prevent the computer from shutting down.</span></span> <span data-ttu-id="72f6f-114">但是，如果計時器過期，則會關閉電腦。</span><span class="sxs-lookup"><span data-stu-id="72f6f-114">However, if the timer expires, the computer is shut down.</span></span> <span data-ttu-id="72f6f-115">這些函式也可以在關機操作後重新開機電腦。</span><span class="sxs-lookup"><span data-stu-id="72f6f-115">These functions can also restart the computer following a shutdown operation.</span></span> <span data-ttu-id="72f6f-116">如需詳細資訊，請參閱 [顯示關閉對話方塊](displaying-the-shutdown-dialog-box.md)。</span><span class="sxs-lookup"><span data-stu-id="72f6f-116">For more information, see [Displaying the Shutdown Dialog Box](displaying-the-shutdown-dialog-box.md).</span></span>

## <a name="shutdown-notifications"></a><span data-ttu-id="72f6f-117">關機通知</span><span class="sxs-lookup"><span data-stu-id="72f6f-117">Shutdown Notifications</span></span>

<span data-ttu-id="72f6f-118">具有視窗和訊息佇列的應用程式會透過 [**wm \_ QUERYENDSESSION**](wm-queryendsession.md) 和 [**wm \_ ENDSESSION**](wm-endsession.md) 訊息接收關機通知。</span><span class="sxs-lookup"><span data-stu-id="72f6f-118">Applications with a window and message queue receive shutdown notifications through the [**WM\_QUERYENDSESSION**](wm-queryendsession.md) and [**WM\_ENDSESSION**](wm-endsession.md) messages.</span></span> <span data-ttu-id="72f6f-119">這些應用程式應該會傳回 **TRUE** ，表示可以終止它們。</span><span class="sxs-lookup"><span data-stu-id="72f6f-119">These applications should return **TRUE** to indicate that they can be terminated.</span></span> <span data-ttu-id="72f6f-120">除非絕對必要，否則應用程式不應封鎖系統關機。</span><span class="sxs-lookup"><span data-stu-id="72f6f-120">Applications should not block system shutdown unless it is absolutely necessary.</span></span> <span data-ttu-id="72f6f-121">應用程式應該在處理 **WM \_ ENDSESSION** 時執行任何必要的清除。</span><span class="sxs-lookup"><span data-stu-id="72f6f-121">Applications should perform any required cleanup while processing **WM\_ENDSESSION**.</span></span> <span data-ttu-id="72f6f-122">具有未儲存資料的應用程式可以將資料儲存至暫存位置，並在應用程式下次啟動時還原資料。</span><span class="sxs-lookup"><span data-stu-id="72f6f-122">Applications that have unsaved data could save the data to a temporary location and restore it the next time the application starts.</span></span> <span data-ttu-id="72f6f-123">建議應用程式經常儲存其資料和狀態。例如，會在使用者起始的儲存作業之間自動儲存資料，以減少在關機時要儲存的資料量。</span><span class="sxs-lookup"><span data-stu-id="72f6f-123">It is recommended that applications save their data and state frequently; for example, automatically save data between save operations initiated by the user to reduce the amount of data to be saved at shutdown.</span></span>

<span data-ttu-id="72f6f-124">主控台應用程式會在其處理常式常式中接收關機通知。</span><span class="sxs-lookup"><span data-stu-id="72f6f-124">Console applications receive shutdown notifications in their handler routines.</span></span> <span data-ttu-id="72f6f-125">若要註冊主控台處理常式，請使用 [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) 函數。</span><span class="sxs-lookup"><span data-stu-id="72f6f-125">To register a console handler, use the [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) function.</span></span>

<span data-ttu-id="72f6f-126">服務應用程式會在其處理常式常式中接收關機通知。</span><span class="sxs-lookup"><span data-stu-id="72f6f-126">Service applications receive shutdown notifications in their handler routines.</span></span> <span data-ttu-id="72f6f-127">若要註冊服務控制處理常式，請使用 [**RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) 函數。</span><span class="sxs-lookup"><span data-stu-id="72f6f-127">To register a service control handler, use the [**RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) function.</span></span>

## <a name="blocking-shutdown"></a><span data-ttu-id="72f6f-128">封鎖關機</span><span class="sxs-lookup"><span data-stu-id="72f6f-128">Blocking Shutdown</span></span>

<span data-ttu-id="72f6f-129">如果應用程式必須封鎖可能的系統關閉，則可以呼叫 [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) 函數。</span><span class="sxs-lookup"><span data-stu-id="72f6f-129">If an application must block a potential system shutdown, it can call the [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) function.</span></span> <span data-ttu-id="72f6f-130">呼叫端會提供將向使用者顯示的原因字串。</span><span class="sxs-lookup"><span data-stu-id="72f6f-130">The caller provides a reason string that will be displayed to the user.</span></span> <span data-ttu-id="72f6f-131">原因字串應該簡短且清楚明瞭，提供使用者決定是否要繼續關閉系統所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="72f6f-131">The reason string should be short and clear, providing the user with the information necessary to decide whether to continue shutting down the system.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72f6f-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="72f6f-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72f6f-133">如何關機系統</span><span class="sxs-lookup"><span data-stu-id="72f6f-133">How to Shut Down the System</span></span>](how-to-shut-down-the-system.md)
</dt> </dl>

 

 
