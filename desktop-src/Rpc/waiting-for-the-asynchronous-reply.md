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
# <a name="waiting-for-the-asynchronous-reply"></a><span data-ttu-id="57c5d-104">等候非同步回復</span><span class="sxs-lookup"><span data-stu-id="57c5d-104">Waiting for the Asynchronous Reply</span></span>

<span data-ttu-id="57c5d-105">用戶端在等候來自伺服器的回復時所執行的工作，取決於所選取的通知機制。</span><span class="sxs-lookup"><span data-stu-id="57c5d-105">What the client does while it waits to be notified of a reply from the server depends on the notification mechanism it selects.</span></span>

<span data-ttu-id="57c5d-106">如果用戶端使用事件來進行通知，通常會呼叫 [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) 函式或 [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) 函式。</span><span class="sxs-lookup"><span data-stu-id="57c5d-106">If the client uses an event for notification, it will typically call the [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) function or the [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) function.</span></span> <span data-ttu-id="57c5d-107">當用戶端呼叫其中一個函式時，會進入封鎖狀態。</span><span class="sxs-lookup"><span data-stu-id="57c5d-107">The client enters a blocked state when it calls either of these functions.</span></span> <span data-ttu-id="57c5d-108">這會很有效率，因為用戶端不會在它被封鎖時使用 CPU 執行循環。</span><span class="sxs-lookup"><span data-stu-id="57c5d-108">This is efficient because the client does not consume CPU run cycles while it is blocked.</span></span>

<span data-ttu-id="57c5d-109">當它使用輪詢等候其結果時，用戶端程式會進入迴圈來重複呼叫函式 [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus)。</span><span class="sxs-lookup"><span data-stu-id="57c5d-109">When it uses polling to wait for its results, the client program enters a loop that repeatedly calls the function [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus).</span></span> <span data-ttu-id="57c5d-110">這是一種有效的方法，可讓您的用戶端程式在輪詢迴圈中進行其他處理。</span><span class="sxs-lookup"><span data-stu-id="57c5d-110">This is an efficient method of waiting if your client program does other processing in the polling loop.</span></span> <span data-ttu-id="57c5d-111">例如，它可以針對後續的非同步遠端程序呼叫，以較小的區塊來準備資料。</span><span class="sxs-lookup"><span data-stu-id="57c5d-111">For instance, it can prepare data in small chunks for a subsequent asynchronous remote procedure call.</span></span> <span data-ttu-id="57c5d-112">在每個區塊完成之後，您的用戶端就可以輪詢未完成的非同步遠端程序呼叫，以查看是否已完成。</span><span class="sxs-lookup"><span data-stu-id="57c5d-112">After each chunk is finished, your client can poll the outstanding asynchronous remote procedure call to see if it is complete.</span></span>

<span data-ttu-id="57c5d-113">您的用戶端程式可以提供 (APC) 的非同步程序呼叫，這是一種回呼函式，當非同步遠端程序呼叫完成時，RPC 執行時間程式庫會叫用此類型的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="57c5d-113">Your client program can provide an asynchronous procedure call (APC), which is a type of callback function that the RPC run-time library will invoke when the asynchronous remote procedure call completes.</span></span> <span data-ttu-id="57c5d-114">您的用戶端程式必須處於可提供警示等候狀態。</span><span class="sxs-lookup"><span data-stu-id="57c5d-114">Your client program must be in an alertable wait state.</span></span> <span data-ttu-id="57c5d-115">這通常表示用戶端會呼叫 Windows API 函式，使其成為封鎖狀態。</span><span class="sxs-lookup"><span data-stu-id="57c5d-115">This typically means that the client calls a Windows API function to put itself in a blocked state.</span></span> <span data-ttu-id="57c5d-116">如需詳細資訊，請參閱 [非同步程序呼叫](/windows/desktop/Sync/asynchronous-procedure-calls)。</span><span class="sxs-lookup"><span data-stu-id="57c5d-116">For more information, see [Asynchronous Procedure Calls](/windows/desktop/Sync/asynchronous-procedure-calls).</span></span>

