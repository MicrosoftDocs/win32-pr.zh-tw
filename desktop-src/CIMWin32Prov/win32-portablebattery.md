---
description: Win32 \_ PORTABLEBATTERY WMI 類別包含便攜電池的相關屬性，例如筆記本電腦電池。
ms.assetid: ca7d061f-8fc6-4a1e-aa75-2465ce5e2735
ms.tgt_platform: multiple
title: Win32_PortableBattery 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PortableBattery
- Win32_PortableBattery.Reset
- Win32_PortableBattery.SetPowerState
- Win32_PortableBattery.Availability
- Win32_PortableBattery.BatteryStatus
- Win32_PortableBattery.CapacityMultiplier
- Win32_PortableBattery.Caption
- Win32_PortableBattery.Chemistry
- Win32_PortableBattery.ConfigManagerErrorCode
- Win32_PortableBattery.ConfigManagerUserConfig
- Win32_PortableBattery.CreationClassName
- Win32_PortableBattery.Description
- Win32_PortableBattery.DesignCapacity
- Win32_PortableBattery.DesignVoltage
- Win32_PortableBattery.DeviceID
- Win32_PortableBattery.ErrorCleared
- Win32_PortableBattery.ErrorDescription
- Win32_PortableBattery.EstimatedChargeRemaining
- Win32_PortableBattery.EstimatedRunTime
- Win32_PortableBattery.ExpectedBatteryLife
- Win32_PortableBattery.ExpectedLife
- Win32_PortableBattery.FullChargeCapacity
- Win32_PortableBattery.InstallDate
- Win32_PortableBattery.LastErrorCode
- Win32_PortableBattery.Location
- Win32_PortableBattery.ManufactureDate
- Win32_PortableBattery.Manufacturer
- Win32_PortableBattery.MaxBatteryError
- Win32_PortableBattery.MaxRechargeTime
- Win32_PortableBattery.Name
- Win32_PortableBattery.PNPDeviceID
- Win32_PortableBattery.PowerManagementCapabilities
- Win32_PortableBattery.PowerManagementSupported
- Win32_PortableBattery.SmartBatteryVersion
- Win32_PortableBattery.Status
- Win32_PortableBattery.StatusInfo
- Win32_PortableBattery.SystemCreationClassName
- Win32_PortableBattery.SystemName
- Win32_PortableBattery.TimeOnBattery
- Win32_PortableBattery.TimeToFullCharge
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9db875e7e4d1736cf45945b53f2f20fec0490a47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688632"
---
# <a name="win32_portablebattery-class"></a><span data-ttu-id="7ea2a-103">Win32 \_ PortableBattery 類別</span><span class="sxs-lookup"><span data-stu-id="7ea2a-103">Win32\_PortableBattery class</span></span>

<span data-ttu-id="7ea2a-104">**Win32 \_ PortableBattery** [WMI 類別](../wmisdk/retrieving-a-class.md)包含便攜電池的相關屬性，例如筆記本電腦電池。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-104">The **Win32\_PortableBattery** [WMI class](../wmisdk/retrieving-a-class.md) contains the properties related to a portable battery, such as a notebook computer battery.</span></span>

