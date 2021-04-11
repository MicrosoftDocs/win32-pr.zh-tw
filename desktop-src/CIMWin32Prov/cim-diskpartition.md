---
description: CIM \_ DiskPartition 類別代表由作業系統透過分割區的類型和子類型欄位識別的連續邏輯區塊範圍。
ms.assetid: 22a0e5be-c66b-40a2-9a7a-047d2edc0278
ms.tgt_platform: multiple
title: CIM_DiskPartition 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskPartition
- CIM_DiskPartition.Access
- CIM_DiskPartition.Availability
- CIM_DiskPartition.BlockSize
- CIM_DiskPartition.Bootable
- CIM_DiskPartition.Caption
- CIM_DiskPartition.ConfigManagerErrorCode
- CIM_DiskPartition.ConfigManagerUserConfig
- CIM_DiskPartition.CreationClassName
- CIM_DiskPartition.Description
- CIM_DiskPartition.DeviceID
- CIM_DiskPartition.ErrorCleared
- CIM_DiskPartition.ErrorDescription
- CIM_DiskPartition.ErrorMethodology
- CIM_DiskPartition.InstallDate
- CIM_DiskPartition.LastErrorCode
- CIM_DiskPartition.Name
- CIM_DiskPartition.NumberOfBlocks
- CIM_DiskPartition.PNPDeviceID
- CIM_DiskPartition.PowerManagementCapabilities
- CIM_DiskPartition.PowerManagementSupported
- CIM_DiskPartition.PrimaryPartition
- CIM_DiskPartition.Purpose
- CIM_DiskPartition.Status
- CIM_DiskPartition.StatusInfo
- CIM_DiskPartition.SystemCreationClassName
- CIM_DiskPartition.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d1761e140813c26e67594872df5a8d2f7361768b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847430"
---
# <a name="cim_diskpartition-class"></a><span data-ttu-id="7b96a-103">CIM \_ DiskPartition 類別</span><span class="sxs-lookup"><span data-stu-id="7b96a-103">CIM\_DiskPartition class</span></span>

