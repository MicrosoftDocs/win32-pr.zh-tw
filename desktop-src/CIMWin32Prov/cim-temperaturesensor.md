---
description: CIM \_ 溫度感應器類別存在，可回溯相容于舊版 cim 架構定義。
ms.assetid: ddef21db-e33a-4e2b-ac31-df3f0acd6fc2
ms.tgt_platform: multiple
title: CIM_TemperatureSensor 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TemperatureSensor
- CIM_TemperatureSensor.Accuracy
- CIM_TemperatureSensor.Availability
- CIM_TemperatureSensor.Caption
- CIM_TemperatureSensor.ConfigManagerErrorCode
- CIM_TemperatureSensor.ConfigManagerUserConfig
- CIM_TemperatureSensor.CreationClassName
- CIM_TemperatureSensor.CurrentReading
- CIM_TemperatureSensor.Description
- CIM_TemperatureSensor.DeviceID
- CIM_TemperatureSensor.ErrorCleared
- CIM_TemperatureSensor.ErrorDescription
- CIM_TemperatureSensor.InstallDate
- CIM_TemperatureSensor.IsLinear
- CIM_TemperatureSensor.LastErrorCode
- CIM_TemperatureSensor.LowerThresholdCritical
- CIM_TemperatureSensor.LowerThresholdFatal
- CIM_TemperatureSensor.LowerThresholdNonCritical
- CIM_TemperatureSensor.MaxReadable
- CIM_TemperatureSensor.MinReadable
- CIM_TemperatureSensor.Name
- CIM_TemperatureSensor.NominalReading
- CIM_TemperatureSensor.NormalMax
- CIM_TemperatureSensor.NormalMin
- CIM_TemperatureSensor.PNPDeviceID
- CIM_TemperatureSensor.PowerManagementCapabilities
- CIM_TemperatureSensor.PowerManagementSupported
- CIM_TemperatureSensor.Resolution
- CIM_TemperatureSensor.Status
- CIM_TemperatureSensor.StatusInfo
- CIM_TemperatureSensor.SystemCreationClassName
- CIM_TemperatureSensor.SystemName
- CIM_TemperatureSensor.Tolerance
- CIM_TemperatureSensor.UpperThresholdCritical
- CIM_TemperatureSensor.UpperThresholdFatal
- CIM_TemperatureSensor.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f48988db3cb213c06013b7ebac61095dbc365daa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317920"
---
# <a name="cim_temperaturesensor-class"></a><span data-ttu-id="6f504-103">CIM \_ 溫度感應器類別</span><span class="sxs-lookup"><span data-stu-id="6f504-103">CIM\_TemperatureSensor class</span></span>

<span data-ttu-id="6f504-104">**Cim \_ 溫度感應器** 類別存在，可回溯相容于舊版 cim 架構定義。</span><span class="sxs-lookup"><span data-stu-id="6f504-104">The **CIM\_TemperatureSensor** class exists for backward compatibility with earlier CIM schema definitions.</span></span> <span data-ttu-id="6f504-105">在2.2 版中，有 [**cim \_ 感應器**](cim-sensor.md) 和 [**cim \_ NumericSensor**](cim-numericsensor.md) 類別的新增功能，不再需要。</span><span class="sxs-lookup"><span data-stu-id="6f504-105">With additions to the [**CIM\_Sensor**](cim-sensor.md) and [**CIM\_NumericSensor**](cim-numericsensor.md) classes in version 2.2, it is no longer necessary.</span></span> <span data-ttu-id="6f504-106">您可以藉由將 **SensorType** 屬性（繼承自 **CIM \_ 感應器**）設定為 2 ( 「溫度」 ) 來定義溫度感應器。</span><span class="sxs-lookup"><span data-stu-id="6f504-106">A temperature sensor can be defined by setting the **SensorType** property, inherited from **CIM\_Sensor**, to 2 ("Temperature").</span></span> <span data-ttu-id="6f504-107">此類別的其他屬性會硬式編碼為對應至感應器階層中定義的常數值。</span><span class="sxs-lookup"><span data-stu-id="6f504-107">Other properties of this class are hardcoded as constant values that correspond to definitions in the sensor hierarchy.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6f504-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="6f504-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6f504-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="6f504-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6f504-110">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="6f504-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6f504-111">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="6f504-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f504-112">語法</span><span class="sxs-lookup"><span data-stu-id="6f504-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{9565979D-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_TemperatureSensor : CIM_NumericSensor
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

## <a name="members"></a><span data-ttu-id="6f504-113">成員</span><span class="sxs-lookup"><span data-stu-id="6f504-113">Members</span></span>

<span data-ttu-id="6f504-114">**CIM \_ 溫度感應器** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6f504-114">The **CIM\_TemperatureSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="6f504-115">方法</span><span class="sxs-lookup"><span data-stu-id="6f504-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="6f504-116">屬性</span><span class="sxs-lookup"><span data-stu-id="6f504-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6f504-117">方法</span><span class="sxs-lookup"><span data-stu-id="6f504-117">Methods</span></span>

<span data-ttu-id="6f504-118">**CIM \_ 溫度感應器** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="6f504-118">The **CIM\_TemperatureSensor** class has these methods.</span></span>



| <span data-ttu-id="6f504-119">方法</span><span class="sxs-lookup"><span data-stu-id="6f504-119">Method</span></span>                                                                       | <span data-ttu-id="6f504-120">描述</span><span class="sxs-lookup"><span data-stu-id="6f504-120">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f504-121">**重設**</span><span class="sxs-lookup"><span data-stu-id="6f504-121">**Reset**</span></span>](reset-method-in-class-cim-temperaturesensor.md)                 | <span data-ttu-id="6f504-122">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="6f504-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="6f504-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="6f504-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="6f504-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="6f504-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-temperaturesensor.md) | <span data-ttu-id="6f504-125">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="6f504-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="6f504-126">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="6f504-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6f504-127">屬性</span><span class="sxs-lookup"><span data-stu-id="6f504-127">Properties</span></span>

