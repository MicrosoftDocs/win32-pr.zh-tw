---
title: IP Helper 函式
description: 下列函式會在本機電腦上抓取和修改 TCP/IP 傳輸的設定。
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5f562470-f3e8-4305-a015-3a84cd09a1eb
ms.openlocfilehash: ae19803c25512242b613735a060c7beda8c1df70
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549503"
---
# <a name="ip-helper-functions"></a><span data-ttu-id="6d764-103">IP Helper 函式</span><span class="sxs-lookup"><span data-stu-id="6d764-103">IP Helper functions</span></span>

<span data-ttu-id="6d764-104">下列函式會在本機電腦上抓取和修改 TCP/IP 傳輸的設定。</span><span class="sxs-lookup"><span data-stu-id="6d764-104">The following functions retrieve and modify configuration settings for the TCP/IP transport on the local computer.</span></span> <span data-ttu-id="6d764-105">下列類別清單可協助您判斷哪一組函數最適合指定的工作。</span><span class="sxs-lookup"><span data-stu-id="6d764-105">The following categorical listing can help determine which collection of functions is best suited for a given task.</span></span>

-   [<span data-ttu-id="6d764-106">**GetNetworkConnectivityHint**</span><span class="sxs-lookup"><span data-stu-id="6d764-106">**GetNetworkConnectivityHint**</span></span>](/windows/win32/api/netioapi/nf-netioapi-getnetworkconnectivityhint)
-   [<span data-ttu-id="6d764-107">**GetNetworkConnectivityHintForInterface**</span><span class="sxs-lookup"><span data-stu-id="6d764-107">**GetNetworkConnectivityHintForInterface**</span></span>](/windows/win32/api/netioapi/nf-netioapi-getnetworkconnectivityhintforinterface)
-   [<span data-ttu-id="6d764-108">**NotifyNetworkConnectivityHintChange**</span><span class="sxs-lookup"><span data-stu-id="6d764-108">**NotifyNetworkConnectivityHintChange**</span></span>](/windows/win32/api/netioapi/nf-netioapi-notifynetworkconnectivityhintchange)

## <a name="adapter-management"></a><span data-ttu-id="6d764-109">介面卡管理</span><span class="sxs-lookup"><span data-stu-id="6d764-109">Adapter management</span></span>

-   [<span data-ttu-id="6d764-110">**GetAdapterIndex**</span><span class="sxs-lookup"><span data-stu-id="6d764-110">**GetAdapterIndex**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadapterindex)
-   [<span data-ttu-id="6d764-111">**GetAdaptersAddresses**</span><span class="sxs-lookup"><span data-stu-id="6d764-111">**GetAdaptersAddresses**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses)
-   [<span data-ttu-id="6d764-112">**GetAdaptersInfo**</span><span class="sxs-lookup"><span data-stu-id="6d764-112">**GetAdaptersInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadaptersinfo)
-   [<span data-ttu-id="6d764-113">**GetPerAdapterInfo**</span><span class="sxs-lookup"><span data-stu-id="6d764-113">**GetPerAdapterInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getperadapterinfo)
-   [<span data-ttu-id="6d764-114">**GetUniDirectionalAdapterInfo**</span><span class="sxs-lookup"><span data-stu-id="6d764-114">**GetUniDirectionalAdapterInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo)

## <a name="address-resolution-protocol-arp-management"></a><span data-ttu-id="6d764-115"> (ARP) 管理的位址解析通訊協定</span><span class="sxs-lookup"><span data-stu-id="6d764-115">Address Resolution Protocol (ARP) management</span></span>

-   [<span data-ttu-id="6d764-116">**CreateIpNetEntry**</span><span class="sxs-lookup"><span data-stu-id="6d764-116">**CreateIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createipnetentry)
-   [<span data-ttu-id="6d764-117">**CreateProxyArpEntry**</span><span class="sxs-lookup"><span data-stu-id="6d764-117">**CreateProxyArpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createproxyarpentry)
-   [<span data-ttu-id="6d764-118">**DeleteIpNetEntry**</span><span class="sxs-lookup"><span data-stu-id="6d764-118">**DeleteIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipnetentry)
-   [<span data-ttu-id="6d764-119">**DeleteProxyArpEntry**</span><span class="sxs-lookup"><span data-stu-id="6d764-119">**DeleteProxyArpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry)
-   [<span data-ttu-id="6d764-120">**FlushIpNetTable**</span><span class="sxs-lookup"><span data-stu-id="6d764-120">**FlushIpNetTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-flushipnettable)
-   [<span data-ttu-id="6d764-121">**GetIpNetTable**</span><span class="sxs-lookup"><span data-stu-id="6d764-121">**GetIpNetTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipnettable)
-   [<span data-ttu-id="6d764-122">**SendARP**</span><span class="sxs-lookup"><span data-stu-id="6d764-122">**SendARP**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-sendarp)
-   [<span data-ttu-id="6d764-123">**SetIpNetEntry**</span><span class="sxs-lookup"><span data-stu-id="6d764-123">**SetIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipnetentry)

