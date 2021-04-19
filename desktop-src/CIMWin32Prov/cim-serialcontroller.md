---
description: CIM \_ SerialController 類別代表序列埠邏輯裝置的功能和管理。
ms.assetid: 7d5a96aa-fa6c-4904-8ca1-88ec14748810
ms.tgt_platform: multiple
title: 'CIM_SerialController 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SerialController
- CIM_SerialController.Availability
- CIM_SerialController.Capabilities
- CIM_SerialController.CapabilityDescriptions
- CIM_SerialController.Caption
- CIM_SerialController.ConfigManagerErrorCode
- CIM_SerialController.ConfigManagerUserConfig
- CIM_SerialController.CreationClassName
- CIM_SerialController.Description
- CIM_SerialController.DeviceID
- CIM_SerialController.ErrorCleared
- CIM_SerialController.ErrorDescription
- CIM_SerialController.InstallDate
- CIM_SerialController.LastErrorCode
- CIM_SerialController.MaxBaudRate
- CIM_SerialController.MaxNumberControlled
- CIM_SerialController.Name
- CIM_SerialController.PNPDeviceID
- CIM_SerialController.PowerManagementCapabilities
- CIM_SerialController.PowerManagementSupported
- CIM_SerialController.ProtocolSupported
- CIM_SerialController.Status
- CIM_SerialController.StatusInfo
- CIM_SerialController.SystemCreationClassName
- CIM_SerialController.SystemName
- CIM_SerialController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e23c9183dabb9b4d9ea25f5f92bd4c8ec6667c04
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970918"
---
# <a name="cim_serialcontroller-class-cimwin32-wmi-providers"></a><span data-ttu-id="39e8c-103">CIM_SerialController 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="39e8c-103">CIM_SerialController class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="39e8c-104">**CIM \_ SerialController** 類別代表序列埠邏輯裝置的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="39e8c-104">The **CIM\_SerialController** class represents the capabilities and management of the serial port logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="39e8c-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="39e8c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="39e8c-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="39e8c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="39e8c-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="39e8c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="39e8c-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="39e8c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="39e8c-109">語法</span><span class="sxs-lookup"><span data-stu-id="39e8c-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C554-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_SerialController : CIM_Controller
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
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
  uint32   MaxBaudRate;
  uint32   MaxNumberControlled;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="39e8c-110">成員</span><span class="sxs-lookup"><span data-stu-id="39e8c-110">Members</span></span>

<span data-ttu-id="39e8c-111">**CIM \_ SerialController** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="39e8c-111">The **CIM\_SerialController** class has these types of members:</span></span>

-   [<span data-ttu-id="39e8c-112">方法</span><span class="sxs-lookup"><span data-stu-id="39e8c-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="39e8c-113">屬性</span><span class="sxs-lookup"><span data-stu-id="39e8c-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="39e8c-114">方法</span><span class="sxs-lookup"><span data-stu-id="39e8c-114">Methods</span></span>

<span data-ttu-id="39e8c-115">**CIM \_ SerialController** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="39e8c-115">The **CIM\_SerialController** class has these methods.</span></span>



| <span data-ttu-id="39e8c-116">方法</span><span class="sxs-lookup"><span data-stu-id="39e8c-116">Method</span></span>                                                                      | <span data-ttu-id="39e8c-117">描述</span><span class="sxs-lookup"><span data-stu-id="39e8c-117">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39e8c-118">**重設**</span><span class="sxs-lookup"><span data-stu-id="39e8c-118">**Reset**</span></span>](reset-method-in-class-cim-serialcontroller.md)                 | <span data-ttu-id="39e8c-119">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="39e8c-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="39e8c-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="39e8c-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="39e8c-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="39e8c-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-serialcontroller.md) | <span data-ttu-id="39e8c-122">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="39e8c-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="39e8c-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="39e8c-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="39e8c-124">屬性</span><span class="sxs-lookup"><span data-stu-id="39e8c-124">Properties</span></span>

<span data-ttu-id="39e8c-125">**CIM \_ SerialController** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="39e8c-125">The **CIM\_SerialController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="39e8c-126">**可用性**</span><span class="sxs-lookup"><span data-stu-id="39e8c-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e8c-127">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="39e8c-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39e8c-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-129">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="39e8c-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="39e8c-130">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="39e8c-130">Availability and status of the device.</span></span>

