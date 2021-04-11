---
description: CIM \_ 印表機類別代表印表機邏輯裝置的功能和管理。
ms.assetid: e41ff580-0202-4d3f-8d78-4705d5fb41b3
ms.tgt_platform: multiple
title: CIM_Printer 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Printer
- CIM_Printer.Availability
- CIM_Printer.AvailableJobSheets
- CIM_Printer.Capabilities
- CIM_Printer.CapabilityDescriptions
- CIM_Printer.Caption
- CIM_Printer.CharSetsSupported
- CIM_Printer.ConfigManagerErrorCode
- CIM_Printer.ConfigManagerUserConfig
- CIM_Printer.CreationClassName
- CIM_Printer.CurrentCapabilities
- CIM_Printer.CurrentCharSet
- CIM_Printer.CurrentLanguage
- CIM_Printer.CurrentMimeType
- CIM_Printer.CurrentNaturalLanguage
- CIM_Printer.CurrentPaperType
- CIM_Printer.DefaultCapabilities
- CIM_Printer.DefaultCopies
- CIM_Printer.DefaultLanguage
- CIM_Printer.DefaultMimeType
- CIM_Printer.DefaultNumberUp
- CIM_Printer.DefaultPaperType
- CIM_Printer.Description
- CIM_Printer.DetectedErrorState
- CIM_Printer.DeviceID
- CIM_Printer.ErrorCleared
- CIM_Printer.ErrorDescription
- CIM_Printer.ErrorInformation
- CIM_Printer.HorizontalResolution
- CIM_Printer.InstallDate
- CIM_Printer.JobCountSinceLastReset
- CIM_Printer.LanguagesSupported
- CIM_Printer.LastErrorCode
- CIM_Printer.MarkingTechnology
- CIM_Printer.MaxCopies
- CIM_Printer.MaxNumberUp
- CIM_Printer.MaxSizeSupported
- CIM_Printer.MimeTypesSupported
- CIM_Printer.Name
- CIM_Printer.NaturalLanguagesSupported
- CIM_Printer.PaperSizesSupported
- CIM_Printer.PaperTypesAvailable
- CIM_Printer.PNPDeviceID
- CIM_Printer.PowerManagementCapabilities
- CIM_Printer.PowerManagementSupported
- CIM_Printer.PrinterStatus
- CIM_Printer.Status
- CIM_Printer.StatusInfo
- CIM_Printer.SystemCreationClassName
- CIM_Printer.SystemName
- CIM_Printer.TimeOfLastReset
- CIM_Printer.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5c673d6c58e6235e782a718b3b258a15790046eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111541"
---
# <a name="cim_printer-class"></a><span data-ttu-id="06381-103">CIM \_ 印表機類別</span><span class="sxs-lookup"><span data-stu-id="06381-103">CIM\_Printer class</span></span>

<span data-ttu-id="06381-104">**CIM \_ 印表機** 類別代表印表機邏輯裝置的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="06381-104">The **CIM\_Printer** class represents the capabilities and management of the printer logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="06381-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="06381-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="06381-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="06381-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="06381-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="06381-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="06381-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="06381-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="06381-109">語法</span><span class="sxs-lookup"><span data-stu-id="06381-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C54A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Printer : CIM_LogicalDevice
{
  uint16   Availability;
  string   AvailableJobSheets[];
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CharSetsSupported[];
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint16   CurrentCapabilities[];
  string   CurrentCharSet;
  uint16   CurrentLanguage;
  string   CurrentMimeType;
  string   CurrentNaturalLanguage;
  string   CurrentPaperType;
  uint16   DefaultCapabilities[];
  uint32   DefaultCopies;
  uint16   DefaultLanguage;
  string   DefaultMimeType;
  uint32   DefaultNumberUp;
  string   DefaultPaperType;
  string   Description;
  uint16   DetectedErrorState;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorInformation[];
  uint32   HorizontalResolution;
  datetime InstallDate;
  uint32   JobCountSinceLastReset;
  uint16   LanguagesSupported[];
  uint32   LastErrorCode;
  uint16   MarkingTechnology;
  uint32   MaxCopies;
  uint32   MaxNumberUp;
  uint32   MaxSizeSupported;
  string   MimeTypesSupported[];
  string   Name;
  string   NaturalLanguagesSupported[];
  uint16   PaperSizesSupported[];
  string   PaperTypesAvailable[];
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PrinterStatus;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
  uint32   VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="06381-110">成員</span><span class="sxs-lookup"><span data-stu-id="06381-110">Members</span></span>

<span data-ttu-id="06381-111">**CIM \_ 印表機** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="06381-111">The **CIM\_Printer** class has these types of members:</span></span>

-   [<span data-ttu-id="06381-112">方法</span><span class="sxs-lookup"><span data-stu-id="06381-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="06381-113">屬性</span><span class="sxs-lookup"><span data-stu-id="06381-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="06381-114">方法</span><span class="sxs-lookup"><span data-stu-id="06381-114">Methods</span></span>

<span data-ttu-id="06381-115">**CIM \_ 印表機** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="06381-115">The **CIM\_Printer** class has these methods.</span></span>



| <span data-ttu-id="06381-116">方法</span><span class="sxs-lookup"><span data-stu-id="06381-116">Method</span></span>                                                             | <span data-ttu-id="06381-117">描述</span><span class="sxs-lookup"><span data-stu-id="06381-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06381-118">**重設**</span><span class="sxs-lookup"><span data-stu-id="06381-118">**Reset**</span></span>](reset-method-in-class-cim-printer.md)                 | <span data-ttu-id="06381-119">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="06381-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="06381-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="06381-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="06381-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="06381-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-printer.md) | <span data-ttu-id="06381-122">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="06381-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="06381-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="06381-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="06381-124">屬性</span><span class="sxs-lookup"><span data-stu-id="06381-124">Properties</span></span>

<span data-ttu-id="06381-125">**CIM \_ 印表機** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="06381-125">The **CIM\_Printer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="06381-126">**可用性**</span><span class="sxs-lookup"><span data-stu-id="06381-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-127">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06381-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06381-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-129">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="06381-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="06381-130">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="06381-130">Availability and status of the device.</span></span>

<span data-ttu-id="06381-131">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="06381-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="06381-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="06381-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06381-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="06381-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="06381-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="06381-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="06381-135">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="06381-135">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="06381-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="06381-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="06381-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="06381-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="06381-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="06381-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="06381-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="06381-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="06381-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="06381-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="06381-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="06381-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="06381-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="06381-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="06381-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="06381-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="06381-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="06381-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="06381-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="06381-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="06381-146">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="06381-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="06381-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="06381-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="06381-148">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="06381-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="06381-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="06381-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="06381-150">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="06381-150">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="06381-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="06381-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="06381-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="06381-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="06381-153">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="06381-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="06381-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="06381-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="06381-155">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="06381-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="06381-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="06381-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="06381-157">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="06381-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="06381-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="06381-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="06381-159">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="06381-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="06381-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="06381-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="06381-161">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="06381-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="06381-162">**AvailableJobSheets**</span><span class="sxs-lookup"><span data-stu-id="06381-162">**AvailableJobSheets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-163">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="06381-163">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="06381-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-165">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM \_ PrintJob. RequiredJobSheets" ) </span><span class="sxs-lookup"><span data-stu-id="06381-165">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.RequiredJobSheets")</span></span>
</dt> </dl>

<span data-ttu-id="06381-166">描述印表機上所有可用的工作表。</span><span class="sxs-lookup"><span data-stu-id="06381-166">Describes all of the job sheets that are available on the printer.</span></span> <span data-ttu-id="06381-167">這也可以用來描述印表機可能會在每個作業開始時提供的橫幅，也可以描述其他使用者指定的選項。</span><span class="sxs-lookup"><span data-stu-id="06381-167">This can also be used to describe the banner that a printer might provide at the beginning of each job, or can describe other user specified options.</span></span>

</dd> <dt>

<span data-ttu-id="06381-168">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="06381-168">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-169">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="06381-169">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="06381-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-171">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (」**CIM \_ 印表機**。CapabilityDescriptions "、" CIM \_ PrintJob. 完成 "、" cim \_ PrintService. 功能 ") </span><span class="sxs-lookup"><span data-stu-id="06381-171">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.CapabilityDescriptions", "CIM\_PrintJob.Finishing", "CIM\_PrintService.Capabilities")</span></span>
</dt> </dl>

<span data-ttu-id="06381-172">印表機功能。</span><span class="sxs-lookup"><span data-stu-id="06381-172">Printer capabilities.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06381-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="06381-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="06381-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="06381-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="06381-175"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**色彩列印** (2) </span><span class="sxs-lookup"><span data-stu-id="06381-175"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="06381-176"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**雙工列印** (3) </span><span class="sxs-lookup"><span data-stu-id="06381-176"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="06381-177"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span> (4) **複製**</span><span class="sxs-lookup"><span data-stu-id="06381-177"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="06381-178"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>定 **序** (5) </span><span class="sxs-lookup"><span data-stu-id="06381-178"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="06381-179"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**裝訂** (6) </span><span class="sxs-lookup"><span data-stu-id="06381-179"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="06381-180"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span> (7) 的 **透明列印**</span><span class="sxs-lookup"><span data-stu-id="06381-180"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="06381-181"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**打孔** (8) </span><span class="sxs-lookup"><span data-stu-id="06381-181"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="06381-182"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**涵蓋** (9) </span><span class="sxs-lookup"><span data-stu-id="06381-182"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="06381-183"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>系 **結 (10**) </span><span class="sxs-lookup"><span data-stu-id="06381-183"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="06381-184"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**黑白列印** (11) </span><span class="sxs-lookup"><span data-stu-id="06381-184"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="06381-185"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**一側** (12) </span><span class="sxs-lookup"><span data-stu-id="06381-185"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="06381-186">單面</span><span class="sxs-lookup"><span data-stu-id="06381-186">One-sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="06381-187"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**雙側長邊緣** (13) </span><span class="sxs-lookup"><span data-stu-id="06381-187"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="06381-188">雙面長邊緣</span><span class="sxs-lookup"><span data-stu-id="06381-188">Two-sided long edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="06381-189"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**兩個側邊短邊緣** (14) </span><span class="sxs-lookup"><span data-stu-id="06381-189"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="06381-190">雙側短邊緣</span><span class="sxs-lookup"><span data-stu-id="06381-190">Two-sided short edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="06381-191"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**縱向** (15) </span><span class="sxs-lookup"><span data-stu-id="06381-191"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="06381-192"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**橫向** (16) </span><span class="sxs-lookup"><span data-stu-id="06381-192"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="06381-193"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**反向縱向** (17) </span><span class="sxs-lookup"><span data-stu-id="06381-193"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="06381-194"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**反向橫向** (18) </span><span class="sxs-lookup"><span data-stu-id="06381-194"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="06381-195"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**高品質** (19) </span><span class="sxs-lookup"><span data-stu-id="06381-195"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd>

<span data-ttu-id="06381-196">高品質</span><span class="sxs-lookup"><span data-stu-id="06381-196">Quality high</span></span>

</dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="06381-197"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**高品質標準** (20) </span><span class="sxs-lookup"><span data-stu-id="06381-197"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd>

<span data-ttu-id="06381-198">品質正常</span><span class="sxs-lookup"><span data-stu-id="06381-198">Quality normal</span></span>

</dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="06381-199"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**品質低** (21) </span><span class="sxs-lookup"><span data-stu-id="06381-199"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd>

