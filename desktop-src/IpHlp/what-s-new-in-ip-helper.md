---
description: IP Helper 的新功能
ms.assetid: fa9d72d0-2f9c-433d-b05a-8423664b2e3e
title: IP Helper 的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2c1a6eebb3e9e785e8988b822df0b2a80ae6eba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320583"
---
# <a name="whats-new-in-ip-helper"></a><span data-ttu-id="d2660-103">IP Helper 的新功能</span><span class="sxs-lookup"><span data-stu-id="d2660-103">What's New in IP Helper</span></span>

## <a name="windows-8-and-windows-server-2012"></a><span data-ttu-id="d2660-104">Windows 8 與 Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d2660-104">Windows 8 and Windows Server 2012</span></span>

<span data-ttu-id="d2660-105">下列功能已新增至 Windows 8 和 Windows Server 2012 上的 IP 協助程式 Api。</span><span class="sxs-lookup"><span data-stu-id="d2660-105">The following features have been added to the IP Helper APIs on Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="d2660-106">函式，可抓取網路連接的歷程記錄頻寬估計值。</span><span class="sxs-lookup"><span data-stu-id="d2660-106">A function that retrieves historical bandwidth estimates for a network connection.</span></span> <span data-ttu-id="d2660-107">如需詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="d2660-107">For more information, see:</span></span>

-   [<span data-ttu-id="d2660-108">**GetIpNetworkConnectionBandwidthEstimates**</span><span class="sxs-lookup"><span data-stu-id="d2660-108">**GetIpNetworkConnectionBandwidthEstimates**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getipnetworkconnectionbandwidthestimates)

<span data-ttu-id="d2660-109">結構，其中包含 TCP/IP 堆疊所決定之可用頻寬估計值和相關聯的變異數的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d2660-109">A structure that contains information on the available bandwidth estimates and associated variance as determined by the TCP/IP stack.</span></span> <span data-ttu-id="d2660-110">如需詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="d2660-110">For more information, see:</span></span>

-   [<span data-ttu-id="d2660-111">**NL \_ 頻寬 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="d2660-111">**NL\_BANDWIDTH\_INFORMATION**</span></span>](/windows/desktop/api/Nldef/ns-nldef-nl_bandwidth_information)

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="d2660-112">Windows 7 與 Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d2660-112">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="d2660-113">下列功能已新增至 Windows 7 和 Windows Server 2008 R2 上的 IP 協助程式 Api。</span><span class="sxs-lookup"><span data-stu-id="d2660-113">The following features have been added to the IP Helper APIs on Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="d2660-114">在乙太網路 MAC 位址的二進位格式和字串格式之間轉換乙太網路位址的函式。</span><span class="sxs-lookup"><span data-stu-id="d2660-114">Functions that convert an Ethernet address between a binary format and string format for the Ethernet MAC address.</span></span> <span data-ttu-id="d2660-115">如需詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="d2660-115">For more information, see:</span></span>

-   [<span data-ttu-id="d2660-116">**RtlEthernetAddressToString**</span><span class="sxs-lookup"><span data-stu-id="d2660-116">**RtlEthernetAddressToString**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlethernetaddresstostringa)
-   [<span data-ttu-id="d2660-117">**RtlEthernetStringToAddress**</span><span class="sxs-lookup"><span data-stu-id="d2660-117">**RtlEthernetStringToAddress**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlethernetstringtoaddressa)

## <a name="windows-server-2008-and-windows-vista-sp1"></a><span data-ttu-id="d2660-118">Windows Server 2008 和 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="d2660-118">Windows Server 2008 and Windows Vista SP1</span></span>

<span data-ttu-id="d2660-119">下列功能已新增至 Windows Server 2008 和 Windows Vista Service Pack 1 (SP1) 上的 IP 協助程式 Api。</span><span class="sxs-lookup"><span data-stu-id="d2660-119">The following functions have been added to the IP Helper APIs on Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="d2660-120">適用于 IPv4 和網際網路控制訊息通訊協定的函式 (ICMP) 。</span><span class="sxs-lookup"><span data-stu-id="d2660-120">A function that works with IPv4 and the Internet Control Message Protocol (ICMP).</span></span> <span data-ttu-id="d2660-121">如需詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="d2660-121">For more information, see:</span></span>

