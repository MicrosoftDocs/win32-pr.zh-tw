---
title: 用戶端服務作業
ms.assetid: 9d6e2441-91de-4108-b1c4-282fbca5fe7c
description: 深入瞭解：用戶端服務作業
keywords:
- Windows 的用戶端服務作業 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73ccbb0c742d0be09570b0959c9c1a663d7f4d0f054cc88070d842ac6d954ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657298"
---
# <a name="client-side-service-operations"></a>用戶端服務作業

以下是用戶端服務作業的版面配置：

-   [WS \_服務 \_ proxy](ws-service-proxy.md) \* serviceProxy：用於呼叫的[服務 proxy](service-proxy.md) 。
-   [WS \_堆積](ws-heap.md) \* 堆積：必要的堆積，用於進行[ \_ 訊息](ws-message.md)的主體序列化和還原序列化。
-   服務作業參數：與服務作業相關的參數。
-   [**呼叫屬性及其計數**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property)：呼叫屬性的陣列。
-   [**呼叫**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property) 屬性計數：呼叫屬性的計數。
-   [**WS \_非同步 \_ 內容**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) asyncCoNtext：非同步執行呼叫的非同步內容。
-   [WS \_錯誤](ws-error.md) 錯誤： Rich error 物件。


### <a name="signature-for-client-side-service-operations"></a>用戶端服務作業的簽章

``` syntax
typedef HRESULT(CALLBACK *ICalculator_Add)(WS_SERVICE_PROXY* serviceProxy, 
                                           WS_HEAP* heap, 
                                           ULONG a, ULONG b, ULONG* result, 
                                           const WS_CALL_PROPERTY* callProperties, 
                                           const ULONG callPropertyCount, 
                                           const WS_ASYNC_CONTEXT* asyncContext, 
                                           WS_ERROR* error);
```

### <a name="memory-considerations-for-client-side-service-operations"></a>用戶端服務作業的記憶體考慮

對服務作業的呼叫會採用[WS \_ 堆積](ws-heap.md) \* 做為參數。 這是必要參數，用於將訊息內文序列化/還原序列化為參數。

應用程式必須呼叫 [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) ，指出呼叫是否成功。 如果呼叫成功，而且它有傳出參數，應用程式應該在完成時，立即呼叫 **WsResetHeap** ，然後再使用外寄參數。

應用程式應該使用 [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc)為 in 和 out 參數配置記憶體。 服務 proxy 可能需要重新配置它們，以便覆寫提供的指標。 嘗試釋放這類記憶體會導致應用程式損毀。

### <a name="client-side-service-operation-and-ws_heap"></a>用戶端服務操作和 WS \_ 堆積

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

### <a name="error-parameter"></a>Error 參數

應用程式應該一律將錯誤參數傳入：

-   如果在服務操作呼叫期間發生失敗，請取得豐富的錯誤資訊。
-   如果服務傳回錯誤，請取得錯誤物件。 錯誤包含在錯誤物件中。 在此情況下，從服務作業傳回的 **HRESULT** 值為 **WS \_ E \_ 端點 \_ 錯誤 \_** (請參閱 [Windows Web 服務傳回值](windows-web-services-return-values.md)) 。

### <a name="call-properties-for-client-side-service-operations"></a>呼叫用戶端服務作業的屬性

呼叫屬性可讓應用程式指定指定之呼叫的自訂設定。 目前只有一個呼叫屬性可用於服務模型、 [**WS \_ 呼叫 \_ 屬性 \_ 呼叫 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id)。

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

### <a name="abandoning-a-call"></a>放棄呼叫

通常最好是放棄呼叫的結果，以便將控制權取回給應用程式，如此一來，實際的呼叫完成就會由基礎結構來處理。 服務 proxy 會透過 [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)提供此功能。

請注意，對呼叫端的控制權可能不會立即傳回，唯一的保證是服務 proxy 執行時間所提供的，就是它不會等待任何 i/o 系結作業完成，然後再將控制權授與呼叫端。

呼叫 [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)時，可以放棄用戶端服務作業上的呼叫。 它會採用服務 proxy 和呼叫識別碼。呼叫識別碼是在服務作業的呼叫屬性中提供。

如果呼叫識別碼為0，則服務 proxy 將放棄該實例上所有暫止的呼叫。

### <a name="call-timeouts"></a>呼叫超時

根據預設，每個呼叫的服務 proxy 都有30秒的超時時間。 透過 [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)建立服務 proxy 時， [**WS \_ PROXY \_ property \_ call \_ timeout**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)服務 proxy 屬性可以變更呼叫的超時時間。

到達超時時間之後，就會放棄呼叫。

### <a name="return-values"></a>傳回值

所有成功的 **HRESULT** 值都必須視為成功，而且所有的失敗值都必須視為失敗。 以下是應用程式可能預期的部分 **HRESULT** 值：

-   **WS \_S \_ ASYNC**：呼叫將會以非同步方式完成。
-   >AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR：呼叫已成功完成。
-   **WS \_E 作業已 \_ \_ 放棄**：已放棄呼叫。 錯誤物件包含放棄的原因。
-   **WS \_E \_ 無效 \_** 的作業：服務 proxy 不是處於適當的狀態，無法進行呼叫，請檢查服務 proxy 狀態以找出服務 proxy 的狀態。

如需傳回值的完整清單，請參閱[Windows Web 服務傳回值](windows-web-services-return-values.md)。

### <a name="code-examples"></a>程式碼範例

如需程式碼範例，請參閱下列內容：

-   [CallAbandonExample](callabandonexample.md)
-   [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)

 

 




