---
description: Windows 管理基礎結構 (WMI) 、Management Instrumentation (MI) 和開放式管理基礎結構 (OMI) 全部使用管理物件格式 (MOF) 檔，以描述透過其個別提供者提供的資訊。
ms.assetid: 5ec3c6a2-df23-446d-a4da-b8e207eeb6f6
title: WMI/MI/OMI 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505a0853d9df7d9cf6f2371f6342b77f61f536b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001770"
---
# <a name="wmimiomi-providers"></a>WMI/MI/OMI 提供者

Windows 管理基礎結構 (WMI) 、Management Instrumentation (MI) 和開放式管理基礎結構 (OMI) 全部使用管理物件格式 (MOF) 檔，以描述透過其個別提供者提供的資訊。

<dl> <dt>

<span id="Active_Directory"></span><span id="active_directory"></span><span id="ACTIVE_DIRECTORY"></span>[Active Directory](/previous-versions/windows/desktop/dsprov/active-directory-provider)
</dt> <dd>

Active Directory 提供者（也稱為目錄服務 (DS) 提供者）會將 Active Directory 物件對應至 WMI。 藉由在 WMI 中存取輕量型目錄存取協定 (LDAP) 命名空間，您可以在 Active Directory 中參考或建立物件的別名。

</dd> <dt>

<span id="Application_Inventory"></span><span id="application_inventory"></span><span id="APPLICATION_INVENTORY"></span>[應用程式清查](/previous-versions/windows/desktop/appdevinvprov/applicationanddeviceinventory-portal)
</dt> <dd>

應用程式清查的 WMI 類別可讓您探索 Windows 系統上已安裝的 Win32 應用程式和 Windows store 應用程式。

</dd> <dt>

<span id="Application_Proxy"></span><span id="application_proxy"></span><span id="APPLICATION_PROXY"></span>[應用程式 Proxy](/previous-versions/windows/desktop/appproxypsprov/application-proxy-wmi-provider-portal)
</dt> <dd>

應用程式 Proxy WMI 提供者可讓開發人員存取 Web 應用程式 Proxy 服務，讓系統管理員可以發行應用程式以進行外部存取。 Web 應用程式 Proxy 是 Active Directory 同盟服務 (AD FS) 的反向 Proxy。

</dd> <dt>

<span id="BitLocker_Drive_Encryption__BDE_"></span><span id="bitlocker_drive_encryption__bde_"></span><span id="BITLOCKER_DRIVE_ENCRYPTION__BDE_"></span>[BitLocker 磁碟機加密 (MANAGE-BDE) ](/windows/desktop/SecProv/bitlocker-drive-encryption-provider)
</dt> <dd>

提供在硬碟上設定和管理儲存空間的區域（由 [**Win32 \_ EncryptableVolume**](/windows/desktop/SecProv/win32-encryptablevolume)的實例表示），可以使用加密來保護。

</dd> <dt>

