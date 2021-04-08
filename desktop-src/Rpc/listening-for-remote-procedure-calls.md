---
title: 接聽遠端程序呼叫
description: 當伺服器程式註冊其系結資訊，並在名稱服務資料庫中通告其存在時，就可以開始接聽遠端程序呼叫的端點。
ms.assetid: 1c116e44-03a4-4b86-ae37-0b9187981e53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69d9463e0591279377502394541190be685cccd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020734"
---
# <a name="listening-for-remote-procedure-calls"></a><span data-ttu-id="27c4a-103">接聽遠端程序呼叫</span><span class="sxs-lookup"><span data-stu-id="27c4a-103">Listening for Remote Procedure Calls</span></span>

<span data-ttu-id="27c4a-104">當伺服器程式註冊其系結資訊，並在名稱服務資料庫中通告其存在時，就可以開始接聽遠端程序呼叫的端點。</span><span class="sxs-lookup"><span data-stu-id="27c4a-104">After a server program registers its binding information and advertises its presence in a name service database, it can begin listening to the endpoint for remote procedure calls.</span></span> <span data-ttu-id="27c4a-105">伺服器程式會呼叫 [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) 函數，以監視遠端程式的用戶端調用的端點。</span><span class="sxs-lookup"><span data-stu-id="27c4a-105">Server programs call the [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) function to monitor endpoints for client invocations of remote procedures.</span></span>

<span data-ttu-id="27c4a-106">[**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten)的 DCE 規格指出，在伺服器程式中的函式呼叫 [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening)之前，不應傳回。</span><span class="sxs-lookup"><span data-stu-id="27c4a-106">The DCE specification of [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) indicates that it should not return until a function in the server program calls [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening).</span></span> <span data-ttu-id="27c4a-107">Microsoft RPC 的 **RpcServerListen** 執行會使用兩個未出現在 DCE 規格中的參數： *DontWait* 和 *MinimumCallThreads*。</span><span class="sxs-lookup"><span data-stu-id="27c4a-107">The Microsoft RPC implementation of **RpcServerListen** uses two parameters that do not appear in the DCE specification: *DontWait* and *MinimumCallThreads*.</span></span> <span data-ttu-id="27c4a-108">您的伺服器程式可以傳遞非零值給 *DontWait* 參數。</span><span class="sxs-lookup"><span data-stu-id="27c4a-108">Your server program can pass a nonzero value for the *DontWait* parameter.</span></span> <span data-ttu-id="27c4a-109">如果有的話， **RpcServerListen** 函式將會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="27c4a-109">If it does, the **RpcServerListen** function will return immediately.</span></span> <span data-ttu-id="27c4a-110">使用 [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) 常式來執行通常與 **RpcServerListen** 相關聯的等候作業。</span><span class="sxs-lookup"><span data-stu-id="27c4a-110">Use the [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) routine to perform the wait operation usually associated with **RpcServerListen**.</span></span>

 

 




