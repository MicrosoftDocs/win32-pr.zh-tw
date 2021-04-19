---
description: IPv6 連結-本機和網站-本機位址稱為範圍位址。
ms.assetid: d31882f6-b747-47c7-83cb-a9a03fe11cb8
title: IPv6 連結-本機和網站-本機位址
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb80b8e201adf382b10dd31fe5607de903d6c588
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972033"
---
# <a name="ipv6-link-local-and-site-local-addresses"></a><span data-ttu-id="f6cf6-103">IPv6 連結-本機和網站-本機位址</span><span class="sxs-lookup"><span data-stu-id="f6cf6-103">IPv6 Link-local and Site-local Addresses</span></span>

<span data-ttu-id="f6cf6-104">IPv6 連結-本機和網站-本機位址稱為範圍位址。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-104">IPv6 link-local and site-local addresses are called scoped addresses.</span></span> <span data-ttu-id="f6cf6-105">Windows 通訊端 (Winsock) API 支援 [**sockaddr \_ in6**](sockaddr-2.md)結構中的 **sin6 \_ 範圍 \_ 識別碼** 成員，以搭配範圍位址使用。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-105">The Windows Sockets (Winsock) API supports the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure for use with scoped addresses.</span></span> <span data-ttu-id="f6cf6-106">針對 IPv6 連結-本機位址 (fe80：：/10 首碼) ， **sockaddr \_ in6** 結構中的 **sin6 \_ 範圍 \_ 識別碼** 成員是介面編號。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-106">For IPv6 link-local addresses (fe80::/10 prefix), the **sin6\_scope\_id** member in the **sockaddr\_in6** structure is the interface number.</span></span> <span data-ttu-id="f6cf6-107">針對 IPv6 網站-本機位址 (fec0：：/10 首碼) ， **sockaddr \_ in6** 結構中的 **sin6 \_ 範圍 \_ 識別碼** 成員是網站識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-107">For IPv6 site-local addresses (fec0::/10 prefix), the **sin6\_scope\_id** member in the **sockaddr\_in6** structure is a site identifier.</span></span>

<span data-ttu-id="f6cf6-108">介面5上的連結-本機 IPv6 位址範例 \# 如下：</span><span class="sxs-lookup"><span data-stu-id="f6cf6-108">An example of a link-local IPv6 address on interface \#5 is the following:</span></span>

``` syntax
fe80::208:74ff:feda:625c%5
```

<span data-ttu-id="f6cf6-109">下列命令適用于 Windows XP Service Pack 1 (SP1) 和更新版本，可在本機電腦上查詢和設定 IPv6：</span><span class="sxs-lookup"><span data-stu-id="f6cf6-109">The following command is available on Windows XP with Service Pack 1 (SP1) and later to query and configure IPv6 on a local computer:</span></span>

-   [<span data-ttu-id="f6cf6-110">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="f6cf6-110">Netsh.exe</span></span>](netsh-exe.md)

<span data-ttu-id="f6cf6-111">使用 Netsh.exe 命令所做的設定變更是永久性的，而且在重新開機電腦或 IPv6 通訊協定時不會遺失。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-111">Configuration changes made using the Netsh.exe commands are permanent and are not lost when the computer or the IPv6 protocol is restarted.</span></span>

<span data-ttu-id="f6cf6-112">在 Windows XP Service Pack 1 (SP1) 之前，IPv6 設定和管理使用了數種舊版命令列工具 (Net.exe、Ipv6.exe 和 Ipsec6.exe) 來設定及管理 IPv6。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-112">Prior to Windows XP with Service Pack 1 (SP1), IPv6 configuration and management used several older command-line tools (Net.exe, Ipv6.exe, and Ipsec6.exe) to configure and manage IPv6.</span></span> <span data-ttu-id="f6cf6-113">使用這些較舊的工具，IPv6 變更不是永久性的，而且會在電腦或 IPv6 通訊協定重新開機時遺失。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-113">Using these older tools, the IPv6 changes are not permanent and are lost when the computer or the IPv6 protocol was restarted.</span></span> <span data-ttu-id="f6cf6-114">這些舊版的命令列工具只有在 Windows XP 上才受到支援。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-114">These older command-line tools are only supported on Windows XP.</span></span>

