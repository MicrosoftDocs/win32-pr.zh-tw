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
# <a name="sending-the-asynchronous-reply"></a>傳送非同步回復

非同步呼叫完成時，伺服器會呼叫 [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) 函式，並將非同步控制碼傳遞給用戶端，藉此將回復傳送給用戶端。 即使非同步呼叫的傳回值為 void，而且沒有 out 參數，也需要進行此呼叫 \[ \] 。 如果函式有傳回值，則會以傳址方式傳遞至 **RpcAsyncCompleteCall**。

當伺服器呼叫 [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) 或 **RpcAsyncAbortCall**，或呼叫完成，因為在伺服器管理員常式中引發例外狀況時，RPC 執行時間程式庫會自動損毀伺服器的非同步控制碼。

> [!Note]  
> 伺服器必須在 \[ 呼叫 RpcAsyncCompleteCall 之前，先完成更新 in、out \] 和 \[ out \] 參數。  呼叫 **RpcAsyncCompleteCall** 之後，就不能對這些參數或非同步控制碼進行任何變更。 如果 **RpcAsyncCompleteCall** 函式呼叫失敗，RPC 執行時間就會釋出參數。

 

下列範例示範簡單的非同步程序呼叫。


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



為了簡單起見，這個非同步伺服器常式不會處理實際的資料。 它只會讓自己進入睡眠狀態。

> [!Note]  
> **RpcAsyncCompleteCall** 函數可以在接收呼叫的執行緒上呼叫，或在進程中的任何其他執行緒上呼叫。 如果完成呼叫所需的所有資料都可立即使用，則伺服器可能會將它們填入相同的執行緒，並在相同的執行緒上呼叫 **RpcAsyncCompleteCall** 。 這種方法可節省一些內容切換，並提升效能。 這類呼叫稱為伺機非同步。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**RPC \_ 非同步 \_ 狀態**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state)
</dt> <dt>

[**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)
</dt> <dt>

[**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)
</dt> <dt>

[**RpcServerTestCancel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel)
</dt> </dl>

 

 




