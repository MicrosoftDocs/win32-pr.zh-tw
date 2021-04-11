---
title: 作業內容存留期和執行緒
description: 作業內容的存留期（以 WS 作業 \_ \_ 內容控制碼表示）會決定它所包含之屬性的存留期。
ms.assetid: 37caf382-2b33-464d-b6c1-e4bd3271a5aa
keywords:
- 適用于 Windows 的操作內容存留期和執行緒 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ea27b0b1dc41ccd029df7d726fe92631adc1ee4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103684252"
---
# <a name="operation-context-lifetime-and-threading"></a><span data-ttu-id="27a39-106">作業內容存留期和執行緒</span><span class="sxs-lookup"><span data-stu-id="27a39-106">Operation Context Lifetime and Threading</span></span>

<span data-ttu-id="27a39-107">作業內容的存留期（以 [WS 作業 \_ \_ 內容](ws-operation-context.md) 控制碼表示）會決定它所包含之屬性的存留期。</span><span class="sxs-lookup"><span data-stu-id="27a39-107">The lifetime of the operation context, represented by a [WS\_OPERATION\_CONTEXT](ws-operation-context.md) handle, determines the lifetime of the properties it contains.</span></span> <span data-ttu-id="27a39-108">因此，應該只在 [服務](service-operation.md) 作業的存留期內或其提供的回呼中使用內容。</span><span class="sxs-lookup"><span data-stu-id="27a39-108">Therefore, a context should only be used within the lifetime of the [service operation](service-operation.md) or the callback to which its provided.</span></span> <span data-ttu-id="27a39-109">同步呼叫的存留期是函數本身的執行。</span><span class="sxs-lookup"><span data-stu-id="27a39-109">The lifetime of a synchronous call is the execution of function itself.</span></span> <span data-ttu-id="27a39-110">若為非同步呼叫，存留期會在非同步呼叫完成後結束。</span><span class="sxs-lookup"><span data-stu-id="27a39-110">For an asynchronous call the lifetime ends once the asynchronous call is completed.</span></span> <span data-ttu-id="27a39-111">一旦呼叫完成後，服務模型不會保證內容。</span><span class="sxs-lookup"><span data-stu-id="27a39-111">The Service Model gives no guarantees about the context once the call is completed.</span></span> <span data-ttu-id="27a39-112">依賴作業內容或其任何屬性超過其存留期的行為未定義。</span><span class="sxs-lookup"><span data-stu-id="27a39-112">The behavior of relying on operation context or any of its properties beyond its lifetime is undefined.</span></span>


<span data-ttu-id="27a39-113">另請參閱以會話為基礎的計算機範例， [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md)。</span><span class="sxs-lookup"><span data-stu-id="27a39-113">See also, the session based calculator example, [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md).</span></span>

## <a name="threading-model"></a><span data-ttu-id="27a39-114">執行緒模型</span><span class="sxs-lookup"><span data-stu-id="27a39-114">Threading Model</span></span>

<span data-ttu-id="27a39-115">作業內容支援無限制執行緒，不過，這對作業內容本身而言是正確的，而且不會套用至它所包含的任何屬性。</span><span class="sxs-lookup"><span data-stu-id="27a39-115">The operation context supports free threading, however this is true of the operation context itself and does not apply to any of the properties it contains.</span></span>

<span data-ttu-id="27a39-116">當您透過 [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) 函式註冊服務作業的取消回呼時，請注意，第一次註冊將會成功;不過，將取消回呼設定多次會失敗。</span><span class="sxs-lookup"><span data-stu-id="27a39-116">When you register a cancel callback for a service operation through the [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) function, note that the first registration will succeed; setting the cancel callback multiple times, however, will fail.</span></span>

 

 




