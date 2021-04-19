---
description: CIM \_ UninterruptiblePowerSupply 類別代表 (UPS) 的不斷電供應系統供應器的功能和管理。
ms.assetid: 27ddc955-906b-40b9-981b-96872356477c
ms.tgt_platform: multiple
title: CIM_UninterruptiblePowerSupply 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UninterruptiblePowerSupply
- CIM_UninterruptiblePowerSupply.ActiveInputVoltage
- CIM_UninterruptiblePowerSupply.Availability
- CIM_UninterruptiblePowerSupply.Caption
- CIM_UninterruptiblePowerSupply.ConfigManagerErrorCode
- CIM_UninterruptiblePowerSupply.ConfigManagerUserConfig
- CIM_UninterruptiblePowerSupply.CreationClassName
- CIM_UninterruptiblePowerSupply.Description
- CIM_UninterruptiblePowerSupply.DeviceID
- CIM_UninterruptiblePowerSupply.ErrorCleared
- CIM_UninterruptiblePowerSupply.ErrorDescription
- CIM_UninterruptiblePowerSupply.EstimatedChargeRemaining
- CIM_UninterruptiblePowerSupply.EstimatedRunTime
- CIM_UninterruptiblePowerSupply.InstallDate
- CIM_UninterruptiblePowerSupply.IsSwitchingSupply
- CIM_UninterruptiblePowerSupply.LastErrorCode
- CIM_UninterruptiblePowerSupply.Name
- CIM_UninterruptiblePowerSupply.PNPDeviceID
- CIM_UninterruptiblePowerSupply.PowerManagementCapabilities
- CIM_UninterruptiblePowerSupply.PowerManagementSupported
- CIM_UninterruptiblePowerSupply.Range1InputFrequencyHigh
- CIM_UninterruptiblePowerSupply.Range1InputFrequencyLow
- CIM_UninterruptiblePowerSupply.Range1InputVoltageHigh
- CIM_UninterruptiblePowerSupply.Range1InputVoltageLow
- CIM_UninterruptiblePowerSupply.Range2InputFrequencyHigh
- CIM_UninterruptiblePowerSupply.Range2InputFrequencyLow
- CIM_UninterruptiblePowerSupply.Range2InputVoltageHigh
- CIM_UninterruptiblePowerSupply.Range2InputVoltageLow
- CIM_UninterruptiblePowerSupply.RemainingCapacityStatus
- CIM_UninterruptiblePowerSupply.Status
- CIM_UninterruptiblePowerSupply.StatusInfo
- CIM_UninterruptiblePowerSupply.SystemCreationClassName
- CIM_UninterruptiblePowerSupply.SystemName
- CIM_UninterruptiblePowerSupply.TimeOnBackup
- CIM_UninterruptiblePowerSupply.TotalOutputPower
- CIM_UninterruptiblePowerSupply.TypeOfRangeSwitching
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 214517fd6518cf2ca406523c61f522ae9c1adc46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970710"
---
# <a name="cim_uninterruptiblepowersupply-class"></a><span data-ttu-id="e2f95-103">CIM \_ UninterruptiblePowerSupply 類別</span><span class="sxs-lookup"><span data-stu-id="e2f95-103">CIM\_UninterruptiblePowerSupply class</span></span>

