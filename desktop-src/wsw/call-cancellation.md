---
title: 呼叫取消
description: 呼叫取消通知會取消伺服器端服務作業和服務模型回呼的操作。
ms.assetid: dc371921-869f-4775-98d3-80a1006358ba
keywords:
- 呼叫 Windows 的取消 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5107f9ece421a3130f99c78b3b33788ee6c7e9f0
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "106969741"
---
# <a name="call-cancellation"></a><span data-ttu-id="73e02-106">呼叫取消</span><span class="sxs-lookup"><span data-stu-id="73e02-106">Call cancellation</span></span>

<span data-ttu-id="73e02-107">呼叫取消通知會取消 [伺服器端服務作業](server-side-service-operations.md) 和服務模型回呼的操作。</span><span class="sxs-lookup"><span data-stu-id="73e02-107">Call cancellation notification cancels the operation of [server side service operations](server-side-service-operations.md) and service-model callbacks.</span></span> <span data-ttu-id="73e02-108">這類取消的原因有二：</span><span class="sxs-lookup"><span data-stu-id="73e02-108">Such cancellation can be for one of two reasons:</span></span>

-   <span data-ttu-id="73e02-109">因為呼叫 [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost) 函式，所以服務主機已停止作業。</span><span class="sxs-lookup"><span data-stu-id="73e02-109">The service host has stopped operations because of a call to the [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost) function.</span></span>
-   <span data-ttu-id="73e02-110">基礎通道引發錯誤。</span><span class="sxs-lookup"><span data-stu-id="73e02-110">The underlying channel has raised a fault.</span></span>


<span data-ttu-id="73e02-111">若要接收取消通知，服務作業或服務模型回呼必須藉由呼叫 [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel)函式來註冊 [**WS 作業 \_ \_ CANCEL \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)回呼。</span><span class="sxs-lookup"><span data-stu-id="73e02-111">To receive a cancellation notification, the service operation or service-model callback must register a [**WS\_OPERATION\_CANCEL\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) callback by calling the [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) function.</span></span>

<span data-ttu-id="73e02-112">（選擇性）在註冊取消通知的過程中，服務作業或服務模型回呼也可以註冊應用程式特定的狀態資料和 WS 作業 [**的 \_ \_ 可用 \_ 狀態 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) 回呼。</span><span class="sxs-lookup"><span data-stu-id="73e02-112">Optionally, as part of the registering for cancellation notification, the service operation or service-model callback can also register application-specific state data and the [**WS\_OPERATION\_FREE\_STATE\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) callback.</span></span>

<span data-ttu-id="73e02-113">狀態資料可供 [**WS 作業 \_ \_ 取消 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) 回呼使用。</span><span class="sxs-lookup"><span data-stu-id="73e02-113">The state data is made available to the [**WS\_OPERATION\_CANCEL\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) callback.</span></span> <span data-ttu-id="73e02-114">呼叫完成時，會呼叫 [**WS 作業 \_ \_ 可用 \_ 狀態 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) 回呼，讓應用程式有機會釋放狀態資料。</span><span class="sxs-lookup"><span data-stu-id="73e02-114">On call completion, the [**WS\_OPERATION\_FREE\_STATE\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) callback is called to give the application an opportunity to free the state data.</span></span>

<span data-ttu-id="73e02-115">如需程式碼範例，請參閱 [BlockingServiceExample](blockingserviceexample.md)。</span><span class="sxs-lookup"><span data-stu-id="73e02-115">For a code example, see [BlockingServiceExample](blockingserviceexample.md).</span></span>

<span data-ttu-id="73e02-116">在 [伺服器端服務作業](server-side-service-operations.md) 或回呼函數的存留期內，取消回呼只會呼叫一次。</span><span class="sxs-lookup"><span data-stu-id="73e02-116">The cancellation callback is called only once for the lifetime of the [server side service operations](server-side-service-operations.md) or callback function.</span></span>

<span data-ttu-id="73e02-117">使用 [WS 作業 \_ \_ 內容](ws-operation-context.md) 做為參數的所有服務主機回呼都可以使用呼叫取消。</span><span class="sxs-lookup"><span data-stu-id="73e02-117">Call cancellation is available in for all service host callbacks that take [WS\_OPERATION\_CONTEXT](ws-operation-context.md) as a parameter.</span></span>

<span data-ttu-id="73e02-118">下列 API 元素與呼叫取消有關。</span><span class="sxs-lookup"><span data-stu-id="73e02-118">The following API elements relate to call cancellation.</span></span>

| <span data-ttu-id="73e02-119">回呼</span><span class="sxs-lookup"><span data-stu-id="73e02-119">Callback</span></span>                                                                         | <span data-ttu-id="73e02-120">Description</span><span class="sxs-lookup"><span data-stu-id="73e02-120">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73e02-121">**WS \_ 操作 \_ 取消 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="73e02-121">**WS\_OPERATION\_CANCEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)          | <span data-ttu-id="73e02-122">由服務模型叫用，以通知因服務主機中止關機而取消非同步服務作業。</span><span class="sxs-lookup"><span data-stu-id="73e02-122">Invoked by service model to notify a cancellation of an asynchronous service operation as a result of an aborted shutdown of service host.</span></span> |
| [<span data-ttu-id="73e02-123">**WS \_ 作業 \_ 可用 \_ 狀態 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="73e02-123">**WS\_OPERATION\_FREE\_STATE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) | <span data-ttu-id="73e02-124">由服務模型叫用，以允許應用程式清除以取消回呼註冊的狀態資料。</span><span class="sxs-lookup"><span data-stu-id="73e02-124">Invoked by service model to allow an application to clean up state data that was registered with the cancellation callback.</span></span>                |



 



| <span data-ttu-id="73e02-125">函式</span><span class="sxs-lookup"><span data-stu-id="73e02-125">Function</span></span>                                                             | <span data-ttu-id="73e02-126">描述</span><span class="sxs-lookup"><span data-stu-id="73e02-126">Description</span></span>                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73e02-127">**WsRegisterOperationForCancel**</span><span class="sxs-lookup"><span data-stu-id="73e02-127">**WsRegisterOperationForCancel**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) | <span data-ttu-id="73e02-128">允許服務作業或服務模型回呼註冊取消通知。</span><span class="sxs-lookup"><span data-stu-id="73e02-128">Allows a service operation or service-model callback to register for a cancellation notification.</span></span> |



 

 

 




