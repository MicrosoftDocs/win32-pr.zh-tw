---
description: 表示在執行 Windows 的電腦系統上，視訊控制器的功能和管理能力。
ms.assetid: 5c81994b-4a84-46ff-8689-09998dc66f91
ms.tgt_platform: multiple
title: Win32_VideoController 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoController
- Win32_VideoController.Reset
- Win32_VideoController.SetPowerState
- Win32_VideoController.AcceleratorCapabilities
- Win32_VideoController.AdapterCompatibility
- Win32_VideoController.AdapterDACType
- Win32_VideoController.AdapterRAM
- Win32_VideoController.Availability
- Win32_VideoController.CapabilityDescriptions
- Win32_VideoController.Caption
- Win32_VideoController.ColorTableEntries
- Win32_VideoController.ConfigManagerErrorCode
- Win32_VideoController.ConfigManagerUserConfig
- Win32_VideoController.CreationClassName
- Win32_VideoController.CurrentBitsPerPixel
- Win32_VideoController.CurrentHorizontalResolution
- Win32_VideoController.CurrentNumberOfColors
- Win32_VideoController.CurrentNumberOfColumns
- Win32_VideoController.CurrentNumberOfRows
- Win32_VideoController.CurrentRefreshRate
- Win32_VideoController.CurrentScanMode
- Win32_VideoController.CurrentVerticalResolution
- Win32_VideoController.Description
- Win32_VideoController.DeviceID
- Win32_VideoController.DeviceSpecificPens
- Win32_VideoController.DitherType
- Win32_VideoController.DriverDate
- Win32_VideoController.DriverVersion
- Win32_VideoController.ErrorCleared
- Win32_VideoController.ErrorDescription
- Win32_VideoController.ICMIntent
- Win32_VideoController.ICMMethod
- Win32_VideoController.InfFilename
- Win32_VideoController.InfSection
- Win32_VideoController.InstallDate
- Win32_VideoController.InstalledDisplayDrivers
- Win32_VideoController.LastErrorCode
- Win32_VideoController.MaxMemorySupported
- Win32_VideoController.MaxNumberControlled
- Win32_VideoController.MaxRefreshRate
- Win32_VideoController.MinRefreshRate
- Win32_VideoController.Monochrome
- Win32_VideoController.Name
- Win32_VideoController.NumberOfColorPlanes
- Win32_VideoController.NumberOfVideoPages
- Win32_VideoController.PNPDeviceID
- Win32_VideoController.PowerManagementCapabilities
- Win32_VideoController.PowerManagementSupported
- Win32_VideoController.ProtocolSupported
- Win32_VideoController.ReservedSystemPaletteEntries
- Win32_VideoController.SpecificationVersion
- Win32_VideoController.Status
- Win32_VideoController.StatusInfo
- Win32_VideoController.SystemCreationClassName
- Win32_VideoController.SystemName
- Win32_VideoController.SystemPaletteEntries
- Win32_VideoController.TimeOfLastReset
- Win32_VideoController.VideoArchitecture
- Win32_VideoController.VideoMemoryType
- Win32_VideoController.VideoMode
- Win32_VideoController.VideoModeDescription
- Win32_VideoController.VideoProcessor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: deb6903ba6cf27170539281da90569a14471999c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104467972"
---
# <a name="win32_videocontroller-class"></a>Win32 \_ VideoController 類別

**Win32 \_ VideoController** [WMI 類別](../wmisdk/retrieving-a-class.md)代表在執行 Windows 的電腦系統上，影片控制器的功能和管理能力。