## <a name="interface-conversion"></a><span data-ttu-id="6d764-124">介面轉換</span><span class="sxs-lookup"><span data-stu-id="6d764-124">Interface conversion</span></span>

-   [<span data-ttu-id="6d764-125">**ConvertInterfaceAliasToLuid**</span><span class="sxs-lookup"><span data-stu-id="6d764-125">**ConvertInterfaceAliasToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacealiastoluid)
-   [<span data-ttu-id="6d764-126">**ConvertInterfaceGuidToLuid**</span><span class="sxs-lookup"><span data-stu-id="6d764-126">**ConvertInterfaceGuidToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceguidtoluid)
-   [<span data-ttu-id="6d764-127">**ConvertInterfaceIndexToLuid**</span><span class="sxs-lookup"><span data-stu-id="6d764-127">**ConvertInterfaceIndexToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceindextoluid)
-   [<span data-ttu-id="6d764-128">**ConvertInterfaceLuidToAlias**</span><span class="sxs-lookup"><span data-stu-id="6d764-128">**ConvertInterfaceLuidToAlias**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoalias)
-   [<span data-ttu-id="6d764-129">**ConvertInterfaceLuidToGuid**</span><span class="sxs-lookup"><span data-stu-id="6d764-129">**ConvertInterfaceLuidToGuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoguid)
-   [<span data-ttu-id="6d764-130">**ConvertInterfaceLuidToIndex**</span><span class="sxs-lookup"><span data-stu-id="6d764-130">**ConvertInterfaceLuidToIndex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoindex)
-   [<span data-ttu-id="6d764-131">**ConvertInterfaceLuidToNameA**</span><span class="sxs-lookup"><span data-stu-id="6d764-131">**ConvertInterfaceLuidToNameA**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtonamea)
-   [<span data-ttu-id="6d764-132">**ConvertInterfaceLuidToNameW**</span><span class="sxs-lookup"><span data-stu-id="6d764-132">**ConvertInterfaceLuidToNameW**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtonamew)
-   [<span data-ttu-id="6d764-133">**ConvertInterfaceNameToLuidA**</span><span class="sxs-lookup"><span data-stu-id="6d764-133">**ConvertInterfaceNameToLuidA**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacenametoluida)
-   [<span data-ttu-id="6d764-134">**ConvertInterfaceNameToLuidW**</span><span class="sxs-lookup"><span data-stu-id="6d764-134">**ConvertInterfaceNameToLuidW**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacenametoluidw)
-   [<span data-ttu-id="6d764-135">**如果 \_ indextoname**</span><span class="sxs-lookup"><span data-stu-id="6d764-135">**if\_indextoname**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-if_indextoname)
-   [<span data-ttu-id="6d764-136">**如果 \_ nametoindex**</span><span class="sxs-lookup"><span data-stu-id="6d764-136">**if\_nametoindex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-if_nametoindex)

## <a name="interface-management"></a><span data-ttu-id="6d764-137">介面管理</span><span class="sxs-lookup"><span data-stu-id="6d764-137">Interface management</span></span>

