---
description: IPV6 \_ 保護 \_ 等級通訊端選項可讓開發人員在 ipv6 通訊端上放置存取限制。
ms.assetid: bfb934b3-1e86-431f-a21c-880048d32d35
title: IPV6_PROTECTION_LEVEL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e2a8dd70bb1fb5b21f74f8939f11da0d9e2a3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971397"
---
# <a name="ipv6_protection_level"></a><span data-ttu-id="24daf-103">IPV6 \_ 保護 \_ 層級</span><span class="sxs-lookup"><span data-stu-id="24daf-103">IPV6\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="24daf-104">IPV6 \_ 保護 \_ 等級通訊端選項可讓開發人員在 ipv6 通訊端上放置存取限制。</span><span class="sxs-lookup"><span data-stu-id="24daf-104">The IPV6\_PROTECTION\_LEVEL socket option enables developers to place access restrictions on IPv6 sockets.</span></span> <span data-ttu-id="24daf-105">這類限制可以讓應用程式在私人 LAN 上執行，簡便又穩當地強化應用程式對外部攻擊的抵禦。</span><span class="sxs-lookup"><span data-stu-id="24daf-105">Such restrictions enable an application running on a private LAN to simply and robustly harden itself against external attacks.</span></span> <span data-ttu-id="24daf-106">IPV6 \_ 保護 \_ 等級通訊端選項可擴大或縮小接聽通訊端的範圍，並在適當時啟用不受限制的公用和私用使用者存取，或僅視需要限制對相同網站的存取。</span><span class="sxs-lookup"><span data-stu-id="24daf-106">The IPV6\_PROTECTION\_LEVEL socket option widens or narrows the scope of a listening socket, enabling unrestricted access from public and private users when appropriate, or restricting access only to the same site, as required.</span></span>

<span data-ttu-id="24daf-107">IPV6 \_ 保護 \_ 等級目前有三個已定義的保護層級。</span><span class="sxs-lookup"><span data-stu-id="24daf-107">IPV6\_PROTECTION\_LEVEL currently has three defined protection levels.</span></span>



| <span data-ttu-id="24daf-108">保護等級</span><span class="sxs-lookup"><span data-stu-id="24daf-108">Protection level</span></span>                                                                                                                                 | <span data-ttu-id="24daf-109">描述</span><span class="sxs-lookup"><span data-stu-id="24daf-109">Description</span></span>                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24daf-110"><span id="PROTECTION_LEVEL_UNRESTRICTED"></span><span id="protection_level_unrestricted"></span>不 \_ 受限制的保護層級 \_</span><span class="sxs-lookup"><span data-stu-id="24daf-110"><span id="PROTECTION_LEVEL_UNRESTRICTED"></span><span id="protection_level_unrestricted"></span>PROTECTION\_LEVEL\_UNRESTRICTED</span></span><br/>       | <span data-ttu-id="24daf-111">由設計用來在網際網路上運作的應用程式所使用，包括利用 Windows (Teredo 內建的 IPv6 NAT 遍歷功能的應用程式，例如) 。</span><span class="sxs-lookup"><span data-stu-id="24daf-111">Used by applications designed to operate across the Internet, including applications taking advantage of IPv6 NAT traversal capabilities built into Windows (Teredo, for example).</span></span> <span data-ttu-id="24daf-112">這些應用程式可能會略過 IPv4 防火牆，因此必須加強應用程式，以抵禦在開啟的通訊埠位置遭受的直接網路攻擊。</span><span class="sxs-lookup"><span data-stu-id="24daf-112">These applications may bypass IPv4 firewalls, so applications must be hardened against Internet attacks directed at the opened port.</span></span><br/> |
| <span data-ttu-id="24daf-113"><span id="PROTECTION_LEVEL_EDGERESTRICTED"></span><span id="protection_level_edgerestricted"></span>保護 \_ 層級 \_ EDGERESTRICTED</span><span class="sxs-lookup"><span data-stu-id="24daf-113"><span id="PROTECTION_LEVEL_EDGERESTRICTED"></span><span id="protection_level_edgerestricted"></span>PROTECTION\_LEVEL\_EDGERESTRICTED</span></span><br/> | <span data-ttu-id="24daf-114">由設計來在網際網路上操作的應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="24daf-114">Used by applications designed to operate across the Internet.</span></span> <span data-ttu-id="24daf-115">此設定不允許使用 Windows Teredo 執行的 NAT 遍歷。</span><span class="sxs-lookup"><span data-stu-id="24daf-115">This setting does not allow NAT traversal using the Windows Teredo implementation.</span></span> <span data-ttu-id="24daf-116">這些應用程式可能會略過 IPv4 防火牆，因此必須加強應用程式，以抵禦在開啟的通訊埠位置遭受的直接網路攻擊。</span><span class="sxs-lookup"><span data-stu-id="24daf-116">These applications may bypass IPv4 firewalls, so applications must be hardened against Internet attacks directed at the opened port.</span></span><br/>                                   |
| <span data-ttu-id="24daf-117"><span id="PROTECTION_LEVEL_RESTRICTED"></span><span id="protection_level_restricted"></span>\_ \_ 受限制的保護等級</span><span class="sxs-lookup"><span data-stu-id="24daf-117"><span id="PROTECTION_LEVEL_RESTRICTED"></span><span id="protection_level_restricted"></span>PROTECTION\_LEVEL\_RESTRICTED</span></span><br/>             | <span data-ttu-id="24daf-118">由未執行網際網路案例的內部網路應用程式所使用。</span><span class="sxs-lookup"><span data-stu-id="24daf-118">Used by intranet applications that do not implement Internet scenarios.</span></span> <span data-ttu-id="24daf-119">這些應用程式通常不會就網路攻擊測試進行測試或是採取強化。</span><span class="sxs-lookup"><span data-stu-id="24daf-119">These applications are generally not tested or hardened against Internet-style attacks.</span></span><br/> <span data-ttu-id="24daf-120">這個設定會將接收傳輸限制於僅連結和本機之間。</span><span class="sxs-lookup"><span data-stu-id="24daf-120">This setting will limit the received traffic to link-local only.</span></span><br/>                                                                             |



 