<span data-ttu-id="39e8c-131">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="39e8c-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="39e8c-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="39e8c-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="39e8c-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="39e8c-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="39e8c-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="39e8c-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="39e8c-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="39e8c-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="39e8c-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="39e8c-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="39e8c-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="39e8c-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="39e8c-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="39e8c-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="39e8c-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="39e8c-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="39e8c-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="39e8c-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="39e8c-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="39e8c-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="39e8c-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="39e8c-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="39e8c-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="39e8c-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="39e8c-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="39e8c-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-145">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="39e8c-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="39e8c-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="39e8c-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-147">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="39e8c-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="39e8c-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="39e8c-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-149">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="39e8c-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="39e8c-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="39e8c-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="39e8c-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="39e8c-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-152">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="39e8c-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="39e8c-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="39e8c-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-154">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="39e8c-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="39e8c-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="39e8c-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-156">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="39e8c-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="39e8c-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="39e8c-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-158">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="39e8c-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="39e8c-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="39e8c-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-160">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="39e8c-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="39e8c-161">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="39e8c-161">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e8c-162">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="39e8c-162">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39e8c-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-164">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 序列埠 \| 004.7 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SerialController**。**CapabilityDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="39e8c-164">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Serial Ports\|004.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SerialController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="39e8c-165">序列控制器的晶片層級相容性。</span><span class="sxs-lookup"><span data-stu-id="39e8c-165">Chip-level compatibility for the serial controller.</span></span> <span data-ttu-id="39e8c-166">此屬性描述可能在晶片硬體內的緩衝區和序列控制器的其他功能。</span><span class="sxs-lookup"><span data-stu-id="39e8c-166">This property describes buffering and other capabilities of the serial controller, that may be inherent in the chip hardware.</span></span> <span data-ttu-id="39e8c-167">這個屬性是列舉的整數。</span><span class="sxs-lookup"><span data-stu-id="39e8c-167">This property is an enumerated integer.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="39e8c-168">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="39e8c-168">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="39e8c-169">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="39e8c-169">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="39e8c-170">**XT/相容** (3) </span><span class="sxs-lookup"><span data-stu-id="39e8c-170">**XT/AT Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="16450_Compatible"></span><span id="16450_compatible"></span><span id="16450_COMPATIBLE"></span>

<span data-ttu-id="39e8c-171">**16450 相容** (4) </span><span class="sxs-lookup"><span data-stu-id="39e8c-171">**16450 Compatible** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="16550_Compatible"></span><span id="16550_compatible"></span><span id="16550_COMPATIBLE"></span>

<span data-ttu-id="39e8c-172">**16550 相容** (5) </span><span class="sxs-lookup"><span data-stu-id="39e8c-172">**16550 Compatible** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="16550A_Compatible"></span><span id="16550a_compatible"></span><span id="16550A_COMPATIBLE"></span>

<span data-ttu-id="39e8c-173">**16550A 相容** (6) </span><span class="sxs-lookup"><span data-stu-id="39e8c-173">**16550A Compatible** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

<span data-ttu-id="39e8c-174">**8251 相容** (160) </span><span class="sxs-lookup"><span data-stu-id="39e8c-174">**8251 Compatible** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="8251FIFO_Compatible"></span><span id="8251fifo_compatible"></span><span id="8251FIFO_COMPATIBLE"></span>

<span data-ttu-id="39e8c-175">**8251FIFO 相容** (161) </span><span class="sxs-lookup"><span data-stu-id="39e8c-175">**8251FIFO Compatible** (161)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="39e8c-176">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="39e8c-176">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e8c-177">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="39e8c-177">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39e8c-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-179">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ SerialController**。**功能**") </span><span class="sxs-lookup"><span data-stu-id="39e8c-179">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SerialController**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="39e8c-180">自由格式字串，提供 **功能** 陣列中所指出之序列控制器功能的詳細說明。</span><span class="sxs-lookup"><span data-stu-id="39e8c-180">Free-form strings that provide detailed explanations for the serial controller features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="39e8c-181">這個陣列的每個專案都與位於相同索引的 **功能** 陣列中的專案相關。</span><span class="sxs-lookup"><span data-stu-id="39e8c-181">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="39e8c-182">**標題**</span><span class="sxs-lookup"><span data-stu-id="39e8c-182">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e8c-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="39e8c-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39e8c-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-185">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="39e8c-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="39e8c-186">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="39e8c-186">Short textual description of the object.</span></span>

