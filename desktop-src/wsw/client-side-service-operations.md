---
title: 用戶端服務作業
ms.assetid: 9d6e2441-91de-4108-b1c4-282fbca5fe7c
description: 深入瞭解：用戶端服務作業
keywords:
- 適用于 Windows 的用戶端服務作業 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4cd00bfbd832db12a722363bf5b1af8f7298345
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193694"
---
# <a name="client-side-service-operations"></a><span data-ttu-id="1dee2-106">用戶端服務作業</span><span class="sxs-lookup"><span data-stu-id="1dee2-106">Client-side Service Operations</span></span>

<span data-ttu-id="1dee2-107">以下是用戶端服務作業的版面配置：</span><span class="sxs-lookup"><span data-stu-id="1dee2-107">The following is the layout of a client-side service operation:</span></span>

-   <span data-ttu-id="1dee2-108">[WS \_服務 \_ proxy](ws-service-proxy.md) \* serviceProxy：用於呼叫的[服務 proxy](service-proxy.md) 。</span><span class="sxs-lookup"><span data-stu-id="1dee2-108">[WS\_SERVICE\_PROXY](ws-service-proxy.md)\* serviceProxy: The [service proxy](service-proxy.md) for the call.</span></span>
-   <span data-ttu-id="1dee2-109">[WS \_堆積](ws-heap.md) \* 堆積：必要的堆積，用於進行[ \_ 訊息](ws-message.md)的主體序列化和還原序列化。</span><span class="sxs-lookup"><span data-stu-id="1dee2-109">[WS\_HEAP](ws-heap.md)\* heap: A required heap used for body serialization and deserialization of the [WS\_MESSAGE](ws-message.md).</span></span>
-   <span data-ttu-id="1dee2-110">服務作業參數：與服務作業相關的參數。</span><span class="sxs-lookup"><span data-stu-id="1dee2-110">Service Operations Parameters: Parameters pertaining to the service operation.</span></span>
-   <span data-ttu-id="1dee2-111">[**呼叫屬性及其計數**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property)：呼叫屬性的陣列。</span><span class="sxs-lookup"><span data-stu-id="1dee2-111">[**Call Properties and their count**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property): An array of call properties.</span></span>
-   <span data-ttu-id="1dee2-112">[**呼叫**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property) 屬性計數：呼叫屬性的計數。</span><span class="sxs-lookup"><span data-stu-id="1dee2-112">[**Call**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property) property count: The count of call properties.</span></span>
-   <span data-ttu-id="1dee2-113">[**WS \_非同步 \_ 內容**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) asyncCoNtext：非同步執行呼叫的非同步內容。</span><span class="sxs-lookup"><span data-stu-id="1dee2-113">[**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) asyncContext: Async context for executing the call asynchronously.</span></span>
-   <span data-ttu-id="1dee2-114">[WS \_錯誤](ws-error.md) 錯誤： Rich error 物件。</span><span class="sxs-lookup"><span data-stu-id="1dee2-114">[WS\_ERROR](ws-error.md) error: Rich error object.</span></span>


### <a name="signature-for-client-side-service-operations"></a><span data-ttu-id="1dee2-115">用戶端服務作業的簽章</span><span class="sxs-lookup"><span data-stu-id="1dee2-115">Signature for Client-side Service Operations</span></span>

``` syntax
typedef HRESULT(CALLBACK *ICalculator_Add)(WS_SERVICE_PROXY* serviceProxy, 
                                           WS_HEAP* heap, 
                                           ULONG a, ULONG b, ULONG* result, 
                                           const WS_CALL_PROPERTY* callProperties, 
                                           const ULONG callPropertyCount, 
                                           const WS_ASYNC_CONTEXT* asyncContext, 
                                           WS_ERROR* error);
```

### <a name="memory-considerations-for-client-side-service-operations"></a><span data-ttu-id="1dee2-116">用戶端服務作業的記憶體考慮</span><span class="sxs-lookup"><span data-stu-id="1dee2-116">Memory Considerations for Client-side Service Operations</span></span>

