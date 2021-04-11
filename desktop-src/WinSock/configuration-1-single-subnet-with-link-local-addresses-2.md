---
description: 第一個設定不需要額外的設定，除了安裝 Microsoft IPv6 技術預覽通訊協定之外。
ms.assetid: ceed4983-e088-44e8-9cfc-26afb3c35ba0
title: 設定1：具有連結-本機位址的單一子網
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d09feb44c222b7213da18a6745fc632f3903209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026222"
---
# <a name="configuration-1-single-subnet-with-link-local-addresses"></a><span data-ttu-id="fa723-103">設定1：具有連結-本機位址的單一子網</span><span class="sxs-lookup"><span data-stu-id="fa723-103">Configuration 1: Single Subnet with Link-local Addresses</span></span>

<span data-ttu-id="fa723-104">第一個設定不需要額外的設定，除了安裝 Microsoft IPv6 技術預覽通訊協定之外。</span><span class="sxs-lookup"><span data-stu-id="fa723-104">The first configuration requires no additional configuration beyond installing the Microsoft IPv6 Technology Preview protocol.</span></span> <span data-ttu-id="fa723-105">這項設定是由相同的子網上至少包含兩個節點所組成。</span><span class="sxs-lookup"><span data-stu-id="fa723-105">This configuration consists of at least two nodes on the same subnet.</span></span> <span data-ttu-id="fa723-106">在 IPv6 術語中，這兩個節點位於沒有中繼路由器的相同連結上。</span><span class="sxs-lookup"><span data-stu-id="fa723-106">In IPv6 terminology, the two nodes are on the same link with no intermediate routers.</span></span>

<span data-ttu-id="fa723-107">下圖顯示使用連結-本機位址在單一子網上設定兩個節點的設定。</span><span class="sxs-lookup"><span data-stu-id="fa723-107">The following illustration shows the configuration of two nodes on a single subnet using link-local addresses.</span></span>

![使用連結-本機位址的兩個節點。](images/v6mig-1.png)

<span data-ttu-id="fa723-109">根據預設，IPv6 會為每個對應到已安裝 Ethernet 網路介面卡的介面設定連結-本機 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="fa723-109">By default, IPv6 configures link-local IP addresses for each interface corresponding to installed Ethernet network adapters.</span></span> <span data-ttu-id="fa723-110">連結-本機位址的前置詞為 fe80：：/64。</span><span class="sxs-lookup"><span data-stu-id="fa723-110">Link-local addresses have the prefix fe80::/64.</span></span> <span data-ttu-id="fa723-111">IPv6 位址的最後64位稱為介面識別碼，並衍生自網路介面卡的48位 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="fa723-111">The last 64 bits of the IPv6 address is known as the interface identifier and is derived from the 48-bit MAC address of the network adapter.</span></span>

<span data-ttu-id="fa723-112">若要從48位 (6 位元組) 乙太網路 MAC 位址建立 IPv6 介面識別碼：</span><span class="sxs-lookup"><span data-stu-id="fa723-112">To create the IPv6 interface identifier from the 48-bit (6-byte) Ethernet MAC address:</span></span>

-   <span data-ttu-id="fa723-113">在 MAC 位址的第三個和第四個位元組之間插入十六進位數位 0xff-fe。</span><span class="sxs-lookup"><span data-stu-id="fa723-113">The hex digits 0xff-fe are inserted between the third and fourth byte of the MAC address.</span></span>
-   <span data-ttu-id="fa723-114">全域/本地位（MAC 位址的第一個位元組的第二個低序位位）會進行求一。</span><span class="sxs-lookup"><span data-stu-id="fa723-114">The Universal/Local bit, the second low-order bit of the first byte of the MAC address, is complemented.</span></span> <span data-ttu-id="fa723-115">如果是1，則會變成0，如果是0，則會變成1。</span><span class="sxs-lookup"><span data-stu-id="fa723-115">If it is a 1, it is turned to 0, and if it is a 0, it is turned to 1.</span></span>