<span data-ttu-id="6f504-128">**CIM \_ 溫度感應器** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6f504-128">The **CIM\_TemperatureSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6f504-129">**精確度**</span><span class="sxs-lookup"><span data-stu-id="6f504-129">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-130">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="6f504-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-132">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「精確度」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 溫度探查 \| 001.19 ") </span><span class="sxs-lookup"><span data-stu-id="6f504-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Accuracy"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="6f504-133">測量的屬性之感應器的精確度。</span><span class="sxs-lookup"><span data-stu-id="6f504-133">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="6f504-134">其值會記錄為加號或減號百分之一%。</span><span class="sxs-lookup"><span data-stu-id="6f504-134">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="6f504-135">這個屬性（property）和 **解析** 和 **容錯** 屬性（property）可用來計算測量實體屬性的實際值。</span><span class="sxs-lookup"><span data-stu-id="6f504-135">This property, and the **Resolution** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="6f504-136">精確度可能會根據裝置的動態範圍是否為線性而有所不同。</span><span class="sxs-lookup"><span data-stu-id="6f504-136">Accuracy can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="6f504-137">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-137">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-138">**可用性**</span><span class="sxs-lookup"><span data-stu-id="6f504-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-139">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6f504-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-141">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="6f504-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="6f504-142">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="6f504-142">Availability and status of the device.</span></span>

<span data-ttu-id="6f504-143">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6f504-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="6f504-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6f504-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="6f504-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="6f504-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="6f504-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-147">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="6f504-147">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="6f504-148"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="6f504-148"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="6f504-149"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="6f504-149"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6f504-150"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="6f504-150"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="6f504-151"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="6f504-151"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="6f504-152"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="6f504-152"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="6f504-153"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="6f504-153"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6f504-154"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="6f504-154"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="6f504-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="6f504-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="6f504-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="6f504-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="6f504-157"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="6f504-157"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-158">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="6f504-158">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="6f504-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="6f504-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-160">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="6f504-160">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="6f504-161"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="6f504-161"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-162">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="6f504-162">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="6f504-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="6f504-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="6f504-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="6f504-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-165">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="6f504-165">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="6f504-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="6f504-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-167">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="6f504-167">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="6f504-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="6f504-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-169">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="6f504-169">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="6f504-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="6f504-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-171">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="6f504-171">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="6f504-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="6f504-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-173">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="6f504-173">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6f504-174">**標題**</span><span class="sxs-lookup"><span data-stu-id="6f504-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-175">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f504-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-177">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="6f504-177">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6f504-178">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="6f504-178">Short textual description of the object.</span></span>

