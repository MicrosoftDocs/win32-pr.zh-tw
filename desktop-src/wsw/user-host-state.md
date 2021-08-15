---
title: 服務主機使用者狀態
description: 服務主機可讓應用程式關聯服務主機層級範圍內的狀態資料。
ms.assetid: e18c6c0c-3205-4f88-9a9b-2515a7cfc462
keywords:
- Windows 的使用者主機狀態 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04530b74ef1ab0125b31e56751cdd6cec8109711f603c909f3afeb66970f081a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118192428"
---
# <a name="service-host-user-state"></a>服務主機使用者狀態

[服務主機](service-host.md)可讓應用程式關聯服務主機層級範圍內的狀態資料。 此狀態是由當應用程式建立 [服務主機](service-host.md)時傳遞至 [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost)函式的 [**WS \_ 服務 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property)結構所指定，如下列範例所示。

``` syntax
void* quotePtr = (void*) quotes;
WS_SERVICE_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_PROPERTY_HOST_USER_STATE;
serviceProperties[0].value = &quotePtr; // assume this is some state that you want to associate with the service host
serviceProperties[0].valueSize = sizeof(quotePtr);
```


狀態資料適用于所有服務主機回呼和 [服務作業](service-operation.md)。 回呼和服務作業會藉由呼叫 [**WsGetOperationCoNtextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty)函式並指定內容（由 [ws 作業 \_ \_ 內容](ws-operation-context.md)結構參考）和內容屬性（如下列範例所示）的其中一個值，取得資訊。 [**\_ \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id)

``` syntax
QuoteTable* table = NULL;
HRESULT hr = NOERROR;
if (FAILED (WsGetOperationContextProperty (context, WS_OPERATION_CONTEXT_PROPERTY_HOST_USER_STATE, &table, sizeof(table), NULL, error)))
    return hr;
```

 

 




