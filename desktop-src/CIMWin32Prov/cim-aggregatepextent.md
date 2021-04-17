---
description: CIM \_ AggregatePExtent 類別提供有關可定址邏輯區塊的摘要資訊，這些區塊位於相同的儲存體冗余群組，且位於相同的實體媒體上。
ms.assetid: c8def347-e8d7-48d5-94d0-f6e704e7b40e
ms.tgt_platform: multiple
title: CIM_AggregatePExtent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregatePExtent
- CIM_AggregatePExtent.Caption
- CIM_AggregatePExtent.Description
- CIM_AggregatePExtent.InstallDate
- CIM_AggregatePExtent.Name
- CIM_AggregatePExtent.Status
- CIM_AggregatePExtent.Availability
- CIM_AggregatePExtent.ConfigManagerErrorCode
- CIM_AggregatePExtent.ConfigManagerUserConfig
- CIM_AggregatePExtent.CreationClassName
- CIM_AggregatePExtent.DeviceID
- CIM_AggregatePExtent.PowerManagementCapabilities
- CIM_AggregatePExtent.ErrorCleared
- CIM_AggregatePExtent.ErrorDescription
- CIM_AggregatePExtent.LastErrorCode
- CIM_AggregatePExtent.PNPDeviceID
- CIM_AggregatePExtent.PowerManagementSupported
- CIM_AggregatePExtent.StatusInfo
- CIM_AggregatePExtent.SystemCreationClassName
- CIM_AggregatePExtent.SystemName
- CIM_AggregatePExtent.Access
- CIM_AggregatePExtent.BlockSize
- CIM_AggregatePExtent.ErrorMethodology
- CIM_AggregatePExtent.Purpose
- CIM_AggregatePExtent.NumberOfBlocks
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a2f1b2b5b7e08876317888d02d4830cd72659bc0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510637"
---
# <a name="cim_aggregatepextent-class"></a><span data-ttu-id="0380f-103">CIM \_ AggregatePExtent 類別</span><span class="sxs-lookup"><span data-stu-id="0380f-103">CIM\_AggregatePExtent class</span></span>

<span data-ttu-id="0380f-104">**CIM \_ AggregatePExtent** 類別提供有關可定址邏輯區塊的摘要資訊，這些區塊位於相同的儲存體冗余群組，且位於相同的實體媒體上。</span><span class="sxs-lookup"><span data-stu-id="0380f-104">The **CIM\_AggregatePExtent** class provides summary information about addressable logical blocks, which are in the same storage redundancy group and located on the same physical media.</span></span>

