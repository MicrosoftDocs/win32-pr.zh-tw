---
title: Teredo 元件
ms.assetid: 95d83030-b1de-4f09-b9d0-f443d9672ca1
description: 深入瞭解： Teredo 元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b4de66f38d5eb64b8321b6bb89e78fbb763e60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997076"
---
# <a name="teredo-components"></a><span data-ttu-id="66aff-103">Teredo 元件</span><span class="sxs-lookup"><span data-stu-id="66aff-103">Teredo Components</span></span>

<span data-ttu-id="66aff-104">[Teredo](about-teredo.md)基礎結構包含下列元件：</span><span class="sxs-lookup"><span data-stu-id="66aff-104">The [Teredo](about-teredo.md) infrastructure consists of the following components:</span></span>

## <a name="teredo-clients"></a><span data-ttu-id="66aff-105">Teredo 用戶端</span><span class="sxs-lookup"><span data-stu-id="66aff-105">Teredo Clients</span></span>

<span data-ttu-id="66aff-106">Teredo 用戶端是一個支援 Teredo 通道介面的 IPv6/IPv4 節點，透過 Teredo 通道介面，封包會透過 Teredo 轉送) 傳送至 IPv6 網際網路上的其他 Teredo 用戶端或節點 (。</span><span class="sxs-lookup"><span data-stu-id="66aff-106">A Teredo client is an IPv6/IPv4 node that supports a Teredo tunneling interface through which packets are tunneled to other Teredo clients or nodes on the IPv6 Internet (via a Teredo relay).</span></span> <span data-ttu-id="66aff-107">Teredo 用戶端會與 Teredo 伺服器通訊，以取得設定或使用以 Teredo 為基礎的 IPv6 位址所使用的位址首碼，以促進 IPv6 網際網路上其他 Teredo 用戶端或主機的通訊。</span><span class="sxs-lookup"><span data-stu-id="66aff-107">A Teredo client communicates with a Teredo server to obtain an address prefix from which a Teredo-based IPv6 address is configured or used to facilitate communication with other Teredo clients or hosts on the IPv6 Internet.</span></span>

<span data-ttu-id="66aff-108">Windows XP Service Pack 1 (SP1) 搭配 Advanced 網路套件、Windows XP Service Pack 2 (SP2) 、Windows Server 2003 （含 Service pack 1） (SP1) 、Windows Server 2003 Service pack 2 (SP2) 、Windows Vista 和 Windows Server 2008 全都包含 Teredo 用戶端。</span><span class="sxs-lookup"><span data-stu-id="66aff-108">Windows XP with Service Pack 1 (SP1) with the Advanced Networking Pack, Windows XP with Service Pack 2 (SP2), Windows Server 2003 with Service Pack 1 (SP1),Windows Server 2003 with Service Pack 2 (SP2), Windows Vista, and Windows Server 2008 all include the Teredo client.</span></span>

## <a name="teredo-servers"></a><span data-ttu-id="66aff-109">Teredo 伺服器</span><span class="sxs-lookup"><span data-stu-id="66aff-109">Teredo Servers</span></span>

<span data-ttu-id="66aff-110">Teredo 伺服器是一個同時連線至 IPv4 網際網路和 IPv6 網際網路的 IPv6/IPv4 節點，可支援接收封包的 Teredo 通道介面。</span><span class="sxs-lookup"><span data-stu-id="66aff-110">A Teredo server is an IPv6/IPv4 node that is connected to both the IPv4 Internet and the IPv6 Internet, and supports a Teredo tunneling interface over which packets are received.</span></span> <span data-ttu-id="66aff-111">Teredo 伺服器的一般角色是協助 Teredo 用戶端的位址設定，並協助 Teredo 用戶端與其他 Teredo 用戶端之間的初始通訊，或 Teredo 用戶端與 IPv6 專用主機之間的初始通訊。</span><span class="sxs-lookup"><span data-stu-id="66aff-111">The general role of the Teredo server is to assist in the address configuration of Teredo clients and to facilitate the initial communication between Teredo clients and other Teredo clients or between Teredo clients and IPv6-only hosts.</span></span> <span data-ttu-id="66aff-112">Teredo 伺服器會接聽 UDP 埠3544的 Teredo 流量。</span><span class="sxs-lookup"><span data-stu-id="66aff-112">The Teredo server listens on UDP port 3544 for Teredo traffic.</span></span>

<span data-ttu-id="66aff-113">與用戶端不同的是，Teredo 伺服器不包含在 Microsoft 作業系統中。</span><span class="sxs-lookup"><span data-stu-id="66aff-113">Unlike the client, the Teredo server is not included with Microsoft operating platforms.</span></span> <span data-ttu-id="66aff-114">為了方便 Windows 型 Teredo 用戶端電腦之間的通訊，Microsoft 已將 Teredo 伺服器部署在 IPv4 網際網路上。</span><span class="sxs-lookup"><span data-stu-id="66aff-114">To facilitate communication between Windows-based Teredo client computers, Microsoft has deployed Teredo servers on the IPv4 Internet.</span></span>

## <a name="teredo-relays"></a><span data-ttu-id="66aff-115">Teredo 轉送</span><span class="sxs-lookup"><span data-stu-id="66aff-115">Teredo Relays</span></span>

<span data-ttu-id="66aff-116">Teredo 轉送是一種 IPv6/IPv4 路由器，可以在 IPv4 網際網路上的 Teredo 用戶端之間轉送封包 (使用 Teredo 通道介面) 和 IPv6 專用主機。</span><span class="sxs-lookup"><span data-stu-id="66aff-116">A Teredo relay is an IPv6/IPv4 router that can forward packets between Teredo clients on the IPv4 Internet (using a Teredo tunneling interface) and IPv6-only hosts.</span></span> <span data-ttu-id="66aff-117">在某些情況下，Teredo 轉送會與 Teredo 伺服器互動，以促進 Teredo 用戶端與 IPv6 專用主機之間的初始通訊。</span><span class="sxs-lookup"><span data-stu-id="66aff-117">In some cases, the Teredo relay interacts with a Teredo server to facilitate initial communication between Teredo clients and IPv6-only hosts.</span></span> <span data-ttu-id="66aff-118">Teredo 轉送會接聽 UDP 埠3544的 Teredo 流量。</span><span class="sxs-lookup"><span data-stu-id="66aff-118">The Teredo relay listens on UDP port 3544 for Teredo traffic.</span></span>

<span data-ttu-id="66aff-119">如同 Teredo 伺服器，Microsoft 作業系統不包含 Teredo 轉送功能。</span><span class="sxs-lookup"><span data-stu-id="66aff-119">Like the Teredo server, Microsoft operating platforms do not include Teredo relay functionality.</span></span> <span data-ttu-id="66aff-120">Microsoft 目前不打算在 IPv4 網際網路上部署 Teredo 轉送。</span><span class="sxs-lookup"><span data-stu-id="66aff-120">Microsoft does not currently plan to deploy Teredo relays on the IPv4 Internet.</span></span> <span data-ttu-id="66aff-121">Teredo 轉送不需要與 Teredo 主機特定轉送通訊。</span><span class="sxs-lookup"><span data-stu-id="66aff-121">Teredo relays are not required to communicate with Teredo host-specific relays.</span></span>

## <a name="teredo-host-specific-relays"></a><span data-ttu-id="66aff-122">Teredo Host-Specific 轉送</span><span class="sxs-lookup"><span data-stu-id="66aff-122">Teredo Host-Specific Relays</span></span>

<span data-ttu-id="66aff-123">Teredo 用戶端與使用全域位址設定的 IPv6 主機之間的通訊必須經過 Teredo 轉送。</span><span class="sxs-lookup"><span data-stu-id="66aff-123">Communication between Teredo clients and IPv6 hosts that are configured with a global address must go through a Teredo relay.</span></span> <span data-ttu-id="66aff-124">連線到 IPv6 網際網路的 IPv6 專用主機需要這項功能。</span><span class="sxs-lookup"><span data-stu-id="66aff-124">This is required for IPv6-only hosts connected to the IPv6 Internet.</span></span> <span data-ttu-id="66aff-125">但是，當 IPv6 主機具備 IPv6 和 IPv4 功能，並同時連線到 IPv4 網際網路和 IPv6 網際網路時，就應該透過 IPv4 網際網路在 Teredo 用戶端與 IPv6 主機之間進行通訊，而不需要跨越 IPv6 網際網路並經過 Teredo 轉送。</span><span class="sxs-lookup"><span data-stu-id="66aff-125">However, when the IPv6 host is IPv6 and IPv4-capable and connected to both the IPv4 Internet and IPv6 Internet, then communication should occur between the Teredo client and the IPv6 host over the IPv4 Internet, rather than having to traverse the IPv6 Internet and go through a Teredo relay.</span></span>

<span data-ttu-id="66aff-126">Teredo 主機特定轉送是一種 IPv6/IPv4 節點，其具有 IPv4 網際網路和 IPv6 網際網路的介面和連線能力，且可以透過 IPv4 網際網路直接與 Teredo 用戶端通訊，而不需要中繼 Teredo 轉送。</span><span class="sxs-lookup"><span data-stu-id="66aff-126">A Teredo host-specific relay is an IPv6/IPv4 node that has an interface and connectivity to both the IPv4 Internet and the IPv6 Internet and can communicate directly with Teredo clients over the IPv4 Internet, without the need for an intermediate Teredo relay.</span></span> <span data-ttu-id="66aff-127">IPv4 網際網路的連線可以透過公用 IPv4 位址，或透過私人 IPv4 位址和連續的 NAT 來進行。</span><span class="sxs-lookup"><span data-stu-id="66aff-127">The connectivity to the IPv4 Internet can be through a public IPv4 address or through a private IPv4 address and a neighboring NAT.</span></span> <span data-ttu-id="66aff-128">IPv6 網際網路的連線能力可透過直接連線到 IPv6 網際網路，或透過 IPv6 轉換技術（例如6to4）進行，其中 IPv6 封包會在 IPv4 網際網路上進行通道處理。</span><span class="sxs-lookup"><span data-stu-id="66aff-128">The connectivity to the IPv6 Internet can be through a direct connection to the IPv6 Internet or through an IPv6 transition technology such as 6to4, where IPv6 packets are tunneled across the IPv4 Internet.</span></span> <span data-ttu-id="66aff-129">Teredo 主機特定轉送會接聽 UDP 埠3544的 Teredo 流量。</span><span class="sxs-lookup"><span data-stu-id="66aff-129">The Teredo host-specific relay listens on UDP port 3544 for Teredo traffic.</span></span>

<span data-ttu-id="66aff-130">具有 Advanced 網路功能套件的 windows XP （含 SP1）、Windows XP 加裝 SP2、Windows Server 2003 （含 SP1）、Windows Server 2003 SP2、Windows Vista 及 Windows Server 2008 包含 Teredo 主機特定轉送功能，如果電腦有指派的全域位址，則會自動啟用此功能。</span><span class="sxs-lookup"><span data-stu-id="66aff-130">Windows XP with SP1 with the Advanced Networking Pack, Windows XP with SP2, Windows Server 2003 with SP1, Windows Server 2003 with SP2, Windows Vista, and Windows Server 2008 include Teredo host-specific relay functionality, which is automatically enabled if the computer has a global address assigned.</span></span> <span data-ttu-id="66aff-131">系統會從原生 IPv6 路由器、ISATAP 路由器或6to4 路由器，在接收的路由器通告訊息中指派全域位址。</span><span class="sxs-lookup"><span data-stu-id="66aff-131">A global address is assigned in a received Router Advertisement message from a native IPv6 router, an ISATAP router, or a 6to4 router.</span></span> <span data-ttu-id="66aff-132">如果電腦沒有全域位址，便會啟用 Teredo 用戶端功能。</span><span class="sxs-lookup"><span data-stu-id="66aff-132">If the computer does not have a global address, Teredo client functionality is enabled.</span></span>

<span data-ttu-id="66aff-133">Teredo 主機特定轉送可讓 Teredo 用戶端有效率地與6to4 主機、使用非6to4 全域首碼的 IPv6 主機，或在其位址使用全域首碼的組織內的 ISATAP 或6over4 主機進行通訊，前提是這兩個主機都使用支援 Teredo 的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="66aff-133">The Teredo host-specific relay allows Teredo clients to efficiently communicate with 6to4 hosts, IPv6 hosts with a non-6to4 global prefix, or ISATAP or 6over4 hosts within organizations that use a global prefix for their addresses, provided both hosts are using a version of Windows that supports Teredo.</span></span>

 

 