-   [<span data-ttu-id="6d764-138">**GetFriendlyIfIndex**</span><span class="sxs-lookup"><span data-stu-id="6d764-138">**GetFriendlyIfIndex**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex)
-   [<span data-ttu-id="6d764-139">**GetIfEntry**</span><span class="sxs-lookup"><span data-stu-id="6d764-139">**GetIfEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getifentry)
-   [<span data-ttu-id="6d764-140">**GetIfEntry2**</span><span class="sxs-lookup"><span data-stu-id="6d764-140">**GetIfEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifentry2)
-   [<span data-ttu-id="6d764-141">**GetIfEntry2Ex**</span><span class="sxs-lookup"><span data-stu-id="6d764-141">**GetIfEntry2Ex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifentry2ex)
-   [<span data-ttu-id="6d764-142">**GetIfStackTable**</span><span class="sxs-lookup"><span data-stu-id="6d764-142">**GetIfStackTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifstacktable)
-   [<span data-ttu-id="6d764-143">**GetIfTable**</span><span class="sxs-lookup"><span data-stu-id="6d764-143">**GetIfTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getiftable)
-   [<span data-ttu-id="6d764-144">**GetIfTable2**</span><span class="sxs-lookup"><span data-stu-id="6d764-144">**GetIfTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getiftable2)
-   [<span data-ttu-id="6d764-145">**GetIfTable2Ex**</span><span class="sxs-lookup"><span data-stu-id="6d764-145">**GetIfTable2Ex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getiftable2ex)
-   [<span data-ttu-id="6d764-146">**GetInterfaceInfo**</span><span class="sxs-lookup"><span data-stu-id="6d764-146">**GetInterfaceInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo)
-   [<span data-ttu-id="6d764-147">**GetInvertedIfStackTable**</span><span class="sxs-lookup"><span data-stu-id="6d764-147">**GetInvertedIfStackTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getinvertedifstacktable)
-   [<span data-ttu-id="6d764-148">**GetIpInterfaceEntry**</span><span class="sxs-lookup"><span data-stu-id="6d764-148">**GetIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipinterfaceentry)
-   [<span data-ttu-id="6d764-149">**GetIpInterfaceTable**</span><span class="sxs-lookup"><span data-stu-id="6d764-149">**GetIpInterfaceTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipinterfacetable)
-   [<span data-ttu-id="6d764-150">**GetNumberOfInterfaces**</span><span class="sxs-lookup"><span data-stu-id="6d764-150">**GetNumberOfInterfaces**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces)
-   [<span data-ttu-id="6d764-151">**InitializeIpInterfaceEntry**</span><span class="sxs-lookup"><span data-stu-id="6d764-151">**InitializeIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeipinterfaceentry)
-   [<span data-ttu-id="6d764-152">**SetIfEntry**</span><span class="sxs-lookup"><span data-stu-id="6d764-152">**SetIfEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setifentry)
-   [<span data-ttu-id="6d764-153">**SetIpInterfaceEntry**</span><span class="sxs-lookup"><span data-stu-id="6d764-153">**SetIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipinterfaceentry)

## <a name="internet-protocol-ip-and-internet-control-message-protocol-icmp"></a><span data-ttu-id="6d764-154">網際網路通訊協定 (IP) 和網際網路控制訊息通訊協定 (ICMP) </span><span class="sxs-lookup"><span data-stu-id="6d764-154">Internet Protocol (IP) and Internet Control Message Protocol (ICMP)</span></span>

-   [<span data-ttu-id="6d764-155">**GetIcmpStatistics**</span><span class="sxs-lookup"><span data-stu-id="6d764-155">**GetIcmpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-geticmpstatistics)
-   [<span data-ttu-id="6d764-156">**GetIpStatistics**</span><span class="sxs-lookup"><span data-stu-id="6d764-156">**GetIpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipstatistics)
-   [<span data-ttu-id="6d764-157">**Icmp6CreateFile**</span><span class="sxs-lookup"><span data-stu-id="6d764-157">**Icmp6CreateFile**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6createfile)
-   [<span data-ttu-id="6d764-158">**Icmp6ParseReplies**</span><span class="sxs-lookup"><span data-stu-id="6d764-158">**Icmp6ParseReplies**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6parsereplies)
-   [<span data-ttu-id="6d764-159">**Icmp6SendEcho2**</span><span class="sxs-lookup"><span data-stu-id="6d764-159">**Icmp6SendEcho2**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6sendecho2)
-   [<span data-ttu-id="6d764-160">**IcmpCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="6d764-160">**IcmpCloseHandle**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpclosehandle)
-   [<span data-ttu-id="6d764-161">**IcmpCreateFile**</span><span class="sxs-lookup"><span data-stu-id="6d764-161">**IcmpCreateFile**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpcreatefile)
-   [<span data-ttu-id="6d764-162">**IcmpParseReplies**</span><span class="sxs-lookup"><span data-stu-id="6d764-162">**IcmpParseReplies**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpparsereplies)
-   [<span data-ttu-id="6d764-163">**IcmpSendEcho**</span><span class="sxs-lookup"><span data-stu-id="6d764-163">**IcmpSendEcho**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho)
-   [<span data-ttu-id="6d764-164">**IcmpSendEcho2**</span><span class="sxs-lookup"><span data-stu-id="6d764-164">**IcmpSendEcho2**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho2)
-   [<span data-ttu-id="6d764-165">**IcmpSendEcho2Ex**</span><span class="sxs-lookup"><span data-stu-id="6d764-165">**IcmpSendEcho2Ex**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho2ex)
-   [<span data-ttu-id="6d764-166">**SetIpTTL**</span><span class="sxs-lookup"><span data-stu-id="6d764-166">**SetIpTTL**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipttl)

