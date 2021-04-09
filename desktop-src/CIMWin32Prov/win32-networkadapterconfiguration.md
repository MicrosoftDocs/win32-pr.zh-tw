---
description: 代表網路介面卡的屬性和行為。 此類別包含額外的屬性和方法，可支援與網路介面卡無關的 TCP/IP 通訊協定管理。
ms.assetid: 690b46ed-a065-4973-b044-0df4e81e41a1
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration
- Win32_NetworkAdapterConfiguration.Caption
- Win32_NetworkAdapterConfiguration.Description
- Win32_NetworkAdapterConfiguration.SettingID
- Win32_NetworkAdapterConfiguration.ArpAlwaysSourceRoute
- Win32_NetworkAdapterConfiguration.ArpUseEtherSNAP
- Win32_NetworkAdapterConfiguration.DatabasePath
- Win32_NetworkAdapterConfiguration.DeadGWDetectEnabled
- Win32_NetworkAdapterConfiguration.DefaultIPGateway
- Win32_NetworkAdapterConfiguration.DefaultTOS
- Win32_NetworkAdapterConfiguration.DefaultTTL
- Win32_NetworkAdapterConfiguration.DHCPEnabled
- Win32_NetworkAdapterConfiguration.DHCPLeaseExpires
- Win32_NetworkAdapterConfiguration.DHCPLeaseObtained
- Win32_NetworkAdapterConfiguration.DHCPServer
- Win32_NetworkAdapterConfiguration.DNSDomain
- Win32_NetworkAdapterConfiguration.DNSDomainSuffixSearchOrder
- Win32_NetworkAdapterConfiguration.DNSEnabledForWINSResolution
- Win32_NetworkAdapterConfiguration.DNSHostName
- Win32_NetworkAdapterConfiguration.DNSServerSearchOrder
- Win32_NetworkAdapterConfiguration.DomainDNSRegistrationEnabled
- Win32_NetworkAdapterConfiguration.ForwardBufferMemory
- Win32_NetworkAdapterConfiguration.FullDNSRegistrationEnabled
- Win32_NetworkAdapterConfiguration.GatewayCostMetric
- Win32_NetworkAdapterConfiguration.IGMPLevel
- Win32_NetworkAdapterConfiguration.Index
- Win32_NetworkAdapterConfiguration.InterfaceIndex
- Win32_NetworkAdapterConfiguration.IPAddress
- Win32_NetworkAdapterConfiguration.IPConnectionMetric
- Win32_NetworkAdapterConfiguration.IPEnabled
- Win32_NetworkAdapterConfiguration.IPFilterSecurityEnabled
- Win32_NetworkAdapterConfiguration.IPPortSecurityEnabled
- Win32_NetworkAdapterConfiguration.IPSecPermitIPProtocols
- Win32_NetworkAdapterConfiguration.IPSecPermitTCPPorts
- Win32_NetworkAdapterConfiguration.IPSecPermitUDPPorts
- Win32_NetworkAdapterConfiguration.IPSubnet
- Win32_NetworkAdapterConfiguration.IPUseZeroBroadcast
- Win32_NetworkAdapterConfiguration.IPXAddress
- Win32_NetworkAdapterConfiguration.IPXEnabled
- Win32_NetworkAdapterConfiguration.IPXFrameType
- Win32_NetworkAdapterConfiguration.IPXMediaType
- Win32_NetworkAdapterConfiguration.IPXNetworkNumber
- Win32_NetworkAdapterConfiguration.IPXVirtualNetNumber
- Win32_NetworkAdapterConfiguration.KeepAliveInterval
- Win32_NetworkAdapterConfiguration.KeepAliveTime
- Win32_NetworkAdapterConfiguration.MACAddress
- Win32_NetworkAdapterConfiguration.MTU
- Win32_NetworkAdapterConfiguration.NumForwardPackets
- Win32_NetworkAdapterConfiguration.PMTUBHDetectEnabled
- Win32_NetworkAdapterConfiguration.PMTUDiscoveryEnabled
- Win32_NetworkAdapterConfiguration.ServiceName
- Win32_NetworkAdapterConfiguration.TcpipNetbiosOptions
- Win32_NetworkAdapterConfiguration.TcpMaxConnectRetransmissions
- Win32_NetworkAdapterConfiguration.TcpMaxDataRetransmissions
- Win32_NetworkAdapterConfiguration.TcpNumConnections
- Win32_NetworkAdapterConfiguration.TcpUseRFC1122UrgentPointer
- Win32_NetworkAdapterConfiguration.TcpWindowSize
- Win32_NetworkAdapterConfiguration.WINSEnableLMHostsLookup
- Win32_NetworkAdapterConfiguration.WINSHostLookupFile
- Win32_NetworkAdapterConfiguration.WINSPrimaryServer
- Win32_NetworkAdapterConfiguration.WINSScopeID
- Win32_NetworkAdapterConfiguration.WINSSecondaryServer
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2bccbe7fc44e75c2448d2eda800fe3c14cd13a9b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111353"
---
# <a name="win32_networkadapterconfiguration-class"></a><span data-ttu-id="334d4-104">Win32 \_ >networkadapterconfiguration 類別</span><span class="sxs-lookup"><span data-stu-id="334d4-104">Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="334d4-105">**Win32 \_ >networkadapterconfiguration** [WMI 類別](../wmisdk/retrieving-a-class.md)代表網路介面卡的屬性和行為。</span><span class="sxs-lookup"><span data-stu-id="334d4-105">The **Win32\_NetworkAdapterConfiguration** [WMI class](../wmisdk/retrieving-a-class.md)represents the attributes and behaviors of a network adapter.</span></span> <span data-ttu-id="334d4-106">此類別包含額外的屬性和方法，可支援與網路介面卡無關的 TCP/IP 通訊協定管理。</span><span class="sxs-lookup"><span data-stu-id="334d4-106">This class includes extra properties and methods that support the management of the TCP/IP protocol that are independent from the network adapter.</span></span>

