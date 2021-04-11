---
title: 處理非同步呼叫
description: 非同步函式的管理員常式一律會接收非同步控制碼做為第一個參數。 伺服器必須追蹤此控制碼，並在非同步遠端程序呼叫完成時，使用它來傳送回復。
ms.assetid: 4f38b68b-0bea-4fa7-8c7e-dd09e7daf8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e04dc7feed0d7bee47f6fa51583cf8de3a8e42f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372301"
---
# <a name="handling-asynchronous-calls"></a><span data-ttu-id="a8e2a-104">處理非同步呼叫</span><span class="sxs-lookup"><span data-stu-id="a8e2a-104">Handling Asynchronous Calls</span></span>

<span data-ttu-id="a8e2a-105">非同步函式的管理員常式一律會接收非同步控制碼做為第一個參數。</span><span class="sxs-lookup"><span data-stu-id="a8e2a-105">The manager routine of an asynchronous function always receives the asynchronous handle as the first parameter.</span></span> <span data-ttu-id="a8e2a-106">伺服器必須追蹤此控制碼，並在非同步遠端程序呼叫完成時，使用它來傳送回復。</span><span class="sxs-lookup"><span data-stu-id="a8e2a-106">The server must keep track of this handle and use it to send the reply when the asynchronous remote procedure call finishes.</span></span>

<span data-ttu-id="a8e2a-107">如果伺服器需要中止非同步 RPC，則會呼叫 [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)。</span><span class="sxs-lookup"><span data-stu-id="a8e2a-107">If the server needs to abort an asynchronous RPC, it calls [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall).</span></span> <span data-ttu-id="a8e2a-108">這個函式會執行與 [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) 相同的伺服器端清除，並且將伺服器應用程式所提供的例外狀況程式碼 (傳播) 回用戶端，不過它不會執行 out 引數的封送處理。</span><span class="sxs-lookup"><span data-stu-id="a8e2a-108">This function performs the same server-side cleanup as [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) and propagates an exception code (provided by the server application) back to the client, except that it does not perform marshalling of the out arguments.</span></span>

<span data-ttu-id="a8e2a-109">如需非同步程式的範例，請參閱傳送 [非同步回復](sending-the-asynchronous-reply.md)。</span><span class="sxs-lookup"><span data-stu-id="a8e2a-109">For an example of an asynchronous procedure, see [Sending the Asynchronous Reply](sending-the-asynchronous-reply.md).</span></span>

 

 




