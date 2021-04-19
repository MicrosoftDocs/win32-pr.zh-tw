---
description: 表示在執行 Windows 的電腦系統上，解析為實際本機儲存裝置的資料來源。
ms.assetid: 134a90cc-b2c3-4ade-a317-b96c4aabe63d
ms.tgt_platform: multiple
title: Win32_LogicalDisk 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk
- Win32_LogicalDisk.Reset
- Win32_LogicalDisk.SetPowerState
- Win32_LogicalDisk.Access
- Win32_LogicalDisk.Availability
- Win32_LogicalDisk.BlockSize
- Win32_LogicalDisk.Caption
- Win32_LogicalDisk.Compressed
- Win32_LogicalDisk.ConfigManagerErrorCode
- Win32_LogicalDisk.ConfigManagerUserConfig
- Win32_LogicalDisk.CreationClassName
- Win32_LogicalDisk.Description
- Win32_LogicalDisk.DeviceID
- Win32_LogicalDisk.DriveType
- Win32_LogicalDisk.ErrorCleared
- Win32_LogicalDisk.ErrorDescription
- Win32_LogicalDisk.ErrorMethodology
- Win32_LogicalDisk.FileSystem
- Win32_LogicalDisk.FreeSpace
- Win32_LogicalDisk.InstallDate
- Win32_LogicalDisk.LastErrorCode
- Win32_LogicalDisk.MaximumComponentLength
- Win32_LogicalDisk.MediaType
- Win32_LogicalDisk.Name
- Win32_LogicalDisk.NumberOfBlocks
- Win32_LogicalDisk.PNPDeviceID
- Win32_LogicalDisk.PowerManagementCapabilities
- Win32_LogicalDisk.PowerManagementSupported
- Win32_LogicalDisk.ProviderName
- Win32_LogicalDisk.Purpose
- Win32_LogicalDisk.QuotasDisabled
- Win32_LogicalDisk.QuotasIncomplete
- Win32_LogicalDisk.QuotasRebuilding
- Win32_LogicalDisk.Size
- Win32_LogicalDisk.Status
- Win32_LogicalDisk.StatusInfo
- Win32_LogicalDisk.SupportsDiskQuotas
- Win32_LogicalDisk.SupportsFileBasedCompression
- Win32_LogicalDisk.SystemCreationClassName
- Win32_LogicalDisk.SystemName
- Win32_LogicalDisk.VolumeDirty
- Win32_LogicalDisk.VolumeName
- Win32_LogicalDisk.VolumeSerialNumber
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ad1472f14e73d06c19ccc0808794a47f7588cf9b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973760"
---
# <a name="win32_logicaldisk-class"></a><span data-ttu-id="0765a-103">Win32 \_ LogicalDisk 類別</span><span class="sxs-lookup"><span data-stu-id="0765a-103">Win32\_LogicalDisk class</span></span>

<span data-ttu-id="0765a-104">**Win32 \_ LogicalDisk** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表在執行 Windows 的電腦系統上，解析為實際本機儲存裝置的資料來源。</span><span class="sxs-lookup"><span data-stu-id="0765a-104">The **Win32\_LogicalDisk** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a data source that resolves to an actual local storage device on a computer system running Windows.</span></span>

