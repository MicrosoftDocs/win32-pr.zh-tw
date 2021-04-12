---
description: 所有 IPv6 設定都是使用 Ipv6.exe 工具來完成。
ms.assetid: cb701070-cb7f-472a-97c7-1de9c0ddec0f
title: Ipv6.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e6fb0266609d22116cc72151e0db26006c415a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191334"
---
# <a name="ipv6exe"></a><span data-ttu-id="d3c44-103">Ipv6.exe</span><span class="sxs-lookup"><span data-stu-id="d3c44-103">Ipv6.exe</span></span>

<span data-ttu-id="d3c44-104">所有 IPv6 設定都是使用 Ipv6.exe 工具來完成。</span><span class="sxs-lookup"><span data-stu-id="d3c44-104">All IPv6 configuration is done with the Ipv6.exe tool.</span></span> <span data-ttu-id="d3c44-105">此工具主要用於查詢和設定 IPv6 介面、位址、快取和路由。</span><span class="sxs-lookup"><span data-stu-id="d3c44-105">This tool is primarily used for the querying and configuring of IPv6 interfaces, addresses, caches, and routes.</span></span> <span data-ttu-id="d3c44-106">以下是 IPv6 子命令：</span><span class="sxs-lookup"><span data-stu-id="d3c44-106">The following are IPv6 subcommands:</span></span>

<dl> <dt>

