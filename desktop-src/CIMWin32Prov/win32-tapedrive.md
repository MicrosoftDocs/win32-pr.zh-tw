---
description: Win32 \_ DISABLE-TAPEDRIVE WMI 類別代表電腦系統上執行 Windows 的磁帶機。 磁帶磁片磁碟機主要是以可依序存取的方式來區分。
ms.assetid: ceefec7b-a904-4b2f-a6b6-b84917a33023
ms.tgt_platform: multiple
title: Win32_TapeDrive 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TapeDrive
- Win32_TapeDrive.Reset
- Win32_TapeDrive.SetPowerState
- Win32_TapeDrive.Availability
- Win32_TapeDrive.Capabilities
- Win32_TapeDrive.CapabilityDescriptions
- Win32_TapeDrive.Caption
- Win32_TapeDrive.Compression
- Win32_TapeDrive.CompressionMethod
- Win32_TapeDrive.ConfigManagerErrorCode
- Win32_TapeDrive.ConfigManagerUserConfig
- Win32_TapeDrive.CreationClassName
- Win32_TapeDrive.DefaultBlockSize
- Win32_TapeDrive.Description
- Win32_TapeDrive.DeviceID
- Win32_TapeDrive.ECC
- Win32_TapeDrive.EOTWarningZoneSize
- Win32_TapeDrive.ErrorCleared
- Win32_TapeDrive.ErrorDescription
- Win32_TapeDrive.ErrorMethodology
- Win32_TapeDrive.FeaturesHigh
- Win32_TapeDrive.FeaturesLow
- Win32_TapeDrive.Id
- Win32_TapeDrive.InstallDate
- Win32_TapeDrive.LastErrorCode
- Win32_TapeDrive.Manufacturer
- Win32_TapeDrive.MaxBlockSize
- Win32_TapeDrive.MaxMediaSize
- Win32_TapeDrive.MaxPartitionCount
- Win32_TapeDrive.MediaType
- Win32_TapeDrive.MinBlockSize
- Win32_TapeDrive.Name
- Win32_TapeDrive.NeedsCleaning
- Win32_TapeDrive.NumberOfMediaSupported
- Win32_TapeDrive.Padding
- Win32_TapeDrive.PNPDeviceID
- Win32_TapeDrive.PowerManagementCapabilities
- Win32_TapeDrive.PowerManagementSupported
- Win32_TapeDrive.ReportSetMarks
- Win32_TapeDrive.Status
- Win32_TapeDrive.StatusInfo
- Win32_TapeDrive.SystemCreationClassName
- Win32_TapeDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6c7e7d3b754a0399acb152dba043da269f67a06f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973386"
---
# <a name="win32_tapedrive-class"></a><span data-ttu-id="05025-104">Win32 \_ disable-tapedrive 類別</span><span class="sxs-lookup"><span data-stu-id="05025-104">Win32\_TapeDrive class</span></span>

<span data-ttu-id="05025-105">**Win32 \_ disable-tapedrive** [WMI 類別](../wmisdk/retrieving-a-class.md)代表電腦系統上執行 Windows 的磁帶機。</span><span class="sxs-lookup"><span data-stu-id="05025-105">The **Win32\_TapeDrive** [WMI class](../wmisdk/retrieving-a-class.md) represents a tape drive on a computer system running Windows.</span></span> <span data-ttu-id="05025-106">磁帶磁片磁碟機主要是以可依序存取的方式來區分。</span><span class="sxs-lookup"><span data-stu-id="05025-106">Tape drives are primarily distinguished by the fact that they can only be accessed sequentially.</span></span>

<span data-ttu-id="05025-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="05025-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="05025-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="05025-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="05025-109">語法</span><span class="sxs-lookup"><span data-stu-id="05025-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_TapeDrive : CIM_TapeDrive
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   Compression;
  string   CompressionMethod;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint64   DefaultBlockSize;
  string   Description;
  string   DeviceID;
  uint32   ECC;
  uint32   EOTWarningZoneSize;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  uint32   FeaturesHigh;
  uint32   FeaturesLow;
  string   Id;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint32   MaxPartitionCount;
  string   MediaType;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  uint32   Padding;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   ReportSetMarks;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="05025-110">成員</span><span class="sxs-lookup"><span data-stu-id="05025-110">Members</span></span>

<span data-ttu-id="05025-111">**Win32 \_ disable-tapedrive** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="05025-111">The **Win32\_TapeDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="05025-112">方法</span><span class="sxs-lookup"><span data-stu-id="05025-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="05025-113">屬性</span><span class="sxs-lookup"><span data-stu-id="05025-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="05025-114">方法</span><span class="sxs-lookup"><span data-stu-id="05025-114">Methods</span></span>

<span data-ttu-id="05025-115">**Win32 \_ disable-tapedrive** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="05025-115">The **Win32\_TapeDrive** class has these methods.</span></span>



