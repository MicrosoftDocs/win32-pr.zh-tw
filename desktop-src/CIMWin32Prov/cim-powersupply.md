---
description: CIM 電源 \_ 供應器類別代表電源供應器邏輯裝置的功能和管理。
ms.assetid: a9b79564-01d9-42a4-8586-782f179c179f
ms.tgt_platform: multiple
title: CIM_PowerSupply 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PowerSupply
- CIM_PowerSupply.ActiveInputVoltage
- CIM_PowerSupply.Availability
- CIM_PowerSupply.Caption
- CIM_PowerSupply.ConfigManagerErrorCode
- CIM_PowerSupply.ConfigManagerUserConfig
- CIM_PowerSupply.CreationClassName
- CIM_PowerSupply.Description
- CIM_PowerSupply.DeviceID
- CIM_PowerSupply.ErrorCleared
- CIM_PowerSupply.ErrorDescription
- CIM_PowerSupply.InstallDate
- CIM_PowerSupply.IsSwitchingSupply
- CIM_PowerSupply.LastErrorCode
- CIM_PowerSupply.Name
- CIM_PowerSupply.PNPDeviceID
- CIM_PowerSupply.PowerManagementCapabilities
- CIM_PowerSupply.PowerManagementSupported
- CIM_PowerSupply.Range1InputFrequencyHigh
- CIM_PowerSupply.Range1InputFrequencyLow
- CIM_PowerSupply.Range1InputVoltageHigh
- CIM_PowerSupply.Range1InputVoltageLow
- CIM_PowerSupply.Range2InputFrequencyHigh
- CIM_PowerSupply.Range2InputFrequencyLow
- CIM_PowerSupply.Range2InputVoltageHigh
- CIM_PowerSupply.Range2InputVoltageLow
- CIM_PowerSupply.Status
- CIM_PowerSupply.StatusInfo
- CIM_PowerSupply.SystemCreationClassName
- CIM_PowerSupply.SystemName
- CIM_PowerSupply.TotalOutputPower
- CIM_PowerSupply.TypeOfRangeSwitching
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35a1eb73c258b800bb8b33ad7aa75ea86cd0ef4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187694"
---
# <a name="cim_powersupply-class"></a><span data-ttu-id="28114-103">CIM \_ 電源供應類別</span><span class="sxs-lookup"><span data-stu-id="28114-103">CIM\_PowerSupply class</span></span>

