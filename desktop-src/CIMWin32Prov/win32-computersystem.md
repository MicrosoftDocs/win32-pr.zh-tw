---
description: 代表執行 Windows 的電腦系統。
ms.assetid: fdb9fe36-1b8a-4dfa-a1cd-55065017ba2a
ms.tgt_platform: multiple
title: Win32_ComputerSystem 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem
- Win32_ComputerSystem.SetPowerState
- Win32_ComputerSystem.AdminPasswordStatus
- Win32_ComputerSystem.AutomaticManagedPagefile
- Win32_ComputerSystem.AutomaticResetBootOption
- Win32_ComputerSystem.AutomaticResetCapability
- Win32_ComputerSystem.BootOptionOnLimit
- Win32_ComputerSystem.BootOptionOnWatchDog
- Win32_ComputerSystem.BootROMSupported
- Win32_ComputerSystem.BootupState
- Win32_ComputerSystem.BootStatus
- Win32_ComputerSystem.Caption
- Win32_ComputerSystem.ChassisBootupState
- Win32_ComputerSystem.ChassisSKUNumber
- Win32_ComputerSystem.CreationClassName
- Win32_ComputerSystem.CurrentTimeZone
- Win32_ComputerSystem.DaylightInEffect
- Win32_ComputerSystem.Description
- Win32_ComputerSystem.DNSHostName
- Win32_ComputerSystem.Domain
- Win32_ComputerSystem.DomainRole
- Win32_ComputerSystem.EnableDaylightSavingsTime
- Win32_ComputerSystem.FrontPanelResetStatus
- Win32_ComputerSystem.HypervisorPresent
- Win32_ComputerSystem.InfraredSupported
- Win32_ComputerSystem.InitialLoadInfo
- Win32_ComputerSystem.InstallDate
- Win32_ComputerSystem.KeyboardPasswordStatus
- Win32_ComputerSystem.LastLoadInfo
- Win32_ComputerSystem.Manufacturer
- Win32_ComputerSystem.Model
- Win32_ComputerSystem.Name
- Win32_ComputerSystem.NameFormat
- Win32_ComputerSystem.NetworkServerModeEnabled
- Win32_ComputerSystem.NumberOfLogicalProcessors
- Win32_ComputerSystem.NumberOfProcessors
- Win32_ComputerSystem.OEMLogoBitmap
- Win32_ComputerSystem.OEMStringArray
- Win32_ComputerSystem.PartOfDomain
- Win32_ComputerSystem.PauseAfterReset
- Win32_ComputerSystem.PCSystemType
- Win32_ComputerSystem.PCSystemTypeEx
- Win32_ComputerSystem.PowerManagementCapabilities
- Win32_ComputerSystem.PowerManagementSupported
- Win32_ComputerSystem.PowerOnPasswordStatus
- Win32_ComputerSystem.PowerState
- Win32_ComputerSystem.PowerSupplyState
- Win32_ComputerSystem.PrimaryOwnerContact
- Win32_ComputerSystem.PrimaryOwnerName
- Win32_ComputerSystem.ResetCapability
- Win32_ComputerSystem.ResetCount
- Win32_ComputerSystem.ResetLimit
- Win32_ComputerSystem.Roles
- Win32_ComputerSystem.Status
- Win32_ComputerSystem.SupportContactDescription
- Win32_ComputerSystem.SystemFamily
- Win32_ComputerSystem.SystemSKUNumber
- Win32_ComputerSystem.SystemStartupDelay
- Win32_ComputerSystem.SystemStartupOptions
- Win32_ComputerSystem.SystemStartupSetting
- Win32_ComputerSystem.SystemType
- Win32_ComputerSystem.ThermalState
- Win32_ComputerSystem.TotalPhysicalMemory
- Win32_ComputerSystem.UserName
- Win32_ComputerSystem.WakeUpType
- Win32_ComputerSystem.Workgroup
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6c6a2d965a764be8925fda55958302d815b62ad6180ce4d3abb48d399fc2e817
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119699998"
---
# <a name="win32_computersystem-class"></a>Win32 本身 \_ 類別