## <a name="ip-address-management"></a><span data-ttu-id="6d764-167">IP 位址管理</span><span class="sxs-lookup"><span data-stu-id="6d764-167">IP address management</span></span>

-   [<span data-ttu-id="6d764-168">**AddIPAddress**</span><span class="sxs-lookup"><span data-stu-id="6d764-168">**AddIPAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-addipaddress)
-   [<span data-ttu-id="6d764-169">**CreateAnycastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="6d764-169">**CreateAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createanycastipaddressentry)
-   [<span data-ttu-id="6d764-170">**CreateUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="6d764-170">**CreateUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createunicastipaddressentry)
-   [<span data-ttu-id="6d764-171">**DeleteIPAddress**</span><span class="sxs-lookup"><span data-stu-id="6d764-171">**DeleteIPAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipaddress)
-   [<span data-ttu-id="6d764-172">**DeleteAnycastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="6d764-172">**DeleteAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteanycastipaddressentry)
-   [<span data-ttu-id="6d764-173">**DeleteUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="6d764-173">**DeleteUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteunicastipaddressentry)
-   [<span data-ttu-id="6d764-174">**GetAnycastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="6d764-174">**GetAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getanycastipaddressentry)
-   [<span data-ttu-id="6d764-175">**GetAnycastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="6d764-175">**GetAnycastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getanycastipaddresstable)
-   [<span data-ttu-id="6d764-176">**GetIpAddrTable**</span><span class="sxs-lookup"><span data-stu-id="6d764-176">**GetIpAddrTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipaddrtable)
-   [<span data-ttu-id="6d764-177">**GetMulticastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="6d764-177">**GetMulticastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getmulticastipaddressentry)
-   [<span data-ttu-id="6d764-178">**GetMulticastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="6d764-178">**GetMulticastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getmulticastipaddresstable)
-   [<span data-ttu-id="6d764-179">**GetUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="6d764-179">**GetUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getunicastipaddressentry)
-   [<span data-ttu-id="6d764-180">**GetUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="6d764-180">**GetUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getunicastipaddresstable)
-   [<span data-ttu-id="6d764-181">**InitializeUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="6d764-181">**InitializeUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeunicastipaddressentry)
-   [<span data-ttu-id="6d764-182">**IpReleaseAddress**</span><span class="sxs-lookup"><span data-stu-id="6d764-182">**IpReleaseAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress)
-   [<span data-ttu-id="6d764-183">**IpRenewAddress**</span><span class="sxs-lookup"><span data-stu-id="6d764-183">**IpRenewAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-iprenewaddress)
-   [<span data-ttu-id="6d764-184">**NotifyStableUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="6d764-184">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)
-   [<span data-ttu-id="6d764-185">**SetUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="6d764-185">**SetUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setunicastipaddressentry)

## <a name="ip-address-string-conversion"></a><span data-ttu-id="6d764-186">IP 位址字串轉換</span><span class="sxs-lookup"><span data-stu-id="6d764-186">IP address string conversion</span></span>

-   [<span data-ttu-id="6d764-187">**RtlIpv4AddressToString**</span><span class="sxs-lookup"><span data-stu-id="6d764-187">**RtlIpv4AddressToString**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4addresstostringa)
-   [<span data-ttu-id="6d764-188">**RtlIpv4AddressToStringEx**</span><span class="sxs-lookup"><span data-stu-id="6d764-188">**RtlIpv4AddressToStringEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4addresstostringexw)
-   [<span data-ttu-id="6d764-189">**RtlIpv4StringToAddress**</span><span class="sxs-lookup"><span data-stu-id="6d764-189">**RtlIpv4StringToAddress**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa)
-   [<span data-ttu-id="6d764-190">**RtlIpv4StringToAddressEx**</span><span class="sxs-lookup"><span data-stu-id="6d764-190">**RtlIpv4StringToAddressEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw)
-   [<span data-ttu-id="6d764-191">**RtlIpv6AddressToString**</span><span class="sxs-lookup"><span data-stu-id="6d764-191">**RtlIpv6AddressToString**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringa)
-   [<span data-ttu-id="6d764-192">**RtlIpv6AddressToStringEx**</span><span class="sxs-lookup"><span data-stu-id="6d764-192">**RtlIpv6AddressToStringEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringexw)
-   [<span data-ttu-id="6d764-193">**RtlIpv6StringToAddress**</span><span class="sxs-lookup"><span data-stu-id="6d764-193">**RtlIpv6StringToAddress**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)
-   [<span data-ttu-id="6d764-194">**RtlIpv6StringToAddressEx**</span><span class="sxs-lookup"><span data-stu-id="6d764-194">**RtlIpv6StringToAddressEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw)

