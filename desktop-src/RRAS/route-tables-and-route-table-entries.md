---
title: 路由表和路由表專案
description: 路由表管理員會為每個通訊協定系列維護不同的路由表。
ms.assetid: 3848d93d-cc54-4a08-bd36-a9700cde6ce0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f118ec1d0a6f8fe4ef301654e139f217257c3a0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106995138"
---
# <a name="route-tables-and-route-table-entries"></a><span data-ttu-id="fdaa3-103">路由表和路由表專案</span><span class="sxs-lookup"><span data-stu-id="fdaa3-103">Route Tables and Route Table Entries</span></span>

<span data-ttu-id="fdaa3-104">**Windows Server 2003：** 此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。</span><span class="sxs-lookup"><span data-stu-id="fdaa3-104">**Windows Server 2003:** This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="fdaa3-105">新的應用程式應該使用路由表管理員第2版 API。</span><span class="sxs-lookup"><span data-stu-id="fdaa3-105">New applications should use the Routing Table Manager Version 2 API.</span></span>

<span data-ttu-id="fdaa3-106">路由表管理員會為每個通訊協定系列維護不同的路由表。</span><span class="sxs-lookup"><span data-stu-id="fdaa3-106">The routing table manager maintains distinct route tables for each protocol family.</span></span> <span data-ttu-id="fdaa3-107">目前， (IP) 和網際網路封包交換 (IPX) 路由通訊協定系列的網際網路通訊協定，提供明確的支援。</span><span class="sxs-lookup"><span data-stu-id="fdaa3-107">Currently, explicit support is provided for the Internet Protocol (IP) and Internet Packet Exchange (IPX) routing protocol families.</span></span> <span data-ttu-id="fdaa3-108">無論通訊協定系列為何，每個路由專案都會包含下列資訊：</span><span class="sxs-lookup"><span data-stu-id="fdaa3-108">Regardless of the protocol family, each route entry contains the following information:</span></span>

-   <span data-ttu-id="fdaa3-109">目的地網路。</span><span class="sxs-lookup"><span data-stu-id="fdaa3-109">Destination network.</span></span>
-   <span data-ttu-id="fdaa3-110">新增路由的通訊協定識別碼。</span><span class="sxs-lookup"><span data-stu-id="fdaa3-110">Identifier of the protocol that added the route.</span></span>
-   <span data-ttu-id="fdaa3-111">取得路由的介面索引。</span><span class="sxs-lookup"><span data-stu-id="fdaa3-111">Index of interface through which the route was obtained.</span></span> <span data-ttu-id="fdaa3-112">此索引值是指派給網路介面的數值， (以硬體為基礎或虛擬) 將資料傳輸到網路。</span><span class="sxs-lookup"><span data-stu-id="fdaa3-112">This index value is the numeric value assigned to a network interface (hardware-based or virtual) that transmits the data onto the network.</span></span> <span data-ttu-id="fdaa3-113">例如， (Ethernet NIC 或 802.1 b 的無線卡。 ) </span><span class="sxs-lookup"><span data-stu-id="fdaa3-113">(For example, an Ethernet NIC, or a 802.1b wireless card.)</span></span>
-   <span data-ttu-id="fdaa3-114">下一個躍點路由器的位址。</span><span class="sxs-lookup"><span data-stu-id="fdaa3-114">Address of the next hop router.</span></span> <span data-ttu-id="fdaa3-115">如果網路未直接連接，RRAS 會使用此路由器將封包轉送到目的地網路。</span><span class="sxs-lookup"><span data-stu-id="fdaa3-115">RRAS uses this router to forward packets to the destination network if the network is not directly connected.</span></span>
-   <span data-ttu-id="fdaa3-116">路由建立或上次更新的時間。</span><span class="sxs-lookup"><span data-stu-id="fdaa3-116">The time the route was created or last updated.</span></span>
-   <span data-ttu-id="fdaa3-117">此路由保留在路由表中的時間量。</span><span class="sxs-lookup"><span data-stu-id="fdaa3-117">The amount of time this route is kept in the routing table.</span></span> <span data-ttu-id="fdaa3-118">如果經過的時間量過久，而且路由尚未更新，路由表管理員就會從資料表中移除路由。</span><span class="sxs-lookup"><span data-stu-id="fdaa3-118">If this amount of time elapses, and the route has not been updated, the routing table manager removes the route from the table.</span></span> <span data-ttu-id="fdaa3-119">在此情況下，會將路由視為已 *過時*。</span><span class="sxs-lookup"><span data-stu-id="fdaa3-119">In this case, the route is said to have *aged out*.</span></span>
-   <span data-ttu-id="fdaa3-120">通訊協定系列的特定資料。</span><span class="sxs-lookup"><span data-stu-id="fdaa3-120">Data specific to the protocol family.</span></span> <span data-ttu-id="fdaa3-121">這項資料對 RTMv1 而言是透明的。</span><span class="sxs-lookup"><span data-stu-id="fdaa3-121">This data is transparent to RTMv1.</span></span> <span data-ttu-id="fdaa3-122">但是，如果此資料變更為指定為「最佳路由」的路由，路由表管理員就會送出路由變更通知。</span><span class="sxs-lookup"><span data-stu-id="fdaa3-122">However, if this data changes for a route designated as a "best route," the routing table manager sends out route-change notification.</span></span>
-   <span data-ttu-id="fdaa3-123">路由通訊協定特有的資料。</span><span class="sxs-lookup"><span data-stu-id="fdaa3-123">Data specific to the routing protocol.</span></span> <span data-ttu-id="fdaa3-124">這項資料對路由表管理員而言是完全透明的，在此情況下，對此資料所做的變更不會導致路由變更通知。</span><span class="sxs-lookup"><span data-stu-id="fdaa3-124">This data is completely transparent to the routing table manager, in that, changes to this data do not cause route change notification.</span></span>

