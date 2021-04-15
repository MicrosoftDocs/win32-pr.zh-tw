---
description: 表示在執行 Windows 的電腦系統上，視訊控制器的功能和管理能力。
ms.assetid: 5c81994b-4a84-46ff-8689-09998dc66f91
ms.tgt_platform: multiple
title: Win32_VideoController 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoController
- Win32_VideoController.Reset
- Win32_VideoController.SetPowerState
- Win32_VideoController.AcceleratorCapabilities
- Win32_VideoController.AdapterCompatibility
- Win32_VideoController.AdapterDACType
- Win32_VideoController.AdapterRAM
- Win32_VideoController.Availability
- Win32_VideoController.CapabilityDescriptions
- Win32_VideoController.Caption
- Win32_VideoController.ColorTableEntries
- Win32_VideoController.ConfigManagerErrorCode
- Win32_VideoController.ConfigManagerUserConfig
- Win32_VideoController.CreationClassName
- Win32_VideoController.CurrentBitsPerPixel
- Win32_VideoController.CurrentHorizontalResolution
- Win32_VideoController.CurrentNumberOfColors
- Win32_VideoController.CurrentNumberOfColumns
- Win32_VideoController.CurrentNumberOfRows
- Win32_VideoController.CurrentRefreshRate
- Win32_VideoController.CurrentScanMode
- Win32_VideoController.CurrentVerticalResolution
- Win32_VideoController.Description
- Win32_VideoController.DeviceID
- Win32_VideoController.DeviceSpecificPens
- Win32_VideoController.DitherType
- Win32_VideoController.DriverDate
- Win32_VideoController.DriverVersion
- Win32_VideoController.ErrorCleared
- Win32_VideoController.ErrorDescription
- Win32_VideoController.ICMIntent
- Win32_VideoController.ICMMethod
- Win32_VideoController.InfFilename
- Win32_VideoController.InfSection
- Win32_VideoController.InstallDate
- Win32_VideoController.InstalledDisplayDrivers
- Win32_VideoController.LastErrorCode
- Win32_VideoController.MaxMemorySupported
- Win32_VideoController.MaxNumberControlled
- Win32_VideoController.MaxRefreshRate
- Win32_VideoController.MinRefreshRate
- Win32_VideoController.Monochrome
- Win32_VideoController.Name
- Win32_VideoController.NumberOfColorPlanes
- Win32_VideoController.NumberOfVideoPages
- Win32_VideoController.PNPDeviceID
- Win32_VideoController.PowerManagementCapabilities
- Win32_VideoController.PowerManagementSupported
- Win32_VideoController.ProtocolSupported
- Win32_VideoController.ReservedSystemPaletteEntries
- Win32_VideoController.SpecificationVersion
- Win32_VideoController.Status
- Win32_VideoController.StatusInfo
- Win32_VideoController.SystemCreationClassName
- Win32_VideoController.SystemName
- Win32_VideoController.SystemPaletteEntries
- Win32_VideoController.TimeOfLastReset
- Win32_VideoController.VideoArchitecture
- Win32_VideoController.VideoMemoryType
- Win32_VideoController.VideoMode
- Win32_VideoController.VideoModeDescription
- Win32_VideoController.VideoProcessor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: deb6903ba6cf27170539281da90569a14471999c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104467972"
---
# <a name="win32_videocontroller-class"></a><span data-ttu-id="92563-103">Win32 \_ VideoController 類別</span><span class="sxs-lookup"><span data-stu-id="92563-103">Win32\_VideoController class</span></span>

<span data-ttu-id="92563-104">**Win32 \_ VideoController** [WMI 類別](../wmisdk/retrieving-a-class.md)代表在執行 Windows 的電腦系統上，影片控制器的功能和管理能力。</span><span class="sxs-lookup"><span data-stu-id="92563-104">The **Win32\_VideoController** [WMI class](../wmisdk/retrieving-a-class.md) represents the capabilities and management capacity of the video controller on a computer system running Windows.</span></span>

<span data-ttu-id="92563-105">與 Windows 顯示驅動程式模型不相容的硬體 (WDDM) 會傳回這個類別之實例的不正確屬性值。</span><span class="sxs-lookup"><span data-stu-id="92563-105">Hardware that is not compatible with Windows Display Driver Model (WDDM) returns inaccurate property values for instances of this class.</span></span>

