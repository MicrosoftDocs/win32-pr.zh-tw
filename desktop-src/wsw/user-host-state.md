---
title: 服務主機使用者狀態
description: 服務主機可讓應用程式關聯服務主機層級範圍內的狀態資料。
ms.assetid: e18c6c0c-3205-4f88-9a9b-2515a7cfc462
keywords:
- 適用于 Windows 的使用者主機狀態 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56f43942f7743d28534e0286a45203dc01e0e7b6
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "106965263"
---
# <a name="service-host-user-state"></a><span data-ttu-id="c1021-106">服務主機使用者狀態</span><span class="sxs-lookup"><span data-stu-id="c1021-106">Service Host User State</span></span>

<span data-ttu-id="c1021-107">[服務主機](service-host.md)可讓應用程式關聯服務主機層級範圍內的狀態資料。</span><span class="sxs-lookup"><span data-stu-id="c1021-107">The [service host](service-host.md) enables an application to associate state data that is scoped at the service-host level.</span></span> <span data-ttu-id="c1021-108">此狀態是由當應用程式建立 [服務主機](service-host.md)時傳遞至 [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost)函式的 [**WS \_ 服務 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property)結構所指定，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="c1021-108">This state is is specified by a [**WS\_SERVICE\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) structure that is passed to the [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) function when the application creates a [service host](service-host.md), as illustrated in the following example.</span></span>

``` syntax
void* quotePtr = (void*) quotes;
WS_SERVICE_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_PROPERTY_HOST_USER_STATE;
serviceProperties[0].value = &quotePtr; // assume this is some state that you want to associate with the service host
serviceProperties[0].valueSize = sizeof(quotePtr);
```


<span data-ttu-id="c1021-109">狀態資料適用于所有服務主機回呼和 [服務作業](service-operation.md)。</span><span class="sxs-lookup"><span data-stu-id="c1021-109">The state data is available to all service host callbacks and [service operations](service-operation.md).</span></span> <span data-ttu-id="c1021-110">回呼和服務作業會藉由呼叫 [**WsGetOperationCoNtextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty)函式並指定內容（由 [ws 作業 \_ \_ 內容](ws-operation-context.md)結構參考）和內容屬性（如下列範例所示）的其中一個值，取得資訊。 [**\_ \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id)</span><span class="sxs-lookup"><span data-stu-id="c1021-110">Callbacks and service operations retrieve the information by calling the [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) function and specifying the context, referenced by the [WS\_OPERATION\_CONTEXT](ws-operation-context.md) structure, and the context property, as one of the values of the [**WS\_OPERATION\_CONTEXT\_PROPERTY\_HOST\_USER\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id) eunumeration, as illustrated in the following example.</span></span>

``` syntax
QuoteTable* table = NULL;
HRESULT hr = NOERROR;
if (FAILED (WsGetOperationContextProperty (context, WS_OPERATION_CONTEXT_PROPERTY_HOST_USER_STATE, &table, sizeof(table), NULL, error)))
    return hr;
```

 

 