<span data-ttu-id="1dee2-117">對服務作業的呼叫會採用[WS \_ 堆積](ws-heap.md) \* 做為參數。</span><span class="sxs-lookup"><span data-stu-id="1dee2-117">The call to the service operation takes a [WS\_HEAP](ws-heap.md)\* as parameter.</span></span> <span data-ttu-id="1dee2-118">這是必要參數，用於將訊息內文序列化/還原序列化為參數。</span><span class="sxs-lookup"><span data-stu-id="1dee2-118">This is a required parameter used for serialization/deserialization of message bodies to parameters.</span></span>

<span data-ttu-id="1dee2-119">應用程式必須呼叫 [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) ，指出呼叫是否成功。</span><span class="sxs-lookup"><span data-stu-id="1dee2-119">The application must call [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) whether the call succeeded or not.</span></span> <span data-ttu-id="1dee2-120">如果呼叫成功，而且它有傳出參數，應用程式應該在完成時，立即呼叫 **WsResetHeap** ，然後再使用外寄參數。</span><span class="sxs-lookup"><span data-stu-id="1dee2-120">If the call succeeded and it has outgoing parameters, the application should call **WsResetHeap** immediately after it is finished with the outgoing parameters.</span></span>

<span data-ttu-id="1dee2-121">應用程式應該使用 [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc)為 in 和 out 參數配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="1dee2-121">The application should allocate memory for in and out parameters with [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc).</span></span> <span data-ttu-id="1dee2-122">服務 proxy 可能需要重新配置它們，以便覆寫提供的指標。</span><span class="sxs-lookup"><span data-stu-id="1dee2-122">The service proxy may need to reallocate them so provided pointers will be overwritten.</span></span> <span data-ttu-id="1dee2-123">嘗試釋放這類記憶體會導致應用程式損毀。</span><span class="sxs-lookup"><span data-stu-id="1dee2-123">An attempt to free such memory will cause the application to crash.</span></span>

### <a name="client-side-service-operation-and-ws_heap"></a><span data-ttu-id="1dee2-124">用戶端服務操作和 WS \_ 堆積</span><span class="sxs-lookup"><span data-stu-id="1dee2-124">Client-side Service Operation and WS\_HEAP</span></span>

``` syntax
HRESULT hr = IProcessOrder_ProcessOrder(serviceProxy, heap, orderNumber, &orderReceipt, NULL, 0, NULL, error);
if(FAILED(hr))
    goto error;
hr = ProcessReceipt(orderReceipt);
WsResetHeap(heap);
if(FAILED(hr))
    goto error;
hr = IProcessOrder_CompleteOrder(serviceProxy, heap, orderNumber, &orderMemo, NULL, 0, NULL, error);
if(FAILED(hr))
    goto error;
hr = ProcessMemo(orderMemo);
WsResetHeap(heap);
if(FAILED(hr))
    goto error;
```

### <a name="error-parameter"></a><span data-ttu-id="1dee2-125">Error 參數</span><span class="sxs-lookup"><span data-stu-id="1dee2-125">Error parameter</span></span>

<span data-ttu-id="1dee2-126">應用程式應該一律將錯誤參數傳入：</span><span class="sxs-lookup"><span data-stu-id="1dee2-126">The application should always pass in the error parameter to:</span></span>

-   <span data-ttu-id="1dee2-127">如果在服務操作呼叫期間發生失敗，請取得豐富的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="1dee2-127">Get rich error information if a failure occurs during the service operation call.</span></span>
-   <span data-ttu-id="1dee2-128">如果服務傳回錯誤，請取得錯誤物件。</span><span class="sxs-lookup"><span data-stu-id="1dee2-128">Get the fault object if the service returned back a fault.</span></span> <span data-ttu-id="1dee2-129">錯誤包含在錯誤物件中。</span><span class="sxs-lookup"><span data-stu-id="1dee2-129">The fault is contained in the error object.</span></span> <span data-ttu-id="1dee2-130">在此情況下，從服務作業傳回的 **HRESULT** 值為 **WS \_ E \_ 端點 \_ 錯誤 \_** (請參閱 [Windows Web 服務傳回值](windows-web-services-return-values.md)) 。</span><span class="sxs-lookup"><span data-stu-id="1dee2-130">In this case, the **HRESULT** value returned from the service operation is **WS\_E\_ENDPOINT\_FAULT\_RECEIVED** (see [Windows Web Services Return Values](windows-web-services-return-values.md)).</span></span>

