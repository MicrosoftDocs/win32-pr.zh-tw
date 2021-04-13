---
description: 代表執行 Windows 作業系統的電腦所見的實體磁片磁碟機。
ms.assetid: c1fc6a1e-e725-484b-aacf-279f777e9b19
ms.tgt_platform: multiple
title: Win32_DiskDrive 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskDrive
- Win32_DiskDrive.Reset
- Win32_DiskDrive.SetPowerState
- Win32_DiskDrive.Availability
- Win32_DiskDrive.BytesPerSector
- Win32_DiskDrive.Capabilities
- Win32_DiskDrive.CapabilityDescriptions
- Win32_DiskDrive.Caption
- Win32_DiskDrive.CompressionMethod
- Win32_DiskDrive.ConfigManagerErrorCode
- Win32_DiskDrive.ConfigManagerUserConfig
- Win32_DiskDrive.CreationClassName
- Win32_DiskDrive.DefaultBlockSize
- Win32_DiskDrive.Description
- Win32_DiskDrive.DeviceID
- Win32_DiskDrive.ErrorCleared
- Win32_DiskDrive.ErrorDescription
- Win32_DiskDrive.ErrorMethodology
- Win32_DiskDrive.FirmwareRevision
- Win32_DiskDrive.Index
- Win32_DiskDrive.InstallDate
- Win32_DiskDrive.InterfaceType
- Win32_DiskDrive.LastErrorCode
- Win32_DiskDrive.Manufacturer
- Win32_DiskDrive.MaxBlockSize
- Win32_DiskDrive.MaxMediaSize
- Win32_DiskDrive.MediaLoaded
- Win32_DiskDrive.MediaType
- Win32_DiskDrive.MinBlockSize
- Win32_DiskDrive.Model
- Win32_DiskDrive.Name
- Win32_DiskDrive.NeedsCleaning
- Win32_DiskDrive.NumberOfMediaSupported
- Win32_DiskDrive.Partitions
- Win32_DiskDrive.PNPDeviceID
- Win32_DiskDrive.PowerManagementCapabilities
- Win32_DiskDrive.PowerManagementSupported
- Win32_DiskDrive.SCSIBus
- Win32_DiskDrive.SCSILogicalUnit
- Win32_DiskDrive.SCSIPort
- Win32_DiskDrive.SCSITargetId
- Win32_DiskDrive.SectorsPerTrack
- Win32_DiskDrive.SerialNumber
- Win32_DiskDrive.Signature
- Win32_DiskDrive.Size
- Win32_DiskDrive.Status
- Win32_DiskDrive.StatusInfo
- Win32_DiskDrive.SystemCreationClassName
- Win32_DiskDrive.SystemName
- Win32_DiskDrive.TotalCylinders
- Win32_DiskDrive.TotalHeads
- Win32_DiskDrive.TotalSectors
- Win32_DiskDrive.TotalTracks
- Win32_DiskDrive.TracksPerCylinder
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 751dee053574be417cb312f6b046ae6b7703d543
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510657"
---
# <a name="win32_diskdrive-class"></a><span data-ttu-id="10077-103">Win32 \_ DiskDrive 類別</span><span class="sxs-lookup"><span data-stu-id="10077-103">Win32\_DiskDrive class</span></span>

<span data-ttu-id="10077-104">**Win32 \_ DiskDrive** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表執行 Windows 作業系統的電腦所見的實體磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="10077-104">The **Win32\_DiskDrive** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a physical disk drive as seen by a computer running the Windows operating system.</span></span>