<span data-ttu-id="fa723-116">例如，針對 MAC 位址 00-60-08-52-f9-d8：</span><span class="sxs-lookup"><span data-stu-id="fa723-116">For example, for the MAC address 00-60-08-52-f9-d8:</span></span>

-   <span data-ttu-id="fa723-117">在 0x08 (第三個位元組) 和 0x52 (MAC 位址的第四個位元組) （形成64位位址 00-60-08-ff-fe-52-f9-d8）之間，會插入十六進位數位 0xff-fe。</span><span class="sxs-lookup"><span data-stu-id="fa723-117">The hex digits 0xff-fe are inserted between 0x08 (the third byte) and 0x52 (the fourth byte) of the MAC address, forming the 64-bit address 00-60-08-ff-fe-52-f9-d8.</span></span>
-   <span data-ttu-id="fa723-118">在 MAC 位址的第一個位元組)  (的通用/本地位，0x00 的第二個低序位位。</span><span class="sxs-lookup"><span data-stu-id="fa723-118">The Universal/Local bit, the second low-order bit of 0x00 (the first byte) of the MAC address is complemented.</span></span> <span data-ttu-id="fa723-119">第二個低序位位為0x00 的是0，而在求時，會變成1。</span><span class="sxs-lookup"><span data-stu-id="fa723-119">The second low-order bit of 0x00 is 0 which, when complemented, becomes 1.</span></span> <span data-ttu-id="fa723-120">結果是，如果第一個位元組，0x00 會成為0x02。</span><span class="sxs-lookup"><span data-stu-id="fa723-120">The result is that for the first byte, 0x00 becomes 0x02.</span></span>

<span data-ttu-id="fa723-121">因此，對應至 Ethernet MAC 位址 00-60-08-52-f9-d8 的 IPv6 介面識別碼是 02-60-08-ff-fe-52-f9-d8。</span><span class="sxs-lookup"><span data-stu-id="fa723-121">Therefore, the IPv6 interface identifier corresponding to the Ethernet MAC address of 00-60-08-52-f9-d8 is 02-60-08-ff-fe-52-f9-d8.</span></span>

<span data-ttu-id="fa723-122">節點的連結-本機位址是首碼 fe80：：/64 以及以 IPv6 冒號-十六進位標記法表示的64位介面識別碼的組合。</span><span class="sxs-lookup"><span data-stu-id="fa723-122">The link-local address of a node is the combination of the prefix fe80::/64 and the 64-bit interface identifier expressed in IPv6 colon-hexadecimal notation.</span></span> <span data-ttu-id="fa723-123">因此，此範例節點的連結-本機位址的前置詞 fe80：：/64 和介面識別碼 02-60-08-ff-fe-52-f9-d8 是 fe80：：260：8ff： fe52： f9d8。</span><span class="sxs-lookup"><span data-stu-id="fa723-123">Therefore, the link-local address of this example node with the prefix fe80::/64 and the interface identifier 02-60-08-ff-fe-52-f9-d8 is fe80::260:8ff:fe52:f9d8.</span></span>

<span data-ttu-id="fa723-124">如下列範例所示，您可以使用 ipv6 來查看連結本機位址：</span><span class="sxs-lookup"><span data-stu-id="fa723-124">You can view your link local address by using ipv6 if, as demonstrated in the following example:</span></span>

<span data-ttu-id="fa723-125">**ipv6 if**</span><span class="sxs-lookup"><span data-stu-id="fa723-125">**ipv6 if**</span></span>

``` syntax
Interface 4 (site 1): Local Area Connection
  uses Neighbor Discovery
  link-level address: 00-10-5a-aa-20-a2
    preferred address fe80::210:5aff:feaa:20a2, infinite/infinite
    multicast address ff02::1, 1 refs, not reportable
    multicast address ff02::1:ffaa:20a2, 1 refs, last reporter
  link MTU 1500 (true link MTU 1500)
  current hop limit 128
  reachable time 43500ms (base 30000ms)
  retransmission interval 1000ms
  DAD transmits 1
Interface 3 (site 1): 6-over-4 Virtual Interface
  uses Neighbor Discovery
  link-level address: 10.0.0.2
    preferred address fe80::a00:2, infinite/infinite
    multicast address ff02::1, 1 refs, not reportable
    multicast address ff02::1:ff00:2, 1 refs, last reporter
  link MTU 1280 (true link MTU 65515)
  current hop limit 128
  reachable time 34000ms (base 30000ms)
  retransmission interval 1000ms
  DAD transmits 1
Interface 2 (site 0): Tunnel Pseudo-Interface
  does not use Neighbor Discovery
  link-level address: 0.0.0.0
    preferred address ::10.0.0.2, infinite/infinite
  link MTU 1280 (true link MTU 65515)
  current hop limit 128
  reachable time 0ms (base 0ms)
  retransmission interval 0ms
  DAD transmits 0
Interface 1 (site 0): Loopback Pseudo-Interface
  does not use Neighbor Discovery
  link-level address:
    preferred address ::1, infinite/infinite
  link MTU 1500 (true link MTU 1500)
  current hop limit 1
  reachable time 0ms (base 0ms)
  retransmission interval 0ms
  DAD transmits 0
```

<span data-ttu-id="fa723-126">介面4是對應至已安裝乙太網路介面卡的介面，其連結-本機位址為 fe80：：210：5aff： feaa：20a2。</span><span class="sxs-lookup"><span data-stu-id="fa723-126">Interface 4 is an interface corresponding to an installed Ethernet adapter with a link-local address of fe80::210:5aff:feaa:20a2.</span></span>

<span data-ttu-id="fa723-127">如需 IPv6 位址的詳細資訊和 IPv6 概念的總覽，請參閱 IPv6 簡介白皮書。</span><span class="sxs-lookup"><span data-stu-id="fa723-127">For more information on IPv6 addressing and an overview of IPv6 concepts, see the Introduction to IPv6 white paper.</span></span>

## <a name="testing-connectivity-between-two-link-local-hosts"></a><span data-ttu-id="fa723-128">測試兩個連結本機主機之間的連線能力</span><span class="sxs-lookup"><span data-stu-id="fa723-128">Testing Connectivity Between Two Link-local Hosts</span></span>

<span data-ttu-id="fa723-129">您可以執行簡單的 ping (在兩個連結本機主機之間使用 IPv6) ICMPv6 Echo 要求和回應回復訊息的交換。</span><span class="sxs-lookup"><span data-stu-id="fa723-129">You can do a simple ping (an exchange of ICMPv6 Echo Request and Echo Reply messages) using IPv6 between two link-local hosts.</span></span>

<span data-ttu-id="fa723-130">**使用 IPv6 在兩個連結本機主機之間進行 ping**</span><span class="sxs-lookup"><span data-stu-id="fa723-130">**To ping using IPv6 between two link-local hosts**</span></span>

1.  <span data-ttu-id="fa723-131">在兩部 Windows 主機上安裝適用于 Windows 的 Microsoft IPv6 技術預覽 (主機 A 和主機 B) 位於相同連結 (子網) 。</span><span class="sxs-lookup"><span data-stu-id="fa723-131">Install the Microsoft IPv6 Technology Preview for Windows on two Windows hosts (Host A and Host B) that are on the same link (subnet).</span></span>
2.  <span data-ttu-id="fa723-132">在主機 A 上使用 ipv6，以取得乙太網路介面的連結-本機位址。</span><span class="sxs-lookup"><span data-stu-id="fa723-132">Use ipv6 if on Host A to obtain the link-local address for the Ethernet interface.</span></span>

    <span data-ttu-id="fa723-133">範例：主機 A 的連結-本機位址是 fe80：：210：5aff： feaa：20a2。</span><span class="sxs-lookup"><span data-stu-id="fa723-133">Example: The link-local address of Host A is fe80::210:5aff:feaa:20a2.</span></span>

3.  <span data-ttu-id="fa723-134">在主機 B 上使用 ipv6 來取得乙太網路介面的連結-本機位址。</span><span class="sxs-lookup"><span data-stu-id="fa723-134">Use ipv6 if on Host B to obtain the link-local address for the Ethernet interface.</span></span>

    <span data-ttu-id="fa723-135">範例：主機 B 的連結-本機位址是 fe80：：260：97ff： fe02：6ea5。</span><span class="sxs-lookup"><span data-stu-id="fa723-135">Example: The link-local address of Host B is fe80::260:97ff:fe02:6ea5.</span></span>

4.  <span data-ttu-id="fa723-136">從主機 A，使用 Ping6.exe ping 主機 B。</span><span class="sxs-lookup"><span data-stu-id="fa723-136">From Host A, ping Host B using Ping6.exe.</span></span>

    <span data-ttu-id="fa723-137">範例： ping6 fe80：：260：97ff： fe02：6ea5</span><span class="sxs-lookup"><span data-stu-id="fa723-137">Example: ping6 fe80::260:97ff:fe02:6ea5</span></span>

<span data-ttu-id="fa723-138">若要指定傳送 Echo 要求訊息的來源位址，您也可以使用 Ping6.exe s 選項。</span><span class="sxs-lookup"><span data-stu-id="fa723-138">To specify the source address from which the Echo Request messages are sent, you can also use the Ping6.exe -s option.</span></span> <span data-ttu-id="fa723-139">例如，若要從 fe80：：210：5aff： feaa：20a2 的 IPv6 位址傳送 Echo 要求至主機 B，請使用下列命令：</span><span class="sxs-lookup"><span data-stu-id="fa723-139">For example, to send Echo Requests to Host B from the IPv6 address of fe80::210:5aff:feaa:20a2, use the following command:</span></span>

<span data-ttu-id="fa723-140">**fe80：：210：5aff： feaa： 20a2% 4 fe80：：260：97ff： fe02：6ea5**</span><span class="sxs-lookup"><span data-stu-id="fa723-140">**ping6 -s fe80::210:5aff:feaa:20a2%4 fe80::260:97ff:fe02:6ea5**</span></span>

<span data-ttu-id="fa723-141">在 ping 連結本機或網站本機位址時，建議您指定範圍識別碼以明確地讓目的位址。</span><span class="sxs-lookup"><span data-stu-id="fa723-141">When pinging a link-local or site-local address, it is recommended to specify the scope-ID to make the destination address unambiguous.</span></span> <span data-ttu-id="fa723-142">指定範圍識別碼的標記法是位址% 範圍識別碼。</span><span class="sxs-lookup"><span data-stu-id="fa723-142">The notation to specify the scope-ID is address%scope-ID.</span></span> <span data-ttu-id="fa723-143">若為連結-本機位址，範圍識別碼會等於 ipv6 if 命令中顯示的介面編號。</span><span class="sxs-lookup"><span data-stu-id="fa723-143">For link-local addresses, the scope-ID is equal to the interface number as displayed in the ipv6 if command.</span></span> <span data-ttu-id="fa723-144">若為網站本機位址，範圍識別碼會等於 ipv6 if 命令中顯示的網站號碼。</span><span class="sxs-lookup"><span data-stu-id="fa723-144">For site-local addresses, the scope-ID is equal to the site number as displayed in the ipv6 if command.</span></span> <span data-ttu-id="fa723-145">例如，若要使用範圍識別碼4將 Echo 要求訊息傳送至主機 B，請使用下列命令：</span><span class="sxs-lookup"><span data-stu-id="fa723-145">For example, to send Echo Request messages to Host B using scope-ID 4, use the following command:</span></span>

<span data-ttu-id="fa723-146">**ping6 fe80：：260：97ff： fe02： 6ea5% 4**</span><span class="sxs-lookup"><span data-stu-id="fa723-146">**ping6 fe80::260:97ff:fe02:6ea5%4**</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa723-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="fa723-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa723-148">IPv6 的建議設定</span><span class="sxs-lookup"><span data-stu-id="fa723-148">Recommended Configurations for IPv6</span></span>](recommended-configurations-2.md)
</dt> </dl>

 

 



