---
description: CIM \_ 風扇類別代表風扇冷卻裝置的功能和管理。
ms.assetid: eddfb694-cba1-45e2-998f-f93355520c80
ms.tgt_platform: multiple
title: CIM_Fan 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Fan
- CIM_Fan.ActiveCooling
- CIM_Fan.Availability
- CIM_Fan.Caption
- CIM_Fan.ConfigManagerErrorCode
- CIM_Fan.ConfigManagerUserConfig
- CIM_Fan.CreationClassName
- CIM_Fan.Description
- CIM_Fan.DesiredSpeed
- CIM_Fan.DeviceID
- CIM_Fan.ErrorCleared
- CIM_Fan.ErrorDescription
- CIM_Fan.InstallDate
- CIM_Fan.LastErrorCode
- CIM_Fan.Name
- CIM_Fan.PNPDeviceID
- CIM_Fan.PowerManagementCapabilities
- CIM_Fan.PowerManagementSupported
- CIM_Fan.Status
- CIM_Fan.StatusInfo
- CIM_Fan.SystemCreationClassName
- CIM_Fan.SystemName
- CIM_Fan.VariableSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6a06e0ddebbdadf7cb4e6dd61afa3fa7c178f661
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847362"
---
# <a name="cim_fan-class"></a><span data-ttu-id="feba4-103">CIM \_ 風扇類別</span><span class="sxs-lookup"><span data-stu-id="feba4-103">CIM\_Fan class</span></span>

<span data-ttu-id="feba4-104">**CIM \_ 風扇** 類別代表風扇冷卻裝置的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="feba4-104">The **CIM\_Fan** class represents the capabilities and management of a fan cooling device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="feba4-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="feba4-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="feba4-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="feba4-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="feba4-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="feba4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="feba4-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="feba4-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="feba4-109">語法</span><span class="sxs-lookup"><span data-stu-id="feba4-109">Syntax</span></span>