## <a name="ip-neighbor-address-management"></a><span data-ttu-id="6d764-195">IP 鄰居位址管理</span><span class="sxs-lookup"><span data-stu-id="6d764-195">IP neighbor address management</span></span>

-   [<span data-ttu-id="6d764-196">**CreateIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="6d764-196">**CreateIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createipnetentry2)
-   [<span data-ttu-id="6d764-197">**DeleteIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="6d764-197">**DeleteIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteipnetentry2)
-   [<span data-ttu-id="6d764-198">**FlushIpNetTable2**</span><span class="sxs-lookup"><span data-stu-id="6d764-198">**FlushIpNetTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-flushipnettable2)
-   [<span data-ttu-id="6d764-199">**GetIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="6d764-199">**GetIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipnetentry2)
-   [<span data-ttu-id="6d764-200">**GetIpNetTable2**</span><span class="sxs-lookup"><span data-stu-id="6d764-200">**GetIpNetTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipnettable2)
-   [<span data-ttu-id="6d764-201">**ResolveIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="6d764-201">**ResolveIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-resolveipnetentry2)
-   [<span data-ttu-id="6d764-202">**ResolveNeighbor**</span><span class="sxs-lookup"><span data-stu-id="6d764-202">**ResolveNeighbor**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-resolveneighbor)
-   [<span data-ttu-id="6d764-203">**SetIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="6d764-203">**SetIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipnetentry2)

## <a name="ip-path-management"></a><span data-ttu-id="6d764-204">IP 路徑管理</span><span class="sxs-lookup"><span data-stu-id="6d764-204">IP path management</span></span>

-   [<span data-ttu-id="6d764-205">**FlushIpPathTable**</span><span class="sxs-lookup"><span data-stu-id="6d764-205">**FlushIpPathTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-flushippathtable)
-   [<span data-ttu-id="6d764-206">**GetIpPathEntry**</span><span class="sxs-lookup"><span data-stu-id="6d764-206">**GetIpPathEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getippathentry)
-   [<span data-ttu-id="6d764-207">**GetIpPathTable**</span><span class="sxs-lookup"><span data-stu-id="6d764-207">**GetIpPathTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getippathtable)

## <a name="ip-route-management"></a><span data-ttu-id="6d764-208">IP 路由管理</span><span class="sxs-lookup"><span data-stu-id="6d764-208">IP route management</span></span>

-   [<span data-ttu-id="6d764-209">**CreateIpForwardEntry**</span><span class="sxs-lookup"><span data-stu-id="6d764-209">**CreateIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createipforwardentry)
-   [<span data-ttu-id="6d764-210">**CreateIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="6d764-210">**CreateIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createipforwardentry2)
-   [<span data-ttu-id="6d764-211">**DeleteIpForwardEntry**</span><span class="sxs-lookup"><span data-stu-id="6d764-211">**DeleteIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)
-   [<span data-ttu-id="6d764-212">**DeleteIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="6d764-212">**DeleteIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteipforwardentry2)
-   [<span data-ttu-id="6d764-213">**EnableRouter**</span><span class="sxs-lookup"><span data-stu-id="6d764-213">**EnableRouter**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-enablerouter)
-   [<span data-ttu-id="6d764-214">**GetBestInterface**</span><span class="sxs-lookup"><span data-stu-id="6d764-214">**GetBestInterface**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestinterface)
-   [<span data-ttu-id="6d764-215">**GetBestInterfaceEx**</span><span class="sxs-lookup"><span data-stu-id="6d764-215">**GetBestInterfaceEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestinterfaceex)
-   [<span data-ttu-id="6d764-216">**GetBestRoute**</span><span class="sxs-lookup"><span data-stu-id="6d764-216">**GetBestRoute**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestroute)
-   [<span data-ttu-id="6d764-217">**GetBestRoute2**</span><span class="sxs-lookup"><span data-stu-id="6d764-217">**GetBestRoute2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getbestroute2)
-   [<span data-ttu-id="6d764-218">**GetIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="6d764-218">**GetIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipforwardentry2)
-   [<span data-ttu-id="6d764-219">**GetIpForwardTable**</span><span class="sxs-lookup"><span data-stu-id="6d764-219">**GetIpForwardTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipforwardtable)
-   [<span data-ttu-id="6d764-220">**GetIpForwardTable2**</span><span class="sxs-lookup"><span data-stu-id="6d764-220">**GetIpForwardTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipforwardtable2)
-   [<span data-ttu-id="6d764-221">**GetRTTAndHopCount**</span><span class="sxs-lookup"><span data-stu-id="6d764-221">**GetRTTAndHopCount**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getrttandhopcount)
-   [<span data-ttu-id="6d764-222">**InitializeIpForwardEntry**</span><span class="sxs-lookup"><span data-stu-id="6d764-222">**InitializeIpForwardEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeipforwardentry)
-   [<span data-ttu-id="6d764-223">**SetIpForwardEntry**</span><span class="sxs-lookup"><span data-stu-id="6d764-223">**SetIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipforwardentry)
-   [<span data-ttu-id="6d764-224">**SetIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="6d764-224">**SetIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipforwardentry2)
-   [<span data-ttu-id="6d764-225">**SetIpStatistics**</span><span class="sxs-lookup"><span data-stu-id="6d764-225">**SetIpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipstatistics)
-   [<span data-ttu-id="6d764-226">**SetIpStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="6d764-226">**SetIpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipstatisticsex)
-   [<span data-ttu-id="6d764-227">**UnenableRouter**</span><span class="sxs-lookup"><span data-stu-id="6d764-227">**UnenableRouter**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-unenablerouter)

