---
description: CIM \_ VideoController 類別代表影片控制器的功能和管理。
ms.assetid: 7cf6bf2a-62a5-46fa-8c8f-976604360461
ms.tgt_platform: multiple
title: CIM_VideoController 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoController
- CIM_VideoController.AcceleratorCapabilities
- CIM_VideoController.Availability
- CIM_VideoController.CapabilityDescriptions
- CIM_VideoController.Caption
- CIM_VideoController.ConfigManagerErrorCode
- CIM_VideoController.ConfigManagerUserConfig
- CIM_VideoController.CreationClassName
- CIM_VideoController.CurrentBitsPerPixel
- CIM_VideoController.CurrentHorizontalResolution
- CIM_VideoController.CurrentNumberOfColors
- CIM_VideoController.CurrentNumberOfColumns
- CIM_VideoController.CurrentNumberOfRows
- CIM_VideoController.CurrentRefreshRate
- CIM_VideoController.CurrentScanMode
- CIM_VideoController.CurrentVerticalResolution
- CIM_VideoController.Description
- CIM_VideoController.DeviceID
- CIM_VideoController.ErrorCleared
- CIM_VideoController.ErrorDescription
- CIM_VideoController.InstallDate
- CIM_VideoController.LastErrorCode
- CIM_VideoController.MaxMemorySupported
- CIM_VideoController.MaxNumberControlled
- CIM_VideoController.MaxRefreshRate
- CIM_VideoController.MinRefreshRate
- CIM_VideoController.Name
- CIM_VideoController.NumberOfVideoPages
- CIM_VideoController.PNPDeviceID
- CIM_VideoController.PowerManagementCapabilities
- CIM_VideoController.PowerManagementSupported
- CIM_VideoController.ProtocolSupported
- CIM_VideoController.Status
- CIM_VideoController.StatusInfo
- CIM_VideoController.SystemCreationClassName
- CIM_VideoController.SystemName
- CIM_VideoController.TimeOfLastReset
- CIM_VideoController.VideoMemoryType
- CIM_VideoController.VideoProcessor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6475c99e7a6f2ee1bef56bf2c266c788efc0b805
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847496"
---
# <a name="cim_videocontroller-class"></a><span data-ttu-id="fc20e-103">CIM \_ VideoController 類別</span><span class="sxs-lookup"><span data-stu-id="fc20e-103">CIM\_VideoController class</span></span>

