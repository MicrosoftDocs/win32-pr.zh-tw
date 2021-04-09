---
description: CIM \_ WORMDrive 類別代表 WORM 磁片磁碟機（媒體存取裝置的子類型）的功能和管理。
ms.assetid: df77084a-01f2-4cca-b395-d74ee64ef526
ms.tgt_platform: multiple
title: CIM_WORMDrive 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_WORMDrive
- CIM_WORMDrive.Availability
- CIM_WORMDrive.Capabilities
- CIM_WORMDrive.CapabilityDescriptions
- CIM_WORMDrive.Caption
- CIM_WORMDrive.CompressionMethod
- CIM_WORMDrive.ConfigManagerErrorCode
- CIM_WORMDrive.ConfigManagerUserConfig
- CIM_WORMDrive.CreationClassName
- CIM_WORMDrive.DefaultBlockSize
- CIM_WORMDrive.Description
- CIM_WORMDrive.DeviceID
- CIM_WORMDrive.ErrorCleared
- CIM_WORMDrive.ErrorDescription
- CIM_WORMDrive.ErrorMethodology
- CIM_WORMDrive.InstallDate
- CIM_WORMDrive.LastErrorCode
- CIM_WORMDrive.MaxBlockSize
- CIM_WORMDrive.MaxMediaSize
- CIM_WORMDrive.MinBlockSize
- CIM_WORMDrive.Name
- CIM_WORMDrive.NeedsCleaning
- CIM_WORMDrive.NumberOfMediaSupported
- CIM_WORMDrive.PNPDeviceID
- CIM_WORMDrive.PowerManagementCapabilities
- CIM_WORMDrive.PowerManagementSupported
- CIM_WORMDrive.Status
- CIM_WORMDrive.StatusInfo
- CIM_WORMDrive.SystemCreationClassName
- CIM_WORMDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 08133d1abdcb6fc401ee4ad730d82ef97fb30200
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110249"
---
# <a name="cim_wormdrive-class"></a><span data-ttu-id="bd098-103">CIM \_ WORMDrive 類別</span><span class="sxs-lookup"><span data-stu-id="bd098-103">CIM\_WORMDrive class</span></span>

<span data-ttu-id="bd098-104">**CIM \_ WORMDrive** 類別代表 WORM 磁片磁碟機（媒體存取裝置的子類型）的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="bd098-104">The **CIM\_WORMDrive** class represents the capabilities and management of a WORM drive, a subtype of the media access device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bd098-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="bd098-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bd098-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="bd098-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="bd098-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="bd098-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="bd098-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="bd098-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd098-109">語法</span><span class="sxs-lookup"><span data-stu-id="bd098-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FFB58B9A-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_WORMDrive : CIM_MediaAccessDevice
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CompressionMethod;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint64   DefaultBlockSize;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="bd098-110">成員</span><span class="sxs-lookup"><span data-stu-id="bd098-110">Members</span></span>

<span data-ttu-id="bd098-111">**CIM \_ WORMDrive** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bd098-111">The **CIM\_WORMDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="bd098-112">方法</span><span class="sxs-lookup"><span data-stu-id="bd098-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="bd098-113">屬性</span><span class="sxs-lookup"><span data-stu-id="bd098-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bd098-114">方法</span><span class="sxs-lookup"><span data-stu-id="bd098-114">Methods</span></span>

<span data-ttu-id="bd098-115">**CIM \_ WORMDrive** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="bd098-115">The **CIM\_WORMDrive** class has these methods.</span></span>



| <span data-ttu-id="bd098-116">方法</span><span class="sxs-lookup"><span data-stu-id="bd098-116">Method</span></span>                                                               | <span data-ttu-id="bd098-117">描述</span><span class="sxs-lookup"><span data-stu-id="bd098-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd098-118">**重設**</span><span class="sxs-lookup"><span data-stu-id="bd098-118">**Reset**</span></span>](reset-method-in-class-cim-wormdrive.md)                 | <span data-ttu-id="bd098-119">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="bd098-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="bd098-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="bd098-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="bd098-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="bd098-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-wormdrive.md) | <span data-ttu-id="bd098-122">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="bd098-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="bd098-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="bd098-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bd098-124">屬性</span><span class="sxs-lookup"><span data-stu-id="bd098-124">Properties</span></span>

