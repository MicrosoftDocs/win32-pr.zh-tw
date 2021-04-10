---
description: CIM \_ PhysicalExtent 類別代表 SCC RAID 的執行。
ms.assetid: d1950464-e17a-4651-aa53-6385659994ff
ms.tgt_platform: multiple
title: CIM_PhysicalExtent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalExtent
- CIM_PhysicalExtent.Access
- CIM_PhysicalExtent.Availability
- CIM_PhysicalExtent.BlockSize
- CIM_PhysicalExtent.Caption
- CIM_PhysicalExtent.ConfigManagerErrorCode
- CIM_PhysicalExtent.ConfigManagerUserConfig
- CIM_PhysicalExtent.CreationClassName
- CIM_PhysicalExtent.Description
- CIM_PhysicalExtent.DeviceID
- CIM_PhysicalExtent.ErrorCleared
- CIM_PhysicalExtent.ErrorDescription
- CIM_PhysicalExtent.ErrorMethodology
- CIM_PhysicalExtent.InstallDate
- CIM_PhysicalExtent.LastErrorCode
- CIM_PhysicalExtent.Name
- CIM_PhysicalExtent.NumberOfBlocks
- CIM_PhysicalExtent.PNPDeviceID
- CIM_PhysicalExtent.PowerManagementCapabilities
- CIM_PhysicalExtent.PowerManagementSupported
- CIM_PhysicalExtent.Purpose
- CIM_PhysicalExtent.Status
- CIM_PhysicalExtent.StatusInfo
- CIM_PhysicalExtent.SystemCreationClassName
- CIM_PhysicalExtent.SystemName
- CIM_PhysicalExtent.UnitsBeforeCheckDataInterleave
- CIM_PhysicalExtent.UnitsOfCheckData
- CIM_PhysicalExtent.UnitsOfUserData
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 31e05d3b339d64fd640460716376c3d8b538fa95
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688600"
---
# <a name="cim_physicalextent-class"></a><span data-ttu-id="145ca-103">CIM \_ PhysicalExtent 類別</span><span class="sxs-lookup"><span data-stu-id="145ca-103">CIM\_PhysicalExtent class</span></span>