<span data-ttu-id="fc20e-104">**CIM \_ VideoController** 類別代表影片控制器的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="fc20e-104">The **CIM\_VideoController** class represents the capabilities and management of the video controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fc20e-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="fc20e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fc20e-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="fc20e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fc20e-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="fc20e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="fc20e-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="fc20e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc20e-109">語法</span><span class="sxs-lookup"><span data-stu-id="fc20e-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCE5-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_VideoController : CIM_Controller
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
  uint16   VideoMemoryType;
  string   VideoProcessor;
};
```

## <a name="members"></a><span data-ttu-id="fc20e-110">成員</span><span class="sxs-lookup"><span data-stu-id="fc20e-110">Members</span></span>

<span data-ttu-id="fc20e-111">**CIM \_ VideoController** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fc20e-111">The **CIM\_VideoController** class has these types of members:</span></span>

-   [<span data-ttu-id="fc20e-112">方法</span><span class="sxs-lookup"><span data-stu-id="fc20e-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="fc20e-113">屬性</span><span class="sxs-lookup"><span data-stu-id="fc20e-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fc20e-114">方法</span><span class="sxs-lookup"><span data-stu-id="fc20e-114">Methods</span></span>

<span data-ttu-id="fc20e-115">**CIM \_ VideoController** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="fc20e-115">The **CIM\_VideoController** class has these methods.</span></span>



| <span data-ttu-id="fc20e-116">方法</span><span class="sxs-lookup"><span data-stu-id="fc20e-116">Method</span></span>                                                                     | <span data-ttu-id="fc20e-117">描述</span><span class="sxs-lookup"><span data-stu-id="fc20e-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fc20e-118">**重設**</span><span class="sxs-lookup"><span data-stu-id="fc20e-118">**Reset**</span></span>](reset-method-in-class-cim-videocontroller.md)                 | <span data-ttu-id="fc20e-119">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="fc20e-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="fc20e-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="fc20e-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="fc20e-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="fc20e-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-videocontroller.md) | <span data-ttu-id="fc20e-122">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="fc20e-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="fc20e-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="fc20e-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="fc20e-124">屬性</span><span class="sxs-lookup"><span data-stu-id="fc20e-124">Properties</span></span>

<span data-ttu-id="fc20e-125">**CIM \_ VideoController** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fc20e-125">The **CIM\_VideoController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc20e-126">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="fc20e-126">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-127">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="fc20e-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-129">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ VideoController**.**CapabilityDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="fc20e-129">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-130">影片控制器的圖形和3D 功能。</span><span class="sxs-lookup"><span data-stu-id="fc20e-130">Graphics and 3-D capabilities of the video controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fc20e-131">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="fc20e-131">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fc20e-132">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="fc20e-132">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="fc20e-133">**圖形加速器** (2) </span><span class="sxs-lookup"><span data-stu-id="fc20e-133">**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="fc20e-134">**3D 加速器** (3) </span><span class="sxs-lookup"><span data-stu-id="fc20e-134">**3D Accelerator** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fc20e-135">**可用性**</span><span class="sxs-lookup"><span data-stu-id="fc20e-135">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-136">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fc20e-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-138">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="fc20e-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-139">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="fc20e-139">Availability and status of the device.</span></span>

<span data-ttu-id="fc20e-140">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="fc20e-140">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fc20e-141"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="fc20e-141"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fc20e-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="fc20e-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="fc20e-143"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="fc20e-143"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="fc20e-144"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="fc20e-144"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="fc20e-145"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="fc20e-145"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="fc20e-146"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="fc20e-146"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="fc20e-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="fc20e-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="fc20e-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="fc20e-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="fc20e-149"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="fc20e-149"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="fc20e-150"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="fc20e-150"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="fc20e-151"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="fc20e-151"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="fc20e-152"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="fc20e-152"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="fc20e-153"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="fc20e-153"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-154">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="fc20e-154">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="fc20e-155"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="fc20e-155"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-156">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="fc20e-156">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="fc20e-157"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="fc20e-157"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-158">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="fc20e-158">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="fc20e-159"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="fc20e-159"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="fc20e-160"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="fc20e-160"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-161">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="fc20e-161">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="fc20e-162"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="fc20e-162"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-163">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="fc20e-163">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="fc20e-164"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="fc20e-164"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-165">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="fc20e-165">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="fc20e-166"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="fc20e-166"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-167">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="fc20e-167">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="fc20e-168"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="fc20e-168"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-169">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="fc20e-169">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fc20e-170">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="fc20e-170">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-171">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="fc20e-171">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-173">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ VideoController**。**AcceleratorCapabilities**") </span><span class="sxs-lookup"><span data-stu-id="fc20e-173">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoController**.**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-174">提供 **AcceleratorCapabilities** 陣列中所指出的影片加速器功能詳細描述的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="fc20e-174">Free-form strings that provide detailed descriptions for the video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="fc20e-175">這個陣列的每個專案都與 **AcceleratorCapabilities** 陣列中位於相同索引的專案有關。</span><span class="sxs-lookup"><span data-stu-id="fc20e-175">Each entry of this array is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="fc20e-176">**標題**</span><span class="sxs-lookup"><span data-stu-id="fc20e-176">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fc20e-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-179">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="fc20e-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-180">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="fc20e-180">Short textual description of the object.</span></span>

<span data-ttu-id="fc20e-181">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="fc20e-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc20e-182">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="fc20e-182">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-183">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fc20e-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-185">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="fc20e-185">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-186">Windows 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fc20e-186">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="fc20e-187">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="fc20e-187">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="fc20e-188"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-188"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="fc20e-189"> (0)</span><span class="sxs-lookup"><span data-stu-id="fc20e-189">(0)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-190">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="fc20e-190">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="fc20e-191"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-191"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="fc20e-192">(1)</span><span class="sxs-lookup"><span data-stu-id="fc20e-192">(1)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-193">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="fc20e-193">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="fc20e-194"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-194"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="fc20e-195">(2)</span><span class="sxs-lookup"><span data-stu-id="fc20e-195">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="fc20e-196"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-196"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="fc20e-197">(3)</span><span class="sxs-lookup"><span data-stu-id="fc20e-197">(3)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-198">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="fc20e-198">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="fc20e-199"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-199"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="fc20e-200">(4)</span><span class="sxs-lookup"><span data-stu-id="fc20e-200">(4)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-201">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="fc20e-201">Device is not working properly.</span></span> <span data-ttu-id="fc20e-202">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="fc20e-202">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="fc20e-203"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-203"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="fc20e-204">(5)</span><span class="sxs-lookup"><span data-stu-id="fc20e-204">(5)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-205">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="fc20e-205">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="fc20e-206"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-206"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="fc20e-207">(6)</span><span class="sxs-lookup"><span data-stu-id="fc20e-207">(6)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-208">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="fc20e-208">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="fc20e-209"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-209"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="fc20e-210">(7)</span><span class="sxs-lookup"><span data-stu-id="fc20e-210">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="fc20e-211"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-211"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="fc20e-212">(8)</span><span class="sxs-lookup"><span data-stu-id="fc20e-212">(8)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-213">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="fc20e-213">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="fc20e-214"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-214"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="fc20e-215">(9)</span><span class="sxs-lookup"><span data-stu-id="fc20e-215">(9)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-216">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="fc20e-216">Device is not working properly.</span></span> <span data-ttu-id="fc20e-217">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="fc20e-217">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="fc20e-218"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-218"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="fc20e-219">(10)</span><span class="sxs-lookup"><span data-stu-id="fc20e-219">(10)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-220">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="fc20e-220">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="fc20e-221"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-221"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="fc20e-222">(11)</span><span class="sxs-lookup"><span data-stu-id="fc20e-222">(11)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-223">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="fc20e-223">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="fc20e-224"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-224"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="fc20e-225"> (12) </span><span class="sxs-lookup"><span data-stu-id="fc20e-225">(12)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-226">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="fc20e-226">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="fc20e-227"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-227"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="fc20e-228">(13)</span><span class="sxs-lookup"><span data-stu-id="fc20e-228">(13)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-229">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="fc20e-229">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="fc20e-230"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-230"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="fc20e-231">(14)</span><span class="sxs-lookup"><span data-stu-id="fc20e-231">(14)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-232">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="fc20e-232">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="fc20e-233"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-233"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="fc20e-234">(15)</span><span class="sxs-lookup"><span data-stu-id="fc20e-234">(15)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-235">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="fc20e-235">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="fc20e-236"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-236"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="fc20e-237">(16)</span><span class="sxs-lookup"><span data-stu-id="fc20e-237">(16)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-238">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="fc20e-238">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="fc20e-239"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-239"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="fc20e-240">(17)</span><span class="sxs-lookup"><span data-stu-id="fc20e-240">(17)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-241">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="fc20e-241">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="fc20e-242"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-242"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="fc20e-243">(18)</span><span class="sxs-lookup"><span data-stu-id="fc20e-243">(18)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-244">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="fc20e-244">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="fc20e-245"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-245"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="fc20e-246">(19)</span><span class="sxs-lookup"><span data-stu-id="fc20e-246">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="fc20e-247"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-247"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="fc20e-248">(20)</span><span class="sxs-lookup"><span data-stu-id="fc20e-248">(20)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-249">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="fc20e-249">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="fc20e-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="fc20e-251">(21)</span><span class="sxs-lookup"><span data-stu-id="fc20e-251">(21)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-252">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="fc20e-252">System failure.</span></span> <span data-ttu-id="fc20e-253">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="fc20e-253">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="fc20e-254">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="fc20e-254">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="fc20e-255"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-255"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="fc20e-256">(22)</span><span class="sxs-lookup"><span data-stu-id="fc20e-256">(22)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-257">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="fc20e-257">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="fc20e-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="fc20e-259">(23)</span><span class="sxs-lookup"><span data-stu-id="fc20e-259">(23)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-260">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="fc20e-260">System failure.</span></span> <span data-ttu-id="fc20e-261">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="fc20e-261">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="fc20e-262"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-262"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="fc20e-263">(24)</span><span class="sxs-lookup"><span data-stu-id="fc20e-263">(24)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-264">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="fc20e-264">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="fc20e-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="fc20e-266">(25)</span><span class="sxs-lookup"><span data-stu-id="fc20e-266">(25)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-267">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="fc20e-267">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="fc20e-268"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-268"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="fc20e-269">(26)</span><span class="sxs-lookup"><span data-stu-id="fc20e-269">(26)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-270">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="fc20e-270">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="fc20e-271"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-271"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="fc20e-272">(27)</span><span class="sxs-lookup"><span data-stu-id="fc20e-272">(27)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-273">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="fc20e-273">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="fc20e-274"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-274"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="fc20e-275">(28)</span><span class="sxs-lookup"><span data-stu-id="fc20e-275">(28)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-276">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="fc20e-276">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="fc20e-277"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-277"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="fc20e-278">(29)</span><span class="sxs-lookup"><span data-stu-id="fc20e-278">(29)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-279">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="fc20e-279">Device is disabled.</span></span> <span data-ttu-id="fc20e-280">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="fc20e-280">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="fc20e-281"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-281"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="fc20e-282">(30)</span><span class="sxs-lookup"><span data-stu-id="fc20e-282">(30)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-283">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="fc20e-283">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="fc20e-284"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="fc20e-284"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="fc20e-285"> (31) </span><span class="sxs-lookup"><span data-stu-id="fc20e-285">(31)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-286">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="fc20e-286">Device is not working properly.</span></span> <span data-ttu-id="fc20e-287">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="fc20e-287">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fc20e-288">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="fc20e-288">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-289">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fc20e-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-290">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-291">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="fc20e-291">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-292">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="fc20e-292">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="fc20e-293">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="fc20e-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc20e-294">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fc20e-294">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-295">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fc20e-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-296">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-297">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fc20e-297">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-298">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc20e-298">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="fc20e-299">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="fc20e-299">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="fc20e-300">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="fc20e-300">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc20e-301">**CurrentBitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="fc20e-301">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-302">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fc20e-302">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-303">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-304">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 003.12 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ") </span><span class="sxs-lookup"><span data-stu-id="fc20e-304">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-305">用來顯示每個圖元的位數。</span><span class="sxs-lookup"><span data-stu-id="fc20e-305">Number of bits used to display each pixel.</span></span>

</dd> <dt>

<span data-ttu-id="fc20e-306">**CurrentHorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="fc20e-306">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-307">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fc20e-307">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-308">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-309">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 003.11 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 圖元 ") </span><span class="sxs-lookup"><span data-stu-id="fc20e-309">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-310">目前的水準圖元數目。</span><span class="sxs-lookup"><span data-stu-id="fc20e-310">Current number of horizontal pixels.</span></span>

</dd> <dt>

<span data-ttu-id="fc20e-311">**CurrentNumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="fc20e-311">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-312">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="fc20e-312">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-313">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-314">目前解析度所支援的色彩數目。</span><span class="sxs-lookup"><span data-stu-id="fc20e-314">Number of colors supported at the current resolution.</span></span>

<span data-ttu-id="fc20e-315">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="fc20e-315">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="fc20e-316">**CurrentNumberOfColumns**</span><span class="sxs-lookup"><span data-stu-id="fc20e-316">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-317">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fc20e-317">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-318">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-319">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 003.14 ") </span><span class="sxs-lookup"><span data-stu-id="fc20e-319">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.14")</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-320">如果在字元模式中，則為影片控制器的欄數;否則，請輸入0。</span><span class="sxs-lookup"><span data-stu-id="fc20e-320">If in character mode, number of columns for the video controller; otherwise, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="fc20e-321">**CurrentNumberOfRows**</span><span class="sxs-lookup"><span data-stu-id="fc20e-321">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-322">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fc20e-322">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-323">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-324">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 003.13 ") </span><span class="sxs-lookup"><span data-stu-id="fc20e-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-325">如果在字元模式中，則為影片控制器的資料列數目;否則，請輸入0。</span><span class="sxs-lookup"><span data-stu-id="fc20e-325">If in character mode, number of rows for the video controller; otherwise, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="fc20e-326">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="fc20e-326">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-327">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fc20e-327">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-328">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-329">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 003.15 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 赫茲 ") </span><span class="sxs-lookup"><span data-stu-id="fc20e-329">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-330">目前的重新整理速率（以赫茲為單位）。</span><span class="sxs-lookup"><span data-stu-id="fc20e-330">Current refresh rate, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="fc20e-331">**CurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="fc20e-331">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-332">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fc20e-332">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-333">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-334">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 003.8 ") </span><span class="sxs-lookup"><span data-stu-id="fc20e-334">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-335">目前的掃描模式。</span><span class="sxs-lookup"><span data-stu-id="fc20e-335">Current scan mode.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fc20e-336">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="fc20e-336">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fc20e-337">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="fc20e-337">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="fc20e-338">**交錯** 式 (3) </span><span class="sxs-lookup"><span data-stu-id="fc20e-338">**Interlaced** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="fc20e-339">**非交錯** 式 (4) </span><span class="sxs-lookup"><span data-stu-id="fc20e-339">**Non Interlaced** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fc20e-340">**CurrentVerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="fc20e-340">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-341">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fc20e-341">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-342">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-343">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 003.10 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 圖元 ") </span><span class="sxs-lookup"><span data-stu-id="fc20e-343">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-344">目前的垂直圖元數目。</span><span class="sxs-lookup"><span data-stu-id="fc20e-344">Current number of vertical pixels.</span></span>

</dd> <dt>

<span data-ttu-id="fc20e-345">**說明**</span><span class="sxs-lookup"><span data-stu-id="fc20e-345">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-346">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fc20e-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-347">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-348">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="fc20e-348">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-349">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="fc20e-349">Textual description of the object.</span></span>

<span data-ttu-id="fc20e-350">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="fc20e-350">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc20e-351">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="fc20e-351">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-352">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fc20e-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-353">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-354">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fc20e-354">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-355">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="fc20e-355">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="fc20e-356">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="fc20e-356">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc20e-357">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="fc20e-357">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-358">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fc20e-358">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-359">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-360">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="fc20e-360">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="fc20e-361">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="fc20e-361">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc20e-362">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="fc20e-362">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-363">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fc20e-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-364">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-365">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="fc20e-365">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="fc20e-366">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="fc20e-366">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc20e-367">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="fc20e-367">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-368">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="fc20e-368">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-369">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-370">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="fc20e-370">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-371">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="fc20e-371">Date and time the object was installed.</span></span> <span data-ttu-id="fc20e-372">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="fc20e-372">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="fc20e-373">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="fc20e-373">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc20e-374">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="fc20e-374">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-375">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fc20e-375">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-376">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-377">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fc20e-377">Last error code reported by the logical device.</span></span>

<span data-ttu-id="fc20e-378">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="fc20e-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc20e-379">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="fc20e-379">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-380">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fc20e-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-381">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-382">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="fc20e-382">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-383">支援的最大記憶體數量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="fc20e-383">Maximum amount of memory supported, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="fc20e-384">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="fc20e-384">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-385">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fc20e-385">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-386">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-387">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 匯流排埠 \| 001.9 ") </span><span class="sxs-lookup"><span data-stu-id="fc20e-387">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-388">控制器支援的直接可定址實體數目上限。</span><span class="sxs-lookup"><span data-stu-id="fc20e-388">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="fc20e-389">如果數位為未知或無限制，則應使用0值。</span><span class="sxs-lookup"><span data-stu-id="fc20e-389">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="fc20e-390">這個屬性繼承自 [**CIM \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="fc20e-390">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc20e-391">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="fc20e-391">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-392">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fc20e-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-393">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-394">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 003.5 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 赫茲 ") </span><span class="sxs-lookup"><span data-stu-id="fc20e-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-395">影片控制器的最大重新整理頻率（以赫茲為單位）。</span><span class="sxs-lookup"><span data-stu-id="fc20e-395">Maximum refresh rate of the video controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="fc20e-396">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="fc20e-396">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-397">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fc20e-397">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-398">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-399">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 003.4 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 赫茲 ") </span><span class="sxs-lookup"><span data-stu-id="fc20e-399">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-400">影片控制器的最小重新整理頻率（以赫茲為單位）。</span><span class="sxs-lookup"><span data-stu-id="fc20e-400">Minimum refresh rate of the video controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="fc20e-401">**名稱**</span><span class="sxs-lookup"><span data-stu-id="fc20e-401">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-402">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fc20e-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-403">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-404">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="fc20e-404">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-405">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="fc20e-405">Label by which the object is known.</span></span> <span data-ttu-id="fc20e-406">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="fc20e-406">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="fc20e-407">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="fc20e-407">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc20e-408">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="fc20e-408">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-409">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fc20e-409">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-410">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-411">提供目前的解析度和可用記憶體所支援的影片頁面數目。</span><span class="sxs-lookup"><span data-stu-id="fc20e-411">Number of video pages supported given the current resolutions and available memory.</span></span>

</dd> <dt>

<span data-ttu-id="fc20e-412">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="fc20e-412">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-413">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fc20e-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-414">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-415">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="fc20e-415">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-416">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="fc20e-416">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="fc20e-417">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="fc20e-417">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="fc20e-418">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="fc20e-418">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="fc20e-419">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="fc20e-419">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-420">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="fc20e-420">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-421">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-422">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="fc20e-422">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="fc20e-423">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="fc20e-423">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fc20e-424"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="fc20e-424"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="fc20e-425"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="fc20e-425"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="fc20e-426"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="fc20e-426"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="fc20e-427"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="fc20e-427"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-428">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="fc20e-428">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="fc20e-429"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="fc20e-429"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-430">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="fc20e-430">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="fc20e-431"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="fc20e-431"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-432">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="fc20e-432">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="fc20e-433">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="fc20e-433">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="fc20e-434">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="fc20e-434">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="fc20e-435"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="fc20e-435"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-436">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="fc20e-436">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="fc20e-437"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="fc20e-437"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="fc20e-438">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="fc20e-438">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fc20e-439">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="fc20e-439">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-440">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fc20e-440">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-441">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-442">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="fc20e-442">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="fc20e-443">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="fc20e-443">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="fc20e-444">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="fc20e-444">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="fc20e-445">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="fc20e-445">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="fc20e-446">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="fc20e-446">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc20e-447">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="fc20e-447">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-448">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fc20e-448">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-449">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-450">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 匯流排埠 \| 001.2 "，" MIF。DMTF \| 磁片 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="fc20e-450">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-451">控制器用來存取「受控制」裝置的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="fc20e-451">Protocol used by the controller to access 'controlled' devices.</span></span>

<span data-ttu-id="fc20e-452">這個屬性繼承自 [**CIM \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="fc20e-452">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="fc20e-453">值為：</span><span class="sxs-lookup"><span data-stu-id="fc20e-453">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fc20e-454">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="fc20e-454">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fc20e-455">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="fc20e-455">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="fc20e-456">**EISA** (3) </span><span class="sxs-lookup"><span data-stu-id="fc20e-456">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="fc20e-457">**ISA** (4) </span><span class="sxs-lookup"><span data-stu-id="fc20e-457">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="fc20e-458">**PCI** (5) </span><span class="sxs-lookup"><span data-stu-id="fc20e-458">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="fc20e-459">**ATA/ATAPI** (6) </span><span class="sxs-lookup"><span data-stu-id="fc20e-459">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="fc20e-460">**彈性磁片** (7) </span><span class="sxs-lookup"><span data-stu-id="fc20e-460">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="fc20e-461">**1496** (8) </span><span class="sxs-lookup"><span data-stu-id="fc20e-461">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="fc20e-462">**SCSI 平行介面** (9) </span><span class="sxs-lookup"><span data-stu-id="fc20e-462">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="fc20e-463">**SCSI 光纖通道通訊協定** (10) </span><span class="sxs-lookup"><span data-stu-id="fc20e-463">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="fc20e-464">**SCSI 序列匯流排通訊協定** (11) </span><span class="sxs-lookup"><span data-stu-id="fc20e-464">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="fc20e-465">**SCSI 序列匯流排通訊協定-2 (1394)** (12) </span><span class="sxs-lookup"><span data-stu-id="fc20e-465">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="fc20e-466">**SCSI 序列儲存架構** (13) </span><span class="sxs-lookup"><span data-stu-id="fc20e-466">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="fc20e-467">**VESA** (14) </span><span class="sxs-lookup"><span data-stu-id="fc20e-467">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="fc20e-468">**PCMCIA** (15) </span><span class="sxs-lookup"><span data-stu-id="fc20e-468">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="fc20e-469">**通用序列匯流排** (16) </span><span class="sxs-lookup"><span data-stu-id="fc20e-469">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="fc20e-470">**平行通訊協定** (17) </span><span class="sxs-lookup"><span data-stu-id="fc20e-470">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="fc20e-471">**ESCON** (18) </span><span class="sxs-lookup"><span data-stu-id="fc20e-471">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="fc20e-472">**診斷** (19) </span><span class="sxs-lookup"><span data-stu-id="fc20e-472">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="fc20e-473">**I2C** (20) </span><span class="sxs-lookup"><span data-stu-id="fc20e-473">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="fc20e-474">**Power** (21) </span><span class="sxs-lookup"><span data-stu-id="fc20e-474">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="fc20e-475">**HIPPI** (22) </span><span class="sxs-lookup"><span data-stu-id="fc20e-475">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="fc20e-476">**MultiBus** (23) </span><span class="sxs-lookup"><span data-stu-id="fc20e-476">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="fc20e-477">**Vm** (24) </span><span class="sxs-lookup"><span data-stu-id="fc20e-477">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="fc20e-478">**IPI** (25) </span><span class="sxs-lookup"><span data-stu-id="fc20e-478">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="fc20e-479">**IEEE-488** (26) </span><span class="sxs-lookup"><span data-stu-id="fc20e-479">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="fc20e-480">**RS232** (27) </span><span class="sxs-lookup"><span data-stu-id="fc20e-480">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="fc20e-481">**IEEE 802.3 10BASE5** (28) </span><span class="sxs-lookup"><span data-stu-id="fc20e-481">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="fc20e-482">**IEEE 802.3 10BASE2** (29) </span><span class="sxs-lookup"><span data-stu-id="fc20e-482">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="fc20e-483">**IEEE 802.3 1BASE5** (30) </span><span class="sxs-lookup"><span data-stu-id="fc20e-483">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="fc20e-484">**IEEE 802.3 10BROAD36** (31) </span><span class="sxs-lookup"><span data-stu-id="fc20e-484">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="fc20e-485">**IEEE 802.3 100BASEVG** (32) </span><span class="sxs-lookup"><span data-stu-id="fc20e-485">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="fc20e-486">**IEEE 802.5 權杖-環形** (33) </span><span class="sxs-lookup"><span data-stu-id="fc20e-486">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="fc20e-487">**ANSI x3t 9.5 FDDI** (34) </span><span class="sxs-lookup"><span data-stu-id="fc20e-487">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="fc20e-488">**MCA** (35) </span><span class="sxs-lookup"><span data-stu-id="fc20e-488">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="fc20e-489">**ESDI** (36) </span><span class="sxs-lookup"><span data-stu-id="fc20e-489">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="fc20e-490">**IDE** (37) </span><span class="sxs-lookup"><span data-stu-id="fc20e-490">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="fc20e-491">**CMD** (38) </span><span class="sxs-lookup"><span data-stu-id="fc20e-491">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="fc20e-492">**ST506** (39) </span><span class="sxs-lookup"><span data-stu-id="fc20e-492">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="fc20e-493">**」 Dssi 小組** (40) </span><span class="sxs-lookup"><span data-stu-id="fc20e-493">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="fc20e-494">**QIC2** (41) </span><span class="sxs-lookup"><span data-stu-id="fc20e-494">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="fc20e-495">**增強型 ATA/IDE** (42) </span><span class="sxs-lookup"><span data-stu-id="fc20e-495">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="fc20e-496">**AGP** (43) </span><span class="sxs-lookup"><span data-stu-id="fc20e-496">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="fc20e-497">**TWIRP (雙向紅外線)** (44) </span><span class="sxs-lookup"><span data-stu-id="fc20e-497">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="fc20e-498">**(快速紅外線)** (45) 的杉樹</span><span class="sxs-lookup"><span data-stu-id="fc20e-498">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="fc20e-499">**SIR (串列紅外線)** (46) </span><span class="sxs-lookup"><span data-stu-id="fc20e-499">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="fc20e-500">**IrBus** (47) </span><span class="sxs-lookup"><span data-stu-id="fc20e-500">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fc20e-501">**狀態**</span><span class="sxs-lookup"><span data-stu-id="fc20e-501">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-502">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fc20e-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-503">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-503">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-504">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="fc20e-504">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-505">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="fc20e-505">Current status of the object.</span></span> <span data-ttu-id="fc20e-506">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="fc20e-506">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="fc20e-507">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="fc20e-507">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="fc20e-508">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="fc20e-508">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="fc20e-509">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="fc20e-509">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="fc20e-510">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="fc20e-510">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fc20e-511">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="fc20e-511">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="fc20e-512">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="fc20e-512">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="fc20e-513">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="fc20e-513">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="fc20e-514">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="fc20e-514">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="fc20e-515">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="fc20e-515">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="fc20e-516">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="fc20e-516">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="fc20e-517">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="fc20e-517">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="fc20e-518">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="fc20e-518">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="fc20e-519">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="fc20e-519">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fc20e-520">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="fc20e-520">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-521">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fc20e-521">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-522">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-523">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="fc20e-523">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-524">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="fc20e-524">State of the logical device.</span></span> <span data-ttu-id="fc20e-525">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="fc20e-525">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="fc20e-526">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="fc20e-526">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fc20e-527">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="fc20e-527">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fc20e-528">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="fc20e-528">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="fc20e-529">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="fc20e-529">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="fc20e-530">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="fc20e-530">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="fc20e-531">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="fc20e-531">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fc20e-532">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fc20e-532">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-533">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fc20e-533">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-534">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-534">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-535">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fc20e-535">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-536">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="fc20e-536">Scoping system's creation class name.</span></span>

<span data-ttu-id="fc20e-537">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="fc20e-537">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc20e-538">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="fc20e-538">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-539">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fc20e-539">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-540">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-541">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fc20e-541">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-542">設定系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="fc20e-542">Scoping system's name.</span></span>

<span data-ttu-id="fc20e-543">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="fc20e-543">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc20e-544">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="fc20e-544">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-545">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="fc20e-545">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-546">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-546">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-547">上次重設控制器的日期和時間，表示控制器已關機或重新初始化。</span><span class="sxs-lookup"><span data-stu-id="fc20e-547">Date and time the controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="fc20e-548">這個屬性繼承自 [**CIM \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="fc20e-548">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc20e-549">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="fc20e-549">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-550">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fc20e-550">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-551">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-551">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-552">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 003.6 ") </span><span class="sxs-lookup"><span data-stu-id="fc20e-552">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.6")</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-553">視訊記憶體的類型。</span><span class="sxs-lookup"><span data-stu-id="fc20e-553">Type of video memory.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fc20e-554">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="fc20e-554">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fc20e-555">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="fc20e-555">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="fc20e-556">**VRAM** (3) </span><span class="sxs-lookup"><span data-stu-id="fc20e-556">**VRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="fc20e-557">**DRAM** (4) </span><span class="sxs-lookup"><span data-stu-id="fc20e-557">**DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="fc20e-558">**SRAM** (5) </span><span class="sxs-lookup"><span data-stu-id="fc20e-558">**SRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="fc20e-559">**WRAM** (6) </span><span class="sxs-lookup"><span data-stu-id="fc20e-559">**WRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="fc20e-560">**EDO RAM** (7) </span><span class="sxs-lookup"><span data-stu-id="fc20e-560">**EDO RAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="fc20e-561">高載 **同步 DRAM** (8) </span><span class="sxs-lookup"><span data-stu-id="fc20e-561">**Burst Synchronous DRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="fc20e-562">**管線** 高載 SRAM (9) </span><span class="sxs-lookup"><span data-stu-id="fc20e-562">**Pipelined Burst SRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="fc20e-563">**CDRAM** (10) </span><span class="sxs-lookup"><span data-stu-id="fc20e-563">**CDRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="fc20e-564">**3DRAM** (11) </span><span class="sxs-lookup"><span data-stu-id="fc20e-564">**3DRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="fc20e-565">**SDRAM** (12) </span><span class="sxs-lookup"><span data-stu-id="fc20e-565">**SDRAM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="fc20e-566">**SGRAM** (13) </span><span class="sxs-lookup"><span data-stu-id="fc20e-566">**SGRAM** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fc20e-567">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="fc20e-567">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc20e-568">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fc20e-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc20e-569">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc20e-569">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc20e-570">描述視頻處理器或控制器的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="fc20e-570">Free-form string that describes the video processor or controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc20e-571">備註</span><span class="sxs-lookup"><span data-stu-id="fc20e-571">Remarks</span></span>

<span data-ttu-id="fc20e-572">**Cim \_ VideoController** 類別衍生自 [**cim \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="fc20e-572">The **CIM\_VideoController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="fc20e-573">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="fc20e-573">WMI does not implement this class.</span></span> <span data-ttu-id="fc20e-574">針對衍生自 **CIM \_ VIDEOCONTROLLER** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="fc20e-574">For WMI classes derived from **CIM\_VideoController**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="fc20e-575">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="fc20e-575">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fc20e-576">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="fc20e-576">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc20e-577">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc20e-577">Requirements</span></span>



| <span data-ttu-id="fc20e-578">需求</span><span class="sxs-lookup"><span data-stu-id="fc20e-578">Requirement</span></span> | <span data-ttu-id="fc20e-579">值</span><span class="sxs-lookup"><span data-stu-id="fc20e-579">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc20e-580">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fc20e-580">Minimum supported client</span></span><br/> | <span data-ttu-id="fc20e-581">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fc20e-581">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fc20e-582">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fc20e-582">Minimum supported server</span></span><br/> | <span data-ttu-id="fc20e-583">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc20e-583">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fc20e-584">命名空間</span><span class="sxs-lookup"><span data-stu-id="fc20e-584">Namespace</span></span><br/>                | <span data-ttu-id="fc20e-585">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fc20e-585">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fc20e-586">MOF</span><span class="sxs-lookup"><span data-stu-id="fc20e-586">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc20e-587"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc20e-587"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc20e-588">DLL</span><span class="sxs-lookup"><span data-stu-id="fc20e-588">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc20e-589"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc20e-589"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc20e-590">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc20e-590">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc20e-591">**CIM \_ 控制器**</span><span class="sxs-lookup"><span data-stu-id="fc20e-591">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