<span data-ttu-id="334d4-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="334d4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="334d4-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="334d4-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="334d4-109">語法</span><span class="sxs-lookup"><span data-stu-id="334d4-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C515-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapterConfiguration : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  boolean  ArpAlwaysSourceRoute;
  boolean  ArpUseEtherSNAP;
  string   DatabasePath;
  boolean  DeadGWDetectEnabled;
  string   DefaultIPGateway[];
  uint8    DefaultTOS;
  uint8    DefaultTTL;
  boolean  DHCPEnabled;
  datetime DHCPLeaseExpires;
  datetime DHCPLeaseObtained;
  string   DHCPServer;
  string   DNSDomain;
  string   DNSDomainSuffixSearchOrder[];
  boolean  DNSEnabledForWINSResolution;
  string   DNSHostName;
  string   DNSServerSearchOrder[];
  boolean  DomainDNSRegistrationEnabled;
  uint32   ForwardBufferMemory;
  boolean  FullDNSRegistrationEnabled;
  uint16   GatewayCostMetric[];
  uint8    IGMPLevel;
  uint32   Index;
  uint32   InterfaceIndex;
  string   IPAddress[];
  uint32   IPConnectionMetric;
  boolean  IPEnabled;
  boolean  IPFilterSecurityEnabled;
  boolean  IPPortSecurityEnabled;
  string   IPSecPermitIPProtocols[];
  string   IPSecPermitTCPPorts[];
  string   IPSecPermitUDPPorts[];
  string   IPSubnet[];
  boolean  IPUseZeroBroadcast;
  string   IPXAddress;
  boolean  IPXEnabled;
  uint32   IPXFrameType[];
  uint32   IPXMediaType;
  string   IPXNetworkNumber[];
  string   IPXVirtualNetNumber;
  uint32   KeepAliveInterval;
  uint32   KeepAliveTime;
  string   MACAddress;
  uint32   MTU;
  uint32   NumForwardPackets;
  boolean  PMTUBHDetectEnabled;
  boolean  PMTUDiscoveryEnabled;
  string   ServiceName;
  uint32   TcpipNetbiosOptions;
  uint32   TcpMaxConnectRetransmissions;
  uint32   TcpMaxDataRetransmissions;
  uint32   TcpNumConnections;
  boolean  TcpUseRFC1122UrgentPointer;
  uint16   TcpWindowSize;
  boolean  WINSEnableLMHostsLookup;
  string   WINSHostLookupFile;
  string   WINSPrimaryServer;
  string   WINSScopeID;
  string   WINSSecondaryServer;
};
```

## <a name="members"></a><span data-ttu-id="334d4-110">成員</span><span class="sxs-lookup"><span data-stu-id="334d4-110">Members</span></span>

<span data-ttu-id="334d4-111">**Win32 \_ >networkadapterconfiguration** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="334d4-111">The **Win32\_NetworkAdapterConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="334d4-112">方法</span><span class="sxs-lookup"><span data-stu-id="334d4-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="334d4-113">屬性</span><span class="sxs-lookup"><span data-stu-id="334d4-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="334d4-114">方法</span><span class="sxs-lookup"><span data-stu-id="334d4-114">Methods</span></span>

<span data-ttu-id="334d4-115">**Win32 \_ >networkadapterconfiguration** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="334d4-115">The **Win32\_NetworkAdapterConfiguration** class has these methods.</span></span>



| <span data-ttu-id="334d4-116">方法</span><span class="sxs-lookup"><span data-stu-id="334d4-116">Method</span></span>                                                                                                                       | <span data-ttu-id="334d4-117">描述</span><span class="sxs-lookup"><span data-stu-id="334d4-117">Description</span></span>                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="334d4-118">**DisableIPSec**</span><span class="sxs-lookup"><span data-stu-id="334d4-118">**DisableIPSec**</span></span>](disableipsec-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="334d4-119">停用此啟用 TCP/IP 的網路介面卡上的 IPsec。</span><span class="sxs-lookup"><span data-stu-id="334d4-119">Disables IPsec on this TCP/IP-enabled network adapter.</span></span><br/>                                                                                     |
| [<span data-ttu-id="334d4-120">**EnableDHCP**</span><span class="sxs-lookup"><span data-stu-id="334d4-120">**EnableDHCP**</span></span>](enabledhcp-method-in-class-win32-networkadapterconfiguration.md)                                           | <span data-ttu-id="334d4-121">使用此網路介面卡啟用動態主機設定通訊協定 (DHCP) 的服務。</span><span class="sxs-lookup"><span data-stu-id="334d4-121">Enables the Dynamic Host Configuration Protocol (DHCP) for service with this network adapter.</span></span><br/>                                              |
| [<span data-ttu-id="334d4-122">**EnableDNS**</span><span class="sxs-lookup"><span data-stu-id="334d4-122">**EnableDNS**</span></span>](enabledns-method-in-class-win32-networkadapterconfiguration.md)                                             | <span data-ttu-id="334d4-123">針對此 TCP/IP 系結網路介面卡上的服務，啟用網域名稱系統 (DNS) 。</span><span class="sxs-lookup"><span data-stu-id="334d4-123">Enables the Domain Name System (DNS) for service on this TCP/IP-bound network adapter.</span></span><br/>                                                     |
| [<span data-ttu-id="334d4-124">**EnableIPFilterSec**</span><span class="sxs-lookup"><span data-stu-id="334d4-124">**EnableIPFilterSec**</span></span>](enableipfiltersec-method-in-class-win32-networkadapterconfiguration.md)                             | <span data-ttu-id="334d4-125">在所有 IP 系結的網路介面卡上全域啟用 IPsec。</span><span class="sxs-lookup"><span data-stu-id="334d4-125">Enables IPsec globally across all IP-bound network adapters.</span></span><br/>                                                                               |
| [<span data-ttu-id="334d4-126">**EnableIPSec**</span><span class="sxs-lookup"><span data-stu-id="334d4-126">**EnableIPSec**</span></span>](enableipsec-method-in-class-win32-networkadapterconfiguration.md)                                         | <span data-ttu-id="334d4-127">在啟用此特定 TCP/IP 的網路介面卡上啟用 IPsec。</span><span class="sxs-lookup"><span data-stu-id="334d4-127">Enables IPsec on this specific TCP/IP-enabled network adapter.</span></span><br/>                                                                             |
| [<span data-ttu-id="334d4-128">**EnableStatic**</span><span class="sxs-lookup"><span data-stu-id="334d4-128">**EnableStatic**</span></span>](enablestatic-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="334d4-129">啟用目標網路介面卡的靜態 TCP/IP 定址。</span><span class="sxs-lookup"><span data-stu-id="334d4-129">Enables static TCP/IP addressing for the target network adapter.</span></span><br/>                                                                           |
| [<span data-ttu-id="334d4-130">**>enablewins**</span><span class="sxs-lookup"><span data-stu-id="334d4-130">**EnableWINS**</span></span>](enablewins-method-in-class-win32-networkadapterconfiguration.md)                                           | <span data-ttu-id="334d4-131">啟用 TCP/IP 專屬的 WINS 設定，但與網路介面卡無關。</span><span class="sxs-lookup"><span data-stu-id="334d4-131">Enables WINS settings specific to TCP/IP, but independent of the network adapter.</span></span><br/>                                                          |
| [<span data-ttu-id="334d4-132">**ReleaseDHCPLease**</span><span class="sxs-lookup"><span data-stu-id="334d4-132">**ReleaseDHCPLease**</span></span>](releasedhcplease-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="334d4-133">釋放系結至已啟用 DHCP 之特定網路介面卡的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="334d4-133">Releases the IP address bound to a specific DHCP-enabled network adapter.</span></span><br/>                                                                  |
| [<span data-ttu-id="334d4-134">**>releasedhcpleaseall**</span><span class="sxs-lookup"><span data-stu-id="334d4-134">**ReleaseDHCPLeaseAll**</span></span>](releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                         | <span data-ttu-id="334d4-135">釋放系結至所有啟用 DHCP 之網路介面卡的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="334d4-135">Releases the IP addresses bound to all DHCP-enabled network adapters.</span></span><br/>                                                                      |
| [<span data-ttu-id="334d4-136">**RenewDHCPLease**</span><span class="sxs-lookup"><span data-stu-id="334d4-136">**RenewDHCPLease**</span></span>](renewdhcplease-method-in-class-win32-networkadapterconfiguration.md)                                   | <span data-ttu-id="334d4-137">更新已啟用 DHCP 的特定網路介面卡上的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="334d4-137">Renews the IP address on specific DHCP-enabled network adapters.</span></span><br/>                                                                           |
| [<span data-ttu-id="334d4-138">**RenewDHCPLeaseAll**</span><span class="sxs-lookup"><span data-stu-id="334d4-138">**RenewDHCPLeaseAll**</span></span>](renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                             | <span data-ttu-id="334d4-139">在所有已啟用 DHCP 的網路介面卡上，更新 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="334d4-139">Renews the IP addresses on all DHCP-enabled network adapters.</span></span><br/>                                                                              |
| [<span data-ttu-id="334d4-140">**SetArpAlwaysSourceRoute**</span><span class="sxs-lookup"><span data-stu-id="334d4-140">**SetArpAlwaysSourceRoute**</span></span>](setarpalwayssourceroute-method-in-class-win32-networkadapterconfiguration.md)                 | <span data-ttu-id="334d4-141">依 TCP/IP 設定 ARP 查詢的傳輸。</span><span class="sxs-lookup"><span data-stu-id="334d4-141">Sets the transmission of ARP queries by the TCP/IP.</span></span><br/>                                                                                        |
| [<span data-ttu-id="334d4-142">**SetArpUseEtherSNAP**</span><span class="sxs-lookup"><span data-stu-id="334d4-142">**SetArpUseEtherSNAP**</span></span>](setarpuseethersnap-method-in-class-win32-networkadapterconfiguration.md)                           | <span data-ttu-id="334d4-143">讓乙太網路封包使用802.3 貼齊編碼。</span><span class="sxs-lookup"><span data-stu-id="334d4-143">Enables Ethernet packets to use 802.3 SNAP encoding.</span></span><br/>                                                                                       |
| [<span data-ttu-id="334d4-144">**SetDatabasePath**</span><span class="sxs-lookup"><span data-stu-id="334d4-144">**SetDatabasePath**</span></span>](setdatabasepath-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="334d4-145">設定)  (主機、LMHOSTS、網路和通訊協定之標準網際網路資料庫檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="334d4-145">Sets the path to the standard Internet database files (HOSTS, LMHOSTS, NETWORKS, and PROTOCOLS).</span></span><br/>                                           |
| [<span data-ttu-id="334d4-146">**SetDeadGWDetect**</span><span class="sxs-lookup"><span data-stu-id="334d4-146">**SetDeadGWDetect**</span></span>](setdeadgwdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="334d4-147">啟用死閘道偵測。</span><span class="sxs-lookup"><span data-stu-id="334d4-147">Enables dead gateway detection.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="334d4-148">**SetDefaultTOS**</span><span class="sxs-lookup"><span data-stu-id="334d4-148">**SetDefaultTOS**</span></span>](setdefaulttos-method-in-class-win32-networkadapterconfiguration.md)                                     | <span data-ttu-id="334d4-149">已過時。</span><span class="sxs-lookup"><span data-stu-id="334d4-149">Obsolete.</span></span> <span data-ttu-id="334d4-150">這個方法會在連出 IP 封包的標頭中，設定服務 (TOS) 值的預設類型。</span><span class="sxs-lookup"><span data-stu-id="334d4-150">This method sets the default Type of Service (TOS) value in the header of outgoing IP packets.</span></span><br/>                                   |
| [<span data-ttu-id="334d4-151">**SetDefaultTTL**</span><span class="sxs-lookup"><span data-stu-id="334d4-151">**SetDefaultTTL**</span></span>](setdefaultttl-method-in-class-win32-networkadapterconfiguration.md)                                     | <span data-ttu-id="334d4-152">設定傳出 IP 封包標頭中 (TTL) 值的預設存留時間。</span><span class="sxs-lookup"><span data-stu-id="334d4-152">Sets the default Time to Live (TTL) value in the header of outgoing IP packets.</span></span><br/>                                                            |
| [<span data-ttu-id="334d4-153">**SetDNSDomain**</span><span class="sxs-lookup"><span data-stu-id="334d4-153">**SetDNSDomain**</span></span>](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="334d4-154">設定 DNS 網域。</span><span class="sxs-lookup"><span data-stu-id="334d4-154">Sets the DNS domain.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="334d4-155">**SetDNSServerSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="334d4-155">**SetDNSServerSearchOrder**</span></span>](setdnsserversearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | <span data-ttu-id="334d4-156">將伺服器搜尋順序設定為元素陣列。</span><span class="sxs-lookup"><span data-stu-id="334d4-156">Sets the server search order as an array of elements.</span></span><br/>                                                                                      |
| [<span data-ttu-id="334d4-157">**SetDNSSuffixSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="334d4-157">**SetDNSSuffixSearchOrder**</span></span>](setdnssuffixsearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | <span data-ttu-id="334d4-158">將尾碼搜尋順序設定為元素陣列。</span><span class="sxs-lookup"><span data-stu-id="334d4-158">Sets the suffix search order as an array of elements.</span></span><br/>                                                                                      |
| [<span data-ttu-id="334d4-159">**SetDynamicDNSRegistration**</span><span class="sxs-lookup"><span data-stu-id="334d4-159">**SetDynamicDNSRegistration**</span></span>](setdynamicdnsregistration-method-in-class-win32-networkadapterconfiguration.md)             | <span data-ttu-id="334d4-160">指出此 IP 系結介面卡的 IP 位址動態 DNS 註冊。</span><span class="sxs-lookup"><span data-stu-id="334d4-160">Indicates dynamic DNS registration of IP addresses for this IP-bound adapter.</span></span><br/>                                                              |
| [<span data-ttu-id="334d4-161">**SetForwardBufferMemory**</span><span class="sxs-lookup"><span data-stu-id="334d4-161">**SetForwardBufferMemory**</span></span>](setforwardbuffermemory-method-in-class-win32-networkadapterconfiguration.md)                   | <span data-ttu-id="334d4-162">指定要將封包資料儲存在路由器封包佇列中的記憶體 IP 分配數量。</span><span class="sxs-lookup"><span data-stu-id="334d4-162">Specifies how much memory IP allocates to store packet data in the router packet queue.</span></span><br/>                                                    |
| [<span data-ttu-id="334d4-163">**SetGateways**</span><span class="sxs-lookup"><span data-stu-id="334d4-163">**SetGateways**</span></span>](setgateways-method-in-class-win32-networkadapterconfiguration.md)                                         | <span data-ttu-id="334d4-164">指定閘道清單，以路由傳送至與此介面卡所連接的子網不同的子網的封包。</span><span class="sxs-lookup"><span data-stu-id="334d4-164">Specifies a list of gateways for routing packets destined for a different subnet than the one this adapter is connected to.</span></span><br/>                |
| [<span data-ttu-id="334d4-165">**SetIGMPLevel**</span><span class="sxs-lookup"><span data-stu-id="334d4-165">**SetIGMPLevel**</span></span>](setigmplevel-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="334d4-166">設定系統支援 IP 多播並參與網際網路群組管理通訊協定的範圍。</span><span class="sxs-lookup"><span data-stu-id="334d4-166">Sets the extent to which the system supports IP multicasting and participates in the Internet Group Management Protocol.</span></span><br/>                   |
| [<span data-ttu-id="334d4-167">**SetIPConnectionMetric**</span><span class="sxs-lookup"><span data-stu-id="334d4-167">**SetIPConnectionMetric**</span></span>](setipconnectionmetric-method-in-class-win32-networkadapterconfiguration.md)                     | <span data-ttu-id="334d4-168">設定與此 IP 系結介面卡相關聯的路由度量。</span><span class="sxs-lookup"><span data-stu-id="334d4-168">Sets the routing metric associated with this IP-bound adapter.</span></span><br/>                                                                             |
| [<span data-ttu-id="334d4-169">**SetIPUseZeroBroadcast**</span><span class="sxs-lookup"><span data-stu-id="334d4-169">**SetIPUseZeroBroadcast**</span></span>](setipusezerobroadcast-method-in-class-win32-networkadapterconfiguration.md)                     | <span data-ttu-id="334d4-170">設定 IP 零廣播使用方式。</span><span class="sxs-lookup"><span data-stu-id="334d4-170">Sets IP zero broadcast usage.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="334d4-171">**SetIPXFrameTypeNetworkPairs**</span><span class="sxs-lookup"><span data-stu-id="334d4-171">**SetIPXFrameTypeNetworkPairs**</span></span>](win32-networkadapterconfiguration-setipxframetypenetworkpairs.md)                         | <span data-ttu-id="334d4-172">為此網路介面卡) 網路編號/框架組，設定網路封包交換 (。</span><span class="sxs-lookup"><span data-stu-id="334d4-172">Sets Internetworking Packet Exchange (IPX) network number/frame pairs for this network adapter.</span></span><br/>                                            |
| [<span data-ttu-id="334d4-173">**SetIPXVirtualNetworkNumber**</span><span class="sxs-lookup"><span data-stu-id="334d4-173">**SetIPXVirtualNetworkNumber**</span></span>](win32-networkadapterconfiguration-setipxvirtualnetworknumber.md)                           | <span data-ttu-id="334d4-174">設定目的電腦系統上的封包交換 (IPX) 虛擬網路編號。</span><span class="sxs-lookup"><span data-stu-id="334d4-174">Sets the Internetworking Packet Exchange (IPX) virtual network number on the target computer system.</span></span><br/>                                       |
| [<span data-ttu-id="334d4-175">**SetKeepAliveInterval**</span><span class="sxs-lookup"><span data-stu-id="334d4-175">**SetKeepAliveInterval**</span></span>](setkeepaliveinterval-method-in-class-win32-networkadapterconfiguration.md)                       | <span data-ttu-id="334d4-176">設定分隔保持運作的間隔，直到收到回應為止。</span><span class="sxs-lookup"><span data-stu-id="334d4-176">Sets the interval separating Keep Alive Retransmissions until a response is received.</span></span><br/>                                                      |
| [<span data-ttu-id="334d4-177">**SetKeepAliveTime**</span><span class="sxs-lookup"><span data-stu-id="334d4-177">**SetKeepAliveTime**</span></span>](setkeepalivetime-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="334d4-178">藉由傳送 Keep-alive 封包，設定 TCP 嘗試驗證閒置連線是否仍可供使用的頻率。</span><span class="sxs-lookup"><span data-stu-id="334d4-178">Sets how often TCP attempts to verify that an idle connection is still available by sending a Keep Alive packet.</span></span><br/>                           |
| [<span data-ttu-id="334d4-179">**SetMTU**</span><span class="sxs-lookup"><span data-stu-id="334d4-179">**SetMTU**</span></span>](setmtu-method-in-class-win32-networkadapterconfiguration.md)                                                   | <span data-ttu-id="334d4-180">設定網路介面 (MTU) 的預設最大傳輸單位。</span><span class="sxs-lookup"><span data-stu-id="334d4-180">Sets the default Maximum Transmission Unit (MTU) for a network interface.</span></span><br/> <span data-ttu-id="334d4-181">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="334d4-181">This method is not supported.</span></span><br/>                         |
| [<span data-ttu-id="334d4-182">**SetNumForwardPackets**</span><span class="sxs-lookup"><span data-stu-id="334d4-182">**SetNumForwardPackets**</span></span>](setnumforwardpackets-method-in-class-win32-networkadapterconfiguration.md)                       | <span data-ttu-id="334d4-183">設定為路由器封包佇列配置的 IP 封包標頭數目。</span><span class="sxs-lookup"><span data-stu-id="334d4-183">Sets the number of IP packet headers allocated for the router packet queue.</span></span><br/>                                                                |
| [<span data-ttu-id="334d4-184">**SetPMTUBHDetect**</span><span class="sxs-lookup"><span data-stu-id="334d4-184">**SetPMTUBHDetect**</span></span>](setpmtubhdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="334d4-185">啟用對黑洞路由器的偵測。</span><span class="sxs-lookup"><span data-stu-id="334d4-185">Enables detection of Black Hole routers.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="334d4-186">**SetPMTUDiscovery**</span><span class="sxs-lookup"><span data-stu-id="334d4-186">**SetPMTUDiscovery**</span></span>](setpmtudiscovery-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="334d4-187">啟用 (MTU) 探索的最大傳輸單位。</span><span class="sxs-lookup"><span data-stu-id="334d4-187">Enables Maximum Transmission Unit (MTU) discovery.</span></span><br/>                                                                                         |
| [<span data-ttu-id="334d4-188">**SetTcpipNetbios**</span><span class="sxs-lookup"><span data-stu-id="334d4-188">**SetTcpipNetbios**</span></span>](settcpipnetbios-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="334d4-189">設定 NetBIOS over TCP/IP 的預設運算。</span><span class="sxs-lookup"><span data-stu-id="334d4-189">Sets the default operation of NetBIOS over TCP/IP.</span></span><br/>                                                                                         |
| [<span data-ttu-id="334d4-190">**SetTcpMaxConnectRetransmissions**</span><span class="sxs-lookup"><span data-stu-id="334d4-190">**SetTcpMaxConnectRetransmissions**</span></span>](settcpmaxconnectretransmissions-method-in-class-win32-networkadapterconfiguration.md) | <span data-ttu-id="334d4-191">設定在中止之前 TCP 將會重新傳輸連接要求的次數。</span><span class="sxs-lookup"><span data-stu-id="334d4-191">Sets the number of attempts TCP will retransmit a connect request before aborting.</span></span><br/>                                                         |
| [<span data-ttu-id="334d4-192">**SetTcpMaxDataRetransmissions**</span><span class="sxs-lookup"><span data-stu-id="334d4-192">**SetTcpMaxDataRetransmissions**</span></span>](settcpmaxdataretransmissions-method-in-class-win32-networkadapterconfiguration.md)       | <span data-ttu-id="334d4-193">設定在中止連接之前，TCP 會重新傳輸個別資料區段的次數。</span><span class="sxs-lookup"><span data-stu-id="334d4-193">Sets the number of times TCP will retransmit an individual data segment before aborting the connection.</span></span><br/>                                    |
| [<span data-ttu-id="334d4-194">**SetTcpNumConnections**</span><span class="sxs-lookup"><span data-stu-id="334d4-194">**SetTcpNumConnections**</span></span>](settcpnumconnections-method-in-class-win32-networkadapterconfiguration.md)                       | <span data-ttu-id="334d4-195">設定 TCP 可能同時開啟的最大連接數目。</span><span class="sxs-lookup"><span data-stu-id="334d4-195">Sets the maximum number of connections that TCP may have open simultaneously.</span></span><br/>                                                              |
| [<span data-ttu-id="334d4-196">**SetTcpUseRFC1122UrgentPointer**</span><span class="sxs-lookup"><span data-stu-id="334d4-196">**SetTcpUseRFC1122UrgentPointer**</span></span>](settcpuserfc1122urgentpointer-method-in-class-win32-networkadapterconfiguration.md)     | <span data-ttu-id="334d4-197">指定 TCP 是否使用緊急資料的 RFC 1122 規格，或 Berkeley Software Design (BSD) 衍生系統所使用的模式。</span><span class="sxs-lookup"><span data-stu-id="334d4-197">Specifies whether TCP uses the RFC 1122 specification for urgent data, or the mode used by Berkeley Software Design (BSD) derived systems.</span></span><br/> |
| [<span data-ttu-id="334d4-198">**SetTcpWindowSize**</span><span class="sxs-lookup"><span data-stu-id="334d4-198">**SetTcpWindowSize**</span></span>](settcpwindowsize-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="334d4-199">設定系統提供的 TCP 接收視窗大小上限。</span><span class="sxs-lookup"><span data-stu-id="334d4-199">Sets the maximum TCP Receive Window size offered by the system.</span></span><br/>                                                                            |
| [<span data-ttu-id="334d4-200">**SetWINSServer**</span><span class="sxs-lookup"><span data-stu-id="334d4-200">**SetWINSServer**</span></span>](setwinsserver-method-in-class-win32-networkadapterconfiguration.md)                                     | <span data-ttu-id="334d4-201">設定此 TCP/IP 系結網路介面卡上 (WINS) 伺服器的主要和次要 Windows 網際網路命名服務。</span><span class="sxs-lookup"><span data-stu-id="334d4-201">Sets the primary and secondary Windows Internet Naming Service (WINS) servers on this TCP/IP-bound network adapter.</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="334d4-202">屬性</span><span class="sxs-lookup"><span data-stu-id="334d4-202">Properties</span></span>

<span data-ttu-id="334d4-203">**Win32 \_ >networkadapterconfiguration** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="334d4-203">The **Win32\_NetworkAdapterConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="334d4-204">**ArpAlwaysSourceRoute**</span><span class="sxs-lookup"><span data-stu-id="334d4-204">**ArpAlwaysSourceRoute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-205">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="334d4-205">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-206">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-207">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| ArpAlwaysSourceRoute" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-207">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ArpAlwaysSourceRoute")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-208">若 **為 TRUE**，tcp/ip 會將位址解析通訊協定 (ARP) 在權杖環狀網路上啟用來源路由的查詢。</span><span class="sxs-lookup"><span data-stu-id="334d4-208">If **TRUE**, TCP/IP transmits Address Resolution Protocol (ARP) queries with source routing enabled on Token Ring networks.</span></span> <span data-ttu-id="334d4-209">根據預設 (FALSE) ，則會在沒有來源路由的情況下進行 ARP 的第一次查詢，如果未收到回復，則會在啟用來源路由的情況下</span><span class="sxs-lookup"><span data-stu-id="334d4-209">By default (FALSE), ARP first queries without source routing, and then retries with source routing enabled if no reply is received.</span></span> <span data-ttu-id="334d4-210">來源路由允許在不同類型的網路之間路由傳送網路封包。</span><span class="sxs-lookup"><span data-stu-id="334d4-210">Source routing allows the routing of network packets across different types of networks.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-211">**ArpUseEtherSNAP**</span><span class="sxs-lookup"><span data-stu-id="334d4-211">**ArpUseEtherSNAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-212">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="334d4-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-214">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| ArpUseEtherSNAP" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-214">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ArpUseEtherSNAP")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-215">若 **為 TRUE**，乙太網路封包會遵循 IEEE 802.3 Sub-Network 存取通訊協定 (貼齊) 編碼。</span><span class="sxs-lookup"><span data-stu-id="334d4-215">If **TRUE**, Ethernet packets follow the IEEE 802.3 Sub-Network Access Protocol (SNAP) encoding.</span></span> <span data-ttu-id="334d4-216">將此參數設定為1，會強制 TCP/IP 使用802.3 貼齊編碼來傳輸乙太網路封包。</span><span class="sxs-lookup"><span data-stu-id="334d4-216">Setting this parameter to 1 forces TCP/IP to transmit Ethernet packets by using 802.3 SNAP encoding.</span></span> <span data-ttu-id="334d4-217">根據預設 (FALSE) ，堆疊會以 DIX Ethernet 格式傳送封包。</span><span class="sxs-lookup"><span data-stu-id="334d4-217">By default (FALSE), the stack transmits packets in DIX Ethernet format.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-218">**標題**</span><span class="sxs-lookup"><span data-stu-id="334d4-218">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-219">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="334d4-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-221">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="334d4-221">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="334d4-222">目前物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="334d4-222">Short textual description of the current object.</span></span>

<span data-ttu-id="334d4-223">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="334d4-223">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="334d4-224">**DatabasePath**</span><span class="sxs-lookup"><span data-stu-id="334d4-224">**DatabasePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-225">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="334d4-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-226">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-227">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| DatabasePath" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-227">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|DatabasePath")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-228">)  (主機、LMHOSTS、網路和通訊協定的標準網際網路資料庫檔案的 Windows 檔案路徑有效。</span><span class="sxs-lookup"><span data-stu-id="334d4-228">Valid Windows file path to standard Internet database files (HOSTS, LMHOSTS, NETWORKS, and PROTOCOLS).</span></span> <span data-ttu-id="334d4-229">Windows 通訊端介面使用檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="334d4-229">The file path is used by the Windows Sockets interface.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-230">**DeadGWDetectEnabled**</span><span class="sxs-lookup"><span data-stu-id="334d4-230">**DeadGWDetectEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-231">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="334d4-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-232">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-233">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| EnableDeadGWDetect" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-233">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnableDeadGWDetect")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-234">若 **為 TRUE，則** 會進行死閘道偵測。</span><span class="sxs-lookup"><span data-stu-id="334d4-234">If **TRUE**, dead gateway detection occurs.</span></span> <span data-ttu-id="334d4-235">啟用這項功能之後，傳輸控制通訊協定 (TCP) 會要求網際網路通訊協定 (IP) 變更為備份閘道，如果它會多次重新傳輸區段，而不會收到回應。</span><span class="sxs-lookup"><span data-stu-id="334d4-235">With this feature enabled, Transmission Control Protocol (TCP) asks Internet Protocol (IP) to change to a backup gateway if it retransmits a segment several times without receiving a response.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-236">**DefaultIPGateway**</span><span class="sxs-lookup"><span data-stu-id="334d4-236">**DefaultIPGateway**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-237">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="334d4-237">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="334d4-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-239">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \| DefaultGateway" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\|DefaultGateway")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-240">電腦系統使用之預設閘道的 IP 位址陣列。</span><span class="sxs-lookup"><span data-stu-id="334d4-240">Array of IP addresses of default gateways that the computer system uses.</span></span>

<span data-ttu-id="334d4-241">範例： "192.168.12.1 192.168.46.1"</span><span class="sxs-lookup"><span data-stu-id="334d4-241">Example: "192.168.12.1 192.168.46.1"</span></span>

</dd> <dt>

<span data-ttu-id="334d4-242">**DefaultTOS**</span><span class="sxs-lookup"><span data-stu-id="334d4-242">**DefaultTOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-243">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="334d4-243">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-244">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-245">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| DefaultTOS" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-245">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|DefaultTOS")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-246">預設的服務類型 (TOS 在連出 IP 封包的標頭中設定的) 值。</span><span class="sxs-lookup"><span data-stu-id="334d4-246">Default Type Of Service (TOS) value set in the header of outgoing IP packets.</span></span> <span data-ttu-id="334d4-247"> (RFC) 791 的批註要求會定義值。</span><span class="sxs-lookup"><span data-stu-id="334d4-247">Request for Comments (RFC) 791 defines the values.</span></span> <span data-ttu-id="334d4-248">預設值： 0 (零) ，有效範圍： 0-255。</span><span class="sxs-lookup"><span data-stu-id="334d4-248">Default: 0 (zero), Valid Range: 0 - 255.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-249">**DefaultTTL**</span><span class="sxs-lookup"><span data-stu-id="334d4-249">**DefaultTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-250">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="334d4-250">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-251">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-252">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| DefaultTTL" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|DefaultTTL")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-253">預設存留時間 (TTL) 在傳出 IP 封包的標頭中設定的值。</span><span class="sxs-lookup"><span data-stu-id="334d4-253">Default Time To Live (TTL) value set in the header of outgoing IP packets.</span></span> <span data-ttu-id="334d4-254">TTL 會指定 IP 封包在被捨棄之前，可以通過的路由器數量來到達目的地。</span><span class="sxs-lookup"><span data-stu-id="334d4-254">The TTL specifies the number of routers an IP packet can pass through to reach its destination before being discarded.</span></span> <span data-ttu-id="334d4-255">當 TTL 為 0 (零) 時，每個路由器會以傳遞的封包的 TTL 計數遞減並捨棄封包。</span><span class="sxs-lookup"><span data-stu-id="334d4-255">Each router decrements by one the TTL count of a packet as it passes through and discards the packets—if the TTL is 0 (zero).</span></span> <span data-ttu-id="334d4-256">預設值：32，有效範圍： 1-255。</span><span class="sxs-lookup"><span data-stu-id="334d4-256">Default: 32, Valid Range: 1 - 255.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-257">**說明**</span><span class="sxs-lookup"><span data-stu-id="334d4-257">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-258">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="334d4-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-259">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="334d4-260">目前物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="334d4-260">Textual description of the current object.</span></span>

<span data-ttu-id="334d4-261">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="334d4-261">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="334d4-262">**DHCPEnabled**</span><span class="sxs-lookup"><span data-stu-id="334d4-262">**DHCPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-263">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="334d4-263">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-264">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-265">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| EnableDHCP" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-265">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|EnableDHCP")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-266">若 **為 TRUE**，則在建立網路連線時， (DHCP) server 的動態主機設定通訊協定會自動將 IP 位址指派給電腦系統。</span><span class="sxs-lookup"><span data-stu-id="334d4-266">If **TRUE**, the dynamic host configuration protocol (DHCP) server automatically assigns an IP address to the computer system when establishing a network connection.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-267">**DHCPLeaseExpires**</span><span class="sxs-lookup"><span data-stu-id="334d4-267">**DHCPLeaseExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-268">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="334d4-268">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-269">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-270">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| LeaseTerminatesTime" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-270">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|LeaseTerminatesTime")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-271">由動態主機設定通訊協定指派給電腦的租用 IP 位址的到期日期和時間 (DHCP) 伺服器。</span><span class="sxs-lookup"><span data-stu-id="334d4-271">Expiration date and time for a leased IP address that was assigned to the computer by the dynamic host configuration protocol (DHCP) server.</span></span>

<span data-ttu-id="334d4-272">範例：20521201000230.000000000</span><span class="sxs-lookup"><span data-stu-id="334d4-272">Example: 20521201000230.000000000</span></span>

</dd> <dt>

<span data-ttu-id="334d4-273">**DHCPLeaseObtained**</span><span class="sxs-lookup"><span data-stu-id="334d4-273">**DHCPLeaseObtained**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-274">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="334d4-274">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-275">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-276">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| LeaseObtainedTime" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-276">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|LeaseObtainedTime")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-277">使用動態主機設定通訊協定指派給電腦之 IP 位址的日期和時間 (DHCP) 伺服器。</span><span class="sxs-lookup"><span data-stu-id="334d4-277">Date and time the lease was obtained for the IP address assigned to the computer by the dynamic host configuration protocol (DHCP) server.</span></span>

<span data-ttu-id="334d4-278">範例：19521201000230.000000000</span><span class="sxs-lookup"><span data-stu-id="334d4-278">Example: 19521201000230.000000000</span></span>

</dd> <dt>

<span data-ttu-id="334d4-279">**DHCPServer**</span><span class="sxs-lookup"><span data-stu-id="334d4-279">**DHCPServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-280">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="334d4-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-281">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-282">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| DhcpServer" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-282">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|DhcpServer")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-283">動態主機設定通訊協定 (DHCP) server 的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="334d4-283">IP address of the dynamic host configuration protocol (DHCP) server.</span></span>

<span data-ttu-id="334d4-284">範例： "10.55.34.2"</span><span class="sxs-lookup"><span data-stu-id="334d4-284">Example: "10.55.34.2"</span></span>

</dd> <dt>

<span data-ttu-id="334d4-285">**DNSDomain**</span><span class="sxs-lookup"><span data-stu-id="334d4-285">**DNSDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-286">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="334d4-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-287">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-288">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| Domain" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-288">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|Domain")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-289">組織名稱後面接著句點和指出組織類型的延伸模組，例如 "microsoft.com"。</span><span class="sxs-lookup"><span data-stu-id="334d4-289">Organization name followed by a period and an extension that indicates the type of organization, such as "microsoft.com".</span></span> <span data-ttu-id="334d4-290">名稱可以是字母 A 到 Z 的任何組合、數位0到9，以及連字號 ( ) ，再加上句點 (. 用來作為分隔符號的 ) 字元。</span><span class="sxs-lookup"><span data-stu-id="334d4-290">The name can be any combination of the letters A through Z, the numerals 0 through 9, and the hyphen (-), plus the period (.) character used as a separator.</span></span>

<span data-ttu-id="334d4-291">範例： "microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="334d4-291">Example: "microsoft.com"</span></span>

</dd> <dt>

<span data-ttu-id="334d4-292">**DNSDomainSuffixSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="334d4-292">**DNSDomainSuffixSearchOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-293">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="334d4-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="334d4-294">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-295">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| SearchList" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-295">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|SearchList")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-296">DNS 網域尾碼的陣列，要在名稱解析期間附加至主機名稱的結尾。</span><span class="sxs-lookup"><span data-stu-id="334d4-296">Array of DNS domain suffixes to be appended to the end of host names during name resolution.</span></span> <span data-ttu-id="334d4-297">當您嘗試從僅限主機名稱稱)  (FQDN 來解析完整功能變數名稱時，系統會先附加本機功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="334d4-297">When attempting to resolve a fully qualified domain name (FQDN) from a host-only name, the system will first append the local domain name.</span></span> <span data-ttu-id="334d4-298">如果不成功，系統將使用 [網域尾碼] 清單，依列出的順序建立其他 Fqdn，並查詢 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="334d4-298">If this is not successful, the system will use the domain suffix list to create additional FQDNs in the order listed and query DNS servers for each.</span></span>

<span data-ttu-id="334d4-299">範例： "samples.microsoft.com example.microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="334d4-299">Example: "samples.microsoft.com example.microsoft.com"</span></span>

</dd> <dt>

<span data-ttu-id="334d4-300">**DNSEnabledForWINSResolution**</span><span class="sxs-lookup"><span data-stu-id="334d4-300">**DNSEnabledForWINSResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-301">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="334d4-301">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-302">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-303">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| EnableDNS" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-303">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnableDNS")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-304">若 **為 TRUE**，則會啟用透過 Windows 網際網路進行名稱解析的網域名稱系統 (DNS) 命名服務 (WINS) 解決方案。</span><span class="sxs-lookup"><span data-stu-id="334d4-304">If **TRUE**, the Domain Name System (DNS) is enabled for name resolution over Windows Internet Naming Service (WINS) resolution.</span></span> <span data-ttu-id="334d4-305">如果無法使用 DNS 來解析名稱，則會將名稱要求轉送至 WINS 以進行解析。</span><span class="sxs-lookup"><span data-stu-id="334d4-305">If the name cannot be resolved using DNS, the name request is forwarded to WINS for resolution.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-306">**DNSHostName**</span><span class="sxs-lookup"><span data-stu-id="334d4-306">**DNSHostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-307">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="334d4-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-308">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-309">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| Hostname" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-309">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|Hostname")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-310">用來識別本機電腦以供某些公用程式進行驗證的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="334d4-310">Host name used to identify the local computer for authentication by some utilities.</span></span> <span data-ttu-id="334d4-311">其他以 TCP/IP 為基礎的公用程式可以使用此值來取得本機電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="334d4-311">Other TCP/IP-based utilities can use this value to acquire the name of the local computer.</span></span> <span data-ttu-id="334d4-312">主機名稱會儲存在 DNS 伺服器的資料表中，該資料表會將名稱對應至 IP 位址，以供 DNS 使用。</span><span class="sxs-lookup"><span data-stu-id="334d4-312">Host names are stored on DNS servers in a table that maps names to IP addresses for use by DNS.</span></span> <span data-ttu-id="334d4-313">名稱可以是字母 A 到 Z 的任何組合、數位0到9，以及連字號 ( ) ，再加上句點 (. 用來作為分隔符號的 ) 字元。</span><span class="sxs-lookup"><span data-stu-id="334d4-313">The name can be any combination of the letters A through Z, the numerals 0 through 9, and the hyphen (-), plus the period (.) character used as a separator.</span></span> <span data-ttu-id="334d4-314">依預設，此值是 Microsoft 網路電腦名稱稱，但網路系統管理員可以指派其他主機名稱，而不會影響電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="334d4-314">By default, this value is the Microsoft networking computer name, but the network administrator can assign another host name without affecting the computer name.</span></span>

<span data-ttu-id="334d4-315">範例： "corpdns"</span><span class="sxs-lookup"><span data-stu-id="334d4-315">Example: "corpdns"</span></span>

</dd> <dt>

<span data-ttu-id="334d4-316">**DNSServerSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="334d4-316">**DNSServerSearchOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-317">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="334d4-317">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="334d4-318">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-319">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| NameServer" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-319">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|NameServer")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-320">要用於查詢 DNS 伺服器的伺服器 IP 位址陣列。</span><span class="sxs-lookup"><span data-stu-id="334d4-320">Array of server IP addresses to be used in querying for DNS servers.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-321">**DomainDNSRegistrationEnabled**</span><span class="sxs-lookup"><span data-stu-id="334d4-321">**DomainDNSRegistrationEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-322">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="334d4-322">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-323">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="334d4-324">若為 **TRUE**，除了在電腦的完整 DNS 名稱下註冊之外，此連線的 IP 位址也會在此連線的功能變數名稱下註冊于 DNS 中。</span><span class="sxs-lookup"><span data-stu-id="334d4-324">If **TRUE**, the IP addresses for this connection are registered in DNS under the domain name of this connection in addition to being registered under the computer's full DNS name.</span></span> <span data-ttu-id="334d4-325">此連接的功能變數名稱可使用 [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md) () 方法設定，或由 DSCP 指派。</span><span class="sxs-lookup"><span data-stu-id="334d4-325">The domain name of this connection is either set using the [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)() method or assigned by DSCP.</span></span> <span data-ttu-id="334d4-326">註冊的名稱是已附加功能變數名稱之電腦的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="334d4-326">The registered name is the host name of the computer with the domain name appended.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-327">**ForwardBufferMemory**</span><span class="sxs-lookup"><span data-stu-id="334d4-327">**ForwardBufferMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-328">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="334d4-328">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-329">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-330">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| ForwardBufferMemory" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-330">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ForwardBufferMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-331">由 IP 配置的記憶體，用來將封包資料儲存在路由器封包佇列中。</span><span class="sxs-lookup"><span data-stu-id="334d4-331">Memory allocated by IP to store packet data in the router packet queue.</span></span> <span data-ttu-id="334d4-332">填滿此緩衝區空間時，路由器會開始從其佇列中隨機捨棄封包。</span><span class="sxs-lookup"><span data-stu-id="334d4-332">When this buffer space is filled, the router begins discarding packets at random from its queue.</span></span> <span data-ttu-id="334d4-333">封包佇列資料緩衝區的長度為256個位元組，因此此參數的值應該是256的倍數。</span><span class="sxs-lookup"><span data-stu-id="334d4-333">Packet queue data buffers are 256 bytes in length, so the value of this parameter should be a multiple of 256.</span></span> <span data-ttu-id="334d4-334">多個緩衝區會連結在一起，以取得較大的封包。</span><span class="sxs-lookup"><span data-stu-id="334d4-334">Multiple buffers are chained together for larger packets.</span></span> <span data-ttu-id="334d4-335">封包的 IP 標頭會分開儲存。</span><span class="sxs-lookup"><span data-stu-id="334d4-335">The IP header for a packet is stored separately.</span></span> <span data-ttu-id="334d4-336">如果未啟用 IP 路由器，則會忽略此參數，且不會配置任何緩衝區。</span><span class="sxs-lookup"><span data-stu-id="334d4-336">This parameter is ignored and no buffers are allocated if the IP router is not enabled.</span></span> <span data-ttu-id="334d4-337">緩衝區大小的範圍可以從網路 MTU 到小於0xFFFFFFFF 的值。</span><span class="sxs-lookup"><span data-stu-id="334d4-337">The buffer size can range from the network MTU to a value smaller than 0xFFFFFFFF.</span></span> <span data-ttu-id="334d4-338">預設值： 74240 (50 1480 位元組封包，四捨五入為 256) 的倍數。</span><span class="sxs-lookup"><span data-stu-id="334d4-338">Default: 74240 (fifty 1480-byte packets, rounded to a multiple of 256).</span></span>

</dd> <dt>

<span data-ttu-id="334d4-339">**FullDNSRegistrationEnabled**</span><span class="sxs-lookup"><span data-stu-id="334d4-339">**FullDNSRegistrationEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-340">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="334d4-340">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-341">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="334d4-342">若為 **TRUE**，則此連線的 IP 位址會在 dns 中，以電腦的完整 dns 名稱註冊。</span><span class="sxs-lookup"><span data-stu-id="334d4-342">If **TRUE**, the IP addresses for this connection are registered in DNS under the computer's full DNS name.</span></span> <span data-ttu-id="334d4-343">電腦的完整 DNS 名稱會顯示在主控台的系統應用程式的 [ **網路識別** ] 索引標籤上。</span><span class="sxs-lookup"><span data-stu-id="334d4-343">The full DNS name of the computer is displayed on the **Network Identification** tab in the System application in Control Panel.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-344">**GatewayCostMetric**</span><span class="sxs-lookup"><span data-stu-id="334d4-344">**GatewayCostMetric**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-345">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="334d4-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="334d4-346">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="334d4-347">整數成本計量值的陣列 (範圍從1到 9999) ，用來計算最快、最可靠或最少的資源密集路由。</span><span class="sxs-lookup"><span data-stu-id="334d4-347">Array of integer cost metric values (ranging from 1 to 9999) to be used in calculating the fastest, most reliable, or least resource-intensive routes.</span></span> <span data-ttu-id="334d4-348">這個引數與 **DefaultIPGateway** 屬性具有一對一的對應關係。</span><span class="sxs-lookup"><span data-stu-id="334d4-348">This argument has a one-to-one correspondence with the **DefaultIPGateway** property.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-349">**IGMPLevel**</span><span class="sxs-lookup"><span data-stu-id="334d4-349">**IGMPLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-350">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="334d4-350">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-351">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-352">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| IGMPLevel" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-352">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|IGMPLevel")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-353">系統支援 IP 多播並參與網際網路群組管理通訊協定 (IGMP) 的範圍。</span><span class="sxs-lookup"><span data-stu-id="334d4-353">Extent to which the system supports IP multicast and participates in the Internet Group Management Protocol (IGMP).</span></span> <span data-ttu-id="334d4-354">在層級 0 (零) ，系統不會提供任何多播支援。</span><span class="sxs-lookup"><span data-stu-id="334d4-354">At level 0 (zero), the system provides no multicast support.</span></span> <span data-ttu-id="334d4-355">在層級1，系統可能只會傳送 IP 多播封包。</span><span class="sxs-lookup"><span data-stu-id="334d4-355">At level 1, the system may only send IP multicast packets.</span></span> <span data-ttu-id="334d4-356">在層級2，系統可能會傳送 IP 多播封包，並完整地參與 IGMP 以接收多播封包。</span><span class="sxs-lookup"><span data-stu-id="334d4-356">At level 2, the system may send IP multicast packets and fully participate in IGMP to receive multicast packets.</span></span>

<dt>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>

<span data-ttu-id="334d4-357"><span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>**沒有多播** (0) </span><span class="sxs-lookup"><span data-stu-id="334d4-357"><span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>**No Multicast** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>

<span data-ttu-id="334d4-358"><span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>**IP 多播** (1) </span><span class="sxs-lookup"><span data-stu-id="334d4-358"><span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>**IP Multicast** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>

<span data-ttu-id="334d4-359"><span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>**IP & IGMP 多播** (2) </span><span class="sxs-lookup"><span data-stu-id="334d4-359"><span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>**IP & IGMP multicast** (2)</span></span>


</dt> <dd>

<span data-ttu-id="334d4-360">IP 和 IGMP 多播 (預設) </span><span class="sxs-lookup"><span data-stu-id="334d4-360">IP and IGMP Multicast (default)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="334d4-361">**Index**</span><span class="sxs-lookup"><span data-stu-id="334d4-361">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-362">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="334d4-362">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-363">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-364">限定詞： [**key**](../wmisdk/key-qualifier.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-364">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E972-E325-11CE-BFC1-08002BE10318}")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-365">Windows 網路介面卡設定的索引編號。</span><span class="sxs-lookup"><span data-stu-id="334d4-365">Index number of the Windows network adapter configuration.</span></span> <span data-ttu-id="334d4-366">當有多個可用的設定時，就會使用索引編號。</span><span class="sxs-lookup"><span data-stu-id="334d4-366">The index number is used when there is more than one configuration available.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-367">**InterfaceIndex**</span><span class="sxs-lookup"><span data-stu-id="334d4-367">**InterfaceIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-368">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="334d4-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-369">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="334d4-370">可唯一識別區域網路介面的索引值。</span><span class="sxs-lookup"><span data-stu-id="334d4-370">Index value that uniquely identifies a local network interface.</span></span> <span data-ttu-id="334d4-371">這個屬性中的值與 [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)實例（代表路由表中的網路介面）的 **InterfaceIndex** 屬性值相同。</span><span class="sxs-lookup"><span data-stu-id="334d4-371">The value in this property is the same as the value in the **InterfaceIndex** property in the instance of [**Win32\_IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) that represents the network interface in the route table.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-372">**IPAddress**</span><span class="sxs-lookup"><span data-stu-id="334d4-372">**IPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-373">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="334d4-373">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="334d4-374">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-375">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \\ \\ Tcpip \| IPAddress" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-375">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\\\\Tcpip\|IPAddress")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-376">所有與目前網路介面卡相關聯的 IP 位址陣列。</span><span class="sxs-lookup"><span data-stu-id="334d4-376">Array of all of the IP addresses associated with the current network adapter.</span></span> <span data-ttu-id="334d4-377">這個屬性可以包含 IPv6 位址或 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="334d4-377">This property can contain either IPv6 addresses or IPv4 addresses.</span></span> <span data-ttu-id="334d4-378">如需詳細資訊，請參閱 [WMI 中的 IPv6 和 IPv4 支援](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="334d4-378">For more information, see [IPv6 and IPv4 Support in WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).</span></span>

<span data-ttu-id="334d4-379">範例 IPv6 位址： "2010：836B：4179：：836B： 4179"</span><span class="sxs-lookup"><span data-stu-id="334d4-379">Example IPv6 address: "2010:836B:4179::836B:4179"</span></span>

</dd> <dt>

<span data-ttu-id="334d4-380">**IPConnectionMetric**</span><span class="sxs-lookup"><span data-stu-id="334d4-380">**IPConnectionMetric**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-381">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="334d4-381">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-382">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="334d4-383">使用針對 IP 系結介面卡設定的路由，以及 IP 路由表中這些路由的加權值的成本。</span><span class="sxs-lookup"><span data-stu-id="334d4-383">Cost of using the configured routes for the IP bound adapter and is the weighted value for those routes in the IP routing table.</span></span> <span data-ttu-id="334d4-384">如果 IP 路由表中有多個目的地的路由，則會使用最低計量的路由。</span><span class="sxs-lookup"><span data-stu-id="334d4-384">If there are multiple routes to a destination in the IP routing table, the route with the lowest metric is used.</span></span> <span data-ttu-id="334d4-385">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="334d4-385">The default value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-386">**IPEnabled**</span><span class="sxs-lookup"><span data-stu-id="334d4-386">**IPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-387">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="334d4-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-388">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-389">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \\ \\ Tcpip" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\\\\Tcpip")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-390">若 **為 TRUE**，則會在此網路介面卡上系結並啟用 tcp/ip。</span><span class="sxs-lookup"><span data-stu-id="334d4-390">If **TRUE**, TCP/IP is bound and enabled on this network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-391">**IPFilterSecurityEnabled**</span><span class="sxs-lookup"><span data-stu-id="334d4-391">**IPFilterSecurityEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-392">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="334d4-392">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-393">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-394">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| IPFilterSecurityEnabled" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-394">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|IPFilterSecurityEnabled")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-395">若 **為 TRUE**，則會在所有 ip 系結的網路介面卡上全域啟用 ip 埠安全性，而且與個別網路介面卡相關聯的安全性值就會生效。</span><span class="sxs-lookup"><span data-stu-id="334d4-395">If **TRUE**, IP port security is enabled globally across all IP-bound network adapters and the security values associated with individual network adapters are in effect.</span></span> <span data-ttu-id="334d4-396">這個屬性會與 **IPSecPermitTCPPorts**、 **IPSecPermitUDPPorts** 和 **IPSecPermitIPProtocols** 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="334d4-396">This property is used in conjunction with **IPSecPermitTCPPorts**, **IPSecPermitUDPPorts**, and **IPSecPermitIPProtocols**.</span></span> <span data-ttu-id="334d4-397">若 **為 FALSE**，則會在所有網路介面卡上停用 IP 篩選器安全性，並允許所有埠和通訊協定流量進行未篩選的流程。</span><span class="sxs-lookup"><span data-stu-id="334d4-397">If **FALSE**, IP filter security is disabled across all network adapters and allows all port and protocol traffic to flow unfiltered.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-398">**IPPortSecurityEnabled**</span><span class="sxs-lookup"><span data-stu-id="334d4-398">**IPPortSecurityEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-399">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="334d4-399">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-400">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-401">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ >networkadapterconfiguration \| IPFilterSecurityEnabled" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-401">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkAdapterConfiguration\|IPFilterSecurityEnabled")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-402">若 **為 TRUE**，則會在所有 ip 系結的網路介面卡上全域啟用 ip 埠安全性。</span><span class="sxs-lookup"><span data-stu-id="334d4-402">If **TRUE**, IP port security is enabled globally across all IP-bound network adapters.</span></span> <span data-ttu-id="334d4-403">這個屬性已經過時。</span><span class="sxs-lookup"><span data-stu-id="334d4-403">This property is obsolete.</span></span> <span data-ttu-id="334d4-404">若要取代這個屬性，您應該使用 **IPFilterSecurityEnabled**。</span><span class="sxs-lookup"><span data-stu-id="334d4-404">In place of this property, you should use **IPFilterSecurityEnabled**.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-405">**IPSecPermitIPProtocols**</span><span class="sxs-lookup"><span data-stu-id="334d4-405">**IPSecPermitIPProtocols**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-406">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="334d4-406">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="334d4-407">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-408">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| RawIPAllowedProtocols" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-408">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|RawIPAllowedProtocols")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-409">允許透過 IP 執行的通訊協定陣列。</span><span class="sxs-lookup"><span data-stu-id="334d4-409">Array of the protocols permitted to run over the IP.</span></span> <span data-ttu-id="334d4-410">通訊協定清單是使用 [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) 方法來定義。</span><span class="sxs-lookup"><span data-stu-id="334d4-410">The list of protocols is defined using the [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span> <span data-ttu-id="334d4-411">此清單會是空的或包含數值。</span><span class="sxs-lookup"><span data-stu-id="334d4-411">The list will either be empty or contain numeric values.</span></span> <span data-ttu-id="334d4-412">數值 0 (零) 表示授與所有通訊協定的存取權限。</span><span class="sxs-lookup"><span data-stu-id="334d4-412">A numeric value of 0 (zero) indicates access permission is granted for all protocols.</span></span> <span data-ttu-id="334d4-413">空字串表示當 **IPFilterSecurityEnabled** 為 **TRUE** 時，不允許執行任何通訊協定。</span><span class="sxs-lookup"><span data-stu-id="334d4-413">An empty string indicates that no protocols are permitted to run when **IPFilterSecurityEnabled** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-414">**IPSecPermitTCPPorts**</span><span class="sxs-lookup"><span data-stu-id="334d4-414">**IPSecPermitTCPPorts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-415">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="334d4-415">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="334d4-416">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-417">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| TCPAllowedPorts" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-417">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TCPAllowedPorts")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-418">將授與 TCP 存取權限之埠的陣列。</span><span class="sxs-lookup"><span data-stu-id="334d4-418">Array of the ports that will be granted access permission for TCP.</span></span> <span data-ttu-id="334d4-419">通訊協定清單是使用 [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) 方法來定義。</span><span class="sxs-lookup"><span data-stu-id="334d4-419">The list of protocols is defined using the [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span> <span data-ttu-id="334d4-420">此清單會是空的或包含數值。</span><span class="sxs-lookup"><span data-stu-id="334d4-420">The list will either be empty or contain numeric values.</span></span> <span data-ttu-id="334d4-421">數值 0 (零) 表示授與所有埠的存取權限。</span><span class="sxs-lookup"><span data-stu-id="334d4-421">A numeric value of 0 (zero)indicates access permission is granted for all ports.</span></span> <span data-ttu-id="334d4-422">空字串表示當 **IPFilterSecurityEnabled** 為 **TRUE** 時，沒有任何埠被授與存取權限。</span><span class="sxs-lookup"><span data-stu-id="334d4-422">An empty string indicates that no ports are granted access permission when **IPFilterSecurityEnabled** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-423">**IPSecPermitUDPPorts**</span><span class="sxs-lookup"><span data-stu-id="334d4-423">**IPSecPermitUDPPorts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-424">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="334d4-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="334d4-425">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-426">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| UDPAllowedPorts" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-426">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|UDPAllowedPorts")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-427">將授與使用者資料包協定 (UDP) 存取權限之埠的陣列。</span><span class="sxs-lookup"><span data-stu-id="334d4-427">Array of the ports that will be granted User Datagram Protocol (UDP) access permission.</span></span> <span data-ttu-id="334d4-428">通訊協定清單是使用 [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) 方法來定義。</span><span class="sxs-lookup"><span data-stu-id="334d4-428">The list of protocols is defined using the [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span> <span data-ttu-id="334d4-429">此清單會是空的或包含數值。</span><span class="sxs-lookup"><span data-stu-id="334d4-429">The list will either be empty or contain numeric values.</span></span> <span data-ttu-id="334d4-430">數值 0 (零) 表示授與所有埠的存取權限。</span><span class="sxs-lookup"><span data-stu-id="334d4-430">A numeric value of 0 (zero) indicates access permission is granted for all ports.</span></span> <span data-ttu-id="334d4-431">空字串表示當 **IPFilterSecurityEnabled** 為 **TRUE** 時，沒有任何埠被授與存取權限。</span><span class="sxs-lookup"><span data-stu-id="334d4-431">An empty string indicates that no ports are granted access permission when **IPFilterSecurityEnabled** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-432">**IPSubnet**</span><span class="sxs-lookup"><span data-stu-id="334d4-432">**IPSubnet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-433">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="334d4-433">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="334d4-434">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-435">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \| SubnetMask" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-435">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\|SubnetMask")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-436">所有與目前網路介面卡相關聯的子網路遮罩的陣列。</span><span class="sxs-lookup"><span data-stu-id="334d4-436">Array of all of the subnet masks associated with the current network adapter.</span></span>

<span data-ttu-id="334d4-437">範例： "255.255.0.0"</span><span class="sxs-lookup"><span data-stu-id="334d4-437">Example: "255.255.0.0"</span></span>

</dd> <dt>

<span data-ttu-id="334d4-438">**IPUseZeroBroadcast**</span><span class="sxs-lookup"><span data-stu-id="334d4-438">**IPUseZeroBroadcast**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-439">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="334d4-439">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-440">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-441">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| UseZeroBroadcast" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-441">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|UseZeroBroadcast")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-442">若 **為 TRUE**，則會使用 IP 零廣播 (0.0.0.0) ，而且系統會使用 (255.255.255.255) 的廣播。</span><span class="sxs-lookup"><span data-stu-id="334d4-442">If **TRUE**, IP zeros-broadcasts are used (0.0.0.0), and the system uses ones-broadcasts (255.255.255.255).</span></span> <span data-ttu-id="334d4-443">電腦系統通常會使用其中一種廣播，但衍生自 BSD 的專案則會使用零的廣播。</span><span class="sxs-lookup"><span data-stu-id="334d4-443">Computer systems generally use ones-broadcasts, but those derived from BSD implementations use zeros-broadcasts.</span></span> <span data-ttu-id="334d4-444">未使用相同廣播的系統將無法在相同網路上互通。</span><span class="sxs-lookup"><span data-stu-id="334d4-444">Systems that do not use that same broadcasts will not interoperate on the same network.</span></span> <span data-ttu-id="334d4-445">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="334d4-445">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-446">**IPXAddress**</span><span class="sxs-lookup"><span data-stu-id="334d4-446">**IPXAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-447">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="334d4-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-448">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-448">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-449">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Windows 通訊端第2版 \| [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) \| IPX \_ ADDRESS" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-449">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Sockets Version 2\|[**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt)\|IPX\_ADDRESS")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-450">網路封包交換 (IPX) 技術已不再支援，而且此屬性不包含有用的資料。</span><span class="sxs-lookup"><span data-stu-id="334d4-450">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-451">**IPXEnabled**</span><span class="sxs-lookup"><span data-stu-id="334d4-451">**IPXEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-452">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="334d4-452">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-453">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-454">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-454">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-455">網路封包交換 (IPX) 技術已不再支援，而且此屬性不包含有用的資料。</span><span class="sxs-lookup"><span data-stu-id="334d4-455">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-456">**IPXFrameType**</span><span class="sxs-lookup"><span data-stu-id="334d4-456">**IPXFrameType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-457">資料類型： **uint32** 陣列</span><span class="sxs-lookup"><span data-stu-id="334d4-457">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="334d4-458">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-459">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx \\ \\ Parameters \| PktType" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-459">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|PktType")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-460">網路封包交換 (IPX) 技術已不再支援，而且此屬性不包含有用的資料。</span><span class="sxs-lookup"><span data-stu-id="334d4-460">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

<span data-ttu-id="334d4-461">**ETHERNET II** (0) </span><span class="sxs-lookup"><span data-stu-id="334d4-461">**Ethernet II** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="334d4-462">**Ethernet 802.3** (1) </span><span class="sxs-lookup"><span data-stu-id="334d4-462">**Ethernet 802.3** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

<span data-ttu-id="334d4-463">**Ethernet 802.2** (2) </span><span class="sxs-lookup"><span data-stu-id="334d4-463">**Ethernet 802.2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

<span data-ttu-id="334d4-464">**Ethernet 貼齊** (3) </span><span class="sxs-lookup"><span data-stu-id="334d4-464">**Ethernet SNAP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

<span data-ttu-id="334d4-465">**自動** (255) </span><span class="sxs-lookup"><span data-stu-id="334d4-465">**AUTO** (255)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="334d4-466">**IPXMediaType**</span><span class="sxs-lookup"><span data-stu-id="334d4-466">**IPXMediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-467">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="334d4-467">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-468">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-469">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx \\ \\ Parameters \| 媒體" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-469">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|MediaType")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-470">網路封包交換 (IPX) 技術已不再支援，而且此屬性不包含有用的資料。</span><span class="sxs-lookup"><span data-stu-id="334d4-470">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

<dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="334d4-471">**Ethernet** (1) </span><span class="sxs-lookup"><span data-stu-id="334d4-471">**Ethernet** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

<span data-ttu-id="334d4-472">**權杖環** (2) </span><span class="sxs-lookup"><span data-stu-id="334d4-472">**Token ring** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="334d4-473">**FDDI** (3) </span><span class="sxs-lookup"><span data-stu-id="334d4-473">**FDDI** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

<span data-ttu-id="334d4-474">**ARCNET** (8) </span><span class="sxs-lookup"><span data-stu-id="334d4-474">**ARCNET** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="334d4-475">**IPXNetworkNumber**</span><span class="sxs-lookup"><span data-stu-id="334d4-475">**IPXNetworkNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-476">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="334d4-476">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="334d4-477">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-478">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx \\ \\ Parameters \| NetworkNumber" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-478">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|NetworkNumber")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-479">網路封包交換 (IPX) 技術已不再支援，而且此屬性不包含有用的資料。</span><span class="sxs-lookup"><span data-stu-id="334d4-479">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-480">**IPXVirtualNetNumber**</span><span class="sxs-lookup"><span data-stu-id="334d4-480">**IPXVirtualNetNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-481">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="334d4-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-482">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-483">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx \\ \\ Parameters \| VirtualNetworkNumber" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-483">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|VirtualNetworkNumber")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-484">網路封包交換 (IPX) 技術已不再支援，而且此屬性不包含有用的資料。</span><span class="sxs-lookup"><span data-stu-id="334d4-484">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-485">**KeepAliveInterval**</span><span class="sxs-lookup"><span data-stu-id="334d4-485">**KeepAliveInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-486">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="334d4-486">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-487">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-488">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| KeepAliveInterval" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "毫秒" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-488">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-489">分隔保持運作的間隔，直到收到回應為止。</span><span class="sxs-lookup"><span data-stu-id="334d4-489">Interval separating Keep Alive Retransmissions until a response is received.</span></span> <span data-ttu-id="334d4-490">收到回應之後，會延遲到下一個保持運作的傳輸，再由 **KeepAliveTime** 的值控制。</span><span class="sxs-lookup"><span data-stu-id="334d4-490">After a response is received, the delay until the next Keep Alive Transmission is again controlled by the value of **KeepAliveTime**.</span></span> <span data-ttu-id="334d4-491">連線將會在 **TcpMaxDataRetransmissions** 所指定的重新傳輸次數尚未接聽之後中止。</span><span class="sxs-lookup"><span data-stu-id="334d4-491">The connection will be aborted after the number of retransmissions specified by **TcpMaxDataRetransmissions** have gone unanswered.</span></span> <span data-ttu-id="334d4-492">預設值：1000，有效範圍： 1-0xFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="334d4-492">Default: 1000, Valid Range: 1 - 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-493">**KeepAliveTime**</span><span class="sxs-lookup"><span data-stu-id="334d4-493">**KeepAliveTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-494">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="334d4-494">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-495">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-496">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| KeepAliveInterval" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "毫秒" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-496">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-497">**KeepAliveTime** 屬性會藉由傳送 Keep-alive 封包，指出 TCP 嘗試驗證閒置連線是否仍保持不變的頻率。</span><span class="sxs-lookup"><span data-stu-id="334d4-497">The **KeepAliveTime** property indicates how often the TCP attempts to verify that an idle connection is still intact by sending a Keep Alive Packet.</span></span> <span data-ttu-id="334d4-498">可觸達的遠端系統將會認可保持運作傳輸狀態。</span><span class="sxs-lookup"><span data-stu-id="334d4-498">A remote system that is reachable will acknowledge the keep alive transmission.</span></span> <span data-ttu-id="334d4-499">預設不會傳送存活的封包。</span><span class="sxs-lookup"><span data-stu-id="334d4-499">Keep Alive packets are not sent by default.</span></span> <span data-ttu-id="334d4-500">這項功能可以在應用程式的連接中啟用。</span><span class="sxs-lookup"><span data-stu-id="334d4-500">This feature may be enabled in a connection by an application.</span></span> <span data-ttu-id="334d4-501">預設值： 7200000 (兩個小時) 。</span><span class="sxs-lookup"><span data-stu-id="334d4-501">Default: 7,200,000 (two hours).</span></span>

</dd> <dt>

<span data-ttu-id="334d4-502">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="334d4-502">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-503">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="334d4-503">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-504">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-504">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-505">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device Input and Output 函數 \| DeviceIoControl" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-505">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-506">媒體存取控制 (網路介面卡的 MAC) 位址。</span><span class="sxs-lookup"><span data-stu-id="334d4-506">Media Access Control (MAC) address of the network adapter.</span></span> <span data-ttu-id="334d4-507">製造商會指派 MAC 位址來唯一識別網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="334d4-507">A MAC address is assigned by the manufacturer to uniquely identify the network adapter.</span></span>

<span data-ttu-id="334d4-508">範例： "00：80： C7：8F：6C： 96"</span><span class="sxs-lookup"><span data-stu-id="334d4-508">Example: "00:80:C7:8F:6C:96"</span></span>

</dd> <dt>

<span data-ttu-id="334d4-509">**MTU**</span><span class="sxs-lookup"><span data-stu-id="334d4-509">**MTU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-510">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="334d4-510">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-511">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-512">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| MTU" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-512">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|MTU"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-513">覆寫網路介面 (MTU) 的預設最大傳輸單位。</span><span class="sxs-lookup"><span data-stu-id="334d4-513">Overrides the default Maximum Transmission Unit (MTU) for a network interface.</span></span> <span data-ttu-id="334d4-514">MTU 是最大的封包大小 (包括傳輸會透過基礎網路傳輸的傳輸標頭) 。</span><span class="sxs-lookup"><span data-stu-id="334d4-514">The MTU is the maximum packet size (including the transport header) that the transport will transmit over the underlying network.</span></span> <span data-ttu-id="334d4-515">IP 資料包可以跨多個封包。</span><span class="sxs-lookup"><span data-stu-id="334d4-515">The IP datagram can span multiple packets.</span></span> <span data-ttu-id="334d4-516">此值的範圍會跨越基礎網路所支援的 MTU (68) 的最小封包大小。</span><span class="sxs-lookup"><span data-stu-id="334d4-516">The range of this value spans the minimum packet size (68) to the MTU supported by the underlying network.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-517">**NumForwardPackets**</span><span class="sxs-lookup"><span data-stu-id="334d4-517">**NumForwardPackets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-518">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="334d4-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-519">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-520">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| NumForwardPackets" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-520">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|NumForwardPackets")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-521">配置給路由器封包佇列的 IP 封包標頭數目。</span><span class="sxs-lookup"><span data-stu-id="334d4-521">Number of IP packet headers allocated for the router packet queue.</span></span> <span data-ttu-id="334d4-522">當所有標頭都在使用中時，路由器會開始隨機捨棄佇列中的封包。</span><span class="sxs-lookup"><span data-stu-id="334d4-522">When all headers are in use, the router will begin to discard packets from the queue at random.</span></span> <span data-ttu-id="334d4-523">此值應該至少等於 **ForwardBufferMemory** 值除以連線到路由器的網路 IP 資料大小上限。</span><span class="sxs-lookup"><span data-stu-id="334d4-523">This value should be at least as large as the **ForwardBufferMemory** value divided by the maximum IP data size of the networks connected to the router.</span></span> <span data-ttu-id="334d4-524">它應該不會大於 **ForwardBufferMemory** 值除以256，因為每個封包都使用至少256個位元組的轉送緩衝區記憶體。</span><span class="sxs-lookup"><span data-stu-id="334d4-524">It should be no larger than the **ForwardBufferMemory** value divided by 256, since at least 256 bytes of forward buffer memory are used for each packet.</span></span> <span data-ttu-id="334d4-525">給定 **ForwardBufferMemory** 大小的最佳轉寄封包數目，取決於網路上的流量類型。</span><span class="sxs-lookup"><span data-stu-id="334d4-525">The optimal number of forward packets for a given **ForwardBufferMemory** size depends on the type of traffic on the network.</span></span> <span data-ttu-id="334d4-526">它會在這兩個值之間的某處。</span><span class="sxs-lookup"><span data-stu-id="334d4-526">It will be somewhere between these two values.</span></span> <span data-ttu-id="334d4-527">如果未啟用路由器，則會忽略此參數，且不會配置任何標頭。</span><span class="sxs-lookup"><span data-stu-id="334d4-527">If the router is not enabled, this parameter is ignored and no headers are allocated.</span></span> <span data-ttu-id="334d4-528">預設值：50，有效範圍： 1-0xFFFFFFFE。</span><span class="sxs-lookup"><span data-stu-id="334d4-528">Default: 50, Valid Range: 1 - 0xFFFFFFFE.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-529">**PMTUBHDetectEnabled**</span><span class="sxs-lookup"><span data-stu-id="334d4-529">**PMTUBHDetectEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-530">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="334d4-530">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-531">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-531">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-532">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| EnablePMTUBHDetect" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-532">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnablePMTUBHDetect")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-533">若 **為 TRUE**，當 TCP 探索最大傳輸單位的路徑時，就會偵測到黑洞路由器。</span><span class="sxs-lookup"><span data-stu-id="334d4-533">If **TRUE**, detection of black hole routers occurs while TCP discovers the path of the Maximum Transmission Unit.</span></span> <span data-ttu-id="334d4-534">當您需要將未設定片段位的 IP 資料包分割時，黑洞路由器不會傳回 ICMP 目的地無法連線的訊息。</span><span class="sxs-lookup"><span data-stu-id="334d4-534">A black hole router does not return ICMP Destination Unreachable messages when it needs to fragment an IP datagram with the Don't Fragment bit set.</span></span> <span data-ttu-id="334d4-535">TCP 取決於接收這些訊息來執行路徑 MTU 探索。</span><span class="sxs-lookup"><span data-stu-id="334d4-535">TCP depends on receiving these messages to perform Path MTU Discovery.</span></span> <span data-ttu-id="334d4-536">啟用這項功能之後，如果區段的數次重新傳輸未確認，TCP 將會嘗試傳送區段，而不會設定片段位。</span><span class="sxs-lookup"><span data-stu-id="334d4-536">With this feature enabled, TCP will try to send segments without the Don't Fragment bit set if several retransmissions of a segment go unacknowledged.</span></span> <span data-ttu-id="334d4-537">如果已通知區段，則 MSS 將會減少，而不會在連接的未來封包中設定「不片段」位。</span><span class="sxs-lookup"><span data-stu-id="334d4-537">If the segment is acknowledged as a result, the MSS will be decreased and the Don't Fragment bit will be set in future packets on the connection.</span></span> <span data-ttu-id="334d4-538">啟用黑洞偵測會增加針對指定區段執行的重新傳輸數目上限。</span><span class="sxs-lookup"><span data-stu-id="334d4-538">Enabling black hole detection increases the maximum number of retransmissions performed for a given segment.</span></span> <span data-ttu-id="334d4-539">這個屬性的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="334d4-539">The default value of this property is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-540">**PMTUDiscoveryEnabled**</span><span class="sxs-lookup"><span data-stu-id="334d4-540">**PMTUDiscoveryEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-541">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="334d4-541">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-542">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-543">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| EnablePMTUDiscovery" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-543">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnablePMTUDiscovery")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-544">若為 **TRUE**，則會在遠端主機的路徑上探索最大傳輸單位 (MTU) 路徑。</span><span class="sxs-lookup"><span data-stu-id="334d4-544">If **TRUE**, the Maximum Transmission Unit (MTU) path is discovered over the path to a remote host.</span></span> <span data-ttu-id="334d4-545">藉由探索 MTU 路徑，並將 TCP 區段限制為此大小，TCP 可以在連接具有不同 Mtu 之網路的路徑中，排除路由器上的片段。</span><span class="sxs-lookup"><span data-stu-id="334d4-545">By discovering the MTU path and limiting TCP segments to this size, TCP can eliminate fragmentation at routers along the path that connect networks with different MTUs.</span></span> <span data-ttu-id="334d4-546">片段會對 TCP 輸送量和網路擁塞造成負面影響。</span><span class="sxs-lookup"><span data-stu-id="334d4-546">Fragmentation adversely affects TCP throughput and network congestion.</span></span> <span data-ttu-id="334d4-547">若將此參數設定為 **FALSE** ，則會將576個位元組的 MTU 用於非本機子網上電腦的所有連接。</span><span class="sxs-lookup"><span data-stu-id="334d4-547">Setting this parameter to **FALSE** causes an MTU of 576 bytes to be used for all connections that are not to machines on the local subnet.</span></span> <span data-ttu-id="334d4-548">預設值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="334d4-548">The default is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-549">**ServiceName**</span><span class="sxs-lookup"><span data-stu-id="334d4-549">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-550">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="334d4-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-551">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-551">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-552">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| ServiceName" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-552">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|ServiceName")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-553">網路介面卡的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="334d4-553">Service name of the network adapter.</span></span> <span data-ttu-id="334d4-554">這個名稱通常比完整的產品名稱短。</span><span class="sxs-lookup"><span data-stu-id="334d4-554">This name is usually shorter than the full product name.</span></span>

<span data-ttu-id="334d4-555">範例： "Elnkii"</span><span class="sxs-lookup"><span data-stu-id="334d4-555">Example: "Elnkii"</span></span>

</dd> <dt>

<span data-ttu-id="334d4-556">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="334d4-556">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-557">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="334d4-557">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-558">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-559">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="334d4-559">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="334d4-560">已知目前物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="334d4-560">Identifier by which the current object is known.</span></span>

<span data-ttu-id="334d4-561">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="334d4-561">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="334d4-562">**TcpipNetbiosOptions**</span><span class="sxs-lookup"><span data-stu-id="334d4-562">**TcpipNetbiosOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-563">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="334d4-563">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-564">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-564">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="334d4-565">NetBIOS over TCP/IP 相關可能設定的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="334d4-565">Bitmap of the possible settings related to NetBIOS over TCP/IP.</span></span> <span data-ttu-id="334d4-566">下列清單中會識別值。</span><span class="sxs-lookup"><span data-stu-id="334d4-566">Values are identified in the following list.</span></span>

<dt>

<span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>

<span data-ttu-id="334d4-567">**EnableNetbiosViaDhcp** (0) </span><span class="sxs-lookup"><span data-stu-id="334d4-567">**EnableNetbiosViaDhcp** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>

<span data-ttu-id="334d4-568">**EnableNetbios** (1) </span><span class="sxs-lookup"><span data-stu-id="334d4-568">**EnableNetbios** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>

<span data-ttu-id="334d4-569">**DisableNetbios** (2) </span><span class="sxs-lookup"><span data-stu-id="334d4-569">**DisableNetbios** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="334d4-570">**TcpMaxConnectRetransmissions**</span><span class="sxs-lookup"><span data-stu-id="334d4-570">**TcpMaxConnectRetransmissions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-571">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="334d4-571">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-572">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-573">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| TcpMaxConnectRetransmissions" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-573">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpMaxConnectRetransmissions")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-574">TCP 在終止連接之前嘗試重新傳輸連接要求的次數。</span><span class="sxs-lookup"><span data-stu-id="334d4-574">Number of times TCP attempts to retransmit a Connect Request before terminating the connection.</span></span> <span data-ttu-id="334d4-575">初始重新傳輸超時時間為3秒。</span><span class="sxs-lookup"><span data-stu-id="334d4-575">The initial retransmission timeout is 3 seconds.</span></span> <span data-ttu-id="334d4-576">每次嘗試的重新傳輸超時都會加倍。</span><span class="sxs-lookup"><span data-stu-id="334d4-576">The retransmission timeout doubles for each attempt.</span></span> <span data-ttu-id="334d4-577">預設值：3，有效範圍： 0-0xFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="334d4-577">Default: 3, Valid Range: 0 - 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-578">**TcpMaxDataRetransmissions**</span><span class="sxs-lookup"><span data-stu-id="334d4-578">**TcpMaxDataRetransmissions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-579">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="334d4-579">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-580">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-581">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| TcpMaxDataRetransmissions" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-581">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpMaxDataRetransmissions")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-582">在終止連接之前，TCP 重新傳輸個別資料區段 (nonconnect 區段) 的次數。</span><span class="sxs-lookup"><span data-stu-id="334d4-582">Number of times TCP retransmits an individual data segment (nonconnect segment) before terminating the connection.</span></span> <span data-ttu-id="334d4-583">重新傳輸超時會加倍，並在連線上每次重新傳輸。</span><span class="sxs-lookup"><span data-stu-id="334d4-583">The retransmission timeout doubles with each successive retransmission on a connection.</span></span> <span data-ttu-id="334d4-584">預設值：5，有效範圍： 0-0xFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="334d4-584">Default: 5, Valid Range: 0 - 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-585">**TcpNumConnections**</span><span class="sxs-lookup"><span data-stu-id="334d4-585">**TcpNumConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-586">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="334d4-586">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-587">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-587">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-588">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| TcpNumConnections" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-588">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpNumConnections")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-589">TCP 可以同時開啟的最大連接數目。</span><span class="sxs-lookup"><span data-stu-id="334d4-589">Maximum number of connections that TCP can have open simultaneously.</span></span> <span data-ttu-id="334d4-590">預設值：0xFFFFFE，有效範圍： 0-0xFFFFFE。</span><span class="sxs-lookup"><span data-stu-id="334d4-590">Default: 0xFFFFFE, Valid Range: 0 - 0xFFFFFE.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-591">**TcpUseRFC1122UrgentPointer**</span><span class="sxs-lookup"><span data-stu-id="334d4-591">**TcpUseRFC1122UrgentPointer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-592">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="334d4-592">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-593">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-593">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-594">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| TcpUseRFC1122UrgentPointer" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-594">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpUseRFC1122UrgentPointer")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-595">若 **為 TRUE**，TCP 會使用 RFC 1122 規格來進行緊急資料。</span><span class="sxs-lookup"><span data-stu-id="334d4-595">If **TRUE**, TCP uses the RFC 1122 specification for urgent data.</span></span> <span data-ttu-id="334d4-596">如果 **為 FALSE** (預設) ，TCP 會使用 Berkeley Software DESIGN (BSD) 衍生系統所使用的模式。</span><span class="sxs-lookup"><span data-stu-id="334d4-596">If **FALSE** (default), TCP uses the mode used by Berkeley Software Design (BSD) derived systems.</span></span> <span data-ttu-id="334d4-597">這兩種機制會以不同方式解讀緊急指標，而且無法互通。</span><span class="sxs-lookup"><span data-stu-id="334d4-597">The two mechanisms interpret the urgent pointer differently and are not interoperable.</span></span> <span data-ttu-id="334d4-598">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="334d4-598">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-599">**TcpWindowSize**</span><span class="sxs-lookup"><span data-stu-id="334d4-599">**TcpWindowSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-600">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="334d4-600">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-601">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-601">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-602">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| TcpWindowSize" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-602">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpWindowSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-603">系統提供的 TCP 接收視窗大小上限。</span><span class="sxs-lookup"><span data-stu-id="334d4-603">Maximum TCP Receive Window size offered by the system.</span></span> <span data-ttu-id="334d4-604">接收視窗會指定傳送者在未收到通知的情況下，可能會傳送的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="334d4-604">The Receive Window specifies the number of bytes a sender may transmit without receiving an acknowledgment.</span></span> <span data-ttu-id="334d4-605">一般而言，較大的接收視窗會透過高延遲和高頻寬的網路來提升效能。</span><span class="sxs-lookup"><span data-stu-id="334d4-605">In general, larger receiving windows will improve performance over high-delay and high-bandwidth networks.</span></span> <span data-ttu-id="334d4-606">為了提高效率，接收視窗應該是 (MSS) 的 TCP 最大區段大小的倍數。</span><span class="sxs-lookup"><span data-stu-id="334d4-606">For efficiency, the receiving window should be an even multiple of the TCP Maximum Segment Size (MSS).</span></span> <span data-ttu-id="334d4-607">預設值： TCP 資料大小上限的四倍，或是最大的 TCP 資料大小的倍數，舍入到最接近的8192倍數。</span><span class="sxs-lookup"><span data-stu-id="334d4-607">Default: Four times the maximum TCP data size or an even multiple of TCP data size rounded up to the nearest multiple of 8192.</span></span> <span data-ttu-id="334d4-608">Ethernet 網路預設為8760。</span><span class="sxs-lookup"><span data-stu-id="334d4-608">Ethernet networks default to 8760.</span></span> <span data-ttu-id="334d4-609">有效範圍： 0-65535。</span><span class="sxs-lookup"><span data-stu-id="334d4-609">Valid range: 0 - 65535.</span></span>

> [!Note]  
> <span data-ttu-id="334d4-610">Windows Vista：此屬性會存取 `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` 登錄專案，此專案不會用於目前的作業系統執行。</span><span class="sxs-lookup"><span data-stu-id="334d4-610">Windows Vista: This property accesses the `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` registry entry, which is not used in the current implementation of the operating system.</span></span>

 

</dd> <dt>

<span data-ttu-id="334d4-611">**WINSEnableLMHostsLookup**</span><span class="sxs-lookup"><span data-stu-id="334d4-611">**WINSEnableLMHostsLookup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-612">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="334d4-612">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-613">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-613">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-614">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| EnableLMHOSTS" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-614">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnableLMHOSTS")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-615">若 **為 TRUE**，則會使用本機查閱檔案。</span><span class="sxs-lookup"><span data-stu-id="334d4-615">If **TRUE**, local lookup files are used.</span></span> <span data-ttu-id="334d4-616">查閱檔案將包含 IP 位址與主機名稱的對應。</span><span class="sxs-lookup"><span data-stu-id="334d4-616">Lookup files will contain a map of IP addresses to host names.</span></span> <span data-ttu-id="334d4-617">如果它們存在於本機系統上，則會在% SystemRoot% \\ system32 \\ 驅動程式等中找到 \\ 。</span><span class="sxs-lookup"><span data-stu-id="334d4-617">If they exist on the local system, they will be found in %SystemRoot%\\system32\\drivers\\etc.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-618">**WINSHostLookupFile**</span><span class="sxs-lookup"><span data-stu-id="334d4-618">**WINSHostLookupFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-619">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="334d4-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-620">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-620">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-621">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 系統資訊函式 \| [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) \| \\ \\ 驅動程式 \\ \\ 等 \\ \\ lmhosts" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-621">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions\|[**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)\|\\\\drivers\\\\etc\\\\lmhosts")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-622">本機系統上 WINS 查閱檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="334d4-622">Path to a WINS lookup file on the local system.</span></span> <span data-ttu-id="334d4-623">此檔案會包含主機名稱的 IP 位址對應。</span><span class="sxs-lookup"><span data-stu-id="334d4-623">This file will contain a map of IP addresses to host names.</span></span> <span data-ttu-id="334d4-624">如果找到這個屬性中指定的檔案，則會將它複製到本機系統的% SystemRoot% \\ system32 \\ 驅動程式 \\ 等資料夾。</span><span class="sxs-lookup"><span data-stu-id="334d4-624">If the file specified in this property is found, it will be copied to the %SystemRoot%\\system32\\drivers\\etc folder of the local system.</span></span> <span data-ttu-id="334d4-625">只有在 **WINSEnableLMHostsLookup** 屬性為 **TRUE** 時才有效。</span><span class="sxs-lookup"><span data-stu-id="334d4-625">Valid only if the **WINSEnableLMHostsLookup** property is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-626">**WINSPrimaryServer**</span><span class="sxs-lookup"><span data-stu-id="334d4-626">**WINSPrimaryServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-627">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="334d4-627">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-628">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-628">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-629">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device Input and Output 函數 \| DeviceIoControl" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-629">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-630">主要 WINS 伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="334d4-630">IP address for the primary WINS server.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-631">**WINSScopeID**</span><span class="sxs-lookup"><span data-stu-id="334d4-631">**WINSScopeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-632">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="334d4-632">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-633">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-633">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-634">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| ScopeID" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-634">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ScopeID")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-635">附加至 NetBIOS 名稱結尾的值，可隔離一組電腦系統彼此通訊。</span><span class="sxs-lookup"><span data-stu-id="334d4-635">Value appended to the end of the NetBIOS name that isolates a group of computer systems communicating with only each other.</span></span> <span data-ttu-id="334d4-636">它可用於所有透過 TCP/IP 通訊的電腦系統的 NetBIOS 交易。</span><span class="sxs-lookup"><span data-stu-id="334d4-636">It is used for all NetBIOS transactions over TCP/IP communications from that computer system.</span></span> <span data-ttu-id="334d4-637">使用相同的範圍識別碼設定的電腦可以與這部電腦通訊。</span><span class="sxs-lookup"><span data-stu-id="334d4-637">Computers configured with identical scope identifiers are able to communicate with this computer.</span></span> <span data-ttu-id="334d4-638">具有不同範圍識別碼的 TCP/IP 用戶端會忽略來自具有此範圍識別碼之電腦的封包。</span><span class="sxs-lookup"><span data-stu-id="334d4-638">TCP/IP clients with different scope identifiers disregard packets from computers with this scope identifier.</span></span> <span data-ttu-id="334d4-639">只有在 [**>enablewins**](enablewins-method-in-class-win32-networkadapterconfiguration.md) 方法執行成功時才有效。</span><span class="sxs-lookup"><span data-stu-id="334d4-639">Valid only when the [**EnableWINS**](enablewins-method-in-class-win32-networkadapterconfiguration.md) method executes successfully.</span></span>

</dd> <dt>

<span data-ttu-id="334d4-640">**WINSSecondaryServer**</span><span class="sxs-lookup"><span data-stu-id="334d4-640">**WINSSecondaryServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="334d4-641">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="334d4-641">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="334d4-642">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="334d4-642">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="334d4-643">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device Input and Output 函數 \| DeviceIoControl" ) </span><span class="sxs-lookup"><span data-stu-id="334d4-643">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="334d4-644">次要 WINS 伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="334d4-644">IP address for the secondary WINS server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="334d4-645">備註</span><span class="sxs-lookup"><span data-stu-id="334d4-645">Remarks</span></span>

<span data-ttu-id="334d4-646">**Win32 \_ >networkadapterconfiguration** 類別衍生自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="334d4-646">The **Win32\_NetworkAdapterConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="examples"></a><span data-ttu-id="334d4-647">範例</span><span class="sxs-lookup"><span data-stu-id="334d4-647">Examples</span></span>

<span data-ttu-id="334d4-648">TechNet 資源庫上的 [WMI 資訊](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) 取回程序 VBScript 程式碼範例會使用 **Win32 \_ >networkadapterconfiguration** 類別，從多部遠端電腦抓取網路設定資訊。</span><span class="sxs-lookup"><span data-stu-id="334d4-648">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_NetworkAdapterConfiguration** class to retrieve network configuration information from a number of remote computers.</span></span>

<span data-ttu-id="334d4-649">[本機/遠端電腦上的 Get-computerinfo 查詢電腦資訊（ (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell 範例（英文）： TechNet 資源庫上的 PowerShell 範例會使用一些硬體和軟體的呼叫，包括 **Win32 \_ >networkadapterconfiguration**，以顯示本機或遠端系統的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="334d4-649">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_NetworkAdapterConfiguration**, to display information about a local or remote system.</span></span>

<span data-ttu-id="334d4-650">下列 PowerShell 程式碼會抓取 Microsoft ISTAP Adapter 的設定。</span><span class="sxs-lookup"><span data-stu-id="334d4-650">The following PowerShell code retrieves the configuration settings for the Microsoft ISTAP Adapter.</span></span>


```PowerShell
$IstapAdapterConfig = Get-WmiObject Win32_NetworkAdapterConfiguration | Where-Object {$_.Description -eq "Microsoft ISATAP Adapter"}
$IstapAdapterConfig
```



<span data-ttu-id="334d4-651">下列 C 範例會抓取 \# 所有網路介面卡設定實例的描述和索引編號。</span><span class="sxs-lookup"><span data-stu-id="334d4-651">The following C\# sample retrieves the description and index number of all network adapter configuration instances.</span></span> <span data-ttu-id="334d4-652">請注意，此 C \# 範例使用的是 [管理基礎結構](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) 命名空間，其通常會比 [管理](/dotnet/api/system.management) 命名空間 WMI 類別更有效率地進行調整。</span><span class="sxs-lookup"><span data-stu-id="334d4-652">Note that this C\# sample uses the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace, which generally scales more efficiently than the [System.Management](/dotnet/api/system.management) namespace WMI classes.</span></span>


```CSharp
using Microsoft.Management.Infrastructure;
...
static void QueryInstanceFunc()
{
   CimSession session = CimSession.Create("localHost");
   IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_NetworkAdapterConfiguration");

   foreach (CimInstance cimObj in queryInstance)
   {
      Console.WriteLine(cimObj.CimInstanceProperties["Index"].ToString());
      Console.WriteLine(cimObj.CimInstanceProperties["Description"].ToString());
      Console.WriteLine();
   }

Console.ReadLine();
}
```



<span data-ttu-id="334d4-653">下列 C 範例會抓取 \# 所有網路介面卡設定實例的描述和索引編號。</span><span class="sxs-lookup"><span data-stu-id="334d4-653">The following C\# sample retrieves the description and index number of all network adapter configuration instances.</span></span> <span data-ttu-id="334d4-654">請注意，此 C \# 範例會使用由[Microsoft](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))所取代的原始[管理](/dotnet/api/system.management)命名空間。</span><span class="sxs-lookup"><span data-stu-id="334d4-654">Note that this C\# sample uses the original [System.Management](/dotnet/api/system.management) namespace, which has been superceded by [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)).</span></span>


```CSharp
using System.Management;
...
static void oldSchoolQueryInstanceFunc()
{

   ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_NetworkAdapterConfiguration");
   ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);

   ManagementObjectCollection queryCollection = searcher.Get();
   foreach (ManagementObject m in queryCollection)
   {
      Console.WriteLine("Index : {0}", m["Index"]);
      Console.WriteLine("Description : {0}", m["Description"]);
      Console.WriteLine();
   }
   Console.ReadLine();
}
```



<span data-ttu-id="334d4-655">下列範例會從 **Win32 \_ >networkadapterconfiguration** 類別中取出資訊。</span><span class="sxs-lookup"><span data-stu-id="334d4-655">The following example retrieves information from the **Win32\_NetworkAdapterConfiguration** class.</span></span>


```VB
on error resume next


