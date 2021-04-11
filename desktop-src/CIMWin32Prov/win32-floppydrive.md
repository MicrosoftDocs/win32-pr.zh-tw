---
description: Win32 \_ FLOPPYDRIVE WMI 類別會管理軟碟磁碟機的功能。
ms.assetid: 41823eeb-4831-4deb-a798-7b3589ebf3e2
ms.tgt_platform: multiple
title: Win32_FloppyDrive 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_FloppyDrive
- Win32_FloppyDrive.Reset
- Win32_FloppyDrive.SetPowerState
- Win32_FloppyDrive.Availability
- Win32_FloppyDrive.Capabilities
- Win32_FloppyDrive.CapabilityDescriptions
- Win32_FloppyDrive.Caption
- Win32_FloppyDrive.CompressionMethod
- Win32_FloppyDrive.ConfigManagerErrorCode
- Win32_FloppyDrive.ConfigManagerUserConfig
- Win32_FloppyDrive.CreationClassName
- Win32_FloppyDrive.DefaultBlockSize
- Win32_FloppyDrive.Description
- Win32_FloppyDrive.DeviceID
- Win32_FloppyDrive.ErrorCleared
- Win32_FloppyDrive.ErrorDescription
- Win32_FloppyDrive.ErrorMethodology
- Win32_FloppyDrive.InstallDate
- Win32_FloppyDrive.LastErrorCode
- Win32_FloppyDrive.Manufacturer
- Win32_FloppyDrive.MaxBlockSize
- Win32_FloppyDrive.MaxMediaSize
- Win32_FloppyDrive.MinBlockSize
- Win32_FloppyDrive.Name
- Win32_FloppyDrive.NeedsCleaning
- Win32_FloppyDrive.NumberOfMediaSupported
- Win32_FloppyDrive.PNPDeviceID
- Win32_FloppyDrive.PowerManagementCapabilities
- Win32_FloppyDrive.PowerManagementSupported
- Win32_FloppyDrive.Status
- Win32_FloppyDrive.StatusInfo
- Win32_FloppyDrive.SystemCreationClassName
- Win32_FloppyDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 832b5fad0ce54d1436fd6b2e47765af0fabfd2bb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111216"
---
# <a name="win32_floppydrive-class"></a><span data-ttu-id="3d158-103">Win32 \_ FloppyDrive 類別</span><span class="sxs-lookup"><span data-stu-id="3d158-103">Win32\_FloppyDrive class</span></span>

<span data-ttu-id="3d158-104">\[**Win32 \_FloppyDrive** 不再適用于 Windows 10 和 Windows Server 2016。\]</span><span class="sxs-lookup"><span data-stu-id="3d158-104">\[**Win32\_FloppyDrive** is no longer available for use as of Windows 10 and Windows Server 2016.\]</span></span>

<span data-ttu-id="3d158-105">**Win32 \_ FloppyDrive** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會管理軟碟磁碟機的功能。</span><span class="sxs-lookup"><span data-stu-id="3d158-105">The **Win32\_FloppyDrive** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) manages the functions of a floppy disk drive.</span></span>

<span data-ttu-id="3d158-106">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3d158-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3d158-107">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="3d158-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d158-108">語法</span><span class="sxs-lookup"><span data-stu-id="3d158-108">Syntax</span></span>