<span data-ttu-id="7b96a-104">**CIM \_ DiskPartition** 類別代表由作業系統透過分割區的類型和子類型欄位識別的連續邏輯區塊範圍。</span><span class="sxs-lookup"><span data-stu-id="7b96a-104">The **CIM\_DiskPartition** class represents a contiguous range of logical blocks that is identifiable by the operating system by way of the partition's type and subtype fields.</span></span> <span data-ttu-id="7b96a-105">磁碟分割應由 [**CIM \_ RealizesDiskPartition**](cim-realizesdiskpartition.md) 關聯) 或建立于儲存磁片區的實體媒體 (直接實現。</span><span class="sxs-lookup"><span data-stu-id="7b96a-105">Disk partitions should be directly realized by physical media (indicated by the [**CIM\_RealizesDiskPartition**](cim-realizesdiskpartition.md) association) or built on storage volumes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7b96a-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="7b96a-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7b96a-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7b96a-108">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="7b96a-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7b96a-109">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="7b96a-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b96a-110">語法</span><span class="sxs-lookup"><span data-stu-id="7b96a-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C541-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DiskPartition : CIM_StorageExtent
{
  uint16   Access;
  uint16   Availability;
  uint64   BlockSize;
  boolean  Bootable;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  boolean  PrimaryPartition;
  string   Purpose;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="7b96a-111">成員</span><span class="sxs-lookup"><span data-stu-id="7b96a-111">Members</span></span>

<span data-ttu-id="7b96a-112">**CIM \_ DiskPartition** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7b96a-112">The **CIM\_DiskPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="7b96a-113">方法</span><span class="sxs-lookup"><span data-stu-id="7b96a-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="7b96a-114">屬性</span><span class="sxs-lookup"><span data-stu-id="7b96a-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7b96a-115">方法</span><span class="sxs-lookup"><span data-stu-id="7b96a-115">Methods</span></span>

<span data-ttu-id="7b96a-116">**CIM \_ DiskPartition** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="7b96a-116">The **CIM\_DiskPartition** class has these methods.</span></span>



| <span data-ttu-id="7b96a-117">方法</span><span class="sxs-lookup"><span data-stu-id="7b96a-117">Method</span></span>                                                                   | <span data-ttu-id="7b96a-118">描述</span><span class="sxs-lookup"><span data-stu-id="7b96a-118">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7b96a-119">**重設**</span><span class="sxs-lookup"><span data-stu-id="7b96a-119">**Reset**</span></span>](reset-method-in-class-cim-diskpartition.md)                 | <span data-ttu-id="7b96a-120">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="7b96a-120">Requests a reset of the logical device.</span></span> <span data-ttu-id="7b96a-121">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="7b96a-121">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="7b96a-122">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="7b96a-122">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-diskpartition.md) | <span data-ttu-id="7b96a-123">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="7b96a-123">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="7b96a-124">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="7b96a-124">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7b96a-125">屬性</span><span class="sxs-lookup"><span data-stu-id="7b96a-125">Properties</span></span>

<span data-ttu-id="7b96a-126">**CIM \_ DiskPartition** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7b96a-126">The **CIM\_DiskPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b96a-127">**存取**</span><span class="sxs-lookup"><span data-stu-id="7b96a-127">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b96a-128">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7b96a-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b96a-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b96a-130">指定媒體是否為可讀取、可寫入或兩者皆可讀取。</span><span class="sxs-lookup"><span data-stu-id="7b96a-130">Specifies whether the media is readable, writeable, or both, for example.</span></span> <span data-ttu-id="7b96a-131">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-131">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7b96a-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="7b96a-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-133">不明。</span><span class="sxs-lookup"><span data-stu-id="7b96a-133">Unknown.</span></span>

</dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="7b96a-134"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**可讀取** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="7b96a-134"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-135">讀。</span><span class="sxs-lookup"><span data-stu-id="7b96a-135">Readable.</span></span>

</dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="7b96a-136"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>可 **寫入** (2) </span><span class="sxs-lookup"><span data-stu-id="7b96a-136"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-137">寫入.</span><span class="sxs-lookup"><span data-stu-id="7b96a-137">Writeable.</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="7b96a-138"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>支援 (3) 的 **讀取/寫入**</span><span class="sxs-lookup"><span data-stu-id="7b96a-138"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-139">支援讀取/寫入。</span><span class="sxs-lookup"><span data-stu-id="7b96a-139">Read/write supported.</span></span>

</dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="7b96a-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**撰寫一次** (4) </span><span class="sxs-lookup"><span data-stu-id="7b96a-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-141">寫入一次。</span><span class="sxs-lookup"><span data-stu-id="7b96a-141">Write once.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7b96a-142">**可用性**</span><span class="sxs-lookup"><span data-stu-id="7b96a-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b96a-143">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7b96a-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b96a-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-145">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="7b96a-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="7b96a-146">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="7b96a-146">Availability and status of the device.</span></span>

<span data-ttu-id="7b96a-147">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-147">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7b96a-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="7b96a-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7b96a-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="7b96a-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="7b96a-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="7b96a-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="7b96a-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="7b96a-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="7b96a-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="7b96a-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7b96a-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="7b96a-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="7b96a-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="7b96a-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="7b96a-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="7b96a-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="7b96a-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="7b96a-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7b96a-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="7b96a-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="7b96a-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="7b96a-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="7b96a-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="7b96a-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="7b96a-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="7b96a-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-161">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="7b96a-161">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="7b96a-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="7b96a-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-163">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="7b96a-163">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="7b96a-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="7b96a-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-165">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="7b96a-165">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="7b96a-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="7b96a-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="7b96a-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="7b96a-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-168">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="7b96a-168">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="7b96a-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="7b96a-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-170">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="7b96a-170">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="7b96a-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="7b96a-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-172">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="7b96a-172">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="7b96a-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="7b96a-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-174">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="7b96a-174">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="7b96a-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="7b96a-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-176">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="7b96a-176">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7b96a-177">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="7b96a-177">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b96a-178">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="7b96a-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b96a-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-180">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrStorageAllocationUnits ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="7b96a-180">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="7b96a-181">形成儲存範圍之區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7b96a-181">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="7b96a-182">如果它是變數區塊大小，則應該指定最大區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7b96a-182">If it is a variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="7b96a-183">如果區塊大小未知，或區塊概念無效 (例如，針對匯總延伸區、記憶體或邏輯磁片) ，請輸入值1。</span><span class="sxs-lookup"><span data-stu-id="7b96a-183">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter the value 1.</span></span>

<span data-ttu-id="7b96a-184">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-184">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="7b96a-185">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-185">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="7b96a-186">**啟動**</span><span class="sxs-lookup"><span data-stu-id="7b96a-186">**Bootable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b96a-187">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="7b96a-187">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b96a-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b96a-189">若 **為 TRUE**，則會將磁碟分割標示為可開機。</span><span class="sxs-lookup"><span data-stu-id="7b96a-189">If **TRUE**, the disk partition is labeled as bootable.</span></span> <span data-ttu-id="7b96a-190">這並不表示已在磁碟分割上載入作業系統。</span><span class="sxs-lookup"><span data-stu-id="7b96a-190">This does not mean that an operating system is loaded on the partition.</span></span>

</dd> <dt>

<span data-ttu-id="7b96a-191">**標題**</span><span class="sxs-lookup"><span data-stu-id="7b96a-191">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b96a-192">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7b96a-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b96a-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-194">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="7b96a-194">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7b96a-195">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="7b96a-195">Short textual description of the object.</span></span>

<span data-ttu-id="7b96a-196">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b96a-197">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7b96a-197">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b96a-198">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7b96a-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b96a-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-200">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="7b96a-200">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7b96a-201">Windows 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7b96a-201">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="7b96a-202">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-202">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="7b96a-203"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-203"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="7b96a-204"> (0)</span><span class="sxs-lookup"><span data-stu-id="7b96a-204">(0)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-205">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="7b96a-205">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="7b96a-206"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-206"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="7b96a-207">(1)</span><span class="sxs-lookup"><span data-stu-id="7b96a-207">(1)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-208">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="7b96a-208">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7b96a-209"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-209"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="7b96a-210">(2)</span><span class="sxs-lookup"><span data-stu-id="7b96a-210">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="7b96a-211"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-211"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="7b96a-212">(3)</span><span class="sxs-lookup"><span data-stu-id="7b96a-212">(3)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-213">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="7b96a-213">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7b96a-214"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-214"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="7b96a-215">(4)</span><span class="sxs-lookup"><span data-stu-id="7b96a-215">(4)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-216">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="7b96a-216">Device is not working properly.</span></span> <span data-ttu-id="7b96a-217">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="7b96a-217">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="7b96a-218"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-218"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="7b96a-219">(5)</span><span class="sxs-lookup"><span data-stu-id="7b96a-219">(5)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-220">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="7b96a-220">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="7b96a-221"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-221"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="7b96a-222">(6)</span><span class="sxs-lookup"><span data-stu-id="7b96a-222">(6)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-223">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="7b96a-223">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="7b96a-224"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-224"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="7b96a-225">(7)</span><span class="sxs-lookup"><span data-stu-id="7b96a-225">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="7b96a-226"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-226"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="7b96a-227">(8)</span><span class="sxs-lookup"><span data-stu-id="7b96a-227">(8)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-228">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="7b96a-228">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="7b96a-229"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-229"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="7b96a-230">(9)</span><span class="sxs-lookup"><span data-stu-id="7b96a-230">(9)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-231">裝置無法正常運作;控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="7b96a-231">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="7b96a-232"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-232"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="7b96a-233">(10)</span><span class="sxs-lookup"><span data-stu-id="7b96a-233">(10)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-234">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="7b96a-234">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="7b96a-235"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-235"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="7b96a-236">(11)</span><span class="sxs-lookup"><span data-stu-id="7b96a-236">(11)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-237">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="7b96a-237">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="7b96a-238"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-238"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="7b96a-239"> (12) </span><span class="sxs-lookup"><span data-stu-id="7b96a-239">(12)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-240">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="7b96a-240">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="7b96a-241"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-241"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="7b96a-242">(13)</span><span class="sxs-lookup"><span data-stu-id="7b96a-242">(13)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-243">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="7b96a-243">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="7b96a-244"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-244"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="7b96a-245">(14)</span><span class="sxs-lookup"><span data-stu-id="7b96a-245">(14)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-246">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="7b96a-246">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="7b96a-247"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-247"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="7b96a-248">(15)</span><span class="sxs-lookup"><span data-stu-id="7b96a-248">(15)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-249">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="7b96a-249">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="7b96a-250"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-250"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="7b96a-251">(16)</span><span class="sxs-lookup"><span data-stu-id="7b96a-251">(16)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-252">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="7b96a-252">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="7b96a-253"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-253"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="7b96a-254">(17)</span><span class="sxs-lookup"><span data-stu-id="7b96a-254">(17)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-255">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="7b96a-255">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7b96a-256"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-256"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="7b96a-257">(18)</span><span class="sxs-lookup"><span data-stu-id="7b96a-257">(18)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-258">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="7b96a-258">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="7b96a-259"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-259"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="7b96a-260">(19)</span><span class="sxs-lookup"><span data-stu-id="7b96a-260">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7b96a-261"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-261"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="7b96a-262">(20)</span><span class="sxs-lookup"><span data-stu-id="7b96a-262">(20)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-263">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="7b96a-263">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="7b96a-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="7b96a-265">(21)</span><span class="sxs-lookup"><span data-stu-id="7b96a-265">(21)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-266">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="7b96a-266">System failure.</span></span> <span data-ttu-id="7b96a-267">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="7b96a-267">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="7b96a-268">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="7b96a-268">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="7b96a-269"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-269"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="7b96a-270">(22)</span><span class="sxs-lookup"><span data-stu-id="7b96a-270">(22)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-271">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="7b96a-271">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="7b96a-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="7b96a-273">(23)</span><span class="sxs-lookup"><span data-stu-id="7b96a-273">(23)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-274">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="7b96a-274">System failure.</span></span> <span data-ttu-id="7b96a-275">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="7b96a-275">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="7b96a-276"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-276"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="7b96a-277">(24)</span><span class="sxs-lookup"><span data-stu-id="7b96a-277">(24)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-278">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="7b96a-278">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7b96a-279"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-279"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="7b96a-280">(25)</span><span class="sxs-lookup"><span data-stu-id="7b96a-280">(25)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-281">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="7b96a-281">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7b96a-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="7b96a-283">(26)</span><span class="sxs-lookup"><span data-stu-id="7b96a-283">(26)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-284">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="7b96a-284">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="7b96a-285"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-285"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="7b96a-286">(27)</span><span class="sxs-lookup"><span data-stu-id="7b96a-286">(27)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-287">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="7b96a-287">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="7b96a-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="7b96a-289">(28)</span><span class="sxs-lookup"><span data-stu-id="7b96a-289">(28)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-290">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="7b96a-290">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="7b96a-291"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-291"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="7b96a-292">(29)</span><span class="sxs-lookup"><span data-stu-id="7b96a-292">(29)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-293">裝置已停用;裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="7b96a-293">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="7b96a-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="7b96a-295">(30)</span><span class="sxs-lookup"><span data-stu-id="7b96a-295">(30)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-296">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="7b96a-296">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7b96a-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="7b96a-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="7b96a-298"> (31) </span><span class="sxs-lookup"><span data-stu-id="7b96a-298">(31)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-299">裝置無法正常運作;Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="7b96a-299">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7b96a-300">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="7b96a-300">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b96a-301">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="7b96a-301">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-302">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b96a-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-303">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="7b96a-303">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7b96a-304">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="7b96a-304">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="7b96a-305">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-305">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b96a-306">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7b96a-306">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b96a-307">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7b96a-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-308">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b96a-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-309">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b96a-309">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b96a-310">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="7b96a-310">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="7b96a-311">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="7b96a-311">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="7b96a-312">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-312">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b96a-313">**說明**</span><span class="sxs-lookup"><span data-stu-id="7b96a-313">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b96a-314">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7b96a-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-315">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b96a-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-316">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="7b96a-316">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7b96a-317">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="7b96a-317">Textual description of the object.</span></span>

<span data-ttu-id="7b96a-318">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-318">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b96a-319">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="7b96a-319">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b96a-320">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7b96a-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b96a-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-322">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b96a-322">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b96a-323">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="7b96a-323">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="7b96a-324">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b96a-325">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="7b96a-325">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b96a-326">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="7b96a-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-327">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b96a-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b96a-328">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="7b96a-328">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="7b96a-329">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b96a-330">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="7b96a-330">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b96a-331">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7b96a-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-332">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b96a-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b96a-333">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的詳細資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="7b96a-333">Free-form string that supplies more information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="7b96a-334">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b96a-335">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="7b96a-335">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b96a-336">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7b96a-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-337">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b96a-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b96a-338">描述儲存範圍所支援之錯誤偵測和更正類型的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="7b96a-338">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="7b96a-339">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-339">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b96a-340">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7b96a-340">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b96a-341">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="7b96a-341">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-342">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b96a-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-343">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="7b96a-343">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7b96a-344">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="7b96a-344">Date and time the object was installed.</span></span> <span data-ttu-id="7b96a-345">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="7b96a-345">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="7b96a-346">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-346">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b96a-347">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7b96a-347">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b96a-348">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7b96a-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-349">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b96a-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b96a-350">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7b96a-350">Last error code reported by the logical device.</span></span>

<span data-ttu-id="7b96a-351">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-351">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b96a-352">**名稱**</span><span class="sxs-lookup"><span data-stu-id="7b96a-352">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b96a-353">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7b96a-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-354">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b96a-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-355">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="7b96a-355">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7b96a-356">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="7b96a-356">Label by which the object is known.</span></span> <span data-ttu-id="7b96a-357">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="7b96a-357">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="7b96a-358">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-358">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b96a-359">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="7b96a-359">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b96a-360">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="7b96a-360">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-361">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b96a-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-362">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrStorageSize ") </span><span class="sxs-lookup"><span data-stu-id="7b96a-362">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="7b96a-363">連續區塊的數目，每個區塊會封鎖包含在 **區塊** 屬性中的值大小，以形成儲存區的範圍。</span><span class="sxs-lookup"><span data-stu-id="7b96a-363">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which forms the storage extent.</span></span> <span data-ttu-id="7b96a-364">您可以將 [ **區塊** ] 屬性的值乘以這個屬性的值，以計算儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="7b96a-364">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="7b96a-365">如果 **區塊** 的值是1，則這個屬性是儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="7b96a-365">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="7b96a-366">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-366">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="7b96a-367">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-367">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="7b96a-368">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="7b96a-368">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b96a-369">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7b96a-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-370">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b96a-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-371">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="7b96a-371">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7b96a-372">邏輯裝置的 Win32 隨插即用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="7b96a-372">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="7b96a-373">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-373">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="7b96a-374">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="7b96a-374">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="7b96a-375">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="7b96a-375">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b96a-376">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="7b96a-376">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-377">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b96a-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b96a-378">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="7b96a-378">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="7b96a-379">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="7b96a-379">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7b96a-380"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="7b96a-380"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="7b96a-381"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="7b96a-381"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7b96a-382"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="7b96a-382"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7b96a-383"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="7b96a-383"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-384">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="7b96a-384">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="7b96a-385"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="7b96a-385"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-386">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="7b96a-386">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="7b96a-387"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="7b96a-387"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-388">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="7b96a-388">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="7b96a-389">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="7b96a-389">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="7b96a-390">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-390">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="7b96a-391"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="7b96a-391"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-392">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="7b96a-392">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="7b96a-393"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="7b96a-393"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="7b96a-394">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="7b96a-394">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7b96a-395">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="7b96a-395">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b96a-396">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="7b96a-396">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-397">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b96a-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b96a-398">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="7b96a-398">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="7b96a-399">如果 **為 False**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="7b96a-399">If **False**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="7b96a-400">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="7b96a-400">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="7b96a-401">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="7b96a-401">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="7b96a-402">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-402">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b96a-403">**PrimaryPartition**</span><span class="sxs-lookup"><span data-stu-id="7b96a-403">**PrimaryPartition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b96a-404">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="7b96a-404">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-405">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b96a-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b96a-406">若 **為 TRUE**，則會將磁碟分割標示為電腦系統的主要磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="7b96a-406">If **TRUE**, the disk partition is labeled as the primary partition for a computer system.</span></span>