<span data-ttu-id="6f504-179">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-180">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6f504-180">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-181">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6f504-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-183">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="6f504-183">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6f504-184">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6f504-184">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="6f504-185">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-185">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="6f504-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="6f504-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="6f504-187"> (0)</span><span class="sxs-lookup"><span data-stu-id="6f504-187">(0)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-188">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="6f504-188">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="6f504-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="6f504-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="6f504-190">(1)</span><span class="sxs-lookup"><span data-stu-id="6f504-190">(1)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-191">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="6f504-191">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6f504-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="6f504-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="6f504-193">(2)</span><span class="sxs-lookup"><span data-stu-id="6f504-193">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="6f504-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="6f504-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="6f504-195">(3)</span><span class="sxs-lookup"><span data-stu-id="6f504-195">(3)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-196">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="6f504-196">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6f504-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="6f504-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="6f504-198">(4)</span><span class="sxs-lookup"><span data-stu-id="6f504-198">(4)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-199">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="6f504-199">Device is not working properly.</span></span> <span data-ttu-id="6f504-200">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="6f504-200">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="6f504-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="6f504-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="6f504-202">(5)</span><span class="sxs-lookup"><span data-stu-id="6f504-202">(5)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-203">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="6f504-203">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="6f504-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="6f504-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="6f504-205">(6)</span><span class="sxs-lookup"><span data-stu-id="6f504-205">(6)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-206">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="6f504-206">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="6f504-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="6f504-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="6f504-208">(7)</span><span class="sxs-lookup"><span data-stu-id="6f504-208">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="6f504-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="6f504-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="6f504-210">(8)</span><span class="sxs-lookup"><span data-stu-id="6f504-210">(8)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-211">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="6f504-211">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="6f504-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="6f504-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="6f504-213">(9)</span><span class="sxs-lookup"><span data-stu-id="6f504-213">(9)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-214">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="6f504-214">Device is not working properly.</span></span> <span data-ttu-id="6f504-215">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="6f504-215">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="6f504-216"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="6f504-216"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="6f504-217">(10)</span><span class="sxs-lookup"><span data-stu-id="6f504-217">(10)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-218">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="6f504-218">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="6f504-219"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="6f504-219"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="6f504-220">(11)</span><span class="sxs-lookup"><span data-stu-id="6f504-220">(11)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-221">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="6f504-221">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="6f504-222"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="6f504-222"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="6f504-223"> (12) </span><span class="sxs-lookup"><span data-stu-id="6f504-223">(12)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-224">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="6f504-224">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="6f504-225"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="6f504-225"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="6f504-226">(13)</span><span class="sxs-lookup"><span data-stu-id="6f504-226">(13)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-227">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="6f504-227">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="6f504-228"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="6f504-228"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="6f504-229">(14)</span><span class="sxs-lookup"><span data-stu-id="6f504-229">(14)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-230">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="6f504-230">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="6f504-231"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="6f504-231"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="6f504-232">(15)</span><span class="sxs-lookup"><span data-stu-id="6f504-232">(15)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-233">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="6f504-233">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="6f504-234"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="6f504-234"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="6f504-235">(16)</span><span class="sxs-lookup"><span data-stu-id="6f504-235">(16)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-236">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="6f504-236">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="6f504-237"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="6f504-237"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="6f504-238">(17)</span><span class="sxs-lookup"><span data-stu-id="6f504-238">(17)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-239">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="6f504-239">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6f504-240"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="6f504-240"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="6f504-241">(18)</span><span class="sxs-lookup"><span data-stu-id="6f504-241">(18)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-242">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="6f504-242">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="6f504-243"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="6f504-243"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="6f504-244">(19)</span><span class="sxs-lookup"><span data-stu-id="6f504-244">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6f504-245"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="6f504-245"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="6f504-246">(20)</span><span class="sxs-lookup"><span data-stu-id="6f504-246">(20)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-247">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="6f504-247">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="6f504-248"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="6f504-248"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="6f504-249">(21)</span><span class="sxs-lookup"><span data-stu-id="6f504-249">(21)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-250">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="6f504-250">System failure.</span></span> <span data-ttu-id="6f504-251">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="6f504-251">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="6f504-252">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="6f504-252">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="6f504-253"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="6f504-253"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="6f504-254">(22)</span><span class="sxs-lookup"><span data-stu-id="6f504-254">(22)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-255">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="6f504-255">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="6f504-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="6f504-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="6f504-257">(23)</span><span class="sxs-lookup"><span data-stu-id="6f504-257">(23)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-258">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="6f504-258">System failure.</span></span> <span data-ttu-id="6f504-259">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="6f504-259">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="6f504-260"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="6f504-260"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="6f504-261">(24)</span><span class="sxs-lookup"><span data-stu-id="6f504-261">(24)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-262">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="6f504-262">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6f504-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="6f504-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="6f504-264">(25)</span><span class="sxs-lookup"><span data-stu-id="6f504-264">(25)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-265">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="6f504-265">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6f504-266"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="6f504-266"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="6f504-267">(26)</span><span class="sxs-lookup"><span data-stu-id="6f504-267">(26)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-268">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="6f504-268">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="6f504-269"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="6f504-269"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="6f504-270">(27)</span><span class="sxs-lookup"><span data-stu-id="6f504-270">(27)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-271">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="6f504-271">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="6f504-272"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="6f504-272"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="6f504-273">(28)</span><span class="sxs-lookup"><span data-stu-id="6f504-273">(28)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-274">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="6f504-274">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="6f504-275"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="6f504-275"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="6f504-276">(29)</span><span class="sxs-lookup"><span data-stu-id="6f504-276">(29)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-277">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="6f504-277">Device is disabled.</span></span> <span data-ttu-id="6f504-278">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="6f504-278">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="6f504-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="6f504-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="6f504-280">(30)</span><span class="sxs-lookup"><span data-stu-id="6f504-280">(30)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-281">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="6f504-281">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6f504-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="6f504-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="6f504-283"> (31) </span><span class="sxs-lookup"><span data-stu-id="6f504-283">(31)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-284">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="6f504-284">Device is not working properly.</span></span> <span data-ttu-id="6f504-285">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="6f504-285">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6f504-286">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="6f504-286">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-287">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="6f504-287">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-288">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-289">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="6f504-289">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6f504-290">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="6f504-290">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="6f504-291">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-291">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-292">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6f504-292">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-293">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f504-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-294">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-295">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6f504-295">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6f504-296">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f504-296">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="6f504-297">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="6f504-297">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="6f504-298">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-299">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="6f504-299">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-300">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="6f504-300">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-301">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-302">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CurrentReading" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 溫度探查 \| 001.5 「) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「十分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="6f504-302">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6f504-303">感應器指出的目前值。</span><span class="sxs-lookup"><span data-stu-id="6f504-303">Current value indicated by the sensor.</span></span>