<span data-ttu-id="f6cf6-115">在 Windows XP （含 SP1）上，下列命令會顯示本機電腦上的 IPv6 介面清單，包括介面索引、介面名稱和各種其他介面屬性。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-115">On Windows XP with SP1, the following command will display the list of IPv6 interfaces on a local computer including the interface index, the interface name, and various other interface properties.</span></span>

<span data-ttu-id="f6cf6-116">**netsh interface ipv6 show 介面**</span><span class="sxs-lookup"><span data-stu-id="f6cf6-116">**netsh interface ipv6 show interface**</span></span>

<span data-ttu-id="f6cf6-117">在 Windows XP （含 SP1）上，下列命令會變更與介面索引相關聯的網站識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-117">On Windows XP with SP1, the following command will change the site identifier associated with an interface index.</span></span>

<span data-ttu-id="f6cf6-118">**netsh interface ipv6 set interface <InterfaceIndex or Name> siteid = value**</span><span class="sxs-lookup"><span data-stu-id="f6cf6-118">**netsh interface ipv6 set interface <InterfaceIndex or Name> siteid=value**</span></span>

<span data-ttu-id="f6cf6-119">在 Windows XP 上，下列舊版命令也會將與網站-本機位址相關聯的網站識別碼變更為3。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-119">On Windows XP, the following older command will also change the site identifier associated with a site-local address to 3.</span></span>

<span data-ttu-id="f6cf6-120">**ipv6 rtu fec0：：/10 3**</span><span class="sxs-lookup"><span data-stu-id="f6cf6-120">**ipv6 rtu fec0::/10 3**</span></span>

<span data-ttu-id="f6cf6-121">如果您要傳送或連接至範圍位址，則 [**sockaddr \_ in6**](sockaddr-2.md)結構中的 **sin6 \_ 範圍 \_ 識別碼** 成員可以保留未指定 (零) 代表不明確的範圍位址。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-121">If you are sending or connecting to a scoped address, then the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure can be left unspecified (zero) which represents an ambiguous scoped address.</span></span> <span data-ttu-id="f6cf6-122">例如，下列連結-本機位址是不明確的：</span><span class="sxs-lookup"><span data-stu-id="f6cf6-122">For example, the following link-local address is ambiguous:</span></span>

``` syntax
fe80::10
```

<span data-ttu-id="f6cf6-123">如果您要系結至有範圍的位址，則 [**sockaddr \_ in6**](sockaddr-2.md)結構中的 **sin6 \_ 範圍 \_ 識別碼** 成員必須包含非零值，以指定連結-本機位址的有效介面編號，或網站-本機位址的網站識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-123">If you are binding to a scoped address, then the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure must contain a nonzero value that specifies a valid interface number for a link-local address or a site identifier for a site-local address.</span></span>

## <a name="ambiguous-scoped-addresses"></a><span data-ttu-id="f6cf6-124">不明確的範圍位址</span><span class="sxs-lookup"><span data-stu-id="f6cf6-124">Ambiguous Scoped Addresses</span></span>

<span data-ttu-id="f6cf6-125">如果您要傳送或連接至範圍內的位址，而且尚未在 [**sockaddr \_ in6**](sockaddr-2.md)結構中指定 **sin6 \_ 範圍 \_ 識別碼** 成員，則範圍位址不明確。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-125">If you are sending or connecting to a scoped address and have not specified the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure, then the scoped address is ambiguous.</span></span> <span data-ttu-id="f6cf6-126">若要解決此問題，IPv6 通訊協定會先判斷您是否已將通訊端系結至來源位址。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-126">To resolve this, the IPv6 protocol first determines whether you have bound the socket to a source address.</span></span> <span data-ttu-id="f6cf6-127">如果是，系結來源位址會藉由提供介面編號或網站識別碼來解析不明確的情況。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-127">If so, the bound source address resolves the ambiguity by supplying an interface number or site identifier.</span></span>