| <span data-ttu-id="05025-116">方法</span><span class="sxs-lookup"><span data-stu-id="05025-116">Method</span></span>            | <span data-ttu-id="05025-117">描述</span><span class="sxs-lookup"><span data-stu-id="05025-117">Description</span></span>                                                                                                                                                                            |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05025-118">**重設**</span><span class="sxs-lookup"><span data-stu-id="05025-118">**Reset**</span></span>         | <span data-ttu-id="05025-119">未實作。</span><span class="sxs-lookup"><span data-stu-id="05025-119">Not implemented.</span></span> <span data-ttu-id="05025-120">若要執行此方法，請參閱 [**CIM \_ disable-tapedrive**](cim-tapedrive.md)中的 [**Reset**](reset-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="05025-120">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span><br/>                 |
| <span data-ttu-id="05025-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="05025-121">**SetPowerState**</span></span> | <span data-ttu-id="05025-122">未實作。</span><span class="sxs-lookup"><span data-stu-id="05025-122">Not implemented.</span></span> <span data-ttu-id="05025-123">若要執行此方法，請參閱 [**CIM \_ disable-tapedrive**](cim-tapedrive.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="05025-123">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="05025-124">屬性</span><span class="sxs-lookup"><span data-stu-id="05025-124">Properties</span></span>

<span data-ttu-id="05025-125">**Win32 \_ disable-tapedrive** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="05025-125">The **Win32\_TapeDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="05025-126">**可用性**</span><span class="sxs-lookup"><span data-stu-id="05025-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-127">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="05025-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="05025-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-129">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="05025-129">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="05025-130">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="05025-130">Availability and status of the device.</span></span>

<span data-ttu-id="05025-131">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="05025-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="05025-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="05025-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="05025-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="05025-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="05025-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="05025-135">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="05025-135">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="05025-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="05025-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="05025-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="05025-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="05025-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="05025-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="05025-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="05025-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="05025-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="05025-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="05025-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="05025-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="05025-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="05025-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="05025-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="05025-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="05025-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="05025-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="05025-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="05025-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="05025-146">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="05025-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="05025-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="05025-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="05025-148">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="05025-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="05025-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="05025-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="05025-150">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="05025-150">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="05025-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="05025-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="05025-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="05025-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="05025-153">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="05025-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="05025-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="05025-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="05025-155">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="05025-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="05025-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="05025-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="05025-157">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="05025-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="05025-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="05025-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="05025-159">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="05025-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="05025-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="05025-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="05025-161">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="05025-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="05025-162">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="05025-162">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-163">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="05025-163">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="05025-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-165">限定詞： [**ArrayType**](../wmisdk/standard-qualifiers.md) ( 「已編制索引」 ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) (」 MIF。DMTF \| 儲存裝置 \| 001.9 "，" MIF。DMTF \| 儲存裝置 \| 001.11 "，" MIF。DMTF \| 儲存裝置 \| 001.12 "，" MIF。DMTF \| 磁片 \| 003.7 ") ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。**CapabilityDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="05025-165">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="05025-166">媒體存取裝置的功能陣列。</span><span class="sxs-lookup"><span data-stu-id="05025-166">Array of capabilities of the media access device.</span></span> <span data-ttu-id="05025-167">例如，裝置可能支援隨機存取、卸載式媒體和自動清除。</span><span class="sxs-lookup"><span data-stu-id="05025-167">For example, the device may support Random Access, removable media and Automatic Cleaning.</span></span> <span data-ttu-id="05025-168">在此情況下，會將3、7和9值寫入陣列中。</span><span class="sxs-lookup"><span data-stu-id="05025-168">In this case, the values 3, 7, and 9 would be written to the array.</span></span>

<span data-ttu-id="05025-169">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-169">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="05025-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="05025-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="05025-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="05025-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="05025-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**順序存取** (2) </span><span class="sxs-lookup"><span data-stu-id="05025-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="05025-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**隨機存取** (3) </span><span class="sxs-lookup"><span data-stu-id="05025-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="05025-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**支援寫入** (4) </span><span class="sxs-lookup"><span data-stu-id="05025-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="05025-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**加密** (5) </span><span class="sxs-lookup"><span data-stu-id="05025-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="05025-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**壓縮** (6) </span><span class="sxs-lookup"><span data-stu-id="05025-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="05025-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**支援卸除式媒體** (7) </span><span class="sxs-lookup"><span data-stu-id="05025-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="05025-178">支援卸載式媒體</span><span class="sxs-lookup"><span data-stu-id="05025-178">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="05025-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**手動清除** (8) </span><span class="sxs-lookup"><span data-stu-id="05025-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="05025-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**自動清除** (9) </span><span class="sxs-lookup"><span data-stu-id="05025-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="05025-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**智慧型通知** (10) </span><span class="sxs-lookup"><span data-stu-id="05025-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="05025-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**支援雙側媒體** (11) </span><span class="sxs-lookup"><span data-stu-id="05025-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="05025-183">支援 Dual-Sided 媒體</span><span class="sxs-lookup"><span data-stu-id="05025-183">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="05025-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**不需要 Predismount 退出** (12) </span><span class="sxs-lookup"><span data-stu-id="05025-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="05025-185">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="05025-185">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-186">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="05025-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="05025-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-188">限定詞： [**ArrayType**](../wmisdk/standard-qualifiers.md) ( "Indexed" ) ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。**功能**") </span><span class="sxs-lookup"><span data-stu-id="05025-188">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="05025-189">自由格式字串的陣列，可針對 **功能** 陣列中指出的任何存取裝置功能提供更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="05025-189">Array of free-form strings providing more detailed explanations for any of the access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="05025-190">請注意，這個陣列的每個專案都與位於相同索引的 **功能** 陣列中的專案相關。</span><span class="sxs-lookup"><span data-stu-id="05025-190">Note that each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="05025-191">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-191">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05025-192">**標題**</span><span class="sxs-lookup"><span data-stu-id="05025-192">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-193">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05025-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05025-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-195">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="05025-195">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="05025-196">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="05025-196">Short description of the object.</span></span>