-   [<span data-ttu-id="d2660-122">**IcmpSendEcho2Ex**</span><span class="sxs-lookup"><span data-stu-id="d2660-122">**IcmpSendEcho2Ex**</span></span>](/windows/desktop/api/Icmpapi/nf-icmpapi-icmpsendecho2ex)

## <a name="windows-vista"></a><span data-ttu-id="d2660-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2660-123">Windows Vista</span></span>

<span data-ttu-id="d2660-124">Windows Vista 和更新版本上的 IP 協助程式 Api 已新增下列函式群組。</span><span class="sxs-lookup"><span data-stu-id="d2660-124">The following groups of functions have been added to the IP Helper APIs on Windows Vista and later.</span></span>

<span data-ttu-id="d2660-125">使用 IPv6 和 IPv4 進行介面轉換的函式。</span><span class="sxs-lookup"><span data-stu-id="d2660-125">Functions that work with both IPv6 and IPv4 for interface conversion.</span></span> <span data-ttu-id="d2660-126">如需詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="d2660-126">For more information, see:</span></span>

-   [<span data-ttu-id="d2660-127">**ConvertInterfaceAliasToLuid**</span><span class="sxs-lookup"><span data-stu-id="d2660-127">**ConvertInterfaceAliasToLuid**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfacealiastoluid)
-   [<span data-ttu-id="d2660-128">**ConvertInterfaceGuidToLuid**</span><span class="sxs-lookup"><span data-stu-id="d2660-128">**ConvertInterfaceGuidToLuid**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceguidtoluid)
-   [<span data-ttu-id="d2660-129">**ConvertInterfaceIndexToLuid**</span><span class="sxs-lookup"><span data-stu-id="d2660-129">**ConvertInterfaceIndexToLuid**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceindextoluid)
-   [<span data-ttu-id="d2660-130">**ConvertInterfaceLuidToGuid**</span><span class="sxs-lookup"><span data-stu-id="d2660-130">**ConvertInterfaceLuidToGuid**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtoguid)
-   [<span data-ttu-id="d2660-131">**ConvertInterfaceLuidToIndex**</span><span class="sxs-lookup"><span data-stu-id="d2660-131">**ConvertInterfaceLuidToIndex**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtoindex)
-   [<span data-ttu-id="d2660-132">**ConvertInterfaceLuidToNameA**</span><span class="sxs-lookup"><span data-stu-id="d2660-132">**ConvertInterfaceLuidToNameA**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtonamea)
-   [<span data-ttu-id="d2660-133">**ConvertInterfaceLuidToNameW**</span><span class="sxs-lookup"><span data-stu-id="d2660-133">**ConvertInterfaceLuidToNameW**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtonamew)
-   [<span data-ttu-id="d2660-134">**ConvertInterfaceNameToLuidA**</span><span class="sxs-lookup"><span data-stu-id="d2660-134">**ConvertInterfaceNameToLuidA**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfacenametoluida)
-   [<span data-ttu-id="d2660-135">**ConvertInterfaceNameToLuidW**</span><span class="sxs-lookup"><span data-stu-id="d2660-135">**ConvertInterfaceNameToLuidW**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfacenametoluidw)
-   [<span data-ttu-id="d2660-136">**如果 \_ indextoname**</span><span class="sxs-lookup"><span data-stu-id="d2660-136">**if\_indextoname**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-if_indextoname)
-   [<span data-ttu-id="d2660-137">**如果 \_ nametoindex**</span><span class="sxs-lookup"><span data-stu-id="d2660-137">**if\_nametoindex**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-if_nametoindex)

<span data-ttu-id="d2660-138">使用 IPv6 和 IPv4 進行介面管理的函式。</span><span class="sxs-lookup"><span data-stu-id="d2660-138">Functions that work with both IPv6 and IPv4 for interface management.</span></span> <span data-ttu-id="d2660-139">如需詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="d2660-139">For more information, see:</span></span>

