---
title: 伺服器端服務作業
description: 本節說明服務端服務作業。
ms.assetid: d209cf2f-47f5-4025-8af4-1626c867a66a
keywords:
- 適用于 Windows 的伺服器端服務作業 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c7ad5a327c1cb79278aa562bfaa1753f008a542
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383298"
---
# <a name="server-side-service-operations"></a><span data-ttu-id="f02c2-106">伺服器端服務作業</span><span class="sxs-lookup"><span data-stu-id="f02c2-106">Server Side Service Operations</span></span>

<span data-ttu-id="f02c2-107">本節說明服務端服務作業。</span><span class="sxs-lookup"><span data-stu-id="f02c2-107">This section describes service side service operations.</span></span>


<span data-ttu-id="f02c2-108">以下是伺服器端服務作業的版面配置</span><span class="sxs-lookup"><span data-stu-id="f02c2-108">The following is the layout of a server side service operation</span></span>

-   <span data-ttu-id="f02c2-109">const [WS \_ 作業 \_ ](ws-operation-context.md)內容內容 \* ：作業[內容](context.md)。</span><span class="sxs-lookup"><span data-stu-id="f02c2-109">const [WS\_OPERATION\_CONTEXT](ws-operation-context.md)\* context: The operation [context](context.md).</span></span>
-   <span data-ttu-id="f02c2-110">服務作業參數：與服務作業相關的參數。</span><span class="sxs-lookup"><span data-stu-id="f02c2-110">Service Operations Parameters: Parameters pertaining to the service operation.</span></span>
-   <span data-ttu-id="f02c2-111">const [**WS \_ ASYNC \_ coNtext**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) \* asyncCoNtext：非同步執行服務作業的非同步內容。</span><span class="sxs-lookup"><span data-stu-id="f02c2-111">const [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)\* asyncContext: Async context for executing the service operations asynchronously.</span></span>
-   <span data-ttu-id="f02c2-112">[WS \_錯誤](ws-error.md) \* 錯誤： Rich error 物件。</span><span class="sxs-lookup"><span data-stu-id="f02c2-112">[WS\_ERROR](ws-error.md)\* error: Rich error object.</span></span>

``` syntax
HRESULT CALLBACK Add(const WS_OPERATION_CONTEXT* context, 
                     ULONG a, ULONG b, ULONG* result, 
                     const WS_ASYNC_CONTEXT* asyncContext, 
                     WS_ERROR* error)
{
    *result = a +b;
    return NOERROR;
}
```

## <a name="fault-and-error-handling"></a><span data-ttu-id="f02c2-113">錯誤和錯誤處理</span><span class="sxs-lookup"><span data-stu-id="f02c2-113">Fault And Error Handling</span></span>

<span data-ttu-id="f02c2-114">伺服器端應該使用錯誤將錯誤狀況傳遞給用戶端。</span><span class="sxs-lookup"><span data-stu-id="f02c2-114">The server side should use faults to deliver error conditions to the client.</span></span> <span data-ttu-id="f02c2-115">它可以藉由傳回失敗的 HRESULT 並將錯誤內嵌在錯誤物件中。</span><span class="sxs-lookup"><span data-stu-id="f02c2-115">It can do so by returning a failing HRESULT and embedding the fault in the error object.</span></span>

<span data-ttu-id="f02c2-116">如果錯誤物件上未設定錯誤，而且傳回失敗 HRESULT，則基礎結構會嘗試將錯誤傳遞回用戶端。</span><span class="sxs-lookup"><span data-stu-id="f02c2-116">If the fault is not set on the error object and a failure HRESULT is returned, the infrastructure will attempt deliver a fault back to client.</span></span> <span data-ttu-id="f02c2-117">在這種情況下，對用戶端公開的詳細資料層級是由 [服務主機](service-host.md)上的 [**WS \_ 服務 \_ 屬性 \_ 錯誤 \_ 洩漏**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id)服務屬性所控制。</span><span class="sxs-lookup"><span data-stu-id="f02c2-117">The level of details disclosed to the client in such a case is controlled by [**WS\_SERVICE\_PROPERTY\_FAULT\_DISCLOSURE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) service property on the [Service Host](service-host.md).</span></span>

## <a name="call-completion"></a><span data-ttu-id="f02c2-118">呼叫完成</span><span class="sxs-lookup"><span data-stu-id="f02c2-118">Call Completion</span></span>

<span data-ttu-id="f02c2-119">當同步伺服器端服務作業已將控制權傳回給服務主機時，就會被視為已完成的呼叫。</span><span class="sxs-lookup"><span data-stu-id="f02c2-119">A call on a synchronous server side service operation is said to be complete when either it has returned control back to the service host.</span></span> <span data-ttu-id="f02c2-120">針對非同步服務作業，一旦服務作業執行發出回呼通知，就會將呼叫視為已完成。</span><span class="sxs-lookup"><span data-stu-id="f02c2-120">For an asynchronous service operation a call is considered complete once the callback notification is issued by the service operation implementation.</span></span>

## <a name="call-lifetime"></a><span data-ttu-id="f02c2-121">呼叫存留期</span><span class="sxs-lookup"><span data-stu-id="f02c2-121">Call Lifetime</span></span>

