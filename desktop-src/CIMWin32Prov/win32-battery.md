---
description: 代表連接到電腦系統的電池。
ms.assetid: b07ccb1d-008e-4bf1-8299-33706cbcbaee
ms.tgt_platform: multiple
title: Win32_Battery 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Battery
- Win32_Battery.Reset
- Win32_Battery.SetPowerState
- Win32_Battery.Availability
- Win32_Battery.BatteryRechargeTime
- Win32_Battery.BatteryStatus
- Win32_Battery.Caption
- Win32_Battery.Chemistry
- Win32_Battery.ConfigManagerErrorCode
- Win32_Battery.ConfigManagerUserConfig
- Win32_Battery.CreationClassName
- Win32_Battery.Description
- Win32_Battery.DesignCapacity
- Win32_Battery.DesignVoltage
- Win32_Battery.DeviceID
- Win32_Battery.ErrorCleared
- Win32_Battery.ErrorDescription
- Win32_Battery.EstimatedChargeRemaining
- Win32_Battery.EstimatedRunTime
- Win32_Battery.ExpectedBatteryLife
- Win32_Battery.ExpectedLife
- Win32_Battery.FullChargeCapacity
- Win32_Battery.InstallDate
- Win32_Battery.LastErrorCode
- Win32_Battery.MaxRechargeTime
- Win32_Battery.Name
- Win32_Battery.PNPDeviceID
- Win32_Battery.PowerManagementCapabilities
- Win32_Battery.PowerManagementSupported
- Win32_Battery.SmartBatteryVersion
- Win32_Battery.Status
- Win32_Battery.StatusInfo
- Win32_Battery.SystemCreationClassName
- Win32_Battery.SystemName
- Win32_Battery.TimeOnBattery
- Win32_Battery.TimeToFullCharge
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 75477bcf670bcc0cf16c63f130f95d4c38d7b783
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026002"
---
# <a name="win32_battery-class"></a><span data-ttu-id="83a78-103">Win32 \_ 電池類別</span><span class="sxs-lookup"><span data-stu-id="83a78-103">Win32\_Battery class</span></span>

<span data-ttu-id="83a78-104">**Win32 \_ 電池** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表連接到電腦系統的電池。</span><span class="sxs-lookup"><span data-stu-id="83a78-104">The **Win32\_Battery** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a battery connected to the computer system.</span></span>

