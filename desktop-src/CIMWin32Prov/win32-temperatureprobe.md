---
description: Win32 \_ TemperatureProbe&\# 32;WMI 類別代表溫度感應器的屬性， (的電子溫度計) 。
ms.assetid: 63ba1ae2-6abc-4d86-a7f6-f02536ebd8ac
ms.tgt_platform: multiple
title: Win32_TemperatureProbe 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TemperatureProbe
- Win32_TemperatureProbe.Reset
- Win32_TemperatureProbe.SetPowerState
- Win32_TemperatureProbe.Accuracy
- Win32_TemperatureProbe.Availability
- Win32_TemperatureProbe.Caption
- Win32_TemperatureProbe.ConfigManagerErrorCode
- Win32_TemperatureProbe.ConfigManagerUserConfig
- Win32_TemperatureProbe.CreationClassName
- Win32_TemperatureProbe.CurrentReading
- Win32_TemperatureProbe.Description
- Win32_TemperatureProbe.DeviceID
- Win32_TemperatureProbe.ErrorCleared
- Win32_TemperatureProbe.ErrorDescription
- Win32_TemperatureProbe.InstallDate
- Win32_TemperatureProbe.IsLinear
- Win32_TemperatureProbe.LastErrorCode
- Win32_TemperatureProbe.LowerThresholdCritical
- Win32_TemperatureProbe.LowerThresholdFatal
- Win32_TemperatureProbe.LowerThresholdNonCritical
- Win32_TemperatureProbe.MaxReadable
- Win32_TemperatureProbe.MinReadable
- Win32_TemperatureProbe.Name
- Win32_TemperatureProbe.NominalReading
- Win32_TemperatureProbe.NormalMax
- Win32_TemperatureProbe.NormalMin
- Win32_TemperatureProbe.PNPDeviceID
- Win32_TemperatureProbe.PowerManagementCapabilities
- Win32_TemperatureProbe.PowerManagementSupported
- Win32_TemperatureProbe.Resolution
- Win32_TemperatureProbe.Status
- Win32_TemperatureProbe.StatusInfo
- Win32_TemperatureProbe.SystemCreationClassName
- Win32_TemperatureProbe.SystemName
- Win32_TemperatureProbe.Tolerance
- Win32_TemperatureProbe.UpperThresholdCritical
- Win32_TemperatureProbe.UpperThresholdFatal
- Win32_TemperatureProbe.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b6de4ed6334747e8313098075bc916a1975f520c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847309"
---
# <a name="win32_temperatureprobe-class"></a><span data-ttu-id="b459b-103">Win32 \_ TemperatureProbe 類別</span><span class="sxs-lookup"><span data-stu-id="b459b-103">Win32\_TemperatureProbe class</span></span>

<span data-ttu-id="b459b-104">**Win32 \_ TemperatureProbe** [WMI 類別](../wmisdk/retrieving-a-class.md)代表溫度感應器的屬性 (的) 。</span><span class="sxs-lookup"><span data-stu-id="b459b-104">The **Win32\_TemperatureProbe** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a temperature sensor (electronic thermometer).</span></span>

<span data-ttu-id="b459b-105">**Win32 \_ TemperatureProbe** WMI 類別所提供的大部分資訊都來自 SMBIOS。</span><span class="sxs-lookup"><span data-stu-id="b459b-105">Most of the information that the **Win32\_TemperatureProbe** WMI class provides comes from SMBIOS.</span></span> <span data-ttu-id="b459b-106">**CurrentReading** 屬性的即時讀數無法從 SMBIOS 資料表中解壓縮。</span><span class="sxs-lookup"><span data-stu-id="b459b-106">Real-time readings for the **CurrentReading** property cannot be extracted from SMBIOS tables.</span></span> <span data-ttu-id="b459b-107">因此，目前的 WMI 執行不會填入 **CurrentReading** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b459b-107">For this reason, current implementations of WMI do not populate the **CurrentReading** property.</span></span> <span data-ttu-id="b459b-108">**CurrentReading** 屬性的目前狀態已保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="b459b-108">The **CurrentReading** property's presence is reserved for future use.</span></span>

