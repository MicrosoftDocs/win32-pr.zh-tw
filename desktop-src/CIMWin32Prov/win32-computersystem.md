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
ms.openlocfilehash: 5e5282c854bfdb1ce4b80f61a202ebecac990576
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110349"
---
# <a name="win32_computersystem-class"></a><span data-ttu-id="8f17f-103">Win32 本身 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="8f17f-103">Win32\_ComputerSystem class</span></span>

<span data-ttu-id="8f17f-104">**\_ Win32** 系統系統的 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表執行 Windows 的電腦系統。</span><span class="sxs-lookup"><span data-stu-id="8f17f-104">The **Win32\_ComputerSystem** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a computer system running Windows.</span></span>

<span data-ttu-id="8f17f-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8f17f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f17f-106">語法</span><span class="sxs-lookup"><span data-stu-id="8f17f-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="8f17f-107">成員</span><span class="sxs-lookup"><span data-stu-id="8f17f-107">Members</span></span>

<span data-ttu-id="8f17f-108">**Win32 執行 \_** 程式類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8f17f-108">The **Win32\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="8f17f-109">方法</span><span class="sxs-lookup"><span data-stu-id="8f17f-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="8f17f-110">屬性</span><span class="sxs-lookup"><span data-stu-id="8f17f-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8f17f-111">方法</span><span class="sxs-lookup"><span data-stu-id="8f17f-111">Methods</span></span>

<span data-ttu-id="8f17f-112">**Win32 無 \_** 程式類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8f17f-112">The **Win32\_ComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="8f17f-113">方法</span><span class="sxs-lookup"><span data-stu-id="8f17f-113">Method</span></span>                                                                                          | <span data-ttu-id="8f17f-114">描述</span><span class="sxs-lookup"><span data-stu-id="8f17f-114">Description</span></span>                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f17f-115">**JoinDomainOrWorkgroup**</span><span class="sxs-lookup"><span data-stu-id="8f17f-115">**JoinDomainOrWorkgroup**</span></span>](joindomainorworkgroup-method-in-class-win32-computersystem.md)     | <span data-ttu-id="8f17f-116">將電腦系統新增至網域或工作組。</span><span class="sxs-lookup"><span data-stu-id="8f17f-116">Adds a computer system to a domain or workgroup.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="8f17f-117">**重新命名**</span><span class="sxs-lookup"><span data-stu-id="8f17f-117">**Rename**</span></span>](rename-method-in-class-win32-computersystem.md)                                   | <span data-ttu-id="8f17f-118">重新命名本機電腦。</span><span class="sxs-lookup"><span data-stu-id="8f17f-118">Renames a local computer.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="8f17f-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="8f17f-119">**SetPowerState**</span></span>                                                                               | <span data-ttu-id="8f17f-120">未實作。</span><span class="sxs-lookup"><span data-stu-id="8f17f-120">Not implemented.</span></span> <span data-ttu-id="8f17f-121">如需如何執行此方法的詳細資訊，請參閱 [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="8f17f-121">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span><br/> |
| [<span data-ttu-id="8f17f-122">**UnjoinDomainOrWorkgroup**</span><span class="sxs-lookup"><span data-stu-id="8f17f-122">**UnjoinDomainOrWorkgroup**</span></span>](unjoindomainorworkgroup-method-in-class-win32-computersystem.md) | <span data-ttu-id="8f17f-123">從網域或工作組移除電腦系統。</span><span class="sxs-lookup"><span data-stu-id="8f17f-123">Removes a computer system from a domain or workgroup.</span></span><br/>                                                                                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="8f17f-124">屬性</span><span class="sxs-lookup"><span data-stu-id="8f17f-124">Properties</span></span>

<span data-ttu-id="8f17f-125">**Win32 無 \_** 程式類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8f17f-125">The **Win32\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8f17f-126">**AdminPasswordStatus**</span><span class="sxs-lookup"><span data-stu-id="8f17f-126">**AdminPasswordStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-127">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8f17f-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-129">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 24 \| 硬體 Security Settings \| AdminPasswordStatus" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|AdminPasswordStatus")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-130">系統管理員密碼狀態的系統硬體安全性設定。</span><span class="sxs-lookup"><span data-stu-id="8f17f-130">System hardware security settings for administrator password status.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8f17f-131">**停用** (0) </span><span class="sxs-lookup"><span data-stu-id="8f17f-131">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8f17f-132">**已啟用** (1) </span><span class="sxs-lookup"><span data-stu-id="8f17f-132">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="8f17f-133">**未執行** (2) </span><span class="sxs-lookup"><span data-stu-id="8f17f-133">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f17f-134">**未知** 的 (3) </span><span class="sxs-lookup"><span data-stu-id="8f17f-134">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f17f-135">**AutomaticManagedPagefile**</span><span class="sxs-lookup"><span data-stu-id="8f17f-135">**AutomaticManagedPagefile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-136">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8f17f-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-137">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8f17f-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-138">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-139">若 **為 True**，系統會管理頁面檔。</span><span class="sxs-lookup"><span data-stu-id="8f17f-139">If **True**, the system manages the page file.</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-140">**AutomaticResetBootOption**</span><span class="sxs-lookup"><span data-stu-id="8f17f-140">**AutomaticResetBootOption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-141">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8f17f-141">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8f17f-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-143">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| AutoReboot" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|AutoReboot")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-144">若 **為 True**，則會啟用自動重設開機選項。</span><span class="sxs-lookup"><span data-stu-id="8f17f-144">If **True**, the automatic reset boot option is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-145">**AutomaticResetCapability**</span><span class="sxs-lookup"><span data-stu-id="8f17f-145">**AutomaticResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-146">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8f17f-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-148">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-149">若 **為 True**，則會啟用自動重設。</span><span class="sxs-lookup"><span data-stu-id="8f17f-149">If **True**, the automatic reset is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-150">**BootOptionOnLimit**</span><span class="sxs-lookup"><span data-stu-id="8f17f-150">**BootOptionOnLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-151">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8f17f-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-153">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 23 能力開機 \| \| 選項 on Limit" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-153">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|Capabilites\|Boot Option on Limit")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-154">開機選項限制為開啟。</span><span class="sxs-lookup"><span data-stu-id="8f17f-154">Boot option limit is ON.</span></span> <span data-ttu-id="8f17f-155">識別到達 **ResetLimit** 值時的系統動作。</span><span class="sxs-lookup"><span data-stu-id="8f17f-155">Identifies the system action when the **ResetLimit** value is reached.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="8f17f-156">**保留** (0) </span><span class="sxs-lookup"><span data-stu-id="8f17f-156">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

<span data-ttu-id="8f17f-157">**作業系統** (1) </span><span class="sxs-lookup"><span data-stu-id="8f17f-157">**Operating system** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

<span data-ttu-id="8f17f-158">**系統公用程式** (2) </span><span class="sxs-lookup"><span data-stu-id="8f17f-158">**System utilities** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

<span data-ttu-id="8f17f-159">**請勿重新開機** (3) </span><span class="sxs-lookup"><span data-stu-id="8f17f-159">**Do not reboot** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f17f-160">**BootOptionOnWatchDog**</span><span class="sxs-lookup"><span data-stu-id="8f17f-160">**BootOptionOnWatchDog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-161">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8f17f-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-163">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 23 \| 功能 \| 開機選項" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|Capabilities\|Boot Option")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-164">在監視計時器經過的時間之後，重新開機動作的類型。</span><span class="sxs-lookup"><span data-stu-id="8f17f-164">Type of reboot action after the time on the watchdog timer is elapsed.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="8f17f-165">**保留** (0) </span><span class="sxs-lookup"><span data-stu-id="8f17f-165">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

<span data-ttu-id="8f17f-166">**作業系統** (1) </span><span class="sxs-lookup"><span data-stu-id="8f17f-166">**Operating system** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

<span data-ttu-id="8f17f-167">**系統公用程式** (2) </span><span class="sxs-lookup"><span data-stu-id="8f17f-167">**System utilities** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

<span data-ttu-id="8f17f-168">**請勿重新開機** (3) </span><span class="sxs-lookup"><span data-stu-id="8f17f-168">**Do not reboot** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f17f-169">**BootROMSupported**</span><span class="sxs-lookup"><span data-stu-id="8f17f-169">**BootROMSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-170">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8f17f-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-172">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-172">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-173">若 **為 True**，表示是否支援開機 ROM。</span><span class="sxs-lookup"><span data-stu-id="8f17f-173">If **True**, indicates whether a boot ROM is supported.</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-174">**BootStatus**</span><span class="sxs-lookup"><span data-stu-id="8f17f-174">**BootStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-175">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="8f17f-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-177">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「SMBIOS \| 類型 32 \| 系統開機資訊 \| 開機狀態」 ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-177">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 32\|System Boot Information\|Boot Status")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-178">識別開機狀態的狀態和其他資料欄位。</span><span class="sxs-lookup"><span data-stu-id="8f17f-178">Status and Additional Data fields that identify the boot status.</span></span>

<span data-ttu-id="8f17f-179">此值來自 SMBIOS 資訊中 **系統開機資訊** 結構的 **開機狀態** 成員。</span><span class="sxs-lookup"><span data-stu-id="8f17f-179">This value comes from the **Boot Status** member of the **System Boot Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="8f17f-180">**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows 10 和 Windows Server 2016 之前，不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="8f17f-180">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-181">**BootupState**</span><span class="sxs-lookup"><span data-stu-id="8f17f-181">**BootupState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-182">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f17f-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-184">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ CLEANBOOT" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-184">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)\|SM\_CLEANBOOT")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-185">系統已啟動。</span><span class="sxs-lookup"><span data-stu-id="8f17f-185">System is started.</span></span> <span data-ttu-id="8f17f-186">「安全開機」會略過使用者啟動檔案，也稱為安全開機。</span><span class="sxs-lookup"><span data-stu-id="8f17f-186">Fail-safe boot bypasses the user startup files also called SafeBoot.</span></span>

<span data-ttu-id="8f17f-187">下列清單包含必要的值：</span><span class="sxs-lookup"><span data-stu-id="8f17f-187">The following list contains the required values:</span></span>