**\_ Win32** 系統狀態 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表執行 Windows 的電腦系統。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4B0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ComputerSystem : CIM_UnitaryComputerSystem
{
  uint16   AdminPasswordStatus;
  boolean  AutomaticManagedPagefile;
  boolean  AutomaticResetBootOption;
  boolean  AutomaticResetCapability;
  uint16   BootOptionOnLimit;
  uint16   BootOptionOnWatchDog;
  boolean  BootROMSupported;
  string   BootupState;
  uint16   BootStatus[];
  string   Caption;
  uint16   ChassisBootupState;
  string   ChassisSKUNumber;
  string   CreationClassName;
  sint16   CurrentTimeZone;
  boolean  DaylightInEffect;
  string   Description;
  string   DNSHostName;
  string   Domain;
  uint16   DomainRole;
  boolean  EnableDaylightSavingsTime;
  uint16   FrontPanelResetStatus;
  boolean  HypervisorPresent;
  boolean  InfraredSupported;
  string   InitialLoadInfo[];
  datetime InstallDate;
  uint16   KeyboardPasswordStatus;
  string   LastLoadInfo;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   NameFormat;
  boolean  NetworkServerModeEnabled;
  uint32   NumberOfLogicalProcessors;
  uint32   NumberOfProcessors;
  uint8    OEMLogoBitmap[];
  string   OEMStringArray[];
  boolean  PartOfDomain;
  sint64   PauseAfterReset;
  uint16   PCSystemType;
  uint16   PCSystemTypeEx;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PowerOnPasswordStatus;
  uint16   PowerState;
  uint16   PowerSupplyState;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  uint16   ResetCapability;
  sint16   ResetCount;
  sint16   ResetLimit;
  string   Roles[];
  string   Status;
  string   SupportContactDescription[];
  string   SystemFamily;
  string   SystemSKUNumber;
  uint16   SystemStartupDelay;
  string   SystemStartupOptions[];
  uint8    SystemStartupSetting;
  string   SystemType;
  uint16   ThermalState;
  uint64   TotalPhysicalMemory;
  string   UserName;
  uint16   WakeUpType;
  string   Workgroup;
};
```

## <a name="members"></a>成員

**Win32 執行 \_** 程式類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 無 \_** 程式類別有這些方法。



| 方法                                                                                          | 描述                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**JoinDomainOrWorkgroup**](joindomainorworkgroup-method-in-class-win32-computersystem.md)     | 將電腦系統新增至網域或工作組。<br/>                                                                                                                                                                                   |
| [**重新命名**](rename-method-in-class-win32-computersystem.md)                                   | 重新命名本機電腦。<br/>                                                                                                                                                                                                          |
| **SetPowerState**                                                                               | 未實作。 如需如何執行此方法的詳細資訊，請參閱 [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法。<br/> |
| [**UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md) | 從網域或工作組移除電腦系統。<br/>                                                                                                                                                                              |



 

### <a name="properties"></a>屬性

**Win32 無 \_** 程式類別具有這些屬性。

<dl> <dt>

**AdminPasswordStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 24 \| 硬體 Security 設定 \| AdminPasswordStatus" ) 
</dt> </dl>

系統管理員密碼狀態的系統硬體安全性設定。

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**停用** (0) 


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**已啟用** (1) 


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**未執行** (2) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (3) 


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticManagedPagefile**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) 
</dt> </dl>

若 **為 True**，系統會管理頁面檔。

</dd> <dt>

**AutomaticResetBootOption**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| AutoReboot" ) 
</dt> </dl>

若 **為 True**，則會啟用自動重設開機選項。

</dd> <dt>

**AutomaticResetCapability**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) 
</dt> </dl>

若 **為 True**，則會啟用自動重設。

</dd> <dt>

**BootOptionOnLimit**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 23 能力開機 \| \| 選項 on Limit" ) 
</dt> </dl>

開機選項限制為開啟。 識別到達 **ResetLimit** 值時的系統動作。

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**保留** (0) 


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

**作業系統** (1) 


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

**系統公用程式** (2) 


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

**請勿重新開機** (3) 


</dt> <dd></dd> </dl>

</dd> <dt>

**BootOptionOnWatchDog**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 23 \| 功能 \| 開機選項" ) 
</dt> </dl>

在監視計時器經過的時間之後，重新開機動作的類型。

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**保留** (0) 


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

**作業系統** (1) 


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

**系統公用程式** (2) 


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

**請勿重新開機** (3) 


</dt> <dd></dd> </dl>

</dd> <dt>

**BootROMSupported**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) 
</dt> </dl>

若 **為 True**，表示是否支援開機 ROM。

</dd> <dt>

**BootStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「SMBIOS \| 類型 32 \| 系統開機資訊 \| 開機狀態」 ) 
</dt> </dl>

識別開機狀態的狀態和其他資料欄位。

此值來自 SMBIOS 資訊中 **系統開機資訊** 結構的 **開機狀態** 成員。

**Windows Server 2012 R2、Windows 8.1、Windows Server 2012、Windows 8、Windows server 2008 R2、Windows 7、Windows server 2008 和 Windows Vista：** 在 Windows 10 和 Windows Server 2016 之前，不支援這個屬性。

</dd> <dt>

**BootupState**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ CLEANBOOT" ) 
</dt> </dl>

系統已啟動。 「安全開機」會略過使用者啟動檔案，也稱為安全開機。

下列清單包含必要的值：

<dl> <dd>「正常開機」</dd> <dd>「安全開機」</dd> <dd>「使用網路開機時無法安全」</dd> </dl>

<dt>

<span id="Normal_boot"></span><span id="normal_boot"></span><span id="NORMAL_BOOT"></span>

**正常開機** ( 「正常開機」 ) 


</dt> <dd></dd> <dt>

<span id="Fail-safe_boot"></span><span id="fail-safe_boot"></span><span id="FAIL-SAFE_BOOT"></span>

「**安全** 開機」 ( 「故障安全開機」 ) 


</dt> <dd></dd> <dt>

<span id="Fail-safe_with_network_boot"></span><span id="fail-safe_with_network_boot"></span><span id="FAIL-SAFE_WITH_NETWORK_BOOT"></span>

使用網路開機 ( 「使用網路開機時無法安全」的 **網路開機**) 的安全


</dt> <dd></dd> </dl>

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) 
</dt> </dl>

物件的簡短描述（單行字串）。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**ChassisBootupState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 3 \| 啟動狀態" ) 
</dt> </dl>

主機殼的開機狀態。

此值來自于 SMBIOS 資訊中 **系統主機殼或底座** 結構的 **開機狀態** 成員。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (2) 


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

**保管庫** (3) 


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**警告** (4) 


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**重大** (5) 


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

**無法復原的** (6) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ChassisSKUNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 3 \| 底座 \| SKU Number" ) 
</dt> </dl>

作為字串的底座或主機殼 SKU 編號。

此值來自于 **系統主機殼** 的 **SKU 編號** 成員或 SMBIOS 資訊中的底座結構。

**Windows Server 2012 R2、Windows 8.1、Windows Server 2012、Windows 8、Windows server 2008 R2、Windows 7、Windows server 2008 和 Windows Vista：** 在 Windows 10 和 Windows Server 2016 之前，不支援這個屬性。

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

實例之繼承鏈中的第一個具體類別的名稱。 您可以使用這個屬性搭配類別的其他屬性，來識別類別和其子類別的所有實例。

這個屬性繼承自 [**CIM \_ 系統**](cim-system.md)。

</dd> <dt>

**CurrentTimeZone**
</dt> <dd> <dl> <dt>

資料類型： **sint16**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 時間結構 \| [**時區 \_ \_ 資訊**](/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information) \| 偏差」 ) ，[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「分鐘」 ) 
</dt> </dl>

單一電腦系統從國際標準時間 (UTC) 位移的時間量。

</dd> <dt>

**DaylightInEffect**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Time 函數 \| [**GetTimeZoneInformation**](/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)" ) 
</dt> </dl>

若 **為 True**，表示日光節約模式為開啟。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) 
</dt> </dl>

物件的描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**DNSHostName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| GetComputerNameEx \| ComputerNameDnsHostname" ) 
</dt> </dl>

根據功能變數名稱伺服器 (DNS) 的本機電腦名稱稱。

</dd> <dt>

**網域**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Network Management 結構 \| [**WKSTA \_ INFO \_ 100**](/windows/desktop/api/lmwksta/ns-lmwksta-wksta_info_100) \| wki100 \_ langroup" ) 
</dt> </dl>

電腦所屬之網域的名稱。

> [!Note]  
> 如果電腦不是網域的一部分，則會傳回工作組的名稱。

 

</dd> <dt>

**DomainRole**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Directory Service (Ds) 結構 \| [**DSROLE \_ 主域 \_ \_ 資訊 \_ 基本**](/windows/desktop/api/dsrole/ns-dsrole-dsrole_primary_domain_info_basic) \| [**DSROLE \_ 電腦 \_ 角色**](/windows/desktop/api/dsrole/ne-dsrole-dsrole_machine_role) \| MachineRole" ) 
</dt> </dl>

已指派網域工作組中電腦的角色。 網域工作組是相同網路上的電腦集合。 例如， **DomainRole** 屬性可能會顯示電腦是成員工作站。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

<dt>

<span id="Standalone_Workstation"></span><span id="standalone_workstation"></span><span id="STANDALONE_WORKSTATION"></span>

**獨立工作站** (0) 


</dt> <dd></dd> <dt>

<span id="Member_Workstation"></span><span id="member_workstation"></span><span id="MEMBER_WORKSTATION"></span>

**成員工作站** (1) 


</dt> <dd></dd> <dt>

<span id="Standalone_Server"></span><span id="standalone_server"></span><span id="STANDALONE_SERVER"></span>

**獨立伺服器** (2) 


</dt> <dd></dd> <dt>

<span id="Member_Server"></span><span id="member_server"></span><span id="MEMBER_SERVER"></span>

**成員伺服器** (3) 


</dt> <dd></dd> <dt>

<span id="Backup_Domain_Controller"></span><span id="backup_domain_controller"></span><span id="BACKUP_DOMAIN_CONTROLLER"></span>

**備份網域控制站** (4) 


</dt> <dd></dd> <dt>

<span id="Primary_Domain_Controller"></span><span id="primary_domain_controller"></span><span id="PRIMARY_DOMAIN_CONTROLLER"></span>

**網域主控站** (5) 


</dt> <dd></dd> </dl>

</dd> <dt>

**EnableDaylightSavingsTime**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

啟用電腦上 (DST) 的日光節約時間。 值為 **True** 表示系統時間在 DST 開始或結束時，會變更為一小時前或之後。 值為 **False** 表示系統時間在 DST 開始或結束時，不會在一小時前或之後變更為一小時。 **Null** 值表示系統上的 DST 狀態是未知的。

</dd> <dt>

**FrontPanelResetStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 24 \| 硬體 Security 設定 \| FrontPanelResetStatus" ) 
</dt> </dl>

下表列出電腦上 [重設] 按鈕的硬體安全性設定。

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**停用** (0) 


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**已啟用** (1) 


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**未執行** (2) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (3) 


</dt> <dd></dd> </dl>

</dd> <dt>

**HypervisorPresent**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) 
</dt> </dl>

若 **為 True**，則表示有虛擬程式。

**Windows server 2008 R2、Windows 7、Windows Server 2008 和 Windows Vista：** 在 Windows 8 和 Windows Server 2012 之前，不支援這個屬性。

</dd> <dt>

**InfraredSupported**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) 
</dt> </dl>

若 **為 True**，則表示電腦系統上有紅外線 (IR) 埠。

</dd> <dt>

**InitialLoadInfo**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

尋找初始載入裝置或啟動服務以要求作業系統啟動所需的資料。

這個屬性繼承自 [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md)。

**Windows Server 2008 R2：** 這個屬性是可用的，但卻是空的。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") 
</dt> </dl>

已安裝物件。 物件不需要值來表示已安裝。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**KeyboardPasswordStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 24 \| 硬體 Security 設定 \| KeyboardPasswordStatus" ) 
</dt> </dl>

鍵盤密碼狀態的系統硬體安全性設定。

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**停用** (0) 


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**已啟用** (1) 


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**未執行** (2) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (3) 


</dt> <dd></dd> </dl>

</dd> <dt>

**LastLoadInfo**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

**InitialLoadInfo** 屬性的陣列專案，其中包含用來啟動載入之作業系統的資料。

這個屬性繼承自 [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md)。

</dd> <dt>

**製造商**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 1 \| 系統資訊 \| 製造商" ) 
</dt> </dl>

電腦製造商的名稱。

範例：艾德作品

</dd> <dt>

**型號**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 1 \| 系統資訊 \| Product Name" ) 
</dt> </dl>

製造商為電腦提供的產品名稱。 這個屬性必須有值。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

企業環境中 [**CIM \_ 系統**](cim-system.md) 實例的索引鍵。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

自動產生的電腦系統 **名稱** 值。 Cim 系統元件和其衍生物件是通用訊息模型 (CIM) 的最上層物件。 [**\_**](cim-computersystem.md) 它們提供數個元件的範圍。 唯一的 [**CIM \_ 系統**](cim-system.md)金鑰是必要的，但您可以定義啟發式來建立可產生相同名稱的 CIM 系統名稱，且與探索通訊協定無關。 **\_** 當相同的資產或實體發現多次，但無法解析成一個物件時，這可避免清查和管理問題。 建議使用啟發學習法，但非必要。

啟發學習法會在 CIM V2 一般模型規格中概述，並假設已記載的規則會用來決定和指派名稱。 **NameFormat** 值清單會定義指派電腦系統名稱的順序。 有數個規則對應到相同的值。

使用啟發學習法計算的 [**CIM 系統 \_ 名稱**](cim-computersystem.md) 值是系統的索引鍵值。 不過，您可以使用別名來指派不同的 **CIM \_** 系統名稱，對您的公司來說可能更是唯一的名稱。

這個屬性繼承自 [**CIM \_ 系統**](cim-system.md)。

包括下列值：

<dt>

<span id="IP"></span><span id="ip"></span>

**Ip** ( 「ip」 ) 


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

**撥號** ( 「撥號」 ) 


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

**Hid** ( "hid" ) 


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

**NWA** ( "NWA" ) 


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

**HWA** ( "HWA" ) 


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

**X25** ( "x25" ) 


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

**Isdn** ( "isdn" ) 


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

**Ipx** ( 「ipx」 ) 


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

**DCC** ( "DCC" ) 


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

**Icd** ( 「icd」 ) 


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

**E.** ( "e. 164" ) 


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

**Sna** ( 「sna」 ) 


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

**Oid/osi** ( "OID/osi" ) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** ( "其他" ) 


</dt> <dd></dd> </dl>

</dd> <dt>

**NetworkServerModeEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Network Management 結構 \| [**伺服器 \_ 資訊 \_ 101**](/windows/desktop/api/lmserver/ns-lmserver-server_info_101) \| sv101 \_ type \| SV \_ type \_ SERVER" ) 
</dt> </dl>

若 **為 True**，則會啟用網路伺服器模式。

</dd> <dt>

**NumberOfLogicalProcessors**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) 
</dt> </dl>

電腦上可用的邏輯處理器數目。

您可以使用 **NumberOfLogicalProcessors** 和 **NumberOfProcessors** 來判斷電腦是否為超執行緒。 如需詳細資訊，請參閱＜備註＞。

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| 系統資訊結構 \| [**系統 \_ 資訊**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| dwNumberOfProcessors" ) 
</dt> </dl>

系統目前可用的實體處理器數目。 這是系統已啟用的處理器數目，不包括已停用的處理器。 如果電腦系統有兩個實體處理器，每個都包含兩個邏輯處理器，則 **NumberOfProcessors** 的值為2，而 **NumberOfLogicalProcessors** 為4。 這些處理器可能是多核心的，也可能是超執行緒處理器。 如需詳細資訊，請參閱＜備註＞。

</dd> <dt>

**OEMLogoBitmap**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) 
</dt> </dl>

原始設備製造商 (OEM) 所建立的點陣圖資料清單。

</dd> <dt>

**OEMStringArray**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 11 \| OEM Strings" ) 
</dt> </dl>

OEM 定義的自由格式字串清單。 例如，OEM 會定義系統參考檔的元件編號、製造商連絡人資訊等等。

</dd> <dt>

**PartOfDomain**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "" ) 
</dt> </dl>

若 **為 True**，則表示電腦是網域的一部分。 如果值為 **Null**，則電腦不在網域中，或狀態不明。 如果您將電腦從網域中移除，此值就會變成 **false**。

</dd> <dt>

**PauseAfterReset**
</dt> <dd> <dl> <dt>

資料類型： **sint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 23 \| Timeout" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫秒" ) 
</dt> </dl>

啟動重新開機之前的時間延遲（以毫秒為單位）。 它會在系統電源週期、本機或遠端系統重設，以及自動重設系統之後使用。 1)  (值為1，表示暫停值不明。

**Windows Vista：** 這個屬性可能會傳回未知的數位。

</dd> <dt>

**PCSystemType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "" ) 
</dt> </dl>

使用中的電腦類型，例如膝上型電腦、桌上型電腦或平板電腦。

<dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>**未指定** (0) 


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (1) 


</dt> <dd></dd> <dt>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>**Mobile** (2) 


</dt> <dd></dd> <dt>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>**工作站** (3) 


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>**Enterprise Server** (4) 


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>**SOHO 伺服器** (5) 


</dt> <dd>

小型 Office 和家用 Office (SOHO) 伺服器

</dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>**設備電腦** (6) 


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>**效能伺服器** (7) 


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**最大** (8) 


</dt> <dd></dd> </dl>

</dd> <dt>

**PCSystemTypeEx**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "" ) 
</dt> </dl>

使用中的電腦類型，例如膝上型電腦、桌上型電腦或平板電腦。

**Windows Server 2012、Windows 8、Windows server 2008 R2、Windows 7、Windows Server 2008 和 Windows Vista：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個屬性。

<dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

**未指定** (0) 


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

**Desktop** (1) 


</dt> <dd></dd> <dt>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>

**Mobile** (2) 


</dt> <dd></dd> <dt>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>

**工作站** (3) 


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

**Enterprise Server** (4) 


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

**SOHO 伺服器** (5) 


</dt> <dd></dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

**設備電腦** (6) 


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

**效能伺服器** (7) 


</dt> <dd></dd> <dt>

<span id="Slate"></span><span id="slate"></span><span id="SLATE"></span>

 (8) 的 **平板**


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

**最大** (9) 


</dt> <dd></dd> </dl>

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統電源控制項 \| 001.2 ") 
</dt> </dl>

邏輯裝置的特定電源相關功能陣列。

這個屬性繼承自 **CIM \_ LogicalDevice**。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) 


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) 


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) 


</dt> <dd>

電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) 


</dt> <dd>

裝置可以根據使用方式或其他準則來變更其電源狀態。

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) 


</dt> <dd>

支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。 這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。 如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**


</dt> <dd>

您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**


</dt> <dd>

支援計時 Power-On

您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。

</dd> </dl>

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 True**，則裝置可以電源管理，例如，裝置可進入暫停模式，依此類推。 這個屬性不會指出電源管理功能目前已啟用，但它會指出邏輯裝置能夠進行電源管理。

這個屬性繼承自 [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md)。

</dd> <dt>

**PowerOnPasswordStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 24 \| 硬體 Security 設定 \| PowerOnPasswordStatus" ) 
</dt> </dl>

Power-On 密碼狀態的系統硬體安全性設定。

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**停用** (0) 


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**已啟用** (1) 


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**未執行** (2) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (3) 


</dt> <dd></dd> </dl>

</dd> <dt>

**>powerstate**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

電腦的目前電源狀態及其相關聯的作業系統。 省電狀態具有下列值： [值 4] ([未知]) 表示系統已知處於省電模式，但在此模式中的確切狀態為未知;2 (低電源模式) 指出系統處於省電狀態，但仍在運作中，而且效能可能會降低。3 (待命) 指出系統無法正常運作，但可快速進入完整電源;和 7 (警告) 指出電腦系統處於警告狀態和省電模式。

這個屬性繼承自 [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md)。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1) 


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (2) 


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (3) 


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (4) 


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**電源週期** (5) 


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (6) 的電源


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (7) 


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>省 **電-休眠** (8) 


</dt> <dd>

省電休眠。

</dd> <dt>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>省 **電-軟關閉** (9) 


</dt> <dd>

省電。

</dd> </dl>

</dd> <dt>

**PowerSupplyState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「SMBIOS \| Type 3 \| 系統主機殼或底座 \| 電源供應器狀態」 ) 
</dt> </dl>

電源供應器的狀態，或在上一次開機時提供的電源。

此值來自于 SMBIOS 資訊中 **系統主機殼或底座** 結構的 **電源供應器狀態** 成員。

下列清單會識別此屬性的值。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) 


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>**保管庫** (3) 


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) 


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**重大** (5) 


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>**無法復原的** (6) 


</dt> <dd>

恢復

</dd> </dl>

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

主要系統擁有者的連絡人資訊，例如電話號碼、電子郵件地址等等。

這個屬性繼承自 [**CIM \_ 系統**](cim-system.md)。

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

主要系統擁有者的名稱。

這個屬性繼承自 [**CIM \_ 系統**](cim-system.md)。

</dd> <dt>

**ResetCapability**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統硬體安全性 \| 001.4」 ) 
</dt> </dl>

如果啟用，則值為4，而單一電腦系統可以使用 [電源] 和 [重設] 按鈕來重設。 如果停用，則值為3，不允許重設。

這個屬性繼承自 [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md)。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) 


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) 


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (4) 


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>**未執行** (5) 


</dt> <dd>

恢復

</dd> </dl>

</dd> <dt>

**ResetCount**
</dt> <dd> <dl> <dt>

資料類型： **sint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「SMBIOS \| 類型 23 \| 系統重設 \| 計數」 ) 
</dt> </dl>

自上次重設之後自動重設的次數。 1 (的值減去一個) 表示計數未知。

</dd> <dt>

**ResetLimit**
</dt> <dd> <dl> <dt>

資料類型： **sint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「SMBIOS \| 類型 23 \| 系統重設 \| 重設限制」 ) 
</dt> </dl>

嘗試重設系統的連續次數。 1 (的值減去一個) 表示限制未知。

</dd> <dt>

**角色**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

此清單會指定資訊技術環境中系統的角色。

這個屬性繼承自 [**CIM \_ 系統**](cim-system.md)。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) 
</dt> </dl>

物件的目前狀態。

針對 Win32_ComputerSystem，狀態一律為「確定」。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dl>

</dd> <dt>

**SupportContactDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| [**GetPrivateProfileString**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilestring) \| Support Information" ) 
</dt> </dl>

Windows 作業系統的支援連絡人資訊清單。

</dd> <dt>

**SystemFamily**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「SMBIOS \| 類型 1 \| 系統資訊 \| 系列」 ) 
</dt> </dl>

特定電腦所屬的系列。 系列是指一組類似于硬體或軟體觀點的電腦，但不完全相同。

此值來自 SMBIOS 資訊中 **系統資訊** 結構的 **家庭** 成員。

**Windows Server 2012 R2、Windows 8.1、Windows Server 2012、Windows 8、Windows server 2008 R2、Windows 7、Windows server 2008 和 Windows Vista：** 在 Windows 10 和 Windows Server 2016 之前，不支援這個屬性。

</dd> <dt>

**SystemSKUNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 1 \| 系統資訊 \| SKU Number" ) 
</dt> </dl>

識別要銷售的特定電腦設定。 有時也稱為產品識別碼或採購單號碼。

此值來自 SMBIOS 資訊中 **系統資訊** 結構的 **SKU 編號** 成員。

**Windows Server 2012 R2、Windows 8.1、Windows Server 2012、Windows 8、Windows server 2008 R2、Windows 7、Windows server 2008 和 Windows Vista：** 在 Windows 10 和 Windows Server 2016 之前，不支援這個屬性。

</dd> <dt>

**SystemStartupDelay**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、[**許可權**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "SeSystemEnvironmentPrivilege" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| [**GetPrivateProfileInt**](/windows/desktop/api/winbase/nf-winbase-getprivateprofileint) \| Boot 載入器 \| timeout" ) 、[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "seconds" ) 
</dt> </dl>

**SystemStartupDelay** 不再可供使用，因為 Boot.ini 不會用來設定系統啟動。 相反地，請使用開機設定資料 (BCD) WMI 提供者或 **Bcdedit** 命令所提供的 [bcd 類別](/previous-versions/windows/desktop/bcd/bcd-classes)。

</dd> <dt>

**SystemStartupOptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)，[**許可權**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "SeSystemEnvironmentPrivilege" ) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| [**GetPrivateProfileSection**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilesection) \| 作業系統" ) 
</dt> </dl>

**SystemStartupOptions** 不再可供使用，因為 Boot.ini 不會用來設定系統啟動。 相反地，請使用開機設定資料 (BCD) WMI 提供者或 **Bcdedit** 命令所提供的 [bcd 類別](/previous-versions/windows/desktop/bcd/bcd-classes)。

</dd> <dt>

**SystemStartupSetting**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**許可權**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "SeSystemEnvironmentPrivilege" ) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) 
</dt> </dl>

**SystemStartupSetting** 不再可供使用，因為 Boot.ini 不會用來設定系統啟動。 相反地，請使用開機設定資料 (BCD) WMI 提供者或 **Bcdedit** 命令所提供的 [bcd 類別](/previous-versions/windows/desktop/bcd/bcd-classes)。

</dd> <dt>

**SystemType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| 系統資訊結構 \| [**系統 \_ 資訊**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| wProcessorArchitecture" ) 
</dt> </dl>

在 Windows 電腦上執行的系統。 這個屬性必須有值。

下列清單會識別此屬性的一些可能值。

<dl> <dd>「x64 型電腦」</dd> <dd>「X86 型電腦」</dd> <dd>「MIPS 型電腦」</dd> <dd>「以 Alpha 為基礎的電腦」</dd> <dd>「Power PC」</dd> <dd>"SH-x PC"</dd> <dd>「StrongARM PC」</dd> <dd>「64位 Intel 電腦」</dd> <dd>「64位 Alpha 電腦」</dd> <dd>不明</dd> <dd>「X86-Nec98 PC」</dd> </dl>

<dt>

<span id="X86-based_PC"></span><span id="x86-based_pc"></span><span id="X86-BASED_PC"></span>

**X86 電腦** ( 「X86 型電腦」 ) 


</dt> <dd></dd> <dt>

<span id="MIPS-based_PC"></span><span id="mips-based_pc"></span><span id="MIPS-BASED_PC"></span>

以 **mips 為基礎的電腦** ( 「MIPS 型電腦」 ) 


</dt> <dd></dd> <dt>

<span id="Alpha-based_PC"></span><span id="alpha-based_pc"></span><span id="ALPHA-BASED_PC"></span>

以 **Alpha 為基礎的電腦** ( 「ALPHA 型電腦」 ) 


</dt> <dd></dd> <dt>

<span id="Power_PC"></span><span id="power_pc"></span><span id="POWER_PC"></span>

**POWER pc** ( 「power pc」 ) 


</dt> <dd></dd> <dt>

<span id="SH-x_PC"></span><span id="sh-x_pc"></span><span id="SH-X_PC"></span>

**Sh-x pc** ( "SH-x pc" ) 


</dt> <dd></dd> <dt>

<span id="StrongARM_PC"></span><span id="strongarm_pc"></span><span id="STRONGARM_PC"></span>

**STRONGARM pc** ( "StrongARM pc" ) 


</dt> <dd></dd> <dt>

<span id="64-bit_Intel_PC"></span><span id="64-bit_intel_pc"></span><span id="64-BIT_INTEL_PC"></span>

**64 位 INTEL pc** ( 「64位 intel pc」 ) 


</dt> <dd></dd> <dt>

<span id="x64-based_PC"></span><span id="x64-based_pc"></span><span id="X64-BASED_PC"></span>

以 **x64 為基礎的電腦** ( 「X64 型電腦」 ) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 ( 「未知」 ) 


</dt> <dd></dd> <dt>

<span id="X86-Nec98_PC"></span><span id="x86-nec98_pc"></span><span id="X86-NEC98_PC"></span>

**X86 NEC98 pc** ( 「X86-Nec98 pc」 ) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ThermalState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「SMBIOS \| Type 3 \| 系統主機殼或底座 \| 熱狀態」 ) 
</dt> </dl>

最後一次開機時系統的熱狀態。

此值來自于 SMBIOS 資訊中 **系統主機殼或底座** 結構的 **溫度狀態** 成員。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (2) 


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

**保管庫** (3) 


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**警告** (4) 


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**重大** (5) 


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

**無法復原的** (6) 


</dt> <dd></dd> </dl>

</dd> <dt>

**TotalPhysicalMemory**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Memory Management 結構 \| [**MEMORYSTATUS**](/windows/desktop/api/winbase/ns-winbase-memorystatus) \| dwTotalPhys" ) ，[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) 
</dt> </dl>

實體記憶體的總大小。 請注意，在某些情況下，此屬性可能不會傳回實際記憶體的精確值。 例如，如果 BIOS 使用部分實體記憶體，則不正確。 若要取得精確的值，請改用 [**Win32 \_ PhysicalMemory**](win32-physicalmemory.md)中的 **容量** 屬性。

範例：67108864

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。

</dd> <dt>

**使用者名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| 系統資訊函數 \| [**GetUserName**](/windows/desktop/api/winbase/nf-winbase-getusernamea)" ) 
</dt> </dl>

目前登入的使用者名稱。 這個屬性必須有值。 在終端機服務會話中 **，使用者** 名稱會傳回登入主控台的使用者名稱，而不是使用者在終端機服務會話期間登入的使用者名稱。

範例： jeffsmith

</dd> <dt>

**WakeUpType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| type 1 \| 系統資訊 \| 喚醒類型" ) 
</dt> </dl>

導致系統開機的事件。

此值來自 SMBIOS 資訊中 **系統資訊** 結構的 **喚醒類型** 成員。

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**保留** (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (2) 


</dt> <dd></dd> <dt>

<span id="APM_Timer"></span><span id="apm_timer"></span><span id="APM_TIMER"></span>

**APM 計時器** (3) 


</dt> <dd></dd> <dt>

<span id="Modem_Ring"></span><span id="modem_ring"></span><span id="MODEM_RING"></span>

**數據機響鈴** (4) 


</dt> <dd></dd> <dt>

<span id="LAN_Remote"></span><span id="lan_remote"></span><span id="LAN_REMOTE"></span>

**區域網路遠端** (5) 


</dt> <dd></dd> <dt>

<span id="Power_Switch"></span><span id="power_switch"></span><span id="POWER_SWITCH"></span>

**電源開關** (6) 


</dt> <dd></dd> <dt>

<span id="PCI_PME_"></span><span id="pci_pme_"></span>

**PCI PME \#** (7) 


</dt> <dd></dd> <dt>

<span id="AC_Power_Restored"></span><span id="ac_power_restored"></span><span id="AC_POWER_RESTORED"></span>

**AC 電源已還原** (8) 


</dt> <dd></dd> </dl>

</dd> <dt>

**工作群組**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "" ) 
</dt> </dl>

此電腦的工作組名稱。 如果 **PartOfDomain** 屬性的值為 **False**，則會傳回工作組的名稱。

</dd> </dl>

## <a name="remarks"></a>備註

若要判斷與電腦系統物件相關聯的處理器實例總數，請使用 [**Win32 \_ ComputerSystemProcessor**](win32-computersystemprocessor.md) association 類別。

具有多個實體處理器的 Win32 實例實例具有多個與它相關聯的 [**win32 \_ 處理器**](win32-processor.md)實例。 **\_** 如果 **NumberOfLogicalProcessors** 的值大於 **NumberOfProcessors** 的值，則電腦系統可能是多核心系統，或有一或多個處理器已啟用超執行緒。 如需詳細資訊，請參閱 **Win32 \_ 處理器** 中的 **NumberOfLogicalProcessors** 和 **NumberOfCores** 屬性和備註一節。

Win32 [**\_ UnitaryComputerSystem**](cim-unitarycomputersystem.md)類別衍生自 CIM。 **\_**

## <a name="examples"></a>範例

下列的腳本中心程式 [代碼範例](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Display-computers-status-c8ff289d)會使用 Win32 程式碼，從許多電腦系統中取出資訊，並將它們顯示在 GUI 中。 **\_**

您可以在 [**win32 \_ 處理器**](win32-processor.md)主題範例中，找到從 **win32 \_** 程式碼、 [**win32 \_ 處理器**](win32-processor.md)和 win32 作業系統取得 [**作業系統 \_**](win32-operatingsystem.md)和處理器資料的範例腳本。

下列 VBScript 範例說明如何從 **Win32 \_** 執行程式實例中取出本機電腦的功能變數名稱。


```VB
Set SystemSet = GetObject("winmgmts:").InstancesOf ("Win32_ComputerSystem")

