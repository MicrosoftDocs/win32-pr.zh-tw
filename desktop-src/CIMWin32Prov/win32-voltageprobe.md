---
description: Win32 \_ VOLTAGEPROBE WMI 類別代表電壓感應器的屬性 (電子電壓表) 。
ms.assetid: ca27c1df-fb38-412d-b77c-d9ccf7941c66
ms.tgt_platform: multiple
title: Win32_VoltageProbe 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VoltageProbe
- Win32_VoltageProbe.Reset
- Win32_VoltageProbe.SetPowerState
- Win32_VoltageProbe.Accuracy
- Win32_VoltageProbe.Availability
- Win32_VoltageProbe.Caption
- Win32_VoltageProbe.ConfigManagerErrorCode
- Win32_VoltageProbe.ConfigManagerUserConfig
- Win32_VoltageProbe.CreationClassName
- Win32_VoltageProbe.CurrentReading
- Win32_VoltageProbe.Description
- Win32_VoltageProbe.DeviceID
- Win32_VoltageProbe.ErrorCleared
- Win32_VoltageProbe.ErrorDescription
- Win32_VoltageProbe.InstallDate
- Win32_VoltageProbe.IsLinear
- Win32_VoltageProbe.LastErrorCode
- Win32_VoltageProbe.LowerThresholdCritical
- Win32_VoltageProbe.LowerThresholdFatal
- Win32_VoltageProbe.LowerThresholdNonCritical
- Win32_VoltageProbe.MaxReadable
- Win32_VoltageProbe.MinReadable
- Win32_VoltageProbe.Name
- Win32_VoltageProbe.NominalReading
- Win32_VoltageProbe.NormalMax
- Win32_VoltageProbe.NormalMin
- Win32_VoltageProbe.PNPDeviceID
- Win32_VoltageProbe.PowerManagementCapabilities
- Win32_VoltageProbe.PowerManagementSupported
- Win32_VoltageProbe.Resolution
- Win32_VoltageProbe.Status
- Win32_VoltageProbe.StatusInfo
- Win32_VoltageProbe.SystemCreationClassName
- Win32_VoltageProbe.SystemName
- Win32_VoltageProbe.Tolerance
- Win32_VoltageProbe.UpperThresholdCritical
- Win32_VoltageProbe.UpperThresholdFatal
- Win32_VoltageProbe.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: acb5fe56706ed55098443ad9667eb980a1fe6d23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187616"
---
# <a name="win32_voltageprobe-class"></a><span data-ttu-id="7a46a-103">Win32 \_ VoltageProbe 類別</span><span class="sxs-lookup"><span data-stu-id="7a46a-103">Win32\_VoltageProbe class</span></span>

<span data-ttu-id="7a46a-104">**Win32 \_ VoltageProbe** [WMI 類別](../wmisdk/retrieving-a-class.md)代表電壓感應器的屬性 (電子電壓表) 。</span><span class="sxs-lookup"><span data-stu-id="7a46a-104">The **Win32\_VoltageProbe** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a voltage sensor (electronic voltmeter).</span></span>

<span data-ttu-id="7a46a-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="7a46a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7a46a-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="7a46a-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a46a-107">語法</span><span class="sxs-lookup"><span data-stu-id="7a46a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFAB8-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_VoltageProbe : CIM_VoltageSensor
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

## <a name="members"></a><span data-ttu-id="7a46a-108">成員</span><span class="sxs-lookup"><span data-stu-id="7a46a-108">Members</span></span>

<span data-ttu-id="7a46a-109">**Win32 \_ VoltageProbe** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7a46a-109">The **Win32\_VoltageProbe** class has these types of members:</span></span>