-   [<span data-ttu-id="d2660-140">**GetIfEntry2**</span><span class="sxs-lookup"><span data-stu-id="d2660-140">**GetIfEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getifentry2)
-   [<span data-ttu-id="d2660-141">**GetIfStackTable**</span><span class="sxs-lookup"><span data-stu-id="d2660-141">**GetIfStackTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getifstacktable)
-   [<span data-ttu-id="d2660-142">**GetIfTable2**</span><span class="sxs-lookup"><span data-stu-id="d2660-142">**GetIfTable2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getiftable2)
-   [<span data-ttu-id="d2660-143">**GetIfTable2Ex**</span><span class="sxs-lookup"><span data-stu-id="d2660-143">**GetIfTable2Ex**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getiftable2ex)
-   [<span data-ttu-id="d2660-144">**GetInvertedIfStackTable**</span><span class="sxs-lookup"><span data-stu-id="d2660-144">**GetInvertedIfStackTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getinvertedifstacktable)
-   [<span data-ttu-id="d2660-145">**GetIpInterfaceEntry**</span><span class="sxs-lookup"><span data-stu-id="d2660-145">**GetIpInterfaceEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getipinterfaceentry)
-   [<span data-ttu-id="d2660-146">**GetIpInterfaceTable**</span><span class="sxs-lookup"><span data-stu-id="d2660-146">**GetIpInterfaceTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getipinterfacetable)
-   [<span data-ttu-id="d2660-147">**InitializeIpInterfaceEntry**</span><span class="sxs-lookup"><span data-stu-id="d2660-147">**InitializeIpInterfaceEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-initializeipinterfaceentry)
-   [<span data-ttu-id="d2660-148">**SetIpInterfaceEntry**</span><span class="sxs-lookup"><span data-stu-id="d2660-148">**SetIpInterfaceEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-setipinterfaceentry)

<span data-ttu-id="d2660-149">適用于 IP 位址管理的 IPv6 和 IPv4 功能。</span><span class="sxs-lookup"><span data-stu-id="d2660-149">Functions that work with both IPv6 and IPv4 for IP address management.</span></span> <span data-ttu-id="d2660-150">如需詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="d2660-150">For more information, see:</span></span>

-   [<span data-ttu-id="d2660-151">**CreateAnycastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="d2660-151">**CreateAnycastIpAddressEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-createanycastipaddressentry)
-   [<span data-ttu-id="d2660-152">**CreateUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="d2660-152">**CreateUnicastIpAddressEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-createunicastipaddressentry)
-   [<span data-ttu-id="d2660-153">**DeleteAnycastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="d2660-153">**DeleteAnycastIpAddressEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-deleteanycastipaddressentry)
-   [<span data-ttu-id="d2660-154">**DeleteUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="d2660-154">**DeleteUnicastIpAddressEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-deleteunicastipaddressentry)
-   [<span data-ttu-id="d2660-155">**GetAnycastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="d2660-155">**GetAnycastIpAddressEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getanycastipaddressentry)
-   [<span data-ttu-id="d2660-156">**GetAnycastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="d2660-156">**GetAnycastIpAddressTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getanycastipaddresstable)
-   [<span data-ttu-id="d2660-157">**GetMulticastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="d2660-157">**GetMulticastIpAddressEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getmulticastipaddressentry)
-   [<span data-ttu-id="d2660-158">**GetMulticastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="d2660-158">**GetMulticastIpAddressTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getmulticastipaddresstable)
-   [<span data-ttu-id="d2660-159">**GetUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="d2660-159">**GetUnicastIpAddressEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getunicastipaddressentry)
-   [<span data-ttu-id="d2660-160">**GetUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="d2660-160">**GetUnicastIpAddressTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getunicastipaddresstable)
-   [<span data-ttu-id="d2660-161">**InitializeUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="d2660-161">**InitializeUnicastIpAddressEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-initializeunicastipaddressentry)
-   [<span data-ttu-id="d2660-162">**NotifyStableUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="d2660-162">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)
-   [<span data-ttu-id="d2660-163">**SetUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="d2660-163">**SetUnicastIpAddressEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-setunicastipaddressentry)

