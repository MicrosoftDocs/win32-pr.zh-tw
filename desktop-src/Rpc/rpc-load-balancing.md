---
title: RPC 負載平衡
description: RPC 負載平衡
ms.assetid: c646f748-d5f2-422d-8305-1f86c0dc61b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4039742fcfcc67280c610270908bed51034f691a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020891"
---
# <a name="rpc-load-balancing"></a><span data-ttu-id="338c0-103">RPC 負載平衡</span><span class="sxs-lookup"><span data-stu-id="338c0-103">RPC Load Balancing</span></span>

<span data-ttu-id="338c0-104">Microsoft RPC 負載平衡旨在提供可調整的解決方案，適用于需要高負載 [RPC OVER HTTP](remote-procedure-calls-using-rpc-over-http.md) 流量的案例。</span><span class="sxs-lookup"><span data-stu-id="338c0-104">Microsoft RPC Load Balancing is intended to provide a scalable solution for scenarios which demand a high load of [RPC over HTTP](remote-procedure-calls-using-rpc-over-http.md) traffic.</span></span> <span data-ttu-id="338c0-105">RPC Load Balancer 的主要用途是確保伺服器陣列可以服務 RPC/HTTP 流量，以改善擴充性。</span><span class="sxs-lookup"><span data-stu-id="338c0-105">The RPC Load Balancer’s primary purpose is to ensure RPC/HTTP traffic can be serviced by a server farm to improve scalability.</span></span> <span data-ttu-id="338c0-106">為了達成此目的，RPC 必須確保用戶端進程的所有連接都是由伺服器陣列中的相同伺服器端點所服務。</span><span class="sxs-lookup"><span data-stu-id="338c0-106">To achieve this, RPC must ensure that all connections from a client process are serviced by the same server endpoint in the server farm.</span></span> <span data-ttu-id="338c0-107">RPC Load Balancer 會實作為服務，以與 RPC over HTTP Proxy 服務一起執行。</span><span class="sxs-lookup"><span data-stu-id="338c0-107">The RPC Load Balancer is implemented as a service which runs in conjunction with the RPC over HTTP Proxy service.</span></span>

<span data-ttu-id="338c0-108">若要啟用負載平衡，在每部伺服器上執行的 RPC 負載平衡服務會彼此通訊，以判斷初始用戶端連接的慣用伺服器。</span><span class="sxs-lookup"><span data-stu-id="338c0-108">To enable load balancing, the RPC Load Balancing service running on each of the servers communicates with each other to determine the preferred server for the initial client connection.</span></span> <span data-ttu-id="338c0-109">此程式稱為仲裁，它會在初始用戶端連線時進行。</span><span class="sxs-lookup"><span data-stu-id="338c0-109">This process is called arbitration and it occurs at the time of the initial client connection.</span></span> <span data-ttu-id="338c0-110">為了減少跨伺服器流量，如果用戶端尚未與伺服器相關聯，則 RPC 負載平衡服務會選擇本機端點來服務連接。</span><span class="sxs-lookup"><span data-stu-id="338c0-110">To reduce cross server traffic, the RPC Load Balancing service chooses the local endpoint to service the connection if the client is not already associated with a server.</span></span> <span data-ttu-id="338c0-111">針對指定的用戶端連接，仲裁的結果有兩種：</span><span class="sxs-lookup"><span data-stu-id="338c0-111">For a given client connection, the outcome of arbitration is one of two possibilities:</span></span>