與 Windows 顯示驅動程式模型不相容的硬體 (WDDM) 會傳回這個類別之實例的不正確屬性值。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCF1-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class Win32_VideoController : CIM_PCVideoController
{
  uint16   AcceleratorCapabilities[];
  string   AdapterCompatibility;
  string   AdapterDACType;
  uint32   AdapterRAM;
  uint16   Availability;
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ColorTableEntries;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint32   CurrentBitsPerPixel;
  uint32   CurrentHorizontalResolution;
  uint64   CurrentNumberOfColors;
  uint32   CurrentNumberOfColumns;
  uint32   CurrentNumberOfRows;
  uint32   CurrentRefreshRate;
  uint16   CurrentScanMode;
  uint32   CurrentVerticalResolution;
  string   Description;
  string   DeviceID;
  uint32   DeviceSpecificPens;
  uint32   DitherType;
  datetime DriverDate;
  string   DriverVersion;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   ICMIntent;
  uint32   ICMMethod;
  string   InfFilename;
  string   InfSection;
  datetime InstallDate;
  string   InstalledDisplayDrivers;
  uint32   LastErrorCode;
  uint32   MaxMemorySupported;
  uint32   MaxNumberControlled;
  uint32   MaxRefreshRate;
  uint32   MinRefreshRate;
  boolean  Monochrome;
  string   Name;
  uint16   NumberOfColorPlanes;
  uint32   NumberOfVideoPages;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  uint32   ReservedSystemPaletteEntries;
  uint32   SpecificationVersion;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   SystemPaletteEntries;
  datetime TimeOfLastReset;
  uint16   VideoArchitecture;
  uint16   VideoMemoryType;
  uint16   VideoMode;
  string   VideoModeDescription;
  string   VideoProcessor;
};
```

## <a name="members"></a>成員

**Win32 \_ VideoController** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ VideoController** 類別具有這些方法。



| 方法            | 描述                                                                                                                                                                                            |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **重設**         | 未實作。 若要執行此方法，請參閱 [**CIM \_ PCVideoController**](cim-pcvideocontroller.md)中的 [**Reset**](reset-method-in-class-cim-controller.md)方法。<br/>                 |
| **SetPowerState** | 未實作。 若要執行此方法，請參閱 [**CIM \_ PCVideoController**](cim-pcvideocontroller.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法。<br/> |



 

### <a name="properties"></a>屬性

**Win32 \_ VideoController** 類別具有這些屬性。

<dl> <dt>

**AcceleratorCapabilities**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "[**CIM \_ VideoController**](cim-videocontroller.md).**CapabilityDescriptions**") 
</dt> </dl>

影片控制器的圖形陣列和立體功能。

這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**圖形加速器** (2) 


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**3D 加速器** (3) 


</dt> <dd>

3-d 加速器

</dd> </dl>

</dd> <dt>

**AdapterCompatibility**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry" ) 
</dt> </dl>

此控制器使用的一般晶片來比較與系統之間的相容性。

</dd> <dt>

**AdapterDACType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| HardwareInformation. DACType" ) 
</dt> </dl>

數位轉類比轉換器 (DAC) 晶片的名稱或識別碼。 這個屬性的字元集是英數位元。

</dd> <dt>

**AdapterRAM**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| HardwareInformation. MemorySize" ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) 
</dt> </dl>

視訊卡的記憶體大小。

範例：64000

</dd> <dt>

**可用性**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") 
</dt> </dl>

裝置的可用性和狀態。

這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) 


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) 


</dt> <dd>

執行中或完整電源

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) 


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) 


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) 


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) 


</dt> <dd>

離線

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) 


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) 


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) 


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) 


</dt> <dd>

裝置已知處於省電模式，但其確切狀態不明。

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) 


</dt> <dd>

裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) 


</dt> <dd>

裝置無法正常運作，但可快速進入完整電源。

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) 


</dt> <dd>

裝置處於警告狀態，但也處於省電模式。

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) 


</dt> <dd>

裝置已暫停。

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) 


</dt> <dd>

裝置未就緒。

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) 


</dt> <dd>

裝置未設定。

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) 


</dt> <dd>

裝置為靜音。

</dd> </dl>

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](../wmisdk/standard-qualifiers.md) ( "Indexed" ) ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "[**CIM \_ VideoController**](cim-videocontroller.md)。**AcceleratorCapabilities**") 
</dt> </dl>

自由格式字串提供 **AcceleratorCapabilities** 陣列中所指出之任何影片加速器功能的詳細說明。 請注意，這個陣列的每個專案都與 **AcceleratorCapabilities** 陣列中位於相同索引的專案有關。

這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) 
</dt> </dl>

物件的簡短描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**ColorTableEntries**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)" ) 
</dt> </dl>

系統色彩表的大小。 裝置的色彩深度必須為每圖元不超過8個位;否則，就不會設定這個屬性。

範例：256

</dd> <dt>

**ConfigManagerErrorCode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) 
</dt> </dl>

Win32 設定管理員錯誤碼。

這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**  (0)


</dt> <dd>

裝置運作正常。

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。** (1)


</dt> <dd>

裝置未正確設定。

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。** (2)


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。** (3)


</dt> <dd>

此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。** (4)


</dt> <dd>

裝置無法正常運作。 其中一個驅動程式或登錄可能已損毀。

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。** (5)


</dt> <dd>

裝置的驅動程式需要 Windows 無法管理的資源。

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。** (6)


</dt> <dd>

裝置的開機設定與其他裝置發生衝突。

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。** (7)


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。** (8)


</dt> <dd>

遺漏裝置的驅動程式載入器。

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。** (9)


</dt> <dd>

裝置無法正常運作。 控制的固件未正確報告裝置的資源。

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。** (10)


</dt> <dd>

裝置無法啟動。

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。** (11)


</dt> <dd>

裝置失敗。

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**  (12) 


</dt> <dd>

裝置找不到足夠的可用資源。

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。** (13)


</dt> <dd>

Windows 無法驗證裝置的資源。

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。** (14)


</dt> <dd>

裝置在重新開機電腦之前無法正常運作。

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。** (15)


</dt> <dd>

裝置因可能的重新列舉問題而無法正常運作。

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。** (16)


</dt> <dd>

Windows 無法識別裝置使用的所有資源。

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。** (17)


</dt> <dd>

裝置正在要求未知的資源類型。

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。** (18)


</dt> <dd>

必須重新安裝設備磁碟機。

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。** (19)


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。** (20)


</dt> <dd>

登錄可能已損毀。

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。** (21)


</dt> <dd>

系統失敗。 如果變更設備磁碟機是不正確，請參閱硬體檔。 Windows 正在移除裝置。

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。** (22)


</dt> <dd>

裝置已停用。

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。** (23)


</dt> <dd>

系統失敗。 如果變更設備磁碟機是不正確，請參閱硬體檔。

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。** (24)


</dt> <dd>

裝置不存在、無法正常運作，或未安裝所有的驅動程式。

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。** (25)


</dt> <dd>

Windows 仍在設定裝置。

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。** (26)


</dt> <dd>

Windows 仍在設定裝置。

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。** (27)


</dt> <dd>

裝置沒有有效的記錄檔設定。

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。** (28)


</dt> <dd>

未安裝設備磁碟機。

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。** (29)


</dt> <dd>

裝置已停用。 裝置固件未提供所需的資源。

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。** (30)


</dt> <dd>

裝置正在使用其他裝置正在使用的 IRQ 資源。

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**  (31) 


</dt> <dd>

裝置無法正常運作。 Windows 無法載入所需的設備磁碟機。

</dd> </dl>

</dd> <dt>

**ConfigManagerUserConfig**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) 
</dt> </dl>

若 **為 TRUE**，則裝置會使用使用者定義的設定。

這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [ **CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。 搭配類別的其他索引鍵屬性使用時，此屬性可讓這個類別和其子類別的所有實例都能唯一識別。

這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

</dd> <dt>

**CurrentBitsPerPixel**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| Video \| 003.12 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" bits ") 
</dt> </dl>

用來顯示每個圖元的位數。

這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。

</dd> <dt>

**CurrentHorizontalResolution**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| Video \| 003.11 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" 圖元 ") 
</dt> </dl>

目前的水準圖元數目。

這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。

</dd> <dt>

**CurrentNumberOfColors**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目前解析度所支援的色彩數目。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。

這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。

</dd> <dt>

**CurrentNumberOfColumns**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| Video \| 003.14 ") 
</dt> </dl>

此影片控制器 (的資料行數目（以字元模式) ）。 否則，請輸入 0 (零) 。

這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。

</dd> <dt>

**CurrentNumberOfRows**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| Video \| 003.13 ") 
</dt> </dl>

此影片控制器 (的資料列數目（以字元模式) ）。 否則，請輸入 0 (零) 。

這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。

</dd> <dt>

**CurrentRefreshRate**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "CurrentRefreshRate" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| HardwareInformation"。) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "赫茲" ) 
</dt> </dl>

影片控制器重新整理監視器影像的頻率。 值為 0 (零) 表示正在使用預設速率，而0xFFFFFFFF 表示使用的是最佳的速率。

這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。

</dd> <dt>

**CurrentScanMode**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| Video \| 003.8 ") 
</dt> </dl>

目前的掃描模式。

這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) 


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>**交錯** 式 (3) 


</dt> <dd></dd> <dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**非交錯** 式 (4) 


</dt> <dd>

Noninterlaced

</dd> </dl>

</dd> <dt>

**CurrentVerticalResolution**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| Video \| 003.10 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" 圖元 ") 
</dt> </dl>

目前的垂直圖元數目。

這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) 
</dt> </dl>

物件的描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "DeviceId" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) 
</dt> </dl>

此影片控制器的電腦系統) 的唯一 (識別碼。

這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

</dd> <dt>

**DeviceSpecificPens**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)" ) 
</dt> </dl>

裝置特定畫筆的目前數目。 值0xffff 表示裝置不支援畫筆。

範例：3

</dd> <dt>

**DitherType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| EnumDisplaySettings" ) 
</dt> </dl>

影片控制器的遞色類型。 屬性可以是其中一個預先定義的值，或是大於或等於256的驅動程式定義值。 如果選擇了線條藝術遞色，控制器會使用遞色方法，在黑色、白色和灰色 scalings 之間產生定義完善的框線。 線條藝術遞色不適合包含濃度和色調（如掃描的相片）中連續 graduations 的影像。

<dt>

<span id="No_dithering"></span><span id="no_dithering"></span><span id="NO_DITHERING"></span>

**沒有遞色** (1) 


</dt> <dd></dd> <dt>

<span id="Dithering_with_a_coarse_brush"></span><span id="dithering_with_a_coarse_brush"></span><span id="DITHERING_WITH_A_COARSE_BRUSH"></span>

**使用粗略筆刷** (2) 遞色


</dt> <dd></dd> <dt>

<span id="Dithering_with_a_fine_brush"></span><span id="dithering_with_a_fine_brush"></span><span id="DITHERING_WITH_A_FINE_BRUSH"></span>

**使用微調筆刷** (3) 遞色


</dt> <dd></dd> <dt>

<span id="Line_art_dithering"></span><span id="line_art_dithering"></span><span id="LINE_ART_DITHERING"></span>

第 **藝術色** (4) 


</dt> <dd></dd> <dt>

<span id="Device_does_gray_scaling"></span><span id="device_does_gray_scaling"></span><span id="DEVICE_DOES_GRAY_SCALING"></span>

**裝置會以灰色縮放** (5) 


</dt> <dd></dd> </dl>

</dd> <dt>

**DriverDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ " ) 
</dt> </dl>

目前已安裝之視頻驅動程式的上次修改日期和時間。

</dd> <dt>

**DriverVersion**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| File 安裝程式庫函數 \| GetFileVersionInfo" ) 
</dt> </dl>

影片驅動程式的版本號碼。

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。

這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

自由格式的字串提供 **LastErrorCode** 屬性中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。

這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

</dd> <dt>

**ICMIntent**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 列印和列印多工緩衝處理器結構 \| DevMode \| dmICMIntent」 ) 
</dt> </dl>

預設應使用的三種可能色彩比對方法或意圖之一的特定值。 這個屬性主要用於非 ICM 應用程式。 ICM 應用程式使用 ICM 函數來建立意圖。 這個屬性可以是預先定義的值，或是大於或等於256的驅動程式定義值。 當不需要遞色時，根據飽和度的色彩比對是最適合的商務圖形選擇。 以對比為依據的色彩比對，在需要遞色時，是掃描或攝影影像最適合的選擇。 針對符合所要求的確切色彩進行優化的色彩比對，最適合在需要完全相符的色彩時，與商務標誌或其他影像一起使用。

<dt>

<span id="Saturation"></span><span id="saturation"></span><span id="SATURATION"></span>

**飽和度** (1) 


</dt> <dd></dd> <dt>

<span id="Contrast"></span><span id="contrast"></span><span id="CONTRAST"></span>

**對比** (2) 


</dt> <dd></dd> <dt>

<span id="Exact_Color"></span><span id="exact_color"></span><span id="EXACT_COLOR"></span>

**確切色彩** (3) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ICMMethod**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 列印和列印多工緩衝處理器結構 \| DevMode \| dmICMMethod」 ) 
</dt> </dl>

處理 ICM 的方法。 若為非 ICM 應用程式，此屬性會判斷是否已啟用 ICM。 針對 ICM 應用程式，系統會檢查這個屬性，以判斷如何處理 ICM 支援。 這個屬性可以是預先定義的值，或是大於或等於256的驅動程式定義值。 此值會決定處理影像色彩比對的系統。

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**停用** (1) 


</dt> <dd></dd> <dt>

<span id="Windows"></span><span id="windows"></span><span id="WINDOWS"></span>

**Windows** (2) 


</dt> <dd></dd> <dt>

<span id="Device_Driver"></span><span id="device_driver"></span><span id="DEVICE_DRIVER"></span>

**設備磁碟機** (3) 


</dt> <dd></dd> <dt>

<span id="Destination_Device"></span><span id="destination_device"></span><span id="DESTINATION_DEVICE"></span>

**目的地裝置** (4) 


</dt> <dd></dd> </dl>

</dd> <dt>

**InfFilename**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E968-E325-11CE-BFC1-08002BE10318} \\ \\ 0000" ) 
</dt> </dl>

視訊卡 .inf 檔案的路徑。

範例： "C： \\ Windows \\ SYSTEM32 \\ 驅動程式"

</dd> <dt>

**InfSection**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E968-E325-11CE-BFC1-08002BE10318} \\ \\ 0000" ) 
</dt> </dl>

Windows 影片資訊所在 .inf 檔案的區段。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") 
</dt> </dl>

物件的安裝日期和時間。 這個屬性不需要值來表示已安裝物件。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**InstalledDisplayDrivers**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ " ) 
</dt> </dl>

已安裝顯示裝置磁碟機的名稱。

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

邏輯裝置所報告的最後一個錯誤碼。

這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

</dd> <dt>

**MaxMemorySupported**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) 
</dt> </dl>

支援的最大記憶體數量（以位元組為單位）。

這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。

</dd> <dt>

**MaxNumberControlled**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 匯流排埠 \| 001.9 ") 
</dt> </dl>

此控制器可支援的直接可定址實體數目上限。 值為 0 (零) 如果數位未知，則應使用此值。

這個屬性繼承自 [**CIM \_ 控制器**](cim-controller.md)。

</dd> <dt>

**MaxRefreshRate**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| Video \| 003.5 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" 赫茲 ") 
</dt> </dl>

影片控制器的最大重新整理速率（以赫茲為單位）。

這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。

</dd> <dt>

**MinRefreshRate**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| Video \| 003.4 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" 赫茲 ") 
</dt> </dl>

影片控制器的最小更新速率（以赫茲為單位）。

這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。

</dd> <dt>

**單色**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) 
</dt> </dl>

若 **為 TRUE**，則會使用灰色縮放來顯示影像。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) 
</dt> </dl>

已知物件的標籤。 子類別化時，可以將屬性覆寫為索引鍵屬性。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**NumberOfColorPlanes**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目前的色彩平面數目。 如果此值不適用於目前的影片設定，請輸入 0 (零) 。

這個屬性繼承自 [**CIM \_ PCVideoController**](cim-pcvideocontroller.md)。

</dd> <dt>

**NumberOfVideoPages**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提供目前的解析度和可用記憶體所支援的影片頁面數目。

這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) 
</dt> </dl>

Windows 隨插即用邏輯裝置的裝置識別碼。

範例： " \* PNP030b"

這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

邏輯裝置的特定電源相關功能陣列。

這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

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

支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。 這個方法可在父 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 類別上找到，並且可以實作為。 如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](../wmisdk/designing-managed-object-format--mof--classes.md)。

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

若 **為 TRUE**，則裝置可以是電源管理 (可進入暫停模式，依此類推) 。 屬性不表示電源管理功能目前已啟用，只有邏輯裝置能夠進行電源管理。

這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

</dd> <dt>

**ProtocolSupported**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 匯流排埠 \| 001.2 "，" MIF。DMTF \| 磁片 \| 003.3 ") 
</dt> </dl>

控制器用來存取「受控制」裝置的通訊協定。

這個屬性繼承自 [**CIM \_ 控制器**](cim-controller.md)。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) 


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span id="EISA"></span><span id="eisa"></span>**EISA** (3) 


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span id="ISA"></span><span id="isa"></span>**ISA** (4) 


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span id="PCI"></span><span id="pci"></span>**PCI** (5) 


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6) 


</dt> <dd>

ATA 或 ATAPI

</dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**彈性磁片** (7) 


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span id="1496"></span>**1496** (8) 


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**SCSI 平行介面** (9) 


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**SCSI 光纖通道通訊協定** (10) 


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**SCSI 序列匯流排通訊協定** (11) 


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**SCSI 序列匯流排通訊協定-2 (1394)** (12) 


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**SCSI 序列儲存架構** (13) 


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span id="VESA"></span><span id="vesa"></span>**VESA** (14) 


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15) 


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**通用序列匯流排** (16) 


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**平行通訊協定** (17) 


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span id="ESCON"></span><span id="escon"></span>**ESCON** (18) 


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**診斷** (19) 


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span id="I2C"></span><span id="i2c"></span>**I2C** (20) 


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (21) 


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22) 


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**MultiBus** (23) 


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span id="VME"></span><span id="vme"></span>**Vm** (24) 


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span id="IPI"></span><span id="ipi"></span>**IPI** (25) 


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26) 


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span id="RS232"></span><span id="rs232"></span>**RS232** (27) 


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span id="ieee_802.3_10base5"></span>**IEEE 802.3 10BASE5** (28) 


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span id="ieee_802.3_10base2"></span>**IEEE 802.3 10BASE2** (29) 


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span id="ieee_802.3_1base5"></span>**IEEE 802.3 1BASE5** (30) 


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span id="ieee_802.3_10broad36"></span>**IEEE 802.3 10BROAD36** (31) 


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span id="ieee_802.3_100basevg"></span>**IEEE 802.3 100BASEVG** (32) 


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**IEEE 802.5 權杖-環形** (33) 


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span id="ansi_x3t9.5_fddi"></span>**ANSI x3t 9.5 FDDI** (34) 


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span id="MCA"></span><span id="mca"></span>**MCA** (35) 


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span id="ESDI"></span><span id="esdi"></span>**ESDI** (36) 


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span id="IDE"></span><span id="ide"></span>**IDE** (37) 


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span id="CMD"></span><span id="cmd"></span>**CMD** (38) 


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span id="ST506"></span><span id="st506"></span>**ST506** (39) 


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span id="DSSI"></span><span id="dssi"></span>**」 Dssi 小組** (40) 


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span id="QIC2"></span><span id="qic2"></span>**QIC2** (41) 


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**增強型 ATA/IDE** (42) 


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span id="AGP"></span><span id="agp"></span>**AGP** (43) 


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (雙向紅外線)** (44) 


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**(快速紅外線)** (45) 的杉樹


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**SIR (串列紅外線)** (46) 


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**IrBus** (47) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ReservedSystemPaletteEntries**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)" ) 
</dt> </dl>

系統調色板中的保留專案數目。 作業系統可能會保留專案，以支援工作列和其他桌面顯示專案的標準色彩。 只有當設備磁碟機在 RASTERCAPS 索引中設定 RC 選擇 **區 \_** 位時，此索引才有效，而且只有在驅動程式與16位 Windows 相容時才可使用。 如果系統未使用調色板，則不會設定 **ReservedSystemPaletteEntries** 。

範例：20

</dd> <dt>

**SpecificationVersion**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 列印和列印多工緩衝處理器結構 \| DevMode \| dmSpecVersion」 ) 
</dt> </dl>

結構以) 為基礎 (初始化資料規格的版本號碼。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) 
</dt> </dl>

物件的目前狀態。 您可以定義各種操作和 nonoperational 狀態。 作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。 Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。 後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。 並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

包括下列值：

<dt>

<span id="OK"></span><span id="ok"></span>

**確定** ( [確定] ) 


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**錯誤** ( 「錯誤」 ) 


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**降級** ( 「降級」 ) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 ( 「未知」 ) 


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred 失敗** ( 「Pred 失敗」 ) 


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**開始** ( 「開始」 ) 


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**停止** ( 「正在停止」 ) 


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**服務** ( 「服務」 ) 


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**壓力** ( 「壓力」 ) 


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ( "NonRecover" ) 


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**沒有連絡人** ( 「沒有連絡人」 ) 


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**遺失的 comm** ( 「遺失的通訊」 ) 


</dt> <dd></dd> </dl>

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") 
</dt> </dl>

邏輯裝置的狀態。 如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。

這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (2) 


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**已啟用** (3) 


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**已停用** (4) 


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**不適用** (5) 


</dt> <dd></dd> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

範圍電腦之 **CreationClassName** 屬性的值。

這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

範圍系統的名稱。

這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

</dd> <dt>

**SystemPaletteEntries**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)" ) 
</dt> </dl>

系統調色板中目前的色彩索引項目數目。 只有當設備磁碟機在 RASTERCAPS 索引中設定 RC 選擇 **區 \_** 位時，此索引才有效，而且只有在驅動程式與16位 Windows 相容時才可使用。 如果系統未使用調色板，則不會設定 **SystemPaletteEntries** 。

範例：20

</dd> <dt>

**TimeOfLastReset**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

上次重設此控制器的日期和時間。 這可能表示控制器已關機或重新初始化。

這個屬性繼承自 [**CIM \_ 控制器**](cim-controller.md)。

</dd> <dt>

**VideoArchitecture**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| Video \| 003.2 ") 
</dt> </dl>

影片架構的類型。

這個屬性繼承自 [**CIM \_ PCVideoController**](cim-pcvideocontroller.md)。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (2) 


</dt> <dd></dd> <dt>

<span id="CGA"></span><span id="cga"></span>

 (3) 的 **CGA**


</dt> <dd></dd> <dt>

<span id="EGA"></span><span id="ega"></span>

**EGA** (4) 


</dt> <dd></dd> <dt>

<span id="VGA"></span><span id="vga"></span>

**VGA** (5) 


</dt> <dd></dd> <dt>

<span id="SVGA"></span><span id="svga"></span>

**SVGA** (6) 


</dt> <dd></dd> <dt>

<span id="MDA"></span><span id="mda"></span>

**MDA** (7) 


</dt> <dd></dd> <dt>

<span id="HGC"></span><span id="hgc"></span>

**HGC** (8) 


</dt> <dd></dd> <dt>

<span id="MCGA"></span><span id="mcga"></span>

**MCGA** (9) 


</dt> <dd></dd> <dt>

<span id="8514A"></span><span id="8514a"></span>

**8514A** (10) 


</dt> <dd></dd> <dt>

<span id="XGA"></span><span id="xga"></span>

**XGA** (11) 


</dt> <dd></dd> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>

**線性框架緩衝區** (12) 


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

**PC-98** (160) 


</dt> <dd></dd> </dl>

</dd> <dt>

**VideoMemoryType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| Video \| 003.6 ") 
</dt> </dl>

視訊記憶體的類型。

這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (2) 


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

**VRAM** (3) 


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

**DRAM** (4) 


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

**SRAM** (5) 


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

**WRAM** (6) 


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

**EDO RAM** (7) 


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

高載 **同步 DRAM** (8) 


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

**管線** 高載 SRAM (9) 


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

**CDRAM** (10) 


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

**3DRAM** (11) 


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

**SDRAM** (12) 


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

**SGRAM** (13) 


</dt> <dd></dd> </dl>

</dd> <dt>

**VideoMode**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| Video \| 003.3 ") 
</dt> </dl>

目前的影片模式。

這個屬性繼承自 [**CIM \_ PCVideoController**](cim-pcvideocontroller.md)。

</dd> <dt>

**VideoModeDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)" ) 
</dt> </dl>

影片控制器目前的解析度、色彩和掃描模式設定。

範例： "1024 x 768 x 256 色彩"

</dd> <dt>

**VideoProcessor**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述視頻處理器的自由格式字串。

這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ VideoController** 類別衍生自 [**CIM \_ PCVideoController**](cim-pcvideocontroller.md)。

如需使用此類別的詳細資訊，例如從多個監視器抓取資訊，請參閱 [使用 PowerShell 探索多監視器資訊](https://blogs.technet.com/b/heyscriptingguy/archive/2013/10/03/use-powershell-to-discover-multi-monitor-information.aspx)。

## <a name="examples"></a>範例

[列出影片控制器屬性](https://Gallery.TechNet.Microsoft.Com/6c1a585c-742f-4f51-bb57-23838e8f011f)VBScript 範例會列出影片控制器屬性。

下列 PowerShell 範例會列出影片控制器屬性。


```VB
$strComputer = "." 
 
