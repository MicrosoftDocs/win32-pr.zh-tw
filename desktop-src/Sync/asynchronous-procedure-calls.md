---
description: " (APC) 的非同步程序呼叫，是在特定執行緒內容中以非同步方式執行的函式。"
ms.assetid: 0197d78e-a4dc-414b-88ba-c5ec5f2ed614
title: 非同步程序呼叫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1c024506c2afc9a895db645fd386ed76f915f6e1178c6b8ce3a257aa7d40fa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661448"
---
# <a name="asynchronous-procedure-calls"></a>非同步程序呼叫

 (APC) 的 *非同步程序呼叫* ，是在特定執行緒內容中以非同步方式執行的函式。 當 APC 排入執行緒佇列時，系統會發出軟體插斷。 下次排程執行緒時，它會執行 APC 函數。 系統所產生的 APC 稱為 *核心模式 apc*。 應用程式所產生的一個 APC 稱為 *使用者模式*。 執行緒必須處於可提供警示狀態，才能執行使用者模式的 APC。

每個執行緒都有自己的 APC 佇列。 應用程式會藉由呼叫 [**QueueUserAPC**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queueuserapc) 函式，將 APC 排入執行緒佇列。 呼叫執行緒會在呼叫 **QueueUserAPC** 時指定 APC 函數的位址。 APC 的佇列是要求執行緒呼叫 APC 函數的要求。

當使用者模式 APC 排入佇列時，除非它處於可提供警示狀態，否則它排入佇列的執行緒不會被導向呼叫 APC 函數。 執行緒在呼叫 [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex)、 [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait)、 [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex)、 [**WaitForMultipleObjectsEx**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjectsex)或 [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) 函數時進入可提供警示狀態。 如果在 APC 排入佇列之前滿足等候，執行緒就不再處於可提供警示等候狀態，因此不會執行 APC 函數。 不過，APC 仍會排入佇列，所以當執行緒呼叫另一個可提供警示 wait 函式時，就會執行 APC 函數。

[**ReadFileEx**](/windows/win32/api/fileapi/nf-fileapi-readfileex)、 [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer)、 [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)和 [**WriteFileEx**](/windows/win32/api/fileapi/nf-fileapi-writefileex)函式是使用 APC 作為完成通知回呼機制來執行。

如果您使用 [執行緒集](../procthread/thread-pools.md)區，請注意，apc 無法運作，以及其他信號機制，因為系統會控制執行緒集區執行緒的存留期，因此在傳遞通知之前，執行緒可能會終止。 與其使用以 APC 為基礎的信號機制（例如 [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer)或 [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)的 *pfnCompletionRoutine* 參數），您不需要使用可等候物件，例如使用 [**CreateThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer)建立的計時器。 針對 i/o，請使用以 [**CreateThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio)建立的 i/o 完成物件或以 *hEvent*[**為基礎的**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)重迭結構，其中事件可傳遞至 [**SetThreadpoolWait**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait)函數。

## <a name="synchronization-internals"></a>同步處理內部

發出 i/o 要求時，會配置結構以代表要求。 此結構稱為 i/o 要求封包 (IRP) 。 使用同步 i/o 時，執行緒會建立 IRP、將它傳送至裝置堆疊，並在核心中等待 IRP 完成。 使用非同步 i/o 時，執行緒會建立 IRP，並將其傳送至裝置堆疊。 堆疊可能會立即完成 IRP，或可能會傳回暫止狀態，表示要求正在進行中。 發生這種情況時，IRP 仍會與執行緒相關聯，因此如果執行緒終止或呼叫函式（例如 [**CancelIo**](/windows/win32/api/ioapiset/nf-ioapiset-cancelio)），就會取消此作業。 在此同時，當裝置堆疊繼續處理 IRP 時，執行緒可以繼續執行其他工作。

有幾種方式可讓系統指出 IRP 已完成：

-   將重迭的結構更新為作業的結果，讓執行緒可以進行輪詢，以判斷作業是否已完成。
-   以重迭的結構表示事件，讓執行緒可以在事件上進行同步處理，並在作業完成時喚醒。
-   將 IRP 排入執行緒的擱置中，使執行緒在進入可提供警示等候狀態並從等待作業傳回時執行 APC 常式，並將狀態指出它已執行一或多個 APC 常式。
-   將 IRP 排入 i/o 完成埠的佇列，以等候完成埠的下一個執行緒執行。

等候 i/o 完成埠的執行緒不會在可提供警示狀態等候。 因此，如果這些執行緒發出的 Irp 設定為完成執行緒的 Apc，這些 IPC 完成將不會及時發生;只有當執行緒從 i/o 完成埠收取要求，然後進入可提供警示等候時，才會發生這些情況。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用具有非同步程序呼叫的可等候計時器](using-a-waitable-timer-with-an-asynchronous-procedure-call.md)
</dt> </dl>

 

 