<span data-ttu-id="d2660-164">適用于 IP 資料表記憶體管理的 IPv6 和 IPv4 函數。</span><span class="sxs-lookup"><span data-stu-id="d2660-164">A function that works with both IPv6 and IPv4 for IP table memory management.</span></span> <span data-ttu-id="d2660-165">如需詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="d2660-165">For more information, see:</span></span>

-   [<span data-ttu-id="d2660-166">**FreeMibTable**</span><span class="sxs-lookup"><span data-stu-id="d2660-166">**FreeMibTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-freemibtable)

<span data-ttu-id="d2660-167">適用于 IP 鄰居位址管理的 IPv6 和 IPv4 功能。</span><span class="sxs-lookup"><span data-stu-id="d2660-167">Functions that work with both IPv6 and IPv4 for IP neighbor address management.</span></span> <span data-ttu-id="d2660-168">如需詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="d2660-168">For more information, see:</span></span>

-   [<span data-ttu-id="d2660-169">**CreateIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="d2660-169">**CreateIpNetEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-createipnetentry2)
-   [<span data-ttu-id="d2660-170">**DeleteIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="d2660-170">**DeleteIpNetEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-deleteipnetentry2)
-   [<span data-ttu-id="d2660-171">**FlushIpNetTable2**</span><span class="sxs-lookup"><span data-stu-id="d2660-171">**FlushIpNetTable2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-flushipnettable2)
-   [<span data-ttu-id="d2660-172">**GetIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="d2660-172">**GetIpNetEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getipnetentry2)
-   [<span data-ttu-id="d2660-173">**GetIpNetTable2**</span><span class="sxs-lookup"><span data-stu-id="d2660-173">**GetIpNetTable2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getipnettable2)
-   [<span data-ttu-id="d2660-174">**ResolveIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="d2660-174">**ResolveIpNetEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-resolveipnetentry2)
-   [<span data-ttu-id="d2660-175">**ResolveNeighbor**</span><span class="sxs-lookup"><span data-stu-id="d2660-175">**ResolveNeighbor**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-resolveneighbor)
-   [<span data-ttu-id="d2660-176">**SetIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="d2660-176">**SetIpNetEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-setipnetentry2)

<span data-ttu-id="d2660-177">適用于 IP 路徑管理的 IPv6 和 IPv4 功能。</span><span class="sxs-lookup"><span data-stu-id="d2660-177">Functions that work with both IPv6 and IPv4 for IP path management.</span></span> <span data-ttu-id="d2660-178">如需詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="d2660-178">For more information, see:</span></span>

-   [<span data-ttu-id="d2660-179">**FlushIpPathTable**</span><span class="sxs-lookup"><span data-stu-id="d2660-179">**FlushIpPathTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-flushippathtable)
-   [<span data-ttu-id="d2660-180">**GetIpPathEntry**</span><span class="sxs-lookup"><span data-stu-id="d2660-180">**GetIpPathEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getippathentry)
-   [<span data-ttu-id="d2660-181">**GetIpPathTable**</span><span class="sxs-lookup"><span data-stu-id="d2660-181">**GetIpPathTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getippathtable)

<span data-ttu-id="d2660-182">適用于 IP 路由管理的 IPv6 和 IPv4 功能。</span><span class="sxs-lookup"><span data-stu-id="d2660-182">Functions that work with both IPv6 and IPv4 for IP route management.</span></span> <span data-ttu-id="d2660-183">如需詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="d2660-183">For more information, see:</span></span>

