---
description: Win32 \_ CURRENTPROBE WMI 類別代表目前監視感應器 (ammeter) 的屬性。
ms.assetid: 2e1da856-b787-404b-ac4b-080c4950bad8
ms.tgt_platform: multiple
title: Win32_CurrentProbe 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CurrentProbe
- Win32_CurrentProbe.Reset
- Win32_CurrentProbe.SetPowerState
- Win32_CurrentProbe.Accuracy
- Win32_CurrentProbe.Availability
- Win32_CurrentProbe.Caption
- Win32_CurrentProbe.ConfigManagerErrorCode
- Win32_CurrentProbe.ConfigManagerUserConfig
- Win32_CurrentProbe.CreationClassName
- Win32_CurrentProbe.CurrentReading
- Win32_CurrentProbe.Description
- Win32_CurrentProbe.DeviceID
- Win32_CurrentProbe.ErrorCleared
- Win32_CurrentProbe.ErrorDescription
- Win32_CurrentProbe.InstallDate
- Win32_CurrentProbe.IsLinear
- Win32_CurrentProbe.LastErrorCode
- Win32_CurrentProbe.LowerThresholdCritical
- Win32_CurrentProbe.LowerThresholdFatal
- Win32_CurrentProbe.LowerThresholdNonCritical
- Win32_CurrentProbe.MaxReadable
- Win32_CurrentProbe.MinReadable
- Win32_CurrentProbe.Name
- Win32_CurrentProbe.NominalReading
- Win32_CurrentProbe.NormalMax
- Win32_CurrentProbe.NormalMin
- Win32_CurrentProbe.PNPDeviceID
- Win32_CurrentProbe.PowerManagementCapabilities
- Win32_CurrentProbe.PowerManagementSupported
- Win32_CurrentProbe.Resolution
- Win32_CurrentProbe.Status
- Win32_CurrentProbe.StatusInfo
- Win32_CurrentProbe.SystemCreationClassName
- Win32_CurrentProbe.SystemName
- Win32_CurrentProbe.Tolerance
- Win32_CurrentProbe.UpperThresholdCritical
- Win32_CurrentProbe.UpperThresholdFatal
- Win32_CurrentProbe.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: be834e56eb3d958a8cd6ee653dc9a248c14ae3bc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847592"
---
# <a name="win32_currentprobe-class"></a><span data-ttu-id="46659-103">Win32 \_ CurrentProbe 類別</span><span class="sxs-lookup"><span data-stu-id="46659-103">Win32\_CurrentProbe class</span></span>

<span data-ttu-id="46659-104">**Win32 \_ CurrentProbe** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表目前監視感應器 (ammeter) 的屬性。</span><span class="sxs-lookup"><span data-stu-id="46659-104">The **Win32\_CurrentProbe** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a current monitoring sensor (ammeter).</span></span>

<span data-ttu-id="46659-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="46659-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="46659-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="46659-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="46659-107">語法</span><span class="sxs-lookup"><span data-stu-id="46659-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFABA-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_CurrentProbe : CIM_CurrentSensor
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

## <a name="members"></a><span data-ttu-id="46659-108">成員</span><span class="sxs-lookup"><span data-stu-id="46659-108">Members</span></span>

<span data-ttu-id="46659-109">**Win32 \_ CurrentProbe** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="46659-109">The **Win32\_CurrentProbe** class has these types of members:</span></span>

