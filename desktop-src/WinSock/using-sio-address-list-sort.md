---
description: SIO \_ 位址 \_ 清單 \_ 排序 IOCTL 可讓應用程式開發人員排序 IPv6 和 IPv4 目的地位址的清單，以判斷建立連接的最佳可用位址。 \_ \_ \_ Windows XP 和更新版本支援 SIO 地址清單排序的 IOCTL。
ms.assetid: bf380ddf-8171-4ef4-be47-94c7a6aabf0a
title: 使用 SIO_ADDRESS_LIST_SORT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6452023b69ccf72c78b393c5059fee497997af51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194723"
---
# <a name="using-sio_address_list_sort"></a><span data-ttu-id="37786-104">使用 SIO \_ 通訊 \_ 清單 \_ 排序</span><span class="sxs-lookup"><span data-stu-id="37786-104">Using SIO\_ADDRESS\_LIST\_SORT</span></span>

<span data-ttu-id="37786-105">**SIO \_ 位址 \_ 清單 \_ 排序** IOCTL 可讓應用程式開發人員排序 IPv6 和 IPv4 目的地位址的清單，以判斷建立連接的最佳可用位址。</span><span class="sxs-lookup"><span data-stu-id="37786-105">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL allows application developers to sort a list of IPv6 and IPv4 destination addresses to determine the best available address for making a connection.</span></span> <span data-ttu-id="37786-106">Windows XP 和更新版本支援 **SIO \_ 位址 \_ 清單 \_ 排序** 的 IOCTL。</span><span class="sxs-lookup"><span data-stu-id="37786-106">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL is supported on Windows XP and later.</span></span>

<span data-ttu-id="37786-107">在 Windows Vista 和更新版本上， [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) 函式會採用提供的潛在 IP 目的地地址清單、將目的地位址與主機電腦的本機 IP 位址配對，並根據最適合兩個對等互連的位址組來排序配對。</span><span class="sxs-lookup"><span data-stu-id="37786-107">On Windows Vista and later, the [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) function takes a supplied list of potential IP destination addresses, pairs the destination addresses with the host machine's local IP addresses, and sorts the pairs according to which address pair is best suited for communication between the two peers.</span></span> <span data-ttu-id="37786-108">**CreateSortedAddressPairs** 函式應該用在 Windows Vista 和更新版本上，而不是 **SIO \_ 通訊 \_ 清單 \_ 排序** 的 IOCTL。</span><span class="sxs-lookup"><span data-stu-id="37786-108">The **CreateSortedAddressPairs** function should be used instead of the **SIO\_ADDRESS\_LIST\_SORT** IOCTL on Windows Vista and later.</span></span>

<span data-ttu-id="37786-109">下列各節說明 **SIO \_ 通訊 \_ 清單 \_ 排序** 的使用考慮。</span><span class="sxs-lookup"><span data-stu-id="37786-109">The following sections describe usage considerations for **SIO\_ADDRESS\_LIST\_SORT**.</span></span>

## <a name="parameters"></a><span data-ttu-id="37786-110">參數</span><span class="sxs-lookup"><span data-stu-id="37786-110">Parameters</span></span>

<span data-ttu-id="37786-111">傳遞至 **SIO \_ 位址 \_ 清單 \_ 排序** 的緩衝區是 [**通訊端 \_ 位址 \_ 清單**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) 結構。</span><span class="sxs-lookup"><span data-stu-id="37786-111">The buffer passed to **SIO\_ADDRESS\_LIST\_SORT** is a [**SOCKET\_ADDRESS\_LIST**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) structure.</span></span> <span data-ttu-id="37786-112">清單中的每個 [**通訊端 \_ 位址**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) 都必須是 SOCKADDR \_ IN6 格式。</span><span class="sxs-lookup"><span data-stu-id="37786-112">Each [**SOCKET\_ADDRESS**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) in the list must be in SOCKADDR\_IN6 format.</span></span>

