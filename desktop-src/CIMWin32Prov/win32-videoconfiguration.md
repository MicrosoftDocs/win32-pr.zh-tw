---
description: Win32 \_ VideoConfiguration 類別不在使用中。 因為沒有支援的提供者，所以它不會傳回任何實例。
ms.assetid: 8dd15e8a-ff9b-4e75-bae9-8c80548301ab
ms.tgt_platform: multiple
title: Win32_VideoConfiguration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoConfiguration
- Win32_VideoConfiguration.Caption
- Win32_VideoConfiguration.Description
- Win32_VideoConfiguration.SettingID
- Win32_VideoConfiguration.ActualColorResolution
- Win32_VideoConfiguration.AdapterChipType
- Win32_VideoConfiguration.AdapterCompatibility
- Win32_VideoConfiguration.AdapterDACType
- Win32_VideoConfiguration.AdapterDescription
- Win32_VideoConfiguration.AdapterRAM
- Win32_VideoConfiguration.AdapterType
- Win32_VideoConfiguration.BitsPerPixel
- Win32_VideoConfiguration.ColorPlanes
- Win32_VideoConfiguration.ColorTableEntries
- Win32_VideoConfiguration.DeviceSpecificPens
- Win32_VideoConfiguration.DriverDate
- Win32_VideoConfiguration.HorizontalResolution
- Win32_VideoConfiguration.InfFilename
- Win32_VideoConfiguration.InfSection
- Win32_VideoConfiguration.InstalledDisplayDrivers
- Win32_VideoConfiguration.MonitorManufacturer
- Win32_VideoConfiguration.MonitorType
- Win32_VideoConfiguration.Name
- Win32_VideoConfiguration.PixelsPerXLogicalInch
- Win32_VideoConfiguration.PixelsPerYLogicalInch
- Win32_VideoConfiguration.RefreshRate
- Win32_VideoConfiguration.ScanMode
- Win32_VideoConfiguration.ScreenHeight
- Win32_VideoConfiguration.ScreenWidth
- Win32_VideoConfiguration.SystemPaletteEntries
- Win32_VideoConfiguration.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 96ad4206cc50953a135b23257526ffb5cdc59b6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510460"
---
# <a name="win32_videoconfiguration-class"></a><span data-ttu-id="369bb-104">Win32 \_ VideoConfiguration 類別</span><span class="sxs-lookup"><span data-stu-id="369bb-104">Win32\_VideoConfiguration class</span></span>

<span data-ttu-id="369bb-105">**Win32 \_ VideoConfiguration** 類別不在使用中。</span><span class="sxs-lookup"><span data-stu-id="369bb-105">The **Win32\_VideoConfiguration** class is not active.</span></span> <span data-ttu-id="369bb-106">因為沒有支援的提供者，所以它不會傳回任何實例。</span><span class="sxs-lookup"><span data-stu-id="369bb-106">It will not return any instances as there is no provider backing it.</span></span>

<span data-ttu-id="369bb-107">**Win32 \_ VideoConfiguration** 類別代表影片子系統的設定。</span><span class="sxs-lookup"><span data-stu-id="369bb-107">The **Win32\_VideoConfiguration** class represents a configuration of a video subsystem.</span></span> <span data-ttu-id="369bb-108">這個類別已被取代，以取代 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md)和 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) 類別中包含的屬性</span><span class="sxs-lookup"><span data-stu-id="369bb-108">This class has been deprecated in favor of the properties contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), and [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) classes</span></span>

<span data-ttu-id="369bb-109">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="369bb-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="369bb-110">語法</span><span class="sxs-lookup"><span data-stu-id="369bb-110">Syntax</span></span>