## <a name="ip-table-memory-management"></a><span data-ttu-id="6d764-228">IP 資料表記憶體管理</span><span class="sxs-lookup"><span data-stu-id="6d764-228">IP table memory management</span></span>

-   [<span data-ttu-id="6d764-229">**FreeMibTable**</span><span class="sxs-lookup"><span data-stu-id="6d764-229">**FreeMibTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-freemibtable)

## <a name="ip-utility"></a><span data-ttu-id="6d764-230">IP 公用程式</span><span class="sxs-lookup"><span data-stu-id="6d764-230">IP utility</span></span>

-   [<span data-ttu-id="6d764-231">**ConvertIpv4MaskToLength**</span><span class="sxs-lookup"><span data-stu-id="6d764-231">**ConvertIpv4MaskToLength**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertipv4masktolength)
-   [<span data-ttu-id="6d764-232">**ConvertLengthToIpv4Mask**</span><span class="sxs-lookup"><span data-stu-id="6d764-232">**ConvertLengthToIpv4Mask**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertlengthtoipv4mask)
-   [<span data-ttu-id="6d764-233">**CreateSortedAddressPairs**</span><span class="sxs-lookup"><span data-stu-id="6d764-233">**CreateSortedAddressPairs**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createsortedaddresspairs)
-   [<span data-ttu-id="6d764-234">**ParseNetworkString**</span><span class="sxs-lookup"><span data-stu-id="6d764-234">**ParseNetworkString**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-parsenetworkstring)

## <a name="network-configuration"></a><span data-ttu-id="6d764-235">網路組態</span><span class="sxs-lookup"><span data-stu-id="6d764-235">Network configuration</span></span>

-   [<span data-ttu-id="6d764-236">**GetNetworkParams**</span><span class="sxs-lookup"><span data-stu-id="6d764-236">**GetNetworkParams**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getnetworkparams)

## <a name="notification"></a><span data-ttu-id="6d764-237">通知</span><span class="sxs-lookup"><span data-stu-id="6d764-237">Notification</span></span>

-   [<span data-ttu-id="6d764-238">**CancelMibChangeNotify2**</span><span class="sxs-lookup"><span data-stu-id="6d764-238">**CancelMibChangeNotify2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-cancelmibchangenotify2)
-   [<span data-ttu-id="6d764-239">**NotifyAddrChange**</span><span class="sxs-lookup"><span data-stu-id="6d764-239">**NotifyAddrChange**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-notifyaddrchange)
-   [<span data-ttu-id="6d764-240">**NotifyIpInterfaceChange**</span><span class="sxs-lookup"><span data-stu-id="6d764-240">**NotifyIpInterfaceChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyipinterfacechange)
-   [<span data-ttu-id="6d764-241">**NotifyRouteChange**</span><span class="sxs-lookup"><span data-stu-id="6d764-241">**NotifyRouteChange**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-notifyroutechange)
-   [<span data-ttu-id="6d764-242">**NotifyRouteChange2**</span><span class="sxs-lookup"><span data-stu-id="6d764-242">**NotifyRouteChange2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyroutechange2)
-   [<span data-ttu-id="6d764-243">**NotifyUnicastIpAddressChange**</span><span class="sxs-lookup"><span data-stu-id="6d764-243">**NotifyUnicastIpAddressChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyunicastipaddresschange)

## <a name="packet-timestamping"></a><span data-ttu-id="6d764-244">封包時間戳記</span><span class="sxs-lookup"><span data-stu-id="6d764-244">Packet timestamping</span></span>