<span data-ttu-id="05025-197">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="05025-198">**壓縮**</span><span class="sxs-lookup"><span data-stu-id="05025-198">**Compression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-199">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="05025-199">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05025-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-201">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 磁帶備份結構 \| [**磁帶 \_ 取得 \_ 磁片磁碟機 \_ 參數**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| 壓縮" ) </span><span class="sxs-lookup"><span data-stu-id="05025-201">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|Compression")</span></span>
</dt> </dl>

<span data-ttu-id="05025-202">若 **為 TRUE**，則會啟用硬體資料壓縮。</span><span class="sxs-lookup"><span data-stu-id="05025-202">If **TRUE**, hardware data compression is enabled.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="05025-203"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="05025-203"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="05025-204">FALSE</span><span class="sxs-lookup"><span data-stu-id="05025-204">FALSE</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="05025-205"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="05025-205"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="05025-206">true</span><span class="sxs-lookup"><span data-stu-id="05025-206">TRUE</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="05025-207">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="05025-207">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-208">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05025-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05025-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05025-210">自由格式字串，指出裝置用來支援壓縮的演算法或工具。</span><span class="sxs-lookup"><span data-stu-id="05025-210">Free-form string indicating the algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="05025-211">如果不可能或不想要描述壓縮配置 (可能是因為) 不知道，請使用下列文字：「未知」表示不知道裝置是否支援壓縮功能;「已壓縮」表示裝置支援壓縮功能，但其壓縮配置未知或未洩漏;和「未壓縮」表示裝置不支援壓縮功能。</span><span class="sxs-lookup"><span data-stu-id="05025-211">If it is not possible or not desired to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the device supports compression capabilities or not; "Compressed" to represent that the device supports compression capabilities but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the device does not support compression capabilities.</span></span>

<span data-ttu-id="05025-212">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-212">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="05025-213"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="05025-213">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="05025-214">壓縮配置未知或未描述。</span><span class="sxs-lookup"><span data-stu-id="05025-214">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="05025-215"> ( 「壓縮」 ) </span><span class="sxs-lookup"><span data-stu-id="05025-215">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="05025-216">邏輯檔案已壓縮，但壓縮配置未知或未描述</span><span class="sxs-lookup"><span data-stu-id="05025-216">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="05025-217"> ( 「未壓縮」 ) </span><span class="sxs-lookup"><span data-stu-id="05025-217">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="05025-218">如果邏輯檔案未壓縮</span><span class="sxs-lookup"><span data-stu-id="05025-218">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="05025-219">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="05025-219">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-220">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="05025-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05025-221">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-222">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="05025-222">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="05025-223">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="05025-223">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="05025-224">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-224">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="05025-225"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="05025-225"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="05025-226"> (0)</span><span class="sxs-lookup"><span data-stu-id="05025-226">(0)</span></span>


</dt> <dd>

<span data-ttu-id="05025-227">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="05025-227">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="05025-228"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="05025-228"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="05025-229">(1)</span><span class="sxs-lookup"><span data-stu-id="05025-229">(1)</span></span>


</dt> <dd>

<span data-ttu-id="05025-230">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="05025-230">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="05025-231"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="05025-231"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="05025-232">(2)</span><span class="sxs-lookup"><span data-stu-id="05025-232">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="05025-233"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="05025-233"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="05025-234">(3)</span><span class="sxs-lookup"><span data-stu-id="05025-234">(3)</span></span>


</dt> <dd>

<span data-ttu-id="05025-235">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="05025-235">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="05025-236"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="05025-236"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="05025-237">(4)</span><span class="sxs-lookup"><span data-stu-id="05025-237">(4)</span></span>


</dt> <dd>