<span data-ttu-id="f02c2-122">在執行伺服器端服務作業的存留期時，應特別注意。</span><span class="sxs-lookup"><span data-stu-id="f02c2-122">Special care should be taken when implementing a server side service operation about its lifetime.</span></span> <span data-ttu-id="f02c2-123">呼叫的存留期可能會大幅影響服務主機關機所需的時間。</span><span class="sxs-lookup"><span data-stu-id="f02c2-123">The lifetime of a call can greatly affect how long the service host takes to shutdown.</span></span>

<span data-ttu-id="f02c2-124">如果伺服器端服務作業預期因為某些 IO 系結作業而封鎖，建議它註冊取消回呼，以便在服務主機被中止時或用戶端關閉基礎連接時收到通知。</span><span class="sxs-lookup"><span data-stu-id="f02c2-124">If a server side service operation is expected to block because of some IO bound operation, it is recommended that it registers a cancellation callback such that it is notified if when service host is being aborted, or when the underlying connection is closed by the client.</span></span>

## <a name="server-side-service-operations-and-memory-consideration"></a><span data-ttu-id="f02c2-125">伺服器端服務作業和記憶體考慮</span><span class="sxs-lookup"><span data-stu-id="f02c2-125">Server side service operations and memory consideration</span></span>

<span data-ttu-id="f02c2-126">如果服務作業需要為其外寄參數配置記憶體，它應該使用可透過[ws 作業 \_ \_ 內容](ws-operation-context.md)取得的[ws \_ 堆積](ws-heap.md)物件。</span><span class="sxs-lookup"><span data-stu-id="f02c2-126">If a service operation needs to allocate memory for its outgoing parameters, it should use [WS\_HEAP](ws-heap.md) object available to it through the [WS\_OPERATION\_CONTEXT](ws-operation-context.md).</span></span>

<span data-ttu-id="f02c2-127">範例：服務作業和 WS \_ 堆積</span><span class="sxs-lookup"><span data-stu-id="f02c2-127">Example: Service Operation and WS\_HEAP</span></span>

``` syntax
HRESULT CALLBACK ProcessOrder (const WS_OPERATION_CONTEXT* context, const ULONG orderNumber, OrderReceipt** orderReceipt, const WS_ASYNC_CONTEXT* asyncContext, WS_ERROR* error)
{
    WS_HEAP* heap;
    HRESULT hr = WsGetOperationContextProperty (context, WS_OPERATION_CONTEXT_PROPERTY_HEAP, &heap, sizeof(heap), NULL, error);
    if (FAILED(hr))
        return hr;
    hr = WsAlloc(heap, sizeof (OrderReceipt), orderReceipt, error);
    if (FAILED(hr))
        return hr;
    hr = FillInReceipt(*orderReceipt);
    if (FAILED(hr))
        return hr;
    return NOERROR;
} 
```

## <a name="return-values"></a><span data-ttu-id="f02c2-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="f02c2-128">Return Values</span></span>

-   <span data-ttu-id="f02c2-129">WS \_ S \_ Async：呼叫將會以非同步完成。</span><span class="sxs-lookup"><span data-stu-id="f02c2-129">WS\_S\_ASYNC: Call will be completed async.</span></span>
-   <span data-ttu-id="f02c2-130">WS-ADDRESSING \_ \_ END：呼叫已成功完成，伺服器不會預期來自用戶端的任何 [WS \_ 訊息](ws-message.md) 超出此呼叫的範圍。</span><span class="sxs-lookup"><span data-stu-id="f02c2-130">WS\_S\_END: Call completed successfully, the server is not expecting any [WS\_MESSAGE](ws-message.md) from the client beyond this call.</span></span> <span data-ttu-id="f02c2-131">如果另一個 WS \_ 訊息傳入，則伺服器應該中止通道。</span><span class="sxs-lookup"><span data-stu-id="f02c2-131">If another WS\_MESSAGE comes in then the server should abort the channel.</span></span>
-   <span data-ttu-id="f02c2-132">>AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR/所有其他成功 HRESULT：呼叫已成功完成。</span><span class="sxs-lookup"><span data-stu-id="f02c2-132">NOERROR/All other success HRESULTS: Call completed successfully.</span></span> <span data-ttu-id="f02c2-133">請注意，如果服務作業成功完成，建議應用程式不應該傳回 HRESULT，然後 >AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR。</span><span class="sxs-lookup"><span data-stu-id="f02c2-133">Note that it is recommended that the application should not return HRESULT other then NOERROR for successful completion of service operation.</span></span>
-   <span data-ttu-id="f02c2-134">具有失敗 HRESULT 的所有專案：錯誤會傳回給用戶端（如果 WS 錯誤有提供的話） \_ 。</span><span class="sxs-lookup"><span data-stu-id="f02c2-134">Everything with a failure HRESULT: A fault is send back to the client if one is available in WS\_ERROR.</span></span> <span data-ttu-id="f02c2-135">否則，會將一般錯誤傳送回用戶端。</span><span class="sxs-lookup"><span data-stu-id="f02c2-135">Otherwise a generic fault is send back to the client.</span></span> <span data-ttu-id="f02c2-136">請參閱上述的錯誤討論。</span><span class="sxs-lookup"><span data-stu-id="f02c2-136">See fault discussion above.</span></span>

<span data-ttu-id="f02c2-137">請參閱， [呼叫取消](call-cancellation.md)。</span><span class="sxs-lookup"><span data-stu-id="f02c2-137">See, [Call cancellation](call-cancellation.md).</span></span>

 

 




