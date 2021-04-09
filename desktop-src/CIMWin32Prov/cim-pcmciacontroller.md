---
description: CIM \_ PCMCIAController 類別代表個人電腦記憶卡國際協會 (PCMCIA) 控制器的功能和管理。
ms.assetid: 341cbc6c-dd25-4dea-bcce-cd4e3f4d5324
ms.tgt_platform: multiple
title: CIM_PCMCIAController 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCMCIAController
- CIM_PCMCIAController.Availability
- CIM_PCMCIAController.Caption
- CIM_PCMCIAController.ConfigManagerErrorCode
- CIM_PCMCIAController.ConfigManagerUserConfig
- CIM_PCMCIAController.CreationClassName
- CIM_PCMCIAController.Description
- CIM_PCMCIAController.DeviceID
- CIM_PCMCIAController.ErrorCleared
- CIM_PCMCIAController.ErrorDescription
- CIM_PCMCIAController.InstallDate
- CIM_PCMCIAController.LastErrorCode
- CIM_PCMCIAController.Manufacturer
- CIM_PCMCIAController.MaxNumberControlled
- CIM_PCMCIAController.Name
- CIM_PCMCIAController.PNPDeviceID
- CIM_PCMCIAController.PowerManagementCapabilities
- CIM_PCMCIAController.PowerManagementSupported
- CIM_PCMCIAController.ProtocolSupported
- CIM_PCMCIAController.Status
- CIM_PCMCIAController.StatusInfo
- CIM_PCMCIAController.SystemCreationClassName
- CIM_PCMCIAController.SystemName
- CIM_PCMCIAController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 95d05e11dd0c439708c477e3ec776bc7a2c333d7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110525"
---
# <a name="cim_pcmciacontroller-class"></a><span data-ttu-id="f95ff-103">CIM \_ PCMCIAController 類別</span><span class="sxs-lookup"><span data-stu-id="f95ff-103">CIM\_PCMCIAController class</span></span>