<span data-ttu-id="e2f95-104">**CIM \_ UninterruptiblePowerSupply** 類別代表 (UPS) 的不斷電供應系統供應器的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="e2f95-104">The **CIM\_UninterruptiblePowerSupply** class represents the capabilities and management of an uninterruptible power supply (UPS).</span></span> <span data-ttu-id="e2f95-105">UPS 裝置的內容會指出何時修剪或提升傳入電源，以及組成裝置的電池、產生器等的匯總資訊。</span><span class="sxs-lookup"><span data-stu-id="e2f95-105">The properties of the UPS device indicate when incoming power is trimmed or boosted, and the aggregated information of the batteries, generators, and so on, that make up the device.</span></span> <span data-ttu-id="e2f95-106">個別元件 (例如，多個電池) 也可以獨立建立模型並與 UPS 相關聯。</span><span class="sxs-lookup"><span data-stu-id="e2f95-106">The individual components (for example, multiple batteries) can also be independently modeled and associated with the UPS.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e2f95-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="e2f95-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e2f95-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e2f95-109">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e2f95-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e2f95-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="e2f95-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2f95-111">語法</span><span class="sxs-lookup"><span data-stu-id="e2f95-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C54F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_UninterruptiblePowerSupply : CIM_PowerSupply
{
  uint16   ActiveInputVoltage;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   EstimatedChargeRemaining;
  uint32   EstimatedRunTime;
  datetime InstallDate;
  boolean  IsSwitchingSupply;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   Range1InputFrequencyHigh;
  uint32   Range1InputFrequencyLow;
  uint32   Range1InputVoltageHigh;
  uint32   Range1InputVoltageLow;
  uint32   Range2InputFrequencyHigh;
  uint32   Range2InputFrequencyLow;
  uint32   Range2InputVoltageHigh;
  uint32   Range2InputVoltageLow;
  uint16   RemainingCapacityStatus;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TimeOnBackup;
  uint32   TotalOutputPower;
  uint16   TypeOfRangeSwitching;
};
```

## <a name="members"></a><span data-ttu-id="e2f95-112">成員</span><span class="sxs-lookup"><span data-stu-id="e2f95-112">Members</span></span>

<span data-ttu-id="e2f95-113">**CIM \_ UninterruptiblePowerSupply** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e2f95-113">The **CIM\_UninterruptiblePowerSupply** class has these types of members:</span></span>

-   [<span data-ttu-id="e2f95-114">方法</span><span class="sxs-lookup"><span data-stu-id="e2f95-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="e2f95-115">屬性</span><span class="sxs-lookup"><span data-stu-id="e2f95-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e2f95-116">方法</span><span class="sxs-lookup"><span data-stu-id="e2f95-116">Methods</span></span>

<span data-ttu-id="e2f95-117">**CIM \_ UninterruptiblePowerSupply** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e2f95-117">The **CIM\_UninterruptiblePowerSupply** class has these methods.</span></span>



| <span data-ttu-id="e2f95-118">方法</span><span class="sxs-lookup"><span data-stu-id="e2f95-118">Method</span></span>                                                                                | <span data-ttu-id="e2f95-119">描述</span><span class="sxs-lookup"><span data-stu-id="e2f95-119">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2f95-120">**重設**</span><span class="sxs-lookup"><span data-stu-id="e2f95-120">**Reset**</span></span>](reset-method-in-class-cim-uninterruptiblepowersupply.md)                 | <span data-ttu-id="e2f95-121">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="e2f95-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="e2f95-122">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="e2f95-122">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="e2f95-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="e2f95-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-uninterruptiblepowersupply.md) | <span data-ttu-id="e2f95-124">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="e2f95-124">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="e2f95-125">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="e2f95-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e2f95-126">屬性</span><span class="sxs-lookup"><span data-stu-id="e2f95-126">Properties</span></span>

<span data-ttu-id="e2f95-127">**CIM \_ UninterruptiblePowerSupply** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e2f95-127">The **CIM\_UninterruptiblePowerSupply** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2f95-128">**ActiveInputVoltage**</span><span class="sxs-lookup"><span data-stu-id="e2f95-128">**ActiveInputVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-129">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e2f95-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-131">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電源供應器 \| 002.15」 ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.15")</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-132">輸入電壓範圍目前正在使用中。</span><span class="sxs-lookup"><span data-stu-id="e2f95-132">Input voltage range is currently in use.</span></span> <span data-ttu-id="e2f95-133">如果供應目前未繪製電源，則可以指定值 6 ( 「不會」 ) 。</span><span class="sxs-lookup"><span data-stu-id="e2f95-133">If the supply is not currently drawing power, the value 6 ("Neither") can be specified.</span></span> <span data-ttu-id="e2f95-134">這項資訊在 UPS （ [**CIM \_ 電源**](cim-powersupply.md)的子類別）的情況下是必要的。</span><span class="sxs-lookup"><span data-stu-id="e2f95-134">This information is necessary in the case of a UPS, a subclass of [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

<span data-ttu-id="e2f95-135">這個屬性繼承自 [**CIM \_ 電源電源**](cim-powersupply.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-135">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e2f95-136">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="e2f95-136">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e2f95-137">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="e2f95-137">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span data-ttu-id="e2f95-138">**範圍 1** (3) </span><span class="sxs-lookup"><span data-stu-id="e2f95-138">**Range 1** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span data-ttu-id="e2f95-139">**範圍 2** (4) </span><span class="sxs-lookup"><span data-stu-id="e2f95-139">**Range 2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="e2f95-140">**(5**) </span><span class="sxs-lookup"><span data-stu-id="e2f95-140">**Both** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Neither"></span><span id="neither"></span><span id="NEITHER"></span>

<span data-ttu-id="e2f95-141">**不** (6) </span><span class="sxs-lookup"><span data-stu-id="e2f95-141">**Neither** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e2f95-142">**可用性**</span><span class="sxs-lookup"><span data-stu-id="e2f95-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-143">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e2f95-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-145">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="e2f95-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-146">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="e2f95-146">Availability and status of the device.</span></span>

<span data-ttu-id="e2f95-147">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-147">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e2f95-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="e2f95-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e2f95-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="e2f95-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="e2f95-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="e2f95-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-151">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="e2f95-151">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="e2f95-152"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="e2f95-152"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="e2f95-153"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="e2f95-153"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e2f95-154"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="e2f95-154"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="e2f95-155"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="e2f95-155"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="e2f95-156"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="e2f95-156"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="e2f95-157"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="e2f95-157"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e2f95-158"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="e2f95-158"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="e2f95-159"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="e2f95-159"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="e2f95-160"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="e2f95-160"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="e2f95-161"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="e2f95-161"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-162">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="e2f95-162">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="e2f95-163"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="e2f95-163"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-164">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="e2f95-164">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="e2f95-165"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="e2f95-165"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-166">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="e2f95-166">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="e2f95-167"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="e2f95-167"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="e2f95-168"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="e2f95-168"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-169">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="e2f95-169">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="e2f95-170"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="e2f95-170"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-171">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="e2f95-171">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="e2f95-172"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="e2f95-172"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-173">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="e2f95-173">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="e2f95-174"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="e2f95-174"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-175">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="e2f95-175">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="e2f95-176"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="e2f95-176"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-177">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="e2f95-177">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e2f95-178">**標題**</span><span class="sxs-lookup"><span data-stu-id="e2f95-178">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-179">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2f95-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-181">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-182">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="e2f95-182">Short textual description of the object.</span></span>

<span data-ttu-id="e2f95-183">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-183">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-184">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e2f95-184">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-185">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e2f95-185">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-187">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-187">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-188">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e2f95-188">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="e2f95-189">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-189">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="e2f95-190"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-190"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="e2f95-191"> (0)</span><span class="sxs-lookup"><span data-stu-id="e2f95-191">(0)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-192">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="e2f95-192">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="e2f95-193"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-193"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="e2f95-194">(1)</span><span class="sxs-lookup"><span data-stu-id="e2f95-194">(1)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-195">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="e2f95-195">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e2f95-196"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-196"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="e2f95-197">(2)</span><span class="sxs-lookup"><span data-stu-id="e2f95-197">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="e2f95-198"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-198"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="e2f95-199">(3)</span><span class="sxs-lookup"><span data-stu-id="e2f95-199">(3)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-200">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="e2f95-200">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e2f95-201"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-201"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="e2f95-202">(4)</span><span class="sxs-lookup"><span data-stu-id="e2f95-202">(4)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-203">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="e2f95-203">Device is not working properly.</span></span> <span data-ttu-id="e2f95-204">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="e2f95-204">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="e2f95-205"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-205"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="e2f95-206">(5)</span><span class="sxs-lookup"><span data-stu-id="e2f95-206">(5)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-207">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="e2f95-207">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="e2f95-208"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-208"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="e2f95-209">(6)</span><span class="sxs-lookup"><span data-stu-id="e2f95-209">(6)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-210">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="e2f95-210">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="e2f95-211"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-211"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="e2f95-212">(7)</span><span class="sxs-lookup"><span data-stu-id="e2f95-212">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="e2f95-213"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-213"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="e2f95-214">(8)</span><span class="sxs-lookup"><span data-stu-id="e2f95-214">(8)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-215">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="e2f95-215">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="e2f95-216"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-216"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="e2f95-217">(9)</span><span class="sxs-lookup"><span data-stu-id="e2f95-217">(9)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-218">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="e2f95-218">Device is not working properly.</span></span> <span data-ttu-id="e2f95-219">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="e2f95-219">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="e2f95-220"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-220"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="e2f95-221">(10)</span><span class="sxs-lookup"><span data-stu-id="e2f95-221">(10)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-222">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="e2f95-222">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="e2f95-223"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-223"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="e2f95-224">(11)</span><span class="sxs-lookup"><span data-stu-id="e2f95-224">(11)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-225">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="e2f95-225">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="e2f95-226"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-226"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="e2f95-227"> (12) </span><span class="sxs-lookup"><span data-stu-id="e2f95-227">(12)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-228">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="e2f95-228">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="e2f95-229"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-229"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="e2f95-230">(13)</span><span class="sxs-lookup"><span data-stu-id="e2f95-230">(13)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-231">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="e2f95-231">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="e2f95-232"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-232"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="e2f95-233">(14)</span><span class="sxs-lookup"><span data-stu-id="e2f95-233">(14)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-234">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="e2f95-234">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="e2f95-235"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-235"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="e2f95-236">(15)</span><span class="sxs-lookup"><span data-stu-id="e2f95-236">(15)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-237">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="e2f95-237">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="e2f95-238"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-238"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="e2f95-239">(16)</span><span class="sxs-lookup"><span data-stu-id="e2f95-239">(16)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-240">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="e2f95-240">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="e2f95-241"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-241"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="e2f95-242">(17)</span><span class="sxs-lookup"><span data-stu-id="e2f95-242">(17)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-243">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="e2f95-243">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e2f95-244"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-244"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="e2f95-245">(18)</span><span class="sxs-lookup"><span data-stu-id="e2f95-245">(18)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-246">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="e2f95-246">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="e2f95-247"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-247"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="e2f95-248">(19)</span><span class="sxs-lookup"><span data-stu-id="e2f95-248">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e2f95-249"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-249"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="e2f95-250">(20)</span><span class="sxs-lookup"><span data-stu-id="e2f95-250">(20)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-251">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="e2f95-251">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="e2f95-252"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-252"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="e2f95-253">(21)</span><span class="sxs-lookup"><span data-stu-id="e2f95-253">(21)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-254">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="e2f95-254">System failure.</span></span> <span data-ttu-id="e2f95-255">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="e2f95-255">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="e2f95-256">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="e2f95-256">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="e2f95-257"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-257"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="e2f95-258">(22)</span><span class="sxs-lookup"><span data-stu-id="e2f95-258">(22)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-259">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="e2f95-259">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="e2f95-260"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-260"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="e2f95-261">(23)</span><span class="sxs-lookup"><span data-stu-id="e2f95-261">(23)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-262">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="e2f95-262">System failure.</span></span> <span data-ttu-id="e2f95-263">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="e2f95-263">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="e2f95-264"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-264"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="e2f95-265">(24)</span><span class="sxs-lookup"><span data-stu-id="e2f95-265">(24)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-266">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="e2f95-266">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e2f95-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e2f95-268">(25)</span><span class="sxs-lookup"><span data-stu-id="e2f95-268">(25)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-269">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="e2f95-269">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e2f95-270"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-270"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e2f95-271">(26)</span><span class="sxs-lookup"><span data-stu-id="e2f95-271">(26)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-272">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="e2f95-272">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="e2f95-273"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-273"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="e2f95-274">(27)</span><span class="sxs-lookup"><span data-stu-id="e2f95-274">(27)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-275">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="e2f95-275">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="e2f95-276"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-276"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="e2f95-277">(28)</span><span class="sxs-lookup"><span data-stu-id="e2f95-277">(28)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-278">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="e2f95-278">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="e2f95-279"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-279"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="e2f95-280">(29)</span><span class="sxs-lookup"><span data-stu-id="e2f95-280">(29)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-281">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="e2f95-281">Device is disabled.</span></span> <span data-ttu-id="e2f95-282">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="e2f95-282">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="e2f95-283"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-283"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="e2f95-284">(30)</span><span class="sxs-lookup"><span data-stu-id="e2f95-284">(30)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-285">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="e2f95-285">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e2f95-286"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="e2f95-286"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="e2f95-287"> (31) </span><span class="sxs-lookup"><span data-stu-id="e2f95-287">(31)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-288">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="e2f95-288">Device is not working properly.</span></span> <span data-ttu-id="e2f95-289">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="e2f95-289">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e2f95-290">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="e2f95-290">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-291">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e2f95-291">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-292">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-293">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-293">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-294">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="e2f95-294">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="e2f95-295">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-295">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-296">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e2f95-296">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-297">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2f95-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-298">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-299">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e2f95-299">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-300">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2f95-300">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e2f95-301">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="e2f95-301">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="e2f95-302">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-302">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-303">**說明**</span><span class="sxs-lookup"><span data-stu-id="e2f95-303">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-304">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2f95-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-305">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-306">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-307">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="e2f95-307">Textual description of the object.</span></span>

<span data-ttu-id="e2f95-308">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-308">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-309">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="e2f95-309">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-310">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2f95-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-311">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-312">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e2f95-312">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-313">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="e2f95-313">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="e2f95-314">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-314">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-315">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="e2f95-315">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-316">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e2f95-316">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-317">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-318">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="e2f95-318">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="e2f95-319">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-320">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e2f95-320">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-321">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2f95-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-322">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-323">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="e2f95-323">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="e2f95-324">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-325">**EstimatedChargeRemaining**</span><span class="sxs-lookup"><span data-stu-id="e2f95-325">**EstimatedChargeRemaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-326">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e2f95-326">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-327">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-328">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| UPS 電池 \| 001.4」 ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「百分比」 ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-328">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|UPS Battery\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-329">使用電池技術的 UPS 剩餘的完整費用百分比估計。</span><span class="sxs-lookup"><span data-stu-id="e2f95-329">Percentage estimate of the remaining full charge for a UPS that uses battery technology.</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-330">**EstimatedRunTime**</span><span class="sxs-lookup"><span data-stu-id="e2f95-330">**EstimatedRunTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-331">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e2f95-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-332">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-333">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| UPS 電池 \| 001.3 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 分鐘 ") </span><span class="sxs-lookup"><span data-stu-id="e2f95-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|UPS Battery\|001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-334">估計的時間（以分鐘為單位），在目前的負載狀況下，如果公用程式電源關閉或遺失並保持關閉，則會在目前的負載狀況下耗盡電池、產生器或其他電源。</span><span class="sxs-lookup"><span data-stu-id="e2f95-334">Estimated time, in minutes, until the battery, generator, or other power source is depleted under the present load conditions if the utility power is off, or is lost and remains off.</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-335">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e2f95-335">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-336">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="e2f95-336">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-337">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-338">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="e2f95-338">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-339">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="e2f95-339">Date and time the object was installed.</span></span> <span data-ttu-id="e2f95-340">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="e2f95-340">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="e2f95-341">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-341">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-342">**IsSwitchingSupply**</span><span class="sxs-lookup"><span data-stu-id="e2f95-342">**IsSwitchingSupply**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-343">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e2f95-343">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-344">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-345">若 **為 TRUE**，則表示電源供應器 (切換，而非線性) 供應。</span><span class="sxs-lookup"><span data-stu-id="e2f95-345">If **TRUE**, the power supply is a switching (rather than linear) supply.</span></span>

<span data-ttu-id="e2f95-346">這個屬性繼承自 [**CIM \_ 電源電源**](cim-powersupply.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-346">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-347">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e2f95-347">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-348">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e2f95-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-349">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-350">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e2f95-350">Last error code reported by the logical device.</span></span>

<span data-ttu-id="e2f95-351">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-351">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-352">**名稱**</span><span class="sxs-lookup"><span data-stu-id="e2f95-352">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-353">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2f95-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-354">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-355">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-355">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-356">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="e2f95-356">Label by which the object is known.</span></span> <span data-ttu-id="e2f95-357">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="e2f95-357">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="e2f95-358">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-358">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-359">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="e2f95-359">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-360">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2f95-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-361">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-362">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-362">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-363">邏輯裝置的 Win32 隨插即用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="e2f95-363">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="e2f95-364">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="e2f95-365">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="e2f95-365">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-366">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e2f95-366">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-367">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="e2f95-367">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-368">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-369">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="e2f95-369">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="e2f95-370">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="e2f95-370">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e2f95-371"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="e2f95-371"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="e2f95-372"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="e2f95-372"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e2f95-373"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="e2f95-373"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e2f95-374"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="e2f95-374"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-375">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="e2f95-375">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="e2f95-376"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="e2f95-376"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-377">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="e2f95-377">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="e2f95-378"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="e2f95-378"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-379">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="e2f95-379">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="e2f95-380">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="e2f95-380">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="e2f95-381">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-381">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="e2f95-382"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="e2f95-382"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-383">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="e2f95-383">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="e2f95-384"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="e2f95-384"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-385">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="e2f95-385">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e2f95-386">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="e2f95-386">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-387">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e2f95-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-388">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-389">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="e2f95-389">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="e2f95-390">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="e2f95-390">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="e2f95-391">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="e2f95-391">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="e2f95-392">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="e2f95-392">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="e2f95-393">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-393">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-394">**Range1InputFrequencyHigh**</span><span class="sxs-lookup"><span data-stu-id="e2f95-394">**Range1InputFrequencyHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-395">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e2f95-395">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-396">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-397">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "赫茲" ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-397">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-398">電源供應器輸入頻率範圍1的高階頻率（以赫茲為單位）。</span><span class="sxs-lookup"><span data-stu-id="e2f95-398">Frequency, in hertz, at the high-end of the power supply's input frequency range 1.</span></span> <span data-ttu-id="e2f95-399">值為 0 (零) 表示 DC。</span><span class="sxs-lookup"><span data-stu-id="e2f95-399">A value of 0 (zero) implies DC.</span></span>

<span data-ttu-id="e2f95-400">這個屬性繼承自 [**CIM \_ 電源電源**](cim-powersupply.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-400">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-401">**Range1InputFrequencyLow**</span><span class="sxs-lookup"><span data-stu-id="e2f95-401">**Range1InputFrequencyLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-402">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e2f95-402">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-403">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-404">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電源供應器 \| 002.17 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 赫茲 ") </span><span class="sxs-lookup"><span data-stu-id="e2f95-404">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-405">電源供應器輸入頻率範圍1的低端頻率（以赫茲為單位）。</span><span class="sxs-lookup"><span data-stu-id="e2f95-405">Frequency, in hertz, at the low-end of the power supply's input frequency range 1.</span></span> <span data-ttu-id="e2f95-406">值為 0 (零) 表示 DC。</span><span class="sxs-lookup"><span data-stu-id="e2f95-406">A value of 0 (zero) implies DC.</span></span>

<span data-ttu-id="e2f95-407">這個屬性繼承自 [**CIM \_ 電源電源**](cim-powersupply.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-407">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-408">**Range1InputVoltageHigh**</span><span class="sxs-lookup"><span data-stu-id="e2f95-408">**Range1InputVoltageHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-409">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e2f95-409">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-410">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-411">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Range1InputVoltageHigh" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫伏" ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-411">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range1InputVoltageHigh"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-412">如果電壓（以毫伏為單位）高於 **Range1InputVoltageHigh** 屬性所指定的值，則會藉由修剪電壓來彌補 UPS。</span><span class="sxs-lookup"><span data-stu-id="e2f95-412">If the voltage, in millivolts, rises above the value specified by the **Range1InputVoltageHigh** property, the UPS will compensate by trimming the voltage.</span></span> <span data-ttu-id="e2f95-413">值為 0 (零) 表示發生修剪的電壓未知。</span><span class="sxs-lookup"><span data-stu-id="e2f95-413">A value of 0 (zero) indicates that the voltage at which trimming occurs is unknown.</span></span>

<span data-ttu-id="e2f95-414">這個屬性繼承自 [**CIM \_ 電源電源**](cim-powersupply.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-414">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-415">**Range1InputVoltageLow**</span><span class="sxs-lookup"><span data-stu-id="e2f95-415">**Range1InputVoltageLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-416">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e2f95-416">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-417">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-418">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Range1InputVoltageLow" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫伏" ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-418">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range1InputVoltageLow"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-419">如果電壓（以毫伏為單位）低於 **Range1InputVoltageLow** 屬性指定的值，則會使用其電源線來提高電壓來彌補 UPS。</span><span class="sxs-lookup"><span data-stu-id="e2f95-419">If the voltage, in millivolts, drops below the value specified by the **Range1InputVoltageLow** property, the UPS will compensate by boosting the voltage using its power sources.</span></span> <span data-ttu-id="e2f95-420">值為0表示發生提升的電壓為未知。</span><span class="sxs-lookup"><span data-stu-id="e2f95-420">A value of 0 indicates that the voltage at which boosting occurs is unknown.</span></span>

<span data-ttu-id="e2f95-421">這個屬性繼承自 [**CIM \_ 電源電源**](cim-powersupply.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-421">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-422">**Range2InputFrequencyHigh**</span><span class="sxs-lookup"><span data-stu-id="e2f95-422">**Range2InputFrequencyHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-423">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e2f95-423">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-424">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-425">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電源供應器 \| 002.20 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 赫茲 ") </span><span class="sxs-lookup"><span data-stu-id="e2f95-425">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.20"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-426">電源供應器輸入頻率範圍2的高階頻率（以赫茲為單位）。</span><span class="sxs-lookup"><span data-stu-id="e2f95-426">Frequency, in hertz, at the high-end of the power supply's input frequency range 2.</span></span> <span data-ttu-id="e2f95-427">值為 0 (零) 表示 DC。</span><span class="sxs-lookup"><span data-stu-id="e2f95-427">A value of 0 (zero) implies DC.</span></span>

<span data-ttu-id="e2f95-428">這個屬性繼承自 [**CIM \_ 電源電源**](cim-powersupply.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-428">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-429">**Range2InputFrequencyLow**</span><span class="sxs-lookup"><span data-stu-id="e2f95-429">**Range2InputFrequencyLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-430">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e2f95-430">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-431">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-432">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電源供應器 \| 002.19 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 赫茲 ") </span><span class="sxs-lookup"><span data-stu-id="e2f95-432">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.19"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-433">電源供應器輸入頻率範圍2的低端頻率（以赫茲為單位）。</span><span class="sxs-lookup"><span data-stu-id="e2f95-433">Frequency, in hertz, at the low-end of the power supply's input frequency range 2.</span></span> <span data-ttu-id="e2f95-434">0值表示 DC。</span><span class="sxs-lookup"><span data-stu-id="e2f95-434">A value of 0 implies DC.</span></span>

<span data-ttu-id="e2f95-435">這個屬性繼承自 [**CIM \_ 電源電源**](cim-powersupply.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-435">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-436">**Range2InputVoltageHigh**</span><span class="sxs-lookup"><span data-stu-id="e2f95-436">**Range2InputVoltageHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-437">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e2f95-437">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-438">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-438">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-439">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Range2InputVoltageHigh" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫伏" ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-439">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range2InputVoltageHigh"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-440">如果電壓（以毫伏為單位）高於 **Range2InputVoltageHigh** 屬性所指定的值，則會藉由修剪電壓來彌補 UPS。</span><span class="sxs-lookup"><span data-stu-id="e2f95-440">If the voltage, in millivolts, rises above the value specified by the **Range2InputVoltageHigh** property, the UPS will compensate by trimming the voltage.</span></span> <span data-ttu-id="e2f95-441">值為 0 (零) 表示發生修剪的電壓未知。</span><span class="sxs-lookup"><span data-stu-id="e2f95-441">A value of 0 (zero) indicates that the voltage at which trimming occurs is unknown.</span></span>

<span data-ttu-id="e2f95-442">這個屬性繼承自 [**CIM \_ 電源電源**](cim-powersupply.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-442">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-443">**Range2InputVoltageLow**</span><span class="sxs-lookup"><span data-stu-id="e2f95-443">**Range2InputVoltageLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-444">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e2f95-444">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-445">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-445">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-446">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Range2InputVoltageLow" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫伏" ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-446">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range2InputVoltageLow"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-447">如果電壓（以毫伏為單位）低於 **Range2InputVoltageLow** 屬性指定的值，則會使用其電源線來提高電壓來彌補 UPS。</span><span class="sxs-lookup"><span data-stu-id="e2f95-447">If the voltage, in millivolts, drops below the value specified by the **Range2InputVoltageLow** property, the UPS will compensate by boosting the voltage using its power sources.</span></span> <span data-ttu-id="e2f95-448">值為 0 (零) 表示發生提升的電壓為未知。</span><span class="sxs-lookup"><span data-stu-id="e2f95-448">A value of 0 (zero) indicates that the voltage at which boosting occurs is unknown.</span></span>

<span data-ttu-id="e2f95-449">這個屬性繼承自 [**CIM \_ 電源電源**](cim-powersupply.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-449">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-450">**RemainingCapacityStatus**</span><span class="sxs-lookup"><span data-stu-id="e2f95-450">**RemainingCapacityStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-451">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e2f95-451">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-452">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-452">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-453">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| UPS 電池 \| 001.1」 ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-453">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|UPS Battery\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-454">指出 UPS 的電池、發電機或其他來源中剩餘的容量。</span><span class="sxs-lookup"><span data-stu-id="e2f95-454">Indication of the capacity remaining in the UPS's batteries, generator, or other source.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e2f95-455"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="e2f95-455"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="e2f95-456"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**一般** (2) </span><span class="sxs-lookup"><span data-stu-id="e2f95-456"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-457">執行時間剩餘的預估分鐘數大於 UPS 定義的低電源狀態 (通常是兩分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="e2f95-457">Remaining estimated minutes of run-time is greater than the UPS's defined low-power state (typically, two minutes).</span></span>

</dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="e2f95-458"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**低** (3) </span><span class="sxs-lookup"><span data-stu-id="e2f95-458"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-459">執行時間的剩餘估計分鐘數小於或等於 UPS 的已定義低電源狀態。</span><span class="sxs-lookup"><span data-stu-id="e2f95-459">Remaining estimated minutes of run-time is less than or equal to the UPS's defined low-power state.</span></span>

</dd> <dt>

<span id="Depleted"></span><span id="depleted"></span><span id="DEPLETED"></span>

<span data-ttu-id="e2f95-460"><span id="Depleted"></span><span id="depleted"></span><span id="DEPLETED"></span> (4) **耗盡**</span><span class="sxs-lookup"><span data-stu-id="e2f95-460"><span id="Depleted"></span><span id="depleted"></span><span id="DEPLETED"></span>**Depleted** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e2f95-461">當公用程式電源遺失時，UPS 將無法承受目前的負載 (包括) 的公用程式電源目前不存在的可能性。</span><span class="sxs-lookup"><span data-stu-id="e2f95-461">The UPS will be unable to sustain the present load when the utility power is lost (including the possibility that the utility power is currently absent).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e2f95-462">**狀態**</span><span class="sxs-lookup"><span data-stu-id="e2f95-462">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-463">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2f95-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-464">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-464">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-465">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-465">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-466">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="e2f95-466">Current status of the object.</span></span> <span data-ttu-id="e2f95-467">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-467">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e2f95-468">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="e2f95-468">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e2f95-469">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-469">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e2f95-470">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-470">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e2f95-471">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-471">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e2f95-472">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-472">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e2f95-473">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-473">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e2f95-474">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-474">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e2f95-475">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-475">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e2f95-476">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-476">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e2f95-477">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-477">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e2f95-478">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-478">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e2f95-479">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-479">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e2f95-480">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-480">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e2f95-481">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="e2f95-481">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-482">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e2f95-482">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-483">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-483">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-484">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="e2f95-484">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-485">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="e2f95-485">State of the logical device.</span></span> <span data-ttu-id="e2f95-486">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="e2f95-486">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="e2f95-487">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-487">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e2f95-488">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="e2f95-488">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e2f95-489">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="e2f95-489">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e2f95-490">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="e2f95-490">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e2f95-491">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="e2f95-491">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e2f95-492">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="e2f95-492">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e2f95-493">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e2f95-493">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-494">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2f95-494">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-495">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-496">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e2f95-496">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-497">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="e2f95-497">Scoping system's creation class name.</span></span>

<span data-ttu-id="e2f95-498">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-498">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-499">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e2f95-499">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-500">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2f95-500">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-501">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-501">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-502">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e2f95-502">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-503">設定系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="e2f95-503">Scoping system's name.</span></span>

<span data-ttu-id="e2f95-504">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-504">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-505">**TimeOnBackup**</span><span class="sxs-lookup"><span data-stu-id="e2f95-505">**TimeOnBackup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-506">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e2f95-506">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-507">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-508">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| UPS 電池 \| 001.2 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 秒 ") </span><span class="sxs-lookup"><span data-stu-id="e2f95-508">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|UPS Battery\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-509">UPS 上次切換至電池電力、產生器或其他電源的經過時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e2f95-509">Elapsed time, in seconds, since the UPS last switched to battery power, generator, or other power source.</span></span> <span data-ttu-id="e2f95-510">或者，自從 UPS 上次重新開機的時間，以較少者為准。</span><span class="sxs-lookup"><span data-stu-id="e2f95-510">Or, the time since the UPS was last restarted, whichever is less.</span></span> <span data-ttu-id="e2f95-511">如果 UPS 上線，則會傳回 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="e2f95-511">If the UPS is online, 0 (zero) will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-512">**TotalOutputPower**</span><span class="sxs-lookup"><span data-stu-id="e2f95-512">**TotalOutputPower**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-513">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e2f95-513">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-514">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-514">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-515">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電源供應器 \| 002.21 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 毫瓦 ") </span><span class="sxs-lookup"><span data-stu-id="e2f95-515">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.21"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatts")</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-516">電源供應器的總輸出能力，以毫瓦。</span><span class="sxs-lookup"><span data-stu-id="e2f95-516">Total output power of the power supply, in milliwatts.</span></span> <span data-ttu-id="e2f95-517">值為 0 (零) 表示不明。</span><span class="sxs-lookup"><span data-stu-id="e2f95-517">A value of 0 (zero) denotes unknown.</span></span>

<span data-ttu-id="e2f95-518">這個屬性繼承自 [**CIM \_ 電源電源**](cim-powersupply.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-518">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2f95-519">**TypeOfRangeSwitching**</span><span class="sxs-lookup"><span data-stu-id="e2f95-519">**TypeOfRangeSwitching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2f95-520">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e2f95-520">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-521">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2f95-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2f95-522">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電源供應器 \| 002.16」 ) </span><span class="sxs-lookup"><span data-stu-id="e2f95-522">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.16")</span></span>
</dt> </dl>

<span data-ttu-id="e2f95-523">在電源供應器中實作為輸入電壓範圍切換的類型。</span><span class="sxs-lookup"><span data-stu-id="e2f95-523">Type of input-voltage range switching implemented in the power supply.</span></span>

<span data-ttu-id="e2f95-524">這個屬性繼承自 [**CIM \_ 電源電源**](cim-powersupply.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-524">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e2f95-525">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="e2f95-525">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e2f95-526">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="e2f95-526">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="e2f95-527">**手動** (3) </span><span class="sxs-lookup"><span data-stu-id="e2f95-527">**Manual** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Autoswitch"></span><span id="autoswitch"></span><span id="AUTOSWITCH"></span>

<span data-ttu-id="e2f95-528">**Autoswitch** (4) </span><span class="sxs-lookup"><span data-stu-id="e2f95-528">**Autoswitch** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Wide_Range"></span><span id="wide_range"></span><span id="WIDE_RANGE"></span>

<span data-ttu-id="e2f95-529">**寬範圍** (5) </span><span class="sxs-lookup"><span data-stu-id="e2f95-529">**Wide Range** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e2f95-530">**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="e2f95-530">**Not Applicable** (6)</span></span>


<span data-ttu-id="e2f95-531"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e2f95-531"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="e2f95-532">備註</span><span class="sxs-lookup"><span data-stu-id="e2f95-532">Remarks</span></span>

<span data-ttu-id="e2f95-533">**Cim \_ UninterruptiblePowerSupply** 類別衍生自 [**cim \_ 電源供應**](cim-powersupply.md)器。</span><span class="sxs-lookup"><span data-stu-id="e2f95-533">The **CIM\_UninterruptiblePowerSupply** class is derived from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

<span data-ttu-id="e2f95-534">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="e2f95-534">WMI does not implement this class.</span></span> <span data-ttu-id="e2f95-535">針對衍生自 **CIM \_ UNINTERRUPTIBLEPOWERSUPPLY** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f95-535">For WMI classes derived from **CIM\_UninterruptiblePowerSupply**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e2f95-536">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="e2f95-536">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e2f95-537">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e2f95-537">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2f95-538">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2f95-538">Requirements</span></span>



| <span data-ttu-id="e2f95-539">需求</span><span class="sxs-lookup"><span data-stu-id="e2f95-539">Requirement</span></span> | <span data-ttu-id="e2f95-540">值</span><span class="sxs-lookup"><span data-stu-id="e2f95-540">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2f95-541">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e2f95-541">Minimum supported client</span></span><br/> | <span data-ttu-id="e2f95-542">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2f95-542">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e2f95-543">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e2f95-543">Minimum supported server</span></span><br/> | <span data-ttu-id="e2f95-544">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2f95-544">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e2f95-545">命名空間</span><span class="sxs-lookup"><span data-stu-id="e2f95-545">Namespace</span></span><br/>                | <span data-ttu-id="e2f95-546">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e2f95-546">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e2f95-547">MOF</span><span class="sxs-lookup"><span data-stu-id="e2f95-547">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2f95-548"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2f95-548"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2f95-549">DLL</span><span class="sxs-lookup"><span data-stu-id="e2f95-549">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2f95-550"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2f95-550"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2f95-551">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2f95-551">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2f95-552">**CIM \_ 電源**</span><span class="sxs-lookup"><span data-stu-id="e2f95-552">**CIM\_PowerSupply**</span></span>](cim-powersupply.md)
</dt> </dl>

 

