---
description: CIM \_ CurrentSensor 類別存在，可回溯相容于舊版 cim 架構定義。
ms.assetid: d1835b09-4286-4586-92ec-f5f77791aea6
ms.tgt_platform: multiple
title: CIM_CurrentSensor 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CurrentSensor
- CIM_CurrentSensor.Accuracy
- CIM_CurrentSensor.Availability
- CIM_CurrentSensor.Caption
- CIM_CurrentSensor.ConfigManagerErrorCode
- CIM_CurrentSensor.ConfigManagerUserConfig
- CIM_CurrentSensor.CreationClassName
- CIM_CurrentSensor.CurrentReading
- CIM_CurrentSensor.Description
- CIM_CurrentSensor.DeviceID
- CIM_CurrentSensor.ErrorCleared
- CIM_CurrentSensor.ErrorDescription
- CIM_CurrentSensor.InstallDate
- CIM_CurrentSensor.IsLinear
- CIM_CurrentSensor.LastErrorCode
- CIM_CurrentSensor.LowerThresholdCritical
- CIM_CurrentSensor.LowerThresholdFatal
- CIM_CurrentSensor.LowerThresholdNonCritical
- CIM_CurrentSensor.MaxReadable
- CIM_CurrentSensor.MinReadable
- CIM_CurrentSensor.Name
- CIM_CurrentSensor.NominalReading
- CIM_CurrentSensor.NormalMax
- CIM_CurrentSensor.NormalMin
- CIM_CurrentSensor.PNPDeviceID
- CIM_CurrentSensor.PowerManagementCapabilities
- CIM_CurrentSensor.PowerManagementSupported
- CIM_CurrentSensor.Resolution
- CIM_CurrentSensor.Status
- CIM_CurrentSensor.StatusInfo
- CIM_CurrentSensor.SystemCreationClassName
- CIM_CurrentSensor.SystemName
- CIM_CurrentSensor.Tolerance
- CIM_CurrentSensor.UpperThresholdCritical
- CIM_CurrentSensor.UpperThresholdFatal
- CIM_CurrentSensor.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1fe2a34e2e598d5c9655abbf84324dbf9982e416
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110881"
---
# <a name="cim_currentsensor-class"></a><span data-ttu-id="528c2-103">CIM \_ CurrentSensor 類別</span><span class="sxs-lookup"><span data-stu-id="528c2-103">CIM\_CurrentSensor class</span></span>

<span data-ttu-id="528c2-104">**Cim \_ CurrentSensor** 類別存在，可回溯相容于舊版 cim 架構定義。</span><span class="sxs-lookup"><span data-stu-id="528c2-104">The **CIM\_CurrentSensor** class exists for backward compatibility to earlier CIM schema definitions.</span></span>

<span data-ttu-id="528c2-105">2.2 版中 [**cim \_ 感應器**](cim-sensor.md) 和 [**cim \_ NumericSensor**](cim-numericsensor.md) 的新增專案不再需要。</span><span class="sxs-lookup"><span data-stu-id="528c2-105">Additions to [**CIM\_Sensor**](cim-sensor.md) and [**CIM\_NumericSensor**](cim-numericsensor.md) in version 2.2 make it no longer necessary.</span></span> <span data-ttu-id="528c2-106">您可以藉由將 **SensorType** 屬性（繼承自 **cim \_ 感應器**）設定為 4 ( 「目前」 ) 來定義 **CIM \_ CurrentSensor** 類別。</span><span class="sxs-lookup"><span data-stu-id="528c2-106">A **CIM\_CurrentSensor** class can be defined by setting the **SensorType** property, inherited from **CIM\_Sensor**, to 4 ("Current").</span></span> <span data-ttu-id="528c2-107">此類別的其他屬性會硬式編碼為常數值，這些值會對應至感應器階層中的定義。</span><span class="sxs-lookup"><span data-stu-id="528c2-107">Other properties of this class are hard-coded to constant values, which correspond to definitions in the sensor hierarchy.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="528c2-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="528c2-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="528c2-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="528c2-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="528c2-110">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="528c2-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="528c2-111">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="528c2-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="528c2-112">語法</span><span class="sxs-lookup"><span data-stu-id="528c2-112">Syntax</span></span>

