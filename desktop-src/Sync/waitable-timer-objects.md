---
description: 可等候計時器物件是一種同步處理物件，其狀態會在指定的到期時間到達時設為已發出信號。
ms.assetid: 5d39ada0-ea31-40d7-b075-aeb657ee508c
title: 可等候計時器物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9597617705fcd78bb71f63e33a475e3bca78e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994437"
---
# <a name="waitable-timer-objects"></a>可等候計時器物件

*可等候計時器物件* 是一種同步處理物件，其狀態會在指定的到期時間到達時設為已發出信號。 您可以建立兩種類型的可等候計時器：手動重設和同步處理。 這兩種類型的計時器也可以是週期性計時器。



| Object                | 描述                                                                                                                                                                                             |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 手動重設計時器    | 在呼叫 [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) 來建立新的到期時間之前，其狀態會維持為信號的計時器。                                                                          |
| 同步處理計時器 | 線上程完成計時器物件的等候作業之前，其狀態會維持為信號的計時器。                                                                                                     |
| 定期計時器        | 每次指定期間過期時，會重新開機的計時器，直到計時器重設或取消為止。 定期計時器是定期手動重設計時器或定期同步處理計時器。 |



 

> [!Note]  
> 當計時器收到信號時，處理器必須執行以處理相關聯的指令。 高頻率的定期計時器會讓處理器持續忙碌，以防止系統以較低的 [電源狀態](../power/system-power-states.md) 維持任何有意義的時間長度。 這可能會對可攜式電腦的電池壽命和案例造成負面影響，這取決於有效的電源管理（例如大型資料中心）。 為了提高能源效率，請考慮在應用程式中使用以事件為基礎的通知，而不是以時間為基礎的通知。 如果需要計時器，請使用一次發出信號的計時器，而不是定期計時器，或將間隔設定為大於一秒的值。

 

執行緒使用 [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) 或 [**CreateWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerexw) 函數來建立計時器物件。 建立執行緒會指定計時器是手動重設計時器或同步處理計時器。 建立執行緒可以指定計時器物件的名稱。 其他進程中的執行緒可以藉由在 [**OpenWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw) 函式的呼叫中指定其名稱，來開啟現有計時器的控制碼。 任何具有計時器物件之控制碼的執行緒都可以使用其中一個 [等候](wait-functions.md) 函式來等候計時器狀態設定為已發出信號。

-   執行緒會呼叫 [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) 函數來啟動計時器。 請注意下列 **SetWaitableTimer** 參數的用法：
-   使用 *lpDueTime* 參數來指定計時器設定為信號狀態的時間。 當手動重設計時器設定為已發出信號的狀態時，它會維持在此狀態中，直到 [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) 建立新的到期時間為止。 當同步處理計時器設定為已發出信號的狀態時，它會維持在此狀態中，直到執行緒完成計時器物件的等候作業為止。
-   使用 [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer)函數的 *lPeriod* 參數來指定計時器週期。 如果句號不是零，則計時器是定期計時器;它會在每次過期期間重新開機，直到計時器重設或取消為止。 如果句號為零，則計時器不是定期計時器;它會發出一次信號，然後停用。

執行緒可以使用 [**CancelWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-cancelwaitabletimer) 函數將計時器設為非使用中狀態。 若要重設計時器，請呼叫 [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer)。 當您完成計時器物件時，請呼叫 [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) 來關閉計時器物件的控制碼。

可等候計時器的行為可摘要如下：

-   設定計時器之後，如果計時器已在使用中，則會將其取消，計時器的狀態為未收到信號，而計時器則放置於核心計時器佇列中。
-   當計時器過期時，計時器會設定為已發出信號的狀態。 如果計時器有完成常式，則會將它排入設定計時器的執行緒佇列。 完成常式會線上程進入可提供警示等候狀態之前，線上程的 (APC) 佇列中保持在 [非同步程序呼叫](asynchronous-procedure-calls.md) 中。 屆時，會分派 APC 並呼叫完成常式。 如果計時器是週期性的，則會將它放回核心計時器佇列中。
-   當計時器取消時，它會從核心計時器佇列中移除（如果已暫止）。 如果計時器已過期，但仍有一個 APC 排入設定計時器的執行緒，則會從執行緒的 APC 佇列中移除 APC。 計時器的信號狀態不會受到影響。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[非同步程序呼叫](asynchronous-procedure-calls.md)
</dt> <dt>

[使用可等候計時器物件](using-waitable-timer-objects.md)
</dt> </dl>

 

 