-   [<span data-ttu-id="7a46a-110">方法</span><span class="sxs-lookup"><span data-stu-id="7a46a-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="7a46a-111">屬性</span><span class="sxs-lookup"><span data-stu-id="7a46a-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7a46a-112">方法</span><span class="sxs-lookup"><span data-stu-id="7a46a-112">Methods</span></span>

<span data-ttu-id="7a46a-113">**Win32 \_ VoltageProbe** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="7a46a-113">The **Win32\_VoltageProbe** class has these methods.</span></span>



| <span data-ttu-id="7a46a-114">方法</span><span class="sxs-lookup"><span data-stu-id="7a46a-114">Method</span></span>            | <span data-ttu-id="7a46a-115">描述</span><span class="sxs-lookup"><span data-stu-id="7a46a-115">Description</span></span>                                                                                                                                                                                    |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a46a-116">**重設**</span><span class="sxs-lookup"><span data-stu-id="7a46a-116">**Reset**</span></span>         | <span data-ttu-id="7a46a-117">未實作。</span><span class="sxs-lookup"><span data-stu-id="7a46a-117">Not implemented.</span></span> <span data-ttu-id="7a46a-118">若要執行此方法，請參閱 [**CIM \_ 電壓感應器**](cim-voltagesensor.md)中的 [**Reset**](reset-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="7a46a-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_VoltageSensor**](cim-voltagesensor.md).</span></span><br/>                 |
| <span data-ttu-id="7a46a-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="7a46a-119">**SetPowerState**</span></span> | <span data-ttu-id="7a46a-120">未實作。</span><span class="sxs-lookup"><span data-stu-id="7a46a-120">Not implemented.</span></span> <span data-ttu-id="7a46a-121">若要執行此方法，請參閱 [**CIM \_ 電壓感應器**](cim-voltagesensor.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="7a46a-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_VoltageSensor**](cim-voltagesensor.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7a46a-122">屬性</span><span class="sxs-lookup"><span data-stu-id="7a46a-122">Properties</span></span>

<span data-ttu-id="7a46a-123">**Win32 \_ VoltageProbe** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7a46a-123">The **Win32\_VoltageProbe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7a46a-124">**精確度**</span><span class="sxs-lookup"><span data-stu-id="7a46a-124">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-125">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="7a46a-125">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-127">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 電壓探查 \| 001.19 ") </span><span class="sxs-lookup"><span data-stu-id="7a46a-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-128">測量的屬性之感應器的精確度。</span><span class="sxs-lookup"><span data-stu-id="7a46a-128">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="7a46a-129">精確度值會記錄為加號或減號百分之一%。</span><span class="sxs-lookup"><span data-stu-id="7a46a-129">The accuracy value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="7a46a-130">精確度（連同解析和容錯）是用來計算測量實體屬性的實際值。</span><span class="sxs-lookup"><span data-stu-id="7a46a-130">Accuracy, along with resolution and tolerance, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="7a46a-131">精確度可能會有所不同，取決於裝置在其動態範圍中是否為線性。</span><span class="sxs-lookup"><span data-stu-id="7a46a-131">The accuracy may vary and depends on whether or not the device is linear in its dynamic range.</span></span>

<span data-ttu-id="7a46a-132">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-132">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-133">**可用性**</span><span class="sxs-lookup"><span data-stu-id="7a46a-133">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-134">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7a46a-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-136">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="7a46a-136">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-137">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="7a46a-137">Availability and status of the device.</span></span>

<span data-ttu-id="7a46a-138">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-138">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7a46a-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="7a46a-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7a46a-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="7a46a-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="7a46a-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="7a46a-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="7a46a-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="7a46a-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="7a46a-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="7a46a-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7a46a-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="7a46a-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="7a46a-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="7a46a-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="7a46a-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="7a46a-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="7a46a-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="7a46a-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7a46a-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="7a46a-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="7a46a-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="7a46a-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="7a46a-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="7a46a-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="7a46a-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="7a46a-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-152">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="7a46a-152">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="7a46a-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="7a46a-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-154">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="7a46a-154">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="7a46a-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="7a46a-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-156">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="7a46a-156">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="7a46a-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="7a46a-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="7a46a-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="7a46a-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-159">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="7a46a-159">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="7a46a-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="7a46a-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-161">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="7a46a-161">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="7a46a-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="7a46a-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-163">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="7a46a-163">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="7a46a-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="7a46a-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-165">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="7a46a-165">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="7a46a-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="7a46a-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-167">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="7a46a-167">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7a46a-168">**標題**</span><span class="sxs-lookup"><span data-stu-id="7a46a-168">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-169">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7a46a-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-171">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="7a46a-171">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-172">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="7a46a-172">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="7a46a-173">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-174">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7a46a-174">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-175">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7a46a-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-177">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="7a46a-177">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-178">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7a46a-178">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="7a46a-179">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-179">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="7a46a-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="7a46a-181"> (0)</span><span class="sxs-lookup"><span data-stu-id="7a46a-181">(0)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-182">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="7a46a-182">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="7a46a-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="7a46a-184">(1)</span><span class="sxs-lookup"><span data-stu-id="7a46a-184">(1)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-185">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="7a46a-185">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7a46a-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="7a46a-187">(2)</span><span class="sxs-lookup"><span data-stu-id="7a46a-187">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="7a46a-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="7a46a-189">(3)</span><span class="sxs-lookup"><span data-stu-id="7a46a-189">(3)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-190">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="7a46a-190">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7a46a-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="7a46a-192">(4)</span><span class="sxs-lookup"><span data-stu-id="7a46a-192">(4)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-193">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="7a46a-193">Device is not working properly.</span></span> <span data-ttu-id="7a46a-194">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="7a46a-194">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="7a46a-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="7a46a-196">(5)</span><span class="sxs-lookup"><span data-stu-id="7a46a-196">(5)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-197">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="7a46a-197">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="7a46a-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="7a46a-199">(6)</span><span class="sxs-lookup"><span data-stu-id="7a46a-199">(6)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-200">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="7a46a-200">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="7a46a-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="7a46a-202">(7)</span><span class="sxs-lookup"><span data-stu-id="7a46a-202">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="7a46a-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="7a46a-204">(8)</span><span class="sxs-lookup"><span data-stu-id="7a46a-204">(8)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-205">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="7a46a-205">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="7a46a-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="7a46a-207">(9)</span><span class="sxs-lookup"><span data-stu-id="7a46a-207">(9)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-208">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="7a46a-208">Device is not working properly.</span></span> <span data-ttu-id="7a46a-209">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="7a46a-209">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="7a46a-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="7a46a-211">(10)</span><span class="sxs-lookup"><span data-stu-id="7a46a-211">(10)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-212">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="7a46a-212">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="7a46a-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="7a46a-214">(11)</span><span class="sxs-lookup"><span data-stu-id="7a46a-214">(11)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-215">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="7a46a-215">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="7a46a-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="7a46a-217"> (12) </span><span class="sxs-lookup"><span data-stu-id="7a46a-217">(12)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-218">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="7a46a-218">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="7a46a-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="7a46a-220">(13)</span><span class="sxs-lookup"><span data-stu-id="7a46a-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-221">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="7a46a-221">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="7a46a-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="7a46a-223">(14)</span><span class="sxs-lookup"><span data-stu-id="7a46a-223">(14)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-224">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="7a46a-224">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="7a46a-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="7a46a-226">(15)</span><span class="sxs-lookup"><span data-stu-id="7a46a-226">(15)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-227">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="7a46a-227">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="7a46a-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="7a46a-229">(16)</span><span class="sxs-lookup"><span data-stu-id="7a46a-229">(16)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-230">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="7a46a-230">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="7a46a-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="7a46a-232">(17)</span><span class="sxs-lookup"><span data-stu-id="7a46a-232">(17)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-233">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="7a46a-233">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7a46a-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="7a46a-235">(18)</span><span class="sxs-lookup"><span data-stu-id="7a46a-235">(18)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-236">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="7a46a-236">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="7a46a-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="7a46a-238">(19)</span><span class="sxs-lookup"><span data-stu-id="7a46a-238">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7a46a-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="7a46a-240">(20)</span><span class="sxs-lookup"><span data-stu-id="7a46a-240">(20)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-241">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="7a46a-241">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="7a46a-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="7a46a-243">(21)</span><span class="sxs-lookup"><span data-stu-id="7a46a-243">(21)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-244">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="7a46a-244">System failure.</span></span> <span data-ttu-id="7a46a-245">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="7a46a-245">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="7a46a-246">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="7a46a-246">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="7a46a-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="7a46a-248">(22)</span><span class="sxs-lookup"><span data-stu-id="7a46a-248">(22)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-249">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="7a46a-249">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="7a46a-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="7a46a-251">(23)</span><span class="sxs-lookup"><span data-stu-id="7a46a-251">(23)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-252">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="7a46a-252">System failure.</span></span> <span data-ttu-id="7a46a-253">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="7a46a-253">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="7a46a-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="7a46a-255">(24)</span><span class="sxs-lookup"><span data-stu-id="7a46a-255">(24)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-256">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="7a46a-256">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7a46a-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="7a46a-258">(25)</span><span class="sxs-lookup"><span data-stu-id="7a46a-258">(25)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-259">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="7a46a-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7a46a-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="7a46a-261">(26)</span><span class="sxs-lookup"><span data-stu-id="7a46a-261">(26)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-262">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="7a46a-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="7a46a-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="7a46a-264">(27)</span><span class="sxs-lookup"><span data-stu-id="7a46a-264">(27)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-265">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="7a46a-265">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="7a46a-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="7a46a-267">(28)</span><span class="sxs-lookup"><span data-stu-id="7a46a-267">(28)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-268">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="7a46a-268">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="7a46a-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="7a46a-270">(29)</span><span class="sxs-lookup"><span data-stu-id="7a46a-270">(29)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-271">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="7a46a-271">Device is disabled.</span></span> <span data-ttu-id="7a46a-272">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="7a46a-272">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="7a46a-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="7a46a-274">(30)</span><span class="sxs-lookup"><span data-stu-id="7a46a-274">(30)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-275">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="7a46a-275">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7a46a-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="7a46a-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="7a46a-277"> (31) </span><span class="sxs-lookup"><span data-stu-id="7a46a-277">(31)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-278">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="7a46a-278">Device is not working properly.</span></span> <span data-ttu-id="7a46a-279">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="7a46a-279">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7a46a-280">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="7a46a-280">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-281">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="7a46a-281">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-282">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-283">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="7a46a-283">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-284">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="7a46a-284">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="7a46a-285">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-285">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-286">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7a46a-286">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-287">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7a46a-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-288">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-289">限定詞： [ **CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="7a46a-289">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-290">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="7a46a-290">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="7a46a-291">搭配類別的其他索引鍵屬性使用時，此屬性可讓這個類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="7a46a-291">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="7a46a-292">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-292">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-293">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="7a46a-293">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-294">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="7a46a-294">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-295">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-296">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 電壓探查 \| 001.5 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" 毫伏 ") </span><span class="sxs-lookup"><span data-stu-id="7a46a-296">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-297">感應器指出的目前值。</span><span class="sxs-lookup"><span data-stu-id="7a46a-297">Current value indicated by the sensor.</span></span>

<span data-ttu-id="7a46a-298">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-298">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-299">**說明**</span><span class="sxs-lookup"><span data-stu-id="7a46a-299">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-300">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7a46a-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-301">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-302">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="7a46a-302">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-303">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="7a46a-303">Description of the object.</span></span>

<span data-ttu-id="7a46a-304">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-305">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="7a46a-305">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-306">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7a46a-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-307">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-308">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "DeviceId" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="7a46a-308">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-309">電壓探查的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="7a46a-309">Unique identifier of the voltage probe.</span></span>

<span data-ttu-id="7a46a-310">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-311">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="7a46a-311">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-312">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="7a46a-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-313">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-314">若 **為 TRUE**，則表示 **LastErrorCode** 中回報的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="7a46a-314">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="7a46a-315">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-316">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="7a46a-316">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-317">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7a46a-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-318">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-319">**LastErrorCode** 中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7a46a-319">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="7a46a-320">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-321">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7a46a-321">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-322">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="7a46a-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-323">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-324">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="7a46a-324">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-325">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="7a46a-325">Date and time the object is installed.</span></span> <span data-ttu-id="7a46a-326">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="7a46a-326">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="7a46a-327">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-327">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-328">**IsLinear**</span><span class="sxs-lookup"><span data-stu-id="7a46a-328">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-329">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="7a46a-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-330">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-331">若 **為 TRUE**，表示感應器在其動態範圍內是線性的。</span><span class="sxs-lookup"><span data-stu-id="7a46a-331">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="7a46a-332">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-332">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-333">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7a46a-333">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-334">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7a46a-334">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-335">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-336">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7a46a-336">Last error code reported by the logical device.</span></span>

<span data-ttu-id="7a46a-337">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-338">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="7a46a-338">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-339">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="7a46a-339">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-340">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-341">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 電壓探查 \| 001.13 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" 毫伏 ") </span><span class="sxs-lookup"><span data-stu-id="7a46a-341">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.13"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-342">感應器閾值會指定 (最小值和最大值的範圍，) 判斷感應器是否在正常、非關鍵性、重大或嚴重狀況下運作。</span><span class="sxs-lookup"><span data-stu-id="7a46a-342">Sensor threshold values specify the ranges (minimum and maximum values) to determine if the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="7a46a-343">如果 **CurrentReading** 介於 **LowerThresholdCritical** 和 **LowerThresholdFatal** 之間，則目前的狀態為「嚴重」。</span><span class="sxs-lookup"><span data-stu-id="7a46a-343">If **CurrentReading** is between **LowerThresholdCritical** and **LowerThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="7a46a-344">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-344">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-345">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="7a46a-345">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-346">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="7a46a-346">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-347">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-348">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 電壓探查 \| 001.15 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" 毫伏 ") </span><span class="sxs-lookup"><span data-stu-id="7a46a-348">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.15"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-349">感應器閾值會指定 (最小值和最大值的範圍，) 判斷感應器是否在正常、非關鍵性、重大或嚴重狀況下運作。</span><span class="sxs-lookup"><span data-stu-id="7a46a-349">Sensor threshold values specify the ranges (minimum and maximum values) to determine if the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="7a46a-350">如果 **CurrentReading** 低於 **LowerThresholdFatal**，則目前的狀態為「嚴重」。</span><span class="sxs-lookup"><span data-stu-id="7a46a-350">If **CurrentReading** is below **LowerThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="7a46a-351">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-351">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-352">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="7a46a-352">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-353">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="7a46a-353">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-354">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-355">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 電壓探查 \| 001.11 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" 毫伏 ") </span><span class="sxs-lookup"><span data-stu-id="7a46a-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-356">感應器閾值會指定 (最小值和最大值的範圍，) 判斷感應器是否在正常、非關鍵性、重大或嚴重狀況下運作。</span><span class="sxs-lookup"><span data-stu-id="7a46a-356">Sensor threshold values specify the ranges (minimum and maximum values) to determine if the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="7a46a-357">如果 **CurrentReading** 介於 **LowerThresholdNonCritical** 和 **UpperThresholdNonCritical** 之間，則感應器會回報正常值。</span><span class="sxs-lookup"><span data-stu-id="7a46a-357">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="7a46a-358">如果 **CurrentReading** 介於 **LowerThresholdNonCritical** 和 **LowerThresholdCritical** 之間，則目前的狀態為非關鍵性。</span><span class="sxs-lookup"><span data-stu-id="7a46a-358">If **CurrentReading** is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="7a46a-359">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-359">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-360">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="7a46a-360">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-361">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="7a46a-361">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-362">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-363">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 電壓探查 \| 001.9 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" 毫伏 ") </span><span class="sxs-lookup"><span data-stu-id="7a46a-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.9"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-364">數值感應器可讀取之已測量屬性的最大值。</span><span class="sxs-lookup"><span data-stu-id="7a46a-364">Largest value of the measured property that the numeric sensor can read.</span></span>