``` syntax
[UUID("{0A59C856-E3D4-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_Fan : CIM_CoolingDevice
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

## <a name="members"></a><span data-ttu-id="feba4-110">成員</span><span class="sxs-lookup"><span data-stu-id="feba4-110">Members</span></span>

<span data-ttu-id="feba4-111">**CIM \_ 風扇** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="feba4-111">The **CIM\_Fan** class has these types of members:</span></span>

-   [<span data-ttu-id="feba4-112">方法</span><span class="sxs-lookup"><span data-stu-id="feba4-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="feba4-113">屬性</span><span class="sxs-lookup"><span data-stu-id="feba4-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="feba4-114">方法</span><span class="sxs-lookup"><span data-stu-id="feba4-114">Methods</span></span>

<span data-ttu-id="feba4-115">**CIM \_ 風扇** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="feba4-115">The **CIM\_Fan** class has these methods.</span></span>



| <span data-ttu-id="feba4-116">方法</span><span class="sxs-lookup"><span data-stu-id="feba4-116">Method</span></span>                                                         | <span data-ttu-id="feba4-117">描述</span><span class="sxs-lookup"><span data-stu-id="feba4-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="feba4-118">**重設**</span><span class="sxs-lookup"><span data-stu-id="feba4-118">**Reset**</span></span>](reset-method-in-class-cim-fan.md)                 | <span data-ttu-id="feba4-119">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="feba4-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="feba4-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="feba4-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="feba4-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="feba4-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-fan.md) | <span data-ttu-id="feba4-122">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="feba4-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="feba4-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="feba4-123">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="feba4-124">**SetSpeed**</span><span class="sxs-lookup"><span data-stu-id="feba4-124">**SetSpeed**</span></span>](setspeed-method-in-class-cim-fan.md)           | <span data-ttu-id="feba4-125">設定風扇速度。</span><span class="sxs-lookup"><span data-stu-id="feba4-125">Sets the fan speed.</span></span> <span data-ttu-id="feba4-126">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="feba4-126">Not implemented by WMI.</span></span><br/>                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="feba4-127">屬性</span><span class="sxs-lookup"><span data-stu-id="feba4-127">Properties</span></span>

<span data-ttu-id="feba4-128">**CIM \_ 風扇** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="feba4-128">The **CIM\_Fan** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="feba4-129">**ActiveCooling**</span><span class="sxs-lookup"><span data-stu-id="feba4-129">**ActiveCooling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feba4-130">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="feba4-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="feba4-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="feba4-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="feba4-132">若 **為 TRUE**，則冷卻裝置會提供作用中的 (，而非被動) 冷卻。</span><span class="sxs-lookup"><span data-stu-id="feba4-132">If **TRUE**, the cooling device provides active (as opposed to passive) cooling.</span></span>

<span data-ttu-id="feba4-133">這個屬性繼承自 [**CIM \_ CoolingDevice**](cim-coolingdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="feba4-133">This property is inherited from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="feba4-134">**可用性**</span><span class="sxs-lookup"><span data-stu-id="feba4-134">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feba4-135">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="feba4-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="feba4-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="feba4-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="feba4-137">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="feba4-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="feba4-138">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="feba4-138">Availability and status of the device.</span></span>

<span data-ttu-id="feba4-139">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="feba4-139">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="feba4-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="feba4-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="feba4-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="feba4-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="feba4-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="feba4-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="feba4-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="feba4-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="feba4-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="feba4-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="feba4-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="feba4-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="feba4-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="feba4-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="feba4-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="feba4-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="feba4-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="feba4-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="feba4-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="feba4-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="feba4-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="feba4-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="feba4-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="feba4-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="feba4-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="feba4-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-153">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="feba4-153">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="feba4-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="feba4-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-155">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="feba4-155">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="feba4-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="feba4-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-157">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="feba4-157">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="feba4-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="feba4-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="feba4-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="feba4-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-160">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="feba4-160">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="feba4-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="feba4-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-162">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="feba4-162">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="feba4-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="feba4-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-164">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="feba4-164">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="feba4-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="feba4-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-166">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="feba4-166">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="feba4-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="feba4-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-168">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="feba4-168">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="feba4-169">**標題**</span><span class="sxs-lookup"><span data-stu-id="feba4-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feba4-170">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="feba4-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="feba4-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="feba4-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="feba4-172">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="feba4-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="feba4-173">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="feba4-173">Short textual description of the object.</span></span>

<span data-ttu-id="feba4-174">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="feba4-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="feba4-175">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="feba4-175">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feba4-176">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="feba4-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="feba4-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="feba4-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="feba4-178">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="feba4-178">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="feba4-179">Windows 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="feba4-179">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="feba4-180">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="feba4-180">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="feba4-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="feba4-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="feba4-182"> (0)</span><span class="sxs-lookup"><span data-stu-id="feba4-182">(0)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-183">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="feba4-183">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="feba4-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="feba4-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="feba4-185">(1)</span><span class="sxs-lookup"><span data-stu-id="feba4-185">(1)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-186">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="feba4-186">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="feba4-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="feba4-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="feba4-188">(2)</span><span class="sxs-lookup"><span data-stu-id="feba4-188">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="feba4-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="feba4-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="feba4-190">(3)</span><span class="sxs-lookup"><span data-stu-id="feba4-190">(3)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-191">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="feba4-191">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="feba4-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="feba4-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="feba4-193">(4)</span><span class="sxs-lookup"><span data-stu-id="feba4-193">(4)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-194">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="feba4-194">Device is not working properly.</span></span> <span data-ttu-id="feba4-195">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="feba4-195">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="feba4-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="feba4-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="feba4-197">(5)</span><span class="sxs-lookup"><span data-stu-id="feba4-197">(5)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-198">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="feba4-198">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="feba4-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="feba4-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="feba4-200">(6)</span><span class="sxs-lookup"><span data-stu-id="feba4-200">(6)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-201">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="feba4-201">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="feba4-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="feba4-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="feba4-203">(7)</span><span class="sxs-lookup"><span data-stu-id="feba4-203">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="feba4-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="feba4-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="feba4-205">(8)</span><span class="sxs-lookup"><span data-stu-id="feba4-205">(8)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-206">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="feba4-206">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="feba4-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="feba4-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="feba4-208">(9)</span><span class="sxs-lookup"><span data-stu-id="feba4-208">(9)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-209">裝置無法正常運作;控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="feba4-209">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="feba4-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="feba4-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="feba4-211">(10)</span><span class="sxs-lookup"><span data-stu-id="feba4-211">(10)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-212">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="feba4-212">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="feba4-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="feba4-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="feba4-214">(11)</span><span class="sxs-lookup"><span data-stu-id="feba4-214">(11)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-215">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="feba4-215">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="feba4-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="feba4-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="feba4-217"> (12) </span><span class="sxs-lookup"><span data-stu-id="feba4-217">(12)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-218">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="feba4-218">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="feba4-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="feba4-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="feba4-220">(13)</span><span class="sxs-lookup"><span data-stu-id="feba4-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-221">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="feba4-221">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="feba4-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="feba4-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="feba4-223">(14)</span><span class="sxs-lookup"><span data-stu-id="feba4-223">(14)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-224">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="feba4-224">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="feba4-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="feba4-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="feba4-226">(15)</span><span class="sxs-lookup"><span data-stu-id="feba4-226">(15)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-227">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="feba4-227">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="feba4-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="feba4-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="feba4-229">(16)</span><span class="sxs-lookup"><span data-stu-id="feba4-229">(16)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-230">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="feba4-230">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="feba4-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="feba4-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="feba4-232">(17)</span><span class="sxs-lookup"><span data-stu-id="feba4-232">(17)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-233">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="feba4-233">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="feba4-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="feba4-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="feba4-235">(18)</span><span class="sxs-lookup"><span data-stu-id="feba4-235">(18)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-236">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="feba4-236">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="feba4-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="feba4-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="feba4-238">(19)</span><span class="sxs-lookup"><span data-stu-id="feba4-238">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="feba4-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="feba4-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="feba4-240">(20)</span><span class="sxs-lookup"><span data-stu-id="feba4-240">(20)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-241">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="feba4-241">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="feba4-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="feba4-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="feba4-243">(21)</span><span class="sxs-lookup"><span data-stu-id="feba4-243">(21)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-244">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="feba4-244">System failure.</span></span> <span data-ttu-id="feba4-245">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="feba4-245">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="feba4-246">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="feba4-246">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="feba4-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="feba4-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="feba4-248">(22)</span><span class="sxs-lookup"><span data-stu-id="feba4-248">(22)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-249">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="feba4-249">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="feba4-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="feba4-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="feba4-251">(23)</span><span class="sxs-lookup"><span data-stu-id="feba4-251">(23)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-252">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="feba4-252">System failure.</span></span> <span data-ttu-id="feba4-253">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="feba4-253">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="feba4-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="feba4-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="feba4-255">(24)</span><span class="sxs-lookup"><span data-stu-id="feba4-255">(24)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-256">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="feba4-256">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="feba4-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="feba4-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="feba4-258">(25)</span><span class="sxs-lookup"><span data-stu-id="feba4-258">(25)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-259">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="feba4-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="feba4-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="feba4-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="feba4-261">(26)</span><span class="sxs-lookup"><span data-stu-id="feba4-261">(26)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-262">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="feba4-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="feba4-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="feba4-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="feba4-264">(27)</span><span class="sxs-lookup"><span data-stu-id="feba4-264">(27)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-265">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="feba4-265">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="feba4-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="feba4-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="feba4-267">(28)</span><span class="sxs-lookup"><span data-stu-id="feba4-267">(28)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-268">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="feba4-268">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="feba4-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="feba4-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="feba4-270">(29)</span><span class="sxs-lookup"><span data-stu-id="feba4-270">(29)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-271">裝置已停用;裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="feba4-271">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="feba4-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="feba4-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="feba4-273">(30)</span><span class="sxs-lookup"><span data-stu-id="feba4-273">(30)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-274">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="feba4-274">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="feba4-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="feba4-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="feba4-276"> (31) </span><span class="sxs-lookup"><span data-stu-id="feba4-276">(31)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-277">裝置無法正常運作;Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="feba4-277">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="feba4-278">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="feba4-278">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feba4-279">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="feba4-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="feba4-280">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="feba4-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="feba4-281">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="feba4-281">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="feba4-282">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="feba4-282">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="feba4-283">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="feba4-283">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="feba4-284">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="feba4-284">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feba4-285">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="feba4-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="feba4-286">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="feba4-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="feba4-287">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="feba4-287">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="feba4-288">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="feba4-288">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="feba4-289">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="feba4-289">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="feba4-290">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="feba4-290">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="feba4-291">**說明**</span><span class="sxs-lookup"><span data-stu-id="feba4-291">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feba4-292">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="feba4-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="feba4-293">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="feba4-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="feba4-294">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="feba4-294">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="feba4-295">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="feba4-295">Textual description of the object.</span></span>

<span data-ttu-id="feba4-296">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="feba4-296">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="feba4-297">**DesiredSpeed**</span><span class="sxs-lookup"><span data-stu-id="feba4-297">**DesiredSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feba4-298">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="feba4-298">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="feba4-299">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="feba4-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="feba4-300">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「每分鐘的旋轉」 ) </span><span class="sxs-lookup"><span data-stu-id="feba4-300">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="feba4-301">當支援變速風扇時，要求的風扇速度（以每分鐘的旋轉所定義）。</span><span class="sxs-lookup"><span data-stu-id="feba4-301">Requested fan speed, defined in revolutions per minute, when a variable speed fan is supported.</span></span> <span data-ttu-id="feba4-302">目前的速度取決於與使用 [**cim \_ AssociatedSensor**](cim-associatedsensor.md)關聯性之風扇相關聯的感應器 ([**CIM \_ 流速**](cim-tachometer.md)) 。</span><span class="sxs-lookup"><span data-stu-id="feba4-302">The current speed is determined by a sensor ([**CIM\_Tachometer**](cim-tachometer.md)) that is associated with the fan using the [**CIM\_AssociatedSensor**](cim-associatedsensor.md) relationship.</span></span>

<span data-ttu-id="feba4-303">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="feba4-303">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="feba4-304">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="feba4-304">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feba4-305">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="feba4-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="feba4-306">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="feba4-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="feba4-307">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="feba4-307">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="feba4-308">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="feba4-308">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="feba4-309">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="feba4-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="feba4-310">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="feba4-310">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feba4-311">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="feba4-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="feba4-312">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="feba4-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="feba4-313">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="feba4-313">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="feba4-314">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="feba4-314">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="feba4-315">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="feba4-315">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feba4-316">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="feba4-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="feba4-317">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="feba4-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="feba4-318">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="feba4-318">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="feba4-319">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="feba4-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="feba4-320">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="feba4-320">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feba4-321">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="feba4-321">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="feba4-322">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="feba4-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="feba4-323">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="feba4-323">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="feba4-324">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="feba4-324">Date and time the object was installed.</span></span> <span data-ttu-id="feba4-325">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="feba4-325">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="feba4-326">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="feba4-326">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="feba4-327">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="feba4-327">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feba4-328">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="feba4-328">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="feba4-329">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="feba4-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="feba4-330">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="feba4-330">Last error code reported by the logical device.</span></span>

<span data-ttu-id="feba4-331">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="feba4-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="feba4-332">**名稱**</span><span class="sxs-lookup"><span data-stu-id="feba4-332">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feba4-333">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="feba4-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="feba4-334">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="feba4-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="feba4-335">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="feba4-335">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="feba4-336">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="feba4-336">Label by which the object is known.</span></span> <span data-ttu-id="feba4-337">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="feba4-337">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="feba4-338">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="feba4-338">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="feba4-339">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="feba4-339">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feba4-340">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="feba4-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="feba4-341">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="feba4-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="feba4-342">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="feba4-342">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="feba4-343">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="feba4-343">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="feba4-344">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="feba4-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="feba4-345">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="feba4-345">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="feba4-346">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="feba4-346">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feba4-347">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="feba4-347">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="feba4-348">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="feba4-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="feba4-349">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="feba4-349">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="feba4-350">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="feba4-350">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="feba4-351"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="feba4-351"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="feba4-352"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="feba4-352"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-353">此裝置不支援與電源相關的容量。</span><span class="sxs-lookup"><span data-stu-id="feba4-353">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="feba4-354"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="feba4-354"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="feba4-355"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="feba4-355"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-356">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="feba4-356">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="feba4-357"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="feba4-357"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-358">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="feba4-358">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="feba4-359"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="feba4-359"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-360">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="feba4-360">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="feba4-361">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="feba4-361">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="feba4-362">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="feba4-362">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="feba4-363"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="feba4-363"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-364">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="feba4-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="feba4-365"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="feba4-365"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="feba4-366">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="feba4-366">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="feba4-367">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="feba4-367">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feba4-368">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="feba4-368">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="feba4-369">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="feba4-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="feba4-370">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="feba4-370">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="feba4-371">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="feba4-371">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="feba4-372">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="feba4-372">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="feba4-373">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="feba4-373">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="feba4-374">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="feba4-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="feba4-375">**狀態**</span><span class="sxs-lookup"><span data-stu-id="feba4-375">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feba4-376">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="feba4-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="feba4-377">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="feba4-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="feba4-378">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="feba4-378">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="feba4-379">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="feba4-379">Current status of the object.</span></span> <span data-ttu-id="feba4-380">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="feba4-380">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="feba4-381">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="feba4-381">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="feba4-382">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="feba4-382">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="feba4-383">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="feba4-383">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="feba4-384">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="feba4-384">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="feba4-385">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="feba4-385">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="feba4-386">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="feba4-386">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="feba4-387">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="feba4-387">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="feba4-388">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="feba4-388">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="feba4-389">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="feba4-389">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="feba4-390">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="feba4-390">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="feba4-391">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="feba4-391">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="feba4-392">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="feba4-392">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="feba4-393">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="feba4-393">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="feba4-394">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="feba4-394">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feba4-395">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="feba4-395">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="feba4-396">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="feba4-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="feba4-397">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="feba4-397">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="feba4-398">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="feba4-398">State of the logical device.</span></span> <span data-ttu-id="feba4-399">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="feba4-399">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="feba4-400">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="feba4-400">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="feba4-401">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="feba4-401">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="feba4-402">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="feba4-402">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="feba4-403">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="feba4-403">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="feba4-404">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="feba4-404">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="feba4-405">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="feba4-405">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="feba4-406">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="feba4-406">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feba4-407">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="feba4-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="feba4-408">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="feba4-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="feba4-409">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="feba4-409">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="feba4-410">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="feba4-410">Scoping system's creation class name.</span></span>

<span data-ttu-id="feba4-411">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="feba4-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="feba4-412">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="feba4-412">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feba4-413">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="feba4-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="feba4-414">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="feba4-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="feba4-415">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="feba4-415">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="feba4-416">設定系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="feba4-416">Scoping system's name.</span></span>

<span data-ttu-id="feba4-417">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="feba4-417">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="feba4-418">**VariableSpeed**</span><span class="sxs-lookup"><span data-stu-id="feba4-418">**VariableSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feba4-419">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="feba4-419">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="feba4-420">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="feba4-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="feba4-421">若 **為 TRUE**，則風扇支援可變速度。</span><span class="sxs-lookup"><span data-stu-id="feba4-421">If **TRUE**, the fan supports variable speeds.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="feba4-422">備註</span><span class="sxs-lookup"><span data-stu-id="feba4-422">Remarks</span></span>

<span data-ttu-id="feba4-423">**Cim \_ 風扇** 類別衍生自 [**cim \_ CoolingDevice**](cim-coolingdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="feba4-423">The **CIM\_Fan** class is derived from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

<span data-ttu-id="feba4-424">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="feba4-424">WMI does not implement this class.</span></span> <span data-ttu-id="feba4-425">針對衍生自 **CIM \_ 風扇** 的類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="feba4-425">For classes derived from **CIM\_Fan**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="feba4-426">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="feba4-426">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="feba4-427">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="feba4-427">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="feba4-428">規格需求</span><span class="sxs-lookup"><span data-stu-id="feba4-428">Requirements</span></span>



| <span data-ttu-id="feba4-429">需求</span><span class="sxs-lookup"><span data-stu-id="feba4-429">Requirement</span></span> | <span data-ttu-id="feba4-430">值</span><span class="sxs-lookup"><span data-stu-id="feba4-430">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="feba4-431">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="feba4-431">Minimum supported client</span></span><br/> | <span data-ttu-id="feba4-432">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feba4-432">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="feba4-433">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="feba4-433">Minimum supported server</span></span><br/> | <span data-ttu-id="feba4-434">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="feba4-434">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="feba4-435">命名空間</span><span class="sxs-lookup"><span data-stu-id="feba4-435">Namespace</span></span><br/>                | <span data-ttu-id="feba4-436">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="feba4-436">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="feba4-437">MOF</span><span class="sxs-lookup"><span data-stu-id="feba4-437">MOF</span></span><br/>                      | <dl> <span data-ttu-id="feba4-438"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="feba4-438"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="feba4-439">DLL</span><span class="sxs-lookup"><span data-stu-id="feba4-439">DLL</span></span><br/>                      | <dl> <span data-ttu-id="feba4-440"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="feba4-440"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="feba4-441">另請參閱</span><span class="sxs-lookup"><span data-stu-id="feba4-441">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feba4-442">**CIM \_ CoolingDevice**</span><span class="sxs-lookup"><span data-stu-id="feba4-442">**CIM\_CoolingDevice**</span></span>](cim-coolingdevice.md)
</dt> </dl>

 

