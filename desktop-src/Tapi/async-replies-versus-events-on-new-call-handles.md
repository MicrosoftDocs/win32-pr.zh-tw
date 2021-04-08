---
description: TSPI 包含許多作業，可啟動呼叫控制碼的存留期。
ms.assetid: 28e171a3-db47-40fd-9c5a-d7b76d834a99
title: 非同步回復與新呼叫控制碼上的事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02511a083c318afb227e3e172191d3ab84a69fed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850487"
---
# <a name="async-replies-versus-events-on-new-call-handles"></a>非同步回復與新呼叫控制碼上的事件

TSPI 包含許多作業，可啟動呼叫控制碼的存留期。 如果服務提供者針對這類作業傳回成功，它必須填入 **HDRVCALL** 類型的不透明控制碼，它會在傳回之前將它用於新的呼叫。 在收到相符的 [*完成 \_*](/windows/win32/api/tspi/nc-tspi-async_completion) 程式之前，TAPI 永遠不會在呼叫上執行作業。 如果服務提供者傳回失敗，控制碼就會自動變成不正確 (也就是沒有 [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)) 。 實際上，在非同步完成之前，TAPI 會將控制碼視為「尚未生效」。

在收到相符的 [*完成 \_*](/windows/win32/api/tspi/nc-tspi-async_completion) 程式之後，服務提供者也必須將控制碼視為「無效」。 換句話說，它不得針對新的呼叫發出任何 [*line \_ 事件*](/windows/win32/api/tspi/nc-tspi-lineevent) 函式，或將它包含在訊息的呼叫計數或該行的狀態資料結構中。

TAPI 等級也符合這些生命週期的限制;在相符的 [**行 \_ 回復**](./line-reply.md) 訊息之前，不會傳回或有效的新呼叫控制碼，而且新呼叫的任何事件都不會傳遞至應用程式，直到行 \_ 回復訊息為止。

此「啟動存留期」原則適用的 TSPI 作業如下：

-   [**TSPI \_ lineCompleteTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)
-   [**TSPI \_ lineForward**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)
-   [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)
-   [**TSPI \_ linePickup**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)
-   [**TSPI \_ linePrepareAddToConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference)
-   [**TSPI \_ lineSetupConference**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference)
-   [**TSPI \_ lineSetupTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)
-   [**TSPI \_ lineUnpark**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)

 

 