<span data-ttu-id="0765a-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0765a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0765a-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="0765a-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0765a-107">語法</span><span class="sxs-lookup"><span data-stu-id="0765a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4B7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LogicalDisk : CIM_LogicalDisk
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
  uint32   DriveType;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  string   FileSystem;
  uint64   FreeSpace;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaximumComponentLength;
  uint32   MediaType;
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
  string   Size;
  string   Status;
  uint16   StatusInfo;
  boolean  SupportsDiskQuotas;
  boolean  SupportsFileBasedCompression;
  string   SystemCreationClassName;
  string   SystemName;
  boolean  VolumeDirty;
  string   VolumeName;
  string   VolumeSerialNumber;
};
```

## <a name="members"></a><span data-ttu-id="0765a-108">成員</span><span class="sxs-lookup"><span data-stu-id="0765a-108">Members</span></span>

<span data-ttu-id="0765a-109">**Win32 \_ LogicalDisk** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0765a-109">The **Win32\_LogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="0765a-110">方法</span><span class="sxs-lookup"><span data-stu-id="0765a-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="0765a-111">屬性</span><span class="sxs-lookup"><span data-stu-id="0765a-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0765a-112">方法</span><span class="sxs-lookup"><span data-stu-id="0765a-112">Methods</span></span>

<span data-ttu-id="0765a-113">**Win32 \_ LogicalDisk** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="0765a-113">The **Win32\_LogicalDisk** class has these methods.</span></span>



| <span data-ttu-id="0765a-114">方法</span><span class="sxs-lookup"><span data-stu-id="0765a-114">Method</span></span>                                                                             | <span data-ttu-id="0765a-115">描述</span><span class="sxs-lookup"><span data-stu-id="0765a-115">Description</span></span>                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0765a-116">**Chkdsk**</span><span class="sxs-lookup"><span data-stu-id="0765a-116">**Chkdsk**</span></span>](chkdsk-method-in-class-win32-logicaldisk.md)                         | <span data-ttu-id="0765a-117">在磁片上叫用 [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) 操作。</span><span class="sxs-lookup"><span data-stu-id="0765a-117">Invokes the [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) operation on the disk.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="0765a-118">**ExcludeFromAutochk**</span><span class="sxs-lookup"><span data-stu-id="0765a-118">**ExcludeFromAutochk**</span></span>](excludefromautochk-method-in-class-win32-logicaldisk.md) | <span data-ttu-id="0765a-119">在下次重新開機時，從 [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) 作業中排除要執行的磁片。</span><span class="sxs-lookup"><span data-stu-id="0765a-119">Excludes disks from the [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) operation to be run at the next restart.</span></span><br/>                                                                                      |
| <span data-ttu-id="0765a-120">**重設**</span><span class="sxs-lookup"><span data-stu-id="0765a-120">**Reset**</span></span>                                                                          | <span data-ttu-id="0765a-121">未實作。</span><span class="sxs-lookup"><span data-stu-id="0765a-121">Not implemented.</span></span> <span data-ttu-id="0765a-122">如需如何執行此方法的詳細資訊，請參閱 [**CIM \_ LogicalDisk**](cim-logicaldisk.md)中的 [**Reset**](reset-method-in-class-cim-controller.md)方法以取得檔。</span><span class="sxs-lookup"><span data-stu-id="0765a-122">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDisk**](cim-logicaldisk.md) for documentation.</span></span><br/> |
| [<span data-ttu-id="0765a-123">**ScheduleAutoChk**</span><span class="sxs-lookup"><span data-stu-id="0765a-123">**ScheduleAutoChk**</span></span>](scheduleautochk-method-in-class-win32-logicaldisk.md)       | <span data-ttu-id="0765a-124">排定在下次重新開機時執行 [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) （如果已設定中途位）。</span><span class="sxs-lookup"><span data-stu-id="0765a-124">Schedules [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) to be run at the next restart if the dirty bit has been set.</span></span><br/>                                                                                |
| <span data-ttu-id="0765a-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0765a-125">**SetPowerState**</span></span>                                                                  | <span data-ttu-id="0765a-126">未實作。</span><span class="sxs-lookup"><span data-stu-id="0765a-126">Not implemented.</span></span> <span data-ttu-id="0765a-127">如需如何執行此方法的詳細資訊，請參閱 [**CIM \_ LogicalDisk**](cim-logicaldisk.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="0765a-127">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span><br/>   |



 

### <a name="properties"></a><span data-ttu-id="0765a-128">屬性</span><span class="sxs-lookup"><span data-stu-id="0765a-128">Properties</span></span>

<span data-ttu-id="0765a-129">**Win32 \_ LogicalDisk** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0765a-129">The **Win32\_LogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0765a-130">**存取**</span><span class="sxs-lookup"><span data-stu-id="0765a-130">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-131">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0765a-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0765a-133">可用的媒體存取類型。</span><span class="sxs-lookup"><span data-stu-id="0765a-133">Type of media access available.</span></span>

<span data-ttu-id="0765a-134">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="0765a-134">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0765a-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="0765a-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="0765a-136"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**可讀取** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="0765a-136"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="0765a-137"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>可 **寫入** (2) </span><span class="sxs-lookup"><span data-stu-id="0765a-137"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-138">可寫入</span><span class="sxs-lookup"><span data-stu-id="0765a-138">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="0765a-139"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>支援 (3) 的 **讀取/寫入**</span><span class="sxs-lookup"><span data-stu-id="0765a-139"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="0765a-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**撰寫一次** (4) </span><span class="sxs-lookup"><span data-stu-id="0765a-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0765a-141">**可用性**</span><span class="sxs-lookup"><span data-stu-id="0765a-141">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-142">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0765a-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0765a-144">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="0765a-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="0765a-145">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="0765a-145">Availability and status of the device.</span></span>

<span data-ttu-id="0765a-146">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0765a-146">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0765a-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="0765a-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0765a-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="0765a-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="0765a-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="0765a-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-150">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="0765a-150">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="0765a-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="0765a-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="0765a-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="0765a-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0765a-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="0765a-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="0765a-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="0765a-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="0765a-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="0765a-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-156">離線</span><span class="sxs-lookup"><span data-stu-id="0765a-156">Offline</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="0765a-157"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="0765a-157"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0765a-158"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="0765a-158"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="0765a-159"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="0765a-159"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="0765a-160"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="0765a-160"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="0765a-161"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="0765a-161"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-162">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="0765a-162">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="0765a-163"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="0765a-163"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-164">裝置處於省電狀態，但仍正常運作，而且可能會顯示效能下降。</span><span class="sxs-lookup"><span data-stu-id="0765a-164">The device is in a power save state, but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="0765a-165"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="0765a-165"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-166">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="0765a-166">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="0765a-167"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="0765a-167"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="0765a-168"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="0765a-168"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-169">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="0765a-169">The device is in a warning state, but also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="0765a-170"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="0765a-170"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-171">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="0765a-171">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="0765a-172"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="0765a-172"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-173">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="0765a-173">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="0765a-174"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="0765a-174"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-175">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="0765a-175">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="0765a-176"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="0765a-176"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-177">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="0765a-177">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0765a-178">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="0765a-178">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-179">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="0765a-179">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0765a-181">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrStorageAllocationUnits ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="0765a-181">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0765a-182">形成此儲存區之區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="0765a-182">Size, in bytes, of the blocks that form this storage extent.</span></span> <span data-ttu-id="0765a-183">如果未知或區塊概念無效 (例如，針對匯總範圍、記憶體或邏輯磁片) ，請輸入1。</span><span class="sxs-lookup"><span data-stu-id="0765a-183">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter 1.</span></span>

<span data-ttu-id="0765a-184">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="0765a-184">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="0765a-185">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="0765a-185">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0765a-186">**標題**</span><span class="sxs-lookup"><span data-stu-id="0765a-186">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-187">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0765a-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0765a-189">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="0765a-189">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0765a-190">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="0765a-190">Short description of the object a one-line string.</span></span>

<span data-ttu-id="0765a-191">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0765a-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0765a-192">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="0765a-192">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-193">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0765a-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0765a-195">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 檔案系統函式 \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| FS \_ 音量 \_ 已 \_ 壓縮」 ) </span><span class="sxs-lookup"><span data-stu-id="0765a-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)\|FS\_VOL\_IS\_COMPRESSED")</span></span>
</dt> </dl>

<span data-ttu-id="0765a-196">若 **為 True**，則邏輯磁片區會以單一壓縮的實體形式存在，例如 DoubleSpace 磁片區。</span><span class="sxs-lookup"><span data-stu-id="0765a-196">If **True**, the logical volume exists as a single compressed entity, such as a DoubleSpace volume.</span></span> <span data-ttu-id="0765a-197">如果支援以檔案為基礎的壓縮，例如 NTFS，則此屬性為 **False**。</span><span class="sxs-lookup"><span data-stu-id="0765a-197">If file based compression is supported, such as on NTFS, this property is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="0765a-198">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0765a-198">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-199">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0765a-199">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0765a-201">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="0765a-201">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0765a-202">Windows 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0765a-202">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="0765a-203">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0765a-203">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="0765a-204"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="0765a-204"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="0765a-205"> (0)</span><span class="sxs-lookup"><span data-stu-id="0765a-205">(0)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-206">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="0765a-206">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="0765a-207"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="0765a-207"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="0765a-208">(1)</span><span class="sxs-lookup"><span data-stu-id="0765a-208">(1)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-209">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="0765a-209">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0765a-210"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="0765a-210"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="0765a-211">(2)</span><span class="sxs-lookup"><span data-stu-id="0765a-211">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="0765a-212"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="0765a-212"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="0765a-213">(3)</span><span class="sxs-lookup"><span data-stu-id="0765a-213">(3)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-214">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="0765a-214">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0765a-215"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="0765a-215"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="0765a-216">(4)</span><span class="sxs-lookup"><span data-stu-id="0765a-216">(4)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-217">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="0765a-217">Device is not working properly.</span></span> <span data-ttu-id="0765a-218">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="0765a-218">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="0765a-219"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="0765a-219"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="0765a-220">(5)</span><span class="sxs-lookup"><span data-stu-id="0765a-220">(5)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-221">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="0765a-221">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="0765a-222"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="0765a-222"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="0765a-223">(6)</span><span class="sxs-lookup"><span data-stu-id="0765a-223">(6)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-224">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="0765a-224">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="0765a-225"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="0765a-225"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="0765a-226">(7)</span><span class="sxs-lookup"><span data-stu-id="0765a-226">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="0765a-227"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="0765a-227"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="0765a-228">(8)</span><span class="sxs-lookup"><span data-stu-id="0765a-228">(8)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-229">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="0765a-229">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="0765a-230"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="0765a-230"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="0765a-231">(9)</span><span class="sxs-lookup"><span data-stu-id="0765a-231">(9)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-232">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="0765a-232">Device is not working properly.</span></span> <span data-ttu-id="0765a-233">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="0765a-233">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="0765a-234"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="0765a-234"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="0765a-235">(10)</span><span class="sxs-lookup"><span data-stu-id="0765a-235">(10)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-236">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="0765a-236">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="0765a-237"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="0765a-237"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="0765a-238">(11)</span><span class="sxs-lookup"><span data-stu-id="0765a-238">(11)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-239">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="0765a-239">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="0765a-240"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="0765a-240"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="0765a-241"> (12) </span><span class="sxs-lookup"><span data-stu-id="0765a-241">(12)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-242">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="0765a-242">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="0765a-243"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="0765a-243"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="0765a-244">(13)</span><span class="sxs-lookup"><span data-stu-id="0765a-244">(13)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-245">Windows 無法驗證裝置資源。</span><span class="sxs-lookup"><span data-stu-id="0765a-245">Windows cannot verify the device resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="0765a-246"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="0765a-246"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="0765a-247">(14)</span><span class="sxs-lookup"><span data-stu-id="0765a-247">(14)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-248">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="0765a-248">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="0765a-249"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="0765a-249"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="0765a-250">(15)</span><span class="sxs-lookup"><span data-stu-id="0765a-250">(15)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-251">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="0765a-251">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="0765a-252"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="0765a-252"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="0765a-253">(16)</span><span class="sxs-lookup"><span data-stu-id="0765a-253">(16)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-254">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="0765a-254">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="0765a-255"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="0765a-255"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="0765a-256">(17)</span><span class="sxs-lookup"><span data-stu-id="0765a-256">(17)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-257">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="0765a-257">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0765a-258"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="0765a-258"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="0765a-259">(18)</span><span class="sxs-lookup"><span data-stu-id="0765a-259">(18)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-260">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="0765a-260">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="0765a-261"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="0765a-261"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="0765a-262">(19)</span><span class="sxs-lookup"><span data-stu-id="0765a-262">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0765a-263"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="0765a-263"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="0765a-264">(20)</span><span class="sxs-lookup"><span data-stu-id="0765a-264">(20)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-265">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="0765a-265">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="0765a-266"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="0765a-266"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="0765a-267">(21)</span><span class="sxs-lookup"><span data-stu-id="0765a-267">(21)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-268">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="0765a-268">System failure.</span></span> <span data-ttu-id="0765a-269">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="0765a-269">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="0765a-270">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="0765a-270">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="0765a-271"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="0765a-271"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="0765a-272">(22)</span><span class="sxs-lookup"><span data-stu-id="0765a-272">(22)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-273">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="0765a-273">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="0765a-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="0765a-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="0765a-275">(23)</span><span class="sxs-lookup"><span data-stu-id="0765a-275">(23)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-276">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="0765a-276">System failure.</span></span> <span data-ttu-id="0765a-277">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="0765a-277">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="0765a-278"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="0765a-278"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="0765a-279">(24)</span><span class="sxs-lookup"><span data-stu-id="0765a-279">(24)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-280">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="0765a-280">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0765a-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="0765a-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0765a-282">(25)</span><span class="sxs-lookup"><span data-stu-id="0765a-282">(25)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-283">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="0765a-283">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0765a-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="0765a-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0765a-285">(26)</span><span class="sxs-lookup"><span data-stu-id="0765a-285">(26)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-286">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="0765a-286">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="0765a-287"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="0765a-287"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="0765a-288">(27)</span><span class="sxs-lookup"><span data-stu-id="0765a-288">(27)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-289">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="0765a-289">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="0765a-290"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="0765a-290"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="0765a-291">(28)</span><span class="sxs-lookup"><span data-stu-id="0765a-291">(28)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-292">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="0765a-292">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="0765a-293"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="0765a-293"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="0765a-294">(29)</span><span class="sxs-lookup"><span data-stu-id="0765a-294">(29)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-295">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="0765a-295">Device is disabled.</span></span> <span data-ttu-id="0765a-296">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="0765a-296">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="0765a-297"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="0765a-297"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="0765a-298">(30)</span><span class="sxs-lookup"><span data-stu-id="0765a-298">(30)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-299">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="0765a-299">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0765a-300"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="0765a-300"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="0765a-301"> (31) </span><span class="sxs-lookup"><span data-stu-id="0765a-301">(31)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-302">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="0765a-302">Device is not working properly.</span></span> <span data-ttu-id="0765a-303">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="0765a-303">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0765a-304">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="0765a-304">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-305">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0765a-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-306">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0765a-307">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="0765a-307">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0765a-308">若 **為 True**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="0765a-308">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="0765a-309">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0765a-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0765a-310">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0765a-310">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-311">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0765a-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-312">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0765a-313">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0765a-313">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0765a-314">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="0765a-314">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="0765a-315">搭配類別的其他索引鍵屬性使用時，屬性可讓這個類別的所有實例和其子類別都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="0765a-315">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="0765a-316">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0765a-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0765a-317">**說明**</span><span class="sxs-lookup"><span data-stu-id="0765a-317">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-318">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0765a-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-319">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0765a-320">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="0765a-320">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0765a-321">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="0765a-321">Description of the object.</span></span>

<span data-ttu-id="0765a-322">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0765a-322">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0765a-323">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0765a-323">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-324">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0765a-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-325">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0765a-326">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "DeviceId" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="0765a-326">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="0765a-327">系統上其他裝置之邏輯磁片的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="0765a-327">Unique identifier of the logical disk from other devices on the system.</span></span>

<span data-ttu-id="0765a-328">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0765a-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="0765a-329">如需抓取此屬性的程式碼範例，請參閱下方的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="0765a-329">For a code example that retrieves this property, see the Remarks section, below.</span></span>

</dd> <dt>

<span data-ttu-id="0765a-330">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="0765a-330">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-331">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0765a-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-332">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0765a-333">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| FileFunctions \| GetDriveType" ) </span><span class="sxs-lookup"><span data-stu-id="0765a-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|FileFunctions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="0765a-334">對應到此邏輯磁片所代表之磁片磁碟機類型的數值。</span><span class="sxs-lookup"><span data-stu-id="0765a-334">Numeric value that corresponds to the type of disk drive this logical disk represents.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0765a-335">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="0765a-335">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Root_Directory"></span><span id="no_root_directory"></span><span id="NO_ROOT_DIRECTORY"></span>

<span data-ttu-id="0765a-336">**沒有根目錄** (1) </span><span class="sxs-lookup"><span data-stu-id="0765a-336">**No Root Directory** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Disk"></span><span id="removable_disk"></span><span id="REMOVABLE_DISK"></span>

<span data-ttu-id="0765a-337">**抽取式磁碟** (2) </span><span class="sxs-lookup"><span data-stu-id="0765a-337">**Removable Disk** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Local_Disk"></span><span id="local_disk"></span><span id="LOCAL_DISK"></span>

<span data-ttu-id="0765a-338">**本機磁片** (3) </span><span class="sxs-lookup"><span data-stu-id="0765a-338">**Local Disk** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Network_Drive"></span><span id="network_drive"></span><span id="NETWORK_DRIVE"></span>

<span data-ttu-id="0765a-339">**網路磁碟機** 機 (4) </span><span class="sxs-lookup"><span data-stu-id="0765a-339">**Network Drive** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Compact_Disc"></span><span id="compact_disc"></span><span id="COMPACT_DISC"></span>

<span data-ttu-id="0765a-340">**光碟 (5**) </span><span class="sxs-lookup"><span data-stu-id="0765a-340">**Compact Disc** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM_Disk"></span><span id="ram_disk"></span><span id="RAM_DISK"></span>

<span data-ttu-id="0765a-341">**RAM 磁碟** (6) </span><span class="sxs-lookup"><span data-stu-id="0765a-341">**RAM Disk** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0765a-342">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="0765a-342">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-343">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0765a-343">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-344">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0765a-345">若 **為 True**，則表示 **LastErrorCode** 中回報的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="0765a-345">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="0765a-346">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0765a-346">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0765a-347">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0765a-347">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-348">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0765a-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-349">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0765a-350">有關 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0765a-350">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="0765a-351">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0765a-351">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0765a-352">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="0765a-352">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-353">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0765a-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-354">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0765a-355">此儲存範圍所支援的錯誤偵測類型和修正。</span><span class="sxs-lookup"><span data-stu-id="0765a-355">Type of error detection and correction supported by this storage extent.</span></span>

<span data-ttu-id="0765a-356">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="0765a-356">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="0765a-357">**檔**</span><span class="sxs-lookup"><span data-stu-id="0765a-357">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-358">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0765a-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-359">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0765a-360">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 檔案系統函數 [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)) </span><span class="sxs-lookup"><span data-stu-id="0765a-360">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="0765a-361">邏輯磁片上的檔案系統。</span><span class="sxs-lookup"><span data-stu-id="0765a-361">File system on the logical disk.</span></span>

<span data-ttu-id="0765a-362">範例： "NTFS"</span><span class="sxs-lookup"><span data-stu-id="0765a-362">Example: "NTFS"</span></span>

</dd> <dt>

<span data-ttu-id="0765a-363">**FreeSpace**</span><span class="sxs-lookup"><span data-stu-id="0765a-363">**FreeSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-364">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="0765a-364">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-365">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0765a-366">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="0765a-366">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0765a-367">邏輯磁片上可用的空間（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="0765a-367">Space, in bytes, available on the logical disk.</span></span>

<span data-ttu-id="0765a-368">這個屬性繼承自 [**CIM \_ LogicalDisk**](cim-logicaldisk.md)。</span><span class="sxs-lookup"><span data-stu-id="0765a-368">This property is inherited from [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span>

<span data-ttu-id="0765a-369">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="0765a-369">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0765a-370">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0765a-370">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-371">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="0765a-371">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-372">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0765a-373">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="0765a-373">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0765a-374">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="0765a-374">Date and time the object was installed.</span></span> <span data-ttu-id="0765a-375">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="0765a-375">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="0765a-376">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0765a-376">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0765a-377">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0765a-377">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-378">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0765a-378">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-379">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0765a-380">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0765a-380">Last error code reported by the logical device.</span></span>

<span data-ttu-id="0765a-381">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0765a-381">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0765a-382">**MaximumComponentLength**</span><span class="sxs-lookup"><span data-stu-id="0765a-382">**MaximumComponentLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-383">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0765a-383">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-384">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-384">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0765a-385">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 檔案系統函數 [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)) </span><span class="sxs-lookup"><span data-stu-id="0765a-385">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="0765a-386">Windows 磁片磁碟機所支援之檔案名元件的最大長度。</span><span class="sxs-lookup"><span data-stu-id="0765a-386">Maximum length of a filename component supported by the Windows drive.</span></span> <span data-ttu-id="0765a-387">Filename 元件是在反斜線之間的檔案名部分。</span><span class="sxs-lookup"><span data-stu-id="0765a-387">A filename component is that portion of a filename between backslashes.</span></span> <span data-ttu-id="0765a-388">此值可用來指出指定的檔案系統所支援的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="0765a-388">The value can be used to indicate that long names are supported by the specified file system.</span></span> <span data-ttu-id="0765a-389">例如，對於支援長名稱的 FAT 檔案系統，此函式會儲存值255，而不是先前的8.3 指標。</span><span class="sxs-lookup"><span data-stu-id="0765a-389">For example, for a FAT file system supporting long names, the function stores the value 255, rather than the previous 8.3 indicator.</span></span> <span data-ttu-id="0765a-390">使用 NTFS 檔案系統的系統也可以支援完整名稱。</span><span class="sxs-lookup"><span data-stu-id="0765a-390">Long names can also be supported on systems that use the NTFS file system.</span></span>

<span data-ttu-id="0765a-391">範例：255</span><span class="sxs-lookup"><span data-stu-id="0765a-391">Example: 255</span></span>

</dd> <dt>

<span data-ttu-id="0765a-392">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="0765a-392">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-393">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0765a-393">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-394">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0765a-395">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Device Input and Output 函數 \| DeviceIoControl" ) </span><span class="sxs-lookup"><span data-stu-id="0765a-395">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="0765a-396">目前存在於邏輯磁碟機中的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="0765a-396">Type of media currently present in the logical drive.</span></span> <span data-ttu-id="0765a-397">這個值會是 Winioctl 中所定義之媒體類型列舉的其中一個值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0765a-397">This value will be one of the values of the MEDIA\_TYPE enumeration defined in Winioctl.h.</span></span> <span data-ttu-id="0765a-398">如果磁片磁碟機中目前沒有媒體，則此值可能不會完全適用于抽取式磁碟機。</span><span class="sxs-lookup"><span data-stu-id="0765a-398">The value may not be exact for removable drives if currently there is no media in the drive.</span></span>

<dt>

<span id="Format_is_unknown"></span><span id="format_is_unknown"></span><span id="FORMAT_IS_UNKNOWN"></span>

<span data-ttu-id="0765a-399"><span id="Format_is_unknown"></span><span id="format_is_unknown"></span><span id="FORMAT_IS_UNKNOWN"></span>**格式不明** (0) </span><span class="sxs-lookup"><span data-stu-id="0765a-399"><span id="Format_is_unknown"></span><span id="format_is_unknown"></span><span id="FORMAT_IS_UNKNOWN"></span>**Format is unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="0765a-400"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 英寸磁片** 磁碟機 (1) </span><span class="sxs-lookup"><span data-stu-id="0765a-400"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-401">5 1/4 英寸的磁片磁碟機-1.2 MB-512 位元組/磁區</span><span class="sxs-lookup"><span data-stu-id="0765a-401">5 1/4-Inch Floppy Disk - 1.2 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="0765a-402"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 寸磁片** 磁碟機 (2) </span><span class="sxs-lookup"><span data-stu-id="0765a-402"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-403">3 1/2 英寸的磁片磁碟機-1.44 MB-512 個位元組/磁區</span><span class="sxs-lookup"><span data-stu-id="0765a-403">3 1/2-Inch Floppy Disk - 1.44 MB -512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="0765a-404"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 寸磁片** 磁碟機 (3) </span><span class="sxs-lookup"><span data-stu-id="0765a-404"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-405">3 1/2 英寸的磁片磁碟機-2.88 MB-512 個位元組/磁區</span><span class="sxs-lookup"><span data-stu-id="0765a-405">3 1/2-Inch Floppy Disk - 2.88 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="0765a-406"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 寸磁片磁碟機** (4) </span><span class="sxs-lookup"><span data-stu-id="0765a-406"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-407">3 1/2 英寸的磁片磁碟機-20.8 MB-512 個位元組/磁區</span><span class="sxs-lookup"><span data-stu-id="0765a-407">3 1/2-Inch Floppy Disk - 20.8 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="0765a-408"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 寸磁片** 磁碟機 (5) </span><span class="sxs-lookup"><span data-stu-id="0765a-408"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-409">3 1/2 英寸的磁片磁碟機-720 KB-512 位元組/磁區</span><span class="sxs-lookup"><span data-stu-id="0765a-409">3 1/2-Inch Floppy Disk - 720 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="0765a-410"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 英寸磁片** 磁碟機 (6) </span><span class="sxs-lookup"><span data-stu-id="0765a-410"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-411">5 1/4 英寸磁片磁碟機-360 KB-512 位元組/磁區</span><span class="sxs-lookup"><span data-stu-id="0765a-411">5 1/4-Inch Floppy Disk - 360 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="0765a-412"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 英寸磁片磁碟機** (7) </span><span class="sxs-lookup"><span data-stu-id="0765a-412"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-413">5 1/4 英寸磁片磁碟機-320 KB-512 位元組/磁區</span><span class="sxs-lookup"><span data-stu-id="0765a-413">5 1/4-Inch Floppy Disk - 320 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="0765a-414"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 寸磁片** 磁碟機 (8) </span><span class="sxs-lookup"><span data-stu-id="0765a-414"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (8)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-415">5 1/4 英寸磁片磁碟機-320 KB-1024 位元組/磁區</span><span class="sxs-lookup"><span data-stu-id="0765a-415">5 1/4-Inch Floppy Disk - 320 KB - 1024 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="0765a-416"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 英寸磁片磁碟機** (9) </span><span class="sxs-lookup"><span data-stu-id="0765a-416"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (9)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-417">5 1/4 英寸磁片磁碟機-180 KB-512 位元組/磁區</span><span class="sxs-lookup"><span data-stu-id="0765a-417">5 1/4-Inch Floppy Disk - 180 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="0765a-418"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 寸磁片磁碟機** (10) </span><span class="sxs-lookup"><span data-stu-id="0765a-418"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (10)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-419">5 1/4 英寸磁片磁碟機-160 KB-512 位元組/磁區</span><span class="sxs-lookup"><span data-stu-id="0765a-419">5 1/4-Inch Floppy Disk - 160 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="Removable_media_other_than_floppy"></span><span id="removable_media_other_than_floppy"></span><span id="REMOVABLE_MEDIA_OTHER_THAN_FLOPPY"></span>

<span data-ttu-id="0765a-420"><span id="Removable_media_other_than_floppy"></span><span id="removable_media_other_than_floppy"></span><span id="REMOVABLE_MEDIA_OTHER_THAN_FLOPPY"></span>非軟盤機 (11) 的卸載式 **媒體**</span><span class="sxs-lookup"><span data-stu-id="0765a-420"><span id="Removable_media_other_than_floppy"></span><span id="removable_media_other_than_floppy"></span><span id="REMOVABLE_MEDIA_OTHER_THAN_FLOPPY"></span>**Removable media other than floppy** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_hard_disk_media"></span><span id="fixed_hard_disk_media"></span><span id="FIXED_HARD_DISK_MEDIA"></span>

<span data-ttu-id="0765a-421"><span id="Fixed_hard_disk_media"></span><span id="fixed_hard_disk_media"></span><span id="FIXED_HARD_DISK_MEDIA"></span>**固定硬碟媒體** (12) </span><span class="sxs-lookup"><span data-stu-id="0765a-421"><span id="Fixed_hard_disk_media"></span><span id="fixed_hard_disk_media"></span><span id="FIXED_HARD_DISK_MEDIA"></span>**Fixed hard disk media** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="0765a-422"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 寸磁片磁碟機** (13) </span><span class="sxs-lookup"><span data-stu-id="0765a-422"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (13)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-423">3 1/2 英寸的磁片磁碟機-120 MB-512 個位元組/磁區</span><span class="sxs-lookup"><span data-stu-id="0765a-423">3 1/2-Inch Floppy Disk - 120 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="0765a-424"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 寸磁片** 磁碟機 (14) </span><span class="sxs-lookup"><span data-stu-id="0765a-424"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (14)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-425">3 1/2 英寸的磁片磁碟機-640 KB-512 位元組/磁區</span><span class="sxs-lookup"><span data-stu-id="0765a-425">3 1/2-Inch Floppy Disk - 640 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="0765a-426"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 寸磁片** 磁碟機 (15) </span><span class="sxs-lookup"><span data-stu-id="0765a-426"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (15)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-427">5 1/4 英寸磁片磁碟機-640 KB-512 位元組/磁區</span><span class="sxs-lookup"><span data-stu-id="0765a-427">5 1/4-Inch Floppy Disk - 640 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="0765a-428"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 寸磁片磁碟機** (16) </span><span class="sxs-lookup"><span data-stu-id="0765a-428"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (16)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-429">5 1/4 英寸磁片磁碟機-720 KB-512 位元組/磁區</span><span class="sxs-lookup"><span data-stu-id="0765a-429">5 1/4-Inch Floppy Disk - 720 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="0765a-430"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 寸磁片磁碟機** (17) </span><span class="sxs-lookup"><span data-stu-id="0765a-430"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (17)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-431">3 1/2 英寸的磁片磁碟機-1.2 MB-512 個位元組/磁區</span><span class="sxs-lookup"><span data-stu-id="0765a-431">3 1/2-Inch Floppy Disk - 1.2 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="0765a-432"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 寸磁片磁碟機** (18) </span><span class="sxs-lookup"><span data-stu-id="0765a-432"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (18)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-433">3 1/2 英寸的磁片磁碟機-1.23 MB-1024 個位元組/磁區</span><span class="sxs-lookup"><span data-stu-id="0765a-433">3 1/2-Inch Floppy Disk - 1.23 MB - 1024 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="0765a-434"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 寸磁片磁碟機** (19) </span><span class="sxs-lookup"><span data-stu-id="0765a-434"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (19)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-435">5 1/4 英寸的磁片磁碟機-1.23 MB-1024 位元組/磁區</span><span class="sxs-lookup"><span data-stu-id="0765a-435">5 1/4-Inch Floppy Disk - 1.23 MB - 1024 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="0765a-436"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 寸磁片** (20) </span><span class="sxs-lookup"><span data-stu-id="0765a-436"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (20)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-437">3 1/2 英寸的磁片磁碟機-128 MB-512 個位元組/磁區</span><span class="sxs-lookup"><span data-stu-id="0765a-437">3 1/2-Inch Floppy Disk - 128 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="0765a-438"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 寸磁片磁碟機** (21) </span><span class="sxs-lookup"><span data-stu-id="0765a-438"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (21)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-439">3 1/2 英寸的磁片磁碟機-230 MB-512 個位元組/磁區</span><span class="sxs-lookup"><span data-stu-id="0765a-439">3 1/2-Inch Floppy Disk - 230 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="8-Inch_Floppy_Disk"></span><span id="8-inch_floppy_disk"></span><span id="8-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="0765a-440"><span id="8-Inch_Floppy_Disk"></span><span id="8-inch_floppy_disk"></span><span id="8-INCH_FLOPPY_DISK"></span>**8 英寸的磁片磁碟機** (22) </span><span class="sxs-lookup"><span data-stu-id="0765a-440"><span id="8-Inch_Floppy_Disk"></span><span id="8-inch_floppy_disk"></span><span id="8-INCH_FLOPPY_DISK"></span>**8-Inch Floppy Disk** (22)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-441">8寸磁片-256 KB-128 位元組/磁區</span><span class="sxs-lookup"><span data-stu-id="0765a-441">8-Inch Floppy Disk - 256 KB - 128 bytes/sector</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0765a-442">**名稱**</span><span class="sxs-lookup"><span data-stu-id="0765a-442">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-443">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0765a-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-444">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0765a-445">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="0765a-445">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0765a-446">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="0765a-446">Label by which the object is known.</span></span> <span data-ttu-id="0765a-447">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="0765a-447">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="0765a-448">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0765a-448">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0765a-449">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="0765a-449">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-450">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="0765a-450">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-451">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0765a-452">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrStorageSize ") </span><span class="sxs-lookup"><span data-stu-id="0765a-452">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="0765a-453">連續區塊總數，每個區塊會封鎖 **區塊** 屬性中包含的值大小，這會形成此儲存範圍。</span><span class="sxs-lookup"><span data-stu-id="0765a-453">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="0765a-454">您可以將 [ **區塊** ] 屬性的值乘以這個屬性的值，以計算儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="0765a-454">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="0765a-455">如果 **區塊** 的值是1，則這個屬性是儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="0765a-455">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="0765a-456">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="0765a-456">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="0765a-457">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="0765a-457">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0765a-458">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="0765a-458">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-459">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0765a-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-460">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0765a-461">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="0765a-461">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0765a-462">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="0765a-462">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="0765a-463">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0765a-463">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="0765a-464">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="0765a-464">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="0765a-465">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0765a-465">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-466">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="0765a-466">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0765a-467">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0765a-468">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="0765a-468">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="0765a-469">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="0765a-469">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0765a-470"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="0765a-470"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="0765a-471"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="0765a-471"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0765a-472"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="0765a-472"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0765a-473"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="0765a-473"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-474">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="0765a-474">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="0765a-475"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="0765a-475"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-476">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="0765a-476">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="0765a-477"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="0765a-477"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-478">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="0765a-478">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="0765a-479">這個方法可在父 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="0765a-479">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="0765a-480">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="0765a-480">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="0765a-481"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="0765a-481"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-482">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="0765a-482">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="0765a-483"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="0765a-483"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0765a-484">支援計時 Power-On</span><span class="sxs-lookup"><span data-stu-id="0765a-484">Timed Power-On Supported</span></span>

<span data-ttu-id="0765a-485">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="0765a-485">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0765a-486">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="0765a-486">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-487">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0765a-487">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-488">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-488">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0765a-489">若 **為 True**，則裝置可以是電源管理 (可進入暫停模式，依此類推) 。</span><span class="sxs-lookup"><span data-stu-id="0765a-489">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="0765a-490">這個屬性不表示電源管理功能目前已啟用，只有邏輯裝置能夠進行電源管理。</span><span class="sxs-lookup"><span data-stu-id="0765a-490">This property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="0765a-491">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0765a-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0765a-492">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="0765a-492">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-493">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0765a-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-494">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0765a-495">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Windows 網路功能 \| WNetGetConnection" ) </span><span class="sxs-lookup"><span data-stu-id="0765a-495">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Windows Networking Functions\|WNetGetConnection")</span></span>
</dt> </dl>

<span data-ttu-id="0765a-496">邏輯裝置的網路路徑。</span><span class="sxs-lookup"><span data-stu-id="0765a-496">Network path to the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="0765a-497">**目的**</span><span class="sxs-lookup"><span data-stu-id="0765a-497">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-498">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0765a-498">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-499">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0765a-500">描述媒體及其用途的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="0765a-500">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="0765a-501">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="0765a-501">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="0765a-502">**QuotasDisabled**</span><span class="sxs-lookup"><span data-stu-id="0765a-502">**QuotasDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-503">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0765a-503">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-504">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0765a-505">指出未在此系統上啟用配額管理 (TRUE) 。</span><span class="sxs-lookup"><span data-stu-id="0765a-505">Indicates that quota management is not enabled (TRUE) on this system.</span></span>

</dd> <dt>

<span data-ttu-id="0765a-506">**QuotasIncomplete**</span><span class="sxs-lookup"><span data-stu-id="0765a-506">**QuotasIncomplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-507">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0765a-507">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-508">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0765a-509">表示已使用配額管理，但已停用 (**True**) 。</span><span class="sxs-lookup"><span data-stu-id="0765a-509">Indicates that the quota management was used but has been disabled (**True**).</span></span> <span data-ttu-id="0765a-510">[不完整] 指的是停用配額管理之後，檔案系統中剩餘的資訊。</span><span class="sxs-lookup"><span data-stu-id="0765a-510">Incomplete refers to the information left in the file system after quota management was disabled.</span></span>

</dd> <dt>

<span data-ttu-id="0765a-511">**QuotasRebuilding**</span><span class="sxs-lookup"><span data-stu-id="0765a-511">**QuotasRebuilding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-512">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0765a-512">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-513">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-513">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0765a-514">若 **為 True**，表示檔案系統正在編譯資訊的使用中進程，以及設定磁片以進行配額管理。</span><span class="sxs-lookup"><span data-stu-id="0765a-514">If **True**, indicates that the file system is in the active process of compiling information and setting the disk up for quota management.</span></span>

</dd> <dt>

<span data-ttu-id="0765a-515">**大小**</span><span class="sxs-lookup"><span data-stu-id="0765a-515">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-516">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0765a-516">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-517">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-517">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0765a-518">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="0765a-518">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0765a-519">磁片磁碟機的大小。</span><span class="sxs-lookup"><span data-stu-id="0765a-519">Size of the disk drive.</span></span>

<span data-ttu-id="0765a-520">這個屬性繼承自 [**CIM \_ LogicalDisk**](cim-logicaldisk.md)。</span><span class="sxs-lookup"><span data-stu-id="0765a-520">This property is inherited from [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span>

<span data-ttu-id="0765a-521">如需抓取此屬性的程式碼範例，請參閱下方的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="0765a-521">For a code example that retrieves this property, see the Remarks section, below.</span></span>

</dd> <dt>

<span data-ttu-id="0765a-522">**狀態**</span><span class="sxs-lookup"><span data-stu-id="0765a-522">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-523">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0765a-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-524">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0765a-525">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="0765a-525">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0765a-526">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="0765a-526">Current status of the object.</span></span> <span data-ttu-id="0765a-527">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="0765a-527">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0765a-528">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="0765a-528">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0765a-529">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="0765a-529">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0765a-530">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="0765a-530">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0765a-531">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="0765a-531">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0765a-532">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0765a-532">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0765a-533">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="0765a-533">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0765a-534">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="0765a-534">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0765a-535">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="0765a-535">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0765a-536">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="0765a-536">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0765a-537">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="0765a-537">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0765a-538">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="0765a-538">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0765a-539">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="0765a-539">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0765a-540">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="0765a-540">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0765a-541">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="0765a-541">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0765a-542">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="0765a-542">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0765a-543">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="0765a-543">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0765a-544">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="0765a-544">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0765a-545">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="0765a-545">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0765a-546">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="0765a-546">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-547">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0765a-547">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-548">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0765a-549">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="0765a-549">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="0765a-550">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="0765a-550">State of the logical device.</span></span> <span data-ttu-id="0765a-551">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="0765a-551">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="0765a-552">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0765a-552">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0765a-553">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="0765a-553">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0765a-554">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="0765a-554">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0765a-555">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="0765a-555">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0765a-556">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="0765a-556">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0765a-557">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="0765a-557">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0765a-558">**SupportsDiskQuotas**</span><span class="sxs-lookup"><span data-stu-id="0765a-558">**SupportsDiskQuotas**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-559">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0765a-559">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-560">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-560">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0765a-561">若 **為 True**，則此磁片區支援磁片配額。</span><span class="sxs-lookup"><span data-stu-id="0765a-561">If **True**, this volume supports disk quotas.</span></span>

</dd> <dt>

<span data-ttu-id="0765a-562">**SupportsFileBasedCompression**</span><span class="sxs-lookup"><span data-stu-id="0765a-562">**SupportsFileBasedCompression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-563">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0765a-563">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-564">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-564">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0765a-565">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 檔案系統函數 \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| FS \_ 檔 \_ 壓縮」 ) </span><span class="sxs-lookup"><span data-stu-id="0765a-565">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)\|FS\_FILE\_COMPRESSION")</span></span>
</dt> </dl>

<span data-ttu-id="0765a-566">若 **為 True**，則邏輯磁碟分割支援以檔案為基礎的壓縮，例如 NTFS 檔案系統的情況。</span><span class="sxs-lookup"><span data-stu-id="0765a-566">If **True**, the logical disk partition supports file-based compression, such as is the case with the NTFS file system.</span></span> <span data-ttu-id="0765a-567">當 **壓縮** 的屬性為 **True** 時，這個屬性為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="0765a-567">This property is **False** when the **Compressed** property is **True**.</span></span>

</dd> <dt>

<span data-ttu-id="0765a-568">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0765a-568">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-569">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0765a-569">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-570">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-570">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0765a-571">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0765a-571">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0765a-572">設定電腦 **CreationClassName** 的範圍值屬性值。</span><span class="sxs-lookup"><span data-stu-id="0765a-572">Value of the scoping computer **CreationClassName** property.</span></span>

<span data-ttu-id="0765a-573">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0765a-573">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0765a-574">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0765a-574">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-575">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0765a-575">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-576">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-576">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0765a-577">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0765a-577">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0765a-578">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="0765a-578">Name of the scoping system.</span></span>

<span data-ttu-id="0765a-579">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0765a-579">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0765a-580">**VolumeDirty**</span><span class="sxs-lookup"><span data-stu-id="0765a-580">**VolumeDirty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-581">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0765a-581">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-582">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-582">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0765a-583">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「FSCTL \_ 是磁片區中途」 \_ \_ ) </span><span class="sxs-lookup"><span data-stu-id="0765a-583">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FSCTL\_IS\_VOLUME\_DIRTY")</span></span>
</dt> </dl>

<span data-ttu-id="0765a-584">若 **為 True**，則磁片需要在下次重新開機時執行 [**ChkDsk**](chkdsk-method-in-class-win32-logicaldisk.md) 。</span><span class="sxs-lookup"><span data-stu-id="0765a-584">If **True**, the disk requires [**ChkDsk**](chkdsk-method-in-class-win32-logicaldisk.md) to be run at the next restart.</span></span> <span data-ttu-id="0765a-585">這個屬性只適用于代表電腦上實體磁片的邏輯磁片實例。</span><span class="sxs-lookup"><span data-stu-id="0765a-585">This property is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="0765a-586">它不適用於對應的邏輯磁碟機。</span><span class="sxs-lookup"><span data-stu-id="0765a-586">It is not applicable to mapped logical drives.</span></span>

</dd> <dt>

<span data-ttu-id="0765a-587">**VolumeName**</span><span class="sxs-lookup"><span data-stu-id="0765a-587">**VolumeName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-588">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0765a-588">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-589">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0765a-589">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0765a-590">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 檔案系統函數 [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)) </span><span class="sxs-lookup"><span data-stu-id="0765a-590">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="0765a-591">邏輯磁片的磁片區名稱。</span><span class="sxs-lookup"><span data-stu-id="0765a-591">Volume name of the logical disk.</span></span>

<span data-ttu-id="0765a-592">條件約束：最多32個字元。</span><span class="sxs-lookup"><span data-stu-id="0765a-592">Constraints: Maximum 32 characters.</span></span>

<span data-ttu-id="0765a-593">如需抓取此屬性的程式碼範例，請參閱下方的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="0765a-593">For a code example that retrieves this property, see the Remarks section, below.</span></span>

</dd> <dt>

<span data-ttu-id="0765a-594">**VolumeSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="0765a-594">**VolumeSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0765a-595">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0765a-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0765a-596">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0765a-596">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0765a-597">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 檔案系統函數 [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)) </span><span class="sxs-lookup"><span data-stu-id="0765a-597">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="0765a-598">邏輯磁片的音量序號。</span><span class="sxs-lookup"><span data-stu-id="0765a-598">Volume serial number of the logical disk.</span></span>

<span data-ttu-id="0765a-599">條件約束：最多11個字元。</span><span class="sxs-lookup"><span data-stu-id="0765a-599">Constraints: Maximum 11 characters.</span></span>

<span data-ttu-id="0765a-600">範例： "A8C3-D032"</span><span class="sxs-lookup"><span data-stu-id="0765a-600">Example: "A8C3-D032"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0765a-601">備註</span><span class="sxs-lookup"><span data-stu-id="0765a-601">Remarks</span></span>

<span data-ttu-id="0765a-602">**Win32 \_ LogicalDisk** 類別衍生自 cim [**\_ LogicalDisk**](cim-logicaldisk.md) ，它衍生自 [**cim \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="0765a-602">The **Win32\_LogicalDisk** class is derived from [**CIM\_LogicalDisk**](cim-logicaldisk.md) which derives from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span> <span data-ttu-id="0765a-603">**Cim \_ StorageExtent** 類別衍生自 [**cim \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0765a-603">The **CIM\_StorageExtent** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="0765a-604">實體磁片磁碟機是任何存放裝置管理系統的基石。</span><span class="sxs-lookup"><span data-stu-id="0765a-604">A physical disk drive is the cornerstone of any storage management system.</span></span> <span data-ttu-id="0765a-605">不過，在安裝實體磁片磁碟機之後，使用者和系統管理員通常都不會直接處理硬體。</span><span class="sxs-lookup"><span data-stu-id="0765a-605">However, after a physical disk drive has been installed, neither users nor system administrators typically deal with the hardware directly.</span></span> <span data-ttu-id="0765a-606">相反地，使用者和系統管理員會與已在磁片上建立的邏輯磁碟機互動。</span><span class="sxs-lookup"><span data-stu-id="0765a-606">Instead, both users and system administrators interact with the logical drives that have been created on the disk.</span></span>

<span data-ttu-id="0765a-607">邏輯磁碟機是磁碟分割的細分，已被指派自己的磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="0765a-607">A logical drive is a subdivision of a partition that has been assigned its own drive letter.</span></span> <span data-ttu-id="0765a-608"> (可以有尚未指派磁碟機號的磁碟分割。 ) 當您討論磁片磁碟機 C 或磁片磁碟機 D 時，您指的是邏輯磁片磁碟機，而不是實體磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="0765a-608">(It is possible to have a partition that has not been assigned a drive letter.) When you talk about drive C or drive D, you are referring to a logical drive rather than to a physical disk drive.</span></span> <span data-ttu-id="0765a-609">同樣地，當您將檔儲存至 E 磁片磁碟機時，您會將它儲存到邏輯磁碟機。</span><span class="sxs-lookup"><span data-stu-id="0765a-609">Likewise, when you save a document to drive E, you are saving it to the logical drive.</span></span> <span data-ttu-id="0765a-610">實體磁片構成組成磁片磁碟機的硬體，包括標頭、磁區和圓柱等元件。</span><span class="sxs-lookup"><span data-stu-id="0765a-610">Physical disks compose the hardware that makes up a drive, including such components as heads, sectors, and cylinders.</span></span> <span data-ttu-id="0765a-611">相反地，邏輯磁片磁碟機有像是磁碟空間、可用磁碟空間和磁碟機號等的屬性。</span><span class="sxs-lookup"><span data-stu-id="0765a-611">Logical drives, by contrast, have properties such as disk space, available disk space, and drive letters.</span></span>

> [!Note]  
> <span data-ttu-id="0765a-612">**Win32 \_ LogicalDisk** 類別只能用來列舉本機磁片磁碟機的屬性。</span><span class="sxs-lookup"><span data-stu-id="0765a-612">The **Win32\_LogicalDisk** class can be used only to enumerate the properties of local disk drives.</span></span> <span data-ttu-id="0765a-613">不過，您可以使用 [**Win32 \_ MappedLogicalDisk**](win32-mappedlogicaldisk.md) 類別來列舉已對應網路磁碟機機的屬性。</span><span class="sxs-lookup"><span data-stu-id="0765a-613">However, you can use the [**Win32\_MappedLogicalDisk**](win32-mappedlogicaldisk.md) class to enumerate the properties of mapped network drives.</span></span>

 

## <a name="examples"></a><span data-ttu-id="0765a-614">範例</span><span class="sxs-lookup"><span data-stu-id="0765a-614">Examples</span></span>

<span data-ttu-id="0765a-615">您可以使用 **Win32 \_ LogicalDisk** 尋找其他範例，以取得 [WMI 工作：磁片和檔案系統](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems) 主題中的磁片或磁片區資料。</span><span class="sxs-lookup"><span data-stu-id="0765a-615">You can find other examples using **Win32\_LogicalDisk** to obtain disk or volume data in the [WMI Tasks: Disks and File Systems](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems) topic.</span></span>

<span data-ttu-id="0765a-616">TechNet 資源庫上的 [WMI 資訊](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) 取回程序 VBScript 程式碼範例會使用 **Win32 \_ LogicalDisk** 類別，從多部遠端電腦抓取硬體資訊。</span><span class="sxs-lookup"><span data-stu-id="0765a-616">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_LogicalDisk** class to retrieve hardware information from a number of remote computers.</span></span>

<span data-ttu-id="0765a-617">[使用 wmi/Cim 取得磁片資訊 ...](https://Gallery.TechNet.Microsoft.Com/Get-Disk-info-using-wmicim-ff0bd352)TechNet 元件庫上的 PowerShell 程式碼範例會使用 **Win32 \_ LogicalDisk** ，從目標裝置取出 **DeviceID**、 **VolumeName** 和 **大小**。</span><span class="sxs-lookup"><span data-stu-id="0765a-617">The [Get Disk info using wmi/cim...](https://Gallery.TechNet.Microsoft.Com/Get-Disk-info-using-wmicim-ff0bd352) PowerShell code example on the TechNet Gallery uses **Win32\_LogicalDisk** to retrieve **DeviceID**, **VolumeName**, and **Size** from a target device.</span></span> <span data-ttu-id="0765a-618">尤其是，此範例包含嚴格的例外狀況處理，並會針對每部電腦（而不是每個磁片）傳回單一物件。</span><span class="sxs-lookup"><span data-stu-id="0765a-618">In particular, this sample includes rigorous exception handling, and returns a single object per computer, rather than per disk.</span></span>

<span data-ttu-id="0765a-619">企業腳本處理通常需要在遠端電腦上設定硬體和軟體;接著，這需要您事先知道安裝在電腦上的磁片磁碟機類型。</span><span class="sxs-lookup"><span data-stu-id="0765a-619">Enterprise scripting often involves configuring hardware and software on remote computers; in turn, this requires you to know, in advance, the type of disk drives installed on a computer.</span></span> <span data-ttu-id="0765a-620">例如，將應用程式安裝在 E 磁片磁碟機上的腳本，只有在磁片磁碟機 E 是硬碟時才能運作。</span><span class="sxs-lookup"><span data-stu-id="0765a-620">For example, a script that installs an application on drive E works only if drive E is a hard disk.</span></span> <span data-ttu-id="0765a-621">如果磁片磁碟機 E 代表磁片或 CD-ROM 光碟機，腳本會失敗。</span><span class="sxs-lookup"><span data-stu-id="0765a-621">If drive E happens to represent a floppy disk or a CD-ROM drive, the script fails.</span></span> <span data-ttu-id="0765a-622">下列程式碼會識別電腦上所安裝的磁片磁碟機和磁片磁碟機類型。</span><span class="sxs-lookup"><span data-stu-id="0765a-622">The following code identifies the drives and drive types installed on a computer</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("SELECT * FROM Win32_LogicalDisk")
For Each objDisk in colDisks
 Wscript.Echo "DeviceID: "& objDisk.DeviceID 
 Select Case objDisk.DriveType
 Case 1
 Wscript.Echo "No root directory."
 Case 2
 Wscript.Echo "DriveType: Removable drive."
 Case 3
 Wscript.Echo "DriveType: Local hard disk."
 Case 4
 Wscript.Echo "DriveType: Network disk." 
 Case 5
 Wscript.Echo "DriveType: Compact disk." 
 Case 6
 Wscript.Echo "DriveType: RAM disk." 
 Case Else
 Wscript.Echo "Drive type could not be determined."
 End Select
Next
```