<span data-ttu-id="bd098-125">**CIM \_ WORMDrive** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bd098-125">The **CIM\_WORMDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bd098-126">**可用性**</span><span class="sxs-lookup"><span data-stu-id="bd098-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-127">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="bd098-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bd098-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd098-129">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="bd098-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="bd098-130">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="bd098-130">Availability and status of the device.</span></span>

<span data-ttu-id="bd098-131">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bd098-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="bd098-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bd098-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="bd098-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="bd098-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="bd098-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-135">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="bd098-135">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="bd098-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="bd098-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="bd098-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="bd098-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="bd098-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="bd098-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="bd098-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="bd098-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="bd098-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="bd098-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="bd098-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="bd098-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="bd098-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="bd098-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="bd098-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="bd098-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="bd098-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="bd098-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="bd098-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="bd098-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-146">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="bd098-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="bd098-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="bd098-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-148">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="bd098-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="bd098-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="bd098-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-150">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="bd098-150">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="bd098-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="bd098-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="bd098-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="bd098-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-153">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="bd098-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="bd098-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="bd098-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-155">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="bd098-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="bd098-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="bd098-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-157">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="bd098-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="bd098-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="bd098-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-159">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="bd098-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="bd098-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="bd098-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-161">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="bd098-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bd098-162">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="bd098-162">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-163">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="bd098-163">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bd098-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd098-165">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 儲存裝置 \| 001.9 "，" MIF。DMTF \| 儲存裝置 \| 001.11 "，" MIF。DMTF \| 儲存裝置 \| 001.12 "，" MIF。DMTF \| 磁片 \| 003.7 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。**CapabilityDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="bd098-165">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="bd098-166">媒體存取裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="bd098-166">Capabilities of the media access device.</span></span> <span data-ttu-id="bd098-167">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-167">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bd098-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="bd098-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bd098-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="bd098-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="bd098-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**順序存取** (2) </span><span class="sxs-lookup"><span data-stu-id="bd098-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="bd098-171"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**隨機存取** (3) </span><span class="sxs-lookup"><span data-stu-id="bd098-171"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="bd098-172"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**支援寫入** (4) </span><span class="sxs-lookup"><span data-stu-id="bd098-172"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="bd098-173"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**加密** (5) </span><span class="sxs-lookup"><span data-stu-id="bd098-173"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="bd098-174"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**壓縮** (6) </span><span class="sxs-lookup"><span data-stu-id="bd098-174"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="bd098-175"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**支援卸除式媒體** (7) </span><span class="sxs-lookup"><span data-stu-id="bd098-175"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-176">卸除式媒體。</span><span class="sxs-lookup"><span data-stu-id="bd098-176">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="bd098-177"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**手動清除** (8) </span><span class="sxs-lookup"><span data-stu-id="bd098-177"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="bd098-178"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**自動清除** (9) </span><span class="sxs-lookup"><span data-stu-id="bd098-178"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="bd098-179"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**智慧型通知** (10) </span><span class="sxs-lookup"><span data-stu-id="bd098-179"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="bd098-180"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**支援雙側媒體** (11) </span><span class="sxs-lookup"><span data-stu-id="bd098-180"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-181">區分可以從唯讀取一側的裝置存取雙面媒體兩側，且需要開啟媒體的裝置。</span><span class="sxs-lookup"><span data-stu-id="bd098-181">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="bd098-182"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**不需要 Predismount 退出** (12) </span><span class="sxs-lookup"><span data-stu-id="bd098-182"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-183">表示不需要明確地從裝置上取出媒體，即可透過選擇器元素來存取。</span><span class="sxs-lookup"><span data-stu-id="bd098-183">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bd098-184">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="bd098-184">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-185">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="bd098-185">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bd098-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd098-187">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。**功能**") </span><span class="sxs-lookup"><span data-stu-id="bd098-187">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="bd098-188">提供 **功能** 陣列中所指出之存取裝置功能詳細描述的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="bd098-188">Free-form strings that provide detailed descriptions for the access device features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="bd098-189">這個陣列的每個專案都與位於相同索引的 **功能** 陣列中的專案相關。</span><span class="sxs-lookup"><span data-stu-id="bd098-189">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

 

<span data-ttu-id="bd098-190">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-190">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd098-191">**標題**</span><span class="sxs-lookup"><span data-stu-id="bd098-191">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-192">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bd098-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd098-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd098-194">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="bd098-194">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="bd098-195">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="bd098-195">Short textual description of the object.</span></span>