<span data-ttu-id="10077-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="10077-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="10077-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="10077-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="10077-107">語法</span><span class="sxs-lookup"><span data-stu-id="10077-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskDrive : CIM_DiskDrive
{
  uint16   Availability;
  uint32   BytesPerSector;
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
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  string   FirmwareRevision;
  uint32   Index;
  datetime InstallDate;
  string   InterfaceType;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  boolean  MediaLoaded;
  string   MediaType;
  uint64   MinBlockSize;
  string   Model;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  uint32   Partitions;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   SCSIBus;
  uint16   SCSILogicalUnit;
  uint16   SCSIPort;
  uint16   SCSITargetId;
  uint32   SectorsPerTrack;
  string   SerialNumber;
  uint32   Signature;
  uint64   Size;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint64   TotalCylinders;
  uint32   TotalHeads;
  uint64   TotalSectors;
  uint64   TotalTracks;
  uint32   TracksPerCylinder;
};
```

## <a name="members"></a><span data-ttu-id="10077-108">成員</span><span class="sxs-lookup"><span data-stu-id="10077-108">Members</span></span>

<span data-ttu-id="10077-109">**Win32 \_ DiskDrive** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="10077-109">The **Win32\_DiskDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="10077-110">方法</span><span class="sxs-lookup"><span data-stu-id="10077-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="10077-111">屬性</span><span class="sxs-lookup"><span data-stu-id="10077-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="10077-112">方法</span><span class="sxs-lookup"><span data-stu-id="10077-112">Methods</span></span>

<span data-ttu-id="10077-113">**Win32 \_ DiskDrive** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="10077-113">The **Win32\_DiskDrive** class has these methods.</span></span>



| <span data-ttu-id="10077-114">方法</span><span class="sxs-lookup"><span data-stu-id="10077-114">Method</span></span>            | <span data-ttu-id="10077-115">描述</span><span class="sxs-lookup"><span data-stu-id="10077-115">Description</span></span>                                                                                                                                                                                              |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10077-116">**重設**</span><span class="sxs-lookup"><span data-stu-id="10077-116">**Reset**</span></span>         | <span data-ttu-id="10077-117">未實作。</span><span class="sxs-lookup"><span data-stu-id="10077-117">Not implemented.</span></span> <span data-ttu-id="10077-118">若要執行此方法，請參閱 [**CIM \_ DiskDrive**](cim-diskdrive.md)中的 [**Reset**](reset-method-in-class-cim-controller.md)方法以取得檔。</span><span class="sxs-lookup"><span data-stu-id="10077-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_DiskDrive**](cim-diskdrive.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="10077-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="10077-119">**SetPowerState**</span></span> | <span data-ttu-id="10077-120">未實作。</span><span class="sxs-lookup"><span data-stu-id="10077-120">Not implemented.</span></span> <span data-ttu-id="10077-121">若要執行此方法，請參閱 [**CIM \_ DiskDrive**](cim-diskdrive.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法，以取得檔。</span><span class="sxs-lookup"><span data-stu-id="10077-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_DiskDrive**](cim-diskdrive.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="10077-122">屬性</span><span class="sxs-lookup"><span data-stu-id="10077-122">Properties</span></span>

<span data-ttu-id="10077-123">**Win32 \_ DiskDrive** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="10077-123">The **Win32\_DiskDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="10077-124">**可用性**</span><span class="sxs-lookup"><span data-stu-id="10077-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-125">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="10077-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10077-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-127">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="10077-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="10077-128">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="10077-128">Availability and status of the device.</span></span>

<span data-ttu-id="10077-129">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10077-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="10077-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10077-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="10077-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="10077-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="10077-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="10077-133">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="10077-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="10077-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="10077-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="10077-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="10077-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="10077-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="10077-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="10077-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="10077-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="10077-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="10077-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="10077-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="10077-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="10077-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="10077-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="10077-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="10077-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="10077-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="10077-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="10077-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="10077-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="10077-144">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="10077-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="10077-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="10077-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="10077-146">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="10077-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="10077-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="10077-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="10077-148">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="10077-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="10077-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="10077-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="10077-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="10077-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="10077-151">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="10077-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="10077-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="10077-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="10077-153"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="10077-153"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="10077-154"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="10077-154"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="10077-155"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="10077-155"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="10077-156">磁片磁碟機無法使用。</span><span class="sxs-lookup"><span data-stu-id="10077-156">The disk drive is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="10077-157">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="10077-157">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-158">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="10077-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10077-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-160">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 裝置輸入和輸出結構 \| [**磁片 \_ 幾何**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| BytesPerSector」 ) ，[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「位元組」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|BytesPerSector"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="10077-161">每個磁區中實體磁片磁碟機的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="10077-161">Number of bytes in each sector for the physical disk drive.</span></span>

<span data-ttu-id="10077-162">範例：512</span><span class="sxs-lookup"><span data-stu-id="10077-162">Example: 512</span></span>

</dd> <dt>

<span data-ttu-id="10077-163">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="10077-163">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-164">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="10077-164">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="10077-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-166">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 儲存裝置 \| 001.9 "，" MIF。DMTF \| 儲存裝置 \| 001.11 "，" MIF。DMTF \| 儲存裝置 \| 001.12 "，" MIF。DMTF \| 磁片 \| 003.7 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。**CapabilityDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="10077-166">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="10077-167">媒體存取裝置的功能陣列。</span><span class="sxs-lookup"><span data-stu-id="10077-167">Array of capabilities of the media access device.</span></span> <span data-ttu-id="10077-168">例如，裝置可能支援隨機存取 (3) 、卸載式媒體 (7) ，以及自動清除 (9) 。</span><span class="sxs-lookup"><span data-stu-id="10077-168">For example, the device may support random access (3), removable media (7), and automatic cleaning (9).</span></span>

<span data-ttu-id="10077-169">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-169">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10077-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="10077-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10077-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="10077-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="10077-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**順序存取** (2) </span><span class="sxs-lookup"><span data-stu-id="10077-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="10077-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**隨機存取** (3) </span><span class="sxs-lookup"><span data-stu-id="10077-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="10077-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**支援寫入** (4) </span><span class="sxs-lookup"><span data-stu-id="10077-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="10077-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**加密** (5) </span><span class="sxs-lookup"><span data-stu-id="10077-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="10077-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**壓縮** (6) </span><span class="sxs-lookup"><span data-stu-id="10077-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="10077-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**支援卸除式媒體** (7) </span><span class="sxs-lookup"><span data-stu-id="10077-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="10077-178">支援卸載式媒體</span><span class="sxs-lookup"><span data-stu-id="10077-178">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="10077-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**手動清除** (8) </span><span class="sxs-lookup"><span data-stu-id="10077-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="10077-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**自動清除** (9) </span><span class="sxs-lookup"><span data-stu-id="10077-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="10077-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**智慧型通知** (10) </span><span class="sxs-lookup"><span data-stu-id="10077-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="10077-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**支援雙側媒體** (11) </span><span class="sxs-lookup"><span data-stu-id="10077-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="10077-183">支援 Dual-Sided 媒體</span><span class="sxs-lookup"><span data-stu-id="10077-183">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="10077-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**不需要 Predismount 退出** (12) </span><span class="sxs-lookup"><span data-stu-id="10077-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="10077-185">不需要卸載磁片磁碟機之前先彈出</span><span class="sxs-lookup"><span data-stu-id="10077-185">Ejection Prior to Drive Dismount Not Required</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="10077-186">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="10077-186">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-187">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="10077-187">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="10077-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-189">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。**功能**") </span><span class="sxs-lookup"><span data-stu-id="10077-189">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="10077-190">**功能** 陣列中所指出的任何存取裝置功能的詳細說明清單。</span><span class="sxs-lookup"><span data-stu-id="10077-190">List of more detailed explanations for any of the access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="10077-191">請注意，這個陣列的每個專案都與位於相同索引的 **功能** 陣列中的專案相關。</span><span class="sxs-lookup"><span data-stu-id="10077-191">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="10077-192">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-192">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10077-193">**標題**</span><span class="sxs-lookup"><span data-stu-id="10077-193">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-194">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10077-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10077-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-196">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="10077-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="10077-197">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="10077-197">Short description of the object.</span></span>

<span data-ttu-id="10077-198">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="10077-199">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="10077-199">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-200">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10077-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10077-201">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10077-202">裝置用來支援壓縮的演算法或工具。</span><span class="sxs-lookup"><span data-stu-id="10077-202">Algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="10077-203">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-203">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="10077-204">壓縮演算法的名稱，或下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="10077-204">The name of the compression algorithm or one of the following values.</span></span>

<dt>



 <span data-ttu-id="10077-205"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-205">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="10077-206">裝置是否支援壓縮功能，但不知道。</span><span class="sxs-lookup"><span data-stu-id="10077-206">Whether the device supports compression capabilities or not is not known.</span></span>

</dd> <dt>



 <span data-ttu-id="10077-207"> ( 「壓縮」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-207">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="10077-208">裝置支援壓縮功能，但其壓縮配置未知或未公開。</span><span class="sxs-lookup"><span data-stu-id="10077-208">The device supports compression capabilities but its compression scheme is not known or not disclosed.</span></span>

</dd> <dt>



 <span data-ttu-id="10077-209"> ( 「未壓縮」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-209">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="10077-210">裝置不支援壓縮。</span><span class="sxs-lookup"><span data-stu-id="10077-210">The device does not support compression.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="10077-211">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="10077-211">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-212">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="10077-212">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10077-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-214">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="10077-214">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="10077-215">Windows 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="10077-215">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="10077-216">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-216">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="10077-217"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="10077-217"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="10077-218"> (0)</span><span class="sxs-lookup"><span data-stu-id="10077-218">(0)</span></span>


</dt> <dd>

<span data-ttu-id="10077-219">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="10077-219">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="10077-220"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="10077-220"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="10077-221">(1)</span><span class="sxs-lookup"><span data-stu-id="10077-221">(1)</span></span>


</dt> <dd>

<span data-ttu-id="10077-222">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="10077-222">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="10077-223"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="10077-223"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="10077-224">(2)</span><span class="sxs-lookup"><span data-stu-id="10077-224">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="10077-225"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="10077-225"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="10077-226">(3)</span><span class="sxs-lookup"><span data-stu-id="10077-226">(3)</span></span>


</dt> <dd>

<span data-ttu-id="10077-227">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="10077-227">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="10077-228"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="10077-228"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="10077-229">(4)</span><span class="sxs-lookup"><span data-stu-id="10077-229">(4)</span></span>


</dt> <dd>

<span data-ttu-id="10077-230">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="10077-230">Device is not working properly.</span></span> <span data-ttu-id="10077-231">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="10077-231">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="10077-232"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="10077-232"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="10077-233">(5)</span><span class="sxs-lookup"><span data-stu-id="10077-233">(5)</span></span>


</dt> <dd>

<span data-ttu-id="10077-234">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="10077-234">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="10077-235"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="10077-235"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="10077-236">(6)</span><span class="sxs-lookup"><span data-stu-id="10077-236">(6)</span></span>


</dt> <dd>

<span data-ttu-id="10077-237">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="10077-237">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="10077-238"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="10077-238"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="10077-239">(7)</span><span class="sxs-lookup"><span data-stu-id="10077-239">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="10077-240"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="10077-240"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="10077-241">(8)</span><span class="sxs-lookup"><span data-stu-id="10077-241">(8)</span></span>


</dt> <dd>

<span data-ttu-id="10077-242">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="10077-242">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="10077-243"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="10077-243"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="10077-244">(9)</span><span class="sxs-lookup"><span data-stu-id="10077-244">(9)</span></span>


</dt> <dd>

<span data-ttu-id="10077-245">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="10077-245">Device is not working properly.</span></span> <span data-ttu-id="10077-246">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="10077-246">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="10077-247"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="10077-247"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="10077-248">(10)</span><span class="sxs-lookup"><span data-stu-id="10077-248">(10)</span></span>


</dt> <dd>

<span data-ttu-id="10077-249">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="10077-249">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="10077-250"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="10077-250"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="10077-251">(11)</span><span class="sxs-lookup"><span data-stu-id="10077-251">(11)</span></span>


</dt> <dd>

<span data-ttu-id="10077-252">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="10077-252">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="10077-253"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="10077-253"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="10077-254"> (12) </span><span class="sxs-lookup"><span data-stu-id="10077-254">(12)</span></span>


</dt> <dd>

<span data-ttu-id="10077-255">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="10077-255">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="10077-256"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="10077-256"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="10077-257">(13)</span><span class="sxs-lookup"><span data-stu-id="10077-257">(13)</span></span>


</dt> <dd>

<span data-ttu-id="10077-258">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="10077-258">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="10077-259"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="10077-259"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="10077-260">(14)</span><span class="sxs-lookup"><span data-stu-id="10077-260">(14)</span></span>


</dt> <dd>

<span data-ttu-id="10077-261">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="10077-261">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="10077-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="10077-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="10077-263">(15)</span><span class="sxs-lookup"><span data-stu-id="10077-263">(15)</span></span>


</dt> <dd>

<span data-ttu-id="10077-264">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="10077-264">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="10077-265"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="10077-265"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="10077-266">(16)</span><span class="sxs-lookup"><span data-stu-id="10077-266">(16)</span></span>


</dt> <dd>

<span data-ttu-id="10077-267">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="10077-267">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="10077-268"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="10077-268"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="10077-269">(17)</span><span class="sxs-lookup"><span data-stu-id="10077-269">(17)</span></span>


</dt> <dd>

<span data-ttu-id="10077-270">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="10077-270">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="10077-271"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="10077-271"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="10077-272">(18)</span><span class="sxs-lookup"><span data-stu-id="10077-272">(18)</span></span>


</dt> <dd>

<span data-ttu-id="10077-273">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="10077-273">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="10077-274"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="10077-274"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="10077-275">(19)</span><span class="sxs-lookup"><span data-stu-id="10077-275">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="10077-276"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="10077-276"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="10077-277">(20)</span><span class="sxs-lookup"><span data-stu-id="10077-277">(20)</span></span>


</dt> <dd>

<span data-ttu-id="10077-278">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="10077-278">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="10077-279"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="10077-279"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="10077-280">(21)</span><span class="sxs-lookup"><span data-stu-id="10077-280">(21)</span></span>


</dt> <dd>

<span data-ttu-id="10077-281">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="10077-281">System failure.</span></span> <span data-ttu-id="10077-282">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="10077-282">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="10077-283">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="10077-283">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="10077-284"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="10077-284"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="10077-285">(22)</span><span class="sxs-lookup"><span data-stu-id="10077-285">(22)</span></span>


</dt> <dd>

<span data-ttu-id="10077-286">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="10077-286">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="10077-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="10077-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="10077-288">(23)</span><span class="sxs-lookup"><span data-stu-id="10077-288">(23)</span></span>


</dt> <dd>

<span data-ttu-id="10077-289">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="10077-289">System failure.</span></span> <span data-ttu-id="10077-290">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="10077-290">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="10077-291"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="10077-291"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="10077-292">(24)</span><span class="sxs-lookup"><span data-stu-id="10077-292">(24)</span></span>


</dt> <dd>

<span data-ttu-id="10077-293">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="10077-293">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="10077-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="10077-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="10077-295">(25)</span><span class="sxs-lookup"><span data-stu-id="10077-295">(25)</span></span>


</dt> <dd>

<span data-ttu-id="10077-296">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="10077-296">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="10077-297"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="10077-297"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="10077-298">(26)</span><span class="sxs-lookup"><span data-stu-id="10077-298">(26)</span></span>


</dt> <dd>

<span data-ttu-id="10077-299">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="10077-299">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="10077-300"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="10077-300"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="10077-301">(27)</span><span class="sxs-lookup"><span data-stu-id="10077-301">(27)</span></span>


</dt> <dd>

<span data-ttu-id="10077-302">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="10077-302">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="10077-303"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="10077-303"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="10077-304">(28)</span><span class="sxs-lookup"><span data-stu-id="10077-304">(28)</span></span>


</dt> <dd>

<span data-ttu-id="10077-305">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="10077-305">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="10077-306"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="10077-306"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="10077-307">(29)</span><span class="sxs-lookup"><span data-stu-id="10077-307">(29)</span></span>


</dt> <dd>

<span data-ttu-id="10077-308">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="10077-308">Device is disabled.</span></span> <span data-ttu-id="10077-309">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="10077-309">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="10077-310"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="10077-310"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="10077-311">(30)</span><span class="sxs-lookup"><span data-stu-id="10077-311">(30)</span></span>


</dt> <dd>

<span data-ttu-id="10077-312">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="10077-312">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="10077-313"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="10077-313"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="10077-314"> (31) </span><span class="sxs-lookup"><span data-stu-id="10077-314">(31)</span></span>


</dt> <dd>

<span data-ttu-id="10077-315">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="10077-315">Device is not working properly.</span></span> <span data-ttu-id="10077-316">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="10077-316">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="10077-317">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="10077-317">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-318">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="10077-318">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10077-319">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-320">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="10077-320">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="10077-321">若 **為 True**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="10077-321">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="10077-322">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10077-323">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="10077-323">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-324">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10077-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10077-325">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-326">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="10077-326">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="10077-327">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="10077-327">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="10077-328">搭配類別的其他索引鍵屬性使用時，屬性可讓這個類別的所有實例和其子類別都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="10077-328">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="10077-329">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10077-330">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="10077-330">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-331">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="10077-331">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="10077-332">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-333">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="10077-333">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="10077-334">此裝置的預設區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="10077-334">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="10077-335">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-335">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="10077-336">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="10077-336">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="10077-337">**說明**</span><span class="sxs-lookup"><span data-stu-id="10077-337">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-338">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10077-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10077-339">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-340">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="10077-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="10077-341">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="10077-341">Description of the object.</span></span>

<span data-ttu-id="10077-342">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="10077-343">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="10077-343">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-344">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10077-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10077-345">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-346">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "DeviceId" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="10077-346">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="10077-347">系統上其他裝置之磁片磁碟機的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="10077-347">Unique identifier of the disk drive with other devices on the system.</span></span>

<span data-ttu-id="10077-348">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-348">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10077-349">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="10077-349">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-350">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="10077-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10077-351">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10077-352">若 **為 True**，則表示 **LastErrorCode** 中回報的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="10077-352">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="10077-353">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-353">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10077-354">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="10077-354">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-355">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10077-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10077-356">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10077-357">有關 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="10077-357">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="10077-358">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-358">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10077-359">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="10077-359">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-360">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10077-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10077-361">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10077-362">此裝置支援的錯誤偵測和修正類型。</span><span class="sxs-lookup"><span data-stu-id="10077-362">Type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="10077-363">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-363">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10077-364">**FirmwareRevision**</span><span class="sxs-lookup"><span data-stu-id="10077-364">**FirmwareRevision**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-365">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10077-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10077-366">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-367">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 裝置輸入和輸出結構 \| [**儲存 \_ 裝置 \_ 描述**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)項 \| ProductRevisionOffset」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-367">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|ProductRevisionOffset")</span></span>
</dt> </dl>

<span data-ttu-id="10077-368">製造商所指派之磁片磁碟機固件的修訂。</span><span class="sxs-lookup"><span data-stu-id="10077-368">Revision for the disk drive firmware that is assigned by the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="10077-369">**Index**</span><span class="sxs-lookup"><span data-stu-id="10077-369">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-370">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="10077-370">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10077-371">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-372">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Windows 95/98 函式 \| 磁片磁碟機 \_ MAP \_ INFO \| btInt13Unit" ) </span><span class="sxs-lookup"><span data-stu-id="10077-372">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Windows 95/98 Functions\|DRIVE\_MAP\_INFO\|btInt13Unit")</span></span>
</dt> </dl>

<span data-ttu-id="10077-373">指定磁片磁碟機的實體磁片磁碟機編號。</span><span class="sxs-lookup"><span data-stu-id="10077-373">Physical drive number of the given drive.</span></span> <span data-ttu-id="10077-374">這個屬性會填入從 [**IOCTL \_ 儲存體 \_ 取得 \_ 裝置 \_ 編號**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_get_device_number)控制程式代碼傳回的 [**儲存 \_ 裝置 \_ 編號**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_number)結構。</span><span class="sxs-lookup"><span data-stu-id="10077-374">This property is filled by the [**STORAGE\_DEVICE\_NUMBER**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_number) structure returned from the [**IOCTL\_STORAGE\_GET\_DEVICE\_NUMBER**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_get_device_number) control code.</span></span> <span data-ttu-id="10077-375">0xffffffff 的值表示指定的磁片磁碟機不會對應至實體磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="10077-375">A value of 0xffffffff indicates that the given drive does not map to a physical drive.</span></span>

<span data-ttu-id="10077-376">範例：1</span><span class="sxs-lookup"><span data-stu-id="10077-376">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="10077-377">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="10077-377">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-378">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="10077-378">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="10077-379">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-379">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-380">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="10077-380">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="10077-381">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="10077-381">Date and time the object was installed.</span></span> <span data-ttu-id="10077-382">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="10077-382">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="10077-383">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-383">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="10077-384">**InterfaceType**</span><span class="sxs-lookup"><span data-stu-id="10077-384">**InterfaceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-385">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10077-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10077-386">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-387">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Device Input and Output 函數 \| [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)" ) </span><span class="sxs-lookup"><span data-stu-id="10077-387">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Functions\|[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)")</span></span>
</dt> </dl>

<span data-ttu-id="10077-388">實體磁片磁碟機的介面類別型。</span><span class="sxs-lookup"><span data-stu-id="10077-388">Interface type of physical disk drive.</span></span>

<span data-ttu-id="10077-389">值如下：</span><span class="sxs-lookup"><span data-stu-id="10077-389">The values are:</span></span>

<span data-ttu-id="10077-390">SCSI</span><span class="sxs-lookup"><span data-stu-id="10077-390">SCSI</span></span>

<span data-ttu-id="10077-391">HDC</span><span class="sxs-lookup"><span data-stu-id="10077-391">HDC</span></span>

<span data-ttu-id="10077-392">IDE</span><span class="sxs-lookup"><span data-stu-id="10077-392">IDE</span></span>

<span data-ttu-id="10077-393">USB</span><span class="sxs-lookup"><span data-stu-id="10077-393">USB</span></span>

<span data-ttu-id="10077-394">1394</span><span class="sxs-lookup"><span data-stu-id="10077-394">1394</span></span>

</dd> <dt>

<span data-ttu-id="10077-395">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="10077-395">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-396">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="10077-396">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10077-397">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10077-398">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="10077-398">Last error code reported by the logical device.</span></span>

<span data-ttu-id="10077-399">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-399">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10077-400">**製造商**</span><span class="sxs-lookup"><span data-stu-id="10077-400">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-401">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10077-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10077-402">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-403">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ 硬體 \\ \\ DEVICEMAP \\ \\ Scsi \\ \\ scsi 埠 \\ \\ Scsi Bus \\ \\ Target id \\ \\ 邏輯單元識別碼 \\ \\ "，"Win32Registry \| 製造商" ) </span><span class="sxs-lookup"><span data-stu-id="10077-403">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\HARDWARE\\\\DEVICEMAP\\\\Scsi\\\\Scsi Port\\\\Scsi Bus\\\\Target Id\\\\Logical Unit Id\\\\Identifier", "Win32Registry\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="10077-404">磁片磁碟機製造商的名稱。</span><span class="sxs-lookup"><span data-stu-id="10077-404">Name of the disk drive manufacturer.</span></span>

<span data-ttu-id="10077-405">範例： "Seagate"</span><span class="sxs-lookup"><span data-stu-id="10077-405">Example: "Seagate"</span></span>

</dd> <dt>

<span data-ttu-id="10077-406">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="10077-406">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-407">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="10077-407">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="10077-408">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-409">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="10077-409">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="10077-410">此裝置所存取媒體的最大區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="10077-410">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="10077-411">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-411">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="10077-412">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="10077-412">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="10077-413">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="10077-413">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-414">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="10077-414">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="10077-415">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-416">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 順序存取裝置 \| 001.2 「) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「kb」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-416">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="10077-417">此裝置支援的媒體大小上限（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="10077-417">Maximum media size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="10077-418">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-418">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="10077-419">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="10077-419">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="10077-420">**MediaLoaded**</span><span class="sxs-lookup"><span data-stu-id="10077-420">**MediaLoaded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-421">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="10077-421">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10077-422">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-423">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 裝置輸入和輸出結構 \| [**磁片 \_ 幾何媒體空間**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| FixedMedia」 \| ) </span><span class="sxs-lookup"><span data-stu-id="10077-423">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|MediaType\|FixedMedia")</span></span>
</dt> </dl>

<span data-ttu-id="10077-424">若為 **True**，則表示磁片磁碟機的媒體已載入，這表示裝置具有可讀取的檔案系統，且可供存取。</span><span class="sxs-lookup"><span data-stu-id="10077-424">If **True**, the media for a disk drive is loaded, which means that the device has a readable file system and is accessible.</span></span> <span data-ttu-id="10077-425">若為固定磁片磁碟機，此屬性一律為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="10077-425">For fixed disk drives, this property will always be **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="10077-426">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="10077-426">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-427">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10077-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10077-428">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-429">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 裝置輸入和輸出結構 \| [**磁片 \_ 幾何**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| 媒體媒體媒體媒體空間」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-429">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|MediaType")</span></span>
</dt> </dl>

<span data-ttu-id="10077-430">此裝置使用或存取的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="10077-430">Type of media used or accessed by this device.</span></span>

<span data-ttu-id="10077-431">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="10077-431">Possible values are:</span></span>

<dt>

<span id="External_hard_disk_media"></span><span id="external_hard_disk_media"></span><span id="EXTERNAL_HARD_DISK_MEDIA"></span>

<span data-ttu-id="10077-432">**外部硬碟媒體**</span><span class="sxs-lookup"><span data-stu-id="10077-432">**External hard disk media**</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_media"></span><span id="removable_media"></span><span id="REMOVABLE_MEDIA"></span>

<span data-ttu-id="10077-433">卸載式 **媒體** ( 「軟碟以外的卸載式媒體」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-433">**Removable media** ("Removable media other than floppy")</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_hard_disk"></span><span id="fixed_hard_disk"></span><span id="FIXED_HARD_DISK"></span>

<span data-ttu-id="10077-434">**硬碟** ( 固定硬碟媒體] ) </span><span class="sxs-lookup"><span data-stu-id="10077-434">**Fixed hard disk** ("Fixed hard disk media")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10077-435">**未知** 的 ( "格式不明" ) </span><span class="sxs-lookup"><span data-stu-id="10077-435">**Unknown** ("Format is unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10077-436">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="10077-436">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-437">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="10077-437">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="10077-438">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-438">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-439">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="10077-439">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="10077-440">此裝置所存取媒體的區塊大小下限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="10077-440">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="10077-441">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-441">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="10077-442">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="10077-442">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="10077-443">**型號**</span><span class="sxs-lookup"><span data-stu-id="10077-443">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-444">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10077-444">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10077-445">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-445">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-446">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ 硬體 \\ \\ DEVICEMAP \\ \\ Scsi \\ \\ scsi 埠 \\ \\ Scsi Bus \\ \\ Target id \\ \\ 邏輯單元識別碼 \\ \\ "，"Win32Registry \| ProductId" ) </span><span class="sxs-lookup"><span data-stu-id="10077-446">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\HARDWARE\\\\DEVICEMAP\\\\Scsi\\\\Scsi Port\\\\Scsi Bus\\\\Target Id\\\\Logical Unit Id\\\\Identifier", "Win32Registry\|ProductId")</span></span>
</dt> </dl>

<span data-ttu-id="10077-447">製造商的磁片磁碟機型號編號。</span><span class="sxs-lookup"><span data-stu-id="10077-447">Manufacturer's model number of the disk drive.</span></span>

<span data-ttu-id="10077-448">範例： "ST32171W"</span><span class="sxs-lookup"><span data-stu-id="10077-448">Example: "ST32171W"</span></span>

</dd> <dt>

<span data-ttu-id="10077-449">**名稱**</span><span class="sxs-lookup"><span data-stu-id="10077-449">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-450">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10077-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10077-451">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-452">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="10077-452">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="10077-453">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="10077-453">Label by which the object is known.</span></span> <span data-ttu-id="10077-454">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="10077-454">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="10077-455">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-455">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="10077-456">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="10077-456">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-457">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="10077-457">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10077-458">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10077-459">若 **為 True**，則媒體存取裝置需要清除。</span><span class="sxs-lookup"><span data-stu-id="10077-459">If **True**, the media access device needs cleaning.</span></span> <span data-ttu-id="10077-460">在 [ **功能** ] 屬性中，是否可能指出手動或自動清除。</span><span class="sxs-lookup"><span data-stu-id="10077-460">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="10077-461">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-461">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10077-462">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="10077-462">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-463">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="10077-463">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10077-464">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-464">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10077-465">媒體存取裝置支援多個個別媒體) 時，可支援或插入 (媒體的數目上限。</span><span class="sxs-lookup"><span data-stu-id="10077-465">Maximum number of media which can be supported or inserted (when the media access device supports multiple individual media).</span></span>

<span data-ttu-id="10077-466">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-466">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10077-467">**分區**</span><span class="sxs-lookup"><span data-stu-id="10077-467">**Partitions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-468">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="10077-468">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10077-469">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-470">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 裝置輸入和輸出結構的資料 \| [**分割 \_ 資訊**](/windows/desktop/api/winioctl/ns-winioctl-partition_information) \| RecognizedPartition」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-470">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**PARTITION\_INFORMATION**](/windows/desktop/api/winioctl/ns-winioctl-partition_information)\|RecognizedPartition")</span></span>
</dt> </dl>

<span data-ttu-id="10077-471">此實體磁片磁碟機上作業系統可辨識的磁碟分割數目。</span><span class="sxs-lookup"><span data-stu-id="10077-471">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

<span data-ttu-id="10077-472">範例：2</span><span class="sxs-lookup"><span data-stu-id="10077-472">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="10077-473">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="10077-473">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-474">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10077-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10077-475">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-476">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="10077-476">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="10077-477">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="10077-477">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="10077-478">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="10077-479">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="10077-479">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="10077-480">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="10077-480">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-481">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="10077-481">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="10077-482">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-482">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10077-483">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="10077-483">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="10077-484">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="10077-484">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10077-485"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="10077-485"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="10077-486"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="10077-486"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="10077-487">此裝置不支援與電源相關的容量。</span><span class="sxs-lookup"><span data-stu-id="10077-487">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="10077-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="10077-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="10077-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="10077-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="10077-490">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="10077-490">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="10077-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="10077-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="10077-492">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="10077-492">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="10077-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="10077-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="10077-494">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="10077-494">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="10077-495">這個方法可在父 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="10077-495">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="10077-496">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="10077-496">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="10077-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="10077-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="10077-498">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="10077-498">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="10077-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="10077-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="10077-500">支援計時 Power-On</span><span class="sxs-lookup"><span data-stu-id="10077-500">Timed Power-On Supported</span></span>

<span data-ttu-id="10077-501">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="10077-501">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="10077-502">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="10077-502">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-503">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="10077-503">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10077-504">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10077-505">若 **為 True**，則裝置可以是電源管理 (可進入暫停模式，依此類推) 。</span><span class="sxs-lookup"><span data-stu-id="10077-505">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="10077-506">屬性不表示電源管理功能目前已啟用，只有邏輯裝置能夠進行電源管理。</span><span class="sxs-lookup"><span data-stu-id="10077-506">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="10077-507">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-507">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10077-508">**SCSIBus**</span><span class="sxs-lookup"><span data-stu-id="10077-508">**SCSIBus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-509">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="10077-509">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10077-510">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-510">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-511">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 裝置輸入和輸出結構 \| [**SCSI \_ 位址**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| PathId」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-511">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|PathId")</span></span>
</dt> </dl>

<span data-ttu-id="10077-512">磁片磁碟機的 SCSI 匯流排號碼。</span><span class="sxs-lookup"><span data-stu-id="10077-512">SCSI bus number of the disk drive.</span></span>

<span data-ttu-id="10077-513">範例：0</span><span class="sxs-lookup"><span data-stu-id="10077-513">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="10077-514">**SCSILogicalUnit**</span><span class="sxs-lookup"><span data-stu-id="10077-514">**SCSILogicalUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-515">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="10077-515">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10077-516">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-516">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-517">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 裝置輸入和輸出結構 \| [**SCSI \_ 位址**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| Lun」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-517">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|Lun")</span></span>
</dt> </dl>

<span data-ttu-id="10077-518">磁片磁碟機的 SCSI 邏輯單元編號 (LUN) 。</span><span class="sxs-lookup"><span data-stu-id="10077-518">SCSI logical unit number (LUN) of the disk drive.</span></span>

<span data-ttu-id="10077-519">範例：0</span><span class="sxs-lookup"><span data-stu-id="10077-519">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="10077-520">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="10077-520">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-521">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="10077-521">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10077-522">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-523">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 裝置輸入和輸出結構 \| [**SCSI \_ 位址**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| PortNumber」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-523">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|PortNumber")</span></span>
</dt> </dl>

<span data-ttu-id="10077-524">磁片磁碟機的 SCSI 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="10077-524">SCSI port number of the disk drive.</span></span>

<span data-ttu-id="10077-525">範例：0</span><span class="sxs-lookup"><span data-stu-id="10077-525">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="10077-526">**SCSITargetId**</span><span class="sxs-lookup"><span data-stu-id="10077-526">**SCSITargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-527">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="10077-527">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10077-528">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-528">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-529">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 裝置輸入和輸出結構 \| [**SCSI \_ 位址**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| TargetId」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-529">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|TargetId")</span></span>
</dt> </dl>

<span data-ttu-id="10077-530">磁片磁碟機的 SCSI 識別碼號碼。</span><span class="sxs-lookup"><span data-stu-id="10077-530">SCSI identifier number of the disk drive.</span></span>

<span data-ttu-id="10077-531">範例：0</span><span class="sxs-lookup"><span data-stu-id="10077-531">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="10077-532">**SectorsPerTrack**</span><span class="sxs-lookup"><span data-stu-id="10077-532">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-533">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="10077-533">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10077-534">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-534">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-535">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 裝置輸入和輸出結構 \| [**磁片 \_ 幾何**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| SectorsPerTrack」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-535">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|SectorsPerTrack")</span></span>
</dt> </dl>

<span data-ttu-id="10077-536">此實體磁片磁碟機每個播放軌中的磁區數目。</span><span class="sxs-lookup"><span data-stu-id="10077-536">Number of sectors in each track for this physical disk drive.</span></span>

<span data-ttu-id="10077-537">範例：63</span><span class="sxs-lookup"><span data-stu-id="10077-537">Example: 63</span></span>

</dd> <dt>

<span data-ttu-id="10077-538">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="10077-538">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-539">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10077-539">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10077-540">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-541">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 裝置輸入和輸出結構 \| [**儲存 \_ 裝置 \_ 描述**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)項 \| SerialNumberOffset」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-541">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|SerialNumberOffset")</span></span>
</dt> </dl>

<span data-ttu-id="10077-542">製造商配置用來識別實體媒體的號碼。</span><span class="sxs-lookup"><span data-stu-id="10077-542">Number allocated by the manufacturer to identify the physical media.</span></span>

<span data-ttu-id="10077-543">範例： WD-WM3493798728</span><span class="sxs-lookup"><span data-stu-id="10077-543">Example: WD-WM3493798728</span></span>

</dd> <dt>

<span data-ttu-id="10077-544">**簽名**</span><span class="sxs-lookup"><span data-stu-id="10077-544">**Signature**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-545">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="10077-545">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10077-546">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-546">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-547">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 裝置輸入和輸出結構 \| [**磁片磁碟機配置 \_ \_ 資訊**](/windows/desktop/api/winioctl/ns-winioctl-drive_layout_information)簽章」 \| ) </span><span class="sxs-lookup"><span data-stu-id="10077-547">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DRIVE\_LAYOUT\_INFORMATION**](/windows/desktop/api/winioctl/ns-winioctl-drive_layout_information)\|Signature")</span></span>
</dt> </dl>

<span data-ttu-id="10077-548">磁片識別。</span><span class="sxs-lookup"><span data-stu-id="10077-548">Disk identification.</span></span> <span data-ttu-id="10077-549">這個屬性可以用來識別共用資源。</span><span class="sxs-lookup"><span data-stu-id="10077-549">This property can be used to identify a shared resource.</span></span>

</dd> <dt>

<span data-ttu-id="10077-550">**大小**</span><span class="sxs-lookup"><span data-stu-id="10077-550">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-551">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="10077-551">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="10077-552">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-552">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-553">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 裝置輸入和輸出結構 \| [**磁片 \_ 幾何**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)」 ) ，[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「位元組」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-553">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="10077-554">磁片磁碟機的大小。</span><span class="sxs-lookup"><span data-stu-id="10077-554">Size of the disk drive.</span></span> <span data-ttu-id="10077-555">其計算方式是將柱面總數、每個圓柱中的追蹤、每個軌跡中的磁區，以及每個磁區中的位元組相乘。</span><span class="sxs-lookup"><span data-stu-id="10077-555">It is calculated by multiplying the total number of cylinders, tracks in each cylinder, sectors in each track, and bytes in each sector.</span></span>

<span data-ttu-id="10077-556">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="10077-556">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="10077-557">**狀態**</span><span class="sxs-lookup"><span data-stu-id="10077-557">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-558">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10077-558">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10077-559">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-559">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-560">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="10077-560">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="10077-561">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="10077-561">Current status of the object.</span></span> <span data-ttu-id="10077-562">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="10077-562">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="10077-563">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="10077-563">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="10077-564">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="10077-564">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="10077-565">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="10077-565">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="10077-566">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="10077-566">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="10077-567">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-567">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="10077-568">值為：</span><span class="sxs-lookup"><span data-stu-id="10077-568">Values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="10077-569">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="10077-569">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="10077-570">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-570">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="10077-571">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-571">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10077-572">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-572">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="10077-573">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-573">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="10077-574">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-574">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="10077-575">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-575">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="10077-576">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-576">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="10077-577">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-577">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="10077-578">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="10077-578">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="10077-579">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-579">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="10077-580">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-580">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10077-581">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="10077-581">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-582">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="10077-582">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10077-583">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-583">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-584">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="10077-584">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="10077-585">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="10077-585">State of the logical device.</span></span> <span data-ttu-id="10077-586">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="10077-586">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="10077-587">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-587">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10077-588">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="10077-588">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10077-589">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="10077-589">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="10077-590">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="10077-590">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="10077-591">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="10077-591">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="10077-592">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="10077-592">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10077-593">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="10077-593">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-594">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10077-594">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10077-595">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-595">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-596">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="10077-596">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="10077-597">範圍電腦之 **CreationClassName** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="10077-597">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="10077-598">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-598">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10077-599">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="10077-599">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-600">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10077-600">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10077-601">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-601">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-602">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="10077-602">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="10077-603">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="10077-603">Name of the scoping system.</span></span>

<span data-ttu-id="10077-604">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-604">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10077-605">**TotalCylinders**</span><span class="sxs-lookup"><span data-stu-id="10077-605">**TotalCylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-606">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="10077-606">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="10077-607">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-607">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-608">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 裝置輸入和輸出結構 \| [**磁片 \_ 幾何**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| 圓柱」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-608">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|Cylinders")</span></span>
</dt> </dl>

<span data-ttu-id="10077-609">實體磁片磁碟機上的圓柱總數。</span><span class="sxs-lookup"><span data-stu-id="10077-609">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="10077-610">注意：這個屬性的值是透過 BIOS 中斷13h 的擴充功能取得。</span><span class="sxs-lookup"><span data-stu-id="10077-610">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="10077-611">如果磁片磁碟機使用轉譯配置來支援高容量的磁片大小，則此值可能不正確。</span><span class="sxs-lookup"><span data-stu-id="10077-611">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="10077-612">請洽詢製造商取得準確的磁片磁碟機規格。</span><span class="sxs-lookup"><span data-stu-id="10077-612">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="10077-613">範例：657</span><span class="sxs-lookup"><span data-stu-id="10077-613">Example: 657</span></span>

<span data-ttu-id="10077-614">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="10077-614">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="10077-615">**TotalHeads**</span><span class="sxs-lookup"><span data-stu-id="10077-615">**TotalHeads**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-616">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="10077-616">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10077-617">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-617">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-618">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 裝置輸入和輸出結構 \| [**磁片 \_ 幾何**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| TracksPerCylinder」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-618">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|TracksPerCylinder")</span></span>
</dt> </dl>

<span data-ttu-id="10077-619">磁片磁碟機上的總標頭數目。</span><span class="sxs-lookup"><span data-stu-id="10077-619">Total number of heads on the disk drive.</span></span> <span data-ttu-id="10077-620">注意：這個屬性的值是透過 BIOS 中斷13h 的擴充功能取得。</span><span class="sxs-lookup"><span data-stu-id="10077-620">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="10077-621">如果磁片磁碟機使用轉譯配置來支援高容量的磁片大小，則此值可能不正確。</span><span class="sxs-lookup"><span data-stu-id="10077-621">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="10077-622">請洽詢製造商取得準確的磁片磁碟機規格。</span><span class="sxs-lookup"><span data-stu-id="10077-622">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="10077-623">**TotalSectors**</span><span class="sxs-lookup"><span data-stu-id="10077-623">**TotalSectors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-624">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="10077-624">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="10077-625">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-625">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-626">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 裝置輸入和輸出結構 \| [**磁片 \_ 幾何**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| SectorsPerTrack」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-626">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|SectorsPerTrack")</span></span>
</dt> </dl>

<span data-ttu-id="10077-627">實體磁片磁碟機上的磁區總數。</span><span class="sxs-lookup"><span data-stu-id="10077-627">Total number of sectors on the physical disk drive.</span></span> <span data-ttu-id="10077-628">注意：這個屬性的值是透過 BIOS 中斷13h 的擴充功能取得。</span><span class="sxs-lookup"><span data-stu-id="10077-628">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="10077-629">如果磁片磁碟機使用轉譯配置來支援高容量的磁片大小，則此值可能不正確。</span><span class="sxs-lookup"><span data-stu-id="10077-629">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="10077-630">請洽詢製造商取得準確的磁片磁碟機規格。</span><span class="sxs-lookup"><span data-stu-id="10077-630">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="10077-631">範例：2649024</span><span class="sxs-lookup"><span data-stu-id="10077-631">Example: 2649024</span></span>

<span data-ttu-id="10077-632">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="10077-632">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="10077-633">**TotalTracks**</span><span class="sxs-lookup"><span data-stu-id="10077-633">**TotalTracks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-634">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="10077-634">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="10077-635">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-635">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-636">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 裝置輸入和輸出結構 \| [**磁片 \_ 幾何**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| TracksPerCylinder」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-636">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|TracksPerCylinder")</span></span>
</dt> </dl>

<span data-ttu-id="10077-637">實體磁片磁碟機上的總追蹤數。</span><span class="sxs-lookup"><span data-stu-id="10077-637">Total number of tracks on the physical disk drive.</span></span> <span data-ttu-id="10077-638">注意：這個屬性的值是透過 BIOS 中斷13h 的擴充功能取得。</span><span class="sxs-lookup"><span data-stu-id="10077-638">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="10077-639">如果磁片磁碟機使用轉譯配置來支援高容量的磁片大小，則此值可能不正確。</span><span class="sxs-lookup"><span data-stu-id="10077-639">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="10077-640">請洽詢製造商取得準確的磁片磁碟機規格。</span><span class="sxs-lookup"><span data-stu-id="10077-640">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="10077-641">範例：42048</span><span class="sxs-lookup"><span data-stu-id="10077-641">Example: 42048</span></span>

<span data-ttu-id="10077-642">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="10077-642">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="10077-643">**TracksPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="10077-643">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10077-644">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="10077-644">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10077-645">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10077-645">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10077-646">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 裝置輸入和輸出結構 \| [**磁片 \_ 幾何**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| TracksPerCylinder」 ) </span><span class="sxs-lookup"><span data-stu-id="10077-646">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|TracksPerCylinder")</span></span>
</dt> </dl>

<span data-ttu-id="10077-647">實體磁片磁碟機上每個圓柱的曲目數目。</span><span class="sxs-lookup"><span data-stu-id="10077-647">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="10077-648">注意：這個屬性的值是透過 BIOS 中斷13h 的擴充功能取得。</span><span class="sxs-lookup"><span data-stu-id="10077-648">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="10077-649">如果磁片磁碟機使用轉譯配置來支援高容量的磁片大小，則此值可能不正確。</span><span class="sxs-lookup"><span data-stu-id="10077-649">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="10077-650">請洽詢製造商取得準確的磁片磁碟機規格。</span><span class="sxs-lookup"><span data-stu-id="10077-650">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="10077-651">範例：64</span><span class="sxs-lookup"><span data-stu-id="10077-651">Example: 64</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10077-652">備註</span><span class="sxs-lookup"><span data-stu-id="10077-652">Remarks</span></span>

<span data-ttu-id="10077-653">實體硬碟是任何運算環境中資訊的主要儲存媒體。</span><span class="sxs-lookup"><span data-stu-id="10077-653">Physical hard disk drives are the primary storage medium for information in any computing environment.</span></span> <span data-ttu-id="10077-654">雖然組織通常會使用磁帶機之類的裝置，以及用來封存資料的光碟磁片磁碟機，但這些裝置不適合用來儲存每日的使用者資料。</span><span class="sxs-lookup"><span data-stu-id="10077-654">Although organizations often use devices such as tape drives and compact disc drives for archiving data, these devices are not suited for day-to-day storage of user data.</span></span> <span data-ttu-id="10077-655">只有實體硬碟提供儲存資料和執行應用程式和作業系統所需的速度和易用性。</span><span class="sxs-lookup"><span data-stu-id="10077-655">Only physical hard disks offer the speed and ease of use required for storing data and for running applications and the operating system.</span></span>

<span data-ttu-id="10077-656">若要有效率地管理資料，請務必詳細清查您的所有實體磁片、其功能和容量。</span><span class="sxs-lookup"><span data-stu-id="10077-656">To efficiently manage data, it is important to have a detailed inventory of all your physical disks, their capabilities, and their capacities.</span></span> <span data-ttu-id="10077-657">您可以使用 **Win32 \_ DiskDrive** 類別來衍生這種類型的清查。</span><span class="sxs-lookup"><span data-stu-id="10077-657">You can use the **Win32\_DiskDrive** class to derive this type of inventory.</span></span>

<span data-ttu-id="10077-658">Windows 實體磁片磁碟機的任何介面都是此類別 (或成員) 的子系。</span><span class="sxs-lookup"><span data-stu-id="10077-658">Any interface to a Windows physical disk drive is a descendant (or member) of this class.</span></span> <span data-ttu-id="10077-659">透過此物件查看之磁片磁碟機的功能，會對應到磁片磁碟機的邏輯和管理特性。</span><span class="sxs-lookup"><span data-stu-id="10077-659">The features of the disk drive seen through this object correspond to the logical and management characteristics of the drive.</span></span> <span data-ttu-id="10077-660">在某些情況下，這可能不會反映裝置的實際實體特性。</span><span class="sxs-lookup"><span data-stu-id="10077-660">In some cases, this may not reflect the actual physical characteristics of the device.</span></span> <span data-ttu-id="10077-661">以其他邏輯裝置為基礎的任何物件都不會是此類別的成員。</span><span class="sxs-lookup"><span data-stu-id="10077-661">Any object based on another logical device would not be a member of this class.</span></span>

<span data-ttu-id="10077-662">基於安全性理由，從遠端電腦連接的使用者必須啟用 **SC \_ MANAGER \_ CONNECT** 許可權，才能列舉此類別。</span><span class="sxs-lookup"><span data-stu-id="10077-662">For security reasons, a user connecting from a remote computer must have the **SC\_MANAGER\_CONNECT** privilege enabled to be able to enumerate this class.</span></span> <span data-ttu-id="10077-663">如需詳細資訊，請參閱 [服務安全性和存取權限](/windows/desktop/Services/service-security-and-access-rights)。</span><span class="sxs-lookup"><span data-stu-id="10077-663">For more information, see [Service Security and Access Rights](/windows/desktop/Services/service-security-and-access-rights).</span></span>

<span data-ttu-id="10077-664">**Win32 \_ DiskDrive** 類別衍生自 cim [**\_ DiskDrive**](cim-diskdrive.md) ，它衍生自 [**cim \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-664">The **Win32\_DiskDrive** class is derived from [**CIM\_DiskDrive**](cim-diskdrive.md) which derives from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span> <span data-ttu-id="10077-665">**Cim \_ MediaAccessDevice** 類別衍生自 [**cim \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="10077-665">The **CIM\_MediaAccessDevice** class derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="10077-666">範例</span><span class="sxs-lookup"><span data-stu-id="10077-666">Examples</span></span>

<span data-ttu-id="10077-667">[伺服器清查報告-TechNet 資源庫上的 WMI & CIM PowerShell 程式](https://Gallery.TechNet.Microsoft.Com/Servers-Inventory-report-e79e2b24)代碼範例會使用許多類別（包括 **Win32 \_ DiskDrive**）來傳回伺服器狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="10077-667">The [Servers Inventory report-WMI & CIM](https://Gallery.TechNet.Microsoft.Com/Servers-Inventory-report-e79e2b24) PowerShell code example on TechNet Gallery uses a number of classes, including **Win32\_DiskDrive**, to return information about server status.</span></span>

<span data-ttu-id="10077-668">[使用 Win32 \_ DiskDrive 介面型別屬性](https://Gallery.TechNet.Microsoft.Com/Map-Drive-to-Drive-Letter-1fff91ad)PowerShell 程式碼範例將磁片磁碟機對應至磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="10077-668">The [Map Drive to Drive Letter Using the Win32\_DiskDrive Interface Type Property](https://Gallery.TechNet.Microsoft.Com/Map-Drive-to-Drive-Letter-1fff91ad) PowerShell code sample maps a drive to a drive letter.</span></span>

## <a name="requirements"></a><span data-ttu-id="10077-669">規格需求</span><span class="sxs-lookup"><span data-stu-id="10077-669">Requirements</span></span>



| <span data-ttu-id="10077-670">需求</span><span class="sxs-lookup"><span data-stu-id="10077-670">Requirement</span></span> | <span data-ttu-id="10077-671">值</span><span class="sxs-lookup"><span data-stu-id="10077-671">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10077-672">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10077-672">Minimum supported client</span></span><br/> | <span data-ttu-id="10077-673">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10077-673">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="10077-674">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10077-674">Minimum supported server</span></span><br/> | <span data-ttu-id="10077-675">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10077-675">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="10077-676">命名空間</span><span class="sxs-lookup"><span data-stu-id="10077-676">Namespace</span></span><br/>                | <span data-ttu-id="10077-677">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="10077-677">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="10077-678">MOF</span><span class="sxs-lookup"><span data-stu-id="10077-678">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10077-679"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="10077-679"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="10077-680">DLL</span><span class="sxs-lookup"><span data-stu-id="10077-680">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10077-681"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10077-681"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10077-682">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10077-682">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10077-683">**CIM \_ DiskDrive**</span><span class="sxs-lookup"><span data-stu-id="10077-683">**CIM\_DiskDrive**</span></span>](cim-diskdrive.md)
</dt> <dt>

[<span data-ttu-id="10077-684">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="10077-684">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="10077-685">WMI 工作：磁片和檔案系統</span><span class="sxs-lookup"><span data-stu-id="10077-685">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

