---
description: Win32 \_ 風扇 WMI 類別代表電腦系統中的風扇裝置屬性。 例如，CPU 冷卻風扇。
ms.assetid: ff48b788-d759-45cf-812f-a80dba0c9192
ms.tgt_platform: multiple
title: Win32_Fan 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Fan
- Win32_Fan.Reset
- Win32_Fan.SetPowerState
- Win32_Fan.SetSpeed
- Win32_Fan.ActiveCooling
- Win32_Fan.Availability
- Win32_Fan.Caption
- Win32_Fan.ConfigManagerErrorCode
- Win32_Fan.ConfigManagerUserConfig
- Win32_Fan.CreationClassName
- Win32_Fan.Description
- Win32_Fan.DesiredSpeed
- Win32_Fan.DeviceID
- Win32_Fan.ErrorCleared
- Win32_Fan.ErrorDescription
- Win32_Fan.InstallDate
- Win32_Fan.LastErrorCode
- Win32_Fan.Name
- Win32_Fan.PNPDeviceID
- Win32_Fan.PowerManagementCapabilities
- Win32_Fan.PowerManagementSupported
- Win32_Fan.Status
- Win32_Fan.StatusInfo
- Win32_Fan.SystemCreationClassName
- Win32_Fan.SystemName
- Win32_Fan.VariableSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 67f248b74fa665f30c9c3b9ffa51cb8cee5a5782
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510434"
---
# <a name="win32_fan-class"></a><span data-ttu-id="c65b5-104">Win32 \_ 風扇類別</span><span class="sxs-lookup"><span data-stu-id="c65b5-104">Win32\_Fan class</span></span>

<span data-ttu-id="c65b5-105">**Win32 \_ 風扇** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表電腦系統中的風扇裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="c65b5-105">The **Win32\_Fan** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a fan device in the computer system.</span></span> <span data-ttu-id="c65b5-106">例如，CPU 冷卻風扇。</span><span class="sxs-lookup"><span data-stu-id="c65b5-106">For example, the CPU cooling fan.</span></span>