<span data-ttu-id="06381-200">品質低</span><span class="sxs-lookup"><span data-stu-id="06381-200">Quality low</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="06381-201">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="06381-201">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-202">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="06381-202">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="06381-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-204">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (」**CIM \_ 印表機**。**功能**") </span><span class="sxs-lookup"><span data-stu-id="06381-204">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="06381-205">自由格式字串，提供 **功能** 陣列中所指出之任何印表機功能的詳細說明。</span><span class="sxs-lookup"><span data-stu-id="06381-205">Free-form strings that provide detailed explanations for any of the printer features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="06381-206">這個陣列的每個專案都與位於相同索引的 **功能** 陣列中的專案相關。</span><span class="sxs-lookup"><span data-stu-id="06381-206">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="06381-207">**標題**</span><span class="sxs-lookup"><span data-stu-id="06381-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-208">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06381-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06381-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-210">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="06381-210">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="06381-211">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="06381-211">Short textual description of the object.</span></span>

<span data-ttu-id="06381-212">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="06381-212">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="06381-213">**CharSetsSupported**</span><span class="sxs-lookup"><span data-stu-id="06381-213">**CharSetsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-214">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="06381-214">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="06381-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-216">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**MODELCORRESPONDENCE**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM \_ PrintJob. 字元集" ) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 印表機-prtLocalizationCharacterSet ") </span><span class="sxs-lookup"><span data-stu-id="06381-216">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.CharSet"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtLocalizationCharacterSet")</span></span>
</dt> </dl>

<span data-ttu-id="06381-217">與管理印表機相關之文字輸出的可用字元集。</span><span class="sxs-lookup"><span data-stu-id="06381-217">Available character sets for the output of text related to managing the printer.</span></span> <span data-ttu-id="06381-218">在此屬性中提供的字串，應該符合 RFC 2046 (MIME 第2部分) 中的第4.1.2 節 ( "字元集參數" ) 所指定的語義和語法，並且包含在 IANA 字元集登錄中。</span><span class="sxs-lookup"><span data-stu-id="06381-218">Strings provided in this property should conform to the semantics and syntax specified by section 4.1.2 ("Charset parameter") in RFC 2046 (MIME Part 2), and contained in the IANA character-set registry.</span></span> <span data-ttu-id="06381-219">範例包括 "utf-8"、"us-ascii" 和 "iso-8859-1"。</span><span class="sxs-lookup"><span data-stu-id="06381-219">Examples include "utf-8", "us-ascii", and "iso-8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="06381-220">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="06381-220">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-221">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="06381-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06381-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-223">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="06381-223">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="06381-224">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="06381-224">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="06381-225">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="06381-225">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="06381-226"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="06381-226"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="06381-227"> (0)</span><span class="sxs-lookup"><span data-stu-id="06381-227">(0)</span></span>


</dt> <dd>

<span data-ttu-id="06381-228">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="06381-228">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="06381-229"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="06381-229"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="06381-230">(1)</span><span class="sxs-lookup"><span data-stu-id="06381-230">(1)</span></span>


</dt> <dd>

<span data-ttu-id="06381-231">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="06381-231">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="06381-232"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="06381-232"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="06381-233">(2)</span><span class="sxs-lookup"><span data-stu-id="06381-233">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="06381-234"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="06381-234"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="06381-235">(3)</span><span class="sxs-lookup"><span data-stu-id="06381-235">(3)</span></span>


</dt> <dd>

<span data-ttu-id="06381-236">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="06381-236">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="06381-237"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="06381-237"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="06381-238">(4)</span><span class="sxs-lookup"><span data-stu-id="06381-238">(4)</span></span>


</dt> <dd>

<span data-ttu-id="06381-239">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="06381-239">Device is not working properly.</span></span> <span data-ttu-id="06381-240">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="06381-240">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="06381-241"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="06381-241"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="06381-242">(5)</span><span class="sxs-lookup"><span data-stu-id="06381-242">(5)</span></span>


</dt> <dd>

<span data-ttu-id="06381-243">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="06381-243">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="06381-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="06381-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="06381-245">(6)</span><span class="sxs-lookup"><span data-stu-id="06381-245">(6)</span></span>


</dt> <dd>

<span data-ttu-id="06381-246">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="06381-246">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="06381-247"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="06381-247"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="06381-248">(7)</span><span class="sxs-lookup"><span data-stu-id="06381-248">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="06381-249"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="06381-249"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="06381-250">(8)</span><span class="sxs-lookup"><span data-stu-id="06381-250">(8)</span></span>


</dt> <dd>

<span data-ttu-id="06381-251">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="06381-251">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="06381-252"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="06381-252"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="06381-253">(9)</span><span class="sxs-lookup"><span data-stu-id="06381-253">(9)</span></span>


</dt> <dd>

<span data-ttu-id="06381-254">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="06381-254">Device is not working properly.</span></span> <span data-ttu-id="06381-255">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="06381-255">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="06381-256"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="06381-256"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="06381-257">(10)</span><span class="sxs-lookup"><span data-stu-id="06381-257">(10)</span></span>


</dt> <dd>

<span data-ttu-id="06381-258">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="06381-258">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="06381-259"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="06381-259"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="06381-260">(11)</span><span class="sxs-lookup"><span data-stu-id="06381-260">(11)</span></span>


</dt> <dd>

<span data-ttu-id="06381-261">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="06381-261">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="06381-262"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="06381-262"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="06381-263"> (12) </span><span class="sxs-lookup"><span data-stu-id="06381-263">(12)</span></span>


</dt> <dd>

<span data-ttu-id="06381-264">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="06381-264">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="06381-265"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="06381-265"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="06381-266">(13)</span><span class="sxs-lookup"><span data-stu-id="06381-266">(13)</span></span>


</dt> <dd>

<span data-ttu-id="06381-267">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="06381-267">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="06381-268"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="06381-268"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="06381-269">(14)</span><span class="sxs-lookup"><span data-stu-id="06381-269">(14)</span></span>


</dt> <dd>

<span data-ttu-id="06381-270">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="06381-270">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="06381-271"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="06381-271"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="06381-272">(15)</span><span class="sxs-lookup"><span data-stu-id="06381-272">(15)</span></span>


</dt> <dd>

<span data-ttu-id="06381-273">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="06381-273">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="06381-274"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="06381-274"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="06381-275">(16)</span><span class="sxs-lookup"><span data-stu-id="06381-275">(16)</span></span>


</dt> <dd>

<span data-ttu-id="06381-276">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="06381-276">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="06381-277"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="06381-277"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="06381-278">(17)</span><span class="sxs-lookup"><span data-stu-id="06381-278">(17)</span></span>


</dt> <dd>

<span data-ttu-id="06381-279">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="06381-279">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="06381-280"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="06381-280"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="06381-281">(18)</span><span class="sxs-lookup"><span data-stu-id="06381-281">(18)</span></span>


</dt> <dd>

<span data-ttu-id="06381-282">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="06381-282">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="06381-283"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="06381-283"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="06381-284">(19)</span><span class="sxs-lookup"><span data-stu-id="06381-284">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="06381-285"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="06381-285"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="06381-286">(20)</span><span class="sxs-lookup"><span data-stu-id="06381-286">(20)</span></span>


</dt> <dd>

<span data-ttu-id="06381-287">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="06381-287">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="06381-288"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="06381-288"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="06381-289">(21)</span><span class="sxs-lookup"><span data-stu-id="06381-289">(21)</span></span>


</dt> <dd>

<span data-ttu-id="06381-290">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="06381-290">System failure.</span></span> <span data-ttu-id="06381-291">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="06381-291">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="06381-292">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="06381-292">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="06381-293"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="06381-293"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="06381-294">(22)</span><span class="sxs-lookup"><span data-stu-id="06381-294">(22)</span></span>


</dt> <dd>

<span data-ttu-id="06381-295">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="06381-295">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="06381-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="06381-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="06381-297">(23)</span><span class="sxs-lookup"><span data-stu-id="06381-297">(23)</span></span>


</dt> <dd>

<span data-ttu-id="06381-298">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="06381-298">System failure.</span></span> <span data-ttu-id="06381-299">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="06381-299">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="06381-300"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="06381-300"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="06381-301">(24)</span><span class="sxs-lookup"><span data-stu-id="06381-301">(24)</span></span>


</dt> <dd>

<span data-ttu-id="06381-302">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="06381-302">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="06381-303"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="06381-303"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="06381-304">(25)</span><span class="sxs-lookup"><span data-stu-id="06381-304">(25)</span></span>


</dt> <dd>

<span data-ttu-id="06381-305">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="06381-305">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="06381-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="06381-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="06381-307">(26)</span><span class="sxs-lookup"><span data-stu-id="06381-307">(26)</span></span>


</dt> <dd>

<span data-ttu-id="06381-308">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="06381-308">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="06381-309"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="06381-309"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="06381-310">(27)</span><span class="sxs-lookup"><span data-stu-id="06381-310">(27)</span></span>


</dt> <dd>

<span data-ttu-id="06381-311">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="06381-311">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="06381-312"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="06381-312"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="06381-313">(28)</span><span class="sxs-lookup"><span data-stu-id="06381-313">(28)</span></span>


</dt> <dd>

<span data-ttu-id="06381-314">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="06381-314">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="06381-315"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="06381-315"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="06381-316">(29)</span><span class="sxs-lookup"><span data-stu-id="06381-316">(29)</span></span>


</dt> <dd>

<span data-ttu-id="06381-317">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="06381-317">Device is disabled.</span></span> <span data-ttu-id="06381-318">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="06381-318">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="06381-319"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="06381-319"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="06381-320">(30)</span><span class="sxs-lookup"><span data-stu-id="06381-320">(30)</span></span>


</dt> <dd>

<span data-ttu-id="06381-321">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="06381-321">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="06381-322"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="06381-322"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="06381-323"> (31) </span><span class="sxs-lookup"><span data-stu-id="06381-323">(31)</span></span>


</dt> <dd>

<span data-ttu-id="06381-324">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="06381-324">Device is not working properly.</span></span> <span data-ttu-id="06381-325">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="06381-325">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="06381-326">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="06381-326">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-327">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="06381-327">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06381-328">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-329">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="06381-329">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="06381-330">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="06381-330">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="06381-331">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="06381-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="06381-332">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="06381-332">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-333">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06381-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06381-334">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-335">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="06381-335">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="06381-336">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="06381-336">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="06381-337">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="06381-337">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="06381-338">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="06381-338">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="06381-339">**CurrentCapabilities**</span><span class="sxs-lookup"><span data-stu-id="06381-339">**CurrentCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-340">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="06381-340">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="06381-341">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-342">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 印表機**」。**功能**") </span><span class="sxs-lookup"><span data-stu-id="06381-342">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="06381-343">目前正在使用之印表機的 Finishings 和其他功能。</span><span class="sxs-lookup"><span data-stu-id="06381-343">Finishings and other capabilities of the printer that are currently in use.</span></span> <span data-ttu-id="06381-344">這個屬性中的每個專案也應該列在 **功能** 陣列中。</span><span class="sxs-lookup"><span data-stu-id="06381-344">Each entry in this property should also be listed in the **Capabilities** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06381-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="06381-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="06381-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="06381-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="06381-347"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**色彩列印** (2) </span><span class="sxs-lookup"><span data-stu-id="06381-347"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="06381-348"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**雙工列印** (3) </span><span class="sxs-lookup"><span data-stu-id="06381-348"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="06381-349"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span> (4) **複製**</span><span class="sxs-lookup"><span data-stu-id="06381-349"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="06381-350"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>定 **序** (5) </span><span class="sxs-lookup"><span data-stu-id="06381-350"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="06381-351"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**裝訂** (6) </span><span class="sxs-lookup"><span data-stu-id="06381-351"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="06381-352"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span> (7) 的 **透明列印**</span><span class="sxs-lookup"><span data-stu-id="06381-352"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="06381-353"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**打孔** (8) </span><span class="sxs-lookup"><span data-stu-id="06381-353"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="06381-354"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**涵蓋** (9) </span><span class="sxs-lookup"><span data-stu-id="06381-354"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="06381-355"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>系 **結 (10**) </span><span class="sxs-lookup"><span data-stu-id="06381-355"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="06381-356"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**黑白列印** (11) </span><span class="sxs-lookup"><span data-stu-id="06381-356"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="06381-357"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**一側** (12) </span><span class="sxs-lookup"><span data-stu-id="06381-357"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="06381-358">單面</span><span class="sxs-lookup"><span data-stu-id="06381-358">One-sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="06381-359"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**雙側長邊緣** (13) </span><span class="sxs-lookup"><span data-stu-id="06381-359"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="06381-360">雙面長邊緣</span><span class="sxs-lookup"><span data-stu-id="06381-360">Two-sided long edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="06381-361"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**兩個側邊短邊緣** (14) </span><span class="sxs-lookup"><span data-stu-id="06381-361"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="06381-362">雙側短邊緣</span><span class="sxs-lookup"><span data-stu-id="06381-362">Two-sided short edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="06381-363"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**縱向** (15) </span><span class="sxs-lookup"><span data-stu-id="06381-363"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="06381-364"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**橫向** (16) </span><span class="sxs-lookup"><span data-stu-id="06381-364"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="06381-365"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**反向縱向** (17) </span><span class="sxs-lookup"><span data-stu-id="06381-365"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="06381-366"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**反向橫向** (18) </span><span class="sxs-lookup"><span data-stu-id="06381-366"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="06381-367"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**高品質** (19) </span><span class="sxs-lookup"><span data-stu-id="06381-367"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd>