-   [<span data-ttu-id="d2660-184">**CreateIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="d2660-184">**CreateIpForwardEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-createipforwardentry2)
-   [<span data-ttu-id="d2660-185">**DeleteIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="d2660-185">**DeleteIpForwardEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-deleteipforwardentry2)
-   [<span data-ttu-id="d2660-186">**GetBestRoute2**</span><span class="sxs-lookup"><span data-stu-id="d2660-186">**GetBestRoute2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getbestroute2)
-   [<span data-ttu-id="d2660-187">**GetIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="d2660-187">**GetIpForwardEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getipforwardentry2)
-   [<span data-ttu-id="d2660-188">**GetIpForwardTable2**</span><span class="sxs-lookup"><span data-stu-id="d2660-188">**GetIpForwardTable2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getipforwardtable2)
-   [<span data-ttu-id="d2660-189">**InitializeIpForwardEntry**</span><span class="sxs-lookup"><span data-stu-id="d2660-189">**InitializeIpForwardEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-initializeipforwardentry)
-   [<span data-ttu-id="d2660-190">**SetIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="d2660-190">**SetIpForwardEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-setipforwardentry2)
-   [<span data-ttu-id="d2660-191">**SetIpStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="d2660-191">**SetIpStatisticsEx**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatisticsex)

<span data-ttu-id="d2660-192">適用于通知的 IPv6 和 IPv4 函數。</span><span class="sxs-lookup"><span data-stu-id="d2660-192">Functions that work with both IPv6 and IPv4 for notification.</span></span> <span data-ttu-id="d2660-193">如需詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="d2660-193">For more information, see:</span></span>

-   [<span data-ttu-id="d2660-194">**CancelMibChangeNotify2**</span><span class="sxs-lookup"><span data-stu-id="d2660-194">**CancelMibChangeNotify2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-cancelmibchangenotify2)
-   [<span data-ttu-id="d2660-195">**NotifyIpInterfaceChange**</span><span class="sxs-lookup"><span data-stu-id="d2660-195">**NotifyIpInterfaceChange**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-notifyipinterfacechange)
-   [<span data-ttu-id="d2660-196">**NotifyRouteChange2**</span><span class="sxs-lookup"><span data-stu-id="d2660-196">**NotifyRouteChange2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-notifyroutechange2)
-   [<span data-ttu-id="d2660-197">**NotifyUnicastIpAddressChange**</span><span class="sxs-lookup"><span data-stu-id="d2660-197">**NotifyUnicastIpAddressChange**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-notifyunicastipaddresschange)

<span data-ttu-id="d2660-198">使用 IP 位址的公用程式函數。</span><span class="sxs-lookup"><span data-stu-id="d2660-198">Utility functions that work with IP addresses.</span></span> <span data-ttu-id="d2660-199">如需詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="d2660-199">For more information, see:</span></span>

-   [<span data-ttu-id="d2660-200">**ConvertIpv4MaskToLength**</span><span class="sxs-lookup"><span data-stu-id="d2660-200">**ConvertIpv4MaskToLength**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertipv4masktolength)
-   [<span data-ttu-id="d2660-201">**ConvertLengthToIpv4Mask**</span><span class="sxs-lookup"><span data-stu-id="d2660-201">**ConvertLengthToIpv4Mask**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertlengthtoipv4mask)
-   [<span data-ttu-id="d2660-202">**CreateSortedAddressPairs**</span><span class="sxs-lookup"><span data-stu-id="d2660-202">**CreateSortedAddressPairs**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-createsortedaddresspairs)
-   [<span data-ttu-id="d2660-203">**ParseNetworkString**</span><span class="sxs-lookup"><span data-stu-id="d2660-203">**ParseNetworkString**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-parsenetworkstring)

<span data-ttu-id="d2660-204">使用傳輸控制通訊協定的函式 (TCP) 和使用者資料包協定 (UDP) ，以抓取 IPv6 或 IPv4 TCP 連接資料表或 UDP 接聽程式資料表。</span><span class="sxs-lookup"><span data-stu-id="d2660-204">Functions that work with Transmission Control Protocol (TCP) and User Datagram Protocol (UDP) to retrieve the IPv6 or IPv4 TCP connection table or UDP listener table.</span></span> <span data-ttu-id="d2660-205">如需詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="d2660-205">For more information, see:</span></span>