-   [<span data-ttu-id="46659-110">方法</span><span class="sxs-lookup"><span data-stu-id="46659-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="46659-111">屬性</span><span class="sxs-lookup"><span data-stu-id="46659-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="46659-112">方法</span><span class="sxs-lookup"><span data-stu-id="46659-112">Methods</span></span>

<span data-ttu-id="46659-113">**Win32 \_ CurrentProbe** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="46659-113">The **Win32\_CurrentProbe** class has these methods.</span></span>



| <span data-ttu-id="46659-114">方法</span><span class="sxs-lookup"><span data-stu-id="46659-114">Method</span></span>            | <span data-ttu-id="46659-115">描述</span><span class="sxs-lookup"><span data-stu-id="46659-115">Description</span></span>                                                                                                                                                                                                      |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46659-116">**重設**</span><span class="sxs-lookup"><span data-stu-id="46659-116">**Reset**</span></span>         | <span data-ttu-id="46659-117">未實作。</span><span class="sxs-lookup"><span data-stu-id="46659-117">Not implemented.</span></span> <span data-ttu-id="46659-118">若要執行此方法，請參閱 [**CIM \_ CurrentSensor**](cim-currentsensor.md)中的 [**Reset**](reset-method-in-class-cim-controller.md)方法以取得檔。</span><span class="sxs-lookup"><span data-stu-id="46659-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_CurrentSensor**](cim-currentsensor.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="46659-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="46659-119">**SetPowerState**</span></span> | <span data-ttu-id="46659-120">未實作。</span><span class="sxs-lookup"><span data-stu-id="46659-120">Not implemented.</span></span> <span data-ttu-id="46659-121">若要執行此方法，請參閱 [**CIM \_ CurrentSensor**](cim-currentsensor.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法，以取得檔。</span><span class="sxs-lookup"><span data-stu-id="46659-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_CurrentSensor**](cim-currentsensor.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="46659-122">屬性</span><span class="sxs-lookup"><span data-stu-id="46659-122">Properties</span></span>

<span data-ttu-id="46659-123">**Win32 \_ CurrentProbe** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="46659-123">The **Win32\_CurrentProbe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="46659-124">**精確度**</span><span class="sxs-lookup"><span data-stu-id="46659-124">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-125">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="46659-125">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="46659-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-127">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電子目前的探查 \| 001.19」 ) </span><span class="sxs-lookup"><span data-stu-id="46659-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="46659-128">測量的屬性之感應器的精確度。</span><span class="sxs-lookup"><span data-stu-id="46659-128">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="46659-129">此值會記錄為加號或減號百分之一%。</span><span class="sxs-lookup"><span data-stu-id="46659-129">The value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="46659-130">精確度（連同解析和容錯）是用來計算測量實體屬性的實際值。</span><span class="sxs-lookup"><span data-stu-id="46659-130">Accuracy, along with resolution and tolerance, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="46659-131">精確度可能會有所不同，取決於裝置在其動態範圍上是否為線性。</span><span class="sxs-lookup"><span data-stu-id="46659-131">Accuracy may vary and depends on whether or not the device is linear over its dynamic range.</span></span>

<span data-ttu-id="46659-132">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-132">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-133">**可用性**</span><span class="sxs-lookup"><span data-stu-id="46659-133">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-134">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="46659-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="46659-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-136">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="46659-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="46659-137">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="46659-137">Availability and status of the device.</span></span>

<span data-ttu-id="46659-138">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-138">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="46659-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="46659-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="46659-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="46659-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="46659-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="46659-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="46659-142">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="46659-142">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="46659-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="46659-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="46659-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="46659-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="46659-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="46659-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="46659-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="46659-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="46659-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="46659-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="46659-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="46659-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="46659-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="46659-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="46659-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="46659-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="46659-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="46659-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="46659-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="46659-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="46659-153">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="46659-153">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="46659-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="46659-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="46659-155">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="46659-155">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="46659-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="46659-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="46659-157">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="46659-157">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="46659-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="46659-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="46659-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="46659-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="46659-160">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="46659-160">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="46659-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="46659-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="46659-162">已暫停。</span><span class="sxs-lookup"><span data-stu-id="46659-162">Paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="46659-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="46659-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="46659-164">未就緒。</span><span class="sxs-lookup"><span data-stu-id="46659-164">Not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="46659-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="46659-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="46659-166">尚未設定。</span><span class="sxs-lookup"><span data-stu-id="46659-166">Not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="46659-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="46659-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="46659-168">目前的感應器無法使用。</span><span class="sxs-lookup"><span data-stu-id="46659-168">Current sensor is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="46659-169">**標題**</span><span class="sxs-lookup"><span data-stu-id="46659-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-170">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="46659-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46659-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-172">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="46659-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="46659-173">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="46659-173">Short description of the object a one-line string.</span></span>

<span data-ttu-id="46659-174">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-175">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="46659-175">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-176">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="46659-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46659-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-178">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="46659-178">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="46659-179">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="46659-179">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="46659-180">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-180">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="46659-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="46659-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="46659-182"> (0)</span><span class="sxs-lookup"><span data-stu-id="46659-182">(0)</span></span>


</dt> <dd>

<span data-ttu-id="46659-183">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="46659-183">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="46659-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="46659-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="46659-185">(1)</span><span class="sxs-lookup"><span data-stu-id="46659-185">(1)</span></span>


</dt> <dd>

<span data-ttu-id="46659-186">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="46659-186">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="46659-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="46659-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="46659-188">(2)</span><span class="sxs-lookup"><span data-stu-id="46659-188">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="46659-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="46659-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="46659-190">(3)</span><span class="sxs-lookup"><span data-stu-id="46659-190">(3)</span></span>


</dt> <dd>

<span data-ttu-id="46659-191">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="46659-191">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="46659-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="46659-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="46659-193">(4)</span><span class="sxs-lookup"><span data-stu-id="46659-193">(4)</span></span>


</dt> <dd>

<span data-ttu-id="46659-194">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="46659-194">Device is not working properly.</span></span> <span data-ttu-id="46659-195">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="46659-195">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="46659-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="46659-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="46659-197">(5)</span><span class="sxs-lookup"><span data-stu-id="46659-197">(5)</span></span>


</dt> <dd>

<span data-ttu-id="46659-198">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="46659-198">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="46659-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="46659-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="46659-200">(6)</span><span class="sxs-lookup"><span data-stu-id="46659-200">(6)</span></span>


</dt> <dd>

<span data-ttu-id="46659-201">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="46659-201">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="46659-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="46659-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="46659-203">(7)</span><span class="sxs-lookup"><span data-stu-id="46659-203">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="46659-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="46659-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="46659-205">(8)</span><span class="sxs-lookup"><span data-stu-id="46659-205">(8)</span></span>


</dt> <dd>

<span data-ttu-id="46659-206">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="46659-206">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="46659-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="46659-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="46659-208">(9)</span><span class="sxs-lookup"><span data-stu-id="46659-208">(9)</span></span>


</dt> <dd>

<span data-ttu-id="46659-209">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="46659-209">Device is not working properly.</span></span> <span data-ttu-id="46659-210">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="46659-210">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="46659-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="46659-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="46659-212">(10)</span><span class="sxs-lookup"><span data-stu-id="46659-212">(10)</span></span>


</dt> <dd>

<span data-ttu-id="46659-213">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="46659-213">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="46659-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="46659-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="46659-215">(11)</span><span class="sxs-lookup"><span data-stu-id="46659-215">(11)</span></span>


</dt> <dd>

<span data-ttu-id="46659-216">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="46659-216">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="46659-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="46659-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="46659-218"> (12) </span><span class="sxs-lookup"><span data-stu-id="46659-218">(12)</span></span>


</dt> <dd>

<span data-ttu-id="46659-219">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="46659-219">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="46659-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="46659-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="46659-221">(13)</span><span class="sxs-lookup"><span data-stu-id="46659-221">(13)</span></span>


</dt> <dd>

<span data-ttu-id="46659-222">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="46659-222">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="46659-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="46659-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="46659-224">(14)</span><span class="sxs-lookup"><span data-stu-id="46659-224">(14)</span></span>


</dt> <dd>

<span data-ttu-id="46659-225">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="46659-225">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="46659-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="46659-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="46659-227">(15)</span><span class="sxs-lookup"><span data-stu-id="46659-227">(15)</span></span>


</dt> <dd>

<span data-ttu-id="46659-228">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="46659-228">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="46659-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="46659-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="46659-230">(16)</span><span class="sxs-lookup"><span data-stu-id="46659-230">(16)</span></span>


</dt> <dd>

<span data-ttu-id="46659-231">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="46659-231">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="46659-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="46659-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="46659-233">(17)</span><span class="sxs-lookup"><span data-stu-id="46659-233">(17)</span></span>


</dt> <dd>

<span data-ttu-id="46659-234">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="46659-234">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="46659-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="46659-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="46659-236">(18)</span><span class="sxs-lookup"><span data-stu-id="46659-236">(18)</span></span>


</dt> <dd>

<span data-ttu-id="46659-237">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="46659-237">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="46659-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="46659-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="46659-239">(19)</span><span class="sxs-lookup"><span data-stu-id="46659-239">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="46659-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="46659-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="46659-241">(20)</span><span class="sxs-lookup"><span data-stu-id="46659-241">(20)</span></span>


</dt> <dd>

<span data-ttu-id="46659-242">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="46659-242">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="46659-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="46659-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="46659-244">(21)</span><span class="sxs-lookup"><span data-stu-id="46659-244">(21)</span></span>


</dt> <dd>

<span data-ttu-id="46659-245">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="46659-245">System failure.</span></span> <span data-ttu-id="46659-246">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="46659-246">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="46659-247">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="46659-247">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="46659-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="46659-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="46659-249">(22)</span><span class="sxs-lookup"><span data-stu-id="46659-249">(22)</span></span>


</dt> <dd>

<span data-ttu-id="46659-250">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="46659-250">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="46659-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="46659-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="46659-252">(23)</span><span class="sxs-lookup"><span data-stu-id="46659-252">(23)</span></span>


</dt> <dd>

<span data-ttu-id="46659-253">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="46659-253">System failure.</span></span> <span data-ttu-id="46659-254">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="46659-254">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="46659-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="46659-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="46659-256">(24)</span><span class="sxs-lookup"><span data-stu-id="46659-256">(24)</span></span>


</dt> <dd>

<span data-ttu-id="46659-257">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="46659-257">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="46659-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="46659-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="46659-259">(25)</span><span class="sxs-lookup"><span data-stu-id="46659-259">(25)</span></span>


</dt> <dd>

<span data-ttu-id="46659-260">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="46659-260">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="46659-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="46659-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="46659-262">(26)</span><span class="sxs-lookup"><span data-stu-id="46659-262">(26)</span></span>


</dt> <dd>

<span data-ttu-id="46659-263">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="46659-263">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="46659-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="46659-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="46659-265">(27)</span><span class="sxs-lookup"><span data-stu-id="46659-265">(27)</span></span>


</dt> <dd>

<span data-ttu-id="46659-266">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="46659-266">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="46659-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="46659-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="46659-268">(28)</span><span class="sxs-lookup"><span data-stu-id="46659-268">(28)</span></span>


</dt> <dd>

<span data-ttu-id="46659-269">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="46659-269">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="46659-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="46659-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="46659-271">(29)</span><span class="sxs-lookup"><span data-stu-id="46659-271">(29)</span></span>


</dt> <dd>

<span data-ttu-id="46659-272">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="46659-272">Device is disabled.</span></span> <span data-ttu-id="46659-273">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="46659-273">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="46659-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="46659-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="46659-275">(30)</span><span class="sxs-lookup"><span data-stu-id="46659-275">(30)</span></span>


</dt> <dd>

<span data-ttu-id="46659-276">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="46659-276">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="46659-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="46659-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="46659-278"> (31) </span><span class="sxs-lookup"><span data-stu-id="46659-278">(31)</span></span>


</dt> <dd>

<span data-ttu-id="46659-279">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="46659-279">Device is not working properly.</span></span> <span data-ttu-id="46659-280">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="46659-280">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="46659-281">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="46659-281">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-282">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="46659-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46659-283">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-284">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="46659-284">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="46659-285">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="46659-285">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="46659-286">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-287">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="46659-287">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-288">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="46659-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46659-289">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-290">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="46659-290">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="46659-291">第一個具象類別的名稱，這個類別會出現在建立實例時所用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="46659-291">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="46659-292">當搭配類別的其他索引鍵屬性使用時，屬性允許唯一識別此類別的所有實例和其子類別。</span><span class="sxs-lookup"><span data-stu-id="46659-292">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="46659-293">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-294">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="46659-294">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-295">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="46659-295">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="46659-296">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-297">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電子目前 \| 的探查 001.5 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ") </span><span class="sxs-lookup"><span data-stu-id="46659-297">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="46659-298">感應器指出的目前值。</span><span class="sxs-lookup"><span data-stu-id="46659-298">Current value indicated by the sensor.</span></span>

<span data-ttu-id="46659-299">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-299">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-300">**說明**</span><span class="sxs-lookup"><span data-stu-id="46659-300">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-301">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="46659-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46659-302">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-303">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="46659-303">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="46659-304">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="46659-304">Description of the object.</span></span>

<span data-ttu-id="46659-305">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-305">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-306">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="46659-306">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-307">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="46659-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46659-308">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-309">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "DeviceId" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="46659-309">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="46659-310">目前探查的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="46659-310">Unique identifier of the current probe.</span></span>

<span data-ttu-id="46659-311">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-312">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="46659-312">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-313">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="46659-313">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46659-314">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46659-315">若 **為 TRUE**，則表示 **LastErrorCode** 中回報的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="46659-315">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="46659-316">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-317">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="46659-317">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-318">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="46659-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46659-319">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46659-320">**LastErrorCode** 中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="46659-320">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="46659-321">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-321">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="46659-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-323">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="46659-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="46659-324">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-325">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="46659-325">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="46659-326">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="46659-326">Date and time the object was installed.</span></span> <span data-ttu-id="46659-327">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="46659-327">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="46659-328">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-328">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-329">**IsLinear**</span><span class="sxs-lookup"><span data-stu-id="46659-329">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-330">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="46659-330">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46659-331">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46659-332">若 **為 TRUE**，表示感應器在其動態範圍內是線性的。</span><span class="sxs-lookup"><span data-stu-id="46659-332">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="46659-333">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-333">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-334">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="46659-334">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-335">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="46659-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46659-336">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46659-337">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="46659-337">Last error code reported by the logical device.</span></span>

<span data-ttu-id="46659-338">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-338">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-339">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="46659-339">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-340">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="46659-340">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="46659-341">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-342">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電子目前 \| 的探查 001.13 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ") </span><span class="sxs-lookup"><span data-stu-id="46659-342">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.13"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="46659-343">感應器閾值會指定 (最小值和最大值的範圍，) 判斷感應器是否在正常、非關鍵性、重大或嚴重狀況下運作。</span><span class="sxs-lookup"><span data-stu-id="46659-343">Sensor threshold values specify the ranges (minimum and maximum values) to determine whether or not the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="46659-344">如果 **CurrentReading** 介於 **LowerThresholdCritical** 和 **LowerThresholdFatal** 之間，則目前的狀態為「嚴重」。</span><span class="sxs-lookup"><span data-stu-id="46659-344">If **CurrentReading** is between **LowerThresholdCritical** and **LowerThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="46659-345">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-345">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-346">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="46659-346">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-347">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="46659-347">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="46659-348">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-349">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電子目前 \| 的探查 001.15 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ") </span><span class="sxs-lookup"><span data-stu-id="46659-349">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="46659-350">感應器的閾值會指定範圍 (最小值和最大值) ，以判斷感應器是否在正常、非關鍵性、重大或嚴重狀況下運作。</span><span class="sxs-lookup"><span data-stu-id="46659-350">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="46659-351">如果 **CurrentReading** 低於 **LowerThresholdFatal**，則目前的狀態為「嚴重」。</span><span class="sxs-lookup"><span data-stu-id="46659-351">If **CurrentReading** is below **LowerThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="46659-352">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-352">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-353">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="46659-353">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-354">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="46659-354">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="46659-355">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-356">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電子目前 \| 的探查 001.11 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ") </span><span class="sxs-lookup"><span data-stu-id="46659-356">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="46659-357">感應器的閾值會指定範圍 (最小值和最大值) ，以判斷感應器是否在正常、非關鍵性、重大或嚴重狀況下運作。</span><span class="sxs-lookup"><span data-stu-id="46659-357">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="46659-358">如果 **CurrentReading** 介於 **LowerThresholdNonCritical** 和 **UpperThresholdNonCritical** 之間，則感應器會回報正常值。</span><span class="sxs-lookup"><span data-stu-id="46659-358">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="46659-359">如果 **CurrentReading** 介於 **LowerThresholdNonCritical** 和 **LowerThresholdCritical** 之間，則目前的狀態為非關鍵性。</span><span class="sxs-lookup"><span data-stu-id="46659-359">If **CurrentReading** is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="46659-360">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-360">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-361">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="46659-361">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-362">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="46659-362">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="46659-363">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-364">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電子目前 \| 的探查 001.9 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ") </span><span class="sxs-lookup"><span data-stu-id="46659-364">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="46659-365">數值感應器可讀取之已測量屬性的最大值。</span><span class="sxs-lookup"><span data-stu-id="46659-365">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="46659-366">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-366">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-367">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="46659-367">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-368">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="46659-368">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="46659-369">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-370">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電子目前 \| 的探查 001.10 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ") </span><span class="sxs-lookup"><span data-stu-id="46659-370">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="46659-371">數值感應器可讀取之已測量屬性的最小值。</span><span class="sxs-lookup"><span data-stu-id="46659-371">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="46659-372">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-372">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-373">**名稱**</span><span class="sxs-lookup"><span data-stu-id="46659-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-374">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="46659-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46659-375">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-376">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="46659-376">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="46659-377">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="46659-377">Label by which the object is known.</span></span> <span data-ttu-id="46659-378">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="46659-378">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="46659-379">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-379">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-380">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="46659-380">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-381">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="46659-381">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="46659-382">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-383">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電子目前 \| 的探查 001.6 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ") </span><span class="sxs-lookup"><span data-stu-id="46659-383">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="46659-384">數值感應器的一般或預期值。</span><span class="sxs-lookup"><span data-stu-id="46659-384">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="46659-385">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-385">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-386">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="46659-386">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-387">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="46659-387">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="46659-388">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-389">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電子目前 \| 的探查 001.7 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ") </span><span class="sxs-lookup"><span data-stu-id="46659-389">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="46659-390">數值感應器的一般或預期值。</span><span class="sxs-lookup"><span data-stu-id="46659-390">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="46659-391">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-391">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-392">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="46659-392">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-393">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="46659-393">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="46659-394">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-395">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電子目前 \| 的探查 001.8 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ") </span><span class="sxs-lookup"><span data-stu-id="46659-395">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="46659-396">使用者的指引，以取得數值感應器的一般最小範圍。</span><span class="sxs-lookup"><span data-stu-id="46659-396">Guidance for the user as to the normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="46659-397">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-397">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-398">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="46659-398">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-399">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="46659-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46659-400">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-401">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="46659-401">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="46659-402">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="46659-402">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="46659-403">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-403">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="46659-404">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="46659-404">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="46659-405">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="46659-405">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-406">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="46659-406">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="46659-407">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46659-408">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="46659-408">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="46659-409">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="46659-409">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="46659-410"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="46659-410"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="46659-411"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="46659-411"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="46659-412"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="46659-412"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="46659-413"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="46659-413"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="46659-414">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="46659-414">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="46659-415"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="46659-415"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="46659-416">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="46659-416">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="46659-417"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="46659-417"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="46659-418">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="46659-418">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="46659-419">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="46659-419">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="46659-420">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="46659-420">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="46659-421"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="46659-421"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="46659-422">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="46659-422">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="46659-423"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="46659-423"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="46659-424">支援計時 Power-On</span><span class="sxs-lookup"><span data-stu-id="46659-424">Timed Power-On Supported</span></span>