<span data-ttu-id="06381-368">高品質</span><span class="sxs-lookup"><span data-stu-id="06381-368">Quality high</span></span>

</dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="06381-369"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**高品質標準** (20) </span><span class="sxs-lookup"><span data-stu-id="06381-369"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd>

<span data-ttu-id="06381-370">品質正常</span><span class="sxs-lookup"><span data-stu-id="06381-370">Quality normal</span></span>

</dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="06381-371"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**品質低** (21) </span><span class="sxs-lookup"><span data-stu-id="06381-371"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd>

<span data-ttu-id="06381-372">品質低</span><span class="sxs-lookup"><span data-stu-id="06381-372">Quality low</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="06381-373">**CurrentCharSet**</span><span class="sxs-lookup"><span data-stu-id="06381-373">**CurrentCharSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-374">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06381-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06381-375">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-376">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 印表機**」。**CharSetsSupported**") </span><span class="sxs-lookup"><span data-stu-id="06381-376">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**CharSetsSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="06381-377">目前的字元集，用於與印表機管理相關的文字輸出。</span><span class="sxs-lookup"><span data-stu-id="06381-377">Current character set used for the output of text relating to management of the printer.</span></span> <span data-ttu-id="06381-378">這個屬性所描述的字元集也應該列在 **CharsetsSupported** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="06381-378">The character set described by this property should also be listed in the **CharsetsSupported** property.</span></span> <span data-ttu-id="06381-379">這個屬性所指定的字串應該符合 RFC 2046 (MIME 第2部分) 中的第4.1.2 節 ( "字元集參數" ) 所指定的語義和語法，並且包含在 IANA 字元集登錄中。</span><span class="sxs-lookup"><span data-stu-id="06381-379">The string specified by this property should conform to the semantics and syntax specified by section 4.1.2 ("Charset parameter") in RFC 2046 (MIME Part 2), and contained in the IANA character-set registry.</span></span> <span data-ttu-id="06381-380">範例包括 "utf-8"、"us-ascii" 和 "iso-8859-1"。</span><span class="sxs-lookup"><span data-stu-id="06381-380">Examples include "utf-8", "us-ascii", and "iso-8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="06381-381">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="06381-381">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-382">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06381-382">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06381-383">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-384">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 印表機**」。LanguagesSupported "、" CIM \_ Printer. CurrentMimeType ") </span><span class="sxs-lookup"><span data-stu-id="06381-384">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.LanguagesSupported", "CIM\_Printer.CurrentMimeType")</span></span>
</dt> </dl>

<span data-ttu-id="06381-385">目前使用的印表機語言;語言也應列在 **LanguagesSupported** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="06381-385">Current printer language being used; the language should also be listed in the **LanguagesSupported** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="06381-386">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="06381-386">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06381-387">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="06381-387">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="06381-388">**PCL** (3) </span><span class="sxs-lookup"><span data-stu-id="06381-388">**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="06381-389">**HPGL** (4) </span><span class="sxs-lookup"><span data-stu-id="06381-389">**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="06381-390">**PJL** (5) </span><span class="sxs-lookup"><span data-stu-id="06381-390">**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="06381-391">**PS** (6) </span><span class="sxs-lookup"><span data-stu-id="06381-391">**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="06381-392">**PSPrinter** (7) </span><span class="sxs-lookup"><span data-stu-id="06381-392">**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="06381-393">**Ipd** (8) </span><span class="sxs-lookup"><span data-stu-id="06381-393">**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="06381-394">**PPDS** (9) </span><span class="sxs-lookup"><span data-stu-id="06381-394">**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="06381-395">**EscapeP** (10) </span><span class="sxs-lookup"><span data-stu-id="06381-395">**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="06381-396">**Epson** (11) </span><span class="sxs-lookup"><span data-stu-id="06381-396">**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="06381-397">**DDIF** (12) </span><span class="sxs-lookup"><span data-stu-id="06381-397">**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="06381-398">**Interpress** (13) </span><span class="sxs-lookup"><span data-stu-id="06381-398">**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="06381-399">**ISO6429** (14) </span><span class="sxs-lookup"><span data-stu-id="06381-399">**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="06381-400">**行資料** (15) </span><span class="sxs-lookup"><span data-stu-id="06381-400">**Line Data** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="06381-401">**MODCA** (16) </span><span class="sxs-lookup"><span data-stu-id="06381-401">**MODCA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="06381-402">**REGIS** (17) </span><span class="sxs-lookup"><span data-stu-id="06381-402">**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="06381-403">**SCS** (18) </span><span class="sxs-lookup"><span data-stu-id="06381-403">**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="06381-404">**SPDL** (19) </span><span class="sxs-lookup"><span data-stu-id="06381-404">**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="06381-405">**TEK4014** (20) </span><span class="sxs-lookup"><span data-stu-id="06381-405">**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="06381-406">**PDS** (21) </span><span class="sxs-lookup"><span data-stu-id="06381-406">**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="06381-407">**IGP** (22) </span><span class="sxs-lookup"><span data-stu-id="06381-407">**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="06381-408">**CodeV** (23) </span><span class="sxs-lookup"><span data-stu-id="06381-408">**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="06381-409">**DSCDSE** (24) </span><span class="sxs-lookup"><span data-stu-id="06381-409">**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="06381-410">**WPS** (25) </span><span class="sxs-lookup"><span data-stu-id="06381-410">**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="06381-411">**LN03** (26) </span><span class="sxs-lookup"><span data-stu-id="06381-411">**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="06381-412">**CCITT** (27) </span><span class="sxs-lookup"><span data-stu-id="06381-412">**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="06381-413">**QUIC** (28) </span><span class="sxs-lookup"><span data-stu-id="06381-413">**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="06381-414">**CPAP** (29) </span><span class="sxs-lookup"><span data-stu-id="06381-414">**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="06381-415">**DecPPL** (30) </span><span class="sxs-lookup"><span data-stu-id="06381-415">**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="06381-416">**簡單文字** (31) </span><span class="sxs-lookup"><span data-stu-id="06381-416">**Simple Text** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="06381-417">**NPAP** (32) </span><span class="sxs-lookup"><span data-stu-id="06381-417">**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="06381-418">**DOC** (33) </span><span class="sxs-lookup"><span data-stu-id="06381-418">**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="06381-419"> (34) 的 **印象深刻**</span><span class="sxs-lookup"><span data-stu-id="06381-419">**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="06381-420">**Pinwriter** (35) </span><span class="sxs-lookup"><span data-stu-id="06381-420">**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="06381-421">**NPDL** (36) </span><span class="sxs-lookup"><span data-stu-id="06381-421">**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="06381-422">**NEC201PL** (37) </span><span class="sxs-lookup"><span data-stu-id="06381-422">**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="06381-423">**自動** (38) </span><span class="sxs-lookup"><span data-stu-id="06381-423">**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="06381-424">**頁面** (39) </span><span class="sxs-lookup"><span data-stu-id="06381-424">**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="06381-425">**Lip** (40) </span><span class="sxs-lookup"><span data-stu-id="06381-425">**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="06381-426">**TIFF** (41) </span><span class="sxs-lookup"><span data-stu-id="06381-426">**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="06381-427">**診斷** (42) </span><span class="sxs-lookup"><span data-stu-id="06381-427">**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="06381-428">**CaPSL** (43) </span><span class="sxs-lookup"><span data-stu-id="06381-428">**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="06381-429">**排除** (44) </span><span class="sxs-lookup"><span data-stu-id="06381-429">**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="06381-430">**Lcd** (45) </span><span class="sxs-lookup"><span data-stu-id="06381-430">**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="06381-431">**XES** (46) </span><span class="sxs-lookup"><span data-stu-id="06381-431">**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="06381-432">**MIME** (47) </span><span class="sxs-lookup"><span data-stu-id="06381-432">**MIME** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06381-433">**CurrentMimeType**</span><span class="sxs-lookup"><span data-stu-id="06381-433">**CurrentMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-434">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06381-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06381-435">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-436">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 印表機**」。**CurrentLanguage**") </span><span class="sxs-lookup"><span data-stu-id="06381-436">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**CurrentLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="06381-437">當 **CurrentLanguage** 屬性設定為表示正在使用 mime 類型時，印表機目前正在使用的 mime 類型。</span><span class="sxs-lookup"><span data-stu-id="06381-437">Mime type currently in use by the printer when the **CurrentLanguage** property is set to indicate that a mime type is in use.</span></span>

</dd> <dt>

<span data-ttu-id="06381-438">**CurrentNaturalLanguage**</span><span class="sxs-lookup"><span data-stu-id="06381-438">**CurrentNaturalLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-439">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06381-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06381-440">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-441">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 印表機**」。**NaturalLanguagesSupported**") </span><span class="sxs-lookup"><span data-stu-id="06381-441">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**NaturalLanguagesSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="06381-442">印表機正在使用的目前語言進行管理。</span><span class="sxs-lookup"><span data-stu-id="06381-442">Current language in use by the printer for management.</span></span> <span data-ttu-id="06381-443">此處所列的語言也應該列在 **NaturalLanguagesSupported** 中。</span><span class="sxs-lookup"><span data-stu-id="06381-443">The language listed here should also be listed in **NaturalLanguagesSupported**.</span></span>

</dd> <dt>

<span data-ttu-id="06381-444">**CurrentPaperType**</span><span class="sxs-lookup"><span data-stu-id="06381-444">**CurrentPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-445">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06381-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06381-446">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-447">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 印表機**」。**PaperTypesAvailable**") </span><span class="sxs-lookup"><span data-stu-id="06381-447">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="06381-448">印表機目前正在使用的紙張類型。</span><span class="sxs-lookup"><span data-stu-id="06381-448">Paper type currently in use by the printer.</span></span> <span data-ttu-id="06381-449">此字串應該以 ISO/IEC 10175 檔列印應用程式所指定的格式來表示 (DPA) ，也會在 RFC 1759 (印表機 MIB) 的附錄 C 中摘要說明。</span><span class="sxs-lookup"><span data-stu-id="06381-449">The string should be expressed in the form specified by ISO/IEC 10175 Document Printing Application (DPA), which is also summarized in Appendix C of RFC 1759 (Printer MIB).</span></span>

