---
title: 進行非同步呼叫
description: 用戶端必須先初始化非同步控制碼，然後才能進行非同步遠端呼叫。 用戶端和伺服器程式會使用 \_ \_ 非同步控制碼的 RPC 非同步狀態結構指標。
ms.assetid: b40308ef-88ae-4c80-9118-29c5ffee77ad
keywords:
- 遠端程序呼叫 RPC、工作、進行非同步呼叫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa06f60b43a7dff3a29223ff1d8e9ad726c0e938
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965441"
---
# <a name="making-the-asynchronous-call"></a><span data-ttu-id="ad4bd-105">進行非同步呼叫</span><span class="sxs-lookup"><span data-stu-id="ad4bd-105">Making the Asynchronous Call</span></span>

<span data-ttu-id="ad4bd-106">用戶端必須先初始化非同步控制碼，然後才能進行非同步遠端呼叫。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-106">Before it can make an asynchronous remote call, the client must initialize the asynchronous handle.</span></span> <span data-ttu-id="ad4bd-107">用戶端和伺服器程式會使用非同步控制碼的 [**RPC \_ 非同步 \_ 狀態**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-107">Client and server programs use pointers to the [**RPC\_ASYNC\_STATE**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state) structure for asynchronous handles.</span></span>

<span data-ttu-id="ad4bd-108">每個未完成的呼叫都必須有自己的唯一非同步控制碼。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-108">Every outstanding call must have its own unique asynchronous handle.</span></span> <span data-ttu-id="ad4bd-109">用戶端會建立控制碼，並將其傳遞至 [**RpcAsyncInitializeHandle**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncinitializehandle) 函式。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-109">The client creates the handle and passes it to the [**RpcAsyncInitializeHandle**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncinitializehandle) function.</span></span> <span data-ttu-id="ad4bd-110">若要讓呼叫正確完成，用戶端必須確保在接收到伺服器的非同步回復之前，不會釋放控制碼的記憶體。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-110">For the call to complete correctly, the client must ensure that the memory for the handle is not released until it receives the server's asynchronous reply.</span></span> <span data-ttu-id="ad4bd-111">此外，在對現有的非同步控制碼進行另一個呼叫之前，用戶端必須重新初始化控制碼。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-111">Also, before making another call on an existing asynchronous handle, the client must reinitialize the handle.</span></span> <span data-ttu-id="ad4bd-112">若未這麼做，可能會導致用戶端存根在呼叫期間引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-112">Failure to do this can cause the client stub to raise an exception during the call.</span></span> <span data-ttu-id="ad4bd-113">用戶端也必須確保它為 out 參數提供的緩衝區 \[ [](/windows/desktop/Midl/out-idl) \] ，而 \[ [](/windows/desktop/Midl/in)非同步遠端程式的 **out** \] 參數會保持配置，直到它從伺服器收到回復為止。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-113">The client must also ensure that the buffers it supplies for \[[**out**](/windows/desktop/Midl/out-idl)\] parameters and \[[**in**](/windows/desktop/Midl/in), **out**\] parameters to an asynchronous remote procedure remain allocated until it has received the reply from the server.</span></span>

<span data-ttu-id="ad4bd-114">當它叫用非同步遠端程式時，用戶端必須選取 RPC 執行時間程式庫將用來通知呼叫完成的方法。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-114">When it invokes an asynchronous remote procedure, the client must select the method that the RPC run-time library will use to notify it of the call's completion.</span></span> <span data-ttu-id="ad4bd-115">用戶端可以透過下列其中一種方式接收此通知：</span><span class="sxs-lookup"><span data-stu-id="ad4bd-115">The client can receive this notification in any one of the following ways:</span></span>

