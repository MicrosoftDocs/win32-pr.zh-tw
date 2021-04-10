---
title: 部署負載平衡
description: 部署負載平衡
ms.assetid: d80b8999-16c9-4fc8-a1cb-35a65f434884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc00430e8e93334c04dc74c57fc8b50db7d3c899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183296"
---
# <a name="deploying-load-balancing"></a><span data-ttu-id="60f8a-103">部署負載平衡</span><span class="sxs-lookup"><span data-stu-id="60f8a-103">Deploying Load Balancing</span></span>

<span data-ttu-id="60f8a-104">典型的部署環境和使用案例是使用 RPC 負載平衡器，如下所示：</span><span class="sxs-lookup"><span data-stu-id="60f8a-104">The typical deployment environment and use case is which the RPC Load balancer is utilized is shown below:</span></span>![rpc 負載平衡](images/rpc-load-balancing.png)

1.  <span data-ttu-id="60f8a-106">RPC 用戶端會對伺服器陣列進行 RPC/HTTP 連接。</span><span class="sxs-lookup"><span data-stu-id="60f8a-106">The RPC client makes an RPC/HTTP connection to the server farm.</span></span>
2.  <span data-ttu-id="60f8a-107">連線會透過網路轉送至前端負載平衡器</span><span class="sxs-lookup"><span data-stu-id="60f8a-107">The connection is forwarded through the network to a front end load balancer</span></span>
3.  <span data-ttu-id="60f8a-108">前端負載平衡器會選擇要為要求提供服務的伺服器。</span><span class="sxs-lookup"><span data-stu-id="60f8a-108">The front end load balancer chooses a server to service the request.</span></span> <span data-ttu-id="60f8a-109">在此範例中，前端負載平衡器會將連接轉送到伺服器1。</span><span class="sxs-lookup"><span data-stu-id="60f8a-109">In this example, the front end load balancer forwards the connection to Server 1.</span></span>
4.  <span data-ttu-id="60f8a-110">RPC 負載平衡器服務會仲裁連接。</span><span class="sxs-lookup"><span data-stu-id="60f8a-110">The RPC Load balancer service arbitrates the connection.</span></span> <span data-ttu-id="60f8a-111">它會判斷這是用戶端的第一個連接，並將連接與本機伺服器伺服器1產生關聯。</span><span class="sxs-lookup"><span data-stu-id="60f8a-111">It determines that this is the first connection from the client and associates the connection with the local server, Server 1.</span></span>
5.  <span data-ttu-id="60f8a-112">用戶端會進行第二個 RPC/HTTP 要求。</span><span class="sxs-lookup"><span data-stu-id="60f8a-112">The client makes a second RPC/HTTP request.</span></span>
6.  <span data-ttu-id="60f8a-113">要求會透過網路轉送至前端負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="60f8a-113">The request is forwarded through the network to the front end load balancer.</span></span>
7.  <span data-ttu-id="60f8a-114">前端負載平衡器會選擇要為要求提供服務的伺服器。</span><span class="sxs-lookup"><span data-stu-id="60f8a-114">The front end load balancer chooses a server to service the request.</span></span> <span data-ttu-id="60f8a-115">在此情況下，前端負載平衡器會選擇 Server 2 來服務要求。</span><span class="sxs-lookup"><span data-stu-id="60f8a-115">In this case, the front end load balancer chooses Server 2 to service the request.</span></span>
8.  <span data-ttu-id="60f8a-116">RPC Load Balancer 服務會仲裁連接。</span><span class="sxs-lookup"><span data-stu-id="60f8a-116">The RPC Load Balancer service arbitrates the connection.</span></span> <span data-ttu-id="60f8a-117">它會辨識出來自此用戶端的連線正在由伺服器1提供服務。</span><span class="sxs-lookup"><span data-stu-id="60f8a-117">It recognizes that connections from this client is being serviced by Server 1.</span></span>
9.  <span data-ttu-id="60f8a-118">連接會轉送至伺服器1。</span><span class="sxs-lookup"><span data-stu-id="60f8a-118">The connection is forwarded to Server 1.</span></span>

 

 