<span data-ttu-id="39e8c-187">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="39e8c-187">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="39e8c-188">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="39e8c-188">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e8c-189">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="39e8c-189">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39e8c-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-191">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="39e8c-191">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="39e8c-192">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="39e8c-192">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="39e8c-193">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="39e8c-193">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="39e8c-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="39e8c-195"> (0)</span><span class="sxs-lookup"><span data-stu-id="39e8c-195">(0)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-196">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="39e8c-196">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="39e8c-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="39e8c-198">(1)</span><span class="sxs-lookup"><span data-stu-id="39e8c-198">(1)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-199">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="39e8c-199">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="39e8c-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="39e8c-201">(2)</span><span class="sxs-lookup"><span data-stu-id="39e8c-201">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="39e8c-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="39e8c-203">(3)</span><span class="sxs-lookup"><span data-stu-id="39e8c-203">(3)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-204">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="39e8c-204">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="39e8c-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="39e8c-206">(4)</span><span class="sxs-lookup"><span data-stu-id="39e8c-206">(4)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-207">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="39e8c-207">Device is not working properly.</span></span> <span data-ttu-id="39e8c-208">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="39e8c-208">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="39e8c-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="39e8c-210">(5)</span><span class="sxs-lookup"><span data-stu-id="39e8c-210">(5)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-211">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="39e8c-211">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="39e8c-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="39e8c-213">(6)</span><span class="sxs-lookup"><span data-stu-id="39e8c-213">(6)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-214">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="39e8c-214">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="39e8c-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="39e8c-216">(7)</span><span class="sxs-lookup"><span data-stu-id="39e8c-216">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="39e8c-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="39e8c-218">(8)</span><span class="sxs-lookup"><span data-stu-id="39e8c-218">(8)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-219">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="39e8c-219">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="39e8c-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="39e8c-221">(9)</span><span class="sxs-lookup"><span data-stu-id="39e8c-221">(9)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-222">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="39e8c-222">Device is not working properly.</span></span> <span data-ttu-id="39e8c-223">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="39e8c-223">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="39e8c-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="39e8c-225">(10)</span><span class="sxs-lookup"><span data-stu-id="39e8c-225">(10)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-226">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="39e8c-226">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="39e8c-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="39e8c-228">(11)</span><span class="sxs-lookup"><span data-stu-id="39e8c-228">(11)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-229">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="39e8c-229">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="39e8c-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="39e8c-231"> (12) </span><span class="sxs-lookup"><span data-stu-id="39e8c-231">(12)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-232">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="39e8c-232">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="39e8c-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="39e8c-234">(13)</span><span class="sxs-lookup"><span data-stu-id="39e8c-234">(13)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-235">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="39e8c-235">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="39e8c-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="39e8c-237">(14)</span><span class="sxs-lookup"><span data-stu-id="39e8c-237">(14)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-238">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="39e8c-238">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="39e8c-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="39e8c-240">(15)</span><span class="sxs-lookup"><span data-stu-id="39e8c-240">(15)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-241">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="39e8c-241">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="39e8c-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="39e8c-243">(16)</span><span class="sxs-lookup"><span data-stu-id="39e8c-243">(16)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-244">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="39e8c-244">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="39e8c-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="39e8c-246">(17)</span><span class="sxs-lookup"><span data-stu-id="39e8c-246">(17)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-247">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="39e8c-247">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="39e8c-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="39e8c-249">(18)</span><span class="sxs-lookup"><span data-stu-id="39e8c-249">(18)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-250">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="39e8c-250">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="39e8c-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="39e8c-252">(19)</span><span class="sxs-lookup"><span data-stu-id="39e8c-252">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="39e8c-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="39e8c-254">(20)</span><span class="sxs-lookup"><span data-stu-id="39e8c-254">(20)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-255">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="39e8c-255">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="39e8c-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="39e8c-257">(21)</span><span class="sxs-lookup"><span data-stu-id="39e8c-257">(21)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-258">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="39e8c-258">System failure.</span></span> <span data-ttu-id="39e8c-259">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="39e8c-259">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="39e8c-260">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="39e8c-260">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="39e8c-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="39e8c-262">(22)</span><span class="sxs-lookup"><span data-stu-id="39e8c-262">(22)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-263">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="39e8c-263">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="39e8c-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="39e8c-265">(23)</span><span class="sxs-lookup"><span data-stu-id="39e8c-265">(23)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-266">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="39e8c-266">System failure.</span></span> <span data-ttu-id="39e8c-267">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="39e8c-267">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="39e8c-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="39e8c-269">(24)</span><span class="sxs-lookup"><span data-stu-id="39e8c-269">(24)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-270">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="39e8c-270">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="39e8c-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="39e8c-272">(25)</span><span class="sxs-lookup"><span data-stu-id="39e8c-272">(25)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-273">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="39e8c-273">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="39e8c-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="39e8c-275">(26)</span><span class="sxs-lookup"><span data-stu-id="39e8c-275">(26)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-276">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="39e8c-276">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="39e8c-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="39e8c-278">(27)</span><span class="sxs-lookup"><span data-stu-id="39e8c-278">(27)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-279">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="39e8c-279">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="39e8c-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="39e8c-281">(28)</span><span class="sxs-lookup"><span data-stu-id="39e8c-281">(28)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-282">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="39e8c-282">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="39e8c-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="39e8c-284">(29)</span><span class="sxs-lookup"><span data-stu-id="39e8c-284">(29)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-285">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="39e8c-285">Device is disabled.</span></span> <span data-ttu-id="39e8c-286">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="39e8c-286">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="39e8c-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="39e8c-288">(30)</span><span class="sxs-lookup"><span data-stu-id="39e8c-288">(30)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-289">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="39e8c-289">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="39e8c-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="39e8c-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="39e8c-291"> (31) </span><span class="sxs-lookup"><span data-stu-id="39e8c-291">(31)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-292">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="39e8c-292">Device is not working properly.</span></span> <span data-ttu-id="39e8c-293">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="39e8c-293">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="39e8c-294">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="39e8c-294">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e8c-295">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="39e8c-295">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-296">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39e8c-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-297">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="39e8c-297">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="39e8c-298">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="39e8c-298">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="39e8c-299">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="39e8c-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="39e8c-300">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="39e8c-300">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e8c-301">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="39e8c-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-302">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39e8c-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-303">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="39e8c-303">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="39e8c-304">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="39e8c-304">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="39e8c-305">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="39e8c-305">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="39e8c-306">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="39e8c-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="39e8c-307">**說明**</span><span class="sxs-lookup"><span data-stu-id="39e8c-307">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e8c-308">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="39e8c-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-309">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39e8c-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-310">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="39e8c-310">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="39e8c-311">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="39e8c-311">Textual description of the object.</span></span>