``` syntax
[UUID("{DCA1D084-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_CurrentSensor : CIM_NumericSensor
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

## <a name="members"></a><span data-ttu-id="528c2-113">成員</span><span class="sxs-lookup"><span data-stu-id="528c2-113">Members</span></span>

<span data-ttu-id="528c2-114">**CIM \_ CurrentSensor** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="528c2-114">The **CIM\_CurrentSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="528c2-115">方法</span><span class="sxs-lookup"><span data-stu-id="528c2-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="528c2-116">屬性</span><span class="sxs-lookup"><span data-stu-id="528c2-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="528c2-117">方法</span><span class="sxs-lookup"><span data-stu-id="528c2-117">Methods</span></span>

<span data-ttu-id="528c2-118">**CIM \_ CurrentSensor** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="528c2-118">The **CIM\_CurrentSensor** class has these methods.</span></span>



| <span data-ttu-id="528c2-119">方法</span><span class="sxs-lookup"><span data-stu-id="528c2-119">Method</span></span>                                                                   | <span data-ttu-id="528c2-120">描述</span><span class="sxs-lookup"><span data-stu-id="528c2-120">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="528c2-121">**重設**</span><span class="sxs-lookup"><span data-stu-id="528c2-121">**Reset**</span></span>](reset-method-in-class-cim-currentsensor.md)                 | <span data-ttu-id="528c2-122">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="528c2-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="528c2-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="528c2-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="528c2-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="528c2-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-currentsensor.md) | <span data-ttu-id="528c2-125">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="528c2-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="528c2-126">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="528c2-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="528c2-127">屬性</span><span class="sxs-lookup"><span data-stu-id="528c2-127">Properties</span></span>

<span data-ttu-id="528c2-128">**CIM \_ CurrentSensor** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="528c2-128">The **CIM\_CurrentSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="528c2-129">**精確度**</span><span class="sxs-lookup"><span data-stu-id="528c2-129">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-130">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="528c2-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-132">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「精確度」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 電子目前的探查 \| 001.19」 ) </span><span class="sxs-lookup"><span data-stu-id="528c2-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Accuracy"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="528c2-133">測量的屬性之感應器的精確度。</span><span class="sxs-lookup"><span data-stu-id="528c2-133">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="528c2-134">其值會記錄為加號或減號百分之一%。</span><span class="sxs-lookup"><span data-stu-id="528c2-134">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="528c2-135">這個屬性（property）和 **解析** 和 **容錯** 屬性（property）可用來計算測量實體屬性的實際值。</span><span class="sxs-lookup"><span data-stu-id="528c2-135">This property, and the **Resolution** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="528c2-136">精確度可能會根據裝置的動態範圍是否為線性而有所不同。</span><span class="sxs-lookup"><span data-stu-id="528c2-136">Accuracy can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="528c2-137">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-137">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-138">**可用性**</span><span class="sxs-lookup"><span data-stu-id="528c2-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-139">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="528c2-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-141">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="528c2-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="528c2-142">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="528c2-142">Availability and status of the device.</span></span>

<span data-ttu-id="528c2-143">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="528c2-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="528c2-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="528c2-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="528c2-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="528c2-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="528c2-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="528c2-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="528c2-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="528c2-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="528c2-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="528c2-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="528c2-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="528c2-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="528c2-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="528c2-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="528c2-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="528c2-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="528c2-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="528c2-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="528c2-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="528c2-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="528c2-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="528c2-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="528c2-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="528c2-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="528c2-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-157">省電不明。</span><span class="sxs-lookup"><span data-stu-id="528c2-157">Power save   unknown.</span></span>

<span data-ttu-id="528c2-158">裝置處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="528c2-158">Device is in a power-save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="528c2-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="528c2-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-160">省電低電源模式。</span><span class="sxs-lookup"><span data-stu-id="528c2-160">Power save   low-power mode.</span></span>

<span data-ttu-id="528c2-161">裝置處於省電模式且仍正常運作，但可能會顯示效能下降。</span><span class="sxs-lookup"><span data-stu-id="528c2-161">Device is in a power-save mode and still functioning, but may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="528c2-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="528c2-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-163">省電待命。</span><span class="sxs-lookup"><span data-stu-id="528c2-163">Power save   standby.</span></span>

<span data-ttu-id="528c2-164">裝置無法正常運作，但可以快速獲得完整的電源。</span><span class="sxs-lookup"><span data-stu-id="528c2-164">Device is not functioning, but it could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="528c2-165"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="528c2-165"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="528c2-166"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="528c2-166"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-167">省電警告。</span><span class="sxs-lookup"><span data-stu-id="528c2-167">Power save   warning.</span></span>

<span data-ttu-id="528c2-168">裝置處於警告狀態和省電模式。</span><span class="sxs-lookup"><span data-stu-id="528c2-168">Device is in a warning state and a power-save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="528c2-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="528c2-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="528c2-170"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="528c2-170"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="528c2-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="528c2-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="528c2-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="528c2-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-173">目前的感應器無法使用。</span><span class="sxs-lookup"><span data-stu-id="528c2-173">Current sensor is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="528c2-174">**標題**</span><span class="sxs-lookup"><span data-stu-id="528c2-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-175">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="528c2-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-177">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="528c2-177">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="528c2-178">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="528c2-178">Short textual description of the object.</span></span>

<span data-ttu-id="528c2-179">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-180">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="528c2-180">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-181">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="528c2-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-183">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="528c2-183">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="528c2-184">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="528c2-184">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="528c2-185">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-185">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="528c2-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="528c2-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="528c2-187"> (0)</span><span class="sxs-lookup"><span data-stu-id="528c2-187">(0)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-188">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="528c2-188">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="528c2-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="528c2-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="528c2-190">(1)</span><span class="sxs-lookup"><span data-stu-id="528c2-190">(1)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-191">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="528c2-191">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="528c2-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="528c2-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="528c2-193">(2)</span><span class="sxs-lookup"><span data-stu-id="528c2-193">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="528c2-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="528c2-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="528c2-195">(3)</span><span class="sxs-lookup"><span data-stu-id="528c2-195">(3)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-196">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="528c2-196">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="528c2-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="528c2-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="528c2-198">(4)</span><span class="sxs-lookup"><span data-stu-id="528c2-198">(4)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-199">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="528c2-199">Device is not working properly.</span></span> <span data-ttu-id="528c2-200">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="528c2-200">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="528c2-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="528c2-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="528c2-202">(5)</span><span class="sxs-lookup"><span data-stu-id="528c2-202">(5)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-203">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="528c2-203">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="528c2-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="528c2-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="528c2-205">(6)</span><span class="sxs-lookup"><span data-stu-id="528c2-205">(6)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-206">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="528c2-206">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="528c2-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="528c2-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="528c2-208">(7)</span><span class="sxs-lookup"><span data-stu-id="528c2-208">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="528c2-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="528c2-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="528c2-210">(8)</span><span class="sxs-lookup"><span data-stu-id="528c2-210">(8)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-211">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="528c2-211">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="528c2-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="528c2-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="528c2-213">(9)</span><span class="sxs-lookup"><span data-stu-id="528c2-213">(9)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-214">裝置無法正常運作;控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="528c2-214">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="528c2-215"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="528c2-215"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="528c2-216">(10)</span><span class="sxs-lookup"><span data-stu-id="528c2-216">(10)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-217">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="528c2-217">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="528c2-218"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="528c2-218"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="528c2-219">(11)</span><span class="sxs-lookup"><span data-stu-id="528c2-219">(11)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-220">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="528c2-220">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="528c2-221"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="528c2-221"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="528c2-222"> (12) </span><span class="sxs-lookup"><span data-stu-id="528c2-222">(12)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-223">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="528c2-223">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="528c2-224"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="528c2-224"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="528c2-225">(13)</span><span class="sxs-lookup"><span data-stu-id="528c2-225">(13)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-226">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="528c2-226">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="528c2-227"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="528c2-227"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="528c2-228">(14)</span><span class="sxs-lookup"><span data-stu-id="528c2-228">(14)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-229">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="528c2-229">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="528c2-230"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="528c2-230"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="528c2-231">(15)</span><span class="sxs-lookup"><span data-stu-id="528c2-231">(15)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-232">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="528c2-232">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="528c2-233"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="528c2-233"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="528c2-234">(16)</span><span class="sxs-lookup"><span data-stu-id="528c2-234">(16)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-235">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="528c2-235">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="528c2-236"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="528c2-236"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="528c2-237">(17)</span><span class="sxs-lookup"><span data-stu-id="528c2-237">(17)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-238">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="528c2-238">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="528c2-239"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="528c2-239"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="528c2-240">(18)</span><span class="sxs-lookup"><span data-stu-id="528c2-240">(18)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-241">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="528c2-241">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="528c2-242"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="528c2-242"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="528c2-243">(19)</span><span class="sxs-lookup"><span data-stu-id="528c2-243">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="528c2-244"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="528c2-244"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="528c2-245">(20)</span><span class="sxs-lookup"><span data-stu-id="528c2-245">(20)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-246">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="528c2-246">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="528c2-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="528c2-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="528c2-248">(21)</span><span class="sxs-lookup"><span data-stu-id="528c2-248">(21)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-249">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="528c2-249">System failure.</span></span> <span data-ttu-id="528c2-250">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="528c2-250">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="528c2-251">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="528c2-251">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="528c2-252"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="528c2-252"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="528c2-253">(22)</span><span class="sxs-lookup"><span data-stu-id="528c2-253">(22)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-254">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="528c2-254">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="528c2-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="528c2-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="528c2-256">(23)</span><span class="sxs-lookup"><span data-stu-id="528c2-256">(23)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-257">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="528c2-257">System failure.</span></span> <span data-ttu-id="528c2-258">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="528c2-258">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="528c2-259"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="528c2-259"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="528c2-260">(24)</span><span class="sxs-lookup"><span data-stu-id="528c2-260">(24)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-261">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="528c2-261">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="528c2-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="528c2-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="528c2-263">(25)</span><span class="sxs-lookup"><span data-stu-id="528c2-263">(25)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-264">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="528c2-264">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="528c2-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="528c2-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="528c2-266">(26)</span><span class="sxs-lookup"><span data-stu-id="528c2-266">(26)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-267">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="528c2-267">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="528c2-268"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="528c2-268"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="528c2-269">(27)</span><span class="sxs-lookup"><span data-stu-id="528c2-269">(27)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-270">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="528c2-270">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="528c2-271"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="528c2-271"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="528c2-272">(28)</span><span class="sxs-lookup"><span data-stu-id="528c2-272">(28)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-273">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="528c2-273">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="528c2-274"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="528c2-274"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="528c2-275">(29)</span><span class="sxs-lookup"><span data-stu-id="528c2-275">(29)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-276">裝置已停用;裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="528c2-276">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="528c2-277"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="528c2-277"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="528c2-278">(30)</span><span class="sxs-lookup"><span data-stu-id="528c2-278">(30)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-279">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="528c2-279">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="528c2-280"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="528c2-280"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="528c2-281"> (31) </span><span class="sxs-lookup"><span data-stu-id="528c2-281">(31)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-282">裝置無法正常運作;Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="528c2-282">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="528c2-283">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="528c2-283">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-284">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="528c2-284">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-285">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-286">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="528c2-286">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="528c2-287">指出裝置是否使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="528c2-287">Indicates whether the device is using a user-defined configuration.</span></span>

<span data-ttu-id="528c2-288">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-288">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-289">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="528c2-289">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-290">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="528c2-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-291">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-292">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="528c2-292">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="528c2-293">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="528c2-293">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="528c2-294">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="528c2-294">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="528c2-295">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-295">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-296">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="528c2-296">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-297">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="528c2-297">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-298">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-299">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CurrentReading" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電子目前 \| 的探查 001.5 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ") </span><span class="sxs-lookup"><span data-stu-id="528c2-299">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="528c2-300">感應器指出的目前值。</span><span class="sxs-lookup"><span data-stu-id="528c2-300">Current value indicated by the sensor.</span></span>

<span data-ttu-id="528c2-301">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-301">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-302">**說明**</span><span class="sxs-lookup"><span data-stu-id="528c2-302">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-303">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="528c2-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-304">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-305">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="528c2-305">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="528c2-306">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="528c2-306">Textual description of the object.</span></span>

<span data-ttu-id="528c2-307">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-307">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-308">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="528c2-308">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-309">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="528c2-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-310">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-311">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="528c2-311">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="528c2-312">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="528c2-312">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="528c2-313">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-314">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="528c2-314">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-315">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="528c2-315">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-316">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="528c2-317">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="528c2-317">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="528c2-318">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-319">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="528c2-319">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-320">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="528c2-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="528c2-322">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="528c2-322">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="528c2-323">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-324">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="528c2-324">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-325">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="528c2-325">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-326">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-327">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="528c2-327">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="528c2-328">安裝物件的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="528c2-328">Date and time when the object was installed.</span></span> <span data-ttu-id="528c2-329">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="528c2-329">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="528c2-330">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-330">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-331">**IsLinear**</span><span class="sxs-lookup"><span data-stu-id="528c2-331">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-332">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="528c2-332">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-333">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="528c2-334">若 **為 TRUE**，表示感應器在其動態範圍內是線性的。</span><span class="sxs-lookup"><span data-stu-id="528c2-334">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="528c2-335">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-335">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-336">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="528c2-336">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-337">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="528c2-337">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-338">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="528c2-339">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="528c2-339">Last error code reported by the logical device.</span></span>

<span data-ttu-id="528c2-340">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-340">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-341">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="528c2-341">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-342">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="528c2-342">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-343">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-344">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "LowerThresholdCritical" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電子目前 \| 的探查 001.13 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ") </span><span class="sxs-lookup"><span data-stu-id="528c2-344">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.13"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="528c2-345">臨界值，指定感應器是否在重大情況下運作。</span><span class="sxs-lookup"><span data-stu-id="528c2-345">Threshold value that specifies whether the sensor is operating under critical conditions.</span></span> <span data-ttu-id="528c2-346">如果 **CurrentReading** 屬性是在 **LowerThresholdCritical** 和 **LowerThresholdFatal** 之間，則目前的狀態為「嚴重」。</span><span class="sxs-lookup"><span data-stu-id="528c2-346">If the **CurrentReading** property is between **LowerThresholdCritical** and **LowerThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="528c2-347">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-347">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-348">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="528c2-348">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-349">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="528c2-349">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-350">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-351">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "LowerThresholdFatal" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電子目前 \| 的探查 001.15 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ") </span><span class="sxs-lookup"><span data-stu-id="528c2-351">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="528c2-352">臨界值，指定感應器是否在嚴重狀況下運作。</span><span class="sxs-lookup"><span data-stu-id="528c2-352">Threshold value that specifies whether the sensor is operating under fatal conditions.</span></span> <span data-ttu-id="528c2-353">如果 **CurrentReading** 屬性低於 **LowerThresholdFatal**，則目前的狀態為「嚴重」。</span><span class="sxs-lookup"><span data-stu-id="528c2-353">If the **CurrentReading** property is below **LowerThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="528c2-354">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-354">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-355">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="528c2-355">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-356">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="528c2-356">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-357">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-358">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "LowerThresholdNonCritical" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電子目前 \| 的探查 001.11 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ") </span><span class="sxs-lookup"><span data-stu-id="528c2-358">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="528c2-359">臨界值，指定感應器是否在正常或非重大狀況下運作。</span><span class="sxs-lookup"><span data-stu-id="528c2-359">Threshold value that specifies whether the sensor is operating under normal or non-critical conditions.</span></span> <span data-ttu-id="528c2-360">如果 **CurrentReading** 屬性是在 **LowerThresholdNonCritical** 和 **UpperThresholdNonCritical** 之間，則感應器會回報正常值。</span><span class="sxs-lookup"><span data-stu-id="528c2-360">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="528c2-361">但是，如果 **CurrentReading** 屬性是在 **LowerThresholdNonCritical** 和 **LowerThresholdCritical** 之間，則目前的狀態為非關鍵性。</span><span class="sxs-lookup"><span data-stu-id="528c2-361">If the **CurrentReading** property, however, is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="528c2-362">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-362">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-363">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="528c2-363">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-364">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="528c2-364">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-365">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-366">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MaxReadable" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電子目前 \| 的探查 001.9 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ") </span><span class="sxs-lookup"><span data-stu-id="528c2-366">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="528c2-367">數值感應器可讀取之已測量屬性的最大值。</span><span class="sxs-lookup"><span data-stu-id="528c2-367">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="528c2-368">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-368">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-369">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="528c2-369">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-370">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="528c2-370">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-371">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-372">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MinReadable" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電子目前 \| 的探查 001.10 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ") </span><span class="sxs-lookup"><span data-stu-id="528c2-372">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="528c2-373">數值感應器可讀取之已測量屬性的最小值。</span><span class="sxs-lookup"><span data-stu-id="528c2-373">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="528c2-374">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-374">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-375">**名稱**</span><span class="sxs-lookup"><span data-stu-id="528c2-375">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-376">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="528c2-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-377">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-378">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="528c2-378">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="528c2-379">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="528c2-379">Label by which the object is known.</span></span> <span data-ttu-id="528c2-380">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="528c2-380">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="528c2-381">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-381">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-382">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="528c2-382">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-383">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="528c2-383">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-384">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-384">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-385">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "NominalReading" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電子目前 \| 的探查 001.6 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ") </span><span class="sxs-lookup"><span data-stu-id="528c2-385">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="528c2-386">數值感應器的預期值。</span><span class="sxs-lookup"><span data-stu-id="528c2-386">Expected value for the numeric sensor.</span></span>

<span data-ttu-id="528c2-387">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-387">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-388">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="528c2-388">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-389">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="528c2-389">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-390">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-391">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "NormalMax" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電子目前 \| 的探查 001.7 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ") </span><span class="sxs-lookup"><span data-stu-id="528c2-391">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="528c2-392">數值感應器的標準最大範圍。</span><span class="sxs-lookup"><span data-stu-id="528c2-392">Normal maximum range for the numeric sensor.</span></span>

<span data-ttu-id="528c2-393">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-393">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-394">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="528c2-394">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-395">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="528c2-395">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-396">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-397">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "NormalMin" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電子目前 \| 的探查 001.8 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ") </span><span class="sxs-lookup"><span data-stu-id="528c2-397">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="528c2-398">數值感應器的一般最小範圍。</span><span class="sxs-lookup"><span data-stu-id="528c2-398">Normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="528c2-399">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-399">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-400">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="528c2-400">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-401">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="528c2-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-402">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-403">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="528c2-403">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="528c2-404">邏輯裝置的 Win32 隨插即用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="528c2-404">Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="528c2-405">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="528c2-405">Example: "\*PNP030b"</span></span>

<span data-ttu-id="528c2-406">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-406">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-407">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="528c2-407">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-408">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="528c2-408">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="528c2-409">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="528c2-410">邏輯裝置的特定電源相關功能。</span><span class="sxs-lookup"><span data-stu-id="528c2-410">Specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="528c2-411">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="528c2-412"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="528c2-412"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="528c2-413"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="528c2-413"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="528c2-414"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="528c2-414"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="528c2-415"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="528c2-415"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-416">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="528c2-416">Power management features are currently enabled, but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="528c2-417"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="528c2-417"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-418">裝置可以根據使用或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="528c2-418">Device can change its power state based on use or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="528c2-419"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="528c2-419"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-420">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="528c2-420">The [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) method is supported.</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="528c2-421"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="528c2-421"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-422">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) 。</span><span class="sxs-lookup"><span data-stu-id="528c2-422">The [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="528c2-423"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="528c2-423"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="528c2-424">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) ，並將 *時間* 參數設定為特定日期和時間（或間隔），以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="528c2-424">The [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="528c2-425">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="528c2-425">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-426">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="528c2-426">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-427">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-427">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="528c2-428">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="528c2-428">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="528c2-429">這個屬性不表示電源管理功能目前已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="528c2-429">This property does not indicate that power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="528c2-430">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="528c2-430">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="528c2-431">如果為 **FALSE**，則字串為 "不支援" 的整數值1應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="528c2-431">If **FALSE**, the integer value 1, for the string "Not Supported", should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="528c2-432">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-433">**解決方法**</span><span class="sxs-lookup"><span data-stu-id="528c2-433">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-434">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="528c2-434">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-435">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-436">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「解析」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 電子目前 \| 的探查 001.17 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 十分之一 of milliamps ") </span><span class="sxs-lookup"><span data-stu-id="528c2-436">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="528c2-437">感應器解決測量屬性差異的能力。</span><span class="sxs-lookup"><span data-stu-id="528c2-437">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="528c2-438">這個屬性和 **精確度** 和 **容錯** 屬性是用來計算測量實體屬性的實際值。</span><span class="sxs-lookup"><span data-stu-id="528c2-438">This property, and the **Accuracy** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="528c2-439">此值可能會根據裝置的動態範圍是否為線性而有所不同。</span><span class="sxs-lookup"><span data-stu-id="528c2-439">This value can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="528c2-440">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-440">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-441">**狀態**</span><span class="sxs-lookup"><span data-stu-id="528c2-441">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-442">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="528c2-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-443">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-444">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="528c2-444">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="528c2-445">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="528c2-445">String that indicates the current status of the object.</span></span> <span data-ttu-id="528c2-446">您可以定義操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="528c2-446">Operational and nonoperational status can be defined.</span></span> <span data-ttu-id="528c2-447">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="528c2-447">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="528c2-448">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="528c2-448">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="528c2-449">Nonoperational 狀態可能包含「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="528c2-449">Nonoperational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="528c2-450">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="528c2-450">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="528c2-451">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="528c2-451">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="528c2-452">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-452">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="528c2-453">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="528c2-453">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="528c2-454">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="528c2-454">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="528c2-455">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="528c2-455">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="528c2-456">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="528c2-456">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="528c2-457">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="528c2-457">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="528c2-458">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="528c2-458">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="528c2-459">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="528c2-459">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="528c2-460">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="528c2-460">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="528c2-461">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="528c2-461">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="528c2-462">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="528c2-462">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="528c2-463">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="528c2-463">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="528c2-464">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="528c2-464">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="528c2-465">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="528c2-465">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="528c2-466">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="528c2-466">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-467">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="528c2-467">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-468">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-469">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="528c2-469">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="528c2-470">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="528c2-470">State of the logical device.</span></span> <span data-ttu-id="528c2-471">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="528c2-471">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="528c2-472">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-472">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="528c2-473">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="528c2-473">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="528c2-474">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="528c2-474">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="528c2-475">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="528c2-475">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="528c2-476">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="528c2-476">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="528c2-477">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="528c2-477">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="528c2-478">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="528c2-478">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-479">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="528c2-479">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-480">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-480">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-481">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="528c2-481">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="528c2-482">設定系統的 **CreationClassName** 屬性範圍。</span><span class="sxs-lookup"><span data-stu-id="528c2-482">Scoping system's **CreationClassName** property.</span></span>

<span data-ttu-id="528c2-483">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-483">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-484">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="528c2-484">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-485">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="528c2-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-486">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-486">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-487">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="528c2-487">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="528c2-488">範圍系統的 **名稱** 屬性。</span><span class="sxs-lookup"><span data-stu-id="528c2-488">Scoping system's **Name** property.</span></span>

<span data-ttu-id="528c2-489">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-489">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-490">**寬容**</span><span class="sxs-lookup"><span data-stu-id="528c2-490">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-491">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="528c2-491">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-492">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-493">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「容錯」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 電子目前 \| 的探查 001.18 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ") </span><span class="sxs-lookup"><span data-stu-id="528c2-493">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tolerance"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.18"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="528c2-494">測量屬性之感應器的容錯。</span><span class="sxs-lookup"><span data-stu-id="528c2-494">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="528c2-495">這個屬性（property）和 **解析** 和 **精確度** 屬性（property）可用來計算測量實體屬性的實際值。</span><span class="sxs-lookup"><span data-stu-id="528c2-495">This property, and the **Resolution** and **Accuracy** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="528c2-496">容錯可能會根據裝置的動態範圍是否為線性而有所不同。</span><span class="sxs-lookup"><span data-stu-id="528c2-496">Tolerance can vary depending on whether the device is linear over its dynamic range.</span></span>

</dd> <dt>

<span data-ttu-id="528c2-497">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="528c2-497">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-498">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="528c2-498">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-499">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-500">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "UpperThresholdCritical" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電子目前 \| 的探查 001.14 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ") </span><span class="sxs-lookup"><span data-stu-id="528c2-500">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="528c2-501">臨界值，指定感應器是否在重大情況下運作。</span><span class="sxs-lookup"><span data-stu-id="528c2-501">Threshold value that specifies whether the sensor is operating under critical conditions.</span></span> <span data-ttu-id="528c2-502">如果 **CurrentReading** 屬性是在 **UpperThresholdCritical** 和 **UpperThresholdFatal** 之間，則目前的狀態為「嚴重」。</span><span class="sxs-lookup"><span data-stu-id="528c2-502">If the **CurrentReading** property is between **UpperThresholdCritical** and **UpperThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="528c2-503">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-503">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-504">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="528c2-504">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-505">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="528c2-505">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-506">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-506">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-507">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "UpperThresholdFatal" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電子目前 \| 的探查 001.16 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ") </span><span class="sxs-lookup"><span data-stu-id="528c2-507">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="528c2-508">臨界值，指定感應器是否在嚴重狀況下運作。</span><span class="sxs-lookup"><span data-stu-id="528c2-508">Threshold value that specifies whether the sensor is operating under fatal conditions.</span></span> <span data-ttu-id="528c2-509">如果 **CurrentReading** 屬性高於 **UpperThresholdFatal**，則目前的狀態為「嚴重」。</span><span class="sxs-lookup"><span data-stu-id="528c2-509">If the **CurrentReading** property is above **UpperThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="528c2-510">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-510">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="528c2-511">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="528c2-511">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c2-512">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="528c2-512">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="528c2-513">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="528c2-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="528c2-514">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "UpperThresholdNonCritical" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 電子目前 \| 的探查 001.12 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ") </span><span class="sxs-lookup"><span data-stu-id="528c2-514">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="528c2-515">臨界值，指定感應器是否在正常或非重大狀況下運作。</span><span class="sxs-lookup"><span data-stu-id="528c2-515">Threshold value that specifies whether the sensor is operating under normal or non-critical conditions.</span></span> <span data-ttu-id="528c2-516">如果 **CurrentReading** 屬性是在 **LowerThresholdNonCritical** 和 **UpperThresholdNonCritical** 之間，則感應器會回報正常值。</span><span class="sxs-lookup"><span data-stu-id="528c2-516">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="528c2-517">但是，如果 **CurrentReading** 屬性是在 **UpperThresholdNonCritical** 和 **UpperThresholdCritical** 之間，則目前的狀態為非關鍵性。</span><span class="sxs-lookup"><span data-stu-id="528c2-517">If the **CurrentReading** property, however, is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="528c2-518">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-518">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="528c2-519">備註</span><span class="sxs-lookup"><span data-stu-id="528c2-519">Remarks</span></span>

<span data-ttu-id="528c2-520">**Cim \_ CurrentSensor** 類別衍生自 [**cim \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-520">The **CIM\_CurrentSensor** class is derived from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

<span data-ttu-id="528c2-521">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="528c2-521">WMI does not implement this class.</span></span> <span data-ttu-id="528c2-522">如需衍生自 **CIM \_ CURRENTSENSOR** 之 WMI 類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="528c2-522">For more information about WMI classes derived from **CIM\_CurrentSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="528c2-523">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="528c2-523">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="528c2-524">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="528c2-524">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="528c2-525">規格需求</span><span class="sxs-lookup"><span data-stu-id="528c2-525">Requirements</span></span>



| <span data-ttu-id="528c2-526">需求</span><span class="sxs-lookup"><span data-stu-id="528c2-526">Requirement</span></span> | <span data-ttu-id="528c2-527">值</span><span class="sxs-lookup"><span data-stu-id="528c2-527">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="528c2-528">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="528c2-528">Minimum supported client</span></span><br/> | <span data-ttu-id="528c2-529">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="528c2-529">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="528c2-530">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="528c2-530">Minimum supported server</span></span><br/> | <span data-ttu-id="528c2-531">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="528c2-531">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="528c2-532">命名空間</span><span class="sxs-lookup"><span data-stu-id="528c2-532">Namespace</span></span><br/>                | <span data-ttu-id="528c2-533">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="528c2-533">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="528c2-534">MOF</span><span class="sxs-lookup"><span data-stu-id="528c2-534">MOF</span></span><br/>                      | <dl> <span data-ttu-id="528c2-535"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="528c2-535"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="528c2-536">DLL</span><span class="sxs-lookup"><span data-stu-id="528c2-536">DLL</span></span><br/>                      | <dl> <span data-ttu-id="528c2-537"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="528c2-537"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="528c2-538">另請參閱</span><span class="sxs-lookup"><span data-stu-id="528c2-538">See also</span></span>

<dl> <dt>

[<span data-ttu-id="528c2-539">**CIM \_ NumericSensor**</span><span class="sxs-lookup"><span data-stu-id="528c2-539">**CIM\_NumericSensor**</span></span>](cim-numericsensor.md)
</dt> </dl>

 