<span data-ttu-id="92563-106">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="92563-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="92563-107">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="92563-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="92563-108">語法</span><span class="sxs-lookup"><span data-stu-id="92563-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCF1-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class Win32_VideoController : CIM_PCVideoController
{
  uint16   AcceleratorCapabilities[];
  string   AdapterCompatibility;
  string   AdapterDACType;
  uint32   AdapterRAM;
  uint16   Availability;
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ColorTableEntries;
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
  uint32   DeviceSpecificPens;
  uint32   DitherType;
  datetime DriverDate;
  string   DriverVersion;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   ICMIntent;
  uint32   ICMMethod;
  string   InfFilename;
  string   InfSection;
  datetime InstallDate;
  string   InstalledDisplayDrivers;
  uint32   LastErrorCode;
  uint32   MaxMemorySupported;
  uint32   MaxNumberControlled;
  uint32   MaxRefreshRate;
  uint32   MinRefreshRate;
  boolean  Monochrome;
  string   Name;
  uint16   NumberOfColorPlanes;
  uint32   NumberOfVideoPages;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  uint32   ReservedSystemPaletteEntries;
  uint32   SpecificationVersion;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   SystemPaletteEntries;
  datetime TimeOfLastReset;
  uint16   VideoArchitecture;
  uint16   VideoMemoryType;
  uint16   VideoMode;
  string   VideoModeDescription;
  string   VideoProcessor;
};
```

## <a name="members"></a><span data-ttu-id="92563-109">成員</span><span class="sxs-lookup"><span data-stu-id="92563-109">Members</span></span>

<span data-ttu-id="92563-110">**Win32 \_ VideoController** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="92563-110">The **Win32\_VideoController** class has these types of members:</span></span>

-   [<span data-ttu-id="92563-111">方法</span><span class="sxs-lookup"><span data-stu-id="92563-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="92563-112">屬性</span><span class="sxs-lookup"><span data-stu-id="92563-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="92563-113">方法</span><span class="sxs-lookup"><span data-stu-id="92563-113">Methods</span></span>

<span data-ttu-id="92563-114">**Win32 \_ VideoController** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="92563-114">The **Win32\_VideoController** class has these methods.</span></span>



| <span data-ttu-id="92563-115">方法</span><span class="sxs-lookup"><span data-stu-id="92563-115">Method</span></span>            | <span data-ttu-id="92563-116">描述</span><span class="sxs-lookup"><span data-stu-id="92563-116">Description</span></span>                                                                                                                                                                                            |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92563-117">**重設**</span><span class="sxs-lookup"><span data-stu-id="92563-117">**Reset**</span></span>         | <span data-ttu-id="92563-118">未實作。</span><span class="sxs-lookup"><span data-stu-id="92563-118">Not implemented.</span></span> <span data-ttu-id="92563-119">若要執行此方法，請參閱 [**CIM \_ PCVideoController**](cim-pcvideocontroller.md)中的 [**Reset**](reset-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="92563-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span><br/>                 |
| <span data-ttu-id="92563-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="92563-120">**SetPowerState**</span></span> | <span data-ttu-id="92563-121">未實作。</span><span class="sxs-lookup"><span data-stu-id="92563-121">Not implemented.</span></span> <span data-ttu-id="92563-122">若要執行此方法，請參閱 [**CIM \_ PCVideoController**](cim-pcvideocontroller.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="92563-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="92563-123">屬性</span><span class="sxs-lookup"><span data-stu-id="92563-123">Properties</span></span>

<span data-ttu-id="92563-124">**Win32 \_ VideoController** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="92563-124">The **Win32\_VideoController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="92563-125">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="92563-125">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-126">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="92563-126">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="92563-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-128">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "[**CIM \_ VideoController**](cim-videocontroller.md).**CapabilityDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="92563-128">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_VideoController**](cim-videocontroller.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="92563-129">影片控制器的圖形陣列和立體功能。</span><span class="sxs-lookup"><span data-stu-id="92563-129">Array of graphics and 3-D capabilities of the video controller.</span></span>

<span data-ttu-id="92563-130">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-130">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="92563-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="92563-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="92563-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="92563-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="92563-133"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**圖形加速器** (2) </span><span class="sxs-lookup"><span data-stu-id="92563-133"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="92563-134"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**3D 加速器** (3) </span><span class="sxs-lookup"><span data-stu-id="92563-134"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**3D Accelerator** (3)</span></span>


</dt> <dd>

<span data-ttu-id="92563-135">3-d 加速器</span><span class="sxs-lookup"><span data-stu-id="92563-135">3-D Accelerator</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="92563-136">**AdapterCompatibility**</span><span class="sxs-lookup"><span data-stu-id="92563-136">**AdapterCompatibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="92563-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92563-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-139">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry" ) </span><span class="sxs-lookup"><span data-stu-id="92563-139">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="92563-140">此控制器使用的一般晶片來比較與系統之間的相容性。</span><span class="sxs-lookup"><span data-stu-id="92563-140">General chipset used for this controller to compare compatibilities with the system.</span></span>

</dd> <dt>

<span data-ttu-id="92563-141">**AdapterDACType**</span><span class="sxs-lookup"><span data-stu-id="92563-141">**AdapterDACType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="92563-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92563-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-144">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| HardwareInformation. DACType" ) </span><span class="sxs-lookup"><span data-stu-id="92563-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HardwareInformation.DACType")</span></span>
</dt> </dl>

<span data-ttu-id="92563-145">數位轉類比轉換器 (DAC) 晶片的名稱或識別碼。</span><span class="sxs-lookup"><span data-stu-id="92563-145">Name or identifier of the digital-to-analog converter (DAC) chip.</span></span> <span data-ttu-id="92563-146">這個屬性的字元集是英數位元。</span><span class="sxs-lookup"><span data-stu-id="92563-146">The character set of this property is alphanumeric.</span></span>

</dd> <dt>

<span data-ttu-id="92563-147">**AdapterRAM**</span><span class="sxs-lookup"><span data-stu-id="92563-147">**AdapterRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-148">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92563-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92563-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-150">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| HardwareInformation. MemorySize" ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="92563-150">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HardwareInformation.MemorySize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="92563-151">視訊卡的記憶體大小。</span><span class="sxs-lookup"><span data-stu-id="92563-151">Memory size of the video adapter.</span></span>

<span data-ttu-id="92563-152">範例：64000</span><span class="sxs-lookup"><span data-stu-id="92563-152">Example: 64000</span></span>

</dd> <dt>

<span data-ttu-id="92563-153">**可用性**</span><span class="sxs-lookup"><span data-stu-id="92563-153">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-154">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="92563-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="92563-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-156">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="92563-156">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="92563-157">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="92563-157">Availability and status of the device.</span></span>

<span data-ttu-id="92563-158">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-158">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="92563-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="92563-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="92563-160"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="92563-160"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="92563-161"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="92563-161"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="92563-162">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="92563-162">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="92563-163"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="92563-163"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="92563-164"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="92563-164"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="92563-165"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="92563-165"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="92563-166"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="92563-166"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="92563-167"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="92563-167"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="92563-168">離線</span><span class="sxs-lookup"><span data-stu-id="92563-168">Offline</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="92563-169"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="92563-169"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="92563-170"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="92563-170"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="92563-171"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="92563-171"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="92563-172"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="92563-172"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="92563-173"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="92563-173"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="92563-174">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="92563-174">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="92563-175"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="92563-175"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="92563-176">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="92563-176">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="92563-177"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="92563-177"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="92563-178">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="92563-178">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="92563-179"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="92563-179"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="92563-180"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="92563-180"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="92563-181">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="92563-181">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="92563-182"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="92563-182"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="92563-183">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="92563-183">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="92563-184"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="92563-184"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="92563-185">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="92563-185">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="92563-186"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="92563-186"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="92563-187">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="92563-187">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="92563-188"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="92563-188"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="92563-189">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="92563-189">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="92563-190">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="92563-190">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-191">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="92563-191">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="92563-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-193">限定詞： [**ArrayType**](../wmisdk/standard-qualifiers.md) ( "Indexed" ) ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "[**CIM \_ VideoController**](cim-videocontroller.md)。**AcceleratorCapabilities**") </span><span class="sxs-lookup"><span data-stu-id="92563-193">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_VideoController**](cim-videocontroller.md).**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="92563-194">自由格式字串提供 **AcceleratorCapabilities** 陣列中所指出之任何影片加速器功能的詳細說明。</span><span class="sxs-lookup"><span data-stu-id="92563-194">Free-form strings providing more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span> <span data-ttu-id="92563-195">請注意，這個陣列的每個專案都與 **AcceleratorCapabilities** 陣列中位於相同索引的專案有關。</span><span class="sxs-lookup"><span data-stu-id="92563-195">Note, each entry of this array is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span>

<span data-ttu-id="92563-196">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-196">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-197">**標題**</span><span class="sxs-lookup"><span data-stu-id="92563-197">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-198">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="92563-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92563-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-200">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="92563-200">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="92563-201">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="92563-201">Short description of the object.</span></span>

<span data-ttu-id="92563-202">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-202">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-203">**ColorTableEntries**</span><span class="sxs-lookup"><span data-stu-id="92563-203">**ColorTableEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-204">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92563-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92563-205">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-206">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)" ) </span><span class="sxs-lookup"><span data-stu-id="92563-206">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="92563-207">系統色彩表的大小。</span><span class="sxs-lookup"><span data-stu-id="92563-207">Size of the system's color table.</span></span> <span data-ttu-id="92563-208">裝置的色彩深度必須為每圖元不超過8個位;否則，就不會設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="92563-208">The device must have a color depth of no more than 8 bits per pixel; otherwise, this property is not set.</span></span>

<span data-ttu-id="92563-209">範例：256</span><span class="sxs-lookup"><span data-stu-id="92563-209">Example: 256</span></span>

</dd> <dt>

<span data-ttu-id="92563-210">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="92563-210">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-211">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92563-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92563-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-213">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="92563-213">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="92563-214">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="92563-214">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="92563-215">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-215">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="92563-216"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="92563-216"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="92563-217"> (0)</span><span class="sxs-lookup"><span data-stu-id="92563-217">(0)</span></span>


</dt> <dd>

<span data-ttu-id="92563-218">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="92563-218">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="92563-219"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="92563-219"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="92563-220">(1)</span><span class="sxs-lookup"><span data-stu-id="92563-220">(1)</span></span>


</dt> <dd>

<span data-ttu-id="92563-221">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="92563-221">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="92563-222"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="92563-222"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="92563-223">(2)</span><span class="sxs-lookup"><span data-stu-id="92563-223">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="92563-224"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="92563-224"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="92563-225">(3)</span><span class="sxs-lookup"><span data-stu-id="92563-225">(3)</span></span>


</dt> <dd>

<span data-ttu-id="92563-226">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="92563-226">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="92563-227"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="92563-227"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="92563-228">(4)</span><span class="sxs-lookup"><span data-stu-id="92563-228">(4)</span></span>


</dt> <dd>

<span data-ttu-id="92563-229">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="92563-229">Device is not working properly.</span></span> <span data-ttu-id="92563-230">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="92563-230">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="92563-231"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="92563-231"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="92563-232">(5)</span><span class="sxs-lookup"><span data-stu-id="92563-232">(5)</span></span>


</dt> <dd>

<span data-ttu-id="92563-233">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="92563-233">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="92563-234"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="92563-234"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="92563-235">(6)</span><span class="sxs-lookup"><span data-stu-id="92563-235">(6)</span></span>


</dt> <dd>

<span data-ttu-id="92563-236">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="92563-236">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="92563-237"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="92563-237"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="92563-238">(7)</span><span class="sxs-lookup"><span data-stu-id="92563-238">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="92563-239"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="92563-239"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="92563-240">(8)</span><span class="sxs-lookup"><span data-stu-id="92563-240">(8)</span></span>


</dt> <dd>

<span data-ttu-id="92563-241">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="92563-241">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="92563-242"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="92563-242"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="92563-243">(9)</span><span class="sxs-lookup"><span data-stu-id="92563-243">(9)</span></span>


</dt> <dd>

<span data-ttu-id="92563-244">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="92563-244">Device is not working properly.</span></span> <span data-ttu-id="92563-245">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="92563-245">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="92563-246"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="92563-246"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="92563-247">(10)</span><span class="sxs-lookup"><span data-stu-id="92563-247">(10)</span></span>


</dt> <dd>

<span data-ttu-id="92563-248">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="92563-248">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="92563-249"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="92563-249"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="92563-250">(11)</span><span class="sxs-lookup"><span data-stu-id="92563-250">(11)</span></span>


</dt> <dd>

<span data-ttu-id="92563-251">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="92563-251">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="92563-252"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="92563-252"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="92563-253"> (12) </span><span class="sxs-lookup"><span data-stu-id="92563-253">(12)</span></span>


</dt> <dd>

<span data-ttu-id="92563-254">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="92563-254">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="92563-255"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="92563-255"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="92563-256">(13)</span><span class="sxs-lookup"><span data-stu-id="92563-256">(13)</span></span>


</dt> <dd>

<span data-ttu-id="92563-257">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="92563-257">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="92563-258"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="92563-258"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="92563-259">(14)</span><span class="sxs-lookup"><span data-stu-id="92563-259">(14)</span></span>


</dt> <dd>

<span data-ttu-id="92563-260">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="92563-260">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="92563-261"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="92563-261"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="92563-262">(15)</span><span class="sxs-lookup"><span data-stu-id="92563-262">(15)</span></span>


</dt> <dd>

<span data-ttu-id="92563-263">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="92563-263">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="92563-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="92563-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="92563-265">(16)</span><span class="sxs-lookup"><span data-stu-id="92563-265">(16)</span></span>


</dt> <dd>

<span data-ttu-id="92563-266">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="92563-266">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="92563-267"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="92563-267"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="92563-268">(17)</span><span class="sxs-lookup"><span data-stu-id="92563-268">(17)</span></span>


</dt> <dd>

<span data-ttu-id="92563-269">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="92563-269">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="92563-270"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="92563-270"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="92563-271">(18)</span><span class="sxs-lookup"><span data-stu-id="92563-271">(18)</span></span>


</dt> <dd>

<span data-ttu-id="92563-272">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="92563-272">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="92563-273"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="92563-273"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="92563-274">(19)</span><span class="sxs-lookup"><span data-stu-id="92563-274">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="92563-275"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="92563-275"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="92563-276">(20)</span><span class="sxs-lookup"><span data-stu-id="92563-276">(20)</span></span>


</dt> <dd>

<span data-ttu-id="92563-277">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="92563-277">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="92563-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="92563-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="92563-279">(21)</span><span class="sxs-lookup"><span data-stu-id="92563-279">(21)</span></span>


</dt> <dd>

<span data-ttu-id="92563-280">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="92563-280">System failure.</span></span> <span data-ttu-id="92563-281">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="92563-281">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="92563-282">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="92563-282">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="92563-283"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="92563-283"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="92563-284">(22)</span><span class="sxs-lookup"><span data-stu-id="92563-284">(22)</span></span>


</dt> <dd>

<span data-ttu-id="92563-285">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="92563-285">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="92563-286"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="92563-286"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="92563-287">(23)</span><span class="sxs-lookup"><span data-stu-id="92563-287">(23)</span></span>


</dt> <dd>

<span data-ttu-id="92563-288">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="92563-288">System failure.</span></span> <span data-ttu-id="92563-289">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="92563-289">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="92563-290"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="92563-290"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="92563-291">(24)</span><span class="sxs-lookup"><span data-stu-id="92563-291">(24)</span></span>


</dt> <dd>

<span data-ttu-id="92563-292">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="92563-292">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="92563-293"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="92563-293"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="92563-294">(25)</span><span class="sxs-lookup"><span data-stu-id="92563-294">(25)</span></span>


</dt> <dd>

<span data-ttu-id="92563-295">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="92563-295">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="92563-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="92563-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="92563-297">(26)</span><span class="sxs-lookup"><span data-stu-id="92563-297">(26)</span></span>


</dt> <dd>

<span data-ttu-id="92563-298">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="92563-298">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="92563-299"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="92563-299"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="92563-300">(27)</span><span class="sxs-lookup"><span data-stu-id="92563-300">(27)</span></span>


</dt> <dd>

<span data-ttu-id="92563-301">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="92563-301">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="92563-302"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="92563-302"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="92563-303">(28)</span><span class="sxs-lookup"><span data-stu-id="92563-303">(28)</span></span>


</dt> <dd>

<span data-ttu-id="92563-304">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="92563-304">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="92563-305"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="92563-305"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="92563-306">(29)</span><span class="sxs-lookup"><span data-stu-id="92563-306">(29)</span></span>


</dt> <dd>

<span data-ttu-id="92563-307">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="92563-307">Device is disabled.</span></span> <span data-ttu-id="92563-308">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="92563-308">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="92563-309"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="92563-309"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="92563-310">(30)</span><span class="sxs-lookup"><span data-stu-id="92563-310">(30)</span></span>


</dt> <dd>

<span data-ttu-id="92563-311">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="92563-311">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="92563-312"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="92563-312"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="92563-313"> (31) </span><span class="sxs-lookup"><span data-stu-id="92563-313">(31)</span></span>


</dt> <dd>

<span data-ttu-id="92563-314">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="92563-314">Device is not working properly.</span></span> <span data-ttu-id="92563-315">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="92563-315">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="92563-316">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="92563-316">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-317">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="92563-317">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="92563-318">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-319">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="92563-319">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="92563-320">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="92563-320">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="92563-321">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-321">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-322">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="92563-322">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-323">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="92563-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92563-324">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-325">限定詞： [ **CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="92563-325">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="92563-326">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="92563-326">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="92563-327">搭配類別的其他索引鍵屬性使用時，此屬性可讓這個類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="92563-327">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="92563-328">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-329">**CurrentBitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="92563-329">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-330">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92563-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92563-331">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-332">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| Video \| 003.12 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" bits ") </span><span class="sxs-lookup"><span data-stu-id="92563-332">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.12"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="92563-333">用來顯示每個圖元的位數。</span><span class="sxs-lookup"><span data-stu-id="92563-333">Number of bits used to display each pixel.</span></span>

<span data-ttu-id="92563-334">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-334">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-335">**CurrentHorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="92563-335">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-336">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92563-336">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92563-337">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-338">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| Video \| 003.11 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" 圖元 ") </span><span class="sxs-lookup"><span data-stu-id="92563-338">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="92563-339">目前的水準圖元數目。</span><span class="sxs-lookup"><span data-stu-id="92563-339">Current number of horizontal pixels.</span></span>

<span data-ttu-id="92563-340">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-340">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-341">**CurrentNumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="92563-341">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-342">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="92563-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="92563-343">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92563-344">目前解析度所支援的色彩數目。</span><span class="sxs-lookup"><span data-stu-id="92563-344">Number of colors supported at the current resolution.</span></span>

<span data-ttu-id="92563-345">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-345">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="92563-346">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-346">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-347">**CurrentNumberOfColumns**</span><span class="sxs-lookup"><span data-stu-id="92563-347">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-348">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92563-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92563-349">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-350">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| Video \| 003.14 ") </span><span class="sxs-lookup"><span data-stu-id="92563-350">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.14")</span></span>
</dt> </dl>

<span data-ttu-id="92563-351">此影片控制器 (的資料行數目（以字元模式) ）。</span><span class="sxs-lookup"><span data-stu-id="92563-351">Number of columns for this video controller (if in character mode).</span></span> <span data-ttu-id="92563-352">否則，請輸入 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="92563-352">Otherwise, enter 0 (zero).</span></span>

<span data-ttu-id="92563-353">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-353">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-354">**CurrentNumberOfRows**</span><span class="sxs-lookup"><span data-stu-id="92563-354">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-355">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92563-355">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92563-356">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-357">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| Video \| 003.13 ") </span><span class="sxs-lookup"><span data-stu-id="92563-357">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="92563-358">此影片控制器 (的資料列數目（以字元模式) ）。</span><span class="sxs-lookup"><span data-stu-id="92563-358">Number of rows for this video controller (if in character mode).</span></span> <span data-ttu-id="92563-359">否則，請輸入 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="92563-359">Otherwise, enter 0 (zero).</span></span>

<span data-ttu-id="92563-360">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-360">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-361">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="92563-361">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-362">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92563-362">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92563-363">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-364">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "CurrentRefreshRate" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| HardwareInformation"。) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "赫茲" ) </span><span class="sxs-lookup"><span data-stu-id="92563-364">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("CurrentRefreshRate"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HardwareInformation."), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="92563-365">影片控制器重新整理監視器影像的頻率。</span><span class="sxs-lookup"><span data-stu-id="92563-365">Frequency at which the video controller refreshes the image for the monitor.</span></span> <span data-ttu-id="92563-366">值為 0 (零) 表示正在使用預設速率，而0xFFFFFFFF 表示使用的是最佳的速率。</span><span class="sxs-lookup"><span data-stu-id="92563-366">A value of 0 (zero) indicates the default rate is being used, while 0xFFFFFFFF indicates the optimal rate is being used.</span></span>

<span data-ttu-id="92563-367">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-367">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-368">**CurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="92563-368">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-369">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="92563-369">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="92563-370">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-371">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| Video \| 003.8 ") </span><span class="sxs-lookup"><span data-stu-id="92563-371">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="92563-372">目前的掃描模式。</span><span class="sxs-lookup"><span data-stu-id="92563-372">Current scan mode.</span></span>

<span data-ttu-id="92563-373">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-373">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="92563-374"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="92563-374"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="92563-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="92563-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="92563-376"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>**交錯** 式 (3) </span><span class="sxs-lookup"><span data-stu-id="92563-376"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>**Interlaced** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="92563-377"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**非交錯** 式 (4) </span><span class="sxs-lookup"><span data-stu-id="92563-377"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**Non Interlaced** (4)</span></span>


</dt> <dd>

<span data-ttu-id="92563-378">Noninterlaced</span><span class="sxs-lookup"><span data-stu-id="92563-378">Noninterlaced</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="92563-379">**CurrentVerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="92563-379">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-380">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92563-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92563-381">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-382">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| Video \| 003.10 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" 圖元 ") </span><span class="sxs-lookup"><span data-stu-id="92563-382">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.10"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="92563-383">目前的垂直圖元數目。</span><span class="sxs-lookup"><span data-stu-id="92563-383">Current number of vertical pixels.</span></span>

<span data-ttu-id="92563-384">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-384">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-385">**說明**</span><span class="sxs-lookup"><span data-stu-id="92563-385">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-386">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="92563-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92563-387">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-388">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="92563-388">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="92563-389">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="92563-389">Description of the object.</span></span>

<span data-ttu-id="92563-390">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-390">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-391">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="92563-391">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-392">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="92563-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92563-393">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-394">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "DeviceId" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="92563-394">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="92563-395">此影片控制器的電腦系統) 的唯一 (識別碼。</span><span class="sxs-lookup"><span data-stu-id="92563-395">Identifier (unique to the computer system) for this video controller.</span></span>

<span data-ttu-id="92563-396">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-397">**DeviceSpecificPens**</span><span class="sxs-lookup"><span data-stu-id="92563-397">**DeviceSpecificPens**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-398">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92563-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92563-399">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-400">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)" ) </span><span class="sxs-lookup"><span data-stu-id="92563-400">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="92563-401">裝置特定畫筆的目前數目。</span><span class="sxs-lookup"><span data-stu-id="92563-401">Current number of device-specific pens.</span></span> <span data-ttu-id="92563-402">值0xffff 表示裝置不支援畫筆。</span><span class="sxs-lookup"><span data-stu-id="92563-402">A value of 0xffff means that the device does not support pens.</span></span>

<span data-ttu-id="92563-403">範例：3</span><span class="sxs-lookup"><span data-stu-id="92563-403">Example: 3</span></span>

</dd> <dt>

<span data-ttu-id="92563-404">**DitherType**</span><span class="sxs-lookup"><span data-stu-id="92563-404">**DitherType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-405">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92563-405">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92563-406">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-407">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| EnumDisplaySettings" ) </span><span class="sxs-lookup"><span data-stu-id="92563-407">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|EnumDisplaySettings")</span></span>
</dt> </dl>

<span data-ttu-id="92563-408">影片控制器的遞色類型。</span><span class="sxs-lookup"><span data-stu-id="92563-408">Dither type of the video controller.</span></span> <span data-ttu-id="92563-409">屬性可以是其中一個預先定義的值，或是大於或等於256的驅動程式定義值。</span><span class="sxs-lookup"><span data-stu-id="92563-409">The property can be one of the predefined values, or a driver-defined value greater than or equal to 256.</span></span> <span data-ttu-id="92563-410">如果選擇了線條藝術遞色，控制器會使用遞色方法，在黑色、白色和灰色 scalings 之間產生定義完善的框線。</span><span class="sxs-lookup"><span data-stu-id="92563-410">If line art dithering is chosen, the controller uses a dithering method that produces well-defined borders between black, white, and gray scalings.</span></span> <span data-ttu-id="92563-411">線條藝術遞色不適合包含濃度和色調（如掃描的相片）中連續 graduations 的影像。</span><span class="sxs-lookup"><span data-stu-id="92563-411">Line art dithering is not suitable for images that include continuous graduations in intensity and hue such as scanned photographs.</span></span>

<dt>

<span id="No_dithering"></span><span id="no_dithering"></span><span id="NO_DITHERING"></span>

<span data-ttu-id="92563-412">**沒有遞色** (1) </span><span class="sxs-lookup"><span data-stu-id="92563-412">**No dithering** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Dithering_with_a_coarse_brush"></span><span id="dithering_with_a_coarse_brush"></span><span id="DITHERING_WITH_A_COARSE_BRUSH"></span>

<span data-ttu-id="92563-413">**使用粗略筆刷** (2) 遞色</span><span class="sxs-lookup"><span data-stu-id="92563-413">**Dithering with a coarse brush** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dithering_with_a_fine_brush"></span><span id="dithering_with_a_fine_brush"></span><span id="DITHERING_WITH_A_FINE_BRUSH"></span>

<span data-ttu-id="92563-414">**使用微調筆刷** (3) 遞色</span><span class="sxs-lookup"><span data-stu-id="92563-414">**Dithering with a fine brush** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_art_dithering"></span><span id="line_art_dithering"></span><span id="LINE_ART_DITHERING"></span>

<span data-ttu-id="92563-415">第 **藝術色** (4) </span><span class="sxs-lookup"><span data-stu-id="92563-415">**Line art dithering** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_does_gray_scaling"></span><span id="device_does_gray_scaling"></span><span id="DEVICE_DOES_GRAY_SCALING"></span>

<span data-ttu-id="92563-416">**裝置會以灰色縮放** (5) </span><span class="sxs-lookup"><span data-stu-id="92563-416">**Device does gray scaling** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="92563-417">**DriverDate**</span><span class="sxs-lookup"><span data-stu-id="92563-417">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-418">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="92563-418">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="92563-419">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-420">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ " ) </span><span class="sxs-lookup"><span data-stu-id="92563-420">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\")</span></span>
</dt> </dl>

<span data-ttu-id="92563-421">目前已安裝之視頻驅動程式的上次修改日期和時間。</span><span class="sxs-lookup"><span data-stu-id="92563-421">Last modification date and time of the currently installed video driver.</span></span>

</dd> <dt>

<span data-ttu-id="92563-422">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="92563-422">**DriverVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-423">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="92563-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92563-424">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-425">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| File 安裝程式庫函數 \| GetFileVersionInfo" ) </span><span class="sxs-lookup"><span data-stu-id="92563-425">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Installation Library Functions\|GetFileVersionInfo")</span></span>
</dt> </dl>

<span data-ttu-id="92563-426">影片驅動程式的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="92563-426">Version number of the video driver.</span></span>

</dd> <dt>

<span data-ttu-id="92563-427">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="92563-427">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-428">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="92563-428">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="92563-429">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92563-430">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="92563-430">If **TRUE**, the error reported in **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="92563-431">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-432">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="92563-432">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-433">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="92563-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92563-434">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92563-435">自由格式的字串提供 **LastErrorCode** 屬性中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="92563-435">Free-form string supplying more information about the error recorded in **LastErrorCode** property, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="92563-436">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-436">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-437">**ICMIntent**</span><span class="sxs-lookup"><span data-stu-id="92563-437">**ICMIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-438">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92563-438">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92563-439">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-439">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-440">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 列印和列印多工緩衝處理器結構 \| DevMode \| dmICMIntent」 ) </span><span class="sxs-lookup"><span data-stu-id="92563-440">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Printing and Print Spooler Structures\|DevMode\|dmICMIntent")</span></span>
</dt> </dl>

<span data-ttu-id="92563-441">預設應使用的三種可能色彩比對方法或意圖之一的特定值。</span><span class="sxs-lookup"><span data-stu-id="92563-441">Specific value of one of the three possible color-matching methods or intents that should be used by default.</span></span> <span data-ttu-id="92563-442">這個屬性主要用於非 ICM 應用程式。</span><span class="sxs-lookup"><span data-stu-id="92563-442">This property is used primarily for non-ICM applications.</span></span> <span data-ttu-id="92563-443">ICM 應用程式使用 ICM 函數來建立意圖。</span><span class="sxs-lookup"><span data-stu-id="92563-443">ICM applications establish intents by using the ICM functions.</span></span> <span data-ttu-id="92563-444">這個屬性可以是預先定義的值，或是大於或等於256的驅動程式定義值。</span><span class="sxs-lookup"><span data-stu-id="92563-444">This property can be a predefined value or a driver defined value greater than or equal to 256.</span></span> <span data-ttu-id="92563-445">當不需要遞色時，根據飽和度的色彩比對是最適合的商務圖形選擇。</span><span class="sxs-lookup"><span data-stu-id="92563-445">Color matching based on saturation is the most appropriate choice for business graphs when dithering is not desired.</span></span> <span data-ttu-id="92563-446">以對比為依據的色彩比對，在需要遞色時，是掃描或攝影影像最適合的選擇。</span><span class="sxs-lookup"><span data-stu-id="92563-446">Color matching based on contrast is the most appropriate choice for scanned or photographic images when dithering is desired.</span></span> <span data-ttu-id="92563-447">針對符合所要求的確切色彩進行優化的色彩比對，最適合在需要完全相符的色彩時，與商務標誌或其他影像一起使用。</span><span class="sxs-lookup"><span data-stu-id="92563-447">Color matching optimized to match the exact color requested is most appropriate for use with business logos or other images when an exact color match is desired.</span></span>

<dt>

<span id="Saturation"></span><span id="saturation"></span><span id="SATURATION"></span>

<span data-ttu-id="92563-448">**飽和度** (1) </span><span class="sxs-lookup"><span data-stu-id="92563-448">**Saturation** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Contrast"></span><span id="contrast"></span><span id="CONTRAST"></span>

<span data-ttu-id="92563-449">**對比** (2) </span><span class="sxs-lookup"><span data-stu-id="92563-449">**Contrast** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Exact_Color"></span><span id="exact_color"></span><span id="EXACT_COLOR"></span>

<span data-ttu-id="92563-450">**確切色彩** (3) </span><span class="sxs-lookup"><span data-stu-id="92563-450">**Exact Color** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="92563-451">**ICMMethod**</span><span class="sxs-lookup"><span data-stu-id="92563-451">**ICMMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-452">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92563-452">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92563-453">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-454">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 列印和列印多工緩衝處理器結構 \| DevMode \| dmICMMethod」 ) </span><span class="sxs-lookup"><span data-stu-id="92563-454">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Printing and Print Spooler Structures\|DevMode\|dmICMMethod")</span></span>
</dt> </dl>

<span data-ttu-id="92563-455">處理 ICM 的方法。</span><span class="sxs-lookup"><span data-stu-id="92563-455">Method of handling ICM.</span></span> <span data-ttu-id="92563-456">若為非 ICM 應用程式，此屬性會判斷是否已啟用 ICM。</span><span class="sxs-lookup"><span data-stu-id="92563-456">For non-ICM applications, this property determines if ICM is enabled.</span></span> <span data-ttu-id="92563-457">針對 ICM 應用程式，系統會檢查這個屬性，以判斷如何處理 ICM 支援。</span><span class="sxs-lookup"><span data-stu-id="92563-457">For ICM applications, the system examines this property to determine how to handle ICM support.</span></span> <span data-ttu-id="92563-458">這個屬性可以是預先定義的值，或是大於或等於256的驅動程式定義值。</span><span class="sxs-lookup"><span data-stu-id="92563-458">This property can be a predefined value or a driver-defined value greater than or equal to 256.</span></span> <span data-ttu-id="92563-459">此值會決定處理影像色彩比對的系統。</span><span class="sxs-lookup"><span data-stu-id="92563-459">The value determines which system handles image color matching.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="92563-460">**停用** (1) </span><span class="sxs-lookup"><span data-stu-id="92563-460">**Disabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows"></span><span id="windows"></span><span id="WINDOWS"></span>

<span data-ttu-id="92563-461">**Windows** (2) </span><span class="sxs-lookup"><span data-stu-id="92563-461">**Windows** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Driver"></span><span id="device_driver"></span><span id="DEVICE_DRIVER"></span>

<span data-ttu-id="92563-462">**設備磁碟機** (3) </span><span class="sxs-lookup"><span data-stu-id="92563-462">**Device Driver** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Destination_Device"></span><span id="destination_device"></span><span id="DESTINATION_DEVICE"></span>

<span data-ttu-id="92563-463">**目的地裝置** (4) </span><span class="sxs-lookup"><span data-stu-id="92563-463">**Destination Device** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="92563-464">**InfFilename**</span><span class="sxs-lookup"><span data-stu-id="92563-464">**InfFilename**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-465">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="92563-465">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92563-466">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-467">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E968-E325-11CE-BFC1-08002BE10318} \\ \\ 0000" ) </span><span class="sxs-lookup"><span data-stu-id="92563-467">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E968-E325-11CE-BFC1-08002BE10318}\\\\0000")</span></span>
</dt> </dl>

<span data-ttu-id="92563-468">視訊卡 .inf 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="92563-468">Path to the video adapter's .inf file.</span></span>

<span data-ttu-id="92563-469">範例： "C： \\ Windows \\ SYSTEM32 \\ 驅動程式"</span><span class="sxs-lookup"><span data-stu-id="92563-469">Example: "C:\\Windows\\SYSTEM32\\DRIVERS"</span></span>

</dd> <dt>

<span data-ttu-id="92563-470">**InfSection**</span><span class="sxs-lookup"><span data-stu-id="92563-470">**InfSection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-471">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="92563-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92563-472">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-473">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E968-E325-11CE-BFC1-08002BE10318} \\ \\ 0000" ) </span><span class="sxs-lookup"><span data-stu-id="92563-473">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E968-E325-11CE-BFC1-08002BE10318}\\\\0000")</span></span>
</dt> </dl>

<span data-ttu-id="92563-474">Windows 影片資訊所在 .inf 檔案的區段。</span><span class="sxs-lookup"><span data-stu-id="92563-474">Section of the .inf file where the Windows video information resides.</span></span>

</dd> <dt>

<span data-ttu-id="92563-475">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="92563-475">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-476">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="92563-476">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="92563-477">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-478">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="92563-478">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="92563-479">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="92563-479">Date and time the object was installed.</span></span> <span data-ttu-id="92563-480">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="92563-480">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="92563-481">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-481">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-482">**InstalledDisplayDrivers**</span><span class="sxs-lookup"><span data-stu-id="92563-482">**InstalledDisplayDrivers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-483">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="92563-483">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92563-484">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-485">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ " ) </span><span class="sxs-lookup"><span data-stu-id="92563-485">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\")</span></span>
</dt> </dl>

<span data-ttu-id="92563-486">已安裝顯示裝置磁碟機的名稱。</span><span class="sxs-lookup"><span data-stu-id="92563-486">Name of the installed display device driver.</span></span>

</dd> <dt>

<span data-ttu-id="92563-487">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="92563-487">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-488">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92563-488">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92563-489">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92563-490">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="92563-490">Last error code reported by the logical device.</span></span>

<span data-ttu-id="92563-491">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-492">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="92563-492">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-493">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92563-493">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92563-494">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-495">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="92563-495">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="92563-496">支援的最大記憶體數量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="92563-496">Maximum amount of memory supported in bytes.</span></span>

<span data-ttu-id="92563-497">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-497">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-498">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="92563-498">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-499">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92563-499">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92563-500">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-500">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-501">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 匯流排埠 \| 001.9 ") </span><span class="sxs-lookup"><span data-stu-id="92563-501">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="92563-502">此控制器可支援的直接可定址實體數目上限。</span><span class="sxs-lookup"><span data-stu-id="92563-502">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="92563-503">值為 0 (零) 如果數位未知，則應使用此值。</span><span class="sxs-lookup"><span data-stu-id="92563-503">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="92563-504">這個屬性繼承自 [**CIM \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-504">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-505">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="92563-505">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-506">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92563-506">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92563-507">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-508">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| Video \| 003.5 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" 赫茲 ") </span><span class="sxs-lookup"><span data-stu-id="92563-508">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="92563-509">影片控制器的最大重新整理速率（以赫茲為單位）。</span><span class="sxs-lookup"><span data-stu-id="92563-509">Maximum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="92563-510">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-510">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-511">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="92563-511">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-512">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92563-512">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92563-513">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-514">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| Video \| 003.4 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" 赫茲 ") </span><span class="sxs-lookup"><span data-stu-id="92563-514">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.4"), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="92563-515">影片控制器的最小更新速率（以赫茲為單位）。</span><span class="sxs-lookup"><span data-stu-id="92563-515">Minimum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="92563-516">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-516">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-517">**單色**</span><span class="sxs-lookup"><span data-stu-id="92563-517">**Monochrome**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-518">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="92563-518">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="92563-519">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-520">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="92563-520">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="92563-521">若 **為 TRUE**，則會使用灰色縮放來顯示影像。</span><span class="sxs-lookup"><span data-stu-id="92563-521">If **TRUE**, gray scale is used to display images.</span></span>

</dd> <dt>

<span data-ttu-id="92563-522">**名稱**</span><span class="sxs-lookup"><span data-stu-id="92563-522">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-523">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="92563-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92563-524">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-525">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="92563-525">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="92563-526">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="92563-526">Label by which the object is known.</span></span> <span data-ttu-id="92563-527">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="92563-527">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="92563-528">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-528">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-529">**NumberOfColorPlanes**</span><span class="sxs-lookup"><span data-stu-id="92563-529">**NumberOfColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-530">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="92563-530">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="92563-531">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-531">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92563-532">目前的色彩平面數目。</span><span class="sxs-lookup"><span data-stu-id="92563-532">Current number of color planes.</span></span> <span data-ttu-id="92563-533">如果此值不適用於目前的影片設定，請輸入 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="92563-533">If this value is not applicable for the current video configuration, enter 0 (zero).</span></span>

<span data-ttu-id="92563-534">這個屬性繼承自 [**CIM \_ PCVideoController**](cim-pcvideocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-534">This property is inherited from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-535">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="92563-535">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-536">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92563-536">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92563-537">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92563-538">提供目前的解析度和可用記憶體所支援的影片頁面數目。</span><span class="sxs-lookup"><span data-stu-id="92563-538">Number of video pages supported given the current resolutions and available memory.</span></span>

<span data-ttu-id="92563-539">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-539">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-540">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="92563-540">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-541">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="92563-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92563-542">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-543">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="92563-543">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="92563-544">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="92563-544">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="92563-545">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="92563-545">Example: "\*PNP030b"</span></span>

<span data-ttu-id="92563-546">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-546">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-547">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="92563-547">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-548">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="92563-548">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="92563-549">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-549">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92563-550">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="92563-550">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="92563-551">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-551">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="92563-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="92563-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="92563-553"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="92563-553"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="92563-554"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="92563-554"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="92563-555"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="92563-555"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="92563-556">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="92563-556">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="92563-557"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="92563-557"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="92563-558">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="92563-558">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="92563-559"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="92563-559"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="92563-560">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="92563-560">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="92563-561">這個方法可在父 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="92563-561">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="92563-562">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](../wmisdk/designing-managed-object-format--mof--classes.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-562">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="92563-563"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="92563-563"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="92563-564">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="92563-564">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="92563-565"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="92563-565"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="92563-566">支援計時 Power-On</span><span class="sxs-lookup"><span data-stu-id="92563-566">Timed Power-On Supported</span></span>

<span data-ttu-id="92563-567">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="92563-567">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="92563-568">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="92563-568">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-569">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="92563-569">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="92563-570">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-570">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92563-571">若 **為 TRUE**，則裝置可以是電源管理 (可進入暫停模式，依此類推) 。</span><span class="sxs-lookup"><span data-stu-id="92563-571">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="92563-572">屬性不表示電源管理功能目前已啟用，只有邏輯裝置能夠進行電源管理。</span><span class="sxs-lookup"><span data-stu-id="92563-572">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="92563-573">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-573">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-574">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="92563-574">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-575">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="92563-575">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="92563-576">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-576">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-577">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 匯流排埠 \| 001.2 "，" MIF。DMTF \| 磁片 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="92563-577">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="92563-578">控制器用來存取「受控制」裝置的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="92563-578">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="92563-579">這個屬性繼承自 [**CIM \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-579">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="92563-580"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="92563-580"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="92563-581"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="92563-581"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="92563-582"><span id="EISA"></span><span id="eisa"></span>**EISA** (3) </span><span class="sxs-lookup"><span data-stu-id="92563-582"><span id="EISA"></span><span id="eisa"></span>**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="92563-583"><span id="ISA"></span><span id="isa"></span>**ISA** (4) </span><span class="sxs-lookup"><span data-stu-id="92563-583"><span id="ISA"></span><span id="isa"></span>**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="92563-584"><span id="PCI"></span><span id="pci"></span>**PCI** (5) </span><span class="sxs-lookup"><span data-stu-id="92563-584"><span id="PCI"></span><span id="pci"></span>**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="92563-585"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6) </span><span class="sxs-lookup"><span data-stu-id="92563-585"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)</span></span>


</dt> <dd>

<span data-ttu-id="92563-586">ATA 或 ATAPI</span><span class="sxs-lookup"><span data-stu-id="92563-586">ATA or ATAPI</span></span>

</dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="92563-587"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**彈性磁片** (7) </span><span class="sxs-lookup"><span data-stu-id="92563-587"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="92563-588"><span id="1496"></span>**1496** (8) </span><span class="sxs-lookup"><span data-stu-id="92563-588"><span id="1496"></span>**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="92563-589"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**SCSI 平行介面** (9) </span><span class="sxs-lookup"><span data-stu-id="92563-589"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="92563-590"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**SCSI 光纖通道通訊協定** (10) </span><span class="sxs-lookup"><span data-stu-id="92563-590"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="92563-591"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**SCSI 序列匯流排通訊協定** (11) </span><span class="sxs-lookup"><span data-stu-id="92563-591"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="92563-592"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**SCSI 序列匯流排通訊協定-2 (1394)** (12) </span><span class="sxs-lookup"><span data-stu-id="92563-592"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="92563-593"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**SCSI 序列儲存架構** (13) </span><span class="sxs-lookup"><span data-stu-id="92563-593"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="92563-594"><span id="VESA"></span><span id="vesa"></span>**VESA** (14) </span><span class="sxs-lookup"><span data-stu-id="92563-594"><span id="VESA"></span><span id="vesa"></span>**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="92563-595"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15) </span><span class="sxs-lookup"><span data-stu-id="92563-595"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="92563-596"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**通用序列匯流排** (16) </span><span class="sxs-lookup"><span data-stu-id="92563-596"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="92563-597"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**平行通訊協定** (17) </span><span class="sxs-lookup"><span data-stu-id="92563-597"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="92563-598"><span id="ESCON"></span><span id="escon"></span>**ESCON** (18) </span><span class="sxs-lookup"><span data-stu-id="92563-598"><span id="ESCON"></span><span id="escon"></span>**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="92563-599"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**診斷** (19) </span><span class="sxs-lookup"><span data-stu-id="92563-599"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="92563-600"><span id="I2C"></span><span id="i2c"></span>**I2C** (20) </span><span class="sxs-lookup"><span data-stu-id="92563-600"><span id="I2C"></span><span id="i2c"></span>**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="92563-601"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (21) </span><span class="sxs-lookup"><span data-stu-id="92563-601"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="92563-602"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22) </span><span class="sxs-lookup"><span data-stu-id="92563-602"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="92563-603"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**MultiBus** (23) </span><span class="sxs-lookup"><span data-stu-id="92563-603"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="92563-604"><span id="VME"></span><span id="vme"></span>**Vm** (24) </span><span class="sxs-lookup"><span data-stu-id="92563-604"><span id="VME"></span><span id="vme"></span>**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="92563-605"><span id="IPI"></span><span id="ipi"></span>**IPI** (25) </span><span class="sxs-lookup"><span data-stu-id="92563-605"><span id="IPI"></span><span id="ipi"></span>**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="92563-606"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26) </span><span class="sxs-lookup"><span data-stu-id="92563-606"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="92563-607"><span id="RS232"></span><span id="rs232"></span>**RS232** (27) </span><span class="sxs-lookup"><span data-stu-id="92563-607"><span id="RS232"></span><span id="rs232"></span>**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="92563-608"><span id="ieee_802.3_10base5"></span>**IEEE 802.3 10BASE5** (28) </span><span class="sxs-lookup"><span data-stu-id="92563-608"><span id="ieee_802.3_10base5"></span>**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="92563-609"><span id="ieee_802.3_10base2"></span>**IEEE 802.3 10BASE2** (29) </span><span class="sxs-lookup"><span data-stu-id="92563-609"><span id="ieee_802.3_10base2"></span>**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="92563-610"><span id="ieee_802.3_1base5"></span>**IEEE 802.3 1BASE5** (30) </span><span class="sxs-lookup"><span data-stu-id="92563-610"><span id="ieee_802.3_1base5"></span>**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="92563-611"><span id="ieee_802.3_10broad36"></span>**IEEE 802.3 10BROAD36** (31) </span><span class="sxs-lookup"><span data-stu-id="92563-611"><span id="ieee_802.3_10broad36"></span>**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="92563-612"><span id="ieee_802.3_100basevg"></span>**IEEE 802.3 100BASEVG** (32) </span><span class="sxs-lookup"><span data-stu-id="92563-612"><span id="ieee_802.3_100basevg"></span>**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="92563-613"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**IEEE 802.5 權杖-環形** (33) </span><span class="sxs-lookup"><span data-stu-id="92563-613"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="92563-614"><span id="ansi_x3t9.5_fddi"></span>**ANSI x3t 9.5 FDDI** (34) </span><span class="sxs-lookup"><span data-stu-id="92563-614"><span id="ansi_x3t9.5_fddi"></span>**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="92563-615"><span id="MCA"></span><span id="mca"></span>**MCA** (35) </span><span class="sxs-lookup"><span data-stu-id="92563-615"><span id="MCA"></span><span id="mca"></span>**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="92563-616"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36) </span><span class="sxs-lookup"><span data-stu-id="92563-616"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="92563-617"><span id="IDE"></span><span id="ide"></span>**IDE** (37) </span><span class="sxs-lookup"><span data-stu-id="92563-617"><span id="IDE"></span><span id="ide"></span>**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="92563-618"><span id="CMD"></span><span id="cmd"></span>**CMD** (38) </span><span class="sxs-lookup"><span data-stu-id="92563-618"><span id="CMD"></span><span id="cmd"></span>**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="92563-619"><span id="ST506"></span><span id="st506"></span>**ST506** (39) </span><span class="sxs-lookup"><span data-stu-id="92563-619"><span id="ST506"></span><span id="st506"></span>**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="92563-620"><span id="DSSI"></span><span id="dssi"></span>**」 Dssi 小組** (40) </span><span class="sxs-lookup"><span data-stu-id="92563-620"><span id="DSSI"></span><span id="dssi"></span>**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="92563-621"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41) </span><span class="sxs-lookup"><span data-stu-id="92563-621"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="92563-622"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**增強型 ATA/IDE** (42) </span><span class="sxs-lookup"><span data-stu-id="92563-622"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="92563-623"><span id="AGP"></span><span id="agp"></span>**AGP** (43) </span><span class="sxs-lookup"><span data-stu-id="92563-623"><span id="AGP"></span><span id="agp"></span>**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="92563-624"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (雙向紅外線)** (44) </span><span class="sxs-lookup"><span data-stu-id="92563-624"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="92563-625"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**(快速紅外線)** (45) 的杉樹</span><span class="sxs-lookup"><span data-stu-id="92563-625"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="92563-626"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**SIR (串列紅外線)** (46) </span><span class="sxs-lookup"><span data-stu-id="92563-626"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="92563-627"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**IrBus** (47) </span><span class="sxs-lookup"><span data-stu-id="92563-627"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="92563-628">**ReservedSystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="92563-628">**ReservedSystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-629">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92563-629">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92563-630">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-630">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-631">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)" ) </span><span class="sxs-lookup"><span data-stu-id="92563-631">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="92563-632">系統調色板中的保留專案數目。</span><span class="sxs-lookup"><span data-stu-id="92563-632">Number of reserved entries in the system palette.</span></span> <span data-ttu-id="92563-633">作業系統可能會保留專案，以支援工作列和其他桌面顯示專案的標準色彩。</span><span class="sxs-lookup"><span data-stu-id="92563-633">The operating system may reserve entries to support standard colors for task bars and other desktop display items.</span></span> <span data-ttu-id="92563-634">只有當設備磁碟機在 RASTERCAPS 索引中設定 RC 選擇 **區 \_** 位時，此索引才有效，而且只有在驅動程式與16位 Windows 相容時才可使用。</span><span class="sxs-lookup"><span data-stu-id="92563-634">This index is valid only if the device driver sets the **RC\_PALETTE** bit in the RASTERCAPS index, and is available only if the driver is compatible with 16-bit Windows.</span></span> <span data-ttu-id="92563-635">如果系統未使用調色板，則不會設定 **ReservedSystemPaletteEntries** 。</span><span class="sxs-lookup"><span data-stu-id="92563-635">If the system is not using a palette, **ReservedSystemPaletteEntries** is not set.</span></span>

<span data-ttu-id="92563-636">範例：20</span><span class="sxs-lookup"><span data-stu-id="92563-636">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="92563-637">**SpecificationVersion**</span><span class="sxs-lookup"><span data-stu-id="92563-637">**SpecificationVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-638">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92563-638">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92563-639">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-639">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-640">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 列印和列印多工緩衝處理器結構 \| DevMode \| dmSpecVersion」 ) </span><span class="sxs-lookup"><span data-stu-id="92563-640">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Printing and Print Spooler Structures\|DevMode\|dmSpecVersion")</span></span>
</dt> </dl>

<span data-ttu-id="92563-641">結構以) 為基礎 (初始化資料規格的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="92563-641">Version number of the initialization data specification (upon which the structure is based).</span></span>

</dd> <dt>

<span data-ttu-id="92563-642">**狀態**</span><span class="sxs-lookup"><span data-stu-id="92563-642">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-643">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="92563-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92563-644">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-644">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-645">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="92563-645">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="92563-646">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="92563-646">Current status of the object.</span></span> <span data-ttu-id="92563-647">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="92563-647">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="92563-648">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="92563-648">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="92563-649">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="92563-649">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="92563-650">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="92563-650">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="92563-651">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="92563-651">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="92563-652">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-652">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="92563-653">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="92563-653">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="92563-654">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="92563-654">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="92563-655">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="92563-655">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="92563-656">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="92563-656">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="92563-657">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="92563-657">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="92563-658">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="92563-658">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="92563-659">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="92563-659">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="92563-660">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="92563-660">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="92563-661">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="92563-661">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="92563-662">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="92563-662">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="92563-663">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="92563-663">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="92563-664">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="92563-664">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="92563-665">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="92563-665">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="92563-666">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="92563-666">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-667">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="92563-667">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="92563-668">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-668">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-669">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="92563-669">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="92563-670">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="92563-670">State of the logical device.</span></span> <span data-ttu-id="92563-671">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="92563-671">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="92563-672">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-672">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="92563-673">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="92563-673">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="92563-674">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="92563-674">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="92563-675">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="92563-675">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="92563-676">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="92563-676">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="92563-677">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="92563-677">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="92563-678">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="92563-678">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-679">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="92563-679">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92563-680">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-680">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-681">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="92563-681">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="92563-682">範圍電腦之 **CreationClassName** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="92563-682">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="92563-683">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-683">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-684">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="92563-684">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-685">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="92563-685">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92563-686">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-686">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-687">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="92563-687">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="92563-688">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="92563-688">Name of the scoping system.</span></span>

<span data-ttu-id="92563-689">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-689">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-690">**SystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="92563-690">**SystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-691">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92563-691">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92563-692">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-692">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-693">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)" ) </span><span class="sxs-lookup"><span data-stu-id="92563-693">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="92563-694">系統調色板中目前的色彩索引項目數目。</span><span class="sxs-lookup"><span data-stu-id="92563-694">Current number of color index entries in the system palette.</span></span> <span data-ttu-id="92563-695">只有當設備磁碟機在 RASTERCAPS 索引中設定 RC 選擇 **區 \_** 位時，此索引才有效，而且只有在驅動程式與16位 Windows 相容時才可使用。</span><span class="sxs-lookup"><span data-stu-id="92563-695">This index is valid only if the device driver sets the **RC\_PALETTE** bit in the RASTERCAPS index, and is available only if the driver is compatible with 16-bit Windows.</span></span> <span data-ttu-id="92563-696">如果系統未使用調色板，則不會設定 **SystemPaletteEntries** 。</span><span class="sxs-lookup"><span data-stu-id="92563-696">If the system is not using a palette, **SystemPaletteEntries** is not set.</span></span>

<span data-ttu-id="92563-697">範例：20</span><span class="sxs-lookup"><span data-stu-id="92563-697">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="92563-698">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="92563-698">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-699">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="92563-699">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="92563-700">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-700">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92563-701">上次重設此控制器的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="92563-701">Date and time this controller was last reset.</span></span> <span data-ttu-id="92563-702">這可能表示控制器已關機或重新初始化。</span><span class="sxs-lookup"><span data-stu-id="92563-702">This could mean the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="92563-703">這個屬性繼承自 [**CIM \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-703">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-704">**VideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="92563-704">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-705">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="92563-705">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="92563-706">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-706">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-707">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| Video \| 003.2 ") </span><span class="sxs-lookup"><span data-stu-id="92563-707">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="92563-708">影片架構的類型。</span><span class="sxs-lookup"><span data-stu-id="92563-708">Type of video architecture.</span></span>

<span data-ttu-id="92563-709">這個屬性繼承自 [**CIM \_ PCVideoController**](cim-pcvideocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-709">This property is inherited from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="92563-710">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="92563-710">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="92563-711">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="92563-711">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CGA"></span><span id="cga"></span>

<span data-ttu-id="92563-712"> (3) 的 **CGA**</span><span class="sxs-lookup"><span data-stu-id="92563-712">**CGA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="EGA"></span><span id="ega"></span>

<span data-ttu-id="92563-713">**EGA** (4) </span><span class="sxs-lookup"><span data-stu-id="92563-713">**EGA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VGA"></span><span id="vga"></span>

<span data-ttu-id="92563-714">**VGA** (5) </span><span class="sxs-lookup"><span data-stu-id="92563-714">**VGA** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SVGA"></span><span id="svga"></span>

<span data-ttu-id="92563-715">**SVGA** (6) </span><span class="sxs-lookup"><span data-stu-id="92563-715">**SVGA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="MDA"></span><span id="mda"></span>

<span data-ttu-id="92563-716">**MDA** (7) </span><span class="sxs-lookup"><span data-stu-id="92563-716">**MDA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HGC"></span><span id="hgc"></span>

<span data-ttu-id="92563-717">**HGC** (8) </span><span class="sxs-lookup"><span data-stu-id="92563-717">**HGC** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="MCGA"></span><span id="mcga"></span>

<span data-ttu-id="92563-718">**MCGA** (9) </span><span class="sxs-lookup"><span data-stu-id="92563-718">**MCGA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="8514A"></span><span id="8514a"></span>

<span data-ttu-id="92563-719">**8514A** (10) </span><span class="sxs-lookup"><span data-stu-id="92563-719">**8514A** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="XGA"></span><span id="xga"></span>

<span data-ttu-id="92563-720">**XGA** (11) </span><span class="sxs-lookup"><span data-stu-id="92563-720">**XGA** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>

<span data-ttu-id="92563-721">**線性框架緩衝區** (12) </span><span class="sxs-lookup"><span data-stu-id="92563-721">**Linear Frame Buffer** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="92563-722">**PC-98** (160) </span><span class="sxs-lookup"><span data-stu-id="92563-722">**PC-98** (160)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="92563-723">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="92563-723">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-724">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="92563-724">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="92563-725">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-725">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-726">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| Video \| 003.6 ") </span><span class="sxs-lookup"><span data-stu-id="92563-726">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.6")</span></span>
</dt> </dl>

<span data-ttu-id="92563-727">視訊記憶體的類型。</span><span class="sxs-lookup"><span data-stu-id="92563-727">Type of video memory.</span></span>

<span data-ttu-id="92563-728">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-728">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="92563-729">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="92563-729">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="92563-730">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="92563-730">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="92563-731">**VRAM** (3) </span><span class="sxs-lookup"><span data-stu-id="92563-731">**VRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="92563-732">**DRAM** (4) </span><span class="sxs-lookup"><span data-stu-id="92563-732">**DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="92563-733">**SRAM** (5) </span><span class="sxs-lookup"><span data-stu-id="92563-733">**SRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="92563-734">**WRAM** (6) </span><span class="sxs-lookup"><span data-stu-id="92563-734">**WRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="92563-735">**EDO RAM** (7) </span><span class="sxs-lookup"><span data-stu-id="92563-735">**EDO RAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="92563-736">高載 **同步 DRAM** (8) </span><span class="sxs-lookup"><span data-stu-id="92563-736">**Burst Synchronous DRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="92563-737">**管線** 高載 SRAM (9) </span><span class="sxs-lookup"><span data-stu-id="92563-737">**Pipelined Burst SRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="92563-738">**CDRAM** (10) </span><span class="sxs-lookup"><span data-stu-id="92563-738">**CDRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="92563-739">**3DRAM** (11) </span><span class="sxs-lookup"><span data-stu-id="92563-739">**3DRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="92563-740">**SDRAM** (12) </span><span class="sxs-lookup"><span data-stu-id="92563-740">**SDRAM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="92563-741">**SGRAM** (13) </span><span class="sxs-lookup"><span data-stu-id="92563-741">**SGRAM** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="92563-742">**VideoMode**</span><span class="sxs-lookup"><span data-stu-id="92563-742">**VideoMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-743">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="92563-743">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="92563-744">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-744">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-745">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| Video \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="92563-745">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="92563-746">目前的影片模式。</span><span class="sxs-lookup"><span data-stu-id="92563-746">Current video mode.</span></span>

<span data-ttu-id="92563-747">這個屬性繼承自 [**CIM \_ PCVideoController**](cim-pcvideocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-747">This property is inherited from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="92563-748">**VideoModeDescription**</span><span class="sxs-lookup"><span data-stu-id="92563-748">**VideoModeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-749">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="92563-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92563-750">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-750">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92563-751">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)" ) </span><span class="sxs-lookup"><span data-stu-id="92563-751">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="92563-752">影片控制器目前的解析度、色彩和掃描模式設定。</span><span class="sxs-lookup"><span data-stu-id="92563-752">Current resolution, color, and scan mode settings of the video controller.</span></span>

<span data-ttu-id="92563-753">範例： "1024 x 768 x 256 色彩"</span><span class="sxs-lookup"><span data-stu-id="92563-753">Example: "1024 x 768 x 256 colors"</span></span>

</dd> <dt>

<span data-ttu-id="92563-754">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="92563-754">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92563-755">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="92563-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92563-756">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92563-756">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92563-757">描述視頻處理器的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="92563-757">Free-form string describing the video processor.</span></span>

<span data-ttu-id="92563-758">這個屬性繼承自 [**CIM \_ VideoController**](cim-videocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-758">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92563-759">備註</span><span class="sxs-lookup"><span data-stu-id="92563-759">Remarks</span></span>

<span data-ttu-id="92563-760">**Win32 \_ VideoController** 類別衍生自 [**CIM \_ PCVideoController**](cim-pcvideocontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="92563-760">The **Win32\_VideoController** class is derived from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

<span data-ttu-id="92563-761">如需使用此類別的詳細資訊，例如從多個監視器抓取資訊，請參閱 [使用 PowerShell 探索多監視器資訊](https://blogs.technet.com/b/heyscriptingguy/archive/2013/10/03/use-powershell-to-discover-multi-monitor-information.aspx)。</span><span class="sxs-lookup"><span data-stu-id="92563-761">For more information about using this class, such as retrieving information from multiple monitors, see [Use PowerShell to Discover Multi-Monitor Information](https://blogs.technet.com/b/heyscriptingguy/archive/2013/10/03/use-powershell-to-discover-multi-monitor-information.aspx).</span></span>

## <a name="examples"></a><span data-ttu-id="92563-762">範例</span><span class="sxs-lookup"><span data-stu-id="92563-762">Examples</span></span>

<span data-ttu-id="92563-763">[列出影片控制器屬性](https://Gallery.TechNet.Microsoft.Com/6c1a585c-742f-4f51-bb57-23838e8f011f)VBScript 範例會列出影片控制器屬性。</span><span class="sxs-lookup"><span data-stu-id="92563-763">The [List Video Controller Properties](https://Gallery.TechNet.Microsoft.Com/6c1a585c-742f-4f51-bb57-23838e8f011f) VBScript sample lists the video controller properties.</span></span>

<span data-ttu-id="92563-764">下列 PowerShell 範例會列出影片控制器屬性。</span><span class="sxs-lookup"><span data-stu-id="92563-764">The following PowerShell example lists the video controller properties.</span></span>


```VB
$strComputer = "." 
 