<span data-ttu-id="bd098-196">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd098-197">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="bd098-197">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-198">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bd098-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd098-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd098-200">自由格式字串，表示用來壓縮邏輯檔案的演算法或工具。</span><span class="sxs-lookup"><span data-stu-id="bd098-200">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="bd098-201">如果壓縮配置未知或未描述，請使用「未知」。</span><span class="sxs-lookup"><span data-stu-id="bd098-201">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="bd098-202">如果已壓縮邏輯檔案，但壓縮配置未知或未描述，請使用「壓縮」。</span><span class="sxs-lookup"><span data-stu-id="bd098-202">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="bd098-203">如果邏輯檔案未壓縮，請使用「未壓縮」。</span><span class="sxs-lookup"><span data-stu-id="bd098-203">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="bd098-204">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-204">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="bd098-205"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="bd098-205">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="bd098-206">壓縮配置未知或未描述。</span><span class="sxs-lookup"><span data-stu-id="bd098-206">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="bd098-207"> ( 「壓縮」 ) </span><span class="sxs-lookup"><span data-stu-id="bd098-207">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="bd098-208">邏輯檔案已壓縮，但壓縮配置未知或未描述</span><span class="sxs-lookup"><span data-stu-id="bd098-208">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="bd098-209"> ( 「未壓縮」 ) </span><span class="sxs-lookup"><span data-stu-id="bd098-209">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="bd098-210">如果邏輯檔案未壓縮</span><span class="sxs-lookup"><span data-stu-id="bd098-210">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bd098-211">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="bd098-211">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-212">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="bd098-212">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd098-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd098-214">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="bd098-214">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="bd098-215">Windows 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bd098-215">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="bd098-216">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-216">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="bd098-217"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="bd098-217"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="bd098-218"> (0)</span><span class="sxs-lookup"><span data-stu-id="bd098-218">(0)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-219">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="bd098-219">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="bd098-220"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="bd098-220"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="bd098-221">(1)</span><span class="sxs-lookup"><span data-stu-id="bd098-221">(1)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-222">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="bd098-222">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="bd098-223"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="bd098-223"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="bd098-224">(2)</span><span class="sxs-lookup"><span data-stu-id="bd098-224">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="bd098-225"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="bd098-225"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="bd098-226">(3)</span><span class="sxs-lookup"><span data-stu-id="bd098-226">(3)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-227">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="bd098-227">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="bd098-228"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="bd098-228"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="bd098-229">(4)</span><span class="sxs-lookup"><span data-stu-id="bd098-229">(4)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-230">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="bd098-230">Device is not working properly.</span></span> <span data-ttu-id="bd098-231">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="bd098-231">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="bd098-232"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="bd098-232"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="bd098-233">(5)</span><span class="sxs-lookup"><span data-stu-id="bd098-233">(5)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-234">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="bd098-234">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="bd098-235"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="bd098-235"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="bd098-236">(6)</span><span class="sxs-lookup"><span data-stu-id="bd098-236">(6)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-237">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="bd098-237">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="bd098-238"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="bd098-238"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="bd098-239">(7)</span><span class="sxs-lookup"><span data-stu-id="bd098-239">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="bd098-240"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="bd098-240"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="bd098-241">(8)</span><span class="sxs-lookup"><span data-stu-id="bd098-241">(8)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-242">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="bd098-242">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="bd098-243"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="bd098-243"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="bd098-244">(9)</span><span class="sxs-lookup"><span data-stu-id="bd098-244">(9)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-245">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="bd098-245">Device is not working properly.</span></span> <span data-ttu-id="bd098-246">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="bd098-246">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="bd098-247"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="bd098-247"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="bd098-248">(10)</span><span class="sxs-lookup"><span data-stu-id="bd098-248">(10)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-249">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="bd098-249">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="bd098-250"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="bd098-250"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="bd098-251">(11)</span><span class="sxs-lookup"><span data-stu-id="bd098-251">(11)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-252">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="bd098-252">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="bd098-253"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="bd098-253"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="bd098-254"> (12) </span><span class="sxs-lookup"><span data-stu-id="bd098-254">(12)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-255">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="bd098-255">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="bd098-256"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="bd098-256"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="bd098-257">(13)</span><span class="sxs-lookup"><span data-stu-id="bd098-257">(13)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-258">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="bd098-258">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="bd098-259"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="bd098-259"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="bd098-260">(14)</span><span class="sxs-lookup"><span data-stu-id="bd098-260">(14)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-261">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="bd098-261">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="bd098-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="bd098-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="bd098-263">(15)</span><span class="sxs-lookup"><span data-stu-id="bd098-263">(15)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-264">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="bd098-264">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="bd098-265"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="bd098-265"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="bd098-266">(16)</span><span class="sxs-lookup"><span data-stu-id="bd098-266">(16)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-267">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="bd098-267">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="bd098-268"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="bd098-268"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="bd098-269">(17)</span><span class="sxs-lookup"><span data-stu-id="bd098-269">(17)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-270">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="bd098-270">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="bd098-271"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="bd098-271"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="bd098-272">(18)</span><span class="sxs-lookup"><span data-stu-id="bd098-272">(18)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-273">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="bd098-273">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="bd098-274"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="bd098-274"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="bd098-275">(19)</span><span class="sxs-lookup"><span data-stu-id="bd098-275">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="bd098-276"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="bd098-276"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="bd098-277">(20)</span><span class="sxs-lookup"><span data-stu-id="bd098-277">(20)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-278">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="bd098-278">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="bd098-279"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="bd098-279"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="bd098-280">(21)</span><span class="sxs-lookup"><span data-stu-id="bd098-280">(21)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-281">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="bd098-281">System failure.</span></span> <span data-ttu-id="bd098-282">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="bd098-282">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="bd098-283">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="bd098-283">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="bd098-284"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="bd098-284"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="bd098-285">(22)</span><span class="sxs-lookup"><span data-stu-id="bd098-285">(22)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-286">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="bd098-286">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="bd098-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="bd098-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="bd098-288">(23)</span><span class="sxs-lookup"><span data-stu-id="bd098-288">(23)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-289">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="bd098-289">System failure.</span></span> <span data-ttu-id="bd098-290">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="bd098-290">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="bd098-291"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="bd098-291"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="bd098-292">(24)</span><span class="sxs-lookup"><span data-stu-id="bd098-292">(24)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-293">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="bd098-293">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="bd098-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="bd098-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="bd098-295">(25)</span><span class="sxs-lookup"><span data-stu-id="bd098-295">(25)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-296">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="bd098-296">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="bd098-297"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="bd098-297"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="bd098-298">(26)</span><span class="sxs-lookup"><span data-stu-id="bd098-298">(26)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-299">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="bd098-299">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="bd098-300"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="bd098-300"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="bd098-301">(27)</span><span class="sxs-lookup"><span data-stu-id="bd098-301">(27)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-302">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="bd098-302">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="bd098-303"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="bd098-303"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="bd098-304">(28)</span><span class="sxs-lookup"><span data-stu-id="bd098-304">(28)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-305">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="bd098-305">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="bd098-306"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="bd098-306"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="bd098-307">(29)</span><span class="sxs-lookup"><span data-stu-id="bd098-307">(29)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-308">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="bd098-308">Device is disabled.</span></span> <span data-ttu-id="bd098-309">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="bd098-309">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="bd098-310"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="bd098-310"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="bd098-311">(30)</span><span class="sxs-lookup"><span data-stu-id="bd098-311">(30)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-312">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="bd098-312">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="bd098-313"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="bd098-313"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="bd098-314"> (31) </span><span class="sxs-lookup"><span data-stu-id="bd098-314">(31)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-315">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="bd098-315">Device is not working properly.</span></span> <span data-ttu-id="bd098-316">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="bd098-316">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bd098-317">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="bd098-317">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-318">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="bd098-318">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bd098-319">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd098-320">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="bd098-320">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="bd098-321">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="bd098-321">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="bd098-322">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd098-323">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bd098-323">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-324">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bd098-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd098-325">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd098-326">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="bd098-326">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="bd098-327">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd098-327">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="bd098-328">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="bd098-328">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="bd098-329">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd098-330">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="bd098-330">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-331">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="bd098-331">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bd098-332">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd098-333">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="bd098-333">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="bd098-334">裝置的預設區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="bd098-334">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="bd098-335">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-335">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="bd098-336">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="bd098-336">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="bd098-337">**說明**</span><span class="sxs-lookup"><span data-stu-id="bd098-337">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-338">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bd098-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd098-339">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd098-340">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="bd098-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="bd098-341">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="bd098-341">Textual description of the object.</span></span>