<span data-ttu-id="39e8c-312">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="39e8c-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="39e8c-313">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="39e8c-313">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e8c-314">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="39e8c-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-315">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39e8c-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-316">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="39e8c-316">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="39e8c-317">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="39e8c-317">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="39e8c-318">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="39e8c-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="39e8c-319">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="39e8c-319">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e8c-320">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="39e8c-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39e8c-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39e8c-322">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="39e8c-322">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="39e8c-323">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="39e8c-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="39e8c-324">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="39e8c-324">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e8c-325">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="39e8c-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-326">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39e8c-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39e8c-327">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="39e8c-327">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="39e8c-328">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="39e8c-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="39e8c-329">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="39e8c-329">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e8c-330">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="39e8c-330">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-331">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39e8c-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-332">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="39e8c-332">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="39e8c-333">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="39e8c-333">Date and time the object was installed.</span></span> <span data-ttu-id="39e8c-334">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="39e8c-334">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="39e8c-335">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="39e8c-335">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="39e8c-336">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="39e8c-336">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e8c-337">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="39e8c-337">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-338">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39e8c-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39e8c-339">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="39e8c-339">Last error code reported by the logical device.</span></span>

<span data-ttu-id="39e8c-340">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="39e8c-340">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="39e8c-341">**MaxBaudRate**</span><span class="sxs-lookup"><span data-stu-id="39e8c-341">**MaxBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e8c-342">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="39e8c-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-343">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39e8c-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-344">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 序列埠 \| 004.6 「) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="39e8c-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Serial Ports\|004.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="39e8c-345">序列控制器支援的最大傳輸速率（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="39e8c-345">Maximum baud rate, in bits-per-second, supported by the serial controller.</span></span>

</dd> <dt>