<span data-ttu-id="6f504-304">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-304">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-305">**說明**</span><span class="sxs-lookup"><span data-stu-id="6f504-305">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-306">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f504-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-307">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-308">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="6f504-308">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6f504-309">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="6f504-309">Textual description of the object.</span></span>

<span data-ttu-id="6f504-310">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-310">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-311">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="6f504-311">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-312">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f504-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-313">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-314">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6f504-314">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6f504-315">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="6f504-315">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="6f504-316">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-317">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="6f504-317">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-318">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="6f504-318">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-319">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f504-320">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="6f504-320">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="6f504-321">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-321">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-322">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="6f504-322">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-323">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f504-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-324">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f504-325">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="6f504-325">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="6f504-326">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-326">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-327">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6f504-327">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-328">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="6f504-328">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-329">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-330">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="6f504-330">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6f504-331">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="6f504-331">Date and time the object was installed.</span></span> <span data-ttu-id="6f504-332">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="6f504-332">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="6f504-333">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-333">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-334">**IsLinear**</span><span class="sxs-lookup"><span data-stu-id="6f504-334">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-335">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="6f504-335">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-336">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f504-337">若 **為 TRUE**，表示感應器在其動態範圍內是線性的。</span><span class="sxs-lookup"><span data-stu-id="6f504-337">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="6f504-338">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-338">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-339">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6f504-339">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-340">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6f504-340">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-341">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f504-342">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6f504-342">Last error code reported by the logical device.</span></span>

