---
description: 從 Windows Vista 開始，WMI 包含許多以 WMI 使用者要求為基礎的新功能。
ms.assetid: 604a86d2-9a8e-4266-93b8-13676f768b29
ms.tgt_platform: multiple
title: Windows Vista 的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee950becb906f89445f9ddfb258f4f7a608ce1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991936"
---
# <a name="whats-new-in-windowsvista"></a><span data-ttu-id="80f07-103">Windows Vista 的新功能</span><span class="sxs-lookup"><span data-stu-id="80f07-103">Whats New in Windows�Vista</span></span>

<span data-ttu-id="80f07-104">從 Windows Vista 開始，WMI 包含許多以 WMI 使用者要求為基礎的新功能。</span><span class="sxs-lookup"><span data-stu-id="80f07-104">Starting with Windows Vista, WMI contains many new features based upon requests by WMI users.</span></span>

-   [<span data-ttu-id="80f07-105">新的疑難排解工具</span><span class="sxs-lookup"><span data-stu-id="80f07-105">New Troubleshooting Tool</span></span>](#new-troubleshooting-tool)
-   [<span data-ttu-id="80f07-106">Windows Vista 中的新安全性功能</span><span class="sxs-lookup"><span data-stu-id="80f07-106">New Security Features in Windows Vista</span></span>](#new-security-features-in-windows-vista)
-   [<span data-ttu-id="80f07-107">Windows Vista 中的其他新功能</span><span class="sxs-lookup"><span data-stu-id="80f07-107">Other New Features in Windows Vista</span></span>](#other-new-features-in-windows-vista)
-   [<span data-ttu-id="80f07-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="80f07-108">Related topics</span></span>](#related-topics)

## <a name="new-troubleshooting-tool"></a><span data-ttu-id="80f07-109">新的疑難排解工具</span><span class="sxs-lookup"><span data-stu-id="80f07-109">New Troubleshooting Tool</span></span>

<span data-ttu-id="80f07-110">有新的疑難排解工具可供下載。</span><span class="sxs-lookup"><span data-stu-id="80f07-110">A new troubleshooting tool is available for download.</span></span>

<dl> <dt>

<span data-ttu-id="80f07-111"><span id="WMI_Diagnosis_Utility"></span><span id="wmi_diagnosis_utility"></span><span id="WMI_DIAGNOSIS_UTILITY"></span>WMI Diagnosis Utility</span><span class="sxs-lookup"><span data-stu-id="80f07-111"><span id="WMI_Diagnosis_Utility"></span><span id="wmi_diagnosis_utility"></span><span id="WMI_DIAGNOSIS_UTILITY"></span>WMI Diagnosis Utility</span></span>
</dt> <dd>

<span data-ttu-id="80f07-112">此公用程式會檢查本機電腦上 WMI 服務的目前狀態以及相關元件、DCOM 設定和登錄設定。</span><span class="sxs-lookup"><span data-stu-id="80f07-112">This utility examines the current state of the WMI service and related components, DCOM settings, and registry settings on the local computer.</span></span> <span data-ttu-id="80f07-113">此公用程式會報告問題，並提供修復的建議。</span><span class="sxs-lookup"><span data-stu-id="80f07-113">The utility reports problems and offers suggestions for repair.</span></span> <span data-ttu-id="80f07-114">如需詳細資訊及下載公用程式，請參閱 [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en)。</span><span class="sxs-lookup"><span data-stu-id="80f07-114">For more information and to download the utility, see [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en).</span></span>

</dd> </dl>

## <a name="new-security-features-in-windows-vista"></a><span data-ttu-id="80f07-115">Windows Vista 中的新安全性功能</span><span class="sxs-lookup"><span data-stu-id="80f07-115">New Security Features in Windows Vista</span></span>

<span data-ttu-id="80f07-116">下列清單列出 Windows Vista 中可用的新 WMI 安全性功能。</span><span class="sxs-lookup"><span data-stu-id="80f07-116">The following list lists the new WMI security features that are available in Windows Vista.</span></span>

<dl> <dt>

<span data-ttu-id="80f07-117"><span id="Tracing_and_logging_events"></span><span id="tracing_and_logging_events"></span><span id="TRACING_AND_LOGGING_EVENTS"></span>追蹤和記錄事件</span><span class="sxs-lookup"><span data-stu-id="80f07-117"><span id="Tracing_and_logging_events"></span><span id="tracing_and_logging_events"></span><span id="TRACING_AND_LOGGING_EVENTS"></span>Tracing and logging events</span></span>
</dt> <dd>

<span data-ttu-id="80f07-118">WMI 服務不再使用大部分的 [Wmi 記錄](wmi-log-files.md)檔。</span><span class="sxs-lookup"><span data-stu-id="80f07-118">WMI service no longer uses most of the [WMI Log Files](wmi-log-files.md).</span></span> <span data-ttu-id="80f07-119">相反地，它會使用 [事件追蹤](/windows/desktop/ETW/event-tracing-portal) (ETW) ，而事件則是透過 **事件檢視器** UI 或 Wevtutil 命令列工具提供。</span><span class="sxs-lookup"><span data-stu-id="80f07-119">Instead it uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) and events are available through the **Event Viewer** UI or the Wevtutil command line tool.</span></span> <span data-ttu-id="80f07-120">如需詳細資訊，請參閱 [追蹤 WMI 活動](tracing-wmi-activity.md)。</span><span class="sxs-lookup"><span data-stu-id="80f07-120">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

</dd> <dt>

<span data-ttu-id="80f07-121"><span id="Setting_WMI_namespace_security_in_the_MOF_file"></span><span id="setting_wmi_namespace_security_in_the_mof_file"></span><span id="SETTING_WMI_NAMESPACE_SECURITY_IN_THE_MOF_FILE"></span>設定 MOF 檔案中的 WMI 命名空間安全性</span><span class="sxs-lookup"><span data-stu-id="80f07-121"><span id="Setting_WMI_namespace_security_in_the_MOF_file"></span><span id="setting_wmi_namespace_security_in_the_mof_file"></span><span id="SETTING_WMI_NAMESPACE_SECURITY_IN_THE_MOF_FILE"></span>Setting WMI namespace security in the MOF file</span></span>
</dt> <dd>

<span data-ttu-id="80f07-122">**NamespaceSecuritySDDL** 限定詞可以用來保護任何命名空間。</span><span class="sxs-lookup"><span data-stu-id="80f07-122">The **NamespaceSecuritySDDL** qualifier can be used to secure any namespace.</span></span> <span data-ttu-id="80f07-123">如需詳細資訊，請參閱 [在建立命名空間時設定命名空間安全性](setting-namespace-security-when-the-namespace-is-created.md)。</span><span class="sxs-lookup"><span data-stu-id="80f07-123">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span>

</dd> <dt>

<span data-ttu-id="80f07-124"><span id="Security_Auditing_of_WMI_namespaces"></span><span id="security_auditing_of_wmi_namespaces"></span><span id="SECURITY_AUDITING_OF_WMI_NAMESPACES"></span>WMI 命名空間的安全性審核</span><span class="sxs-lookup"><span data-stu-id="80f07-124"><span id="Security_Auditing_of_WMI_namespaces"></span><span id="security_auditing_of_wmi_namespaces"></span><span id="SECURITY_AUDITING_OF_WMI_NAMESPACES"></span>Security Auditing of WMI namespaces</span></span>
</dt> <dd>

<span data-ttu-id="80f07-125">WMI 會使用命名空間系統存取控制清單 (SACL) 來審核命名空間活動，並將附隨報告到安全性事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="80f07-125">WMI uses the namespace system access control lists (SACL) to audit namespace activity and report events to the Security event log.</span></span> <span data-ttu-id="80f07-126">如需詳細資訊，請參閱 [存取 WMI 命名空間](access-to-wmi-namespaces.md) 和 [設定命名空間安全描述項](setting-namespace-security-descriptors.md)。</span><span class="sxs-lookup"><span data-stu-id="80f07-126">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md) and [Setting Namespace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

</dd> <dt>

<span data-ttu-id="80f07-127"><span id="Get_and_Set_security_descriptor_methods_for_securable_objects"></span><span id="get_and_set_security_descriptor_methods_for_securable_objects"></span><span id="GET_AND_SET_SECURITY_DESCRIPTOR_METHODS_FOR_SECURABLE_OBJECTS"></span>取得和設定安全物件的安全描述項方法</span><span class="sxs-lookup"><span data-stu-id="80f07-127"><span id="Get_and_Set_security_descriptor_methods_for_securable_objects"></span><span id="get_and_set_security_descriptor_methods_for_securable_objects"></span><span id="GET_AND_SET_SECURITY_DESCRIPTOR_METHODS_FOR_SECURABLE_OBJECTS"></span>Get and Set security descriptor methods for securable objects</span></span>
</dt> <dd>

<span data-ttu-id="80f07-128">[**Win32 \_ 印表機**](/windows/desktop/CIMWin32Prov/win32-printer)、 [**win32 \_ Service**](/windows/desktop/CIMWin32Prov/win32-service)、 [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov)、 [**win32 \_ DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)和 [**\_ \_ SystemSecurity**](--systemsecurity.md)已新增可用於取得及設定安全描述項的新可編寫腳本方法。</span><span class="sxs-lookup"><span data-stu-id="80f07-128">New scriptable methods to get and set security descriptors have been added to [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer), [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), [**Win32\_DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting), and [**\_\_SystemSecurity**](--systemsecurity.md).</span></span> <span data-ttu-id="80f07-129">如需詳細資訊，請參閱 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="80f07-129">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="80f07-130"><span id="Manipulate_Security_Descriptors_in_scripts"></span><span id="manipulate_security_descriptors_in_scripts"></span><span id="MANIPULATE_SECURITY_DESCRIPTORS_IN_SCRIPTS"></span>在腳本中操作安全描述項</span><span class="sxs-lookup"><span data-stu-id="80f07-130"><span id="Manipulate_Security_Descriptors_in_scripts"></span><span id="manipulate_security_descriptors_in_scripts"></span><span id="MANIPULATE_SECURITY_DESCRIPTORS_IN_SCRIPTS"></span>Manipulate Security Descriptors in scripts</span></span>
</dt> <dd>

<span data-ttu-id="80f07-131">[**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)類別具有允許腳本將安全物件上的二進位安全描述項轉換成 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)物件或 [安全描述項定義語言](/windows/desktop/SecAuthZ/security-descriptor-definition-language)字串的方法。</span><span class="sxs-lookup"><span data-stu-id="80f07-131">The [**Win32\_SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) class has methods that allow scripts to convert binary security descriptors on securable objects to [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) objects or [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) strings.</span></span> <span data-ttu-id="80f07-132">如需詳細資訊，請參閱 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="80f07-132">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="80f07-133"><span id="User_Account_Control"></span><span id="user_account_control"></span><span id="USER_ACCOUNT_CONTROL"></span>使用者帳戶控制</span><span class="sxs-lookup"><span data-stu-id="80f07-133"><span id="User_Account_Control"></span><span id="user_account_control"></span><span id="USER_ACCOUNT_CONTROL"></span>User Account Control</span></span>
</dt> <dd>

<span data-ttu-id="80f07-134"> (UAC) 的使用者帳戶控制會影響傳回的 WMI 資料、遠端存取，以及腳本必須如何執行。</span><span class="sxs-lookup"><span data-stu-id="80f07-134">User Account Control (UAC) affects what WMI data is returned, remote access, and how scripts must be run.</span></span> <span data-ttu-id="80f07-135">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](user-account-control-and-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="80f07-135">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span> <span data-ttu-id="80f07-136">如需 UAC 的詳細資訊，請參閱 [使用 Windows Vista 的使用者帳戶控制開始使用](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista)。</span><span class="sxs-lookup"><span data-stu-id="80f07-136">For more information about UAC, see [Getting Started with User Account Control on Windows Vista](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).</span></span>

</dd> </dl>

## <a name="other-new-features-in-windows-vista"></a><span data-ttu-id="80f07-137">Windows Vista 中的其他新功能</span><span class="sxs-lookup"><span data-stu-id="80f07-137">Other New Features in Windows Vista</span></span>

<span data-ttu-id="80f07-138">下列清單列出 Windows Vista 中可用的新 WMI 功能。</span><span class="sxs-lookup"><span data-stu-id="80f07-138">The following list lists new WMI features that are available in Windows Vista.</span></span>

<dl> <dt>

<span data-ttu-id="80f07-139"><span id="New_performance_counter_data_providers"></span><span id="new_performance_counter_data_providers"></span><span id="NEW_PERFORMANCE_COUNTER_DATA_PROVIDERS"></span>新的效能計數器資料提供者</span><span class="sxs-lookup"><span data-stu-id="80f07-139"><span id="New_performance_counter_data_providers"></span><span id="new_performance_counter_data_providers"></span><span id="NEW_PERFORMANCE_COUNTER_DATA_PROVIDERS"></span>New performance counter data providers</span></span>
</dt> <dd>

<span data-ttu-id="80f07-140">自動探索/AutoPurge (ADAP) 進程不再將效能計數器物件傳輸至 WMI 儲存機制中的 WMI 效能類別。</span><span class="sxs-lookup"><span data-stu-id="80f07-140">The AutoDiscovery/AutoPurge (ADAP) process no longer transfers performance counter objects into WMI performance classes in the WMI repository.</span></span> <span data-ttu-id="80f07-141">如需詳細資訊，請參閱 [效能程式庫和 WMI](performance-libraries-and-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="80f07-141">For more information, see [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span> <span data-ttu-id="80f07-142">[WMIPerfClass 提供者](wmiperfclass-provider.md)會建立 WMI 效能計數器類別。</span><span class="sxs-lookup"><span data-stu-id="80f07-142">The [WMIPerfClass Provider](wmiperfclass-provider.md) creates the WMI Performance Counter Classes.</span></span> <span data-ttu-id="80f07-143">[WMIPerfInst 提供者](wmiperfinst-provider.md)會動態提供這些 WMI 效能類別的資料。</span><span class="sxs-lookup"><span data-stu-id="80f07-143">Data is dynamically supplied to these WMI performance classes by the [WMIPerfInst Provider](wmiperfinst-provider.md).</span></span>

</dd> <dt>

<span data-ttu-id="80f07-144"><span id="Indexer_for_collections"></span><span id="indexer_for_collections"></span><span id="INDEXER_FOR_COLLECTIONS"></span>集合的索引子</span><span class="sxs-lookup"><span data-stu-id="80f07-144"><span id="Indexer_for_collections"></span><span id="indexer_for_collections"></span><span id="INDEXER_FOR_COLLECTIONS"></span>Indexer for collections</span></span>
</dt> <dd>

<span data-ttu-id="80f07-145">[**SWbemObject. ItemIndex**](swbemobjectset-itemindex.md)方法會將與指定索引相關聯的物件傳回集合中。</span><span class="sxs-lookup"><span data-stu-id="80f07-145">The [**SWbemObject.ItemIndex**](swbemobjectset-itemindex.md) method returns the object associated with a specified index into a collection.</span></span>

</dd> <dt>

<span data-ttu-id="80f07-146"><span id="Support_for_IPv6_and_IPv4"></span><span id="support_for_ipv6_and_ipv4"></span><span id="SUPPORT_FOR_IPV6_AND_IPV4"></span>支援 IPv6 和 IPv4</span><span class="sxs-lookup"><span data-stu-id="80f07-146"><span id="Support_for_IPv6_and_IPv4"></span><span id="support_for_ipv6_and_ipv4"></span><span id="SUPPORT_FOR_IPV6_AND_IPV4"></span>Support for IPv6 and IPv4</span></span>
</dt> <dd>

<span data-ttu-id="80f07-147">WMI [IP 路由提供者](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) 和網路類別可提供 IPv4 位址的資料。</span><span class="sxs-lookup"><span data-stu-id="80f07-147">WMI [IP Route Provider](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) and network classes supply data for IPv4 addresses.</span></span> <span data-ttu-id="80f07-148">從 Windows Vista 開始，WMI 也提供對 IPv6 網路功能的有限支援。</span><span class="sxs-lookup"><span data-stu-id="80f07-148">Starting with Windows Vista, WMI also provides limited support for IPv6 network capabilities.</span></span> <span data-ttu-id="80f07-149">如需詳細資訊，請參閱 [WMI 中的 IPv6 和 IPv4 支援](ipv6-and-ipv4-support-in-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="80f07-149">For more information, see [IPv6 and IPv4 Support in WMI](ipv6-and-ipv4-support-in-wmi.md).</span></span>

</dd> <dt>

<span data-ttu-id="80f07-150"><span id="Changes_to_remote_connections"></span><span id="changes_to_remote_connections"></span><span id="CHANGES_TO_REMOTE_CONNECTIONS"></span>遠端連線的變更</span><span class="sxs-lookup"><span data-stu-id="80f07-150"><span id="Changes_to_remote_connections"></span><span id="changes_to_remote_connections"></span><span id="CHANGES_TO_REMOTE_CONNECTIONS"></span>Changes to remote connections</span></span>
</dt> <dd>

<span data-ttu-id="80f07-151">連接到執行 Windows Vista 的遠端電腦上的 WMI 命名空間，可能需要變更 [Windows 防火牆](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx)、 [使用者帳戶控制](/previous-versions/aa905108(v=msdn.10))或 DCOM 的設定。</span><span class="sxs-lookup"><span data-stu-id="80f07-151">Connecting to a WMI namespace on a remote computer running Windows Vista may require changes to settings for [Windows Firewall](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx), [User Account Control](/previous-versions/aa905108(v=msdn.10)), or DCOM.</span></span> <span data-ttu-id="80f07-152">如需詳細資訊，請參閱 [從 Vista 開始遠端連線到 WMI](connecting-to-wmi-remotely-starting-with-vista.md)。</span><span class="sxs-lookup"><span data-stu-id="80f07-152">For more information, see [Connecting to WMI Remotely Starting with Vista](connecting-to-wmi-remotely-starting-with-vista.md).</span></span>

</dd> <dt>

<span data-ttu-id="80f07-153"><span id="Changes_to_________Win32_QuickFixEngineering"></span><span id="changes_to_________win32_quickfixengineering"></span><span id="CHANGES_TO_________WIN32_QUICKFIXENGINEERING"></span>[ **Win32 \_ QuickFixEngineering** 的變更](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)</span><span class="sxs-lookup"><span data-stu-id="80f07-153"><span id="Changes_to_________Win32_QuickFixEngineering"></span><span id="changes_to_________win32_quickfixengineering"></span><span id="CHANGES_TO_________WIN32_QUICKFIXENGINEERING"></span>Changes to [**Win32\_QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)</span></span>
</dt> <dd>

<span data-ttu-id="80f07-154">如果是在 Windows Vista 和更新版本的作業系統上執行的系統，這個類別只會傳回以元件為基礎的服務 (CBS) 所提供的更新。</span><span class="sxs-lookup"><span data-stu-id="80f07-154">For systems running on the Windows Vista and later operating system, this class returns only the updates supplied by Component Based Servicing (CBS).</span></span> <span data-ttu-id="80f07-155">這些更新不會列在登錄中。</span><span class="sxs-lookup"><span data-stu-id="80f07-155">These updates are not listed in the registry.</span></span> <span data-ttu-id="80f07-156">[**Win32 \_ QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)不會傳回 Windows Installer (MSI) 或 [Windows Update](https://update.microsoft.com/microsoftupdate/v6/default.aspx?ln=en-us)所提供的更新。</span><span class="sxs-lookup"><span data-stu-id="80f07-156">Updates supplied by Windows Installer (MSI) or the [Windows Update](https://update.microsoft.com/microsoftupdate/v6/default.aspx?ln=en-us) are not returned by [**Win32\_QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering).</span></span>

</dd> <dt>

<span data-ttu-id="80f07-157"><span id="Enabling_and_disabling_a_NIC"></span><span id="enabling_and_disabling_a_nic"></span><span id="ENABLING_AND_DISABLING_A_NIC"></span>啟用和停用 NIC</span><span class="sxs-lookup"><span data-stu-id="80f07-157"><span id="Enabling_and_disabling_a_NIC"></span><span id="enabling_and_disabling_a_nic"></span><span id="ENABLING_AND_DISABLING_A_NIC"></span>Enabling and disabling a NIC</span></span>
</dt> <dd>

<span data-ttu-id="80f07-158">[**Win32 \_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) 有新的方法可啟用和停用網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="80f07-158">[**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) has new methods to enable and disable the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="80f07-159"><span id="Windows_Installer_Provider_changes"></span><span id="windows_installer_provider_changes"></span><span id="WINDOWS_INSTALLER_PROVIDER_CHANGES"></span>Windows Installer 提供者變更</span><span class="sxs-lookup"><span data-stu-id="80f07-159"><span id="Windows_Installer_Provider_changes"></span><span id="windows_installer_provider_changes"></span><span id="WINDOWS_INSTALLER_PROVIDER_CHANGES"></span>Windows Installer Provider changes</span></span>
</dt> <dd>

<span data-ttu-id="80f07-160">[**Win32 \_產品**](/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)) 有新的屬性和方法，可提供更多關於產品的資料。</span><span class="sxs-lookup"><span data-stu-id="80f07-160">[**Win32\_Product**](/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)) has new properties and methods to provide more data about the product.</span></span>

</dd> <dt>

<span data-ttu-id="80f07-161"><span id="New_display_monitor_classes"></span><span id="new_display_monitor_classes"></span><span id="NEW_DISPLAY_MONITOR_CLASSES"></span>新的顯示器監視類別</span><span class="sxs-lookup"><span data-stu-id="80f07-161"><span id="New_display_monitor_classes"></span><span id="new_display_monitor_classes"></span><span id="NEW_DISPLAY_MONITOR_CLASSES"></span>New display monitor classes</span></span>
</dt> <dd>

<span data-ttu-id="80f07-162">[監視器顯示類別](/windows/desktop/WmiCoreProv/wmi-core-provider-) 包含 [WDM 提供者](/windows/desktop/WmiCoreProv/wdm-provider) 所提供的資料，可提供顯示監視器的相關資料。</span><span class="sxs-lookup"><span data-stu-id="80f07-162">[Monitor Display Classes](/windows/desktop/WmiCoreProv/wmi-core-provider-) contain data supplied by the [WDM Provider](/windows/desktop/WmiCoreProv/wdm-provider) that provides data about display monitors.</span></span>

</dd> <dt>

<span data-ttu-id="80f07-163"><span id="Intelligent_Platform_Management_Interface_provider"></span><span id="intelligent_platform_management_interface_provider"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE_PROVIDER"></span>智慧型平臺管理介面提供者</span><span class="sxs-lookup"><span data-stu-id="80f07-163"><span id="Intelligent_Platform_Management_Interface_provider"></span><span id="intelligent_platform_management_interface_provider"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE_PROVIDER"></span>Intelligent Platform Management Interface provider</span></span>
</dt> <dd>

<span data-ttu-id="80f07-164">WMI [IPMI 提供者](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) 提供基礎板管理控制器 (BMC) 作業到作業系統的資料。</span><span class="sxs-lookup"><span data-stu-id="80f07-164">The WMI [IPMI Provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) supplies data from baseboard management controller (BMC) operations to the operating system.</span></span> <span data-ttu-id="80f07-165">此提供者會將資訊提供給智慧型平臺管理資訊類別，以提供感應器資料和 BMC 系統事件記錄檔 (的) 訊息資料。</span><span class="sxs-lookup"><span data-stu-id="80f07-165">The provider supplies information to the Intelligent Platform Management Information Classes, which provide sensors data and BMC System Event Log (SEL) message data.</span></span>

</dd> <dt>

<span data-ttu-id="80f07-166"><span id="Detecting_hyperthreading_and_multicore_processors"></span><span id="detecting_hyperthreading_and_multicore_processors"></span><span id="DETECTING_HYPERTHREADING_AND_MULTICORE_PROCESSORS"></span>偵測超執行緒和多核心處理器</span><span class="sxs-lookup"><span data-stu-id="80f07-166"><span id="Detecting_hyperthreading_and_multicore_processors"></span><span id="detecting_hyperthreading_and_multicore_processors"></span><span id="DETECTING_HYPERTHREADING_AND_MULTICORE_PROCESSORS"></span>Detecting hyperthreading and multicore processors</span></span>
</dt> <dd>

<span data-ttu-id="80f07-167">[**Win32 \_電腦系統和**](/windows/desktop/CIMWin32Prov/win32-computersystem) [**Win32 \_ 處理器**](/windows/desktop/CIMWin32Prov/win32-processor) 都有新的屬性，可讓您撰寫腳本來判斷電腦系統是否有多核心或超執行緒處理器。</span><span class="sxs-lookup"><span data-stu-id="80f07-167">[**Win32\_ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) and [**Win32\_Processor**](/windows/desktop/CIMWin32Prov/win32-processor) have new properties that enable you to write scripts to determine whether the computer system has multicore or hyperthreading processors.</span></span>

</dd> <dt>

<span data-ttu-id="80f07-168"><span id="Event_messages"></span><span id="event_messages"></span><span id="EVENT_MESSAGES"></span>事件訊息</span><span class="sxs-lookup"><span data-stu-id="80f07-168"><span id="Event_messages"></span><span id="event_messages"></span><span id="EVENT_MESSAGES"></span>Event messages</span></span>
</dt> <dd>

<span data-ttu-id="80f07-169">Windows Vista 有新的事件訊息。</span><span class="sxs-lookup"><span data-stu-id="80f07-169">Windows Vista has new event messages.</span></span> <span data-ttu-id="80f07-170">如需詳細資訊，請參閱 [WMI 事件](wmi-events.md)。</span><span class="sxs-lookup"><span data-stu-id="80f07-170">For more information, see [WMI Events](wmi-events.md).</span></span>

</dd> <dt>

<span data-ttu-id="80f07-171"><span id="Inventory_improvements"></span><span id="inventory_improvements"></span><span id="INVENTORY_IMPROVEMENTS"></span>清查改進</span><span class="sxs-lookup"><span data-stu-id="80f07-171"><span id="Inventory_improvements"></span><span id="inventory_improvements"></span><span id="INVENTORY_IMPROVEMENTS"></span>Inventory improvements</span></span>
</dt> <dd>

<span data-ttu-id="80f07-172">許多硬體類別都有變更來改善硬體清查。</span><span class="sxs-lookup"><span data-stu-id="80f07-172">Many hardware classes have had changes to improve hardware inventory.</span></span> <span data-ttu-id="80f07-173">例如，在 [**win32 \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) 和 [**win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive)中加入了序號屬性。</span><span class="sxs-lookup"><span data-stu-id="80f07-173">For example, a serial number property was added to [**Win32\_CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) and [**Win32\_DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive).</span></span>

</dd> <dt>

<span data-ttu-id="80f07-174"><span id="New_provider_hosting_models"></span><span id="new_provider_hosting_models"></span><span id="NEW_PROVIDER_HOSTING_MODELS"></span>新的提供者裝載模型</span><span class="sxs-lookup"><span data-stu-id="80f07-174"><span id="New_provider_hosting_models"></span><span id="new_provider_hosting_models"></span><span id="NEW_PROVIDER_HOSTING_MODELS"></span>New provider hosting models</span></span>
</dt> <dd>

<span data-ttu-id="80f07-175">已針對 Windows Vista 加入新的提供者裝載模型。</span><span class="sxs-lookup"><span data-stu-id="80f07-175">New provider hosting models have been added for Windows Vista.</span></span> <span data-ttu-id="80f07-176">如需詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。</span><span class="sxs-lookup"><span data-stu-id="80f07-176">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="80f07-177">相關主題</span><span class="sxs-lookup"><span data-stu-id="80f07-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80f07-178">關於 WMI</span><span class="sxs-lookup"><span data-stu-id="80f07-178">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 