<span data-ttu-id="bd098-342">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd098-343">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="bd098-343">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-344">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bd098-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd098-345">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd098-346">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="bd098-346">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="bd098-347">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="bd098-347">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="bd098-348">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-348">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd098-349">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="bd098-349">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-350">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="bd098-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bd098-351">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd098-352">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="bd098-352">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="bd098-353">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-353">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd098-354">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="bd098-354">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-355">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bd098-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd098-356">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd098-357">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="bd098-357">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="bd098-358">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-358">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd098-359">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="bd098-359">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-360">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bd098-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd098-361">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd098-362">描述裝置所支援之錯誤偵測和更正類型的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="bd098-362">Free-form string that describes the types of error detection and correction supported by the device.</span></span>

<span data-ttu-id="bd098-363">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-363">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd098-364">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="bd098-364">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-365">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="bd098-365">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bd098-366">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd098-367">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="bd098-367">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="bd098-368">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="bd098-368">Date and time the object was installed.</span></span> <span data-ttu-id="bd098-369">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="bd098-369">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="bd098-370">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-370">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd098-371">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="bd098-371">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-372">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="bd098-372">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd098-373">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd098-374">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bd098-374">Last error code reported by the logical device.</span></span>

<span data-ttu-id="bd098-375">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-375">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd098-376">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="bd098-376">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-377">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="bd098-377">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bd098-378">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd098-379">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="bd098-379">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="bd098-380">裝置所存取媒體的最大區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="bd098-380">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="bd098-381">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-381">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="bd098-382">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="bd098-382">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="bd098-383">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="bd098-383">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-384">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="bd098-384">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bd098-385">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd098-386">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 順序存取裝置 \| 001.2 「) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「kb」 ) </span><span class="sxs-lookup"><span data-stu-id="bd098-386">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="bd098-387">裝置所支援媒體的大小上限（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="bd098-387">Maximum size, in kilobytes, of media supported by the device.</span></span> <span data-ttu-id="bd098-388">Kb 會被視為位元組數目乘以 1000 (而不是位元組數乘以 1024) 。</span><span class="sxs-lookup"><span data-stu-id="bd098-388">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="bd098-389">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-389">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="bd098-390">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="bd098-390">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="bd098-391">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="bd098-391">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-392">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="bd098-392">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bd098-393">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd098-394">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="bd098-394">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="bd098-395">裝置所存取媒體的區塊大小下限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="bd098-395">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="bd098-396">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-396">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="bd098-397">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="bd098-397">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="bd098-398">**名稱**</span><span class="sxs-lookup"><span data-stu-id="bd098-398">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-399">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bd098-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd098-400">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd098-401">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="bd098-401">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="bd098-402">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="bd098-402">Label by which the object is known.</span></span> <span data-ttu-id="bd098-403">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="bd098-403">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="bd098-404">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-404">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd098-405">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="bd098-405">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-406">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="bd098-406">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bd098-407">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd098-408">若 **為 TRUE**，則媒體存取裝置需要清除。</span><span class="sxs-lookup"><span data-stu-id="bd098-408">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="bd098-409">在 [ **功能** 陣列] 屬性中，是否可能指出手動或自動清除。</span><span class="sxs-lookup"><span data-stu-id="bd098-409">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="bd098-410">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-410">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd098-411">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="bd098-411">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-412">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="bd098-412">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd098-413">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd098-414">當媒體存取裝置支援多個個別媒體時，這個屬性會定義可支援或插入的最大數目。</span><span class="sxs-lookup"><span data-stu-id="bd098-414">When the media access device supports multiple individual media, this property defines the maximum number that can be supported or inserted.</span></span>

