---
description: 系統會將一組預設裝置變更事件廣播至所有應用程式和服務。
ms.assetid: 672ad753-210b-41c3-b8c7-e041ce7b1671
title: 裝置通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7caeee8ba50a62a3bc393172347be09d1ac58085
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111177"
---
# <a name="device-notifications"></a><span data-ttu-id="6eebf-103">裝置通知</span><span class="sxs-lookup"><span data-stu-id="6eebf-103">Device Notifications</span></span>

<span data-ttu-id="6eebf-104">系統會將一組預設裝置變更事件廣播至所有應用程式和服務。</span><span class="sxs-lookup"><span data-stu-id="6eebf-104">The system broadcasts a set of default device change events to all applications and services.</span></span> <span data-ttu-id="6eebf-105">您不需要註冊來接收這些預設事件。</span><span class="sxs-lookup"><span data-stu-id="6eebf-105">You do not need to register to receive these default events.</span></span> <span data-ttu-id="6eebf-106">如需詳細資訊，請參閱 [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) 中的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="6eebf-106">See the Remarks section in [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) for details.</span></span> <span data-ttu-id="6eebf-107">若要指定您的應用程式或服務應該接收的其他事件，請使用 **RegisterDeviceNotification** 函數。</span><span class="sxs-lookup"><span data-stu-id="6eebf-107">To specify other events your application or service should receive, use the **RegisterDeviceNotification** function.</span></span>

<span data-ttu-id="6eebf-108">當應用程式或服務呼叫 [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)時，它也會指定將接收通知事件的視窗。</span><span class="sxs-lookup"><span data-stu-id="6eebf-108">When an application or service calls [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), it also specifies the window that will receive the notification events.</span></span> <span data-ttu-id="6eebf-109">服務可以指定服務狀態控制碼，而不是視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="6eebf-109">Services can specify a service status handle instead of a window handle.</span></span> <span data-ttu-id="6eebf-110">如果服務指定其服務狀態控制碼，則其服務控制處理常式會收到通知事件。</span><span class="sxs-lookup"><span data-stu-id="6eebf-110">If a service specifies its service status handle, its service control handler will receive the notification events.</span></span> <span data-ttu-id="6eebf-111">如需詳細資訊，請參閱 [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex)。</span><span class="sxs-lookup"><span data-stu-id="6eebf-111">For more information, see [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).</span></span>

<span data-ttu-id="6eebf-112">請務必儘快處理隨插即用的裝置事件。</span><span class="sxs-lookup"><span data-stu-id="6eebf-112">Be sure to handle Plug and Play device events as quickly as possible.</span></span> <span data-ttu-id="6eebf-113">否則，系統可能會變成沒有回應。</span><span class="sxs-lookup"><span data-stu-id="6eebf-113">Otherwise, the system may become unresponsive.</span></span> <span data-ttu-id="6eebf-114">如果您的事件處理常式是執行可能會封鎖執行 (例如 i/o) 的作業，最好先啟動另一個執行緒，以非同步方式執行作業。</span><span class="sxs-lookup"><span data-stu-id="6eebf-114">If your event handler is to perform an operation that may block execution (such as I/O), it is best to start another thread to perform the operation asynchronously.</span></span>

<span data-ttu-id="6eebf-115">當您不再需要 [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) 時，必須呼叫 [**UnregisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) 函式來關閉裝置通知控制碼。</span><span class="sxs-lookup"><span data-stu-id="6eebf-115">Device notification handles returned by [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) must be closed by calling the [**UnregisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) function when they are no longer needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6eebf-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="6eebf-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6eebf-117">註冊裝置通知</span><span class="sxs-lookup"><span data-stu-id="6eebf-117">Registering for device notification</span></span>](registering-for-device-notification.md)
</dt> </dl>

 

 
