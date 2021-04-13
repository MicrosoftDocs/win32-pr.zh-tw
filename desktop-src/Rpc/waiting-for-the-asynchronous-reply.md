---
title: 等候非同步回復
description: 用戶端在等候來自伺服器的回復時所執行的工作，取決於所選取的通知機制。
ms.assetid: b1d4ea54-26bc-49f9-8cc1-a74fd4ffced3
keywords:
- 遠端程序呼叫 RPC、工作、等候非同步回復
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0890b3024a05bb704f7b5a803c4b1e517c65ee21
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315886"
---
# <a name="waiting-for-the-asynchronous-reply"></a>等候非同步回復

用戶端在等候來自伺服器的回復時所執行的工作，取決於所選取的通知機制。

如果用戶端使用事件來進行通知，通常會呼叫 [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) 函式或 [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) 函式。 當用戶端呼叫其中一個函式時，會進入封鎖狀態。 這會很有效率，因為用戶端不會在它被封鎖時使用 CPU 執行循環。

當它使用輪詢等候其結果時，用戶端程式會進入迴圈來重複呼叫函式 [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus)。 這是一種有效的方法，可讓您的用戶端程式在輪詢迴圈中進行其他處理。 例如，它可以針對後續的非同步遠端程序呼叫，以較小的區塊來準備資料。 在每個區塊完成之後，您的用戶端就可以輪詢未完成的非同步遠端程序呼叫，以查看是否已完成。

您的用戶端程式可以提供 (APC) 的非同步程序呼叫，這是一種回呼函式，當非同步遠端程序呼叫完成時，RPC 執行時間程式庫會叫用此類型的回呼函數。 您的用戶端程式必須處於可提供警示等候狀態。 這通常表示用戶端會呼叫 Windows API 函式，使其成為封鎖狀態。 如需詳細資訊，請參閱 [非同步程序呼叫](/windows/desktop/Sync/asynchronous-procedure-calls)。

> [!Note]  
> 如果在非同步呼叫期間引發 RPC 例外狀況，則不會從非同步 RPC 常式傳回完成的通知。

 

如果您的用戶端程式使用 i/o 完成埠來接收完成通知，則必須呼叫 [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函數。 當它執行時，它可以無限期地等候回應，或繼續執行其他處理。 如果它在等候回復時進行其他處理，它必須使用 **GetQueuedCompletionStatus** 函式來輪詢完成埠。 在此情況下，通常需要將 *dwMilliseconds* 設定為零。 這會導致 **GetQueuedCompletionStatus** 立即傳回，即使非同步呼叫尚未完成。

用戶端程式也可以透過其視窗訊息佇列接收完成通知。 在此情況下，他們只會處理完成訊息，就像處理任何 Windows 訊息一樣。

在多執行緒應用程式中，只有在發出呼叫的執行緒已成功從呼叫傳回之後，用戶端才可以取消非同步呼叫。 這可確保呼叫不會在失敗同步呼叫之後，由另一個執行緒以非同步方式取消。 如同標準做法，同步失敗的非同步呼叫不應該以非同步方式取消。 如果可以在不同的執行緒上發出和取消呼叫，用戶端應用程式必須觀察到此行為。 此外，在取消呼叫之後，用戶端程式代碼必須等待完成通知並完成呼叫。 [**RpcAsyncCancelCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall)函式只會尖峰完成通知;它不是完成通話的替代方案。

下列程式碼片段會說明用戶端程式如何使用事件來等候非同步回復。


```C++
// This code fragment assumes that Async is a valid asynchronous
// RPC handle.
if (WaitForSingleObject(Async.u.hEvent, INFINITE) == WAIT_FAILED)
{
    RpcRaiseException(APP_ERROR);
}
```



使用 APC 接收非同步回復通知的用戶端程式，通常會將自己變成封鎖狀態。 下列程式碼片段顯示此程式碼。


```C++
if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
{
    RpcRaiseException(APP_ERROR);
}
```



在此情況下，用戶端程式會進入睡眠狀態，不耗用 CPU 週期，直到 RPC 執行時間程式庫呼叫 APC (未顯示) 。

下一個範例示範使用 i/o 完成埠來等候非同步回復的用戶端。


```C++
// This code fragment assumes that Async is a valid asynchronous
// RPC handle.
if (!GetQueuedCompletionStatus(
         Async.u.IOC.hIOPort,
         &Async.u.IOC.dwNumberOfBytesTransferred,
         &Async.u.IOC.dwCompletionKey,
         &Async.u.IOC.lpOverlapped,
         INFINITE))
{
    RpcRaiseException(APP_ERROR);
}
```



在上述範例中， [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 的呼叫會無限期等候，直到非同步遠端程序呼叫完成為止。

撰寫多執行緒應用程式時，會發生一種可能的缺陷。 如果執行緒叫用遠端程序呼叫，然後在收到傳送完成的通知之前終止，則遠端程序呼叫可能會失敗，而且用戶端 stub 可能會關閉與伺服器的連接。 因此，呼叫遠端程式的執行緒不應在呼叫完成之前終止，或在不需要行為時取消。

 

 