<span data-ttu-id="7ea2a-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7ea2a-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ea2a-107">語法</span><span class="sxs-lookup"><span data-stu-id="7ea2a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PortableBattery : CIM_Battery
{
  uint16   Availability;
  uint16   BatteryStatus;
  uint16   CapacityMultiplier;
  string   Caption;
  uint16   Chemistry;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  uint32   DesignCapacity;
  uint64   DesignVoltage;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   EstimatedChargeRemaining;
  uint32   EstimatedRunTime;
  uint32   ExpectedBatteryLife;
  uint32   ExpectedLife;
  uint32   FullChargeCapacity;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Location;
  string   ManufactureDate;
  string   Manufacturer;
  uint16   MaxBatteryError;
  uint32   MaxRechargeTime;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   SmartBatteryVersion;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TimeOnBattery;
  uint32   TimeToFullCharge;
};
```

## <a name="members"></a><span data-ttu-id="7ea2a-108">成員</span><span class="sxs-lookup"><span data-stu-id="7ea2a-108">Members</span></span>

<span data-ttu-id="7ea2a-109">**Win32 \_ PortableBattery** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7ea2a-109">The **Win32\_PortableBattery** class has these types of members:</span></span>

-   [<span data-ttu-id="7ea2a-110">方法</span><span class="sxs-lookup"><span data-stu-id="7ea2a-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="7ea2a-111">屬性</span><span class="sxs-lookup"><span data-stu-id="7ea2a-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7ea2a-112">方法</span><span class="sxs-lookup"><span data-stu-id="7ea2a-112">Methods</span></span>

<span data-ttu-id="7ea2a-113">**Win32 \_ PortableBattery** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-113">The **Win32\_PortableBattery** class has these methods.</span></span>



| <span data-ttu-id="7ea2a-114">方法</span><span class="sxs-lookup"><span data-stu-id="7ea2a-114">Method</span></span>            | <span data-ttu-id="7ea2a-115">描述</span><span class="sxs-lookup"><span data-stu-id="7ea2a-115">Description</span></span>                                                                                                                                                                        |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ea2a-116">**重設**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-116">**Reset**</span></span>         | <span data-ttu-id="7ea2a-117">未實作。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-117">Not implemented.</span></span> <span data-ttu-id="7ea2a-118">若要執行此方法，請參閱 [**CIM \_ 電池**](cim-battery.md)中的 [**Reset**](reset-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md).</span></span><br/>                 |
| <span data-ttu-id="7ea2a-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-119">**SetPowerState**</span></span> | <span data-ttu-id="7ea2a-120">未實作。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-120">Not implemented.</span></span> <span data-ttu-id="7ea2a-121">若要執行此方法，請參閱 [**CIM \_ 電池**](cim-battery.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7ea2a-122">屬性</span><span class="sxs-lookup"><span data-stu-id="7ea2a-122">Properties</span></span>

<span data-ttu-id="7ea2a-123">**Win32 \_ PortableBattery** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-123">The **Win32\_PortableBattery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7ea2a-124">**可用性**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-125">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-127">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="7ea2a-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-128">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-128">Availability and status of the device.</span></span>

<span data-ttu-id="7ea2a-129">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7ea2a-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7ea2a-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="7ea2a-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-133">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="7ea2a-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="7ea2a-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="7ea2a-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7ea2a-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="7ea2a-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="7ea2a-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="7ea2a-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="7ea2a-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7ea2a-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="7ea2a-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="7ea2a-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="7ea2a-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-144">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="7ea2a-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-146">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="7ea2a-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-148">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="7ea2a-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="7ea2a-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-151">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="7ea2a-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-153">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="7ea2a-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-155">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="7ea2a-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-157">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="7ea2a-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-159">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7ea2a-160">**BatteryStatus**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-160">**BatteryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-161">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-163">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 便攜電池 \| 002.14」 ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.14")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-164">電池充電狀態的描述。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-164">Description of the battery's charge status.</span></span> <span data-ttu-id="7ea2a-165">在通用訊息模型 (CIM) 架構中，值 10 (未定義的) 無效，因為在桌面管理介面 (DMI) 它指出沒有安裝電池。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-165">The value 10 (Undefined) is not valid in the Common Information Model (CIM) schema because in Desktop Management Interface (DMI) it indicates that no battery is installed.</span></span> <span data-ttu-id="7ea2a-166">在此情況下，不應將這個物件具現化。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-166">In this case, this object should not be instantiated.</span></span>

<span data-ttu-id="7ea2a-167">這個屬性繼承自 [**CIM \_ 電池**](cim-battery.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-167">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7ea2a-168">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-168">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7ea2a-169">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-169">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>

<span data-ttu-id="7ea2a-170"> (3) **完全收費**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-170">**Fully Charged** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="7ea2a-171">**低** (4) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-171">**Low** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="7ea2a-172">**重大** (5) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-172">**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>

<span data-ttu-id="7ea2a-173">**充電** (6) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-173">**Charging** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>

<span data-ttu-id="7ea2a-174">**充電和高** (7) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-174">**Charging and High** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>

<span data-ttu-id="7ea2a-175">**充電和低** (8) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-175">**Charging and Low** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>

<span data-ttu-id="7ea2a-176">**充電和重大** (9) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-176">**Charging and Critical** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="7ea2a-177">**未定義** (10) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-177">**Undefined** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>

<span data-ttu-id="7ea2a-178">**部分計費** (11) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-178">**Partially Charged** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7ea2a-179">**CapacityMultiplier**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-179">**CapacityMultiplier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-180">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-182">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 22 \| Design 容量乘數" ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-182">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Design Capacity Multiplier")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-183">**DesignCapacity** 值的乘法因數，以確保毫瓦小時值不會在智慧電池資料規格 (SBDS) 的情況溢位。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-183">Multiplication factor of the **DesignCapacity** value to ensure that the milliwatt hour value does not overflow for Smart Battery Data Specification (SBDS) implementations.</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-184">**標題**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-185">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-187">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-187">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-188">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-188">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="7ea2a-189">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-190">**化學**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-190">**Chemistry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-191">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-193">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 便攜電池 \| 002.7」 ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-193">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-194">電池化學。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-194">Chemistry of the battery.</span></span>

<span data-ttu-id="7ea2a-195">這個屬性繼承自 [**CIM \_ 電池**](cim-battery.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-195">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7ea2a-196">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-196">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7ea2a-197">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-197">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>

<span data-ttu-id="7ea2a-198">**潛在客戶 Acid** (3) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-198">**Lead Acid** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>

<span data-ttu-id="7ea2a-199">**五分錢鎘** (4) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-199">**Nickel Cadmium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>

<span data-ttu-id="7ea2a-200">**五分錢裸機氫化** (5) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-200">**Nickel Metal Hydride** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>

<span data-ttu-id="7ea2a-201">**鋰離子** (6) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-201">**Lithium-ion** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>

<span data-ttu-id="7ea2a-202">**Zinc air** (7) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-202">**Zinc air** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>

<span data-ttu-id="7ea2a-203">**鋰聚合體** (8) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-203">**Lithium Polymer** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7ea2a-204">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-204">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-205">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-206">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-207">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-207">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-208">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-208">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="7ea2a-209">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-209">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="7ea2a-210"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-210"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="7ea2a-211"> (0)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-211">(0)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-212">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-212">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="7ea2a-213"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-213"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="7ea2a-214">(1)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-214">(1)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-215">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-215">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7ea2a-216"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-216"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="7ea2a-217">(2)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-217">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="7ea2a-218"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-218"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="7ea2a-219">(3)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-219">(3)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-220">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-220">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7ea2a-221"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-221"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="7ea2a-222">(4)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-222">(4)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-223">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-223">Device is not working properly.</span></span> <span data-ttu-id="7ea2a-224">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-224">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="7ea2a-225"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-225"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="7ea2a-226">(5)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-226">(5)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-227">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-227">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="7ea2a-228"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-228"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="7ea2a-229">(6)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-229">(6)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-230">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-230">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="7ea2a-231"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-231"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="7ea2a-232">(7)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-232">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="7ea2a-233"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-233"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="7ea2a-234">(8)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-234">(8)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-235">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-235">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="7ea2a-236"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-236"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="7ea2a-237">(9)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-237">(9)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-238">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-238">Device is not working properly.</span></span> <span data-ttu-id="7ea2a-239">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-239">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="7ea2a-240"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-240"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="7ea2a-241">(10)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-241">(10)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-242">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-242">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="7ea2a-243"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-243"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="7ea2a-244">(11)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-244">(11)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-245">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-245">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="7ea2a-246"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-246"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="7ea2a-247"> (12) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-247">(12)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-248">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-248">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="7ea2a-249"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-249"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="7ea2a-250">(13)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-250">(13)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-251">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-251">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="7ea2a-252"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-252"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="7ea2a-253">(14)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-253">(14)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-254">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-254">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="7ea2a-255"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-255"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="7ea2a-256">(15)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-256">(15)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-257">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-257">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="7ea2a-258"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-258"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="7ea2a-259">(16)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-259">(16)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-260">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-260">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="7ea2a-261"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-261"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="7ea2a-262">(17)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-262">(17)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-263">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-263">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7ea2a-264"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-264"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="7ea2a-265">(18)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-265">(18)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-266">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-266">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="7ea2a-267"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-267"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="7ea2a-268">(19)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-268">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7ea2a-269"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-269"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="7ea2a-270">(20)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-270">(20)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-271">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-271">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="7ea2a-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="7ea2a-273">(21)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-273">(21)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-274">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-274">System failure.</span></span> <span data-ttu-id="7ea2a-275">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-275">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="7ea2a-276">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-276">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="7ea2a-277"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-277"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="7ea2a-278">(22)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-278">(22)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-279">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-279">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="7ea2a-280"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-280"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="7ea2a-281">(23)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-281">(23)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-282">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-282">System failure.</span></span> <span data-ttu-id="7ea2a-283">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-283">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="7ea2a-284"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-284"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="7ea2a-285">(24)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-285">(24)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-286">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-286">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7ea2a-287"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-287"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="7ea2a-288">(25)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-288">(25)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-289">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-289">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7ea2a-290"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-290"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="7ea2a-291">(26)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-291">(26)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-292">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-292">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="7ea2a-293"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-293"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="7ea2a-294">(27)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-294">(27)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-295">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-295">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="7ea2a-296"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-296"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="7ea2a-297">(28)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-297">(28)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-298">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-298">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="7ea2a-299"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-299"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="7ea2a-300">(29)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-300">(29)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-301">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-301">Device is disabled.</span></span> <span data-ttu-id="7ea2a-302">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-302">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="7ea2a-303"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-303"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="7ea2a-304">(30)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-304">(30)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-305">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-305">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7ea2a-306"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-306"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="7ea2a-307"> (31) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-307">(31)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-308">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-308">Device is not working properly.</span></span> <span data-ttu-id="7ea2a-309">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-309">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7ea2a-310">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-310">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-311">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-312">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-313">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-313">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-314">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-314">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="7ea2a-315">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-316">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-316">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-317">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-318">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-319">限定詞： [ **CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-319">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-320">第一個具象類別的名稱，這個類別會出現在建立實例時所用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-320">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="7ea2a-321">搭配類別的其他索引鍵屬性使用時，屬性可讓這個類別的所有實例和其子類別都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-321">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="7ea2a-322">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-323">**說明**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-323">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-324">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-325">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-326">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-326">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-327">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-327">Description of the object.</span></span>

<span data-ttu-id="7ea2a-328">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-328">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-329">**DesignCapacity**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-329">**DesignCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-330">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-331">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-332">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 便攜電池 \| 002.8」 ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "毫瓦-小時" ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-332">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-333">在毫瓦時設計電池的容量。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-333">Design capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="7ea2a-334">如果不支援此屬性，請輸入 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-334">If this property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="7ea2a-335">這個屬性繼承自 [**CIM \_ 電池**](cim-battery.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-335">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-336">**DesignVoltage**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-336">**DesignVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-337">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-337">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-338">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-339">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 便攜電池 \| 002.9」 ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "毫伏" ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-339">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.9"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-340">以毫伏設計的電池電壓。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-340">Design voltage of the battery in millivolts.</span></span> <span data-ttu-id="7ea2a-341">如果不支援此屬性，請輸入 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-341">If this attribute is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="7ea2a-342">這個屬性繼承自 [**CIM \_ 電池**](cim-battery.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-342">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<span data-ttu-id="7ea2a-343">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-343">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-344">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-344">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-345">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-346">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-347">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "DeviceId" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-347">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-348">電池識別碼。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-348">Battery identifier.</span></span>

<span data-ttu-id="7ea2a-349">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="7ea2a-350">範例：「內部電池」</span><span class="sxs-lookup"><span data-stu-id="7ea2a-350">Example: "Internal Battery"</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-351">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-351">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-352">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-352">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-353">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-354">若 **為 TRUE**，則表示 **LastErrorCode** 中回報的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-354">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="7ea2a-355">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-355">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-356">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-356">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-357">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-358">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-359">**LastErrorCode** 中所記錄錯誤的詳細資訊，以及任何可能採取的更正動作。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-359">More information about the error recorded in **LastErrorCode**, and any corrective actions that may be taken.</span></span>

<span data-ttu-id="7ea2a-360">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-361">**EstimatedChargeRemaining**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-361">**EstimatedChargeRemaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-362">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-363">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-364">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( 「百分比」 ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-364">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-365">估計剩餘的完整費用百分比。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-365">Estimate of the percentage of full charge remaining.</span></span>

<span data-ttu-id="7ea2a-366">這個屬性繼承自 [**CIM \_ 電池**](cim-battery.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-366">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-367">**EstimatedRunTime**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-367">**EstimatedRunTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-368">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-369">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-370">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 便攜電池 \| 002.15 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" 分鐘 ") </span><span class="sxs-lookup"><span data-stu-id="7ea2a-370">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.15"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-371">如果公用程式電源關閉、遺失並保持關閉狀態，或膝上型電腦與電源中斷連線，則在目前的負載條件下估計電池計量耗盡的時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-371">Estimate in minutes of the time to battery charge depletion under the present load conditions if the utility power is off, or lost and remains off, or a laptop is disconnected from a power source.</span></span>

<span data-ttu-id="7ea2a-372">這個屬性繼承自 [**CIM \_ 電池**](cim-battery.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-372">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-373">**ExpectedBatteryLife**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-373">**ExpectedBatteryLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-374">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-375">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-376">不支援。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-376">Not supported.</span></span>

<span data-ttu-id="7ea2a-377">這個屬性繼承自 [**CIM \_ 電池**](cim-battery.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-377">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-378">**ExpectedLife**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-378">**ExpectedLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-379">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-379">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-380">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-381">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "分鐘" ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-381">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-382">電池的預期存留期（以分鐘為單位）（假設電池已完全收費）。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-382">Battery's expected lifetime in minutes, assuming that the battery is fully charged.</span></span> <span data-ttu-id="7ea2a-383">此屬性代表電池的預期存留期總計，而不是其目前剩餘的存留期（由 **EstimatedRunTime** 屬性工作表示）。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-383">This property represents the total expected life of the battery, not its current remaining life, which is indicated by the **EstimatedRunTime** property.</span></span>

<span data-ttu-id="7ea2a-384">這個屬性繼承自 [**CIM \_ 電池**](cim-battery.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-384">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-385">**FullChargeCapacity**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-385">**FullChargeCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-386">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-387">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-388">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 便攜電池 \| 002.11」 ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "毫瓦-小時" ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-389">毫瓦-小時內電池的完整收費容量。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-389">Full charge capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="7ea2a-390">此值與 **DesignCapacity** 屬性的比較會決定何時需要更換電池。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-390">Comparison of this value to the **DesignCapacity** property determines when the battery requires replacement.</span></span> <span data-ttu-id="7ea2a-391">電池生命週期結束通常是在 **FullChargeCapacity** 屬性低於80% 的 **DesignCapacity** 屬性。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-391">A battery's end of life is typically when the **FullChargeCapacity** property falls below 80% of the **DesignCapacity** property.</span></span> <span data-ttu-id="7ea2a-392">如果不支援此屬性，請輸入 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-392">If this property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="7ea2a-393">這個屬性繼承自 [**CIM \_ 電池**](cim-battery.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-393">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-394">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-394">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-395">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-395">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-396">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-397">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="7ea2a-397">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-398">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-398">Date and time the object was installed.</span></span> <span data-ttu-id="7ea2a-399">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-399">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="7ea2a-400">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-400">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-401">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-401">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-402">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-402">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-403">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-404">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-404">Last error code reported by the logical device.</span></span>

<span data-ttu-id="7ea2a-405">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-405">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-406">**位置**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-406">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-407">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-408">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-409">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 22 \| Location" ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-409">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Location")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-410">電池的實體位置。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-410">Physical location of the battery.</span></span> <span data-ttu-id="7ea2a-411">這個屬性是由電腦製造商所填滿。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-411">This property is filled by the computer manufacturer.</span></span>

<span data-ttu-id="7ea2a-412">範例：「回到左邊的」</span><span class="sxs-lookup"><span data-stu-id="7ea2a-412">Example: "In the back, on the left"</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-413">**ManufactureDate**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-413">**ManufactureDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-414">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-415">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-416">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「SMBIOS \| Type 22 \| 製造日期」 ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-416">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Manufacture Date")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-417">製造電池的日期。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-417">Date when the battery was manufactured.</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-418">**製造商**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-418">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-419">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-420">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-420">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-421">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 22 \| 製造商" ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-421">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-422">電池的製造商。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-422">Manufacturer of the battery.</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-423">**MaxBatteryError**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-423">**MaxBatteryError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-424">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-425">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-426">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 22 \| Error in 電池 Data" ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "percent" ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-426">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Maximum Error in Battery Data"), [**Units**](../wmisdk/standard-qualifiers.md) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-427">電池所剩的最高預估能源量與電池所報告的目前數量之間的差異。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-427">Difference between the highest estimated amount of energy left in the battery and the current amount reported by the battery.</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-428">**MaxRechargeTime**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-428">**MaxRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-429">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-429">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-430">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-431">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "分鐘" ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-431">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-432">完全充電電池的最長時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-432">Maximum time, in minutes, to fully charge the battery.</span></span> <span data-ttu-id="7ea2a-433">此屬性代表將完全耗盡的電池充電的時間，而不是目前剩餘的費用時間（在 **TimeToFullCharge** 屬性中表示）。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-433">This property represents the time to recharge a fully depleted battery, not the current remaining charge time, which is indicated in the **TimeToFullCharge** property.</span></span>

<span data-ttu-id="7ea2a-434">這個屬性繼承自 [**CIM \_ 電池**](cim-battery.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-434">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-435">**名稱**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-435">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-436">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-437">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-438">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-438">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-439">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-439">Label by which the object is known.</span></span> <span data-ttu-id="7ea2a-440">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-440">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="7ea2a-441">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-441">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-442">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-442">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-443">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-444">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-445">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-445">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-446">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-446">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="7ea2a-447">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-447">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="7ea2a-448">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="7ea2a-448">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-449">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-449">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-450">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="7ea2a-450">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-451">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-452">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-452">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="7ea2a-453">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-453">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7ea2a-454"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-454"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="7ea2a-455"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-455"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7ea2a-456"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-456"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7ea2a-457"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-457"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-458">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-458">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="7ea2a-459"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-459"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-460">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-460">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="7ea2a-461"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-461"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-462">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-462">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="7ea2a-463">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-463">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="7ea2a-464">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](../wmisdk/designing-managed-object-format--mof--classes.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-464">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="7ea2a-465"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-465"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-466">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-466">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="7ea2a-467"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-467"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="7ea2a-468">支援計時 Power-On</span><span class="sxs-lookup"><span data-stu-id="7ea2a-468">Timed Power-On Supported</span></span>

<span data-ttu-id="7ea2a-469">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-469">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7ea2a-470">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-470">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-471">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-471">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-472">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-473">若 **為 TRUE**，則裝置可以是電源管理 (可進入暫停模式，依此類推) 。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-473">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="7ea2a-474">屬性不表示電源管理功能目前已啟用，只有邏輯裝置能夠進行電源管理。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-474">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="7ea2a-475">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-475">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-476">**SmartBatteryVersion**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-476">**SmartBatteryVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-477">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-478">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-479">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) (」 MIF。DMTF \| 便攜電池 \| 002.10」 ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-479">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.10")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-480">此電池支援的智慧型電池資料規格版本號碼。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-480">Smart Battery Data Specification version number supported by this battery.</span></span> <span data-ttu-id="7ea2a-481">如果電池不支援此功能，此值應保留空白。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-481">If the battery does not support this function, the value should be left blank.</span></span>

<span data-ttu-id="7ea2a-482">這個屬性繼承自 [**CIM \_ 電池**](cim-battery.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-482">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-483">**狀態**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-483">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-484">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-485">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-485">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-486">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-486">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-487">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-487">Current status of the object.</span></span> <span data-ttu-id="7ea2a-488">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-488">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="7ea2a-489">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-489">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="7ea2a-490">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-490">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7ea2a-491">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-491">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7ea2a-492">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-492">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7ea2a-493">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-493">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7ea2a-494">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="7ea2a-494">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7ea2a-495">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-495">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7ea2a-496">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-496">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7ea2a-497">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-497">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7ea2a-498">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-498">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7ea2a-499">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-499">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7ea2a-500">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-500">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7ea2a-501">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-501">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7ea2a-502">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-502">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7ea2a-503">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-503">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7ea2a-504">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-504">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7ea2a-505">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-505">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7ea2a-506">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-506">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7ea2a-507">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-507">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-508">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-508">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-509">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-510">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="7ea2a-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-511">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-511">State of the logical device.</span></span> <span data-ttu-id="7ea2a-512">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-512">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="7ea2a-513">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-513">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7ea2a-514">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-514">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7ea2a-515">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-515">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7ea2a-516">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-516">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7ea2a-517">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-517">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7ea2a-518">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-518">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7ea2a-519">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-519">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-520">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-521">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-522">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-522">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-523">範圍電腦之 **CreationClassName** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-523">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="7ea2a-524">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-524">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-525">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-525">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-526">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-527">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-527">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-528">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="7ea2a-528">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-529">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-529">Name of the scoping system.</span></span>

<span data-ttu-id="7ea2a-530">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-530">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-531">**TimeOnBattery**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-531">**TimeOnBattery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-532">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-532">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-533">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-533">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-534">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( 「秒」 ) </span><span class="sxs-lookup"><span data-stu-id="7ea2a-534">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-535">電腦系統 UPS 上一次切換到電池電源，或自系統或 UPS 上一次重新開機之後的時間（以較小者為准）的經過時間（秒）。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-535">Elapsed time in seconds since the computer system's UPS last switched to battery power, or the time since the system or UPS was last restarted, whichever is less.</span></span> <span data-ttu-id="7ea2a-536">如果電池已上線，則會傳回 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-536">If the battery is online, 0 (zero) is returned.</span></span>

<span data-ttu-id="7ea2a-537">這個屬性繼承自 [**CIM \_ 電池**](cim-battery.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-537">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ea2a-538">**TimeToFullCharge**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-538">**TimeToFullCharge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ea2a-539">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-539">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-540">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ea2a-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ea2a-541">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 便攜電池 \| 002.16 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" 分鐘 ") </span><span class="sxs-lookup"><span data-stu-id="7ea2a-541">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.16"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="7ea2a-542">以目前的費率和使用量為單位的剩餘時間（以分鐘為單位），完全收取電池費用。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-542">Remaining time in minutes to charge the battery fully at the current charge rate and usage.</span></span>

<span data-ttu-id="7ea2a-543">這個屬性繼承自 [**CIM \_ 電池**](cim-battery.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-543">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ea2a-544">備註</span><span class="sxs-lookup"><span data-stu-id="7ea2a-544">Remarks</span></span>

<span data-ttu-id="7ea2a-545">**Win32 \_ PortableBattery** 類別衍生自 [**CIM \_ 電池**](cim-battery.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea2a-545">The **Win32\_PortableBattery** class is derived from [**CIM\_Battery**](cim-battery.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ea2a-546">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ea2a-546">Requirements</span></span>



| <span data-ttu-id="7ea2a-547">需求</span><span class="sxs-lookup"><span data-stu-id="7ea2a-547">Requirement</span></span> | <span data-ttu-id="7ea2a-548">值</span><span class="sxs-lookup"><span data-stu-id="7ea2a-548">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ea2a-549">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7ea2a-549">Minimum supported client</span></span><br/> | <span data-ttu-id="7ea2a-550">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7ea2a-550">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7ea2a-551">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7ea2a-551">Minimum supported server</span></span><br/> | <span data-ttu-id="7ea2a-552">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ea2a-552">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7ea2a-553">命名空間</span><span class="sxs-lookup"><span data-stu-id="7ea2a-553">Namespace</span></span><br/>                | <span data-ttu-id="7ea2a-554">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7ea2a-554">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7ea2a-555">MOF</span><span class="sxs-lookup"><span data-stu-id="7ea2a-555">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ea2a-556"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="7ea2a-556"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ea2a-557">DLL</span><span class="sxs-lookup"><span data-stu-id="7ea2a-557">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ea2a-558"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ea2a-558"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ea2a-559">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ea2a-559">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ea2a-560">**CIM \_ 電池**</span><span class="sxs-lookup"><span data-stu-id="7ea2a-560">**CIM\_Battery**</span></span>](cim-battery.md)
</dt> <dt>

[<span data-ttu-id="7ea2a-561">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="7ea2a-561">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
