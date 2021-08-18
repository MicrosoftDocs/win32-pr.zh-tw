---
description: I/o 完成埠可提供有效率的執行緒模型，以處理多處理器系統上的多個非同步 i/o 要求。
ms.assetid: 213c48e8-bb21-43ed-9c00-2a5cf8ac25f0
title: I/o 完成埠
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2133bb14c661580eaf8004bd92c6f947b3b8777a4b1a5f6b330fe631b2be6c81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050828"
---
# <a name="io-completion-ports"></a>I/o 完成埠

I/o 完成埠可提供有效率的執行緒模型，以處理多處理器系統上的多個非同步 i/o 要求。 當進程建立 i/o 完成埠時，系統會針對其唯一目的是要為這些要求提供服務的要求，建立相關聯的佇列物件。 處理許多並行非同步 i/o 要求的處理常式可以更快速且有效率地使用 i/o 完成埠搭配預先配置的執行緒集區，而不是在收到 i/o 要求時建立執行緒。

## <a name="how-io-completion-ports-work"></a>I/o 完成埠的運作方式

[**CreateIoCompletionPort**](createiocompletionport.md)函式會建立 i/o 完成埠，並將一個或多個檔案控制代碼與該通訊埠產生關聯。 當其中一個檔案控制代碼的非同步 i/o 作業完成時，i/o 完成封包會以先進先出的方式排入佇列中， (FIFO) 順序寫入相關聯的 i/o 完成通訊埠。 這項機制的一個強大用途是將多個檔案控制代碼的同步處理點結合成單一物件，雖然另外還有其他有用的應用程式。 請注意，當封包以 FIFO 順序排入佇列時，它們可能會以不同順序排入佇列。

> [!Note]
>
> 此處所用的詞彙 *檔案控制代碼* 是指代表重迭 i/o 端點（而不只是磁片上的檔案）的系統抽象概念。 例如，它可以是網路端點、TCP 通訊端、具名管道或郵件位置。 您可以使用任何支援重迭 i/o 的系統物件。 如需相關 i/o 函數的清單，請參閱本主題的結尾。

 

當檔案控制代碼與完成埠相關聯時，傳入的狀態欄塊將不會更新，除非封包從完成埠移除。 唯一的例外狀況是，如果原始作業以同步方式傳回，就會發生錯誤。 執行緒 (由主執行緒或主執行緒本身建立的執行緒) 使用 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函式來等候完成封包排入 i/o 完成埠的佇列，而不是直接等候非同步 i/o 完成。 在 i/o 完成埠上封鎖其執行的執行緒，會以後進先出的 (LIFO) 順序來釋出，而下一個完成封包則會從該執行緒的 i/o 完成埠 FIFO 佇列中提取。 這表示，當完成封包釋出至執行緒時，系統會釋放與該埠相關聯的最後一個 (最近) 執行緒，並將最舊 i/o 完成的完成資訊傳遞給它。

雖然任何數目的執行緒都可以針對指定的 i/o 完成埠呼叫 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) ，但當指定的執行緒第一次呼叫 **GetQueuedCompletionStatus** 時，它會變成與指定的 i/o 完成埠相關聯，直到發生下列其中一種情況為止：執行緒結束、指定不同的 i/o 完成埠，或關閉 i/o 完成埠。 換句話說，單一線程最多可與一個 i/o 完成埠相關聯。

當完成封包排入 i/o 完成埠的佇列時，系統會先檢查與該埠相關聯的執行緒數目是否正在執行。 如果執行的執行緒數目小於並行值 () 下一節中所討論的，其中一個等候中的執行緒 (最新的) 可處理完成封包。 當執行中的執行緒完成其處理時，通常會再次呼叫 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) ，此時它會傳回下一個完成封包，或等候佇列是空的。

執行緒可以使用 [**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md) 函式，將完成的封包放入 i/o 完成埠的佇列中。 如此一來，除了從 i/o 系統接收 i/o 完成封包之外，還可以使用完成埠來接收來自進程其他執行緒的通訊。 **PostQueuedCompletionStatus** 函式可讓應用程式將其專屬的特殊用途完成封包排入 i/o 完成埠的佇列，而不需啟動非同步 i/o 作業。 例如，如果要通知外來事件的背景工作執行緒，這就很有用。

I/o 完成通訊埠控制碼，以及與該特定 i/o 完成埠相關聯的每個檔案控制代碼，稱為 *i/o 完成埠的參考*。 當 i/o 完成通訊埠沒有其他參考時，就會釋放它。 因此，所有這些控制碼都必須適當地關閉，才能釋放 i/o 完成埠及其相關聯的系統資源。 滿足這些條件之後，應用程式應該呼叫 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 函式來關閉 i/o 完成埠控制碼。

