---
description: Win32 \_ MappedLogicalDisk &\# 32;WMI 類別代表網路儲存裝置，這些裝置會對應為電腦系統上的邏輯磁片。
ms.assetid: 5dd4b0eb-7872-4f2d-9c8b-ea03f7e2c16d
ms.tgt_platform: multiple
title: Win32_MappedLogicalDisk 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MappedLogicalDisk
- Win32_MappedLogicalDisk.Reset
- Win32_MappedLogicalDisk.SetPowerState
- Win32_MappedLogicalDisk.Access
- Win32_MappedLogicalDisk.Availability
- Win32_MappedLogicalDisk.BlockSize
- Win32_MappedLogicalDisk.Caption
- Win32_MappedLogicalDisk.Compressed
- Win32_MappedLogicalDisk.ConfigManagerErrorCode
- Win32_MappedLogicalDisk.ConfigManagerUserConfig
- Win32_MappedLogicalDisk.CreationClassName
- Win32_MappedLogicalDisk.Description
- Win32_MappedLogicalDisk.DeviceID
- Win32_MappedLogicalDisk.ErrorCleared
- Win32_MappedLogicalDisk.ErrorDescription
- Win32_MappedLogicalDisk.ErrorMethodology
- Win32_MappedLogicalDisk.FileSystem
- Win32_MappedLogicalDisk.FreeSpace
- Win32_MappedLogicalDisk.InstallDate
- Win32_MappedLogicalDisk.LastErrorCode
- Win32_MappedLogicalDisk.MaximumComponentLength
- Win32_MappedLogicalDisk.Name
- Win32_MappedLogicalDisk.NumberOfBlocks
- Win32_MappedLogicalDisk.PNPDeviceID
- Win32_MappedLogicalDisk.PowerManagementCapabilities
- Win32_MappedLogicalDisk.PowerManagementSupported
- Win32_MappedLogicalDisk.ProviderName
- Win32_MappedLogicalDisk.Purpose
- Win32_MappedLogicalDisk.QuotasDisabled
- Win32_MappedLogicalDisk.QuotasIncomplete
- Win32_MappedLogicalDisk.QuotasRebuilding
- Win32_MappedLogicalDisk.SessionID
- Win32_MappedLogicalDisk.Size
- Win32_MappedLogicalDisk.Status
- Win32_MappedLogicalDisk.StatusInfo
- Win32_MappedLogicalDisk.SupportsDiskQuotas
- Win32_MappedLogicalDisk.SupportsFileBasedCompression
- Win32_MappedLogicalDisk.SystemCreationClassName
- Win32_MappedLogicalDisk.SystemName
- Win32_MappedLogicalDisk.VolumeName
- Win32_MappedLogicalDisk.VolumeSerialNumber
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 75c3dfee876c34f36fd0b4cf0b59d3a61afcd75c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111488"
---
# <a name="win32_mappedlogicaldisk-class"></a><span data-ttu-id="c0b71-103">Win32 \_ MappedLogicalDisk 類別</span><span class="sxs-lookup"><span data-stu-id="c0b71-103">Win32\_MappedLogicalDisk class</span></span>

<span data-ttu-id="c0b71-104">**Win32 \_ MappedLogicalDisk** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表電腦系統上對應為邏輯磁片的網路存放裝置。</span><span class="sxs-lookup"><span data-stu-id="c0b71-104">The **Win32\_MappedLogicalDisk** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents network storage devices that are mapped as logical disks on the computer system.</span></span>