<span data-ttu-id="6f504-343">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-343">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-344">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="6f504-344">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-345">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="6f504-345">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-346">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-347">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "LowerThresholdCritical" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 溫度探查 \| 001.13 「) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「十分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="6f504-347">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.13"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6f504-348">指定範圍 (最小值和最大值的閾值，) 以判斷感應器是否在正常、非關鍵性、重大或嚴重狀況下運作。</span><span class="sxs-lookup"><span data-stu-id="6f504-348">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="6f504-349">如果 **CurrentReading** 屬性是在 **LowerThresholdCritical** 和 **LowerThresholdFatal** 之間，則目前的狀態為「嚴重」。</span><span class="sxs-lookup"><span data-stu-id="6f504-349">If the **CurrentReading** property is between **LowerThresholdCritical** and **LowerThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="6f504-350">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-350">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-351">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="6f504-351">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-352">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="6f504-352">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-353">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-354">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "LowerThresholdFatal" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 溫度探查 \| 001.15 「) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「十分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="6f504-354">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6f504-355">指定範圍 (最小值和最大值的閾值，) 以判斷感應器是否在正常、非關鍵性、重大或嚴重狀況下運作。</span><span class="sxs-lookup"><span data-stu-id="6f504-355">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="6f504-356">如果 **CurrentReading** 屬性低於 **LowerThresholdFatal**，則目前的狀態為「嚴重」。</span><span class="sxs-lookup"><span data-stu-id="6f504-356">If the **CurrentReading** property is below **LowerThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="6f504-357">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-357">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-358">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="6f504-358">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-359">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="6f504-359">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-360">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-361">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "LowerThresholdNonCritical" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 溫度探查 \| 001.11 「) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「十分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="6f504-361">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6f504-362">指定範圍 (最小值和最大值的閾值，) 以判斷感應器是否在正常、非關鍵性、重大或嚴重狀況下運作。</span><span class="sxs-lookup"><span data-stu-id="6f504-362">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="6f504-363">如果 **CurrentReading** 屬性是在 **LowerThresholdNonCritical** 和 **UpperThresholdNonCritical** 之間，則感應器會回報正常值。</span><span class="sxs-lookup"><span data-stu-id="6f504-363">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="6f504-364">如果 **CurrentReading** 屬性是在 **LowerThresholdNonCritical** 和 **LowerThresholdCritical** 之間，則目前的狀態為非關鍵性。</span><span class="sxs-lookup"><span data-stu-id="6f504-364">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="6f504-365">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-365">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-366">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="6f504-366">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-367">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="6f504-367">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-368">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-369">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MaxReadable" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 溫度探查 \| 001.9 「) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「十分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="6f504-369">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6f504-370">數值感應器可讀取之已測量屬性的最大值。</span><span class="sxs-lookup"><span data-stu-id="6f504-370">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="6f504-371">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-371">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-372">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="6f504-372">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-373">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="6f504-373">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-374">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-375">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MinReadable" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 溫度探查 \| 001.10 「) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「十分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="6f504-375">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6f504-376">數值感應器可讀取之已測量屬性的最小值。</span><span class="sxs-lookup"><span data-stu-id="6f504-376">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="6f504-377">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-377">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-378">**名稱**</span><span class="sxs-lookup"><span data-stu-id="6f504-378">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-379">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f504-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-380">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-381">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="6f504-381">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6f504-382">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="6f504-382">Label by which the object is known.</span></span> <span data-ttu-id="6f504-383">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="6f504-383">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="6f504-384">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-384">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-385">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="6f504-385">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-386">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="6f504-386">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-387">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-388">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "NominalReading" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 溫度探查 \| 001.6 「) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「十分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="6f504-388">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6f504-389">數值感應器的預期值或標準值。</span><span class="sxs-lookup"><span data-stu-id="6f504-389">Expected or normal value for the numeric sensor.</span></span>

<span data-ttu-id="6f504-390">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-390">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-391">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="6f504-391">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-392">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="6f504-392">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-393">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-394">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "NormalMax" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 溫度探查 \| 001.7 「) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「十分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="6f504-394">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6f504-395">數值感應器的標準最大範圍。</span><span class="sxs-lookup"><span data-stu-id="6f504-395">Normal maximum range for the numeric sensor.</span></span>

