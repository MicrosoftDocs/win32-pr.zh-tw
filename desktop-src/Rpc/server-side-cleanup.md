---
title: 伺服器端清除
description: " (RPC) 的伺服器端清除和遠端程序呼叫。"
ms.assetid: 8a48f698-82ae-464b-bdd9-f0245bbc7733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a66272fc3cca209d6825ac34d5158094ddff39
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021707"
---
# <a name="server-side-cleanup"></a><span data-ttu-id="aa461-103">伺服器端清除</span><span class="sxs-lookup"><span data-stu-id="aa461-103">Server-side Cleanup</span></span>

<span data-ttu-id="aa461-104">想像下列案例：</span><span class="sxs-lookup"><span data-stu-id="aa461-104">Imagine the following scenario:</span></span>

<span data-ttu-id="aa461-105">用戶端會開啟內容控制碼，然後停止或中斷與伺服器的連線。</span><span class="sxs-lookup"><span data-stu-id="aa461-105">A client opens a context handle, and then either stops or loses connectivity to the server.</span></span> <span data-ttu-id="aa461-106">伺服器如何偵測到用戶端已失敗，而內容控制碼應該會向下執行？</span><span class="sxs-lookup"><span data-stu-id="aa461-106">How does the server detect that the client has failed and the context handle should be run down?</span></span> <span data-ttu-id="aa461-107">有兩個個子案例：一個是用戶端以有條理的方式關閉。</span><span class="sxs-lookup"><span data-stu-id="aa461-107">There are two subscenarios: one is that the client is shut down in an orderly manner.</span></span> <span data-ttu-id="aa461-108">在這種情況下，它會通知伺服器它正在關機，而伺服器可以清除，包括執行內容執行。</span><span class="sxs-lookup"><span data-stu-id="aa461-108">In such case, it notifies the server that it is shutting down, and the server can clean up, including performing context run downs.</span></span> <span data-ttu-id="aa461-109">如果用戶端未以順序關機或無法通知伺服器，則伺服器會使用保持連接狀態，以判斷用戶端是否仍然可用。</span><span class="sxs-lookup"><span data-stu-id="aa461-109">If the client does not shut down in an orderly manner or it cannot notify the server, the server uses keep alives to determine whether the client is still available.</span></span> <span data-ttu-id="aa461-110">在伺服器端， [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) 函數沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="aa461-110">On the server side, the [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) function has no effect.</span></span> <span data-ttu-id="aa461-111">相反地，伺服器會使用每台電腦的全域-保持運作設定，預設為大約兩小時。</span><span class="sxs-lookup"><span data-stu-id="aa461-111">Instead, the server uses the global per machine–keep alive setting, which defaults to approximately two hours.</span></span> <span data-ttu-id="aa461-112">如果用戶端沒有回應伺服器的持續連線，連接就會關閉。</span><span class="sxs-lookup"><span data-stu-id="aa461-112">If the client does not respond to the server's keep alives, the connection is closed.</span></span> <span data-ttu-id="aa461-113">當指定之用戶端進程的所有連接都已關閉時，伺服器會清除並執行未完成的內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="aa461-113">When all connections to a given client process are closed, the server cleans up and runs down outstanding context handles.</span></span>

 

 