<span data-ttu-id="c0b71-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c0b71-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c0b71-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="c0b71-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0b71-107">語法</span><span class="sxs-lookup"><span data-stu-id="c0b71-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{BCF02FFE-5560-4de2-B419-272918693426}"), AMENDMENT]
class Win32_MappedLogicalDisk : CIM_LogicalDisk
{
  uint16   Access;
  uint16   Availability;
  uint64   BlockSize;
  string   Caption;
  boolean  Compressed;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  string   FileSystem;
  uint64   FreeSpace;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaximumComponentLength;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   ProviderName;
  string   Purpose;
  boolean  QuotasDisabled;
  boolean  QuotasIncomplete;
  boolean  QuotasRebuilding;
  string   SessionID;
  uint64   Size;
  string   Status;
  uint16   StatusInfo;
  boolean  SupportsDiskQuotas;
  boolean  SupportsFileBasedCompression;
  string   SystemCreationClassName;
  string   SystemName;
  string   VolumeName;
  string   VolumeSerialNumber;
};
```

## <a name="members"></a><span data-ttu-id="c0b71-108">成員</span><span class="sxs-lookup"><span data-stu-id="c0b71-108">Members</span></span>

<span data-ttu-id="c0b71-109">**Win32 \_ MappedLogicalDisk** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c0b71-109">The **Win32\_MappedLogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="c0b71-110">方法</span><span class="sxs-lookup"><span data-stu-id="c0b71-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="c0b71-111">屬性</span><span class="sxs-lookup"><span data-stu-id="c0b71-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c0b71-112">方法</span><span class="sxs-lookup"><span data-stu-id="c0b71-112">Methods</span></span>

<span data-ttu-id="c0b71-113">**Win32 \_ MappedLogicalDisk** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c0b71-113">The **Win32\_MappedLogicalDisk** class has these methods.</span></span>



| <span data-ttu-id="c0b71-114">方法</span><span class="sxs-lookup"><span data-stu-id="c0b71-114">Method</span></span>            | <span data-ttu-id="c0b71-115">描述</span><span class="sxs-lookup"><span data-stu-id="c0b71-115">Description</span></span>                                                                                                                                                                                |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0b71-116">**重設**</span><span class="sxs-lookup"><span data-stu-id="c0b71-116">**Reset**</span></span>         | <span data-ttu-id="c0b71-117">未實作。</span><span class="sxs-lookup"><span data-stu-id="c0b71-117">Not implemented.</span></span> <span data-ttu-id="c0b71-118">若要執行此方法，請參閱 [**CIM \_ LogicalDisk**](cim-logicaldisk.md)中的 [**Reset**](reset-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="c0b71-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span><br/>                 |
| <span data-ttu-id="c0b71-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c0b71-119">**SetPowerState**</span></span> | <span data-ttu-id="c0b71-120">未實作。</span><span class="sxs-lookup"><span data-stu-id="c0b71-120">Not implemented.</span></span> <span data-ttu-id="c0b71-121">若要執行此方法，請參閱 [**CIM \_ LogicalDisk**](cim-logicaldisk.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="c0b71-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c0b71-122">屬性</span><span class="sxs-lookup"><span data-stu-id="c0b71-122">Properties</span></span>

<span data-ttu-id="c0b71-123">**Win32 \_ MappedLogicalDisk** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c0b71-123">The **Win32\_MappedLogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c0b71-124">**存取**</span><span class="sxs-lookup"><span data-stu-id="c0b71-124">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-125">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c0b71-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-127">裝置存取狀態。</span><span class="sxs-lookup"><span data-stu-id="c0b71-127">Device access state.</span></span>

<span data-ttu-id="c0b71-128">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-128">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c0b71-129">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c0b71-129">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="c0b71-130">**可讀取** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="c0b71-130">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="c0b71-131">可 **寫入** (2) </span><span class="sxs-lookup"><span data-stu-id="c0b71-131">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="c0b71-132">支援 (3) 的 **讀取/寫入**</span><span class="sxs-lookup"><span data-stu-id="c0b71-132">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="c0b71-133">**撰寫一次** (4) </span><span class="sxs-lookup"><span data-stu-id="c0b71-133">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c0b71-134">**可用性**</span><span class="sxs-lookup"><span data-stu-id="c0b71-134">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-135">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c0b71-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-137">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="c0b71-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-138">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="c0b71-138">Availability and status of the device.</span></span>

<span data-ttu-id="c0b71-139">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-139">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c0b71-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c0b71-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c0b71-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="c0b71-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="c0b71-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="c0b71-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-143">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="c0b71-143">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="c0b71-144"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="c0b71-144"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="c0b71-145"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="c0b71-145"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c0b71-146"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="c0b71-146"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="c0b71-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="c0b71-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="c0b71-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="c0b71-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-149">離線</span><span class="sxs-lookup"><span data-stu-id="c0b71-149">Offline</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="c0b71-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="c0b71-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c0b71-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="c0b71-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="c0b71-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="c0b71-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="c0b71-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="c0b71-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="c0b71-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="c0b71-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-155">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="c0b71-155">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="c0b71-156"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="c0b71-156"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-157">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="c0b71-157">The device is in a power save state but still functioning and can exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="c0b71-158"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="c0b71-158"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-159">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="c0b71-159">The device is not functioning, but can be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="c0b71-160"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="c0b71-160"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="c0b71-161"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="c0b71-161"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-162">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="c0b71-162">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="c0b71-163"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="c0b71-163"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-164">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="c0b71-164">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="c0b71-165"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="c0b71-165"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-166">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="c0b71-166">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="c0b71-167"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="c0b71-167"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-168">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="c0b71-168">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="c0b71-169"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="c0b71-169"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-170">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="c0b71-170">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c0b71-171">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="c0b71-171">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-172">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c0b71-172">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-174">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrStorageAllocationUnits ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="c0b71-174">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-175">形成此儲存區之區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c0b71-175">Size, in bytes, of the blocks that form this storage extent.</span></span> <span data-ttu-id="c0b71-176">如果此概念對裝置類型無效，則值為1。</span><span class="sxs-lookup"><span data-stu-id="c0b71-176">If this concept is not valid for the device type, the value is 1.</span></span>

<span data-ttu-id="c0b71-177">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-177">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="c0b71-178">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-178">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-179">**標題**</span><span class="sxs-lookup"><span data-stu-id="c0b71-179">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c0b71-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-182">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="c0b71-182">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-183">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="c0b71-183">Short description of the object.</span></span>

<span data-ttu-id="c0b71-184">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-185">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="c0b71-185">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-186">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c0b71-186">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-188">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 檔案系統函式 \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| FS \_ 音量 \_ 已 \_ 壓縮」 ) </span><span class="sxs-lookup"><span data-stu-id="c0b71-188">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)\|FS\_VOL\_IS\_COMPRESSED")</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-189">若 **為 True**，則會壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="c0b71-189">If **True**, the file is compressed.</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-190">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c0b71-190">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-191">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c0b71-191">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-193">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="c0b71-193">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-194">Windows 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c0b71-194">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="c0b71-195">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-195">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="c0b71-196"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-196"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="c0b71-197"> (0)</span><span class="sxs-lookup"><span data-stu-id="c0b71-197">(0)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-198">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="c0b71-198">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="c0b71-199"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-199"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="c0b71-200">(1)</span><span class="sxs-lookup"><span data-stu-id="c0b71-200">(1)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-201">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="c0b71-201">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c0b71-202"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-202"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="c0b71-203">(2)</span><span class="sxs-lookup"><span data-stu-id="c0b71-203">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="c0b71-204"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-204"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="c0b71-205">(3)</span><span class="sxs-lookup"><span data-stu-id="c0b71-205">(3)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-206">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="c0b71-206">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c0b71-207"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-207"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="c0b71-208">(4)</span><span class="sxs-lookup"><span data-stu-id="c0b71-208">(4)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-209">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="c0b71-209">Device is not working properly.</span></span> <span data-ttu-id="c0b71-210">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="c0b71-210">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="c0b71-211"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-211"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="c0b71-212">(5)</span><span class="sxs-lookup"><span data-stu-id="c0b71-212">(5)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-213">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="c0b71-213">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="c0b71-214"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-214"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="c0b71-215">(6)</span><span class="sxs-lookup"><span data-stu-id="c0b71-215">(6)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-216">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="c0b71-216">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="c0b71-217"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-217"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="c0b71-218">(7)</span><span class="sxs-lookup"><span data-stu-id="c0b71-218">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="c0b71-219"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-219"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="c0b71-220">(8)</span><span class="sxs-lookup"><span data-stu-id="c0b71-220">(8)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-221">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="c0b71-221">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="c0b71-222"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-222"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="c0b71-223">(9)</span><span class="sxs-lookup"><span data-stu-id="c0b71-223">(9)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-224">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="c0b71-224">Device is not working properly.</span></span> <span data-ttu-id="c0b71-225">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="c0b71-225">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="c0b71-226"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-226"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="c0b71-227">(10)</span><span class="sxs-lookup"><span data-stu-id="c0b71-227">(10)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-228">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="c0b71-228">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="c0b71-229"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-229"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="c0b71-230">(11)</span><span class="sxs-lookup"><span data-stu-id="c0b71-230">(11)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-231">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="c0b71-231">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="c0b71-232"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-232"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="c0b71-233"> (12) </span><span class="sxs-lookup"><span data-stu-id="c0b71-233">(12)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-234">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="c0b71-234">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="c0b71-235"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-235"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="c0b71-236">(13)</span><span class="sxs-lookup"><span data-stu-id="c0b71-236">(13)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-237">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="c0b71-237">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="c0b71-238"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-238"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="c0b71-239">(14)</span><span class="sxs-lookup"><span data-stu-id="c0b71-239">(14)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-240">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="c0b71-240">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="c0b71-241"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-241"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="c0b71-242">(15)</span><span class="sxs-lookup"><span data-stu-id="c0b71-242">(15)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-243">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="c0b71-243">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="c0b71-244"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-244"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="c0b71-245">(16)</span><span class="sxs-lookup"><span data-stu-id="c0b71-245">(16)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-246">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="c0b71-246">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="c0b71-247"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-247"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="c0b71-248">(17)</span><span class="sxs-lookup"><span data-stu-id="c0b71-248">(17)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-249">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="c0b71-249">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c0b71-250"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-250"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="c0b71-251">(18)</span><span class="sxs-lookup"><span data-stu-id="c0b71-251">(18)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-252">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="c0b71-252">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="c0b71-253"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-253"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="c0b71-254">(19)</span><span class="sxs-lookup"><span data-stu-id="c0b71-254">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c0b71-255"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-255"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="c0b71-256">(20)</span><span class="sxs-lookup"><span data-stu-id="c0b71-256">(20)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-257">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="c0b71-257">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="c0b71-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="c0b71-259">(21)</span><span class="sxs-lookup"><span data-stu-id="c0b71-259">(21)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-260">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="c0b71-260">System failure.</span></span> <span data-ttu-id="c0b71-261">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="c0b71-261">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="c0b71-262">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="c0b71-262">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="c0b71-263"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-263"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="c0b71-264">(22)</span><span class="sxs-lookup"><span data-stu-id="c0b71-264">(22)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-265">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="c0b71-265">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="c0b71-266"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-266"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="c0b71-267">(23)</span><span class="sxs-lookup"><span data-stu-id="c0b71-267">(23)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-268">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="c0b71-268">System failure.</span></span> <span data-ttu-id="c0b71-269">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="c0b71-269">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="c0b71-270"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-270"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="c0b71-271">(24)</span><span class="sxs-lookup"><span data-stu-id="c0b71-271">(24)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-272">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="c0b71-272">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c0b71-273"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-273"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c0b71-274">(25)</span><span class="sxs-lookup"><span data-stu-id="c0b71-274">(25)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-275">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="c0b71-275">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c0b71-276"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-276"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c0b71-277">(26)</span><span class="sxs-lookup"><span data-stu-id="c0b71-277">(26)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-278">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="c0b71-278">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="c0b71-279"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-279"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="c0b71-280">(27)</span><span class="sxs-lookup"><span data-stu-id="c0b71-280">(27)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-281">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="c0b71-281">Device does not have a valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="c0b71-282"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-282"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="c0b71-283">(28)</span><span class="sxs-lookup"><span data-stu-id="c0b71-283">(28)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-284">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="c0b71-284">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="c0b71-285"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-285"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="c0b71-286">(29)</span><span class="sxs-lookup"><span data-stu-id="c0b71-286">(29)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-287">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="c0b71-287">Device is disabled.</span></span> <span data-ttu-id="c0b71-288">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="c0b71-288">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="c0b71-289"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-289"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="c0b71-290">(30)</span><span class="sxs-lookup"><span data-stu-id="c0b71-290">(30)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-291">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="c0b71-291">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c0b71-292"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="c0b71-292"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="c0b71-293"> (31) </span><span class="sxs-lookup"><span data-stu-id="c0b71-293">(31)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-294">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="c0b71-294">Device is not working properly.</span></span> <span data-ttu-id="c0b71-295">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="c0b71-295">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c0b71-296">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="c0b71-296">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-297">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c0b71-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-298">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-299">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="c0b71-299">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-300">若 **為 True**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="c0b71-300">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="c0b71-301">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-302">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c0b71-302">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-303">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c0b71-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-304">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-305">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c0b71-305">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-306">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="c0b71-306">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="c0b71-307">搭配類別的其他索引鍵屬性使用時，此屬性可讓這個類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="c0b71-307">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c0b71-308">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-309">**說明**</span><span class="sxs-lookup"><span data-stu-id="c0b71-309">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-310">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c0b71-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-311">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-312">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="c0b71-312">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-313">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="c0b71-313">Description of the object.</span></span>

<span data-ttu-id="c0b71-314">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-315">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c0b71-315">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-316">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c0b71-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-317">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-318">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "DeviceId" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="c0b71-318">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-319">記憶體陣列的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="c0b71-319">Unique identifier of the memory array.</span></span>

<span data-ttu-id="c0b71-320">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="c0b71-321">範例：「記憶體陣列1」</span><span class="sxs-lookup"><span data-stu-id="c0b71-321">Example: "Memory Array 1"</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-322">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="c0b71-322">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-323">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c0b71-323">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-324">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-325">若 **為 True**，則表示 **LastErrorCode** 中回報的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="c0b71-325">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="c0b71-326">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-326">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-327">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c0b71-327">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-328">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c0b71-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-329">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-330">有關 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及可採取的任何矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c0b71-330">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that can be taken.</span></span>

<span data-ttu-id="c0b71-331">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-332">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="c0b71-332">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-333">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c0b71-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-334">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-335">硬體使用的錯誤檢查類型。</span><span class="sxs-lookup"><span data-stu-id="c0b71-335">Types of error checking used by the hardware.</span></span>

<span data-ttu-id="c0b71-336">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-336">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-337">**檔**</span><span class="sxs-lookup"><span data-stu-id="c0b71-337">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-338">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c0b71-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-339">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-340">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 檔案系統函數 [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)) </span><span class="sxs-lookup"><span data-stu-id="c0b71-340">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-341">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-341">Access type: Read-only</span></span>

<span data-ttu-id="c0b71-342">邏輯磁片上的檔案系統。</span><span class="sxs-lookup"><span data-stu-id="c0b71-342">File system on the logical disk.</span></span>

<span data-ttu-id="c0b71-343">範例： "NTFS"</span><span class="sxs-lookup"><span data-stu-id="c0b71-343">Example: "NTFS"</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-344">**FreeSpace**</span><span class="sxs-lookup"><span data-stu-id="c0b71-344">**FreeSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-345">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c0b71-345">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-346">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-347">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="c0b71-347">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-348">邏輯磁片上的可用空間。</span><span class="sxs-lookup"><span data-stu-id="c0b71-348">Space available on the logical disk.</span></span>

<span data-ttu-id="c0b71-349">這個屬性繼承自 [**CIM \_ LogicalDisk**](cim-logicaldisk.md)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-349">This property is inherited from [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span>

<span data-ttu-id="c0b71-350">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-350">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-351">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c0b71-351">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-352">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="c0b71-352">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-353">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-354">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="c0b71-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-355">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-355">Access type: Read-only</span></span>

<span data-ttu-id="c0b71-356">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="c0b71-356">Date and time the object was installed.</span></span> <span data-ttu-id="c0b71-357">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="c0b71-357">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c0b71-358">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-358">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-359">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c0b71-359">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-360">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c0b71-360">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-361">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-362">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c0b71-362">Last error code reported by the logical device.</span></span>

<span data-ttu-id="c0b71-363">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-364">**MaximumComponentLength**</span><span class="sxs-lookup"><span data-stu-id="c0b71-364">**MaximumComponentLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-365">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c0b71-365">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-366">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-367">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 檔案系統函數 [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)) </span><span class="sxs-lookup"><span data-stu-id="c0b71-367">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-368">包含 Windows 磁片磁碟機所支援之檔案名元件的最大長度。</span><span class="sxs-lookup"><span data-stu-id="c0b71-368">Contains the maximum length of a file-name component supported by the Windows drive.</span></span>

<span data-ttu-id="c0b71-369">範例：255</span><span class="sxs-lookup"><span data-stu-id="c0b71-369">Example: 255</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-370">**名稱**</span><span class="sxs-lookup"><span data-stu-id="c0b71-370">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-371">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c0b71-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-372">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-373">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="c0b71-373">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-374">物件標籤。</span><span class="sxs-lookup"><span data-stu-id="c0b71-374">Object label.</span></span>

<span data-ttu-id="c0b71-375">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-375">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-376">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="c0b71-376">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-377">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c0b71-377">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-378">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-379">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrStorageSize ") </span><span class="sxs-lookup"><span data-stu-id="c0b71-379">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-380">連續區塊總數，每個區塊會封鎖 **區塊** 屬性中包含的值大小，這會形成此儲存範圍。</span><span class="sxs-lookup"><span data-stu-id="c0b71-380">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="c0b71-381">您可以將 [ **區塊** ] 屬性的值乘以這個屬性的值，以計算儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="c0b71-381">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="c0b71-382">如果 **區塊** 的值是1，則這個屬性是儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="c0b71-382">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="c0b71-383">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-383">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="c0b71-384">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-384">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-385">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="c0b71-385">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-386">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c0b71-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-387">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-388">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="c0b71-388">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-389">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="c0b71-389">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="c0b71-390">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-390">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="c0b71-391">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="c0b71-391">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-392">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c0b71-392">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-393">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="c0b71-393">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-394">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-395">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="c0b71-395">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="c0b71-396">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="c0b71-396">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c0b71-397"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c0b71-397"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="c0b71-398"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="c0b71-398"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c0b71-399"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="c0b71-399"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c0b71-400"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="c0b71-400"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-401">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="c0b71-401">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="c0b71-402"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="c0b71-402"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-403">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="c0b71-403">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="c0b71-404"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="c0b71-404"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-405">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c0b71-405">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="c0b71-406">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="c0b71-406">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="c0b71-407">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-407">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="c0b71-408"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="c0b71-408"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-409">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="c0b71-409">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="c0b71-410"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="c0b71-410"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c0b71-411">支援計時 Power-On</span><span class="sxs-lookup"><span data-stu-id="c0b71-411">Timed Power-On Supported</span></span>

<span data-ttu-id="c0b71-412">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="c0b71-412">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c0b71-413">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="c0b71-413">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-414">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c0b71-414">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-415">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-416">若 **為 True**，則裝置可以是電源管理 (可進入暫停模式，依此類推) 。</span><span class="sxs-lookup"><span data-stu-id="c0b71-416">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="c0b71-417">屬性不表示電源管理功能目前已啟用，只有邏輯裝置能夠進行電源管理。</span><span class="sxs-lookup"><span data-stu-id="c0b71-417">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="c0b71-418">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-418">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-419">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="c0b71-419">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-420">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c0b71-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-421">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-422">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Windows 網路功能 \| WNetGetConnection" ) </span><span class="sxs-lookup"><span data-stu-id="c0b71-422">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Windows Networking Functions\|WNetGetConnection")</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-423">邏輯裝置的網路路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="c0b71-423">Network path name to the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-424">**目的**</span><span class="sxs-lookup"><span data-stu-id="c0b71-424">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-425">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c0b71-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-426">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-427">描述媒體及其用途的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="c0b71-427">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="c0b71-428">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-428">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-429">**QuotasDisabled**</span><span class="sxs-lookup"><span data-stu-id="c0b71-429">**QuotasDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-430">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c0b71-430">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-431">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-432">若 **為 True**，則不會為此磁片區啟用配額管理。</span><span class="sxs-lookup"><span data-stu-id="c0b71-432">If **True**, quota management is not enabled for this volume.</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-433">**QuotasIncomplete**</span><span class="sxs-lookup"><span data-stu-id="c0b71-433">**QuotasIncomplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-434">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c0b71-434">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-435">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-436">若 **為 True，則** 使用配額管理，但已停用。</span><span class="sxs-lookup"><span data-stu-id="c0b71-436">If **True**, quota management was used but has been disabled.</span></span> <span data-ttu-id="c0b71-437">[不完整] 指的是停用配額管理之後，檔案系統中剩餘的資訊。</span><span class="sxs-lookup"><span data-stu-id="c0b71-437">Incomplete refers to the information left in the file system after quota management has been disabled.</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-438">**QuotasRebuilding**</span><span class="sxs-lookup"><span data-stu-id="c0b71-438">**QuotasRebuilding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-439">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c0b71-439">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-440">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-441">若為 **True**，則表示檔案系統正在設定配額管理。</span><span class="sxs-lookup"><span data-stu-id="c0b71-441">If **True**, the file system is setting up for quota management.</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-442">**SessionID**</span><span class="sxs-lookup"><span data-stu-id="c0b71-442">**SessionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-443">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c0b71-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-444">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-445">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c0b71-445">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-446">使用者會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c0b71-446">ID of the user's session.</span></span> <span data-ttu-id="c0b71-447">使用者可以使用本機登入或終端機會話進行連接。</span><span class="sxs-lookup"><span data-stu-id="c0b71-447">The user may be connected using a local login or a terminal session.</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-448">**大小**</span><span class="sxs-lookup"><span data-stu-id="c0b71-448">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-449">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c0b71-449">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-450">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-451">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="c0b71-451">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-452">邏輯磁片的大小。</span><span class="sxs-lookup"><span data-stu-id="c0b71-452">Size of the logical disk.</span></span>

<span data-ttu-id="c0b71-453">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-453">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="c0b71-454">這個屬性繼承自 [**CIM \_ LogicalDisk**](cim-logicaldisk.md)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-454">This property is inherited from [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-455">**狀態**</span><span class="sxs-lookup"><span data-stu-id="c0b71-455">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-456">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c0b71-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-457">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-458">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="c0b71-458">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-459">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="c0b71-459">Current status of the object.</span></span> <span data-ttu-id="c0b71-460">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="c0b71-460">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c0b71-461">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素，例如智慧型啟用的硬碟可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="c0b71-461">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive may function properly, but predicts a failure in the near future).</span></span> <span data-ttu-id="c0b71-462">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="c0b71-462">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c0b71-463">服務狀態適用于系統管理工作，例如磁片的鏡像重新同步處理、重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="c0b71-463">The Service status applies to administrative work, such as mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c0b71-464">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="c0b71-464">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c0b71-465">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-465">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c0b71-466">值如下：</span><span class="sxs-lookup"><span data-stu-id="c0b71-466">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c0b71-467">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="c0b71-467">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c0b71-468">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="c0b71-468">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c0b71-469">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="c0b71-469">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c0b71-470">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="c0b71-470">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c0b71-471">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="c0b71-471">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c0b71-472">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="c0b71-472">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c0b71-473">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="c0b71-473">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c0b71-474">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="c0b71-474">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c0b71-475">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="c0b71-475">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c0b71-476">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="c0b71-476">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c0b71-477">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="c0b71-477">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c0b71-478">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="c0b71-478">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c0b71-479">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c0b71-479">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-480">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c0b71-480">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-481">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-482">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="c0b71-482">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-483">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="c0b71-483">State of the logical device.</span></span> <span data-ttu-id="c0b71-484">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="c0b71-484">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="c0b71-485">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c0b71-486">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c0b71-486">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c0b71-487">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="c0b71-487">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c0b71-488">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="c0b71-488">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c0b71-489">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="c0b71-489">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c0b71-490">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="c0b71-490">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c0b71-491">**SupportsDiskQuotas**</span><span class="sxs-lookup"><span data-stu-id="c0b71-491">**SupportsDiskQuotas**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-492">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c0b71-492">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-493">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-493">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-494">若 **為 True**，則表示此網路磁碟機機對應的檔案系統支援磁片配額。</span><span class="sxs-lookup"><span data-stu-id="c0b71-494">If **True**, then the file system on which this network drive is mapped supports disk quotas.</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-495">**SupportsFileBasedCompression**</span><span class="sxs-lookup"><span data-stu-id="c0b71-495">**SupportsFileBasedCompression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-496">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c0b71-496">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-497">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-497">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-498">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 檔案系統函數 \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| FS \_ 檔 \_ 壓縮」 ) </span><span class="sxs-lookup"><span data-stu-id="c0b71-498">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)\|FS\_FILE\_COMPRESSION")</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-499">若 **為 True**，則邏輯磁碟分割支援以檔案為基礎的壓縮，例如 NTFS 的情況。</span><span class="sxs-lookup"><span data-stu-id="c0b71-499">If **True**, the logical disk partition supports file-based compression, such as is the case with NTFS.</span></span> <span data-ttu-id="c0b71-500">當 **壓縮** 的屬性為 **True** 時，這個屬性為 **False**。</span><span class="sxs-lookup"><span data-stu-id="c0b71-500">This property is **False**, when the **Compressed** property is **True**.</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-501">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c0b71-501">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-502">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c0b71-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-503">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-503">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-504">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c0b71-504">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-505">範圍電腦之 **CreationClassName** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="c0b71-505">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="c0b71-506">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-506">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-507">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c0b71-507">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-508">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c0b71-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-509">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-510">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c0b71-510">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-511">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0b71-511">Name of the scoping system.</span></span>

<span data-ttu-id="c0b71-512">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-512">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-513">**VolumeName**</span><span class="sxs-lookup"><span data-stu-id="c0b71-513">**VolumeName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-514">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c0b71-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-515">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c0b71-515">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-516">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 檔案系統函數 [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)) </span><span class="sxs-lookup"><span data-stu-id="c0b71-516">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-517">邏輯磁片的磁片區名稱。</span><span class="sxs-lookup"><span data-stu-id="c0b71-517">Volume name of the logical disk.</span></span> <span data-ttu-id="c0b71-518">這個屬性值最多可有32個字元。</span><span class="sxs-lookup"><span data-stu-id="c0b71-518">This property value can have a maximum of 32 characters.</span></span>

</dd> <dt>

<span data-ttu-id="c0b71-519">**VolumeSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="c0b71-519">**VolumeSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b71-520">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c0b71-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-521">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0b71-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0b71-522">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 檔案系統函數 [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)) </span><span class="sxs-lookup"><span data-stu-id="c0b71-522">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="c0b71-523">邏輯磁片的音量序號。</span><span class="sxs-lookup"><span data-stu-id="c0b71-523">Volume serial number of the logical disk.</span></span> <span data-ttu-id="c0b71-524">這個屬性值最多可有11個字元。</span><span class="sxs-lookup"><span data-stu-id="c0b71-524">This property value can have a maximum of 11 characters.</span></span>

<span data-ttu-id="c0b71-525">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c0b71-525">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="c0b71-526">範例： "A8C3-D032"</span><span class="sxs-lookup"><span data-stu-id="c0b71-526">Example: "A8C3-D032"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0b71-527">備註</span><span class="sxs-lookup"><span data-stu-id="c0b71-527">Remarks</span></span>

<span data-ttu-id="c0b71-528">針對此類別傳回的實例如下所示，假設使用者 A 正在列舉實例：</span><span class="sxs-lookup"><span data-stu-id="c0b71-528">The instances returned for this class are as follows, supposing that user A is enumerating the instances:</span></span>

-   <span data-ttu-id="c0b71-529">此提供者會在該電腦上尋找使用者 A 的登入會話：</span><span class="sxs-lookup"><span data-stu-id="c0b71-529">The provider looks for a logon session of user A on that machine:</span></span>

    -   <span data-ttu-id="c0b71-530">如果有一個 (，而且只有一個) 這類登入會話，則提供者會傳回該會話的對應磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="c0b71-530">If there is one (and only one) such logon session, then the provider returns the mapped drives of that session.</span></span>
    -   <span data-ttu-id="c0b71-531">如果電腦上的使用者 A 有一個以上的會話，則不會傳回任何對應的磁片磁碟機實例 (因為提供者沒有合理的方式來決定要使用哪個會話) 。</span><span class="sxs-lookup"><span data-stu-id="c0b71-531">If there is more than one session for user A on the machine, then no mapped drive instances are returned (because the provider has no reasonable way of deciding which session to use).</span></span>

-   <span data-ttu-id="c0b71-532">如果沒有執行中使用者的會話，而且有本機登入的使用者 B：</span><span class="sxs-lookup"><span data-stu-id="c0b71-532">If there are no sessions of user A running, and there is a locally logged on user B:</span></span>

    -   <span data-ttu-id="c0b71-533">如果使用者 B 有單一會話，則提供者會模擬，並傳回使用者 B 的對應磁片磁碟機。此案例支援技術服務人員想要查看本機登入使用者實例的案例。</span><span class="sxs-lookup"><span data-stu-id="c0b71-533">If there is a single session for user B, then the provider impersonates A and returns the mapped drives of user B. This case supports the scenario of Helpdesk wanting to see the instances of a locally logged on user.</span></span> <span data-ttu-id="c0b71-534">不過，是否傳回實例取決於主控台系統管理工具中的本機安全性原則設定。</span><span class="sxs-lookup"><span data-stu-id="c0b71-534">However, whether instances are returned depends on the Local Security Policy settings in the Control Panel Administrative Tools.</span></span> <span data-ttu-id="c0b71-535">如果下列原則設定為 [物件建立者]，則即使是 Administrators 群組的成員，也不會傳回任何對應的磁片磁碟機實例：</span><span class="sxs-lookup"><span data-stu-id="c0b71-535">If the following policy is set to "Object Creator", then no mapped drive instances are returned, even if A is a member of the Administrators group:</span></span>

        <span data-ttu-id="c0b71-536">「系統物件：系統管理員群組成員所建立物件的預設擁有者」。</span><span class="sxs-lookup"><span data-stu-id="c0b71-536">"System object: default owner for objects created by members of the administrators group."</span></span>

    -   <span data-ttu-id="c0b71-537">同樣地，如果電腦上執行的使用者 B 有一個以上的會話，則提供者無法決定要使用哪一種。</span><span class="sxs-lookup"><span data-stu-id="c0b71-537">Again, if there is more than one session of user B running on the machine, then the provider has no way of deciding which to use.</span></span> <span data-ttu-id="c0b71-538">在此情況下，不會傳回任何對應的磁片磁碟機實例。</span><span class="sxs-lookup"><span data-stu-id="c0b71-538">In this case, no mapped drive instances are returned.</span></span>

<span data-ttu-id="c0b71-539">如需使用 **Win32 \_ MappedLogicalDisk** 的詳細資訊，請參閱 [如何判斷哪些磁片磁碟機對應至網路共用？](https://blogs.technet.com/b/heyscriptingguy/archive/2005/10/27/how-can-i-determine-which-drives-are-mapped-to-network-shares.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0b71-539">For more information on using **Win32\_MappedLogicalDisk**, see [How Can I Determine Which Drives are Mapped to Network Shares?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/10/27/how-can-i-determine-which-drives-are-mapped-to-network-shares.aspx)</span></span>

## <a name="examples"></a><span data-ttu-id="c0b71-540">範例</span><span class="sxs-lookup"><span data-stu-id="c0b71-540">Examples</span></span>

<span data-ttu-id="c0b71-541">下列 PowerShell 程式碼片段會顯示對應的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="c0b71-541">The following PowerShell snippet shows mapped drives.</span></span>


```PowerShell
Get-WmiObject Win32_MappedLogicalDisk | Select Name, ProviderName, FileSystem, Size, FreeSpace | Format-Table
```



## <a name="requirements"></a><span data-ttu-id="c0b71-542">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0b71-542">Requirements</span></span>



| <span data-ttu-id="c0b71-543">需求</span><span class="sxs-lookup"><span data-stu-id="c0b71-543">Requirement</span></span> | <span data-ttu-id="c0b71-544">值</span><span class="sxs-lookup"><span data-stu-id="c0b71-544">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0b71-545">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0b71-545">Minimum supported client</span></span><br/> | <span data-ttu-id="c0b71-546">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0b71-546">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c0b71-547">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0b71-547">Minimum supported server</span></span><br/> | <span data-ttu-id="c0b71-548">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0b71-548">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c0b71-549">命名空間</span><span class="sxs-lookup"><span data-stu-id="c0b71-549">Namespace</span></span><br/>                | <span data-ttu-id="c0b71-550">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c0b71-550">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c0b71-551">MOF</span><span class="sxs-lookup"><span data-stu-id="c0b71-551">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0b71-552"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0b71-552"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0b71-553">DLL</span><span class="sxs-lookup"><span data-stu-id="c0b71-553">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0b71-554"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0b71-554"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0b71-555">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0b71-555">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0b71-556">**CIM \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="c0b71-556">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="c0b71-557">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="c0b71-557">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="c0b71-558">WMI 工作：磁片和檔案系統</span><span class="sxs-lookup"><span data-stu-id="c0b71-558">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

