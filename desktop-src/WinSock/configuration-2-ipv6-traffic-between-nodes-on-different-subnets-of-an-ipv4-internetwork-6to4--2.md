---
description: 6to4 是一種方法，可透過現有的 IPv4 網際網路基礎結構連接 IPv6 主機或網站。
ms.assetid: 3ca8518d-42f0-428c-b94c-ff244d17b314
title: '設定2： IPv4 網路上不同子網的節點之間的 IPv6 流量 (6to4) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1abd5477005e6a1e71c13aaf19a734e9191097d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469061"
---
# <a name="configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4"></a><span data-ttu-id="8737a-103">設定2： IPv4 網路上不同子網的節點之間的 IPv6 流量 (6to4) </span><span class="sxs-lookup"><span data-stu-id="8737a-103">Configuration 2: IPv6 Traffic Between Nodes on Different Subnets of an IPv4 Internetwork (6to4)</span></span>

<span data-ttu-id="8737a-104">6to4 是一種方法，可透過現有的 IPv4 網際網路基礎結構連接 IPv6 主機或網站。</span><span class="sxs-lookup"><span data-stu-id="8737a-104">6to4 is a method for connecting IPv6 hosts or sites over the existing IPv4 Internet infrastructure.</span></span> <span data-ttu-id="8737a-105">它會使用唯一的位址前置詞，為隔離的 IPv6 網站提供自己的 IPv6 位址空間。</span><span class="sxs-lookup"><span data-stu-id="8737a-105">It uses a unique address prefix to give isolated IPv6 sites their own IPv6 address space.</span></span> <span data-ttu-id="8737a-106">6to4 就像是提供 IPv6 連線的「虛擬 ISP」。</span><span class="sxs-lookup"><span data-stu-id="8737a-106">6to4 is like a "pseudo-ISP" providing IPv6 connectivity.</span></span> <span data-ttu-id="8737a-107">您可以使用6to4 直接與其他6to4 網站進行通訊。</span><span class="sxs-lookup"><span data-stu-id="8737a-107">You can use 6to4 to communicate directly with other 6to4 sites.</span></span> <span data-ttu-id="8737a-108">6to4 不需要使用 IPv6 路由器，其 IPv6 流量會以 IPv4 標頭封裝。</span><span class="sxs-lookup"><span data-stu-id="8737a-108">6to4 does not require the use of IPv6 routers and its IPv6 traffic is encapsulated with an IPv4 header.</span></span>

<span data-ttu-id="8737a-109">下圖顯示使用6to4 在 IPv4 路由器之間進行通訊的不同子網上，兩個節點的設定。</span><span class="sxs-lookup"><span data-stu-id="8737a-109">The following illustration shows the configuration of two nodes on separate subnets using 6to4 to communicate across an IPv4 router.</span></span>

![使用6to4 在 ipv4 路由器之間通訊的節點。](images/v6mig-2.png)

<span data-ttu-id="8737a-111">使用6to4 的主要需求是您網站的一個可全域路由的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="8737a-111">The main requirement for using 6to4 is one globally routable IPv4 address for your site.</span></span> <span data-ttu-id="8737a-112">假設您的網站是由一組您管理的 IPv6 電腦所組成， (某些執行的 Microsoft IPv6 通訊協定，以及一些執行中的其他 IPv6 執行) 。</span><span class="sxs-lookup"><span data-stu-id="8737a-112">Suppose that your site consists of a collection of IPv6 computers that you manage (some running the Microsoft IPv6 protocol and some running other IPv6 implementations).</span></span> <span data-ttu-id="8737a-113">也假設所有 IPv6 電腦都是使用乙太網路或6到4來直接連接。</span><span class="sxs-lookup"><span data-stu-id="8737a-113">Assume also that all IPv6 computers are directly connected using Ethernet or 6-over-4.</span></span> <span data-ttu-id="8737a-114">您必須將可全域路由的 IPv4 位址指派給執行 Microsoft IPv6 通訊協定的其中一部電腦。</span><span class="sxs-lookup"><span data-stu-id="8737a-114">The globally routable IPv4 address must be assigned to one of your computers running the Microsoft IPv6 protocol.</span></span> <span data-ttu-id="8737a-115">這部電腦將是您的6to4 閘道。</span><span class="sxs-lookup"><span data-stu-id="8737a-115">This computer will be your 6to4 gateway.</span></span>