PrintAll_NICAdapter_information()

'PrintOnlyEnabled_NICAdapter_information()


Function PrintAll_NICAdapter_information()


    strComputer = "."

    Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2")


    Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_NetworkAdapterConfiguration",,48)


    i = 0

    For Each objItem in colItems

        i = i + 1

        Wscript.Echo "-----------------------------------"

        Wscript.Echo "Win32_NetworkAdapterConfiguration instance: " & i

        Wscript.Echo "-----------------------------------"

        

        strDefaultIPGateway = GetMultiString_FromArray(objitem.DefaultIPGateway, ", ")

        Wscript.Echo "MACAddress                  : " & vbtab & objItem.MACAddress
        Wscript.Echo "Description                 : " & vbtab & objItem.Description
        Wscript.Echo "DHCPEnabled                 : " & vbtab & objItem.DHCPEnabled

        strIPAddress=GetMultiString_FromArray(objitem.IPAddress, ", ")

        Wscript.Echo "IPAddress                   : " & vbtab & strIPAddress

        strIPSubnet = GetMultiString_FromArray(objitem.IPSubnet, ", ")

        Wscript.Echo "IPSubnet                    : " & vbtab & strIPSubnet
        Wscript.Echo "IPConnectionMetric          : " & vbtab & objItem.IPConnectionMetric
        Wscript.Echo "DHCPLeaseExpires            : " & vbtab & objItem.DHCPLeaseExpires
        Wscript.Echo "DHCPLeaseObtained           : " & vbtab & objItem.DHCPLeaseObtained
        Wscript.Echo "DHCPServer                  : " & vbtab & objItem.DHCPServer
        Wscript.Echo "DNSDomain                   : " & vbtab & objItem.DNSDomain
        Wscript.Echo "IPEnabled                   : " & vbtab & objItem.IPEnabled
        Wscript.Echo "DefaultIPGateway            : " & vbtab & strDefaultIPGateway
        Wscript.Echo "GatewayCostMetric           : " & vbtab & strGatewayCostMetric
        Wscript.Echo "IPFilterSecurityEnabled     : " & vbtab & objItem.IPFilterSecurityEnabled
        Wscript.Echo "IPPortSecurityEnabled       : " & vbtab & objItem.IPPortSecurityEnabled

        strDNSDomainSuffixSearchOrder = GetMultiString_FromArray(objitem.DNSDomainSuffixSearchOrder, ", ")

        Wscript.Echo "DNSDomainSuffixSearchOrder  : " & vbtab & strDNSDomainSuffixSearchOrder
        Wscript.Echo "DNSEnabledForWINSResolution : " & vbtab & objItem.DNSEnabledForWINSResolution
        Wscript.Echo "DNSHostName                 : " & vbtab & objItem.DNSHostName

        

        strDNSServerSearchOrder = GetMultiString_FromArray(objitem.DNSServerSearchOrder, ", ")

        Wscript.Echo "DNSServerSearchOrder        : " & vbtab & strDNSServerSearchOrder
        Wscript.Echo "DomainDNSRegistrationEnabled: " & vbtab & objItem.DomainDNSRegistrationEnabled
        Wscript.Echo "ForwardBufferMemory         : " & vbtab & objItem.ForwardBufferMemory
        Wscript.Echo "FullDNSRegistrationEnabled  : " & vbtab & objItem.FullDNSRegistrationEnabled

        strGatewayCostMetric = GetMultiString_FromArray(objitem.GatewayCostMetric, ", ")

        Wscript.Echo "IGMPLevel                   : " & vbtab & objItem.IGMPLevel
        Wscript.Echo "Index                       : " & vbtab & objItem.Index

        strIPSecPermitIPProtocols = GetMultiString_FromArray(objitem.IPSecPermitIPProtocols, ", ")

        Wscript.Echo "IPSecPermitIPProtocols      : " & vbtab & strIPSecPermitIPProtocols


        strIPSecPermitTCPPorts =GetMultiString_FromArray(objitem.IPSecPermitTCPPorts, ", ")

        Wscript.Echo "IPSecPermitTCPPorts         : " & vbtab & strIPSecPermitTCPPorts


        strIPSecPermitUDPPorts = GetMultiString_FromArray(objitem.IPSecPermitUDPPorts, ", ")

        Wscript.Echo "IPSecPermitUDPPorts         : " & vbtab & strIPSecPermitUDPPorts


        Wscript.Echo "IPUseZeroBroadcast          : " & vbtab & objItem.IPUseZeroBroadcast
        Wscript.Echo "IPXAddress                  : " & vbtab & objItem.IPXAddress
        Wscript.Echo "IPXEnabled                  : " & vbtab & objItem.IPXEnabled

        strIPXFrameType=GetMultiString_FromArray(objitem.IPXFrameType, ", ")

        Wscript.Echo "IPXFrameType                : " & vbtab & strIPXFrameType


        strIPXNetworkNumber=GetMultiString_FromArray(objitem.IPXNetworkNumber, ", ")

        Wscript.Echo "IPXNetworkNumber            : " & vbtab & strIPXNetworkNumber
        Wscript.Echo "IPXVirtualNetNumber         : " & vbtab & objItem.IPXVirtualNetNumber
        Wscript.Echo "KeepAliveInterval           : " & vbtab & objItem.KeepAliveInterval

        Wscript.Echo "KeepAliveTime               : " & vbtab & objItem.KeepAliveTime
        Wscript.Echo "MTU                         : " & vbtab & objItem.MTU
        Wscript.Echo "NumForwardPackets           : " & vbtab & objItem.NumForwardPackets
        Wscript.Echo "PMTUBHDetectEnabled         : " & vbtab & objItem.PMTUBHDetectEnabled
        Wscript.Echo "PMTUDiscoveryEnabled        : " & vbtab & objItem.PMTUDiscoveryEnabled
        Wscript.Echo "ServiceName                 : " & vbtab & objItem.ServiceName
        Wscript.Echo "SettingID                   : " & vbtab & objItem.SettingID
        Wscript.Echo "TcpipNetbiosOptions         : " & vbtab & objItem.TcpipNetbiosOptions
        Wscript.Echo "TcpMaxConnectRetransmissions: " & vbtab & objItem.TcpMaxConnectRetransmissions
        Wscript.Echo "TcpMaxDataRetransmissions   : " & vbtab & objItem.TcpMaxDataRetransmissions
        Wscript.Echo "TcpNumConnections           : " & vbtab & objItem.TcpNumConnections
        Wscript.Echo "TcpUseRFC1122UrgentPointer  : " & vbtab & objItem.TcpUseRFC1122UrgentPointer
        Wscript.Echo "TcpWindowSize               : " & vbtab & objItem.TcpWindowSize
        Wscript.Echo "WINSEnableLMHostsLookup     : " & vbtab & objItem.WINSEnableLMHostsLookup
        Wscript.Echo "WINSHostLookupFile          : " & vbtab & objItem.WINSHostLookupFile
        Wscript.Echo "WINSPrimaryServer           : " & vbtab & objItem.WINSPrimaryServer
        Wscript.Echo "WINSScopeID                 : " & vbtab & objItem.WINSScopeID
        Wscript.Echo "WINSSecondaryServer         : " & vbtab & objItem.WINSSecondaryServer
        Wscript.Echo "ArpAlwaysSourceRoute        : " & vbtab & objItem.ArpAlwaysSourceRoute
        Wscript.Echo "ArpUseEtherSNAP             : " & vbtab & objItem.ArpUseEtherSNAP
        Wscript.Echo "DatabasePath                : " & vbtab & objItem.DatabasePath
        Wscript.Echo "DeadGWDetectEnabled         : " & vbtab & objItem.DeadGWDetectEnabled

        Wscript.Echo "DefaultTOS                  : " & vbtab & objItem.DefaultTOS
        Wscript.Echo "DefaultTTL                  : " & vbtab & objItem.DefaultTTL

        

    Next

