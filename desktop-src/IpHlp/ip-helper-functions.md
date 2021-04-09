---
description: 下列函式會在本機電腦上抓取和修改 TCP/IP 傳輸的設定。
ms.assetid: 5f562470-f3e8-4305-a015-3a84cd09a1eb
title: IP 協助程式函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c8bff21f41c04bb5aecf505b251fbbe2f8bc62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695627"
---
# <a name="ip-helper-functions"></a><span data-ttu-id="7dba0-103">IP Helper 函式</span><span class="sxs-lookup"><span data-stu-id="7dba0-103">IP Helper functions</span></span>

<span data-ttu-id="7dba0-104">下列函式會在本機電腦上抓取和修改 TCP/IP 傳輸的設定。</span><span class="sxs-lookup"><span data-stu-id="7dba0-104">The following functions retrieve and modify configuration settings for the TCP/IP transport on the local computer.</span></span> <span data-ttu-id="7dba0-105">下列類別清單可協助您判斷哪一組函數最適合指定的工作。</span><span class="sxs-lookup"><span data-stu-id="7dba0-105">The following categorical listing can help determine which collection of functions is best suited for a given task.</span></span>

-   [<span data-ttu-id="7dba0-106">**GetNetworkConnectivityHint**</span><span class="sxs-lookup"><span data-stu-id="7dba0-106">**GetNetworkConnectivityHint**</span></span>](/windows/win32/api/netioapi/nf-netioapi-getnetworkconnectivityhint)
-   [<span data-ttu-id="7dba0-107">**GetNetworkConnectivityHintForInterface**</span><span class="sxs-lookup"><span data-stu-id="7dba0-107">**GetNetworkConnectivityHintForInterface**</span></span>](/windows/win32/api/netioapi/nf-netioapi-getnetworkconnectivityhintforinterface)
-   [<span data-ttu-id="7dba0-108">**NotifyNetworkConnectivityHintChange**</span><span class="sxs-lookup"><span data-stu-id="7dba0-108">**NotifyNetworkConnectivityHintChange**</span></span>](/windows/win32/api/netioapi/nf-netioapi-notifynetworkconnectivityhintchange)

## <a name="adapter-management"></a><span data-ttu-id="7dba0-109">介面卡管理</span><span class="sxs-lookup"><span data-stu-id="7dba0-109">Adapter management</span></span>

-   [<span data-ttu-id="7dba0-110">**GetAdapterIndex**</span><span class="sxs-lookup"><span data-stu-id="7dba0-110">**GetAdapterIndex**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadapterindex)
-   [<span data-ttu-id="7dba0-111">**GetAdaptersAddresses**</span><span class="sxs-lookup"><span data-stu-id="7dba0-111">**GetAdaptersAddresses**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses)
-   [<span data-ttu-id="7dba0-112">**GetAdaptersInfo**</span><span class="sxs-lookup"><span data-stu-id="7dba0-112">**GetAdaptersInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadaptersinfo)
-   [<span data-ttu-id="7dba0-113">**GetPerAdapterInfo**</span><span class="sxs-lookup"><span data-stu-id="7dba0-113">**GetPerAdapterInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getperadapterinfo)
-   [<span data-ttu-id="7dba0-114">**GetUniDirectionalAdapterInfo**</span><span class="sxs-lookup"><span data-stu-id="7dba0-114">**GetUniDirectionalAdapterInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo)

## <a name="address-resolution-protocol-arp-management"></a><span data-ttu-id="7dba0-115"> (ARP) 管理的位址解析通訊協定</span><span class="sxs-lookup"><span data-stu-id="7dba0-115">Address Resolution Protocol (ARP) management</span></span>

