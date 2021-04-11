---
description: 代表執行 Windows 的電腦系統上的 CD-ROM 光碟機。
ms.assetid: 08087976-ca88-4ac8-9456-0d8bd799e66c
ms.tgt_platform: multiple
title: Win32_CDROMDrive 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CDROMDrive
- Win32_CDROMDrive.Reset
- Win32_CDROMDrive.SetPowerState
- Win32_CDROMDrive.Availability
- Win32_CDROMDrive.Capabilities
- Win32_CDROMDrive.CapabilityDescriptions
- Win32_CDROMDrive.Caption
- Win32_CDROMDrive.CompressionMethod
- Win32_CDROMDrive.ConfigManagerErrorCode
- Win32_CDROMDrive.ConfigManagerUserConfig
- Win32_CDROMDrive.CreationClassName
- Win32_CDROMDrive.DefaultBlockSize
- Win32_CDROMDrive.Description
- Win32_CDROMDrive.DeviceID
- Win32_CDROMDrive.Drive
- Win32_CDROMDrive.DriveIntegrity
- Win32_CDROMDrive.ErrorCleared
- Win32_CDROMDrive.ErrorDescription
- Win32_CDROMDrive.ErrorMethodology
- Win32_CDROMDrive.FileSystemFlags
- Win32_CDROMDrive.FileSystemFlagsEx
- Win32_CDROMDrive.Id
- Win32_CDROMDrive.InstallDate
- Win32_CDROMDrive.LastErrorCode
- Win32_CDROMDrive.Manufacturer
- Win32_CDROMDrive.MaxBlockSize
- Win32_CDROMDrive.MaximumComponentLength
- Win32_CDROMDrive.MaxMediaSize
- Win32_CDROMDrive.MediaLoaded
- Win32_CDROMDrive.MediaType
- Win32_CDROMDrive.MfrAssignedRevisionLevel
- Win32_CDROMDrive.MinBlockSize
- Win32_CDROMDrive.Name
- Win32_CDROMDrive.NeedsCleaning
- Win32_CDROMDrive.NumberOfMediaSupported
- Win32_CDROMDrive.PNPDeviceID
- Win32_CDROMDrive.PowerManagementCapabilities
- Win32_CDROMDrive.PowerManagementSupported
- Win32_CDROMDrive.RevisionLevel
- Win32_CDROMDrive.SCSIBus
- Win32_CDROMDrive.SCSILogicalUnit
- Win32_CDROMDrive.SCSIPort
- Win32_CDROMDrive.SCSITargetId
- Win32_CDROMDrive.SerialNumber
- Win32_CDROMDrive.Size
- Win32_CDROMDrive.Status
- Win32_CDROMDrive.StatusInfo
- Win32_CDROMDrive.SystemCreationClassName
- Win32_CDROMDrive.SystemName
- Win32_CDROMDrive.TransferRate
- Win32_CDROMDrive.VolumeName
- Win32_CDROMDrive.VolumeSerialNumber
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6c352d2ee717f5eb888b49d6e5e8ff456cc5a85f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936429"
---
# <a name="win32_cdromdrive-class"></a><span data-ttu-id="2e999-103">Win32 \_ CDROMDrive 類別</span><span class="sxs-lookup"><span data-stu-id="2e999-103">Win32\_CDROMDrive class</span></span>

<span data-ttu-id="2e999-104">**Win32 \_ CDROMDrive** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表執行 Windows 的電腦系統上的 cd-rom 光碟機。</span><span class="sxs-lookup"><span data-stu-id="2e999-104">The **Win32\_CDROMDrive** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a CD-ROM drive on a computer system running Windows.</span></span>

> [!Note]  
> <span data-ttu-id="2e999-105">請注意，磁片磁碟機的名稱不會對應至指派給裝置的邏輯磁碟機代號。</span><span class="sxs-lookup"><span data-stu-id="2e999-105">Be aware that the name of the drive does not correspond to the logical drive letter assigned to the device.</span></span>

 