<span data-ttu-id="39e8c-346">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="39e8c-346">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e8c-347">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="39e8c-347">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-348">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39e8c-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-349">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 匯流排埠 \| 001.9 ") </span><span class="sxs-lookup"><span data-stu-id="39e8c-349">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="39e8c-350">控制器支援的直接可定址實體數目上限。</span><span class="sxs-lookup"><span data-stu-id="39e8c-350">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="39e8c-351">如果數位為未知或無限制，則應使用0值。</span><span class="sxs-lookup"><span data-stu-id="39e8c-351">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="39e8c-352">這個屬性繼承自 [**CIM \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="39e8c-352">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="39e8c-353">**名稱**</span><span class="sxs-lookup"><span data-stu-id="39e8c-353">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e8c-354">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="39e8c-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-355">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39e8c-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-356">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="39e8c-356">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="39e8c-357">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="39e8c-357">Label by which the object is known.</span></span> <span data-ttu-id="39e8c-358">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="39e8c-358">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="39e8c-359">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="39e8c-359">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="39e8c-360">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="39e8c-360">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e8c-361">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="39e8c-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-362">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39e8c-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-363">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="39e8c-363">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="39e8c-364">邏輯裝置的 Win32 隨插即用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="39e8c-364">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="39e8c-365">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="39e8c-365">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="39e8c-366">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="39e8c-366">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="39e8c-367">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="39e8c-367">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e8c-368">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="39e8c-368">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-369">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39e8c-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39e8c-370">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="39e8c-370">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="39e8c-371">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="39e8c-371">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="39e8c-372"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="39e8c-372"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="39e8c-373"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="39e8c-373"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="39e8c-374"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="39e8c-374"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="39e8c-375"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="39e8c-375"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-376">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="39e8c-376">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="39e8c-377"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="39e8c-377"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-378">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="39e8c-378">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="39e8c-379"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="39e8c-379"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-380">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="39e8c-380">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="39e8c-381">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="39e8c-381">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="39e8c-382">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="39e8c-382">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="39e8c-383"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="39e8c-383"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-384">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="39e8c-384">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="39e8c-385"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="39e8c-385"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="39e8c-386">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="39e8c-386">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="39e8c-387">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="39e8c-387">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e8c-388">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="39e8c-388">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-389">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39e8c-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39e8c-390">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="39e8c-390">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="39e8c-391">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="39e8c-391">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="39e8c-392">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="39e8c-392">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="39e8c-393">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="39e8c-393">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="39e8c-394">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="39e8c-394">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="39e8c-395">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="39e8c-395">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e8c-396">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="39e8c-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-397">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39e8c-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-398">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 匯流排埠 \| 001.2 "，" MIF。DMTF \| 磁片 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="39e8c-398">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="39e8c-399">控制器用來存取「受控制」裝置的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="39e8c-399">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="39e8c-400">這個屬性繼承自 [**CIM \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="39e8c-400">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="39e8c-401">值為：</span><span class="sxs-lookup"><span data-stu-id="39e8c-401">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="39e8c-402">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="39e8c-402">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="39e8c-403">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="39e8c-403">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="39e8c-404">**EISA** (3) </span><span class="sxs-lookup"><span data-stu-id="39e8c-404">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="39e8c-405">**ISA** (4) </span><span class="sxs-lookup"><span data-stu-id="39e8c-405">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="39e8c-406">**PCI** (5) </span><span class="sxs-lookup"><span data-stu-id="39e8c-406">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="39e8c-407">**ATA/ATAPI** (6) </span><span class="sxs-lookup"><span data-stu-id="39e8c-407">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="39e8c-408">**彈性磁片** (7) </span><span class="sxs-lookup"><span data-stu-id="39e8c-408">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="39e8c-409">**1496** (8) </span><span class="sxs-lookup"><span data-stu-id="39e8c-409">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="39e8c-410">**SCSI 平行介面** (9) </span><span class="sxs-lookup"><span data-stu-id="39e8c-410">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="39e8c-411">**SCSI 光纖通道通訊協定** (10) </span><span class="sxs-lookup"><span data-stu-id="39e8c-411">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="39e8c-412">**SCSI 序列匯流排通訊協定** (11) </span><span class="sxs-lookup"><span data-stu-id="39e8c-412">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="39e8c-413">**SCSI 序列匯流排通訊協定-2 (1394)** (12) </span><span class="sxs-lookup"><span data-stu-id="39e8c-413">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="39e8c-414">**SCSI 序列儲存架構** (13) </span><span class="sxs-lookup"><span data-stu-id="39e8c-414">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="39e8c-415">**VESA** (14) </span><span class="sxs-lookup"><span data-stu-id="39e8c-415">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="39e8c-416">**PCMCIA** (15) </span><span class="sxs-lookup"><span data-stu-id="39e8c-416">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="39e8c-417">**通用序列匯流排** (16) </span><span class="sxs-lookup"><span data-stu-id="39e8c-417">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="39e8c-418">**平行通訊協定** (17) </span><span class="sxs-lookup"><span data-stu-id="39e8c-418">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="39e8c-419">**ESCON** (18) </span><span class="sxs-lookup"><span data-stu-id="39e8c-419">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="39e8c-420">**診斷** (19) </span><span class="sxs-lookup"><span data-stu-id="39e8c-420">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="39e8c-421">**I2C** (20) </span><span class="sxs-lookup"><span data-stu-id="39e8c-421">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="39e8c-422">**Power** (21) </span><span class="sxs-lookup"><span data-stu-id="39e8c-422">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="39e8c-423">**HIPPI** (22) </span><span class="sxs-lookup"><span data-stu-id="39e8c-423">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="39e8c-424">**MultiBus** (23) </span><span class="sxs-lookup"><span data-stu-id="39e8c-424">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="39e8c-425">**Vm** (24) </span><span class="sxs-lookup"><span data-stu-id="39e8c-425">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="39e8c-426">**IPI** (25) </span><span class="sxs-lookup"><span data-stu-id="39e8c-426">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="39e8c-427">**IEEE-488** (26) </span><span class="sxs-lookup"><span data-stu-id="39e8c-427">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="39e8c-428">**RS232** (27) </span><span class="sxs-lookup"><span data-stu-id="39e8c-428">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="39e8c-429">**IEEE 802.3 10BASE5** (28) </span><span class="sxs-lookup"><span data-stu-id="39e8c-429">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="39e8c-430">**IEEE 802.3 10BASE2** (29) </span><span class="sxs-lookup"><span data-stu-id="39e8c-430">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="39e8c-431">**IEEE 802.3 1BASE5** (30) </span><span class="sxs-lookup"><span data-stu-id="39e8c-431">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="39e8c-432">**IEEE 802.3 10BROAD36** (31) </span><span class="sxs-lookup"><span data-stu-id="39e8c-432">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="39e8c-433">**IEEE 802.3 100BASEVG** (32) </span><span class="sxs-lookup"><span data-stu-id="39e8c-433">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="39e8c-434">**IEEE 802.5 權杖-環形** (33) </span><span class="sxs-lookup"><span data-stu-id="39e8c-434">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="39e8c-435">**ANSI x3t 9.5 FDDI** (34) </span><span class="sxs-lookup"><span data-stu-id="39e8c-435">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="39e8c-436">**MCA** (35) </span><span class="sxs-lookup"><span data-stu-id="39e8c-436">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="39e8c-437">**ESDI** (36) </span><span class="sxs-lookup"><span data-stu-id="39e8c-437">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="39e8c-438">**IDE** (37) </span><span class="sxs-lookup"><span data-stu-id="39e8c-438">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="39e8c-439">**CMD** (38) </span><span class="sxs-lookup"><span data-stu-id="39e8c-439">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="39e8c-440">**ST506** (39) </span><span class="sxs-lookup"><span data-stu-id="39e8c-440">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="39e8c-441">**」 Dssi 小組** (40) </span><span class="sxs-lookup"><span data-stu-id="39e8c-441">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="39e8c-442">**QIC2** (41) </span><span class="sxs-lookup"><span data-stu-id="39e8c-442">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="39e8c-443">**增強型 ATA/IDE** (42) </span><span class="sxs-lookup"><span data-stu-id="39e8c-443">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="39e8c-444">**AGP** (43) </span><span class="sxs-lookup"><span data-stu-id="39e8c-444">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="39e8c-445">**TWIRP (雙向紅外線)** (44) </span><span class="sxs-lookup"><span data-stu-id="39e8c-445">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="39e8c-446">**(快速紅外線)** (45) 的杉樹</span><span class="sxs-lookup"><span data-stu-id="39e8c-446">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="39e8c-447">**SIR (串列紅外線)** (46) </span><span class="sxs-lookup"><span data-stu-id="39e8c-447">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="39e8c-448">**IrBus** (47) </span><span class="sxs-lookup"><span data-stu-id="39e8c-448">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="39e8c-449">**狀態**</span><span class="sxs-lookup"><span data-stu-id="39e8c-449">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e8c-450">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="39e8c-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-451">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39e8c-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-452">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="39e8c-452">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="39e8c-453">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="39e8c-453">Current status of the object.</span></span> <span data-ttu-id="39e8c-454">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="39e8c-454">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="39e8c-455">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="39e8c-455">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="39e8c-456">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="39e8c-456">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="39e8c-457">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="39e8c-457">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="39e8c-458">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="39e8c-458">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="39e8c-459">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="39e8c-459">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="39e8c-460">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="39e8c-460">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="39e8c-461">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="39e8c-461">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="39e8c-462">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="39e8c-462">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="39e8c-463">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="39e8c-463">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="39e8c-464">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="39e8c-464">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="39e8c-465">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="39e8c-465">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="39e8c-466">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="39e8c-466">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="39e8c-467">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="39e8c-467">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="39e8c-468">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="39e8c-468">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e8c-469">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="39e8c-469">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-470">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39e8c-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-471">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="39e8c-471">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="39e8c-472">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="39e8c-472">State of the logical device.</span></span> <span data-ttu-id="39e8c-473">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="39e8c-473">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="39e8c-474">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="39e8c-474">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="39e8c-475">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="39e8c-475">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="39e8c-476">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="39e8c-476">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="39e8c-477">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="39e8c-477">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="39e8c-478">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="39e8c-478">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="39e8c-479">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="39e8c-479">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="39e8c-480">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="39e8c-480">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e8c-481">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="39e8c-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-482">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39e8c-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-483">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="39e8c-483">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="39e8c-484">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="39e8c-484">Scoping system's creation class name.</span></span>

<span data-ttu-id="39e8c-485">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="39e8c-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="39e8c-486">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="39e8c-486">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e8c-487">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="39e8c-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-488">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39e8c-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-489">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="39e8c-489">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="39e8c-490">設定系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="39e8c-490">Scoping system's name.</span></span>

<span data-ttu-id="39e8c-491">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="39e8c-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="39e8c-492">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="39e8c-492">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e8c-493">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="39e8c-493">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="39e8c-494">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39e8c-494">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39e8c-495">上次重設控制器的日期和時間，表示控制器已關機或重新初始化。</span><span class="sxs-lookup"><span data-stu-id="39e8c-495">Date and time the controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="39e8c-496">這個屬性繼承自 [**CIM \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="39e8c-496">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39e8c-497">備註</span><span class="sxs-lookup"><span data-stu-id="39e8c-497">Remarks</span></span>

<span data-ttu-id="39e8c-498">**Cim \_ SerialController** 類別衍生自 [**cim \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="39e8c-498">The **CIM\_SerialController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="39e8c-499">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="39e8c-499">WMI does not implement this class.</span></span> <span data-ttu-id="39e8c-500">針對衍生自 **CIM \_ SERIALCONTROLLER** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="39e8c-500">For WMI classes derived from **CIM\_SerialController**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="39e8c-501">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="39e8c-501">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="39e8c-502">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="39e8c-502">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="39e8c-503">規格需求</span><span class="sxs-lookup"><span data-stu-id="39e8c-503">Requirements</span></span>



| <span data-ttu-id="39e8c-504">需求</span><span class="sxs-lookup"><span data-stu-id="39e8c-504">Requirement</span></span> | <span data-ttu-id="39e8c-505">值</span><span class="sxs-lookup"><span data-stu-id="39e8c-505">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39e8c-506">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="39e8c-506">Minimum supported client</span></span><br/> | <span data-ttu-id="39e8c-507">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39e8c-507">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="39e8c-508">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="39e8c-508">Minimum supported server</span></span><br/> | <span data-ttu-id="39e8c-509">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39e8c-509">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="39e8c-510">命名空間</span><span class="sxs-lookup"><span data-stu-id="39e8c-510">Namespace</span></span><br/>                | <span data-ttu-id="39e8c-511">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="39e8c-511">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="39e8c-512">MOF</span><span class="sxs-lookup"><span data-stu-id="39e8c-512">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39e8c-513"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="39e8c-513"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="39e8c-514">DLL</span><span class="sxs-lookup"><span data-stu-id="39e8c-514">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39e8c-515"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39e8c-515"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39e8c-516">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39e8c-516">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39e8c-517">**CIM \_ 控制器**</span><span class="sxs-lookup"><span data-stu-id="39e8c-517">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

