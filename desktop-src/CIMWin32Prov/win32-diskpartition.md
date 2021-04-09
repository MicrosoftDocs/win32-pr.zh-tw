---
description: 表示在執行 Windows 的電腦系統上，實體磁片之資料分割區域的功能和管理容量。
ms.assetid: 7e78be3f-bae4-4374-abbf-7c4e63ba7593
ms.tgt_platform: multiple
title: Win32_DiskPartition 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskPartition
- Win32_DiskPartition.AdditionalAvailability
- Win32_DiskPartition.Availability
- Win32_DiskPartition.PowerManagementCapabilities
- Win32_DiskPartition.IdentifyingDescriptions
- Win32_DiskPartition.MaxQuiesceTime
- Win32_DiskPartition.OtherIdentifyingInfo
- Win32_DiskPartition.StatusInfo
- Win32_DiskPartition.PowerOnHours
- Win32_DiskPartition.TotalPowerOnHours
- Win32_DiskPartition.Access
- Win32_DiskPartition.BlockSize
- Win32_DiskPartition.Bootable
- Win32_DiskPartition.BootPartition
- Win32_DiskPartition.Caption
- Win32_DiskPartition.ConfigManagerErrorCode
- Win32_DiskPartition.ConfigManagerUserConfig
- Win32_DiskPartition.CreationClassName
- Win32_DiskPartition.Description
- Win32_DiskPartition.DeviceID
- Win32_DiskPartition.DiskIndex
- Win32_DiskPartition.ErrorCleared
- Win32_DiskPartition.ErrorDescription
- Win32_DiskPartition.ErrorMethodology
- Win32_DiskPartition.HiddenSectors
- Win32_DiskPartition.Index
- Win32_DiskPartition.InstallDate
- Win32_DiskPartition.LastErrorCode
- Win32_DiskPartition.Name
- Win32_DiskPartition.NumberOfBlocks
- Win32_DiskPartition.PNPDeviceID
- Win32_DiskPartition.PowerManagementSupported
- Win32_DiskPartition.PrimaryPartition
- Win32_DiskPartition.Purpose
- Win32_DiskPartition.RewritePartition
- Win32_DiskPartition.Size
- Win32_DiskPartition.StartingOffset
- Win32_DiskPartition.Status
- Win32_DiskPartition.SystemCreationClassName
- Win32_DiskPartition.SystemName
- Win32_DiskPartition.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4f9a9c16f58d0119c8027848c481479985e7505e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847486"
---
# <a name="win32_diskpartition-class"></a><span data-ttu-id="c4745-103">Win32 \_ DiskPartition 類別</span><span class="sxs-lookup"><span data-stu-id="c4745-103">Win32\_DiskPartition class</span></span>

<span data-ttu-id="c4745-104">**Win32 \_ DiskPartition** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表在執行 Windows 的電腦系統上，實體磁片之分割區區域的功能和管理能力。</span><span class="sxs-lookup"><span data-stu-id="c4745-104">The **Win32\_DiskPartition** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the capabilities and management capacity of a partitioned area of a physical disk on a computer system running Windows.</span></span> <span data-ttu-id="c4745-105">範例：磁片 \# 0、磁碟分割 \# 1。</span><span class="sxs-lookup"><span data-stu-id="c4745-105">Example: Disk \#0, Partition \#1.</span></span>