```CSharp

//be sure to References->Add->System.Management to your project
using System.Management;
...
{
   string strComputer = &quot;.&quot;;
            
   ManagementScope namespaceScope = new ManagementScope(&quot;\\\\&quot; + strComputer + &quot;\\ROOT\\CIMV2&quot;);
   ObjectQuery diskQuery = new ObjectQuery(&quot;SELECT * FROM Win32_LogicalDisk&quot;);
   ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher(namespaceScope, diskQuery);
   ManagementObjectCollection colDisks = mgmtObjSearcher.Get();

   foreach (ManagementObject objDisk in colDisks)
   {
      Console.WriteLine(&quot;Device ID : {0}&quot;, objDisk[&quot;DeviceID&quot;]);
                
      switch ((uint)(objDisk[&quot;DriveType&quot;]))
      {
         case 1: {   Console.WriteLine(&quot;No root directory.&quot;);
                     break;}
         case 2: {   Console.WriteLine(&quot;DriveType: Removable drive.&quot;); 
                     break;}
         case 3: {   Console.WriteLine(&quot;DriveType: Local hard disk.&quot;);
                     break;}
         case 4: {   Console.WriteLine(&quot;DriveType: Network disk.&quot;);
                     break;}
         case 5: {   Console.WriteLine(&quot;DriveType: Compact disk.&quot;);
                     break;}
         case 6: {   Console.WriteLine(&quot;DriveType: RAM disk.&quot;);
                     break;}
         default: {  Console.WriteLine(&quot;Drive type could not be determined.&quot;);
                     break;}
      }
      //Readline is in here so the user can see the result before the code exists
      Console.ReadLine();
   }
}
```