<span data-ttu-id="b459b-109">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b459b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b459b-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="b459b-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b459b-111">語法</span><span class="sxs-lookup"><span data-stu-id="b459b-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFABB-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_TemperatureProbe : CIM_TemperatureSensor
{
  sint32   Accuracy;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  sint32   CurrentReading;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  boolean  IsLinear;
  uint32   LastErrorCode;
  sint32   LowerThresholdCritical;
  sint32   LowerThresholdFatal;
  sint32   LowerThresholdNonCritical;
  sint32   MaxReadable;
  sint32   MinReadable;
  string   Name;
  sint32   NominalReading;
  sint32   NormalMax;
  sint32   NormalMin;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   Resolution;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  sint32   Tolerance;
  sint32   UpperThresholdCritical;
  sint32   UpperThresholdFatal;
  sint32   UpperThresholdNonCritical;
};
```

## <a name="members"></a><span data-ttu-id="b459b-112">成員</span><span class="sxs-lookup"><span data-stu-id="b459b-112">Members</span></span>

<span data-ttu-id="b459b-113">**Win32 \_ TemperatureProbe** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b459b-113">The **Win32\_TemperatureProbe** class has these types of members:</span></span>

-   [<span data-ttu-id="b459b-114">方法</span><span class="sxs-lookup"><span data-stu-id="b459b-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="b459b-115">屬性</span><span class="sxs-lookup"><span data-stu-id="b459b-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b459b-116">方法</span><span class="sxs-lookup"><span data-stu-id="b459b-116">Methods</span></span>

<span data-ttu-id="b459b-117">**Win32 \_ TemperatureProbe** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b459b-117">The **Win32\_TemperatureProbe** class has these methods.</span></span>



| <span data-ttu-id="b459b-118">方法</span><span class="sxs-lookup"><span data-stu-id="b459b-118">Method</span></span>            | <span data-ttu-id="b459b-119">描述</span><span class="sxs-lookup"><span data-stu-id="b459b-119">Description</span></span>                                                                                                                                                                                                                     |
|:------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b459b-120">**重設**</span><span class="sxs-lookup"><span data-stu-id="b459b-120">**Reset**</span></span>         | <span data-ttu-id="b459b-121">未實作。</span><span class="sxs-lookup"><span data-stu-id="b459b-121">Not implemented.</span></span> <span data-ttu-id="b459b-122">若要執行此方法，請參閱 [**CIM \_ 溫度感應器**](cim-temperaturesensor.md)中的 [**Reset**](reset-method-in-class-cim-temperaturesensor.md)方法以取得檔。</span><span class="sxs-lookup"><span data-stu-id="b459b-122">To implement this method, see the [**Reset**](reset-method-in-class-cim-temperaturesensor.md) method in [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="b459b-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b459b-123">**SetPowerState**</span></span> | <span data-ttu-id="b459b-124">未實作。</span><span class="sxs-lookup"><span data-stu-id="b459b-124">Not implemented.</span></span> <span data-ttu-id="b459b-125">若要執行此方法，請參閱 [**CIM \_ 溫度感應器**](cim-temperaturesensor.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-temperaturesensor.md)方法，以取得檔。</span><span class="sxs-lookup"><span data-stu-id="b459b-125">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-temperaturesensor.md) method in [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b459b-126">屬性</span><span class="sxs-lookup"><span data-stu-id="b459b-126">Properties</span></span>

<span data-ttu-id="b459b-127">**Win32 \_ TemperatureProbe** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b459b-127">The **Win32\_TemperatureProbe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b459b-128">**精確度**</span><span class="sxs-lookup"><span data-stu-id="b459b-128">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-129">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b459b-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-131">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 溫度探查 \| 001.19 ") </span><span class="sxs-lookup"><span data-stu-id="b459b-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="b459b-132">測量的屬性之感應器的精確度。</span><span class="sxs-lookup"><span data-stu-id="b459b-132">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="b459b-133">其值會記錄為加號或減號百分之一%。</span><span class="sxs-lookup"><span data-stu-id="b459b-133">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="b459b-134">精確度、解析度和容錯可用來計算測量實體屬性的實際值。</span><span class="sxs-lookup"><span data-stu-id="b459b-134">Accuracy, resolution, and tolerance are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="b459b-135">精確度可能會有所不同，取決於裝置在其動態範圍上是否為線性。</span><span class="sxs-lookup"><span data-stu-id="b459b-135">Accuracy may vary and depends on whether or not the device is linear over its dynamic range.</span></span>

<span data-ttu-id="b459b-136">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-136">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-137">**可用性**</span><span class="sxs-lookup"><span data-stu-id="b459b-137">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-138">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b459b-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-140">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="b459b-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b459b-141">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="b459b-141">Availability and status of the device.</span></span>

<span data-ttu-id="b459b-142">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b459b-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="b459b-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b459b-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="b459b-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="b459b-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="b459b-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b459b-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="b459b-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="b459b-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="b459b-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b459b-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="b459b-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b459b-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="b459b-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="b459b-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="b459b-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-151">離線</span><span class="sxs-lookup"><span data-stu-id="b459b-151">Offline</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="b459b-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="b459b-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b459b-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="b459b-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="b459b-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="b459b-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="b459b-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="b459b-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b459b-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="b459b-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-157">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="b459b-157">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b459b-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="b459b-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-159">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="b459b-159">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b459b-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="b459b-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-161">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="b459b-161">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b459b-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="b459b-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b459b-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="b459b-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-164">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="b459b-164">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b459b-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="b459b-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-166">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="b459b-166">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="b459b-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="b459b-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-168">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="b459b-168">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="b459b-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="b459b-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-170">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="b459b-170">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="b459b-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="b459b-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-172">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="b459b-172">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b459b-173">**標題**</span><span class="sxs-lookup"><span data-stu-id="b459b-173">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b459b-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-176">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="b459b-176">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b459b-177">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="b459b-177">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="b459b-178">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-179">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b459b-179">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-180">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b459b-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-182">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="b459b-182">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b459b-183">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b459b-183">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="b459b-184">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-184">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="b459b-185"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="b459b-185"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="b459b-186"> (0)</span><span class="sxs-lookup"><span data-stu-id="b459b-186">(0)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-187">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="b459b-187">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="b459b-188"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="b459b-188"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="b459b-189">(1)</span><span class="sxs-lookup"><span data-stu-id="b459b-189">(1)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-190">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="b459b-190">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b459b-191"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="b459b-191"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="b459b-192">(2)</span><span class="sxs-lookup"><span data-stu-id="b459b-192">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="b459b-193"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="b459b-193"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="b459b-194">(3)</span><span class="sxs-lookup"><span data-stu-id="b459b-194">(3)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-195">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="b459b-195">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b459b-196"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="b459b-196"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="b459b-197">(4)</span><span class="sxs-lookup"><span data-stu-id="b459b-197">(4)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-198">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="b459b-198">Device is not working properly.</span></span> <span data-ttu-id="b459b-199">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="b459b-199">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="b459b-200"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="b459b-200"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="b459b-201">(5)</span><span class="sxs-lookup"><span data-stu-id="b459b-201">(5)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-202">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="b459b-202">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="b459b-203"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="b459b-203"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="b459b-204">(6)</span><span class="sxs-lookup"><span data-stu-id="b459b-204">(6)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-205">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="b459b-205">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="b459b-206"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="b459b-206"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="b459b-207">(7)</span><span class="sxs-lookup"><span data-stu-id="b459b-207">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="b459b-208"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="b459b-208"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="b459b-209">(8)</span><span class="sxs-lookup"><span data-stu-id="b459b-209">(8)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-210">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="b459b-210">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="b459b-211"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="b459b-211"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="b459b-212">(9)</span><span class="sxs-lookup"><span data-stu-id="b459b-212">(9)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-213">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="b459b-213">Device is not working properly.</span></span> <span data-ttu-id="b459b-214">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="b459b-214">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="b459b-215"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="b459b-215"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="b459b-216">(10)</span><span class="sxs-lookup"><span data-stu-id="b459b-216">(10)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-217">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="b459b-217">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="b459b-218"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="b459b-218"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="b459b-219">(11)</span><span class="sxs-lookup"><span data-stu-id="b459b-219">(11)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-220">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="b459b-220">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="b459b-221"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="b459b-221"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="b459b-222"> (12) </span><span class="sxs-lookup"><span data-stu-id="b459b-222">(12)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-223">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="b459b-223">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="b459b-224"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="b459b-224"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="b459b-225">(13)</span><span class="sxs-lookup"><span data-stu-id="b459b-225">(13)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-226">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="b459b-226">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="b459b-227"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="b459b-227"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="b459b-228">(14)</span><span class="sxs-lookup"><span data-stu-id="b459b-228">(14)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-229">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="b459b-229">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="b459b-230"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="b459b-230"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="b459b-231">(15)</span><span class="sxs-lookup"><span data-stu-id="b459b-231">(15)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-232">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="b459b-232">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="b459b-233"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="b459b-233"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="b459b-234">(16)</span><span class="sxs-lookup"><span data-stu-id="b459b-234">(16)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-235">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="b459b-235">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="b459b-236"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="b459b-236"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="b459b-237">(17)</span><span class="sxs-lookup"><span data-stu-id="b459b-237">(17)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-238">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="b459b-238">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b459b-239"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="b459b-239"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="b459b-240">(18)</span><span class="sxs-lookup"><span data-stu-id="b459b-240">(18)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-241">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="b459b-241">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="b459b-242"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="b459b-242"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="b459b-243">(19)</span><span class="sxs-lookup"><span data-stu-id="b459b-243">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b459b-244"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="b459b-244"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="b459b-245">(20)</span><span class="sxs-lookup"><span data-stu-id="b459b-245">(20)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-246">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="b459b-246">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="b459b-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="b459b-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="b459b-248">(21)</span><span class="sxs-lookup"><span data-stu-id="b459b-248">(21)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-249">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="b459b-249">System failure.</span></span> <span data-ttu-id="b459b-250">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="b459b-250">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="b459b-251">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="b459b-251">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="b459b-252"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="b459b-252"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="b459b-253">(22)</span><span class="sxs-lookup"><span data-stu-id="b459b-253">(22)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-254">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="b459b-254">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="b459b-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="b459b-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="b459b-256">(23)</span><span class="sxs-lookup"><span data-stu-id="b459b-256">(23)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-257">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="b459b-257">System failure.</span></span> <span data-ttu-id="b459b-258">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="b459b-258">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="b459b-259"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="b459b-259"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="b459b-260">(24)</span><span class="sxs-lookup"><span data-stu-id="b459b-260">(24)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-261">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b459b-261">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b459b-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="b459b-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b459b-263">(25)</span><span class="sxs-lookup"><span data-stu-id="b459b-263">(25)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-264">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="b459b-264">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b459b-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="b459b-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b459b-266">(26)</span><span class="sxs-lookup"><span data-stu-id="b459b-266">(26)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-267">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="b459b-267">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="b459b-268"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="b459b-268"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="b459b-269">(27)</span><span class="sxs-lookup"><span data-stu-id="b459b-269">(27)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-270">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="b459b-270">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="b459b-271"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="b459b-271"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="b459b-272">(28)</span><span class="sxs-lookup"><span data-stu-id="b459b-272">(28)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-273">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="b459b-273">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="b459b-274"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="b459b-274"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="b459b-275">(29)</span><span class="sxs-lookup"><span data-stu-id="b459b-275">(29)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-276">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="b459b-276">Device is disabled.</span></span> <span data-ttu-id="b459b-277">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="b459b-277">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="b459b-278"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="b459b-278"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="b459b-279">(30)</span><span class="sxs-lookup"><span data-stu-id="b459b-279">(30)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-280">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="b459b-280">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b459b-281"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="b459b-281"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="b459b-282"> (31) </span><span class="sxs-lookup"><span data-stu-id="b459b-282">(31)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-283">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="b459b-283">Device is not working properly.</span></span> <span data-ttu-id="b459b-284">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="b459b-284">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b459b-285">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="b459b-285">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-286">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b459b-286">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-287">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-288">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="b459b-288">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b459b-289">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="b459b-289">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="b459b-290">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-290">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-291">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b459b-291">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-292">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b459b-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-293">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-294">限定詞： [ **CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="b459b-294">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="b459b-295">第一個具象類別的名稱，這個類別會出現在建立實例時所用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="b459b-295">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="b459b-296">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="b459b-296">When used with the other key properties of a class, this property allows all instances of the class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="b459b-297">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-297">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-298">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="b459b-298">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-299">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b459b-299">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-300">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-301">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 溫度探查 \| 001.5 「) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「十分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="b459b-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="b459b-302">感應器指出的目前值。</span><span class="sxs-lookup"><span data-stu-id="b459b-302">Current value indicated by the sensor.</span></span>

<span data-ttu-id="b459b-303">目前的 WMI 執行不會填入 **CurrentReading** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b459b-303">Current implementations of WMI do not populate the **CurrentReading** property.</span></span> <span data-ttu-id="b459b-304">**CurrentReading** 屬性的目前狀態已保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="b459b-304">The **CurrentReading** property's presence is reserved for future use.</span></span>

<span data-ttu-id="b459b-305">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-305">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-306">**說明**</span><span class="sxs-lookup"><span data-stu-id="b459b-306">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-307">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b459b-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-308">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-309">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="b459b-309">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b459b-310">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="b459b-310">Description of the object.</span></span>

<span data-ttu-id="b459b-311">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-312">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b459b-312">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-313">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b459b-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-314">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-315">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "DeviceId" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="b459b-315">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b459b-316">目前探查的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="b459b-316">Unique identifier of the current probe.</span></span>

<span data-ttu-id="b459b-317">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-318">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="b459b-318">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-319">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b459b-319">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-320">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b459b-321">若 **為 TRUE**，則表示 **LastErrorCode** 中回報的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="b459b-321">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="b459b-322">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-323">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b459b-323">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-324">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b459b-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-325">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b459b-326">有關 **LastErrorCode** 中記錄錯誤的詳細資訊，以及您可以採取之任何矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b459b-326">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that you can take.</span></span>

<span data-ttu-id="b459b-327">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-328">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b459b-328">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-329">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="b459b-329">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-330">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-331">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="b459b-331">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b459b-332">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="b459b-332">Date and time the object is installed.</span></span> <span data-ttu-id="b459b-333">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="b459b-333">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b459b-334">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-334">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-335">**IsLinear**</span><span class="sxs-lookup"><span data-stu-id="b459b-335">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-336">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b459b-336">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-337">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b459b-338">若 **為 TRUE**，表示感應器在其動態範圍內是線性的。</span><span class="sxs-lookup"><span data-stu-id="b459b-338">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="b459b-339">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-339">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-340">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b459b-340">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-341">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b459b-341">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-342">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b459b-343">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b459b-343">Last error code reported by the logical device.</span></span>

<span data-ttu-id="b459b-344">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-345">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="b459b-345">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-346">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b459b-346">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-347">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-348">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 溫度探查 \| 001.13 「) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「十分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="b459b-348">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.13"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="b459b-349">指定範圍 (最小值和最大值的感應器閾值) 識別感應器操作狀況，可能是正常、非關鍵性、重大或嚴重狀況。</span><span class="sxs-lookup"><span data-stu-id="b459b-349">Sensor threshold value to specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="b459b-350">如果 **CurrentReading** 介於 **LowerThresholdCritical** 和 **LowerThresholdFatal** 之間，則目前的狀態為「嚴重」。</span><span class="sxs-lookup"><span data-stu-id="b459b-350">If **CurrentReading** is between **LowerThresholdCritical** and **LowerThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="b459b-351">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-351">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-352">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="b459b-352">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-353">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b459b-353">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-354">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-355">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 溫度探查 \| 001.15 「) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「十分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="b459b-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.15"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="b459b-356">指定範圍 (最小值和最大值的感應器閾值) 識別感應器操作狀況，可能是正常、非關鍵性、重大或嚴重狀況。</span><span class="sxs-lookup"><span data-stu-id="b459b-356">Sensor threshold value to specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="b459b-357">如果 **CurrentReading** 低於 **LowerThresholdFatal**，則目前的狀態為「嚴重」。</span><span class="sxs-lookup"><span data-stu-id="b459b-357">If **CurrentReading** is below **LowerThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="b459b-358">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-358">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-359">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="b459b-359">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-360">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b459b-360">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-361">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-362">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 溫度探查 \| 001.11 「) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「十分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="b459b-362">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="b459b-363">指定範圍 (最小值和最大值的感應器閾值) 識別感應器操作狀況，可能是正常、非關鍵性、重大或嚴重狀況。</span><span class="sxs-lookup"><span data-stu-id="b459b-363">Sensor threshold value to specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="b459b-364">如果 **CurrentReading** 介於 **LowerThresholdNonCritical** 和 **UpperThresholdNonCritical** 之間，則感應器會回報正常值。</span><span class="sxs-lookup"><span data-stu-id="b459b-364">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="b459b-365">如果 **CurrentReading** 介於 **LowerThresholdNonCritical** 和 **LowerThresholdCritical** 之間，則目前的狀態為非關鍵性。</span><span class="sxs-lookup"><span data-stu-id="b459b-365">If **CurrentReading** is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="b459b-366">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-366">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-367">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="b459b-367">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-368">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b459b-368">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-369">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-370">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 溫度探查 \| 001.9 「) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「十分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="b459b-370">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.9"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="b459b-371">數值感應器可讀取之已測量屬性的最大值。</span><span class="sxs-lookup"><span data-stu-id="b459b-371">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="b459b-372">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-372">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-373">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="b459b-373">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-374">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b459b-374">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-375">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-376">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 溫度探查 \| 001.10 「) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「十分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="b459b-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.10"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="b459b-377">數值感應器可讀取之已測量屬性的最小值。</span><span class="sxs-lookup"><span data-stu-id="b459b-377">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="b459b-378">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-378">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-379">**名稱**</span><span class="sxs-lookup"><span data-stu-id="b459b-379">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-380">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b459b-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-381">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-382">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="b459b-382">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b459b-383">物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="b459b-383">Label for the object.</span></span> <span data-ttu-id="b459b-384">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="b459b-384">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="b459b-385">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-386">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="b459b-386">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-387">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b459b-387">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-388">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-389">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 溫度探查 \| 001.6 「) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「十分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="b459b-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.6"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="b459b-390">數值感應器的一般或預期值。</span><span class="sxs-lookup"><span data-stu-id="b459b-390">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="b459b-391">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-391">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-392">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="b459b-392">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-393">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b459b-393">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-394">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-395">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 溫度探查 \| 001.7 「) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「十分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="b459b-395">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.7"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="b459b-396">數值感應器的一般或預期值。</span><span class="sxs-lookup"><span data-stu-id="b459b-396">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="b459b-397">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-397">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-398">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="b459b-398">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-399">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b459b-399">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-400">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-401">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 溫度探查 \| 001.8 「) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「十分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="b459b-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="b459b-402">使用者的指引，以取得數值感應器的一般最小範圍。</span><span class="sxs-lookup"><span data-stu-id="b459b-402">Guidance for the user as to the normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="b459b-403">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-403">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-404">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b459b-404">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-405">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b459b-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-406">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-407">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="b459b-407">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b459b-408">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="b459b-408">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="b459b-409">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="b459b-409">Example: "\*PNP030b"</span></span>

<span data-ttu-id="b459b-410">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-410">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-411">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b459b-411">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-412">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="b459b-412">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b459b-413">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b459b-414">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="b459b-414">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="b459b-415">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b459b-416"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="b459b-416"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b459b-417"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="b459b-417"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b459b-418"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="b459b-418"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b459b-419"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="b459b-419"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-420">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="b459b-420">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b459b-421"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="b459b-421"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-422">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="b459b-422">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b459b-423"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="b459b-423"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-424">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="b459b-424">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="b459b-425">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="b459b-425">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="b459b-426">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](../wmisdk/designing-managed-object-format--mof--classes.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-426">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b459b-427"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="b459b-427"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-428">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="b459b-428">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b459b-429"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="b459b-429"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b459b-430">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="b459b-430">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b459b-431">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="b459b-431">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-432">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b459b-432">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-433">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b459b-434">若 **為 TRUE**，則裝置可以是電源管理 (可進入暫停模式，依此類推) 。</span><span class="sxs-lookup"><span data-stu-id="b459b-434">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="b459b-435">屬性不表示電源管理功能目前已啟用，只有邏輯裝置能夠進行電源管理。</span><span class="sxs-lookup"><span data-stu-id="b459b-435">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="b459b-436">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-436">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-437">**解決方法**</span><span class="sxs-lookup"><span data-stu-id="b459b-437">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-438">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b459b-438">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-439">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-439">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-440">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 溫度探查 \| 001.17」 ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「百分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="b459b-440">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.17"), [**Units**](../wmisdk/standard-qualifiers.md) ("hundredths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="b459b-441">感應器解決測量屬性差異的能力。</span><span class="sxs-lookup"><span data-stu-id="b459b-441">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="b459b-442">此值可能會根據裝置的動態範圍是否為線性而有所不同。</span><span class="sxs-lookup"><span data-stu-id="b459b-442">This value may vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="b459b-443">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-443">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-444">**狀態**</span><span class="sxs-lookup"><span data-stu-id="b459b-444">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-445">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b459b-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-446">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-447">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="b459b-447">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b459b-448">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="b459b-448">Current status of the object.</span></span> <span data-ttu-id="b459b-449">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="b459b-449">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b459b-450">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="b459b-450">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b459b-451">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="b459b-451">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b459b-452">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="b459b-452">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b459b-453">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="b459b-453">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b459b-454">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-454">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b459b-455">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="b459b-455">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b459b-456">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="b459b-456">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b459b-457">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="b459b-457">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b459b-458">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="b459b-458">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b459b-459">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="b459b-459">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b459b-460">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="b459b-460">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b459b-461">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="b459b-461">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b459b-462">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="b459b-462">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b459b-463">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="b459b-463">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b459b-464">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="b459b-464">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b459b-465">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="b459b-465">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b459b-466">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="b459b-466">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b459b-467">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="b459b-467">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b459b-468">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b459b-468">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-469">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b459b-469">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-470">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-471">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="b459b-471">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b459b-472">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="b459b-472">State of the logical device.</span></span> <span data-ttu-id="b459b-473">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="b459b-473">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="b459b-474">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-474">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b459b-475">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="b459b-475">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b459b-476">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="b459b-476">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b459b-477">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="b459b-477">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b459b-478">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="b459b-478">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b459b-479">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="b459b-479">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b459b-480">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b459b-480">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-481">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b459b-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-482">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-483">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="b459b-483">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="b459b-484">範圍電腦之 **CreationClassName** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="b459b-484">Value for the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="b459b-485">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-486">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b459b-486">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-487">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b459b-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-488">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-489">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="b459b-489">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="b459b-490">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="b459b-490">Name of the scoping system.</span></span>

<span data-ttu-id="b459b-491">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-492">**寬容**</span><span class="sxs-lookup"><span data-stu-id="b459b-492">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-493">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b459b-493">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-494">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-495">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 溫度探查 \| 001.18 「) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「十分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="b459b-495">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.18"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="b459b-496">測量屬性之感應器的容錯。</span><span class="sxs-lookup"><span data-stu-id="b459b-496">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="b459b-497">容錯功能以及解析度和精確度，可用來計算測量實體屬性的實際值。</span><span class="sxs-lookup"><span data-stu-id="b459b-497">Tolerance, along with resolution and accuracy, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="b459b-498">容錯可能會根據裝置的動態範圍是否為線性而有所不同。</span><span class="sxs-lookup"><span data-stu-id="b459b-498">Tolerance may vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="b459b-499">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-499">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-500">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="b459b-500">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-501">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b459b-501">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-502">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-503">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 溫度探查 \| 001.14 「) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「十分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="b459b-503">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.14"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="b459b-504">感應器的閾值會指定 (最小值和最大值) 的範圍，以識別感應器操作狀況（可能是正常、非關鍵性、重大或嚴重狀況）。</span><span class="sxs-lookup"><span data-stu-id="b459b-504">Sensor's threshold values specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="b459b-505">如果 **CurrentReading** 介於 **UpperThresholdCritical** 和 **UpperThresholdFatal** 之間，則目前的狀態為「嚴重」。</span><span class="sxs-lookup"><span data-stu-id="b459b-505">If **CurrentReading** is between **UpperThresholdCritical** and **UpperThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="b459b-506">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-506">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-507">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="b459b-507">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-508">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b459b-508">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-509">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-510">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 溫度探查 \| 001.16 「) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「十分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="b459b-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.16"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="b459b-511">感應器的閾值會指定 (最小值和最大值) 的範圍，以識別感應器操作狀況（可能是正常、非關鍵性、重大或嚴重狀況）。</span><span class="sxs-lookup"><span data-stu-id="b459b-511">Sensor's threshold values specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="b459b-512">如果 **CurrentReading** 超過 **UpperThresholdFatal**，則目前的狀態為「嚴重」。</span><span class="sxs-lookup"><span data-stu-id="b459b-512">If **CurrentReading** is above **UpperThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="b459b-513">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-513">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b459b-514">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="b459b-514">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b459b-515">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b459b-515">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b459b-516">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b459b-516">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b459b-517">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 溫度探查 \| 001.12 「) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「十分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="b459b-517">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.12"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="b459b-518">感應器的閾值會指定 (最小值和最大值) 的範圍，以識別感應器操作狀況（可能是正常、非關鍵性、重大或嚴重狀況）。</span><span class="sxs-lookup"><span data-stu-id="b459b-518">Sensor's threshold values specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="b459b-519">如果 **CurrentReading** 介於 **LowerThresholdNonCritical** 和 **UpperThresholdNonCritical** 之間，則感應器會回報正常值。</span><span class="sxs-lookup"><span data-stu-id="b459b-519">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="b459b-520">如果 **CurrentReading** 介於 **UpperThresholdNonCritical** 和 **UpperThresholdCritical** 之間，則目前的狀態為非關鍵性。</span><span class="sxs-lookup"><span data-stu-id="b459b-520">If **CurrentReading** is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="b459b-521">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-521">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b459b-522">備註</span><span class="sxs-lookup"><span data-stu-id="b459b-522">Remarks</span></span>

<span data-ttu-id="b459b-523">**Win32 \_ TemperatureProbe** 類別衍生自 [**CIM \_ 溫度感應器**](cim-temperaturesensor.md)。</span><span class="sxs-lookup"><span data-stu-id="b459b-523">The **Win32\_TemperatureProbe** class is derived from [**CIM\_TemperatureSensor**](cim-temperaturesensor.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b459b-524">範例</span><span class="sxs-lookup"><span data-stu-id="b459b-524">Examples</span></span>

<span data-ttu-id="b459b-525">下列範例會傳回本機電腦的溫度探查資料。</span><span class="sxs-lookup"><span data-stu-id="b459b-525">The following example returns temperature probe data for the local computer.</span></span>


```VB
strComputer = "."
Set colTempProbe = GetObject("Winmgmts:"_
    & "{impersonationLevel=impersonate}!\\"_ 
    & strComputer & "\root\cimv2")._
    InstancesOf("Win32_TemperatureProbe")
