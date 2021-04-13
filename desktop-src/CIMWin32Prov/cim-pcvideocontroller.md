---
description: CIM \_ PCVideoController 代表個人電腦影片控制器的功能和管理，也就是影片控制器的子類型。
ms.assetid: bf937727-a332-445b-9397-7d87d58c4a5b
ms.tgt_platform: multiple
title: CIM_PCVideoController 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCVideoController
- CIM_PCVideoController.AcceleratorCapabilities
- CIM_PCVideoController.Availability
- CIM_PCVideoController.CapabilityDescriptions
- CIM_PCVideoController.Caption
- CIM_PCVideoController.ConfigManagerErrorCode
- CIM_PCVideoController.ConfigManagerUserConfig
- CIM_PCVideoController.CreationClassName
- CIM_PCVideoController.CurrentBitsPerPixel
- CIM_PCVideoController.CurrentHorizontalResolution
- CIM_PCVideoController.CurrentNumberOfColors
- CIM_PCVideoController.CurrentNumberOfColumns
- CIM_PCVideoController.CurrentNumberOfRows
- CIM_PCVideoController.CurrentRefreshRate
- CIM_PCVideoController.CurrentScanMode
- CIM_PCVideoController.CurrentVerticalResolution
- CIM_PCVideoController.Description
- CIM_PCVideoController.DeviceID
- CIM_PCVideoController.ErrorCleared
- CIM_PCVideoController.ErrorDescription
- CIM_PCVideoController.InstallDate
- CIM_PCVideoController.LastErrorCode
- CIM_PCVideoController.MaxMemorySupported
- CIM_PCVideoController.MaxNumberControlled
- CIM_PCVideoController.MaxRefreshRate
- CIM_PCVideoController.MinRefreshRate
- CIM_PCVideoController.Name
- CIM_PCVideoController.NumberOfColorPlanes
- CIM_PCVideoController.NumberOfVideoPages
- CIM_PCVideoController.PNPDeviceID
- CIM_PCVideoController.PowerManagementCapabilities
- CIM_PCVideoController.PowerManagementSupported
- CIM_PCVideoController.ProtocolSupported
- CIM_PCVideoController.Status
- CIM_PCVideoController.StatusInfo
- CIM_PCVideoController.SystemCreationClassName
- CIM_PCVideoController.SystemName
- CIM_PCVideoController.TimeOfLastReset
- CIM_PCVideoController.VideoArchitecture
- CIM_PCVideoController.VideoMemoryType
- CIM_PCVideoController.VideoMode
- CIM_PCVideoController.VideoProcessor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 94465862c34cc9c6fb645f63c0add48d0fded56b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385952"
---
# <a name="cim_pcvideocontroller-class"></a><span data-ttu-id="06128-103">CIM \_ PCVideoController 類別</span><span class="sxs-lookup"><span data-stu-id="06128-103">CIM\_PCVideoController class</span></span>