<span data-ttu-id="d3c44-107"><span id="ipv6_if__if__"></span><span id="IPV6_IF__IF__"></span>**ipv6 if** \[如果\#\]</span><span class="sxs-lookup"><span data-stu-id="d3c44-107"><span id="ipv6_if__if__"></span><span id="IPV6_IF__IF__"></span>**ipv6 if** \[if\#\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c44-108">顯示介面的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d3c44-108">Displays information about interfaces.</span></span> <span data-ttu-id="d3c44-109">如果指定了介面編號，則只會顯示該介面的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d3c44-109">If an interface number is specified, only information about that interface is displayed.</span></span> <span data-ttu-id="d3c44-110">否則，就會顯示所有介面的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d3c44-110">Otherwise, information about all interfaces is displayed.</span></span> <span data-ttu-id="d3c44-111">輸出會包含介面的連結層位址和指派給介面的 IPv6 地址清單，包括介面目前的 MTU，以及介面可支援的 (true) MTU 的最大值。</span><span class="sxs-lookup"><span data-stu-id="d3c44-111">The output includes the interface's link-layer address and the list of IPv6 addresses assigned to the interface, including the interface's current MTU and the maximum (true) MTU that the interface can support.</span></span>

<span data-ttu-id="d3c44-112">介面 \# 1 是用於回送的虛擬介面。</span><span class="sxs-lookup"><span data-stu-id="d3c44-112">Interface \#1 is a pseudo-interface used for loopback.</span></span> <span data-ttu-id="d3c44-113">介面 \# 2 是用於設定通道、自動通道和6to4 通道的虛擬介面。</span><span class="sxs-lookup"><span data-stu-id="d3c44-113">Interface \#2 is a pseudo-interface used for configured tunneling, automatic tunneling, and 6to4 tunneling.</span></span> <span data-ttu-id="d3c44-114">其他介面會依照建立的順序依序編號。</span><span class="sxs-lookup"><span data-stu-id="d3c44-114">Other interfaces are numbered sequentially in the order in which they are created.</span></span> <span data-ttu-id="d3c44-115">此順序會因一部電腦而異。</span><span class="sxs-lookup"><span data-stu-id="d3c44-115">This order varies from one computer to another.</span></span>

<span data-ttu-id="d3c44-116">*Aa* - *bb* - *cc* - *dd* - *ee* - *ff* 格式的連結層位址是乙太網路位址。</span><span class="sxs-lookup"><span data-stu-id="d3c44-116">Link-layer addresses in *aa*-*bb*-*cc*-*dd*-*ee*-*ff* format are Ethernet addresses.</span></span> <span data-ttu-id="d3c44-117">中 *的* 連結層位址。*b.**c.**d* 形式為6個以上的介面。</span><span class="sxs-lookup"><span data-stu-id="d3c44-117">Link-layer address in *a*.*b*.*c*.*d* form are 6-over-4 interfaces.</span></span> <span data-ttu-id="d3c44-118">如需 6-4 以上的詳細資訊，請參閱 RFC 2529。</span><span class="sxs-lookup"><span data-stu-id="d3c44-118">For more information on 6-over-4, see RFC 2529.</span></span>

<span data-ttu-id="d3c44-119">這兩個虛擬介面不會使用 IPv6 鄰居探索。</span><span class="sxs-lookup"><span data-stu-id="d3c44-119">The two pseudo-interfaces do not use IPv6 Neighbor Discovery.</span></span>

</dd> <dt>

<span data-ttu-id="d3c44-120"><span id="ipv6_ifc_if___forwards___advertises___-forwards___-advertises___mtu__bytes___site_site-identifier_"></span><span id="IPV6_IFC_IF___FORWARDS___ADVERTISES___-FORWARDS___-ADVERTISES___MTU__BYTES___SITE_SITE-IDENTIFIER_"></span>**ipv6 ifc** 如果 \# \[ 轉送轉送 \] \[ \] \[ -轉送 \] \[ 的 \] \[ mtu \# 位元組 \] \[ 網站識別碼\]</span><span class="sxs-lookup"><span data-stu-id="d3c44-120"><span id="ipv6_ifc_if___forwards___advertises___-forwards___-advertises___mtu__bytes___site_site-identifier_"></span><span id="IPV6_IFC_IF___FORWARDS___ADVERTISES___-FORWARDS___-ADVERTISES___MTU__BYTES___SITE_SITE-IDENTIFIER_"></span>**ipv6 ifc** if\# \[forwards\] \[advertises\] \[-forwards\] \[-advertises\] \[mtu \#bytes\] \[site site-identifier\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c44-121">控制介面屬性。</span><span class="sxs-lookup"><span data-stu-id="d3c44-121">Controls interface attributes.</span></span> <span data-ttu-id="d3c44-122">介面可以轉送，在這種情況下，它們會轉送具有未指派給介面之目的地位址的封包。</span><span class="sxs-lookup"><span data-stu-id="d3c44-122">Interfaces can be forwarding, in which case they forward packets with destination addresses not assigned to the interface.</span></span> <span data-ttu-id="d3c44-123">介面可以是廣告，在這種情況下，它們會傳送路由器通告。</span><span class="sxs-lookup"><span data-stu-id="d3c44-123">Interfaces can be advertising, in which case they send router advertisements.</span></span> <span data-ttu-id="d3c44-124">這些屬性可以獨立控制。</span><span class="sxs-lookup"><span data-stu-id="d3c44-124">These attributes can be independently controlled.</span></span> <span data-ttu-id="d3c44-125">介面會傳送路由器請求並接收路由器通告，或接收路由器請求並傳送路由器通告。</span><span class="sxs-lookup"><span data-stu-id="d3c44-125">An interface either sends router solicitations and receives router advertisements, or receives router solicitations and sends router advertisements.</span></span>

<span data-ttu-id="d3c44-126">因為這兩個虛擬介面不使用鄰近探索，所以無法將其設定為傳送路由器通告。</span><span class="sxs-lookup"><span data-stu-id="d3c44-126">Because the two pseudo-interfaces do not use Neighbor Discovery, they cannot be configured to send router advertisements.</span></span>

<span data-ttu-id="d3c44-127">轉寄可以縮寫為 forw，並公告為進階。</span><span class="sxs-lookup"><span data-stu-id="d3c44-127">Forwards can be abbreviated as forw, and advertised as adv.</span></span>

<span data-ttu-id="d3c44-128">介面的 MTU 也可以設定。</span><span class="sxs-lookup"><span data-stu-id="d3c44-128">The MTU for the interface can also be set.</span></span> <span data-ttu-id="d3c44-129">如果) 和大於或等於最小的 IPv6 MTU (1280 個位元組) ，則新的 MTU 必須小於或等於連結的最大 (true) MTU (（依 ipv6 回報）。</span><span class="sxs-lookup"><span data-stu-id="d3c44-129">The new MTU must be less than or equal to the link's maximum (true) MTU (as reported by ipv6 if) and greater than or equal to the minimum IPv6 MTU (1280 bytes).</span></span>

<span data-ttu-id="d3c44-130">您也可以變更介面的網站識別碼。</span><span class="sxs-lookup"><span data-stu-id="d3c44-130">The site-identifier for an interface can also be changed.</span></span> <span data-ttu-id="d3c44-131">網站識別碼會用於 sin6 \_ 範圍 \_ 識別碼欄位中，並具有網站本機位址。</span><span class="sxs-lookup"><span data-stu-id="d3c44-131">Site identifiers are used in the sin6\_scope\_id field with site-local addresses.</span></span>

</dd> <dt>

<span data-ttu-id="d3c44-132"><span id="ipv6_ifd_if_"></span><span id="IPV6_IFD_IF_"></span>**ipv6 ifd** if\#</span><span class="sxs-lookup"><span data-stu-id="d3c44-132"><span id="ipv6_ifd_if_"></span><span id="IPV6_IFD_IF_"></span>**ipv6 ifd** if\#</span></span>
</dt> <dd>

<span data-ttu-id="d3c44-133">刪除介面。</span><span class="sxs-lookup"><span data-stu-id="d3c44-133">Deletes an interface.</span></span> <span data-ttu-id="d3c44-134">無法刪除回送和通道虛擬介面。</span><span class="sxs-lookup"><span data-stu-id="d3c44-134">The loopback and tunnel pseudo-interfaces cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="d3c44-135"><span id="ipv6_nc__if___address__"></span><span id="IPV6_NC__IF___ADDRESS__"></span>**ipv6 nc** \[如果 \# \[ 位址\]\]</span><span class="sxs-lookup"><span data-stu-id="d3c44-135"><span id="ipv6_nc__if___address__"></span><span id="IPV6_NC__IF___ADDRESS__"></span>**ipv6 nc** \[if\# \[address\]\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c44-136">顯示鄰近快取的內容。</span><span class="sxs-lookup"><span data-stu-id="d3c44-136">Displays the contents of the neighbor cache.</span></span> <span data-ttu-id="d3c44-137">如果指定了介面編號，則只會顯示該介面的相鄰快取內容。</span><span class="sxs-lookup"><span data-stu-id="d3c44-137">If an interface number is specified, only the contents of that interface's neighbor cache are displayed.</span></span> <span data-ttu-id="d3c44-138">否則，會顯示所有介面的相鄰快取內容。</span><span class="sxs-lookup"><span data-stu-id="d3c44-138">Otherwise, the contents of all the interface's neighbor caches are displayed.</span></span> <span data-ttu-id="d3c44-139">如果指定了介面，則可以指定 IPv6 位址，只顯示該鄰近快取專案。</span><span class="sxs-lookup"><span data-stu-id="d3c44-139">If an interface is specified, an IPv6 address can be specified to display only that neighbor cache entry.</span></span>

<span data-ttu-id="d3c44-140">針對每個鄰近的快取專案，會顯示介面、IPv6 位址、連結層位址和觸達狀態。</span><span class="sxs-lookup"><span data-stu-id="d3c44-140">For each neighbor cache entry, the interface, IPv6 address, link-layer address, and reach state are displayed.</span></span>

</dd> <dt>

<span data-ttu-id="d3c44-141"><span id="ipv6_ncf__if___address__"></span><span id="IPV6_NCF__IF___ADDRESS__"></span>**ipv6 ncf** \[如果 \# \[ 位址\]\]</span><span class="sxs-lookup"><span data-stu-id="d3c44-141"><span id="ipv6_ncf__if___address__"></span><span id="IPV6_NCF__IF___ADDRESS__"></span>**ipv6 ncf** \[if\# \[address\]\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c44-142">清除指定的鄰近快取專案。</span><span class="sxs-lookup"><span data-stu-id="d3c44-142">Flushes the specified neighbor cache entries.</span></span> <span data-ttu-id="d3c44-143">只會清除沒有參考的鄰近快取專案。</span><span class="sxs-lookup"><span data-stu-id="d3c44-143">Only neighbor cache entries without references are purged.</span></span> <span data-ttu-id="d3c44-144">由於路由快取專案會保留鄰近快取專案的參考，因此應該先清除路由快取。</span><span class="sxs-lookup"><span data-stu-id="d3c44-144">Because route cache entries hold references to neighbor cache entries, the route cache should be flushed first.</span></span> <span data-ttu-id="d3c44-145">路由表專案也可以保留鄰近快取專案的參考。</span><span class="sxs-lookup"><span data-stu-id="d3c44-145">Routing table entries can also hold references to neighbor cache entries.</span></span>

</dd> <dt>

<span data-ttu-id="d3c44-146"><span id="ipv6_rc__if__address_"></span><span id="IPV6_RC__IF__ADDRESS_"></span>**ipv6 rc** \[如果 \# 位址\]</span><span class="sxs-lookup"><span data-stu-id="d3c44-146"><span id="ipv6_rc__if__address_"></span><span id="IPV6_RC__IF__ADDRESS_"></span>**ipv6 rc** \[if\# address\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c44-147">顯示路由快取的內容。</span><span class="sxs-lookup"><span data-stu-id="d3c44-147">Displays the contents of the route cache.</span></span> <span data-ttu-id="d3c44-148">路由快取是目的地快取的 Microsoft IPv6 實作為名稱。</span><span class="sxs-lookup"><span data-stu-id="d3c44-148">The route cache is the Microsoft IPv6 implementation name for the destination cache.</span></span> <span data-ttu-id="d3c44-149">如果指定了介面和位址，則會顯示透過介面到達位址的路由快取專案。</span><span class="sxs-lookup"><span data-stu-id="d3c44-149">If an interface and address are specified, the route cache entry for reaching the address through the interface is displayed.</span></span> <span data-ttu-id="d3c44-150">否則，會顯示所有的路由快取專案。</span><span class="sxs-lookup"><span data-stu-id="d3c44-150">Otherwise, all route cache entries are displayed.</span></span>

<span data-ttu-id="d3c44-151">針對每個路由快取專案，會顯示 IPv6 位址和目前的下一個躍點介面和鄰近位址。</span><span class="sxs-lookup"><span data-stu-id="d3c44-151">For each route cache entry, the IPv6 address and the current next-hop interface and neighbor address are displayed.</span></span> <span data-ttu-id="d3c44-152">與此目的地搭配使用的慣用來源位址、透過介面到達此目的地的目前路徑 MTU，以及判斷這是否為特定介面–路由快取專案也會顯示。</span><span class="sxs-lookup"><span data-stu-id="d3c44-152">The preferred source address for use with this destination, the current path MTU for reaching this destination through the interface, and the determination of whether this is an interface specific–route cache entry are also displayed.</span></span> <span data-ttu-id="d3c44-153">任何針對目的地位址的行動性) 的轉交位址 (也會一併顯示。</span><span class="sxs-lookup"><span data-stu-id="d3c44-153">Any care-of address (for mobility) for the destination address is displayed as well.</span></span>

<span data-ttu-id="d3c44-154">目的地位址可以有多個路由快取專案，最多可有一個用於每個輸出介面。</span><span class="sxs-lookup"><span data-stu-id="d3c44-154">A destination address can have multiple route cache entries—as many as one for each outgoing interface.</span></span> <span data-ttu-id="d3c44-155">不過，目的地位址最多可有一個不是介面特定的路由快取專案。</span><span class="sxs-lookup"><span data-stu-id="d3c44-155">However, a destination address can have a maximum of one route cache entry that is not interface-specific.</span></span> <span data-ttu-id="d3c44-156">只有在應用程式明確指定該連出介面時，才會使用特定的介面-路由快取專案。</span><span class="sxs-lookup"><span data-stu-id="d3c44-156">An interface specific–route cache entry is only used if the application explicitly specifies that outgoing interface.</span></span>

</dd> <dt>

<span data-ttu-id="d3c44-157"><span id="ipv6_rcf__if___address__"></span><span id="IPV6_RCF__IF___ADDRESS__"></span>**ipv6 rcf** \[如果 \# \[ 位址\]\]</span><span class="sxs-lookup"><span data-stu-id="d3c44-157"><span id="ipv6_rcf__if___address__"></span><span id="IPV6_RCF__IF___ADDRESS__"></span>**ipv6 rcf** \[if\# \[address\]\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c44-158">清除指定的路由快取專案。</span><span class="sxs-lookup"><span data-stu-id="d3c44-158">Flushes the specified route cache entries.</span></span>

</dd> <dt>

<span data-ttu-id="d3c44-159"><span id="ipv6_bc"></span><span id="IPV6_BC"></span>**ipv6 bc**</span><span class="sxs-lookup"><span data-stu-id="d3c44-159"><span id="ipv6_bc"></span><span id="IPV6_BC"></span>**ipv6 bc**</span></span>
</dt> <dd>

<span data-ttu-id="d3c44-160">顯示系結快取的內容，其保存家用位址與行動 IPv6 的轉交位址之間的系結。</span><span class="sxs-lookup"><span data-stu-id="d3c44-160">Displays the contents of the binding cache, which holds bindings between home addresses and care-of addresses for mobile IPv6.</span></span>

<span data-ttu-id="d3c44-161">針對每個系結，會顯示首頁位址、轉交位址、系結序號和存留期。</span><span class="sxs-lookup"><span data-stu-id="d3c44-161">For each binding, the home address, care-of address, binding sequence number, and lifetime are displayed.</span></span>

</dd> <dt>

<span data-ttu-id="d3c44-162"><span id="ipv6_adu_if__address__lifetime_VL__PL____anycast___unicast_"></span><span id="ipv6_adu_if__address__lifetime_vl__pl____anycast___unicast_"></span><span id="IPV6_ADU_IF__ADDRESS__LIFETIME_VL__PL____ANYCAST___UNICAST_"></span>**ipv6 adu** if \# /address \[ 存留期 VL \[ /PL \] \] \[ 任意傳播 \] \[ 單播\]</span><span class="sxs-lookup"><span data-stu-id="d3c44-162"><span id="ipv6_adu_if__address__lifetime_VL__PL____anycast___unicast_"></span><span id="ipv6_adu_if__address__lifetime_vl__pl____anycast___unicast_"></span><span id="IPV6_ADU_IF__ADDRESS__LIFETIME_VL__PL____ANYCAST___UNICAST_"></span>**ipv6 adu** if\#/address \[lifetime VL\[/PL\]\] \[anycast\] \[unicast\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c44-163">在介面上新增或移除單播或任意傳播位址指派。</span><span class="sxs-lookup"><span data-stu-id="d3c44-163">Adds or removes a unicast or anycast address assignment on an interface.</span></span> <span data-ttu-id="d3c44-164">除非指定了任意傳播，否則會對單播位址採取動作。</span><span class="sxs-lookup"><span data-stu-id="d3c44-164">The unicast address is acted upon unless anycast is specified.</span></span>

<span data-ttu-id="d3c44-165">如果未指定，則存留期為無限。</span><span class="sxs-lookup"><span data-stu-id="d3c44-165">Lifetime is infinite if unspecified.</span></span> <span data-ttu-id="d3c44-166">如果只指定有效的存留期，則慣用的存留期等於有效的存留期。</span><span class="sxs-lookup"><span data-stu-id="d3c44-166">If only a valid lifetime is specified, the preferred lifetime is equal to the valid lifetime.</span></span> <span data-ttu-id="d3c44-167">您可以指定無限期的存留期，或以秒為單位的有限值。</span><span class="sxs-lookup"><span data-stu-id="d3c44-167">An infinite lifetime may be specified, or a finite value in seconds.</span></span> <span data-ttu-id="d3c44-168">慣用的存留期必須小於或等於有效的存留期。</span><span class="sxs-lookup"><span data-stu-id="d3c44-168">The preferred lifetime must be less than or equal to the valid lifetime.</span></span> <span data-ttu-id="d3c44-169">指定零的存留期會導致移除位址。</span><span class="sxs-lookup"><span data-stu-id="d3c44-169">Specifying a lifetime of zero causes the address to be removed.</span></span>

<span data-ttu-id="d3c44-170">您可以縮寫存留期的存留期。</span><span class="sxs-lookup"><span data-stu-id="d3c44-170">You can abbreviate lifetime as life.</span></span>

<span data-ttu-id="d3c44-171">針對任意傳播位址，唯一有效的存留期值為零和無限。</span><span class="sxs-lookup"><span data-stu-id="d3c44-171">For anycast addresses, the only valid lifetime values are zero and infinite.</span></span>

</dd> <dt>

<span data-ttu-id="d3c44-172"><span id="ipv6_spt"></span><span id="IPV6_SPT"></span>**ipv6 spt**</span><span class="sxs-lookup"><span data-stu-id="d3c44-172"><span id="ipv6_spt"></span><span id="IPV6_SPT"></span>**ipv6 spt**</span></span>
</dt> <dd>

<span data-ttu-id="d3c44-173">顯示網站首碼表的目前內容。</span><span class="sxs-lookup"><span data-stu-id="d3c44-173">Displays the current contents of the site prefix table.</span></span>

<span data-ttu-id="d3c44-174">針對每個網站首碼，此命令會顯示首碼、網站首碼套用的介面，以及首碼存留期（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d3c44-174">For each site prefix, the command displays the prefix, the interface to which the site prefix applies, and the prefix lifetime in seconds.</span></span>

<span data-ttu-id="d3c44-175">網站首碼通常是從路由器公告自動設定的。</span><span class="sxs-lookup"><span data-stu-id="d3c44-175">Site prefixes are normally auto-configured from router advertisements.</span></span> <span data-ttu-id="d3c44-176">在 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) 函式中，會使用它們來篩選不當的網站-本機位址。</span><span class="sxs-lookup"><span data-stu-id="d3c44-176">They are used in the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function to filter inappropriate site-local addresses.</span></span>

</dd> <dt>

<span data-ttu-id="d3c44-177"><span id="ipv6_spu_prefix_if___lifetime_L_"></span><span id="ipv6_spu_prefix_if___lifetime_l_"></span><span id="IPV6_SPU_PREFIX_IF___LIFETIME_L_"></span>**ipv6 spu** 首碼（如果 \# \[ 存留期為 L）\]</span><span class="sxs-lookup"><span data-stu-id="d3c44-177"><span id="ipv6_spu_prefix_if___lifetime_L_"></span><span id="ipv6_spu_prefix_if___lifetime_l_"></span><span id="IPV6_SPU_PREFIX_IF___LIFETIME_L_"></span>**ipv6 spu** prefix if\# \[lifetime L\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c44-178">新增、移除或更新網站首碼資料表中的前置詞。</span><span class="sxs-lookup"><span data-stu-id="d3c44-178">Adds, removes, or updates a prefix in the site prefix table.</span></span>

<span data-ttu-id="d3c44-179">前置詞和介面編號是必要的。</span><span class="sxs-lookup"><span data-stu-id="d3c44-179">The prefix and interface number are required.</span></span> <span data-ttu-id="d3c44-180">如果未指定，網站首碼存留期（以秒為單位指定）預設為無限。</span><span class="sxs-lookup"><span data-stu-id="d3c44-180">The site prefix lifetime, specified in seconds, defaults to infinite if not specified.</span></span> <span data-ttu-id="d3c44-181">指定零的存留期會刪除網站首碼。</span><span class="sxs-lookup"><span data-stu-id="d3c44-181">Specifying a lifetime of zero deletes the site prefix.</span></span>

<span data-ttu-id="d3c44-182">主機或路由器的一般設定不需要此命令。</span><span class="sxs-lookup"><span data-stu-id="d3c44-182">This command is unnecessary for the normal configuration of hosts or routers.</span></span>

</dd> <dt>

<span data-ttu-id="d3c44-183"><span id="ipv6_rt"></span><span id="IPV6_RT"></span>**ipv6 rt**</span><span class="sxs-lookup"><span data-stu-id="d3c44-183"><span id="ipv6_rt"></span><span id="IPV6_RT"></span>**ipv6 rt**</span></span>
</dt> <dd>

<span data-ttu-id="d3c44-184">顯示路由表的目前內容。</span><span class="sxs-lookup"><span data-stu-id="d3c44-184">Displays the current contents of the routing table.</span></span>

<span data-ttu-id="d3c44-185">針對每個路由表專案，此命令會顯示路由前置詞、內部連結介面或介面上的下個躍點相鄰、偏好值 (較小的) 和存留期（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d3c44-185">For each routing table entry, the command displays the route prefix, an on-link interface or a next-hop neighbor on an interface, a preference value (smaller is preferred), and a lifetime in seconds.</span></span>

<span data-ttu-id="d3c44-186">路由表專案也可以有 **發行** 和 **過時** 屬性。</span><span class="sxs-lookup"><span data-stu-id="d3c44-186">Routing table entries may also have **publish** and **aging** attributes.</span></span> <span data-ttu-id="d3c44-187">根據預設，他們會存留存留期 (存留期，而不是剩餘的常數) ，也不會發佈 (用來建立) 的路由器公告。</span><span class="sxs-lookup"><span data-stu-id="d3c44-187">By default, they age (the lifetime counts down, rather than remaining constant) and are not published (not used in constructing router advertisements).</span></span>

<span data-ttu-id="d3c44-188">在主機上，路由表專案通常會從路由器公告自動設定。</span><span class="sxs-lookup"><span data-stu-id="d3c44-188">On hosts, routing table entries are normally auto-configured from router advertisements.</span></span>

</dd> <dt>

<span data-ttu-id="d3c44-189"><span id="ipv6_rtu_prefix_if___nexthop___lifetime_L___preference_P___publish___age___spl_site-prefix-length_"></span><span id="ipv6_rtu_prefix_if___nexthop___lifetime_l___preference_p___publish___age___spl_site-prefix-length_"></span><span id="IPV6_RTU_PREFIX_IF___NEXTHOP___LIFETIME_L___PREFERENCE_P___PUBLISH___AGE___SPL_SITE-PREFIX-LENGTH_"></span>**ipv6 rtu** 首碼 \# \[ （如果/nexthop \] \[ 存留期 L \] \[ 喜好設定 P \] \[ 發佈 \] \[ age） \] \[ spl 網站-首碼-長度\]</span><span class="sxs-lookup"><span data-stu-id="d3c44-189"><span id="ipv6_rtu_prefix_if___nexthop___lifetime_L___preference_P___publish___age___spl_site-prefix-length_"></span><span id="ipv6_rtu_prefix_if___nexthop___lifetime_l___preference_p___publish___age___spl_site-prefix-length_"></span><span id="IPV6_RTU_PREFIX_IF___NEXTHOP___LIFETIME_L___PREFERENCE_P___PUBLISH___AGE___SPL_SITE-PREFIX-LENGTH_"></span>**ipv6 rtu** prefix if\#\[/nexthop\] \[lifetime L\] \[preference P\] \[publish\] \[age\] \[spl site-prefix-length\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c44-190">新增或移除路由表中的路由。</span><span class="sxs-lookup"><span data-stu-id="d3c44-190">Adds or removes a route in the routing table.</span></span> <span data-ttu-id="d3c44-191">需要路由前置詞。</span><span class="sxs-lookup"><span data-stu-id="d3c44-191">The route prefix is required.</span></span> <span data-ttu-id="d3c44-192">前置詞可以連結至指定的介面（或下一個躍點），並以介面上的鄰近位址指定。</span><span class="sxs-lookup"><span data-stu-id="d3c44-192">The prefix can be on-link to a specified interface, or next-hop, specified with a neighbor address on an interface.</span></span> <span data-ttu-id="d3c44-193">路由可以有以秒為單位的存留期（預設為無限）和喜好設定，預設值為零或最慣用。</span><span class="sxs-lookup"><span data-stu-id="d3c44-193">The route can have a lifetime in seconds, with the default infinite, and a preference, with the default of zero, or most preferred.</span></span> <span data-ttu-id="d3c44-194">指定零的存留期會刪除路由。</span><span class="sxs-lookup"><span data-stu-id="d3c44-194">Specifying a lifetime of zero deletes the route.</span></span>

<span data-ttu-id="d3c44-195">如果路由是指定為已發佈的，表示它將用於建立路由器公告，則不會存在。</span><span class="sxs-lookup"><span data-stu-id="d3c44-195">If the route is specified as published, indicating it will be used in constructing router advertisements, it does not age.</span></span> <span data-ttu-id="d3c44-196">路由的存留期不會進行計數，因此實際上是無限的，但此值是在路由器公告中使用。</span><span class="sxs-lookup"><span data-stu-id="d3c44-196">The route's lifetime does not count down and therefore is effectively infinite, but the value is used in router advertisements.</span></span> <span data-ttu-id="d3c44-197">您可以選擇性地將路由指定為已發佈的路由，也就是年齡。</span><span class="sxs-lookup"><span data-stu-id="d3c44-197">Optionally, a route can be specified as a published route that also ages.</span></span> <span data-ttu-id="d3c44-198">依預設，nonpublished 路由一律為年齡。</span><span class="sxs-lookup"><span data-stu-id="d3c44-198">A nonpublished route by default always ages.</span></span>

<span data-ttu-id="d3c44-199">選擇性的 spl 子選項可以用來指定與路由相關聯的網站前置長度。</span><span class="sxs-lookup"><span data-stu-id="d3c44-199">The optional spl suboption can be used to specify a site prefix length associated with the route.</span></span> <span data-ttu-id="d3c44-200">只有在傳送路由器公告時，才會使用網站前置長度。</span><span class="sxs-lookup"><span data-stu-id="d3c44-200">The site prefix length is used only when sending router advertisements.</span></span>

<span data-ttu-id="d3c44-201">存留期可以縮寫為 life、喜好設定為 pref，然後發佈為 pub。</span><span class="sxs-lookup"><span data-stu-id="d3c44-201">Lifetime can be abbreviated as life, preference as pref, and publish as pub.</span></span>

</dd> </dl>

 

 



