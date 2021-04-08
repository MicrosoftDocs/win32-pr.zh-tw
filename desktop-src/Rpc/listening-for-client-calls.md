---
title: 接聽用戶端呼叫
description: 當您的伺服器應用程式已註冊其介面、建立必要的系結資訊，並註冊其端點之後，就可以開始接聽來自用戶端程式的遠端程序呼叫。
ms.assetid: ca9d24ed-0acc-45de-bbb2-761c56745a58
keywords:
- 遠端程序呼叫 RPC、工作、接聽用戶端呼叫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f375a4620e301f59d168bf5f7a4dbeedc0fb89f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840627"
---
# <a name="listening-for-client-calls"></a><span data-ttu-id="3a044-104">接聽用戶端呼叫</span><span class="sxs-lookup"><span data-stu-id="3a044-104">Listening for Client Calls</span></span>

<span data-ttu-id="3a044-105">當您的伺服器應用程式已註冊其介面、建立必要的系結資訊，並註冊其端點之後，就可以開始接聽來自用戶端程式的遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="3a044-105">After your server application has registered its interfaces, created the necessary binding information, and registered its endpoints, it is ready to begin listening for remote procedure calls from client programs.</span></span>

<span data-ttu-id="3a044-106">若要接聽遠端程序呼叫，您的伺服器程式必須呼叫 [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten)，如下列程式碼片段所示：</span><span class="sxs-lookup"><span data-stu-id="3a044-106">To listen for remote procedure calls, your server program must call [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), as shown in the following code fragment:</span></span>


```C++
RPC_STATUS status;
status = RpcServerListen(
    1,
    RPC_C_LISTEN_MAX_CALLS_DEFAULT,
    0);
```



<span data-ttu-id="3a044-107">RPC 伺服器有一或多個執行緒可挑選用戶端呼叫，並將它們傳遞至已註冊介面中的常式。</span><span class="sxs-lookup"><span data-stu-id="3a044-107">An RPC Server has one or more threads that pick up client calls and deliver them to the routines in the registered interfaces.</span></span> <span data-ttu-id="3a044-108">[**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten)函數的第一個參數是要建立之執行緒的最小數目。</span><span class="sxs-lookup"><span data-stu-id="3a044-108">The first parameter to the [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) function is the minimum number of threads to create.</span></span> <span data-ttu-id="3a044-109">參數只是提示;RPC 執行時間可能會選擇忽略它。</span><span class="sxs-lookup"><span data-stu-id="3a044-109">The parameter is only a hint; the RPC run time may chose to ignore it.</span></span>

<span data-ttu-id="3a044-110">[**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten)的第二個參數是要處理的並行遠端程序呼叫的最大數目。</span><span class="sxs-lookup"><span data-stu-id="3a044-110">The second parameter to [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) is the maximum number of concurrent remote procedure calls to handle.</span></span> <span data-ttu-id="3a044-111">如果您想要讓應用程式使用預設的最大值，請將 RPC \_ C \_ 接聽 \_ 的最大 \_ 呼叫預設值傳遞 \_ 為此參數的值。</span><span class="sxs-lookup"><span data-stu-id="3a044-111">If you want your application to use the default maximum value, pass RPC\_C\_LISTEN\_MAX\_CALLS\_DEFAULT as the value for this parameter.</span></span>

<span data-ttu-id="3a044-112">DCE 規格會呼叫 [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) 以繼續執行，直到它收到停止的信號為止。</span><span class="sxs-lookup"><span data-stu-id="3a044-112">The DCE specification calls for [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) to keep running until it receives a signal to stop.</span></span> <span data-ttu-id="3a044-113">這個函式有一個 Microsoft 擴充功能，可讓它開始接聽並立即返回。</span><span class="sxs-lookup"><span data-stu-id="3a044-113">One Microsoft extension to this function is to enable it to begin listening and return immediately.</span></span> <span data-ttu-id="3a044-114">如果您想要讓應用程式使用預設的 DCE 行為，請將第三個參數設定為零。</span><span class="sxs-lookup"><span data-stu-id="3a044-114">If you want your application to use the default DCE behavior, set the third parameter to zero.</span></span> <span data-ttu-id="3a044-115">如需詳細資訊，請參閱 [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten)、 [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening)和 [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) 。</span><span class="sxs-lookup"><span data-stu-id="3a044-115">See [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), and [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) for details.</span></span>

 

 