> [!Note]
>
> I/o 完成埠與建立它的進程相關聯，而且無法在進程之間共用。 不過，在相同進程中的執行緒之間可共用單一控制碼。

 

## <a name="threads-and-concurrency"></a>執行緒和平行存取

要謹慎考慮的 i/o 完成埠最重要的屬性是並行值。 當使用 [**CreateIoCompletionPort**](createiocompletionport.md) 透過 *NumberOfConcurrentThreads* 參數建立時，就會指定完成埠的並行值。 此值會限制與完成埠相關聯之可執行檔執行緒數目。 當與完成埠相關聯的可執行執行緒總數達到並行值時，系統會封鎖與該完成埠相關聯之任何後續執行緒的執行，直到可執行檔執行緒數目低於並行值為止。

在佇列中等候完成封包時，會發生最有效率的情況，但由於埠已達到其並行限制，因此不會滿足任何等候。 請考慮在 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函式呼叫中，有一個和多個執行緒的並行值會發生什麼事。 在此情況下，如果佇列永遠有等候中的完成封包，當執行中的執行緒呼叫 **GetQueuedCompletionStatus** 時，它將不會封鎖執行，因為如先前所述，執行緒佇列為 LIFO。 相反地，這個執行緒會立即取得下一個排入佇列的完成封包。 因為執行中的執行緒會持續收取完成封包，而其他執行緒無法執行，所以不會發生任何執行緒內容切換。

> [!Note]
>
> 在上述範例中，額外的執行緒看似無用且永遠不會執行，但這會假設執行中的執行緒永遠不會被其他機制進入等候狀態，而會終止或關閉其相關聯的 i/o 完成通訊埠。 在設計應用程式時，請考慮所有這類執行緒執行的後果。

 

針對並行值挑選的最佳整體最大值是電腦上的 Cpu 數目。 如果您的交易需要較長的計算，則較大的並行值會允許更多執行緒執行。 每個完成封包可能需要較長的時間才能完成，但會同時處理更多的完成封包。 您可以搭配程式碼剖析工具來試驗並行值，以達到應用程式的最佳效果。

如果另一個與相同 i/o 完成埠相關聯的執行中線程因其他原因而進入等候狀態（例如 [**SuspendThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-suspendthread)函式），則系統也可讓等候 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)的執行緒完成封包。 當等候狀態中的執行緒再次開始執行時，使用中線程的數目超過並行值時，可能會有短暫的時間。 不過，系統會在作用中線程的數目低於並行值之前，藉由不允許任何新的使用中線程，快速減少此數目。 這是讓您的應用程式在其執行緒集區中建立比並行值更多執行緒的原因之一。 執行緒集區管理已超出本主題的範圍，但良好的經驗法則是線上程集區中最少有兩個執行緒，如同系統上的處理器。 如需執行緒共用的詳細資訊，請參閱 [執行緒](/windows/desktop/ProcThread/thread-pools)集區。

## <a name="supported-io-functions"></a>支援的 i/o 函數

下列函式可用於啟動使用 i/o 完成埠完成的 i/o 作業。 您 [**必須將重迭結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 實例和先前與 i/o 完成埠相關聯的檔案控制代碼傳遞給函式， (呼叫 [**CreateIoCompletionPort**](createiocompletionport.md)) 來啟用 i/o 完成埠機制：

-   [**ConnectNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)
-   [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
-   [**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
-   [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)
-   [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
-   [**TransactNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)
-   [**WaitCommEvent**](/windows/desktop/api/winbase/nf-winbase-waitcommevent)
-   [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
-   [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)
-   [**WSASendTo**](/windows/desktop/api/winsock2/nf-winsock2-wsasendto)
-   [**WSASend**](/windows/desktop/api/winsock2/nf-winsock2-wsasend)
-   [**WSARecvFrom**](/windows/desktop/api/winsock2/nf-winsock2-wsarecvfrom)
-   [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
-   [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv)

## <a name="related-topics"></a>相關主題

<dl> <dt>


</dt> <dt>

[關於處理序和執行緒](/windows/desktop/ProcThread/about-processes-and-threads)
</dt> <dt>

[**BindIoCompletionCallback**](/windows/desktop/api/winbase/nf-winbase-bindiocompletioncallback)
</dt> <dt>

[**CreateIoCompletionPort**](createiocompletionport.md)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**GetQueuedCompletionStatusEx**](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md)
</dt> </dl>

 

 