$colItems = get-wmiobject -class "Win32_VideoController" -namespace "root\CIMV2" ` 
-computername $strComputer 
 
foreach ($objItem in $colItems) { 
      write-host "Accelerator Capabilities: " $objItem.AcceleratorCapabilities 
      write-host "Adapter Compatibility: " $objItem.AdapterCompatibility 
      write-host "Adapter DAC Type: " $objItem.AdapterDACType 
      write-host "Adapter RAM: " $objItem.AdapterRAM 
      write-host "Availability: " $objItem.Availability 
      write-host "Capability Descriptions: " $objItem.CapabilityDescriptions 
      write-host "Caption: " $objItem.Caption 
      write-host "Color Table Entries: " $objItem.ColorTableEntries 
      write-host "Configuration Manager Error Code: " $objItem.ConfigManagerErrorCode 
      write-host "Configuration Manager User Configuration: " $objItem.ConfigManagerUserConfig 
      write-host "Creation Class Name: " $objItem.CreationClassName 
      write-host "Current Bits Per Pixel: " $objItem.CurrentBitsPerPixel 
      write-host "Current Horizontal Resolution: " $objItem.CurrentHorizontalResolution 
      write-host "Current Number Of Colors: " $objItem.CurrentNumberOfColors 
      write-host "Current Number Of Columns: " $objItem.CurrentNumberOfColumns 
      write-host "Current Number Of Rows: " $objItem.CurrentNumberOfRows 
      write-host "Current Refresh Rate: " $objItem.CurrentRefreshRate 
      write-host "Current Scan Mode: " $objItem.CurrentScanMode 
      write-host "Current Vertical Resolution: " $objItem.CurrentVerticalResolution 
      write-host "Description: " $objItem.Description 
      write-host "Device ID: " $objItem.DeviceID 
      write-host "Device Specific Pens: " $objItem.DeviceSpecificPens 
      write-host "Dither Type: " $objItem.DitherType 
      write-host "Driver Date: " $objItem.DriverDate 
      write-host "Driver Version: " $objItem.DriverVersion 
      write-host "Error Cleared: " $objItem.ErrorCleared 
      write-host "Error Description: " $objItem.ErrorDescription 
      write-host "ICM Intent: " $objItem.ICMIntent 
      write-host "ICM Method: " $objItem.ICMMethod 
      write-host "Inf File Name: " $objItem.InfFilename 
      write-host "Inf Section: " $objItem.InfSection 
      write-host "Installation Date: " $objItem.InstallDate 
      write-host "Installed Display Drivers: " $objItem.InstalledDisplayDrivers 
      write-host "Last Error Code: " $objItem.LastErrorCode 
      write-host "Maximum Memory Supported: " $objItem.MaxMemorySupported 
      write-host "Maximum Number Controlled: " $objItem.MaxNumberControlled 
      write-host "Maximum Refresh Rate: " $objItem.MaxRefreshRate 
      write-host "Minimum Refresh Rate: " $objItem.MinRefreshRate 
      write-host "Monochrome: " $objItem.Monochrome 
      write-host "Name: " $objItem.Name 
      write-host "Number Of Color Planes: " $objItem.NumberOfColorPlanes 
      write-host "Number Of Video Pages: " $objItem.NumberOfVideoPages 
      write-host "PNP Device ID: " $objItem.PNPDeviceID 
      write-host "Power Management Capabilities: " $objItem.PowerManagementCapabilities 
      write-host "Power Management Supported: " $objItem.PowerManagementSupported 
      write-host "Protocol Supported: " $objItem.ProtocolSupported 
      write-host "Reserved System Palette Entries: " $objItem.ReservedSystemPaletteEntries 
      write-host "Specification Version: " $objItem.SpecificationVersion 
      write-host "Status: " $objItem.Status 
      write-host "Status Information: " $objItem.StatusInfo 
      write-host "System Creation Class Name: " $objItem.SystemCreationClassName 
      write-host "System Name: " $objItem.SystemName 
      write-host "System Palette Entries: " $objItem.SystemPaletteEntries 
      write-host "Time Of Last Reset: " $objItem.TimeOfLastReset 
      write-host "Video Architecture: " $objItem.VideoArchitecture 
      write-host "Video Memory Type: " $objItem.VideoMemoryType 
      write-host "Video Mode: " $objItem.VideoMode 
      write-host "Video Mode Description: " $objItem.VideoModeDescription 
      write-host "Video Processor: " $objItem.VideoProcessor 
      write-host 
} 
```



