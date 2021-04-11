---
title: 伺服器端非同步管道處理
description: 非同步函式的管理員常式一律會接收非同步控制碼做為第一個參數。
ms.assetid: ddf9c319-6c4d-4de1-ab29-0ef9b76531ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2b0f11372090f1fd181c0d7272aa1446e5e3d22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023585"
---
# <a name="server-side-asynchronous-pipe-handling"></a><span data-ttu-id="4a992-103">伺服器端非同步管道處理</span><span class="sxs-lookup"><span data-stu-id="4a992-103">Server-side Asynchronous Pipe Handling</span></span>

<span data-ttu-id="4a992-104">非同步函式的管理員常式一律會接收非同步控制碼做為第一個參數。</span><span class="sxs-lookup"><span data-stu-id="4a992-104">The manager routine of an asynchronous function always receives the asynchronous handle as the first parameter.</span></span> <span data-ttu-id="4a992-105">伺服器會使用此控制碼來傳送回復，並在輸出管道資料可用時傳送。</span><span class="sxs-lookup"><span data-stu-id="4a992-105">The server uses this handle to send the reply and to send the out pipe data as it becomes available.</span></span> <span data-ttu-id="4a992-106">控制碼會維持有效，直到在其上呼叫 [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) 、由 [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)中止呼叫，或在管理員常式中發生例外狀況。</span><span class="sxs-lookup"><span data-stu-id="4a992-106">The handle remains valid until [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) is called on it, the call is aborted by [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall), or an exception occurs in the manager routine.</span></span> <span data-ttu-id="4a992-107">應用程式必須追蹤 out 和 out 參數的所有最上層指標 \[  \] ，才能 \[  \] 在完成呼叫之前加以更新。</span><span class="sxs-lookup"><span data-stu-id="4a992-107">The application must keep track of all top-level pointers for the \[**out**\] and \[**in, out**\] parameters, in order to update them before completing the call.</span></span> <span data-ttu-id="4a992-108">應用程式也必須追蹤 \[ [**in**](/windows/desktop/Midl/in) \] 和 \[ [**out**](/windows/desktop/Midl/out-idl) \] 管道。</span><span class="sxs-lookup"><span data-stu-id="4a992-108">The application must also keep track of the \[[**in**](/windows/desktop/Midl/in)\] and \[[**out**](/windows/desktop/Midl/out-idl)\] pipes.</span></span>