</dd> <dt>

<span data-ttu-id="06381-450">**DefaultCapabilities**</span><span class="sxs-lookup"><span data-stu-id="06381-450">**DefaultCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-451">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="06381-451">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="06381-452">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-452">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-453">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 印表機**」。**功能**") </span><span class="sxs-lookup"><span data-stu-id="06381-453">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="06381-454">印表機的預設 finishings 和其他功能。</span><span class="sxs-lookup"><span data-stu-id="06381-454">Default finishings and other capabilities of the printer.</span></span> <span data-ttu-id="06381-455">這個屬性中的每個專案也應該列在 **功能** 陣列中。</span><span class="sxs-lookup"><span data-stu-id="06381-455">Each entry in this property should also be listed in the **Capabilities** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06381-456"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="06381-456"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="06381-457"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="06381-457"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="06381-458"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**色彩列印** (2) </span><span class="sxs-lookup"><span data-stu-id="06381-458"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="06381-459"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**雙工列印** (3) </span><span class="sxs-lookup"><span data-stu-id="06381-459"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="06381-460"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span> (4) **複製**</span><span class="sxs-lookup"><span data-stu-id="06381-460"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="06381-461"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>定 **序** (5) </span><span class="sxs-lookup"><span data-stu-id="06381-461"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="06381-462"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**裝訂** (6) </span><span class="sxs-lookup"><span data-stu-id="06381-462"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="06381-463"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span> (7) 的 **透明列印**</span><span class="sxs-lookup"><span data-stu-id="06381-463"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="06381-464"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**打孔** (8) </span><span class="sxs-lookup"><span data-stu-id="06381-464"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="06381-465"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**涵蓋** (9) </span><span class="sxs-lookup"><span data-stu-id="06381-465"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="06381-466"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>系 **結 (10**) </span><span class="sxs-lookup"><span data-stu-id="06381-466"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="06381-467"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**黑白列印** (11) </span><span class="sxs-lookup"><span data-stu-id="06381-467"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="06381-468"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**一側** (12) </span><span class="sxs-lookup"><span data-stu-id="06381-468"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="06381-469">單面</span><span class="sxs-lookup"><span data-stu-id="06381-469">One-sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="06381-470"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**雙側長邊緣** (13) </span><span class="sxs-lookup"><span data-stu-id="06381-470"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="06381-471">雙面長邊緣</span><span class="sxs-lookup"><span data-stu-id="06381-471">Two-sided long edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="06381-472"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**兩個側邊短邊緣** (14) </span><span class="sxs-lookup"><span data-stu-id="06381-472"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="06381-473">雙側短邊緣</span><span class="sxs-lookup"><span data-stu-id="06381-473">Two-sided short edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="06381-474"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**縱向** (15) </span><span class="sxs-lookup"><span data-stu-id="06381-474"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="06381-475"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**橫向** (16) </span><span class="sxs-lookup"><span data-stu-id="06381-475"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="06381-476"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**反向縱向** (17) </span><span class="sxs-lookup"><span data-stu-id="06381-476"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="06381-477"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**反向橫向** (18) </span><span class="sxs-lookup"><span data-stu-id="06381-477"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="06381-478"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**高品質** (19) </span><span class="sxs-lookup"><span data-stu-id="06381-478"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd>

<span data-ttu-id="06381-479">高品質</span><span class="sxs-lookup"><span data-stu-id="06381-479">Quality high</span></span>

</dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="06381-480"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**高品質標準** (20) </span><span class="sxs-lookup"><span data-stu-id="06381-480"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd>

<span data-ttu-id="06381-481">品質正常</span><span class="sxs-lookup"><span data-stu-id="06381-481">Quality normal</span></span>

</dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="06381-482"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**品質低** (21) </span><span class="sxs-lookup"><span data-stu-id="06381-482"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd>

<span data-ttu-id="06381-483">品質低</span><span class="sxs-lookup"><span data-stu-id="06381-483">Quality low</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="06381-484">**DefaultCopies**</span><span class="sxs-lookup"><span data-stu-id="06381-484">**DefaultCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-485">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="06381-485">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06381-486">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06381-487">除非另有指定，否則單一作業將會產生的複本數目。</span><span class="sxs-lookup"><span data-stu-id="06381-487">Number of copies that a single job will produce, unless otherwise specified.</span></span>

</dd> <dt>

<span data-ttu-id="06381-488">**DefaultLanguage**</span><span class="sxs-lookup"><span data-stu-id="06381-488">**DefaultLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-489">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06381-489">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06381-490">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-490">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-491">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 印表機**」。LanguagesSupported "、" CIM \_ Printer. DefaultMimeType ") </span><span class="sxs-lookup"><span data-stu-id="06381-491">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.LanguagesSupported", "CIM\_Printer.DefaultMimeType")</span></span>
</dt> </dl>

<span data-ttu-id="06381-492">預設印表機語言。</span><span class="sxs-lookup"><span data-stu-id="06381-492">Default printer language.</span></span> <span data-ttu-id="06381-493">語言也應列在 **LanguagesSupported** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="06381-493">The language should also be listed in the **LanguagesSupported** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="06381-494">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="06381-494">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06381-495">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="06381-495">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="06381-496">**PCL** (3) </span><span class="sxs-lookup"><span data-stu-id="06381-496">**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="06381-497">**HPGL** (4) </span><span class="sxs-lookup"><span data-stu-id="06381-497">**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="06381-498">**PJL** (5) </span><span class="sxs-lookup"><span data-stu-id="06381-498">**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="06381-499">**PS** (6) </span><span class="sxs-lookup"><span data-stu-id="06381-499">**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="06381-500">**PSPrinter** (7) </span><span class="sxs-lookup"><span data-stu-id="06381-500">**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="06381-501">**Ipd** (8) </span><span class="sxs-lookup"><span data-stu-id="06381-501">**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="06381-502">**PPDS** (9) </span><span class="sxs-lookup"><span data-stu-id="06381-502">**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="06381-503">**EscapeP** (10) </span><span class="sxs-lookup"><span data-stu-id="06381-503">**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="06381-504">**Epson** (11) </span><span class="sxs-lookup"><span data-stu-id="06381-504">**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="06381-505">**DDIF** (12) </span><span class="sxs-lookup"><span data-stu-id="06381-505">**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="06381-506">**Interpress** (13) </span><span class="sxs-lookup"><span data-stu-id="06381-506">**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="06381-507">**ISO6429** (14) </span><span class="sxs-lookup"><span data-stu-id="06381-507">**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="06381-508">**行資料** (15) </span><span class="sxs-lookup"><span data-stu-id="06381-508">**Line Data** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="06381-509">**MODCA** (16) </span><span class="sxs-lookup"><span data-stu-id="06381-509">**MODCA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="06381-510">**REGIS** (17) </span><span class="sxs-lookup"><span data-stu-id="06381-510">**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="06381-511">**SCS** (18) </span><span class="sxs-lookup"><span data-stu-id="06381-511">**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="06381-512">**SPDL** (19) </span><span class="sxs-lookup"><span data-stu-id="06381-512">**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="06381-513">**TEK4014** (20) </span><span class="sxs-lookup"><span data-stu-id="06381-513">**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="06381-514">**PDS** (21) </span><span class="sxs-lookup"><span data-stu-id="06381-514">**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="06381-515">**IGP** (22) </span><span class="sxs-lookup"><span data-stu-id="06381-515">**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="06381-516">**CodeV** (23) </span><span class="sxs-lookup"><span data-stu-id="06381-516">**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="06381-517">**DSCDSE** (24) </span><span class="sxs-lookup"><span data-stu-id="06381-517">**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="06381-518">**WPS** (25) </span><span class="sxs-lookup"><span data-stu-id="06381-518">**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="06381-519">**LN03** (26) </span><span class="sxs-lookup"><span data-stu-id="06381-519">**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="06381-520">**CCITT** (27) </span><span class="sxs-lookup"><span data-stu-id="06381-520">**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="06381-521">**QUIC** (28) </span><span class="sxs-lookup"><span data-stu-id="06381-521">**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="06381-522">**CPAP** (29) </span><span class="sxs-lookup"><span data-stu-id="06381-522">**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="06381-523">**DecPPL** (30) </span><span class="sxs-lookup"><span data-stu-id="06381-523">**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="06381-524">**簡單文字** (31) </span><span class="sxs-lookup"><span data-stu-id="06381-524">**Simple Text** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="06381-525">**NPAP** (32) </span><span class="sxs-lookup"><span data-stu-id="06381-525">**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="06381-526">**DOC** (33) </span><span class="sxs-lookup"><span data-stu-id="06381-526">**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="06381-527"> (34) 的 **印象深刻**</span><span class="sxs-lookup"><span data-stu-id="06381-527">**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="06381-528">**Pinwriter** (35) </span><span class="sxs-lookup"><span data-stu-id="06381-528">**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="06381-529">**NPDL** (36) </span><span class="sxs-lookup"><span data-stu-id="06381-529">**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="06381-530">**NEC201PL** (37) </span><span class="sxs-lookup"><span data-stu-id="06381-530">**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="06381-531">**自動** (38) </span><span class="sxs-lookup"><span data-stu-id="06381-531">**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="06381-532">**頁面** (39) </span><span class="sxs-lookup"><span data-stu-id="06381-532">**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="06381-533">**Lip** (40) </span><span class="sxs-lookup"><span data-stu-id="06381-533">**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="06381-534">**TIFF** (41) </span><span class="sxs-lookup"><span data-stu-id="06381-534">**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="06381-535">**診斷** (42) </span><span class="sxs-lookup"><span data-stu-id="06381-535">**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="06381-536">**CaPSL** (43) </span><span class="sxs-lookup"><span data-stu-id="06381-536">**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="06381-537">**排除** (44) </span><span class="sxs-lookup"><span data-stu-id="06381-537">**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="06381-538">**Lcd** (45) </span><span class="sxs-lookup"><span data-stu-id="06381-538">**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="06381-539">**XES** (46) </span><span class="sxs-lookup"><span data-stu-id="06381-539">**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="06381-540">**MIME** (47) </span><span class="sxs-lookup"><span data-stu-id="06381-540">**MIME** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06381-541">**DefaultMimeType**</span><span class="sxs-lookup"><span data-stu-id="06381-541">**DefaultMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-542">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06381-542">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06381-543">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-544">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 印表機**」。**DefaultLanguage**") </span><span class="sxs-lookup"><span data-stu-id="06381-544">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**DefaultLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="06381-545">當 **DefaultLanguage** 屬性設定為表示正在使用 mime 類型時，印表機所使用的預設 mime 類型。</span><span class="sxs-lookup"><span data-stu-id="06381-545">Default mime type used by the printer when the **DefaultLanguage** property is set to indicate that a mime type is in use.</span></span>

</dd> <dt>