``` syntax
[Dynamic, provider("CIMWin32"), UUID("{FB1F3A64-BBAC-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class Win32_FloppyDrive : CIM_DisketteDrive
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
  string   Manufacturer;
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

## <a name="members"></a><span data-ttu-id="3d158-109">成員</span><span class="sxs-lookup"><span data-stu-id="3d158-109">Members</span></span>

<span data-ttu-id="3d158-110">**Win32 \_ FloppyDrive** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3d158-110">The **Win32\_FloppyDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="3d158-111">方法</span><span class="sxs-lookup"><span data-stu-id="3d158-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="3d158-112">屬性</span><span class="sxs-lookup"><span data-stu-id="3d158-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3d158-113">方法</span><span class="sxs-lookup"><span data-stu-id="3d158-113">Methods</span></span>

<span data-ttu-id="3d158-114">**Win32 \_ FloppyDrive** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3d158-114">The **Win32\_FloppyDrive** class has these methods.</span></span>



| <span data-ttu-id="3d158-115">方法</span><span class="sxs-lookup"><span data-stu-id="3d158-115">Method</span></span>            | <span data-ttu-id="3d158-116">描述</span><span class="sxs-lookup"><span data-stu-id="3d158-116">Description</span></span>                                                                                                                                                                                                                   |
|:------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d158-117">**重設**</span><span class="sxs-lookup"><span data-stu-id="3d158-117">**Reset**</span></span>         | <span data-ttu-id="3d158-118">未實作。</span><span class="sxs-lookup"><span data-stu-id="3d158-118">Not implemented.</span></span> <span data-ttu-id="3d158-119">如需如何執行此方法的詳細資訊，請參閱 [**CIM \_ DisketteDrive**](cim-diskettedrive.md)中的 [**Reset**](reset-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="3d158-119">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_DisketteDrive**](cim-diskettedrive.md).</span></span><br/>                 |
| <span data-ttu-id="3d158-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="3d158-120">**SetPowerState**</span></span> | <span data-ttu-id="3d158-121">未實作。</span><span class="sxs-lookup"><span data-stu-id="3d158-121">Not implemented.</span></span> <span data-ttu-id="3d158-122">如需如何執行此方法的詳細資訊，請參閱 [**CIM \_ DisketteDrive**](cim-diskettedrive.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="3d158-122">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_DisketteDrive**](cim-diskettedrive.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3d158-123">屬性</span><span class="sxs-lookup"><span data-stu-id="3d158-123">Properties</span></span>

<span data-ttu-id="3d158-124">**Win32 \_ FloppyDrive** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3d158-124">The **Win32\_FloppyDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3d158-125">**可用性**</span><span class="sxs-lookup"><span data-stu-id="3d158-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-126">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3d158-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3d158-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d158-128">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="3d158-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="3d158-129">裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="3d158-129">Status of the device.</span></span>

<span data-ttu-id="3d158-130">這個屬性繼承自 [ **CIM \_ LogicalDevice**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="3d158-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md)</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3d158-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="3d158-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3d158-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="3d158-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="3d158-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="3d158-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-134">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="3d158-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="3d158-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="3d158-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="3d158-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="3d158-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="3d158-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="3d158-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="3d158-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="3d158-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="3d158-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="3d158-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="3d158-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="3d158-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3d158-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="3d158-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="3d158-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="3d158-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="3d158-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="3d158-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="3d158-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="3d158-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-145">省電-不明</span><span class="sxs-lookup"><span data-stu-id="3d158-145">Power Save - Unknown</span></span>

<span data-ttu-id="3d158-146">裝置處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="3d158-146">The device in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="3d158-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="3d158-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-148">省電-低電源模式</span><span class="sxs-lookup"><span data-stu-id="3d158-148">Power Save - Low Power Mode</span></span>

<span data-ttu-id="3d158-149">裝置處於省電狀態，但仍正常運作，而且可能會顯示效能下降。</span><span class="sxs-lookup"><span data-stu-id="3d158-149">The device is in a power save state, but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="3d158-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="3d158-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-151">省電-待命</span><span class="sxs-lookup"><span data-stu-id="3d158-151">Power Save - Standby</span></span>

<span data-ttu-id="3d158-152">裝置無法正常運作，但可以快速還原至全電源。</span><span class="sxs-lookup"><span data-stu-id="3d158-152">The device is not functioning, but can be quickly restored to full-power.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="3d158-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="3d158-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="3d158-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="3d158-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-155">省電-警告</span><span class="sxs-lookup"><span data-stu-id="3d158-155">Power Save - Warning</span></span>

<span data-ttu-id="3d158-156">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="3d158-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="3d158-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="3d158-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-158">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="3d158-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="3d158-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="3d158-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-160">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="3d158-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="3d158-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="3d158-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-162">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="3d158-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="3d158-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="3d158-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-164">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="3d158-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3d158-165">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="3d158-165">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-166">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="3d158-166">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3d158-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d158-168">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 儲存裝置 \| 001.9 "，" MIF。DMTF \| 儲存裝置 \| 001.11 "，" MIF。DMTF \| 儲存裝置 \| 001.12 "，" MIF。DMTF \| 磁片 \| 003.7 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。**CapabilityDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="3d158-168">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="3d158-169">媒體存取裝置的功能陣列。</span><span class="sxs-lookup"><span data-stu-id="3d158-169">Array of capabilities of the media access device.</span></span> <span data-ttu-id="3d158-170">例如，裝置可能支援隨機存取、卸載式媒體和自動清除。</span><span class="sxs-lookup"><span data-stu-id="3d158-170">For example, the device may support Random Access, Removable Media, and Automatic Cleaning.</span></span> <span data-ttu-id="3d158-171">在此情況下，會將3、7和9值寫入陣列中。</span><span class="sxs-lookup"><span data-stu-id="3d158-171">In this case, the values 3, 7, and 9 would be written to the array.</span></span>

<span data-ttu-id="3d158-172">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-172">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3d158-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="3d158-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3d158-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="3d158-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="3d158-175"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**順序存取** (2) </span><span class="sxs-lookup"><span data-stu-id="3d158-175"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="3d158-176"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**隨機存取** (3) </span><span class="sxs-lookup"><span data-stu-id="3d158-176"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="3d158-177"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**支援寫入** (4) </span><span class="sxs-lookup"><span data-stu-id="3d158-177"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="3d158-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**加密** (5) </span><span class="sxs-lookup"><span data-stu-id="3d158-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="3d158-179"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**壓縮** (6) </span><span class="sxs-lookup"><span data-stu-id="3d158-179"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="3d158-180"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**支援卸除式媒體** (7) </span><span class="sxs-lookup"><span data-stu-id="3d158-180"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-181">支援卸載式媒體</span><span class="sxs-lookup"><span data-stu-id="3d158-181">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="3d158-182"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**手動清除** (8) </span><span class="sxs-lookup"><span data-stu-id="3d158-182"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="3d158-183"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**自動清除** (9) </span><span class="sxs-lookup"><span data-stu-id="3d158-183"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="3d158-184"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**智慧型通知** (10) </span><span class="sxs-lookup"><span data-stu-id="3d158-184"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="3d158-185"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**支援雙側媒體** (11) </span><span class="sxs-lookup"><span data-stu-id="3d158-185"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-186">支援 Dual-Sided 媒體</span><span class="sxs-lookup"><span data-stu-id="3d158-186">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="3d158-187"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**不需要 Predismount 退出** (12) </span><span class="sxs-lookup"><span data-stu-id="3d158-187"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3d158-188">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="3d158-188">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-189">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="3d158-189">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3d158-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d158-191">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。**功能**") </span><span class="sxs-lookup"><span data-stu-id="3d158-191">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="3d158-192">自由格式字串的陣列，為 **功能** 陣列中指出的任何序列控制器功能提供更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="3d158-192">Array of free-form strings providing more detailed explanations for any of the serial controller features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="3d158-193">請注意，這個陣列的每個專案都與位於相同索引的 **功能** 陣列中的專案相關。</span><span class="sxs-lookup"><span data-stu-id="3d158-193">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="3d158-194">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-194">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d158-195">**標題**</span><span class="sxs-lookup"><span data-stu-id="3d158-195">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-196">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3d158-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d158-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d158-198">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="3d158-198">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3d158-199">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="3d158-199">Short description of the object.</span></span>

<span data-ttu-id="3d158-200">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-200">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d158-201">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="3d158-201">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-202">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3d158-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d158-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d158-204">自由格式字串，指出裝置用來支援壓縮的演算法或工具。</span><span class="sxs-lookup"><span data-stu-id="3d158-204">Free form string indicating the algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="3d158-205">如果不可能或不想要描述壓縮配置 (可能是因為) 不知道，請使用「未知」表示它不知道裝置是否支援壓縮功能;「已壓縮」表示裝置支援壓縮功能，但其壓縮配置未知或未洩漏;和「未壓縮」表示裝置不支援壓縮功能。</span><span class="sxs-lookup"><span data-stu-id="3d158-205">If it is not possible or not desired to describe the compression scheme (perhaps because it is not known), use "Unknown" to represent that it is not known whether the device supports compression capabilities or not; "Compressed" to represent that the device supports compression capabilities, but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the device does not support compression capabilities.</span></span>

<span data-ttu-id="3d158-206">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-206">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="3d158-207"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="3d158-207">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="3d158-208">壓縮配置未知或未描述。</span><span class="sxs-lookup"><span data-stu-id="3d158-208">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="3d158-209"> ( 「壓縮」 ) </span><span class="sxs-lookup"><span data-stu-id="3d158-209">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="3d158-210">邏輯檔案已壓縮，但壓縮配置未知或未描述</span><span class="sxs-lookup"><span data-stu-id="3d158-210">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="3d158-211"> ( 「未壓縮」 ) </span><span class="sxs-lookup"><span data-stu-id="3d158-211">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="3d158-212">如果邏輯檔案未壓縮</span><span class="sxs-lookup"><span data-stu-id="3d158-212">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3d158-213">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="3d158-213">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-214">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="3d158-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d158-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d158-216">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="3d158-216">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3d158-217">Windows 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3d158-217">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="3d158-218">這個屬性繼承自 [ **CIM \_ LogicalDevice**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="3d158-218">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md)</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="3d158-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="3d158-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="3d158-220"> (0)</span><span class="sxs-lookup"><span data-stu-id="3d158-220">(0)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-221">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="3d158-221">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="3d158-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="3d158-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="3d158-223">(1)</span><span class="sxs-lookup"><span data-stu-id="3d158-223">(1)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-224">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="3d158-224">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="3d158-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="3d158-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="3d158-226">(2)</span><span class="sxs-lookup"><span data-stu-id="3d158-226">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="3d158-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="3d158-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="3d158-228">(3)</span><span class="sxs-lookup"><span data-stu-id="3d158-228">(3)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-229">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="3d158-229">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="3d158-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="3d158-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="3d158-231">(4)</span><span class="sxs-lookup"><span data-stu-id="3d158-231">(4)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-232">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="3d158-232">Device is not working properly.</span></span> <span data-ttu-id="3d158-233">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="3d158-233">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="3d158-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="3d158-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="3d158-235">(5)</span><span class="sxs-lookup"><span data-stu-id="3d158-235">(5)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-236">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="3d158-236">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="3d158-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="3d158-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="3d158-238">(6)</span><span class="sxs-lookup"><span data-stu-id="3d158-238">(6)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-239">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="3d158-239">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="3d158-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="3d158-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="3d158-241">(7)</span><span class="sxs-lookup"><span data-stu-id="3d158-241">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="3d158-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="3d158-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="3d158-243">(8)</span><span class="sxs-lookup"><span data-stu-id="3d158-243">(8)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-244">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="3d158-244">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="3d158-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="3d158-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="3d158-246">(9)</span><span class="sxs-lookup"><span data-stu-id="3d158-246">(9)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-247">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="3d158-247">Device is not working properly.</span></span> <span data-ttu-id="3d158-248">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="3d158-248">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="3d158-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="3d158-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="3d158-250">(10)</span><span class="sxs-lookup"><span data-stu-id="3d158-250">(10)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-251">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="3d158-251">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="3d158-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="3d158-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="3d158-253">(11)</span><span class="sxs-lookup"><span data-stu-id="3d158-253">(11)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-254">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="3d158-254">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="3d158-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="3d158-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="3d158-256"> (12) </span><span class="sxs-lookup"><span data-stu-id="3d158-256">(12)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-257">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="3d158-257">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="3d158-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="3d158-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="3d158-259">(13)</span><span class="sxs-lookup"><span data-stu-id="3d158-259">(13)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-260">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="3d158-260">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="3d158-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="3d158-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="3d158-262">(14)</span><span class="sxs-lookup"><span data-stu-id="3d158-262">(14)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-263">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="3d158-263">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="3d158-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="3d158-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="3d158-265">(15)</span><span class="sxs-lookup"><span data-stu-id="3d158-265">(15)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-266">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="3d158-266">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="3d158-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="3d158-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="3d158-268">(16)</span><span class="sxs-lookup"><span data-stu-id="3d158-268">(16)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-269">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="3d158-269">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="3d158-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="3d158-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="3d158-271">(17)</span><span class="sxs-lookup"><span data-stu-id="3d158-271">(17)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-272">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="3d158-272">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="3d158-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="3d158-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="3d158-274">(18)</span><span class="sxs-lookup"><span data-stu-id="3d158-274">(18)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-275">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="3d158-275">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="3d158-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="3d158-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="3d158-277">(19)</span><span class="sxs-lookup"><span data-stu-id="3d158-277">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="3d158-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="3d158-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="3d158-279">(20)</span><span class="sxs-lookup"><span data-stu-id="3d158-279">(20)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-280">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="3d158-280">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="3d158-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="3d158-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="3d158-282">(21)</span><span class="sxs-lookup"><span data-stu-id="3d158-282">(21)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-283">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="3d158-283">System failure.</span></span> <span data-ttu-id="3d158-284">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="3d158-284">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="3d158-285">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="3d158-285">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="3d158-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="3d158-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="3d158-287">(22)</span><span class="sxs-lookup"><span data-stu-id="3d158-287">(22)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-288">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="3d158-288">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="3d158-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="3d158-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="3d158-290">(23)</span><span class="sxs-lookup"><span data-stu-id="3d158-290">(23)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-291">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="3d158-291">System failure.</span></span> <span data-ttu-id="3d158-292">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="3d158-292">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="3d158-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="3d158-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="3d158-294">(24)</span><span class="sxs-lookup"><span data-stu-id="3d158-294">(24)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-295">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="3d158-295">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="3d158-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="3d158-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="3d158-297">(25)</span><span class="sxs-lookup"><span data-stu-id="3d158-297">(25)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-298">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="3d158-298">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="3d158-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="3d158-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="3d158-300">(26)</span><span class="sxs-lookup"><span data-stu-id="3d158-300">(26)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-301">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="3d158-301">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="3d158-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="3d158-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="3d158-303">(27)</span><span class="sxs-lookup"><span data-stu-id="3d158-303">(27)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-304">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="3d158-304">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="3d158-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="3d158-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="3d158-306">(28)</span><span class="sxs-lookup"><span data-stu-id="3d158-306">(28)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-307">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="3d158-307">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="3d158-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="3d158-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="3d158-309">(29)</span><span class="sxs-lookup"><span data-stu-id="3d158-309">(29)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-310">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="3d158-310">Device is disabled.</span></span> <span data-ttu-id="3d158-311">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="3d158-311">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="3d158-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="3d158-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="3d158-313">(30)</span><span class="sxs-lookup"><span data-stu-id="3d158-313">(30)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-314">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="3d158-314">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="3d158-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="3d158-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="3d158-316"> (31) </span><span class="sxs-lookup"><span data-stu-id="3d158-316">(31)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-317">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="3d158-317">Device is not working properly.</span></span> <span data-ttu-id="3d158-318">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="3d158-318">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3d158-319">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="3d158-319">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-320">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3d158-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3d158-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d158-322">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="3d158-322">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3d158-323">若 **為 True**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="3d158-323">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="3d158-324">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d158-325">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3d158-325">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-326">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3d158-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d158-327">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d158-328">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3d158-328">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3d158-329">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="3d158-329">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="3d158-330">搭配類別的其他索引鍵屬性使用時，屬性可讓這個類別的所有實例和其子類別都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="3d158-330">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="3d158-331">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d158-332">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="3d158-332">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-333">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="3d158-333">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3d158-334">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d158-335">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="3d158-335">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3d158-336">此裝置的預設區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3d158-336">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="3d158-337">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-337">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="3d158-338">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="3d158-338">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3d158-339">**說明**</span><span class="sxs-lookup"><span data-stu-id="3d158-339">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-340">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3d158-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d158-341">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d158-342">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="3d158-342">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="3d158-343">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="3d158-343">Description of the object.</span></span>

<span data-ttu-id="3d158-344">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d158-345">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="3d158-345">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-346">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3d158-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d158-347">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d158-348">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3d158-348">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3d158-349">磁片磁碟機的唯一識別碼與系統上的其他裝置。</span><span class="sxs-lookup"><span data-stu-id="3d158-349">Unique identifier of the floppy disk drive with other devices on the system.</span></span>

<span data-ttu-id="3d158-350">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d158-351">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="3d158-351">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-352">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3d158-352">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3d158-353">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d158-354">若 **為 True**，則表示 **LastErrorCode** 中回報的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="3d158-354">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="3d158-355">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-355">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d158-356">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="3d158-356">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-357">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3d158-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d158-358">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d158-359">提供 **LastErrorCode** 所記錄錯誤詳細資訊的自由格式字串，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3d158-359">Free-form string that supplies more information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="3d158-360">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d158-361">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="3d158-361">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-362">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3d158-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d158-363">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d158-364">描述此裝置所支援之錯誤偵測和更正類型的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="3d158-364">Free-form string that describes the type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="3d158-365">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-365">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d158-366">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3d158-366">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-367">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="3d158-367">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3d158-368">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d158-369">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="3d158-369">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3d158-370">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="3d158-370">Date and time the object was installed.</span></span> <span data-ttu-id="3d158-371">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="3d158-371">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="3d158-372">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-372">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d158-373">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="3d158-373">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-374">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="3d158-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d158-375">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d158-376">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3d158-376">Last error code reported by the logical device.</span></span>

<span data-ttu-id="3d158-377">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d158-378">**製造商**</span><span class="sxs-lookup"><span data-stu-id="3d158-378">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-379">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3d158-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d158-380">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d158-381">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry" ) </span><span class="sxs-lookup"><span data-stu-id="3d158-381">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="3d158-382">磁片磁碟機的製造商名稱。</span><span class="sxs-lookup"><span data-stu-id="3d158-382">Name of the manufacturer of the floppy disk drive.</span></span>

<span data-ttu-id="3d158-383">範例： "Acme"</span><span class="sxs-lookup"><span data-stu-id="3d158-383">Example: "Acme"</span></span>

</dd> <dt>

<span data-ttu-id="3d158-384">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="3d158-384">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-385">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="3d158-385">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3d158-386">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d158-387">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="3d158-387">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3d158-388">此裝置所存取媒體的最大區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3d158-388">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="3d158-389">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-389">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="3d158-390">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="3d158-390">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3d158-391">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="3d158-391">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-392">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="3d158-392">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3d158-393">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d158-394">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 順序存取裝置 \| 001.2 「) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「kb」 ) </span><span class="sxs-lookup"><span data-stu-id="3d158-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="3d158-395">此裝置支援的媒體大小上限（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="3d158-395">Maximum size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="3d158-396">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-396">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="3d158-397">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="3d158-397">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3d158-398">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="3d158-398">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-399">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="3d158-399">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3d158-400">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d158-401">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="3d158-401">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3d158-402">此裝置所存取媒體的區塊大小下限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3d158-402">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="3d158-403">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-403">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="3d158-404">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="3d158-404">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3d158-405">**名稱**</span><span class="sxs-lookup"><span data-stu-id="3d158-405">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-406">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3d158-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d158-407">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d158-408">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="3d158-408">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="3d158-409">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="3d158-409">Label by which the object is known.</span></span> <span data-ttu-id="3d158-410">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="3d158-410">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="3d158-411">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-411">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d158-412">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="3d158-412">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-413">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3d158-413">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3d158-414">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d158-415">若 **為 True**，則媒體存取裝置需要清除。</span><span class="sxs-lookup"><span data-stu-id="3d158-415">If **True**, the media access device requires cleaning.</span></span> <span data-ttu-id="3d158-416">在 [ **功能** ] 屬性中，是否可能指出手動或自動清除。</span><span class="sxs-lookup"><span data-stu-id="3d158-416">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="3d158-417">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-417">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d158-418">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="3d158-418">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-419">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="3d158-419">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d158-420">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d158-421">支援的) 時，可支援或插入媒體存取裝置 (的個別媒體數目上限。</span><span class="sxs-lookup"><span data-stu-id="3d158-421">Maximum number of individual media which can be supported or inserted in the media access device (when supported).</span></span>

<span data-ttu-id="3d158-422">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-422">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d158-423">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="3d158-423">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-424">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3d158-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d158-425">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d158-426">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="3d158-426">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3d158-427">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="3d158-427">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="3d158-428">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-428">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="3d158-429">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="3d158-429">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="3d158-430">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="3d158-430">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-431">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="3d158-431">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3d158-432">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d158-433">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="3d158-433">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="3d158-434">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="3d158-434">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3d158-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="3d158-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="3d158-436"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="3d158-436"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3d158-437"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="3d158-437"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="3d158-438"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="3d158-438"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-439">已啟用</span><span class="sxs-lookup"><span data-stu-id="3d158-439">Enabled</span></span>

<span data-ttu-id="3d158-440">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="3d158-440">The power management features are currently enabled, but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="3d158-441"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="3d158-441"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-442">自動輸入的省電模式</span><span class="sxs-lookup"><span data-stu-id="3d158-442">Power Saving Modes Entered Automatically</span></span>

<span data-ttu-id="3d158-443">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="3d158-443">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="3d158-444"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="3d158-444"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-445">可設定的電源狀態</span><span class="sxs-lookup"><span data-stu-id="3d158-445">Power State Settable</span></span>

<span data-ttu-id="3d158-446">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="3d158-446">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="3d158-447">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="3d158-447">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="3d158-448">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="3d158-448">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="3d158-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="3d158-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-450">支援電源迴圈</span><span class="sxs-lookup"><span data-stu-id="3d158-450">Power Cycling Supported</span></span>

<span data-ttu-id="3d158-451">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="3d158-451">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="3d158-452"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="3d158-452"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="3d158-453">支援計時 Power-On</span><span class="sxs-lookup"><span data-stu-id="3d158-453">Timed Power-On Supported</span></span>

<span data-ttu-id="3d158-454">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="3d158-454">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3d158-455">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="3d158-455">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-456">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3d158-456">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3d158-457">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-457">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d158-458">若 **為 True**，則裝置可以是電源管理 (可進入暫停模式，依此類推) 。</span><span class="sxs-lookup"><span data-stu-id="3d158-458">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="3d158-459">屬性不表示電源管理功能目前已啟用，只有邏輯裝置能夠進行電源管理。</span><span class="sxs-lookup"><span data-stu-id="3d158-459">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="3d158-460">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-460">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d158-461">**狀態**</span><span class="sxs-lookup"><span data-stu-id="3d158-461">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-462">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3d158-462">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d158-463">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-463">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d158-464">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="3d158-464">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3d158-465">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="3d158-465">Current status of the object.</span></span> <span data-ttu-id="3d158-466">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="3d158-466">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="3d158-467">作業狀態包括：「確定」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="3d158-467">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly, but predicting a failure in the near future).</span></span> <span data-ttu-id="3d158-468">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="3d158-468">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="3d158-469">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="3d158-469">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="3d158-470">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="3d158-470">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="3d158-471">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-471">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3d158-472">值如下：</span><span class="sxs-lookup"><span data-stu-id="3d158-472">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3d158-473">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="3d158-473">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3d158-474">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="3d158-474">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3d158-475">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="3d158-475">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3d158-476">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="3d158-476">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3d158-477">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="3d158-477">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3d158-478">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="3d158-478">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3d158-479">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="3d158-479">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3d158-480">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="3d158-480">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3d158-481">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="3d158-481">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3d158-482">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="3d158-482">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3d158-483">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="3d158-483">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3d158-484">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="3d158-484">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3d158-485">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="3d158-485">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-486">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3d158-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3d158-487">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d158-488">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="3d158-488">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="3d158-489">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="3d158-489">State of the logical device.</span></span> <span data-ttu-id="3d158-490">如果此屬性不適用於邏輯裝置，則應該使用值 5 ( 「不適用」 ) 。</span><span class="sxs-lookup"><span data-stu-id="3d158-490">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="3d158-491">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3d158-492">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="3d158-492">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3d158-493">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="3d158-493">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="3d158-494">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="3d158-494">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3d158-495">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="3d158-495">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="3d158-496">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="3d158-496">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3d158-497">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3d158-497">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-498">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3d158-498">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d158-499">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d158-500">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3d158-500">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3d158-501">設定電腦 **CreationClassName** 的範圍值屬性值。</span><span class="sxs-lookup"><span data-stu-id="3d158-501">Value of the scoping computer **CreationClassName** property.</span></span> <span data-ttu-id="3d158-502">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-502">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="3d158-503">這個屬性繼承自 [ **CIM \_ LogicalDevice**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="3d158-503">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md)</span></span>

</dd> <dt>

<span data-ttu-id="3d158-504">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="3d158-504">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d158-505">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3d158-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d158-506">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3d158-506">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d158-507">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3d158-507">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3d158-508">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d158-508">Name of the scoping system.</span></span>

<span data-ttu-id="3d158-509">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-509">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d158-510">備註</span><span class="sxs-lookup"><span data-stu-id="3d158-510">Remarks</span></span>

<span data-ttu-id="3d158-511">**Win32 \_ FloppyDrive** 類別衍生自 cim [**\_ DisketteDrive**](cim-diskettedrive.md) ，它衍生自 [**cim \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-511">The **Win32\_FloppyDrive** class is derived from [**CIM\_DisketteDrive**](cim-diskettedrive.md) which derives from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span> <span data-ttu-id="3d158-512">**Cim \_ MediaAccessDevice** 類別衍生自 [**cim \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="3d158-512">The **CIM\_MediaAccessDevice** class derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3d158-513">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d158-513">Requirements</span></span>



| <span data-ttu-id="3d158-514">需求</span><span class="sxs-lookup"><span data-stu-id="3d158-514">Requirement</span></span> | <span data-ttu-id="3d158-515">值</span><span class="sxs-lookup"><span data-stu-id="3d158-515">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d158-516">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3d158-516">Minimum supported client</span></span><br/> | <span data-ttu-id="3d158-517">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d158-517">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3d158-518">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3d158-518">Minimum supported server</span></span><br/> | <span data-ttu-id="3d158-519">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d158-519">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3d158-520">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="3d158-520">End of client support</span></span><br/>    | <span data-ttu-id="3d158-521">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3d158-521">Windows 8.1</span></span><br/>                                                                  |
| <span data-ttu-id="3d158-522">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="3d158-522">End of server support</span></span><br/>    | <span data-ttu-id="3d158-523">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3d158-523">Windows Server 2012 R2</span></span><br/>                                                       |
| <span data-ttu-id="3d158-524">命名空間</span><span class="sxs-lookup"><span data-stu-id="3d158-524">Namespace</span></span><br/>                | <span data-ttu-id="3d158-525">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3d158-525">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3d158-526">MOF</span><span class="sxs-lookup"><span data-stu-id="3d158-526">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d158-527"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d158-527"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d158-528">DLL</span><span class="sxs-lookup"><span data-stu-id="3d158-528">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d158-529"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d158-529"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d158-530">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d158-530">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d158-531">**CIM \_ DisketteDrive**</span><span class="sxs-lookup"><span data-stu-id="3d158-531">**CIM\_DisketteDrive**</span></span>](cim-diskettedrive.md)
</dt> <dt>

[<span data-ttu-id="3d158-532">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="3d158-532">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

