---
title: 路由通訊協定
description: 路由通訊協定是一種向路由表管理員註冊的用戶端類型。 路由器會使用路由通訊協定來交換與目的地路由相關的資訊。
ms.assetid: 957ec896-94e3-4bdb-801a-12b861460fff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e64d12912494d0d6c20f484eba588b47670a808
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021353"
---
# <a name="routing-protocol"></a><span data-ttu-id="28655-104">路由通訊協定</span><span class="sxs-lookup"><span data-stu-id="28655-104">Routing Protocol</span></span>

<span data-ttu-id="28655-105">路由通訊協定是一種向路由表管理員註冊的用戶端類型。</span><span class="sxs-lookup"><span data-stu-id="28655-105">A routing protocol is a type of client that registers with the routing table manager.</span></span> <span data-ttu-id="28655-106">路由器會使用路由通訊協定來交換與目的地路由相關的資訊。</span><span class="sxs-lookup"><span data-stu-id="28655-106">Routers use routing protocols to exchange information regarding routes to a destination.</span></span>

<span data-ttu-id="28655-107">路由通訊協定為單播或多播。</span><span class="sxs-lookup"><span data-stu-id="28655-107">Routing protocols are either unicast or multicast.</span></span> <span data-ttu-id="28655-108">路由通訊協定會通告路由到目的地。</span><span class="sxs-lookup"><span data-stu-id="28655-108">Routing protocols advertise routes to a destination.</span></span>

<span data-ttu-id="28655-109">單播路由通訊協定會使用目的地的單播路由，將單播資料轉送至該目的地。</span><span class="sxs-lookup"><span data-stu-id="28655-109">A unicast route to a destination is used by a unicast routing protocol to forward unicast data to that destination.</span></span> <span data-ttu-id="28655-110">單播路由通訊協定的範例包括：路由資訊通訊協定 (RIP) 、Open 最短路徑 First (OSPF) 和邊界閘道協定 (BGP) 。</span><span class="sxs-lookup"><span data-stu-id="28655-110">Examples of unicast routing protocols include: Routing Information Protocol (RIP), Open Shortest Path First (OSPF), and Border Gateway Protocol (BGP).</span></span>

<span data-ttu-id="28655-111">某些多播路由通訊協定會使用目的地的多播路由，來建立用來從路由目的地網路上的主機轉寄多播資料的資訊， (稱為反向路徑轉送) 。多播路由通訊協定的範例包括：多播開放式最短路徑 First (MOSPF) 、距離向量多播路由通訊協定 (DVMRP) ，以及通訊協定獨立多播 (PIM) 。</span><span class="sxs-lookup"><span data-stu-id="28655-111">A multicast route to a destination is used by some multicast routing protocols to create the information that is used to forward multicast data from hosts on the destination network of the route (known as reverse path forwarding).Examples of multicast routing protocols include: Multicast Open Shortest Path First (MOSPF), Distance Vector Multicast Routing Protocol (DVMRP), and Protocol Independent Multicast (PIM).</span></span>

<span data-ttu-id="28655-112">路由表管理員支援相同通訊協定 (的多個實例，例如 Microsoft 的 OSPF 執行以及在路由器上執行的協力廠商 OSPF) 。</span><span class="sxs-lookup"><span data-stu-id="28655-112">The routing table manager supports multiple instances of the same protocol (such as Microsoft's implementation of OSPF and a third-party OSPF) running on the router.</span></span> <span data-ttu-id="28655-113">這可讓路由器使用每個版本的不同功能。</span><span class="sxs-lookup"><span data-stu-id="28655-113">This allows routers to use the different capabilities of each version.</span></span> <span data-ttu-id="28655-114">這些通訊協定具有不同的通訊協定識別碼。</span><span class="sxs-lookup"><span data-stu-id="28655-114">These protocols have different protocol identifiers.</span></span>

<span data-ttu-id="28655-115">通訊協定識別碼是由廠商識別碼和通訊協定特定識別碼所組成。</span><span class="sxs-lookup"><span data-stu-id="28655-115">Protocol identifiers are comprised of a vendor identifier and a protocol-specific identifier.</span></span> <span data-ttu-id="28655-116">通訊協定專屬的識別碼在不同的通訊協定（例如 Microsoft 的 OSPF 執行和協力廠商的 OSPF）上都是相同的。</span><span class="sxs-lookup"><span data-stu-id="28655-116">The protocol-specific identifier is the same for different implementations of the protocol, such as Microsoft's implementation of OSPF and a third-party implementation of OSPF.</span></span> <span data-ttu-id="28655-117">只有在合併廠商和通訊協定特定識別碼時，才會有路由通訊協定的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="28655-117">Only when the vendor and protocol-specific identifiers are combined is there a unique identifier for a routing protocol.</span></span>

<span data-ttu-id="28655-118">通訊協定識別碼相同的通訊協定 (也就是，相同的廠商識別碼和通訊協定專屬的識別碼) 可以多次向路由表管理員註冊。</span><span class="sxs-lookup"><span data-stu-id="28655-118">A protocol with the same protocol identifier (that is, the same vendor identifier and protocol-specific identifier) can register with the routing table manager multiple times.</span></span> <span data-ttu-id="28655-119">通訊協定每次都會使用不同的通訊協定實例識別碼進行註冊。</span><span class="sxs-lookup"><span data-stu-id="28655-119">Each time, the protocol registers using a different protocol instance identifier.</span></span> <span data-ttu-id="28655-120">例如，特定廠商的 OSPF 執行可註冊為廠商-OSPF-1 和廠商-OSPF-2。</span><span class="sxs-lookup"><span data-stu-id="28655-120">For example, an implementation of OSPF from a particular vendor can register as Vendor-OSPF-1 and Vendor-OSPF-2.</span></span> <span data-ttu-id="28655-121">這可讓特定的通訊協定執行分割其在路由表中保留的資訊。</span><span class="sxs-lookup"><span data-stu-id="28655-121">This enables a specific protocol implementation to partition the information that it keeps in the routing table.</span></span>

 

 




