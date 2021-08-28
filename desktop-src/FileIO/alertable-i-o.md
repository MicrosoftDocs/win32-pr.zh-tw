---
description: 可提供警示 i/o 是應用程式執行緒只會在處於可提供警示狀態時處理非同步 i/o 要求的方法。
ms.assetid: d996f1cc-eeab-456b-818b-5307a79effd9
title: 可提供警示 i/o
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b76df0a59726d6fb0eea0bd99ff960e9b18ba80f7c17bf0ae7e4338953895e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766238"
---
# <a name="alertable-io"></a>可提供警示 i/o

可提供警示 i/o 是應用程式執行緒只會在處於可提供警示狀態時處理非同步 i/o 要求的方法。

若要瞭解執行緒處於可提供警示狀態的時間，請考慮下列案例：

1.  執行緒藉由呼叫 [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) 和回呼函式的指標，初始化非同步讀取要求。
2.  執行緒藉由呼叫 [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) 和回呼函式的指標，來起始非同步寫入要求。
3.  執行緒呼叫的函式會從遠端資料庫伺服器提取一列資料。

在此案例中， [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) 和 [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) 的呼叫最可能會在步驟3中的函式呼叫之前傳回。 當他們這麼做時，核心會線上程的非同步程序呼叫上放置回呼函數的指標， (APC) 佇列。 核心會維護此佇列，專門用來保存傳回的 i/o 要求資料，直到對應的執行緒可以處理它為止。

當資料列提取完成且執行緒從函式傳回時，其最高優先順序是藉由呼叫回呼函式來處理佇列上傳回的 i/o 要求。 若要這樣做，它必須進入可提供警示狀態。 執行緒只能藉由使用適當的旗標來呼叫下列其中一個函式來執行此動作：

-   [**SleepEx**](/windows/desktop/api/synchapi/nf-synchapi-sleepex)
-   [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)
-   [**WaitForMultipleObjectsEx**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex)
-   [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait)
-   [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex)

當執行緒進入可提供警示狀態時，會發生下列事件：

1.  核心會檢查執行緒的 APC 佇列。 如果佇列包含回呼函式指標，則核心會移除佇列中的指標，並將它傳送到執行緒。
2.  執行緒執行回呼函數。
3.  佇列中剩餘的每個指標都會重複步驟1和2。
4.  當佇列是空的時，執行緒會從將它置於可提供警示狀態的函式中返回。

在此案例中，一旦執行緒進入可提供警示狀態，它就會呼叫傳送至 [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) 和 [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)的回呼函式，然後從放入可提供警示狀態的函式返回。

如果執行緒在其 APC 佇列是空的情況下進入可提供警示狀態，則在發生下列其中一種情況時，核心會暫停執行緒的執行：

-   正在等待的核心物件會收到信號。
-   在 APC 佇列中放置回呼函式指標。

使用可提供警示 i/o 來處理非同步 i/o [**要求的執行緒**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) ，會比在設定重迭結構中的事件旗標時更有效率，而且可提供警示 i/o 機制的複雜度會比要使用的 [i/o 完成埠](i-o-completion-ports.md) 低。 不過，可提供警示 i/o 只會將 i/o 要求的結果傳回給起始它的執行緒。 I/o 完成埠沒有這項限制。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[非同步程序呼叫](/windows/desktop/Sync/asynchronous-procedure-calls)
</dt> </dl>

 

 