-   [<span data-ttu-id="d2660-206">**GetTcp6Table**</span><span class="sxs-lookup"><span data-stu-id="d2660-206">**GetTcp6Table**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcp6table)
-   [<span data-ttu-id="d2660-207">**GetTcp6Table2**</span><span class="sxs-lookup"><span data-stu-id="d2660-207">**GetTcp6Table2**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcp6table2)
-   [<span data-ttu-id="d2660-208">**GetTcpTable2**</span><span class="sxs-lookup"><span data-stu-id="d2660-208">**GetTcpTable2**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable2)
-   [<span data-ttu-id="d2660-209">**GetUdp6Table**</span><span class="sxs-lookup"><span data-stu-id="d2660-209">**GetUdp6Table**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudp6table)

<span data-ttu-id="d2660-210">使用傳輸控制通訊協定的函式 (TCP) ，以抓取連接上的延伸 TCP 統計資料。</span><span class="sxs-lookup"><span data-stu-id="d2660-210">Functions that work with Transmission Control Protocol (TCP) to retrieve extended TCP statistics on a connection.</span></span> <span data-ttu-id="d2660-211">如需詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="d2660-211">For more information, see:</span></span>

-   [<span data-ttu-id="d2660-212">**GetPerTcp6ConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="d2660-212">**GetPerTcp6ConnectionEStats**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getpertcp6connectionestats)
-   [<span data-ttu-id="d2660-213">**GetPerTcpConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="d2660-213">**GetPerTcpConnectionEStats**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getpertcpconnectionestats)
-   [<span data-ttu-id="d2660-214">**SetPerTcp6ConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="d2660-214">**SetPerTcp6ConnectionEStats**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setpertcp6connectionestats)
-   [<span data-ttu-id="d2660-215">**SetPerTcpConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="d2660-215">**SetPerTcpConnectionEStats**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setpertcpconnectionestats)

<span data-ttu-id="d2660-216">適用于 Teredo IPv6 用戶端管理的新函數。</span><span class="sxs-lookup"><span data-stu-id="d2660-216">New functions that work for Teredo IPv6 client management.</span></span> <span data-ttu-id="d2660-217">如需詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="d2660-217">For more information, see:</span></span>

-   [<span data-ttu-id="d2660-218">**GetTeredoPort**</span><span class="sxs-lookup"><span data-stu-id="d2660-218">**GetTeredoPort**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getteredoport)
-   [<span data-ttu-id="d2660-219">**NotifyTeredoPortChange**</span><span class="sxs-lookup"><span data-stu-id="d2660-219">**NotifyTeredoPortChange**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-notifyteredoportchange)
-   [<span data-ttu-id="d2660-220">**NotifyStableUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="d2660-220">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)

<span data-ttu-id="d2660-221">提供 IP 位址與 IP 位址字串表示之間轉換的公用程式函數。</span><span class="sxs-lookup"><span data-stu-id="d2660-221">Utility functions that provide conversions between IP addresses and string representations of IP addresses.</span></span> <span data-ttu-id="d2660-222">如需詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="d2660-222">For more information, see:</span></span>

-   [<span data-ttu-id="d2660-223">**RtlIpv4AddressToString**</span><span class="sxs-lookup"><span data-stu-id="d2660-223">**RtlIpv4AddressToString**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringa)
-   [<span data-ttu-id="d2660-224">**RtlIpv4AddressToStringEx**</span><span class="sxs-lookup"><span data-stu-id="d2660-224">**RtlIpv4AddressToStringEx**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringexw)
-   [<span data-ttu-id="d2660-225">**RtlIpv4StringToAddress**</span><span class="sxs-lookup"><span data-stu-id="d2660-225">**RtlIpv4StringToAddress**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa)
-   [<span data-ttu-id="d2660-226">**RtlIpv4StringToAddressEx**</span><span class="sxs-lookup"><span data-stu-id="d2660-226">**RtlIpv4StringToAddressEx**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw)
-   [<span data-ttu-id="d2660-227">**RtlIpv6AddressToString**</span><span class="sxs-lookup"><span data-stu-id="d2660-227">**RtlIpv6AddressToString**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa)
-   [<span data-ttu-id="d2660-228">**RtlIpv6AddressToStringEx**</span><span class="sxs-lookup"><span data-stu-id="d2660-228">**RtlIpv6AddressToStringEx**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexw)
-   [<span data-ttu-id="d2660-229">**RtlIpv6StringToAddress**</span><span class="sxs-lookup"><span data-stu-id="d2660-229">**RtlIpv6StringToAddress**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)
-   [<span data-ttu-id="d2660-230">**RtlIpv6StringToAddressEx**</span><span class="sxs-lookup"><span data-stu-id="d2660-230">**RtlIpv6StringToAddressEx**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw)