### <a name="call-properties-for-client-side-service-operations"></a><span data-ttu-id="1dee2-131">呼叫用戶端服務作業的屬性</span><span class="sxs-lookup"><span data-stu-id="1dee2-131">Call Properties for Client-side Service Operations</span></span>

<span data-ttu-id="1dee2-132">呼叫屬性可讓應用程式指定指定之呼叫的自訂設定。</span><span class="sxs-lookup"><span data-stu-id="1dee2-132">Call properties allow an application to specify custom settings for a given call.</span></span> <span data-ttu-id="1dee2-133">目前只有一個呼叫屬性可用於服務模型、 [**WS \_ 呼叫 \_ 屬性 \_ 呼叫 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id)。</span><span class="sxs-lookup"><span data-stu-id="1dee2-133">Currently, only one call property is available with the service model, [**WS\_CALL\_PROPERTY\_CALL\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id).</span></span>

``` syntax
WS_CALL_PROPERTY callProperties[1] = {0};
callProperties[0].id = WS_CALL_PROPERTY_CALL_ID;
callProperties[0].value = 5;

HRESULT hr = IProcessOrder_ProcessOrder(serviceProxy, heap, orderNumber, &orderReceipt,  callProperties, WsCountOf(callProperties), NULL, error);
if(FAILED(hr))
    goto error;
//:
//:
hr = IProcessOrder_CompleteOrder(serviceProxy, heap, orderNumber, &orderReceipt, callProperties, WsCountOf(callProperties), NULL, error);
if(FAILED(hr))
    goto error;

//:
//:
//:
// On a separate thread 
// In this case both the calls belong to call group 5, and will abandon as a result of the call to WsAbandonCall. 
hr = WsAbandonCall(serviceProxy, 5, error);
```

### <a name="abandoning-a-call"></a><span data-ttu-id="1dee2-134">放棄呼叫</span><span class="sxs-lookup"><span data-stu-id="1dee2-134">Abandoning a Call</span></span>

<span data-ttu-id="1dee2-135">通常最好是放棄呼叫的結果，以便將控制權取回給應用程式，如此一來，實際的呼叫完成就會由基礎結構來處理。</span><span class="sxs-lookup"><span data-stu-id="1dee2-135">It is often desirable to abandon the results of a call in order to relinquish the control back to the application, such that the actual call completion is handled by the infrastructure.</span></span> <span data-ttu-id="1dee2-136">服務 proxy 會透過 [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)提供此功能。</span><span class="sxs-lookup"><span data-stu-id="1dee2-136">Service proxy provides this facility through [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).</span></span>

<span data-ttu-id="1dee2-137">請注意，對呼叫端的控制權可能不會立即傳回，唯一的保證是服務 proxy 執行時間所提供的，就是它不會等待任何 i/o 系結作業完成，然後再將控制權授與呼叫端。</span><span class="sxs-lookup"><span data-stu-id="1dee2-137">Note that the control to the caller may not be given back immediately, the only guarantee that the service proxy runtime gives is that it would not wait for any I/O bound operation to complete before it gives control back to the caller.</span></span>

<span data-ttu-id="1dee2-138">呼叫 [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)時，可以放棄用戶端服務作業上的呼叫。</span><span class="sxs-lookup"><span data-stu-id="1dee2-138">Calls on a client side service operation can be abandoned by means of a call to [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).</span></span> <span data-ttu-id="1dee2-139">它會採用服務 proxy 和呼叫識別碼。呼叫識別碼是在服務作業的呼叫屬性中提供。</span><span class="sxs-lookup"><span data-stu-id="1dee2-139">It takes a service proxy and a call id. A call Id is given as part of a call properties on a service operation.</span></span>

<span data-ttu-id="1dee2-140">如果呼叫識別碼為0，則服務 proxy 將放棄該實例上所有暫止的呼叫。</span><span class="sxs-lookup"><span data-stu-id="1dee2-140">If the call Id is 0, then the service proxy will abandon all pending calls at that instance.</span></span>

### <a name="call-timeouts"></a><span data-ttu-id="1dee2-141">呼叫超時</span><span class="sxs-lookup"><span data-stu-id="1dee2-141">Call Timeouts</span></span>