<span data-ttu-id="bd098-415">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-415">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd098-416">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="bd098-416">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-417">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bd098-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd098-418">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd098-419">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="bd098-419">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="bd098-420">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="bd098-420">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="bd098-421">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-421">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="bd098-422">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="bd098-422">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="bd098-423">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="bd098-423">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-424">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="bd098-424">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bd098-425">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd098-426">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="bd098-426">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="bd098-427">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="bd098-427">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bd098-428"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="bd098-428"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="bd098-429"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="bd098-429"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-430">此裝置不支援與電源相關的容量。</span><span class="sxs-lookup"><span data-stu-id="bd098-430">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="bd098-431"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="bd098-431"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="bd098-432"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="bd098-432"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-433">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="bd098-433">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="bd098-434"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="bd098-434"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-435">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="bd098-435">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="bd098-436"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="bd098-436"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-437">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="bd098-437">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="bd098-438">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="bd098-438">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="bd098-439">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="bd098-439">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="bd098-440"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="bd098-440"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-441">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="bd098-441">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="bd098-442"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="bd098-442"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="bd098-443">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="bd098-443">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bd098-444">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="bd098-444">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-445">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="bd098-445">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bd098-446">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd098-447">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="bd098-447">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="bd098-448">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="bd098-448">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="bd098-449">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="bd098-449">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="bd098-450">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="bd098-450">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="bd098-451">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-451">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd098-452">**狀態**</span><span class="sxs-lookup"><span data-stu-id="bd098-452">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-453">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bd098-453">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd098-454">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd098-455">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="bd098-455">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="bd098-456">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="bd098-456">Current status of the object.</span></span> <span data-ttu-id="bd098-457">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-457">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="bd098-458">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="bd098-458">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="bd098-459">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="bd098-459">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="bd098-460">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="bd098-460">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="bd098-461">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="bd098-461">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bd098-462">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="bd098-462">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="bd098-463">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="bd098-463">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="bd098-464">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="bd098-464">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="bd098-465">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="bd098-465">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="bd098-466">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="bd098-466">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="bd098-467">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="bd098-467">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="bd098-468">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="bd098-468">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="bd098-469">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="bd098-469">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="bd098-470">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="bd098-470">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bd098-471">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="bd098-471">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-472">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="bd098-472">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bd098-473">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd098-474">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="bd098-474">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="bd098-475">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="bd098-475">State of the logical device.</span></span> <span data-ttu-id="bd098-476">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="bd098-476">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="bd098-477">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-477">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bd098-478">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="bd098-478">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bd098-479">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="bd098-479">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="bd098-480">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="bd098-480">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="bd098-481">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="bd098-481">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="bd098-482">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="bd098-482">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bd098-483">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bd098-483">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-484">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bd098-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd098-485">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-485">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd098-486">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="bd098-486">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="bd098-487">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="bd098-487">Scoping system's creation class name.</span></span>