<span data-ttu-id="2e999-106">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2e999-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="2e999-107">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="2e999-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e999-108">語法</span><span class="sxs-lookup"><span data-stu-id="2e999-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_CDROMDrive : CIM_CDROMDrive
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CompressionMethod;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint64   DefaultBlockSize;
  string   Description;
  string   DeviceID;
  string   Drive;
  boolean  DriveIntegrity;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  uint16   FileSystemFlags;
  uint32   FileSystemFlagsEx;
  string   Id;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint64   MaxBlockSize;
  uint32   MaximumComponentLength;
  uint64   MaxMediaSize;
  boolean  MediaLoaded;
  string   MediaType;
  string   MfrAssignedRevisionLevel;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   RevisionLevel;
  uint32   SCSIBus;
  uint16   SCSILogicalUnit;
  uint16   SCSIPort;
  uint16   SCSITargetId;
  string   SerialNumber;
  uint64   Size;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  real64   TransferRate;
  string   VolumeName;
  string   VolumeSerialNumber;
};
```

## <a name="members"></a><span data-ttu-id="2e999-109">成員</span><span class="sxs-lookup"><span data-stu-id="2e999-109">Members</span></span>

<span data-ttu-id="2e999-110">**Win32 \_ CDROMDrive** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2e999-110">The **Win32\_CDROMDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="2e999-111">方法</span><span class="sxs-lookup"><span data-stu-id="2e999-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="2e999-112">屬性</span><span class="sxs-lookup"><span data-stu-id="2e999-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2e999-113">方法</span><span class="sxs-lookup"><span data-stu-id="2e999-113">Methods</span></span>

<span data-ttu-id="2e999-114">**Win32 \_ CDROMDrive** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="2e999-114">The **Win32\_CDROMDrive** class has these methods.</span></span>



| <span data-ttu-id="2e999-115">方法</span><span class="sxs-lookup"><span data-stu-id="2e999-115">Method</span></span>            | <span data-ttu-id="2e999-116">描述</span><span class="sxs-lookup"><span data-stu-id="2e999-116">Description</span></span>                                                                                                                                                                                                |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e999-117">**重設**</span><span class="sxs-lookup"><span data-stu-id="2e999-117">**Reset**</span></span>         | <span data-ttu-id="2e999-118">未實作。</span><span class="sxs-lookup"><span data-stu-id="2e999-118">Not implemented.</span></span> <span data-ttu-id="2e999-119">若要執行此方法，請參閱 [**CIM \_ CDROMDrive**](cim-cdromdrive.md)中的 [**Reset**](reset-method-in-class-cim-controller.md)方法以取得檔。</span><span class="sxs-lookup"><span data-stu-id="2e999-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_CDROMDrive**](cim-cdromdrive.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="2e999-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2e999-120">**SetPowerState**</span></span> | <span data-ttu-id="2e999-121">未實作。</span><span class="sxs-lookup"><span data-stu-id="2e999-121">Not implemented.</span></span> <span data-ttu-id="2e999-122">若要執行此方法，請參閱 [**CIM \_ CDROMDrive**](cim-cdromdrive.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法，以取得檔。</span><span class="sxs-lookup"><span data-stu-id="2e999-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_CDROMDrive**](cim-cdromdrive.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2e999-123">屬性</span><span class="sxs-lookup"><span data-stu-id="2e999-123">Properties</span></span>

<span data-ttu-id="2e999-124">**Win32 \_ CDROMDrive** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2e999-124">The **Win32\_CDROMDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2e999-125">**可用性**</span><span class="sxs-lookup"><span data-stu-id="2e999-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-126">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2e999-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-128">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="2e999-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-129">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="2e999-129">Availability and status of the device.</span></span>

<span data-ttu-id="2e999-130">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2e999-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="2e999-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2e999-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="2e999-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="2e999-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="2e999-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-134">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="2e999-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="2e999-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="2e999-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="2e999-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="2e999-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2e999-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="2e999-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="2e999-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="2e999-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="2e999-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="2e999-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="2e999-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="2e999-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2e999-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="2e999-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="2e999-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="2e999-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="2e999-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="2e999-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="2e999-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="2e999-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-145">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="2e999-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="2e999-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="2e999-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-147">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="2e999-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="2e999-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="2e999-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-149">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="2e999-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="2e999-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="2e999-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="2e999-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="2e999-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-152">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="2e999-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="2e999-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="2e999-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-154">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="2e999-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="2e999-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="2e999-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-156">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="2e999-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="2e999-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="2e999-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-158">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="2e999-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="2e999-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="2e999-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-160">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="2e999-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2e999-161">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="2e999-161">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-162">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="2e999-162">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2e999-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-164">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 儲存裝置 \| 001.9 "，" MIF。DMTF \| 儲存裝置 \| 001.11 "，" MIF。DMTF \| 儲存裝置 \| 001.12 "，" MIF。DMTF \| 磁片 \| 003.7 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。**CapabilityDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="2e999-164">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-165">媒體存取裝置的功能陣列。</span><span class="sxs-lookup"><span data-stu-id="2e999-165">Array of capabilities of the media access device.</span></span> <span data-ttu-id="2e999-166">例如，裝置可能支援隨機存取 (3) 、卸載式媒體 (7) ，以及自動清除 (9) 。</span><span class="sxs-lookup"><span data-stu-id="2e999-166">For example, the device may support random access (3), removable media (7), and automatic cleaning (9).</span></span>

<span data-ttu-id="2e999-167">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-167">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2e999-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="2e999-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2e999-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="2e999-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="2e999-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**順序存取** (2) </span><span class="sxs-lookup"><span data-stu-id="2e999-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="2e999-171"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**隨機存取** (3) </span><span class="sxs-lookup"><span data-stu-id="2e999-171"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="2e999-172"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**支援寫入** (4) </span><span class="sxs-lookup"><span data-stu-id="2e999-172"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="2e999-173"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**加密** (5) </span><span class="sxs-lookup"><span data-stu-id="2e999-173"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="2e999-174"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**壓縮** (6) </span><span class="sxs-lookup"><span data-stu-id="2e999-174"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="2e999-175"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**支援卸除式媒體** (7) </span><span class="sxs-lookup"><span data-stu-id="2e999-175"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-176">支援卸載式媒體</span><span class="sxs-lookup"><span data-stu-id="2e999-176">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="2e999-177"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**手動清除** (8) </span><span class="sxs-lookup"><span data-stu-id="2e999-177"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="2e999-178"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**自動清除** (9) </span><span class="sxs-lookup"><span data-stu-id="2e999-178"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="2e999-179"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**智慧型通知** (10) </span><span class="sxs-lookup"><span data-stu-id="2e999-179"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="2e999-180"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**支援雙側媒體** (11) </span><span class="sxs-lookup"><span data-stu-id="2e999-180"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-181">支援 Dual-Sided 媒體</span><span class="sxs-lookup"><span data-stu-id="2e999-181">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="2e999-182"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**不需要 Predismount 退出** (12) </span><span class="sxs-lookup"><span data-stu-id="2e999-182"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2e999-183">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2e999-183">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-184">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="2e999-184">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2e999-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-186">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。**功能**") </span><span class="sxs-lookup"><span data-stu-id="2e999-186">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-187">**功能** 陣列中所指出之任何存取裝置功能的更詳細說明的陣列。</span><span class="sxs-lookup"><span data-stu-id="2e999-187">Array of more detailed explanations for any of the access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="2e999-188">這個陣列的每個專案都與位於相同索引的 **功能** 陣列中的專案相關。</span><span class="sxs-lookup"><span data-stu-id="2e999-188">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="2e999-189">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-189">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e999-190">**標題**</span><span class="sxs-lookup"><span data-stu-id="2e999-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-191">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2e999-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-193">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-194">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="2e999-194">Short description of the object a one-line string.</span></span>

<span data-ttu-id="2e999-195">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e999-196">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="2e999-196">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-197">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2e999-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e999-199">裝置用來支援壓縮的演算法或工具。</span><span class="sxs-lookup"><span data-stu-id="2e999-199">Algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="2e999-200">如果不可能或不想要描述壓縮配置 (可能是因為) 不知道，請使用下列文字：「未知」表示不知道裝置是否支援壓縮功能;「已壓縮」表示裝置支援壓縮功能，但其壓縮配置未知或未洩漏;和「未壓縮」表示裝置不支援壓縮功能。</span><span class="sxs-lookup"><span data-stu-id="2e999-200">If it is not possible or not desired to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the device supports compression capabilities; "Compressed" to represent that the device supports compression capabilities but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the device does not support compression capabilities.</span></span>

<span data-ttu-id="2e999-201">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-201">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="2e999-202"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="2e999-202">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="2e999-203">壓縮配置未知或未描述。</span><span class="sxs-lookup"><span data-stu-id="2e999-203">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="2e999-204"> ( 「壓縮」 ) </span><span class="sxs-lookup"><span data-stu-id="2e999-204">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="2e999-205">邏輯檔案已壓縮，但壓縮配置未知或未描述</span><span class="sxs-lookup"><span data-stu-id="2e999-205">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="2e999-206"> ( 「未壓縮」 ) </span><span class="sxs-lookup"><span data-stu-id="2e999-206">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="2e999-207">如果邏輯檔案未壓縮</span><span class="sxs-lookup"><span data-stu-id="2e999-207">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2e999-208">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2e999-208">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-209">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e999-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-210">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-211">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-211">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-212">Windows 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2e999-212">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="2e999-213">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-213">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="2e999-214"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="2e999-214"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="2e999-215"> (0)</span><span class="sxs-lookup"><span data-stu-id="2e999-215">(0)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-216">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="2e999-216">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="2e999-217"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="2e999-217"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="2e999-218">(1)</span><span class="sxs-lookup"><span data-stu-id="2e999-218">(1)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-219">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="2e999-219">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2e999-220"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="2e999-220"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="2e999-221">(2)</span><span class="sxs-lookup"><span data-stu-id="2e999-221">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="2e999-222"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="2e999-222"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="2e999-223">(3)</span><span class="sxs-lookup"><span data-stu-id="2e999-223">(3)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-224">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="2e999-224">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2e999-225"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="2e999-225"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="2e999-226">(4)</span><span class="sxs-lookup"><span data-stu-id="2e999-226">(4)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-227">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="2e999-227">Device is not working properly.</span></span> <span data-ttu-id="2e999-228">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="2e999-228">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="2e999-229"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="2e999-229"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="2e999-230">(5)</span><span class="sxs-lookup"><span data-stu-id="2e999-230">(5)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-231">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="2e999-231">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="2e999-232"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="2e999-232"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="2e999-233">(6)</span><span class="sxs-lookup"><span data-stu-id="2e999-233">(6)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-234">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="2e999-234">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="2e999-235"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="2e999-235"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="2e999-236">(7)</span><span class="sxs-lookup"><span data-stu-id="2e999-236">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="2e999-237"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="2e999-237"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="2e999-238">(8)</span><span class="sxs-lookup"><span data-stu-id="2e999-238">(8)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-239">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="2e999-239">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="2e999-240"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="2e999-240"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="2e999-241">(9)</span><span class="sxs-lookup"><span data-stu-id="2e999-241">(9)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-242">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="2e999-242">Device is not working properly.</span></span> <span data-ttu-id="2e999-243">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="2e999-243">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="2e999-244"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="2e999-244"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="2e999-245">(10)</span><span class="sxs-lookup"><span data-stu-id="2e999-245">(10)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-246">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="2e999-246">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="2e999-247"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="2e999-247"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="2e999-248">(11)</span><span class="sxs-lookup"><span data-stu-id="2e999-248">(11)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-249">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="2e999-249">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="2e999-250"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="2e999-250"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="2e999-251"> (12) </span><span class="sxs-lookup"><span data-stu-id="2e999-251">(12)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-252">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="2e999-252">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="2e999-253"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="2e999-253"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="2e999-254">(13)</span><span class="sxs-lookup"><span data-stu-id="2e999-254">(13)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-255">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="2e999-255">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="2e999-256"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="2e999-256"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="2e999-257">(14)</span><span class="sxs-lookup"><span data-stu-id="2e999-257">(14)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-258">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="2e999-258">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="2e999-259"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="2e999-259"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="2e999-260">(15)</span><span class="sxs-lookup"><span data-stu-id="2e999-260">(15)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-261">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="2e999-261">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="2e999-262"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="2e999-262"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="2e999-263">(16)</span><span class="sxs-lookup"><span data-stu-id="2e999-263">(16)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-264">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="2e999-264">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="2e999-265"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="2e999-265"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="2e999-266">(17)</span><span class="sxs-lookup"><span data-stu-id="2e999-266">(17)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-267">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="2e999-267">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2e999-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="2e999-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="2e999-269">(18)</span><span class="sxs-lookup"><span data-stu-id="2e999-269">(18)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-270">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="2e999-270">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="2e999-271"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="2e999-271"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="2e999-272">(19)</span><span class="sxs-lookup"><span data-stu-id="2e999-272">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2e999-273"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="2e999-273"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="2e999-274">(20)</span><span class="sxs-lookup"><span data-stu-id="2e999-274">(20)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-275">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="2e999-275">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="2e999-276"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="2e999-276"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="2e999-277">(21)</span><span class="sxs-lookup"><span data-stu-id="2e999-277">(21)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-278">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="2e999-278">System failure.</span></span> <span data-ttu-id="2e999-279">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="2e999-279">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="2e999-280">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="2e999-280">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="2e999-281"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="2e999-281"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="2e999-282">(22)</span><span class="sxs-lookup"><span data-stu-id="2e999-282">(22)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-283">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="2e999-283">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="2e999-284"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="2e999-284"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="2e999-285">(23)</span><span class="sxs-lookup"><span data-stu-id="2e999-285">(23)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-286">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="2e999-286">System failure.</span></span> <span data-ttu-id="2e999-287">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="2e999-287">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="2e999-288"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="2e999-288"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="2e999-289">(24)</span><span class="sxs-lookup"><span data-stu-id="2e999-289">(24)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-290">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="2e999-290">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2e999-291"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="2e999-291"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="2e999-292">(25)</span><span class="sxs-lookup"><span data-stu-id="2e999-292">(25)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-293">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="2e999-293">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2e999-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="2e999-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="2e999-295">(26)</span><span class="sxs-lookup"><span data-stu-id="2e999-295">(26)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-296">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="2e999-296">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="2e999-297"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="2e999-297"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="2e999-298">(27)</span><span class="sxs-lookup"><span data-stu-id="2e999-298">(27)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-299">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="2e999-299">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="2e999-300"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="2e999-300"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="2e999-301">(28)</span><span class="sxs-lookup"><span data-stu-id="2e999-301">(28)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-302">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="2e999-302">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="2e999-303"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="2e999-303"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="2e999-304">(29)</span><span class="sxs-lookup"><span data-stu-id="2e999-304">(29)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-305">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="2e999-305">Device is disabled.</span></span> <span data-ttu-id="2e999-306">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="2e999-306">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="2e999-307"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="2e999-307"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="2e999-308">(30)</span><span class="sxs-lookup"><span data-stu-id="2e999-308">(30)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-309">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="2e999-309">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2e999-310"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="2e999-310"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="2e999-311"> (31) </span><span class="sxs-lookup"><span data-stu-id="2e999-311">(31)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-312">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="2e999-312">Device is not working properly.</span></span> <span data-ttu-id="2e999-313">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="2e999-313">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2e999-314">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="2e999-314">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-315">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2e999-315">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-316">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-317">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-317">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-318">若 **為 True**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="2e999-318">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="2e999-319">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e999-320">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2e999-320">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-321">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2e999-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-322">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-323">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2e999-323">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2e999-324">第一個具象類別的名稱，這個類別會出現在建立實例時所用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="2e999-324">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="2e999-325">當搭配類別的其他索引鍵屬性使用時，屬性允許唯一識別此類別的所有實例和其子類別。</span><span class="sxs-lookup"><span data-stu-id="2e999-325">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="2e999-326">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-326">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e999-327">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="2e999-327">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-328">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="2e999-328">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-329">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-330">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-330">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-331">此裝置的預設區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2e999-331">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="2e999-332">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-332">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="2e999-333">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="2e999-333">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2e999-334">**說明**</span><span class="sxs-lookup"><span data-stu-id="2e999-334">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-335">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2e999-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-336">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-337">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-337">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-338">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="2e999-338">Description of the object.</span></span>

<span data-ttu-id="2e999-339">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-339">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e999-340">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="2e999-340">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-341">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2e999-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-342">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-343">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "DeviceId" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| File 函數 \| GetLogicalDriveStrings" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-343">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetLogicalDriveStrings")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-344">CD-ROM 光碟機的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="2e999-344">Unique identifier for a CD-ROM drive.</span></span>

<span data-ttu-id="2e999-345">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e999-346">**磁碟機**</span><span class="sxs-lookup"><span data-stu-id="2e999-346">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-347">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2e999-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-348">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-349">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| File 函數 \| GetDriveType" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-349">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-350">CD-ROM 光碟機的磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="2e999-350">Drive letter of the CD-ROM drive.</span></span>

<span data-ttu-id="2e999-351">範例： "d： \\ "</span><span class="sxs-lookup"><span data-stu-id="2e999-351">Example: "d:\\"</span></span>

</dd> <dt>

<span data-ttu-id="2e999-352">**DriveIntegrity**</span><span class="sxs-lookup"><span data-stu-id="2e999-352">**DriveIntegrity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-353">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2e999-353">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-354">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-355">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-355">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-356">若 **為 True**，可以從 CD 裝置精確地讀取檔案。</span><span class="sxs-lookup"><span data-stu-id="2e999-356">If **True**, files can be accurately read from the CD device.</span></span> <span data-ttu-id="2e999-357">這是藉由讀取資料區塊兩次，並將資料與本身進行比較來達成。</span><span class="sxs-lookup"><span data-stu-id="2e999-357">This is achieved by reading a block of data twice and comparing the data against itself.</span></span>

</dd> <dt>

<span data-ttu-id="2e999-358">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="2e999-358">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-359">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2e999-359">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-360">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e999-361">若 **為 True**，則表示 **LastErrorCode** 中回報的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="2e999-361">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="2e999-362">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-362">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e999-363">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2e999-363">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-364">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2e999-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-365">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e999-366">有關 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及可採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2e999-366">More information about the error recorded in **LastErrorCode**, and information about corrective actions that can be taken.</span></span>

<span data-ttu-id="2e999-367">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-367">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e999-368">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="2e999-368">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-369">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2e999-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-370">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e999-371">此裝置支援的錯誤偵測和修正類型。</span><span class="sxs-lookup"><span data-stu-id="2e999-371">Type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="2e999-372">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-372">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e999-373">**FileSystemFlags**</span><span class="sxs-lookup"><span data-stu-id="2e999-373">**FileSystemFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-374">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2e999-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-375">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-376">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| File System 函數 \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-376">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-377">這個屬性已經過時。</span><span class="sxs-lookup"><span data-stu-id="2e999-377">This property is obsolete.</span></span> <span data-ttu-id="2e999-378">若要取代這個屬性，請使用 **FileSystemFlagsEx**。</span><span class="sxs-lookup"><span data-stu-id="2e999-378">In place of this property, use **FileSystemFlagsEx**.</span></span>

</dd> <dt>

<span data-ttu-id="2e999-379">**FileSystemFlagsEx**</span><span class="sxs-lookup"><span data-stu-id="2e999-379">**FileSystemFlagsEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-380">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e999-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-381">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-382">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| File System 函數 \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-382">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-383">與 Windows CD-ROM 光碟機相關聯的檔案系統旗標。</span><span class="sxs-lookup"><span data-stu-id="2e999-383">File system flags associated with the Windows CD-ROM drive.</span></span> <span data-ttu-id="2e999-384">此參數可以是旗標的任意組合，但是 **fs \_ 檔 \_ 壓縮** 和 **fs 模式 \_ \_ 會 \_** 互相排斥。</span><span class="sxs-lookup"><span data-stu-id="2e999-384">This parameter can be any combination of flags, but **FS\_FILE\_COMPRESSION** and **FS\_VOL\_IS\_COMPRESSED** are mutually exclusive.</span></span>

<dt>

<span id="Case_Sensitive_Search"></span><span id="case_sensitive_search"></span><span id="CASE_SENSITIVE_SEARCH"></span>

<span data-ttu-id="2e999-385"><span id="Case_Sensitive_Search"></span><span id="case_sensitive_search"></span><span id="CASE_SENSITIVE_SEARCH"></span>區分 **大小寫的搜尋** (1) </span><span class="sxs-lookup"><span data-stu-id="2e999-385"><span id="Case_Sensitive_Search"></span><span id="case_sensitive_search"></span><span id="CASE_SENSITIVE_SEARCH"></span>**Case Sensitive Search** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-386">檔案系統支援區分大小寫的檔案名。</span><span class="sxs-lookup"><span data-stu-id="2e999-386">The file system supports case-sensitive file names.</span></span>

</dd> <dt>

<span id="Case_Preserved_Names"></span><span id="case_preserved_names"></span><span id="CASE_PRESERVED_NAMES"></span>

<span data-ttu-id="2e999-387"><span id="Case_Preserved_Names"></span><span id="case_preserved_names"></span><span id="CASE_PRESERVED_NAMES"></span>**保留大小寫名稱** (2) </span><span class="sxs-lookup"><span data-stu-id="2e999-387"><span id="Case_Preserved_Names"></span><span id="case_preserved_names"></span><span id="CASE_PRESERVED_NAMES"></span>**Case Preserved Names** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-388">檔案系統在磁片上放置名稱時，會保留檔案名的大小寫。</span><span class="sxs-lookup"><span data-stu-id="2e999-388">The file system preserves the case of file names when it places a name on a disk.</span></span>

</dd> <dt>

<span id="Unicode_On_Disk"></span><span id="unicode_on_disk"></span><span id="UNICODE_ON_DISK"></span>

<span data-ttu-id="2e999-389"><span id="Unicode_On_Disk"></span><span id="unicode_on_disk"></span><span id="UNICODE_ON_DISK"></span>**磁片上的 Unicode** (4) </span><span class="sxs-lookup"><span data-stu-id="2e999-389"><span id="Unicode_On_Disk"></span><span id="unicode_on_disk"></span><span id="UNICODE_ON_DISK"></span>**Unicode On Disk** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-390">檔案系統在檔案名中支援 Unicode，因為它們出現在磁片上。</span><span class="sxs-lookup"><span data-stu-id="2e999-390">The file system supports Unicode in file names as they appear on the disk.</span></span>

</dd> <dt>

<span id="Persistent_ACLs"></span><span id="persistent_acls"></span><span id="PERSISTENT_ACLS"></span>

<span data-ttu-id="2e999-391"><span id="Persistent_ACLs"></span><span id="persistent_acls"></span><span id="PERSISTENT_ACLS"></span>**持續性 acl** (8) </span><span class="sxs-lookup"><span data-stu-id="2e999-391"><span id="Persistent_ACLs"></span><span id="persistent_acls"></span><span id="PERSISTENT_ACLS"></span>**Persistent ACLs** (8)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-392">檔案系統會保留並強制執行 (Acl) 的存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="2e999-392">The file system preserves and enforces access control lists (ACLs).</span></span> <span data-ttu-id="2e999-393">例如，NTFS 檔案系統會保留並強制執行 Acl，而 FAT 檔案系統則否。</span><span class="sxs-lookup"><span data-stu-id="2e999-393">For example, the NTFS file system preserves and enforces ACLs and the FAT file system does not.</span></span>

</dd> <dt>

<span id="File_Compression"></span><span id="file_compression"></span><span id="FILE_COMPRESSION"></span>

<span data-ttu-id="2e999-394"><span id="File_Compression"></span><span id="file_compression"></span><span id="FILE_COMPRESSION"></span>**檔案壓縮** (16) </span><span class="sxs-lookup"><span data-stu-id="2e999-394"><span id="File_Compression"></span><span id="file_compression"></span><span id="FILE_COMPRESSION"></span>**File Compression** (16)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-395">檔案系統支援以檔案為基礎的壓縮。</span><span class="sxs-lookup"><span data-stu-id="2e999-395">The file system supports file-based compression.</span></span>

</dd> <dt>

<span id="Volume_Quotas"></span><span id="volume_quotas"></span><span id="VOLUME_QUOTAS"></span>

<span data-ttu-id="2e999-396"><span id="Volume_Quotas"></span><span id="volume_quotas"></span><span id="VOLUME_QUOTAS"></span>**磁片區配額** (32) </span><span class="sxs-lookup"><span data-stu-id="2e999-396"><span id="Volume_Quotas"></span><span id="volume_quotas"></span><span id="VOLUME_QUOTAS"></span>**Volume Quotas** (32)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-397">檔案系統支援磁片配額。</span><span class="sxs-lookup"><span data-stu-id="2e999-397">The file system supports disk quotas.</span></span>

</dd> <dt>

<span id="Supports_Sparse_Files"></span><span id="supports_sparse_files"></span><span id="SUPPORTS_SPARSE_FILES"></span>

<span data-ttu-id="2e999-398"><span id="Supports_Sparse_Files"></span><span id="supports_sparse_files"></span><span id="SUPPORTS_SPARSE_FILES"></span>**支援** (64 的稀疏檔案) </span><span class="sxs-lookup"><span data-stu-id="2e999-398"><span id="Supports_Sparse_Files"></span><span id="supports_sparse_files"></span><span id="SUPPORTS_SPARSE_FILES"></span>**Supports Sparse Files** (64)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-399">檔案系統支援備用檔案。</span><span class="sxs-lookup"><span data-stu-id="2e999-399">The file system supports spare files.</span></span>

</dd> <dt>

<span id="Supports_Reparse_Points"></span><span id="supports_reparse_points"></span><span id="SUPPORTS_REPARSE_POINTS"></span>

<span data-ttu-id="2e999-400"><span id="Supports_Reparse_Points"></span><span id="supports_reparse_points"></span><span id="SUPPORTS_REPARSE_POINTS"></span>支援 (128) 的重新 **剖析點**</span><span class="sxs-lookup"><span data-stu-id="2e999-400"><span id="Supports_Reparse_Points"></span><span id="supports_reparse_points"></span><span id="SUPPORTS_REPARSE_POINTS"></span>**Supports Reparse Points** (128)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-401">檔案系統支援重新分析點。</span><span class="sxs-lookup"><span data-stu-id="2e999-401">The file system supports reparse points.</span></span>

</dd> <dt>

<span id="Supports_Remote_Storage"></span><span id="supports_remote_storage"></span><span id="SUPPORTS_REMOTE_STORAGE"></span>

<span data-ttu-id="2e999-402"><span id="Supports_Remote_Storage"></span><span id="supports_remote_storage"></span><span id="SUPPORTS_REMOTE_STORAGE"></span>**支援遠端存放** (256) </span><span class="sxs-lookup"><span data-stu-id="2e999-402"><span id="Supports_Remote_Storage"></span><span id="supports_remote_storage"></span><span id="SUPPORTS_REMOTE_STORAGE"></span>**Supports Remote Storage** (256)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-403">檔案系統支援檔案的遠端儲存。</span><span class="sxs-lookup"><span data-stu-id="2e999-403">The file system supports the remote storage of files.</span></span>

</dd> <dt>

<span id="Supports_Long_Names"></span><span id="supports_long_names"></span><span id="SUPPORTS_LONG_NAMES"></span>

<span data-ttu-id="2e999-404"><span id="Supports_Long_Names"></span><span id="supports_long_names"></span><span id="SUPPORTS_LONG_NAMES"></span>**支援長名稱** (16384) </span><span class="sxs-lookup"><span data-stu-id="2e999-404"><span id="Supports_Long_Names"></span><span id="supports_long_names"></span><span id="SUPPORTS_LONG_NAMES"></span>**Supports Long Names** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-405">檔案系統支援長度超過八個字元的檔案名。</span><span class="sxs-lookup"><span data-stu-id="2e999-405">The file system supports file names that are longer than eight characters.</span></span>

</dd> <dt>

<span id="Volume_Is_Compressed"></span><span id="volume_is_compressed"></span><span id="VOLUME_IS_COMPRESSED"></span>

<span data-ttu-id="2e999-406"><span id="Volume_Is_Compressed"></span><span id="volume_is_compressed"></span><span id="VOLUME_IS_COMPRESSED"></span>**磁片區已壓縮** (32768) </span><span class="sxs-lookup"><span data-stu-id="2e999-406"><span id="Volume_Is_Compressed"></span><span id="volume_is_compressed"></span><span id="VOLUME_IS_COMPRESSED"></span>**Volume Is Compressed** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-407">指定的磁片區是壓縮的磁片區，例如 DoubleSpace 磁片區。</span><span class="sxs-lookup"><span data-stu-id="2e999-407">The specified disk volume is a compressed volume, for example, a DoubleSpace volume.</span></span>

</dd> <dt>

<span id="Read_Only_Volume"></span><span id="read_only_volume"></span><span id="READ_ONLY_VOLUME"></span>

<span data-ttu-id="2e999-408"><span id="Read_Only_Volume"></span><span id="read_only_volume"></span><span id="READ_ONLY_VOLUME"></span>**唯讀磁片** 區 (524289) </span><span class="sxs-lookup"><span data-stu-id="2e999-408"><span id="Read_Only_Volume"></span><span id="read_only_volume"></span><span id="READ_ONLY_VOLUME"></span>**Read Only Volume** (524289)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-409">指定的磁片區是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="2e999-409">The specified volume is read-only.</span></span>

</dd> <dt>

<span id="Supports_Object_IDS"></span><span id="supports_object_ids"></span><span id="SUPPORTS_OBJECT_IDS"></span>

<span data-ttu-id="2e999-410"><span id="Supports_Object_IDS"></span><span id="supports_object_ids"></span><span id="SUPPORTS_OBJECT_IDS"></span>**支援物件識別碼** (65536) </span><span class="sxs-lookup"><span data-stu-id="2e999-410"><span id="Supports_Object_IDS"></span><span id="supports_object_ids"></span><span id="SUPPORTS_OBJECT_IDS"></span>**Supports Object IDS** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-411">檔案系統支援物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="2e999-411">The file system supports object identifiers.</span></span>

</dd> <dt>

<span id="Supports_Encryption"></span><span id="supports_encryption"></span><span id="SUPPORTS_ENCRYPTION"></span>

<span data-ttu-id="2e999-412"><span id="Supports_Encryption"></span><span id="supports_encryption"></span><span id="SUPPORTS_ENCRYPTION"></span>**支援加密** (131072) </span><span class="sxs-lookup"><span data-stu-id="2e999-412"><span id="Supports_Encryption"></span><span id="supports_encryption"></span><span id="SUPPORTS_ENCRYPTION"></span>**Supports Encryption** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-413">檔案系統支援 (EFS) 的加密檔案系統。</span><span class="sxs-lookup"><span data-stu-id="2e999-413">The file system supports the Encrypted File System (EFS).</span></span>

</dd> <dt>

<span id="Supports_Named_Streams"></span><span id="supports_named_streams"></span><span id="SUPPORTS_NAMED_STREAMS"></span>

<span data-ttu-id="2e999-414"><span id="Supports_Named_Streams"></span><span id="supports_named_streams"></span><span id="SUPPORTS_NAMED_STREAMS"></span>支援 (262144) 的 **命名資料流程**</span><span class="sxs-lookup"><span data-stu-id="2e999-414"><span id="Supports_Named_Streams"></span><span id="supports_named_streams"></span><span id="SUPPORTS_NAMED_STREAMS"></span>**Supports Named Streams** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-415">檔案系統支援指定的資料流程。</span><span class="sxs-lookup"><span data-stu-id="2e999-415">The file system supports named streams.</span></span>

</dd> </dl>

<span data-ttu-id="2e999-416">範例：0</span><span class="sxs-lookup"><span data-stu-id="2e999-416">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="2e999-417">**識別碼**</span><span class="sxs-lookup"><span data-stu-id="2e999-417">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-418">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2e999-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-419">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-420">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| File 函數 \| GetDriveType" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-420">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-421">唯一識別此 CD-ROM 光碟機的磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="2e999-421">Drive letter that uniquely identifies this CD-ROM drive.</span></span>

<span data-ttu-id="2e999-422">範例： "d： \\ "</span><span class="sxs-lookup"><span data-stu-id="2e999-422">Example: "d:\\"</span></span>

</dd> <dt>

<span data-ttu-id="2e999-423">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2e999-423">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-424">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="2e999-424">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-425">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-426">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="2e999-426">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-427">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="2e999-427">Date and time the object is installed.</span></span> <span data-ttu-id="2e999-428">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="2e999-428">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="2e999-429">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-429">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e999-430">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2e999-430">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-431">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e999-431">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-432">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e999-433">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2e999-433">Last error code reported by the logical device.</span></span>

<span data-ttu-id="2e999-434">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-434">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e999-435">**製造商**</span><span class="sxs-lookup"><span data-stu-id="2e999-435">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-436">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2e999-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-437">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-438">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-438">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-439">Windows CD-ROM 光碟機的製造商。</span><span class="sxs-lookup"><span data-stu-id="2e999-439">Manufacturer of the Windows CD-ROM drive.</span></span>

<span data-ttu-id="2e999-440">範例： "PLEXTOR"</span><span class="sxs-lookup"><span data-stu-id="2e999-440">Example: "PLEXTOR"</span></span>

</dd> <dt>

<span data-ttu-id="2e999-441">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="2e999-441">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-442">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="2e999-442">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-443">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-444">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-444">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-445">此裝置所存取媒體的最大區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2e999-445">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="2e999-446">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-446">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="2e999-447">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="2e999-447">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2e999-448">**MaximumComponentLength**</span><span class="sxs-lookup"><span data-stu-id="2e999-448">**MaximumComponentLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-449">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e999-449">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-450">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-451">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| File System 函數 \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-451">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-452">Windows CD-ROM 光碟機所支援的檔案名元件最大長度。</span><span class="sxs-lookup"><span data-stu-id="2e999-452">Maximum length of a filename component supported by the Windows CD-ROM drive.</span></span> <span data-ttu-id="2e999-453">檔案名元件是在反斜線之間的檔案名部分。</span><span class="sxs-lookup"><span data-stu-id="2e999-453">A file name component the portion of a file name between backslashes.</span></span> <span data-ttu-id="2e999-454">此值可用來指出指定的檔案系統所支援的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="2e999-454">The value can be used to indicate that long names are supported by the specified file system.</span></span> <span data-ttu-id="2e999-455">例如，對於支援長名稱的 FAT 檔案系統，此函式會儲存值255，而不是先前的8.3 指標。</span><span class="sxs-lookup"><span data-stu-id="2e999-455">For example, for a FAT file system supporting long names, the function stores the value 255, rather than the previous 8.3 indicator.</span></span> <span data-ttu-id="2e999-456">使用 NTFS 檔案系統的系統也可以支援完整名稱。</span><span class="sxs-lookup"><span data-stu-id="2e999-456">Long names can also be supported on systems that use the NTFS file system.</span></span>

<span data-ttu-id="2e999-457">範例：255</span><span class="sxs-lookup"><span data-stu-id="2e999-457">Example: 255</span></span>

</dd> <dt>

<span data-ttu-id="2e999-458">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="2e999-458">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-459">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="2e999-459">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-460">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-461">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 順序存取裝置 \| 001.2 「) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「kb」 ) </span><span class="sxs-lookup"><span data-stu-id="2e999-461">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-462">此裝置支援的媒體大小上限（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="2e999-462">Maximum size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="2e999-463">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-463">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="2e999-464">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="2e999-464">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2e999-465">**MediaLoaded**</span><span class="sxs-lookup"><span data-stu-id="2e999-465">**MediaLoaded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-466">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2e999-466">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-467">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-467">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-468">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| File System 函數 \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-468">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-469">若 **為 True**，則表示磁片磁碟機中有 cd-rom。</span><span class="sxs-lookup"><span data-stu-id="2e999-469">If **True**, a CD-ROM is in the drive.</span></span>

</dd> <dt>

<span data-ttu-id="2e999-470">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="2e999-470">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-471">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2e999-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-472">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-473">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| GetDriveType" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-473">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-474">此裝置可以使用或存取的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="2e999-474">Type of media that can be used or accessed by this device.</span></span> <span data-ttu-id="2e999-475">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="2e999-475">Possible values are:</span></span>

<dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="2e999-476">**隨機存取** ( 「隨機存取」 ) </span><span class="sxs-lookup"><span data-stu-id="2e999-476">**Random Access** ("Random Access")</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="2e999-477">**支援寫入** ( 「支援寫入」 ) </span><span class="sxs-lookup"><span data-stu-id="2e999-477">**Supports Writing** ("Supports Writing")</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Media"></span><span id="removable_media"></span><span id="REMOVABLE_MEDIA"></span>

<span data-ttu-id="2e999-478">**卸除式媒體** ( 「卸載式媒體」 ) </span><span class="sxs-lookup"><span data-stu-id="2e999-478">**Removable Media** ("Removable Media")</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span data-ttu-id="2e999-479">**Cd-rom ( 「** cd-rom」 ) </span><span class="sxs-lookup"><span data-stu-id="2e999-479">**CD-ROM** ("CD-ROM")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2e999-480">**MfrAssignedRevisionLevel**</span><span class="sxs-lookup"><span data-stu-id="2e999-480">**MfrAssignedRevisionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-481">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2e999-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-482">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-483">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win2000DDK \| KernelModeDrivers \| [**儲存體 \_ 裝置 \_ 描述**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)項 \| ProductRevisionOffset」 ) </span><span class="sxs-lookup"><span data-stu-id="2e999-483">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win2000DDK\|KernelModeDrivers\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|ProductRevisionOffset")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-484">製造商所指派的固件修訂層級。</span><span class="sxs-lookup"><span data-stu-id="2e999-484">Firmware revision level that is assigned by the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="2e999-485">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="2e999-485">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-486">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="2e999-486">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-487">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-488">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-488">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-489">此裝置所存取媒體的區塊大小下限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2e999-489">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="2e999-490">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-490">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="2e999-491">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="2e999-491">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2e999-492">**名稱**</span><span class="sxs-lookup"><span data-stu-id="2e999-492">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-493">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2e999-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-494">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-495">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-495">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-496">物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="2e999-496">Label for the object.</span></span> <span data-ttu-id="2e999-497">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="2e999-497">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="2e999-498">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-498">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e999-499">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="2e999-499">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-500">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2e999-500">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-501">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-501">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e999-502">若 **為 True**，則媒體存取裝置需要清除。</span><span class="sxs-lookup"><span data-stu-id="2e999-502">If **True**, the media access device needs cleaning.</span></span> <span data-ttu-id="2e999-503">在 [ **功能** ] 屬性中，是否可能指出手動或自動清除。</span><span class="sxs-lookup"><span data-stu-id="2e999-503">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="2e999-504">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-504">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e999-505">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="2e999-505">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-506">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e999-506">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-507">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e999-508">當媒體存取裝置支援多個個別媒體時，可支援或插入的媒體數目上限。</span><span class="sxs-lookup"><span data-stu-id="2e999-508">Maximum number of media that can be supported or inserted, when the media access device supports multiple individual media.</span></span>

<span data-ttu-id="2e999-509">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-509">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e999-510">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="2e999-510">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-511">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2e999-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-512">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-513">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-513">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-514">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="2e999-514">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="2e999-515">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-515">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="2e999-516">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="2e999-516">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="2e999-517">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2e999-517">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-518">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="2e999-518">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2e999-519">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e999-520">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="2e999-520">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="2e999-521">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="2e999-521">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2e999-522"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="2e999-522"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="2e999-523"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="2e999-523"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-524">此裝置不支援與電源相關的容量。</span><span class="sxs-lookup"><span data-stu-id="2e999-524">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2e999-525"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="2e999-525"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2e999-526"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="2e999-526"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-527">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="2e999-527">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="2e999-528"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="2e999-528"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-529">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="2e999-529">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="2e999-530"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="2e999-530"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-531">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="2e999-531">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="2e999-532">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="2e999-532">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="2e999-533">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="2e999-533">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="2e999-534"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="2e999-534"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-535">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="2e999-535">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="2e999-536"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="2e999-536"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2e999-537">支援計時 Power-On</span><span class="sxs-lookup"><span data-stu-id="2e999-537">Timed Power-On Supported</span></span>

<span data-ttu-id="2e999-538">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="2e999-538">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2e999-539">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="2e999-539">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-540">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2e999-540">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-541">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-541">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e999-542">若 **為 True**，則裝置可以是電源管理的，這表示它可以進入暫停模式，依此類推。</span><span class="sxs-lookup"><span data-stu-id="2e999-542">If **True**, the device can be power-managed, which means that it can be put into suspend mode, and so on.</span></span> <span data-ttu-id="2e999-543">屬性不表示電源管理功能目前已啟用，只有邏輯裝置能夠進行電源管理。</span><span class="sxs-lookup"><span data-stu-id="2e999-543">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="2e999-544">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-544">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e999-545">**RevisionLevel**</span><span class="sxs-lookup"><span data-stu-id="2e999-545">**RevisionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-546">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2e999-546">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-547">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-547">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-548">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| RevisionLevel" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-548">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|RevisionLevel")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-549">Windows DVD-ROM 磁片磁碟機的固件修訂層級。</span><span class="sxs-lookup"><span data-stu-id="2e999-549">Firmware revision level of the Windows CD-ROM drive.</span></span>

</dd> <dt>

<span data-ttu-id="2e999-550">**SCSIBus**</span><span class="sxs-lookup"><span data-stu-id="2e999-550">**SCSIBus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-551">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e999-551">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-552">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-552">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-553">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| scsi 結構 \| [**scsi \_ REQUEST \_ BLOCK**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block) \| PathId" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-553">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SCSI Structures\|[**SCSI\_REQUEST\_BLOCK**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block)\|PathId")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-554">磁片磁碟機的 SCSI 匯流排號碼。</span><span class="sxs-lookup"><span data-stu-id="2e999-554">SCSI bus number for the disk drive.</span></span>

<span data-ttu-id="2e999-555">範例：0</span><span class="sxs-lookup"><span data-stu-id="2e999-555">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="2e999-556">**SCSILogicalUnit**</span><span class="sxs-lookup"><span data-stu-id="2e999-556">**SCSILogicalUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-557">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2e999-557">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-558">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-559">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| scsi 結構 \| [**scsi \_ REQUEST \_ BLOCK**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block) \| Lun" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-559">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SCSI Structures\|[**SCSI\_REQUEST\_BLOCK**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block)\|Lun")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-560">磁片磁碟機的 SCSI 邏輯單元編號 (LUN) 。</span><span class="sxs-lookup"><span data-stu-id="2e999-560">SCSI logical unit number (LUN) of the disk drive.</span></span> <span data-ttu-id="2e999-561">LUN 可用來指定在使用多個控制器的系統中存取的 SCSI 控制器。</span><span class="sxs-lookup"><span data-stu-id="2e999-561">The LUN is used to designate which SCSI controller is being accessed in a system with more than one controller being used.</span></span> <span data-ttu-id="2e999-562">SCSI 裝置識別碼很類似，但是一個控制器上多個裝置的指定。</span><span class="sxs-lookup"><span data-stu-id="2e999-562">The SCSI device identifier is similar, but is the designation for multiple devices on one controller.</span></span>

<span data-ttu-id="2e999-563">範例：0</span><span class="sxs-lookup"><span data-stu-id="2e999-563">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="2e999-564">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="2e999-564">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-565">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2e999-565">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-566">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-566">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-567">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| scsi 結構 \| [**scsi \_ REQUEST \_ BLOCK**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block) \| ScsiStatus" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-567">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SCSI Structures\|[**SCSI\_REQUEST\_BLOCK**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block)\|ScsiStatus")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-568">磁片磁碟機的 SCSI 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="2e999-568">SCSI port number of the disk drive.</span></span>

<span data-ttu-id="2e999-569">範例：1</span><span class="sxs-lookup"><span data-stu-id="2e999-569">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="2e999-570">**SCSITargetId**</span><span class="sxs-lookup"><span data-stu-id="2e999-570">**SCSITargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-571">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2e999-571">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-572">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-573">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| DeviceIoControl \| IOCTL \_ SCSI \_ GET \_ ADDRESS" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-573">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|DeviceIoControl\|IOCTL\_SCSI\_GET\_ADDRESS")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-574">Windows DVD-ROM 磁片磁碟機的 SCSI 識別碼號碼。</span><span class="sxs-lookup"><span data-stu-id="2e999-574">SCSI identifier number of the Windows CD-ROM drive.</span></span>

<span data-ttu-id="2e999-575">範例：0</span><span class="sxs-lookup"><span data-stu-id="2e999-575">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="2e999-576">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="2e999-576">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-577">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2e999-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-578">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-578">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-579">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 裝置輸入和輸出結構 \| [**儲存 \_ 裝置 \_ 描述**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)項 \| SerialNumberOffset」 ) </span><span class="sxs-lookup"><span data-stu-id="2e999-579">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|SerialNumberOffset")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-580">識別實體媒體的製造商所提供的號碼。</span><span class="sxs-lookup"><span data-stu-id="2e999-580">Number supplied by the manufacturer that identifies the physical media.</span></span> <span data-ttu-id="2e999-581">範例： WD-WM3493798728。</span><span class="sxs-lookup"><span data-stu-id="2e999-581">Example: WD-WM3493798728.</span></span>

</dd> <dt>

<span data-ttu-id="2e999-582">**大小**</span><span class="sxs-lookup"><span data-stu-id="2e999-582">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-583">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="2e999-583">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-584">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-584">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-585">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| File 函數 \| GetDiskFreeSpace" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-585">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDiskFreeSpace"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-586">磁片磁碟機的大小。</span><span class="sxs-lookup"><span data-stu-id="2e999-586">Size of the disk drive.</span></span>

<span data-ttu-id="2e999-587">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="2e999-587">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2e999-588">**狀態**</span><span class="sxs-lookup"><span data-stu-id="2e999-588">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-589">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2e999-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-590">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-591">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-591">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-592">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="2e999-592">Current status of the object.</span></span> <span data-ttu-id="2e999-593">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="2e999-593">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="2e999-594">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="2e999-594">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="2e999-595">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="2e999-595">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2e999-596">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="2e999-596">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2e999-597">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="2e999-597">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2e999-598">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-598">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2e999-599">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="2e999-599">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2e999-600">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="2e999-600">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2e999-601">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="2e999-601">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2e999-602">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="2e999-602">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2e999-603">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="2e999-603">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2e999-604">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="2e999-604">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2e999-605">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="2e999-605">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2e999-606">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="2e999-606">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2e999-607">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="2e999-607">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2e999-608">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="2e999-608">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2e999-609">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-609">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2e999-610">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="2e999-610">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2e999-611">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="2e999-611">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2e999-612">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="2e999-612">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-613">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2e999-613">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-614">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-614">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-615">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="2e999-615">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-616">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="2e999-616">State of the logical device.</span></span> <span data-ttu-id="2e999-617">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="2e999-617">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="2e999-618">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-618">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2e999-619">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="2e999-619">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2e999-620">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="2e999-620">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2e999-621">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="2e999-621">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2e999-622">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="2e999-622">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2e999-623">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="2e999-623">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2e999-624">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2e999-624">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-625">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2e999-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-626">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-626">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-627">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2e999-627">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2e999-628">範圍電腦之 **CreationClassName** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="2e999-628">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="2e999-629">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-629">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e999-630">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2e999-630">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-631">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2e999-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-632">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-632">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-633">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2e999-633">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2e999-634">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="2e999-634">Name of the scoping system.</span></span>

<span data-ttu-id="2e999-635">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-635">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e999-636">**TransferRate**</span><span class="sxs-lookup"><span data-stu-id="2e999-636">**TransferRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-637">資料類型： **real64**</span><span class="sxs-lookup"><span data-stu-id="2e999-637">Data type: **real64**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-638">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-638">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-639">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API 檔案 \| 參考和時間參考」 ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「每秒的 kb 數」 ) </span><span class="sxs-lookup"><span data-stu-id="2e999-639">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Reference and Time Reference"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes per second")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-640">CD-ROM 光碟機的傳送速率。</span><span class="sxs-lookup"><span data-stu-id="2e999-640">Transfer rate of the CD-ROM drive.</span></span> <span data-ttu-id="2e999-641">值為-1 表示無法判斷速率。</span><span class="sxs-lookup"><span data-stu-id="2e999-641">A value of -1 indicates that the rate cannot be determined.</span></span> <span data-ttu-id="2e999-642">發生這種情況時，光碟不在磁片磁碟機中。</span><span class="sxs-lookup"><span data-stu-id="2e999-642">When this happens, the CD is not in the drive.</span></span>

</dd> <dt>

<span data-ttu-id="2e999-643">**VolumeName**</span><span class="sxs-lookup"><span data-stu-id="2e999-643">**VolumeName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-644">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2e999-644">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-645">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-645">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-646">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| File System 函數 \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-646">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-647">Windows CD-ROM 光碟機的磁片區名稱。</span><span class="sxs-lookup"><span data-stu-id="2e999-647">Volume name of the Windows CD-ROM drive.</span></span>

</dd> <dt>

<span data-ttu-id="2e999-648">**VolumeSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="2e999-648">**VolumeSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e999-649">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2e999-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e999-650">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e999-650">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e999-651">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| File System 函數 \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)" ) </span><span class="sxs-lookup"><span data-stu-id="2e999-651">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="2e999-652">CD-ROM 光碟機中媒體的音量序號。</span><span class="sxs-lookup"><span data-stu-id="2e999-652">Volume serial number of the media in the CD-ROM drive.</span></span>

<span data-ttu-id="2e999-653">範例： A8C3-D032</span><span class="sxs-lookup"><span data-stu-id="2e999-653">Example: A8C3-D032</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e999-654">備註</span><span class="sxs-lookup"><span data-stu-id="2e999-654">Remarks</span></span>

<span data-ttu-id="2e999-655">**Win32 \_ CDROMDrive** 類別衍生自 cim [**\_ CDROMDrive**](cim-cdromdrive.md) ，它衍生自 [**cim \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-655">The **Win32\_CDROMDrive** class is derived from [**CIM\_CDROMDrive**](cim-cdromdrive.md) which derives from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span> <span data-ttu-id="2e999-656">**Cim \_ MediaAccessDevice** 類別衍生自 [**cim \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2e999-656">The **CIM\_MediaAccessDevice** class derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2e999-657">範例</span><span class="sxs-lookup"><span data-stu-id="2e999-657">Examples</span></span>

<span data-ttu-id="2e999-658">下列 VBScript 範例會判斷 CD 是否在 CDROM 磁片磁碟機中。</span><span class="sxs-lookup"><span data-stu-id="2e999-658">The following VBScript example determines if a CD is in a CDROM drive.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject(_
    "winmgmts:\\" & strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery( _
    "Select * from Win32_CDROMDrive")
For Each objItem in colItems
    Wscript.Echo "Device ID: " _
        & objItem.DeviceID
    Wscript.Echo "Media Loaded: " _
        & objItem.MediaLoaded
Next
```