<span data-ttu-id="f95ff-104">**CIM \_ PCMCIAController** 類別代表個人電腦記憶卡國際協會 (PCMCIA) 控制器的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="f95ff-104">The **CIM\_PCMCIAController** class represents the capabilities and management of a Personal Computer Memory Card International Association (PCMCIA) controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f95ff-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="f95ff-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f95ff-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="f95ff-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f95ff-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f95ff-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f95ff-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="f95ff-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f95ff-109">語法</span><span class="sxs-lookup"><span data-stu-id="f95ff-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B5A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PCMCIAController : cim_controller
{
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
  string   Manufacturer;
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

## <a name="members"></a><span data-ttu-id="f95ff-110">成員</span><span class="sxs-lookup"><span data-stu-id="f95ff-110">Members</span></span>

<span data-ttu-id="f95ff-111">**CIM \_ PCMCIAController** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f95ff-111">The **CIM\_PCMCIAController** class has these types of members:</span></span>

-   [<span data-ttu-id="f95ff-112">方法</span><span class="sxs-lookup"><span data-stu-id="f95ff-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="f95ff-113">屬性</span><span class="sxs-lookup"><span data-stu-id="f95ff-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f95ff-114">方法</span><span class="sxs-lookup"><span data-stu-id="f95ff-114">Methods</span></span>

<span data-ttu-id="f95ff-115">**CIM \_ PCMCIAController** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="f95ff-115">The **CIM\_PCMCIAController** class has these methods.</span></span>



| <span data-ttu-id="f95ff-116">方法</span><span class="sxs-lookup"><span data-stu-id="f95ff-116">Method</span></span>                                                                      | <span data-ttu-id="f95ff-117">描述</span><span class="sxs-lookup"><span data-stu-id="f95ff-117">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f95ff-118">**重設**</span><span class="sxs-lookup"><span data-stu-id="f95ff-118">**Reset**</span></span>](reset-method-in-class-cim-pcmciacontroller.md)                 | <span data-ttu-id="f95ff-119">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="f95ff-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="f95ff-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="f95ff-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="f95ff-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="f95ff-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-pcmciacontroller.md) | <span data-ttu-id="f95ff-122">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="f95ff-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="f95ff-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="f95ff-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f95ff-124">屬性</span><span class="sxs-lookup"><span data-stu-id="f95ff-124">Properties</span></span>

<span data-ttu-id="f95ff-125">**CIM \_ PCMCIAController** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f95ff-125">The **CIM\_PCMCIAController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f95ff-126">**可用性**</span><span class="sxs-lookup"><span data-stu-id="f95ff-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f95ff-127">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f95ff-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f95ff-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-129">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="f95ff-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="f95ff-130">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="f95ff-130">Availability and status of the device.</span></span> <span data-ttu-id="f95ff-131">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f95ff-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f95ff-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="f95ff-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-133">其他。</span><span class="sxs-lookup"><span data-stu-id="f95ff-133">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f95ff-134"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="f95ff-134"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-135">不明。</span><span class="sxs-lookup"><span data-stu-id="f95ff-135">Unknown.</span></span>

</dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="f95ff-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="f95ff-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-137">執行中或全電源。</span><span class="sxs-lookup"><span data-stu-id="f95ff-137">Running or full power.</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="f95ff-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="f95ff-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-139">警告。</span><span class="sxs-lookup"><span data-stu-id="f95ff-139">Warning.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="f95ff-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="f95ff-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-141">測試。</span><span class="sxs-lookup"><span data-stu-id="f95ff-141">Testing.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f95ff-142"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="f95ff-142"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-143">不適用。</span><span class="sxs-lookup"><span data-stu-id="f95ff-143">Not applicable.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="f95ff-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="f95ff-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-145">關閉電源。</span><span class="sxs-lookup"><span data-stu-id="f95ff-145">Power off.</span></span>

</dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="f95ff-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="f95ff-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-147">離線。</span><span class="sxs-lookup"><span data-stu-id="f95ff-147">Offline.</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="f95ff-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="f95ff-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-149">關閉責任。</span><span class="sxs-lookup"><span data-stu-id="f95ff-149">Off duty.</span></span>

</dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f95ff-150"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="f95ff-150"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-151">已降級。</span><span class="sxs-lookup"><span data-stu-id="f95ff-151">Degraded.</span></span>

</dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="f95ff-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="f95ff-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-153">未安裝。</span><span class="sxs-lookup"><span data-stu-id="f95ff-153">Not installed.</span></span>

</dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="f95ff-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="f95ff-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-155">安裝錯誤。</span><span class="sxs-lookup"><span data-stu-id="f95ff-155">Install error.</span></span>

</dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="f95ff-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="f95ff-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-157">裝置已知處於省電模式，但在此模式中的確切狀態是未知的。</span><span class="sxs-lookup"><span data-stu-id="f95ff-157">Device is known to be in a power save mode, but its exact status in this mode is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="f95ff-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="f95ff-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-159">裝置處於省電狀態，但仍在運作中，而且可能會顯示效能下降。</span><span class="sxs-lookup"><span data-stu-id="f95ff-159">Device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="f95ff-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="f95ff-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-161">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="f95ff-161">Device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="f95ff-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="f95ff-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-163">電源週期。</span><span class="sxs-lookup"><span data-stu-id="f95ff-163">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="f95ff-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="f95ff-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-165">裝置處於警告狀態，也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="f95ff-165">Device is in a warning state and also in a power-save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="f95ff-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="f95ff-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-167">已暫停。</span><span class="sxs-lookup"><span data-stu-id="f95ff-167">Paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="f95ff-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="f95ff-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-169">未就緒。</span><span class="sxs-lookup"><span data-stu-id="f95ff-169">Not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="f95ff-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="f95ff-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-171">尚未設定。</span><span class="sxs-lookup"><span data-stu-id="f95ff-171">Not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="f95ff-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="f95ff-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-173">PCMCIA 控制器無法使用。</span><span class="sxs-lookup"><span data-stu-id="f95ff-173">The PCMCIA controller is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f95ff-174">**標題**</span><span class="sxs-lookup"><span data-stu-id="f95ff-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f95ff-175">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f95ff-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f95ff-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-177">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="f95ff-177">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f95ff-178">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="f95ff-178">Short textual description of the object.</span></span>

<span data-ttu-id="f95ff-179">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f95ff-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f95ff-180">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f95ff-180">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f95ff-181">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f95ff-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f95ff-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-183">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="f95ff-183">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f95ff-184">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f95ff-184">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="f95ff-185">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f95ff-185">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="f95ff-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="f95ff-187"> (0)</span><span class="sxs-lookup"><span data-stu-id="f95ff-187">(0)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-188">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="f95ff-188">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="f95ff-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="f95ff-190">(1)</span><span class="sxs-lookup"><span data-stu-id="f95ff-190">(1)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-191">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="f95ff-191">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f95ff-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="f95ff-193">(2)</span><span class="sxs-lookup"><span data-stu-id="f95ff-193">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="f95ff-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="f95ff-195">(3)</span><span class="sxs-lookup"><span data-stu-id="f95ff-195">(3)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-196">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="f95ff-196">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f95ff-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="f95ff-198">(4)</span><span class="sxs-lookup"><span data-stu-id="f95ff-198">(4)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-199">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="f95ff-199">Device is not working properly.</span></span> <span data-ttu-id="f95ff-200">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="f95ff-200">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="f95ff-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="f95ff-202">(5)</span><span class="sxs-lookup"><span data-stu-id="f95ff-202">(5)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-203">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="f95ff-203">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="f95ff-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="f95ff-205">(6)</span><span class="sxs-lookup"><span data-stu-id="f95ff-205">(6)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-206">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="f95ff-206">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="f95ff-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="f95ff-208">(7)</span><span class="sxs-lookup"><span data-stu-id="f95ff-208">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="f95ff-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="f95ff-210">(8)</span><span class="sxs-lookup"><span data-stu-id="f95ff-210">(8)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-211">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="f95ff-211">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="f95ff-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="f95ff-213">(9)</span><span class="sxs-lookup"><span data-stu-id="f95ff-213">(9)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-214">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="f95ff-214">Device is not working properly.</span></span> <span data-ttu-id="f95ff-215">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="f95ff-215">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="f95ff-216"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-216"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="f95ff-217">(10)</span><span class="sxs-lookup"><span data-stu-id="f95ff-217">(10)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-218">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="f95ff-218">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="f95ff-219"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-219"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="f95ff-220">(11)</span><span class="sxs-lookup"><span data-stu-id="f95ff-220">(11)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-221">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="f95ff-221">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="f95ff-222"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-222"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="f95ff-223"> (12) </span><span class="sxs-lookup"><span data-stu-id="f95ff-223">(12)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-224">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="f95ff-224">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="f95ff-225"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-225"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="f95ff-226">(13)</span><span class="sxs-lookup"><span data-stu-id="f95ff-226">(13)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-227">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="f95ff-227">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="f95ff-228"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-228"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="f95ff-229">(14)</span><span class="sxs-lookup"><span data-stu-id="f95ff-229">(14)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-230">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="f95ff-230">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="f95ff-231"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-231"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="f95ff-232">(15)</span><span class="sxs-lookup"><span data-stu-id="f95ff-232">(15)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-233">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="f95ff-233">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="f95ff-234"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-234"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="f95ff-235">(16)</span><span class="sxs-lookup"><span data-stu-id="f95ff-235">(16)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-236">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="f95ff-236">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="f95ff-237"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-237"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="f95ff-238">(17)</span><span class="sxs-lookup"><span data-stu-id="f95ff-238">(17)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-239">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="f95ff-239">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f95ff-240"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-240"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="f95ff-241">(18)</span><span class="sxs-lookup"><span data-stu-id="f95ff-241">(18)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-242">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="f95ff-242">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="f95ff-243"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-243"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="f95ff-244">(19)</span><span class="sxs-lookup"><span data-stu-id="f95ff-244">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f95ff-245"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-245"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="f95ff-246">(20)</span><span class="sxs-lookup"><span data-stu-id="f95ff-246">(20)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-247">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="f95ff-247">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="f95ff-248"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-248"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="f95ff-249">(21)</span><span class="sxs-lookup"><span data-stu-id="f95ff-249">(21)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-250">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="f95ff-250">System failure.</span></span> <span data-ttu-id="f95ff-251">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="f95ff-251">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="f95ff-252">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="f95ff-252">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="f95ff-253"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-253"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="f95ff-254">(22)</span><span class="sxs-lookup"><span data-stu-id="f95ff-254">(22)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-255">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="f95ff-255">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="f95ff-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="f95ff-257">(23)</span><span class="sxs-lookup"><span data-stu-id="f95ff-257">(23)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-258">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="f95ff-258">System failure.</span></span> <span data-ttu-id="f95ff-259">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="f95ff-259">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="f95ff-260"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-260"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="f95ff-261">(24)</span><span class="sxs-lookup"><span data-stu-id="f95ff-261">(24)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-262">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="f95ff-262">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f95ff-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="f95ff-264">(25)</span><span class="sxs-lookup"><span data-stu-id="f95ff-264">(25)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-265">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="f95ff-265">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f95ff-266"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-266"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="f95ff-267">(26)</span><span class="sxs-lookup"><span data-stu-id="f95ff-267">(26)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-268">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="f95ff-268">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="f95ff-269"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-269"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="f95ff-270">(27)</span><span class="sxs-lookup"><span data-stu-id="f95ff-270">(27)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-271">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="f95ff-271">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="f95ff-272"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-272"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="f95ff-273">(28)</span><span class="sxs-lookup"><span data-stu-id="f95ff-273">(28)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-274">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="f95ff-274">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="f95ff-275"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-275"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="f95ff-276">(29)</span><span class="sxs-lookup"><span data-stu-id="f95ff-276">(29)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-277">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="f95ff-277">Device is disabled.</span></span> <span data-ttu-id="f95ff-278">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="f95ff-278">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="f95ff-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="f95ff-280">(30)</span><span class="sxs-lookup"><span data-stu-id="f95ff-280">(30)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-281">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="f95ff-281">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f95ff-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="f95ff-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="f95ff-283"> (31) </span><span class="sxs-lookup"><span data-stu-id="f95ff-283">(31)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-284">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="f95ff-284">Device is not working properly.</span></span> <span data-ttu-id="f95ff-285">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="f95ff-285">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f95ff-286">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="f95ff-286">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f95ff-287">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f95ff-287">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-288">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f95ff-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-289">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="f95ff-289">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f95ff-290">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="f95ff-290">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="f95ff-291">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f95ff-291">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f95ff-292">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f95ff-292">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f95ff-293">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f95ff-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-294">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f95ff-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-295">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f95ff-295">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f95ff-296">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="f95ff-296">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f95ff-297">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="f95ff-297">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f95ff-298">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f95ff-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f95ff-299">**說明**</span><span class="sxs-lookup"><span data-stu-id="f95ff-299">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f95ff-300">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f95ff-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-301">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f95ff-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-302">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="f95ff-302">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f95ff-303">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="f95ff-303">Textual description of the object.</span></span>

<span data-ttu-id="f95ff-304">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f95ff-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f95ff-305">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="f95ff-305">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f95ff-306">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f95ff-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-307">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f95ff-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-308">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f95ff-308">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f95ff-309">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="f95ff-309">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="f95ff-310">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f95ff-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f95ff-311">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="f95ff-311">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f95ff-312">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f95ff-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-313">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f95ff-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f95ff-314">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="f95ff-314">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="f95ff-315">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f95ff-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f95ff-316">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f95ff-316">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f95ff-317">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f95ff-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-318">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f95ff-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f95ff-319">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="f95ff-319">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="f95ff-320">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f95ff-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f95ff-321">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f95ff-321">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f95ff-322">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="f95ff-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-323">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f95ff-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-324">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="f95ff-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f95ff-325">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="f95ff-325">Date and time the object was installed.</span></span> <span data-ttu-id="f95ff-326">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="f95ff-326">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="f95ff-327">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f95ff-327">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f95ff-328">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f95ff-328">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f95ff-329">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f95ff-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-330">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f95ff-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f95ff-331">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f95ff-331">Last error code reported by the logical device.</span></span>

<span data-ttu-id="f95ff-332">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f95ff-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f95ff-333">**製造商**</span><span class="sxs-lookup"><span data-stu-id="f95ff-333">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f95ff-334">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f95ff-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-335">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f95ff-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-336">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="f95ff-336">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f95ff-337">PCMCIA 控制器製造商的名稱。</span><span class="sxs-lookup"><span data-stu-id="f95ff-337">Name of the PCMCIA controller manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="f95ff-338">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="f95ff-338">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f95ff-339">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f95ff-339">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-340">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f95ff-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-341">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 匯流排埠 \| 001.9 ") </span><span class="sxs-lookup"><span data-stu-id="f95ff-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="f95ff-342">控制器支援的直接可定址實體數目上限。</span><span class="sxs-lookup"><span data-stu-id="f95ff-342">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="f95ff-343">如果數位為未知或無限制，則應使用0值。</span><span class="sxs-lookup"><span data-stu-id="f95ff-343">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="f95ff-344">這個屬性繼承自 [**CIM \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="f95ff-344">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="f95ff-345">**名稱**</span><span class="sxs-lookup"><span data-stu-id="f95ff-345">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f95ff-346">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f95ff-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-347">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f95ff-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-348">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="f95ff-348">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f95ff-349">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="f95ff-349">Label by which the object is known.</span></span> <span data-ttu-id="f95ff-350">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="f95ff-350">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="f95ff-351">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f95ff-351">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f95ff-352">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="f95ff-352">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f95ff-353">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f95ff-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-354">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f95ff-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-355">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="f95ff-355">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f95ff-356">邏輯裝置的 Win32 隨插即用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="f95ff-356">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="f95ff-357">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f95ff-357">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="f95ff-358">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="f95ff-358">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="f95ff-359">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f95ff-359">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f95ff-360">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="f95ff-360">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-361">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f95ff-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f95ff-362">邏輯裝置的特定電源相關功能。</span><span class="sxs-lookup"><span data-stu-id="f95ff-362">Specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="f95ff-363">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f95ff-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f95ff-364"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="f95ff-364"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-365">不明。</span><span class="sxs-lookup"><span data-stu-id="f95ff-365">Unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="f95ff-366"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="f95ff-366"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-367">不支援。</span><span class="sxs-lookup"><span data-stu-id="f95ff-367">Not supported.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f95ff-368"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="f95ff-368"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-369">停用。</span><span class="sxs-lookup"><span data-stu-id="f95ff-369">Disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f95ff-370"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="f95ff-370"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-371">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="f95ff-371">Power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="f95ff-372"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="f95ff-372"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-373">裝置可以根據使用或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="f95ff-373">Device can change its power state based on use or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="f95ff-374"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="f95ff-374"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-375">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="f95ff-375">The [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) method is supported.</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="f95ff-376"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="f95ff-376"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-377">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) 。</span><span class="sxs-lookup"><span data-stu-id="f95ff-377">The [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="f95ff-378"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="f95ff-378"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f95ff-379">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) ，並將 *時間* 參數設定為特定日期和時間（或間隔），以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="f95ff-379">The [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f95ff-380">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="f95ff-380">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f95ff-381">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f95ff-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-382">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f95ff-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f95ff-383">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="f95ff-383">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="f95ff-384">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="f95ff-384">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="f95ff-385">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="f95ff-385">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="f95ff-386">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="f95ff-386">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="f95ff-387">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f95ff-387">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f95ff-388">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="f95ff-388">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f95ff-389">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f95ff-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-390">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f95ff-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-391">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 匯流排埠 \| 001.2 "，" MIF。DMTF \| 磁片 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="f95ff-391">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="f95ff-392">控制器用來存取「受控制」裝置的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f95ff-392">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="f95ff-393">這個屬性繼承自 [**CIM \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="f95ff-393">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="f95ff-394">值為：</span><span class="sxs-lookup"><span data-stu-id="f95ff-394">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f95ff-395">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="f95ff-395">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f95ff-396">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="f95ff-396">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="f95ff-397">**EISA** (3) </span><span class="sxs-lookup"><span data-stu-id="f95ff-397">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="f95ff-398">**ISA** (4) </span><span class="sxs-lookup"><span data-stu-id="f95ff-398">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="f95ff-399">**PCI** (5) </span><span class="sxs-lookup"><span data-stu-id="f95ff-399">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="f95ff-400">**ATA/ATAPI** (6) </span><span class="sxs-lookup"><span data-stu-id="f95ff-400">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="f95ff-401">**彈性磁片** (7) </span><span class="sxs-lookup"><span data-stu-id="f95ff-401">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="f95ff-402">**1496** (8) </span><span class="sxs-lookup"><span data-stu-id="f95ff-402">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="f95ff-403">**SCSI 平行介面** (9) </span><span class="sxs-lookup"><span data-stu-id="f95ff-403">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="f95ff-404">**SCSI 光纖通道通訊協定** (10) </span><span class="sxs-lookup"><span data-stu-id="f95ff-404">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="f95ff-405">**SCSI 序列匯流排通訊協定** (11) </span><span class="sxs-lookup"><span data-stu-id="f95ff-405">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="f95ff-406">**SCSI 序列匯流排通訊協定-2 (1394)** (12) </span><span class="sxs-lookup"><span data-stu-id="f95ff-406">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="f95ff-407">**SCSI 序列儲存架構** (13) </span><span class="sxs-lookup"><span data-stu-id="f95ff-407">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="f95ff-408">**VESA** (14) </span><span class="sxs-lookup"><span data-stu-id="f95ff-408">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="f95ff-409">**PCMCIA** (15) </span><span class="sxs-lookup"><span data-stu-id="f95ff-409">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="f95ff-410">**通用序列匯流排** (16) </span><span class="sxs-lookup"><span data-stu-id="f95ff-410">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="f95ff-411">**平行通訊協定** (17) </span><span class="sxs-lookup"><span data-stu-id="f95ff-411">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="f95ff-412">**ESCON** (18) </span><span class="sxs-lookup"><span data-stu-id="f95ff-412">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="f95ff-413">**診斷** (19) </span><span class="sxs-lookup"><span data-stu-id="f95ff-413">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="f95ff-414">**I2C** (20) </span><span class="sxs-lookup"><span data-stu-id="f95ff-414">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="f95ff-415">**Power** (21) </span><span class="sxs-lookup"><span data-stu-id="f95ff-415">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="f95ff-416">**HIPPI** (22) </span><span class="sxs-lookup"><span data-stu-id="f95ff-416">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="f95ff-417">**MultiBus** (23) </span><span class="sxs-lookup"><span data-stu-id="f95ff-417">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="f95ff-418">**Vm** (24) </span><span class="sxs-lookup"><span data-stu-id="f95ff-418">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="f95ff-419">**IPI** (25) </span><span class="sxs-lookup"><span data-stu-id="f95ff-419">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="f95ff-420">**IEEE-488** (26) </span><span class="sxs-lookup"><span data-stu-id="f95ff-420">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="f95ff-421">**RS232** (27) </span><span class="sxs-lookup"><span data-stu-id="f95ff-421">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="f95ff-422">**IEEE 802.3 10BASE5** (28) </span><span class="sxs-lookup"><span data-stu-id="f95ff-422">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="f95ff-423">**IEEE 802.3 10BASE2** (29) </span><span class="sxs-lookup"><span data-stu-id="f95ff-423">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="f95ff-424">**IEEE 802.3 1BASE5** (30) </span><span class="sxs-lookup"><span data-stu-id="f95ff-424">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="f95ff-425">**IEEE 802.3 10BROAD36** (31) </span><span class="sxs-lookup"><span data-stu-id="f95ff-425">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="f95ff-426">**IEEE 802.3 100BASEVG** (32) </span><span class="sxs-lookup"><span data-stu-id="f95ff-426">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="f95ff-427">**IEEE 802.5 權杖-環形** (33) </span><span class="sxs-lookup"><span data-stu-id="f95ff-427">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="f95ff-428">**ANSI x3t 9.5 FDDI** (34) </span><span class="sxs-lookup"><span data-stu-id="f95ff-428">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="f95ff-429">**MCA** (35) </span><span class="sxs-lookup"><span data-stu-id="f95ff-429">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="f95ff-430">**ESDI** (36) </span><span class="sxs-lookup"><span data-stu-id="f95ff-430">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="f95ff-431">**IDE** (37) </span><span class="sxs-lookup"><span data-stu-id="f95ff-431">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="f95ff-432">**CMD** (38) </span><span class="sxs-lookup"><span data-stu-id="f95ff-432">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="f95ff-433">**ST506** (39) </span><span class="sxs-lookup"><span data-stu-id="f95ff-433">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="f95ff-434">**」 Dssi 小組** (40) </span><span class="sxs-lookup"><span data-stu-id="f95ff-434">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="f95ff-435">**QIC2** (41) </span><span class="sxs-lookup"><span data-stu-id="f95ff-435">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="f95ff-436">**增強型 ATA/IDE** (42) </span><span class="sxs-lookup"><span data-stu-id="f95ff-436">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="f95ff-437">**AGP** (43) </span><span class="sxs-lookup"><span data-stu-id="f95ff-437">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="f95ff-438">**TWIRP (雙向紅外線)** (44) </span><span class="sxs-lookup"><span data-stu-id="f95ff-438">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="f95ff-439">**(快速紅外線)** (45) 的杉樹</span><span class="sxs-lookup"><span data-stu-id="f95ff-439">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="f95ff-440">**SIR (串列紅外線)** (46) </span><span class="sxs-lookup"><span data-stu-id="f95ff-440">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="f95ff-441">**IrBus** (47) </span><span class="sxs-lookup"><span data-stu-id="f95ff-441">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f95ff-442">**狀態**</span><span class="sxs-lookup"><span data-stu-id="f95ff-442">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f95ff-443">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f95ff-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-444">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f95ff-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-445">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="f95ff-445">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f95ff-446">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="f95ff-446">Current status of the object.</span></span> <span data-ttu-id="f95ff-447">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f95ff-447">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f95ff-448">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="f95ff-448">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f95ff-449">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="f95ff-449">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f95ff-450">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="f95ff-450">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f95ff-451">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="f95ff-451">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f95ff-452">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="f95ff-452">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f95ff-453">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="f95ff-453">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f95ff-454">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="f95ff-454">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f95ff-455">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="f95ff-455">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f95ff-456">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="f95ff-456">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f95ff-457">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="f95ff-457">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f95ff-458">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="f95ff-458">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f95ff-459">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="f95ff-459">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f95ff-460">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="f95ff-460">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f95ff-461">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="f95ff-461">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f95ff-462">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f95ff-462">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-463">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f95ff-463">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-464">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="f95ff-464">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="f95ff-465">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="f95ff-465">State of the logical device.</span></span> <span data-ttu-id="f95ff-466">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="f95ff-466">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="f95ff-467">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f95ff-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f95ff-468">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="f95ff-468">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f95ff-469">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="f95ff-469">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f95ff-470">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="f95ff-470">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f95ff-471">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="f95ff-471">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f95ff-472">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="f95ff-472">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f95ff-473">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f95ff-473">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f95ff-474">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f95ff-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-475">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f95ff-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-476">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f95ff-476">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f95ff-477">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="f95ff-477">Scoping system's creation class name.</span></span>

<span data-ttu-id="f95ff-478">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f95ff-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f95ff-479">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f95ff-479">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f95ff-480">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f95ff-480">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-481">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f95ff-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-482">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f95ff-482">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f95ff-483">設定系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="f95ff-483">Scoping system's name.</span></span>

<span data-ttu-id="f95ff-484">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f95ff-484">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f95ff-485">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="f95ff-485">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f95ff-486">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="f95ff-486">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f95ff-487">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f95ff-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f95ff-488">上次重設此控制器的日期和時間，這表示控制器已關機或重新初始化。</span><span class="sxs-lookup"><span data-stu-id="f95ff-488">Date and time this controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="f95ff-489">這個屬性繼承自 [**CIM \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="f95ff-489">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f95ff-490">備註</span><span class="sxs-lookup"><span data-stu-id="f95ff-490">Remarks</span></span>

<span data-ttu-id="f95ff-491">**Cim \_ PCMCIAController** 類別衍生自 [**cim \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="f95ff-491">The **CIM\_PCMCIAController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="f95ff-492">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="f95ff-492">WMI does not implement this class.</span></span> <span data-ttu-id="f95ff-493">針對衍生自 **CIM \_ PCMCIACONTROLLER** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="f95ff-493">For WMI classes that are derived from **CIM\_PCMCIAController**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f95ff-494">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="f95ff-494">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f95ff-495">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f95ff-495">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f95ff-496">規格需求</span><span class="sxs-lookup"><span data-stu-id="f95ff-496">Requirements</span></span>



| <span data-ttu-id="f95ff-497">需求</span><span class="sxs-lookup"><span data-stu-id="f95ff-497">Requirement</span></span> | <span data-ttu-id="f95ff-498">值</span><span class="sxs-lookup"><span data-stu-id="f95ff-498">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f95ff-499">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f95ff-499">Minimum supported client</span></span><br/> | <span data-ttu-id="f95ff-500">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f95ff-500">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f95ff-501">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f95ff-501">Minimum supported server</span></span><br/> | <span data-ttu-id="f95ff-502">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f95ff-502">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f95ff-503">命名空間</span><span class="sxs-lookup"><span data-stu-id="f95ff-503">Namespace</span></span><br/>                | <span data-ttu-id="f95ff-504">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f95ff-504">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f95ff-505">MOF</span><span class="sxs-lookup"><span data-stu-id="f95ff-505">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f95ff-506"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="f95ff-506"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f95ff-507">DLL</span><span class="sxs-lookup"><span data-stu-id="f95ff-507">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f95ff-508"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f95ff-508"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f95ff-509">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f95ff-509">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f95ff-510">**cim \_ 控制器**</span><span class="sxs-lookup"><span data-stu-id="f95ff-510">**cim\_controller**</span></span>](cim-controller.md)
</dt> </dl>

 