<span data-ttu-id="06381-546">**DefaultNumberUp**</span><span class="sxs-lookup"><span data-stu-id="06381-546">**DefaultNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-547">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="06381-547">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06381-548">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-548">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06381-549">除非作業另外指定，否則印表機將轉譯成單一媒體工作表的列印資料流程頁面數目。</span><span class="sxs-lookup"><span data-stu-id="06381-549">Number of print-stream pages that the printer will render onto a single media sheet, unless a job specifies otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="06381-550">**DefaultPaperType**</span><span class="sxs-lookup"><span data-stu-id="06381-550">**DefaultPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-551">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06381-551">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06381-552">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-552">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-553">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 印表機**」。**PaperTypesAvailable**") </span><span class="sxs-lookup"><span data-stu-id="06381-553">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="06381-554">如果 PrintJob 未指定特定類型，印表機將使用的紙張類型。</span><span class="sxs-lookup"><span data-stu-id="06381-554">Paper type that the printer will use if PrintJob does not specify a particular type.</span></span> <span data-ttu-id="06381-555">此字串應該以 ISO/IEC 10175 檔列印應用程式所指定的格式來表示 (DPA) ，也會在 RFC 1759 (印表機 MIB) 的附錄 C 中摘要說明。</span><span class="sxs-lookup"><span data-stu-id="06381-555">The string should be expressed in the form specified by ISO/IEC 10175 Document Printing Application (DPA), which is also summarized in Appendix C of RFC 1759 (Printer MIB).</span></span>

</dd> <dt>

<span data-ttu-id="06381-556">**說明**</span><span class="sxs-lookup"><span data-stu-id="06381-556">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-557">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06381-557">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06381-558">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-559">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="06381-559">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="06381-560">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="06381-560">Textual description of the object.</span></span>

<span data-ttu-id="06381-561">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="06381-561">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="06381-562">**DetectedErrorState**</span><span class="sxs-lookup"><span data-stu-id="06381-562">**DetectedErrorState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-563">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06381-563">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06381-564">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-564">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-565">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 印表機**」。**ErrorInformation**") ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIB。IETF \| 印表機-hrPrinterDetectedErrorState ") </span><span class="sxs-lookup"><span data-stu-id="06381-565">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**ErrorInformation**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.hrPrinterDetectedErrorState")</span></span>
</dt> </dl>

<span data-ttu-id="06381-566">印表機錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="06381-566">Printer error information.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06381-567">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="06381-567">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="06381-568">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="06381-568">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error"></span><span id="no_error"></span><span id="NO_ERROR"></span>

<span data-ttu-id="06381-569">**沒有錯誤** (2) </span><span class="sxs-lookup"><span data-stu-id="06381-569">**No Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Paper"></span><span id="low_paper"></span><span id="LOW_PAPER"></span>

<span data-ttu-id="06381-570">**低紙** (3) </span><span class="sxs-lookup"><span data-stu-id="06381-570">**Low Paper** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Paper"></span><span id="no_paper"></span><span id="NO_PAPER"></span>

<span data-ttu-id="06381-571">**沒有紙張** (4) </span><span class="sxs-lookup"><span data-stu-id="06381-571">**No Paper** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Toner"></span><span id="low_toner"></span><span id="LOW_TONER"></span>

<span data-ttu-id="06381-572">**低碳粉** (5) </span><span class="sxs-lookup"><span data-stu-id="06381-572">**Low Toner** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Toner"></span><span id="no_toner"></span><span id="NO_TONER"></span>

<span data-ttu-id="06381-573">**沒有碳粉** (6) </span><span class="sxs-lookup"><span data-stu-id="06381-573">**No Toner** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Door_Open"></span><span id="door_open"></span><span id="DOOR_OPEN"></span>

<span data-ttu-id="06381-574">**門開啟** (7) </span><span class="sxs-lookup"><span data-stu-id="06381-574">**Door Open** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Jammed"></span><span id="jammed"></span><span id="JAMMED"></span>

<span data-ttu-id="06381-575">**卡** (8) </span><span class="sxs-lookup"><span data-stu-id="06381-575">**Jammed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="06381-576">**離線** (9) </span><span class="sxs-lookup"><span data-stu-id="06381-576">**Offline** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Requested"></span><span id="service_requested"></span><span id="SERVICE_REQUESTED"></span>

<span data-ttu-id="06381-577">**要求的服務** (10) </span><span class="sxs-lookup"><span data-stu-id="06381-577">**Service Requested** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Bin_Full"></span><span id="output_bin_full"></span><span id="OUTPUT_BIN_FULL"></span>

<span data-ttu-id="06381-578">**輸出 Bin Full** (11) </span><span class="sxs-lookup"><span data-stu-id="06381-578">**Output Bin Full** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06381-579">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="06381-579">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-580">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06381-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06381-581">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-582">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="06381-582">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="06381-583">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="06381-583">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="06381-584">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="06381-584">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="06381-585">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="06381-585">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-586">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="06381-586">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06381-587">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-587">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06381-588">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="06381-588">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="06381-589">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="06381-589">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="06381-590">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="06381-590">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-591">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06381-591">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06381-592">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-592">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06381-593">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="06381-593">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="06381-594">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="06381-594">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="06381-595">**ErrorInformation**</span><span class="sxs-lookup"><span data-stu-id="06381-595">**ErrorInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-596">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="06381-596">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="06381-597">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="06381-597">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="06381-598">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 印表機**」。**DetectedErrorState**") </span><span class="sxs-lookup"><span data-stu-id="06381-598">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**DetectedErrorState**")</span></span>
</dt> </dl>

<span data-ttu-id="06381-599">陣列，提供目前錯誤狀態的補充資訊，以 **DetectedErrorState** 屬性工作表示。</span><span class="sxs-lookup"><span data-stu-id="06381-599">Array that provides supplemental information for the current error state, indicated in the **DetectedErrorState** property.</span></span>

</dd> <dt>

<span data-ttu-id="06381-600">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="06381-600">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-601">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="06381-601">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06381-602">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-602">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-603">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM \_ PrintJob. HorizontalResolution" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "圖元/英寸" ) </span><span class="sxs-lookup"><span data-stu-id="06381-603">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="06381-604">水準解析度（以圖元為單位）-每英寸。</span><span class="sxs-lookup"><span data-stu-id="06381-604">Horizontal resolution in pixels-per-inch.</span></span>

</dd> <dt>

<span data-ttu-id="06381-605">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="06381-605">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-606">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="06381-606">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="06381-607">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-607">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-608">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="06381-608">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="06381-609">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="06381-609">Date and time the object was installed.</span></span> <span data-ttu-id="06381-610">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="06381-610">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="06381-611">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="06381-611">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="06381-612">**JobCountSinceLastReset**</span><span class="sxs-lookup"><span data-stu-id="06381-612">**JobCountSinceLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-613">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="06381-613">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06381-614">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-614">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-615">限定詞： **計數器**</span><span class="sxs-lookup"><span data-stu-id="06381-615">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="06381-616">上次重設後處理的印表機工作。</span><span class="sxs-lookup"><span data-stu-id="06381-616">Printer jobs processed since the last reset.</span></span> <span data-ttu-id="06381-617">您可以從一或多個列印佇列處理這些作業。</span><span class="sxs-lookup"><span data-stu-id="06381-617">These jobs can be processed from one or more print queues.</span></span>

</dd> <dt>

<span data-ttu-id="06381-618">**LanguagesSupported**</span><span class="sxs-lookup"><span data-stu-id="06381-618">**LanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-619">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="06381-619">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="06381-620">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-620">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-621">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| printer-prtInterpreterLangFamily ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ printer**。MimeTypesSupported "、" CIM \_ PrintJob Language "、" cim \_ PrintService. LanguagesSupported ") </span><span class="sxs-lookup"><span data-stu-id="06381-621">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtInterpreterLangFamily"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.MimeTypesSupported", "CIM\_PrintJob.Language", "CIM\_PrintService.LanguagesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="06381-622">原生支援的列印語言。</span><span class="sxs-lookup"><span data-stu-id="06381-622">Print languages that are natively supported.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="06381-623">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="06381-623">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06381-624">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="06381-624">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="06381-625">**PCL** (3) </span><span class="sxs-lookup"><span data-stu-id="06381-625">**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="06381-626">**HPGL** (4) </span><span class="sxs-lookup"><span data-stu-id="06381-626">**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="06381-627">**PJL** (5) </span><span class="sxs-lookup"><span data-stu-id="06381-627">**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="06381-628">**PS** (6) </span><span class="sxs-lookup"><span data-stu-id="06381-628">**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="06381-629">**PSPrinter** (7) </span><span class="sxs-lookup"><span data-stu-id="06381-629">**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="06381-630">**Ipd** (8) </span><span class="sxs-lookup"><span data-stu-id="06381-630">**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="06381-631">**PPDS** (9) </span><span class="sxs-lookup"><span data-stu-id="06381-631">**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="06381-632">**EscapeP** (10) </span><span class="sxs-lookup"><span data-stu-id="06381-632">**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="06381-633">**Epson** (11) </span><span class="sxs-lookup"><span data-stu-id="06381-633">**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="06381-634">**DDIF** (12) </span><span class="sxs-lookup"><span data-stu-id="06381-634">**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="06381-635">**Interpress** (13) </span><span class="sxs-lookup"><span data-stu-id="06381-635">**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="06381-636">**ISO6429** (14) </span><span class="sxs-lookup"><span data-stu-id="06381-636">**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="06381-637">**行資料** (15) </span><span class="sxs-lookup"><span data-stu-id="06381-637">**Line Data** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="06381-638">**MODCA** (16) </span><span class="sxs-lookup"><span data-stu-id="06381-638">**MODCA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="06381-639">**REGIS** (17) </span><span class="sxs-lookup"><span data-stu-id="06381-639">**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="06381-640">**SCS** (18) </span><span class="sxs-lookup"><span data-stu-id="06381-640">**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="06381-641">**SPDL** (19) </span><span class="sxs-lookup"><span data-stu-id="06381-641">**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="06381-642">**TEK4014** (20) </span><span class="sxs-lookup"><span data-stu-id="06381-642">**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="06381-643">**PDS** (21) </span><span class="sxs-lookup"><span data-stu-id="06381-643">**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="06381-644">**IGP** (22) </span><span class="sxs-lookup"><span data-stu-id="06381-644">**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="06381-645">**CodeV** (23) </span><span class="sxs-lookup"><span data-stu-id="06381-645">**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="06381-646">**DSCDSE** (24) </span><span class="sxs-lookup"><span data-stu-id="06381-646">**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="06381-647">**WPS** (25) </span><span class="sxs-lookup"><span data-stu-id="06381-647">**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="06381-648">**LN03** (26) </span><span class="sxs-lookup"><span data-stu-id="06381-648">**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="06381-649">**CCITT** (27) </span><span class="sxs-lookup"><span data-stu-id="06381-649">**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="06381-650">**QUIC** (28) </span><span class="sxs-lookup"><span data-stu-id="06381-650">**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="06381-651">**CPAP** (29) </span><span class="sxs-lookup"><span data-stu-id="06381-651">**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="06381-652">**DecPPL** (30) </span><span class="sxs-lookup"><span data-stu-id="06381-652">**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="06381-653">**簡單文字** (31) </span><span class="sxs-lookup"><span data-stu-id="06381-653">**Simple Text** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="06381-654">**NPAP** (32) </span><span class="sxs-lookup"><span data-stu-id="06381-654">**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="06381-655">**DOC** (33) </span><span class="sxs-lookup"><span data-stu-id="06381-655">**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="06381-656"> (34) 的 **印象深刻**</span><span class="sxs-lookup"><span data-stu-id="06381-656">**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="06381-657">**Pinwriter** (35) </span><span class="sxs-lookup"><span data-stu-id="06381-657">**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="06381-658">**NPDL** (36) </span><span class="sxs-lookup"><span data-stu-id="06381-658">**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="06381-659">**NEC201PL** (37) </span><span class="sxs-lookup"><span data-stu-id="06381-659">**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="06381-660">**自動** (38) </span><span class="sxs-lookup"><span data-stu-id="06381-660">**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="06381-661">**頁面** (39) </span><span class="sxs-lookup"><span data-stu-id="06381-661">**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="06381-662">**Lip** (40) </span><span class="sxs-lookup"><span data-stu-id="06381-662">**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="06381-663">**TIFF** (41) </span><span class="sxs-lookup"><span data-stu-id="06381-663">**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="06381-664">**診斷** (42) </span><span class="sxs-lookup"><span data-stu-id="06381-664">**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="06381-665">**CaPSL** (43) </span><span class="sxs-lookup"><span data-stu-id="06381-665">**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="06381-666">**排除** (44) </span><span class="sxs-lookup"><span data-stu-id="06381-666">**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="06381-667">**Lcd** (45) </span><span class="sxs-lookup"><span data-stu-id="06381-667">**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="06381-668">**XES** (46) </span><span class="sxs-lookup"><span data-stu-id="06381-668">**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="06381-669">**MIME** (47) </span><span class="sxs-lookup"><span data-stu-id="06381-669">**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="XPS"></span><span id="xps"></span>