-   <span data-ttu-id="ad4bd-116">事件。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-116">Event.</span></span> <span data-ttu-id="ad4bd-117">用戶端可以指定當呼叫完成時要引發的事件。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-117">The client can specify an event to be fired when the call has completed.</span></span> <span data-ttu-id="ad4bd-118">如需詳細資訊，請參閱 [事件物件](/windows/desktop/Sync/event-objects)。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-118">For details, see [Event Objects](/windows/desktop/Sync/event-objects).</span></span>
-   <span data-ttu-id="ad4bd-119">輪詢。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-119">Polling.</span></span> <span data-ttu-id="ad4bd-120">用戶端可以重複呼叫 [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus)。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-120">The client can repeatedly call [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus).</span></span> <span data-ttu-id="ad4bd-121">如果傳回值是 RPC S ASYNC CALL PENDING 以外的任何其他值 \_ \_ \_ \_ ，則呼叫已完成。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-121">If the return value is anything other than RPC\_S\_ASYNC\_CALL\_PENDING, the call is complete.</span></span> <span data-ttu-id="ad4bd-122">這個方法所使用的 CPU 時間比這裡所述的其他方法更多。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-122">This method uses more CPU time than the other methods described here.</span></span>
-   <span data-ttu-id="ad4bd-123">Apc。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-123">APC.</span></span> <span data-ttu-id="ad4bd-124">用戶端可以指定呼叫完成時呼叫的 [ (APC) 的非同步程序呼叫 ](/windows/desktop/Sync/asynchronous-procedure-calls) 。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-124">The client can specify an [asynchronous procedure call (APC)](/windows/desktop/Sync/asynchronous-procedure-calls) that gets called when the call completes.</span></span> <span data-ttu-id="ad4bd-125">如需 APC 函數的原型，請參閱 [**RPCNOTIFICATION \_ 常式**](/previous-versions/aa375808(v=vs.80))。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-125">For the prototype of the APC function, see [**RPCNOTIFICATION\_ROUTINE**](/previous-versions/aa375808(v=vs.80)).</span></span> <span data-ttu-id="ad4bd-126">將其事件參數設定為 RpcCallComplete 時，會呼叫 APC。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-126">The APC is called with its Event parameter set to RpcCallComplete.</span></span> <span data-ttu-id="ad4bd-127">若要讓 Apc 分派，用戶端執行緒必須處於可提供警示等候狀態。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-127">For APCs to get dispatched, the client thread must be in an alertable wait state.</span></span>

    <span data-ttu-id="ad4bd-128">如果非同步控制碼中的 **hThread** 欄位設定為0，則 apc 會排入進行非同步呼叫的執行緒上。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-128">If the **hThread** field in the asynchronous handle is set to 0, the APCs are queued on the thread that made the asynchronous call.</span></span> <span data-ttu-id="ad4bd-129">如果非零，則會將 Apc 排入 m 所指定的執行緒上。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-129">If it is nonzero, the APCs are queued on the thread specified by m.</span></span>

-   <span data-ttu-id="ad4bd-130">國際 奧會。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-130">IOC.</span></span> <span data-ttu-id="ad4bd-131">I/o 完成通訊埠會以非同步控制碼中指定的參數來通知。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-131">The I/O completion port is notified with the parameters specified in the asynchronous handle.</span></span> <span data-ttu-id="ad4bd-132">如需詳細資訊，請參閱 [**CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport)。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-132">For more information, see [**CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport).</span></span>
-   <span data-ttu-id="ad4bd-133">Windows 控制碼。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-133">Windows handle.</span></span> <span data-ttu-id="ad4bd-134"> (HWND) 將訊息張貼至指定的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-134">A message is posted to the specified window handle (HWND).</span></span>

<span data-ttu-id="ad4bd-135">下列程式碼片段顯示初始化非同步控制碼並使用它來進行非同步遠端程序呼叫所需的必要步驟。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-135">The following code fragment shows the essential steps required for initializing an asynchronous handle and using it to make an asynchronous remote procedure call.</span></span>


```C++
RPC_ASYNC_STATE Async;
RPC_STATUS status;
 
// Initialize the handle.
status = RpcAsyncInitializeHandle(&Async, sizeof(RPC_ASYNC_STATE));
if (status)
{
    // Code to handle the error goes here.
}
 
Async.UserInfo = NULL;
Async.NotificationType = RpcNotificationTypeEvent;
 
Async.u.hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
if (Async.u.hEvent == 0)
{
    // Code to handle the error goes here.
}
// Call an asynchronous RPC routine here
RpcTryExcept
{
    printf("\nCalling the remote procedure 'AsyncFunc'\n");
    AsyncFunc(&Async, AsyncRPC_ClientIfHandle, nAsychDelay);
}
RpcExcept(1)
{
    ulCode = RpcExceptionCode();
    printf("AsyncFunc: Run time reported exception 0x%lx = %ld\n", 
            ulCode, ulCode);
}
RpcEndExcept
 
// Call a synchronous routine while
// the asynchronous procedure is still running
RpcTryExcept
{
    printf("\nCalling the remote procedure 'NonAsyncFunc'\n");
    NonAsyncFunc(AsyncRPC_ClientIfHandle, pszMessage);
    fprintf(stderr, 
            "While 'AsyncFunc' is running asynchronously,\n"
            "we still can send message to the server in the mean "
            "time.\n\n");
}
RpcExcept(1)
{
    ulCode = RpcExceptionCode();
    printf("NonAsyncFunc: Run time reported exception 0x%lx = %ld\n", 
            ulCode, ulCode);
}
RpcEndExcept
```



<span data-ttu-id="ad4bd-136">如這個範例所示，當非同步程序呼叫仍在擱置中時，您的用戶端程式可以執行同步遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-136">As this example demonstrates, your client program can execute synchronous remote procedure calls while an asynchronous procedure call is still pending.</span></span> <span data-ttu-id="ad4bd-137">此用戶端會建立 RPC 執行時間程式庫的事件物件，以便在非同步呼叫完成時用來通知它。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-137">This client creates an event object for the RPC run-time library to use to notify it when the asynchronous call completes.</span></span>

> [!Note]  
> <span data-ttu-id="ad4bd-138">如果在非同步呼叫期間引發 RPC 例外狀況，則不會從非同步 RPC 常式傳回完成的通知。</span><span class="sxs-lookup"><span data-stu-id="ad4bd-138">Notification of completion will not be returned from an asynchronous RPC routine if an RPC exception is raised during an asynchronous call.</span></span>

 

 

 