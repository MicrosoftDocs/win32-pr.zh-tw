---
title: 傳送非同步回復
description: 非同步呼叫完成時，伺服器會呼叫 RpcAsyncCompleteCall 函式，並將非同步控制碼傳遞給用戶端，藉此將回復傳送給用戶端。
ms.assetid: 458bc476-963e-4812-b4c2-9074ff0a8284
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f861c3f2a1befdb85435f5275176c82e23bb06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021899"
---
# <a name="sending-the-asynchronous-reply"></a><span data-ttu-id="57805-103">傳送非同步回復</span><span class="sxs-lookup"><span data-stu-id="57805-103">Sending the Asynchronous Reply</span></span>

<span data-ttu-id="57805-104">非同步呼叫完成時，伺服器會呼叫 [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) 函式，並將非同步控制碼傳遞給用戶端，藉此將回復傳送給用戶端。</span><span class="sxs-lookup"><span data-stu-id="57805-104">When the asynchronous call is complete, the server sends a reply to the client by calling the [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) function and passing it the asynchronous handle.</span></span> <span data-ttu-id="57805-105">即使非同步呼叫的傳回值為 void，而且沒有 out 參數，也需要進行此呼叫 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="57805-105">This call is necessary even if the asynchronous call has a void return value and no \[out\] parameters.</span></span> <span data-ttu-id="57805-106">如果函式有傳回值，則會以傳址方式傳遞至 **RpcAsyncCompleteCall**。</span><span class="sxs-lookup"><span data-stu-id="57805-106">If the function has a return value, it is passed by reference to **RpcAsyncCompleteCall**.</span></span>

<span data-ttu-id="57805-107">當伺服器呼叫 [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) 或 **RpcAsyncAbortCall**，或呼叫完成，因為在伺服器管理員常式中引發例外狀況時，RPC 執行時間程式庫會自動損毀伺服器的非同步控制碼。</span><span class="sxs-lookup"><span data-stu-id="57805-107">When the server calls [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) or **RpcAsyncAbortCall**, or a call completes because an exception was raised in the server-manager routine, the RPC run-time library automatically destroys the server's asynchronous handle.</span></span>

> [!Note]  
> <span data-ttu-id="57805-108">伺服器必須在 \[ 呼叫 RpcAsyncCompleteCall 之前，先完成更新 in、out \] 和 \[ out \] 參數。 </span><span class="sxs-lookup"><span data-stu-id="57805-108">The server must finish updating the \[in, out\] and \[out\] parameters before calling **RpcAsyncCompleteCall**.</span></span> <span data-ttu-id="57805-109">呼叫 **RpcAsyncCompleteCall** 之後，就不能對這些參數或非同步控制碼進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="57805-109">No changes can be made to those parameters or to the asynchronous handle after calling **RpcAsyncCompleteCall**.</span></span> <span data-ttu-id="57805-110">如果 **RpcAsyncCompleteCall** 函式呼叫失敗，RPC 執行時間就會釋出參數。</span><span class="sxs-lookup"><span data-stu-id="57805-110">If the **RpcAsyncCompleteCall** function call fails, the RPC runtime frees the parameters.</span></span>

 

<span data-ttu-id="57805-111">下列範例示範簡單的非同步程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="57805-111">The following example demonstrates a simple asynchronous procedure call.</span></span>