for each System in SystemSet
 WScript.Echo System.Domain
next
```



下列 Perl 範例說明如何從 **Win32 \_** 執行程式實例中取出本機電腦名稱稱。


```
use strict;
use Win32::OLE;

my ($SystemSet, $System);  
eval {$SystemSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
  InstancesOf ("Win32_ComputerSystem") };
  
unless($@)
{
 foreach $System (in $SystemSet)
 {
  print "\n", $System->{Domain}, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



下列 Perl 範例說明如何從 **Win32 \_** 執行程式實例中取出本機電腦的 DNS 功能變數名稱。


```
use strict;
use Win32::OLE;

close (STDERR);

my ($NICSet, $NIC);  
eval {$NICSet = Win32::OLE->GetObject("winmgmts:!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled=true"); };
if (!$@ && defined $NICSet)
{
 foreach $NIC (in $NICSet)
 {
  if(defined $NIC->{DNSDomain})
  {
   print "\n", $NIC->{DNSDomain}, "\n";
  }
 }
}
else
{
 print Win32::OLE->LastError, "\n";
}
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

[**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md)
</dt> <dt>

[作業系統類別](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[WMI 工作：帳戶和網域](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[WMI 工作：電腦硬體](/windows/desktop/WmiSdk/wmi-tasks--computer-hardware)
</dt> <dt>

[WMI 工作：桌面管理](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

