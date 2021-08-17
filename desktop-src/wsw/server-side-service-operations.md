---
title: 伺服器端服務作業
description: 本節說明服務端服務作業。
ms.assetid: d209cf2f-47f5-4025-8af4-1626c867a66a
keywords:
- Windows 的伺服器端服務作業 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f1656e56df08d00a0551946c4e52898beccd4d1a37a5bd96c63eb2066928fe1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119344628"
---
# <a name="server-side-service-operations"></a>伺服器端服務作業

本節說明服務端服務作業。


以下是伺服器端服務作業的版面配置

-   const [WS \_ 作業 \_ ](ws-operation-context.md)內容內容 \* ：作業[內容](context.md)。
-   服務作業參數：與服務作業相關的參數。
-   const [**WS \_ ASYNC \_ coNtext**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) \* asyncCoNtext：非同步執行服務作業的非同步內容。
-   [WS \_錯誤](ws-error.md) \* 錯誤： Rich error 物件。

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

## <a name="fault-and-error-handling"></a>錯誤和錯誤處理

伺服器端應該使用錯誤將錯誤狀況傳遞給用戶端。 它可以藉由傳回失敗的 HRESULT 並將錯誤內嵌在錯誤物件中。

如果錯誤物件上未設定錯誤，而且傳回失敗 HRESULT，則基礎結構會嘗試將錯誤傳遞回用戶端。 在這種情況下，對用戶端公開的詳細資料層級是由 [服務主機](service-host.md)上的 [**WS \_ 服務 \_ 屬性 \_ 錯誤 \_ 洩漏**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id)服務屬性所控制。

## <a name="call-completion"></a>呼叫完成

當同步伺服器端服務作業已將控制權傳回給服務主機時，就會被視為已完成的呼叫。 針對非同步服務作業，一旦服務作業執行發出回呼通知，就會將呼叫視為已完成。

## <a name="call-lifetime"></a>呼叫存留期

在執行伺服器端服務作業的存留期時，應特別注意。 呼叫的存留期可能會大幅影響服務主機關機所需的時間。

如果伺服器端服務作業預期因為某些 IO 系結作業而封鎖，建議它註冊取消回呼，以便在服務主機被中止時或用戶端關閉基礎連接時收到通知。

## <a name="server-side-service-operations-and-memory-consideration"></a>伺服器端服務作業和記憶體考慮

如果服務作業需要為其外寄參數配置記憶體，它應該使用可透過[ws 作業 \_ \_ 內容](ws-operation-context.md)取得的[ws \_ 堆積](ws-heap.md)物件。

範例：服務作業和 WS \_ 堆積

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

## <a name="return-values"></a>傳回值

-   WS \_ S \_ Async：呼叫將會以非同步完成。
-   WS-ADDRESSING \_ \_ END：呼叫已成功完成，伺服器不會預期來自用戶端的任何 [WS \_ 訊息](ws-message.md) 超出此呼叫的範圍。 如果另一個 WS \_ 訊息傳入，則伺服器應該中止通道。
-   >AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR/所有其他成功 HRESULT：呼叫已成功完成。 請注意，如果服務作業成功完成，建議應用程式不應該傳回 HRESULT，然後 >AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR。
-   具有失敗 HRESULT 的所有專案：錯誤會傳回給用戶端（如果 WS 錯誤有提供的話） \_ 。 否則，會將一般錯誤傳送回用戶端。 請參閱上述的錯誤討論。

請參閱， [呼叫取消](call-cancellation.md)。

 

 