<span data-ttu-id="145ca-104">**CIM \_ PhysicalExtent** 類別代表 SCC RAID 的執行。</span><span class="sxs-lookup"><span data-stu-id="145ca-104">The **CIM\_PhysicalExtent** class represents an SCC RAID implementation.</span></span> <span data-ttu-id="145ca-105">它會在單一存放裝置上定義連續可定址的區塊位址，這些位址會被視為相同 [**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md) 類別中的單一儲存區。</span><span class="sxs-lookup"><span data-stu-id="145ca-105">It defines the consecutive addressable block addresses on a single storage device that are treated as a single storage extent in the same [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) class.</span></span> <span data-ttu-id="145ca-106">替代方式是使用自動設定時，是要具現化或擴充 [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="145ca-106">An alternative, when automatic configuration is used, is to instantiate or extend the [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="145ca-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="145ca-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="145ca-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="145ca-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="145ca-109">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="145ca-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="145ca-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="145ca-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="145ca-111">語法</span><span class="sxs-lookup"><span data-stu-id="145ca-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{9565979E-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalExtent : CIM_StorageExtent
{
  uint16   Access;
  uint16   Availability;
  uint64   BlockSize;
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
  string   Purpose;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint64   UnitsBeforeCheckDataInterleave;
  uint64   UnitsOfCheckData;
  uint64   UnitsOfUserData;
};
```

## <a name="members"></a><span data-ttu-id="145ca-112">成員</span><span class="sxs-lookup"><span data-stu-id="145ca-112">Members</span></span>

<span data-ttu-id="145ca-113">**CIM \_ PhysicalExtent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="145ca-113">The **CIM\_PhysicalExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="145ca-114">方法</span><span class="sxs-lookup"><span data-stu-id="145ca-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="145ca-115">屬性</span><span class="sxs-lookup"><span data-stu-id="145ca-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="145ca-116">方法</span><span class="sxs-lookup"><span data-stu-id="145ca-116">Methods</span></span>

<span data-ttu-id="145ca-117">**CIM \_ PhysicalExtent** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="145ca-117">The **CIM\_PhysicalExtent** class has these methods.</span></span>



| <span data-ttu-id="145ca-118">方法</span><span class="sxs-lookup"><span data-stu-id="145ca-118">Method</span></span>                                                                    | <span data-ttu-id="145ca-119">描述</span><span class="sxs-lookup"><span data-stu-id="145ca-119">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="145ca-120">**重設**</span><span class="sxs-lookup"><span data-stu-id="145ca-120">**Reset**</span></span>](reset-method-in-class-cim-physicalextent.md)                 | <span data-ttu-id="145ca-121">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="145ca-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="145ca-122">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="145ca-122">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="145ca-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="145ca-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-physicalextent.md) | <span data-ttu-id="145ca-124">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="145ca-124">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="145ca-125">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="145ca-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="145ca-126">屬性</span><span class="sxs-lookup"><span data-stu-id="145ca-126">Properties</span></span>

<span data-ttu-id="145ca-127">**CIM \_ PhysicalExtent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="145ca-127">The **CIM\_PhysicalExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="145ca-128">**存取**</span><span class="sxs-lookup"><span data-stu-id="145ca-128">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145ca-129">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="145ca-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="145ca-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145ca-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="145ca-131">媒體的讀取/寫入屬性。</span><span class="sxs-lookup"><span data-stu-id="145ca-131">Read/write properties of the media.</span></span>

<span data-ttu-id="145ca-132">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="145ca-132">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="145ca-133">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="145ca-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="145ca-134">**可讀取** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="145ca-134">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="145ca-135">可 **寫入** (2) </span><span class="sxs-lookup"><span data-stu-id="145ca-135">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="145ca-136">支援 (3) 的 **讀取/寫入**</span><span class="sxs-lookup"><span data-stu-id="145ca-136">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="145ca-137">**撰寫一次** (4) </span><span class="sxs-lookup"><span data-stu-id="145ca-137">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="145ca-138">**可用性**</span><span class="sxs-lookup"><span data-stu-id="145ca-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145ca-139">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="145ca-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="145ca-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145ca-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145ca-141">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="145ca-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="145ca-142">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="145ca-142">Availability and status of the device.</span></span>

<span data-ttu-id="145ca-143">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="145ca-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="145ca-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="145ca-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="145ca-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="145ca-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="145ca-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="145ca-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-147">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="145ca-147">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="145ca-148"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="145ca-148"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="145ca-149"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="145ca-149"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="145ca-150"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="145ca-150"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="145ca-151"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="145ca-151"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="145ca-152"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="145ca-152"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="145ca-153"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="145ca-153"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="145ca-154"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="145ca-154"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="145ca-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="145ca-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="145ca-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="145ca-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="145ca-157"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="145ca-157"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-158">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="145ca-158">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="145ca-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="145ca-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-160">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="145ca-160">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="145ca-161"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="145ca-161"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-162">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="145ca-162">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="145ca-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="145ca-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="145ca-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="145ca-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-165">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="145ca-165">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="145ca-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="145ca-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-167">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="145ca-167">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="145ca-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="145ca-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-169">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="145ca-169">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="145ca-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="145ca-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-171">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="145ca-171">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="145ca-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="145ca-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-173">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="145ca-173">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="145ca-174">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="145ca-174">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145ca-175">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="145ca-175">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="145ca-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145ca-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145ca-177">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「區塊」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 實體範圍 \| 001.4 ") </span><span class="sxs-lookup"><span data-stu-id="145ca-177">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("BlockSize"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="145ca-178">形成儲存範圍之區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="145ca-178">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="145ca-179">如果變數區塊大小，則應該指定最大區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="145ca-179">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="145ca-180">如果區塊大小未知或區塊概念無效 (例如，針對匯總延伸區、記憶體或邏輯磁片) ，請輸入 1 (一個) 。</span><span class="sxs-lookup"><span data-stu-id="145ca-180">If the block size is unknown or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one) .</span></span>

<span data-ttu-id="145ca-181">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="145ca-181">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="145ca-182">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="145ca-182">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="145ca-183">**標題**</span><span class="sxs-lookup"><span data-stu-id="145ca-183">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145ca-184">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="145ca-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="145ca-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145ca-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145ca-186">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="145ca-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="145ca-187">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="145ca-187">Short textual description of the object.</span></span>

<span data-ttu-id="145ca-188">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="145ca-188">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="145ca-189">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="145ca-189">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145ca-190">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="145ca-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="145ca-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145ca-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145ca-192">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="145ca-192">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="145ca-193">Windows 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="145ca-193">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="145ca-194">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="145ca-194">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="145ca-195"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="145ca-195"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="145ca-196"> (0)</span><span class="sxs-lookup"><span data-stu-id="145ca-196">(0)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-197">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="145ca-197">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="145ca-198"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="145ca-198"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="145ca-199">(1)</span><span class="sxs-lookup"><span data-stu-id="145ca-199">(1)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-200">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="145ca-200">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="145ca-201"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="145ca-201"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="145ca-202">(2)</span><span class="sxs-lookup"><span data-stu-id="145ca-202">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="145ca-203"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="145ca-203"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="145ca-204">(3)</span><span class="sxs-lookup"><span data-stu-id="145ca-204">(3)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-205">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="145ca-205">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="145ca-206"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="145ca-206"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="145ca-207">(4)</span><span class="sxs-lookup"><span data-stu-id="145ca-207">(4)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-208">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="145ca-208">Device is not working properly.</span></span> <span data-ttu-id="145ca-209">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="145ca-209">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="145ca-210"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="145ca-210"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="145ca-211">(5)</span><span class="sxs-lookup"><span data-stu-id="145ca-211">(5)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-212">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="145ca-212">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="145ca-213"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="145ca-213"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="145ca-214">(6)</span><span class="sxs-lookup"><span data-stu-id="145ca-214">(6)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-215">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="145ca-215">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="145ca-216"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="145ca-216"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="145ca-217">(7)</span><span class="sxs-lookup"><span data-stu-id="145ca-217">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="145ca-218"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="145ca-218"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="145ca-219">(8)</span><span class="sxs-lookup"><span data-stu-id="145ca-219">(8)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-220">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="145ca-220">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="145ca-221"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="145ca-221"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="145ca-222">(9)</span><span class="sxs-lookup"><span data-stu-id="145ca-222">(9)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-223">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="145ca-223">Device is not working properly.</span></span> <span data-ttu-id="145ca-224">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="145ca-224">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="145ca-225"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="145ca-225"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="145ca-226">(10)</span><span class="sxs-lookup"><span data-stu-id="145ca-226">(10)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-227">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="145ca-227">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="145ca-228"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="145ca-228"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="145ca-229">(11)</span><span class="sxs-lookup"><span data-stu-id="145ca-229">(11)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-230">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="145ca-230">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="145ca-231"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="145ca-231"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="145ca-232"> (12) </span><span class="sxs-lookup"><span data-stu-id="145ca-232">(12)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-233">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="145ca-233">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="145ca-234"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="145ca-234"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="145ca-235">(13)</span><span class="sxs-lookup"><span data-stu-id="145ca-235">(13)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-236">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="145ca-236">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="145ca-237"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="145ca-237"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="145ca-238">(14)</span><span class="sxs-lookup"><span data-stu-id="145ca-238">(14)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-239">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="145ca-239">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="145ca-240"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="145ca-240"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="145ca-241">(15)</span><span class="sxs-lookup"><span data-stu-id="145ca-241">(15)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-242">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="145ca-242">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="145ca-243"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="145ca-243"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="145ca-244">(16)</span><span class="sxs-lookup"><span data-stu-id="145ca-244">(16)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-245">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="145ca-245">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="145ca-246"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="145ca-246"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="145ca-247">(17)</span><span class="sxs-lookup"><span data-stu-id="145ca-247">(17)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-248">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="145ca-248">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="145ca-249"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="145ca-249"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="145ca-250">(18)</span><span class="sxs-lookup"><span data-stu-id="145ca-250">(18)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-251">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="145ca-251">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="145ca-252"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="145ca-252"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="145ca-253">(19)</span><span class="sxs-lookup"><span data-stu-id="145ca-253">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="145ca-254"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="145ca-254"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="145ca-255">(20)</span><span class="sxs-lookup"><span data-stu-id="145ca-255">(20)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-256">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="145ca-256">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="145ca-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="145ca-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="145ca-258">(21)</span><span class="sxs-lookup"><span data-stu-id="145ca-258">(21)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-259">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="145ca-259">System failure.</span></span> <span data-ttu-id="145ca-260">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="145ca-260">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="145ca-261">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="145ca-261">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="145ca-262"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="145ca-262"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="145ca-263">(22)</span><span class="sxs-lookup"><span data-stu-id="145ca-263">(22)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-264">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="145ca-264">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="145ca-265"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="145ca-265"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="145ca-266">(23)</span><span class="sxs-lookup"><span data-stu-id="145ca-266">(23)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-267">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="145ca-267">System failure.</span></span> <span data-ttu-id="145ca-268">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="145ca-268">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="145ca-269"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="145ca-269"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="145ca-270">(24)</span><span class="sxs-lookup"><span data-stu-id="145ca-270">(24)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-271">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="145ca-271">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="145ca-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="145ca-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="145ca-273">(25)</span><span class="sxs-lookup"><span data-stu-id="145ca-273">(25)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-274">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="145ca-274">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="145ca-275"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="145ca-275"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="145ca-276">(26)</span><span class="sxs-lookup"><span data-stu-id="145ca-276">(26)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-277">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="145ca-277">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="145ca-278"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="145ca-278"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="145ca-279">(27)</span><span class="sxs-lookup"><span data-stu-id="145ca-279">(27)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-280">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="145ca-280">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="145ca-281"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="145ca-281"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="145ca-282">(28)</span><span class="sxs-lookup"><span data-stu-id="145ca-282">(28)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-283">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="145ca-283">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="145ca-284"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="145ca-284"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="145ca-285">(29)</span><span class="sxs-lookup"><span data-stu-id="145ca-285">(29)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-286">裝置已停用;裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="145ca-286">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="145ca-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="145ca-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="145ca-288">(30)</span><span class="sxs-lookup"><span data-stu-id="145ca-288">(30)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-289">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="145ca-289">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="145ca-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="145ca-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="145ca-291"> (31) </span><span class="sxs-lookup"><span data-stu-id="145ca-291">(31)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-292">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="145ca-292">Device is not working properly.</span></span> <span data-ttu-id="145ca-293">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="145ca-293">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="145ca-294">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="145ca-294">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145ca-295">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="145ca-295">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="145ca-296">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145ca-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145ca-297">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="145ca-297">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="145ca-298">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="145ca-298">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="145ca-299">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="145ca-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="145ca-300">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="145ca-300">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145ca-301">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="145ca-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="145ca-302">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145ca-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145ca-303">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="145ca-303">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="145ca-304">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="145ca-304">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="145ca-305">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="145ca-305">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="145ca-306">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="145ca-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="145ca-307">**說明**</span><span class="sxs-lookup"><span data-stu-id="145ca-307">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145ca-308">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="145ca-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="145ca-309">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145ca-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145ca-310">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="145ca-310">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="145ca-311">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="145ca-311">Textual description of the object.</span></span>

<span data-ttu-id="145ca-312">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="145ca-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="145ca-313">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="145ca-313">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145ca-314">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="145ca-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="145ca-315">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145ca-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145ca-316">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="145ca-316">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="145ca-317">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="145ca-317">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="145ca-318">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="145ca-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="145ca-319">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="145ca-319">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145ca-320">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="145ca-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="145ca-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145ca-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="145ca-322">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="145ca-322">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="145ca-323">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="145ca-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="145ca-324">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="145ca-324">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145ca-325">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="145ca-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="145ca-326">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145ca-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="145ca-327">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="145ca-327">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="145ca-328">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="145ca-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="145ca-329">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="145ca-329">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145ca-330">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="145ca-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="145ca-331">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145ca-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="145ca-332">描述儲存範圍所支援之錯誤偵測和更正類型的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="145ca-332">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="145ca-333">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="145ca-333">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="145ca-334">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="145ca-334">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145ca-335">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="145ca-335">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="145ca-336">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145ca-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145ca-337">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="145ca-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="145ca-338">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="145ca-338">Date and time the object was installed.</span></span> <span data-ttu-id="145ca-339">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="145ca-339">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="145ca-340">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="145ca-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="145ca-341">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="145ca-341">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145ca-342">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="145ca-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="145ca-343">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145ca-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="145ca-344">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="145ca-344">Last error code reported by the logical device.</span></span>

<span data-ttu-id="145ca-345">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="145ca-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="145ca-346">**名稱**</span><span class="sxs-lookup"><span data-stu-id="145ca-346">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145ca-347">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="145ca-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="145ca-348">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145ca-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145ca-349">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="145ca-349">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="145ca-350">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="145ca-350">Label by which the object is known.</span></span> <span data-ttu-id="145ca-351">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="145ca-351">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="145ca-352">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="145ca-352">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="145ca-353">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="145ca-353">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145ca-354">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="145ca-354">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="145ca-355">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145ca-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145ca-356">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "NumberOfBlocks" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 實體範圍 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="145ca-356">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NumberOfBlocks"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="145ca-357">連續區塊總數，每個區塊會封鎖 **區塊** 屬性中包含的值大小，這會形成此儲存範圍。</span><span class="sxs-lookup"><span data-stu-id="145ca-357">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="145ca-358">您可以將 [ **區塊** ] 屬性的值乘以這個屬性的值，以計算儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="145ca-358">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="145ca-359">如果 **區塊** 的值是1，則這個屬性是儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="145ca-359">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="145ca-360">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="145ca-360">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="145ca-361">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="145ca-361">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="145ca-362">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="145ca-362">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145ca-363">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="145ca-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="145ca-364">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145ca-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145ca-365">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="145ca-365">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="145ca-366">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="145ca-366">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="145ca-367">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="145ca-367">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="145ca-368">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="145ca-368">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="145ca-369">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="145ca-369">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145ca-370">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="145ca-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="145ca-371">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145ca-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="145ca-372">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="145ca-372">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="145ca-373">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="145ca-373">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="145ca-374"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="145ca-374"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="145ca-375"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="145ca-375"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="145ca-376"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="145ca-376"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="145ca-377"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="145ca-377"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-378">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="145ca-378">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="145ca-379"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="145ca-379"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-380">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="145ca-380">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="145ca-381"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="145ca-381"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-382">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="145ca-382">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="145ca-383">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="145ca-383">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="145ca-384">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="145ca-384">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="145ca-385"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="145ca-385"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-386">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="145ca-386">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="145ca-387"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="145ca-387"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="145ca-388">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="145ca-388">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="145ca-389">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="145ca-389">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145ca-390">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="145ca-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="145ca-391">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145ca-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="145ca-392">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="145ca-392">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="145ca-393">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="145ca-393">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="145ca-394">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="145ca-394">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="145ca-395">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="145ca-395">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="145ca-396">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="145ca-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="145ca-397">**目的**</span><span class="sxs-lookup"><span data-stu-id="145ca-397">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145ca-398">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="145ca-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="145ca-399">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145ca-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="145ca-400">描述媒體及其用途的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="145ca-400">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="145ca-401">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="145ca-401">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="145ca-402">**狀態**</span><span class="sxs-lookup"><span data-stu-id="145ca-402">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145ca-403">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="145ca-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="145ca-404">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145ca-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145ca-405">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="145ca-405">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="145ca-406">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="145ca-406">Current status of the object.</span></span>

<span data-ttu-id="145ca-407">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="145ca-407">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="145ca-408">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="145ca-408">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="145ca-409">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="145ca-409">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="145ca-410">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="145ca-410">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="145ca-411">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="145ca-411">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="145ca-412">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="145ca-412">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="145ca-413">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="145ca-413">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="145ca-414">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="145ca-414">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="145ca-415">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="145ca-415">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="145ca-416">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="145ca-416">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="145ca-417">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="145ca-417">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="145ca-418">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="145ca-418">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="145ca-419">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="145ca-419">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="145ca-420">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="145ca-420">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="145ca-421">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="145ca-421">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145ca-422">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="145ca-422">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="145ca-423">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145ca-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145ca-424">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="145ca-424">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="145ca-425">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="145ca-425">State of the logical device.</span></span> <span data-ttu-id="145ca-426">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="145ca-426">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="145ca-427">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="145ca-427">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="145ca-428">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="145ca-428">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="145ca-429">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="145ca-429">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="145ca-430">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="145ca-430">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="145ca-431">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="145ca-431">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="145ca-432">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="145ca-432">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="145ca-433">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="145ca-433">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145ca-434">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="145ca-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="145ca-435">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145ca-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145ca-436">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="145ca-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="145ca-437">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="145ca-437">Scoping system's creation class name.</span></span>

<span data-ttu-id="145ca-438">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="145ca-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="145ca-439">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="145ca-439">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145ca-440">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="145ca-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="145ca-441">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145ca-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145ca-442">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="145ca-442">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="145ca-443">設定系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="145ca-443">Scoping system's name.</span></span>

<span data-ttu-id="145ca-444">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="145ca-444">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="145ca-445">**UnitsBeforeCheckDataInterleave**</span><span class="sxs-lookup"><span data-stu-id="145ca-445">**UnitsBeforeCheckDataInterleave**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145ca-446">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="145ca-446">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="145ca-447">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145ca-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145ca-448">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 實體範圍 \| 001.6 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="145ca-448">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="145ca-449">開始檢查資料交錯之前，要略過的使用者資料位元組數目。</span><span class="sxs-lookup"><span data-stu-id="145ca-449">Number of user data bytes to skip before starting the check-data interleave.</span></span>

<span data-ttu-id="145ca-450">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="145ca-450">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="145ca-451">**UnitsOfCheckData**</span><span class="sxs-lookup"><span data-stu-id="145ca-451">**UnitsOfCheckData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145ca-452">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="145ca-452">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="145ca-453">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145ca-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145ca-454">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 實體範圍 \| 001.7 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="145ca-454">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="145ca-455">要保留給檢查資料的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="145ca-455">Number of bytes to be reserved for check data.</span></span>

<span data-ttu-id="145ca-456">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="145ca-456">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="145ca-457">**UnitsOfUserData**</span><span class="sxs-lookup"><span data-stu-id="145ca-457">**UnitsOfUserData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145ca-458">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="145ca-458">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="145ca-459">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145ca-459">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145ca-460">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 實體範圍 \| 001.8 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="145ca-460">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="145ca-461">要保留給使用者資料的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="145ca-461">Number of bytes to be reserved for user data.</span></span>

<span data-ttu-id="145ca-462">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="145ca-462">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="145ca-463">備註</span><span class="sxs-lookup"><span data-stu-id="145ca-463">Remarks</span></span>

<span data-ttu-id="145ca-464">**Cim \_ PhysicalExtent** 類別衍生自 [**cim \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="145ca-464">The **CIM\_PhysicalExtent** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="145ca-465">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="145ca-465">WMI does not implement this class.</span></span>

<span data-ttu-id="145ca-466">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="145ca-466">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="145ca-467">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="145ca-467">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="145ca-468">規格需求</span><span class="sxs-lookup"><span data-stu-id="145ca-468">Requirements</span></span>



| <span data-ttu-id="145ca-469">需求</span><span class="sxs-lookup"><span data-stu-id="145ca-469">Requirement</span></span> | <span data-ttu-id="145ca-470">值</span><span class="sxs-lookup"><span data-stu-id="145ca-470">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="145ca-471">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="145ca-471">Minimum supported client</span></span><br/> | <span data-ttu-id="145ca-472">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="145ca-472">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="145ca-473">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="145ca-473">Minimum supported server</span></span><br/> | <span data-ttu-id="145ca-474">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="145ca-474">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="145ca-475">命名空間</span><span class="sxs-lookup"><span data-stu-id="145ca-475">Namespace</span></span><br/>                | <span data-ttu-id="145ca-476">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="145ca-476">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="145ca-477">MOF</span><span class="sxs-lookup"><span data-stu-id="145ca-477">MOF</span></span><br/>                      | <dl> <span data-ttu-id="145ca-478"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="145ca-478"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="145ca-479">DLL</span><span class="sxs-lookup"><span data-stu-id="145ca-479">DLL</span></span><br/>                      | <dl> <span data-ttu-id="145ca-480"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="145ca-480"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="145ca-481">另請參閱</span><span class="sxs-lookup"><span data-stu-id="145ca-481">See also</span></span>

<dl> <dt>

[<span data-ttu-id="145ca-482">**CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="145ca-482">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