<span data-ttu-id="05025-238">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="05025-238">Device is not working properly.</span></span> <span data-ttu-id="05025-239">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="05025-239">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="05025-240"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="05025-240"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="05025-241">(5)</span><span class="sxs-lookup"><span data-stu-id="05025-241">(5)</span></span>


</dt> <dd>

<span data-ttu-id="05025-242">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="05025-242">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="05025-243"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="05025-243"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="05025-244">(6)</span><span class="sxs-lookup"><span data-stu-id="05025-244">(6)</span></span>


</dt> <dd>

<span data-ttu-id="05025-245">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="05025-245">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="05025-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="05025-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="05025-247">(7)</span><span class="sxs-lookup"><span data-stu-id="05025-247">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="05025-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="05025-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="05025-249">(8)</span><span class="sxs-lookup"><span data-stu-id="05025-249">(8)</span></span>


</dt> <dd>

<span data-ttu-id="05025-250">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="05025-250">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="05025-251"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="05025-251"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="05025-252">(9)</span><span class="sxs-lookup"><span data-stu-id="05025-252">(9)</span></span>


</dt> <dd>

<span data-ttu-id="05025-253">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="05025-253">Device is not working properly.</span></span> <span data-ttu-id="05025-254">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="05025-254">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="05025-255"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="05025-255"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="05025-256">(10)</span><span class="sxs-lookup"><span data-stu-id="05025-256">(10)</span></span>


</dt> <dd>

<span data-ttu-id="05025-257">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="05025-257">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="05025-258"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="05025-258"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="05025-259">(11)</span><span class="sxs-lookup"><span data-stu-id="05025-259">(11)</span></span>


</dt> <dd>

<span data-ttu-id="05025-260">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="05025-260">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="05025-261"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="05025-261"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="05025-262"> (12) </span><span class="sxs-lookup"><span data-stu-id="05025-262">(12)</span></span>


</dt> <dd>

<span data-ttu-id="05025-263">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="05025-263">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="05025-264"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="05025-264"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="05025-265">(13)</span><span class="sxs-lookup"><span data-stu-id="05025-265">(13)</span></span>


</dt> <dd>

<span data-ttu-id="05025-266">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="05025-266">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="05025-267"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="05025-267"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="05025-268">(14)</span><span class="sxs-lookup"><span data-stu-id="05025-268">(14)</span></span>


</dt> <dd>

<span data-ttu-id="05025-269">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="05025-269">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="05025-270"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="05025-270"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="05025-271">(15)</span><span class="sxs-lookup"><span data-stu-id="05025-271">(15)</span></span>


</dt> <dd>

<span data-ttu-id="05025-272">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="05025-272">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="05025-273"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="05025-273"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="05025-274">(16)</span><span class="sxs-lookup"><span data-stu-id="05025-274">(16)</span></span>


</dt> <dd>

<span data-ttu-id="05025-275">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="05025-275">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="05025-276"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="05025-276"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="05025-277">(17)</span><span class="sxs-lookup"><span data-stu-id="05025-277">(17)</span></span>


</dt> <dd>

<span data-ttu-id="05025-278">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="05025-278">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="05025-279"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="05025-279"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="05025-280">(18)</span><span class="sxs-lookup"><span data-stu-id="05025-280">(18)</span></span>


</dt> <dd>

<span data-ttu-id="05025-281">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="05025-281">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="05025-282"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="05025-282"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="05025-283">(19)</span><span class="sxs-lookup"><span data-stu-id="05025-283">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="05025-284"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="05025-284"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="05025-285">(20)</span><span class="sxs-lookup"><span data-stu-id="05025-285">(20)</span></span>


</dt> <dd>

<span data-ttu-id="05025-286">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="05025-286">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="05025-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="05025-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="05025-288">(21)</span><span class="sxs-lookup"><span data-stu-id="05025-288">(21)</span></span>


</dt> <dd>

<span data-ttu-id="05025-289">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="05025-289">System failure.</span></span> <span data-ttu-id="05025-290">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="05025-290">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="05025-291">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="05025-291">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="05025-292"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="05025-292"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="05025-293">(22)</span><span class="sxs-lookup"><span data-stu-id="05025-293">(22)</span></span>


</dt> <dd>

<span data-ttu-id="05025-294">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="05025-294">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="05025-295"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="05025-295"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="05025-296">(23)</span><span class="sxs-lookup"><span data-stu-id="05025-296">(23)</span></span>


</dt> <dd>

<span data-ttu-id="05025-297">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="05025-297">System failure.</span></span> <span data-ttu-id="05025-298">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="05025-298">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="05025-299"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="05025-299"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="05025-300">(24)</span><span class="sxs-lookup"><span data-stu-id="05025-300">(24)</span></span>


</dt> <dd>

<span data-ttu-id="05025-301">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="05025-301">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="05025-302"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="05025-302"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="05025-303">(25)</span><span class="sxs-lookup"><span data-stu-id="05025-303">(25)</span></span>