<span data-ttu-id="06381-670">**XPS** (48) </span><span class="sxs-lookup"><span data-stu-id="06381-670">**XPS** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL2"></span><span id="hpgl2"></span>

<span data-ttu-id="06381-671">**HPGL2** (49) </span><span class="sxs-lookup"><span data-stu-id="06381-671">**HPGL2** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCLXL"></span><span id="pclxl"></span>

<span data-ttu-id="06381-672">**PCLXL** (50) </span><span class="sxs-lookup"><span data-stu-id="06381-672">**PCLXL** (50)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06381-673">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="06381-673">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-674">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="06381-674">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06381-675">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-675">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06381-676">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="06381-676">Last error code reported by the logical device.</span></span>

<span data-ttu-id="06381-677">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="06381-677">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="06381-678">**MarkingTechnology**</span><span class="sxs-lookup"><span data-stu-id="06381-678">**MarkingTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-679">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06381-679">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06381-680">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-680">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-681">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 印表機-prtMarkerMarkTech ") </span><span class="sxs-lookup"><span data-stu-id="06381-681">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtMarkerMarkTech")</span></span>
</dt> </dl>

<span data-ttu-id="06381-682">標示印表機所使用的技術。</span><span class="sxs-lookup"><span data-stu-id="06381-682">Marking technology used by the printer.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="06381-683">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="06381-683">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06381-684">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="06381-684">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_LED"></span><span id="electrophotographic_led"></span><span id="ELECTROPHOTOGRAPHIC_LED"></span>

<span data-ttu-id="06381-685">**ELECTROPHOTOGRAPHIC LED** (3) </span><span class="sxs-lookup"><span data-stu-id="06381-685">**Electrophotographic LED** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Laser"></span><span id="electrophotographic_laser"></span><span id="ELECTROPHOTOGRAPHIC_LASER"></span>

<span data-ttu-id="06381-686">**Electrophotographic 鐳射** (4) </span><span class="sxs-lookup"><span data-stu-id="06381-686">**Electrophotographic Laser** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Other"></span><span id="electrophotographic_other"></span><span id="ELECTROPHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="06381-687">**Electrophotographic 其他** (5) </span><span class="sxs-lookup"><span data-stu-id="06381-687">**Electrophotographic Other** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_9pin"></span><span id="impact_moving_head_dot_matrix_9pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_9PIN"></span>

<span data-ttu-id="06381-688">**移動頭部點矩陣 9pin** (6) 的影響</span><span class="sxs-lookup"><span data-stu-id="06381-688">**Impact Moving Head Dot Matrix 9pin** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_24pin"></span><span id="impact_moving_head_dot_matrix_24pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_24PIN"></span>

<span data-ttu-id="06381-689">**移動頭部點矩陣 24pin** (7) 的影響</span><span class="sxs-lookup"><span data-stu-id="06381-689">**Impact Moving Head Dot Matrix 24pin** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_Other"></span><span id="impact_moving_head_dot_matrix_other"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_OTHER"></span>

<span data-ttu-id="06381-690">將 **頭部點矩陣移至其他** (8) 的影響</span><span class="sxs-lookup"><span data-stu-id="06381-690">**Impact Moving Head Dot Matrix Other** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Fully_Formed"></span><span id="impact_moving_head_fully_formed"></span><span id="IMPACT_MOVING_HEAD_FULLY_FORMED"></span>

<span data-ttu-id="06381-691">移動前端 (9) 的 **完整格式影響**</span><span class="sxs-lookup"><span data-stu-id="06381-691">**Impact Moving Head Fully Formed** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Band"></span><span id="impact_band"></span><span id="IMPACT_BAND"></span>

<span data-ttu-id="06381-692">**影響波段** (10) </span><span class="sxs-lookup"><span data-stu-id="06381-692">**Impact Band** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Other"></span><span id="impact_other"></span><span id="IMPACT_OTHER"></span>

<span data-ttu-id="06381-693">**影響其他** (11) </span><span class="sxs-lookup"><span data-stu-id="06381-693">**Impact Other** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Aqueous"></span><span id="inkjet_aqueous"></span><span id="INKJET_AQUEOUS"></span>

<span data-ttu-id="06381-694">**噴墨 Aqueous** (12) </span><span class="sxs-lookup"><span data-stu-id="06381-694">**Inkjet Aqueous** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Solid"></span><span id="inkjet_solid"></span><span id="INKJET_SOLID"></span>

<span data-ttu-id="06381-695">**噴墨** (13) </span><span class="sxs-lookup"><span data-stu-id="06381-695">**Inkjet Solid** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Other"></span><span id="inkjet_other"></span><span id="INKJET_OTHER"></span>

<span data-ttu-id="06381-696">**其他** (14) 的噴墨</span><span class="sxs-lookup"><span data-stu-id="06381-696">**Inkjet Other** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Pen"></span><span id="pen"></span><span id="PEN"></span>

<span data-ttu-id="06381-697">**畫筆** (15) </span><span class="sxs-lookup"><span data-stu-id="06381-697">**Pen** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Transfer"></span><span id="thermal_transfer"></span><span id="THERMAL_TRANSFER"></span>

<span data-ttu-id="06381-698"> (16) 的 **熱傳輸**</span><span class="sxs-lookup"><span data-stu-id="06381-698">**Thermal Transfer** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Sensitive"></span><span id="thermal_sensitive"></span><span id="THERMAL_SENSITIVE"></span>

<span data-ttu-id="06381-699"> (17) 的 **熱機密**</span><span class="sxs-lookup"><span data-stu-id="06381-699">**Thermal Sensitive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Diffusion"></span><span id="thermal_diffusion"></span><span id="THERMAL_DIFFUSION"></span>

<span data-ttu-id="06381-700"> (18) 的 **熱擴散**</span><span class="sxs-lookup"><span data-stu-id="06381-700">**Thermal Diffusion** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Other"></span><span id="thermal_other"></span><span id="THERMAL_OTHER"></span>

<span data-ttu-id="06381-701">**其他熱** (19) </span><span class="sxs-lookup"><span data-stu-id="06381-701">**Thermal Other** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Electroerosion"></span><span id="electroerosion"></span><span id="ELECTROEROSION"></span>

<span data-ttu-id="06381-702">**Electroerosion** (20) </span><span class="sxs-lookup"><span data-stu-id="06381-702">**Electroerosion** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrostatic"></span><span id="electrostatic"></span><span id="ELECTROSTATIC"></span>

<span data-ttu-id="06381-703">**靜電** (21) </span><span class="sxs-lookup"><span data-stu-id="06381-703">**Electrostatic** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Microfiche"></span><span id="photographic_microfiche"></span><span id="PHOTOGRAPHIC_MICROFICHE"></span>

<span data-ttu-id="06381-704">**攝影縮微膠片** (22) </span><span class="sxs-lookup"><span data-stu-id="06381-704">**Photographic Microfiche** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Imagesetter"></span><span id="photographic_imagesetter"></span><span id="PHOTOGRAPHIC_IMAGESETTER"></span>

<span data-ttu-id="06381-705">**攝影照排機** (23) </span><span class="sxs-lookup"><span data-stu-id="06381-705">**Photographic Imagesetter** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Other"></span><span id="photographic_other"></span><span id="PHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="06381-706">**攝影其他** (24) </span><span class="sxs-lookup"><span data-stu-id="06381-706">**Photographic Other** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Ion_Deposition"></span><span id="ion_deposition"></span><span id="ION_DEPOSITION"></span>

<span data-ttu-id="06381-707">**離子 Deposition** (25) </span><span class="sxs-lookup"><span data-stu-id="06381-707">**Ion Deposition** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="eBeam"></span><span id="ebeam"></span><span id="EBEAM"></span>

<span data-ttu-id="06381-708">**eBeam** (26) </span><span class="sxs-lookup"><span data-stu-id="06381-708">**eBeam** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Typesetter"></span><span id="typesetter"></span><span id="TYPESETTER"></span>

<span data-ttu-id="06381-709">**Typesetter** (27) </span><span class="sxs-lookup"><span data-stu-id="06381-709">**Typesetter** (27)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06381-710">**MaxCopies**</span><span class="sxs-lookup"><span data-stu-id="06381-710">**MaxCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-711">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="06381-711">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06381-712">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-712">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-713">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「CIM \_ PrintJob」 ) </span><span class="sxs-lookup"><span data-stu-id="06381-713">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.Copies")</span></span>
</dt> </dl>

<span data-ttu-id="06381-714">印表機可以從單一作業產生的最大複本數目。</span><span class="sxs-lookup"><span data-stu-id="06381-714">Maximum number of copies that can be produced by the printer from a single job.</span></span>

</dd> <dt>

<span data-ttu-id="06381-715">**MaxNumberUp**</span><span class="sxs-lookup"><span data-stu-id="06381-715">**MaxNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-716">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="06381-716">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06381-717">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-717">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-718">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM \_ PrintJob. NumberUp" ) </span><span class="sxs-lookup"><span data-stu-id="06381-718">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.NumberUp")</span></span>
</dt> </dl>

<span data-ttu-id="06381-719">印表機可以轉譯成單一媒體工作表的列印資料流程頁面數目上限。</span><span class="sxs-lookup"><span data-stu-id="06381-719">Maximum number of print-stream pages that the printer can render onto a single media sheet.</span></span>

</dd> <dt>

<span data-ttu-id="06381-720">**MaxSizeSupported**</span><span class="sxs-lookup"><span data-stu-id="06381-720">**MaxSizeSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-721">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="06381-721">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06381-722">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-722">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-723">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM \_ PrintJob. JobSize" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "kb" ) </span><span class="sxs-lookup"><span data-stu-id="06381-723">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.JobSize"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="06381-724">最大的作業 (為位元組資料流程) ，印表機將接受以 kb 為單位的單位。</span><span class="sxs-lookup"><span data-stu-id="06381-724">Largest job (as a byte stream) that the printer will accept in units of kilobytes.</span></span> <span data-ttu-id="06381-725">值為 0 (零) 表示未設定任何限制。</span><span class="sxs-lookup"><span data-stu-id="06381-725">A value of 0 (zero) indicates that no limit has been set.</span></span>

</dd> <dt>

<span data-ttu-id="06381-726">**MimeTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="06381-726">**MimeTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-727">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="06381-727">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="06381-728">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-728">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-729">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 印表機**」。LanguagesSupported "、" CIM \_ PrintJob. mimetype "、" cim \_ PrintService. MimeTypesSupported ") </span><span class="sxs-lookup"><span data-stu-id="06381-729">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.LanguagesSupported", "CIM\_PrintJob.MimeTypes", "CIM\_PrintService.MimeTypesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="06381-730">提供印表機所支援 mime 類型詳細說明的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="06381-730">Free-form strings that provide detailed explanations of mime types that are supported by the printer.</span></span> <span data-ttu-id="06381-731">如果為此屬性提供資料，則值 47 ( "Mime" ) ，應該包含在 **LanguagesSupported** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="06381-731">If data is provided for this property, then the value 47 ("Mime"), should be included in the **LanguagesSupported** property.</span></span>

