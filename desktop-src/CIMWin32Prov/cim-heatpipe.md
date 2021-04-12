---
description: CIM \_ HeatPipe 類別代表熱度管道冷卻裝置的功能和管理。
ms.assetid: 55cbf645-12d8-4f17-a894-43195d42de0e
ms.tgt_platform: multiple
title: CIM_HeatPipe 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HeatPipe
- CIM_HeatPipe.ActiveCooling
- CIM_HeatPipe.Availability
- CIM_HeatPipe.Caption
- CIM_HeatPipe.ConfigManagerErrorCode
- CIM_HeatPipe.ConfigManagerUserConfig
- CIM_HeatPipe.CreationClassName
- CIM_HeatPipe.Description
- CIM_HeatPipe.DeviceID
- CIM_HeatPipe.ErrorCleared
- CIM_HeatPipe.ErrorDescription
- CIM_HeatPipe.InstallDate
- CIM_HeatPipe.LastErrorCode
- CIM_HeatPipe.Name
- CIM_HeatPipe.PNPDeviceID
- CIM_HeatPipe.PowerManagementCapabilities
- CIM_HeatPipe.PowerManagementSupported
- CIM_HeatPipe.Status
- CIM_HeatPipe.StatusInfo
- CIM_HeatPipe.SystemCreationClassName
- CIM_HeatPipe.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9502509e5a48f4d2f407fddbb6b57766b5f7bffa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317868"
---
# <a name="cim_heatpipe-class"></a><span data-ttu-id="d48af-103">CIM \_ HeatPipe 類別</span><span class="sxs-lookup"><span data-stu-id="d48af-103">CIM\_HeatPipe class</span></span>

<span data-ttu-id="d48af-104">**CIM \_ HeatPipe** 類別代表熱度管道冷卻裝置的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="d48af-104">The **CIM\_HeatPipe** class represents the capabilities and management of a heat pipe cooling device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d48af-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="d48af-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d48af-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="d48af-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d48af-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d48af-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d48af-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="d48af-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d48af-109">語法</span><span class="sxs-lookup"><span data-stu-id="d48af-109">Syntax</span></span>