<span id="BITS"></span><span id="bits"></span>[位](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> <dd>

背景智慧型傳送服務 (位) Compact Server 搭配 BITS 遠端系統管理，可讓經過驗證的系統管理員或控制器應用程式在遠端建立、修改及管理 BITS 傳送工作，而不需使用 Internet Information Services (IIS) 服務。

</dd> <dt>

<span id="BizTalk"></span><span id="biztalk"></span><span id="BIZTALK"></span>[BizTalk](https://msdn.microsoft.com/library/ms941491.aspx)
</dt> <dd>

提供 WMI 類別所表示之 BizTalk 管理物件的存取權。

</dd> <dt>

<span id="Boot_Configuration_Data"></span><span id="boot_configuration_data"></span><span id="BOOT_CONFIGURATION_DATA"></span>[開機設定資料](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal)
</dt> <dd>

開機設定資料 (BCD) 提供者會提供用來描述開機應用程式和開機應用程式設定的存放區。

</dd> <dt>

<span id="Boot_Event_Collector"></span><span id="boot_event_collector"></span><span id="BOOT_EVENT_COLLECTOR"></span>[開機事件收集器](/windows/desktop/BEvtColProv/boot-event-collector-wmi-provider-portal)
</dt> <dd>

開機事件收集器 WMI 提供者可讓您存取 Windows Server 上的設定和開機事件集合功能的連接和設定資訊。

</dd> <dt>

<span id="CIMWin32__Win32__Power_Management_Events"></span><span id="cimwin32__win32__power_management_events"></span><span id="CIMWIN32__WIN32__POWER_MANAGEMENT_EVENTS"></span>[CIMWin32，Win32，電源管理事件](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers)
</dt> <dd>

CIMWin32 提供者支援在 CimWin32.dll 中執行的類別，並包含核心 CIM 類別、這些類別的 Win32 實作為，以及電源管理事件。

</dd> <dt>

<span id="CIMWin32a"></span><span id="cimwin32a"></span><span id="CIMWIN32A"></span>[Cimwin32a.](/previous-versions/windows/desktop/cimwin32a/cimwin32a-provider-classes)
</dt> <dd>

Cimwin32a. 提供者會擴充 [CIMWin32](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers)中可用的類別。

</dd> <dt>

<span id="DcbQosCim"></span><span id="dcbqoscim"></span><span id="DCBQOSCIM"></span>[DcbQosCim](/previous-versions/windows/desktop/dcbwmiprov/dcb-qos)
</dt> <dd>

DcbQosCim 提供者支援描述網路 QOS 設定資料、控制設定資料和流量類別設定資料的類別。

</dd> <dt>

<span id="Distributed_File_System__DFS_"></span><span id="distributed_file_system__dfs_"></span><span id="DISTRIBUTED_FILE_SYSTEM__DFS_"></span>[分散式檔案系統 (DFS) ](/previous-versions/windows/desktop/wmipdfs/dfs-provider)
</dt> <dd>

DFS 提供者透過 WMI 提供可編寫腳本的 DFS 功能。

</dd> <dt>

<span id="Distributed_File_System_Replication__DFSR_"></span><span id="distributed_file_system_replication__dfsr_"></span><span id="DISTRIBUTED_FILE_SYSTEM_REPLICATION__DFSR_"></span>[分散式檔案系統複寫 (DFSR) ](/previous-versions/windows/desktop/dfsr/distributed-file-system-replication--dfsr-)
</dt> <dd>

建立用來設定和監視 [分散式檔案系統 (DFS) ](/previous-versions/windows/desktop/dfs/distributed-file-system) 服務的工具。 如需詳細資訊，請參閱 [DFSR WMI 類別](/previous-versions/windows/desktop/dfsr/dfsr-wmi-classes)。

</dd> <dt>

<span id="Dfsncimprov"></span><span id="dfsncimprov"></span><span id="DFSNCIMPROV"></span>[Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes)
</dt> <dd>

[Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes)提供者支援可執行 DFS 命名空間存取的類別。

</dd> <dt>

<span id="DhcpServerPSProvider"></span><span id="dhcpserverpsprovider"></span><span id="DHCPSERVERPSPROVIDER"></span>[DhcpServerPSProvider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes)
</dt> <dd>

[DhcpServerPSProvider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes)提供者支援與動態主機設定通訊協定 (DHCP) 伺服器互動的類別。

</dd> <dt>

<span id="Disk_Quota"></span><span id="disk_quota"></span><span id="DISK_QUOTA"></span>[磁片配額](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider)
</dt> <dd>

Windows 磁片配額提供者可讓系統管理員控制每位使用者在 NTFS 檔案系統上儲存的資料量。

</dd> <dt>

<span id="Distributed_Transaction_Coordinator__DTC_"></span><span id="distributed_transaction_coordinator__dtc_"></span><span id="DISTRIBUTED_TRANSACTION_COORDINATOR__DTC_"></span>[分散式交易協調器 (DTC) ](/previous-versions/windows/desktop/msdtcwmi/distributed-transaction-coordinator-wmi-provider-portal)
</dt> <dd>

DTC 提供者可讓您管理 DTC。

</dd> <dt>

<span id="DNS"></span><span id="dns"></span>[Dns](/windows/desktop/DNS/dns-wmi-provider)
</dt> <dd>

可讓系統管理員和程式設計師使用 WMI 設定網域名稱系統 (DNS) 資源記錄 (Rr) 和 DNS 伺服器。

</dd> <dt>

<span id="Dnsclientcim_Provider_Classes"></span><span id="dnsclientcim_provider_classes"></span><span id="DNSCLIENTCIM_PROVIDER_CLASSES"></span>[Dnsclientcim 提供者類別](/previous-versions/windows/desktop/dnsclientcimprov/dns-client-classes)
</dt> <dd>

Dnsclientcim 提供者支援 (DNS) 用戶端與網域名稱系統互動的類別。

</dd> <dt>

<span id="DnsClientPSProvider"></span><span id="dnsclientpsprovider"></span><span id="DNSCLIENTPSPROVIDER"></span>[DnsClientPSProvider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes)
</dt> <dd>

[DnsClientPSProvider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes)提供者支援與 DNS 用戶端互動的 WMI 類別。

</dd> <dt>

<span id="DnsServerPSProvider"></span><span id="dnsserverpsprovider"></span><span id="DNSSERVERPSPROVIDER"></span>[DnsServerPSProvider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes)
</dt> <dd>

[DnsServerPSProvider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes)提供者支援與 DNS 伺服器互動的 WMI 類別。

</dd> <dt>

<span id="Event_Log"></span><span id="event_log"></span><span id="EVENT_LOG"></span>[事件記錄檔](/previous-versions/windows/desktop/eventlogprov/event-log-provider)
</dt> <dd>

[事件記錄](/previous-versions/windows/desktop/eventlogprov/event-log-provider)提供者會從事件記錄服務提供資料的存取權，以及事件的通知。

</dd> <dt>

<span id="Event_Tracing_Management"></span><span id="event_tracing_management"></span><span id="EVENT_TRACING_MANAGEMENT"></span>[事件追蹤管理](/previous-versions/windows/desktop/etwmgmt/event-tracing-management-wmi-provider-portal)
</dt> <dd>

事件追蹤管理提供者可存取 Windows (ETW) 自動記錄器會話設定和追蹤事件的事件追蹤。

</dd> <dt>

<span id="Failover_Cluster-Aware_Updating"></span><span id="failover_cluster-aware_updating"></span><span id="FAILOVER_CLUSTER-AWARE_UPDATING"></span>[更新容錯移轉 Cluster-Aware](/previous-versions/windows/desktop/cauwmiv2/failover-cluster-aware-patching-mi-provider-portal)
</dt> <dd>

容錯移轉 Cluster-Aware 更新 (CAU) 提供者可支援與 CAU 的協調及管理。

</dd> <dt>

<span id="Failover_Clustering_Hyper-V"></span><span id="failover_clustering_hyper-v"></span><span id="FAILOVER_CLUSTERING_HYPER-V"></span>[Hyper-v 容錯移轉叢集](/previous-versions/windows/desktop/clushyperv/failover-clustering-hyper-v-wmi-provider-portal)
</dt> <dd>

「容錯移轉叢集」 Hyper-v 提供者提供叢集環境中 Hyper-v 的管理和報告。

</dd> <dt>

<span id="Failover_Clustering_Storage_QoS"></span><span id="failover_clustering_storage_qos"></span><span id="FAILOVER_CLUSTERING_STORAGE_QOS"></span>[容錯移轉叢集儲存體 QoS](/previous-versions/windows/desktop/clusstorageqosprov/failover-clustering-storage-qos-mi-provider-portal)
</dt> <dd>

容錯移轉叢集儲存體服務品質 (QoS) 提供者可提供叢集存放裝置 QoS 原則的管理和報告。

</dd> <dt>

<span id="Failover_Cluster_V1_Provider"></span><span id="failover_cluster_v1_provider"></span><span id="FAILOVER_CLUSTER_V1_PROVIDER"></span>[容錯移轉叢集 V1 提供者](/previous-versions/windows/desktop/cluswmi/failover-cluster-wmi-provider-portal)
</dt> <dd>

容錯移轉叢集 V1 提供者可管理容錯移轉叢集。

</dd> <dt>

<span id="Failover_Cluster_V1_Extensions"></span><span id="failover_cluster_v1_extensions"></span><span id="FAILOVER_CLUSTER_V1_EXTENSIONS"></span>[容錯移轉叢集 V1 擴充功能](/previous-versions/windows/desktop/cluswmiext/failover-cluster-wmi-provider-extensions-portal)
</dt> <dd>

容錯移轉叢集擴充提供者可提供額外的容錯移轉叢集管理。

</dd> <dt>

<span id="Gateway_Health_Monitor"></span><span id="gateway_health_monitor"></span><span id="GATEWAY_HEALTH_MONITOR"></span>[閘道健全狀況監視](/previous-versions/windows/desktop/gatewayhealthmonprov/gateway-health-monitor-wmi-provider-portal)
</dt> <dd>

閘道健全狀況監視提供者會管理閘道健全狀況監視事件和資訊。

</dd> <dt>

<span id="Group_Policy_API"></span><span id="group_policy_api"></span><span id="GROUP_POLICY_API"></span>[群組原則 API](/previous-versions/windows/desktop/Policy/group-policy-start-page)
</dt> <dd>

群組原則提供者會使用 Microsoft Active Directory (AD) 目錄服務來啟用以原則為基礎的系統管理。

</dd> <dt>

<span id="Host_Guardian_Service"></span><span id="host_guardian_service"></span><span id="HOST_GUARDIAN_SERVICE"></span>[主機守護者服務](/previous-versions/windows/desktop/hgsclientwmi/hoster-guardian-service-wmi-provider-portal)
</dt> <dd>

主機守護者服務提供者會為受防護的 Vm 提供主機守護者服務的管理。

</dd> <dt>

<span id="Hyper-V"></span><span id="hyper-v"></span><span id="HYPER-V"></span>[Hyper-v](/previous-versions/windows/desktop/virtual/windows-virtualization-portal)
</dt> <dd>

Hyper-v 提供者可讓您管理和取得虛擬機器的相關資訊。

</dd> <dt>

<span id="Hyper-V__V2_"></span><span id="hyper-v__v2_"></span><span id="HYPER-V__V2_"></span>[Hyper-v (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)
</dt> <dd>

Hyper-v (V2) 提供者會擴充 [hyper-v](/previous-versions/windows/desktop/virtual/windows-virtualization-portal) 提供者。

</dd> <dt>

<span id="Internet_Information_Services__IIS_"></span><span id="internet_information_services__iis_"></span><span id="INTERNET_INFORMATION_SERVICES__IIS_"></span>[Internet Information Services (IIS) ](/previous-versions/iis/6.0-sdk/ms525309(v=vs.90))
</dt> <dd>

公開可用於查詢及設定 IIS 元資料庫的程式設計介面。

</dd> <dt>

<span id="Internet_Protocol_Address_Management__IPAM__Server"></span><span id="internet_protocol_address_management__ipam__server"></span><span id="INTERNET_PROTOCOL_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>[ (IPAM) 伺服器的網際網路通訊協定位址管理](/previous-versions/windows/desktop/ipamserverpsprov/internet-protocol-address-management-server-wmi-provider-portal)
</dt> <dd>

IPAM 伺服器提供者可讓開發人員透過 WMI 管理 IPAM。

</dd> <dt>

<span id="IP_Route_Provider"></span><span id="ip_route_provider"></span><span id="IP_ROUTE_PROVIDER"></span>[IP 路由提供者](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider)
</dt> <dd>

預先安裝的 IP 路由提供者會提供 IPV4 網路路由資訊，包括 (但不限於) 透過 **Route print** 命令提供的資訊。

</dd> <dt>

<span id="Intelligent_Platform_Management_Interface__IPMI_"></span><span id="intelligent_platform_management_interface__ipmi_"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE__IPMI_"></span>[智慧型平臺管理介面 (IPMI) ](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)
</dt> <dd>

提供基礎板管理控制器 (BMC) 作業的 IPMI 資料。

</dd> <dt>

<span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>[iSCSI 目標伺服器](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)
</dt> <dd>

ISCSI 目標伺服器提供者支援 WMI 介面來管理 Microsoft iSCSI 目標伺服器，例如建立虛擬磁片，以及將它們呈現給用戶端。

</dd> <dt>

<span id="Job_Object"></span><span id="job_object"></span><span id="JOB_OBJECT"></span>[工作物件](/previous-versions/windows/desktop/wmipjobobjprov/job-object-provider)
</dt> <dd>

工作物件提供者支援存取命名核心工作物件的資料。

</dd> <dt>

<span id="Kernel_Trace"></span><span id="kernel_trace"></span><span id="KERNEL_TRACE"></span>[核心追蹤](/previous-versions/windows/desktop/krnlprov/kernel-trace-provider)
</dt> <dd>

預先安裝的核心追蹤事件提供者可讓您查看進程建立、進程終止、執行緒建立、執行緒終止和模組載入的核心追蹤事件。

</dd> <dt>

<span id="Live_Communications_Server_2003"></span><span id="live_communications_server_2003"></span><span id="LIVE_COMMUNICATIONS_SERVER_2003"></span>[Live communication Server 2003](/previous-versions/office/developer/office-2003/cc165126(v=office.11))
</dt> <dd>

提供的類別可建立、註冊、設定、管理自訂會話初始通訊協定 (SIP) 應用程式與 [Live Communication Server 2003](/previous-versions/office/aa194012(v=office.11))。

</dd> <dt>

<span id="Management_Tools_Registry"></span><span id="management_tools_registry"></span><span id="MANAGEMENT_TOOLS_REGISTRY"></span>[管理工具登錄](/previous-versions/windows/desktop/mtregprov/managementtools-registry-wmi-provider-portal)
</dt> <dd>

管理工具登錄提供者提供登錄的遠端存取。

</dd> <dt>

<span id="Management_Tools_Task_Manager"></span><span id="management_tools_task_manager"></span><span id="MANAGEMENT_TOOLS_TASK_MANAGER"></span>[管理工具工作管理員](/previous-versions/windows/desktop/mttmprov/management-tools-task-manager-wmi-provider-portal)
</dt> <dd>

管理工具工作管理員提供者可提供工作管理員資料的存取和管理。

</dd> <dt>

<span id="MDM_Application"></span><span id="mdm_application"></span><span id="MDM_APPLICATION"></span>[MDM 應用程式](/previous-versions/windows/desktop/mdmappprov/mobile-device-management-application-provider-portal)
</dt> <dd>

行動裝置管理 (MDM) 應用程式提供者會在訂閱 MDM 服務的裝置上管理應用程式。

</dd> <dt>

<span id="MDM_Bridge"></span><span id="mdm_bridge"></span><span id="MDM_BRIDGE"></span>[MDM 橋接器](/windows/desktop/DMWmiBridgeProv/mdm-bridge-wmi-provider-portal)
</dt> <dd>

MDM 橋接器提供者可啟用網路橋接器的 MDM 管理。

</dd> <dt>

<span id="MDM_Settings"></span><span id="mdm_settings"></span><span id="MDM_SETTINGS"></span>[MDM 設定](/previous-versions/windows/desktop/mdmsettingsprov/mobile-device-management-settings-provider-portal)
</dt> <dd>

MDM 設定提供者可讓您管理以 MDM 服務註冊之裝置上的設定。

</dd> <dt>

<span id="MSFT_PCSVDevice"></span><span id="msft_pcsvdevice"></span><span id="MSFT_PCSVDEVICE"></span>[MSFT \_ PCSVDevice](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes)
</dt> <dd>

[MSFT \_ PCSVDevice](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes)提供者會公開類別，以定義實體電腦系統的視圖類別。

</dd> <dt>

<span id="MsNetImPlatform"></span><span id="msnetimplatform"></span><span id="MSNETIMPLATFORM"></span>[MsNetImPlatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes)
</dt> <dd>

[ [MsNetImPlatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes) 提供者] 區段提供在 NdisIMPlatCim.dll 中執行的 MsNetImPlatform 提供者類別的參考資訊。

</dd> <dt>

<span id="NetAdapterCim"></span><span id="netadaptercim"></span><span id="NETADAPTERCIM"></span>[NetAdapterCim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes)
</dt> <dd>

[NetAdapterCim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes)提供者支援可存取網路介面卡的類別。

</dd> <dt>

<span id="NetDaCim"></span><span id="netdacim"></span><span id="NETDACIM"></span>[NetDaCim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes)
</dt> <dd>

本節提供 [NetDaCim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes) 提供者類別的參考資訊。

</dd> <dt>

<span id="NetNcCim"></span><span id="netnccim"></span><span id="NETNCCIM"></span>[NetNcCim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status)
</dt> <dd>

提供 [NetNcCim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status) 提供者類別的參考資訊。

</dd> <dt>

<span id="NetPeerDist"></span><span id="netpeerdist"></span><span id="NETPEERDIST"></span>[NetPeerDist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache)
</dt> <dd>

[NetPeerDist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache)提供者支援與分支快取基礎結構互動的類別。

</dd> <dt>

<span id="NetQosCim"></span><span id="netqoscim"></span><span id="NETQOSCIM"></span>[NetQosCim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes)
</dt> <dd>

[NetQosCim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes)提供者會提供網路服務品質 (qos) 和 qos 設定資料的資料。

</dd> <dt>

<span id="NetSwitchTeam"></span><span id="netswitchteam"></span><span id="NETSWITCHTEAM"></span>[NetSwitchTeam](/previous-versions/windows/desktop/netswitchteamprov/network-switch-team-classes)
</dt> <dd>

本節提供在 NetSwitchTeam 中宣告並在 NetSwitchTeamCim.dll 中執行的 NetSwitchTeam 提供者類別的參考資訊。

</dd> <dt>

<span id="NetTCPIP"></span><span id="nettcpip"></span><span id="NETTCPIP"></span>[NetTCPIP](/previous-versions/windows/desktop/nettcpipprov/net-tcpip-classes)
</dt> <dd>

NetTCPIP 提供者支援與 TCPIP 連接互動的類別。

</dd> <dt>

<span id="NetTtCim"></span><span id="netttcim"></span><span id="NETTTCIM"></span>[NetTtCim](/previous-versions/windows/desktop/netttcimprov/network-transition-classes)
</dt> <dd>

本節提供在 NetTtCim 中定義並在 NetTtCim.dll 中執行的 NetTtCim 提供者類別的參考資訊。

</dd> <dt>

<span id="NetWNV"></span><span id="netwnv"></span><span id="NETWNV"></span>[NetWNV](/previous-versions/windows/desktop/netwnvprov/net-virtualization-classes)
</dt> <dd>

NetWNV 提供者支援與 net virtualization 技術互動的類別。

</dd> <dt>

<span id="Network_Access_Protection"></span><span id="network_access_protection"></span><span id="NETWORK_ACCESS_PROTECTION"></span>[網路存取保護](/previous-versions/windows/desktop/napprov/network-access-protection-wmi-provider-portal)
</dt> <dd>

網路存取保護提供者會公開平臺，以保護對私人網路的存取。

</dd> <dt>

<span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>[網路負載平衡](/previous-versions/windows/desktop/wlbsprov/network-load-balancing-provider-portal)
</dt> <dd>

 (NLB) 提供者的網路負載平衡可讓您管理 NLB 叢集。

</dd> <dt>

<span id="NetworkController_Server"></span><span id="networkcontroller_server"></span><span id="NETWORKCONTROLLER_SERVER"></span>[NetworkController 伺服器](/previous-versions/windows/desktop/ncserverpsprov/networkcontroller-server-wmi-provider-portal)
</dt> <dd>

此提供者可讓您管理網路控制站伺服器。

</dd> <dt>

<span id="NFS"></span><span id="nfs"></span>[Nfs](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)
</dt> <dd>

Provider for NFS 可讓您建立工具和腳本，以設定和監視 Windows 網路檔案系統。

</dd> <dt>

<span id="Ping"></span><span id="ping"></span><span id="PING"></span>[坪](/previous-versions/windows/desktop/wmipicmp/ping-provider)
</dt> <dd>

Ping 提供者會提供標準 Ping 命令所提供之狀態資訊的存取權。

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>[政策](/previous-versions/windows/desktop/policmanprov/policy-provider)
</dt> <dd>

提供群組原則的延伸模組，並允許在原則的應用程式中進行調整。

</dd> <dt>

<span id="Power_Meter"></span><span id="power_meter"></span><span id="POWER_METER"></span>[電源計量](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-)
</dt> <dd>

電源計量提供者支援 (PMB) 介面的電源計量和預算。 這些類別是用來查詢電源計量介面的主要介面 (從系統上基礎功率計量中的 PMI) 資訊。

</dd> <dt>

<span id="Power_Policy"></span><span id="power_policy"></span><span id="POWER_POLICY"></span>[電源原則](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-)
</dt> <dd>

電源原則提供者讓類別能夠從遠端系統管理所有的電源原則基礎結構。

</dd> <dt>

<span id="RAMgmtPSProvider"></span><span id="ramgmtpsprovider"></span><span id="RAMGMTPSPROVIDER"></span>[RAMgmtPSProvider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management)
</dt> <dd>

[RAMgmtPSProvider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management)提供者會提供類別來管理遠端存取。

</dd> <dt>

<span id="RAServerPSProvider"></span><span id="raserverpsprovider"></span><span id="RASERVERPSPROVIDER"></span>[RAServerPSProvider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server)
</dt> <dd>

[RAServerPSProvider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server)提供者提供了管理遠端存取服務器的類別。

</dd> <dt>

<span id="ReliabilityMetricsProvider"></span><span id="reliabilitymetricsprovider"></span><span id="RELIABILITYMETRICSPROVIDER"></span>[ReliabilityMetricsProvider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes)
</dt> <dd>

[ReliabilityMetricsProvider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes)提供者會公開系統和 Windows 事件記錄檔的可靠性計量。

</dd> <dt>

<span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>[遠端桌面服務](/windows/desktop/TermServ/terminal-services-wmi-provider)
</dt> <dd>

在遠端桌面服務環境中啟用一致的伺服器管理。

</dd> <dt>

<span id="Reporting_Services"></span><span id="reporting_services"></span><span id="REPORTING_SERVICES"></span>[Reporting Services](https://msdn.microsoft.com/library/Aa226200.aspx)
</dt> <dd>

定義類別，可讓您撰寫腳本和程式碼，以修改報表伺服器和報表管理員的設定。

</dd> <dt>

<span id="Resultant_Set_of_Policy__RSoP_"></span><span id="resultant_set_of_policy__rsop_"></span><span id="RESULTANT_SET_OF_POLICY__RSOP_"></span>[原則結果組 (RSoP) ](/previous-versions/windows/desktop/Policy/reporting-group-policy)
</dt> <dd>

提供在假設情況下規劃和偵測原則設定的方法。 這些方法可讓系統管理員輕鬆地判斷適用于或套用至使用者或電腦的原則設定組合。 這就是所謂的原則結果組 (RSoP) 。 如需詳細資訊，請參閱 [關於 RSOP Wmi 方法提供者](/previous-versions/windows/desktop/Policy/about-the-rsop-wmi-method-provider) 和 [rsop wmi 類別](/previous-versions/windows/desktop/Policy/rsop-wmi-classes)。

</dd> <dt>

<span id="Security"></span><span id="security"></span><span id="SECURITY"></span>[安全](/previous-versions/windows/desktop/secrcw32prov/security-provider)
</dt> <dd>

抓取或變更安全性設定，以控制對檔案、目錄和共用的擁有權、審核和存取權限。

</dd> <dt>

<span id="ServerManager.DeploymentProvider"></span><span id="servermanager.deploymentprovider"></span><span id="SERVERMANAGER.DEPLOYMENTPROVIDER"></span>[ServerManager. DeploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment)
</dt> <dd>

[ServerManager](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment)會公開部署功能。

</dd> <dt>

<span id="Session"></span><span id="session"></span><span id="SESSION"></span>[會話](/previous-versions/windows/desktop/wmipsess/session-provider)
</dt> <dd>

管理網路會話與連接。

</dd> <dt>

<span id="Shadow_Copy"></span><span id="shadow_copy"></span><span id="SHADOW_COPY"></span>[陰影複製](/previous-versions/windows/desktop/vsswmi/shadow-copy-provider)
</dt> <dd>

為共用資料夾功能的陰影複製提供管理功能。

</dd> <dt>

<span id="Shielded_VM_Provisioning"></span><span id="shielded_vm_provisioning"></span><span id="SHIELDED_VM_PROVISIONING"></span>[受防護的 VM 布建](/previous-versions/windows/desktop/mspsprov/shielded-vm-provisioning-wmi-provider-portal)
</dt> <dd>

受防護的 VM 布建提供者可讓網狀架構控制器在 Hyper-v 主機上開始安全布建受防護的 VM。

</dd> <dt>

<span id="Shielded_VM_Provisioning_Service"></span><span id="shielded_vm_provisioning_service"></span><span id="SHIELDED_VM_PROVISIONING_SERVICE"></span>[受防護的 VM 布建服務](/previous-versions/windows/desktop/mspsserviceprov/shielded-vm-provisioning-service-wmi-provider-portal)
</dt> <dd>

此提供者可讓您布建受防護的虛擬機器。

</dd> <dt>

<span id="SMB_Management"></span><span id="smb_management"></span><span id="SMB_MANAGEMENT"></span>[SMB 管理](/previous-versions/windows/desktop/smb/smb-management-api-portal)
</dt> <dd>

SMB 管理 API 提供類別和方法來管理共用和共用存取。

</dd> <dt>

<span id="SNMP"></span><span id="snmp"></span>[Snmp](/windows/desktop/WmiSdk/snmp-provider)
</dt> <dd>

將簡單的網路管理通訊協定 (SNMP) 物件，這些物件定義于管理資訊基礎 (MIB) 架構物件至類別中。 如需詳細資訊，請參閱 [設定 WMI SNMP 環境](/windows/desktop/WmiSdk/setting-up-the-wmi-snmp-environment)。

</dd> <dt>

<span id="Software_Inventory_Logging"></span><span id="software_inventory_logging"></span><span id="SOFTWARE_INVENTORY_LOGGING"></span>[軟體清查記錄](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)
</dt> <dd>

軟體清查記錄提供者會收集安裝在 Windows 伺服器上之軟體的授權資料，並提供資料的遠端存取，讓資料中心可以輕鬆地匯總資料。

</dd> <dt>

<span id="Software_Licensing_for_"></span><span id="software_licensing_for_"></span><span id="SOFTWARE_LICENSING_FOR_"></span>[Windows Vista 的軟體授權](/previous-versions/windows/desktop/slwmiprov/software-licensing-classes-for-windows-vista)
</dt> <dd>

用於 Windows Vista 的[軟體授權類別](/previous-versions/windows/desktop/sppwmi/software-license-provider-)。

</dd> <dt>

<span id="Software_License"></span><span id="software_license"></span><span id="SOFTWARE_LICENSE"></span>[軟體授權](/previous-versions/windows/desktop/sppwmi/software-license-provider-)
</dt> <dd>

軟體授權提供者會捕獲軟體授權資料。

</dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>[存放磁片區](/previous-versions/windows/desktop/vdswmi/storage-volume-provider)
</dt> <dd>

存放磁片區提供者會提供磁片區管理功能。

</dd> <dt>

<span id="Storage_Replica"></span><span id="storage_replica"></span><span id="STORAGE_REPLICA"></span>[儲存體複本](/previous-versions/windows/desktop/wvrcimprov/storage-replica-mi-provider-portal)
</dt> <dd>

此提供者可讓您管理儲存體複本。

</dd> <dt>

<span id="System_Registry"></span><span id="system_registry"></span><span id="SYSTEM_REGISTRY"></span>[系統登錄](/previous-versions/windows/desktop/regprov/system-registry-provider)
</dt> <dd>

系統登錄提供者可讓管理應用程式取出和修改系統登錄中的資料，並在發生變更時收到通知。

</dd> <dt>

<span id="System_Restore"></span><span id="system_restore"></span><span id="SYSTEM_RESTORE"></span>[系統還原](/windows/desktop/sr/system-restore-portal)
</dt> <dd>

提供可設定和使用系統還原功能的類別。 如需詳細資訊，請參閱設定 [系統還原](/windows/desktop/sr/configuring-system-restore) 和 [系統還原 WMI 類別](/windows/desktop/sr/system-restore-wmi-classes)。

</dd> <dt>

<span id="Trusted_Platform_Module"></span><span id="trusted_platform_module"></span><span id="TRUSTED_PLATFORM_MODULE"></span>[信賴平臺模組](/windows/desktop/SecProv/trusted-platform-module-provider)
</dt> <dd>

提供安全性裝置相關資料的存取權，該安全性裝置是由 [**Win32 \_ TPM**](/windows/desktop/SecProv/win32-tpm)的實例所代表，也就是 Microsoft Windows 信賴平臺電腦系統的根信任。

</dd> <dt>

<span id="Trustmon"></span><span id="trustmon"></span><span id="TRUSTMON"></span>[Trustmon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider)
</dt> <dd>

[Trustmon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider)提供者是一個執行個體提供者，可使用網域之間的信任關係相關資訊建立類別。

</dd> <dt>

<span id="User_Access_Logging"></span><span id="user_access_logging"></span><span id="USER_ACCESS_LOGGING"></span>[使用者存取記錄](/previous-versions/windows/desktop/ual/user-access-logging)
</dt> <dd>

使用者存取記錄 (UAL) 是 Windows Server 角色的通用架構，可報告其各自的耗用量計量。

</dd> <dt>

<span id="UserProfileProvider"></span><span id="userprofileprovider"></span><span id="USERPROFILEPROVIDER"></span>[UserProfileProvider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes)
</dt> <dd>

[UserProfileProvider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes)提供者會公開類別，以提供 Windows 系統上使用者設定檔的相關資訊，以及重新導向之使用者資料夾的健康情況狀態。

</dd> <dt>

<span id="User_State_Management"></span><span id="user_state_management"></span><span id="USER_STATE_MANAGEMENT"></span>[使用者狀態管理](/previous-versions/windows/desktop/usm/user-state-management-api-portal)
</dt> <dd>

使用者狀態管理提供者會公開適用于企業案例的管理和報告 API。

</dd> <dt>

<span id="View"></span><span id="view"></span><span id="VIEW"></span>[視圖](/windows/desktop/WmiSdk/view-provider)
</dt> <dd>

根據其他類別的實例建立新的實例和方法。 64位平臺上有兩個版本的 View provider。

</dd> <dt>

<span id="VPNClientPSProvider"></span><span id="vpnclientpsprovider"></span><span id="VPNCLIENTPSPROVIDER"></span>[VPNClientPSProvider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client)
</dt> <dd>

[VPNClientPSProvider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client)提供者會公開平臺，以自動化虛擬私人網路用戶端的連線。

</dd> <dt>

<span id="WDM"></span><span id="wdm"></span>[Wdm](/windows/desktop/WmiCoreProv/wdm-provider)
</dt> <dd>

針對符合 Windows Driver Model (WDM) 的硬體驅動程式，提供其類別、實例、方法和事件的存取權。

</dd> <dt>

<span id="WFasCim"></span><span id="wfascim"></span><span id="WFASCIM"></span>[WFasCim](/previous-versions/windows/desktop/wfascimprov/network-security-classes)
</dt> <dd>

[WFasCim](/previous-versions/windows/desktop/wfascimprov/network-security-classes)提供者會公開網路安全性和篩選功能。

</dd> <dt>

<span id="WhqlProvider"></span><span id="whqlprovider"></span><span id="WHQLPROVIDER"></span>[WhqlProvider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes)
</dt> <dd>

[WhqlProvider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes)提供者會公開有關驅動程式的數位簽章資訊。

</dd> <dt>

<span id="Win32ClockProvider"></span><span id="win32clockprovider"></span><span id="WIN32CLOCKPROVIDER"></span>[Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes)
</dt> <dd>

[Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes)提供者會公開電腦系統上以目前、本機和 UTC 為基礎的時間戳記。

</dd> <dt>

<span id="Windows_Data_Access_Components__WDAC_"></span><span id="windows_data_access_components__wdac_"></span><span id="WINDOWS_DATA_ACCESS_COMPONENTS__WDAC_"></span>[Windows Data Access Components (WDAC) ](/previous-versions/windows/desktop/wdacwmiprov/windows-data-access-components-wmi-provider-portal)
</dt> <dd>

提供 WDAC 的管理。

</dd> <dt>

<span id="Windows_Defender"></span><span id="windows_defender"></span><span id="WINDOWS_DEFENDER"></span>[Windows Defender](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)
</dt> <dd>

Windows Defender 提供者會公開 Windows Defender 的安全性功能。

</dd> <dt>

<span id="Windows_Installer"></span><span id="windows_installer"></span><span id="WINDOWS_INSTALLER"></span>[Windows Installer](/previous-versions/windows/desktop/msiprov/windows-installer-provider)
</dt> <dd>

Windows Installer 提供者（也稱為 MSI 提供者）可讓應用程式存取從 Windows Installer 相容的應用程式收集而來的資訊。

</dd> <dt>

<span id="Windows_Product_Activation"></span><span id="windows_product_activation"></span><span id="WINDOWS_PRODUCT_ACTIVATION"></span>[Windows 產品啟用](/previous-versions/windows/desktop/licwmiprov/windows-product-activation-provider)
</dt> <dd>

Windows 產品啟用 (WPA) 提供者是一種反盜版技術，旨在減少軟體的偶爾複製。

</dd> <dt>

<span id="Windows_Server_Manager"></span><span id="windows_server_manager"></span><span id="WINDOWS_SERVER_MANAGER"></span>[Windows 伺服器管理員](/previous-versions/windows/desktop/mgmtprovider/windows-server-manager-wmi-provider-portal)
</dt> <dd>

提供者可以存取和管理伺服器管理員應用程式所控制的設定。

</dd> <dt>

<span id="Windows_Server_Storage_Management__MsftStrgMan_"></span><span id="windows_server_storage_management__msftstrgman_"></span><span id="WINDOWS_SERVER_STORAGE_MANAGEMENT__MSFTSTRGMAN_"></span>[Windows Server 存放裝置管理 (MsftStrgMan) ](/previous-versions/windows/desktop/msftstrgmanprov/windows-storage-management-wmi-provider-portal)
</dt> <dd>

MsftStrgMan 提供者為 Windows Server 產品上的儲存系統提供管理。

</dd> <dt>

<span id="Windows_Storage_Management__StrgMgmt_"></span><span id="windows_storage_management__strgmgmt_"></span><span id="WINDOWS_STORAGE_MANAGEMENT__STRGMGMT_"></span>[Windows 存放裝置管理 (StrgMgmt) ](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
</dt> <dd>

StrgMgmt 提供者可以用來管理各種不同的儲存體設定，從平板電腦到伺服器上的外部存放裝置陣列。

</dd> <dt>

<span id="Windows_System_Assessment_Tool"></span><span id="windows_system_assessment_tool"></span><span id="WINDOWS_SYSTEM_ASSESSMENT_TOOL"></span>[Windows 系統評定工具](/windows/desktop/WinSAT/winsat-mof-classes)
</dt> <dd>

Windows 系統評定工具 (WinSAT) 會公開一些可評估電腦效能特性和功能的類別。

</dd> <dt>

<span id="WMI_Core"></span><span id="wmi_core"></span><span id="WMI_CORE"></span>[WMI 核心](/windows/desktop/WmiCoreProv/wmi-core-provider-)
</dt> <dd>

WMI 核心提供者會定義組成 WMI 核心功能的類別。

</dd> <dt>

<span id="Msft_ProviderSubSystem"></span><span id="msft_providersubsystem"></span><span id="MSFT_PROVIDERSUBSYSTEM"></span>[Msft \_ ProviderSubSystem](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-)
</dt> <dd>

[Msft \_ ProviderSubSystem](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-)提供者支援提供者。

</dd> <dt>

<span id="Win32_Perf"></span><span id="win32_perf"></span><span id="WIN32_PERF"></span>[Win32 \_ 效能](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov)
</dt> <dd>

[**Win32 效能 \_**](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov)抽象類別是效能計數器類別 [**Win32 \_ PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov)和 [**win32 \_ PerfFormattedData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov)的基類（base class）。 它會定義效能計數器類別的 CounterType 演算法中所使用的時間戳記和頻率屬性。

</dd> <dt>

<span id="Win32_PerfFormattedData"></span><span id="win32_perfformatteddata"></span><span id="WIN32_PERFFORMATTEDDATA"></span>[**Win32 \_ PerfFormattedData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov)
</dt> <dd>

預先安裝的計算資料類別的抽象基類。

</dd> <dt>

<span id="Win32_PerfRawData"></span><span id="win32_perfrawdata"></span><span id="WIN32_PERFRAWDATA"></span>[**Win32 \_ PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov)
</dt> <dd>

效能計數器類別 [**Win32 \_ PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) 是所有具體原始效能計數器類別的抽象基類。 若要顯示在 [系統監視器] 中，您必須將效能計數器類別新增至「根 \\ CIMv2」命名空間，並從 **Win32 \_ PerfRawData** 衍生。

</dd> <dt>

<span id="WMIPerfClass"></span><span id="wmiperfclass"></span><span id="WMIPERFCLASS"></span>[WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider)
</dt> <dd>

建立 WMI [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes)。 WMIPerfInst 提供者會動態提供這些效能類別的資料。

</dd> <dt>

<span id="WmiPerfInst"></span><span id="wmiperfinst"></span><span id="WMIPERFINST"></span>[WmiPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider)
</dt> <dd>

從 [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes) 定義動態提供原始和格式化的效能計數器資料。

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>[工作資料夾](/previous-versions/windows/desktop/syncshareservermgmt/sync-share-server-management-portal)
</dt> <dd>

工作資料夾用來同步處理多部電腦和行動裝置的檔案。

</dd> </dl>

 

 