</dd> <dt>

<span data-ttu-id="06381-732">**名稱**</span><span class="sxs-lookup"><span data-stu-id="06381-732">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-733">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06381-733">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06381-734">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-734">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-735">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="06381-735">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="06381-736">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="06381-736">Label by which the object is known.</span></span> <span data-ttu-id="06381-737">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="06381-737">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="06381-738">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="06381-738">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="06381-739">**NaturalLanguagesSupported**</span><span class="sxs-lookup"><span data-stu-id="06381-739">**NaturalLanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-740">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="06381-740">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="06381-741">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-741">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-742">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| Printer-prtLocalizationLanguage ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ PrintJob. NaturalLanguage ") </span><span class="sxs-lookup"><span data-stu-id="06381-742">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtLocalizationLanguage"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.NaturalLanguage")</span></span>
</dt> </dl>

<span data-ttu-id="06381-743">印表機用於管理資訊輸出之字串的可用語言。</span><span class="sxs-lookup"><span data-stu-id="06381-743">Available languages for strings used by the printer for management information output.</span></span> <span data-ttu-id="06381-744">字串應符合 RFC 1766。</span><span class="sxs-lookup"><span data-stu-id="06381-744">The strings should conform to RFC 1766.</span></span> <span data-ttu-id="06381-745">例如，"en" 用於英文。</span><span class="sxs-lookup"><span data-stu-id="06381-745">For example, "en" is used for English.</span></span>

</dd> <dt>

<span data-ttu-id="06381-746">**PaperSizesSupported**</span><span class="sxs-lookup"><span data-stu-id="06381-746">**PaperSizesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-747">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="06381-747">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="06381-748">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-748">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06381-749">支援的紙張類型。</span><span class="sxs-lookup"><span data-stu-id="06381-749">Types of paper supported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06381-750">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="06381-750">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="06381-751">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="06381-751">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="A"></span><span id="a"></span>

<span data-ttu-id="06381-752">**(2**) </span><span class="sxs-lookup"><span data-stu-id="06381-752">**A** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="B"></span><span id="b"></span>

<span data-ttu-id="06381-753">**B** (3) </span><span class="sxs-lookup"><span data-stu-id="06381-753">**B** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="C"></span><span id="c"></span>

<span data-ttu-id="06381-754">**C** (4) </span><span class="sxs-lookup"><span data-stu-id="06381-754">**C** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="D"></span><span id="d"></span>

<span data-ttu-id="06381-755">**D** (5) </span><span class="sxs-lookup"><span data-stu-id="06381-755">**D** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="E"></span><span id="e"></span>

<span data-ttu-id="06381-756">**E** (6) </span><span class="sxs-lookup"><span data-stu-id="06381-756">**E** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>

<span data-ttu-id="06381-757">**字母** (7) </span><span class="sxs-lookup"><span data-stu-id="06381-757">**Letter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>

<span data-ttu-id="06381-758">**合法** (8) </span><span class="sxs-lookup"><span data-stu-id="06381-758">**Legal** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>

<span data-ttu-id="06381-759">**NA-10x13-信封** (9) </span><span class="sxs-lookup"><span data-stu-id="06381-759">**NA-10x13-Envelope** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>

<span data-ttu-id="06381-760">**NA-9x12-信封** (10) </span><span class="sxs-lookup"><span data-stu-id="06381-760">**NA-9x12-Envelope** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>

<span data-ttu-id="06381-761">**NA-數位-10-信封** (11) </span><span class="sxs-lookup"><span data-stu-id="06381-761">**NA-Number-10-Envelope** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>

<span data-ttu-id="06381-762">**NA-7x9-信封** (12) </span><span class="sxs-lookup"><span data-stu-id="06381-762">**NA-7x9-Envelope** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>

<span data-ttu-id="06381-763">**NA-9x11-信封** (13) </span><span class="sxs-lookup"><span data-stu-id="06381-763">**NA-9x11-Envelope** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>

<span data-ttu-id="06381-764">**NA-10x14-信封** (14) </span><span class="sxs-lookup"><span data-stu-id="06381-764">**NA-10x14-Envelope** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>

<span data-ttu-id="06381-765">**NA-數位-9-信封** (15) </span><span class="sxs-lookup"><span data-stu-id="06381-765">**NA-Number-9-Envelope** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>

<span data-ttu-id="06381-766">**NA-6x9-信封** (16) </span><span class="sxs-lookup"><span data-stu-id="06381-766">**NA-6x9-Envelope** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>

<span data-ttu-id="06381-767">**NA-10x15-信封** (17) </span><span class="sxs-lookup"><span data-stu-id="06381-767">**NA-10x15-Envelope** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="A0"></span><span id="a0"></span>

<span data-ttu-id="06381-768">**A0** (18) </span><span class="sxs-lookup"><span data-stu-id="06381-768">**A0** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="A1"></span><span id="a1"></span>

<span data-ttu-id="06381-769">**A1** (19) </span><span class="sxs-lookup"><span data-stu-id="06381-769">**A1** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="A2"></span><span id="a2"></span>

<span data-ttu-id="06381-770">**A2** (20) </span><span class="sxs-lookup"><span data-stu-id="06381-770">**A2** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="A3"></span><span id="a3"></span>

<span data-ttu-id="06381-771">**A3** (21) </span><span class="sxs-lookup"><span data-stu-id="06381-771">**A3** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="A4"></span><span id="a4"></span>

<span data-ttu-id="06381-772">**A4** (22) </span><span class="sxs-lookup"><span data-stu-id="06381-772">**A4** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="A5"></span><span id="a5"></span>

<span data-ttu-id="06381-773">**A5** (23) </span><span class="sxs-lookup"><span data-stu-id="06381-773">**A5** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="A6"></span><span id="a6"></span>

<span data-ttu-id="06381-774">**A6** (24) </span><span class="sxs-lookup"><span data-stu-id="06381-774">**A6** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="A7"></span><span id="a7"></span>

<span data-ttu-id="06381-775">**A7** (25) </span><span class="sxs-lookup"><span data-stu-id="06381-775">**A7** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="A8"></span><span id="a8"></span>

<span data-ttu-id="06381-776">**A8** (26) </span><span class="sxs-lookup"><span data-stu-id="06381-776">**A8** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="A9A10"></span><span id="a9a10"></span>

<span data-ttu-id="06381-777">**A9A10** (27) </span><span class="sxs-lookup"><span data-stu-id="06381-777">**A9A10** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="B0"></span><span id="b0"></span>

<span data-ttu-id="06381-778">**B0** (28) </span><span class="sxs-lookup"><span data-stu-id="06381-778">**B0** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="B1"></span><span id="b1"></span>

<span data-ttu-id="06381-779">**B1** (29) </span><span class="sxs-lookup"><span data-stu-id="06381-779">**B1** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="B2"></span><span id="b2"></span>

<span data-ttu-id="06381-780">**B2** (30) </span><span class="sxs-lookup"><span data-stu-id="06381-780">**B2** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="B3"></span><span id="b3"></span>

<span data-ttu-id="06381-781">**B3** (31) </span><span class="sxs-lookup"><span data-stu-id="06381-781">**B3** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="B4"></span><span id="b4"></span>

<span data-ttu-id="06381-782">**B4** (32) </span><span class="sxs-lookup"><span data-stu-id="06381-782">**B4** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="B5"></span><span id="b5"></span>

<span data-ttu-id="06381-783">**B5** (33) </span><span class="sxs-lookup"><span data-stu-id="06381-783">**B5** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="B6"></span><span id="b6"></span>

<span data-ttu-id="06381-784">**B6** (34) </span><span class="sxs-lookup"><span data-stu-id="06381-784">**B6** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="B7"></span><span id="b7"></span>

<span data-ttu-id="06381-785">**B7** (35) </span><span class="sxs-lookup"><span data-stu-id="06381-785">**B7** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="B8"></span><span id="b8"></span>

<span data-ttu-id="06381-786">**B8** (36) </span><span class="sxs-lookup"><span data-stu-id="06381-786">**B8** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="B9"></span><span id="b9"></span>

<span data-ttu-id="06381-787">**B9** (37) </span><span class="sxs-lookup"><span data-stu-id="06381-787">**B9** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="B10"></span><span id="b10"></span>

<span data-ttu-id="06381-788">**B10** (38) </span><span class="sxs-lookup"><span data-stu-id="06381-788">**B10** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="C0"></span><span id="c0"></span>

<span data-ttu-id="06381-789">**C0** (39) </span><span class="sxs-lookup"><span data-stu-id="06381-789">**C0** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="C1"></span><span id="c1"></span>

<span data-ttu-id="06381-790">**C1** (40) </span><span class="sxs-lookup"><span data-stu-id="06381-790">**C1** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="C2C3"></span><span id="c2c3"></span>

<span data-ttu-id="06381-791">**C2C3** (41) </span><span class="sxs-lookup"><span data-stu-id="06381-791">**C2C3** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="C4"></span><span id="c4"></span>

<span data-ttu-id="06381-792">**C4** (42) </span><span class="sxs-lookup"><span data-stu-id="06381-792">**C4** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="C5"></span><span id="c5"></span>

<span data-ttu-id="06381-793">**C5** (43) </span><span class="sxs-lookup"><span data-stu-id="06381-793">**C5** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="C6"></span><span id="c6"></span>

<span data-ttu-id="06381-794">**C6** (44) </span><span class="sxs-lookup"><span data-stu-id="06381-794">**C6** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="C7"></span><span id="c7"></span>

<span data-ttu-id="06381-795">**C7** (45) </span><span class="sxs-lookup"><span data-stu-id="06381-795">**C7** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="C8"></span><span id="c8"></span>

<span data-ttu-id="06381-796">**C8** (46) </span><span class="sxs-lookup"><span data-stu-id="06381-796">**C8** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>

<span data-ttu-id="06381-797">**ISO-指定** (47) </span><span class="sxs-lookup"><span data-stu-id="06381-797">**ISO-Designated** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B0"></span><span id="jis_b0"></span>

<span data-ttu-id="06381-798">**JIS B0** (48) </span><span class="sxs-lookup"><span data-stu-id="06381-798">**JIS B0** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B1"></span><span id="jis_b1"></span>

<span data-ttu-id="06381-799">**JIS B1** (49) </span><span class="sxs-lookup"><span data-stu-id="06381-799">**JIS B1** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B2"></span><span id="jis_b2"></span>

<span data-ttu-id="06381-800">**JIS B2** (50) </span><span class="sxs-lookup"><span data-stu-id="06381-800">**JIS B2** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B3"></span><span id="jis_b3"></span>

<span data-ttu-id="06381-801">**JIS B3** (51) </span><span class="sxs-lookup"><span data-stu-id="06381-801">**JIS B3** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B4"></span><span id="jis_b4"></span>

<span data-ttu-id="06381-802">**JIS B4** (52) </span><span class="sxs-lookup"><span data-stu-id="06381-802">**JIS B4** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B5"></span><span id="jis_b5"></span>

<span data-ttu-id="06381-803">**JIS B5** (53) </span><span class="sxs-lookup"><span data-stu-id="06381-803">**JIS B5** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B6"></span><span id="jis_b6"></span>

<span data-ttu-id="06381-804">**JIS B6** (54) </span><span class="sxs-lookup"><span data-stu-id="06381-804">**JIS B6** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B7"></span><span id="jis_b7"></span>

