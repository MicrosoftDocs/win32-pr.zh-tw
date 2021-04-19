---
description: 「CIM \_ 電池」類別代表電池邏輯裝置的功能和管理。 此類別適用于膝上型電腦系統中的電池，以及其他內部和外部電池。
ms.assetid: af127b7a-021b-4cd8-af1b-176aff760858
ms.tgt_platform: multiple
title: CIM_Battery 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Battery
- CIM_Battery.Caption
- CIM_Battery.Description
- CIM_Battery.InstallDate
- CIM_Battery.Name
- CIM_Battery.Status
- CIM_Battery.Availability
- CIM_Battery.ConfigManagerErrorCode
- CIM_Battery.ConfigManagerUserConfig
- CIM_Battery.CreationClassName
- CIM_Battery.DeviceID
- CIM_Battery.PowerManagementCapabilities
- CIM_Battery.ErrorCleared
- CIM_Battery.ErrorDescription
- CIM_Battery.LastErrorCode
- CIM_Battery.PNPDeviceID
- CIM_Battery.PowerManagementSupported
- CIM_Battery.StatusInfo
- CIM_Battery.SystemCreationClassName
- CIM_Battery.SystemName
- CIM_Battery.BatteryStatus
- CIM_Battery.Chemistry
- CIM_Battery.DesignCapacity
- CIM_Battery.DesignVoltage
- CIM_Battery.EstimatedChargeRemaining
- CIM_Battery.EstimatedRunTime
- CIM_Battery.ExpectedLife
- CIM_Battery.FullChargeCapacity
- CIM_Battery.MaxRechargeTime
- CIM_Battery.SmartBatteryVersion
- CIM_Battery.TimeOnBattery
- CIM_Battery.TimeToFullCharge
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3719b2700c69cfa58921bed1242aa8a6de158466
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972343"
---
# <a name="cim_battery-class"></a><span data-ttu-id="6ddb5-104">CIM \_ 電池類別</span><span class="sxs-lookup"><span data-stu-id="6ddb5-104">CIM\_Battery class</span></span>

