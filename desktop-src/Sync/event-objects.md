---
description: 事件物件是一種同步處理物件，其狀態可以明確設定為使用 SetEvent 函式來發出信號。 以下是兩種類型的事件物件。
ms.assetid: 63dc2991-e070-4981-9e2d-90b4fdaaee7a
title: " (同步處理的事件物件) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9ea7c77fd61723b6ab927616817a5de2c323bf800431547800e2a96f33deee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886311"
---
# <a name="event-objects-synchronization"></a> (同步處理的事件物件) 

*事件物件* 是一種同步處理物件，其狀態可以明確設定為使用 [**SetEvent**](/windows/win32/api/synchapi/nf-synchapi-setevent)函式來發出信號。 以下是兩種類型的事件物件。



| Object             | 描述                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 手動重設事件 | 在 [**ResetEvent**](/windows/win32/api/synchapi/nf-synchapi-resetevent) 函式明確重設為未收到信號之前，其狀態會維持為信號的事件物件。 當其收到信號時，可以釋出任何數目的等候中線程，或後續在其中一個 [等候](wait-functions.md)函式中指定相同事件物件的執行緒。                                                                                                        |
| 自動重設事件   | 事件物件，其狀態會保持為信號，直到釋放單一等候中的執行緒為止，此時系統會自動將狀態設定為未收到信號。 如果沒有執行緒在等候，事件物件的狀態會維持已收到信號。 如果有多個執行緒正在等候，則會選取等候中的執行緒。 請勿採用先進先出 (FIFO) 順序。 外來事件（例如核心模式 Apc）可以變更等候順序。<br/> |



 

事件物件適用于將信號傳送給指出發生特定事件的執行緒。 例如，在重迭的輸入和輸出中，系統會在重迭的作業完成時，將指定的事件物件設定為已發出信號的狀態。 單一線程可以在數個同時重迭的作業中指定不同的事件物件，然後使用其中一個多物件 [等候](wait-functions.md) 函式來等候任何一個事件物件的狀態被發出信號。

執行緒使用 [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) 或 [**CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa) 函數來建立事件物件。 建立執行緒會指定物件的初始狀態，以及它是否為手動重設或自動重設事件物件。 建立執行緒也可以指定事件物件的名稱。 其他進程中的執行緒可以藉由在 [**OpenEvent**](/windows/win32/api/synchapi/nf-synchapi-openeventa) 函式的呼叫中指定其名稱，來開啟現有事件物件的控制碼。 如需 mutex、事件、信號和計時器物件之名稱的詳細資訊，請參閱 [進程間同步](interprocess-synchronization.md)處理。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用事件物件](using-event-objects.md)
</dt> </dl>

 

 