<span data-ttu-id="06381-805">**JIS B7** (55) </span><span class="sxs-lookup"><span data-stu-id="06381-805">**JIS B7** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B8"></span><span id="jis_b8"></span>

<span data-ttu-id="06381-806">**JIS B8** (56) </span><span class="sxs-lookup"><span data-stu-id="06381-806">**JIS B8** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B9"></span><span id="jis_b9"></span>

<span data-ttu-id="06381-807">**JIS B9** (57) </span><span class="sxs-lookup"><span data-stu-id="06381-807">**JIS B9** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B10"></span><span id="jis_b10"></span>

<span data-ttu-id="06381-808">**JIS B10** (58) </span><span class="sxs-lookup"><span data-stu-id="06381-808">**JIS B10** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>

<span data-ttu-id="06381-809">**NA-字母** (59) </span><span class="sxs-lookup"><span data-stu-id="06381-809">**NA-Letter** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>

<span data-ttu-id="06381-810">**NA-合法** (60) </span><span class="sxs-lookup"><span data-stu-id="06381-810">**NA-Legal** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>

<span data-ttu-id="06381-811">**B4-信封** (61) </span><span class="sxs-lookup"><span data-stu-id="06381-811">**B4-Envelope** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>

<span data-ttu-id="06381-812">**B5-信封** (62) </span><span class="sxs-lookup"><span data-stu-id="06381-812">**B5-Envelope** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>

<span data-ttu-id="06381-813">**C3-信封** (63) </span><span class="sxs-lookup"><span data-stu-id="06381-813">**C3-Envelope** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>

<span data-ttu-id="06381-814">**C4-信封** (64) </span><span class="sxs-lookup"><span data-stu-id="06381-814">**C4-Envelope** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>

<span data-ttu-id="06381-815">**C5-信封** (65) </span><span class="sxs-lookup"><span data-stu-id="06381-815">**C5-Envelope** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>

<span data-ttu-id="06381-816">**C6-信封** (66) </span><span class="sxs-lookup"><span data-stu-id="06381-816">**C6-Envelope** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>

<span data-ttu-id="06381-817">**指定-長信封** (67) </span><span class="sxs-lookup"><span data-stu-id="06381-817">**Designated-Long-Envelope** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>

<span data-ttu-id="06381-818">**Monarch-信封** (68) </span><span class="sxs-lookup"><span data-stu-id="06381-818">**Monarch-Envelope** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="06381-819">**Executive** (69) </span><span class="sxs-lookup"><span data-stu-id="06381-819">**Executive** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>

<span data-ttu-id="06381-820"> (70) 的 **對開**</span><span class="sxs-lookup"><span data-stu-id="06381-820">**Folio** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>

<span data-ttu-id="06381-821">**發票** (71) </span><span class="sxs-lookup"><span data-stu-id="06381-821">**Invoice** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>

<span data-ttu-id="06381-822">**總帳** (72) </span><span class="sxs-lookup"><span data-stu-id="06381-822">**Ledger** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>

<span data-ttu-id="06381-823">**Quarto** (73) </span><span class="sxs-lookup"><span data-stu-id="06381-823">**Quarto** (73)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06381-824">**PaperTypesAvailable**</span><span class="sxs-lookup"><span data-stu-id="06381-824">**PaperTypesAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-825">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="06381-825">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="06381-826">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-826">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-827">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**MODELCORRESPONDENCE**](/windows/desktop/WmiSdk/standard-qualifiers) ( "cim \_ PrintJob. RequiredPaperType"，"cim \_ PrintService. PaperTypesAvailable" ) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 印表機-prtInputMediaName ") </span><span class="sxs-lookup"><span data-stu-id="06381-827">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.RequiredPaperType", "CIM\_PrintService.PaperTypesAvailable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtInputMediaName")</span></span>
</dt> </dl>

<span data-ttu-id="06381-828">自由格式的字串，可指定印表機目前可用的紙張類型。</span><span class="sxs-lookup"><span data-stu-id="06381-828">Free-form strings that specify the types of paper that are currently available for the printer.</span></span> <span data-ttu-id="06381-829">每個字串應該以 ISO/IEC 10175 檔列印應用程式所指定的格式來表示 (DPA) ，也會在 RFC 1759 (印表機 MIB) 的附錄 C 中摘要說明。</span><span class="sxs-lookup"><span data-stu-id="06381-829">Each string should be expressed in the form specified by ISO/IEC 10175 Document Printing Application (DPA), which is also summarized in Appendix C of RFC 1759 (Printer MIB).</span></span> <span data-ttu-id="06381-830">有效字串的範例為 "iso-a4-彩色" 和 "na-10x14-信封"。</span><span class="sxs-lookup"><span data-stu-id="06381-830">Examples of valid strings are "iso-a4-colored" and "na-10x14-envelope".</span></span> <span data-ttu-id="06381-831">根據定義， **PaperTypesAvailable** 屬性中所列的紙張大小應該也會出現在 **PaperSizesSupported** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="06381-831">By definition, a paper size that is available and listed in the **PaperTypesAvailable** property should also appear in the **PaperSizesSupported** property.</span></span>

</dd> <dt>

<span data-ttu-id="06381-832">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="06381-832">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-833">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06381-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06381-834">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-834">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-835">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="06381-835">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="06381-836">邏輯裝置的 Win32 隨插即用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="06381-836">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="06381-837">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="06381-837">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="06381-838">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="06381-838">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="06381-839">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="06381-839">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-840">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="06381-840">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="06381-841">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-841">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06381-842">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="06381-842">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="06381-843">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="06381-843">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06381-844"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="06381-844"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="06381-845"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="06381-845"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="06381-846"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="06381-846"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="06381-847"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="06381-847"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="06381-848">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="06381-848">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="06381-849"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="06381-849"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="06381-850">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="06381-850">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="06381-851"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="06381-851"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="06381-852">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="06381-852">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="06381-853">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="06381-853">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="06381-854">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="06381-854">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="06381-855"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="06381-855"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="06381-856">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="06381-856">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="06381-857"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="06381-857"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="06381-858">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="06381-858">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="06381-859">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="06381-859">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-860">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="06381-860">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06381-861">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-861">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06381-862">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="06381-862">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="06381-863">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="06381-863">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="06381-864">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="06381-864">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="06381-865">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="06381-865">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="06381-866">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="06381-866">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="06381-867">**PrinterStatus**</span><span class="sxs-lookup"><span data-stu-id="06381-867">**PrinterStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-868">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06381-868">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06381-869">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-869">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-870">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 印表機-hrPrinterStatus ") </span><span class="sxs-lookup"><span data-stu-id="06381-870">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.hrPrinterStatus")</span></span>
</dt> </dl>

<span data-ttu-id="06381-871">印表機的狀態資訊（ **可用性** 屬性中指定的以外）。</span><span class="sxs-lookup"><span data-stu-id="06381-871">Status information, beyond that specified in the **Availability** property, for a printer.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="06381-872">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="06381-872">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06381-873">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="06381-873">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="06381-874">**閒置** (3) </span><span class="sxs-lookup"><span data-stu-id="06381-874">**Idle** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>

<span data-ttu-id="06381-875">**列印** (4) </span><span class="sxs-lookup"><span data-stu-id="06381-875">**Printing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>

<span data-ttu-id="06381-876">**預熱** (5) </span><span class="sxs-lookup"><span data-stu-id="06381-876">**Warmup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>

<span data-ttu-id="06381-877">**已停止列印** (6) </span><span class="sxs-lookup"><span data-stu-id="06381-877">**Stopped Printing** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="06381-878">**離線** (7) </span><span class="sxs-lookup"><span data-stu-id="06381-878">**Offline** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06381-879">**狀態**</span><span class="sxs-lookup"><span data-stu-id="06381-879">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-880">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06381-880">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06381-881">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-881">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-882">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="06381-882">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="06381-883">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="06381-883">Current status of the object.</span></span> <span data-ttu-id="06381-884">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="06381-884">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="06381-885">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="06381-885">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="06381-886">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="06381-886">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="06381-887">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="06381-887">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="06381-888">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="06381-888">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06381-889">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="06381-889">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="06381-890">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="06381-890">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="06381-891">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="06381-891">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="06381-892">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="06381-892">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="06381-893">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="06381-893">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="06381-894">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="06381-894">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="06381-895">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="06381-895">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="06381-896">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="06381-896">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="06381-897">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="06381-897">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06381-898">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="06381-898">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-899">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06381-899">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06381-900">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-900">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-901">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="06381-901">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="06381-902">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="06381-902">State of the logical device.</span></span> <span data-ttu-id="06381-903">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="06381-903">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="06381-904">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="06381-904">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="06381-905">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="06381-905">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06381-906">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="06381-906">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="06381-907">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="06381-907">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="06381-908">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="06381-908">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="06381-909">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="06381-909">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06381-910">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="06381-910">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-911">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06381-911">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06381-912">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-912">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-913">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="06381-913">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="06381-914">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="06381-914">Scoping system's creation class name.</span></span>

<span data-ttu-id="06381-915">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="06381-915">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="06381-916">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="06381-916">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-917">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06381-917">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06381-918">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-918">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-919">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="06381-919">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="06381-920">設定系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="06381-920">Scoping system's name.</span></span>

<span data-ttu-id="06381-921">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="06381-921">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="06381-922">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="06381-922">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-923">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="06381-923">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="06381-924">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-924">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06381-925">上次重設印表機的時間。</span><span class="sxs-lookup"><span data-stu-id="06381-925">Time of last printer reset.</span></span>

</dd> <dt>

<span data-ttu-id="06381-926">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="06381-926">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06381-927">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="06381-927">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06381-928">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06381-928">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06381-929">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM \_ PrintJob. HorizontalResolution" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "圖元/英寸" ) </span><span class="sxs-lookup"><span data-stu-id="06381-929">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="06381-930">垂直解析度（以圖元為單位）-每英寸。</span><span class="sxs-lookup"><span data-stu-id="06381-930">Vertical resolution in pixels-per-inch.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06381-931">備註</span><span class="sxs-lookup"><span data-stu-id="06381-931">Remarks</span></span>

<span data-ttu-id="06381-932">**Cim \_ 印表機** 類別衍生自 [**cim \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="06381-932">The **CIM\_Printer** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="06381-933">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="06381-933">WMI does not implement this class.</span></span> <span data-ttu-id="06381-934">針對衍生自 **CIM \_ 印表機** 的 WMI 歸類，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="06381-934">For WMI classed derived from **CIM\_Printer**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="06381-935">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="06381-935">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="06381-936">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="06381-936">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="06381-937">規格需求</span><span class="sxs-lookup"><span data-stu-id="06381-937">Requirements</span></span>



| <span data-ttu-id="06381-938">需求</span><span class="sxs-lookup"><span data-stu-id="06381-938">Requirement</span></span> | <span data-ttu-id="06381-939">值</span><span class="sxs-lookup"><span data-stu-id="06381-939">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06381-940">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="06381-940">Minimum supported client</span></span><br/> | <span data-ttu-id="06381-941">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06381-941">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="06381-942">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="06381-942">Minimum supported server</span></span><br/> | <span data-ttu-id="06381-943">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06381-943">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="06381-944">命名空間</span><span class="sxs-lookup"><span data-stu-id="06381-944">Namespace</span></span><br/>                | <span data-ttu-id="06381-945">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="06381-945">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="06381-946">MOF</span><span class="sxs-lookup"><span data-stu-id="06381-946">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06381-947"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="06381-947"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="06381-948">DLL</span><span class="sxs-lookup"><span data-stu-id="06381-948">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06381-949"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06381-949"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06381-950">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06381-950">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06381-951">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="06381-951">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