<span data-ttu-id="fdaa3-125">下列值會以唯一的方式識別路由表中的路由：</span><span class="sxs-lookup"><span data-stu-id="fdaa3-125">The following values taken together uniquely identify a route in the routing table:</span></span>

-   <span data-ttu-id="fdaa3-126">目的地網路</span><span class="sxs-lookup"><span data-stu-id="fdaa3-126">Destination network</span></span>
-   <span data-ttu-id="fdaa3-127">通訊協定識別碼</span><span class="sxs-lookup"><span data-stu-id="fdaa3-127">Protocol identifier</span></span>
-   <span data-ttu-id="fdaa3-128">介面索引</span><span class="sxs-lookup"><span data-stu-id="fdaa3-128">Interface index</span></span>
-   <span data-ttu-id="fdaa3-129">下個躍點路由器的位址</span><span class="sxs-lookup"><span data-stu-id="fdaa3-129">Address of next-hop router</span></span>

<span data-ttu-id="fdaa3-130">一般而言，路由表管理員會針對這些參數值中的任何一個不同的路由建立不同的專案。</span><span class="sxs-lookup"><span data-stu-id="fdaa3-130">In general, the routing table manager creates separate entries for routes that differ in any of these parameter values.</span></span> <span data-ttu-id="fdaa3-131">但是，不會針對每個目的地網路保留多個專案的路由通訊協定，就會發生例外狀況。</span><span class="sxs-lookup"><span data-stu-id="fdaa3-131">However, an exception is made for routing protocols that do not keep more than one entry for each destination network.</span></span> <span data-ttu-id="fdaa3-132">針對這些通訊協定，路由表管理員會忽略介面索引或下一個躍點位址的差異。</span><span class="sxs-lookup"><span data-stu-id="fdaa3-132">For these protocols, the routing table manager ignores differences in interface index or next-hop address.</span></span> <span data-ttu-id="fdaa3-133">這類通訊協定的範例是開放式最短路徑 First (OSPF) 的 RRAS 執行。</span><span class="sxs-lookup"><span data-stu-id="fdaa3-133">An example of such a protocol is the RRAS implementation of Open Shortest Path First (OSPF).</span></span>

 

 