<span data-ttu-id="6f504-396">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-396">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-397">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="6f504-397">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-398">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="6f504-398">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-399">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-400">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "NormalMin" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 溫度探查 \| 001.8 「) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「十分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="6f504-400">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6f504-401">數值感應器的一般最小範圍。</span><span class="sxs-lookup"><span data-stu-id="6f504-401">Normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="6f504-402">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-402">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-403">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="6f504-403">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-404">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f504-404">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-405">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-406">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="6f504-406">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6f504-407">邏輯裝置的 Win32 隨插即用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f504-407">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="6f504-408">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="6f504-409">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="6f504-409">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="6f504-410">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="6f504-410">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-411">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="6f504-411">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6f504-412">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f504-413">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="6f504-413">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="6f504-414">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="6f504-414">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6f504-415"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="6f504-415"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="6f504-416"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="6f504-416"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6f504-417"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="6f504-417"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6f504-418"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="6f504-418"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-419">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="6f504-419">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="6f504-420"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="6f504-420"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-421">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="6f504-421">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="6f504-422"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="6f504-422"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-423">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="6f504-423">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="6f504-424">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="6f504-424">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="6f504-425">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="6f504-425">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="6f504-426"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="6f504-426"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-427">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="6f504-427">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="6f504-428"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="6f504-428"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6f504-429">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="6f504-429">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6f504-430">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="6f504-430">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-431">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="6f504-431">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-432">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f504-433">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="6f504-433">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="6f504-434">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="6f504-434">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="6f504-435">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="6f504-435">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="6f504-436">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="6f504-436">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="6f504-437">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-437">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-438">**解決方法**</span><span class="sxs-lookup"><span data-stu-id="6f504-438">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-439">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6f504-439">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-440">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-441">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「解析」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 溫度探查 \| 001.17」 ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「百分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="6f504-441">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hundredths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6f504-442">感應器解決測量屬性差異的能力。</span><span class="sxs-lookup"><span data-stu-id="6f504-442">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="6f504-443">此值可能會根據裝置的動態範圍是否為線性而有所不同。</span><span class="sxs-lookup"><span data-stu-id="6f504-443">This value can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="6f504-444">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-444">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-445">**狀態**</span><span class="sxs-lookup"><span data-stu-id="6f504-445">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-446">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f504-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-447">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-448">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="6f504-448">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6f504-449">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="6f504-449">Current status of the object.</span></span> <span data-ttu-id="6f504-450">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-450">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6f504-451">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="6f504-451">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6f504-452">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="6f504-452">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6f504-453">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="6f504-453">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6f504-454">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="6f504-454">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6f504-455">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="6f504-455">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6f504-456">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="6f504-456">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6f504-457">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="6f504-457">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6f504-458">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="6f504-458">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6f504-459">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="6f504-459">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6f504-460">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="6f504-460">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6f504-461">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="6f504-461">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6f504-462">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="6f504-462">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6f504-463">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="6f504-463">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6f504-464">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="6f504-464">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-465">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6f504-465">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-466">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-467">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="6f504-467">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="6f504-468">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="6f504-468">State of the logical device.</span></span> <span data-ttu-id="6f504-469">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="6f504-469">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="6f504-470">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6f504-471">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="6f504-471">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6f504-472">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="6f504-472">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6f504-473">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="6f504-473">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6f504-474">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="6f504-474">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6f504-475">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="6f504-475">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6f504-476">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6f504-476">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-477">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f504-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-478">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-479">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6f504-479">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6f504-480">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="6f504-480">Scoping system's creation class name.</span></span>

<span data-ttu-id="6f504-481">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-481">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-482">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="6f504-482">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-483">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f504-483">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-484">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-485">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6f504-485">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6f504-486">設定系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="6f504-486">Scoping system's name.</span></span>