<span data-ttu-id="0765a-623">下列範例會列舉電腦上所有硬碟上的可用空間。</span><span class="sxs-lookup"><span data-stu-id="0765a-623">The following samples enumerate the free space on all the hard disk drives on a computer.</span></span>


```VB
Const HARD_DISK = 3
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("SELECT * FROM Win32_LogicalDisk WHERE DriveType = " & HARD_DISK & "")
For Each objDisk in colDisks
 Wscript.Echo "Device ID: " & objDisk.DeviceID 
 Wscript.Echo "Free Disk Space: " & objDisk.FreeSpace
Next
```


```CSharp

//be sure to References->Add->System.Management to your project
using System.Management;
...

const int HARD_DISK = 3;
string strComputer = &quot;.&quot;;

ManagementScope namespaceScope = new ManagementScope(&quot;\\\\&quot; + strComputer + &quot;\\ROOT\\CIMV2&quot;);
ObjectQuery diskQuery = new ObjectQuery(&quot;SELECT * FROM Win32_LogicalDisk WHERE DriveType = &quot; + HARD_DISK + &quot;&quot;);
ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher(namespaceScope, diskQuery);
ManagementObjectCollection colDisks = mgmtObjSearcher.Get();

foreach (ManagementObject objDisk in colDisks)
{
    Console.WriteLine(&quot;Device ID : {0}&quot;, objDisk[&quot;DeviceID&quot;]);
    Console.WriteLine(&quot;Free Disk Space : {0}&quot;, objDisk[&quot;FreeSpace&quot;]);
    Console.ReadLine();
}
```