Num = 0
For Each obj In colTempProbe      
    WScript.Echo   obj.Name & VBNewLine _
        & obj.DeviceID & VBNewLine _
        & obj.Status & VBNewLine _
        & obj.Resolution & VBNewLine _
        & obj.Tolerance & VBNewLine _
        & obj.Accuracy 
    Num = Num +1
Next
If Num = 0 Then
    WScript.Echo "No temperature probe data"
End If
```



## <a name="requirements"></a><span data-ttu-id="b459b-526">規格需求</span><span class="sxs-lookup"><span data-stu-id="b459b-526">Requirements</span></span>



| <span data-ttu-id="b459b-527">需求</span><span class="sxs-lookup"><span data-stu-id="b459b-527">Requirement</span></span> | <span data-ttu-id="b459b-528">值</span><span class="sxs-lookup"><span data-stu-id="b459b-528">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b459b-529">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b459b-529">Minimum supported client</span></span><br/> | <span data-ttu-id="b459b-530">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b459b-530">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b459b-531">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b459b-531">Minimum supported server</span></span><br/> | <span data-ttu-id="b459b-532">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b459b-532">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b459b-533">命名空間</span><span class="sxs-lookup"><span data-stu-id="b459b-533">Namespace</span></span><br/>                | <span data-ttu-id="b459b-534">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b459b-534">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b459b-535">MOF</span><span class="sxs-lookup"><span data-stu-id="b459b-535">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b459b-536"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="b459b-536"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b459b-537">DLL</span><span class="sxs-lookup"><span data-stu-id="b459b-537">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b459b-538"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b459b-538"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b459b-539">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b459b-539">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b459b-540">**CIM \_ 溫度感應器**</span><span class="sxs-lookup"><span data-stu-id="b459b-540">**CIM\_TemperatureSensor**</span></span>](cim-temperaturesensor.md)
</dt> <dt>

[<span data-ttu-id="b459b-541">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="b459b-541">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