``` syntax
[DEPRECATED, UUID("{8502C4ED-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_VideoConfiguration : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  uint32   ActualColorResolution;
  string   AdapterChipType;
  string   AdapterCompatibility;
  string   AdapterDACType;
  string   AdapterDescription;
  uint32   AdapterRAM;
  string   AdapterType;
  uint32   BitsPerPixel;
  uint32   ColorPlanes;
  uint32   ColorTableEntries;
  uint32   DeviceSpecificPens;
  datetime DriverDate;
  uint32   HorizontalResolution;
  string   InfFilename;
  string   InfSection;
  string   InstalledDisplayDrivers;
  string   MonitorManufacturer;
  string   MonitorType;
  string   Name;
  uint32   PixelsPerXLogicalInch;
  uint32   PixelsPerYLogicalInch;
  uint32   RefreshRate;
  string   ScanMode;
  uint32   ScreenHeight;
  uint32   ScreenWidth;
  uint32   SystemPaletteEntries;
  uint32   VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="369bb-111">成員</span><span class="sxs-lookup"><span data-stu-id="369bb-111">Members</span></span>

<span data-ttu-id="369bb-112">**Win32 \_ VideoConfiguration** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="369bb-112">The **Win32\_VideoConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="369bb-113">屬性</span><span class="sxs-lookup"><span data-stu-id="369bb-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="369bb-114">屬性</span><span class="sxs-lookup"><span data-stu-id="369bb-114">Properties</span></span>

<span data-ttu-id="369bb-115">**Win32 \_ VideoConfiguration** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="369bb-115">The **Win32\_VideoConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="369bb-116">**ActualColorResolution**</span><span class="sxs-lookup"><span data-stu-id="369bb-116">**ActualColorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-117">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="369bb-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-119">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API 裝置內容函式 \| \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| COLORRES」 ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( 「每個圖元的位」 ) </span><span class="sxs-lookup"><span data-stu-id="369bb-119">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|COLORRES"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits per pixel")</span></span>
</dt> </dl>

<span data-ttu-id="369bb-120">表示影片顯示的目前色彩深度。</span><span class="sxs-lookup"><span data-stu-id="369bb-120">Indicates the current color depth of the video display.</span></span>

<span data-ttu-id="369bb-121">這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-121">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-122">**AdapterChipType**</span><span class="sxs-lookup"><span data-stu-id="369bb-122">**AdapterChipType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="369bb-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-125">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ Info \| ChipType" ) </span><span class="sxs-lookup"><span data-stu-id="369bb-125">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Info\|ChipType")</span></span>
</dt> </dl>

<span data-ttu-id="369bb-126">包含介面卡晶片的名稱。</span><span class="sxs-lookup"><span data-stu-id="369bb-126">Contains the name of the adapter chip.</span></span>

<span data-ttu-id="369bb-127">範例： s3</span><span class="sxs-lookup"><span data-stu-id="369bb-127">Example: s3</span></span>

<span data-ttu-id="369bb-128">這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-128">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-129">**AdapterCompatibility**</span><span class="sxs-lookup"><span data-stu-id="369bb-129">**AdapterCompatibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="369bb-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-132">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)、 [**key**](../wmisdk/key-qualifier.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="369bb-132">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="369bb-133">指定介面卡製造商的名稱。</span><span class="sxs-lookup"><span data-stu-id="369bb-133">Specifies the name of the manufacturer of the adapter.</span></span> <span data-ttu-id="369bb-134">此名稱可用來比較此裝置的相容性與電腦系統的需求。</span><span class="sxs-lookup"><span data-stu-id="369bb-134">This name can be used to compare the compatibility of this device with the needs of the computer system.</span></span>

<span data-ttu-id="369bb-135">這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-135">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-136">**AdapterDACType**</span><span class="sxs-lookup"><span data-stu-id="369bb-136">**AdapterDACType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="369bb-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-139">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ Info \| DACType" ) </span><span class="sxs-lookup"><span data-stu-id="369bb-139">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Info\|DACType")</span></span>
</dt> </dl>

<span data-ttu-id="369bb-140">指出介面卡中使用的數位到類比晶片 (DAC) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="369bb-140">Indicates the name of the digital-to-analog chip (DAC) used in the adapter.</span></span>

<span data-ttu-id="369bb-141">這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-141">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-142">**AdapterDescription**</span><span class="sxs-lookup"><span data-stu-id="369bb-142">**AdapterDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="369bb-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-145">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="369bb-145">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="369bb-146">包含視訊卡的描述或描述性名稱。</span><span class="sxs-lookup"><span data-stu-id="369bb-146">Contains a description or descriptive name of the video adapter.</span></span>

<span data-ttu-id="369bb-147">這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-147">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-148">**AdapterRAM**</span><span class="sxs-lookup"><span data-stu-id="369bb-148">**AdapterRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-149">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="369bb-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-151">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ Info \| VideoMemory" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="369bb-151">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Info\|VideoMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="369bb-152">表示視訊卡的記憶體大小。</span><span class="sxs-lookup"><span data-stu-id="369bb-152">Indicates the memory size of the video adapter.</span></span>

<span data-ttu-id="369bb-153">範例：16777216</span><span class="sxs-lookup"><span data-stu-id="369bb-153">Example: 16777216</span></span>

<span data-ttu-id="369bb-154">這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-154">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-155">**AdapterType**</span><span class="sxs-lookup"><span data-stu-id="369bb-155">**AdapterType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="369bb-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-158">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32Registry \| 硬體 \\ \\ 描述 \\ \\ 系統 \\ \\ DisplayController \\ \\ 0 \\ \\ 識別碼」 ) </span><span class="sxs-lookup"><span data-stu-id="369bb-158">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HARDWARE\\\\Description\\\\System\\\\DisplayController\\\\0\\\\Identifier")</span></span>
</dt> </dl>

<span data-ttu-id="369bb-159">表示視訊卡的類型。</span><span class="sxs-lookup"><span data-stu-id="369bb-159">Indicates the type of video adapter.</span></span>

<span data-ttu-id="369bb-160">字元集：英數位元</span><span class="sxs-lookup"><span data-stu-id="369bb-160">Character Set: Alphanumeric</span></span>

<span data-ttu-id="369bb-161">這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-161">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-162">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="369bb-162">**BitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-163">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="369bb-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-165">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| BITSPIXEL" ) </span><span class="sxs-lookup"><span data-stu-id="369bb-165">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|BITSPIXEL")</span></span>
</dt> </dl>

<span data-ttu-id="369bb-166">指出代表顯示的每個圖元的實際位數。</span><span class="sxs-lookup"><span data-stu-id="369bb-166">Indicates the actual number of bits per pixel representing the display.</span></span> <span data-ttu-id="369bb-167">這可能會調整為目前的影片設定 (由使用者的 ActualColorResolution 屬性) 表示。</span><span class="sxs-lookup"><span data-stu-id="369bb-167">This may be scaled to the current video setting (represented by the ActualColorResolution property) of the user.</span></span>

<span data-ttu-id="369bb-168">範例：8</span><span class="sxs-lookup"><span data-stu-id="369bb-168">Example: 8</span></span>

<span data-ttu-id="369bb-169">這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-169">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-170">**標題**</span><span class="sxs-lookup"><span data-stu-id="369bb-170">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-171">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="369bb-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-173">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="369bb-173">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="369bb-174">目前物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="369bb-174">Short textual description of the current object.</span></span>

<span data-ttu-id="369bb-175">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="369bb-175">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-176">**ColorPlanes**</span><span class="sxs-lookup"><span data-stu-id="369bb-176">**ColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-177">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="369bb-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-179">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API 裝置內容函式 \| \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| 平面」 ) </span><span class="sxs-lookup"><span data-stu-id="369bb-179">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|PLANES")</span></span>
</dt> </dl>

<span data-ttu-id="369bb-180">指出影片顯示中使用的目前色彩平面數目。</span><span class="sxs-lookup"><span data-stu-id="369bb-180">Indicates the current number of color planes used in the video display.</span></span> <span data-ttu-id="369bb-181">色彩平面是代表圖元色彩的另一種方式;色彩平面會將圖形分隔為每個主要色彩元件 (紅色綠色的) ，並將其儲存在自己的平面中，而不是將單一 RGB 值指派給每個圖元。</span><span class="sxs-lookup"><span data-stu-id="369bb-181">A color plane is another way to represent pixel colors; instead of assigning a single RGB value to each a pixel, color planes separate the graphic into each of the primary color components (red green blue), and store them in their own planes.</span></span> <span data-ttu-id="369bb-182">這允許在8和16位的影片系統上有更高的色彩深度。</span><span class="sxs-lookup"><span data-stu-id="369bb-182">This allows for greater color depths on 8 and 16 bit video systems.</span></span> <span data-ttu-id="369bb-183">呈現圖形系統的 bitwidth 夠大，足以儲存色彩深度資訊，因此只需要一個色彩平面。</span><span class="sxs-lookup"><span data-stu-id="369bb-183">Present graphics systems have the bitwidth large enough to store color depth information, making only one color plane necessary.</span></span>

<span data-ttu-id="369bb-184">範例：1</span><span class="sxs-lookup"><span data-stu-id="369bb-184">Example: 1</span></span>

<span data-ttu-id="369bb-185">這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-185">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-186">**ColorTableEntries**</span><span class="sxs-lookup"><span data-stu-id="369bb-186">**ColorTableEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-187">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="369bb-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-189">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| NUMCOLORS" ) </span><span class="sxs-lookup"><span data-stu-id="369bb-189">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|NUMCOLORS")</span></span>
</dt> </dl>

<span data-ttu-id="369bb-190">表示影片顯示色彩表中的色彩索引數目。</span><span class="sxs-lookup"><span data-stu-id="369bb-190">Indicates the number of color indexes in a color table for a video display.</span></span> <span data-ttu-id="369bb-191">如果裝置的色彩深度小於每圖元8位，則會使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="369bb-191">This property is used if the device has a color depth of no more than 8 bits per pixel.</span></span> <span data-ttu-id="369bb-192">如果裝置具有較高的色彩深度，則會傳回-1。</span><span class="sxs-lookup"><span data-stu-id="369bb-192">For devices with greater color depths, -1 is returned.</span></span>

<span data-ttu-id="369bb-193">範例：256</span><span class="sxs-lookup"><span data-stu-id="369bb-193">Example: 256</span></span>

<span data-ttu-id="369bb-194">這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-194">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-195">**說明**</span><span class="sxs-lookup"><span data-stu-id="369bb-195">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-196">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="369bb-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="369bb-198">目前物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="369bb-198">Textual description of the current object.</span></span>

<span data-ttu-id="369bb-199">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="369bb-199">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-200">**DeviceSpecificPens**</span><span class="sxs-lookup"><span data-stu-id="369bb-200">**DeviceSpecificPens**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-201">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="369bb-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-203">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| NUMPENS" ) </span><span class="sxs-lookup"><span data-stu-id="369bb-203">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|NUMPENS")</span></span>
</dt> </dl>

<span data-ttu-id="369bb-204">指出目前的裝置特定畫筆數目。</span><span class="sxs-lookup"><span data-stu-id="369bb-204">Indicates the current number of device-specific pens.</span></span> <span data-ttu-id="369bb-205">0xFFFFFFFF 的值表示裝置不支援畫筆。</span><span class="sxs-lookup"><span data-stu-id="369bb-205">A value of 0xFFFFFFFF means the device does not support pens.</span></span> <span data-ttu-id="369bb-206">畫筆用來繪製多邊形物件的線條和 theborders。</span><span class="sxs-lookup"><span data-stu-id="369bb-206">Pens are used to draw lines and theborders of polygonal objects.</span></span>

<span data-ttu-id="369bb-207">範例：3</span><span class="sxs-lookup"><span data-stu-id="369bb-207">Example: 3</span></span>

<span data-ttu-id="369bb-208">這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-208">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-209">**DriverDate**</span><span class="sxs-lookup"><span data-stu-id="369bb-209">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-210">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="369bb-210">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-212">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ AdapterDescription \| DriverDate" ) </span><span class="sxs-lookup"><span data-stu-id="369bb-212">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\AdapterDescription\|DriverDate")</span></span>
</dt> </dl>

<span data-ttu-id="369bb-213">指出目前的視頻驅動程式安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="369bb-213">Indicates the date and time the current video driver was installed.</span></span>

<span data-ttu-id="369bb-214">這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-214">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-215">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="369bb-215">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-216">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="369bb-216">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-218">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| HORZRES" ) </span><span class="sxs-lookup"><span data-stu-id="369bb-218">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|HORZRES")</span></span>
</dt> </dl>

<span data-ttu-id="369bb-219">以水準方向指出目前的圖元數目 (X 軸的顯示) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-219">Indicates the current number of pixels in the horizontal direction (X axis) of the display.</span></span>

<span data-ttu-id="369bb-220">範例：1024</span><span class="sxs-lookup"><span data-stu-id="369bb-220">Example: 1024</span></span>

<span data-ttu-id="369bb-221">這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-221">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-222">**InfFilename**</span><span class="sxs-lookup"><span data-stu-id="369bb-222">**InfFilename**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-223">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="369bb-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-225">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \| InfPath" ) </span><span class="sxs-lookup"><span data-stu-id="369bb-225">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\|InfPath")</span></span>
</dt> </dl>

<span data-ttu-id="369bb-226">指定視頻驅動程式 .inf 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="369bb-226">Specifies the path to the .inf file of the video driver.</span></span>

<span data-ttu-id="369bb-227">範例： C： \\ Windows \\ System32 \\ 驅動程式</span><span class="sxs-lookup"><span data-stu-id="369bb-227">Example: C:\\Windows\\System32\\Drivers</span></span>

<span data-ttu-id="369bb-228">這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-228">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-229">**InfSection**</span><span class="sxs-lookup"><span data-stu-id="369bb-229">**InfSection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-230">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="369bb-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-232">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \| InfSection" ) </span><span class="sxs-lookup"><span data-stu-id="369bb-232">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\|InfSection")</span></span>
</dt> </dl>

<span data-ttu-id="369bb-233">指出 Win32 影片資訊所在之 .inf 檔案的區段。</span><span class="sxs-lookup"><span data-stu-id="369bb-233">Indicates the section of the .inf file where the Win32 video information resides.</span></span>

<span data-ttu-id="369bb-234">這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-234">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-235">**InstalledDisplayDrivers**</span><span class="sxs-lookup"><span data-stu-id="369bb-235">**InstalledDisplayDrivers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-236">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="369bb-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-237">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-238">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ Defaule \| winspool.drv" ) </span><span class="sxs-lookup"><span data-stu-id="369bb-238">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Defaule\|drv")</span></span>
</dt> </dl>

<span data-ttu-id="369bb-239">表示已安裝的視頻驅動程式名稱。</span><span class="sxs-lookup"><span data-stu-id="369bb-239">Indicates the name of the installed video driver.</span></span>

<span data-ttu-id="369bb-240">這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-240">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-241">**MonitorManufacturer**</span><span class="sxs-lookup"><span data-stu-id="369bb-241">**MonitorManufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-242">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="369bb-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-243">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-244">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="369bb-244">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="369bb-245">指出顯示裝置的製造商名稱。</span><span class="sxs-lookup"><span data-stu-id="369bb-245">Indicates the name of the manufacturer of the display device.</span></span>

<span data-ttu-id="369bb-246">範例： NEC</span><span class="sxs-lookup"><span data-stu-id="369bb-246">Example: NEC</span></span>

<span data-ttu-id="369bb-247">這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-247">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-248">**監視類型**</span><span class="sxs-lookup"><span data-stu-id="369bb-248">**MonitorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-249">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="369bb-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-250">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-251">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32Registry \| 硬體 \\ \\ 描述 \\ \\ 系統 \\ \\ MonitorPeripheral \\ \\ 0 \| 識別碼」 ) </span><span class="sxs-lookup"><span data-stu-id="369bb-251">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HARDWARE\\\\Description\\\\System\\\\MonitorPeripheral\\\\0\|Identifier")</span></span>
</dt> </dl>

<span data-ttu-id="369bb-252">指出顯示裝置的型號名稱。</span><span class="sxs-lookup"><span data-stu-id="369bb-252">Indicates the model name of the display device.</span></span>

<span data-ttu-id="369bb-253">範例： NEC 5FGp</span><span class="sxs-lookup"><span data-stu-id="369bb-253">Example: NEC 5FGp</span></span>

<span data-ttu-id="369bb-254">這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-254">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-255">**名稱**</span><span class="sxs-lookup"><span data-stu-id="369bb-255">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-256">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="369bb-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-257">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-258">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)、 [**key**](../wmisdk/key-qualifier.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="369bb-258">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="369bb-259">包含 video configuration 類別的識別名稱。</span><span class="sxs-lookup"><span data-stu-id="369bb-259">Contains an identifying name for the video configuration class.</span></span>

<span data-ttu-id="369bb-260">這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-260">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-261">**PixelsPerXLogicalInch**</span><span class="sxs-lookup"><span data-stu-id="369bb-261">**PixelsPerXLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-262">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="369bb-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-263">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-264">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| LOGPIXELSX" ) </span><span class="sxs-lookup"><span data-stu-id="369bb-264">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|LOGPIXELSX")</span></span>
</dt> </dl>

<span data-ttu-id="369bb-265">指出沿著 X 軸的每個邏輯英寸的圖元數 (水準方向) 顯示。</span><span class="sxs-lookup"><span data-stu-id="369bb-265">Indicates the number of pixels per logical inch along the X axis (horizontal direction) of the display.</span></span>

<span data-ttu-id="369bb-266">這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-266">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-267">**PixelsPerYLogicalInch**</span><span class="sxs-lookup"><span data-stu-id="369bb-267">**PixelsPerYLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-268">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="369bb-268">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-269">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-270">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| LOGPIXELSY" ) </span><span class="sxs-lookup"><span data-stu-id="369bb-270">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|LOGPIXELSY")</span></span>
</dt> </dl>

<span data-ttu-id="369bb-271">指出沿著 Y 軸的每個邏輯英寸的圖元數， (垂直方向) 顯示。</span><span class="sxs-lookup"><span data-stu-id="369bb-271">Indicates the number of pixels per logical inch along the Y axis (vertical direction) of the display.</span></span>

<span data-ttu-id="369bb-272">這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-272">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-273">**RefreshRate**</span><span class="sxs-lookup"><span data-stu-id="369bb-273">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-274">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="369bb-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-275">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-276">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VREFRESH" ) </span><span class="sxs-lookup"><span data-stu-id="369bb-276">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|VREFRESH")</span></span>
</dt> </dl>

<span data-ttu-id="369bb-277">指出影片設定的更新頻率。</span><span class="sxs-lookup"><span data-stu-id="369bb-277">Indicates the refresh rate of the video configuration.</span></span> <span data-ttu-id="369bb-278">0或1值表示正在使用預設費率。</span><span class="sxs-lookup"><span data-stu-id="369bb-278">A value of 0 or 1 indicates a default rate is being used.</span></span>

<span data-ttu-id="369bb-279">範例：72</span><span class="sxs-lookup"><span data-stu-id="369bb-279">Example: 72</span></span>

<span data-ttu-id="369bb-280">這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-280">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-281">**ScanMode**</span><span class="sxs-lookup"><span data-stu-id="369bb-281">**ScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-282">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="369bb-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-283">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-284">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Device0 \| DefaultSettings. 交錯" ) </span><span class="sxs-lookup"><span data-stu-id="369bb-284">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Device0\|DefaultSettings.Interlaced")</span></span>
</dt> </dl>

<span data-ttu-id="369bb-285">指出顯示裝置是否為交錯式。</span><span class="sxs-lookup"><span data-stu-id="369bb-285">Indicates whether the display device is interlaced.</span></span>

<span data-ttu-id="369bb-286">這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-286">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

<dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="369bb-287">**非交錯** 式 ( 「非交錯」 ) </span><span class="sxs-lookup"><span data-stu-id="369bb-287">**Non Interlaced** ("Non Interlaced")</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="369bb-288">**交錯** 式 ( 「交錯」 ) </span><span class="sxs-lookup"><span data-stu-id="369bb-288">**Interlaced** ("Interlaced")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="369bb-289">**ScreenHeight**</span><span class="sxs-lookup"><span data-stu-id="369bb-289">**ScreenHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-290">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="369bb-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-291">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-292">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VERTSIZE" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "毫米" ) </span><span class="sxs-lookup"><span data-stu-id="369bb-292">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|VERTSIZE"), [**Units**](../wmisdk/standard-qualifiers.md) ("millimeters")</span></span>
</dt> </dl>

<span data-ttu-id="369bb-293">指定實體畫面的高度。</span><span class="sxs-lookup"><span data-stu-id="369bb-293">Specifies the height of the physical screen.</span></span>

<span data-ttu-id="369bb-294">這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-294">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-295">**ScreenWidth**</span><span class="sxs-lookup"><span data-stu-id="369bb-295">**ScreenWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-296">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="369bb-296">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-297">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-298">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| HORZSIZE" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "毫米" ) </span><span class="sxs-lookup"><span data-stu-id="369bb-298">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|HORZSIZE"), [**Units**](../wmisdk/standard-qualifiers.md) ("millimeters")</span></span>
</dt> </dl>

<span data-ttu-id="369bb-299">指定實體畫面的寬度。</span><span class="sxs-lookup"><span data-stu-id="369bb-299">Specifies the width of the physical screen.</span></span>

<span data-ttu-id="369bb-300">這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-300">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-301">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="369bb-301">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-302">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="369bb-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-303">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-304">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="369bb-304">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="369bb-305">已知目前物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="369bb-305">Identifier by which the current object is known.</span></span>

<span data-ttu-id="369bb-306">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="369bb-306">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-307">**SystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="369bb-307">**SystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-308">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="369bb-308">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-309">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-310">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| SIZEPALETTE" ) </span><span class="sxs-lookup"><span data-stu-id="369bb-310">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|SIZEPALETTE")</span></span>
</dt> </dl>

<span data-ttu-id="369bb-311">表示保留給系統使用的目前色彩索引項目數目。</span><span class="sxs-lookup"><span data-stu-id="369bb-311">Iindicates the current number of color index entries reserved for system use.</span></span> <span data-ttu-id="369bb-312">此值僅適用于使用索引調色板的顯示設定。</span><span class="sxs-lookup"><span data-stu-id="369bb-312">This value is only valid for display settings that use an indexed palette .</span></span> <span data-ttu-id="369bb-313">索引的調色板不會用於每圖元8位以上的色彩深度。</span><span class="sxs-lookup"><span data-stu-id="369bb-313">Indexed palettes are not used for color depths greater than 8 bits per pixel.</span></span> <span data-ttu-id="369bb-314">如果色彩深度超過每圖元8位，此值會設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="369bb-314">If the color depth is more than 8 bits per pixel, this value is set to **NULL**.</span></span>

<span data-ttu-id="369bb-315">範例：20</span><span class="sxs-lookup"><span data-stu-id="369bb-315">Example: 20</span></span>

<span data-ttu-id="369bb-316">這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-316">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="369bb-317">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="369bb-317">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369bb-318">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="369bb-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="369bb-319">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="369bb-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369bb-320">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VERTRES" ) </span><span class="sxs-lookup"><span data-stu-id="369bb-320">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|VERTRES")</span></span>
</dt> </dl>

<span data-ttu-id="369bb-321">指出垂直方向中目前的圖元數目 (Y 軸的顯示) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-321">Indicates the current number of pixels in the vertical direction (Y axis) of the display.</span></span>

<span data-ttu-id="369bb-322">範例：768</span><span class="sxs-lookup"><span data-stu-id="369bb-322">Example: 768</span></span>

<span data-ttu-id="369bb-323">這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。</span><span class="sxs-lookup"><span data-stu-id="369bb-323">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="369bb-324">規格需求</span><span class="sxs-lookup"><span data-stu-id="369bb-324">Requirements</span></span>



| <span data-ttu-id="369bb-325">需求</span><span class="sxs-lookup"><span data-stu-id="369bb-325">Requirement</span></span> | <span data-ttu-id="369bb-326">值</span><span class="sxs-lookup"><span data-stu-id="369bb-326">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="369bb-327">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="369bb-327">Minimum supported client</span></span><br/> | <span data-ttu-id="369bb-328">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="369bb-328">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="369bb-329">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="369bb-329">Minimum supported server</span></span><br/> | <span data-ttu-id="369bb-330">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="369bb-330">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="369bb-331">命名空間</span><span class="sxs-lookup"><span data-stu-id="369bb-331">Namespace</span></span><br/>                | <span data-ttu-id="369bb-332">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="369bb-332">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="369bb-333">MOF</span><span class="sxs-lookup"><span data-stu-id="369bb-333">MOF</span></span><br/>                      | <dl> <span data-ttu-id="369bb-334"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="369bb-334"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="369bb-335">DLL</span><span class="sxs-lookup"><span data-stu-id="369bb-335">DLL</span></span><br/>                      | <dl> <span data-ttu-id="369bb-336"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="369bb-336"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="369bb-337">另請參閱</span><span class="sxs-lookup"><span data-stu-id="369bb-337">See also</span></span>

<dl> <dt>

[<span data-ttu-id="369bb-338">**CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="369bb-338">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> </dl>

 

 
