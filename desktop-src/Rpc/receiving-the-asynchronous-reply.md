---
title: 接收非同步回復
description: 在通知伺服器已傳送回復之後，用戶端會以非同步控制碼呼叫 RpcAsyncCompleteCall，以便接收回複。
ms.assetid: 48fb3777-d90a-474b-a1fa-9d034b5791e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9143daaf1f276f784086e2ec17efb47dfd1fb6e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382617"
---
# <a name="receiving-the-asynchronous-reply"></a><span data-ttu-id="813f2-103">接收非同步回復</span><span class="sxs-lookup"><span data-stu-id="813f2-103">Receiving the Asynchronous Reply</span></span>

<span data-ttu-id="813f2-104">在通知伺服器已傳送回復之後，用戶端會以非同步控制碼呼叫 [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) ，以便接收回複。</span><span class="sxs-lookup"><span data-stu-id="813f2-104">After it is notified that the server has sent a reply, the client calls [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) with the asynchronous handle so that it can receive the reply.</span></span> <span data-ttu-id="813f2-105">當 **RpcAsyncCompleteCall** 成功完成時， *回復* 參數會指向包含遠端函式之傳回值的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="813f2-105">When **RpcAsyncCompleteCall** has completed successfully, the *Reply* parameter points to a buffer that contains the return value of the remote function.</span></span> <span data-ttu-id="813f2-106">用戶端程式提供的任何緩衝區做為 \[ [**out**](/windows/desktop/Midl/out-idl) \] 或 \[ [**in**](/windows/desktop/Midl/in)，非同步遠端函式的 **out** \] 參數包含有效的資料。</span><span class="sxs-lookup"><span data-stu-id="813f2-106">Any buffers supplied by the client program as \[[**out**](/windows/desktop/Midl/out-idl)\] or \[[**in**](/windows/desktop/Midl/in), **out**\] parameters to the asynchronous remote function contain valid data.</span></span> <span data-ttu-id="813f2-107">如果用戶端在伺服器傳送回復之前呼叫 **RpcAsyncCompleteCall** ，該呼叫將會失敗，並傳回 RPC \_ S \_ 非同步呼叫的值 \_ 擱置中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="813f2-107">If the client calls **RpcAsyncCompleteCall** before the server has sent the reply, that call will fail and return a value of RPC\_S\_ASYNC\_CALL\_PENDING.</span></span>

<span data-ttu-id="813f2-108">如果您的用戶端程式使用 i/o 完成埠或事件來通知，它必須呼叫 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) ，以在不再需要時釋放埠或處理。</span><span class="sxs-lookup"><span data-stu-id="813f2-108">If your client program uses I/O completion ports or events for notification, it must call [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) to release the port or handle when it no longer needs them.</span></span>

 

 