``` syntax
[UUID("{FE5D55E0-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_HeatPipe : CIM_CoolingDevice
{
  boolean  ActiveCooling;
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
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="d48af-110">成員</span><span class="sxs-lookup"><span data-stu-id="d48af-110">Members</span></span>

<span data-ttu-id="d48af-111">**CIM \_ HeatPipe** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d48af-111">The **CIM\_HeatPipe** class has these types of members:</span></span>

-   [<span data-ttu-id="d48af-112">方法</span><span class="sxs-lookup"><span data-stu-id="d48af-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="d48af-113">屬性</span><span class="sxs-lookup"><span data-stu-id="d48af-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d48af-114">方法</span><span class="sxs-lookup"><span data-stu-id="d48af-114">Methods</span></span>

<span data-ttu-id="d48af-115">**CIM \_ HeatPipe** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d48af-115">The **CIM\_HeatPipe** class has these methods.</span></span>



| <span data-ttu-id="d48af-116">方法</span><span class="sxs-lookup"><span data-stu-id="d48af-116">Method</span></span>                                                              | <span data-ttu-id="d48af-117">描述</span><span class="sxs-lookup"><span data-stu-id="d48af-117">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d48af-118">**重設**</span><span class="sxs-lookup"><span data-stu-id="d48af-118">**Reset**</span></span>](reset-method-in-class-cim-heatpipe.md)                 | <span data-ttu-id="d48af-119">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="d48af-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="d48af-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="d48af-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="d48af-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d48af-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-heatpipe.md) | <span data-ttu-id="d48af-122">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="d48af-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="d48af-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="d48af-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d48af-124">屬性</span><span class="sxs-lookup"><span data-stu-id="d48af-124">Properties</span></span>

<span data-ttu-id="d48af-125">**CIM \_ HeatPipe** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d48af-125">The **CIM\_HeatPipe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d48af-126">**ActiveCooling**</span><span class="sxs-lookup"><span data-stu-id="d48af-126">**ActiveCooling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48af-127">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d48af-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d48af-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d48af-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d48af-129">若 **為 TRUE**，則冷卻裝置會提供作用中的 (，而非被動) 冷卻。</span><span class="sxs-lookup"><span data-stu-id="d48af-129">If **TRUE**, the cooling device provides active (as opposed to passive) cooling.</span></span>

<span data-ttu-id="d48af-130">這個屬性繼承自 [**CIM \_ CoolingDevice**](cim-coolingdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d48af-130">This property is inherited from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d48af-131">**可用性**</span><span class="sxs-lookup"><span data-stu-id="d48af-131">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48af-132">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d48af-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d48af-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d48af-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d48af-134">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="d48af-134">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="d48af-135">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="d48af-135">Availability and status of the device.</span></span>

<span data-ttu-id="d48af-136">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d48af-136">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d48af-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="d48af-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d48af-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="d48af-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="d48af-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="d48af-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="d48af-140"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="d48af-140"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="d48af-141"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="d48af-141"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d48af-142"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="d48af-142"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="d48af-143"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="d48af-143"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="d48af-144"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="d48af-144"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="d48af-145"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="d48af-145"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d48af-146"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="d48af-146"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="d48af-147"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="d48af-147"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="d48af-148"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="d48af-148"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="d48af-149"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="d48af-149"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-150">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="d48af-150">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="d48af-151"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="d48af-151"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-152">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="d48af-152">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="d48af-153"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="d48af-153"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-154">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="d48af-154">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="d48af-155"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="d48af-155"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="d48af-156"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="d48af-156"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-157">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="d48af-157">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="d48af-158"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="d48af-158"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-159">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="d48af-159">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="d48af-160"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="d48af-160"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-161">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="d48af-161">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="d48af-162"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="d48af-162"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-163">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="d48af-163">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="d48af-164"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="d48af-164"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-165">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="d48af-165">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d48af-166">**標題**</span><span class="sxs-lookup"><span data-stu-id="d48af-166">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48af-167">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d48af-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d48af-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d48af-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d48af-169">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="d48af-169">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d48af-170">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="d48af-170">Short textual description of the object.</span></span>

<span data-ttu-id="d48af-171">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d48af-171">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d48af-172">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d48af-172">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48af-173">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d48af-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d48af-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d48af-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d48af-175">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="d48af-175">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d48af-176">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d48af-176">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="d48af-177">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d48af-177">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="d48af-178"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="d48af-178"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="d48af-179"> (0)</span><span class="sxs-lookup"><span data-stu-id="d48af-179">(0)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-180">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="d48af-180">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="d48af-181"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="d48af-181"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="d48af-182">(1)</span><span class="sxs-lookup"><span data-stu-id="d48af-182">(1)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-183">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="d48af-183">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d48af-184"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="d48af-184"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="d48af-185">(2)</span><span class="sxs-lookup"><span data-stu-id="d48af-185">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="d48af-186"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="d48af-186"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="d48af-187">(3)</span><span class="sxs-lookup"><span data-stu-id="d48af-187">(3)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-188">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="d48af-188">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d48af-189"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="d48af-189"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="d48af-190">(4)</span><span class="sxs-lookup"><span data-stu-id="d48af-190">(4)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-191">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="d48af-191">Device is not working properly.</span></span> <span data-ttu-id="d48af-192">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="d48af-192">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="d48af-193"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="d48af-193"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="d48af-194">(5)</span><span class="sxs-lookup"><span data-stu-id="d48af-194">(5)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-195">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="d48af-195">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="d48af-196"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="d48af-196"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="d48af-197">(6)</span><span class="sxs-lookup"><span data-stu-id="d48af-197">(6)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-198">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="d48af-198">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="d48af-199"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="d48af-199"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="d48af-200">(7)</span><span class="sxs-lookup"><span data-stu-id="d48af-200">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="d48af-201"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="d48af-201"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="d48af-202">(8)</span><span class="sxs-lookup"><span data-stu-id="d48af-202">(8)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-203">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="d48af-203">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="d48af-204"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="d48af-204"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="d48af-205">(9)</span><span class="sxs-lookup"><span data-stu-id="d48af-205">(9)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-206">裝置無法正常運作;控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="d48af-206">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="d48af-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="d48af-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="d48af-208">(10)</span><span class="sxs-lookup"><span data-stu-id="d48af-208">(10)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-209">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="d48af-209">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="d48af-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="d48af-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="d48af-211">(11)</span><span class="sxs-lookup"><span data-stu-id="d48af-211">(11)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-212">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="d48af-212">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="d48af-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="d48af-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="d48af-214"> (12) </span><span class="sxs-lookup"><span data-stu-id="d48af-214">(12)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-215">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="d48af-215">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="d48af-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="d48af-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="d48af-217">(13)</span><span class="sxs-lookup"><span data-stu-id="d48af-217">(13)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-218">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="d48af-218">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="d48af-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="d48af-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="d48af-220">(14)</span><span class="sxs-lookup"><span data-stu-id="d48af-220">(14)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-221">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="d48af-221">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="d48af-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="d48af-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="d48af-223">(15)</span><span class="sxs-lookup"><span data-stu-id="d48af-223">(15)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-224">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="d48af-224">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="d48af-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="d48af-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="d48af-226">(16)</span><span class="sxs-lookup"><span data-stu-id="d48af-226">(16)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-227">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="d48af-227">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="d48af-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="d48af-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="d48af-229">(17)</span><span class="sxs-lookup"><span data-stu-id="d48af-229">(17)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-230">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="d48af-230">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d48af-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="d48af-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="d48af-232">(18)</span><span class="sxs-lookup"><span data-stu-id="d48af-232">(18)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-233">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="d48af-233">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="d48af-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="d48af-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="d48af-235">(19)</span><span class="sxs-lookup"><span data-stu-id="d48af-235">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d48af-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="d48af-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="d48af-237">(20)</span><span class="sxs-lookup"><span data-stu-id="d48af-237">(20)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-238">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="d48af-238">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="d48af-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="d48af-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="d48af-240">(21)</span><span class="sxs-lookup"><span data-stu-id="d48af-240">(21)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-241">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="d48af-241">System failure.</span></span> <span data-ttu-id="d48af-242">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="d48af-242">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="d48af-243">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="d48af-243">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="d48af-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="d48af-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="d48af-245">(22)</span><span class="sxs-lookup"><span data-stu-id="d48af-245">(22)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-246">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="d48af-246">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="d48af-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="d48af-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="d48af-248">(23)</span><span class="sxs-lookup"><span data-stu-id="d48af-248">(23)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-249">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="d48af-249">System failure.</span></span> <span data-ttu-id="d48af-250">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="d48af-250">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="d48af-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="d48af-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="d48af-252">(24)</span><span class="sxs-lookup"><span data-stu-id="d48af-252">(24)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-253">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="d48af-253">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d48af-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="d48af-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d48af-255">(25)</span><span class="sxs-lookup"><span data-stu-id="d48af-255">(25)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-256">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="d48af-256">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d48af-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="d48af-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d48af-258">(26)</span><span class="sxs-lookup"><span data-stu-id="d48af-258">(26)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-259">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="d48af-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="d48af-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="d48af-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="d48af-261">(27)</span><span class="sxs-lookup"><span data-stu-id="d48af-261">(27)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-262">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="d48af-262">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="d48af-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="d48af-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="d48af-264">(28)</span><span class="sxs-lookup"><span data-stu-id="d48af-264">(28)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-265">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="d48af-265">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="d48af-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="d48af-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="d48af-267">(29)</span><span class="sxs-lookup"><span data-stu-id="d48af-267">(29)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-268">裝置已停用;裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="d48af-268">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="d48af-269"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="d48af-269"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="d48af-270">(30)</span><span class="sxs-lookup"><span data-stu-id="d48af-270">(30)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-271">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="d48af-271">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d48af-272"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="d48af-272"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="d48af-273"> (31) </span><span class="sxs-lookup"><span data-stu-id="d48af-273">(31)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-274">裝置無法正常運作;Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="d48af-274">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d48af-275">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="d48af-275">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48af-276">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d48af-276">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d48af-277">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d48af-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d48af-278">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="d48af-278">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d48af-279">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="d48af-279">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="d48af-280">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d48af-280">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d48af-281">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d48af-281">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48af-282">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d48af-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d48af-283">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d48af-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d48af-284">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d48af-284">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d48af-285">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="d48af-285">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="d48af-286">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="d48af-286">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="d48af-287">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d48af-287">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d48af-288">**說明**</span><span class="sxs-lookup"><span data-stu-id="d48af-288">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48af-289">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d48af-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d48af-290">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d48af-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d48af-291">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="d48af-291">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d48af-292">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="d48af-292">Textual description of the object.</span></span>

<span data-ttu-id="d48af-293">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d48af-293">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d48af-294">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="d48af-294">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48af-295">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d48af-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d48af-296">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d48af-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d48af-297">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d48af-297">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d48af-298">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="d48af-298">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="d48af-299">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d48af-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d48af-300">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="d48af-300">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48af-301">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d48af-301">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d48af-302">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d48af-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d48af-303">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="d48af-303">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="d48af-304">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d48af-304">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d48af-305">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d48af-305">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48af-306">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d48af-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d48af-307">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d48af-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d48af-308">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的詳細資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="d48af-308">Free-form string that supplies more information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="d48af-309">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d48af-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d48af-310">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d48af-310">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48af-311">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="d48af-311">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d48af-312">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d48af-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d48af-313">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="d48af-313">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d48af-314">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="d48af-314">Date and time the object was installed.</span></span> <span data-ttu-id="d48af-315">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="d48af-315">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="d48af-316">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d48af-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d48af-317">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d48af-317">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48af-318">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d48af-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d48af-319">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d48af-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d48af-320">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d48af-320">Last error code reported by the logical device.</span></span>

<span data-ttu-id="d48af-321">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d48af-321">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d48af-322">**名稱**</span><span class="sxs-lookup"><span data-stu-id="d48af-322">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48af-323">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d48af-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d48af-324">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d48af-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d48af-325">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="d48af-325">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d48af-326">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="d48af-326">Label by which the object is known.</span></span> <span data-ttu-id="d48af-327">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="d48af-327">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="d48af-328">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d48af-328">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d48af-329">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="d48af-329">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48af-330">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d48af-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d48af-331">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d48af-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d48af-332">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="d48af-332">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d48af-333">邏輯裝置的 Win32 隨插即用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="d48af-333">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="d48af-334">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d48af-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="d48af-335">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="d48af-335">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="d48af-336">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d48af-336">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48af-337">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="d48af-337">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d48af-338">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d48af-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d48af-339">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="d48af-339">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="d48af-340">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="d48af-340">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d48af-341"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="d48af-341"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="d48af-342"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="d48af-342"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-343">此裝置不支援與電源相關的容量。</span><span class="sxs-lookup"><span data-stu-id="d48af-343">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d48af-344"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="d48af-344"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d48af-345"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="d48af-345"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-346">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="d48af-346">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="d48af-347"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="d48af-347"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-348">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="d48af-348">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="d48af-349"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="d48af-349"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-350">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="d48af-350">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="d48af-351">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="d48af-351">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="d48af-352">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="d48af-352">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="d48af-353"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="d48af-353"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-354">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="d48af-354">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="d48af-355"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="d48af-355"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d48af-356">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="d48af-356">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d48af-357">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="d48af-357">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48af-358">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d48af-358">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d48af-359">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d48af-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d48af-360">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="d48af-360">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="d48af-361">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="d48af-361">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="d48af-362">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="d48af-362">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="d48af-363">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="d48af-363">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="d48af-364">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d48af-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d48af-365">**狀態**</span><span class="sxs-lookup"><span data-stu-id="d48af-365">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48af-366">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d48af-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d48af-367">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d48af-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d48af-368">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="d48af-368">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d48af-369">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="d48af-369">Current status of the object.</span></span> <span data-ttu-id="d48af-370">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d48af-370">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d48af-371">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="d48af-371">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d48af-372">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="d48af-372">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d48af-373">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="d48af-373">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d48af-374">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="d48af-374">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d48af-375">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="d48af-375">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d48af-376">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="d48af-376">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d48af-377">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="d48af-377">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d48af-378">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="d48af-378">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d48af-379">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="d48af-379">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d48af-380">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="d48af-380">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d48af-381">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="d48af-381">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d48af-382">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="d48af-382">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d48af-383">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="d48af-383">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d48af-384">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d48af-384">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48af-385">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d48af-385">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d48af-386">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d48af-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d48af-387">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="d48af-387">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="d48af-388">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="d48af-388">State of the logical device.</span></span> <span data-ttu-id="d48af-389">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="d48af-389">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="d48af-390">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d48af-390">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d48af-391">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="d48af-391">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d48af-392">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="d48af-392">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d48af-393">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="d48af-393">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d48af-394">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="d48af-394">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d48af-395">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="d48af-395">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d48af-396">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d48af-396">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48af-397">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d48af-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d48af-398">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d48af-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d48af-399">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d48af-399">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d48af-400">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="d48af-400">Scoping system's creation class name.</span></span>

<span data-ttu-id="d48af-401">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d48af-401">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d48af-402">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d48af-402">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48af-403">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d48af-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d48af-404">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d48af-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d48af-405">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d48af-405">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d48af-406">設定系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="d48af-406">Scoping system's name.</span></span>

<span data-ttu-id="d48af-407">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d48af-407">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d48af-408">備註</span><span class="sxs-lookup"><span data-stu-id="d48af-408">Remarks</span></span>

<span data-ttu-id="d48af-409">**Cim \_ HeatPipe** 類別衍生自 [**cim \_ CoolingDevice**](cim-coolingdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d48af-409">The **CIM\_HeatPipe** class is derived from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

<span data-ttu-id="d48af-410">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="d48af-410">WMI does not implement this class.</span></span> <span data-ttu-id="d48af-411">針對衍生自 **CIM \_ HeatPipe** 的類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="d48af-411">For classes derived from **CIM\_HeatPipe**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="d48af-412">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="d48af-412">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d48af-413">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="d48af-413">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d48af-414">規格需求</span><span class="sxs-lookup"><span data-stu-id="d48af-414">Requirements</span></span>



| <span data-ttu-id="d48af-415">需求</span><span class="sxs-lookup"><span data-stu-id="d48af-415">Requirement</span></span> | <span data-ttu-id="d48af-416">值</span><span class="sxs-lookup"><span data-stu-id="d48af-416">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d48af-417">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d48af-417">Minimum supported client</span></span><br/> | <span data-ttu-id="d48af-418">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d48af-418">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d48af-419">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d48af-419">Minimum supported server</span></span><br/> | <span data-ttu-id="d48af-420">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d48af-420">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d48af-421">命名空間</span><span class="sxs-lookup"><span data-stu-id="d48af-421">Namespace</span></span><br/>                | <span data-ttu-id="d48af-422">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d48af-422">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d48af-423">MOF</span><span class="sxs-lookup"><span data-stu-id="d48af-423">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d48af-424"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="d48af-424"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d48af-425">DLL</span><span class="sxs-lookup"><span data-stu-id="d48af-425">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d48af-426"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d48af-426"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d48af-427">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d48af-427">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d48af-428">**CIM \_ CoolingDevice**</span><span class="sxs-lookup"><span data-stu-id="d48af-428">**CIM\_CoolingDevice**</span></span>](cim-coolingdevice.md)
</dt> </dl>

 

