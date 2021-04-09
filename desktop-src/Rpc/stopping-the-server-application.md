---
title: 停止伺服器應用程式
description: 伺服器應用程式可以藉由呼叫 RpcMgmtStopServerListening 和 RpcServerUnregisterIf，或直接結束主機進程，來停止接聽用戶端。
ms.assetid: 9d310cfb-72ad-448f-a66a-db6ac2478824
keywords:
- 遠端程序呼叫 RPC、工作、停止伺服器應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f95ba05588e0575949614e05370f86de78207d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675320"
---
# <a name="stopping-the-server-application"></a><span data-ttu-id="aa2b3-104">停止伺服器應用程式</span><span class="sxs-lookup"><span data-stu-id="aa2b3-104">Stopping the Server Application</span></span>

<span data-ttu-id="aa2b3-105">伺服器應用程式可以藉由呼叫 [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) 和 [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)，或直接結束主機進程，來停止接聽用戶端。</span><span class="sxs-lookup"><span data-stu-id="aa2b3-105">A server application can stop listening for clients by calling [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) and [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif), or by simply exiting the host process.</span></span> <span data-ttu-id="aa2b3-106">這兩種方法都是可接受的。</span><span class="sxs-lookup"><span data-stu-id="aa2b3-106">Both methods are acceptable.</span></span> <span data-ttu-id="aa2b3-107">如果伺服器採用第一種方法，則應該執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="aa2b3-107">If the server follows the first approach, it should implement the following steps:</span></span>

<span data-ttu-id="aa2b3-108">在發生例外狀況或呼叫 [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening)之前，伺服器函數 [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten)不會傳回呼叫程式。</span><span class="sxs-lookup"><span data-stu-id="aa2b3-108">The server function [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) does not return to the calling program until an exception occurs or until a call to [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) occurs.</span></span> <span data-ttu-id="aa2b3-109">依預設，只有另一個伺服器執行緒可以使用 **RpcMgmtStopServerListening** 來中止 RPC 伺服器。</span><span class="sxs-lookup"><span data-stu-id="aa2b3-109">By default, only another server thread is allowed to halt the RPC server by using **RpcMgmtStopServerListening**.</span></span> <span data-ttu-id="aa2b3-110">嘗試停止伺服器的用戶端將會收到錯誤的「 \_ RPC \_ 拒絕存取」錯誤 \_ 。</span><span class="sxs-lookup"><span data-stu-id="aa2b3-110">Clients who try to halt the server will receive the error RPC\_S\_ACCESS\_DENIED.</span></span> <span data-ttu-id="aa2b3-111">不過，您可以設定 RPC 允許部分或所有用戶端停止伺服器。</span><span class="sxs-lookup"><span data-stu-id="aa2b3-111">However, it is possible to configure RPC to allow some or all clients to stop the server.</span></span> <span data-ttu-id="aa2b3-112">如需詳細資訊，請參閱 **RpcMgmtStopServerListening** 。</span><span class="sxs-lookup"><span data-stu-id="aa2b3-112">See **RpcMgmtStopServerListening** for details.</span></span>

<span data-ttu-id="aa2b3-113">您也可以讓用戶端應用程式對伺服器上的 shutdown 常式進行遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="aa2b3-113">You can also have the client application make a remote procedure call to a shutdown routine on the server.</span></span> <span data-ttu-id="aa2b3-114">Shutdown 常式會呼叫 [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) 和 [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)。</span><span class="sxs-lookup"><span data-stu-id="aa2b3-114">The shutdown routine calls [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) and [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif).</span></span> <span data-ttu-id="aa2b3-115">本教學課程範例程式應用程式會使用這種方法，方法是將新的遠端函式（ **Shutdown**）新增至 Hellop 檔案。</span><span class="sxs-lookup"><span data-stu-id="aa2b3-115">This tutorial example program application uses this approach by adding a new remote function, **Shutdown**, to the file Hellop.c.</span></span>

<span data-ttu-id="aa2b3-116">在 **Shutdown** 函式中， [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) 的單一 null 參數表示本機應用程式應該停止接聽遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="aa2b3-116">In the **Shutdown** function, the single null parameter to [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) indicates that the local application should stop listening for remote procedure calls.</span></span> <span data-ttu-id="aa2b3-117">要 [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) 的兩個 null 參數是萬用字元，表示所有介面都應該取消註冊。</span><span class="sxs-lookup"><span data-stu-id="aa2b3-117">The two null parameters to [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) are wildcards, indicating that all interfaces should be unregistered.</span></span> <span data-ttu-id="aa2b3-118">**FALSE** 參數表示應該立即從登錄中移除介面，而不是等候暫止的呼叫完成。</span><span class="sxs-lookup"><span data-stu-id="aa2b3-118">The **FALSE** parameter indicates that the interface should be removed from the registry immediately, rather than waiting for pending calls to complete.</span></span>


```C++
/* add this function to hellop.c */
void Shutdown(void)
{
    RPC_STATUS status;
 
    status = RpcMgmtStopServerListening(NULL);
 
    if (status) 
    {
       exit(status);
    }
 
    status = RpcServerUnregisterIf(NULL, NULL, FALSE);
 
    if (status) 
    {
       exit(status);
    }
} //end Shutdown
```



 

 




