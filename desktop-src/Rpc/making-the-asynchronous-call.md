---
title: 進行非同步呼叫
description: 用戶端必須先初始化非同步控制碼，然後才能進行非同步遠端呼叫。 用戶端和伺服器程式會使用 \_ \_ 非同步控制碼的 RPC 非同步狀態結構指標。
ms.assetid: b40308ef-88ae-4c80-9118-29c5ffee77ad
keywords:
- 遠端程序呼叫 RPC、工作、進行非同步呼叫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d8399071cae6ea39aaac3f966e7e799b2c93b32a152048a7d18282b465f929
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928374"
---
# <a name="making-the-asynchronous-call"></a>進行非同步呼叫

用戶端必須先初始化非同步控制碼，然後才能進行非同步遠端呼叫。 用戶端和伺服器程式會使用非同步控制碼的 [**RPC \_ 非同步 \_ 狀態**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state) 結構指標。

每個未完成的呼叫都必須有自己的唯一非同步控制碼。 用戶端會建立控制碼，並將其傳遞至 [**RpcAsyncInitializeHandle**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncinitializehandle) 函式。 若要讓呼叫正確完成，用戶端必須確保在接收到伺服器的非同步回復之前，不會釋放控制碼的記憶體。 此外，在對現有的非同步控制碼進行另一個呼叫之前，用戶端必須重新初始化控制碼。 若未這麼做，可能會導致用戶端存根在呼叫期間引發例外狀況。 用戶端也必須確保它為 out 參數提供的緩衝區 \[ [](/windows/desktop/Midl/out-idl) \] ，而 \[ [](/windows/desktop/Midl/in)非同步遠端程式的 **out** \] 參數會保持配置，直到它從伺服器收到回復為止。

當它叫用非同步遠端程式時，用戶端必須選取 RPC 執行時間程式庫將用來通知呼叫完成的方法。 用戶端可以透過下列其中一種方式接收此通知：

-   事件。 用戶端可以指定當呼叫完成時要引發的事件。 如需詳細資訊，請參閱 [事件物件](/windows/desktop/Sync/event-objects)。
-   輪詢。 用戶端可以重複呼叫 [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus)。 如果傳回值是 RPC S ASYNC CALL PENDING 以外的任何其他值 \_ \_ \_ \_ ，則呼叫已完成。 這個方法所使用的 CPU 時間比這裡所述的其他方法更多。
-   APC。 用戶端可以指定呼叫完成時呼叫的 [ (APC) 的非同步程序呼叫 ](/windows/desktop/Sync/asynchronous-procedure-calls) 。 如需 APC 函數的原型，請參閱 [**RPCNOTIFICATION \_ 常式**](/previous-versions/aa375808(v=vs.80))。 將其事件參數設定為 RpcCallComplete 時，會呼叫 APC。 若要讓 Apc 分派，用戶端執行緒必須處於可提供警示等候狀態。

    如果非同步控制碼中的 **hThread** 欄位設定為0，則 apc 會排入進行非同步呼叫的執行緒上。 如果非零，則會將 Apc 排入 m 所指定的執行緒上。

-   國際 奧會。 I/o 完成通訊埠會以非同步控制碼中指定的參數來通知。 如需詳細資訊，請參閱 [**CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport)。
-   Windows 控制碼。  (HWND) 將訊息張貼至指定的視窗控制碼。

下列程式碼片段顯示初始化非同步控制碼並使用它來進行非同步遠端程序呼叫所需的必要步驟。


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



如這個範例所示，當非同步程序呼叫仍在擱置中時，您的用戶端程式可以執行同步遠端程序呼叫。 此用戶端會建立 RPC 執行時間程式庫的事件物件，以便在非同步呼叫完成時用來通知它。

> [!Note]  
> 如果在非同步呼叫期間引發 RPC 例外狀況，則不會從非同步 RPC 常式傳回完成的通知。

 

 

 