<span data-ttu-id="f6cf6-128">如果您要傳送或連接至範圍位址，但未指定 **sin6 \_ 範圍 \_ 識別碼** 成員或系結來源位址，則 IPv6 通訊協定會檢查路由表。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-128">If you are sending or connecting to a scoped address and have neither specified the **sin6\_scope\_id** member nor bound a source address, then the IPv6 protocol checks the routing table.</span></span> <span data-ttu-id="f6cf6-129">例如，下列命令會在本機電腦上顯示 IPv6 路由表：</span><span class="sxs-lookup"><span data-stu-id="f6cf6-129">For example, the following command will display the IPv6 routing table on a local computer:</span></span>

<span data-ttu-id="f6cf6-130">**netsh interface ipv6 show route**</span><span class="sxs-lookup"><span data-stu-id="f6cf6-130">**netsh interface ipv6 show route**</span></span>

``` syntax
No   Manual   256  fe80::/64      13  Local Area Connection
No   Manual   256  fe80::/64      14  Wireless Network Connection
```

<span data-ttu-id="f6cf6-131">這表示預設會將連結-本機位址視為介面 \# 13 和14的連結 \# 。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-131">This indicates that link-local addresses are treated as on-link to interface \#13 and \#14 by default.</span></span>

<span data-ttu-id="f6cf6-132">當本機電腦有多張網路介面卡時，會發生混淆。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-132">Ambiguity arises when a local computer has multiple network adapters.</span></span> <span data-ttu-id="f6cf6-133">例如，上述的 **netsh** 命令表示有兩個網路介面 (區域網路連線，而無線網路連線) 。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-133">For example, the **netsh** command above indicates there are two network interfaces (Local Area Connection and Wireless Network Connection).</span></span> <span data-ttu-id="f6cf6-134">當應用程式指定目的地連結-本機位址 (fe80：：10時（例如) 不含範圍識別碼），並不會清除要用來傳送封包的介面卡。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-134">When an application specifies a destination link-local address (fe80::10, for example) without a scope ID, it is not clear which adapter to use to send the packet.</span></span> <span data-ttu-id="f6cf6-135">只有連結-本機單播 (fe80：：/64) 或連結範圍多播 (ff00：：/8) IPv6 目的地位址在傳送封包時，不會有範圍識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-135">Only a link-local unicast (fe80::/64) or a link-scope multicast (ff00::/8) IPv6 destination address can suffer from not having a scope ID when sending a packet.</span></span>

## <a name="neighbor-discovery"></a><span data-ttu-id="f6cf6-136">鄰居搜索</span><span class="sxs-lookup"><span data-stu-id="f6cf6-136">Neighbor Discovery</span></span>

<span data-ttu-id="f6cf6-137">如果您尚未在 [**sockaddr \_ in6**](sockaddr-2.md)結構中指定 **sin6 \_ 範圍 \_ 識別碼** 成員、未系結來源位址，而且尚未指定連結-本機位址的路由，則 IPv6 通訊協定會嘗試使用鄰居探索來解析目的地連結-本機位址。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-137">If you have not specified the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure, have not bound a source address, and have not specified a route for link-local addresses, then the IPv6 protocol will try Neighbor Discovery to resolve the destination link-local address.</span></span> <span data-ttu-id="f6cf6-138">針對正在傳送的指定封包，會嘗試一個介面。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-138">For a given packet being sent, one interface is tried.</span></span> <span data-ttu-id="f6cf6-139">第一個嘗試的介面視為最慣用的介面。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-139">This first interface that is tried is considered the most preferred interface.</span></span> <span data-ttu-id="f6cf6-140">如果鄰居探索無法解析介面上的連結-本機位址，則會捨棄要傳送的封包，而系統會記得目的地連結-本機位址無法透過該介面連線。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-140">If Neighbor Discovery fails to resolve the link-local address on an interface, the packet to be sent is dropped and the system remembers that the destination link-local address is not reachable over that interface.</span></span> <span data-ttu-id="f6cf6-141">在下一個要在所有相同條件下傳送的封包上，會嘗試使用不同的介面來進行鄰居探索。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-141">On the next packet to be sent under all of the same conditions, a different interface is tried for Neighbor Discovery.</span></span> <span data-ttu-id="f6cf6-142">此程式會繼續執行每個新封包的本機電腦上的每個介面，直到鄰近探索回應目的地連結-本機位址，或已嘗試和失敗所有可能的介面為止。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-142">This process continues through each of the interfaces on a local computer for each new packet until Neighbor Discovery responds for the destination link-local address or all of the possible interfaces have been tried and failed.</span></span> <span data-ttu-id="f6cf6-143">每次嘗試解決鄰近的問題時，就會刪除該鄰居的一個介面。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-143">Each time an attempt to resolve the neighbor fails, one interface is eliminated for that neighbor.</span></span>

