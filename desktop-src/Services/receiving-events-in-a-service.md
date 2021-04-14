---
description: 做為主控台應用程式的服務可以註冊主控台控制處理常式，以便在使用者登出時收到通知。
ms.assetid: 86ace8b8-c1cb-4646-bc92-86bd578a82c5
title: 接收服務中的事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b95f7329383ffc8aea08102a2fe8cf8b49e0ef9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514048"
---
# <a name="receiving-events-in-a-service"></a><span data-ttu-id="2696e-103">接收服務中的事件</span><span class="sxs-lookup"><span data-stu-id="2696e-103">Receiving Events in a Service</span></span>

<span data-ttu-id="2696e-104">做為主控台應用程式的服務可以註冊 [主控台控制處理常式](/windows/console/console-control-handlers) ，以便在使用者登出時收到通知。</span><span class="sxs-lookup"><span data-stu-id="2696e-104">A service that is a console application can register a [console control handler](/windows/console/console-control-handlers) to receive notification when a user logs off.</span></span> <span data-ttu-id="2696e-105">不過，當互動式使用者登入時，並不會傳送任何的主控台事件。</span><span class="sxs-lookup"><span data-stu-id="2696e-105">However, there is no console event sent when an interactive user logs on.</span></span> <span data-ttu-id="2696e-106">如需使用者登入時收到通知的相關資訊，請參閱 [建立 Winlogon 通知套件](/windows/desktop/SecAuthN/creating-a-winlogon-notification-package)。</span><span class="sxs-lookup"><span data-stu-id="2696e-106">For information on receiving notification when a user logs on, see [Creating a Winlogon Notification Package](/windows/desktop/SecAuthN/creating-a-winlogon-notification-package).</span></span>

<span data-ttu-id="2696e-107">系統會將裝置變更事件廣播到所有服務。</span><span class="sxs-lookup"><span data-stu-id="2696e-107">The system broadcasts device change events to all services.</span></span> <span data-ttu-id="2696e-108">服務可以在視窗程式或其服務控制處理常式中接收這些事件。</span><span class="sxs-lookup"><span data-stu-id="2696e-108">These events can be received by a service in a window procedure or in its service control handler.</span></span> <span data-ttu-id="2696e-109">若要指定您的服務應該接收哪些事件，請使用 [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) 函數。</span><span class="sxs-lookup"><span data-stu-id="2696e-109">To specify which events your service should receive, use the [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) function.</span></span>

<span data-ttu-id="2696e-110">請務必儘快處理隨插即用的裝置事件。</span><span class="sxs-lookup"><span data-stu-id="2696e-110">Be sure to handle Plug and Play device events as quickly as possible.</span></span> <span data-ttu-id="2696e-111">否則，系統可能會變成沒有回應。</span><span class="sxs-lookup"><span data-stu-id="2696e-111">Otherwise, the system may become unresponsive.</span></span> <span data-ttu-id="2696e-112">如果您的事件處理常式是執行可能會封鎖執行 (例如 i/o) 的作業，最好先啟動另一個執行緒，以非同步方式執行作業。</span><span class="sxs-lookup"><span data-stu-id="2696e-112">If your event handler is to perform an operation that may block execution (such as I/O), it is best to start another thread to perform the operation asynchronously.</span></span>

<span data-ttu-id="2696e-113">當服務呼叫 [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa)時，服務也會指定視窗控制碼或服務狀態控制碼。</span><span class="sxs-lookup"><span data-stu-id="2696e-113">When a service calls [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa), the service also specifies either a window handle or a service status handle.</span></span> <span data-ttu-id="2696e-114">如果服務指定視窗控制碼，則視窗程式會收到通知事件。</span><span class="sxs-lookup"><span data-stu-id="2696e-114">If a service specifies a window handle, the window procedure receives the notification events.</span></span> <span data-ttu-id="2696e-115">如果服務指定其服務狀態控制碼，則其服務控制處理常式會收到通知事件。</span><span class="sxs-lookup"><span data-stu-id="2696e-115">If a service specifies its service status handle, its service control handler receives the notification events.</span></span> <span data-ttu-id="2696e-116">如需詳細資訊，請參閱 [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex)。</span><span class="sxs-lookup"><span data-stu-id="2696e-116">For more information, see [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex).</span></span>

<span data-ttu-id="2696e-117">當您不再需要 [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) 時，必須呼叫 [**UnregisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-unregisterdevicenotification) 函式來關閉裝置通知控制碼。</span><span class="sxs-lookup"><span data-stu-id="2696e-117">Device notification handles returned by [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) must be closed by calling the [**UnregisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-unregisterdevicenotification) function when they are no longer needed.</span></span>

 

 