<span data-ttu-id="28114-104">**CIM 電源 \_ 供應器** 類別代表電源供應器邏輯裝置的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="28114-104">The **CIM\_PowerSupply** class represents the capabilities and management of the power supply logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="28114-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="28114-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="28114-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="28114-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="28114-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="28114-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="28114-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="28114-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="28114-109">語法</span><span class="sxs-lookup"><span data-stu-id="28114-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C547-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_PowerSupply : CIM_LogicalDevice
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
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TotalOutputPower;
  uint16   TypeOfRangeSwitching;
};
```

## <a name="members"></a><span data-ttu-id="28114-110">成員</span><span class="sxs-lookup"><span data-stu-id="28114-110">Members</span></span>

<span data-ttu-id="28114-111">**CIM \_ 電源供應** 器類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="28114-111">The **CIM\_PowerSupply** class has these types of members:</span></span>

-   [<span data-ttu-id="28114-112">方法</span><span class="sxs-lookup"><span data-stu-id="28114-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="28114-113">屬性</span><span class="sxs-lookup"><span data-stu-id="28114-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="28114-114">方法</span><span class="sxs-lookup"><span data-stu-id="28114-114">Methods</span></span>

<span data-ttu-id="28114-115">**CIM \_ 電源供應** 器類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="28114-115">The **CIM\_PowerSupply** class has these methods.</span></span>



| <span data-ttu-id="28114-116">方法</span><span class="sxs-lookup"><span data-stu-id="28114-116">Method</span></span>                                                                 | <span data-ttu-id="28114-117">描述</span><span class="sxs-lookup"><span data-stu-id="28114-117">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="28114-118">**重設**</span><span class="sxs-lookup"><span data-stu-id="28114-118">**Reset**</span></span>](reset-method-in-class-cim-powersupply.md)                 | <span data-ttu-id="28114-119">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="28114-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="28114-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="28114-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="28114-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="28114-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-powersupply.md) | <span data-ttu-id="28114-122">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="28114-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="28114-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="28114-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="28114-124">屬性</span><span class="sxs-lookup"><span data-stu-id="28114-124">Properties</span></span>

<span data-ttu-id="28114-125">**CIM \_ 電源供應** 器類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="28114-125">The **CIM\_PowerSupply** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="28114-126">**ActiveInputVoltage**</span><span class="sxs-lookup"><span data-stu-id="28114-126">**ActiveInputVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-127">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="28114-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="28114-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28114-129">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電源供應器 \| 002.15」 ) </span><span class="sxs-lookup"><span data-stu-id="28114-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.15")</span></span>
</dt> </dl>

<span data-ttu-id="28114-130">目前使用中的電壓範圍。</span><span class="sxs-lookup"><span data-stu-id="28114-130">Voltage range that is currently in use.</span></span> <span data-ttu-id="28114-131">如果供應目前未繪製電源，則可以指定值 6 ( 「不會」 ) 。</span><span class="sxs-lookup"><span data-stu-id="28114-131">If the supply is not currently drawing power, the value 6 ("Neither") can be specified.</span></span> <span data-ttu-id="28114-132">這項資訊是在不斷電供應系統供應 (UPS) （ **CIM \_** 電源供應子類別）時所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="28114-132">This information is necessary in the case of an uninterruptible power supply (UPS), a subclass of **CIM\_PowerSupply**.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="28114-133">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="28114-133">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="28114-134">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="28114-134">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span data-ttu-id="28114-135">**範圍 1** (3) </span><span class="sxs-lookup"><span data-stu-id="28114-135">**Range 1** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span data-ttu-id="28114-136">**範圍 2** (4) </span><span class="sxs-lookup"><span data-stu-id="28114-136">**Range 2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="28114-137">**(5**) </span><span class="sxs-lookup"><span data-stu-id="28114-137">**Both** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Neither"></span><span id="neither"></span><span id="NEITHER"></span>

<span data-ttu-id="28114-138">**不** (6) </span><span class="sxs-lookup"><span data-stu-id="28114-138">**Neither** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="28114-139">**可用性**</span><span class="sxs-lookup"><span data-stu-id="28114-139">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-140">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="28114-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="28114-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28114-142">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="28114-142">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="28114-143">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="28114-143">Availability and status of the device.</span></span>

<span data-ttu-id="28114-144">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="28114-144">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="28114-145"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="28114-145"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="28114-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="28114-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="28114-147"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="28114-147"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="28114-148">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="28114-148">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="28114-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="28114-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="28114-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="28114-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="28114-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="28114-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="28114-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="28114-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="28114-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="28114-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="28114-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="28114-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="28114-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="28114-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="28114-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="28114-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="28114-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="28114-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="28114-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="28114-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="28114-159">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="28114-159">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="28114-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="28114-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="28114-161">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="28114-161">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="28114-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="28114-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="28114-163">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="28114-163">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="28114-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="28114-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="28114-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="28114-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="28114-166">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="28114-166">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="28114-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="28114-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="28114-168">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="28114-168">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="28114-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="28114-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="28114-170">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="28114-170">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="28114-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="28114-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="28114-172">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="28114-172">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="28114-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="28114-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="28114-174">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="28114-174">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="28114-175">**標題**</span><span class="sxs-lookup"><span data-stu-id="28114-175">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-176">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="28114-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="28114-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28114-178">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="28114-178">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="28114-179">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="28114-179">Short textual description of the object.</span></span>

<span data-ttu-id="28114-180">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="28114-180">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="28114-181">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="28114-181">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-182">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="28114-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="28114-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28114-184">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="28114-184">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="28114-185">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="28114-185">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="28114-186">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="28114-186">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="28114-187"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="28114-187"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="28114-188"> (0)</span><span class="sxs-lookup"><span data-stu-id="28114-188">(0)</span></span>


</dt> <dd>

<span data-ttu-id="28114-189">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="28114-189">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="28114-190"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="28114-190"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="28114-191">(1)</span><span class="sxs-lookup"><span data-stu-id="28114-191">(1)</span></span>


</dt> <dd>

<span data-ttu-id="28114-192">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="28114-192">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="28114-193"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="28114-193"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="28114-194">(2)</span><span class="sxs-lookup"><span data-stu-id="28114-194">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="28114-195"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="28114-195"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="28114-196">(3)</span><span class="sxs-lookup"><span data-stu-id="28114-196">(3)</span></span>


</dt> <dd>

<span data-ttu-id="28114-197">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="28114-197">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="28114-198"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="28114-198"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="28114-199">(4)</span><span class="sxs-lookup"><span data-stu-id="28114-199">(4)</span></span>


</dt> <dd>

<span data-ttu-id="28114-200">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="28114-200">Device is not working properly.</span></span> <span data-ttu-id="28114-201">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="28114-201">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="28114-202"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="28114-202"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="28114-203">(5)</span><span class="sxs-lookup"><span data-stu-id="28114-203">(5)</span></span>


</dt> <dd>

<span data-ttu-id="28114-204">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="28114-204">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="28114-205"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="28114-205"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="28114-206">(6)</span><span class="sxs-lookup"><span data-stu-id="28114-206">(6)</span></span>


</dt> <dd>

<span data-ttu-id="28114-207">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="28114-207">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="28114-208"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="28114-208"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="28114-209">(7)</span><span class="sxs-lookup"><span data-stu-id="28114-209">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="28114-210"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="28114-210"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="28114-211">(8)</span><span class="sxs-lookup"><span data-stu-id="28114-211">(8)</span></span>


</dt> <dd>

<span data-ttu-id="28114-212">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="28114-212">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="28114-213"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="28114-213"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="28114-214">(9)</span><span class="sxs-lookup"><span data-stu-id="28114-214">(9)</span></span>


</dt> <dd>

<span data-ttu-id="28114-215">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="28114-215">Device is not working properly.</span></span> <span data-ttu-id="28114-216">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="28114-216">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="28114-217"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="28114-217"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="28114-218">(10)</span><span class="sxs-lookup"><span data-stu-id="28114-218">(10)</span></span>


</dt> <dd>

<span data-ttu-id="28114-219">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="28114-219">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="28114-220"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="28114-220"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="28114-221">(11)</span><span class="sxs-lookup"><span data-stu-id="28114-221">(11)</span></span>


</dt> <dd>

<span data-ttu-id="28114-222">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="28114-222">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="28114-223"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="28114-223"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="28114-224"> (12) </span><span class="sxs-lookup"><span data-stu-id="28114-224">(12)</span></span>


</dt> <dd>

<span data-ttu-id="28114-225">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="28114-225">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="28114-226"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="28114-226"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="28114-227">(13)</span><span class="sxs-lookup"><span data-stu-id="28114-227">(13)</span></span>


</dt> <dd>

<span data-ttu-id="28114-228">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="28114-228">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="28114-229"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="28114-229"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="28114-230">(14)</span><span class="sxs-lookup"><span data-stu-id="28114-230">(14)</span></span>


</dt> <dd>

<span data-ttu-id="28114-231">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="28114-231">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="28114-232"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="28114-232"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="28114-233">(15)</span><span class="sxs-lookup"><span data-stu-id="28114-233">(15)</span></span>


</dt> <dd>

<span data-ttu-id="28114-234">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="28114-234">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="28114-235"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="28114-235"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="28114-236">(16)</span><span class="sxs-lookup"><span data-stu-id="28114-236">(16)</span></span>


</dt> <dd>

<span data-ttu-id="28114-237">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="28114-237">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="28114-238"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="28114-238"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="28114-239">(17)</span><span class="sxs-lookup"><span data-stu-id="28114-239">(17)</span></span>


</dt> <dd>

<span data-ttu-id="28114-240">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="28114-240">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="28114-241"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="28114-241"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="28114-242">(18)</span><span class="sxs-lookup"><span data-stu-id="28114-242">(18)</span></span>


</dt> <dd>

<span data-ttu-id="28114-243">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="28114-243">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="28114-244"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="28114-244"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="28114-245">(19)</span><span class="sxs-lookup"><span data-stu-id="28114-245">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="28114-246"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="28114-246"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="28114-247">(20)</span><span class="sxs-lookup"><span data-stu-id="28114-247">(20)</span></span>


</dt> <dd>

<span data-ttu-id="28114-248">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="28114-248">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="28114-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="28114-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="28114-250">(21)</span><span class="sxs-lookup"><span data-stu-id="28114-250">(21)</span></span>


</dt> <dd>

<span data-ttu-id="28114-251">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="28114-251">System failure.</span></span> <span data-ttu-id="28114-252">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="28114-252">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="28114-253">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="28114-253">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="28114-254"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="28114-254"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="28114-255">(22)</span><span class="sxs-lookup"><span data-stu-id="28114-255">(22)</span></span>


</dt> <dd>

<span data-ttu-id="28114-256">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="28114-256">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="28114-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="28114-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="28114-258">(23)</span><span class="sxs-lookup"><span data-stu-id="28114-258">(23)</span></span>


</dt> <dd>

<span data-ttu-id="28114-259">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="28114-259">System failure.</span></span> <span data-ttu-id="28114-260">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="28114-260">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="28114-261"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="28114-261"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="28114-262">(24)</span><span class="sxs-lookup"><span data-stu-id="28114-262">(24)</span></span>


</dt> <dd>

<span data-ttu-id="28114-263">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="28114-263">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="28114-264"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="28114-264"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="28114-265">(25)</span><span class="sxs-lookup"><span data-stu-id="28114-265">(25)</span></span>


</dt> <dd>

<span data-ttu-id="28114-266">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="28114-266">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="28114-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="28114-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="28114-268">(26)</span><span class="sxs-lookup"><span data-stu-id="28114-268">(26)</span></span>


</dt> <dd>

<span data-ttu-id="28114-269">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="28114-269">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="28114-270"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="28114-270"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="28114-271">(27)</span><span class="sxs-lookup"><span data-stu-id="28114-271">(27)</span></span>


</dt> <dd>

<span data-ttu-id="28114-272">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="28114-272">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="28114-273"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="28114-273"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="28114-274">(28)</span><span class="sxs-lookup"><span data-stu-id="28114-274">(28)</span></span>


</dt> <dd>

<span data-ttu-id="28114-275">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="28114-275">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="28114-276"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="28114-276"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="28114-277">(29)</span><span class="sxs-lookup"><span data-stu-id="28114-277">(29)</span></span>


</dt> <dd>

<span data-ttu-id="28114-278">裝置已停用;裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="28114-278">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="28114-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="28114-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="28114-280">(30)</span><span class="sxs-lookup"><span data-stu-id="28114-280">(30)</span></span>


</dt> <dd>

<span data-ttu-id="28114-281">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="28114-281">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="28114-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="28114-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="28114-283"> (31) </span><span class="sxs-lookup"><span data-stu-id="28114-283">(31)</span></span>


</dt> <dd>

<span data-ttu-id="28114-284">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="28114-284">Device is not working properly.</span></span> <span data-ttu-id="28114-285">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="28114-285">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="28114-286">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="28114-286">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-287">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="28114-287">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="28114-288">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28114-289">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="28114-289">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="28114-290">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="28114-290">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="28114-291">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="28114-291">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="28114-292">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="28114-292">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-293">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="28114-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="28114-294">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28114-295">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="28114-295">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="28114-296">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="28114-296">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="28114-297">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="28114-297">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="28114-298">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="28114-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="28114-299">**說明**</span><span class="sxs-lookup"><span data-stu-id="28114-299">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-300">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="28114-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="28114-301">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28114-302">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="28114-302">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="28114-303">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="28114-303">Textual description of the object.</span></span>

<span data-ttu-id="28114-304">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="28114-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="28114-305">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="28114-305">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-306">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="28114-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="28114-307">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28114-308">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="28114-308">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="28114-309">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="28114-309">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="28114-310">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="28114-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="28114-311">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="28114-311">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-312">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="28114-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="28114-313">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="28114-314">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="28114-314">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="28114-315">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="28114-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="28114-316">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="28114-316">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-317">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="28114-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="28114-318">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="28114-319">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="28114-319">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="28114-320">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="28114-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="28114-321">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="28114-321">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-322">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="28114-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="28114-323">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28114-324">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="28114-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="28114-325">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="28114-325">Date and time the object was installed.</span></span> <span data-ttu-id="28114-326">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="28114-326">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="28114-327">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="28114-327">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="28114-328">**IsSwitchingSupply**</span><span class="sxs-lookup"><span data-stu-id="28114-328">**IsSwitchingSupply**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-329">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="28114-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="28114-330">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="28114-331">若 **為 TRUE**，電源供應器會切換 (與線性) 供應。</span><span class="sxs-lookup"><span data-stu-id="28114-331">If **TRUE**, the power supply is a switching (versus linear) supply.</span></span>

</dd> <dt>

<span data-ttu-id="28114-332">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="28114-332">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-333">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="28114-333">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="28114-334">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="28114-335">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="28114-335">Last error code reported by the logical device.</span></span>

<span data-ttu-id="28114-336">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="28114-336">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="28114-337">**名稱**</span><span class="sxs-lookup"><span data-stu-id="28114-337">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-338">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="28114-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="28114-339">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28114-340">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="28114-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="28114-341">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="28114-341">Label by which the object is known.</span></span> <span data-ttu-id="28114-342">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="28114-342">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="28114-343">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="28114-343">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="28114-344">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="28114-344">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-345">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="28114-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="28114-346">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28114-347">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="28114-347">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="28114-348">邏輯裝置的 Win32 隨插即用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="28114-348">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="28114-349">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="28114-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="28114-350">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="28114-350">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="28114-351">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="28114-351">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-352">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="28114-352">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="28114-353">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="28114-354">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="28114-354">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="28114-355">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="28114-355">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="28114-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="28114-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="28114-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="28114-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="28114-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="28114-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="28114-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="28114-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="28114-360">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="28114-360">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="28114-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="28114-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="28114-362">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="28114-362">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="28114-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="28114-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="28114-364">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="28114-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="28114-365">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="28114-365">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="28114-366">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="28114-366">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="28114-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="28114-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="28114-368">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="28114-368">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="28114-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="28114-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="28114-370">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="28114-370">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="28114-371">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="28114-371">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-372">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="28114-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="28114-373">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="28114-374">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="28114-374">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="28114-375">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="28114-375">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="28114-376">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="28114-376">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="28114-377">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="28114-377">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="28114-378">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="28114-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="28114-379">**Range1InputFrequencyHigh**</span><span class="sxs-lookup"><span data-stu-id="28114-379">**Range1InputFrequencyHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-380">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="28114-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="28114-381">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28114-382">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "赫茲" ) </span><span class="sxs-lookup"><span data-stu-id="28114-382">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="28114-383">以赫茲為單位的頻率 (在電源供應器輸入頻率範圍1的高階) 。</span><span class="sxs-lookup"><span data-stu-id="28114-383">Frequency (in hertz) at the high-end of the power supply's input frequency range 1.</span></span> <span data-ttu-id="28114-384">0值表示 DC。</span><span class="sxs-lookup"><span data-stu-id="28114-384">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="28114-385">**Range1InputFrequencyLow**</span><span class="sxs-lookup"><span data-stu-id="28114-385">**Range1InputFrequencyLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-386">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="28114-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="28114-387">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28114-388">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電源供應器 \| 002.17 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 赫茲 ") </span><span class="sxs-lookup"><span data-stu-id="28114-388">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="28114-389">在電源供應器輸入頻率範圍1的低端) 的頻率 (（以赫茲為單位）。</span><span class="sxs-lookup"><span data-stu-id="28114-389">Frequency (in hertz) at the low-end of the power supply's input frequency range 1.</span></span> <span data-ttu-id="28114-390">0值表示 DC。</span><span class="sxs-lookup"><span data-stu-id="28114-390">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="28114-391">**Range1InputVoltageHigh**</span><span class="sxs-lookup"><span data-stu-id="28114-391">**Range1InputVoltageHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-392">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="28114-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="28114-393">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28114-394">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電源供應器 \| 002.8 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 毫伏 ") </span><span class="sxs-lookup"><span data-stu-id="28114-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="28114-395">電源供應器的輸入電壓範圍1的高電壓（以毫伏為單位）。</span><span class="sxs-lookup"><span data-stu-id="28114-395">High voltage of input voltage range 1 for the power supply, in millivolts.</span></span> <span data-ttu-id="28114-396">值為0表示「未知」。</span><span class="sxs-lookup"><span data-stu-id="28114-396">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="28114-397">**Range1InputVoltageLow**</span><span class="sxs-lookup"><span data-stu-id="28114-397">**Range1InputVoltageLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-398">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="28114-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="28114-399">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28114-400">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電源供應器 \| 002.7 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 毫伏 ") </span><span class="sxs-lookup"><span data-stu-id="28114-400">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="28114-401">電源供應器的輸入電壓低電壓範圍1，以毫伏為單位。</span><span class="sxs-lookup"><span data-stu-id="28114-401">Low voltage of input voltage range 1 for the power supply, in millivolts.</span></span> <span data-ttu-id="28114-402">值為0表示「未知」。</span><span class="sxs-lookup"><span data-stu-id="28114-402">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="28114-403">**Range2InputFrequencyHigh**</span><span class="sxs-lookup"><span data-stu-id="28114-403">**Range2InputFrequencyHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-404">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="28114-404">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="28114-405">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28114-406">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電源供應器 \| 002.20 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 赫茲 ") </span><span class="sxs-lookup"><span data-stu-id="28114-406">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.20"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="28114-407">以赫茲為單位的頻率 (，在電源供應器的輸入頻率範圍2的高階) 。</span><span class="sxs-lookup"><span data-stu-id="28114-407">Frequency (in hertz) at the high-end of the power supply's input frequency range 2.</span></span> <span data-ttu-id="28114-408">0值表示 DC。</span><span class="sxs-lookup"><span data-stu-id="28114-408">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="28114-409">**Range2InputFrequencyLow**</span><span class="sxs-lookup"><span data-stu-id="28114-409">**Range2InputFrequencyLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-410">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="28114-410">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="28114-411">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28114-412">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電源供應器 \| 002.19 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 赫茲 ") </span><span class="sxs-lookup"><span data-stu-id="28114-412">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.19"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="28114-413">在電源供應器輸入頻率範圍2的低端) 的頻率 (（以赫茲為單位）。</span><span class="sxs-lookup"><span data-stu-id="28114-413">Frequency (in hertz) at the low-end of the power supply's input frequency range 2.</span></span> <span data-ttu-id="28114-414">0值表示 DC。</span><span class="sxs-lookup"><span data-stu-id="28114-414">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="28114-415">**Range2InputVoltageHigh**</span><span class="sxs-lookup"><span data-stu-id="28114-415">**Range2InputVoltageHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-416">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="28114-416">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="28114-417">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28114-418">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電源供應器 \| 002.12 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 毫伏 ") </span><span class="sxs-lookup"><span data-stu-id="28114-418">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="28114-419">電源供應器的輸入電壓範圍2的高電壓（以毫伏為單位）。</span><span class="sxs-lookup"><span data-stu-id="28114-419">High voltage of input voltage range 2 for the power supply, in millivolts.</span></span> <span data-ttu-id="28114-420">值為0表示「未知」。</span><span class="sxs-lookup"><span data-stu-id="28114-420">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="28114-421">**Range2InputVoltageLow**</span><span class="sxs-lookup"><span data-stu-id="28114-421">**Range2InputVoltageLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-422">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="28114-422">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="28114-423">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28114-424">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電源供應器 \| 002.11 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 毫伏 ") </span><span class="sxs-lookup"><span data-stu-id="28114-424">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="28114-425">此電源供應器的輸入電壓下限範圍2（以毫伏為單位）。</span><span class="sxs-lookup"><span data-stu-id="28114-425">Low voltage of input voltage range 2 for this power supply, in Millivolts.</span></span> <span data-ttu-id="28114-426">值為0表示「未知」。</span><span class="sxs-lookup"><span data-stu-id="28114-426">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="28114-427">**狀態**</span><span class="sxs-lookup"><span data-stu-id="28114-427">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-428">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="28114-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="28114-429">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28114-430">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="28114-430">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="28114-431">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="28114-431">Current status of the object.</span></span>

<span data-ttu-id="28114-432">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="28114-432">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="28114-433">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="28114-433">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="28114-434">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="28114-434">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="28114-435">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="28114-435">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="28114-436">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="28114-436">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="28114-437">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="28114-437">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="28114-438">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="28114-438">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="28114-439">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="28114-439">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="28114-440">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="28114-440">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="28114-441">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="28114-441">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="28114-442">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="28114-442">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="28114-443">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="28114-443">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="28114-444">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="28114-444">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="28114-445">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="28114-445">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="28114-446">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="28114-446">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-447">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="28114-447">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="28114-448">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-448">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28114-449">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="28114-449">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="28114-450">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="28114-450">State of the logical device.</span></span> <span data-ttu-id="28114-451">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="28114-451">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="28114-452">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="28114-452">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="28114-453">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="28114-453">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="28114-454">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="28114-454">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="28114-455">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="28114-455">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="28114-456">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="28114-456">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="28114-457">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="28114-457">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="28114-458">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="28114-458">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-459">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="28114-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="28114-460">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28114-461">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="28114-461">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="28114-462">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="28114-462">Scoping system's creation class name.</span></span>

<span data-ttu-id="28114-463">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="28114-463">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="28114-464">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="28114-464">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-465">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="28114-465">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="28114-466">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28114-467">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="28114-467">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="28114-468">設定系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="28114-468">Scoping system's name.</span></span>

<span data-ttu-id="28114-469">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="28114-469">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="28114-470">**TotalOutputPower**</span><span class="sxs-lookup"><span data-stu-id="28114-470">**TotalOutputPower**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-471">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="28114-471">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="28114-472">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28114-473">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電源供應器 \| 002.21 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 毫瓦 ") </span><span class="sxs-lookup"><span data-stu-id="28114-473">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.21"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatts")</span></span>
</dt> </dl>

<span data-ttu-id="28114-474">電源供應器的總輸出能力，以毫瓦。</span><span class="sxs-lookup"><span data-stu-id="28114-474">Total output power of the power supply, in milliwatts.</span></span> <span data-ttu-id="28114-475">值為0表示「未知」。</span><span class="sxs-lookup"><span data-stu-id="28114-475">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="28114-476">**TypeOfRangeSwitching**</span><span class="sxs-lookup"><span data-stu-id="28114-476">**TypeOfRangeSwitching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28114-477">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="28114-477">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="28114-478">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28114-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28114-479">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電源供應器 \| 002.16」 ) </span><span class="sxs-lookup"><span data-stu-id="28114-479">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.16")</span></span>
</dt> </dl>

<span data-ttu-id="28114-480">在電源供應器中實作為輸入電壓範圍切換的類型。</span><span class="sxs-lookup"><span data-stu-id="28114-480">Type of input voltage range switching implemented in the power supply.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="28114-481">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="28114-481">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="28114-482">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="28114-482">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="28114-483">**手動** (3) </span><span class="sxs-lookup"><span data-stu-id="28114-483">**Manual** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Autoswitch"></span><span id="autoswitch"></span><span id="AUTOSWITCH"></span>

<span data-ttu-id="28114-484">**Autoswitch** (4) </span><span class="sxs-lookup"><span data-stu-id="28114-484">**Autoswitch** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Wide_Range"></span><span id="wide_range"></span><span id="WIDE_RANGE"></span>

<span data-ttu-id="28114-485">**寬範圍** (5) </span><span class="sxs-lookup"><span data-stu-id="28114-485">**Wide Range** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="28114-486">**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="28114-486">**Not Applicable** (6)</span></span>


<span data-ttu-id="28114-487"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="28114-487"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="28114-488">備註</span><span class="sxs-lookup"><span data-stu-id="28114-488">Remarks</span></span>

<span data-ttu-id="28114-489">**Cim \_ 電源供應** 器類別衍生自 [**cim \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="28114-489">The **CIM\_PowerSupply** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="28114-490">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="28114-490">WMI does not implement this class.</span></span> <span data-ttu-id="28114-491">針對衍生自 **CIM \_ 電源供應** 器的 WMI 歸類，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="28114-491">For WMI classed derived from **CIM\_PowerSupply**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="28114-492">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="28114-492">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="28114-493">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="28114-493">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="28114-494">規格需求</span><span class="sxs-lookup"><span data-stu-id="28114-494">Requirements</span></span>



| <span data-ttu-id="28114-495">需求</span><span class="sxs-lookup"><span data-stu-id="28114-495">Requirement</span></span> | <span data-ttu-id="28114-496">值</span><span class="sxs-lookup"><span data-stu-id="28114-496">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28114-497">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="28114-497">Minimum supported client</span></span><br/> | <span data-ttu-id="28114-498">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="28114-498">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="28114-499">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="28114-499">Minimum supported server</span></span><br/> | <span data-ttu-id="28114-500">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28114-500">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="28114-501">命名空間</span><span class="sxs-lookup"><span data-stu-id="28114-501">Namespace</span></span><br/>                | <span data-ttu-id="28114-502">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="28114-502">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="28114-503">MOF</span><span class="sxs-lookup"><span data-stu-id="28114-503">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28114-504"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="28114-504"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="28114-505">DLL</span><span class="sxs-lookup"><span data-stu-id="28114-505">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28114-506"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28114-506"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28114-507">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28114-507">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28114-508">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="28114-508">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