<span data-ttu-id="bd098-488">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-488">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd098-489">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="bd098-489">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd098-490">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bd098-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd098-491">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd098-491">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd098-492">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="bd098-492">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="bd098-493">設定系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="bd098-493">Scoping system's name.</span></span>

<span data-ttu-id="bd098-494">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-494">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bd098-495">備註</span><span class="sxs-lookup"><span data-stu-id="bd098-495">Remarks</span></span>

<span data-ttu-id="bd098-496">**Cim \_ WORMDrive** 類別衍生自 [**cim \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="bd098-496">The **CIM\_WORMDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="bd098-497">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="bd098-497">WMI does not implement this class.</span></span>

<span data-ttu-id="bd098-498">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="bd098-498">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="bd098-499">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="bd098-499">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd098-500">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd098-500">Requirements</span></span>



| <span data-ttu-id="bd098-501">需求</span><span class="sxs-lookup"><span data-stu-id="bd098-501">Requirement</span></span> | <span data-ttu-id="bd098-502">值</span><span class="sxs-lookup"><span data-stu-id="bd098-502">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd098-503">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bd098-503">Minimum supported client</span></span><br/> | <span data-ttu-id="bd098-504">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bd098-504">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bd098-505">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bd098-505">Minimum supported server</span></span><br/> | <span data-ttu-id="bd098-506">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd098-506">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bd098-507">命名空間</span><span class="sxs-lookup"><span data-stu-id="bd098-507">Namespace</span></span><br/>                | <span data-ttu-id="bd098-508">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="bd098-508">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bd098-509">MOF</span><span class="sxs-lookup"><span data-stu-id="bd098-509">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd098-510"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd098-510"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd098-511">DLL</span><span class="sxs-lookup"><span data-stu-id="bd098-511">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd098-512"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd098-512"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd098-513">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd098-513">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd098-514">**CIM \_ MediaAccessDevice**</span><span class="sxs-lookup"><span data-stu-id="bd098-514">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