<span data-ttu-id="46659-425">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="46659-425">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="46659-426">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="46659-426">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-427">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="46659-427">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46659-428">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46659-429">若 **為 TRUE**，則裝置可以是電源管理 (可進入暫停模式，依此類推) 。</span><span class="sxs-lookup"><span data-stu-id="46659-429">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="46659-430">屬性不表示電源管理功能目前已啟用，只有邏輯裝置能夠進行電源管理。</span><span class="sxs-lookup"><span data-stu-id="46659-430">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="46659-431">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-432">**解決方法**</span><span class="sxs-lookup"><span data-stu-id="46659-432">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-433">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="46659-433">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46659-434">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-435">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電子目前 \| 的探查 001.17 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 十分之一 of milliamps ") </span><span class="sxs-lookup"><span data-stu-id="46659-435">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="46659-436">感應器解決測量屬性差異的能力。</span><span class="sxs-lookup"><span data-stu-id="46659-436">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="46659-437">此值可能會根據裝置的動態範圍是否為線性而有所不同。</span><span class="sxs-lookup"><span data-stu-id="46659-437">This value may vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="46659-438">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-438">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-439">**狀態**</span><span class="sxs-lookup"><span data-stu-id="46659-439">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-440">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="46659-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46659-441">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-442">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="46659-442">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="46659-443">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="46659-443">Current status of the object.</span></span> <span data-ttu-id="46659-444">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="46659-444">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="46659-445">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="46659-445">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="46659-446">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="46659-446">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="46659-447">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="46659-447">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="46659-448">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="46659-448">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="46659-449">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-449">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="46659-450">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="46659-450">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="46659-451">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="46659-451">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="46659-452">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="46659-452">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="46659-453">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="46659-453">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="46659-454">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="46659-454">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="46659-455">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="46659-455">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="46659-456">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="46659-456">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="46659-457">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="46659-457">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="46659-458">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="46659-458">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="46659-459">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="46659-459">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="46659-460">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="46659-460">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="46659-461">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="46659-461">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="46659-462">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="46659-462">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="46659-463">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="46659-463">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-464">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="46659-464">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="46659-465">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-465">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-466">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="46659-466">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="46659-467">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="46659-467">State of the logical device.</span></span> <span data-ttu-id="46659-468">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="46659-468">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="46659-469">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-469">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="46659-470">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="46659-470">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="46659-471">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="46659-471">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="46659-472">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="46659-472">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="46659-473">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="46659-473">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="46659-474">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="46659-474">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="46659-475">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="46659-475">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-476">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="46659-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46659-477">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-478">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="46659-478">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="46659-479">範圍電腦之 **CreationClassName** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="46659-479">Value for the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="46659-480">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-480">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-481">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="46659-481">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-482">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="46659-482">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46659-483">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-483">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-484">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="46659-484">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="46659-485">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="46659-485">Name of the scoping system.</span></span>

