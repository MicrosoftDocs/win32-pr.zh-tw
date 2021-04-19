---
description: 為了將控制項要求傳送至執行中的服務，服務控制程式會使用 ControlService 函數。
ms.assetid: d6cdc876-8b74-460e-ad43-6455ddf428dd
title: 服務控制要求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb5edf56137e2c98ea7db440a4db5e55df5e8f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970794"
---
# <a name="service-control-requests"></a><span data-ttu-id="b263b-103">服務控制要求</span><span class="sxs-lookup"><span data-stu-id="b263b-103">Service Control Requests</span></span>

<span data-ttu-id="b263b-104">為了將控制項要求傳送至執行中的服務，服務控制程式會使用 [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) 函數。</span><span class="sxs-lookup"><span data-stu-id="b263b-104">To send control requests to a running service, a service control program uses the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function.</span></span> <span data-ttu-id="b263b-105">此函式會指定傳遞至指定服務之 [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) 函數的控制項值。</span><span class="sxs-lookup"><span data-stu-id="b263b-105">This function specifies a control value that is passed to the [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) function of the specified service.</span></span> <span data-ttu-id="b263b-106">這個控制項值可以是使用者定義的程式碼，也可以是可讓呼叫程式執行下列動作的其中一個標準程式碼：</span><span class="sxs-lookup"><span data-stu-id="b263b-106">This control value can be a user-defined code, or it can be one of the standard codes that enable the calling program to perform the following actions:</span></span>

-   <span data-ttu-id="b263b-107">停止服務 (服務 \_ 控制 \_ 停止) 。</span><span class="sxs-lookup"><span data-stu-id="b263b-107">Stop a service (SERVICE\_CONTROL\_STOP).</span></span>
-   <span data-ttu-id="b263b-108">暫停服務 (服務 \_ 控制 \_ 暫停) 。</span><span class="sxs-lookup"><span data-stu-id="b263b-108">Pause a service (SERVICE\_CONTROL\_PAUSE).</span></span>
-   <span data-ttu-id="b263b-109">繼續執行暫停的服務 (服務 \_ 控制 \_ 繼續) 。</span><span class="sxs-lookup"><span data-stu-id="b263b-109">Resume executing a paused service (SERVICE\_CONTROL\_CONTINUE).</span></span>
-   <span data-ttu-id="b263b-110">從服務取得更新的狀態資訊 (服務 \_ 控制 \_ 詢問) 。</span><span class="sxs-lookup"><span data-stu-id="b263b-110">Retrieve updated status information from a service (SERVICE\_CONTROL\_INTERROGATE).</span></span>

<span data-ttu-id="b263b-111">每個服務都會指定要接受和處理的控制項值。</span><span class="sxs-lookup"><span data-stu-id="b263b-111">Each service specifies the control values that it will accept and process.</span></span> <span data-ttu-id="b263b-112">若要判斷服務接受哪些標準控制項值，請使用 [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) 函數，或 \_ \_ 在 [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) 函數的呼叫中指定服務控制查閱控制項值。</span><span class="sxs-lookup"><span data-stu-id="b263b-112">To determine which of the standard control values are accepted by a service, use the [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) function or specify the SERVICE\_CONTROL\_INTERROGATE control value in a call to the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function.</span></span> <span data-ttu-id="b263b-113">這些函數所傳回之 [**服務 \_ 狀態**](/windows/desktop/api/Winsvc/ns-winsvc-service_status)結構的 **dwControlsAccepted** 成員會指出服務是否可以停止、暫停或繼續。</span><span class="sxs-lookup"><span data-stu-id="b263b-113">The **dwControlsAccepted** member of the [**SERVICE\_STATUS**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) structure returned by these functions indicates whether the service can be stopped, paused, or resumed.</span></span> <span data-ttu-id="b263b-114">所有服務都接受服務 \_ 控制的查閱 \_ 控制值。</span><span class="sxs-lookup"><span data-stu-id="b263b-114">All services accept the SERVICE\_CONTROL\_INTERROGATE control value.</span></span>

<span data-ttu-id="b263b-115">[**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex)函數會報告指定服務的最新狀態，但不會從服務本身取得更新的狀態。</span><span class="sxs-lookup"><span data-stu-id="b263b-115">The [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) function reports the most recent status for a specified service, but does not get an updated status from the service itself.</span></span> <span data-ttu-id="b263b-116">\_ \_ 在 [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice)呼叫中使用服務控制查閱控制項值，可確保傳回的狀態資訊是最新的。</span><span class="sxs-lookup"><span data-stu-id="b263b-116">Using the SERVICE\_CONTROL\_INTERROGATE control value in a call to [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) ensures that the status information returned is current.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b263b-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="b263b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b263b-118">使用 SC 控制服務</span><span class="sxs-lookup"><span data-stu-id="b263b-118">Controlling a Service Using SC</span></span>](controlling-a-service-using-sc.md)
</dt> </dl>

 

 