<dl> <dd><span data-ttu-id="8f17f-188">「正常開機」</span><span class="sxs-lookup"><span data-stu-id="8f17f-188">"Normal boot"</span></span></dd> <dd><span data-ttu-id="8f17f-189">「安全開機」</span><span class="sxs-lookup"><span data-stu-id="8f17f-189">"Fail-safe boot"</span></span></dd> <dd><span data-ttu-id="8f17f-190">「使用網路開機時無法安全」</span><span class="sxs-lookup"><span data-stu-id="8f17f-190">"Fail-safe with network boot"</span></span></dd> </dl>

<dt>

<span id="Normal_boot"></span><span id="normal_boot"></span><span id="NORMAL_BOOT"></span>

<span data-ttu-id="8f17f-191">**正常開機** ( 「正常開機」 ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-191">**Normal boot** ("Normal boot")</span></span>


</dt> <dd></dd> <dt>

<span id="Fail-safe_boot"></span><span id="fail-safe_boot"></span><span id="FAIL-SAFE_BOOT"></span>

<span data-ttu-id="8f17f-192">「**安全** 開機」 ( 「故障安全開機」 ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-192">**Fail-safe boot** ("Fail-safe boot")</span></span>


</dt> <dd></dd> <dt>

<span id="Fail-safe_with_network_boot"></span><span id="fail-safe_with_network_boot"></span><span id="FAIL-SAFE_WITH_NETWORK_BOOT"></span>

<span data-ttu-id="8f17f-193">使用網路開機 ( 「使用網路開機時無法安全」的 **網路開機**) 的安全</span><span class="sxs-lookup"><span data-stu-id="8f17f-193">**Fail-safe with network boot** ("Fail-safe with network boot")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f17f-194">**標題**</span><span class="sxs-lookup"><span data-stu-id="8f17f-194">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-195">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f17f-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-196">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-197">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-197">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-198">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="8f17f-198">Short description of the object a one-line string.</span></span>

<span data-ttu-id="8f17f-199">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8f17f-199">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-200">**ChassisBootupState**</span><span class="sxs-lookup"><span data-stu-id="8f17f-200">**ChassisBootupState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-201">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8f17f-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-203">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 3 \| 啟動狀態" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-203">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|Bootup State")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-204">主機殼的開機狀態。</span><span class="sxs-lookup"><span data-stu-id="8f17f-204">Boot up state of the chassis.</span></span>

<span data-ttu-id="8f17f-205">此值來自于 SMBIOS 資訊中 **系統主機殼或底座** 結構的 **開機狀態** 成員。</span><span class="sxs-lookup"><span data-stu-id="8f17f-205">This value comes from the **Boot-up State** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8f17f-206">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="8f17f-206">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f17f-207">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="8f17f-207">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span data-ttu-id="8f17f-208">**Safe** (3) </span><span class="sxs-lookup"><span data-stu-id="8f17f-208">**Safe** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="8f17f-209">**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="8f17f-209">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="8f17f-210">**重大** (5) </span><span class="sxs-lookup"><span data-stu-id="8f17f-210">**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

<span data-ttu-id="8f17f-211">**無法復原的** (6) </span><span class="sxs-lookup"><span data-stu-id="8f17f-211">**Non-recoverable** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f17f-212">**ChassisSKUNumber**</span><span class="sxs-lookup"><span data-stu-id="8f17f-212">**ChassisSKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-213">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f17f-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-214">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-215">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 3 \| 底座 \| SKU Number" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-215">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|Chassis\|SKU Number")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-216">作為字串的底座或主機殼 SKU 編號。</span><span class="sxs-lookup"><span data-stu-id="8f17f-216">The chassis or enclosure SKU number as a string.</span></span>

<span data-ttu-id="8f17f-217">此值來自于 **系統主機殼** 的 **SKU 編號** 成員或 SMBIOS 資訊中的底座結構。</span><span class="sxs-lookup"><span data-stu-id="8f17f-217">This value comes from the **SKU Number** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="8f17f-218">**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows 10 和 Windows Server 2016 之前，不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="8f17f-218">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-219">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8f17f-219">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-220">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f17f-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-221">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-222">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8f17f-222">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-223">實例之繼承鏈中的第一個具體類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f17f-223">Name of the first concrete class in the inheritance chain of an instance.</span></span> <span data-ttu-id="8f17f-224">您可以使用這個屬性搭配類別的其他屬性，來識別類別和其子類別的所有實例。</span><span class="sxs-lookup"><span data-stu-id="8f17f-224">You can use this property with other properties of the class to identify all instances of the class and its subclasses.</span></span>

<span data-ttu-id="8f17f-225">這個屬性繼承自 [**CIM \_ 系統**](cim-system.md)。</span><span class="sxs-lookup"><span data-stu-id="8f17f-225">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-226">**CurrentTimeZone**</span><span class="sxs-lookup"><span data-stu-id="8f17f-226">**CurrentTimeZone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-227">資料類型： **sint16**</span><span class="sxs-lookup"><span data-stu-id="8f17f-227">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-228">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8f17f-228">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-229">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 時間結構 \| [**時區 \_ \_ 資訊**](/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information) \| 偏差」 ) ，[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「分鐘」 ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-229">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information)\|Bias"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-230">單一電腦系統從國際標準時間 (UTC) 位移的時間量。</span><span class="sxs-lookup"><span data-stu-id="8f17f-230">Amount of time the unitary computer system is offset from Coordinated Universal Time (UTC).</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-231">**DaylightInEffect**</span><span class="sxs-lookup"><span data-stu-id="8f17f-231">**DaylightInEffect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-232">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8f17f-232">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-233">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-234">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Time 函數 \| [**GetTimeZoneInformation**](/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-234">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Time Functions\|[**GetTimeZoneInformation**](/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-235">若 **為 True**，表示日光節約模式為開啟。</span><span class="sxs-lookup"><span data-stu-id="8f17f-235">If **True**, the daylight savings mode is ON.</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-236">**說明**</span><span class="sxs-lookup"><span data-stu-id="8f17f-236">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-237">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f17f-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-239">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-239">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-240">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="8f17f-240">Description of the object.</span></span>

<span data-ttu-id="8f17f-241">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8f17f-241">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-242">**DNSHostName**</span><span class="sxs-lookup"><span data-stu-id="8f17f-242">**DNSHostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-243">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f17f-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-244">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-245">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| GetComputerNameEx \| ComputerNameDnsHostname" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-245">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|GetComputerNameEx\|ComputerNameDnsHostname")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-246">根據功能變數名稱伺服器 (DNS) 的本機電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="8f17f-246">Name of local computer according to the domain name server (DNS).</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-247">**網域**</span><span class="sxs-lookup"><span data-stu-id="8f17f-247">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-248">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f17f-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-249">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-250">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Network Management 結構 \| [**WKSTA \_ INFO \_ 100**](/windows/desktop/api/lmwksta/ns-lmwksta-wksta_info_100) \| wki100 \_ langroup" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-250">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**WKSTA\_INFO\_100**](/windows/desktop/api/lmwksta/ns-lmwksta-wksta_info_100)\|wki100\_langroup")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-251">電腦所屬之網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f17f-251">Name of the domain to which a computer belongs.</span></span>

> [!Note]  
> <span data-ttu-id="8f17f-252">如果電腦不是網域的一部分，則會傳回工作組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f17f-252">If the computer is not part of a domain, then the name of the workgroup is returned.</span></span>

 

</dd> <dt>

<span data-ttu-id="8f17f-253">**DomainRole**</span><span class="sxs-lookup"><span data-stu-id="8f17f-253">**DomainRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-254">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8f17f-254">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-255">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-256">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Directory Service (Ds) 結構 \| [**DSROLE \_ 主域 \_ \_ 資訊 \_ 基本**](/windows/desktop/api/dsrole/ns-dsrole-dsrole_primary_domain_info_basic) \| [**DSROLE \_ 電腦 \_ 角色**](/windows/desktop/api/dsrole/ne-dsrole-dsrole_machine_role) \| MachineRole" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-256">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Directory Service (Ds) Structures\| [**DSROLE\_PRIMARY\_DOMAIN\_INFO\_BASIC**](/windows/desktop/api/dsrole/ns-dsrole-dsrole_primary_domain_info_basic)\|[**DSROLE\_MACHINE\_ROLE**](/windows/desktop/api/dsrole/ne-dsrole-dsrole_machine_role)\| MachineRole")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-257">已指派網域工作組中電腦的角色。</span><span class="sxs-lookup"><span data-stu-id="8f17f-257">Role of a computer in an assigned domain workgroup.</span></span> <span data-ttu-id="8f17f-258">網域工作組是相同網路上的電腦集合。</span><span class="sxs-lookup"><span data-stu-id="8f17f-258">A domain workgroup is a collection of computers on the same network.</span></span> <span data-ttu-id="8f17f-259">例如， **DomainRole** 屬性可能會顯示電腦是成員工作站。</span><span class="sxs-lookup"><span data-stu-id="8f17f-259">For example, a **DomainRole** property may show that a computer is a member workstation.</span></span>

<span data-ttu-id="8f17f-260">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8f17f-260">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>

<span id="Standalone_Workstation"></span><span id="standalone_workstation"></span><span id="STANDALONE_WORKSTATION"></span>

<span data-ttu-id="8f17f-261">**獨立工作站** (0) </span><span class="sxs-lookup"><span data-stu-id="8f17f-261">**Standalone Workstation** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Member_Workstation"></span><span id="member_workstation"></span><span id="MEMBER_WORKSTATION"></span>

<span data-ttu-id="8f17f-262">**成員工作站** (1) </span><span class="sxs-lookup"><span data-stu-id="8f17f-262">**Member Workstation** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Standalone_Server"></span><span id="standalone_server"></span><span id="STANDALONE_SERVER"></span>

<span data-ttu-id="8f17f-263">**獨立伺服器** (2) </span><span class="sxs-lookup"><span data-stu-id="8f17f-263">**Standalone Server** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Member_Server"></span><span id="member_server"></span><span id="MEMBER_SERVER"></span>

<span data-ttu-id="8f17f-264">**成員伺服器** (3) </span><span class="sxs-lookup"><span data-stu-id="8f17f-264">**Member Server** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Backup_Domain_Controller"></span><span id="backup_domain_controller"></span><span id="BACKUP_DOMAIN_CONTROLLER"></span>

<span data-ttu-id="8f17f-265">**備份網域控制站** (4) </span><span class="sxs-lookup"><span data-stu-id="8f17f-265">**Backup Domain Controller** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary_Domain_Controller"></span><span id="primary_domain_controller"></span><span id="PRIMARY_DOMAIN_CONTROLLER"></span>