<span data-ttu-id="c4745-106">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c4745-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c4745-107">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="c4745-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4745-108">語法</span><span class="sxs-lookup"><span data-stu-id="c4745-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskPartition : CIM_DiskPartition
{
  unit16   AdditionalAvailability;
  uint16   Availability;
  uint16   PowerManagementCapabilities[];
  string   IdentifyingDescriptions[1];
  uint64   MaxQuiesceTime;
  uint64   OtherIdentifyingInfo;
  uint16   StatusInfo;
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  uint16   Access;
  uint64   BlockSize;
  boolean  Bootable;
  boolean  BootPartition;
  string.  Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string.  CreationClassName;
  string   Description;
  string   DeviceID;
  uint32   DiskIndex;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  uint32   HiddenSectors;
  uint32   Index;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  boolean  PrimaryPartition;
  string   Purpose;
  boolean  RewritePartition;
  uint64   Size;
  uint64   StartingOffset;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  string   Type;
};
```

## <a name="members"></a><span data-ttu-id="c4745-109">成員</span><span class="sxs-lookup"><span data-stu-id="c4745-109">Members</span></span>

<span data-ttu-id="c4745-110">**Win32 \_ DiskPartition** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c4745-110">The **Win32\_DiskPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="c4745-111">方法</span><span class="sxs-lookup"><span data-stu-id="c4745-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="c4745-112">屬性</span><span class="sxs-lookup"><span data-stu-id="c4745-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c4745-113">方法</span><span class="sxs-lookup"><span data-stu-id="c4745-113">Methods</span></span>

<span data-ttu-id="c4745-114">**Win32 \_ DiskPartition** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c4745-114">The **Win32\_DiskPartition** class has these methods.</span></span>



| <span data-ttu-id="c4745-115">方法</span><span class="sxs-lookup"><span data-stu-id="c4745-115">Method</span></span>                                                     | <span data-ttu-id="c4745-116">描述</span><span class="sxs-lookup"><span data-stu-id="c4745-116">Description</span></span>                                                                                                   |
|:-----------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c4745-117">**重設**</span><span class="sxs-lookup"><span data-stu-id="c4745-117">**Reset**</span></span>](win32-diskpartition-reset.md)                 | <span data-ttu-id="c4745-118">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="c4745-118">Requests a reset of the logical device.</span></span><br/>                                                            |
| [<span data-ttu-id="c4745-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c4745-119">**SetPowerState**</span></span>](win32-diskpartition-setpowerstate.md) | <span data-ttu-id="c4745-120">設定邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="c4745-120">Sets the desired power state for a logical device and when a device should be put into that state.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c4745-121">屬性</span><span class="sxs-lookup"><span data-stu-id="c4745-121">Properties</span></span>

<span data-ttu-id="c4745-122">**Win32 \_ DiskPartition** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c4745-122">The **Win32\_DiskPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c4745-123">**存取**</span><span class="sxs-lookup"><span data-stu-id="c4745-123">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-124">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c4745-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4745-126">媒體存取可用。</span><span class="sxs-lookup"><span data-stu-id="c4745-126">Media access available.</span></span>

<span data-ttu-id="c4745-127">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-127">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c4745-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c4745-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="c4745-129"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**可讀取** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="c4745-129"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="c4745-130"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>可 **寫入** (2) </span><span class="sxs-lookup"><span data-stu-id="c4745-130"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c4745-131">可寫入</span><span class="sxs-lookup"><span data-stu-id="c4745-131">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="c4745-132"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>支援 (3) 的 **讀取/寫入**</span><span class="sxs-lookup"><span data-stu-id="c4745-132"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="c4745-133"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**撰寫一次** (4) </span><span class="sxs-lookup"><span data-stu-id="c4745-133"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c4745-134">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="c4745-134">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-135">資料類型： **unit16**</span><span class="sxs-lookup"><span data-stu-id="c4745-135">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-136">存取類型：僅限寫入</span><span class="sxs-lookup"><span data-stu-id="c4745-136">Access type: Write-only</span></span>
</dt> </dl>

<span data-ttu-id="c4745-137">裝置的其他可用性和狀態，超出可用性屬性中指定的範圍。</span><span class="sxs-lookup"><span data-stu-id="c4745-137">Additional availability and status of the Device, beyond that specified in the Availability property.</span></span> <span data-ttu-id="c4745-138">**Availability** 屬性代表裝置的主要狀態和可用性。</span><span class="sxs-lookup"><span data-stu-id="c4745-138">The **Availability** property denotes the primary status and availability of the Device.</span></span> <span data-ttu-id="c4745-139">在某些情況下，這並不是用來表示裝置的完整狀態。</span><span class="sxs-lookup"><span data-stu-id="c4745-139">In some cases, this will not be sufficient to denote the complete status of the Device.</span></span> <span data-ttu-id="c4745-140">在這些情況下， **AdditionalAvailability** 屬性可以用來提供進一步的資訊。</span><span class="sxs-lookup"><span data-stu-id="c4745-140">In those cases, the **AdditionalAvailability** property can be used to provide further information.</span></span> <span data-ttu-id="c4745-141">例如，裝置的主要 **可用性** 可能會 (值 = 8) ，但可能也處於低電源狀態 (**AdditonalAvailability** 值 = 14) ，或裝置可能在測試 (中執行診斷) **AdditionalAvailability** 值 = 5」。</span><span class="sxs-lookup"><span data-stu-id="c4745-141">For example, a Device's primary **Availability** may be Off line (value=8), but it may also be in a low power state (**AdditonalAvailability** value=14), or the Device could be running Diagnostics (**AdditionalAvailability** value=5, In Test)."</span></span>

<span data-ttu-id="c4745-142">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c4745-143">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c4745-143">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c4745-144">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="c4745-144">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="c4745-145">執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="c4745-145">**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="c4745-146">**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="c4745-146">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="c4745-147">**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="c4745-147">**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c4745-148">**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="c4745-148">**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="c4745-149">**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="c4745-149">**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="c4745-150">**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="c4745-150">**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="c4745-151">**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="c4745-151">**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c4745-152"> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="c4745-152">**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="c4745-153">**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="c4745-153">**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="c4745-154">**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="c4745-154">**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="c4745-155">省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="c4745-155">**Power Save - Unknown** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="c4745-156">省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="c4745-156">**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="c4745-157">省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="c4745-157">**Power Save - Standby** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="c4745-158"> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="c4745-158">**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="c4745-159">省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="c4745-159">**Power Save - Warning** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="c4745-160">已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="c4745-160">**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="c4745-161">**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="c4745-161">**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="c4745-162">**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="c4745-162">**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="c4745-163">**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="c4745-163">**Quiesce** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c4745-164">**可用性**</span><span class="sxs-lookup"><span data-stu-id="c4745-164">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-165">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c4745-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4745-167">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="c4745-167">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="c4745-168">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="c4745-168">Availability and status of the device.</span></span>

<span data-ttu-id="c4745-169">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-169">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c4745-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c4745-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c4745-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="c4745-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="c4745-172"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="c4745-172"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="c4745-173"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="c4745-173"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="c4745-174"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="c4745-174"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c4745-175"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="c4745-175"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="c4745-176"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="c4745-176"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="c4745-177"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="c4745-177"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="c4745-178"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="c4745-178"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c4745-179"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="c4745-179"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="c4745-180"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="c4745-180"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="c4745-181"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="c4745-181"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="c4745-182"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="c4745-182"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c4745-183">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="c4745-183">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="c4745-184"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="c4745-184"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="c4745-185">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="c4745-185">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="c4745-186"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="c4745-186"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="c4745-187">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="c4745-187">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="c4745-188"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="c4745-188"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="c4745-189"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="c4745-189"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="c4745-190">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="c4745-190">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="c4745-191"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="c4745-191"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="c4745-192">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="c4745-192">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="c4745-193"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="c4745-193"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="c4745-194">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="c4745-194">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="c4745-195"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="c4745-195"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="c4745-196">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="c4745-196">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="c4745-197"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="c4745-197"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="c4745-198">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="c4745-198">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c4745-199">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="c4745-199">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-200">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c4745-200">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-201">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4745-202">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrStorageAllocationUnits ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="c4745-202">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c4745-203">形成此儲存範圍之區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c4745-203">Size in bytes of the blocks which form this storage extent.</span></span> <span data-ttu-id="c4745-204">如果未知或區塊概念無效 (例如，針對匯總範圍、記憶體或邏輯磁片) ，請輸入1。</span><span class="sxs-lookup"><span data-stu-id="c4745-204">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter a 1.</span></span>

<span data-ttu-id="c4745-205">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="c4745-205">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="c4745-206">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-206">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4745-207">**啟動**</span><span class="sxs-lookup"><span data-stu-id="c4745-207">**Bootable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-208">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c4745-208">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4745-210">指出是否可以從此磁碟分割啟動電腦。</span><span class="sxs-lookup"><span data-stu-id="c4745-210">Indicates whether the computer can be booted from this partition.</span></span>

<span data-ttu-id="c4745-211">這個屬性繼承自 [**CIM \_ DiskPartition**](cim-diskpartition.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-211">This property is inherited from [**CIM\_DiskPartition**](cim-diskpartition.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4745-212">**BootPartition**</span><span class="sxs-lookup"><span data-stu-id="c4745-212">**BootPartition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-213">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c4745-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-214">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4745-215">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| File 函數 \| ReadFile" ) </span><span class="sxs-lookup"><span data-stu-id="c4745-215">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile")</span></span>
</dt> </dl>

<span data-ttu-id="c4745-216">分割區是使用中的資料分割。</span><span class="sxs-lookup"><span data-stu-id="c4745-216">Partition is the active partition.</span></span> <span data-ttu-id="c4745-217">從硬碟開機時，作業系統會使用作用中磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="c4745-217">The operating system uses the active partition when booting from a hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="c4745-218">**標題**</span><span class="sxs-lookup"><span data-stu-id="c4745-218">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-219">資料類型： **字串。**</span><span class="sxs-lookup"><span data-stu-id="c4745-219">Data type: **string.**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4745-221">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="c4745-221">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c4745-222">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="c4745-222">Short description of the object.</span></span>

<span data-ttu-id="c4745-223">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-223">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4745-224">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c4745-224">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-225">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c4745-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-226">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4745-227">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="c4745-227">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c4745-228">Windows 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c4745-228">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="c4745-229">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-229">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="c4745-230"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="c4745-230"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="c4745-231"> (0)</span><span class="sxs-lookup"><span data-stu-id="c4745-231">(0)</span></span>


</dt> <dd>

<span data-ttu-id="c4745-232">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="c4745-232">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="c4745-233"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="c4745-233"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="c4745-234">(1)</span><span class="sxs-lookup"><span data-stu-id="c4745-234">(1)</span></span>


</dt> <dd>

<span data-ttu-id="c4745-235">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="c4745-235">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c4745-236"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="c4745-236"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="c4745-237">(2)</span><span class="sxs-lookup"><span data-stu-id="c4745-237">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="c4745-238"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="c4745-238"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="c4745-239">(3)</span><span class="sxs-lookup"><span data-stu-id="c4745-239">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c4745-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="c4745-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="c4745-241">(4)</span><span class="sxs-lookup"><span data-stu-id="c4745-241">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="c4745-242"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="c4745-242"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="c4745-243">(5)</span><span class="sxs-lookup"><span data-stu-id="c4745-243">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="c4745-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="c4745-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="c4745-245">(6)</span><span class="sxs-lookup"><span data-stu-id="c4745-245">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="c4745-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="c4745-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="c4745-247">(7)</span><span class="sxs-lookup"><span data-stu-id="c4745-247">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="c4745-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="c4745-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="c4745-249">(8)</span><span class="sxs-lookup"><span data-stu-id="c4745-249">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="c4745-250"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="c4745-250"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="c4745-251">(9)</span><span class="sxs-lookup"><span data-stu-id="c4745-251">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="c4745-252"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="c4745-252"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="c4745-253">(10)</span><span class="sxs-lookup"><span data-stu-id="c4745-253">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="c4745-254"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="c4745-254"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="c4745-255">(11)</span><span class="sxs-lookup"><span data-stu-id="c4745-255">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="c4745-256"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="c4745-256"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="c4745-257"> (12) </span><span class="sxs-lookup"><span data-stu-id="c4745-257">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="c4745-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="c4745-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="c4745-259">(13)</span><span class="sxs-lookup"><span data-stu-id="c4745-259">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="c4745-260"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="c4745-260"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="c4745-261">(14)</span><span class="sxs-lookup"><span data-stu-id="c4745-261">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="c4745-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="c4745-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="c4745-263">(15)</span><span class="sxs-lookup"><span data-stu-id="c4745-263">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="c4745-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="c4745-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="c4745-265">(16)</span><span class="sxs-lookup"><span data-stu-id="c4745-265">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="c4745-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="c4745-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="c4745-267">(17)</span><span class="sxs-lookup"><span data-stu-id="c4745-267">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c4745-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="c4745-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="c4745-269">(18)</span><span class="sxs-lookup"><span data-stu-id="c4745-269">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="c4745-270"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="c4745-270"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="c4745-271">(19)</span><span class="sxs-lookup"><span data-stu-id="c4745-271">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c4745-272"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="c4745-272"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="c4745-273">(20)</span><span class="sxs-lookup"><span data-stu-id="c4745-273">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="c4745-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="c4745-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="c4745-275">(21)</span><span class="sxs-lookup"><span data-stu-id="c4745-275">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="c4745-276"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="c4745-276"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="c4745-277">(22)</span><span class="sxs-lookup"><span data-stu-id="c4745-277">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="c4745-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="c4745-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="c4745-279">(23)</span><span class="sxs-lookup"><span data-stu-id="c4745-279">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="c4745-280"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="c4745-280"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="c4745-281">(24)</span><span class="sxs-lookup"><span data-stu-id="c4745-281">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c4745-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="c4745-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c4745-283">(25)</span><span class="sxs-lookup"><span data-stu-id="c4745-283">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c4745-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="c4745-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c4745-285">(26)</span><span class="sxs-lookup"><span data-stu-id="c4745-285">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="c4745-286"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="c4745-286"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="c4745-287">(27)</span><span class="sxs-lookup"><span data-stu-id="c4745-287">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="c4745-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="c4745-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="c4745-289">(28)</span><span class="sxs-lookup"><span data-stu-id="c4745-289">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="c4745-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="c4745-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="c4745-291">(29)</span><span class="sxs-lookup"><span data-stu-id="c4745-291">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="c4745-292"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="c4745-292"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="c4745-293">(30)</span><span class="sxs-lookup"><span data-stu-id="c4745-293">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c4745-294"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="c4745-294"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="c4745-295"> (31) </span><span class="sxs-lookup"><span data-stu-id="c4745-295">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c4745-296">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="c4745-296">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-297">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c4745-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-298">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4745-299">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="c4745-299">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c4745-300">若 **為 True**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="c4745-300">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="c4745-301">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4745-302">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c4745-302">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-303">資料類型： **字串。**</span><span class="sxs-lookup"><span data-stu-id="c4745-303">Data type: **string.**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-304">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4745-305">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c4745-305">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c4745-306">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="c4745-306">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="c4745-307">搭配類別的其他索引鍵屬性使用時，屬性可讓這個類別的所有實例和其子類別都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="c4745-307">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c4745-308">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4745-309">**說明**</span><span class="sxs-lookup"><span data-stu-id="c4745-309">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-310">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c4745-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-311">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4745-312">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="c4745-312">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c4745-313">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="c4745-313">Description of the object.</span></span>

<span data-ttu-id="c4745-314">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4745-315">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c4745-315">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-316">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c4745-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-317">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4745-318">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "DeviceId" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="c4745-318">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="c4745-319">磁片磁碟機和磁碟分割的唯一識別碼，從系統的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="c4745-319">Unique identifier of the disk drive and partition, from the rest of the system.</span></span>

</dd> <dt>

<span data-ttu-id="c4745-320">**DiskIndex**</span><span class="sxs-lookup"><span data-stu-id="c4745-320">**DiskIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-321">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c4745-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-322">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4745-323">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| File 函數 \| ReadFile" ) </span><span class="sxs-lookup"><span data-stu-id="c4745-323">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile")</span></span>
</dt> </dl>

<span data-ttu-id="c4745-324">包含此分割區之磁片的索引編號。</span><span class="sxs-lookup"><span data-stu-id="c4745-324">Index number of the disk containing this partition.</span></span>

<span data-ttu-id="c4745-325">範例：0</span><span class="sxs-lookup"><span data-stu-id="c4745-325">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="c4745-326">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="c4745-326">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-327">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c4745-327">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-328">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4745-329">若 **為 True**，則表示 **LastErrorCode** 中回報的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="c4745-329">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="c4745-330">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4745-331">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c4745-331">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-332">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c4745-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-333">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4745-334">**LastErrorCode** 中所記錄之錯誤的相關資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c4745-334">Information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="c4745-335">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4745-336">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="c4745-336">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-337">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c4745-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-338">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4745-339">此儲存範圍所支援的錯誤偵測類型和修正。</span><span class="sxs-lookup"><span data-stu-id="c4745-339">Type of error detection and correction supported by this storage extent.</span></span>

<span data-ttu-id="c4745-340">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-340">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4745-341">**HiddenSectors**</span><span class="sxs-lookup"><span data-stu-id="c4745-341">**HiddenSectors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-342">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c4745-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-343">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4745-344">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API" ) </span><span class="sxs-lookup"><span data-stu-id="c4745-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API")</span></span>
</dt> </dl>

<span data-ttu-id="c4745-345">分割區中隱藏的磁區數目。</span><span class="sxs-lookup"><span data-stu-id="c4745-345">Number of hidden sectors in the partition.</span></span>

<span data-ttu-id="c4745-346">範例：63</span><span class="sxs-lookup"><span data-stu-id="c4745-346">Example: 63</span></span>

</dd> <dt>

<span data-ttu-id="c4745-347">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c4745-347">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-348">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="c4745-348">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c4745-349">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4745-350">自由格式字串的陣列，提供 OtherIdentifyingInfo 陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c4745-350">An array of free-form strings providing explanations and details behind the entries in the OtherIdentifyingInfo array.</span></span> <span data-ttu-id="c4745-351">請注意，這個陣列的每個專案都與 OtherIdentifyingInfo 中位於相同索引的專案相關。</span><span class="sxs-lookup"><span data-stu-id="c4745-351">Note, each entry of this array is related to the entry in OtherIdentifyingInfo that is located at the same index.</span></span>

<span data-ttu-id="c4745-352">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-352">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4745-353">**Index**</span><span class="sxs-lookup"><span data-stu-id="c4745-353">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-354">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c4745-354">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-355">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4745-356">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="c4745-356">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="c4745-357">資料分割的索引編號。</span><span class="sxs-lookup"><span data-stu-id="c4745-357">Index number of the partition.</span></span>

<span data-ttu-id="c4745-358">範例：1</span><span class="sxs-lookup"><span data-stu-id="c4745-358">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="c4745-359">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c4745-359">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-360">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="c4745-360">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-361">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4745-362">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="c4745-362">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c4745-363">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="c4745-363">Date the object was installed.</span></span> <span data-ttu-id="c4745-364">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="c4745-364">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c4745-365">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-365">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4745-366">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c4745-366">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-367">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c4745-367">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-368">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4745-369">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c4745-369">Last error code reported by the logical device.</span></span>

<span data-ttu-id="c4745-370">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-370">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4745-371">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="c4745-371">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-372">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c4745-372">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-373">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4745-374">限定詞： **淘汰**</span><span class="sxs-lookup"><span data-stu-id="c4745-374">Qualifiers: **Depricated**</span></span>
</dt> </dl>

<span data-ttu-id="c4745-375">裝置可在靜止狀態下執行的最長時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="c4745-375">Maximum time in milliseconds, that a Device can run in a Quiesced state.</span></span> <span data-ttu-id="c4745-376">裝置的狀態是在其 Availability 和 AdditionalAvailability 屬性中定義，其中的靜止是由值21所傳達。</span><span class="sxs-lookup"><span data-stu-id="c4745-376">A Device's state is defined in its Availability and AdditionalAvailability properties, where Quiesced is conveyed by the value 21.</span></span> <span data-ttu-id="c4745-377">時間限制的結束時會發生什麼狀況。</span><span class="sxs-lookup"><span data-stu-id="c4745-377">What occurs at the end of the time limit is device-specific.</span></span> <span data-ttu-id="c4745-378">裝置可能結束靜止狀態、離線或採取其他動作。</span><span class="sxs-lookup"><span data-stu-id="c4745-378">The Device may unquiesce, may offline or take other action.</span></span> <span data-ttu-id="c4745-379">值為0表示裝置可以無限期地保持靜止。</span><span class="sxs-lookup"><span data-stu-id="c4745-379">A value of 0 indicates that a Device can remain quiesced indefinitely.</span></span>

> [!Note]
>
> <span data-ttu-id="c4745-380">「MaxQuiesceTime 屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="c4745-380">"The MaxQuiesceTime property has been deprecated.</span></span> <span data-ttu-id="c4745-381">當您評估靜止的使用時，它會判斷這個單一屬性不適合用來描述裝置何時會自動離開靜止狀態。</span><span class="sxs-lookup"><span data-stu-id="c4745-381">When evaluating the use of Quiesce, it was determine that this single property is not adequate for describing when a device will automatically exit a quiescent state.</span></span> <span data-ttu-id="c4745-382">事實上，最可能的情況是，裝置離開靜止狀態的最可能案例是根據已排入佇列的未處理要求數目，而不是時間上限。</span><span class="sxs-lookup"><span data-stu-id="c4745-382">In fact, the most likely scenario for a device to exit a quiescent state was determined to be based on the number of outstanding requests queued rather than on a maximum time.</span></span> <span data-ttu-id="c4745-383">這將會重新評估，並于稍後重新置放。</span><span class="sxs-lookup"><span data-stu-id="c4745-383">This will be re-evaluated and repositioned later.</span></span> <span data-ttu-id="c4745-384">\\n</span><span class="sxs-lookup"><span data-stu-id="c4745-384">\\n</span></span>

 

<span data-ttu-id="c4745-385">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4745-386">**名稱**</span><span class="sxs-lookup"><span data-stu-id="c4745-386">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-387">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c4745-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-388">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4745-389">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="c4745-389">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c4745-390">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="c4745-390">Label by which the object is known.</span></span> <span data-ttu-id="c4745-391">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="c4745-391">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="c4745-392">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-392">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4745-393">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="c4745-393">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-394">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c4745-394">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-395">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-395">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4745-396">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrStorageSize ") </span><span class="sxs-lookup"><span data-stu-id="c4745-396">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="c4745-397">連續區塊總數，每個區塊會封鎖 **區塊** 屬性中包含的值大小，這會形成此儲存範圍。</span><span class="sxs-lookup"><span data-stu-id="c4745-397">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="c4745-398">您可以將 [ **區塊** ] 屬性的值乘以這個屬性的值，以計算儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="c4745-398">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="c4745-399">如果 **區塊** 的值是1，則這個屬性是儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="c4745-399">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="c4745-400">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="c4745-400">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="c4745-401">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-401">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4745-402">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="c4745-402">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-403">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c4745-403">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-404">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4745-405">可以用來識別 LogicalDevice 的其他資料（除了 DeviceID 資訊以外）的陣列。</span><span class="sxs-lookup"><span data-stu-id="c4745-405">Array that captures additional data, beyond DeviceID information, that could be used to identify a LogicalDevice.</span></span> <span data-ttu-id="c4745-406">其中一個範例是在這個屬性中保存裝置的作業系統使用者易記名稱。</span><span class="sxs-lookup"><span data-stu-id="c4745-406">One example would be to hold the Operating System's user friendly name for the Device in this property.</span></span> <span data-ttu-id="c4745-407">最大長度為256。</span><span class="sxs-lookup"><span data-stu-id="c4745-407">Maximum length is 256.</span></span>

<span data-ttu-id="c4745-408">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4745-409">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="c4745-409">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-410">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c4745-410">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-411">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4745-412">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="c4745-412">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c4745-413">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="c4745-413">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="c4745-414">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="c4745-414">Example: "\*PNP030b"</span></span>

<span data-ttu-id="c4745-415">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4745-416">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c4745-416">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-417">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="c4745-417">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c4745-418">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4745-419">指出邏輯裝置的特定電源相關功能。</span><span class="sxs-lookup"><span data-stu-id="c4745-419">Indicates the specific power-related capabilities of the logical device.</span></span> <span data-ttu-id="c4745-420">陣列值、0 = "未知"、1 = "不支援" 和 2 = "已停用" 是一目了然的。</span><span class="sxs-lookup"><span data-stu-id="c4745-420">The array values, 0="Unknown", 1="Not Supported" and 2="Disabled" are self-explanatory.</span></span> <span data-ttu-id="c4745-421">值 3 = "Enabled" 表示目前已啟用電源管理功能，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="c4745-421">The value, 3="Enabled" indicates that the power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span> <span data-ttu-id="c4745-422">「自動輸入的省電模式」 (4) 說明裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="c4745-422">"Power Saving Modes Entered Automatically" (4) describes that a device can change its power state based on usage or other criteria.</span></span> <span data-ttu-id="c4745-423">「電源狀態可設定」 (5) 表示支援 SetPowerState 方法。</span><span class="sxs-lookup"><span data-stu-id="c4745-423">"Power State Settable" (5) indicates that the SetPowerState method is supported.</span></span> <span data-ttu-id="c4745-424">「支援電源週期」 (6) 表示可以叫用 SetPowerState 方法，並將 >powerstate 輸入變數設定為 5 ( 「電源週期」 ) 。</span><span class="sxs-lookup"><span data-stu-id="c4745-424">"Power Cycling Supported" (6) indicates that the SetPowerState method can be invoked with the PowerState input variable set to 5 ("Power Cycle").</span></span> <span data-ttu-id="c4745-425">「受支援的支援時間」 (7) 表示可以叫用 SetPowerState 方法，並將 >powerstate 輸入變數設定為 5 ( 「電源週期」 ) 以及將 Time 參數設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="c4745-425">"Timed Power On Supported" (7) indicates that the SetPowerState method can be invoked with the PowerState input variable set to 5 ("Power Cycle") and the Time parameter set to a specific date and time, or interval, for power-on.</span></span>

<span data-ttu-id="c4745-426">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-426">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c4745-427">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c4745-427">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="c4745-428">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="c4745-428">**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c4745-429">**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="c4745-429">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c4745-430">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="c4745-430">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="c4745-431">**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="c4745-431">**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="c4745-432">可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="c4745-432">**Power State Settable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="c4745-433">支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="c4745-433">**Power Cycling Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="c4745-434">**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="c4745-434">**Timed Power On Supported** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c4745-435">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="c4745-435">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-436">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c4745-436">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-437">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4745-438">若 **為 True**，則裝置可以是電源管理 (可進入暫停模式，依此類推) 。</span><span class="sxs-lookup"><span data-stu-id="c4745-438">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="c4745-439">屬性不表示電源管理功能目前已啟用，只有邏輯裝置能夠進行電源管理。</span><span class="sxs-lookup"><span data-stu-id="c4745-439">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="c4745-440">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-440">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4745-441">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="c4745-441">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-442">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c4745-442">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-443">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4745-444">自上次電源週期起，此裝置已電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="c4745-444">The number of consecutive hours that this Device has been powered, since its last power cycle.</span></span>

<span data-ttu-id="c4745-445">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-445">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4745-446">**PrimaryPartition**</span><span class="sxs-lookup"><span data-stu-id="c4745-446">**PrimaryPartition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-447">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c4745-447">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-448">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4745-449">若 **為 True**，則這是主要磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="c4745-449">If **True**, this is the primary partition.</span></span>

<span data-ttu-id="c4745-450">這個屬性繼承自 [**CIM \_ DiskPartition**](cim-diskpartition.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-450">This property is inherited from [**CIM\_DiskPartition**](cim-diskpartition.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4745-451">**目的**</span><span class="sxs-lookup"><span data-stu-id="c4745-451">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-452">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c4745-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-453">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4745-454">媒體及其用途的描述。</span><span class="sxs-lookup"><span data-stu-id="c4745-454">Description of the media and its use.</span></span>

<span data-ttu-id="c4745-455">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-455">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4745-456">**RewritePartition**</span><span class="sxs-lookup"><span data-stu-id="c4745-456">**RewritePartition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-457">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c4745-457">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-458">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4745-459">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 裝置輸入和輸出結構的資料 \| [**分割 \_ 資訊**](/windows/desktop/api/winioctl/ns-winioctl-partition_information) \| RewritePartition」 ) </span><span class="sxs-lookup"><span data-stu-id="c4745-459">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**PARTITION\_INFORMATION**](/windows/desktop/api/winioctl/ns-winioctl-partition_information)\|RewritePartition")</span></span>
</dt> </dl>

<span data-ttu-id="c4745-460">若 **為 True**，表示資料分割資訊已變更。</span><span class="sxs-lookup"><span data-stu-id="c4745-460">If **True**, the partition information has changed.</span></span> <span data-ttu-id="c4745-461">當您使用 [ [**IOCTL \_ 磁片 \_ 設定磁片 \_ 磁碟機 \_**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout) 配置]) 來變更分割 (時，系統會使用這個屬性來判斷哪些分割區已變更，且需要重新撰寫其資訊。</span><span class="sxs-lookup"><span data-stu-id="c4745-461">When you change a partition (with [**IOCTL\_DISK\_SET\_DRIVE\_LAYOUT**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout)), the system uses this property to determine which partitions have changed and need their information rewritten.</span></span> <span data-ttu-id="c4745-462">若 **為 TRUE**，則必須重寫資料分割。</span><span class="sxs-lookup"><span data-stu-id="c4745-462">If **TRUE**, the partition must be rewritten.</span></span>

</dd> <dt>

<span data-ttu-id="c4745-463">**大小**</span><span class="sxs-lookup"><span data-stu-id="c4745-463">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-464">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c4745-464">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-465">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-465">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4745-466">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| File 函數 \| ReadFile" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="c4745-466">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c4745-467">分割區的總大小。</span><span class="sxs-lookup"><span data-stu-id="c4745-467">Total size of the partition.</span></span>

<span data-ttu-id="c4745-468">範例：1059045376</span><span class="sxs-lookup"><span data-stu-id="c4745-468">Example: 1059045376</span></span>

<span data-ttu-id="c4745-469">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="c4745-469">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c4745-470">**StartingOffset**</span><span class="sxs-lookup"><span data-stu-id="c4745-470">**StartingOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-471">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c4745-471">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-472">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4745-473">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| File 函數 \| ReadFile" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="c4745-473">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c4745-474">分割區的起始位移 (位元組) 。</span><span class="sxs-lookup"><span data-stu-id="c4745-474">Starting offset (in bytes) of the partition.</span></span>

<span data-ttu-id="c4745-475">範例：32256</span><span class="sxs-lookup"><span data-stu-id="c4745-475">Example: 32256</span></span>

<span data-ttu-id="c4745-476">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="c4745-476">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c4745-477">**狀態**</span><span class="sxs-lookup"><span data-stu-id="c4745-477">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-478">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c4745-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-479">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-479">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4745-480">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="c4745-480">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c4745-481">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="c4745-481">Current status of the object.</span></span> <span data-ttu-id="c4745-482">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="c4745-482">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c4745-483">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="c4745-483">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="c4745-484">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="c4745-484">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c4745-485">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="c4745-485">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c4745-486">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="c4745-486">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c4745-487">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-487">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c4745-488">值如下：</span><span class="sxs-lookup"><span data-stu-id="c4745-488">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c4745-489">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="c4745-489">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c4745-490">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="c4745-490">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c4745-491">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="c4745-491">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c4745-492">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="c4745-492">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c4745-493">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="c4745-493">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c4745-494">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="c4745-494">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c4745-495">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="c4745-495">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c4745-496">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="c4745-496">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c4745-497">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="c4745-497">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c4745-498">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="c4745-498">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c4745-499">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="c4745-499">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c4745-500">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="c4745-500">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c4745-501">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c4745-501">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-502">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c4745-502">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-503">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-503">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4745-504">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="c4745-504">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c4745-505">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="c4745-505">State of the logical device.</span></span> <span data-ttu-id="c4745-506">如果此屬性不適用於邏輯裝置，則應該使用值 5 ( 「不適用」 ) 。</span><span class="sxs-lookup"><span data-stu-id="c4745-506">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="c4745-507">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-507">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c4745-508">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c4745-508">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c4745-509">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="c4745-509">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c4745-510">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="c4745-510">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c4745-511">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="c4745-511">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c4745-512">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="c4745-512">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c4745-513">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c4745-513">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-514">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c4745-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-515">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-515">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4745-516">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c4745-516">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c4745-517">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="c4745-517">Creation class name of the scoping system.</span></span>

<span data-ttu-id="c4745-518">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-518">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4745-519">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c4745-519">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-520">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c4745-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-521">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4745-522">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c4745-522">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c4745-523">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4745-523">Name of the scoping system.</span></span>

<span data-ttu-id="c4745-524">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-524">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4745-525">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="c4745-525">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-526">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c4745-526">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-527">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-527">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4745-528">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="c4745-528">The total number of hours that this device has been powered.</span></span>

<span data-ttu-id="c4745-529">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-529">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4745-530">**型別**</span><span class="sxs-lookup"><span data-stu-id="c4745-530">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4745-531">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c4745-531">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4745-532">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4745-532">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4745-533">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| PartitionRecord \| dwPartitionType" ) </span><span class="sxs-lookup"><span data-stu-id="c4745-533">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|PartitionRecord\|dwPartitionType")</span></span>
</dt> </dl>

<span data-ttu-id="c4745-534">資料分割的類型。</span><span class="sxs-lookup"><span data-stu-id="c4745-534">Type of the partition.</span></span>

<span data-ttu-id="c4745-535">值如下：</span><span class="sxs-lookup"><span data-stu-id="c4745-535">The values are:</span></span>

<dl> <dd><span data-ttu-id="c4745-536">尚未</span><span class="sxs-lookup"><span data-stu-id="c4745-536">"Unused"</span></span></dd> <dd><span data-ttu-id="c4745-537">"12-bit FAT"</span><span class="sxs-lookup"><span data-stu-id="c4745-537">"12-bit FAT"</span></span></dd> <dd><span data-ttu-id="c4745-538">「Xenix 類型1」</span><span class="sxs-lookup"><span data-stu-id="c4745-538">"Xenix Type 1"</span></span></dd> <dd><span data-ttu-id="c4745-539">「Xenix 類型2」</span><span class="sxs-lookup"><span data-stu-id="c4745-539">"Xenix Type 2"</span></span></dd> <dd><span data-ttu-id="c4745-540">"16-bit FAT"</span><span class="sxs-lookup"><span data-stu-id="c4745-540">"16-bit FAT"</span></span></dd> <dd><span data-ttu-id="c4745-541">「擴充的資料分割」</span><span class="sxs-lookup"><span data-stu-id="c4745-541">"Extended Partition"</span></span></dd> <dd><span data-ttu-id="c4745-542">「MS-DOS V4 龐大」</span><span class="sxs-lookup"><span data-stu-id="c4745-542">"MS-DOS V4 Huge"</span></span></dd> <dd><span data-ttu-id="c4745-543">「可安裝的檔案系統」</span><span class="sxs-lookup"><span data-stu-id="c4745-543">"Installable File System"</span></span></dd> <dd><span data-ttu-id="c4745-544">「PowerPC 參考平臺」</span><span class="sxs-lookup"><span data-stu-id="c4745-544">"PowerPC Reference Platform"</span></span></dd> <dd><span data-ttu-id="c4745-545">UNIX</span><span class="sxs-lookup"><span data-stu-id="c4745-545">"UNIX"</span></span></dd> <dd><span data-ttu-id="c4745-546">NFS</span><span class="sxs-lookup"><span data-stu-id="c4745-546">"NTFS"</span></span></dd> <dd><span data-ttu-id="c4745-547">"Win95 w/Extended Int 13"</span><span class="sxs-lookup"><span data-stu-id="c4745-547">"Win95 w/Extended Int 13"</span></span></dd> <dd><span data-ttu-id="c4745-548">「擴充的 w/Extended Int 13」</span><span class="sxs-lookup"><span data-stu-id="c4745-548">"Extended w/Extended Int 13"</span></span></dd> <dd><span data-ttu-id="c4745-549">「邏輯磁片管理員」</span><span class="sxs-lookup"><span data-stu-id="c4745-549">"Logical Disk Manager"</span></span></dd> <dd><span data-ttu-id="c4745-550">不明</span><span class="sxs-lookup"><span data-stu-id="c4745-550">"Unknown"</span></span></dd> </dl>

<dt>

<span id="Unused"></span><span id="unused"></span><span id="UNUSED"></span>

<span data-ttu-id="c4745-551">**未使用** ( 「未使用」 ) </span><span class="sxs-lookup"><span data-stu-id="c4745-551">**Unused** ("Unused")</span></span>


</dt> <dd></dd> <dt>

<span id="12-bit_FAT"></span><span id="12-bit_fat"></span><span id="12-BIT_FAT"></span>

<span data-ttu-id="c4745-552">**12 位 fat** ( "12 bit fat" ) </span><span class="sxs-lookup"><span data-stu-id="c4745-552">**12-bit FAT** ("12-bit FAT")</span></span>


</dt> <dd></dd> <dt>

<span id="Xenix_Type_1"></span><span id="xenix_type_1"></span><span id="XENIX_TYPE_1"></span>

<span data-ttu-id="c4745-553">**Xenix 類型 1** ( "Xenix type 1" ) </span><span class="sxs-lookup"><span data-stu-id="c4745-553">**Xenix Type 1** ("Xenix Type 1")</span></span>


</dt> <dd></dd> <dt>

<span id="Xenix_Type_2"></span><span id="xenix_type_2"></span><span id="XENIX_TYPE_2"></span>

<span data-ttu-id="c4745-554">**Xenix 類型 2** ( "Xenix type 2" ) </span><span class="sxs-lookup"><span data-stu-id="c4745-554">**Xenix Type 2** ("Xenix Type 2")</span></span>


</dt> <dd></dd> <dt>

<span id="16-bit_FAT"></span><span id="16-bit_fat"></span><span id="16-BIT_FAT"></span>

<span data-ttu-id="c4745-555">**16 位 fat** ( "16-bit fat" ) </span><span class="sxs-lookup"><span data-stu-id="c4745-555">**16-bit FAT** ("16-bit FAT")</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_Partition"></span><span id="extended_partition"></span><span id="EXTENDED_PARTITION"></span>

<span data-ttu-id="c4745-556">**擴充磁碟分割** ( 「擴充資料分割」 ) </span><span class="sxs-lookup"><span data-stu-id="c4745-556">**Extended Partition** ("Extended Partition")</span></span>


</dt> <dd></dd> <dt>

<span id="MS-DOS_V4_Huge"></span><span id="ms-dos_v4_huge"></span><span id="MS-DOS_V4_HUGE"></span>

<span data-ttu-id="c4745-557">**Ms-dos V4 龐大** ( 「Ms-dos v4 龐大」 ) </span><span class="sxs-lookup"><span data-stu-id="c4745-557">**MS-DOS V4 Huge** ("MS-DOS V4 Huge")</span></span>


</dt> <dd></dd> <dt>

<span id="Installable_File_System"></span><span id="installable_file_system"></span><span id="INSTALLABLE_FILE_SYSTEM"></span>

<span data-ttu-id="c4745-558">可 **安裝的檔案系統** ( 「可安裝的檔案系統」 ) </span><span class="sxs-lookup"><span data-stu-id="c4745-558">**Installable File System** ("Installable File System")</span></span>


</dt> <dd></dd> <dt>

<span id="PowerPC_Reference_Platform"></span><span id="powerpc_reference_platform"></span><span id="POWERPC_REFERENCE_PLATFORM"></span>

<span data-ttu-id="c4745-559">**PowerPC 參考平臺** ( 「PowerPC 參考平臺」 ) </span><span class="sxs-lookup"><span data-stu-id="c4745-559">**PowerPC Reference Platform** ("PowerPC Reference Platform")</span></span>


</dt> <dd></dd> <dt>

<span id="UNIX"></span><span id="unix"></span>

<span data-ttu-id="c4745-560">**Unix** ( "unix" ) </span><span class="sxs-lookup"><span data-stu-id="c4745-560">**UNIX** ("UNIX")</span></span>


</dt> <dd></dd> <dt>

<span id="NTFS"></span><span id="ntfs"></span>

<span data-ttu-id="c4745-561">**Ntfs** ( "ntfs" ) </span><span class="sxs-lookup"><span data-stu-id="c4745-561">**NTFS** ("NTFS")</span></span>


</dt> <dd></dd> <dt>

<span id="Win95_w_Extended_Int_13"></span><span id="win95_w_extended_int_13"></span><span id="WIN95_W_EXTENDED_INT_13"></span>

<span data-ttu-id="c4745-562">**Win95 w/Extended int 13** ( "Win95 w/extended int 13" ) </span><span class="sxs-lookup"><span data-stu-id="c4745-562">**Win95 w/Extended Int 13** ("Win95 w/Extended Int 13")</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_w_Extended_Int_13"></span><span id="extended_w_extended_int_13"></span><span id="EXTENDED_W_EXTENDED_INT_13"></span>

<span data-ttu-id="c4745-563">**外延 w/Extended int 13** ( 「延長 w/擴充的 int 13」 ) </span><span class="sxs-lookup"><span data-stu-id="c4745-563">**Extended w/Extended Int 13** ("Extended w/Extended Int 13")</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk_Manager"></span><span id="logical_disk_manager"></span><span id="LOGICAL_DISK_MANAGER"></span>

<span data-ttu-id="c4745-564">**邏輯磁片管理員** ( 「邏輯磁片管理員」 ) </span><span class="sxs-lookup"><span data-stu-id="c4745-564">**Logical Disk Manager** ("Logical Disk Manager")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c4745-565">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="c4745-565">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="c4745-566"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c4745-566"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="c4745-567">備註</span><span class="sxs-lookup"><span data-stu-id="c4745-567">Remarks</span></span>

<span data-ttu-id="c4745-568">**Win32 \_ DiskPartition** 類別衍生自 [**CIM \_ DiskPartition**](cim-diskpartition.md)。</span><span class="sxs-lookup"><span data-stu-id="c4745-568">The **Win32\_DiskPartition** class is derived from [**CIM\_DiskPartition**](cim-diskpartition.md).</span></span>

<span data-ttu-id="c4745-569">磁碟分割是實體磁片磁碟機的結構化分割。</span><span class="sxs-lookup"><span data-stu-id="c4745-569">A partition is a structural division of a physical disk drive.</span></span> <span data-ttu-id="c4745-570">雖然磁片磁碟機可以包含單一磁碟分割，但較大的磁片區通常會分成多個磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="c4745-570">Although a drive can contain a single partition, larger volumes are often divided into multiple partitions.</span></span> <span data-ttu-id="c4745-571">這就是為什麼您的電腦只有一個實體硬碟，才能使用 C、D 和 E 磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="c4745-571">This is why you might have drives C, D, and E even though your computer has only a single physical hard disk.</span></span>

<span data-ttu-id="c4745-572">Windows 支援下列磁碟分割類型：</span><span class="sxs-lookup"><span data-stu-id="c4745-572">Windows supports the following partition types:</span></span>

-   <span data-ttu-id="c4745-573">主要磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="c4745-573">Primary partition.</span></span> <span data-ttu-id="c4745-574">這是唯一可以安裝作業系統的資料分割類型。</span><span class="sxs-lookup"><span data-stu-id="c4745-574">This is the only type of partition that can have an operating system installed.</span></span> <span data-ttu-id="c4745-575">每個磁片磁碟機最多可以有四個主要磁碟分割，每個磁碟分割都指派不同的磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="c4745-575">Each drive can have as many as four primary partitions, each assigned a different drive letter.</span></span>
-   <span data-ttu-id="c4745-576">擴充的資料分割。</span><span class="sxs-lookup"><span data-stu-id="c4745-576">Extended partition.</span></span> <span data-ttu-id="c4745-577">可細分為多個邏輯磁碟機的額外磁碟分割，每個都指派一個唯一的磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="c4745-577">An additional partition that can be subdivided into multiple logical drives, each assigned a unique drive letter.</span></span> <span data-ttu-id="c4745-578">磁片磁碟機只能有一個擴充磁碟分割;不過，您可以將此分割區分割成多個邏輯磁碟機。</span><span class="sxs-lookup"><span data-stu-id="c4745-578">A drive can have only one extended partition; however, you can divide this partition into multiple logical drives.</span></span> <span data-ttu-id="c4745-579">這可讓磁片擁有超過四個允許的主要磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="c4745-579">This enables a disk to have more than just the four allowed primary partitions.</span></span>
-   <span data-ttu-id="c4745-580">系統磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="c4745-580">System partition.</span></span> <span data-ttu-id="c4745-581">包含作業系統的任何主要磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="c4745-581">Any primary partition containing an operating system.</span></span>

<span data-ttu-id="c4745-582">磁碟分割可以告訴您實際使用的實體磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="c4745-582">Partitions can tell you how a physical disk drive is actually being used.</span></span> <span data-ttu-id="c4745-583">藉由檢查磁片上的實體磁碟分割，您可以判斷下列類型的專案：</span><span class="sxs-lookup"><span data-stu-id="c4745-583">By examining the physical partitions on a disk, you can determine the following types of things:</span></span>

-   <span data-ttu-id="c4745-584">磁片如何分成邏輯磁碟機。</span><span class="sxs-lookup"><span data-stu-id="c4745-584">How the disk has been divided into logical drives.</span></span>
-   <span data-ttu-id="c4745-585">如果磁片上有未分區的空間可用。</span><span class="sxs-lookup"><span data-stu-id="c4745-585">If there is unpartitioned space available on the disk.</span></span> <span data-ttu-id="c4745-586">這可以藉由將磁片上的所有磁碟分割大小減去磁片本身的大小來決定。</span><span class="sxs-lookup"><span data-stu-id="c4745-586">This can be determined by subtracting the size of all the partitions on a disk from the size of the disk itself.</span></span>
-   <span data-ttu-id="c4745-587">如果您可以從該磁片將電腦開機 (也就是磁片包含開機磁碟分割) 。</span><span class="sxs-lookup"><span data-stu-id="c4745-587">If you can boot the computer from that disk (that is, does the disk contain a boot partition).</span></span>

<span data-ttu-id="c4745-588">您可以使用 **Win32 \_ DiskPartition** 類別來解決這些問題。</span><span class="sxs-lookup"><span data-stu-id="c4745-588">All these questions can be resolved by using the **Win32\_DiskPartition** class.</span></span>

## <a name="examples"></a><span data-ttu-id="c4745-589">範例</span><span class="sxs-lookup"><span data-stu-id="c4745-589">Examples</span></span>

<span data-ttu-id="c4745-590">下列 PowerShell 程式碼範例會檢查電腦上的磁片對齊方式：如果位移是小數，則磁片未正確對齊。</span><span class="sxs-lookup"><span data-stu-id="c4745-590">The following PowerShell code sample checks the alignment of disks on a computer: if the offset is fractional, the disk is not aligned correctly.</span></span>


```PowerShell
$wql = "SELECT DiskIndex,Index,StartingOffset FROM Win32_DiskPartition"
Get-WmiObject -Query $wql -ComputerName '.' | Select-Object DiskIndex,Index,@{Name='Offset (KB)';Expression={$_.StartingOffset / 1024}} | Format-Table -AutoSize
```



## <a name="requirements"></a><span data-ttu-id="c4745-591">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4745-591">Requirements</span></span>



| <span data-ttu-id="c4745-592">需求</span><span class="sxs-lookup"><span data-stu-id="c4745-592">Requirement</span></span> | <span data-ttu-id="c4745-593">值</span><span class="sxs-lookup"><span data-stu-id="c4745-593">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4745-594">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c4745-594">Minimum supported client</span></span><br/> | <span data-ttu-id="c4745-595">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4745-595">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c4745-596">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c4745-596">Minimum supported server</span></span><br/> | <span data-ttu-id="c4745-597">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4745-597">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c4745-598">命名空間</span><span class="sxs-lookup"><span data-stu-id="c4745-598">Namespace</span></span><br/>                | <span data-ttu-id="c4745-599">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c4745-599">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c4745-600">MOF</span><span class="sxs-lookup"><span data-stu-id="c4745-600">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4745-601"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4745-601"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4745-602">DLL</span><span class="sxs-lookup"><span data-stu-id="c4745-602">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4745-603"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4745-603"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4745-604">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4745-604">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4745-605">**CIM \_ DiskPartition**</span><span class="sxs-lookup"><span data-stu-id="c4745-605">**CIM\_DiskPartition**</span></span>](cim-diskpartition.md)
</dt> <dt>

<span data-ttu-id="c4745-606">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c4745-606">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c4745-607">WMI 工作：磁片和檔案系統</span><span class="sxs-lookup"><span data-stu-id="c4745-607">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

