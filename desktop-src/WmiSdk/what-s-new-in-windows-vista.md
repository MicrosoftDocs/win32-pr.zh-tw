---
description: 從 Windows Vista 開始，wmi 包含許多以 wmi 使用者要求為基礎的新功能。
ms.assetid: 604a86d2-9a8e-4266-93b8-13676f768b29
ms.tgt_platform: multiple
title: Windows Vista 的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c47a2e63307004430099923d3d0a151ed9122b7fb96ff127c59145f1a911a1dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553263"
---
# <a name="whats-new-in-windowsvista"></a>Windows Vista 的新功能

從 Windows Vista 開始，wmi 包含許多以 wmi 使用者要求為基礎的新功能。

-   [新的疑難排解工具](#new-troubleshooting-tool)
-   [Windows Vista 中的新安全性功能](#new-security-features-in-windows-vista)
-   [Windows Vista 中的其他新功能](#other-new-features-in-windows-vista)
-   [相關主題](#related-topics)

## <a name="new-troubleshooting-tool"></a>新的疑難排解工具

有新的疑難排解工具可供下載。

<dl> <dt>

<span id="WMI_Diagnosis_Utility"></span><span id="wmi_diagnosis_utility"></span><span id="WMI_DIAGNOSIS_UTILITY"></span>WMI Diagnosis Utility
</dt> <dd>

此公用程式會檢查本機電腦上 WMI 服務的目前狀態以及相關元件、DCOM 設定和登錄設定。 此公用程式會報告問題，並提供修復的建議。 如需詳細資訊及下載公用程式，請參閱[WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en)。

</dd> </dl>

## <a name="new-security-features-in-windows-vista"></a>Windows Vista 中的新安全性功能

下列清單列出 Windows Vista 中可用的新 WMI 安全性功能。

<dl> <dt>

<span id="Tracing_and_logging_events"></span><span id="tracing_and_logging_events"></span><span id="TRACING_AND_LOGGING_EVENTS"></span>追蹤和記錄事件
</dt> <dd>

WMI 服務不再使用大部分的 [Wmi 記錄](wmi-log-files.md)檔。 相反地，它會使用 [事件追蹤](/windows/desktop/ETW/event-tracing-portal) (ETW) ，而事件則是透過 **事件檢視器** UI 或 Wevtutil 命令列工具提供。 如需詳細資訊，請參閱 [追蹤 WMI 活動](tracing-wmi-activity.md)。

</dd> <dt>

<span id="Setting_WMI_namespace_security_in_the_MOF_file"></span><span id="setting_wmi_namespace_security_in_the_mof_file"></span><span id="SETTING_WMI_NAMESPACE_SECURITY_IN_THE_MOF_FILE"></span>設定 MOF 檔案中的 WMI 命名空間安全性
</dt> <dd>

**NamespaceSecuritySDDL** 限定詞可以用來保護任何命名空間。 如需詳細資訊，請參閱 [在建立命名空間時設定命名空間安全性](setting-namespace-security-when-the-namespace-is-created.md)。

</dd> <dt>

<span id="Security_Auditing_of_WMI_namespaces"></span><span id="security_auditing_of_wmi_namespaces"></span><span id="SECURITY_AUDITING_OF_WMI_NAMESPACES"></span>WMI 命名空間的安全性審核
</dt> <dd>

WMI 會使用命名空間系統存取控制清單 (SACL) 來審核命名空間活動，並將附隨報告到安全性事件記錄檔。 如需詳細資訊，請參閱 [存取 WMI 命名空間](access-to-wmi-namespaces.md) 和 [設定命名空間安全描述項](setting-namespace-security-descriptors.md)。

</dd> <dt>

<span id="Get_and_Set_security_descriptor_methods_for_securable_objects"></span><span id="get_and_set_security_descriptor_methods_for_securable_objects"></span><span id="GET_AND_SET_SECURITY_DESCRIPTOR_METHODS_FOR_SECURABLE_OBJECTS"></span>取得和設定安全物件的安全描述項方法
</dt> <dd>

[**Win32 \_ 印表機**](/windows/desktop/CIMWin32Prov/win32-printer)、 [**win32 \_ Service**](/windows/desktop/CIMWin32Prov/win32-service)、 [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov)、 [**win32 \_ DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)和 [**\_ \_ SystemSecurity**](--systemsecurity.md)已新增可用於取得及設定安全描述項的新可編寫腳本方法。 如需詳細資訊，請參閱 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。

</dd> <dt>

<span id="Manipulate_Security_Descriptors_in_scripts"></span><span id="manipulate_security_descriptors_in_scripts"></span><span id="MANIPULATE_SECURITY_DESCRIPTORS_IN_SCRIPTS"></span>在腳本中操作安全描述項
</dt> <dd>

[**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)類別具有允許腳本將安全物件上的二進位安全描述項轉換成 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)物件或 [安全描述項定義語言](/windows/desktop/SecAuthZ/security-descriptor-definition-language)字串的方法。 如需詳細資訊，請參閱 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。

</dd> <dt>

<span id="User_Account_Control"></span><span id="user_account_control"></span><span id="USER_ACCOUNT_CONTROL"></span>使用者帳戶控制
</dt> <dd>

 (UAC) 的使用者帳戶控制會影響傳回的 WMI 資料、遠端存取，以及腳本必須如何執行。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](user-account-control-and-wmi.md)。 如需 UAC 的詳細資訊，請參閱[Windows Vista 上的開始使用與使用者帳戶控制](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista)。

</dd> </dl>

## <a name="other-new-features-in-windows-vista"></a>Windows Vista 中的其他新功能

下列清單列出 Windows Vista 中可用的新 WMI 功能。

<dl> <dt>

<span id="New_performance_counter_data_providers"></span><span id="new_performance_counter_data_providers"></span><span id="NEW_PERFORMANCE_COUNTER_DATA_PROVIDERS"></span>新的效能計數器資料提供者
</dt> <dd>

自動探索/AutoPurge (ADAP) 進程不再將效能計數器物件傳輸至 WMI 儲存機制中的 WMI 效能類別。 如需詳細資訊，請參閱 [效能程式庫和 WMI](performance-libraries-and-wmi.md)。 [WMIPerfClass 提供者](wmiperfclass-provider.md)會建立 WMI 效能計數器類別。 [WMIPerfInst 提供者](wmiperfinst-provider.md)會動態提供這些 WMI 效能類別的資料。

</dd> <dt>

<span id="Indexer_for_collections"></span><span id="indexer_for_collections"></span><span id="INDEXER_FOR_COLLECTIONS"></span>集合的索引子
</dt> <dd>

[**SWbemObject. ItemIndex**](swbemobjectset-itemindex.md)方法會將與指定索引相關聯的物件傳回集合中。

</dd> <dt>

<span id="Support_for_IPv6_and_IPv4"></span><span id="support_for_ipv6_and_ipv4"></span><span id="SUPPORT_FOR_IPV6_AND_IPV4"></span>支援 IPv6 和 IPv4
</dt> <dd>

WMI [IP 路由提供者](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) 和網路類別可提供 IPv4 位址的資料。 從 Windows Vista 開始，WMI 也提供對 IPv6 網路功能的有限支援。 如需詳細資訊，請參閱 [WMI 中的 IPv6 和 IPv4 支援](ipv6-and-ipv4-support-in-wmi.md)。

</dd> <dt>

<span id="Changes_to_remote_connections"></span><span id="changes_to_remote_connections"></span><span id="CHANGES_TO_REMOTE_CONNECTIONS"></span>遠端連線的變更
</dt> <dd>

連接到執行 Windows Vista 之遠端電腦上的 WMI 命名空間，可能需要變更[Windows 防火牆](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx)、[使用者帳戶控制](/previous-versions/aa905108(v=msdn.10))或 DCOM 的設定。 如需詳細資訊，請參閱 [從 Vista 開始遠端連線到 WMI](connecting-to-wmi-remotely-starting-with-vista.md)。

</dd> <dt>

<span id="Changes_to_________Win32_QuickFixEngineering"></span><span id="changes_to_________win32_quickfixengineering"></span><span id="CHANGES_TO_________WIN32_QUICKFIXENGINEERING"></span>[ **Win32 \_ QuickFixEngineering** 的變更](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)
</dt> <dd>

針對在 Windows Vista 和更新版本的作業系統上執行的系統，這個類別只會傳回以元件為基礎的服務 (CBS) 所提供的更新。 這些更新不會列在登錄中。 [**Win32 \_ QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)不會傳回 Windows Installer (MSI) 或 [Windows Update](https://update.microsoft.com/microsoftupdate/v6/default.aspx?ln=en-us)所提供的更新。

</dd> <dt>

<span id="Enabling_and_disabling_a_NIC"></span><span id="enabling_and_disabling_a_nic"></span><span id="ENABLING_AND_DISABLING_A_NIC"></span>啟用和停用 NIC
</dt> <dd>

[**Win32 \_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) 有新的方法可啟用和停用網路介面卡。

</dd> <dt>

<span id="Windows_Installer_Provider_changes"></span><span id="windows_installer_provider_changes"></span><span id="WINDOWS_INSTALLER_PROVIDER_CHANGES"></span>Windows安裝程式提供者變更
</dt> <dd>

[**Win32 \_產品**](/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)) 有新的屬性和方法，可提供更多關於產品的資料。

</dd> <dt>

<span id="New_display_monitor_classes"></span><span id="new_display_monitor_classes"></span><span id="NEW_DISPLAY_MONITOR_CLASSES"></span>新的顯示器監視類別
</dt> <dd>

[監視器顯示類別](/windows/desktop/WmiCoreProv/wmi-core-provider-) 包含 [WDM 提供者](/windows/desktop/WmiCoreProv/wdm-provider) 所提供的資料，可提供顯示監視器的相關資料。

</dd> <dt>

<span id="Intelligent_Platform_Management_Interface_provider"></span><span id="intelligent_platform_management_interface_provider"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE_PROVIDER"></span>智慧型平臺管理介面提供者
</dt> <dd>

WMI [IPMI 提供者](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) 提供基礎板管理控制器 (BMC) 作業到作業系統的資料。 此提供者會將資訊提供給智慧型平臺管理資訊類別，以提供感應器資料和 BMC 系統事件記錄檔 (的) 訊息資料。

</dd> <dt>

<span id="Detecting_hyperthreading_and_multicore_processors"></span><span id="detecting_hyperthreading_and_multicore_processors"></span><span id="DETECTING_HYPERTHREADING_AND_MULTICORE_PROCESSORS"></span>偵測超執行緒和多核心處理器
</dt> <dd>

[**Win32 \_電腦系統和**](/windows/desktop/CIMWin32Prov/win32-computersystem) [**Win32 \_ 處理器**](/windows/desktop/CIMWin32Prov/win32-processor) 都有新的屬性，可讓您撰寫腳本來判斷電腦系統是否有多核心或超執行緒處理器。

</dd> <dt>

<span id="Event_messages"></span><span id="event_messages"></span><span id="EVENT_MESSAGES"></span>事件訊息
</dt> <dd>

WindowsVista 有新的事件訊息。 如需詳細資訊，請參閱 [WMI 事件](wmi-events.md)。

</dd> <dt>

<span id="Inventory_improvements"></span><span id="inventory_improvements"></span><span id="INVENTORY_IMPROVEMENTS"></span>清查改進
</dt> <dd>

許多硬體類別都有變更來改善硬體清查。 例如，在 [**win32 \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) 和 [**win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive)中加入了序號屬性。

</dd> <dt>

<span id="New_provider_hosting_models"></span><span id="new_provider_hosting_models"></span><span id="NEW_PROVIDER_HOSTING_MODELS"></span>新的提供者裝載模型
</dt> <dd>

已針對 Windows Vista 加入新的提供者裝載模型。 如需詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 WMI](about-wmi.md)
</dt> </dl>

 

 