<span data-ttu-id="8f17f-266">**網域主控站** (5) </span><span class="sxs-lookup"><span data-stu-id="8f17f-266">**Primary Domain Controller** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f17f-267">**EnableDaylightSavingsTime**</span><span class="sxs-lookup"><span data-stu-id="8f17f-267">**EnableDaylightSavingsTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-268">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8f17f-268">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-269">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8f17f-269">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-270">啟用電腦上 (DST) 的日光節約時間。</span><span class="sxs-lookup"><span data-stu-id="8f17f-270">Enables daylight savings time (DST) on a computer.</span></span> <span data-ttu-id="8f17f-271">值為 **True** 表示系統時間在 DST 開始或結束時，會變更為一小時前或之後。</span><span class="sxs-lookup"><span data-stu-id="8f17f-271">A value of **True** indicates that the system time changes to an hour ahead or behind when DST starts or ends.</span></span> <span data-ttu-id="8f17f-272">值為 **False** 表示系統時間在 DST 開始或結束時，不會在一小時前或之後變更為一小時。</span><span class="sxs-lookup"><span data-stu-id="8f17f-272">A value of **False** indicates that the system time does not change to an hour ahead or behind when DST starts or ends.</span></span> <span data-ttu-id="8f17f-273">**Null** 值表示系統上的 DST 狀態是未知的。</span><span class="sxs-lookup"><span data-stu-id="8f17f-273">A value of **NULL** indicates that the DST status is unknown on a system.</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-274">**FrontPanelResetStatus**</span><span class="sxs-lookup"><span data-stu-id="8f17f-274">**FrontPanelResetStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-275">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8f17f-275">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-276">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-277">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 24 \| 硬體 Security Settings \| FrontPanelResetStatus" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-277">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|FrontPanelResetStatus")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-278">下表列出電腦上 [重設] 按鈕的硬體安全性設定。</span><span class="sxs-lookup"><span data-stu-id="8f17f-278">The following table lists the hardware security settings for the reset button on a computer.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8f17f-279">**停用** (0) </span><span class="sxs-lookup"><span data-stu-id="8f17f-279">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8f17f-280">**已啟用** (1) </span><span class="sxs-lookup"><span data-stu-id="8f17f-280">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="8f17f-281">**未執行** (2) </span><span class="sxs-lookup"><span data-stu-id="8f17f-281">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f17f-282">**未知** 的 (3) </span><span class="sxs-lookup"><span data-stu-id="8f17f-282">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f17f-283">**HypervisorPresent**</span><span class="sxs-lookup"><span data-stu-id="8f17f-283">**HypervisorPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-284">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8f17f-284">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-285">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-286">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-286">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-287">若 **為 True**，則表示有虛擬程式。</span><span class="sxs-lookup"><span data-stu-id="8f17f-287">If **True**, a hypervisor is present.</span></span>

<span data-ttu-id="8f17f-288">**Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows 8 和 Windows Server 2012 之前，不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="8f17f-288">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 8 and Windows Server 2012.</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-289">**InfraredSupported**</span><span class="sxs-lookup"><span data-stu-id="8f17f-289">**InfraredSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-290">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8f17f-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-291">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-292">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-292">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-293">若 **為 True**，則表示電腦系統上有紅外線 (IR) 埠。</span><span class="sxs-lookup"><span data-stu-id="8f17f-293">If **True**, an infrared (IR) port exists on a computer system.</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-294">**InitialLoadInfo**</span><span class="sxs-lookup"><span data-stu-id="8f17f-294">**InitialLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-295">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="8f17f-295">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-296">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-297">尋找初始載入裝置或啟動服務以要求作業系統啟動所需的資料。</span><span class="sxs-lookup"><span data-stu-id="8f17f-297">Data required to find the initial load device or boot service to request that the operating system start up.</span></span>

<span data-ttu-id="8f17f-298">這個屬性繼承自 [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md)。</span><span class="sxs-lookup"><span data-stu-id="8f17f-298">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

<span data-ttu-id="8f17f-299">**Windows Server 2008 R2：** 這個屬性是可用的，但卻是空的。</span><span class="sxs-lookup"><span data-stu-id="8f17f-299">**Windows Server 2008 R2:** This property is available, but empty.</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-300">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8f17f-300">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-301">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="8f17f-301">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-302">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-303">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="8f17f-303">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-304">已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="8f17f-304">Object is installed.</span></span> <span data-ttu-id="8f17f-305">物件不需要值來表示已安裝。</span><span class="sxs-lookup"><span data-stu-id="8f17f-305">An object does not need a value to indicate that it is installed.</span></span>

<span data-ttu-id="8f17f-306">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8f17f-306">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-307">**KeyboardPasswordStatus**</span><span class="sxs-lookup"><span data-stu-id="8f17f-307">**KeyboardPasswordStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-308">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8f17f-308">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-309">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-310">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 24 \| 硬體 Security Settings \| KeyboardPasswordStatus" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|KeyboardPasswordStatus")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-311">鍵盤密碼狀態的系統硬體安全性設定。</span><span class="sxs-lookup"><span data-stu-id="8f17f-311">System hardware security settings for Keyboard Password Status.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8f17f-312">**停用** (0) </span><span class="sxs-lookup"><span data-stu-id="8f17f-312">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8f17f-313">**已啟用** (1) </span><span class="sxs-lookup"><span data-stu-id="8f17f-313">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="8f17f-314">**未執行** (2) </span><span class="sxs-lookup"><span data-stu-id="8f17f-314">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f17f-315">**未知** 的 (3) </span><span class="sxs-lookup"><span data-stu-id="8f17f-315">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f17f-316">**LastLoadInfo**</span><span class="sxs-lookup"><span data-stu-id="8f17f-316">**LastLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-317">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f17f-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-318">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-319">**InitialLoadInfo** 屬性的陣列專案，其中包含用來啟動載入之作業系統的資料。</span><span class="sxs-lookup"><span data-stu-id="8f17f-319">Array entry of the **InitialLoadInfo** property that contains the data to start the loaded operating system.</span></span>

<span data-ttu-id="8f17f-320">這個屬性繼承自 [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md)。</span><span class="sxs-lookup"><span data-stu-id="8f17f-320">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-321">**製造商**</span><span class="sxs-lookup"><span data-stu-id="8f17f-321">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-322">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f17f-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-323">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-324">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 1 \| 系統資訊 \| 製造商" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-325">電腦製造商的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f17f-325">Name of a computer manufacturer.</span></span>

<span data-ttu-id="8f17f-326">範例：艾德作品</span><span class="sxs-lookup"><span data-stu-id="8f17f-326">Example: Adventure Works</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-327">**型號**</span><span class="sxs-lookup"><span data-stu-id="8f17f-327">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-328">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f17f-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-329">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-330">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 1 \| 系統資訊 \| Product Name" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-330">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Product Name")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-331">製造商為電腦提供的產品名稱。</span><span class="sxs-lookup"><span data-stu-id="8f17f-331">Product name that a manufacturer gives to a computer.</span></span> <span data-ttu-id="8f17f-332">這個屬性必須有值。</span><span class="sxs-lookup"><span data-stu-id="8f17f-332">This property must have a value.</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-333">**名稱**</span><span class="sxs-lookup"><span data-stu-id="8f17f-333">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-334">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f17f-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-335">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-336">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8f17f-336">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-337">企業環境中 [**CIM \_ 系統**](cim-system.md) 實例的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="8f17f-337">Key of a [**CIM\_System**](cim-system.md) instance in an enterprise environment.</span></span>

<span data-ttu-id="8f17f-338">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8f17f-338">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-339">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="8f17f-339">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-340">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f17f-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-341">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-342">自動產生的電腦系統 **名稱** 值。</span><span class="sxs-lookup"><span data-stu-id="8f17f-342">Computer system **Name** value that is generated automatically.</span></span> <span data-ttu-id="8f17f-343">Cim 系統元件和其衍生物件是通用訊息模型 (CIM) 的最上層物件。 [**\_**](cim-computersystem.md)</span><span class="sxs-lookup"><span data-stu-id="8f17f-343">The [**CIM\_ComputerSystem**](cim-computersystem.md) object and its derivatives are top-level objects of the Common Information Model (CIM).</span></span> <span data-ttu-id="8f17f-344">它們提供數個元件的範圍。</span><span class="sxs-lookup"><span data-stu-id="8f17f-344">They provide the scope for several components.</span></span> <span data-ttu-id="8f17f-345">唯一的 [**CIM \_ 系統**](cim-system.md)金鑰是必要的，但您可以定義啟發式來建立可產生相同名稱的 CIM 系統名稱，且與探索通訊協定無關。 **\_**</span><span class="sxs-lookup"><span data-stu-id="8f17f-345">Unique [**CIM\_System**](cim-system.md) keys are required, but you can define a heuristic to create the **CIM\_ComputerSystem** name that generates the same name, and is independent from the discovery protocol.</span></span> <span data-ttu-id="8f17f-346">當相同的資產或實體發現多次，但無法解析成一個物件時，這可避免清查和管理問題。</span><span class="sxs-lookup"><span data-stu-id="8f17f-346">This prevents inventory and management problems when the same asset or entity is discovered multiple times, but cannot be resolved to one object.</span></span> <span data-ttu-id="8f17f-347">建議使用啟發學習法，但非必要。</span><span class="sxs-lookup"><span data-stu-id="8f17f-347">Using a heuristic is recommended, but not required.</span></span>

<span data-ttu-id="8f17f-348">啟發學習法會在 CIM V2 一般模型規格中概述，並假設已記載的規則會用來決定和指派名稱。</span><span class="sxs-lookup"><span data-stu-id="8f17f-348">The heuristic is outlined in the CIM V2 Common Model specification, and assumes that the documented rules are used to determine and assign a name.</span></span> <span data-ttu-id="8f17f-349">**NameFormat** 值清單會定義指派電腦系統名稱的順序。</span><span class="sxs-lookup"><span data-stu-id="8f17f-349">The **NameFormat** values list defines the order to assign a computer system name.</span></span> <span data-ttu-id="8f17f-350">有數個規則對應到相同的值。</span><span class="sxs-lookup"><span data-stu-id="8f17f-350">Several rules map to the same value.</span></span>