## <a name="requirements"></a><span data-ttu-id="92563-765">規格需求</span><span class="sxs-lookup"><span data-stu-id="92563-765">Requirements</span></span>



| <span data-ttu-id="92563-766">需求</span><span class="sxs-lookup"><span data-stu-id="92563-766">Requirement</span></span> | <span data-ttu-id="92563-767">值</span><span class="sxs-lookup"><span data-stu-id="92563-767">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92563-768">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="92563-768">Minimum supported client</span></span><br/> | <span data-ttu-id="92563-769">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92563-769">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="92563-770">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="92563-770">Minimum supported server</span></span><br/> | <span data-ttu-id="92563-771">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92563-771">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="92563-772">命名空間</span><span class="sxs-lookup"><span data-stu-id="92563-772">Namespace</span></span><br/>                | <span data-ttu-id="92563-773">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="92563-773">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="92563-774">MOF</span><span class="sxs-lookup"><span data-stu-id="92563-774">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92563-775"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="92563-775"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="92563-776">DLL</span><span class="sxs-lookup"><span data-stu-id="92563-776">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92563-777"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92563-777"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92563-778">另請參閱</span><span class="sxs-lookup"><span data-stu-id="92563-778">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92563-779">**CIM \_ PCVideoController**</span><span class="sxs-lookup"><span data-stu-id="92563-779">**CIM\_PCVideoController**</span></span>](cim-pcvideocontroller.md)
</dt> <dt>

[<span data-ttu-id="92563-780">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="92563-780">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