<span data-ttu-id="c65b5-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c65b5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c65b5-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="c65b5-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c65b5-109">語法</span><span class="sxs-lookup"><span data-stu-id="c65b5-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFAB5-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_Fan : CIM_Fan
{
  boolean  ActiveCooling;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  uint64   DesiredSpeed;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  boolean  VariableSpeed;
};
```

## <a name="members"></a><span data-ttu-id="c65b5-110">成員</span><span class="sxs-lookup"><span data-stu-id="c65b5-110">Members</span></span>

<span data-ttu-id="c65b5-111">**Win32 \_ 風扇** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c65b5-111">The **Win32\_Fan** class has these types of members:</span></span>

-   [<span data-ttu-id="c65b5-112">方法</span><span class="sxs-lookup"><span data-stu-id="c65b5-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="c65b5-113">屬性</span><span class="sxs-lookup"><span data-stu-id="c65b5-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c65b5-114">方法</span><span class="sxs-lookup"><span data-stu-id="c65b5-114">Methods</span></span>

<span data-ttu-id="c65b5-115">**Win32 \_ 風扇** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c65b5-115">The **Win32\_Fan** class has these methods.</span></span>



| <span data-ttu-id="c65b5-116">方法</span><span class="sxs-lookup"><span data-stu-id="c65b5-116">Method</span></span>            | <span data-ttu-id="c65b5-117">描述</span><span class="sxs-lookup"><span data-stu-id="c65b5-117">Description</span></span>                                                                                                                                                                                  |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c65b5-118">**重設**</span><span class="sxs-lookup"><span data-stu-id="c65b5-118">**Reset**</span></span>         | <span data-ttu-id="c65b5-119">未實作。</span><span class="sxs-lookup"><span data-stu-id="c65b5-119">Not implemented.</span></span> <span data-ttu-id="c65b5-120">若要執行此方法，請參閱 [**CIM \_ 風扇**](cim-fan.md)中的 [**Reset**](reset-method-in-class-cim-controller.md)方法以取得檔。</span><span class="sxs-lookup"><span data-stu-id="c65b5-120">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Fan**](cim-fan.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="c65b5-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c65b5-121">**SetPowerState**</span></span> | <span data-ttu-id="c65b5-122">未實作。</span><span class="sxs-lookup"><span data-stu-id="c65b5-122">Not implemented.</span></span> <span data-ttu-id="c65b5-123">若要執行此方法，請參閱 [**CIM \_ 風扇**](cim-fan.md)中適用于檔的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="c65b5-123">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Fan**](cim-fan.md) for documentation.</span></span><br/> |
| <span data-ttu-id="c65b5-124">**SetSpeed**</span><span class="sxs-lookup"><span data-stu-id="c65b5-124">**SetSpeed**</span></span>      | <span data-ttu-id="c65b5-125">未實作。</span><span class="sxs-lookup"><span data-stu-id="c65b5-125">Not implemented.</span></span><br/>                                                                                                                                                                  |



 

### <a name="properties"></a><span data-ttu-id="c65b5-126">屬性</span><span class="sxs-lookup"><span data-stu-id="c65b5-126">Properties</span></span>

<span data-ttu-id="c65b5-127">**Win32 \_ 風扇** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c65b5-127">The **Win32\_Fan** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c65b5-128">**ActiveCooling**</span><span class="sxs-lookup"><span data-stu-id="c65b5-128">**ActiveCooling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65b5-129">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c65b5-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c65b5-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c65b5-131">若 **為 True**，則冷卻裝置會提供作用中的 (，而非被動) 冷卻。</span><span class="sxs-lookup"><span data-stu-id="c65b5-131">If **True**, the cooling device provides active (as opposed to passive) cooling.</span></span>

<span data-ttu-id="c65b5-132">這個屬性繼承自 [**CIM \_ CoolingDevice**](cim-coolingdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c65b5-132">This property is inherited from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c65b5-133">**可用性**</span><span class="sxs-lookup"><span data-stu-id="c65b5-133">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65b5-134">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c65b5-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c65b5-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-136">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="c65b5-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="c65b5-137">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="c65b5-137">Availability and status of the device.</span></span>

<span data-ttu-id="c65b5-138">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c65b5-138">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c65b5-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c65b5-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c65b5-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="c65b5-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="c65b5-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="c65b5-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-142">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="c65b5-142">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="c65b5-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="c65b5-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="c65b5-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="c65b5-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c65b5-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="c65b5-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="c65b5-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="c65b5-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="c65b5-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="c65b5-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="c65b5-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="c65b5-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c65b5-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="c65b5-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="c65b5-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="c65b5-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="c65b5-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="c65b5-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="c65b5-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="c65b5-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-153">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="c65b5-153">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="c65b5-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="c65b5-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-155">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="c65b5-155">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="c65b5-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="c65b5-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-157">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="c65b5-157">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="c65b5-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="c65b5-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="c65b5-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="c65b5-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-160">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="c65b5-160">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="c65b5-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="c65b5-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-162">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="c65b5-162">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="c65b5-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="c65b5-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-164">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="c65b5-164">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="c65b5-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="c65b5-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-166">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="c65b5-166">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="c65b5-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="c65b5-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-168">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="c65b5-168">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c65b5-169">**標題**</span><span class="sxs-lookup"><span data-stu-id="c65b5-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65b5-170">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c65b5-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c65b5-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-172">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="c65b5-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c65b5-173">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="c65b5-173">Short description of the object a one-line string.</span></span>

<span data-ttu-id="c65b5-174">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c65b5-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c65b5-175">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c65b5-175">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65b5-176">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c65b5-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c65b5-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-178">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="c65b5-178">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c65b5-179">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c65b5-179">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="c65b5-180">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c65b5-180">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="c65b5-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="c65b5-182"> (0)</span><span class="sxs-lookup"><span data-stu-id="c65b5-182">(0)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-183">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="c65b5-183">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="c65b5-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="c65b5-185">(1)</span><span class="sxs-lookup"><span data-stu-id="c65b5-185">(1)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-186">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="c65b5-186">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c65b5-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="c65b5-188">(2)</span><span class="sxs-lookup"><span data-stu-id="c65b5-188">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="c65b5-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="c65b5-190">(3)</span><span class="sxs-lookup"><span data-stu-id="c65b5-190">(3)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-191">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="c65b5-191">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c65b5-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="c65b5-193">(4)</span><span class="sxs-lookup"><span data-stu-id="c65b5-193">(4)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-194">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="c65b5-194">Device is not working properly.</span></span> <span data-ttu-id="c65b5-195">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="c65b5-195">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="c65b5-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="c65b5-197">(5)</span><span class="sxs-lookup"><span data-stu-id="c65b5-197">(5)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-198">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="c65b5-198">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="c65b5-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="c65b5-200">(6)</span><span class="sxs-lookup"><span data-stu-id="c65b5-200">(6)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-201">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="c65b5-201">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="c65b5-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="c65b5-203">(7)</span><span class="sxs-lookup"><span data-stu-id="c65b5-203">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="c65b5-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="c65b5-205">(8)</span><span class="sxs-lookup"><span data-stu-id="c65b5-205">(8)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-206">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="c65b5-206">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="c65b5-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="c65b5-208">(9)</span><span class="sxs-lookup"><span data-stu-id="c65b5-208">(9)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-209">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="c65b5-209">Device is not working properly.</span></span> <span data-ttu-id="c65b5-210">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="c65b5-210">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="c65b5-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="c65b5-212">(10)</span><span class="sxs-lookup"><span data-stu-id="c65b5-212">(10)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-213">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="c65b5-213">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="c65b5-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="c65b5-215">(11)</span><span class="sxs-lookup"><span data-stu-id="c65b5-215">(11)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-216">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="c65b5-216">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="c65b5-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="c65b5-218"> (12) </span><span class="sxs-lookup"><span data-stu-id="c65b5-218">(12)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-219">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="c65b5-219">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="c65b5-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="c65b5-221">(13)</span><span class="sxs-lookup"><span data-stu-id="c65b5-221">(13)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-222">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="c65b5-222">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="c65b5-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="c65b5-224">(14)</span><span class="sxs-lookup"><span data-stu-id="c65b5-224">(14)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-225">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="c65b5-225">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="c65b5-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="c65b5-227">(15)</span><span class="sxs-lookup"><span data-stu-id="c65b5-227">(15)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-228">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="c65b5-228">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="c65b5-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="c65b5-230">(16)</span><span class="sxs-lookup"><span data-stu-id="c65b5-230">(16)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-231">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="c65b5-231">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="c65b5-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="c65b5-233">(17)</span><span class="sxs-lookup"><span data-stu-id="c65b5-233">(17)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-234">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="c65b5-234">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c65b5-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="c65b5-236">(18)</span><span class="sxs-lookup"><span data-stu-id="c65b5-236">(18)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-237">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="c65b5-237">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="c65b5-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="c65b5-239">(19)</span><span class="sxs-lookup"><span data-stu-id="c65b5-239">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c65b5-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="c65b5-241">(20)</span><span class="sxs-lookup"><span data-stu-id="c65b5-241">(20)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-242">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="c65b5-242">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="c65b5-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="c65b5-244">(21)</span><span class="sxs-lookup"><span data-stu-id="c65b5-244">(21)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-245">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="c65b5-245">System failure.</span></span> <span data-ttu-id="c65b5-246">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="c65b5-246">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="c65b5-247">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="c65b5-247">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="c65b5-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="c65b5-249">(22)</span><span class="sxs-lookup"><span data-stu-id="c65b5-249">(22)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-250">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="c65b5-250">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="c65b5-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="c65b5-252">(23)</span><span class="sxs-lookup"><span data-stu-id="c65b5-252">(23)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-253">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="c65b5-253">System failure.</span></span> <span data-ttu-id="c65b5-254">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="c65b5-254">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="c65b5-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="c65b5-256">(24)</span><span class="sxs-lookup"><span data-stu-id="c65b5-256">(24)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-257">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="c65b5-257">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c65b5-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c65b5-259">(25)</span><span class="sxs-lookup"><span data-stu-id="c65b5-259">(25)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-260">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="c65b5-260">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c65b5-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c65b5-262">(26)</span><span class="sxs-lookup"><span data-stu-id="c65b5-262">(26)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-263">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="c65b5-263">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="c65b5-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="c65b5-265">(27)</span><span class="sxs-lookup"><span data-stu-id="c65b5-265">(27)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-266">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="c65b5-266">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="c65b5-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="c65b5-268">(28)</span><span class="sxs-lookup"><span data-stu-id="c65b5-268">(28)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-269">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="c65b5-269">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="c65b5-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="c65b5-271">(29)</span><span class="sxs-lookup"><span data-stu-id="c65b5-271">(29)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-272">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="c65b5-272">Device is disabled.</span></span> <span data-ttu-id="c65b5-273">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="c65b5-273">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="c65b5-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="c65b5-275">(30)</span><span class="sxs-lookup"><span data-stu-id="c65b5-275">(30)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-276">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="c65b5-276">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c65b5-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="c65b5-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="c65b5-278"> (31) </span><span class="sxs-lookup"><span data-stu-id="c65b5-278">(31)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-279">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="c65b5-279">Device is not working properly.</span></span> <span data-ttu-id="c65b5-280">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="c65b5-280">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c65b5-281">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="c65b5-281">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65b5-282">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c65b5-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-283">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c65b5-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-284">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="c65b5-284">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c65b5-285">若 **為 True**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="c65b5-285">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="c65b5-286">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c65b5-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c65b5-287">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c65b5-287">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65b5-288">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c65b5-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-289">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c65b5-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-290">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c65b5-290">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c65b5-291">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="c65b5-291">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="c65b5-292">當搭配類別的其他索引鍵屬性使用時，屬性允許唯一識別此類別的所有實例和其子類別。</span><span class="sxs-lookup"><span data-stu-id="c65b5-292">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="c65b5-293">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c65b5-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c65b5-294">**說明**</span><span class="sxs-lookup"><span data-stu-id="c65b5-294">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65b5-295">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c65b5-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-296">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c65b5-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-297">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="c65b5-297">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c65b5-298">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="c65b5-298">Description of the object.</span></span>

<span data-ttu-id="c65b5-299">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c65b5-299">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c65b5-300">**DesiredSpeed**</span><span class="sxs-lookup"><span data-stu-id="c65b5-300">**DesiredSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65b5-301">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c65b5-301">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-302">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c65b5-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-303">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「每分鐘的旋轉」 ) </span><span class="sxs-lookup"><span data-stu-id="c65b5-303">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="c65b5-304">目前要求的風扇速度（在每分鐘的旋轉中定義），當支援變速風扇時 (**VariableSpeed** 為 **TRUE**) 。</span><span class="sxs-lookup"><span data-stu-id="c65b5-304">Currently requested fan speed, defined in revolutions per minute, when a variable speed fan is supported (**VariableSpeed** is **TRUE**).</span></span> <span data-ttu-id="c65b5-305">目前的速度取決於與使用 [**cim \_ AssociatedSensor**](cim-associatedsensor.md)關聯性之風扇相關聯的感應器 ([**CIM \_ 流速**](cim-tachometer.md)) 。</span><span class="sxs-lookup"><span data-stu-id="c65b5-305">The current speed is determined by a sensor ([**CIM\_Tachometer**](cim-tachometer.md)) that is associated with the fan using the [**CIM\_AssociatedSensor**](cim-associatedsensor.md) relationship.</span></span>

<span data-ttu-id="c65b5-306">這個屬性繼承自 [**CIM \_ 風扇**](cim-fan.md)。</span><span class="sxs-lookup"><span data-stu-id="c65b5-306">This property is inherited from [**CIM\_Fan**](cim-fan.md).</span></span>

<span data-ttu-id="c65b5-307">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="c65b5-307">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c65b5-308">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c65b5-308">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65b5-309">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c65b5-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-310">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c65b5-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-311">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "DeviceId" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="c65b5-311">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="c65b5-312">識別風扇裝置。</span><span class="sxs-lookup"><span data-stu-id="c65b5-312">Identifies the fan device.</span></span> <span data-ttu-id="c65b5-313">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c65b5-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c65b5-314">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="c65b5-314">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65b5-315">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c65b5-315">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-316">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c65b5-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c65b5-317">若 **為 True**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="c65b5-317">If **True**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="c65b5-318">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c65b5-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c65b5-319">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c65b5-319">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65b5-320">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c65b5-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c65b5-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c65b5-322">自由格式的字串提供 **LastErrorCode** 屬性中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c65b5-322">Free-form string supplying more information about the error recorded in **LastErrorCode** property, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="c65b5-323">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c65b5-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c65b5-324">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c65b5-324">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65b5-325">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="c65b5-325">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-326">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c65b5-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-327">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="c65b5-327">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c65b5-328">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="c65b5-328">Date and time the object was installed.</span></span> <span data-ttu-id="c65b5-329">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="c65b5-329">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c65b5-330">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c65b5-330">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c65b5-331">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c65b5-331">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65b5-332">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c65b5-332">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-333">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c65b5-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c65b5-334">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c65b5-334">Last error code reported by the logical device.</span></span>

<span data-ttu-id="c65b5-335">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c65b5-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c65b5-336">**名稱**</span><span class="sxs-lookup"><span data-stu-id="c65b5-336">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65b5-337">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c65b5-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-338">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c65b5-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-339">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="c65b5-339">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c65b5-340">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="c65b5-340">Label by which the object is known.</span></span> <span data-ttu-id="c65b5-341">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="c65b5-341">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="c65b5-342">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c65b5-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c65b5-343">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="c65b5-343">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65b5-344">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c65b5-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-345">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c65b5-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-346">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="c65b5-346">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c65b5-347">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="c65b5-347">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="c65b5-348">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c65b5-348">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="c65b5-349">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="c65b5-349">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="c65b5-350">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c65b5-350">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65b5-351">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="c65b5-351">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-352">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c65b5-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c65b5-353">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="c65b5-353">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="c65b5-354">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="c65b5-354">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c65b5-355"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c65b5-355"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="c65b5-356"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="c65b5-356"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-357">此裝置不支援與電源相關的容量。</span><span class="sxs-lookup"><span data-stu-id="c65b5-357">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c65b5-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="c65b5-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c65b5-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="c65b5-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-360">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="c65b5-360">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="c65b5-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="c65b5-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-362">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="c65b5-362">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="c65b5-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="c65b5-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-364">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c65b5-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="c65b5-365">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="c65b5-365">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="c65b5-366">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="c65b5-366">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="c65b5-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="c65b5-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-368">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="c65b5-368">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="c65b5-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="c65b5-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c65b5-370">支援計時 Power-On</span><span class="sxs-lookup"><span data-stu-id="c65b5-370">Timed Power-On Supported</span></span>

<span data-ttu-id="c65b5-371">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="c65b5-371">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c65b5-372">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="c65b5-372">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65b5-373">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c65b5-373">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-374">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c65b5-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c65b5-375">若 **為 True**，則裝置可以是電源管理 (可進入暫停模式，依此類推) 。</span><span class="sxs-lookup"><span data-stu-id="c65b5-375">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="c65b5-376">屬性不表示電源管理功能目前已啟用，只有邏輯裝置能夠進行電源管理。</span><span class="sxs-lookup"><span data-stu-id="c65b5-376">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="c65b5-377">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c65b5-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c65b5-378">**狀態**</span><span class="sxs-lookup"><span data-stu-id="c65b5-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65b5-379">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c65b5-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-380">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c65b5-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-381">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="c65b5-381">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c65b5-382">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="c65b5-382">Current status of the object.</span></span> <span data-ttu-id="c65b5-383">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="c65b5-383">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c65b5-384">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="c65b5-384">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="c65b5-385">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="c65b5-385">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c65b5-386">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="c65b5-386">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c65b5-387">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="c65b5-387">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c65b5-388">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c65b5-388">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c65b5-389">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="c65b5-389">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c65b5-390">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="c65b5-390">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c65b5-391">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="c65b5-391">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c65b5-392">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="c65b5-392">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c65b5-393">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="c65b5-393">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c65b5-394">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="c65b5-394">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c65b5-395">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="c65b5-395">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c65b5-396">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="c65b5-396">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c65b5-397">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="c65b5-397">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c65b5-398">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="c65b5-398">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c65b5-399">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="c65b5-399">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c65b5-400">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="c65b5-400">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c65b5-401">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="c65b5-401">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c65b5-402">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c65b5-402">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65b5-403">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c65b5-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-404">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c65b5-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-405">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="c65b5-405">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c65b5-406">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="c65b5-406">State of the logical device.</span></span> <span data-ttu-id="c65b5-407">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="c65b5-407">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="c65b5-408">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c65b5-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c65b5-409">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c65b5-409">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c65b5-410">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="c65b5-410">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c65b5-411">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="c65b5-411">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c65b5-412">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="c65b5-412">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c65b5-413">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="c65b5-413">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c65b5-414">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c65b5-414">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65b5-415">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c65b5-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-416">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c65b5-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-417">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c65b5-417">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c65b5-418">範圍電腦之 **CreationClassName** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="c65b5-418">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="c65b5-419">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c65b5-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c65b5-420">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c65b5-420">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65b5-421">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c65b5-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-422">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c65b5-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-423">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c65b5-423">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c65b5-424">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="c65b5-424">Name of the scoping system.</span></span>

<span data-ttu-id="c65b5-425">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c65b5-425">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c65b5-426">**VariableSpeed**</span><span class="sxs-lookup"><span data-stu-id="c65b5-426">**VariableSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65b5-427">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c65b5-427">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c65b5-428">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c65b5-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c65b5-429">若 **為 True**，則風扇支援可變速度。</span><span class="sxs-lookup"><span data-stu-id="c65b5-429">If **True**, the fan supports variable speeds.</span></span>

<span data-ttu-id="c65b5-430">這個屬性繼承自 [**CIM \_ 風扇**](cim-fan.md)。</span><span class="sxs-lookup"><span data-stu-id="c65b5-430">This property is inherited from [**CIM\_Fan**](cim-fan.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c65b5-431">備註</span><span class="sxs-lookup"><span data-stu-id="c65b5-431">Remarks</span></span>

<span data-ttu-id="c65b5-432">**Win32 \_ 風扇** 類別衍生自 [**CIM \_ 風扇**](cim-fan.md)。</span><span class="sxs-lookup"><span data-stu-id="c65b5-432">The **Win32\_Fan** class is derived from [**CIM\_Fan**](cim-fan.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c65b5-433">範例</span><span class="sxs-lookup"><span data-stu-id="c65b5-433">Examples</span></span>

<span data-ttu-id="c65b5-434">[列出電腦風扇資訊](https://Gallery.TechNet.Microsoft.Com/d1534503-704f-4450-8dab-f3e760bf818c)PowerShell 範例會捕獲電腦上所安裝之冷卻風扇的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c65b5-434">The [List Computer Fan Information](https://Gallery.TechNet.Microsoft.Com/d1534503-704f-4450-8dab-f3e760bf818c) PowerShell sample retrieves information about the cooling fans installed in a computer.</span></span>

<span data-ttu-id="c65b5-435">下列範例會捕獲電腦上所安裝之冷卻風扇的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c65b5-435">The following sample retrieves information about the cooling fans installed on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_Fan") 
 
For Each objItem in colItems 
    Wscript.Echo "Active Cooling: " & objItem.ActiveCooling 
    Wscript.Echo "Availability: " & objItem.Availability 
    Wscript.Echo "Device ID: " & objItem.DeviceID 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Status Information: " & objItem.StatusInfo 
    Wscript.Echo 
Next
```


