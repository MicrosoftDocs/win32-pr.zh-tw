---
title: 'Web 服務的內容 (Windows) '
description: 內容會在服務模型服務作業和回呼中用來將相關的狀態資料傳遞至服務作業或回呼（當叫用時）。
ms.assetid: 44283854-96df-4e6b-8464-3df685896f07
keywords:
- Windows 的內容 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd7863f22193dd1496134afff991ff54efbee5026f2a11e52359b2b016c878c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026626"
---
# <a name="context-windows-web-services"></a>Web 服務的內容 (Windows) 

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

 

 