-   <span data-ttu-id="338c0-112">如果用戶端已建立連接，則第一次接收連接的伺服器將會處理後續的連線。</span><span class="sxs-lookup"><span data-stu-id="338c0-112">If the client has already made a connection, the server to first receive the connection will handle the subsequent connections.</span></span>
-   <span data-ttu-id="338c0-113">如果這是用戶端的第一個連接，仲裁將會導致本機伺服器處理連線，因此會產生來自用戶端的所有連接。</span><span class="sxs-lookup"><span data-stu-id="338c0-113">If this is the first connection from the client, arbitration will result in the local server handling the connection, and thus all connections from the client.</span></span> <span data-ttu-id="338c0-114">這項資訊一旦決定後，就會認可到伺服器陣列中的其他 RPC Load Balancer 服務，因此會通知伺服器處理所有用戶端的要求。</span><span class="sxs-lookup"><span data-stu-id="338c0-114">This information, once determined, will be committed to the other RPC Load Balancer services in the server farm, thus informing them of the server handling all of the client’s requests.</span></span>

<span data-ttu-id="338c0-115">本節提供下列主題中的 RPC 負載平衡總覽：</span><span class="sxs-lookup"><span data-stu-id="338c0-115">This section provides an overview of RPC Load Balancing in the following topics:</span></span>

-   [<span data-ttu-id="338c0-116">部署負載平衡</span><span class="sxs-lookup"><span data-stu-id="338c0-116">Deploying Load Balancing</span></span>](deploying-load-balancing.md)
-   [<span data-ttu-id="338c0-117">設定負載平衡</span><span class="sxs-lookup"><span data-stu-id="338c0-117">Configuring Load Balancing</span></span>](configuring-load-balancing.md)
-   [<span data-ttu-id="338c0-118">負載平衡的最佳作法</span><span class="sxs-lookup"><span data-stu-id="338c0-118">Load Balancing Best Practices</span></span>](load-balancing-best-practices.md)

## <a name="requirements"></a><span data-ttu-id="338c0-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="338c0-119">Requirements</span></span>

<span data-ttu-id="338c0-120">執行 windows Server 2008 R2 或更新版本的伺服器，以及執行 Windows 7 或更新版本 Windows 的用戶端，都支援 RPC 負載平衡服務。</span><span class="sxs-lookup"><span data-stu-id="338c0-120">The RPC Load Balancing service is supported on servers running Windows Server 2008 R2 or later and clients running Windows 7 or later versions of Windows.</span></span>

<span data-ttu-id="338c0-121">RPC Proxy 服務、RPC 負載平衡服務和伺服器端點都必須在同一部電腦上執行。</span><span class="sxs-lookup"><span data-stu-id="338c0-121">The RPC Proxy service, the RPC Load Balancing service and the server endpoints must all be running on the same machine.</span></span> <span data-ttu-id="338c0-122">此外，伺服器陣列中的所有伺服器都必須能夠服務所要求的端點。</span><span class="sxs-lookup"><span data-stu-id="338c0-122">Additionally, all servers in the server farm must be capable of servicing the requested endpoint.</span></span> <span data-ttu-id="338c0-123">如需設定 RPC Proxy 服務與 RPC 負載平衡服務的相關資訊，請參閱分別設定 [rpc OVER HTTP 的電腦](configuring-computers-for-rpc-over-http.md) 和設定 [負載平衡](configuring-load-balancing.md)。</span><span class="sxs-lookup"><span data-stu-id="338c0-123">For information on configuring the RPC Proxy service and the RPC Load Balancing service, see [Configuring Computers for RPC over HTTP](configuring-computers-for-rpc-over-http.md) and [Configuring Load Balancing](configuring-load-balancing.md), respectively.</span></span>

## <a name="limitations"></a><span data-ttu-id="338c0-124">限制</span><span class="sxs-lookup"><span data-stu-id="338c0-124">Limitations</span></span>

<span data-ttu-id="338c0-125">目前，RPC 負載平衡只支援每個資源一個伺服器陣列。</span><span class="sxs-lookup"><span data-stu-id="338c0-125">At this time, RPC Load Balancing supports only one server farm per resource.</span></span> <span data-ttu-id="338c0-126">所有伺服器陣列中的所有伺服器也必須能夠服務所有資源。</span><span class="sxs-lookup"><span data-stu-id="338c0-126">All servers in all server farms must be capable of servicing all resources as well.</span></span>

 

 