-   [<span data-ttu-id="6d764-245">**CaptureInterfaceHardwareCrossTimestamp**</span><span class="sxs-lookup"><span data-stu-id="6d764-245">**CaptureInterfaceHardwareCrossTimestamp**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp)
-   [<span data-ttu-id="6d764-246">**GetInterfaceActiveTimestampCapabilities**</span><span class="sxs-lookup"><span data-stu-id="6d764-246">**GetInterfaceActiveTimestampCapabilities**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities)
-   [<span data-ttu-id="6d764-247">**GetInterfaceSupportedTimestampCapabilities**</span><span class="sxs-lookup"><span data-stu-id="6d764-247">**GetInterfaceSupportedTimestampCapabilities**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities)
-   [<span data-ttu-id="6d764-248">**RegisterInterfaceTimestampConfigChange**</span><span class="sxs-lookup"><span data-stu-id="6d764-248">**RegisterInterfaceTimestampConfigChange**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-registerinterfacetimestampconfigchange)
-   [<span data-ttu-id="6d764-249">**UnregisterInterfaceTimestampConfigChange**</span><span class="sxs-lookup"><span data-stu-id="6d764-249">**UnregisterInterfaceTimestampConfigChange**</span></span>](/windows/win32/api/iphlpapi/unregisterinterfacetimestampconfigchange)

## <a name="persistent-port-reservation"></a><span data-ttu-id="6d764-250">持續性埠保留</span><span class="sxs-lookup"><span data-stu-id="6d764-250">Persistent port reservation</span></span>