<span data-ttu-id="0380f-105">如果只需要摘要資訊，或使用自動設定，則 **CIM \_ AggregatePExtent** 類別是實體範圍的替代群組。</span><span class="sxs-lookup"><span data-stu-id="0380f-105">The **CIM\_AggregatePExtent** class is an alternative grouping for physical extents when only summary information is needed, or when automatic configuration is used.</span></span> <span data-ttu-id="0380f-106">自動設定可能會導致定義上千個實體範圍。</span><span class="sxs-lookup"><span data-stu-id="0380f-106">Automatic configuration can result in thousands of physical extents being defined.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0380f-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="0380f-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0380f-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="0380f-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0380f-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0380f-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0380f-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="0380f-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0380f-111">語法</span><span class="sxs-lookup"><span data-stu-id="0380f-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{9565979F-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_AggregatePExtent : CIM_StorageExtent
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   Access;
  uint64   BlockSize;
  string   ErrorMethodology;
  string   Purpose;
  uint64   NumberOfBlocks;
};
```

## <a name="members"></a><span data-ttu-id="0380f-112">成員</span><span class="sxs-lookup"><span data-stu-id="0380f-112">Members</span></span>

<span data-ttu-id="0380f-113">**CIM \_ AggregatePExtent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0380f-113">The **CIM\_AggregatePExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="0380f-114">方法</span><span class="sxs-lookup"><span data-stu-id="0380f-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="0380f-115">屬性</span><span class="sxs-lookup"><span data-stu-id="0380f-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0380f-116">方法</span><span class="sxs-lookup"><span data-stu-id="0380f-116">Methods</span></span>

<span data-ttu-id="0380f-117">**CIM \_ AggregatePExtent** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="0380f-117">The **CIM\_AggregatePExtent** class has these methods.</span></span>



| <span data-ttu-id="0380f-118">方法</span><span class="sxs-lookup"><span data-stu-id="0380f-118">Method</span></span>                                                                      | <span data-ttu-id="0380f-119">描述</span><span class="sxs-lookup"><span data-stu-id="0380f-119">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0380f-120">**重設**</span><span class="sxs-lookup"><span data-stu-id="0380f-120">**Reset**</span></span>](reset-method-in-class-cim-aggregatepextent.md)                 | <span data-ttu-id="0380f-121">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="0380f-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="0380f-122">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="0380f-122">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="0380f-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0380f-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-aggregatepextent.md) | <span data-ttu-id="0380f-124">定義邏輯裝置的預期電源狀態，以及裝置何時應進入該狀態。</span><span class="sxs-lookup"><span data-stu-id="0380f-124">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="0380f-125">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="0380f-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0380f-126">屬性</span><span class="sxs-lookup"><span data-stu-id="0380f-126">Properties</span></span>

<span data-ttu-id="0380f-127">**CIM \_ AggregatePExtent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0380f-127">The **CIM\_AggregatePExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0380f-128">**存取**</span><span class="sxs-lookup"><span data-stu-id="0380f-128">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0380f-129">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0380f-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0380f-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0380f-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0380f-131">描述媒體的讀取/寫入屬性。</span><span class="sxs-lookup"><span data-stu-id="0380f-131">Describes the read/write properties of the media.</span></span>

<span data-ttu-id="0380f-132">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="0380f-132">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0380f-133">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="0380f-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="0380f-134">**可讀取** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="0380f-134">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="0380f-135">可 **寫入** (2) </span><span class="sxs-lookup"><span data-stu-id="0380f-135">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="0380f-136">支援 (3) 的 **讀取/寫入**</span><span class="sxs-lookup"><span data-stu-id="0380f-136">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="0380f-137">**撰寫一次** (4) </span><span class="sxs-lookup"><span data-stu-id="0380f-137">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0380f-138">**可用性**</span><span class="sxs-lookup"><span data-stu-id="0380f-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0380f-139">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0380f-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0380f-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0380f-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0380f-141">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="0380f-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="0380f-142">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="0380f-142">Availability and status of the device.</span></span>

<span data-ttu-id="0380f-143">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0380f-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0380f-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="0380f-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0380f-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="0380f-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="0380f-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="0380f-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="0380f-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="0380f-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="0380f-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="0380f-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0380f-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="0380f-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="0380f-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="0380f-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="0380f-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="0380f-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="0380f-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="0380f-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0380f-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="0380f-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="0380f-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="0380f-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="0380f-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="0380f-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="0380f-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="0380f-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="0380f-157">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="0380f-157">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="0380f-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="0380f-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="0380f-159">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="0380f-159">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="0380f-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="0380f-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="0380f-161">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="0380f-161">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="0380f-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="0380f-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="0380f-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="0380f-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="0380f-164">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="0380f-164">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="0380f-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="0380f-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="0380f-166">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="0380f-166">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="0380f-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="0380f-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="0380f-168">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="0380f-168">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="0380f-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="0380f-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="0380f-170">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="0380f-170">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="0380f-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="0380f-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="0380f-172">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="0380f-172">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0380f-173">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="0380f-173">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0380f-174">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="0380f-174">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0380f-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0380f-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0380f-176">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrStorageAllocationUnits ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="0380f-176">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0380f-177">形成儲存範圍之區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="0380f-177">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="0380f-178">如果變數區塊大小，則應該指定最大區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="0380f-178">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="0380f-179">如果區塊大小未知，或區塊概念無效 (例如，針對匯總延伸區、記憶體或邏輯磁片) ，請輸入 1 (一個) 。</span><span class="sxs-lookup"><span data-stu-id="0380f-179">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="0380f-180">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="0380f-180">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="0380f-181">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="0380f-181">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="0380f-182">**標題**</span><span class="sxs-lookup"><span data-stu-id="0380f-182">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0380f-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0380f-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0380f-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0380f-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0380f-185">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="0380f-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0380f-186">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="0380f-186">A short textual description of the object.</span></span>

<span data-ttu-id="0380f-187">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0380f-187">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0380f-188">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0380f-188">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0380f-189">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0380f-189">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0380f-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0380f-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0380f-191">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="0380f-191">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0380f-192">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0380f-192">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="0380f-193">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0380f-193">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="0380f-194">**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="0380f-194">**This device is working properly.**</span></span> <span data-ttu-id="0380f-195"> (0)</span><span class="sxs-lookup"><span data-stu-id="0380f-195">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="0380f-196">**這個裝置並未正確設定。**</span><span class="sxs-lookup"><span data-stu-id="0380f-196">**This device is not configured correctly.**</span></span> <span data-ttu-id="0380f-197">(1)</span><span class="sxs-lookup"><span data-stu-id="0380f-197">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0380f-198">**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="0380f-198">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="0380f-199">(2)</span><span class="sxs-lookup"><span data-stu-id="0380f-199">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="0380f-200">**這個裝置的驅動程式可能已損毀，或您系統的記憶體或其他資源可能不足。**</span><span class="sxs-lookup"><span data-stu-id="0380f-200">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="0380f-201">(3)</span><span class="sxs-lookup"><span data-stu-id="0380f-201">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0380f-202">**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="0380f-202">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="0380f-203">(4)</span><span class="sxs-lookup"><span data-stu-id="0380f-203">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="0380f-204">**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="0380f-204">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="0380f-205">(5)</span><span class="sxs-lookup"><span data-stu-id="0380f-205">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="0380f-206">**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="0380f-206">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="0380f-207">(6)</span><span class="sxs-lookup"><span data-stu-id="0380f-207">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="0380f-208">**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="0380f-208">**Cannot filter.**</span></span> <span data-ttu-id="0380f-209">(7)</span><span class="sxs-lookup"><span data-stu-id="0380f-209">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="0380f-210">**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="0380f-210">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="0380f-211">(8)</span><span class="sxs-lookup"><span data-stu-id="0380f-211">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="0380f-212">**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="0380f-212">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="0380f-213">(9)</span><span class="sxs-lookup"><span data-stu-id="0380f-213">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="0380f-214">**這個裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="0380f-214">**This device cannot start.**</span></span> <span data-ttu-id="0380f-215">(10)</span><span class="sxs-lookup"><span data-stu-id="0380f-215">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="0380f-216">**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="0380f-216">**This device failed.**</span></span> <span data-ttu-id="0380f-217">(11)</span><span class="sxs-lookup"><span data-stu-id="0380f-217">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="0380f-218">**這個裝置沒有足夠資源可供使用。**</span><span class="sxs-lookup"><span data-stu-id="0380f-218">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="0380f-219"> (12) </span><span class="sxs-lookup"><span data-stu-id="0380f-219">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="0380f-220">**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="0380f-220">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="0380f-221">(13)</span><span class="sxs-lookup"><span data-stu-id="0380f-221">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="0380f-222">**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="0380f-222">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="0380f-223">(14)</span><span class="sxs-lookup"><span data-stu-id="0380f-223">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="0380f-224">**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="0380f-224">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="0380f-225">(15)</span><span class="sxs-lookup"><span data-stu-id="0380f-225">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="0380f-226">**Windows 無法識別這個裝置所使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="0380f-226">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="0380f-227">(16)</span><span class="sxs-lookup"><span data-stu-id="0380f-227">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="0380f-228">**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="0380f-228">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="0380f-229">(17)</span><span class="sxs-lookup"><span data-stu-id="0380f-229">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0380f-230">**重新安裝這個裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="0380f-230">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="0380f-231">(18)</span><span class="sxs-lookup"><span data-stu-id="0380f-231">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="0380f-232">**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="0380f-232">**Failure using the VxD loader.**</span></span> <span data-ttu-id="0380f-233">(19)</span><span class="sxs-lookup"><span data-stu-id="0380f-233">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0380f-234">**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="0380f-234">**Your registry might be corrupted.**</span></span> <span data-ttu-id="0380f-235">(20)</span><span class="sxs-lookup"><span data-stu-id="0380f-235">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="0380f-236">**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="0380f-236">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="0380f-237">(21)</span><span class="sxs-lookup"><span data-stu-id="0380f-237">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="0380f-238">**這個裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="0380f-238">**This device is disabled.**</span></span> <span data-ttu-id="0380f-239">(22)</span><span class="sxs-lookup"><span data-stu-id="0380f-239">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="0380f-240">**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="0380f-240">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="0380f-241">(23)</span><span class="sxs-lookup"><span data-stu-id="0380f-241">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="0380f-242">**這個裝置可能不存在、運作不正確、或並未安裝所有的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="0380f-242">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="0380f-243">(24)</span><span class="sxs-lookup"><span data-stu-id="0380f-243">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0380f-244">**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="0380f-244">**Windows is still setting up this device.**</span></span> <span data-ttu-id="0380f-245">(25)</span><span class="sxs-lookup"><span data-stu-id="0380f-245">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0380f-246">**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="0380f-246">**Windows is still setting up this device.**</span></span> <span data-ttu-id="0380f-247">(26)</span><span class="sxs-lookup"><span data-stu-id="0380f-247">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="0380f-248">**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="0380f-248">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="0380f-249">(27)</span><span class="sxs-lookup"><span data-stu-id="0380f-249">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="0380f-250">**這個裝置的驅動程式尚未安裝。**</span><span class="sxs-lookup"><span data-stu-id="0380f-250">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="0380f-251">(28)</span><span class="sxs-lookup"><span data-stu-id="0380f-251">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="0380f-252">**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="0380f-252">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="0380f-253">(29)</span><span class="sxs-lookup"><span data-stu-id="0380f-253">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="0380f-254">**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="0380f-254">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="0380f-255">(30)</span><span class="sxs-lookup"><span data-stu-id="0380f-255">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0380f-256">**這個裝置並未正確執行，因為 Windows 無法載入這個裝置必需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="0380f-256">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="0380f-257"> (31) </span><span class="sxs-lookup"><span data-stu-id="0380f-257">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0380f-258">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="0380f-258">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0380f-259">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0380f-259">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0380f-260">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0380f-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0380f-261">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="0380f-261">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0380f-262">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="0380f-262">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="0380f-263">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0380f-263">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0380f-264">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0380f-264">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0380f-265">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0380f-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0380f-266">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0380f-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0380f-267">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0380f-267">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0380f-268">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="0380f-268">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="0380f-269">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="0380f-269">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="0380f-270">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0380f-270">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0380f-271">**說明**</span><span class="sxs-lookup"><span data-stu-id="0380f-271">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0380f-272">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0380f-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0380f-273">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0380f-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0380f-274">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="0380f-274">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0380f-275">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="0380f-275">A textual description of the object.</span></span>

<span data-ttu-id="0380f-276">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0380f-276">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0380f-277">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0380f-277">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0380f-278">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0380f-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0380f-279">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0380f-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0380f-280">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0380f-280">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0380f-281">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="0380f-281">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="0380f-282">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0380f-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0380f-283">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="0380f-283">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0380f-284">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0380f-284">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0380f-285">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0380f-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0380f-286">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="0380f-286">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="0380f-287">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0380f-287">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0380f-288">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0380f-288">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0380f-289">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0380f-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0380f-290">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0380f-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0380f-291">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="0380f-291">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="0380f-292">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0380f-292">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0380f-293">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="0380f-293">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0380f-294">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0380f-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0380f-295">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0380f-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0380f-296">描述儲存範圍所支援之錯誤偵測和更正類型的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="0380f-296">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="0380f-297">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="0380f-297">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="0380f-298">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0380f-298">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0380f-299">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="0380f-299">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0380f-300">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0380f-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0380f-301">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="0380f-301">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0380f-302">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="0380f-302">Indicates when the object was installed.</span></span> <span data-ttu-id="0380f-303">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="0380f-303">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0380f-304">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0380f-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0380f-305">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0380f-305">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0380f-306">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0380f-306">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0380f-307">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0380f-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0380f-308">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0380f-308">Last error code reported by the logical device.</span></span>

<span data-ttu-id="0380f-309">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0380f-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0380f-310">**名稱**</span><span class="sxs-lookup"><span data-stu-id="0380f-310">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0380f-311">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0380f-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0380f-312">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0380f-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0380f-313">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="0380f-313">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0380f-314">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="0380f-314">Label by which the object is known.</span></span> <span data-ttu-id="0380f-315">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="0380f-315">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="0380f-316">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0380f-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0380f-317">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="0380f-317">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0380f-318">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="0380f-318">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0380f-319">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0380f-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0380f-320">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "NumberOfBlocks" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 匯總實體範圍 \| 001.2 ") </span><span class="sxs-lookup"><span data-stu-id="0380f-320">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NumberOfBlocks"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Aggregate Physical Extent\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="0380f-321">區塊總數 (包含此匯總實體範圍內) 的檢查資料區塊。</span><span class="sxs-lookup"><span data-stu-id="0380f-321">Total number of blocks (including the check data blocks) contained in this aggregate physical extent.</span></span> <span data-ttu-id="0380f-322">區塊大小 (繼承的屬性) 應該設定為與此範圍相關聯之媒體存取裝置的相同值。</span><span class="sxs-lookup"><span data-stu-id="0380f-322">The block size (an inherited property) should be set to the same value as for the media access device associated with this extent.</span></span>

</dd> <dt>

<span data-ttu-id="0380f-323">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="0380f-323">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0380f-324">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0380f-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0380f-325">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0380f-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0380f-326">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="0380f-326">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0380f-327">指出邏輯裝置的 Win32 隨插即用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="0380f-327">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="0380f-328">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="0380f-328">Example: "\*PNP030b"</span></span>

<span data-ttu-id="0380f-329">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0380f-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0380f-330">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0380f-330">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0380f-331">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="0380f-331">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0380f-332">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0380f-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0380f-333">指出邏輯裝置的特定電源相關功能。</span><span class="sxs-lookup"><span data-stu-id="0380f-333">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="0380f-334">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0380f-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0380f-335"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="0380f-335"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0380f-336">電源相關的容量未知。</span><span class="sxs-lookup"><span data-stu-id="0380f-336">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="0380f-337"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="0380f-337"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0380f-338">此裝置不支援與電源相關的容量。</span><span class="sxs-lookup"><span data-stu-id="0380f-338">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0380f-339"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="0380f-339"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0380f-340">電源相關容量已停用。</span><span class="sxs-lookup"><span data-stu-id="0380f-340">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0380f-341"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="0380f-341"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0380f-342">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="0380f-342">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="0380f-343"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="0380f-343"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0380f-344">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="0380f-344">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="0380f-345"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="0380f-345"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0380f-346">支援 **SetPowerState** 方法。</span><span class="sxs-lookup"><span data-stu-id="0380f-346">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="0380f-347">這個方法可在父 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="0380f-347">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="0380f-348">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="0380f-348">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="0380f-349"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="0380f-349"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0380f-350">您可以叫用 **SetPowerState** 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) 。</span><span class="sxs-lookup"><span data-stu-id="0380f-350">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="0380f-351"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="0380f-351"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0380f-352">您可以叫用 **SetPowerState** 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) ，並將 *時間* 參數設定為特定日期和時間（或間隔），以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="0380f-352">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0380f-353">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="0380f-353">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0380f-354">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0380f-354">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0380f-355">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0380f-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0380f-356">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="0380f-356">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="0380f-357">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="0380f-357">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="0380f-358">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="0380f-358">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="0380f-359">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="0380f-359">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="0380f-360">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0380f-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0380f-361">**目的**</span><span class="sxs-lookup"><span data-stu-id="0380f-361">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0380f-362">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0380f-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0380f-363">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0380f-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0380f-364">描述媒體及其用途的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="0380f-364">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="0380f-365">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="0380f-365">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="0380f-366">**狀態**</span><span class="sxs-lookup"><span data-stu-id="0380f-366">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0380f-367">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0380f-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0380f-368">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0380f-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0380f-369">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="0380f-369">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0380f-370">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="0380f-370">String that indicates the current status of the object.</span></span> <span data-ttu-id="0380f-371">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="0380f-371">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="0380f-372">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="0380f-372">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="0380f-373">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="0380f-373">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="0380f-374">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="0380f-374">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0380f-375">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="0380f-375">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0380f-376">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="0380f-376">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0380f-377">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0380f-377">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0380f-378">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="0380f-378">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0380f-379">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="0380f-379">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0380f-380">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="0380f-380">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0380f-381">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="0380f-381">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0380f-382">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="0380f-382">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0380f-383">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="0380f-383">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0380f-384">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="0380f-384">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0380f-385">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="0380f-385">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0380f-386">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="0380f-386">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0380f-387">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="0380f-387">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0380f-388">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="0380f-388">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0380f-389">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="0380f-389">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0380f-390">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="0380f-390">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0380f-391">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="0380f-391">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0380f-392">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0380f-392">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0380f-393">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0380f-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0380f-394">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="0380f-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="0380f-395">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="0380f-395">State of the logical device.</span></span> <span data-ttu-id="0380f-396">如果此屬性不適用於邏輯裝置，則應該使用值 5 ( 「不適用」 ) 。</span><span class="sxs-lookup"><span data-stu-id="0380f-396">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="0380f-397">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0380f-397">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0380f-398">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="0380f-398">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0380f-399">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="0380f-399">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0380f-400">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="0380f-400">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0380f-401">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="0380f-401">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0380f-402">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="0380f-402">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0380f-403">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0380f-403">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0380f-404">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0380f-404">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0380f-405">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0380f-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0380f-406">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0380f-406">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0380f-407">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="0380f-407">The scoping system's creation class name.</span></span>

<span data-ttu-id="0380f-408">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0380f-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0380f-409">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0380f-409">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0380f-410">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0380f-410">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0380f-411">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0380f-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0380f-412">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0380f-412">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0380f-413">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="0380f-413">The scoping system's name.</span></span>

<span data-ttu-id="0380f-414">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0380f-414">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0380f-415">備註</span><span class="sxs-lookup"><span data-stu-id="0380f-415">Remarks</span></span>

<span data-ttu-id="0380f-416">**Cim \_ AggregatePExtent** 類別衍生自 [**cim \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="0380f-416">The **CIM\_AggregatePExtent** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="0380f-417">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="0380f-417">WMI does not implement this class.</span></span>

<span data-ttu-id="0380f-418">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="0380f-418">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0380f-419">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="0380f-419">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0380f-420">規格需求</span><span class="sxs-lookup"><span data-stu-id="0380f-420">Requirements</span></span>



| <span data-ttu-id="0380f-421">需求</span><span class="sxs-lookup"><span data-stu-id="0380f-421">Requirement</span></span> | <span data-ttu-id="0380f-422">值</span><span class="sxs-lookup"><span data-stu-id="0380f-422">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0380f-423">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0380f-423">Minimum supported client</span></span><br/> | <span data-ttu-id="0380f-424">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0380f-424">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0380f-425">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0380f-425">Minimum supported server</span></span><br/> | <span data-ttu-id="0380f-426">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0380f-426">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0380f-427">命名空間</span><span class="sxs-lookup"><span data-stu-id="0380f-427">Namespace</span></span><br/>                | <span data-ttu-id="0380f-428">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0380f-428">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0380f-429">MOF</span><span class="sxs-lookup"><span data-stu-id="0380f-429">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0380f-430"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="0380f-430"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0380f-431">DLL</span><span class="sxs-lookup"><span data-stu-id="0380f-431">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0380f-432"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0380f-432"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0380f-433">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0380f-433">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0380f-434">**CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="0380f-434">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> <dt>

[<span data-ttu-id="0380f-435">CIM 類別</span><span class="sxs-lookup"><span data-stu-id="0380f-435">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