```C++
#define DEFAULT_ASYNC_DELAY 20;
#define ASYNC_CANCEL_CHECK 100;

void AsyncFunc(IN PRPC_ASYNC_STATE pAsync,
               IN RPC_BINDING_HANDLE hBinding,
               IN OUT unsigned long nAsychDelay)
{
    int nReply = 1;
    RPC_STATUS status;
    unsigned long nTmpAsychDelay;
    int i;
 
    if (nAsychDelay < 0){
        nAsychDelay = DEFAULT_ASYNC_DELAY;
    }else if (nAsychDelay < 100){
        nAsychDelay = 100;
    }

    // We only call RpcServerTestCancel if the call
    // takes longer than ASYNC_CANCEL_CHECK ms
    if(nAsychDelay > ASYNC_CANCEL_CHECK){
        
        nTmpAsychDelay = nAsychDelay/100;
 
        for (i = 0; i < 100; i++){
            Sleep(nTmpAsychDelay);
 
            if (i%5 == 0){
                fprintf(stderr, 
                        "\rRunning AsyncFunc (%lu ms) (%d%c) ... ",
                        nAsychDelay, i+5, PERCENT);
 
                status = 
                    RpcServerTestCancel(
                        RpcAsyncGetCallHandle(pAsync));
                if (status == RPC_S_OK){
                    fprintf(stderr, 
                            "\nAsyncFunc has been canceled!!!\n");
                    break;
                }else if (status != RPC_S_CALL_IN_PROGRESS){
                    printf(
                        "RpcAsyncInitializeHandle returned 0x%x\n", 
                        status);
                    exit(status); 
                }
            }
        }
    }else{
        Sleep(nAsychDelay);
    }
 
    printf("\nCalling RpcAsyncCompleteCall\n");
    status = RpcAsyncCompleteCall(pAsync, &nReply);
    printf("RpcAsyncCompleteCall returned 0x%x\n", status);
    if (status){
        exit(status);
    }
}
```



<span data-ttu-id="57805-112">為了簡單起見，這個非同步伺服器常式不會處理實際的資料。</span><span class="sxs-lookup"><span data-stu-id="57805-112">For the sake of simplicity, this asynchronous server routine does not process actual data.</span></span> <span data-ttu-id="57805-113">它只會讓自己進入睡眠狀態。</span><span class="sxs-lookup"><span data-stu-id="57805-113">It simply puts itself to sleep for awhile.</span></span>

> [!Note]  
> <span data-ttu-id="57805-114">**RpcAsyncCompleteCall** 函數可以在接收呼叫的執行緒上呼叫，或在進程中的任何其他執行緒上呼叫。</span><span class="sxs-lookup"><span data-stu-id="57805-114">The **RpcAsyncCompleteCall** function can be called either on the thread that received the call, or on any other thread in the process.</span></span> <span data-ttu-id="57805-115">如果完成呼叫所需的所有資料都可立即使用，則伺服器可能會將它們填入相同的執行緒，並在相同的執行緒上呼叫 **RpcAsyncCompleteCall** 。</span><span class="sxs-lookup"><span data-stu-id="57805-115">If all the data necessary to complete the call are readily available, the server may fill them in on the same thread, and call the **RpcAsyncCompleteCall** on the same thread.</span></span> <span data-ttu-id="57805-116">這種方法可節省一些內容切換，並提升效能。</span><span class="sxs-lookup"><span data-stu-id="57805-116">This approach saves some context switching and improves performance.</span></span> <span data-ttu-id="57805-117">這類呼叫稱為伺機非同步。</span><span class="sxs-lookup"><span data-stu-id="57805-117">Such calls are called opportunistically asynchronous.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="57805-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="57805-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57805-119">**RPC \_ 非同步 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="57805-119">**RPC\_ASYNC\_STATE**</span></span>](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state)
</dt> <dt>

[<span data-ttu-id="57805-120">**RpcAsyncCompleteCall**</span><span class="sxs-lookup"><span data-stu-id="57805-120">**RpcAsyncCompleteCall**</span></span>](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)
</dt> <dt>

[<span data-ttu-id="57805-121">**RpcAsyncAbortCall**</span><span class="sxs-lookup"><span data-stu-id="57805-121">**RpcAsyncAbortCall**</span></span>](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)
</dt> <dt>

[<span data-ttu-id="57805-122">**RpcServerTestCancel**</span><span class="sxs-lookup"><span data-stu-id="57805-122">**RpcServerTestCancel**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel)
</dt> </dl>

 

 