<span data-ttu-id="d2660-231">為本機電腦上的 TCP 或 UDP 埠連續區塊提供持續保留的函式。</span><span class="sxs-lookup"><span data-stu-id="d2660-231">Functions that provide persistent reservations for a consecutive block of TCP or UDP ports on the local computer.</span></span> <span data-ttu-id="d2660-232">如需詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="d2660-232">For more information, see:</span></span>

-   [<span data-ttu-id="d2660-233">**CreatePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="d2660-233">**CreatePersistentTcpPortReservation**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)
-   [<span data-ttu-id="d2660-234">**CreatePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="d2660-234">**CreatePersistentUdpPortReservation**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createpersistentudpportreservation)
-   [<span data-ttu-id="d2660-235">**DeletePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="d2660-235">**DeletePersistentTcpPortReservation**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)
-   [<span data-ttu-id="d2660-236">**DeletePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="d2660-236">**DeletePersistentUdpPortReservation**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)
-   [<span data-ttu-id="d2660-237">**LookupPersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="d2660-237">**LookupPersistentTcpPortReservation**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)
-   [<span data-ttu-id="d2660-238">**LookupPersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="d2660-238">**LookupPersistentUdpPortReservation**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

## <a name="windows-server-2003"></a><span data-ttu-id="d2660-239">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d2660-239">Windows Server 2003</span></span>

<span data-ttu-id="d2660-240">下列函式已新增至 Windows Server 2003 和更新版本上的 IP Helper Api：</span><span class="sxs-lookup"><span data-stu-id="d2660-240">The following functions have been added to the IP Helper APIs on Windows Server 2003 and later:</span></span>

-   <span data-ttu-id="d2660-241">[**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d2660-241">[**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))</span></span>
-   <span data-ttu-id="d2660-242">[**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d2660-242">[**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))</span></span>

## <a name="windows-xp-sp2"></a><span data-ttu-id="d2660-243">Windows XP SP2</span><span class="sxs-lookup"><span data-stu-id="d2660-243">Windows XP SP2</span></span>

<span data-ttu-id="d2660-244">下列功能已新增至 Windows XP Service Pack 2 (SP2) 和更新版本上的 IP 協助程式 Api：</span><span class="sxs-lookup"><span data-stu-id="d2660-244">The following functions have been added to the IP Helper APIs on Windows XP with Service Pack 2 (SP2) and later:</span></span>

-   [<span data-ttu-id="d2660-245">**GetOwnerModuleFromTcpEntry**</span><span class="sxs-lookup"><span data-stu-id="d2660-245">**GetOwnerModuleFromTcpEntry**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcpentry)
-   [<span data-ttu-id="d2660-246">**GetOwnerModuleFromTcp6Entry**</span><span class="sxs-lookup"><span data-stu-id="d2660-246">**GetOwnerModuleFromTcp6Entry**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcp6entry)
-   [<span data-ttu-id="d2660-247">**GetOwnerModuleFromUdpEntry**</span><span class="sxs-lookup"><span data-stu-id="d2660-247">**GetOwnerModuleFromUdpEntry**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromudpentry)
-   [<span data-ttu-id="d2660-248">**GetOwnerModuleFromUdp6Entry**</span><span class="sxs-lookup"><span data-stu-id="d2660-248">**GetOwnerModuleFromUdp6Entry**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromudp6entry)

 

 