<span data-ttu-id="0765a-624">下列程式碼範例會傳回電腦上每個磁片磁碟機上的檔案系統類型 (FAT、NTFS、FAT32 等) 。</span><span class="sxs-lookup"><span data-stu-id="0765a-624">The following code example returns the type of file system (FAT, NTFS, FAT32, and so on) used on each drive in a computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colDisks = objWMIService.ExecQuery ("Select * from Win32_LogicalDisk")
For Each objDisk in colDisks
    Wscript.Echo "DeviceID: "& vbTab &  objDisk.DeviceID  
    Wscript.Echo "File System: "& vbTab & objDisk.FileSystem
Next
```


```PowerShell

Get-WMIObject Win32_LogicalDisk | Select DeviceID, FileSystem | Format=Table -AutoSize
```





<span data-ttu-id="0765a-625">下列 PowerShell 程式碼範例會抓取邏輯本機磁片的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0765a-625">The following PowerShell code sample retrieves additional information about the logical local disks.</span></span>


```PowerShell
Write-Host "Drive information for $env:ComputerName"

Get-WmiObject -Class Win32_LogicalDisk |
    Where-Object {$_.DriveType -ne 5} |
    Sort-Object -Property Name | 
    Select-Object Name, VolumeName, FileSystem, Description, VolumeDirty, `
        @{"Label"="DiskSize(GB)";"Expression"={"{0:N}" -f ($_.Size/1GB) -as [float]}}, `
        @{"Label"="FreeSpace(GB)";"Expression"={"{0:N}" -f ($_.FreeSpace/1GB) -as [float]}}, `
        @{"Label"="%Free";"Expression"={"{0:N}" -f ($_.FreeSpace/$_.Size*100) -as [float]}} |
    Format-Table -AutoSize
```