<span data-ttu-id="6ddb5-105">「 **CIM \_ 電池** 」類別代表電池邏輯裝置的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-105">The **CIM\_Battery** class represents the capabilities and management of the battery logical device.</span></span> <span data-ttu-id="6ddb5-106">此類別適用于膝上型電腦系統中的電池，以及其他內部和外部電池。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-106">This class applies to batteries in laptop systems and other internal and external batteries.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6ddb5-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6ddb5-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6ddb5-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6ddb5-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ddb5-111">語法</span><span class="sxs-lookup"><span data-stu-id="6ddb5-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C548-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Battery : CIM_LogicalDevice
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
  uint16   BatteryStatus;
  uint16   Chemistry;
  uint32   DesignCapacity;
  uint64   DesignVoltage;
  uint16   EstimatedChargeRemaining;
  uint32   EstimatedRunTime;
  uint32   ExpectedLife;
  uint32   FullChargeCapacity;
  uint32   MaxRechargeTime;
  string   SmartBatteryVersion;
  uint32   TimeOnBattery;
  uint32   TimeToFullCharge;
};
```

## <a name="members"></a><span data-ttu-id="6ddb5-112">成員</span><span class="sxs-lookup"><span data-stu-id="6ddb5-112">Members</span></span>

<span data-ttu-id="6ddb5-113">**CIM \_ 電池** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6ddb5-113">The **CIM\_Battery** class has these types of members:</span></span>

-   [<span data-ttu-id="6ddb5-114">方法</span><span class="sxs-lookup"><span data-stu-id="6ddb5-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="6ddb5-115">屬性</span><span class="sxs-lookup"><span data-stu-id="6ddb5-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6ddb5-116">方法</span><span class="sxs-lookup"><span data-stu-id="6ddb5-116">Methods</span></span>

<span data-ttu-id="6ddb5-117">**CIM \_ 電池** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-117">The **CIM\_Battery** class has these methods.</span></span>



| <span data-ttu-id="6ddb5-118">方法</span><span class="sxs-lookup"><span data-stu-id="6ddb5-118">Method</span></span>                                                             | <span data-ttu-id="6ddb5-119">描述</span><span class="sxs-lookup"><span data-stu-id="6ddb5-119">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6ddb5-120">**重設**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-120">**Reset**</span></span>](reset-method-in-class-cim-battery.md)                 | <span data-ttu-id="6ddb5-121">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="6ddb5-122">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-122">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="6ddb5-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-battery.md) | <span data-ttu-id="6ddb5-124">定義邏輯裝置的預期電源狀態，以及裝置何時應進入該狀態。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-124">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="6ddb5-125">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6ddb5-126">屬性</span><span class="sxs-lookup"><span data-stu-id="6ddb5-126">Properties</span></span>

<span data-ttu-id="6ddb5-127">**CIM \_ 電池** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-127">The **CIM\_Battery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6ddb5-128">**可用性**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-129">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-131">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="6ddb5-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-132">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-132">Availability and status of the device.</span></span>

<span data-ttu-id="6ddb5-133">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-133">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6ddb5-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6ddb5-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="6ddb5-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="6ddb5-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="6ddb5-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6ddb5-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="6ddb5-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="6ddb5-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="6ddb5-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="6ddb5-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6ddb5-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="6ddb5-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="6ddb5-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="6ddb5-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-147">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-147">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="6ddb5-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-149">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-149">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="6ddb5-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-151">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-151">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="6ddb5-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="6ddb5-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-154">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-154">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="6ddb5-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-156">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-156">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="6ddb5-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-158">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-158">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="6ddb5-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-160">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-160">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="6ddb5-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-162">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-162">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6ddb5-163">**BatteryStatus**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-163">**BatteryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-164">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-166">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 便攜電池 \| 002.14」 ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.14")</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-167">電池充電狀態的描述。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-167">Description of the battery's charge status.</span></span> <span data-ttu-id="6ddb5-168">在 CIM 架構中，值10是不正確，這表示在桌面管理介面 (DMI) 不會安裝電池。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-168">The value 10 is not valid in the CIM schema, which represents no battery being installed in Desktop Management Interface (DMI).</span></span> <span data-ttu-id="6ddb5-169">在此情況下，不應該具現化物件。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-169">In this case, the object should not be instantiated.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6ddb5-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-171">其他。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-171">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6ddb5-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-173">不明。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-173">Unknown.</span></span>

</dd> <dt>

<span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>

<span data-ttu-id="6ddb5-174"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span> (3) **完全收費**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-174"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>**Fully Charged** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-175">完全收費。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-175">Fully charged.</span></span>

</dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="6ddb5-176"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**低** (4) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-176"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-177">低。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-177">Low.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="6ddb5-178"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**重大** (5) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-178"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-179">嚴重。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-179">Critical.</span></span>

</dd> <dt>

<span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>

<span data-ttu-id="6ddb5-180"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>**充電** (6) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-180"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>**Charging** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-181">充電。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-181">Charging.</span></span>

</dd> <dt>

<span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>

<span data-ttu-id="6ddb5-182"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>**充電和高** (7) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-182"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>**Charging and High** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-183">充電和高。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-183">Charging and high.</span></span>

</dd> <dt>

<span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>

<span data-ttu-id="6ddb5-184"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>**充電和低** (8) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-184"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>**Charging and Low** (8)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-185">充電和低度。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-185">Charging and low.</span></span>

</dd> <dt>

<span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>

<span data-ttu-id="6ddb5-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>**充電和重大** (9) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>**Charging and Critical** (9)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-187">收費和重要。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-187">Charging and critical.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="6ddb5-188"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**未定義** (10) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-188"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (10)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-189">未定義。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-189">Undefined.</span></span>

</dd> <dt>

<span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>

<span data-ttu-id="6ddb5-190"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**部分計費** (11) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-190"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**Partially Charged** (11)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-191">部分收費。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-191">Partially charged.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6ddb5-192">**標題**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-192">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-193">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-195">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-195">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-196">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-196">A short textual description of the object.</span></span>

<span data-ttu-id="6ddb5-197">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ddb5-198">**化學**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-198">**Chemistry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-199">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-201">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 便攜電池 \| 002.7」 ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-201">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-202">描述電池化學的列舉。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-202">Enumeration that describes the battery's chemistry.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6ddb5-203"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-203"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-204">其他。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-204">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6ddb5-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-206">不明。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-206">Unknown.</span></span>

</dd> <dt>

<span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>

<span data-ttu-id="6ddb5-207"><span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>**潛在客戶 Acid** (3) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-207"><span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>**Lead Acid** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-208">潛在客戶 acid。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-208">Lead acid.</span></span>

</dd> <dt>

<span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>

<span data-ttu-id="6ddb5-209"><span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>**五分錢鎘** (4) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-209"><span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>**Nickel Cadmium** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-210">五分錢鎘。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-210">Nickel cadmium.</span></span>

</dd> <dt>

<span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>

<span data-ttu-id="6ddb5-211"><span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>**五分錢裸機氫化** (5) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-211"><span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>**Nickel Metal Hydride** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-212">五分錢金屬氫化。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-212">Nickel metal hydride.</span></span>

</dd> <dt>

<span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>

<span data-ttu-id="6ddb5-213"><span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>**鋰離子** (6) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-213"><span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>**Lithium-ion** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-214">鋰離子。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-214">Lithium ion.</span></span>

</dd> <dt>

<span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>

<span data-ttu-id="6ddb5-215"><span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>**Zinc air** (7) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-215"><span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>**Zinc air** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-216">Zinc 空氣。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-216">Zinc air.</span></span>

</dd> <dt>

<span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>

<span data-ttu-id="6ddb5-217"><span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>**鋰聚合體** (8) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-217"><span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>**Lithium Polymer** (8)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-218">鋰聚合體。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-218">Lithium polymer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6ddb5-219">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-219">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-220">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-221">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-222">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-222">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-223">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-223">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="6ddb5-224">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-224">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="6ddb5-225">**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-225">**This device is working properly.**</span></span> <span data-ttu-id="6ddb5-226"> (0)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-226">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="6ddb5-227">**這個裝置並未正確設定。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-227">**This device is not configured correctly.**</span></span> <span data-ttu-id="6ddb5-228">(1)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-228">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6ddb5-229">**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-229">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="6ddb5-230">(2)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-230">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="6ddb5-231">**這個裝置的驅動程式可能已損毀，或您系統的記憶體或其他資源可能不足。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-231">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="6ddb5-232">(3)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-232">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6ddb5-233">**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-233">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="6ddb5-234">(4)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-234">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="6ddb5-235">**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-235">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="6ddb5-236">(5)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-236">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="6ddb5-237">**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-237">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="6ddb5-238">(6)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-238">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="6ddb5-239">**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-239">**Cannot filter.**</span></span> <span data-ttu-id="6ddb5-240">(7)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-240">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="6ddb5-241">**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-241">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="6ddb5-242">(8)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-242">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="6ddb5-243">**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-243">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="6ddb5-244">(9)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-244">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="6ddb5-245">**這個裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-245">**This device cannot start.**</span></span> <span data-ttu-id="6ddb5-246">(10)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-246">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="6ddb5-247">**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-247">**This device failed.**</span></span> <span data-ttu-id="6ddb5-248">(11)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-248">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="6ddb5-249">**這個裝置沒有足夠資源可供使用。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-249">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="6ddb5-250"> (12) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-250">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="6ddb5-251">**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-251">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="6ddb5-252">(13)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-252">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="6ddb5-253">**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-253">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="6ddb5-254">(14)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-254">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="6ddb5-255">**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-255">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="6ddb5-256">(15)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-256">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="6ddb5-257">**Windows 無法識別這個裝置所使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-257">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="6ddb5-258">(16)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-258">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="6ddb5-259">**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-259">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="6ddb5-260">(17)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-260">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6ddb5-261">**重新安裝這個裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-261">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="6ddb5-262">(18)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-262">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="6ddb5-263">**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-263">**Failure using the VxD loader.**</span></span> <span data-ttu-id="6ddb5-264">(19)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-264">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6ddb5-265">**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-265">**Your registry might be corrupted.**</span></span> <span data-ttu-id="6ddb5-266">(20)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-266">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="6ddb5-267">**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-267">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="6ddb5-268">(21)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-268">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="6ddb5-269">**這個裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-269">**This device is disabled.**</span></span> <span data-ttu-id="6ddb5-270">(22)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-270">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="6ddb5-271">**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-271">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="6ddb5-272">(23)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-272">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="6ddb5-273">**這個裝置可能不存在、運作不正確、或並未安裝所有的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-273">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="6ddb5-274">(24)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-274">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6ddb5-275">**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-275">**Windows is still setting up this device.**</span></span> <span data-ttu-id="6ddb5-276">(25)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-276">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6ddb5-277">**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-277">**Windows is still setting up this device.**</span></span> <span data-ttu-id="6ddb5-278">(26)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-278">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="6ddb5-279">**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-279">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="6ddb5-280">(27)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-280">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="6ddb5-281">**這個裝置的驅動程式尚未安裝。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-281">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="6ddb5-282">(28)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-282">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="6ddb5-283">**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-283">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="6ddb5-284">(29)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-284">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="6ddb5-285">**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-285">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="6ddb5-286">(30)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-286">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6ddb5-287">**這個裝置並未正確執行，因為 Windows 無法載入這個裝置必需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-287">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="6ddb5-288"> (31) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-288">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6ddb5-289">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-289">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-290">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-291">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-292">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-292">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-293">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-293">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="6ddb5-294">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ddb5-295">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-295">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-296">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-297">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-298">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-298">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-299">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-299">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="6ddb5-300">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-300">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="6ddb5-301">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ddb5-302">**說明**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-302">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-303">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-304">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-305">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-305">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-306">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-306">A textual description of the object.</span></span>

<span data-ttu-id="6ddb5-307">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-307">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ddb5-308">**DesignCapacity**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-308">**DesignCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-309">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-309">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-310">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-311">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 便攜電池 \| 002.8」 ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫瓦-小時" ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-311">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-312">以毫瓦時數設計的電池容量。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-312">Designed capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="6ddb5-313">如果不支援此屬性，請輸入0。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-313">If this property is not supported, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="6ddb5-314">**DesignVoltage**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-314">**DesignVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-315">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-315">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-316">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-317">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 便攜電池 \| 002.9」 ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫伏" ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-317">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-318">以毫伏為單位的電池電壓。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-318">Designed voltage of the battery in millivolts.</span></span> <span data-ttu-id="6ddb5-319">如果不支援此屬性，請輸入0。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-319">If this attribute is not supported, enter 0.</span></span>

<span data-ttu-id="6ddb5-320">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-320">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="6ddb5-321">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-321">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-322">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-323">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-324">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-324">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-325">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-325">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="6ddb5-326">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-326">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ddb5-327">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-327">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-328">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-328">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-329">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-330">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-330">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="6ddb5-331">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ddb5-332">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-332">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-333">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-334">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-335">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-335">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="6ddb5-336">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-336">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ddb5-337">**EstimatedChargeRemaining**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-337">**EstimatedChargeRemaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-338">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-338">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-339">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-340">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「百分比」 ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-340">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-341">剩餘完整費用的估計百分比。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-341">Estimated percentage of the remaining full charge.</span></span>

</dd> <dt>

<span data-ttu-id="6ddb5-342">**EstimatedRunTime**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-342">**EstimatedRunTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-343">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-344">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-345">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 便攜電池 \| 002.15 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 分鐘 ") </span><span class="sxs-lookup"><span data-stu-id="6ddb5-345">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-346">以分鐘為單位的預估時間（以分鐘為單位），在目前的負載條件下，如果公用程式電源關閉、遺失並保持關閉狀態，或膝上型電腦與電源中斷連線，則會在目前的負載狀況下耗盡電池計量。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-346">Estimated time, in minutes, until the battery charge is depleted under the present load conditions if the utility power is off, is lost and remains off, or if a laptop is disconnected from a power source.</span></span>

</dd> <dt>

<span data-ttu-id="6ddb5-347">**ExpectedLife**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-347">**ExpectedLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-348">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-349">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-350">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "分鐘" ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-350">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-351">電池的預期存留期（以分鐘為單位）（假設電池已完全收費）。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-351">Battery's expected lifetime, in minutes, assuming that the battery is fully charged.</span></span> <span data-ttu-id="6ddb5-352">此屬性代表電池的預期存留期總計，而不是其目前剩餘的存留期（由 **EstimatedRunTime** 屬性工作表示）。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-352">This property represents the total expected life of the battery, not its current remaining life, which is indicated by the **EstimatedRunTime** property.</span></span>

</dd> <dt>

<span data-ttu-id="6ddb5-353">**FullChargeCapacity**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-353">**FullChargeCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-354">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-354">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-355">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-356">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 便攜電池 \| 002.11」 ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫瓦-小時" ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-356">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-357">電池的完整費用（以毫瓦時數為單位）。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-357">The full charge capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="6ddb5-358">將此值與 **DesignCapacity** 屬性進行比較，以判斷電池何時需要更換。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-358">Compare this value to the **DesignCapacity** property to determine when the battery requires replacement.</span></span> <span data-ttu-id="6ddb5-359">當 **FullChargeCapacity** 屬性低於 **DesignCapacity** 屬性的80% 時，通常會發生電池的終端壽命。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-359">A battery's end-life is typically when the **FullChargeCapacity** property falls below 80 percent of the **DesignCapacity** property.</span></span> <span data-ttu-id="6ddb5-360">如果不支援此屬性，請輸入0。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-360">If this property is not supported, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="6ddb5-361">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-361">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-362">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-362">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-363">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-364">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="6ddb5-364">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-365">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-365">Indicates when the object was installed.</span></span> <span data-ttu-id="6ddb5-366">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-366">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6ddb5-367">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-367">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ddb5-368">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-368">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-369">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-369">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-370">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-371">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-371">Last error code reported by the logical device.</span></span>

<span data-ttu-id="6ddb5-372">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-372">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ddb5-373">**MaxRechargeTime**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-373">**MaxRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-374">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-375">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-376">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "分鐘" ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-376">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-377">完全充電電池的最長時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-377">Maximum time, in minutes, to fully charge the battery.</span></span> <span data-ttu-id="6ddb5-378">此屬性代表將完全耗盡的電池充電的時間，而不是目前剩餘的充電時間（在 **TimeToFullCharge** 屬性中表示）。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-378">This property represents the time to recharge a fully depleted battery, not the current remaining charging time, which is indicated in the **TimeToFullCharge** property.</span></span>

</dd> <dt>

<span data-ttu-id="6ddb5-379">**名稱**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-379">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-380">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-381">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-382">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-382">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-383">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-383">Label by which the object is known.</span></span> <span data-ttu-id="6ddb5-384">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-384">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="6ddb5-385">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ddb5-386">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-386">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-387">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-388">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-389">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-389">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-390">指出邏輯裝置的 Win32 隨插即用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-390">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="6ddb5-391">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="6ddb5-391">Example: "\*PNP030b"</span></span>

<span data-ttu-id="6ddb5-392">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ddb5-393">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-393">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-394">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="6ddb5-394">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-395">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-396">指出邏輯裝置的特定電源相關功能。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-396">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="6ddb5-397">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-397">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6ddb5-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-399">電源相關的容量未知。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-399">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="6ddb5-400"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-400"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-401">此裝置不支援與電源相關的容量。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-401">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6ddb5-402"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-402"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-403">電源相關容量已停用。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-403">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6ddb5-404"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-404"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-405">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-405">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="6ddb5-406"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-406"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-407">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-407">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="6ddb5-408"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-408"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-409">支援 **SetPowerState** 方法。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-409">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="6ddb5-410">這個方法可在父 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-410">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="6ddb5-411">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-411">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="6ddb5-412"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-412"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-413">您可以叫用 **SetPowerState** 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) 。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-413">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="6ddb5-414"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-414"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6ddb5-415">您可以叫用 **SetPowerState** 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) ，並將 *時間* 參數設定為特定日期和時間（或間隔），以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-415">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6ddb5-416">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-416">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-417">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-417">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-418">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-419">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-419">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="6ddb5-420">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-420">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="6ddb5-421">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-421">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="6ddb5-422">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-422">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="6ddb5-423">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-423">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ddb5-424">**SmartBatteryVersion**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-424">**SmartBatteryVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-425">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-426">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-426">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-427">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 便攜電池 \| 002.10」 ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-427">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.10")</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-428">此電池所支援的智慧型電池資料規格版本號碼。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-428">Smart battery data-specification version number that is supported by this battery.</span></span> <span data-ttu-id="6ddb5-429">如果電池不支援此功能，此值應保留空白。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-429">If the battery does not support this function, the value should be left empty.</span></span>

</dd> <dt>

<span data-ttu-id="6ddb5-430">**狀態**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-430">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-431">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-431">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-432">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-432">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-433">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-433">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-434">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-434">String that indicates the current status of the object.</span></span> <span data-ttu-id="6ddb5-435">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-435">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="6ddb5-436">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-436">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="6ddb5-437">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-437">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="6ddb5-438">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-438">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6ddb5-439">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-439">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6ddb5-440">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-440">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6ddb5-441">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-441">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6ddb5-442">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="6ddb5-442">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6ddb5-443">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-443">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6ddb5-444">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-444">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6ddb5-445">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-445">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6ddb5-446">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-446">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6ddb5-447">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-447">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6ddb5-448">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-448">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6ddb5-449">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-449">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6ddb5-450">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-450">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6ddb5-451">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-451">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6ddb5-452">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-452">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6ddb5-453">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-453">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6ddb5-454">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-454">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6ddb5-455">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-455">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-456">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-456">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-457">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-458">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="6ddb5-458">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-459">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-459">State of the logical device.</span></span> <span data-ttu-id="6ddb5-460">如果此屬性不適用於邏輯裝置，則應該使用值 5 ( 「不適用」 ) 。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-460">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="6ddb5-461">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-461">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6ddb5-462">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-462">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6ddb5-463">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-463">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6ddb5-464">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-464">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6ddb5-465">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-465">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6ddb5-466">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-466">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6ddb5-467">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-467">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-468">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-469">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-470">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-470">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-471">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-471">The scoping system's creation class name.</span></span>

<span data-ttu-id="6ddb5-472">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-472">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ddb5-473">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-473">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-474">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-475">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-476">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6ddb5-476">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-477">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-477">The scoping system's name.</span></span>

<span data-ttu-id="6ddb5-478">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ddb5-479">**TimeOnBattery**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-479">**TimeOnBattery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-480">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-480">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-481">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-482">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「秒」 ) </span><span class="sxs-lookup"><span data-stu-id="6ddb5-482">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-483">電腦系統的 UPS 上一次切換到電池電源，或自上次重新開機系統或 UPS 後的時間量（以較小者為准）的經過時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-483">Elapsed time, in seconds, since the computer system's UPS last switched to battery power, or the amount of time since the system or UPS was last restarted, whichever is less.</span></span> <span data-ttu-id="6ddb5-484">如果電池為「線上」，則會傳回0值。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-484">A value of 0 is returned if the battery is "online."</span></span>

</dd> <dt>

<span data-ttu-id="6ddb5-485">**TimeToFullCharge**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-485">**TimeToFullCharge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ddb5-486">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-486">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-487">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ddb5-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ddb5-488">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 便攜電池 \| 002.16 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 分鐘 ") </span><span class="sxs-lookup"><span data-stu-id="6ddb5-488">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="6ddb5-489">以分鐘為單位的剩餘時間（以分鐘為單位），以目前的充電費率和使用方式完全收取電池費用。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-489">Remaining time, in minutes, to charge the battery fully at the current charging rate and use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ddb5-490">備註</span><span class="sxs-lookup"><span data-stu-id="6ddb5-490">Remarks</span></span>

<span data-ttu-id="6ddb5-491">**Cim \_ 電池** 類別衍生自 [**cim \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-491">The **CIM\_Battery** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="6ddb5-492">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-492">WMI does not implement this class.</span></span> <span data-ttu-id="6ddb5-493">如需衍生自 **CIM \_ 電池** 之類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-493">For more information about classes derived from **CIM\_Battery**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="6ddb5-494">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-494">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6ddb5-495">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="6ddb5-495">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ddb5-496">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ddb5-496">Requirements</span></span>



| <span data-ttu-id="6ddb5-497">需求</span><span class="sxs-lookup"><span data-stu-id="6ddb5-497">Requirement</span></span> | <span data-ttu-id="6ddb5-498">值</span><span class="sxs-lookup"><span data-stu-id="6ddb5-498">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ddb5-499">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6ddb5-499">Minimum supported client</span></span><br/> | <span data-ttu-id="6ddb5-500">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ddb5-500">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6ddb5-501">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6ddb5-501">Minimum supported server</span></span><br/> | <span data-ttu-id="6ddb5-502">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ddb5-502">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6ddb5-503">命名空間</span><span class="sxs-lookup"><span data-stu-id="6ddb5-503">Namespace</span></span><br/>                | <span data-ttu-id="6ddb5-504">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6ddb5-504">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6ddb5-505">MOF</span><span class="sxs-lookup"><span data-stu-id="6ddb5-505">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ddb5-506"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ddb5-506"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ddb5-507">DLL</span><span class="sxs-lookup"><span data-stu-id="6ddb5-507">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ddb5-508"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ddb5-508"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ddb5-509">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ddb5-509">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ddb5-510">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="6ddb5-510">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