</dd> <dt>

<span data-ttu-id="7b96a-407">**目的**</span><span class="sxs-lookup"><span data-stu-id="7b96a-407">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b96a-408">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7b96a-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-409">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b96a-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b96a-410">描述媒體及其用途。</span><span class="sxs-lookup"><span data-stu-id="7b96a-410">Describes the media and its use.</span></span>

<span data-ttu-id="7b96a-411">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-411">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b96a-412">**狀態**</span><span class="sxs-lookup"><span data-stu-id="7b96a-412">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b96a-413">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7b96a-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-414">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b96a-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-415">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="7b96a-415">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7b96a-416">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="7b96a-416">Current status of the object.</span></span>

<span data-ttu-id="7b96a-417">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-417">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7b96a-418">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="7b96a-418">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7b96a-419">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="7b96a-419">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7b96a-420">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="7b96a-420">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7b96a-421">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="7b96a-421">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7b96a-422">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="7b96a-422">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7b96a-423">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="7b96a-423">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7b96a-424">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="7b96a-424">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7b96a-425">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="7b96a-425">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7b96a-426">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="7b96a-426">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7b96a-427">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="7b96a-427">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7b96a-428">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="7b96a-428">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7b96a-429">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="7b96a-429">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7b96a-430">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="7b96a-430">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7b96a-431">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="7b96a-431">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b96a-432">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7b96a-432">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-433">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b96a-433">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-434">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="7b96a-434">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="7b96a-435">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="7b96a-435">State of the logical device.</span></span> <span data-ttu-id="7b96a-436">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="7b96a-436">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="7b96a-437">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-437">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7b96a-438">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="7b96a-438">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7b96a-439">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="7b96a-439">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7b96a-440">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="7b96a-440">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7b96a-441">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="7b96a-441">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7b96a-442">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="7b96a-442">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7b96a-443">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7b96a-443">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b96a-444">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7b96a-444">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-445">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b96a-445">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-446">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b96a-446">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b96a-447">設定系統的 **CreationClassName** 屬性範圍。</span><span class="sxs-lookup"><span data-stu-id="7b96a-447">Scoping system's **CreationClassName** property.</span></span>