</dt> <dd>

<span data-ttu-id="05025-304">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="05025-304">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="05025-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="05025-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="05025-306">(26)</span><span class="sxs-lookup"><span data-stu-id="05025-306">(26)</span></span>


</dt> <dd>

<span data-ttu-id="05025-307">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="05025-307">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="05025-308"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="05025-308"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="05025-309">(27)</span><span class="sxs-lookup"><span data-stu-id="05025-309">(27)</span></span>


</dt> <dd>

<span data-ttu-id="05025-310">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="05025-310">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="05025-311"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="05025-311"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="05025-312">(28)</span><span class="sxs-lookup"><span data-stu-id="05025-312">(28)</span></span>


</dt> <dd>

<span data-ttu-id="05025-313">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="05025-313">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="05025-314"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="05025-314"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="05025-315">(29)</span><span class="sxs-lookup"><span data-stu-id="05025-315">(29)</span></span>


</dt> <dd>

<span data-ttu-id="05025-316">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="05025-316">Device is disabled.</span></span> <span data-ttu-id="05025-317">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="05025-317">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="05025-318"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="05025-318"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="05025-319">(30)</span><span class="sxs-lookup"><span data-stu-id="05025-319">(30)</span></span>


</dt> <dd>

<span data-ttu-id="05025-320">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="05025-320">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="05025-321"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="05025-321"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="05025-322"> (31) </span><span class="sxs-lookup"><span data-stu-id="05025-322">(31)</span></span>


</dt> <dd>

<span data-ttu-id="05025-323">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="05025-323">Device is not working properly.</span></span> <span data-ttu-id="05025-324">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="05025-324">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="05025-325">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="05025-325">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-326">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="05025-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05025-327">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-328">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="05025-328">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="05025-329">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="05025-329">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="05025-330">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05025-331">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="05025-331">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-332">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05025-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05025-333">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-334">限定詞： [ **CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="05025-334">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="05025-335">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="05025-335">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="05025-336">搭配類別的其他索引鍵屬性使用時，此屬性可讓這個類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="05025-336">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="05025-337">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05025-338">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="05025-338">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-339">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="05025-339">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="05025-340">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-341">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="05025-341">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="05025-342">此裝置的預設區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="05025-342">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="05025-343">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-343">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="05025-344">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-344">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="05025-345">**說明**</span><span class="sxs-lookup"><span data-stu-id="05025-345">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-346">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05025-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05025-347">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-348">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="05025-348">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="05025-349">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="05025-349">Description of the object.</span></span>

<span data-ttu-id="05025-350">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-350">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="05025-351">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="05025-351">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-352">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05025-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05025-353">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-354">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "DeviceId" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| File 函數 \| CreateFile" ) </span><span class="sxs-lookup"><span data-stu-id="05025-354">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Functions\|CreateFile")</span></span>
</dt> </dl>

<span data-ttu-id="05025-355">磁片磁碟機的唯一識別碼與系統上的其他裝置。</span><span class="sxs-lookup"><span data-stu-id="05025-355">Unique identifier of the tape drive with other devices on the system.</span></span>

<span data-ttu-id="05025-356">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-356">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05025-357">**ECC**</span><span class="sxs-lookup"><span data-stu-id="05025-357">**ECC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-358">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="05025-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05025-359">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-360">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 磁帶備份結構 \| [**磁帶 \_ 取得 \_ 磁片磁碟機 \_ 參數**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| ECC" ) </span><span class="sxs-lookup"><span data-stu-id="05025-360">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|ECC")</span></span>
</dt> </dl>

<span data-ttu-id="05025-361">若 **為 TRUE**，則表示裝置支援硬體錯誤修正。</span><span class="sxs-lookup"><span data-stu-id="05025-361">If **TRUE**, the device supports hardware error correction.</span></span>

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="05025-362">**False** (0) </span><span class="sxs-lookup"><span data-stu-id="05025-362">**False** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="05025-363">**True** (1) </span><span class="sxs-lookup"><span data-stu-id="05025-363">**True** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="05025-364">**EOTWarningZoneSize**</span><span class="sxs-lookup"><span data-stu-id="05025-364">**EOTWarningZoneSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-365">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="05025-365">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05025-366">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-367">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="05025-367">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="05025-368">磁帶結尾 (EOT) 警告的區域大小。</span><span class="sxs-lookup"><span data-stu-id="05025-368">Zone size for the end of tape (EOT) warning.</span></span>

