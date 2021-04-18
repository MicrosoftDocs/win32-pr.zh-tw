---
description: CIM \_ 處理器類別代表處理器邏輯裝置的功能和管理。
ms.assetid: 7af3208f-f1d5-4911-b6ab-46b54eec0b69
ms.tgt_platform: multiple
title: 'CIM_Processor 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Processor
- CIM_Processor.AddressWidth
- CIM_Processor.Availability
- CIM_Processor.Caption
- CIM_Processor.ConfigManagerErrorCode
- CIM_Processor.ConfigManagerUserConfig
- CIM_Processor.CreationClassName
- CIM_Processor.CurrentClockSpeed
- CIM_Processor.DataWidth
- CIM_Processor.Description
- CIM_Processor.DeviceID
- CIM_Processor.ErrorCleared
- CIM_Processor.ErrorDescription
- CIM_Processor.Family
- CIM_Processor.InstallDate
- CIM_Processor.LastErrorCode
- CIM_Processor.LoadPercentage
- CIM_Processor.MaxClockSpeed
- CIM_Processor.Name
- CIM_Processor.OtherFamilyDescription
- CIM_Processor.PNPDeviceID
- CIM_Processor.PowerManagementCapabilities
- CIM_Processor.PowerManagementSupported
- CIM_Processor.Role
- CIM_Processor.Status
- CIM_Processor.StatusInfo
- CIM_Processor.Stepping
- CIM_Processor.SystemCreationClassName
- CIM_Processor.SystemName
- CIM_Processor.UniqueId
- CIM_Processor.UpgradeMethod
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0120ce0327c21098b8c2950bd5dfa9a9fe2a709c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468085"
---
# <a name="cim_processor-class-cimwin32-wmi-providers"></a><span data-ttu-id="ca8c2-103">CIM_Processor 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-103">CIM_Processor class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="ca8c2-104">**CIM \_ 處理器** 類別代表處理器邏輯裝置的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-104">The **CIM\_Processor** class represents the capabilities and management of the processor logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ca8c2-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ca8c2-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ca8c2-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="ca8c2-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca8c2-109">語法</span><span class="sxs-lookup"><span data-stu-id="ca8c2-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C54B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Processor : CIM_LogicalDevice
{
  uint16   AddressWidth;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint32   CurrentClockSpeed;
  uint16   DataWidth;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   Family;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint16   LoadPercentage;
  uint32   MaxClockSpeed;
  string   Name;
  string   OtherFamilyDescription;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Role;
  string   Status;
  uint16   StatusInfo;
  string   Stepping;
  string   SystemCreationClassName;
  string   SystemName;
  string   UniqueId;
  uint16   UpgradeMethod;
};
```

## <a name="members"></a><span data-ttu-id="ca8c2-110">成員</span><span class="sxs-lookup"><span data-stu-id="ca8c2-110">Members</span></span>

<span data-ttu-id="ca8c2-111">**CIM \_ 處理器** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ca8c2-111">The **CIM\_Processor** class has these types of members:</span></span>

-   [<span data-ttu-id="ca8c2-112">方法</span><span class="sxs-lookup"><span data-stu-id="ca8c2-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="ca8c2-113">屬性</span><span class="sxs-lookup"><span data-stu-id="ca8c2-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ca8c2-114">方法</span><span class="sxs-lookup"><span data-stu-id="ca8c2-114">Methods</span></span>

<span data-ttu-id="ca8c2-115">**CIM \_ 處理器** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-115">The **CIM\_Processor** class has these methods.</span></span>



| <span data-ttu-id="ca8c2-116">方法</span><span class="sxs-lookup"><span data-stu-id="ca8c2-116">Method</span></span>                                                               | <span data-ttu-id="ca8c2-117">描述</span><span class="sxs-lookup"><span data-stu-id="ca8c2-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ca8c2-118">**重設**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-118">**Reset**</span></span>](reset-method-in-class-cim-processor.md)                 | <span data-ttu-id="ca8c2-119">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="ca8c2-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="ca8c2-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-processor.md) | <span data-ttu-id="ca8c2-122">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="ca8c2-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ca8c2-124">屬性</span><span class="sxs-lookup"><span data-stu-id="ca8c2-124">Properties</span></span>

<span data-ttu-id="ca8c2-125">**CIM \_ 處理器** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-125">The **CIM\_Processor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ca8c2-126">**AddressWidth**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-126">**AddressWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-127">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-129">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bits" ) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-129">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-130">處理器位址寬度（以位為單位）。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-130">Processor address width, in bits.</span></span>

</dd> <dt>

<span data-ttu-id="ca8c2-131">**可用性**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-131">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-132">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-134">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="ca8c2-134">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-135">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-135">Availability and status of the device.</span></span>

<span data-ttu-id="ca8c2-136">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-136">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ca8c2-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ca8c2-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="ca8c2-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-140">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="ca8c2-140">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="ca8c2-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="ca8c2-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ca8c2-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="ca8c2-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="ca8c2-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="ca8c2-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="ca8c2-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ca8c2-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="ca8c2-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="ca8c2-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="ca8c2-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-151">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-151">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="ca8c2-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-153">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-153">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="ca8c2-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-155">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-155">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="ca8c2-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="ca8c2-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-158">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-158">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="ca8c2-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-160">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-160">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="ca8c2-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-162">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-162">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="ca8c2-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-164">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-164">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="ca8c2-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-166">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-166">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ca8c2-167">**標題**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-167">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-170">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-171">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-171">Short textual description of the object.</span></span>

<span data-ttu-id="ca8c2-172">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca8c2-173">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-173">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-174">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-176">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-176">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-177">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-177">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="ca8c2-178">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-178">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="ca8c2-179"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-179"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="ca8c2-180"> (0)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-180">(0)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-181">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-181">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="ca8c2-182"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-182"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="ca8c2-183">(1)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-183">(1)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-184">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-184">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ca8c2-185"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-185"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="ca8c2-186">(2)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-186">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="ca8c2-187"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-187"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="ca8c2-188">(3)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-188">(3)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-189">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-189">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="ca8c2-190"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-190"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="ca8c2-191">(4)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-191">(4)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-192">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-192">Device is not working properly.</span></span> <span data-ttu-id="ca8c2-193">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-193">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="ca8c2-194"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-194"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="ca8c2-195">(5)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-195">(5)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-196">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-196">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="ca8c2-197"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-197"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="ca8c2-198">(6)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-198">(6)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-199">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-199">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="ca8c2-200"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-200"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="ca8c2-201">(7)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-201">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="ca8c2-202"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-202"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="ca8c2-203">(8)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-203">(8)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-204">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-204">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="ca8c2-205"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-205"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="ca8c2-206">(9)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-206">(9)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-207">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-207">Device is not working properly.</span></span> <span data-ttu-id="ca8c2-208">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-208">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="ca8c2-209"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-209"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="ca8c2-210">(10)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-210">(10)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-211">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-211">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="ca8c2-212"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-212"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="ca8c2-213">(11)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-213">(11)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-214">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-214">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="ca8c2-215"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-215"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="ca8c2-216"> (12) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-216">(12)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-217">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-217">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="ca8c2-218"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-218"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="ca8c2-219">(13)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-219">(13)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-220">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-220">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="ca8c2-221"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-221"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="ca8c2-222">(14)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-222">(14)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-223">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-223">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="ca8c2-224"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-224"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="ca8c2-225">(15)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-225">(15)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-226">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-226">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="ca8c2-227"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-227"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="ca8c2-228">(16)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-228">(16)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-229">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-229">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="ca8c2-230"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-230"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="ca8c2-231">(17)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-231">(17)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-232">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-232">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ca8c2-233"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-233"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="ca8c2-234">(18)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-234">(18)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-235">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-235">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="ca8c2-236"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-236"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="ca8c2-237">(19)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-237">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="ca8c2-238"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-238"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="ca8c2-239">(20)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-239">(20)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-240">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-240">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="ca8c2-241"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-241"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="ca8c2-242">(21)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-242">(21)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-243">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-243">System failure.</span></span> <span data-ttu-id="ca8c2-244">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-244">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="ca8c2-245">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-245">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="ca8c2-246"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-246"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="ca8c2-247">(22)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-247">(22)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-248">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-248">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="ca8c2-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="ca8c2-250">(23)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-250">(23)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-251">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-251">System failure.</span></span> <span data-ttu-id="ca8c2-252">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-252">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="ca8c2-253"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-253"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="ca8c2-254">(24)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-254">(24)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-255">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-255">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="ca8c2-256"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-256"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="ca8c2-257">(25)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-257">(25)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-258">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-258">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="ca8c2-259"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-259"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="ca8c2-260">(26)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-260">(26)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-261">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-261">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="ca8c2-262"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-262"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="ca8c2-263">(27)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-263">(27)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-264">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-264">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="ca8c2-265"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-265"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="ca8c2-266">(28)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-266">(28)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-267">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-267">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="ca8c2-268"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-268"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="ca8c2-269">(29)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-269">(29)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-270">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-270">Device is disabled.</span></span> <span data-ttu-id="ca8c2-271">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-271">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="ca8c2-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="ca8c2-273">(30)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-273">(30)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-274">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-274">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ca8c2-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="ca8c2-276"> (31) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-276">(31)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-277">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-277">Device is not working properly.</span></span> <span data-ttu-id="ca8c2-278">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-278">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ca8c2-279">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-279">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-280">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-280">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-281">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-282">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-282">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-283">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-283">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="ca8c2-284">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca8c2-285">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-285">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-286">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-287">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-288">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-288">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-289">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-289">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="ca8c2-290">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-290">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="ca8c2-291">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-291">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca8c2-292">**CurrentClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-292">**CurrentClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-293">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-293">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-294">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-295">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 處理器 \| 006.6 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" mhz ") </span><span class="sxs-lookup"><span data-stu-id="ca8c2-295">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|006.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-296">目前的速度 (以 mhz 的處理器) 。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-296">Current speed (in megahertz) of the processor.</span></span>

</dd> <dt>

<span data-ttu-id="ca8c2-297">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-297">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-298">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-298">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-299">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-300">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bits" ) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-300">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-301">處理器資料寬度（以位為單位）。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-301">Processor data width, in bits.</span></span>

</dd> <dt>

<span data-ttu-id="ca8c2-302">**說明**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-302">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-303">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-304">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-305">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-305">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-306">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-306">Textual description of the object.</span></span>

<span data-ttu-id="ca8c2-307">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-307">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca8c2-308">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-308">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-309">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-310">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-311">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-311">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-312">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-312">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="ca8c2-313">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca8c2-314">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-314">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-315">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-315">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-316">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-317">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-317">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="ca8c2-318">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca8c2-319">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-319">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-320">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-322">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-322">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="ca8c2-323">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca8c2-324">**系列**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-324">**Family**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-325">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-325">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-326">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-327">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 處理器 \| 014.3 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ 處理器**。**OtherFamilyDescription**") </span><span class="sxs-lookup"><span data-stu-id="ca8c2-327">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|014.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Processor**.**OtherFamilyDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-328">處理器系列類型。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-328">Processor family type.</span></span>

<span data-ttu-id="ca8c2-329">這個屬性繼承自 **CIM \_ 處理器**。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-329">This property is inherited from **CIM\_Processor**.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ca8c2-330"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-330"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ca8c2-331"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-331"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="8086"></span>

<span data-ttu-id="ca8c2-332"><span id="8086"></span>**8086** (3) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-332"><span id="8086"></span>**8086** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="80286"></span>

<span data-ttu-id="ca8c2-333"><span id="80286"></span>**80286** (4) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-333"><span id="80286"></span>**80286** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="80386"></span>

<span data-ttu-id="ca8c2-334"><span id="80386"></span>**80386** (5) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-334"><span id="80386"></span>**80386** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="80486"></span>

<span data-ttu-id="ca8c2-335"><span id="80486"></span>**80486** (6) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-335"><span id="80486"></span>**80486** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8087"></span>

<span data-ttu-id="ca8c2-336"><span id="8087"></span>**8087** (7) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-336"><span id="8087"></span>**8087** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="80287"></span>

<span data-ttu-id="ca8c2-337"><span id="80287"></span>**80287** (8) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-337"><span id="80287"></span>**80287** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="80387"></span>

<span data-ttu-id="ca8c2-338"><span id="80387"></span>**80387** (9) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-338"><span id="80387"></span>**80387** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="80487"></span>

<span data-ttu-id="ca8c2-339"><span id="80487"></span>**80487** (10) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-339"><span id="80487"></span>**80487** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__brand"></span><span id="pentium_r__brand"></span><span id="PENTIUM_R__BRAND"></span>

<span data-ttu-id="ca8c2-340"><span id="Pentium_R__brand"></span><span id="pentium_r__brand"></span><span id="PENTIUM_R__BRAND"></span>**Pentium (R) 品牌** (11) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-340"><span id="Pentium_R__brand"></span><span id="pentium_r__brand"></span><span id="PENTIUM_R__BRAND"></span>**Pentium(R) brand** (11)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-341">Pentium 品牌</span><span class="sxs-lookup"><span data-stu-id="ca8c2-341">Pentium brand</span></span>

</dd> <dt>

<span id="Pentium_R__Pro"></span><span id="pentium_r__pro"></span><span id="PENTIUM_R__PRO"></span>

<span data-ttu-id="ca8c2-342"><span id="Pentium_R__Pro"></span><span id="pentium_r__pro"></span><span id="PENTIUM_R__PRO"></span>**Pentium (R) Pro** (12) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-342"><span id="Pentium_R__Pro"></span><span id="pentium_r__pro"></span><span id="PENTIUM_R__PRO"></span>**Pentium(R) Pro** (12)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-343">Pentium Pro</span><span class="sxs-lookup"><span data-stu-id="ca8c2-343">Pentium Pro</span></span>

</dd> <dt>

<span id="Pentium_R__II"></span><span id="pentium_r__ii"></span><span id="PENTIUM_R__II"></span>

<span data-ttu-id="ca8c2-344"><span id="Pentium_R__II"></span><span id="pentium_r__ii"></span><span id="PENTIUM_R__II"></span>**Pentium (R) II** (13) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-344"><span id="Pentium_R__II"></span><span id="pentium_r__ii"></span><span id="PENTIUM_R__II"></span>**Pentium(R) II** (13)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-345">Pentium II</span><span class="sxs-lookup"><span data-stu-id="ca8c2-345">Pentium II</span></span>

</dd> <dt>

<span id="Pentium_R__processor_with_MMX_TM__technology"></span><span id="pentium_r__processor_with_mmx_tm__technology"></span><span id="PENTIUM_R__PROCESSOR_WITH_MMX_TM__TECHNOLOGY"></span>

<span data-ttu-id="ca8c2-346"><span id="Pentium_R__processor_with_MMX_TM__technology"></span><span id="pentium_r__processor_with_mmx_tm__technology"></span><span id="PENTIUM_R__PROCESSOR_WITH_MMX_TM__TECHNOLOGY"></span>**具有 MMX (TM) 技術的 Pentium (R) 處理器** (14) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-346"><span id="Pentium_R__processor_with_MMX_TM__technology"></span><span id="pentium_r__processor_with_mmx_tm__technology"></span><span id="PENTIUM_R__PROCESSOR_WITH_MMX_TM__TECHNOLOGY"></span>**Pentium(R) processor with MMX(TM) technology** (14)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-347">具有 MMX 技術的 Pentium 處理器</span><span class="sxs-lookup"><span data-stu-id="ca8c2-347">Pentium processor with MMX technology</span></span>

</dd> <dt>

<span id="Celeron_TM_"></span><span id="celeron_tm_"></span><span id="CELERON_TM_"></span>

<span data-ttu-id="ca8c2-348"><span id="Celeron_TM_"></span><span id="celeron_tm_"></span><span id="CELERON_TM_"></span>**賽揚 (TM)** (15) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-348"><span id="Celeron_TM_"></span><span id="celeron_tm_"></span><span id="CELERON_TM_"></span>**Celeron(TM)** (15)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-349">賽揚</span><span class="sxs-lookup"><span data-stu-id="ca8c2-349">Celeron</span></span>

</dd> <dt>

<span id="Pentium_R__II_Xeon_TM_"></span><span id="pentium_r__ii_xeon_tm_"></span><span id="PENTIUM_R__II_XEON_TM_"></span>

<span data-ttu-id="ca8c2-350"><span id="Pentium_R__II_Xeon_TM_"></span><span id="pentium_r_:xeon_tm_"></span><span id="PENTIUM_R__II_XEON_TM_"></span>**Pentium (R) II 強 (TM)** (16) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-350"><span id="Pentium_R__II_Xeon_TM_"></span><span id="pentium_r__ii_xeon_tm_"></span><span id="PENTIUM_R__II_XEON_TM_"></span>**Pentium(R) II Xeon(TM)** (16)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-351">Pentium II</span><span class="sxs-lookup"><span data-stu-id="ca8c2-351">Pentium II Xeon</span></span>

</dd> <dt>

<span id="Pentium_R__III"></span><span id="pentium_r__iii"></span><span id="PENTIUM_R__III"></span>

<span data-ttu-id="ca8c2-352"><span id="Pentium_R__III"></span><span id="pentium_r__iii"></span><span id="PENTIUM_R__III"></span>**Pentium (R) III** (17) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-352"><span id="Pentium_R__III"></span><span id="pentium_r__iii"></span><span id="PENTIUM_R__III"></span>**Pentium(R) III** (17)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-353">Pentium III</span><span class="sxs-lookup"><span data-stu-id="ca8c2-353">Pentium III</span></span>

</dd> <dt>

<span id="M1_Family"></span><span id="m1_family"></span><span id="M1_FAMILY"></span>

<span data-ttu-id="ca8c2-354"><span id="M1_Family"></span><span id="m1_family"></span><span id="M1_FAMILY"></span>**M1 系列** (18) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-354"><span id="M1_Family"></span><span id="m1_family"></span><span id="M1_FAMILY"></span>**M1 Family** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="M2_Family"></span><span id="m2_family"></span><span id="M2_FAMILY"></span>

<span data-ttu-id="ca8c2-355"><span id="M2_Family"></span><span id="m2_family"></span><span id="M2_FAMILY"></span>**M2 系列** (19) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-355"><span id="M2_Family"></span><span id="m2_family"></span><span id="M2_FAMILY"></span>**M2 Family** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="K5_Family"></span><span id="k5_family"></span><span id="K5_FAMILY"></span>

<span data-ttu-id="ca8c2-356"><span id="K5_Family"></span><span id="k5_family"></span><span id="K5_FAMILY"></span>**K5 系列** (24) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-356"><span id="K5_Family"></span><span id="k5_family"></span><span id="K5_FAMILY"></span>**K5 Family** (24)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-357">AMD Duron 處理器系列</span><span class="sxs-lookup"><span data-stu-id="ca8c2-357">AMD Duron  Processor Family</span></span>

</dd> <dt>

<span id="K6_Family"></span><span id="k6_family"></span><span id="K6_FAMILY"></span>

<span data-ttu-id="ca8c2-358"><span id="K6_Family"></span><span id="k6_family"></span><span id="K6_FAMILY"></span>**K6 系列** (25) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-358"><span id="K6_Family"></span><span id="k6_family"></span><span id="K6_FAMILY"></span>**K6 Family** (25)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-359">K5 系列</span><span class="sxs-lookup"><span data-stu-id="ca8c2-359">K5 Family</span></span>

</dd> <dt>

<span id="K6-2"></span><span id="k6-2"></span>

<span data-ttu-id="ca8c2-360"><span id="K6-2"></span><span id="k6-2"></span>**K6-2** (26) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-360"><span id="K6-2"></span><span id="k6-2"></span>**K6-2** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="K6-3"></span><span id="k6-3"></span>

<span data-ttu-id="ca8c2-361"><span id="K6-3"></span><span id="k6-3"></span>**K6-3** (27) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-361"><span id="K6-3"></span><span id="k6-3"></span>**K6-3** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__Processor_Family"></span><span id="amd_athlon_tm__processor_family"></span><span id="AMD_ATHLON_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="ca8c2-362"><span id="AMD_Athlon_TM__Processor_Family"></span><span id="amd_athlon_tm__processor_family"></span><span id="AMD_ATHLON_TM__PROCESSOR_FAMILY"></span>**AMD 速龍 (TM) 處理器系列** (28) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-362"><span id="AMD_Athlon_TM__Processor_Family"></span><span id="amd_athlon_tm__processor_family"></span><span id="AMD_ATHLON_TM__PROCESSOR_FAMILY"></span>**AMD Athlon(TM) Processor Family** (28)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-363">AMD 速龍處理器系列</span><span class="sxs-lookup"><span data-stu-id="ca8c2-363">AMD Athlon Processor Family</span></span>

</dd> <dt>

<span id="AMD_R__Duron_TM__Processor"></span><span id="amd_r__duron_tm__processor"></span><span id="AMD_R__DURON_TM__PROCESSOR"></span>

<span data-ttu-id="ca8c2-364"><span id="AMD_R__Duron_TM__Processor"></span><span id="amd_r__duron_tm__processor"></span><span id="AMD_R__DURON_TM__PROCESSOR"></span>**AMD (R) Duron (TM) 處理器** (29) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-364"><span id="AMD_R__Duron_TM__Processor"></span><span id="amd_r__duron_tm__processor"></span><span id="AMD_R__DURON_TM__PROCESSOR"></span>**AMD(R) Duron(TM) Processor** (29)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-365">AMD Duron 處理器</span><span class="sxs-lookup"><span data-stu-id="ca8c2-365">AMD  Duron Processor</span></span>

</dd> <dt>

<span id="AMD29000_Family"></span><span id="amd29000_family"></span><span id="AMD29000_FAMILY"></span>

<span data-ttu-id="ca8c2-366"><span id="AMD29000_Family"></span><span id="amd29000_family"></span><span id="AMD29000_FAMILY"></span>**AMD29000 系列** (30) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-366"><span id="AMD29000_Family"></span><span id="amd29000_family"></span><span id="AMD29000_FAMILY"></span>**AMD29000 Family** (30)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-367">AMD2900 系列</span><span class="sxs-lookup"><span data-stu-id="ca8c2-367">AMD2900 Family</span></span>

</dd> <dt>

<span id="K6-2_"></span><span id="k6-2_"></span>

<span data-ttu-id="ca8c2-368"><span id="K6-2_"></span><span id="k6-2_"></span>**K6-2 +** (31) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-368"><span id="K6-2_"></span><span id="k6-2_"></span>**K6-2+** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_Family"></span><span id="power_pc_family"></span><span id="POWER_PC_FAMILY"></span>

<span data-ttu-id="ca8c2-369"><span id="Power_PC_Family"></span><span id="power_pc_family"></span><span id="POWER_PC_FAMILY"></span>**POWER PC 系列** (32) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-369"><span id="Power_PC_Family"></span><span id="power_pc_family"></span><span id="POWER_PC_FAMILY"></span>**Power PC Family** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_601"></span><span id="power_pc_601"></span><span id="POWER_PC_601"></span>

<span data-ttu-id="ca8c2-370"><span id="Power_PC_601"></span><span id="power_pc_601"></span><span id="POWER_PC_601"></span>**POWER PC 601** (33) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-370"><span id="Power_PC_601"></span><span id="power_pc_601"></span><span id="POWER_PC_601"></span>**Power PC 601** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_603"></span><span id="power_pc_603"></span><span id="POWER_PC_603"></span>

<span data-ttu-id="ca8c2-371"><span id="Power_PC_603"></span><span id="power_pc_603"></span><span id="POWER_PC_603"></span>**POWER PC 603** (34) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-371"><span id="Power_PC_603"></span><span id="power_pc_603"></span><span id="POWER_PC_603"></span>**Power PC 603** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_603_"></span><span id="power_pc_603_"></span><span id="POWER_PC_603_"></span>

<span data-ttu-id="ca8c2-372"><span id="Power_PC_603_"></span><span id="power_pc_603_"></span><span id="POWER_PC_603_"></span>**POWER PC 603 +** (35) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-372"><span id="Power_PC_603_"></span><span id="power_pc_603_"></span><span id="POWER_PC_603_"></span>**Power PC 603+** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_604"></span><span id="power_pc_604"></span><span id="POWER_PC_604"></span>

<span data-ttu-id="ca8c2-373"><span id="Power_PC_604"></span><span id="power_pc_604"></span><span id="POWER_PC_604"></span>**POWER PC 604** (36) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-373"><span id="Power_PC_604"></span><span id="power_pc_604"></span><span id="POWER_PC_604"></span>**Power PC 604** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_620"></span><span id="power_pc_620"></span><span id="POWER_PC_620"></span>

<span data-ttu-id="ca8c2-374"><span id="Power_PC_620"></span><span id="power_pc_620"></span><span id="POWER_PC_620"></span>**POWER PC 620** (37) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-374"><span id="Power_PC_620"></span><span id="power_pc_620"></span><span id="POWER_PC_620"></span>**Power PC 620** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_X704"></span><span id="power_pc_x704"></span><span id="POWER_PC_X704"></span>

<span data-ttu-id="ca8c2-375"><span id="Power_PC_X704"></span><span id="power_pc_x704"></span><span id="POWER_PC_X704"></span>**POWER PC X704** (38) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-375"><span id="Power_PC_X704"></span><span id="power_pc_x704"></span><span id="POWER_PC_X704"></span>**Power PC X704** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_750"></span><span id="power_pc_750"></span><span id="POWER_PC_750"></span>

<span data-ttu-id="ca8c2-376"><span id="Power_PC_750"></span><span id="power_pc_750"></span><span id="POWER_PC_750"></span>**POWER PC 750** (39) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-376"><span id="Power_PC_750"></span><span id="power_pc_750"></span><span id="POWER_PC_750"></span>**Power PC 750** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_Family"></span><span id="alpha_family"></span><span id="ALPHA_FAMILY"></span>

<span data-ttu-id="ca8c2-377"><span id="Alpha_Family"></span><span id="alpha_family"></span><span id="ALPHA_FAMILY"></span>**Alpha 系列** (48) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-377"><span id="Alpha_Family"></span><span id="alpha_family"></span><span id="ALPHA_FAMILY"></span>**Alpha Family** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21064"></span><span id="alpha_21064"></span><span id="ALPHA_21064"></span>

<span data-ttu-id="ca8c2-378"><span id="Alpha_21064"></span><span id="alpha_21064"></span><span id="ALPHA_21064"></span>**Alpha 21064** (49) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-378"><span id="Alpha_21064"></span><span id="alpha_21064"></span><span id="ALPHA_21064"></span>**Alpha 21064** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21066"></span><span id="alpha_21066"></span><span id="ALPHA_21066"></span>

<span data-ttu-id="ca8c2-379"><span id="Alpha_21066"></span><span id="alpha_21066"></span><span id="ALPHA_21066"></span>**Alpha 21066** (50) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-379"><span id="Alpha_21066"></span><span id="alpha_21066"></span><span id="ALPHA_21066"></span>**Alpha 21066** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21164"></span><span id="alpha_21164"></span><span id="ALPHA_21164"></span>

<span data-ttu-id="ca8c2-380"><span id="Alpha_21164"></span><span id="alpha_21164"></span><span id="ALPHA_21164"></span>**Alpha 21164** (51) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-380"><span id="Alpha_21164"></span><span id="alpha_21164"></span><span id="ALPHA_21164"></span>**Alpha 21164** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21164PC"></span><span id="alpha_21164pc"></span><span id="ALPHA_21164PC"></span>

<span data-ttu-id="ca8c2-381"><span id="Alpha_21164PC"></span><span id="alpha_21164pc"></span><span id="ALPHA_21164PC"></span>**ALPHA 21164PC** (52) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-381"><span id="Alpha_21164PC"></span><span id="alpha_21164pc"></span><span id="ALPHA_21164PC"></span>**Alpha 21164PC** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21164a"></span><span id="alpha_21164a"></span><span id="ALPHA_21164A"></span>

<span data-ttu-id="ca8c2-382"><span id="Alpha_21164a"></span><span id="alpha_21164a"></span><span id="ALPHA_21164A"></span>**Alpha 21164a** (53) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-382"><span id="Alpha_21164a"></span><span id="alpha_21164a"></span><span id="ALPHA_21164A"></span>**Alpha 21164a** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21264"></span><span id="alpha_21264"></span><span id="ALPHA_21264"></span>

<span data-ttu-id="ca8c2-383"><span id="Alpha_21264"></span><span id="alpha_21264"></span><span id="ALPHA_21264"></span>**Alpha 21264** (54) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-383"><span id="Alpha_21264"></span><span id="alpha_21264"></span><span id="ALPHA_21264"></span>**Alpha 21264** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21364"></span><span id="alpha_21364"></span><span id="ALPHA_21364"></span>

<span data-ttu-id="ca8c2-384"><span id="Alpha_21364"></span><span id="alpha_21364"></span><span id="ALPHA_21364"></span>**Alpha 21364** (55) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-384"><span id="Alpha_21364"></span><span id="alpha_21364"></span><span id="ALPHA_21364"></span>**Alpha 21364** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_Family"></span><span id="mips_family"></span><span id="MIPS_FAMILY"></span>

<span data-ttu-id="ca8c2-385"><span id="MIPS_Family"></span><span id="mips_family"></span><span id="MIPS_FAMILY"></span>**MIPS 系列** (64) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-385"><span id="MIPS_Family"></span><span id="mips_family"></span><span id="MIPS_FAMILY"></span>**MIPS Family** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4000"></span><span id="mips_r4000"></span>

<span data-ttu-id="ca8c2-386"><span id="MIPS_R4000"></span><span id="mips_r4000"></span>**MIPS R4000** (65) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-386"><span id="MIPS_R4000"></span><span id="mips_r4000"></span>**MIPS R4000** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4200"></span><span id="mips_r4200"></span>

<span data-ttu-id="ca8c2-387"><span id="MIPS_R4200"></span><span id="mips_r4200"></span>**MIPS R4200** (66) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-387"><span id="MIPS_R4200"></span><span id="mips_r4200"></span>**MIPS R4200** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4400"></span><span id="mips_r4400"></span>

<span data-ttu-id="ca8c2-388"><span id="MIPS_R4400"></span><span id="mips_r4400"></span>**MIPS R4400** (67) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-388"><span id="MIPS_R4400"></span><span id="mips_r4400"></span>**MIPS R4400** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4600"></span><span id="mips_r4600"></span>

<span data-ttu-id="ca8c2-389"><span id="MIPS_R4600"></span><span id="mips_r4600"></span>**MIPS R4600** (68) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-389"><span id="MIPS_R4600"></span><span id="mips_r4600"></span>**MIPS R4600** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R10000"></span><span id="mips_r10000"></span>

<span data-ttu-id="ca8c2-390"><span id="MIPS_R10000"></span><span id="mips_r10000"></span>**MIPS R10000** (69) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-390"><span id="MIPS_R10000"></span><span id="mips_r10000"></span>**MIPS R10000** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="SPARC_Family"></span><span id="sparc_family"></span><span id="SPARC_FAMILY"></span>

<span data-ttu-id="ca8c2-391"><span id="SPARC_Family"></span><span id="sparc_family"></span><span id="SPARC_FAMILY"></span>**SPARC 系列** (80) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-391"><span id="SPARC_Family"></span><span id="sparc_family"></span><span id="SPARC_FAMILY"></span>**SPARC Family** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="SuperSPARC"></span><span id="supersparc"></span><span id="SUPERSPARC"></span>

<span data-ttu-id="ca8c2-392"><span id="SuperSPARC"></span><span id="supersparc"></span><span id="SUPERSPARC"></span>**SuperSPARC** (81) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-392"><span id="SuperSPARC"></span><span id="supersparc"></span><span id="SUPERSPARC"></span>**SuperSPARC** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="microSPARC_II"></span><span id="microsparc_ii"></span><span id="MICROSPARC_II"></span>

<span data-ttu-id="ca8c2-393"><span id="microSPARC_II"></span><span id="microsparc_ii"></span><span id="MICROSPARC_II"></span>**MICROSPARC II** (82) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-393"><span id="microSPARC_II"></span><span id="microsparc_ii"></span><span id="MICROSPARC_II"></span>**microSPARC II** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="microSPARC_IIep"></span><span id="microsparc_iiep"></span><span id="MICROSPARC_IIEP"></span>

<span data-ttu-id="ca8c2-394"><span id="microSPARC_IIep"></span><span id="microsparc_iiep"></span><span id="MICROSPARC_IIEP"></span>**MicroSPARC IIep** (83) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-394"><span id="microSPARC_IIep"></span><span id="microsparc_iiep"></span><span id="MICROSPARC_IIEP"></span>**microSPARC IIep** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC"></span><span id="ultrasparc"></span><span id="ULTRASPARC"></span>

<span data-ttu-id="ca8c2-395"><span id="UltraSPARC"></span><span id="ultrasparc"></span><span id="ULTRASPARC"></span>**UltraSPARC** (84) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-395"><span id="UltraSPARC"></span><span id="ultrasparc"></span><span id="ULTRASPARC"></span>**UltraSPARC** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_II"></span><span id="ultrasparc_ii"></span><span id="ULTRASPARC_II"></span>

<span data-ttu-id="ca8c2-396"><span id="UltraSPARC_II"></span><span id="ultrasparc_ii"></span><span id="ULTRASPARC_II"></span>**ULTRASPARC II** (85) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-396"><span id="UltraSPARC_II"></span><span id="ultrasparc_ii"></span><span id="ULTRASPARC_II"></span>**UltraSPARC II** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_IIi"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>

<span data-ttu-id="ca8c2-397"><span id="UltraSPARC_IIi"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>**UltraSPARC IIi** (86) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-397"><span id="UltraSPARC_IIi"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>**UltraSPARC IIi** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_III"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>

<span data-ttu-id="ca8c2-398"><span id="UltraSPARC_III"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>**ULTRASPARC III** (87) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-398"><span id="UltraSPARC_III"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>**UltraSPARC III** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_IIIi"></span><span id="ultrasparc_iiii"></span><span id="ULTRASPARC_IIII"></span>

<span data-ttu-id="ca8c2-399"><span id="UltraSPARC_IIIi"></span><span id="ultrasparc_iiii"></span><span id="ULTRASPARC_IIII"></span>**UltraSPARC IIIi** (88) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-399"><span id="UltraSPARC_IIIi"></span><span id="ultrasparc_iiii"></span><span id="ULTRASPARC_IIII"></span>**UltraSPARC IIIi** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="68040"></span>

<span data-ttu-id="ca8c2-400"><span id="68040"></span>**68040** (96) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-400"><span id="68040"></span>**68040** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="68xxx_Family"></span><span id="68xxx_family"></span><span id="68XXX_FAMILY"></span>

<span data-ttu-id="ca8c2-401"><span id="68xxx_Family"></span><span id="68xxx_family"></span><span id="68XXX_FAMILY"></span>**68Xxx 系列** (97) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-401"><span id="68xxx_Family"></span><span id="68xxx_family"></span><span id="68XXX_FAMILY"></span>**68xxx Family** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="68000"></span>

<span data-ttu-id="ca8c2-402"><span id="68000"></span>**68000** (98) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-402"><span id="68000"></span>**68000** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="68010"></span>

<span data-ttu-id="ca8c2-403"><span id="68010"></span>**68010** (99) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-403"><span id="68010"></span>**68010** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="68020"></span>

<span data-ttu-id="ca8c2-404"><span id="68020"></span>**68020** (100) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-404"><span id="68020"></span>**68020** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="68030"></span>

<span data-ttu-id="ca8c2-405"><span id="68030"></span>**68030** (101) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-405"><span id="68030"></span>**68030** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Hobbit_Family"></span><span id="hobbit_family"></span><span id="HOBBIT_FAMILY"></span>

<span data-ttu-id="ca8c2-406"><span id="Hobbit_Family"></span><span id="hobbit_family"></span><span id="HOBBIT_FAMILY"></span>**Hobbit 系列** (112) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-406"><span id="Hobbit_Family"></span><span id="hobbit_family"></span><span id="HOBBIT_FAMILY"></span>**Hobbit Family** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Crusoe_TM__TM5000_Family"></span><span id="crusoe_tm__tm5000_family"></span><span id="CRUSOE_TM__TM5000_FAMILY"></span>

<span data-ttu-id="ca8c2-407"><span id="Crusoe_TM__TM5000_Family"></span><span id="crusoe_tm__tm5000_family"></span><span id="CRUSOE_TM__TM5000_FAMILY"></span>**Crusoe (TM) TM5000 系列** (120) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-407"><span id="Crusoe_TM__TM5000_Family"></span><span id="crusoe_tm__tm5000_family"></span><span id="CRUSOE_TM__TM5000_FAMILY"></span>**Crusoe(TM) TM5000 Family** (120)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-408">Crusoe TM5000 系列</span><span class="sxs-lookup"><span data-stu-id="ca8c2-408">Crusoe TM5000 Family</span></span>

</dd> <dt>

<span id="Crusoe_TM__TM3000_Family"></span><span id="crusoe_tm__tm3000_family"></span><span id="CRUSOE_TM__TM3000_FAMILY"></span>

<span data-ttu-id="ca8c2-409"><span id="Crusoe_TM__TM3000_Family"></span><span id="crusoe_tm__tm3000_family"></span><span id="CRUSOE_TM__TM3000_FAMILY"></span>**Crusoe (TM) TM3000 系列** (121) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-409"><span id="Crusoe_TM__TM3000_Family"></span><span id="crusoe_tm__tm3000_family"></span><span id="CRUSOE_TM__TM3000_FAMILY"></span>**Crusoe(TM) TM3000 Family** (121)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-410">Crusoe TM3000 系列</span><span class="sxs-lookup"><span data-stu-id="ca8c2-410">Crusoe TM3000 Family</span></span>

</dd> <dt>

<span id="Efficeon_TM__TM8000_Family"></span><span id="efficeon_tm__tm8000_family"></span><span id="EFFICEON_TM__TM8000_FAMILY"></span>

<span data-ttu-id="ca8c2-411"><span id="Efficeon_TM__TM8000_Family"></span><span id="efficeon_tm__tm8000_family"></span><span id="EFFICEON_TM__TM8000_FAMILY"></span>**Efficeon (TM) TM8000 系列** (122) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-411"><span id="Efficeon_TM__TM8000_Family"></span><span id="efficeon_tm__tm8000_family"></span><span id="EFFICEON_TM__TM8000_FAMILY"></span>**Efficeon(TM) TM8000 Family** (122)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-412">Efficeon8000 系列</span><span class="sxs-lookup"><span data-stu-id="ca8c2-412">Efficeon8000 Family</span></span>

</dd> <dt>

<span id="Weitek"></span><span id="weitek"></span><span id="WEITEK"></span>

<span data-ttu-id="ca8c2-413"><span id="Weitek"></span><span id="weitek"></span><span id="WEITEK"></span>**Weitek** (128) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-413"><span id="Weitek"></span><span id="weitek"></span><span id="WEITEK"></span>**Weitek** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="Itanium_TM__Processor"></span><span id="itanium_tm__processor"></span><span id="ITANIUM_TM__PROCESSOR"></span>

<span data-ttu-id="ca8c2-414"><span id="Itanium_TM__Processor"></span><span id="itanium_tm__processor"></span><span id="ITANIUM_TM__PROCESSOR"></span>**Itanium (TM) 處理器** (130) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-414"><span id="Itanium_TM__Processor"></span><span id="itanium_tm__processor"></span><span id="ITANIUM_TM__PROCESSOR"></span>**Itanium(TM) Processor** (130)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-415">Itanium 處理器</span><span class="sxs-lookup"><span data-stu-id="ca8c2-415">Itanium  Processor</span></span>

</dd> <dt>

<span id="AMD_Athlon_TM__64_Processor_Family"></span><span id="amd_athlon_tm__64_processor_family"></span><span id="AMD_ATHLON_TM__64_PROCESSOR_FAMILY"></span>

<span data-ttu-id="ca8c2-416"><span id="AMD_Athlon_TM__64_Processor_Family"></span><span id="amd_athlon_tm__64_processor_family"></span><span id="AMD_ATHLON_TM__64_PROCESSOR_FAMILY"></span>**AMD 速龍 (TM) 64 處理器系列** (131) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-416"><span id="AMD_Athlon_TM__64_Processor_Family"></span><span id="amd_athlon_tm__64_processor_family"></span><span id="AMD_ATHLON_TM__64_PROCESSOR_FAMILY"></span>**AMD Athlon(TM) 64 Processor Family** (131)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-417">AMD 速龍</span><span class="sxs-lookup"><span data-stu-id="ca8c2-417">AMD Athlon</span></span> 

</dd> <dt>

<span id="AMD_Opteron_TM__Family"></span><span id="amd_opteron_tm__family"></span><span id="AMD_OPTERON_TM__FAMILY"></span>

<span data-ttu-id="ca8c2-418"><span id="AMD_Opteron_TM__Family"></span><span id="amd_opteron_tm__family"></span><span id="AMD_OPTERON_TM__FAMILY"></span>**AMD 皓龍 (TM) 系列** (132) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-418"><span id="AMD_Opteron_TM__Family"></span><span id="amd_opteron_tm__family"></span><span id="AMD_OPTERON_TM__FAMILY"></span>**AMD Opteron(TM) Family** (132)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-419">AMD 皓龍系列</span><span class="sxs-lookup"><span data-stu-id="ca8c2-419">AMD Opteron  Family</span></span>

</dd> <dt>

<span id="PA-RISC_Family"></span><span id="pa-risc_family"></span><span id="PA-RISC_FAMILY"></span>

<span data-ttu-id="ca8c2-420"><span id="PA-RISC_Family"></span><span id="pa-risc_family"></span><span id="PA-RISC_FAMILY"></span>**PA-RISC 系列** (144) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-420"><span id="PA-RISC_Family"></span><span id="pa-risc_family"></span><span id="PA-RISC_FAMILY"></span>**PA-RISC Family** (144)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_8500"></span><span id="pa-risc_8500"></span>

<span data-ttu-id="ca8c2-421"><span id="PA-RISC_8500"></span><span id="pa-risc_8500"></span>**PA-RISC 8500** (145) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-421"><span id="PA-RISC_8500"></span><span id="pa-risc_8500"></span>**PA-RISC 8500** (145)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_8000"></span><span id="pa-risc_8000"></span>

<span data-ttu-id="ca8c2-422"><span id="PA-RISC_8000"></span><span id="pa-risc_8000"></span>**PA-RISC 8000** (146) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-422"><span id="PA-RISC_8000"></span><span id="pa-risc_8000"></span>**PA-RISC 8000** (146)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7300LC"></span><span id="pa-risc_7300lc"></span>

<span data-ttu-id="ca8c2-423"><span id="PA-RISC_7300LC"></span><span id="pa-risc_7300lc"></span>**PA-RISC 7300LC** (147) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-423"><span id="PA-RISC_7300LC"></span><span id="pa-risc_7300lc"></span>**PA-RISC 7300LC** (147)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7200"></span><span id="pa-risc_7200"></span>

<span data-ttu-id="ca8c2-424"><span id="PA-RISC_7200"></span><span id="pa-risc_7200"></span>**PA-RISC 7200** (148) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-424"><span id="PA-RISC_7200"></span><span id="pa-risc_7200"></span>**PA-RISC 7200** (148)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7100LC"></span><span id="pa-risc_7100lc"></span>

<span data-ttu-id="ca8c2-425"><span id="PA-RISC_7100LC"></span><span id="pa-risc_7100lc"></span>**PA-RISC 7100LC** (149) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-425"><span id="PA-RISC_7100LC"></span><span id="pa-risc_7100lc"></span>**PA-RISC 7100LC** (149)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7100"></span><span id="pa-risc_7100"></span>

<span data-ttu-id="ca8c2-426"><span id="PA-RISC_7100"></span><span id="pa-risc_7100"></span>**PA-RISC 7100** (150) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-426"><span id="PA-RISC_7100"></span><span id="pa-risc_7100"></span>**PA-RISC 7100** (150)</span></span>


</dt> <dd></dd> <dt>

<span id="V30_Family"></span><span id="v30_family"></span><span id="V30_FAMILY"></span>

<span data-ttu-id="ca8c2-427"><span id="V30_Family"></span><span id="v30_family"></span><span id="V30_FAMILY"></span>**V30 系列** (160) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-427"><span id="V30_Family"></span><span id="v30_family"></span><span id="V30_FAMILY"></span>**V30 Family** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__III_Xeon_TM_"></span><span id="pentium_r__iii_xeon_tm_"></span><span id="PENTIUM_R__III_XEON_TM_"></span>

<span data-ttu-id="ca8c2-428"><span id="Pentium_R__III_Xeon_TM_"></span><span id="pentium_r__iii_xeon_tm_"></span><span id="PENTIUM_R__III_XEON_TM_"></span>**Pentium (R) III 強 (TM)** (176) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-428"><span id="Pentium_R__III_Xeon_TM_"></span><span id="pentium_r__iii_xeon_tm_"></span><span id="PENTIUM_R__III_XEON_TM_"></span>**Pentium(R) III Xeon(TM)** (176)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-429">Pentium III</span><span class="sxs-lookup"><span data-stu-id="ca8c2-429">Pentium III Xeon</span></span>

</dd> <dt>

<span id="Pentium_R__III_Processor_with_Intel_R__SpeedStep_TM__Technology"></span><span id="pentium_r__iii_processor_with_intel_r__speedstep_tm__technology"></span><span id="PENTIUM_R__III_PROCESSOR_WITH_INTEL_R__SPEEDSTEP_TM__TECHNOLOGY"></span>

<span data-ttu-id="ca8c2-430"><span id="Pentium_R__III_Processor_with_Intel_R__SpeedStep_TM__Technology"></span><span id="pentium_r__iii_processor_with_intel_r__speedstep_tm__technology"></span><span id="PENTIUM_R__III_PROCESSOR_WITH_INTEL_R__SPEEDSTEP_TM__TECHNOLOGY"></span>**Pentium (r) III 處理器搭配 Intel (R) SpeedStep (TM) 技術** (177) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-430"><span id="Pentium_R__III_Processor_with_Intel_R__SpeedStep_TM__Technology"></span><span id="pentium_r__iii_processor_with_intel_r__speedstep_tm__technology"></span><span id="PENTIUM_R__III_PROCESSOR_WITH_INTEL_R__SPEEDSTEP_TM__TECHNOLOGY"></span>**Pentium(R) III Processor with Intel(R) SpeedStep(TM) Technology** (177)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-431">具有 Intel SpeedStep 技術的 Pentium III 處理器</span><span class="sxs-lookup"><span data-stu-id="ca8c2-431">Pentium III Processor with Intel SpeedStep Technology</span></span>

</dd> <dt>

<span id="Pentium_R__4"></span><span id="pentium_r__4"></span><span id="PENTIUM_R__4"></span>

<span data-ttu-id="ca8c2-432"><span id="Pentium_R__4"></span><span id="pentium_r__4"></span><span id="PENTIUM_R__4"></span>**Pentium (R) 4** (178) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-432"><span id="Pentium_R__4"></span><span id="pentium_r__4"></span><span id="PENTIUM_R__4"></span>**Pentium(R) 4** (178)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-433">Pentium 4</span><span class="sxs-lookup"><span data-stu-id="ca8c2-433">Pentium 4</span></span>

</dd> <dt>

<span id="Intel_R__Xeon_TM_"></span><span id="intel_r__xeon_tm_"></span><span id="INTEL_R__XEON_TM_"></span>

<span data-ttu-id="ca8c2-434"><span id="Intel_R__Xeon_TM_"></span><span id="intel_r__xeon_tm_"></span><span id="INTEL_R__XEON_TM_"></span>**Intel (R) )  (TM** (179) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-434"><span id="Intel_R__Xeon_TM_"></span><span id="intel_r__xeon_tm_"></span><span id="INTEL_R__XEON_TM_"></span>**Intel(R) Xeon(TM)** (179)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-435">Intel （r）</span><span class="sxs-lookup"><span data-stu-id="ca8c2-435">Intel Xeon</span></span>

</dd> <dt>

<span id="AS400_Family"></span><span id="as400_family"></span><span id="AS400_FAMILY"></span>

<span data-ttu-id="ca8c2-436"><span id="AS400_Family"></span><span id="as400_family"></span><span id="AS400_FAMILY"></span>**AS400 系列** (180) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-436"><span id="AS400_Family"></span><span id="as400_family"></span><span id="AS400_FAMILY"></span>**AS400 Family** (180)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Xeon_TM__processor_MP"></span><span id="intel_r__xeon_tm__processor_mp"></span><span id="INTEL_R__XEON_TM__PROCESSOR_MP"></span>

<span data-ttu-id="ca8c2-437"><span id="Intel_R__Xeon_TM__processor_MP"></span><span id="intel_r__xeon_tm__processor_mp"></span><span id="INTEL_R__XEON_TM__PROCESSOR_MP"></span>**Intel (R) )  (TM 處理器 MP** (181) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-437"><span id="Intel_R__Xeon_TM__processor_MP"></span><span id="intel_r__xeon_tm__processor_mp"></span><span id="INTEL_R__XEON_TM__PROCESSOR_MP"></span>**Intel(R) Xeon(TM) processor MP** (181)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-438">Intel 以上處理器 MP</span><span class="sxs-lookup"><span data-stu-id="ca8c2-438">Intel Xeon Processor MP</span></span>

</dd> <dt>

<span id="AMD_AthlonXP_TM__Family"></span><span id="amd_athlonxp_tm__family"></span><span id="AMD_ATHLONXP_TM__FAMILY"></span>

<span data-ttu-id="ca8c2-439"><span id="AMD_AthlonXP_TM__Family"></span><span id="amd_athlonxp_tm__family"></span><span id="AMD_ATHLONXP_TM__FAMILY"></span>**AMD AthlonXP (TM) 系列** (182) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-439"><span id="AMD_AthlonXP_TM__Family"></span><span id="amd_athlonxp_tm__family"></span><span id="AMD_ATHLONXP_TM__FAMILY"></span>**AMD AthlonXP(TM) Family** (182)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-440">AMD AthlonXP 系列</span><span class="sxs-lookup"><span data-stu-id="ca8c2-440">AMD AthlonXP Family</span></span>

</dd> <dt>

<span id="AMD_AthlonMP_TM__Family"></span><span id="amd_athlonmp_tm__family"></span><span id="AMD_ATHLONMP_TM__FAMILY"></span>

<span data-ttu-id="ca8c2-441"><span id="AMD_AthlonMP_TM__Family"></span><span id="amd_athlonmp_tm__family"></span><span id="AMD_ATHLONMP_TM__FAMILY"></span>**AMD AthlonMP (TM) 系列** (183) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-441"><span id="AMD_AthlonMP_TM__Family"></span><span id="amd_athlonmp_tm__family"></span><span id="AMD_ATHLONMP_TM__FAMILY"></span>**AMD AthlonMP(TM) Family** (183)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-442">AMD AthlonMP 系列</span><span class="sxs-lookup"><span data-stu-id="ca8c2-442">AMD AthlonMP Family</span></span>

</dd> <dt>

<span id="Intel_R__Itanium_R__2"></span><span id="intel_r__itanium_r__2"></span><span id="INTEL_R__ITANIUM_R__2"></span>

<span data-ttu-id="ca8c2-443"><span id="Intel_R__Itanium_R__2"></span><span id="intel_r__itanium_r__2"></span><span id="INTEL_R__ITANIUM_R__2"></span>**Intel (R) Itanium (r) 2** (184) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-443"><span id="Intel_R__Itanium_R__2"></span><span id="intel_r__itanium_r__2"></span><span id="INTEL_R__ITANIUM_R__2"></span>**Intel(R) Itanium(R) 2** (184)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-444">Intel Itanium 2</span><span class="sxs-lookup"><span data-stu-id="ca8c2-444">Intel Itanium 2</span></span>

</dd> <dt>

<span id="Intel_Pentium_M_Processor"></span><span id="intel_pentium_m_processor"></span><span id="INTEL_PENTIUM_M_PROCESSOR"></span>

<span data-ttu-id="ca8c2-445"><span id="Intel_Pentium_M_Processor"></span><span id="intel_pentium_m_processor"></span><span id="INTEL_PENTIUM_M_PROCESSOR"></span>**Intel Pentium M 處理器** (185) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-445"><span id="Intel_Pentium_M_Processor"></span><span id="intel_pentium_m_processor"></span><span id="INTEL_PENTIUM_M_PROCESSOR"></span>**Intel Pentium M Processor** (185)</span></span>


</dt> <dd></dd> <dt>

<span id="K7"></span><span id="k7"></span>

<span data-ttu-id="ca8c2-446"><span id="K7"></span><span id="k7"></span>**K7** (190) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-446"><span id="K7"></span><span id="k7"></span>**K7** (190)</span></span>


</dt> <dd></dd> <dt>

<span id="IBM390_Family"></span><span id="ibm390_family"></span><span id="IBM390_FAMILY"></span>

<span data-ttu-id="ca8c2-447"><span id="IBM390_Family"></span><span id="ibm390_family"></span><span id="IBM390_FAMILY"></span>**IBM390 系列** (200) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-447"><span id="IBM390_Family"></span><span id="ibm390_family"></span><span id="IBM390_FAMILY"></span>**IBM390 Family** (200)</span></span>


</dt> <dd></dd> <dt>

<span id="G4"></span><span id="g4"></span>

<span data-ttu-id="ca8c2-448"><span id="G4"></span><span id="g4"></span>4 **代 (201**) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-448"><span id="G4"></span><span id="g4"></span>**G4** (201)</span></span>


</dt> <dd></dd> <dt>

<span id="G5"></span><span id="g5"></span>

<span data-ttu-id="ca8c2-449"><span id="G5"></span><span id="g5"></span>**G5** (202) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-449"><span id="G5"></span><span id="g5"></span>**G5** (202)</span></span>


</dt> <dd></dd> <dt>

<span id="G6"></span><span id="g6"></span>

<span data-ttu-id="ca8c2-450"><span id="G6"></span><span id="g6"></span>**G6** (203) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-450"><span id="G6"></span><span id="g6"></span>**G6** (203)</span></span>


</dt> <dd></dd> <dt>

<span id="z_Architecture_base"></span><span id="z_architecture_base"></span><span id="Z_ARCHITECTURE_BASE"></span>

<span data-ttu-id="ca8c2-451"><span id="z_Architecture_base"></span><span id="z_architecture_base"></span><span id="Z_ARCHITECTURE_BASE"></span>**z/架構基底** (204) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-451"><span id="z_Architecture_base"></span><span id="z_architecture_base"></span><span id="Z_ARCHITECTURE_BASE"></span>**z/Architecture base** (204)</span></span>


</dt> <dd></dd> <dt>

<span id="i860"></span><span id="I860"></span>

<span data-ttu-id="ca8c2-452"><span id="i860"></span><span id="I860"></span>**i860** (250) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-452"><span id="i860"></span><span id="I860"></span>**i860** (250)</span></span>


</dt> <dd></dd> <dt>

<span id="i960"></span><span id="I960"></span>

<span data-ttu-id="ca8c2-453"><span id="i960"></span><span id="I960"></span>**i960** (251) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-453"><span id="i960"></span><span id="I960"></span>**i960** (251)</span></span>


</dt> <dd></dd> <dt>

<span id="SH-3"></span><span id="sh-3"></span>

<span data-ttu-id="ca8c2-454"><span id="SH-3"></span><span id="sh-3"></span>**SH-3** (260) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-454"><span id="SH-3"></span><span id="sh-3"></span>**SH-3** (260)</span></span>


</dt> <dd></dd> <dt>

<span id="SH-4"></span><span id="sh-4"></span>

<span data-ttu-id="ca8c2-455"><span id="SH-4"></span><span id="sh-4"></span>**SH-4** (261) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-455"><span id="SH-4"></span><span id="sh-4"></span>**SH-4** (261)</span></span>


</dt> <dd></dd> <dt>

<span id="ARM"></span><span id="arm"></span>

<span data-ttu-id="ca8c2-456"><span id="ARM"></span><span id="arm"></span>**ARM** (280) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-456"><span id="ARM"></span><span id="arm"></span>**ARM** (280)</span></span>


</dt> <dd></dd> <dt>

<span id="StrongARM"></span><span id="strongarm"></span><span id="STRONGARM"></span>

<span data-ttu-id="ca8c2-457"><span id="StrongARM"></span><span id="strongarm"></span><span id="STRONGARM"></span>**StrongARM** (281) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-457"><span id="StrongARM"></span><span id="strongarm"></span><span id="STRONGARM"></span>**StrongARM** (281)</span></span>


</dt> <dd></dd> <dt>

<span id="6x86"></span><span id="6X86"></span>

<span data-ttu-id="ca8c2-458"><span id="6x86"></span><span id="6X86"></span>**6x86** (300) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-458"><span id="6x86"></span><span id="6X86"></span>**6x86** (300)</span></span>


</dt> <dd></dd> <dt>

<span id="MediaGX"></span><span id="mediagx"></span><span id="MEDIAGX"></span>

<span data-ttu-id="ca8c2-459"><span id="MediaGX"></span><span id="mediagx"></span><span id="MEDIAGX"></span>**MediaGX** (301) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-459"><span id="MediaGX"></span><span id="mediagx"></span><span id="MEDIAGX"></span>**MediaGX** (301)</span></span>


</dt> <dd></dd> <dt>

<span id="MII"></span><span id="mii"></span>

<span data-ttu-id="ca8c2-460"><span id="MII"></span><span id="mii"></span>**MII** (302) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-460"><span id="MII"></span><span id="mii"></span>**MII** (302)</span></span>


</dt> <dd></dd> <dt>

<span id="WinChip"></span><span id="winchip"></span><span id="WINCHIP"></span>

<span data-ttu-id="ca8c2-461"><span id="WinChip"></span><span id="winchip"></span><span id="WINCHIP"></span>**WinChip** (320) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-461"><span id="WinChip"></span><span id="winchip"></span><span id="WINCHIP"></span>**WinChip** (320)</span></span>


</dt> <dd></dd> <dt>

<span id="DSP"></span><span id="dsp"></span>

<span data-ttu-id="ca8c2-462"><span id="DSP"></span><span id="dsp"></span>**DSP** (350) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-462"><span id="DSP"></span><span id="dsp"></span>**DSP** (350)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_Processor"></span><span id="video_processor"></span><span id="VIDEO_PROCESSOR"></span>

<span data-ttu-id="ca8c2-463"><span id="Video_Processor"></span><span id="video_processor"></span><span id="VIDEO_PROCESSOR"></span>**影片處理器** (500) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-463"><span id="Video_Processor"></span><span id="video_processor"></span><span id="VIDEO_PROCESSOR"></span>**Video Processor** (500)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ca8c2-464">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-464">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-465">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-465">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-466">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-467">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="ca8c2-467">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-468">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-468">Date and time the object was installed.</span></span> <span data-ttu-id="ca8c2-469">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-469">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="ca8c2-470">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-470">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca8c2-471">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-471">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-472">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-472">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-473">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-473">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-474">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-474">Last error code reported by the logical device.</span></span>

<span data-ttu-id="ca8c2-475">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-475">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca8c2-476">**LoadPercentage**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-476">**LoadPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-477">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-477">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-478">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-479">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrProcessorLoad ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" percent ") </span><span class="sxs-lookup"><span data-stu-id="ca8c2-479">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrProcessorLoad"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-480">處理器的載入（以百分比表示的平均）。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-480">Loading of the processor, averaged over the last minute, in a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="ca8c2-481">**MaxClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-481">**MaxClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-482">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-482">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-483">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-483">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-484">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 處理器 \| 006.5 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" mhz ") </span><span class="sxs-lookup"><span data-stu-id="ca8c2-484">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|006.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-485">處理器的最大速率 (mhz) 。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-485">Maximum speed (in megahertz) of the processor.</span></span>

</dd> <dt>

<span data-ttu-id="ca8c2-486">**名稱**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-486">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-487">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-488">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-489">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-489">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-490">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-490">Label by which the object is known.</span></span> <span data-ttu-id="ca8c2-491">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-491">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="ca8c2-492">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-492">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca8c2-493">**OtherFamilyDescription**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-493">**OtherFamilyDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-494">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-494">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-495">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-496">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (」**CIM \_ 處理器**。**系列**」 ) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-496">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Processor**.**Family**")</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-497">處理器系列類型的描述。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-497">Description of the processor family type.</span></span> <span data-ttu-id="ca8c2-498">當 [ **系列** ] 屬性設定為 1 ( "其他" ) 時，會使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-498">This property is used when the **Family** property is set to 1 ("Other").</span></span> <span data-ttu-id="ca8c2-499">當 **系列** 屬性是1以外的值時，此字串應該設為 null。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-499">This string should be set to null when the **Family** property is a value other than 1.</span></span>

</dd> <dt>

<span data-ttu-id="ca8c2-500">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-500">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-501">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-501">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-502">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-503">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-503">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-504">隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-504">Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="ca8c2-505">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-505">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="ca8c2-506">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="ca8c2-506">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="ca8c2-507">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-507">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-508">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="ca8c2-508">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-509">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-509">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-510">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-510">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="ca8c2-511">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-511">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ca8c2-512"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-512"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="ca8c2-513"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-513"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ca8c2-514"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-514"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ca8c2-515"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-515"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-516">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-516">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="ca8c2-517"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-517"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-518">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-518">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="ca8c2-519"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-519"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-520">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-520">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="ca8c2-521">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-521">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="ca8c2-522">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-522">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="ca8c2-523"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-523"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-524">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-524">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="ca8c2-525"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-525"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-526">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-526">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ca8c2-527">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-527">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-528">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-528">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-529">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-529">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-530">若 **為 True**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-530">If **True**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="ca8c2-531">如果 **為 False**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-531">If **False**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="ca8c2-532">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-532">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="ca8c2-533">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-533">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="ca8c2-534">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-534">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca8c2-535">**角色**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-535">**Role**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-536">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-536">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-537">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-538">描述處理器角色的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-538">Free-form string that describes the role of the processor.</span></span> <span data-ttu-id="ca8c2-539">例如，「中央處理器」或「數學處理器」。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-539">For example, "Central Processor" or "Math Processor".</span></span>

</dd> <dt>

<span data-ttu-id="ca8c2-540">**狀態**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-540">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-541">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-542">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-543">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-543">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-544">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-544">Current status of the object.</span></span>

<span data-ttu-id="ca8c2-545">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-545">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ca8c2-546">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="ca8c2-546">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ca8c2-547">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-547">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ca8c2-548">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-548">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ca8c2-549">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-549">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ca8c2-550">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-550">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ca8c2-551">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-551">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ca8c2-552">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-552">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ca8c2-553">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-553">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ca8c2-554">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-554">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ca8c2-555">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-555">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ca8c2-556">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-556">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ca8c2-557">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-557">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ca8c2-558">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-558">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ca8c2-559">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-559">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-560">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-560">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-561">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-561">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-562">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="ca8c2-562">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-563">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-563">State of the logical device.</span></span> <span data-ttu-id="ca8c2-564">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-564">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="ca8c2-565">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-565">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ca8c2-566">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-566">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ca8c2-567">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-567">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ca8c2-568">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-568">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ca8c2-569">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-569">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ca8c2-570">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-570">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ca8c2-571">**逐步執行**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-571">**Stepping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-572">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-572">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-573">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-573">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-574">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 處理器**」。**系列**」 ) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-574">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Processor**.**Family**")</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-575">表示處理器系列內處理器修訂層級的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-575">Free-form string that indicates the revision level of the processor within the processor family.</span></span>

</dd> <dt>

<span data-ttu-id="ca8c2-576">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-576">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-577">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-578">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-578">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-579">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-579">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-580">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-580">Scoping system's creation class name.</span></span>

<span data-ttu-id="ca8c2-581">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-581">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca8c2-582">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-582">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-583">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-584">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-584">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-585">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ca8c2-585">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-586">設定系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-586">Scoping system's name.</span></span>

<span data-ttu-id="ca8c2-587">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-587">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca8c2-588">**唯一**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-588">**UniqueId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-589">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-590">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-590">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-591">處理器的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-591">Globally unique identifier for the processor.</span></span> <span data-ttu-id="ca8c2-592">此識別碼在處理器系列中只能是唯一的。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-592">This identifier can only be unique within a processor family.</span></span>

</dd> <dt>

<span data-ttu-id="ca8c2-593">**UpgradeMethod**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-593">**UpgradeMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca8c2-594">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-594">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-595">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca8c2-595">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca8c2-596">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 處理器 \| 006.7」 ) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-596">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|006.7")</span></span>
</dt> </dl>

<span data-ttu-id="ca8c2-597">CPU 通訊端資訊，其中包含有關如何升級處理器 (的資料) 是否支援升級。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-597">CPU socket information, which includes data on how to upgrade the processor (if upgrades are supported).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ca8c2-598"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-598"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ca8c2-599"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-599"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Daughter_Board"></span><span id="daughter_board"></span><span id="DAUGHTER_BOARD"></span>

<span data-ttu-id="ca8c2-600"><span id="Daughter_Board"></span><span id="daughter_board"></span><span id="DAUGHTER_BOARD"></span>**子板** (3) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-600"><span id="Daughter_Board"></span><span id="daughter_board"></span><span id="DAUGHTER_BOARD"></span>**Daughter Board** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ZIF_Socket"></span><span id="zif_socket"></span><span id="ZIF_SOCKET"></span>

<span data-ttu-id="ca8c2-601"><span id="ZIF_Socket"></span><span id="zif_socket"></span><span id="ZIF_SOCKET"></span>**ZIF 通訊端** (4) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-601"><span id="ZIF_Socket"></span><span id="zif_socket"></span><span id="ZIF_SOCKET"></span>**ZIF Socket** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Replacement_Piggy_Back"></span><span id="replacement_piggy_back"></span><span id="REPLACEMENT_PIGGY_BACK"></span>

<span data-ttu-id="ca8c2-602"><span id="Replacement_Piggy_Back"></span><span id="replacement_piggy_back"></span><span id="REPLACEMENT_PIGGY_BACK"></span>**取代/Piggy 後** (5) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-602"><span id="Replacement_Piggy_Back"></span><span id="replacement_piggy_back"></span><span id="REPLACEMENT_PIGGY_BACK"></span>**Replacement/Piggy Back** (5)</span></span>


</dt> <dd>

<span data-ttu-id="ca8c2-603">取代或 piggy 回</span><span class="sxs-lookup"><span data-stu-id="ca8c2-603">Replacement or piggy back</span></span>

</dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="ca8c2-604"><span id="None"></span><span id="none"></span><span id="NONE"></span>**無** (6) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-604"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="LIF_Socket"></span><span id="lif_socket"></span><span id="LIF_SOCKET"></span>

<span data-ttu-id="ca8c2-605"><span id="LIF_Socket"></span><span id="lif_socket"></span><span id="LIF_SOCKET"></span>**LIF 通訊端** (7) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-605"><span id="LIF_Socket"></span><span id="lif_socket"></span><span id="LIF_SOCKET"></span>**LIF Socket** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_1"></span><span id="slot_1"></span><span id="SLOT_1"></span>

<span data-ttu-id="ca8c2-606"><span id="Slot_1"></span><span id="slot_1"></span><span id="SLOT_1"></span>**插槽 1** (8) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-606"><span id="Slot_1"></span><span id="slot_1"></span><span id="SLOT_1"></span>**Slot 1** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_2"></span><span id="slot_2"></span><span id="SLOT_2"></span>

<span data-ttu-id="ca8c2-607"><span id="Slot_2"></span><span id="slot_2"></span><span id="SLOT_2"></span>**插槽 2** (9) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-607"><span id="Slot_2"></span><span id="slot_2"></span><span id="SLOT_2"></span>**Slot 2** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="370_Pin_Socket"></span><span id="370_pin_socket"></span><span id="370_PIN_SOCKET"></span>

<span data-ttu-id="ca8c2-608"><span id="370_Pin_Socket"></span><span id="370_pin_socket"></span><span id="370_PIN_SOCKET"></span>**370 Pin 通訊端** (10) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-608"><span id="370_Pin_Socket"></span><span id="370_pin_socket"></span><span id="370_PIN_SOCKET"></span>**370 Pin Socket** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_A"></span><span id="slot_a"></span><span id="SLOT_A"></span>

<span data-ttu-id="ca8c2-609"><span id="Slot_A"></span><span id="slot_a"></span><span id="SLOT_A"></span>**插槽 A** (11) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-609"><span id="Slot_A"></span><span id="slot_a"></span><span id="SLOT_A"></span>**Slot A** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_M"></span><span id="slot_m"></span><span id="SLOT_M"></span>

<span data-ttu-id="ca8c2-610"><span id="Slot_M"></span><span id="slot_m"></span><span id="SLOT_M"></span>**插槽 M** (12) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-610"><span id="Slot_M"></span><span id="slot_m"></span><span id="SLOT_M"></span>**Slot M** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_423"></span><span id="socket_423"></span><span id="SOCKET_423"></span>

<span data-ttu-id="ca8c2-611"><span id="Socket_423"></span><span id="socket_423"></span><span id="SOCKET_423"></span>**通訊端 423** (13) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-611"><span id="Socket_423"></span><span id="socket_423"></span><span id="SOCKET_423"></span>**Socket 423** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_A__Socket_462_"></span><span id="socket_a__socket_462_"></span><span id="SOCKET_A__SOCKET_462_"></span>

<span data-ttu-id="ca8c2-612"><span id="Socket_A__Socket_462_"></span><span id="socket_a__socket_462_"></span><span id="SOCKET_A__SOCKET_462_"></span>**通訊端 A (通訊端 462)** (14) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-612"><span id="Socket_A__Socket_462_"></span><span id="socket_a__socket_462_"></span><span id="SOCKET_A__SOCKET_462_"></span>**Socket A (Socket 462)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_478"></span><span id="socket_478"></span><span id="SOCKET_478"></span>

<span data-ttu-id="ca8c2-613"><span id="Socket_478"></span><span id="socket_478"></span><span id="SOCKET_478"></span>**通訊端 478** (15) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-613"><span id="Socket_478"></span><span id="socket_478"></span><span id="SOCKET_478"></span>**Socket 478** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_754"></span><span id="socket_754"></span><span id="SOCKET_754"></span>

<span data-ttu-id="ca8c2-614"><span id="Socket_754"></span><span id="socket_754"></span><span id="SOCKET_754"></span>**通訊端 754** (16) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-614"><span id="Socket_754"></span><span id="socket_754"></span><span id="SOCKET_754"></span>**Socket 754** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_940"></span><span id="socket_940"></span><span id="SOCKET_940"></span>

<span data-ttu-id="ca8c2-615"><span id="Socket_940"></span><span id="socket_940"></span><span id="SOCKET_940"></span>**通訊端 940** (17) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-615"><span id="Socket_940"></span><span id="socket_940"></span><span id="SOCKET_940"></span>**Socket 940** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_939"></span><span id="socket_939"></span><span id="SOCKET_939"></span>

<span data-ttu-id="ca8c2-616"><span id="Socket_939"></span><span id="socket_939"></span><span id="SOCKET_939"></span>**通訊端 939** (18) </span><span class="sxs-lookup"><span data-stu-id="ca8c2-616"><span id="Socket_939"></span><span id="socket_939"></span><span id="SOCKET_939"></span>**Socket 939** (18)</span></span>


<span data-ttu-id="ca8c2-617"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ca8c2-617"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="ca8c2-618">備註</span><span class="sxs-lookup"><span data-stu-id="ca8c2-618">Remarks</span></span>

<span data-ttu-id="ca8c2-619">**Cim \_ 處理器** 類別衍生自 [**cim \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-619">The **CIM\_Processor** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="ca8c2-620">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-620">WMI does not implement this class.</span></span> <span data-ttu-id="ca8c2-621">針對衍生自 **CIM \_ 處理器** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-621">For WMI classes derived from **CIM\_Processor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="ca8c2-622">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-622">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ca8c2-623">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="ca8c2-623">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca8c2-624">規格需求</span><span class="sxs-lookup"><span data-stu-id="ca8c2-624">Requirements</span></span>



| <span data-ttu-id="ca8c2-625">需求</span><span class="sxs-lookup"><span data-stu-id="ca8c2-625">Requirement</span></span> | <span data-ttu-id="ca8c2-626">值</span><span class="sxs-lookup"><span data-stu-id="ca8c2-626">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca8c2-627">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ca8c2-627">Minimum supported client</span></span><br/> | <span data-ttu-id="ca8c2-628">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca8c2-628">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ca8c2-629">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ca8c2-629">Minimum supported server</span></span><br/> | <span data-ttu-id="ca8c2-630">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca8c2-630">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ca8c2-631">命名空間</span><span class="sxs-lookup"><span data-stu-id="ca8c2-631">Namespace</span></span><br/>                | <span data-ttu-id="ca8c2-632">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ca8c2-632">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ca8c2-633">MOF</span><span class="sxs-lookup"><span data-stu-id="ca8c2-633">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca8c2-634"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca8c2-634"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca8c2-635">DLL</span><span class="sxs-lookup"><span data-stu-id="ca8c2-635">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca8c2-636"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca8c2-636"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca8c2-637">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ca8c2-637">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca8c2-638">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="ca8c2-638">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