End Function ' Function PrintAll_NICAdapter_information()


' Script to get comprehensive nic info

sub appendCollection(msg, colctn, nm)

    i=0
    for each t in colctn
        msg = msg & "nic." & nm & "["&i&"]: " & t & vbCRLF
        i = i + 1
    next
end sub


Function PrintOnlyEnabled_NICAdapter_information()

    strComputer = "."

    Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
    Set colNicConfigs = objWMIService.ExecQuery ("SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled = True")


    for each nic in colNicConfigs

        msg = "nic.ArpAlwaysSourceRoute: " & nic.ArpAlwaysSourceRoute & vbCRLF _
        & "nic.ArpUseEtherSNAP: " & nic.ArpUseEtherSNAP & vbCRLF _
        & "nic.Caption: " & nic.Caption & vbCRLF _
        & "nic.DatabasePath: " & nic.DatabasePath & vbCRLF _
        & "nic.DeadGWDetectEnabled: " & nic.DeadGWDetectEnabled & vbCRLF _
        & "nic.DefaultTOS: " & nic.DefaultTOS & vbCRLF _
        & "nic.DefaultTTL: " & nic.DefaultTTL & vbCRLF _
        & "nic.Description: " & nic.Description & vbCRLF _
        & "nic.DHCPEnabled: " & nic.DHCPEnabled & vbCRLF _
        & "nic.DHCPLeaseExpires: " & nic.DHCPLeaseExpires & vbCRLF _
        & "nic.DHCPLeaseObtained: " & nic.DHCPLeaseObtained & vbCRLF _
        & "nic.DHCPServer: " & nic.DHCPServer & vbCRLF _
        & "nic.DNSDomain: " & nic.DNSDomain & vbCRLF _
        & "nic.DNSEnabledForWINSResolution: " & nic.DNSEnabledForWINSResolution & vbCRLF _
        & "nic.DNSHostName: " & nic.DNSHostName & vbCRLF _
        & "nic.DomainDNSRegistrationEnabled: " & nic.DomainDNSRegistrationEnabled & vbCRLF _
        & "nic.DNSDomainSuffixSearchOrder: " & nic.DNSDomainSuffixSearchOrder & vbCRLF _
        & "nic.ForwardBufferMemory: " & nic.ForwardBufferMemory & vbCRLF _
        & "nic.FullDNSRegistrationEnabled: " & nic.FullDNSRegistrationEnabled & vbCRLF _
        & "nic.IGMPLevel: " & nic.IGMPLevel & vbCRLF _
        & "nic.Index: " & nic.Index & vbCRLF _
        & "nic.IPConnectionMetric: " & nic.IPConnectionMetric & vbCRLF _
        & "nic.IPEnabled: " & nic.IPEnabled & vbCRLF _
        & "nic.IPFilterSecurityEnabled: " & nic.IPFilterSecurityEnabled & vbCRLF _
        & "nic.IPPortSecurityEnabled: " & nic.IPPortSecurityEnabled & vbCRLF _
        & "nic.IPUseZeroBroadcast: " & nic.IPUseZeroBroadcast & vbCRLF _
        & "nic.IPXAddress: " & nic.IPXAddress & vbCRLF _
        & "nic.IPXEnabled: " & nic.IPXEnabled & vbCRLF _
        & "nic.IPXFrameType: " & nic.IPXFrameType & vbCRLF _
        & "nic.IPXMediaType: " & nic.IPXMediaType & vbCRLF _
        & "nic.IPXNetworkNumber: " & nic.IPXNetworkNumber & vbCRLF _
        & "nic.IPXVirtualNetNumber: " & nic.IPXVirtualNetNumber & vbCRLF _
        & "nic.KeepAliveInterval: " & nic.KeepAliveInterval & vbCRLF _
        & "nic.KeepAliveTime: " & nic.KeepAliveTime & vbCRLF _
        & "nic.MACAddress: " & nic.MACAddress & vbCRLF _
        & "nic.MTU: " & nic.MTU & vbCRLF _
        & "nic.NumForwardPackets: " & nic.NumForwardPackets & vbCRLF _
        & "nic.PMTUBHDetectEnabled: " & nic.PMTUBHDetectEnabled & vbCRLF _
        & "nic.PMTUDiscoveryEnabled: " & nic.PMTUDiscoveryEnabled & vbCRLF _
        & "nic.ServiceName: " & nic.ServiceName & vbCRLF _
        & "nic.SettingID: " & nic.SettingID & vbCRLF _
        & "nic.TcpipNetbiosOptions: " & nic.TcpipNetbiosOptions & vbCRLF _
        & "nic.TcpMaxConnectRetransmissions: " & nic.TcpMaxConnectRetransmissions & vbCRLF _
        & "nic.TcpMaxDataRetransmissions: " & nic.TcpMaxDataRetransmissions & vbCRLF _
        & "nic.TcpNumConnections: " & nic.TcpNumConnections & vbCRLF _
        & "nic.TcpUseRFC1122UrgentPointer: " & nic.TcpUseRFC1122UrgentPointer & vbCRLF _
        & "nic.TcpWindowSize: " & nic.TcpWindowSize & vbCRLF _
        & "nic.WINSEnableLMHostsLookup: " & nic.WINSEnableLMHostsLookup & vbCRLF _
        & "nic.WINSHostLookupFile: " & nic.WINSHostLookupFile & vbCRLF _
        & "nic.WINSPrimaryServer: " & nic.WINSPrimaryServer & vbCRLF _
        & "nic.WINSScopeID: " & nic.WINSScopeID & vbCRLF _
        & "nic.WINSSecondaryServer: " & nic.WINSSecondaryServer & vbCRLF _
        '& "nic.InterfaceIndex: " & "|"&nic.InterfaceIndex & vbCRLF _


        appendCollection msg, nic.DefaultIPGateway, "DefaultIPGateway"
        appendCollection msg, nic.DNSServerSearchOrder, "DNSServerSearchOrder"
        appendCollection msg, nic.GatewayCostMetric, "GatewayCostMetric"
        appendCollection msg, nic.IPAddress, "IPAddress"
        appendCollection msg, nic.IPSecPermitIPProtocols, "IPSecPermitIPProtocols"
        appendCollection msg, nic.IPSecPermitTCPPorts, "IPSecPermitTCPPorts"
        appendCollection msg, nic.IPSecPermitUDPPorts, "IPSecPermitUDPPorts"
        appendCollection msg, nic.IPSubnet, "IPSubnet"


        WScript.Echo msg

    next


    'Vista only code???

    'Set colAdapters = objWMIService.Execquery ("SELECT * FROM Win32_NetworkAdapter WHERE NetEnabled = True")

    'For Each nic in colAdapters

    ' msg = "nic.DeviceId: " & nic.DeviceId & vbCRLF _

    ' & "nic.Name: " & nic.Name & vbCRLF _

    '

    'Next