<span data-ttu-id="05025-369">這個屬性繼承自 [**CIM \_ disable-tapedrive**](cim-tapedrive.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-369">This property is inherited from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

</dd> <dt>

<span data-ttu-id="05025-370">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="05025-370">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-371">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="05025-371">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05025-372">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05025-373">若 **為 TRUE**，則表示 **LastErrorCode** 中回報的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="05025-373">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="05025-374">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05025-375">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="05025-375">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-376">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05025-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05025-377">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05025-378">自由格式字串提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="05025-378">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="05025-379">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-379">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05025-380">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="05025-380">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-381">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05025-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05025-382">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05025-383">描述此裝置所支援之錯誤偵測和修正類型的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="05025-383">Free-form string describing the type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="05025-384">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-384">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05025-385">**FeaturesHigh**</span><span class="sxs-lookup"><span data-stu-id="05025-385">**FeaturesHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-386">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="05025-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05025-387">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-388">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 磁帶備份結構 \| [**磁帶 \_ 取得 \_ 磁片磁碟機 \_ 參數**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| FeaturesHigh" ) </span><span class="sxs-lookup"><span data-stu-id="05025-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|FeaturesHigh")</span></span>
</dt> </dl>

<span data-ttu-id="05025-389">裝置功能旗標的高序位32位。</span><span class="sxs-lookup"><span data-stu-id="05025-389">High-order 32 bits of the device features flag.</span></span>

</dd> <dt>

<span data-ttu-id="05025-390">**FeaturesLow**</span><span class="sxs-lookup"><span data-stu-id="05025-390">**FeaturesLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-391">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="05025-391">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05025-392">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-393">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 磁帶備份結構 \| [**磁帶 \_ 取得 \_ 磁片磁碟機 \_ 參數**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| FeaturesLow" ) </span><span class="sxs-lookup"><span data-stu-id="05025-393">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|FeaturesLow")</span></span>
</dt> </dl>

<span data-ttu-id="05025-394">裝置功能旗標的低序位32位。</span><span class="sxs-lookup"><span data-stu-id="05025-394">Low-order 32 bits of the device features flag.</span></span>

</dd> <dt>

<span data-ttu-id="05025-395">**識別碼**</span><span class="sxs-lookup"><span data-stu-id="05025-395">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-396">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05025-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05025-397">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-398">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| File 函數" ) </span><span class="sxs-lookup"><span data-stu-id="05025-398">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Functions")</span></span>
</dt> </dl>

<span data-ttu-id="05025-399">製造商的識別碼： Windows CD 光碟機的名稱。</span><span class="sxs-lookup"><span data-stu-id="05025-399">Manufacturer's identifying name of the Windows CD ROM drive.</span></span>

<span data-ttu-id="05025-400">範例： "PLEXTOR CD-ROM PX-12CS 1.01"</span><span class="sxs-lookup"><span data-stu-id="05025-400">Example: "PLEXTOR CD-ROM PX-12CS 1.01"</span></span>

</dd> <dt>

<span data-ttu-id="05025-401">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="05025-401">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-402">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="05025-402">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="05025-403">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-404">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="05025-404">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="05025-405">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="05025-405">Date and time the object was installed.</span></span> <span data-ttu-id="05025-406">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="05025-406">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="05025-407">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-407">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="05025-408">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="05025-408">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-409">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="05025-409">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05025-410">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05025-411">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="05025-411">Last error code reported by the logical device.</span></span>

<span data-ttu-id="05025-412">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-412">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05025-413">**製造商**</span><span class="sxs-lookup"><span data-stu-id="05025-413">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-414">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05025-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05025-415">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-416">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry" ) </span><span class="sxs-lookup"><span data-stu-id="05025-416">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="05025-417">Windows CD-ROM 光碟機的製造商。</span><span class="sxs-lookup"><span data-stu-id="05025-417">Manufacturer of the Windows CD-ROM drive.</span></span>

<span data-ttu-id="05025-418">範例： "PLEXTOR"</span><span class="sxs-lookup"><span data-stu-id="05025-418">Example: "PLEXTOR"</span></span>

</dd> <dt>

<span data-ttu-id="05025-419">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="05025-419">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-420">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="05025-420">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="05025-421">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-422">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="05025-422">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="05025-423">此裝置所存取媒體的最大區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="05025-423">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="05025-424">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-424">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="05025-425">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-425">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="05025-426">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="05025-426">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-427">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="05025-427">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="05025-428">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-429">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 順序存取裝置 \| 001.2 「) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「kb」 ) </span><span class="sxs-lookup"><span data-stu-id="05025-429">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="05025-430">此裝置支援的媒體大小上限（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="05025-430">Maximum size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="05025-431">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-431">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="05025-432">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-432">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="05025-433">**MaxPartitionCount**</span><span class="sxs-lookup"><span data-stu-id="05025-433">**MaxPartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-434">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="05025-434">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05025-435">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05025-436">磁帶機的最大分割區計數。</span><span class="sxs-lookup"><span data-stu-id="05025-436">Maximum partition count for the tape drive.</span></span>