-   [<span data-ttu-id="7dba0-116">**CreateIpNetEntry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-116">**CreateIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createipnetentry)
-   [<span data-ttu-id="7dba0-117">**CreateProxyArpEntry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-117">**CreateProxyArpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createproxyarpentry)
-   [<span data-ttu-id="7dba0-118">**DeleteIpNetEntry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-118">**DeleteIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipnetentry)
-   [<span data-ttu-id="7dba0-119">**DeleteProxyArpEntry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-119">**DeleteProxyArpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry)
-   [<span data-ttu-id="7dba0-120">**FlushIpNetTable**</span><span class="sxs-lookup"><span data-stu-id="7dba0-120">**FlushIpNetTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-flushipnettable)
-   [<span data-ttu-id="7dba0-121">**GetIpNetTable**</span><span class="sxs-lookup"><span data-stu-id="7dba0-121">**GetIpNetTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipnettable)
-   [<span data-ttu-id="7dba0-122">**SendARP**</span><span class="sxs-lookup"><span data-stu-id="7dba0-122">**SendARP**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-sendarp)
-   [<span data-ttu-id="7dba0-123">**SetIpNetEntry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-123">**SetIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipnetentry)

## <a name="interface-conversion"></a><span data-ttu-id="7dba0-124">介面轉換</span><span class="sxs-lookup"><span data-stu-id="7dba0-124">Interface conversion</span></span>

-   [<span data-ttu-id="7dba0-125">**ConvertInterfaceAliasToLuid**</span><span class="sxs-lookup"><span data-stu-id="7dba0-125">**ConvertInterfaceAliasToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacealiastoluid)
-   [<span data-ttu-id="7dba0-126">**ConvertInterfaceGuidToLuid**</span><span class="sxs-lookup"><span data-stu-id="7dba0-126">**ConvertInterfaceGuidToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceguidtoluid)
-   [<span data-ttu-id="7dba0-127">**ConvertInterfaceIndexToLuid**</span><span class="sxs-lookup"><span data-stu-id="7dba0-127">**ConvertInterfaceIndexToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceindextoluid)
-   [<span data-ttu-id="7dba0-128">**ConvertInterfaceLuidToAlias**</span><span class="sxs-lookup"><span data-stu-id="7dba0-128">**ConvertInterfaceLuidToAlias**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoalias)
-   [<span data-ttu-id="7dba0-129">**ConvertInterfaceLuidToGuid**</span><span class="sxs-lookup"><span data-stu-id="7dba0-129">**ConvertInterfaceLuidToGuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoguid)
-   [<span data-ttu-id="7dba0-130">**ConvertInterfaceLuidToIndex**</span><span class="sxs-lookup"><span data-stu-id="7dba0-130">**ConvertInterfaceLuidToIndex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoindex)
-   [<span data-ttu-id="7dba0-131">**ConvertInterfaceLuidToNameA**</span><span class="sxs-lookup"><span data-stu-id="7dba0-131">**ConvertInterfaceLuidToNameA**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtonamea)
-   [<span data-ttu-id="7dba0-132">**ConvertInterfaceLuidToNameW**</span><span class="sxs-lookup"><span data-stu-id="7dba0-132">**ConvertInterfaceLuidToNameW**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtonamew)
-   [<span data-ttu-id="7dba0-133">**ConvertInterfaceNameToLuidA**</span><span class="sxs-lookup"><span data-stu-id="7dba0-133">**ConvertInterfaceNameToLuidA**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacenametoluida)
-   [<span data-ttu-id="7dba0-134">**ConvertInterfaceNameToLuidW**</span><span class="sxs-lookup"><span data-stu-id="7dba0-134">**ConvertInterfaceNameToLuidW**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacenametoluidw)
-   [<span data-ttu-id="7dba0-135">**如果 \_ indextoname**</span><span class="sxs-lookup"><span data-stu-id="7dba0-135">**if\_indextoname**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-if_indextoname)
-   [<span data-ttu-id="7dba0-136">**如果 \_ nametoindex**</span><span class="sxs-lookup"><span data-stu-id="7dba0-136">**if\_nametoindex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-if_nametoindex)

## <a name="interface-management"></a><span data-ttu-id="7dba0-137">介面管理</span><span class="sxs-lookup"><span data-stu-id="7dba0-137">Interface management</span></span>

-   [<span data-ttu-id="7dba0-138">**GetFriendlyIfIndex**</span><span class="sxs-lookup"><span data-stu-id="7dba0-138">**GetFriendlyIfIndex**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex)
-   [<span data-ttu-id="7dba0-139">**GetIfEntry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-139">**GetIfEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getifentry)
-   [<span data-ttu-id="7dba0-140">**GetIfEntry2**</span><span class="sxs-lookup"><span data-stu-id="7dba0-140">**GetIfEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifentry2)
-   [<span data-ttu-id="7dba0-141">**GetIfEntry2Ex**</span><span class="sxs-lookup"><span data-stu-id="7dba0-141">**GetIfEntry2Ex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifentry2ex)
-   [<span data-ttu-id="7dba0-142">**GetIfStackTable**</span><span class="sxs-lookup"><span data-stu-id="7dba0-142">**GetIfStackTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifstacktable)
-   [<span data-ttu-id="7dba0-143">**GetIfTable**</span><span class="sxs-lookup"><span data-stu-id="7dba0-143">**GetIfTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getiftable)
-   [<span data-ttu-id="7dba0-144">**GetIfTable2**</span><span class="sxs-lookup"><span data-stu-id="7dba0-144">**GetIfTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getiftable2)
-   [<span data-ttu-id="7dba0-145">**GetIfTable2Ex**</span><span class="sxs-lookup"><span data-stu-id="7dba0-145">**GetIfTable2Ex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getiftable2ex)
-   [<span data-ttu-id="7dba0-146">**GetInterfaceInfo**</span><span class="sxs-lookup"><span data-stu-id="7dba0-146">**GetInterfaceInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo)
-   [<span data-ttu-id="7dba0-147">**GetInvertedIfStackTable**</span><span class="sxs-lookup"><span data-stu-id="7dba0-147">**GetInvertedIfStackTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getinvertedifstacktable)
-   [<span data-ttu-id="7dba0-148">**GetIpInterfaceEntry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-148">**GetIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipinterfaceentry)
-   [<span data-ttu-id="7dba0-149">**GetIpInterfaceTable**</span><span class="sxs-lookup"><span data-stu-id="7dba0-149">**GetIpInterfaceTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipinterfacetable)
-   [<span data-ttu-id="7dba0-150">**GetNumberOfInterfaces**</span><span class="sxs-lookup"><span data-stu-id="7dba0-150">**GetNumberOfInterfaces**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces)
-   [<span data-ttu-id="7dba0-151">**InitializeIpInterfaceEntry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-151">**InitializeIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeipinterfaceentry)
-   [<span data-ttu-id="7dba0-152">**SetIfEntry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-152">**SetIfEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setifentry)
-   [<span data-ttu-id="7dba0-153">**SetIpInterfaceEntry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-153">**SetIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipinterfaceentry)

## <a name="internet-protocol-ip-and-internet-control-message-protocol-icmp"></a><span data-ttu-id="7dba0-154">網際網路通訊協定 (IP) 和網際網路控制訊息通訊協定 (ICMP) </span><span class="sxs-lookup"><span data-stu-id="7dba0-154">Internet Protocol (IP) and Internet Control Message Protocol (ICMP)</span></span>

-   [<span data-ttu-id="7dba0-155">**GetIcmpStatistics**</span><span class="sxs-lookup"><span data-stu-id="7dba0-155">**GetIcmpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-geticmpstatistics)
-   [<span data-ttu-id="7dba0-156">**GetIpStatistics**</span><span class="sxs-lookup"><span data-stu-id="7dba0-156">**GetIpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipstatistics)
-   [<span data-ttu-id="7dba0-157">**Icmp6CreateFile**</span><span class="sxs-lookup"><span data-stu-id="7dba0-157">**Icmp6CreateFile**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6createfile)
-   [<span data-ttu-id="7dba0-158">**Icmp6ParseReplies**</span><span class="sxs-lookup"><span data-stu-id="7dba0-158">**Icmp6ParseReplies**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6parsereplies)
-   [<span data-ttu-id="7dba0-159">**Icmp6SendEcho2**</span><span class="sxs-lookup"><span data-stu-id="7dba0-159">**Icmp6SendEcho2**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6sendecho2)
-   [<span data-ttu-id="7dba0-160">**IcmpCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="7dba0-160">**IcmpCloseHandle**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpclosehandle)
-   [<span data-ttu-id="7dba0-161">**IcmpCreateFile**</span><span class="sxs-lookup"><span data-stu-id="7dba0-161">**IcmpCreateFile**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpcreatefile)
-   [<span data-ttu-id="7dba0-162">**IcmpParseReplies**</span><span class="sxs-lookup"><span data-stu-id="7dba0-162">**IcmpParseReplies**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpparsereplies)
-   [<span data-ttu-id="7dba0-163">**IcmpSendEcho**</span><span class="sxs-lookup"><span data-stu-id="7dba0-163">**IcmpSendEcho**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho)
-   [<span data-ttu-id="7dba0-164">**IcmpSendEcho2**</span><span class="sxs-lookup"><span data-stu-id="7dba0-164">**IcmpSendEcho2**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho2)
-   [<span data-ttu-id="7dba0-165">**IcmpSendEcho2Ex**</span><span class="sxs-lookup"><span data-stu-id="7dba0-165">**IcmpSendEcho2Ex**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho2ex)
-   [<span data-ttu-id="7dba0-166">**SetIpTTL**</span><span class="sxs-lookup"><span data-stu-id="7dba0-166">**SetIpTTL**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipttl)

## <a name="ip-address-management"></a><span data-ttu-id="7dba0-167">IP 位址管理</span><span class="sxs-lookup"><span data-stu-id="7dba0-167">IP address management</span></span>

-   [<span data-ttu-id="7dba0-168">**AddIPAddress**</span><span class="sxs-lookup"><span data-stu-id="7dba0-168">**AddIPAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-addipaddress)
-   [<span data-ttu-id="7dba0-169">**CreateAnycastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-169">**CreateAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createanycastipaddressentry)
-   [<span data-ttu-id="7dba0-170">**CreateUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-170">**CreateUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createunicastipaddressentry)
-   [<span data-ttu-id="7dba0-171">**DeleteIPAddress**</span><span class="sxs-lookup"><span data-stu-id="7dba0-171">**DeleteIPAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipaddress)
-   [<span data-ttu-id="7dba0-172">**DeleteAnycastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-172">**DeleteAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteanycastipaddressentry)
-   [<span data-ttu-id="7dba0-173">**DeleteUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-173">**DeleteUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteunicastipaddressentry)
-   [<span data-ttu-id="7dba0-174">**GetAnycastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-174">**GetAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getanycastipaddressentry)
-   [<span data-ttu-id="7dba0-175">**GetAnycastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="7dba0-175">**GetAnycastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getanycastipaddresstable)
-   [<span data-ttu-id="7dba0-176">**GetIpAddrTable**</span><span class="sxs-lookup"><span data-stu-id="7dba0-176">**GetIpAddrTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipaddrtable)
-   [<span data-ttu-id="7dba0-177">**GetMulticastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-177">**GetMulticastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getmulticastipaddressentry)
-   [<span data-ttu-id="7dba0-178">**GetMulticastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="7dba0-178">**GetMulticastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getmulticastipaddresstable)
-   [<span data-ttu-id="7dba0-179">**GetUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-179">**GetUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getunicastipaddressentry)
-   [<span data-ttu-id="7dba0-180">**GetUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="7dba0-180">**GetUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getunicastipaddresstable)
-   [<span data-ttu-id="7dba0-181">**InitializeUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-181">**InitializeUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeunicastipaddressentry)
-   [<span data-ttu-id="7dba0-182">**IpReleaseAddress**</span><span class="sxs-lookup"><span data-stu-id="7dba0-182">**IpReleaseAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress)
-   [<span data-ttu-id="7dba0-183">**IpRenewAddress**</span><span class="sxs-lookup"><span data-stu-id="7dba0-183">**IpRenewAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-iprenewaddress)
-   [<span data-ttu-id="7dba0-184">**NotifyStableUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="7dba0-184">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)
-   [<span data-ttu-id="7dba0-185">**SetUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-185">**SetUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setunicastipaddressentry)

## <a name="ip-address-string-conversion"></a><span data-ttu-id="7dba0-186">IP 位址字串轉換</span><span class="sxs-lookup"><span data-stu-id="7dba0-186">IP address string conversion</span></span>

-   [<span data-ttu-id="7dba0-187">**RtlIpv4AddressToString**</span><span class="sxs-lookup"><span data-stu-id="7dba0-187">**RtlIpv4AddressToString**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4addresstostringa)
-   [<span data-ttu-id="7dba0-188">**RtlIpv4AddressToStringEx**</span><span class="sxs-lookup"><span data-stu-id="7dba0-188">**RtlIpv4AddressToStringEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4addresstostringexw)
-   [<span data-ttu-id="7dba0-189">**RtlIpv4StringToAddress**</span><span class="sxs-lookup"><span data-stu-id="7dba0-189">**RtlIpv4StringToAddress**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa)
-   [<span data-ttu-id="7dba0-190">**RtlIpv4StringToAddressEx**</span><span class="sxs-lookup"><span data-stu-id="7dba0-190">**RtlIpv4StringToAddressEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw)
-   [<span data-ttu-id="7dba0-191">**RtlIpv6AddressToString**</span><span class="sxs-lookup"><span data-stu-id="7dba0-191">**RtlIpv6AddressToString**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringa)
-   [<span data-ttu-id="7dba0-192">**RtlIpv6AddressToStringEx**</span><span class="sxs-lookup"><span data-stu-id="7dba0-192">**RtlIpv6AddressToStringEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringexw)
-   [<span data-ttu-id="7dba0-193">**RtlIpv6StringToAddress**</span><span class="sxs-lookup"><span data-stu-id="7dba0-193">**RtlIpv6StringToAddress**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)
-   [<span data-ttu-id="7dba0-194">**RtlIpv6StringToAddressEx**</span><span class="sxs-lookup"><span data-stu-id="7dba0-194">**RtlIpv6StringToAddressEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw)

## <a name="ip-neighbor-address-management"></a><span data-ttu-id="7dba0-195">IP 鄰居位址管理</span><span class="sxs-lookup"><span data-stu-id="7dba0-195">IP neighbor address management</span></span>

-   [<span data-ttu-id="7dba0-196">**CreateIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="7dba0-196">**CreateIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createipnetentry2)
-   [<span data-ttu-id="7dba0-197">**DeleteIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="7dba0-197">**DeleteIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteipnetentry2)
-   [<span data-ttu-id="7dba0-198">**FlushIpNetTable2**</span><span class="sxs-lookup"><span data-stu-id="7dba0-198">**FlushIpNetTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-flushipnettable2)
-   [<span data-ttu-id="7dba0-199">**GetIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="7dba0-199">**GetIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipnetentry2)
-   [<span data-ttu-id="7dba0-200">**GetIpNetTable2**</span><span class="sxs-lookup"><span data-stu-id="7dba0-200">**GetIpNetTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipnettable2)
-   [<span data-ttu-id="7dba0-201">**ResolveIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="7dba0-201">**ResolveIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-resolveipnetentry2)
-   [<span data-ttu-id="7dba0-202">**ResolveNeighbor**</span><span class="sxs-lookup"><span data-stu-id="7dba0-202">**ResolveNeighbor**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-resolveneighbor)
-   [<span data-ttu-id="7dba0-203">**SetIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="7dba0-203">**SetIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipnetentry2)

## <a name="ip-path-management"></a><span data-ttu-id="7dba0-204">IP 路徑管理</span><span class="sxs-lookup"><span data-stu-id="7dba0-204">IP path management</span></span>

-   [<span data-ttu-id="7dba0-205">**FlushIpPathTable**</span><span class="sxs-lookup"><span data-stu-id="7dba0-205">**FlushIpPathTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-flushippathtable)
-   [<span data-ttu-id="7dba0-206">**GetIpPathEntry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-206">**GetIpPathEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getippathentry)
-   [<span data-ttu-id="7dba0-207">**GetIpPathTable**</span><span class="sxs-lookup"><span data-stu-id="7dba0-207">**GetIpPathTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getippathtable)

## <a name="ip-route-management"></a><span data-ttu-id="7dba0-208">IP 路由管理</span><span class="sxs-lookup"><span data-stu-id="7dba0-208">IP route management</span></span>

-   [<span data-ttu-id="7dba0-209">**CreateIpForwardEntry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-209">**CreateIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createipforwardentry)
-   [<span data-ttu-id="7dba0-210">**CreateIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="7dba0-210">**CreateIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createipforwardentry2)
-   [<span data-ttu-id="7dba0-211">**DeleteIpForwardEntry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-211">**DeleteIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)
-   [<span data-ttu-id="7dba0-212">**DeleteIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="7dba0-212">**DeleteIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteipforwardentry2)
-   [<span data-ttu-id="7dba0-213">**EnableRouter**</span><span class="sxs-lookup"><span data-stu-id="7dba0-213">**EnableRouter**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-enablerouter)
-   [<span data-ttu-id="7dba0-214">**GetBestInterface**</span><span class="sxs-lookup"><span data-stu-id="7dba0-214">**GetBestInterface**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestinterface)
-   [<span data-ttu-id="7dba0-215">**GetBestInterfaceEx**</span><span class="sxs-lookup"><span data-stu-id="7dba0-215">**GetBestInterfaceEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestinterfaceex)
-   [<span data-ttu-id="7dba0-216">**GetBestRoute**</span><span class="sxs-lookup"><span data-stu-id="7dba0-216">**GetBestRoute**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestroute)
-   [<span data-ttu-id="7dba0-217">**GetBestRoute2**</span><span class="sxs-lookup"><span data-stu-id="7dba0-217">**GetBestRoute2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getbestroute2)
-   [<span data-ttu-id="7dba0-218">**GetIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="7dba0-218">**GetIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipforwardentry2)
-   [<span data-ttu-id="7dba0-219">**GetIpForwardTable**</span><span class="sxs-lookup"><span data-stu-id="7dba0-219">**GetIpForwardTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipforwardtable)
-   [<span data-ttu-id="7dba0-220">**GetIpForwardTable2**</span><span class="sxs-lookup"><span data-stu-id="7dba0-220">**GetIpForwardTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipforwardtable2)
-   [<span data-ttu-id="7dba0-221">**GetRTTAndHopCount**</span><span class="sxs-lookup"><span data-stu-id="7dba0-221">**GetRTTAndHopCount**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getrttandhopcount)
-   [<span data-ttu-id="7dba0-222">**InitializeIpForwardEntry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-222">**InitializeIpForwardEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeipforwardentry)
-   [<span data-ttu-id="7dba0-223">**SetIpForwardEntry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-223">**SetIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipforwardentry)
-   [<span data-ttu-id="7dba0-224">**SetIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="7dba0-224">**SetIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipforwardentry2)
-   [<span data-ttu-id="7dba0-225">**SetIpStatistics**</span><span class="sxs-lookup"><span data-stu-id="7dba0-225">**SetIpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipstatistics)
-   [<span data-ttu-id="7dba0-226">**SetIpStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="7dba0-226">**SetIpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipstatisticsex)
-   [<span data-ttu-id="7dba0-227">**UnenableRouter**</span><span class="sxs-lookup"><span data-stu-id="7dba0-227">**UnenableRouter**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-unenablerouter)

## <a name="ip-table-memory-management"></a><span data-ttu-id="7dba0-228">IP 資料表記憶體管理</span><span class="sxs-lookup"><span data-stu-id="7dba0-228">IP table memory management</span></span>

-   [<span data-ttu-id="7dba0-229">**FreeMibTable**</span><span class="sxs-lookup"><span data-stu-id="7dba0-229">**FreeMibTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-freemibtable)

## <a name="ip-utility"></a><span data-ttu-id="7dba0-230">IP 公用程式</span><span class="sxs-lookup"><span data-stu-id="7dba0-230">IP utility</span></span>

-   [<span data-ttu-id="7dba0-231">**ConvertIpv4MaskToLength**</span><span class="sxs-lookup"><span data-stu-id="7dba0-231">**ConvertIpv4MaskToLength**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertipv4masktolength)
-   [<span data-ttu-id="7dba0-232">**ConvertLengthToIpv4Mask**</span><span class="sxs-lookup"><span data-stu-id="7dba0-232">**ConvertLengthToIpv4Mask**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertlengthtoipv4mask)
-   [<span data-ttu-id="7dba0-233">**CreateSortedAddressPairs**</span><span class="sxs-lookup"><span data-stu-id="7dba0-233">**CreateSortedAddressPairs**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createsortedaddresspairs)
-   [<span data-ttu-id="7dba0-234">**ParseNetworkString**</span><span class="sxs-lookup"><span data-stu-id="7dba0-234">**ParseNetworkString**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-parsenetworkstring)

## <a name="network-configuration"></a><span data-ttu-id="7dba0-235">網路組態</span><span class="sxs-lookup"><span data-stu-id="7dba0-235">Network configuration</span></span>

-   [<span data-ttu-id="7dba0-236">**GetNetworkParams**</span><span class="sxs-lookup"><span data-stu-id="7dba0-236">**GetNetworkParams**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getnetworkparams)

## <a name="notification"></a><span data-ttu-id="7dba0-237">通知</span><span class="sxs-lookup"><span data-stu-id="7dba0-237">Notification</span></span>

-   [<span data-ttu-id="7dba0-238">**CancelMibChangeNotify2**</span><span class="sxs-lookup"><span data-stu-id="7dba0-238">**CancelMibChangeNotify2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-cancelmibchangenotify2)
-   [<span data-ttu-id="7dba0-239">**NotifyAddrChange**</span><span class="sxs-lookup"><span data-stu-id="7dba0-239">**NotifyAddrChange**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-notifyaddrchange)
-   [<span data-ttu-id="7dba0-240">**NotifyIpInterfaceChange**</span><span class="sxs-lookup"><span data-stu-id="7dba0-240">**NotifyIpInterfaceChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyipinterfacechange)
-   [<span data-ttu-id="7dba0-241">**NotifyRouteChange**</span><span class="sxs-lookup"><span data-stu-id="7dba0-241">**NotifyRouteChange**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-notifyroutechange)
-   [<span data-ttu-id="7dba0-242">**NotifyRouteChange2**</span><span class="sxs-lookup"><span data-stu-id="7dba0-242">**NotifyRouteChange2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyroutechange2)
-   [<span data-ttu-id="7dba0-243">**NotifyUnicastIpAddressChange**</span><span class="sxs-lookup"><span data-stu-id="7dba0-243">**NotifyUnicastIpAddressChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyunicastipaddresschange)

## <a name="persistent-port-reservation"></a><span data-ttu-id="7dba0-244">持續性埠保留</span><span class="sxs-lookup"><span data-stu-id="7dba0-244">Persistent port reservation</span></span>

-   [<span data-ttu-id="7dba0-245">**CreatePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="7dba0-245">**CreatePersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)
-   [<span data-ttu-id="7dba0-246">**CreatePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="7dba0-246">**CreatePersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createpersistentudpportreservation)
-   [<span data-ttu-id="7dba0-247">**DeletePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="7dba0-247">**DeletePersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)
-   [<span data-ttu-id="7dba0-248">**DeletePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="7dba0-248">**DeletePersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)
-   [<span data-ttu-id="7dba0-249">**LookupPersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="7dba0-249">**LookupPersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)
-   [<span data-ttu-id="7dba0-250">**LookupPersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="7dba0-250">**LookupPersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

## <a name="security-health"></a><span data-ttu-id="7dba0-251">安全性健康狀態</span><span class="sxs-lookup"><span data-stu-id="7dba0-251">Security health</span></span>

-   <span data-ttu-id="7dba0-252">[**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7dba0-252">[**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))</span></span>
-   <span data-ttu-id="7dba0-253">[**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7dba0-253">[**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))</span></span>

<span data-ttu-id="7dba0-254">這些函式只會在 Windows Server 2003 上定義。</span><span class="sxs-lookup"><span data-stu-id="7dba0-254">These functions are defined only on Windows Server 2003.</span></span>

> [!Note]  
> <span data-ttu-id="7dba0-255">這些功能不適用於 Windows Vista，也不適用於 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="7dba0-255">These functions are not available on Windows Vista, nor on Windows Server 2008.</span></span>

## <a name="teredo-ipv6-client-management"></a><span data-ttu-id="7dba0-256">Teredo IPv6 用戶端管理</span><span class="sxs-lookup"><span data-stu-id="7dba0-256">Teredo IPv6 client management</span></span>

-   [<span data-ttu-id="7dba0-257">**GetTeredoPort**</span><span class="sxs-lookup"><span data-stu-id="7dba0-257">**GetTeredoPort**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getteredoport)
-   [<span data-ttu-id="7dba0-258">**NotifyTeredoPortChange**</span><span class="sxs-lookup"><span data-stu-id="7dba0-258">**NotifyTeredoPortChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyteredoportchange)
-   [<span data-ttu-id="7dba0-259">**NotifyStableUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="7dba0-259">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)

## <a name="transmission-control-protocol-tcp-and-user-datagram-protocol-udp"></a><span data-ttu-id="7dba0-260">傳輸控制通訊協定 (TCP) 和使用者資料包協定 (UDP) </span><span class="sxs-lookup"><span data-stu-id="7dba0-260">Transmission Control Protocol (TCP) and User Datagram Protocol (UDP)</span></span>

-   [<span data-ttu-id="7dba0-261">**GetExtendedTcpTable**</span><span class="sxs-lookup"><span data-stu-id="7dba0-261">**GetExtendedTcpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getextendedtcptable)
-   [<span data-ttu-id="7dba0-262">**GetExtendedUdpTable**</span><span class="sxs-lookup"><span data-stu-id="7dba0-262">**GetExtendedUdpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getextendedudptable)
-   [<span data-ttu-id="7dba0-263">**GetOwnerModuleFromTcp6Entry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-263">**GetOwnerModuleFromTcp6Entry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcp6entry)
-   [<span data-ttu-id="7dba0-264">**GetOwnerModuleFromTcpEntry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-264">**GetOwnerModuleFromTcpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcpentry)
-   [<span data-ttu-id="7dba0-265">**GetOwnerModuleFromUdp6Entry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-265">**GetOwnerModuleFromUdp6Entry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromudp6entry)
-   [<span data-ttu-id="7dba0-266">**GetOwnerModuleFromUdpEntry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-266">**GetOwnerModuleFromUdpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromudpentry)
-   [<span data-ttu-id="7dba0-267">**GetPerTcp6ConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="7dba0-267">**GetPerTcp6ConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getpertcp6connectionestats)
-   [<span data-ttu-id="7dba0-268">**GetPerTcpConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="7dba0-268">**GetPerTcpConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getpertcpconnectionestats)
-   [<span data-ttu-id="7dba0-269">**GetTcpStatistics**</span><span class="sxs-lookup"><span data-stu-id="7dba0-269">**GetTcpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatistics)
-   [<span data-ttu-id="7dba0-270">**GetTcpStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="7dba0-270">**GetTcpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatisticsex)
-   [<span data-ttu-id="7dba0-271">**GetTcpStatisticsEx2**</span><span class="sxs-lookup"><span data-stu-id="7dba0-271">**GetTcpStatisticsEx2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatisticsex2)
-   [<span data-ttu-id="7dba0-272">**GetTcp6Table**</span><span class="sxs-lookup"><span data-stu-id="7dba0-272">**GetTcp6Table**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcp6table)
-   [<span data-ttu-id="7dba0-273">**GetTcp6Table2**</span><span class="sxs-lookup"><span data-stu-id="7dba0-273">**GetTcp6Table2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcp6table2)
-   [<span data-ttu-id="7dba0-274">**GetTcpTable**</span><span class="sxs-lookup"><span data-stu-id="7dba0-274">**GetTcpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcptable)
-   [<span data-ttu-id="7dba0-275">**GetTcpTable2**</span><span class="sxs-lookup"><span data-stu-id="7dba0-275">**GetTcpTable2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcptable2)
-   [<span data-ttu-id="7dba0-276">**SetPerTcp6ConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="7dba0-276">**SetPerTcp6ConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setpertcp6connectionestats)
-   [<span data-ttu-id="7dba0-277">**SetPerTcpConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="7dba0-277">**SetPerTcpConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setpertcpconnectionestats)
-   [<span data-ttu-id="7dba0-278">**SetTcpEntry**</span><span class="sxs-lookup"><span data-stu-id="7dba0-278">**SetTcpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-settcpentry)
-   [<span data-ttu-id="7dba0-279">**GetUdp6Table**</span><span class="sxs-lookup"><span data-stu-id="7dba0-279">**GetUdp6Table**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudp6table)
-   [<span data-ttu-id="7dba0-280">**GetUdpStatistics**</span><span class="sxs-lookup"><span data-stu-id="7dba0-280">**GetUdpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatistics)
-   [<span data-ttu-id="7dba0-281">**GetUdpStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="7dba0-281">**GetUdpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatisticsex)
-   [<span data-ttu-id="7dba0-282">**GetUdpStatisticsEx2**</span><span class="sxs-lookup"><span data-stu-id="7dba0-282">**GetUdpStatisticsEx2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatisticsex2)
-   [<span data-ttu-id="7dba0-283">**GetUdpTable**</span><span class="sxs-lookup"><span data-stu-id="7dba0-283">**GetUdpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudptable)

## <a name="deprecated-apis"></a><span data-ttu-id="7dba0-284">已被取代的 API</span><span class="sxs-lookup"><span data-stu-id="7dba0-284">Deprecated APIs</span></span>

> [!Note]  
> <span data-ttu-id="7dba0-285">這些函式已被取代，Microsoft 並不支援這些功能。</span><span class="sxs-lookup"><span data-stu-id="7dba0-285">These functions are deprecated, and are not supported by Microsoft.</span></span>

-   [<span data-ttu-id="7dba0-286">**AllocateAndGetTcpExTableFromStack**</span><span class="sxs-lookup"><span data-stu-id="7dba0-286">**AllocateAndGetTcpExTableFromStack**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-allocateandgettcpextablefromstack)
-   [<span data-ttu-id="7dba0-287">**AllocateAndGetUdpExTableFromStack**</span><span class="sxs-lookup"><span data-stu-id="7dba0-287">**AllocateAndGetUdpExTableFromStack**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-allocateandgetudpextablefromstack)