<span data-ttu-id="1dee2-142">根據預設，每個呼叫的服務 proxy 都有30秒的超時時間。</span><span class="sxs-lookup"><span data-stu-id="1dee2-142">By default a service proxy has a 30 second timeout for every call.</span></span> <span data-ttu-id="1dee2-143">透過 [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)建立服務 proxy 時， [**WS \_ PROXY \_ property \_ call \_ timeout**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)服務 proxy 屬性可以變更呼叫的超時時間。</span><span class="sxs-lookup"><span data-stu-id="1dee2-143">The timeout on a call can be changed by [**WS\_PROXY\_PROPERTY\_CALL\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) service proxy property when creating a service proxy through [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy).</span></span>

<span data-ttu-id="1dee2-144">到達超時時間之後，就會放棄呼叫。</span><span class="sxs-lookup"><span data-stu-id="1dee2-144">After a timeout is reached, the call is abandoned.</span></span>

### <a name="return-values"></a><span data-ttu-id="1dee2-145">傳回值</span><span class="sxs-lookup"><span data-stu-id="1dee2-145">Return Values</span></span>

<span data-ttu-id="1dee2-146">所有成功的 **HRESULT** 值都必須視為成功，而且所有的失敗值都必須視為失敗。</span><span class="sxs-lookup"><span data-stu-id="1dee2-146">All success **HRESULT** values must be treated as success, and all failure values must be treated as failures.</span></span> <span data-ttu-id="1dee2-147">以下是應用程式可能預期的部分 **HRESULT** 值：</span><span class="sxs-lookup"><span data-stu-id="1dee2-147">The following are some of the **HRESULT** values that an application can expect:</span></span>

-   <span data-ttu-id="1dee2-148">**WS \_S \_ ASYNC**：呼叫將會以非同步方式完成。</span><span class="sxs-lookup"><span data-stu-id="1dee2-148">**WS\_S\_ASYNC**: Call will be completed asynchronously.</span></span>
-   <span data-ttu-id="1dee2-149">>AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR：呼叫已成功完成。</span><span class="sxs-lookup"><span data-stu-id="1dee2-149">NOERROR: Call completed successfully.</span></span>
-   <span data-ttu-id="1dee2-150">**WS \_E 作業已 \_ \_ 放棄**：已放棄呼叫。</span><span class="sxs-lookup"><span data-stu-id="1dee2-150">**WS\_E\_OPERATION\_ABANDONED**: The call has been abandoned.</span></span> <span data-ttu-id="1dee2-151">錯誤物件包含放棄的原因。</span><span class="sxs-lookup"><span data-stu-id="1dee2-151">The error object contains the reason for abandon.</span></span>
-   <span data-ttu-id="1dee2-152">**WS \_E \_ 無效 \_** 的作業：服務 proxy 不是處於適當的狀態，無法進行呼叫，請檢查服務 proxy 狀態以找出服務 proxy 的狀態。</span><span class="sxs-lookup"><span data-stu-id="1dee2-152">**WS\_E\_INVALID\_OPERATION**: The service proxy is not in an appropriate state to make a call, check the service proxy state to figure out the state of the service proxy.</span></span>

<span data-ttu-id="1dee2-153">如需傳回值的完整清單，請參閱 [Windows Web 服務傳回值](windows-web-services-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="1dee2-153">For a complete list of return values, see [Windows Web Services Return Values](windows-web-services-return-values.md).</span></span>

### <a name="code-examples"></a><span data-ttu-id="1dee2-154">程式碼範例</span><span class="sxs-lookup"><span data-stu-id="1dee2-154">Code Examples</span></span>

<span data-ttu-id="1dee2-155">如需程式碼範例，請參閱下列內容：</span><span class="sxs-lookup"><span data-stu-id="1dee2-155">For code examples, see the following:</span></span>

-   [<span data-ttu-id="1dee2-156">CallAbandonExample</span><span class="sxs-lookup"><span data-stu-id="1dee2-156">CallAbandonExample</span></span>](callabandonexample.md)
-   [<span data-ttu-id="1dee2-157">**WsAbandonCall**</span><span class="sxs-lookup"><span data-stu-id="1dee2-157">**WsAbandonCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)

 

 