$colItems = get-wmiobject -class "Win32_VideoController" -namespace "root\CIMV2" ` 
-computername $strComputer 
 
foreach ($objItem in $colItems) { 
      write-host "Accelerator Capabilities: " $objItem.AcceleratorCapabilities 
      write-host "Adapter Compatibility: " $objItem.AdapterCompatibility 
      write-host "Adapter DAC Type: " $objItem.AdapterDACType 
      write-host "Adapter RAM: " $objItem.AdapterRAM 
      write-host "Availability: " $objItem.Availability 
      write-host "Capability Descriptions: " $objItem.CapabilityDescriptions 
      write-host "Caption: " $objItem.Caption 
      write-host "Color Table Entries: " $objItem.ColorTableEntries 
      write-host "Configuration Manager Error Code: " $objItem.ConfigManagerErrorCode 
      write-host "Configuration Manager User Configuration: " $objItem.ConfigManagerUserConfig 
      write-host "Creation Class Name: " $objItem.CreationClassName 
      write-host "Current Bits Per Pixel: " $objItem.CurrentBitsPerPixel 
      write-host "Current Horizontal Resolution: " $objItem.CurrentHorizontalResolution 
      write-host "Current Number Of Colors: " $objItem.CurrentNumberOfColors 
      write-host "Current Number Of Columns: " $objItem.CurrentNumberOfColumns 
      write-host "Current Number Of Rows: " $objItem.CurrentNumberOfRows 
      write-host "Current Refresh Rate: " $objItem.CurrentRefreshRate 
      write-host "Current Scan Mode: " $objItem.CurrentScanMode 
      write-host "Current Vertical Resolution: " $objItem.CurrentVerticalResolution 
      write-host "Description: " $objItem.Description 
      write-host "Device ID: " $objItem.DeviceID 
      write-host "Device Specific Pens: " $objItem.DeviceSpecificPens 
      write-host "Dither Type: " $objItem.DitherType 
      write-host "Driver Date: " $objItem.DriverDate 
      write-host "Driver Version: " $objItem.DriverVersion 
      write-host "Error Cleared: " $objItem.ErrorCleared 
      write-host "Error Description: " $objItem.ErrorDescription 
      write-host "ICM Intent: " $objItem.ICMIntent 
      write-host "ICM Method: " $objItem.ICMMethod 
      write-host "Inf File Name: " $objItem.InfFilename 
      write-host "Inf Section: " $objItem.InfSection 
      write-host "Installation Date: " $objItem.InstallDate 
      write-host "Installed Display Drivers: " $objItem.InstalledDisplayDrivers 
      write-host "Last Error Code: " $objItem.LastErrorCode 
      write-host "Maximum Memory Supported: " $objItem.MaxMemorySupported 
      write-host "Maximum Number Controlled: " $objItem.MaxNumberControlled 
      write-host "Maximum Refresh Rate: " $objItem.MaxRefreshRate 
      write-host "Minimum Refresh Rate: " $objItem.MinRefreshRate 
      write-host "Monochrome: " $objItem.Monochrome 
      write-host "Name: " $objItem.Name 
      write-host "Number Of Color Planes: " $objItem.NumberOfColorPlanes 
      write-host "Number Of Video Pages: " $objItem.NumberOfVideoPages 
      write-host "PNP Device ID: " $objItem.PNPDeviceID 
      write-host "Power Management Capabilities: " $objItem.PowerManagementCapabilities 
      write-host "Power Management Supported: " $objItem.PowerManagementSupported 
      write-host "Protocol Supported: " $objItem.ProtocolSupported 
      write-host "Reserved System Palette Entries: " $objItem.ReservedSystemPaletteEntries 
      write-host "Specification Version: " $objItem.SpecificationVersion 
      write-host "Status: " $objItem.Status 
      write-host "Status Information: " $objItem.StatusInfo 
      write-host "System Creation Class Name: " $objItem.SystemCreationClassName 
      write-host "System Name: " $objItem.SystemName 
      write-host "System Palette Entries: " $objItem.SystemPaletteEntries 
      write-host "Time Of Last Reset: " $objItem.TimeOfLastReset 
      write-host "Video Architecture: " $objItem.VideoArchitecture 
      write-host "Video Memory Type: " $objItem.VideoMemoryType 
      write-host "Video Mode: " $objItem.VideoMode 
      write-host "Video Mode Description: " $objItem.VideoModeDescription 
      write-host "Video Processor: " $objItem.VideoProcessor 
      write-host 
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

[**CIM \_ PCVideoController**](cim-pcvideocontroller.md)
</dt> <dt>

[電腦系統硬體類別](computer-system-hardware-classes.md)
</dt> </dl>

 

 