<span data-ttu-id="05025-437">這個屬性繼承自 [**CIM \_ disable-tapedrive**](cim-tapedrive.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-437">This property is inherited from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

</dd> <dt>

<span data-ttu-id="05025-438">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="05025-438">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-439">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05025-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05025-440">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-441">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32 \_ disable-tapedrive \| 媒體媒體磁片 \| 磁碟機" ) </span><span class="sxs-lookup"><span data-stu-id="05025-441">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_TapeDrive\|MediaType\|Tape Drive")</span></span>
</dt> </dl>

<span data-ttu-id="05025-442"> (所使用的媒體類型或) 此裝置所存取的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="05025-442">Media type used by (or accessed by) this device.</span></span> <span data-ttu-id="05025-443">在此情況下，它會設定為「磁帶機」。</span><span class="sxs-lookup"><span data-stu-id="05025-443">In this case, it is set to "Tape Drive".</span></span>

</dd> <dt>

<span data-ttu-id="05025-444">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="05025-444">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-445">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="05025-445">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="05025-446">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-447">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="05025-447">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="05025-448">此裝置所存取媒體的區塊大小下限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="05025-448">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="05025-449">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-449">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="05025-450">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-450">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="05025-451">**名稱**</span><span class="sxs-lookup"><span data-stu-id="05025-451">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-452">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05025-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05025-453">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-454">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="05025-454">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="05025-455">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="05025-455">Label by which the object is known.</span></span> <span data-ttu-id="05025-456">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="05025-456">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="05025-457">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-457">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="05025-458">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="05025-458">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-459">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="05025-459">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05025-460">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05025-461">若 **為 TRUE**，則媒體存取裝置需要清除。</span><span class="sxs-lookup"><span data-stu-id="05025-461">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="05025-462">在 [ **功能** ] 屬性中，是否可能指出手動或自動清除。</span><span class="sxs-lookup"><span data-stu-id="05025-462">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="05025-463">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-463">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05025-464">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="05025-464">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-465">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="05025-465">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05025-466">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-466">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05025-467">支援的) 時，可支援或插入媒體存取裝置 (的個別媒體數目上限。</span><span class="sxs-lookup"><span data-stu-id="05025-467">Maximum number of individual media which can be supported or inserted in the media access device (when supported).</span></span>

<span data-ttu-id="05025-468">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-468">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05025-469">**填補**</span><span class="sxs-lookup"><span data-stu-id="05025-469">**Padding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-470">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="05025-470">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05025-471">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-471">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-472">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="05025-472">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="05025-473">在磁帶媒體上的區塊之間插入的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="05025-473">Number of bytes inserted between blocks on a tape media.</span></span>

<span data-ttu-id="05025-474">這個屬性繼承自 [**CIM \_ disable-tapedrive**](cim-tapedrive.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-474">This property is inherited from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

</dd> <dt>

<span data-ttu-id="05025-475">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="05025-475">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-476">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05025-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05025-477">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-478">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="05025-478">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="05025-479">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="05025-479">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="05025-480">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-480">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="05025-481">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="05025-481">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="05025-482">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="05025-482">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-483">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="05025-483">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="05025-484">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-484">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05025-485">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="05025-485">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="05025-486">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="05025-486">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="05025-487"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="05025-487"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="05025-488"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="05025-488"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="05025-489">此裝置不支援與電源相關的容量。</span><span class="sxs-lookup"><span data-stu-id="05025-489">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="05025-490"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="05025-490"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="05025-491"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="05025-491"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="05025-492">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="05025-492">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="05025-493"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="05025-493"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="05025-494">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="05025-494">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="05025-495"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="05025-495"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="05025-496">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="05025-496">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="05025-497">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="05025-497">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="05025-498">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](../wmisdk/designing-managed-object-format--mof--classes.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-498">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="05025-499"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="05025-499"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="05025-500">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="05025-500">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="05025-501"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="05025-501"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="05025-502">支援計時 Power-On</span><span class="sxs-lookup"><span data-stu-id="05025-502">Timed Power-On Supported</span></span>

<span data-ttu-id="05025-503">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="05025-503">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="05025-504">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="05025-504">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-505">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="05025-505">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05025-506">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-506">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05025-507">若 **為 TRUE**，則裝置可以是電源管理 (可進入暫停模式，依此類推) 。</span><span class="sxs-lookup"><span data-stu-id="05025-507">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="05025-508">屬性不表示電源管理功能目前已啟用，只有邏輯裝置能夠進行電源管理。</span><span class="sxs-lookup"><span data-stu-id="05025-508">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="05025-509">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-509">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05025-510">**ReportSetMarks**</span><span class="sxs-lookup"><span data-stu-id="05025-510">**ReportSetMarks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-511">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="05025-511">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05025-512">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-513">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 磁帶備份結構 \| [**磁帶 \_ 取得 \_ 磁片磁碟機 \_ 參數**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| ReportSetmarks" ) </span><span class="sxs-lookup"><span data-stu-id="05025-513">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|ReportSetmarks")</span></span>
</dt> </dl>