<span data-ttu-id="37786-113">**SIO \_ 位址 \_ 清單 \_ 排序** IOCTL 會在 Windows Vista 和更新版本上排序 IPv6 和 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="37786-113">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL sorts both IPv6 and IPv4 addresses on Windows Vista and later.</span></span> <span data-ttu-id="37786-114">清單中要排序的任何 IPv4 位址都必須是 IPv4 對應的 IPv6 位址格式。</span><span class="sxs-lookup"><span data-stu-id="37786-114">Any IPv4 addresses in the list to be sorted must be in the IPv4-mapped IPv6 address format.</span></span> <span data-ttu-id="37786-115">如需有關 IPv4 對應 IPv6 位址格式的詳細資訊，請參閱 [雙重堆疊通訊端](dual-stack-sockets.md)。</span><span class="sxs-lookup"><span data-stu-id="37786-115">For more information on the IPv4-mapped IPv6 address format, see [Dual-Stack Sockets](dual-stack-sockets.md).</span></span>

<span data-ttu-id="37786-116">在 Windows Server 2003 和 Windows XP 上， **SIO \_ 位址 \_ 清單 \_ 排序** 只會排序 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="37786-116">On Windows Server 2003, and Windows XP, **SIO\_ADDRESS\_LIST\_SORT** sorts only IPv6 addresses.</span></span> <span data-ttu-id="37786-117">不支援 ipv4 對應 IPv6 位址格式的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="37786-117">IPv4 addresses in the IPv4-mapped IPv6 address format are not supported.</span></span>

<span data-ttu-id="37786-118">在輸出中，如果 IOCTL 程式碼判斷某些目的地位址無效，則 [**通訊端 \_ 位址 \_ 清單**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85))結構的 **iAddressCount** 成員可能會小於輸入。</span><span class="sxs-lookup"><span data-stu-id="37786-118">On output, the **iAddressCount** member of the [**SOCKET\_ADDRESS\_LIST**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) structure may be smaller than on input if the IOCTL code determines that some destination addresses are invalid.</span></span>

## <a name="sorting-determination"></a><span data-ttu-id="37786-119">排序決定</span><span class="sxs-lookup"><span data-stu-id="37786-119">Sorting Determination</span></span>

<span data-ttu-id="37786-120">SIO 地址清單排序 IOCTL 的 IPv6 位址排序 \_ 順序 \_ 是以前置詞 \_ 原則表格為基礎。</span><span class="sxs-lookup"><span data-stu-id="37786-120">The sorting order for IPv6 addresses for the SIO\_ADDRESS\_LIST\_SORT IOCTL is based on the prefix policy table.</span></span> <span data-ttu-id="37786-121">首碼原則表格是使用 *Netsh.exe* 命令列公用程式來設定。</span><span class="sxs-lookup"><span data-stu-id="37786-121">The prefix policy table is configured using the *Netsh.exe* command line utility.</span></span> <span data-ttu-id="37786-122">下列命令列程式碼片段說明基本 *Netsh.exe* 首碼原則資料表設定命令：</span><span class="sxs-lookup"><span data-stu-id="37786-122">The following command line snippets illustrate basic *Netsh.exe* prefix policy table configuration commands:</span></span>

``` syntax
netsh interface ipv6 show prefixpolicies
netsh interface ipv6 add prefixpolicy ::/96 3 4
netsh interface ipv6 delete prefixpolicy ::/96
netsh interface ipv6 set prefixpolicy ::/96 3 4
```

> [!Note]  
> <span data-ttu-id="37786-123">在 Windows Server 2003 和 Windows XP 上，上面所列的第一個 netsh 命令如下所示。</span><span class="sxs-lookup"><span data-stu-id="37786-123">On Windows Server 2003 and Windows XP, the first netsh command listed above was as follows.</span></span> <span data-ttu-id="37786-124">所有其他相關的命令都相同。</span><span class="sxs-lookup"><span data-stu-id="37786-124">All other related commands are the same.</span></span>

 

``` syntax
netsh interface ipv6 show prefixpolicy
```