End Function 'Function PrintOnlyEnabled_NICAdapter_information()

Function GetMultiString_FromArray( ArrayString, Seprator)

    If IsNull ( ArrayString ) Then

        StrMultiArray = ArrayString

    else

        StrMultiArray = Join( ArrayString, Seprator )

   end if

   GetMultiString_FromArray = StrMultiArray

End Function
```



## <a name="requirements"></a><span data-ttu-id="334d4-656">規格需求</span><span class="sxs-lookup"><span data-stu-id="334d4-656">Requirements</span></span>



| <span data-ttu-id="334d4-657">需求</span><span class="sxs-lookup"><span data-stu-id="334d4-657">Requirement</span></span> | <span data-ttu-id="334d4-658">值</span><span class="sxs-lookup"><span data-stu-id="334d4-658">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="334d4-659">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="334d4-659">Minimum supported client</span></span><br/> | <span data-ttu-id="334d4-660">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="334d4-660">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="334d4-661">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="334d4-661">Minimum supported server</span></span><br/> | <span data-ttu-id="334d4-662">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="334d4-662">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="334d4-663">命名空間</span><span class="sxs-lookup"><span data-stu-id="334d4-663">Namespace</span></span><br/>                | <span data-ttu-id="334d4-664">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="334d4-664">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="334d4-665">MOF</span><span class="sxs-lookup"><span data-stu-id="334d4-665">MOF</span></span><br/>                      | <dl> <span data-ttu-id="334d4-666"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="334d4-666"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="334d4-667">DLL</span><span class="sxs-lookup"><span data-stu-id="334d4-667">DLL</span></span><br/>                      | <dl> <span data-ttu-id="334d4-668"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="334d4-668"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="334d4-669">另請參閱</span><span class="sxs-lookup"><span data-stu-id="334d4-669">See also</span></span>

<dl> <dt>

[<span data-ttu-id="334d4-670">**CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="334d4-670">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="334d4-671">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="334d4-671">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="334d4-672">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="334d4-672">WMI Tasks: Networking</span></span>](../wmisdk/wmi-tasks--networking.md)
</dt> <dt>

[<span data-ttu-id="334d4-673">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="334d4-673">WMI Tasks: Accounts and Domains</span></span>](../wmisdk/wmi-tasks--accounts-and-domains.md)
</dt> <dt>

[<span data-ttu-id="334d4-674">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="334d4-674">IPv6 and IPv4 Support in WMI</span></span>](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