<span data-ttu-id="8737a-116">如果您的 IPv4 位址是私人位址空間的一部分 (10.0.0.0/8、172.16.0.0/12 或 192.168.0.0/16) 或自動私人 IP 位址 (APIPA) 位址空間（由 Windows 2000 使用），則無法全域路由傳送。</span><span class="sxs-lookup"><span data-stu-id="8737a-116">If you have an IPv4 address that is part of the private address space (10.0.0.0/8, 172.16.0.0/12, or 192.168.0.0/16) or the Automatic Private IP Addressing (APIPA) address space of 169.254.0.0/16 used by Windows 2000, it is not globally routable.</span></span> <span data-ttu-id="8737a-117">否則，它可能是公用 IP 位址，而且可全域路由傳送。</span><span class="sxs-lookup"><span data-stu-id="8737a-117">Otherwise, it is probably a public IP address and is globally routable.</span></span> <span data-ttu-id="8737a-118">See the [Debugging 6to4 Configuration](#debugging-6to4-configuration) topic in this document for more help in determining whether your ISP connection supports 6to4.</span><span class="sxs-lookup"><span data-stu-id="8737a-118">See the [Debugging 6to4 Configuration](#debugging-6to4-configuration) topic in this document for more help in determining whether your ISP connection supports 6to4.</span></span>

## <a name="the-6to4cfgexe-tool"></a><span data-ttu-id="8737a-119">6to4cfg.exe 工具</span><span class="sxs-lookup"><span data-stu-id="8737a-119">The 6to4cfg.exe Tool</span></span>

<span data-ttu-id="8737a-120">6to4cfg.exe 工具會將6to4 設定自動化，自動探索您全域可路由傳送的 IPv4 位址，以及建立6to4 首碼。</span><span class="sxs-lookup"><span data-stu-id="8737a-120">The 6to4cfg.exe tool automates 6to4 configuration, automatically discovering your globally routable IPv4 address and creating a 6to4 prefix.</span></span> <span data-ttu-id="8737a-121">它會直接執行設定，也可以撰寫您稍後可以檢查和執行的設定腳本。</span><span class="sxs-lookup"><span data-stu-id="8737a-121">It either performs the configuration directly, or it can write a configuration script that you can inspect and run later.</span></span>

<span data-ttu-id="8737a-122">基本 6to4cfg.exe 命令語法如下所示。</span><span class="sxs-lookup"><span data-stu-id="8737a-122">The basic 6to4cfg.exe command syntax is as follows.</span></span>

``` syntax
6to4cfg [-r] [-s] [-u] [-R relay] [-b] [-S address] [filename]
```

<dl> <dt>

<span data-ttu-id="8737a-123"><span id="_filename_"></span><span id="_FILENAME_"></span>\[*檔案名*\]</span><span class="sxs-lookup"><span data-stu-id="8737a-123"><span id="_filename_"></span><span id="_FILENAME_"></span>\[*filename*\]</span></span>
</dt> <dd>

<span data-ttu-id="8737a-124">如果您指定檔案名，則將設定腳本寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="8737a-124">Writes the configuration script to a file, if you specify a file name.</span></span> <span data-ttu-id="8737a-125">設定腳本會使用 Ipv6.exe。</span><span class="sxs-lookup"><span data-stu-id="8737a-125">The configuration script uses Ipv6.exe.</span></span>

<span data-ttu-id="8737a-126">您可以指定檔案名的 con 將設定腳本寫入主控台輸出，這對於查看測試案例中的 6to4cfg.exe 會有説明。</span><span class="sxs-lookup"><span data-stu-id="8737a-126">You can specify con for the file name to write the configuration script to console output, which is useful for seeing what 6to4cfg.exe will do in a test scenario.</span></span>

<span data-ttu-id="8737a-127">如果您沒有指定檔案名，6to4cfg.exe 直接更新您電腦上的 IPv6 設定。</span><span class="sxs-lookup"><span data-stu-id="8737a-127">If you do not specify a file name, 6to4cfg.exe directly updates the IPv6 configuration on your computer.</span></span>

</dd> <dt>

<span data-ttu-id="8737a-128"><span id="-r"></span><span id="-R"></span>-r</span><span class="sxs-lookup"><span data-stu-id="8737a-128"><span id="-r"></span><span id="-R"></span>-r</span></span>
</dt> <dd>

<span data-ttu-id="8737a-129">成為區域網路的6to4 閘道路由器，可在您的所有介面和指派的子網首碼上啟用路由。</span><span class="sxs-lookup"><span data-stu-id="8737a-129">Becomes a 6to4 gateway router for your local network, enabling routing on all of your interfaces and assigned subnet prefixes.</span></span>

</dd> <dt>

<span data-ttu-id="8737a-130"><span id="-s"></span><span id="-S"></span>-s</span><span class="sxs-lookup"><span data-stu-id="8737a-130"><span id="-s"></span><span id="-S"></span>-s</span></span>
</dt> <dd>

<span data-ttu-id="8737a-131">在您的6to4 網站中啟用網站本機定址。</span><span class="sxs-lookup"><span data-stu-id="8737a-131">Enables site-local addressing in your 6to4 site.</span></span> <span data-ttu-id="8737a-132">此命令只有在搭配-r 使用時才有用。</span><span class="sxs-lookup"><span data-stu-id="8737a-132">This command is only useful when used in conjunction with -r.</span></span>

</dd> <dt>

<span data-ttu-id="8737a-133"><span id="-u"></span><span id="-U"></span>-u</span><span class="sxs-lookup"><span data-stu-id="8737a-133"><span id="-u"></span><span id="-U"></span>-u</span></span>
</dt> <dd>

<span data-ttu-id="8737a-134">指定反轉6to4 設定。</span><span class="sxs-lookup"><span data-stu-id="8737a-134">Specifies that the 6to4 configuration be reversed.</span></span> <span data-ttu-id="8737a-135">因此，6to4cfg-u 會反轉6to4cfg 和6to4cfg 的效果-r-u 會反轉 6to4cfg-r 的效果，依此類推。</span><span class="sxs-lookup"><span data-stu-id="8737a-135">Therefore 6to4cfg -u reverses the effect of 6to4cfg and 6to4cfg -r -u reverses the effect of 6to4cfg -r, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="8737a-136"><span id="-R_relay"></span><span id="-r_relay"></span><span id="-R_RELAY"></span>-R *轉送*</span><span class="sxs-lookup"><span data-stu-id="8737a-136"><span id="-R_relay"></span><span id="-r_relay"></span><span id="-R_RELAY"></span>-R *relay*</span></span>
</dt> <dd>

<span data-ttu-id="8737a-137">指定6to4 轉送路由器的名稱或 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="8737a-137">Specifies the name or IPv4 address of a 6to4 relay router.</span></span> <span data-ttu-id="8737a-138">預設名稱是6to4.ipv6.microsoft.com，也就是網際網路上的6to4 轉送路由器。</span><span class="sxs-lookup"><span data-stu-id="8737a-138">The default name is 6to4.ipv6.microsoft.com, the 6to4 relay router on the Internet.</span></span>

</dd> <dt>

<span data-ttu-id="8737a-139"><span id="-b"></span><span id="-B"></span>-b</span><span class="sxs-lookup"><span data-stu-id="8737a-139"><span id="-b"></span><span id="-B"></span>-b</span></span>
</dt> <dd>

<span data-ttu-id="8737a-140">指定 6to4cfg.exe 挑選「最佳」轉送位址，而不是第一個位址。</span><span class="sxs-lookup"><span data-stu-id="8737a-140">Specifies that 6to4cfg.exe picks the "best" relay address instead of the first.</span></span>

</dd> <dt>

<span data-ttu-id="8737a-141"><span id="-S_address"></span><span id="-s_address"></span><span id="-S_ADDRESS"></span>-S *位址*</span><span class="sxs-lookup"><span data-stu-id="8737a-141"><span id="-S_address"></span><span id="-s_address"></span><span id="-S_ADDRESS"></span>-S *address*</span></span>
</dt> <dd>

<span data-ttu-id="8737a-142">指定6to4 首碼的本機 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="8737a-142">Specifies the local IPv4 address for the 6to4 prefix.</span></span>

</dd> </dl>

## <a name="manual-6to4-configuration"></a><span data-ttu-id="8737a-143">手動設定6to4</span><span class="sxs-lookup"><span data-stu-id="8737a-143">Manual 6to4 Configuration</span></span>

<span data-ttu-id="8737a-144">在此範例中，會 172.31.42.239 6to4 閘道的位址。</span><span class="sxs-lookup"><span data-stu-id="8737a-144">In this example the address of the 6to4 gateway is 172.31.42.239.</span></span> <span data-ttu-id="8737a-145">您需要您專屬可全域路由的 IPv4 位址，才能使用6to4。</span><span class="sxs-lookup"><span data-stu-id="8737a-145">You need your own globally routable IPv4 address to use 6to4.</span></span>

> [!Note]  
> <span data-ttu-id="8737a-146">IP 位址172.31.42.239 僅供範例之用。</span><span class="sxs-lookup"><span data-stu-id="8737a-146">The IP address 172.31.42.239 is used for example purposes only.</span></span> <span data-ttu-id="8737a-147">這是私人位址，無法在網際網路上以全球方式路由傳送。</span><span class="sxs-lookup"><span data-stu-id="8737a-147">This is a private address and is not globally routable on the Internet.</span></span>

 

<span data-ttu-id="8737a-148">32位可全域路由的 IPv4 位址會與16位首碼2002::/16 結合，以形成您網站的48位 IPv6 位址首碼。</span><span class="sxs-lookup"><span data-stu-id="8737a-148">The 32-bit globally routable IPv4 address is combined with the 16-bit prefix 2002::/16 to form a 48-bit IPv6 address prefix for your site.</span></span> <span data-ttu-id="8737a-149">在此範例中，6to4 網站首碼是2002： ac1f：2aef：：/48。</span><span class="sxs-lookup"><span data-stu-id="8737a-149">In this example, the 6to4 site prefix is 2002:ac1f:2aef::/48.</span></span> <span data-ttu-id="8737a-150">請注意，ac1f：2aef 是 172.31.42.239 (的十六進位編碼方式，您將使用不同的前置詞，並根據您專屬可全域路由的 IPv4 位址) 。</span><span class="sxs-lookup"><span data-stu-id="8737a-150">Note that ac1f:2aef is the hexadecimal encoding of 172.31.42.239 (of course, you will use a different prefix based on your own globally routable IPv4 address).</span></span> <span data-ttu-id="8737a-151">您可以使用6to4 網站首碼來指派網站內的位址和子網首碼。</span><span class="sxs-lookup"><span data-stu-id="8737a-151">Using the 6to4 site prefix, you can assign addresses and subnet prefixes inside your site.</span></span>

<span data-ttu-id="8737a-152">此範例假設您使用子網0手動設定6to4 閘道電腦上的6to4 位址，並使用子網1自動設定 Ethernet 網路區段上的位址。</span><span class="sxs-lookup"><span data-stu-id="8737a-152">This example assumes that you use subnet 0 for manually configuring a 6to4 address on your 6to4 gateway computer and that you use subnet 1 for automatically configuring addresses on your Ethernet network segment.</span></span> <span data-ttu-id="8737a-153">不過，也可以選擇其他選項。</span><span class="sxs-lookup"><span data-stu-id="8737a-153">However, other choices are possible.</span></span>

1.  <span data-ttu-id="8737a-154">使用 Ipv6.exe 在您的6to4 閘道電腦上啟用6to4：</span><span class="sxs-lookup"><span data-stu-id="8737a-154">Use Ipv6.exe to enable 6to4 on your 6to4 gateway computer:</span></span>

    <span data-ttu-id="8737a-155">**ipv6 rtu 2002::/16 2**</span><span class="sxs-lookup"><span data-stu-id="8737a-155">**ipv6 rtu 2002::/16 2**</span></span>

    <span data-ttu-id="8737a-156">**Ipv6 rtu** 命令會執行路由表更新。</span><span class="sxs-lookup"><span data-stu-id="8737a-156">The **ipv6 rtu** command performs a routing table update.</span></span> <span data-ttu-id="8737a-157">可以用來新增、移除或更新路由。</span><span class="sxs-lookup"><span data-stu-id="8737a-157">It can be used to add, remove, or update a route.</span></span> <span data-ttu-id="8737a-158">在此情況下，它會啟用6to4。</span><span class="sxs-lookup"><span data-stu-id="8737a-158">In this case it is enabling 6to4.</span></span>

    <span data-ttu-id="8737a-159">2002::/16 引數是路由的前置詞，指定唯一的6to4 前置詞。</span><span class="sxs-lookup"><span data-stu-id="8737a-159">The 2002::/16 argument is the prefix of the route, specifying the unique 6to4 prefix.</span></span>

    <span data-ttu-id="8737a-160">2個引數會指定這個前置詞的內部連結介面。</span><span class="sxs-lookup"><span data-stu-id="8737a-160">The 2 argument specifies the on-link interface for this prefix.</span></span> <span data-ttu-id="8737a-161">介面 \# 2 是用於設定通道、自動通道和6to4 的「虛擬介面」。</span><span class="sxs-lookup"><span data-stu-id="8737a-161">Interface \#2 is the "pseudo-interface" used for configured tunnels, automatic tunneling, and 6to4.</span></span> <span data-ttu-id="8737a-162">當 IPv6 目的地位址符合2002::/16 首碼時，會解壓縮目的地位址前置詞後面的32位以形成 IPv4 目的地位址。</span><span class="sxs-lookup"><span data-stu-id="8737a-162">When an IPv6 destination address matches the 2002::/16 prefix, the 32 bits that follow the prefix in the destination address are extracted to form an IPv4 destination address.</span></span> <span data-ttu-id="8737a-163">封包會以 IPv4 標頭封裝，並傳送至 IPv4 目的地位址。</span><span class="sxs-lookup"><span data-stu-id="8737a-163">The packet is encapsulated with an IPv4 header and sent to the IPv4 destination address.</span></span>

2.  <span data-ttu-id="8737a-164">在您的6to4 閘道電腦上設定6to4 位址：</span><span class="sxs-lookup"><span data-stu-id="8737a-164">Configure a 6to4 address on your 6to4 gateway computer:</span></span>

    <span data-ttu-id="8737a-165">**ipv6 adu 2/2002： ac1f：2aef：： ac1f：2aef**</span><span class="sxs-lookup"><span data-stu-id="8737a-165">**ipv6 adu 2/2002:ac1f:2aef::ac1f:2aef**</span></span>

    <span data-ttu-id="8737a-166">**Ipv6 adu** 命令會執行位址更新。</span><span class="sxs-lookup"><span data-stu-id="8737a-166">The **ipv6 adu** command performs an address update.</span></span> <span data-ttu-id="8737a-167">可以用來新增、移除或更新介面上的位址。</span><span class="sxs-lookup"><span data-stu-id="8737a-167">It can be used to add, remove, or update an address on an interface.</span></span> <span data-ttu-id="8737a-168">在此情況下，它會設定電腦的6to4 位址。</span><span class="sxs-lookup"><span data-stu-id="8737a-168">In this instance, it is configuring the computer's 6to4 address.</span></span>

    <span data-ttu-id="8737a-169">2/2002： ac1f：2aef：： ac1f：2aef 引數同時指定介面和位址。</span><span class="sxs-lookup"><span data-stu-id="8737a-169">The 2/2002:ac1f:2aef::ac1f:2aef argument specifies both the interface and the address.</span></span> <span data-ttu-id="8737a-170">它需要在介面2上設定 address 2002： ac1f：2aef：： ac1f： 2aef \# 。</span><span class="sxs-lookup"><span data-stu-id="8737a-170">It requires configuring address 2002:ac1f:2aef::ac1f:2aef on interface \#2.</span></span> <span data-ttu-id="8737a-171">位址會使用網站首碼2002： ac1f：2aef：：/48、子網0來提供子網首碼2002： ac1f：2aef：：/64 和64位介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="8737a-171">The address is created using the site prefix 2002:ac1f:2aef::/48, subnet 0 to give a subnet prefix 2002:ac1f:2aef::/64, and a 64-bit interface identifier.</span></span> <span data-ttu-id="8737a-172">此慣例針對指派給介面2的位址，使用電腦的 IPv4 位址作為介面識別碼 \# 。</span><span class="sxs-lookup"><span data-stu-id="8737a-172">The convention demonstrated uses the computer's IPv4 address for the interface identifier for addresses assigned to interface \#2.</span></span> <span data-ttu-id="8737a-173">針對您的使用，ac1f：2aef 應該由您專屬可全域路由的 IPv4 位址的十六進位編碼來取代。</span><span class="sxs-lookup"><span data-stu-id="8737a-173">For your use, ac1f:2aef should be replaced by the hexadecimal encoding of your own globally routable IPv4 address.</span></span>

<span data-ttu-id="8737a-174">上述兩個命令足以允許與其他6to4 網站進行通訊。</span><span class="sxs-lookup"><span data-stu-id="8737a-174">The two preceding commands are sufficient to allow communication with other 6to4 sites.</span></span> <span data-ttu-id="8737a-175">例如，您可以嘗試 ping Microsoft 6to4 網站：</span><span class="sxs-lookup"><span data-stu-id="8737a-175">For example, you can try pinging the Microsoft 6to4 site:</span></span>

<span data-ttu-id="8737a-176">**ping6 2002：836b：9820：：836b：9820**</span><span class="sxs-lookup"><span data-stu-id="8737a-176">**ping6 2002:836b:9820::836b:9820**</span></span>

<span data-ttu-id="8737a-177">若要啟用與6bone 的通訊，您必須建立通往6to4 轉送的預設設定通道。</span><span class="sxs-lookup"><span data-stu-id="8737a-177">To enable communication with the 6bone, you must create a default configured tunnel to a 6to4 relay.</span></span> <span data-ttu-id="8737a-178">您可以使用 Microsoft 6to4 轉送路由器131.107.152.32：</span><span class="sxs-lookup"><span data-stu-id="8737a-178">You can use the Microsoft 6to4 relay router, 131.107.152.32:</span></span>

<span data-ttu-id="8737a-179">**ipv6 rtu：：/0 2/：： 131.107.152.32 pub life 1800**</span><span class="sxs-lookup"><span data-stu-id="8737a-179">**ipv6 rtu ::/0 2/::131.107.152.32 pub life 1800**</span></span>

<span data-ttu-id="8737a-180">**Ipv6 rtu** 命令會執行路由表更新，在此實例中建立通往6to4 轉送的預設路由。</span><span class="sxs-lookup"><span data-stu-id="8737a-180">The **ipv6 rtu** command performs a routing table update, establishing, in this instance, a default route to the 6to4 relay.</span></span>

<span data-ttu-id="8737a-181">：：/0 引數是路由前置詞。</span><span class="sxs-lookup"><span data-stu-id="8737a-181">The ::/0 argument is the route prefix.</span></span> <span data-ttu-id="8737a-182">長度為零的前置詞表示它是預設路由。</span><span class="sxs-lookup"><span data-stu-id="8737a-182">The zero-length prefix indicates that it is a default route.</span></span>

<span data-ttu-id="8737a-183">2/：：131.107.152.32 引數會指定這個前置詞的下一個躍點相鄰。</span><span class="sxs-lookup"><span data-stu-id="8737a-183">The 2/::131.107.152.32 argument specifies the next-hop neighbor for this prefix.</span></span> <span data-ttu-id="8737a-184">它需要使用介面2將符合前置詞的封包轉送至位址：： 131.107.152.32 \# 。</span><span class="sxs-lookup"><span data-stu-id="8737a-184">It requires that packets matching the prefix are forwarded to address ::131.107.152.32 using interface \#2.</span></span> <span data-ttu-id="8737a-185">在介面2上將封包轉送至：： 131.107.152.32 \# 會導致它以 v4 標頭封裝並傳送至131.107.152.32。</span><span class="sxs-lookup"><span data-stu-id="8737a-185">Forwarding a packet to ::131.107.152.32 on interface \#2 causes it to be encapsulated with a v4 header and sent to 131.107.152.32.</span></span>

<span data-ttu-id="8737a-186">Pub 引數使其成為已發佈的路由。</span><span class="sxs-lookup"><span data-stu-id="8737a-186">The pub argument makes this a published route.</span></span> <span data-ttu-id="8737a-187">因為這只與路由器有關，所以在啟用路由之前，它沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="8737a-187">Because this is only relevant for routers, it has no effect until routing is enabled.</span></span> <span data-ttu-id="8737a-188">同樣地，30分鐘的存留期僅適用于啟用路由。</span><span class="sxs-lookup"><span data-stu-id="8737a-188">Similarly, the 30-minute lifetime pertains only if routing is enabled.</span></span>

<span data-ttu-id="8737a-189">您應該能夠存取6bone 網站和6to4 網站。</span><span class="sxs-lookup"><span data-stu-id="8737a-189">You should be able to access 6bone sites as well as 6to4 sites.</span></span> <span data-ttu-id="8737a-190">您可以使用下列命令來測試此項：</span><span class="sxs-lookup"><span data-stu-id="8737a-190">You can use the following command to test this:</span></span>

<span data-ttu-id="8737a-191">**ping6 3ffe：1cff：0： f5：：1**</span><span class="sxs-lookup"><span data-stu-id="8737a-191">**ping6 3ffe:1cff:0:f5::1**</span></span>

<span data-ttu-id="8737a-192">最後一個步驟是在您的6to4 閘道上啟用路由。</span><span class="sxs-lookup"><span data-stu-id="8737a-192">The final step is to enable routing on your 6to4 gateway.</span></span> <span data-ttu-id="8737a-193">此範例假設 \# 您閘道電腦上的介面3是乙太網路介面，而介面 \# 4 是6到4。</span><span class="sxs-lookup"><span data-stu-id="8737a-193">This example assumes that interface \#3 on your gateway computer is an Ethernet interface and interface \#4 is 6-over-4.</span></span> <span data-ttu-id="8737a-194">您的電腦可能會以不同的方式來為其介面編號。</span><span class="sxs-lookup"><span data-stu-id="8737a-194">Your computer might number its interfaces differently.</span></span> <span data-ttu-id="8737a-195">下列兩個命令會將子網首碼指派給這兩個連結。</span><span class="sxs-lookup"><span data-stu-id="8737a-195">The following two commands assign subnet prefixes to the two links.</span></span> <span data-ttu-id="8737a-196">子網首碼衍生自網站的6to4 首碼2002： ac1f：2aef：：/48：</span><span class="sxs-lookup"><span data-stu-id="8737a-196">The subnet prefixes are derived from the site's 6to4 prefix 2002:ac1f:2aef::/48:</span></span>

<span data-ttu-id="8737a-197">**ipv6 rtu 2002： ac1f：2aef：1：：/64 3 pub life 1800**</span><span class="sxs-lookup"><span data-stu-id="8737a-197">**ipv6 rtu 2002:ac1f:2aef:1::/64 3 pub life 1800**</span></span>

<span data-ttu-id="8737a-198">**ipv6 rtu 2002： ac1f：2aef：2：：/64 4 pub life 1800**</span><span class="sxs-lookup"><span data-stu-id="8737a-198">**ipv6 rtu 2002:ac1f:2aef:2::/64 4 pub life 1800**</span></span>

<span data-ttu-id="8737a-199">**Ipv6 rtu** 命令指定首碼2002： ac1f：2aef：1：：/64 是在介面3的連結上 \# 。</span><span class="sxs-lookup"><span data-stu-id="8737a-199">The **ipv6 rtu** command specifies that the prefix 2002:ac1f:2aef:1::/64 is on-link to interface \#3.</span></span> <span data-ttu-id="8737a-200">它會設定 Ethernet 介面上的第一個子網前置詞。</span><span class="sxs-lookup"><span data-stu-id="8737a-200">It is configuring the first subnet prefix on the Ethernet interface.</span></span> <span data-ttu-id="8737a-201">此路由會在存留期30分鐘內發佈。</span><span class="sxs-lookup"><span data-stu-id="8737a-201">The route is published with a lifetime of 30 minutes.</span></span>

<span data-ttu-id="8737a-202">同樣地，2002： ac1f：2aef：2：：/64 首碼是在6個以上的介面上進行設定。</span><span class="sxs-lookup"><span data-stu-id="8737a-202">Similarly, the 2002:ac1f:2aef:2::/64 prefix is configured on the 6-over-4 interface.</span></span>

<span data-ttu-id="8737a-203">接下來的三個命令可讓6to4 閘道電腦以路由器的形式運作：</span><span class="sxs-lookup"><span data-stu-id="8737a-203">The next three commands enable the 6to4 gateway computer to function as a router:</span></span>

<span data-ttu-id="8737a-204">**ipv6 ifc 2 forw**</span><span class="sxs-lookup"><span data-stu-id="8737a-204">**ipv6 ifc 2 forw**</span></span>

<span data-ttu-id="8737a-205">**ipv6 ifc 3 forw 進階**</span><span class="sxs-lookup"><span data-stu-id="8737a-205">**ipv6 ifc 3 forw adv**</span></span>

<span data-ttu-id="8737a-206">**ipv6 ifc 4 forw 進階**</span><span class="sxs-lookup"><span data-stu-id="8737a-206">**ipv6 ifc 4 forw adv**</span></span>

<span data-ttu-id="8737a-207">**Ipv6 ifc** 命令可控制介面的屬性。</span><span class="sxs-lookup"><span data-stu-id="8737a-207">The **ipv6 ifc** command controls attributes of an interface.</span></span> <span data-ttu-id="8737a-208">路由器會轉送封包並傳送路由器通告。</span><span class="sxs-lookup"><span data-stu-id="8737a-208">A router forwards packets and sends router advertisements.</span></span> <span data-ttu-id="8737a-209">在 Microsoft IPv6 的執行中，這些每個介面屬性會分開控制。</span><span class="sxs-lookup"><span data-stu-id="8737a-209">In the Microsoft IPv6 implementation, these per-interface attributes are controlled separately.</span></span>

<span data-ttu-id="8737a-210">\#不需要介面2來進行廣告，因為它是虛擬介面。</span><span class="sxs-lookup"><span data-stu-id="8737a-210">Interface \#2 is not needed for advertising because it is a pseudo-interface.</span></span>

<span data-ttu-id="8737a-211">如果您的電腦有其他介面，也應該將它們設定為轉送和廣告。</span><span class="sxs-lookup"><span data-stu-id="8737a-211">If your computer has additional interfaces, they should also be configured to be forwarding and advertising.</span></span>

<span data-ttu-id="8737a-212">執行這些命令之後，Microsoft IPv6 通訊協定會 \# 使用各自的子網首碼在介面3和4上自動設定位址， \# 而這兩個介面會開始傳送路由器公告大約3到10分鐘。</span><span class="sxs-lookup"><span data-stu-id="8737a-212">After running these commands, the Microsoft IPv6 protocol will automatically configure addresses on interfaces \#3 and \#4 using the respective subnet prefixes and the two interfaces will start sending router advertisements at approximately 3 to 10 minute intervals.</span></span>

<span data-ttu-id="8737a-213">接收這些路由器公告的主機會自動設定預設路由，以及衍生自其連結子網首碼的6to4 位址。</span><span class="sxs-lookup"><span data-stu-id="8737a-213">Hosts receiving these router advertisements will automatically configure themselves with a default route and a 6to4 address derived from the subnet prefix of their link.</span></span> <span data-ttu-id="8737a-214">他們會透過閘道電腦與其他6to4 網站和6bone 進行通訊。</span><span class="sxs-lookup"><span data-stu-id="8737a-214">They will have communication to other 6to4 sites and the 6bone through the gateway computer.</span></span>

## <a name="debugging-6to4-configuration"></a><span data-ttu-id="8737a-215">進行6to4 設定的調試</span><span class="sxs-lookup"><span data-stu-id="8737a-215">Debugging 6to4 Configuration</span></span>

<span data-ttu-id="8737a-216">**若要偵測您的6to4 設定**</span><span class="sxs-lookup"><span data-stu-id="8737a-216">**To debug your 6to4 configuration**</span></span>

1.  <span data-ttu-id="8737a-217">檢查 IPv4 與6to4 轉送路由器之間的連線能力：</span><span class="sxs-lookup"><span data-stu-id="8737a-217">Check your IPv4 connectivity to the 6to4 relay router:</span></span>

    <span data-ttu-id="8737a-218">**ping 6to4.ipv6.microsoft.com**</span><span class="sxs-lookup"><span data-stu-id="8737a-218">**ping 6to4.ipv6.microsoft.com**</span></span>

    <span data-ttu-id="8737a-219">如果失敗，您就不會有全球網際網路連線能力。</span><span class="sxs-lookup"><span data-stu-id="8737a-219">If this fails, then you do not have global Internet connectivity.</span></span>

2.  <span data-ttu-id="8737a-220">使用自動通道檢查 IPv6 封裝：</span><span class="sxs-lookup"><span data-stu-id="8737a-220">Check IPv6 encapsulation by using automatic tunneling:</span></span>

    <span data-ttu-id="8737a-221">**ping6：：131.107.152.32**</span><span class="sxs-lookup"><span data-stu-id="8737a-221">**ping6 ::131.107.152.32**</span></span>

    <span data-ttu-id="8737a-222">如果失敗，則您的電腦與網際網路之間可能會有防火牆或網路位址轉譯器 (NAT) 。</span><span class="sxs-lookup"><span data-stu-id="8737a-222">If this fails, then you might have a firewall or network address translator (NAT) between your computer and the Internet.</span></span> <span data-ttu-id="8737a-223">如果成功，則您的網際網路連接可以支援6to4。</span><span class="sxs-lookup"><span data-stu-id="8737a-223">If this is successful, then your Internet connection can support 6to4.</span></span>

3.  <span data-ttu-id="8737a-224">檢查 ipv6 rt 命令的顯示。</span><span class="sxs-lookup"><span data-stu-id="8737a-224">Check the display of the ipv6 rt command.</span></span> <span data-ttu-id="8737a-225">您應該會看到 2002::/16-> 2 路由。</span><span class="sxs-lookup"><span data-stu-id="8737a-225">You should see a 2002::/16 -> 2 route.</span></span> <span data-ttu-id="8737a-226">檢查 ipv6 的顯示是否為2個命令。</span><span class="sxs-lookup"><span data-stu-id="8737a-226">Check the display of the ipv6 if 2 command.</span></span> <span data-ttu-id="8737a-227">您應該會看到含有2002::/16 前置詞的慣用位址。</span><span class="sxs-lookup"><span data-stu-id="8737a-227">You should see a preferred address with a 2002::/16 prefix.</span></span>

> [!Note]  
> <span data-ttu-id="8737a-228">131.107.152.32 的 Microsoft 6to4 轉送路由器的 IPv4 位址可能會變更。</span><span class="sxs-lookup"><span data-stu-id="8737a-228">The IPv4 address of the Microsoft 6to4 relay router of 131.107.152.32 is subject to change.</span></span> <span data-ttu-id="8737a-229">如果上述步驟2無法運作，請在步驟1中檢查 ping 命令的輸出，以確認 Microsoft 6to4 轉送路由器的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="8737a-229">If Step 2 above does not work, check the output of the ping command in step 1 to verify the IPv4 address of the Microsoft 6to4 relay router.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8737a-230">相關主題</span><span class="sxs-lookup"><span data-stu-id="8737a-230">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8737a-231">IPv6 的建議設定</span><span class="sxs-lookup"><span data-stu-id="8737a-231">Recommended Configurations for IPv6</span></span>](recommended-configurations-2.md)
</dt> <dt>

[<span data-ttu-id="8737a-232">具有連結-本機位址的單一子網</span><span class="sxs-lookup"><span data-stu-id="8737a-232">Single subnet with link-local addresses</span></span>](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="8737a-233">在兩個本機連結主機之間使用 IPsec</span><span class="sxs-lookup"><span data-stu-id="8737a-233">Using IPsec between two local link hosts</span></span>](configuration-4-using-ipsec-between-two-local-link-hosts-2.md)
</dt> </dl>

 

 