<span data-ttu-id="83a78-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="83a78-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="83a78-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="83a78-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="83a78-107">語法</span><span class="sxs-lookup"><span data-stu-id="83a78-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Battery : CIM_Battery
{
  uint16   Availability;
  uint32   BatteryRechargeTime;
  uint16   BatteryStatus;
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

## <a name="members"></a><span data-ttu-id="83a78-108">成員</span><span class="sxs-lookup"><span data-stu-id="83a78-108">Members</span></span>

<span data-ttu-id="83a78-109">**Win32 \_ 電池** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="83a78-109">The **Win32\_Battery** class has these types of members:</span></span>

-   [<span data-ttu-id="83a78-110">方法</span><span class="sxs-lookup"><span data-stu-id="83a78-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="83a78-111">屬性</span><span class="sxs-lookup"><span data-stu-id="83a78-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="83a78-112">方法</span><span class="sxs-lookup"><span data-stu-id="83a78-112">Methods</span></span>

<span data-ttu-id="83a78-113">**Win32 \_ 電池** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="83a78-113">The **Win32\_Battery** class has these methods.</span></span>



| <span data-ttu-id="83a78-114">方法</span><span class="sxs-lookup"><span data-stu-id="83a78-114">Method</span></span>            | <span data-ttu-id="83a78-115">描述</span><span class="sxs-lookup"><span data-stu-id="83a78-115">Description</span></span>                                                                                                                                                                                          |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83a78-116">**重設**</span><span class="sxs-lookup"><span data-stu-id="83a78-116">**Reset**</span></span>         | <span data-ttu-id="83a78-117">未實作。</span><span class="sxs-lookup"><span data-stu-id="83a78-117">Not implemented.</span></span> <span data-ttu-id="83a78-118">若要執行此方法，請參閱 [**CIM \_ 電池**](cim-battery.md)中的 [**Reset**](reset-method-in-class-cim-controller.md)方法以取得檔。</span><span class="sxs-lookup"><span data-stu-id="83a78-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="83a78-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="83a78-119">**SetPowerState**</span></span> | <span data-ttu-id="83a78-120">未實作。</span><span class="sxs-lookup"><span data-stu-id="83a78-120">Not implemented.</span></span> <span data-ttu-id="83a78-121">若要執行此方法，請參閱 [**CIM \_ 電池**](cim-battery.md)中適用于檔的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="83a78-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="83a78-122">屬性</span><span class="sxs-lookup"><span data-stu-id="83a78-122">Properties</span></span>

<span data-ttu-id="83a78-123">**Win32 \_ 電池** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="83a78-123">The **Win32\_Battery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="83a78-124">**可用性**</span><span class="sxs-lookup"><span data-stu-id="83a78-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-125">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="83a78-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-127">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="83a78-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="83a78-128">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="83a78-128">Availability and status of the device.</span></span>

<span data-ttu-id="83a78-129">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="83a78-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="83a78-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="83a78-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="83a78-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="83a78-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="83a78-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-133">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="83a78-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="83a78-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="83a78-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="83a78-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="83a78-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="83a78-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="83a78-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="83a78-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="83a78-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="83a78-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="83a78-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="83a78-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="83a78-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="83a78-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="83a78-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="83a78-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="83a78-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="83a78-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="83a78-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="83a78-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="83a78-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-144">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="83a78-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="83a78-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="83a78-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-146">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="83a78-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="83a78-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="83a78-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-148">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="83a78-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="83a78-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="83a78-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="83a78-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="83a78-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-151">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="83a78-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="83a78-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="83a78-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-153">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="83a78-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="83a78-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="83a78-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-155">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="83a78-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="83a78-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="83a78-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-157">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="83a78-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="83a78-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="83a78-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-159">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="83a78-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="83a78-160">**BatteryRechargeTime**</span><span class="sxs-lookup"><span data-stu-id="83a78-160">**BatteryRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-161">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="83a78-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-163">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "HKEY \_ LOCAL \_ MACHINE \\ \\ System \\ \\ CurrentControlSet \\ \\ Services \| RechargeRate" ) ，[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "分鐘" ) </span><span class="sxs-lookup"><span data-stu-id="83a78-163">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("HKEY\_LOCAL\_MACHINE\\\\System\\\\CurrentControlSet\\\\Services\|RechargeRate"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="83a78-164">完全充電電池所需的時間。</span><span class="sxs-lookup"><span data-stu-id="83a78-164">Time required to fully charge the battery.</span></span> <span data-ttu-id="83a78-165">不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="83a78-165">This property is not supported.</span></span> <span data-ttu-id="83a78-166">**BatteryRechargeTime** 沒有取代屬性，現在已被視為已淘汰。</span><span class="sxs-lookup"><span data-stu-id="83a78-166">**BatteryRechargeTime** does not have a replacement property, and is now considered obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="83a78-167">**BatteryStatus**</span><span class="sxs-lookup"><span data-stu-id="83a78-167">**BatteryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-168">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="83a78-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-170">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 便攜電池 \| 002.14」 ) </span><span class="sxs-lookup"><span data-stu-id="83a78-170">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.14")</span></span>
</dt> </dl>

<span data-ttu-id="83a78-171">電池的狀態。</span><span class="sxs-lookup"><span data-stu-id="83a78-171">Status of the battery.</span></span> <span data-ttu-id="83a78-172">在 CIM 架構中，值 10 (未定義的) 無效，因為在 DMI 中，它代表未安裝電池。</span><span class="sxs-lookup"><span data-stu-id="83a78-172">The value 10 (Undefined) is not valid in the CIM schema because in DMI it represents that no battery is installed.</span></span> <span data-ttu-id="83a78-173">在此情況下，不應該具現化物件。</span><span class="sxs-lookup"><span data-stu-id="83a78-173">In this case, the object should not be instantiated.</span></span>

<span data-ttu-id="83a78-174">這個屬性繼承自 [**CIM \_ 電池**](cim-battery.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-174">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="83a78-175"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="83a78-175"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-176">電池正在進行放電。</span><span class="sxs-lookup"><span data-stu-id="83a78-176">The battery is discharging.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="83a78-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="83a78-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-178">系統具有 AC 的存取權，因此不會耗盡電池。</span><span class="sxs-lookup"><span data-stu-id="83a78-178">The system has access to AC so no battery is being discharged.</span></span> <span data-ttu-id="83a78-179">不過，電池不一定會收取費用。</span><span class="sxs-lookup"><span data-stu-id="83a78-179">However, the battery is not necessarily charging.</span></span>

</dd> <dt>

<span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>

<span data-ttu-id="83a78-180"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span> (3) **完全收費**</span><span class="sxs-lookup"><span data-stu-id="83a78-180"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>**Fully Charged** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="83a78-181"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**低** (4) </span><span class="sxs-lookup"><span data-stu-id="83a78-181"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="83a78-182"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**重大** (5) </span><span class="sxs-lookup"><span data-stu-id="83a78-182"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>

<span data-ttu-id="83a78-183"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>**充電** (6) </span><span class="sxs-lookup"><span data-stu-id="83a78-183"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>**Charging** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>

<span data-ttu-id="83a78-184"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>**充電和高** (7) </span><span class="sxs-lookup"><span data-stu-id="83a78-184"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>**Charging and High** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>

<span data-ttu-id="83a78-185"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>**充電和低** (8) </span><span class="sxs-lookup"><span data-stu-id="83a78-185"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>**Charging and Low** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>

<span data-ttu-id="83a78-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>**充電和重大** (9) </span><span class="sxs-lookup"><span data-stu-id="83a78-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>**Charging and Critical** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="83a78-187"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**未定義** (10) </span><span class="sxs-lookup"><span data-stu-id="83a78-187"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>

<span data-ttu-id="83a78-188"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**部分計費** (11) </span><span class="sxs-lookup"><span data-stu-id="83a78-188"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**Partially Charged** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="83a78-189">**標題**</span><span class="sxs-lookup"><span data-stu-id="83a78-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-190">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="83a78-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-192">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="83a78-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="83a78-193">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="83a78-193">Short description of the object a one-line string.</span></span>

<span data-ttu-id="83a78-194">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="83a78-195">**化學**</span><span class="sxs-lookup"><span data-stu-id="83a78-195">**Chemistry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-196">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="83a78-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-198">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 便攜電池 \| 002.7」 ) </span><span class="sxs-lookup"><span data-stu-id="83a78-198">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="83a78-199">描述電池化學的列舉。</span><span class="sxs-lookup"><span data-stu-id="83a78-199">Enumeration that describes the battery's chemistry.</span></span>

<span data-ttu-id="83a78-200">這個屬性繼承自 [**CIM \_ 電池**](cim-battery.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-200">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="83a78-201">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="83a78-201">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="83a78-202">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="83a78-202">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>

<span data-ttu-id="83a78-203">**潛在客戶 Acid** (3) </span><span class="sxs-lookup"><span data-stu-id="83a78-203">**Lead Acid** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>

<span data-ttu-id="83a78-204">**五分錢鎘** (4) </span><span class="sxs-lookup"><span data-stu-id="83a78-204">**Nickel Cadmium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>

<span data-ttu-id="83a78-205">**五分錢裸機氫化** (5) </span><span class="sxs-lookup"><span data-stu-id="83a78-205">**Nickel Metal Hydride** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>

<span data-ttu-id="83a78-206">**鋰離子** (6) </span><span class="sxs-lookup"><span data-stu-id="83a78-206">**Lithium-ion** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>

<span data-ttu-id="83a78-207">**Zinc air** (7) </span><span class="sxs-lookup"><span data-stu-id="83a78-207">**Zinc air** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>

<span data-ttu-id="83a78-208">**鋰聚合體** (8) </span><span class="sxs-lookup"><span data-stu-id="83a78-208">**Lithium Polymer** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="83a78-209">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="83a78-209">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-210">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="83a78-210">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-212">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="83a78-212">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="83a78-213">Windows 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="83a78-213">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="83a78-214">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-214">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="83a78-215"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="83a78-215"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="83a78-216"> (0)</span><span class="sxs-lookup"><span data-stu-id="83a78-216">(0)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-217">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="83a78-217">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="83a78-218"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="83a78-218"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="83a78-219">(1)</span><span class="sxs-lookup"><span data-stu-id="83a78-219">(1)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-220">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="83a78-220">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="83a78-221"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="83a78-221"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="83a78-222">(2)</span><span class="sxs-lookup"><span data-stu-id="83a78-222">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="83a78-223"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="83a78-223"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="83a78-224">(3)</span><span class="sxs-lookup"><span data-stu-id="83a78-224">(3)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-225">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="83a78-225">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="83a78-226"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="83a78-226"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="83a78-227">(4)</span><span class="sxs-lookup"><span data-stu-id="83a78-227">(4)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-228">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="83a78-228">Device is not working properly.</span></span> <span data-ttu-id="83a78-229">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="83a78-229">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="83a78-230"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="83a78-230"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="83a78-231">(5)</span><span class="sxs-lookup"><span data-stu-id="83a78-231">(5)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-232">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="83a78-232">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="83a78-233"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="83a78-233"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="83a78-234">(6)</span><span class="sxs-lookup"><span data-stu-id="83a78-234">(6)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-235">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="83a78-235">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="83a78-236"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="83a78-236"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="83a78-237">(7)</span><span class="sxs-lookup"><span data-stu-id="83a78-237">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="83a78-238"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="83a78-238"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="83a78-239">(8)</span><span class="sxs-lookup"><span data-stu-id="83a78-239">(8)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-240">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="83a78-240">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="83a78-241"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="83a78-241"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="83a78-242">(9)</span><span class="sxs-lookup"><span data-stu-id="83a78-242">(9)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-243">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="83a78-243">Device is not working properly.</span></span> <span data-ttu-id="83a78-244">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="83a78-244">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="83a78-245"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="83a78-245"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="83a78-246">(10)</span><span class="sxs-lookup"><span data-stu-id="83a78-246">(10)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-247">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="83a78-247">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="83a78-248"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="83a78-248"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="83a78-249">(11)</span><span class="sxs-lookup"><span data-stu-id="83a78-249">(11)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-250">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="83a78-250">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="83a78-251"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="83a78-251"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="83a78-252"> (12) </span><span class="sxs-lookup"><span data-stu-id="83a78-252">(12)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-253">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="83a78-253">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="83a78-254"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="83a78-254"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="83a78-255">(13)</span><span class="sxs-lookup"><span data-stu-id="83a78-255">(13)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-256">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="83a78-256">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="83a78-257"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="83a78-257"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="83a78-258">(14)</span><span class="sxs-lookup"><span data-stu-id="83a78-258">(14)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-259">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="83a78-259">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="83a78-260"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="83a78-260"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="83a78-261">(15)</span><span class="sxs-lookup"><span data-stu-id="83a78-261">(15)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-262">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="83a78-262">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="83a78-263"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="83a78-263"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="83a78-264">(16)</span><span class="sxs-lookup"><span data-stu-id="83a78-264">(16)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-265">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="83a78-265">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="83a78-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="83a78-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="83a78-267">(17)</span><span class="sxs-lookup"><span data-stu-id="83a78-267">(17)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-268">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="83a78-268">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="83a78-269"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="83a78-269"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="83a78-270">(18)</span><span class="sxs-lookup"><span data-stu-id="83a78-270">(18)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-271">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="83a78-271">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="83a78-272"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="83a78-272"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="83a78-273">(19)</span><span class="sxs-lookup"><span data-stu-id="83a78-273">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="83a78-274"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="83a78-274"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="83a78-275">(20)</span><span class="sxs-lookup"><span data-stu-id="83a78-275">(20)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-276">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="83a78-276">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="83a78-277"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="83a78-277"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="83a78-278">(21)</span><span class="sxs-lookup"><span data-stu-id="83a78-278">(21)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-279">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="83a78-279">System failure.</span></span> <span data-ttu-id="83a78-280">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="83a78-280">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="83a78-281">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="83a78-281">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="83a78-282"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="83a78-282"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="83a78-283">(22)</span><span class="sxs-lookup"><span data-stu-id="83a78-283">(22)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-284">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="83a78-284">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="83a78-285"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="83a78-285"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="83a78-286">(23)</span><span class="sxs-lookup"><span data-stu-id="83a78-286">(23)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-287">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="83a78-287">System failure.</span></span> <span data-ttu-id="83a78-288">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="83a78-288">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="83a78-289"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="83a78-289"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="83a78-290">(24)</span><span class="sxs-lookup"><span data-stu-id="83a78-290">(24)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-291">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="83a78-291">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="83a78-292"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="83a78-292"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="83a78-293">(25)</span><span class="sxs-lookup"><span data-stu-id="83a78-293">(25)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-294">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="83a78-294">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="83a78-295"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="83a78-295"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="83a78-296">(26)</span><span class="sxs-lookup"><span data-stu-id="83a78-296">(26)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-297">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="83a78-297">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="83a78-298"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="83a78-298"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="83a78-299">(27)</span><span class="sxs-lookup"><span data-stu-id="83a78-299">(27)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-300">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="83a78-300">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="83a78-301"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="83a78-301"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="83a78-302">(28)</span><span class="sxs-lookup"><span data-stu-id="83a78-302">(28)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-303">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="83a78-303">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="83a78-304"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="83a78-304"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="83a78-305">(29)</span><span class="sxs-lookup"><span data-stu-id="83a78-305">(29)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-306">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="83a78-306">Device is disabled.</span></span> <span data-ttu-id="83a78-307">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="83a78-307">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="83a78-308"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="83a78-308"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="83a78-309">(30)</span><span class="sxs-lookup"><span data-stu-id="83a78-309">(30)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-310">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="83a78-310">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="83a78-311"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="83a78-311"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="83a78-312"> (31) </span><span class="sxs-lookup"><span data-stu-id="83a78-312">(31)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-313">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="83a78-313">Device is not working properly.</span></span> <span data-ttu-id="83a78-314">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="83a78-314">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="83a78-315">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="83a78-315">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-316">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="83a78-316">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-317">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-318">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="83a78-318">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="83a78-319">若 **為 True**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="83a78-319">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="83a78-320">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83a78-321">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="83a78-321">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-322">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="83a78-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-323">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-324">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="83a78-324">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="83a78-325">第一個具象類別的名稱，這個類別會出現在建立實例時所用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="83a78-325">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="83a78-326">當搭配類別的其他索引鍵屬性使用時，屬性允許唯一識別此類別的所有實例和其子類別。</span><span class="sxs-lookup"><span data-stu-id="83a78-326">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="83a78-327">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83a78-328">**說明**</span><span class="sxs-lookup"><span data-stu-id="83a78-328">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-329">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="83a78-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-330">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-331">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="83a78-331">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="83a78-332">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="83a78-332">Description of the object.</span></span>

<span data-ttu-id="83a78-333">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-333">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="83a78-334">**DesignCapacity**</span><span class="sxs-lookup"><span data-stu-id="83a78-334">**DesignCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-335">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="83a78-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-336">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-337">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 便攜電池 \| 002.8」 ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫瓦-小時" ) </span><span class="sxs-lookup"><span data-stu-id="83a78-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="83a78-338">在毫瓦時設計電池的容量。</span><span class="sxs-lookup"><span data-stu-id="83a78-338">Design capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="83a78-339">如果不支援此屬性，請輸入 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="83a78-339">If the property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="83a78-340">這個屬性繼承自 [**CIM \_ 電池**](cim-battery.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-340">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="83a78-341">**DesignVoltage**</span><span class="sxs-lookup"><span data-stu-id="83a78-341">**DesignVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-342">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="83a78-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-343">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-344">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 便攜電池 \| 002.9」 ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫伏" ) </span><span class="sxs-lookup"><span data-stu-id="83a78-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="83a78-345">以毫伏設計的電池電壓。</span><span class="sxs-lookup"><span data-stu-id="83a78-345">Design voltage of the battery in millivolts.</span></span> <span data-ttu-id="83a78-346">如果不支援此屬性，請輸入 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="83a78-346">If the attribute is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="83a78-347">這個屬性繼承自 [**CIM \_ 電池**](cim-battery.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-347">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<span data-ttu-id="83a78-348">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="83a78-348">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="83a78-349">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="83a78-349">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-350">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="83a78-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-351">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-352">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "DeviceId" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="83a78-352">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="83a78-353">識別電池。</span><span class="sxs-lookup"><span data-stu-id="83a78-353">Identifies the battery.</span></span>

<span data-ttu-id="83a78-354">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-354">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="83a78-355">範例：「內部電池」</span><span class="sxs-lookup"><span data-stu-id="83a78-355">Example: "Internal Battery"</span></span>

</dd> <dt>

<span data-ttu-id="83a78-356">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="83a78-356">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-357">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="83a78-357">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-358">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83a78-359">若 **為 True**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="83a78-359">If **True**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="83a78-360">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83a78-361">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="83a78-361">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-362">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="83a78-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-363">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83a78-364">提供 **LastErrorCode** 屬性中所記錄錯誤之詳細資訊的自由格式字串，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="83a78-364">Free-form string that supplies more information about the error recorded in **LastErrorCode** property, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="83a78-365">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-365">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83a78-366">**EstimatedChargeRemaining**</span><span class="sxs-lookup"><span data-stu-id="83a78-366">**EstimatedChargeRemaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-367">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="83a78-367">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-368">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-369">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「百分比」 ) </span><span class="sxs-lookup"><span data-stu-id="83a78-369">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="83a78-370">估計剩餘的完整費用百分比。</span><span class="sxs-lookup"><span data-stu-id="83a78-370">Estimate of the percentage of full charge remaining.</span></span>

<span data-ttu-id="83a78-371">這個屬性繼承自 [**CIM \_ 電池**](cim-battery.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-371">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="83a78-372">**EstimatedRunTime**</span><span class="sxs-lookup"><span data-stu-id="83a78-372">**EstimatedRunTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-373">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="83a78-373">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-374">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-375">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 便攜電池 \| 002.15 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 分鐘 ") </span><span class="sxs-lookup"><span data-stu-id="83a78-375">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="83a78-376">如果公用程式電源關閉、遺失並保持關閉狀態，或膝上型電腦與電源中斷連線，則在目前的負載條件下估計電池計量耗盡的時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="83a78-376">Estimate in minutes of the time to battery charge depletion under the present load conditions if the utility power is off, or lost and remains off, or a laptop is disconnected from a power source.</span></span>

<span data-ttu-id="83a78-377">這個屬性繼承自 [**CIM \_ 電池**](cim-battery.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-377">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="83a78-378">**ExpectedBatteryLife**</span><span class="sxs-lookup"><span data-stu-id="83a78-378">**ExpectedBatteryLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-379">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="83a78-379">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-380">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-381">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "HKEY \_ LOCAL \_ MACHINE \\ \\ System \\ \\ CurrentControlSet \\ \\ Services \| BatteryLife" ) ，[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "分鐘" ) </span><span class="sxs-lookup"><span data-stu-id="83a78-381">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("HKEY\_LOCAL\_MACHINE\\\\System\\\\CurrentControlSet\\\\Services\|BatteryLife"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="83a78-382">完全收費後完全清空電池所需的時間量。</span><span class="sxs-lookup"><span data-stu-id="83a78-382">Amount of time it takes to completely drain the battery after it is fully charged.</span></span> <span data-ttu-id="83a78-383">這個屬性已不再使用，並被視為已淘汰。</span><span class="sxs-lookup"><span data-stu-id="83a78-383">This property is no longer used and is considered obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="83a78-384">**ExpectedLife**</span><span class="sxs-lookup"><span data-stu-id="83a78-384">**ExpectedLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-385">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="83a78-385">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-386">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-387">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "分鐘" ) </span><span class="sxs-lookup"><span data-stu-id="83a78-387">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="83a78-388">電池的預期存留期（以分鐘為單位）（假設電池已完全收費）。</span><span class="sxs-lookup"><span data-stu-id="83a78-388">Battery's expected lifetime in minutes, assuming that the battery is fully charged.</span></span> <span data-ttu-id="83a78-389">屬性代表電池的預期存留期總計，而不是其目前剩餘的存留期（由 **EstimatedRunTime** 屬性工作表示）。</span><span class="sxs-lookup"><span data-stu-id="83a78-389">The property represents the total expected life of the battery, not its current remaining life, which is indicated by the **EstimatedRunTime** property.</span></span>

<span data-ttu-id="83a78-390">這個屬性繼承自 [**CIM \_ 電池**](cim-battery.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-390">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="83a78-391">**FullChargeCapacity**</span><span class="sxs-lookup"><span data-stu-id="83a78-391">**FullChargeCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-392">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="83a78-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-393">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-394">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 便攜電池 \| 002.11」 ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫瓦-小時" ) </span><span class="sxs-lookup"><span data-stu-id="83a78-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="83a78-395">毫瓦-小時內電池的完整收費容量。</span><span class="sxs-lookup"><span data-stu-id="83a78-395">Full charge capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="83a78-396">值與 **DesignCapacity** 屬性的比較會決定何時需要更換電池。</span><span class="sxs-lookup"><span data-stu-id="83a78-396">Comparison of the value to the **DesignCapacity** property determines when the battery requires replacement.</span></span> <span data-ttu-id="83a78-397">電池生命週期結束通常是在 **FullChargeCapacity** 屬性低於80% 的 **DesignCapacity** 屬性。</span><span class="sxs-lookup"><span data-stu-id="83a78-397">A battery's end of life is typically when the **FullChargeCapacity** property falls below 80% of the **DesignCapacity** property.</span></span> <span data-ttu-id="83a78-398">如果不支援此屬性，請輸入 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="83a78-398">If the property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="83a78-399">這個屬性繼承自 [**CIM \_ 電池**](cim-battery.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-399">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="83a78-400">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="83a78-400">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-401">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="83a78-401">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-402">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-403">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="83a78-403">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="83a78-404">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="83a78-404">Date and time the object was installed.</span></span> <span data-ttu-id="83a78-405">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="83a78-405">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="83a78-406">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-406">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="83a78-407">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="83a78-407">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-408">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="83a78-408">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-409">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83a78-410">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="83a78-410">Last error code reported by the logical device.</span></span>

<span data-ttu-id="83a78-411">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83a78-412">**MaxRechargeTime**</span><span class="sxs-lookup"><span data-stu-id="83a78-412">**MaxRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-413">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="83a78-413">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-414">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-415">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "分鐘" ) </span><span class="sxs-lookup"><span data-stu-id="83a78-415">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="83a78-416">完全充電電池的最長時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="83a78-416">Maximum time, in minutes, to fully charge the battery.</span></span> <span data-ttu-id="83a78-417">屬性代表重新充電完全耗盡電池的時間，而不是目前剩餘的費用時間（在 **TimeToFullCharge** 屬性中表示）。</span><span class="sxs-lookup"><span data-stu-id="83a78-417">The property represents the time to recharge a fully depleted battery, not the current remaining charge time, which is indicated in the **TimeToFullCharge** property.</span></span>

<span data-ttu-id="83a78-418">這個屬性繼承自 [**CIM \_ 電池**](cim-battery.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-418">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="83a78-419">**名稱**</span><span class="sxs-lookup"><span data-stu-id="83a78-419">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-420">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="83a78-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-421">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-422">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="83a78-422">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="83a78-423">定義物件已知的標籤。</span><span class="sxs-lookup"><span data-stu-id="83a78-423">Defines the label by which the object is known.</span></span> <span data-ttu-id="83a78-424">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="83a78-424">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="83a78-425">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-425">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="83a78-426">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="83a78-426">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-427">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="83a78-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-428">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-429">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="83a78-429">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="83a78-430">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="83a78-430">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="83a78-431">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="83a78-432">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="83a78-432">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="83a78-433">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="83a78-433">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-434">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="83a78-434">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="83a78-435">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83a78-436">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="83a78-436">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="83a78-437">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="83a78-437">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="83a78-438"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="83a78-438"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="83a78-439"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="83a78-439"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="83a78-440"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="83a78-440"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="83a78-441"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="83a78-441"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-442">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="83a78-442">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="83a78-443"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="83a78-443"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-444">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="83a78-444">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="83a78-445"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="83a78-445"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-446">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="83a78-446">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="83a78-447">這個方法可在父 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="83a78-447">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="83a78-448">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="83a78-448">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="83a78-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="83a78-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-450">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="83a78-450">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="83a78-451"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="83a78-451"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="83a78-452">支援計時 Power-On</span><span class="sxs-lookup"><span data-stu-id="83a78-452">Timed Power-On Supported</span></span>

<span data-ttu-id="83a78-453">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="83a78-453">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="83a78-454">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="83a78-454">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-455">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="83a78-455">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-456">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83a78-457">若 **為 True**，則裝置可以是電源管理 (可進入暫停模式，依此類推) 。</span><span class="sxs-lookup"><span data-stu-id="83a78-457">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="83a78-458">屬性不表示電源管理功能目前已啟用，只有邏輯裝置能夠進行電源管理。</span><span class="sxs-lookup"><span data-stu-id="83a78-458">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="83a78-459">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-459">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83a78-460">**SmartBatteryVersion**</span><span class="sxs-lookup"><span data-stu-id="83a78-460">**SmartBatteryVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-461">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="83a78-461">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-462">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-462">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-463">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 便攜電池 \| 002.10」 ) </span><span class="sxs-lookup"><span data-stu-id="83a78-463">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.10")</span></span>
</dt> </dl>

<span data-ttu-id="83a78-464">電池所支援的資料規格版本號碼。</span><span class="sxs-lookup"><span data-stu-id="83a78-464">Data Specification version number supported by the battery.</span></span> <span data-ttu-id="83a78-465">如果電池不支援此功能，此值應保留空白。</span><span class="sxs-lookup"><span data-stu-id="83a78-465">If the battery does not support this function, the value should be left blank.</span></span>

<span data-ttu-id="83a78-466">這個屬性繼承自 [**CIM \_ 電池**](cim-battery.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-466">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="83a78-467">**狀態**</span><span class="sxs-lookup"><span data-stu-id="83a78-467">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-468">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="83a78-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-469">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-470">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="83a78-470">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="83a78-471">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="83a78-471">Current status of the object.</span></span> <span data-ttu-id="83a78-472">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="83a78-472">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="83a78-473">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="83a78-473">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="83a78-474">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="83a78-474">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="83a78-475">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="83a78-475">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="83a78-476">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="83a78-476">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="83a78-477">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-477">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="83a78-478">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="83a78-478">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="83a78-479">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="83a78-479">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="83a78-480">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="83a78-480">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="83a78-481">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="83a78-481">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="83a78-482">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="83a78-482">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="83a78-483">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="83a78-483">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="83a78-484">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="83a78-484">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="83a78-485">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="83a78-485">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="83a78-486">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="83a78-486">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="83a78-487">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="83a78-487">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="83a78-488">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="83a78-488">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="83a78-489">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="83a78-489">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="83a78-490">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="83a78-490">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="83a78-491">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="83a78-491">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-492">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="83a78-492">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-493">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-493">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-494">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="83a78-494">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="83a78-495">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="83a78-495">State of the logical device.</span></span> <span data-ttu-id="83a78-496">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="83a78-496">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="83a78-497">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-497">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="83a78-498">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="83a78-498">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="83a78-499">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="83a78-499">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="83a78-500">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="83a78-500">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="83a78-501">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="83a78-501">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="83a78-502">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="83a78-502">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="83a78-503">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="83a78-503">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-504">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="83a78-504">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-505">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-505">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-506">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="83a78-506">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="83a78-507">範圍電腦之 **CreationClassName** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="83a78-507">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="83a78-508">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-508">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83a78-509">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="83a78-509">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-510">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="83a78-510">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-511">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-512">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="83a78-512">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="83a78-513">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="83a78-513">Name of the scoping system.</span></span>

<span data-ttu-id="83a78-514">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-514">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83a78-515">**TimeOnBattery**</span><span class="sxs-lookup"><span data-stu-id="83a78-515">**TimeOnBattery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-516">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="83a78-516">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-517">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-517">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-518">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「秒」 ) </span><span class="sxs-lookup"><span data-stu-id="83a78-518">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="83a78-519">電腦系統 UPS 上一次切換到電池電源，或自系統或 UPS 上一次重新開機之後的時間（以較小者為准）的經過時間（秒）。</span><span class="sxs-lookup"><span data-stu-id="83a78-519">Elapsed time in seconds since the computer system's UPS last switched to battery power, or the time since the system or UPS was last restarted, whichever is less.</span></span> <span data-ttu-id="83a78-520">如果電池為「線上」，則會傳回 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="83a78-520">If the battery is "on line", 0 (zero) is returned.</span></span>

<span data-ttu-id="83a78-521">這個屬性繼承自 [**CIM \_ 電池**](cim-battery.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-521">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="83a78-522">**TimeToFullCharge**</span><span class="sxs-lookup"><span data-stu-id="83a78-522">**TimeToFullCharge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83a78-523">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="83a78-523">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83a78-524">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83a78-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83a78-525">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 便攜電池 \| 002.16 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 分鐘 ") </span><span class="sxs-lookup"><span data-stu-id="83a78-525">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="83a78-526">以目前的充電費率和使用量，在幾分鐘內完全收取電池費用的剩餘時間。</span><span class="sxs-lookup"><span data-stu-id="83a78-526">Remaining time to charge the battery fully in minutes at the current charging rate and usage.</span></span>

<span data-ttu-id="83a78-527">這個屬性繼承自 [**CIM \_ 電池**](cim-battery.md)。</span><span class="sxs-lookup"><span data-stu-id="83a78-527">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83a78-528">備註</span><span class="sxs-lookup"><span data-stu-id="83a78-528">Remarks</span></span>

<span data-ttu-id="83a78-529">**Win32 \_ 電池** 類別衍生自 cim [**\_ 電池**](cim-battery.md)（衍生自 [**cim \_ LogicalDevice**](cim-logicaldevice.md)）。</span><span class="sxs-lookup"><span data-stu-id="83a78-529">The **Win32\_Battery** class is derived from [**CIM\_Battery**](cim-battery.md) which derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="83a78-530">Windows Server 2008 包含作業系統中的 (APC) UPS 驅動程式，可讓您將 UPS 視為電池供電。</span><span class="sxs-lookup"><span data-stu-id="83a78-530">Windows Server 2008 contains the (APC) UPS drivers in the OS, which allows you to treat the UPS as a battery supply.</span></span> <span data-ttu-id="83a78-531">這可讓您使用腳本來監視 UPS 狀態，並在必要時採取動作。</span><span class="sxs-lookup"><span data-stu-id="83a78-531">This allows you to monitor the UPS status using a script and take actions when necessary.</span></span>

## <a name="examples"></a><span data-ttu-id="83a78-532">範例</span><span class="sxs-lookup"><span data-stu-id="83a78-532">Examples</span></span>

<span data-ttu-id="83a78-533">[Toggle-Wireless.ps1](https://Gallery.TechNet.Microsoft.Com/Toggle-Wirelessps1-2d244a8f) PowerShell 程式碼範例會查詢 **Win32 \_ 電池**，以判斷是否要切換無線以節省電源。</span><span class="sxs-lookup"><span data-stu-id="83a78-533">The [Toggle-Wireless.ps1](https://Gallery.TechNet.Microsoft.Com/Toggle-Wirelessps1-2d244a8f) PowerShell code sample queries **Win32\_Battery** to determine whether or not to toggle the wireless in order to save power.</span></span>

<span data-ttu-id="83a78-534">[列出 UPS 資訊](https://Gallery.TechNet.Microsoft.Com/7196121e-97de-4290-9939-26d0ce266270)Perl 範例會列出連接到電腦的不斷電供應系統來源的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="83a78-534">The [List UPS Information](https://Gallery.TechNet.Microsoft.Com/7196121e-97de-4290-9939-26d0ce266270) Perl sample Lists information about the uninterruptible power sources attached to a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="83a78-535">規格需求</span><span class="sxs-lookup"><span data-stu-id="83a78-535">Requirements</span></span>



| <span data-ttu-id="83a78-536">需求</span><span class="sxs-lookup"><span data-stu-id="83a78-536">Requirement</span></span> | <span data-ttu-id="83a78-537">值</span><span class="sxs-lookup"><span data-stu-id="83a78-537">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83a78-538">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="83a78-538">Minimum supported client</span></span><br/> | <span data-ttu-id="83a78-539">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83a78-539">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="83a78-540">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="83a78-540">Minimum supported server</span></span><br/> | <span data-ttu-id="83a78-541">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83a78-541">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="83a78-542">命名空間</span><span class="sxs-lookup"><span data-stu-id="83a78-542">Namespace</span></span><br/>                | <span data-ttu-id="83a78-543">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="83a78-543">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="83a78-544">MOF</span><span class="sxs-lookup"><span data-stu-id="83a78-544">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83a78-545"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="83a78-545"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="83a78-546">DLL</span><span class="sxs-lookup"><span data-stu-id="83a78-546">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83a78-547"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83a78-547"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83a78-548">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83a78-548">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83a78-549">**CIM \_ 電池**</span><span class="sxs-lookup"><span data-stu-id="83a78-549">**CIM\_Battery**</span></span>](cim-battery.md)
</dt> <dt>

[<span data-ttu-id="83a78-550">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="83a78-550">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