<span data-ttu-id="7a46a-365">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-365">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-366">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="7a46a-366">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-367">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="7a46a-367">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-368">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-369">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 電壓探查 \| 001.10 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" 毫伏 ") </span><span class="sxs-lookup"><span data-stu-id="7a46a-369">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.10"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-370">數值感應器可讀取之已測量屬性的最小值。</span><span class="sxs-lookup"><span data-stu-id="7a46a-370">Smallest value of the measured property that the numeric sensor can read.</span></span>

<span data-ttu-id="7a46a-371">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-371">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-372">**名稱**</span><span class="sxs-lookup"><span data-stu-id="7a46a-372">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-373">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7a46a-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-374">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-375">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="7a46a-375">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-376">物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="7a46a-376">Label for an object.</span></span> <span data-ttu-id="7a46a-377">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="7a46a-377">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="7a46a-378">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-378">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-379">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="7a46a-379">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-380">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="7a46a-380">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-381">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-382">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 電壓探查 \| 001.6 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" 毫伏 ") </span><span class="sxs-lookup"><span data-stu-id="7a46a-382">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.6"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-383">數值感應器的一般或預期值。</span><span class="sxs-lookup"><span data-stu-id="7a46a-383">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="7a46a-384">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-384">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-385">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="7a46a-385">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-386">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="7a46a-386">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-387">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-388">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 電壓探查 \| 001.7 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" 毫伏 ") </span><span class="sxs-lookup"><span data-stu-id="7a46a-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.7"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-389">數值感應器的一般或預期值。</span><span class="sxs-lookup"><span data-stu-id="7a46a-389">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="7a46a-390">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-390">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-391">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="7a46a-391">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-392">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="7a46a-392">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-393">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-394">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 電壓探查 \| 001.8 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" 毫伏 ") </span><span class="sxs-lookup"><span data-stu-id="7a46a-394">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-395">指示，讓使用者指出數值感應器的一般最小範圍。</span><span class="sxs-lookup"><span data-stu-id="7a46a-395">Guidance for the user to indicate the normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="7a46a-396">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-396">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-397">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="7a46a-397">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-398">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7a46a-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-399">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-400">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="7a46a-400">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-401">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="7a46a-401">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="7a46a-402">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-402">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="7a46a-403">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="7a46a-403">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-404">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="7a46a-404">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-405">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="7a46a-405">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-406">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-407">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="7a46a-407">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="7a46a-408">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="7a46a-408">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7a46a-409"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="7a46a-409"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="7a46a-410"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="7a46a-410"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7a46a-411"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="7a46a-411"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7a46a-412"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="7a46a-412"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-413">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="7a46a-413">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="7a46a-414"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="7a46a-414"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-415">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="7a46a-415">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="7a46a-416"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="7a46a-416"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-417">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="7a46a-417">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="7a46a-418">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="7a46a-418">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="7a46a-419">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](../wmisdk/designing-managed-object-format--mof--classes.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-419">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="7a46a-420"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="7a46a-420"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-421">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="7a46a-421">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="7a46a-422"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="7a46a-422"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="7a46a-423">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="7a46a-423">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7a46a-424">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="7a46a-424">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-425">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="7a46a-425">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-426">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-427">若 **為 TRUE**，則裝置可以是電源管理的，這表示它可以進入暫停模式，依此類推。</span><span class="sxs-lookup"><span data-stu-id="7a46a-427">If **TRUE**, the device can be power-managed, which means that it can be put into suspend mode, and so on.</span></span> <span data-ttu-id="7a46a-428">屬性不會指出電源管理功能目前已啟用，但它會指出邏輯裝置能夠進行電源管理。</span><span class="sxs-lookup"><span data-stu-id="7a46a-428">The property does not indicate that power management features are currently enabled, but it does indicate that the logical device is capable of power management.</span></span>

<span data-ttu-id="7a46a-429">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-429">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-430">**解決方法**</span><span class="sxs-lookup"><span data-stu-id="7a46a-430">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-431">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7a46a-431">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-432">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-432">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-433">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 電壓探查 \| 001.17 「) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「十分之一個毫伏」 ) </span><span class="sxs-lookup"><span data-stu-id="7a46a-433">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.17"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-434">感應器解決測量屬性差異的能力。</span><span class="sxs-lookup"><span data-stu-id="7a46a-434">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="7a46a-435">此值可能會不同，且取決於裝置在其動態範圍中是否為線性。</span><span class="sxs-lookup"><span data-stu-id="7a46a-435">This value may vary and depends on whether the device is linear in its dynamic range.</span></span>

<span data-ttu-id="7a46a-436">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-436">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-437">**狀態**</span><span class="sxs-lookup"><span data-stu-id="7a46a-437">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-438">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7a46a-438">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-439">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-439">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-440">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="7a46a-440">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-441">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="7a46a-441">Current status of the object.</span></span> <span data-ttu-id="7a46a-442">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="7a46a-442">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="7a46a-443">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="7a46a-443">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="7a46a-444">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="7a46a-444">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7a46a-445">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="7a46a-445">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7a46a-446">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="7a46a-446">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7a46a-447">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-447">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7a46a-448">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="7a46a-448">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7a46a-449">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="7a46a-449">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7a46a-450">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="7a46a-450">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7a46a-451">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="7a46a-451">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7a46a-452">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="7a46a-452">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7a46a-453">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="7a46a-453">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7a46a-454">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="7a46a-454">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7a46a-455">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="7a46a-455">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7a46a-456">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="7a46a-456">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7a46a-457">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="7a46a-457">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7a46a-458">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="7a46a-458">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7a46a-459">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="7a46a-459">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7a46a-460">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="7a46a-460">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7a46a-461">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="7a46a-461">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-462">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7a46a-462">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-463">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-463">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-464">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="7a46a-464">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-465">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="7a46a-465">State of the logical device.</span></span> <span data-ttu-id="7a46a-466">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="7a46a-466">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="7a46a-467">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7a46a-468">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="7a46a-468">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7a46a-469">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="7a46a-469">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7a46a-470">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="7a46a-470">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7a46a-471">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="7a46a-471">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7a46a-472">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="7a46a-472">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7a46a-473">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7a46a-473">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-474">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7a46a-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-475">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-476">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="7a46a-476">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-477">範圍電腦之 **CreationClassName** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="7a46a-477">Value for the **CreationClassName** property of the scoping computer.</span></span>

<span data-ttu-id="7a46a-478">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-479">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="7a46a-479">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-480">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7a46a-480">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-481">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-482">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="7a46a-482">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-483">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a46a-483">Name of the scoping system.</span></span>

<span data-ttu-id="7a46a-484">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-484">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-485">**寬容**</span><span class="sxs-lookup"><span data-stu-id="7a46a-485">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-486">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="7a46a-486">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-487">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-488">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 電壓探查 \| 001.18 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" 毫伏 ") </span><span class="sxs-lookup"><span data-stu-id="7a46a-488">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.18"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-489">測量屬性之感應器的容錯。</span><span class="sxs-lookup"><span data-stu-id="7a46a-489">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="7a46a-490">容錯功能以及解析度和精確度，可用來計算測量實體屬性的實際值。</span><span class="sxs-lookup"><span data-stu-id="7a46a-490">Tolerance, along with resolution and accuracy, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="7a46a-491">容錯可能會有所不同，取決於裝置在其動態範圍中是否為線性。</span><span class="sxs-lookup"><span data-stu-id="7a46a-491">Tolerance may vary, and depends on whether the device is linear in its dynamic range.</span></span>

<span data-ttu-id="7a46a-492">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-492">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-493">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="7a46a-493">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-494">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="7a46a-494">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-495">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-496">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 電壓探查 \| 001.14 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" 毫伏 ") </span><span class="sxs-lookup"><span data-stu-id="7a46a-496">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.14"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-497">感應器臨界值會指定範圍 (最小值和最大值，) 判斷感應器是否正常運作、非關鍵性、重大或嚴重狀況。</span><span class="sxs-lookup"><span data-stu-id="7a46a-497">Sensor threshold values specify the ranges (minimum and maximum values) to determine whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="7a46a-498">如果 **CurrentReading** 介於 **UpperThresholdCritical** 和 **UpperThresholdFatal** 之間，則目前的狀態為「嚴重」。</span><span class="sxs-lookup"><span data-stu-id="7a46a-498">If **CurrentReading** is between **UpperThresholdCritical** and **UpperThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="7a46a-499">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-499">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-500">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="7a46a-500">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-501">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="7a46a-501">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-502">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-503">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 電壓探查 \| 001.16 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" 毫伏 ") </span><span class="sxs-lookup"><span data-stu-id="7a46a-503">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.16"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-504">感應器臨界值會指定範圍 (最小值和最大值，) 判斷感應器是否正常運作、非關鍵性、重大或嚴重狀況。</span><span class="sxs-lookup"><span data-stu-id="7a46a-504">Sensor threshold values specify the ranges (minimum and maximum values) to determine whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="7a46a-505">如果 **CurrentReading** 超過 **UpperThresholdFatal**，則目前的狀態為「嚴重」。</span><span class="sxs-lookup"><span data-stu-id="7a46a-505">If **CurrentReading** is above **UpperThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="7a46a-506">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-506">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a46a-507">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="7a46a-507">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a46a-508">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="7a46a-508">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-509">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a46a-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a46a-510">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 電壓探查 \| 001.12 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" 毫伏 ") </span><span class="sxs-lookup"><span data-stu-id="7a46a-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.12"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="7a46a-511">感應器臨界值會指定範圍 (最小值和最大值，) 判斷感應器是否正常運作、非關鍵性、重大或嚴重狀況。</span><span class="sxs-lookup"><span data-stu-id="7a46a-511">Sensor threshold values specify the ranges (minimum and maximum values) to determine whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="7a46a-512">如果 **CurrentReading** 介於 **LowerThresholdNonCritical** 和 **UpperThresholdNonCritical** 之間，則感應器會回報正常值。</span><span class="sxs-lookup"><span data-stu-id="7a46a-512">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="7a46a-513">如果 **CurrentReading** 介於 **UpperThresholdNonCritical** 和 **UpperThresholdCritical** 之間，則目前的狀態為非關鍵性。</span><span class="sxs-lookup"><span data-stu-id="7a46a-513">If **CurrentReading** is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="7a46a-514">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-514">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a46a-515">備註</span><span class="sxs-lookup"><span data-stu-id="7a46a-515">Remarks</span></span>