<span data-ttu-id="6f504-487">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-487">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-488">**寬容**</span><span class="sxs-lookup"><span data-stu-id="6f504-488">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-489">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="6f504-489">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-490">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-490">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-491">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「容錯」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 溫度探查 \| 001.18 「) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「十分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="6f504-491">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tolerance"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.18"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6f504-492">測量屬性之感應器的容錯。</span><span class="sxs-lookup"><span data-stu-id="6f504-492">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="6f504-493">這個屬性（property）和 **解析** 和 **精確度** 屬性（property）可用來計算測量實體屬性的實際值。</span><span class="sxs-lookup"><span data-stu-id="6f504-493">This property, and the **Resolution** and **Accuracy** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="6f504-494">容錯可能會根據裝置的動態範圍是否為線性而有所不同。</span><span class="sxs-lookup"><span data-stu-id="6f504-494">Tolerance can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="6f504-495">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-495">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-496">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="6f504-496">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-497">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="6f504-497">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-498">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-498">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-499">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "UpperThresholdCritical" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 溫度探查 \| 001.14 「) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「十分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="6f504-499">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6f504-500">指定範圍 (最小值和最大值的閾值，) 以判斷感應器是否在正常、非關鍵性、重大或嚴重狀況下運作。</span><span class="sxs-lookup"><span data-stu-id="6f504-500">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="6f504-501">如果 **CurrentReading** 屬性是在 **UpperThresholdCritical** 和 **UpperThresholdFatal** 之間，則目前的狀態為「嚴重」。</span><span class="sxs-lookup"><span data-stu-id="6f504-501">If the **CurrentReading** property is between **UpperThresholdCritical** and **UpperThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="6f504-502">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-502">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-503">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="6f504-503">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-504">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="6f504-504">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-505">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-505">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-506">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "UpperThresholdFatal" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 溫度探查 \| 001.16 「) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「十分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="6f504-506">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6f504-507">指定範圍 (最小值和最大值的閾值，) 以判斷感應器是否在正常、非關鍵性、重大或嚴重狀況下運作。</span><span class="sxs-lookup"><span data-stu-id="6f504-507">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="6f504-508">如果 **CurrentReading** 屬性高於 **UpperThresholdFatal**，則目前的狀態為「嚴重」。</span><span class="sxs-lookup"><span data-stu-id="6f504-508">If the **CurrentReading** property is above **UpperThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="6f504-509">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-509">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f504-510">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="6f504-510">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f504-511">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="6f504-511">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f504-512">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f504-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f504-513">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "UpperThresholdNonCritical" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 溫度探查 \| 001.12 「) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「十分之一度攝氏」 ) </span><span class="sxs-lookup"><span data-stu-id="6f504-513">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6f504-514">指定範圍 (最小值和最大值的閾值，) 以判斷感應器是否在正常、非關鍵性、重大或嚴重狀況下運作。</span><span class="sxs-lookup"><span data-stu-id="6f504-514">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="6f504-515">如果 **CurrentReading** 屬性是在 **LowerThresholdNonCritical** 和 **UpperThresholdNonCritical** 之間，則感應器會回報正常值。</span><span class="sxs-lookup"><span data-stu-id="6f504-515">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="6f504-516">如果 **CurrentReading** 屬性是在 **UpperThresholdNonCritical** 和 **UpperThresholdCritical** 之間，則目前的狀態為非關鍵性。</span><span class="sxs-lookup"><span data-stu-id="6f504-516">If the **CurrentReading** property is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="6f504-517">這個屬性繼承自 [**CIM \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-517">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6f504-518">備註</span><span class="sxs-lookup"><span data-stu-id="6f504-518">Remarks</span></span>

<span data-ttu-id="6f504-519">**Cim \_ 溫度感應器** 類別衍生自 [**cim \_ NumericSensor**](cim-numericsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-519">The **CIM\_TemperatureSensor** class is derived from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

<span data-ttu-id="6f504-520">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="6f504-520">WMI does not implement this class.</span></span> <span data-ttu-id="6f504-521">針對衍生自 **CIM \_ 溫度感應器** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="6f504-521">For WMI classes derived from **CIM\_TemperatureSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="6f504-522">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="6f504-522">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6f504-523">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="6f504-523">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f504-524">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f504-524">Requirements</span></span>



| <span data-ttu-id="6f504-525">需求</span><span class="sxs-lookup"><span data-stu-id="6f504-525">Requirement</span></span> | <span data-ttu-id="6f504-526">值</span><span class="sxs-lookup"><span data-stu-id="6f504-526">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f504-527">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6f504-527">Minimum supported client</span></span><br/> | <span data-ttu-id="6f504-528">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f504-528">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6f504-529">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6f504-529">Minimum supported server</span></span><br/> | <span data-ttu-id="6f504-530">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f504-530">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6f504-531">命名空間</span><span class="sxs-lookup"><span data-stu-id="6f504-531">Namespace</span></span><br/>                | <span data-ttu-id="6f504-532">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6f504-532">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6f504-533">MOF</span><span class="sxs-lookup"><span data-stu-id="6f504-533">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f504-534"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f504-534"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f504-535">DLL</span><span class="sxs-lookup"><span data-stu-id="6f504-535">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f504-536"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f504-536"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f504-537">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f504-537">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f504-538">**CIM \_ NumericSensor**</span><span class="sxs-lookup"><span data-stu-id="6f504-538">**CIM\_NumericSensor**</span></span>](cim-numericsensor.md)
</dt> </dl>

 