```PowerShell
$colItems = Get-WmiObject Win32_Fan -Namespace "root\cimv2"
foreach ($objItem in $colItems)
{
    "Active Cooling: " + $objItem.ActiveCooling 
    "Availability: " + $objItem.Availability 
    "Device ID: " + $objItem.DeviceID 
    "Name: " + $objItem.Name 
    "Status Information: " + $objItem.StatusInfo 
}
```





## <a name="requirements"></a><span data-ttu-id="c65b5-436">規格需求</span><span class="sxs-lookup"><span data-stu-id="c65b5-436">Requirements</span></span>



| <span data-ttu-id="c65b5-437">需求</span><span class="sxs-lookup"><span data-stu-id="c65b5-437">Requirement</span></span> | <span data-ttu-id="c65b5-438">值</span><span class="sxs-lookup"><span data-stu-id="c65b5-438">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c65b5-439">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c65b5-439">Minimum supported client</span></span><br/> | <span data-ttu-id="c65b5-440">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c65b5-440">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c65b5-441">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c65b5-441">Minimum supported server</span></span><br/> | <span data-ttu-id="c65b5-442">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c65b5-442">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c65b5-443">命名空間</span><span class="sxs-lookup"><span data-stu-id="c65b5-443">Namespace</span></span><br/>                | <span data-ttu-id="c65b5-444">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c65b5-444">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c65b5-445">MOF</span><span class="sxs-lookup"><span data-stu-id="c65b5-445">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c65b5-446"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="c65b5-446"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c65b5-447">DLL</span><span class="sxs-lookup"><span data-stu-id="c65b5-447">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c65b5-448"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c65b5-448"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c65b5-449">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c65b5-449">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c65b5-450">**CIM \_ 風扇**</span><span class="sxs-lookup"><span data-stu-id="c65b5-450">**CIM\_Fan**</span></span>](cim-fan.md)
</dt> <dt>

[<span data-ttu-id="c65b5-451">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="c65b5-451">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