<span data-ttu-id="05025-514">若 **為 TRUE**，則會啟用 setmark 報告。</span><span class="sxs-lookup"><span data-stu-id="05025-514">If **TRUE**, setmark reporting is enabled.</span></span> <span data-ttu-id="05025-515">Setmark 報告使用未包含使用者資料的特製化記錄元素。</span><span class="sxs-lookup"><span data-stu-id="05025-515">Setmark reporting makes use of a specialized recorded element that does not contain user data.</span></span> <span data-ttu-id="05025-516">這個錄製的元素可用來提供以階層方式優於標記的分割配置。</span><span class="sxs-lookup"><span data-stu-id="05025-516">This recorded element is used to provide a segmentation scheme that is hierarchically superior to filemarks.</span></span> <span data-ttu-id="05025-517">Setmarks 可讓您更快速地在高容量磁帶上定位。</span><span class="sxs-lookup"><span data-stu-id="05025-517">Setmarks provide faster positioning on high-capacity tapes.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="05025-518"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="05025-518"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="05025-519">FALSE</span><span class="sxs-lookup"><span data-stu-id="05025-519">FALSE</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="05025-520"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="05025-520"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="05025-521">true</span><span class="sxs-lookup"><span data-stu-id="05025-521">TRUE</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="05025-522">**狀態**</span><span class="sxs-lookup"><span data-stu-id="05025-522">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-523">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05025-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05025-524">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-525">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="05025-525">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="05025-526">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="05025-526">Current status of the object.</span></span> <span data-ttu-id="05025-527">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="05025-527">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="05025-528">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="05025-528">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="05025-529">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="05025-529">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="05025-530">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="05025-530">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="05025-531">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="05025-531">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="05025-532">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-532">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="05025-533">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="05025-533">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="05025-534">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="05025-534">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="05025-535">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="05025-535">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="05025-536">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="05025-536">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="05025-537">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="05025-537">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="05025-538">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="05025-538">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="05025-539">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="05025-539">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="05025-540">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="05025-540">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="05025-541">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="05025-541">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="05025-542">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="05025-542">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="05025-543">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="05025-543">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="05025-544">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="05025-544">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="05025-545">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="05025-545">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="05025-546">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="05025-546">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-547">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="05025-547">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="05025-548">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-549">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="05025-549">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="05025-550">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="05025-550">State of the logical device.</span></span> <span data-ttu-id="05025-551">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="05025-551">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="05025-552">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-552">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="05025-553">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="05025-553">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="05025-554">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="05025-554">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="05025-555">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="05025-555">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="05025-556">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="05025-556">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="05025-557">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="05025-557">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="05025-558">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="05025-558">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-559">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05025-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05025-560">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-560">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-561">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="05025-561">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="05025-562">範圍電腦之 **CreationClassName** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="05025-562">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="05025-563">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-563">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05025-564">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="05025-564">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05025-565">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05025-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05025-566">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05025-566">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05025-567">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="05025-567">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="05025-568">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="05025-568">Name of the scoping system.</span></span>

<span data-ttu-id="05025-569">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-569">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05025-570">備註</span><span class="sxs-lookup"><span data-stu-id="05025-570">Remarks</span></span>

<span data-ttu-id="05025-571">**Win32 \_ disable-tapedrive** 類別衍生自 [**CIM \_ disable-tapedrive**](cim-tapedrive.md)。</span><span class="sxs-lookup"><span data-stu-id="05025-571">The **Win32\_TapeDrive** class is derived from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05025-572">規格需求</span><span class="sxs-lookup"><span data-stu-id="05025-572">Requirements</span></span>



| <span data-ttu-id="05025-573">需求</span><span class="sxs-lookup"><span data-stu-id="05025-573">Requirement</span></span> | <span data-ttu-id="05025-574">值</span><span class="sxs-lookup"><span data-stu-id="05025-574">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05025-575">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="05025-575">Minimum supported client</span></span><br/> | <span data-ttu-id="05025-576">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="05025-576">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="05025-577">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="05025-577">Minimum supported server</span></span><br/> | <span data-ttu-id="05025-578">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="05025-578">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="05025-579">命名空間</span><span class="sxs-lookup"><span data-stu-id="05025-579">Namespace</span></span><br/>                | <span data-ttu-id="05025-580">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="05025-580">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="05025-581">MOF</span><span class="sxs-lookup"><span data-stu-id="05025-581">MOF</span></span><br/>                      | <dl> <span data-ttu-id="05025-582"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="05025-582"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="05025-583">DLL</span><span class="sxs-lookup"><span data-stu-id="05025-583">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05025-584"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05025-584"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05025-585">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05025-585">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05025-586">**CIM \_ disable-tapedrive**</span><span class="sxs-lookup"><span data-stu-id="05025-586">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> <dt>

[<span data-ttu-id="05025-587">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="05025-587">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