<span data-ttu-id="f6cf6-144">如果目的地連結-本機位址解析，則會使用該介面來傳送目前的封包。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-144">If the destination link-local address resolves, then that interface is used to send the current packet.</span></span> <span data-ttu-id="f6cf6-145">此介面也會用於傳送至相同連結-本機目的地位址的任何後續不明確範圍封包。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-145">This interface is also used for any subsequent ambiguously-scoped packets that are sent to the same link-local destination address.</span></span>

<span data-ttu-id="f6cf6-146">如果鄰居探索無法解析所有介面上的目的地連結-本機位址，系統就會嘗試在最慣用的介面上傳送封包， (第一個介面嘗試) 。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-146">If Neighbor Discovery fails to resolve the destination link-local address on all interfaces, the system then tries to send the packet on the most preferred interface (the first interface tried).</span></span> <span data-ttu-id="f6cf6-147">網路堆疊會持續嘗試解析最慣用介面上的目的地連結-本機位址。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-147">The network stack keeps trying to resolve the destination link-local address on the most preferred interface.</span></span> <span data-ttu-id="f6cf6-148">在所有介面上的鄰近探索失敗之後的一段時間之後，網路堆疊會再次重新開機進程，並嘗試解析所有介面上的目的地連結-本機位址。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-148">After a period of time after Neighbor Discovery has failed on all interfaces, the network stack will restart the process again and try to resolve the destination link-local address on all of the interfaces.</span></span> <span data-ttu-id="f6cf6-149">目前，當鄰近探索在所有介面上再次嘗試時，此時間間隔為60秒。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-149">Currently, this time interval when Neighbor Discovery is again tried on all interfaces is 60 seconds.</span></span> <span data-ttu-id="f6cf6-150">不過，此時間間隔可能會在 Windows 版本上變更，因此應用程式不應假設。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-150">However, this time interval may change on versions of Windows and should not be assumed by an application.</span></span>

> [!Note]  
> <span data-ttu-id="f6cf6-151">如果應用程式在鄰居探索解析出連結-本機位址之後，將相同的連結-本機位址系結至不同的介面，則不會覆寫鄰居探索所傳回之連結-本機目的地位址的介面。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-151">If an application binds the same link-local address to a different interface after Neighbor Discovery has resolved the link-local address, that will not override the interface with the link-local destination address returned by Neighbor Discovery.</span></span>

 

<span data-ttu-id="f6cf6-152">如需有關 IP 第6版之鄰居探索的詳細資訊，請參閱 IETF 發佈的 [RFC4861](https://tools.ietf.org/html/rfc4861) 。</span><span class="sxs-lookup"><span data-stu-id="f6cf6-152">For more information on Neighbor Discovery for IP version 6, see [RFC4861](https://tools.ietf.org/html/rfc4861) published by the IETF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6cf6-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="f6cf6-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6cf6-154">IPv6 網站首碼</span><span class="sxs-lookup"><span data-stu-id="f6cf6-154">IPv6 Site Prefixes</span></span>](site-prefixes-2.md)
</dt> <dt>

[<span data-ttu-id="f6cf6-155">Ipv6.exe</span><span class="sxs-lookup"><span data-stu-id="f6cf6-155">Ipv6.exe</span></span>](ipv6-exe-2.md)
</dt> <dt>

[<span data-ttu-id="f6cf6-156">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="f6cf6-156">Netsh.exe</span></span>](netsh-exe.md)
</dt> <dt>

[<span data-ttu-id="f6cf6-157">使用 IPv6</span><span class="sxs-lookup"><span data-stu-id="f6cf6-157">Using IPv6</span></span>](using-ipv6-2.md)
</dt> </dl>

 

 