## <a name="requirements"></a><span data-ttu-id="0765a-626">規格需求</span><span class="sxs-lookup"><span data-stu-id="0765a-626">Requirements</span></span>



| <span data-ttu-id="0765a-627">需求</span><span class="sxs-lookup"><span data-stu-id="0765a-627">Requirement</span></span> | <span data-ttu-id="0765a-628">值</span><span class="sxs-lookup"><span data-stu-id="0765a-628">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0765a-629">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0765a-629">Minimum supported client</span></span><br/> | <span data-ttu-id="0765a-630">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0765a-630">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0765a-631">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0765a-631">Minimum supported server</span></span><br/> | <span data-ttu-id="0765a-632">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0765a-632">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0765a-633">命名空間</span><span class="sxs-lookup"><span data-stu-id="0765a-633">Namespace</span></span><br/>                | <span data-ttu-id="0765a-634">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0765a-634">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0765a-635">MOF</span><span class="sxs-lookup"><span data-stu-id="0765a-635">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0765a-636"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="0765a-636"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0765a-637">DLL</span><span class="sxs-lookup"><span data-stu-id="0765a-637">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0765a-638"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0765a-638"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0765a-639">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0765a-639">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0765a-640">**CIM \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="0765a-640">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="0765a-641">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="0765a-641">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="0765a-642">WMI 工作：磁片和檔案系統</span><span class="sxs-lookup"><span data-stu-id="0765a-642">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

