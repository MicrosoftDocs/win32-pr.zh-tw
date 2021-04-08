---
title: 下一個躍點
description: 路由有一或多個與其相關聯的下一個躍點。
ms.assetid: 90e5a79b-4fee-479c-9888-fcb3b6d38c1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26fcbc13ea7ad7c886ebd9f6f945f7cf6d6efe6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020927"
---
# <a name="next-hops"></a><span data-ttu-id="8d38b-103">下一個躍點</span><span class="sxs-lookup"><span data-stu-id="8d38b-103">Next Hops</span></span>

<span data-ttu-id="8d38b-104">路由有一或多個與其相關聯的下一個躍點。</span><span class="sxs-lookup"><span data-stu-id="8d38b-104">Routes have one or more next hops associated with them.</span></span> <span data-ttu-id="8d38b-105">如果目的地不是直接連線的網路，則下一個躍點是連出網路上下一個路由器 (或網路) 的位址，可將資料路由傳送至目的地。</span><span class="sxs-lookup"><span data-stu-id="8d38b-105">If the destination is not on a directly connected network, the next hop is the address of the next router (or network) on the outgoing network that can best route data to the destination.</span></span> <span data-ttu-id="8d38b-106">最佳路由是根據使用中的路由原則，具有最低成本的路由。</span><span class="sxs-lookup"><span data-stu-id="8d38b-106">The best route is the route that has the least cost, based on the routing policy in use.</span></span> <span data-ttu-id="8d38b-107">每個下一個躍點都可以用來將路徑上的資料轉送到目的地。</span><span class="sxs-lookup"><span data-stu-id="8d38b-107">Each next hop can be used to forward data on the path to the destination.</span></span> <span data-ttu-id="8d38b-108">用戶端所擁有的所有路由都會共用用戶端新增的一組常見的下一個躍點專案。</span><span class="sxs-lookup"><span data-stu-id="8d38b-108">All routes owned by a client share a common set of next-hop entries that were added by the client.</span></span>

<span data-ttu-id="8d38b-109">每個下一個躍點都是由下一個躍點的位址，以及用來觸達下一個躍點的介面索引來唯一識別。</span><span class="sxs-lookup"><span data-stu-id="8d38b-109">Each next hop is uniquely identified by the address of the next hop and the interface index used to reach the next hop.</span></span>

<span data-ttu-id="8d38b-110">如果下一個躍點本身未直接連接，則會標示為「遠端」下一個躍點。</span><span class="sxs-lookup"><span data-stu-id="8d38b-110">If the next hop itself is not directly connected, it is marked as a "remote" next hop.</span></span> <span data-ttu-id="8d38b-111">在此情況下，轉寄站必須使用下一個躍點的網路位址來執行另一個查閱。</span><span class="sxs-lookup"><span data-stu-id="8d38b-111">In this case, the forwarder must perform another lookup using the next hop's network address.</span></span> <span data-ttu-id="8d38b-112">需要此查閱才能找出用來連接遠端下一個躍點和目的地的「本機」下一個躍點。</span><span class="sxs-lookup"><span data-stu-id="8d38b-112">This lookup is necessary to find the "local" next hop used to reach the remote next hop and the destination.</span></span>

<span data-ttu-id="8d38b-113">路由表中的下一個躍點專案包括：</span><span class="sxs-lookup"><span data-stu-id="8d38b-113">A next-hop entry in the routing table includes:</span></span>

-   <span data-ttu-id="8d38b-114">下一個躍點的網路位址</span><span class="sxs-lookup"><span data-stu-id="8d38b-114">The network address of the next hop</span></span>
-   <span data-ttu-id="8d38b-115">下一個躍點的擁有者</span><span class="sxs-lookup"><span data-stu-id="8d38b-115">The owner of the next hop</span></span>
-   <span data-ttu-id="8d38b-116">輸出介面的識別碼</span><span class="sxs-lookup"><span data-stu-id="8d38b-116">The identifier of the outgoing interface</span></span>
-   <span data-ttu-id="8d38b-117">下一個躍點的狀態</span><span class="sxs-lookup"><span data-stu-id="8d38b-117">The state of the next hop</span></span>
-   <span data-ttu-id="8d38b-118">與下一個躍點相關聯的旗標</span><span class="sxs-lookup"><span data-stu-id="8d38b-118">Flags associated with the next hop</span></span>
-   <span data-ttu-id="8d38b-119">下一個躍點擁有者私用的資訊</span><span class="sxs-lookup"><span data-stu-id="8d38b-119">Information that is private to the owner of the next hop</span></span>
-   <span data-ttu-id="8d38b-120">目的地的控制碼，對應至遠端下一個躍點</span><span class="sxs-lookup"><span data-stu-id="8d38b-120">A handle to the destination corresponding to the remote next hop</span></span>

 

 