<span data-ttu-id="7a46a-516">**Win32 \_ VoltageProbe** 類別衍生自 [**CIM \_ 電壓感應器**](cim-voltagesensor.md)。</span><span class="sxs-lookup"><span data-stu-id="7a46a-516">The **Win32\_VoltageProbe** class is derived from [**CIM\_VoltageSensor**](cim-voltagesensor.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a46a-517">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a46a-517">Requirements</span></span>



| <span data-ttu-id="7a46a-518">需求</span><span class="sxs-lookup"><span data-stu-id="7a46a-518">Requirement</span></span> | <span data-ttu-id="7a46a-519">值</span><span class="sxs-lookup"><span data-stu-id="7a46a-519">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a46a-520">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7a46a-520">Minimum supported client</span></span><br/> | <span data-ttu-id="7a46a-521">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a46a-521">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7a46a-522">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7a46a-522">Minimum supported server</span></span><br/> | <span data-ttu-id="7a46a-523">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a46a-523">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7a46a-524">命名空間</span><span class="sxs-lookup"><span data-stu-id="7a46a-524">Namespace</span></span><br/>                | <span data-ttu-id="7a46a-525">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7a46a-525">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7a46a-526">MOF</span><span class="sxs-lookup"><span data-stu-id="7a46a-526">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a46a-527"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="7a46a-527"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a46a-528">DLL</span><span class="sxs-lookup"><span data-stu-id="7a46a-528">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a46a-529"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a46a-529"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a46a-530">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a46a-530">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a46a-531">**CIM \_ 電壓感應器**</span><span class="sxs-lookup"><span data-stu-id="7a46a-531">**CIM\_VoltageSensor**</span></span>](cim-voltagesensor.md)
</dt> <dt>

[<span data-ttu-id="7a46a-532">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="7a46a-532">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
