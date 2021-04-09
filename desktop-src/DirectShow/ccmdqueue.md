---
description: CCmdQueue 類別是一個基類，可提供 CDeferredCommand 物件和成員函式的佇列，以新增、移除、檢查狀態，以及叫用已排入佇列的命令。
ms.assetid: 6bd0f0f3-3c56-47d2-9fd8-e2863a2afa33
title: CCmdQueue 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue
api_type:
- COM
api_location: ''
ms.openlocfilehash: 78af7a975d54ba832bbdf1fb7f8027f87b747660
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108677"
---
# <a name="ccmdqueue-class"></a>CCmdQueue 類別

`CCmdQueue`類別是基類，提供 [**CDeferredCommand**](cdeferredcommand.md)物件和成員函式的佇列，以新增、移除、檢查狀態，以及叫用已排入佇列的命令。 `CCmdQueue`物件是物件的一部分，它會執行 [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand)方法。 篩選圖形管理員會實 **IQueueCommand** 方法，讓應用程式可以將命令排入篩選圖形。 執行 **IQueueCommand** 介面的篩選器會直接使用這個類別。 如果您想要使用 **CDeferredCommand** 物件，則必須從這個類別衍生您的佇列。

同步處理的模式有兩種：粗略且精確。 在粗略模式中，應用程式會等到指定的時間抵達，然後執行命令。 在精確的模式中，應用程式會等到處理開始于當時出現的範例上執行，然後執行命令。 篩選準則會決定要執行哪一個。 篩選圖形管理員一律會針對在篩選圖形管理員中排入佇列的命令，實施粗略模式。

如果您想要進行粗略的同步處理，您可能會想要等到有命令到期，然後執行它。 您可以藉由呼叫 [**CCmdQueue：： GetDueCommand**](ccmdqueue-getduecommand.md)來執行這項作業。 如果您有幾件事要等候，請從 [**CCmdQueue：： GetDueHandle**](ccmdqueue-getduehandle.md) 取得事件控制碼，然後在收到通知時呼叫 **CCmdQueue：： GetDueCommand** 。 [**stream time**](stream-time.md) 只會在 [**CCmdQueue：： Run**](ccmdqueue-run.md) 和 [**CCmdQueue：： EndRun**](ccmdqueue-endrun.md) 成員函式的呼叫之間前進。 如果已設定控制碼，就無法保證會有命令可供使用。 每次通知事件時，呼叫 **GetDueCommand** 成員函式 (可能有零) 的超時;如果沒有任何命令就緒，這可能會傳回 E \_ ABORT。

如果您想要精確的同步處理，請呼叫 [**CCmdQueue：： GetCommandDueFor**](ccmdqueue-getcommandduefor.md) 成員函式，並將您即將處理的範例傳遞為參數。 這會傳回下列內容：

-   資料流程時間或該資料流程時間之前或之前的資料流程時間命令。
-   在呈現資料流程時間之前或之前的呈現時間命令。 請只在 [**CCmdQueue：： Run**](ccmdqueue-run.md) 和 [**CCmdQueue：： EndRun**](ccmdqueue-endrun.md) 成員函式之間執行此動作，因為在此之外，從資料流程時間到呈現時間的對應不是已知的。
-   立即到期的任何展示時間命令。

如果您想要對可能在暫停模式期間處理的樣本進行精確的同步處理，則必須使用資料流程時間命令。

在所有情況下，命令都會保持佇列，直到呼叫或取消為止。 事件控制碼的設定和重設完全由此佇列物件管理。



| 受保護的資料成員                                 | Description                                                                                            |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| m \_ bRunning                                            | 執行狀態的旗標;執行時，請設定 **TRUE** 。                                                     |
| m \_ dwAdvise                                            | 如果沒有未完成的建議) ，則建議參考時鐘中的識別碼 (零。                            |
| m \_ evDue                                               | 設定任何命令即將到期的時間。                                                               |
| m \_ listPresentation                                    | 將命令儲存在展示時間佇列中。                                                           |
| m \_ listStream                                          | 儲存以資料流程時間佇列的命令。                                                                 |
| m \_ 鎖定                                                | 保護對清單的存取。                                                                              |
| m \_ pClock                                              | 目前的參考時鐘。                                                                               |
| m \_ StreamTimeOffset                                    | 當 **m \_ BRunning** 為 **TRUE** 時，包含資料流程時間位移。                                      |
| m \_ StreamTimeOffset                                    | 當 **m \_ BRunning** 為 **TRUE** 時，包含資料流程時間位移。                                      |
| 成員函數                                       | Description                                                                                            |
| [**CCmdQueue**](ccmdqueue-ccmdqueue.md)               | 結構 **CCmdQueue** 物件。                                                                     |
| [**CheckTime**](ccmdqueue-checktime.md)               | 判斷指定的時間是否為逾期。                                                                     |
| [**GetDueHandle**](ccmdqueue-getduehandle.md)         | 抓取將發出信號的事件控制碼。                                                      |
| 可覆寫的成員函式                           | Description                                                                                            |
| [**EndRun**](ccmdqueue-endrun.md)                     | 切換為 [已停止] 或 [已暫停] 模式。                                                                    |
| [**GetCommandDueFor**](ccmdqueue-getcommandduefor.md) | 抓取在指定時間排程的延後命令。                                    |
| [**GetDueCommand**](ccmdqueue-getduecommand.md)       | 抓取下一個已到期命令的指標。                                                   |
| [**插入**](ccmdqueue-insert.md)                     | 將 [**CDeferredCommand**](cdeferredcommand.md) 物件新增至佇列。                             |
| [**新增**](ccmdqueue-new.md)                           | 初始化要執行的命令，並傳回新的 [**CDeferredCommand**](cdeferredcommand.md) 物件。 |
| [**移除**](ccmdqueue-remove.md)                     | 從佇列中移除 [**CDeferredCommand**](cdeferredcommand.md) 物件。                        |
| [**執行**](ccmdqueue-run.md)                           | 切換至執行模式。                                                                              |
| [**SetSyncSource**](ccmdqueue-setsyncsource.md)       | 設定用於時間的時鐘。                                                                        |
| [**SetTimeAdvise**](ccmdqueue-settimeadvise.md)       | 使用參考時鐘來設定計時器事件。                                                        |



 

 

 



