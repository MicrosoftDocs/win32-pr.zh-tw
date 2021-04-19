---
description: 為了將控制項要求傳送至執行中的服務，服務控制程式會使用 ControlService 函數。
ms.assetid: d6cdc876-8b74-460e-ad43-6455ddf428dd
title: 服務控制要求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb5edf56137e2c98ea7db440a4db5e55df5e8f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970794"
---
# <a name="service-control-requests"></a>服務控制要求

為了將控制項要求傳送至執行中的服務，服務控制程式會使用 [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) 函數。 此函式會指定傳遞至指定服務之 [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) 函數的控制項值。 這個控制項值可以是使用者定義的程式碼，也可以是可讓呼叫程式執行下列動作的其中一個標準程式碼：

-   停止服務 (服務 \_ 控制 \_ 停止) 。
-   暫停服務 (服務 \_ 控制 \_ 暫停) 。
-   繼續執行暫停的服務 (服務 \_ 控制 \_ 繼續) 。
-   從服務取得更新的狀態資訊 (服務 \_ 控制 \_ 詢問) 。

每個服務都會指定要接受和處理的控制項值。 若要判斷服務接受哪些標準控制項值，請使用 [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) 函數，或 \_ \_ 在 [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) 函數的呼叫中指定服務控制查閱控制項值。 這些函數所傳回之 [**服務 \_ 狀態**](/windows/desktop/api/Winsvc/ns-winsvc-service_status)結構的 **dwControlsAccepted** 成員會指出服務是否可以停止、暫停或繼續。 所有服務都接受服務 \_ 控制的查閱 \_ 控制值。

[**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex)函數會報告指定服務的最新狀態，但不會從服務本身取得更新的狀態。 \_ \_ 在 [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice)呼叫中使用服務控制查閱控制項值，可確保傳回的狀態資訊是最新的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 SC 控制服務](controlling-a-service-using-sc.md)
</dt> </dl>

 

 



