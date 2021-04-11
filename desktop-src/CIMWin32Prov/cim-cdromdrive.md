---
description: CIM \_ CDROMDrive 類別代表電腦上的 cd-rom 光碟機。
ms.assetid: 044c9687-fc25-4a8c-b2ef-bd7ea332af7b
ms.tgt_platform: multiple
title: 'CIM_CDROMDrive 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CDROMDrive
- CIM_CDROMDrive.Caption
- CIM_CDROMDrive.Description
- CIM_CDROMDrive.InstallDate
- CIM_CDROMDrive.Name
- CIM_CDROMDrive.Status
- CIM_CDROMDrive.Availability
- CIM_CDROMDrive.ConfigManagerErrorCode
- CIM_CDROMDrive.ConfigManagerUserConfig
- CIM_CDROMDrive.CreationClassName
- CIM_CDROMDrive.DeviceID
- CIM_CDROMDrive.PowerManagementCapabilities
- CIM_CDROMDrive.ErrorCleared
- CIM_CDROMDrive.ErrorDescription
- CIM_CDROMDrive.LastErrorCode
- CIM_CDROMDrive.PNPDeviceID
- CIM_CDROMDrive.PowerManagementSupported
- CIM_CDROMDrive.StatusInfo
- CIM_CDROMDrive.SystemCreationClassName
- CIM_CDROMDrive.SystemName
- CIM_CDROMDrive.Capabilities
- CIM_CDROMDrive.CapabilityDescriptions
- CIM_CDROMDrive.CompressionMethod
- CIM_CDROMDrive.DefaultBlockSize
- CIM_CDROMDrive.ErrorMethodology
- CIM_CDROMDrive.MaxBlockSize
- CIM_CDROMDrive.MaxMediaSize
- CIM_CDROMDrive.MinBlockSize
- CIM_CDROMDrive.NeedsCleaning
- CIM_CDROMDrive.NumberOfMediaSupported
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 499607e050124533465a40da9e73d433142e6515
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847408"
---
# <a name="cim_cdromdrive-class-cimwin32-wmi-providers"></a><span data-ttu-id="2edb3-103">CIM_CDROMDrive 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="2edb3-103">CIM_CDROMDrive class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="2edb3-104">**CIM \_ CDROMDrive** 類別代表電腦上的 cd-rom 光碟機。</span><span class="sxs-lookup"><span data-stu-id="2edb3-104">The **CIM\_CDROMDrive** class represents a CD-ROM drive on the computer.</span></span>

> [!Note]  
> <span data-ttu-id="2edb3-105">磁片磁碟機的名稱不會對應至指派給裝置的邏輯磁碟機代號，也就是相依于該磁片磁碟機的邏輯存放裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="2edb3-105">The name of the drive does not correspond to the logical drive letter assigned to the device, which is the name of the logical storage device that is dependent on the drive.</span></span>

 