<span data-ttu-id="8f17f-351">使用啟發學習法計算的 [**CIM 系統 \_ 名稱**](cim-computersystem.md) 值是系統的索引鍵值。</span><span class="sxs-lookup"><span data-stu-id="8f17f-351">The [**CIM\_ComputerSystem Name**](cim-computersystem.md) value that is calculated using the heuristic is the key value of the system.</span></span> <span data-ttu-id="8f17f-352">不過，您可以使用別名來指派不同的 **CIM \_** 系統名稱，對您的公司來說可能更是唯一的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f17f-352">However, use aliases to assign a different name for **CIM\_ComputerSystem**, which can be more unique to your company.</span></span>

<span data-ttu-id="8f17f-353">這個屬性繼承自 [**CIM \_ 系統**](cim-system.md)。</span><span class="sxs-lookup"><span data-stu-id="8f17f-353">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="8f17f-354">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="8f17f-354">Values include the following:</span></span>

<dt>

<span id="IP"></span><span id="ip"></span>

<span data-ttu-id="8f17f-355">**Ip** ( 「ip」 ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-355">**IP** ("IP")</span></span>


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

<span data-ttu-id="8f17f-356">**撥號** ( 「撥號」 ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-356">**Dial** ("Dial")</span></span>


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

<span data-ttu-id="8f17f-357">**Hid** ( "hid" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-357">**HID** ("HID")</span></span>


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

<span data-ttu-id="8f17f-358">**NWA** ( "NWA" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-358">**NWA** ("NWA")</span></span>


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

<span data-ttu-id="8f17f-359">**HWA** ( "HWA" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-359">**HWA** ("HWA")</span></span>


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

<span data-ttu-id="8f17f-360">**X25** ( "x25" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-360">**X25** ("X25")</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

<span data-ttu-id="8f17f-361">**Isdn** ( "isdn" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-361">**ISDN** ("ISDN")</span></span>


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

<span data-ttu-id="8f17f-362">**Ipx** ( 「ipx」 ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-362">**IPX** ("IPX")</span></span>


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

<span data-ttu-id="8f17f-363">**DCC** ( "DCC" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-363">**DCC** ("DCC")</span></span>


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

<span data-ttu-id="8f17f-364">**Icd** ( 「icd」 ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-364">**ICD** ("ICD")</span></span>


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

<span data-ttu-id="8f17f-365">**E.** ( "e. 164" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-365">**E.164** ("E.164")</span></span>


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

<span data-ttu-id="8f17f-366">**Sna** ( 「sna」 ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-366">**SNA** ("SNA")</span></span>


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

<span data-ttu-id="8f17f-367">**Oid/osi** ( "OID/osi" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-367">**OID/OSI** ("OID/OSI")</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8f17f-368">**其他** ( "其他" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-368">**Other** ("Other")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f17f-369">**NetworkServerModeEnabled**</span><span class="sxs-lookup"><span data-stu-id="8f17f-369">**NetworkServerModeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-370">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8f17f-370">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-371">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-372">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Network Management 結構 \| [**伺服器 \_ 資訊 \_ 101**](/windows/desktop/api/lmserver/ns-lmserver-server_info_101) \| sv101 \_ type \| SV \_ type \_ SERVER" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-372">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SERVER\_INFO\_101**](/windows/desktop/api/lmserver/ns-lmserver-server_info_101)\|sv101\_type\|SV\_TYPE\_SERVER")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-373">若 **為 True**，則會啟用網路伺服器模式。</span><span class="sxs-lookup"><span data-stu-id="8f17f-373">If **True**, the network Server Mode is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-374">**NumberOfLogicalProcessors**</span><span class="sxs-lookup"><span data-stu-id="8f17f-374">**NumberOfLogicalProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-375">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8f17f-375">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-376">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-377">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-377">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-378">電腦上可用的邏輯處理器數目。</span><span class="sxs-lookup"><span data-stu-id="8f17f-378">Number of logical processors available on the computer.</span></span>

<span data-ttu-id="8f17f-379">您可以使用 **NumberOfLogicalProcessors** 和 **NumberOfProcessors** 來判斷電腦是否為超執行緒。</span><span class="sxs-lookup"><span data-stu-id="8f17f-379">You can use **NumberOfLogicalProcessors** and **NumberOfProcessors** to determine if the computer is hyperthreading.</span></span> <span data-ttu-id="8f17f-380">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="8f17f-380">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-381">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="8f17f-381">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-382">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8f17f-382">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-383">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-384">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| 系統資訊結構 \| [**系統 \_ 資訊**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| dwNumberOfProcessors" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-384">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Information Structures\|[**SYSTEM\_INFO**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info)\|dwNumberOfProcessors")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-385">系統目前可用的實體處理器數目。</span><span class="sxs-lookup"><span data-stu-id="8f17f-385">Number of physical processors currently available on a system.</span></span> <span data-ttu-id="8f17f-386">這是系統已啟用的處理器數目，不包括已停用的處理器。</span><span class="sxs-lookup"><span data-stu-id="8f17f-386">This is the number of enabled processors for a system, which does not include the disabled processors.</span></span> <span data-ttu-id="8f17f-387">如果電腦系統有兩個實體處理器，每個都包含兩個邏輯處理器，則 **NumberOfProcessors** 的值為2，而 **NumberOfLogicalProcessors** 為4。</span><span class="sxs-lookup"><span data-stu-id="8f17f-387">If a computer system has two physical processors each containing two logical processors, then the value of **NumberOfProcessors** is 2 and **NumberOfLogicalProcessors** is 4.</span></span> <span data-ttu-id="8f17f-388">這些處理器可能是多核心的，也可能是超執行緒處理器。</span><span class="sxs-lookup"><span data-stu-id="8f17f-388">The processors may be multicore or they may be hyperthreading processors.</span></span> <span data-ttu-id="8f17f-389">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="8f17f-389">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-390">**OEMLogoBitmap**</span><span class="sxs-lookup"><span data-stu-id="8f17f-390">**OEMLogoBitmap**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-391">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="8f17f-391">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-392">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-393">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-393">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-394">原始設備製造商 (OEM) 所建立的點陣圖資料清單。</span><span class="sxs-lookup"><span data-stu-id="8f17f-394">List of data for a bitmap that the original equipment manufacturer (OEM) creates.</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-395">**OEMStringArray**</span><span class="sxs-lookup"><span data-stu-id="8f17f-395">**OEMStringArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-396">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="8f17f-396">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-397">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-398">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 11 \| OEM Strings" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-398">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 11\|OEM Strings")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-399">OEM 定義的自由格式字串清單。</span><span class="sxs-lookup"><span data-stu-id="8f17f-399">List of free-form strings that an OEM defines.</span></span> <span data-ttu-id="8f17f-400">例如，OEM 會定義系統參考檔的元件編號、製造商連絡人資訊等等。</span><span class="sxs-lookup"><span data-stu-id="8f17f-400">For example, an OEM defines the part numbers for system reference documents, manufacturer contact information, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-401">**PartOfDomain**</span><span class="sxs-lookup"><span data-stu-id="8f17f-401">**PartOfDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-402">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8f17f-402">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-403">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-404">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-404">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-405">若 **為 True**，則表示電腦是網域的一部分。</span><span class="sxs-lookup"><span data-stu-id="8f17f-405">If **True**, the computer is part of a domain.</span></span> <span data-ttu-id="8f17f-406">如果值為 **Null**，則電腦不在網域中，或狀態不明。</span><span class="sxs-lookup"><span data-stu-id="8f17f-406">If the value is **NULL**, the computer is not in a domain or the status is unknown.</span></span> <span data-ttu-id="8f17f-407">如果您將電腦從網域中移除，此值就會變成 **false**。</span><span class="sxs-lookup"><span data-stu-id="8f17f-407">If you remove the computer from a domain, the value becomes **false**.</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-408">**PauseAfterReset**</span><span class="sxs-lookup"><span data-stu-id="8f17f-408">**PauseAfterReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-409">資料類型： **sint64**</span><span class="sxs-lookup"><span data-stu-id="8f17f-409">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-410">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-411">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 23 \| Timeout" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫秒" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-411">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|Timeout"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-412">啟動重新開機之前的時間延遲（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="8f17f-412">Time delay before a reboot is initiated in milliseconds.</span></span> <span data-ttu-id="8f17f-413">它會在系統電源週期、本機或遠端系統重設，以及自動重設系統之後使用。</span><span class="sxs-lookup"><span data-stu-id="8f17f-413">It is used after a system power cycle, local or remote system reset, and automatic system reset.</span></span> <span data-ttu-id="8f17f-414">1)  (值為1，表示暫停值不明。</span><span class="sxs-lookup"><span data-stu-id="8f17f-414">A value of  1 (minus one) indicates that the pause value is unknown.</span></span>

<span data-ttu-id="8f17f-415">**Windows Vista：** 這個屬性可能會傳回未知的數位。</span><span class="sxs-lookup"><span data-stu-id="8f17f-415">**Windows Vista:** This property may return an unknown number.</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-416">**PCSystemType**</span><span class="sxs-lookup"><span data-stu-id="8f17f-416">**PCSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-417">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8f17f-417">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-418">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-419">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-419">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-420">使用中的電腦類型，例如膝上型電腦、桌上型電腦或平板電腦。</span><span class="sxs-lookup"><span data-stu-id="8f17f-420">Type of the computer in use, such as laptop, desktop, or Tablet.</span></span>

<dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

<span data-ttu-id="8f17f-421"><span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>**未指定** (0) </span><span class="sxs-lookup"><span data-stu-id="8f17f-421"><span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>**Unspecified** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="8f17f-422"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (1) </span><span class="sxs-lookup"><span data-stu-id="8f17f-422"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>

<span data-ttu-id="8f17f-423"><span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>**Mobile** (2) </span><span class="sxs-lookup"><span data-stu-id="8f17f-423"><span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>**Mobile** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>

<span data-ttu-id="8f17f-424"><span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>**工作站** (3) </span><span class="sxs-lookup"><span data-stu-id="8f17f-424"><span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>**Workstation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

<span data-ttu-id="8f17f-425"><span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>**Enterprise Server** (4) </span><span class="sxs-lookup"><span data-stu-id="8f17f-425"><span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>**Enterprise Server** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

<span data-ttu-id="8f17f-426"><span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>**SOHO 伺服器** (5) </span><span class="sxs-lookup"><span data-stu-id="8f17f-426"><span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>**SOHO Server** (5)</span></span>


</dt> <dd>

<span data-ttu-id="8f17f-427">小型辦公室和家用辦公室 (SOHO) Server</span><span class="sxs-lookup"><span data-stu-id="8f17f-427">Small Office and Home Office (SOHO) Server</span></span>

</dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

<span data-ttu-id="8f17f-428"><span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>**設備電腦** (6) </span><span class="sxs-lookup"><span data-stu-id="8f17f-428"><span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>**Appliance PC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

<span data-ttu-id="8f17f-429"><span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>**效能伺服器** (7) </span><span class="sxs-lookup"><span data-stu-id="8f17f-429"><span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>**Performance Server** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="8f17f-430"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**最大** (8) </span><span class="sxs-lookup"><span data-stu-id="8f17f-430"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f17f-431">**PCSystemTypeEx**</span><span class="sxs-lookup"><span data-stu-id="8f17f-431">**PCSystemTypeEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-432">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8f17f-432">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-433">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-433">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-434">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-434">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-435">使用中的電腦類型，例如膝上型電腦、桌上型電腦或平板電腦。</span><span class="sxs-lookup"><span data-stu-id="8f17f-435">Type of the computer in use, such as laptop, desktop, or Tablet.</span></span>

<span data-ttu-id="8f17f-436">**Windows server 2012、Windows 8、Windows server 2008 R2、Windows 7、Windows server 2008 和 Windows Vista：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="8f17f-436">**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

<span data-ttu-id="8f17f-437">**未指定** (0) </span><span class="sxs-lookup"><span data-stu-id="8f17f-437">**Unspecified** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="8f17f-438">**Desktop** (1) </span><span class="sxs-lookup"><span data-stu-id="8f17f-438">**Desktop** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>

<span data-ttu-id="8f17f-439">**Mobile** (2) </span><span class="sxs-lookup"><span data-stu-id="8f17f-439">**Mobile** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>

<span data-ttu-id="8f17f-440">**工作站** (3) </span><span class="sxs-lookup"><span data-stu-id="8f17f-440">**Workstation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

<span data-ttu-id="8f17f-441">**Enterprise Server** (4) </span><span class="sxs-lookup"><span data-stu-id="8f17f-441">**Enterprise Server** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

<span data-ttu-id="8f17f-442">**SOHO 伺服器** (5) </span><span class="sxs-lookup"><span data-stu-id="8f17f-442">**SOHO Server** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

<span data-ttu-id="8f17f-443">**設備電腦** (6) </span><span class="sxs-lookup"><span data-stu-id="8f17f-443">**Appliance PC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

<span data-ttu-id="8f17f-444">**效能伺服器** (7) </span><span class="sxs-lookup"><span data-stu-id="8f17f-444">**Performance Server** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Slate"></span><span id="slate"></span><span id="SLATE"></span>

<span data-ttu-id="8f17f-445"> (8) 的 **平板**</span><span class="sxs-lookup"><span data-stu-id="8f17f-445">**Slate** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="8f17f-446">**最大** (9) </span><span class="sxs-lookup"><span data-stu-id="8f17f-446">**Maximum** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f17f-447">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8f17f-447">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-448">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="8f17f-448">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-449">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-450">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統電源控制項 \| 001.2 ") </span><span class="sxs-lookup"><span data-stu-id="8f17f-450">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Power Controls\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-451">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="8f17f-451">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="8f17f-452">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="8f17f-452">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f17f-453"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="8f17f-453"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="8f17f-454"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="8f17f-454"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8f17f-455"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="8f17f-455"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8f17f-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="8f17f-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8f17f-457">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="8f17f-457">The power management features are currently enabled, but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="8f17f-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="8f17f-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8f17f-459">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="8f17f-459">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="8f17f-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="8f17f-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="8f17f-461">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="8f17f-461">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="8f17f-462">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="8f17f-462">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="8f17f-463">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="8f17f-463">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="8f17f-464"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="8f17f-464"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="8f17f-465">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="8f17f-465">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="8f17f-466"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="8f17f-466"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="8f17f-467">支援計時 Power-On</span><span class="sxs-lookup"><span data-stu-id="8f17f-467">Timed Power-On Supported</span></span>

<span data-ttu-id="8f17f-468">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="8f17f-468">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f17f-469">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="8f17f-469">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-470">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8f17f-470">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-471">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-471">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-472">若 **為 True**，則裝置可以電源管理，例如，裝置可進入暫停模式，依此類推。</span><span class="sxs-lookup"><span data-stu-id="8f17f-472">If **True**, device can be power-managed, for example, a device can be put into suspend mode, and so on.</span></span> <span data-ttu-id="8f17f-473">這個屬性不會指出電源管理功能目前已啟用，但它會指出邏輯裝置能夠進行電源管理。</span><span class="sxs-lookup"><span data-stu-id="8f17f-473">This property does not indicate that power management features are enabled currently, but it does indicate that the logical device is capable of power management.</span></span>

<span data-ttu-id="8f17f-474">這個屬性繼承自 [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md)。</span><span class="sxs-lookup"><span data-stu-id="8f17f-474">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-475">**PowerOnPasswordStatus**</span><span class="sxs-lookup"><span data-stu-id="8f17f-475">**PowerOnPasswordStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-476">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8f17f-476">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-477">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-478">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 24 \| 硬體 Security Settings \| PowerOnPasswordStatus" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-478">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|PowerOnPasswordStatus")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-479">Power-On 密碼狀態的系統硬體安全性設定。</span><span class="sxs-lookup"><span data-stu-id="8f17f-479">System hardware security settings for Power-On Password Status.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8f17f-480">**停用** (0) </span><span class="sxs-lookup"><span data-stu-id="8f17f-480">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8f17f-481">**已啟用** (1) </span><span class="sxs-lookup"><span data-stu-id="8f17f-481">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="8f17f-482">**未執行** (2) </span><span class="sxs-lookup"><span data-stu-id="8f17f-482">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f17f-483">**未知** 的 (3) </span><span class="sxs-lookup"><span data-stu-id="8f17f-483">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f17f-484">**>powerstate**</span><span class="sxs-lookup"><span data-stu-id="8f17f-484">**PowerState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-485">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8f17f-485">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-486">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-487">電腦的目前電源狀態及其相關聯的作業系統。</span><span class="sxs-lookup"><span data-stu-id="8f17f-487">Current power state of a computer and its associated operating system.</span></span> <span data-ttu-id="8f17f-488">省電狀態具有下列值： [值 4] ([未知]) 表示系統已知處於省電模式，但在此模式中的確切狀態為未知;2 (低電源模式) 指出系統處於省電狀態，但仍在運作中，而且效能可能會降低。3 (待命) 指出系統無法正常運作，但可快速進入完整電源;和 7 (警告) 指出電腦系統處於警告狀態和省電模式。</span><span class="sxs-lookup"><span data-stu-id="8f17f-488">The power saving states have the following values: Value 4 (Unknown) indicates that the system is known to be in a power save mode, but its exact status in this mode is unknown; 2 (Low Power Mode) indicates that the system is in a power save state, but still functioning and may exhibit degraded performance; 3 (Standby) indicates that the system is not functioning, but could be brought to full power quickly; and 7 (Warning) indicates that the computer system is in a warning state and a power save mode.</span></span>

<span data-ttu-id="8f17f-489">這個屬性繼承自 [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md)。</span><span class="sxs-lookup"><span data-stu-id="8f17f-489">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f17f-490"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="8f17f-490"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="8f17f-491"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1) </span><span class="sxs-lookup"><span data-stu-id="8f17f-491"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="8f17f-492"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (2) </span><span class="sxs-lookup"><span data-stu-id="8f17f-492"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="8f17f-493"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (3) </span><span class="sxs-lookup"><span data-stu-id="8f17f-493"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="8f17f-494"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (4) </span><span class="sxs-lookup"><span data-stu-id="8f17f-494"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="8f17f-495"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**電源週期** (5) </span><span class="sxs-lookup"><span data-stu-id="8f17f-495"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="8f17f-496"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (6) 的電源</span><span class="sxs-lookup"><span data-stu-id="8f17f-496"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="8f17f-497"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (7) </span><span class="sxs-lookup"><span data-stu-id="8f17f-497"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>

<span data-ttu-id="8f17f-498"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>省 **電-休眠** (8) </span><span class="sxs-lookup"><span data-stu-id="8f17f-498"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>**Power Save - Hibernate** (8)</span></span>


</dt> <dd>

<span data-ttu-id="8f17f-499">省電休眠。</span><span class="sxs-lookup"><span data-stu-id="8f17f-499">Power save   hibernate.</span></span>

</dd> <dt>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>

<span data-ttu-id="8f17f-500"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>省 **電-軟關閉** (9) </span><span class="sxs-lookup"><span data-stu-id="8f17f-500"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>**Power Save - Soft Off** (9)</span></span>


</dt> <dd>

<span data-ttu-id="8f17f-501">省電。</span><span class="sxs-lookup"><span data-stu-id="8f17f-501">Power save   soft off.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f17f-502">**PowerSupplyState**</span><span class="sxs-lookup"><span data-stu-id="8f17f-502">**PowerSupplyState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-503">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8f17f-503">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-504">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-504">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-505">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「SMBIOS \| Type 3 \| 系統主機殼或底座 \| 電源供應器狀態」 ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-505">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|System Enclosure or Chassis\|Power Supply State")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-506">電源供應器的狀態，或在上一次開機時提供的電源。</span><span class="sxs-lookup"><span data-stu-id="8f17f-506">State of the power supply or supplies when last booted.</span></span>

<span data-ttu-id="8f17f-507">此值來自于 SMBIOS 資訊中 **系統主機殼或底座** 結構的 **電源供應器狀態** 成員。</span><span class="sxs-lookup"><span data-stu-id="8f17f-507">This value comes from the **Power Supply State** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="8f17f-508">下列清單會識別此屬性的值。</span><span class="sxs-lookup"><span data-stu-id="8f17f-508">The following list identifies the values for this property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8f17f-509"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="8f17f-509"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f17f-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="8f17f-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span data-ttu-id="8f17f-511"><span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>**Safe** (3) </span><span class="sxs-lookup"><span data-stu-id="8f17f-511"><span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>**Safe** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="8f17f-512"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="8f17f-512"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="8f17f-513"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**重大** (5) </span><span class="sxs-lookup"><span data-stu-id="8f17f-513"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

<span data-ttu-id="8f17f-514"><span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>**無法復原的** (6) </span><span class="sxs-lookup"><span data-stu-id="8f17f-514"><span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>**Non-recoverable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="8f17f-515">恢復</span><span class="sxs-lookup"><span data-stu-id="8f17f-515">Nonrecoverable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f17f-516">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="8f17f-516">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-517">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f17f-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-518">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-519">主要系統擁有者的連絡人資訊，例如電話號碼、電子郵件地址等等。</span><span class="sxs-lookup"><span data-stu-id="8f17f-519">Contact information for the primary system owner, for example, phone number, email address, and so on.</span></span>

<span data-ttu-id="8f17f-520">這個屬性繼承自 [**CIM \_ 系統**](cim-system.md)。</span><span class="sxs-lookup"><span data-stu-id="8f17f-520">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-521">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="8f17f-521">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-522">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f17f-522">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-523">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-523">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-524">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="8f17f-524">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-525">主要系統擁有者的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f17f-525">Name of the primary system owner.</span></span>

<span data-ttu-id="8f17f-526">這個屬性繼承自 [**CIM \_ 系統**](cim-system.md)。</span><span class="sxs-lookup"><span data-stu-id="8f17f-526">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-527">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="8f17f-527">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-528">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8f17f-528">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-529">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-529">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-530">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統硬體安全性 \| 001.4」 ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-530">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Hardware Security\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-531">如果啟用，則值為4，而單一電腦系統可以使用 [電源] 和 [重設] 按鈕來重設。</span><span class="sxs-lookup"><span data-stu-id="8f17f-531">If enabled, the value is 4 and the unitary computer system can be reset using the power and reset buttons.</span></span> <span data-ttu-id="8f17f-532">如果停用，則值為3，不允許重設。</span><span class="sxs-lookup"><span data-stu-id="8f17f-532">If disabled, the value is 3, and a reset is not allowed.</span></span>

<span data-ttu-id="8f17f-533">這個屬性繼承自 [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md)。</span><span class="sxs-lookup"><span data-stu-id="8f17f-533">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8f17f-534"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="8f17f-534"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f17f-535"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="8f17f-535"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8f17f-536"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="8f17f-536"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8f17f-537"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (4) </span><span class="sxs-lookup"><span data-stu-id="8f17f-537"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="8f17f-538"><span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>**未執行** (5) </span><span class="sxs-lookup"><span data-stu-id="8f17f-538"><span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>**Not Implemented** (5)</span></span>


</dt> <dd>

<span data-ttu-id="8f17f-539">恢復</span><span class="sxs-lookup"><span data-stu-id="8f17f-539">Nonrecoverable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f17f-540">**ResetCount**</span><span class="sxs-lookup"><span data-stu-id="8f17f-540">**ResetCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-541">資料類型： **sint16**</span><span class="sxs-lookup"><span data-stu-id="8f17f-541">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-542">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-543">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「SMBIOS \| 類型 23 \| 系統重設 \| 計數」 ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-543">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|System Reset\|Reset Count")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-544">自上次重設之後自動重設的次數。</span><span class="sxs-lookup"><span data-stu-id="8f17f-544">Number of automatic resets since the last reset.</span></span> <span data-ttu-id="8f17f-545">1 (的值減去一個) 表示計數未知。</span><span class="sxs-lookup"><span data-stu-id="8f17f-545">A value of  1 (minus one) indicates that the count is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-546">**ResetLimit**</span><span class="sxs-lookup"><span data-stu-id="8f17f-546">**ResetLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-547">資料類型： **sint16**</span><span class="sxs-lookup"><span data-stu-id="8f17f-547">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-548">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-549">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「SMBIOS \| 類型 23 \| 系統重設 \| 重設限制」 ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-549">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|System Reset\| Reset Limit")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-550">嘗試重設系統的連續次數。</span><span class="sxs-lookup"><span data-stu-id="8f17f-550">Number of consecutive times a system reset is attempted.</span></span> <span data-ttu-id="8f17f-551">1 (的值減去一個) 表示限制未知。</span><span class="sxs-lookup"><span data-stu-id="8f17f-551">A value of  1 (minus one) indicates that the limit is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-552">**角色**</span><span class="sxs-lookup"><span data-stu-id="8f17f-552">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-553">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="8f17f-553">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-554">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8f17f-554">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-555">此清單會指定資訊技術環境中系統的角色。</span><span class="sxs-lookup"><span data-stu-id="8f17f-555">List that specifies the roles of a system in the information technology environment.</span></span>

<span data-ttu-id="8f17f-556">這個屬性繼承自 [**CIM \_ 系統**](cim-system.md)。</span><span class="sxs-lookup"><span data-stu-id="8f17f-556">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-557">**狀態**</span><span class="sxs-lookup"><span data-stu-id="8f17f-557">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-558">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f17f-558">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-559">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-559">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-560">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-560">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-561">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="8f17f-561">Current status of an object.</span></span>

<span data-ttu-id="8f17f-562">針對 Win32_ComputerSystem，狀態一律為「確定」。</span><span class="sxs-lookup"><span data-stu-id="8f17f-562">For Win32_ComputerSystem, the Status is always “OK”.</span></span>

<span data-ttu-id="8f17f-563">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8f17f-563">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dl>

</dd> <dt>

<span data-ttu-id="8f17f-564">**SupportContactDescription**</span><span class="sxs-lookup"><span data-stu-id="8f17f-564">**SupportContactDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-565">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="8f17f-565">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-566">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-566">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-567">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| [**GetPrivateProfileString**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilestring) \| Support Information" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-567">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetPrivateProfileString**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilestring)\|Support Information")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-568">Windows 作業系統的支援連絡人資訊清單。</span><span class="sxs-lookup"><span data-stu-id="8f17f-568">List of the support contact information for the Windows operating system.</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-569">**SystemFamily**</span><span class="sxs-lookup"><span data-stu-id="8f17f-569">**SystemFamily**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-570">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f17f-570">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-571">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-571">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-572">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「SMBIOS \| 類型 1 \| 系統資訊 \| 系列」 ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-572">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Family")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-573">特定電腦所屬的系列。</span><span class="sxs-lookup"><span data-stu-id="8f17f-573">The family to which a particular computer belongs.</span></span> <span data-ttu-id="8f17f-574">系列是指一組類似于硬體或軟體觀點的電腦，但不完全相同。</span><span class="sxs-lookup"><span data-stu-id="8f17f-574">A family refers to a set of computers that are similar but not identical from a hardware or software point of view.</span></span>

<span data-ttu-id="8f17f-575">此值來自 SMBIOS 資訊中 **系統資訊** 結構的 **家庭** 成員。</span><span class="sxs-lookup"><span data-stu-id="8f17f-575">This value comes from the **Family** member of the **System Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="8f17f-576">**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows 10 和 Windows Server 2016 之前，不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="8f17f-576">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-577">**SystemSKUNumber**</span><span class="sxs-lookup"><span data-stu-id="8f17f-577">**SystemSKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-578">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f17f-578">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-579">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-579">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-580">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 1 \| 系統資訊 \| SKU Number" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-580">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|SKU Number")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-581">識別要銷售的特定電腦設定。</span><span class="sxs-lookup"><span data-stu-id="8f17f-581">Identifies a particular computer configuration for sale.</span></span> <span data-ttu-id="8f17f-582">有時也稱為產品識別碼或採購單號碼。</span><span class="sxs-lookup"><span data-stu-id="8f17f-582">It is sometimes also called a product ID or purchase order number.</span></span>

<span data-ttu-id="8f17f-583">此值來自 SMBIOS 資訊中 **系統資訊** 結構的 **SKU 編號** 成員。</span><span class="sxs-lookup"><span data-stu-id="8f17f-583">This value comes from the **SKU Number** member of the **System Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="8f17f-584">**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows 10 和 Windows Server 2016 之前，不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="8f17f-584">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-585">**SystemStartupDelay**</span><span class="sxs-lookup"><span data-stu-id="8f17f-585">**SystemStartupDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-586">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8f17f-586">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-587">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8f17f-587">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-588">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、[**許可權**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "SeSystemEnvironmentPrivilege" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| [**GetPrivateProfileInt**](/windows/desktop/api/winbase/nf-winbase-getprivateprofileint) \| Boot 載入器 \| timeout" ) 、[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "seconds" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-588">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetPrivateProfileInt**](/windows/desktop/api/winbase/nf-winbase-getprivateprofileint)\|Boot Loader\|timeout"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-589">**SystemStartupDelay** 不再可供使用，因為 Boot.ini 不會用來設定系統啟動。</span><span class="sxs-lookup"><span data-stu-id="8f17f-589">**SystemStartupDelay** is no longer available for use because Boot.ini is not used to configure system startup.</span></span> <span data-ttu-id="8f17f-590">相反地，請使用開機設定資料 (BCD) WMI 提供者或 **Bcdedit** 命令所提供的 [bcd 類別](/previous-versions/windows/desktop/bcd/bcd-classes)。</span><span class="sxs-lookup"><span data-stu-id="8f17f-590">Instead, use the [BCD classes](/previous-versions/windows/desktop/bcd/bcd-classes) supplied by the Boot Configuration Data (BCD) WMI provider or the **Bcdedit** command.</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-591">**SystemStartupOptions**</span><span class="sxs-lookup"><span data-stu-id="8f17f-591">**SystemStartupOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-592">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="8f17f-592">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-593">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8f17f-593">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-594">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)，[**許可權**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "SeSystemEnvironmentPrivilege" ) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| [**GetPrivateProfileSection**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilesection) \| 作業系統" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-594">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetPrivateProfileSection**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilesection)\|Operating Systems")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-595">**SystemStartupOptions** 不再可供使用，因為 Boot.ini 不會用來設定系統啟動。</span><span class="sxs-lookup"><span data-stu-id="8f17f-595">**SystemStartupOptions** is no longer available for use because Boot.ini is not used to configure system startup.</span></span> <span data-ttu-id="8f17f-596">相反地，請使用開機設定資料 (BCD) WMI 提供者或 **Bcdedit** 命令所提供的 [bcd 類別](/previous-versions/windows/desktop/bcd/bcd-classes)。</span><span class="sxs-lookup"><span data-stu-id="8f17f-596">Instead, use the [BCD classes](/previous-versions/windows/desktop/bcd/bcd-classes) supplied by the Boot Configuration Data (BCD) WMI provider or the **Bcdedit** command.</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-597">**SystemStartupSetting**</span><span class="sxs-lookup"><span data-stu-id="8f17f-597">**SystemStartupSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-598">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="8f17f-598">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-599">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8f17f-599">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-600">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**許可權**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "SeSystemEnvironmentPrivilege" ) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-600">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-601">**SystemStartupSetting** 不再可供使用，因為 Boot.ini 不會用來設定系統啟動。</span><span class="sxs-lookup"><span data-stu-id="8f17f-601">**SystemStartupSetting** is no longer available for use because Boot.ini is not used to configure system startup.</span></span> <span data-ttu-id="8f17f-602">相反地，請使用開機設定資料 (BCD) WMI 提供者或 **Bcdedit** 命令所提供的 [bcd 類別](/previous-versions/windows/desktop/bcd/bcd-classes)。</span><span class="sxs-lookup"><span data-stu-id="8f17f-602">Instead, use the [BCD classes](/previous-versions/windows/desktop/bcd/bcd-classes) supplied by the Boot Configuration Data (BCD) WMI provider or the **Bcdedit** command.</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-603">**SystemType**</span><span class="sxs-lookup"><span data-stu-id="8f17f-603">**SystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-604">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f17f-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-605">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-605">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-606">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| 系統資訊結構 \| [**系統 \_ 資訊**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| wProcessorArchitecture" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-606">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Information Structures\|[**SYSTEM\_INFO**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info)\|wProcessorArchitecture")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-607">在 Windows 電腦上執行的系統。</span><span class="sxs-lookup"><span data-stu-id="8f17f-607">System running on the Windows-based computer.</span></span> <span data-ttu-id="8f17f-608">這個屬性必須有值。</span><span class="sxs-lookup"><span data-stu-id="8f17f-608">This property must have a value.</span></span>

<span data-ttu-id="8f17f-609">下列清單會識別此屬性的一些可能值。</span><span class="sxs-lookup"><span data-stu-id="8f17f-609">The following list identifies some of the possible values for this property.</span></span>

<dl> <dd><span data-ttu-id="8f17f-610">「x64 型電腦」</span><span class="sxs-lookup"><span data-stu-id="8f17f-610">"x64-based PC"</span></span></dd> <dd><span data-ttu-id="8f17f-611">「X86 型電腦」</span><span class="sxs-lookup"><span data-stu-id="8f17f-611">"X86-based PC"</span></span></dd> <dd><span data-ttu-id="8f17f-612">「MIPS 型電腦」</span><span class="sxs-lookup"><span data-stu-id="8f17f-612">"MIPS-based PC"</span></span></dd> <dd><span data-ttu-id="8f17f-613">「以 Alpha 為基礎的電腦」</span><span class="sxs-lookup"><span data-stu-id="8f17f-613">"Alpha-based PC"</span></span></dd> <dd><span data-ttu-id="8f17f-614">「Power PC」</span><span class="sxs-lookup"><span data-stu-id="8f17f-614">"Power PC"</span></span></dd> <dd><span data-ttu-id="8f17f-615">"SH-x PC"</span><span class="sxs-lookup"><span data-stu-id="8f17f-615">"SH-x PC"</span></span></dd> <dd><span data-ttu-id="8f17f-616">「StrongARM PC」</span><span class="sxs-lookup"><span data-stu-id="8f17f-616">"StrongARM PC"</span></span></dd> <dd><span data-ttu-id="8f17f-617">「64位 Intel 電腦」</span><span class="sxs-lookup"><span data-stu-id="8f17f-617">"64-bit Intel PC"</span></span></dd> <dd><span data-ttu-id="8f17f-618">「64位 Alpha 電腦」</span><span class="sxs-lookup"><span data-stu-id="8f17f-618">"64-bit Alpha PC"</span></span></dd> <dd><span data-ttu-id="8f17f-619">不明</span><span class="sxs-lookup"><span data-stu-id="8f17f-619">"Unknown"</span></span></dd> <dd><span data-ttu-id="8f17f-620">「X86-Nec98 PC」</span><span class="sxs-lookup"><span data-stu-id="8f17f-620">"X86-Nec98 PC"</span></span></dd> </dl>

<dt>

<span id="X86-based_PC"></span><span id="x86-based_pc"></span><span id="X86-BASED_PC"></span>

<span data-ttu-id="8f17f-621">**X86 電腦** ( 「X86 型電腦」 ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-621">**X86-based PC** ("X86-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS-based_PC"></span><span id="mips-based_pc"></span><span id="MIPS-BASED_PC"></span>

<span data-ttu-id="8f17f-622">以 **mips 為基礎的電腦** ( 「MIPS 型電腦」 ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-622">**MIPS-based PC** ("MIPS-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha-based_PC"></span><span id="alpha-based_pc"></span><span id="ALPHA-BASED_PC"></span>

<span data-ttu-id="8f17f-623">以 **Alpha 為基礎的電腦** ( 「ALPHA 型電腦」 ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-623">**Alpha-based PC** ("Alpha-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC"></span><span id="power_pc"></span><span id="POWER_PC"></span>

<span data-ttu-id="8f17f-624">**POWER pc** ( 「power pc」 ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-624">**Power PC** ("Power PC")</span></span>


</dt> <dd></dd> <dt>

<span id="SH-x_PC"></span><span id="sh-x_pc"></span><span id="SH-X_PC"></span>

<span data-ttu-id="8f17f-625">**Sh-x pc** ( "SH-x pc" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-625">**SH-x PC** ("SH-x PC")</span></span>


</dt> <dd></dd> <dt>

<span id="StrongARM_PC"></span><span id="strongarm_pc"></span><span id="STRONGARM_PC"></span>

<span data-ttu-id="8f17f-626">**STRONGARM pc** ( "StrongARM pc" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-626">**StrongARM PC** ("StrongARM PC")</span></span>


</dt> <dd></dd> <dt>

<span id="64-bit_Intel_PC"></span><span id="64-bit_intel_pc"></span><span id="64-BIT_INTEL_PC"></span>

<span data-ttu-id="8f17f-627">**64 位 INTEL pc** ( 「64位 intel pc」 ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-627">**64-bit Intel PC** ("64-bit Intel PC")</span></span>


</dt> <dd></dd> <dt>

<span id="x64-based_PC"></span><span id="x64-based_pc"></span><span id="X64-BASED_PC"></span>

<span data-ttu-id="8f17f-628">以 **x64 為基礎的電腦** ( 「X64 型電腦」 ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-628">**x64-based PC** ("x64-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f17f-629">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-629">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="X86-Nec98_PC"></span><span id="x86-nec98_pc"></span><span id="X86-NEC98_PC"></span>

<span data-ttu-id="8f17f-630">**X86 NEC98 pc** ( 「X86-Nec98 pc」 ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-630">**X86-Nec98 PC** ("X86-Nec98 PC")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f17f-631">**ThermalState**</span><span class="sxs-lookup"><span data-stu-id="8f17f-631">**ThermalState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-632">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8f17f-632">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-633">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-633">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-634">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「SMBIOS \| Type 3 \| 系統主機殼或底座 \| 熱狀態」 ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-634">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|System Enclosure or Chassis\|Thermal State")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-635">最後一次開機時系統的熱狀態。</span><span class="sxs-lookup"><span data-stu-id="8f17f-635">Thermal state of the system when last booted.</span></span>

<span data-ttu-id="8f17f-636">此值來自于 SMBIOS 資訊中 **系統主機殼或底座** 結構的 **溫度狀態** 成員。</span><span class="sxs-lookup"><span data-stu-id="8f17f-636">This value comes from the **Thermal State** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8f17f-637">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="8f17f-637">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f17f-638">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="8f17f-638">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span data-ttu-id="8f17f-639">**Safe** (3) </span><span class="sxs-lookup"><span data-stu-id="8f17f-639">**Safe** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="8f17f-640">**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="8f17f-640">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="8f17f-641">**重大** (5) </span><span class="sxs-lookup"><span data-stu-id="8f17f-641">**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

<span data-ttu-id="8f17f-642">**無法復原的** (6) </span><span class="sxs-lookup"><span data-stu-id="8f17f-642">**Non-recoverable** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f17f-643">**TotalPhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="8f17f-643">**TotalPhysicalMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-644">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="8f17f-644">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-645">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-645">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-646">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Memory Management 結構 \| [**MEMORYSTATUS**](/windows/desktop/api/winbase/ns-winbase-memorystatus) \| dwTotalPhys" ) ，[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-646">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Memory Management Structures\|[**MEMORYSTATUS**](/windows/desktop/api/winbase/ns-winbase-memorystatus)\|dwTotalPhys"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-647">實體記憶體的總大小。</span><span class="sxs-lookup"><span data-stu-id="8f17f-647">Total size of physical memory.</span></span> <span data-ttu-id="8f17f-648">請注意，在某些情況下，此屬性可能不會傳回實際記憶體的精確值。</span><span class="sxs-lookup"><span data-stu-id="8f17f-648">Be aware that, under some circumstances, this property may not return an accurate value for the physical memory.</span></span> <span data-ttu-id="8f17f-649">例如，如果 BIOS 使用部分實體記憶體，則不正確。</span><span class="sxs-lookup"><span data-stu-id="8f17f-649">For example, it is not accurate if the BIOS is using some of the physical memory.</span></span> <span data-ttu-id="8f17f-650">若要取得精確的值，請改用 [**Win32 \_ PhysicalMemory**](win32-physicalmemory.md)中的 **容量** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8f17f-650">For an accurate value, use the **Capacity** property in [**Win32\_PhysicalMemory**](win32-physicalmemory.md) instead.</span></span>

<span data-ttu-id="8f17f-651">範例：67108864</span><span class="sxs-lookup"><span data-stu-id="8f17f-651">Example: 67108864</span></span>

<span data-ttu-id="8f17f-652">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="8f17f-652">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-653">**使用者名稱**</span><span class="sxs-lookup"><span data-stu-id="8f17f-653">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-654">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f17f-654">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-655">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-655">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-656">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| 系統資訊函數 \| [**GetUserName**](/windows/desktop/api/winbase/nf-winbase-getusernamea)" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-656">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Information Functions\|[**GetUserName**](/windows/desktop/api/winbase/nf-winbase-getusernamea)")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-657">目前登入的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="8f17f-657">Name of a user that is logged on currently.</span></span> <span data-ttu-id="8f17f-658">這個屬性必須有值。</span><span class="sxs-lookup"><span data-stu-id="8f17f-658">This property must have a value.</span></span> <span data-ttu-id="8f17f-659">在終端機服務會話中 **，使用者** 名稱會傳回登入主控台的使用者名稱，而不是使用者在終端機服務會話期間登入的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="8f17f-659">In a terminal services session, **UserName** returns the name of the user that is logged on to the console not the user logged on during the terminal service session.</span></span>

<span data-ttu-id="8f17f-660">範例： jeffsmith</span><span class="sxs-lookup"><span data-stu-id="8f17f-660">Example: jeffsmith</span></span>

</dd> <dt>

<span data-ttu-id="8f17f-661">**WakeUpType**</span><span class="sxs-lookup"><span data-stu-id="8f17f-661">**WakeUpType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-662">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8f17f-662">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-663">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f17f-663">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-664">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| type 1 \| 系統資訊 \| 喚醒類型" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-664">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Wake-up Type")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-665">導致系統開機的事件。</span><span class="sxs-lookup"><span data-stu-id="8f17f-665">Event that causes the system to power up.</span></span>

<span data-ttu-id="8f17f-666">此值來自 SMBIOS 資訊中 **系統資訊** 結構的 **喚醒類型** 成員。</span><span class="sxs-lookup"><span data-stu-id="8f17f-666">This value comes from the **Wake-up Type** member of the **System Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="8f17f-667">**保留** (0) </span><span class="sxs-lookup"><span data-stu-id="8f17f-667">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8f17f-668">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="8f17f-668">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f17f-669">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="8f17f-669">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="APM_Timer"></span><span id="apm_timer"></span><span id="APM_TIMER"></span>

<span data-ttu-id="8f17f-670">**APM 計時器** (3) </span><span class="sxs-lookup"><span data-stu-id="8f17f-670">**APM Timer** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Modem_Ring"></span><span id="modem_ring"></span><span id="MODEM_RING"></span>

<span data-ttu-id="8f17f-671">**數據機響鈴** (4) </span><span class="sxs-lookup"><span data-stu-id="8f17f-671">**Modem Ring** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="LAN_Remote"></span><span id="lan_remote"></span><span id="LAN_REMOTE"></span>

<span data-ttu-id="8f17f-672">**區域網路遠端** (5) </span><span class="sxs-lookup"><span data-stu-id="8f17f-672">**LAN Remote** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Switch"></span><span id="power_switch"></span><span id="POWER_SWITCH"></span>

<span data-ttu-id="8f17f-673">**電源開關** (6) </span><span class="sxs-lookup"><span data-stu-id="8f17f-673">**Power Switch** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_PME_"></span><span id="pci_pme_"></span>

<span data-ttu-id="8f17f-674">**PCI PME \#** (7) </span><span class="sxs-lookup"><span data-stu-id="8f17f-674">**PCI PME\#** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="AC_Power_Restored"></span><span id="ac_power_restored"></span><span id="AC_POWER_RESTORED"></span>

<span data-ttu-id="8f17f-675">**AC 電源已還原** (8) </span><span class="sxs-lookup"><span data-stu-id="8f17f-675">**AC Power Restored** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f17f-676">**工作群組**</span><span class="sxs-lookup"><span data-stu-id="8f17f-676">**Workgroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f17f-677">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f17f-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-678">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8f17f-678">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8f17f-679">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "" ) </span><span class="sxs-lookup"><span data-stu-id="8f17f-679">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="8f17f-680">此電腦的工作組名稱。</span><span class="sxs-lookup"><span data-stu-id="8f17f-680">Name of the workgroup for this computer.</span></span> <span data-ttu-id="8f17f-681">如果 **PartOfDomain** 屬性的值為 **False**，則會傳回工作組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f17f-681">If the value of the **PartOfDomain** property is **False**, then the name of the workgroup is returned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f17f-682">備註</span><span class="sxs-lookup"><span data-stu-id="8f17f-682">Remarks</span></span>

<span data-ttu-id="8f17f-683">若要判斷與電腦系統物件相關聯的處理器實例總數，請使用 [**Win32 \_ ComputerSystemProcessor**](win32-computersystemprocessor.md) association 類別。</span><span class="sxs-lookup"><span data-stu-id="8f17f-683">To determine the total number of processor instances associated with a computer system object, use the [**Win32\_ComputerSystemProcessor**](win32-computersystemprocessor.md) association class.</span></span>

<span data-ttu-id="8f17f-684">具有多個實體處理器的 Win32 實例實例具有多個與它相關聯的 [**win32 \_ 處理器**](win32-processor.md)實例。 **\_**</span><span class="sxs-lookup"><span data-stu-id="8f17f-684">A **Win32\_ComputerSystem** instance that has multiple physical processors has multiple [**Win32\_Processor**](win32-processor.md) instances associated with it.</span></span> <span data-ttu-id="8f17f-685">如果 **NumberOfLogicalProcessors** 的值大於 **NumberOfProcessors** 的值，則電腦系統可能是多核心系統，或有一或多個處理器已啟用超執行緒。</span><span class="sxs-lookup"><span data-stu-id="8f17f-685">If the value of **NumberOfLogicalProcessors** is greater than the value of **NumberOfProcessors** then the computer system is either a multicore system or has one or more processors enabled for hyperthreading.</span></span> <span data-ttu-id="8f17f-686">如需詳細資訊，請參閱 **Win32 \_ 處理器** 中的 **NumberOfLogicalProcessors** 和 **NumberOfCores** 屬性和備註一節。</span><span class="sxs-lookup"><span data-stu-id="8f17f-686">For more information, see the **NumberOfLogicalProcessors** and **NumberOfCores** properties and Remarks section in **Win32\_Processor**.</span></span>

<span data-ttu-id="8f17f-687">Win32 [**\_ UnitaryComputerSystem**](cim-unitarycomputersystem.md)類別衍生自 CIM。 **\_**</span><span class="sxs-lookup"><span data-stu-id="8f17f-687">The **Win32\_ComputerSystem** class is derived from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8f17f-688">範例</span><span class="sxs-lookup"><span data-stu-id="8f17f-688">Examples</span></span>

<span data-ttu-id="8f17f-689">下列的腳本中心程式 [代碼範例](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Display-computers-status-c8ff289d)會使用 Win32 程式碼，從許多電腦系統中取出資訊，並將它們顯示在 GUI 中。 **\_**</span><span class="sxs-lookup"><span data-stu-id="8f17f-689">The following Scripting Center [code example](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Display-computers-status-c8ff289d) uses the **Win32\_ComputerSystem** to retrieve information from a number of computer systems, and display them in a GUI.</span></span>

<span data-ttu-id="8f17f-690">您可以在 [**win32 \_ 處理器**](win32-processor.md)主題範例中，找到從 **win32 \_** 程式碼、 [**win32 \_ 處理器**](win32-processor.md)和 win32 作業系統取得 [**作業系統 \_**](win32-operatingsystem.md)和處理器資料的範例腳本。</span><span class="sxs-lookup"><span data-stu-id="8f17f-690">You can find an example script that obtains operating system and processor data from **Win32\_ComputerSystem**, [**Win32\_Processor**](win32-processor.md), and [**Win32\_OperatingSystem**](win32-operatingsystem.md) in the [**Win32\_Processor**](win32-processor.md) topic examples.</span></span>

<span data-ttu-id="8f17f-691">下列 VBScript 範例說明如何從 **Win32 \_** 執行程式實例中取出本機電腦的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="8f17f-691">The following VBScript sample describes how to retrieve the domain name of the local machine from instances of **Win32\_ComputerSystem**.</span></span>


```VB
Set SystemSet = GetObject("winmgmts:").InstancesOf ("Win32_ComputerSystem")

for each System in SystemSet
 WScript.Echo System.Domain
next
```



<span data-ttu-id="8f17f-692">下列 Perl 範例說明如何從 **Win32 \_** 執行程式實例中取出本機電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="8f17f-692">The following Perl sample describes how to retrieve the local machine name from instances of **Win32\_ComputerSystem**.</span></span>


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



<span data-ttu-id="8f17f-693">下列 Perl 範例說明如何從 **Win32 \_** 執行程式實例中取出本機電腦的 DNS 功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="8f17f-693">The following Perl sample describes how to retrieve the DNS domain name of the local machine from instances of **Win32\_ComputerSystem**.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="8f17f-694">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f17f-694">Requirements</span></span>



| <span data-ttu-id="8f17f-695">需求</span><span class="sxs-lookup"><span data-stu-id="8f17f-695">Requirement</span></span> | <span data-ttu-id="8f17f-696">值</span><span class="sxs-lookup"><span data-stu-id="8f17f-696">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f17f-697">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8f17f-697">Minimum supported client</span></span><br/> | <span data-ttu-id="8f17f-698">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f17f-698">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8f17f-699">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8f17f-699">Minimum supported server</span></span><br/> | <span data-ttu-id="8f17f-700">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f17f-700">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f17f-701">命名空間</span><span class="sxs-lookup"><span data-stu-id="8f17f-701">Namespace</span></span><br/>                | <span data-ttu-id="8f17f-702">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8f17f-702">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8f17f-703">MOF</span><span class="sxs-lookup"><span data-stu-id="8f17f-703">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f17f-704"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f17f-704"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f17f-705">DLL</span><span class="sxs-lookup"><span data-stu-id="8f17f-705">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f17f-706"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f17f-706"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f17f-707">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f17f-707">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f17f-708">**CIM \_ UnitaryComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="8f17f-708">**CIM\_UnitaryComputerSystem**</span></span>](cim-unitarycomputersystem.md)
</dt> <dt>

<span data-ttu-id="8f17f-709">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8f17f-709">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8f17f-710">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="8f17f-710">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="8f17f-711">WMI 工作：電腦硬體</span><span class="sxs-lookup"><span data-stu-id="8f17f-711">WMI Tasks: Computer Hardware</span></span>](/windows/desktop/WmiSdk/wmi-tasks--computer-hardware)
</dt> <dt>

[<span data-ttu-id="8f17f-712">WMI 工作：桌面管理</span><span class="sxs-lookup"><span data-stu-id="8f17f-712">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

