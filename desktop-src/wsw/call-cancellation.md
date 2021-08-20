---
title: 呼叫取消
description: 呼叫取消通知會取消伺服器端服務作業和服務模型回呼的操作。
ms.assetid: dc371921-869f-4775-98d3-80a1006358ba
keywords:
- 針對 Windows 呼叫取消 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dda4ec4227403bed5239b68cfa05d2064976517a7473fa7926c8de5f56227645
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026696"
---
# <a name="call-cancellation"></a>呼叫取消

呼叫取消通知會取消 [伺服器端服務作業](server-side-service-operations.md) 和服務模型回呼的操作。 這類取消的原因有二：

-   因為呼叫 [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost) 函式，所以服務主機已停止作業。
-   基礎通道引發錯誤。


若要接收取消通知，服務作業或服務模型回呼必須藉由呼叫 [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel)函式來註冊 [**WS 作業 \_ \_ CANCEL \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)回呼。

（選擇性）在註冊取消通知的過程中，服務作業或服務模型回呼也可以註冊應用程式特定的狀態資料和 WS 作業 [**的 \_ \_ 可用 \_ 狀態 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) 回呼。

狀態資料可供 [**WS 作業 \_ \_ 取消 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) 回呼使用。 呼叫完成時，會呼叫 [**WS 作業 \_ \_ 可用 \_ 狀態 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) 回呼，讓應用程式有機會釋放狀態資料。

如需程式碼範例，請參閱 [BlockingServiceExample](blockingserviceexample.md)。

在 [伺服器端服務作業](server-side-service-operations.md) 或回呼函數的存留期內，取消回呼只會呼叫一次。

使用 [WS 作業 \_ \_ 內容](ws-operation-context.md) 做為參數的所有服務主機回呼都可以使用呼叫取消。

下列 API 元素與呼叫取消有關。

| 回呼                                                                         | 描述                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**WS \_ 操作 \_ 取消 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)          | 由服務模型叫用，以通知因服務主機中止關機而取消非同步服務作業。 |
| [**WS \_ 作業 \_ 可用 \_ 狀態 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) | 由服務模型叫用，以允許應用程式清除以取消回呼註冊的狀態資料。                |



 



| 函式                                                             | 描述                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) | 允許服務作業或服務模型回呼註冊取消通知。 |



 

 

 