> [!IMPORTANT]
> <span data-ttu-id="2edb3-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="2edb3-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2edb3-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2edb3-108">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2edb3-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2edb3-109">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="2edb3-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2edb3-110">語法</span><span class="sxs-lookup"><span data-stu-id="2edb3-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C52B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_CDROMDrive : CIM_MediaAccessDevice
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
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   CompressionMethod;
  uint64   DefaultBlockSize;
  string   ErrorMethodology;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint64   MinBlockSize;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
};
```

## <a name="members"></a><span data-ttu-id="2edb3-111">成員</span><span class="sxs-lookup"><span data-stu-id="2edb3-111">Members</span></span>

<span data-ttu-id="2edb3-112">**CIM \_ CDROMDrive** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2edb3-112">The **CIM\_CDROMDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="2edb3-113">方法</span><span class="sxs-lookup"><span data-stu-id="2edb3-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="2edb3-114">屬性</span><span class="sxs-lookup"><span data-stu-id="2edb3-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2edb3-115">方法</span><span class="sxs-lookup"><span data-stu-id="2edb3-115">Methods</span></span>

<span data-ttu-id="2edb3-116">**CIM \_ CDROMDrive** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="2edb3-116">The **CIM\_CDROMDrive** class has these methods.</span></span>



| <span data-ttu-id="2edb3-117">方法</span><span class="sxs-lookup"><span data-stu-id="2edb3-117">Method</span></span>                                                                | <span data-ttu-id="2edb3-118">描述</span><span class="sxs-lookup"><span data-stu-id="2edb3-118">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2edb3-119">**重設**</span><span class="sxs-lookup"><span data-stu-id="2edb3-119">**Reset**</span></span>](reset-method-in-class-cim-cdromdrive.md)                 | <span data-ttu-id="2edb3-120">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="2edb3-120">Requests a reset of the logical device.</span></span> <span data-ttu-id="2edb3-121">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="2edb3-121">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="2edb3-122">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2edb3-122">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-cdromdrive.md) | <span data-ttu-id="2edb3-123">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="2edb3-123">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="2edb3-124">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="2edb3-124">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2edb3-125">屬性</span><span class="sxs-lookup"><span data-stu-id="2edb3-125">Properties</span></span>

<span data-ttu-id="2edb3-126">**CIM \_ CDROMDrive** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2edb3-126">The **CIM\_CDROMDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2edb3-127">**可用性**</span><span class="sxs-lookup"><span data-stu-id="2edb3-127">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-128">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2edb3-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-130">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="2edb3-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-131">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="2edb3-131">Availability and status of the device.</span></span>

<span data-ttu-id="2edb3-132">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-132">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2edb3-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="2edb3-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2edb3-134"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="2edb3-134"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="2edb3-135"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="2edb3-135"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="2edb3-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="2edb3-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="2edb3-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="2edb3-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2edb3-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="2edb3-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="2edb3-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="2edb3-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="2edb3-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="2edb3-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="2edb3-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="2edb3-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2edb3-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="2edb3-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="2edb3-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="2edb3-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="2edb3-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="2edb3-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="2edb3-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="2edb3-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-146">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="2edb3-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="2edb3-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="2edb3-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-148">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="2edb3-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="2edb3-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="2edb3-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-150">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="2edb3-150">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="2edb3-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="2edb3-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="2edb3-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="2edb3-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-153">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="2edb3-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="2edb3-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="2edb3-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-155">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="2edb3-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="2edb3-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="2edb3-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-157">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="2edb3-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="2edb3-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="2edb3-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-159">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="2edb3-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="2edb3-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="2edb3-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-161">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="2edb3-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2edb3-162">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="2edb3-162">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-163">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="2edb3-163">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-165">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 儲存裝置 \| 001.9 "，" MIF。DMTF \| 儲存裝置 \| 001.11 "，" MIF。DMTF \| 儲存裝置 \| 001.12 "，" MIF。DMTF \| 磁片 \| 003.7 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。**CapabilityDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="2edb3-165">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-166">媒體存取裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="2edb3-166">Capabilities of the media access device.</span></span>

<span data-ttu-id="2edb3-167">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-167">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2edb3-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="2edb3-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-169">不明。</span><span class="sxs-lookup"><span data-stu-id="2edb3-169">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2edb3-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="2edb3-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-171">其他。</span><span class="sxs-lookup"><span data-stu-id="2edb3-171">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="2edb3-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**順序存取** (2) </span><span class="sxs-lookup"><span data-stu-id="2edb3-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-173">順序存取。</span><span class="sxs-lookup"><span data-stu-id="2edb3-173">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="2edb3-174"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**隨機存取** (3) </span><span class="sxs-lookup"><span data-stu-id="2edb3-174"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-175">隨機存取。</span><span class="sxs-lookup"><span data-stu-id="2edb3-175">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="2edb3-176"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**支援寫入** (4) </span><span class="sxs-lookup"><span data-stu-id="2edb3-176"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-177">撰寫。</span><span class="sxs-lookup"><span data-stu-id="2edb3-177">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="2edb3-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**加密** (5) </span><span class="sxs-lookup"><span data-stu-id="2edb3-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-179">加密。</span><span class="sxs-lookup"><span data-stu-id="2edb3-179">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="2edb3-180"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**壓縮** (6) </span><span class="sxs-lookup"><span data-stu-id="2edb3-180"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-181">壓縮。</span><span class="sxs-lookup"><span data-stu-id="2edb3-181">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="2edb3-182"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**支援卸除式媒體** (7) </span><span class="sxs-lookup"><span data-stu-id="2edb3-182"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-183">卸除式媒體。</span><span class="sxs-lookup"><span data-stu-id="2edb3-183">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="2edb3-184"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**手動清除** (8) </span><span class="sxs-lookup"><span data-stu-id="2edb3-184"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-185">手動清除。</span><span class="sxs-lookup"><span data-stu-id="2edb3-185">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="2edb3-186"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**自動清除** (9) </span><span class="sxs-lookup"><span data-stu-id="2edb3-186"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-187">自動清除。</span><span class="sxs-lookup"><span data-stu-id="2edb3-187">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="2edb3-188"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**智慧型通知** (10) </span><span class="sxs-lookup"><span data-stu-id="2edb3-188"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-189">智慧型通知。</span><span class="sxs-lookup"><span data-stu-id="2edb3-189">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="2edb3-190"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**支援雙側媒體** (11) </span><span class="sxs-lookup"><span data-stu-id="2edb3-190"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-191">區分可以從唯讀取一側的裝置存取雙面媒體兩側，且需要開啟媒體的裝置。</span><span class="sxs-lookup"><span data-stu-id="2edb3-191">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="2edb3-192"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**不需要 Predismount 退出** (12) </span><span class="sxs-lookup"><span data-stu-id="2edb3-192"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-193">表示不需要明確地從裝置上取出媒體，即可透過選擇器元素來存取。</span><span class="sxs-lookup"><span data-stu-id="2edb3-193">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2edb3-194">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2edb3-194">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-195">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="2edb3-195">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-196">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-197">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。**功能**") </span><span class="sxs-lookup"><span data-stu-id="2edb3-197">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-198">自由格式字串的陣列，提供 **功能** 陣列中指出之存取裝置功能的詳細說明。</span><span class="sxs-lookup"><span data-stu-id="2edb3-198">Array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="2edb3-199">這個陣列的每個專案都與 **功能** 陣列中位於相同索引的專案有關。</span><span class="sxs-lookup"><span data-stu-id="2edb3-199">Each entry of this array is related to the entry in the **Capabilities** array, located at the same index.</span></span>

 

<span data-ttu-id="2edb3-200">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-200">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2edb3-201">**標題**</span><span class="sxs-lookup"><span data-stu-id="2edb3-201">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-202">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2edb3-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-204">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="2edb3-204">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-205">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="2edb3-205">A short textual description of the object.</span></span>

<span data-ttu-id="2edb3-206">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-206">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2edb3-207">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="2edb3-207">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-208">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2edb3-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-210">自由格式字串，表示用來壓縮邏輯檔案的演算法或工具。</span><span class="sxs-lookup"><span data-stu-id="2edb3-210">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="2edb3-211">如果無法描述壓縮配置 (因為) 未知，請使用下列各項：如果為，則使用「未知」。</span><span class="sxs-lookup"><span data-stu-id="2edb3-211">If it is not possible to describe the compression scheme (because it is unknown), use the following:If , use "Unknown".</span></span> <span data-ttu-id="2edb3-212">如果為，則使用「壓縮」。</span><span class="sxs-lookup"><span data-stu-id="2edb3-212">If , use "Compressed".</span></span> <span data-ttu-id="2edb3-213">，請使用「未壓縮」。</span><span class="sxs-lookup"><span data-stu-id="2edb3-213">, use "Not Compressed".</span></span>

<span data-ttu-id="2edb3-214">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-214">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="2edb3-215"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="2edb3-215">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-216">壓縮配置未知或未描述。</span><span class="sxs-lookup"><span data-stu-id="2edb3-216">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="2edb3-217"> ( 「壓縮」 ) </span><span class="sxs-lookup"><span data-stu-id="2edb3-217">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-218">邏輯檔案已壓縮，但壓縮配置未知或未描述</span><span class="sxs-lookup"><span data-stu-id="2edb3-218">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="2edb3-219"> ( 「未壓縮」 ) </span><span class="sxs-lookup"><span data-stu-id="2edb3-219">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-220">如果邏輯檔案未壓縮</span><span class="sxs-lookup"><span data-stu-id="2edb3-220">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2edb3-221">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2edb3-221">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-222">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2edb3-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-223">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-224">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="2edb3-224">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-225">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2edb3-225">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="2edb3-226">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-226">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="2edb3-227">**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-227">**This device is working properly.**</span></span> <span data-ttu-id="2edb3-228"> (0)</span><span class="sxs-lookup"><span data-stu-id="2edb3-228">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="2edb3-229">**這個裝置並未正確設定。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-229">**This device is not configured correctly.**</span></span> <span data-ttu-id="2edb3-230">(1)</span><span class="sxs-lookup"><span data-stu-id="2edb3-230">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2edb3-231">**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-231">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="2edb3-232">(2)</span><span class="sxs-lookup"><span data-stu-id="2edb3-232">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="2edb3-233">**這個裝置的驅動程式可能已損毀，或您系統的記憶體或其他資源可能不足。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-233">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="2edb3-234">(3)</span><span class="sxs-lookup"><span data-stu-id="2edb3-234">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2edb3-235">**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-235">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="2edb3-236">(4)</span><span class="sxs-lookup"><span data-stu-id="2edb3-236">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="2edb3-237">**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-237">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="2edb3-238">(5)</span><span class="sxs-lookup"><span data-stu-id="2edb3-238">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="2edb3-239">**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-239">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="2edb3-240">(6)</span><span class="sxs-lookup"><span data-stu-id="2edb3-240">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="2edb3-241">**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-241">**Cannot filter.**</span></span> <span data-ttu-id="2edb3-242">(7)</span><span class="sxs-lookup"><span data-stu-id="2edb3-242">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="2edb3-243">**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-243">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="2edb3-244">(8)</span><span class="sxs-lookup"><span data-stu-id="2edb3-244">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="2edb3-245">**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-245">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="2edb3-246">(9)</span><span class="sxs-lookup"><span data-stu-id="2edb3-246">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="2edb3-247">**這個裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-247">**This device cannot start.**</span></span> <span data-ttu-id="2edb3-248">(10)</span><span class="sxs-lookup"><span data-stu-id="2edb3-248">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="2edb3-249">**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-249">**This device failed.**</span></span> <span data-ttu-id="2edb3-250">(11)</span><span class="sxs-lookup"><span data-stu-id="2edb3-250">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="2edb3-251">**這個裝置沒有足夠資源可供使用。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-251">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="2edb3-252"> (12) </span><span class="sxs-lookup"><span data-stu-id="2edb3-252">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="2edb3-253">**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-253">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="2edb3-254">(13)</span><span class="sxs-lookup"><span data-stu-id="2edb3-254">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="2edb3-255">**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-255">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="2edb3-256">(14)</span><span class="sxs-lookup"><span data-stu-id="2edb3-256">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="2edb3-257">**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-257">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="2edb3-258">(15)</span><span class="sxs-lookup"><span data-stu-id="2edb3-258">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="2edb3-259">**Windows 無法識別這個裝置所使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-259">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="2edb3-260">(16)</span><span class="sxs-lookup"><span data-stu-id="2edb3-260">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="2edb3-261">**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-261">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="2edb3-262">(17)</span><span class="sxs-lookup"><span data-stu-id="2edb3-262">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2edb3-263">**重新安裝這個裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-263">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="2edb3-264">(18)</span><span class="sxs-lookup"><span data-stu-id="2edb3-264">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="2edb3-265">**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-265">**Failure using the VxD loader.**</span></span> <span data-ttu-id="2edb3-266">(19)</span><span class="sxs-lookup"><span data-stu-id="2edb3-266">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2edb3-267">**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-267">**Your registry might be corrupted.**</span></span> <span data-ttu-id="2edb3-268">(20)</span><span class="sxs-lookup"><span data-stu-id="2edb3-268">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="2edb3-269">**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-269">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="2edb3-270">(21)</span><span class="sxs-lookup"><span data-stu-id="2edb3-270">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="2edb3-271">**這個裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-271">**This device is disabled.**</span></span> <span data-ttu-id="2edb3-272">(22)</span><span class="sxs-lookup"><span data-stu-id="2edb3-272">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="2edb3-273">**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-273">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="2edb3-274">(23)</span><span class="sxs-lookup"><span data-stu-id="2edb3-274">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="2edb3-275">**這個裝置可能不存在、運作不正確、或並未安裝所有的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-275">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="2edb3-276">(24)</span><span class="sxs-lookup"><span data-stu-id="2edb3-276">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2edb3-277">**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-277">**Windows is still setting up this device.**</span></span> <span data-ttu-id="2edb3-278">(25)</span><span class="sxs-lookup"><span data-stu-id="2edb3-278">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2edb3-279">**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-279">**Windows is still setting up this device.**</span></span> <span data-ttu-id="2edb3-280">(26)</span><span class="sxs-lookup"><span data-stu-id="2edb3-280">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="2edb3-281">**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-281">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="2edb3-282">(27)</span><span class="sxs-lookup"><span data-stu-id="2edb3-282">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="2edb3-283">**這個裝置的驅動程式尚未安裝。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-283">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="2edb3-284">(28)</span><span class="sxs-lookup"><span data-stu-id="2edb3-284">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="2edb3-285">**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-285">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="2edb3-286">(29)</span><span class="sxs-lookup"><span data-stu-id="2edb3-286">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="2edb3-287">**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-287">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="2edb3-288">(30)</span><span class="sxs-lookup"><span data-stu-id="2edb3-288">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2edb3-289">**這個裝置並未正確執行，因為 Windows 無法載入這個裝置必需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="2edb3-289">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="2edb3-290"> (31) </span><span class="sxs-lookup"><span data-stu-id="2edb3-290">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2edb3-291">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="2edb3-291">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-292">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2edb3-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-293">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-294">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="2edb3-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-295">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="2edb3-295">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="2edb3-296">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2edb3-297">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2edb3-297">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-298">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2edb3-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-299">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-300">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2edb3-300">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-301">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="2edb3-301">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2edb3-302">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="2edb3-302">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="2edb3-303">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-303">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2edb3-304">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="2edb3-304">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-305">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="2edb3-305">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-306">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-307">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="2edb3-307">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-308">裝置的預設區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2edb3-308">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="2edb3-309">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-309">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="2edb3-310">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-310">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2edb3-311">**說明**</span><span class="sxs-lookup"><span data-stu-id="2edb3-311">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-312">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2edb3-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-313">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-314">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="2edb3-314">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-315">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="2edb3-315">A textual description of the object.</span></span>

<span data-ttu-id="2edb3-316">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2edb3-317">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="2edb3-317">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-318">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2edb3-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-319">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-320">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2edb3-320">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-321">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="2edb3-321">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="2edb3-322">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2edb3-323">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="2edb3-323">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-324">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2edb3-324">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-325">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-326">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="2edb3-326">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="2edb3-327">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2edb3-328">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2edb3-328">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-329">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2edb3-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-330">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-331">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="2edb3-331">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="2edb3-332">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2edb3-333">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="2edb3-333">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-334">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2edb3-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-335">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-336">描述裝置所支援之錯誤偵測和更正類型的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="2edb3-336">Free-form string that describes the types of error detection and correction supported by the device.</span></span>

<span data-ttu-id="2edb3-337">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-337">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2edb3-338">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2edb3-338">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-339">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="2edb3-339">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-340">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-341">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="2edb3-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-342">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="2edb3-342">Indicates when the object was installed.</span></span> <span data-ttu-id="2edb3-343">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="2edb3-343">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="2edb3-344">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2edb3-345">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2edb3-345">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-346">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2edb3-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-347">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-348">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2edb3-348">Last error code reported by the logical device.</span></span>

<span data-ttu-id="2edb3-349">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2edb3-350">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="2edb3-350">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-351">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="2edb3-351">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-352">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-353">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="2edb3-353">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-354">裝置所存取媒體的最大區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2edb3-354">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="2edb3-355">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-355">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="2edb3-356">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-356">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2edb3-357">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="2edb3-357">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-358">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="2edb3-358">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-359">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-360">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 順序存取裝置 \| 001.2 「) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「kb」 ) </span><span class="sxs-lookup"><span data-stu-id="2edb3-360">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-361">此裝置支援的媒體大小上限（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="2edb3-361">Maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="2edb3-362">Kb 會被視為位元組數目乘以 1000 (而不是位元組數乘以 1024) 。</span><span class="sxs-lookup"><span data-stu-id="2edb3-362">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="2edb3-363">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-363">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="2edb3-364">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-364">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2edb3-365">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="2edb3-365">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-366">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="2edb3-366">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-367">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-368">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="2edb3-368">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-369">裝置所存取媒體的區塊大小下限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2edb3-369">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="2edb3-370">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-370">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="2edb3-371">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-371">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2edb3-372">**名稱**</span><span class="sxs-lookup"><span data-stu-id="2edb3-372">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-373">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2edb3-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-374">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-375">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="2edb3-375">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-376">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="2edb3-376">Label by which the object is known.</span></span> <span data-ttu-id="2edb3-377">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="2edb3-377">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="2edb3-378">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-378">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2edb3-379">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="2edb3-379">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-380">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2edb3-380">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-381">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-382">若 **為 TRUE**，則媒體存取裝置需要清除。</span><span class="sxs-lookup"><span data-stu-id="2edb3-382">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="2edb3-383">在 [ **功能** 陣列] 屬性中，是否可能指出手動或自動清除。</span><span class="sxs-lookup"><span data-stu-id="2edb3-383">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="2edb3-384">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-384">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2edb3-385">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="2edb3-385">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-386">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2edb3-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-387">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-388">可以支援或插入的多個個別媒體的最大數目。</span><span class="sxs-lookup"><span data-stu-id="2edb3-388">Maximum number of multiple individual media that can be supported or inserted.</span></span>

<span data-ttu-id="2edb3-389">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-389">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2edb3-390">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="2edb3-390">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-391">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2edb3-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-392">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-393">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="2edb3-393">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-394">指出邏輯裝置的 Win32 隨插即用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="2edb3-394">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="2edb3-395">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="2edb3-395">Example: "\*PNP030b"</span></span>

<span data-ttu-id="2edb3-396">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2edb3-397">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2edb3-397">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-398">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="2edb3-398">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-399">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-400">指出邏輯裝置的特定電源相關功能。</span><span class="sxs-lookup"><span data-stu-id="2edb3-400">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="2edb3-401">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-401">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2edb3-402"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="2edb3-402"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-403">電源相關的容量未知。</span><span class="sxs-lookup"><span data-stu-id="2edb3-403">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="2edb3-404"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="2edb3-404"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-405">此裝置不支援與電源相關的容量。</span><span class="sxs-lookup"><span data-stu-id="2edb3-405">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2edb3-406"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="2edb3-406"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-407">電源相關容量已停用。</span><span class="sxs-lookup"><span data-stu-id="2edb3-407">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2edb3-408"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="2edb3-408"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-409">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="2edb3-409">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="2edb3-410"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="2edb3-410"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-411">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="2edb3-411">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="2edb3-412"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="2edb3-412"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-413">支援 **SetPowerState** 方法。</span><span class="sxs-lookup"><span data-stu-id="2edb3-413">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="2edb3-414">這個方法可在父 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="2edb3-414">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="2edb3-415">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-415">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="2edb3-416"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="2edb3-416"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-417">您可以叫用 **SetPowerState** 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) 。</span><span class="sxs-lookup"><span data-stu-id="2edb3-417">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="2edb3-418"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="2edb3-418"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2edb3-419">您可以叫用 **SetPowerState** 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) ，並將 *時間* 參數設定為特定日期和時間（或間隔），以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="2edb3-419">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2edb3-420">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="2edb3-420">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-421">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2edb3-421">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-422">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-423">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="2edb3-423">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="2edb3-424">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="2edb3-424">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="2edb3-425">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="2edb3-425">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="2edb3-426">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="2edb3-426">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="2edb3-427">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-427">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2edb3-428">**狀態**</span><span class="sxs-lookup"><span data-stu-id="2edb3-428">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-429">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2edb3-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-430">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-431">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="2edb3-431">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-432">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="2edb3-432">String that indicates the current status of the object.</span></span> <span data-ttu-id="2edb3-433">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="2edb3-433">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="2edb3-434">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="2edb3-434">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="2edb3-435">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="2edb3-435">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="2edb3-436">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="2edb3-436">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2edb3-437">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="2edb3-437">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2edb3-438">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="2edb3-438">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2edb3-439">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-439">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2edb3-440">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="2edb3-440">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2edb3-441">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="2edb3-441">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2edb3-442">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="2edb3-442">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2edb3-443">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="2edb3-443">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2edb3-444">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="2edb3-444">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2edb3-445">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="2edb3-445">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2edb3-446">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="2edb3-446">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2edb3-447">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="2edb3-447">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2edb3-448">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="2edb3-448">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2edb3-449">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="2edb3-449">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2edb3-450">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="2edb3-450">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2edb3-451">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="2edb3-451">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2edb3-452">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="2edb3-452">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2edb3-453">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="2edb3-453">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-454">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2edb3-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-455">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-456">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="2edb3-456">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-457">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="2edb3-457">State of the logical device.</span></span> <span data-ttu-id="2edb3-458">如果此屬性不適用於邏輯裝置，則應該使用值 5 ( 「不適用」 ) 。</span><span class="sxs-lookup"><span data-stu-id="2edb3-458">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="2edb3-459">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-459">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2edb3-460">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="2edb3-460">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2edb3-461">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="2edb3-461">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2edb3-462">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="2edb3-462">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2edb3-463">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="2edb3-463">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2edb3-464">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="2edb3-464">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2edb3-465">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2edb3-465">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-466">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2edb3-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-467">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-467">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-468">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2edb3-468">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-469">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="2edb3-469">The scoping system's creation class name.</span></span>

<span data-ttu-id="2edb3-470">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2edb3-471">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2edb3-471">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2edb3-472">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2edb3-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-473">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2edb3-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2edb3-474">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2edb3-474">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2edb3-475">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="2edb3-475">The scoping system's name.</span></span>

<span data-ttu-id="2edb3-476">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-476">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2edb3-477">備註</span><span class="sxs-lookup"><span data-stu-id="2edb3-477">Remarks</span></span>

<span data-ttu-id="2edb3-478">**Cim \_ CDROMDrive** 類別衍生自 [**cim \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-478">The **CIM\_CDROMDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="2edb3-479">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="2edb3-479">WMI does not implement this class.</span></span> <span data-ttu-id="2edb3-480">如需衍生自 **CIM \_ CDROMDrive** 之類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="2edb3-480">For more information about classes derived from **CIM\_CDROMDrive**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="2edb3-481">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="2edb3-481">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2edb3-482">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="2edb3-482">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2edb3-483">規格需求</span><span class="sxs-lookup"><span data-stu-id="2edb3-483">Requirements</span></span>



| <span data-ttu-id="2edb3-484">需求</span><span class="sxs-lookup"><span data-stu-id="2edb3-484">Requirement</span></span> | <span data-ttu-id="2edb3-485">值</span><span class="sxs-lookup"><span data-stu-id="2edb3-485">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2edb3-486">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2edb3-486">Minimum supported client</span></span><br/> | <span data-ttu-id="2edb3-487">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2edb3-487">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2edb3-488">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2edb3-488">Minimum supported server</span></span><br/> | <span data-ttu-id="2edb3-489">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2edb3-489">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2edb3-490">命名空間</span><span class="sxs-lookup"><span data-stu-id="2edb3-490">Namespace</span></span><br/>                | <span data-ttu-id="2edb3-491">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2edb3-491">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2edb3-492">MOF</span><span class="sxs-lookup"><span data-stu-id="2edb3-492">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2edb3-493"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="2edb3-493"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2edb3-494">DLL</span><span class="sxs-lookup"><span data-stu-id="2edb3-494">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2edb3-495"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2edb3-495"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2edb3-496">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2edb3-496">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2edb3-497">**CIM \_ MediaAccessDevice**</span><span class="sxs-lookup"><span data-stu-id="2edb3-497">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