<span data-ttu-id="46659-486">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-486">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-487">**寬容**</span><span class="sxs-lookup"><span data-stu-id="46659-487">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-488">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="46659-488">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="46659-489">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-489">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-490">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電子目前 \| 的探查 001.18 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ") </span><span class="sxs-lookup"><span data-stu-id="46659-490">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.18"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="46659-491">測量屬性之感應器的容錯。</span><span class="sxs-lookup"><span data-stu-id="46659-491">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="46659-492">容錯功能以及解析度和精確度，可用來計算測量實體屬性的實際值。</span><span class="sxs-lookup"><span data-stu-id="46659-492">Tolerance, along with resolution and accuracy, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="46659-493">容錯可能會根據裝置的動態範圍是否為線性而有所不同。</span><span class="sxs-lookup"><span data-stu-id="46659-493">Tolerance may vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="46659-494">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-494">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-495">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="46659-495">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-496">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="46659-496">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="46659-497">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-497">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-498">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電子目前 \| 的探查 001.14 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ") </span><span class="sxs-lookup"><span data-stu-id="46659-498">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="46659-499">感應器的閾值會指定範圍 (最小值和最大值) ，以判斷感應器是否在正常、非關鍵性、重大或嚴重狀況下運作。</span><span class="sxs-lookup"><span data-stu-id="46659-499">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="46659-500">如果 **CurrentReading** 介於 **UpperThresholdCritical** 和 **UpperThresholdFatal** 之間，則目前的狀態為「嚴重」。</span><span class="sxs-lookup"><span data-stu-id="46659-500">If **CurrentReading** is between **UpperThresholdCritical** and **UpperThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="46659-501">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-501">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-502">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="46659-502">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-503">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="46659-503">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="46659-504">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-504">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-505">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電子目前 \| 的探查 001.16 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ") </span><span class="sxs-lookup"><span data-stu-id="46659-505">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="46659-506">感應器的閾值會指定範圍 (最小值和最大值) ，以判斷感應器是否在正常、非關鍵性、重大或嚴重狀況下運作。</span><span class="sxs-lookup"><span data-stu-id="46659-506">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="46659-507">如果 **CurrentReading** 超過 **UpperThresholdFatal**，則目前的狀態為「嚴重」。</span><span class="sxs-lookup"><span data-stu-id="46659-507">If **CurrentReading** is above **UpperThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="46659-508">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-508">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="46659-509">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="46659-509">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46659-510">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="46659-510">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="46659-511">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46659-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46659-512">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電子目前 \| 的探查 001.12 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ") </span><span class="sxs-lookup"><span data-stu-id="46659-512">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="46659-513">感應器的閾值會指定範圍 (最小值和最大值) ，以判斷感應器是否在正常、非關鍵性、重大或嚴重狀況下運作。</span><span class="sxs-lookup"><span data-stu-id="46659-513">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="46659-514">如果 **CurrentReading** 介於 **LowerThresholdNonCritical** 和 **UpperThresholdNonCritical** 之間，則感應器會回報正常值。</span><span class="sxs-lookup"><span data-stu-id="46659-514">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="46659-515">如果 **CurrentReading** 介於 **UpperThresholdNonCritical** 和 **UpperThresholdCritical** 之間，則目前的狀態為非關鍵性。</span><span class="sxs-lookup"><span data-stu-id="46659-515">If **CurrentReading** is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="46659-516">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-516">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46659-517">備註</span><span class="sxs-lookup"><span data-stu-id="46659-517">Remarks</span></span>