<span data-ttu-id="7b96a-448">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-448">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b96a-449">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="7b96a-449">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b96a-450">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7b96a-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-451">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b96a-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b96a-452">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b96a-452">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b96a-453">範圍系統的 **名稱** 屬性。</span><span class="sxs-lookup"><span data-stu-id="7b96a-453">Scoping system's **Name** property.</span></span>

<span data-ttu-id="7b96a-454">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-454">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b96a-455">備註</span><span class="sxs-lookup"><span data-stu-id="7b96a-455">Remarks</span></span>

<span data-ttu-id="7b96a-456">**Cim \_ DiskPartition** 類別衍生自 [**cim \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-456">The **CIM\_DiskPartition** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="7b96a-457">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="7b96a-457">WMI does not implement this class.</span></span> <span data-ttu-id="7b96a-458">針對衍生自 **CIM \_ DiskPartition** 的類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="7b96a-458">For classes derived from **CIM\_DiskPartition**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="7b96a-459">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="7b96a-459">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7b96a-460">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="7b96a-460">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b96a-461">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b96a-461">Requirements</span></span>



| <span data-ttu-id="7b96a-462">需求</span><span class="sxs-lookup"><span data-stu-id="7b96a-462">Requirement</span></span> | <span data-ttu-id="7b96a-463">值</span><span class="sxs-lookup"><span data-stu-id="7b96a-463">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b96a-464">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7b96a-464">Minimum supported client</span></span><br/> | <span data-ttu-id="7b96a-465">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b96a-465">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7b96a-466">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7b96a-466">Minimum supported server</span></span><br/> | <span data-ttu-id="7b96a-467">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b96a-467">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7b96a-468">命名空間</span><span class="sxs-lookup"><span data-stu-id="7b96a-468">Namespace</span></span><br/>                | <span data-ttu-id="7b96a-469">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7b96a-469">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7b96a-470">MOF</span><span class="sxs-lookup"><span data-stu-id="7b96a-470">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b96a-471"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b96a-471"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b96a-472">DLL</span><span class="sxs-lookup"><span data-stu-id="7b96a-472">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b96a-473"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b96a-473"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b96a-474">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b96a-474">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b96a-475">**CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="7b96a-475">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