<span data-ttu-id="24daf-121">下列程式碼範例會提供每個的定義值：</span><span class="sxs-lookup"><span data-stu-id="24daf-121">The following code example provides the defined values for each:</span></span>

``` syntax
#define PROTECTION_LEVEL_UNRESTRICTED   10  /* for peer-to-peer apps */
#define PROTECTION_LEVEL_EDGERESTRICTED 20  /* Same as unrestricted, except for Teredo  */
#define PROTECTION_LEVEL_RESTRICTED     30  /* for Intranet apps     */
```

<span data-ttu-id="24daf-122">這些值是互斥的，無法在單一 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函式呼叫中結合。</span><span class="sxs-lookup"><span data-stu-id="24daf-122">These values are mutually exclusive, and cannot be combined in a single [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function call.</span></span> <span data-ttu-id="24daf-123">此通訊端選項的其他值是保留的。</span><span class="sxs-lookup"><span data-stu-id="24daf-123">Other values for this socket option are reserved.</span></span> <span data-ttu-id="24daf-124">這些保護層級只適用于連入連線。</span><span class="sxs-lookup"><span data-stu-id="24daf-124">These protection levels apply only to incoming connections.</span></span> <span data-ttu-id="24daf-125">設定這個通訊端選項對輸出封包或連接沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="24daf-125">Setting this socket option has no effect on outbound packets or connections.</span></span>

<span data-ttu-id="24daf-126">在 Windows 7 和 Windows Server 2008 R2 上，未指定 IPV6 保護層級的預設值， \_ \_ 且 **保護 \_ 等級 \_ 預設** 值定義為-1，這是 IPV6 \_ 保護層級的不合法值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="24daf-126">On Windows 7 and Windows Server 2008 R2, the default value for IPV6\_PROTECTION\_LEVEL is unspecified and **PROTECTION\_LEVEL\_DEFAULT** is defined to -1, an illegal value for IPV6\_PROTECTION\_LEVEL.</span></span>

<span data-ttu-id="24daf-127">在 Windows Vista 和 Windows Server 2008 上，IPV6 \_ 保護層級的預設值 \_ 是不 **\_ \_ 受保護的保護層** 級，而 **保護 \_ 等級 \_ 預設** 值定義為-1，這是 IPV6 \_ 保護層級的不合法值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="24daf-127">On Windows Vista and Windows Server 2008, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED** and **PROTECTION\_LEVEL\_DEFAULT** is defined to -1, an illegal value for IPV6\_PROTECTION\_LEVEL.</span></span>

<span data-ttu-id="24daf-128">在 Windows Server 2003 和 Windows XP 上，IPV6 \_ 保護層級的預設值 \_ 為 **保護 \_ 層級 \_ EDGERESTRICTED** ，而 **保護 \_ 等級 \_ 預設** 值定義為 **保護 \_ 層級 \_ EDGERESTRICTED**。</span><span class="sxs-lookup"><span data-stu-id="24daf-128">On Windows Server 2003 and Windows XP, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_EDGERESTRICTED** and **PROTECTION\_LEVEL\_DEFAULT** is defined to be **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span>

> [!Note]  
> <span data-ttu-id="24daf-129">在系 \_ \_ 結器之前，應設定 IPV6 保護等級通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="24daf-129">The IPV6\_PROTECTION\_LEVEL socket option should be set before the socket is bound.</span></span> <span data-ttu-id="24daf-130">否則，在 [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) 和 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 呼叫之間收到的封包會符合 **保護 \_ 層級 \_ EDGERESTRICTED**，並且可傳遞至應用程式。</span><span class="sxs-lookup"><span data-stu-id="24daf-130">Otherwise, packets received between [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) and [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) calls will conform to **PROTECTION\_LEVEL\_EDGERESTRICTED**, and may be delivered to the application.</span></span>

 

<span data-ttu-id="24daf-131">下表說明將每個保護等級套用至接聽通訊端的效果。</span><span class="sxs-lookup"><span data-stu-id="24daf-131">The following table describes the effect of applying each protection level to a listening socket.</span></span>

<span data-ttu-id="24daf-132">保護等級</span><span class="sxs-lookup"><span data-stu-id="24daf-132">Protection level</span></span>

<span data-ttu-id="24daf-133">允許連入流量</span><span class="sxs-lookup"><span data-stu-id="24daf-133">Incoming traffic permitted</span></span>

<span data-ttu-id="24daf-134">相同網站</span><span class="sxs-lookup"><span data-stu-id="24daf-134">Same site</span></span>

<span data-ttu-id="24daf-135">外部</span><span class="sxs-lookup"><span data-stu-id="24daf-135">External</span></span>

<span data-ttu-id="24daf-136"> (Teredo) 的 NAT 遍歷</span><span class="sxs-lookup"><span data-stu-id="24daf-136">NAT traversal (Teredo)</span></span>

<span data-ttu-id="24daf-137">\_ \_ 受限制的保護等級</span><span class="sxs-lookup"><span data-stu-id="24daf-137">PROTECTION\_LEVEL\_RESTRICTED</span></span>

<span data-ttu-id="24daf-138">是</span><span class="sxs-lookup"><span data-stu-id="24daf-138">Yes</span></span>

<span data-ttu-id="24daf-139">否</span><span class="sxs-lookup"><span data-stu-id="24daf-139">No</span></span>

<span data-ttu-id="24daf-140">否</span><span class="sxs-lookup"><span data-stu-id="24daf-140">No</span></span>

<span data-ttu-id="24daf-141">保護 \_ 層級 \_ EDGERESTRICTED</span><span class="sxs-lookup"><span data-stu-id="24daf-141">PROTECTION\_LEVEL\_EDGERESTRICTED</span></span>

<span data-ttu-id="24daf-142">是</span><span class="sxs-lookup"><span data-stu-id="24daf-142">Yes</span></span>

<span data-ttu-id="24daf-143">是</span><span class="sxs-lookup"><span data-stu-id="24daf-143">Yes</span></span>

<span data-ttu-id="24daf-144">否</span><span class="sxs-lookup"><span data-stu-id="24daf-144">No</span></span>

<span data-ttu-id="24daf-145">不 \_ 受限制的保護層級 \_</span><span class="sxs-lookup"><span data-stu-id="24daf-145">PROTECTION\_LEVEL\_UNRESTRICTED</span></span>

<span data-ttu-id="24daf-146">是</span><span class="sxs-lookup"><span data-stu-id="24daf-146">Yes</span></span>

<span data-ttu-id="24daf-147">是</span><span class="sxs-lookup"><span data-stu-id="24daf-147">Yes</span></span>

<span data-ttu-id="24daf-148">是</span><span class="sxs-lookup"><span data-stu-id="24daf-148">Yes</span></span>



 

<span data-ttu-id="24daf-149">在上表中， **相同的網站** 資料行是下列各項的組合：</span><span class="sxs-lookup"><span data-stu-id="24daf-149">In the table above, the **Same site** column is a combination of the following:</span></span>

-   <span data-ttu-id="24daf-150">連結本機位址</span><span class="sxs-lookup"><span data-stu-id="24daf-150">Link local addresses</span></span>
-   <span data-ttu-id="24daf-151">網站本機位址</span><span class="sxs-lookup"><span data-stu-id="24daf-151">Site Local addresses</span></span>
-   <span data-ttu-id="24daf-152">已知屬於相同網站的全域位址 (符合網站首碼資料表) </span><span class="sxs-lookup"><span data-stu-id="24daf-152">Global addresses known to belong to the same site (matching the site prefix table)</span></span>

<span data-ttu-id="24daf-153">在 Windows 7 和 Windows Server 2008 R2 上，未 \_ 指定 IPV6 保護層級的預設值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="24daf-153">On Windows 7 and Windows Server 2008 R2, the default value for IPV6\_PROTECTION\_LEVEL is unspecified.</span></span> <span data-ttu-id="24daf-154">如果本機電腦上沒有安裝 edge 遍歷感知防火牆軟體 (Windows 防火牆已停用，或已安裝其他會忽略 Teredo 流量) 的防火牆，則只有在您將 [IPV6 \_ 保護 \_ 等級通訊端] 選項設定為 [不 **\_ \_ 受保護的保護等級**] 時，才會收到 Teredo 流量。</span><span class="sxs-lookup"><span data-stu-id="24daf-154">If there is no edge-traversal aware firewall software installed on the local computer (Windows firewall is disabled or some other firewall is installed that ignores Teredo traffic), you will receive Teredo traffic only if you set the IPV6\_PROTECTION\_LEVEL socket option to **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span> <span data-ttu-id="24daf-155">不過，Windows 防火牆或任何邊緣遍歷感知防火牆原則可能會根據防火牆的原則設定來忽略此選項。</span><span class="sxs-lookup"><span data-stu-id="24daf-155">However, Windows firewall or any edge-traversal aware firewall policy may ignore this option based on policy settings for the firewall.</span></span> <span data-ttu-id="24daf-156">藉由將此通訊端選項設定為不 **\_ \_ 受限制的保護層級**，應用程式就會傳達其明確意圖，以接收在本機電腦上安裝的主機防火牆的邊緣流量。</span><span class="sxs-lookup"><span data-stu-id="24daf-156">By setting this socket option to **PROTECTION\_LEVEL\_UNRESTRICTED**, the application is communicating its explicit intent to receive edge traversed traffic by the host firewall installed on the local machine.</span></span> <span data-ttu-id="24daf-157">因此，如果已安裝 edge 遍歷感知主機防火牆，它就會有接受封包的最後決定。</span><span class="sxs-lookup"><span data-stu-id="24daf-157">So if there is an edge-traversal aware host firewall installed, it will have the final decision on accepting a packet.</span></span> <span data-ttu-id="24daf-158">依預設，不會設定任何通訊端選項：</span><span class="sxs-lookup"><span data-stu-id="24daf-158">By default, without any socket option set:</span></span>

-   <span data-ttu-id="24daf-159">o 如果已啟用 Windows 防火牆 (或在本機電腦上安裝了另一個邊緣進行感知的主機防火牆) ，則會觀察到它所強制執行的任何內容。</span><span class="sxs-lookup"><span data-stu-id="24daf-159">o If Windows firewall is enabled (or another edge-traversal aware host firewall is installed) on the local computer, whatever it enforces will be observed.</span></span> <span data-ttu-id="24daf-160">一般邊緣遍歷感知主機防火牆預設會封鎖 Teredo 流量。</span><span class="sxs-lookup"><span data-stu-id="24daf-160">Typical edge-traversal aware host firewall will block Teredo traffic by default.</span></span> <span data-ttu-id="24daf-161">因此，應用程式會觀察到預設值，就像是 **保護 \_ 層級 \_ EDGERESTRICTED** 一樣。</span><span class="sxs-lookup"><span data-stu-id="24daf-161">Therefore applications will observe the default as if it was **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span>
-   <span data-ttu-id="24daf-162">o 如果未啟用 Windows 防火牆，且本機系統上未安裝任何其他邊緣遍歷感知主機防火牆，則預設值將會是 **保護 \_ 層級 \_ EDGERESTRICTED**。</span><span class="sxs-lookup"><span data-stu-id="24daf-162">o If Windows firewall is not enabled and no other edge-traversal aware host firewall is installed on the local system, the default will be **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span>

<span data-ttu-id="24daf-163">在 Windows Vista 和 Windows Server 2008 上，IPV6 \_ 保護層級的預設值 \_ 是不 **\_ \_ 受保護的保護層** 級。</span><span class="sxs-lookup"><span data-stu-id="24daf-163">On Windows Vista and Windows Server 2008, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span> <span data-ttu-id="24daf-164">但有效的值取決於是否已啟用 Windows 防火牆。</span><span class="sxs-lookup"><span data-stu-id="24daf-164">But the effective value depends on whether Windows firewall is enabled.</span></span> <span data-ttu-id="24daf-165">無論為 IPV6 保護層級設定的值為何，Windows 防火牆都可感知邊緣對 (Teredo 感知) \_ ， \_ 而且如果 ipv6 \_ 保護 \_ 層級不 **\_ \_ 受保護**，則會忽略。</span><span class="sxs-lookup"><span data-stu-id="24daf-165">The Windows firewall is edge-traversal aware (Teredo aware), no matter what value is set for the IPV6\_PROTECTION\_LEVEL and ignores if IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span> <span data-ttu-id="24daf-166">因此有效的值取決於防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="24daf-166">So the effective value depends on the firewall policy.</span></span> <span data-ttu-id="24daf-167">當停用 Windows 防火牆，且本機電腦上未安裝任何其他邊緣遍歷感知防火牆時，IPV6 \_ 保護層級的預設值 \_ 會是不 **\_ \_ 受限制的保護層級**。</span><span class="sxs-lookup"><span data-stu-id="24daf-167">When Windows firewall is disabled and no other edge-traversal aware firewall is installed on the local computer, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span>

<span data-ttu-id="24daf-168">在 Windows Server 2003 和 Windows XP 上，IPV6 \_ 保護層級的預設值 \_ 為 **保護 \_ 層級 \_ EDGERESTRICTED**。</span><span class="sxs-lookup"><span data-stu-id="24daf-168">On Windows Server 2003 and Windows XP, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span> <span data-ttu-id="24daf-169">除非您已將 IPV6 \_ 保護 \_ 等級通訊端選項設定為不 **\_ \_ 受限制的保護層級**，否則您不會收到任何 Teredo 流量。</span><span class="sxs-lookup"><span data-stu-id="24daf-169">Unless you have set the IPV6\_PROTECTION\_LEVEL socket option to **PROTECTION\_LEVEL\_UNRESTRICTED**, you would not receive any Teredo traffic.</span></span>

<span data-ttu-id="24daf-170">視 IPV6 \_ 保護 \_ 等級而定，需要來自網際網路的未經要求流量的應用程式可能無法接收未經要求的流量。</span><span class="sxs-lookup"><span data-stu-id="24daf-170">Depending on the IPV6\_PROTECTION\_LEVEL, an application that requires unsolicited traffic from the Internet may not be capable of receiving unsolicited traffic.</span></span> <span data-ttu-id="24daf-171">不過，透過 Windows Teredo 介面接收要求的流量並不需要這些需求。</span><span class="sxs-lookup"><span data-stu-id="24daf-171">However, these requirements are not necessary for receiving solicited traffic over the Windows Teredo interface.</span></span> <span data-ttu-id="24daf-172">如需與 Teredo 互動的詳細資訊，請參閱透過 [Teredo 接收請求的流量](../teredo/receiving-solicited-traffic-over-teredo.md)。</span><span class="sxs-lookup"><span data-stu-id="24daf-172">For more details on the interaction with Teredo, see [Receiving Solicited Traffic Over Teredo](../teredo/receiving-solicited-traffic-over-teredo.md).</span></span>

<span data-ttu-id="24daf-173">當連入封包或連線因為設定保護層級而遭到拒絕時，將會以不是任何應用程式在該通訊端上接聽的方式來處理拒絕。</span><span class="sxs-lookup"><span data-stu-id="24daf-173">When incoming packets or connections are refused due to the set protection level, rejection is handled as if no application was listening on that socket.</span></span>

> [!Note]
>
> <span data-ttu-id="24daf-174">IPV6 \_ 保護 \_ 等級通訊端選項不一定會在 ipv6 通訊端上放置存取限制，也不一定會使用 Windows Teredo 以外的某種方法來限制 NAT 的存取，或甚至是其他廠商使用其他的 Teredo 執行。</span><span class="sxs-lookup"><span data-stu-id="24daf-174">The IPV6\_PROTECTION\_LEVEL socket option does not necessarily place access restrictions on IPv6 sockets or restrict NAT traversal using some method other than Windows Teredo or even using another implementation of Teredo by another vendor.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="24daf-175">相關主題</span><span class="sxs-lookup"><span data-stu-id="24daf-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24daf-176">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="24daf-176">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="24daf-177">透過 Teredo 接收請求的流量</span><span class="sxs-lookup"><span data-stu-id="24daf-177">Receiving Solicited Traffic Over Teredo</span></span>](../teredo/receiving-solicited-traffic-over-teredo.md)
</dt> <dt>

[<span data-ttu-id="24daf-178">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="24daf-178">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 
