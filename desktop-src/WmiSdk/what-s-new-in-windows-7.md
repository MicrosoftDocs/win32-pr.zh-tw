---
description: Windows 7 的新功能
ms.assetid: C3FE15EF-CBF0-4A5D-ADCC-108795F8CE7A
ms.tgt_platform: multiple
title: Windows 7 的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 682e4f125fcc11a1b6679af7df78fddba5a766ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986607"
---
# <a name="whats-new-in-windows-7"></a>Windows 7 的新功能

## <a name="new-security-feature-in-windows-7"></a>Windows 7 的新安全性功能

以下列出 Windows 7 提供的新 Windows Management Instrumentation (WMI) 安全性功能。

<dl> <dt>

<span id="Controlling_provider_security"></span><span id="controlling_provider_security"></span><span id="CONTROLLING_PROVIDER_SECURITY"></span>控制提供者安全性
</dt> <dd>

為了增強 WMI 共用提供者主機進程的安全性， (wmiprvse.exe) 的變更。 這些變更引進三個新的群組原則，以及兩個 WMI 共用主機的執行模式，稱為安全且相容的模式。 如需詳細資訊，請參閱 [控制提供者安全性的](registry-keys-for-controlling-provider-security-.md)登錄機碼。

</dd> </dl>

## <a name="other-new-or-updated-features-in-windows-7"></a>Windows 7 中的其他新功能或更新功能

下列清單列出 Windows 7 提供的新 WMI 功能。

<dl> <dt>

<span id="CIM_schema_compatibility"></span><span id="cim_schema_compatibility"></span><span id="CIM_SCHEMA_COMPATIBILITY"></span>CIM 架構相容性
</dt> <dd>

從 Windows 7 開始，WMI 與通用訊息模型 (CIM) 架構版本2.17.1 相容。 如需詳細資訊，請參閱 [CIM 架構相容性](cim-schema-compatibility.md)。

</dd> <dt>

<span id="Cross-namespace_association_traversal"></span><span id="cross-namespace_association_traversal"></span><span id="CROSS-NAMESPACE_ASSOCIATION_TRAVERSAL"></span>跨命名空間關聯的遍歷
</dt> <dd>

WMI 採用標準機制來探索使用 CIM 架構的設定檔。 如需詳細資訊，請參閱 [跨命名空間關聯的遍歷](cross-namespace-association-traversal.md)。

</dd> <dt>

<span id="Association_providers"></span><span id="association_providers"></span><span id="ASSOCIATION_PROVIDERS"></span>關聯提供者
</dt> <dd>

有關撰寫和註冊關聯提供者的資訊。 關聯提供者可用來公開標準設定檔，例如電源設定檔。 如需詳細資訊，請參閱 [撰寫 Interop 的關聯提供者](writing-an-association-provider-for-interop.md)。

</dd> <dt>

<span id="Optional_feature_status"></span><span id="optional_feature_status"></span><span id="OPTIONAL_FEATURE_STATUS"></span>選用功能狀態
</dt> <dd>

WMI 已實作為 [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) 類別。 此類別會查詢並傳回存在於電腦上之選用功能的狀態。 如需使用 Windows PowerShell 的查詢範例，請參閱 [查詢選擇性功能的狀態](querying-the-status-of-optional-features.md)。

</dd> <dt>

<span id="Changing_the_default_behavior_for_the_AutoRestore_repository_feature"></span><span id="changing_the_default_behavior_for_the_autorestore_repository_feature"></span><span id="CHANGING_THE_DEFAULT_BEHAVIOR_FOR_THE_AUTORESTORE_REPOSITORY_FEATURE"></span>變更 AutoRestore 儲存機制功能的預設行為
</dt> <dd>

WMI 具有新的登錄機碼，可啟用或停用 AutoRestore 存放庫功能。 如需詳細資訊，請參閱存放 [庫設定的](registry-key-for-repository-configuration.md)登錄機碼。

</dd> <dt>

<span id="New__PowerShell_command_classes"></span><span id="new__powershell_command_classes"></span><span id="NEW__POWERSHELL_COMMAND_CLASSES"></span>新的 Windows PowerShell 命令類別
</dt> <dd>

Windows PowerShell Cmdlet 可讓使用者完成管理本機和遠端電腦所需的端對端工作。 如需詳細資訊，請參閱 [WMI PowerShell 命令類別的受控參考](managed-reference-for-wmi-powershell-command-classes.md)。

</dd> <dt>

<span id="New_mechanism_to_connect_to_remote_computers"></span><span id="new_mechanism_to_connect_to_remote_computers"></span><span id="NEW_MECHANISM_TO_CONNECT_TO_REMOTE_COMPUTERS"></span>連接至遠端電腦的新機制
</dt> <dd>

Windows PowerShell 提供簡單的機制，以連接到遠端電腦上的 WMI。 如需詳細資訊，請參閱 [使用 PowerShell 連接至遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)。

</dd> <dt>

<span id="Changes_to_the_software_licensing_classes"></span><span id="changes_to_the_software_licensing_classes"></span><span id="CHANGES_TO_THE_SOFTWARE_LICENSING_CLASSES"></span>軟體授權類別的變更
</dt> <dd>

[軟體授權類別](/previous-versions/windows/desktop/sppwmi/software-license-provider-)具有新的方法和屬性，可提供更多的軟體授權資料。 此外，也新增了 [**SoftwareLicensingTokenActivationLicense**](/previous-versions/windows/desktop/sppwmi/softwarelicensingtokenactivationlicense) 類別。

</dd> <dt>

<span id="New_power_metering_and_budgeting_classes"></span><span id="new_power_metering_and_budgeting_classes"></span><span id="NEW_POWER_METERING_AND_BUDGETING_CLASSES"></span>新的電源計量和預算類別
</dt> <dd>

[電源計量和預算類別](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-) 是用來查詢電源計量介面的主要介面 (從系統上的基礎電源計量查詢的 PMI) 資訊。

</dd> <dt>

<span id="New_power_policy_classes"></span><span id="new_power_policy_classes"></span><span id="NEW_POWER_POLICY_CLASSES"></span>新的電源原則類別
</dt> <dd>

[電源原則類別](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-) 可讓您從遠端系統管理所有的電源原則基礎結構。

</dd> <dt>

<span id="Changes_to_the_Win32_ServerFeature_class"></span><span id="changes_to_the_win32_serverfeature_class"></span><span id="CHANGES_TO_THE_WIN32_SERVERFEATURE_CLASS"></span>[**Win32 \_ ServerFeature**](win32-serverfeature.md)類別的變更
</dt> <dd>

已更新 [**Win32 \_ ServerFeature**](win32-serverfeature.md)的 **ID** 屬性。

</dd> </dl>

如需舊版作業系統新功能的詳細資訊，請參閱 [Windows Vista 的新](what-s-new-in-windows-vista.md)功能。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 WMI](about-wmi.md)
</dt> </dl>

 

 
