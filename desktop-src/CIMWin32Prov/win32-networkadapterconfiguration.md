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
ms.openlocfilehash: e93ae76ae3c4880c7ad041e6e90d39f1b22820d3
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153571"
---
# <a name="win32_networkadapterconfiguration-class"></a>Win32 \_ >networkadapterconfiguration 類別

**Win32 \_ >networkadapterconfiguration** [WMI 類別](../wmisdk/retrieving-a-class.md)代表網路介面卡的屬性和行為。 此類別包含額外的屬性和方法，可支援與網路介面卡無關的 TCP/IP 通訊協定管理。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

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

## <a name="members"></a>成員

**Win32 \_ >networkadapterconfiguration** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ >networkadapterconfiguration** 類別具有這些方法。



| 方法                                                                                                                       | 描述                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DisableIPSec**](disableipsec-method-in-class-win32-networkadapterconfiguration.md)                                       | 停用此啟用 TCP/IP 的網路介面卡上的 IPsec。<br/>                                                                                     |
| [**EnableDHCP**](enabledhcp-method-in-class-win32-networkadapterconfiguration.md)                                           | 使用此網路介面卡啟用動態主機設定通訊協定 (DHCP) 的服務。<br/>                                              |
| [**EnableDNS**](enabledns-method-in-class-win32-networkadapterconfiguration.md)                                             | 針對此 TCP/IP 系結網路介面卡上的服務，啟用網域名稱系統 (DNS) 。<br/>                                                     |
| [**EnableIPFilterSec**](enableipfiltersec-method-in-class-win32-networkadapterconfiguration.md)                             | 在所有 IP 系結的網路介面卡上全域啟用 IPsec。<br/>                                                                               |
| [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md)                                         | 在啟用此特定 TCP/IP 的網路介面卡上啟用 IPsec。<br/>                                                                             |
| [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md)                                       | 啟用目標網路介面卡的靜態 TCP/IP 定址。<br/>                                                                           |
| [**>enablewins**](enablewins-method-in-class-win32-networkadapterconfiguration.md)                                           | 啟用 TCP/IP 專屬的 WINS 設定，但與網路介面卡無關。<br/>                                                          |
| [**ReleaseDHCPLease**](releasedhcplease-method-in-class-win32-networkadapterconfiguration.md)                               | 釋放系結至已啟用 DHCP 之特定網路介面卡的 IP 位址。<br/>                                                                  |
| [**>releasedhcpleaseall**](releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                         | 釋放系結至所有啟用 DHCP 之網路介面卡的 IP 位址。<br/>                                                                      |
| [**RenewDHCPLease**](renewdhcplease-method-in-class-win32-networkadapterconfiguration.md)                                   | 更新已啟用 DHCP 的特定網路介面卡上的 IP 位址。<br/>                                                                           |
| [**RenewDHCPLeaseAll**](renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                             | 在所有已啟用 DHCP 的網路介面卡上，更新 IP 位址。<br/>                                                                              |
| [**SetArpAlwaysSourceRoute**](setarpalwayssourceroute-method-in-class-win32-networkadapterconfiguration.md)                 | 依 TCP/IP 設定 ARP 查詢的傳輸。<br/>                                                                                        |
| [**SetArpUseEtherSNAP**](setarpuseethersnap-method-in-class-win32-networkadapterconfiguration.md)                           | 讓乙太網路封包使用802.3 貼齊編碼。<br/>                                                                                       |
| [**SetDatabasePath**](setdatabasepath-method-in-class-win32-networkadapterconfiguration.md)                                 | 設定)  (主機、LMHOSTS、網路和通訊協定之標準網際網路資料庫檔案的路徑。<br/>                                           |
| [**SetDeadGWDetect**](setdeadgwdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | 啟用死閘道偵測。<br/>                                                                                                            |
| [**SetDefaultTOS**](setdefaulttos-method-in-class-win32-networkadapterconfiguration.md)                                     | 已過時。 這個方法會在連出 IP 封包的標頭中，設定服務 (TOS) 值的預設類型。<br/>                                   |
| [**SetDefaultTTL**](setdefaultttl-method-in-class-win32-networkadapterconfiguration.md)                                     | 設定傳出 IP 封包標頭中 (TTL) 值的預設存留時間。<br/>                                                            |
| [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)                                       | 設定 DNS 網域。<br/>                                                                                                                       |
| [**SetDNSServerSearchOrder**](setdnsserversearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | 將伺服器搜尋順序設定為元素陣列。<br/>                                                                                      |
| [**SetDNSSuffixSearchOrder**](setdnssuffixsearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | 將尾碼搜尋順序設定為元素陣列。<br/>                                                                                      |
| [**SetDynamicDNSRegistration**](setdynamicdnsregistration-method-in-class-win32-networkadapterconfiguration.md)             | 指出此 IP 系結介面卡的 IP 位址動態 DNS 註冊。<br/>                                                              |
| [**SetForwardBufferMemory**](setforwardbuffermemory-method-in-class-win32-networkadapterconfiguration.md)                   | 指定要將封包資料儲存在路由器封包佇列中的記憶體 IP 分配數量。<br/>                                                    |
| [**SetGateways**](setgateways-method-in-class-win32-networkadapterconfiguration.md)                                         | 指定閘道清單，以路由傳送至與此介面卡所連接的子網不同的子網的封包。<br/>                |
| [**SetIGMPLevel**](setigmplevel-method-in-class-win32-networkadapterconfiguration.md)                                       | 設定系統支援 IP 多播並參與網際網路群組管理通訊協定的範圍。<br/>                   |
| [**SetIPConnectionMetric**](setipconnectionmetric-method-in-class-win32-networkadapterconfiguration.md)                     | 設定與此 IP 系結介面卡相關聯的路由度量。<br/>                                                                             |
| [**SetIPUseZeroBroadcast**](setipusezerobroadcast-method-in-class-win32-networkadapterconfiguration.md)                     | 設定 IP 零廣播使用方式。<br/>                                                                                                              |
| [**SetIPXFrameTypeNetworkPairs**](win32-networkadapterconfiguration-setipxframetypenetworkpairs.md)                         | 為此網路介面卡) 網路編號/框架組，設定網路封包交換 (。<br/>                                            |
| [**SetIPXVirtualNetworkNumber**](win32-networkadapterconfiguration-setipxvirtualnetworknumber.md)                           | 設定目的電腦系統上的封包交換 (IPX) 虛擬網路編號。<br/>                                       |
| [**SetKeepAliveInterval**](setkeepaliveinterval-method-in-class-win32-networkadapterconfiguration.md)                       | 設定分隔保持運作的間隔，直到收到回應為止。<br/>                                                      |
| [**SetKeepAliveTime**](setkeepalivetime-method-in-class-win32-networkadapterconfiguration.md)                               | 藉由傳送 Keep-alive 封包，設定 TCP 嘗試驗證閒置連線是否仍可供使用的頻率。<br/>                           |
| [**SetMTU**](setmtu-method-in-class-win32-networkadapterconfiguration.md)                                                   | 設定網路介面 (MTU) 的預設最大傳輸單位。<br/> 不支援這個方法。<br/>                         |
| [**SetNumForwardPackets**](setnumforwardpackets-method-in-class-win32-networkadapterconfiguration.md)                       | 設定為路由器封包佇列配置的 IP 封包標頭數目。<br/>                                                                |
| [**SetPMTUBHDetect**](setpmtubhdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | 啟用對黑洞路由器的偵測。<br/>                                                                                                   |
| [**SetPMTUDiscovery**](setpmtudiscovery-method-in-class-win32-networkadapterconfiguration.md)                               | 啟用 (MTU) 探索的最大傳輸單位。<br/>                                                                                         |
| [**SetTcpipNetbios**](settcpipnetbios-method-in-class-win32-networkadapterconfiguration.md)                                 | 設定 NetBIOS over TCP/IP 的預設運算。<br/>                                                                                         |
| [**SetTcpMaxConnectRetransmissions**](settcpmaxconnectretransmissions-method-in-class-win32-networkadapterconfiguration.md) | 設定在中止之前 TCP 將會重新傳輸連接要求的次數。<br/>                                                         |
| [**SetTcpMaxDataRetransmissions**](settcpmaxdataretransmissions-method-in-class-win32-networkadapterconfiguration.md)       | 設定在中止連接之前，TCP 會重新傳輸個別資料區段的次數。<br/>                                    |
| [**SetTcpNumConnections**](settcpnumconnections-method-in-class-win32-networkadapterconfiguration.md)                       | 設定 TCP 可能同時開啟的最大連接數目。<br/>                                                              |
| [**SetTcpUseRFC1122UrgentPointer**](settcpuserfc1122urgentpointer-method-in-class-win32-networkadapterconfiguration.md)     | 指定 TCP 是否使用緊急資料的 RFC 1122 規格，或 Berkeley Software Design (BSD) 衍生系統所使用的模式。<br/> |
| [**SetTcpWindowSize**](settcpwindowsize-method-in-class-win32-networkadapterconfiguration.md)                               | 設定系統提供的 TCP 接收視窗大小上限。<br/>                                                                            |
| [**SetWINSServer**](setwinsserver-method-in-class-win32-networkadapterconfiguration.md)                                     | 設定此 TCP/IP 系結網路介面卡上 (WINS) 伺服器的主要和次要 Windows 網際網路命名服務。<br/>                        |



 

### <a name="properties"></a>屬性

**Win32 \_ >networkadapterconfiguration** 類別具有這些屬性。

<dl> <dt>

**ArpAlwaysSourceRoute**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| ArpAlwaysSourceRoute" ) 
</dt> </dl>

若 **為 TRUE**，tcp/ip 會將位址解析通訊協定 (ARP) 在權杖環狀網路上啟用來源路由的查詢。 根據預設 (FALSE) ，則會在沒有來源路由的情況下進行 ARP 的第一次查詢，如果未收到回復，則會在啟用來源路由的情況下 來源路由允許在不同類型的網路之間路由傳送網路封包。

</dd> <dt>

**ArpUseEtherSNAP**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| ArpUseEtherSNAP" ) 
</dt> </dl>

若 **為 TRUE**，乙太網路封包會遵循 IEEE 802.3 Sub-Network 存取通訊協定 (貼齊) 編碼。 將此參數設定為1，會強制 TCP/IP 使用802.3 貼齊編碼來傳輸乙太網路封包。 根據預設 (FALSE) ，堆疊會以 DIX Ethernet 格式傳送封包。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) 
</dt> </dl>

目前物件的簡短文字描述。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**DatabasePath**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| DatabasePath" ) 
</dt> </dl>

)  (主機、LMHOSTS、網路和通訊協定的標準網際網路資料庫檔案的 Windows 檔案路徑有效。 Windows 通訊端介面使用檔案路徑。

</dd> <dt>

**DeadGWDetectEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| EnableDeadGWDetect" ) 
</dt> </dl>

若 **為 TRUE，則** 會進行死閘道偵測。 啟用這項功能之後，傳輸控制通訊協定 (TCP) 會要求網際網路通訊協定 (IP) 變更為備份閘道，如果它會多次重新傳輸區段，而不會收到回應。

</dd> <dt>

**DefaultIPGateway**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \| DefaultGateway" ) 
</dt> </dl>

電腦系統使用之預設閘道的 IP 位址陣列。

範例： "192.168.12.1 192.168.46.1"

</dd> <dt>

**DefaultTOS**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| DefaultTOS" ) 
</dt> </dl>

預設的服務類型 (TOS 在連出 IP 封包的標頭中設定的) 值。  (RFC) 791 的批註要求會定義值。 預設值： 0 (零) ，有效範圍： 0-255。

</dd> <dt>

**DefaultTTL**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| DefaultTTL" ) 
</dt> </dl>

預設存留時間 (TTL) 在傳出 IP 封包的標頭中設定的值。 TTL 會指定 IP 封包在被捨棄之前，可以通過的路由器數量來到達目的地。 當 TTL 為 0 (零) 時，每個路由器會以傳遞的封包的 TTL 計數遞減並捨棄封包。 預設值：32，有效範圍： 1-255。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目前物件的文字描述。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**DHCPEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| EnableDHCP" ) 
</dt> </dl>

若 **為 TRUE**，則在建立網路連線時， (DHCP) server 的動態主機設定通訊協定會自動將 IP 位址指派給電腦系統。

</dd> <dt>

**DHCPLeaseExpires**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| LeaseTerminatesTime" ) 
</dt> </dl>

由動態主機設定通訊協定指派給電腦的租用 IP 位址的到期日期和時間 (DHCP) 伺服器。

範例：20521201000230.000000000

</dd> <dt>

**DHCPLeaseObtained**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| LeaseObtainedTime" ) 
</dt> </dl>

使用動態主機設定通訊協定指派給電腦之 IP 位址的日期和時間 (DHCP) 伺服器。

範例：19521201000230.000000000

</dd> <dt>

**DHCPServer**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| DhcpServer" ) 
</dt> </dl>

動態主機設定通訊協定 (DHCP) server 的 IP 位址。

範例： "10.55.34.2"

</dd> <dt>

**DNSDomain**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| Domain" ) 
</dt> </dl>

組織名稱後面接著句點和指出組織類型的延伸模組，例如 "microsoft.com"。 名稱可以是字母 A 到 Z 的任何組合、數位0到9，以及連字號 ( ) ，再加上句點 (. 用來作為分隔符號的 ) 字元。

範例： "microsoft.com"

</dd> <dt>

**DNSDomainSuffixSearchOrder**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| SearchList" ) 
</dt> </dl>

DNS 網域尾碼的陣列，要在名稱解析期間附加至主機名稱的結尾。 當您嘗試從僅限主機名稱稱)  (FQDN 來解析完整功能變數名稱時，系統會先附加本機功能變數名稱。 如果不成功，系統將使用 [網域尾碼] 清單，依列出的順序建立其他 Fqdn，並查詢 DNS 伺服器。

範例： "samples.microsoft.com example.microsoft.com"

</dd> <dt>

**DNSEnabledForWINSResolution**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| EnableDNS" ) 
</dt> </dl>

若 **為 TRUE**，則會啟用透過 Windows 網際網路進行名稱解析的網域名稱系統 (DNS) 命名服務 (WINS) 解決方案。 如果無法使用 DNS 來解析名稱，則會將名稱要求轉送至 WINS 以進行解析。

</dd> <dt>

**DNSHostName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| Hostname" ) 
</dt> </dl>

用來識別本機電腦以供某些公用程式進行驗證的主機名稱。 其他以 TCP/IP 為基礎的公用程式可以使用此值來取得本機電腦的名稱。 主機名稱會儲存在 DNS 伺服器的資料表中，該資料表會將名稱對應至 IP 位址，以供 DNS 使用。 名稱可以是字母 A 到 Z 的任何組合、數位0到9，以及連字號 ( ) ，再加上句點 (. 用來作為分隔符號的 ) 字元。 依預設，此值是 Microsoft 網路電腦名稱稱，但網路系統管理員可以指派其他主機名稱，而不會影響電腦名稱稱。

範例： "corpdns"

</dd> <dt>

**DNSServerSearchOrder**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| NameServer" ) 
</dt> </dl>

要用於查詢 DNS 伺服器的伺服器 IP 位址陣列。

</dd> <dt>

**DomainDNSRegistrationEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若為 **TRUE**，除了在電腦的完整 DNS 名稱下註冊之外，此連線的 IP 位址也會在此連線的功能變數名稱下註冊于 DNS 中。 此連接的功能變數名稱可使用 [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md) () 方法設定，或由 DSCP 指派。 註冊的名稱是已附加功能變數名稱之電腦的主機名稱。

</dd> <dt>

**ForwardBufferMemory**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| ForwardBufferMemory" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) 
</dt> </dl>

由 IP 配置的記憶體，用來將封包資料儲存在路由器封包佇列中。 填滿此緩衝區空間時，路由器會開始從其佇列中隨機捨棄封包。 封包佇列資料緩衝區的長度為256個位元組，因此此參數的值應該是256的倍數。 多個緩衝區會連結在一起，以取得較大的封包。 封包的 IP 標頭會分開儲存。 如果未啟用 IP 路由器，則會忽略此參數，且不會配置任何緩衝區。 緩衝區大小的範圍可以從網路 MTU 到小於0xFFFFFFFF 的值。 預設值： 74240 (50 1480 位元組封包，四捨五入為 256) 的倍數。

</dd> <dt>

**FullDNSRegistrationEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若為 **TRUE**，則此連線的 IP 位址會在 dns 中，以電腦的完整 dns 名稱註冊。 電腦的完整 DNS 名稱會顯示在主控台的系統應用程式的 [ **網路識別** ] 索引標籤上。

</dd> <dt>

**GatewayCostMetric**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

整數成本計量值的陣列 (範圍從1到 9999) ，用來計算最快、最可靠或最少的資源密集路由。 這個引數與 **DefaultIPGateway** 屬性具有一對一的對應關係。

</dd> <dt>

**IGMPLevel**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| IGMPLevel" ) 
</dt> </dl>

系統支援 IP 多播並參與網際網路群組管理通訊協定 (IGMP) 的範圍。 在層級 0 (零) ，系統不會提供任何多播支援。 在層級1，系統可能只會傳送 IP 多播封包。 在層級2，系統可能會傳送 IP 多播封包，並完整地參與 IGMP 以接收多播封包。

<dt>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>**沒有多播** (0) 


</dt> <dd></dd> <dt>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>**IP 多播** (1) 


</dt> <dd></dd> <dt>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>**IP & IGMP 多播** (2) 


</dt> <dd>

IP 和 IGMP 多播 (預設) 

</dd> </dl>

</dd> <dt>

**Index**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](../wmisdk/key-qualifier.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}" ) 
</dt> </dl>

Windows 網路介面卡設定的索引編號。 當有多個可用的設定時，就會使用索引編號。

</dd> <dt>

**InterfaceIndex**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

可唯一識別區域網路介面的索引值。 這個屬性中的值與 [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)實例（代表路由表中的網路介面）的 **InterfaceIndex** 屬性值相同。

</dd> <dt>

**IPAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \\ \\ Tcpip \| IPAddress" ) 
</dt> </dl>

所有與目前網路介面卡相關聯的 IP 位址陣列。 這個屬性可以包含 IPv6 位址或 IPv4 位址。 如需詳細資訊，請參閱 [WMI 中的 IPv6 和 IPv4 支援](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)。

範例 IPv6 位址： "2010：836B：4179：：836B： 4179"

</dd> <dt>

**IPConnectionMetric**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

使用針對 IP 系結介面卡設定的路由，以及 IP 路由表中這些路由的加權值的成本。 如果 IP 路由表中有多個目的地的路由，則會使用最低計量的路由。 預設值為 1。

</dd> <dt>

**IPEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \\ \\ Tcpip" ) 
</dt> </dl>

若 **為 TRUE**，則會在此網路介面卡上系結並啟用 tcp/ip。

</dd> <dt>

**IPFilterSecurityEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| IPFilterSecurityEnabled" ) 
</dt> </dl>

若 **為 TRUE**，則會在所有 ip 系結的網路介面卡上全域啟用 ip 埠安全性，而且與個別網路介面卡相關聯的安全性值就會生效。 這個屬性會與 **IPSecPermitTCPPorts**、 **IPSecPermitUDPPorts** 和 **IPSecPermitIPProtocols** 搭配使用。 若 **為 FALSE**，則會在所有網路介面卡上停用 IP 篩選器安全性，並允許所有埠和通訊協定流量進行未篩選的流程。

</dd> <dt>

**IPPortSecurityEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ >networkadapterconfiguration \| IPFilterSecurityEnabled" ) 
</dt> </dl>

若 **為 TRUE**，則會在所有 ip 系結的網路介面卡上全域啟用 ip 埠安全性。 這個屬性已經過時。 若要取代這個屬性，您應該使用 **IPFilterSecurityEnabled**。

</dd> <dt>

**IPSecPermitIPProtocols**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| RawIPAllowedProtocols" ) 
</dt> </dl>

允許透過 IP 執行的通訊協定陣列。 通訊協定清單是使用 [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) 方法來定義。 此清單會是空的或包含數值。 數值 0 (零) 表示授與所有通訊協定的存取權限。 空字串表示當 **IPFilterSecurityEnabled** 為 **TRUE** 時，不允許執行任何通訊協定。

</dd> <dt>

**IPSecPermitTCPPorts**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| TCPAllowedPorts" ) 
</dt> </dl>

將授與 TCP 存取權限之埠的陣列。 通訊協定清單是使用 [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) 方法來定義。 此清單會是空的或包含數值。 數值 0 (零) 表示授與所有埠的存取權限。 空字串表示當 **IPFilterSecurityEnabled** 為 **TRUE** 時，沒有任何埠被授與存取權限。

</dd> <dt>

**IPSecPermitUDPPorts**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| UDPAllowedPorts" ) 
</dt> </dl>

將授與使用者資料包協定 (UDP) 存取權限之埠的陣列。 通訊協定清單是使用 [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) 方法來定義。 此清單會是空的或包含數值。 數值 0 (零) 表示授與所有埠的存取權限。 空字串表示當 **IPFilterSecurityEnabled** 為 **TRUE** 時，沒有任何埠被授與存取權限。

</dd> <dt>

**IPSubnet**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \| SubnetMask" ) 
</dt> </dl>

所有與目前網路介面卡相關聯的子網路遮罩的陣列。

範例： "255.255.0.0"

</dd> <dt>

**IPUseZeroBroadcast**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| UseZeroBroadcast" ) 
</dt> </dl>

若 **為 TRUE**，則會使用 IP 零廣播 (0.0.0.0) ，而且系統會使用 (255.255.255.255) 的廣播。 電腦系統通常會使用其中一種廣播，但衍生自 BSD 的專案則會使用零的廣播。 未使用相同廣播的系統將無法在相同網路上互通。 預設值為 **FALSE**。

</dd> <dt>

**IPXAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Windows 通訊端第2版 \| [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) \| IPX \_ ADDRESS" ) 
</dt> </dl>

網路封包交換 (IPX) 技術已不再支援，而且此屬性不包含有用的資料。

</dd> <dt>

**IPXEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI" ) 
</dt> </dl>

網路封包交換 (IPX) 技術已不再支援，而且此屬性不包含有用的資料。

</dd> <dt>

**IPXFrameType**
</dt> <dd> <dl> <dt>

資料類型： **uint32** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx \\ \\ Parameters \| PktType" ) 
</dt> </dl>

網路封包交換 (IPX) 技術已不再支援，而且此屬性不包含有用的資料。

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

**ETHERNET II** (0) 


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

**Ethernet 802.3** (1) 


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

**Ethernet 802.2** (2) 


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

**Ethernet 貼齊** (3) 


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

**自動** (255) 


</dt> <dd></dd> </dl>

</dd> <dt>

**IPXMediaType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx \\ \\ Parameters \| 媒體" ) 
</dt> </dl>

網路封包交換 (IPX) 技術已不再支援，而且此屬性不包含有用的資料。

<dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (1) 


</dt> <dd></dd> <dt>

<span id="Token_ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

**權杖環** (2) 


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

**FDDI** (3) 


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

**ARCNET** (8) 


</dt> <dd></dd> </dl>

</dd> <dt>

**IPXNetworkNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx \\ \\ Parameters \| NetworkNumber" ) 
</dt> </dl>

網路封包交換 (IPX) 技術已不再支援，而且此屬性不包含有用的資料。

</dd> <dt>

**IPXVirtualNetNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx \\ \\ Parameters \| VirtualNetworkNumber" ) 
</dt> </dl>

網路封包交換 (IPX) 技術已不再支援，而且此屬性不包含有用的資料。

</dd> <dt>

**KeepAliveInterval**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| KeepAliveInterval" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "毫秒" ) 
</dt> </dl>

分隔保持運作的間隔，直到收到回應為止。 收到回應之後，會延遲到下一個保持運作的傳輸，再由 **KeepAliveTime** 的值控制。 連線將會在 **TcpMaxDataRetransmissions** 所指定的重新傳輸次數尚未接聽之後中止。 預設值：1000，有效範圍： 1-0xFFFFFFFF。

</dd> <dt>

**KeepAliveTime**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| KeepAliveInterval" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "毫秒" ) 
</dt> </dl>

**KeepAliveTime** 屬性會藉由傳送 Keep-alive 封包，指出 TCP 嘗試驗證閒置連線是否仍保持不變的頻率。 可觸達的遠端系統將會認可保持運作傳輸狀態。 預設不會傳送存活的封包。 這項功能可以在應用程式的連接中啟用。 預設值： 7200000 (兩個小時) 。

</dd> <dt>

**MACAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device Input and Output 函數 \| DeviceIoControl" ) 
</dt> </dl>

媒體存取控制 (網路介面卡的 MAC) 位址。 製造商會指派 MAC 位址來唯一識別網路介面卡。

範例： "00：80： C7：8F：6C： 96"

</dd> <dt>

**MTU**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| MTU" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) 
</dt> </dl>

覆寫網路介面 (MTU) 的預設最大傳輸單位。 MTU 是最大的封包大小 (包括傳輸會透過基礎網路傳輸的傳輸標頭) 。 IP 資料包可以跨多個封包。 此值的範圍會跨越基礎網路所支援的 MTU (68) 的最小封包大小。

</dd> <dt>

**NumForwardPackets**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| NumForwardPackets" ) 
</dt> </dl>

配置給路由器封包佇列的 IP 封包標頭數目。 當所有標頭都在使用中時，路由器會開始隨機捨棄佇列中的封包。 此值應該至少等於 **ForwardBufferMemory** 值除以連線到路由器的網路 IP 資料大小上限。 它應該不會大於 **ForwardBufferMemory** 值除以256，因為每個封包都使用至少256個位元組的轉送緩衝區記憶體。 給定 **ForwardBufferMemory** 大小的最佳轉寄封包數目，取決於網路上的流量類型。 它會在這兩個值之間的某處。 如果未啟用路由器，則會忽略此參數，且不會配置任何標頭。 預設值：50，有效範圍： 1-0xFFFFFFFE。

</dd> <dt>

**PMTUBHDetectEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| EnablePMTUBHDetect" ) 
</dt> </dl>

若 **為 TRUE**，當 TCP 探索最大傳輸單位的路徑時，就會偵測到黑洞路由器。 當您需要將未設定片段位的 IP 資料包分割時，黑洞路由器不會傳回 ICMP 目的地無法連線的訊息。 TCP 取決於接收這些訊息來執行路徑 MTU 探索。 啟用這項功能之後，如果區段的數次重新傳輸未確認，TCP 將會嘗試傳送區段，而不會設定片段位。 如果已通知區段，則 MSS 將會減少，而不會在連接的未來封包中設定「不片段」位。 啟用黑洞偵測會增加針對指定區段執行的重新傳輸數目上限。 這個屬性的預設值為 **FALSE**。

</dd> <dt>

**PMTUDiscoveryEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| EnablePMTUDiscovery" ) 
</dt> </dl>

若為 **TRUE**，則會在遠端主機的路徑上探索最大傳輸單位 (MTU) 路徑。 藉由探索 MTU 路徑，並將 TCP 區段限制為此大小，TCP 可以在連接具有不同 Mtu 之網路的路徑中，排除路由器上的片段。 片段會對 TCP 輸送量和網路擁塞造成負面影響。 若將此參數設定為 **FALSE** ，則會將576個位元組的 MTU 用於非本機子網上電腦的所有連接。 預設值為 **TRUE**。

</dd> <dt>

**ServiceName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| ServiceName" ) 
</dt> </dl>

網路介面卡的服務名稱。 這個名稱通常比完整的產品名稱短。

範例： "Elnkii"

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 
</dt> </dl>

已知目前物件的識別碼。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**TcpipNetbiosOptions**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

NetBIOS over TCP/IP 相關可能設定的點陣圖。 下列清單中會識別值。

<dt>

<span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>

**EnableNetbiosViaDhcp** (0) 


</dt> <dd></dd> <dt>

<span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>

**EnableNetbios** (1) 


</dt> <dd></dd> <dt>

<span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>

**DisableNetbios** (2) 


</dt> <dd></dd> </dl>

</dd> <dt>

**TcpMaxConnectRetransmissions**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| TcpMaxConnectRetransmissions" ) 
</dt> </dl>

TCP 在終止連接之前嘗試重新傳輸連接要求的次數。 初始重新傳輸超時時間為3秒。 每次嘗試的重新傳輸超時都會加倍。 預設值：3，有效範圍： 0-0xFFFFFFFF。

</dd> <dt>

**TcpMaxDataRetransmissions**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| TcpMaxDataRetransmissions" ) 
</dt> </dl>

在終止連接之前，TCP 重新傳輸個別資料區段 (nonconnect 區段) 的次數。 重新傳輸超時會加倍，並在連線上每次重新傳輸。 預設值：5，有效範圍： 0-0xFFFFFFFF。

</dd> <dt>

**TcpNumConnections**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| TcpNumConnections" ) 
</dt> </dl>

TCP 可以同時開啟的最大連接數目。 預設值：0xFFFFFE，有效範圍： 0-0xFFFFFE。

</dd> <dt>

**TcpUseRFC1122UrgentPointer**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| TcpUseRFC1122UrgentPointer" ) 
</dt> </dl>

若 **為 TRUE**，TCP 會使用 RFC 1122 規格來進行緊急資料。 如果 **為 FALSE** (預設) ，TCP 會使用 Berkeley Software DESIGN (BSD) 衍生系統所使用的模式。 這兩種機制會以不同方式解讀緊急指標，而且無法互通。 預設值為 **FALSE**。

</dd> <dt>

**TcpWindowSize**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| TcpWindowSize" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) 
</dt> </dl>

系統提供的 TCP 接收視窗大小上限。 接收視窗會指定傳送者在未收到通知的情況下，可能會傳送的位元組數目。 一般而言，較大的接收視窗會透過高延遲和高頻寬的網路來提升效能。 為了提高效率，接收視窗應該是 (MSS) 的 TCP 最大區段大小的倍數。 預設值： TCP 資料大小上限的四倍，或是最大的 TCP 資料大小的倍數，舍入到最接近的8192倍數。 Ethernet 網路預設為8760。 有效範圍： 0-65535。

> [!Note]  
> Windows Vista：此屬性會存取 `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` 登錄專案，此專案不會用於目前的作業系統執行。

 

</dd> <dt>

**WINSEnableLMHostsLookup**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| EnableLMHOSTS" ) 
</dt> </dl>

若 **為 TRUE**，則會使用本機查閱檔案。 查閱檔案將包含 IP 位址與主機名稱的對應。 如果它們存在於本機系統上，則會在% SystemRoot% \\ system32 \\ 驅動程式等中找到 \\ 。

</dd> <dt>

**WINSHostLookupFile**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 系統資訊函式 \| [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) \| \\ \\ 驅動程式 \\ \\ 等 \\ \\ lmhosts" ) 
</dt> </dl>

本機系統上 WINS 查閱檔案的路徑。 此檔案會包含主機名稱的 IP 位址對應。 如果找到這個屬性中指定的檔案，則會將它複製到本機系統的% SystemRoot% \\ system32 \\ 驅動程式 \\ 等資料夾。 只有在 **WINSEnableLMHostsLookup** 屬性為 **TRUE** 時才有效。

</dd> <dt>

**WINSPrimaryServer**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device Input and Output 函數 \| DeviceIoControl" ) 
</dt> </dl>

主要 WINS 伺服器的 IP 位址。

</dd> <dt>

**WINSScopeID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| ScopeID" ) 
</dt> </dl>

附加至 NetBIOS 名稱結尾的值，可隔離一組電腦系統彼此通訊。 它可用於所有透過 TCP/IP 通訊的電腦系統的 NetBIOS 交易。 使用相同的範圍識別碼設定的電腦可以與這部電腦通訊。 具有不同範圍識別碼的 TCP/IP 用戶端會忽略來自具有此範圍識別碼之電腦的封包。 只有在 [**>enablewins**](enablewins-method-in-class-win32-networkadapterconfiguration.md) 方法執行成功時才有效。

</dd> <dt>

**WINSSecondaryServer**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device Input and Output 函數 \| DeviceIoControl" ) 
</dt> </dl>

次要 WINS 伺服器的 IP 位址。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ >networkadapterconfiguration** 類別衍生自 [**CIM \_ 設定**](cim-setting.md)。

## <a name="examples"></a>範例

TechNet 資源庫上的 [WMI 資訊](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) 取回程序 VBScript 程式碼範例會使用 **Win32 \_ >networkadapterconfiguration** 類別，從多部遠端電腦抓取網路設定資訊。

[本機/遠端電腦上的 Get-computerinfo 查詢電腦資訊（ (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell 範例（英文）： TechNet 資源庫上的 PowerShell 範例會使用一些硬體和軟體的呼叫，包括 **Win32 \_ >networkadapterconfiguration**，以顯示本機或遠端系統的相關資訊。

下列 PowerShell 程式碼會抓取 Microsoft ISTAP Adapter 的設定。


```PowerShell
$IstapAdapterConfig = Get-WmiObject Win32_NetworkAdapterConfiguration | Where-Object {$_.Description -eq "Microsoft ISATAP Adapter"}
$IstapAdapterConfig
```



下列 C 範例會抓取 \# 所有網路介面卡設定實例的描述和索引編號。 請注意，此 C \# 範例使用的是 [管理基礎結構](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) 命名空間，其通常會比 [管理](/dotnet/api/system.management) 命名空間 WMI 類別更有效率地進行調整。


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



下列 C 範例會抓取 \# 所有網路介面卡設定實例的描述和索引編號。 請注意，此 C \# 範例會使用由[Microsoft](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))所取代的原始[管理](/dotnet/api/system.management)命名空間。


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



下列範例會從 **Win32 \_ >networkadapterconfiguration** 類別中取出資訊。


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



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 設定**](cim-setting.md)
</dt> <dt>

[電腦系統硬體類別](computer-system-hardware-classes.md)
</dt> <dt>

[WMI 工作：網路功能](../wmisdk/wmi-tasks--networking.md)
</dt> <dt>

[WMI 工作：帳戶和網域](../wmisdk/wmi-tasks--accounts-and-domains.md)
</dt> <dt>

[WMI 中的 IPv6 和 IPv4 支援](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