<span data-ttu-id="37786-125">位址順序也是由 IETF *(IPv6) 在 Internet Protocol 第6版3484的預設位址選擇* 上所述的演算法所決定。</span><span class="sxs-lookup"><span data-stu-id="37786-125">Address ordering is also determined by an algorithm outlined in the RFC 3484 on *Default Address Selection for Internet Protocol version 6 (IPv6)* published by the IETF.</span></span> <span data-ttu-id="37786-126">如需詳細資訊，請參閱 [https://www.ietf.org/rfc/rfc3484.txt](https://tools.ietf.org/html/rfc3484)。</span><span class="sxs-lookup"><span data-stu-id="37786-126">For more information, see [https://www.ietf.org/rfc/rfc3484.txt](https://tools.ietf.org/html/rfc3484).</span></span> <span data-ttu-id="37786-127"> (此資源可能僅提供英文版。 ) </span><span class="sxs-lookup"><span data-stu-id="37786-127">(This resource may only be available in English.)</span></span>

<span data-ttu-id="37786-128">**SIO \_ 位址 \_ 清單 \_ 排序** 的 IOCTL 會將位址從最差排序到最差，並視需要填滿 **sin6 \_ 範圍 \_ 識別碼** 成員。</span><span class="sxs-lookup"><span data-stu-id="37786-128">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL sorts addresses from best to worst, and fills in **sin6\_scope\_id** members, if needed.</span></span> <span data-ttu-id="37786-129">針對網站-本機位址，SIO \_ 位址 \_ 清單 \_ 排序會填入範圍識別碼，或移除位址。</span><span class="sxs-lookup"><span data-stu-id="37786-129">For site-local addresses, SIO\_ADDRESS\_LIST\_SORT either fills in the scope-id, or removes the address.</span></span>

<span data-ttu-id="37786-130">**SIO \_ 位址 \_ 清單 \_ 排序** IOCTL 會忽略系結至通訊端的來源位址，而且只會依據作為參數傳遞的目的地地址清單來排序。</span><span class="sxs-lookup"><span data-stu-id="37786-130">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL ignores the source address bound to the socket and only sorts by the destination address list passed as a parameter.</span></span>

<span data-ttu-id="37786-131">[**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs)函式應該用在 Windows Vista 和更新版本上，而不是 **SIO \_ 通訊 \_ 清單 \_ 排序** 的 IOCTL。</span><span class="sxs-lookup"><span data-stu-id="37786-131">The [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) function should be used instead of the **SIO\_ADDRESS\_LIST\_SORT** IOCTL on Windows Vista and later.</span></span> <span data-ttu-id="37786-132">**CreateSortedAddressPairs** 函式會傳回位址組清單，其中包含本機來源位址和目的地位址。</span><span class="sxs-lookup"><span data-stu-id="37786-132">The **CreateSortedAddressPairs** function returns a list of address pairs that contains a local source address and a destination address.</span></span> <span data-ttu-id="37786-133">這會提供應用程式正確的來源位址，以用於每個目的地位址。</span><span class="sxs-lookup"><span data-stu-id="37786-133">This provides an application the correct source address to use for each destination address.</span></span> <span data-ttu-id="37786-134">應用程式也可以藉由尋找特定的來源位址來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="37786-134">An application can also filter the results by looking for a specific source address.</span></span> <span data-ttu-id="37786-135">。</span><span class="sxs-lookup"><span data-stu-id="37786-135">in the results.</span></span>

## <a name="requirements"></a><span data-ttu-id="37786-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="37786-136">Requirements</span></span>

<span data-ttu-id="37786-137">**SIO \_ 位址 \_ 清單 \_ 排序** IOCTL 定義于 *Winsock2* 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="37786-137">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL is defined in the *Winsock2.h* header file.</span></span> <span data-ttu-id="37786-138">在 Windows Vista 和更新版本的 Microsoft Windows 軟體開發套件 (SDK) 發行時，標頭檔的組織已變更，且 **SIO \_ 位址 \_ 清單 \_ 排序** IOCTL 定義于 *Ws2def .h* 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="37786-138">On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and **SIO\_ADDRESS\_LIST\_SORT** IOCTL is defined in the *Ws2def.h* header file.</span></span> <span data-ttu-id="37786-139">請注意， *Ws2def .h* 標頭檔會自動包含在 *Winsock2* 中，而且絕不能直接使用。</span><span class="sxs-lookup"><span data-stu-id="37786-139">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

<span data-ttu-id="37786-140">Windows XP 和更新版本支援 **SIO \_ 位址 \_ 清單 \_ 排序** 的 IOCTL。</span><span class="sxs-lookup"><span data-stu-id="37786-140">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL is supported on Windows XP and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="37786-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="37786-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37786-142">**CreateSortedAddressPairs**</span><span class="sxs-lookup"><span data-stu-id="37786-142">**CreateSortedAddressPairs**</span></span>](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs)
</dt> </dl>

 

 