<span data-ttu-id="46659-518">**Win32 \_ CurrentProbe** 類別衍生自 [**CIM \_ CurrentSensor**](cim-currentsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="46659-518">The **Win32\_CurrentProbe** class is derived from [**CIM\_CurrentSensor**](cim-currentsensor.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="46659-519">規格需求</span><span class="sxs-lookup"><span data-stu-id="46659-519">Requirements</span></span>



| <span data-ttu-id="46659-520">需求</span><span class="sxs-lookup"><span data-stu-id="46659-520">Requirement</span></span> | <span data-ttu-id="46659-521">值</span><span class="sxs-lookup"><span data-stu-id="46659-521">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46659-522">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46659-522">Minimum supported client</span></span><br/> | <span data-ttu-id="46659-523">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46659-523">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="46659-524">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46659-524">Minimum supported server</span></span><br/> | <span data-ttu-id="46659-525">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46659-525">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="46659-526">命名空間</span><span class="sxs-lookup"><span data-stu-id="46659-526">Namespace</span></span><br/>                | <span data-ttu-id="46659-527">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="46659-527">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="46659-528">MOF</span><span class="sxs-lookup"><span data-stu-id="46659-528">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46659-529"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="46659-529"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="46659-530">DLL</span><span class="sxs-lookup"><span data-stu-id="46659-530">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46659-531"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46659-531"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46659-532">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46659-532">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46659-533">**CIM \_ CurrentSensor**</span><span class="sxs-lookup"><span data-stu-id="46659-533">**CIM\_CurrentSensor**</span></span>](cim-currentsensor.md)
</dt> <dt>

[<span data-ttu-id="46659-534">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="46659-534">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

