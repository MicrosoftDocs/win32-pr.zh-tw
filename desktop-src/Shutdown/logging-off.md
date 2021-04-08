---
description: ExitWindows 函式會將目前的使用者登出。 您也可以使用 EXW 登出旗標來呼叫 ExitWindowsEx 函數 \_ 。
ms.assetid: 906d92f1-7cbe-454e-9c71-34b4383aebab
title: 登出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0571c0522c494acd763d57dcae8d200125cd53d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853116"
---
# <a name="logging-off"></a><span data-ttu-id="9fd1e-104">登出</span><span class="sxs-lookup"><span data-stu-id="9fd1e-104">Logging Off</span></span>

<span data-ttu-id="9fd1e-105">[**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows)函式會將目前的使用者登出。</span><span class="sxs-lookup"><span data-stu-id="9fd1e-105">The [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) function logs off the current user.</span></span> <span data-ttu-id="9fd1e-106">您也可以使用 EXW 登出旗標來呼叫 [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) 函數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9fd1e-106">You can also call the [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) function with the EXW\_LOGOFF flag.</span></span>

<span data-ttu-id="9fd1e-107">根據預設，當應用程式使用 [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) 或 [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) 來登出時，系統會將 [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) 訊息傳送至每個視窗。</span><span class="sxs-lookup"><span data-stu-id="9fd1e-107">By default, when an application uses [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) or [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) to log off, the system sends the [**WM\_QUERYENDSESSION**](wm-queryendsession.md) message to each window.</span></span> <span data-ttu-id="9fd1e-108">應用程式在收到此訊息時，會傳回 **TRUE** 來同意終止。</span><span class="sxs-lookup"><span data-stu-id="9fd1e-108">Applications agree to terminate by returning **TRUE** when they receive this message.</span></span> <span data-ttu-id="9fd1e-109">如果任何應用程式在處理此訊息時傳回 **FALSE** ，就會取消登出作業。</span><span class="sxs-lookup"><span data-stu-id="9fd1e-109">If any application returns **FALSE** when processing this message, the log-off operation is canceled.</span></span> <span data-ttu-id="9fd1e-110">如果您的應用程式會處理 **WM \_ QUERYENDSESSION** 訊息，您可以允許使用者取消登出作業，即使另一個應用程式或系統產生了端對端會話的要求也是一樣。</span><span class="sxs-lookup"><span data-stu-id="9fd1e-110">If your application handles the **WM\_QUERYENDSESSION** message, you can allow the user to cancel the log-off operation, even if another application or the system originated the end-session request.</span></span> <span data-ttu-id="9fd1e-111">如需範例，請參閱 [如何登出目前的使用者](how-to-log-off-the-current-user.md)。</span><span class="sxs-lookup"><span data-stu-id="9fd1e-111">For an example, see [How to Log Off the Current User](how-to-log-off-the-current-user.md).</span></span>

<span data-ttu-id="9fd1e-112">當應用程式針對 [**wm \_ QUERYENDSESSION**](wm-queryendsession.md)傳回 **TRUE** 時，無論其他應用程式如何回應 **wm \_ QUERYENDSESSION** 訊息，它都會收到 [**wm \_ ENDSESSION**](wm-endsession.md)訊息並將它終止。</span><span class="sxs-lookup"><span data-stu-id="9fd1e-112">When an application returns **TRUE** for [**WM\_QUERYENDSESSION**](wm-queryendsession.md), it receives the [**WM\_ENDSESSION**](wm-endsession.md) message and it is terminated, regardless of how the other applications respond to the **WM\_QUERYENDSESSION** message.</span></span>

<span data-ttu-id="9fd1e-113">若要強制所有應用程式終止，請使用 [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)，並指定 EXW \_ force 旗標。</span><span class="sxs-lookup"><span data-stu-id="9fd1e-113">To force all applications to terminate, use [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex), and specify the EXW\_FORCE flag.</span></span> <span data-ttu-id="9fd1e-114">這可防止系統傳送 [**WM 的 \_ QUERYENDSESSION**](wm-queryendsession.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="9fd1e-114">This prevents the system from sending [**WM\_QUERYENDSESSION**](wm-queryendsession.md) messages.</span></span>

<span data-ttu-id="9fd1e-115">系統也會在登出作業期間，將 CTRL \_ 登出 \_ 事件控制信號傳送至每個進程。</span><span class="sxs-lookup"><span data-stu-id="9fd1e-115">The system also sends the CTRL\_LOGOFF\_EVENT control signal to every process during a log-off operation.</span></span> <span data-ttu-id="9fd1e-116">主控台應用程式可以註冊 [**HandlerRoutine**](/windows/console/handlerroutine) 來處理這些訊息。</span><span class="sxs-lookup"><span data-stu-id="9fd1e-116">A console application can register a [**HandlerRoutine**](/windows/console/handlerroutine) to process these messages.</span></span>

<span data-ttu-id="9fd1e-117">如果呼叫 [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) 的進程在互動式使用者的登入會話中執行，登入會話中的所有處理常式都會終止。</span><span class="sxs-lookup"><span data-stu-id="9fd1e-117">If the process that called [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) is running in the logon session of the interactive user, all processes in the logon session are terminated.</span></span> <span data-ttu-id="9fd1e-118">如果呼叫 **ExitWindowsEx** 的進程在其他登入會話中，則只會發出通知;沒有進程終止。</span><span class="sxs-lookup"><span data-stu-id="9fd1e-118">If the process calling **ExitWindowsEx** is in some other logon session, only the notifications are made; no processes are terminated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9fd1e-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="9fd1e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fd1e-120">如何登出目前的使用者</span><span class="sxs-lookup"><span data-stu-id="9fd1e-120">How to Log Off the Current User</span></span>](how-to-log-off-the-current-user.md)
</dt> </dl>

 

 