<span data-ttu-id="4a992-109">伺服器會以與用戶端相同的方式傳送非同步管道資料。</span><span class="sxs-lookup"><span data-stu-id="4a992-109">The server sends asynchronous pipe data in the same manner as the client.</span></span> <span data-ttu-id="4a992-110">請參閱 [用戶端非同步管道處理](client-side-asynchronous-pipe-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="4a992-110">See [Client-Side Asynchronous Pipe Handling](client-side-asynchronous-pipe-handling.md).</span></span>

<span data-ttu-id="4a992-111">伺服器會以與用戶端相同的方式接收非同步管道資料。</span><span class="sxs-lookup"><span data-stu-id="4a992-111">The server receives asynchronous pipe data in the same manner as the client.</span></span> <span data-ttu-id="4a992-112">如果接收機制是非同步程序呼叫 (Apc) ，則伺服器必須在 pAsync >hThread) 中指定執行緒控制碼 (，然後向執行時間程式庫註冊非同步控制碼。</span><span class="sxs-lookup"><span data-stu-id="4a992-112">If the receive mechanism is asynchronous procedure calls (APCs), the server must specify a thread handle (in pAsync->u.APC.hThread) and register the asynchronous handle with the run-time library.</span></span>

## <a name="example"></a><span data-ttu-id="4a992-113">範例</span><span class="sxs-lookup"><span data-stu-id="4a992-113">Example</span></span>

<span data-ttu-id="4a992-114">在此範例中，伺服器管理員常式 MyAsyncPipeFunc 會處理來自用戶端的遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="4a992-114">In this example, the server manager routine, MyAsyncPipeFunc, handles the remote procedure call from the client.</span></span>


```C++
typedef struct 
{
    PRPC_ASYNC_STATE pAsync;
    ASYNC_INTPIPE *inpipe;
    ASYNC_INTPIPE *outpipe;
    int i;
    int *b;
    int PipeBuffer[ASYNC_CHUNK_SIZE];
} PIPE_CALL_COOKIE;
 
void MyAsyncPipeFunc(
    IN PRPC_ASYNC_STATE pAsync,
    IN RPC_BINDING_HANDLE hBinding,
    IN int a,
    IN ASYNC_INTPIPE *inpipe,
    OUT ASYNC_INTPIPE *outpipe,
    OUT int *b)
{
    unsigned long ThreadIdentifier;
    HANDLE HandleToThread;
    PIPE_CALL_COOKIE *PipeCallCookie;
 
    PipeCallCookie = new PIPE_CALL_COOKIE;
    PipeCallCookie->pAsync = pAsync;
    PipeCallCookie->inpipe = inpipe;
    PipeCallCookie->outpipe = outpipe;
    PipeCallCookie->b = b;
 
    pAsync->u.APC.hThread = 0;
    pAsync->u.APC.hThread = CreateThread(
                                0, DefaultThreadStackSize,
                                (LPTHREAD_START_ROUTINE)   
                                ThreadProcPipes,
                                PipeCallCookie, 0,
                                &ThreadIdentifier);
}// endMyAsyncPipeFunc
 
//Sending pipe data
//This APC routine is called when a pipe send completes, 
//or when an asynchronous call completes. 
 
//This thread routine receives pipe data, processes the call, 
//sends the reply back to the client, and 
//completes the asynchronous call.
 
void ThreadProcPipes(IN PIPE_CALL_COOKIE  *Cookie)
{
    int *ptr ;
    int  n ;
    int retval ;
 
    while (pAsync->u.APC.hThread == 0)
    {
        Sleep(10);
    }
 
    pAsync->Flags = RPC_C_NOTIFY_ON_SEND_COMPLETE;
    pAsync->UserInfo = (void *) PipeCallCookie;
    pAsync->NotificationType = RpcNotificationTypeApc;
    pAsync->u.APC.NotificationRoutine = MyAsyncPipeAPCRoutine;
    pAsync->u.APC.hThread = HandleToThread;
 
    RpcAsyncRegisterHandle(pAsync);
 
    while (!fDone)
    {
        Cookie->inpipe->pull(
            Cookie->inpipe.state,
            (int *) Cookie->PipeBuffer,
            ASYNC_CHUNK_SIZE,
            &num_elements);
        switch (Status)
        {
            case RPC_S_ASYNC_CALL_PENDING:
                if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
                {
                    RpcRaiseException(APP_ERROR) ;
                }
            break;
 
            case RPC_S_OK:
                if (num_elements == 0)
                {
                    fDone = 1;
                }
                else
                {
                    // process the received data
                }
            break;
 
            default:
                fDone = 1;
            break;
        }
    }
 
    Cookie->i = 1;
    Cookie->outpipe->push(
        Cookie->outpipe.state,
        0,
        Cookie->PipeBuffer,
        ASYNC_CHUNK_SIZE) ;
 
    while (Cookie->i < ASYNC_NUM_CHUNKS+1)
    {
        if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
        {
            RpcRaiseException (APP_ERROR);
        }
    }
    // sending non pipe reply
    *(Cookie->b) = 10;
    Status = RpcAsyncCompleteCall (Cookie->pAsync, &retval);
}
 
void MyAsyncPipeAPCRoutine (
    IN PRPC_ASYNC_STATE pAsync,
    IN void *Context,
    IN unsigned int Flags)
{
    PIPE_CALL_COOKIE *Cookie = (PIPE_CALL_COOKIE *) pAsync->UserInfo;
 
    if (Flags & RPC_ASYNC_PIPE_SEND_COMPLETE)
    {
        if (Cookie->i & ASYNC_NUM_CHUNKS)
        {
            Cookie->outpipe->push(
                Cookie->outpipe.state,
                0,
                (int *) Cookie->PipeBuffer,
                ASYNC_CHUNK_SIZE);
            Cookie->i++ ;
        }
        else
        {
            pAsync->Flags = 0;
            Cookie->outpipe->push(Cookie->outpipe.state, 0, 0, 0);
            Cookie->i++;
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="4a992-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="4a992-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a992-116">管道</span><span class="sxs-lookup"><span data-stu-id="4a992-116">Pipes</span></span>](pipes.md)
</dt> <dt>

[<span data-ttu-id="4a992-117">非同步 MIDL</span><span class="sxs-lookup"><span data-stu-id="4a992-117">Asynchronous MIDL</span></span>](/windows/desktop/Midl/async)
</dt> <dt>

[<span data-ttu-id="4a992-118">伺服器端非同步 RPC</span><span class="sxs-lookup"><span data-stu-id="4a992-118">Server-Side Asynchronous RPC</span></span>](server-side-asynchronous-rpc.md)
</dt> </dl>

 

 