## <a name="requirements"></a><span data-ttu-id="2e999-659">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e999-659">Requirements</span></span>



| <span data-ttu-id="2e999-660">需求</span><span class="sxs-lookup"><span data-stu-id="2e999-660">Requirement</span></span> | <span data-ttu-id="2e999-661">值</span><span class="sxs-lookup"><span data-stu-id="2e999-661">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e999-662">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2e999-662">Minimum supported client</span></span><br/> | <span data-ttu-id="2e999-663">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e999-663">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2e999-664">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2e999-664">Minimum supported server</span></span><br/> | <span data-ttu-id="2e999-665">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e999-665">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2e999-666">命名空間</span><span class="sxs-lookup"><span data-stu-id="2e999-666">Namespace</span></span><br/>                | <span data-ttu-id="2e999-667">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2e999-667">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2e999-668">MOF</span><span class="sxs-lookup"><span data-stu-id="2e999-668">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e999-669"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e999-669"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e999-670">DLL</span><span class="sxs-lookup"><span data-stu-id="2e999-670">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e999-671"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e999-671"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e999-672">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e999-672">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e999-673">**CIM \_ CDROMDrive**</span><span class="sxs-lookup"><span data-stu-id="2e999-673">**CIM\_CDROMDrive**</span></span>](cim-cdromdrive.md)
</dt> <dt>

[<span data-ttu-id="2e999-674">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="2e999-674">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="2e999-675">WMI 工作：電腦硬體</span><span class="sxs-lookup"><span data-stu-id="2e999-675">WMI Tasks: Computer Hardware</span></span>](/windows/desktop/WmiSdk/wmi-tasks--computer-hardware)
</dt> <dt>

[<span data-ttu-id="2e999-676">WMI 工作：磁片和檔案系統</span><span class="sxs-lookup"><span data-stu-id="2e999-676">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

