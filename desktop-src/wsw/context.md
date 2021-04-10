---
title: 'Windows Web 服務的內容 () '
description: 內容會在服務模型服務作業和回呼中用來將相關的狀態資料傳遞至服務作業或回呼（當叫用時）。
ms.assetid: 44283854-96df-4e6b-8464-3df685896f07
keywords:
- 適用于 Windows 的內容 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7edd1f8c93bbf4fd4b4d5feea5b2219bc522ea
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "103932833"
---
# <a name="context-windows-web-services"></a>Windows Web 服務的內容 () 

內容會在服務模型 [服務作業](service-operation.md) 和回呼中用來將相關的狀態資料傳遞至服務作業或回呼（當叫用時）。 內容是由 [WS \_ 操作 \_ 內容](ws-operation-context.md) 結構所參考。 您可以使用 [**WsGetOperationCoNtextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) 函數來抓取內容的屬性，如下列程式碼所示。

``` syntax
WS_MESSAGE* requestMessage = NULL;
HRESULT hr = WsGetOperationContextProperty (
                context, 
                WS_OPERATION_CONTEXT_PROPERTY_INPUT_MESSAGE, 
                &requestMessage, 
                sizeof(requestMessage),
                error);
```

並非所有內容屬性都可在任何指定時間使用。 請參閱有關回呼或 [服務](service-operation.md)作業中特定屬性可用性的內容屬性檔。

如需如何維護作業內容存留期和執行緒的詳細資訊，請參閱 [操作內容存留期和執行緒](operation-context-lifetime-and-threading.md) 主題。

下列列舉是內容的一部分：

-   [**WS \_ 操作 \_ 上下文 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id)

下列函數是內容的一部分：

-   [**WsGetOperationCoNtextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty)

下列控制碼是內容的一部分：

-   [WS \_ 操作 \_ 內容](ws-operation-context.md)

 

 