> [!Note]  
> <span data-ttu-id="57c5d-117">如果在非同步呼叫期間引發 RPC 例外狀況，則不會從非同步 RPC 常式傳回完成的通知。</span><span class="sxs-lookup"><span data-stu-id="57c5d-117">Notification of completion will not be returned from an asynchronous RPC routine if an RPC exception is raised during a asynchronous call.</span></span>

 

<span data-ttu-id="57c5d-118">如果您的用戶端程式使用 i/o 完成埠來接收完成通知，則必須呼叫 [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函數。</span><span class="sxs-lookup"><span data-stu-id="57c5d-118">If your client program uses an I/O completion port to receive completion notification, it must call the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span> <span data-ttu-id="57c5d-119">當它執行時，它可以無限期地等候回應，或繼續執行其他處理。</span><span class="sxs-lookup"><span data-stu-id="57c5d-119">When it does, it can either wait indefinitely for a response or continue to do other processing.</span></span> <span data-ttu-id="57c5d-120">如果它在等候回復時進行其他處理，它必須使用 **GetQueuedCompletionStatus** 函式來輪詢完成埠。</span><span class="sxs-lookup"><span data-stu-id="57c5d-120">If it does other processing while it waits for a reply, it must poll the completion port with the **GetQueuedCompletionStatus** function.</span></span> <span data-ttu-id="57c5d-121">在此情況下，通常需要將 *dwMilliseconds* 設定為零。</span><span class="sxs-lookup"><span data-stu-id="57c5d-121">In this case, it typically needs to set the *dwMilliseconds* to zero.</span></span> <span data-ttu-id="57c5d-122">這會導致 **GetQueuedCompletionStatus** 立即傳回，即使非同步呼叫尚未完成。</span><span class="sxs-lookup"><span data-stu-id="57c5d-122">This causes **GetQueuedCompletionStatus** to return immediately, even if the asynchronous call has not completed.</span></span>

<span data-ttu-id="57c5d-123">用戶端程式也可以透過其視窗訊息佇列接收完成通知。</span><span class="sxs-lookup"><span data-stu-id="57c5d-123">Client programs can also receive completion notification through their window message queues.</span></span> <span data-ttu-id="57c5d-124">在此情況下，他們只會處理完成訊息，就像處理任何 Windows 訊息一樣。</span><span class="sxs-lookup"><span data-stu-id="57c5d-124">In this situation, they simply process the completion message as they would any Windows message.</span></span>

<span data-ttu-id="57c5d-125">在多執行緒應用程式中，只有在發出呼叫的執行緒已成功從呼叫傳回之後，用戶端才可以取消非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="57c5d-125">In a multithreaded application, an asynchronous call can be canceled by the client only after the thread that originated the call has returned successfully from the call.</span></span> <span data-ttu-id="57c5d-126">這可確保呼叫不會在失敗同步呼叫之後，由另一個執行緒以非同步方式取消。</span><span class="sxs-lookup"><span data-stu-id="57c5d-126">This ensures that the call is not canceled asynchronously by another thread after it failed a synchronous call.</span></span> <span data-ttu-id="57c5d-127">如同標準做法，同步失敗的非同步呼叫不應該以非同步方式取消。</span><span class="sxs-lookup"><span data-stu-id="57c5d-127">As standard practice, an asynchronous call that fails synchronously should not be canceled asynchronously.</span></span> <span data-ttu-id="57c5d-128">如果可以在不同的執行緒上發出和取消呼叫，用戶端應用程式必須觀察到此行為。</span><span class="sxs-lookup"><span data-stu-id="57c5d-128">The client application must observe this behavior if calls may be issued and canceled on different threads.</span></span> <span data-ttu-id="57c5d-129">此外，在取消呼叫之後，用戶端程式代碼必須等待完成通知並完成呼叫。</span><span class="sxs-lookup"><span data-stu-id="57c5d-129">Also, after the call is canceled, the client code must wait for the completion notification and complete the call.</span></span> <span data-ttu-id="57c5d-130">[**RpcAsyncCancelCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall)函式只會尖峰完成通知;它不是完成通話的替代方案。</span><span class="sxs-lookup"><span data-stu-id="57c5d-130">The [**RpcAsyncCancelCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall) function simply rushes the completion notification; it is not a substitute for completing the call.</span></span>

<span data-ttu-id="57c5d-131">下列程式碼片段會說明用戶端程式如何使用事件來等候非同步回復。</span><span class="sxs-lookup"><span data-stu-id="57c5d-131">The following code fragment illustrates how a client program can use an event to wait for an asynchronous reply.</span></span>


```C++
// This code fragment assumes that Async is a valid asynchronous
// RPC handle.
if (WaitForSingleObject(Async.u.hEvent, INFINITE) == WAIT_FAILED)
{
    RpcRaiseException(APP_ERROR);
}
```



<span data-ttu-id="57c5d-132">使用 APC 接收非同步回復通知的用戶端程式，通常會將自己變成封鎖狀態。</span><span class="sxs-lookup"><span data-stu-id="57c5d-132">Client programs that use an APC to receive notification of an asynchronous reply typically put themselves into a blocked state.</span></span> <span data-ttu-id="57c5d-133">下列程式碼片段顯示此程式碼。</span><span class="sxs-lookup"><span data-stu-id="57c5d-133">The following code fragment shows this.</span></span>


```C++
if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
{
    RpcRaiseException(APP_ERROR);
}
```



<span data-ttu-id="57c5d-134">在此情況下，用戶端程式會進入睡眠狀態，不耗用 CPU 週期，直到 RPC 執行時間程式庫呼叫 APC (未顯示) 。</span><span class="sxs-lookup"><span data-stu-id="57c5d-134">In this case, the client program goes to sleep, consuming no CPU cycles, until the RPC run-time library calls the APC (not shown).</span></span>

<span data-ttu-id="57c5d-135">下一個範例示範使用 i/o 完成埠來等候非同步回復的用戶端。</span><span class="sxs-lookup"><span data-stu-id="57c5d-135">The next example demonstrates a client that uses an I/O completion port to wait for an asynchronous reply.</span></span>


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



<span data-ttu-id="57c5d-136">在上述範例中， [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 的呼叫會無限期等候，直到非同步遠端程序呼叫完成為止。</span><span class="sxs-lookup"><span data-stu-id="57c5d-136">In the preceding example, the call to [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) waits indefinitely until the asynchronous remote procedure call completes.</span></span>

<span data-ttu-id="57c5d-137">撰寫多執行緒應用程式時，會發生一種可能的缺陷。</span><span class="sxs-lookup"><span data-stu-id="57c5d-137">One potential pitfall occurs when writing multithreaded applications.</span></span> <span data-ttu-id="57c5d-138">如果執行緒叫用遠端程序呼叫，然後在收到傳送完成的通知之前終止，則遠端程序呼叫可能會失敗，而且用戶端 stub 可能會關閉與伺服器的連接。</span><span class="sxs-lookup"><span data-stu-id="57c5d-138">If a thread invokes a remote procedure call and then terminates before it receives notification that the send completed, the remote procedure call may fail and the client stub may close the connection to the server.</span></span> <span data-ttu-id="57c5d-139">因此，呼叫遠端程式的執行緒不應在呼叫完成之前終止，或在不需要行為時取消。</span><span class="sxs-lookup"><span data-stu-id="57c5d-139">Therefore, threads that call a remote procedure should not terminate before the call is completed or canceled when behavior is undesirable.</span></span>

 

 