-   [<span data-ttu-id="6d764-251">**CreatePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="6d764-251">**CreatePersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)
-   [<span data-ttu-id="6d764-252">**CreatePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="6d764-252">**CreatePersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createpersistentudpportreservation)
-   [<span data-ttu-id="6d764-253">**DeletePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="6d764-253">**DeletePersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)
-   [<span data-ttu-id="6d764-254">**DeletePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="6d764-254">**DeletePersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)
-   [<span data-ttu-id="6d764-255">**LookupPersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="6d764-255">**LookupPersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)
-   [<span data-ttu-id="6d764-256">**LookupPersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="6d764-256">**LookupPersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

## <a name="security-health"></a><span data-ttu-id="6d764-257">安全性健康狀態</span><span class="sxs-lookup"><span data-stu-id="6d764-257">Security health</span></span>

-   <span data-ttu-id="6d764-258">[**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6d764-258">[**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))</span></span>
-   <span data-ttu-id="6d764-259">[**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6d764-259">[**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))</span></span>

<span data-ttu-id="6d764-260">這些函式只會在 Windows Server 2003 上定義。</span><span class="sxs-lookup"><span data-stu-id="6d764-260">These functions are defined only on Windows Server 2003.</span></span>

> [!Note]  
> <span data-ttu-id="6d764-261">這些功能不適用於 Windows Vista，也不適用於 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="6d764-261">These functions are not available on Windows Vista, nor on Windows Server 2008.</span></span>

## <a name="teredo-ipv6-client-management"></a><span data-ttu-id="6d764-262">Teredo IPv6 用戶端管理</span><span class="sxs-lookup"><span data-stu-id="6d764-262">Teredo IPv6 client management</span></span>

-   [<span data-ttu-id="6d764-263">**GetTeredoPort**</span><span class="sxs-lookup"><span data-stu-id="6d764-263">**GetTeredoPort**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getteredoport)
-   [<span data-ttu-id="6d764-264">**NotifyTeredoPortChange**</span><span class="sxs-lookup"><span data-stu-id="6d764-264">**NotifyTeredoPortChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyteredoportchange)
-   [<span data-ttu-id="6d764-265">**NotifyStableUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="6d764-265">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)

## <a name="transmission-control-protocol-tcp-and-user-datagram-protocol-udp"></a><span data-ttu-id="6d764-266">傳輸控制通訊協定 (TCP) 和使用者資料包協定 (UDP) </span><span class="sxs-lookup"><span data-stu-id="6d764-266">Transmission Control Protocol (TCP) and User Datagram Protocol (UDP)</span></span>

-   [<span data-ttu-id="6d764-267">**GetExtendedTcpTable**</span><span class="sxs-lookup"><span data-stu-id="6d764-267">**GetExtendedTcpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getextendedtcptable)
-   [<span data-ttu-id="6d764-268">**GetExtendedUdpTable**</span><span class="sxs-lookup"><span data-stu-id="6d764-268">**GetExtendedUdpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getextendedudptable)
-   [<span data-ttu-id="6d764-269">**GetOwnerModuleFromTcp6Entry**</span><span class="sxs-lookup"><span data-stu-id="6d764-269">**GetOwnerModuleFromTcp6Entry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcp6entry)
-   [<span data-ttu-id="6d764-270">**GetOwnerModuleFromTcpEntry**</span><span class="sxs-lookup"><span data-stu-id="6d764-270">**GetOwnerModuleFromTcpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcpentry)
-   [<span data-ttu-id="6d764-271">**GetOwnerModuleFromUdp6Entry**</span><span class="sxs-lookup"><span data-stu-id="6d764-271">**GetOwnerModuleFromUdp6Entry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromudp6entry)
-   [<span data-ttu-id="6d764-272">**GetOwnerModuleFromUdpEntry**</span><span class="sxs-lookup"><span data-stu-id="6d764-272">**GetOwnerModuleFromUdpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromudpentry)
-   [<span data-ttu-id="6d764-273">**GetPerTcp6ConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="6d764-273">**GetPerTcp6ConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getpertcp6connectionestats)
-   [<span data-ttu-id="6d764-274">**GetPerTcpConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="6d764-274">**GetPerTcpConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getpertcpconnectionestats)
-   [<span data-ttu-id="6d764-275">**GetTcpStatistics**</span><span class="sxs-lookup"><span data-stu-id="6d764-275">**GetTcpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatistics)
-   [<span data-ttu-id="6d764-276">**GetTcpStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="6d764-276">**GetTcpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatisticsex)
-   [<span data-ttu-id="6d764-277">**GetTcpStatisticsEx2**</span><span class="sxs-lookup"><span data-stu-id="6d764-277">**GetTcpStatisticsEx2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatisticsex2)
-   [<span data-ttu-id="6d764-278">**GetTcp6Table**</span><span class="sxs-lookup"><span data-stu-id="6d764-278">**GetTcp6Table**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcp6table)
-   [<span data-ttu-id="6d764-279">**GetTcp6Table2**</span><span class="sxs-lookup"><span data-stu-id="6d764-279">**GetTcp6Table2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcp6table2)
-   [<span data-ttu-id="6d764-280">**GetTcpTable**</span><span class="sxs-lookup"><span data-stu-id="6d764-280">**GetTcpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcptable)
-   [<span data-ttu-id="6d764-281">**GetTcpTable2**</span><span class="sxs-lookup"><span data-stu-id="6d764-281">**GetTcpTable2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcptable2)
-   [<span data-ttu-id="6d764-282">**SetPerTcp6ConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="6d764-282">**SetPerTcp6ConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setpertcp6connectionestats)
-   [<span data-ttu-id="6d764-283">**SetPerTcpConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="6d764-283">**SetPerTcpConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setpertcpconnectionestats)
-   [<span data-ttu-id="6d764-284">**SetTcpEntry**</span><span class="sxs-lookup"><span data-stu-id="6d764-284">**SetTcpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-settcpentry)
-   [<span data-ttu-id="6d764-285">**GetUdp6Table**</span><span class="sxs-lookup"><span data-stu-id="6d764-285">**GetUdp6Table**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudp6table)
-   [<span data-ttu-id="6d764-286">**GetUdpStatistics**</span><span class="sxs-lookup"><span data-stu-id="6d764-286">**GetUdpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatistics)
-   [<span data-ttu-id="6d764-287">**GetUdpStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="6d764-287">**GetUdpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatisticsex)
-   [<span data-ttu-id="6d764-288">**GetUdpStatisticsEx2**</span><span class="sxs-lookup"><span data-stu-id="6d764-288">**GetUdpStatisticsEx2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatisticsex2)
-   [<span data-ttu-id="6d764-289">**GetUdpTable**</span><span class="sxs-lookup"><span data-stu-id="6d764-289">**GetUdpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudptable)

## <a name="deprecated-apis"></a><span data-ttu-id="6d764-290">已被取代的 API</span><span class="sxs-lookup"><span data-stu-id="6d764-290">Deprecated APIs</span></span>

> [!Note]  
> <span data-ttu-id="6d764-291">這些函式已被取代，Microsoft 並不支援這些功能。</span><span class="sxs-lookup"><span data-stu-id="6d764-291">These functions are deprecated, and are not supported by Microsoft.</span></span>

-   [<span data-ttu-id="6d764-292">**AllocateAndGetTcpExTableFromStack**</span><span class="sxs-lookup"><span data-stu-id="6d764-292">**AllocateAndGetTcpExTableFromStack**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-allocateandgettcpextablefromstack)
-   [<span data-ttu-id="6d764-293">**AllocateAndGetUdpExTableFromStack**</span><span class="sxs-lookup"><span data-stu-id="6d764-293">**AllocateAndGetUdpExTableFromStack**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-allocateandgetudpextablefromstack)