<span data-ttu-id="06128-104">**CIM \_ PCVideoController** 代表個人電腦影片控制器的功能和管理，也就是影片控制器的子類型。</span><span class="sxs-lookup"><span data-stu-id="06128-104">The **CIM\_PCVideoController** represents the capabilities and management of a personal computer video controller, a subtype of a video controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="06128-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="06128-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="06128-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="06128-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="06128-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="06128-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="06128-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="06128-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="06128-109">語法</span><span class="sxs-lookup"><span data-stu-id="06128-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCE6-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_PCVideoController : CIM_VideoController
{
  uint16   AcceleratorCapabilities[];
  uint16   Availability;
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint32   CurrentBitsPerPixel;
  uint32   CurrentHorizontalResolution;
  uint64   CurrentNumberOfColors;
  uint32   CurrentNumberOfColumns;
  uint32   CurrentNumberOfRows;
  uint32   CurrentRefreshRate;
  uint16   CurrentScanMode;
  uint32   CurrentVerticalResolution;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxMemorySupported;
  uint32   MaxNumberControlled;
  uint32   MaxRefreshRate;
  uint32   MinRefreshRate;
  string   Name;
  uint16   NumberOfColorPlanes;
  uint32   NumberOfVideoPages;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
  uint16   VideoArchitecture;
  uint16   VideoMemoryType;
  uint16   VideoMode;
  string   VideoProcessor;
};
```

## <a name="members"></a><span data-ttu-id="06128-110">成員</span><span class="sxs-lookup"><span data-stu-id="06128-110">Members</span></span>

<span data-ttu-id="06128-111">**CIM \_ PCVideoController** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="06128-111">The **CIM\_PCVideoController** class has these types of members:</span></span>

-   [<span data-ttu-id="06128-112">方法</span><span class="sxs-lookup"><span data-stu-id="06128-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="06128-113">屬性</span><span class="sxs-lookup"><span data-stu-id="06128-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="06128-114">方法</span><span class="sxs-lookup"><span data-stu-id="06128-114">Methods</span></span>

<span data-ttu-id="06128-115">**CIM \_ PCVideoController** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="06128-115">The **CIM\_PCVideoController** class has these methods.</span></span>



| <span data-ttu-id="06128-116">方法</span><span class="sxs-lookup"><span data-stu-id="06128-116">Method</span></span>                                                                       | <span data-ttu-id="06128-117">描述</span><span class="sxs-lookup"><span data-stu-id="06128-117">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06128-118">**重設**</span><span class="sxs-lookup"><span data-stu-id="06128-118">**Reset**</span></span>](reset-method-in-class-cim-pcvideocontroller.md)                 | <span data-ttu-id="06128-119">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="06128-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="06128-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="06128-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="06128-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="06128-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-pcvideocontroller.md) | <span data-ttu-id="06128-122">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="06128-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="06128-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="06128-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="06128-124">屬性</span><span class="sxs-lookup"><span data-stu-id="06128-124">Properties</span></span>

<span data-ttu-id="06128-125">**CIM \_ PCVideoController** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="06128-125">The **CIM\_PCVideoController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="06128-126">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="06128-126">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-127">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="06128-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="06128-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-129">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VideoController**](cim-videocontroller.md).**CapabilityDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="06128-129">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="06128-130">影片控制器的圖形和3D 功能。</span><span class="sxs-lookup"><span data-stu-id="06128-130">Graphics and 3-D capabilities of the video controller.</span></span>

<span data-ttu-id="06128-131">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-131">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06128-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="06128-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="06128-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="06128-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="06128-134"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**圖形加速器** (2) </span><span class="sxs-lookup"><span data-stu-id="06128-134"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="06128-135"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**3D 加速器** (3) </span><span class="sxs-lookup"><span data-stu-id="06128-135"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**3D Accelerator** (3)</span></span>


</dt> <dd>

<span data-ttu-id="06128-136">3-d 加速器</span><span class="sxs-lookup"><span data-stu-id="06128-136">3-D accelerator</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="06128-137">**可用性**</span><span class="sxs-lookup"><span data-stu-id="06128-137">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-138">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06128-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06128-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-140">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="06128-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="06128-141">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="06128-141">Availability and status of the device.</span></span>

<span data-ttu-id="06128-142">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="06128-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="06128-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06128-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="06128-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="06128-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="06128-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="06128-146">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="06128-146">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="06128-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="06128-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="06128-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="06128-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="06128-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="06128-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="06128-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="06128-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="06128-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="06128-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="06128-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="06128-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="06128-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="06128-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="06128-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="06128-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="06128-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="06128-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="06128-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="06128-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="06128-157">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="06128-157">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="06128-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="06128-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="06128-159">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="06128-159">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="06128-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="06128-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="06128-161">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="06128-161">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="06128-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="06128-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="06128-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="06128-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="06128-164">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="06128-164">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="06128-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="06128-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="06128-166">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="06128-166">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="06128-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="06128-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="06128-168">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="06128-168">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="06128-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="06128-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="06128-170">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="06128-170">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="06128-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="06128-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="06128-172">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="06128-172">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="06128-173">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="06128-173">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-174">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="06128-174">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="06128-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-176">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VideoController**](cim-videocontroller.md)。**AcceleratorCapabilities**") </span><span class="sxs-lookup"><span data-stu-id="06128-176">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="06128-177">提供 **AcceleratorCapabilities** 陣列中所指出的影片加速器功能詳細說明的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="06128-177">Free-form strings that provide detailed explanations for video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="06128-178">每個陣列專案都與 **AcceleratorCapabilities** 陣列中位於相同索引的專案相關。</span><span class="sxs-lookup"><span data-stu-id="06128-178">Each array entry is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span>

 

<span data-ttu-id="06128-179">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-179">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="06128-180">**標題**</span><span class="sxs-lookup"><span data-stu-id="06128-180">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-181">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06128-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06128-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-183">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="06128-183">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="06128-184">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="06128-184">Short textual description of the object.</span></span>

<span data-ttu-id="06128-185">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-185">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="06128-186">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="06128-186">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-187">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="06128-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06128-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-189">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="06128-189">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="06128-190">Windows 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="06128-190">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="06128-191">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-191">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="06128-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="06128-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="06128-193"> (0)</span><span class="sxs-lookup"><span data-stu-id="06128-193">(0)</span></span>


</dt> <dd>

<span data-ttu-id="06128-194">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="06128-194">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="06128-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="06128-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="06128-196">(1)</span><span class="sxs-lookup"><span data-stu-id="06128-196">(1)</span></span>


</dt> <dd>

<span data-ttu-id="06128-197">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="06128-197">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="06128-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="06128-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="06128-199">(2)</span><span class="sxs-lookup"><span data-stu-id="06128-199">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="06128-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="06128-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="06128-201">(3)</span><span class="sxs-lookup"><span data-stu-id="06128-201">(3)</span></span>


</dt> <dd>

<span data-ttu-id="06128-202">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="06128-202">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="06128-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="06128-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="06128-204">(4)</span><span class="sxs-lookup"><span data-stu-id="06128-204">(4)</span></span>


</dt> <dd>

<span data-ttu-id="06128-205">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="06128-205">Device is not working properly.</span></span> <span data-ttu-id="06128-206">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="06128-206">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="06128-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="06128-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="06128-208">(5)</span><span class="sxs-lookup"><span data-stu-id="06128-208">(5)</span></span>


</dt> <dd>

<span data-ttu-id="06128-209">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="06128-209">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="06128-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="06128-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="06128-211">(6)</span><span class="sxs-lookup"><span data-stu-id="06128-211">(6)</span></span>


</dt> <dd>

<span data-ttu-id="06128-212">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="06128-212">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="06128-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="06128-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="06128-214">(7)</span><span class="sxs-lookup"><span data-stu-id="06128-214">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="06128-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="06128-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="06128-216">(8)</span><span class="sxs-lookup"><span data-stu-id="06128-216">(8)</span></span>


</dt> <dd>

<span data-ttu-id="06128-217">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="06128-217">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="06128-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="06128-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="06128-219">(9)</span><span class="sxs-lookup"><span data-stu-id="06128-219">(9)</span></span>


</dt> <dd>

<span data-ttu-id="06128-220">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="06128-220">Device is not working properly.</span></span> <span data-ttu-id="06128-221">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="06128-221">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="06128-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="06128-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="06128-223">(10)</span><span class="sxs-lookup"><span data-stu-id="06128-223">(10)</span></span>


</dt> <dd>

<span data-ttu-id="06128-224">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="06128-224">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="06128-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="06128-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="06128-226">(11)</span><span class="sxs-lookup"><span data-stu-id="06128-226">(11)</span></span>


</dt> <dd>

<span data-ttu-id="06128-227">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="06128-227">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="06128-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="06128-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="06128-229"> (12) </span><span class="sxs-lookup"><span data-stu-id="06128-229">(12)</span></span>


</dt> <dd>

<span data-ttu-id="06128-230">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="06128-230">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="06128-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="06128-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="06128-232">(13)</span><span class="sxs-lookup"><span data-stu-id="06128-232">(13)</span></span>


</dt> <dd>

<span data-ttu-id="06128-233">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="06128-233">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="06128-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="06128-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="06128-235">(14)</span><span class="sxs-lookup"><span data-stu-id="06128-235">(14)</span></span>


</dt> <dd>

<span data-ttu-id="06128-236">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="06128-236">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="06128-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="06128-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="06128-238">(15)</span><span class="sxs-lookup"><span data-stu-id="06128-238">(15)</span></span>


</dt> <dd>

<span data-ttu-id="06128-239">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="06128-239">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="06128-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="06128-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="06128-241">(16)</span><span class="sxs-lookup"><span data-stu-id="06128-241">(16)</span></span>


</dt> <dd>

<span data-ttu-id="06128-242">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="06128-242">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="06128-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="06128-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="06128-244">(17)</span><span class="sxs-lookup"><span data-stu-id="06128-244">(17)</span></span>


</dt> <dd>

<span data-ttu-id="06128-245">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="06128-245">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="06128-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="06128-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="06128-247">(18)</span><span class="sxs-lookup"><span data-stu-id="06128-247">(18)</span></span>


</dt> <dd>

<span data-ttu-id="06128-248">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="06128-248">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="06128-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="06128-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="06128-250">(19)</span><span class="sxs-lookup"><span data-stu-id="06128-250">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="06128-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="06128-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="06128-252">(20)</span><span class="sxs-lookup"><span data-stu-id="06128-252">(20)</span></span>


</dt> <dd>

<span data-ttu-id="06128-253">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="06128-253">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="06128-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="06128-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="06128-255">(21)</span><span class="sxs-lookup"><span data-stu-id="06128-255">(21)</span></span>


</dt> <dd>

<span data-ttu-id="06128-256">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="06128-256">System failure.</span></span> <span data-ttu-id="06128-257">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="06128-257">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="06128-258">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="06128-258">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="06128-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="06128-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="06128-260">(22)</span><span class="sxs-lookup"><span data-stu-id="06128-260">(22)</span></span>


</dt> <dd>

<span data-ttu-id="06128-261">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="06128-261">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="06128-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="06128-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="06128-263">(23)</span><span class="sxs-lookup"><span data-stu-id="06128-263">(23)</span></span>


</dt> <dd>

<span data-ttu-id="06128-264">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="06128-264">System failure.</span></span> <span data-ttu-id="06128-265">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="06128-265">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="06128-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="06128-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="06128-267">(24)</span><span class="sxs-lookup"><span data-stu-id="06128-267">(24)</span></span>


</dt> <dd>

<span data-ttu-id="06128-268">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="06128-268">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="06128-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="06128-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="06128-270">(25)</span><span class="sxs-lookup"><span data-stu-id="06128-270">(25)</span></span>


</dt> <dd>

<span data-ttu-id="06128-271">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="06128-271">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="06128-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="06128-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="06128-273">(26)</span><span class="sxs-lookup"><span data-stu-id="06128-273">(26)</span></span>


</dt> <dd>

<span data-ttu-id="06128-274">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="06128-274">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="06128-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="06128-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="06128-276">(27)</span><span class="sxs-lookup"><span data-stu-id="06128-276">(27)</span></span>


</dt> <dd>

<span data-ttu-id="06128-277">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="06128-277">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="06128-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="06128-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="06128-279">(28)</span><span class="sxs-lookup"><span data-stu-id="06128-279">(28)</span></span>


</dt> <dd>

<span data-ttu-id="06128-280">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="06128-280">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="06128-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="06128-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="06128-282">(29)</span><span class="sxs-lookup"><span data-stu-id="06128-282">(29)</span></span>


</dt> <dd>

<span data-ttu-id="06128-283">裝置已停用;裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="06128-283">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="06128-284"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="06128-284"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="06128-285">(30)</span><span class="sxs-lookup"><span data-stu-id="06128-285">(30)</span></span>


</dt> <dd>

<span data-ttu-id="06128-286">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="06128-286">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="06128-287"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="06128-287"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="06128-288"> (31) </span><span class="sxs-lookup"><span data-stu-id="06128-288">(31)</span></span>


</dt> <dd>

<span data-ttu-id="06128-289">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="06128-289">Device is not working properly.</span></span> <span data-ttu-id="06128-290">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="06128-290">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="06128-291">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="06128-291">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-292">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="06128-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06128-293">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-294">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="06128-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="06128-295">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="06128-295">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="06128-296">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="06128-297">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="06128-297">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-298">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06128-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06128-299">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-300">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="06128-300">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="06128-301">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="06128-301">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="06128-302">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="06128-302">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="06128-303">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-303">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="06128-304">**CurrentBitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="06128-304">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-305">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="06128-305">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06128-306">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-307">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 003.12 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ") </span><span class="sxs-lookup"><span data-stu-id="06128-307">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="06128-308">用來顯示每個圖元的位數。</span><span class="sxs-lookup"><span data-stu-id="06128-308">Number of bits used to display each pixel.</span></span>

<span data-ttu-id="06128-309">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-309">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="06128-310">**CurrentHorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="06128-310">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-311">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="06128-311">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06128-312">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-313">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 003.11 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 圖元 ") </span><span class="sxs-lookup"><span data-stu-id="06128-313">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="06128-314">目前的水準圖元數目。</span><span class="sxs-lookup"><span data-stu-id="06128-314">Current number of horizontal pixels.</span></span>

<span data-ttu-id="06128-315">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-315">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="06128-316">**CurrentNumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="06128-316">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-317">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="06128-317">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06128-318">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06128-319">目前的解析度所支援的色彩數目。</span><span class="sxs-lookup"><span data-stu-id="06128-319">Number of colors supported at the current resolutions.</span></span>

<span data-ttu-id="06128-320">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-320">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<span data-ttu-id="06128-321">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="06128-321">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="06128-322">**CurrentNumberOfColumns**</span><span class="sxs-lookup"><span data-stu-id="06128-322">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-323">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="06128-323">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06128-324">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-325">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 003.14 ") </span><span class="sxs-lookup"><span data-stu-id="06128-325">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.14")</span></span>
</dt> </dl>

<span data-ttu-id="06128-326">如果在字元模式中，則為影片控制器的欄數;否則，請輸入0。</span><span class="sxs-lookup"><span data-stu-id="06128-326">If in character mode, number of columns for the video controller; otherwise, enter 0.</span></span>

<span data-ttu-id="06128-327">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-327">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="06128-328">**CurrentNumberOfRows**</span><span class="sxs-lookup"><span data-stu-id="06128-328">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-329">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="06128-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06128-330">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-331">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 003.13 ") </span><span class="sxs-lookup"><span data-stu-id="06128-331">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="06128-332">如果在字元模式中，則為此影片控制器的資料列數目;否則，請輸入0。</span><span class="sxs-lookup"><span data-stu-id="06128-332">If in character mode, number of rows for this video controller; otherwise, enter 0.</span></span>

<span data-ttu-id="06128-333">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-333">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="06128-334">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="06128-334">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-335">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="06128-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06128-336">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-337">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 003.15 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 赫茲 ") </span><span class="sxs-lookup"><span data-stu-id="06128-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="06128-338">目前的更新速率（以赫茲為單位）。</span><span class="sxs-lookup"><span data-stu-id="06128-338">Current refresh rate in hertz.</span></span>

<span data-ttu-id="06128-339">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-339">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="06128-340">**CurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="06128-340">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-341">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06128-341">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06128-342">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-343">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 003.8 ") </span><span class="sxs-lookup"><span data-stu-id="06128-343">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="06128-344">目前的掃描模式。</span><span class="sxs-lookup"><span data-stu-id="06128-344">Current scan mode.</span></span> <span data-ttu-id="06128-345">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-345">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="06128-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="06128-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06128-347"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="06128-347"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="06128-348"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>**交錯** 式 (3) </span><span class="sxs-lookup"><span data-stu-id="06128-348"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>**Interlaced** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="06128-349"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**非交錯** 式 (4) </span><span class="sxs-lookup"><span data-stu-id="06128-349"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**Non Interlaced** (4)</span></span>


</dt> <dd>

<span data-ttu-id="06128-350">非交錯式</span><span class="sxs-lookup"><span data-stu-id="06128-350">Non-interlaced</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="06128-351">**CurrentVerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="06128-351">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-352">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="06128-352">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06128-353">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-354">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 003.10 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 圖元 ") </span><span class="sxs-lookup"><span data-stu-id="06128-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="06128-355">目前的垂直圖元數目。</span><span class="sxs-lookup"><span data-stu-id="06128-355">Current number of vertical pixels.</span></span>

<span data-ttu-id="06128-356">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-356">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="06128-357">**說明**</span><span class="sxs-lookup"><span data-stu-id="06128-357">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-358">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06128-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06128-359">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-360">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="06128-360">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="06128-361">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="06128-361">Textual description of the object.</span></span>

<span data-ttu-id="06128-362">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-362">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="06128-363">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="06128-363">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-364">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06128-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06128-365">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-366">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="06128-366">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="06128-367">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="06128-367">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="06128-368">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-368">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="06128-369">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="06128-369">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-370">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="06128-370">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06128-371">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06128-372">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="06128-372">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="06128-373">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-373">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="06128-374">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="06128-374">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-375">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06128-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06128-376">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06128-377">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="06128-377">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="06128-378">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="06128-379">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="06128-379">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-380">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="06128-380">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="06128-381">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-382">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="06128-382">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="06128-383">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="06128-383">Date and time the object was installed.</span></span> <span data-ttu-id="06128-384">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="06128-384">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="06128-385">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="06128-386">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="06128-386">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-387">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="06128-387">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06128-388">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06128-389">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="06128-389">Last error code reported by the logical device.</span></span>

<span data-ttu-id="06128-390">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-390">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="06128-391">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="06128-391">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-392">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="06128-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06128-393">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-394">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="06128-394">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="06128-395">支援的最大記憶體數量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="06128-395">Maximum amount of memory supported, in bytes.</span></span>

<span data-ttu-id="06128-396">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-396">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="06128-397">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="06128-397">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-398">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="06128-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06128-399">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-400">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 匯流排埠 \| 001.9 ") </span><span class="sxs-lookup"><span data-stu-id="06128-400">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="06128-401">控制器支援的直接可定址實體數目上限。</span><span class="sxs-lookup"><span data-stu-id="06128-401">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="06128-402">如果數位為未知或無限制，則應使用0值。</span><span class="sxs-lookup"><span data-stu-id="06128-402">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="06128-403">這個屬性繼承自 [**CIM \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-403">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="06128-404">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="06128-404">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-405">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="06128-405">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06128-406">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-407">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 003.5 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 赫茲 ") </span><span class="sxs-lookup"><span data-stu-id="06128-407">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="06128-408">影片控制器的最大重新整理速率（以赫茲為單位）。</span><span class="sxs-lookup"><span data-stu-id="06128-408">Maximum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="06128-409">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-409">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="06128-410">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="06128-410">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-411">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="06128-411">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06128-412">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-412">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-413">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 003.4 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 赫茲 ") </span><span class="sxs-lookup"><span data-stu-id="06128-413">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="06128-414">影片控制器的最小更新速率（以赫茲為單位）。</span><span class="sxs-lookup"><span data-stu-id="06128-414">Minimum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="06128-415">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-415">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="06128-416">**名稱**</span><span class="sxs-lookup"><span data-stu-id="06128-416">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-417">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06128-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06128-418">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-419">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="06128-419">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="06128-420">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="06128-420">Label by which the object is known.</span></span> <span data-ttu-id="06128-421">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="06128-421">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="06128-422">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-422">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="06128-423">**NumberOfColorPlanes**</span><span class="sxs-lookup"><span data-stu-id="06128-423">**NumberOfColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-424">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06128-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06128-425">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06128-426">目前的色彩平面數目。</span><span class="sxs-lookup"><span data-stu-id="06128-426">Current number of color planes.</span></span> <span data-ttu-id="06128-427">如果此值不適用於目前的影片設定，請輸入0。</span><span class="sxs-lookup"><span data-stu-id="06128-427">If this value is not applicable for the current video configuration, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="06128-428">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="06128-428">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-429">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="06128-429">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06128-430">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06128-431">提供目前的解析度和可用記憶體所支援的影片頁面數目。</span><span class="sxs-lookup"><span data-stu-id="06128-431">Number of video pages supported given the current resolutions and available memory.</span></span>

<span data-ttu-id="06128-432">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-432">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="06128-433">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="06128-433">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-434">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06128-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06128-435">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-436">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="06128-436">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="06128-437">邏輯裝置的 Win32 隨插即用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="06128-437">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="06128-438">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="06128-439">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="06128-439">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="06128-440">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="06128-440">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-441">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="06128-441">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="06128-442">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06128-443">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="06128-443">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="06128-444">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="06128-444">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06128-445"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="06128-445"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="06128-446"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="06128-446"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="06128-447"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="06128-447"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="06128-448"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="06128-448"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="06128-449">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="06128-449">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="06128-450"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="06128-450"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="06128-451">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="06128-451">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="06128-452"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="06128-452"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="06128-453">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="06128-453">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="06128-454">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="06128-454">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="06128-455">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="06128-455">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="06128-456"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="06128-456"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="06128-457">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="06128-457">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="06128-458"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="06128-458"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="06128-459">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="06128-459">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="06128-460">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="06128-460">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-461">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="06128-461">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06128-462">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-462">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06128-463">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="06128-463">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="06128-464">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="06128-464">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="06128-465">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="06128-465">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="06128-466">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="06128-466">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="06128-467">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="06128-468">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="06128-468">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-469">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06128-469">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06128-470">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-471">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 匯流排埠 \| 001.2 "，" MIF。DMTF \| 磁片 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="06128-471">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="06128-472">控制器用來存取「受控制」裝置的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="06128-472">Protocol used by the controller to access 'controlled' devices.</span></span>

<span data-ttu-id="06128-473">這個屬性繼承自 [**CIM \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-473">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="06128-474">值為：</span><span class="sxs-lookup"><span data-stu-id="06128-474">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="06128-475">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="06128-475">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06128-476">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="06128-476">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="06128-477">**EISA** (3) </span><span class="sxs-lookup"><span data-stu-id="06128-477">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="06128-478">**ISA** (4) </span><span class="sxs-lookup"><span data-stu-id="06128-478">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="06128-479">**PCI** (5) </span><span class="sxs-lookup"><span data-stu-id="06128-479">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="06128-480">**ATA/ATAPI** (6) </span><span class="sxs-lookup"><span data-stu-id="06128-480">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="06128-481">**彈性磁片** (7) </span><span class="sxs-lookup"><span data-stu-id="06128-481">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="06128-482">**1496** (8) </span><span class="sxs-lookup"><span data-stu-id="06128-482">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="06128-483">**SCSI 平行介面** (9) </span><span class="sxs-lookup"><span data-stu-id="06128-483">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="06128-484">**SCSI 光纖通道通訊協定** (10) </span><span class="sxs-lookup"><span data-stu-id="06128-484">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="06128-485">**SCSI 序列匯流排通訊協定** (11) </span><span class="sxs-lookup"><span data-stu-id="06128-485">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="06128-486">**SCSI 序列匯流排通訊協定-2 (1394)** (12) </span><span class="sxs-lookup"><span data-stu-id="06128-486">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="06128-487">**SCSI 序列儲存架構** (13) </span><span class="sxs-lookup"><span data-stu-id="06128-487">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="06128-488">**VESA** (14) </span><span class="sxs-lookup"><span data-stu-id="06128-488">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="06128-489">**PCMCIA** (15) </span><span class="sxs-lookup"><span data-stu-id="06128-489">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="06128-490">**通用序列匯流排** (16) </span><span class="sxs-lookup"><span data-stu-id="06128-490">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="06128-491">**平行通訊協定** (17) </span><span class="sxs-lookup"><span data-stu-id="06128-491">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="06128-492">**ESCON** (18) </span><span class="sxs-lookup"><span data-stu-id="06128-492">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="06128-493">**診斷** (19) </span><span class="sxs-lookup"><span data-stu-id="06128-493">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="06128-494">**I2C** (20) </span><span class="sxs-lookup"><span data-stu-id="06128-494">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="06128-495">**Power** (21) </span><span class="sxs-lookup"><span data-stu-id="06128-495">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="06128-496">**HIPPI** (22) </span><span class="sxs-lookup"><span data-stu-id="06128-496">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="06128-497">**MultiBus** (23) </span><span class="sxs-lookup"><span data-stu-id="06128-497">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="06128-498">**Vm** (24) </span><span class="sxs-lookup"><span data-stu-id="06128-498">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="06128-499">**IPI** (25) </span><span class="sxs-lookup"><span data-stu-id="06128-499">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="06128-500">**IEEE-488** (26) </span><span class="sxs-lookup"><span data-stu-id="06128-500">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="06128-501">**RS232** (27) </span><span class="sxs-lookup"><span data-stu-id="06128-501">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="06128-502">**IEEE 802.3 10BASE5** (28) </span><span class="sxs-lookup"><span data-stu-id="06128-502">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="06128-503">**IEEE 802.3 10BASE2** (29) </span><span class="sxs-lookup"><span data-stu-id="06128-503">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="06128-504">**IEEE 802.3 1BASE5** (30) </span><span class="sxs-lookup"><span data-stu-id="06128-504">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="06128-505">**IEEE 802.3 10BROAD36** (31) </span><span class="sxs-lookup"><span data-stu-id="06128-505">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="06128-506">**IEEE 802.3 100BASEVG** (32) </span><span class="sxs-lookup"><span data-stu-id="06128-506">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="06128-507">**IEEE 802.5 權杖-環形** (33) </span><span class="sxs-lookup"><span data-stu-id="06128-507">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="06128-508">**ANSI x3t 9.5 FDDI** (34) </span><span class="sxs-lookup"><span data-stu-id="06128-508">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="06128-509">**MCA** (35) </span><span class="sxs-lookup"><span data-stu-id="06128-509">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="06128-510">**ESDI** (36) </span><span class="sxs-lookup"><span data-stu-id="06128-510">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="06128-511">**IDE** (37) </span><span class="sxs-lookup"><span data-stu-id="06128-511">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="06128-512">**CMD** (38) </span><span class="sxs-lookup"><span data-stu-id="06128-512">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="06128-513">**ST506** (39) </span><span class="sxs-lookup"><span data-stu-id="06128-513">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="06128-514">**」 Dssi 小組** (40) </span><span class="sxs-lookup"><span data-stu-id="06128-514">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="06128-515">**QIC2** (41) </span><span class="sxs-lookup"><span data-stu-id="06128-515">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="06128-516">**增強型 ATA/IDE** (42) </span><span class="sxs-lookup"><span data-stu-id="06128-516">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="06128-517">**AGP** (43) </span><span class="sxs-lookup"><span data-stu-id="06128-517">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="06128-518">**TWIRP (雙向紅外線)** (44) </span><span class="sxs-lookup"><span data-stu-id="06128-518">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="06128-519">**(快速紅外線)** (45) 的杉樹</span><span class="sxs-lookup"><span data-stu-id="06128-519">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="06128-520">**SIR (串列紅外線)** (46) </span><span class="sxs-lookup"><span data-stu-id="06128-520">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="06128-521">**IrBus** (47) </span><span class="sxs-lookup"><span data-stu-id="06128-521">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06128-522">**狀態**</span><span class="sxs-lookup"><span data-stu-id="06128-522">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-523">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06128-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06128-524">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-525">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="06128-525">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="06128-526">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="06128-526">Current status of the object.</span></span> <span data-ttu-id="06128-527">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-527">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="06128-528">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="06128-528">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="06128-529">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="06128-529">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="06128-530">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="06128-530">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="06128-531">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="06128-531">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06128-532">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="06128-532">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="06128-533">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="06128-533">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="06128-534">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="06128-534">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="06128-535">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="06128-535">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="06128-536">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="06128-536">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="06128-537">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="06128-537">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="06128-538">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="06128-538">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="06128-539">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="06128-539">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="06128-540">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="06128-540">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06128-541">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="06128-541">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-542">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06128-542">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06128-543">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-544">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="06128-544">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="06128-545">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="06128-545">State of the logical device.</span></span> <span data-ttu-id="06128-546">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="06128-546">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="06128-547">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-547">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="06128-548">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="06128-548">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06128-549">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="06128-549">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="06128-550">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="06128-550">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="06128-551">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="06128-551">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="06128-552">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="06128-552">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06128-553">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="06128-553">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-554">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06128-554">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06128-555">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-555">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-556">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="06128-556">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="06128-557">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="06128-557">Scoping system's creation class name.</span></span>

<span data-ttu-id="06128-558">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-558">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="06128-559">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="06128-559">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-560">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06128-560">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06128-561">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-561">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-562">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="06128-562">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="06128-563">設定系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="06128-563">Scoping system's name.</span></span>

<span data-ttu-id="06128-564">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-564">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="06128-565">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="06128-565">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-566">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="06128-566">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="06128-567">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-567">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06128-568">上次重設此控制器的日期和時間，表示控制器已關機或重新初始化。</span><span class="sxs-lookup"><span data-stu-id="06128-568">Date and time this controller was last reset meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="06128-569">這個屬性繼承自 [**CIM \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-569">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="06128-570">**VideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="06128-570">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-571">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06128-571">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06128-572">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-573">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 003.2 ") </span><span class="sxs-lookup"><span data-stu-id="06128-573">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="06128-574">影片架構。</span><span class="sxs-lookup"><span data-stu-id="06128-574">Video architecture.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="06128-575">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="06128-575">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06128-576">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="06128-576">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CGA"></span><span id="cga"></span>

<span data-ttu-id="06128-577"> (3) 的 **CGA**</span><span class="sxs-lookup"><span data-stu-id="06128-577">**CGA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="EGA"></span><span id="ega"></span>

<span data-ttu-id="06128-578">**EGA** (4) </span><span class="sxs-lookup"><span data-stu-id="06128-578">**EGA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VGA"></span><span id="vga"></span>

<span data-ttu-id="06128-579">**VGA** (5) </span><span class="sxs-lookup"><span data-stu-id="06128-579">**VGA** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SVGA"></span><span id="svga"></span>

<span data-ttu-id="06128-580">**SVGA** (6) </span><span class="sxs-lookup"><span data-stu-id="06128-580">**SVGA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="MDA"></span><span id="mda"></span>

<span data-ttu-id="06128-581">**MDA** (7) </span><span class="sxs-lookup"><span data-stu-id="06128-581">**MDA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HGC"></span><span id="hgc"></span>

<span data-ttu-id="06128-582">**HGC** (8) </span><span class="sxs-lookup"><span data-stu-id="06128-582">**HGC** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="MCGA"></span><span id="mcga"></span>

<span data-ttu-id="06128-583">**MCGA** (9) </span><span class="sxs-lookup"><span data-stu-id="06128-583">**MCGA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="8514A"></span><span id="8514a"></span>

<span data-ttu-id="06128-584">**8514A** (10) </span><span class="sxs-lookup"><span data-stu-id="06128-584">**8514A** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="XGA"></span><span id="xga"></span>

<span data-ttu-id="06128-585">**XGA** (11) </span><span class="sxs-lookup"><span data-stu-id="06128-585">**XGA** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>

<span data-ttu-id="06128-586">**線性框架緩衝區** (12) </span><span class="sxs-lookup"><span data-stu-id="06128-586">**Linear Frame Buffer** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="06128-587">**PC-98** (160) </span><span class="sxs-lookup"><span data-stu-id="06128-587">**PC-98** (160)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06128-588">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="06128-588">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-589">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06128-589">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06128-590">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-591">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 003.6 ") </span><span class="sxs-lookup"><span data-stu-id="06128-591">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.6")</span></span>
</dt> </dl>

<span data-ttu-id="06128-592">視訊記憶體的類型。</span><span class="sxs-lookup"><span data-stu-id="06128-592">Type of video memory.</span></span>

<span data-ttu-id="06128-593">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-593">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="06128-594">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="06128-594">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06128-595">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="06128-595">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="06128-596">**VRAM** (3) </span><span class="sxs-lookup"><span data-stu-id="06128-596">**VRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="06128-597">**DRAM** (4) </span><span class="sxs-lookup"><span data-stu-id="06128-597">**DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="06128-598">**SRAM** (5) </span><span class="sxs-lookup"><span data-stu-id="06128-598">**SRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="06128-599">**WRAM** (6) </span><span class="sxs-lookup"><span data-stu-id="06128-599">**WRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="06128-600">**EDO RAM** (7) </span><span class="sxs-lookup"><span data-stu-id="06128-600">**EDO RAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="06128-601">高載 **同步 DRAM** (8) </span><span class="sxs-lookup"><span data-stu-id="06128-601">**Burst Synchronous DRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="06128-602">**管線** 高載 SRAM (9) </span><span class="sxs-lookup"><span data-stu-id="06128-602">**Pipelined Burst SRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="06128-603">**CDRAM** (10) </span><span class="sxs-lookup"><span data-stu-id="06128-603">**CDRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="06128-604">**3DRAM** (11) </span><span class="sxs-lookup"><span data-stu-id="06128-604">**3DRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="06128-605">**SDRAM** (12) </span><span class="sxs-lookup"><span data-stu-id="06128-605">**SDRAM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="06128-606">**SGRAM** (13) </span><span class="sxs-lookup"><span data-stu-id="06128-606">**SGRAM** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06128-607">**VideoMode**</span><span class="sxs-lookup"><span data-stu-id="06128-607">**VideoMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-608">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06128-608">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06128-609">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-609">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06128-610">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="06128-610">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="06128-611">目前的影片模式。</span><span class="sxs-lookup"><span data-stu-id="06128-611">Current video mode.</span></span>

</dd> <dt>

<span data-ttu-id="06128-612">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="06128-612">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06128-613">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06128-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06128-614">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06128-614">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06128-615">描述視頻處理器/控制器的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="06128-615">Free-form string that describes the video processor/controller.</span></span>

<span data-ttu-id="06128-616">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-616">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06128-617">備註</span><span class="sxs-lookup"><span data-stu-id="06128-617">Remarks</span></span>

<span data-ttu-id="06128-618">**Cim \_ PCVideoController** 類別衍生自 [**cim \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-618">The **CIM\_PCVideoController** class is derived from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<span data-ttu-id="06128-619">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="06128-619">WMI does not implement this class.</span></span> <span data-ttu-id="06128-620">針對衍生自 [**CIM \_ PCVIDEOCONTROLLER**](cim-videocontroller.md)的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="06128-620">For WMI classes derived from [**CIM\_PCVideoController**](cim-videocontroller.md), see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="06128-621">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="06128-621">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="06128-622">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="06128-622">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="06128-623">規格需求</span><span class="sxs-lookup"><span data-stu-id="06128-623">Requirements</span></span>



| <span data-ttu-id="06128-624">需求</span><span class="sxs-lookup"><span data-stu-id="06128-624">Requirement</span></span> | <span data-ttu-id="06128-625">值</span><span class="sxs-lookup"><span data-stu-id="06128-625">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06128-626">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="06128-626">Minimum supported client</span></span><br/> | <span data-ttu-id="06128-627">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06128-627">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="06128-628">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="06128-628">Minimum supported server</span></span><br/> | <span data-ttu-id="06128-629">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06128-629">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="06128-630">命名空間</span><span class="sxs-lookup"><span data-stu-id="06128-630">Namespace</span></span><br/>                | <span data-ttu-id="06128-631">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="06128-631">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="06128-632">MOF</span><span class="sxs-lookup"><span data-stu-id="06128-632">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06128-633"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="06128-633"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="06128-634">DLL</span><span class="sxs-lookup"><span data-stu-id="06128-634">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06128-635"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06128-635"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06128-636">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06128-636">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06128-637">**CIM \_ VideoController**</span><span class="sxs-lookup"><span data-stu-id="06128-637">**CIM\_VideoController**</span></span>](cim-videocontroller.md)
</dt> </dl>

 

